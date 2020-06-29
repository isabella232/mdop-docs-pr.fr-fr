---
title: Déploiement du client MBAM dans le cadre d'un déploiement de Windows
description: Déploiement du client MBAM dans le cadre d'un déploiement de Windows
author: dansimp
ms.assetid: 67387de7-8b02-4412-9850-3b8d8e5c18af
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d75e5748167d2d4866f98e9d3611584067ecd418
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810667"
---
# <span data-ttu-id="50f33-103">Déploiement du client MBAM dans le cadre d'un déploiement de Windows</span><span class="sxs-lookup"><span data-stu-id="50f33-103">How to Deploy the MBAM Client as Part of a Windows Deployment</span></span>


<span data-ttu-id="50f33-104">Le client Microsoft BitLocker Administration and Analysis (MBAM) permet aux administrateurs d’appliquer et de surveiller le chiffrement de lecteur BitLocker sur les ordinateurs de l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="50f33-104">The Microsoft BitLocker Administration and Monitoring (MBAM) Client enables administrators to enforce and monitor BitLocker drive encryption on computers in the enterprise.</span></span> <span data-ttu-id="50f33-105">Si les ordinateurs disposant d’une puce de module de plateforme sécurisée (TPM), le client BitLocker peut être intégré au sein d’une organisation en activant la gestion et le chiffrement de BitLocker sur les ordinateurs clients dans le cadre du processus de déploiement d’imagerie et Windows.</span><span class="sxs-lookup"><span data-stu-id="50f33-105">If computers that have a Trusted Platform Module (TPM) chip, the BitLocker client can be integrated into an organization by enabling BitLocker management and encryption on client computers as part of the imaging and Windows deployment process.</span></span>

