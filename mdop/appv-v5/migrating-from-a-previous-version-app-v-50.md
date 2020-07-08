---
title: Migration à partir d'une version précédente
description: Migration à partir d'une version précédente
author: dansimp
ms.assetid: a13cd353-b22a-48f7-af1e-5d54ede2a7e5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a05bbd498cdb77a1ddf694b1aab6aeb42124775b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805065"
---
# Migration à partir d'une version précédente


Avec App-V 5,0, vous pouvez migrer votre infrastructure App-V 4,6 existante vers une infrastructure plus flexible, intégrée et plus facile à 5,0 gérer.

Tenez compte des sections suivantes lors de la planification de votre stratégie de migration:

**Remarques**  Pour plus d’informations sur les différences entre App-V 4,6 et App-V 5,0, voir **différences entre les sections App-v 4,6 et App-v 5,0** de l' [application-v 5,0](about-app-v-50.md).

 

## Conversion de packages créés à l’aide d’une version antérieure d’App-V


Utilisez l’utilitaire convertisseur de package pour mettre à niveau des packages d’applications virtuelles créés à l’aide de versions précédentes d’App-V. Le convertisseur de package utilise PowerShell pour convertir des packages et peut faciliter l’automatisation du processus si vous avez de nombreux packages qui nécessitent une conversion.

**Important**  Après avoir converti un package existant, vous devez tester le package avant de déployer le package pour vérifier que le processus de conversion a abouti.

 

**Ce que vous devez savoir avant de convertir des packages existants**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Problème</th>
<th align="left">Solution de contournement</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Les scripts de package ne sont pas convertis.</p></td>
<td align="left"><p>Testez le package converti. Le cas échéant, convertissez le script.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Les substitutions de paramètre de registre de package ne sont pas converties.</p></td>
<td align="left"><p>Testez le package converti. Le cas échéant, rajoutez les remplacements du Registre.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Les packages virtuels utilisant DSC ne sont pas liés après la conversion.</p></td>
<td align="left"><p>Liez les packages à l’aide de groupes de connexion. Voir <a href="managing-connection-groups.md" data-raw-source="[Managing Connection Groups](managing-connection-groups.md)"> gestion des groupes de connexion </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Des conflits de variables d’environnement sont détectés lors de la conversion.</p></td>
<td align="left"><p>Résoudre les conflits dans le <strong> fichier. OSD associé </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Les chemins d’accès codés en dur sont détectés lors de la conversion.</p></td>
<td align="left"><p>Les chemins d’accès codés en dur sont difficiles à convertir correctement. Le convertisseur de package détectera et renverra des packages avec des fichiers contenant des chemins d’accès codés en dur. Affichez le fichier avec le chemin codé en dur et déterminez s’il nécessite le fichier. Si tel est le cas, nous vous recommandons de réorganiser le package.</p></td>
</tr>
</tbody>
</table>

 

Lors de la conversion d’un package Vérifiez l’absence de raccourcis vers les fichiers ou les raccourcis. Recherchez l’élément dans le package App-V 4,6. Il peut s’agir d’un chemin d’accès codé en dur. Convertissez le chemin d’accès.

**Remarques**  Nous vous recommandons d’utiliser le Sequencer App-V 5,0 pour convertir des applications ou applications critiques qui doivent tirer parti de fonctionnalités. Pour plus d' [informations sur la façon de séquencer une nouvelle application avec App-V 5,0](how-to-sequence-a-new-application-with-app-v-50-beta-gb18030.md), voir.

Si un package converti ne s’ouvre pas après l’avoir converti, il est également recommandé de réorganiser l’application à l’aide du séquenceur App-V 5,0.

 

