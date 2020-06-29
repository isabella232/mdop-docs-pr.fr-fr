---
title: Onglet général des propriétés de virtualisation des applications
description: Onglet général des propriétés de virtualisation des applications
author: dansimp
ms.assetid: be7449d9-171a-4a11-9382-83b7008ccbdd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6ee00bfc7f70ee7b17da42aad61356540a7a0be0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808006"
---
# <span data-ttu-id="292d9-103">Propriétés d'Application Virtualization: onglet Général</span><span class="sxs-lookup"><span data-stu-id="292d9-103">Application Virtualization Properties: General Tab</span></span>


<span data-ttu-id="292d9-104">Utilisez l’onglet **général** de la boîte de dialogue **Propriétés de virtualisation d’application** pour modifier les paramètres du journal et les emplacements des données.</span><span class="sxs-lookup"><span data-stu-id="292d9-104">Use the **General** tab of the **Application Virtualization Properties** dialog box to modify log settings and data locations.</span></span>

<span data-ttu-id="292d9-105">Cet onglet contient les éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="292d9-105">This tab contains the following elements.</span></span>

<a href="" id="log-level"></a>**<span data-ttu-id="292d9-106">Niveau du journal</span><span class="sxs-lookup"><span data-stu-id="292d9-106">Log Level</span></span>**  
<span data-ttu-id="292d9-107">Sélectionnez le niveau dans la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="292d9-107">Select the level from the drop-down list.</span></span> <span data-ttu-id="292d9-108">Le niveau par défaut est **informations**.</span><span class="sxs-lookup"><span data-stu-id="292d9-108">The default level is **Information**.</span></span>

<a href="" id="reset-log"></a>**<span data-ttu-id="292d9-109">Réinitialiser le journal</span><span class="sxs-lookup"><span data-stu-id="292d9-109">Reset Log</span></span>**  
<span data-ttu-id="292d9-110">Cliquez sur ce bouton pour sauvegarder le fichier journal actuel et commencer immédiatement un nouveau fichier journal.</span><span class="sxs-lookup"><span data-stu-id="292d9-110">Click this button to back up the current log file and immediately start a new log file.</span></span>

<a href="" id="location"></a>**<span data-ttu-id="292d9-111">Location</span><span class="sxs-lookup"><span data-stu-id="292d9-111">Location</span></span>**  
<span data-ttu-id="292d9-112">Accédez à l’emplacement où vous souhaitez enregistrer le fichier journal sftlog.txt.</span><span class="sxs-lookup"><span data-stu-id="292d9-112">Enter or browse to the location where you want to save the log file sftlog.txt.</span></span> <span data-ttu-id="292d9-113">Les emplacements par défaut sont les suivants:</span><span class="sxs-lookup"><span data-stu-id="292d9-113">The default locations are as follows:</span></span>

-   <span data-ttu-id="292d9-114">Pour WindowsXP, Windows Server2003 —*C:\\Documents et settings\\All users\\application Data\\Microsoft\\Application client de virtualisation*</span><span class="sxs-lookup"><span data-stu-id="292d9-114">For WindowsXP, Windows Server2003—*C:\\Documents and Settings\\All Users\\Application Data\\Microsoft\\Application Virtualization Client*</span></span>

-   <span data-ttu-id="292d9-115">Pour Windows Vista, Windows 7, Windows Server 2008 —*client de virtualisation C:\\ProgramData\\Microsoft\\Application*</span><span class="sxs-lookup"><span data-stu-id="292d9-115">For Windows Vista, Windows 7, Windows Server2008—*C:\\ProgramData\\Microsoft\\Application Virtualization Client*</span></span>

<a href="" id="system-log-level"></a>**<span data-ttu-id="292d9-116">Niveau du journal système</span><span class="sxs-lookup"><span data-stu-id="292d9-116">System Log Level</span></span>**  
<span data-ttu-id="292d9-117">Sélectionnez le niveau dans la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="292d9-117">Select the level from the drop-down list.</span></span> <span data-ttu-id="292d9-118">Le niveau par défaut est **Avertissement**.</span><span class="sxs-lookup"><span data-stu-id="292d9-118">The default level is **Warning**.</span></span>

