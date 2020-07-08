---
title: Notes de publication pour Microsoft User Experience Virtualization (UE-V)2.0
description: Notes de publication pour Microsoft User Experience Virtualization (UE-V)2.0
author: dansimp
ms.assetid: 5ef66cd1-ba2b-4383-9f45-e7cde41f1ba1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ad3deffa5cd567a70711e5447197e630f04ea254
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811063"
---
# Notes de publication pour Microsoft User Experience Virtualization (UE-V)2.0


Pour effectuer une recherche dans les notes de publication de Microsoft User Interface (UE-V) 2,0, appuyez sur Ctrl + F.

Nous vous conseillons de lire soigneusement ces notes de publication avant d’installer UE-V. Les notes de publication contiennent des informations nécessaires à l’installation réussie de la virtualisation de l’interface utilisateur et contiennent des informations supplémentaires qui ne sont pas disponibles dans la documentation du produit. S’il existe des différences entre ces notes de publication et d’autres documents UE-V, la dernière modification doit être considérée comme faisant autorité. Ces notes de publication remplacent le contenu qui est inclus dans ce produit.

## Envoi de commentaires


Dites-nous ce que vous pensez de notre documentation pour MDOP en nous fournissant vos commentaires et commentaires. Envoyez votre commentaires de documentation à [mdopdocs@microsoft.com](mailto:mdopdocs@microsoft.com?subject=UE-V%20Documentation).

## UE-V problèmes connus


Cette section contient des notes de publication relatives à la virtualisation de l’utilisation de l’utilisateur.

### Les paramètres de registre ne sont pas synchronisés entre App-V et les applications natives sur le même ordinateur

Lorsqu’un ordinateur dispose d’une application installée par le biais de la virtualisation des applications (App-V) et d’une application locale avec un fichier Windows Installer (. msi), les paramètres basés sur le registre ne sont pas synchronisés entre les technologies.

**Solution de contournement:** Pour résoudre ce problème, exécutez l’application en sélectionnant l’une des deux technologies, mais pas les deux.

### <a href="" id="settings-do-not-synchronization-when-network-share-is-outside-user-s-domain"></a>Les paramètres ne sont pas synchronisés lorsque le partage réseau se trouve hors du domaine de l’utilisateur

Lorsque Windows® 8 tente de synchroniser les paramètres du système d’exploitation, la synchronisation échoue avec le message d’erreur suivant: **Boost:: FileSystem:: existe:: nom d’utilisateur ou mot de passe incorrect**. Cette erreur peut indiquer que le partage réseau se trouve en dehors du domaine de l’utilisateur ou d’un domaine ayant une relation d’approbation avec ce domaine. Pour vérifier les événements du journal opérationnel, ouvrez l' **Observateur d’événements** et naviguez jusqu’à **applications et services consigne**le fonctionnement de l’enregistrement de la virtualisation de l'  /  **Microsoft**  /  **interface utilisateur**de Microsoft  /  **Logging**  /  **Operational**. Les partages réseau utilisés pour les emplacements de stockage des paramètres UE-V doivent résider dans le même domaine Active Directory que l’utilisateur ou un domaine approuvé du domaine de l’utilisateur.

**Solution de contournement:** Utilisez les partages réseau du même domaine Active Directory que l’utilisateur.

### Résultats inattendus avec Office 2010 et Office 2013 installés

Lorsqu’un utilisateur a installé Office 2010 et Office 2013, tous les paramètres courants entre les deux versions d’Office sont itinérants par UE-V. Cela risque de rendre la taille du package Office 2010 trop importante ou engendrer des conflits inattendus avec 2013, en particulier si la version d’Office 365 est utilisée.

**Solution de contournement:** Installer une seule version d’Office ou limiter les paramètres qui sont synchronisés par UE-V.

### La désinstallation de l’application Windows 8 rétablit les paramètres à l’état initial

Lors de l’utilisation de la synchronisation des paramètres d’UE-V pour une application Windows 8, si l’utilisateur désinstalle l’application, puis réinstalle l’application, les paramètres de l’application rétablissent leurs valeurs par défaut.Ce problème se produit car la désinstallation supprime la copie locale (mise en cache) des paramètres de l’application, mais ne supprime pas le package de paramètres UE-V local.Lorsque l’application est réinstallée et lancée, UE-V rassemblez les paramètres d’application qui ont été réinitialisés aux valeurs par défaut de l’application, puis chargez les paramètres par défaut sur l’emplacement de stockage central.D’autres ordinateurs exécutant l’application téléchargent les paramètres par défaut.Ce comportement est identique au comportement des applications de bureau.

**Solution de contournement:** Néant.

### Signature électronique de signature pour Outlook 2010

UE-V va itinérance des fichiers de signature Outlook 2010 entre les appareils. Toutefois, les options de signature par défaut pour les nouveaux messages, les réponses aux messages et les transferts ne sont pas synchronisées. Ces deux paramètres sont stockés dans le profil Outlook, dont UE-V n’est pas itinérant.

