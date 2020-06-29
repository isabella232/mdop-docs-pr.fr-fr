---
title: Gérer des exemptions d'ordinateurs au chiffrement BitLocker
description: Gérer des exemptions d'ordinateurs au chiffrement BitLocker
author: dansimp
ms.assetid: d4400a0d-b36b-4cf5-a294-1f53ec47f9ee
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 51b93061468508900eaee7fce8a7827e2db61d19
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811298"
---
# <span data-ttu-id="56b40-103">Gérer des exemptions d'ordinateurs au chiffrement BitLocker</span><span class="sxs-lookup"><span data-stu-id="56b40-103">How to Manage Computer BitLocker Encryption Exemptions</span></span>


<span data-ttu-id="56b40-104">L’utilisation de Microsoft BitLocker administration et de la surveillance (MBAM) permet d’exempter certains ordinateurs de la protection BitLocker.</span><span class="sxs-lookup"><span data-stu-id="56b40-104">Microsoft BitLocker Administration and Monitoring (MBAM) can be used to exempt certain computers from BitLocker protection.</span></span> <span data-ttu-id="56b40-105">Par exemple, une organisation risque de contrôler l’exemption de BitLocker en fonction de votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="56b40-105">For example, an organization may decide to control BitLocker exemption on a computer-by-computer basis.</span></span>

<span data-ttu-id="56b40-106">Pour exempter un ordinateur d’un chiffrement BitLocker, vous devez ajouter l’ordinateur à un groupe de sécurité dans ActiveDirectoryDomainServices pour ignorer toutes les règles de protection BitLocker basées sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="56b40-106">To exempt a computer from BitLocker encryption, you must add the computer to a security group in ActiveDirectoryDomainServices in order to bypass any computer-based BitLocker protection rules.</span></span>

<span data-ttu-id="56b40-107">**Remarques**  Si l’ordinateur est déjà protégé par BitLocker, la stratégie d’exemption d’ordinateur n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="56b40-107">**Note** If the computer is already BitLocker-protected, the computer exemption policy has no effect.</span></span>

 

**<span data-ttu-id="56b40-108">Pour exempter un ordinateur d’un chiffrement BitLocker</span><span class="sxs-lookup"><span data-stu-id="56b40-108">To exempt a computer from BitLocker encryption</span></span>**

1.  <span data-ttu-id="56b40-109">Ajoutez le compte d’ordinateur que vous souhaitez exempter d’un groupe de sécurité dans ActiveDirectoryDomainServices.</span><span class="sxs-lookup"><span data-stu-id="56b40-109">Add the computer account that you want to be exempted to a security group in ActiveDirectoryDomainServices.</span></span> <span data-ttu-id="56b40-110">Cela vous permet d’ignorer toutes les règles de protection BitLocker basées sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="56b40-110">This allows you to bypass any computer-based BitLocker protection rules.</span></span>

2.  <span data-ttu-id="56b40-111">Créez un objet de stratégie de groupe à l’aide du modèle de stratégie de groupe MBAM, puis associez l’objet de stratégie de groupe au groupe Active Directory que vous avez créé à l’étape précédente.</span><span class="sxs-lookup"><span data-stu-id="56b40-111">Create a Group Policy Object by using the MBAM Group Policy template, then associate the Group Policy Object with the Active Directory group that you created in the previous step.</span></span> <span data-ttu-id="56b40-112">Pour plus d’informations sur la création des objets de stratégie de groupe nécessaires, voir [déploiement d’objets de stratégie de groupe MBAM 1,0](deploying-mbam-10-group-policy-objects.md).</span><span class="sxs-lookup"><span data-stu-id="56b40-112">For more information about creating the necessary Group Policy Objects, see [Deploying MBAM 1.0 Group Policy Objects](deploying-mbam-10-group-policy-objects.md).</span></span>

3.  <span data-ttu-id="56b40-113">Lors du démarrage d’un ordinateur exempté, le client MBAM vérifie le paramètre de stratégie d’exemption de l’ordinateur et suspend la protection en fonction de la présence de l’ordinateur dans le groupe de sécurité d’exemption BitLocker.</span><span class="sxs-lookup"><span data-stu-id="56b40-113">When an exempted computer starts, the MBAM client checks the Computer Exemption Policy setting and suspends protection based on whether the computer is part of the BitLocker exemption security group.</span></span>

## <span data-ttu-id="56b40-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="56b40-114">Related topics</span></span>


[<span data-ttu-id="56b40-115">Administration des composants de MBAM1.0</span><span class="sxs-lookup"><span data-stu-id="56b40-115">Administering MBAM 1.0 Features</span></span>](administering-mbam-10-features.md)

 

 





