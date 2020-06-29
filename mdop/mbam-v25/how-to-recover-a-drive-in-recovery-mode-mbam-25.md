---
title: Procédure de récupération d'un lecteur en mode de récupération
description: Procédure de récupération d'un lecteur en mode de récupération
author: dansimp
ms.assetid: e126eaf8-9ae7-40fe-a28e-dbd78d26859e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d15f33f461e60fceeed3acbce3a0c82b02b56f98
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809912"
---
# <span data-ttu-id="280ce-103">Procédure de récupération d'un lecteur en mode de récupération</span><span class="sxs-lookup"><span data-stu-id="280ce-103">How to Recover a Drive in Recovery Mode</span></span>


<span data-ttu-id="280ce-104">Cette rubrique explique comment utiliser le site Web d’administration et de contrôle (également appelé support technique) pour obtenir un mot de passe de récupération à mettre aux utilisateurs finaux si leur lecteur protégé par BitLocker passe en mode de récupération.</span><span class="sxs-lookup"><span data-stu-id="280ce-104">This topic explains how to use the Administration and Monitoring Website (also referred to as the Help Desk) to get a recovery password to give to end users if their BitLocker-protected drive goes into recovery mode.</span></span> <span data-ttu-id="280ce-105">Les lecteurs se trouvent dans le mode de récupération si les utilisateurs perdent ou oublient leur code confidentiel ou leur mot de passe, ou si le processeur de plateforme sécurisée (TPM) détecte des modifications apportées aux fichiers du BIOS ou de démarrage d’un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="280ce-105">Drives go into recovery mode if users lose or forget their PIN or password or if the Trusted Module Platform (TPM) chip detects changes to the BIOS or startup files of a computer.</span></span>

<span data-ttu-id="280ce-106">Pour obtenir un mot de passe de récupération, utilisez la zone de **récupération de lecteur** du site Web d’administration et de surveillance.</span><span class="sxs-lookup"><span data-stu-id="280ce-106">To get a recovery password, use the **Drive Recovery** area of the Administration and Monitoring Website.</span></span> <span data-ttu-id="280ce-107">Vous devez être attribué au rôle utilisateurs du support technique MBAM ou au rôle MBAM Advanced helpdesk Users pour accéder à cette zone du site Web.</span><span class="sxs-lookup"><span data-stu-id="280ce-107">You must be assigned the MBAM Helpdesk Users role or the MBAM Advanced Helpdesk Users role to access this area of the website.</span></span>

**<span data-ttu-id="280ce-108">Remarque</span><span class="sxs-lookup"><span data-stu-id="280ce-108">Note</span></span>**  
<span data-ttu-id="280ce-109">Il est possible que vous ayez attribué un nom différent aux rôles lorsque vous les avez créés.</span><span class="sxs-lookup"><span data-stu-id="280ce-109">You may have given these roles different names when you created them.</span></span> <span data-ttu-id="280ce-110">Pour plus d’informations, reportez-vous [à planification pour les comptes et groupes MBAM 2,5](planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles).</span><span class="sxs-lookup"><span data-stu-id="280ce-110">For more information, see [Planning for MBAM 2.5 Groups and Accounts](planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles).</span></span>



**<span data-ttu-id="280ce-111">Important</span><span class="sxs-lookup"><span data-stu-id="280ce-111">Important</span></span>**  
<span data-ttu-id="280ce-112">Expiration des mots de passe de récupération après une utilisation unique.</span><span class="sxs-lookup"><span data-stu-id="280ce-112">Recovery passwords expire after a single use.</span></span> <span data-ttu-id="280ce-113">Sur les lecteurs du système d’exploitation et les lecteurs de données fixes, la règle à utilisation unique est appliquée automatiquement.</span><span class="sxs-lookup"><span data-stu-id="280ce-113">On operating system drives and fixed data drives, the single-use rule is applied automatically.</span></span> <span data-ttu-id="280ce-114">Sur les lecteurs amovibles, il est appliqué lors de la suppression du lecteur, puis réinséré et déverrouillé sur un ordinateur qui a activé les paramètres de stratégie de groupe pour gérer les lecteurs amovibles.</span><span class="sxs-lookup"><span data-stu-id="280ce-114">On removable drives, it is applied when the drive is removed and then reinserted and unlocked on a computer that has Group Policy settings activated to manage removable drives.</span></span>



**<span data-ttu-id="280ce-115">Pour récupérer un lecteur en mode de récupération</span><span class="sxs-lookup"><span data-stu-id="280ce-115">To recover a drive in recovery mode</span></span>**

1.  <span data-ttu-id="280ce-116">Ouvrez un navigateur Web, puis accédez au **site Web d’administration et de surveillance**.</span><span class="sxs-lookup"><span data-stu-id="280ce-116">Open a web browser and navigate to the **Administration and Monitoring Website**.</span></span>

