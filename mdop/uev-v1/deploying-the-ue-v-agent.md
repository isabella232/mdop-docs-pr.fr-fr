---
title: Déploiement de l'agent UE-V
description: Déploiement de l'agent UE-V
author: dansimp
ms.assetid: ec1c16c4-4be0-41ff-93bc-3e2b1afb5832
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 19f3b798ad7d3a43b0a274a25dd97b651435de51
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812203"
---
# Déploiement de l'agent UE-V


L’agent Microsoft User Interface Virtualization (UE-V) doit s’exécuter sur chaque ordinateur qui utilise UE-V pour rendre itinérants les paramètres d’application et de fenêtre. Dans le cas d’un fichier d’installation unique, AgentSetup.exe, l’agent UE-V est installé sur les systèmes d’exploitation 32 bits et 64 bits. Les paramètres de ligne de commande de l’agent UE-V sont les suivants:

**AgentSetup.exe des paramètres de ligne de commande**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong>Paramètre de ligne de commande</strong></th>
<th align="left"><strong>Définition</strong></th>
<th align="left"><strong>Remarques</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>/Help ou/h ou/?</p></td>
<td align="left"><p>Affiche la boîte de dialogue d’utilisation de AgentSetup.exe.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>SettingsStoragePath</p></td>
<td align="left"><p>Indique le chemin UNC (Universal Naming Convention) qui définit l’emplacement de stockage des paramètres.</p></td>
<td align="left"><p>les variables d’environnement% nom d’utilisateur% ou% nom_ordinateur% sont acceptées. Les scripts peuvent nécessiter des variables d’échappement.</p>
<p><strong>Par défaut </strong> : &lt; aucun &gt; (accueil de l’utilisateur Active Directory)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>SettingsTemplateCatalogPath</p></td>
<td align="left"><p>Indique le chemin UNC (Universal Naming Convention) qui définit l’emplacement dans lequel les nouveaux modèles d’emplacement des paramètres sont consultés.</p></td>
<td align="left"><p>Requis uniquement pour les modèles d’emplacement des paramètres personnalisés</p></td>
</tr>
<tr class="even">
<td align="left"><p>RegisterMSTemplates</p></td>
<td align="left"><p>Indique si les modèles Microsoft par défaut doivent être inscrits lors de l’installation.</p></td>
<td align="left"><p>True | Fals</p>
<p><strong>Valeur par défaut </strong> : vrai</p></td>
</tr>
<tr class="odd">
<td align="left"><p>PowerSchool</p></td>
<td align="left"><p>Spécifie la méthode de synchronisation à utiliser.</p></td>
<td align="left"><p>OfflineFiles | Néant</p>
<p><strong>Par défaut </strong> : OFFLINEFILES</p></td>
</tr>
<tr class="even">
<td align="left"><p>SyncTimeoutInMilliseconds</p></td>
<td align="left"><p>Spécifie le nombre de millisecondes avant dépassement du délai d’attente lors de la récupération des paramètres utilisateur à partir de l’emplacement de stockage des paramètres.</p></td>
<td align="left"><p><strong>Par défaut </strong> : 2000 millisecondes</p>
<p>(attendez 2 secondes)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>SyncEnabled</p></td>
<td align="left"><p>Indique si la synchronisation UE-V est activée ou désactivée.</p></td>
<td align="left"><p>True | Fals</p>
<p><strong>Valeur par défaut </strong> : vrai</p></td>
</tr>
<tr class="even">
<td align="left"><p>MaxPackageSizeInBytes</p></td>
<td align="left"><p>Spécifie la taille de fichier du package de paramètres en octets lorsque l’agent UE-V signale que les fichiers dépassent le seuil.</p></td>
<td align="left"><p>&lt;papier&gt;</p>
<p><strong>Par défaut </strong> : aucun (aucun seuil d’avertissement)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>CEIPEnabled</p></td>
<td align="left"><p>Spécifie le paramètre de participation au programme d’amélioration du produit. S’il est défini sur true, les informations du programme d’installation sont téléchargées sur le site du programme d’amélioration du produit de Microsoft. Si elle a la valeur false, aucune information n’est téléchargée.</p></td>
<td align="left"><p>True | Fals</p>
<p><strong>Valeur par défaut </strong> : false</p>
<p><strong>Sur Windows 7 </strong> : vrai</p></td>
</tr>
</tbody>
</table>

 

Lors de l’installation, le paramètre de ligne de commande SettingsStoragePath spécifie l’emplacement de stockage des paramètres pour les valeurs de paramètres. Un emplacement de stockage des paramètres peut être défini avant le déploiement de l’agent UE-V. Si aucun emplacement de stockage des paramètres n’est défini, UE-V utilise le répertoire de base de l’utilisateur Active Directory comme emplacement de stockage des paramètres. Lorsque vous spécifiez la configuration SettingsStoragePath lors de l’installation et que vous utilisez le% nom_utilisateur% dans le cadre de la valeur, vous pouvez utiliser les mêmes paramètres utilisateur sur tous les ordinateurs ou sessions dans lesquels l’utilisateur se connecte. Si vous spécifiez les variables%username%\\%ComputerName% dans le cadre de la valeur SettingsStoragePath, cela préserve l’interface des paramètres pour chaque ordinateur.

