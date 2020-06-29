---
title: Procédure pour configurer le client pour la prise en charge du domaine MIT Kerberos
description: Procédure pour configurer le client pour la prise en charge du domaine MIT Kerberos
author: dansimp
ms.assetid: 46102f4c-270c-4115-8eb4-7ff5ae3be32d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ae5cd73d00f340bc50070fdd0a5fd3e038cc3789
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807257"
---
# <span data-ttu-id="83537-103">Procédure pour configurer le client pour la prise en charge du domaine MIT Kerberos</span><span class="sxs-lookup"><span data-stu-id="83537-103">How to Configure the Client for MIT Kerberos Realm Support</span></span>


<span data-ttu-id="83537-104">Dans Application Virtualization (App-V) 4,5 SP1, la prise en charge des domaines Kerberos MIT est ajoutée.</span><span class="sxs-lookup"><span data-stu-id="83537-104">In Application Virtualization (App-V) 4.5 SP1, support was added for MIT Kerberos realms.</span></span> <span data-ttu-id="83537-105">Cette rubrique fournit des informations détaillées sur l’activation de cette assistance.</span><span class="sxs-lookup"><span data-stu-id="83537-105">This topic provides detailed information on how to enable that support.</span></span>

**<span data-ttu-id="83537-106">Pour activer la prise en charge des domaines Kerberos MIT</span><span class="sxs-lookup"><span data-stu-id="83537-106">To enable support for MIT Kerberos Realms</span></span>**

-   <span data-ttu-id="83537-107">Créez une nouvelle clé de Registre nommée **UseMitKerberos** de type DWORD, comme suit, puis définissez-la sur la valeur 1.</span><span class="sxs-lookup"><span data-stu-id="83537-107">Create a new registry key named **UseMitKerberos** of type DWORD, as follows, and then set it to a value of 1.</span></span>

    <span data-ttu-id="83537-108">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\UseMitKerberos</span><span class="sxs-lookup"><span data-stu-id="83537-108">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\UseMitKerberos</span></span>

 

 





