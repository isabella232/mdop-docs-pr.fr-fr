---
title: Gestion des paramètres de configuration d'espace de travail MED-V
description: Gestion des paramètres de configuration d'espace de travail MED-V
author: dansimp
ms.assetid: 517d04de-c31f-4b50-b2b3-5f8c312ed37b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 97add695f605b71547b564789cce07a1d58763f2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811586"
---
# Gestion des paramètres de configuration d'espace de travail MED-V


Microsoft Enterprise Desktop Virtualization (MED-V) 2,0 enregistre ses paramètres de configuration dans le registre. Les informations que nous inclurons ici pour le registre peuvent vous aider à mieux gérer vos services MED-V.

MED-V utilise le chemin de recherche suivant pour rechercher les valeurs des paramètres résultants:

MED-V examine d’abord la stratégie de l’ordinateur.

Si la valeur est introuvable, MED-V effectue une recherche dans la stratégie de l’utilisateur.

Si la valeur est introuvable, MED-V effectue une recherche dans la ruche HKEY \ _LOCAL \ _MACHINE \\System.

Si la valeur est introuvable, MED-V effectue une recherche dans la ruche du registre de l’utilisateur HKEY \ _CURRENT.

Si la valeur est toujours introuvable, MED-V utilise la valeur par défaut.

Nous vous conseillons de définir la valeur dans la ruche HKEY \ _LOCAL \ _MACHINE \\System ou la stratégie de l’ordinateur. Toutefois, si vous voulez que l’utilisateur final puisse configurer un paramètre particulier, vous devez le laisser.

**Remarque**  
Avant de déployer vos espaces de travail MED-V, vous pouvez utiliser un éditeur de script pour modifier le script Windows PowerShell (fichier. ps1) créé par le gestionnaire de package MED-V. Pour plus d’informations, reportez-vous à [Configuration des paramètres avancés à l’aide de Windows PowerShell](configuring-advanced-settings-by-using-windows-powershell.md).

Après avoir déployé vos espaces de travail MED-V, vous pouvez modifier certains paramètres de configuration de MED-V en modifiant les entrées du Registre.



Cette section répertorie toutes les clés de Registre MED-V configurables et explique leur utilisation.

## Clé de diagnostic


Le tableau suivant fournit des informations sur les valeurs de Registre associées à la clé HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Medv\\v2\\Diagnostics.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nom </th>
<th align="left">Type </th>
<th align="left">Données/par défaut </th>
<th align="left">Description </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>EventLogLevel </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>Par défaut = 3</p></td>
<td align="left"><p>Type d’informations enregistrées dans le journal des événements. Les niveaux incluent les éléments suivants: 0 (aucun), 1 (erreur), 2 (avertissement), 3 (information), 4 (débogage).</p></td>
</tr>
</tbody>
</table>



## Clé FTS


