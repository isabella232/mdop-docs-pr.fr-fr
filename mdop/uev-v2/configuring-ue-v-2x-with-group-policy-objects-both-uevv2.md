---
title: Configuration d’UE-V 2. x avec des objets de stratégie de groupe
description: Configuration d’UE-V 2. x avec des objets de stratégie de groupe
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
ms.openlocfilehash: bdff63b948752b9bec83e77e275f1cb20a384463
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810547"
---
# Configuration d’UE-V 2. x avec des objets de stratégie de groupe


Certains paramètres de la stratégie de groupe Microsoft User performance (UE-V) 2,0, 2,1 et 2,1 SP1 peuvent être définis pour les ordinateurs, et les autres paramètres de stratégie de groupe pour les utilisateurs. Pour plus d’informations sur l’installation des fichiers ADMX de stratégie de groupe UE-v, voir [installation des modèles ADMX de stratégie de groupe UE-v 2](https://technet.microsoft.com/library/dn458891.aspx#admx).

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
<th align="left">Description du paramètre de stratégie de groupe</th>
<th align="left">Options de configuration</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Texte du lien Contactez-le</p></td>
<td align="left"><p>Ordinateurs uniquement</p></td>
<td align="left"><p>Ce paramètre de stratégie de groupe spécifie le texte du lien hypertexte d’URL de contact dans le centre de paramètres de l’entreprise.</p></td>
<td align="left"><p>Si vous activez ce paramètre de stratégie de groupe, le centre de paramètres de la société affiche le texte spécifié dans le lien vers l’URL du contact.</p></td>
</tr>
<tr class="even">
<td align="left"><p>URL de contact</p></td>
<td align="left"><p>Ordinateurs uniquement</p></td>
<td align="left"><p>Ce paramètre de stratégie de groupe spécifie l’URL du lien de contact dans le centre de paramètres de la société.</p></td>
<td align="left"><p>Si vous activez ce paramètre, le centre de paramètres de la société adresse le lien vers l’URL spécifiée. Le lien peut être de n’importe quel protocole standard, tel que HTTP ou mailto.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Ne pas utiliser le fournisseur de synchronisation</p></td>
<td align="left"><p>Ordinateurs et utilisateurs</p></td>
<td align="left"><p>En utilisant ce paramètre de stratégie de groupe, vous pouvez configurer le fait que UE-V utilise la fonctionnalité du fournisseur de synchronisation. Ce paramètre de stratégie vous permet également d’activer la notification lorsque l’importation des paramètres utilisateur est retardée.</p></td>
<td align="left"><p>Activez ce paramètre pour configurer l’agent UE-V de façon à ce qu’il ne fasse pas appel au fournisseur de synchronisation.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Notification d’utilisation initiale</p></td>
<td align="left"><p>Ordinateurs uniquement</p></td>
<td align="left"><p>Ce paramètre de stratégie de groupe permet de notifier dans la zone de notification qui s’affiche lorsque UE-V</p>
<p>l’agent s’exécute pour la première fois.</p></td>
<td align="left"><p>La valeur par défaut est activée.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Paramètres des fenêtres itinérantes</p></td>
<td align="left"><p>Ordinateurs et utilisateurs</p></td>
<td align="left"><p>Ce paramètre de stratégie de groupe configure la synchronisation des paramètres Windows.</p></td>
<td align="left"><p>Sélectionnez les paramètres Windows à synchroniser entre les ordinateurs.</p>
<p>Par défaut, les thèmes Windows, les paramètres de bureau et les options d’ergonomie synchronisent les paramètres entre les ordinateurs de la même version du système d’exploitation.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Seuil d’avertissement de taille de package paramètres</p></td>
<td align="left"><p>Ordinateurs et utilisateurs</p></td>
<td align="left"><p>Ce paramètre de stratégie de groupe vous permet de configurer l’agent UE-V pour signaler l’arrivée d’un seuil défini pour la taille du fichier de package de paramètres.</p></td>
<td align="left"><p>Spécifiez le seuil préféré pour les tailles de packages de paramètres en kilo-octets (Ko).</p>
<p>Par défaut, l’agent UE-V n’a pas de seuil de taille de fichier de package.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Emplacement de stockage des paramètres</p></td>
<td align="left"><p>Ordinateurs et utilisateurs</p></td>
<td align="left"><p>Ce paramètre de stratégie de groupe permet de configurer l’emplacement de stockage des paramètres utilisateur.</p></td>
<td align="left"><p>Entrez le chemin d’accès UNC (Universal Naming Convention) et les variables comme \Server\SettingsShare%username%.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Chemin du catalogue de modèles de paramètres</p></td>
<td align="left"><p>Ordinateurs uniquement</p></td>
<td align="left"><p>Ce paramètre de stratégie de groupe permet de configurer l’emplacement de stockage des modèles d’emplacement des paramètres personnalisés. Ce paramètre de stratégie définit également si le catalogue doit être utilisé pour remplacer les modèles Microsoft par défaut installés avec l’agent UE-V.</p></td>
<td align="left"><p>Entrez un chemin d’accès UNC (Universal Naming Convention) tel que \Server\TemplateShare ou un dossier sur l’ordinateur.</p>
<p>Activez la case à cocher pour remplacer les modèles Microsoft par défaut.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Paramètres de synchronisation sur les connexions limitées</p></td>
<td align="left"><p>Ordinateurs et utilisateurs</p></td>
<td align="left"><p>Ce paramètre de stratégie de groupe définit si UE-V synchronise les paramètres de connexions limitées.</p></td>
<td align="left"><p>Par défaut, l’agent UE-V ne synchronise pas les paramètres sur une connexion limitée.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Paramètres de synchronisation sur les connexions limitées, même en cas d’itinérance</p></td>
<td align="left"><p>Ordinateurs et utilisateurs</p></td>
<td align="left"><p>Ce paramètre de stratégie de groupe définit si UE-V synchronise les paramètres de connexions limitées en dehors du réseau des fournisseurs de réseaux domestiques, par exemple lorsque la connexion de données est en mode itinérant.</p></td>
<td align="left"><p>Par défaut, UE-V ne synchronise pas les paramètres sur une connexion limitée lorsqu’il est en mode itinérant.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Délai d’expiration de la synchronisation</p></td>
<td align="left"><p>Ordinateurs et utilisateurs</p></td>
<td align="left"><p>Ce paramètre de stratégie de groupe configure le nombre de millisecondes avant qu’il n’expire lors de la récupération des paramètres utilisateur à partir de l’emplacement des paramètres distants. Si l’emplacement de stockage à distance n’est pas disponible et que l’utilisateur n’utilise pas le fournisseur de synchronisation, le démarrage de l’application est retardée de ce nombre de millisecondes.</p></td>
<td align="left"><p>Spécifiez le délai d’expiration de la synchronisation par défaut en millisecondes. La valeur par défaut est 2000 millisecondes.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Icône de la barre d’état système</p></td>
<td align="left"><p>Ordinateurs uniquement</p></td>
<td align="left"><p>Ce paramètre de stratégie de groupe permet de l’icône de la barre d’état utilisateur de la virtualisation.</p></td>
<td align="left"><p>La valeur par défaut est activée.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Utiliser la virtualisation de l’utilisation de l’utilisateur (UE-V)</p></td>
<td align="left"><p>Ordinateurs et utilisateurs</p></td>
<td align="left"><p>Ce paramètre de stratégie de groupe vous permet d’activer ou de désactiver la virtualisation de l’utilisation de l’utilisateur.</p></td>
<td align="left"><p>Activez ou désactivez ce paramètre de stratégie de groupe.</p></td>
</tr>
</tbody>
</table>

 

**Remarques**  De plus, les paramètres de stratégie de groupe sont disponibles pour de nombreuses applications de bureau et applications Windows. Vous pouvez utiliser ces paramètres pour activer ou désactiver la synchronisation des paramètres pour des applications spécifiques.

 

**Paramètres de stratégie de groupe des applications Windows**

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
<th align="left">Description du paramètre de stratégie de groupe</th>
<th align="left">Options de configuration</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Ne pas synchroniser les applications Windows</p></td>
<td align="left"><p>Ordinateurs et utilisateurs</p></td>
<td align="left"><p>Ce paramètre de stratégie de groupe définit si UE-V agent synchronise les paramètres des applications Windows.</p></td>
<td align="left"><p>La valeur par défaut consiste à synchroniser les applications Windows.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Liste des applications Windows</p></td>
<td align="left"><p>Ordinateur et utilisateur</p></td>
<td align="left"><p>Ce paramètre dresse la liste des noms de famille de packages des applications Windows et indique expressément si UE-V synchronise les paramètres de l’application.</p></td>
<td align="left"><p>Vous pouvez utiliser ce paramètre pour spécifier que les paramètres d’une application ne sont jamais synchronisés par UE-V, même si les paramètres de toutes les autres applications Windows sont synchronisés.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Synchroniser les applications Windows non répertoriées</p></td>
<td align="left"><p>Ordinateur et utilisateur</p></td>
<td align="left"><p>Ce paramètre de stratégie de groupe définit le comportement de synchronisation des paramètres par défaut de l’agent UE-V pour les applications Windows qui ne figurent pas explicitement dans la liste des applications Windows.</p></td>
<td align="left"><p>Par défaut, l’agent UE-V synchronise uniquement les paramètres des applications Windows qui sont incluses dans la liste des applications Windows.</p></td>
</tr>
</tbody>
</table>

 

Pour plus d’informations sur la synchronisation des applications Windows, voir [liste des applications Windows](https://technet.microsoft.com/library/dn458925.aspx#win8applist).

**Pour configurer les paramètres de stratégie de groupe ciblés par l’ordinateur**

1.  Utilisez la console de gestion des stratégies de groupe (GPMC) ou la gestion avancée des stratégies de groupe (AGPM) sur l’ordinateur qui sert de contrôleur de domaine pour gérer les paramètres de stratégie de groupe pour les ordinateurs UE-V. Accédez à **Configuration ordinateur**, sélectionnez **stratégies**, **modèles d’administration**, cliquez sur **composants Windows**, puis sélectionnez **virtualisation**de l’utilisation de Microsoft.

2.  Sélectionnez le paramètre de stratégie de groupe que vous voulez modifier.

**Pour configurer les paramètres de stratégie de groupe ciblés par l’utilisateur**

1.  Utilisez la console de gestion des stratégies de groupe (GPMC) ou l’outil de gestion des stratégies de groupe (AGPM) dans Microsoft Desktop Optimization Pack (MDOP) sur l’ordinateur contrôleur de domaine pour gérer les paramètres de stratégie de groupe pour UE-V. Accédez à **Configuration utilisateur**, sélectionnez **stratégies**, sélectionnez **modèles d’administration**, cliquez sur **composants Windows**, puis sélectionnez virtualisation de l' **utilisation de Microsoft**.

2.  Sélectionnez le paramètre de stratégie de groupe modifié.

L’agent UE-V utilise l’ordre de priorité suivant pour déterminer la synchronisation.

**Ordre de priorité pour les paramètres d’UE-V**

1.  Paramètres ciblés par l’utilisateur, gérés par des paramètres de stratégie de groupe, ces paramètres de configuration sont stockés dans la clé de Registre par la stratégie de groupe `HKEY_CURRENT_USER\Software\Policies\Microsoft\Uev\Agent\Configuration` .

2.  Paramètres ciblés par ordinateur gérés par des paramètres de stratégie de groupe: ces paramètres de configuration sont stockés dans la clé de Registre par la stratégie de groupe `HKEY_LOCAL_MACHINE\Software\Policies\Microsoft\Uev\Agent\Configuration` .

3.  Paramètres de configuration définis par l’utilisateur actuel à l’aide de Windows PowerShell ou de Windows Management Instrumentation (WMI)-ces paramètres de configuration sont stockés par l’agent UE-V sous cet emplacement du Registre: `HKEY_CURRENT_USER\Software\Microsoft\Uev\Agent\Configuration` .

4.  Paramètres de configuration définis pour l’ordinateur à l’aide de Windows PowerShell ou WMI. Ces paramètres de configuration sont stockés par l’agent UE-V sous cet emplacement du Registre: `HKEY_LOCAL_MACHINE\Software\Microsoft\Uev\Agent\Configuration` .

    Vous **avez une suggestion pour UE-V**? Ajoutez ou Votez en fonction [de suggestions.](http://uev.uservoice.com/forums/280428-microsoft-user-experience-virtualization) Vous **avez un problème UE-V**? Utiliser le [Forum de TechNet UE-V](https://social.technet.microsoft.com/Forums/home?forum=mdopuev).

## Rubriques connexes


[Administration d’UE-V 2. x](administering-ue-v-2x-new-uevv2.md)

[Gérer les configurations pour UE-V2.x](manage-configurations-for-ue-v-2x-new-uevv2.md)

 

 





