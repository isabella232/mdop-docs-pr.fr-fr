---
title: Procédure d'utilisation du fichier Differential SFT
description: Procédure d'utilisation du fichier Differential SFT
author: dansimp
ms.assetid: 607e30fd-2f0e-4e2f-b669-0b3f010aebb0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 85cc45f9665569d77fcf275db6dbc080eb919229
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806686"
---
# <span data-ttu-id="a8178-103">Procédure d'utilisation du fichier Differential SFT</span><span class="sxs-lookup"><span data-stu-id="a8178-103">How to Use the Differential SFT File</span></span>


<span data-ttu-id="a8178-104">Lorsque vous séquençagez une application, le Sequencer Microsoft Application Virtualization (App-V) crée des fichiers SFT (. sft) pour stocker tout le contenu et les informations de configuration de chaque application virtuelle.</span><span class="sxs-lookup"><span data-stu-id="a8178-104">When sequencing an application, the Microsoft Application Virtualization (App-V) Sequencer creates SFT files (.sft) to store all of the virtual application’s files content and configuration information.</span></span> <span data-ttu-id="a8178-105">Dans la version 4.5 de App-V, le fichier SFT SFT (. dsft) a été introduit.</span><span class="sxs-lookup"><span data-stu-id="a8178-105">In version4.5 of App-V, the Differential SFT (.dsft) file has been introduced.</span></span> <span data-ttu-id="a8178-106">Après avoir utilisé le Sequencer pour créer une mise à niveau d’un package existant, vous pouvez choisir de générer ce fichier pour stocker uniquement les différences entre le package d’application séquencé d’origine et la nouvelle version.</span><span class="sxs-lookup"><span data-stu-id="a8178-106">After using the Sequencer to create an upgrade for an existing package, you can choose to generate this file to store only the differences between the original sequenced application package and the new version.</span></span> <span data-ttu-id="a8178-107">C’est donc beaucoup plus petit que le fichier SFT complet serait destiné à la nouvelle version de l’application et réduit l’impact de la mise à jour des mises à jour de package sur une connexion réseau à faible bande passante.</span><span class="sxs-lookup"><span data-stu-id="a8178-107">It is therefore much smaller than the full SFT file would be for the new version of the application and reduces the impact of sending package updates over low-bandwidth network connections.</span></span> <span data-ttu-id="a8178-108">Toutefois, son utilisation est uniquement prise en charge dans certaines situations restreintes.</span><span class="sxs-lookup"><span data-stu-id="a8178-108">However, its use is supported only in certain restricted situations.</span></span> <span data-ttu-id="a8178-109">Cette fonctionnalité était conçue pour une utilisation spécifique lorsque vous utilisez un système de distribution de logiciels électroniques pour gérer un groupe d’utilisateurs à l’aide d’un serveur de fichiers local par le biais d’une connexion à faible bande passante et que vous n’utilisez pas les serveurs de streaming App-V.</span><span class="sxs-lookup"><span data-stu-id="a8178-109">This feature was intended to be used specifically where you are using an electronic software distribution (ESD) system to manage a group of users with a local file server over a low-bandwidth connection and you are not using App-V streaming servers.</span></span>

<span data-ttu-id="a8178-110">Vous n’avez pas besoin d’utiliser le fichier SFT différentielle si vous utilisez la configuration Manager2007 pour gérer les utilisateurs, car Configuration Manager prend en charge les déploiements à faible bande passante déjà intégrés.</span><span class="sxs-lookup"><span data-stu-id="a8178-110">You do not need to use the Differential SFT file if you are using Configuration Manager2007 to manage the users, because Configuration Manager has support for low-bandwidth deployments already built in.</span></span> <span data-ttu-id="a8178-111">Ce n’est pas non plus obligatoire si vous utilisez la gestion des applications (App-V) ou les serveurs de streaming avec la mise à niveau active, car le client récupère uniquement les différences entre les anciennes et les nouvelles versions de package.</span><span class="sxs-lookup"><span data-stu-id="a8178-111">It is also not required if you are using Application Virtualization (App-V) Management or Streaming Servers with Active Upgrade because the client will retrieve only the differences between the old and new package versions.</span></span>

