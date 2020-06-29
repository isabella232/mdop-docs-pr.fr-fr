---
title: Copie des modèles de stratégie de groupe MBAM2.5
description: Copie des modèles de stratégie de groupe MBAM2.5
author: dansimp
ms.assetid: e526ecec-07ff-435e-bc90-3084b617b84b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/28/2017
ms.openlocfilehash: a3436552256b1632a11037dc94751207cde89d5c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811027"
---
# <span data-ttu-id="3cfa3-103">Copie des modèles de stratégie de groupe MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="3cfa3-103">Copying the MBAM 2.5 Group Policy Templates</span></span>


<span data-ttu-id="3cfa3-104">Avant de déployer l’installation du client MBAM, vous devez télécharger les modèles de stratégie de groupe MBAM qui contiennent des paramètres de stratégie de groupe définissant les paramètres d’implémentation MBAM pour le chiffrement de lecteur BitLocker.</span><span class="sxs-lookup"><span data-stu-id="3cfa3-104">Before deploying the MBAM Client installation, you must download the MBAM Group Policy Templates, which contain Group Policy settings that define MBAM implementation settings for BitLocker Drive Encryption.</span></span> <span data-ttu-id="3cfa3-105">Après avoir téléchargé les modèles, vous définissez les paramètres de stratégie de groupe à implémenter au sein de votre entreprise.</span><span class="sxs-lookup"><span data-stu-id="3cfa3-105">After downloading the templates, you then set the Group Policy settings to implement across your enterprise.</span></span>

## <span data-ttu-id="3cfa3-106">Télécharger et déployer les modèles de stratégie de groupe MDOP</span><span class="sxs-lookup"><span data-stu-id="3cfa3-106">Downloading and deploying the MDOP Group Policy templates</span></span>


<span data-ttu-id="3cfa3-107">Les modèles de stratégie de groupe MDOP peuvent être téléchargés dans un fichier auto-extractible, compressé, groupé par technologie et version.</span><span class="sxs-lookup"><span data-stu-id="3cfa3-107">MDOP Group Policy templates are available for download in a self-extracting, compressed file, grouped by technology and version.</span></span>

**<span data-ttu-id="3cfa3-108">Télécharger et déployer les modèles de stratégie de groupe MDOP</span><span class="sxs-lookup"><span data-stu-id="3cfa3-108">How to download and deploy the MDOP Group Policy templates</span></span>**

