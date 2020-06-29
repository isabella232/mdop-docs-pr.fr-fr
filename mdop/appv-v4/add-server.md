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
# <span data-ttu-id="0f0f4-103">ADD SERVER</span><span class="sxs-lookup"><span data-stu-id="0f0f4-103">ADD SERVER</span></span>


<span data-ttu-id="0f0f4-104">Ajoute un serveur de publication.</span><span class="sxs-lookup"><span data-stu-id="0f0f4-104">Adds a publishing server.</span></span>

`SFTMIME ADD SERVER:server-name /HOST hostname /TYPE {HTTP|RTSP}                 /PATH path [/PORT port] [/REFRESH {ON|OFF}] [/SECURE]                 [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="0f0f4-105">Paramètre</span><span class="sxs-lookup"><span data-stu-id="0f0f4-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="0f0f4-106">Description</span><span class="sxs-lookup"><span data-stu-id="0f0f4-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0f0f4-107">SERVEUR: &lt; nom du serveur&gt;</span><span class="sxs-lookup"><span data-stu-id="0f0f4-107">SERVER:&lt;server-name&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="0f0f4-108">Nom d’affichage du serveur de publication.</span><span class="sxs-lookup"><span data-stu-id="0f0f4-108">The display name for the publishing server.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0f0f4-109">&lt;Nom d’hôte/host&gt;</span><span class="sxs-lookup"><span data-stu-id="0f0f4-109">/HOST &lt;hostname&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="0f0f4-110">Nom d’hôte ou adresse IP du serveur de publication.</span><span class="sxs-lookup"><span data-stu-id="0f0f4-110">The host name or IP address for the publishing server.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0f0f4-111">/TYPE {HTTP | RTSP</span><span class="sxs-lookup"><span data-stu-id="0f0f4-111">/TYPE {HTTP|RTSP}</span></span></p></td>
<td align="left"><p><span data-ttu-id="0f0f4-112">Indique s’il s’agit d’un serveur Web ( &quot; http &quot; ) ou d’un serveur de virtualisation des applications ( &quot; RTSP &quot; ).</span><span class="sxs-lookup"><span data-stu-id="0f0f4-112">Indicates whether the publishing server is a Web server (&quot;HTTP&quot;) or an Application Virtualization Server (&quot;RTSP&quot;).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0f0f4-113">/PORT &lt; port&gt;</span><span class="sxs-lookup"><span data-stu-id="0f0f4-113">/PORT &lt;port&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="0f0f4-114">Le port que le serveur de publication écoute.</span><span class="sxs-lookup"><span data-stu-id="0f0f4-114">The port on which the publishing server listens.</span></span> <span data-ttu-id="0f0f4-115">Par défaut, la valeur est 80 pour les serveurs HTTP normaux, 443 pour les serveurs HTTP utilisant une sécurité améliorée, 554 pour les serveurs de virtualisation des applications normaux et 322 pour les serveurs utilisant une sécurité améliorée.</span><span class="sxs-lookup"><span data-stu-id="0f0f4-115">Defaults to 80 for normal HTTP servers, 443 for HTTP servers using enhanced security, 554 for normal Application Virtualization Servers, and 322 for servers using enhanced security.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0f0f4-116">CheminAccès &lt; path&gt;</span><span class="sxs-lookup"><span data-stu-id="0f0f4-116">/PATH &lt;path&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="0f0f4-117">Partie Path de l’URL utilisée dans une demande de publication.</span><span class="sxs-lookup"><span data-stu-id="0f0f4-117">The path portion of the URL used in a publishing request.</span></span> <span data-ttu-id="0f0f4-118">Si le paramètre de TYPE est défini sur RTSP, le chemin d’accès est facultatif et est défini par défaut sur &quot; / &quot; .</span><span class="sxs-lookup"><span data-stu-id="0f0f4-118">If the TYPE parameter is set to RTSP, the path is optional and defaults to &quot;/&quot;.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0f0f4-119">/REFRESH</span><span class="sxs-lookup"><span data-stu-id="0f0f4-119">/REFRESH</span></span></p></td>
<td align="left"><p><span data-ttu-id="0f0f4-120">S’il est activé, les informations de publication seront actualisées lors de la connexion de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0f0f4-120">If set to ON, publishing information will be refreshed when the user logs in.</span></span> <span data-ttu-id="0f0f4-121">Est activé.</span><span class="sxs-lookup"><span data-stu-id="0f0f4-121">Defaults to ON.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0f0f4-122">/SECURE</span><span class="sxs-lookup"><span data-stu-id="0f0f4-122">/SECURE</span></span></p></td>
<td align="left"><p><span data-ttu-id="0f0f4-123">Le cas échéant, indique qu’une connexion avec une sécurité améliorée doit être établie sur le serveur de publication.</span><span class="sxs-lookup"><span data-stu-id="0f0f4-123">If present, indicates that a connection with enhanced security should be established to the publishing server.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0f0f4-124">/LOG</span><span class="sxs-lookup"><span data-stu-id="0f0f4-124">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="0f0f4-125">Si ce paramètre est spécifié, la sortie est enregistrée dans le nom du chemin d’accès spécifié.</span><span class="sxs-lookup"><span data-stu-id="0f0f4-125">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0f0f4-126">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="0f0f4-126">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="0f0f4-127">Si ce paramètre est spécifié, la sortie est présentée dans la fenêtre de la console active (par défaut).</span><span class="sxs-lookup"><span data-stu-id="0f0f4-127">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0f0f4-128">/GUI</span><span class="sxs-lookup"><span data-stu-id="0f0f4-128">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="0f0f4-129">Si ce paramètre est spécifié, la sortie est présentée dans une boîte de dialogue Windows.</span><span class="sxs-lookup"><span data-stu-id="0f0f4-129">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="0f0f4-130">Pour la version 4.6, l’option suivante a été ajoutée.</span><span class="sxs-lookup"><span data-stu-id="0f0f4-130">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0f0f4-131">/LOGU</span><span class="sxs-lookup"><span data-stu-id="0f0f4-131">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="0f0f4-132">Si ce paramètre est spécifié, la sortie est enregistrée dans le nom du chemin d’accès spécifié au format UNICODE.</span><span class="sxs-lookup"><span data-stu-id="0f0f4-132">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="0f0f4-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0f0f4-133">Related topics</span></span>


[<span data-ttu-id="0f0f4-134">Référence de commande SFTMIME</span><span class="sxs-lookup"><span data-stu-id="0f0f4-134">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