Le tableau suivant fournit des informations sur les valeurs de Registre associées à la clé HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Medv\\v2\\Fts.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nom</th>
<th align="left">Type</th>
<th align="left">Données/par défaut</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>AddUserToAdminGroupEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Par défaut = 0</p></td>
<td align="left"><p>Configure la première fois que le programme d’installation ajoute automatiquement l’utilisateur final au groupe&#39;s administrateur. 0 = faux; 1 = vrai.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = faux: le programme d’installation pour la première fois n’ajoute pas automatiquement l’utilisateur final au groupe&#39;les administrateurs.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = vrai: le programme d’installation ajoute automatiquement l’utilisateur final au groupe&#39;s administrateur.</p></td>
</tr>
<tr class="even">
<td align="left"><p>ComputerNameMask </p></td>
<td align="left"><p>SZ</p></td>
<td align="left"><p>MEDV* </p></td>
<td align="left"><p>Le masque du nom de l’ordinateur utilisé pour créer l’ordinateur virtuel invité&#39;le nom de l’ordinateur.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>Le masque peut contenir une balise% username% pour insérer le nom d’utilisateur dans le nom de l’ordinateur. De même, la balise% hostname% insère le nom de l’ordinateur hôte.</p>
<p>Chaque &quot; # &quot; caractère du masque est remplacé par un chiffre aléatoire. Le caractère astérisque (*) à la fin du masque est remplacé par un caractère alphanumérique aléatoire.</p>
<p>Un nombre déterminé de caractères du nom d’utilisateur% et du nom d’utilisateur% peut être capturé à l’aide de crochets. Par exemple, &quot; % nom_utilisateur% [3] &quot; utilisera les trois premiers caractères du nom d’utilisateur.</p></td>
</tr>
<tr class="even">
<td align="left"><p>DeleteVMStateTimeout</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Valeur par défaut = 90</p></td>
<td align="left"><p>Valeur du délai d’expiration, en secondes, lors de la première tentative de configuration de l’ordinateur virtuel. Plage = 0 à 2147483647.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>DetachVfdTimeout</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Par défaut = 120</p></td>
<td align="left"><p>La valeur du délai d’expiration en secondes, lors de la première tentative de configuration de la disquette virtuelle de l’ordinateur virtuel. Plage = 0 à 2147483647.</p></td>
</tr>
<tr class="even">
<td align="left"><p>DialogUrl </p></td>
<td align="left"><p>SZ</p></td>
<td align="left"><p></p></td>
<td align="left"><p>URL personnalisable qui s’associe à la page Web interne et qui s’affiche lorsque vous affichez un message de boîte de dialogue pour la première fois. </p></td>
</tr>
<tr class="odd">
<td align="left"><p>ExplorerTimeout</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Par défaut = 900</p></td>
<td align="left"><p>Valeur du délai d’attente, en secondes, que le programme d’installation attend pour la première fois pour l’Explorateur Windows. Plage = 0 à 2147483647.</p></td>
</tr>
<tr class="even">
<td align="left"><p>FailureDialogMsg </p></td>
<td align="left"><p>MULTI_SZ</p></td>
<td align="left"><p>Le message est disponible dans le fichier de ressources </p></td>
<td align="left"><p>Message personnalisable qui s’affiche à l’utilisateur final lorsque le programme ne peut pas être exécuté pour la première fois.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>GiveUserGroupRightsMaxRetryCount </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>Par défaut = 3</p></td>
<td align="left"><p>Le nombre maximal de fois que MED-V tente de lui accorder des droits de groupe d’utilisateurs finaux. Le dépassement de la valeur de réessayer spécifiée sans être en mesure de donner aux droits de groupe d’utilisateurs finaux entraîne un échec de préparation d’ordinateur virtuel, qui est ensuite soumis à la valeur MaxRetryCount. Plage = 0 à 2147483647.</p></td>
</tr>
<tr class="even">
<td align="left"><p>GiveUserGroupRightsTimeout </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Par défaut = 300</p></td>
<td align="left"><p>Valeur du délai d’expiration, en secondes, lors de la fourniture de droits de groupe d’utilisateurs. Plage = 0 à 2147483647.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>LogFilePaths </p></td>
<td align="left"><p>MULTI_SZ</p></td>
<td align="left"><p></p></td>
<td align="left"><p>Liste des chemins d’accès aux fichiers journaux collectés par MED-V lors de la première configuration. </p></td>
</tr>
<tr class="even">
<td align="left"><p>MaxPostponeTime </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Par défaut = 120</p></td>
<td align="left"><p>Le nombre maximal d’heures qui peuvent être reportées par l’utilisateur final pour la première fois. Plage = 0 à 2147483647.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MaxRetryCount </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Par défaut = 3</p></td>
<td align="left"><p>Le nombre maximal de fois que MED-V tente de préparer une machine virtuelle si chaque tentative se termine par un échec autre qu’une erreur logicielle. En cas d’échec de la préparation de l’ordinateur virtuel et du nombre de tentatives de configuration pour la première fois, MED-V informe l’utilisateur final de l’échec et ne donne pas la possibilité de réessayer. Le nombre est remis à zéro chaque fois que MED-V est démarré. Plage = 0 à 2147483647.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Mode </p></td>
<td align="left"><p>SZ</p></td>
<td align="left"><p>Par défaut = sans assistance</p></td>
<td align="left"><p>Configure le mode d’interaction de l’utilisateur pour la première fois. Les valeurs possibles sont les suivantes:</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong>Surveillance.</strong> L’utilisateur final doit entrer des informations lors de la première configuration.</p>
<div class="alert">
<strong>Remarque</strong><br/><p>Si vous avez créé le fichier Sysprep. inf de manière à ce que la mini-installation nécessite l’entrée de l’utilisateur, vous devez sélectionner le <strong> </strong> mode assisté ou des problèmes peuvent se produire lors de la première configuration.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong>Sans assistance </strong> . Lors de la première installation, la machine virtuelle n’est pas visible pour l’utilisateur final, mais l’utilisateur final est invité avant le premier démarrage de l’installation.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong>Silent </strong> . Lors de la première installation, la machine virtuelle n’est pas visible pour l’utilisateur final.</p></td>
</tr>
<tr class="even">
<td align="left"><p>NonInteractiveRetryTimeoutInc </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Par défaut = 15</p></td>
<td align="left"><p>La valeur du délai d’expiration, en minutes, lors de la première configuration du mode interactif de configuration pour la première fois lors de la nouvelle tentative d’installation. Plage = 0 à 2147483647.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>NonInteractiveTimeout </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Par défaut = 45</p></td>
<td align="left"><p>La valeur du délai d’expiration, en minutes, lors de la première configuration du mode interactif de configuration pour la première fois. Plage = 0 à 2147483647.</p></td>
</tr>
<tr class="even">
<td align="left"><p>PostponeUtcDateTimeLimit </p></td>
<td align="left"><p>SZ</p></td>
<td align="left"><p></p></td>
<td align="left"><p>La date et l’heure au format DateTime UTC, qui peut être ajourné pour la première fois. Entrez au format &quot; aaaa-mm-jj hh: mm &quot; avec les heures spécifiées à l’aide de la norme d’horloge de 24 heures.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>RetryDialogMsg </p></td>
<td align="left"><p>MULTI_SZ</p></td>
<td align="left"><p>Le message est disponible dans le fichier de ressources </p></td>
<td align="left"><p>Message personnalisable qui s’affiche à l’utilisateur final lors du premier démarrage de l’installation.</p></td>
</tr>
<tr class="even">
<td align="left"><p>SetComputerNameEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Par défaut = 0</p></td>
<td align="left"><p>La configuration de l’entrée NomOrdinateur dans la section [UserData] du fichier Sysprep. inf dans l’invité doit être mise à jour en fonction du ComputerNameMask spécifié.   0 = faux; 1 = vrai.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = false: l’entrée NomOrdinateur dans le fichier Sysprep. inf n’est pas mise à jour en fonction de ComputerNameMask.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = vrai: l’entrée NomOrdinateur dans le fichier Sysprep. inf est mise à jour en fonction de ComputerNameMask.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>SetJoinDomainEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Par défaut = 0</p></td>
<td align="left"><p>Configure si le paramètre JoinDomain sous la section [identification] du fichier Sysprep. inf dans l’invité doit être mis à jour de façon à correspondre aux paramètres de l’hôte.  0 = faux; 1 = vrai.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = false: le paramètre JoinDomain dans le fichier Sysprep. inf n’est pas mis à jour pour correspondre aux paramètres de l’hôte.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = vrai: le paramètre JoinDomain dans le fichier Sysprep. inf est mis à jour de façon à correspondre aux paramètres de l’hôte.</p></td>
</tr>
<tr class="even">
<td align="left"><p>SetMachineObjectOUEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Par défaut = 0</p></td>
<td align="left"><p>Configure si le paramètre MachineObjectOU sous la section [identification] du fichier Sysprep. inf de l’invité est mis à jour de façon à correspondre à l’hôte.  0 = faux; 1 = vrai.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = false: le paramètre MachineObjectOU dans le fichier Sysprep. inf n’est pas mis à jour pour correspondre aux paramètres de l’hôte.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = vrai: le paramètre MachineObjectOU dans le fichier Sysprep. inf est mis à jour de façon à correspondre aux paramètres de l’hôte.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>SetRegionalSettingsEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Par défaut = 0</p></td>
<td align="left"><p>Configure le mode de mise à jour des paramètres de la section [RegionalSettings] du fichier Sysprep. inf dans l’invité pour correspondre à l’hôte.  0 = faux; 1 = vrai.</p>
<div class="alert">
<strong>Remarque</strong><br/><p>Par défaut, le paramètre TimeZone dans l’invité est toujours synchronisé avec le paramètre TimeZone de l’hôte.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = false: les paramètres de la section [RegionalSettings] du fichier Sysprep. inf dans l’invité ne sont pas mis à jour pour correspondre à l’hôte.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = vrai: les paramètres de la section [RegionalSettings] du fichier Sysprep. inf de l’invité sont mis à jour de façon à correspondre à l’hôte.</p></td>
</tr>
<tr class="even">
<td align="left"><p>SetUserDataEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Par défaut = 0</p></td>
<td align="left"><p>Indique si les paramètres FullName et OrgName figurant sous la section [UserData] du fichier Sysprep. inf de l’invité sont mis à jour de façon à correspondre aux paramètres de l’hôte.  0 = faux; 1 = vrai.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = false: les paramètres NomComplet et OrgName du fichier Sysprep. inf ne sont pas mis à jour pour correspondre aux paramètres de l’hôte.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = vrai: les paramètres NomComplet et OrgName du fichier Sysprep. inf sont mis à jour de façon à correspondre aux paramètres de l’hôte.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>StartDialogMsg </p></td>
<td align="left"><p>MULTI_SZ</p></td>
<td align="left"><p>Le message est disponible dans le fichier de ressources </p></td>
<td align="left"><p>Message personnalisable qui s’affiche à l’utilisateur final lors du premier démarrage de l’installation. </p></td>
</tr>
<tr class="even">
<td align="left"><p>TaskCancelTimeout</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Par défaut = 30</p></td>
<td align="left"><p>La valeur du délai d’expiration, en secondes, lors de la première installation, le programme d’installation attend une réponse de l’ordinateur virtuel pour une opération d’annulation. Plage = 0 à 2147483647.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>TaskVMTurnOffTimeout</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Par défaut = 60</p></td>
<td align="left"><p>La valeur du délai d’expiration, en secondes, lors de la première installation, le programme d’installation attend que l’ordinateur virtuel s’arrête. Plage = 0 à 2147483647.</p></td>
</tr>
<tr class="even">
<td align="left"><p>UpgradeTimeout</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Par défaut = 600</p></td>
<td align="left"><p>Durée, en secondes, avant la mise à niveau du logiciel de l’agent invité MED-V. Plage = 0 à 2147483647.</p></td>
</tr>
</tbody>
</table>



