---
title: Notes de publication pour MED-V1.0
description: Notes de publication pour MED-V1.0
author: dansimp
ms.assetid: 006a3537-5c5b-43b5-8df8-4bf6ddd3cd2f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 683056f768a3d547828996a9b191d58337c21ad6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811849"
---
# <span data-ttu-id="1a975-103">Notes de publication pour MED-V1.0</span><span class="sxs-lookup"><span data-stu-id="1a975-103">MED-V 1.0 Release Notes</span></span>


## <span data-ttu-id="1a975-104">Problèmes connus avec MED-V</span><span class="sxs-lookup"><span data-stu-id="1a975-104">Known Issues with MED-V</span></span>


<span data-ttu-id="1a975-105">Cette section fournit des informations détaillées sur les problèmes généraux liés à la plateforme Microsoft Enterprise Desktop Virtualization (MED-V).</span><span class="sxs-lookup"><span data-stu-id="1a975-105">This section provides the most up-to-date information about general issues with the Microsoft Enterprise Desktop Virtualization (MED-V) platform.</span></span> <span data-ttu-id="1a975-106">Ces problèmes n’apparaissent pas dans la documentation du produit et, dans certains cas, il peut s’avérer contradictoire.</span><span class="sxs-lookup"><span data-stu-id="1a975-106">These issues do not appear in the product documentation and in some cases might contradict existing product documentation.</span></span> <span data-ttu-id="1a975-107">Dans la mesure du possible, ces problèmes seront résolus dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="1a975-107">Whenever possible, these issues will be addressed in later releases.</span></span>

### <span data-ttu-id="1a975-108">Les téléchargements de fichiers ne respectent pas les règles de redirection Web</span><span class="sxs-lookup"><span data-stu-id="1a975-108">File downloads do not follow Web redirection rules</span></span>

<span data-ttu-id="1a975-109">Les téléchargements de fichiers ne respectent pas les règles de redirection Web définies dans une stratégie d’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="1a975-109">File downloads do not follow Web redirection rules set in a MED-V workspace policy.</span></span>

### <span data-ttu-id="1a975-110">Lorsque vous développez une fenêtre d’application publiée sur la console en mode plein écran, cette dernière disparaît</span><span class="sxs-lookup"><span data-stu-id="1a975-110">When expanding a console-published application window to full screen, it disappears</span></span>

<span data-ttu-id="1a975-111">Si vous développez une application de console publiée (par exemple, cmd.exe) en plein écran à l’intérieur d’un espace de travail MED-V configuré en mode d’intégration transparente, la fenêtre de l’application peut disparaître ou ne pas répondre.</span><span class="sxs-lookup"><span data-stu-id="1a975-111">If you expand a console-published application (such as cmd.exe) window to full screen inside a MED-V workspace configured in seamless integration mode, the application window might disappear or not respond.</span></span>

### <span data-ttu-id="1a975-112">Lorsque vous travaillez en mode Bureau complet, les emplacements des icônes sur le Bureau ne sont pas enregistrés</span><span class="sxs-lookup"><span data-stu-id="1a975-112">When working in full desktop mode, icon locations on the desktop are not saved</span></span>

<span data-ttu-id="1a975-113">Lorsque vous travaillez en mode Bureau complet, le changement d’emplacement manuel des icônes sur le bureau n’est pas enregistré entre les sessions d’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="1a975-113">When working in full desktop mode, manual location changes of icons on the desktop are not saved between MED-V workspace sessions.</span></span>

### <span data-ttu-id="1a975-114">Une image locale et une image de test portant le même nom ne peuvent pas exister dans le même domaine</span><span class="sxs-lookup"><span data-stu-id="1a975-114">A local image and a test image with the same name cannot exist in the same domain</span></span>

<span data-ttu-id="1a975-115">Si une image locale est jointe au domaine et que l’administrateur crée une nouvelle version de la même image portant le même nom d’ordinateur qu’une image de test, lorsque l’image de test rejoint le domaine, l’action joindre le domaine échoue ou l’image locale est supprimée du domaine.</span><span class="sxs-lookup"><span data-stu-id="1a975-115">If a local image is joined to the domain and the administrator creates a new version of the same image with the same computer name as a test image, when the test image joins the domain, either the join domain action fails or it succeeds and the local image is removed from the domain.</span></span>

### <span data-ttu-id="1a975-116">MED-V ne prend pas en charge les fonctionnalités de Windows Aero</span><span class="sxs-lookup"><span data-stu-id="1a975-116">MED-V does not support Windows Aero features</span></span>

<span data-ttu-id="1a975-117">MED-V ne prend pas en charge les fonctionnalités de Windows Aero (comme Aero Flip 3D).</span><span class="sxs-lookup"><span data-stu-id="1a975-117">MED-V does not support Windows Aero features (such as Aero Flip 3D).</span></span>

### <span data-ttu-id="1a975-118">La console de gestion ne peut être utilisée que par un seul utilisateur Windows par ordinateur</span><span class="sxs-lookup"><span data-stu-id="1a975-118">The management console can be used by only one Windows user per computer</span></span>

<span data-ttu-id="1a975-119">La console de gestion MED-V ne peut être utilisée que par les administrateurs et les utilisateurs Windows qui ont installé l’application de gestion.</span><span class="sxs-lookup"><span data-stu-id="1a975-119">The MED-V management console can be used only by administrators and the Windows user who installed the management application.</span></span>

### <span data-ttu-id="1a975-120">L’utilitaire de configuration de serveur MED-V teste la connectivité de Microsoft SQL Server sous le contexte de l’utilisateur plutôt que dans le contexte de service du serveur MED-V.</span><span class="sxs-lookup"><span data-stu-id="1a975-120">The MED-V Server configuration utility tests Microsoft SQL Server connectivity under user context rather than under MED-V Server service context</span></span>

<span data-ttu-id="1a975-121">MED-V utilise le contexte de service du serveur MED-V pour collecter des rapports à partir de la base de données Microsoft SQL Server Reports.</span><span class="sxs-lookup"><span data-stu-id="1a975-121">MED-V uses MED-V Server service context to collect reports from the Microsoft SQL Server reports database.</span></span> <span data-ttu-id="1a975-122">L’utilitaire de configuration de serveur MED-V vérifie la base de données et teste la chaîne de connexion de la base de données.</span><span class="sxs-lookup"><span data-stu-id="1a975-122">The MED-V Server configuration utility verifies the database and tests the database connection string.</span></span> <span data-ttu-id="1a975-123">Cela ne valide pas l’accès au service du serveur MED-V à la base de données.</span><span class="sxs-lookup"><span data-stu-id="1a975-123">It does not validate the access of MED-V Server service to the database.</span></span>

 

 





