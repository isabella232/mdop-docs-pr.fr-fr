---
title: Administration des composants de MBAM1.0
description: Administration des composants de MBAM1.0
author: dansimp
ms.assetid: dd9a9eff-f1ad-4af3-85d9-c19131a4ad22
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a99ac556227c0f113fb20f3aca32d21c204877b0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808627"
---
# <span data-ttu-id="1b2fd-103">Administration des composants de MBAM1.0</span><span class="sxs-lookup"><span data-stu-id="1b2fd-103">Administering MBAM 1.0 Features</span></span>


<span data-ttu-id="1b2fd-104">Après avoir exécuté la planification et le déploiement de la planification et du déploiement de Microsoft BitLocker requis, vous pouvez configurer et utiliser MBAM pour gérer le chiffrement d’entreprise BitLocker.</span><span class="sxs-lookup"><span data-stu-id="1b2fd-104">After you complete all necessary Microsoft BitLocker Administration and Monitoring (MBAM) planning and deployment, you can configure and use MBAM to manage enterprise BitLocker encryption.</span></span> <span data-ttu-id="1b2fd-105">Les informations contenues dans cette section décrivent les tâches d’opérations relatives aux fonctionnalités de la fonctionnalité de MBAM d’installation.</span><span class="sxs-lookup"><span data-stu-id="1b2fd-105">The information in this section describes post-installation day-to-day MBAM feature operations tasks.</span></span>

## <span data-ttu-id="1b2fd-106">Gérer les rôles d’administrateur MBAM</span><span class="sxs-lookup"><span data-stu-id="1b2fd-106">Manage MBAM Administrator Roles</span></span>


<span data-ttu-id="1b2fd-107">Une fois l’installation d’MBAM terminée pour toutes les fonctionnalités du serveur, les utilisateurs administratifs doivent avoir accès à ces fonctionnalités serveur.</span><span class="sxs-lookup"><span data-stu-id="1b2fd-107">After MBAM Setup is complete for all server features, administrative users must be granted access to these server features.</span></span> <span data-ttu-id="1b2fd-108">Il est recommandé que les administrateurs qui gèrent ou utilisent les fonctionnalités du serveur MBAM doivent être assignés aux groupes de sécurité Active Directory, puis ces groupes doivent être ajoutés au groupe local administratif approprié MBAM.</span><span class="sxs-lookup"><span data-stu-id="1b2fd-108">As a best practice, administrators who will manage or use MBAM server features, should be assigned to Active Directory security groups and then those groups should be added to the appropriate MBAM administrative local group.</span></span>

