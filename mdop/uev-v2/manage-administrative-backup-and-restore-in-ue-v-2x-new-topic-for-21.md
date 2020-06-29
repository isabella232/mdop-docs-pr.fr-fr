---
title: Gérer la sauvegarde et la restauration d’administration dans UE-V 2. x
description: Gérer la sauvegarde et la restauration d’administration dans UE-V 2. x
author: dansimp
ms.assetid: 2eb5ae75-65e5-4afc-adb6-4e83cf4364ae
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 11c168b54b71731c51417b2b7c4737c85f42035a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812324"
---
# Gérer la sauvegarde et la restauration d’administration dans UE-V 2. x


En tant qu’administrateur de Microsoft User Interface Virtualization (UE-V) 2,0, 2,1 ou 2,1 SP1, vous pouvez restaurer les paramètres d’application et de fenêtre à l’état d’origine. Dans le cadre de l’ajout d’un nouvel appareil dans UE-V 2,1, vous pouvez également restaurer des paramètres supplémentaires.

## Restaurer les paramètres dans UE-V 2,1 ou UE-V 2,1 SP1 lorsqu’un utilisateur adopte un nouvel appareil


Pour restaurer les paramètres lors de la mise en place d’un nouvel appareil par un utilisateur, vous pouvez placer un modèle d’emplacement des paramètres dans le profil de **sauvegarde** ou d' **itinérance (par défaut)** à l’aide de l’applet de connexion Set-UevTemplateProfile PowerShell. Cela permet aux paramètres de l’ordinateur de se synchroniser avec le nouvel ordinateur, en plus des paramètres utilisateur. Les modèles attribués au profil de sauvegarde sont sauvegardés pour cet appareil et configurés sur une base par appareil. Pour sauvegarder les paramètres d’un modèle, utilisez l’applet de commande suivante dans Windows PowerShell:

``` syntax
Set-UevTemplateProfile -ID <TemplateID> -Profile <backup>
```

-   &lt;TemplateID &gt; est l’ID du modèle UE-V.

-   &lt;la sauvegarde &gt; peut être de type sauvegarde ou itinérance.

Lorsque vous remplacez l’appareil d’un utilisateur-V, les paramètres sont restaurés automatiquement si le domaine, le nom d’utilisateur et le nom de l’appareil de l’utilisateur correspondent. Toutes les données synchronisées et toutes les données de sauvegarde sont automatiquement restaurées sur l’appareil.

Vous pouvez également utiliser la nouvelle cmdlet PowerShell, Restore-UevBackup, pour restaurer les paramètres d’un autre appareil. Pour cloner les packages de paramètres pour le nouvel appareil, utilisez l’applet de commande suivante dans Windows PowerShell:

``` syntax
Restore-UevBackup –Machine <MachineName>
```

où &lt; nomordinateur &gt; correspond au nom d’ordinateur de l’appareil.

Les modèles tels que le modèle Office 2013 qui incluent de nombreuses applications peuvent tous être inclus dans le profil itinérant (par défaut) ou sauvegardé. Chaque application individuelle d’une suite de modèles suit le groupe. Les modèles de zone de boîte de votre entreprise 2013 incluent des paramètres d’itinérance et de sauvegarde uniquement. Les paramètres de sauvegarde ne peuvent pas être inclus dans un profil itinérant.

Dans le cadre de la fonctionnalité de sauvegarde/restauration, UE-V a ajouté le **dernier fonctionnement connu (LKG)** aux options permettant de restaurer les paramètres. Dans cette version, vous pouvez restaurer les paramètres d’origine ou les paramètres LKG. Les paramètres LKG permettent aux utilisateurs de revenir à un point intermédiaire et stable avant l’État pre-UE-V des paramètres.

### Sauvegarder et restaurer des modèles avec UE-V

Voici les composants clés de sauvegarde et de restauration de UE-V:

-   Profils de modèles

-   Emplacement des packages de paramètres dans le modèle d’emplacement de stockage des paramètres

-   Déclencheur de sauvegarde

-   Restauration des paramètres

**Profils de modèles**

Un profil de modèle UE-V est défini lorsque le modèle est enregistré sur l’appareil ou après l’inscription via l’utilitaire de configuration PowerShell/WMI. Les types de profils sont les suivants:

-   Itinérance (par défaut)

-   Sauvegarde

-   En un coup de passe

Tous les modèles sont inclus dans le profil d’itinérance s’ils sont enregistrés sauf spécification contraire. Les modèles suivants permettent de synchroniser les paramètres avec tous les appareils sur lesquels le modèle correspondant a été activé.

