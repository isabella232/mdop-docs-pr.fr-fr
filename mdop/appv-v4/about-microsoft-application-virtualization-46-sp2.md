---
title: À propos de Microsoft Application Virtualization4.6 SP2
description: À propos de Microsoft Application Virtualization4.6 SP2
author: dansimp
ms.assetid: 1429e314-9c38-472b-8687-3bed6cf0015c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 16303380782a086cfd750c7a8b2f99bf4f4c8b5d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808138"
---
# <span data-ttu-id="95171-103">À propos de Microsoft Application Virtualization4.6 SP2</span><span class="sxs-lookup"><span data-stu-id="95171-103">About Microsoft Application Virtualization 4.6 SP2</span></span>


<span data-ttu-id="95171-104">Microsoft Application Virtualization (App-V) 4.6 SP2 fournit différentes améliorations et nouvelles fonctionnalités, décrites dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="95171-104">Microsoft Application Virtualization (App-V)4.6 SP2 provides several enhancements and new features, which are described in this topic.</span></span>

<span data-ttu-id="95171-105">**Attention**  Cette rubrique explique comment modifier le Registre Windows à l’aide de l’éditeur du Registre.</span><span class="sxs-lookup"><span data-stu-id="95171-105">**Caution** This topic describes how to change the Windows registry by using Registry Editor.</span></span> <span data-ttu-id="95171-106">Si vous modifiez la clé de registre de Windows de manière incorrecte, vous pouvez être à l’origine de problèmes importants qui peuvent nécessiter la réinstallation de Windows.</span><span class="sxs-lookup"><span data-stu-id="95171-106">If you change the Windows registry incorrectly, you can cause serious problems that might require you to reinstall Windows.</span></span> <span data-ttu-id="95171-107">Vous devez faire une copie de sauvegarde des fichiers du Registre (System. dat et User. dat) avant de modifier le registre.</span><span class="sxs-lookup"><span data-stu-id="95171-107">You should make a backup copy of the registry files (System.dat and User.dat) before you change the registry.</span></span> <span data-ttu-id="95171-108">Microsoft ne peut pas garantir que les problèmes qui peuvent survenir lorsque vous modifiez le registre peuvent être résolus.</span><span class="sxs-lookup"><span data-stu-id="95171-108">Microsoft cannot guarantee that the problems that might occur when you change the registry can be resolved.</span></span> <span data-ttu-id="95171-109">Changez de Registre à vos propres risques.</span><span class="sxs-lookup"><span data-stu-id="95171-109">Change the registry at your own risk.</span></span>

 

**<span data-ttu-id="95171-110">Prise en charge de Windows 8 et Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="95171-110">Support for Windows 8 and Windows Server 2012</span></span>**

<span data-ttu-id="95171-111">App-V 4.6 SP2 ajoute la prise en charge des services Bureau à distance de Windows 8 et Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="95171-111">App-V4.6SP2 adds support for Windows 8 and Windows Server 2012 Remote Desktop Services.</span></span>

**<span data-ttu-id="95171-112">Prise en charge de la coexistence avec le client App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="95171-112">Support for coexistence with App-V 5.0 client</span></span>**

