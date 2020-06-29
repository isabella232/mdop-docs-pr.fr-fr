---
title: Planification de la migration à partir de versions antérieures
description: Planification de la migration à partir de versions antérieures
author: dansimp
ms.assetid: 62967bf1-542f-41b0-838f-c62f3430ac73
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9b239e09da06270b30b401151cf12e817e2cf8d4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806502"
---
# <span data-ttu-id="f3b15-103">Planification de la migration à partir de versions antérieures</span><span class="sxs-lookup"><span data-stu-id="f3b15-103">Planning for Migration from Previous Versions</span></span>


<span data-ttu-id="f3b15-104">Avant d’essayer de procéder à la mise à niveau vers Microsoft Application Virtualization 4.5 ou versions ultérieures, toute version antérieure à 4.1 doit être mise à niveau vers la version 4.1.</span><span class="sxs-lookup"><span data-stu-id="f3b15-104">Before attempting to upgrade to Microsoft Application Virtualization4.5 or later versions, any version prior to4.1 must be upgraded to version4.1.</span></span> <span data-ttu-id="f3b15-105">Envisagez de mettre à niveau vos clients d’abord, puis mettez à niveau les composants serveur.</span><span class="sxs-lookup"><span data-stu-id="f3b15-105">You should plan to upgrade your clients first, and then upgrade the server components.</span></span> <span data-ttu-id="f3b15-106">Les clients qui ont été mis à niveau vers la version 4.5 continuent de fonctionner avec des serveurs de virtualisation des applications qui n’ont pas encore été mis à niveau.</span><span class="sxs-lookup"><span data-stu-id="f3b15-106">Clients that have been upgraded to4.5 will continue to work with Application Virtualization servers that have not yet been upgraded.</span></span> <span data-ttu-id="f3b15-107">Les versions antérieures du client ne sont pas prises en charge sur les serveurs qui ont été mis à niveau vers la version 4.5.</span><span class="sxs-lookup"><span data-stu-id="f3b15-107">Earlier versions of the client are not supported on servers that have been upgraded to4.5.</span></span> <span data-ttu-id="f3b15-108">Pour plus d’informations sur la mise à niveau des composants système, voir [considérations relatives au déploiement et à la mise à niveau](application-virtualization-deployment-and-upgrade-considerations.md)de l’application.</span><span class="sxs-lookup"><span data-stu-id="f3b15-108">For more information about upgrading the system components, see [Application Virtualization Deployment and Upgrade Considerations](application-virtualization-deployment-and-upgrade-considerations.md).</span></span>

<span data-ttu-id="f3b15-109">Pour garantir une migration réussie, vous devez mettre à niveau les composants du système de virtualisation des applications dans l’ordre suivant:</span><span class="sxs-lookup"><span data-stu-id="f3b15-109">To help ensure a successful migration, the Application Virtualization system components should be upgraded in the following order:</span></span>

1.  **<span data-ttu-id="f3b15-110">Clients Microsoft Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="f3b15-110">Microsoft Application Virtualization Clients.</span></span>** <span data-ttu-id="f3b15-111">Pour obtenir des instructions de mise à niveau détaillées, voir [Comment mettre à niveau le client de virtualisation des applications](how-to-upgrade-the-application-virtualization-client.md).</span><span class="sxs-lookup"><span data-stu-id="f3b15-111">For step-by-step upgrade instructions, see [How to Upgrade the Application Virtualization Client](how-to-upgrade-the-application-virtualization-client.md).</span></span>

