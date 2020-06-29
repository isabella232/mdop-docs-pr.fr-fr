---
title: Déploiement du client MBAM dans le cadre d'un déploiement de Windows
description: Déploiement du client MBAM dans le cadre d'un déploiement de Windows
author: dansimp
ms.assetid: 8704bf33-535d-41da-b9b2-45b60754367e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a63311bcc93d84472ceff5c80c9222fefd5445c0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810841"
---
# <span data-ttu-id="f65e5-103">Déploiement du client MBAM dans le cadre d'un déploiement de Windows</span><span class="sxs-lookup"><span data-stu-id="f65e5-103">How to Deploy the MBAM Client as Part of a Windows Deployment</span></span>


<span data-ttu-id="f65e5-104">Le client Microsoft BitLocker Administration and Analysis (MBAM) permet aux administrateurs d’appliquer et de surveiller le chiffrement de lecteur BitLocker sur les ordinateurs de l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="f65e5-104">The Microsoft BitLocker Administration and Monitoring (MBAM) Client enables administrators to enforce and monitor BitLocker drive encryption on computers in the enterprise.</span></span> <span data-ttu-id="f65e5-105">Le client BitLocker peut être intégré au sein d’une organisation en activant la gestion et le chiffrement de BitLocker sur les ordinateurs clients lors du processus de déploiement d’images et Windows.</span><span class="sxs-lookup"><span data-stu-id="f65e5-105">The BitLocker Client can be integrated into an organization by enabling BitLocker management and encryption on client computers during the computer imaging and Windows deployment process.</span></span>

