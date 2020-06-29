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
# Liste de contrôle pour la post-installation d'App-V


La liste de vérification suivante fournit une liste générale des éléments à prendre en considération et vous explique les étapes à suivre une fois que vous avez terminé l’installation de Microsoft Application Virtualization (App-V) Server, serveur de diffusion en continu (App-v) et client de bureau App-V.

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
<td align="left"><p>Créer des exceptions de pare-feu pour le serveur de gestion des applications ou les services de serveur de diffusion.</p></td>
<td align="left"><p><a href="configuring-the-firewall-for-the-app-v-servers.md" data-raw-source="[Configuring the Firewall for the App-V Servers](configuring-the-firewall-for-the-app-v-servers.md)">Configuration du pare-feu pour les serveurs App-V Server</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Assurez-vous que le système App-V fonctionne correctement en publiant, en continuant et en testant l’application par défaut.</p></td>
<td align="left"><p><a href="how-to-install-and-configure-the-default-application.md" data-raw-source="[How to Install and Configure the Default Application](how-to-install-and-configure-the-default-application.md)">Procédure pour installer et configurer l'application par défaut</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Configurez le client App-V de façon à utiliser le serveur de streaming App-V ou un autre serveur pour le streaming au moyen des <strong> </strong> paramètres APPLICATIONSOURCEROOT, <strong> IconSourceRoot </strong> et <strong> OSDSourceRoot </strong> .</p></td>
<td align="left"><p><a href="how-to-configure-the-client-for-application-package-retrieval.md" data-raw-source="[How to Configure the Client for Application Package Retrieval](how-to-configure-the-client-for-application-package-retrieval.md)">Procédure pour configurer le client afin d'extraire le package d'application</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Découvrez comment utiliser la version de fichier. msi des packages d’application séquencés pour le déploiement hors connexion.</p></td>
<td align="left"><p><a href="how-to-publish-a-virtual-application-on-the-client.md" data-raw-source="[How to Publish a Virtual Application on the Client](how-to-publish-a-virtual-application-on-the-client.md)">Procédure pour publier une application virtuelle sur le client</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Facultatif Configurez la mise en miroir de base de données SQL Server pour la base de données App-V.</p></td>
<td align="left"><p><a href="how-to-configure-microsoft-sql-server-mirroring-support-for-app-v.md" data-raw-source="[How to Configure Microsoft SQL Server Mirroring Support for App-V](how-to-configure-microsoft-sql-server-mirroring-support-for-app-v.md)">Procédure pour configurer la prise en charge de la mise en miroir de Microsoft SQL Server pour App-V</a></p></td>
</tr>
</tbody>
</table>

 

## Rubriques connexes


[Listes de contrôle pour le déploiement et la mise à niveau d'Application Virtualization](application-virtualization-deployment-and-upgrade-checklists.md)

 

 





