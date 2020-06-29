---
title: Meilleures pratiques concernant MED-V2.0
description: Meilleures pratiques concernant MED-V2.0
author: dansimp
ms.assetid: 47ba2dd1-6c6e-4d6e-8e18-b42291f8e02a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7b664d33b403b821ce6bc9c045d937380ab4f91b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811561"
---
# <span data-ttu-id="d645b-103">Meilleures pratiques concernant MED-V2.0</span><span class="sxs-lookup"><span data-stu-id="d645b-103">MED-V 2.0 Best Practices</span></span>


<span data-ttu-id="d645b-104">Lors de la planification, du déploiement et de la gestion de MED-V au sein de votre entreprise, il est possible que vous trouviez les recommandations recommandées.</span><span class="sxs-lookup"><span data-stu-id="d645b-104">When you are planning, deploying, and managing MED-V in your enterprise, you may find the best practice recommendations to be useful.</span></span>

### <span data-ttu-id="d645b-105">Configurer le programme pour qu’il soit exécuté pour la première fois</span><span class="sxs-lookup"><span data-stu-id="d645b-105">Configure first time setup to run unattended</span></span>

<span data-ttu-id="d645b-106">Même si vous pouvez spécifier les paramètres de votre choix, il est recommandé de créer le fichier Sysprep. inf pour permettre l’exécution du programme d' **installation pour la** première fois.</span><span class="sxs-lookup"><span data-stu-id="d645b-106">Although you can specify any settings that you prefer, a MED-V best practice is that you create the Sysprep.inf file so that first time setup can be run in **Unattended** mode.</span></span> <span data-ttu-id="d645b-107">Pour cela, vous devez fournir toutes les informations de paramètres requises lors de la poursuite de l’Assistant gestion de l' **installation** .</span><span class="sxs-lookup"><span data-stu-id="d645b-107">This requires you to provide all the required settings information as you continue through the **Setup Manager** wizard.</span></span> <span data-ttu-id="d645b-108">Pour plus d’informations sur la configuration de l’image MED-V, voir [configuration d’une image de PC virtuel Windows pour med-v](configuring-a-windows-virtual-pc-image-for-med-v.md).</span><span class="sxs-lookup"><span data-stu-id="d645b-108">For more information about how to configure the MED-V image, see [Configuring a Windows Virtual PC Image for MED-V](configuring-a-windows-virtual-pc-image-for-med-v.md).</span></span>

### <span data-ttu-id="d645b-109">Désactiver les points de restauration sur l’ordinateur virtuel</span><span class="sxs-lookup"><span data-stu-id="d645b-109">Disable restore points on the virtual machine</span></span>

