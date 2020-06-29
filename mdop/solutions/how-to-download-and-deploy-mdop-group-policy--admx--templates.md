---
title: Téléchargement et déploiement des modèles de stratégie de groupe MDOP (.admx)
description: Téléchargement et déploiement des modèles de stratégie de groupe MDOP (.admx)
author: dansimp
ms.assetid: fdb64505-6c66-4fdf-ad74-a6a161191e3f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/15/2018
ms.openlocfilehash: 5bc5f8d536c113ccbc0a1931e6c7e4ed3c7a9a37
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812042"
---
# <span data-ttu-id="8ba8f-103">Téléchargement et déploiement des modèles de stratégie de groupe MDOP (.admx)</span><span class="sxs-lookup"><span data-stu-id="8ba8f-103">How to Download and Deploy MDOP Group Policy (.admx) Templates</span></span>


<span data-ttu-id="8ba8f-104">Vous pouvez gérer les paramètres de fonctionnalité de certaines technologies du pack d’optimisation du bureau Microsoft (par exemple, app-v, UE-V ou MBAM) à l’aide de modèles de stratégie de groupe, fichiers. admx et. adml.</span><span class="sxs-lookup"><span data-stu-id="8ba8f-104">You can manage the feature settings of certain Microsoft Desktop Optimization Pack (MDOP) technologies (for example, App-V, UE-V, or MBAM) by using Group Policy templates, the .admx and .adml files.</span></span> <span data-ttu-id="8ba8f-105">Les modèles de stratégie de groupe MDOP peuvent être téléchargés dans un fichier auto-extractible, compressé, groupé par technologie et version.</span><span class="sxs-lookup"><span data-stu-id="8ba8f-105">MDOP Group Policy templates are available for download in a self-extracting, compressed file, grouped by technology and version.</span></span>

## <span data-ttu-id="8ba8f-106">Modèles de stratégie de groupe MDOP</span><span class="sxs-lookup"><span data-stu-id="8ba8f-106">MDOP Group Policy templates</span></span>

**<span data-ttu-id="8ba8f-107">Télécharger et déployer les modèles de stratégie de groupe MDOP</span><span class="sxs-lookup"><span data-stu-id="8ba8f-107">How to download and deploy the MDOP Group Policy templates</span></span>**