## Clé UserExperience


Le tableau suivant fournit des informations sur les valeurs de Registre associées à la clé HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Medv\\v2\\UserExperience et à la clé HKEY \ _CURRENT \ _USER \\Software\\Microsoft\\Medv\\v2\\UserExperience.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nom</th>
<th align="left">Type</th>
<th align="left">Données/par défaut</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>AppPublishingEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Par défaut = 1</p></td>
<td align="left"><p>Configure le mode d’activation de la publication d’application de l’invité vers l’hôte.  0 = faux; 1 = vrai.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = false: désactive la publication d’applications de l’invité auprès de l’hôte.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = true: permet la publication d’applications de l’invité auprès de l’hôte.</p></td>
</tr>
<tr class="even">
<td align="left"><p>AudioSharingEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Par défaut = 1</p></td>
<td align="left"><p>Indique si le partage de l’appareil d’e/s audio entre l’invité et l’hôte est activé.  0 = faux; 1 = vrai.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = false: désactive le partage du périphérique d’e/s audio entre l’invité et l’hôte.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = true: active le partage de l’appareil d’e/s audio entre l’invité et l’hôte.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ClipboardSharingEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Par défaut = 1</p></td>
<td align="left"><p>Indique si le partage du presse-papiers entre l’invité et l’hôte est activé.  0 = faux; 1 = vrai.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = false: désactive le partage du presse-papiers entre l’invité et l’hôte.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = true: active le partage du presse-papiers entre l’invité et l’hôte.</p></td>
</tr>
<tr class="even">
<td align="left"><p>DialogTimeout</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Par défaut = 300</p></td>
<td align="left"><p>Durée, en secondes, avant le délai de démarrage de la première boîte de dialogue de démarrage de l’installation. Plage = 0 à 2147483647.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>HideVmTimeout</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Par défaut = 30</p></td>
<td align="left"><p>Valeur du délai d’expiration (en minutes) à laquelle la fenêtre de l’ordinateur virtuel en plein écran est cachée lors d’une longue tentative d’ouverture de session.</p></td>
</tr>
<tr class="even">
<td align="left"><p>LogonStartEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Par défaut = 1</p></td>
<td align="left"><p>Indique si l’invité doit être démarré lorsque l’utilisateur final se connecte à l’ordinateur de bureau ou lorsque la première application invité est démarrée.  0 = faux; 1 = vrai.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = false: l’invité est démarré lorsque la première application invité est démarrée.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = vrai: l’invité est démarré lorsque l’utilisateur final se connecte à l’ordinateur de bureau.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>PrinterSharingEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Par défaut = 1</p></td>
<td align="left"><p>Indique si le partage d’imprimantes entre l’invité et l’hôte est activé.  0 = faux; 1 = vrai.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = false: désactive le partage d’imprimantes entre l’invité et l’hôte.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = true: permet le partage d’imprimantes entre l’invité et l’hôte.</p></td>
</tr>
<tr class="even">
<td align="left"><p>RebootAbsoluteDelayTimeout </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Par défaut = 1440</p></td>
<td align="left"><p>Valeur du délai d’expiration, en minutes, lors du premier démarrage de l’installation. Plage = 0 à 2147483647.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>RedirectUrls </p></td>
<td align="left"><p>MULTI_SZ</p></td>
<td align="left"><p>Liste d’URL spécifiée</p></td>
<td align="left"><p>Spécifie une liste d’URL à rediriger de l’hôte vers l’invité. </p></td>
</tr>
<tr class="even">
<td align="left"><p>SmartCardLogonEnabled</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Par défaut = 0</p></td>
<td align="left"><p>Permet de configurer l’utilisation des cartes à puce pour l’authentification des utilisateurs dans MED-V. 0 = faux; 1 = vrai.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = faux: ne permet pas aux cartes à puce d’authentifier les utilisateurs finaux sur MED-V.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = vrai: permet aux cartes à puce d’authentifier les utilisateurs finaux sur MED-V.</p>
<div class="alert">
<strong>Important</strong><br/><p>Si SmartCardLogonEnabled et CredentialCacheEnabled sont activés, SmartCardLogonEnabled substitutions CredentialCacheEnabled.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>SmartCardSharingEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Par défaut = 1</p></td>
<td align="left"><p>Configure le partage des cartes à puce entre l’invité et l’hôte.  0 = faux; 1 = vrai.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = false: désactive le partage des cartes à puce entre l’invité et l’hôte.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = true: permet le partage de cartes à puce entre l’invité et l’hôte.</p></td>
</tr>
<tr class="even">
<td align="left"><p>USBDeviceSharingEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Par défaut = 1</p></td>
<td align="left"><p>Configure le partage des périphériques USB entre l’invité et l’hôte.  0 = faux; 1 = vrai.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = false: désactive le partage des périphériques USB entre l’invité et l’hôte.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = true: permet le partage d’appareils USB entre l’invité et l’hôte.</p></td>
</tr>
</tbody>
</table>



