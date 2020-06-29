---
title: Déploiement de Microsoft Office2010 à l'aide d'App-V
description: Déploiement de Microsoft Office2010 à l'aide d'App-V
author: dansimp
ms.assetid: ae0b0459-c0d6-4946-b62d-ff153f52d1fb
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 90454373e9a1c894eba8cbf1b8642656b986bc94
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805868"
---
# <span data-ttu-id="c1a2d-103">Déploiement de Microsoft Office2010 à l'aide d'App-V</span><span class="sxs-lookup"><span data-stu-id="c1a2d-103">Deploying Microsoft Office 2010 by Using App-V</span></span>


<span data-ttu-id="c1a2d-104">Vous pouvez créer des packages Office 2010 pour Microsoft Application Virtualization (App-V) 5,1 à l’aide de l’une des méthodes suivantes:</span><span class="sxs-lookup"><span data-stu-id="c1a2d-104">You can create Office 2010 packages for Microsoft Application Virtualization (App-V) 5.1 using one of the following methods:</span></span>

-   <span data-ttu-id="c1a2d-105">Sequencer Application Virtualization (App-V)</span><span class="sxs-lookup"><span data-stu-id="c1a2d-105">Application Virtualization (App-V) Sequencer</span></span>

-   <span data-ttu-id="c1a2d-106">Accélérateur de package Application Virtualization (App-V)</span><span class="sxs-lookup"><span data-stu-id="c1a2d-106">Application Virtualization (App-V) Package Accelerator</span></span>

## <span data-ttu-id="c1a2d-107">Prise en charge de App-V pour Office 2010</span><span class="sxs-lookup"><span data-stu-id="c1a2d-107">App-V support for Office 2010</span></span>


<span data-ttu-id="c1a2d-108">Le tableau suivant indique les versions d’App-V, les méthodes de création de packages Office, les licences prises en charge et les déploiements pris en charge pour Office 2010.</span><span class="sxs-lookup"><span data-stu-id="c1a2d-108">The following table shows the App-V versions, methods of Office package creation, supported licensing, and supported deployments for Office 2010.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c1a2d-109">Élément pris en charge</span><span class="sxs-lookup"><span data-stu-id="c1a2d-109">Supported item</span></span></th>
<th align="left"><span data-ttu-id="c1a2d-110">Niveau de prise en charge</span><span class="sxs-lookup"><span data-stu-id="c1a2d-110">Level of support</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c1a2d-111">Versions d’App-V prises en charge</span><span class="sxs-lookup"><span data-stu-id="c1a2d-111">Supported App-V versions</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="c1a2d-112">4,6</span><span class="sxs-lookup"><span data-stu-id="c1a2d-112">4.6</span></span></p></li>
<li><p><span data-ttu-id="c1a2d-113">5.0</span><span class="sxs-lookup"><span data-stu-id="c1a2d-113">5.0</span></span></p></li>
<li><p><span data-ttu-id="c1a2d-114">5,1</span><span class="sxs-lookup"><span data-stu-id="c1a2d-114">5.1</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c1a2d-115">Création de package</span><span class="sxs-lookup"><span data-stu-id="c1a2d-115">Package creation</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="c1a2d-116">Séquençage</span><span class="sxs-lookup"><span data-stu-id="c1a2d-116">Sequencing</span></span></p></li>
<li><p><span data-ttu-id="c1a2d-117">Package Accelerator</span><span class="sxs-lookup"><span data-stu-id="c1a2d-117">Package Accelerator</span></span></p></li>
<li><p><span data-ttu-id="c1a2d-118">Kit de déploiement Office</span><span class="sxs-lookup"><span data-stu-id="c1a2d-118">Office Deployment Kit</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c1a2d-119">Licences prises en charge</span><span class="sxs-lookup"><span data-stu-id="c1a2d-119">Supported licensing</span></span></p></td>
<td align="left"><p><span data-ttu-id="c1a2d-120">Gestion des licences en volume</span><span class="sxs-lookup"><span data-stu-id="c1a2d-120">Volume Licensing</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c1a2d-121">Déploiements pris en charge</span><span class="sxs-lookup"><span data-stu-id="c1a2d-121">Supported deployments</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="c1a2d-122">Bureau</span><span class="sxs-lookup"><span data-stu-id="c1a2d-122">Desktop</span></span></p></li>
<li><p><span data-ttu-id="c1a2d-123">VDI personnel</span><span class="sxs-lookup"><span data-stu-id="c1a2d-123">Personal VDI</span></span></p></li>
<li><p><span data-ttu-id="c1a2d-124">RDS</span><span class="sxs-lookup"><span data-stu-id="c1a2d-124">RDS</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="c1a2d-125">Création d’une application Office 2010-V 5,1 à l’aide du Sequencer</span><span class="sxs-lookup"><span data-stu-id="c1a2d-125">Creating Office 2010 App-V 5.1 using the sequencer</span></span>


