---
title: Liste de contrôle pour la mise à niveau d'App-V
description: Liste de contrôle pour la mise à niveau d'App-V
author: dansimp
ms.assetid: 64e317d2-d260-4b67-8a49-ba9ac513087a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ad856ce3067c327f3e604f9269ee384a66a1675a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808026"
---
# <span data-ttu-id="7df9d-103">Liste de contrôle pour la mise à niveau d'App-V</span><span class="sxs-lookup"><span data-stu-id="7df9d-103">App-V Upgrade Checklist</span></span>


<span data-ttu-id="7df9d-104">Avant d’essayer de procéder à la mise à niveau vers la version 4,5 ou ultérieure de Microsoft Application Virtualization, toute version antérieure à l’application-V 4,1 doit être mise à niveau vers App-V 4,1.</span><span class="sxs-lookup"><span data-stu-id="7df9d-104">Before trying to upgrade to Microsoft Application Virtualization (App-V) 4.5 or later versions, any version earlier than App-V 4.1 must be upgraded to App-V 4.1.</span></span> <span data-ttu-id="7df9d-105">Envisagez d’abord de mettre à jour les clients, puis de mettre à niveau les composants serveur.</span><span class="sxs-lookup"><span data-stu-id="7df9d-105">You should plan to upgrade clients first, and then upgrade the server components.</span></span> <span data-ttu-id="7df9d-106">Les clients App-V qui ont été mis à niveau vers App-v 4,5 continuent de fonctionner avec des serveurs App-V qui n’ont pas encore été mis à niveau.</span><span class="sxs-lookup"><span data-stu-id="7df9d-106">App-V clients that have been upgraded to App-V 4.5 continue to work with App-V servers that have not yet been upgraded.</span></span> <span data-ttu-id="7df9d-107">Les versions antérieures du client ne sont pas prises en charge sur les serveurs qui ont été mis à niveau vers App-V 4,5.</span><span class="sxs-lookup"><span data-stu-id="7df9d-107">Earlier versions of the client are not supported on servers that have been upgraded to App-V 4.5.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7df9d-108">Étape</span><span class="sxs-lookup"><span data-stu-id="7df9d-108">Step</span></span></th>
<th align="left"><span data-ttu-id="7df9d-109">Référence</span><span class="sxs-lookup"><span data-stu-id="7df9d-109">Reference</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7df9d-110">Mettez à niveau les clients App-V.</span><span class="sxs-lookup"><span data-stu-id="7df9d-110">Upgrade the App-V clients.</span></span></p></td>
<td align="left"><p><a href="how-to-upgrade-the-application-virtualization-client.md" data-raw-source="[How to Upgrade the Application Virtualization Client](how-to-upgrade-the-application-virtualization-client.md)"><span data-ttu-id="7df9d-111">Procédure pour mettre à niveau Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="7df9d-111">How to Upgrade the Application Virtualization Client</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7df9d-112">Mettez à niveau la base de données et les serveurs App-V.</span><span class="sxs-lookup"><span data-stu-id="7df9d-112">Upgrade the App-V servers and database.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="7df9d-113">Important</span><span class="sxs-lookup"><span data-stu-id="7df9d-113">Important</span></span></strong><br/><p><span data-ttu-id="7df9d-114">Si vous disposez de plusieurs serveurs de partage d’accès à la base de données App-V, tous les serveurs doivent être déconnectés pendant la mise à niveau de la base de données.</span><span class="sxs-lookup"><span data-stu-id="7df9d-114">If you have more than one server sharing access to the App-V database, all those servers must be taken offline while the database is being upgraded.</span></span> <span data-ttu-id="7df9d-115">Vous devez suivre les pratiques d’entreprise standard pour la mise à niveau de la base de données, mais nous vous recommandons de tester la mise à niveau de la base de données en utilisant d’abord une copie de sauvegarde de la base de données sur un serveur de test.</span><span class="sxs-lookup"><span data-stu-id="7df9d-115">You should follow your regular business practices for the database upgrade, but we recommend that you test the database upgrade by using a backup copy of the database first on a test server.</span></span> <span data-ttu-id="7df9d-116">Ensuite, vous devez sélectionner l’un des serveurs pour la première mise à niveau, qui mettra à niveau le schéma de la base de données.</span><span class="sxs-lookup"><span data-stu-id="7df9d-116">Then, you should select one of the servers for the first upgrade, which will upgrade the database schema.</span></span> <span data-ttu-id="7df9d-117">Après la mise à niveau de la base de données de production, vous pouvez mettre à niveau le logiciel App-V sur les autres serveurs.</span><span class="sxs-lookup"><span data-stu-id="7df9d-117">After the production database has been successfully upgraded, you can upgrade the App-V software on the other servers.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><a href="how-to-upgrade-the-servers-and-system-components.md" data-raw-source="[How to Upgrade the Servers and System Components](how-to-upgrade-the-servers-and-system-components.md)"><span data-ttu-id="7df9d-118">Procédure pour mettre à niveau les serveurs et les composants système</span><span class="sxs-lookup"><span data-stu-id="7df9d-118">How to Upgrade the Servers and System Components</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7df9d-119">Mettez à niveau le service Web de gestion des applications-V.</span><span class="sxs-lookup"><span data-stu-id="7df9d-119">Upgrade the App-V Management Web Service.</span></span></p>
<p><span data-ttu-id="7df9d-120">Cette étape s’applique uniquement si le service Web de gestion se trouve sur un serveur distinct, ce qui vous oblige à exécuter le programme d’installation du serveur sur ce serveur distinct pour mettre à niveau le service Web de gestion.</span><span class="sxs-lookup"><span data-stu-id="7df9d-120">This step applies only if the Management Web Service is on a separate server, which would require that you run the server installer program on that separate server to upgrade the Management Web service.</span></span> <span data-ttu-id="7df9d-121">Dans le cas contraire, l’étape de mise à niveau précédente du serveur met automatiquement à niveau le service Web de gestion.</span><span class="sxs-lookup"><span data-stu-id="7df9d-121">Otherwise, the previous server upgrade step will automatically upgrade the Management Web Service.</span></span></p></td>
<td align="left"><p><a href="how-to-upgrade-the-servers-and-system-components.md" data-raw-source="[How to Upgrade the Servers and System Components](how-to-upgrade-the-servers-and-system-components.md)"><span data-ttu-id="7df9d-122">Procédure pour mettre à niveau les serveurs et les composants système</span><span class="sxs-lookup"><span data-stu-id="7df9d-122">How to Upgrade the Servers and System Components</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7df9d-123">Mettez à niveau la console de gestion des applications.</span><span class="sxs-lookup"><span data-stu-id="7df9d-123">Upgrade the App-V Management Console.</span></span></p>
<p><span data-ttu-id="7df9d-124">Cette étape s’applique uniquement si la console de gestion se trouve sur un autre ordinateur, ce qui vous oblige à exécuter le programme d’installation du serveur sur cet ordinateur distinct pour mettre à niveau la console.</span><span class="sxs-lookup"><span data-stu-id="7df9d-124">This step applies only if the Management Console is on a separate computer, which would require that you run the server installer program on that separate computer to upgrade the console.</span></span> <span data-ttu-id="7df9d-125">Dans le cas contraire, l’étape de mise à niveau précédente du serveur met à niveau la console de gestion.</span><span class="sxs-lookup"><span data-stu-id="7df9d-125">Otherwise, the previous server upgrade step will upgrade the Management Console.</span></span></p></td>
<td align="left"><p><a href="how-to-upgrade-the-servers-and-system-components.md" data-raw-source="[How to Upgrade the Servers and System Components](how-to-upgrade-the-servers-and-system-components.md)"><span data-ttu-id="7df9d-126">Procédure pour mettre à niveau les serveurs et les composants système</span><span class="sxs-lookup"><span data-stu-id="7df9d-126">How to Upgrade the Servers and System Components</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7df9d-127">Mettez à niveau le Sequencer App-V.</span><span class="sxs-lookup"><span data-stu-id="7df9d-127">Upgrade the App-V Sequencer.</span></span></p></td>
<td align="left"><p><a href="how-to-upgrade-the-application-virtualization-sequencer.md" data-raw-source="[How to Upgrade the Application Virtualization Sequencer](how-to-upgrade-the-application-virtualization-sequencer.md)"><span data-ttu-id="7df9d-128">Procédure pour mettre à niveau Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="7df9d-128">How to Upgrade the Application Virtualization Sequencer</span></span></a></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="7df9d-129">Autres considérations en matière de mise à niveau</span><span class="sxs-lookup"><span data-stu-id="7df9d-129">Additional Upgrade Considerations</span></span>