2.  **<span data-ttu-id="f3b15-112">Serveurs et base de données Microsoft Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="f3b15-112">Microsoft Application Virtualization Servers and Database.</span></span>** <span data-ttu-id="f3b15-113">Pour obtenir des instructions de mise à niveau détaillées, voir [mise à niveau des serveurs et composants système](how-to-upgrade-the-servers-and-system-components.md).</span><span class="sxs-lookup"><span data-stu-id="f3b15-113">For step-by-step upgrade instructions, see [How to Upgrade the Servers and System Components](how-to-upgrade-the-servers-and-system-components.md).</span></span>

    <span data-ttu-id="f3b15-114">**Remarques**  Si vous avez plusieurs accès du serveur à la base de données de virtualisation des applications, tous les serveurs doivent être déconnectés pendant la mise à niveau de la base de données.</span><span class="sxs-lookup"><span data-stu-id="f3b15-114">**Note** If you have more than one server sharing access to the Application Virtualization database, all those servers must be taken offline while the database is being upgraded.</span></span> <span data-ttu-id="f3b15-115">Nous vous conseillons de suivre les pratiques normales de votre entreprise pour la mise à niveau de la base de données, mais il est recommandé de tester la mise à niveau de la base de données en utilisant d’abord une copie de sauvegarde de la base de données sur un serveur de test.</span><span class="sxs-lookup"><span data-stu-id="f3b15-115">You should follow your normal business practices for the database upgrade, but it is highly advisable that you test the database upgrade by using a backup copy of the database first on a test server.</span></span> <span data-ttu-id="f3b15-116">Ensuite, vous devez sélectionner l’un des serveurs pour la première mise à niveau, qui mettra à niveau le schéma de la base de données.</span><span class="sxs-lookup"><span data-stu-id="f3b15-116">Then, you should select one of the servers for the first upgrade, which will upgrade the database schema.</span></span> <span data-ttu-id="f3b15-117">Après avoir effectué la mise à niveau de la base de données de production, vous pouvez mettre à niveau les autres serveurs.</span><span class="sxs-lookup"><span data-stu-id="f3b15-117">After the production database has been successfully upgraded, you can upgrade the other servers.</span></span>

     

3.  **<span data-ttu-id="f3b15-118">Service Web de gestion de Microsoft Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="f3b15-118">Microsoft Application Virtualization Management Web Service.</span></span>** <span data-ttu-id="f3b15-119">Cette étape s’applique uniquement si le service Web de gestion se trouve sur un serveur distinct, ce qui vous oblige à exécuter le programme d’installation du serveur sur ce serveur distinct pour mettre à niveau le service Web.</span><span class="sxs-lookup"><span data-stu-id="f3b15-119">This step applies only if the Management Web Service is on a separate server, which would require that you run the server installer program on that separate server to upgrade the Web service.</span></span> <span data-ttu-id="f3b15-120">Dans le cas contraire, l’étape de mise à niveau précédente du serveur met automatiquement à niveau le service Web de gestion.</span><span class="sxs-lookup"><span data-stu-id="f3b15-120">Otherwise, the previous server upgrade step will automatically upgrade the Management Web Service.</span></span>

4.  **<span data-ttu-id="f3b15-121">Console de gestion de Microsoft Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="f3b15-121">Microsoft Application Virtualization Management Console.</span></span>** <span data-ttu-id="f3b15-122">Cette étape s’applique uniquement si la console de gestion se trouve sur un autre ordinateur, ce qui vous oblige à exécuter le programme d’installation du serveur sur cet ordinateur distinct pour mettre à niveau la console.</span><span class="sxs-lookup"><span data-stu-id="f3b15-122">This step applies only if the Management Console is on a separate computer, which would require that you run the server installer program on that separate computer to upgrade the console.</span></span> <span data-ttu-id="f3b15-123">Dans le cas contraire, l’étape de mise à niveau précédente du serveur met à niveau la console de gestion.</span><span class="sxs-lookup"><span data-stu-id="f3b15-123">Otherwise, the previous server upgrade step will upgrade the Management Console.</span></span>

