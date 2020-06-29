---
title: Gestion des mises à jour automatiques pour les espaces de travail MED-V
description: Gestion des mises à jour automatiques pour les espaces de travail MED-V
author: dansimp
ms.assetid: 306f28a2-d653-480d-b737-4b8b3132de5d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: b22d3250db806e740c1d62da4fed98d5956b0eeb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811069"
---
# <span data-ttu-id="af318-103">Gestion des mises à jour automatiques pour les espaces de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="af318-103">Managing Automatic Updates for MED-V Workspaces</span></span>


<span data-ttu-id="af318-104">L’espace de travail MED-V est une machine virtuelle qui contient un système d’exploitation distinct, dont le processus automatique de mise à jour des logiciels doit être géré de la même manière que les ordinateurs physiques de votre entreprise.</span><span class="sxs-lookup"><span data-stu-id="af318-104">The MED-V workspace is a virtual machine that contains a separate operating system, whose automatic software update process must be managed just like the physical computers in your enterprise.</span></span> <span data-ttu-id="af318-105">Étant donné que le système d’exploitation invité n’est pas toujours en cours d’exécution quand le système d’exploitation hôte est en cours d’exécution, vous devez vous assurer que l’ordinateur virtuel MED-V est configuré de telle sorte que les mises à jour logicielles puissent être appliquées au système d’exploitation invité selon les besoins.</span><span class="sxs-lookup"><span data-stu-id="af318-105">Because the guest operating system is not always necessarily running when the host operating system is running, you must ensure that the MED-V virtual machine is configured in such a way that software updates can be applied to the guest operating system as required.</span></span> <span data-ttu-id="af318-106">La solution 2,0 de Microsoft Enterprise Desktop Virtualization (MED-V) fournit des fonctionnalités qui vous permettent de déterminer la façon dont les mises à jour logicielles automatiques sont traitées dans un espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="af318-106">The Microsoft Enterprise Desktop Virtualization (MED-V) 2.0 solution provides the functionality that lets you determine how automatic software updates are processed in a MED-V workspace.</span></span>

## <span data-ttu-id="af318-107">Gestion de la stratégie de réveil d’un espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="af318-107">Managing MED-V Workspace Wake-Up Policy</span></span>


<span data-ttu-id="af318-108">La politique de mise en éveil de l’espace de travail MED-V garantit que l’ordinateur virtuel MED-V est mis à disposition pour les mises à jour de la durée spécifiée dans les paramètres de configuration de MED-V.</span><span class="sxs-lookup"><span data-stu-id="af318-108">The MED-V workspace wake-up policy guarantees that the MED-V virtual machine is made available for updates for the time that you specify in your MED-V configuration settings.</span></span> <span data-ttu-id="af318-109">Cela s’applique aux mises à jour publiées par Microsoft via Windows Update et mises à jour déployées et contrôlées par d’autres solutions que Microsoft (par exemple, des applications antivirus).</span><span class="sxs-lookup"><span data-stu-id="af318-109">This applies to both updates that are published from Microsoft through Windows Update and updates deployed and controlled by non-Microsoft solutions, such as antivirus applications.</span></span>