-   <span data-ttu-id="7df9d-130">Tout package d’application virtuelle séquencé dans la version 4,2 ne doit pas être séquencé pour une utilisation avec la version 4,5.</span><span class="sxs-lookup"><span data-stu-id="7df9d-130">Any virtual application packages sequenced in version 4.2 will not have to be sequenced again for use with version 4.5.</span></span> <span data-ttu-id="7df9d-131">Toutefois, vous devez envisager de mettre à niveau les packages virtuels vers le format Microsoft Application Virtualization 4,5 Si vous souhaitez appliquer des listes de contrôle d’accès par défaut ou générer un fichier d’installation Windows.</span><span class="sxs-lookup"><span data-stu-id="7df9d-131">However, you should consider upgrading the virtual packages to the Microsoft Application Virtualization 4.5 format if you want to apply default access control lists (ACLs) or generate a Windows Installer file.</span></span> <span data-ttu-id="7df9d-132">Il s’agit d’un processus simple qui nécessite uniquement l’ouverture et l’enregistrement du package d’application virtuel existant avec le Sequencer App-V 4,5.</span><span class="sxs-lookup"><span data-stu-id="7df9d-132">This is a simple process and requires only that the existing virtual application package be opened and saved with the App-V 4.5 Sequencer.</span></span> <span data-ttu-id="7df9d-133">Cela peut être automatisé à l’aide de l’interface de ligne de commande App-VSequencer.</span><span class="sxs-lookup"><span data-stu-id="7df9d-133">This can be automated by using the App-VSequencer command-line interface.</span></span> <span data-ttu-id="7df9d-134">Pour plus d’informations, reportez-vous [à création ou mise à niveau d’applications virtuelles à l’aide du Sequencer App-V](how-to-create-or-upgrade-virtual-applications-using--the-app-v-sequencer.md)</span><span class="sxs-lookup"><span data-stu-id="7df9d-134">For more information, see [How to Create or Upgrade Virtual Applications Using the App-V Sequencer](how-to-create-or-upgrade-virtual-applications-using--the-app-v-sequencer.md)</span></span>

