---
title: Considérations relatives à la sécurité pour DaRT7.0
description: Considérations relatives à la sécurité pour DaRT7.0
author: dansimp
ms.assetid: 52ad7e6c-c169-4ba4-aa76-56335a585eb8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 739c0319195aeb26e38d55ffe01d14b623de7f43
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809533"
---
# <span data-ttu-id="44f1f-103">Considérations relatives à la sécurité pour DaRT7.0</span><span class="sxs-lookup"><span data-stu-id="44f1f-103">Security Considerations for DaRT 7.0</span></span>


<span data-ttu-id="44f1f-104">Microsoft Diagnostics and Recovery Tools (DaRT) 7 inclut une fonctionnalité qui permet à un administrateur d’exécuter les outils DaRT à distance pour résoudre les problèmes sur un ordinateur d’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="44f1f-104">Microsoft Diagnostics and Recovery Toolset (DaRT)7 includes functionality that lets an administrator run the DaRT tools remotely to resolve problems on an end-user computer.</span></span> <span data-ttu-id="44f1f-105">Dans les versions précédentes de DaRT, un technicien du support technique ou un administrateur devait se trouver physiquement sur un ordinateur d’un utilisateur final et démarrer dans DaRT en utilisant le CD ou DVD qui incluait l’image de récupération DaRT.</span><span class="sxs-lookup"><span data-stu-id="44f1f-105">In earlier releases of DaRT, a help desk technician or administrator had to physically be at an end-user computer and boot into DaRT by using the CD or DVD that included the DaRT recovery image.</span></span> <span data-ttu-id="44f1f-106">À présent, le technicien de support technique ou l’administrateur peut effectuer les mêmes procédures à distance.</span><span class="sxs-lookup"><span data-stu-id="44f1f-106">Now, the help desk technician or administrator can perform the same procedures remotely.</span></span>

<span data-ttu-id="44f1f-107">Dans DaRT7, en plus de graver un CD ou un DVD, vous pouvez désormais enregistrer l’image ISO (International Organization for Standardization) sur une clé USB.</span><span class="sxs-lookup"><span data-stu-id="44f1f-107">Also in DaRT7, in addition to burning a CD or DVD, you are now able to save the International Organization for Standardization (ISO) image to a USB flash drive.</span></span> <span data-ttu-id="44f1f-108">Vous pouvez également placer l’image ISO sur un réseau ou inclure son contenu comme partition de récupération sur le disque dur de votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="44f1f-108">You can also put the ISO image on a network or include its contents as a recovery partition on a computer hard disk.</span></span>

<span data-ttu-id="44f1f-109">La fonctionnalité de **connexion à distance** de DaRT7 permet aux utilisateurs finaux d’accéder au DART en utilisant l’une de ces nouvelles méthodes de déploiement.</span><span class="sxs-lookup"><span data-stu-id="44f1f-109">The **Remote Connection** feature in DaRT7 lets end users access DaRT by using one of these new deployment methods.</span></span> <span data-ttu-id="44f1f-110">C’est pourquoi il est plus facile de démarrer DaRT et d’accéder aux outils DaRT.</span><span class="sxs-lookup"><span data-stu-id="44f1f-110">Therefore, they can more easily start DaRT and access the DaRT tools.</span></span>

<span data-ttu-id="44f1f-111">Les nouvelles fonctionnalités de DaRT7 fournissent une plus grande flexibilité dans le mode d’utilisation de DaRT dans votre entreprise.</span><span class="sxs-lookup"><span data-stu-id="44f1f-111">The new functionalities in DaRT7 provide much more flexibility in how you use DaRT in your enterprise.</span></span> <span data-ttu-id="44f1f-112">Toutefois, ils créent également un ensemble de problèmes de sécurité qui doivent être résolus.</span><span class="sxs-lookup"><span data-stu-id="44f1f-112">However, they also create their own set of security issues that must be addressed.</span></span> <span data-ttu-id="44f1f-113">Nous vous recommandons de prendre en compte les conseils de sécurité suivants lorsque vous configurez DaRT.</span><span class="sxs-lookup"><span data-stu-id="44f1f-113">We recommend that you consider the following security tips when you configure DaRT.</span></span>

## <span data-ttu-id="44f1f-114">Pour garantir la sécurité lors de la création de l’image de récupération DaRT</span><span class="sxs-lookup"><span data-stu-id="44f1f-114">To help maintain security when you create the DaRT recovery image</span></span>


<span data-ttu-id="44f1f-115">Lorsque vous créez l’image de récupération DaRT, vous pouvez sélectionner les outils que vous souhaitez inclure.</span><span class="sxs-lookup"><span data-stu-id="44f1f-115">When you are creating the DaRT recovery image, you can select the tools that you want to include.</span></span> <span data-ttu-id="44f1f-116">Pour des raisons de sécurité, vous souhaiterez peut-être limiter l’accès de l’utilisateur final aux outils DaRT plus puissants, tels que l’effacement de disque et Locksmith.</span><span class="sxs-lookup"><span data-stu-id="44f1f-116">For security reasons, you might want to restrict end-user access to the more powerful DaRT tools, such as Disk Wipe and Locksmith.</span></span> <span data-ttu-id="44f1f-117">Dans DaRT7, vous pouvez désactiver certains outils lors de la configuration tout en les rendant accessibles aux agents de support technique lorsque l’utilisateur final démarre la fonctionnalité de connexion à distance.</span><span class="sxs-lookup"><span data-stu-id="44f1f-117">In DaRT7, you can disable certain tools during configuration and still make them available to helpdesk agents when the end user starts the Remote Connection feature.</span></span>

