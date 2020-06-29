---
title: Notes de publication pour DaRT7.0
description: Notes de publication pour DaRT7.0
author: dansimp
ms.assetid: fad227d0-5c22-4efd-9187-0e5922f7250b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 5114acfe5a46a2c78f722a2bb6394c0dbef55dd4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809551"
---
# <span data-ttu-id="8a31c-103">Notes de publication pour DaRT7.0</span><span class="sxs-lookup"><span data-stu-id="8a31c-103">Release Notes for DaRT 7.0</span></span>


**<span data-ttu-id="8a31c-104">Pour effectuer une recherche dans ces notes de publication, appuyez sur CTRL + F.</span><span class="sxs-lookup"><span data-stu-id="8a31c-104">To search these release notes, press CTRL+F.</span></span>**

<span data-ttu-id="8a31c-105">Lisez attentivement ces notes de publication avant de procéder à l’installation de Microsoft Diagnostics and Recovery Tools (DaRT) 7.</span><span class="sxs-lookup"><span data-stu-id="8a31c-105">Read these release notes thoroughly before you install Microsoft Diagnostics and Recovery Toolset (DaRT)7.</span></span>

## <span data-ttu-id="8a31c-106">À propos de Microsoft Diagnostics and Recovery Tools Tools 7,0</span><span class="sxs-lookup"><span data-stu-id="8a31c-106">About Microsoft Diagnostics and Recovery Toolset 7.0</span></span>


<span data-ttu-id="8a31c-107">Ces notes de publication contiennent des informations requises pour l’installation d’DaRT7 et contiennent des informations qui ne sont pas disponibles dans la documentation du produit.</span><span class="sxs-lookup"><span data-stu-id="8a31c-107">These release notes contain information that is required to successfully install DaRT7 and contain information that is not available in the product documentation.</span></span> <span data-ttu-id="8a31c-108">S’il existe une différence entre ces notes de publication et d’autres documents de la plateforme DaRT, la dernière modification doit être considérée comme faisant autorité.</span><span class="sxs-lookup"><span data-stu-id="8a31c-108">If there is a difference between these release notes and other DaRT platform documentation, the latest change should be considered authoritative.</span></span> <span data-ttu-id="8a31c-109">Ces notes de publication remplacent le contenu fourni avec ce produit.</span><span class="sxs-lookup"><span data-stu-id="8a31c-109">These release notes supersede the content included with this product.</span></span>

## <span data-ttu-id="8a31c-110">À propos de la documentation relative aux produits</span><span class="sxs-lookup"><span data-stu-id="8a31c-110">About the Product Documentation</span></span>


<span data-ttu-id="8a31c-111">La documentation pour Microsoft Diagnostics and Recovery Tools (DaRT) 7 est distribuée avec le produit et sur le site de connexion.</span><span class="sxs-lookup"><span data-stu-id="8a31c-111">Documentation for Microsoft Diagnostics and Recovery Toolset (DaRT)7 is distributed with the product and on the Connect site.</span></span>

<span data-ttu-id="8a31c-112">Pour obtenir une aide détaillée sur l’utilisation des outils dans DaRT7, consultez le fichier d’aide disponible dans le menu des **outils de diagnostics et de récupération** .</span><span class="sxs-lookup"><span data-stu-id="8a31c-112">For detailed help about how to use the tools in DaRT7, see the Help file available on the **Diagnostics and Recovery Toolset** menu.</span></span>

## <span data-ttu-id="8a31c-113">Envoi de commentaires</span><span class="sxs-lookup"><span data-stu-id="8a31c-113">Providing feedback</span></span>