-   <span data-ttu-id="7df9d-135">L’une des fonctionnalités du Sequencer 4,5 est la possibilité de créer des fichiers Windows Installer (. msi) en tant que points de contrôle pour l’interopérabilité d’un package d’application virtuel avec des systèmes de distribution de logiciels électroniques, tels que Microsoft Endpoint Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="7df9d-135">One of the features of the 4.5 Sequencer is the ability to create Windows Installer (.msi) files as control points for virtual application package interoperability with electronic software distribution (ESD) systems, such as Microsoft Endpoint Configuration Manager.</span></span> <span data-ttu-id="7df9d-136">Les fichiers Windows Installer antérieurs créés à l’aide de l’outil MSI pour la virtualisation de l’application qui étaient installés sur un client App-V 4,1 ou 4,2 qui est ensuite mis à niveau vers App-V 4,5 continuent de fonctionner, même s’ils ne peuvent pas être installés sur le client App-V 4,5.</span><span class="sxs-lookup"><span data-stu-id="7df9d-136">Previous Windows Installer files created with the MSI tool for Application Virtualization that were installed on a App-V 4.1 or 4.2 client that is subsequently upgraded to App-V 4.5 will continue to work, although they cannot be installed on the App-V 4.5 client.</span></span> <span data-ttu-id="7df9d-137">Toutefois, ils ne peuvent pas être supprimés ou mis à niveau sauf s’ils sont mis à niveau dans le Sequencer App-V 4,5.</span><span class="sxs-lookup"><span data-stu-id="7df9d-137">However, they cannot be removed or upgraded unless they are upgraded in the App-V 4.5 Sequencer.</span></span> <span data-ttu-id="7df9d-138">Le package App-V d’origine antérieur à 4,5 doit être ouvert dans le Sequencer App-V 4,5, puis enregistré en tant que fichier Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="7df9d-138">The original App-V package earlier than 4.5 has to be opened in the App-V 4.5 Sequencer and then saved as a Windows Installer File.</span></span>

    **<span data-ttu-id="7df9d-139">Remarque</span><span class="sxs-lookup"><span data-stu-id="7df9d-139">Note</span></span>**  
    <span data-ttu-id="7df9d-140">Si le client App-V 4,2 a déjà fait l’objet d’une mise à niveau vers App-V 4,5, il est possible de créer une solution de contournement pour conserver les packages de la version 4,2 sur les clients de la version 4,5 et permettre leur gestion.</span><span class="sxs-lookup"><span data-stu-id="7df9d-140">If the App-V 4.2 Client has already been upgraded to App-V 4.5, it is possible to script a workaround to preserve the version 4.2 packages on version 4.5 clients and allow them to be managed.</span></span> <span data-ttu-id="7df9d-141">Ce script doit copier deux fichiers, msvcp71.dll et msvcr71.dll, dans le dossier d’installation de App-V et définir les valeurs de clé de Registre suivantes sous la clé de Registre: \ [HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\]:</span><span class="sxs-lookup"><span data-stu-id="7df9d-141">This script must copy two files, msvcp71.dll and msvcr71.dll, to the App-V installation folder and set the following registry key values under the registry key:\[HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\]:</span></span>

    <span data-ttu-id="7df9d-142">"ClientVersion" = "4.2.1.20"</span><span class="sxs-lookup"><span data-stu-id="7df9d-142">"ClientVersion"="4.2.1.20"</span></span>

    <span data-ttu-id="7df9d-143">«GlobalDataDirectory» = «C:\\\\Documents and Settings\\\\All Users\\\\Documents\\\\» (emplacement accessible en écriture dans le monde)</span><span class="sxs-lookup"><span data-stu-id="7df9d-143">"GlobalDataDirectory"="C:\\\\Documents and Settings\\\\All Users\\\\Documents\\\\" (a globally writeable location)</span></span>