<span data-ttu-id="44f1f-118">Vous pouvez même configurer l’image DaRT de telle sorte que la possibilité de démarrer une session de connexion à distance est le seul outil disponible pour un utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="44f1f-118">You can even configure the DaRT image so that the option to start a remote connection session is the only tool available to an end user.</span></span>

<span data-ttu-id="44f1f-119">**Important**  Une fois la connexion distante établie, tous les outils que vous avez inclus dans l’image de récupération, y compris ceux qui ne sont pas disponibles pour l’utilisateur final, deviennent disponibles pour l’agent du support technique fonctionnant sur l’ordinateur de l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="44f1f-119">**Important** After the remote connection is established, all the tools that you included in the recovery image, including those unavailable to the end user, will become available to the helpdesk agent working on the end–user computer.</span></span>

 

<span data-ttu-id="44f1f-120">Pour plus d’informations sur l’ajout d’outils dans l’image de récupération DaRT, voir [utilisation de l’Assistant image de récupération DART pour créer l’image de récupération](how-to-use-the-dart-recovery-image-wizard-to-create-the-recovery-image-dart-7.md).</span><span class="sxs-lookup"><span data-stu-id="44f1f-120">For more information about including tools in the DaRT recovery image, see [How to Use the DaRT Recovery Image Wizard to Create the Recovery Image](how-to-use-the-dart-recovery-image-wizard-to-create-the-recovery-image-dart-7.md).</span></span>

## <span data-ttu-id="44f1f-121">Pour garantir la sécurité par le chiffrement de l’image de récupération DaRT</span><span class="sxs-lookup"><span data-stu-id="44f1f-121">To help maintain security by encrypting the DaRT recovery image</span></span>


<span data-ttu-id="44f1f-122">Si vous utilisez l’une des options de déploiement nouvelles dans DaRT7, par exemple, l’enregistrement sur un lecteur flash USB ou la création d’une partition distante ou d’une partition de récupération, vous pouvez inclure la méthode de chiffrement de lecteur préférée de votre entreprise sur la norme ISO.</span><span class="sxs-lookup"><span data-stu-id="44f1f-122">If you use one of the deployment options new in DaRT7, for example, saving to a USB flash drive or creating a remote partition or a recovery partition, you can include your company’s preferred method of drive encryption on the ISO.</span></span> <span data-ttu-id="44f1f-123">Cela permet de s’assurer qu’un utilisateur final ne peut pas utiliser les fonctionnalités de DaRT pour accéder à l’image de récupération.</span><span class="sxs-lookup"><span data-stu-id="44f1f-123">This will help make sure that an end user cannot use the functionality of DaRT should they gain access to the recovery image.</span></span> <span data-ttu-id="44f1f-124">Par ailleurs, il est également certain que les utilisateurs non autorisés ne peuvent pas démarrer dans DaRT sur des ordinateurs qui appartiennent à une autre personne.</span><span class="sxs-lookup"><span data-stu-id="44f1f-124">And it will also make sure that unauthorized users cannot boot into DaRT on computers that belong to someone else.</span></span>

<span data-ttu-id="44f1f-125">Votre méthode de chiffrement doit être déployée et activée sur tous les ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="44f1f-125">Your encryption method should be deployed and enabled in all computers.</span></span>

<span data-ttu-id="44f1f-126">**Remarques**  DaRT7 prend en charge BitLocker en mode natif.</span><span class="sxs-lookup"><span data-stu-id="44f1f-126">**Note** DaRT7 supports BitLocker natively.</span></span>

 

## <span data-ttu-id="44f1f-127">Pour garantir la sécurité entre deux ordinateurs lors de la connexion à distance</span><span class="sxs-lookup"><span data-stu-id="44f1f-127">To help maintain security between two computers during Remote Connection</span></span>


<span data-ttu-id="44f1f-128">Par défaut, la communication entre deux ordinateurs ayant établi une session de **connexion à distance** n’est pas chiffrée.</span><span class="sxs-lookup"><span data-stu-id="44f1f-128">By default, the communication between two computers that have established a **Remote Connection** session may not be encrypted.</span></span> <span data-ttu-id="44f1f-129">Par conséquent, pour renforcer la sécurité entre les deux ordinateurs, nous vous conseillons de faire en sorte que les deux ordinateurs font partie du même réseau.</span><span class="sxs-lookup"><span data-stu-id="44f1f-129">Therefore, to help maintain security between the two computers, we recommend that both computers are a part of the same network.</span></span>

## <span data-ttu-id="44f1f-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="44f1f-130">Related topics</span></span>


[<span data-ttu-id="44f1f-131">Opérations de DaRT7.0</span><span class="sxs-lookup"><span data-stu-id="44f1f-131">Operations for DaRT 7.0</span></span>](operations-for-dart-70-new-ia.md)

 

 