<span data-ttu-id="95171-113">App-V 4.6 SP2 fournit une prise en charge de la coexistence avec le client Microsoft Application Virtualization 5,0.</span><span class="sxs-lookup"><span data-stu-id="95171-113">App-V4.6SP2 provides support for coexistence with the Microsoft Application Virtualization 5.0 client.</span></span> <span data-ttu-id="95171-114">Pour obtenir des instructions sur la configuration du client App-v 5,0 pour la coexistence avec le client App-v 4.6 SP2, consultez la documentation de l’application-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="95171-114">Review the App-V 5.0 documentation for instructions on how to configure the App-V 5.0 client for coexistence with the App-V4.6SP2 client.</span></span> <span data-ttu-id="95171-115">Pour plus d’informations sur App-V 5,0, voir [Application Virtualization 5](https://go.microsoft.com/fwlink/?LinkId=267599) sur TechNet.</span><span class="sxs-lookup"><span data-stu-id="95171-115">For more information about App-V 5.0, see [Application Virtualization 5](https://go.microsoft.com/fwlink/?LinkId=267599) on TechNet.</span></span>

**<span data-ttu-id="95171-116">Possibilité de virtualiser Adobe Reader X avec le mode protégé</span><span class="sxs-lookup"><span data-stu-id="95171-116">Ability to virtualize Adobe Reader X with Protected Mode</span></span>**

<span data-ttu-id="95171-117">Pour virtualiser Adobe Reader X, vous pouvez activer la fonction mode protégé en procédant comme suit.</span><span class="sxs-lookup"><span data-stu-id="95171-117">You can virtualize Adobe Reader X with its Protected Mode feature turned on by using the following procedures.</span></span> <span data-ttu-id="95171-118">Auparavant, vous deviez désactiver le mode protégé afin de virtualiser Adobe Reader X.</span><span class="sxs-lookup"><span data-stu-id="95171-118">Previously you had to disable Protected Mode in order to virtualize Adobe Reader X.</span></span>

<span data-ttu-id="95171-119">Avant de lancer le Sequencer App-V, créez la valeur de Registre suivante sous HKEY \ _LOCAL \ _MACHINE \\SOFTWARE \\Microsoft\\SoftGrid\\4.5\\SystemGuard\\Overrides:</span><span class="sxs-lookup"><span data-stu-id="95171-119">Before launching the App-V Sequencer, create the following registry value under HKEY\_LOCAL\_MACHINE\\SOFTWARE \\Microsoft\\SoftGrid\\4.5\\SystemGuard\\Overrides:</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="95171-120">Nom</span><span class="sxs-lookup"><span data-stu-id="95171-120">Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="95171-121">Type</span><span class="sxs-lookup"><span data-stu-id="95171-121">Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="95171-122">Données</span><span class="sxs-lookup"><span data-stu-id="95171-122">Data</span></span></p></td>
<td align="left"><p><span data-ttu-id="95171-123">Description</span><span class="sxs-lookup"><span data-stu-id="95171-123">Description</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="95171-124">EnableVFSPassthrough</span><span class="sxs-lookup"><span data-stu-id="95171-124">EnableVFSPassthrough</span></span></p></td>
<td align="left"><p><span data-ttu-id="95171-125">DWORD</span><span class="sxs-lookup"><span data-stu-id="95171-125">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="95171-126">1</span><span class="sxs-lookup"><span data-stu-id="95171-126">1</span></span></p></td>
<td align="left"><p><span data-ttu-id="95171-127">Définissez cette valeur sur <strong> 1 pour </strong> Démarrer Adobe Reader X en mode protégé lors de la phase de lancement.</span><span class="sxs-lookup"><span data-stu-id="95171-127">Set this value to <strong>1</strong> in order to start Adobe Reader X in Protected Mode during the launch phase.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="95171-128">**Remarques**  Sur un ordinateur exécutant un système d’exploitation 64 bits, créez la valeur Registry sous HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\SystemGuard\\Overrides.</span><span class="sxs-lookup"><span data-stu-id="95171-128">**Note** On a computer running a 64-bit operating system, create the registry value under HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\SystemGuard\\Overrides.</span></span>

 

<span data-ttu-id="95171-129">Pour chaque fichier OSD dans votre package Adobe Reader X, ajoutez les éléments suivants sous l' &lt; élément policies &gt; :</span><span class="sxs-lookup"><span data-stu-id="95171-129">For each OSD-file in your Adobe Reader X package, add the following items under the &lt;POLICIES&gt; element:</span></span>

`<VIRTUAL_FILE_SYSTEM_PASS_THROUGH>TRUE</VIRTUAL_FILE_SYSTEM_PASS_THROUGH>`

`<VIRTUAL_REGISTRY_PASS_THROUGH>TRUE</VIRTUAL_REGISTRY_PASS_THROUGH>`

`<ENFORCE_ACLS_ON_VREG_MODIFY>TRUE</ENFORCE_ACLS_ON_VREG_MODIFY>`

**<span data-ttu-id="95171-130">Paramètre de ligne de commande du nouveau Sequencer</span><span class="sxs-lookup"><span data-stu-id="95171-130">New Sequencer command-line parameter</span></span>**

<span data-ttu-id="95171-131">Lorsque vous créez un accélérateur de package à l’aide de l’interface utilisateur de Sequencer, vous pouvez sélectionner un fichier RTF ou TXT qui fournit des instructions sur la création de packages et de déploiement aux administrateurs qui appliquent l’accélérateur de package.</span><span class="sxs-lookup"><span data-stu-id="95171-131">When you create a Package Accelerator (PA) through the Sequencer GUI, you can select an RTF or TXT file that provides packaging and deployment guidance to the administrators who will apply the Package Accelerator.</span></span> <span data-ttu-id="95171-132">Cette fonctionnalité est désormais disponible à l’aide de l’interface CLI de Sequencer.</span><span class="sxs-lookup"><span data-stu-id="95171-132">This functionality is now available using the Sequencer CLI.</span></span>

`/ACCELERATORDESCRIPTIONFILE:PathToDescriptionFile`

<span data-ttu-id="95171-133">Spécifiez un chemin d’accès à un fichier RTF ou TXT qui fournit des instructions sur le déploiement et l’empaquetage lors de la création d’un accélérateur de package.</span><span class="sxs-lookup"><span data-stu-id="95171-133">Specify a path to an RTF or TXT file that provides packaging and deployment guidance when creating a Package Accelerator.</span></span>

**<span data-ttu-id="95171-134">Le signalement d’erreurs Microsoft application ne doit plus être installé</span><span class="sxs-lookup"><span data-stu-id="95171-134">Microsoft Application Error Reporting no longer needs to be installed</span></span>**

<span data-ttu-id="95171-135">Lorsque vous installez le client App-V 4.6 SP2 à l’aide de setup.msi, vous n’avez plus besoin d’installer le signalement d’erreurs d’application Microsoft (dw20shared.msi).</span><span class="sxs-lookup"><span data-stu-id="95171-135">When you are installing the App-V4.6SP2 client by using setup.msi, you no longer need to install Microsoft Application Error Reporting (dw20shared.msi).</span></span> <span data-ttu-id="95171-136">App-V 4.6 SP2 utilise désormais le signalement d’erreurs Microsoft.</span><span class="sxs-lookup"><span data-stu-id="95171-136">App-V4.6SP2 now uses Microsoft Error Reporting.</span></span> <span data-ttu-id="95171-137">Pour plus d’informations, reportez-vous [à comment installer le client App-V à l’aide de Setup.msi](https://go.microsoft.com/fwlink/?LinkId=267237).</span><span class="sxs-lookup"><span data-stu-id="95171-137">For more information, see [How to Install the App-V Client by Using Setup.msi](https://go.microsoft.com/fwlink/?LinkId=267237).</span></span>

**<span data-ttu-id="95171-138">Commentaires des clients et ROLLUP de HotFix</span><span class="sxs-lookup"><span data-stu-id="95171-138">Customer feedback and hotfix rollup</span></span>**

<span data-ttu-id="95171-139">App-V 4.6 SP2 inclut un correctif cumulatif pour résoudre les problèmes détectés depuis la version App-V 4,6 SP1.</span><span class="sxs-lookup"><span data-stu-id="95171-139">App-V4.6SP2 includes a rollup of fixes to address issues found since the App-V 4.6 SP1 release.</span></span> <span data-ttu-id="95171-140">App-V 4.6 SP2 contient les derniers correctifs de Microsoft Application Virtualization 4,6 SP1 Hotfix 6.</span><span class="sxs-lookup"><span data-stu-id="95171-140">App-V4.6SP2 contains the latest fixes up to and including Microsoft Application Virtualization 4.6 SP1 Hotfix 6.</span></span>

## <span data-ttu-id="95171-141">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="95171-141">In This Section</span></span>


<a href="" id="app-v-4-6-sp2-release-notes"></a>[<span data-ttu-id="95171-142">Notes de publication d'App-V4.6SP2</span><span class="sxs-lookup"><span data-stu-id="95171-142">App-V 4.6 SP2 Release Notes</span></span>](https://go.microsoft.com/fwlink/?LinkId=267600)  
<span data-ttu-id="95171-143">Fournit les informations mises à jour sur les problèmes connus liés à l’application-V 4.6 SP2.</span><span class="sxs-lookup"><span data-stu-id="95171-143">Provides the most up-to-date information about known issues with App-V4.6SP2.</span></span>

 

 