<span data-ttu-id="c1a2d-126">Le séquençage d’Office 2010 est l’une des principales méthodes de création d’un package Office 2010 sur App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="c1a2d-126">Sequencing Office 2010 is one of the main methods for creating an Office 2010 package on App-V 5.1.</span></span> <span data-ttu-id="c1a2d-127">Microsoft a fourni une recette détaillée par le biais d’un article de la base de connaissances.</span><span class="sxs-lookup"><span data-stu-id="c1a2d-127">Microsoft has provided a detailed recipe through a Knowledge Base article.</span></span> <span data-ttu-id="c1a2d-128">Pour créer un package 2010 Office sur App-V 5,1, voir les liens suivants pour obtenir des instructions détaillées:</span><span class="sxs-lookup"><span data-stu-id="c1a2d-128">To create an Office 2010 package on App-V 5.1, refer to the following link for detailed instructions:</span></span>

[<span data-ttu-id="c1a2d-129">Comment séquencer Microsoft Office 2010 dans Microsoft Application Virtualization 5,0</span><span class="sxs-lookup"><span data-stu-id="c1a2d-129">How To Sequence Microsoft Office 2010 in Microsoft Application Virtualization 5.0</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330676)

## <span data-ttu-id="c1a2d-130">Créer des packages App-V 5,1 Office 2010 à l’aide des accélérateurs de package</span><span class="sxs-lookup"><span data-stu-id="c1a2d-130">Creating Office 2010 App-V 5.1 packages using package accelerators</span></span>


<span data-ttu-id="c1a2d-131">Les packages App-V 5,1 d’Office 2010 peuvent être créés via accélérateurs de package.</span><span class="sxs-lookup"><span data-stu-id="c1a2d-131">Office 2010 App-V 5.1 packages can be created through package accelerators.</span></span> <span data-ttu-id="c1a2d-132">Microsoft a fourni des accélérateurs de package pour la création d’Office 2010 sur Windows 10, Windows 8 et Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c1a2d-132">Microsoft has provided package accelerators for creating Office 2010 on Windows 10, Windows 8 and Windows 7.</span></span> <span data-ttu-id="c1a2d-133">Pour créer des packages Office 2010 sur App-V à l’aide d’accélérateurs de package, reportez-vous aux pages suivantes pour accéder à l’accélérateur de package approprié:</span><span class="sxs-lookup"><span data-stu-id="c1a2d-133">To create Office 2010 packages on App-V using Package accelerators, refer to the following pages to access the appropriate package accelerator:</span></span>

-   [<span data-ttu-id="c1a2d-134">App-V 5,0 package Accelerator pour Office professionnel plus 2010 – Windows 8</span><span class="sxs-lookup"><span data-stu-id="c1a2d-134">App-V 5.0 Package Accelerator for Office Professional Plus 2010 – Windows 8</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330677)

-   [<span data-ttu-id="c1a2d-135">App-V 5,0 package Accelerator pour Office professionnel plus 2010-Windows 7</span><span class="sxs-lookup"><span data-stu-id="c1a2d-135">App-V 5.0 Package Accelerator for Office Professional Plus 2010 – Windows 7</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330678)

<span data-ttu-id="c1a2d-136">Pour obtenir des instructions détaillées sur la création de packages d’applications virtuelles à l’aide des accélérateurs de package App-V, voir [créer un package d’application virtuelle à l’aide d’un accélérateur de package App-v](how-to-create-a-virtual-application-package-using-an-app-v-package-accelerator51.md).</span><span class="sxs-lookup"><span data-stu-id="c1a2d-136">For detailed instructions on how to create virtual application packages using App-V package accelerators, see [How to Create a Virtual Application Package Using an App-V Package Accelerator](how-to-create-a-virtual-application-package-using-an-app-v-package-accelerator51.md).</span></span>

## <span data-ttu-id="c1a2d-137">Déploiement du package Microsoft Office pour App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="c1a2d-137">Deploying the Microsoft Office package for App-V 5.1</span></span>