<span data-ttu-id="a8178-112">La procédure suivante vous explique comment utiliser la mkdiffpkg.exe incluse dans l’installation de Sequencer pour créer le fichier SFT différentielle, après avoir effectué la mise à niveau du package d’application virtuelle et déployé le fichier SFT différentielle.</span><span class="sxs-lookup"><span data-stu-id="a8178-112">The following procedure shows how to use the mkdiffpkg.exe that is included in the Sequencer installation to create the Differential SFT file, after completing the upgrade of the virtual application package, and to deploy the Differential SFT file.</span></span> <span data-ttu-id="a8178-113">Cette procédure permet de s’assurer que si le package est d’une grande utilisation de l’ordinateur client, lors de la prochaine tentative d’exécution de l’application par l’utilisateur, le client revient à l’URL de remplacement, qui est définie pour diffuser en continu la version complète du package v2. SFT du partage de fichiers local.</span><span class="sxs-lookup"><span data-stu-id="a8178-113">Completing this procedure helps ensure that if the package is somehow unloaded from the client computer, the next time the user tries to run the application, the client will fall back to the override URL, which is set to stream the full package V2.sft from the local file share.</span></span> <span data-ttu-id="a8178-114">Cela évite tout échec de l’utilisateur au démarrage de l’application.</span><span class="sxs-lookup"><span data-stu-id="a8178-114">This will avoid any failure for the user when starting the application.</span></span> <span data-ttu-id="a8178-115">Si le client entier est endommagé ou a été désinstallé, il est recommandé de configurer le système ESD pour déployer la version complète du package mis à niveau, v2. SFT, sur le client.</span><span class="sxs-lookup"><span data-stu-id="a8178-115">If the entire client becomes corrupted or is uninstalled, it is recommended that the ESD system be configured to deploy the full version of the upgraded package, V2.sft, to the client.</span></span>

<span data-ttu-id="a8178-116">Pour plus d’informations sur la mise à niveau d’un package, voir la section «Comment mettre à niveau une application virtuelle existante» dans le guide des opérations App-V 4.5 à</span><span class="sxs-lookup"><span data-stu-id="a8178-116">For more information about upgrading a package, see “How to Upgrade an Existing Virtual Application” in the App-V4.5 Operations Guide at</span></span> <https://go.microsoft.com/fwlink/?LinkId=133129>

<span data-ttu-id="a8178-117">**Remarques**  Le cas échéant, tous les ordinateurs utilisateur ciblés par la fonction ESD doivent disposer du fichier v1. SFT dans leur cache local, et le flux de fichiers doit être activé sur tous les ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="a8178-117">**Note** As a prerequisite, all user computers being targeted by the ESD must have the V1.sft file fully loaded into their local cache, and file streaming must be enabled on all computers.</span></span>

 

**<span data-ttu-id="a8178-118">Pour utiliser le fichier SFT différentielle</span><span class="sxs-lookup"><span data-stu-id="a8178-118">To use the Differential SFT file</span></span>**

1.  <span data-ttu-id="a8178-119">Connectez-vous à l’ordinateur Sequencer à l’aide d’un compte disposant de droits d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="a8178-119">Log on to the Sequencer computer by using an account with administrator rights.</span></span> <span data-ttu-id="a8178-120">Ouvrez le package d’origine (v1) pour la mise à niveau dans le Sequencer, puis mettez à niveau le package vers la nouvelle version (v2) et enregistrez-le en tant que nouveau v2. sft.</span><span class="sxs-lookup"><span data-stu-id="a8178-120">Open the original package (V1) for upgrade in the Sequencer, and then upgrade the package to the new version (V2) and save it as a new V2.sft.</span></span>

