---
title: Gérer la compatibilité matérielle
description: Gérer la compatibilité matérielle
author: dansimp
ms.assetid: c74b96b9-8161-49bc-b5bb-4838734e7df5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cf9e2c5b2b33ea93d9834a81700bd2be8a9b9757
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804638"
---
# <span data-ttu-id="279c0-103">Gérer la compatibilité matérielle</span><span class="sxs-lookup"><span data-stu-id="279c0-103">How to Manage Hardware Compatibility</span></span>


<span data-ttu-id="279c0-104">Le système d’administration et de surveillance de BitLocker Microsoft (MBAM) peut collecter des informations sur le fabricant et le modèle d’ordinateurs clients après le déploiement de la stratégie de groupe autoriser le contrôle de compatibilité matérielle.</span><span class="sxs-lookup"><span data-stu-id="279c0-104">Microsoft BitLocker Administration and Monitoring (MBAM) can collect information about the manufacturer and model of client computers after you deploy the Allow Hardware Compatibility Checking Group Policy.</span></span> <span data-ttu-id="279c0-105">Si vous configurez cette stratégie, l’agent MBAM rapporte les informations sur la marque et le modèle de l’ordinateur au serveur MBAM lorsque le client MBAM est déployé sur un ordinateur client.</span><span class="sxs-lookup"><span data-stu-id="279c0-105">If you configure this policy, the MBAM agent reports the computer make and model information to the MBAM Server when the MBAM Client is deployed on a client computer.</span></span>

<span data-ttu-id="279c0-106">La fonctionnalité de compatibilité matérielle est utile si votre organisation a des matériels informatiques ou des ordinateurs plus anciens qui ne prennent pas en charge les puces de module de plateforme sécurisée (TPM).</span><span class="sxs-lookup"><span data-stu-id="279c0-106">The Hardware Compatibility feature is helpful when your organization has older computer hardware or computers that do not support Trusted Platform Module (TPM) chips.</span></span> <span data-ttu-id="279c0-107">Dans ces cas, vous pouvez utiliser la fonctionnalité de compatibilité matérielle pour vous assurer que le chiffrement BitLocker est appliqué uniquement aux modèles d’ordinateur qui le prennent en charge.</span><span class="sxs-lookup"><span data-stu-id="279c0-107">In these cases, you can use the Hardware Compatibility feature to ensure that BitLocker encryption is applied only to computer models that support it.</span></span> <span data-ttu-id="279c0-108">Si tous les ordinateurs de votre organisation prennent en charge BitLocker, vous n’avez pas besoin d’utiliser la fonctionnalité de compatibilité matérielle.</span><span class="sxs-lookup"><span data-stu-id="279c0-108">If all computers in your organization will support BitLocker, you do not have to use the Hardware Compatibility feature.</span></span>

<span data-ttu-id="279c0-109">**Remarques**  Par défaut, la fonctionnalité de compatibilité matérielle MBAM n’est pas activée.</span><span class="sxs-lookup"><span data-stu-id="279c0-109">**Note** By default, MBAM Hardware Compatibility feature is not enabled.</span></span> <span data-ttu-id="279c0-110">Pour l’activer, sélectionnez la fonctionnalité **compatibilité matérielle** sous la fonctionnalité **administration et analyse du serveur** lors de l’installation.</span><span class="sxs-lookup"><span data-stu-id="279c0-110">To enable it, select the **Hardware Compatibility** feature under the **Administration and Monitoring Server** feature during setup.</span></span> <span data-ttu-id="279c0-111">Pour plus d’informations sur la configuration et la configuration de la compatibilité matérielle, reportez-vous à [la rubrique déploiement de l’infrastructure du serveur MBAM 1,0](deploying-the-mbam-10-server-infrastructure.md).</span><span class="sxs-lookup"><span data-stu-id="279c0-111">For more information about how to set up and configure Hardware Compatibility, see [Deploying the MBAM 1.0 Server Infrastructure](deploying-the-mbam-10-server-infrastructure.md).</span></span>

 

<span data-ttu-id="279c0-112">La fonctionnalité de compatibilité matérielle fonctionne de la manière suivante.</span><span class="sxs-lookup"><span data-stu-id="279c0-112">The Hardware Compatibility feature works in the following way.</span></span>

****

1.  <span data-ttu-id="279c0-113">L’agent client MBAM Découvre des informations d’ordinateur de base, telles que le fabricant, le modèle, le BIOS, la version du BIOS, le module de plateforme sécurisée et la version TPM, puis transmet ces informations au serveur MBAM.</span><span class="sxs-lookup"><span data-stu-id="279c0-113">The MBAM client agent discovers basic computer information such as manufacturer, model, BIOS maker, BIOS version, TPM maker, and TPM version, and then passes this information to the MBAM server.</span></span>

