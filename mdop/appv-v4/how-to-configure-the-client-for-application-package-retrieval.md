---
title: Procédure pour configurer le client afin d'extraire le package d'application
description: Procédure pour configurer le client afin d'extraire le package d'application
author: dansimp
ms.assetid: 891f2739-da7a-46da-b452-b8c0af075525
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f5eeb0b977c6ecd44947d5d1c42d25d47b9e2530
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807262"
---
# Procédure pour configurer le client afin d'extraire le package d'application


Lorsque le client est configuré à l’aide d’un serveur de gestion des applications (App-V) en tant que serveur de publication, par défaut lors du prochain cycle d’actualisation de la publication, le client récupère à partir du serveur les fichiers du manifeste de l’OSD (Open Software Descriptor) et du manifeste de package pour chaque package que l’utilisateur est autorisé à utiliser. Le client utilise les informations de source de package définies dans ces fichiers pour déterminer où trouver le contenu, les icônes et les associations de types de fichiers du package.

Si vous voulez que le client obtienne le contenu du package (fichier SFT) à partir d’un serveur de streaming App-V local ou d’une autre source, telle qu’un serveur Web ou un serveur de fichiers, au lieu du serveur d’administration App-V, vous pouvez configurer la valeur de clé de registre ApplicationSourceRoot sur l’ordinateur de manière à ce qu’elle pointe vers le partage de contenu local sur Le fichier OSD définit quand même le chemin source d’origine pour le contenu du package. Toutefois, le client utilise la valeur du paramètre ApplicationSourceRoot à la place du serveur et du partage spécifiés dans le chemin d’accès du contenu du fichier OSD. Cette opération permet de rediriger le client pour récupérer le contenu à partir de l’autre serveur.

Vous pouvez également configurer les valeurs de clé de Registre OSDSourceRoot et IconSourceRoot si vous souhaitez remplacer ces paramètres dans le fichier manifeste du package ou dans les chemins d’accès envoyés par un serveur de publication. OSDSourceRoot spécifie un emplacement source pour la récupération de fichier OSD pour un package d’application au cours de la publication. IconSourceRoot spécifie un emplacement source pour la récupération d’icône pour un package d’application lors de la publication.

**Remarque**  
-   Les paramètres IconSourceRoot et OSDSourceRoot remplacent les valeurs figurant dans le fichier manifeste du package, de sorte que si vous tentez de déployer un package à l’aide de la méthode de fichier Windows Installer (. msi), il remplacera également les valeurs du fichier manifeste de package contenu dans ce fichier. msi.

-   Au cours des opérations de diffusion en continu de publication et HTTP (S), les clients App-V 4,5 SP1 utilisent les paramètres du serveur proxy configurés dans Internet Explorer sur l’ordinateur de l’utilisateur.



**Pour configurer la valeur de clé de registre ApplicationSourceRoot**

-   Dans la valeur de clé de Registre suivante, configurez le ApplicationSourceRoot à l’aide d’un chemin UNC ou d’une URL:

    HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\ApplicationSourceRoot

    Le format correct pour le chemin d’accès UNC (Universal Naming Convention) est **\\\\computername\\sharefolder\\\ [dossier \] \ [\ \ \]**, où le **dossier** est facultatif. **Nomordinateur** peut être un nom de domaine complet (FQDN, Fully Qualified Domain Name) ou une adresse IP, et **ShareFolder** peut être une lettre d’unité. Seule la partie **\\\\computername\\sharedfolder** ou lettre de lecteur du chemin OSD est remplacée.

    Le format correct pour le chemin d’accès URL est **Protocol://servername: \ [port \] \ [/path\] \ [/\]**, où le **port** et le **chemin d’accès** sont facultatifs. Si **port** n’est pas spécifié, le port par défaut du protocole est utilisé. Seule la partie **protocole://Server: port** de l’URL d’OSD est remplacée.

    **Important**  
    Les variables d’environnement ne sont pas prises en charge dans la définition de ApplicationSourceRoot.



