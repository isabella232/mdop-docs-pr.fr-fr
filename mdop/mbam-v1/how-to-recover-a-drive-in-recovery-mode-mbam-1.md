---
title: Procédure de récupération d'un lecteur en mode de récupération
description: Procédure de récupération d'un lecteur en mode de récupération
author: dansimp
ms.assetid: 09d27e4b-57fa-47c7-a004-8b876a49f27e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c1151ffe7453eb8d07d2aa6dcb4c41f6b3efe6de
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804614"
---
# <span data-ttu-id="8b237-103">Procédure de récupération d'un lecteur en mode de récupération</span><span class="sxs-lookup"><span data-stu-id="8b237-103">How to Recover a Drive in Recovery Mode</span></span>


<span data-ttu-id="8b237-104">Le contrôle et l’administration de BitLocker Microsoft (MBAM) inclut des fonctionnalités de récupération de lecteur chiffrées.</span><span class="sxs-lookup"><span data-stu-id="8b237-104">Microsoft BitLocker Administration and Monitoring (MBAM) includes Encrypted Drive Recovery features.</span></span> <span data-ttu-id="8b237-105">Ces fonctionnalités garantissent la capture et le stockage des données et la disponibilité des outils requis pour accéder au volume protégé par BitLocker lorsque BitLocker place le volume en mode de récupération.</span><span class="sxs-lookup"><span data-stu-id="8b237-105">These features ensure the capture and storage of data and availability of tools that are required to access a BitLocker-protected volume when BitLocker puts that volume into recovery mode.</span></span> <span data-ttu-id="8b237-106">Un volume protégé par BitLocker est intégré au mode de récupération lors de la perte ou de l’oubli d’un code confidentiel ou d’un mot de passe, ou lorsque le processeur de plateforme sécurisée (TPM) détecte une modification apportée au BIOS ou aux fichiers de démarrage de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="8b237-106">A BitLocker-protected volume goes into recovery mode when a PIN or password is lost or forgotten, or when the Trusted Module Platform (TPM) chip detects a change to the computer's BIOS or startup files.</span></span>

<span data-ttu-id="8b237-107">Utilisez cette procédure pour accéder au système de données de récupération de clés centralisées qui peut fournir un mot de passe de récupération lorsque l’ID du mot de passe de récupération et l’identificateur d’utilisateur associé sont fournis.</span><span class="sxs-lookup"><span data-stu-id="8b237-107">Use this procedure to access the centralized Key Recovery data system that can provide a recovery password when a recovery password ID and associated user identifier are supplied.</span></span>

<span data-ttu-id="8b237-108">**Important**  MBAM génère des clés de récupération à utilisation unique.</span><span class="sxs-lookup"><span data-stu-id="8b237-108">**Important** MBAM generates single-use recovery keys.</span></span> <span data-ttu-id="8b237-109">Dans le cadre de cette limitation, une clé de récupération ne peut être utilisée qu’une seule fois et n’est plus valide.</span><span class="sxs-lookup"><span data-stu-id="8b237-109">Under this limitation, a recovery key can be used only once and then it is no longer valid.</span></span> <span data-ttu-id="8b237-110">L’utilisation unique d’un mot de passe de récupération est appliquée automatiquement aux lecteurs du système d’exploitation et aux disques durs fixes.</span><span class="sxs-lookup"><span data-stu-id="8b237-110">The single use of a recovery password is automatically applied to operating system drives and fixed drives.</span></span> <span data-ttu-id="8b237-111">Sur les lecteurs amovibles, la seule utilisation est appliquée lors de la suppression du lecteur, puis de l’insertion et de la désactivation sur un ordinateur qui a activé les paramètres de stratégie de groupe pour gérer les lecteurs amovibles.</span><span class="sxs-lookup"><span data-stu-id="8b237-111">On removable drives, the single use is applied when the drive is removed and then re-inserted and unlocked on a computer that has the group policy settings activated to manage removable drives.</span></span>

 

**<span data-ttu-id="8b237-112">Pour récupérer un lecteur en mode de récupération</span><span class="sxs-lookup"><span data-stu-id="8b237-112">To recover a drive in Recovery Mode</span></span>**

1.  <span data-ttu-id="8b237-113">Ouvrez le site Web MBAM.</span><span class="sxs-lookup"><span data-stu-id="8b237-113">Open the MBAM website.</span></span>

2.  <span data-ttu-id="8b237-114">Dans le volet de navigation, cliquez sur **récupération de lecteur**.</span><span class="sxs-lookup"><span data-stu-id="8b237-114">In the navigation pane, click **Drive Recovery**.</span></span> <span data-ttu-id="8b237-115">Le bouton **récupérer l’accès à une page Web de lecteur chiffrée** s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="8b237-115">The **Recover access to an encrypted drive** webpage opens.</span></span>

