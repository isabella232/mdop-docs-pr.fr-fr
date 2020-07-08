---
title: À propos de l'onglet Déploiement
description: À propos de l'onglet Déploiement
author: dansimp
ms.assetid: 12891798-baa4-45a5-b845-b9505ab95633
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 147e8b1057c789d97087461a585fa3f365089784
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808117"
---
# À propos de l'onglet Déploiement


Pour modifier les informations relatives à une application que vous allez mettre en ordre, utilisez l’onglet **déploiement** de la console Cet onglet contient les éléments suivants.

## URL du serveur


Utilisez les contrôles d' **URL du serveur** pour spécifier les paramètres de configuration du serveur d’applications virtuel.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Contrôle</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Protocole</strong></p></td>
<td align="left"><p>Vous permet de sélectionner le protocole qui diffusera en continu le package d’application séquencé d’un serveur d’application virtuel vers un client de bureau de virtualisation d’applications. Les protocoles suivants sont disponibles:</p>
<ul>
<li><p><strong>RTSP </strong> : le protocole par défaut spécifie que le protocole de diffusion en continu en temps réel contrôle l’échange d’applications compatibles avec la virtualisation.</p></li>
<li><p><strong>RTSP </strong> : spécifie que le protocole de diffusion en continu en temps réel avec la sécurité au niveau de transport contrôle l’échange d’un package d’application séquencé.</p></li>
<li><p><strong>Fichier </strong> — spécifie que l’application séquencée sera diffusée à partir d’un partage de fichiers.</p></li>
<li><p><strong>HTTPs </strong> : indique que le protocole SSL (Secure Hypertext Transport Protocol) contrôle l’échange d’un package.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Nom</strong></p></td>
<td align="left"><p>Vous permet de sélectionner le serveur d’applications virtuelles ou l’équilibrage de charge dans le premier plan d’un groupe de serveurs d’applications virtuelles qui diffusera le package logiciel sur un client de bureau de virtualisation des applications. Vous devez renseigner cet élément pour créer un package d’application séquencé, mais vous pouvez passer de la variable d’environnement% SFT_SOFTGRIDSERVER% par défaut au nom d’hôte ou à l’adresse IP réelle d’un serveur d’applications virtuelles.</p>
<div class="alert">
<strong>Remarque</strong><br/><p>Si vous choisissez de ne pas spécifier de nom d’hôte ou d’adresse IP statique, vous devez configurer une variable d’environnement appelée SFT_SOFTGRIDSERVER dans chaque client de bureau. Sa valeur doit correspondre au nom d’hôte ou à l’adresse IP du serveur d’applications virtuel ou de l’équilibrage de charge qui est le client&#39;source d’applications. Cette variable d’environnement doit être une variable système plutôt qu’une variable utilisateur. Toute session de client de bureau de virtualisation d’application en cours d’exécution sur cet ordinateur lors de votre affectation de cette variable doit être fermée, puis ouverte pour que la session de reprise puisse être consciente de sa nouvelle source d’application.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Port</strong></p></td>
<td align="left"><p>Vous permet de spécifier le port sur lequel le serveur d’applications virtuelles ou le point d’équilibrage de charge écoutera un client de bureau de la virtualisation des applications&#39;demande du package. Ces informations sont nécessaires pour créer un package, mais vous pouvez le modifier. Le port par défaut est 554.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Chemin d'accès</strong></p></td>
<td align="left"><p>Vous permet de spécifier le chemin d’accès relatif du serveur d’application virtuel sur lequel est stocké le package logiciel et celui à partir duquel il sera diffusé. Ces informations sont nécessaires pour créer un package si le fichier SFT est stocké dans un sous-répertoire de contenu. dans le cas contraire, ces informations ne sont pas obligatoires.</p></td>
</tr>
</tbody>
</table>



## Systèmes d’exploitation


Utilisez les contrôles des **systèmes d’exploitation** pour spécifier la configuration requise pour le système d’exploitation de l’application. Si un client de bureau de virtualisation des applications ne peut pas prendre en charge les systèmes d’exploitation sélectionnés, l’application ne démarre pas.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Contrôles</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Systèmes d’exploitation disponibles</strong></p></td>
<td align="left"><p>Affiche la liste des systèmes d’exploitation qui peuvent prendre en charge les applications du package.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Systèmes d’exploitation sélectionnés</strong></p></td>
<td align="left"><p>Affiche la liste des systèmes d’exploitation sélectionnés qui prennent en charge les applications du package.</p></td>
</tr>
</tbody>
</table>



## Options de sortie


Utilisez les contrôles **options de sortie** pour spécifier les options de sortie que l’application doit installer.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Contrôle</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Algorithme de compression</strong></p></td>
<td align="left"><p>Permet de sélectionner la méthode permettant de compresser le fichier SFT pour la diffusion en continu sur un réseau. Sélectionnez l’une des méthodes de compression suivantes:</p>
<ul>
<li><p><strong>Compressé </strong> : indique que le fichier SFT est compressé au <a href="https://go.microsoft.com/fwlink/?LinkId=111475" data-raw-source="[ZLIB](https://go.microsoft.com/fwlink/?LinkId=111475)"> format zlib </a> .</p></li>
<li><p><strong>Non compressé </strong> : la valeur par défaut spécifie que le fichier SFT ne doit pas être compressé.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Mettre en place des descripteurs de sécurité</strong></p></td>
<td align="left"><p>Sélectionnez cette option pour appliquer les descripteurs de sécurité des applications du package après leur déploiement sur le client.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Générer un package Microsoft Windows Installer (MSI)</strong></p></td>
<td align="left"><p>Pour installer ou déployer un package d’application séquencé à l’aide du programme d’installation Windows. Si vous avez apporté des modifications à l’aide du Sequencer, les modifications ne sont pas incluses dans le fichier du programme d’installation Windows. Le fichier du programme d’installation Windows sera toujours créé à l’aide du fichier. SFT enregistré sur le disque dur.</p></td>
</tr>
</tbody>
</table>



## Rubriques connexes


[Procédure pour modifier les propriétés de déploiement](how-to-change-deployment-properties.md)

[Console Sequencer](sequencer-console.md)









