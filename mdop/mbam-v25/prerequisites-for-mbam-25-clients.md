---
title: Conditions préalables pour les clients MBAM2.5
description: Conditions préalables pour les clients MBAM2.5
author: dansimp
ms.assetid: fc230679-9c84-4b99-a77c-bae7e7bf8145
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 04/23/2017
ms.openlocfilehash: ac5e211e5ea038f47db3d5e68155eb5af38aa231
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812072"
---
# <span data-ttu-id="7b275-103">Conditions préalables pour les clients MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="7b275-103">Prerequisites for MBAM 2.5 Clients</span></span>


<span data-ttu-id="7b275-104">Avant d’installer le logiciel client MBAM sur les ordinateurs des utilisateurs finaux, assurez-vous que votre environnement et vos ordinateurs clients répondent aux conditions préalables suivantes.</span><span class="sxs-lookup"><span data-stu-id="7b275-104">Before you install the MBAM Client software on end users' computers, ensure that your environment and the client computers meet the following prerequisites.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7b275-105">Prérequises</span><span class="sxs-lookup"><span data-stu-id="7b275-105">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="7b275-106">Détails</span><span class="sxs-lookup"><span data-stu-id="7b275-106">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7b275-107">Le domaine d’entreprise doit contenir au moins un contrôleur de domaine Windows Server 2008 (ou version ultérieure).</span><span class="sxs-lookup"><span data-stu-id="7b275-107">The enterprise domain must contain at least one Windows Server 2008 (or later) domain controller.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7b275-108">L’ordinateur client doit être connecté à l’intranet de l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="7b275-108">The client computer must be logged on to the enterprise intranet.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7b275-109">Pour les ordinateurs clients Windows 7 uniquement: chaque client doit disposer de la fonctionnalité de module de plateforme sécurisée (TPM 1,2 ou version ultérieure).</span><span class="sxs-lookup"><span data-stu-id="7b275-109">For Windows 7 client computers only: Each client must have Trusted Platform Module (TPM) capability (TPM 1.2 or later).</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7b275-110">Pour les ordinateurs clients Windows 8,1, Windows 10 ou Windows 10 version 1511 uniquement: Si vous souhaitez que MBAM puisse stocker et gérer les clés de récupération du TPM, la fonction de configuration automatique du TPM doit être désactivée, et MBAM doit être défini en tant que propriétaire du TPM avant le déploiement d’MBAM.</span><span class="sxs-lookup"><span data-stu-id="7b275-110">For Windows 8.1, Windows 10 RTM or Windows 10 version 1511 client computers only: If you want MBAM to be able to store and manage the TPM recovery keys, TPM auto-provisioning must be turned off, and MBAM must be set as the owner of the TPM before you deploy MBAM.</span></span></p>
<p><span data-ttu-id="7b275-111">Dans MBAM 2,5 SP1 uniquement, il n’est plus nécessaire de désactiver la mise en service automatique du module de plateforme sécurisée, mais vous devez vous assurer que les objets de stratégie de groupe du TPM sont définis sur not TRUSTed OwnerAuth to Active Directory.</span><span class="sxs-lookup"><span data-stu-id="7b275-111">In MBAM 2.5 SP1 only, you no longer need to turn off TPM auto-provisioning, but you must make sure that the TPM Group Policy Objects are set to not escrow TPM OwnerAuth to Active Directory.</span></span></p></td>
<td align="left"><p><a href="mbam-25-security-considerations.md#bkmk-tpm" data-raw-source="[MBAM 2.5 Security Considerations](mbam-25-security-considerations.md#bkmk-tpm)"><span data-ttu-id="7b275-112">Considérations relatives à la sécurité pour MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="7b275-112">MBAM 2.5 Security Considerations</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7b275-113">Pour Windows 10, version 1607 ou ultérieure, seules les fenêtres peuvent prendre possession du module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="7b275-113">For Windows 10, version 1607 or later, only Windows can take ownership of the TPM.</span></span> <span data-ttu-id="7b275-114">Dans addiiton, Windows ne conserve pas le mot de passe du propriétaire du TPM lors de la mise en service du module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="7b275-114">In addiiton, Windows will not retain the TPM owner password when provisioning the TPM.</span></span></p>
<p><span data-ttu-id="7b275-115">Dans MBAM 2,5 SP1, vous devez activer la configuration automatique.</span><span class="sxs-lookup"><span data-stu-id="7b275-115">In MBAM 2.5 SP1, you must turn on auto-provisioning.</span></span></p>
</p></td>
<td align="left"><p><span data-ttu-id="7b275-116">Pour en savoir <a href="https://technet.microsoft.com/itpro/windows/keep-secure/change-the-tpm-owner-password" data-raw-source="[TPM owner password](https://technet.microsoft.com/itpro/windows/keep-secure/change-the-tpm-owner-password)"> plus, voir mot de passe </a> du propriétaire du TPM.</span><span class="sxs-lookup"><span data-stu-id="7b275-116">See <a href="https://technet.microsoft.com/itpro/windows/keep-secure/change-the-tpm-owner-password" data-raw-source="[TPM owner password](https://technet.microsoft.com/itpro/windows/keep-secure/change-the-tpm-owner-password)">TPM owner password</a> for further details.</span></span>
</p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7b275-117">Le processeur du TPM doit être activé dans le BIOS et être Resettable du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="7b275-117">The TPM chip must be turned on in the BIOS and be resettable from the operating system.</span></span></p></td>
<td align="left"><p><span data-ttu-id="7b275-118">Pour plus d’informations, consultez la documentation relative au BIOS.</span><span class="sxs-lookup"><span data-stu-id="7b275-118">See the BIOS documentation for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7b275-119">Le disque dur de l’ordinateur doit avoir au moins deux partitions et doit être mis en forme avec le système de fichiers NTFS.</span><span class="sxs-lookup"><span data-stu-id="7b275-119">The computer’s hard disk must have at least two partitions and must be formatted with the NTFS file system.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7b275-120">Le disque dur de l’ordinateur doit être équipé d’un BIOS compatible avec le TPM et prenant en charge les appareils USB au démarrage de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="7b275-120">The computer’s hard disk must have a BIOS that is compatible with TPM and that supports USB devices during computer startup.</span></span></p></td>
<td align="left"><div class="alert">
<strong><span data-ttu-id="7b275-121">Remarque</span><span class="sxs-lookup"><span data-stu-id="7b275-121">Note</span></span></strong><br/><p><span data-ttu-id="7b275-122">Assurez-vous que le clavier, la vidéo ou la souris sont directement connectés et ne sont pas gérés par le biais d’un clavier, d’une vidéo ou d’un commutateur de souris (KVM).</span><span class="sxs-lookup"><span data-stu-id="7b275-122">Ensure that the keyboard, video, or mouse are directly connected and not managed through a keyboard, video, or mouse (KVM) switch.</span></span> <span data-ttu-id="7b275-123">Un commutateur KVM peut interférer avec la capacité de l’ordinateur à détecter la présence physique du matériel.</span><span class="sxs-lookup"><span data-stu-id="7b275-123">A KVM switch can interfere with the ability of the computer to detect the physical presence of hardware.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7b275-124">Si vous utilisez un proxy, il doit être visible dans le contexte système.</span><span class="sxs-lookup"><span data-stu-id="7b275-124">If you use a proxy, it must be visible in the system context.</span></span> <span data-ttu-id="7b275-125">MBAM s’exécute dans le contexte du système, et non dans le contexte de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7b275-125">MBAM runs under the system context, not the user context.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="7b275-126">Important</span><span class="sxs-lookup"><span data-stu-id="7b275-126">Important</span></span>**  
<span data-ttu-id="7b275-127">Si BitLocker a été utilisé sans MBAM, MBAM peut être installé et utiliser les informations existantes du TPM.</span><span class="sxs-lookup"><span data-stu-id="7b275-127">If BitLocker was used without MBAM, MBAM can be installed and utilize the existing TPM information.</span></span>




## <span data-ttu-id="7b275-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7b275-128">Related topics</span></span>


[<span data-ttu-id="7b275-129">Configurations prises en charge par MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="7b275-129">MBAM 2.5 Supported Configurations</span></span>](mbam-25-supported-configurations.md)

[<span data-ttu-id="7b275-130">Planification du déploiement de MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="7b275-130">Planning to Deploy MBAM 2.5</span></span>](planning-to-deploy-mbam-25.md)


## <span data-ttu-id="7b275-131">Vous avez une suggestion pour MBAM?</span><span class="sxs-lookup"><span data-stu-id="7b275-131">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="7b275-132">Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)</span><span class="sxs-lookup"><span data-stu-id="7b275-132">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span>
- <span data-ttu-id="7b275-133">Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="7b275-133">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>






