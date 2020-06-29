---
title: Migration à partir d'une version précédente
description: Migration à partir d'une version précédente
author: dansimp
ms.assetid: a13cd353-b22a-48f7-af1e-5d54ede2a7e5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a05bbd498cdb77a1ddf694b1aab6aeb42124775b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805065"
---
# <span data-ttu-id="8d7a4-103">Migration à partir d'une version précédente</span><span class="sxs-lookup"><span data-stu-id="8d7a4-103">Migrating from a Previous Version</span></span>


<span data-ttu-id="8d7a4-104">Avec App-V 5,0, vous pouvez migrer votre infrastructure App-V 4,6 existante vers une infrastructure plus flexible, intégrée et plus facile à 5,0 gérer.</span><span class="sxs-lookup"><span data-stu-id="8d7a4-104">With App-V 5.0 you can migrate your existing App-V 4.6 infrastructure to the more flexible, integrated, and easier to manage App-V 5.0 infrastructure.</span></span>

<span data-ttu-id="8d7a4-105">Tenez compte des sections suivantes lors de la planification de votre stratégie de migration:</span><span class="sxs-lookup"><span data-stu-id="8d7a4-105">Consider the following sections when you plan your migration strategy:</span></span>

<span data-ttu-id="8d7a4-106">**Remarques**  Pour plus d’informations sur les différences entre App-V 4,6 et App-V 5,0, voir **différences entre les sections App-v 4,6 et App-v 5,0** de l' [application-v 5,0](about-app-v-50.md).</span><span class="sxs-lookup"><span data-stu-id="8d7a4-106">**Note** For more information about the differences between App-V 4.6 and App-V 5.0, see the **Differences between App-V 4.6 and App-V 5.0 section** of [About App-V 5.0](about-app-v-50.md).</span></span>

 

## <span data-ttu-id="8d7a4-107">Conversion de packages créés à l’aide d’une version antérieure d’App-V</span><span class="sxs-lookup"><span data-stu-id="8d7a4-107">Converting packages created using a prior version of App-V</span></span>


<span data-ttu-id="8d7a4-108">Utilisez l’utilitaire convertisseur de package pour mettre à niveau des packages d’applications virtuelles créés à l’aide de versions précédentes d’App-V.</span><span class="sxs-lookup"><span data-stu-id="8d7a4-108">Use the package converter utility to upgrade virtual application packages created using previous versions of App-V.</span></span> <span data-ttu-id="8d7a4-109">Le convertisseur de package utilise PowerShell pour convertir des packages et peut faciliter l’automatisation du processus si vous avez de nombreux packages qui nécessitent une conversion.</span><span class="sxs-lookup"><span data-stu-id="8d7a4-109">The package converter uses PowerShell to convert packages and can help automate the process if you have many packages that require conversion.</span></span>

<span data-ttu-id="8d7a4-110">**Important**  Après avoir converti un package existant, vous devez tester le package avant de déployer le package pour vérifier que le processus de conversion a abouti.</span><span class="sxs-lookup"><span data-stu-id="8d7a4-110">**Important** After you convert an existing package you should test the package prior to deploying the package to ensure the conversion process was successful.</span></span>

 

