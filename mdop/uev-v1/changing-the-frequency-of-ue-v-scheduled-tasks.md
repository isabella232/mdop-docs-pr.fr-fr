---
title: Modification de la fréquence des tâches planifiées UE-V
description: Modification de la fréquence des tâches planifiées UE-V
author: dansimp
ms.assetid: 33c2674e-0df4-4717-9c3d-820a90b16e19
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ced608608ffae82a29fb5ca84cfca281082b8127
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809504"
---
# Modification de la fréquence des tâches planifiées UE-V


Le programme d’installation de l’agent Microsoft User Interface Virtualization (UE-V), AgentSetup.exe, crée deux tâches planifiées au cours de l’installation de l’agent UE-V. Les deux tâches sont la tâche de **mise à jour automatique de modèle** et la tâche définir l’état de l' **emplacement de stockage** . Ces tâches planifiées ne peuvent pas être configurées avec les outils UE-V. Les administrateurs désireux de modifier la tâche planifiée pour ces éléments peuvent créer un script qui utilise les options de la ligne de commande Schtasks.exe.

Pour plus d’informations sur les Schtasks.exe, voir [utilisation de schtasks, exe pour planifier des tâches dans Windows Server 2003](https://go.microsoft.com/fwlink/?LinkID=264854).

## Mise à jour automatique de modèle


La tâche de **mise à jour automatique de modèle** vérifie dans le catalogue de modèles de paramètres les modèles nouveaux, mis à jour ou supprimés. Cette tâche s’exécute uniquement si la SettingsTemplateCatalog est configurée. La tâche de **mise à jour automatique du modèle** exécute le fichier ApplySettingsCatalog.exe situé dans le répertoire d’installation de l’agent UE-V.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nom de la tâche</th>
<th align="left">Déclencheur par défaut</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Mise à jour automatique \Microsoft\UE-V\Template</p></td>
<td align="left"><p>3:30 AM tous les jours</p></td>
</tr>
</tbody>
</table>

 

**Par exemple:** La commande suivante configure l’agent pour vérifier dans le magasin de catalogues de modèles les paramètres chaque heure.

``` syntax
schtasks /change /tn "Microsoft\UE-V\Template Auto Update" /ri 60
```

## État de l’emplacement de stockage des paramètres


La tâche définir l’état de l' **emplacement de stockage** effectue les actions suivantes:

1.  Vérifie que les dossiers UE-V sont toujours épinglés ou enregistrés à l’aide de la fonctionnalité fichiers en mode hors connexion.

2.  Vérifie si l’emplacement de stockage des paramètres est hors connexion ou en ligne.

3.  Force une synchronisation à l’intervalle spécifié au lieu de l’intervalle par défaut des fichiers en mode hors connexion.

4.  Synchronise les packages de paramètres qui sont configurés pour être prédéfinis.

5.  Vérifie si le chemin d’accès du répertoire de base Active Directory a changé.

6.  Écrit la configuration de stockage des paramètres actuelle sous l’emplacement suivant.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Nom de la tâche</th>
    <th align="left">Déclencheur par défaut</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>État de l’emplacement de stockage \Microsoft\UE-V\Settings</p></td>
    <td align="left"><p>Lors de la connexion de tout utilisateur, après un déclenchement répété, répéter toutes les 30 minutes.</p></td>
    </tr>
    </tbody>
    </table>

     

**Par exemple:** La commande suivante configure l’agent pour qu’il exécute l’action située au-dessus toutes les heures.

``` syntax
schtasks /change /tn "\Microsoft\UE-V\Settings Storage Location Status" /ri 60
```

## Rubriques connexes


[Administration d'UE-V1.0](administering-ue-v-10.md)

[Opérations d'UE-V1.0](operations-for-ue-v-10.md)

 

 