2.  <span data-ttu-id="279c0-114">Le serveur MBAM génère une liste de modèles et de modèles d’ordinateur client pour vous permettre de distinguer les personnes qui peuvent ou ne peuvent pas prendre en charge BitLocker.</span><span class="sxs-lookup"><span data-stu-id="279c0-114">The MBAM server generates a list of client computer makes and models to enable you to differentiate between those that can or cannot support BitLocker</span></span>

3.  <span data-ttu-id="279c0-115">Les agents clients MBAM déployés dans l’entreprise effectuent automatiquement la mise à jour de cette liste à l’aide de tous les nouveaux modèles et modes d’ordinateur identifiés avec l’état **inconnu**.</span><span class="sxs-lookup"><span data-stu-id="279c0-115">The MBAM client agents that are deployed in the enterprise automatically update this list with all new computer makes and models that are discovered with a state of **Unknown**.</span></span> <span data-ttu-id="279c0-116">Un administrateur peut ensuite utiliser le site Web d’administration de MBAM pour modifier les entrées de liste afin de spécifier une marque et un modèle d’ordinateur particulier comme **compatible** ou **incompatible**.</span><span class="sxs-lookup"><span data-stu-id="279c0-116">An administrator can then use the MBAM administration website to change list entries to specify a particular computer make and model as **Compatible** or **Incompatible**.</span></span>

4.  <span data-ttu-id="279c0-117">Pour que l’agent client MBAM commence à chiffrer un lecteur, l’agent vérifie d’abord la compatibilité de chiffrement BitLocker du matériel sur lequel il s’exécute.</span><span class="sxs-lookup"><span data-stu-id="279c0-117">Before the MBAM client agent begins encrypting a drive, the agent first verifies the BitLocker encryption compatibility of the hardware it is running on.</span></span>

    -   <span data-ttu-id="279c0-118">Si le matériel est marqué comme étant compatible, le processus de chiffrement BitLocker démarre.</span><span class="sxs-lookup"><span data-stu-id="279c0-118">If the hardware is marked as compatible, the BitLocker encryption process starts.</span></span> <span data-ttu-id="279c0-119">MBAM revérifiera également l’état de compatibilité matérielle de l’ordinateur une fois par jour.</span><span class="sxs-lookup"><span data-stu-id="279c0-119">MBAM will also recheck the hardware compatibility status of the computer one time per day.</span></span>

    -   <span data-ttu-id="279c0-120">Si le matériel est marqué comme incompatible, l’agent enregistre un événement et transmet un état «matériel exempté» dans le cadre du rapport de conformité.</span><span class="sxs-lookup"><span data-stu-id="279c0-120">If the hardware is marked as incompatible, the agent logs an event and passes a “hardware exempted” state as part of compliance reporting.</span></span> <span data-ttu-id="279c0-121">L’agent vérifie chaque semaine pour déterminer si l’État a changé en «compatible».</span><span class="sxs-lookup"><span data-stu-id="279c0-121">The agent checks every seven days to see whether the state has changed to “compatible.”</span></span>

    -   <span data-ttu-id="279c0-122">Si le matériel est marqué comme inconnu, le processus de chiffrement BitLocker ne démarre pas.</span><span class="sxs-lookup"><span data-stu-id="279c0-122">If the hardware is marked as unknown, the BitLocker encryption process will not begin.</span></span> <span data-ttu-id="279c0-123">L’agent client MBAM revérifiera l’état de compatibilité matérielle de l’ordinateur une fois par jour.</span><span class="sxs-lookup"><span data-stu-id="279c0-123">The MBAM client agent will recheck the hardware compatibility status of the computer one time per day.</span></span>

<span data-ttu-id="279c0-124">**Avertissement**  Si l’agent client MBAM tente de chiffrer un ordinateur qui ne prend pas en charge le chiffrement de lecteur BitLocker, il est possible que l’ordinateur soit endommagé.</span><span class="sxs-lookup"><span data-stu-id="279c0-124">**Warning** If the MBAM client agent tries to encrypt a computer that does not support BitLocker drive encryption, there is a possibility that the computer will become corrupted.</span></span> <span data-ttu-id="279c0-125">Assurez-vous que la fonctionnalité de compatibilité matérielle est correctement configurée lorsque votre organisation dispose d’un matériel ancien qui ne prend pas en charge BitLocker.</span><span class="sxs-lookup"><span data-stu-id="279c0-125">Ensure that the hardware compatibility feature is correctly configured when your organization has older hardware that does not support BitLocker.</span></span>

 