Les fichiers Windows Installer (. msi) spécifiques à l’architecture sont fournis pour l’installation de l’agent UE-V, en plus du programme d’installation 32 bits et 64 bits combinés. Les fichiers AgentSetupx86.msi ou AgentSetupx64.msi d’installation sont plus petits que le fichier AgentSetup.exe et peuvent rationaliser les déploiements des agents. Les paramètres de ligne de commande du programme d’installation de AgentSetup.exe sont pris en charge pour l’installation de Windows Installer (. msi).

**Remarques**  Lors de l’installation ou de la désinstallation d’UE-V agent, vous pouvez utiliser le fichier AgentSetup.exe ou le AgentSetup &lt; arch &gt; . msi, mais pas les deux. Le même fichier doit être utilisé pour désinstaller l’agent UE-V tel qu’il a été utilisé pour installer l’agent UE-V.

 

Veillez à utiliser le format de variable approprié lors de l’installation de l’agent UE-V. Le tableau suivant contient des exemples d’options de déploiement pour l’utilisation des fichiers d’installation de AgentSetup.exe ou Windows Installer (. msi).

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong>Type de déploiement</strong></th>
<th align="left"><strong>Description du déploiement</strong></th>
<th align="left"><strong>Exemple</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Invite de commandes</p></td>
<td align="left"><p>Lorsque vous installez l’agent UE-V à partir d’une invite de commandes, utilisez le format de variable% ^ nom_utilisateur%. Si des guillemets sont nécessaires en raison d’espaces dans le chemin de stockage des paramètres, utilisez un fichier de script de commandes pour le déploiement.</p>
<p></p></td>
<td align="left"><p><code>AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%^username%</code></p>
<p></p>
<p><code>msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l<em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%^username%</code></p></td>
</tr>
<tr class="even">
<td align="left"><p>Script de commande</p></td>
<td align="left"><p>Lorsque vous installez l’agent UE-V à partir d’un fichier de script de commandes, utilisez le format de variable%% nom_utilisateur%%. Si vous utilisez cette méthode d’installation, vous devez ignorer la variable contenant les caractères%%. Sans ce caractère, le script développe la variable nom d’utilisateur au moment de l’installation, plutôt qu’au moment de l’exécution, provoquant l’utilisation d’un emplacement de stockage des paramètres unique pour tous les utilisateurs.</p></td>
<td align="left"><p><code>AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=&quot;\server\settingsshare%%username%%&quot;</code></p>
<p></p>
<p><code>msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l</em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=&quot;\server\settingsshare%%username%%&quot;</code></p>
<p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>PowerShell</p></td>
<td align="left"><p>Lorsque vous installez l’agent UE-V à partir d’une invite PowerShell ou d’un script PowerShell, utilisez le format de variable% nom_utilisateur%.</p></td>
<td align="left"><p><code>&amp; AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%username%</code></p>
<p></p>
<p><code>&amp; msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l<em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%username%</code></p>
<p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Distribution de logiciel électronique, comme le déploiement du déploiement logiciel de Configuration Manager)</p></td>
<td align="left"><p>Lorsque vous installez l’agent UE-V avec Configuration Manager, utilisez le format de variable ^% nom_utilisateur ^%.</p></td>
<td align="left"><p><code>AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare^%username^%</code></p>
<p></p>
<p><code>msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l</em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare^%username^%</code></p></td>
</tr>
</tbody>
</table>

 

**Remarques**  L’installation de l’agent U-EV nécessite des droits d’administrateur et l’ordinateur exige un redémarrage pour que l’agent UE-V puisse s’exécuter.

 

## Méthodes de déploiement d’agent UE-V à partir d’un partage réseau


Pour déployer l’agent UE-V, vous pouvez utiliser les méthodes suivantes:

-   Une solution de distribution de logiciels électronique (ESD) qui peut installer un fichier Windows Installer (. msi).

-   Script d’installation qui fait référence au fichier Windows Installer (. msi) qui est stocké sur un partage centralisé.

-   Exécution manuelle du programme d’installation sur l’ordinateur.

Pour déployer l’agent UE-V à partir d’un partage réseau, procédez comme suit:

**Pour installer et configurer l’agent UE-V à partir d’un partage réseau**

1.  Copiez le fichier d’installation de l’agent UE-V (AgentSetup.exe) sur un partage réseau auquel les utilisateurs disposent d’une autorisation de lecture.

2.  Déploiement d’un script sur des ordinateurs utilisateurs qui installent l’agent UE-V. Le script doit spécifier l’emplacement de stockage des paramètres.

**Mettre à jour l’agent UE-V**

Les mises à jour du logiciel d’agent UE-V seront fournies par le biais de Microsoft Update. Lors d’une mise à niveau d’un agent UE-V, le groupe par défaut des modèles d’emplacement des paramètres pour les applications Microsoft courantes et les paramètres Windows est susceptible d’être mis à jour. UE-V les mises à jour de l’agent peuvent être déployées à l’aide de l’infrastructure de distribution de logiciels d’entreprise.

## Rubriques connexes


[Déploiement d'UE-V1.0](deploying-ue-v-10.md)

[Configurations prises en charge pour UE-V1.0](supported-configurations-for-ue-v-10.md)

[Déploiement de l'emplacement de stockage des paramètres pour UE-V1.0](deploying-the-settings-storage-location-for-ue-v-10.md)

[Installation du Générateur UE-V](installing-the-ue-v-generator.md)

Déploiement de l’agent de virtualisation de l’utilisation de l’utilisateur
 

 





