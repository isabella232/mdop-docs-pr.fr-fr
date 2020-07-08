---
title: Modification de la fréquence des tâches planifiées UE-V 2. x
description: Modification de la fréquence des tâches planifiées UE-V 2. x
author: dansimp
ms.assetid: ee486570-c6cf-4fd9-ba48-0059ba877c10
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 09/29/2016
ms.openlocfilehash: 1c1e3c091431dc56068dcd1fe0e849b0df1f6aa0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810548"
---
# Modification de la fréquence des tâches planifiées UE-V 2. x


Le programme d’installation de Microsoft User Interface Virtualization (UE-V) 2,0, 2,1 ou 2,1 SP1 agent, AgentSetup.exe, crée les tâches planifiées suivantes lors de l’installation d’UE-V agent:

-   **Surveiller les paramètres de l’application**

-   **Application de contrôleur de synchronisation**

-   **Synchroniser les paramètres lors de la fermeture de session**

-   **Mise à jour automatique de modèle**

-   **Collecter les données du programme d’amélioration du produit**

-   **Télécharger les données du programme d’amélioration du produit**

**Remarques**  À l’exception de la collecte des données du programme d’amélioration du produit, les tâches suivantes doivent rester activées car UE-V ne peut pas fonctionner sans eux.

 

Ces tâches planifiées ne peuvent pas être configurées avec les outils UE-V. Les administrateurs désireux de modifier la tâche planifiée pour ces éléments peuvent créer un script qui utilise les options de la ligne de commande Schtasks.exe.

