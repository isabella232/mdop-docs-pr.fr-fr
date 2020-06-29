---
title: Liste de contrôle pour la pré-installation d'App-V
description: Liste de contrôle pour la pré-installation d'App-V
author: dansimp
ms.assetid: 3af609b1-2c09-4edb-b083-b913b6d5e8c4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 70e71d3dea02daeadedb4cff78c58302ac743dda
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808046"
---
# <span data-ttu-id="90893-103">Liste de contrôle pour la pré-installation d'App-V</span><span class="sxs-lookup"><span data-stu-id="90893-103">App-V Pre-Installation Checklist</span></span>


<span data-ttu-id="90893-104">La liste de contrôle suivante est destinée à fournir une liste générale des éléments à prendre en considération et à définir les étapes à suivre avant d’installer les serveurs Microsoft Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="90893-104">The following checklist is intended to provide a high-level list of items to consider and outlines the steps you should take before you install the Microsoft Application Virtualization (App-V) servers.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="90893-105">Étape</span><span class="sxs-lookup"><span data-stu-id="90893-105">Step</span></span></th>
<th align="left"><span data-ttu-id="90893-106">Référence</span><span class="sxs-lookup"><span data-stu-id="90893-106">Reference</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="90893-107">Assurez-vous que votre environnement informatique satisfait aux configurations prises en charge pour App-V.</span><span class="sxs-lookup"><span data-stu-id="90893-107">Ensure your computing environment meets the supported configurations required for App-V.</span></span></p></td>
<td align="left"><p><a href="application-virtualization-deployment-requirements.md" data-raw-source="[Application Virtualization Deployment Requirements](application-virtualization-deployment-requirements.md)"><span data-ttu-id="90893-108">Configuration requise pour le déploiement d'Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="90893-108">Application Virtualization Deployment Requirements</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="90893-109">Configurez les comptes et groupes Active Directory nécessaires.</span><span class="sxs-lookup"><span data-stu-id="90893-109">Configure the necessary Active Directory groups and accounts.</span></span></p></td>
<td align="left"><p><a href="configuring-prerequisite-groups-in-active-directory-for-app-v.md" data-raw-source="[Configuring Prerequisite Groups in Active Directory for App-V](configuring-prerequisite-groups-in-active-directory-for-app-v.md)"><span data-ttu-id="90893-110">Configuration des groupes prérequis dans Active Directory pour App-V</span><span class="sxs-lookup"><span data-stu-id="90893-110">Configuring Prerequisite Groups in Active Directory for App-V</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="90893-111">Configurez les paramètres des services Internet (IIS) sur le serveur exécutant IIS.</span><span class="sxs-lookup"><span data-stu-id="90893-111">Configure the Internet Information Services (IIS) settings on the server that is running IIS.</span></span></p></td>
<td align="left"><p><a href="how-to-configure-windows-server-2008-for-app-v-management-servers.md" data-raw-source="[How to Configure Windows Server 2008 for App-V Management Servers](how-to-configure-windows-server-2008-for-app-v-management-servers.md)"><span data-ttu-id="90893-112">Procédure pour configurer les serveurs Windows Server2008 pour App-V Management Server</span><span class="sxs-lookup"><span data-stu-id="90893-112">How to Configure Windows Server 2008 for App-V Management Servers</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="90893-113">Configurez le serveur qui exécute IIS pour être approuvé pour la délégation.</span><span class="sxs-lookup"><span data-stu-id="90893-113">Configure the server that is running IIS to be trusted for delegation.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="90893-114">Remarque</span><span class="sxs-lookup"><span data-stu-id="90893-114">Note</span></span></strong><br/><p><span data-ttu-id="90893-115">Cela est requis uniquement si vous installez le serveur de gestion des applications-V à l’aide d’une architecture de système distribuée, c’est-à-dire si vous installez la console de gestion des applications-V, le service Web de gestion et la base de données sur des ordinateurs différents.</span><span class="sxs-lookup"><span data-stu-id="90893-115">This is required only if you are installing the App-V Management Server by using a distributed system architecture, that is, if you install the App-V Management Console, the Management Web Service, and the database on different computers.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><a href="how-to-configure-the-server-to-be-trusted-for-delegation.md" data-raw-source="[How to Configure the Server to be Trusted for Delegation](how-to-configure-the-server-to-be-trusted-for-delegation.md)"><span data-ttu-id="90893-116">Procédure pour configurer le serveur afin qu'il soit approuvé pour délégation</span><span class="sxs-lookup"><span data-stu-id="90893-116">How to Configure the Server to be Trusted for Delegation</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="90893-117">Installez Microsoft SQL Server 2008.</span><span class="sxs-lookup"><span data-stu-id="90893-117">Install Microsoft SQL Server 2008.</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=181924" data-raw-source="[Install SQL Server 2008](https://go.microsoft.com/fwlink/?LinkId=181924)"><span data-ttu-id="90893-118">Installez SQL Server 2008 </a> ( <a href="https://go.microsoft.com/fwlink/?LinkId=181924" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=181924"> https://go.microsoft.com/fwlink/?LinkId=181924 </a> ).</span><span class="sxs-lookup"><span data-stu-id="90893-118">Install SQL Server 2008</a> (<a href="https://go.microsoft.com/fwlink/?LinkId=181924" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=181924">https://go.microsoft.com/fwlink/?LinkId=181924</a>).</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="90893-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="90893-119">Related topics</span></span>


[<span data-ttu-id="90893-120">Listes de contrôle pour le déploiement et la mise à niveau d'Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="90893-120">Application Virtualization Deployment and Upgrade Checklists</span></span>](application-virtualization-deployment-and-upgrade-checklists.md)

[<span data-ttu-id="90893-121">Liste de contrôle pour l'installation d'App-V</span><span class="sxs-lookup"><span data-stu-id="90893-121">App-V Installation Checklist</span></span>](app-v-installation-checklist.md)