3.  <span data-ttu-id="8b237-116">Entrez le domaine d’ouverture de session Windows et le nom d’utilisateur de l’utilisateur, ainsi que les huit premiers chiffres de l’ID de clé de récupération, pour recevoir la liste des clés de récupération correspondantes possibles.</span><span class="sxs-lookup"><span data-stu-id="8b237-116">Enter the user's Windows Logon domain and user name and the first eight digits of the recovery key ID, to receive a list of possible matching recovery keys.</span></span> <span data-ttu-id="8b237-117">Vous pouvez également entrer l’ID de clé de récupération complet pour recevoir la clé de récupération exacte.</span><span class="sxs-lookup"><span data-stu-id="8b237-117">Alternatively, enter the entire recovery key ID to receive the exact recovery key.</span></span> <span data-ttu-id="8b237-118">Sélectionnez l’une des options prédéfinies dans la liste déroulante **raison du verrouillage du lecteur** , puis cliquez sur **valider**.</span><span class="sxs-lookup"><span data-stu-id="8b237-118">Select one of the predefined options in the **Reason for Drive Unlock** drop-down list, and then click **Submit**.</span></span>

    <span data-ttu-id="8b237-119">**Remarques**  Si vous êtes un utilisateur d’assistance technique avancée MBAM, les entrées de domaine et d’ID d’utilisateur ne sont pas obligatoires.</span><span class="sxs-lookup"><span data-stu-id="8b237-119">**Note** If you are an MBAM Advanced Helpdesk User, the user domain and user ID entries are not required.</span></span>

     

4.  <span data-ttu-id="8b237-120">MBAM renvoie la valeur suivante:</span><span class="sxs-lookup"><span data-stu-id="8b237-120">MBAM returns the following:</span></span>

    1.  <span data-ttu-id="8b237-121">Message d’erreur s’il n’existe aucun mot de passe de récupération correspondant</span><span class="sxs-lookup"><span data-stu-id="8b237-121">An error message if no matching recovery password is found</span></span>

    2.  <span data-ttu-id="8b237-122">Plusieurs correspondances possibles si l’utilisateur possède plusieurs mots de passe de récupération correspondants</span><span class="sxs-lookup"><span data-stu-id="8b237-122">Multiple possible matches if the user has multiple matching recovery passwords</span></span>

    3.  <span data-ttu-id="8b237-123">Le mot de passe de récupération et le package de récupération pour l’utilisateur soumis</span><span class="sxs-lookup"><span data-stu-id="8b237-123">The recovery password and recovery package for the submitted user</span></span>

        <span data-ttu-id="8b237-124">**Remarques**  Si vous récupérez un lecteur endommagé, l’option de package de récupération fournit BitLocker avec les informations critiques nécessaires à la récupération.</span><span class="sxs-lookup"><span data-stu-id="8b237-124">**Note** If you are recovering a damaged drive, the recovery package option provides BitLocker with the critical information necessary to attempt the recovery.</span></span>

         

5.  <span data-ttu-id="8b237-125">Après l’extraction du mot de passe de récupération et du package de récupération, le mot de passe de récupération s’affiche.</span><span class="sxs-lookup"><span data-stu-id="8b237-125">After the recovery password and recovery package are retrieved, the recovery password is displayed.</span></span> <span data-ttu-id="8b237-126">Pour copier le mot de passe, cliquez sur **copier la clé**, puis collez le mot de passe de récupération dans un message électronique ou dans un autre fichier texte pour le stockage temporaire.</span><span class="sxs-lookup"><span data-stu-id="8b237-126">To copy the password, click **Copy Key**, and then paste the recovery password into an email or other text file for temporary storage.</span></span> <span data-ttu-id="8b237-127">Pour enregistrer le mot de passe de récupération dans un fichier, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="8b237-127">Or, to save the recovery password to a file, click **Save**.</span></span>

6.  <span data-ttu-id="8b237-128">Lorsque l’utilisateur tape le mot de passe de récupération dans le système ou utilise le package de récupération, le lecteur est déverrouillé.</span><span class="sxs-lookup"><span data-stu-id="8b237-128">When the user types the recovery password into the system or uses the recovery package, the drive is unlocked.</span></span>

## <span data-ttu-id="8b237-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8b237-129">Related topics</span></span>


[<span data-ttu-id="8b237-130">Gestion de BitLocker avec MBAM</span><span class="sxs-lookup"><span data-stu-id="8b237-130">Performing BitLocker Management with MBAM</span></span>](performing-bitlocker-management-with-mbam.md)

 

 





