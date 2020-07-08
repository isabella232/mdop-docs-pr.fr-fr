---
title: Planification du déploiement du serveur App-V5.0
description: Planification du déploiement du serveur App-V5.0
author: dansimp
ms.assetid: fd89b324-3961-471a-ad90-c8f9ae7a8155
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 06c7c17fd081b89337bbecd31f20f6796338f697
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804992"
---
# Planification du déploiement du serveur App-V5.0


L’infrastructure de serveur Microsoft Application Virtualization (App-V) 5,0 inclut un ensemble de fonctionnalités spécialisées qui peuvent être installées sur un ou plusieurs ordinateurs serveur, en fonction des besoins de l’entreprise.

## Planification du déploiement de l’application-V 5,0 Server


Le serveur App-V 5,0 comprend les fonctionnalités suivantes:

-   Serveur de gestion: fournit une fonctionnalité de gestion générale de l’infrastructure App-V 5,0.

-   Base de données de gestion: facilite le déploiement de base de données pour la gestion d’App-V 5,0.

-   Serveur de publication: fournit des fonctionnalités d’hébergement et de streaming pour les applications virtuelles.

-   Serveur de création de rapports-fournit une application-V 5,0 Reporting Services.

-   Base de données de création de rapports: facilite les déploiements de base de données pour la création de rapports App-V 5,0.

La liste suivante présente les méthodes recommandées pour l’installation de l’infrastructure du serveur App-V 5,0:

-   Installez le serveur App-V 5,0. Pour plus d’informations, reportez-vous à la rubrique [déploiement du serveur App-V 5,0](how-to-deploy-the-app-v-50-server-50sp3.md).

-   Installez les fonctionnalités de base de données, de création de rapports et de gestion sur des ordinateurs séparés. Pour plus d’informations, reportez-vous à la rubrique [Comment installer les bases de données de gestion et de création de rapports sur des ordinateurs séparés à partir de Management et Reporting Services](how-to-install-the-management-and-reporting-databases-on-separate-computers-from-the-management-and-reporting-services.md).

-   Utiliser la distribution de logiciels électroniques. Pour plus d’informations, reportez-vous [à la rubrique déploiement de packages App-V 5,0 à l’aide de la distribution de logiciels électroniques](how-to-deploy-app-v-50-packages-using-electronic-software-distribution.md).

-   Installez toutes les fonctionnalités du serveur sur un seul ordinateur.

## <a href="" id="---------app-v-5-0-server-interaction"></a> Interaction App-V 5,0 Server


Cette section contient des informations sur la façon dont les différents rôles de serveur App-V 5,0 interagissent entre eux.

Le serveur de gestion App-V 5,0 contient le référentiel des packages et leurs configurations affectées. Pour les serveurs de publication qui sont inscrits auprès du serveur de gestion, les métadonnées associées sont fournies aux serveurs de publication pour une utilisation lors de la publication de demandes d’actualisation d’ordinateurs exécutant le client App-V 5,0. Les serveurs de publication App-V 5,0 gérés par un serveur de gestion unique peuvent utiliser différents clients et peuvent avoir des noms de site Web et des liaisons de port différents. De plus, tous les serveurs de publication gérés par le même serveur de gestion sont répliques les uns des autres.

**Remarques**  Le serveur de gestion n’effectue aucun équilibrage de charge. Les métadonnées associées sont simplement transmises au serveur de publication pour être utilisées lors du traitement des requêtes client.

 

## Protocoles liés au serveur et fonctionnalités externes


L’exemple suivant affiche des informations sur les protocoles liés au serveur utilisés par les serveurs App-V 5,0. La table inclut également le mécanisme de création de rapports pour chaque type de serveur.

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Type de serveur</th>
<th align="left">Protocoles</th>
<th align="left">Fonctionnalités externes nécessaires</th>
<th align="left">Rapports</th>
<th align="left"></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Serveur IIS</p></td>
<td align="left"><p>HTTP</p>
<p>HTTPS</p></td>
<td align="left"><p>Cette combinaison de protocoles serveur nécessite un mécanisme de synchronisation du contenu entre le serveur de gestion et le serveur de diffusion en continu. Dans le cadre de l’utilisation de HTTP ou HTTPs, utilisez un serveur IIS et un pare-feu pour protéger votre serveur contre son exposition à Internet.</p></td>
<td align="left"><p>Interne</p></td>
<td align="left"></td>
</tr>
<tr class="even">
<td align="left"><p>Fichier</p></td>
<td align="left"><p>SMB</p></td>
<td align="left"><p>Cette combinaison de protocoles serveur nécessite une prise en charge de la synchronisation du contenu entre le serveur de gestion et le serveur de diffusion en continu. Utiliser un ordinateur client avec la fonctionnalité de partage de fichiers ou de flux.</p></td>
<td align="left"><p>Interne</p></td>
<td align="left"></td>
</tr>
</tbody>
</table>

 






## Rubriques connexes


[Envisager de déployer App-V](planning-to-deploy-app-v.md)

[Déploiement du serveur App-V5.0](deploying-the-app-v-50-server.md)

 

 





