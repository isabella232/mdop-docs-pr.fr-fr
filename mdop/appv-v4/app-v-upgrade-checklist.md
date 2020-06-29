---
title: Liste de contrôle pour la mise à niveau d'App-V
description: Liste de contrôle pour la mise à niveau d'App-V
author: dansimp
ms.assetid: 64e317d2-d260-4b67-8a49-ba9ac513087a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ad856ce3067c327f3e604f9269ee384a66a1675a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808026"
---
# Liste de contrôle pour la mise à niveau d'App-V


Avant d’essayer de procéder à la mise à niveau vers la version 4,5 ou ultérieure de Microsoft Application Virtualization, toute version antérieure à l’application-V 4,1 doit être mise à niveau vers App-V 4,1. Envisagez d’abord de mettre à jour les clients, puis de mettre à niveau les composants serveur. Les clients App-V qui ont été mis à niveau vers App-v 4,5 continuent de fonctionner avec des serveurs App-V qui n’ont pas encore été mis à niveau. Les versions antérieures du client ne sont pas prises en charge sur les serveurs qui ont été mis à niveau vers App-V 4,5.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Étape</th>
<th align="left">Référence</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Mettez à niveau les clients App-V.</p></td>
<td align="left"><p><a href="how-to-upgrade-the-application-virtualization-client.md" data-raw-source="[How to Upgrade the Application Virtualization Client](how-to-upgrade-the-application-virtualization-client.md)">Procédure pour mettre à niveau Application Virtualization Client</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Mettez à niveau la base de données et les serveurs App-V.</p>
<div class="alert">
<strong>Important</strong><br/><p>Si vous disposez de plusieurs serveurs de partage d’accès à la base de données App-V, tous les serveurs doivent être déconnectés pendant la mise à niveau de la base de données. Vous devez suivre les pratiques d’entreprise standard pour la mise à niveau de la base de données, mais nous vous recommandons de tester la mise à niveau de la base de données en utilisant d’abord une copie de sauvegarde de la base de données sur un serveur de test. Ensuite, vous devez sélectionner l’un des serveurs pour la première mise à niveau, qui mettra à niveau le schéma de la base de données. Après la mise à niveau de la base de données de production, vous pouvez mettre à niveau le logiciel App-V sur les autres serveurs.</p>
</div>
<div>

</div></td>
<td align="left"><p><a href="how-to-upgrade-the-servers-and-system-components.md" data-raw-source="[How to Upgrade the Servers and System Components](how-to-upgrade-the-servers-and-system-components.md)">Procédure pour mettre à niveau les serveurs et les composants système</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Mettez à niveau le service Web de gestion des applications-V.</p>
<p>Cette étape s’applique uniquement si le service Web de gestion se trouve sur un serveur distinct, ce qui vous oblige à exécuter le programme d’installation du serveur sur ce serveur distinct pour mettre à niveau le service Web de gestion. Dans le cas contraire, l’étape de mise à niveau précédente du serveur met automatiquement à niveau le service Web de gestion.</p></td>
<td align="left"><p><a href="how-to-upgrade-the-servers-and-system-components.md" data-raw-source="[How to Upgrade the Servers and System Components](how-to-upgrade-the-servers-and-system-components.md)">Procédure pour mettre à niveau les serveurs et les composants système</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Mettez à niveau la console de gestion des applications.</p>
<p>Cette étape s’applique uniquement si la console de gestion se trouve sur un autre ordinateur, ce qui vous oblige à exécuter le programme d’installation du serveur sur cet ordinateur distinct pour mettre à niveau la console. Dans le cas contraire, l’étape de mise à niveau précédente du serveur met à niveau la console de gestion.</p></td>
<td align="left"><p><a href="how-to-upgrade-the-servers-and-system-components.md" data-raw-source="[How to Upgrade the Servers and System Components](how-to-upgrade-the-servers-and-system-components.md)">Procédure pour mettre à niveau les serveurs et les composants système</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Mettez à niveau le Sequencer App-V.</p></td>
<td align="left"><p><a href="how-to-upgrade-the-application-virtualization-sequencer.md" data-raw-source="[How to Upgrade the Application Virtualization Sequencer](how-to-upgrade-the-application-virtualization-sequencer.md)">Procédure pour mettre à niveau Application Virtualization Sequencer</a></p></td>
</tr>
</tbody>
</table>