## Clé VM


Le tableau suivant fournit des informations sur les valeurs de Registre associées à la clé HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Medv\\v2\\VM et à la clé HKEY \ _CURRENT \ _USER \\Software\\Microsoft\\Medv\\v2\\VM.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nom</th>
<th align="left">Type</th>
<th align="left">Données/par défaut</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>CloseAction </p></td>
<td align="left"><p>SZ</p></td>
<td align="left"><p>Par défaut = mise en veille prolongée</p></td>
<td align="left"><p>L’action exécutée par l’ordinateur virtuel après la dernière application en cours d’exécution est fermée. Ce paramètre est ignoré si la valeur LogonStartEnabled est activée. Les options disponibles sont les suivantes:</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong>Mise en veille prolongée </strong> . Cette option libère toutes les ressources physiques utilisées par l’ordinateur virtuel, comme la mémoire et le processeur, et enregistre l’état de toutes les applications et opérations en cours d’exécution.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong>ARRÊT </strong> . Cette option arrête le système d’exploitation invité de manière sécurisée, puis libère toutes les ressources physiques utilisées par l’ordinateur virtuel, comme la mémoire et l’UC.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong>DÉSACTIVER </strong> . Cette option peut entraîner une perte de données, car elle est identique à la désactivation du bouton d’alimentation ou du retrait du cordon d’alimentation sur un ordinateur physique. Utilisez cette option uniquement si vous ne pouvez pas utiliser l’une des deux autres options.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>GuestMemFromHostMem </p></td>
<td align="left"><p>MULTI_SZ</p></td>
<td align="left"><p>378, 512, 1024, 1536, 2048 </p></td>
<td align="left"><p>Liste de valeurs de mémoire (Mo) pour l’invité. Cette valeur est utilisée pour déterminer la quantité de RAM disponible pour l’invité. Combinée à HostMemToGuestMem, une table de recherche est créée pour déterminer la quantité de mémoire RAM à allouer sur l’ordinateur virtuel invité. Les valeurs possibles peuvent être comprises entre 128 et 3712.</p></td>
</tr>
<tr class="even">
<td align="left"><p>GuestUpdateDuration </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Par défaut = 240</p></td>
<td align="left"><p>Le nombre de minutes écoulées par MED-V pour la mise à jour automatique de l’invité, en commençant à l’heure spécifiée dans la valeur GuestUpdateTime. Plage = 0 à 1440. Si vous définissez cette valeur sur zéro (0), la fonction de correction invité est désactivée.</p>
<p>Pour plus d’informations sur la mise à jour automatique des invités, voir <a href="managing-automatic-updates-for-med-v-workspaces.md" data-raw-source="[Managing Automatic Updates for MED-V Workspaces](managing-automatic-updates-for-med-v-workspaces.md)"> gestion des mises à jour automatiques pour les espaces de travail MED-V </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>GuestUpdateTime </p></td>
<td align="left"><p>SZ</p></td>
<td align="left"><p>Par défaut = 00:00</p></td>
<td align="left"><p>Les heures et les minutes chaque jour lorsque MED-V doit réveiller l’invité pour la mise à jour automatique, en utilisant la norme d’horloge de 24 heures. Spécifiez l’heure au format HH: MM.  </p>
<p>Pour plus d’informations sur la mise à jour automatique des invités, voir <a href="managing-automatic-updates-for-med-v-workspaces.md" data-raw-source="[Managing Automatic Updates for MED-V Workspaces](managing-automatic-updates-for-med-v-workspaces.md)"> gestion des mises à jour automatiques pour les espaces de travail MED-V </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>HostMemToGuestMem </p></td>
<td align="left"><p>MULTI_SZ</p></td>
<td align="left"><p>1024, 2048, 4096, 8192, 16384 </p></td>
<td align="left"><p>Liste de valeurs de mémoire (Mo) pour l’invité, définies par la mémoire RAM disponible sur l’hôte. Combinée à GuestMemFromHostMem, une table de recherche est créée pour déterminer la quantité de mémoire RAM à allouer sur l’ordinateur virtuel invité. Les valeurs possibles peuvent être comprises entre 1024 et 16384.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>HostMemToGuestMemCalcEnabled</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Par défaut = 1</p></td>
<td align="left"><p>Configure si la mémoire allouée pour l’invité est calculée à partir de la mémoire présente sur l’hôte.  0 = faux; 1 = vrai.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = false: la mémoire allouée pour l’invité n’est pas calculée à partir de la mémoire présente sur l’hôte.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = vrai: la mémoire allouée pour l’invité est calculée à partir de la mémoire présente sur l’hôte.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Mémoire </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Par défaut = 512</p></td>
<td align="left"><p>RAM (Mo) qui doit être allouée pour l’ordinateur virtuel invité. Ce paramètre est ignoré si le paramètre HostMemToGuestMemEnabled est activé. Plage = 128 à 2048.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MultiUserEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Par défaut = 0</p></td>
<td align="left"><p>Configure si plusieurs utilisateurs partagent le même espace de travail MED-V.  0 = faux; 1 = vrai.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = faux: plusieurs utilisateurs ne partagent pas le même espace de travail MED-V.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = vrai: plusieurs utilisateurs partagent le même espace de travail MED-V.</p></td>
</tr>
<tr class="even">
<td align="left"><p>NetworkingMode </p></td>
<td align="left"><p>SZ</p></td>
<td align="left"><p>Par défaut = NAT</p></td>
<td align="left"><p>Type de connexion réseau utilisée sur l’invité. Les valeurs possibles sont les suivantes:</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong>Bridged </strong> . MED-V dispose de sa propre adresse réseau, généralement obtenue par le biais du protocole DHCP.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong>TAR </strong> . MED-V utilise la traduction d’adresses réseau (NAT) pour partager l’adresse IP de l’hôte&#39;s pour le trafic sortant.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>TaskTimeout </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Par défaut = 600</p></td>
<td align="left"><p>Valeur de délai d’expiration générale, en secondes, que MED-V attend qu’une tâche se termine, par exemple, redémarrage et arrêt. Plage = 0 à 2147483647.</p></td>
</tr>
</tbody>
</table>



