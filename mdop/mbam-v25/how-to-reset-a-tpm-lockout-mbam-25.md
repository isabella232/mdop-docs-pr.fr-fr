---
title: Réinitialisation d'un verrouillage TPM
description: Réinitialisation d'un verrouillage TPM
author: dansimp
ms.assetid: dd20a728-c52e-48e6-9f6c-1311c71dee74
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f5aea277e80c54fb01d1a6c00b62f0c617d1ad12
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809887"
---
# <span data-ttu-id="085f0-103">Réinitialisation d'un verrouillage TPM</span><span class="sxs-lookup"><span data-stu-id="085f0-103">How to Reset a TPM Lockout</span></span>


<span data-ttu-id="085f0-104">Cette rubrique explique comment utiliser le site Web d’administration et de contrôle (également appelé support technique) pour réinitialiser un verrouillage du TPM.</span><span class="sxs-lookup"><span data-stu-id="085f0-104">This topic explains how to use the Administration and Monitoring Website (also referred to as the Help Desk) to reset a TPM lockout.</span></span> <span data-ttu-id="085f0-105">Les verrouillages de TPM peuvent se produire si un utilisateur final entre trop de fois le code confidentiel incorrect.</span><span class="sxs-lookup"><span data-stu-id="085f0-105">TPM lockouts can occur if an end user enters the incorrect PIN too many times.</span></span> <span data-ttu-id="085f0-106">Le nombre de fois qu’un utilisateur peut entrer un code confidentiel incorrect avant que les verrouillages du TPM ne varient d’un fabricant au fabricant.</span><span class="sxs-lookup"><span data-stu-id="085f0-106">The number of times that a user can enter an incorrect PIN before the TPM locks varies from manufacturer to manufacturer.</span></span>

<span data-ttu-id="085f0-107">À partir de la zone **gérer le module de plateforme sécurisée** du site Web d’administration et de surveillance, vous pouvez accéder au système de données de récupération de clés centralisées, qui fournit un fichier de mot de passe de propriétaire du TPM lorsque vous fournissez un ID d’ordinateur et un identificateur d’utilisateur associé.</span><span class="sxs-lookup"><span data-stu-id="085f0-107">From the **Manage TPM** area of the Administration and Monitoring Website, you can access the centralized Key Recovery data system, which provides a TPM owner password file when you supply a computer ID and associated user identifier.</span></span>

<span data-ttu-id="085f0-108">Pour accéder à la zone gérer le module de plateforme sécurisée du site Web d’administration et de surveillance, vous devez disposer du rôle utilisateurs du support technique MBAM ou du rôle utilisateurs avancés du support technique MBAM.</span><span class="sxs-lookup"><span data-stu-id="085f0-108">To access the Manage TPM area of the Administration and Monitoring Website, you must be assigned the MBAM Helpdesk Users role or the MBAM Advanced Helpdesk Users role.</span></span> <span data-ttu-id="085f0-109">Ces rôles sont des groupes que les administrateurs créent dans Active Directory.</span><span class="sxs-lookup"><span data-stu-id="085f0-109">These roles are groups that administrators create in Active Directory.</span></span> <span data-ttu-id="085f0-110">Vous pouvez utiliser n’importe quel nom pour ces groupes.</span><span class="sxs-lookup"><span data-stu-id="085f0-110">You can use any name for these groups.</span></span> <span data-ttu-id="085f0-111">Pour plus d’informations, reportez-vous [à planification pour les comptes et groupes MBAM 2,5](planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles).</span><span class="sxs-lookup"><span data-stu-id="085f0-111">For more information, see [Planning for MBAM 2.5 Groups and Accounts](planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles).</span></span>

