---
title: Comment charger une image MED-V sur le serveur
description: Comment charger une image MED-V sur le serveur
author: dansimp
ms.assetid: 0e70dfdf-3e3a-4860-970c-535806caa907
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6703eb24bc3542c280af41988a257a2f14643645
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811315"
---
# Comment charger une image MED-V sur le serveur


Après avoir testé une image MED-V, celle-ci peut être empaquetée puis chargée sur le serveur. Pour plus d’informations sur la configuration d’un serveur de distribution Web d’images, voir [Comment configurer le serveur de distribution Web d’images](how-to-configure-the-image-web-distribution-server.md).

Une fois qu’une image MED-V est compactée et téléchargée sur le serveur, elle peut être distribuée aux utilisateurs à l’aide d’un centre de distribution de logiciels d’entreprise, ou elle peut être téléchargée par les utilisateurs à l’aide d’un package de déploiement. Pour plus d’informations sur le déploiement à l’aide d’un centre de distribution de logiciels d’entreprise, voir [déploiement d’un espace de travail MED-V à l’aide d’un système de distribution de logiciels d’entreprise](deploying-a-med-v-workspace-using-an-enterprise-software-distribution-system.md). Pour plus d’informations sur le déploiement à l’aide d’un package, voir [déploiement d’un espace de travail MED-V à l’aide d’un package de déploiement](deploying-a-med-v-workspace-using-a-deployment-package.md).

**Remarque**  
Avant de télécharger une image, vérifiez qu’aucun proxy Web n’est défini dans les paramètres de votre navigateur et que Windows Update n’est pas en cours d’exécution actuellement.



**Pour télécharger une image MED-V sur le serveur**

1.  Dans le volet **images groupées locales** , sélectionnez l’image que vous avez créée.

2.  Cliquez sur **Télécharger**.

    L’image est téléchargée sur le serveur. Cette opération peut prendre un certain temps.

    Les images du serveur sont définies avec les propriétés répertoriées dans le tableau suivant.

**Images empaquetées sur les propriétés du serveur**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Propriété</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Nom de l’image</p></td>
<td align="left"><p>Nom de l’image compactée telle qu’elle a été définie lors de la création de l’image par l’administrateur.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Version</p></td>
<td align="left"><p>Version de l’image affichée.</p>
<div class="alert">
<strong>Remarque</strong><br/><p>Toutes les versions précédentes sont conservées sauf si supprimées.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>Taille du fichier (compressé)</p></td>
<td align="left"><p>Taille compressée physique de l’image.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Taille de l’image (non compressée)</p></td>
<td align="left"><p>Taille de l’image qui n’est pas compressée.</p></td>
</tr>
</tbody>
</table>



## Rubriques connexes


[Comment installer le client MED-V et la console de gestion MED-V](how-to-install-med-v-client-and-med-v-management-console.md)

[Utilisation de l'interface utilisateur de la console de gestion MED-V](using-the-med-v-management-console-user-interface.md)

[Création d'une image Virtual PC pour MED-V](creating-a-virtual-pc-image-for-med-v.md)

[Comment empaqueter une image MED-V](how-to-pack-a-med-v-image.md)









