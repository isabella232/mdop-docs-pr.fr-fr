---
title: Installation de Sequencer
description: Installation de Sequencer
author: dansimp
ms.assetid: a122caf0-f408-458c-b119-dc84123c1d58
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a8542abfecd7f1d543228ab1a86a59b9ee918947
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805364"
---
# <span data-ttu-id="9ce76-103">Installation de Sequencer</span><span class="sxs-lookup"><span data-stu-id="9ce76-103">How to Install the Sequencer</span></span>


<span data-ttu-id="9ce76-104">Utilisez la procédure suivante pour installer le Sequencer Microsoft Application Virtualization (App-V) 5,0.</span><span class="sxs-lookup"><span data-stu-id="9ce76-104">Use the following procedure to install the Microsoft Application Virtualization (App-V) 5.0 sequencer.</span></span> <span data-ttu-id="9ce76-105">L’ordinateur qui exécute le Sequencer ne doit pas exécuter de version du client App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="9ce76-105">The computer that will run the sequencer must not be running any version of the App-V 5.0 client.</span></span>

<span data-ttu-id="9ce76-106">La mise à niveau d’une installation antérieure du Sequencer App-V n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="9ce76-106">Upgrading a previous installation of the App-V sequencer is not supported.</span></span>

<span data-ttu-id="9ce76-107">**Important**  Pour obtenir la liste complète de la configuration requise pour le Sequencer, voir sections de Sequencer de l' [application-v 5,0 requise](app-v-50-prerequisites.md) et [configurations de app-v 5,0 prises en charge](app-v-50-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="9ce76-107">**Important** For a full list of the sequencer requirements see sequencer sections of [App-V 5.0 Prerequisites](app-v-50-prerequisites.md) and [App-V 5.0 Supported Configurations](app-v-50-supported-configurations.md).</span></span>

 

