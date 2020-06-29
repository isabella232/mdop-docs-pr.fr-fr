---
title: Procédure de déploiement de DaRT7.0
description: Procédure de déploiement de DaRT7.0
author: dansimp
ms.assetid: 30522441-40cb-4eca-99b4-dff758f5c647
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c2059b64e5f3ae7af8926bc00e5965598ede4288
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804686"
---
# <span data-ttu-id="9006c-103">Procédure de déploiement de DaRT7.0</span><span class="sxs-lookup"><span data-stu-id="9006c-103">How to Deploy DaRT 7.0</span></span>


<span data-ttu-id="9006c-104">Cette rubrique fournit des instructions sur le déploiement de Microsoft Diagnostics and Recovery Tools (DaRT) 7 dans votre environnement.</span><span class="sxs-lookup"><span data-stu-id="9006c-104">This topic provides instructions to deploy Microsoft Diagnostics and Recovery Toolset (DaRT)7 in your environment.</span></span> <span data-ttu-id="9006c-105">La première procédure décrite dans cette rubrique part du principe que vous installez toutes les fonctionnalités sur un ordinateur d’administration.</span><span class="sxs-lookup"><span data-stu-id="9006c-105">The first procedure in this topic assumes that you are installing all functionality on one administrator computer.</span></span> <span data-ttu-id="9006c-106">Lorsque vous devez déployer ou désinstaller DaRT sur plusieurs ordinateurs, à l’aide d’un système de distribution de logiciels électronique par exemple, il peut être plus facile d’utiliser les options d’installation de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="9006c-106">When you need to deploy or uninstall DaRT on multiple computers, using an electronic software distribution system for example, it might be easier to use command line installation options.</span></span> <span data-ttu-id="9006c-107">Ces options sont définies dans la deuxième procédure de cette rubrique, qui fournit un exemple d’utilisation pour les options de ligne de commande disponibles.</span><span class="sxs-lookup"><span data-stu-id="9006c-107">Those options are defined in the second procedure in this topic which provides example usage for the available command line options.</span></span>

<span data-ttu-id="9006c-108">**Important**  Avant d’installer DaRT, assurez-vous que l’ordinateur répond à la configuration minimale requise décrite dans [configurations dart 7,0 prises en charge](dart-70-supported-configurations-dart-7.md).</span><span class="sxs-lookup"><span data-stu-id="9006c-108">**Important** Before you install DaRT, ensure that the computer meets the minimum system requirements listed in [DaRT 7.0 Supported Configurations](dart-70-supported-configurations-dart-7.md).</span></span>

 

**<span data-ttu-id="9006c-109">Pour installer DaRT sur un ordinateur d’administration</span><span class="sxs-lookup"><span data-stu-id="9006c-109">To install DaRT on an administrator computer</span></span>**

1.  <span data-ttu-id="9006c-110">Recherchez les fichiers d’installation de DaRT que vous avez reçus dans le cadre de votre téléchargement de logiciels.</span><span class="sxs-lookup"><span data-stu-id="9006c-110">Locate the DaRT installation files that you received as part of your software download.</span></span>

2.  <span data-ttu-id="9006c-111">Double-cliquez sur le fichier d’installation DaRT qui correspond à la configuration système requise: 32-bits ou 64 bits.</span><span class="sxs-lookup"><span data-stu-id="9006c-111">Double-click the DaRT installation file that corresponds to your system requirements, either 32-bit or 64-bit.</span></span> <span data-ttu-id="9006c-112">Le fichier d’installation de DaRT est nommé **MSDaRT70.msi**.</span><span class="sxs-lookup"><span data-stu-id="9006c-112">The DaRT installation file is named **MSDaRT70.msi**.</span></span>

3.  <span data-ttu-id="9006c-113">Acceptez les termes du contrat de licence logiciel Microsoft, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="9006c-113">Accept the Microsoft Software License Terms, and then click **Next**.</span></span>

4.  <span data-ttu-id="9006c-114">Sélectionnez le dossier de destination pour l’installation de DaRT, indiquez si le DaRT doit être installé pour tous les utilisateurs ou uniquement pour l’utilisateur actuel, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="9006c-114">Select the destination folder for installing DaRT, select whether DaRT should be installed for all users or just the current user, and then click **Next**.</span></span>