<span data-ttu-id="c1a2d-138">Vous pouvez déployer les packages Office 2010 à l’aide de l’une des méthodes de déploiement d’App-V suivantes:</span><span class="sxs-lookup"><span data-stu-id="c1a2d-138">You can deploy Office 2010 packages by using any of the following App-V deployment methods:</span></span>

-   <span data-ttu-id="c1a2d-139">SystemCenterConfigurationManager</span><span class="sxs-lookup"><span data-stu-id="c1a2d-139">System Center Configuration Manager</span></span>

-   <span data-ttu-id="c1a2d-140">App-V Server</span><span class="sxs-lookup"><span data-stu-id="c1a2d-140">App-V server</span></span>

-   <span data-ttu-id="c1a2d-141">Commandes PowerShell autonomes</span><span class="sxs-lookup"><span data-stu-id="c1a2d-141">Stand-alone through PowerShell commands</span></span>

## <span data-ttu-id="c1a2d-142">Gestion et personnalisation des packages App-V pour Office</span><span class="sxs-lookup"><span data-stu-id="c1a2d-142">Office App-V package management and customization</span></span>


<span data-ttu-id="c1a2d-143">Les packages 2010 Office peuvent être gérés comme n’importe quel autre package App-V 5,1 par le biais de mécanismes de gestion des packages connus.</span><span class="sxs-lookup"><span data-stu-id="c1a2d-143">Office 2010 packages can be managed like any other App-V 5.1 packages through known package management mechanisms.</span></span> <span data-ttu-id="c1a2d-144">Aucune instruction spéciale n’est nécessaire (par exemple, pour ajouter, publier, annuler ou supprimer des packages Office).</span><span class="sxs-lookup"><span data-stu-id="c1a2d-144">No special instructions are needed, for example, to add, publish, unpublish, or remove Office packages.</span></span>

## <span data-ttu-id="c1a2d-145">Intégration de Microsoft Office à Windows</span><span class="sxs-lookup"><span data-stu-id="c1a2d-145">Microsoft Office integration with Windows</span></span>


