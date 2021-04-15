---
title: Configuration d'UE-V 2.x avec des objets de stratégie de groupe
description: Configuration d'UE-V 2.x avec des objets de stratégie de groupe
author: dansimp
ms.assetid: 2bb55834-26ee-4f19-9860-dfdf3c797143
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b6c9636df36a53cbf65bf1904965f2809484b99c
ms.sourcegitcommit: bdc377477a8cc9e973fbcdd67c2f07b882c5d61e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2021
ms.locfileid: "11494059"
---
# <a name="configuring-ue-v-2x-with-group-policy-objects"></a>Configuration d'UE-V 2.x avec des objets de stratégie de groupe


Certains paramètres de stratégie de groupe Microsoft User Experience Virtualization (UE-V) 2.0, 2.1 et 2.1 SP1 peuvent être définis pour les ordinateurs, et d'autres paramètres de stratégie de groupe pour les utilisateurs. Pour plus d'informations sur l'installation des fichiers ADMX de stratégie de groupe UE-V, voir l'installation des modèles ADMX de stratégie de groupe [UE-V 2.](https://technet.microsoft.com/library/dn458891.aspx#admx)

Les paramètres de stratégie suivants peuvent être configurés pour UE-V.

**Paramètres de stratégie de groupe**

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nom du paramètre de stratégie de groupe</th>
<th align="left">Target</th>
<th align="left">Description des paramètres de stratégie de groupe</th>
<th align="left">Options de configuration</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Configurer la méthode sync</p></td>
<td align="left"><p>Ordinateurs et utilisateurs</p></td>
<td align="left"><p>À l'aide de ce paramètre de stratégie de groupe, vous pouvez configurer si User Experience Virtualization (UE-V) utilise la fonctionnalité de fournisseur de synchronisation. Ce paramètre de stratégie vous permet également d'activer l'apparition d'une notification lorsque l'importation des paramètres utilisateur est retardée.</p></td>
<td align="left"><p>Activez ce paramètre pour configurer l'agent UE-V afin de ne pas utiliser le fournisseur de synchronisation ou le moteur de synchronisation externe.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Contact IT Link Text</p></td>
<td align="left"><p>Ordinateurs uniquement</p></td>
<td align="left"><p>Ce paramètre de stratégie de groupe spécifie le texte du lien hypertexte de l'URL du contact it dans le Centre de paramètres de l'entreprise.</p></td>
<td align="left"><p>Si vous activez ce paramètre de stratégie de groupe, le Centre de paramètres d'entreprise affiche le texte spécifié dans le lien vers l'URL du contact it.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Contact IT URL</p></td>
<td align="left"><p>Ordinateurs uniquement</p></td>
<td align="left"><p>Ce paramètre de stratégie de groupe spécifie l'URL du lien Contact IT dans le Centre de paramètres de l'entreprise.</p></td>
<td align="left"><p>Si vous activez ce paramètre, le Centre de paramètres d’entreprise contacte le texte it vers l’URL spécifiée. Le lien peut être de n’importe quel protocole standard, tel que HTTP ou mailto.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Notification de première utilisation</p></td>
<td align="left"><p>Ordinateurs uniquement</p></td>
<td align="left"><p>Ce paramètre de stratégie de groupe active une notification dans la zone de notification qui s’affiche lorsque l’UE-V</p>
<p>s’exécute pour la première fois.</p></td>
<td align="left"><p>La valeur par défaut est activée.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Ping sur l’emplacement de stockage des paramètres avant synchronisation</p></td>
<td align="left"><p>Ordinateurs et utilisateurs</p></td>
<td align="left"><p>Ce paramètre de stratégie permet à la configuration du fournisseur de synchronisation UE-V d’envoyer un ping sur le chemin de stockage des paramètres avant de tenter de synchroniser les paramètres afin de vérifier la connexion.</p></td>
<td align="left"><p>Activez ou désactivez ce paramètre de stratégie de groupe.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Seuil d’avertissement de taille de package Paramètres</p></td>
<td align="left"><p>Ordinateurs et utilisateurs</p></td>
<td align="left"><p>Ce paramètre de stratégie de groupe vous permet de configurer l’agent UE-V pour signaler quand la taille d’un fichier de package de paramètres atteint un seuil défini.</p></td>
<td align="left"><p>Spécifiez le seuil préféré pour les tailles de package de paramètres en kilo-octets (Ko).</p>
<p>Par défaut, l’agent UE-V n’a pas de seuil de taille de fichier de package.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Chemin de stockage des paramètres</p></td>
<td align="left"><p>Ordinateurs et utilisateurs</p></td>
<td align="left"><p>Ce paramètre de stratégie de groupe configure l’endroit où les paramètres utilisateur doivent être stockés.</p></td>
<td align="left"><p>Entrez un chemin d’accès UNC (Universal Naming Convention) et des variables telles que \Server\SettingsShare%username%.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Chemin d’accès du catalogue de modèles de paramètres</p></td>
<td align="left"><p>Ordinateurs uniquement</p></td>
<td align="left"><p>Ce paramètre de stratégie de groupe configure l’emplacement des modèles d’emplacement des paramètres personnalisés. Ce paramètre de stratégie configure également si le catalogue doit être utilisé pour remplacer les modèles Microsoft par défaut installés avec l’agent UE-V.</p></td>
<td align="left"><p>Entrez un chemin d’accès UNC (Universal Naming Convention) tel que \Server\TemplateShare ou un emplacement de dossier sur l’ordinateur.</p>
<p>Cochez la case pour remplacer les modèles Microsoft par défaut.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Paramètres de synchronisation sur les connexions à connexions avec des compteurs</p></td>
<td align="left"><p>Ordinateurs et utilisateurs</p></td>
<td align="left"><p>Ce paramètre de stratégie de groupe définit si UE-V synchronise les paramètres sur les connexions à connexions avec jauge.</p></td>
<td align="left"><p>Par défaut, l’agent UE-V ne synchronise pas les paramètres sur une connexion à connexion sécurisée.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Synchroniser les paramètres sur les connexions avec des compteurs, même en itinérance</p></td>
<td align="left"><p>Ordinateurs et utilisateurs</p></td>
<td align="left"><p>Ce paramètre de stratégie de groupe définit si UE-V synchronise les paramètres sur les connexions à connexions avec des compteurs en dehors du réseau du fournisseur d’accueil, par exemple, lorsque la connexion de données est en mode d’itinérance.</p></td>
<td align="left"><p>Par défaut, UE-V ne synchronise pas les paramètres sur une connexion avec mesure lorsqu’il est en mode d’itinérance.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Délai d’délai de synchronisation</p></td>
<td align="left"><p>Ordinateurs et utilisateurs</p></td>
<td align="left"><p>Ce paramètre de stratégie de groupe configure le nombre de millisecondes que l’ordinateur attend avant un délai d’attente lorsqu’il récupère les paramètres utilisateur à partir de l’emplacement des paramètres distants. Si l’emplacement de stockage distant n’est pas disponible et que l’utilisateur n’utilise pas le fournisseur de synchronisation, le démarrage de l’application est retardé de ce nombre de millisecondes.</p></td>
<td align="left"><p>Spécifiez le délai d’délai de synchronisation préféré en millisecondes. La valeur par défaut est 2 000 millisecondes.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Synchroniser les paramètres Windows </p></td>
<td align="left"><p>Ordinateurs et utilisateurs</p></td>
<td align="left"><p>Ce paramètre de stratégie de groupe configure la synchronisation des paramètres Windows.</p></td>
<td align="left"><p>Sélectionnez les paramètres Windows synchronisés entre les ordinateurs.</p>
<p>Par défaut, les thèmes Windows, les paramètres de bureau et les paramètres d’accessibilité synchronisent les paramètres entre les ordinateurs de la même version du système d’exploitation.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Icône Tray</p></td>
<td align="left"><p>Ordinateurs uniquement</p></td>
<td align="left"><p>Ce paramètre de stratégie de groupe active l’icône de bac UE-V.</p></td>
<td align="left"><p>La valeur par défaut est activée.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Utiliser User Experience Virtualization (UE-V)</p></td>
<td align="left"><p>Ordinateurs et utilisateurs</p></td>
<td align="left"><p>Ce paramètre de stratégie de groupe vous permet d’activer ou de désactiver UE-V.</p></td>
<td align="left"><p>Activez ou désactivez ce paramètre de stratégie de groupe.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>VDI Configuration</p></td>
<td align="left"><p>Ordinateurs et utilisateurs</p></td>
<td align="left"><p>Ce paramètre de stratégie configure la synchronisation des informations de récupération UE-V pour les ordinateurs qui s’exécutent dans un environnement VDI en pool. Si cette stratégie est activée, l’état de restauration UE-V est copié sur l’emplacement de stockage des paramètres lors de la connexion et restauré lors de la connexion.</p></td>
<td align="left"><p>Activez ou désactivez ce paramètre de stratégie de groupe.</p></td>
</tr>
</tbody>
</table>

 

**Remarque**  
En outre, les paramètres de stratégie de groupe sont disponibles pour de nombreuses applications de bureau et applications Windows. Vous pouvez utiliser ces paramètres pour activer ou désactiver la synchronisation des paramètres pour des applications spécifiques.

 

**Paramètres de stratégie de groupe Des applications Windows**

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nom du paramètre de stratégie de groupe</th>
<th align="left">Target</th>
<th align="left">Description des paramètres de stratégie de groupe</th>
<th align="left">Options de configuration</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Ne pas synchroniser les applications Windows</p></td>
<td align="left"><p>Ordinateurs et utilisateurs</p></td>
<td align="left"><p>Ce paramètre de stratégie de groupe définit si l'agent UE-V synchronise les paramètres des applications Windows.</p></td>
<td align="left"><p>La valeur par défaut consiste à synchroniser les applications Windows.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Liste des applications Windows</p></td>
<td align="left"><p>Ordinateur et utilisateur</p></td>
<td align="left"><p>Ce paramètre répertorie les noms de package de famille des applications Windows et indique expressément si UE-V synchronise les paramètres de cette application.</p></td>
<td align="left"><p>Vous pouvez utiliser ce paramètre pour spécifier que les paramètres d'une application ne sont jamais synchronisés par UE-V, même si les paramètres de toutes les autres applications Windows sont synchronisés.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Synchroniser les applications Windows non listées</p></td>
<td align="left"><p>Ordinateur et utilisateur</p></td>
<td align="left"><p>Ce paramètre de stratégie de groupe définit le comportement de synchronisation des paramètres par défaut de l'agent UE-V pour les applications Windows qui ne sont pas explicitement répertoriées dans la liste des applications Windows.</p></td>
<td align="left"><p>Par défaut, l'agent UE-V synchronise uniquement les paramètres des applications Windows incluses dans la liste des applications Windows.</p></td>
</tr>
</tbody>
</table>

 

Pour plus d'informations sur la synchronisation des applications Windows, voir [Liste des applications Windows.](https://technet.microsoft.com/library/dn458925.aspx#win8applist)

**Pour configurer les paramètres de stratégie de groupe ciblés par l'ordinateur**

1.  Utilisez la Console de gestion des stratégies de groupe (GPMC) ou la Gestion avancée des stratégies de groupe (AGPM) sur l'ordinateur qui agit en tant que contrôleur de domaine pour gérer les paramètres de stratégie de groupe pour les ordinateurs UE-V. Accédez **à Configuration ordinateur,** sélectionnez **Stratégies,** sélectionnez Modèles d'administration, cliquez sur **Composants Windows,** puis sélectionnez **Microsoft User Experience Virtualization**. ****

2.  Sélectionnez le paramètre de stratégie de groupe à modifier.

**Pour configurer les paramètres de stratégie de groupe ciblés par l'utilisateur**

1.  Utilisez la Console de gestion des stratégies de groupe (GPMC) ou l'outil Gestion avancée des stratégies de groupe (AGPM) dans Microsoft Desktop Optimization Pack (MDOP) sur l'ordinateur du contrôleur de domaine pour gérer les paramètres de stratégie de groupe pour UE-V. Accédez **à configuration utilisateur,** sélectionnez **Stratégies,** sélectionnez Modèles d'administration, cliquez sur **Composants Windows,** puis sélectionnez **Microsoft User Experience Virtualization**. ****

2.  Sélectionnez le paramètre de stratégie de groupe modifié.

L'agent UE-V utilise l'ordre de priorité suivant pour déterminer la synchronisation.

**Ordre de priorité pour les paramètres UE-V**

1.  Paramètres ciblés par l'utilisateur gérés par les paramètres de stratégie de groupe : ces paramètres de configuration sont stockés dans la clé de Registre par la stratégie de groupe sous `HKEY_CURRENT_USER\Software\Policies\Microsoft\Uev\Agent\Configuration` .

2.  Paramètres ciblés par l'ordinateur gérés par les paramètres de stratégie de groupe : ces paramètres de configuration sont stockés dans la clé de Registre par la stratégie de groupe sous `HKEY_LOCAL_MACHINE\Software\Policies\Microsoft\Uev\Agent\Configuration` .

3.  Paramètres de configuration définis par l'utilisateur actuel à l'aide de Windows PowerShell ou windows management Instrumentation (WMI) : ces paramètres de configuration sont stockés par l'agent UE-V sous cet emplacement de Registre : `HKEY_CURRENT_USER\Software\Microsoft\Uev\Agent\Configuration`

4.  Paramètres de configuration définis pour l'ordinateur à l'aide de Windows PowerShell ou WMI. Ces paramètres de configuration sont stockés par l'agent UE-V sous cet emplacement de Registre `HKEY_LOCAL_MACHINE\Software\Microsoft\Uev\Agent\Configuration` :

    **Vous avez une suggestion pour UE-V**? Ajoutez ou votez sur les suggestions [ici.](http://uev.uservoice.com/forums/280428-microsoft-user-experience-virtualization) **Vous avez un problème UE-V**? Utilisez le [forum TechNet UE-V.](https://social.technet.microsoft.com/Forums/home?forum=mdopuev)

## <a name="related-topics"></a>Rubriques connexes


[Administration d'UE-V 2.x](administering-ue-v-2x-new-uevv2.md)

[Gérer les configurations pour UE-V 2.x](manage-configurations-for-ue-v-2x-new-uevv2.md)

 

 
