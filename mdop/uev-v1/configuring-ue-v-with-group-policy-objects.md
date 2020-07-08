---
title: Configuration d’UE-V avec les objets de stratégie de groupe
description: Configuration d’UE-V avec les objets de stratégie de groupe
author: dansimp
ms.assetid: 5c9be706-a05f-4397-9a38-e6b73ebff1e5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7e479e6bef1a2b38cf822ffca19ed4220b0c59fe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811910"
---
# Configuration d’UE-V avec les objets de stratégie de groupe


Certains paramètres de stratégie de groupe de Microsoft User performance (UE-V) peuvent être définis pour les ordinateurs et d’autres pour les utilisateurs. UE-V les paramètres de stratégie de configuration de l’agent peuvent être définis pour des ordinateurs ou des utilisateurs. Pour plus d’informations sur l’installation des fichiers ADMX de stratégie de groupe UE-V, voir [installation des modèles ADMX de stratégie de groupe UE-v](installing-the-ue-v-group-policy-admx-templates.md).

Les paramètres de stratégie suivants peuvent être configurés pour UE-V:

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Nom du paramètre de stratégie</strong></p></td>
<td align="left"><p><strong>Target</strong></p></td>
<td align="left"><p><strong>Description du paramètre de stratégie</strong></p></td>
<td align="left"><p><strong>Options de configuration</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>Utiliser la virtualisation de l’utilisation de l’utilisateur (UE-V)</p></td>
<td align="left"><p>Ordinateurs et utilisateurs</p></td>
<td align="left"><p>Ce paramètre de stratégie vous permet d’activer ou de désactiver la virtualisation de l’utilisation de l’utilisateur.</p></td>
<td align="left"><p>Activez ou désactivez ce paramètre de stratégie.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Emplacement de stockage des paramètres</p></td>
<td align="left"><p>Ordinateurs et utilisateurs</p></td>
<td align="left"><p>Ce paramètre de stratégie permet de configurer l’emplacement de stockage des paramètres utilisateur.</p></td>
<td align="left"><p>Spécifiez un chemin d’accès UNC (Universal Naming Convention) et des variables (par exemple, \Server\SettingsShare%username%.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Chemin du catalogue de modèles de paramètres</p></td>
<td align="left"><p>Ordinateurs uniquement</p></td>
<td align="left"><p>Ce paramètre de stratégie configure l’emplacement de stockage des modèles d’emplacement des paramètres personnalisés. Ce paramètre de stratégie configure également si le catalogue est utilisé pour remplacer les modèles Microsoft par défaut installés avec l’agent UE-V.</p></td>
<td align="left"><p>Fournissez un chemin UNC (Universal Naming Convention) tel que \Server\TemplateShare ou un dossier sur l’ordinateur.</p>
<p></p>
<p>Activez la case à cocher pour remplacer les modèles Microsoft par défaut.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Ne pas utiliser de fichiers hors connexion</p></td>
<td align="left"><p>Ordinateurs et utilisateurs</p></td>
<td align="left"><p>Ce paramètre de stratégie vous permet de configurer l’utilisation de la fonctionnalité fichiers en mode hors connexion de Windows pour UE-V. Ce paramètre de stratégie vous permet également d’activer la notification lorsque l’importation des paramètres utilisateur est retardée.</p></td>
<td align="left"><p>Pour configurer l’agent UE-V de façon à ne pas utiliser de fichiers hors connexion, activez ce paramètre.</p>
<p></p>
<p>Spécifiez si les notifications doivent être fournies lorsque l’importation des paramètres est retardée.</p>
<p></p>
<p>Spécifiez la durée en secondes d’attente avant l’affichage de la notification.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Délai d’expiration de la synchronisation</p></td>
<td align="left"><p>Ordinateurs et utilisateurs</p></td>
<td align="left"><p>Ce paramètre de stratégie configure le nombre de millisecondes que l’ordinateur attend avant un délai d’expiration lors de la récupération des paramètres utilisateur à partir de l’emplacement des paramètres distants. Si l’emplacement de stockage à distance n’est pas disponible, le lancement de l’application est retardée de ce nombre de millisecondes.</p></td>
<td align="left"><p>Spécifiez le délai d’expiration de la synchronisation préféré, en millisecondes. Valeur par défaut de 2000 millisecondes.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Seuil d’avertissement de taille de package</p></td>
<td align="left"><p>Ordinateurs et utilisateurs</p></td>
<td align="left"><p>Ce paramètre de stratégie vous permet de configurer l’agent UE-V pour signaler l’arrivée d’un seuil défini pour la taille du fichier de package de paramètres.</p></td>
<td align="left"><p>Spécifié le seuil préféré pour les tailles de packages de paramètres en kilo-octets.</p>
<p>Par défaut, l’agent UE-V n’a pas de seuil de taille de fichier de package.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Paramètres d’application itinérante</p></td>
<td align="left"><p>Utilisateurs uniquement</p></td>
<td align="left"><p>Ce paramètre de stratégie configure l’itinérance des paramètres utilisateur des applications.</p></td>
<td align="left"><p>Sélectionnez les paramètres Windows qui seront itinérants entre les ordinateurs.</p>
<p>Par défaut, les paramètres utilisateur des applications avec le modèle de paramètres fourni par UE-V sont itinérants entre les ordinateurs.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Paramètres de Windows en itinérance</p></td>
<td align="left"><p>Utilisateurs uniquement</p></td>
<td align="left"><p>Ce paramètre de stratégie configure l’itinérance des paramètres Windows.</p></td>
<td align="left"><p>Sélectionner les applications qui peuvent être déplacées entre les ordinateurs.</p>
<p>Par défaut, les thèmes Windows sont itinérants entre les ordinateurs de la même version du système d’exploitation. Les paramètres de bureau Windows et les options d’ergonomie ne sont pas itinérants.</p></td>
</tr>
</tbody>
</table>

 

**Pour configurer des stratégies ciblées par l’ordinateur**

1.  Utilisez la console de gestion des stratégies de groupe (GPMC) ou la gestion avancée des stratégies de groupe (AGPM) sur l’ordinateur contrôleur de domaine qui gère la stratégie de groupe pour les ordinateurs UE-V. Accédez à **Configuration ordinateur**, sélectionnez **stratégies**, **modèles d’administration**, cliquez sur **composants Windows**, puis sélectionnez **virtualisation**de l’utilisation de Microsoft.

2.  Sélectionnez le paramètre de stratégie à modifier.

**Pour configurer des stratégies ciblées par l’utilisateur**

1.  Servez-vous de la console de gestion des stratégies de groupe (GPMC) ou de l’outil de gestion des stratégies de groupe (AGPM) dans Microsoft Desktop Optimization Pack Accédez à **Configuration utilisateur**, sélectionnez **stratégies**, sélectionnez **modèles d’administration**, cliquez sur **composants Windows**, puis sélectionnez virtualisation de l' **utilisation de Microsoft**.

2.  Sélectionnez le paramètre de stratégie modifié.

L’agent UE-V utilise l’ordre de priorité suivant pour déterminer la synchronisation.

**Ordre de priorité pour les paramètres d’UE-V**

1.  Paramètres ciblés par l’utilisateur gérés par une stratégie de groupe: ces paramètres de configuration sont stockés dans la clé de Registre par la stratégie de groupe `HKEY_CURRENT_USER\Software\Policies\Microsoft\Uev\Agent\Configuration` .

2.  Paramètres de l’ordinateur gérés par une stratégie de groupe: ces paramètres de configuration sont stockés dans la clé de Registre par la stratégie de groupe `HKEY_LOCAL_MACHINE\Software\Policies\Microsoft\Uev\Agent\Configuration` .

3.  Paramètres de configuration définis par l’utilisateur actuel à l’aide de PowerShell ou WMI; ces paramètres de configuration sont stockés par l’agent UE-V sous cet emplacement du Registre: `HKEY_CURRENT_USER\Software\Microsoft\Uev\Agent\Configuration` .

4.  Paramètres de configuration définis pour l’ordinateur utilisant PowerShell ou WMI. Ces paramètres de configuration sont stockés par l’agent UE-V sous le `HKEY_LOCAL_MACHINE \Software\Microsoft\Uev\Agent\Configuration` .

## Rubriques connexes


[Administration d'UE-V1.0](administering-ue-v-10.md)

[Opérations d'UE-V1.0](operations-for-ue-v-10.md)

 

 





