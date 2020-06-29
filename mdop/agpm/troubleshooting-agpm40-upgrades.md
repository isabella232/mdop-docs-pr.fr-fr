---
title: Résoudre les problèmes de mise à niveau d’AGPM
description: Résoudre les problèmes de mise à niveau d’AGPM
author: dansimp
ms.assetid: 1abbf0c1-fd32-46a8-a3ba-c005f066523d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2089eac51803dca60da51f61ebdb112fbf0bda08
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807430"
---
# <span data-ttu-id="24bd2-103">Résoudre les problèmes de mise à niveau d’AGPM</span><span class="sxs-lookup"><span data-stu-id="24bd2-103">Troubleshooting AGPM Upgrades</span></span>

<span data-ttu-id="24bd2-104">Cette section répertorie les problèmes courants que vous pouvez rencontrer lors de la mise à niveau de votre serveur de gestion des stratégies de groupe (AGPM) avancé vers une nouvelle version (par exemple, AGPM 4,0 vers AGPM 4,3).</span><span class="sxs-lookup"><span data-stu-id="24bd2-104">This section lists common issues that you may encounter when you upgrade your Advanced Group Policy Management (AGPM) server to a newer version (e.g. AGPM 4.0 to AGPM 4.3).</span></span> <span data-ttu-id="24bd2-105">Pour diagnostiquer des problèmes qui ne sont pas répertoriés ici, il est possible que vous deviez Voir la [résolution des](troubleshooting-agpm-agpm40.md) problèmes d’AGPM ou d’un administrateur AGPM (contrôle total) pour utiliser la journalisation et le suivi.</span><span class="sxs-lookup"><span data-stu-id="24bd2-105">To diagnose issues not listed here, it may be helpful to view the [Troubleshooting AGPM](troubleshooting-agpm-agpm40.md) or for an AGPM Administrator (Full Control) to use logging and tracing.</span></span> <span data-ttu-id="24bd2-106">Pour plus d’informations, voir [configurer la journalisation et le suivi](configure-logging-and-tracing-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="24bd2-106">For more information, see [Configure Logging and Tracing](configure-logging-and-tracing-agpm40.md).</span></span>

## <span data-ttu-id="24bd2-107">Quels problèmes rencontrez-vous?</span><span class="sxs-lookup"><span data-stu-id="24bd2-107">What problems are you having?</span></span>

-   [<span data-ttu-id="24bd2-108">Échec de la génération d’un rapport de différences d’objets de stratégie de groupe HTML (code d’erreur 80004003)</span><span class="sxs-lookup"><span data-stu-id="24bd2-108">Failed to generate a HTML GPO difference report (Error code 80004003)</span></span>](#bkmk-error-80004003)

### <a href="" id="bkmk-error-80004003"></a><span data-ttu-id="24bd2-109">Échec de la génération d’un rapport de différences d’objets de stratégie de groupe HTML (code d’erreur 80004003)</span><span class="sxs-lookup"><span data-stu-id="24bd2-109">Failed to generate a HTML GPO difference report (Error code 80004003)</span></span>

-   <span data-ttu-id="24bd2-110">**Cause**: vous avez installé le package de mise à niveau d’AGPM avec un compte incorrect.</span><span class="sxs-lookup"><span data-stu-id="24bd2-110">**Cause**: You have installed the AGPM upgrade package with an incorrect account.</span></span>

-   <span data-ttu-id="24bd2-111">**Solution**: vous devrez être un administrateur d’AGPM pour pouvoir résoudre ce problème.</span><span class="sxs-lookup"><span data-stu-id="24bd2-111">**Solution**: You will need to be an AGPM administrator in order to fix this issue.</span></span>
    
    -   <span data-ttu-id="24bd2-112">Vérifiez que vous connaissez le nom d’utilisateur & mot de passe de votre **compte de service AGPM**.</span><span class="sxs-lookup"><span data-stu-id="24bd2-112">Ensure you know the username & password of your **AGPM service account**.</span></span>

    -   <span data-ttu-id="24bd2-113">Connectez-vous sur votre serveur AGPM de manière interactive en tant que compte de service AGPM.</span><span class="sxs-lookup"><span data-stu-id="24bd2-113">Log onto your AGPM server interactively as your AGPM service account.</span></span>
        
        -   <span data-ttu-id="24bd2-114">C’est essentiel, car l’installation échoue si vous utilisez un autre compte.</span><span class="sxs-lookup"><span data-stu-id="24bd2-114">This is critically important, as the install will fail if you use a different account.</span></span>

    -   <span data-ttu-id="24bd2-115">Arrêtez le service AGPM.</span><span class="sxs-lookup"><span data-stu-id="24bd2-115">Shutdown the AGPM service.</span></span>
    
    -   <span data-ttu-id="24bd2-116">Installez le correctif requis.</span><span class="sxs-lookup"><span data-stu-id="24bd2-116">Install the required hotfix.</span></span>
    
    -   <span data-ttu-id="24bd2-117">Connectez-vous à AGPM à l’aide d’un client AGPM pour vérifier que vos rapports de différences fonctionnent désormais.</span><span class="sxs-lookup"><span data-stu-id="24bd2-117">Connect to AGPM using an AGPM client to test that your difference reports are now functioning.</span></span>
    
## <span data-ttu-id="24bd2-118">Installer le correctif logiciel 1 pour la gestion avancée de la stratégie de groupe Microsoft 4,0 SP3</span><span class="sxs-lookup"><span data-stu-id="24bd2-118">Install Hotfix Package 1 for Microsoft Advanced Group Policy Management 4.0 SP3</span></span>
    
<span data-ttu-id="24bd2-119">**Problème résolu dans ce correctif**: AGPM ne peut pas générer de rapports de différences quand il contrôle ou gère de nouveaux objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="24bd2-119">**Issue fixed in this hotfix**: AGPM can't generate difference reports when it controls or manages new Group Policy Objects (GPOs).</span></span>

<span data-ttu-id="24bd2-120">**Pour obtenir cette mise à jour**, procédez comme suit: Installez la dernière version de Microsoft Desktop Optimization Pack ([version de maintenance du 2017 mars](https://www.microsoft.com/download/details.aspx?id=54967)).</span><span class="sxs-lookup"><span data-stu-id="24bd2-120">**How to get this update**: Install the latest version of Microsoft Desktop Optimization Pack ([March 2017 Servicing Release](https://www.microsoft.com/download/details.aspx?id=54967)).</span></span> <span data-ttu-id="24bd2-121">Pour plus d’informations, voir [KB 4014009](https://support.microsoft.com/help/4014009/) .</span><span class="sxs-lookup"><span data-stu-id="24bd2-121">See [KB 4014009](https://support.microsoft.com/help/4014009/) for more information.</span></span>

<span data-ttu-id="24bd2-122">Plus précisément, vous pouvez choisir de télécharger uniquement le premier fichier, `AGPM4.0SP1_Server_X64_KB4014009.exe` dans la liste qui s’affiche après avoir appuyé sur le bouton Télécharger.</span><span class="sxs-lookup"><span data-stu-id="24bd2-122">More specifically, you can choose to download only the first file, `AGPM4.0SP1_Server_X64_KB4014009.exe`, from the list presented after pressing the download button.</span></span>
      
<span data-ttu-id="24bd2-123">Pour plus d’informations [, consultez le](https://www.microsoft.com/download/details.aspx?id=54967)lien de téléchargement du pack d’optimisation de bureau de Microsoft (version de service de mars 2017).</span><span class="sxs-lookup"><span data-stu-id="24bd2-123">The download link to the Microsoft Desktop Optimization Pack (March 2017 Servicing Release) can be found [here](https://www.microsoft.com/download/details.aspx?id=54967).</span></span>
      
      
## <span data-ttu-id="24bd2-124">Lien de référence</span><span class="sxs-lookup"><span data-stu-id="24bd2-124">Reference link</span></span>
https://support.microsoft.com/help/3127165/hotfix-package-1-for-microsoft-advanced-group-policy-management-4-0-sp
      