<span data-ttu-id="8a31c-114">Vos commentaires vous intéressent sur DaRT7.</span><span class="sxs-lookup"><span data-stu-id="8a31c-114">We are interested in your feedback on DaRT7.</span></span> <span data-ttu-id="8a31c-115">Vous pouvez envoyer vos commentaires à dart7feedback@microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="8a31c-115">You can send your feedback to dart7feedback@microsoft.com.</span></span> <span data-ttu-id="8a31c-116">Cette adresse de messagerie n’est pas un canal de support, mais vos commentaires nous aideront à planifier des changements ultérieurs pour ces outils afin de les rendre plus utiles.</span><span class="sxs-lookup"><span data-stu-id="8a31c-116">This email address is not a support channel, but your feedback will help us to plan future changes for these tools to make them more useful to you in the future.</span></span>

## <span data-ttu-id="8a31c-117">Se protéger contre les failles de sécurité et les virus</span><span class="sxs-lookup"><span data-stu-id="8a31c-117">Protect Against Security Vulnerabilities and Viruses</span></span>


<span data-ttu-id="8a31c-118">Pour vous aider à vous protéger contre les failles de sécurité, nous vous recommandons d’installer les mises à jour de sécurité disponibles pour tout nouveau logiciel installé.</span><span class="sxs-lookup"><span data-stu-id="8a31c-118">To help protect against security vulnerabilities and viruses, we recommend that you install the latest available security updates for any new software being installed.</span></span> <span data-ttu-id="8a31c-119">Pour plus d’informations, reportez-vous à la rubrique [sécurité Microsoft](https://go.microsoft.com/fwlink/?LinkId=3482) ( https://go.microsoft.com/fwlink/?LinkId=3482) .</span><span class="sxs-lookup"><span data-stu-id="8a31c-119">For more information, see [Microsoft Security](https://go.microsoft.com/fwlink/?LinkId=3482) (https://go.microsoft.com/fwlink/?LinkId=3482).</span></span>

## <span data-ttu-id="8a31c-120">Problèmes connus avec le 7,0 DaRT</span><span class="sxs-lookup"><span data-stu-id="8a31c-120">Known Issues with DaRT 7.0</span></span>


### <span data-ttu-id="8a31c-121">L’analyse SFC ne peut pas démarrer si le nettoyeur système autonome est ouvert</span><span class="sxs-lookup"><span data-stu-id="8a31c-121">SFC Scan cannot start if Standalone System Sweeper is open</span></span>

<span data-ttu-id="8a31c-122">Si le nettoyeur système autonome est en cours d’exécution, l’analyse SFC ne peut pas démarrer ou s’exécuter en raison d’un conflit de ressources entre les deux outils.</span><span class="sxs-lookup"><span data-stu-id="8a31c-122">If the Standalone System Sweeper is running, SFC Scan cannot start or run because of a resource conflict between the two tools.</span></span>

<span data-ttu-id="8a31c-123">**Solution de contournement:** Fermez le nettoyeur système autonome avant d’essayer d’ouvrir ou d’exécuter l’outil d’analyse SFC.</span><span class="sxs-lookup"><span data-stu-id="8a31c-123">**Workaround:** Close the Standalone System Sweeper before you try to open or run the SFC Scan tool.</span></span>

### <span data-ttu-id="8a31c-124">Les caractères Unicode risquent de ne pas s’afficher dans les noms de fichiers</span><span class="sxs-lookup"><span data-stu-id="8a31c-124">Unicode characters may not be displayed in file names</span></span>

<span data-ttu-id="8a31c-125">Si vous supprimez un fichier qui comporte des caractères Unicode dans son nom de fichier et que vous essayez de restaurer le fichier à l’aide de l’outil de restauration de fichiers, le fichier est introuvable.</span><span class="sxs-lookup"><span data-stu-id="8a31c-125">If you delete a file that has Unicode characters in its file name and try to restore the file by using the File Restore tool, the file is not found.</span></span> <span data-ttu-id="8a31c-126">Cela se produit uniquement lorsque vous utilisez des caractères d’une langue autre que celle du DVD Windows utilisé pour créer l’image de récupération.</span><span class="sxs-lookup"><span data-stu-id="8a31c-126">This only occurs when you use characters from a language other than the language of the Windows DVD that was used to create the recovery image.</span></span>

<span data-ttu-id="8a31c-127">**Solution de contournement:** Assurez-vous que la langue utilisée par DaRT correspond à la langue utilisée par le système d’exploitation à partir duquel il tente de restaurer des fichiers.</span><span class="sxs-lookup"><span data-stu-id="8a31c-127">**Workaround:** Make sure that the language that is used by DaRT matches the language that is used by the operating system from which it is trying to restore files.</span></span>

### <span data-ttu-id="8a31c-128">L’installation de la ligne de commande DaRT risque de ne pas fonctionner en silence</span><span class="sxs-lookup"><span data-stu-id="8a31c-128">DaRT command-line installation may fail silently</span></span>

<span data-ttu-id="8a31c-129">L’installation de l’outil de ligne de commande DaRT échoue en silence s’il est exécuté en mode quiet, sauf si elle est exécutée à l’aide d’autorisations d’administrateur élevés.</span><span class="sxs-lookup"><span data-stu-id="8a31c-129">DaRT command-line installation fails silently if run with the quiet mode option unless it is run by using elevated administrator permissions.</span></span>

<span data-ttu-id="8a31c-130">**Solution de contournement:** Exécutez l’installation de la ligne de commande à l’aide d’autorisations d’administrateur élevées.</span><span class="sxs-lookup"><span data-stu-id="8a31c-130">**Workaround:** Run the command-line installation by using elevated administrator permissions.</span></span> <span data-ttu-id="8a31c-131">L’installation de DaRT prend en charge les options de Windows Installer standard pour l’installation de lignes de commande.</span><span class="sxs-lookup"><span data-stu-id="8a31c-131">DaRT installation supports the typical Windows Installer options for command-line installation.</span></span> <span data-ttu-id="8a31c-132">Pour plus d’informations sur les différents commutateurs disponibles, voir [options de ligne de commande](https://go.microsoft.com/fwlink/?LinkId=160689) pour Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="8a31c-132">Please see [Command-Line Options](https://go.microsoft.com/fwlink/?LinkId=160689) for Windows Installer for more information about the several available switches.</span></span>

### <span data-ttu-id="8a31c-133">La recherche de fichiers ne peut pas déplacer un dossier vers un autre volume</span><span class="sxs-lookup"><span data-stu-id="8a31c-133">File Search cannot move a folder to a different volume</span></span>

<span data-ttu-id="8a31c-134">Le déplacement de dossiers entre des volumes n’est pas pris en charge par l’application de recherche de fichiers.</span><span class="sxs-lookup"><span data-stu-id="8a31c-134">Moving folders between volumes is not supported by the File Search application.</span></span> <span data-ttu-id="8a31c-135">Si vous tentez de déplacer un dossier vers un autre volume dans le cadre de la recherche de fichier, le message d’erreur suivant est retourné: «une erreur s’est produite lors de l’écriture du \* &lt; nom &gt; \*de fichier.</span><span class="sxs-lookup"><span data-stu-id="8a31c-135">If you try to move a folder to a different volume in File Search, the following error is returned: "An error occurred while writing the file *&lt;filename&gt;*.</span></span> <span data-ttu-id="8a31c-136">Assurez-vous que le lecteur dispose de suffisamment d’espace et que le chemin de destination est accessible.</span><span class="sxs-lookup"><span data-stu-id="8a31c-136">Make sure that the drive has sufficient space and the destination path is accessible."</span></span>

<span data-ttu-id="8a31c-137">**Solution de contournement:** Utilisez l’Explorateur pour déplacer un dossier vers un autre volume.</span><span class="sxs-lookup"><span data-stu-id="8a31c-137">**Workaround:** Use the Explorer to move a folder to a different volume.</span></span>

### <span data-ttu-id="8a31c-138">Certaines données risquent de ne pas être disponibles sur les ordinateurs sur lesquels les lettres de lecteur sont remappées</span><span class="sxs-lookup"><span data-stu-id="8a31c-138">Some data may not be available on computers where the drive letters are remapped</span></span>

<span data-ttu-id="8a31c-139">Ce problème peut se produire sur des ordinateurs compatibles avec BitLocker et sur des ordinateurs à démarrage multiple.</span><span class="sxs-lookup"><span data-stu-id="8a31c-139">This problem can occur on BitLocker-enabled computers and multiboot computers.</span></span> <span data-ttu-id="8a31c-140">Ce problème se produit car certaines informations du Registre hors connexion ont des lettres de lecteur codées en dur, et DaRT utilise des lettres différentes pour les mêmes volumes.</span><span class="sxs-lookup"><span data-stu-id="8a31c-140">This occurs because some information in the offline registry has hard-coded drive letters, and DaRT uses different letters for the same volumes.</span></span> <span data-ttu-id="8a31c-141">Les effets courants incluent l’accès à certains comptes d’utilisateurs locaux dans l’éditeur du Registre.</span><span class="sxs-lookup"><span data-stu-id="8a31c-141">The typical effects include not having access to certain local user accounts in Registry Editor.</span></span> <span data-ttu-id="8a31c-142">Par ailleurs, il est possible que certains outils ne soient pas en mesure d’obtenir des propriétés qui s’appuient sur la résolution des chemins d’accès aux fichiers.</span><span class="sxs-lookup"><span data-stu-id="8a31c-142">Additionally, some tools may be unable to obtain properties that rely on resolving file paths.</span></span>

<span data-ttu-id="8a31c-143">**Solution de contournement:** Utilisez l’option pour remapper les lettres de lecteur au démarrage de DaRT.</span><span class="sxs-lookup"><span data-stu-id="8a31c-143">**Workaround:** Use the option to remap the drive letters as DaRT starts.</span></span> <span data-ttu-id="8a31c-144">Cela aligne généralement les lettres de lecteur typiques sur ce qui est attendu.</span><span class="sxs-lookup"><span data-stu-id="8a31c-144">This usually aligns the typical drive letters to what is expected.</span></span>

### <span data-ttu-id="8a31c-145">La désinstallation de HotFix ne peut pas désinstaller certaines mises à jour</span><span class="sxs-lookup"><span data-stu-id="8a31c-145">Hotfix Uninstall might not uninstall certain updates</span></span>

<span data-ttu-id="8a31c-146">Certains service packs et mises à jour ne peuvent pas être désinstallés parce qu’ils sont marqués comme étant désinstallés ou qu’ils doivent être désinstallés dans Windows 7.</span><span class="sxs-lookup"><span data-stu-id="8a31c-146">Some updates and service packs cannot be uninstalled because they are marked as un-installable or because they need to be uninstalled from within Windows 7.</span></span> <span data-ttu-id="8a31c-147">Dans ces cas, l’outil de désinstallation de correctif risque d’indiquer que ces mises à jour ont été désinstallées, même si elles ne le sont pas.</span><span class="sxs-lookup"><span data-stu-id="8a31c-147">In these instances, the Hotfix Uninstall tool may indicate that these updates have been uninstalled even though they have not been.</span></span>

<span data-ttu-id="8a31c-148">**Solution de contournement:** Désinstaller ces mises à jour problématiques de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="8a31c-148">**Workaround:** Uninstall these problematic updates from Windows 7.</span></span>

### <span data-ttu-id="8a31c-149">Effacement de disque: les disques contenant des volumes fractionnés, des volumes agrégés ou des volumes en miroir ne peuvent pas être supprimés.</span><span class="sxs-lookup"><span data-stu-id="8a31c-149">Disk Wipe: Disks with spanned volumes, striped volumes, or mirrored volumes cannot be deleted</span></span>

<span data-ttu-id="8a31c-150">La réinitialisation du disque ne prend pas en charge la suppression de disques qui sont fractionnés, en miroir ou en agrégats entre plusieurs volumes.</span><span class="sxs-lookup"><span data-stu-id="8a31c-150">Disk Wipe does not support deleting disks that are spanned, mirrored, or striped across one or more volumes.</span></span>

<span data-ttu-id="8a31c-151">**Solution de contournement:** Sélectionnez et supprimez chaque disque dans le volume séparément.</span><span class="sxs-lookup"><span data-stu-id="8a31c-151">**Workaround:** Select and delete each disk in the volume separately.</span></span>

## <span data-ttu-id="8a31c-152">Informations de copyright des notes de publication</span><span class="sxs-lookup"><span data-stu-id="8a31c-152">Release Notes Copyright Information</span></span>


<span data-ttu-id="8a31c-153">Ce document est fourni «en l’absence».</span><span class="sxs-lookup"><span data-stu-id="8a31c-153">This document is provided “as-is”.</span></span> <span data-ttu-id="8a31c-154">Les informations et les vues exprimées dans le présent document, y compris les URL et les autres références de site Web Internet, risquent de changer sans préavis.</span><span class="sxs-lookup"><span data-stu-id="8a31c-154">Information and views expressed in this document, including URL and other Internet website references, may change without notice.</span></span> <span data-ttu-id="8a31c-155">Vous assumez le risque d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="8a31c-155">You bear the risk of using it.</span></span>

<span data-ttu-id="8a31c-156">Quelques exemples présentés dans les présentes sont fournis à titre indicatif uniquement et sont fictifs.</span><span class="sxs-lookup"><span data-stu-id="8a31c-156">Some examples depicted herein are provided for illustration only and are fictitious.</span></span><span data-ttu-id="8a31c-157">Aucune association ou connexion réelle ne doit être intentionnelle ou intentionnelle.</span><span class="sxs-lookup"><span data-stu-id="8a31c-157">No real association or connection is intended or should be inferred.</span></span>

<span data-ttu-id="8a31c-158">Ce document ne vous fournit aucun droit légal de propriété intellectuelle de tout produit Microsoft.</span><span class="sxs-lookup"><span data-stu-id="8a31c-158">This document does not provide you with any legal rights to any intellectual property in any Microsoft product.</span></span> <span data-ttu-id="8a31c-159">Ce document est confidentiel et exclusif à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="8a31c-159">This document is confidential and proprietary to Microsoft.</span></span> <span data-ttu-id="8a31c-160">Il est divulgué et ne peut être utilisé que dans le cadre d’un accord de non-divulgation.</span><span class="sxs-lookup"><span data-stu-id="8a31c-160">It is disclosed and can be used only pursuant to a nondisclosure agreement.</span></span>



<span data-ttu-id="8a31c-161">Microsoft, Active Directory, ActiveSync, MS-DOS, Windows, windowsserver2003 et Windows Vista sont des marques commerciales du groupe de sociétés Microsoft.</span><span class="sxs-lookup"><span data-stu-id="8a31c-161">Microsoft, Active Directory, ActiveSync, MS-DOS, Windows, WindowsServer, and Windows Vista are trademarks of the Microsoft group of companies.</span></span>

<span data-ttu-id="8a31c-162">Toutes les autres marques déposées sont la propriété de leurs détenteurs respectifs.</span><span class="sxs-lookup"><span data-stu-id="8a31c-162">All other trademarks are property of their respective owners.</span></span>

## <span data-ttu-id="8a31c-163">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8a31c-163">Related topics</span></span>


[<span data-ttu-id="8a31c-164">À propos de DaRT7.0</span><span class="sxs-lookup"><span data-stu-id="8a31c-164">About DaRT 7.0</span></span>](about-dart-70-new-ia.md)

 

 





