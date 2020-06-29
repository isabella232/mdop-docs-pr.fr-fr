---
title: Planification de la migration à partir de versions antérieures
description: Planification de la migration à partir de versions antérieures
author: dansimp
ms.assetid: 62967bf1-542f-41b0-838f-c62f3430ac73
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9b239e09da06270b30b401151cf12e817e2cf8d4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806502"
---
# Planification de la migration à partir de versions antérieures


Avant d’essayer de procéder à la mise à niveau vers Microsoft Application Virtualization 4.5 ou versions ultérieures, toute version antérieure à 4.1 doit être mise à niveau vers la version 4.1. Envisagez de mettre à niveau vos clients d’abord, puis mettez à niveau les composants serveur. Les clients qui ont été mis à niveau vers la version 4.5 continuent de fonctionner avec des serveurs de virtualisation des applications qui n’ont pas encore été mis à niveau. Les versions antérieures du client ne sont pas prises en charge sur les serveurs qui ont été mis à niveau vers la version 4.5. Pour plus d’informations sur la mise à niveau des composants système, voir [considérations relatives au déploiement et à la mise à niveau](application-virtualization-deployment-and-upgrade-considerations.md)de l’application.

Pour garantir une migration réussie, vous devez mettre à niveau les composants du système de virtualisation des applications dans l’ordre suivant:

1.  **Clients Microsoft Application Virtualization.** Pour obtenir des instructions de mise à niveau détaillées, voir [Comment mettre à niveau le client de virtualisation des applications](how-to-upgrade-the-application-virtualization-client.md).

2.  **Serveurs et base de données Microsoft Application Virtualization.** Pour obtenir des instructions de mise à niveau détaillées, voir [mise à niveau des serveurs et composants système](how-to-upgrade-the-servers-and-system-components.md).

    **Remarques**  Si vous avez plusieurs accès du serveur à la base de données de virtualisation des applications, tous les serveurs doivent être déconnectés pendant la mise à niveau de la base de données. Nous vous conseillons de suivre les pratiques normales de votre entreprise pour la mise à niveau de la base de données, mais il est recommandé de tester la mise à niveau de la base de données en utilisant d’abord une copie de sauvegarde de la base de données sur un serveur de test. Ensuite, vous devez sélectionner l’un des serveurs pour la première mise à niveau, qui mettra à niveau le schéma de la base de données. Après avoir effectué la mise à niveau de la base de données de production, vous pouvez mettre à niveau les autres serveurs.

     

3.  **Service Web de gestion de Microsoft Application Virtualization.** Cette étape s’applique uniquement si le service Web de gestion se trouve sur un serveur distinct, ce qui vous oblige à exécuter le programme d’installation du serveur sur ce serveur distinct pour mettre à niveau le service Web. Dans le cas contraire, l’étape de mise à niveau précédente du serveur met automatiquement à niveau le service Web de gestion.

4.  **Console de gestion de Microsoft Application Virtualization.** Cette étape s’applique uniquement si la console de gestion se trouve sur un autre ordinateur, ce qui vous oblige à exécuter le programme d’installation du serveur sur cet ordinateur distinct pour mettre à niveau la console. Dans le cas contraire, l’étape de mise à niveau précédente du serveur met à niveau la console de gestion.

5.  **Microsoft Application Virtualization Sequencer.** Pour obtenir des instructions détaillées, reportez-vous à la rubrique [Comment installer le Sequencer](how-to-install-the-application-virtualization-sequencer.md). Tout package d’application virtuelle séquencé dans la version 4.2 n’aura pas à être reséquencé pour une utilisation avec la version 4.5. Toutefois, vous devez envisager de mettre à niveau les packages virtuels vers le format Microsoft Application Virtualization 4.5 Si vous souhaitez appliquer des listes de contrôle d’accès par défaut ou générer un fichier d’installation Windows. Il s’agit d’un processus simple qui nécessite uniquement l’ouverture et l’enregistrement du package d’application virtuel existant avec le Sequencer 4.5. Cela peut être automatisé à l’aide de l’interface de ligne de commande du séquence de virtualisation d’application.

## <a href="" id="app-v-4-6-client-package-support-"></a>Prise en charge de package client App-V 4.6


Vous pouvez déployer des packages créés dans des versions antérieures de App-V pour les clients App-V 4.6. Toutefois, vous devez modifier le fichier **. OSD** associé de manière à inclure les informations appropriées sur le système d’exploitation et l’architecture du processeur. Utilisez les valeurs suivantes.

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

 

Pour exécuter un package 32, vous devez séquencer l’application sur un ordinateur exécutant un système d’exploitation 32 bits sur lequel est installé le Sequencer App-V 4.6. Après avoir séquencé l’application, dans la console de Sequencer, sélectionnez l’onglet **déploiement** , puis spécifiez le système d’exploitation et l’architecture de processeur appropriés, le cas échéant.

**Important**  Les applications séquencées sur un ordinateur exécutant un système d’exploitation 64 bits doivent être déployées sur des ordinateurs exécutant un système d’exploitation 64 bits. Les nouveaux packages 32 bits créés à l’aide du Sequencer App-V 4.6 ne s’exécuteront pas sur les ordinateurs exécutant le client App-V 4,5.

 

Pour exécuter de nouveaux packages 64 bits sur le client App-V 4.6, vous devez séquencer l’application sur un ordinateur exécutant le Sequencer App-V 4.6 et exécutant un système d’exploitation 64 bits. Après avoir séquencé l’application, dans la console de Sequencer, sélectionnez l’onglet **déploiement** , puis spécifiez le système d’exploitation et l’architecture de processeur appropriés, le cas échéant.

