---
title: CONFIGURE SERVER
description: CONFIGURE SERVER
author: dansimp
ms.assetid: c916eddd-74f2-46e4-953d-120b23284e37
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7757f281ec57645d20367056ba0013ef476a91a1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809077"
---
# <span data-ttu-id="b9a62-103">CONFIGURE SERVER</span><span class="sxs-lookup"><span data-stu-id="b9a62-103">CONFIGURE SERVER</span></span>


<span data-ttu-id="b9a62-104">Permet à un utilisateur de modifier l’installation d’un serveur; aucun paramètre non spécifié ne sera modifié.</span><span class="sxs-lookup"><span data-stu-id="b9a62-104">Enables a user to change the setup of a server; any settings not specified will not be modified.</span></span>

`SFTMIME CONFIGURE SERVER:server-name [/NAME display-name] [/HOST hostname]                 [/PORT port] [/PATH path] [/TYPE {HTTP|RTSP}]                 [/REFRESH {ON|OFF}] [/SECURE]                 [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b9a62-105">Paramètre</span><span class="sxs-lookup"><span data-stu-id="b9a62-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="b9a62-106">Description</span><span class="sxs-lookup"><span data-stu-id="b9a62-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b9a62-107">SERVEUR: &lt; nom du serveur&gt;</span><span class="sxs-lookup"><span data-stu-id="b9a62-107">SERVER:&lt;server-name&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9a62-108">Nom d’affichage du serveur de publication.</span><span class="sxs-lookup"><span data-stu-id="b9a62-108">The display name for the publishing server.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b9a62-109">/NOM d' &lt; affichage du nom&gt;</span><span class="sxs-lookup"><span data-stu-id="b9a62-109">/NAME &lt;display-name&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9a62-110">Nouveau nom d’affichage du serveur.</span><span class="sxs-lookup"><span data-stu-id="b9a62-110">New display name for the server.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b9a62-111">&lt;Nom d’hôte/host&gt;</span><span class="sxs-lookup"><span data-stu-id="b9a62-111">/HOST &lt;hostname&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9a62-112">Nom d’hôte ou adresse IP du serveur de publication.</span><span class="sxs-lookup"><span data-stu-id="b9a62-112">The host name or IP address for the publishing server.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b9a62-113">/PORT &lt; port&gt;</span><span class="sxs-lookup"><span data-stu-id="b9a62-113">/PORT &lt;port&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9a62-114">Le port que le serveur de publication écoute.</span><span class="sxs-lookup"><span data-stu-id="b9a62-114">The port on which the publishing server listens.</span></span> <span data-ttu-id="b9a62-115">Par défaut, la valeur est 80 pour les serveurs HTTP normaux, 443 pour les serveurs HTTP utilisant une sécurité améliorée, 554 pour les serveurs de virtualisation des applications normaux et 322 pour les serveurs utilisant une sécurité améliorée.</span><span class="sxs-lookup"><span data-stu-id="b9a62-115">Defaults to 80 for normal HTTP servers, 443 for HTTP servers using enhanced security, 554 for normal Application Virtualization Servers, and 322 for servers using enhanced security.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b9a62-116">CheminAccès &lt; path&gt;</span><span class="sxs-lookup"><span data-stu-id="b9a62-116">/PATH &lt;path&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9a62-117">Partie Path de l’URL utilisée dans une demande de publication.</span><span class="sxs-lookup"><span data-stu-id="b9a62-117">The path portion of the URL used in a publishing request.</span></span> <span data-ttu-id="b9a62-118">Si le paramètre de TYPE est défini sur RTSP, le chemin d’accès est facultatif et est défini par défaut sur &quot; / &quot; .</span><span class="sxs-lookup"><span data-stu-id="b9a62-118">If the TYPE parameter is set to RTSP, the path is optional and defaults to &quot;/&quot;.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b9a62-119">/TYPE</span><span class="sxs-lookup"><span data-stu-id="b9a62-119">/TYPE</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9a62-120">Indique s’il s’agit d’un serveur Web ( &quot; http &quot; ) ou d’un serveur de virtualisation des applications ( &quot; RTSP &quot; ).</span><span class="sxs-lookup"><span data-stu-id="b9a62-120">Indicates whether the publishing server is a Web server (&quot;HTTP&quot;) or an Application Virtualization Server (&quot;RTSP&quot;).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b9a62-121">/REFRESH</span><span class="sxs-lookup"><span data-stu-id="b9a62-121">/REFRESH</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9a62-122">S’il est activé, les informations de publication seront actualisées lors de la connexion de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b9a62-122">If set to ON, publishing information will be refreshed when the user logs in.</span></span> <span data-ttu-id="b9a62-123">Est activé.</span><span class="sxs-lookup"><span data-stu-id="b9a62-123">Defaults to ON.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b9a62-124">/SECURE</span><span class="sxs-lookup"><span data-stu-id="b9a62-124">/SECURE</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9a62-125">Le cas échéant, indique qu’une connexion avec une sécurité améliorée doit être établie sur le serveur de publication.</span><span class="sxs-lookup"><span data-stu-id="b9a62-125">If present, indicates that a connection with enhanced security should be established to the publishing server.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b9a62-126">/LOG</span><span class="sxs-lookup"><span data-stu-id="b9a62-126">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9a62-127">Si ce paramètre est spécifié, la sortie est enregistrée dans le nom du chemin d’accès spécifié.</span><span class="sxs-lookup"><span data-stu-id="b9a62-127">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b9a62-128">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="b9a62-128">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9a62-129">Si ce paramètre est spécifié, la sortie est présentée dans la fenêtre de la console active (par défaut).</span><span class="sxs-lookup"><span data-stu-id="b9a62-129">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b9a62-130">/GUI</span><span class="sxs-lookup"><span data-stu-id="b9a62-130">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9a62-131">Si ce paramètre est spécifié, la sortie est présentée dans une boîte de dialogue Windows.</span><span class="sxs-lookup"><span data-stu-id="b9a62-131">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="b9a62-132">Pour la version 4.6, l’option suivante a été ajoutée.</span><span class="sxs-lookup"><span data-stu-id="b9a62-132">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b9a62-133">/LOGU</span><span class="sxs-lookup"><span data-stu-id="b9a62-133">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9a62-134">Si ce paramètre est spécifié, la sortie est enregistrée dans le nom du chemin d’accès spécifié au format UNICODE.</span><span class="sxs-lookup"><span data-stu-id="b9a62-134">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="b9a62-135">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b9a62-135">Related topics</span></span>


[<span data-ttu-id="b9a62-136">Référence de commande SFTMIME</span><span class="sxs-lookup"><span data-stu-id="b9a62-136">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





