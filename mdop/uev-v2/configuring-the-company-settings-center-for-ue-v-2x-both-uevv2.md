---
title: Configuration du centre de paramètres de société pour UE-V 2. x
description: Configuration du centre de paramètres de société pour UE-V 2. x
author: dansimp
ms.assetid: 48fadb0a-c0dc-4287-9474-f94ce1417003
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 0226b3c156a6d6ca39b0214de8acf0c5990db349
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809869"
---
# <span data-ttu-id="24bf3-103">Configuration du centre de paramètres de société pour UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="24bf3-103">Configuring the Company Settings Center for UE-V 2.x</span></span>


<span data-ttu-id="24bf3-104">La virtualisation de l’interface utilisateur de Microsoft (UE-V) 2,0, 2,1 et 2,1 SP1 inclut une nouvelle application, le centre de paramètres de l’entreprise, qui aide les utilisateurs à gérer les paramètres à synchroniser.</span><span class="sxs-lookup"><span data-stu-id="24bf3-104">Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, and 2.1 SP1 include a new application, the Company Settings Center, which helps users manage settings to synchronize.</span></span> <span data-ttu-id="24bf3-105">Le centre de paramètres d’une entreprise est installé à l’aide de l’agent UE-V.</span><span class="sxs-lookup"><span data-stu-id="24bf3-105">The Company Settings Center is installed by using the UE-V Agent.</span></span> <span data-ttu-id="24bf3-106">Les utilisateurs accèdent au centre de paramètres d’une entreprise dans le panneau de configuration, dans le menu **Démarrer** ou l’écran d' **Accueil** , puis via l’icône de zone de notification UE-V.</span><span class="sxs-lookup"><span data-stu-id="24bf3-106">Users access the Company Settings Center in Control Panel, in the **Start** menu or on the **Start** screen, and via the UE-V notification area icon.</span></span> <span data-ttu-id="24bf3-107">Le centre de paramètres de la société affiche les paramètres qui sont synchronisés et aide les utilisateurs à consulter l’état de synchronisation d’UE-V.</span><span class="sxs-lookup"><span data-stu-id="24bf3-107">Company Settings Center displays which settings are synchronized and helps users see the synchronization status of UE-V.</span></span> <span data-ttu-id="24bf3-108">Les utilisateurs peuvent utiliser le centre de paramètres de la société pour sélectionner les applications ou fonctionnalités Windows qui synchronisent leurs paramètres entre eux.</span><span class="sxs-lookup"><span data-stu-id="24bf3-108">Users can use the Company Settings Center to select which applications or Windows features synchronize their settings between computers.</span></span> <span data-ttu-id="24bf3-109">Ils peuvent également cliquer sur le bouton **Synchroniser maintenant** pour synchroniser tous les paramètres immédiatement.</span><span class="sxs-lookup"><span data-stu-id="24bf3-109">They can also click the **Sync Now** button to synchronize all settings immediately.</span></span> <span data-ttu-id="24bf3-110">L’administrateur peut également inclure un lien pour le support dans le centre de paramètres de l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="24bf3-110">The administrator can also include a link for support in the Company Settings Center.</span></span>

## <span data-ttu-id="24bf3-111">À propos du centre de paramètres de la société</span><span class="sxs-lookup"><span data-stu-id="24bf3-111">About the Company Settings Center</span></span>


<span data-ttu-id="24bf3-112">L’application de bureau centre de paramètres de l’entreprise fournit aux utilisateurs des informations relatives à la synchronisation des paramètres d’UE-V.</span><span class="sxs-lookup"><span data-stu-id="24bf3-112">The Company Settings Center desktop application provides users with information about UE-V settings synchronization.</span></span> <span data-ttu-id="24bf3-113">Le centre de paramètres d’une entreprise est accessible de différentes manières:</span><span class="sxs-lookup"><span data-stu-id="24bf3-113">The Company Settings Center is accessible in several different ways:</span></span>

-   <span data-ttu-id="24bf3-114">Icône de la zone de notification: avec le paramètre de stratégie de groupe icône de la **barre d’État** ou configuration Windows PowerShell activée, l’icône UE-V apparaît dans la zone de notification.</span><span class="sxs-lookup"><span data-stu-id="24bf3-114">Notification area icon – With the **Tray Icon** Group Policy setting or Windows PowerShell configuration enabled, the UE-V icon appears in the notification area.</span></span> <span data-ttu-id="24bf3-115">Cliquez sur l’icône UE-V pour ouvrir le centre de paramètres de la société.</span><span class="sxs-lookup"><span data-stu-id="24bf3-115">Click the UE-V icon to open the Company Settings Center.</span></span>

    <span data-ttu-id="24bf3-116">**Remarques**  L’icône zone de notification peut être désactivée en utilisant les paramètres suivants:</span><span class="sxs-lookup"><span data-stu-id="24bf3-116">**Note** The notification area icon can be disabled by using the following settings:</span></span>

    -   <span data-ttu-id="24bf3-117">Paramètre de stratégie de groupe:</span><span class="sxs-lookup"><span data-stu-id="24bf3-117">Group Policy setting:</span></span> `Policy Tray Icon`

    -   <span data-ttu-id="24bf3-118">Cmdlet Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="24bf3-118">Windows PowerShell cmdlet:</span></span> `TrayIconEnabled`

    -   <span data-ttu-id="24bf3-119">Élément de configuration dans le Pack de configuration UE-V pour SystemCenter2012 ConfigurationManager:</span><span class="sxs-lookup"><span data-stu-id="24bf3-119">Configuration item in the UE-V Configuration Pack for SystemCenter2012 ConfigurationManager:</span></span> `Tray icon enabled`

     

