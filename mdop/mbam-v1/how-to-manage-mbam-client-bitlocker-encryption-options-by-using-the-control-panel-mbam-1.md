---
title: Gestion des options de chiffrement BitLocker du client MBAM à l'aide du Panneau de configuration
description: Gestion des options de chiffrement BitLocker du client MBAM à l'aide du Panneau de configuration
author: dansimp
ms.assetid: c08077e1-5529-468f-9370-c3b33fc258f3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 271147d0e5581f6ce49fe0b46aa83dae6ae4556b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804615"
---
# <span data-ttu-id="6b667-103">Gestion des options de chiffrement BitLocker du client MBAM à l'aide du Panneau de configuration</span><span class="sxs-lookup"><span data-stu-id="6b667-103">How to Manage MBAM Client BitLocker Encryption Options by Using the Control Panel</span></span>


<span data-ttu-id="6b667-104">Une application du panneau de configuration Microsoft BitLocker administration et surveillance (MBAM), appelée options de chiffrement BitLocker, sera disponible sous **système et sécurité** lorsque le client MBAM est installé.</span><span class="sxs-lookup"><span data-stu-id="6b667-104">A Microsoft BitLocker Administration and Monitoring (MBAM) control panel application, called BitLocker Encryption Options, will be available under **System and Security** when the MBAM Client is installed.</span></span> <span data-ttu-id="6b667-105">Ce panneau de configuration MBAM personnalisé remplace le panneau de configuration Windows BitLocker par défaut.</span><span class="sxs-lookup"><span data-stu-id="6b667-105">This customized MBAM control panel replaces the default Windows BitLocker control panel.</span></span> <span data-ttu-id="6b667-106">Le panneau de configuration MBAM vous permet de déverrouiller des lecteurs chiffrés (résolus et amovibles) et de gérer également votre code confidentiel ou votre mot de passe.</span><span class="sxs-lookup"><span data-stu-id="6b667-106">The MBAM control panel enables you to unlock encrypted drives (fixed and removable), and also helps you manage your PIN or password.</span></span> <span data-ttu-id="6b667-107">Pour plus d’informations sur l’activation du panneau de configuration MBAM, voir [comment masquer le chiffrement BitLocker par défaut dans le panneau de configuration Windows](how-to-hide-default-bitlocker-encryption-in-the-windows-control-panel.md).</span><span class="sxs-lookup"><span data-stu-id="6b667-107">For more information about enabling the MBAM control panel, see [How to Hide Default BitLocker Encryption in The Windows Control Panel](how-to-hide-default-bitlocker-encryption-in-the-windows-control-panel.md).</span></span>

<span data-ttu-id="6b667-108">**Remarques**  Pour le client BitLocker, les fichiers du journal d’administration et du journal opérationnel sont situés dans l’observateur d’événements, sous **applications et services consignent**  /  **Microsoft**  /  **Windows**  /  **BitLockerManagement**.</span><span class="sxs-lookup"><span data-stu-id="6b667-108">**Note** For the BitLocker client, the Admin and Operational log files are located in Event Viewer, under **Application and Services Logs** / **Microsoft** / **Windows** / **BitLockerManagement**.</span></span>

 

**<span data-ttu-id="6b667-109">Pour utiliser le panneau de configuration du client MBAM</span><span class="sxs-lookup"><span data-stu-id="6b667-109">To use the MBAM Client Control Panel</span></span>**

1.  <span data-ttu-id="6b667-110">Pour ouvrir les options de chiffrement BitLocker, cliquez sur **Démarrer**, puis sélectionnez **panneau de configuration**.</span><span class="sxs-lookup"><span data-stu-id="6b667-110">To open BitLocker Encryption Options, click **Start**, and then select **Control Panel**.</span></span> <span data-ttu-id="6b667-111">Lorsque **le panneau de configuration** s’ouvre, sélectionnez **système et sécurité**.</span><span class="sxs-lookup"><span data-stu-id="6b667-111">When **Control Panel** opens, select **System and Security**.</span></span>

2.  <span data-ttu-id="6b667-112">Double-cliquez sur **options de chiffrement BitLocker** pour ouvrir le panneau de configuration MBAM personnalisé.</span><span class="sxs-lookup"><span data-stu-id="6b667-112">Double-click **BitLocker Encryption Options** to open the customized MBAM control panel.</span></span> <span data-ttu-id="6b667-113">La liste de tous les disques durs de l’ordinateur s’affiche, ainsi que leur état de cryptage.</span><span class="sxs-lookup"><span data-stu-id="6b667-113">You will see a list of all the hard disk drives on the computer and their encryption status.</span></span> <span data-ttu-id="6b667-114">Vous verrez également une option permettant de gérer votre code confidentiel ou vos mots de passe.</span><span class="sxs-lookup"><span data-stu-id="6b667-114">You will also see an option to manage your PIN or passwords.</span></span>

3.  <span data-ttu-id="6b667-115">Utilisez la liste des disques durs de l’ordinateur pour vérifier le statut de chiffrement, déverrouiller un lecteur ou demander une exemption pour la protection de BitLocker si les stratégies d’exemption des utilisateurs et des ordinateurs ont été déployées.</span><span class="sxs-lookup"><span data-stu-id="6b667-115">Use the list of hard disk drives on the computer to verify the encryption status, unlock a drive, or request an exemption for BitLocker protection if the User and Computer Exemption policies have been deployed.</span></span>

4.  <span data-ttu-id="6b667-116">Les non-administrateurs peuvent utiliser le panneau de configuration options de chiffrement de BitLocker pour gérer les codes confidentiels ou mots de passe.</span><span class="sxs-lookup"><span data-stu-id="6b667-116">Non-administrators can use the BitLocker Encryption Options control panel to manage PINs or passwords.</span></span> <span data-ttu-id="6b667-117">Un utilisateur peut sélectionner **gérer le code confidentiel,** puis entrer un code confidentiel actuel et un nouveau code secret.</span><span class="sxs-lookup"><span data-stu-id="6b667-117">A user can select **Manage PIN,** and then enter both a current PIN and a new PIN.</span></span> <span data-ttu-id="6b667-118">Les utilisateurs peuvent également confirmer leur nouveau code secret.</span><span class="sxs-lookup"><span data-stu-id="6b667-118">Users can also confirm their new PIN.</span></span> <span data-ttu-id="6b667-119">La fonction de **mise à jour de l’épingle** rétablit le code confidentiel en nouveau que l’utilisateur sélectionne.</span><span class="sxs-lookup"><span data-stu-id="6b667-119">The **Update PIN** function will reset the PIN to the new one that the user selects.</span></span>

5.  <span data-ttu-id="6b667-120">Pour gérer votre mot de passe, sélectionnez **verrouiller le lecteur** et entrez votre mot de passe actuel.</span><span class="sxs-lookup"><span data-stu-id="6b667-120">To manage your password, select **Unlock drive** and enter your current password.</span></span> <span data-ttu-id="6b667-121">Dès que le lecteur est déverrouillé, sélectionnez **Réinitialiser le mot de passe** pour modifier votre mot de passe actuel.</span><span class="sxs-lookup"><span data-stu-id="6b667-121">As soon as the drive is unlocked, select **Reset Password** to change your current password.</span></span>

## <span data-ttu-id="6b667-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6b667-122">Related topics</span></span>


[<span data-ttu-id="6b667-123">Administration des composants de MBAM1.0</span><span class="sxs-lookup"><span data-stu-id="6b667-123">Administering MBAM 1.0 Features</span></span>](administering-mbam-10-features.md)

 

 