<span data-ttu-id="9ce76-108">Vous pouvez également utiliser la ligne de commande pour installer le Sequencer App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="9ce76-108">You can also use the command line to install the App-V 5.0 sequencer.</span></span> <span data-ttu-id="9ce76-109">La liste suivante présente des informations sur les options d’installation du Sequencer à l’aide de la ligne de commande et **appv\_sequencer\_setup.exe**:</span><span class="sxs-lookup"><span data-stu-id="9ce76-109">The following list displays information about options for installing the sequencer using the command line and **appv\_sequencer\_setup.exe**:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9ce76-110">Commande</span><span class="sxs-lookup"><span data-stu-id="9ce76-110">Command</span></span></th>
<th align="left"><span data-ttu-id="9ce76-111">Description</span><span class="sxs-lookup"><span data-stu-id="9ce76-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9ce76-112">/INSTALLDIR</span><span class="sxs-lookup"><span data-stu-id="9ce76-112">/INSTALLDIR</span></span></p></td>
<td align="left"><p><span data-ttu-id="9ce76-113">Spécifie le répertoire d’installation.</span><span class="sxs-lookup"><span data-stu-id="9ce76-113">Specifies the installation directory.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9ce76-114">/CEIPOPTIN</span><span class="sxs-lookup"><span data-stu-id="9ce76-114">/CEIPOPTIN</span></span></p></td>
<td align="left"><p><span data-ttu-id="9ce76-115">Permet de participer au programme d’amélioration du produit de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="9ce76-115">Enables participation in the Microsoft Customer Experience Improvement Program.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9ce76-116">/Log</span><span class="sxs-lookup"><span data-stu-id="9ce76-116">/Log</span></span></p></td>
<td align="left"><p><span data-ttu-id="9ce76-117">Spécifie l’emplacement dans lequel le journal d’installation sera enregistré, l’emplacement par défaut est <strong> % temp% </strong> .</span><span class="sxs-lookup"><span data-stu-id="9ce76-117">Specifies where the installation log will be saved, the default location is <strong>%Temp%</strong>.</span></span> <span data-ttu-id="9ce76-118">Par exemple, <strong> C:\ Consigne </strong> . log.</span><span class="sxs-lookup"><span data-stu-id="9ce76-118">For example, <strong>C:\ Logs \ log.log</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9ce76-119">établit</span><span class="sxs-lookup"><span data-stu-id="9ce76-119">/q</span></span></p></td>
<td align="left"><p><span data-ttu-id="9ce76-120">Spécifie une installation silencieuse ou silencieuse.</span><span class="sxs-lookup"><span data-stu-id="9ce76-120">Specifies a quiet or silent installation.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9ce76-121">/Uninstall</span><span class="sxs-lookup"><span data-stu-id="9ce76-121">/Uninstall</span></span></p></td>
<td align="left"><p><span data-ttu-id="9ce76-122">Spécifie la suppression du Sequencer.</span><span class="sxs-lookup"><span data-stu-id="9ce76-122">Specifies the removal of the sequencer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9ce76-123">/ACCEPTEULA</span><span class="sxs-lookup"><span data-stu-id="9ce76-123">/ACCEPTEULA</span></span></p></td>
<td align="left"><p><span data-ttu-id="9ce76-124">Accepter le contrat de licence.</span><span class="sxs-lookup"><span data-stu-id="9ce76-124">Accepts the license agreement.</span></span> <span data-ttu-id="9ce76-125">Ce type de fichier est requis pour une installation sans assistance.</span><span class="sxs-lookup"><span data-stu-id="9ce76-125">This is required for an unattended installation.</span></span> <span data-ttu-id="9ce76-126">Exemple d’utilisation: <strong> /AcceptEULA </strong> ou <strong> /ACCEPTEULA = 1 </strong> .</span><span class="sxs-lookup"><span data-stu-id="9ce76-126">Example usage: <strong>/ACCEPTEULA</strong> or <strong>/ACCEPTEULA=1</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9ce76-127">/LAYOUT</span><span class="sxs-lookup"><span data-stu-id="9ce76-127">/LAYOUT</span></span></p></td>
<td align="left"><p><span data-ttu-id="9ce76-128">Spécifie l’action de disposition associée.</span><span class="sxs-lookup"><span data-stu-id="9ce76-128">Specifies the associated layout action.</span></span> <span data-ttu-id="9ce76-129">Il extrait également les fichiers Windows Installer (. msi) et script dans un dossier sans installer App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="9ce76-129">It also extracts the Windows Installer (.msi) and script files to a folder without installing App-V 5.0.</span></span> <span data-ttu-id="9ce76-130">Aucune valeur n’est attendue.</span><span class="sxs-lookup"><span data-stu-id="9ce76-130">No value is expected.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9ce76-131">/LAYOUTDIR</span><span class="sxs-lookup"><span data-stu-id="9ce76-131">/LAYOUTDIR</span></span></p></td>
<td align="left"><p><span data-ttu-id="9ce76-132">Spécifie le répertoire de disposition.</span><span class="sxs-lookup"><span data-stu-id="9ce76-132">Specifies the layout directory.</span></span> <span data-ttu-id="9ce76-133">Nécessite une valeur de chaîne.</span><span class="sxs-lookup"><span data-stu-id="9ce76-133">Requires a string value.</span></span> <span data-ttu-id="9ce76-134">Exemple d’utilisation: <strong> /LAYOUTDIR = «client de virtualisation C:\Application» </strong> .</span><span class="sxs-lookup"><span data-stu-id="9ce76-134">Example usage: <strong>/LAYOUTDIR=”C:\Application Virtualization Client”</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9ce76-135">/?</span><span class="sxs-lookup"><span data-stu-id="9ce76-135">/?</span></span> <span data-ttu-id="9ce76-136">Ou/h ou/Help</span><span class="sxs-lookup"><span data-stu-id="9ce76-136">Or /h or /help</span></span></p></td>
<td align="left"><p><span data-ttu-id="9ce76-137">Affiche l’aide associée.</span><span class="sxs-lookup"><span data-stu-id="9ce76-137">Displays associated help.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="9ce76-138">Pour installer le Sequencer App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="9ce76-138">To install the App-V 5.0 sequencer</span></span>**

1.  <span data-ttu-id="9ce76-139">Copiez les fichiers d’installation de Sequencer App-V 5,0 sur l’ordinateur sur lequel il est installé.</span><span class="sxs-lookup"><span data-stu-id="9ce76-139">Copy the App-V 5.0 sequencer installation files to the computer on which it will be installed.</span></span> <span data-ttu-id="9ce76-140">Double-cliquez sur **appv\_sequencer\_setup.exe** puis cliquez sur **installer**.</span><span class="sxs-lookup"><span data-stu-id="9ce76-140">Double-click **appv\_sequencer\_setup.exe** and then click **Install**.</span></span>

2.  <span data-ttu-id="9ce76-141">Sur la page termes du contrat de **licence logiciel** , prenez connaissance des termes du contrat de licence.</span><span class="sxs-lookup"><span data-stu-id="9ce76-141">On the **Software License Terms** page, you should review the license terms.</span></span> <span data-ttu-id="9ce76-142">Pour accepter les termes du contrat de licence **, sélectionnez J’accepte les termes du contrat de licence.**</span><span class="sxs-lookup"><span data-stu-id="9ce76-142">To accept the license terms select **I accept the license terms.**</span></span> <span data-ttu-id="9ce76-143">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="9ce76-143">Click **Next**.</span></span>

