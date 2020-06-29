---
title: Planification d'une migration à partir d'une version précédente d'App-V
description: Planification d'une migration à partir d'une version précédente d'App-V
author: dansimp
ms.assetid: 4a058047-9674-41bc-8050-c58c97a80a9b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: d7f2496b355aee6a598fee44c84e7e8c0f755c4f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804999"
---
# Planification d'une migration à partir d'une version précédente d'App-V


Utilisez les informations suivantes pour planifier la migration vers Microsoft Application Virtualization (App-V) 5,1 à partir de versions précédentes d’App-V.

## Exigences de migration


Avant de commencer une mise à niveau, consultez la configuration requise suivante:

-   Si vous effectuez une mise à niveau à partir d’une version antérieure à celle du SP2 App-V 4,6, effectuez d’abord la mise à niveau vers la version App-v 4,6 SP3 avant de procéder à la mise à niveau vers App-V 5,1 ou une version ultérieure. Dans ce scénario, mettez d’abord à niveau les clients App-V, puis mettez à niveau les composants serveur.
**Remarque:** App-V 4,6 a quitté le support technique standard.

-   App-V 5,1 prend en charge uniquement les packages de création utilisant App-V 5,0 ou App-V 5,1 ou les packages qui ont été convertis au format **. AppV** .

-   Si vous effectuez une mise à niveau de l’application-V Server vers App-V 5,0 SP1, voir [à propos de App-v 5,1](about-app-v-51.md#bkmk-migrate-to-51) pour obtenir des instructions.

## Exécution simultanée du client App-V 5,1 avec App-V 4,6


Vous pouvez exécuter le client App-V 5,1 simultanément sur le même ordinateur que le client App-V 4.6 SP3.

Lorsque vous exécutez le coexistence de clients App-V, vous pouvez:

-   Convertissez un package App-V 4,6 SP3 au format App-V 5,1 et publiez les deux packages lorsque les deux clients s’exécutent.

-   Définissez la stratégie de migration pour le package converti, qui permet au package App-V 5,1 converti de supposer les associations de types de fichiers et les raccourcis du package App-V 4,6.

### Scénarios de coexistence pris en charge

Le tableau suivant répertorie les scénarios de coexistence App-V pris en charge. Nous vous recommandons d’installer les dernières mises à jour disponibles d’une version donnée lorsque vous exécutez un client coexistant.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Type de client App-V 4,6</th>
<th align="left">Type de client App-V 5,1</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>App-V 4,6 SP3</p></td>
<td align="left"><p>App-V 5.1</p></td>
</tr>
<tr class="even">
<td align="left"><p>App-V 4,6 SP3 RDS</p></td>
<td align="left"><p>App-V 5,1 RDS</p></td>
</tr>
</tbody>
</table>

 

### Configuration requise pour l’utilisation de clients coexistant

Pour exécuter des clients coexistants, vous devez:

-   Installez le client App-V 4.6 avant d’installer le client App-V 5,1.

-   Activez le paramètre Activer la stratégie de groupe du **mode migration** , qui se trouve dans le nœud de coexistence du client **App-V** &gt; **Client Coexistence** . Pour déployer le modèle. admx, voir [Comment télécharger et déployer des modèles de stratégie de groupe MDOP (. admx)](https://technet.microsoft.com/library/dn659707.aspx).

**Remarques**  Les packages App-V 5,1 peuvent s’exécuter côte à côte avec les packages App-V 4,6 Si vous disposez d’installations coexistantes d’App-V 5,1 et 4,6. Toutefois, les packages App-V 5,1 ne peuvent pas interagir avec les packages App-V 4,6 dans le même environnement virtuel.

 

### Téléchargements et documentation du client

Le tableau suivant fournit des liens vers les téléchargements de clients App-V 4,6 et la documentation TechNet sur les versions. Les téléchargements incluent les clients application-V «Regular» et RDS. La documentation TechNet relative au client App-V s’applique aux deux clients, sauf indication contraire.

<table>
<colgroup>
<col width="33%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Version App-V</th>
<th align="left">Lien vers la documentation TechNet</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>App-V 4.6 SP3</p></td>
<td align="left"><p><a href="https://technet.microsoft.com/library/dn511019.aspx" data-raw-source="[About Microsoft Application Virtualization 4.6 SP3](https://technet.microsoft.com/library/dn511019.aspx)">À propos de Microsoft Application Virtualization4.6 SP3</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>App-V 4.6 SP3</p></td>
<td align="left"><p><a href="about-app-v-51.md" data-raw-source="[About Microsoft Application Virtualization 5.1](about-app-v-51.md)">À propos de Microsoft Application Virtualization 5,1</a></p></td>
</tr>
</tbody>
</table>

 

Pour plus d’informations sur la configuration de la coexistence du client App-V 5,1, voir:

-   [Déploiement de l’application-V 4,6 et du client App-V 5,1 sur le même ordinateur](how-to-deploy-the-app-v-46-and-the-app-v--51-client-on-the-same-computer.md)

-   [Coexistence et migration avec App-V 5,0](https://technet.microsoft.com/windows/jj835811.aspx)

## <a href="" id="converting--previous-version--packages-using-the-package-converter-"></a>Conversion de packages «Previous-version» à l’aide du convertisseur de package


Avant de migrer un package créé à l’aide de App-4,6 SP2 ou version antérieure vers App-V 5,1, consultez la configuration requise suivante:

-   Vous devez convertir le package au format de fichier **. AppV** .

-   Le convertisseur de package prend uniquement en charge la conversion directe des packages qui ont été créés à l’aide de App-V 4,5 et versions ultérieures. Pour utiliser le convertisseur de package sur un package qui a été créé à l’aide d’une version antérieure, vous devez utiliser une application-V 4.5 ou version ultérieure du Sequencer pour mettre à niveau le package, puis vous pouvez effectuer la conversion du package.

Pour plus d’informations sur l’utilisation du convertisseur de package pour convertir un package, voir [Comment convertir un package créé dans une version antérieure d’App-V](how-to-convert-a-package-created-in-a-previous-version-of-app-v51.md). Après avoir converti le fichier, vous pouvez le déployer sur des ordinateurs cibles qui exécutent le client App-V 5,1.






## Rubriques connexes


[Envisager de déployer App-V](planning-to-deploy-app-v51.md)

 

 





