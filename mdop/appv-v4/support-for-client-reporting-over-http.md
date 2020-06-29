---
title: Prise en charge de la création de rapports du client via HTTP
description: Prise en charge de la création de rapports du client via HTTP
author: dansimp
ms.assetid: 4a26ac80-1fb5-4c05-83de-4d06793f7bf2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 4e1759bb4df39ac403e2837c4083275a8b3436f5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806246"
---
# <span data-ttu-id="08359-103">Prise en charge de la création de rapports du client via HTTP</span><span class="sxs-lookup"><span data-stu-id="08359-103">Support for Client Reporting over HTTP</span></span>


<span data-ttu-id="08359-104">La version 4,6 du client App-V prend désormais en charge l’utilisation de la communication HTTP lors de l’envoi de données de rapport client vers le serveur de publication.</span><span class="sxs-lookup"><span data-stu-id="08359-104">Version 4.6 of the App-V client now supports the use of HTTP communication when sending client reporting data to the publishing server.</span></span> <span data-ttu-id="08359-105">Cette fonctionnalité prend en charge les scénarios dans lesquels un client a implémenté un serveur de publication HTTP (S) personnalisé configuré pour collecter et traiter les données client.</span><span class="sxs-lookup"><span data-stu-id="08359-105">This feature supports scenarios where a customer has implemented a custom HTTP(S) publishing server that is configured to collect and process client data.</span></span>

<span data-ttu-id="08359-106">Pour plus d’informations sur les serveurs de publication HTTP, voir</span><span class="sxs-lookup"><span data-stu-id="08359-106">For more information on HTTP publishing servers, see</span></span> <https://go.microsoft.com/fwlink/?LinkId=157426>

## <span data-ttu-id="08359-107">Rapport client sur HTTP</span><span class="sxs-lookup"><span data-stu-id="08359-107">Client Reporting over HTTP</span></span>


<span data-ttu-id="08359-108">Le client démarre la collecte des données lors de la réception d’un attribut «report =» TRUE» dans le code XML de réponse d’actualisation de publication du serveur de publication.</span><span class="sxs-lookup"><span data-stu-id="08359-108">The client starts collecting data when it receives a “REPORTING=”TRUE””attribute in the publishing refresh response XML from the publishing server.</span></span> <span data-ttu-id="08359-109">Lorsque cet attribut est reçu, le client envoie toutes les données cumulées au serveur de publication qui a envoyé l’actualisation de la publication.</span><span class="sxs-lookup"><span data-stu-id="08359-109">When this attribute is received, the client sends any accumulated data to the publishing server that sent the publishing refresh.</span></span> <span data-ttu-id="08359-110">Les détails de ce processus sont les suivants:</span><span class="sxs-lookup"><span data-stu-id="08359-110">The details of this process are as follows:</span></span>

-   <span data-ttu-id="08359-111">Le client envoie une requête GET HTTP au serveur de publication pour une actualisation de publication.</span><span class="sxs-lookup"><span data-stu-id="08359-111">The client sends an HTTP GET request to the publishing server for a publishing refresh.</span></span> <span data-ttu-id="08359-112">L’en-tête de ce message contient un en-tête personnalisé «AppV-op: Refresh» qu’utilise le serveur de publication personnalisé HTTP (S) pour identifier le type du message.</span><span class="sxs-lookup"><span data-stu-id="08359-112">The header of this message contains an “AppV-Op:Refresh” custom header that the custom HTTP(S) publishing server uses to identify the message type.</span></span>

-   <span data-ttu-id="08359-113">Le serveur de publication envoie alors le code XML de réponse d’actualisation de publication contenant une valeur «rapport =» TRUE».</span><span class="sxs-lookup"><span data-stu-id="08359-113">The publishing server then sends the publishing refresh response XML that contains a “REPORTING=”TRUE”” value.</span></span>

-   <span data-ttu-id="08359-114">Le client envoie alors une requête HTTP POST au serveur de publication, ainsi que les données de rapport collectées depuis la dernière actualisation.</span><span class="sxs-lookup"><span data-stu-id="08359-114">The client then sends an HTTP POST request to the publishing server along with the reporting data that has been gathered since the previous refresh.</span></span> <span data-ttu-id="08359-115">L’en-tête de ce message contient un en-tête personnalisé «AppV-op: report» qu’utilise le serveur de publication personnalisé HTTP (S) pour identifier le type du message.</span><span class="sxs-lookup"><span data-stu-id="08359-115">The header of this message contains an “AppV-Op:Report” custom header that the custom HTTP(S) publishing server uses to identify the message type.</span></span>

<span data-ttu-id="08359-116">Le schéma suivant fournit des détails spécifiques du package et des données d’application qui sont envoyées au serveur.</span><span class="sxs-lookup"><span data-stu-id="08359-116">The following schema gives specific details of the package and the application data that is sent to the server.</span></span>

```xml
<?xml version="1.0"?>
<xs:schema xmlns:xs="http://www.w3.org/2001/XMLSchema">

    <xs:element name="CLIENT_DATA">
        <xs:complexType>
            <xs:all>
                <xs:element ref="PKG_LIST" minOccurs="1" maxOccurs="1"/>
                <xs:element ref="APP_RECORDS" minOccurs="1" maxOccurs="1"/>
            </xs:all>
            <!-- no regex for Ver because we want to allow tags like "Beta" -->
            <xs:attribute name="Ver" type="xs:normalizedString" use="required"/>
            <xs:attribute name="Host" type="xs:token" use="required"/>
            <xs:attribute name="CacheSize" type="xs:nonNegativeInteger" use="required"/>
            <xs:attribute name="CacheUsed" type="xs:nonNegativeInteger" use="required"/>
        </xs:complexType>
    </xs:element>

    <xs:element name="PKG_LIST">
        <xs:complexType>
            <xs:choice>
                <xs:element ref="PKG_DATA" minOccurs="0" maxOccurs="unbounded"/>
            </xs:choice>
        </xs:complexType>
    </xs:element>

    <xs:element name="PKG_DATA">
        <xs:complexType>
            <xs:attribute name="Name" type="xs:normalizedString" use="required"/>
            <xs:attribute name="Guid" type="xs:token" use="required"/>
            <xs:attribute name="Ver" type="xs:normalizedString" use="required"/>
            <xs:attribute name="VerGuid" type="xs:token" use="required"/>
            <xs:attribute name="Source" type="xs:normalizedString" use="required"/>
            <xs:attribute name="PctCached" use="required">
                <xs:simpleType>
                    <xs:restriction base="xs:nonNegativeInteger">
                        <xs:minInclusive value="0"/>
                        <xs:maxInclusive value="100"/>
                    </xs:restriction>
                </xs:simpleType>
            </xs:attribute>
        </xs:complexType>
    </xs:element>

    <xs:element name="APP_RECORDS">
         <xs:complexType>
            <xs:choice>
                <xs:element ref="APP_RECORD" minOccurs="0" maxOccurs="unbounded"/>
            </xs:choice>
        </xs:complexType>
   </xs:element>

    <xs:element name="APP_RECORD">
            <xs:attribute name="Name" type="xs:normalizedString" use="required"/>
            <xs:attribute name="Ver" type="xs:normalizedString" use="required"/>
            <xs:attribute name="Server" type="xs:normalizedString" use="required"/>
            <xs:attribute name="User" type="xs:normalizedString" use="required"/>
            <xs:attribute name="Launched" type="xs:dateTime" use="required"/>
            <xs:attribute name="Shutdown" type="xs:dateTime" use="optional"/>
    </xs:element>

</xs:schema>
```

 

 