2.  <span data-ttu-id="280ce-117">Dans le volet gauche, sélectionnez **récupération de lecteur** pour ouvrir la page **récupérer l’accès à un lecteur chiffré** .</span><span class="sxs-lookup"><span data-stu-id="280ce-117">In the left pane, select **Drive Recovery** to open the **Recover access to an encrypted drive** page.</span></span>

3.  <span data-ttu-id="280ce-118">Entrez le nom d’utilisateur et le domaine d’ouverture de session Windows de l’utilisateur final pour afficher les informations de récupération.</span><span class="sxs-lookup"><span data-stu-id="280ce-118">Enter the end user’s Windows log-on domain and user name to view recovery information.</span></span>

    **<span data-ttu-id="280ce-119">Remarque</span><span class="sxs-lookup"><span data-stu-id="280ce-119">Note</span></span>**  
    <span data-ttu-id="280ce-120">Si vous vous trouvez dans le groupe utilisateurs du support technique avancé MBAM, les champs utilisateur et ID d’utilisateur ne sont pas obligatoires.</span><span class="sxs-lookup"><span data-stu-id="280ce-120">If you are in the MBAM Advanced Helpdesk Users group, the user domain and user ID fields are not required.</span></span>



4.  <span data-ttu-id="280ce-121">Entrez les huit premiers chiffres de l’ID de clé de récupération pour afficher une liste des clés de récupération correspondantes possibles, ou entrez l’ID de la clé de récupération complète pour obtenir la clé de récupération exacte.</span><span class="sxs-lookup"><span data-stu-id="280ce-121">Enter the first eight digits of the recovery key ID to see a list of possible matching recovery keys, or enter the entire recovery key ID to get the exact recovery key.</span></span>

5.  <span data-ttu-id="280ce-122">Dans la liste **raison de la déverrouillage du lecteur** , sélectionnez l’une des options prédéfinies, puis cliquez sur **valider**.</span><span class="sxs-lookup"><span data-stu-id="280ce-122">From the **Reason for Drive Unlock** list, select one of the predefined options, and then click **Submit**.</span></span>

    <span data-ttu-id="280ce-123">MBAM renvoie la valeur suivante:</span><span class="sxs-lookup"><span data-stu-id="280ce-123">MBAM returns the following:</span></span>

    -   <span data-ttu-id="280ce-124">Message d’erreur s’il n’existe aucun mot de passe de récupération correspondant</span><span class="sxs-lookup"><span data-stu-id="280ce-124">An error message if no matching recovery password is found</span></span>

    -   <span data-ttu-id="280ce-125">Plusieurs correspondances possibles si l’utilisateur possède plusieurs mots de passe de récupération correspondants</span><span class="sxs-lookup"><span data-stu-id="280ce-125">Multiple possible matches if the user has multiple matching recovery passwords</span></span>

    -   <span data-ttu-id="280ce-126">Le mot de passe de récupération et le package de récupération pour l’utilisateur soumis</span><span class="sxs-lookup"><span data-stu-id="280ce-126">The recovery password and recovery package for the submitted user</span></span>

        **<span data-ttu-id="280ce-127">Remarque</span><span class="sxs-lookup"><span data-stu-id="280ce-127">Note</span></span>**  
        <span data-ttu-id="280ce-128">Si vous récupérez un lecteur endommagé, l’option de package de récupération fournit les informations critiques de BitLocker dont il a besoin pour récupérer le lecteur.</span><span class="sxs-lookup"><span data-stu-id="280ce-128">If you are recovering a damaged drive, the recovery package option provides BitLocker with critical information that it needs to recover the drive.</span></span>



~~~
After the recovery password and recovery package are retrieved, the recovery password is displayed.
~~~

6. <span data-ttu-id="280ce-129">Pour copier le mot de passe, cliquez sur **copier la clé**, puis collez le mot de passe de récupération dans un message électronique.</span><span class="sxs-lookup"><span data-stu-id="280ce-129">To copy the password, click **Copy Key**, and then paste the recovery password into an email message.</span></span> <span data-ttu-id="280ce-130">Vous pouvez également cliquer sur **Enregistrer** pour enregistrer le mot de passe de récupération dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="280ce-130">Alternatively, click **Save** to save the recovery password to a file.</span></span>

   <span data-ttu-id="280ce-131">Lorsque l’utilisateur tape le mot de passe de récupération dans le système ou utilise le package de récupération, le lecteur est déverrouillé.</span><span class="sxs-lookup"><span data-stu-id="280ce-131">When the user types the recovery password into the system or uses the recovery package, the drive is unlocked.</span></span>



## <span data-ttu-id="280ce-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="280ce-132">Related topics</span></span>


[<span data-ttu-id="280ce-133">Gestion de BitLocker avec MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="280ce-133">Performing BitLocker Management with MBAM 2.5</span></span>](performing-bitlocker-management-with-mbam-25.md)



## <span data-ttu-id="280ce-134">Vous avez une suggestion pour MBAM?</span><span class="sxs-lookup"><span data-stu-id="280ce-134">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="280ce-135">Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)</span><span class="sxs-lookup"><span data-stu-id="280ce-135">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="280ce-136">Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="280ce-136">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





