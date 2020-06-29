---
title: Liste de contrôle pour la post-installation d'App-V
description: Liste de contrôle pour la post-installation d'App-V
author: dansimp
ms.assetid: 74db297e-a744-4287-bcc6-0e096ca8b57a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 79728bd2043076b20eb37ba0b1fa6f834a0d94bf
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808053"
---
# <span data-ttu-id="f4530-103">Liste de contrôle pour la post-installation d'App-V</span><span class="sxs-lookup"><span data-stu-id="f4530-103">App-V Postinstallation Checklist</span></span>


<span data-ttu-id="f4530-104">La liste de vérification suivante fournit une liste générale des éléments à prendre en considération et vous explique les étapes à suivre une fois que vous avez terminé l’installation de Microsoft Application Virtualization (App-V) Server, serveur de diffusion en continu (App-v) et client de bureau App-V.</span><span class="sxs-lookup"><span data-stu-id="f4530-104">The following checklist provides a high-level list of items to consider and outlines the steps you should take after you have completed the installation of the Microsoft Application Virtualization (App-V) Management Server, App-V Streaming Server, and the App-V Desktop Client.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f4530-105">Étape</span><span class="sxs-lookup"><span data-stu-id="f4530-105">Step</span></span></th>
<th align="left"><span data-ttu-id="f4530-106">Référence</span><span class="sxs-lookup"><span data-stu-id="f4530-106">Reference</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f4530-107">Créer des exceptions de pare-feu pour le serveur de gestion des applications ou les services de serveur de diffusion.</span><span class="sxs-lookup"><span data-stu-id="f4530-107">Create firewall exceptions for the App-V Management Server or Streaming Server services.</span></span></p></td>
<td align="left"><p><a href="configuring-the-firewall-for-the-app-v-servers.md" data-raw-source="[Configuring the Firewall for the App-V Servers](configuring-the-firewall-for-the-app-v-servers.md)"><span data-ttu-id="f4530-108">Configuration du pare-feu pour les serveurs App-V Server</span><span class="sxs-lookup"><span data-stu-id="f4530-108">Configuring the Firewall for the App-V Servers</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f4530-109">Assurez-vous que le système App-V fonctionne correctement en publiant, en continuant et en testant l’application par défaut.</span><span class="sxs-lookup"><span data-stu-id="f4530-109">Verify that the App-V system is functioning correctly by publishing, streaming, and testing the default application.</span></span></p></td>
<td align="left"><p><a href="how-to-install-and-configure-the-default-application.md" data-raw-source="[How to Install and Configure the Default Application](how-to-install-and-configure-the-default-application.md)"><span data-ttu-id="f4530-110">Procédure pour installer et configurer l'application par défaut</span><span class="sxs-lookup"><span data-stu-id="f4530-110">How to Install and Configure the Default Application</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f4530-111">Configurez le client App-V de façon à utiliser le serveur de streaming App-V ou un autre serveur pour le streaming au moyen des <strong> </strong> paramètres APPLICATIONSOURCEROOT, <strong> IconSourceRoot </strong> et <strong> OSDSourceRoot </strong> .</span><span class="sxs-lookup"><span data-stu-id="f4530-111">Configure the App-V Client to use the App-V Streaming Server or other server for streaming by means of the <strong>ApplicationSourceRoot</strong>, <strong>IconSourceRoot</strong>, and <strong>OSDSourceRoot</strong> settings.</span></span></p></td>
<td align="left"><p><a href="how-to-configure-the-client-for-application-package-retrieval.md" data-raw-source="[How to Configure the Client for Application Package Retrieval](how-to-configure-the-client-for-application-package-retrieval.md)"><span data-ttu-id="f4530-112">Procédure pour configurer le client afin d'extraire le package d'application</span><span class="sxs-lookup"><span data-stu-id="f4530-112">How to Configure the Client for Application Package Retrieval</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f4530-113">Découvrez comment utiliser la version de fichier. msi des packages d’application séquencés pour le déploiement hors connexion.</span><span class="sxs-lookup"><span data-stu-id="f4530-113">Understand how to use the .msi file version of sequenced application packages for offline deployment.</span></span></p></td>
<td align="left"><p><a href="how-to-publish-a-virtual-application-on-the-client.md" data-raw-source="[How to Publish a Virtual Application on the Client](how-to-publish-a-virtual-application-on-the-client.md)"><span data-ttu-id="f4530-114">Procédure pour publier une application virtuelle sur le client</span><span class="sxs-lookup"><span data-stu-id="f4530-114">How to Publish a Virtual Application on the Client</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f4530-115">Facultatif Configurez la mise en miroir de base de données SQL Server pour la base de données App-V.</span><span class="sxs-lookup"><span data-stu-id="f4530-115">(Optional) Configure SQL Server database mirroring for the App-V database.</span></span></p></td>
<td align="left"><p><a href="how-to-configure-microsoft-sql-server-mirroring-support-for-app-v.md" data-raw-source="[How to Configure Microsoft SQL Server Mirroring Support for App-V](how-to-configure-microsoft-sql-server-mirroring-support-for-app-v.md)"><span data-ttu-id="f4530-116">Procédure pour configurer la prise en charge de la mise en miroir de Microsoft SQL Server pour App-V</span><span class="sxs-lookup"><span data-stu-id="f4530-116">How to Configure Microsoft SQL Server Mirroring Support for App-V</span></span></a></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="f4530-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f4530-117">Related topics</span></span>


[<span data-ttu-id="f4530-118">Listes de contrôle pour le déploiement et la mise à niveau d'Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="f4530-118">Application Virtualization Deployment and Upgrade Checklists</span></span>](application-virtualization-deployment-and-upgrade-checklists.md)

 

 