**<span data-ttu-id="8d7a4-111">Ce que vous devez savoir avant de convertir des packages existants</span><span class="sxs-lookup"><span data-stu-id="8d7a4-111">What to know before you convert existing packages</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8d7a4-112">Problème</span><span class="sxs-lookup"><span data-stu-id="8d7a4-112">Issue</span></span></th>
<th align="left"><span data-ttu-id="8d7a4-113">Solution de contournement</span><span class="sxs-lookup"><span data-stu-id="8d7a4-113">Workaround</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8d7a4-114">Les scripts de package ne sont pas convertis.</span><span class="sxs-lookup"><span data-stu-id="8d7a4-114">Package scripts are not converted.</span></span></p></td>
<td align="left"><p><span data-ttu-id="8d7a4-115">Testez le package converti.</span><span class="sxs-lookup"><span data-stu-id="8d7a4-115">Test the converted package.</span></span> <span data-ttu-id="8d7a4-116">Le cas échéant, convertissez le script.</span><span class="sxs-lookup"><span data-stu-id="8d7a4-116">If necessary convert the script.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8d7a4-117">Les substitutions de paramètre de registre de package ne sont pas converties.</span><span class="sxs-lookup"><span data-stu-id="8d7a4-117">Package registry setting overrides are not converted.</span></span></p></td>
<td align="left"><p><span data-ttu-id="8d7a4-118">Testez le package converti.</span><span class="sxs-lookup"><span data-stu-id="8d7a4-118">Test the converted package.</span></span> <span data-ttu-id="8d7a4-119">Le cas échéant, rajoutez les remplacements du Registre.</span><span class="sxs-lookup"><span data-stu-id="8d7a4-119">If necessary, re-add registry overrides.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8d7a4-120">Les packages virtuels utilisant DSC ne sont pas liés après la conversion.</span><span class="sxs-lookup"><span data-stu-id="8d7a4-120">Virtual packages using DSC are not linked after conversion.</span></span></p></td>
<td align="left"><p><span data-ttu-id="8d7a4-121">Liez les packages à l’aide de groupes de connexion.</span><span class="sxs-lookup"><span data-stu-id="8d7a4-121">Link the packages using connection groups.</span></span> <span data-ttu-id="8d7a4-122">Voir <a href="managing-connection-groups.md" data-raw-source="[Managing Connection Groups](managing-connection-groups.md)"> gestion des groupes de connexion </a> .</span><span class="sxs-lookup"><span data-stu-id="8d7a4-122">See <a href="managing-connection-groups.md" data-raw-source="[Managing Connection Groups](managing-connection-groups.md)">Managing Connection Groups</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8d7a4-123">Des conflits de variables d’environnement sont détectés lors de la conversion.</span><span class="sxs-lookup"><span data-stu-id="8d7a4-123">Environment variable conflicts are detected during conversion.</span></span></p></td>
<td align="left"><p><span data-ttu-id="8d7a4-124">Résoudre les conflits dans le <strong> fichier. OSD associé </strong> .</span><span class="sxs-lookup"><span data-stu-id="8d7a4-124">Resolve any conflicts in the associated <strong>.osd</strong> file.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8d7a4-125">Les chemins d’accès codés en dur sont détectés lors de la conversion.</span><span class="sxs-lookup"><span data-stu-id="8d7a4-125">Hard-coded paths are detected during conversion.</span></span></p></td>
<td align="left"><p><span data-ttu-id="8d7a4-126">Les chemins d’accès codés en dur sont difficiles à convertir correctement.</span><span class="sxs-lookup"><span data-stu-id="8d7a4-126">Hard-coded paths are difficult to convert correctly.</span></span> <span data-ttu-id="8d7a4-127">Le convertisseur de package détectera et renverra des packages avec des fichiers contenant des chemins d’accès codés en dur.</span><span class="sxs-lookup"><span data-stu-id="8d7a4-127">The package converter will detect and return packages with files that contain hard-coded paths.</span></span> <span data-ttu-id="8d7a4-128">Affichez le fichier avec le chemin codé en dur et déterminez s’il nécessite le fichier.</span><span class="sxs-lookup"><span data-stu-id="8d7a4-128">View the file with the hard-coded path, and determine whether the package requires the file.</span></span> <span data-ttu-id="8d7a4-129">Si tel est le cas, nous vous recommandons de réorganiser le package.</span><span class="sxs-lookup"><span data-stu-id="8d7a4-129">If so, it is recommended to re-sequence the package.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="8d7a4-130">Lors de la conversion d’un package Vérifiez l’absence de raccourcis vers les fichiers ou les raccourcis.</span><span class="sxs-lookup"><span data-stu-id="8d7a4-130">When converting a package check for failing files or shortcuts.</span></span> <span data-ttu-id="8d7a4-131">Recherchez l’élément dans le package App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="8d7a4-131">Locate the item in App-V 4.6 package.</span></span> <span data-ttu-id="8d7a4-132">Il peut s’agir d’un chemin d’accès codé en dur.</span><span class="sxs-lookup"><span data-stu-id="8d7a4-132">It could possibly be hard-coded path.</span></span> <span data-ttu-id="8d7a4-133">Convertissez le chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="8d7a4-133">Convert the path.</span></span>