**<span data-ttu-id="f65e5-106">Remarque</span><span class="sxs-lookup"><span data-stu-id="f65e5-106">Note</span></span>**  
<span data-ttu-id="f65e5-107">Pour vérifier la configuration système requise pour le client MBAM, voir [Configurations prises en charge par MBAM 1,0](mbam-10-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="f65e5-107">To review the MBAM Client system requirements, see [MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md).</span></span>



<span data-ttu-id="f65e5-108">Le chiffrement d’ordinateurs clients avec BitLocker lors de la phase d’imagerie initiale d’un déploiement de Windows peut réduire la surcharge d’administration de l’implémentation de MBAM.</span><span class="sxs-lookup"><span data-stu-id="f65e5-108">Encryption of client computers with BitLocker during the initial imaging stage of a Windows deployment can lower the administrative overhead for MBAM implementation.</span></span> <span data-ttu-id="f65e5-109">Cette approche permet également de s’assurer que chaque ordinateur déployé possède déjà BitLocker et qu’il est configuré correctement.</span><span class="sxs-lookup"><span data-stu-id="f65e5-109">This approach also ensures that every computer that is deployed already has BitLocker running and is configured correctly.</span></span>

**<span data-ttu-id="f65e5-110">Warning</span><span class="sxs-lookup"><span data-stu-id="f65e5-110">Warning</span></span>**  
<span data-ttu-id="f65e5-111">Cette rubrique explique comment modifier le Registre Windows à l’aide de l’éditeur du Registre.</span><span class="sxs-lookup"><span data-stu-id="f65e5-111">This topic describes how to change the Windows registry by using Registry Editor.</span></span> <span data-ttu-id="f65e5-112">Si vous modifiez la clé de registre de Windows de manière incorrecte, vous pouvez être à l’origine de problèmes importants qui peuvent nécessiter la réinstallation de Windows.</span><span class="sxs-lookup"><span data-stu-id="f65e5-112">If you change the Windows registry incorrectly, you can cause serious problems that might require you to reinstall Windows.</span></span> <span data-ttu-id="f65e5-113">Vous devez faire une copie de sauvegarde des fichiers du Registre (System. dat et User. dat) avant de modifier le registre.</span><span class="sxs-lookup"><span data-stu-id="f65e5-113">You should make a backup copy of the registry files (System.dat and User.dat) before you change the registry.</span></span> <span data-ttu-id="f65e5-114">Microsoft ne peut pas garantir que les problèmes qui peuvent survenir lorsque vous modifiez le registre peuvent être résolus.</span><span class="sxs-lookup"><span data-stu-id="f65e5-114">Microsoft cannot guarantee that the problems that might occur when you change the registry can be resolved.</span></span> <span data-ttu-id="f65e5-115">Changez de Registre à vos propres risques.</span><span class="sxs-lookup"><span data-stu-id="f65e5-115">Change the registry at your own risk.</span></span>



**<span data-ttu-id="f65e5-116">Pour chiffrer un ordinateur dans le cadre du déploiement Windows</span><span class="sxs-lookup"><span data-stu-id="f65e5-116">To encrypt a computer as part of Windows deployment</span></span>**

1.  <span data-ttu-id="f65e5-117">Si votre organisation envisage d’utiliser le protecteur de module de plateforme sécurisée (TPM) ou les options de protecteur de TPM + PIN dans BitLocker, vous devez activer le processeur du TPM avant le déploiement initial d’MBAM.</span><span class="sxs-lookup"><span data-stu-id="f65e5-117">If your organization plans to use the Trusted Platform Module (TPM) protector or the TPM + PIN protector options in BitLocker, you must activate the TPM chip before the initial deployment of MBAM.</span></span> <span data-ttu-id="f65e5-118">Lorsque vous activez le processeur du TPM, vous évitez un redémarrage ultérieur dans le processus et vous vous assurez que les puces du TPM sont correctement configurées conformément aux exigences de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="f65e5-118">When you activate the TPM chip, you avoid a reboot later in the process, and you ensure that the TPM chips are correctly configured according to the requirements of your organization.</span></span> <span data-ttu-id="f65e5-119">Vous devez activer manuellement le processeur du TPM dans le BIOS de votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="f65e5-119">You must activate the TPM chip manually in the computer's BIOS.</span></span> <span data-ttu-id="f65e5-120">Pour plus d’informations sur la façon de configurer le processeur du TPM, consultez la documentation fournie par le fabricant.</span><span class="sxs-lookup"><span data-stu-id="f65e5-120">Refer to the manufacturer documentation for more details about how to configure the TPM chip.</span></span>

2.  <span data-ttu-id="f65e5-121">Installez l’agent client MBAM.</span><span class="sxs-lookup"><span data-stu-id="f65e5-121">Install the MBAM client agent.</span></span>

3.  <span data-ttu-id="f65e5-122">Nous vous recommandons de joindre l’ordinateur à un domaine...</span><span class="sxs-lookup"><span data-stu-id="f65e5-122">We recommend that you join the computer to a domain...</span></span>

    -   <span data-ttu-id="f65e5-123">Si l’ordinateur n’est pas joint à un domaine, le mot de passe de récupération n’est pas stocké dans le service de récupération de clé MBAM.</span><span class="sxs-lookup"><span data-stu-id="f65e5-123">If the computer is not joined to a domain, the recovery password is not stored in the MBAM Key Recovery service.</span></span> <span data-ttu-id="f65e5-124">Par défaut, MBAM ne permet pas d’effectuer le chiffrement, sauf si la clé de récupération peut être stockée.</span><span class="sxs-lookup"><span data-stu-id="f65e5-124">By default, MBAM does not allow encryption to occur unless the recovery key can be stored.</span></span>

    -   <span data-ttu-id="f65e5-125">Si un ordinateur démarre en mode de récupération avant que la clé de récupération ne soit stockée sur le serveur MBAM, l’ordinateur doit être rephoto.</span><span class="sxs-lookup"><span data-stu-id="f65e5-125">If a computer starts in recovery mode before the recovery key is stored on the MBAM server, the computer has to be reimaged.</span></span> <span data-ttu-id="f65e5-126">Aucune méthode de récupération n’est disponible.</span><span class="sxs-lookup"><span data-stu-id="f65e5-126">No recovery method is available.</span></span>

4.  <span data-ttu-id="f65e5-127">Ouvrez une invite de commandes en tant qu’administrateur, arrêtez le service MBAM, puis définissez le service sur **Manuel** ou à **la demande**.</span><span class="sxs-lookup"><span data-stu-id="f65e5-127">Open a command prompt as an administrator, stop the MBAM service, and then set the service to **manual** or **on demand**.</span></span> <span data-ttu-id="f65e5-128">Exécutez ensuite les commandes suivantes:</span><span class="sxs-lookup"><span data-stu-id="f65e5-128">Then, run the following commands:</span></span>

    **<span data-ttu-id="f65e5-129">net stop mbamagent</span><span class="sxs-lookup"><span data-stu-id="f65e5-129">net stop mbamagent</span></span>**

    **<span data-ttu-id="f65e5-130">sc config mbamagent Start = Demand</span><span class="sxs-lookup"><span data-stu-id="f65e5-130">sc config mbamagent start= demand</span></span>**

5.  <span data-ttu-id="f65e5-131">Définissez les paramètres de registre de l’agent MBAM pour qu’il ignore les stratégies de groupe et exécutez le module de plateforme sécurisée pour le **système d’exploitation uniquement le chiffrement** pour effectuer cette opération, exécutez **regedit**, puis importez le modèle de clé de Registre à partir de C:\\Program Files\\Microsoft\\MDOP MBAM\\MBAMDeploymentKeyTemplate.reg.</span><span class="sxs-lookup"><span data-stu-id="f65e5-131">Set the registry settings for the MBAM agent to ignore Group Policy and run the TPM for **operating system only encryption** To do this, run **regedit**, and then import the registry key template from C:\\Program Files\\Microsoft\\MDOP MBAM\\MBAMDeploymentKeyTemplate.reg.</span></span>

6.  <span data-ttu-id="f65e5-132">Dans Regedit, accédez à HKLM\\SOFTWARE\\Microsoft\\MBAM et configurez les paramètres indiqués dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="f65e5-132">In regedit, go to HKLM\\SOFTWARE\\Microsoft\\MBAM and configure the settings that are listed in the following table.</span></span>

    <span data-ttu-id="f65e5-133">Entrée du Registre</span><span class="sxs-lookup"><span data-stu-id="f65e5-133">Registry entry</span></span>

    <span data-ttu-id="f65e5-134">Paramètres de configuration</span><span class="sxs-lookup"><span data-stu-id="f65e5-134">Configuration settings</span></span>

    <span data-ttu-id="f65e5-135">DeploymentTime</span><span class="sxs-lookup"><span data-stu-id="f65e5-135">DeploymentTime</span></span>

    <span data-ttu-id="f65e5-136">0 = DÉSACTIVÉ</span><span class="sxs-lookup"><span data-stu-id="f65e5-136">0 = OFF</span></span>

    <span data-ttu-id="f65e5-137">1 = utiliser les paramètres de stratégie de moment de déploiement (par défaut)</span><span class="sxs-lookup"><span data-stu-id="f65e5-137">1 = Use deployment time policy settings (default)</span></span>

    <span data-ttu-id="f65e5-138">UseKeyRecoveryService</span><span class="sxs-lookup"><span data-stu-id="f65e5-138">UseKeyRecoveryService</span></span>

    <span data-ttu-id="f65e5-139">0 = ne pas utiliser le tiers de confiance principal (les deux entrées de Registre suivantes ne sont pas requises dans le cas présent).</span><span class="sxs-lookup"><span data-stu-id="f65e5-139">0 = Do not use key escrow (The next two registry entries are not required in this case.)</span></span>

    <span data-ttu-id="f65e5-140">1 = utiliser le tiers de confiance principal dans le système de récupération de clés (par défaut)</span><span class="sxs-lookup"><span data-stu-id="f65e5-140">1 = Use key escrow in Key Recovery system (default)</span></span>

    <span data-ttu-id="f65e5-141">Recommandé: l’ordinateur doit pouvoir communiquer avec le service de récupération de clés.</span><span class="sxs-lookup"><span data-stu-id="f65e5-141">Recommended: The computer must be able to communicate with the Key Recovery service.</span></span> <span data-ttu-id="f65e5-142">Vérifiez que l’ordinateur peut communiquer avec le service avant de continuer.</span><span class="sxs-lookup"><span data-stu-id="f65e5-142">Verify that the computer can communicate with the service before you proceed.</span></span>

    <span data-ttu-id="f65e5-143">KeyRecoveryOptions</span><span class="sxs-lookup"><span data-stu-id="f65e5-143">KeyRecoveryOptions</span></span>

    <span data-ttu-id="f65e5-144">0 = Télécharger la clé de récupération uniquement</span><span class="sxs-lookup"><span data-stu-id="f65e5-144">0 = Upload Recovery Key Only</span></span>

    <span data-ttu-id="f65e5-145">1 = Télécharger la clé de récupération et le package de récupération de clé (par défaut)</span><span class="sxs-lookup"><span data-stu-id="f65e5-145">1 = Upload Recovery Key and Key Recovery Package (default)</span></span>

    <span data-ttu-id="f65e5-146">KeyRecoveryServiceEndPoint</span><span class="sxs-lookup"><span data-stu-id="f65e5-146">KeyRecoveryServiceEndPoint</span></span>

    <span data-ttu-id="f65e5-147">Définissez cette valeur sur l’URL du serveur Web de récupération de clés.</span><span class="sxs-lookup"><span data-stu-id="f65e5-147">Set this value to the URL for the Key Recovery web server.</span></span>

    <span data-ttu-id="f65e5-148">Par exemple: http:// &lt; nom d’ordinateur &gt; /MBAMRecoveryAndHardwareService/CoreService.svc.</span><span class="sxs-lookup"><span data-stu-id="f65e5-148">Example: http://&lt;computer name&gt;/MBAMRecoveryAndHardwareService/CoreService.svc.</span></span>



~~~
**Note**  
MBAM policy or registry values can be set here to override the previously set values.
~~~



7. <span data-ttu-id="f65e5-149">L’agent MBAM redémarre le système lors du déploiement du client MBAM.</span><span class="sxs-lookup"><span data-stu-id="f65e5-149">The MBAM agent restarts the system during MBAM client deployment.</span></span> <span data-ttu-id="f65e5-150">Lorsque vous êtes prêt à redémarrer, exécutez la commande suivante à l’invite de commandes en tant qu’administrateur:</span><span class="sxs-lookup"><span data-stu-id="f65e5-150">When you are ready for this reboot, run the following command at a command prompt as an administrator:</span></span>

   **<span data-ttu-id="f65e5-151">mbamagent de début net</span><span class="sxs-lookup"><span data-stu-id="f65e5-151">net start mbamagent</span></span>**

8. <span data-ttu-id="f65e5-152">Au redémarrage de l’ordinateur et le BIOS vous demande d’accepter un changement de TPM, acceptez la modification.</span><span class="sxs-lookup"><span data-stu-id="f65e5-152">When the computers restarts and the BIOS prompts you to accept a TPM change, accept the change.</span></span>

9. <span data-ttu-id="f65e5-153">Pendant le processus d’imagerie du système d’exploitation du client Windows, lorsque vous êtes prêt à commencer le chiffrement, redémarrez le service de l’agent MBAM.</span><span class="sxs-lookup"><span data-stu-id="f65e5-153">During the Windows client operating system imaging process, when you are ready to start encryption, restart the MBAM agent service.</span></span> <span data-ttu-id="f65e5-154">Pour définir l’option de démarrage **automatique**, ouvrez une invite de commandes en tant qu’administrateur et exécutez les commandes suivantes:</span><span class="sxs-lookup"><span data-stu-id="f65e5-154">Then, to set start to **automatic**, open a command prompt as an administrator and run the following commands:</span></span>

   **<span data-ttu-id="f65e5-155">sc config mbamagent start = auto</span><span class="sxs-lookup"><span data-stu-id="f65e5-155">sc config mbamagent start= auto</span></span>**

   **<span data-ttu-id="f65e5-156">mbamagent de début net</span><span class="sxs-lookup"><span data-stu-id="f65e5-156">net start mbamagent</span></span>**

10. <span data-ttu-id="f65e5-157">Supprimez les valeurs de Registre Bypass.</span><span class="sxs-lookup"><span data-stu-id="f65e5-157">Remove the bypass registry values.</span></span> <span data-ttu-id="f65e5-158">Pour cela, exécutez regedit, accédez à l’entrée de Registre HKLM\\SOFTWARE\\Microsoft, cliquez avec le bouton droit sur le nœud **MBAM** , puis cliquez sur **supprimer**.</span><span class="sxs-lookup"><span data-stu-id="f65e5-158">To do this, run regedit, browse to the HKLM\\SOFTWARE\\Microsoft registry entry, right-click the **MBAM** node, and then click **Delete**.</span></span>

## <span data-ttu-id="f65e5-159">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f65e5-159">Related topics</span></span>


[<span data-ttu-id="f65e5-160">Déploiement du client MBAM1.0</span><span class="sxs-lookup"><span data-stu-id="f65e5-160">Deploying the MBAM 1.0 Client</span></span>](deploying-the-mbam-10-client.md)









