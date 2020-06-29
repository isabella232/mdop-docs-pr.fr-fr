---
title: Comment masquer le chiffrement BitLocker par défaut dans le Panneau de configuration Windows
description: Comment masquer le chiffrement BitLocker par défaut dans le Panneau de configuration Windows
author: dansimp
ms.assetid: 6674aa51-2b5d-4e4a-8b43-2cc18d008285
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: eda8fafbd7b3ebf414520354eba6def2e97f6237
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810343"
---
# <span data-ttu-id="3a0ad-103">Comment masquer le chiffrement BitLocker par défaut dans le Panneau de configuration Windows</span><span class="sxs-lookup"><span data-stu-id="3a0ad-103">How to Hide Default BitLocker Encryption in the Windows Control Panel</span></span>


<span data-ttu-id="3a0ad-104">Le système d’administration et de surveillance de BitLocker Microsoft (MBAM) propose un panneau de configuration personnalisé pour l’administration et la surveillance de l’ordinateur client par Microsoft BitLocker, appelés options de chiffrement de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="3a0ad-104">Microsoft BitLocker Administration and Monitoring (MBAM) offers a customized control panel for Microsoft BitLocker Administration and Monitoring client computers, called BitLocker Encryption Options.</span></span> <span data-ttu-id="3a0ad-105">Ce panneau de configuration personnalisé peut remplacer le panneau de configuration Windows BitLocker par défaut, qui est appelé chiffrement de lecteur BitLocker.</span><span class="sxs-lookup"><span data-stu-id="3a0ad-105">This customized control panel can replace the default Windows BitLocker control panel, which is called BitLocker Drive Encryption.</span></span> <span data-ttu-id="3a0ad-106">Le panneau de configuration personnalisé, qui se trouve dans le panneau de configuration, sous système et sécurité, permet aux utilisateurs de gérer leur code confidentiel et leur mot de passe, de déverrouiller les lecteurs et de masquer l’interface permettant aux administrateurs de déchiffrer un lecteur ou de suspendre ou de reprendre le chiffrement de lecteur BitLocker.</span><span class="sxs-lookup"><span data-stu-id="3a0ad-106">The customized control panel, which is in Control Panel under System and Security, enables users to manage their PIN and passwords and to unlock drives, and hides the interface that enables administrators to decrypt a drive or to suspend or resume BitLocker drive encryption.</span></span>

**<span data-ttu-id="3a0ad-107">Pour masquer le chiffrement de lecteur BitLocker par défaut dans le panneau de configuration Windows</span><span class="sxs-lookup"><span data-stu-id="3a0ad-107">To hide default BitLocker drive encryption in Windows Control Panel</span></span>**

1.  <span data-ttu-id="3a0ad-108">Dans la console de gestion des stratégies de groupe (GPMC), la gestion avancée de la stratégie de groupe (AGPM) ou l’éditeur de stratégie de groupe locale sur l’ordinateur stratégies de groupe BitLocker, accédez à **Configuration utilisateur**.</span><span class="sxs-lookup"><span data-stu-id="3a0ad-108">In the Group Policy Management Console (GPMC), the Advanced Group Policy Management (AGPM), or the Local Group Policy Editor on the BitLocker Group Policies computer, browse to **User configuration**.</span></span>

2.  <span data-ttu-id="3a0ad-109">Cliquez ensuite sur **stratégies**, sélectionnez **modèles d’administration**, puis cliquez sur **panneau de configuration**.</span><span class="sxs-lookup"><span data-stu-id="3a0ad-109">Next, click **Policies**, select **Administrative Templates**, and then click **Control Panel**.</span></span>

3.  <span data-ttu-id="3a0ad-110">Double-cliquez sur **Masquer les éléments du panneau de configuration spécifiés** dans le volet **Détails** , puis sélectionnez **activé**.</span><span class="sxs-lookup"><span data-stu-id="3a0ad-110">Double-click **Hide specified Control Panel items** in the **Details** pane, and then select **Enabled**.</span></span>

4.  <span data-ttu-id="3a0ad-111">Cliquez sur **Afficher**, puis sur **Ajouter**et tapez **Microsoft. BitLockerDriveEncryption**.</span><span class="sxs-lookup"><span data-stu-id="3a0ad-111">Click **Show**, click **Add**, and then type **Microsoft.BitLockerDriveEncryption**.</span></span> <span data-ttu-id="3a0ad-112">Cette stratégie masque l’outil de gestion de BitLocker Windows par défaut dans le panneau de configuration Windows, puis, dans le panneau de configuration, il permet à l’utilisateur d’ouvrir l’outil mise à jour MBAM BitLocker options dans système et sécurité.</span><span class="sxs-lookup"><span data-stu-id="3a0ad-112">This policy hides the default Windows BitLocker Management tool from the Windows Control Panel and, in Control Panel, lets the user open the updated MBAM BitLocker Encryption Options tool under System and Security.</span></span>

## <span data-ttu-id="3a0ad-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3a0ad-113">Related topics</span></span>


[<span data-ttu-id="3a0ad-114">Déploiement d'objets de stratégie de groupe MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="3a0ad-114">Deploying MBAM 2.0 Group Policy Objects</span></span>](deploying-mbam-20-group-policy-objects-mbam-2.md)

 

 





