---
title: Configurer les composants requis pour l'installation
description: Configurer les composants requis pour l'installation
author: dansimp
ms.assetid: ff9cf28a-3eac-4b6c-8ce9-bfc202f57947
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 6cd9379804c45a2025064a6eecf363c010980369
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807854"
---
# <span data-ttu-id="8517e-103">Configurer les composants requis pour l'installation</span><span class="sxs-lookup"><span data-stu-id="8517e-103">Configure Installation Prerequisites</span></span>


<span data-ttu-id="8517e-104">Les instructions suivantes sont les conditions préalables à l’installation et à l’utilisation de Microsoft Enterprise Desktop Virtualization (MED-V) 2,0:</span><span class="sxs-lookup"><span data-stu-id="8517e-104">The following instructions are prerequisites for installing and using Microsoft Enterprise Desktop Virtualization (MED-V) 2.0:</span></span>

[<span data-ttu-id="8517e-105">PC virtuel Windows</span><span class="sxs-lookup"><span data-stu-id="8517e-105">Windows Virtual PC</span></span>](#bkmk-howtoinstallandconfiguremicrosoftvirtualpc7)

[<span data-ttu-id="8517e-106">Mise à jour de Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="8517e-106">Windows Virtual PC Update</span></span>](#bkmk-howtoinstallandconfiguremicrosoftvirtualpc7update)

[<span data-ttu-id="8517e-107">Configuration de logiciels antivirus/de sauvegarde</span><span class="sxs-lookup"><span data-stu-id="8517e-107">Antivirus/Backup Software Configuration</span></span>](#bkmk-antivirusbackupsoftwareconfiguration)

## <a href="" id="bkmk-howtoinstallandconfiguremicrosoftvirtualpc7"></a><span data-ttu-id="8517e-108">Installer et configurer l’ordinateur virtuel Windows</span><span class="sxs-lookup"><span data-stu-id="8517e-108">How to Install and Configure Windows Virtual PC</span></span>


<span data-ttu-id="8517e-109">**Important**  S’il existe déjà une version de Virtual PC pour Windows sur l’ordinateur hôte, vous devez la désinstaller avant d’installer le PC virtuel Windows.</span><span class="sxs-lookup"><span data-stu-id="8517e-109">**Important** If a version of Virtual PC for Windows already exists on the host computer, you must uninstall it before you install Windows Virtual PC.</span></span>

 

**<span data-ttu-id="8517e-110">Pour installer l’ordinateur virtuel Windows</span><span class="sxs-lookup"><span data-stu-id="8517e-110">To install Windows Virtual PC</span></span>**

1.  <span data-ttu-id="8517e-111">Téléchargez le [PC virtuel Windows](https://go.microsoft.com/fwlink/?LinkId=195918) à partir du centre de téléchargement Microsoft ( https://go.microsoft.com/fwlink/?LinkId=195918) .</span><span class="sxs-lookup"><span data-stu-id="8517e-111">Download [Windows Virtual PC](https://go.microsoft.com/fwlink/?LinkId=195918) from the Microsoft Download Center (https://go.microsoft.com/fwlink/?LinkId=195918).</span></span>

2.  <span data-ttu-id="8517e-112">Exécutez le fichier d’installation sur l’ordinateur hôte, puis suivez les étapes de l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="8517e-112">Run the installation file on the host computer, and follow the steps in the wizard.</span></span>

<span data-ttu-id="8517e-113">**Important**  Windows Virtual PC inclut le package composants d’intégration, qui fournit des fonctionnalités qui améliorent l’interaction entre l’environnement virtuel et l’ordinateur physique.</span><span class="sxs-lookup"><span data-stu-id="8517e-113">**Important** Windows Virtual PC includes the Integration Components package, which provides features that improve the interaction between the virtual environment and the physical computer.</span></span> <span data-ttu-id="8517e-114">Par exemple, il permet de déplacer la souris entre l’hôte et les ordinateurs invités.</span><span class="sxs-lookup"><span data-stu-id="8517e-114">For example, it lets your mouse move between the host and the guest computers.</span></span> <span data-ttu-id="8517e-115">MED-V nécessite l’installation du package composants d’intégration.</span><span class="sxs-lookup"><span data-stu-id="8517e-115">MED-V requires the installation of the Integration Components package.</span></span>

 

## <a href="" id="bkmk-howtoinstallandconfiguremicrosoftvirtualpc7update"></a><span data-ttu-id="8517e-116">Installation et configuration de la mise à jour de Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="8517e-116">How to Install and Configure the Windows Virtual PC Update</span></span>


<span data-ttu-id="8517e-117">La mise à jour Microsoft associée à l’article KB977206 permet le mode Windows XP pour les ordinateurs sans technologie HAV.</span><span class="sxs-lookup"><span data-stu-id="8517e-117">The Microsoft update associated with article KB977206 enables Windows XP Mode for computers without hardware-assisted virtualization (HAV) technology.</span></span> <span data-ttu-id="8517e-118">Nous vous recommandons d’installer cette mise à jour, car il est possible que certaines fonctionnalités d’intégration ne fonctionnent pas correctement si le package composants d’intégration du système d’exploitation invité ne correspond pas à la version de PC virtuel Windows installée sur l’ordinateur hôte.</span><span class="sxs-lookup"><span data-stu-id="8517e-118">We recommended that you install this update because some integration features might not work correctly if the Integration Components package in the guest operating system do not match the version of Windows Virtual PC that is installed on the host computer.</span></span>

<span data-ttu-id="8517e-119">**Important**  Vous n’avez pas besoin d’installer cette mise à jour lorsque vous installez MED-V sur des ordinateurs hôtes exécutant Windows 7 avec Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="8517e-119">**Important** You do not have to install this update when you are installing MED-V on host computers that are running Windows 7 with Service Pack 1.</span></span>

 

<span data-ttu-id="8517e-120">**Astuce**  Outre la mise à jour répertoriée ici, nous vous conseillons de passer en revue toutes les mises à jour de PC virtuelles Windows disponibles et d’appliquer les mises à jour appropriées ou nécessaires pour votre environnement.</span><span class="sxs-lookup"><span data-stu-id="8517e-120">**Tip** In addition to the update listed here, we recommend that you review all available Windows Virtual PC updates and apply those updates that are appropriate or necessary for your environment.</span></span>

 

**<span data-ttu-id="8517e-121">Pour installer la mise à jour de Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="8517e-121">To install the Windows Virtual PC Update</span></span>**

1.  <span data-ttu-id="8517e-122">Téléchargez la mise à jour de PC virtuel Windows requise à partir du centre de téléchargement Microsoft.</span><span class="sxs-lookup"><span data-stu-id="8517e-122">Download the required Windows Virtual PC update from the Microsoft Download Center.</span></span>

    <span data-ttu-id="8517e-123">[mise à jour 32 bits](https://go.microsoft.com/fwlink/?LinkId=195919) ( https://go.microsoft.com/fwlink/?LinkId=195919) .</span><span class="sxs-lookup"><span data-stu-id="8517e-123">[32-bit Update](https://go.microsoft.com/fwlink/?LinkId=195919) (https://go.microsoft.com/fwlink/?LinkId=195919).</span></span>

    <span data-ttu-id="8517e-124">[mise à jour 64 bits](https://go.microsoft.com/fwlink/?LinkId=195920) ( https://go.microsoft.com/fwlink/?LinkId=195920) .</span><span class="sxs-lookup"><span data-stu-id="8517e-124">[64-bit Update](https://go.microsoft.com/fwlink/?LinkId=195920) (https://go.microsoft.com/fwlink/?LinkId=195920).</span></span>

2.  <span data-ttu-id="8517e-125">Exécutez le fichier d’installation sur l’ordinateur hôte en mode avec élévation de privilèges, puis suivez les étapes de l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="8517e-125">Run the installation file on the host computer in elevated mode, and follow the steps in the wizard.</span></span>

    <span data-ttu-id="8517e-126">Pour plus d’informations sur le correctif logiciel pour PC virtuel Windows, voir [l’article 977206](https://go.microsoft.com/fwlink/?LinkId=195921) ( https://go.microsoft.com/fwlink/?LinkId=195921) .</span><span class="sxs-lookup"><span data-stu-id="8517e-126">For more information about the hotfix package for Windows Virtual PC, see [article 977206](https://go.microsoft.com/fwlink/?LinkId=195921) (https://go.microsoft.com/fwlink/?LinkId=195921).</span></span>

## <a href="" id="bkmk-antivirusbackupsoftwareconfiguration"></a><span data-ttu-id="8517e-127">Comment configurer un logiciel antivirus/de sauvegarde</span><span class="sxs-lookup"><span data-stu-id="8517e-127">How to Configure Antivirus/Backup Software</span></span>


<span data-ttu-id="8517e-128">Pour empêcher les activités de protection antivirus d’affecter les performances de la version de bureau virtuelle, nous vous conseillons, par exemple, d’exclure les types de fichiers d’ordinateur virtuel suivants de tout logiciel antivirus ou de processus de sauvegarde qui s’exécute sur l’ordinateur hôte:</span><span class="sxs-lookup"><span data-stu-id="8517e-128">To prevent antivirus activity from affecting the performance of the virtual desktop, we recommend, where you can, to exclude the following virtual machine file types from any antivirus or backup process that is running on the host computer:</span></span>

-   <span data-ttu-id="8517e-129">\*. COMPATIBLE</span><span class="sxs-lookup"><span data-stu-id="8517e-129">\*.VMC</span></span>

-   <span data-ttu-id="8517e-130">\*. VUD</span><span class="sxs-lookup"><span data-stu-id="8517e-130">\*.VUD</span></span>

-   <span data-ttu-id="8517e-131">\*. VSV</span><span class="sxs-lookup"><span data-stu-id="8517e-131">\*.VSV</span></span>

-   <span data-ttu-id="8517e-132">\*. VIRTUELS</span><span class="sxs-lookup"><span data-stu-id="8517e-132">\*.VHD</span></span>

## <span data-ttu-id="8517e-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8517e-133">Related topics</span></span>


[<span data-ttu-id="8517e-134">Configurer la configuration requise de l'environnement</span><span class="sxs-lookup"><span data-stu-id="8517e-134">Configure Environment Prerequisites</span></span>](configure-environment-prerequisites.md)

[<span data-ttu-id="8517e-135">Architecture de haut niveau</span><span class="sxs-lookup"><span data-stu-id="8517e-135">High-Level Architecture</span></span>](high-level-architecturemedv2.md)

[<span data-ttu-id="8517e-136">Configurations prises en charge par MED-V2.0</span><span class="sxs-lookup"><span data-stu-id="8517e-136">MED-V 2.0 Supported Configurations</span></span>](med-v-20-supported-configurations.md)

 

 





