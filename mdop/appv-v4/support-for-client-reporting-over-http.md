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
# Prise en charge de la création de rapports du client via HTTP


La version 4,6 du client App-V prend désormais en charge l’utilisation de la communication HTTP lors de l’envoi de données de rapport client vers le serveur de publication. Cette fonctionnalité prend en charge les scénarios dans lesquels un client a implémenté un serveur de publication HTTP (S) personnalisé configuré pour collecter et traiter les données client.

Pour plus d’informations sur les serveurs de publication HTTP, voir <https://go.microsoft.com/fwlink/?LinkId=157426>

## Rapport client sur HTTP


Le client démarre la collecte des données lors de la réception d’un attribut «report =» TRUE» dans le code XML de réponse d’actualisation de publication du serveur de publication. Lorsque cet attribut est reçu, le client envoie toutes les données cumulées au serveur de publication qui a envoyé l’actualisation de la publication. Les détails de ce processus sont les suivants:

-   Le client envoie une requête GET HTTP au serveur de publication pour une actualisation de publication. L’en-tête de ce message contient un en-tête personnalisé «AppV-op: Refresh» qu’utilise le serveur de publication personnalisé HTTP (S) pour identifier le type du message.

-   Le serveur de publication envoie alors le code XML de réponse d’actualisation de publication contenant une valeur «rapport =» TRUE».

-   Le client envoie alors une requête HTTP POST au serveur de publication, ainsi que les données de rapport collectées depuis la dernière actualisation. L’en-tête de ce message contient un en-tête personnalisé «AppV-op: report» qu’utilise le serveur de publication personnalisé HTTP (S) pour identifier le type du message.

Le schéma suivant fournit des détails spécifiques du package et des données d’application qui sont envoyées au serveur.

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

 

 