5.  **<span data-ttu-id="f3b15-124">Microsoft Application Virtualization Sequencer.</span><span class="sxs-lookup"><span data-stu-id="f3b15-124">Microsoft Application Virtualization Sequencer.</span></span>** <span data-ttu-id="f3b15-125">Pour obtenir des instructions détaillées, reportez-vous à la rubrique [Comment installer le Sequencer](how-to-install-the-application-virtualization-sequencer.md).</span><span class="sxs-lookup"><span data-stu-id="f3b15-125">For step-by-step instructions, see [How to Install the Application Virtualization Sequencer](how-to-install-the-application-virtualization-sequencer.md).</span></span> <span data-ttu-id="f3b15-126">Tout package d’application virtuelle séquencé dans la version 4.2 n’aura pas à être reséquencé pour une utilisation avec la version 4.5.</span><span class="sxs-lookup"><span data-stu-id="f3b15-126">Any virtual application packages sequenced in version4.2 will not have to be re-sequenced for use with version4.5.</span></span> <span data-ttu-id="f3b15-127">Toutefois, vous devez envisager de mettre à niveau les packages virtuels vers le format Microsoft Application Virtualization 4.5 Si vous souhaitez appliquer des listes de contrôle d’accès par défaut ou générer un fichier d’installation Windows.</span><span class="sxs-lookup"><span data-stu-id="f3b15-127">However, you should consider upgrading the virtual packages to the Microsoft Application Virtualization4.5 format if you would like to apply default access control lists (ACLs) or generate a Windows Installer file.</span></span> <span data-ttu-id="f3b15-128">Il s’agit d’un processus simple qui nécessite uniquement l’ouverture et l’enregistrement du package d’application virtuel existant avec le Sequencer 4.5.</span><span class="sxs-lookup"><span data-stu-id="f3b15-128">This is a simple process and requires only that the existing virtual application package be opened and saved with the4.5 Sequencer.</span></span> <span data-ttu-id="f3b15-129">Cela peut être automatisé à l’aide de l’interface de ligne de commande du séquence de virtualisation d’application.</span><span class="sxs-lookup"><span data-stu-id="f3b15-129">This can be automated by using the Application Virtualization Sequencer command-line interface.</span></span>

## <a href="" id="app-v-4-6-client-package-support-"></a><span data-ttu-id="f3b15-130">Prise en charge de package client App-V 4.6</span><span class="sxs-lookup"><span data-stu-id="f3b15-130">App-V4.6 Client Package Support</span></span>


<span data-ttu-id="f3b15-131">Vous pouvez déployer des packages créés dans des versions antérieures de App-V pour les clients App-V 4.6.</span><span class="sxs-lookup"><span data-stu-id="f3b15-131">You can deploy packages created in previous versions of App-V to App-V4.6 Clients.</span></span> <span data-ttu-id="f3b15-132">Toutefois, vous devez modifier le fichier **. OSD** associé de manière à inclure les informations appropriées sur le système d’exploitation et l’architecture du processeur.</span><span class="sxs-lookup"><span data-stu-id="f3b15-132">However, you must modify the associated **.osd** file so that it includes the appropriate operating system and chip architecture information.</span></span> <span data-ttu-id="f3b15-133">Utilisez les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="f3b15-133">Use the following values.</span></span>

<table>
<colgroup>
<col width="100%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f3b15-134">Valeur du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="f3b15-134">OS Value</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f3b15-135">&lt;VALEUR du système d’exploitation = «Win2003TS»/&gt;</span><span class="sxs-lookup"><span data-stu-id="f3b15-135">&lt;OS VALUE=”Win2003TS”/&gt;</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f3b15-136">&lt;VALEUR du système d’exploitation = «Win2003TS64»/&gt;</span><span class="sxs-lookup"><span data-stu-id="f3b15-136">&lt;OS VALUE=”Win2003TS64”/&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f3b15-137">&lt;VALEUR du système d’exploitation = «Win2008TS»/&gt;</span><span class="sxs-lookup"><span data-stu-id="f3b15-137">&lt;OS VALUE=”Win2008TS”/&gt;</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f3b15-138">&lt;VALEUR du système d’exploitation = «Win2008TS64»/&gt;</span><span class="sxs-lookup"><span data-stu-id="f3b15-138">&lt;OS VALUE=”Win2008TS64”/&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f3b15-139">&lt;VALEUR du système d’exploitation = «Win2008R2TS64»/&gt;</span><span class="sxs-lookup"><span data-stu-id="f3b15-139">&lt;OS VALUE=”Win2008R2TS64”/&gt;</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f3b15-140">&lt;VALEUR du système d’exploitation = «Win7»/&gt;</span><span class="sxs-lookup"><span data-stu-id="f3b15-140">&lt;OS VALUE=”Win7”/&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f3b15-141">&lt;VALEUR du système d’exploitation = «Win764»/&gt;</span><span class="sxs-lookup"><span data-stu-id="f3b15-141">&lt;OS VALUE=”Win764”/&gt;</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f3b15-142">&lt;VALEUR du système d’exploitation = «WinVista»/&gt;</span><span class="sxs-lookup"><span data-stu-id="f3b15-142">&lt;OS VALUE=”WinVista”/&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f3b15-143">&lt;VALEUR du système d’exploitation = «WinVista64»/&gt;</span><span class="sxs-lookup"><span data-stu-id="f3b15-143">&lt;OS VALUE=”WinVista64”/&gt;</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f3b15-144">&lt;VALEUR du système d’exploitation = «WinXP»/&gt;</span><span class="sxs-lookup"><span data-stu-id="f3b15-144">&lt;OS VALUE=”WinXP”/&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f3b15-145">&lt;VALEUR du système d’exploitation = «WinXP64»/&gt;</span><span class="sxs-lookup"><span data-stu-id="f3b15-145">&lt;OS VALUE=”WinXP64”/&gt;</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="f3b15-146">Pour exécuter un package 32, vous devez séquencer l’application sur un ordinateur exécutant un système d’exploitation 32 bits sur lequel est installé le Sequencer App-V 4.6.</span><span class="sxs-lookup"><span data-stu-id="f3b15-146">To run a newly created 32-bit package, you must sequence the application on a computer running a 32-bit operating system with the App-V4.6 Sequencer installed.</span></span> <span data-ttu-id="f3b15-147">Après avoir séquencé l’application, dans la console de Sequencer, sélectionnez l’onglet **déploiement** , puis spécifiez le système d’exploitation et l’architecture de processeur appropriés, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="f3b15-147">After you have sequenced the application, in the Sequencer console, select the **Deployment** tab and then specify the appropriate operating system and chip architecture as required.</span></span>

