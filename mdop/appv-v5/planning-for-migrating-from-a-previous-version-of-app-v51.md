---
title: Planification d'une migration à partir d'une version précédente d'App-V
description: Planification d'une migration à partir d'une version précédente d'App-V
author: dansimp
ms.assetid: 4a058047-9674-41bc-8050-c58c97a80a9b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: d7f2496b355aee6a598fee44c84e7e8c0f755c4f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804999"
---
# <span data-ttu-id="89369-103">Planification d'une migration à partir d'une version précédente d'App-V</span><span class="sxs-lookup"><span data-stu-id="89369-103">Planning for Migrating from a Previous Version of App-V</span></span>


<span data-ttu-id="89369-104">Utilisez les informations suivantes pour planifier la migration vers Microsoft Application Virtualization (App-V) 5,1 à partir de versions précédentes d’App-V.</span><span class="sxs-lookup"><span data-stu-id="89369-104">Use the following information to plan how to migrate to Microsoft Application Virtualization (App-V) 5.1 from previous versions of App-V.</span></span>

## <span data-ttu-id="89369-105">Exigences de migration</span><span class="sxs-lookup"><span data-stu-id="89369-105">Migration requirements</span></span>


<span data-ttu-id="89369-106">Avant de commencer une mise à niveau, consultez la configuration requise suivante:</span><span class="sxs-lookup"><span data-stu-id="89369-106">Before you start any upgrades, review the following requirements:</span></span>

-   <span data-ttu-id="89369-107">Si vous effectuez une mise à niveau à partir d’une version antérieure à celle du SP2 App-V 4,6, effectuez d’abord la mise à niveau vers la version App-v 4,6 SP3 avant de procéder à la mise à niveau vers App-V 5,1 ou une version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="89369-107">If you are upgrading from a version earlier than App-V 4.6 SP2, upgrade to version App-V 4.6 SP3 first before upgrading to App-V 5.1 or later.</span></span> <span data-ttu-id="89369-108">Dans ce scénario, mettez d’abord à niveau les clients App-V, puis mettez à niveau les composants serveur.</span><span class="sxs-lookup"><span data-stu-id="89369-108">In this scenario, upgrade the App-V clients first, and then upgrade the server components.</span></span>
<span data-ttu-id="89369-109">**Remarque:** App-V 4,6 a quitté le support technique standard.</span><span class="sxs-lookup"><span data-stu-id="89369-109">**Note:** App-V 4.6 has exited Mainstream support.</span></span>

-   <span data-ttu-id="89369-110">App-V 5,1 prend en charge uniquement les packages de création utilisant App-V 5,0 ou App-V 5,1 ou les packages qui ont été convertis au format **. AppV** .</span><span class="sxs-lookup"><span data-stu-id="89369-110">App-V 5.1 supports only packages that are created using App-V 5.0 or App-V 5.1, or packages that have been converted to the **.appv** format.</span></span>