<span data-ttu-id="c1a2d-146">Le tableau suivant répertorie la liste complète des points d’intégration pris en charge pour Office 2010.</span><span class="sxs-lookup"><span data-stu-id="c1a2d-146">The following table provides a full list of supported integration points for Office 2010.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c1a2d-147">Point d’extension</span><span class="sxs-lookup"><span data-stu-id="c1a2d-147">Extension Point</span></span></th>
<th align="left"><span data-ttu-id="c1a2d-148">Description</span><span class="sxs-lookup"><span data-stu-id="c1a2d-148">Description</span></span></th>
<th align="left"><span data-ttu-id="c1a2d-149">Office 2010</span><span class="sxs-lookup"><span data-stu-id="c1a2d-149">Office 2010</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c1a2d-150">Plug-in Lync Meeting join pour Firefox et chrome</span><span class="sxs-lookup"><span data-stu-id="c1a2d-150">Lync meeting Join Plug-in for Firefox and Chrome</span></span></p></td>
<td align="left"><p><span data-ttu-id="c1a2d-151">Les utilisateurs peuvent participer à des réunions Lync depuis Firefox et chrome</span><span class="sxs-lookup"><span data-stu-id="c1a2d-151">User can join Lync meetings from Firefox and Chrome</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c1a2d-152">Envoyés vers le pilote d’impression OneNote</span><span class="sxs-lookup"><span data-stu-id="c1a2d-152">Sent to OneNote Print Driver</span></span></p></td>
<td align="left"><p><span data-ttu-id="c1a2d-153">L’utilisateur peut imprimer dans OneNote</span><span class="sxs-lookup"><span data-stu-id="c1a2d-153">User can print to OneNote</span></span></p></td>
<td align="left"><p><span data-ttu-id="c1a2d-154">Oui</span><span class="sxs-lookup"><span data-stu-id="c1a2d-154">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c1a2d-155">Notes liées OneNote</span><span class="sxs-lookup"><span data-stu-id="c1a2d-155">OneNote Linked Notes</span></span></p></td>
<td align="left"><p><span data-ttu-id="c1a2d-156">Notes liées OneNote</span><span class="sxs-lookup"><span data-stu-id="c1a2d-156">OneNote Linked Notes</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c1a2d-157">Envoyer vers le complément OneNote sur le Web Explorer</span><span class="sxs-lookup"><span data-stu-id="c1a2d-157">Send to OneNote Internet Explorer Add-In</span></span></p></td>
<td align="left"><p><span data-ttu-id="c1a2d-158">L’utilisateur peut envoyer à OneNote à partir d’Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="c1a2d-158">User can send to OneNote from IE</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c1a2d-159">Exception de pare-feu pour Lync et Outlook</span><span class="sxs-lookup"><span data-stu-id="c1a2d-159">Firewall Exception for Lync and Outlook</span></span></p></td>
<td align="left"><p><span data-ttu-id="c1a2d-160">Exception de pare-feu pour Lync et Outlook</span><span class="sxs-lookup"><span data-stu-id="c1a2d-160">Firewall Exception for Lync and Outlook</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c1a2d-161">Client MAPI</span><span class="sxs-lookup"><span data-stu-id="c1a2d-161">MAPI Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="c1a2d-162">Les applications et les compléments natifs peuvent interagir avec les applications virtuelles Outlook via MAPI</span><span class="sxs-lookup"><span data-stu-id="c1a2d-162">Native apps and add-ins can interact with virtual Outlook through MAPI</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c1a2d-163">Plug-in SharePoint pour Firefox</span><span class="sxs-lookup"><span data-stu-id="c1a2d-163">SharePoint Plugin for Firefox</span></span></p></td>
<td align="left"><p><span data-ttu-id="c1a2d-164">Les utilisateurs peuvent utiliser les fonctionnalités SharePoint dans Firefox</span><span class="sxs-lookup"><span data-stu-id="c1a2d-164">User can use SharePoint features in Firefox</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c1a2d-165">Applet panneau de configuration de la messagerie</span><span class="sxs-lookup"><span data-stu-id="c1a2d-165">Mail Control Panel Applet</span></span></p></td>
<td align="left"><p><span data-ttu-id="c1a2d-166">L’utilisateur obtient l’applet panneau de configuration de la messagerie dans Outlook</span><span class="sxs-lookup"><span data-stu-id="c1a2d-166">User gets the mail control panel applet in Outlook</span></span></p></td>
<td align="left"><p><span data-ttu-id="c1a2d-167">Oui</span><span class="sxs-lookup"><span data-stu-id="c1a2d-167">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c1a2d-168">Assemblys d’interopérabilité principaux</span><span class="sxs-lookup"><span data-stu-id="c1a2d-168">Primary Interop Assemblies</span></span></p></td>
<td align="left"><p><span data-ttu-id="c1a2d-169">Compléments gérés par le support</span><span class="sxs-lookup"><span data-stu-id="c1a2d-169">Support managed add-ins</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c1a2d-170">Gestionnaire de cache de documents Office</span><span class="sxs-lookup"><span data-stu-id="c1a2d-170">Office Document Cache Handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="c1a2d-171">Autorise le cache de documents pour les applications Office</span><span class="sxs-lookup"><span data-stu-id="c1a2d-171">Allows Document Cache for Office applications</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c1a2d-172">Gestionnaire de recherche du protocole Outlook</span><span class="sxs-lookup"><span data-stu-id="c1a2d-172">Outlook Protocol Search handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="c1a2d-173">L’utilisateur peut effectuer une recherche dans Outlook</span><span class="sxs-lookup"><span data-stu-id="c1a2d-173">User can search in outlook</span></span></p></td>
<td align="left"><p><span data-ttu-id="c1a2d-174">Oui</span><span class="sxs-lookup"><span data-stu-id="c1a2d-174">Yes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c1a2d-175">Contrôles Active X:</span><span class="sxs-lookup"><span data-stu-id="c1a2d-175">Active X Controls:</span></span></p></td>
<td align="left"><p><span data-ttu-id="c1a2d-176">Pour plus d’informations sur les contrôles ActiveX, voir informations de référence sur les <a href="https://go.microsoft.com/fwlink/p/?LinkId=331361" data-raw-source="[ActiveX Control API Reference](https://go.microsoft.com/fwlink/p/?LinkId=331361)"> API de contrôles ActiveX </a> .</span><span class="sxs-lookup"><span data-stu-id="c1a2d-176">For more information on ActiveX controls, refer to <a href="https://go.microsoft.com/fwlink/p/?LinkId=331361" data-raw-source="[ActiveX Control API Reference](https://go.microsoft.com/fwlink/p/?LinkId=331361)">ActiveX Control API Reference</a>.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="c1a2d-177">Groove. SiteClient</span><span class="sxs-lookup"><span data-stu-id="c1a2d-177">Groove.SiteClient</span></span></p></td>
<td align="left"><p><span data-ttu-id="c1a2d-178">Contrôle Active X</span><span class="sxs-lookup"><span data-stu-id="c1a2d-178">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="c1a2d-179">PortalConnect.PersonalSite</span><span class="sxs-lookup"><span data-stu-id="c1a2d-179">PortalConnect.PersonalSite</span></span></p></td>
<td align="left"><p><span data-ttu-id="c1a2d-180">Contrôle Active X</span><span class="sxs-lookup"><span data-stu-id="c1a2d-180">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="c1a2d-181">SharePoint. openDocuments</span><span class="sxs-lookup"><span data-stu-id="c1a2d-181">SharePoint.openDocuments</span></span></p></td>
<td align="left"><p><span data-ttu-id="c1a2d-182">Contrôle Active X</span><span class="sxs-lookup"><span data-stu-id="c1a2d-182">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="c1a2d-183">SharePoint. ExportDatabase</span><span class="sxs-lookup"><span data-stu-id="c1a2d-183">SharePoint.ExportDatabase</span></span></p></td>
<td align="left"><p><span data-ttu-id="c1a2d-184">Contrôle Active X</span><span class="sxs-lookup"><span data-stu-id="c1a2d-184">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="c1a2d-185">SharePoint. SpreadSheetLauncher</span><span class="sxs-lookup"><span data-stu-id="c1a2d-185">SharePoint.SpreadSheetLauncher</span></span></p></td>
<td align="left"><p><span data-ttu-id="c1a2d-186">Contrôle Active X</span><span class="sxs-lookup"><span data-stu-id="c1a2d-186">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="c1a2d-187">SharePoint. StssyncHander</span><span class="sxs-lookup"><span data-stu-id="c1a2d-187">SharePoint.StssyncHander</span></span></p></td>
<td align="left"><p><span data-ttu-id="c1a2d-188">Contrôle Active X</span><span class="sxs-lookup"><span data-stu-id="c1a2d-188">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="c1a2d-189">SharePoint. DragUploadCtl</span><span class="sxs-lookup"><span data-stu-id="c1a2d-189">SharePoint.DragUploadCtl</span></span></p></td>
<td align="left"><p><span data-ttu-id="c1a2d-190">Contrôle Active X</span><span class="sxs-lookup"><span data-stu-id="c1a2d-190">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="c1a2d-191">SharePoint. DragDownloadCtl</span><span class="sxs-lookup"><span data-stu-id="c1a2d-191">SharePoint.DragDownloadCtl</span></span></p></td>
<td align="left"><p><span data-ttu-id="c1a2d-192">Contrôle Active X</span><span class="sxs-lookup"><span data-stu-id="c1a2d-192">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="c1a2d-193">SharePoint. OpenXMLDocuments</span><span class="sxs-lookup"><span data-stu-id="c1a2d-193">Sharpoint.OpenXMLDocuments</span></span></p></td>
<td align="left"><p><span data-ttu-id="c1a2d-194">Contrôle Active X</span><span class="sxs-lookup"><span data-stu-id="c1a2d-194">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="c1a2d-195">SharePoint. ClipboardCtl</span><span class="sxs-lookup"><span data-stu-id="c1a2d-195">Sharepoint.ClipboardCtl</span></span></p></td>
<td align="left"><p><span data-ttu-id="c1a2d-196">Contrôle Active X</span><span class="sxs-lookup"><span data-stu-id="c1a2d-196">Active X control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="c1a2d-197">WinProj. Activator</span><span class="sxs-lookup"><span data-stu-id="c1a2d-197">WinProj.Activator</span></span></p></td>
<td align="left"><p><span data-ttu-id="c1a2d-198">Contrôle Active X</span><span class="sxs-lookup"><span data-stu-id="c1a2d-198">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="c1a2d-199">Nom. NameCtrl</span><span class="sxs-lookup"><span data-stu-id="c1a2d-199">Name.NameCtrl</span></span></p></td>
<td align="left"><p><span data-ttu-id="c1a2d-200">Contrôle Active X</span><span class="sxs-lookup"><span data-stu-id="c1a2d-200">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="c1a2d-201">STSUPld.CopyCtl</span><span class="sxs-lookup"><span data-stu-id="c1a2d-201">STSUPld.CopyCtl</span></span></p></td>
<td align="left"><p><span data-ttu-id="c1a2d-202">Contrôle Active X</span><span class="sxs-lookup"><span data-stu-id="c1a2d-202">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="c1a2d-203">CommunicatorMeetingJoinAx.JoinManager</span><span class="sxs-lookup"><span data-stu-id="c1a2d-203">CommunicatorMeetingJoinAx.JoinManager</span></span></p></td>
<td align="left"><p><span data-ttu-id="c1a2d-204">Contrôle Active X</span><span class="sxs-lookup"><span data-stu-id="c1a2d-204">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="c1a2d-205">LISTNET. Listnet</span><span class="sxs-lookup"><span data-stu-id="c1a2d-205">LISTNET.Listnet</span></span></p></td>
<td align="left"><p><span data-ttu-id="c1a2d-206">Contrôle Active X</span><span class="sxs-lookup"><span data-stu-id="c1a2d-206">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="c1a2d-207">Programme d’assistance du navigateur OneDrive Pro</span><span class="sxs-lookup"><span data-stu-id="c1a2d-207">OneDrive Pro Browser Helper</span></span></p></td>
<td align="left"><p><span data-ttu-id="c1a2d-208">Contrôle ActiveX</span><span class="sxs-lookup"><span data-stu-id="c1a2d-208">Active X Control]</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c1a2d-209">Superpositions d’icônes OneDrive Pro</span><span class="sxs-lookup"><span data-stu-id="c1a2d-209">OneDrive Pro Icon Overlays</span></span></p></td>
<td align="left"><p><span data-ttu-id="c1a2d-210">Icônes de l’interface utilisateur de l’Explorateur Windows lorsque les utilisateurs regardent les dossiers OneDrive Pro</span><span class="sxs-lookup"><span data-stu-id="c1a2d-210">Windows explorer shell icon overlays when users look at folders OneDrive Pro folders</span></span></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="c1a2d-211">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="c1a2d-211">Additional resources</span></span>


