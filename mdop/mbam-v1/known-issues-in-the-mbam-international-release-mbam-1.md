---
title: Problèmes connus dans MBAM International Release
description: Problèmes connus dans MBAM International Release
author: dansimp
ms.assetid: bbf888dc-93c1-4323-b43c-0ded098e9b93
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: af32551135ff297d25930f94b40bf04c0fcaaafe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811364"
---
# <span data-ttu-id="76998-103">Problèmes connus dans MBAM International Release</span><span class="sxs-lookup"><span data-stu-id="76998-103">Known Issues in the MBAM International Release</span></span>

<span data-ttu-id="76998-104">Cette section contient des problèmes connus de la version internationale de Microsoft BitLocker (MBAM).</span><span class="sxs-lookup"><span data-stu-id="76998-104">This section contains known issues for Microsoft BitLocker Administration and Monitoring (MBAM) International Release.</span></span>

## <span data-ttu-id="76998-105">Problèmes connus dans MBAM International Release</span><span class="sxs-lookup"><span data-stu-id="76998-105">Known Issues in the MBAM International Release</span></span>

### <span data-ttu-id="76998-106">Le processus d’installation ne spécifie pas de mise à jour</span><span class="sxs-lookup"><span data-stu-id="76998-106">The Installation Process Does Not Specify Update</span></span>

<span data-ttu-id="76998-107">Lors de la mise à jour du serveur d’administration et de contrôle Microsoft BitLocker, le programme d’installation ne vérifie pas l’installation d’une mise à jour.</span><span class="sxs-lookup"><span data-stu-id="76998-107">Upon updating the Microsoft BitLocker Administration and Monitoring server or servers, the Setup program does not state that an update is being installed.</span></span>

<span data-ttu-id="76998-108">**Solution de contournement**: aucune.</span><span class="sxs-lookup"><span data-stu-id="76998-108">**Workaround**: None.</span></span>

### <span data-ttu-id="76998-109">Certificats utilisés pour le rôle serveur d’administration et de surveillance</span><span class="sxs-lookup"><span data-stu-id="76998-109">Certificates Used for the Administration and Monitoring Server Role</span></span>

<span data-ttu-id="76998-110">Si vous utilisez un certificat pour l’authentification entre MBAM Servers, après avoir mis à jour le serveur d’administration et de surveillance MBAM, vous devez vous assurer que le certificat est valide et qu’il n’est pas révoqué ou expiré.</span><span class="sxs-lookup"><span data-stu-id="76998-110">If you are using a certificate for authentication between MBAM servers, after updating the MBAM Administration and Monitoring server you must ensure that the certificate is valid and not revoked or expired.</span></span>

<span data-ttu-id="76998-111">**Solution de contournement**: aucune.</span><span class="sxs-lookup"><span data-stu-id="76998-111">**Workaround**: None.</span></span>

### <span data-ttu-id="76998-112">MBAM svclog de remplissage de fichier</span><span class="sxs-lookup"><span data-stu-id="76998-112">MBAM Svclog File Filling Disk Space</span></span>

<span data-ttu-id="76998-113">Si vous avez suivi les étapes de la [base de connaissances 2668170](https://go.microsoft.com/fwlink/?LinkID=247277), il se peut que vous deviez répéter les étapes Ko après l’installation de cette mise à jour.</span><span class="sxs-lookup"><span data-stu-id="76998-113">If you have followed [Knowledge Base article 2668170](https://go.microsoft.com/fwlink/?LinkID=247277), you might have to repeat the KB steps after you install this update.</span></span>

<span data-ttu-id="76998-114">**Solution de contournement**: aucune.</span><span class="sxs-lookup"><span data-stu-id="76998-114">**Workaround**: None.</span></span>

## <span data-ttu-id="76998-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="76998-115">Related topics</span></span>

[<span data-ttu-id="76998-116">Déploiement de MBAM1.0 Language Release Update</span><span class="sxs-lookup"><span data-stu-id="76998-116">Deploying the MBAM 1.0 Language Release Update</span></span>](deploying-the-mbam-10-language-release-update.md)

 

 