<span data-ttu-id="f3b15-148">**Important**  Les applications séquencées sur un ordinateur exécutant un système d’exploitation 64 bits doivent être déployées sur des ordinateurs exécutant un système d’exploitation 64 bits.</span><span class="sxs-lookup"><span data-stu-id="f3b15-148">**Important** Applications sequenced on a computer running a 64-bit operating system must be deployed to computers running a 64-bit operating system.</span></span> <span data-ttu-id="f3b15-149">Les nouveaux packages 32 bits créés à l’aide du Sequencer App-V 4.6 ne s’exécuteront pas sur les ordinateurs exécutant le client App-V 4,5.</span><span class="sxs-lookup"><span data-stu-id="f3b15-149">New 32-bit packages created by using the App-V4.6 Sequencer will not run on computers running the App-V 4.5 Client.</span></span>

 

<span data-ttu-id="f3b15-150">Pour exécuter de nouveaux packages 64 bits sur le client App-V 4.6, vous devez séquencer l’application sur un ordinateur exécutant le Sequencer App-V 4.6 et exécutant un système d’exploitation 64 bits.</span><span class="sxs-lookup"><span data-stu-id="f3b15-150">To run new 64-bit packages on the App-V4.6 Client, you must sequence the application on a computer running the App-V4.6 Sequencer and that is running a 64-bit operating system.</span></span> <span data-ttu-id="f3b15-151">Après avoir séquencé l’application, dans la console de Sequencer, sélectionnez l’onglet **déploiement** , puis spécifiez le système d’exploitation et l’architecture de processeur appropriés, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="f3b15-151">After you have sequenced the application, in the Sequencer console, select the **Deployment** tab and then specify the appropriate operating system and chip architecture as required.</span></span>

<span data-ttu-id="f3b15-152">Le tableau suivant répertorie les versions clientes qui exécutent des packages créés à l’aide des différentes versions du Sequencer.</span><span class="sxs-lookup"><span data-stu-id="f3b15-152">The following table lists which client versions will run packages created by using the various versions of the Sequencer.</span></span>