-   <span data-ttu-id="7df9d-144">Les fichiers Windows Installer générés par le Sequencer App-V 4,5 affichent le message d’erreur «ce package nécessite le client Microsoft Application Virtualization 4,5 ou une version ultérieure» lorsque vous tentez de les exécuter sur un client App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="7df9d-144">Windows Installer files generated by the App-V 4.5 Sequencer display the error message "This package requires Microsoft Application Virtualization Client 4.5 or later" when trying to run them on an App-V 4.6 Client.</span></span> <span data-ttu-id="7df9d-145">Ouvrez l’ancien package avec le Sequencer App-V 4,5 SP1 ou le Sequencer App-V 4,6 et générez un nouveau fichier. msi pour le package.</span><span class="sxs-lookup"><span data-stu-id="7df9d-145">Open the old package with either the App-V 4.5 SP1 Sequencer or the App-V 4.6 Sequencer and generate a new .msi file for the package.</span></span>

-   <span data-ttu-id="7df9d-146">Tout rapport de version 4,2 créé et enregistré sera écrasé lorsque le serveur sera mis à niveau vers la version 4,5.</span><span class="sxs-lookup"><span data-stu-id="7df9d-146">Any version 4.2 reports that were created and saved will be overwritten when the server is upgraded to version 4.5.</span></span> <span data-ttu-id="7df9d-147">Si vous devez conserver ces rapports, vous devez enregistrer une copie de sauvegarde du fichier SftMMC. msc qui se trouve dans le dossier de la console de gestion SoftGrid du serveur et utiliser cette copie pour remplacer le nouveau SftMMC. msc qui est installé lors de la mise à niveau.</span><span class="sxs-lookup"><span data-stu-id="7df9d-147">If you have to keep these reports, you must save a backup copy of the SftMMC.msc file located in the SoftGrid Management Console folder on the server and use that copy to replace the new SftMMC.msc that is installed during the upgrade.</span></span>