## Paramètres du Registre invité


Cette section répertorie les clés de registre d’invité MED-V configurables et explique leur utilisation.

### v2

Le tableau suivant fournit des informations sur la valeur du Registre invité associée à la clé HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Medv\\v2\\.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nom </th>
<th align="left">Type </th>
<th align="left">Données/par défaut </th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>EnableGPWorkarounds</p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>Par défaut = 1 </p></td>
<td align="left"><p>Configure la façon dont MED-V gère les clés BufferPolicyReads et GroupPolicyMinTransferRate.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>Par défaut, MED-V définit ces clés comme suit:</p>
<p>BufferPolicyReads = 1 et GroupPolicyMinTransferRate = 0.</p>
<p>Créez la clé EnableGPWorkarounds, si nécessaire, puis affectez la valeur zéro à la clé si vous ne souhaitez pas que MED-V modifie les paramètres par défaut de BufferPolicyReads et GroupPolicyMinTransferRate.</p>
<div class="alert">
<strong>Remarque</strong><br/><p>Si votre espace de travail MED-V s’exécute en mode NAT, EnableGPWorkarounds affecte les clés de Registre BufferPolicyReads et GroupPolicyMinTransferRate. Si votre espace de travail MED-V s’exécute en mode BRIDGEd, EnableGPWorkarounds affecte uniquement la clé de Registre BufferPolicyReads.</p>
</div>
<div>

</div>
<p>1 = vrai: MED-V définit les touches BufferPolicyReads = 1 et GroupPolicyMinTransferRate = 0 (en cas d’exécution en mode NAT) ou simplement BufferPolicyReads = 1 (en mode pont).</p>
<p>0 = faux: MED-V n’apporte aucune modification aux clés BufferPolicyReads et GroupPolicyMinTransferRate.</p></td>
</tr>
</tbody>
</table>



## Rubriques connexes


[Gérer les applications de l'espace de travail MED-V](manage-med-v-workspace-applications.md)

[Gérer la redirection d'URL MED-V](manage-med-v-url-redirection.md)

[Gérer les paramètres de l'espace de travail MED-V](manage-med-v-workspace-settings.md)