-   <span data-ttu-id="24bf3-120">Application du panneau de configuration: dans le panneau de configuration, accédez à **apparence et personnalisation**, puis cliquez sur Centre de gestion des **entreprises**.</span><span class="sxs-lookup"><span data-stu-id="24bf3-120">Control Panel application – In Control Panel, browse to **Appearance and Personalization**, and then click **Company Settings Center**.</span></span>

-   <span data-ttu-id="24bf3-121">Notification d’utilisation initiale: sauf si elle est désactivée, l’agent UE-V avertit l’utilisateur que les paramètres sont maintenant synchronisés lorsque l’agent UE-V est exécuté pour la première fois sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="24bf3-121">First use notification – Unless disabled, the UE-V Agent alerts the user that settings are now synchronized when the UE-V agent runs for the first time on a computer.</span></span> <span data-ttu-id="24bf3-122">Cliquez sur la boîte de dialogue de notification pour ouvrir le centre de paramètres de la société.</span><span class="sxs-lookup"><span data-stu-id="24bf3-122">Click the notification dialog box to open the Company Settings Center.</span></span>

-   <span data-ttu-id="24bf3-123">L’écran d' **Accueil** ou le menu **Démarrer** inclut un lien vers le centre de paramètres de l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="24bf3-123">The **Start** screen or **Start** menu includes a link to the Company Settings Center.</span></span> <span data-ttu-id="24bf3-124">La recherche du centre de paramètres de la société trouve l’application.</span><span class="sxs-lookup"><span data-stu-id="24bf3-124">A search for Company Settings Center finds the application.</span></span>

## <span data-ttu-id="24bf3-125">Configuration du lien support dans le centre de paramètres de la société</span><span class="sxs-lookup"><span data-stu-id="24bf3-125">Configuring the support link in the Company Settings Center</span></span>


<span data-ttu-id="24bf3-126">Le centre de paramètres de la société peut inclure un lien hypertexte sur lequel les utilisateurs peuvent cliquer pour obtenir de l’aide sur les problèmes de synchronisation des paramètres d’UE-V.</span><span class="sxs-lookup"><span data-stu-id="24bf3-126">The Company Settings Center can include a hyperlink that users can click to get support with UE-V settings synchronization problems.</span></span> <span data-ttu-id="24bf3-127">Ce lien peut ouvrir des protocoles d’URL valides, tels que http://pour une page Web ou mailto://pour un message électronique.</span><span class="sxs-lookup"><span data-stu-id="24bf3-127">This link can open any valid URL protocol, such as http:// for a webpage or mailto:// for an email.</span></span> <span data-ttu-id="24bf3-128">Le lien support peut être configuré à l’aide d’une stratégie de groupe, de Windows PowerShell ou du Pack de configuration de System Center 2012 Configuration Manager UE-V.</span><span class="sxs-lookup"><span data-stu-id="24bf3-128">The support link can be configured by using Group Policy, Windows PowerShell, or the System Center 2012 Configuration Manager UE-V Configuration Pack.</span></span>

**<span data-ttu-id="24bf3-129">Comment configurer le lien du support du centre de paramètres de la société</span><span class="sxs-lookup"><span data-stu-id="24bf3-129">How to configure the Company Settings Center support link</span></span>**

