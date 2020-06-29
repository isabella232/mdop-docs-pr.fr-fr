---
title: Procédure pour importer une application
description: Procédure pour importer une application
author: dansimp
ms.assetid: ab40acad-1025-478d-8e13-0e1ff1bd37e4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7d9cd6d065ca28b5d856acdae7d10a1280105e9d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807093"
---
# <span data-ttu-id="b491a-103">Procédure pour importer une application</span><span class="sxs-lookup"><span data-stu-id="b491a-103">How to Import an Application</span></span>


<span data-ttu-id="b491a-104">En règle générale, vous importez des applications pour les rendre accessibles au flux d’un serveur de gestion des applications.</span><span class="sxs-lookup"><span data-stu-id="b491a-104">Typically, you import applications to make them available to stream from an Application Virtualization Management Server.</span></span> <span data-ttu-id="b491a-105">Vous pouvez également ajouter une application manuellement, mais vous devez fournir des informations précises et détaillées sur celle-ci.</span><span class="sxs-lookup"><span data-stu-id="b491a-105">You can also add an application manually, but you must provide precise, detailed information about the application to do so.</span></span> <span data-ttu-id="b491a-106">Pour plus d’informations, voir [comment ajouter une application manuellement](how-to-manually-add-an-application.md).</span><span class="sxs-lookup"><span data-stu-id="b491a-106">For more information, see [How to Manually Add an Application](how-to-manually-add-an-application.md).</span></span>

<span data-ttu-id="b491a-107">**Remarques**  Pour importer une application, vous devez disposer d’un fichier d’OSD (Open Software Descriptor) en séquence ou du fichier de projet de séquence (SPRJ) sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="b491a-107">**Note** To import an application, you must have its sequenced Open Software Descriptor (OSD) file or its Sequencer Project (SPRJ) file available on the server.</span></span>

 

<span data-ttu-id="b491a-108">Lors de l’importation d’une application, assurez-vous que le serveur est configuré à l’aide d’une valeur dans le champ **chemin d’accès par défaut** sous l’onglet **général** de la boîte de dialogue **Options système** (accessible en cliquant avec le bouton droit sur le nœud **système de virtualisation des applications** dans la console App-V Server).</span><span class="sxs-lookup"><span data-stu-id="b491a-108">When importing an application, you should make sure the server is configured with a value in the **Default Content Path** field on the **General** tab of the **System Options** dialog (accessible by right-clicking the **Application Virtualization System** node in the App-V Server Console).</span></span> <span data-ttu-id="b491a-109">La valeur de chemin d’accès par défaut définit l’emplacement d’importation des applications, et Pendant le processus d’importation, cette valeur est utilisée pour modifier les chemins d’accès définis dans le fichier OSD du fichier SFT et des raccourcis d’icônes.</span><span class="sxs-lookup"><span data-stu-id="b491a-109">The default content path value defines where the applications will be imported, and during the import process, this value is used to modify the paths defined in the OSD file for the SFT file and for the icon shortcuts.</span></span> <span data-ttu-id="b491a-110">Dans le fichier OSD, le chemin d’accès du fichier SFT est spécifié dans l’entrée du code base HREF et le chemin d’accès des icônes est indiqué dans l’entrée raccourcis.</span><span class="sxs-lookup"><span data-stu-id="b491a-110">In the OSD file, the path for the SFT file is specified in the CODEBASE HREF entry and the path for the icons is specified in the SHORTCUTS entry.</span></span>

<span data-ttu-id="b491a-111">Pendant le processus d’importation, le protocole, le serveur et, le cas échéant, le port spécifié dans ces deux chemins d’accès au fichier OSD est remplacé par la valeur du chemin d’accès au contenu par défaut.</span><span class="sxs-lookup"><span data-stu-id="b491a-111">During the import process, the protocol, server, and, if present, port specified in these two paths in the OSD file will be replaced with the value from the default content path.</span></span> <span data-ttu-id="b491a-112">Le tableau suivant illustre un exemple de la façon dont le chemin d’importation sera affecté.</span><span class="sxs-lookup"><span data-stu-id="b491a-112">The following table provides an example of how the import path will be affected.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b491a-113">Chemin d’accès au contenu par défaut</span><span class="sxs-lookup"><span data-stu-id="b491a-113">Default Content Path</span></span></th>
<th align="left"><span data-ttu-id="b491a-114">CODE base de fichier OSD HREF</span><span class="sxs-lookup"><span data-stu-id="b491a-114">OSD File CODEBASE HREF</span></span></th>
<th align="left"><span data-ttu-id="b491a-115">Valeur résultante</span><span class="sxs-lookup"><span data-stu-id="b491a-115">Resulting Value</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b491a-116">\server\content &lt; /p&gt;</span><span class="sxs-lookup"><span data-stu-id="b491a-116">\server\content&lt;/p&gt;</span></span></td>
<td align="left"><p><a href="http://WebServer/myFolder/package.sft" data-raw-source="http://WebServer/myFolder/package.sft">http://WebServer/myFolder/package.sft</a></p></td>
<td align="left"><p><span data-ttu-id="b491a-117">\server\content\myFolder\package.sft</span><span class="sxs-lookup"><span data-stu-id="b491a-117">\server\content\myFolder\package.sft</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="b491a-118">Pour importer une application</span><span class="sxs-lookup"><span data-stu-id="b491a-118">To import an application</span></span>**

1.  <span data-ttu-id="b491a-119">Dans le volet gauche, cliquez avec le bouton droit sur le nœud **applications** et sélectionnez **importer des applications**.</span><span class="sxs-lookup"><span data-stu-id="b491a-119">Right-click the **Applications** node in the left pane, and choose **Import Applications**.</span></span>

