---
title: Utilisation du portail de support technique
description: Utilisation du portail de support technique
author: dansimp
ms.assetid: c27f7737-10c8-4164-9de8-57987292c89c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa8813fbe9a7b6980b656ecc673ac4ed618c4cf7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811688"
---
# <span data-ttu-id="51dbf-103">Utilisation du portail de support technique</span><span class="sxs-lookup"><span data-stu-id="51dbf-103">How to Use the Help Desk Portal</span></span>


<span data-ttu-id="51dbf-104">Le site Web d’administration et de surveillance de MBAM, également appelé portail d’assistance technique, est une interface d’administration de BitLocker Drive Encryption qui est installée dans le cadre de l’infrastructure du serveur Microsoft BitLocker (MBAM).</span><span class="sxs-lookup"><span data-stu-id="51dbf-104">The MBAM Administration and Monitoring website, also referred to as the Help Desk Portal, is an administrative interface to BitLocker drive encryption that is installed as part of the Microsoft BitLocker Administration and Monitoring (MBAM) server infrastructure.</span></span> <span data-ttu-id="51dbf-105">Les sections suivantes décrivent comment vous pouvez utiliser ce site Web pour passer en revue des rapports, récupérer les lecteurs des utilisateurs finaux et gérer les utilisateurs TPMs.</span><span class="sxs-lookup"><span data-stu-id="51dbf-105">The following sections describe how you can use this website to review reports, recover end users’ drives, and manage end users’ TPMs.</span></span>

## <a href="" id="bkmk-reports"></a><span data-ttu-id="51dbf-106">Rapports</span><span class="sxs-lookup"><span data-stu-id="51dbf-106">Reports</span></span>


