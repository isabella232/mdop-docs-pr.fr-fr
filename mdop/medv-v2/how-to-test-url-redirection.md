---
title: Comment tester la redirection d'URL
description: Comment tester la redirection d'URL
author: dansimp
ms.assetid: 38d80088-da1d-4098-b27e-76f9e78f81dc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: d964cf9d0114d3085d7e8952eebc82486b7b76cc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810560"
---
# <span data-ttu-id="0309d-103">Comment tester la redirection d'URL</span><span class="sxs-lookup"><span data-stu-id="0309d-103">How to Test URL Redirection</span></span>


<span data-ttu-id="0309d-104">Suite à l’exécution de votre test de configuration pour la première fois, vous pouvez vérifier que la fonctionnalité de redirection d’URL fonctionne normalement en effectuant les tâches suivantes.</span><span class="sxs-lookup"><span data-stu-id="0309d-104">After your test of first time setup finishes, you can verify that the URL redirection functionality is working as expected by performing the following tasks.</span></span>

<span data-ttu-id="0309d-105">**Important**  L’agent hôte MED-V doit être en cours d’exécution pour que la redirection d’URL fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="0309d-105">**Important** The MED-V Host Agent must be running for URL redirection to function correctly.</span></span>

<a href="" id="bkmk-urlredir"></a>**<span data-ttu-id="0309d-106">Pour tester la redirection d’URL</span><span class="sxs-lookup"><span data-stu-id="0309d-106">To test URL Redirection</span></span>**

1.  <span data-ttu-id="0309d-107">Ouvrez un navigateur Internet Explorer sur l’ordinateur hôte, puis entrez l’URL que vous avez spécifiée pour la redirection.</span><span class="sxs-lookup"><span data-stu-id="0309d-107">Open an Internet Explorer browser in the host computer and enter a URL that you specified for redirection.</span></span>

2.  <span data-ttu-id="0309d-108">Vérifiez que la page Web est ouverte dans Internet Explorer sur l’ordinateur virtuel invité.</span><span class="sxs-lookup"><span data-stu-id="0309d-108">Verify that the webpage is opened in Internet Explorer on the guest virtual machine.</span></span>

3.  <span data-ttu-id="0309d-109">Répétez cette procédure pour chaque URL que vous souhaitez tester.</span><span class="sxs-lookup"><span data-stu-id="0309d-109">Repeat this process for each URL that you want to test.</span></span>

**<span data-ttu-id="0309d-110">Pour vérifier qu’il est possible d’ajouter ou de supprimer une URL</span><span class="sxs-lookup"><span data-stu-id="0309d-110">To test that a URL can be added or removed</span></span>**

1.  <span data-ttu-id="0309d-111">Ajoutez ou supprimez une URL de l’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="0309d-111">Add or remove a URL from the MED-V workspace.</span></span>

    <span data-ttu-id="0309d-112">Pour plus d’informations sur la façon d’ajouter et de supprimer des URL pour la redirection dans un espace de travail MED-V, voir [gérer la redirection d’URL med-v](manage-med-v-url-redirection.md).</span><span class="sxs-lookup"><span data-stu-id="0309d-112">For information about how to add and remove URLs for redirection on a MED-V workspace, see [Manage MED-V URL Redirection](manage-med-v-url-redirection.md).</span></span>

2.  <span data-ttu-id="0309d-113">Si vous avez ajouté une URL à la liste de redirection, répétez les étapes de la procédure [de test de redirection d’URL](#bkmk-urlredir) pour vérifier que la nouvelle URL est redirigée comme prévu.</span><span class="sxs-lookup"><span data-stu-id="0309d-113">If you added a URL to the redirection list, repeat the steps in [To Test URL Redirection](#bkmk-urlredir) to verify that the new URL redirects as intended.</span></span>

3.  <span data-ttu-id="0309d-114">Si vous avez supprimé une URL de la liste de redirection, vérifiez qu’elle est supprimée en procédant comme suit:</span><span class="sxs-lookup"><span data-stu-id="0309d-114">If you removed a URL from the redirection list, verify that it is removed by following these steps:</span></span>

    1.  <span data-ttu-id="0309d-115">Ouvrez un navigateur Internet Explorer sur l’ordinateur hôte et entrez l’URL que vous avez supprimée de la liste de redirection.</span><span class="sxs-lookup"><span data-stu-id="0309d-115">Open an Internet Explorer browser in the host computer and enter the URL that you removed from the redirection list.</span></span>

    2.  <span data-ttu-id="0309d-116">Vérifiez que l’ouverture de la page Web s’ouvre dans Internet Explorer sur l’ordinateur hôte plutôt que sur l’ordinateur virtuel invité.</span><span class="sxs-lookup"><span data-stu-id="0309d-116">Verify that the webpage is opened in Internet Explorer on the host computer instead of on the guest virtual machine.</span></span>

        <span data-ttu-id="0309d-117">**Remarques**  Quelques secondes peuvent s’écouler avant que les modifications de redirection d’URL soient effectuées.</span><span class="sxs-lookup"><span data-stu-id="0309d-117">**Note** It can take several seconds for the URL redirection changes to take place.</span></span>

<span data-ttu-id="0309d-118">**Remarques**  Si vous rencontrez des problèmes lors de la vérification de vos paramètres de redirection d’URL, voir [résolution des problèmes d’opérations](operations-troubleshooting-medv2.md).</span><span class="sxs-lookup"><span data-stu-id="0309d-118">**Note** If you encounter any problems when verifying your URL redirection settings, see [Operations Troubleshooting](operations-troubleshooting-medv2.md).</span></span>

<span data-ttu-id="0309d-119">Lorsque vous avez terminé de tester la redirection d’URL dans votre espace de travail MED-V, vous pouvez tester d’autres configurations pour vérifier qu’elles fonctionnent comme prévu.</span><span class="sxs-lookup"><span data-stu-id="0309d-119">After you have completed testing URL redirection in your MED-V workspace, you can test other configurations to verify that they function as intended.</span></span>

<span data-ttu-id="0309d-120">Une fois que vous avez terminé de tester votre package d’espace de travail MED-V et que vous avez vérifié son fonctionnement, vous pouvez déployer l’espace de travail MED-V dans votre entreprise.</span><span class="sxs-lookup"><span data-stu-id="0309d-120">After you have completed testing your MED-V workspace package and have verified that it is functioning as intended, you can deploy the MED-V workspace to your enterprise.</span></span>

## <span data-ttu-id="0309d-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0309d-121">Related topics</span></span>

[<span data-ttu-id="0309d-122">Comment tester la publication d'applications</span><span class="sxs-lookup"><span data-stu-id="0309d-122">How to Test Application Publishing</span></span>](how-to-test-application-publishing.md)

[<span data-ttu-id="0309d-123">Comment vérifier les paramètres de première installation</span><span class="sxs-lookup"><span data-stu-id="0309d-123">How to Verify First Time Setup Settings</span></span>](how-to-verify-first-time-setup-settings.md)

[<span data-ttu-id="0309d-124">Déploiement du package d'espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="0309d-124">Deploying the MED-V Workspace Package</span></span>](deploying-the-med-v-workspace-package.md)

 

 





