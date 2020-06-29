---
title: Considérations relatives à la sécurité pour DaRT8.0
description: Considérations relatives à la sécurité pour DaRT8.0
author: dansimp
ms.assetid: 45ef8164-fee7-41a1-9a36-de4e3264e7a8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 02d32d926c0def7d33bebd399cd380eed4e8385e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804422"
---
# <span data-ttu-id="a19b7-103">Considérations relatives à la sécurité pour DaRT8.0</span><span class="sxs-lookup"><span data-stu-id="a19b7-103">Security Considerations for DaRT 8.0</span></span>


<span data-ttu-id="a19b7-104">Cette rubrique fournit une vue d’ensemble des comptes et des groupes, des fichiers journaux et d’autres considérations en matière de sécurité pour Microsoft Diagnostics et les outils de récupération (DaRT) 8,0.</span><span class="sxs-lookup"><span data-stu-id="a19b7-104">This topic contains a brief overview about the accounts and groups, log files, and other security-related considerations for Microsoft Diagnostics and Recovery Toolset (DaRT) 8.0.</span></span> <span data-ttu-id="a19b7-105">Pour plus d’informations, suivez les liens fournis dans cet article.</span><span class="sxs-lookup"><span data-stu-id="a19b7-105">For more information, follow the links within this article.</span></span>

## <span data-ttu-id="a19b7-106">Considérations générales en matière de sécurité</span><span class="sxs-lookup"><span data-stu-id="a19b7-106">General security considerations</span></span>


<span data-ttu-id="a19b7-107">**Comprenez les risques en matière de sécurité**.</span><span class="sxs-lookup"><span data-stu-id="a19b7-107">**Understand the security risks**.</span></span> <span data-ttu-id="a19b7-108">Le DaRT 8,0 inclut des fonctionnalités qui permettent à un administrateur ou à un service de support technique d’exécuter les outils DaRT à distance pour résoudre les problèmes sur un ordinateur d’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="a19b7-108">DaRT 8.0 includes functionality that lets an administrator or a help desk worker run the DaRT tools remotely to resolve problems on an end-user computer.</span></span> <span data-ttu-id="a19b7-109">De plus, vous pouvez enregistrer l’image ISO (International Organization for Standardization) sur un lecteur flash USB ou placer l’image ISO sur un réseau afin d’inclure son contenu comme partition de récupération sur le disque dur de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="a19b7-109">In addition, you can save the International Organization for Standardization (ISO) image to a USB flash drive or put the ISO image on a network to include its contents as a recovery partition on a computer’s hard disk.</span></span> <span data-ttu-id="a19b7-110">Ces fonctionnalités permettent d’offrir une plus grande souplesse et de créer des risques de sécurité potentiels que vous devez prendre en compte lors de la configuration de DaRT.</span><span class="sxs-lookup"><span data-stu-id="a19b7-110">These capabilities provide flexibility, but also create potential security risks that you should consider when configuring DaRT.</span></span>

<span data-ttu-id="a19b7-111">**Sécurisez vos ordinateurs de façon sécurisée**.</span><span class="sxs-lookup"><span data-stu-id="a19b7-111">**Physically secure your computers**.</span></span> <span data-ttu-id="a19b7-112">Lorsque des administrateurs et des travailleurs de bureau d’assistance ne sont pas physiquement sur leur ordinateur, ils doivent verrouiller leurs ordinateurs et utiliser un écran de veille sécurisé.</span><span class="sxs-lookup"><span data-stu-id="a19b7-112">When administrators and help desk workers are not physically at their computers, they should lock their computers and use a secured screen saver.</span></span>