<span data-ttu-id="d645b-110">Avant de créer le package d’espace de travail MED-V, nous vous recommandons de désactiver les points de restauration sur l’ordinateur virtuel pour empêcher le disque de différenciation de croître.</span><span class="sxs-lookup"><span data-stu-id="d645b-110">Before you create the MED-V workspace package, we recommend that you disable restore points on the virtual machine to prevent the differencing disk from growing unbounded.</span></span> <span data-ttu-id="d645b-111">Pour plus d’informations, reportez-vous à la rubrique désactivation [et activation de la restauration du système dans Windows XP](https://go.microsoft.com/fwlink/?LinkId=195927) ( https://go.microsoft.com/fwlink/?LinkId=195927) .</span><span class="sxs-lookup"><span data-stu-id="d645b-111">For more information, see [How to turn off and turn on System Restore in Windows XP](https://go.microsoft.com/fwlink/?LinkId=195927) (https://go.microsoft.com/fwlink/?LinkId=195927).</span></span>

### <span data-ttu-id="d645b-112">Configurer l’image MED-V pour utiliser les profils locaux</span><span class="sxs-lookup"><span data-stu-id="d645b-112">Configure MED-V image to use local profiles</span></span>

<span data-ttu-id="d645b-113">Nous vous recommandons d’appliquer uniquement ces stratégies qui sont utiles dans un environnement de compatibilité des applications pour Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d645b-113">We recommend that you apply only those policies that make sense in an application compatibility environment for Windows XP.</span></span> <span data-ttu-id="d645b-114">Par exemple, la stratégie de personnalisation du Bureau ne doit généralement pas être appliquée et doit être désactivée.</span><span class="sxs-lookup"><span data-stu-id="d645b-114">For example, desktop customization policies do not typically have to be applied and should be disabled.</span></span> <span data-ttu-id="d645b-115">Pour plus d’informations sur la façon de n’autoriser que les profils locaux, voir [paramètres de stratégie de groupe pour les profils utilisateur errants](https://go.microsoft.com/fwlink/?LinkId=205072) ( https://go.microsoft.com/fwlink/?LinkId=205072) .</span><span class="sxs-lookup"><span data-stu-id="d645b-115">For more information about how to allow only local profiles, see [Group Policy Settings for Roaming User Profiles](https://go.microsoft.com/fwlink/?LinkId=205072) (https://go.microsoft.com/fwlink/?LinkId=205072).</span></span>

### <span data-ttu-id="d645b-116">Configurer une mise à jour de performance de la stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="d645b-116">Configure a Group Policy performance update</span></span>

<span data-ttu-id="d645b-117">Par défaut, la stratégie de groupe est téléchargée sur un ordinateur à la fois.</span><span class="sxs-lookup"><span data-stu-id="d645b-117">By default, Group Policy is downloaded to a computer one byte at a time.</span></span> <span data-ttu-id="d645b-118">Cela entraîne des retards lorsque MED-V est joint au domaine.</span><span class="sxs-lookup"><span data-stu-id="d645b-118">This causes delays when MED-V is being joined to the domain.</span></span> <span data-ttu-id="d645b-119">Pour améliorer les performances de la stratégie de groupe, nous vous conseillons de définir la valeur de clé de Registre suivante sur le registre:</span><span class="sxs-lookup"><span data-stu-id="d645b-119">To increase the performance of Group Policy, we recommend that you set the following registry key value to the registry:</span></span>

<span data-ttu-id="d645b-120">Sous-clé de Registre: HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Winlogon</span><span class="sxs-lookup"><span data-stu-id="d645b-120">Registry subkey: HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Winlogon</span></span>

<span data-ttu-id="d645b-121">Entrée: BufferPolicyReads</span><span class="sxs-lookup"><span data-stu-id="d645b-121">Entry: BufferPolicyReads</span></span>

<span data-ttu-id="d645b-122">Type: DWORD</span><span class="sxs-lookup"><span data-stu-id="d645b-122">Type: DWORD</span></span>

<span data-ttu-id="d645b-123">Valeur : 1</span><span class="sxs-lookup"><span data-stu-id="d645b-123">Value: 1</span></span>

### <span data-ttu-id="d645b-124">Distribuer un avis légal par le biais d’une stratégie de groupe plutôt que dans l’image MED-V</span><span class="sxs-lookup"><span data-stu-id="d645b-124">Distribute legal notice through Group Policy instead of in the MED-V image</span></span>

<span data-ttu-id="d645b-125">Si vous souhaitez que les utilisateurs finaux puissent voir un contrat de niveau de service (SLA) avant d’accéder à MED-V, nous vous recommandons d’appliquer le SLA par le biais de la stratégie de groupe, de façon à ce qu’il soit présenté à l’utilisateur final une fois la première configuration terminée.</span><span class="sxs-lookup"><span data-stu-id="d645b-125">If you want end users to see a service level agreement (SLA) before they access MED-V, we recommend that you enforce the SLA through Group Policy later so that the SLA is displayed to the end user after the first time setup is finished.</span></span>

<span data-ttu-id="d645b-126">**Attention**  Même s’il est préférable d’exécuter la première configuration en mode **sans assistance** , si vous décidez de définir la stratégie locale ou l’entrée de Registre afin d’inclure un SLA dans votre image (disque dur virtuel), vous devez également spécifier la première fois que le programme d’installation s’exécute en mode **assisté** ou si le programme d’installation peut échouer.</span><span class="sxs-lookup"><span data-stu-id="d645b-126">**Caution** Even though a best practice is to run first time setup in **Unattended** mode, if you decide to set the local policy or registry entry to include an SLA in your image (virtual hard disk), you must also specify that first time setup is run in **Attended** mode, or first time setup can fail.</span></span>

 

### <span data-ttu-id="d645b-127">Compactez le disque dur virtuel</span><span class="sxs-lookup"><span data-stu-id="d645b-127">Compact the virtual hard disk</span></span>

<span data-ttu-id="d645b-128">Nous vous recommandons de compacter votre disque dur virtuel pour récupérer l’espace libre sur le disque et de réduire la taille du disque dur virtuel.</span><span class="sxs-lookup"><span data-stu-id="d645b-128">We recommend that you compact your virtual hard disk to reclaim empty disk space and reduce the size of the virtual hard disk.</span></span> <span data-ttu-id="d645b-129">Pour plus d’informations sur la façon de compacter votre disque dur virtuel, voir [compactage du disque dur virtuel MED-V](compacting-the-med-v-virtual-hard-disk.md).</span><span class="sxs-lookup"><span data-stu-id="d645b-129">For more information about how to compact your virtual hard disk, see [Compacting the MED-V Virtual Hard Disk](compacting-the-med-v-virtual-hard-disk.md).</span></span>

### <span data-ttu-id="d645b-130">Configurer l’ordinateur virtuel pour qu’il redémarre sur écran bleu</span><span class="sxs-lookup"><span data-stu-id="d645b-130">Configure virtual machine to restart on blue screen crash</span></span>

<span data-ttu-id="d645b-131">Nous vous recommandons de configurer l’ordinateur virtuel de l’espace de travail MED-V de façon à ce qu’il se bloque automatiquement lorsqu’il rencontre un blocage de l’écran bleu.</span><span class="sxs-lookup"><span data-stu-id="d645b-131">We recommend that you configure the MED-V workspace virtual machine to automatically restart when it encounters a blue screen crash.</span></span> <span data-ttu-id="d645b-132">Pour configurer ce paramètre dans l’invité, définissez la valeur de redémarrage dans la clé HKEY \ _LOCAL \ _MACHINE \\SYSTEM\\CurrentControlSet\\Control\\CrashControl sur «1».</span><span class="sxs-lookup"><span data-stu-id="d645b-132">To configure this setting in the guest, set the AutoReboot value in the HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Control\\CrashControl key to “1”.</span></span>

<span data-ttu-id="d645b-133">Vous pouvez également configurer ce paramètre en cliquant sur **Démarrer**, puis sur **panneau**de configuration et sur **système**.</span><span class="sxs-lookup"><span data-stu-id="d645b-133">You can also configure this setting by clicking **Start**, clicking **Control Panel**, and then clicking **System**.</span></span> <span data-ttu-id="d645b-134">Ensuite, dans la zone **démarrage et récupération** de l’onglet **avancé** , cliquez sur **paramètres**.</span><span class="sxs-lookup"><span data-stu-id="d645b-134">Then, in the **Startup and Recovery** area of the **Advanced** tab, click **Settings**.</span></span> <span data-ttu-id="d645b-135">Cochez la case **redémarrer automatiquement** , puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="d645b-135">Select the **Automatically restart** check box and click **OK**.</span></span>

### <span data-ttu-id="d645b-136">Sauvegarder l’image MED-V avant de la sceller</span><span class="sxs-lookup"><span data-stu-id="d645b-136">Back up MED-V image before sealing it</span></span>

<span data-ttu-id="d645b-137">Nous vous recommandons de créer une copie de sauvegarde de l’image MED-V avant de la sceller.</span><span class="sxs-lookup"><span data-stu-id="d645b-137">We recommend that you create a backup copy of the MED-V image before you seal it.</span></span> <span data-ttu-id="d645b-138">Pour plus d’informations sur la façon de sceller votre image MED-V, voir [configurer une image de PC virtuel Windows pour med-v](configuring-a-windows-virtual-pc-image-for-med-v.md).</span><span class="sxs-lookup"><span data-stu-id="d645b-138">For more information about sealing your MED-V image, see [Configuring a Windows Virtual PC Image for MED-V](configuring-a-windows-virtual-pc-image-for-med-v.md).</span></span>

### <span data-ttu-id="d645b-139">Installer le PC virtuel Windows en dernier lors de l’installation à partir d’un fichier de commandes</span><span class="sxs-lookup"><span data-stu-id="d645b-139">Install Windows Virtual PC last when installing from a batch file</span></span>

<span data-ttu-id="d645b-140">Lorsque vous installez les composants MED-V à l’aide d’un fichier de commandes, spécifiez que le PC virtuel Windows et le correctif Windows Virtual PC sont installés après l’agent d’hébergement MED-v et les fichiers de package d’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="d645b-140">When you install the MED-V components by using a batch file, specify that Windows Virtual PC and the Windows Virtual PC hotfix are installed after the MED-V Host Agent and the MED-V workspace package files.</span></span> <span data-ttu-id="d645b-141">Cela permet de s’assurer que Windows Update n’entraîne aucune interférence avec le processus d’installation en nécessitant un redémarrage.</span><span class="sxs-lookup"><span data-stu-id="d645b-141">This ensures that Windows Update will not cause any interference with the installation process by requiring a restart.</span></span>

### <span data-ttu-id="d645b-142">Installer l’espace de travail MED-V à partir du dossier local</span><span class="sxs-lookup"><span data-stu-id="d645b-142">Install MED-V workspace from local folder</span></span>

<span data-ttu-id="d645b-143">En raison de problèmes qui peuvent survenir lors de l’installation de MED-V à partir d’un emplacement réseau, il est recommandé de copier les fichiers de configuration de l’espace de travail MED-V localement, puis d’exécuter setup.exe.</span><span class="sxs-lookup"><span data-stu-id="d645b-143">Because of problems that can occur when you install MED-V from a network location, we recommend that you copy the MED-V workspace setup files locally and then run setup.exe.</span></span>

### <a href="" id="manage-printer-redirection-in-one-manner-only-"></a><span data-ttu-id="d645b-144">Gestion de la redirection d’imprimante en une seule fois</span><span class="sxs-lookup"><span data-stu-id="d645b-144">Manage printer redirection in one manner only</span></span>

<span data-ttu-id="d645b-145">Si une imprimante est installée manuellement sur l’ordinateur virtuel de l’invité MED-V et si la même imprimante est installée sur l’ordinateur hôte, le résultat est qu’il est installé à deux reprises dans l’invité.</span><span class="sxs-lookup"><span data-stu-id="d645b-145">If a printer is manually installed on the MED-V guest virtual machine, and the same printer is later installed on the host computer, the result is that it is installed two times in the guest.</span></span> <span data-ttu-id="d645b-146">Pour éviter ce problème, nous vous recommandons d’utiliser la meilleure pratique MED-V pour gérer la redirection d’imprimante en une seule fois: désactivez la redirection et l’installation manuelle de l’imprimante sur l’invité ou activez la redirection et n’installez pas les imprimantes manuellement sur l’invité.</span><span class="sxs-lookup"><span data-stu-id="d645b-146">To avoid this situation, we recommend as MED-V best practice that you manage printer redirection in one manner only: either disable redirection and install printers manually on the guest, or enable redirection and do not install printers manually on the guest.</span></span>

### <a href="" id="configure-settings-for-med-v-guest-patching-"></a><span data-ttu-id="d645b-147">Configurer les paramètres pour la mise à jour d’invité MED-V</span><span class="sxs-lookup"><span data-stu-id="d645b-147">Configure settings for MED-V guest patching</span></span>

<span data-ttu-id="d645b-148">Vous pouvez contrôler quand et Pendant combien de temps la machine virtuelle MED-V s’est désréveillé pour recevoir des mises à jour automatiques en définissant les valeurs de configuration pertinentes dans le registre.</span><span class="sxs-lookup"><span data-stu-id="d645b-148">You can control when and for how long the MED-V virtual machine awakens to receive automatic updates by defining the relevant configuration values in the registry.</span></span> <span data-ttu-id="d645b-149">Dans le cadre de la meilleure pratique MED-V, vous devez configurer votre intervalle de mise en éveil pour qu’il corresponde à l’heure à laquelle vous avez planifié des mises à jour régulières des machines virtuelles MED-V.</span><span class="sxs-lookup"><span data-stu-id="d645b-149">A MED-V best practice is to set your wake-up interval to match the time when you have scheduled regular updates for MED-V virtual machines.</span></span> <span data-ttu-id="d645b-150">Par ailleurs, il est recommandé de configurer ces paramètres de manière à ce qu’ils ressemblent au comportement de l’ordinateur hôte.</span><span class="sxs-lookup"><span data-stu-id="d645b-150">In addition, we recommend that you configure these settings to resemble the host computer’s behavior.</span></span>

<span data-ttu-id="d645b-151">Pour plus d’informations sur la configuration des paramètres de correction d’invité MED-V, voir [gestion des mises à jour automatiques pour les espaces de travail MED-v](managing-automatic-updates-for-med-v-workspaces.md).</span><span class="sxs-lookup"><span data-stu-id="d645b-151">For more information about how to configure settings for MED-V guest patching, see [Managing Automatic Updates for MED-V Workspaces](managing-automatic-updates-for-med-v-workspaces.md).</span></span>

### <span data-ttu-id="d645b-152">Configurer un logiciel antivirus/de sauvegarde</span><span class="sxs-lookup"><span data-stu-id="d645b-152">Configure antivirus/backup software</span></span>

<span data-ttu-id="d645b-153">Pour empêcher l’activité de l’antivirus d’affecter les performances du bureau virtuel, nous vous conseillons de le faire à l’exclusion des types de fichiers d’ordinateur virtuel suivants de tout logiciel antivirus ou de processus de sauvegarde qui s’exécute sur l’ordinateur hôte MED-V:</span><span class="sxs-lookup"><span data-stu-id="d645b-153">To prevent antivirus activity from affecting the performance of the virtual desktop, we recommend that when you can, you exclude the following virtual machine file types from any antivirus or backup process that is running on the MED-V host computer:</span></span>

-   <span data-ttu-id="d645b-154">\*. COMPATIBLE</span><span class="sxs-lookup"><span data-stu-id="d645b-154">\*.VMC</span></span>

-   <span data-ttu-id="d645b-155">\*. VUD</span><span class="sxs-lookup"><span data-stu-id="d645b-155">\*.VUD</span></span>

-   <span data-ttu-id="d645b-156">\*. VSV</span><span class="sxs-lookup"><span data-stu-id="d645b-156">\*.VSV</span></span>

-   <span data-ttu-id="d645b-157">\*. VIRTUELS</span><span class="sxs-lookup"><span data-stu-id="d645b-157">\*.VHD</span></span>

## <span data-ttu-id="d645b-158">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d645b-158">Related topics</span></span>


[<span data-ttu-id="d645b-159">Sécurité et protection de MED-V</span><span class="sxs-lookup"><span data-stu-id="d645b-159">Security and Protection for MED-V</span></span>](security-and-protection-for-med-v.md)

 

 





