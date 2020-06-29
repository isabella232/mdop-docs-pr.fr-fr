---
title: Paramètres Journalisation et suivi
description: Paramètres Journalisation et suivi
author: dansimp
ms.assetid: db6b43c7-fdde-4d11-b5ab-a81346e56940
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: bef0f8367647aad688c2aec7586ecdaae2e22143
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808366"
---
# <span data-ttu-id="abb51-103">Paramètres Journalisation et suivi</span><span class="sxs-lookup"><span data-stu-id="abb51-103">Logging and Tracing Settings</span></span>


<span data-ttu-id="abb51-104">Les paramètres de modèle d’administration de Advanced Group Policy Management (AGPM) vous permettent de configurer de manière centralisée les options de journalisation et de suivi des serveurs et clients AGPM pour lesquels un objet de stratégie de groupe avec ces paramètres est appliqué.</span><span class="sxs-lookup"><span data-stu-id="abb51-104">The Administrative Template settings for Advanced Group Policy Management (AGPM) enable you to centrally configure logging and tracing options for AGPM Servers and clients to which a Group Policy object (GPO) with these settings is applied.</span></span>

<span data-ttu-id="abb51-105">Le paramètre suivant est disponible sous Computer Configuration\\Administrative Templates\\Windows Components\\AGPM dans l' **éditeur d’objets de stratégie de groupe** lors de la modification d’un objet de stratégie de groupe dans la console de gestion des stratégies de groupe (GPMC).</span><span class="sxs-lookup"><span data-stu-id="abb51-105">The following setting is available under Computer Configuration\\Administrative Templates\\Windows Components\\AGPM in the **Group Policy Object Editor** when editing a GPO in the Group Policy Management Console (GPMC).</span></span> <span data-ttu-id="abb51-106">Si ce chemin d’accès n’est pas visible, cliquez avec le bouton droit sur **modèles d’administration**, puis ajoutez le modèle AGPM. admx ou AGPM. adm.</span><span class="sxs-lookup"><span data-stu-id="abb51-106">If this path is not visible, right-click **Administrative Templates**, and add the agpm.admx or agpm.adm template.</span></span>

<span data-ttu-id="abb51-107">**Emplacement des fichiers de suivi**:</span><span class="sxs-lookup"><span data-stu-id="abb51-107">**Trace file locations**:</span></span>

-   <span data-ttu-id="abb51-108">Client:%LocalAppData%\\Microsoft\\AGPM\\agpm.log</span><span class="sxs-lookup"><span data-stu-id="abb51-108">Client: %LocalAppData%\\Microsoft\\AGPM\\agpm.log</span></span>

-   <span data-ttu-id="abb51-109">Serveur:%CommonAppData%\\Microsoft\\AGPM\\agpmserv.log</span><span class="sxs-lookup"><span data-stu-id="abb51-109">Server: %CommonAppData%\\Microsoft\\AGPM\\agpmserv.log</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="abb51-110">Paramètre</span><span class="sxs-lookup"><span data-stu-id="abb51-110">Setting</span></span></th>
<th align="left"><span data-ttu-id="abb51-111">Effet</span><span class="sxs-lookup"><span data-stu-id="abb51-111">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="abb51-112">Journalisation d’AGPM</span><span class="sxs-lookup"><span data-stu-id="abb51-112">AGPM Logging</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="abb51-113">S’il est activé, ce paramètre configure si le suivi est activé et le niveau de détail.</span><span class="sxs-lookup"><span data-stu-id="abb51-113">If enabled, this setting configures whether tracing is turned on and the level of detail.</span></span> <span data-ttu-id="abb51-114">Ce paramètre affecte à la fois les composants client et serveur d’AGPM.</span><span class="sxs-lookup"><span data-stu-id="abb51-114">This setting affects both client and server components of AGPM.</span></span></p>
<p><span data-ttu-id="abb51-115">Si elle est désactivée ou n’est pas configurée, ce paramètre n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="abb51-115">If disabled or not configured, this setting has no effect.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="abb51-116">Références supplémentaires</span><span class="sxs-lookup"><span data-stu-id="abb51-116">Additional references</span></span>

-   [<span data-ttu-id="abb51-117">Paramètres de modèles d'administration</span><span class="sxs-lookup"><span data-stu-id="abb51-117">Administrative Template Settings</span></span>](administrative-template-settings.md)

 

 





