---
title: Gestion des options de chiffrement BitLocker du client MBAM à l'aide du Panneau de configuration
description: Gestion des options de chiffrement BitLocker du client MBAM à l'aide du Panneau de configuration
author: dansimp
ms.assetid: e2ff153e-5770-4a12-b79d-cda998b8a8ab
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a42901ac9d8a1a3527712f4cf342b5c0ca9ffdfd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810956"
---
# <span data-ttu-id="43cb0-103">Gestion des options de chiffrement BitLocker du client MBAM à l'aide du Panneau de configuration</span><span class="sxs-lookup"><span data-stu-id="43cb0-103">How to Manage MBAM Client BitLocker Encryption Options by Using the Control Panel</span></span>


<span data-ttu-id="43cb0-104">Une application du panneau de configuration Microsoft BitLocker d’administration et de surveillance (MBAM) Microsoft, appelée options de chiffrement BitLocker, sera disponible sous **système et sécurité** lorsque le client d’administration et de surveillance Microsoft BitLocker sera installé.</span><span class="sxs-lookup"><span data-stu-id="43cb0-104">A Microsoft BitLocker Administration and Monitoring (MBAM) control panel application, called BitLocker Encryption Options, will be available under **System and Security** when the Microsoft BitLocker Administration and Monitoring Client is installed.</span></span> <span data-ttu-id="43cb0-105">Ce panneau de configuration MBAM personnalisé est un panneau de configuration supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="43cb0-105">This custom MBAM control panel is an additional control panel.</span></span> <span data-ttu-id="43cb0-106">Cela ne remplace pas le panneau de configuration Windows BitLocker par défaut.</span><span class="sxs-lookup"><span data-stu-id="43cb0-106">It does not replace the default Windows BitLocker control panel.</span></span> <span data-ttu-id="43cb0-107">Le panneau de configuration MBAM peut être utilisé pour déverrouiller les disques durs fixes et amovibles chiffrés et gérer également votre code confidentiel ou votre mot de passe.</span><span class="sxs-lookup"><span data-stu-id="43cb0-107">The MBAM control panel can be used to unlock encrypted fixed and removable drives, and also manage your PIN or password.</span></span> <span data-ttu-id="43cb0-108">Pour plus d’informations sur l’activation du panneau de configuration MBAM, voir [comment masquer le chiffrement BitLocker par défaut dans le panneau de configuration Windows](how-to-hide-default-bitlocker-encryption-in-the-windows-control-panel-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="43cb0-108">For more information about enabling the MBAM control panel, see [How to Hide Default BitLocker Encryption in the Windows Control Panel](how-to-hide-default-bitlocker-encryption-in-the-windows-control-panel-mbam-2.md).</span></span>

**<span data-ttu-id="43cb0-109">Pour utiliser le panneau de configuration du client MBAM</span><span class="sxs-lookup"><span data-stu-id="43cb0-109">To use the MBAM Client Control Panel</span></span>**

1.  <span data-ttu-id="43cb0-110">Pour ouvrir les options de chiffrement BitLocker, cliquez sur **Démarrer** , puis sélectionnez **panneau de configuration**.</span><span class="sxs-lookup"><span data-stu-id="43cb0-110">To open BitLocker Encryption Options, click **Start** and then select **Control Panel**.</span></span> <span data-ttu-id="43cb0-111">Lorsque **le panneau de configuration** s’ouvre, sélectionnez **système et sécurité**.</span><span class="sxs-lookup"><span data-stu-id="43cb0-111">When **Control Panel** opens, select **System and Security**.</span></span>

2.  <span data-ttu-id="43cb0-112">Double-cliquez sur **options de chiffrement BitLocker** pour ouvrir le panneau de configuration MBAM personnalisé.</span><span class="sxs-lookup"><span data-stu-id="43cb0-112">Double-click **BitLocker Encryption Options** to open the customized MBAM control panel.</span></span> <span data-ttu-id="43cb0-113">Vous verrez la liste de tous les disques durs de votre ordinateur et leur état de chiffrement, en plus d’une option de gestion de votre code confidentiel ou de votre mot de passe.</span><span class="sxs-lookup"><span data-stu-id="43cb0-113">You will see a list of all the hard disk drives on the computer and their encryption status, in addition to an option to manage your PIN or passwords.</span></span>

    <span data-ttu-id="43cb0-114">La liste des disques durs de l’ordinateur peut être utilisée pour vérifier le statut de chiffrement, déverrouiller un lecteur ou demander une exemption de protection de BitLocker si les stratégies d’exemption des utilisateurs et des ordinateurs ont été déployées.</span><span class="sxs-lookup"><span data-stu-id="43cb0-114">The list of hard disk drives on the computer can be used to verify encryption status, unlock a drive, or request an exemption for BitLocker protection if the User and Computer Exemption policies have been deployed.</span></span>

    <span data-ttu-id="43cb0-115">Le panneau de configuration options de chiffrement BitLocker autorise également les utilisateurs non administrateurs à gérer leur code confidentiel ou leur mot de passe.</span><span class="sxs-lookup"><span data-stu-id="43cb0-115">The BitLocker Encryption Options control panel also allows for non-administrator users to manage their PIN or passwords.</span></span> <span data-ttu-id="43cb0-116">En sélectionnant **gérer le code confidentiel**, les utilisateurs sont invités à entrer un code confidentiel actuel et un nouveau code confidentiel (en plus de confirmer le nouveau code confidentiel).</span><span class="sxs-lookup"><span data-stu-id="43cb0-116">By selecting **Manage PIN**, users are prompted to enter both a current PIN and a new PIN (in addition to confirming the new PIN).</span></span> <span data-ttu-id="43cb0-117">Le choix de **mettre à jour le code confidentiel** entraîne la réinitialisation du code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="43cb0-117">Selecting **Update PIN** will reset the PIN to the new one that the users selected.</span></span>

    <span data-ttu-id="43cb0-118">Pour gérer votre mot de passe, sélectionnez **verrouiller le lecteur** et entrez votre mot de passe actuel.</span><span class="sxs-lookup"><span data-stu-id="43cb0-118">To manage your password, select **Unlock drive** and enter your current password.</span></span> <span data-ttu-id="43cb0-119">Dès que le lecteur est déverrouillé, sélectionnez **Réinitialiser le mot de passe** pour modifier votre mot de passe actuel.</span><span class="sxs-lookup"><span data-stu-id="43cb0-119">As soon as the drive is unlocked, select **Reset Password** to change your current password.</span></span>

## <span data-ttu-id="43cb0-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="43cb0-120">Related topics</span></span>


[<span data-ttu-id="43cb0-121">Administration des composants de MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="43cb0-121">Administering MBAM 2.0 Features</span></span>](administering-mbam-20-features-mbam-2.md)

 

 





