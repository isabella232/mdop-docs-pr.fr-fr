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
# Liste de contrôle pour la pré-installation d'App-V


La liste de contrôle suivante est destinée à fournir une liste générale des éléments à prendre en considération et à définir les étapes à suivre avant d’installer les serveurs Microsoft Application Virtualization (App-V).

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Étape</th>
<th align="left">Référence</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Assurez-vous que votre environnement informatique satisfait aux configurations prises en charge pour App-V.</p></td>
<td align="left"><p><a href="application-virtualization-deployment-requirements.md" data-raw-source="[Application Virtualization Deployment Requirements](application-virtualization-deployment-requirements.md)">Configuration requise pour le déploiement d'Application Virtualization</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Configurez les comptes et groupes Active Directory nécessaires.</p></td>
<td align="left"><p><a href="configuring-prerequisite-groups-in-active-directory-for-app-v.md" data-raw-source="[Configuring Prerequisite Groups in Active Directory for App-V](configuring-prerequisite-groups-in-active-directory-for-app-v.md)">Configuration des groupes prérequis dans Active Directory pour App-V</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Configurez les paramètres des services Internet (IIS) sur le serveur exécutant IIS.</p></td>
<td align="left"><p><a href="how-to-configure-windows-server-2008-for-app-v-management-servers.md" data-raw-source="[How to Configure Windows Server 2008 for App-V Management Servers](how-to-configure-windows-server-2008-for-app-v-management-servers.md)">Procédure pour configurer les serveurs Windows Server2008 pour App-V Management Server</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Configurez le serveur qui exécute IIS pour être approuvé pour la délégation.</p>
<div class="alert">
<strong>Remarque</strong><br/><p>Cela est requis uniquement si vous installez le serveur de gestion des applications-V à l’aide d’une architecture de système distribuée, c’est-à-dire si vous installez la console de gestion des applications-V, le service Web de gestion et la base de données sur des ordinateurs différents.</p>
</div>
<div>

</div></td>
<td align="left"><p><a href="how-to-configure-the-server-to-be-trusted-for-delegation.md" data-raw-source="[How to Configure the Server to be Trusted for Delegation](how-to-configure-the-server-to-be-trusted-for-delegation.md)">Procédure pour configurer le serveur afin qu'il soit approuvé pour délégation</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Installez Microsoft SQL Server 2008.</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=181924" data-raw-source="[Install SQL Server 2008](https://go.microsoft.com/fwlink/?LinkId=181924)">Installez SQL Server 2008 </a> ( <a href="https://go.microsoft.com/fwlink/?LinkId=181924" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=181924"> https://go.microsoft.com/fwlink/?LinkId=181924 </a> ).</p></td>
</tr>
</tbody>
</table>



## Rubriques connexes


[Listes de contrôle pour le déploiement et la mise à niveau d'Application Virtualization](application-virtualization-deployment-and-upgrade-checklists.md)

[Liste de contrôle pour l'installation d'App-V](app-v-installation-checklist.md)