## Autres considérations en matière de mise à niveau


-   Tout package d’application virtuelle séquencé dans la version 4,2 ne doit pas être séquencé pour une utilisation avec la version 4,5. Toutefois, vous devez envisager de mettre à niveau les packages virtuels vers le format Microsoft Application Virtualization 4,5 Si vous souhaitez appliquer des listes de contrôle d’accès par défaut ou générer un fichier d’installation Windows. Il s’agit d’un processus simple qui nécessite uniquement l’ouverture et l’enregistrement du package d’application virtuel existant avec le Sequencer App-V 4,5. Cela peut être automatisé à l’aide de l’interface de ligne de commande App-VSequencer. Pour plus d’informations, reportez-vous [à création ou mise à niveau d’applications virtuelles à l’aide du Sequencer App-V](how-to-create-or-upgrade-virtual-applications-using--the-app-v-sequencer.md)

-   L’une des fonctionnalités du Sequencer 4,5 est la possibilité de créer des fichiers Windows Installer (. msi) en tant que points de contrôle pour l’interopérabilité d’un package d’application virtuel avec des systèmes de distribution de logiciels électroniques, tels que Microsoft Endpoint Configuration Manager. Les fichiers Windows Installer antérieurs créés à l’aide de l’outil MSI pour la virtualisation de l’application qui étaient installés sur un client App-V 4,1 ou 4,2 qui est ensuite mis à niveau vers App-V 4,5 continuent de fonctionner, même s’ils ne peuvent pas être installés sur le client App-V 4,5. Toutefois, ils ne peuvent pas être supprimés ou mis à niveau sauf s’ils sont mis à niveau dans le Sequencer App-V 4,5. Le package App-V d’origine antérieur à 4,5 doit être ouvert dans le Sequencer App-V 4,5, puis enregistré en tant que fichier Windows Installer.

    **Remarque**  
    Si le client App-V 4,2 a déjà fait l’objet d’une mise à niveau vers App-V 4,5, il est possible de créer une solution de contournement pour conserver les packages de la version 4,2 sur les clients de la version 4,5 et permettre leur gestion. Ce script doit copier deux fichiers, msvcp71.dll et msvcr71.dll, dans le dossier d’installation de App-V et définir les valeurs de clé de Registre suivantes sous la clé de Registre: \ [HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\]:

    "ClientVersion" = "4.2.1.20"

    «GlobalDataDirectory» = «C:\\\\Documents and Settings\\\\All Users\\\\Documents\\\\» (emplacement accessible en écriture dans le monde)



-   Les fichiers Windows Installer générés par le Sequencer App-V 4,5 affichent le message d’erreur «ce package nécessite le client Microsoft Application Virtualization 4,5 ou une version ultérieure» lorsque vous tentez de les exécuter sur un client App-V 4,6. Ouvrez l’ancien package avec le Sequencer App-V 4,5 SP1 ou le Sequencer App-V 4,6 et générez un nouveau fichier. msi pour le package.

-   Tout rapport de version 4,2 créé et enregistré sera écrasé lorsque le serveur sera mis à niveau vers la version 4,5. Si vous devez conserver ces rapports, vous devez enregistrer une copie de sauvegarde du fichier SftMMC. msc qui se trouve dans le dossier de la console de gestion SoftGrid du serveur et utiliser cette copie pour remplacer le nouveau SftMMC. msc qui est installé lors de la mise à niveau.