3.  <span data-ttu-id="9ce76-144">Sur la page **utiliser Microsoft Update pour garantir la sécurité et** la mise à jour de votre ordinateur, activez la **case à cocher utiliser Microsoft Update lorsque je recherche des mises à jour (recommandé).**</span><span class="sxs-lookup"><span data-stu-id="9ce76-144">On the **Use Microsoft Update to help keep your computer secure and up-to-date** page, to enable Microsoft updates select **Use Microsoft Update when I check for updates (recommended).**</span></span> <span data-ttu-id="9ce76-145">Pour désactiver l’exécution des mises à jour de Microsoft, sélectionnez **je ne veux pas utiliser Microsoft Update**.</span><span class="sxs-lookup"><span data-stu-id="9ce76-145">To disable Microsoft updates from running select **I don’t want to use Microsoft Update**.</span></span> <span data-ttu-id="9ce76-146">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="9ce76-146">Click **Next**.</span></span>

4.  <span data-ttu-id="9ce76-147">Sur la page du **programme d’amélioration** du produit, pour participer au programme, sélectionnez **participer au programme d’amélioration du**produit.</span><span class="sxs-lookup"><span data-stu-id="9ce76-147">On the **Customer Experience Improvement Program** page, to participate in the program select **Join the Customer Experience Improvement Program**.</span></span> <span data-ttu-id="9ce76-148">Cela permettra d’obtenir des informations sur l’utilisation de l’application-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="9ce76-148">This will allow information to be collected about how you are using App-V 5.0.</span></span> <span data-ttu-id="9ce76-149">Si vous ne voulez pas participer au programme, sélectionnez **je ne veux pas**participer au programme pour le moment.</span><span class="sxs-lookup"><span data-stu-id="9ce76-149">If you don’t want to participate in the program select **I don’t want to join the program at this time**.</span></span> <span data-ttu-id="9ce76-150">Cliquez sur **Installer**.</span><span class="sxs-lookup"><span data-stu-id="9ce76-150">Click **Install**.</span></span>

5.  <span data-ttu-id="9ce76-151">Pour ouvrir le Sequencer, cliquez sur **Démarrer** , puis sur **Microsoft Application Virtualization Sequencer**.</span><span class="sxs-lookup"><span data-stu-id="9ce76-151">To open the sequencer, click **Start** and then click **Microsoft Application Virtualization Sequencer**.</span></span>

**<span data-ttu-id="9ce76-152">Pour résoudre les problèmes liés à l’installation de Sequencer App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="9ce76-152">To troubleshoot the App-V 5.0 sequencer installation</span></span>**

-   <span data-ttu-id="9ce76-153">Pour plus d’informations sur l’installation de Sequencer, vous pouvez afficher le journal des erreurs dans le dossier **% temp%** .</span><span class="sxs-lookup"><span data-stu-id="9ce76-153">For more information regarding the sequencer installation, you can view the error log in the **%temp%** folder.</span></span> <span data-ttu-id="9ce76-154">Pour passer en revue les fichiers journaux, cliquez sur **Démarrer**, tapez **% temp%**, puis recherchez le **Journal appv\_**.</span><span class="sxs-lookup"><span data-stu-id="9ce76-154">To review the log files, click **Start**, type **%temp%**, and then look for the **appv\_ log**.</span></span>

    <span data-ttu-id="9ce76-155">Vous **avez une suggestion pour App-V**?</span><span class="sxs-lookup"><span data-stu-id="9ce76-155">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="9ce76-156">Ajoutez ou Votez en fonction [de suggestions.](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)</span><span class="sxs-lookup"><span data-stu-id="9ce76-156">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="9ce76-157">Vous avez un problème lié à l’application-V?</span><span class="sxs-lookup"><span data-stu-id="9ce76-157">Got an App-V issue?</span></span>** <span data-ttu-id="9ce76-158">Utilisez le [Forum TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="9ce76-158">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="9ce76-159">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9ce76-159">Related topics</span></span>


[<span data-ttu-id="9ce76-160">Envisager de déployer App-V</span><span class="sxs-lookup"><span data-stu-id="9ce76-160">Planning to Deploy App-V</span></span>](planning-to-deploy-app-v.md)

 

 