~~~
The following table lists examples of acceptable URL and UNC path formats.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">ApplicationSourceRoot</th>
<th align="left">OSD File HREF Path</th>
<th align="left">Result</th>
<th align="left">Comments</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>rtsps://mainserver:322</p></td>
<td align="left"><p>rtsp://appserver/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p>rtsps://mainserver:322/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>rtsps://mainserver:322/prodapps</p></td>
<td align="left"><p>rtsp://appserver/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p>rtsps://mainserver:322/prodapps/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>https://mainserver:443/prodapps</p></td>
<td align="left"><p>rtsp://appserver/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p>https://mainserver:443/prodapps/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>rtsps://mainserver:322/prodapps</p></td>
<td align="left"><p>rtsp://%SFT_APPVSERVER%:554/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p>rtsps://mainserver:322/prodapps/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>rtsps://mainserver:322</p></td>
<td align="left"><p>\\uncserver\share\productivity\office2k3.sft</p></td>
<td align="left"><p>rtsps://mainserver:322/productivity/office2k3.sft</p></td>
<td align="left"><p>‘\’ converted to ‘/’</p></td>
</tr>
<tr class="even">
<td align="left"><p>rtsps://mainserver:322</p></td>
<td align="left"><p>file://\\uncserver\share\productivity\office2k3.sft</p></td>
<td align="left"><p>rtsps://mainserver:322/productivity/office2k3.sft</p></td>
<td align="left"><p>‘\’ converted to ‘/’</p></td>
</tr>
<tr class="odd">
<td align="left"><p>\\uncserver\share</p></td>
<td align="left"><p>rtsp://appserver/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p>\\uncserver\share\productivity\office2k3.sft</p></td>
<td align="left"><p>‘/’ converted to ‘\’ and parameter dropped when converting to UNC path</p></td>
</tr>
<tr class="even">
<td align="left"><p>\\uncserver\share\prodapps</p></td>
<td align="left"><p>rtsp://appserver/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p>\\uncserver\share\prodapps\productivity\office2k3.sft</p></td>
<td align="left"><p>‘/’ converted to ‘\’ and parameter dropped when converting to UNC path</p></td>
</tr>
<tr class="odd">
<td align="left"><p>M:</p></td>
<td align="left"><p>\\uncserver\share\productivity\office2k3.sft</p></td>
<td align="left"><p>M:\productivity\office2k3.sft</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>M:\prodapps</p></td>
<td align="left"><p>\\uncserver\share\productivity\office2k3.sft</p></td>
<td align="left"><p>M:\prodapps\productivity\office2k3.sft</p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>
~~~



**Pour configurer la valeur OSDSourceRoot**

-   Dans la valeur de clé de Registre suivante, configurez le OSDSourceRoot à l’aide d’un chemin UNC ou d’une URL:

    HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\OSDSourceRoot

    Les formats acceptables pour le OSDSourceRoot incluent des chemins d’accès UNC et des URL, comme dans l’exemple suivant:

    **\\\\computername\\sharefolder\\resource** ou **\\\\computername\\content** ou ** &lt; Drive &gt; : \\FolderName**

    **http://computername/productivity/** ou**https://computername/productivity/**

**Pour configurer la valeur IconSourceRoot**

-   Dans la valeur de clé de Registre suivante, configurez le IconSourceRoot à l’aide d’un chemin UNC ou d’une URL:

    HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\IconSourceRoot

    Les formats acceptables pour le IconSourceRoot incluent des chemins d’accès UNC et des URL, comme dans l’exemple suivant:

    **\\\\computername\\sharefolder\\resource** ou **\\\\computername\\content** ou ** &lt; Drive &gt; : \\FolderName**

    **http://computername/productivity/** ou**https://computername/productivity/**

## Rubriques connexes


[Procédure pour configurer les paramètres de registre du client App-V Client à l'aide de la ligne de commande](how-to-configure-the-app-v-client-registry-settings-by-using-the-command-line.md)