<table style="width:100%;">
<colgroup>
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left"><span data-ttu-id="f3b15-153">Séquence en utilisant le séquenceur App-V 4,2</span><span class="sxs-lookup"><span data-stu-id="f3b15-153">Sequenced by using the App-V 4.2 Sequencer</span></span></th>
<th align="left"><span data-ttu-id="f3b15-154">Séquence en utilisant le séquenceur App-V 4,5</span><span class="sxs-lookup"><span data-stu-id="f3b15-154">Sequenced by using the App-V 4.5 Sequencer</span></span></th>
<th align="left"><span data-ttu-id="f3b15-155">Séquencé en utilisant le Sequencer App-V 4,6 32-bit</span><span class="sxs-lookup"><span data-stu-id="f3b15-155">Sequenced by using the 32-bit App-V 4.6 Sequencer</span></span></th>
<th align="left"><span data-ttu-id="f3b15-156">Séquencé en utilisant le Sequencer App-V 4,6 64-bit</span><span class="sxs-lookup"><span data-stu-id="f3b15-156">Sequenced by using the 64-bit App-V 4.6 Sequencer</span></span></th>
<th align="left"><span data-ttu-id="f3b15-157">Séquence en utilisant le Sequencer App-V 4,6 SP1 d’application 32 bits</span><span class="sxs-lookup"><span data-stu-id="f3b15-157">Sequenced by using the 32-bit App-V 4.6 SP1 Sequencer</span></span></th>
<th align="left"><span data-ttu-id="f3b15-158">Séquence en utilisant le Sequencer App-V 4,6 SP1 d’application 64 bits</span><span class="sxs-lookup"><span data-stu-id="f3b15-158">Sequenced by using the 64-bit App-V 4.6 SP1 Sequencer</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f3b15-159">Client 4,2</span><span class="sxs-lookup"><span data-stu-id="f3b15-159">4.2 Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="f3b15-160">Oui</span><span class="sxs-lookup"><span data-stu-id="f3b15-160">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="f3b15-161">Non</span><span class="sxs-lookup"><span data-stu-id="f3b15-161">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="f3b15-162">Non</span><span class="sxs-lookup"><span data-stu-id="f3b15-162">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="f3b15-163">Non</span><span class="sxs-lookup"><span data-stu-id="f3b15-163">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="f3b15-164">Non</span><span class="sxs-lookup"><span data-stu-id="f3b15-164">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="f3b15-165">Non</span><span class="sxs-lookup"><span data-stu-id="f3b15-165">No</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f3b15-166">4,5 client ¹</span><span class="sxs-lookup"><span data-stu-id="f3b15-166">4.5 Client ¹</span></span></p></td>
<td align="left"><p><span data-ttu-id="f3b15-167">Oui</span><span class="sxs-lookup"><span data-stu-id="f3b15-167">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="f3b15-168">Oui</span><span class="sxs-lookup"><span data-stu-id="f3b15-168">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="f3b15-169">Non</span><span class="sxs-lookup"><span data-stu-id="f3b15-169">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="f3b15-170">Non</span><span class="sxs-lookup"><span data-stu-id="f3b15-170">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="f3b15-171">Non</span><span class="sxs-lookup"><span data-stu-id="f3b15-171">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="f3b15-172">Non</span><span class="sxs-lookup"><span data-stu-id="f3b15-172">No</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f3b15-173">Client 4,6 (32 bits)</span><span class="sxs-lookup"><span data-stu-id="f3b15-173">4.6 Client (32-bit)</span></span></p></td>
<td align="left"><p><span data-ttu-id="f3b15-174">Oui</span><span class="sxs-lookup"><span data-stu-id="f3b15-174">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="f3b15-175">Oui</span><span class="sxs-lookup"><span data-stu-id="f3b15-175">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="f3b15-176">Oui</span><span class="sxs-lookup"><span data-stu-id="f3b15-176">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="f3b15-177">Non</span><span class="sxs-lookup"><span data-stu-id="f3b15-177">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="f3b15-178">Oui</span><span class="sxs-lookup"><span data-stu-id="f3b15-178">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="f3b15-179">Non</span><span class="sxs-lookup"><span data-stu-id="f3b15-179">No</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f3b15-180">Client 4,6 (64 bits)</span><span class="sxs-lookup"><span data-stu-id="f3b15-180">4.6 Client (64-bit)</span></span></p></td>
<td align="left"><p><span data-ttu-id="f3b15-181">Oui</span><span class="sxs-lookup"><span data-stu-id="f3b15-181">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="f3b15-182">Oui</span><span class="sxs-lookup"><span data-stu-id="f3b15-182">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="f3b15-183">Oui</span><span class="sxs-lookup"><span data-stu-id="f3b15-183">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="f3b15-184">Oui</span><span class="sxs-lookup"><span data-stu-id="f3b15-184">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="f3b15-185">Oui</span><span class="sxs-lookup"><span data-stu-id="f3b15-185">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="f3b15-186">Oui</span><span class="sxs-lookup"><span data-stu-id="f3b15-186">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f3b15-187">Client 4,6 SP1</span><span class="sxs-lookup"><span data-stu-id="f3b15-187">4.6 SP1 Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="f3b15-188">Oui</span><span class="sxs-lookup"><span data-stu-id="f3b15-188">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="f3b15-189">Oui</span><span class="sxs-lookup"><span data-stu-id="f3b15-189">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="f3b15-190">Oui</span><span class="sxs-lookup"><span data-stu-id="f3b15-190">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="f3b15-191">Non</span><span class="sxs-lookup"><span data-stu-id="f3b15-191">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="f3b15-192">Oui</span><span class="sxs-lookup"><span data-stu-id="f3b15-192">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="f3b15-193">Non</span><span class="sxs-lookup"><span data-stu-id="f3b15-193">No</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f3b15-194">Client 4,6 SP1 (64 bits)</span><span class="sxs-lookup"><span data-stu-id="f3b15-194">4.6 SP1 Client (64-bit)</span></span></p></td>
<td align="left"><p><span data-ttu-id="f3b15-195">Oui</span><span class="sxs-lookup"><span data-stu-id="f3b15-195">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="f3b15-196">Oui</span><span class="sxs-lookup"><span data-stu-id="f3b15-196">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="f3b15-197">Oui</span><span class="sxs-lookup"><span data-stu-id="f3b15-197">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="f3b15-198">Oui</span><span class="sxs-lookup"><span data-stu-id="f3b15-198">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="f3b15-199">Oui</span><span class="sxs-lookup"><span data-stu-id="f3b15-199">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="f3b15-200">Oui</span><span class="sxs-lookup"><span data-stu-id="f3b15-200">Yes</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="f3b15-201">¹ s’applique à toutes les versions du client App-V 4.5, notamment App-V 4.5, App-V 4.5 CU1 et App-V 4.5 SP1.</span><span class="sxs-lookup"><span data-stu-id="f3b15-201">¹Applies to all versions of the App-V4.5 Client, including App-V4.5, App-V4.5CU1 and App-V4.5 SP1.</span></span>

