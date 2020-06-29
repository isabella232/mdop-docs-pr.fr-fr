---
title: Procédure de récupération d'un lecteur en mode de récupération
description: Procédure de récupération d'un lecteur en mode de récupération
author: dansimp
ms.assetid: 8b792bc8-b671-4345-9d37-0208db3e5b03
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7d5ce509599d0eb800a71360e3be9d0fa3b33f4f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810926"
---
# <span data-ttu-id="f943d-103">Procédure de récupération d'un lecteur en mode de récupération</span><span class="sxs-lookup"><span data-stu-id="f943d-103">How to Recover a Drive in Recovery Mode</span></span>


<span data-ttu-id="f943d-104">Les fonctionnalités de récupération de lecteur chiffrées de l’administration et de la surveillance de BitLocker (MBAM) permettent de capturer et de stocker les données et la disponibilité des outils requis pour accéder au volume protégé par BitLocker lorsque BitLocker passe en mode récupération.</span><span class="sxs-lookup"><span data-stu-id="f943d-104">The encrypted drive recovery features of Microsoft BitLocker Administration and Monitoring (MBAM) ensure the capture and storage of data and availability of tools required to access a BitLocker-protected volume when BitLocker goes into recovery mode.</span></span> <span data-ttu-id="f943d-105">Un volume protégé par BitLocker est intégré au mode de récupération lors de la perte ou de l’oubli d’un code confidentiel ou d’un mot de passe, ou lorsque le processeur de plateforme sécurisée détecte des modifications apportées aux fichiers du BIOS ou de démarrage d’un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="f943d-105">A BitLocker-protected volume goes into recovery mode when a PIN or password is lost or forgotten, or when the Trusted Module Platform (TPM) chip detects changes to the BIOS or startup files of a computer.</span></span>

<span data-ttu-id="f943d-106">Utilisez cette procédure pour accéder au système de données de récupération de clés centralisées, qui peut fournir un mot de passe de récupération si un ID de mot de passe de récupération et un identificateur d’utilisateur associé sont fournis.</span><span class="sxs-lookup"><span data-stu-id="f943d-106">Use this procedure to access the centralized key recovery data system, which can provide a recovery password if a recovery password ID and associated user identifier are supplied.</span></span>

**<span data-ttu-id="f943d-107">Important</span><span class="sxs-lookup"><span data-stu-id="f943d-107">Important</span></span>**  
<span data-ttu-id="f943d-108">L’analyse et l’administration de BitLocker utilise des clés de récupération à utilisation unique qui expirent lors de l’utilisation.</span><span class="sxs-lookup"><span data-stu-id="f943d-108">Microsoft BitLocker Administration and Monitoring uses single-use recovery keys that expire upon use.</span></span> <span data-ttu-id="f943d-109">L’utilisation unique d’un mot de passe de récupération est appliquée automatiquement aux lecteurs du système d’exploitation et aux disques durs fixes.</span><span class="sxs-lookup"><span data-stu-id="f943d-109">The single use of a recovery password is automatically applied to operating system drives and fixed drives.</span></span> <span data-ttu-id="f943d-110">Sur les lecteurs amovibles, il est appliqué lors de la suppression du lecteur, puis de nouveau l’insertion et le déverrouillage sur un ordinateur qui a activé les paramètres de stratégie de groupe pour gérer les lecteurs amovibles.</span><span class="sxs-lookup"><span data-stu-id="f943d-110">On removable drives, it is applied when the drive is removed and then re-inserted and unlocked on a computer that has Group Policy settings activated to manage removable drives.</span></span>



**<span data-ttu-id="f943d-111">Pour récupérer un lecteur en mode de récupération</span><span class="sxs-lookup"><span data-stu-id="f943d-111">To recover a drive in recovery mode</span></span>**

1.  <span data-ttu-id="f943d-112">Ouvrez un navigateur Web, puis accédez au site Web d’administration et de surveillance.</span><span class="sxs-lookup"><span data-stu-id="f943d-112">Open a web browser and navigate to the Administration and Monitoring website.</span></span>

2.  <span data-ttu-id="f943d-113">Dans le volet de navigation, cliquez sur **récupération de lecteur**.</span><span class="sxs-lookup"><span data-stu-id="f943d-113">In the navigation pane, click **Drive Recovery**.</span></span> <span data-ttu-id="f943d-114">La page Web «récupérer l’accès à un lecteur chiffré» s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="f943d-114">The “Recover access to an encrypted drive” webpage opens.</span></span>

3.  <span data-ttu-id="f943d-115">Entrez le domaine d’ouverture de session Windows et le nom d’utilisateur de l’utilisateur pour afficher les informations de récupération et les huit premiers chiffres de l’ID de clé de récupération pour recevoir une liste de clés de récupération correspondantes, ou l’ID de la clé de récupération complète pour recevoir la clé de récupération exacte.</span><span class="sxs-lookup"><span data-stu-id="f943d-115">Enter the Windows Logon domain and user name of the user to view recovery information and the first eight digits of the recovery key ID to receive a list of possible matching recovery keys or the entire recovery key ID to receive the exact recovery key.</span></span>

4.  <span data-ttu-id="f943d-116">Sélectionnez l’une des options prédéfinies dans la liste **raison pour le verrouillage du lecteur** , puis cliquez sur **valider**.</span><span class="sxs-lookup"><span data-stu-id="f943d-116">Select one of the predefined options from the **Reason for Drive Unlock** list, and then click **Submit**.</span></span>

    **<span data-ttu-id="f943d-117">Remarque</span><span class="sxs-lookup"><span data-stu-id="f943d-117">Note</span></span>**  
    <span data-ttu-id="f943d-118">Si vous êtes un utilisateur d’assistance technique avancée MBAM, les entrées de domaine et d’ID d’utilisateur ne sont pas obligatoires.</span><span class="sxs-lookup"><span data-stu-id="f943d-118">If you are an MBAM Advanced Helpdesk user, the user domain and user ID entries are not required.</span></span>



~~~
MBAM returns the following:

-   An error message if no matching recovery password is found

-   Multiple possible matches if the user has multiple matching recovery passwords

-   The recovery password and recovery package for the submitted user

    **Note**  
    If you are recovering a damaged drive, the recovery package option provides BitLocker with critical information that it needs to recover the drive.



After the recovery password and recovery package are retrieved, the recovery password is displayed.
~~~

5. <span data-ttu-id="f943d-119">Pour copier le mot de passe, cliquez sur **copier la clé**, puis collez le mot de passe de récupération dans un message électronique.</span><span class="sxs-lookup"><span data-stu-id="f943d-119">To copy the password, click **Copy Key**, and then paste the recovery password into an email message.</span></span> <span data-ttu-id="f943d-120">Vous pouvez également cliquer sur **Enregistrer** pour enregistrer le mot de passe de récupération dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="f943d-120">Alternatively, click **Save** to save the recovery password to a file.</span></span>

   <span data-ttu-id="f943d-121">Lorsque l’utilisateur tape le mot de passe de récupération dans le système ou utilise le package de récupération, le lecteur est déverrouillé.</span><span class="sxs-lookup"><span data-stu-id="f943d-121">When the user types the recovery password into the system or uses the recovery package, the drive is unlocked.</span></span>

## <span data-ttu-id="f943d-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f943d-122">Related topics</span></span>


[<span data-ttu-id="f943d-123">Gestion de BitLocker avec MBAM</span><span class="sxs-lookup"><span data-stu-id="f943d-123">Performing BitLocker Management with MBAM</span></span>](performing-bitlocker-management-with-mbam-mbam-2.md)