<span data-ttu-id="af318-110">**Important**  La stratégie de réveil de l’espace de travail MED-V est optimisée pour l’infrastructure Microsoft Update.</span><span class="sxs-lookup"><span data-stu-id="af318-110">**Important** The MED-V workspace wake-up policy is optimized for the Microsoft Update infrastructure.</span></span> <span data-ttu-id="af318-111">Si vous utilisez Microsoft System Center Configuration Manager pour déployer des mises à jour non Microsoft, nous vous conseillons d’utiliser également l’éditeur de mises à jour de System Center, qui tire parti de la même infrastructure que Microsoft Update et, par conséquent, les avantages de la stratégie de réveil de l’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="af318-111">If you are using Microsoft System Center Configuration Manager to deploy non-Microsoft updates, we recommend that you also use the System Center Updates Publisher, which takes advantage of the same infrastructure as Microsoft Update and therefore benefits from the MED-V workspace wake-up policy.</span></span> <span data-ttu-id="af318-112">Pour plus d’informations, reportez-vous à la rubrique [Publisher System Center Updates](https://go.microsoft.com/fwlink/?LinkId=200035) ( https://go.microsoft.com/fwlink/?LinkId=200035) .</span><span class="sxs-lookup"><span data-stu-id="af318-112">For more information, see [System Center Updates Publisher](https://go.microsoft.com/fwlink/?LinkId=200035) (https://go.microsoft.com/fwlink/?LinkId=200035).</span></span>

 

<span data-ttu-id="af318-113">Lorsque vous avez créé votre package d’espace de travail MED-V, vous avez configuré le moment et le mode de démarrage de celui-ci lorsque l’utilisateur final se connecte (**démarrage rapide**) ou lorsque l’utilisateur final ouvre une application publiée (**début normal**).</span><span class="sxs-lookup"><span data-stu-id="af318-113">When you created your MED-V workspace package, you configured when and how it starts, either when the end user logs on (**Fast Start**) or when the end user first opens a published application (**Normal Start**).</span></span> <span data-ttu-id="af318-114">Vous pouvez également définir l’option pour permettre à l’utilisateur final de contrôler ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="af318-114">Or you set the option to let the end user control this setting.</span></span>

<span data-ttu-id="af318-115">Quelle que soit la méthode choisie, chaque fois que l’option **démarrage rapide** est sélectionnée, l’ordinateur virtuel continue de s’exécuter tant que l’hôte MED-V est connecté en tant qu’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="af318-115">Either way, whenever the **Fast Start** option is selected, the virtual machine continues to run as long as the MED-V host is logged on as User.</span></span> <span data-ttu-id="af318-116">Dans cette configuration, dans la mesure où MED-V est actif lorsque l’hôte est actif, des mises à jour automatiques sont appliquées sans nécessiter de traitement supplémentaire de MED-V.</span><span class="sxs-lookup"><span data-stu-id="af318-116">In this configuration, because MED-V is active when the host is active, automatic updates are applied without requiring any extra processing from MED-V.</span></span>

<span data-ttu-id="af318-117">Néanmoins, dans les cas où le **démarrage rapide** n’est pas spécifié ou la mise en veille prolongée de la machine virtuelle, med-v garantit que le système d’exploitation invité est mis à jour régulièrement, même lorsque MED-v n’est pas utilisé régulièrement.</span><span class="sxs-lookup"><span data-stu-id="af318-117">However, for those cases in which **Fast Start** is not specified or the virtual machine hibernates or stops, MED-V guarantees through its MED-V workspace wake-up policy that the guest operating system is being regularly updated even when MED-V is not used regularly.</span></span> <span data-ttu-id="af318-118">MED-V effectue cette fonction en réappliquant régulièrement l’ordinateur virtuel en fonction des paramètres de configuration que vous spécifiez.</span><span class="sxs-lookup"><span data-stu-id="af318-118">MED-V performs this function by regularly waking up the virtual machine based on the configuration settings that you specify.</span></span> <span data-ttu-id="af318-119">Cela permet aux clients de mise à jour automatique de l’ordinateur virtuel de s’exécuter en fonction de leurs configurations.</span><span class="sxs-lookup"><span data-stu-id="af318-119">This enables the automatic update clients in the virtual machine to execute based on their configurations.</span></span><span data-ttu-id="af318-120">Au terme de la période définie par le paramètre de configuration MED-V, MED-V renvoie l’ordinateur virtuel à son état antérieur.</span><span class="sxs-lookup"><span data-stu-id="af318-120">After the time period defined by the MED-V configuration setting elapses, MED-V returns the virtual machine to its previous state.</span></span>

<span data-ttu-id="af318-121">**Remarques**  Si l’utilisateur final ouvre une application publiée pendant la période de mise à jour, les mises à jour requises sont appliquées, mais MED-V n’est pas automatiquement mis en veille ou n’est pas arrêté après la fin de la période de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="af318-121">**Note** If the end user opens a published application during the update period, the required updates are applied, but MED-V is not automatically hibernated or shut down after the update period ends.</span></span> <span data-ttu-id="af318-122">En revanche, MED-V continue de s’exécuter.</span><span class="sxs-lookup"><span data-stu-id="af318-122">Instead, MED-V continues running.</span></span>

 

<span data-ttu-id="af318-123">La stratégie de réveil de l’espace de travail MED-V comporte trois composants principaux:</span><span class="sxs-lookup"><span data-stu-id="af318-123">The MED-V workspace wake-up policy includes three main components:</span></span>

**<span data-ttu-id="af318-124">Gestionnaire de mise à jour invité</span><span class="sxs-lookup"><span data-stu-id="af318-124">Guest Update Manager</span></span>**

<span data-ttu-id="af318-125">Résidant sur l’hôte MED-V, ce programme exécutable autonome est responsable de la réactivation de la machine virtuelle en fonction d’une planification prédéfinie et configurable.</span><span class="sxs-lookup"><span data-stu-id="af318-125">Residing on the MED-V host, this stand-alone executable program is responsible for waking up the virtual machine according to a predefined, configurable schedule.</span></span> <span data-ttu-id="af318-126">Spécifiez les paramètres de configuration qui indiquent à quel moment le gestionnaire de mise à jour doit réveiller l’ordinateur virtuel tous les jours et la durée de conservation de l’ordinateur virtuel (en minutes) pour permettre l’application des mises à jour.</span><span class="sxs-lookup"><span data-stu-id="af318-126">Specify the configuration settings to indicate at what time the update manager should wake up the virtual machine every day, and how long the virtual machine should be kept awake (in minutes) to allow for updates to be applied.</span></span> <span data-ttu-id="af318-127">Une fois que le nombre de minutes spécifié est atteint, le gestionnaire de mise à jour invité place l’ordinateur virtuel en hibernation, préparé pour une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="af318-127">After the number of minutes specified has been reached, the guest update manager puts the virtual machine into hibernation, prepared for the next use.</span></span> <span data-ttu-id="af318-128">Vous pouvez planifier l’exécution de ce programme exécutable par le biais du gestionnaire des tâches Windows.</span><span class="sxs-lookup"><span data-stu-id="af318-128">You can schedule the execution of this executable program through the Windows Task Manager.</span></span>

**<span data-ttu-id="af318-129">Service de gestion de redémarrage d’invité</span><span class="sxs-lookup"><span data-stu-id="af318-129">Guest Restart Management Service</span></span>**

<span data-ttu-id="af318-130">Résidant sur l’hôte MED-V, ce service a trois responsabilités principales.</span><span class="sxs-lookup"><span data-stu-id="af318-130">Residing on the MED-V host, this service has three primary responsibilities.</span></span> <span data-ttu-id="af318-131">Outre le gestionnaire de mise à jour des invités, il gère le redémarrage de l’ordinateur virtuel lors de la connexion de l’utilisateur, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="af318-131">Along with the Guest Update Manager, it manages the restart of the virtual machine at user logon, if it is required.</span></span> <span data-ttu-id="af318-132">Il détecte le redémarrage de l’ordinateur virtuel requis par le biais des mises à jour installées.</span><span class="sxs-lookup"><span data-stu-id="af318-132">It detects when virtual machine restarts are required caused by updates being installed.</span></span> <span data-ttu-id="af318-133">Le gestionnaire de mise à jour des invités doit donc toujours être planifié en fonction de la configuration.</span><span class="sxs-lookup"><span data-stu-id="af318-133">And it ensures that the task for the Guest Update Manager is always scheduled according to configuration.</span></span>

**<span data-ttu-id="af318-134">Service de mise à jour invité</span><span class="sxs-lookup"><span data-stu-id="af318-134">Guest Update Service</span></span>**

<span data-ttu-id="af318-135">Résidant sur la machine virtuelle MED-V, ce service Windows est responsable de la surveillance des mises à jour installées.</span><span class="sxs-lookup"><span data-stu-id="af318-135">Residing on the MED-V virtual machine, this Windows service has the responsibility of monitoring when installed updates require a restart.</span></span> <span data-ttu-id="af318-136">Lorsque le service a été informé de la nécessité d’un redémarrage, il notifie le service de gestion de redémarrage invité de l’hôte.</span><span class="sxs-lookup"><span data-stu-id="af318-136">After the service becomes aware of the need for a restart, it notifies the guest restart management service on the host.</span></span>

### <span data-ttu-id="af318-137">Paramètres de configuration de la stratégie de réveil de l’espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="af318-137">Configuration Settings for MED-V Workspace Wake-Up Policy</span></span>

<span data-ttu-id="af318-138">Vous pouvez contrôler le moment et la durée pendant laquelle l’ordinateur virtuel s’est réveillé pour recevoir les mises à jour automatiques en définissant les deux valeurs de configuration suivantes dans le registre.</span><span class="sxs-lookup"><span data-stu-id="af318-138">You control when and for how long the virtual machine awakens to receive automatic updates by defining the following two configuration values in the registry.</span></span> <span data-ttu-id="af318-139">Ces deux valeurs se trouvent sous la clé HKLM\\Software\\Microsoft\\MEDV\\v2\\VM.</span><span class="sxs-lookup"><span data-stu-id="af318-139">Both of these values are located under the HKLM\\Software\\Microsoft\\MEDV\\v2\\VM key.</span></span>

<span data-ttu-id="af318-140">**GuestUpdateTime** : configure les heures et les minutes quotidiennement lorsque MED-V doit réveiller l’ordinateur virtuel pour la mise à jour, en fonction de la norme d’horloge de 24 heures.</span><span class="sxs-lookup"><span data-stu-id="af318-140">**GuestUpdateTime** – Configures the hour and minute each day when MED-V must wake up the virtual machine for updating, based on the 24-hour clock standard.</span></span> <span data-ttu-id="af318-141">Spécifiez l’heure au format HH: MM.</span><span class="sxs-lookup"><span data-stu-id="af318-141">Specify the time in the format HH:MM.</span></span> <span data-ttu-id="af318-142">La valeur par défaut est 00:00 (minuit).</span><span class="sxs-lookup"><span data-stu-id="af318-142">The default value is 00:00 (midnight).</span></span>

<span data-ttu-id="af318-143">**GuestUpdateDuration** : configure le nombre de minutes pendant lesquelles MED-V doit conserver l’ordinateur virtuel éveillé pour la mise à jour, en commençant à l’heure spécifiée dans le paramètre de configuration GuestUpdateTime.</span><span class="sxs-lookup"><span data-stu-id="af318-143">**GuestUpdateDuration** – Configures the number of minutes that MED-V must keep the virtual machine awake for updating, starting at the time specified in the GuestUpdateTime configuration setting.</span></span> <span data-ttu-id="af318-144">La valeur par défaut est 240 (4 heures).</span><span class="sxs-lookup"><span data-stu-id="af318-144">The default value is 240 (4 hours).</span></span> <span data-ttu-id="af318-145">Si vous définissez cette valeur sur zéro (0), la stratégie de réactivation de l’espace de travail MED-V est désactivée.</span><span class="sxs-lookup"><span data-stu-id="af318-145">Setting this value to zero (0) disables the MED-V workspace wake-up policy.</span></span>

<span data-ttu-id="af318-146">Pour plus d’informations sur la définition des valeurs de configuration de MED-V, voir [gérer les paramètres de configuration de l’espace de travail MED-v](managing-med-v-workspace-configuration-settings.md).</span><span class="sxs-lookup"><span data-stu-id="af318-146">For more information about how to define your MED-V configuration values, see [Managing MED-V Workspace Configuration Settings](managing-med-v-workspace-configuration-settings.md).</span></span>

<span data-ttu-id="af318-147">**Remarques**  Dans le cadre de la mise à jour des machines virtuelles MED-V, il est recommandé de définir votre intervalle de réveil en fonction de la date à laquelle les ordinateurs virtuels MED-V doivent être mis à jour régulièrement.</span><span class="sxs-lookup"><span data-stu-id="af318-147">**Note** A MED-V best practice is to set your wake up interval to match the time when MED-V virtual machines are planned to be updated regularly.</span></span> <span data-ttu-id="af318-148">Par ailleurs, il est recommandé de configurer ces paramètres de manière à ce qu’ils ressemblent au comportement de l’ordinateur hôte.</span><span class="sxs-lookup"><span data-stu-id="af318-148">In addition, we recommend that you configure these settings to resemble the host computer’s behavior.</span></span>

 

### <span data-ttu-id="af318-149">Redémarrez la notification à l’aide de votre système ESD</span><span class="sxs-lookup"><span data-stu-id="af318-149">Reboot Notification Using your ESD System</span></span>

<span data-ttu-id="af318-150">Vous pouvez configurer votre système de ESD pour avertir MED-V dès qu’un redémarrage est nécessaire pour l’espace de travail MED-V après l’application des mises à jour automatiques.</span><span class="sxs-lookup"><span data-stu-id="af318-150">You can configure your ESD system to notify MED-V whenever a restart is required for the MED-V workspace after automatic updates have been applied.</span></span> <span data-ttu-id="af318-151">Lorsque vous appliquez des mises à jour automatiques par le biais de votre système ESD dont vous savez qu’un redémarrage est nécessaire, vous devez écrire un script pour signaler l’événement global suivant sur l’espace de travail MED-V:</span><span class="sxs-lookup"><span data-stu-id="af318-151">When you apply automatic updates through your ESD system that you know require a restart, you should write a script to signal the following global event on the MED-V workspace:</span></span>

<span data-ttu-id="af318-152">**Important**  Vous devez ouvrir l’événement avec des droits de modification uniquement, puis le signaler.</span><span class="sxs-lookup"><span data-stu-id="af318-152">**Important** You must open the event with Modify Only rights and then signal it.</span></span> <span data-ttu-id="af318-153">Si vous ne l’ouvrez pas avec les autorisations appropriées, il ne fonctionne pas.</span><span class="sxs-lookup"><span data-stu-id="af318-153">If you do not open it with the correct permissions, it does not work.</span></span>

 

``` syntax
/// <summary>
/// The guest is required to be restarted due to an ESD update.
/// </summary>
public const string MedvGuestRebootRequiredEventName = @"Global\MedvGuestRebootRequiredEvent";
using (EventWaitHandle notificationEvent = 
EventWaitHandle.OpenExisting(eventName, EventWaitHandleRights.Modify))
{
notificationEvent.Set();
}
```

<span data-ttu-id="af318-154">Lorsque vous signalez cet événement, MED-V le capture et informe l’ordinateur virtuel qu’un redémarrage est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="af318-154">When you signal this event, MED-V captures it and informs the virtual machine that a restart is required.</span></span>

## <span data-ttu-id="af318-155">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="af318-155">Related topics</span></span>


[<span data-ttu-id="af318-156">Gestion des mises à jour de logiciels pour les espaces de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="af318-156">Managing Software Updates for MED-V Workspaces</span></span>](managing-software-updates-for-med-v-workspaces.md)

 

 