Pour plus d’informations sur les Schtasks.exe, voir [utilisation de schtasks, exe pour planifier des tâches dans Windows Server 2003](https://go.microsoft.com/fwlink/?LinkID=264854).

Pour plus d’informations sur

## Tâches planifiées UE-V


Les tâches planifiées suivantes sont incluses dans UE-V 2 avec des exemples de commandes de configuration de tâches planifiées.

### Collecter les données du programme d’amélioration du produit

Si, à l’issue de l’installation, l’utilisateur ou l’administrateur a choisi de participer au programme d’amélioration du produit (CEIP), UE-V collecte des données afin d’améliorer le produit dans les versions ultérieures. Cette tâche planifiée ne s’exécute qu’à l’ouverture de session. La tâche recueillir les données du programme d' **amélioration du produit** exécute le UevSqmSession.exe figurant dans le répertoire d’installation de l’agent UE-V.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nom de la tâche</th>
<th align="left">Événement par défaut</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>\Microsoft\UE-V\Collect les données du programme d’amélioration du produit</p></td>
<td align="left"><p>Accès</p></td>
</tr>
</tbody>
</table>

 

### Surveiller les paramètres de l’application

La tâche **surveiller les paramètres d’application** permet de synchroniser les paramètres des applications Windows. Elle est exécutée lors de la connexion, mais elle est retardée de 30 secondes sans répercussions sur la connexion. La tâche surveiller l’état de l’application exécute le fichier UevAppMonitor.exe qui se trouve dans le répertoire d’installation de l’agent UE-V.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nom de la tâche</th>
<th align="left">Événement par défaut</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>État de l’application \Microsoft\UE-V\Monitor</p></td>
<td align="left"><p>Accès</p></td>
</tr>
</tbody>
</table>

 

### Application de contrôleur de synchronisation

La tâche de l' **application du contrôleur de synchronisation** est utilisée pour démarrer le contrôleur de synchronisation afin de synchroniser les paramètres de l’ordinateur vers l’emplacement de stockage des paramètres. Par défaut, la tâche est exécutée toutes les 30 minutes. À ce moment, les paramètres locaux sont synchronisés avec l’emplacement de stockage des paramètres, et les paramètres mis à jour à l’emplacement de stockage des paramètres sont synchronisés avec l’ordinateur. L’application de contrôleur de synchronisation exécute le Microsoft.Uev.SyncController.exe qui se trouve dans le répertoire d’installation de l’agent UE-V.
**Remarque:** Comme pour la tâche **surveiller les paramètres** de l’application, cette tâche est exécutée lors de la connexion, mais elle est retardée de 30 secondes sans affecter la connexion.
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nom de la tâche</th>
<th align="left">Événement par défaut</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Application de contrôleur \Microsoft\UE-V\Sync</p></td>
<td align="left"><p>Connexion et toutes les 30 minutes</p></td>
</tr>
</tbody>
</table>

 

Par exemple, la commande suivante configure l’agent pour synchroniser les paramètres toutes les 15 minutes au lieu des 30 minutes par défaut.

``` syntax
Schtasks /change /tn “Microsoft\UE-V\Sync Controller Application” /ri 15
```

### Synchroniser les paramètres lors de la fermeture de session

La tâche **synchroniser les paramètres lors de la déconnexion** est utilisée pour démarrer une application lors de l’ouverture de session qui contrôle la synchronisation des applications lors de la fermeture de session pour UE-V. La tâche synchroniser les paramètres lors de la déconnexion exécute le fichier Microsoft.Uev.SyncController.exe situé dans le répertoire d’installation de l’agent UE-V.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nom de la tâche</th>
<th align="left">Événement par défaut</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Paramètres \Microsoft\UE-V\Synchronize à la fermeture de session</p></td>
<td align="left"><p>Accès</p></td>
</tr>
</tbody>
</table>

 

### Mise à jour automatique de modèle

La tâche de **mise à jour automatique de modèle** vérifie dans le catalogue de modèles de paramètres les modèles nouveaux, mis à jour ou supprimés. Cette tâche s’exécute uniquement si la SettingsTemplateCatalog est configurée. La tâche de **mise à jour automatique du modèle** exécute le fichier ApplySettingsCatalog.exe situé dans le répertoire d’installation de l’agent UE-V.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nom de la tâche</th>
<th align="left">Événement par défaut</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Mise à jour automatique \Microsoft\UE-V\Template</p></td>
<td align="left"><p>Démarrage système et à 3:30 AM tous les jours, à une heure aléatoire au sein d’une fenêtre d’une heure</p></td>
</tr>
</tbody>
</table>

 

**Par exemple:** La commande suivante configure l’agent UE-V pour vérifier le magasin de catalogues de modèles de paramètres chaque heure.

``` syntax
schtasks /change /tn "Microsoft\UE-V\Template Auto Update" /ri 60
```

### Télécharger les données du programme d’amélioration du produit

La tâche **Télécharger les données** du programme d’amélioration du produit s’exécute pendant l’installation si l’utilisateur ou l’administrateur a choisi de participer au programme d’amélioration du produit (CEIP). Cette tâche télécharge les données sur les serveurs du programme d’amélioration du produit dans lesquels les données sont utilisées pour améliorer le produit des futures versions d’UE-V. Cette tâche planifiée s’exécute à l’ouverture de session et toutes les 4 heures par la suite. La tâche Télécharger les données du programme d' **amélioration du produit** exécute le fichier UevSqmUploader.exe situé dans le répertoire d’installation de l’agent UE-V.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nom de la tâche</th>
<th align="left">Événement par défaut</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>\Microsoft\UE-V\Upload les données du programme d’amélioration du produit</p></td>
<td align="left"><p>Lors de l’ouverture de session et toutes les 4 heures</p></td>
</tr>
</tbody>
</table>

 

## UE-V 2-détails de la tâche planifiée


Le tableau suivant fournit des informations supplémentaires sur les tâches planifiées pour UE-V 2:

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Nom de la tâche </strong> (nom du fichier)</p></td>
<td align="left"><p><strong>Fréquence par défaut</strong></p></td>
<td align="left"><p><strong>Bascule d’alimentation</strong></p></td>
<td align="left"><p><strong>Inactif uniquement</strong></p></td>
<td align="left"><p><strong>Connexion réseau</strong></p></td>
<td align="left"><p><strong>Description</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Surveiller les paramètres </strong> de l’application (UevAppMonitor.exe)</p></td>
<td align="left"><p>Démarre 30 secondes après l’ouverture de session et continue jusqu’à la fin de la session.</p></td>
<td align="left"><p>Non</p></td>
<td align="left"><p>Oui</p></td>
<td align="left"><p>N/A</p></td>
<td align="left"><p>Synchronise les paramètres des applications Windows (AppX).</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Application de contrôleur </strong> de synchronisation (Microsoft.Uev.SyncController.exe)</p></td>
<td align="left"><p>À l’ouverture de session et toutes les 30 minutes ultérieures.</p></td>
<td align="left"><p>Oui</p></td>
<td align="left"><p>Oui</p></td>
<td align="left"><p>Uniquement si le réseau est connecté</p></td>
<td align="left"><p>Démarre le contrôleur de synchronisation qui synchronise les paramètres locaux avec l’emplacement de stockage des paramètres.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Synchroniser les paramètres lors de la fermeture </strong> de session (Microsoft.Uev.SyncController.exe)</p></td>
<td align="left"><p>S’exécute à l’ouverture de session, puis attend la fin de la synchronisation des paramètres.</p></td>
<td align="left"><p>Non</p></td>
<td align="left"><p>Oui</p></td>
<td align="left"><p>N/A</p></td>
<td align="left"><p>Démarrez une application lors de l’ouverture de session qui contrôle la synchronisation des applications lors de la fermeture de session.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Mise à jour automatique </strong> de modèle (ApplySettingsCatalog.exe)</p></td>
<td align="left"><p>S’exécute à l’ouverture de session initiale et à 3:30 AM par jour.</p></td>
<td align="left"><p>Oui</p></td>
<td align="left"><p>Non</p></td>
<td align="left"><p>N/A</p></td>
<td align="left"><p>Vérifie si le catalogue de modèles est nouveau, mis à jour ou supprimé. Cette tâche s’exécute uniquement si SettingsTemplateCatalog est configuré.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Collecter les données du programme d’amélioration du produit </strong> (UevSqmSession.exe)</p></td>
<td align="left"><p>Service de lancement d’ouverture de session</p></td>
<td align="left"><p>Non</p></td>
<td align="left"><p>Oui</p></td>
<td align="left"><p>N/A</p></td>
<td align="left"><p>Si l’utilisateur ou l’administrateur décide du programme d’amélioration du produit (CEIP), cette tâche collecte des données qui permettent d’améliorer les versions ultérieures d’UE-V.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Télécharger les données du programme d’amélioration du produit </strong> (UevSqmUploader.exe)</p></td>
<td align="left"><p>S’exécute à l’ouverture de session et à 4:00 AM par jour.</p></td>
<td align="left"><p>Non</p></td>
<td align="left"><p>Oui</p></td>
<td align="left"><p>Uniquement si le réseau est connecté</p></td>
<td align="left"><p>Si l’utilisateur ou l’administrateur décide du programme d’amélioration du produit (CEIP), cette tâche télécharge les données vers les serveurs CEIP.</p></td>
</tr>
</tbody>
</table>

 

**Légende**

-   **Bascule d’alimentation** – le planificateur de tâches optimise la consommation d’énergie quand il n’est pas connecté à une alimentation ca. L’exécution de la tâche risque de ne pas fonctionner si l’ordinateur bascule sur batterie.

-   **Inactif uniquement** : la tâche ne s’exécute pas si l’ordinateur cesse d’être inactif. Par défaut, la tâche ne redémarrera pas lorsque l’ordinateur sera inactif de nouveau. Au lieu de cela, la tâche redémarrera sur le déclencheur de tâche suivant.

-   **Connexion réseau** : les tâches marquées sur «Oui» s’exécutent uniquement si une connexion réseau est disponible sur l’ordinateur. Les tâches marquées «N/A» s’exécutent indépendamment de la connectivité réseau.

### Comment gérer les tâches planifiées

Pour rechercher des tâches planifiées, procédez comme suit:

1.  Ouvrez «planifier les tâches» sur l’ordinateur de l’utilisateur.

2.  Naviguez jusqu’à: planificateur de tâches- &gt; bibliothèque du planificateur de tâches- &gt; Microsoft- &gt; UE-V

3.  Sélectionnez la tâche planifiée que vous voulez gérer et configurer dans le volet Détails.

### Informations complémentaires

Les informations supplémentaires suivantes s’appliquent aux tâches planifiées UE-V:

-   les programmes de séquence de tâches se trouvent dans le dossier d’installation de l’agent UE-V, par `%programFiles%\Microsoft User Experience Virtualization\Agent\[architecture]\` défaut.

-   La tâche planifiée de l’application du contrôleur de synchronisation est le composant essentiel lorsque UE-V PowerSchool est défini sur "SyncProvider" (UE-V 2 Configuration par défaut). Cette tâche planifiée conserve les SettingsSToragePath synchronisés avec les versions mises en cache localement des fichiers du package de paramètres. Si les utilisateurs se plaignent que les paramètres ne sont pas synchronisés assez souvent, vous pouvez réduire le paramètre de tâche planifiée à 1 minute.Vous pouvez également augmenter la valeur par défaut de 30 minutes, si nécessaire. Si les utilisateurs se plaignent que les paramètres ne sont pas synchronisés assez rapidement lors de l’ouverture de session, vous pouvez supprimer le paramètre de délai pour la tâche planifiée. (Vous pouvez trouver le paramètre de délai dans la boîte de dialogue **modifier le déclencheur** )

-   Vous n’avez pas besoin de désactiver la tâche planifiée de mise à jour automatique de modèle si vous utilisez une autre méthode pour synchroniser les modèles des clients (c’est-à-dire les plannings de référence de la stratégie de groupe ou du gestionnaire de configuration). Si la valeur de la propriété SettingsTemplateCatalog n’est pas spécifiée, vous ne parvient pas à UE-V pour vérifier les modèles personnalisés dans le catalogue des paramètres. Cette tâche planifiée exécute ApplySettingsCatalog.exe et renverra essentiellement immédiatement.

-   La tâche planifiée des paramètres d’application vous permet de mettre à jour les paramètres de l’application Windows (AppX) en temps réel, en fonction des déclencheurs de paramètres du programme d’application Windows intégrés dans chaque application.






## Rubriques connexes


[Administration d’UE-V 2. x](administering-ue-v-2x-new-uevv2.md)

[Déployer UE-V 2. x pour des applications personnalisées](deploy-ue-v-2x-for-custom-applications-new-uevv2.md#deploycatalogue)

 

 