5.  <span data-ttu-id="9006c-115">Indiquez si l’installation doit être **normale**, **personnalisée**ou **complète**, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="9006c-115">Select whether the installation should be **Typical**, **Custom**, or **Complete**, and then click **Next**.</span></span>

    -   <span data-ttu-id="9006c-116">Installations **typiques** les outils les plus fréquemment utilisés.</span><span class="sxs-lookup"><span data-stu-id="9006c-116">**Typical** installs the tools that are most frequently used.</span></span> <span data-ttu-id="9006c-117">Cette méthode est recommandée pour la plupart des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="9006c-117">This method is recommended for most users.</span></span>

    -   <span data-ttu-id="9006c-118">**Personnalisé** vous permet de sélectionner les outils qui sont installés et l’emplacement où ils seront installés.</span><span class="sxs-lookup"><span data-stu-id="9006c-118">**Custom** lets you select the tools that are installed and where they will be installed.</span></span> <span data-ttu-id="9006c-119">Cette option est recommandée pour les utilisateurs avancés, en particulier si vous installez différents outils DaRT sur différents ordinateurs du support technique.</span><span class="sxs-lookup"><span data-stu-id="9006c-119">This is recommended for advanced users, especially if you are installing different DaRT tools on different helpdesk computers.</span></span>

    -   <span data-ttu-id="9006c-120">**Complète** installe tous les outils DART et nécessite le plus d’espace disque.</span><span class="sxs-lookup"><span data-stu-id="9006c-120">**Complete** installs all DaRT tools and requires the most disk space.</span></span>

    <span data-ttu-id="9006c-121">Après avoir sélectionné votre mode d’installation, cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="9006c-121">After you have selected your method of installation, click **Next**.</span></span>

6.  <span data-ttu-id="9006c-122">Pour démarrer l’installation, cliquez sur **installer**.</span><span class="sxs-lookup"><span data-stu-id="9006c-122">To start the installation, click **Install**.</span></span>

7.  <span data-ttu-id="9006c-123">Une fois l’installation terminée, cliquez sur **Terminer** pour quitter l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="9006c-123">After the installation is completed successfully, click **Finish** to exit the wizard.</span></span>

**<span data-ttu-id="9006c-124">Pour installer DaRT à l’invite de commandes</span><span class="sxs-lookup"><span data-stu-id="9006c-124">To install DaRT at the command prompt</span></span>**

1.  <span data-ttu-id="9006c-125">L’exemple suivant montre comment installer toutes les fonctionnalités de DaRT.</span><span class="sxs-lookup"><span data-stu-id="9006c-125">The following example shows how to install all DaRT functionality.</span></span>

    ``` syntax
    msiexec /i MSDaRT70.msi ADDLOCAL=CommonFiles,MSDaRTHelp,DaRTRecoveryImage,CrashAnalyzer,RemoteViewer 
    ```

2.  <span data-ttu-id="9006c-126">L’exemple suivant montre comment installer uniquement l' **Assistant image de récupération DART**.</span><span class="sxs-lookup"><span data-stu-id="9006c-126">The following example shows how to install only the **DaRT Recovery Image Wizard**.</span></span>

    ``` syntax
    msiexec /i MSDaRT70.msi ADDLOCAL=CommonFiles,MSDaRTHelp,DaRTRecoveryImage
    ```

3.  <span data-ttu-id="9006c-127">L’exemple suivant montre comment installer uniquement l’analyseur d’incidents et la visionneuse de connexion à distance DaRT.</span><span class="sxs-lookup"><span data-stu-id="9006c-127">The following example shows how to install only the Crash Analyzer and the DaRT Remote Connection Viewer.</span></span>

    ``` syntax
    msiexec /i MSDaRT70.msi ADDLOCAL=CommonFiles,MSDaRTHelp,CrashAnalyzer,RemoteViewer 
    ```

4.  <span data-ttu-id="9006c-128">L’exemple suivant crée un journal d’installation pour le programme d’installation de Windows.</span><span class="sxs-lookup"><span data-stu-id="9006c-128">The following example creates a setup log for the Windows Installer.</span></span> <span data-ttu-id="9006c-129">Cela est utile pour le débogage.</span><span class="sxs-lookup"><span data-stu-id="9006c-129">This is valuable for debugging.</span></span>

    ``` syntax
    msiexec.exe /i MSDaRT70.msi /l*v log.txt 
    ```

<span data-ttu-id="9006c-130">**Remarques**  Vous pouvez ajouter/qn ou/qb aux options d’invite de commandes de l’installation de DaRT pour effectuer une installation silencieuse.</span><span class="sxs-lookup"><span data-stu-id="9006c-130">**Note** You can add /qn or /qb to any of the DaRT installation command prompt options to perform a silent installation.</span></span>

 

## <span data-ttu-id="9006c-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9006c-131">Related topics</span></span>


[<span data-ttu-id="9006c-132">Déploiement de DaRT7.0 sur les ordinateurs des administrateurs</span><span class="sxs-lookup"><span data-stu-id="9006c-132">Deploying DaRT 7.0 to Administrator Computers</span></span>](deploying-dart-70-to-administrator-computers-dart-7.md)

 

 