<span data-ttu-id="085f0-112">Pour plus d’informations sur la propriété MBAM et TPM, voir [considérations relatives à la sécurité dans MBAM 2,5](mbam-25-security-considerations.md#bkmk-tpm).</span><span class="sxs-lookup"><span data-stu-id="085f0-112">For information about MBAM and TPM ownership, see [MBAM 2.5 Security Considerations](mbam-25-security-considerations.md#bkmk-tpm).</span></span>

**<span data-ttu-id="085f0-113">Pour réinitialiser un verrouillage du TPM</span><span class="sxs-lookup"><span data-stu-id="085f0-113">To reset a TPM lockout</span></span>**

1.  <span data-ttu-id="085f0-114">Ouvrez un navigateur Web, puis accédez au **site Web d’administration et de surveillance**.</span><span class="sxs-lookup"><span data-stu-id="085f0-114">Open a web browser and navigate to the **Administration and Monitoring Website**.</span></span>

2.  <span data-ttu-id="085f0-115">Dans le volet gauche, cliquez sur **gérer le TPM** pour ouvrir la page gérer le module de **plateforme sécurisée** .</span><span class="sxs-lookup"><span data-stu-id="085f0-115">In the left pane, click **Manage TPM** to open the **Manage TPM** page.</span></span>

3.  <span data-ttu-id="085f0-116">Entrez le nom de domaine complet de l’ordinateur et le nom de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="085f0-116">Enter the fully qualified domain name for the computer and the computer name.</span></span>

4.  <span data-ttu-id="085f0-117">Entrez le nom d’utilisateur et le domaine d’ouverture de session Windows de l’utilisateur final pour récupérer le fichier de mots de passe du propriétaire du TPM.</span><span class="sxs-lookup"><span data-stu-id="085f0-117">Enter the end user’s Windows log-on domain and user name to retrieve the TPM owner password file.</span></span>

    <span data-ttu-id="085f0-118">**Remarques**  Si vous vous trouvez dans le groupe utilisateurs du support technique avancé MBAM, les champs utilisateur et ID d’utilisateur ne sont pas obligatoires.</span><span class="sxs-lookup"><span data-stu-id="085f0-118">**Note** If you are in the MBAM Advanced Helpdesk Users group, the user domain and user ID fields are not required.</span></span>

     

5.  <span data-ttu-id="085f0-119">Dans la liste des **fichiers de mots de passe du propriétaire du module de plateforme sécurisée** , sélectionnez une raison pour la demande, puis cliquez sur **valider**.</span><span class="sxs-lookup"><span data-stu-id="085f0-119">From the **Reason for requesting TPM owner password file** list, select a reason for the request, and click **Submit**.</span></span>

    <span data-ttu-id="085f0-120">MBAM renvoie l’une des valeurs suivantes:</span><span class="sxs-lookup"><span data-stu-id="085f0-120">MBAM returns one of the following:</span></span>

    -   <span data-ttu-id="085f0-121">Message d’erreur s’il n’existe aucun fichier de mot de passe de propriétaire de TPM correspondant</span><span class="sxs-lookup"><span data-stu-id="085f0-121">An error message if no matching TPM owner password file is found</span></span>

    -   <span data-ttu-id="085f0-122">Fichier de mot de passe du propriétaire du TPM de l’ordinateur soumis</span><span class="sxs-lookup"><span data-stu-id="085f0-122">The TPM owner password file for the submitted computer</span></span>

    <span data-ttu-id="085f0-123">Après l’extraction du mot de passe du propriétaire du TPM, le mot de passe propriétaire est affiché.</span><span class="sxs-lookup"><span data-stu-id="085f0-123">After the TPM owner password is retrieved, the owner password is displayed.</span></span>

6.  <span data-ttu-id="085f0-124">Pour enregistrer le mot de passe dans un fichier. TPM, cliquez sur le bouton **Enregistrer** .</span><span class="sxs-lookup"><span data-stu-id="085f0-124">To save the password to a .tpm file, click the **Save** button.</span></span>

7.  <span data-ttu-id="085f0-125">Dans la zone **gérer le module de plateforme sécurisée** du **site Web d’administration et de surveillance**, sélectionnez l’option **réinitialisation du verrouillage du TPM** et indiquez le fichier de mot de passe du propriétaire du TPM.</span><span class="sxs-lookup"><span data-stu-id="085f0-125">In the **Manage TPM** area of the **Administration and Monitoring Website**, select the **Reset TPM lockout** option and provide the TPM owner password file.</span></span>

    <span data-ttu-id="085f0-126">Le verrouillage du TPM est réinitialisé et l’accès de l’utilisateur final est restauré.</span><span class="sxs-lookup"><span data-stu-id="085f0-126">The TPM lockout is reset and the end user’s access is restored.</span></span>

    <span data-ttu-id="085f0-127">**Important**  Ne donnez pas à la valeur de hachage du TPM ou au fichier de mot de passe du propriétaire du TPM les utilisateurs finaux.</span><span class="sxs-lookup"><span data-stu-id="085f0-127">**Important** Do not give the TPM hash value or TPM owner password file to end users.</span></span> <span data-ttu-id="085f0-128">Les informations sur le TPM ne changent pas, ce qui donne aux utilisateurs finaux des risques en matière de sécurité.</span><span class="sxs-lookup"><span data-stu-id="085f0-128">Because the TPM information does not change, giving the file to end users creates a security risk.</span></span>

     



## <span data-ttu-id="085f0-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="085f0-129">Related topics</span></span>


[<span data-ttu-id="085f0-130">Gestion de BitLocker avec MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="085f0-130">Performing BitLocker Management with MBAM 2.5</span></span>](performing-bitlocker-management-with-mbam-25.md)

 

## <span data-ttu-id="085f0-131">Vous avez une suggestion pour MBAM?</span><span class="sxs-lookup"><span data-stu-id="085f0-131">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="085f0-132">Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)</span><span class="sxs-lookup"><span data-stu-id="085f0-132">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="085f0-133">Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="085f0-133">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





