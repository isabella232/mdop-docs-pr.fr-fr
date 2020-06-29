---
title: Comment vérifier les paramètres de première installation
description: Comment vérifier les paramètres de première installation
author: dansimp
ms.assetid: e8a07d4c-5786-4455-ac43-2deac4042efd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d859d627ec90fbc26d18019062d5e316f907cec6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804668"
---
# <span data-ttu-id="213ae-103">Comment vérifier les paramètres de première installation</span><span class="sxs-lookup"><span data-stu-id="213ae-103">How to Verify First Time Setup Settings</span></span>


<span data-ttu-id="213ae-104">Pendant l’exécution de votre test de configuration pour la première fois ou après la fin de celle-ci, vous pouvez vérifier les paramètres que vous avez configurés dans votre espace de travail MED-V en effectuant les tâches suivantes.</span><span class="sxs-lookup"><span data-stu-id="213ae-104">While your test of first time setup is running or after it finishes, you can verify the settings that you configured in your MED-V workspace by performing the following tasks.</span></span>

<span data-ttu-id="213ae-105">**Remarques**  Pour plus d’informations sur la façon de surveiller la réussite de la première configuration au sein de votre entreprise après le déploiement, voir [surveiller les déploiements de l’espace de travail MED-V](monitoring-med-v-workspace-deployments.md).</span><span class="sxs-lookup"><span data-stu-id="213ae-105">**Note** For information about how to monitor the successful completion of first time setup throughout your enterprise after deployment, see [Monitoring MED-V Workspace Deployments](monitoring-med-v-workspace-deployments.md).</span></span>

 

**<span data-ttu-id="213ae-106">Pour vérifier les paramètres lors de la première configuration</span><span class="sxs-lookup"><span data-stu-id="213ae-106">To verify settings during first time setup</span></span>**

1.  <span data-ttu-id="213ae-107">Lors de la première exécution du programme d’installation, vérifiez les points suivants:</span><span class="sxs-lookup"><span data-stu-id="213ae-107">While first time setup is running, verify the following:</span></span>

    <span data-ttu-id="213ae-108">Si vous avez spécifié le mode **inattendé** , vérifiez que l’ordinateur virtuel ne s’affiche pas lors de la première exécution du programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="213ae-108">If you specified **Unattended** mode, verify that the virtual machine does not appear when first time setup is running.</span></span>

    <span data-ttu-id="213ae-109">Si vous avez spécifié le mode assistance, vérifiez que l’ordinateur virtuel apparaît et que tous les champs qui nécessitent une entrée utilisateur sont affichés.</span><span class="sxs-lookup"><span data-stu-id="213ae-109">If you specified attended mode, verify that the virtual machine appears and that all fields that require user input are displayed.</span></span>