1. <span data-ttu-id="3cfa3-109">Téléchargez les modèles de stratégie de groupe MDOP à partir des [modèles d’administration de la stratégie de groupe Microsoft Desktop Optimization](https://www.microsoft.com/download/details.aspx?id=55531).</span><span class="sxs-lookup"><span data-stu-id="3cfa3-109">Download the MDOP Group Policy templates from [Microsoft Desktop Optimization Pack Group Policy Administrative Templates](https://www.microsoft.com/download/details.aspx?id=55531).</span></span>

2. <span data-ttu-id="3cfa3-110">Exécutez le fichier téléchargé pour extraire les dossiers du modèle.</span><span class="sxs-lookup"><span data-stu-id="3cfa3-110">Run the downloaded file to extract the template folders.</span></span>

   **<span data-ttu-id="3cfa3-111">Warning</span><span class="sxs-lookup"><span data-stu-id="3cfa3-111">Warning</span></span>**  
   <span data-ttu-id="3cfa3-112">Ne récupérez pas les modèles directement dans le répertoire de déploiement de la stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="3cfa3-112">Do not extract the templates directly to the Group Policy deployment directory.</span></span> <span data-ttu-id="3cfa3-113">Plusieurs technologies et versions sont regroupées dans ce fichier.</span><span class="sxs-lookup"><span data-stu-id="3cfa3-113">Multiple technologies and versions are bundled in this file.</span></span>



3. <span data-ttu-id="3cfa3-114">Dans le dossier extraits, recherchez le fichier Technology-version. admx.</span><span class="sxs-lookup"><span data-stu-id="3cfa3-114">In the extracted folder, locate the technology-version .admx file.</span></span> <span data-ttu-id="3cfa3-115">Certaines technologies MDOP disposent de plusieurs ensembles d’objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="3cfa3-115">Certain MDOP technologies have multiple sets of Group Policy Objects (GPOs).</span></span> <span data-ttu-id="3cfa3-116">Par exemple, MBAM inclut des paramètres de gestion MBAM et des paramètres utilisateur MBAM.</span><span class="sxs-lookup"><span data-stu-id="3cfa3-116">For example, MBAM includes MBAM Management settings and MBAM User settings.</span></span>

4. <span data-ttu-id="3cfa3-117">Recherchez le fichier. adml approprié par language-culture ( *c’est-à-dire, en* anglais-États-Unis).</span><span class="sxs-lookup"><span data-stu-id="3cfa3-117">Locate the appropriate .adml file by language-culture (that is, *en* for English-United States).</span></span>

5. <span data-ttu-id="3cfa3-118">Copiez les fichiers. admx et. adml dans un dossier de définition de stratégie.</span><span class="sxs-lookup"><span data-stu-id="3cfa3-118">Copy the .admx and .adml files to a policy definition folder.</span></span> <span data-ttu-id="3cfa3-119">En fonction de l’emplacement de stockage des modèles, vous pouvez configurer les paramètres de stratégie de groupe à partir de l’appareil local ou à partir de n’importe quel ordinateur du domaine.</span><span class="sxs-lookup"><span data-stu-id="3cfa3-119">Depending on where you store the templates, you can configure Group Policy settings from the local device or from any computer on the domain.</span></span>

   **<span data-ttu-id="3cfa3-120">Fichiers locaux.</span><span class="sxs-lookup"><span data-stu-id="3cfa3-120">Local files.</span></span>** <span data-ttu-id="3cfa3-121">Pour configurer les paramètres de stratégie de groupe à partir de l’appareil local, copiez les fichiers de modèles aux emplacements suivants:</span><span class="sxs-lookup"><span data-stu-id="3cfa3-121">To configure Group Policy settings from the local device, copy template files to the following locations:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="3cfa3-122">Type de fichier</span><span class="sxs-lookup"><span data-stu-id="3cfa3-122">File type</span></span></th>
   <th align="left"><span data-ttu-id="3cfa3-123">Emplacement du fichier</span><span class="sxs-lookup"><span data-stu-id="3cfa3-123">File location</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="3cfa3-124">Modèle de stratégie de groupe (. admx)</span><span class="sxs-lookup"><span data-stu-id="3cfa3-124">Group Policy template (.admx)</span></span></p></td>
   <td align="left"><p><code>%systemroot%</code><span data-ttu-id="3cfa3-125">&lt;forte &gt; PolicyDefinitions</span><span class="sxs-lookup"><span data-stu-id="3cfa3-125">&lt;strong&gt;policyDefinitions</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="3cfa3-126">Fichier de langue de la stratégie de groupe (. adml)</span><span class="sxs-lookup"><span data-stu-id="3cfa3-126">Group Policy language file (.adml)</span></span></p></td>
   <td align="left"><p><code>%systemroot%</code><span data-ttu-id="3cfa3-127">&lt;forte &gt; PolicyDefinitions</span><span class="sxs-lookup"><span data-stu-id="3cfa3-127">&lt;strong&gt;policyDefinitions</span></span></strong><code>[MUIculture]</code></p></td>
   </tr>
   </tbody>
   </table>



~~~
**Domain central store.** To enable Group Policy settings configuration by a Group Policy administrator from any computer on the domain, copy files to the following locations on the domain controller:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">File type</th>
<th align="left">File location</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Group Policy template (.admx)</p></td>
<td align="left"><p><code>%systemroot%</code>\<strong>sysvol\domain\policies\PolicyDefinitions</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>Group Policy language file (.adml)</p></td>
<td align="left"><p><code>%systemroot%</code>\<strong>sysvol\domain\policies\PolicyDefinitions\[MUIculture]</strong><code>\[MUIculture]</code></p>
<p>For example, the U.S. English ADML language-specific file will be stored in %systemroot%\sysvol\domain\policies\PolicyDefinitions\en-us.</p></td>
</tr>
</tbody>
</table>
~~~



6. <span data-ttu-id="3cfa3-128">Modifiez les paramètres de stratégie de groupe à l’aide de la console de gestion des stratégies de groupe (GPMC) ou de la gestion de la stratégie de groupe avancée (AGPM) pour configurer les paramètres de stratégie de groupe pour la technologie MDOP.</span><span class="sxs-lookup"><span data-stu-id="3cfa3-128">Edit the Group Policy settings using Group Policy Management Console (GPMC) or Advanced Group Policy Management (AGPM) to configure Group Policy settings for the MDOP technology.</span></span> <span data-ttu-id="3cfa3-129">Pour plus d’informations, reportez-vous à [modification des paramètres de stratégie de groupe MBAM 2,5](editing-the-mbam-25-group-policy-settings.md) .</span><span class="sxs-lookup"><span data-stu-id="3cfa3-129">See [Editing the MBAM 2.5 Group Policy Settings](editing-the-mbam-25-group-policy-settings.md) for more information.</span></span>

   <span data-ttu-id="3cfa3-130">Pour obtenir une description des paramètres de stratégie de groupe, reportez-vous [à la planification des exigences de stratégie de groupe MBAM 2,5](planning-for-mbam-25-group-policy-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="3cfa3-130">For descriptions of the Group Policy settings, see [Planning for MBAM 2.5 Group Policy Requirements](planning-for-mbam-25-group-policy-requirements.md).</span></span>


## <span data-ttu-id="3cfa3-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3cfa3-131">Related topics</span></span>


[<span data-ttu-id="3cfa3-132">Déploiement d'objets de stratégie de groupe MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="3cfa3-132">Deploying MBAM 2.5 Group Policy Objects</span></span>](deploying-mbam-25-group-policy-objects.md)


## <span data-ttu-id="3cfa3-133">Vous avez une suggestion pour MBAM?</span><span class="sxs-lookup"><span data-stu-id="3cfa3-133">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="3cfa3-134">Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)</span><span class="sxs-lookup"><span data-stu-id="3cfa3-134">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="3cfa3-135">Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="3cfa3-135">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>