**<span data-ttu-id="c1a2d-212">Office 2013 App-V-packages de ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="c1a2d-212">Office 2013 App-V Packages Additional Resources</span></span>**

[<span data-ttu-id="c1a2d-213">Scénarios pris en charge pour le déploiement de Microsoft Office en tant que package App-V séquencé</span><span class="sxs-lookup"><span data-stu-id="c1a2d-213">Supported scenarios for deploying Microsoft Office as a sequenced App-V Package</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330680)

**<span data-ttu-id="c1a2d-214">Packages App-V d’Office 2010</span><span class="sxs-lookup"><span data-stu-id="c1a2d-214">Office 2010 App-V Packages</span></span>**

[<span data-ttu-id="c1a2d-215">Kit de séquençage Microsoft Office 2010 pour Microsoft Application Virtualization 5,0</span><span class="sxs-lookup"><span data-stu-id="c1a2d-215">Microsoft Office 2010 Sequencing Kit for Microsoft Application Virtualization 5.0</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330681)

[<span data-ttu-id="c1a2d-216">Problèmes connus lors de la création ou de l’utilisation d’un package App-V 5,0 Office 2010</span><span class="sxs-lookup"><span data-stu-id="c1a2d-216">Known issues when you create or use an App-V 5.0 Office 2010 package</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330682)