2.  <span data-ttu-id="213ae-110">Vous pouvez également surveiller le processus de configuration de la première utilisation lors de l’affichage de l’ordinateur virtuel lors de la première exécution du programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="213ae-110">You can also monitor the complete first time setup process by viewing the virtual machine when first time setup is running.</span></span> <span data-ttu-id="213ae-111">Pour cela, procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="213ae-111">To do this, follow these steps:</span></span>

    1.  <span data-ttu-id="213ae-112">Ouvrez la console de l’ordinateur virtuel Windows.</span><span class="sxs-lookup"><span data-stu-id="213ae-112">Open the Windows Virtual PC Console.</span></span>

        <span data-ttu-id="213ae-113">Cliquez sur **Démarrer**, sur **tous les programmes**, sur **PC virtuel Windows**, puis sur **PC virtuel Windows**.</span><span class="sxs-lookup"><span data-stu-id="213ae-113">Click **Start**, click **All Programs**, click **Windows Virtual PC**, and then click **Windows Virtual PC**.</span></span>

    2.  <span data-ttu-id="213ae-114">Démarrez MED-V s’il n’est pas encore en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="213ae-114">Start MED-V if it is not already running.</span></span>

        <span data-ttu-id="213ae-115">Si ce n’est pas déjà le cas, une machine virtuelle portant le nom de l’espace de travail MED-V s’affiche dans la liste des machines virtuelles.</span><span class="sxs-lookup"><span data-stu-id="213ae-115">If not already present, in a short time, a virtual machine with the name of the deployed MED-V workspace appears in the list of virtual machines.</span></span>

    3.  <span data-ttu-id="213ae-116">Double-cliquez sur la machine virtuelle MED-V pour l’ouvrir.</span><span class="sxs-lookup"><span data-stu-id="213ae-116">Double-click the MED-V virtual machine to open it.</span></span>

        <span data-ttu-id="213ae-117">Vous pouvez observer la machine virtuelle MED-V lorsque celle-ci est en cours de configuration et vous pouvez résoudre les problèmes liés à la mini-installation.</span><span class="sxs-lookup"><span data-stu-id="213ae-117">You can observe the MED-V virtual machine when it is being set up, and you can troubleshoot the Mini-Setup procedure.</span></span> <span data-ttu-id="213ae-118">Vérifiez les informations des différents écrans au fur et à mesure qu’ils sont, par exemple, la configuration des paramètres de mise en réseau, les informations de joint de domaine d’ordinateur, la configuration de l’agent invité, la configuration des paramètres personnels et l’arrêt.</span><span class="sxs-lookup"><span data-stu-id="213ae-118">Verify the information in the different screens as they go by, such as configuring networking settings, computer domain join information, configuring of the Guest Agent, set up of personal settings, and shutdown.</span></span>

    4.  <span data-ttu-id="213ae-119">L’ordinateur virtuel se ferme automatiquement à la fin de la première configuration.</span><span class="sxs-lookup"><span data-stu-id="213ae-119">The virtual machine closes automatically when first time setup finishes.</span></span>

        <span data-ttu-id="213ae-120">**Remarques**  Vous pouvez fermer la fenêtre de l’ordinateur virtuel à tout moment et le programme de configuration pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="213ae-120">**Note** You can close the virtual machine window at any time and first time setup continues.</span></span>

         

**<span data-ttu-id="213ae-121">Pour vérifier les paramètres après la configuration initiale</span><span class="sxs-lookup"><span data-stu-id="213ae-121">To verify settings after first time setup finishes</span></span>**

1.  <span data-ttu-id="213ae-122">Assurez-vous que la première fois que vous avez terminé.</span><span class="sxs-lookup"><span data-stu-id="213ae-122">Ensure that first time setup finished successfully.</span></span>

2.  <span data-ttu-id="213ae-123">Vérifiez que l’espace de travail MED-V est configuré correctement.</span><span class="sxs-lookup"><span data-stu-id="213ae-123">Verify that the MED-V workspace is set up correctly.</span></span>

    1.  <span data-ttu-id="213ae-124">Ouvrez la console de l’ordinateur virtuel Windows.</span><span class="sxs-lookup"><span data-stu-id="213ae-124">Open the Windows Virtual PC Console.</span></span>

        <span data-ttu-id="213ae-125">Cliquez sur **Démarrer**, sur **tous les programmes**, sur **PC virtuel Windows**, puis sur **PC virtuel Windows**.</span><span class="sxs-lookup"><span data-stu-id="213ae-125">Click **Start**, click **All Programs**, click **Windows Virtual PC**, and then click **Windows Virtual PC**.</span></span>

    2.  <span data-ttu-id="213ae-126">Double-cliquez sur l’espace de travail MED-V que vous avez installé.</span><span class="sxs-lookup"><span data-stu-id="213ae-126">Double-click your installed MED-V workspace.</span></span>

        <span data-ttu-id="213ae-127">Si l’espace de travail MED-V exécute déjà une application virtuelle, vous serez peut-être invité à fermer l’application avant de pouvoir ouvrir l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="213ae-127">If the MED-V workspace is already running a virtual application, you might be prompted to close the application before you can open the virtual machine.</span></span>

    3.  <span data-ttu-id="213ae-128">Dans l’espace de travail MED-V, cliquez avec le bouton droit sur **poste**de travail, puis cliquez sur **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="213ae-128">In the MED-V workspace, right-click **My Computer**, and then click **Properties**.</span></span>

    4.  <span data-ttu-id="213ae-129">Vérifiez que l’espace de travail MED-V a rejoint le domaine approprié.</span><span class="sxs-lookup"><span data-stu-id="213ae-129">Verify that the MED-V workspace joined the correct domain.</span></span> <span data-ttu-id="213ae-130">S’il s’applique à votre organisation, testez la jointure de domaines en spécifiant deux domaines différents pour vérifier que le domaine invité est substitué par le domaine hôte.</span><span class="sxs-lookup"><span data-stu-id="213ae-130">If applicable to your organization, test domain joining by specifying two different domains to verify that the guest domain is overridden by the host domain.</span></span>

    5.  <span data-ttu-id="213ae-131">Vérifiez que l’espace de travail MED-V a rejoint l’unité d’organisation du domaine que vous avez spécifiée.</span><span class="sxs-lookup"><span data-stu-id="213ae-131">Verify that the MED-V workspace joined the domain organizational unit that you specified.</span></span>

    6.  <span data-ttu-id="213ae-132">Si vous avez spécifié le masque de nom de l’ordinateur, vérifiez que le nom de l’ordinateur correspond au nom spécifié.</span><span class="sxs-lookup"><span data-stu-id="213ae-132">If you specified the computer name mask, verify that the new computer name matches what was specified.</span></span>

