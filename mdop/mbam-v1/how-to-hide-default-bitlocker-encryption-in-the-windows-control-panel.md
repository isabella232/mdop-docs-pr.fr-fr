---
title: Masquer le chiffrement BitLocker par défaut dans le Panneau de configuration Windows
description: Masquer le chiffrement BitLocker par défaut dans le Panneau de configuration Windows
author: dansimp
ms.assetid: c8503743-220c-497c-9785-e2feeca484d6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 67a61763e556f8c3b93825220dbbd61a14b7d6f4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810596"
---
# <span data-ttu-id="8d686-103">Masquer le chiffrement BitLocker par défaut dans le Panneau de configuration Windows</span><span class="sxs-lookup"><span data-stu-id="8d686-103">How to Hide Default BitLocker Encryption in The Windows Control Panel</span></span>


<span data-ttu-id="8d686-104">Le système d’administration et de surveillance de BitLocker Microsoft (MBAM) propose un panneau de configuration personnalisé pour les ordinateurs clients MBAM appelé options de chiffrement BitLocker.</span><span class="sxs-lookup"><span data-stu-id="8d686-104">Microsoft BitLocker Administration and Monitoring (MBAM) offers a customized control panel for MBAM client computers that is named called BitLocker Encryption Options.</span></span> <span data-ttu-id="8d686-105">Ce panneau de configuration personnalisé peut remplacer le panneau de configuration Windows BitLocker par défaut qui est appelé chiffrement de lecteur BitLocker.</span><span class="sxs-lookup"><span data-stu-id="8d686-105">This customized control panel can replace the default Windows BitLocker control panel that is named BitLocker Drive Encryption.</span></span> <span data-ttu-id="8d686-106">Le panneau de configuration options de chiffrement BitLocker, situé sous système et sécurité dans le panneau de configuration Windows, permet aux utilisateurs de gérer leur code confidentiel et leurs mots de passe, de déverrouiller des lecteurs et de masquer l’interface permettant aux administrateurs de déchiffrer un lecteur ou de suspendre ou de reprendre le chiffrement BitLocker.</span><span class="sxs-lookup"><span data-stu-id="8d686-106">The BitLocker Encryption Options control panel, located under System and Security in the Windows control panel, enables users to manage their PIN and passwords, unlock drives, and hides the interface that allows administrators to decrypt a drive or to suspend or resume BitLocker encryption.</span></span>

**<span data-ttu-id="8d686-107">Pour masquer le chiffrement BitLocker par défaut dans le panneau de configuration Windows</span><span class="sxs-lookup"><span data-stu-id="8d686-107">To hide default BitLocker Encryption in the Windows Control Panel</span></span>**

1.  <span data-ttu-id="8d686-108">Naviguez jusqu’à la **Configuration utilisateur** à l’aide de la console de gestion des stratégies de groupe (GPMC), de la gestion de la stratégie de groupe avancée (AGPM) ou de l’éditeur de stratégie de groupe locale sur l’ordinateur de stratégies de groupe BitLocker.</span><span class="sxs-lookup"><span data-stu-id="8d686-108">Browse to **User configuration** by using the Group Policy Management Console (GPMC), the Advanced Group Policy Management (AGPM), or the Local Group Policy Editor on the BitLocker Group Policies computer.</span></span>

2.  <span data-ttu-id="8d686-109">Cliquez sur **stratégies**, sélectionnez **modèles d’administration**, puis cliquez sur **panneau de configuration**.</span><span class="sxs-lookup"><span data-stu-id="8d686-109">Click **Policies**, select **Administrative Templates**, and then click **Control Panel**.</span></span>

3.  <span data-ttu-id="8d686-110">Dans le volet **Détails** , double-cliquez sur **Masquer les éléments du panneau de configuration spécifiés**, puis sélectionnez **activé**.</span><span class="sxs-lookup"><span data-stu-id="8d686-110">In the **Details** pane, double-click **Hide specified Control Panel items**, and then select **Enabled**.</span></span>

4.  <span data-ttu-id="8d686-111">Cliquez sur **Afficher**, **sur Ajouter...**, puis tapez Microsoft. BitLockerDriveEncryption.</span><span class="sxs-lookup"><span data-stu-id="8d686-111">Click **Show**, **click Add…**, and then type Microsoft.BitLockerDriveEncryption.</span></span> <span data-ttu-id="8d686-112">Ce paramètre de stratégie masque l’outil de gestion de BitLocker Windows par défaut dans le panneau de configuration Windows, et permet à l’utilisateur d’ouvrir l’outil mise à jour MBAM BitLocker options du panneau de configuration Windows.</span><span class="sxs-lookup"><span data-stu-id="8d686-112">This policy hides the default Windows BitLocker Management tool from the Windows Control Panel and allows the user to open the updated MBAM BitLocker Encryption Options tool from the Windows Control Panel.</span></span>

## <span data-ttu-id="8d686-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8d686-113">Related topics</span></span>


[<span data-ttu-id="8d686-114">Déploiement d'objets de stratégie de groupe MBAM1.0</span><span class="sxs-lookup"><span data-stu-id="8d686-114">Deploying MBAM 1.0 Group Policy Objects</span></span>](deploying-mbam-10-group-policy-objects.md)

 

 





