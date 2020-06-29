---
title: Utilisation du portail libre-service pour accéder de nouveau à un ordinateur
description: Utilisation du portail libre-service pour accéder de nouveau à un ordinateur
author: dansimp
ms.assetid: 3c24b13a-d1b1-4763-8ac0-0b2db46267e3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cde9c71a957a5270d69aa8388455895f1cb2432b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811915"
---
# <span data-ttu-id="44ed5-103">Utilisation du portail libre-service pour accéder de nouveau à un ordinateur</span><span class="sxs-lookup"><span data-stu-id="44ed5-103">How to Use the Self-Service Portal to Regain Access to a Computer</span></span>


<span data-ttu-id="44ed5-104">Le portail libre-service est un site Web que les administrateurs informatiques configurent dans le cadre de leur déploiement de 2,5 d’administration et de surveillance de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="44ed5-104">The Self-Service Portal is a website that IT administrators configure as part of their Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 deployment.</span></span> <span data-ttu-id="44ed5-105">Le site Web permet aux utilisateurs finaux de pouvoir accéder de manière indépendante à leurs ordinateurs s’ils sont bloqués.</span><span class="sxs-lookup"><span data-stu-id="44ed5-105">The website enables end users to independently regain access to their computers if they get locked out of Windows.</span></span> <span data-ttu-id="44ed5-106">Le portail libre-service ne nécessite aucune assistance de la part du personnel du support technique.</span><span class="sxs-lookup"><span data-stu-id="44ed5-106">The Self-Service Portal requires no assistance from Help Desk staff.</span></span>

<span data-ttu-id="44ed5-107">Les instructions suivantes sont rédigées du point de vue des utilisateurs finaux, mais les informations peuvent être utiles pour les administrateurs informatiques.</span><span class="sxs-lookup"><span data-stu-id="44ed5-107">The following instructions are written from the perspective of end users, but the information may be useful for IT administrators to understand.</span></span>

<span data-ttu-id="44ed5-108">**Important**  Un utilisateur final doit avoir réussi à se connecter à l’ordinateur (pas à distance) au moins une fois pour pouvoir récupérer sa clé via le portail libre-service.</span><span class="sxs-lookup"><span data-stu-id="44ed5-108">**Important** An end user must have physically logged on to the computer (not remotely) at least one time successfully to be able to recover their key using the Self-Service Portal.</span></span> <span data-ttu-id="44ed5-109">Sinon, ils doivent utiliser le portail du support technique pour la récupération de clés.</span><span class="sxs-lookup"><span data-stu-id="44ed5-109">Otherwise, they must use the Helpdesk Portal for key recovery.</span></span>

 

<span data-ttu-id="44ed5-110">Les utilisateurs finaux peuvent être confrontés aux verrouillages s’ils:</span><span class="sxs-lookup"><span data-stu-id="44ed5-110">End users may experience lockouts if they:</span></span>

-   <span data-ttu-id="44ed5-111">Oublier son mot de passe ou son code confidentiel</span><span class="sxs-lookup"><span data-stu-id="44ed5-111">Forget their password or PIN</span></span>

-   <span data-ttu-id="44ed5-112">Modification des fichiers du système d’exploitation, du BIOS ou du module de plateforme sécurisée (TPM)</span><span class="sxs-lookup"><span data-stu-id="44ed5-112">Change operating system files, the BIOS, or the Trusted Platform Module (TPM)</span></span>

<span data-ttu-id="44ed5-113">**Remarques**  Si l’administrateur informatique a configuré une période de temporisation de l’état de session IIS, un message s’affiche dans le portail libre-service de 60 secondes avant le délai d’expiration.</span><span class="sxs-lookup"><span data-stu-id="44ed5-113">**Note** If the IT administrator configured an IIS Session State time-out, a message is displayed in the Self-Service Portal 60 seconds prior to the time-out.</span></span>

 

**<span data-ttu-id="44ed5-114">Pour pouvoir utiliser le portail libre-service pour accéder à un ordinateur</span><span class="sxs-lookup"><span data-stu-id="44ed5-114">To use the Self-Service Portal to regain access to a computer</span></span>**

1.  <span data-ttu-id="44ed5-115">Dans le champ **KeyId de récupération** , entrez au moins huit l’ID de clé bitlocker de 32 chiffres qui s’affiche dans l’écran de récupération BitLocker de votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="44ed5-115">In the **Recovery KeyId** field, enter a minimum of eight of the 32-digit BitLocker Key ID that is displayed on the BitLocker recovery screen of your computer.</span></span> <span data-ttu-id="44ed5-116">Si les huit premiers chiffres correspondent à plusieurs clés, un message s’affiche et vous demande d’entrer tous les 32 chiffres de l’ID de la clé de récupération.</span><span class="sxs-lookup"><span data-stu-id="44ed5-116">If the first eight digits match multiple keys, a message displays that requires you to enter all 32 digits of the recovery key ID.</span></span>

2.  <span data-ttu-id="44ed5-117">Dans le champ **raison** , sélectionnez une raison pour votre demande de clé de récupération.</span><span class="sxs-lookup"><span data-stu-id="44ed5-117">In the **Reason** field, select a reason for your request for the recovery key.</span></span>

3.  <span data-ttu-id="44ed5-118">Cliquez sur **obtenir la clé**.</span><span class="sxs-lookup"><span data-stu-id="44ed5-118">Click **Get Key**.</span></span> <span data-ttu-id="44ed5-119">Votre clé de récupération BitLocker est affichée dans le champ **votre clé de récupération BitLocker** .</span><span class="sxs-lookup"><span data-stu-id="44ed5-119">Your BitLocker recovery key is displayed in the **Your BitLocker Recovery Key** field.</span></span>

4.  <span data-ttu-id="44ed5-120">Entrez le code de l' 48 sur l’écran de récupération BitLocker sur votre ordinateur pour accéder à l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="44ed5-120">Enter the 48-digit code into the BitLocker recovery screen on your computer to regain access to the computer.</span></span>



## <span data-ttu-id="44ed5-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="44ed5-121">Related topics</span></span>


[<span data-ttu-id="44ed5-122">Gestion de BitLocker avec MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="44ed5-122">Performing BitLocker Management with MBAM 2.5</span></span>](performing-bitlocker-management-with-mbam-25.md)

 
## <span data-ttu-id="44ed5-123">Vous avez une suggestion pour MBAM?</span><span class="sxs-lookup"><span data-stu-id="44ed5-123">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="44ed5-124">Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)</span><span class="sxs-lookup"><span data-stu-id="44ed5-124">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="44ed5-125">Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="44ed5-125">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>
 





