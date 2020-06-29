---
title: Procédure pour configurer les paramètres de registre du client App-V Client à l'aide de la ligne de commande
description: Procédure pour configurer les paramètres de registre du client App-V Client à l'aide de la ligne de commande
author: dansimp
ms.assetid: 3e3d873f-13d2-402f-97b4-f62d0c399171
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c424f39c8209ca641f6073838ebcb8726acc9e25
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807290"
---
# <span data-ttu-id="fc151-103">Procédure pour configurer les paramètres de registre du client App-V Client à l'aide de la ligne de commande</span><span class="sxs-lookup"><span data-stu-id="fc151-103">How to Configure the App-V Client Registry Settings by Using the Command Line</span></span>


<span data-ttu-id="fc151-104">Après le déploiement et la configuration du client App-V) au cours de l’installation à l’aide de la ligne de commande, il peut être nécessaire de modifier un ou plusieurs paramètres de configuration du client.</span><span class="sxs-lookup"><span data-stu-id="fc151-104">After the Application Virtualization (App-V) Client has been deployed and configured during the installation by using the command line, it might be necessary to change one or more client configuration settings.</span></span> <span data-ttu-id="fc151-105">Pour cela, il suffit de modifier les clés de Registre appropriées en utilisant l’une des méthodes suivantes:</span><span class="sxs-lookup"><span data-stu-id="fc151-105">This is accomplished by editing the appropriate registry keys, using one of the following methods:</span></span>

-   <span data-ttu-id="fc151-106">Utilisation de l’éditeur du Registre directement</span><span class="sxs-lookup"><span data-stu-id="fc151-106">Using the Registry Editor directly</span></span>

-   <span data-ttu-id="fc151-107">À l’aide d’un fichier. reg</span><span class="sxs-lookup"><span data-stu-id="fc151-107">Using a .reg file</span></span>

-   <span data-ttu-id="fc151-108">Utiliser un langage de script tel que VBScript ou Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="fc151-108">Using a scripting language such as VBScript or Windows PowerShell</span></span>

<span data-ttu-id="fc151-109">Vous pouvez également utiliser un modèle ADM.</span><span class="sxs-lookup"><span data-stu-id="fc151-109">There is also an ADM template that you can use.</span></span> <span data-ttu-id="fc151-110">Pour plus d’informations sur le modèle ADM, voir <https://go.microsoft.com/fwlink/?LinkId=121835> .</span><span class="sxs-lookup"><span data-stu-id="fc151-110">For more information about the ADM template, see <https://go.microsoft.com/fwlink/?LinkId=121835>.</span></span>

<span data-ttu-id="fc151-111">**Attention**  Soyez vigilant lorsque vous modifiez le registre, car des erreurs peuvent sortir de l’ordinateur dans un état inutilisable.</span><span class="sxs-lookup"><span data-stu-id="fc151-111">**Caution** Use care when you edit the registry because errors can leave the computer in an unusable state.</span></span> <span data-ttu-id="fc151-112">Veillez à suivre les pratiques d’entreprise standard relatives aux modifications du Registre.</span><span class="sxs-lookup"><span data-stu-id="fc151-112">Be sure to follow your standard business practices that relate to registry edits.</span></span> <span data-ttu-id="fc151-113">Testez minutieusement toutes les modifications proposées dans un environnement de test avant de les déployer sur des ordinateurs de production.</span><span class="sxs-lookup"><span data-stu-id="fc151-113">Thoroughly test all proposed changes in a test environment before you deploy them to production computers.</span></span>

 

## <span data-ttu-id="fc151-114">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="fc151-114">In This Section</span></span>


<span data-ttu-id="fc151-115">**Important**  Sur un ordinateur 64 bits, les clés et les valeurs décrites dans les sections suivantes seront sous HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\Client.</span><span class="sxs-lookup"><span data-stu-id="fc151-115">**Important** On a 64-bit computer, the keys and values described in the following sections will be under HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\Client.</span></span>

 

<a href="" id="how-to-reset-the-filesystem-cache"></a>[<span data-ttu-id="fc151-116">Procédure pour réinitialiser le cache de FileSystem</span><span class="sxs-lookup"><span data-stu-id="fc151-116">How to Reset the FileSystem Cache</span></span>](how-to-reset-the-filesystem-cache.md)  
<span data-ttu-id="fc151-117">Fournit les informations nécessaires pour réinitialiser le cache de systèmes de fichiers.</span><span class="sxs-lookup"><span data-stu-id="fc151-117">Provides the information that is required to reset the FileSystem cache.</span></span>

