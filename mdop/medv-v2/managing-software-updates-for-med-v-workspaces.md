---
title: Gestion des mises à jour de logiciels pour les espaces de travail MED-V
description: Gestion des mises à jour de logiciels pour les espaces de travail MED-V
author: dansimp
ms.assetid: a28d6dcd-cb9f-46ba-8dac-1d990837a3a3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 696238a2f5ad9b7e5120f75f6cd09d890d12519b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810781"
---
# <span data-ttu-id="b8061-103">Gestion des mises à jour de logiciels pour les espaces de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="b8061-103">Managing Software Updates for MED-V Workspaces</span></span>


<span data-ttu-id="b8061-104">Différentes options sont à votre disposition pour vous proposer des mises à jour logicielles pour les applications dans l’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="b8061-104">You have several different options available to you for providing software updates for the applications in the deployed MED-V workspace.</span></span>

<span data-ttu-id="b8061-105">**Remarques**  Pour plus d’informations sur la façon de spécifier les paramètres de configuration qui définissent la façon dont MED-V reçoit les mises à jour automatiques, voir [gestion des mises à jour automatiques pour les espaces de travail MED-v](managing-automatic-updates-for-med-v-workspaces.md).</span><span class="sxs-lookup"><span data-stu-id="b8061-105">**Note** For information about how to specify the configuration settings that define how MED-V receives automatic updates, see [Managing Automatic Updates for MED-V Workspaces](managing-automatic-updates-for-med-v-workspaces.md).</span></span>

 

**<span data-ttu-id="b8061-106">Mise à jour des logiciels dans un espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="b8061-106">Updating Software in a MED-V Workspace</span></span>**

1.  **<span data-ttu-id="b8061-107">Utilisation d’un système de distribution de logiciels électronique</span><span class="sxs-lookup"><span data-stu-id="b8061-107">Using an Electronic Software Distribution System</span></span>**

    <span data-ttu-id="b8061-108">Si votre organisation utilise un système de distribution de logiciels électroniques pour déployer le logiciel, vous pouvez l’utiliser pour fournir des mises à jour logicielles pour les applications sur les espaces de travail MED-V, de la même façon que vous fournissez des mises à jour pour les applications sur des ordinateurs physiques.</span><span class="sxs-lookup"><span data-stu-id="b8061-108">If your organization uses an Electronic Software Distribution System (ESD) system to deploy software, you can use it to provide software updates for applications on MED-V workspaces just as you provide updates for applications on physical computers.</span></span>

2.  **<span data-ttu-id="b8061-109">Utilisation d’une stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="b8061-109">Using Group Policy</span></span>**

    <span data-ttu-id="b8061-110">Si votre organisation déploie le logiciel à l’aide d’une stratégie de groupe, vous pouvez l’utiliser pour fournir des mises à jour logicielles pour les applications sur les espaces de travail MED-V, de la même façon que vous fournissez des mises à jour pour les applications sur des ordinateurs physiques.</span><span class="sxs-lookup"><span data-stu-id="b8061-110">If your organization deploys software by using Group Policy, you can use it to provide software updates for applications on MED-V workspaces just as you provide updates for applications on physical computers.</span></span>

3.  **<span data-ttu-id="b8061-111">Utilisation de la virtualisation des applications (APP-V)</span><span class="sxs-lookup"><span data-stu-id="b8061-111">Using Application Virtualization (APP-V)</span></span>**

    <span data-ttu-id="b8061-112">Si vous utilisez MED-V conjointement avec App-V, vous pouvez fournir des mises à jour logicielles aux applications dans l’espace de travail MED-V en suivant les étapes requises par App-V pour la mise à jour du logiciel.</span><span class="sxs-lookup"><span data-stu-id="b8061-112">If you use MED-V together with App-V, you can provide software updates to applications in the MED-V workspace by following the steps that are required by App-V for updating software.</span></span> <span data-ttu-id="b8061-113">Pour plus d’informations, voir [virtualisation des applications](https://go.microsoft.com/fwlink/?LinkId=122939) ( https://go.microsoft.com/fwlink/?LinkId=122939) .</span><span class="sxs-lookup"><span data-stu-id="b8061-113">For more information, see [Application Virtualization](https://go.microsoft.com/fwlink/?LinkId=122939) (https://go.microsoft.com/fwlink/?LinkId=122939).</span></span>

4.  **<span data-ttu-id="b8061-114">Mise à jour des logiciels dans l’image principale</span><span class="sxs-lookup"><span data-stu-id="b8061-114">Updating Software in the Core Image</span></span>**

    <span data-ttu-id="b8061-115">Même si vous n’avez pas envisagé de meilleures pratiques MED-V, vous pouvez installer des mises à jour logicielles sur des applications sur l’image principale.</span><span class="sxs-lookup"><span data-stu-id="b8061-115">Although not considered a MED-V best practice, you can install software updates to applications on the core image.</span></span> <span data-ttu-id="b8061-116">Après avoir installé les mises à jour, vous pouvez redéployer l’espace de travail MED-V vers votre entreprise tout comme vous l’avez déployé à l’origine.</span><span class="sxs-lookup"><span data-stu-id="b8061-116">After you have installed the updates, you can then redeploy the MED-V workspace back out to your enterprise just as you deployed it originally.</span></span>

    <span data-ttu-id="b8061-117">**Important**  Nous déconseillons cette méthode de gestion des mises à jour logicielles.</span><span class="sxs-lookup"><span data-stu-id="b8061-117">**Important** We do not recommend this method of managing software updates.</span></span> <span data-ttu-id="b8061-118">De plus, si vous effectuez la mise à jour du logiciel dans l’image principale et que vous redéployez l’espace de travail MED-V dans votre entreprise, la première fois que vous devez réexécuter le programme d’installation, les données enregistrées dans l’ordinateur virtuel sont perdues.</span><span class="sxs-lookup"><span data-stu-id="b8061-118">In addition, if you update software in the core image and redeploy the MED-V workspace back out to your enterprise, first time setup must run again, and any data saved in the virtual machine is lost.</span></span>

     

## <span data-ttu-id="b8061-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b8061-119">Related topics</span></span>


[<span data-ttu-id="b8061-120">Gestion des mises à jour automatiques pour les espaces de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="b8061-120">Managing Automatic Updates for MED-V Workspaces</span></span>](managing-automatic-updates-for-med-v-workspaces.md)

[<span data-ttu-id="b8061-121">Comment tester la publication d'applications</span><span class="sxs-lookup"><span data-stu-id="b8061-121">How to Test Application Publishing</span></span>](how-to-test-application-publishing.md)

[<span data-ttu-id="b8061-122">Comment publier et annuler la publication d'une application sur l'espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="b8061-122">How to Publish and Unpublish an Application on the MED-V Workspace</span></span>](how-to-publish-and-unpublish-an-application-on-the-med-v-workspace.md)

 

 





