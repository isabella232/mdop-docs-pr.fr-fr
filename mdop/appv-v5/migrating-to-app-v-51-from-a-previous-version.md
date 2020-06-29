---
title: Migration vers App-V5.1 à partir d'une version antérieure
description: Migration vers App-V5.1 à partir d'une version antérieure
author: dansimp
ms.assetid: e7ee0edc-7544-4c0a-aaca-d922a33bc1bb
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7fb6ddbfed4f6fd1ae9613d2ee86361a51918a65
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805064"
---
# Migration vers App-V5.1 à partir d'une version antérieure


La version 5,1 de Microsoft Application Virtualization (App-V) vous permet de migrer votre infrastructure App-v 4,6 ou App-V 5,0 vers une infrastructure plus flexible, intégrée et plus facile à 5,1 gérer.
Toutefois, vous ne pouvez pas effectuer de migration directe de App-V 4. x vers App-V 5,1, vous devez d’abord migrer vers App-V 5,0. Pour plus d’informations sur la migration de App-V 4. x vers App-V 5,0, voir [migration à partir d’une version précédente](migrating-from-a-previous-version-app-v-50.md)  

**Remarques**  Les packages App-V 5,1 sont exactement les mêmes que les packages App-V 5,0. Il n’y a aucune modification du format de package entre les versions et par conséquent, il est inutile de convertir les packages App-V 5,0 en packages App-V 5,1.

Pour plus d’informations sur les différences entre App-V 4,6 et App-V 5,1, voir **différences entre les sections App-v 4,6 et App-v 5,0** de l' [application-v 5,0](about-app-v-50.md).

 

## <a href="" id="bkmk-pkgconvimprove"></a>Améliorations apportées au convertisseur App-V 5,1 package


Vous pouvez désormais utiliser le convertisseur de package pour convertir les packages App-V 4,6 qui contiennent des scripts, et les informations de Registre et les scripts des fichiers source. OSD sont désormais inclus dans la sortie du convertisseur de package.

Vous pouvez également utiliser le `–OSDsToIncludeInPackage` paramètre avec l' `ConvertFrom-AppvLegacyPackage` applet de cmdlet pour spécifier les informations de fichiers. OSD qui sont converties et placées dans le nouveau package.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nouveauté de App-V 5,1</th>
<th align="left">Avant l’application-V 5,1</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Les nouveaux fichiers. XML sont créés correspondant aux fichiers. OSD associés à un package. ces fichiers incluent les informations suivantes:</p>
<ul>
<li><p>variables d’environnement</p></li>
<li><p>associés</p></li>
<li><p>associations de types de fichiers</p></li>
<li><p>informations de Registre</p></li>
<li><p>scripts</p></li>
</ul>
<p>Vous pouvez désormais choisir d’ajouter des informations à partir d’un sous-ensemble de fichiers. OSD du répertoire source au package à l’aide du <code>-OSDsToIncludeInPackage</code> paramètre.</p></td>
<td align="left"><p>Les informations et scripts du Registre inclus dans les fichiers. OSD associés à un package n’ont pas été inclus dans la sortie du convertisseur de package.</p>
<p>Le convertisseur de package remplit le nouveau package avec les informations de tous les fichiers. OSD dans le répertoire source.</p></td>
</tr>
</tbody>
</table>

 

### Exemple d’instruction de conversion

Pour mieux comprendre le nouveau processus, consultez l’exemple d' `ConvertFrom-AppvLegacyPackage` instruction de convertisseur de package suivant.

**Si le répertoire source (\\\\OldPkgStore\\ContosoApp) inclut les éléments suivants:**

-   ContosoApp. sft

-   ContosoApp.msi

-   ContosoApp. sprj

-   ContosoApp\_manifest.xml

-   X. OSD

-   Y. OSD

-   Z. OSD

**Et si vous exécutez la commande suivante:**

``` syntax
ConvertFrom-AppvLegacyPackage –SourcePath \\OldPkgStore\ContosoApp\ 
-DestinationPath \\NewPkgStore\ContosoApp\
-OSDsToIncludeInPackage X.osd,Y.osd
```

**Les informations suivantes sont créées dans le répertoire de destination (\\\\NewPkgStore\\ContosoApp):**

-   ContosoApp. AppV

-   ContosoApp.msi

-   ContosoApp\_DeploymentConfig.xml

-   ContosoApp\_UserConfig.xml

-   X\_Config.xml

-   Y\_Config.xml

-   Z\_Config.xml