<a href="" id="how-to-change-the-size-of-the-filesystem-cache"></a>[<span data-ttu-id="fc151-118">Procédure pour modifier la taille du cache de FileSystem</span><span class="sxs-lookup"><span data-stu-id="fc151-118">How to Change the Size of the FileSystem Cache</span></span>](how-to-change-the-size-of-the-filesystem-cache.md)  
<span data-ttu-id="fc151-119">Décrit la manière dont vous pouvez modifier la taille du cache.</span><span class="sxs-lookup"><span data-stu-id="fc151-119">Explains how you can change the size of the cache.</span></span>

<a href="" id="how-to-use-the-cache-space-management-feature"></a>[<span data-ttu-id="fc151-120">Procédure d'utilisation de la fonction de gestion de l'espace du cache</span><span class="sxs-lookup"><span data-stu-id="fc151-120">How to Use the Cache Space Management Feature</span></span>](how-to-use-the-cache-space-management-feature.md)  
<span data-ttu-id="fc151-121">Décrit la manière dont vous pouvez configurer la fonctionnalité de gestion de l’espace de cache.</span><span class="sxs-lookup"><span data-stu-id="fc151-121">Describes how you can configure the cache space management feature.</span></span>

<a href="" id="how-to-configure-the-client-log-file"></a>[<span data-ttu-id="fc151-122">Procédure pour configurer le fichier journal du client</span><span class="sxs-lookup"><span data-stu-id="fc151-122">How to Configure the Client Log File</span></span>](how-to-configure-the-client-log-file.md)  
<span data-ttu-id="fc151-123">Décrit les différentes valeurs de clé de Registre qui contrôlent le fichier journal du client et la façon de les modifier.</span><span class="sxs-lookup"><span data-stu-id="fc151-123">Describes the various registry key values that control the client log file and how you can change them.</span></span>

<a href="" id="how-to-configure-user-permissions"></a>[<span data-ttu-id="fc151-124">Procédure pour configurer les autorisations des utilisateurs</span><span class="sxs-lookup"><span data-stu-id="fc151-124">How to Configure User Permissions</span></span>](how-to-configure-user-permissions.md)  
<span data-ttu-id="fc151-125">Identifie la clé de Registre qui contrôle les autorisations de l’utilisateur et donne des exemples de la manière dont vous pouvez modifier certaines autorisations.</span><span class="sxs-lookup"><span data-stu-id="fc151-125">Identifies the registry key that controls the user permissions and gives examples of how you can change some permissions.</span></span>

<a href="" id="how-to-configure-the-client-for-application-package-retrieval"></a>[<span data-ttu-id="fc151-126">Procédure pour configurer le client afin d'extraire le package d'application</span><span class="sxs-lookup"><span data-stu-id="fc151-126">How to Configure the Client for Application Package Retrieval</span></span>](how-to-configure-the-client-for-application-package-retrieval.md)  
<span data-ttu-id="fc151-127">Décrit la configuration du client pour récupérer le contenu, les icônes et les associations de types de fichiers dans différentes sources et fournit plusieurs exemples du format de chemin d’accès correct.</span><span class="sxs-lookup"><span data-stu-id="fc151-127">Explains how to configure the client to retrieve package content, icons, and file type associations from different sources, and provides several examples of the correct path format.</span></span>

<a href="" id="how-to-configure-the-client-for-disconnected-operation-mode"></a>[<span data-ttu-id="fc151-128">Procédure pour configurer le client en mode de fonctionnement hors connexion</span><span class="sxs-lookup"><span data-stu-id="fc151-128">How to Configure the Client for Disconnected Operation Mode</span></span>](how-to-configure-the-client-for-disconnected-operation-mode.md)  
<span data-ttu-id="fc151-129">Fournit des informations sur la configuration des différents paramètres associés au mode opérations hors connexion.</span><span class="sxs-lookup"><span data-stu-id="fc151-129">Provides information about how to configure the various settings associated with disconnected operations mode.</span></span>

<a href="" id="how-to-configure-shortcut-and-file-type-association-behavior"></a>[<span data-ttu-id="fc151-130">Procédure pour configurer le comportement d'association de type de fichier et de raccourci</span><span class="sxs-lookup"><span data-stu-id="fc151-130">How to Configure Shortcut and File Type Association Behavior</span></span>](how-to-configure-shortcut-and-file-type-association-behavior-46-only.md)  
<span data-ttu-id="fc151-131">Décrit les valeurs de clé de Registre qui contrôlent les raccourcis et les associations de types de fichiers dans le client App-V, et fournit des détails sur la façon de les configurer.</span><span class="sxs-lookup"><span data-stu-id="fc151-131">Describes the registry key values that control shortcuts and file type associations in the App-V client, and provides details on how to configure them.</span></span>

## <span data-ttu-id="fc151-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fc151-132">Related topics</span></span>


[<span data-ttu-id="fc151-133">Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="fc151-133">Application Virtualization Client</span></span>](application-virtualization-client.md)

 

 