2.  <span data-ttu-id="a8178-121">Ouvrez une fenêtre de commande dans le dossier d’installation du Sequencer App-V 4.5, puis exécutez la commande suivante:</span><span class="sxs-lookup"><span data-stu-id="a8178-121">Open a command window in the App-V4.5 Sequencer installation folder, and run the following command:</span></span>

    `“mkdiffpkg.exe V2.sft V2.dsft”`

3.  <span data-ttu-id="a8178-122">À l’aide du système ESD ou d’un autre processus de copie de fichiers, copiez le fichier de contenu de package V2 complet, v2. SFT, sur un partage de fichiers local accessible aux ordinateurs des utilisateurs sur une connexion réseau bien connectée.</span><span class="sxs-lookup"><span data-stu-id="a8178-122">Using the ESD system or other file copy process, copy the full V2 package content file, V2.sft, to a local file share that is accessible to the user computers on a well-connected network connection.</span></span>

4.  <span data-ttu-id="a8178-123">À l’aide du système ESD, placez une copie du fichier SFT différentielle, v2. dsft, sur chaque ordinateur d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a8178-123">Using the ESD system, place a copy of the Differential SFT file, V2.dsft, on each user computer.</span></span>

5.  <span data-ttu-id="a8178-124">Pour importer le fichier v2. dsft, exécutez la commande SFTMIME suivante sur les ordinateurs des utilisateurs:</span><span class="sxs-lookup"><span data-stu-id="a8178-124">To import the V2.dsft file, run the following SFTMIME command on each user computer:</span></span>

    `“SFTMIME load package:<package name> /SFTPATH <path to V2.dsft>”`

6.  <span data-ttu-id="a8178-125">Exécutez la commande SFTMIME suivante sur les ordinateurs des utilisateurs pour définir l’URL de remplacement de telle sorte qu’elle pointe vers le fichier v2. sft:</span><span class="sxs-lookup"><span data-stu-id="a8178-125">Run the following SFTMIME command on each user computer to set the override URL to point to the V2.sft file:</span></span>

    `“SFTMIME configure package:<package name> /OverrideURL FILE://<network path to V2.sft>”`

**<span data-ttu-id="a8178-126">Remarque</span><span class="sxs-lookup"><span data-stu-id="a8178-126">Note</span></span>**  
-   <span data-ttu-id="a8178-127">Les fichiers SFT différentielle doivent être appliqués aux clients dans l’ordre approprié.</span><span class="sxs-lookup"><span data-stu-id="a8178-127">Differential SFT files must be applied to clients in the correct order.</span></span> <span data-ttu-id="a8178-128">Par exemple, la version v2. dsft doit être appliquée à une application v1 avant la version v3. dsft est appliquée.</span><span class="sxs-lookup"><span data-stu-id="a8178-128">For example, V2.dsft must be applied to a V1 application before V3.dsft is applied.</span></span>

-   <span data-ttu-id="a8178-129">La fonctionnalité **générer le package Microsoft Windows Installer (MSI)** du Sequencer ne peut pas être utilisée avec le fichier SFT différentielle.</span><span class="sxs-lookup"><span data-stu-id="a8178-129">The **Generate Microsoft Windows Installer (MSI) Package** capability in the Sequencer cannot be used with the Differential SFT file.</span></span>

 

## <span data-ttu-id="a8178-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a8178-130">Related topics</span></span>


[<span data-ttu-id="a8178-131">Comment créer ou mettre à niveau des applications virtuelles à l’aide du Sequencer App-V</span><span class="sxs-lookup"><span data-stu-id="a8178-131">How to Create or Upgrade Virtual Applications Using the App-V Sequencer</span></span>](how-to-create-or-upgrade-virtual-applications-using--the-app-v-sequencer.md)

 

 