## <span data-ttu-id="f3b15-202">Autres considérations relatives à la migration</span><span class="sxs-lookup"><span data-stu-id="f3b15-202">Additional Migration Considerations</span></span>


<span data-ttu-id="f3b15-203">L’une des fonctionnalités du Sequencer App-V 4.5 est la possibilité de créer des fichiers Windows Installer (. msi) en tant que points de contrôle pour l’interopérabilité d’un package d’application virtuel avec des systèmes de distribution de logiciels électroniques tels que Microsoft Endpoint Manager.</span><span class="sxs-lookup"><span data-stu-id="f3b15-203">One of the features of the App-V4.5 Sequencer is the ability to create Windows Installer files (.msi) as control points for virtual application package interoperability with electronic software distribution (ESD) systems such as Microsoft Endpoint Configuration Manager.</span></span> <span data-ttu-id="f3b15-204">Les fichiers Windows Installer antérieurs créés à l’aide de l’outil. msi pour la virtualisation d’applications qui ont été installés sur un client App-V 4.1 ou 4.2 qui est ensuite mis à niveau vers la version 4.5 continuent de fonctionner, même s’ils ne peuvent pas être installés sur le client 4.5.</span><span class="sxs-lookup"><span data-stu-id="f3b15-204">Previous Windows Installer files created with the .msi tool for Application Virtualization that were installed on a App-V4.1 or4.2 Client that is subsequently upgraded to4.5 continue to work, although they cannot be installed on the4.5 Client.</span></span> <span data-ttu-id="f3b15-205">Toutefois, ils ne peuvent pas être supprimés ou mis à niveau sauf s’ils sont mis à niveau dans le Sequencer 4.5.</span><span class="sxs-lookup"><span data-stu-id="f3b15-205">However, they cannot be removed or upgraded unless they are upgraded in the4.5 Sequencer.</span></span> <span data-ttu-id="f3b15-206">Le package d’application virtuelle antérieur à 4,5 doit être ouvert dans le Sequencer 4.5, puis enregistré en tant que fichier Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="f3b15-206">The original pre-4.5 virtual application package would need to be opened in the4.5 Sequencer and then saved as a Windows Installer File.</span></span>