<span data-ttu-id="a19b7-113">**Appliquez les mises à jour de sécurité les plus récentes à tous les ordinateurs**.</span><span class="sxs-lookup"><span data-stu-id="a19b7-113">**Apply the most recent security updates to all computers**.</span></span> <span data-ttu-id="a19b7-114">Restez informé des nouvelles mises à jour de systèmes d’exploitation en vous abonnant au service de notification de sécurité ( <https://go.microsoft.com/fwlink/?LinkId=28819> ).</span><span class="sxs-lookup"><span data-stu-id="a19b7-114">Stay informed about new updates for operating systems by subscribing to the Security Notification service (<https://go.microsoft.com/fwlink/?LinkId=28819>).</span></span>

## <span data-ttu-id="a19b7-115">Limiter l’accès des utilisateurs finaux aux outils DaRT</span><span class="sxs-lookup"><span data-stu-id="a19b7-115">Limit end-user access to DaRT tools</span></span>


<span data-ttu-id="a19b7-116">Lorsque vous créez l’image de récupération DaRT, vous pouvez sélectionner les outils que vous souhaitez inclure.</span><span class="sxs-lookup"><span data-stu-id="a19b7-116">When you are creating the DaRT recovery image, you can select the tools that you want to include.</span></span> <span data-ttu-id="a19b7-117">Pour des raisons de sécurité, vous souhaiterez peut-être limiter l’accès de l’utilisateur final aux outils DaRT plus puissants, tels que l’effacement de disque et Locksmith.</span><span class="sxs-lookup"><span data-stu-id="a19b7-117">For security reasons, you might want to restrict end-user access to the more powerful DaRT tools, such as Disk Wipe and Locksmith.</span></span> <span data-ttu-id="a19b7-118">Dans DaRT 8,0, vous pouvez désactiver certains outils lors de la configuration tout en les rendant accessibles aux travailleurs du Bureau lorsque l’utilisateur final démarre la fonction de connexion à distance.</span><span class="sxs-lookup"><span data-stu-id="a19b7-118">In DaRT 8.0, you can disable certain tools during configuration and still make them available to help desk workers when the end user starts the Remote Connection feature.</span></span>

<span data-ttu-id="a19b7-119">Vous pouvez même configurer l’image DaRT de telle sorte que la possibilité de démarrer une session de connexion à distance est le seul outil disponible pour un utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="a19b7-119">You can even configure the DaRT image so that the option to start a remote connection session is the only tool available to an end user.</span></span>

<span data-ttu-id="a19b7-120">**Important**  Une fois la connexion distante établie, tous les outils que vous avez inclus dans l’image de récupération, y compris ceux qui ne sont pas disponibles pour l’utilisateur final, sont mis à la disposition de tout travailleur du support technique qui travaille sur l’ordinateur de l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="a19b7-120">**Important** After the remote connection is established, all the tools that you included in the recovery image, including those unavailable to the end user, will become available to any help desk worker who is working on the end–user computer.</span></span>

 

<span data-ttu-id="a19b7-121">Pour plus d’informations sur l’ajout d’outils dans l’image de récupération DaRT, voir [vue d’ensemble des outils dans dart 8,0](overview-of-the-tools-in-dart-80-dart-8.md).</span><span class="sxs-lookup"><span data-stu-id="a19b7-121">For more information about including tools in the DaRT recovery image, see [Overview of the Tools in DaRT 8.0](overview-of-the-tools-in-dart-80-dart-8.md).</span></span>

## <span data-ttu-id="a19b7-122">Sécuriser l’image de récupération DaRT</span><span class="sxs-lookup"><span data-stu-id="a19b7-122">Secure the DaRT recovery image</span></span>


<span data-ttu-id="a19b7-123">Si vous déployez l’image de récupération DaRT en l’enregistrant sur un disque mémoire USB ou en créant une partition distante ou une partition de récupération, vous souhaiterez peut-être inclure la méthode de chiffrement de lecteur préférée de votre entreprise sur la norme ISO.</span><span class="sxs-lookup"><span data-stu-id="a19b7-123">If you deploy the DaRT recovery image by saving it to a USB flash drive or by creating a remote partition or a recovery partition, you might want to include your company’s preferred method of drive encryption on the ISO.</span></span> <span data-ttu-id="a19b7-124">Le chiffrement de l’ISO permet aux utilisateurs finaux de s’assurer que les utilisateurs finaux ne peuvent pas utiliser la fonctionnalité DaRT s’ils accèdent à l’image de récupération, de sorte que les utilisateurs non autorisés ne peuvent pas démarrer dans DaRT sur des ordinateurs qui appartiennent à une autre personne.</span><span class="sxs-lookup"><span data-stu-id="a19b7-124">Encrypting the ISO helps to ensure that end users cannot use DaRT functionality if they were to gain access to the recovery image, and it ensures that unauthorized users cannot boot into DaRT on computers that belong to someone else.</span></span> <span data-ttu-id="a19b7-125">Si vous utilisez une méthode de chiffrement, assurez-vous de la déployer et de l’activer sur tous les ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="a19b7-125">If you use an encryption method, be sure to deploy and enable it in all computers.</span></span>

<span data-ttu-id="a19b7-126">**Remarques**  Le DaRT 8,0 prend en charge BitLocker en mode natif.</span><span class="sxs-lookup"><span data-stu-id="a19b7-126">**Note** DaRT 8.0 supports BitLocker natively.</span></span>

 

<span data-ttu-id="a19b7-127">Pour inclure le chiffrement de lecteur, ajoutez les fichiers de solution de chiffrement lors de la création de l’image de récupération.</span><span class="sxs-lookup"><span data-stu-id="a19b7-127">To include drive encryption, add the encryption solution files when you create the recovery image.</span></span> <span data-ttu-id="a19b7-128">Votre solution de chiffrement doit être capable de s’exécuter sur WinPE.</span><span class="sxs-lookup"><span data-stu-id="a19b7-128">Your encryption solution must be able to run on WinPE.</span></span> <span data-ttu-id="a19b7-129">Les utilisateurs finaux qui démarrent à partir de l’ISO peuvent alors accéder à cette solution de chiffrement et débloquer le lecteur.</span><span class="sxs-lookup"><span data-stu-id="a19b7-129">End users who boot from the ISO are then able to access that encryption solution and unblock the drive.</span></span>

## <span data-ttu-id="a19b7-130">Préservation de la sécurité entre deux ordinateurs lorsque vous utilisez une connexion à distance.</span><span class="sxs-lookup"><span data-stu-id="a19b7-130">Maintain security between two computers when you use Remote Connection</span></span>


<span data-ttu-id="a19b7-131">Par défaut, la communication entre deux ordinateurs ayant établi une session de **connexion à distance** n’est pas chiffrée.</span><span class="sxs-lookup"><span data-stu-id="a19b7-131">By default, the communication between two computers that have established a **Remote Connection** session may not be encrypted.</span></span> <span data-ttu-id="a19b7-132">Par conséquent, pour renforcer la sécurité entre les deux ordinateurs, nous vous conseillons de faire en sorte que les deux ordinateurs font partie du même réseau.</span><span class="sxs-lookup"><span data-stu-id="a19b7-132">Therefore, to help maintain security between the two computers, we recommend that both computers are a part of the same network.</span></span>

## <span data-ttu-id="a19b7-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a19b7-133">Related topics</span></span>


[<span data-ttu-id="a19b7-134">Sécurité et confidentialité pour DaRT8.0</span><span class="sxs-lookup"><span data-stu-id="a19b7-134">Security and Privacy for DaRT 8.0</span></span>](security-and-privacy-for-dart-80-dart-8.md)

 

 