-   <span data-ttu-id="7df9d-148">Pour plus d’informations sur la mise à niveau à partir d’une version antérieure, voir [mise à niveau vers le Forum aux questions sur Microsoft application virtualization 4,5](https://go.microsoft.com/fwlink/?LinkId=120358) ( https://go.microsoft.com/fwlink/?LinkId=120358) .</span><span class="sxs-lookup"><span data-stu-id="7df9d-148">For additional information about upgrading from previous versions, see [Upgrading to Microsoft Application Virtualization 4.5 FAQ](https://go.microsoft.com/fwlink/?LinkId=120358) (https://go.microsoft.com/fwlink/?LinkId=120358).</span></span>

## <a href="" id="app-v-4-6-client-package-support-"></a><span data-ttu-id="7df9d-149">Prise en charge de package client App-V 4,6</span><span class="sxs-lookup"><span data-stu-id="7df9d-149">App-V 4.6 Client Package Support</span></span>


<span data-ttu-id="7df9d-150">Vous pouvez déployer des packages créés dans des versions antérieures de App-V pour les clients 4,6 App-V.</span><span class="sxs-lookup"><span data-stu-id="7df9d-150">You can deploy packages created in previous versions of App-V to App-V 4.6 clients.</span></span> <span data-ttu-id="7df9d-151">Toutefois, vous devez modifier le fichier. OSD associé de manière à inclure les informations appropriées sur le système d’exploitation et l’architecture du processeur.</span><span class="sxs-lookup"><span data-stu-id="7df9d-151">However, you must modify the associated .osd file so that it includes the appropriate operating system and chip architecture information.</span></span> <span data-ttu-id="7df9d-152">Vous pouvez utiliser les valeurs suivantes:</span><span class="sxs-lookup"><span data-stu-id="7df9d-152">The following values can be used:</span></span>

<table>
<colgroup>
<col width="100%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7df9d-153">Valeur du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="7df9d-153">OS Value</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7df9d-154">&lt;VALEUR du système d’exploitation = «Win2003TS»/&gt;</span><span class="sxs-lookup"><span data-stu-id="7df9d-154">&lt;OS VALUE=”Win2003TS”/&gt;</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7df9d-155">&lt;VALEUR du système d’exploitation = «Win2003TS64»/&gt;</span><span class="sxs-lookup"><span data-stu-id="7df9d-155">&lt;OS VALUE=”Win2003TS64”/&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7df9d-156">&lt;VALEUR du système d’exploitation = «Win2008TS»/&gt;</span><span class="sxs-lookup"><span data-stu-id="7df9d-156">&lt;OS VALUE=”Win2008TS”/&gt;</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7df9d-157">&lt;VALEUR du système d’exploitation = «Win2008TS64»/&gt;</span><span class="sxs-lookup"><span data-stu-id="7df9d-157">&lt;OS VALUE=”Win2008TS64”/&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7df9d-158">&lt;VALEUR du système d’exploitation = «Win2008R2TS64»/&gt;</span><span class="sxs-lookup"><span data-stu-id="7df9d-158">&lt;OS VALUE=”Win2008R2TS64”/&gt;</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7df9d-159">&lt;VALEUR du système d’exploitation = «Win7»/&gt;</span><span class="sxs-lookup"><span data-stu-id="7df9d-159">&lt;OS VALUE=”Win7”/&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7df9d-160">&lt;VALEUR du système d’exploitation = «Win764»/&gt;</span><span class="sxs-lookup"><span data-stu-id="7df9d-160">&lt;OS VALUE=”Win764”/&gt;</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7df9d-161">&lt;VALEUR du système d’exploitation = «WinVista»/&gt;</span><span class="sxs-lookup"><span data-stu-id="7df9d-161">&lt;OS VALUE=”WinVista”/&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7df9d-162">&lt;VALEUR du système d’exploitation = «WinVista64»/&gt;</span><span class="sxs-lookup"><span data-stu-id="7df9d-162">&lt;OS VALUE=”WinVista64”/&gt;</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7df9d-163">&lt;VALEUR du système d’exploitation = «WinXP»/&gt;</span><span class="sxs-lookup"><span data-stu-id="7df9d-163">&lt;OS VALUE=”WinXP”/&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7df9d-164">&lt;VALEUR du système d’exploitation = «WinXP64»/&gt;</span><span class="sxs-lookup"><span data-stu-id="7df9d-164">&lt;OS VALUE=”WinXP64”/&gt;</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="7df9d-165">Pour exécuter un package 32, vous devez séquencer l’application sur un ordinateur exécutant un système d’exploitation 32 bits sur lequel est installé le Sequencer App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="7df9d-165">To run a newly created 32-bit package, you must sequence the application on a computer running a 32-bit operating system with the App-V 4.6 Sequencer installed.</span></span> <span data-ttu-id="7df9d-166">Après avoir séquencé l’application, dans la console de Sequencer, cliquez sur l’onglet **déploiement** , puis spécifiez le système d’exploitation et l’architecture de processeur appropriés, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="7df9d-166">After you have sequenced the application, in the Sequencer console, click the **Deployment** tab and then specify the appropriate operating system and chip architecture as required.</span></span>

**<span data-ttu-id="7df9d-167">Important</span><span class="sxs-lookup"><span data-stu-id="7df9d-167">Important</span></span>**  
<span data-ttu-id="7df9d-168">Les applications séquencées sur un ordinateur exécutant un système d’exploitation 64 bits doivent être déployées sur des ordinateurs exécutant un système d’exploitation 64 bits.</span><span class="sxs-lookup"><span data-stu-id="7df9d-168">Applications sequenced on a computer running a 64-bit operating system must be deployed to computers running a 64-bit operating system.</span></span> <span data-ttu-id="7df9d-169">Les nouveaux packages 32 bits créés à l’aide du Sequencer App-V 4,6 ne s’exécutent pas sur les ordinateurs exécutant le client App-V 4,5.</span><span class="sxs-lookup"><span data-stu-id="7df9d-169">New 32-bit packages created by using the App-V 4.6 Sequencer do not run on computers running the App-V 4.5 client.</span></span>



<span data-ttu-id="7df9d-170">Pour exécuter de nouveaux packages 64 bits sur le client App-V 4,6, vous devez séquencer l’application sur un ordinateur exécutant le Sequencer App-V 4,6 et exécutant un système d’exploitation 64 bits.</span><span class="sxs-lookup"><span data-stu-id="7df9d-170">To run new 64-bit packages on the App-V 4.6 Client, you must sequence the application on a computer running the App-V 4.6 Sequencer and that is running a 64-bit operating system.</span></span> <span data-ttu-id="7df9d-171">Après avoir séquencé l’application, dans la console de Sequencer, cliquez sur l’onglet **déploiement** , puis spécifiez le système d’exploitation et l’architecture de processeur appropriés, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="7df9d-171">After you have sequenced the application, in the Sequencer console, click the **Deployment** tab, and then specify the appropriate operating system and chip architecture as required.</span></span>

<span data-ttu-id="7df9d-172">Le tableau suivant répertorie les versions clientes qui exécutent des packages créés à l’aide des différentes versions du Sequencer.</span><span class="sxs-lookup"><span data-stu-id="7df9d-172">The following table lists which client versions will run packages created by using the various versions of the sequencer.</span></span>

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left"><span data-ttu-id="7df9d-173">Séquence en utilisant le séquenceur App-V 4,2</span><span class="sxs-lookup"><span data-stu-id="7df9d-173">Sequenced by using the App-V 4.2 Sequencer</span></span></th>
<th align="left"><span data-ttu-id="7df9d-174">Séquence en utilisant le séquenceur App-V 4,5</span><span class="sxs-lookup"><span data-stu-id="7df9d-174">Sequenced by using the App-V 4.5 Sequencer</span></span></th>
<th align="left"><span data-ttu-id="7df9d-175">Séquencé en utilisant le Sequencer App-V 4,6 32-bit</span><span class="sxs-lookup"><span data-stu-id="7df9d-175">Sequenced by using the 32-bit App-V 4.6 Sequencer</span></span></th>
<th align="left"><span data-ttu-id="7df9d-176">Séquencé en utilisant le Sequencer App-V 4,6 64-bit</span><span class="sxs-lookup"><span data-stu-id="7df9d-176">Sequenced by using the 64-bit App-V 4.6 Sequencer</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7df9d-177">Client 4,2</span><span class="sxs-lookup"><span data-stu-id="7df9d-177">4.2 Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="7df9d-178">Oui</span><span class="sxs-lookup"><span data-stu-id="7df9d-178">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="7df9d-179">Non</span><span class="sxs-lookup"><span data-stu-id="7df9d-179">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="7df9d-180">Non</span><span class="sxs-lookup"><span data-stu-id="7df9d-180">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="7df9d-181">Non</span><span class="sxs-lookup"><span data-stu-id="7df9d-181">No</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7df9d-182">4,5 client ¹</span><span class="sxs-lookup"><span data-stu-id="7df9d-182">4.5 Client ¹</span></span></p></td>
<td align="left"><p><span data-ttu-id="7df9d-183">Oui</span><span class="sxs-lookup"><span data-stu-id="7df9d-183">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="7df9d-184">Oui</span><span class="sxs-lookup"><span data-stu-id="7df9d-184">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="7df9d-185">Non</span><span class="sxs-lookup"><span data-stu-id="7df9d-185">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="7df9d-186">Non</span><span class="sxs-lookup"><span data-stu-id="7df9d-186">No</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7df9d-187">Client 4,6 (32 bits)</span><span class="sxs-lookup"><span data-stu-id="7df9d-187">4.6 Client (32-bit)</span></span></p></td>
<td align="left"><p><span data-ttu-id="7df9d-188">Oui</span><span class="sxs-lookup"><span data-stu-id="7df9d-188">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="7df9d-189">Oui</span><span class="sxs-lookup"><span data-stu-id="7df9d-189">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="7df9d-190">Oui</span><span class="sxs-lookup"><span data-stu-id="7df9d-190">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="7df9d-191">Non</span><span class="sxs-lookup"><span data-stu-id="7df9d-191">No</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7df9d-192">Client 4,6 (64 bits)</span><span class="sxs-lookup"><span data-stu-id="7df9d-192">4.6 Client (64-bit)</span></span></p></td>
<td align="left"><p><span data-ttu-id="7df9d-193">Oui</span><span class="sxs-lookup"><span data-stu-id="7df9d-193">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="7df9d-194">Oui</span><span class="sxs-lookup"><span data-stu-id="7df9d-194">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="7df9d-195">Oui</span><span class="sxs-lookup"><span data-stu-id="7df9d-195">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="7df9d-196">Oui</span><span class="sxs-lookup"><span data-stu-id="7df9d-196">Yes</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="7df9d-197">¹ s’applique à toutes les versions du client App-V 4,5, notamment App-V 4,5, App-V 4,5 CU1 et App-V 4,5 SP1.</span><span class="sxs-lookup"><span data-stu-id="7df9d-197">¹Applies to all versions of the App-V 4.5 client, including App-V 4.5, App-V 4.5 CU1, and App-V 4.5 SP1.</span></span>









