---
title: Comment créer un groupe de connexion avec des packages publiés par l’utilisateur et globalement
description: Comment créer un groupe de connexion avec des packages publiés par l’utilisateur et globalement
author: dansimp
ms.assetid: 82f7ea7f-7b14-4506-8940-fdcd6c3e117f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: c98981180133881909db17d19cb42771f94bd66a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805664"
---
# Comment créer un groupe de connexion avec des packages publiés par l’utilisateur et globalement
Vous pouvez créer des groupes de connexion habilités par l’utilisateur qui contiennent des packages publiés par l’utilisateur et globalement publiés, en utilisant l’une des méthodes suivantes:

-   [Comment utiliser les applets de connexion PowerShell pour créer des groupes de connexion habilités par l’utilisateur](#bkmk-posh-userentitled-cg)

-   [Utilisation du serveur App-V pour créer des groupes de connexion autorisés par l’utilisateur](#bkmk-appvserver-userentitled-cg)

**Ce que vous devez savoir avant de commencer:**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Scénarios non pris en charge et problèmes potentiels</th>
<th align="left">Résultat</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Vous ne pouvez pas inclure de packages publiés par l’utilisateur dans les groupes de connexion globalement autorisés.</p></td>
<td align="left"><p>Le groupe de connexion ne fonctionnera pas.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Si vous publiez un package dans le monde entier, puis créez un groupe de connexion publié par un utilisateur qui n’est pas facultatif, vous pouvez toujours exécuter <strong> unpublisher-AppvClientPackage &lt; package &gt; -global </strong> pour annuler la publication du package, même si ce package est utilisé dans un autre groupe de connexion.</p></td>
<td align="left"><p>S’il s’agit d’un autre groupe de connexion utilisant ce package, le package échouera dans ces groupes de connexion.</p>
<p>Pour éviter d’annuler accidentellement la publication d’un package non facultatif utilisé dans un autre groupe de connexion, nous vous recommandons d’effectuer le suivi des groupes de connexion dans lesquels vous avez utilisé un package non facultatif.</p></td>
</tr>
</tbody>
</table>

 
<a href="" id="bkmk-posh-userentitled-cg"></a>**Comment utiliser les cmdlets PowerShell pour créer des groupes de connexion qui ont été autorisés par l’utilisateur**

1.  Ajoutez des packages et publiez-les à l’aide des commandes suivantes:

    **Add-AppvClientPackage package1 \ _AppV \ _file \ _Path**

    **Add-AppvClientPackage package2 \ _AppV \ _file \ _Path**

    **Publisher-AppvClientPackage-PackageId package1 \ _ID-VersionId package1 \ _Version ID-global**

    **Publisher-AppvClientPackage-PackageId package2 \ _ID-VersionIdPackage2 \ _ID**

2.  Créez le fichier XML de groupe de connexion. Pour plus d’informations, consultez [à propos du fichier de groupe de connexion](about-the-connection-group-file.md).

3.  Ajoutez et publiez le groupe de connexions en utilisant les commandes suivantes:

    **Connexion Add-AppvClientConnectionGroup \ _Group \ _XML \ _file \ _Path**

    **Enable-AppvClientConnectionGroup-GroupId CG \ _Group \ _ID-CG CG \ _Version \ _ID**

<a href="" id="bkmk-appvserver-userentitled-cg"></a>**Utilisation du serveur App-V pour créer des groupes de connexion autorisés par l’utilisateur**

1.  Ouvrez la console de gestion App-V 5,0.

2.  Suivez les instructions de la [procédure de publication d’un package à l’aide de la console de gestion](how-to-publish-a-package-by-using-the-management-console-50.md) pour publier des packages globalement et pour l’utilisateur.

3.  Suivez les instructions de la [procédure de création d’un groupe de connexion](how-to-create-a-connection-group.md) pour créer le groupe de connexion et ajouter les packages publiés par l’utilisateur et publiés globalement.

    Vous **avez une suggestion pour App-V**? Ajoutez ou Votez en fonction [de suggestions.](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization) **Vous avez un problème lié à l’application-V?** Utilisez le [Forum TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Rubriques connexes


[Gestion des groupes de connexion](managing-connection-groups.md)

[Comment utiliser des packages facultatifs dans les groupes de connexion](how-to-use-optional-packages-in-connection-groups.md)

 

 