**<span data-ttu-id="50f33-106">Remarque</span><span class="sxs-lookup"><span data-stu-id="50f33-106">Note</span></span>**  
<span data-ttu-id="50f33-107">Pour vérifier la configuration système requise pour le client d’administration et de surveillance de BitLocker, voir [Configurations prises en charge par MBAM 2,0](mbam-20-supported-configurations-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="50f33-107">To review the Microsoft BitLocker Administration and Monitoring Client system requirements, see [MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md).</span></span>



<span data-ttu-id="50f33-108">Le chiffrement d’ordinateurs clients avec BitLocker lors de la phase d’imagerie initiale d’un déploiement Windows peut réduire la surcharge administrative nécessaire pour implémenter MBAM au sein d’une organisation.</span><span class="sxs-lookup"><span data-stu-id="50f33-108">Encrypting client computers with BitLocker during the initial imaging stage of a Windows deployment can lower the administrative overhead necessary for implementing MBAM in an organization.</span></span> <span data-ttu-id="50f33-109">Cela permet également de s’assurer que chaque ordinateur déployé possède déjà BitLocker et qu’il est configuré correctement.</span><span class="sxs-lookup"><span data-stu-id="50f33-109">It also ensures that every computer that is deployed already has BitLocker running and is configured correctly.</span></span>

**<span data-ttu-id="50f33-110">Remarque</span><span class="sxs-lookup"><span data-stu-id="50f33-110">Note</span></span>**  
<span data-ttu-id="50f33-111">La procédure décrite dans cette rubrique décrit la modification du Registre Windows.</span><span class="sxs-lookup"><span data-stu-id="50f33-111">The procedure in this topic describes modifying the Windows registry.</span></span> <span data-ttu-id="50f33-112">L’utilisation de l’éditeur du Registre peut être à l’origine de problèmes importants qui peuvent nécessiter la réinstallation de Windows.</span><span class="sxs-lookup"><span data-stu-id="50f33-112">Using Registry Editor incorrectly can cause serious problems that may require you to reinstall Windows.</span></span> <span data-ttu-id="50f33-113">Microsoft ne peut pas garantir que les problèmes résultant de l’utilisation incorrecte de l’éditeur du Registre peuvent être résolus.</span><span class="sxs-lookup"><span data-stu-id="50f33-113">Microsoft cannot guarantee that problems resulting from the incorrect use of Registry Editor can be solved.</span></span> <span data-ttu-id="50f33-114">Utilisez l’éditeur du Registre à vos propres risques.</span><span class="sxs-lookup"><span data-stu-id="50f33-114">Use Registry Editor at your own risk.</span></span>



**<span data-ttu-id="50f33-115">Pour chiffrer un ordinateur dans le cadre du déploiement Windows</span><span class="sxs-lookup"><span data-stu-id="50f33-115">To encrypt a computer as part of Windows deployment</span></span>**

1.  <span data-ttu-id="50f33-116">Si votre organisation envisagez d’utiliser le protecteur de module de plateforme sécurisée (TPM) ou les options de protecteur de TPM + PIN dans BitLocker, vous devez activer le processeur du TPM avant le déploiement initial de MBAM.</span><span class="sxs-lookup"><span data-stu-id="50f33-116">If your organization is planning to use the Trusted Platform Module (TPM) protector or the TPM + PIN protector options in BitLocker, you must activate the TPM chip before the initial deployment of MBAM.</span></span> <span data-ttu-id="50f33-117">Lorsque vous activez le processeur du TPM, vous évitez un redémarrage ultérieur dans le processus et vous vous assurez que les puces du TPM sont correctement configurées conformément aux exigences de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="50f33-117">When you activate the TPM chip, you avoid a reboot later in the process, and you ensure that the TPM chips are correctly configured according to the requirements of your organization.</span></span> <span data-ttu-id="50f33-118">Vous devez activer manuellement le processeur du TPM dans le BIOS de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="50f33-118">You must activate the TPM chip manually in the BIOS of the computer.</span></span>

    **<span data-ttu-id="50f33-119">Remarque</span><span class="sxs-lookup"><span data-stu-id="50f33-119">Note</span></span>**  
    <span data-ttu-id="50f33-120">Certains fournisseurs fournissent des outils permettant d’activer et d’activer le processeur du TPM dans le BIOS à partir du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="50f33-120">Some vendors provide tools to turn on and activate the TPM chip in the BIOS from within the operating system.</span></span> <span data-ttu-id="50f33-121">Pour plus d’informations sur la façon de configurer le processeur du TPM, consultez la documentation fournie par le fabricant.</span><span class="sxs-lookup"><span data-stu-id="50f33-121">Refer to the manufacturer documentation for more details about how to configure the TPM chip.</span></span>



2.  <span data-ttu-id="50f33-122">Installez l’agent client d’administration et de contrôle Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="50f33-122">Install the Microsoft BitLocker Administration and Monitoring client agent.</span></span>

3.  <span data-ttu-id="50f33-123">Rejoignez l’ordinateur à un domaine (recommandé).</span><span class="sxs-lookup"><span data-stu-id="50f33-123">Join the computer to a domain (recommended).</span></span>

    -   <span data-ttu-id="50f33-124">Si l’ordinateur n’est pas joint au domaine, le mot de passe de récupération n’est pas stocké dans le service de récupération de clé MBAM.</span><span class="sxs-lookup"><span data-stu-id="50f33-124">If the computer is not joined to the domain, the recovery password is not stored in the MBAM Key Recovery service.</span></span> <span data-ttu-id="50f33-125">Par défaut, MBAM ne permet pas d’effectuer le chiffrement, sauf si la clé de récupération peut être stockée.</span><span class="sxs-lookup"><span data-stu-id="50f33-125">By default, MBAM does not allow encryption to occur unless the recovery key can be stored.</span></span>

    -   <span data-ttu-id="50f33-126">Si un ordinateur démarre en mode de récupération avant que la clé de récupération ne soit stockée sur le serveur MBAM, l’ordinateur doit être rephoto.</span><span class="sxs-lookup"><span data-stu-id="50f33-126">If a computer starts in recovery mode before the recovery key is stored on the MBAM Server, the computer has to be reimaged.</span></span> <span data-ttu-id="50f33-127">Aucune méthode de récupération n’est disponible.</span><span class="sxs-lookup"><span data-stu-id="50f33-127">No recovery method is available.</span></span>

4.  <span data-ttu-id="50f33-128">Exécutez l’invite de commandes en tant qu’administrateur, arrêtez le service MBAM, puis définissez le service sur **Manuel** ou à **la demande**, puis commencez par taper les commandes suivantes:</span><span class="sxs-lookup"><span data-stu-id="50f33-128">Run the command prompt as an administrator, stop the MBAM service, and then set the service to **manual** or **on demand**, and then start by typing the following commands:</span></span>

    **<span data-ttu-id="50f33-129">net stop mbamagent</span><span class="sxs-lookup"><span data-stu-id="50f33-129">net stop mbamagent</span></span>**

    **<span data-ttu-id="50f33-130">sc config mbamagent Start = Demand</span><span class="sxs-lookup"><span data-stu-id="50f33-130">sc config mbamagent start= demand</span></span>**

5.  <span data-ttu-id="50f33-131">Définissez les paramètres de registre de l’agent MBAM pour ignorer la stratégie de groupe et exécuter le TPM pour le **chiffrement du système d’exploitation uniquement** en exécutant **regedit**, puis en important le modèle de clé de Registre à partir de C:\\Program Files\\Microsoft\\MDOP MBAM\\MBAMDeploymentKeyTemplate.reg.</span><span class="sxs-lookup"><span data-stu-id="50f33-131">Set the registry settings for the MBAM agent to ignore Group Policy and run the TPM for **operating system only encryption** by running **Regedit**, and then importing the registry key template from C:\\Program Files\\Microsoft\\MDOP MBAM\\MBAMDeploymentKeyTemplate.reg.</span></span>

6.  <span data-ttu-id="50f33-132">Dans Regedit, accédez à HKLM\\SOFTWARE\\Microsoft\\MBAM et configurez les paramètres indiqués dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="50f33-132">In regedit, go to HKLM\\SOFTWARE\\Microsoft\\MBAM, and configure the settings that are listed in the following table.</span></span>

    <span data-ttu-id="50f33-133">Entrée du Registre</span><span class="sxs-lookup"><span data-stu-id="50f33-133">Registry entry</span></span>

    <span data-ttu-id="50f33-134">Paramètres de configuration</span><span class="sxs-lookup"><span data-stu-id="50f33-134">Configuration settings</span></span>

    <span data-ttu-id="50f33-135">DeploymentTime</span><span class="sxs-lookup"><span data-stu-id="50f33-135">DeploymentTime</span></span>

    <span data-ttu-id="50f33-136">0 = DÉSACTIVÉ</span><span class="sxs-lookup"><span data-stu-id="50f33-136">0 = OFF</span></span>

    <span data-ttu-id="50f33-137">1 = utiliser les paramètres de stratégie de moment de déploiement (par défaut)</span><span class="sxs-lookup"><span data-stu-id="50f33-137">1 = Use deployment time policy settings (default)</span></span>

    <span data-ttu-id="50f33-138">UseKeyRecoveryService</span><span class="sxs-lookup"><span data-stu-id="50f33-138">UseKeyRecoveryService</span></span>

    <span data-ttu-id="50f33-139">0 = ne pas utiliser la clé de dépôt clé (les deux entrées de Registre suivantes ne sont pas requises dans le cas présent)</span><span class="sxs-lookup"><span data-stu-id="50f33-139">0 = Do not use key escrow ( the next two registry entries are not required in this case)</span></span>

    <span data-ttu-id="50f33-140">1 = utiliser le tiers de confiance principal dans le système de récupération de clés (par défaut)</span><span class="sxs-lookup"><span data-stu-id="50f33-140">1 = Use key escrow in Key Recovery system (default)</span></span>

    <span data-ttu-id="50f33-141">Recommandé: l’ordinateur doit pouvoir communiquer avec le service de récupération de clés.</span><span class="sxs-lookup"><span data-stu-id="50f33-141">Recommended: The computer must be able to communicate with the Key Recovery service.</span></span> <span data-ttu-id="50f33-142">Vérifiez que l’ordinateur peut communiquer avec le service avant de continuer.</span><span class="sxs-lookup"><span data-stu-id="50f33-142">Verify that the computer can communicate with the service before you proceed.</span></span>

    <span data-ttu-id="50f33-143">KeyRecoveryOptions</span><span class="sxs-lookup"><span data-stu-id="50f33-143">KeyRecoveryOptions</span></span>

    <span data-ttu-id="50f33-144">0 = Télécharger uniquement la clé de récupération</span><span class="sxs-lookup"><span data-stu-id="50f33-144">0 = Uploads Recovery Key Only</span></span>

    <span data-ttu-id="50f33-145">1 = Télécharger la clé de récupération et le package de récupération de clé (par défaut)</span><span class="sxs-lookup"><span data-stu-id="50f33-145">1 = Uploads Recovery Key and Key Recovery Package (default)</span></span>

    <span data-ttu-id="50f33-146">KeyRecoveryServiceEndPoint</span><span class="sxs-lookup"><span data-stu-id="50f33-146">KeyRecoveryServiceEndPoint</span></span>

    <span data-ttu-id="50f33-147">Définissez cette valeur sur l’URL du serveur Web de récupération de clé (par exemple, http://nom de l' &lt; ordinateur &gt; /MBAMRecoveryAndHardwareService/CoreService.svc.</span><span class="sxs-lookup"><span data-stu-id="50f33-147">Set this value to the URL for the Key Recovery web server, for example, http://&lt;computer name&gt;/MBAMRecoveryAndHardwareService/CoreService.svc.</span></span>



~~~
**Note**  
MBAM policy or registry values can be set here to override previously set values.
~~~



7. <span data-ttu-id="50f33-148">L’agent MBAM redémarre le système lors du déploiement du client MBAM.</span><span class="sxs-lookup"><span data-stu-id="50f33-148">The MBAM agent restarts the system during MBAM client deployment.</span></span> <span data-ttu-id="50f33-149">Lorsque vous êtes prêt à redémarrer, exécutez la commande suivante à l’invite de commandes en tant qu’administrateur:</span><span class="sxs-lookup"><span data-stu-id="50f33-149">When you are ready for this reboot, run the following command at a command prompt as an administrator:</span></span>

   **<span data-ttu-id="50f33-150">mbamagent de début net</span><span class="sxs-lookup"><span data-stu-id="50f33-150">net start mbamagent</span></span>**

8. <span data-ttu-id="50f33-151">Au redémarrage de l’ordinateur, le BIOS vous demande d’accepter un changement de TPM en acceptant la modification.</span><span class="sxs-lookup"><span data-stu-id="50f33-151">When the computers restarts, and the BIOS prompts you to accept a TPM change, accept the change.</span></span>

9. <span data-ttu-id="50f33-152">Pendant le processus d’imagerie du système d’exploitation du client Windows, lorsque vous êtes prêt à commencer le chiffrement, redémarrez le service de l’agent MBAM et définissez démarrer sur **automatique** en exécutant une invite de commandes en tant qu’administrateur et en entrant les commandes suivantes:</span><span class="sxs-lookup"><span data-stu-id="50f33-152">During the Windows client operating system imaging process, when you are ready to start encryption, restart the MBAM agent service, and set start to **automatic** by running a command prompt as an administrator and typing the following commands:</span></span>

   **<span data-ttu-id="50f33-153">sc config mbamagent start = auto</span><span class="sxs-lookup"><span data-stu-id="50f33-153">sc config mbamagent start= auto</span></span>**

   **<span data-ttu-id="50f33-154">mbamagent de début net</span><span class="sxs-lookup"><span data-stu-id="50f33-154">net start mbamagent</span></span>**

10. <span data-ttu-id="50f33-155">Supprimez les valeurs de registre de contournement en exécutant regedit et en accédant à l’entrée de Registre HKLM\\SOFTWARE\\Microsoft.</span><span class="sxs-lookup"><span data-stu-id="50f33-155">Remove the bypass registry values by running Regedit and going to the HKLM\\SOFTWARE\\Microsoft registry entry.</span></span> <span data-ttu-id="50f33-156">Pour supprimer le nœud **MBAM** , cliquez avec le bouton droit sur le nœud, puis cliquez sur **supprimer**.</span><span class="sxs-lookup"><span data-stu-id="50f33-156">To delete the **MBAM** node, right-click the node and click **Delete**.</span></span>

## <span data-ttu-id="50f33-157">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="50f33-157">Related topics</span></span>


[<span data-ttu-id="50f33-158">Déploiement du client MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="50f33-158">Deploying the MBAM 2.0 Client</span></span>](deploying-the-mbam-20-client-mbam-2.md)