Le tableau suivant répertorie les versions clientes qui exécutent des packages créés à l’aide des différentes versions du Sequencer.

<table style="width:100%;">
<colgroup>
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left">Séquence en utilisant le séquenceur App-V 4,2</th>
<th align="left">Séquence en utilisant le séquenceur App-V 4,5</th>
<th align="left">Séquencé en utilisant le Sequencer App-V 4,6 32-bit</th>
<th align="left">Séquencé en utilisant le Sequencer App-V 4,6 64-bit</th>
<th align="left">Séquence en utilisant le Sequencer App-V 4,6 SP1 d’application 32 bits</th>
<th align="left">Séquence en utilisant le Sequencer App-V 4,6 SP1 d’application 64 bits</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Client 4,2</p></td>
<td align="left"><p>Oui</p></td>
<td align="left"><p>Non</p></td>
<td align="left"><p>Non</p></td>
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
<td align="left"><p>Non</p></td>
<td align="left"><p>Non</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Client 4,6 (32 bits)</p></td>
<td align="left"><p>Oui</p></td>
<td align="left"><p>Oui</p></td>
<td align="left"><p>Oui</p></td>
<td align="left"><p>Non</p></td>
<td align="left"><p>Oui</p></td>
<td align="left"><p>Non</p></td>
</tr>
<tr class="even">
<td align="left"><p>Client 4,6 (64 bits)</p></td>
<td align="left"><p>Oui</p></td>
<td align="left"><p>Oui</p></td>
<td align="left"><p>Oui</p></td>
<td align="left"><p>Oui</p></td>
<td align="left"><p>Oui</p></td>
<td align="left"><p>Oui</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Client 4,6 SP1</p></td>
<td align="left"><p>Oui</p></td>
<td align="left"><p>Oui</p></td>
<td align="left"><p>Oui</p></td>
<td align="left"><p>Non</p></td>
<td align="left"><p>Oui</p></td>
<td align="left"><p>Non</p></td>
</tr>
<tr class="even">
<td align="left"><p>Client 4,6 SP1 (64 bits)</p></td>
<td align="left"><p>Oui</p></td>
<td align="left"><p>Oui</p></td>
<td align="left"><p>Oui</p></td>
<td align="left"><p>Oui</p></td>
<td align="left"><p>Oui</p></td>
<td align="left"><p>Oui</p></td>
</tr>
</tbody>
</table>

 

¹ s’applique à toutes les versions du client App-V 4.5, notamment App-V 4.5, App-V 4.5 CU1 et App-V 4.5 SP1.

## Autres considérations relatives à la migration


L’une des fonctionnalités du Sequencer App-V 4.5 est la possibilité de créer des fichiers Windows Installer (. msi) en tant que points de contrôle pour l’interopérabilité d’un package d’application virtuel avec des systèmes de distribution de logiciels électroniques tels que Microsoft Endpoint Manager. Les fichiers Windows Installer antérieurs créés à l’aide de l’outil. msi pour la virtualisation d’applications qui ont été installés sur un client App-V 4.1 ou 4.2 qui est ensuite mis à niveau vers la version 4.5 continuent de fonctionner, même s’ils ne peuvent pas être installés sur le client 4.5. Toutefois, ils ne peuvent pas être supprimés ou mis à niveau sauf s’ils sont mis à niveau dans le Sequencer 4.5. Le package d’application virtuelle antérieur à 4,5 doit être ouvert dans le Sequencer 4.5, puis enregistré en tant que fichier Windows Installer.

**Remarques**  Si le client App-V 4.2 a déjà été mis à niveau vers la version 4.5, il est possible d’utiliser un script comme solution de contournement pour conserver les packages 4.2 sur des clients 4.5 et permettre leur gestion. Ce script doit copier deux fichiers, msvcp71.dll et msvcr71.dll, dans le dossier d’installation de App-V et définir les valeurs de clé de Registre suivantes sous la clé de Registre \ [HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\]:

"ClientVersion" = "4.2.1.20"

«GlobalDataDirectory» = «C:\\\\Documents and Settings\\\\All Users\\\\Documents\\\\» (emplacement accessible en écriture dans le monde)

 

Les fichiers Windows Installer générés par le Sequencer App-V 4,5 affichent le message d’erreur «ce package nécessite le client Microsoft Application Virtualization 4,5 ou une version ultérieure» lorsque vous tentez de les exécuter sur un client App-V 4,6. Ouvrez l’ancien package avec le Sequencer App-V 4,5 SP1 ou le Sequencer App-V 4,6 et générez un nouveau fichier. msi pour le package.

Tout rapport 4.2 créé et enregistré est écrasé lors de la mise à niveau vers la version 4.5 du serveur. Si vous avez besoin de conserver ces rapports, vous devez enregistrer une copie de sauvegarde du fichier SftMMC. msc qui se trouve dans le dossier de la console de gestion SoftGrid du serveur et utiliser cette copie pour remplacer le nouveau SftMMC. msc qui est installé lors de la mise à niveau.

Pour plus d’informations sur la mise à niveau à partir d’une version antérieure, voir [mise à niveau vers le Forum aux questions sur Microsoft application virtualization 4,5](https://go.microsoft.com/fwlink/?LinkId=120358) ( https://go.microsoft.com/fwlink/?LinkId=120358) .

## Rubriques connexes


[Planification du déploiement du système Application Virtualization](planning-for-application-virtualization-system-deployment.md)

 

 