<span data-ttu-id="292d9-119">**Remarques**  Le paramètre **niveau du journal système** contrôle le niveau de messages envoyés au journal des événements système.</span><span class="sxs-lookup"><span data-stu-id="292d9-119">**Note** The **System Log Level** setting controls the level of messages sent to the system event log.</span></span> <span data-ttu-id="292d9-120">Les messages enregistrés s’affichent de la même façon que les messages qui sont enregistrés dans le journal des événements du client, mais qui sont stockés dans un autre emplacement sans limitations d’espace du journal des événements client.</span><span class="sxs-lookup"><span data-stu-id="292d9-120">The logged messages are identical to the messages that get logged to the client event log, but they are stored in a different location that does not have the space limitations of the client event log.</span></span> <span data-ttu-id="292d9-121">Dans la mesure où le journal des événements système ne présente pas de limitations d’espace, il convient idéalement pour les situations dans lesquelles la journalisation détaillée est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="292d9-121">Because the system event log does not have space limitations, it is ideally suited for situations where verbose logging is necessary.</span></span>

 

<a href="" id="global-data-directory"></a>**<span data-ttu-id="292d9-122">Global Data Directory</span><span class="sxs-lookup"><span data-stu-id="292d9-122">Global Data Directory</span></span>**  
<span data-ttu-id="292d9-123">Accédez à l’emplacement du répertoire du fichier journal.</span><span class="sxs-lookup"><span data-stu-id="292d9-123">Enter or browse to the location of the directory of the log file.</span></span> <span data-ttu-id="292d9-124">Les emplacements par défaut sont les suivants:</span><span class="sxs-lookup"><span data-stu-id="292d9-124">The default locations are as follows:</span></span>

-   <span data-ttu-id="292d9-125">Pour WindowsXP, Windows Server2003 —*C:\\Documents et settings\\All users\\application Data\\Microsoft\\Application client de virtualisation*</span><span class="sxs-lookup"><span data-stu-id="292d9-125">For WindowsXP, Windows Server2003—*C:\\Documents and Settings\\All Users\\Application Data\\Microsoft\\Application Virtualization Client*</span></span>

-   <span data-ttu-id="292d9-126">Pour Windows Vista, Windows 7, Windows Server 2008 —*client de virtualisation C:\\ProgramData\\Microsoft\\Application*</span><span class="sxs-lookup"><span data-stu-id="292d9-126">For Windows Vista, Windows 7, Windows Server2008—*C:\\ProgramData\\Microsoft\\Application Virtualization Client*</span></span>

<a href="" id="user-data-directory"></a>**<span data-ttu-id="292d9-127">Répertoire de données utilisateur</span><span class="sxs-lookup"><span data-stu-id="292d9-127">User Data Directory</span></span>**  
<span data-ttu-id="292d9-128">Accédez à l’emplacement du répertoire où se trouvent les données propres à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="292d9-128">Enter or browse to the location of the directory where user-specific data is stored.</span></span> <span data-ttu-id="292d9-129">La valeur par défaut est% APPDATA%.</span><span class="sxs-lookup"><span data-stu-id="292d9-129">The default is %APPDATA%.</span></span> <span data-ttu-id="292d9-130">Ce chemin doit être une variable d’environnement valide sur l’ordinateur client.</span><span class="sxs-lookup"><span data-stu-id="292d9-130">This path must be a valid environment variable on the client computer.</span></span>

## <span data-ttu-id="292d9-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="292d9-131">Related topics</span></span>


[<span data-ttu-id="292d9-132">Client Management Console: propriétés d'Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="292d9-132">Client Management Console: Application Virtualization Properties</span></span>](client-management-console-application-virtualization-properties.md)

 

 