1. <span data-ttu-id="8ba8f-108">Télécharger les derniers [modèles de stratégie de groupe MDOP](https://www.microsoft.com/download/details.aspx?id=55531)</span><span class="sxs-lookup"><span data-stu-id="8ba8f-108">Download the latest [MDOP Group Policy templates](https://www.microsoft.com/download/details.aspx?id=55531)</span></span> 

2. <span data-ttu-id="8ba8f-109">Développez le fichier téléchargé. cab en exécutant</span><span class="sxs-lookup"><span data-stu-id="8ba8f-109">Expand the downloaded .cab file by running</span></span> `expand <download_folder>\MDOP_ADMX_Templates.cab -F:* <destination_folder>`

   **<span data-ttu-id="8ba8f-110">Warning</span><span class="sxs-lookup"><span data-stu-id="8ba8f-110">Warning</span></span>**  
   <span data-ttu-id="8ba8f-111">Ne récupérez pas les modèles directement dans le répertoire de déploiement de la stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="8ba8f-111">Do not extract the templates directly to the Group Policy deployment directory.</span></span> <span data-ttu-id="8ba8f-112">Plusieurs technologies et versions sont regroupées dans ce fichier.</span><span class="sxs-lookup"><span data-stu-id="8ba8f-112">Multiple technologies and versions are bundled in this file.</span></span>

3. <span data-ttu-id="8ba8f-113">Dans le dossier extraits, recherchez le fichier Technology-version. admx.</span><span class="sxs-lookup"><span data-stu-id="8ba8f-113">In the extracted folder, locate the technology-version .admx file.</span></span> <span data-ttu-id="8ba8f-114">Certaines technologies MDOP disposent de plusieurs ensembles d’objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="8ba8f-114">Certain MDOP technologies have multiple sets of Group Policy Objects (GPOs).</span></span> <span data-ttu-id="8ba8f-115">Par exemple, MBAM inclut des paramètres de gestion MBAM et des paramètres utilisateur MBAM.</span><span class="sxs-lookup"><span data-stu-id="8ba8f-115">For example, MBAM includes MBAM Management settings and MBAM User settings.</span></span>

4. <span data-ttu-id="8ba8f-116">Recherchez le fichier. adml approprié par language-culture (c’est-à-dire, en *-US* pour English-France).</span><span class="sxs-lookup"><span data-stu-id="8ba8f-116">Locate the appropriate .adml file by language-culture (that is, *en-us* for English-United States).</span></span>

5. <span data-ttu-id="8ba8f-117">Copiez les fichiers. admx et. adml dans un dossier de définition de stratégie.</span><span class="sxs-lookup"><span data-stu-id="8ba8f-117">Copy the .admx and .adml files to a policy definition folder.</span></span> <span data-ttu-id="8ba8f-118">En fonction de l’emplacement de stockage des modèles, vous pouvez configurer les paramètres de stratégie de groupe à partir de l’appareil local ou à partir de n’importe quel ordinateur du domaine.</span><span class="sxs-lookup"><span data-stu-id="8ba8f-118">Depending on where you store the templates, you can configure Group Policy settings from the local device or from any computer on the domain.</span></span>

   - <span data-ttu-id="8ba8f-119">**Fichiers locaux:** Pour configurer les paramètres de stratégie de groupe à partir de l’appareil local, copiez les fichiers de modèles aux emplacements suivants:</span><span class="sxs-lookup"><span data-stu-id="8ba8f-119">**Local files:** To configure Group Policy settings from the local device, copy template files to the following locations:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="8ba8f-120">Type de fichier</span><span class="sxs-lookup"><span data-stu-id="8ba8f-120">File type</span></span></th>
   <th align="left"><span data-ttu-id="8ba8f-121">Emplacement du fichier</span><span class="sxs-lookup"><span data-stu-id="8ba8f-121">File location</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="8ba8f-122">Modèle de stratégie de groupe (. admx)</span><span class="sxs-lookup"><span data-stu-id="8ba8f-122">Group Policy template (.admx)</span></span></p></td>
   <td align="left"><p><code>%systemroot%</code><span data-ttu-id="8ba8f-123">&lt;forte &gt; PolicyDefinitions</span><span class="sxs-lookup"><span data-stu-id="8ba8f-123">&lt;strong&gt;policyDefinitions</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="8ba8f-124">Fichier de langue de la stratégie de groupe (. adml)</span><span class="sxs-lookup"><span data-stu-id="8ba8f-124">Group Policy language file (.adml)</span></span></p></td>
   <td align="left"><p><code>%systemroot%</code><span data-ttu-id="8ba8f-125">&lt;forte &gt; PolicyDefinitions</span><span class="sxs-lookup"><span data-stu-id="8ba8f-125">&lt;strong&gt;policyDefinitions</span></span></strong><code>[MUIculture]</code></p></td>
   </tr>
   </tbody>
   </table>

   - <span data-ttu-id="8ba8f-126">**Magasin central du domaine:** Pour activer la configuration des paramètres de stratégie de groupe par un administrateur de stratégie de groupe à partir de n’importe quel ordinateur du domaine, copiez les fichiers aux emplacements suivants sur le contrôleur de domaine:</span><span class="sxs-lookup"><span data-stu-id="8ba8f-126">**Domain central store:** To enable Group Policy settings configuration by a Group Policy administrator from any computer on the domain, copy files to the following locations on the domain controller:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="8ba8f-127">Type de fichier</span><span class="sxs-lookup"><span data-stu-id="8ba8f-127">File type</span></span></th>
   <th align="left"><span data-ttu-id="8ba8f-128">Emplacement du fichier</span><span class="sxs-lookup"><span data-stu-id="8ba8f-128">File location</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="8ba8f-129">Modèle de stratégie de groupe (. admx)</span><span class="sxs-lookup"><span data-stu-id="8ba8f-129">Group Policy template (.admx)</span></span></p></td>
   <td align="left"><p><code>%systemroot%</code><span data-ttu-id="8ba8f-130">&lt;forte &gt; sysvol\domain\policies\PolicyDefinitions</span><span class="sxs-lookup"><span data-stu-id="8ba8f-130">&lt;strong&gt;sysvol\domain\policies\PolicyDefinitions</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="8ba8f-131">Fichier de langue de la stratégie de groupe (. adml)</span><span class="sxs-lookup"><span data-stu-id="8ba8f-131">Group Policy language file (.adml)</span></span></p></td>
   <td align="left"><p><code>%systemroot%</code><span data-ttu-id="8ba8f-132">&lt;forte &gt; sysvol\domain\policies\PolicyDefinitions [MUIculture]</span><span class="sxs-lookup"><span data-stu-id="8ba8f-132">&lt;strong&gt;sysvol\domain\policies\PolicyDefinitions[MUIculture]</span></span></strong><code>[MUIculture]</code></p>
   <p><span data-ttu-id="8ba8f-133">Par exemple, le fichier propre à la langue de l’anglais (États-Unis) est stocké dans%systemroot%\sysvol\domain\policies\PolicyDefinitions\en-us.</span><span class="sxs-lookup"><span data-stu-id="8ba8f-133">For example, the U.S. English ADML language-specific file will be stored in %systemroot%\sysvol\domain\policies\PolicyDefinitions\en-us.</span></span></p></td>
   </tr>
   </tbody>
   </table>

6. <span data-ttu-id="8ba8f-134">Modifiez les paramètres de stratégie de groupe à l’aide de la console de gestion des stratégies de groupe (GPMC) ou de la gestion de la stratégie de groupe avancée (AGPM) pour configurer les paramètres de stratégie de groupe pour la technologie MDOP.</span><span class="sxs-lookup"><span data-stu-id="8ba8f-134">Edit the Group Policy settings using Group Policy Management Console (GPMC) or Advanced Group Policy Management (AGPM) to configure Group Policy settings for the MDOP technology.</span></span>

### <span data-ttu-id="8ba8f-135">Stratégie de groupe MDOP par technologie</span><span class="sxs-lookup"><span data-stu-id="8ba8f-135">MDOP Group Policy by technology</span></span>

<span data-ttu-id="8ba8f-136">Pour plus d’informations sur les stratégies de groupe MDOP prises en charge, voir la documentation spécifique de la technologie.</span><span class="sxs-lookup"><span data-stu-id="8ba8f-136">For more information about supported MDOP Group Policy, see the specific documentation for the technology.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8ba8f-137">Technologie MDOP</span><span class="sxs-lookup"><span data-stu-id="8ba8f-137">MDOP Technology</span></span></th>
<th align="left"><span data-ttu-id="8ba8f-138">Ensembles de versions</span><span class="sxs-lookup"><span data-stu-id="8ba8f-138">Version bundles</span></span></th>
<th align="left"><span data-ttu-id="8ba8f-139">Remarques</span><span class="sxs-lookup"><span data-stu-id="8ba8f-139">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="8ba8f-140">Application Virtualization (App-V)</span><span class="sxs-lookup"><span data-stu-id="8ba8f-140">Application Virtualization (App-V)</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="8ba8f-141">Service packs App-V 5,0 et App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="8ba8f-141">App-V 5.0 and App-V 5.0 Service Packs</span></span></p></td>
<td align="left"><p><a href="../appv-v5/how-to-modify-app-v-50-client-configuration-using-the-admx-template-and-group-policy.md" data-raw-source="[How to Modify App-V 5.0 Client Configuration Using the ADMX Template and Group Policy](../appv-v5/how-to-modify-app-v-50-client-configuration-using-the-admx-template-and-group-policy.md)"><span data-ttu-id="8ba8f-142">Modification de la configuration d'App-V5.0 Client à l'aide du modèle ADMX et d'une stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="8ba8f-142">How to Modify App-V 5.0 Client Configuration Using the ADMX Template and Group Policy</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="8ba8f-143">User Experience Virtualization (UE-V)</span><span class="sxs-lookup"><span data-stu-id="8ba8f-143">User Experience Virtualization (UE-V)</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="8ba8f-144">UE-V 2,0 et UE-V 2,1</span><span class="sxs-lookup"><span data-stu-id="8ba8f-144">UE-V 2.0 and UE-V 2.1</span></span></p></td>
<td align="left"><p><a href="../uev-v2/configuring-ue-v-2x-with-group-policy-objects-both-uevv2.md" data-raw-source="[Configuring UE-V 2.x with Group Policy Objects](../uev-v2/configuring-ue-v-2x-with-group-policy-objects-both-uevv2.md)"><span data-ttu-id="8ba8f-145">Configuration d’UE-V 2. x avec des objets de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="8ba8f-145">Configuring UE-V 2.x with Group Policy Objects</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="8ba8f-146">UE-V 1,0, y compris 1,0 SP1</span><span class="sxs-lookup"><span data-stu-id="8ba8f-146">UE-V 1.0 including 1.0 SP1</span></span></p></td>
<td align="left"><p><a href="../uev-v1/configuring-ue-v-with-group-policy-objects.md" data-raw-source="[Configuring UE-V with Group Policy Objects](../uev-v1/configuring-ue-v-with-group-policy-objects.md)"><span data-ttu-id="8ba8f-147">Configuration d’UE-V avec les objets de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="8ba8f-147">Configuring UE-V with Group Policy Objects</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="8ba8f-148">Microsoft BitLocker Administration and Monitoring (MBAM)</span><span class="sxs-lookup"><span data-stu-id="8ba8f-148">Microsoft BitLocker Administration and Monitoring (MBAM)</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="8ba8f-149">MBAM 2,5</span><span class="sxs-lookup"><span data-stu-id="8ba8f-149">MBAM 2.5</span></span></p></td>
<td align="left"><p><a href="../mbam-v25/planning-for-mbam-25-group-policy-requirements.md" data-raw-source="[Planning for MBAM 2.5 Group Policy Requirements](../mbam-v25/planning-for-mbam-25-group-policy-requirements.md)"><span data-ttu-id="8ba8f-150">Planification des exigences en matière de stratégie de groupe MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="8ba8f-150">Planning for MBAM 2.5 Group Policy Requirements</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="8ba8f-151">MBAM 2,0, y compris 2,0 SP1</span><span class="sxs-lookup"><span data-stu-id="8ba8f-151">MBAM 2.0 including 2.0 SP1</span></span></p></td>
<td align="left"><p><a href="../mbam-v2/planning-for-mbam-20-group-policy-requirements-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Group Policy Requirements](../mbam-v2/planning-for-mbam-20-group-policy-requirements-mbam-2.md)"><span data-ttu-id="8ba8f-152">Planification des exigences en matière de stratégie de groupe MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="8ba8f-152">Planning for MBAM 2.0 Group Policy Requirements</span></span></a></p>
<p><a href="../mbam-v2/deploying-mbam-20-group-policy-objects-mbam-2.md" data-raw-source="[Deploying MBAM 2.0 Group Policy Objects](../mbam-v2/deploying-mbam-20-group-policy-objects-mbam-2.md)"><span data-ttu-id="8ba8f-153">Déploiement d'objets de stratégie de groupe MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="8ba8f-153">Deploying MBAM 2.0 Group Policy Objects</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="8ba8f-154">MBAM 1,0</span><span class="sxs-lookup"><span data-stu-id="8ba8f-154">MBAM 1.0</span></span></p></td>
<td align="left"><p><a href="../mbam-v1/how-to-edit-mbam-10-gpo-settings.md" data-raw-source="[How to Edit MBAM 1.0 GPO Settings](../mbam-v1/how-to-edit-mbam-10-gpo-settings.md)"><span data-ttu-id="8ba8f-155">Procédure de modification des paramètres d'objet de stratégie de groupe MBAM1.0</span><span class="sxs-lookup"><span data-stu-id="8ba8f-155">How to Edit MBAM 1.0 GPO Settings</span></span></a></p></td>
</tr>
</tbody>
</table>

 

 

 