**Dans l’exemple ci-dessus:**

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Fichiers de répertoire sources suivants...</th>
<th align="left">... sont convertis en fichiers de répertoire de destination...</th>
<th align="left">... et contiennent ces éléments.</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><ul>
<li><p>X. OSD</p></li>
<li><p>Y. OSD</p></li>
<li><p>Z. OSD</p></li>
</ul></td>
<td align="left"><ul>
<li><p>X_Config.xml</p></li>
<li><p>Y_Config.xml</p></li>
<li><p>Z_Config.xml</p></li>
</ul></td>
<td align="left"><ul>
<li><p>Variables d’environnement</p></li>
<li><p>Associés</p></li>
<li><p>Associations de types de fichiers</p></li>
<li><p>Informations de Registre</p></li>
<li><p>Scripts</p></li>
</ul></td>
<td align="left"><p>Chaque fichier. OSD est converti en un fichier XML distinct correspondant qui contient les éléments répertoriés ici dans le format de configuration de déploiement App-V 5,1. Ces éléments peuvent ensuite être copiés à partir de ces fichiers. xml et placés dans les fichiers de configuration de déploiement ou de configuration utilisateur comme vous le souhaitez.</p>
<p>Dans cet exemple, il existe trois fichiers. xml correspondant aux trois fichiers. OSD dans le répertoire source. Chaque fichier. xml contient les variables d’environnement, les raccourcis, les associations de types de fichier, les informations de Registre et les scripts dans le fichier. OSD correspondant.</p></td>
</tr>
<tr class="even">
<td align="left"><ul>
<li><p>X. OSD</p></li>
<li><p>Y. OSD</p></li>
</ul></td>
<td align="left"><ul>
<li><p>ContosoApp. AppV</p></li>
<li><p>ContosoApp_DeploymentConfig.xml</p></li>
<li><p>ContosoApp_UserConfig.xml</p></li>
</ul></td>
<td align="left"><ul>
<li><p>Variables d’environnement</p></li>
<li><p>Associés</p></li>
<li><p>Associations de types de fichiers</p></li>
</ul></td>
<td align="left"><p>Les informations des fichiers. OSD spécifiés dans le <code>-OSDsToIncludeInPackage</code> paramètre sont converties et placées à l’intérieur du package. Le convertisseur remplit alors le fichier de configuration du déploiement et le fichier de configuration de l’utilisateur avec le contenu du package, tout comme le Sequencer App-V lors du séquençage d’un nouveau package.</p>
<p>Dans cet exemple, des variables d’environnement, des raccourcis et des associations de types de fichiers incluses dans X. OSD et Y. OSD ont été converties et placées dans le package App-V et certaines de ces informations sont également incluses dans les fichiers de configuration de déploiement et de configuration de l’utilisateur. X. OSD et Y. OSD étaient utilisés, car ils ont été inclus comme arguments pour le <code>-OSDsToIncludeInPackage</code> paramètre. Aucune information de Z. OSD n’est incluse dans le package, car elle n’a pas été incluse dans l’un des arguments suivants.</p></td>
</tr>
</tbody>
</table>

 

## Conversion de packages créés à l’aide d’une version antérieure d’App-V


Utilisez l’utilitaire convertisseur de package pour mettre à niveau des packages d’application virtuels créés à l’aide de versions de App-V antérieures à App-V 5,0. Le convertisseur de package utilise PowerShell pour convertir des packages et peut faciliter l’automatisation du processus si vous avez de nombreux packages qui nécessitent une conversion.

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
<td align="left"><p>Les packages virtuels utilisant DSC ne sont pas liés après la conversion.</p></td>
<td align="left"><p>Liez les packages à l’aide de groupes de connexion. Voir <a href="managing-connection-groups51.md" data-raw-source="[Managing Connection Groups](managing-connection-groups51.md)"> gestion des groupes de connexion </a> .</p></td>
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

**Remarques**  Nous vous recommandons d’utiliser le Sequencer App-V 5,1 pour convertir des applications ou applications critiques qui doivent tirer parti de fonctionnalités. Pour plus d' [informations sur la façon de séquencer une nouvelle application avec App-V 5,1](how-to-sequence-a-new-application-with-app-v-51-beta-gb18030.md), voir.

Si un package converti ne s’ouvre pas après l’avoir converti, il est également recommandé de réorganiser l’application à l’aide du séquenceur App-V 5,1.

 