[<span data-ttu-id="c1a2d-217">Comment séquencer Microsoft Office 2010 dans Microsoft Application Virtualization 5,0</span><span class="sxs-lookup"><span data-stu-id="c1a2d-217">How to sequence Microsoft Office 2010 in Microsoft Application Virtualization 5.0</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330676)

**<span data-ttu-id="c1a2d-218">Groupes de connexion</span><span class="sxs-lookup"><span data-stu-id="c1a2d-218">Connection Groups</span></span>**

[<span data-ttu-id="c1a2d-219">Déploiement de groupes de connexion dans Microsoft App-V v5</span><span class="sxs-lookup"><span data-stu-id="c1a2d-219">Deploying Connection Groups in Microsoft App-V v5</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330683)

[<span data-ttu-id="c1a2d-220">Gestion des groupes de connexion</span><span class="sxs-lookup"><span data-stu-id="c1a2d-220">Managing Connection Groups</span></span>](managing-connection-groups51.md)

**<span data-ttu-id="c1a2d-221">Configuration dynamique</span><span class="sxs-lookup"><span data-stu-id="c1a2d-221">Dynamic Configuration</span></span>**

[<span data-ttu-id="c1a2d-222">À propos de la configuration dynamique d'App-V5.1</span><span class="sxs-lookup"><span data-stu-id="c1a2d-222">About App-V 5.1 Dynamic Configuration</span></span>](about-app-v-51-dynamic-configuration.md)






 

 





