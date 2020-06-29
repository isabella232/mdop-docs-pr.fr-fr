---
title: À propos du fichier de groupe de connexion
description: À propos du fichier de groupe de connexion
author: dansimp
ms.assetid: bfeb6013-a7ca-4e36-9fe3-229702e83f0d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5e5cb93326ce182d71de0f0f89cc569823d6154e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806097"
---
# <span data-ttu-id="65a68-103">À propos du fichier de groupe de connexion</span><span class="sxs-lookup"><span data-stu-id="65a68-103">About the Connection Group File</span></span>


**<span data-ttu-id="65a68-104">Contenu de cet article:</span><span class="sxs-lookup"><span data-stu-id="65a68-104">In this topic:</span></span>**

-   [<span data-ttu-id="65a68-105">Objectif et emplacement du fichier de groupe de connexion</span><span class="sxs-lookup"><span data-stu-id="65a68-105">Connection group file purpose and location</span></span>](#bkmk-cg-purpose-loc)

-   [<span data-ttu-id="65a68-106">Structure du fichier XML de groupe de connexion</span><span class="sxs-lookup"><span data-stu-id="65a68-106">Structure of the connection group XML file</span></span>](#bkmk-define-cg-5-0sp3)

-   [<span data-ttu-id="65a68-107">Configuration de la priorité des packages dans un groupe de connexion</span><span class="sxs-lookup"><span data-stu-id="65a68-107">Configuring the priority of packages in a connection group</span></span>](#bkmk-config-pkg-priority-incg)

-   [<span data-ttu-id="65a68-108">Configurations de connexion d’applications virtuelles prises en charge</span><span class="sxs-lookup"><span data-stu-id="65a68-108">Supported virtual application connection configurations</span></span>](#bkmk-va-conn-configs)

## <a href="" id="bkmk-cg-purpose-loc"></a><span data-ttu-id="65a68-109">Objectif et emplacement du fichier de groupe de connexion</span><span class="sxs-lookup"><span data-stu-id="65a68-109">Connection group file purpose and location</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="65a68-110">Fonction de groupe de connexion</span><span class="sxs-lookup"><span data-stu-id="65a68-110">Connection group purpose</span></span></p></td>
<td align="left"><p><span data-ttu-id="65a68-111">Un groupe de connexions est une fonctionnalité App-V qui vous permet de regrouper les packages pour créer un environnement virtuel dans lequel les applications de ces packages peuvent interagir entre elles.</span><span class="sxs-lookup"><span data-stu-id="65a68-111">A connection group is an App-V feature that enables you to group packages together to create a virtual environment in which the applications in those packages can interact with each other.</span></span></p>
<p><span data-ttu-id="65a68-112">Par exemple: vous voulez utiliser les plug-ins avec Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="65a68-112">Example: You want to use plug-ins with Microsoft Office.</span></span> <span data-ttu-id="65a68-113">Vous pouvez créer un package qui contient les plug-ins et créer un autre package contenant Office, puis ajouter ces deux packages à un groupe de connexion pour permettre à Office d’utiliser ces plug-ins.</span><span class="sxs-lookup"><span data-stu-id="65a68-113">You can create a package that contains the plug-ins, and create another package that contains Office, and then add both packages to a connection group to enable Office to use those plug-ins.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="65a68-114">Fonctionnement du fichier de groupe de connexion</span><span class="sxs-lookup"><span data-stu-id="65a68-114">How the connection group file works</span></span></p></td>
<td align="left"><p><span data-ttu-id="65a68-115">Lorsque vous appliquez un fichier de groupe de connexion à une application de virtualisation d’application 5,0, les packages énumérés dans le fichier seront combinés au moment de l’exécution dans un environnement virtuel unique.</span><span class="sxs-lookup"><span data-stu-id="65a68-115">When you apply an Application Virtualization 5.0 connection group file, the packages that are enumerated in the file will be combined at runtime into a single virtual environment.</span></span> <span data-ttu-id="65a68-116">Utilisez le fichier de groupe de connexion à l’application Microsoft Application Virtualization (App-V) 5,0 pour configurer les groupes de connexion 5,0 existants de la virtualisation des applications.</span><span class="sxs-lookup"><span data-stu-id="65a68-116">Use the Microsoft Application Virtualization (App-V) 5.0 connection group file to configure existing Application Virtualization 5.0 connection groups.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="65a68-117">Exemple de chemin d’accès au fichier</span><span class="sxs-lookup"><span data-stu-id="65a68-117">Example file path</span></span></p></td>
<td align="left"><p><span data-ttu-id="65a68-118">%APPDATA%\Microsoft\AppV\Client\Catalog\PackageGroups {6CCC7575-162E-4152-9407-ED411DA138F4} {4D1E16E1-8EF8-41ED-92D5-8910A8527F96}.</span><span class="sxs-lookup"><span data-stu-id="65a68-118">%APPDATA%\Microsoft\AppV\Client\Catalog\PackageGroups{6CCC7575-162E-4152-9407-ED411DA138F4}{4D1E16E1-8EF8-41ED-92D5-8910A8527F96}.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-define-cg-5-0sp3"></a><span data-ttu-id="65a68-119">Structure du fichier XML de groupe de connexion</span><span class="sxs-lookup"><span data-stu-id="65a68-119">Structure of the connection group XML file</span></span>


**<span data-ttu-id="65a68-120">Dans cette section:</span><span class="sxs-lookup"><span data-stu-id="65a68-120">In this section:</span></span>**

-   [<span data-ttu-id="65a68-121">Paramètres définissant le groupe de connexions</span><span class="sxs-lookup"><span data-stu-id="65a68-121">Parameters that define the connection group</span></span>](#bkmk-params-define-cg)

-   [<span data-ttu-id="65a68-122">Paramètres définissant les packages dans le groupe de connexion</span><span class="sxs-lookup"><span data-stu-id="65a68-122">Parameters that define the packages in the connection group</span></span>](#bkmk-params-define-pkgs-incg)

-   [<span data-ttu-id="65a68-123">Exemple de fichier XML de groupe de connexion App-V 5,0 SP3</span><span class="sxs-lookup"><span data-stu-id="65a68-123">App-V 5.0 SP3 example connection group XML file</span></span>](#bkmk-50sp3-exp-cg-xml)

-   [<span data-ttu-id="65a68-124">App-V 5,0 via App-V 5,0 SP2-exemple de fichier XML de connexion</span><span class="sxs-lookup"><span data-stu-id="65a68-124">App-V 5.0 through App-V 5.0 SP2 example connection group XML file</span></span>](#bkmk-50thru50sp2-exp-cg-xm)

### <a href="" id="bkmk-params-define-cg"></a><span data-ttu-id="65a68-125">Paramètres définissant le groupe de connexions</span><span class="sxs-lookup"><span data-stu-id="65a68-125">Parameters that define the connection group</span></span>

<span data-ttu-id="65a68-126">Le tableau suivant décrit les paramètres du fichier XML qui définissent le groupe de connexions lui-même, et non les packages.</span><span class="sxs-lookup"><span data-stu-id="65a68-126">The following table describes the parameters in the XML file that define the connection group itself, not the packages.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="65a68-127">Champ</span><span class="sxs-lookup"><span data-stu-id="65a68-127">Field</span></span></th>
<th align="left"><span data-ttu-id="65a68-128">Description</span><span class="sxs-lookup"><span data-stu-id="65a68-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="65a68-129">Nom du schéma</span><span class="sxs-lookup"><span data-stu-id="65a68-129">Schema name</span></span></p></td>
<td align="left"><p><span data-ttu-id="65a68-130">Nom du schéma.</span><span class="sxs-lookup"><span data-stu-id="65a68-130">Name of the schema.</span></span></p>
<p><strong><span data-ttu-id="65a68-131">Applicable à partir de l’App-V 5,0 SP3 </strong> : Si vous voulez utiliser les nouvelles fonctionnalités «packages facultatifs» et «utiliser les versions» décrites dans ce tableau, vous devez spécifier le schéma suivant dans le fichier XML:</span><span class="sxs-lookup"><span data-stu-id="65a68-131">Applicable starting in App-V 5.0 SP3</strong>: If you want to use the new “optional packages” and “use any version” features that are described in this table, you must specify the following schema in the XML file:</span></span></p>
<p><code>xmlns=&quot;<a href="https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup&amp;quot" data-raw-source="https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup&amp;quot">https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup&quot</a>;</code></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="65a68-132">AppConnectionGroupId</span><span class="sxs-lookup"><span data-stu-id="65a68-132">AppConnectionGroupId</span></span></p></td>
<td align="left"><p><span data-ttu-id="65a68-133">Identificateur GUID unique pour ce groupe de connexion.</span><span class="sxs-lookup"><span data-stu-id="65a68-133">Unique GUID identifier for this connection group.</span></span> <span data-ttu-id="65a68-134">L’état du groupe de connexions est associé à cet identificateur.</span><span class="sxs-lookup"><span data-stu-id="65a68-134">The connection group state is associated with this identifier.</span></span> <span data-ttu-id="65a68-135">Spécifiez cet identificateur uniquement lors de la création du groupe de connexions.</span><span class="sxs-lookup"><span data-stu-id="65a68-135">Specify this identifier only when you create the connection group.</span></span></p>
<p><span data-ttu-id="65a68-136">Vous pouvez créer un nouveau GUID en tapant: <strong>[Guid]::NewGuid()</strong> .</span><span class="sxs-lookup"><span data-stu-id="65a68-136">You can create a new GUID by typing: <strong>[Guid]::NewGuid()</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="65a68-137">VersionId</span><span class="sxs-lookup"><span data-stu-id="65a68-137">VersionId</span></span></p></td>
<td align="left"><p><span data-ttu-id="65a68-138">Identificateur du GUID de version de cette version du groupe de connexion.</span><span class="sxs-lookup"><span data-stu-id="65a68-138">Version GUID identifier for this version of the connection group.</span></span></p>
<p><span data-ttu-id="65a68-139">Lorsque vous mettez à jour un groupe de connexion (par exemple, en ajoutant ou en mettant à jour un nouveau package), vous devez mettre à jour le GUID de la version pour refléter la nouvelle version.</span><span class="sxs-lookup"><span data-stu-id="65a68-139">When you update a connection group (for example, by adding or updating a new package), you must update the version GUID to reflect the new version.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="65a68-140">DisplayName</span><span class="sxs-lookup"><span data-stu-id="65a68-140">DisplayName</span></span></p></td>
<td align="left"><p><span data-ttu-id="65a68-141">Nom d’affichage du groupe de connexions.</span><span class="sxs-lookup"><span data-stu-id="65a68-141">Display name of the connection group.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="65a68-142">Priority</span><span class="sxs-lookup"><span data-stu-id="65a68-142">Priority</span></span></p></td>
<td align="left"><p><span data-ttu-id="65a68-143">Champ prioritaire facultatif pour le groupe de connexions.</span><span class="sxs-lookup"><span data-stu-id="65a68-143">Optional priority field for the connection group.</span></span></p>
<p><strong><span data-ttu-id="65a68-144">"0" </strong> - indique la priorité la plus élevée.</span><span class="sxs-lookup"><span data-stu-id="65a68-144">“0”</strong> - indicates the highest priority.</span></span></p>
<p><span data-ttu-id="65a68-145">Si une priorité est requise, mais qu’elle n’a pas été configurée, le package échouera, car le groupe de connexion approprié à utiliser ne peut pas être déterminé.</span><span class="sxs-lookup"><span data-stu-id="65a68-145">If a priority is required, but has not been configured, the package will fail because the correct connection group to use cannot be determined.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="bkmk-params-define-pkgs-incg"></a><span data-ttu-id="65a68-146">Paramètres définissant les packages dans le groupe de connexion</span><span class="sxs-lookup"><span data-stu-id="65a68-146">Parameters that define the packages in the connection group</span></span>

<span data-ttu-id="65a68-147">Dans la &lt; &gt; section packages du fichier XML de groupe de connexion, vous répertoriez les packages de membres dans le groupe de connexions en spécifiant l’identificateur de package et l’identificateur de version uniques de chaque package, comme décrit dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="65a68-147">In the &lt;Packages&gt; section of the connection group XML file, you list the member packages in the connection group by specifying each package’s unique package identifier and version identifier, as described in the following table.</span></span> <span data-ttu-id="65a68-148">Le premier package de la liste a la priorité la plus élevée.</span><span class="sxs-lookup"><span data-stu-id="65a68-148">The first package in the list has the highest precedence.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="65a68-149">Champ</span><span class="sxs-lookup"><span data-stu-id="65a68-149">Field</span></span></th>
<th align="left"><span data-ttu-id="65a68-150">Description</span><span class="sxs-lookup"><span data-stu-id="65a68-150">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="65a68-151">PackageId</span><span class="sxs-lookup"><span data-stu-id="65a68-151">PackageId</span></span></p></td>
<td align="left"><p><span data-ttu-id="65a68-152">Identificateur GUID unique pour ce package.</span><span class="sxs-lookup"><span data-stu-id="65a68-152">Unique GUID identifier for this package.</span></span> <span data-ttu-id="65a68-153">Ce GUID ne change pas lors de la publication de versions plus récentes du package.</span><span class="sxs-lookup"><span data-stu-id="65a68-153">This GUID doesn’t change when newer versions of the package are published.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="65a68-154">VersionId</span><span class="sxs-lookup"><span data-stu-id="65a68-154">VersionId</span></span></p></td>
<td align="left"><p><span data-ttu-id="65a68-155">Identificateur GUID unique pour la version du package.</span><span class="sxs-lookup"><span data-stu-id="65a68-155">Unique GUID identifier for the version of the package.</span></span></p>
<p><strong><span data-ttu-id="65a68-156">Applicable à partir de l’App-V 5,0 SP3 </strong> : Si vous spécifiez <strong> «\*» </strong> pour la version du package, le GUID de la dernière version du package disponible est inséré dynamiquement.</span><span class="sxs-lookup"><span data-stu-id="65a68-156">Applicable starting in App-V 5.0 SP3</strong>: If you specify <strong>“\*”</strong> for the package version, the GUID of the latest available package version is dynamically inserted.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="65a68-157">IsOptional</span><span class="sxs-lookup"><span data-stu-id="65a68-157">IsOptional</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="65a68-158">Applicable à partir du paramètre App-V 5,0 SP3 </strong> : qui vous permet de rendre un package facultatif dans le groupe de connexions.</span><span class="sxs-lookup"><span data-stu-id="65a68-158">Applicable starting in App-V 5.0 SP3</strong>: Parameter that enables you to make a package optional within the connection group.</span></span> <span data-ttu-id="65a68-159">Les entrées valides sont les suivantes:</span><span class="sxs-lookup"><span data-stu-id="65a68-159">Valid entries are:</span></span></p>
<ul>
<li><p><strong><span data-ttu-id="65a68-160">"vrai" </strong> : le package est facultatif dans le groupe de connexions</span><span class="sxs-lookup"><span data-stu-id="65a68-160">“true”</strong> – package is optional in the connection group</span></span></p></li>
<li><p><strong><span data-ttu-id="65a68-161">"false" </strong> – le package est requis dans le groupe de connexion</span><span class="sxs-lookup"><span data-stu-id="65a68-161">“false”</strong> – package is required in the connection group</span></span></p></li>
</ul>
<p><span data-ttu-id="65a68-162">Découvrez <a href="how-to-use-optional-packages-in-connection-groups.md" data-raw-source="[How to Use Optional Packages in Connection Groups](how-to-use-optional-packages-in-connection-groups.md)"> comment utiliser les packages facultatifs dans les groupes de connexion </a> .</span><span class="sxs-lookup"><span data-stu-id="65a68-162">See <a href="how-to-use-optional-packages-in-connection-groups.md" data-raw-source="[How to Use Optional Packages in Connection Groups](how-to-use-optional-packages-in-connection-groups.md)">How to Use Optional Packages in Connection Groups</a>.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="bkmk-50sp3-exp-cg-xml"></a><span data-ttu-id="65a68-163">Exemple de fichier XML de groupe de connexion App-V 5,0 SP3</span><span class="sxs-lookup"><span data-stu-id="65a68-163">App-V 5.0 SP3 example connection group XML file</span></span>

<span data-ttu-id="65a68-164">L’exemple de fichier XML de groupe de connexion suivant présente des exemples de champs dans les tableaux précédents et met en évidence les éléments qui sont nouveaux dans le cadre de l’application-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="65a68-164">The following example connection group XML file shows examples of the fields in the previous tables and highlights the items that are new for App-V 5.0 SP3.</span></span>

```XML
<?xml version="1.0" encoding="UTF-16"?>
<appv:AppConnectionGroup 
   xmlns="https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup"
   xmlns:appv="https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup"
   AppConnectionGroupId="61BE9B14-D2B4-41CE-A6E3-A1B658DE7000"
   VersionId="E6B6AA57-F2A7-49C9-ADF8-F2B5B3C8A42F"  
   Priority="0"  
   DisplayName="Sample Connection Group">
   <appv:Packages>
      <appv:Package      
         PackageId="1DC709C8-309F-4AB4-BD47-F75926D04276"
         VersionId="*"
         IsOptional=”true”
      />    
     <appv:Package
        PackageId="04220DCA-EE77-42BE-A9F5-96FD8E8593F2"
        VersionId="E15EFFE9-043D-4C01-BC52-AD2BD1E8BAFA"
        IsOptional="false"
     />  
   </appv:Packages>
</appv:AppConnectionGroup>
```

### <a href="" id="bkmk-50thru50sp2-exp-cg-xm"></a><span data-ttu-id="65a68-165">App-V 5,0 via App-V 5,0 SP2-exemple de fichier XML de connexion</span><span class="sxs-lookup"><span data-stu-id="65a68-165">App-V 5.0 through App-V 5.0 SP2 example connection group XML file</span></span>

<span data-ttu-id="65a68-166">L’exemple de fichier XML de groupe de connexion suivant s’applique à l’application-V 5,0 via App-V 5,0 SP2.</span><span class="sxs-lookup"><span data-stu-id="65a68-166">The following example connection group XML file applies to App-V 5.0 through App-V 5.0 SP2.</span></span> <span data-ttu-id="65a68-167">Il s’agit de exemples de champs du tableau précédent, mais exclut les changements décrits ci-dessus pour App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="65a68-167">It shows examples of the fields in the previous table, but it excludes the changes described above for App-V 5.0 SP3.</span></span>

```XML
<?xml version="1.0" encoding="UTF-16"?>
<appv:AppConnectionGroup
   xmlns="https://schemas.microsoft.com/appv/2010/virtualapplicationconnectiongroup"
   xmlns:appv="https://schemas.microsoft.com/appv/2010/virtualapplicationconnectiongroup"
   AppConnectionGroupId="61BE9B14-D2B4-41CE-A6E3-A1B658DE7000"
   VersionId="E6B6AA57-F2A7-49C9-ADF8-F2B5B3C8A42F"
   Priority="0"
   DisplayName="Sample Connection Group">
   <appv:Packages>
      <appv:Package``      
         PackageId="1DC709C8-309F-4AB4-BD47-F75926D04276"
         VersionId="C7DF4F63-5288-439C-ACEF-EF06BF401EC5"
      />
      <appv:Package
         PackageId="04220DCA-EE77-42BE-A9F5-96FD8E8593F2"
         VersionId="E15EFFE9-043D-4C01-BC52-AD2BD1E8BAFA"
      />
   </appv:Packages>
</appv:AppConnectionGroup
 ```

## <a href="" id="bkmk-config-pkg-priority-incg"></a><span data-ttu-id="65a68-168">Configuration de la priorité des packages dans un groupe de connexion</span><span class="sxs-lookup"><span data-stu-id="65a68-168">Configuring the priority of packages in a connection group</span></span>


<span data-ttu-id="65a68-169">La priorité des packages est configurée à l’aide de l’ordre de la liste des packages.</span><span class="sxs-lookup"><span data-stu-id="65a68-169">Package precedence is configured using the package list order.</span></span> <span data-ttu-id="65a68-170">Le premier package du document a la priorité la plus élevée.</span><span class="sxs-lookup"><span data-stu-id="65a68-170">The first package in the document has the highest precedence.</span></span> <span data-ttu-id="65a68-171">Les packages suivants de la liste ont une priorité décroissante.</span><span class="sxs-lookup"><span data-stu-id="65a68-171">Subsequent packages in the list have descending priority.</span></span>

<span data-ttu-id="65a68-172">La priorité des packages correspond à la résolution des conflits de ressources inévitables lors de l’initialisation de l’environnement virtuel.</span><span class="sxs-lookup"><span data-stu-id="65a68-172">Package precedence is the resolution for otherwise inevitable resource collisions during virtual environment initialization.</span></span> <span data-ttu-id="65a68-173">Par exemple, si deux packages qui s’ouvrent dans le même environnement virtuel définissent la même valeur DWORD de Registre, le package dont la priorité est la plus élevée détermine la valeur définie.</span><span class="sxs-lookup"><span data-stu-id="65a68-173">For example, if two packages that are opening in the same virtual environment define the same registry DWORD value, the package with the highest precedence determines the value that is set.</span></span>

<span data-ttu-id="65a68-174">Vous pouvez utiliser le fichier de groupe de connexion pour configurer chaque groupe de connexions en utilisant les méthodes suivantes:</span><span class="sxs-lookup"><span data-stu-id="65a68-174">You can use the connection group file to configure each connection group by using the following methods:</span></span>

-   <span data-ttu-id="65a68-175">Spécifiez les priorités d’exécution des groupes de connexion.</span><span class="sxs-lookup"><span data-stu-id="65a68-175">Specify runtime priorities for connection groups.</span></span>

    <span data-ttu-id="65a68-176">**Remarques**  Priority est requis uniquement si le package est associé à plusieurs groupes de connexion.</span><span class="sxs-lookup"><span data-stu-id="65a68-176">**Note** Priority is required only if the package is associated with more than one connection group.</span></span>

     

-   <span data-ttu-id="65a68-177">Spécifiez l’ordre de priorité des packages dans le groupe de connexions.</span><span class="sxs-lookup"><span data-stu-id="65a68-177">Specify package precedence within the connection group.</span></span>

<span data-ttu-id="65a68-178">Le champ Priority est requis pour une application virtuelle en cours d’exécution à partir d’une demande d’application native, par exemple Microsoft Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="65a68-178">The priority field is required when a running virtual application initiates from a native application request, for example, Microsoft Windows Explorer.</span></span> <span data-ttu-id="65a68-179">Le client App-V utilise la priorité pour déterminer l’environnement virtuel du groupe de connexion dans lequel l’application doit s’exécuter.</span><span class="sxs-lookup"><span data-stu-id="65a68-179">The App-V client uses the priority to determine which connection group virtual environment the application should run in.</span></span> <span data-ttu-id="65a68-180">Cette situation se produit si une application virtuelle fait partie de plusieurs groupes de connexion.</span><span class="sxs-lookup"><span data-stu-id="65a68-180">This situation occurs if a virtual application is part of multiple connection groups.</span></span>

<span data-ttu-id="65a68-181">Si une application virtuelle est ouverte à l’aide d’une autre application virtuelle, l’environnement virtuel de l’application virtuelle d’origine est utilisé.</span><span class="sxs-lookup"><span data-stu-id="65a68-181">If a virtual application is opened using another virtual application the virtual environment of the original virtual application will be used.</span></span> <span data-ttu-id="65a68-182">Le champ priorité n’est pas utilisé dans le cas présent.</span><span class="sxs-lookup"><span data-stu-id="65a68-182">The priority field is not used in this case.</span></span>

**<span data-ttu-id="65a68-183">Exemple :</span><span class="sxs-lookup"><span data-stu-id="65a68-183">Example:</span></span>**

<span data-ttu-id="65a68-184">L’application virtuelle Microsoft Outlook est en cours d’exécution dans l’environnement virtuel **xyz**.</span><span class="sxs-lookup"><span data-stu-id="65a68-184">The virtual application Microsoft Outlook is running in virtual environment **XYZ**.</span></span> <span data-ttu-id="65a68-185">Lorsque vous ouvrez un document Microsoft Word joint, une version virtualisée de Microsoft Word s’ouvre dans l’environnement virtuel **xyz**, quels que soient les groupes de connexions ou les priorités d’exécution qui sont virtualisés de Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="65a68-185">When you open an attached Microsoft Word document, a virtualized version Microsoft Word opens in the virtual environment **XYZ**, regardless of the virtualized Microsoft Word’s associated connection groups or runtime priorities.</span></span>

## <a href="" id="bkmk-va-conn-configs"></a><span data-ttu-id="65a68-186">Configurations de connexion d’applications virtuelles prises en charge</span><span class="sxs-lookup"><span data-stu-id="65a68-186">Supported virtual application connection configurations</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="65a68-187">Configuration</span><span class="sxs-lookup"><span data-stu-id="65a68-187">Configuration</span></span></th>
<th align="left"><span data-ttu-id="65a68-188">Exemple de scénario</span><span class="sxs-lookup"><span data-stu-id="65a68-188">Example scenario</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="65a68-189">Aucun.</span><span class="sxs-lookup"><span data-stu-id="65a68-189">An.</span></span> <span data-ttu-id="65a68-190">fichier exe et plug-in (. dll)</span><span class="sxs-lookup"><span data-stu-id="65a68-190">exe file and plug-in (.dll)</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="65a68-191">Vous souhaitez distribuer Microsoft Office à tous les utilisateurs, mais distribuer un plug-in Microsoft Excel uniquement à un sous-ensemble d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="65a68-191">You want to distribute Microsoft Office to all users, but distribute a Microsoft Excel plug-in to only a subset of users.</span></span></p></li>
<li><p><span data-ttu-id="65a68-192">Activez le groupe de connexion pour les utilisateurs appropriés.</span><span class="sxs-lookup"><span data-stu-id="65a68-192">Enable the connection group for the appropriate users.</span></span></p></li>
<li><p><span data-ttu-id="65a68-193">Mettez à jour chaque package individuellement selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="65a68-193">Update each package individually as required.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="65a68-194">Aucun.</span><span class="sxs-lookup"><span data-stu-id="65a68-194">An.</span></span> <span data-ttu-id="65a68-195">fichier exe et application middleware</span><span class="sxs-lookup"><span data-stu-id="65a68-195">exe file and a middleware application</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="65a68-196">Une application nécessite une application middleware ou plusieurs applications dépendent de la même version d’exécution du middleware.</span><span class="sxs-lookup"><span data-stu-id="65a68-196">You have an application requires a middleware application, or several applications that all depend on the same middleware runtime version.</span></span></p></li>
<li><p><span data-ttu-id="65a68-197">Tous les ordinateurs qui nécessitent une ou plusieurs de ces applications reçoivent les groupes de connexion avec application et Runtime de l’application middleware.</span><span class="sxs-lookup"><span data-stu-id="65a68-197">All computers that require one or more of the applications receive the connection groups with the application and middleware application runtime.</span></span></p></li>
<li><p><span data-ttu-id="65a68-198">Vous pouvez éventuellement combiner plusieurs applications middleware au sein d’un seul groupe de connexion.</span><span class="sxs-lookup"><span data-stu-id="65a68-198">You can optionally combine multiple middleware applications into a single connection group.</span></span></p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="65a68-199">Exemple</span><span class="sxs-lookup"><span data-stu-id="65a68-199">Example</span></span></th>
<th align="left"><span data-ttu-id="65a68-200">Exemple de description</span><span class="sxs-lookup"><span data-stu-id="65a68-200">Example description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="65a68-201">Groupe de connexion d’application virtuel pour la division financière</span><span class="sxs-lookup"><span data-stu-id="65a68-201">Virtual application connection group for the financial division</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="65a68-202">Application middleware 1</span><span class="sxs-lookup"><span data-stu-id="65a68-202">Middleware application 1</span></span></p></li>
<li><p><span data-ttu-id="65a68-203">Application middleware 2</span><span class="sxs-lookup"><span data-stu-id="65a68-203">Middleware application 2</span></span></p></li>
<li><p><span data-ttu-id="65a68-204">Application middleware 3</span><span class="sxs-lookup"><span data-stu-id="65a68-204">Middleware application 3</span></span></p></li>
<li><p><span data-ttu-id="65a68-205">Exécution de l’application middleware</span><span class="sxs-lookup"><span data-stu-id="65a68-205">Middleware application runtime</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="65a68-206">Groupe de connexion d’application virtuelle pour une division de ressources humaines</span><span class="sxs-lookup"><span data-stu-id="65a68-206">Virtual application connection group for HR division</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="65a68-207">Application middleware 5</span><span class="sxs-lookup"><span data-stu-id="65a68-207">Middleware application 5</span></span></p></li>
<li><p><span data-ttu-id="65a68-208">Application middleware 6</span><span class="sxs-lookup"><span data-stu-id="65a68-208">Middleware application 6</span></span></p></li>
<li><p><span data-ttu-id="65a68-209">Exécution de l’application middleware</span><span class="sxs-lookup"><span data-stu-id="65a68-209">Middleware application runtime</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>
<p> </p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="65a68-210">Aucun.</span><span class="sxs-lookup"><span data-stu-id="65a68-210">An.</span></span> <span data-ttu-id="65a68-211">fichier exe et fichier. exe</span><span class="sxs-lookup"><span data-stu-id="65a68-211">exe file and an .exe file</span></span></p></td>
<td align="left"><p><span data-ttu-id="65a68-212">Vous disposez d’une application qui s’appuie sur une autre application, et vous voulez conserver les packages séparés pour l’efficacité opérationnelle, les restrictions de licence ou les chronologies de déploiement.</span><span class="sxs-lookup"><span data-stu-id="65a68-212">You have an application that relies on another application, and you want to keep the packages separate for operational efficiencies, licensing restrictions, or rollout timelines.</span></span></p>
<p><strong><span data-ttu-id="65a68-213">Exemple :</span><span class="sxs-lookup"><span data-stu-id="65a68-213">Example:</span></span></strong></p>
<p><span data-ttu-id="65a68-214">Si vous déployez Microsoft Lync 2010, vous pouvez utiliser trois packages:</span><span class="sxs-lookup"><span data-stu-id="65a68-214">If you are deploying Microsoft Lync 2010, you can use three packages:</span></span></p>
<ul>
<li><p><span data-ttu-id="65a68-215">Microsoft Office 2010</span><span class="sxs-lookup"><span data-stu-id="65a68-215">Microsoft Office2010</span></span></p></li>
<li><p><span data-ttu-id="65a68-216">Microsoft Communicator2007</span><span class="sxs-lookup"><span data-stu-id="65a68-216">Microsoft Communicator2007</span></span></p></li>
<li><p><span data-ttu-id="65a68-217">Microsoft Lync2010</span><span class="sxs-lookup"><span data-stu-id="65a68-217">Microsoft Lync2010</span></span></p></li>
</ul>
<p><span data-ttu-id="65a68-218">Vous pouvez gérer le déploiement à l’aide des groupes de connexion suivants:</span><span class="sxs-lookup"><span data-stu-id="65a68-218">You can manage the deployment using the following connection groups:</span></span></p>
<ul>
<li><p><span data-ttu-id="65a68-219">Microsoft Office 2010 et Microsoft Communicator2007</span><span class="sxs-lookup"><span data-stu-id="65a68-219">Microsoft Office2010 and Microsoft Communicator2007</span></span></p></li>
<li><p><span data-ttu-id="65a68-220">Microsoft Office 2010 et Microsoft Lync2010</span><span class="sxs-lookup"><span data-stu-id="65a68-220">Microsoft Office2010 and Microsoft Lync2010</span></span></p></li>
</ul>
<p><span data-ttu-id="65a68-221">Lorsque le déploiement s’est terminé, vous pouvez créer un seul compte Microsoft Office 2010 + Microsoft Lync2010, ou le conserver et le conserver en tant que packages distincts et les déployer à l’aide d’un groupe de connexion.</span><span class="sxs-lookup"><span data-stu-id="65a68-221">When the deployment has completed, you can either create a single new Microsoft Office2010 + Microsoft Lync2010 package, or keep and maintain them as separate packages and deploy them by using a connection group.</span></span></p></td>
</tr>
</tbody>
</table>

 






## <span data-ttu-id="65a68-222">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="65a68-222">Related topics</span></span>


[<span data-ttu-id="65a68-223">Gestion des groupes de connexion</span><span class="sxs-lookup"><span data-stu-id="65a68-223">Managing Connection Groups</span></span>](managing-connection-groups.md)

 

 