**Solution de contournement:** Néant.

### UE-V ne prend pas en charge les paramètres d’itinérance entre les versions 32 bits et 64 bits de Microsoft Office

Nous vous recommandons d’installer la version 64 de Microsoft Office pour les ordinateurs modernes. Pour déterminer la version dont vous avez besoin, [cliquez ici](https://support.office.com/article/choose-between-the-64-bit-or-32-bit-version-of-office-2dee7807-8f95-4d0c-b5fe-6c6f49b8d261?ui=en-US&rs=en-US&ad=US#32or64Bit=Newer_Versions). UE-V prend en charge les paramètres d’itinérance entre les différentes versions de l’architecture d’Office. Par exemple, les paramètres d’Office 32 bits s’itinérance entre toutes les instances Office 32 bits. UE-V ne prend pas en charge les paramètres d’itinérance entre les versions 32 bits et 64 bits d’Office.

**Solution de contournement:** Néant

### <a href="" id="msi-s-are-not-localized"></a>Les MSI ne sont pas localisés

UE-V 2,0 inclut un programme d’installation localisé pour l’agent UE-V et le générateur UE-V. Ils sont toujours disponibles, mais l’interface utilisateur est réduite et l’affichage du MSI uniquement en anglais. Malgré le fichier en anglais, le programme d’installation installe toutes les langues prises en charge lors de l’installation.

**Solution de contournement:** Néant

### Les favicons associés à des favoris Internet Explorer 9 ne sont pas itinérants

Les favicons associés à des favoris Internet Explorer 9 ne sont pas itinérants par la virtualisation de l’interface utilisateur et qui n’apparaissent pas à la première apparition des favoris sur un nouvel ordinateur.

**Solution de contournement:** Favicons s’affiche avec les favoris associés lorsque le signet est utilisé et mis en cache dans le navigateur Internet Explorer 9.

### Les chemins d’accès aux paramètres de fichier sont stockés dans le registre

Certains paramètres d’application stockent les chemins d’accès de leurs fichiers de configuration et de paramètres en tant que valeurs dans le registre. Les fichiers référencés sous forme de chemin d’accès dans le registre doivent être synchronisés lorsque les paramètres sont itinérants entre les ordinateurs.

**Solution de contournement:** Utilisez la redirection de dossiers ou d’autres technologies pour vous assurer que tous les fichiers référencés comme chemins d’accès aux paramètres de fichier sont présents et placés au même emplacement sur tous les ordinateurs dans lesquels les paramètres sont itinérants.

### Les chemins de stockage de paramètres longs peuvent générer une erreur

Le raccourci de stockage des paramètres reste le plus court possible. Les chemins longs peuvent empêcher la résolution ou la synchronisation. UE-V utilise le chemin de stockage des paramètres dans le cadre du chemin d’accès calculé au stockage des paramètres. Ce chemin d’accès est calculé comme suit: Path Storage path + "settingspackages" + package dir (ID de modèle) +. pkgx. Si le chemin d’accès calculé est supérieur à 260 caractères, le stockage du package échoue et génère le message d’erreur suivant dans le journal des événements de fonctionnement d’UE-V:

`[boost::filesystem::copy_file: The system cannot find the path specified]`

Pour vérifier les événements du journal opérationnel, ouvrez l’observateur d’événements et naviguez jusqu’à la section journaux des applications et des services/Microsoft/User-Virtualization/Logging/Operations.

**Solution de contournement:** Néant.

### Certains paramètres du système d’exploitation ne suivent que les versions du système d’exploitation

Les paramètres du système d’exploitation pour le narrateur et les caractères de devise spécifiques aux paramètres régionaux (par exemple, les paramètres linguistiques et régionaux) ne sont itinérants que sur les versions de système d’exploitation de Windows. Par exemple, les caractères monétaires ne seront pas itinérants entre Windows 7 et Windows 8.

**Solution de contournement:** Néant

### Les applications Windows 8 ne synchronisent pas les paramètres lors du redémarrage de l’application

Si une application Windows 8 se ferme de manière inattendue après le démarrage, les paramètres de l’application risquent de ne pas être synchronisés lors du redémarrage de l’application.

**Solution de contournement:** Fermez l’application Windows 8, fermez et redémarrez l’application UevAppMonitor.exe (peut utiliser TaskManager), puis redémarrez l’application Windows 8.

### <a href="" id="ue-v-1-agent-generates-errors-when-running-ue-v-2-templates-"></a>UE-V 1 agent génère des erreurs lors de l’exécution de modèles UE-V 2

Si un modèle d’emplacement des paramètres d’UE-V 2 est distribué sur un ordinateur installé avec un agent UE-V 1, certains paramètres ne sont pas synchronisés entre les ordinateurs et l’agent signale les erreurs dans le journal des événements.

**Solution de contournement:** Lors de la migration de UE-V 1 vers UE-V 2, il est possible que vous disposiez d’ordinateurs exécutant la version précédente de l’agent, que vous ayez créé un catalogue UE-V 2,0 distinct pour la prise en charge des modèles et de l’agent 2,0.

## HotFix et Articles de la base de connaissances pour UE-V 2,0


Cette section contient des correctifs et des Articles de la base de connaissances pour UE-V 2,0.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong>Article de la base de connaissances</strong></th>
<th align="left">Title</th>
<th align="left"><strong>Link</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>2927019</p></td>
<td align="left"><p>Package Hotfix 1 pour les utilisateurs de Microsoft-virtualisation 2,0</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2927019" data-raw-source="[support.microsoft.com/kb/2927019](https://support.microsoft.com/kb/2927019)">support.microsoft.com/kb/2927019</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2903501</p></td>
<td align="left"><p>UE-V: compatibilité entre les utilisateurs et la virtualisation de l’interface utilisateur avec les profils utilisateur</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2903501/EN-US" data-raw-source="[support.microsoft.com/kb/2903501/EN-US](https://support.microsoft.com/kb/2903501/EN-US)">support.microsoft.com/kb/2903501/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2770042</p></td>
<td align="left"><p>Paramètres de Registre UE-V</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2770042/EN-US" data-raw-source="[support.microsoft.com/kb/2770042/EN-US](https://support.microsoft.com/kb/2770042/EN-US)">support.microsoft.com/kb/2770042/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2847017</p></td>
<td align="left"><p>Paramètres d’UE-V répliqués par Internet Explorer</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2847017/EN-US" data-raw-source="[support.microsoft.com/kb/2847017/EN-US](https://support.microsoft.com/kb/2847017/EN-US)">support.microsoft.com/kb/2847017/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2930271</p></td>
<td align="left"><p>Présentation des limitations des signatures Outlook en itinérance dans Microsoft UE-V</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2930271/EN-US" data-raw-source="[support.microsoft.com/kb/2930271/EN-US](https://support.microsoft.com/kb/2930271/EN-US)">support.microsoft.com/kb/2930271/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2769631</p></td>
<td align="left"><p>Réparation d’une installation d’UE-V endommagée</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2769631/EN-US" data-raw-source="[support.microsoft.com/kb/2769631/EN-US](https://support.microsoft.com/kb/2769631/EN-US)">support.microsoft.com/kb/2769631/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2850989</p></td>
<td align="left"><p>La migration de profils MAPI avec Microsoft UE-V n’est pas prise en charge.</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2850989/EN-US" data-raw-source="[support.microsoft.com/kb/2850989/EN-US](https://support.microsoft.com/kb/2850989/EN-US)">support.microsoft.com/kb/2850989/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2769586</p></td>
<td align="left"><p>UE-V: itinérance de dossiers et de clés de Registre vides</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2769586/EN-US" data-raw-source="[support.microsoft.com/kb/2769586/EN-US](https://support.microsoft.com/kb/2769586/EN-US)">support.microsoft.com/kb/2769586/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2782997</p></td>
<td align="left"><p>Comment activer la journalisation de débogage dans Microsoft User Interface Virtualization (UE-V)</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2782997/EN-US" data-raw-source="[support.microsoft.com/kb/2782997/EN-US](https://support.microsoft.com/kb/2782997/EN-US)">support.microsoft.com/kb/2782997/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2769570</p></td>
<td align="left"><p>UE-V ne met pas à jour le thème pour les sessions RDS ou VDI</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2769570/EN-US" data-raw-source="[support.microsoft.com/kb/2769570/EN-US](https://support.microsoft.com/kb/2769570/EN-US)">support.microsoft.com/kb/2769570/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2901856</p></td>
<td align="left"><p>Les paramètres de l’application ne se synchronisent pas après le redémarrage sur un ordinateur avec UE-V</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2901856/EN-US" data-raw-source="[support.microsoft.com/kb/2901856/EN-US](https://support.microsoft.com/kb/2901856/EN-US)">support.microsoft.com/kb/2901856/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2850582</p></td>
<td align="left"><p>Utiliser la virtualisation de l’utilisation de Microsoft avec les applications App-V</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2850582/EN-US" data-raw-source="[support.microsoft.com/kb/2850582/EN-US](https://support.microsoft.com/kb/2850582/EN-US)">support.microsoft.com/kb/2850582/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>3041879</p></td>
<td align="left"><p>Versions de fichiers actuelles pour l’utilisation de Microsoft User-virtualisation</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/3041879/EN-US" data-raw-source="[support.microsoft.com/kb/3041879/EN-US](https://support.microsoft.com/kb/3041879/EN-US)">support.microsoft.com/kb/3041879/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2843592</p></td>
<td align="left"><p>Informations sur la virtualisation et la disponibilité des utilisateurs</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2843592/EN-US" data-raw-source="[support.microsoft.com/kb/2843592/EN-US](https://support.microsoft.com/kb/2843592/EN-US)">support.microsoft.com/kb/2843592/EN-US</a></p></td>
</tr>
</tbody>
</table>

 

 

 





