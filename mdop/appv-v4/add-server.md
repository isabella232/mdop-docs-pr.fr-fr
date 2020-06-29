---
title: ADD SERVER
description: ADD SERVER
author: dansimp
ms.assetid: 4be2ac2e-a410-4711-9f84-f305393c8fa7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e15a5943b40e14b2f9031bf8b3ddffa693e32dea
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808086"
---
# ADD SERVER


Ajoute un serveur de publication.

`SFTMIME ADD SERVER:server-name /HOST hostname /TYPE {HTTP|RTSP}                 /PATH path [/PORT port] [/REFRESH {ON|OFF}] [/SECURE]                 [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Paramètre</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>SERVEUR: &lt; nom du serveur&gt;</p></td>
<td align="left"><p>Nom d’affichage du serveur de publication.</p></td>
</tr>
<tr class="even">
<td align="left"><p>&lt;Nom d’hôte/host&gt;</p></td>
<td align="left"><p>Nom d’hôte ou adresse IP du serveur de publication.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/TYPE {HTTP | RTSP</p></td>
<td align="left"><p>Indique s’il s’agit d’un serveur Web ( &quot; http &quot; ) ou d’un serveur de virtualisation des applications ( &quot; RTSP &quot; ).</p></td>
</tr>
<tr class="even">
<td align="left"><p>/PORT &lt; port&gt;</p></td>
<td align="left"><p>Le port que le serveur de publication écoute. Par défaut, la valeur est 80 pour les serveurs HTTP normaux, 443 pour les serveurs HTTP utilisant une sécurité améliorée, 554 pour les serveurs de virtualisation des applications normaux et 322 pour les serveurs utilisant une sécurité améliorée.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>CheminAccès &lt; path&gt;</p></td>
<td align="left"><p>Partie Path de l’URL utilisée dans une demande de publication. Si le paramètre de TYPE est défini sur RTSP, le chemin d’accès est facultatif et est défini par défaut sur &quot; / &quot; .</p></td>
</tr>
<tr class="even">
<td align="left"><p>/REFRESH</p></td>
<td align="left"><p>S’il est activé, les informations de publication seront actualisées lors de la connexion de l’utilisateur. Est activé.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/SECURE</p></td>
<td align="left"><p>Le cas échéant, indique qu’une connexion avec une sécurité améliorée doit être établie sur le serveur de publication.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/LOG</p></td>
<td align="left"><p>Si ce paramètre est spécifié, la sortie est enregistrée dans le nom du chemin d’accès spécifié.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/CONSOLE</p></td>
<td align="left"><p>Si ce paramètre est spécifié, la sortie est présentée dans la fenêtre de la console active (par défaut).</p></td>
</tr>
<tr class="even">
<td align="left"><p>/GUI</p></td>
<td align="left"><p>Si ce paramètre est spécifié, la sortie est présentée dans une boîte de dialogue Windows.</p></td>
</tr>
</tbody>
</table>

 

Pour la version 4.6, l’option suivante a été ajoutée.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>/LOGU</p></td>
<td align="left"><p>Si ce paramètre est spécifié, la sortie est enregistrée dans le nom du chemin d’accès spécifié au format UNICODE.</p></td>
</tr>
</tbody>
</table>

 

## Rubriques connexes


[Référence de commande SFTMIME](sftmime--command-reference.md)

 

 





