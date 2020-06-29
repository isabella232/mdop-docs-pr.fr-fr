---
title: Modification de la configuration d'App-V5.0 Client à l'aide du modèle ADMX et d'une stratégie de groupe
description: Modification de la configuration d'App-V5.0 Client à l'aide du modèle ADMX et d'une stratégie de groupe
author: dansimp
ms.assetid: 79d03a2b-2586-4ca7-bbaa-bdeb0a694279
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: cd257691bf223baa5e2919d83fdbf53d34f271ac
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805280"
---
# <span data-ttu-id="cc5a7-103">Modification de la configuration d'App-V5.0 Client à l'aide du modèle ADMX et d'une stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="cc5a7-103">How to Modify App-V 5.0 Client Configuration Using the ADMX Template and Group Policy</span></span>


<span data-ttu-id="cc5a7-104">Utilisez le modèle ADMX App-V 5,0 pour configurer les paramètres du client App-V 5,0 à l’aide du modèle ADMX et de la stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="cc5a7-104">Use the App-V 5.0 ADMX template to configure App-V 5.0 client settings using the ADMX Template and Group Policy.</span></span>

**<span data-ttu-id="cc5a7-105">Pour modifier la configuration du client App-V 5,0 à l’aide d’une stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="cc5a7-105">To modify App-V 5.0 client configuration using Group Policy</span></span>**

1.  <span data-ttu-id="cc5a7-106">Pour modifier la configuration du client App-V 5,0, recherchez les fichiers **ADMXTemplate** disponibles avec App-v 5,0.</span><span class="sxs-lookup"><span data-stu-id="cc5a7-106">To modify the App-V 5.0 client configuration, locate the **ADMXTemplate** files that are available with App-V 5.0.</span></span>

    <span data-ttu-id="cc5a7-107">**Remarques**  Utilisez le lien suivant pour télécharger les modèles App-V 5,0 **ADMX**: <https://go.microsoft.com/fwlink/p/?LinkId=393941> .</span><span class="sxs-lookup"><span data-stu-id="cc5a7-107">**Note** Use the following link to download the App-V 5.0 **ADMX Templates**: <https://go.microsoft.com/fwlink/p/?LinkId=393941>.</span></span>

     

2.  <span data-ttu-id="cc5a7-108">Sur l’ordinateur sur lequel vous gérez la stratégie de groupe, en général le contrôleur de domaine, copiez le fichier template **. admx** dans le répertoire suivant: \*\* &lt; lecteur d’installation &gt; \ \ Windows \ \ PolicyDefinitions\*\*.</span><span class="sxs-lookup"><span data-stu-id="cc5a7-108">On the computer where you manage group Policy, typically the domain controller, copy the template **.admx** file to the following directory: **&lt;Installation Drive&gt; \\ Windows \\ PolicyDefinitions**.</span></span>

    <span data-ttu-id="cc5a7-109">Ensuite, sur le même ordinateur, copiez le fichier **. adml** dans le répertoire suivant: \*\* &lt; InstallationDrive &gt; \ \ Windows \ \ POLICYDEFINITIONS \ \ en-US\*\*.</span><span class="sxs-lookup"><span data-stu-id="cc5a7-109">Next, on the same computer, copy the **.adml** file to the following directory: **&lt;InstallationDrive&gt; \\ Windows \\ PolicyDefinitions \\ en-US**.</span></span>

3.  <span data-ttu-id="cc5a7-110">Une fois que vous avez copié les fichiers, ouvrez la console de gestion des stratégies de groupe, pour modifier les stratégies associées à vos clients App-v 5,0, accédez à stratégies de configuration de l' **ordinateur**  /  **Policies**  /  -application**modèles d’administration**  /  **System**  /  **-V**.</span><span class="sxs-lookup"><span data-stu-id="cc5a7-110">After you have copied the files open the Group Policy Management Console, to modify the policies associated with your App-V 5.0 clients browse to **Computer Configuration** / **Policies** / **Administrative Templates** / **System** / **App-V**.</span></span>

    <span data-ttu-id="cc5a7-111">Vous **avez une suggestion pour App-V**?</span><span class="sxs-lookup"><span data-stu-id="cc5a7-111">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="cc5a7-112">Ajoutez ou Votez en fonction [de suggestions.](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)</span><span class="sxs-lookup"><span data-stu-id="cc5a7-112">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="cc5a7-113">Vous avez un problème lié à l’application-V?</span><span class="sxs-lookup"><span data-stu-id="cc5a7-113">Got an App-V issue?</span></span>** <span data-ttu-id="cc5a7-114">Utilisez le [Forum TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="cc5a7-114">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="cc5a7-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="cc5a7-115">Related topics</span></span>


[<span data-ttu-id="cc5a7-116">Déploiement d'App-V5.0</span><span class="sxs-lookup"><span data-stu-id="cc5a7-116">Deploying App-V 5.0</span></span>](deploying-app-v-50.md)

[<span data-ttu-id="cc5a7-117">À propos des paramètres de configuration du client</span><span class="sxs-lookup"><span data-stu-id="cc5a7-117">About Client Configuration Settings</span></span>](about-client-configuration-settings.md)

 

 





