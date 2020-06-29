---
title: Procédure pour installer le client via la ligne de commande
description: Procédure pour installer le client via la ligne de commande
author: dansimp
ms.assetid: ed372403-64ff-48ff-a3cd-a46cad04a4d5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: eca594e1399b4ca4f680f68efffcd011fdc5f042
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807061"
---
# <span data-ttu-id="7f6ad-103">Procédure pour installer le client via la ligne de commande</span><span class="sxs-lookup"><span data-stu-id="7f6ad-103">How to Install the Client by Using the Command Line</span></span>


<span data-ttu-id="7f6ad-104">Les rubriques de cette section incluent des procédures permettant d’installer le client de bureau App-V (App-V) ou le client App-V pour les services Bureau à distance (auparavant services Terminal Server) en utilisant setup.exe ou setup.msi.</span><span class="sxs-lookup"><span data-stu-id="7f6ad-104">The topics in this section include procedures to install either the Application Virtualization (App-V) Desktop Client or the App-V Client for Remote Desktop Services (formerly Terminal Services) by using either setup.exe or setup.msi.</span></span> <span data-ttu-id="7f6ad-105">Des droits d’administration sont requis pour exécuter un programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="7f6ad-105">Administrative rights are required to run either setup program.</span></span>

<span data-ttu-id="7f6ad-106">Vous pouvez utiliser des paramètres de ligne de commande facultatifs pour appliquer des paramètres de configuration spécifiques au client App-V lors de l’installation.</span><span class="sxs-lookup"><span data-stu-id="7f6ad-106">You can use optional command-line parameters to apply specific configuration settings to the App-V client during the installation.</span></span> <span data-ttu-id="7f6ad-107">Pour plus d’informations sur l’utilisation des paramètres, voir [paramètres de ligne de commande du programme de virtualisation des applications](application-virtualization-client-installer-command-line-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="7f6ad-107">For more information about using parameters, see [Application Virtualization Client Installer Command-Line Parameters](application-virtualization-client-installer-command-line-parameters.md).</span></span> <span data-ttu-id="7f6ad-108">Si vous avez appliqué des paramètres de Registre à un ordinateur avant de déployer un client, par exemple, à l’aide d’une stratégie de groupe, ces paramètres sont conservés et les paramètres de ligne de commande supplémentaires sont appliqués.</span><span class="sxs-lookup"><span data-stu-id="7f6ad-108">If you have applied registry settings to a computer before deploying a client—for example, by using Group Policy—these settings are retained and any additional command line parameters are applied.</span></span> <span data-ttu-id="7f6ad-109">Les valeurs des paramètres de ligne de commande remplacent toute valeur existante pour le même paramètre.</span><span class="sxs-lookup"><span data-stu-id="7f6ad-109">Command line parameter values will replace any existing value for the same setting.</span></span>

<span data-ttu-id="7f6ad-110">**Remarques**  Lorsque vous installez le client App-V pour une utilisation avec un cache en lecture seule, par exemple avec une implémentation de serveur VDI, vous devez définir le paramètre *AUTOLOADTARGET* sur None pour empêcher le client d’essayer de mettre à jour des applications lorsque le cache est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="7f6ad-110">**Note** When you install the App-V client to use with a read-only cache, for example with a VDI server implementation, you must set the *AUTOLOADTARGET* parameter to NONE to prevent the client from trying to update applications when the cache is read-only.</span></span>

 

<span data-ttu-id="7f6ad-111">Pour plus d’informations sur la définition de ces valeurs de paramètres après l’installation, voir [Comment configurer les paramètres du registre des clients App-v à l’aide de la ligne de commande](https://go.microsoft.com/fwlink/?LinkId=169355) ( https://go.microsoft.com/fwlink/?LinkId=169355) dans le guide des opérations d’application-v).</span><span class="sxs-lookup"><span data-stu-id="7f6ad-111">For more information about setting these parameter values after installation, see [How to Configure the App-V Client Registry Settings by Using the Command Line](https://go.microsoft.com/fwlink/?LinkId=169355) (https://go.microsoft.com/fwlink/?LinkId=169355) in the Application Virtualization (App-V) Operations Guide.</span></span>

<span data-ttu-id="7f6ad-112">**Remarques**  Si un paramètre de configuration de l’ordinateur de l’utilisateur dépend du chemin d’installation du client, Notez que le client de virtualisation des applications (App-V) 4.5 copie ses fichiers d’installation dans un autre dossier que les versions précédentes.</span><span class="sxs-lookup"><span data-stu-id="7f6ad-112">**Note** If a configuration setting on the user’s computer depends on the client installation path, note that the Application Virtualization (App-V)4.5 client copies its installation files to a different folder than previous versions did.</span></span> <span data-ttu-id="7f6ad-113">Par défaut, une nouvelle installation du client App-V 4.5 copie ses fichiers d’installation dans le dossier du client de la virtualisation de l’application C:\\Program Files\\Microsoft.</span><span class="sxs-lookup"><span data-stu-id="7f6ad-113">By default, a new installation of the App-V4.5 client will copy its installation files to the \\Program Files\\Microsoft Application Virtualization Client folder.</span></span> <span data-ttu-id="7f6ad-114">Si une version antérieure du client est déjà installée, l’exécution du programme d’installation du client App-V 4,5 effectue une mise à niveau du client existant à l’aide du dossier d’installation existant.</span><span class="sxs-lookup"><span data-stu-id="7f6ad-114">If an earlier version of the client is already installed, running the App-V 4.5 client installer will perform an upgrade of the existing client using the existing installation folder.</span></span>

 

<span data-ttu-id="7f6ad-115">\ [Valeur du jeton de modèle \]</span><span class="sxs-lookup"><span data-stu-id="7f6ad-115">\[Template Token Value\]</span></span>

<span data-ttu-id="7f6ad-116">**Remarques**  Pour App-version 4.6 ou ultérieure, lorsque le client App-V est installé, SFTLDR.DLL est copié dans l’annuaire Windows\\system32.</span><span class="sxs-lookup"><span data-stu-id="7f6ad-116">**Note** For App-V version4.6 and later, when the App-V client is installed, SFTLDR.DLL is copied to the Windows\\system32 directory.</span></span> <span data-ttu-id="7f6ad-117">Si le client App-V est installé sur un système 64 bits, SFTLDR\_WOW64.DLL est copié dans l’annuaire Windows\\SysWOW64.</span><span class="sxs-lookup"><span data-stu-id="7f6ad-117">If the App-V client is installed on a 64-bit system, SFTLDR\_WOW64.DLL is copied to the Windows\\SysWOW64 directory.</span></span>

 

<span data-ttu-id="7f6ad-118">\ [Valeur du jeton de modèle \]</span><span class="sxs-lookup"><span data-stu-id="7f6ad-118">\[Template Token Value\]</span></span>

## <span data-ttu-id="7f6ad-119">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="7f6ad-119">In This Section</span></span>


<span data-ttu-id="7f6ad-120">Les rubriques suivantes expliquent comment installer le client de bureau App-V ou le client App-V pour les services Bureau à distance (auparavant services Terminal Server) en utilisant setup.exe ou setup.msi.</span><span class="sxs-lookup"><span data-stu-id="7f6ad-120">The following topics describe how to install either the Application Virtualization (App-V) Desktop Client or the App-V Client for Remote Desktop Services (formerly Terminal Services) by using either setup.exe or setup.msi.</span></span>

<a href="" id="how-to-install-the-app-v-client-by-using-setup-exe"></a>[<span data-ttu-id="7f6ad-121">Procédure pour installer le client App-V Client à l'aide de setup.exe</span><span class="sxs-lookup"><span data-stu-id="7f6ad-121">How to Install the App-V Client by Using Setup.exe</span></span>](how-to-install-the-app-v-client-by-using-setupexe-new.md)  
<span data-ttu-id="7f6ad-122">Fournit une procédure pas à pas pour l’installation du client App-V à l’aide du programme setup.exe.</span><span class="sxs-lookup"><span data-stu-id="7f6ad-122">Provides a step-by-step procedure for installing the App-V client by using the setup.exe program.</span></span>

<a href="" id="how-to-install-the-app-v-client-by-using-setup-msi"></a>[<span data-ttu-id="7f6ad-123">Procédure pour installer le client App-V Client à l'aide de setup.msi</span><span class="sxs-lookup"><span data-stu-id="7f6ad-123">How to Install the App-V Client by Using Setup.msi</span></span>](how-to-install-the-app-v-client-by-using-setupmsi-new.md)  
<span data-ttu-id="7f6ad-124">Fournit des procédures pas à pas pour l’installation de logiciels requis et également du client App-V à l’aide du programme setup.msi.</span><span class="sxs-lookup"><span data-stu-id="7f6ad-124">Provides step-by-step procedures for installing any prerequisite software and also the App-V client by using the setup.msi program.</span></span>

## <span data-ttu-id="7f6ad-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7f6ad-125">Related topics</span></span>


[<span data-ttu-id="7f6ad-126">Paramètres de ligne de commande du programme d'installation d'Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="7f6ad-126">Application Virtualization Client Installer Command-Line Parameters</span></span>](application-virtualization-client-installer-command-line-parameters.md)

[<span data-ttu-id="7f6ad-127">Procédure pour installer manuellement Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="7f6ad-127">How to Manually Install the Application Virtualization Client</span></span>](how-to-manually-install-the-application-virtualization-client.md)

[<span data-ttu-id="7f6ad-128">Procédure pour publier une application virtuelle sur le client</span><span class="sxs-lookup"><span data-stu-id="7f6ad-128">How to Publish a Virtual Application on the Client</span></span>](how-to-publish-a-virtual-application-on-the-client.md)

[<span data-ttu-id="7f6ad-129">Procédure pour désinstaller App-V Client</span><span class="sxs-lookup"><span data-stu-id="7f6ad-129">How to Uninstall the App-V Client</span></span>](how-to-uninstall-the-app-v-client.md)

 

 





