---
title: Comment créer un fichier de configuration personnalisé à l'aide de la console de gestion App-V5.1
description: Comment créer un fichier de configuration personnalisé à l'aide de la console de gestion App-V5.1
author: dansimp
ms.assetid: f5ab426a-f49a-47b3-93f3-b9d60aada8f4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 282207b5424442950e88c40a372194e9def768cb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805641"
---
# <span data-ttu-id="05a5b-103">Comment créer un fichier de configuration personnalisé à l'aide de la console de gestion App-V5.1</span><span class="sxs-lookup"><span data-stu-id="05a5b-103">How to Create a Custom Configuration File by Using the App-V 5.1 Management Console</span></span>


<span data-ttu-id="05a5b-104">Vous pouvez utiliser une configuration dynamique pour personnaliser un package App-V 5,1 pour un utilisateur spécifique.</span><span class="sxs-lookup"><span data-stu-id="05a5b-104">You can use a dynamic configuration to customize an App-V 5.1 package for a specific user.</span></span> <span data-ttu-id="05a5b-105">Toutefois, vous devez commencer par créer le fichier de configuration de l’utilisateur dynamique (. Xml) ou de configuration du déploiement dynamique avant de pouvoir utiliser les fichiers.</span><span class="sxs-lookup"><span data-stu-id="05a5b-105">However, you must first create the dynamic user configuration (.xml) file or the dynamic deployment configuration file before you can use the files.</span></span> <span data-ttu-id="05a5b-106">La création du fichier est une opération manuelle avancée.</span><span class="sxs-lookup"><span data-stu-id="05a5b-106">Creation of the file is an advanced manual operation.</span></span> <span data-ttu-id="05a5b-107">Pour obtenir des informations générales sur les fichiers de configuration utilisateur dynamique, voir [à propos de la configuration dynamique App-V 5,1](about-app-v-51-dynamic-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="05a5b-107">For general information about dynamic user configuration files, see, [About App-V 5.1 Dynamic Configuration](about-app-v-51-dynamic-configuration.md).</span></span>

<span data-ttu-id="05a5b-108">Utilisez la procédure suivante pour créer un fichier de configuration utilisateur dynamique à l’aide de la console de gestion App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="05a5b-108">Use the following procedure to create a Dynamic User Configuration file by using the App-V 5.1 Management console.</span></span>

**<span data-ttu-id="05a5b-109">Pour créer un fichier de configuration utilisateur dynamique</span><span class="sxs-lookup"><span data-stu-id="05a5b-109">To create a Dynamic User Configuration file</span></span>**

1.  <span data-ttu-id="05a5b-110">Cliquez avec le bouton droit sur le nom du package que vous souhaitez afficher, puis sélectionnez **modifier l’accès Active Directory** pour afficher la configuration affectée à un groupe d’utilisateurs donné.</span><span class="sxs-lookup"><span data-stu-id="05a5b-110">Right-click the name of the package that you want to view and select **Edit active directory access** to view the configuration that is assigned to a given user group.</span></span> <span data-ttu-id="05a5b-111">Vous pouvez également sélectionner le package, puis cliquer sur **modifier**.</span><span class="sxs-lookup"><span data-stu-id="05a5b-111">Alternatively, select the package, and click **Edit**.</span></span>

2.  <span data-ttu-id="05a5b-112">À l’aide de la liste d' **entités publicitaires avec Access**, sélectionnez le groupe d’annonces que vous voulez personnaliser.</span><span class="sxs-lookup"><span data-stu-id="05a5b-112">Using the list of **AD Entities with Access**, select the AD group that you want to customize.</span></span> <span data-ttu-id="05a5b-113">Sélectionnez **personnalisé** dans la liste déroulante, si ce n’est pas déjà fait.</span><span class="sxs-lookup"><span data-stu-id="05a5b-113">Select **Custom** from the drop-down list, if it is not already selected.</span></span> <span data-ttu-id="05a5b-114">Un lien intitulé **modifier** s’affichera.</span><span class="sxs-lookup"><span data-stu-id="05a5b-114">A link named **Edit** will be displayed.</span></span>

3.  <span data-ttu-id="05a5b-115">Cliquez sur **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="05a5b-115">Click **Edit**.</span></span> <span data-ttu-id="05a5b-116">La configuration utilisateur dynamique affectée au groupe d’annonces est affichée.</span><span class="sxs-lookup"><span data-stu-id="05a5b-116">The Dynamic User Configuration that is assigned to the AD Group will be displayed.</span></span>

4.  <span data-ttu-id="05a5b-117">Cliquez sur **avancé**, puis sur **Exporter la configuration**.</span><span class="sxs-lookup"><span data-stu-id="05a5b-117">Click **Advanced**, and then click **Export Configuration**.</span></span> <span data-ttu-id="05a5b-118">Tapez un nom de fichier, puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="05a5b-118">Type in a filename and click **Save**.</span></span> <span data-ttu-id="05a5b-119">Vous pouvez à présent modifier le fichier pour configurer un package pour un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="05a5b-119">Now you can edit the file to configure a package for a user.</span></span>

    **<span data-ttu-id="05a5b-120">Remarque</span><span class="sxs-lookup"><span data-stu-id="05a5b-120">Note</span></span>**  
    <span data-ttu-id="05a5b-121">Pour exporter une configuration en exécutant sur Windows Server, vous devez désactiver «configuration de la sécurité améliorée d’Internet Explorer».</span><span class="sxs-lookup"><span data-stu-id="05a5b-121">To export a configuration while running on Windows Server, you must disable "IE Enhanced Security Configuration".</span></span> <span data-ttu-id="05a5b-122">Si cette option est activée et définie pour bloquer les téléchargements, vous ne pouvez pas télécharger un fichier à partir de l’App-V Server.</span><span class="sxs-lookup"><span data-stu-id="05a5b-122">If this is enabled and set to block downloads, you cannot download anything from the App-V Server.</span></span>



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## <span data-ttu-id="05a5b-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="05a5b-123">Related topics</span></span>


[<span data-ttu-id="05a5b-124">Opérations d'App-V5.1</span><span class="sxs-lookup"><span data-stu-id="05a5b-124">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)