1.  <span data-ttu-id="24bf3-130">Ouvrez l’outil de gestion de votre choix:</span><span class="sxs-lookup"><span data-stu-id="24bf3-130">Open your preferred management tool:</span></span>

    -   <span data-ttu-id="24bf3-131">**Stratégie de groupe** : Si vous ne l’avez pas déjà fait, téléchargez le modèle ADMX pour UE-V 2 à partir des [modèles d’administration de MDOP](https://go.microsoft.com/fwlink/p/?LinkId=393941).</span><span class="sxs-lookup"><span data-stu-id="24bf3-131">**Group Policy** - If you have not already done so, download the ADMX template for UE-V 2 from [MDOP Administrative Templates](https://go.microsoft.com/fwlink/p/?LinkId=393941).</span></span>

    -   <span data-ttu-id="24bf3-132">**Windows PowerShell** : sur un ordinateur sur lequel l’agent UE-V est installé, ouvrez **Windows PowerShell**.</span><span class="sxs-lookup"><span data-stu-id="24bf3-132">**Windows PowerShell** – On a computer with the UE-V Agent installed, open **Windows PowerShell**.</span></span> <span data-ttu-id="24bf3-133">Pour plus d’informations sur l’administration de UE-V à l’aide de Windows PowerShell, voir [administration d’UE-v 2. x avec Windows PowerShell et WMI](administering-ue-v-2x-with-windows-powershell-and-wmi-both-uevv2.md).</span><span class="sxs-lookup"><span data-stu-id="24bf3-133">For more information about administering UE-V by using Windows PowerShell, see [Administering UE-V 2.x with Windows PowerShell and WMI](administering-ue-v-2x-with-windows-powershell-and-wmi-both-uevv2.md).</span></span>

    -   <span data-ttu-id="24bf3-134">**Module de configuration de System Center 2012 pour l’utilisation de Microsoft User Interface Virtualization (UE-v)** – importez le Pack de configuration pour UE-V et suivez la documentation du module de configuration pour créer des éléments de configuration.</span><span class="sxs-lookup"><span data-stu-id="24bf3-134">**System Center 2012 Configuration Pack for Microsoft User Experience Virtualization (UE-V)** – Import the UE-V Configuration Pack and follow the Configuration Pack documentation to create configuration items.</span></span> <span data-ttu-id="24bf3-135">Pour plus d’informations sur le Pack de configuration pour UE-V, voir [configuration d’UE-v 2. x avec System Center Configuration Manager 2012](configuring-ue-v-2x-with-system-center-configuration-manager-2012-both-uevv2.md).</span><span class="sxs-lookup"><span data-stu-id="24bf3-135">For more information about the UE-V Configuration Pack, see [Configuring UE-V 2.x with System Center Configuration Manager 2012](configuring-ue-v-2x-with-system-center-configuration-manager-2012-both-uevv2.md).</span></span>

2.  <span data-ttu-id="24bf3-136">Modifiez les paramètres des stratégies suivantes:</span><span class="sxs-lookup"><span data-stu-id="24bf3-136">Edit the settings for the following policies:</span></span>

    -   <span data-ttu-id="24bf3-137">**Texte du lien vers le contact** : ce paramètre spécifie le texte du lien hypertexte d’URL de contact dans le centre de paramètres de l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="24bf3-137">**Contact IT Link Text** - This setting specifies the text of the Contact IT URL hyperlink in the Company Settings Center.</span></span> <span data-ttu-id="24bf3-138">Si vous activez ce paramètre, le centre de paramètres de la société affiche le texte spécifié dans le lien vers l’URL du contact.</span><span class="sxs-lookup"><span data-stu-id="24bf3-138">If you enable this setting, the Company Settings Center displays the specified text in the link to the Contact IT URL.</span></span>

        -   <span data-ttu-id="24bf3-139">Paramètres de stratégie de groupe:</span><span class="sxs-lookup"><span data-stu-id="24bf3-139">Group Policy settings:</span></span> `Contact IT Link Text`

        -   <span data-ttu-id="24bf3-140">Cmdlet Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="24bf3-140">Windows PowerShell cmdlet:</span></span> `ContactITDescription`

        -   <span data-ttu-id="24bf3-141">Élément de configuration du module de configuration:</span><span class="sxs-lookup"><span data-stu-id="24bf3-141">Configuration Pack configuration item:</span></span> `IT contact descriptive text`

    -   <span data-ttu-id="24bf3-142">**URL du contact** : ce paramètre spécifie l’URL du lien de contact dans le centre de paramètres de la société dans un protocole d’URL valide tel que http://pour une page web ou mailto://pour un message électronique.</span><span class="sxs-lookup"><span data-stu-id="24bf3-142">**Contact IT URL** - This setting specifies the URL for the Contact IT link in the Company Settings Center in a valid URL protocol, such as http:// for a webpage or mailto:// for an email.</span></span>

        -   <span data-ttu-id="24bf3-143">Paramètres de stratégie de groupe:</span><span class="sxs-lookup"><span data-stu-id="24bf3-143">Group Policy settings:</span></span> `Contact IT URL`

        -   <span data-ttu-id="24bf3-144">Cmdlet Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="24bf3-144">Windows PowerShell cmdlet:</span></span> `ContactITUrl`

        -   <span data-ttu-id="24bf3-145">Élément de configuration du module de configuration:</span><span class="sxs-lookup"><span data-stu-id="24bf3-145">Configuration Pack configuration item:</span></span> `IT contact URL`

3.  <span data-ttu-id="24bf3-146">Déployez les paramètres sur les ordinateurs des utilisateurs à l’aide de l’outil de gestion.</span><span class="sxs-lookup"><span data-stu-id="24bf3-146">Deploy settings to users’ computers by using the management tool.</span></span>






 

 