-   <span data-ttu-id="89369-111">Si vous effectuez une mise à niveau de l’application-V Server vers App-V 5,0 SP1, voir [à propos de App-v 5,1](about-app-v-51.md#bkmk-migrate-to-51) pour obtenir des instructions.</span><span class="sxs-lookup"><span data-stu-id="89369-111">If you are upgrading the App-V Server from App-V 5.0 SP1, see [About App-V 5.1](about-app-v-51.md#bkmk-migrate-to-51) for instructions.</span></span>

## <span data-ttu-id="89369-112">Exécution simultanée du client App-V 5,1 avec App-V 4,6</span><span class="sxs-lookup"><span data-stu-id="89369-112">Running the App-V 5.1 client concurrently with App-V 4.6</span></span>


<span data-ttu-id="89369-113">Vous pouvez exécuter le client App-V 5,1 simultanément sur le même ordinateur que le client App-V 4.6 SP3.</span><span class="sxs-lookup"><span data-stu-id="89369-113">You can run the App-V 5.1 client concurrently on the same computer with the App-V4.6SP3 client.</span></span>

<span data-ttu-id="89369-114">Lorsque vous exécutez le coexistence de clients App-V, vous pouvez:</span><span class="sxs-lookup"><span data-stu-id="89369-114">When you run coexisting App-V clients, you can:</span></span>

-   <span data-ttu-id="89369-115">Convertissez un package App-V 4,6 SP3 au format App-V 5,1 et publiez les deux packages lorsque les deux clients s’exécutent.</span><span class="sxs-lookup"><span data-stu-id="89369-115">Convert an App-V 4.6 SP3 package to the App-V 5.1 format and publish both packages, when you have both clients running.</span></span>

-   <span data-ttu-id="89369-116">Définissez la stratégie de migration pour le package converti, qui permet au package App-V 5,1 converti de supposer les associations de types de fichiers et les raccourcis du package App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="89369-116">Define the migration policy for the converted package, which allows the converted App-V 5.1 package to assume the file type associations and shortcuts from the App-V 4.6 package.</span></span>

### <span data-ttu-id="89369-117">Scénarios de coexistence pris en charge</span><span class="sxs-lookup"><span data-stu-id="89369-117">Supported coexistence scenarios</span></span>

<span data-ttu-id="89369-118">Le tableau suivant répertorie les scénarios de coexistence App-V pris en charge.</span><span class="sxs-lookup"><span data-stu-id="89369-118">The following table shows the supported App-V coexistence scenarios.</span></span> <span data-ttu-id="89369-119">Nous vous recommandons d’installer les dernières mises à jour disponibles d’une version donnée lorsque vous exécutez un client coexistant.</span><span class="sxs-lookup"><span data-stu-id="89369-119">We recommend that you install the latest available updates of a given release when you are running coexisting clients.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="89369-120">Type de client App-V 4,6</span><span class="sxs-lookup"><span data-stu-id="89369-120">App-V 4.6 client type</span></span></th>
<th align="left"><span data-ttu-id="89369-121">Type de client App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="89369-121">App-V 5.1 client type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="89369-122">App-V 4,6 SP3</span><span class="sxs-lookup"><span data-stu-id="89369-122">App-V 4.6 SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="89369-123">App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="89369-123">App-V 5.1</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="89369-124">App-V 4,6 SP3 RDS</span><span class="sxs-lookup"><span data-stu-id="89369-124">App-V 4.6 SP3 RDS</span></span></p></td>
<td align="left"><p><span data-ttu-id="89369-125">App-V 5,1 RDS</span><span class="sxs-lookup"><span data-stu-id="89369-125">App-V 5.1 RDS</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="89369-126">Configuration requise pour l’utilisation de clients coexistant</span><span class="sxs-lookup"><span data-stu-id="89369-126">Requirements for running coexisting clients</span></span>

<span data-ttu-id="89369-127">Pour exécuter des clients coexistants, vous devez:</span><span class="sxs-lookup"><span data-stu-id="89369-127">To run coexisting clients, you must:</span></span>

-   <span data-ttu-id="89369-128">Installez le client App-V 4.6 avant d’installer le client App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="89369-128">Install the App-V4.6 client before you install the App-V 5.1 client.</span></span>

-   <span data-ttu-id="89369-129">Activez le paramètre Activer la stratégie de groupe du **mode migration** , qui se trouve dans le nœud de coexistence du client **App-V** &gt; **Client Coexistence** .</span><span class="sxs-lookup"><span data-stu-id="89369-129">Enable the **Enable Migration Mode** Group Policy setting, which is in the **App-V** &gt; **Client Coexistence** node.</span></span> <span data-ttu-id="89369-130">Pour déployer le modèle. admx, voir [Comment télécharger et déployer des modèles de stratégie de groupe MDOP (. admx)](https://technet.microsoft.com/library/dn659707.aspx).</span><span class="sxs-lookup"><span data-stu-id="89369-130">To deploy the .admx template, see [How to Download and Deploy MDOP Group Policy (.admx) Templates](https://technet.microsoft.com/library/dn659707.aspx).</span></span>

<span data-ttu-id="89369-131">**Remarques**  Les packages App-V 5,1 peuvent s’exécuter côte à côte avec les packages App-V 4,6 Si vous disposez d’installations coexistantes d’App-V 5,1 et 4,6.</span><span class="sxs-lookup"><span data-stu-id="89369-131">**Note** App-V 5.1 packages can run side by side with App-V 4.6 packages if you have coexisting installations of App-V 5.1 and 4.6.</span></span> <span data-ttu-id="89369-132">Toutefois, les packages App-V 5,1 ne peuvent pas interagir avec les packages App-V 4,6 dans le même environnement virtuel.</span><span class="sxs-lookup"><span data-stu-id="89369-132">However, App-V 5.1 packages cannot interact with App-V 4.6 packages in the same virtual environment.</span></span>

 

### <span data-ttu-id="89369-133">Téléchargements et documentation du client</span><span class="sxs-lookup"><span data-stu-id="89369-133">Client downloads and documentation</span></span>

<span data-ttu-id="89369-134">Le tableau suivant fournit des liens vers les téléchargements de clients App-V 4,6 et la documentation TechNet sur les versions.</span><span class="sxs-lookup"><span data-stu-id="89369-134">The following table provides links to the App-V 4.6 client downloads and to the TechNet documentation about the releases.</span></span> <span data-ttu-id="89369-135">Les téléchargements incluent les clients application-V «Regular» et RDS.</span><span class="sxs-lookup"><span data-stu-id="89369-135">The downloads include the App-V “regular” and RDS clients.</span></span> <span data-ttu-id="89369-136">La documentation TechNet relative au client App-V s’applique aux deux clients, sauf indication contraire.</span><span class="sxs-lookup"><span data-stu-id="89369-136">The TechNet documentation about the App-V client applies to both clients, unless stated otherwise.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="89369-137">Version App-V</span><span class="sxs-lookup"><span data-stu-id="89369-137">App-V version</span></span></th>
<th align="left"><span data-ttu-id="89369-138">Lien vers la documentation TechNet</span><span class="sxs-lookup"><span data-stu-id="89369-138">Link to TechNet documentation</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="89369-139">App-V 4.6 SP3</span><span class="sxs-lookup"><span data-stu-id="89369-139">App-V 4.6SP3</span></span></p></td>
<td align="left"><p><a href="https://technet.microsoft.com/library/dn511019.aspx" data-raw-source="[About Microsoft Application Virtualization 4.6 SP3](https://technet.microsoft.com/library/dn511019.aspx)"><span data-ttu-id="89369-140">À propos de Microsoft Application Virtualization4.6 SP3</span><span class="sxs-lookup"><span data-stu-id="89369-140">About Microsoft Application Virtualization 4.6 SP3</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="89369-141">App-V 4.6 SP3</span><span class="sxs-lookup"><span data-stu-id="89369-141">App-V 4.6SP3</span></span></p></td>
<td align="left"><p><a href="about-app-v-51.md" data-raw-source="[About Microsoft Application Virtualization 5.1](about-app-v-51.md)"><span data-ttu-id="89369-142">À propos de Microsoft Application Virtualization 5,1</span><span class="sxs-lookup"><span data-stu-id="89369-142">About Microsoft Application Virtualization 5.1</span></span></a></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="89369-143">Pour plus d’informations sur la configuration de la coexistence du client App-V 5,1, voir:</span><span class="sxs-lookup"><span data-stu-id="89369-143">For more information about how to configure App-V 5.1 client coexistence, see:</span></span>

-   [<span data-ttu-id="89369-144">Déploiement de l’application-V 4,6 et du client App-V 5,1 sur le même ordinateur</span><span class="sxs-lookup"><span data-stu-id="89369-144">How to Deploy the App-V 4.6 and the App-V 5.1 Client on the Same Computer</span></span>](how-to-deploy-the-app-v-46-and-the-app-v--51-client-on-the-same-computer.md)

-   [<span data-ttu-id="89369-145">Coexistence et migration avec App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="89369-145">App-V 5.0 Coexistence and Migration</span></span>](https://technet.microsoft.com/windows/jj835811.aspx)

## <a href="" id="converting--previous-version--packages-using-the-package-converter-"></a><span data-ttu-id="89369-146">Conversion de packages «Previous-version» à l’aide du convertisseur de package</span><span class="sxs-lookup"><span data-stu-id="89369-146">Converting “previous-version” packages using the package converter</span></span>


<span data-ttu-id="89369-147">Avant de migrer un package créé à l’aide de App-4,6 SP2 ou version antérieure vers App-V 5,1, consultez la configuration requise suivante:</span><span class="sxs-lookup"><span data-stu-id="89369-147">Before migrating a package, created using App-4.6SP2 or earlier, to App-V 5.1, review the following requirements:</span></span>

-   <span data-ttu-id="89369-148">Vous devez convertir le package au format de fichier **. AppV** .</span><span class="sxs-lookup"><span data-stu-id="89369-148">You must convert the package to the **.appv** file format.</span></span>

-   <span data-ttu-id="89369-149">Le convertisseur de package prend uniquement en charge la conversion directe des packages qui ont été créés à l’aide de App-V 4,5 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="89369-149">The Package Converter supports only the direct conversion of packages that were created by using App-V 4.5 and later.</span></span> <span data-ttu-id="89369-150">Pour utiliser le convertisseur de package sur un package qui a été créé à l’aide d’une version antérieure, vous devez utiliser une application-V 4.5 ou version ultérieure du Sequencer pour mettre à niveau le package, puis vous pouvez effectuer la conversion du package.</span><span class="sxs-lookup"><span data-stu-id="89369-150">To use the package converter on a package that was created using a previous version, you must use an App-V4.5 or later version of the sequencer to upgrade the package, and then you can perform the package conversion.</span></span>

<span data-ttu-id="89369-151">Pour plus d’informations sur l’utilisation du convertisseur de package pour convertir un package, voir [Comment convertir un package créé dans une version antérieure d’App-V](how-to-convert-a-package-created-in-a-previous-version-of-app-v51.md).</span><span class="sxs-lookup"><span data-stu-id="89369-151">For more information about using the package converter to convert a package, see [How to Convert a Package Created in a Previous Version of App-V](how-to-convert-a-package-created-in-a-previous-version-of-app-v51.md).</span></span> <span data-ttu-id="89369-152">Après avoir converti le fichier, vous pouvez le déployer sur des ordinateurs cibles qui exécutent le client App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="89369-152">After you convert the file, you can deploy it to target computers that run the App-V 5.1 client.</span></span>






## <span data-ttu-id="89369-153">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="89369-153">Related topics</span></span>


[<span data-ttu-id="89369-154">Envisager de déployer App-V</span><span class="sxs-lookup"><span data-stu-id="89369-154">Planning to Deploy App-V</span></span>](planning-to-deploy-app-v51.md)

 

 