[<span data-ttu-id="1b2fd-109">Gérer des rôles d'administrateur MBAM</span><span class="sxs-lookup"><span data-stu-id="1b2fd-109">How to Manage MBAM Administrator Roles</span></span>](how-to-manage-mbam-administrator-roles-mbam-1.md)

## <span data-ttu-id="1b2fd-110">Gérer la compatibilité du matériel</span><span class="sxs-lookup"><span data-stu-id="1b2fd-110">Manage Hardware Compatibility</span></span>


<span data-ttu-id="1b2fd-111">La fonctionnalité de compatibilité matérielle MBAM peut vous aider à vous assurer que seul le matériel informatique que vous spécifiez comme prenant en charge BitLocker sera crypté.</span><span class="sxs-lookup"><span data-stu-id="1b2fd-111">The MBAM Hardware Compatibility feature can help you to ensure that only the computer hardware that you specify as supporting BitLocker will be encrypted.</span></span> <span data-ttu-id="1b2fd-112">Lorsque cette fonctionnalité est activée, le bit \ _admmontla chiffre uniquement les ordinateurs marqués comme compatibles.</span><span class="sxs-lookup"><span data-stu-id="1b2fd-112">When this feature is turned on, bit\_admmontla will encrypt only computers that are marked as Compatible.</span></span>

<span data-ttu-id="1b2fd-113">**Important**  Lorsque cette fonctionnalité est désactivée, tous les ordinateurs sur lesquels la stratégie MBAM est déployée seront chiffrés.</span><span class="sxs-lookup"><span data-stu-id="1b2fd-113">**Important** When this feature is turned off, all computers where the MBAM policy is deployed will be encrypted.</span></span>

 

<span data-ttu-id="1b2fd-114">MBAM peut collecter des informations sur la création et le modèle d’ordinateurs clients si vous déployez la stratégie de groupe «autoriser le contrôle de compatibilité matérielle».</span><span class="sxs-lookup"><span data-stu-id="1b2fd-114">MBAM can collect information on both the make and model of client computers if you deploy the “Allow Hardware Compatibility Checking” Group Policy.</span></span> <span data-ttu-id="1b2fd-115">Si vous configurez cette stratégie, l’agent MBAM rapporte les informations sur la marque et le modèle de l’ordinateur au serveur MBAM lorsque le client MBAM est déployé sur un ordinateur client.</span><span class="sxs-lookup"><span data-stu-id="1b2fd-115">If you configure this policy, the MBAM agent reports the computer make and model information to the MBAM Server when the MBAM Client is deployed on a client computer.</span></span>

[<span data-ttu-id="1b2fd-116">Gérer la compatibilité matérielle</span><span class="sxs-lookup"><span data-stu-id="1b2fd-116">How to Manage Hardware Compatibility</span></span>](how-to-manage-hardware-compatibility-mbam-1.md)

[<span data-ttu-id="1b2fd-117">Gestion des exemptions de chiffrement BitLocker d'utilisateur</span><span class="sxs-lookup"><span data-stu-id="1b2fd-117">How to Manage User BitLocker Encryption Exemptions</span></span>](how-to-manage-user-bitlocker-encryption-exemptions-mbam-1.md)

## <span data-ttu-id="1b2fd-118">Gérer les exemptions de chiffrement BitLocker</span><span class="sxs-lookup"><span data-stu-id="1b2fd-118">Manage BitLocker encryption exemptions</span></span>


<span data-ttu-id="1b2fd-119">MBAM peut accorder deux formes d’exemption du chiffrement BitLocker: exemption d’ordinateur et exemption d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1b2fd-119">MBAM can grant two forms of exemption from BitLocker encryption: computer exemption and user exemption.</span></span> <span data-ttu-id="1b2fd-120">L’exemption d’ordinateur est généralement utilisée lorsqu’une société dispose d’ordinateurs qui n’ont pas besoin d’être chiffrés, tels que des ordinateurs utilisés pour le développement ou les tests, ou des ordinateurs plus anciens qui ne prennent pas en charge BitLocker.</span><span class="sxs-lookup"><span data-stu-id="1b2fd-120">Computer exemption is typically used when a company has computers that do not have to be encrypted, such as computers that are used in development or testing, or older computers that do not support BitLocker.</span></span> <span data-ttu-id="1b2fd-121">Dans certains cas, la législation locale peuvent également exiger que certains ordinateurs ne soient pas chiffrés.</span><span class="sxs-lookup"><span data-stu-id="1b2fd-121">In some cases, local law may also require that certain computers are not encrypted.</span></span> <span data-ttu-id="1b2fd-122">Vous pouvez également choisir d’exempter les utilisateurs qui n’ont pas besoin ou dont leurs lecteurs sont chiffrés.</span><span class="sxs-lookup"><span data-stu-id="1b2fd-122">You may also choose to exempt users who do not need or want their drives encrypted.</span></span>

[<span data-ttu-id="1b2fd-123">Gérer des exemptions d'ordinateurs au chiffrement BitLocker</span><span class="sxs-lookup"><span data-stu-id="1b2fd-123">How to Manage Computer BitLocker Encryption Exemptions</span></span>](how-to-manage-computer-bitlocker-encryption-exemptions.md)

## <span data-ttu-id="1b2fd-124">Gérer les options de chiffrement BitLocker du client MBAM à l’aide du panneau de configuration</span><span class="sxs-lookup"><span data-stu-id="1b2fd-124">Manage MBAM Client BitLocker Encryption Options by using the Control Panel</span></span>


<span data-ttu-id="1b2fd-125">S’il est activé par le biais d’objets de stratégie de groupe (GPO), un panneau de configuration MBAM personnalisé nommé options de chiffrement BitLocker sera disponible sous **système et sécurité**.</span><span class="sxs-lookup"><span data-stu-id="1b2fd-125">If enabled through a Group Policy Objects (GPO), a custom MBAM control panel that is named BitLocker Encryption Options will be available under **System and Security**.</span></span> <span data-ttu-id="1b2fd-126">Ce panneau de configuration personnalisé remplace le panneau de configuration Windows BitLocker par défaut.</span><span class="sxs-lookup"><span data-stu-id="1b2fd-126">This customized control panel replaces the default Windows BitLocker control panel.</span></span> <span data-ttu-id="1b2fd-127">Le panneau de configuration MBAM vous permet de déverrouiller des lecteurs chiffrés (résolus et amovibles) et de gérer également votre code confidentiel ou votre mot de passe.</span><span class="sxs-lookup"><span data-stu-id="1b2fd-127">The MBAM control panel enables you to unlock encrypted drives (fixed and removable), and also helps you manage your PIN or password.</span></span>

[<span data-ttu-id="1b2fd-128">Gestion des options de chiffrement BitLocker du client MBAM à l'aide du Panneau de configuration</span><span class="sxs-lookup"><span data-stu-id="1b2fd-128">How to Manage MBAM Client BitLocker Encryption Options by Using the Control Panel</span></span>](how-to-manage-mbam-client-bitlocker-encryption-options-by-using-the-control-panel-mbam-1.md)

## <span data-ttu-id="1b2fd-129">Autres ressources pour administrer les fonctionnalités de MBAM</span><span class="sxs-lookup"><span data-stu-id="1b2fd-129">Other resources for Administering MBAM features</span></span>


[<span data-ttu-id="1b2fd-130">Opérations de MBAM1.0</span><span class="sxs-lookup"><span data-stu-id="1b2fd-130">Operations for MBAM 1.0</span></span>](operations-for-mbam-10.md)

 

 





