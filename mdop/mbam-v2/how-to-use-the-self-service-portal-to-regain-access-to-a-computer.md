---
title: Utilisation du portail libre-service pour accéder de nouveau à un ordinateur
description: Utilisation du portail libre-service pour accéder de nouveau à un ordinateur
author: dansimp
ms.assetid: bcf095de-0237-4bb0-b450-da8fb6d6f3d0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4abcffcf35e09bd5e24f4715a38dca74518ba29e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811538"
---
# <span data-ttu-id="0de95-103">Utilisation du portail libre-service pour accéder de nouveau à un ordinateur</span><span class="sxs-lookup"><span data-stu-id="0de95-103">How to Use the Self-Service Portal to Regain Access to a Computer</span></span>


<span data-ttu-id="0de95-104">Si les utilisateurs finaux se bloquent pas de Windows par BitLocker, car ils ont oublié leur mot de passe ou leur code confidentiel, ou parce qu’ils ont modifié des fichiers du système d’exploitation ou modifié le BIOS ou le module de plateforme sécurisée (TPM), ils peuvent utiliser le portail libre-service pour accéder à Windows sans demander à leur support technique.</span><span class="sxs-lookup"><span data-stu-id="0de95-104">If end users get locked out of Windows by BitLocker because they forgot their password or PIN, or because they changed operating system files or changed the BIOS or the Trusted Platform Module (TPM), they can use the Self-Service Portal to regain access to Windows without having to ask their Help Desk for assistance.</span></span>

<span data-ttu-id="0de95-105">**Remarques**  Si l’administrateur informatique a configuré une période de temporisation de l’état de la session IIS, un message s’affiche 60 secondes avant le délai d’expiration.</span><span class="sxs-lookup"><span data-stu-id="0de95-105">**Note** If the IT administrator configured an IIS Session State time-out, a message is displayed 60 seconds prior to the time-out.</span></span>

 

<span data-ttu-id="0de95-106">**Remarques**  Ces instructions sont rédigées du point de vue des utilisateurs finaux, et inversement.</span><span class="sxs-lookup"><span data-stu-id="0de95-106">**Note** These instructions are written for and from the perspective of end users.</span></span>

 

**<span data-ttu-id="0de95-107">Pour pouvoir utiliser le portail libre-service pour accéder à un ordinateur</span><span class="sxs-lookup"><span data-stu-id="0de95-107">To use the Self-Service Portal to regain access to a computer</span></span>**

1.  <span data-ttu-id="0de95-108">Dans le champ **KeyId de récupération** , entrez au moins huit l’ID de clé bitlocker de 32 chiffres qui s’affiche dans l’écran de récupération BitLocker de votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="0de95-108">In the **Recovery KeyId** field, enter a minimum of eight of the 32-digit BitLocker Key ID that is displayed on the BitLocker recovery screen of your computer.</span></span>

    <span data-ttu-id="0de95-109">**Remarques**  Si les huit premiers chiffres correspondent à plusieurs clés, un message s’affiche et vous demande d’entrer tous les 32 chiffres de l’ID de la clé de récupération.</span><span class="sxs-lookup"><span data-stu-id="0de95-109">**Note** If the first eight digits match multiple keys, a message displays that requires you to enter all 32 digits of the recovery key ID.</span></span>

     

2.  <span data-ttu-id="0de95-110">Dans le champ **raison** , sélectionnez une raison pour votre demande de clé de récupération.</span><span class="sxs-lookup"><span data-stu-id="0de95-110">In the **Reason** field, select a reason for your request for the recovery key.</span></span>

3.  <span data-ttu-id="0de95-111">Cliquez sur **obtenir la clé**.</span><span class="sxs-lookup"><span data-stu-id="0de95-111">Click **Get Key**.</span></span> <span data-ttu-id="0de95-112">Votre clé de récupération BitLocker est affichée dans le champ «votre clé de récupération BitLocker».</span><span class="sxs-lookup"><span data-stu-id="0de95-112">Your BitLocker recovery key is displayed in the “Your BitLocker Recovery Key” field.</span></span>

4.  <span data-ttu-id="0de95-113">Entrez le code de l' 48 sur l’écran de récupération BitLocker sur votre ordinateur pour accéder à l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="0de95-113">Enter the 48-digit code into the BitLocker recovery screen on your computer to regain access to the computer.</span></span>

## <span data-ttu-id="0de95-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0de95-114">Related topics</span></span>


[<span data-ttu-id="0de95-115">Gestion de BitLocker avec MBAM</span><span class="sxs-lookup"><span data-stu-id="0de95-115">Performing BitLocker Management with MBAM</span></span>](performing-bitlocker-management-with-mbam-mbam-2.md)

 

 





