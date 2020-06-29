---
title: Comment créer un fichier de configuration personnalisé à l'aide de la console de gestion App-V5.0
description: Comment créer un fichier de configuration personnalisé à l'aide de la console de gestion App-V5.0
author: dansimp
ms.assetid: 0d1f6768-be30-4682-8eeb-aa95918b24c3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d54e68caa380025b2ff6f3ea79d30f275b589b30
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805646"
---
# <span data-ttu-id="4148a-103">Comment créer un fichier de configuration personnalisé à l'aide de la console de gestion App-V5.0</span><span class="sxs-lookup"><span data-stu-id="4148a-103">How to Create a Custom Configuration File by Using the App-V 5.0 Management Console</span></span>


<span data-ttu-id="4148a-104">Vous pouvez utiliser une configuration dynamique pour personnaliser un package App-V 5,0 pour un utilisateur spécifique.</span><span class="sxs-lookup"><span data-stu-id="4148a-104">You can use a dynamic configuration to customize an App-V 5.0 package for a specific user.</span></span> <span data-ttu-id="4148a-105">Toutefois, vous devez commencer par créer le fichier de configuration de l’utilisateur dynamique (. Xml) ou de configuration du déploiement dynamique avant de pouvoir utiliser les fichiers.</span><span class="sxs-lookup"><span data-stu-id="4148a-105">However, you must first create the dynamic user configuration (.xml) file or the dynamic deployment configuration file before you can use the files.</span></span> <span data-ttu-id="4148a-106">La création du fichier est une opération manuelle avancée.</span><span class="sxs-lookup"><span data-stu-id="4148a-106">Creation of the file is an advanced manual operation.</span></span> <span data-ttu-id="4148a-107">Pour obtenir des informations générales sur les fichiers de configuration utilisateur dynamique, voir [à propos de la configuration dynamique App-V 5,0](about-app-v-50-dynamic-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="4148a-107">For general information about dynamic user configuration files, see, [About App-V 5.0 Dynamic Configuration](about-app-v-50-dynamic-configuration.md).</span></span>

<span data-ttu-id="4148a-108">Utilisez la procédure suivante pour créer un fichier de configuration utilisateur dynamique à l’aide de la console de gestion App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="4148a-108">Use the following procedure to create a Dynamic User Configuration file by using the App-V 5.0 Management console.</span></span>

**<span data-ttu-id="4148a-109">Pour créer un fichier de configuration utilisateur dynamique</span><span class="sxs-lookup"><span data-stu-id="4148a-109">To create a Dynamic User Configuration file</span></span>**

1.  <span data-ttu-id="4148a-110">Cliquez avec le bouton droit sur le nom du package que vous souhaitez afficher, puis sélectionnez **modifier l’accès Active Directory** pour afficher la configuration affectée à un groupe d’utilisateurs donné.</span><span class="sxs-lookup"><span data-stu-id="4148a-110">Right-click the name of the package that you want to view and select **Edit active directory access** to view the configuration that is assigned to a given user group.</span></span> <span data-ttu-id="4148a-111">Vous pouvez également sélectionner le package, puis cliquer sur **modifier**.</span><span class="sxs-lookup"><span data-stu-id="4148a-111">Alternatively, select the package, and click **Edit**.</span></span>

2.  <span data-ttu-id="4148a-112">À l’aide de la liste d' **entités publicitaires avec Access**, sélectionnez le groupe d’annonces que vous voulez personnaliser.</span><span class="sxs-lookup"><span data-stu-id="4148a-112">Using the list of **AD Entities with Access**, select the AD group that you want to customize.</span></span> <span data-ttu-id="4148a-113">Sélectionnez **personnalisé** dans la liste déroulante, si ce n’est pas déjà fait.</span><span class="sxs-lookup"><span data-stu-id="4148a-113">Select **Custom** from the drop-down list, if it is not already selected.</span></span> <span data-ttu-id="4148a-114">Un lien intitulé **modifier** s’affichera.</span><span class="sxs-lookup"><span data-stu-id="4148a-114">A link named **Edit** will be displayed.</span></span>

3.  <span data-ttu-id="4148a-115">Cliquez sur **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="4148a-115">Click **Edit**.</span></span> <span data-ttu-id="4148a-116">La configuration utilisateur dynamique affectée au groupe d’annonces est affichée.</span><span class="sxs-lookup"><span data-stu-id="4148a-116">The Dynamic User Configuration that is assigned to the AD Group will be displayed.</span></span>

4.  <span data-ttu-id="4148a-117">Cliquez sur **avancé**, puis sur **Exporter la configuration**.</span><span class="sxs-lookup"><span data-stu-id="4148a-117">Click **Advanced**, and then click **Export Configuration**.</span></span> <span data-ttu-id="4148a-118">Tapez un nom de fichier, puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="4148a-118">Type in a filename and click **Save**.</span></span> <span data-ttu-id="4148a-119">Vous pouvez à présent modifier le fichier pour configurer un package pour un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4148a-119">Now you can edit the file to configure a package for a user.</span></span>

    <span data-ttu-id="4148a-120">Vous **avez une suggestion pour App-V**?</span><span class="sxs-lookup"><span data-stu-id="4148a-120">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="4148a-121">Ajoutez ou Votez en fonction [de suggestions.](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)</span><span class="sxs-lookup"><span data-stu-id="4148a-121">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="4148a-122">Vous avez un problème lié à l’application-V?</span><span class="sxs-lookup"><span data-stu-id="4148a-122">Got an App-V issue?</span></span>** <span data-ttu-id="4148a-123">Utilisez le [Forum TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="4148a-123">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="4148a-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4148a-124">Related topics</span></span>


[<span data-ttu-id="4148a-125">Opérations d'App-V5.0</span><span class="sxs-lookup"><span data-stu-id="4148a-125">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 