<span data-ttu-id="f3b15-207">**Remarques**  Si le client App-V 4.2 a déjà été mis à niveau vers la version 4.5, il est possible d’utiliser un script comme solution de contournement pour conserver les packages 4.2 sur des clients 4.5 et permettre leur gestion.</span><span class="sxs-lookup"><span data-stu-id="f3b15-207">**Note** If the App-V4.2 Client has already been upgraded to4.5, it is possible to use script as a workaround to preserve the4.2 packages on4.5 clients and allow them to be managed.</span></span> <span data-ttu-id="f3b15-208">Ce script doit copier deux fichiers, msvcp71.dll et msvcr71.dll, dans le dossier d’installation de App-V et définir les valeurs de clé de Registre suivantes sous la clé de Registre \ [HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\]:</span><span class="sxs-lookup"><span data-stu-id="f3b15-208">This script must copy two files, msvcp71.dll and msvcr71.dll, to the App-V installation folder and set the following registry key values under the registry key \[HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\]:</span></span>

<span data-ttu-id="f3b15-209">"ClientVersion" = "4.2.1.20"</span><span class="sxs-lookup"><span data-stu-id="f3b15-209">"ClientVersion"="4.2.1.20"</span></span>

<span data-ttu-id="f3b15-210">«GlobalDataDirectory» = «C:\\\\Documents and Settings\\\\All Users\\\\Documents\\\\» (emplacement accessible en écriture dans le monde)</span><span class="sxs-lookup"><span data-stu-id="f3b15-210">"GlobalDataDirectory"="C:\\\\Documents and Settings\\\\All Users\\\\Documents\\\\" (a globally writeable location)</span></span>

 

<span data-ttu-id="f3b15-211">Les fichiers Windows Installer générés par le Sequencer App-V 4,5 affichent le message d’erreur «ce package nécessite le client Microsoft Application Virtualization 4,5 ou une version ultérieure» lorsque vous tentez de les exécuter sur un client App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="f3b15-211">Windows Installer files generated by the App-V 4.5 Sequencer display the error message "This package requires Microsoft Application Virtualization Client 4.5 or later" when you try to run them on an App-V 4.6 Client.</span></span> <span data-ttu-id="f3b15-212">Ouvrez l’ancien package avec le Sequencer App-V 4,5 SP1 ou le Sequencer App-V 4,6 et générez un nouveau fichier. msi pour le package.</span><span class="sxs-lookup"><span data-stu-id="f3b15-212">Open the old package with either the App-V 4.5 SP1 Sequencer or the App-V 4.6 Sequencer and generate a new .msi for the package.</span></span>

<span data-ttu-id="f3b15-213">Tout rapport 4.2 créé et enregistré est écrasé lors de la mise à niveau vers la version 4.5 du serveur.</span><span class="sxs-lookup"><span data-stu-id="f3b15-213">Any4.2 reports that were created and saved will be overwritten when the server is upgraded to4.5.</span></span> <span data-ttu-id="f3b15-214">Si vous avez besoin de conserver ces rapports, vous devez enregistrer une copie de sauvegarde du fichier SftMMC. msc qui se trouve dans le dossier de la console de gestion SoftGrid du serveur et utiliser cette copie pour remplacer le nouveau SftMMC. msc qui est installé lors de la mise à niveau.</span><span class="sxs-lookup"><span data-stu-id="f3b15-214">If you need to keep these reports, you must save a backup copy of the SftMMC.msc file located in the SoftGrid Management Console folder on the server and use that copy to replace the new SftMMC.msc that is installed during the upgrade.</span></span>

<span data-ttu-id="f3b15-215">Pour plus d’informations sur la mise à niveau à partir d’une version antérieure, voir [mise à niveau vers le Forum aux questions sur Microsoft application virtualization 4,5](https://go.microsoft.com/fwlink/?LinkId=120358) ( https://go.microsoft.com/fwlink/?LinkId=120358) .</span><span class="sxs-lookup"><span data-stu-id="f3b15-215">For additional information about upgrading from previous versions, see [Upgrading to Microsoft Application Virtualization 4.5 FAQ](https://go.microsoft.com/fwlink/?LinkId=120358) (https://go.microsoft.com/fwlink/?LinkId=120358).</span></span>

## <span data-ttu-id="f3b15-216">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f3b15-216">Related topics</span></span>


[<span data-ttu-id="f3b15-217">Planification du déploiement du système Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="f3b15-217">Planning for Application Virtualization System Deployment</span></span>](planning-for-application-virtualization-system-deployment.md)

 

 





