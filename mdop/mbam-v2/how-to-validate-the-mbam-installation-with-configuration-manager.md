---
title: Validation de l'installation de MBAM avec Configuration Manager
description: Validation de l'installation de MBAM avec Configuration Manager
author: dansimp
ms.assetid: 8e268539-91c3-4e8a-baae-faf3605da818
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 500c6f6ee5138b5677bf1fa20e2627a56981df1f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809474"
---
# <span data-ttu-id="a417f-103">Validation de l'installation de MBAM avec Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="a417f-103">How to Validate the MBAM Installation with Configuration Manager</span></span>


<span data-ttu-id="a417f-104">Après l’installation de Microsoft BitLocker administration et de la surveillance (MBAM) avec Configuration Manager, vérifiez que l’installation a correctement configuré toutes les fonctionnalités nécessaires pour MBAM en effectuant les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="a417f-104">After installing Microsoft BitLocker Administration and Monitoring (MBAM) with Configuration Manager, validate that the installation has successfully set up all the necessary features for MBAM by completing the following steps.</span></span>

**<span data-ttu-id="a417f-105">Pour valider l’installation de la fonctionnalité MBAM Server avec Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="a417f-105">To validate the MBAM Server feature installation with Configuration Manager</span></span>**

1.  <span data-ttu-id="a417f-106">Sur le serveur sur lequel System Center Configuration Manager est déployé, ouvrez le **panneau**de configuration.</span><span class="sxs-lookup"><span data-stu-id="a417f-106">On the server where System Center Configuration Manager is deployed, open **Control Panel**.</span></span> <span data-ttu-id="a417f-107">Sélectionnez le programme utilisé pour désinstaller ou modifier un programme.</span><span class="sxs-lookup"><span data-stu-id="a417f-107">Select the program that is used to uninstall or change a program.</span></span> <span data-ttu-id="a417f-108">Vérifiez que le **contrôle et l’administration de BitLocker Microsoft** s’affichent dans la liste des programmes et fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="a417f-108">Verify that **Microsoft BitLocker Administration and Monitoring** appears in the list of programs and features.</span></span>

    <span data-ttu-id="a417f-109">**Remarques**  Pour valider l’installation, vous devez utiliser un compte de domaine disposant d’informations d’identification d’administrateur local sur chaque serveur.</span><span class="sxs-lookup"><span data-stu-id="a417f-109">**Note** To validate the installation, you must use a domain account that has local computer administrative credentials on each server.</span></span>

     

2.  <span data-ttu-id="a417f-110">Utilisez la console Configuration Manager pour vérifier qu’une nouvelle collection, appelée «MBAM d’ordinateurs pris en charge», s’affiche.</span><span class="sxs-lookup"><span data-stu-id="a417f-110">Use the Configuration Manager console to confirm that a new collection, called “MBAM Supported Computers,” is displayed.</span></span>

    <span data-ttu-id="a417f-111">Pour afficher la collection avec Configuration Manager 2007: cliquez sur **base de données de site** ( &lt; **SiteCode** &gt;  -  &lt; **serveur** &gt; , &lt; **SiteName** &gt; ), gestion de l' **ordinateur**.</span><span class="sxs-lookup"><span data-stu-id="a417f-111">To view the collection with Configuration Manager 2007: Click **Site Database** (&lt;**SiteCode**&gt; - &lt;**ServerName**&gt;, &lt;**SiteName**&gt;), **Computer Management**.</span></span>

    <span data-ttu-id="a417f-112">Pour afficher la collection avec SystemCenter2012 ConfigurationManager: cliquez sur l’espace de travail **ressources et conformité** , **collections de périphériques**.</span><span class="sxs-lookup"><span data-stu-id="a417f-112">To view the collection with SystemCenter2012 ConfigurationManager: Click the **Assets and Compliance** workspace, **Device Collections**.</span></span>

