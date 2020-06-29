---
title: À propos d'User Experience Virtualization1.0
description: À propos d'User Experience Virtualization1.0
author: dansimp
ms.assetid: 3758b100-35a8-4e10-ac08-f583fb8ddbd9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6010f9c4ebc260eec0324fb880dc2c92fd675130
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809521"
---
# <span data-ttu-id="1bfec-103">À propos d'User Experience Virtualization1.0</span><span class="sxs-lookup"><span data-stu-id="1bfec-103">About User Experience Virtualization 1.0</span></span>


<span data-ttu-id="1bfec-104">Microsoft User Interface Virtualization (UE-V) vérifie les modifications apportées par les utilisateurs aux paramètres d’application et aux paramètres du système d’exploitation Windows.</span><span class="sxs-lookup"><span data-stu-id="1bfec-104">Microsoft User Experience Virtualization (UE-V) monitors the changes that are made by users to application settings and Windows operating system settings.</span></span> <span data-ttu-id="1bfec-105">Les paramètres utilisateur sont capturés et centralisés vers un emplacement de stockage des paramètres.</span><span class="sxs-lookup"><span data-stu-id="1bfec-105">The user settings are captured and centralized to a settings storage location.</span></span> <span data-ttu-id="1bfec-106">Ces paramètres peuvent ensuite être appliqués aux différents ordinateurs consultés par l’utilisateur, tels que des ordinateurs de bureau, des ordinateurs portables et des sessions VDI (Virtual Desktop Infrastructure).</span><span class="sxs-lookup"><span data-stu-id="1bfec-106">These settings can then be applied to the different computers that are accessed by the user, including desktop computers, laptop computers, and virtual desktop infrastructure (VDI) sessions.</span></span>

<span data-ttu-id="1bfec-107">La virtualisation de l’interface utilisateur utilise les modèles d’emplacement des paramètres pour spécifier les applications et les paramètres Windows sur les ordinateurs des utilisateurs qui sont surveillés et centralisés.</span><span class="sxs-lookup"><span data-stu-id="1bfec-107">User Experience Virtualization uses settings location templates to specify what applications and Windows settings on the user computers are monitored and centralized.</span></span> <span data-ttu-id="1bfec-108">Le modèle d’emplacement des paramètres est un fichier XML qui spécifie le fichier et les emplacements du Registre associés à chaque paramètre de l’application ou du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="1bfec-108">The settings location template is an XML file that specifies which file and registry locations are associated with each application or operating system setting.</span></span> <span data-ttu-id="1bfec-109">Le modèle ne contient pas de valeurs pour les paramètres. Il contient uniquement les emplacements des paramètres à surveiller.</span><span class="sxs-lookup"><span data-stu-id="1bfec-109">The template does not contain values for the settings; it contains only the locations of the settings that are to be monitored.</span></span>

<span data-ttu-id="1bfec-110">Les paramètres de l’application et les paramètres Windows sont surveillés par UE-V lorsque les utilisateurs travaillent sur leur ordinateur.</span><span class="sxs-lookup"><span data-stu-id="1bfec-110">The application settings and Windows settings are monitored by UE-V when users are working on their computers.</span></span> <span data-ttu-id="1bfec-111">Les valeurs des paramètres de l’application sont stockées sur le serveur de stockage de paramètres lorsque l’utilisateur ferme l’application.</span><span class="sxs-lookup"><span data-stu-id="1bfec-111">The values for the application settings are stored on the settings storage server when the user closes the application.</span></span> <span data-ttu-id="1bfec-112">Les valeurs des paramètres Windows sont stockées lorsque l’utilisateur se déconnecte, lorsque l’ordinateur est verrouillé, ou lorsqu’il se déconnecte à distance à partir d’un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="1bfec-112">The values for the Windows settings are stored when the user logs off, when the computer is locked, or when they disconnect remotely from a computer.</span></span>

<span data-ttu-id="1bfec-113">Un administrateur peut créer un modèle d’emplacement des paramètres UE-V pour spécifier quels paramètres d’application d’entreprise seront itinérants.</span><span class="sxs-lookup"><span data-stu-id="1bfec-113">An administrator can create a UE-V settings location template to specify which enterprise application settings will roam.</span></span> <span data-ttu-id="1bfec-114">UE-V inclut un ensemble de modèles d’emplacement pour certains paramètres de l’application Microsoft et de Windows.</span><span class="sxs-lookup"><span data-stu-id="1bfec-114">UE-V includes a set of settings location templates for some Microsoft applications and Windows settings.</span></span> <span data-ttu-id="1bfec-115">Pour obtenir la liste des applications et paramètres par défaut dans UE-V, voir [planification des applications à synchroniser avec UE-v 1,0](planning-which-applications-to-synchronize-with-ue-v-10.md).</span><span class="sxs-lookup"><span data-stu-id="1bfec-115">For a list of default applications and settings in UE-V, see [Planning Which Applications to Synchronize with UE-V 1.0](planning-which-applications-to-synchronize-with-ue-v-10.md).</span></span>

## <span data-ttu-id="1bfec-116">Notes de publication de UEV 1,0</span><span class="sxs-lookup"><span data-stu-id="1bfec-116">UEV 1.0 Release Notes</span></span>


<span data-ttu-id="1bfec-117">Pour plus d’informations et pour les actualités de dernière minute qui n’ont pas été intégrées à la documentation, voir [notes de publication de Microsoft User Interface Virtualization (UE-V) 1,0](microsoft-user-experience-virtualization--ue-v--10-release-notes.md).</span><span class="sxs-lookup"><span data-stu-id="1bfec-117">For more information, and for late-breaking news that did not make it into the documentation, see [Microsoft User Experience Virtualization (UE-V) 1.0 Release Notes](microsoft-user-experience-virtualization--ue-v--10-release-notes.md).</span></span>

## <span data-ttu-id="1bfec-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1bfec-118">Related topics</span></span>


[<span data-ttu-id="1bfec-119">Prise en main de User Experience Virtualization1.0</span><span class="sxs-lookup"><span data-stu-id="1bfec-119">Getting Started With User Experience Virtualization 1.0</span></span>](getting-started-with-user-experience-virtualization-10.md)

[<span data-ttu-id="1bfec-120">Microsoft User Experience Virtualization (UE-V)1.0</span><span class="sxs-lookup"><span data-stu-id="1bfec-120">Microsoft User Experience Virtualization (UE-V) 1.0</span></span>](index.md)

[<span data-ttu-id="1bfec-121">Architecture de haut niveau pour UE-V1.0</span><span class="sxs-lookup"><span data-stu-id="1bfec-121">High-Level Architecture for UE-V 1.0</span></span>](high-level-architecture-for-ue-v-10.md)

 

 





