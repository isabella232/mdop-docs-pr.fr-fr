---
title: Procédure pour installer le client App-V Client à l'aide de setup.msi
description: Procédure pour installer le client App-V Client à l'aide de setup.msi
author: dansimp
ms.assetid: 7221f384-36d6-409a-94a2-86f54fd75322
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7fb3a145a6c57cccbae3f4e6b191b89d93278ff8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807065"
---
# <span data-ttu-id="007a7-103">Procédure pour installer le client App-V Client à l'aide de setup.msi</span><span class="sxs-lookup"><span data-stu-id="007a7-103">How to Install the App-V Client by Using Setup.msi</span></span>


<span data-ttu-id="007a7-104">Cette rubrique explique comment installer le client App-V à l’aide du programme setup.msi.</span><span class="sxs-lookup"><span data-stu-id="007a7-104">This topic describes how to install the App-V client by using the setup.msi program.</span></span> <span data-ttu-id="007a7-105">Avant d’installer le client App-V à l’aide du programme setup.msi, vous devez d’abord déterminer si des logiciels requis doivent être installés, puis vous devez l’installer.</span><span class="sxs-lookup"><span data-stu-id="007a7-105">Before you install the App-V client using the setup.msi program, you must first determine if any prerequisite software must be installed, and then you must install it.</span></span> <span data-ttu-id="007a7-106">Pour installer les logiciels requis, voir la section [installation de logiciels requis](#prereq-sw) de cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="007a7-106">To install the prerequisite software, see the [Installing Prerequisite Software](#prereq-sw) section of this topic.</span></span> <span data-ttu-id="007a7-107">Pour installer le logiciel client, reportez-vous à la section [installation du client App-V à l’aide de la Setup.msi programme](#msi-setup) de cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="007a7-107">To install the client software, see the [Installing the App-V Client Using the Setup.msi Program](#msi-setup) section of this topic.</span></span>

## <a href="" id="prereq-sw"></a><span data-ttu-id="007a7-108">Installation de logiciels requis</span><span class="sxs-lookup"><span data-stu-id="007a7-108">Installing Prerequisite Software</span></span>


<span data-ttu-id="007a7-109">Vous pouvez utiliser les procédures suivantes pour installer les logiciels requis.</span><span class="sxs-lookup"><span data-stu-id="007a7-109">You can use the following procedures to install the prerequisite software.</span></span> <span data-ttu-id="007a7-110">Vous pouvez créer un fichier de commandes et exécuter les commandes à partir de l’invite de commandes, ou vous pouvez utiliser un langage de script tel que VBScript ou Windows PowerShell pour exécuter les commandes.</span><span class="sxs-lookup"><span data-stu-id="007a7-110">You can create a command file and run the commands from the command prompt, or you can use a scripting language such as VBScript or Windows PowerShell to run the commands.</span></span>

<span data-ttu-id="007a7-111">**Remarques**  Les versions x86 des logiciels suivants sont requises pour les versions x86 et x64 du client App-V.</span><span class="sxs-lookup"><span data-stu-id="007a7-111">**Note** The x86 versions of the following software are required for both x86 and x64 versions of the App-V client.</span></span>

 

**<span data-ttu-id="007a7-112">Pour installer le package redistribuable Microsoft VisualC + + 2005SP1 (x86)</span><span class="sxs-lookup"><span data-stu-id="007a7-112">To install Microsoft VisualC++2005SP1 Redistributable Package (x86)</span></span>**

1. <span data-ttu-id="007a7-113">Téléchargez le package de logiciels [Microsoft Visual C++ 2005 SP1 (x86)](https://go.microsoft.com/fwlink/?LinkId=119961) à partir du centre de téléchargement Microsoft ( <https://go.microsoft.com/fwlink/?LinkId=119961> ).</span><span class="sxs-lookup"><span data-stu-id="007a7-113">Download the [Microsoft Visual C++ 2005 SP1 Redistributable Package (x86)](https://go.microsoft.com/fwlink/?LinkId=119961) software package from the Microsoft Download Center (<https://go.microsoft.com/fwlink/?LinkId=119961>).</span></span> <span data-ttu-id="007a7-114">\ [Valeur de jeton de modèle \] pour la version 4,5 SP2 et les versions ultérieures du client App-V, téléchargez vcredist\_x86.exe à partir de [Microsoft Visual C++ 2005 Service Pack 1 package redistribuable la mise à jour de sécurité ATL](https://go.microsoft.com/fwlink/?LinkId=169360) ( https://go.microsoft.com/fwlink/?LinkId=169360).\ [valeur du jeton de modèle]</span><span class="sxs-lookup"><span data-stu-id="007a7-114">\[Template Token Value\] For version 4.5 SP2 and later of the App-V client, download vcredist\_x86.exe from [Microsoft Visual C++ 2005 Service Pack 1 Redistributable Package ATL Security Update](https://go.microsoft.com/fwlink/?LinkId=169360) (https://go.microsoft.com/fwlink/?LinkId=169360).\[Template Token Value\]</span></span>

2. <span data-ttu-id="007a7-115">Pour procéder à l’installation en silence, utilisez l’option de ligne de commande «/Q» avec vcredist\_x86.exe, par exemple **vcredist\_x86.exe/q**.</span><span class="sxs-lookup"><span data-stu-id="007a7-115">To install silently, use the command-line option “/Q” with vcredist\_x86.exe—for example, **vcredist\_x86.exe /Q**.</span></span>

3. <span data-ttu-id="007a7-116">Pour installer le logiciel à l’aide du fichier vcredist\_x86.msi, utilisez l’option de ligne de commande «/C/T: &lt; fullpathtofolder &gt; » pour extraire les fichiers vcredist.msi et vcredis1.cab de vcredist\_x86.exe dans un dossier temporaire.</span><span class="sxs-lookup"><span data-stu-id="007a7-116">To install the software by using the vcredist\_x86.msi file, use the command-line option “/C /T:&lt;fullpathtofolder&gt;” to extract the files vcredist.msi and vcredis1.cab from vcredist\_x86.exe to a temporary folder.</span></span> <span data-ttu-id="007a7-117">Pour procéder à l’installation en silence, utilisez l’option/quiet de la ligne de commande (par exemple, **msiexec/i vcredist.msi** /quiet.</span><span class="sxs-lookup"><span data-stu-id="007a7-117">To install silently, use the command-line option /quiet—for example, **msiexec /i vcredist.msi** /quiet.</span></span>

### <span data-ttu-id="007a7-118">Pour installer le package redistribuable Microsoft VisualC + + 2008SP1 (x86)</span><span class="sxs-lookup"><span data-stu-id="007a7-118">To install Microsoft VisualC++2008SP1 Redistributable Package (x86)</span></span>

<span data-ttu-id="007a7-119">**Important**  Pour la version 4.6 et une version ultérieure du client App-V, vous devez également installer la mise à jour de sécurité ATL du package redistribuable Microsoft Visual C++ 2008.</span><span class="sxs-lookup"><span data-stu-id="007a7-119">**Important** For version4.6 and later of the App-V client, you must also install the Microsoft Visual C++ 2008 Service Pack 1 Redistributable Package ATL Security Update.</span></span>

 

****

1.  <span data-ttu-id="007a7-120">Téléchargez le package de logiciels de [mise à jour de sécurité ATL de Microsoft Visual C++ 2008 Service Pack 1](https://go.microsoft.com/fwlink/?LinkId=150700) à partir du centre de téléchargement Microsoft ( https://go.microsoft.com/fwlink/?LinkId=150700) .</span><span class="sxs-lookup"><span data-stu-id="007a7-120">Download the [Microsoft Visual C++ 2008 Service Pack 1 Redistributable Package ATL Security Update](https://go.microsoft.com/fwlink/?LinkId=150700) software package from the Microsoft Download Center (https://go.microsoft.com/fwlink/?LinkId=150700).</span></span>

2.  <span data-ttu-id="007a7-121">Pour procéder à l’installation en silence, utilisez l’option de ligne de commande «/Q» avec vcredist\_x86.exe, par exemple **vcredist\_x86.exe/q**.</span><span class="sxs-lookup"><span data-stu-id="007a7-121">To install silently, use the command-line option “/Q” with vcredist\_x86.exe—for example, **vcredist\_x86.exe /Q**.</span></span>

### <span data-ttu-id="007a7-122">Pour installer Microsoft Core XML Services (MSXML) 6.0 SP1 (x86)</span><span class="sxs-lookup"><span data-stu-id="007a7-122">To install Microsoft Core XML Services (MSXML)6.0SP1 (x86)</span></span>

****

1.  <span data-ttu-id="007a7-123">Téléchargez le package de logiciels [Microsoft Core XML Services (MSXML) 6.0 SP1 (x86)](https://go.microsoft.com/fwlink/?LinkId=63266) à partir du centre de téléchargement Microsoft ( https://go.microsoft.com/fwlink/?LinkId=63266) .</span><span class="sxs-lookup"><span data-stu-id="007a7-123">Download the [Microsoft Core XML Services (MSXML)6.0SP1 (x86)](https://go.microsoft.com/fwlink/?LinkId=63266) software package from the Microsoft Download Center (https://go.microsoft.com/fwlink/?LinkId=63266).</span></span>

2.  <span data-ttu-id="007a7-124">Pour procéder à l’installation en silence, utilisez l’option/quiet de la ligne de commande (par exemple, **msiexec/i msxml6\_x86.msi/quiet**).</span><span class="sxs-lookup"><span data-stu-id="007a7-124">To install silently, use the command-line option /quiet—for example, **msiexec /i msxml6\_x86.msi /quiet**.</span></span>

### <span data-ttu-id="007a7-125">Pour installer le rapport d’erreurs d’application Microsoft</span><span class="sxs-lookup"><span data-stu-id="007a7-125">To install Microsoft Application Error Reporting</span></span>

<span data-ttu-id="007a7-126">Lors de l’installation du rapport d’erreurs d’application Microsoft, vous devez utiliser le paramètre *APPGUID* pour spécifier le code de produit App-V.</span><span class="sxs-lookup"><span data-stu-id="007a7-126">When installing Microsoft Application Error Reporting, you must use the *APPGUID* parameter to specify the App-V product code.</span></span> <span data-ttu-id="007a7-127">Le code de produit est unique pour chaque type et version de client App-V.</span><span class="sxs-lookup"><span data-stu-id="007a7-127">The product code is unique for each App-V client type and version.</span></span> <span data-ttu-id="007a7-128">Sélectionnez le bon code de produit du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="007a7-128">Select the correct product code from the following table.</span></span>

<span data-ttu-id="007a7-129">**Important**  Pour App-V 4.6 SP2 et les versions ultérieures, vous n’avez plus besoin d’installer le signalement d’erreurs des applications Microsoft (dw20shared.msi).</span><span class="sxs-lookup"><span data-stu-id="007a7-129">**Important** For App-V4.6SP2 and later, you no longer need to install Microsoft Application Error Reporting (dw20shared.msi).</span></span> <span data-ttu-id="007a7-130">App-V utilise désormais le signalement d’erreurs Microsoft.</span><span class="sxs-lookup"><span data-stu-id="007a7-130">App-V now uses Microsoft Error Reporting.</span></span>

 

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="007a7-131">Version</span><span class="sxs-lookup"><span data-stu-id="007a7-131">Version</span></span></th>
<th align="left"><span data-ttu-id="007a7-132">Code de produit pour le client de bureau</span><span class="sxs-lookup"><span data-stu-id="007a7-132">Product Code for Desktop Client</span></span></th>
<th align="left"><span data-ttu-id="007a7-133">Code de produit du client pour les services Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="007a7-133">Product Code for Client for Remote Desktop Services</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="007a7-134">App-V 4,5 CU1</span><span class="sxs-lookup"><span data-stu-id="007a7-134">App-V 4.5 CU1</span></span></p></td>
<td align="left"><p><span data-ttu-id="007a7-135">FE495DBC-6D42-4698-B61F-86E655E0796D</span><span class="sxs-lookup"><span data-stu-id="007a7-135">FE495DBC-6D42-4698-B61F-86E655E0796D</span></span></p></td>
<td align="left"><p><span data-ttu-id="007a7-136">8A97C241-D92A-47DC-B360-E716C1AAA929</span><span class="sxs-lookup"><span data-stu-id="007a7-136">8A97C241-D92A-47DC-B360-E716C1AAA929</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="007a7-137">App-V 4,5 SP1</span><span class="sxs-lookup"><span data-stu-id="007a7-137">App-V 4.5 SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="007a7-138">93468B43-C19D-44F9-8BCC-114076DB0443</span><span class="sxs-lookup"><span data-stu-id="007a7-138">93468B43-C19D-44F9-8BCC-114076DB0443</span></span></p></td>
<td align="left"><p><span data-ttu-id="007a7-139">0042AD3C-99A4-4E58-B5F0-744D5AD96E1C</span><span class="sxs-lookup"><span data-stu-id="007a7-139">0042AD3C-99A4-4E58-B5F0-744D5AD96E1C</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="007a7-140">App-V 4,5 SP2</span><span class="sxs-lookup"><span data-stu-id="007a7-140">App-V 4.5 SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="007a7-141">C6FC75B9-7D86-4C44-8BDB-EAFE1F0E200D</span><span class="sxs-lookup"><span data-stu-id="007a7-141">C6FC75B9-7D86-4C44-8BDB-EAFE1F0E200D</span></span></p></td>
<td align="left"><p><span data-ttu-id="007a7-142">ECF80BBA-CA07-4A74-9ED6-E064F38AF1F5</span><span class="sxs-lookup"><span data-stu-id="007a7-142">ECF80BBA-CA07-4A74-9ED6-E064F38AF1F5</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="007a7-143">App-V 4,6 x86</span><span class="sxs-lookup"><span data-stu-id="007a7-143">App-V 4.6 x86</span></span></p></td>
<td align="left"><p><span data-ttu-id="007a7-144">9E9D30B2-2065-4FDE-B756-8F1A6EABAFC3</span><span class="sxs-lookup"><span data-stu-id="007a7-144">9E9D30B2-2065-4FDE-B756-8F1A6EABAFC3</span></span></p></td>
<td align="left"><p><span data-ttu-id="007a7-145">439FAC21-B423-41D4-8126-54F9FCB70039</span><span class="sxs-lookup"><span data-stu-id="007a7-145">439FAC21-B423-41D4-8126-54F9FCB70039</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="007a7-146">App-V 4,6 x64</span><span class="sxs-lookup"><span data-stu-id="007a7-146">App-V 4.6 x64</span></span></p></td>
<td align="left"><p><span data-ttu-id="007a7-147">E569E45F-7BA6-4C7F-B6BA-3FFCBE92FC22</span><span class="sxs-lookup"><span data-stu-id="007a7-147">E569E45F-7BA6-4C7F-B6BA-3FFCBE92FC22</span></span></p></td>
<td align="left"><p><span data-ttu-id="007a7-148">D2977C18-D88A-47CB-AFD8-652DD36F4D0D</span><span class="sxs-lookup"><span data-stu-id="007a7-148">D2977C18-D88A-47CB-AFD8-652DD36F4D0D</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="007a7-149">App-V 4,6 x86 ¹</span><span class="sxs-lookup"><span data-stu-id="007a7-149">App-V 4.6 x86 ¹</span></span></p></td>
<td align="left"><p><span data-ttu-id="007a7-150">40C3258B-F9D1-46DF-AE97-72C1F86F2427</span><span class="sxs-lookup"><span data-stu-id="007a7-150">40C3258B-F9D1-46DF-AE97-72C1F86F2427</span></span></p></td>
<td align="left"><p><span data-ttu-id="007a7-151">9915D911-CC73-4122-AF4F-564F89454655</span><span class="sxs-lookup"><span data-stu-id="007a7-151">9915D911-CC73-4122-AF4F-564F89454655</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="007a7-152">App-V 4,6 x64 ¹</span><span class="sxs-lookup"><span data-stu-id="007a7-152">App-V 4.6 x64 ¹</span></span></p></td>
<td align="left"><p><span data-ttu-id="007a7-153">1650E31F-23B8-40B5-A60A-C5934F557E3B</span><span class="sxs-lookup"><span data-stu-id="007a7-153">1650E31F-23B8-40B5-A60A-C5934F557E3B</span></span></p></td>
<td align="left"><p><span data-ttu-id="007a7-154">7580D918-C621-49E7-9877-3CC59F9BD1DA</span><span class="sxs-lookup"><span data-stu-id="007a7-154">7580D918-C621-49E7-9877-3CC59F9BD1DA</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="007a7-155">App-V 4,6 x86 SP1</span><span class="sxs-lookup"><span data-stu-id="007a7-155">App-V 4.6 x86 SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="007a7-156">DB9F70CD-29BC-480B-8BA2-C9C2232C4553</span><span class="sxs-lookup"><span data-stu-id="007a7-156">DB9F70CD-29BC-480B-8BA2-C9C2232C4553</span></span></p></td>
<td align="left"><p><span data-ttu-id="007a7-157">1354855A-2298-4C73-9022-EF0686C65991</span><span class="sxs-lookup"><span data-stu-id="007a7-157">1354855A-2298-4C73-9022-EF0686C65991</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="007a7-158">App-V 4,6 x64 SP1</span><span class="sxs-lookup"><span data-stu-id="007a7-158">App-V 4.6 x64 SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="007a7-159">342C9BB8-65A0-46DE-AB7A-8031E151AF69</span><span class="sxs-lookup"><span data-stu-id="007a7-159">342C9BB8-65A0-46DE-AB7A-8031E151AF69</span></span></p></td>
<td align="left"><p><span data-ttu-id="007a7-160">B2C6C8D5-FE76-4056-A326-EE5D633EA175</span><span class="sxs-lookup"><span data-stu-id="007a7-160">B2C6C8D5-FE76-4056-A326-EE5D633EA175</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="007a7-161">¹ version «langues» App-V.</span><span class="sxs-lookup"><span data-stu-id="007a7-161">¹App-V “Languages” release.</span></span>

<span data-ttu-id="007a7-162">**Remarques**  Si vous avez besoin de trouver le code de produit, vous pouvez utiliser l’éditeur de base de données Orca.exe ou un outil similaire pour examiner les fichiers Windows Installer et rechercher la valeur de la propriété *ProductCode* .</span><span class="sxs-lookup"><span data-stu-id="007a7-162">**Note** If you need to find the product code, you can use the Orca.exe database editor or a similar tool to examine Windows Installer files to find the value of the *ProductCode* property.</span></span> <span data-ttu-id="007a7-163">Pour plus d’informations sur l’utilisation de Orca.exe, voir [outils de développement Windows Installer](https://go.microsoft.com/fwlink/?LinkId=150008) ( https://go.microsoft.com/fwlink/?LinkId=150008) .</span><span class="sxs-lookup"><span data-stu-id="007a7-163">For more information about using Orca.exe, see [Windows Installer Development Tools](https://go.microsoft.com/fwlink/?LinkId=150008) (https://go.microsoft.com/fwlink/?LinkId=150008).</span></span>

 

****

1.  <span data-ttu-id="007a7-164">Recherchez le programme d’installation du signalement d’erreurs Microsoft application, dw20shared.msi, qui se trouve dans le dossier **Support\\Watson** sur le média de publication.</span><span class="sxs-lookup"><span data-stu-id="007a7-164">Locate the Microsoft Application Error Reporting install program, dw20shared.msi, which can be found in the **Support\\Watson** folder on the release media.</span></span>

2.  <span data-ttu-id="007a7-165">Pour installer le logiciel, exécutez la commande suivante:</span><span class="sxs-lookup"><span data-stu-id="007a7-165">To install the software, run the following command:</span></span>

         **msiexec /i dw20shared.msi APPGUID={valuefromtable} REBOOT=Suppress REINSTALL=ALL REINSTALLMODE=vomus**

## <a href="" id="msi-setup"></a><span data-ttu-id="007a7-166">Installation du client App-V à l’aide du programme Setup.msi</span><span class="sxs-lookup"><span data-stu-id="007a7-166">Installing the App-V Client by Using the Setup.msi Program</span></span>


<span data-ttu-id="007a7-167">Utilisez la procédure suivante pour installer le client App-V.</span><span class="sxs-lookup"><span data-stu-id="007a7-167">Use the following procedure to install the App-V client.</span></span> <span data-ttu-id="007a7-168">Assurez-vous que tous les logiciels requis requis sont installés.</span><span class="sxs-lookup"><span data-stu-id="007a7-168">Ensure that any necessary prerequisite software has been installed.</span></span> <span data-ttu-id="007a7-169">\ [Valeur de jeton de modèle] pour la version 4.6 et les versions ultérieures du client App-V, le programme setup.msi vérifie le système et, si la configuration logicielle requise n’est pas installée, il génère un message d’erreur indiquant que l’installation ne peut pas continuer.</span><span class="sxs-lookup"><span data-stu-id="007a7-169">\[Template Token Value\] For version4.6 and later of the App-V client, the setup.msi program checks the system and if prerequisite software is not installed, it generates an error message indicating that installation cannot continue.</span></span> <span data-ttu-id="007a7-170">\ [Valeur du jeton de modèle \]</span><span class="sxs-lookup"><span data-stu-id="007a7-170">\[Template Token Value\]</span></span>

**<span data-ttu-id="007a7-171">Pour installer le client de virtualisation des applications à l’aide de Setup.msi</span><span class="sxs-lookup"><span data-stu-id="007a7-171">To install the Application Virtualization Client by Using Setup.msi</span></span>**

1.  <span data-ttu-id="007a7-172">Vérifiez que vous êtes connecté avec un compte disposant de droits d’administrateur sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="007a7-172">Make sure you are logged on with an account that has administrator rights on the computer.</span></span>

2.  <span data-ttu-id="007a7-173">Ouvrez une fenêtre d’invite de commandes à l’aide de droits élevés, puis modifiez le répertoire dans le dossier contenant les fichiers d’installation.</span><span class="sxs-lookup"><span data-stu-id="007a7-173">Open a Command Prompt window by using elevated rights, and then change the directory to the folder that contains the setup files.</span></span> <span data-ttu-id="007a7-174">Lors de l’installation de la version 4.6 ou d’une version ultérieure du client App-V, vous devez utiliser le programme d’installation approprié pour le système d’exploitation de l’ordinateur, 32 ou 64 bits.</span><span class="sxs-lookup"><span data-stu-id="007a7-174">When installing version4.6 or a later version of the App-V client, you must use the correct installer for the computer’s operating system, 32-bit or 64-bit.</span></span> <span data-ttu-id="007a7-175">L’installation échoue et un message d’erreur s’affiche si vous utilisez le mauvais programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="007a7-175">The installation will fail and an error message will be displayed if you use the wrong installer.</span></span>

3.  <span data-ttu-id="007a7-176">Entrez la chaîne de commande d’installation à l’invite de commandes.</span><span class="sxs-lookup"><span data-stu-id="007a7-176">Enter the install command string at the command prompt.</span></span> <span data-ttu-id="007a7-177">Vous pouvez également créer un fichier de commandes et l’exécuter à partir de l’invite de commandes.</span><span class="sxs-lookup"><span data-stu-id="007a7-177">Alternatively, you can create a command file and run it from the command prompt.</span></span> <span data-ttu-id="007a7-178">Vous pouvez également utiliser un langage de script tel que VBScript ou Windows PowerShell pour exécuter la commande.</span><span class="sxs-lookup"><span data-stu-id="007a7-178">You can also use a scripting language such as VBScript or Windows PowerShell to run the command.</span></span>

4.  <span data-ttu-id="007a7-179">L’exemple de ligne de commande suivant montre comment setup.msi peut être utilisé avec plusieurs paramètres facultatifs.</span><span class="sxs-lookup"><span data-stu-id="007a7-179">The following command-line example shows how setup.msi can be used with a number of optional parameters.</span></span> <span data-ttu-id="007a7-180">Pour plus d’informations sur ces paramètres, voir [paramètres de ligne de commande du programme de virtualisation des applications](application-virtualization-client-installer-command-line-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="007a7-180">For more information about these parameters, see [Application Virtualization Client Installer Command-Line Parameters](application-virtualization-client-installer-command-line-parameters.md).</span></span>

    **<span data-ttu-id="007a7-181">msiexec.exe/i "setup.msi" SWICACHESIZE = "10 240" SWIPUBSVRDISPLAY = "système de production" SWIPUBSVRTYPE = "HTTP/Secure" SWIPUBSVRHOST = "PRODSYS" SWIPUBSVRPORT = "443" SWIPUBSVRPATH = "/AppVirt/appsntype.xml" SWIPUBSVRREFRESH = "sur" SWIGLOBALDATA = "D:\\AppVirt\\Global" SWIUSERDATA = "^% LOCALAPPDATA ^%\\Windows\\Application virtualisation client" SWIFSDRIVE = "S"/q</span><span class="sxs-lookup"><span data-stu-id="007a7-181">msiexec.exe /i "setup.msi" SWICACHESIZE="10240" SWIPUBSVRDISPLAY="Production System" SWIPUBSVRTYPE="HTTP /secure" SWIPUBSVRHOST="PRODSYS" SWIPUBSVRPORT="443" SWIPUBSVRPATH="/AppVirt/appsntype.xml" SWIPUBSVRREFRESH="on" SWIGLOBALDATA="D:\\AppVirt\\Global" SWIUSERDATA="^% LOCALAPPDATA^%\\Windows\\Application Virtualization Client" SWIFSDRIVE="S" /q</span></span>**

    **<span data-ttu-id="007a7-182">Important</span><span class="sxs-lookup"><span data-stu-id="007a7-182">Important</span></span>**  
    -   <span data-ttu-id="007a7-183">Le commutateur Windows Installer «**/q**» est utilisé pour effectuer une installation silencieuse.</span><span class="sxs-lookup"><span data-stu-id="007a7-183">The Windows Installer switch "**/q**" is used to make this a silent installation.</span></span>

    -   <span data-ttu-id="007a7-184">Le caractère «» **%** doit être précédé du caractère «» dans «**% HomeDrive%**» **^** .</span><span class="sxs-lookup"><span data-stu-id="007a7-184">The "**%**" characters in "**%HomeDrive%**" must be preceded by the "**^**" escape character.</span></span> <span data-ttu-id="007a7-185">Dans le cas contraire, l’interpréteur de commandes Windows définit la valeur sur celle de l’utilisateur qui exécute l’installation.</span><span class="sxs-lookup"><span data-stu-id="007a7-185">Otherwise, the Windows command shell sets the value to that of the user who is performing the installation.</span></span>

    -   <span data-ttu-id="007a7-186">Pour activer la journalisation de l’installation, utilisez le \**fichier/l\**</span><span class="sxs-lookup"><span data-stu-id="007a7-186">To turn on installation logging, use the msiexec switch **/l\*v filename.log**.</span></span>

     

## <span data-ttu-id="007a7-187">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="007a7-187">Related topics</span></span>


[<span data-ttu-id="007a7-188">Procédure pour installer le client via la ligne de commande</span><span class="sxs-lookup"><span data-stu-id="007a7-188">How to Install the Client by Using the Command Line</span></span>](how-to-install-the-client-by-using-the-command-line-new.md)

 

 