3.  <span data-ttu-id="a417f-113">Utilisez la console Configuration Manager pour vérifier que les rapports suivants apparaissent dans le dossier **MBAM** :</span><span class="sxs-lookup"><span data-stu-id="a417f-113">Use the Configuration Manager console to verify that the following reports are listed in the **MBAM** folder:</span></span>

    -   <span data-ttu-id="a417f-114">Compatibilité de l’ordinateur BitLocker</span><span class="sxs-lookup"><span data-stu-id="a417f-114">BitLocker Computer Compliance</span></span>

    -   <span data-ttu-id="a417f-115">Tableau de bord de conformité de BitLocker Enterprise</span><span class="sxs-lookup"><span data-stu-id="a417f-115">BitLocker Enterprise Compliance Dashboard</span></span>

    -   <span data-ttu-id="a417f-116">Détails de la conformité à l’entreprise BitLocker</span><span class="sxs-lookup"><span data-stu-id="a417f-116">BitLocker Enterprise Compliance Details</span></span>

    -   <span data-ttu-id="a417f-117">Résumé de conformité de BitLocker Enterprise</span><span class="sxs-lookup"><span data-stu-id="a417f-117">BitLocker Enterprise Compliance Summary</span></span>

    <span data-ttu-id="a417f-118">Pour afficher les rapports avec Configuration Manager 2007: cliquez sur **création**de rapports, **Reporting Services**, \ \ \ \ &lt; **NomServeur** &gt; , **dossiers de rapports** .</span><span class="sxs-lookup"><span data-stu-id="a417f-118">To view the reports with Configuration Manager 2007: Click **Reporting**, **Reporting Services**, \\\\&lt;**ServerName**&gt;, **Report Folders**</span></span>

    <span data-ttu-id="a417f-119">Pour afficher les rapports avec SystemCenter2012 ConfigurationManager: cliquez sur l’espace de travail de **surveillance** , **création**de rapports, **rapports**.</span><span class="sxs-lookup"><span data-stu-id="a417f-119">To view the reports with SystemCenter2012 ConfigurationManager: Click the **Monitoring** workspace, **Reporting**, **Reports**.</span></span>

4.  <span data-ttu-id="a417f-120">Utilisez la console Configuration Manager pour vérifier que la configuration de base de la sécurité de BitLocker figure dans la liste.</span><span class="sxs-lookup"><span data-stu-id="a417f-120">Use the Configuration Manager console to confirm that the configuration baseline “BitLocker Protection” is listed.</span></span>

    <span data-ttu-id="a417f-121">Pour afficher les planifications de configuration à l’aide de Configuration Manager 2007: cliquez sur gestion de la **configuration souhaitée**, **planning de référence de configuration**.</span><span class="sxs-lookup"><span data-stu-id="a417f-121">To view the configuration baselines with Configuration Manager 2007: Click **Desired Configuration Management**, **Configuration Baselines**.</span></span>

    <span data-ttu-id="a417f-122">Pour afficher les lignes de base de configuration avec SystemCenter2012 ConfigurationManager: cliquez sur l’espace de travail **ressources et conformité** , **paramètres de conformité**, **planning de référence de configuration**.</span><span class="sxs-lookup"><span data-stu-id="a417f-122">To view the configuration baselines with SystemCenter2012 ConfigurationManager: Click the **Assets and Compliance** workspace, **Compliance Settings**, **Configuration Baselines**.</span></span>

5.  <span data-ttu-id="a417f-123">Utilisez la console Configuration Manager pour vérifier que les nouveaux éléments de configuration suivants sont affichés:</span><span class="sxs-lookup"><span data-stu-id="a417f-123">Use the Configuration Manager console to confirm that the following new configuration items are displayed:</span></span>

    -   <span data-ttu-id="a417f-124">Protection des lecteurs de données fixes BitLocker</span><span class="sxs-lookup"><span data-stu-id="a417f-124">BitLocker Fixed Data Drives Protection</span></span>

    -   <span data-ttu-id="a417f-125">Protection des lecteurs du système d’exploitation BitLocker</span><span class="sxs-lookup"><span data-stu-id="a417f-125">BitLocker Operating System Drive Protection</span></span>

    <span data-ttu-id="a417f-126">Pour afficher les éléments de configuration avec Configuration Manager 2007: cliquez sur gestion de la configuration, **éléments de configuration** **souhaités**.</span><span class="sxs-lookup"><span data-stu-id="a417f-126">To view the configuration items with Configuration Manager 2007: Click **Desired Configuration Management**, **Configuration Items**.</span></span>

    <span data-ttu-id="a417f-127">Pour afficher les éléments de configuration avec SystemCenter2012 ConfigurationManager: cliquez sur l’espace de travail **ressources et conformité** , **paramètres de conformité**et **éléments de configuration**.</span><span class="sxs-lookup"><span data-stu-id="a417f-127">To view the configuration items with SystemCenter2012 ConfigurationManager: Click the **Assets and Compliance** workspace, **Compliance Settings**, **Configuration Items**.</span></span>

## <span data-ttu-id="a417f-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a417f-128">Related topics</span></span>


[<span data-ttu-id="a417f-129">Déploiement de MBAM avec Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="a417f-129">Deploying MBAM with Configuration Manager</span></span>](deploying-mbam-with-configuration-manager-mbam2.md)

 

 