2.  <span data-ttu-id="b491a-120">Dans la boîte de dialogue **ouvrir** , accédez au fichier SPRJ ou OSD de l’application.</span><span class="sxs-lookup"><span data-stu-id="b491a-120">In the **Open** dialog box, navigate to the application's SPRJ or OSD file.</span></span> <span data-ttu-id="b491a-121">Mettez en surbrillance le fichier, puis cliquez sur **ouvrir**.</span><span class="sxs-lookup"><span data-stu-id="b491a-121">Highlight the file and click **Open**.</span></span>

3.  <span data-ttu-id="b491a-122">Dans l' **Assistant Nouvelle application**, assurez-vous que la case **activé** est cochée pour les applications que vous voulez diffuser.</span><span class="sxs-lookup"><span data-stu-id="b491a-122">In the **New Application Wizard**, be sure the **Enabled** box is selected for applications you want to stream.</span></span> <span data-ttu-id="b491a-123">Vous pouvez également entrer une description et vérifier les chemins d’accès au serveur et aux fichiers.</span><span class="sxs-lookup"><span data-stu-id="b491a-123">There you can also enter a description and verify the server and file paths.</span></span> <span data-ttu-id="b491a-124">Par ailleurs, si vous avez configuré une licence et des groupes de serveurs, vous pouvez les sélectionner.</span><span class="sxs-lookup"><span data-stu-id="b491a-124">Also, if you have set up license and server groups, you can select those.</span></span>

4.  <span data-ttu-id="b491a-125">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="b491a-125">Click **Next**.</span></span>

5.  <span data-ttu-id="b491a-126">Dans l’écran **raccourcis clavier publiés** , sélectionnez les zones correspondant aux emplacements dans lesquels vous souhaitez que les raccourcis d’application apparaissent sur les ordinateurs clients.</span><span class="sxs-lookup"><span data-stu-id="b491a-126">On the **Published Shortcuts** screen, select the boxes for the locations where you would like the application shortcuts to appear on the client computers.</span></span>

6.  <span data-ttu-id="b491a-127">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="b491a-127">Click **Next**.</span></span>

7.  <span data-ttu-id="b491a-128">Dans l’écran **associations de fichiers** , vous pouvez ajouter de nouvelles associations de fichiers à cette application.</span><span class="sxs-lookup"><span data-stu-id="b491a-128">In the **File Associations** screen, you can add new file associations to this application.</span></span> <span data-ttu-id="b491a-129">Pour cela, cliquez sur **Ajouter**, entrez l’extension (sans point précédent), entrez une description, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="b491a-129">To do so, click **Add**, enter the extension (without a preceding dot), enter a description, and click **OK**.</span></span>

    <span data-ttu-id="b491a-130">**Remarques**  Applications séquencées avec Sequencer 4,0 Complétez la boîte de dialogue **associations de fichiers** lors de l’importation ou de la création via la console de gestion.</span><span class="sxs-lookup"><span data-stu-id="b491a-130">**Note** Applications sequenced with Sequencer 4.0 populate the **File Associations** dialog box when you import or create them through the management console.</span></span> <span data-ttu-id="b491a-131">Les applications avec des packages de version de Sequencer antérieurs ne le sont pas.</span><span class="sxs-lookup"><span data-stu-id="b491a-131">Applications with previous Sequencer version packages do not.</span></span>

     

8.  <span data-ttu-id="b491a-132">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="b491a-132">Click **Next**.</span></span>

9.  <span data-ttu-id="b491a-133">Dans l’écran **autorisations d’accès** , cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="b491a-133">In the **Access Permissions** screen, click **Add**.</span></span>

10. <span data-ttu-id="b491a-134">Complétez la boîte de dialogue **Sélectionner des groupes** .</span><span class="sxs-lookup"><span data-stu-id="b491a-134">Complete the **Select Groups** dialog box.</span></span> <span data-ttu-id="b491a-135">Lorsque vous avez terminé, cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="b491a-135">When you finish, click **OK**.</span></span>

11. <span data-ttu-id="b491a-136">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="b491a-136">Click **Next**.</span></span>

12. <span data-ttu-id="b491a-137">Dans l’écran **Résumé** , vous pouvez consulter les paramètres d’importation.</span><span class="sxs-lookup"><span data-stu-id="b491a-137">On the **Summary** screen, you can review the import settings.</span></span> <span data-ttu-id="b491a-138">Cliquez sur **Terminer**, ou cliquez sur **précédent** pour changer d’importation ou cliquez sur **Annuler** pour annuler l’importation.</span><span class="sxs-lookup"><span data-stu-id="b491a-138">Click **Finish**, or click **Back** to change the import or click **Cancel** to cancel the import.</span></span>

## <span data-ttu-id="b491a-139">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b491a-139">Related topics</span></span>


[<span data-ttu-id="b491a-140">Procédure pour gérer des groupes d'applications dans Server Management Console</span><span class="sxs-lookup"><span data-stu-id="b491a-140">How to Manage Application Groups in the Server Management Console</span></span>](how-to-manage-application-groups-in-the-server-management-console.md)

[<span data-ttu-id="b491a-141">Procédure pour gérer des applications dans Server Management Console</span><span class="sxs-lookup"><span data-stu-id="b491a-141">How to Manage Applications in the Server Management Console</span></span>](how-to-manage-applications-in-the-server-management-console.md)

[<span data-ttu-id="b491a-142">Procédure pour ajouter manuellement une application</span><span class="sxs-lookup"><span data-stu-id="b491a-142">How to Manually Add an Application</span></span>](how-to-manually-add-an-application.md)

 

 