<span data-ttu-id="51dbf-107">MBAM collecte des informations à partir d’Active Directory et d’ordinateurs clients, ce qui vous permet d’exécuter différents rapports pour contrôler l’utilisation et la conformité de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="51dbf-107">MBAM collects information from Active Directory and client computers, which enables you to run different reports to monitor BitLocker usage and compliance.</span></span> <span data-ttu-id="51dbf-108">À l’aide de la section **rapports** du site Web d’administration et de surveillance, vous pouvez générer des rapports sur les activités de conformité d’entreprise, d’ordinateur individuel et de récupération de clés.</span><span class="sxs-lookup"><span data-stu-id="51dbf-108">Using the **Reports** section of the Administration and Monitoring website, you can generate reports on enterprise compliance, individual computers, and key recovery activity.</span></span> <span data-ttu-id="51dbf-109">Pour obtenir une description de chaque rapport, voir [Présentation des rapports MBAM](understanding-mbam-reports-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="51dbf-109">For a description of each report, see [Understanding MBAM Reports](understanding-mbam-reports-mbam-2.md).</span></span>

**<span data-ttu-id="51dbf-110">Pour accéder aux rapports</span><span class="sxs-lookup"><span data-stu-id="51dbf-110">To access reports</span></span>**

1.  <span data-ttu-id="51dbf-111">Ouvrez un navigateur Web, puis accédez au site Web d’administration et de contrôle MBAM.</span><span class="sxs-lookup"><span data-stu-id="51dbf-111">Open a web browser and navigate to the MBAM Administration and Monitoring website.</span></span>

2.  <span data-ttu-id="51dbf-112">Dans le volet gauche, sélectionnez **rapports** .</span><span class="sxs-lookup"><span data-stu-id="51dbf-112">Select **Reports** in the left pane.</span></span>

3.  <span data-ttu-id="51dbf-113">Dans la barre de menus supérieure, sélectionnez le type de rapport que vous souhaitez générer.</span><span class="sxs-lookup"><span data-stu-id="51dbf-113">From the top menu bar, select the report type you want to generate.</span></span> <span data-ttu-id="51dbf-114">Pour enregistrer des rapports, cliquez sur le bouton **Exporter** dans la barre de menus rapports.</span><span class="sxs-lookup"><span data-stu-id="51dbf-114">To save reports, click the **Export** button on the Reports menu bar.</span></span>

<span data-ttu-id="51dbf-115">Pour plus d’informations sur l’exécution des rapports MBAM, voir [génération de rapports MBAM](how-to-generate-mbam-reports-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="51dbf-115">For additional information about how to run MBAM reports, see [How to Generate MBAM Reports](how-to-generate-mbam-reports-mbam-2.md).</span></span>

## <a href="" id="bkmk-drirec"></a><span data-ttu-id="51dbf-116">Récupération des lecteurs</span><span class="sxs-lookup"><span data-stu-id="51dbf-116">Drive Recovery</span></span>


<span data-ttu-id="51dbf-117">La fonctionnalité de **récupération de lecteur** du site Web d’administration et de contrôle permet aux utilisateurs ayant des rôles d’administrateur spécifiques (par exemple, les utilisateurs du support technique) d’accéder aux données de clé de récupération collectées par le client MBAM.</span><span class="sxs-lookup"><span data-stu-id="51dbf-117">The **Drive Recovery** feature of the Administration and Monitoring website allows users with specific administrator roles (for example, Help Desk Users) to access recovery key data that has been collected by the MBAM Client.</span></span> <span data-ttu-id="51dbf-118">Ces données peuvent être utilisées pour accéder à un lecteur protégé par BitLocker lorsque BitLocker passe en mode de récupération.</span><span class="sxs-lookup"><span data-stu-id="51dbf-118">This data can be used to access a BitLocker-protected drive when BitLocker goes into recovery mode.</span></span> <span data-ttu-id="51dbf-119">Pour obtenir des instructions sur la façon de récupérer un lecteur qui est en mode récupération, voir [Comment récupérer un lecteur en mode récupération](how-to-recover-a-drive-in-recovery-mode-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="51dbf-119">For instructions on how to recover a drive that is in recovery mode, see [How to Recover a Drive in Recovery Mode](how-to-recover-a-drive-in-recovery-mode-mbam-2.md).</span></span>

<span data-ttu-id="51dbf-120">Vous pouvez également récupérer des lecteurs qui ont été déplacés ou qui sont endommagés:</span><span class="sxs-lookup"><span data-stu-id="51dbf-120">You can also recover drives that have been moved or that are corrupted:</span></span>

-   [<span data-ttu-id="51dbf-121">Récupération d'un lecteur déplacé</span><span class="sxs-lookup"><span data-stu-id="51dbf-121">How to Recover a Moved Drive</span></span>](how-to-recover-a-moved-drive-mbam-2.md)

-   [<span data-ttu-id="51dbf-122">Récupération d'un lecteur endommagé</span><span class="sxs-lookup"><span data-stu-id="51dbf-122">How to Recover a Corrupted Drive</span></span>](how-to-recover-a-corrupted-drive-mbam-2.md)

<span data-ttu-id="51dbf-123">Pour plus d’informations sur la façon de récupérer un lecteur protégé par BitLocker, voir exécution de la [gestion BitLocker avec mbam](performing-bitlocker-management-with-mbam-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="51dbf-123">For additional information about how to recover a BitLocker-protected drive, see [Performing BitLocker Management with MBAM](performing-bitlocker-management-with-mbam-mbam-2.md).</span></span>

## <a href="" id="bkmk-manatpm"></a><span data-ttu-id="51dbf-124">Gérer le TPM</span><span class="sxs-lookup"><span data-stu-id="51dbf-124">Manage TPM</span></span>


<span data-ttu-id="51dbf-125">La fonction de gestion des PUCEs du site Web d’administration et de contrôle donne aux utilisateurs de certains rôles d’administrateur (par exemple, «utilisateurs du support technique MBAM») l’accès aux données du TPM collectées par le client MBAM.</span><span class="sxs-lookup"><span data-stu-id="51dbf-125">The Manage TPM feature of the Administration and Monitoring website gives users with certain administrator roles (for example, “MBAM Helpdesk Users”) access to TPM data that has been collected by the MBAM Client.</span></span> <span data-ttu-id="51dbf-126">Dans le cas d’un verrouillage de module de plateforme sécurisée, un administrateur peut utiliser le site Web d’administration et de surveillance pour récupérer le fichier de mot de passe nécessaire pour déverrouiller le TPM.</span><span class="sxs-lookup"><span data-stu-id="51dbf-126">In a TPM lockout, an administrator can use the Administration and Monitoring website to retrieve the necessary password file to unlock the TPM.</span></span> <span data-ttu-id="51dbf-127">Pour obtenir des instructions sur la réinitialisation d’un TPM après le verrouillage du TPM, voir [Comment réinitialiser un verrouillage du TPM](how-to-reset-a-tpm-lockout-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="51dbf-127">For instructions on how to reset a TPM after a TPM lockout, see [How to Reset a TPM Lockout](how-to-reset-a-tpm-lockout-mbam-2.md).</span></span>

## <a href="" id="bkmk-helpdesk"></a> <span data-ttu-id="51dbf-128">Tâches du support technique MBAM</span><span class="sxs-lookup"><span data-stu-id="51dbf-128">MBAM Help Desk Tasks</span></span>


<span data-ttu-id="51dbf-129">Vous pouvez utiliser le site Web d’administration et de contrôle pour de nombreuses tâches d’administration, telles que la gestion du matériel protégé par BitLocker, la récupération de lecteurs et l’exécution de rapports.</span><span class="sxs-lookup"><span data-stu-id="51dbf-129">You can use the Administration and Monitoring website for many administrative tasks, such as managing BitLocker-protected hardware, recovering drives, and running reports.</span></span> <span data-ttu-id="51dbf-130">Par défaut, l’URL du site Web d’administration et de surveillance est http:// &lt; *MBAMAdministrationServername* &gt; , même si vous pouvez le personnaliser pendant le processus d’installation.</span><span class="sxs-lookup"><span data-stu-id="51dbf-130">By default, the URL for the Administration and Monitoring website is http://&lt;*MBAMAdministrationServername*&gt;, although you can customize it during the installation process.</span></span>

<span data-ttu-id="51dbf-131">**Remarques**  Pour accéder aux diverses fonctionnalités proposées par le site Web d’administration et de surveillance, vous devez disposer des rôles appropriés associés à votre compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="51dbf-131">**Note** To access the various features offered by the Administration and Monitoring website, you must have the appropriate roles associated with your user account.</span></span> <span data-ttu-id="51dbf-132">Pour plus d’informations sur la compréhension des rôles d’utilisateur, voir [Comment gérer les rôles d’administrateur de MBAM](how-to-manage-mbam-administrator-roles-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="51dbf-132">For more information about understanding user roles, see [How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-2.md).</span></span>

 

<span data-ttu-id="51dbf-133">Pour trouver des informations sur les tâches que vous pouvez effectuer à l’aide du site Web d’administration et de contrôle, utilisez les liens suivants:</span><span class="sxs-lookup"><span data-stu-id="51dbf-133">Use the following links to find information about the tasks that you can perform by using the Administration and Monitoring website:</span></span>

-   [<span data-ttu-id="51dbf-134">Réinitialisation d'un verrouillage TPM</span><span class="sxs-lookup"><span data-stu-id="51dbf-134">How to Reset a TPM Lockout</span></span>](how-to-reset-a-tpm-lockout-mbam-2.md)

-   [<span data-ttu-id="51dbf-135">Procédure de récupération d'un lecteur en mode de récupération</span><span class="sxs-lookup"><span data-stu-id="51dbf-135">How to Recover a Drive in Recovery Mode</span></span>](how-to-recover-a-drive-in-recovery-mode-mbam-2.md)

-   [<span data-ttu-id="51dbf-136">Récupération d'un lecteur déplacé</span><span class="sxs-lookup"><span data-stu-id="51dbf-136">How to Recover a Moved Drive</span></span>](how-to-recover-a-moved-drive-mbam-2.md)

-   [<span data-ttu-id="51dbf-137">Récupération d'un lecteur endommagé</span><span class="sxs-lookup"><span data-stu-id="51dbf-137">How to Recover a Corrupted Drive</span></span>](how-to-recover-a-corrupted-drive-mbam-2.md)

-   [<span data-ttu-id="51dbf-138">Détermination de l'état de chiffrement BitLocker des ordinateurs perdus</span><span class="sxs-lookup"><span data-stu-id="51dbf-138">How to Determine BitLocker Encryption State of Lost Computers</span></span>](how-to-determine-bitlocker-encryption-state-of-lost-computers-mbam-2.md)

 

 