<span data-ttu-id="8d7a4-134">**Remarques**  Nous vous recommandons d’utiliser le Sequencer App-V 5,0 pour convertir des applications ou applications critiques qui doivent tirer parti de fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="8d7a4-134">**Note** It is recommended that you use the App-V 5.0 sequencer for converting critical applications or applications that need to take advantage of features.</span></span> <span data-ttu-id="8d7a4-135">Pour plus d' [informations sur la façon de séquencer une nouvelle application avec App-V 5,0](how-to-sequence-a-new-application-with-app-v-50-beta-gb18030.md), voir.</span><span class="sxs-lookup"><span data-stu-id="8d7a4-135">See, [How to Sequence a New Application with App-V 5.0](how-to-sequence-a-new-application-with-app-v-50-beta-gb18030.md).</span></span>

<span data-ttu-id="8d7a4-136">Si un package converti ne s’ouvre pas après l’avoir converti, il est également recommandé de réorganiser l’application à l’aide du séquenceur App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="8d7a4-136">If a converted package does not open after you convert it, it is also recommended that you re-sequence the application using the App-V 5.0 sequencer.</span></span>

 

[<span data-ttu-id="8d7a4-137">Comment convertir un package créé dans une version précédente d'App-V</span><span class="sxs-lookup"><span data-stu-id="8d7a4-137">How to Convert a Package Created in a Previous Version of App-V</span></span>](how-to-convert-a-package-created-in-a-previous-version-of-app-v.md)

## <span data-ttu-id="8d7a4-138">Migration des clients</span><span class="sxs-lookup"><span data-stu-id="8d7a4-138">Migrating Clients</span></span>


<span data-ttu-id="8d7a4-139">Le tableau suivant présente la méthode recommandée pour la mise à niveau des clients.</span><span class="sxs-lookup"><span data-stu-id="8d7a4-139">The following table displays the recommended method for upgrading clients.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8d7a4-140">Tâche</span><span class="sxs-lookup"><span data-stu-id="8d7a4-140">Task</span></span></th>
<th align="left"><span data-ttu-id="8d7a4-141">Plus d’informations</span><span class="sxs-lookup"><span data-stu-id="8d7a4-141">More Information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8d7a4-142">Mettre à niveau votre environnement vers App-V 4.6 SP2</span><span class="sxs-lookup"><span data-stu-id="8d7a4-142">Upgrade your environment to App-V4.6SP2</span></span></p></td>
<td align="left"><p><a href="../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md" data-raw-source="[Application Virtualization Deployment and Upgrade Considerations](../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md)"><span data-ttu-id="8d7a4-143">Considérations en matière de déploiement et de mise à niveau de la virtualisation des applications </a> .</span><span class="sxs-lookup"><span data-stu-id="8d7a4-143">Application Virtualization Deployment and Upgrade Considerations</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8d7a4-144">Installez le client App-V 5,0 avec la coexistence activée.</span><span class="sxs-lookup"><span data-stu-id="8d7a4-144">Install the App-V 5.0 client with co-existence enabled.</span></span></p></td>
<td align="left"><p><a href="how-to-deploy-the-app-v-46-and-the-app-v--50-client-on-the-same-computer.md" data-raw-source="[How to Deploy the App-V 4.6 and the App-V 5.0 Client on the Same Computer](how-to-deploy-the-app-v-46-and-the-app-v--50-client-on-the-same-computer.md)"><span data-ttu-id="8d7a4-145">Déploiement de l’application-V 4,6 et du client App-V 5,0 sur le même ordinateur </a> .</span><span class="sxs-lookup"><span data-stu-id="8d7a4-145">How to Deploy the App-V 4.6 and the App-V 5.0 Client on the Same Computer</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8d7a4-146">Séquence et déploiement des packages App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="8d7a4-146">Sequence and roll out App-V 5.0 packages.</span></span> <span data-ttu-id="8d7a4-147">Le cas échéant, annulez la publication des packages App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="8d7a4-147">As needed, unpublish App-V 4.6 packages.</span></span></p></td>
<td align="left"><p><a href="how-to-sequence-a-new-application-with-app-v-50-beta-gb18030.md" data-raw-source="[How to Sequence a New Application with App-V 5.0](how-to-sequence-a-new-application-with-app-v-50-beta-gb18030.md)"><span data-ttu-id="8d7a4-148">Comment séquencer une nouvelle application avec App-V 5,0 </a> .</span><span class="sxs-lookup"><span data-stu-id="8d7a4-148">How to Sequence a New Application with App-V 5.0</a>.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="8d7a4-149">**Important**  Vous devez exécuter App-V 4.6 SP3 pour utiliser le mode de coexistence.</span><span class="sxs-lookup"><span data-stu-id="8d7a4-149">**Important** You must be running App-V4.6SP3 to use coexistence mode.</span></span> <span data-ttu-id="8d7a4-150">Par ailleurs, lorsque vous séquencez un package, vous devez configurer le paramètre administration de l’autorité, qui se trouve dans la **Configuration utilisateur** , dans la section Configuration de l' **utilisateur** .</span><span class="sxs-lookup"><span data-stu-id="8d7a4-150">Additionally, when you sequence a package, you must configure the Managing Authority setting, which is in the **User Configuration** is located in the **User Configuration** section.</span></span>

 

## <span data-ttu-id="8d7a4-151">Migration de l’infrastructure complète de l’application-V 5,0 Server</span><span class="sxs-lookup"><span data-stu-id="8d7a4-151">Migrating the App-V 5.0 Server Full Infrastructure</span></span>


<span data-ttu-id="8d7a4-152">Il n’existe aucune méthode directe pour effectuer une mise à niveau vers une infrastructure App-V 5,0 complète.</span><span class="sxs-lookup"><span data-stu-id="8d7a4-152">There is no direct method to upgrade to a full App-V 5.0 infrastructure.</span></span> <span data-ttu-id="8d7a4-153">Pour plus d’informations sur la mise à niveau de l’application-V Server, utilisez les informations de la section suivante.</span><span class="sxs-lookup"><span data-stu-id="8d7a4-153">Use the information in the following section for information about upgrading the App-V server.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8d7a4-154">Tâche</span><span class="sxs-lookup"><span data-stu-id="8d7a4-154">Task</span></span></th>
<th align="left"><span data-ttu-id="8d7a4-155">Plus d’informations</span><span class="sxs-lookup"><span data-stu-id="8d7a4-155">More Information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8d7a4-156">Mettez à niveau votre environnement vers App-V 4.6 SP3.</span><span class="sxs-lookup"><span data-stu-id="8d7a4-156">Upgrade your environment to App-V4.6SP3.</span></span></p></td>
<td align="left"><p><a href="../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md" data-raw-source="[Application Virtualization Deployment and Upgrade Considerations](../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md)"><span data-ttu-id="8d7a4-157">Considérations en matière de déploiement et de mise à niveau de la virtualisation des applications </a> .</span><span class="sxs-lookup"><span data-stu-id="8d7a4-157">Application Virtualization Deployment and Upgrade Considerations</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8d7a4-158">Déploiement de la version 5,0 App-V du client.</span><span class="sxs-lookup"><span data-stu-id="8d7a4-158">Deploy App-V 5.0 version of the client.</span></span></p></td>
<td align="left"><p><a href="how-to-deploy-the-app-v-client-gb18030.md" data-raw-source="[How to Deploy the App-V Client](how-to-deploy-the-app-v-client-gb18030.md)"><span data-ttu-id="8d7a4-159">Déploiement du client App-V </a> .</span><span class="sxs-lookup"><span data-stu-id="8d7a4-159">How to Deploy the App-V Client</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8d7a4-160">Installez App-V 5,0 Server.</span><span class="sxs-lookup"><span data-stu-id="8d7a4-160">Install App-V 5.0 server.</span></span></p></td>
<td align="left"><p><a href="how-to-deploy-the-app-v-50-server-50sp3.md" data-raw-source="[How to Deploy the App-V 5.0 Server](how-to-deploy-the-app-v-50-server-50sp3.md)"><span data-ttu-id="8d7a4-161">Déploiement du serveur App-V 5,0 </a> .</span><span class="sxs-lookup"><span data-stu-id="8d7a4-161">How to Deploy the App-V 5.0 Server</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8d7a4-162">Migrer des packages existants.</span><span class="sxs-lookup"><span data-stu-id="8d7a4-162">Migrate existing packages.</span></span></p></td>
<td align="left"><p><span data-ttu-id="8d7a4-163">Voir les <strong> packages de conversion créés à l’aide d’une version antérieure de la section App-V </strong> de cet article.</span><span class="sxs-lookup"><span data-stu-id="8d7a4-163">See the <strong>Converting packages created using a prior version of App-V</strong> section of this article.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="8d7a4-164">Tâches de migration supplémentaires</span><span class="sxs-lookup"><span data-stu-id="8d7a4-164">Additional Migration tasks</span></span>


<span data-ttu-id="8d7a4-165">Vous pouvez également effectuer d’autres tâches de migration telles que la reconfiguration des points de terminaison et l’ouverture d’un package créé à l’aide d’une version antérieure sur un ordinateur exécutant le client App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="8d7a4-165">You can also perform additional migration tasks such as reconfiguring end points as well as opening a package created using a prior version on a computer running the App-V 5.0 client.</span></span> <span data-ttu-id="8d7a4-166">Les liens suivants fournissent des informations supplémentaires sur l’exécution de ces tâches.</span><span class="sxs-lookup"><span data-stu-id="8d7a4-166">The following links provide more information about performing these tasks.</span></span>

[<span data-ttu-id="8d7a4-167">Migration de points d'extension d'un package App-V4.6 vers un package App-V5.0 converti pour tous les utilisateurs sur un ordinateur spécifique</span><span class="sxs-lookup"><span data-stu-id="8d7a4-167">How to Migrate Extension Points From an App-V 4.6 Package to a Converted App-V 5.0 Package for All Users on a Specific Computer</span></span>](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-50-package-for-all-users-on-a-specific-computer.md)

[<span data-ttu-id="8d7a4-168">Migration de points d'extension d'un package App-V4.6 vers un package App-V5.0 pour un utilisateur spécifique</span><span class="sxs-lookup"><span data-stu-id="8d7a4-168">How to Migrate Extension Points From an App-V 4.6 Package to App-V 5.0 for a Specific User</span></span>](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-50-for-a-specific-user.md)

[<span data-ttu-id="8d7a4-169">Restauration de points d'extension d'un package App-V5.0 vers un package App-V4.6 pour tous les utilisateurs sur un ordinateur spécifique</span><span class="sxs-lookup"><span data-stu-id="8d7a4-169">How to Revert Extension Points from an App-V 5.0 Package to an App-V 4.6 Package For All Users on a Specific Computer</span></span>](how-to-revert-extension-points-from-an-app-v-50-package-to-an-app-v-46-package-for-all-users-on-a-specific-computer.md)

[<span data-ttu-id="8d7a4-170">Restauration de points d'extension d'un package App-V5.0 vers un package App-V4.6 pour un utilisateur spécifique</span><span class="sxs-lookup"><span data-stu-id="8d7a4-170">How to Revert Extension Points From an App-V 5.0 Package to an App-V 4.6 Package for a Specific User</span></span>](how-to-revert-extension-points-from-an-app-v-50-package-to-an-app-v-46-package-for-a-specific-user.md)







## <span data-ttu-id="8d7a4-171">Autres ressources pour effectuer des tâches de migration d’application-V</span><span class="sxs-lookup"><span data-stu-id="8d7a4-171">Other resources for performing App-V migration tasks</span></span>


[<span data-ttu-id="8d7a4-172">Opérations d'App-V5.0</span><span class="sxs-lookup"><span data-stu-id="8d7a4-172">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

[<span data-ttu-id="8d7a4-173">Procédure de mise à niveau du serveur de gestion Microsoft App-V 5,1 simplifiée</span><span class="sxs-lookup"><span data-stu-id="8d7a4-173">A simplified Microsoft App-V 5.1 Management Server upgrade procedure</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=786330)

 

 