3.  <span data-ttu-id="213ae-133">Vérifiez que les paramètres régionaux spécifiés sont corrects.</span><span class="sxs-lookup"><span data-stu-id="213ae-133">Verify that the locale settings that you specified are correct.</span></span>

    1.  <span data-ttu-id="213ae-134">Dans l’espace de travail MED-V, cliquez sur **Démarrer** , puis sur **panneau de configuration**.</span><span class="sxs-lookup"><span data-stu-id="213ae-134">In the MED-V workspace, click **Start** and then click **Control Panel**.</span></span>

    2.  <span data-ttu-id="213ae-135">Vérifiez vos paramètres de configuration spécifiés, par exemple, **date et heure** , **Options régionales et linguistiques**.</span><span class="sxs-lookup"><span data-stu-id="213ae-135">Verify your specified configuration settings, for example, **Date and Time** and **Regional and Language**.</span></span>

<span data-ttu-id="213ae-136">**Remarques**  Si vous rencontrez des problèmes lors de la vérification des paramètres de configuration pour la première fois, voir [résolution des](operations-troubleshooting-medv2.md)problèmes d’opérations.</span><span class="sxs-lookup"><span data-stu-id="213ae-136">**Note** If you encounter any problems when verifying your first time setup settings, see [Operations Troubleshooting](operations-troubleshooting-medv2.md).</span></span>

 

<span data-ttu-id="213ae-137">Une fois que vous avez vérifié que les paramètres de votre première utilisation sont corrects, vous pouvez tester les autres configurations d’espace de travail MED-V pour vérifier qu’elles fonctionnent comme prévu, par exemple pour la publication d’applications et la redirection d’URL.</span><span class="sxs-lookup"><span data-stu-id="213ae-137">After you have verified that your first time setup settings are correct, you can test other MED-V workspace configurations to verify that they function as intended, such as application publishing and URL redirection.</span></span>

<span data-ttu-id="213ae-138">Après avoir effectué tous les tests de votre package d’espace de travail MED-V et vérifié qu’il fonctionne comme prévu, vous pouvez déployer l’espace de travail MED-V dans votre entreprise.</span><span class="sxs-lookup"><span data-stu-id="213ae-138">After you have completed all testing of your MED-V workspace package and have verified that it is functioning as intended, you can deploy the MED-V workspace to your enterprise.</span></span>

## <span data-ttu-id="213ae-139">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="213ae-139">Related topics</span></span>


[<span data-ttu-id="213ae-140">Comment tester la publication d'applications</span><span class="sxs-lookup"><span data-stu-id="213ae-140">How to Test Application Publishing</span></span>](how-to-test-application-publishing.md)

[<span data-ttu-id="213ae-141">Comment tester la redirection d'URL</span><span class="sxs-lookup"><span data-stu-id="213ae-141">How to Test URL Redirection</span></span>](how-to-test-url-redirection.md)

[<span data-ttu-id="213ae-142">Déploiement du package d'espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="213ae-142">Deploying the MED-V Workspace Package</span></span>](deploying-the-med-v-workspace-package.md)

[<span data-ttu-id="213ae-143">Gérer les paramètres de l'espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="213ae-143">Manage MED-V Workspace Settings</span></span>](manage-med-v-workspace-settings.md)

 

 