[Comment convertir un package créé dans une version précédente d'App-V](how-to-convert-a-package-created-in-a-previous-version-of-app-v51.md)

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
<td align="left"><p>Mettez à niveau votre environnement vers la dernière version de l’application-V 4.6</p></td>
<td align="left"><p><a href="../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md" data-raw-source="[Application Virtualization Deployment and Upgrade Considerations](../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md)">Considérations en matière de déploiement et de mise à niveau de la virtualisation des applications </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Installez le client App-V 5,1 avec la coexistence activée.</p></td>
<td align="left"><p><a href="how-to-deploy-the-app-v-46-and-the-app-v--51-client-on-the-same-computer.md" data-raw-source="[How to Deploy the App-V 4.6 and the App-V 5.1 Client on the Same Computer](how-to-deploy-the-app-v-46-and-the-app-v--51-client-on-the-same-computer.md)">Déploiement de l’application-V 4,6 et du client App-V 5,1 sur le même ordinateur </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Séquence et déploiement des packages App-V 5,1. Le cas échéant, annulez la publication des packages App-V 4,6.</p></td>
<td align="left"><p><a href="how-to-sequence-a-new-application-with-app-v-51-beta-gb18030.md" data-raw-source="[How to Sequence a New Application with App-V 5.1](how-to-sequence-a-new-application-with-app-v-51-beta-gb18030.md)">Comment séquencer une nouvelle application avec App-V 5,1 </a> .</p></td>
</tr>
</tbody>
</table>

 

**Important**  Vous devez utiliser la dernière version de App-V 4.6 pour utiliser le mode de coexistence. Par ailleurs, lorsque vous séquencez un package, vous devez configurer le paramètre administration de l’autorité, qui se trouve dans la **Configuration utilisateur** , dans la section Configuration de l' **utilisateur** .

 

## Migration de l’infrastructure complète de l’application-V 5,1 Server


Il n’existe aucune méthode directe pour effectuer une mise à niveau vers une infrastructure App-V 5,1 complète. Pour plus d’informations sur la mise à niveau de l’application-V Server, utilisez les informations de la section suivante.

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
<td align="left"><p>Mettez à niveau votre environnement vers la dernière version de App-V 4.6.</p></td>
<td align="left"><p><a href="../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md" data-raw-source="[Application Virtualization Deployment and Upgrade Considerations](../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md)">Considérations en matière de déploiement et de mise à niveau de la virtualisation des applications </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Déploiement de la version 5,1 App-V du client.</p></td>
<td align="left"><p><a href="how-to-deploy-the-app-v-client-51gb18030.md" data-raw-source="[How to Deploy the App-V Client](how-to-deploy-the-app-v-client-51gb18030.md)">Déploiement du client App-V </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Installez App-V 5,1 Server.</p></td>
<td align="left"><p><a href="how-to-deploy-the-app-v-51-server.md" data-raw-source="[How to Deploy the App-V 5.1 Server](how-to-deploy-the-app-v-51-server.md)">Déploiement du serveur App-V 5,1 </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Migrer des packages existants.</p></td>
<td align="left"><p>Voir les <strong> packages de conversion créés à l’aide d’une version antérieure de la section App-V </strong> de cet article.</p></td>
</tr>
</tbody>
</table>

 

## Tâches de migration supplémentaires


Vous pouvez également effectuer d’autres tâches de migration telles que la reconfiguration des points de terminaison et l’ouverture d’un package créé à l’aide d’une version antérieure sur un ordinateur exécutant le client App-V 5,1. Les liens suivants fournissent des informations supplémentaires sur l’exécution de ces tâches.

[Migration de points d'extension d'un package App-V4.6 vers un package App-V5.1 converti pour tous les utilisateurs sur un ordinateur spécifique](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-51-package-for-all-users-on-a-specific-computer.md)

[Migration de points d'extension d'un package App-V4.6 vers un package App-V5.1 pour un utilisateur spécifique](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-51-for-a-specific-user.md)

[Restauration de points d'extension d'un package App-V5.1 vers un package App-V4.6 pour tous les utilisateurs sur un ordinateur spécifique](how-to-revert-extension-points-from-an-app-v-51-package-to-an-app-v-46-package-for-all-users-on-a-specific-computer.md)

[Restauration de points d'extension d'un package App-V5.1 vers un package App-V4.6 pour un utilisateur spécifique](how-to-revert-extension-points-from-an-app-v-51-package-to-an-app-v-46-package-for-a-specific-user.md)







## Autres ressources pour effectuer des tâches de migration d’application-V


[Opérations d'App-V5.1](operations-for-app-v-51.md)

[Procédure de mise à niveau du serveur de gestion Microsoft App-V 5,1 simplifiée](https://go.microsoft.com/fwlink/p/?LinkId=786330)

 

 