**<span data-ttu-id="279c0-126">Pour gérer la compatibilité du matériel</span><span class="sxs-lookup"><span data-stu-id="279c0-126">To manage hardware compatibility</span></span>**

1.  <span data-ttu-id="279c0-127">Ouvrez un navigateur Web, puis accédez au site Web d’administration et de contrôle de Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="279c0-127">Open a web browser and navigate to the Microsoft BitLocker Administration and Monitoring website.</span></span> <span data-ttu-id="279c0-128">Dans la barre de menus de gauche, sélectionnez **matériel** .</span><span class="sxs-lookup"><span data-stu-id="279c0-128">Select **Hardware** in the left menu bar.</span></span>

2.  <span data-ttu-id="279c0-129">Dans le volet droit, cliquez sur **recherche avancée**, puis filtrez pour afficher une liste de tous les modèles d’ordinateur dont le statut de **fonctionnalité** est **inconnu**.</span><span class="sxs-lookup"><span data-stu-id="279c0-129">On the right pane, click **Advanced Search**, and then filter to display a list of all computer models that have a **Capability** status of **Unknown**.</span></span> <span data-ttu-id="279c0-130">La liste des modèles d’ordinateur correspondant au critère de recherche s’affiche.</span><span class="sxs-lookup"><span data-stu-id="279c0-130">A list of computer models matching the search criteria is displayed.</span></span> <span data-ttu-id="279c0-131">Les administrateurs peuvent ajouter, modifier ou supprimer de nouveaux types d’ordinateurs à partir de cette page.</span><span class="sxs-lookup"><span data-stu-id="279c0-131">Administrators can add, edit, or remove new computer types from this page.</span></span>

3.  <span data-ttu-id="279c0-132">Vérifiez chaque configuration matérielle inconnue pour déterminer si la configuration doit être **compatible** ou **incompatible**.</span><span class="sxs-lookup"><span data-stu-id="279c0-132">Review each unknown hardware configuration to determine whether the configuration should be set to **Compatible** or **Incompatible**.</span></span>

4.  <span data-ttu-id="279c0-133">Sélectionnez une ou plusieurs lignes, puis cliquez sur **définir** la compatibilité ou sur définir **incompatible** pour définir la compatibilité BitLocker, le cas échéant, pour les modèles d’ordinateurs sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="279c0-133">Select one or more rows, and then click either **Set Compatible** or **Set Incompatible** to set the BitLocker compatibility, as appropriate, for the selected computer models.</span></span> <span data-ttu-id="279c0-134">S’il est défini sur **compatible**, BitLocker tente d’appliquer une stratégie de chiffrement de lecteur sur des ordinateurs qui correspondent au modèle pris en charge.</span><span class="sxs-lookup"><span data-stu-id="279c0-134">If set to **Compatible**, BitLocker tries to enforce drive encryption policy on computers that match the supported model.</span></span> <span data-ttu-id="279c0-135">S’il est défini sur **incompatible**, BitLocker n’applique pas la stratégie de chiffrement de lecteur sur ces ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="279c0-135">If set to **Incompatible**, BitLocker will not enforce drive encryption policy on those computers.</span></span>

    <span data-ttu-id="279c0-136">**Remarques**  Après avoir configuré un modèle d’ordinateur comme compatible, il peut s’écouler plus de 24 heures pour que le client MBAM commence le chiffrement BitLocker sur les ordinateurs correspondant à ce modèle matériel.</span><span class="sxs-lookup"><span data-stu-id="279c0-136">**Note** After you set a computer model as compatible, it can take more than twenty-four hours for the MBAM Client to begin BitLocker encryption on the computers matching that hardware model.</span></span>

     

5.  <span data-ttu-id="279c0-137">Les administrateurs doivent surveiller régulièrement la liste de compatibilité matérielle pour passer en revue les nouveaux modèles détectés par l’agent MBAM, puis mettre à jour leur paramètre de compatibilité sur **compatible** ou **incompatible** , le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="279c0-137">Administrators should regularly monitor the hardware compatibility list to review new models that are discovered by the MBAM agent, and then update their compatibility setting to **Compatible** or **Incompatible** as appropriate.</span></span>

## <span data-ttu-id="279c0-138">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="279c0-138">Related topics</span></span>


[<span data-ttu-id="279c0-139">Administration des composants de MBAM1.0</span><span class="sxs-lookup"><span data-stu-id="279c0-139">Administering MBAM 1.0 Features</span></span>](administering-mbam-10-features.md)

 

 





