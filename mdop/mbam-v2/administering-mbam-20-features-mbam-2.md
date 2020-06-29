---
title: Administration des composants de MBAM2.0
description: Administration des composants de MBAM2.0
author: dansimp
ms.assetid: 065e0704-069e-4372-9b86-0b57dd7638dd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 35bb855e185ad8e3fa6880853938074cf6185a0d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809996"
---
# <span data-ttu-id="9ec6b-103">Administration des composants de MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="9ec6b-103">Administering MBAM 2.0 Features</span></span>


<span data-ttu-id="9ec6b-104">Après avoir effectué toutes les étapes de planification, puis de déploiement de Microsoft BitLocker administration et surveillance (MBAM), vous pouvez la configurer et l’utiliser pour gérer le chiffrement BitLocker au sein de l’entreprise. les informations dans cette section décrivent les tâches d’administration et de fonctionnalité de surveillance de l’installation de Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="9ec6b-104">After completing all necessary planning and then deploying Microsoft BitLocker Administration and Monitoring (MBAM), you can configure and use it to manage BitLocker encryption across the enterprise The information in this section describes post-installation day-to-day Microsoft BitLocker Administration and Monitoring feature operations tasks.</span></span>

## <span data-ttu-id="9ec6b-105">Gérer les rôles d’administrateur MBAM</span><span class="sxs-lookup"><span data-stu-id="9ec6b-105">Manage MBAM Administrator Roles</span></span>


<span data-ttu-id="9ec6b-106">Une fois l’installation d’MBAM terminée pour toutes les fonctionnalités du serveur, les utilisateurs administratifs doivent y avoir accès.</span><span class="sxs-lookup"><span data-stu-id="9ec6b-106">After MBAM Setup is complete for all server features, administrative users have to be granted access to them.</span></span> <span data-ttu-id="9ec6b-107">Il est recommandé que les administrateurs qui gèrent ou utilisent les fonctionnalités du serveur MBAM puissent être assignés aux groupes de sécurité des services de domaine Active Directory (AD FS), et ces groupes doivent être ajoutés au groupe local d’administration MBAM approprié.</span><span class="sxs-lookup"><span data-stu-id="9ec6b-107">As a best practice, administrators who will manage or use MBAM server features should be assigned to Active Directory Domain Services security groups, and then those groups should be added to the appropriate MBAM administrative local group.</span></span>

[<span data-ttu-id="9ec6b-108">Gérer des rôles d'administrateur MBAM</span><span class="sxs-lookup"><span data-stu-id="9ec6b-108">How to Manage MBAM Administrator Roles</span></span>](how-to-manage-mbam-administrator-roles-mbam-2.md)

## <span data-ttu-id="9ec6b-109">Gérer les exemptions de chiffrement BitLocker</span><span class="sxs-lookup"><span data-stu-id="9ec6b-109">Manage BitLocker Encryption Exemptions</span></span>


<span data-ttu-id="9ec6b-110">MBAM vous permet d’accorder des exemptions de chiffrement à des utilisateurs spécifiques qui n’ont pas besoin ou veulent que leurs lecteurs soient chiffrés.</span><span class="sxs-lookup"><span data-stu-id="9ec6b-110">MBAM lets you grant encryption exemptions to specific users who do not need or want their drives encrypted.</span></span> <span data-ttu-id="9ec6b-111">L’exemption d’ordinateur est généralement utilisée lorsqu’une société dispose d’ordinateurs qui n’ont pas besoin d’être chiffrés, tels que des ordinateurs utilisés pour le développement ou les tests, ou des ordinateurs plus anciens qui ne prennent pas en charge BitLocker.</span><span class="sxs-lookup"><span data-stu-id="9ec6b-111">Computer exemption is typically used when a company has computers that do not have to be encrypted, such as computers that are used in development or testing, or older computers that do not support BitLocker.</span></span> <span data-ttu-id="9ec6b-112">Dans certains cas, la législation locale peuvent également exiger que certains ordinateurs ne soient pas chiffrés.</span><span class="sxs-lookup"><span data-stu-id="9ec6b-112">In some cases, local law may also require that certain computers are not encrypted.</span></span>

[<span data-ttu-id="9ec6b-113">Gestion des exemptions de chiffrement BitLocker d'utilisateur</span><span class="sxs-lookup"><span data-stu-id="9ec6b-113">How to Manage User BitLocker Encryption Exemptions</span></span>](how-to-manage-user-bitlocker-encryption-exemptions-mbam-2.md)

## <span data-ttu-id="9ec6b-114">Gérer les options de chiffrement BitLocker du client MBAM à l’aide du panneau de configuration</span><span class="sxs-lookup"><span data-stu-id="9ec6b-114">Manage MBAM Client BitLocker Encryption Options by Using the Control Panel</span></span>


<span data-ttu-id="9ec6b-115">MBAM fournit un panneau de configuration personnalisé, intitulé options de chiffrement de BitLocker, qui s’affiche sous **système et sécurité**.</span><span class="sxs-lookup"><span data-stu-id="9ec6b-115">MBAM provides a custom control panel, called BitLocker Encryption Options, that will appear under **System and Security**.</span></span> <span data-ttu-id="9ec6b-116">Le panneau de configuration MBAM peut être utilisé pour déverrouiller les disques durs fixes et amovibles chiffrés et gérer également votre code confidentiel ou votre mot de passe.</span><span class="sxs-lookup"><span data-stu-id="9ec6b-116">The MBAM control panel can be used to unlock encrypted fixed and removable drives, and also manage your PIN or password.</span></span>

<span data-ttu-id="9ec6b-117">**Remarques**  Ce panneau de configuration personnalisé ne remplace pas le panneau de configuration Windows BitLocker par défaut.</span><span class="sxs-lookup"><span data-stu-id="9ec6b-117">**Note** This customized control panel does not replace the default Windows BitLocker control panel.</span></span>

 

[<span data-ttu-id="9ec6b-118">Gestion des options de chiffrement BitLocker du client MBAM à l'aide du Panneau de configuration</span><span class="sxs-lookup"><span data-stu-id="9ec6b-118">How to Manage MBAM Client BitLocker Encryption Options by Using the Control Panel</span></span>](how-to-manage-mbam-client-bitlocker-encryption-options-by-using-the-control-panel-mbam-2.md)

## <span data-ttu-id="9ec6b-119">Autres ressources pour administrer les fonctionnalités de MBAM</span><span class="sxs-lookup"><span data-stu-id="9ec6b-119">Other Resources for Administering MBAM Features</span></span>


[<span data-ttu-id="9ec6b-120">Opérations de MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="9ec6b-120">Operations for MBAM 2.0</span></span>](operations-for-mbam-20-mbam-2.md)

 

 





