---
title: Procédure pour publier une application virtuelle sur le client
description: Procédure pour publier une application virtuelle sur le client
author: dansimp
ms.assetid: 90af843e-b5b3-4a71-a3a1-fa5f4c087f28
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b5585f82150db69929ccedbee3aecab969c5e7dc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806881"
---
# <span data-ttu-id="bc02b-103">Procédure pour publier une application virtuelle sur le client</span><span class="sxs-lookup"><span data-stu-id="bc02b-103">How to Publish a Virtual Application on the Client</span></span>


<span data-ttu-id="bc02b-104">Lorsque vous déployez la virtualisation d’application à l’aide d’un système de distribution de logiciels électronique, vous pouvez utiliser l’une des procédures suivantes pour publier un package d’application pour vos utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="bc02b-104">When you deploy Application Virtualization by using an electronic software distribution system, you can use one of the following procedures to publish an application package to your users.</span></span>

**<span data-ttu-id="bc02b-105">Pour publier un package à l’aide d’un fichier Windows Installer autonome</span><span class="sxs-lookup"><span data-stu-id="bc02b-105">To publish a package using a stand-alone Windows Installer file</span></span>**

1.  <span data-ttu-id="bc02b-106">Le client doit être installé avec le paramètre *RequireAuthorizationIfCached* défini sur 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="bc02b-106">The client should be installed with the *REQUIREAUTHORIZATIONIFCACHED* parameter set to 0 (zero).</span></span> <span data-ttu-id="bc02b-107">Pour plus d’informations sur la définition de ce paramètre, voir [paramètres de ligne de commande du programme d’installation de l’application virtualisation du client](application-virtualization-client-installer-command-line-parameters.md)</span><span class="sxs-lookup"><span data-stu-id="bc02b-107">For more information about setting this parameter, see [Application Virtualization Client Installer Command-Line Parameters](application-virtualization-client-installer-command-line-parameters.md)</span></span>

2.  <span data-ttu-id="bc02b-108">Copiez le fichier Windows Installer et le fichier SFT dans le même dossier sur l’ordinateur cible.</span><span class="sxs-lookup"><span data-stu-id="bc02b-108">Copy the Windows Installer file and the SFT file to same folder on the target computer.</span></span>

3.  <span data-ttu-id="bc02b-109">Exécutez la commande suivante sur votre ordinateur:</span><span class="sxs-lookup"><span data-stu-id="bc02b-109">Run the following command on the computer:</span></span>

    `Msiexec.exe /I "packagename.msi" /q`

**<span data-ttu-id="bc02b-110">Pour publier un package à l’aide du programme d’installation Windows et du manifeste du package</span><span class="sxs-lookup"><span data-stu-id="bc02b-110">To publish a package using Windows Installer and the package manifest</span></span>**

1.  <span data-ttu-id="bc02b-111">Copiez le fichier du programme d’installation Windows sur l’ordinateur cible et le fichier SFT dans le partage de contenu sur le serveur de diffusion.</span><span class="sxs-lookup"><span data-stu-id="bc02b-111">Copy the Windows Installer file to the target computer and the SFT file to the CONTENT share on the streaming server.</span></span>

2.  <span data-ttu-id="bc02b-112">Exécutez la commande suivante sur l’ordinateur de l’utilisateur:</span><span class="sxs-lookup"><span data-stu-id="bc02b-112">Run the following command on each user’s computer:</span></span>

    `Msiexec.exe /I "\\pathtomsi\packagename.msi" MODE=STREAMING  OVERRIDEURL="\\\\server\\share\\package.sft" LOAD=TRUE /q`

    <span data-ttu-id="bc02b-113">**Important**  Pour OVERRIDEURL, tous les caractères de barre oblique inverse doivent être placés dans une séquence d’échappement en utilisant une barre oblique inverse précédente ou le chemin OVERRIDEURL ne sera pas analysé correctement.</span><span class="sxs-lookup"><span data-stu-id="bc02b-113">**Important** For OVERRIDEURL all backslash characters must be escaped using a preceding backslash, or the OVERRIDEURL path will not be parsed correctly.</span></span> <span data-ttu-id="bc02b-114">De plus, les propriétés et les valeurs doivent être entrées en majuscules sauf si la valeur est un chemin d’accès à un fichier.</span><span class="sxs-lookup"><span data-stu-id="bc02b-114">Also, properties and values must be entered as uppercase except where the value is a path to a file.</span></span>

     

**<span data-ttu-id="bc02b-115">Pour publier un package à l’aide de SFTMIME</span><span class="sxs-lookup"><span data-stu-id="bc02b-115">To publish a package using SFTMIME</span></span>**

-   <span data-ttu-id="bc02b-116">Pour obtenir un exemple de publication d’une application pour tous les utilisateurs sur un ordinateur, exécutez la commande suivante sur l’ordinateur de l’utilisateur:</span><span class="sxs-lookup"><span data-stu-id="bc02b-116">For an example of how to publish an application for all users on a computer, run the following command on the user’s computer:</span></span>

    `SFTMIME ADD PACKAGE:package-name /MANIFEST manifest-path                                 [/GLOBAL] [/LOG log-pathname | /CONSOLE | /GUI]`

    <span data-ttu-id="bc02b-117">Pour plus d’informations sur ces commandes de SFTMIME et d’autres, voir [référence aux commandes SFTMIME](sftmime--command-reference.md).</span><span class="sxs-lookup"><span data-stu-id="bc02b-117">For additional details about these and other SFTMIME commands, see [SFTMIME Command Reference](sftmime--command-reference.md).</span></span>

## <span data-ttu-id="bc02b-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bc02b-118">Related topics</span></span>


[<span data-ttu-id="bc02b-119">Choisir une méthode de publication</span><span class="sxs-lookup"><span data-stu-id="bc02b-119">Determine Your Publishing Method</span></span>](determine-your-publishing-method.md)

[<span data-ttu-id="bc02b-120">Scénario basé sur une distribution électronique de logiciels</span><span class="sxs-lookup"><span data-stu-id="bc02b-120">Electronic Software Distribution-Based Scenario</span></span>](electronic-software-distribution-based-scenario.md)

[<span data-ttu-id="bc02b-121">Référence de commande SFTMIME</span><span class="sxs-lookup"><span data-stu-id="bc02b-121">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

[<span data-ttu-id="bc02b-122">Scénario de distribution autonome pour les clients Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="bc02b-122">Stand-Alone Delivery Scenario for Application Virtualization Clients</span></span>](stand-alone-delivery-scenario-for-application-virtualization-clients.md)

 

 