[Comment convertir un package créé dans une version précédente d'App-V](how-to-convert-a-package-created-in-a-previous-version-of-app-v.md)

## Migration des clients


Le tableau suivant présente la méthode recommandée pour la mise à niveau des clients.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tâche</th>
<th align="left">Plus d’informations</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Mettre à niveau votre environnement vers App-V 4.6 SP2</p></td>
<td align="left"><p><a href="../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md" data-raw-source="[Application Virtualization Deployment and Upgrade Considerations](../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md)">Considérations en matière de déploiement et de mise à niveau de la virtualisation des applications </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Installez le client App-V 5,0 avec la coexistence activée.</p></td>
<td align="left"><p><a href="how-to-deploy-the-app-v-46-and-the-app-v--50-client-on-the-same-computer.md" data-raw-source="[How to Deploy the App-V 4.6 and the App-V 5.0 Client on the Same Computer](how-to-deploy-the-app-v-46-and-the-app-v--50-client-on-the-same-computer.md)">Déploiement de l’application-V 4,6 et du client App-V 5,0 sur le même ordinateur </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Séquence et déploiement des packages App-V 5,0. Le cas échéant, annulez la publication des packages App-V 4,6.</p></td>
<td align="left"><p><a href="how-to-sequence-a-new-application-with-app-v-50-beta-gb18030.md" data-raw-source="[How to Sequence a New Application with App-V 5.0](how-to-sequence-a-new-application-with-app-v-50-beta-gb18030.md)">Comment séquencer une nouvelle application avec App-V 5,0 </a> .</p></td>
</tr>
</tbody>
</table>

 

**Important**  Vous devez exécuter App-V 4.6 SP3 pour utiliser le mode de coexistence. Par ailleurs, lorsque vous séquencez un package, vous devez configurer le paramètre administration de l’autorité, qui se trouve dans la **Configuration utilisateur** , dans la section Configuration de l' **utilisateur** .

 

## Migration de l’infrastructure complète de l’application-V 5,0 Server


Il n’existe aucune méthode directe pour effectuer une mise à niveau vers une infrastructure App-V 5,0 complète. Pour plus d’informations sur la mise à niveau de l’application-V Server, utilisez les informations de la section suivante.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tâche</th>
<th align="left">Plus d’informations</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Mettez à niveau votre environnement vers App-V 4.6 SP3.</p></td>
<td align="left"><p><a href="../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md" data-raw-source="[Application Virtualization Deployment and Upgrade Considerations](../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md)">Considérations en matière de déploiement et de mise à niveau de la virtualisation des applications </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Déploiement de la version 5,0 App-V du client.</p></td>
<td align="left"><p><a href="how-to-deploy-the-app-v-client-gb18030.md" data-raw-source="[How to Deploy the App-V Client](how-to-deploy-the-app-v-client-gb18030.md)">Déploiement du client App-V </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Installez App-V 5,0 Server.</p></td>
<td align="left"><p><a href="how-to-deploy-the-app-v-50-server-50sp3.md" data-raw-source="[How to Deploy the App-V 5.0 Server](how-to-deploy-the-app-v-50-server-50sp3.md)">Déploiement du serveur App-V 5,0 </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Migrer des packages existants.</p></td>
<td align="left"><p>Voir les <strong> packages de conversion créés à l’aide d’une version antérieure de la section App-V </strong> de cet article.</p></td>
</tr>
</tbody>
</table>

 

## Tâches de migration supplémentaires


Vous pouvez également effectuer d’autres tâches de migration telles que la reconfiguration des points de terminaison et l’ouverture d’un package créé à l’aide d’une version antérieure sur un ordinateur exécutant le client App-V 5,0. Les liens suivants fournissent des informations supplémentaires sur l’exécution de ces tâches.

[Migration de points d'extension d'un package App-V4.6 vers un package App-V5.0 converti pour tous les utilisateurs sur un ordinateur spécifique](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-50-package-for-all-users-on-a-specific-computer.md)

[Migration de points d'extension d'un package App-V4.6 vers un package App-V5.0 pour un utilisateur spécifique](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-50-for-a-specific-user.md)

[Restauration de points d'extension d'un package App-V5.0 vers un package App-V4.6 pour tous les utilisateurs sur un ordinateur spécifique](how-to-revert-extension-points-from-an-app-v-50-package-to-an-app-v-46-package-for-all-users-on-a-specific-computer.md)

[Restauration de points d'extension d'un package App-V5.0 vers un package App-V4.6 pour un utilisateur spécifique](how-to-revert-extension-points-from-an-app-v-50-package-to-an-app-v-46-package-for-a-specific-user.md)







## Autres ressources pour effectuer des tâches de migration d’application-V


[Opérations d'App-V5.0](operations-for-app-v-50.md)

[Procédure de mise à niveau du serveur de gestion Microsoft App-V 5,1 simplifiée](https://go.microsoft.com/fwlink/p/?LinkId=786330)

 

 