-   Pour plus d’informations sur la mise à niveau à partir d’une version antérieure, voir [mise à niveau vers le Forum aux questions sur Microsoft application virtualization 4,5](https://go.microsoft.com/fwlink/?LinkId=120358) ( https://go.microsoft.com/fwlink/?LinkId=120358) .

## <a href="" id="app-v-4-6-client-package-support-"></a>Prise en charge de package client App-V 4,6


Vous pouvez déployer des packages créés dans des versions antérieures de App-V pour les clients 4,6 App-V. Toutefois, vous devez modifier le fichier. OSD associé de manière à inclure les informations appropriées sur le système d’exploitation et l’architecture du processeur. Vous pouvez utiliser les valeurs suivantes:

<table>
<colgroup>
<col width="100%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Valeur du système d’exploitation</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>&lt;VALEUR du système d’exploitation = «Win2003TS»/&gt;</p></td>
</tr>
<tr class="even">
<td align="left"><p>&lt;VALEUR du système d’exploitation = «Win2003TS64»/&gt;</p></td>
</tr>
<tr class="odd">
<td align="left"><p>&lt;VALEUR du système d’exploitation = «Win2008TS»/&gt;</p></td>
</tr>
<tr class="even">
<td align="left"><p>&lt;VALEUR du système d’exploitation = «Win2008TS64»/&gt;</p></td>
</tr>
<tr class="odd">
<td align="left"><p>&lt;VALEUR du système d’exploitation = «Win2008R2TS64»/&gt;</p></td>
</tr>
<tr class="even">
<td align="left"><p>&lt;VALEUR du système d’exploitation = «Win7»/&gt;</p></td>
</tr>
<tr class="odd">
<td align="left"><p>&lt;VALEUR du système d’exploitation = «Win764»/&gt;</p></td>
</tr>
<tr class="even">
<td align="left"><p>&lt;VALEUR du système d’exploitation = «WinVista»/&gt;</p></td>
</tr>
<tr class="odd">
<td align="left"><p>&lt;VALEUR du système d’exploitation = «WinVista64»/&gt;</p></td>
</tr>
<tr class="even">
<td align="left"><p>&lt;VALEUR du système d’exploitation = «WinXP»/&gt;</p></td>
</tr>
<tr class="odd">
<td align="left"><p>&lt;VALEUR du système d’exploitation = «WinXP64»/&gt;</p></td>
</tr>
</tbody>
</table>



Pour exécuter un package 32, vous devez séquencer l’application sur un ordinateur exécutant un système d’exploitation 32 bits sur lequel est installé le Sequencer App-V 4,6. Après avoir séquencé l’application, dans la console de Sequencer, cliquez sur l’onglet **déploiement** , puis spécifiez le système d’exploitation et l’architecture de processeur appropriés, le cas échéant.

**Important**  
Les applications séquencées sur un ordinateur exécutant un système d’exploitation 64 bits doivent être déployées sur des ordinateurs exécutant un système d’exploitation 64 bits. Les nouveaux packages 32 bits créés à l’aide du Sequencer App-V 4,6 ne s’exécutent pas sur les ordinateurs exécutant le client App-V 4,5.



Pour exécuter de nouveaux packages 64 bits sur le client App-V 4,6, vous devez séquencer l’application sur un ordinateur exécutant le Sequencer App-V 4,6 et exécutant un système d’exploitation 64 bits. Après avoir séquencé l’application, dans la console de Sequencer, cliquez sur l’onglet **déploiement** , puis spécifiez le système d’exploitation et l’architecture de processeur appropriés, le cas échéant.

Le tableau suivant répertorie les versions clientes qui exécutent des packages créés à l’aide des différentes versions du Sequencer.

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left">Séquence en utilisant le séquenceur App-V 4,2</th>
<th align="left">Séquence en utilisant le séquenceur App-V 4,5</th>
<th align="left">Séquencé en utilisant le Sequencer App-V 4,6 32-bit</th>
<th align="left">Séquencé en utilisant le Sequencer App-V 4,6 64-bit</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Client 4,2</p></td>
<td align="left"><p>Oui</p></td>
<td align="left"><p>Non</p></td>
<td align="left"><p>Non</p></td>
<td align="left"><p>Non</p></td>
</tr>
<tr class="even">
<td align="left"><p>4,5 client ¹</p></td>
<td align="left"><p>Oui</p></td>
<td align="left"><p>Oui</p></td>
<td align="left"><p>Non</p></td>
<td align="left"><p>Non</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Client 4,6 (32 bits)</p></td>
<td align="left"><p>Oui</p></td>
<td align="left"><p>Oui</p></td>
<td align="left"><p>Oui</p></td>
<td align="left"><p>Non</p></td>
</tr>
<tr class="even">
<td align="left"><p>Client 4,6 (64 bits)</p></td>
<td align="left"><p>Oui</p></td>
<td align="left"><p>Oui</p></td>
<td align="left"><p>Oui</p></td>
<td align="left"><p>Oui</p></td>
</tr>
</tbody>
</table>



¹ s’applique à toutes les versions du client App-V 4,5, notamment App-V 4,5, App-V 4,5 CU1 et App-V 4,5 SP1.