Les modèles peuvent être ajoutés au profil de sauvegarde avec PowerShell ou WMI à l’aide de l’applet de applet Set-UevTemplateProfile. Les modèles dans le profil de sauvegarde enregistrent ces paramètres vers l’emplacement de stockage des paramètres dans un répertoire de noms d’appareils spécial. Les paramètres spécifiés sont sauvegardés à cet emplacement.

Les modèles désignés en dernier incluent des paramètres spécifiques à cet appareil qui ne doivent pas être synchronisés, sauf s’ils sont explicitement restaurés. Ces paramètres sont stockés dans l’emplacement du package de paramètres spécifique à l’appareil, à l’emplacement de stockage des paramètres comme paramètres Backedup. Ces modèles ont un identificateur spécial incorporé dans le modèle qui spécifie qu’ils doivent faire partie de ce profil.

**Emplacement des packages de paramètres dans le modèle d’emplacement de stockage des paramètres**

Les paramètres de profil itinérant sont stockés dans l’emplacement de stockage des paramètres. Les modèles attribués au registre de sauvegarde ou à l’enregistrement par le biais stockent leurs paramètres dans l’emplacement de stockage des paramètres dans un répertoire de noms d’appareils spécial. Chaque appareil doté de modèles dans ces profils possède son nom de l’appareil. UE-V ne nettoie pas ces annuaires.

**Déclencheur de sauvegarde**

La sauvegarde est déclenchée par les mêmes événements déclenchant une synchronisation UE-V.

**Restauration des paramètres**

La restauration de l’appareil d’un utilisateur restaure les paramètres du modèle actuellement inscrits à partir du dossier de sauvegarde d’un autre appareil, ainsi que tous les paramètres synchronisés vers l’ordinateur actuel. Les paramètres sont restaurés de deux manières:

-   **Restauration automatique**

    Si le chemin d’accès, le domaine et le nom de l’ordinateur de l’utilisateur correspondent à l’utilisateur actuel, tous les paramètres de cet utilisateur sont synchronisés, avec uniquement les derniers paramètres appliqués. Si un utilisateur ouvre une session sur un nouvel appareil pour la première fois et que ces critères sont remplis, les données de paramètres sont appliquées à cet appareil.

    **Remarque**  
    Les paramètres d’accessibilité et de bureau Windows requièrent que l’utilisateur se connecte à nouveau pour qu’il s’applique.



-   **Restauration manuelle**

    Si vous souhaitez aider les utilisateurs en restaurant un appareil lors d’une actualisation, vous pouvez choisir d’utiliser l’applet de passe Restore-UevBackup. Cette commande entraîne le téléchargement des paramètres de l’utilisateur à partir de l’emplacement de stockage des paramètres.

## Rétablir l’état d’origine des paramètres d’application et de fenêtre


Les commandes WMI et Windows PowerShell vous permettent de restaurer les paramètres d’application et de Windows aux valeurs de paramètres qui se trouvaient sur l’ordinateur lors du premier démarrage de l’application après l’installation d’UE-V. Cette action de restauration est effectuée en fonction des paramètres par application ou Windows. Les paramètres sont restaurés lors de la prochaine exécution de l’application, ou les paramètres sont restaurés dès que l’utilisateur ouvre une session sur le système d’exploitation.

**Pour restaurer les paramètres d’application et les paramètres Windows avec Windows PowerShell pour UE-V 2. x**

1.  Ouvrez la fenêtre Windows PowerShell.

2.  Entrez l’applet de commande Windows PowerShell suivante pour restaurer les paramètres de l’application et les paramètres Windows.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong>Cmdlet Windows PowerShell</strong></th>
    <th align="left"><strong>Description</strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><code>Restore-UevUserSetting -&lt;TemplateID&gt;</code></p></td>
    <td align="left"><p>Restaure les paramètres utilisateur pour une application ou rétablit un groupe de paramètres Windows.</p></td>
    </tr>
    </tbody>
    </table>



**Pour restaurer les paramètres d’application et les paramètres Windows avec WMI**

1.  Ouvrez une fenêtre Windows PowerShell.

2.  Entrez la commande WMI suivante pour restaurer les paramètres de l’application et les paramètres Windows.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong>Commande WMI</strong></th>
    <th align="left"><strong>Description</strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class UserSettings -Name RestoreByTemplateId -ArgumentList &lt;template_ID&gt;</code></p></td>
    <td align="left"><p>Restaure les paramètres utilisateur pour une application ou rétablit un groupe de paramètres Windows.</p></td>
    </tr>
    </tbody>
    </table>



~~~
**Note**  
UE-V does not provide a settings rollback for Windows apps.
~~~








## Rubriques connexes


[Administration d’UE-V 2. x avec Windows PowerShell et WMI](administering-ue-v-2x-with-windows-powershell-and-wmi-both-uevv2.md)

[Administration d’UE-V 2. x](administering-ue-v-2x-new-uevv2.md)









