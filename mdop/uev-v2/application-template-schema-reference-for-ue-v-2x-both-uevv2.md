---
title: Référence du schéma de modèle d’application pour UE-V 2. x
description: Référence du schéma de modèle d’application pour UE-V 2. x
author: dansimp
ms.assetid: be8735a5-6a3e-4b1f-ba14-2a3bc3e5a8b6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 03ff6eabae68f07c23d5977f901e6a90e292c6ac
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812336"
---
# <span data-ttu-id="9606b-103">Référence du schéma de modèle d’application pour UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="9606b-103">Application Template Schema Reference for UE-V 2.x</span></span>


<span data-ttu-id="9606b-104">Microsoft User expérience Virtualization (UE-V) 2,0, 2,1 et 2,1 SP1 utilisez les modèles d’emplacement des paramètres XML pour définir les paramètres de l’application de bureau et les paramètres Windows qui sont capturés et appliqués par UE-V.</span><span class="sxs-lookup"><span data-stu-id="9606b-104">Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, and 2.1 SP1 use XML settings location templates to define the desktop application settings and Windows settings that are captured and applied by UE-V.</span></span> <span data-ttu-id="9606b-105">UE-V inclut un ensemble de modèles d’emplacement des paramètres par défaut.</span><span class="sxs-lookup"><span data-stu-id="9606b-105">UE-V includes a set of default settings location templates.</span></span> <span data-ttu-id="9606b-106">Vous pouvez également créer des modèles d’emplacement des paramètres personnalisés avec le générateur UE-V.</span><span class="sxs-lookup"><span data-stu-id="9606b-106">You can also create custom settings location templates with the UE-V Generator.</span></span>

<span data-ttu-id="9606b-107">Un utilisateur expérimenté peut personnaliser le fichier XML pour un modèle d’emplacement des paramètres.</span><span class="sxs-lookup"><span data-stu-id="9606b-107">An advanced user can customize the XML file for a settings location template.</span></span> <span data-ttu-id="9606b-108">Cette rubrique décrit en détail la structure XML des modèles d’emplacement des paramètres UE-V 2,1 (SP1) et 2,0 et fournit des recommandations pour la modification de ces fichiers.</span><span class="sxs-lookup"><span data-stu-id="9606b-108">This topic details the XML structure of the UE-V 2.1 (SP1) and 2.0 settings location templates and provides guidance for editing these files.</span></span>

## <span data-ttu-id="9606b-109">Référence du schéma de modèle d’application UE-V 2,1 et 2,1 SP1</span><span class="sxs-lookup"><span data-stu-id="9606b-109">UE-V 2.1 and 2.1 SP1 Application Template Schema Reference</span></span>


<span data-ttu-id="9606b-110">Cette section détaille la structure XML du modèle d’emplacement des paramètres UE-V 2,1 et 2,1 SP1 et fournit des instructions pour la modification de ce fichier.</span><span class="sxs-lookup"><span data-stu-id="9606b-110">This section details the XML structure of the UE-V 2.1 and 2.1 SP1 settings location template and provides guidance for editing this file.</span></span>

### <span data-ttu-id="9606b-111">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="9606b-111">In This Section</span></span>

-   [<span data-ttu-id="9606b-112">Attribut d’encodage et de déclaration XML</span><span class="sxs-lookup"><span data-stu-id="9606b-112">XML Declaration and Encoding Attribute</span></span>](#xml21)

-   [<span data-ttu-id="9606b-113">Espace de noms et élément racine</span><span class="sxs-lookup"><span data-stu-id="9606b-113">Namespace and Root Element</span></span>](#namespace21)

-   [<span data-ttu-id="9606b-114">Types de données</span><span class="sxs-lookup"><span data-stu-id="9606b-114">Data types</span></span>](#data21)

-   [<span data-ttu-id="9606b-115">Élément Name</span><span class="sxs-lookup"><span data-stu-id="9606b-115">Name Element</span></span>](#name21)

-   [<span data-ttu-id="9606b-116">Élément ID</span><span class="sxs-lookup"><span data-stu-id="9606b-116">ID Element</span></span>](#id21)

-   [<span data-ttu-id="9606b-117">Élément version</span><span class="sxs-lookup"><span data-stu-id="9606b-117">Version Element</span></span>](#version21)

-   [<span data-ttu-id="9606b-118">Élément Author</span><span class="sxs-lookup"><span data-stu-id="9606b-118">Author Element</span></span>](#author21)

-   [<span data-ttu-id="9606b-119">Processus et élément de processus</span><span class="sxs-lookup"><span data-stu-id="9606b-119">Processes and Process Element</span></span>](#processes21)

-   [<span data-ttu-id="9606b-120">Élément application</span><span class="sxs-lookup"><span data-stu-id="9606b-120">Application Element</span></span>](#application21)

-   [<span data-ttu-id="9606b-121">Élément commun</span><span class="sxs-lookup"><span data-stu-id="9606b-121">Common Element</span></span>](#common21)

-   [<span data-ttu-id="9606b-122">Élément SettingsLocationTemplate</span><span class="sxs-lookup"><span data-stu-id="9606b-122">SettingsLocationTemplate Element</span></span>](#settingslocationtemplate21)

-   [<span data-ttu-id="9606b-123">Annexe: SettingsLocationTemplate. xsd</span><span class="sxs-lookup"><span data-stu-id="9606b-123">Appendix: SettingsLocationTemplate.xsd</span></span>](#appendix21)

### <a href="" id="xml21"></a><span data-ttu-id="9606b-124">Attribut d’encodage et de déclaration XML</span><span class="sxs-lookup"><span data-stu-id="9606b-124">XML Declaration and Encoding Attribute</span></span>

**<span data-ttu-id="9606b-125">Obligatoire: vrai</span><span class="sxs-lookup"><span data-stu-id="9606b-125">Mandatory: True</span></span>**

**<span data-ttu-id="9606b-126">Type: chaîne</span><span class="sxs-lookup"><span data-stu-id="9606b-126">Type: String</span></span>**

<span data-ttu-id="9606b-127">La déclaration XML doit spécifier l’attribut XML version 1,0 ( &lt; ? xml version = «1.0» &gt; ).</span><span class="sxs-lookup"><span data-stu-id="9606b-127">The XML declaration must specify the XML version 1.0 attribute (&lt;?xml version="1.0"&gt;).</span></span> <span data-ttu-id="9606b-128">Les modèles d’emplacement des paramètres créés par le générateur UE-V sont enregistrés au format UTF-8, même si le codage n’est pas explicitement spécifié.</span><span class="sxs-lookup"><span data-stu-id="9606b-128">Settings location templates created by the UE-V Generator are saved in UTF-8 encoding, although the encoding is not explicitly specified.</span></span> <span data-ttu-id="9606b-129">Nous vous recommandons d’inclure l’attribut Encoding = «UTF-8» dans cet élément comme meilleure pratique.</span><span class="sxs-lookup"><span data-stu-id="9606b-129">We recommend that you include the encoding="UTF-8" attribute in this element as a best practice.</span></span> <span data-ttu-id="9606b-130">Tous les modèles inclus dans le produit spécifient également cette balise (voir les documents dans l’interface utilisateur de%ProgramFiles%\\Microsoft Virtualization\\Templates pour référence).</span><span class="sxs-lookup"><span data-stu-id="9606b-130">All templates included with the product specify this tag as well (see the documents in %ProgramFiles%\\Microsoft User Experience Virtualization\\Templates for reference).</span></span> <span data-ttu-id="9606b-131">Exemple:</span><span class="sxs-lookup"><span data-stu-id="9606b-131">For example:</span></span>

`<?xml version="1.0" encoding="UTF-8"?>`

### <a href="" id="namespace21"></a><span data-ttu-id="9606b-132">Espace de noms et élément racine</span><span class="sxs-lookup"><span data-stu-id="9606b-132">Namespace and Root Element</span></span>

**<span data-ttu-id="9606b-133">Obligatoire: vrai</span><span class="sxs-lookup"><span data-stu-id="9606b-133">Mandatory: True</span></span>**

**<span data-ttu-id="9606b-134">Type: chaîne</span><span class="sxs-lookup"><span data-stu-id="9606b-134">Type: String</span></span>**

<span data-ttu-id="9606b-135">UE-V utilise l' https://schemas.microsoft.com/UserExperienceVirtualization/2012/SettingsLocationTemplate espace de noms pour toutes les applications.</span><span class="sxs-lookup"><span data-stu-id="9606b-135">UE-V uses the https://schemas.microsoft.com/UserExperienceVirtualization/2012/SettingsLocationTemplate namespace for all applications.</span></span> <span data-ttu-id="9606b-136">SettingsLocationTemplate est l’élément racine et contient tous les autres éléments.</span><span class="sxs-lookup"><span data-stu-id="9606b-136">SettingsLocationTemplate is the root element and contains all other elements.</span></span> <span data-ttu-id="9606b-137">Référencez SettingsLocationTemplate dans tous les modèles à l’aide de cette balise:</span><span class="sxs-lookup"><span data-stu-id="9606b-137">Reference SettingsLocationTemplate in all templates using this tag:</span></span>

`<SettingsLocationTemplate xmlns='https://schemas.microsoft.com/UserExperienceVirtualization/2012/SettingsLocationTemplate'>`

### <a href="" id="data21"></a><span data-ttu-id="9606b-138">Types de données</span><span class="sxs-lookup"><span data-stu-id="9606b-138">Data types</span></span>

<span data-ttu-id="9606b-139">Il s’agit des types de données pour le schéma de modèle d’application UE-V.</span><span class="sxs-lookup"><span data-stu-id="9606b-139">These are the data types for the UE-V application template schema.</span></span>

<a href="" id="guid"></a><span data-ttu-id="9606b-140">**GUID** GUID décrit une expression régulière d’identificateur unique global standard au format «\ \ {\ [a-fA-F0-9 \] {8} -\ [a-FA-F0-9] {4} -\ [a------------------- {4} ---- {4} ---------------- {12} ----------------</span><span class="sxs-lookup"><span data-stu-id="9606b-140">**GUID** GUID describes a standard globally unique identifier regular expression in the form "\\{\[a-fA-F0-9\]{8}-\[a-fA-F0-9\]{4}-\[a-fA-F0-9\]{4}-\[a-fA-F0-9\]{4}-\[a-fA-F0-9\]{12}\\}".</span></span> <span data-ttu-id="9606b-141">Cette opération est utilisée dans l’élément Filesetting\\Root\\KnownFolder pour vérifier la mise en forme de dossiers bien connus.</span><span class="sxs-lookup"><span data-stu-id="9606b-141">This is used in the Filesetting\\Root\\KnownFolder element to verify the formatting of well-known folders.</span></span>

<a href="" id="filenamestring"></a><span data-ttu-id="9606b-142">**FilenameString** FilenameString fait référence au nom de fichier d’un processus à surveiller.</span><span class="sxs-lookup"><span data-stu-id="9606b-142">**FilenameString** FilenameString refers to the file name of a process to be monitored.</span></span> <span data-ttu-id="9606b-143">Ses valeurs ne sont pas limitées par le caractère &lt; &gt; Regex \ [^ \ \ \ \ \ ^ /: \] +, (autrement dit, ils ne peuvent pas contenir de caractères de barre oblique inverse, d’astérisques ou de signes d’interrogation, de caractère de barre oblique, de signe supérieur ou inférieur à, de barre oblique ou de deux-points).</span><span class="sxs-lookup"><span data-stu-id="9606b-143">Its values are restricted by the regex \[^\\\\\\?\\\*\\|&lt;&gt;/:\]+, (that is, they may not contain backslash characters, asterisk or question mark wild-card characters, the pipe character, the greater than or less than sign, forward slash, or colon characters).</span></span>

<a href="" id="idstring"></a><span data-ttu-id="9606b-144">**IdString** IDString fait référence à la valeur d’ID des éléments d’application, SettingsLocationTemplate et éléments communs (utilisés pour décrire les suites d’applications qui partagent des paramètres communs).</span><span class="sxs-lookup"><span data-stu-id="9606b-144">**IDString** IDString refers to the ID value of Application elements, SettingsLocationTemplate, and Common elements (used to describe application suites that share common settings).</span></span> <span data-ttu-id="9606b-145">Ce dernier est limité par le même Regex que FilenameString (\ [^ \ \ \ \ \ \? &lt; &gt; /:\]+).</span><span class="sxs-lookup"><span data-stu-id="9606b-145">It is restricted by the same regex as FilenameString (\[^\\\\\\?\\\*\\|&lt;&gt;/:\]+).</span></span>

<a href="" id="templateversion"></a><span data-ttu-id="9606b-146">**TemplateVersion** TemplateVersion est une valeur entière utilisée pour décrire la révision du modèle d’emplacement des paramètres.</span><span class="sxs-lookup"><span data-stu-id="9606b-146">**TemplateVersion** TemplateVersion is an integer value used to describe the revision of the settings location template.</span></span> <span data-ttu-id="9606b-147">Sa valeur est comprise entre 0 et 2147483647.</span><span class="sxs-lookup"><span data-stu-id="9606b-147">Its value may range from 0 to 2147483647.</span></span>

<a href="" id="empty"></a><span data-ttu-id="9606b-148">**Vides** Empty fait référence à une valeur null.</span><span class="sxs-lookup"><span data-stu-id="9606b-148">**Empty** Empty refers to a null value.</span></span> <span data-ttu-id="9606b-149">Ce champ est utilisé dans Process\\ShellProcess pour indiquer qu’il n’y a pas de processus à surveiller.</span><span class="sxs-lookup"><span data-stu-id="9606b-149">This is used in Process\\ShellProcess to indicate that there is no process to monitor.</span></span> <span data-ttu-id="9606b-150">Cette valeur ne doit pas être utilisée dans les modèles d’application.</span><span class="sxs-lookup"><span data-stu-id="9606b-150">This value should not be used in any application templates.</span></span>

<a href="" id="author"></a><span data-ttu-id="9606b-151">**Auteur** Le type de données auteur est un type complexe qui identifie l’auteur d’un modèle.</span><span class="sxs-lookup"><span data-stu-id="9606b-151">**Author** The Author data type is a complex type that identifies the author of a template.</span></span> <span data-ttu-id="9606b-152">Il contient deux éléments enfants: le **nom** et l' **adresse de courrier**.</span><span class="sxs-lookup"><span data-stu-id="9606b-152">It contains two child elements: **Name** and **Email**.</span></span> <span data-ttu-id="9606b-153">Dans le type de données auteur, l’élément nom est obligatoire lorsque l’élément de messagerie est facultatif.</span><span class="sxs-lookup"><span data-stu-id="9606b-153">Within the Author data type, the Name element is mandatory while the Email element is optional.</span></span> <span data-ttu-id="9606b-154">Ce type est décrit plus en détail dans l’élément SettingsLocationTemplate.</span><span class="sxs-lookup"><span data-stu-id="9606b-154">This type is described in more detail under the SettingsLocationTemplate element.</span></span>

<a href="" id="range"></a><span data-ttu-id="9606b-155">**Plage** Range définit une classe entière composée de deux éléments enfants: **minimum** et **maximum**.</span><span class="sxs-lookup"><span data-stu-id="9606b-155">**Range** Range defines an integer class consisting of two child elements: **Minimum** and **Maximum**.</span></span> <span data-ttu-id="9606b-156">Ce type de données est implémenté dans le type de données ProcessVersion.</span><span class="sxs-lookup"><span data-stu-id="9606b-156">This data type is implemented in the ProcessVersion data type.</span></span> <span data-ttu-id="9606b-157">Si ce paramètre est spécifié, les valeurs minimum et maximum doivent être incluses.</span><span class="sxs-lookup"><span data-stu-id="9606b-157">If specified, both Minimum and Maximum values must be included.</span></span>

<a href="" id="processversion"></a><span data-ttu-id="9606b-158">**ProcessVersion** ProcessVersion définit un type avec quatre éléments enfants: **major**, **Minor**, **Build**et **patch**.</span><span class="sxs-lookup"><span data-stu-id="9606b-158">**ProcessVersion** ProcessVersion defines a type with four child elements: **Major**, **Minor**, **Build**, and **Patch**.</span></span> <span data-ttu-id="9606b-159">Ce type de données est utilisé par l’élément process pour remplir ses valeurs ProductVersion et FileVersion.</span><span class="sxs-lookup"><span data-stu-id="9606b-159">This data type is used by the Process element to populate its ProductVersion and FileVersion values.</span></span> <span data-ttu-id="9606b-160">Les données pour ce type constituent une valeur de plage.</span><span class="sxs-lookup"><span data-stu-id="9606b-160">The data for this type is a Range value.</span></span> <span data-ttu-id="9606b-161">L’élément enfant principal est obligatoire et les autres sont facultatifs.</span><span class="sxs-lookup"><span data-stu-id="9606b-161">The Major child element is mandatory and the others are optional.</span></span>

<a href="" id="architecture"></a><span data-ttu-id="9606b-162">**Architecture** Architecture énumère deux valeurs possibles: **Win32** et **Win64**.</span><span class="sxs-lookup"><span data-stu-id="9606b-162">**Architecture** Architecture enumerates two possible values: **Win32** and **Win64**.</span></span> <span data-ttu-id="9606b-163">Ces valeurs sont utilisées pour spécifier l’architecture de processus.</span><span class="sxs-lookup"><span data-stu-id="9606b-163">These values are used to specify process architecture.</span></span>

<a href="" id="process"></a><span data-ttu-id="9606b-164">**Processus** Le type de données de processus est un conteneur utilisé pour décrire les processus à surveiller par UE-V.</span><span class="sxs-lookup"><span data-stu-id="9606b-164">**Process** The Process data type is a container used to describe processes to be monitored by UE-V.</span></span> <span data-ttu-id="9606b-165">Il contient six éléments enfants: **filename**, **architecture**, **ProductName**, **FileDescription**, **ProductVersion**et **FileVersion**.</span><span class="sxs-lookup"><span data-stu-id="9606b-165">It contains six child elements: **Filename**, **Architecture**, **ProductName**, **FileDescription**, **ProductVersion**, and **FileVersion**.</span></span> <span data-ttu-id="9606b-166">Ce tableau présente les différents types de données de chaque élément:</span><span class="sxs-lookup"><span data-stu-id="9606b-166">This table details each element’s respective data type:</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="9606b-167">Élément</span><span class="sxs-lookup"><span data-stu-id="9606b-167">Element</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="9606b-168">Type de données</span><span class="sxs-lookup"><span data-stu-id="9606b-168">Data Type</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="9606b-169">Mandatory</span><span class="sxs-lookup"><span data-stu-id="9606b-169">Mandatory</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9606b-170">Courts</span><span class="sxs-lookup"><span data-stu-id="9606b-170">Filename</span></span></p></td>
<td align="left"><p><span data-ttu-id="9606b-171">FilenameString</span><span class="sxs-lookup"><span data-stu-id="9606b-171">FilenameString</span></span></p></td>
<td align="left"><p><span data-ttu-id="9606b-172">Vrai</span><span class="sxs-lookup"><span data-stu-id="9606b-172">True</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9606b-173">Architecture</span><span class="sxs-lookup"><span data-stu-id="9606b-173">Architecture</span></span></p></td>
<td align="left"><p><span data-ttu-id="9606b-174">Architecture</span><span class="sxs-lookup"><span data-stu-id="9606b-174">Architecture</span></span></p></td>
<td align="left"><p><span data-ttu-id="9606b-175">Faux</span><span class="sxs-lookup"><span data-stu-id="9606b-175">False</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9606b-176">ProductName</span><span class="sxs-lookup"><span data-stu-id="9606b-176">ProductName</span></span></p></td>
<td align="left"><p><span data-ttu-id="9606b-177">String</span><span class="sxs-lookup"><span data-stu-id="9606b-177">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="9606b-178">Faux</span><span class="sxs-lookup"><span data-stu-id="9606b-178">False</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9606b-179">FileDescription</span><span class="sxs-lookup"><span data-stu-id="9606b-179">FileDescription</span></span></p></td>
<td align="left"><p><span data-ttu-id="9606b-180">String</span><span class="sxs-lookup"><span data-stu-id="9606b-180">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="9606b-181">Faux</span><span class="sxs-lookup"><span data-stu-id="9606b-181">False</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9606b-182">ProductVersion</span><span class="sxs-lookup"><span data-stu-id="9606b-182">ProductVersion</span></span></p></td>
<td align="left"><p><span data-ttu-id="9606b-183">ProcessVersion</span><span class="sxs-lookup"><span data-stu-id="9606b-183">ProcessVersion</span></span></p></td>
<td align="left"><p><span data-ttu-id="9606b-184">Faux</span><span class="sxs-lookup"><span data-stu-id="9606b-184">False</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9606b-185">FileVersion</span><span class="sxs-lookup"><span data-stu-id="9606b-185">FileVersion</span></span></p></td>
<td align="left"><p><span data-ttu-id="9606b-186">ProcessVersion</span><span class="sxs-lookup"><span data-stu-id="9606b-186">ProcessVersion</span></span></p></td>
<td align="left"><p><span data-ttu-id="9606b-187">Faux</span><span class="sxs-lookup"><span data-stu-id="9606b-187">False</span></span></p></td>
</tr>
</tbody>
</table>

 

<a href="" id="processes"></a><span data-ttu-id="9606b-188">**Processus** Le type de données processus représente un conteneur pour une collection d’un ou plusieurs éléments de processus.</span><span class="sxs-lookup"><span data-stu-id="9606b-188">**Processes** The Processes data type represents a container for a collection of one or more Process elements.</span></span> <span data-ttu-id="9606b-189">Deux éléments enfants sont pris en charge dans le **type de séquence processus et** **ShellProcess**.</span><span class="sxs-lookup"><span data-stu-id="9606b-189">Two child elements are supported in the Processes sequence type: **Process** and **ShellProcess**.</span></span> <span data-ttu-id="9606b-190">Process est un élément de type process et ShellProcess est de type de données Empty.</span><span class="sxs-lookup"><span data-stu-id="9606b-190">Process is an element of type Process and ShellProcess is of data type Empty.</span></span> <span data-ttu-id="9606b-191">Au moins un élément doit être identifié dans la séquence.</span><span class="sxs-lookup"><span data-stu-id="9606b-191">At least one item must be identified in the sequence.</span></span>

<a href="" id="path"></a><span data-ttu-id="9606b-192">**Path (chemin** ) Path est consommé par RegistrySetting et FileSetting pour faire référence aux chemins d’accès du Registre et des fichiers.</span><span class="sxs-lookup"><span data-stu-id="9606b-192">**Path** Path is consumed by RegistrySetting and FileSetting to refer to registry and file paths.</span></span> <span data-ttu-id="9606b-193">Cet élément prend en charge deux attributs facultatifs: **récurrent** et **DeleteIfNotFound**.</span><span class="sxs-lookup"><span data-stu-id="9606b-193">This element supports two optional attributes: **Recursive** and **DeleteIfNotFound**.</span></span> <span data-ttu-id="9606b-194">Les deux valeurs sont définies sur Default = «false».</span><span class="sxs-lookup"><span data-stu-id="9606b-194">Both values are set to default=”False”.</span></span>

<span data-ttu-id="9606b-195">La récursivité indique que le chemin d’accès et tous les sous-dossiers sont inclus pour les paramètres de fichier ou que toutes les clés de Registre enfant sont incluses pour les paramètres du Registre.</span><span class="sxs-lookup"><span data-stu-id="9606b-195">Recursive indicates that the path and all subfolders are included for file settings or that all child registry keys are included for registry settings.</span></span> <span data-ttu-id="9606b-196">Dans les deux cas, tous les éléments du niveau actuel sont inclus dans les données capturées.</span><span class="sxs-lookup"><span data-stu-id="9606b-196">In both cases, all items at the current level are included in the data captured.</span></span> <span data-ttu-id="9606b-197">Pour un objet FileSettings, tous les fichiers dans le dossier spécifié sont inclus dans les données capturées par UE-V, mais les dossiers ne sont pas inclus.</span><span class="sxs-lookup"><span data-stu-id="9606b-197">For a FileSettings object, all files within the specified folder are included in the data captured by UE-V but folders are not included.</span></span> <span data-ttu-id="9606b-198">Pour les chemins d’accès de Registre, toutes les valeurs du chemin d’accès actuel sont capturées, mais les clés de Registre enfants ne sont pas capturées.</span><span class="sxs-lookup"><span data-stu-id="9606b-198">For registry paths, all values in the current path are captured but child registry keys are not captured.</span></span> <span data-ttu-id="9606b-199">Dans les deux cas, veillez à éviter de capturer des jeux de données volumineux ou d’un grand nombre d’éléments.</span><span class="sxs-lookup"><span data-stu-id="9606b-199">In both cases, care should be taken to avoid capturing large data sets or large numbers of items.</span></span>

<span data-ttu-id="9606b-200">L’attribut DeleteIfNotFound supprime le paramètre des données de chemin d’accès au stockage des paramètres de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9606b-200">The DeleteIfNotFound attribute removes the setting from the user’s settings storage path data.</span></span> <span data-ttu-id="9606b-201">Cela peut être souhaitable dans les cas où la suppression de ces paramètres du package permet d’économiser une grande quantité d’espace disque sur le serveur de fichiers de chemin d’accès de l’emplacement de stockage des paramètres.</span><span class="sxs-lookup"><span data-stu-id="9606b-201">This may be desirable in cases where removing these settings from the package will save a large amount of disk space on the settings storage path file server.</span></span>

<a href="" id="filemask"></a><span data-ttu-id="9606b-202">**Filemask** FileMask spécifie uniquement certains types de fichiers définis par Path.</span><span class="sxs-lookup"><span data-stu-id="9606b-202">**FileMask** FileMask specifies only certain file types for the folder that is defined by Path.</span></span> <span data-ttu-id="9606b-203">Par exemple, path peut être `C:\users\username\files` et filemask peut être `*.txt` pour inclure uniquement des fichiers texte.</span><span class="sxs-lookup"><span data-stu-id="9606b-203">For example, Path might be `C:\users\username\files` and FileMask could be `*.txt` to include only text files.</span></span>

<a href="" id="registrysetting"></a><span data-ttu-id="9606b-204">**RegistrySetting** RegistrySetting représente un conteneur pour les clés et les valeurs de Registre et le comportement souhaité associé au sein de l’agent UE-V.</span><span class="sxs-lookup"><span data-stu-id="9606b-204">**RegistrySetting** RegistrySetting represents a container for registry keys and values and the associated desired behavior on the part of the UE-V Agent.</span></span> <span data-ttu-id="9606b-205">Quatre éléments enfants sont définis dans ce type: **path**, **Name**, **Exclude**et une séquence des valeurs **path** et **Name**.</span><span class="sxs-lookup"><span data-stu-id="9606b-205">Four child elements are defined within this type: **Path**, **Name**, **Exclude**, and a sequence of the values **Path** and **Name**.</span></span>

<a href="" id="filesetting"></a><span data-ttu-id="9606b-206">**FileSetting** FileSetting contient des paramètres associés à des fichiers et des chemins d’accès aux fichiers.</span><span class="sxs-lookup"><span data-stu-id="9606b-206">**FileSetting** FileSetting contains parameters associated with files and files paths.</span></span> <span data-ttu-id="9606b-207">Quatre éléments enfants sont définis: **root**, **path**, **filemask**et **Exclude**.</span><span class="sxs-lookup"><span data-stu-id="9606b-207">Four child elements are defined: **Root**, **Path**, **FileMask**, and **Exclude**.</span></span> <span data-ttu-id="9606b-208">La racine est obligatoire et les autres sont facultatifs.</span><span class="sxs-lookup"><span data-stu-id="9606b-208">Root is mandatory and the others are optional.</span></span>

<a href="" id="settings"></a><span data-ttu-id="9606b-209">**Paramètres** Settings est un conteneur pour tous les paramètres qui s’appliquent à un modèle spécifique.</span><span class="sxs-lookup"><span data-stu-id="9606b-209">**Settings** Settings is a container for all the settings that apply to a particular template.</span></span> <span data-ttu-id="9606b-210">Il contient des instances des paramètres de Registre, de fichier, de SystemParameter et d’CustomAction décrits plus haut.</span><span class="sxs-lookup"><span data-stu-id="9606b-210">It contains instances of the Registry, File, SystemParameter, and CustomAction settings described earlier.</span></span> <span data-ttu-id="9606b-211">De plus, il peut également contenir les éléments enfants suivants avec des comportements décrits:</span><span class="sxs-lookup"><span data-stu-id="9606b-211">In addition, it can also contain the following child elements with behaviors described:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="9606b-212">Élément</span><span class="sxs-lookup"><span data-stu-id="9606b-212">Element</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="9606b-213">Description</span><span class="sxs-lookup"><span data-stu-id="9606b-213">Description</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9606b-214">Asynchrone</span><span class="sxs-lookup"><span data-stu-id="9606b-214">Asynchronous</span></span></p></td>
<td align="left"><p><span data-ttu-id="9606b-215">Les packages de paramètres asynchrones s’appliquent sans bloquer le démarrage de l’application afin que l’application démarre alors que les paramètres sont encore appliqués.</span><span class="sxs-lookup"><span data-stu-id="9606b-215">Asynchronous settings packages are applied without blocking the application startup so that the application start proceeds while the settings are still being applied.</span></span> <span data-ttu-id="9606b-216">Cela s’avère utile pour les paramètres qui peuvent être appliqués de manière asynchrone, par exemple par le <code>get/set</code> biais d’une API telle que SystemParameterSetting.</span><span class="sxs-lookup"><span data-stu-id="9606b-216">This is useful for settings that can be applied asynchronously, such as those <code>get/set</code> through an API, like SystemParameterSetting.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9606b-217">PreventOverlappingSynchronization</span><span class="sxs-lookup"><span data-stu-id="9606b-217">PreventOverlappingSynchronization</span></span></p></td>
<td align="left"><p><span data-ttu-id="9606b-218">Par défaut, UE-V enregistre uniquement les paramètres d’une application lorsque la dernière instance d’une application utilisant le modèle est fermée.</span><span class="sxs-lookup"><span data-stu-id="9606b-218">By default, UE-V only saves settings for an application when the last instance of an application using the template is closed.</span></span> <span data-ttu-id="9606b-219">Lorsque cet élément est défini sur «false», UE-V exporte les paramètres même si d’autres instances d’une application sont en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="9606b-219">When this element is set to ‘false’, UE-V exports the settings even if other instances of an application are running.</span></span> <span data-ttu-id="9606b-220">Les modèles adaptés, qui incluent une section commune des éléments, qui sont livrés avec UE-V, utilisent cet indicateur pour permettre aux paramètres partagés de toujours exporter à la fermeture de l’application, tout en empêchant les paramètres spécifiques à l’application d’être exportés jusqu’à la fin de la dernière instance.</span><span class="sxs-lookup"><span data-stu-id="9606b-220">Suited templates – those that include a Common element section– that are shipped with UE-V use this flag to enable shared settings to always export on application close, while preventing application-specific settings from exporting until the last instance is closed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9606b-221">AlwaysApplySettings</span><span class="sxs-lookup"><span data-stu-id="9606b-221">AlwaysApplySettings</span></span></p></td>
<td align="left"><p><span data-ttu-id="9606b-222">(introduite dans 2,1)</span><span class="sxs-lookup"><span data-stu-id="9606b-222">(introduced in 2.1)</span></span></p>
<p><span data-ttu-id="9606b-223">Ce paramètre force l’application d’un package de paramètres importés même s’il n’y a pas de différences entre le package et l’état actuel de l’application.</span><span class="sxs-lookup"><span data-stu-id="9606b-223">This parameter forces an imported settings package to be applied even if there are no differences between the package and the current state of the application.</span></span> <span data-ttu-id="9606b-224">Ce paramètre doit être utilisé uniquement dans les cas particuliers, car il peut ralentir l’importation des paramètres.</span><span class="sxs-lookup"><span data-stu-id="9606b-224">This parameter should be used only in special cases since it can slow down settings import.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="name21"></a><span data-ttu-id="9606b-225">Élément Name</span><span class="sxs-lookup"><span data-stu-id="9606b-225">Name Element</span></span>

**<span data-ttu-id="9606b-226">Obligatoire: vrai</span><span class="sxs-lookup"><span data-stu-id="9606b-226">Mandatory: True</span></span>**

**<span data-ttu-id="9606b-227">Type: chaîne</span><span class="sxs-lookup"><span data-stu-id="9606b-227">Type: String</span></span>**

<span data-ttu-id="9606b-228">Nom spécifie un nom unique pour le modèle d’emplacement des paramètres.</span><span class="sxs-lookup"><span data-stu-id="9606b-228">Name specifies a unique name for the settings location template.</span></span> <span data-ttu-id="9606b-229">Il est utilisé à des fins d’affichage lors du référencement du modèle dans WMI, PowerShell, Observateur d’événements et journaux de débogage.</span><span class="sxs-lookup"><span data-stu-id="9606b-229">This is used for display purposes when referencing the template in WMI, PowerShell, Event Viewer and debug logs.</span></span> <span data-ttu-id="9606b-230">En règle générale, évitez de référencer les informations de version, car cela peut être objet à partir de l’élément ProductVersion.</span><span class="sxs-lookup"><span data-stu-id="9606b-230">In general, avoid referencing version information, as this can be objected from the ProductVersion element.</span></span> <span data-ttu-id="9606b-231">Par exemple, spécifiez `<Name>My Application</Name>` plutôt que `<Name>My Application 1.1</Name>` .</span><span class="sxs-lookup"><span data-stu-id="9606b-231">For example, specify `<Name>My Application</Name>` rather than `<Name>My Application 1.1</Name>`.</span></span>

<span data-ttu-id="9606b-232">**Remarques**  UE-V ne référence pas les DTD externes, de sorte qu’il n’est pas possible d’utiliser des entités nommées dans un modèle d’emplacement des paramètres.</span><span class="sxs-lookup"><span data-stu-id="9606b-232">**Note** UE-V does not reference external DTDs, so it is not possible to use named entities in a settings location template.</span></span> <span data-ttu-id="9606b-233">Par exemple, n’utilisez pas &reg; pour se référer au signe de marque commerciale enregistré®.</span><span class="sxs-lookup"><span data-stu-id="9606b-233">For example, do not use &reg; to refer to the registered trade mark sign ®.</span></span> <span data-ttu-id="9606b-234">Au lieu de cela, utilisez des références numérotées canoniques pour inclure ces types de caractères spéciaux (par exemple, & \ #174 pour le caractère®.</span><span class="sxs-lookup"><span data-stu-id="9606b-234">Instead, use canonical numbered references to include these types of special characters, for example, &\#174 for the ® character.</span></span> <span data-ttu-id="9606b-235">Cette règle s’applique à toutes les valeurs de chaîne dans ce document.</span><span class="sxs-lookup"><span data-stu-id="9606b-235">This rule applies to all string values in this document.</span></span>

<span data-ttu-id="9606b-236"><http://www.w3.org/TR/xhtml1/dtds.html>Pour obtenir la liste complète des entités de caractères, voir.</span><span class="sxs-lookup"><span data-stu-id="9606b-236">See <http://www.w3.org/TR/xhtml1/dtds.html> for a complete list of character entities.</span></span> <span data-ttu-id="9606b-237">Les documents encodés au format UTF-8 peuvent inclure les caractères Unicode directement.</span><span class="sxs-lookup"><span data-stu-id="9606b-237">UTF-8-encoded documents may include the Unicode characters directly.</span></span> <span data-ttu-id="9606b-238">L’enregistrement de modèles par le biais du générateur UE-V convertit automatiquement des entités de caractères en leur représentation Unicode.</span><span class="sxs-lookup"><span data-stu-id="9606b-238">Saving templates through the UE-V Generator converts character entities to their Unicode representations automatically.</span></span>

 

### <a href="" id="id21"></a><span data-ttu-id="9606b-239">Élément ID</span><span class="sxs-lookup"><span data-stu-id="9606b-239">ID Element</span></span>

**<span data-ttu-id="9606b-240">Obligatoire: vrai</span><span class="sxs-lookup"><span data-stu-id="9606b-240">Mandatory: True</span></span>**

**<span data-ttu-id="9606b-241">Type: chaîne</span><span class="sxs-lookup"><span data-stu-id="9606b-241">Type: String</span></span>**

<span data-ttu-id="9606b-242">ID remplit un identificateur unique pour un modèle particulier.</span><span class="sxs-lookup"><span data-stu-id="9606b-242">ID populates a unique identifier for a particular template.</span></span> <span data-ttu-id="9606b-243">Cette balise devient l’identificateur principal utilisé par l’agent UE-V pour référencer le modèle lors de l’exécution (par exemple, voir la sortie des cmdlets Get-UevTemplate et Get-UevTemplateProgram PowerShell).</span><span class="sxs-lookup"><span data-stu-id="9606b-243">This tag becomes the primary identifier that the UE-V Agent uses to reference the template at runtime (for example, see the output of the Get-UevTemplate and Get-UevTemplateProgram PowerShell cmdlets).</span></span> <span data-ttu-id="9606b-244">Par Convention, cette balise ne doit contenir aucun espace, ce qui simplifie la création de scripts.</span><span class="sxs-lookup"><span data-stu-id="9606b-244">By convention, this tag should not contain any spaces, which simplifies scripting.</span></span> <span data-ttu-id="9606b-245">Le numéro de version des applications doit être spécifié dans cet élément pour faciliter l’identification du modèle, par exemple `<ID>MicrosoftCalculator6</ID>` ou `<ID>MicrosoftOffice2010Win64</ID>` .</span><span class="sxs-lookup"><span data-stu-id="9606b-245">Version numbers of applications should be specified in this element to allow for easy identification of the template, such as `<ID>MicrosoftCalculator6</ID>` or `<ID>MicrosoftOffice2010Win64</ID>`.</span></span>

### <a href="" id="version21"></a><span data-ttu-id="9606b-246">Élément version</span><span class="sxs-lookup"><span data-stu-id="9606b-246">Version Element</span></span>

**<span data-ttu-id="9606b-247">Obligatoire: vrai</span><span class="sxs-lookup"><span data-stu-id="9606b-247">Mandatory: True</span></span>**

**<span data-ttu-id="9606b-248">Type: entier</span><span class="sxs-lookup"><span data-stu-id="9606b-248">Type: Integer</span></span>**

**<span data-ttu-id="9606b-249">Valeur minimale: 0</span><span class="sxs-lookup"><span data-stu-id="9606b-249">Minimum Value: 0</span></span>**

**<span data-ttu-id="9606b-250">Valeur maximale: 2147483647</span><span class="sxs-lookup"><span data-stu-id="9606b-250">Maximum Value: 2147483647</span></span>**

<span data-ttu-id="9606b-251">Version identifie la version du modèle d’emplacement paramètres pour le suivi des modifications.</span><span class="sxs-lookup"><span data-stu-id="9606b-251">Version identifies the version of the settings location template for administrative tracking of changes.</span></span> <span data-ttu-id="9606b-252">Le générateur UE-V augmente automatiquement ce nombre de une unité chaque fois que le modèle est enregistré.</span><span class="sxs-lookup"><span data-stu-id="9606b-252">The UE-V Generator automatically increments this number by one each time the template is saved.</span></span> <span data-ttu-id="9606b-253">Notez que ce champ doit contenir un nombre entier. les valeurs fractionnaires, par exemple, `<Version>2.5</Version>` ne sont pas autorisées.</span><span class="sxs-lookup"><span data-stu-id="9606b-253">Notice that this field must be a whole number integer; fractional values, such as `<Version>2.5</Version>` are not allowed.</span></span>

<span data-ttu-id="9606b-254">**Astuce:** Vous pouvez enregistrer des notes sur les changements de version à l’aide d’indicateurs de commentaires XML `<!-- -->` , par exemple:</span><span class="sxs-lookup"><span data-stu-id="9606b-254">**Hint:** You can save notes about version changes using XML comment tags `<!-- -->`, for example:</span></span>

```xml
  <!--
     Version History

     Version 1 Jul 05, 2012 Initial template created by Generator - Denise@Contoso.com
     Version 2 Jul 31, 2012 Added support for app.exe v2.1.3 - Mark@Contoso.com
     Version 3 Jan 01, 2013 Added font settings support - Mark@Contoso.com
     Version 4 Jan 31, 2013 Added support for plugin settings - Tony@Contoso.com
   -->
  <Version>4</Version>
```

<span data-ttu-id="9606b-255">**Important**  Cette valeur est interrogée pour déterminer si une nouvelle version d’un modèle doit être appliquée à un modèle existant dans les cas suivants:</span><span class="sxs-lookup"><span data-stu-id="9606b-255">**Important** This value is queried to determine if a new version of a template should be applied to an existing template in these instances:</span></span>

-   <span data-ttu-id="9606b-256">Lorsque la tâche de mise à jour automatique du modèle planifié s’exécute</span><span class="sxs-lookup"><span data-stu-id="9606b-256">When the scheduled Template Auto Update task executes</span></span>

-   <span data-ttu-id="9606b-257">Lors de l’exécution de la cmdlet PowerShell Update-UevTemplate</span><span class="sxs-lookup"><span data-stu-id="9606b-257">When the Update-UevTemplate PowerShell cmdlet is executed</span></span>

-   <span data-ttu-id="9606b-258">Lorsque la méthode microsoft\\uev: SettingsLocationTemplate Update est appelée via WMI</span><span class="sxs-lookup"><span data-stu-id="9606b-258">When the microsoft\\uev:SettingsLocationTemplate Update method is called through WMI</span></span>

 

### <a href="" id="author21"></a><span data-ttu-id="9606b-259">Élément Author</span><span class="sxs-lookup"><span data-stu-id="9606b-259">Author Element</span></span>

**<span data-ttu-id="9606b-260">Obligatoire: faux</span><span class="sxs-lookup"><span data-stu-id="9606b-260">Mandatory: False</span></span>**

**<span data-ttu-id="9606b-261">Type: chaîne</span><span class="sxs-lookup"><span data-stu-id="9606b-261">Type: String</span></span>**

<span data-ttu-id="9606b-262">Auteur identifie le créateur du modèle d’emplacement des paramètres.</span><span class="sxs-lookup"><span data-stu-id="9606b-262">Author identifies the creator of the settings location template.</span></span> <span data-ttu-id="9606b-263">Deux éléments enfants facultatifs sont pris en charge: **nom** et **adresse de messagerie**.</span><span class="sxs-lookup"><span data-stu-id="9606b-263">Two optional child elements are supported: **Name** and **Email**.</span></span> <span data-ttu-id="9606b-264">Les deux attributs sont facultatifs, mais si l’élément enfant de l’élément email est spécifié, il doit être accompagné du nom de l’élément.</span><span class="sxs-lookup"><span data-stu-id="9606b-264">Both attributes are optional, but, if the Email child element is specified, it must be accompanied by the Name element.</span></span> <span data-ttu-id="9606b-265">Auteur fait référence au nom complet du contact pour le modèle d’emplacement des paramètres et la messagerie doit désigner une adresse de messagerie de l’auteur.</span><span class="sxs-lookup"><span data-stu-id="9606b-265">Author refers to the full name of the contact for the settings location template, and email should refer to an email address for the author.</span></span> <span data-ttu-id="9606b-266">Nous vous recommandons d’inclure ces informations dans les modèles publiés publiquement (par exemple, dans la [Galerie de modèles UE-V](https://gallery.technet.microsoft.com/site/search?f%5B0%5D.Type=RootCategory&f%5B0%5D.Value=UE-V)).</span><span class="sxs-lookup"><span data-stu-id="9606b-266">We recommend that you include this information in templates published publicly, for example, on the [UE-V Template Gallery](https://gallery.technet.microsoft.com/site/search?f%5B0%5D.Type=RootCategory&f%5B0%5D.Value=UE-V).</span></span>

### <a href="" id="processes21"></a><span data-ttu-id="9606b-267">Processus et élément de processus</span><span class="sxs-lookup"><span data-stu-id="9606b-267">Processes and Process Element</span></span>

**<span data-ttu-id="9606b-268">Obligatoire: vrai</span><span class="sxs-lookup"><span data-stu-id="9606b-268">Mandatory: True</span></span>**

**<span data-ttu-id="9606b-269">Type: élément</span><span class="sxs-lookup"><span data-stu-id="9606b-269">Type: Element</span></span>**

<span data-ttu-id="9606b-270">Processus contient au moins un `<Process>` élément, qui à son tour contient les éléments enfants suivants: **filename**, **architecture**, **ProductName**, **FileDescription**, **ProductVersion**et **FileVersion**.</span><span class="sxs-lookup"><span data-stu-id="9606b-270">Processes contains at least one `<Process>` element, which in turn contains the following child elements: **Filename**, **Architecture**, **ProductName**, **FileDescription**, **ProductVersion**, and **FileVersion**.</span></span> <span data-ttu-id="9606b-271">L’élément enfant de nom de fichier est obligatoire et les autres sont facultatifs.</span><span class="sxs-lookup"><span data-stu-id="9606b-271">The Filename child element is mandatory and the others are optional.</span></span> <span data-ttu-id="9606b-272">Un élément complet contient des balises similaires à ce qui suit:</span><span class="sxs-lookup"><span data-stu-id="9606b-272">A fully populated element contains tags similar to this example:</span></span>

```xml
<Process>
  <Filename>MyApplication.exe</Filename>
  <Architecture>Win64</Architecture>
  <ProductName> MyApplication </ProductName>
  <FileDescription>MyApplication.exe</FileDescription>
  <ProductVersion>
    <Major Minimum="2" Maximum="2" />
    <Minor Minimum="0" Maximum="0" />
    <Build Minimum="0" Maximum="0" />
    <Patch Minimum="5" Maximum="5" />
  </ProductVersion>
  <FileVersion>
    <Major Minimum="2" Maximum="2" />
    <Minor Minimum="0" Maximum="0" />
    <Build Minimum="0" Maximum="0" />
    <Patch Minimum="5" Maximum="5" />
  </FileVersion>
</Process>
```

### <span data-ttu-id="9606b-273">Courts</span><span class="sxs-lookup"><span data-stu-id="9606b-273">Filename</span></span>

**<span data-ttu-id="9606b-274">Obligatoire: vrai</span><span class="sxs-lookup"><span data-stu-id="9606b-274">Mandatory: True</span></span>**

**<span data-ttu-id="9606b-275">Type: chaîne</span><span class="sxs-lookup"><span data-stu-id="9606b-275">Type: String</span></span>**

<span data-ttu-id="9606b-276">Nom de fichier correspond au nom de fichier réel de l’exécutable tel qu’il apparaît dans le système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="9606b-276">Filename refers to the actual file name of the executable as it appears in the file system.</span></span> <span data-ttu-id="9606b-277">Cet élément spécifie le critère principal utilisé par UE-V pour déterminer si un modèle s’applique à un processus ou non.</span><span class="sxs-lookup"><span data-stu-id="9606b-277">This element specifies the primary criterion that UE-V uses to evaluate whether a template applies to a process or not.</span></span> <span data-ttu-id="9606b-278">Cet élément doit être spécifié dans le fichier XML du modèle d’emplacement des paramètres.</span><span class="sxs-lookup"><span data-stu-id="9606b-278">This element must be specified in the settings location template XML.</span></span>

<span data-ttu-id="9606b-279">Les noms de fichier valides ne doivent pas correspondre à l’expression régulière \ [^ \ \ \ \ \ \? &lt; &gt; /: \] +, autrement dit, ils ne peuvent pas contenir de caractères de barre oblique inverse, d’astérisque ou de point d’interrogation, de caractère de barre oblique, de signe supérieur ou inférieur</span><span class="sxs-lookup"><span data-stu-id="9606b-279">Valid filenames must not match the regular expression \[^\\\\\\?\\\*\\|&lt;&gt;/:\]+, that is, they may not contain backslash characters, asterisk or question mark wild-card characters, the pipe character, the greater than or less than sign, forward slash, or colon (the \\ ?</span></span> <span data-ttu-id="9606b-280">\* | &lt; &gt; /ou: caractères.).</span><span class="sxs-lookup"><span data-stu-id="9606b-280">\* | &lt; &gt; / or : characters.).</span></span>

<span data-ttu-id="9606b-281">**Astuce:** Pour tester une chaîne par rapport à cette expression régulière, utilisez une fenêtre de commande PowerShell et remplacez le nom de votre exécutable par **YourFileName**:</span><span class="sxs-lookup"><span data-stu-id="9606b-281">**Hint:** To test a string against this regex, use a PowerShell command window and substitute your executable’s name for **YourFileName**:</span></span>

`"YourFileName.exe" -match  "[\\\?\*\|<>/:]+"`

<span data-ttu-id="9606b-282">La valeur **true** indique que la chaîne contient des caractères non valides.</span><span class="sxs-lookup"><span data-stu-id="9606b-282">A value of **True** indicates that the string contains illegal characters.</span></span> <span data-ttu-id="9606b-283">Voici quelques exemples de valeurs non valides:</span><span class="sxs-lookup"><span data-stu-id="9606b-283">Here are some examples of illegal values:</span></span>

-   <span data-ttu-id="9606b-284">\\\\server\\share\\program.exe</span><span class="sxs-lookup"><span data-stu-id="9606b-284">\\\\server\\share\\program.exe</span></span>

-   <span data-ttu-id="9606b-285">Programme \ \*. exe</span><span class="sxs-lookup"><span data-stu-id="9606b-285">Program\*.exe</span></span>

-   <span data-ttu-id="9606b-286">Pro? ram.exe</span><span class="sxs-lookup"><span data-stu-id="9606b-286">Pro?ram.exe</span></span>

-   <span data-ttu-id="9606b-287">Programme &lt; 1 &gt; . exe</span><span class="sxs-lookup"><span data-stu-id="9606b-287">Program&lt;1&gt;.exe</span></span>

<span data-ttu-id="9606b-288">**Remarques**  Le générateur UE-V encode les caractères supérieur et inférieur, comme &gt; et &lt; respectivement.</span><span class="sxs-lookup"><span data-stu-id="9606b-288">**Note** The UE-V Generator encodes the greater than and less than characters as &gt; and &lt; respectively.</span></span>

 

<span data-ttu-id="9606b-289">Dans de rares cas, la valeur FileName n’inclura pas nécessairement l’extension. exe, mais elle doit être spécifiée dans le cadre de la valeur.</span><span class="sxs-lookup"><span data-stu-id="9606b-289">In rare circumstances, the FileName value will not necessarily include the .exe extension, but it should be specified as part of the value.</span></span> <span data-ttu-id="9606b-290">Par exemple, `<Filename>MyApplictication.exe</Filename>` doit être spécifié au lieu de `<Filename>MyApplictication</Filename>` .</span><span class="sxs-lookup"><span data-stu-id="9606b-290">For example, `<Filename>MyApplictication.exe</Filename>` should be specified instead of `<Filename>MyApplictication</Filename>`.</span></span> <span data-ttu-id="9606b-291">Le second exemple n’applique pas le modèle au processus si le véritable nom du fichier exécutable est «MyApplication.exe».</span><span class="sxs-lookup"><span data-stu-id="9606b-291">The second example will not apply the template to the process if the actual name of the executable file is “MyApplication.exe”.</span></span>

### <span data-ttu-id="9606b-292">Architecture</span><span class="sxs-lookup"><span data-stu-id="9606b-292">Architecture</span></span>

**<span data-ttu-id="9606b-293">Obligatoire: faux</span><span class="sxs-lookup"><span data-stu-id="9606b-293">Mandatory: False</span></span>**

**<span data-ttu-id="9606b-294">Type: architecture (chaîne)</span><span class="sxs-lookup"><span data-stu-id="9606b-294">Type: Architecture (String)</span></span>**

<span data-ttu-id="9606b-295">Architecture fait référence à l’architecture de processeur pour laquelle l’exécutable cible a été compilé.</span><span class="sxs-lookup"><span data-stu-id="9606b-295">Architecture refers to the processor architecture for which the target executable was compiled.</span></span> <span data-ttu-id="9606b-296">Les valeurs valides sont Win32 pour les applications 32 bits ou Win64 pour les applications 64 bits.</span><span class="sxs-lookup"><span data-stu-id="9606b-296">Valid values are Win32 for 32-bit applications or Win64 for 64-bit applications.</span></span> <span data-ttu-id="9606b-297">Le cas échéant, cette balise limite l’applicabilité du modèle d’emplacement des paramètres à une architecture d’application particulière.</span><span class="sxs-lookup"><span data-stu-id="9606b-297">If present, this tag limits the applicability of the settings location template to a particular application architecture.</span></span> <span data-ttu-id="9606b-298">Pour obtenir un exemple, comparez l’utilisation de l’interface utilisateur%ProgramFiles%\\Microsoft MicrosoftOffice2010Win32.xml Virtualization\\templates\\ MicrosoftOffice2010Win64.xml et les fichiers inclus avec UE-V.</span><span class="sxs-lookup"><span data-stu-id="9606b-298">For an example of this, compare the %ProgramFiles%\\Microsoft User Experience Virtualization\\templates\\ MicrosoftOffice2010Win32.xml and MicrosoftOffice2010Win64.xml files included with UE-V.</span></span> <span data-ttu-id="9606b-299">Cette fonctionnalité est utile lorsque des chemins relatifs changent entre différentes versions d’un fichier exécutable ou si des paramètres ont été ajoutés ou supprimés lors du passage d’une architecture de processeur à une autre.</span><span class="sxs-lookup"><span data-stu-id="9606b-299">This is useful when relative paths change between different versions of an executable or if settings have been added or removed when moving from one processor architecture to another.</span></span>

<span data-ttu-id="9606b-300">Si cet élément est absent, le modèle d’emplacement des paramètres ignore l’architecture du processus et s’applique aux processus 32 et 64 bits en cas d’application du nom de fichier et d’autres attributs.</span><span class="sxs-lookup"><span data-stu-id="9606b-300">If this element is absent, the settings location template ignores the process’ architecture and applies to both 32 and 64-bit processes if the file name and other attributes apply.</span></span>

<span data-ttu-id="9606b-301">**Remarques**  UE-V ne prend pas en charge les processeurs ARM dans cette version.</span><span class="sxs-lookup"><span data-stu-id="9606b-301">**Note** UE-V does not support ARM processors in this version.</span></span>

 

### <span data-ttu-id="9606b-302">ProductName</span><span class="sxs-lookup"><span data-stu-id="9606b-302">ProductName</span></span>

**<span data-ttu-id="9606b-303">Obligatoire: faux</span><span class="sxs-lookup"><span data-stu-id="9606b-303">Mandatory: False</span></span>**

**<span data-ttu-id="9606b-304">Type: chaîne</span><span class="sxs-lookup"><span data-stu-id="9606b-304">Type: String</span></span>**

<span data-ttu-id="9606b-305">ProductName est un élément facultatif utilisé pour identifier un produit à des fins d’administration ou de création de rapports.</span><span class="sxs-lookup"><span data-stu-id="9606b-305">ProductName is an optional element used to identify a product for administrative purposes or reporting.</span></span> <span data-ttu-id="9606b-306">ProductName est différent du nom de fichier, car il n’y a pas de restrictions d’expression régulières sur sa valeur.</span><span class="sxs-lookup"><span data-stu-id="9606b-306">ProductName differs from Filename in that there are no regular expression restrictions on its value.</span></span> <span data-ttu-id="9606b-307">Cela permet d’obtenir des descriptions plus faciles à comprendre du processus pour lequel le nom exécutable n’est pas évident.</span><span class="sxs-lookup"><span data-stu-id="9606b-307">This allows for more easily understood descriptions of a process where the executable name may not be obvious.</span></span> <span data-ttu-id="9606b-308">Exemple:</span><span class="sxs-lookup"><span data-stu-id="9606b-308">For example:</span></span>

```xml
<Process>
  <Filename>MyApplication.exe</Filename>
  <ProductName>My Application 6.x by Contoso.com</ProductName>
  <ProductVersion>
    <Major Minimum="6" Maximum="6" />
  </ProductVersion>
</Process>
```

### <span data-ttu-id="9606b-309">FileDescription</span><span class="sxs-lookup"><span data-stu-id="9606b-309">FileDescription</span></span>

**<span data-ttu-id="9606b-310">Obligatoire: faux</span><span class="sxs-lookup"><span data-stu-id="9606b-310">Mandatory: False</span></span>**

**<span data-ttu-id="9606b-311">Type: chaîne</span><span class="sxs-lookup"><span data-stu-id="9606b-311">Type: String</span></span>**

<span data-ttu-id="9606b-312">FileDescription est une balise facultative qui permet d’obtenir une description administrative du fichier exécutable.</span><span class="sxs-lookup"><span data-stu-id="9606b-312">FileDescription is an optional tag that allows for an administrative description of the executable file.</span></span> <span data-ttu-id="9606b-313">Il s’agit d’un champ de texte libre qui peut être utile dans le cas d’un package logiciel permettant d’identifier la fonction du fichier exécutable.</span><span class="sxs-lookup"><span data-stu-id="9606b-313">This is a free text field and can be useful in distinguishing multiple executables within a software package where there is a need to identify the function of the executable.</span></span>

<span data-ttu-id="9606b-314">Par exemple, dans une application adaptée, il peut être utile de fournir des rappels sur la fonction de deux exécutables (MyApplication.exe et MyApplicationHelper.exe), comme illustré ci-dessous:</span><span class="sxs-lookup"><span data-stu-id="9606b-314">For example, in a suited application, it might be useful to provide reminders about the function of two executables (MyApplication.exe and MyApplicationHelper.exe), as shown here:</span></span>

```xml
<Processes>
  <Process>
    <Filename>MyApplication.exe</Filename>
    <FileDescription>My Application Main Engine</ FileDescription>
    <ProductVersion>
      <Major Minimum="6" Maximum="6" />
    </ProductVersion>
  </Process>
  <Process>
    <Filename>MyApplicationHelper.exe</Filename>
    <FileDescription>My Application Background Process Executable</FileDescription>
    <ProductVersion>
      <Major Minimum="6" Maximum="6" />
    </ProductVersion>
  </Process>
</Processes>
```

### <span data-ttu-id="9606b-315">ProductVersion</span><span class="sxs-lookup"><span data-stu-id="9606b-315">ProductVersion</span></span>

**<span data-ttu-id="9606b-316">Obligatoire: faux</span><span class="sxs-lookup"><span data-stu-id="9606b-316">Mandatory: False</span></span>**

**<span data-ttu-id="9606b-317">Type: chaîne</span><span class="sxs-lookup"><span data-stu-id="9606b-317">Type: String</span></span>**

<span data-ttu-id="9606b-318">ProductVersion fait référence aux versions de produit principales et secondaires d’un fichier, ainsi qu’à un niveau de build et de correctif.</span><span class="sxs-lookup"><span data-stu-id="9606b-318">ProductVersion refers to the major and minor product versions of a file, as well as a build and patch level.</span></span> <span data-ttu-id="9606b-319">ProductVersion est un élément facultatif, mais si ce paramètre est spécifié, il doit contenir au moins l’élément enfant principal.</span><span class="sxs-lookup"><span data-stu-id="9606b-319">ProductVersion is an optional element, but if specified, it must contain at least the Major child element.</span></span> <span data-ttu-id="9606b-320">La valeur doit exprimer une plage au format minimum = «X» maximum = «Y» où X et Y sont des entiers.</span><span class="sxs-lookup"><span data-stu-id="9606b-320">The value must express a range in the form Minimum="X" Maximum="Y" where X and Y are integers.</span></span> <span data-ttu-id="9606b-321">Les valeurs minimales et maximales peuvent être identiques.</span><span class="sxs-lookup"><span data-stu-id="9606b-321">The Minimum and Maximum values can be identical.</span></span>

<span data-ttu-id="9606b-322">Le produit et les éléments de version du fichier ne sont pas spécifiés.</span><span class="sxs-lookup"><span data-stu-id="9606b-322">The product and file version elements may be left unspecified.</span></span> <span data-ttu-id="9606b-323">Cela rend le modèle «version agnostique», ce qui signifie que le modèle s’appliquera à toutes les versions du fichier exécutable spécifié.</span><span class="sxs-lookup"><span data-stu-id="9606b-323">Doing so makes the template “version agnostic”, meaning that the template will apply to all versions of the specified executable.</span></span>

**<span data-ttu-id="9606b-324">Exemple1:</span><span class="sxs-lookup"><span data-stu-id="9606b-324">Example 1:</span></span>**

<span data-ttu-id="9606b-325">Version du produit: 1,0 spécifiée dans UE-V Generator génère le code XML suivant:</span><span class="sxs-lookup"><span data-stu-id="9606b-325">Product version: 1.0 specified in the UE-V Generator produces the following XML:</span></span>

```xml
<ProductVersion>
  <Major Minimum="1" Maximum="1" />
  <Minor Minimum="0" Maximum="0" />
</ProductVersion>
```

**<span data-ttu-id="9606b-326">Exemple2:</span><span class="sxs-lookup"><span data-stu-id="9606b-326">Example 2:</span></span>**

<span data-ttu-id="9606b-327">Version du fichier: 5.0.2.1000 spécifiée dans UE-V Generator génère le code XML suivant:</span><span class="sxs-lookup"><span data-stu-id="9606b-327">File version: 5.0.2.1000 specified in the UE-V Generator produces the following XML:</span></span>

```xml
<FileVersion>
  <Major Minimum="5" Maximum="5" />
  <Minor Minimum="0" Maximum="0" />
  <Build Minimum="2" Maximum="2" />
  <Patch Minimum="1000" Maximum="1000" />
</FileVersion>
```

**<span data-ttu-id="9606b-328">Exemple incorrect 1 – plage incomplète:</span><span class="sxs-lookup"><span data-stu-id="9606b-328">Incorrect Example 1 – incomplete range:</span></span>**

<span data-ttu-id="9606b-329">Seul l’attribut minimum est présent.</span><span class="sxs-lookup"><span data-stu-id="9606b-329">Only the Minimum attribute is present.</span></span> <span data-ttu-id="9606b-330">La valeur maximale doit également être incluse dans une plage.</span><span class="sxs-lookup"><span data-stu-id="9606b-330">Maximum must be included in a range as well.</span></span>

```xml
<ProductVersion>
  <Major Minimum="2" />
</ProductVersion>
```

**<span data-ttu-id="9606b-331">Exemple 2 incorrect: Minor spécifié sans élément principal:</span><span class="sxs-lookup"><span data-stu-id="9606b-331">Incorrect Example 2 – Minor specified without Major element:</span></span>**

<span data-ttu-id="9606b-332">Seuls les éléments mineurs sont présents.</span><span class="sxs-lookup"><span data-stu-id="9606b-332">Only the Minor element is present.</span></span> <span data-ttu-id="9606b-333">Important doit également être inclus.</span><span class="sxs-lookup"><span data-stu-id="9606b-333">Major must be included as well.</span></span>

```xml
<ProductVersion>
  <Minor Minimum="0" Maximum="0" />
</ProductVersion>
```

### <span data-ttu-id="9606b-334">FileVersion</span><span class="sxs-lookup"><span data-stu-id="9606b-334">FileVersion</span></span>

**<span data-ttu-id="9606b-335">Obligatoire: faux</span><span class="sxs-lookup"><span data-stu-id="9606b-335">Mandatory: False</span></span>**

**<span data-ttu-id="9606b-336">Type: chaîne</span><span class="sxs-lookup"><span data-stu-id="9606b-336">Type: String</span></span>**

<span data-ttu-id="9606b-337">FileVersion fait la distinction entre la version commerciale d’une application publiée et les détails de la build interne d’un composant exécutable.</span><span class="sxs-lookup"><span data-stu-id="9606b-337">FileVersion differentiates between the release version of a published application and the internal build details of a component executable.</span></span> <span data-ttu-id="9606b-338">Ces numéros sont identiques pour la plupart des applications commerciales.</span><span class="sxs-lookup"><span data-stu-id="9606b-338">For the majority of commercial applications, these numbers are identical.</span></span> <span data-ttu-id="9606b-339">Le cas échéant, la version de produit d’un fichier indique une identification de version générique d’un fichier, tandis que la version du fichier indique une version spécifique d’un fichier (comme dans le cas d’un correctif ou d’une mise à jour).</span><span class="sxs-lookup"><span data-stu-id="9606b-339">Where they vary, the product version of a file indicates a generic version identification of a file, while file version indicates a specific build of a file (as in the case of a hotfix or update).</span></span> <span data-ttu-id="9606b-340">Cela identifie de façon unique les fichiers sans logique de détection de rupture.</span><span class="sxs-lookup"><span data-stu-id="9606b-340">This uniquely identifies files without breaking detection logic.</span></span>

<span data-ttu-id="9606b-341">Pour déterminer la version et la version du produit d’un fichier exécutable particulier, cliquez avec le bouton droit sur le fichier dans l’Explorateur Windows, sélectionnez Propriétés, puis cliquez sur l’onglet Détails.</span><span class="sxs-lookup"><span data-stu-id="9606b-341">To determine the product version and file version of a particular executable, right-click on the file in Windows Explorer, select Properties, then click on the Details tab.</span></span>

<span data-ttu-id="9606b-342">L’inclusion d’un élément FileVersion pour une application permet d’améliorer la logique de détection, mais n’est pas nécessaire pour la plupart des applications.</span><span class="sxs-lookup"><span data-stu-id="9606b-342">Including a FileVersion element for an application allows for more granular fine-tuning detection logic, but is not necessary for most applications.</span></span> <span data-ttu-id="9606b-343">Les paramètres de l’élément ProductVersion sont vérifiés en premier, puis FileVersion est activé.</span><span class="sxs-lookup"><span data-stu-id="9606b-343">The ProductVersion element settings are checked first, and then FileVersion is checked.</span></span> <span data-ttu-id="9606b-344">Le paramètre le plus restrictif s’applique.</span><span class="sxs-lookup"><span data-stu-id="9606b-344">The more restrictive setting will apply.</span></span>

<span data-ttu-id="9606b-345">Les éléments enfants et les règles de syntaxe pour FileVersion sont identiques à ceux de ProductVersion.</span><span class="sxs-lookup"><span data-stu-id="9606b-345">The child elements and syntax rules for FileVersion are identical to those of ProductVersion.</span></span>

```xml
<Process>
  <Filename>MSACCESS.EXE</Filename>
  <Architecture>Win32</Architecture>
  <ProductVersion>
    <Major Minimum="14" Maximum="14" />
    <Minor Minimum="0" Maximum="0" />
  </ProductVersion>
  <FileVersion>
    <Major Minimum="14" Maximum="14" />
    <Minor Minimum="0" Maximum="0" />
  </FileVersion>
</Process>
```

### <a href="" id="application21"></a><span data-ttu-id="9606b-346">Élément application</span><span class="sxs-lookup"><span data-stu-id="9606b-346">Application Element</span></span>

<span data-ttu-id="9606b-347">Application est un conteneur pour les paramètres qui s’appliquent à une application particulière.</span><span class="sxs-lookup"><span data-stu-id="9606b-347">Application is a container for settings that apply to a particular application.</span></span> <span data-ttu-id="9606b-348">Il s’agit d’un ensemble de champs/types suivants.</span><span class="sxs-lookup"><span data-stu-id="9606b-348">It is a collection of the following fields/types.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="9606b-349">Champ/type</span><span class="sxs-lookup"><span data-stu-id="9606b-349">Field/Type</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="9606b-350">Description</span><span class="sxs-lookup"><span data-stu-id="9606b-350">Description</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9606b-351">Name</span><span class="sxs-lookup"><span data-stu-id="9606b-351">Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="9606b-352">Spécifie un nom unique pour le modèle d’emplacement des paramètres.</span><span class="sxs-lookup"><span data-stu-id="9606b-352">Specifies a unique name for the settings location template.</span></span> <span data-ttu-id="9606b-353">Il est utilisé à des fins d’affichage lors du référencement du modèle dans WMI, PowerShell, Observateur d’événements et journaux de débogage.</span><span class="sxs-lookup"><span data-stu-id="9606b-353">This is used for display purposes when referencing the template in WMI, PowerShell, Event Viewer and debug logs.</span></span> <span data-ttu-id="9606b-354">Pour plus d’informations, reportez-vous à la section <a href="#name21" data-raw-source="[Name](#name21)"> nom </a> .</span><span class="sxs-lookup"><span data-stu-id="9606b-354">For more information, see <a href="#name21" data-raw-source="[Name](#name21)">Name</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9606b-355">ID</span><span class="sxs-lookup"><span data-stu-id="9606b-355">ID</span></span></p></td>
<td align="left"><p><span data-ttu-id="9606b-356">Remplit un identificateur unique pour un modèle particulier.</span><span class="sxs-lookup"><span data-stu-id="9606b-356">Populates a unique identifier for a particular template.</span></span> <span data-ttu-id="9606b-357">Cette balise devient l’identificateur principal utilisé par l’agent UE-V pour référencer le modèle lors de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="9606b-357">This tag becomes the primary identifier that the UE-V Agent uses to reference the template at runtime.</span></span> <span data-ttu-id="9606b-358">Pour plus d’informations, consultez la section <a href="#id21" data-raw-source="[ID](#id21)"> ID </a> .</span><span class="sxs-lookup"><span data-stu-id="9606b-358">For more information, see <a href="#id21" data-raw-source="[ID](#id21)">ID</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9606b-359">Description</span><span class="sxs-lookup"><span data-stu-id="9606b-359">Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="9606b-360">Description facultative du modèle.</span><span class="sxs-lookup"><span data-stu-id="9606b-360">An optional description of the template.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9606b-361">LocalizedNames</span><span class="sxs-lookup"><span data-stu-id="9606b-361">LocalizedNames</span></span></p></td>
<td align="left"><p><span data-ttu-id="9606b-362">Nom facultatif affiché dans l’interface utilisateur, localisé par des paramètres régionaux de langue.</span><span class="sxs-lookup"><span data-stu-id="9606b-362">An optional name displayed in the UI, localized by a language locale.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9606b-363">LocalizedDescriptions</span><span class="sxs-lookup"><span data-stu-id="9606b-363">LocalizedDescriptions</span></span></p></td>
<td align="left"><p><span data-ttu-id="9606b-364">Description de modèle facultative localisée par un paramètre régional de langue.</span><span class="sxs-lookup"><span data-stu-id="9606b-364">An optional template description localized by a language locale.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9606b-365">Version</span><span class="sxs-lookup"><span data-stu-id="9606b-365">Version</span></span></p></td>
<td align="left"><p><span data-ttu-id="9606b-366">Identifie la version du modèle d’emplacement des paramètres du suivi des modifications.</span><span class="sxs-lookup"><span data-stu-id="9606b-366">Identifies the version of the settings location template for administrative tracking of changes.</span></span> <span data-ttu-id="9606b-367">Pour plus d’informations, voir <a href="#version21" data-raw-source="[Version](#version21)"> version </a> .</span><span class="sxs-lookup"><span data-stu-id="9606b-367">For more information, see <a href="#version21" data-raw-source="[Version](#version21)">Version</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9606b-368">DeferToMSAccount</span><span class="sxs-lookup"><span data-stu-id="9606b-368">DeferToMSAccount</span></span></p></td>
<td align="left"><p><span data-ttu-id="9606b-369">Détermine si ce modèle est activé en conjonction avec un compte Microsoft.</span><span class="sxs-lookup"><span data-stu-id="9606b-369">Controls whether this template is enabled in conjunction with a Microsoft account or not.</span></span> <span data-ttu-id="9606b-370">Si la synchronisation MSA est activée pour un utilisateur sur un ordinateur, ce modèle sera automatiquement désactivé.</span><span class="sxs-lookup"><span data-stu-id="9606b-370">If MSA syncing is enabled for a user on a machine, then this template will automatically be disabled.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9606b-371">DeferToOffice365</span><span class="sxs-lookup"><span data-stu-id="9606b-371">DeferToOffice365</span></span></p></td>
<td align="left"><p><span data-ttu-id="9606b-372">Comme pour MSA, cette option détermine si ce modèle est activé en conjonction avec Office 365.</span><span class="sxs-lookup"><span data-stu-id="9606b-372">Similar to MSA, this controls whether this template is enabled in conjunction with Office365.</span></span> <span data-ttu-id="9606b-373">Si Office 365 est utilisé pour synchroniser les paramètres, ce modèle sera automatiquement désactivé.</span><span class="sxs-lookup"><span data-stu-id="9606b-373">If Office 365 is being used to sync settings, this template will automatically be disabled.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9606b-374">FixedProfile (introduite dans 2,1)</span><span class="sxs-lookup"><span data-stu-id="9606b-374">FixedProfile (Introduced in 2.1)</span></span></p></td>
<td align="left"><p><span data-ttu-id="9606b-375">Spécifie que ce modèle peut uniquement être associé au profil spécifié dans cet élément et ne peut pas être modifié via WMI ou PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9606b-375">Specifies that this template can only be associated with the profile specified within this element, and cannot be changed via WMI or PowerShell.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9606b-376">Processus</span><span class="sxs-lookup"><span data-stu-id="9606b-376">Processes</span></span></p></td>
<td align="left"><p><span data-ttu-id="9606b-377">Conteneur pour une collection d’un ou de plusieurs éléments de processus.</span><span class="sxs-lookup"><span data-stu-id="9606b-377">A container for a collection of one or more Process elements.</span></span> <span data-ttu-id="9606b-378">Pour plus d’informations, reportez-vous à la section <a href="#processes21" data-raw-source="[Processes](#processes21)"> processus </a> .</span><span class="sxs-lookup"><span data-stu-id="9606b-378">For more information, see <a href="#processes21" data-raw-source="[Processes](#processes21)">Processes</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9606b-379">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9606b-379">Settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="9606b-380">Conteneur de tous les paramètres qui s’appliquent à un modèle spécifique.</span><span class="sxs-lookup"><span data-stu-id="9606b-380">A container for all the settings that apply to a particular template.</span></span> <span data-ttu-id="9606b-381">Il contient des instances des paramètres de Registre, de fichier, de SystemParameter et de CustomAction.</span><span class="sxs-lookup"><span data-stu-id="9606b-381">It contains instances of the Registry, File, SystemParameter, and CustomAction settings.</span></span> <span data-ttu-id="9606b-382">Pour plus d’informations, consultez la section <strong> paramètres </strong> des <a href="#data21" data-raw-source="[Data types](#data21)"> types de données </a> .</span><span class="sxs-lookup"><span data-stu-id="9606b-382">For more information, see <strong>Settings</strong> in <a href="#data21" data-raw-source="[Data types](#data21)">Data types</a>.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="common21"></a><span data-ttu-id="9606b-383">Élément commun</span><span class="sxs-lookup"><span data-stu-id="9606b-383">Common Element</span></span>

<span data-ttu-id="9606b-384">Common est semblable à un élément application, mais il est toujours associé à deux éléments d’application ou davantage.</span><span class="sxs-lookup"><span data-stu-id="9606b-384">Common is similar to an Application element, but it is always associated with two or more Application elements.</span></span> <span data-ttu-id="9606b-385">La section commune représente l’ensemble des paramètres qui sont partagés entre ces instances d’application.</span><span class="sxs-lookup"><span data-stu-id="9606b-385">The Common section represents the set of settings that are shared between those Application instances.</span></span> <span data-ttu-id="9606b-386">Il s’agit d’un ensemble de champs/types suivants.</span><span class="sxs-lookup"><span data-stu-id="9606b-386">It is a collection of the following fields/types.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="9606b-387">Champ/type</span><span class="sxs-lookup"><span data-stu-id="9606b-387">Field/Type</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="9606b-388">Description</span><span class="sxs-lookup"><span data-stu-id="9606b-388">Description</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9606b-389">Name</span><span class="sxs-lookup"><span data-stu-id="9606b-389">Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="9606b-390">Spécifie un nom unique pour le modèle d’emplacement des paramètres.</span><span class="sxs-lookup"><span data-stu-id="9606b-390">Specifies a unique name for the settings location template.</span></span> <span data-ttu-id="9606b-391">Il est utilisé à des fins d’affichage lors du référencement du modèle dans WMI, PowerShell, Observateur d’événements et journaux de débogage.</span><span class="sxs-lookup"><span data-stu-id="9606b-391">This is used for display purposes when referencing the template in WMI, PowerShell, Event Viewer and debug logs.</span></span> <span data-ttu-id="9606b-392">Pour plus d’informations, reportez-vous à la section <a href="#name21" data-raw-source="[Name](#name21)"> nom </a> .</span><span class="sxs-lookup"><span data-stu-id="9606b-392">For more information, see <a href="#name21" data-raw-source="[Name](#name21)">Name</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9606b-393">ID</span><span class="sxs-lookup"><span data-stu-id="9606b-393">ID</span></span></p></td>
<td align="left"><p><span data-ttu-id="9606b-394">Remplit un identificateur unique pour un modèle particulier.</span><span class="sxs-lookup"><span data-stu-id="9606b-394">Populates a unique identifier for a particular template.</span></span> <span data-ttu-id="9606b-395">Cette balise devient l’identificateur principal utilisé par l’agent UE-V pour référencer le modèle lors de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="9606b-395">This tag becomes the primary identifier that the UE-V Agent uses to reference the template at runtime.</span></span> <span data-ttu-id="9606b-396">Pour plus d’informations, consultez la section <a href="#id21" data-raw-source="[ID](#id21)"> ID </a> .</span><span class="sxs-lookup"><span data-stu-id="9606b-396">For more information, see <a href="#id21" data-raw-source="[ID](#id21)">ID</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9606b-397">Description</span><span class="sxs-lookup"><span data-stu-id="9606b-397">Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="9606b-398">Description facultative du modèle.</span><span class="sxs-lookup"><span data-stu-id="9606b-398">An optional description of the template.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9606b-399">LocalizedNames</span><span class="sxs-lookup"><span data-stu-id="9606b-399">LocalizedNames</span></span></p></td>
<td align="left"><p><span data-ttu-id="9606b-400">Nom facultatif affiché dans l’interface utilisateur, localisé par des paramètres régionaux de langue.</span><span class="sxs-lookup"><span data-stu-id="9606b-400">An optional name displayed in the UI, localized by a language locale.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9606b-401">LocalizedDescriptions</span><span class="sxs-lookup"><span data-stu-id="9606b-401">LocalizedDescriptions</span></span></p></td>
<td align="left"><p><span data-ttu-id="9606b-402">Description de modèle facultative localisée par un paramètre régional de langue.</span><span class="sxs-lookup"><span data-stu-id="9606b-402">An optional template description localized by a language locale.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9606b-403">Version</span><span class="sxs-lookup"><span data-stu-id="9606b-403">Version</span></span></p></td>
<td align="left"><p><span data-ttu-id="9606b-404">Identifie la version du modèle d’emplacement des paramètres du suivi des modifications.</span><span class="sxs-lookup"><span data-stu-id="9606b-404">Identifies the version of the settings location template for administrative tracking of changes.</span></span> <span data-ttu-id="9606b-405">Pour plus d’informations, voir <a href="#version21" data-raw-source="[Version](#version21)"> version </a> .</span><span class="sxs-lookup"><span data-stu-id="9606b-405">For more information, see <a href="#version21" data-raw-source="[Version](#version21)">Version</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9606b-406">DeferToMSAccount</span><span class="sxs-lookup"><span data-stu-id="9606b-406">DeferToMSAccount</span></span></p></td>
<td align="left"><p><span data-ttu-id="9606b-407">Détermine si ce modèle est activé en conjonction avec un compte Microsoft.</span><span class="sxs-lookup"><span data-stu-id="9606b-407">Controls whether this template is enabled in conjunction with a Microsoft account or not.</span></span> <span data-ttu-id="9606b-408">Si la synchronisation MSA est activée pour un utilisateur sur un ordinateur, ce modèle sera automatiquement désactivé.</span><span class="sxs-lookup"><span data-stu-id="9606b-408">If MSA syncing is enabled for a user on a machine, then this template will automatically be disabled.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9606b-409">DeferToOffice365</span><span class="sxs-lookup"><span data-stu-id="9606b-409">DeferToOffice365</span></span></p></td>
<td align="left"><p><span data-ttu-id="9606b-410">Comme pour MSA, cette option détermine si ce modèle est activé en conjonction avec Office 365.</span><span class="sxs-lookup"><span data-stu-id="9606b-410">Similar to MSA, this controls whether this template is enabled in conjunction with Office365.</span></span> <span data-ttu-id="9606b-411">Si Office 365 est utilisé pour synchroniser les paramètres, ce modèle sera automatiquement désactivé.</span><span class="sxs-lookup"><span data-stu-id="9606b-411">If Office 365 is being used to sync settings, this template will automatically be disabled.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9606b-412">FixedProfile (introduite dans 2,1)</span><span class="sxs-lookup"><span data-stu-id="9606b-412">FixedProfile (Introduced in 2.1)</span></span></p></td>
<td align="left"><p><span data-ttu-id="9606b-413">Spécifie que ce modèle peut uniquement être associé au profil spécifié dans cet élément et ne peut pas être modifié via WMI ou PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9606b-413">Specifies that this template can only be associated with the profile specified within this element, and cannot be changed via WMI or PowerShell.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9606b-414">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9606b-414">Settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="9606b-415">Conteneur de tous les paramètres qui s’appliquent à un modèle spécifique.</span><span class="sxs-lookup"><span data-stu-id="9606b-415">A container for all the settings that apply to a particular template.</span></span> <span data-ttu-id="9606b-416">Il contient des instances des paramètres de Registre, de fichier, de SystemParameter et de CustomAction.</span><span class="sxs-lookup"><span data-stu-id="9606b-416">It contains instances of the Registry, File, SystemParameter, and CustomAction settings.</span></span> <span data-ttu-id="9606b-417">Pour plus d’informations, consultez la section <strong> paramètres </strong> des <a href="#data21" data-raw-source="[Data types](#data21)"> types de données </a> .</span><span class="sxs-lookup"><span data-stu-id="9606b-417">For more information, see <strong>Settings</strong> in <a href="#data21" data-raw-source="[Data types](#data21)">Data types</a>.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="settingslocationtemplate21"></a><span data-ttu-id="9606b-418">Élément SettingsLocationTemplate</span><span class="sxs-lookup"><span data-stu-id="9606b-418">SettingsLocationTemplate Element</span></span>

<span data-ttu-id="9606b-419">Cet élément définit les paramètres d’une application unique ou d’une suite d’applications.</span><span class="sxs-lookup"><span data-stu-id="9606b-419">This element defines the settings for a single application or a suite of applications.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="9606b-420">Champ/type</span><span class="sxs-lookup"><span data-stu-id="9606b-420">Field/Type</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="9606b-421">Description</span><span class="sxs-lookup"><span data-stu-id="9606b-421">Description</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9606b-422">Name</span><span class="sxs-lookup"><span data-stu-id="9606b-422">Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="9606b-423">Spécifie un nom unique pour le modèle d’emplacement des paramètres.</span><span class="sxs-lookup"><span data-stu-id="9606b-423">Specifies a unique name for the settings location template.</span></span> <span data-ttu-id="9606b-424">Il est utilisé à des fins d’affichage lors du référencement du modèle dans WMI, PowerShell, Observateur d’événements et journaux de débogage.</span><span class="sxs-lookup"><span data-stu-id="9606b-424">This is used for display purposes when referencing the template in WMI, PowerShell, Event Viewer and debug logs.</span></span> <span data-ttu-id="9606b-425">Pour plus d’informations, reportez-vous à la section <a href="#name21" data-raw-source="[Name](#name21)"> nom </a> .</span><span class="sxs-lookup"><span data-stu-id="9606b-425">For more information, see <a href="#name21" data-raw-source="[Name](#name21)">Name</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9606b-426">ID</span><span class="sxs-lookup"><span data-stu-id="9606b-426">ID</span></span></p></td>
<td align="left"><p><span data-ttu-id="9606b-427">Remplit un identificateur unique pour un modèle particulier.</span><span class="sxs-lookup"><span data-stu-id="9606b-427">Populates a unique identifier for a particular template.</span></span> <span data-ttu-id="9606b-428">Cette balise devient l’identificateur principal utilisé par l’agent UE-V pour référencer le modèle lors de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="9606b-428">This tag becomes the primary identifier that the UE-V Agent uses to reference the template at runtime.</span></span> <span data-ttu-id="9606b-429">Pour plus d’informations, consultez la section <a href="#id21" data-raw-source="[ID](#id21)"> ID </a> .</span><span class="sxs-lookup"><span data-stu-id="9606b-429">For more information, see <a href="#id21" data-raw-source="[ID](#id21)">ID</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9606b-430">Description</span><span class="sxs-lookup"><span data-stu-id="9606b-430">Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="9606b-431">Description facultative du modèle.</span><span class="sxs-lookup"><span data-stu-id="9606b-431">An optional description of the template.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9606b-432">LocalizedNames</span><span class="sxs-lookup"><span data-stu-id="9606b-432">LocalizedNames</span></span></p></td>
<td align="left"><p><span data-ttu-id="9606b-433">Nom facultatif affiché dans l’interface utilisateur, localisé par des paramètres régionaux de langue.</span><span class="sxs-lookup"><span data-stu-id="9606b-433">An optional name displayed in the UI, localized by a language locale.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9606b-434">LocalizedDescriptions</span><span class="sxs-lookup"><span data-stu-id="9606b-434">LocalizedDescriptions</span></span></p></td>
<td align="left"><p><span data-ttu-id="9606b-435">Description de modèle facultative localisée par un paramètre régional de langue.</span><span class="sxs-lookup"><span data-stu-id="9606b-435">An optional template description localized by a language locale.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="appendix21"></a><span data-ttu-id="9606b-436">Annexe: SettingsLocationTemplate. xsd</span><span class="sxs-lookup"><span data-stu-id="9606b-436">Appendix: SettingsLocationTemplate.xsd</span></span>

<span data-ttu-id="9606b-437">Voici le fichier SettingsLocationTemplate. xsd montrant ses éléments, éléments enfants, attributs et paramètres:</span><span class="sxs-lookup"><span data-stu-id="9606b-437">Here is the SettingsLocationTemplate.xsd file showing its elements, child elements, attributes, and parameters:</span></span>

```xml
<?xml version="1.0" encoding="utf-8"?>
<xs:schema id="UevSettingsLocationTemplate"
  targetNamespace="https://schemas.microsoft.com/UserExperienceVirtualization/2013A/SettingsLocationTemplate"
  elementFormDefault="qualified"
  xmlns="https://schemas.microsoft.com/UserExperienceVirtualization/2013A/SettingsLocationTemplate"
  xmlns:mstns="https://schemas.microsoft.com/UserExperienceVirtualization/2013A/SettingsLocationTemplate"
  xmlns:xs="http://www.w3.org/2001/XMLSchema">

    <xs:simpleType name="Guid">
        <xs:restriction base="xs:string">
            <xs:pattern value="\{[a-fA-F0-9]{8}-[a-fA-F0-9]{4}-[a-fA-F0-9]{4}-[a-fA-F0-9]{4}-[a-fA-F0-9]{12}\}" />
        </xs:restriction>
    </xs:simpleType>

    <xs:simpleType name="FilenameString">
        <xs:restriction base="xs:string">
            <xs:pattern value="[^\\\?\*\|&lt;&gt;/:]+" />
        </xs:restriction>
    </xs:simpleType>

    <xs:simpleType name="IDString">
        <xs:restriction base="xs:string">
            <xs:pattern value="[^\\\?\*\|&lt;&gt;/:.]+" />
        </xs:restriction>
    </xs:simpleType>

    <xs:simpleType name="CompositeIDString">
        <xs:restriction base="xs:string">
            <xs:pattern value="[^\\\?\*\|&lt;&gt;/:.]+([.][^\\\?\*\|&lt;&gt;/:.]+)?" />
        </xs:restriction>
    </xs:simpleType>

    <xs:simpleType name="TemplateVersion">
        <xs:restriction base="xs:integer">
            <xs:minInclusive value="0" />
            <xs:maxInclusive value="2147483647" />
        </xs:restriction>
    </xs:simpleType>

    <xs:complexType name="Empty">
        <xs:sequence/>
    </xs:complexType>

    <xs:complexType name="LocalizedString">
        <xs:simpleContent>
            <xs:extension base="xs:string">
                <xs:attribute name="Locale" type="xs:string" use="required"/>
            </xs:extension>
        </xs:simpleContent>
    </xs:complexType>

    <xs:complexType name="LocalizedName">
        <xs:sequence>
            <xs:element name="Name" type="LocalizedString" minOccurs="1" maxOccurs="unbounded" />
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="LocalizedDescription">
        <xs:sequence>
            <xs:element name="Description" type="LocalizedString" minOccurs="1" maxOccurs="unbounded" />
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="ReplacedTemplates">
      <xs:sequence>
        <xs:element name="ID" type="CompositeIDString" minOccurs="1" maxOccurs="unbounded" />
    </xs:sequence>
    </xs:complexType>

    <xs:complexType name="Author">
        <xs:all>
            <xs:element name="Name" type="xs:string" minOccurs="1" />
            <xs:element name="Email" type="xs:string" minOccurs="0" />
        </xs:all>
    </xs:complexType>

    <xs:complexType name="Range">
        <xs:attribute name="Minimum" type="xs:integer" use="required"/>
        <xs:attribute name="Maximum" type="xs:integer" use="required"/>
    </xs:complexType>

    <xs:complexType name="ProcessVersion">
        <xs:sequence>
            <xs:element name="Major" type="Range" minOccurs="1" />
            <xs:element name="Minor" type="Range" minOccurs="0" />
            <xs:element name="Build" type="Range" minOccurs="0" />
            <xs:element name="Patch" type="Range" minOccurs="0" />
        </xs:sequence>
    </xs:complexType>

    <xs:simpleType name="Architecture">
        <xs:restriction base="xs:string">
            <xs:enumeration value="Win32"/>
            <xs:enumeration value="Win64"/>
        </xs:restriction>
    </xs:simpleType>

    <xs:complexType name="Process">
        <xs:sequence>
            <xs:element name="Filename" type="FilenameString" minOccurs="1" />
            <xs:element name="Architecture" type="Architecture" minOccurs="0" />
            <xs:element name="ProductName" type="xs:string" minOccurs="0" />
            <xs:element name="FileDescription" type="xs:string" minOccurs="0" />
            <xs:element name="ProductVersion" type="ProcessVersion" minOccurs="0" maxOccurs="unbounded"/>
            <xs:element name="FileVersion" type="ProcessVersion" minOccurs="0" maxOccurs="unbounded"/>
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="Processes">
        <xs:sequence>
            <xs:choice minOccurs="1">
                <xs:element name="Process" type="Process" />
                <xs:element name="ShellProcess" type="Empty" />
            </xs:choice>
            <xs:element name="Process" type="Process" minOccurs="0" maxOccurs="unbounded" />
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="Path">
        <xs:simpleContent>
            <xs:extension base="xs:string">
                <xs:attribute name="Recursive" type="xs:boolean" default="false"/>
                <xs:attribute name="DeleteIfNotFound" type="xs:boolean" default="false"/>
            </xs:extension>
        </xs:simpleContent>
    </xs:complexType>

    <xs:complexType name="RegistrySetting">
        <xs:sequence>
            <xs:element name="Path" type="Path" />
            <xs:element name="Name" type="xs:string" minOccurs="0" maxOccurs="unbounded" />
            <xs:element name="Exclude" minOccurs="0" maxOccurs="unbounded">
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="Path" type="Path" minOccurs="0" />
                        <xs:element name="Name" type="xs:string" minOccurs="0" maxOccurs="unbounded" />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="FileSetting">
        <xs:sequence>

            <xs:element name="Root">
                <xs:complexType>
                    <xs:choice>
                        <xs:element name="KnownFolder" type="Guid" />
                        <xs:element name="RegistryEntry" type="xs:string" />
                        <xs:element name="EnvironmentVariable" type="xs:string" />
                    </xs:choice>
                </xs:complexType>
            </xs:element>

            <xs:element name="Path" minOccurs="0" type="Path" />
            <xs:element name="FileMask" type="xs:string" minOccurs="0" maxOccurs="unbounded"/>

            <xs:element name="Exclude" minOccurs="0" maxOccurs="unbounded">
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="Path" type="Path" minOccurs="0" />
                        <xs:element name="FileMask" type="xs:string" minOccurs="0" maxOccurs="unbounded" />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>

        </xs:sequence>
    </xs:complexType>

    <xs:simpleType name="CustomActionSetting">
        <xs:restriction base="xs:anyURI"/>
    </xs:simpleType>

    <xs:simpleType name="SystemParameterSetting">
        <xs:restriction base="xs:string">

            <!-- Accessibility parameters -->
            <xs:enumeration value="AccessTimeout"/>
            <xs:enumeration value="AudioDescription"/>
            <xs:enumeration value="ClientAreaAnimation"/>
            <xs:enumeration value="DisableOverlappedContent"/>
            <xs:enumeration value="FilterKeys"/>
            <xs:enumeration value="FocusBorderHeight"/>
            <xs:enumeration value="FocusBorderWidth"/>
            <xs:enumeration value="HighContrast"/>
            <xs:enumeration value="MessageDuration"/>
            <xs:enumeration value="MouseClickLock"/>
            <xs:enumeration value="MouseClickLockTime"/>
            <xs:enumeration value="MouseKeys"/>
            <xs:enumeration value="MouseSonar"/>
            <xs:enumeration value="MouseVanish"/>
            <xs:enumeration value="ScreenReader"/>
            <xs:enumeration value="ShowSounds"/>
            <xs:enumeration value="SoundSentry"/>
            <xs:enumeration value="StickyKeys"/>
            <xs:enumeration value="ToggleKeys"/>

            <!-- Input parameters -->
            <xs:enumeration value="Beep"/>
            <xs:enumeration value="BlockSendInputResets"/>
            <xs:enumeration value="DefaultInputLang"/>
            <xs:enumeration value="DoubleClickTime"/>
            <xs:enumeration value="DoubleClkHeight"/>
            <xs:enumeration value="DoubleClkWidth"/>
            <xs:enumeration value="KeyboardCues"/>
            <xs:enumeration value="KeyboardDelay"/>
            <xs:enumeration value="KeyboardPref"/>
            <xs:enumeration value="KeyboardSpeed"/>
            <xs:enumeration value="Mouse"/>
            <xs:enumeration value="MouseButtonSwap"/>
            <xs:enumeration value="MouseHoverHeight"/>
            <xs:enumeration value="MouseHoverTime"/>
            <xs:enumeration value="MouseHoverWidth"/>
            <xs:enumeration value="MouseSpeed"/>
            <xs:enumeration value="MouseTrails"/>
            <xs:enumeration value="SnapToDefButton"/>
            <xs:enumeration value="WheelScrollChars"/>
            <xs:enumeration value="WheelScrollLines"/>

            <!-- Desktop parameters (limited subset) -->
            <xs:enumeration value="DeskWallpaper"/>
            <xs:enumeration value="DesktopColor"/>

        </xs:restriction>
    </xs:simpleType>

    <xs:complexType name="Settings">
        <xs:sequence>
            <xs:element name="Asynchronous" type="xs:boolean" minOccurs="0" />
            <xs:element name="PreventOverlappingSynchronization" type="xs:boolean" minOccurs="0" />
            <xs:element name="AlwaysApplySettings" type="xs:boolean" minOccurs="0" />
            <xs:choice minOccurs="0" maxOccurs="unbounded">
                <xs:element name="Registry" type="RegistrySetting" />
                <xs:element name="File" type="FileSetting" />
                <xs:element name="SystemParameter" type="SystemParameterSetting" />
                <xs:element name="CustomAction" type="CustomActionSetting" />
            </xs:choice>
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="Common">
        <xs:sequence>
            <xs:element name="Name" type="xs:string" />
            <xs:element name="ID" type="IDString" />
            <xs:element name="ReplacedTemplates" type="ReplacedTemplates" minOccurs="0" />
            <xs:element name="Description" type="xs:string" minOccurs="0" />
            <xs:element name="LocalizedNames" type="LocalizedName" minOccurs="0" />
            <xs:element name="LocalizedDescriptions" type="LocalizedDescription" minOccurs="0" />
            <xs:element name="Version" type="xs:integer" />
            <xs:element name="DeferToMSAccount" type="Empty"  minOccurs="0" />
            <xs:element name="DeferToOffice365" type="Empty" minOccurs="0" />
            <xs:element name="Settings" type="Settings" />
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="Application">
        <xs:sequence>
            <xs:element name="Name" type="xs:string" />
            <xs:element name="ID" type="IDString" />
            <xs:element name="ReplacedTemplates" type="ReplacedTemplates" minOccurs="0" />
            <xs:element name="Description" type="xs:string" minOccurs="0" />
            <xs:element name="LocalizedNames" type="LocalizedName" minOccurs="0" />
            <xs:element name="LocalizedDescriptions" type="LocalizedDescription" minOccurs="0" />
            <xs:element name="Version" type="xs:integer" />
            <xs:element name="DeferToMSAccount" type="Empty"  minOccurs="0" />
            <xs:element name="DeferToOffice365" type="Empty" minOccurs="0" />
            <xs:element name="Processes" type="Processes" />
            <xs:element name="Settings" type="Settings" />
        </xs:sequence>
    </xs:complexType>


    <xs:element name="SettingsLocationTemplate">
        <xs:complexType>
            <xs:sequence>

                <xs:element name="Name" type="xs:string" />
                <xs:element name="ID" type="IDString" />
                <xs:element name="Description" type="xs:string" minOccurs="0" />
                <xs:element name="LocalizedNames" type="LocalizedName" minOccurs="0" />
                <xs:element name="LocalizedDescriptions" type="LocalizedDescription" minOccurs="0" />

                <xs:choice>

                    <!-- Single application -->
                    <xs:sequence>
                        <xs:element name="ReplacedTemplates" type="ReplacedTemplates" minOccurs="0" />
                        <xs:element name="Version" type="TemplateVersion" />
                        <xs:element name="Author" type="Author" minOccurs="0" />
                        <xs:element name="FixedProfile" type="xs:string"  minOccurs="0" />
                        <xs:element name="DeferToMSAccount" type="Empty"  minOccurs="0" />
                        <xs:element name="DeferToOffice365" type="Empty" minOccurs="0" />
                        <xs:element name="Processes" type="Processes" />
                        <xs:element name="Settings" type="Settings" />
                    </xs:sequence>

                    <!-- Suite of applications -->
                    <xs:sequence>
                        <xs:element name="ManageSuiteOnly" type="xs:boolean" minOccurs="0" />
                        <xs:element name="Author" type="Author" minOccurs="0" />
                        <xs:element name="FixedProfile" type="xs:string"  minOccurs="0" />
                        <xs:element name="Common" type="Common" />
                        <xs:element name="Application" type="Application" minOccurs="2" maxOccurs="unbounded" />
                    </xs:sequence>

                </xs:choice>

            </xs:sequence>
        </xs:complexType>
    </xs:element>
    <!-- SettingsLocationTemplate -->

</xs:schema>
```

## <span data-ttu-id="9606b-438">Référence du schéma de modèle d’application UE-V 2,0</span><span class="sxs-lookup"><span data-stu-id="9606b-438">UE-V 2.0 Application Template Schema Reference</span></span>


<span data-ttu-id="9606b-439">Cette section détaille la structure XML du modèle d’emplacement des paramètres d’UE-V 2,0 et fournit des recommandations pour la modification de ce fichier.</span><span class="sxs-lookup"><span data-stu-id="9606b-439">This section details the XML structure of the UE-V 2.0 settings location template and provides guidance for editing this file.</span></span>

### <span data-ttu-id="9606b-440">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="9606b-440">In This Section</span></span>

-   [<span data-ttu-id="9606b-441">Attribut d’encodage et de déclaration XML</span><span class="sxs-lookup"><span data-stu-id="9606b-441">XML Declaration and Encoding Attribute</span></span>](#xml)

-   [<span data-ttu-id="9606b-442">Espace de noms et élément racine</span><span class="sxs-lookup"><span data-stu-id="9606b-442">Namespace and Root Element</span></span>](#namespace)

-   [<span data-ttu-id="9606b-443">Types de données</span><span class="sxs-lookup"><span data-stu-id="9606b-443">Data types</span></span>](#data)

-   [<span data-ttu-id="9606b-444">Élément Name</span><span class="sxs-lookup"><span data-stu-id="9606b-444">Name Element</span></span>](#name)

-   [<span data-ttu-id="9606b-445">Élément ID</span><span class="sxs-lookup"><span data-stu-id="9606b-445">ID Element</span></span>](#id)

-   [<span data-ttu-id="9606b-446">Élément version</span><span class="sxs-lookup"><span data-stu-id="9606b-446">Version Element</span></span>](#version)

-   [<span data-ttu-id="9606b-447">Élément Author</span><span class="sxs-lookup"><span data-stu-id="9606b-447">Author Element</span></span>](#author)

-   [<span data-ttu-id="9606b-448">Processus et élément de processus</span><span class="sxs-lookup"><span data-stu-id="9606b-448">Processes and Process Element</span></span>](#processes)

-   [<span data-ttu-id="9606b-449">Élément application</span><span class="sxs-lookup"><span data-stu-id="9606b-449">Application Element</span></span>](#application)

-   [<span data-ttu-id="9606b-450">Élément commun</span><span class="sxs-lookup"><span data-stu-id="9606b-450">Common Element</span></span>](#common)

-   [<span data-ttu-id="9606b-451">Élément SettingsLocationTemplate</span><span class="sxs-lookup"><span data-stu-id="9606b-451">SettingsLocationTemplate Element</span></span>](#settingslocationtemplate)

-   [<span data-ttu-id="9606b-452">Annexe: SettingsLocationTemplate. xsd</span><span class="sxs-lookup"><span data-stu-id="9606b-452">Appendix: SettingsLocationTemplate.xsd</span></span>](#appendix)

### <a href="" id="xml"></a><span data-ttu-id="9606b-453">Attribut d’encodage et de déclaration XML</span><span class="sxs-lookup"><span data-stu-id="9606b-453">XML Declaration and Encoding Attribute</span></span>

**<span data-ttu-id="9606b-454">Obligatoire: vrai</span><span class="sxs-lookup"><span data-stu-id="9606b-454">Mandatory: True</span></span>**

**<span data-ttu-id="9606b-455">Type: chaîne</span><span class="sxs-lookup"><span data-stu-id="9606b-455">Type: String</span></span>**

<span data-ttu-id="9606b-456">La déclaration XML doit spécifier l’attribut XML version 1,0 ( &lt; ? xml version = «1.0» &gt; ).</span><span class="sxs-lookup"><span data-stu-id="9606b-456">The XML declaration must specify the XML version 1.0 attribute (&lt;?xml version="1.0"&gt;).</span></span> <span data-ttu-id="9606b-457">Les modèles d’emplacement des paramètres créés par le générateur UE-V sont enregistrés au format UTF-8, même si le codage n’est pas explicitement spécifié.</span><span class="sxs-lookup"><span data-stu-id="9606b-457">Settings location templates created by the UE-V Generator are saved in UTF-8 encoding, although the encoding is not explicitly specified.</span></span> <span data-ttu-id="9606b-458">Nous vous recommandons d’inclure l’attribut Encoding = «UTF-8» dans cet élément comme meilleure pratique.</span><span class="sxs-lookup"><span data-stu-id="9606b-458">We recommend that you include the encoding="UTF-8" attribute in this element as a best practice.</span></span> <span data-ttu-id="9606b-459">Tous les modèles inclus dans le produit spécifient également cette balise (voir les documents dans l’interface utilisateur de%ProgramFiles%\\Microsoft Virtualization\\Templates pour référence).</span><span class="sxs-lookup"><span data-stu-id="9606b-459">All templates included with the product specify this tag as well (see the documents in %ProgramFiles%\\Microsoft User Experience Virtualization\\Templates for reference).</span></span> <span data-ttu-id="9606b-460">Exemple:</span><span class="sxs-lookup"><span data-stu-id="9606b-460">For example:</span></span>

`<?xml version="1.0" encoding="UTF-8"?>`

### <a href="" id="namespace"></a><span data-ttu-id="9606b-461">Espace de noms et élément racine</span><span class="sxs-lookup"><span data-stu-id="9606b-461">Namespace and Root Element</span></span>

**<span data-ttu-id="9606b-462">Obligatoire: vrai</span><span class="sxs-lookup"><span data-stu-id="9606b-462">Mandatory: True</span></span>**

**<span data-ttu-id="9606b-463">Type: chaîne</span><span class="sxs-lookup"><span data-stu-id="9606b-463">Type: String</span></span>**

<span data-ttu-id="9606b-464">UE-V utilise l' https://schemas.microsoft.com/UserExperienceVirtualization/2012/SettingsLocationTemplate espace de noms pour toutes les applications.</span><span class="sxs-lookup"><span data-stu-id="9606b-464">UE-V uses the https://schemas.microsoft.com/UserExperienceVirtualization/2012/SettingsLocationTemplate namespace for all applications.</span></span> <span data-ttu-id="9606b-465">SettingsLocationTemplate est l’élément racine et contient tous les autres éléments.</span><span class="sxs-lookup"><span data-stu-id="9606b-465">SettingsLocationTemplate is the root element and contains all other elements.</span></span> <span data-ttu-id="9606b-466">Référencez SettingsLocationTemplate dans tous les modèles à l’aide de cette balise:</span><span class="sxs-lookup"><span data-stu-id="9606b-466">Reference SettingsLocationTemplate in all templates using this tag:</span></span>

`<SettingsLocationTemplate xmlns='https://schemas.microsoft.com/UserExperienceVirtualization/2012/SettingsLocationTemplate'>`

### <a href="" id="data"></a><span data-ttu-id="9606b-467">Types de données</span><span class="sxs-lookup"><span data-stu-id="9606b-467">Data types</span></span>

<span data-ttu-id="9606b-468">Il s’agit des types de données pour le schéma de modèle d’application UE-V.</span><span class="sxs-lookup"><span data-stu-id="9606b-468">These are the data types for the UE-V application template schema.</span></span>

<a href="" id="guid"></a><span data-ttu-id="9606b-469">**GUID** GUID décrit une expression régulière d’identificateur unique global standard au format «\ \ {\ [a-fA-F0-9 \] {8} -\ [a-FA-F0-9] {4} -\ [a------------------- {4} ---- {4} ---------------- {12} ----------------</span><span class="sxs-lookup"><span data-stu-id="9606b-469">**GUID** GUID describes a standard globally unique identifier regular expression in the form "\\{\[a-fA-F0-9\]{8}-\[a-fA-F0-9\]{4}-\[a-fA-F0-9\]{4}-\[a-fA-F0-9\]{4}-\[a-fA-F0-9\]{12}\\}".</span></span> <span data-ttu-id="9606b-470">Cette opération est utilisée dans l’élément Filesetting\\Root\\KnownFolder pour vérifier la mise en forme de dossiers bien connus.</span><span class="sxs-lookup"><span data-stu-id="9606b-470">This is used in the Filesetting\\Root\\KnownFolder element to verify the formatting of well-known folders.</span></span>

<a href="" id="filenamestring"></a><span data-ttu-id="9606b-471">**FilenameString** FilenameString fait référence au nom de fichier d’un processus à surveiller.</span><span class="sxs-lookup"><span data-stu-id="9606b-471">**FilenameString** FilenameString refers to the file name of a process to be monitored.</span></span> <span data-ttu-id="9606b-472">Ses valeurs ne sont pas limitées par le caractère &lt; &gt; Regex \ [^ \ \ \ \ \ ^ /: \] +, (autrement dit, ils ne peuvent pas contenir de caractères de barre oblique inverse, d’astérisques ou de signes d’interrogation, de caractère de barre oblique, de signe supérieur ou inférieur à, de barre oblique ou de deux-points).</span><span class="sxs-lookup"><span data-stu-id="9606b-472">Its values are restricted by the regex \[^\\\\\\?\\\*\\|&lt;&gt;/:\]+, (that is, they may not contain backslash characters, asterisk or question mark wild-card characters, the pipe character, the greater than or less than sign, forward slash, or colon characters).</span></span>

<a href="" id="idstring"></a><span data-ttu-id="9606b-473">**IdString** IDString fait référence à la valeur d’ID des éléments d’application, SettingsLocationTemplate et éléments communs (utilisés pour décrire les suites d’applications qui partagent des paramètres communs).</span><span class="sxs-lookup"><span data-stu-id="9606b-473">**IDString** IDString refers to the ID value of Application elements, SettingsLocationTemplate, and Common elements (used to describe application suites that share common settings).</span></span> <span data-ttu-id="9606b-474">Ce dernier est limité par le même Regex que FilenameString (\ [^ \ \ \ \ \ \? &lt; &gt; /:\]+).</span><span class="sxs-lookup"><span data-stu-id="9606b-474">It is restricted by the same regex as FilenameString (\[^\\\\\\?\\\*\\|&lt;&gt;/:\]+).</span></span>

<a href="" id="templateversion"></a><span data-ttu-id="9606b-475">**TemplateVersion** TemplateVersion est une valeur entière utilisée pour décrire la révision du modèle d’emplacement des paramètres.</span><span class="sxs-lookup"><span data-stu-id="9606b-475">**TemplateVersion** TemplateVersion is an integer value used to describe the revision of the settings location template.</span></span> <span data-ttu-id="9606b-476">Sa valeur est comprise entre 0 et 2147483647.</span><span class="sxs-lookup"><span data-stu-id="9606b-476">Its value may range from 0 to 2147483647.</span></span>

<a href="" id="empty"></a><span data-ttu-id="9606b-477">**Vides** Empty fait référence à une valeur null.</span><span class="sxs-lookup"><span data-stu-id="9606b-477">**Empty** Empty refers to a null value.</span></span> <span data-ttu-id="9606b-478">Ce champ est utilisé dans Process\\ShellProcess pour indiquer qu’il n’y a pas de processus à surveiller.</span><span class="sxs-lookup"><span data-stu-id="9606b-478">This is used in Process\\ShellProcess to indicate that there is no process to monitor.</span></span> <span data-ttu-id="9606b-479">Cette valeur ne doit pas être utilisée dans les modèles d’application.</span><span class="sxs-lookup"><span data-stu-id="9606b-479">This value should not be used in any application templates.</span></span>

<a href="" id="author"></a><span data-ttu-id="9606b-480">**Auteur** Le type de données auteur est un type complexe qui identifie l’auteur d’un modèle.</span><span class="sxs-lookup"><span data-stu-id="9606b-480">**Author** The Author data type is a complex type that identifies the author of a template.</span></span> <span data-ttu-id="9606b-481">Il contient deux éléments enfants: le **nom** et l' **adresse de courrier**.</span><span class="sxs-lookup"><span data-stu-id="9606b-481">It contains two child elements: **Name** and **Email**.</span></span> <span data-ttu-id="9606b-482">Dans le type de données auteur, l’élément nom est obligatoire lorsque l’élément de messagerie est facultatif.</span><span class="sxs-lookup"><span data-stu-id="9606b-482">Within the Author data type, the Name element is mandatory while the Email element is optional.</span></span> <span data-ttu-id="9606b-483">Ce type est décrit plus en détail dans l’élément SettingsLocationTemplate.</span><span class="sxs-lookup"><span data-stu-id="9606b-483">This type is described in more detail under the SettingsLocationTemplate element.</span></span>

<a href="" id="range"></a><span data-ttu-id="9606b-484">**Plage** Range définit une classe entière composée de deux éléments enfants: **minimum** et **maximum**.</span><span class="sxs-lookup"><span data-stu-id="9606b-484">**Range** Range defines an integer class consisting of two child elements: **Minimum** and **Maximum**.</span></span> <span data-ttu-id="9606b-485">Ce type de données est implémenté dans le type de données ProcessVersion.</span><span class="sxs-lookup"><span data-stu-id="9606b-485">This data type is implemented in the ProcessVersion data type.</span></span> <span data-ttu-id="9606b-486">Si ce paramètre est spécifié, les valeurs minimum et maximum doivent être incluses.</span><span class="sxs-lookup"><span data-stu-id="9606b-486">If specified, both Minimum and Maximum values must be included.</span></span>

<a href="" id="processversion"></a><span data-ttu-id="9606b-487">**ProcessVersion** ProcessVersion définit un type avec quatre éléments enfants: **major**, **Minor**, **Build**et **patch**.</span><span class="sxs-lookup"><span data-stu-id="9606b-487">**ProcessVersion** ProcessVersion defines a type with four child elements: **Major**, **Minor**, **Build**, and **Patch**.</span></span> <span data-ttu-id="9606b-488">Ce type de données est utilisé par l’élément process pour remplir ses valeurs ProductVersion et FileVersion.</span><span class="sxs-lookup"><span data-stu-id="9606b-488">This data type is used by the Process element to populate its ProductVersion and FileVersion values.</span></span> <span data-ttu-id="9606b-489">Les données pour ce type constituent une valeur de plage.</span><span class="sxs-lookup"><span data-stu-id="9606b-489">The data for this type is a Range value.</span></span> <span data-ttu-id="9606b-490">L’élément enfant principal est obligatoire et les autres sont facultatifs.</span><span class="sxs-lookup"><span data-stu-id="9606b-490">The Major child element is mandatory and the others are optional.</span></span>

<a href="" id="architecture"></a><span data-ttu-id="9606b-491">**Architecture** Architecture énumère deux valeurs possibles: **Win32** et **Win64**.</span><span class="sxs-lookup"><span data-stu-id="9606b-491">**Architecture** Architecture enumerates two possible values: **Win32** and **Win64**.</span></span> <span data-ttu-id="9606b-492">Ces valeurs sont utilisées pour spécifier l’architecture de processus.</span><span class="sxs-lookup"><span data-stu-id="9606b-492">These values are used to specify process architecture.</span></span>

<a href="" id="process"></a><span data-ttu-id="9606b-493">**Processus** Le type de données de processus est un conteneur utilisé pour décrire les processus à surveiller par UE-V.</span><span class="sxs-lookup"><span data-stu-id="9606b-493">**Process** The Process data type is a container used to describe processes to be monitored by UE-V.</span></span> <span data-ttu-id="9606b-494">Il contient six éléments enfants: **filename**, **architecture**, **ProductName**, **FileDescription**, **ProductVersion**et **FileVersion**.</span><span class="sxs-lookup"><span data-stu-id="9606b-494">It contains six child elements: **Filename**, **Architecture**, **ProductName**, **FileDescription**, **ProductVersion**, and **FileVersion**.</span></span> <span data-ttu-id="9606b-495">Ce tableau présente les différents types de données de chaque élément:</span><span class="sxs-lookup"><span data-stu-id="9606b-495">This table details each element’s respective data type:</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9606b-496">Élément</span><span class="sxs-lookup"><span data-stu-id="9606b-496">Element</span></span></th>
<th align="left"><span data-ttu-id="9606b-497">Type de données</span><span class="sxs-lookup"><span data-stu-id="9606b-497">Data Type</span></span></th>
<th align="left"><span data-ttu-id="9606b-498">Mandatory</span><span class="sxs-lookup"><span data-stu-id="9606b-498">Mandatory</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9606b-499">Courts</span><span class="sxs-lookup"><span data-stu-id="9606b-499">Filename</span></span></p></td>
<td align="left"><p><span data-ttu-id="9606b-500">FilenameString</span><span class="sxs-lookup"><span data-stu-id="9606b-500">FilenameString</span></span></p></td>
<td align="left"><p><span data-ttu-id="9606b-501">Vrai</span><span class="sxs-lookup"><span data-stu-id="9606b-501">True</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9606b-502">Architecture</span><span class="sxs-lookup"><span data-stu-id="9606b-502">Architecture</span></span></p></td>
<td align="left"><p><span data-ttu-id="9606b-503">Architecture</span><span class="sxs-lookup"><span data-stu-id="9606b-503">Architecture</span></span></p></td>
<td align="left"><p><span data-ttu-id="9606b-504">Faux</span><span class="sxs-lookup"><span data-stu-id="9606b-504">False</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9606b-505">ProductName</span><span class="sxs-lookup"><span data-stu-id="9606b-505">ProductName</span></span></p></td>
<td align="left"><p><span data-ttu-id="9606b-506">String</span><span class="sxs-lookup"><span data-stu-id="9606b-506">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="9606b-507">Faux</span><span class="sxs-lookup"><span data-stu-id="9606b-507">False</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9606b-508">FileDescription</span><span class="sxs-lookup"><span data-stu-id="9606b-508">FileDescription</span></span></p></td>
<td align="left"><p><span data-ttu-id="9606b-509">String</span><span class="sxs-lookup"><span data-stu-id="9606b-509">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="9606b-510">Faux</span><span class="sxs-lookup"><span data-stu-id="9606b-510">False</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9606b-511">ProductVersion</span><span class="sxs-lookup"><span data-stu-id="9606b-511">ProductVersion</span></span></p></td>
<td align="left"><p><span data-ttu-id="9606b-512">ProcessVersion</span><span class="sxs-lookup"><span data-stu-id="9606b-512">ProcessVersion</span></span></p></td>
<td align="left"><p><span data-ttu-id="9606b-513">Faux</span><span class="sxs-lookup"><span data-stu-id="9606b-513">False</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9606b-514">FileVersion</span><span class="sxs-lookup"><span data-stu-id="9606b-514">FileVersion</span></span></p></td>
<td align="left"><p><span data-ttu-id="9606b-515">ProcessVersion</span><span class="sxs-lookup"><span data-stu-id="9606b-515">ProcessVersion</span></span></p></td>
<td align="left"><p><span data-ttu-id="9606b-516">Faux</span><span class="sxs-lookup"><span data-stu-id="9606b-516">False</span></span></p></td>
</tr>
</tbody>
</table>

 

<a href="" id="processes"></a><span data-ttu-id="9606b-517">**Processus** Le type de données processus représente un conteneur pour une collection d’un ou plusieurs éléments de processus.</span><span class="sxs-lookup"><span data-stu-id="9606b-517">**Processes** The Processes data type represents a container for a collection of one or more Process elements.</span></span> <span data-ttu-id="9606b-518">Deux éléments enfants sont pris en charge dans le **type de séquence processus et** **ShellProcess**.</span><span class="sxs-lookup"><span data-stu-id="9606b-518">Two child elements are supported in the Processes sequence type: **Process** and **ShellProcess**.</span></span> <span data-ttu-id="9606b-519">Process est un élément de type process et ShellProcess est de type de données Empty.</span><span class="sxs-lookup"><span data-stu-id="9606b-519">Process is an element of type Process and ShellProcess is of data type Empty.</span></span> <span data-ttu-id="9606b-520">Au moins un élément doit être identifié dans la séquence.</span><span class="sxs-lookup"><span data-stu-id="9606b-520">At least one item must be identified in the sequence.</span></span>

<a href="" id="path"></a><span data-ttu-id="9606b-521">**Path (chemin** ) Path est consommé par RegistrySetting et FileSetting pour faire référence aux chemins d’accès du Registre et des fichiers.</span><span class="sxs-lookup"><span data-stu-id="9606b-521">**Path** Path is consumed by RegistrySetting and FileSetting to refer to registry and file paths.</span></span> <span data-ttu-id="9606b-522">Cet élément prend en charge deux attributs facultatifs: **récurrent** et **DeleteIfNotFound**.</span><span class="sxs-lookup"><span data-stu-id="9606b-522">This element supports two optional attributes: **Recursive** and **DeleteIfNotFound**.</span></span> <span data-ttu-id="9606b-523">Les deux valeurs sont définies sur Default = «false».</span><span class="sxs-lookup"><span data-stu-id="9606b-523">Both values are set to default=”False”.</span></span>

<span data-ttu-id="9606b-524">La récursivité indique que le chemin d’accès et tous les sous-dossiers sont inclus pour les paramètres de fichier ou que toutes les clés de Registre enfant sont incluses pour les paramètres du Registre.</span><span class="sxs-lookup"><span data-stu-id="9606b-524">Recursive indicates that the path and all subfolders are included for file settings or that all child registry keys are included for registry settings.</span></span> <span data-ttu-id="9606b-525">Dans les deux cas, tous les éléments du niveau actuel sont inclus dans les données capturées.</span><span class="sxs-lookup"><span data-stu-id="9606b-525">In both cases, all items at the current level are included in the data captured.</span></span> <span data-ttu-id="9606b-526">Pour un objet FileSettings, tous les fichiers dans le dossier spécifié sont inclus dans les données capturées par UE-V, mais les dossiers ne sont pas inclus.</span><span class="sxs-lookup"><span data-stu-id="9606b-526">For a FileSettings object, all files within the specified folder are included in the data captured by UE-V but folders are not included.</span></span> <span data-ttu-id="9606b-527">Pour les chemins d’accès de Registre, toutes les valeurs du chemin d’accès actuel sont capturées, mais les clés de Registre enfants ne sont pas capturées.</span><span class="sxs-lookup"><span data-stu-id="9606b-527">For registry paths, all values in the current path are captured but child registry keys are not captured.</span></span> <span data-ttu-id="9606b-528">Dans les deux cas, veillez à éviter de capturer des jeux de données volumineux ou d’un grand nombre d’éléments.</span><span class="sxs-lookup"><span data-stu-id="9606b-528">In both cases, care should be taken to avoid capturing large data sets or large numbers of items.</span></span>

<span data-ttu-id="9606b-529">L’attribut DeleteIfNotFound supprime le paramètre des données de chemin d’accès au stockage des paramètres de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9606b-529">The DeleteIfNotFound attribute removes the setting from the user’s settings storage path data.</span></span> <span data-ttu-id="9606b-530">Cela peut être souhaitable dans les cas où la suppression de ces paramètres du package permet d’économiser une grande quantité d’espace disque sur le serveur de fichiers de chemin d’accès de l’emplacement de stockage des paramètres.</span><span class="sxs-lookup"><span data-stu-id="9606b-530">This may be desirable in cases where removing these settings from the package will save a large amount of disk space on the settings storage path file server.</span></span>

<a href="" id="filemask"></a><span data-ttu-id="9606b-531">**Filemask** FileMask spécifie uniquement certains types de fichiers définis par Path.</span><span class="sxs-lookup"><span data-stu-id="9606b-531">**FileMask** FileMask specifies only certain file types for the folder that is defined by Path.</span></span> <span data-ttu-id="9606b-532">Par exemple, path peut être `C:\users\username\files` et filemask peut être `*.txt` pour inclure uniquement des fichiers texte.</span><span class="sxs-lookup"><span data-stu-id="9606b-532">For example, Path might be `C:\users\username\files` and FileMask could be `*.txt` to include only text files.</span></span>

<a href="" id="registrysetting"></a><span data-ttu-id="9606b-533">**RegistrySetting** RegistrySetting représente un conteneur pour les clés et les valeurs de Registre et le comportement souhaité associé au sein de l’agent UE-V.</span><span class="sxs-lookup"><span data-stu-id="9606b-533">**RegistrySetting** RegistrySetting represents a container for registry keys and values and the associated desired behavior on the part of the UE-V Agent.</span></span> <span data-ttu-id="9606b-534">Quatre éléments enfants sont définis dans ce type: **path**, **Name**, **Exclude**et une séquence des valeurs **path** et **Name**.</span><span class="sxs-lookup"><span data-stu-id="9606b-534">Four child elements are defined within this type: **Path**, **Name**, **Exclude**, and a sequence of the values **Path** and **Name**.</span></span>

<a href="" id="filesetting"></a><span data-ttu-id="9606b-535">**FileSetting** FileSetting contient des paramètres associés à des fichiers et des chemins d’accès aux fichiers.</span><span class="sxs-lookup"><span data-stu-id="9606b-535">**FileSetting** FileSetting contains parameters associated with files and files paths.</span></span> <span data-ttu-id="9606b-536">Quatre éléments enfants sont définis: **root**, **path**, **filemask**et **Exclude**.</span><span class="sxs-lookup"><span data-stu-id="9606b-536">Four child elements are defined: **Root**, **Path**, **FileMask**, and **Exclude**.</span></span> <span data-ttu-id="9606b-537">La racine est obligatoire et les autres sont facultatifs.</span><span class="sxs-lookup"><span data-stu-id="9606b-537">Root is mandatory and the others are optional.</span></span>

<a href="" id="settings"></a><span data-ttu-id="9606b-538">**Paramètres** Settings est un conteneur pour tous les paramètres qui s’appliquent à un modèle spécifique.</span><span class="sxs-lookup"><span data-stu-id="9606b-538">**Settings** Settings is a container for all the settings that apply to a particular template.</span></span> <span data-ttu-id="9606b-539">Il contient des instances des paramètres de Registre, de fichier, de SystemParameter et d’CustomAction décrits plus haut.</span><span class="sxs-lookup"><span data-stu-id="9606b-539">It contains instances of the Registry, File, SystemParameter, and CustomAction settings described earlier.</span></span> <span data-ttu-id="9606b-540">De plus, il peut également contenir les éléments enfants suivants avec des comportements décrits:</span><span class="sxs-lookup"><span data-stu-id="9606b-540">In addition, it can also contain the following child elements with behaviors described:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9606b-541">Élément</span><span class="sxs-lookup"><span data-stu-id="9606b-541">Element</span></span></th>
<th align="left"><span data-ttu-id="9606b-542">Description</span><span class="sxs-lookup"><span data-stu-id="9606b-542">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9606b-543">Asynchrone</span><span class="sxs-lookup"><span data-stu-id="9606b-543">Asynchronous</span></span></p></td>
<td align="left"><p><span data-ttu-id="9606b-544">Les packages de paramètres asynchrones s’appliquent sans bloquer le démarrage de l’application afin que l’application démarre alors que les paramètres sont encore appliqués.</span><span class="sxs-lookup"><span data-stu-id="9606b-544">Asynchronous settings packages are applied without blocking the application startup so that the application start proceeds while the settings are still being applied.</span></span> <span data-ttu-id="9606b-545">Cela s’avère utile pour les paramètres qui peuvent être appliqués de manière asynchrone, par exemple par le <code>get/set</code> biais d’une API telle que SystemParameterSetting.</span><span class="sxs-lookup"><span data-stu-id="9606b-545">This is useful for settings that can be applied asynchronously, such as those <code>get/set</code> through an API, like SystemParameterSetting.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9606b-546">PreventOverlappingSynchronization</span><span class="sxs-lookup"><span data-stu-id="9606b-546">PreventOverlappingSynchronization</span></span></p></td>
<td align="left"><p><span data-ttu-id="9606b-547">Par défaut, UE-V enregistre uniquement les paramètres d’une application lorsque la dernière instance d’une application utilisant le modèle est fermée.</span><span class="sxs-lookup"><span data-stu-id="9606b-547">By default, UE-V only saves settings for an application when the last instance of an application using the template is closed.</span></span> <span data-ttu-id="9606b-548">Lorsque cet élément est défini sur «false», UE-V exporte les paramètres même si d’autres instances d’une application sont en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="9606b-548">When this element is set to ‘false’, UE-V exports the settings even if other instances of an application are running.</span></span> <span data-ttu-id="9606b-549">Les modèles adaptés, qui incluent une section commune des éléments, qui sont livrés avec UE-V, utilisent cet indicateur pour permettre aux paramètres partagés de toujours exporter à la fermeture de l’application, tout en empêchant les paramètres spécifiques à l’application d’être exportés jusqu’à la fin de la dernière instance.</span><span class="sxs-lookup"><span data-stu-id="9606b-549">Suited templates – those that include a Common element section– that are shipped with UE-V use this flag to enable shared settings to always export on application close, while preventing application-specific settings from exporting until the last instance is closed.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="name"></a><span data-ttu-id="9606b-550">Élément Name</span><span class="sxs-lookup"><span data-stu-id="9606b-550">Name Element</span></span>

**<span data-ttu-id="9606b-551">Obligatoire: vrai</span><span class="sxs-lookup"><span data-stu-id="9606b-551">Mandatory: True</span></span>**

**<span data-ttu-id="9606b-552">Type: chaîne</span><span class="sxs-lookup"><span data-stu-id="9606b-552">Type: String</span></span>**

<span data-ttu-id="9606b-553">Nom spécifie un nom unique pour le modèle d’emplacement des paramètres.</span><span class="sxs-lookup"><span data-stu-id="9606b-553">Name specifies a unique name for the settings location template.</span></span> <span data-ttu-id="9606b-554">Il est utilisé à des fins d’affichage lors du référencement du modèle dans WMI, PowerShell, Observateur d’événements et journaux de débogage.</span><span class="sxs-lookup"><span data-stu-id="9606b-554">This is used for display purposes when referencing the template in WMI, PowerShell, Event Viewer and debug logs.</span></span> <span data-ttu-id="9606b-555">En règle générale, évitez de référencer les informations de version, car cela peut être objet à partir de l’élément ProductVersion.</span><span class="sxs-lookup"><span data-stu-id="9606b-555">In general, avoid referencing version information, as this can be objected from the ProductVersion element.</span></span> <span data-ttu-id="9606b-556">Par exemple, spécifiez `<Name>My Application</Name>` plutôt que `<Name>My Application 1.1</Name>` .</span><span class="sxs-lookup"><span data-stu-id="9606b-556">For example, specify `<Name>My Application</Name>` rather than `<Name>My Application 1.1</Name>`.</span></span>

<span data-ttu-id="9606b-557">**Remarques**  UE-V ne référence pas les DTD externes, de sorte qu’il n’est pas possible d’utiliser des entités nommées dans un modèle d’emplacement des paramètres.</span><span class="sxs-lookup"><span data-stu-id="9606b-557">**Note** UE-V does not reference external DTDs, so it is not possible to use named entities in a settings location template.</span></span> <span data-ttu-id="9606b-558">Par exemple, n’utilisez pas &reg; pour se référer au signe de marque commerciale enregistré®.</span><span class="sxs-lookup"><span data-stu-id="9606b-558">For example, do not use &reg; to refer to the registered trade mark sign ®.</span></span> <span data-ttu-id="9606b-559">Au lieu de cela, utilisez des références numérotées canoniques pour inclure ces types de caractères spéciaux (par exemple, & \ #174 pour le caractère®.</span><span class="sxs-lookup"><span data-stu-id="9606b-559">Instead, use canonical numbered references to include these types of special characters, for example, &\#174 for the ® character.</span></span> <span data-ttu-id="9606b-560">Cette règle s’applique à toutes les valeurs de chaîne dans ce document.</span><span class="sxs-lookup"><span data-stu-id="9606b-560">This rule applies to all string values in this document.</span></span>

<span data-ttu-id="9606b-561"><http://www.w3.org/TR/xhtml1/dtds.html>Pour obtenir la liste complète des entités de caractères, voir.</span><span class="sxs-lookup"><span data-stu-id="9606b-561">See <http://www.w3.org/TR/xhtml1/dtds.html> for a complete list of character entities.</span></span> <span data-ttu-id="9606b-562">Les documents encodés au format UTF-8 peuvent inclure les caractères Unicode directement.</span><span class="sxs-lookup"><span data-stu-id="9606b-562">UTF-8-encoded documents may include the Unicode characters directly.</span></span> <span data-ttu-id="9606b-563">L’enregistrement de modèles par le biais du générateur UE-V convertit automatiquement des entités de caractères en leur représentation Unicode.</span><span class="sxs-lookup"><span data-stu-id="9606b-563">Saving templates through the UE-V Generator converts character entities to their Unicode representations automatically.</span></span>

 

### <a href="" id="id"></a><span data-ttu-id="9606b-564">Élément ID</span><span class="sxs-lookup"><span data-stu-id="9606b-564">ID Element</span></span>

**<span data-ttu-id="9606b-565">Obligatoire: vrai</span><span class="sxs-lookup"><span data-stu-id="9606b-565">Mandatory: True</span></span>**

**<span data-ttu-id="9606b-566">Type: chaîne</span><span class="sxs-lookup"><span data-stu-id="9606b-566">Type: String</span></span>**

<span data-ttu-id="9606b-567">ID remplit un identificateur unique pour un modèle particulier.</span><span class="sxs-lookup"><span data-stu-id="9606b-567">ID populates a unique identifier for a particular template.</span></span> <span data-ttu-id="9606b-568">Cette balise devient l’identificateur principal utilisé par l’agent UE-V pour référencer le modèle lors de l’exécution (par exemple, voir la sortie des cmdlets Get-UevTemplate et Get-UevTemplateProgram PowerShell).</span><span class="sxs-lookup"><span data-stu-id="9606b-568">This tag becomes the primary identifier that the UE-V Agent uses to reference the template at runtime (for example, see the output of the Get-UevTemplate and Get-UevTemplateProgram PowerShell cmdlets).</span></span> <span data-ttu-id="9606b-569">Par Convention, cette balise ne doit contenir aucun espace, ce qui simplifie la création de scripts.</span><span class="sxs-lookup"><span data-stu-id="9606b-569">By convention, this tag should not contain any spaces, which simplifies scripting.</span></span> <span data-ttu-id="9606b-570">Le numéro de version des applications doit être spécifié dans cet élément pour faciliter l’identification du modèle, par exemple `<ID>MicrosoftCalculator6</ID>` ou `<ID>MicrosoftOffice2010Win64</ID>` .</span><span class="sxs-lookup"><span data-stu-id="9606b-570">Version numbers of applications should be specified in this element to allow for easy identification of the template, such as `<ID>MicrosoftCalculator6</ID>` or `<ID>MicrosoftOffice2010Win64</ID>`.</span></span>

### <a href="" id="version"></a><span data-ttu-id="9606b-571">Élément version</span><span class="sxs-lookup"><span data-stu-id="9606b-571">Version Element</span></span>

**<span data-ttu-id="9606b-572">Obligatoire: vrai</span><span class="sxs-lookup"><span data-stu-id="9606b-572">Mandatory: True</span></span>**

**<span data-ttu-id="9606b-573">Type: entier</span><span class="sxs-lookup"><span data-stu-id="9606b-573">Type: Integer</span></span>**

**<span data-ttu-id="9606b-574">Valeur minimale: 0</span><span class="sxs-lookup"><span data-stu-id="9606b-574">Minimum Value: 0</span></span>**

**<span data-ttu-id="9606b-575">Valeur maximale: 2147483647</span><span class="sxs-lookup"><span data-stu-id="9606b-575">Maximum Value: 2147483647</span></span>**

<span data-ttu-id="9606b-576">Version identifie la version du modèle d’emplacement paramètres pour le suivi des modifications.</span><span class="sxs-lookup"><span data-stu-id="9606b-576">Version identifies the version of the settings location template for administrative tracking of changes.</span></span> <span data-ttu-id="9606b-577">Le générateur UE-V augmente automatiquement ce nombre de une unité chaque fois que le modèle est enregistré.</span><span class="sxs-lookup"><span data-stu-id="9606b-577">The UE-V Generator automatically increments this number by one each time the template is saved.</span></span> <span data-ttu-id="9606b-578">Notez que ce champ doit contenir un nombre entier. les valeurs fractionnaires, par exemple, `<Version>2.5</Version>` ne sont pas autorisées.</span><span class="sxs-lookup"><span data-stu-id="9606b-578">Notice that this field must be a whole number integer; fractional values, such as `<Version>2.5</Version>` are not allowed.</span></span>

<span data-ttu-id="9606b-579">**Astuce:** Vous pouvez enregistrer des notes sur les changements de version à l’aide d’indicateurs de commentaires XML `<!-- -->` , par exemple:</span><span class="sxs-lookup"><span data-stu-id="9606b-579">**Hint:** You can save notes about version changes using XML comment tags `<!-- -->`, for example:</span></span>

```xml
<!--
    Version History

    Version 1 Jul 05, 2012 Initial template created by Generator - Denise@Contoso.com
    Version 2 Jul 31, 2012 Added support for app.exe v2.1.3 - Mark@Contoso.com
    Version 3 Jan 01, 2013 Added font settings support - Mark@Contoso.com
    Version 4 Jan 31, 2013 Added support for plugin settings - Tony@Contoso.com
  -->
<Version>4</Version>
```

<span data-ttu-id="9606b-580">**Important**  Cette valeur est interrogée pour déterminer si une nouvelle version d’un modèle doit être appliquée à un modèle existant dans les cas suivants:</span><span class="sxs-lookup"><span data-stu-id="9606b-580">**Important** This value is queried to determine if a new version of a template should be applied to an existing template in these instances:</span></span>

-   <span data-ttu-id="9606b-581">Lorsque la tâche de mise à jour automatique du modèle planifié s’exécute</span><span class="sxs-lookup"><span data-stu-id="9606b-581">When the scheduled Template Auto Update task executes</span></span>

-   <span data-ttu-id="9606b-582">Lors de l’exécution de la cmdlet PowerShell Update-UevTemplate</span><span class="sxs-lookup"><span data-stu-id="9606b-582">When the Update-UevTemplate PowerShell cmdlet is executed</span></span>

-   <span data-ttu-id="9606b-583">Lorsque la méthode microsoft\\uev: SettingsLocationTemplate Update est appelée via WMI</span><span class="sxs-lookup"><span data-stu-id="9606b-583">When the microsoft\\uev:SettingsLocationTemplate Update method is called through WMI</span></span>

 

### <a href="" id="author"></a><span data-ttu-id="9606b-584">Élément Author</span><span class="sxs-lookup"><span data-stu-id="9606b-584">Author Element</span></span>

**<span data-ttu-id="9606b-585">Obligatoire: faux</span><span class="sxs-lookup"><span data-stu-id="9606b-585">Mandatory: False</span></span>**

**<span data-ttu-id="9606b-586">Type: chaîne</span><span class="sxs-lookup"><span data-stu-id="9606b-586">Type: String</span></span>**

<span data-ttu-id="9606b-587">Auteur identifie le créateur du modèle d’emplacement des paramètres.</span><span class="sxs-lookup"><span data-stu-id="9606b-587">Author identifies the creator of the settings location template.</span></span> <span data-ttu-id="9606b-588">Deux éléments enfants facultatifs sont pris en charge: **nom** et **adresse de messagerie**.</span><span class="sxs-lookup"><span data-stu-id="9606b-588">Two optional child elements are supported: **Name** and **Email**.</span></span> <span data-ttu-id="9606b-589">Les deux attributs sont facultatifs, mais si l’élément enfant de l’élément email est spécifié, il doit être accompagné du nom de l’élément.</span><span class="sxs-lookup"><span data-stu-id="9606b-589">Both attributes are optional, but, if the Email child element is specified, it must be accompanied by the Name element.</span></span> <span data-ttu-id="9606b-590">Auteur fait référence au nom complet du contact pour le modèle d’emplacement des paramètres et la messagerie doit désigner une adresse de messagerie de l’auteur.</span><span class="sxs-lookup"><span data-stu-id="9606b-590">Author refers to the full name of the contact for the settings location template, and email should refer to an email address for the author.</span></span> <span data-ttu-id="9606b-591">Nous vous recommandons d’inclure ces informations dans les modèles publiés publiquement (par exemple, dans la [Galerie de modèles UE-V](https://gallery.technet.microsoft.com/site/search?f%5B0%5D.Type=RootCategory&f%5B0%5D.Value=UE-V)).</span><span class="sxs-lookup"><span data-stu-id="9606b-591">We recommend that you include this information in templates published publicly, for example, on the [UE-V Template Gallery](https://gallery.technet.microsoft.com/site/search?f%5B0%5D.Type=RootCategory&f%5B0%5D.Value=UE-V).</span></span>

### <a href="" id="processes"></a><span data-ttu-id="9606b-592">Processus et élément de processus</span><span class="sxs-lookup"><span data-stu-id="9606b-592">Processes and Process Element</span></span>

**<span data-ttu-id="9606b-593">Obligatoire: vrai</span><span class="sxs-lookup"><span data-stu-id="9606b-593">Mandatory: True</span></span>**

**<span data-ttu-id="9606b-594">Type: élément</span><span class="sxs-lookup"><span data-stu-id="9606b-594">Type: Element</span></span>**

<span data-ttu-id="9606b-595">Processus contient au moins un `<Process>` élément, qui à son tour contient les éléments enfants suivants: **filename**, **architecture**, **ProductName**, **FileDescription**, **ProductVersion**et **FileVersion**.</span><span class="sxs-lookup"><span data-stu-id="9606b-595">Processes contains at least one `<Process>` element, which in turn contains the following child elements: **Filename**, **Architecture**, **ProductName**, **FileDescription**, **ProductVersion**, and **FileVersion**.</span></span> <span data-ttu-id="9606b-596">L’élément enfant de nom de fichier est obligatoire et les autres sont facultatifs.</span><span class="sxs-lookup"><span data-stu-id="9606b-596">The Filename child element is mandatory and the others are optional.</span></span> <span data-ttu-id="9606b-597">Un élément complet contient des balises similaires à ce qui suit:</span><span class="sxs-lookup"><span data-stu-id="9606b-597">A fully populated element contains tags similar to this example:</span></span>

```xml
<Process>
  <Filename>MyApplication.exe</Filename>
  <Architecture>Win64</Architecture>
  <ProductName> MyApplication </ProductName>
  <FileDescription>MyApplication.exe</FileDescription>
  <ProductVersion>
    <Major Minimum="2" Maximum="2" />
    <Minor Minimum="0" Maximum="0" />
    <Build Minimum="0" Maximum="0" />
    <Patch Minimum="5" Maximum="5" />
  </ProductVersion>
  <FileVersion>
    <Major Minimum="2" Maximum="2" />
    <Minor Minimum="0" Maximum="0" />
    <Build Minimum="0" Maximum="0" />
    <Patch Minimum="5" Maximum="5" />
  </FileVersion>
</Process>
```

### <span data-ttu-id="9606b-598">Courts</span><span class="sxs-lookup"><span data-stu-id="9606b-598">Filename</span></span>

**<span data-ttu-id="9606b-599">Obligatoire: vrai</span><span class="sxs-lookup"><span data-stu-id="9606b-599">Mandatory: True</span></span>**

**<span data-ttu-id="9606b-600">Type: chaîne</span><span class="sxs-lookup"><span data-stu-id="9606b-600">Type: String</span></span>**

<span data-ttu-id="9606b-601">Nom de fichier correspond au nom de fichier réel de l’exécutable tel qu’il apparaît dans le système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="9606b-601">Filename refers to the actual file name of the executable as it appears in the file system.</span></span> <span data-ttu-id="9606b-602">Cet élément spécifie le critère principal utilisé par UE-V pour déterminer si un modèle s’applique à un processus ou non.</span><span class="sxs-lookup"><span data-stu-id="9606b-602">This element specifies the primary criterion that UE-V uses to evaluate whether a template applies to a process or not.</span></span> <span data-ttu-id="9606b-603">Cet élément doit être spécifié dans le fichier XML du modèle d’emplacement des paramètres.</span><span class="sxs-lookup"><span data-stu-id="9606b-603">This element must be specified in the settings location template XML.</span></span>

<span data-ttu-id="9606b-604">Les noms de fichier valides ne doivent pas correspondre à l’expression régulière \ [^ \ \ \ \ \ \? &lt; &gt; /: \] +, autrement dit, ils ne peuvent pas contenir de caractères de barre oblique inverse, d’astérisque ou de point d’interrogation, de caractère de barre oblique, de signe supérieur ou inférieur</span><span class="sxs-lookup"><span data-stu-id="9606b-604">Valid filenames must not match the regular expression \[^\\\\\\?\\\*\\|&lt;&gt;/:\]+, that is, they may not contain backslash characters, asterisk or question mark wild-card characters, the pipe character, the greater than or less than sign, forward slash, or colon (the \\ ?</span></span> <span data-ttu-id="9606b-605">\* | &lt; &gt; /ou: caractères.).</span><span class="sxs-lookup"><span data-stu-id="9606b-605">\* | &lt; &gt; / or : characters.).</span></span>

<span data-ttu-id="9606b-606">**Astuce:** Pour tester une chaîne par rapport à cette expression régulière, utilisez une fenêtre de commande PowerShell et remplacez le nom de votre exécutable par **YourFileName**:</span><span class="sxs-lookup"><span data-stu-id="9606b-606">**Hint:** To test a string against this regex, use a PowerShell command window and substitute your executable’s name for **YourFileName**:</span></span>

`"YourFileName.exe" -match  "[\\\?\*\|<>/:]+"`

<span data-ttu-id="9606b-607">La valeur **true** indique que la chaîne contient des caractères non valides.</span><span class="sxs-lookup"><span data-stu-id="9606b-607">A value of **True** indicates that the string contains illegal characters.</span></span> <span data-ttu-id="9606b-608">Voici quelques exemples de valeurs non valides:</span><span class="sxs-lookup"><span data-stu-id="9606b-608">Here are some examples of illegal values:</span></span>

-   <span data-ttu-id="9606b-609">\\\\server\\share\\program.exe</span><span class="sxs-lookup"><span data-stu-id="9606b-609">\\\\server\\share\\program.exe</span></span>

-   <span data-ttu-id="9606b-610">Programme \ \*. exe</span><span class="sxs-lookup"><span data-stu-id="9606b-610">Program\*.exe</span></span>

-   <span data-ttu-id="9606b-611">Pro? ram.exe</span><span class="sxs-lookup"><span data-stu-id="9606b-611">Pro?ram.exe</span></span>

-   <span data-ttu-id="9606b-612">Programme &lt; 1 &gt; . exe</span><span class="sxs-lookup"><span data-stu-id="9606b-612">Program&lt;1&gt;.exe</span></span>

<span data-ttu-id="9606b-613">**Remarques**  Le générateur UE-V encode les caractères supérieur et inférieur, comme &gt; et &lt; respectivement.</span><span class="sxs-lookup"><span data-stu-id="9606b-613">**Note** The UE-V Generator encodes the greater than and less than characters as &gt; and &lt; respectively.</span></span>

 

<span data-ttu-id="9606b-614">Dans de rares cas, la valeur FileName n’inclura pas nécessairement l’extension. exe, mais elle doit être spécifiée dans le cadre de la valeur.</span><span class="sxs-lookup"><span data-stu-id="9606b-614">In rare circumstances, the FileName value will not necessarily include the .exe extension, but it should be specified as part of the value.</span></span> <span data-ttu-id="9606b-615">Par exemple, `<Filename>MyApplictication.exe</Filename>` doit être spécifié au lieu de `<Filename>MyApplictication</Filename>` .</span><span class="sxs-lookup"><span data-stu-id="9606b-615">For example, `<Filename>MyApplictication.exe</Filename>` should be specified instead of `<Filename>MyApplictication</Filename>`.</span></span> <span data-ttu-id="9606b-616">Le second exemple n’applique pas le modèle au processus si le véritable nom du fichier exécutable est «MyApplication.exe».</span><span class="sxs-lookup"><span data-stu-id="9606b-616">The second example will not apply the template to the process if the actual name of the executable file is “MyApplication.exe”.</span></span>

### <span data-ttu-id="9606b-617">Architecture</span><span class="sxs-lookup"><span data-stu-id="9606b-617">Architecture</span></span>

**<span data-ttu-id="9606b-618">Obligatoire: faux</span><span class="sxs-lookup"><span data-stu-id="9606b-618">Mandatory: False</span></span>**

**<span data-ttu-id="9606b-619">Type: architecture (chaîne)</span><span class="sxs-lookup"><span data-stu-id="9606b-619">Type: Architecture (String)</span></span>**

<span data-ttu-id="9606b-620">Architecture fait référence à l’architecture de processeur pour laquelle l’exécutable cible a été compilé.</span><span class="sxs-lookup"><span data-stu-id="9606b-620">Architecture refers to the processor architecture for which the target executable was compiled.</span></span> <span data-ttu-id="9606b-621">Les valeurs valides sont Win32 pour les applications 32 bits ou Win64 pour les applications 64 bits.</span><span class="sxs-lookup"><span data-stu-id="9606b-621">Valid values are Win32 for 32-bit applications or Win64 for 64-bit applications.</span></span> <span data-ttu-id="9606b-622">Le cas échéant, cette balise limite l’applicabilité du modèle d’emplacement des paramètres à une architecture d’application particulière.</span><span class="sxs-lookup"><span data-stu-id="9606b-622">If present, this tag limits the applicability of the settings location template to a particular application architecture.</span></span> <span data-ttu-id="9606b-623">Pour obtenir un exemple, comparez l’utilisation de l’interface utilisateur%ProgramFiles%\\Microsoft MicrosoftOffice2010Win32.xml Virtualization\\templates\\ MicrosoftOffice2010Win64.xml et les fichiers inclus avec UE-V.</span><span class="sxs-lookup"><span data-stu-id="9606b-623">For an example of this, compare the %ProgramFiles%\\Microsoft User Experience Virtualization\\templates\\ MicrosoftOffice2010Win32.xml and MicrosoftOffice2010Win64.xml files included with UE-V.</span></span> <span data-ttu-id="9606b-624">Cette fonctionnalité est utile lorsque des chemins relatifs changent entre différentes versions d’un fichier exécutable ou si des paramètres ont été ajoutés ou supprimés lors du passage d’une architecture de processeur à une autre.</span><span class="sxs-lookup"><span data-stu-id="9606b-624">This is useful when relative paths change between different versions of an executable or if settings have been added or removed when moving from one processor architecture to another.</span></span>

<span data-ttu-id="9606b-625">Si cet élément est absent, le modèle d’emplacement des paramètres ignore l’architecture du processus et s’applique aux processus 32 et 64 bits en cas d’application du nom de fichier et d’autres attributs.</span><span class="sxs-lookup"><span data-stu-id="9606b-625">If this element is absent, the settings location template ignores the process’ architecture and applies to both 32 and 64-bit processes if the file name and other attributes apply.</span></span>

<span data-ttu-id="9606b-626">**Remarques**  UE-V ne prend pas en charge les processeurs ARM dans cette version.</span><span class="sxs-lookup"><span data-stu-id="9606b-626">**Note** UE-V does not support ARM processors in this version.</span></span>

 

### <span data-ttu-id="9606b-627">ProductName</span><span class="sxs-lookup"><span data-stu-id="9606b-627">ProductName</span></span>

**<span data-ttu-id="9606b-628">Obligatoire: faux</span><span class="sxs-lookup"><span data-stu-id="9606b-628">Mandatory: False</span></span>**

**<span data-ttu-id="9606b-629">Type: chaîne</span><span class="sxs-lookup"><span data-stu-id="9606b-629">Type: String</span></span>**

<span data-ttu-id="9606b-630">ProductName est un élément facultatif utilisé pour identifier un produit à des fins d’administration ou de création de rapports.</span><span class="sxs-lookup"><span data-stu-id="9606b-630">ProductName is an optional element used to identify a product for administrative purposes or reporting.</span></span> <span data-ttu-id="9606b-631">ProductName est différent du nom de fichier, car il n’y a pas de restrictions d’expression régulières sur sa valeur.</span><span class="sxs-lookup"><span data-stu-id="9606b-631">ProductName differs from Filename in that there are no regular expression restrictions on its value.</span></span> <span data-ttu-id="9606b-632">Cela permet d’obtenir des descriptions plus faciles à comprendre du processus pour lequel le nom exécutable n’est pas évident.</span><span class="sxs-lookup"><span data-stu-id="9606b-632">This allows for more easily understood descriptions of a process where the executable name may not be obvious.</span></span> <span data-ttu-id="9606b-633">Exemple:</span><span class="sxs-lookup"><span data-stu-id="9606b-633">For example:</span></span>

```xml
<Process>
  <Filename>MyApplication.exe</Filename>
  <ProductName>My Application 6.x by Contoso.com</ProductName>
  <ProductVersion>
    <Major Minimum="6" Maximum="6" />
  </ProductVersion>
</Process>
```

### <span data-ttu-id="9606b-634">FileDescription</span><span class="sxs-lookup"><span data-stu-id="9606b-634">FileDescription</span></span>

**<span data-ttu-id="9606b-635">Obligatoire: faux</span><span class="sxs-lookup"><span data-stu-id="9606b-635">Mandatory: False</span></span>**

**<span data-ttu-id="9606b-636">Type: chaîne</span><span class="sxs-lookup"><span data-stu-id="9606b-636">Type: String</span></span>**

<span data-ttu-id="9606b-637">FileDescription est une balise facultative qui permet d’obtenir une description administrative du fichier exécutable.</span><span class="sxs-lookup"><span data-stu-id="9606b-637">FileDescription is an optional tag that allows for an administrative description of the executable file.</span></span> <span data-ttu-id="9606b-638">Il s’agit d’un champ de texte libre qui peut être utile dans le cas d’un package logiciel permettant d’identifier la fonction du fichier exécutable.</span><span class="sxs-lookup"><span data-stu-id="9606b-638">This is a free text field and can be useful in distinguishing multiple executables within a software package where there is a need to identify the function of the executable.</span></span>

<span data-ttu-id="9606b-639">Par exemple, dans une application adaptée, il peut être utile de fournir des rappels sur la fonction de deux exécutables (MyApplication.exe et MyApplicationHelper.exe), comme illustré ci-dessous:</span><span class="sxs-lookup"><span data-stu-id="9606b-639">For example, in a suited application, it might be useful to provide reminders about the function of two executables (MyApplication.exe and MyApplicationHelper.exe), as shown here:</span></span>

```xml
<Processes>
  <Process>
    <Filename>MyApplication.exe</Filename>
    <FileDescription>My Application Main Engine</ FileDescription>
    <ProductVersion>
      <Major Minimum="6" Maximum="6" />
    </ProductVersion>
  </Process>
  <Process>
    <Filename>MyApplicationHelper.exe</Filename>
    <FileDescription>My Application Background Process Executable</FileDescription>
    <ProductVersion>
      <Major Minimum="6" Maximum="6" />
    </ProductVersion>
  </Process>
</Processes>
```

### <span data-ttu-id="9606b-640">ProductVersion</span><span class="sxs-lookup"><span data-stu-id="9606b-640">ProductVersion</span></span>

**<span data-ttu-id="9606b-641">Obligatoire: faux</span><span class="sxs-lookup"><span data-stu-id="9606b-641">Mandatory: False</span></span>**

**<span data-ttu-id="9606b-642">Type: chaîne</span><span class="sxs-lookup"><span data-stu-id="9606b-642">Type: String</span></span>**

<span data-ttu-id="9606b-643">ProductVersion fait référence aux versions de produit principales et secondaires d’un fichier, ainsi qu’à un niveau de build et de correctif.</span><span class="sxs-lookup"><span data-stu-id="9606b-643">ProductVersion refers to the major and minor product versions of a file, as well as a build and patch level.</span></span> <span data-ttu-id="9606b-644">ProductVersion est un élément facultatif, mais si ce paramètre est spécifié, il doit contenir au moins l’élément enfant principal.</span><span class="sxs-lookup"><span data-stu-id="9606b-644">ProductVersion is an optional element, but if specified, it must contain at least the Major child element.</span></span> <span data-ttu-id="9606b-645">La valeur doit exprimer une plage au format minimum = «X» maximum = «Y» où X et Y sont des entiers.</span><span class="sxs-lookup"><span data-stu-id="9606b-645">The value must express a range in the form Minimum="X" Maximum="Y" where X and Y are integers.</span></span> <span data-ttu-id="9606b-646">Les valeurs minimales et maximales peuvent être identiques.</span><span class="sxs-lookup"><span data-stu-id="9606b-646">The Minimum and Maximum values can be identical.</span></span>

<span data-ttu-id="9606b-647">Le produit et les éléments de version du fichier ne sont pas spécifiés.</span><span class="sxs-lookup"><span data-stu-id="9606b-647">The product and file version elements may be left unspecified.</span></span> <span data-ttu-id="9606b-648">Cela rend le modèle «version agnostique», ce qui signifie que le modèle s’appliquera à toutes les versions du fichier exécutable spécifié.</span><span class="sxs-lookup"><span data-stu-id="9606b-648">Doing so makes the template “version agnostic”, meaning that the template will apply to all versions of the specified executable.</span></span>

**<span data-ttu-id="9606b-649">Exemple1:</span><span class="sxs-lookup"><span data-stu-id="9606b-649">Example 1:</span></span>**

<span data-ttu-id="9606b-650">Version du produit: 1,0 spécifiée dans UE-V Generator génère le code XML suivant:</span><span class="sxs-lookup"><span data-stu-id="9606b-650">Product version: 1.0 specified in the UE-V Generator produces the following XML:</span></span>

```xml
<ProductVersion>
  <Major Minimum="1" Maximum="1" />
  <Minor Minimum="0" Maximum="0" />
</ProductVersion>
```

**<span data-ttu-id="9606b-651">Exemple2:</span><span class="sxs-lookup"><span data-stu-id="9606b-651">Example 2:</span></span>**

<span data-ttu-id="9606b-652">Version du fichier: 5.0.2.1000 spécifiée dans UE-V Generator génère le code XML suivant:</span><span class="sxs-lookup"><span data-stu-id="9606b-652">File version: 5.0.2.1000 specified in the UE-V Generator produces the following XML:</span></span>

```xml
<FileVersion>
  <Major Minimum="5" Maximum="5" />
  <Minor Minimum="0" Maximum="0" />
  <Build Minimum="2" Maximum="2" />
  <Patch Minimum="1000" Maximum="1000" />
</FileVersion>
```

**<span data-ttu-id="9606b-653">Exemple incorrect 1 – plage incomplète:</span><span class="sxs-lookup"><span data-stu-id="9606b-653">Incorrect Example 1 – incomplete range:</span></span>**

<span data-ttu-id="9606b-654">Seul l’attribut minimum est présent.</span><span class="sxs-lookup"><span data-stu-id="9606b-654">Only the Minimum attribute is present.</span></span> <span data-ttu-id="9606b-655">La valeur maximale doit également être incluse dans une plage.</span><span class="sxs-lookup"><span data-stu-id="9606b-655">Maximum must be included in a range as well.</span></span>

```xml
<ProductVersion>
  <Major Minimum="2" />
</ProductVersion>
```

**<span data-ttu-id="9606b-656">Exemple 2 incorrect: Minor spécifié sans élément principal:</span><span class="sxs-lookup"><span data-stu-id="9606b-656">Incorrect Example 2 – Minor specified without Major element:</span></span>**

<span data-ttu-id="9606b-657">Seuls les éléments mineurs sont présents.</span><span class="sxs-lookup"><span data-stu-id="9606b-657">Only the Minor element is present.</span></span> <span data-ttu-id="9606b-658">Important doit également être inclus.</span><span class="sxs-lookup"><span data-stu-id="9606b-658">Major must be included as well.</span></span>

```xml
<ProductVersion>
  <Minor Minimum="0" Maximum="0" />
</ProductVersion>
```

### <span data-ttu-id="9606b-659">FileVersion</span><span class="sxs-lookup"><span data-stu-id="9606b-659">FileVersion</span></span>

**<span data-ttu-id="9606b-660">Obligatoire: faux</span><span class="sxs-lookup"><span data-stu-id="9606b-660">Mandatory: False</span></span>**

**<span data-ttu-id="9606b-661">Type: chaîne</span><span class="sxs-lookup"><span data-stu-id="9606b-661">Type: String</span></span>**

<span data-ttu-id="9606b-662">FileVersion fait la distinction entre la version commerciale d’une application publiée et les détails de la build interne d’un composant exécutable.</span><span class="sxs-lookup"><span data-stu-id="9606b-662">FileVersion differentiates between the release version of a published application and the internal build details of a component executable.</span></span> <span data-ttu-id="9606b-663">Ces numéros sont identiques pour la plupart des applications commerciales.</span><span class="sxs-lookup"><span data-stu-id="9606b-663">For the majority of commercial applications, these numbers are identical.</span></span> <span data-ttu-id="9606b-664">Le cas échéant, la version de produit d’un fichier indique une identification de version générique d’un fichier, tandis que la version du fichier indique une version spécifique d’un fichier (comme dans le cas d’un correctif ou d’une mise à jour).</span><span class="sxs-lookup"><span data-stu-id="9606b-664">Where they vary, the product version of a file indicates a generic version identification of a file, while file version indicates a specific build of a file (as in the case of a hotfix or update).</span></span> <span data-ttu-id="9606b-665">Cela identifie de façon unique les fichiers sans logique de détection de rupture.</span><span class="sxs-lookup"><span data-stu-id="9606b-665">This uniquely identifies files without breaking detection logic.</span></span>

<span data-ttu-id="9606b-666">Pour déterminer la version et la version du produit d’un fichier exécutable particulier, cliquez avec le bouton droit sur le fichier dans l’Explorateur Windows, sélectionnez Propriétés, puis cliquez sur l’onglet Détails.</span><span class="sxs-lookup"><span data-stu-id="9606b-666">To determine the product version and file version of a particular executable, right-click on the file in Windows Explorer, select Properties, then click on the Details tab.</span></span>

<span data-ttu-id="9606b-667">L’inclusion d’un élément FileVersion pour une application permet d’améliorer la logique de détection, mais n’est pas nécessaire pour la plupart des applications.</span><span class="sxs-lookup"><span data-stu-id="9606b-667">Including a FileVersion element for an application allows for more granular fine-tuning detection logic, but is not necessary for most applications.</span></span> <span data-ttu-id="9606b-668">Les paramètres de l’élément ProductVersion sont vérifiés en premier, puis FileVersion est activé.</span><span class="sxs-lookup"><span data-stu-id="9606b-668">The ProductVersion element settings are checked first, and then FileVersion is checked.</span></span> <span data-ttu-id="9606b-669">Le paramètre le plus restrictif s’applique.</span><span class="sxs-lookup"><span data-stu-id="9606b-669">The more restrictive setting will apply.</span></span>

<span data-ttu-id="9606b-670">Les éléments enfants et les règles de syntaxe pour FileVersion sont identiques à ceux de ProductVersion.</span><span class="sxs-lookup"><span data-stu-id="9606b-670">The child elements and syntax rules for FileVersion are identical to those of ProductVersion.</span></span>

```xml
<Process>
  <Filename>MSACCESS.EXE</Filename>
  <Architecture>Win32</Architecture>
  <ProductVersion>
    <Major Minimum="14" Maximum="14" />
    <Minor Minimum="0" Maximum="0" />
  </ProductVersion>
  <FileVersion>
    <Major Minimum="14" Maximum="14" />
    <Minor Minimum="0" Maximum="0" />
  </FileVersion>
</Process>
```

### <a href="" id="application"></a><span data-ttu-id="9606b-671">Élément application</span><span class="sxs-lookup"><span data-stu-id="9606b-671">Application Element</span></span>

<span data-ttu-id="9606b-672">Application est un conteneur pour les paramètres qui s’appliquent à une application particulière.</span><span class="sxs-lookup"><span data-stu-id="9606b-672">Application is a container for settings that apply to a particular application.</span></span> <span data-ttu-id="9606b-673">Il s’agit d’un ensemble de champs/types suivants.</span><span class="sxs-lookup"><span data-stu-id="9606b-673">It is a collection of the following fields/types.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9606b-674">Champ/type</span><span class="sxs-lookup"><span data-stu-id="9606b-674">Field/Type</span></span></th>
<th align="left"><span data-ttu-id="9606b-675">Description</span><span class="sxs-lookup"><span data-stu-id="9606b-675">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9606b-676">Name</span><span class="sxs-lookup"><span data-stu-id="9606b-676">Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="9606b-677">Spécifie un nom unique pour le modèle d’emplacement des paramètres.</span><span class="sxs-lookup"><span data-stu-id="9606b-677">Specifies a unique name for the settings location template.</span></span> <span data-ttu-id="9606b-678">Il est utilisé à des fins d’affichage lors du référencement du modèle dans WMI, PowerShell, Observateur d’événements et journaux de débogage.</span><span class="sxs-lookup"><span data-stu-id="9606b-678">This is used for display purposes when referencing the template in WMI, PowerShell, Event Viewer and debug logs.</span></span> <span data-ttu-id="9606b-679">Pour plus d’informations, reportez-vous à la section <a href="#name" data-raw-source="[Name](#name)"> nom </a> .</span><span class="sxs-lookup"><span data-stu-id="9606b-679">For more information, see <a href="#name" data-raw-source="[Name](#name)">Name</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9606b-680">ID</span><span class="sxs-lookup"><span data-stu-id="9606b-680">ID</span></span></p></td>
<td align="left"><p><span data-ttu-id="9606b-681">Remplit un identificateur unique pour un modèle particulier.</span><span class="sxs-lookup"><span data-stu-id="9606b-681">Populates a unique identifier for a particular template.</span></span> <span data-ttu-id="9606b-682">Cette balise devient l’identificateur principal utilisé par l’agent UE-V pour référencer le modèle lors de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="9606b-682">This tag becomes the primary identifier that the UE-V Agent uses to reference the template at runtime.</span></span> <span data-ttu-id="9606b-683">Pour plus d’informations, consultez la section <a href="#id" data-raw-source="[ID](#id)"> ID </a> .</span><span class="sxs-lookup"><span data-stu-id="9606b-683">For more information, see <a href="#id" data-raw-source="[ID](#id)">ID</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9606b-684">Description</span><span class="sxs-lookup"><span data-stu-id="9606b-684">Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="9606b-685">Description facultative du modèle.</span><span class="sxs-lookup"><span data-stu-id="9606b-685">An optional description of the template.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9606b-686">LocalizedNames</span><span class="sxs-lookup"><span data-stu-id="9606b-686">LocalizedNames</span></span></p></td>
<td align="left"><p><span data-ttu-id="9606b-687">Nom facultatif affiché dans l’interface utilisateur, localisé par des paramètres régionaux de langue.</span><span class="sxs-lookup"><span data-stu-id="9606b-687">An optional name displayed in the UI, localized by a language locale.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9606b-688">LocalizedDescriptions</span><span class="sxs-lookup"><span data-stu-id="9606b-688">LocalizedDescriptions</span></span></p></td>
<td align="left"><p><span data-ttu-id="9606b-689">Description de modèle facultative localisée par un paramètre régional de langue.</span><span class="sxs-lookup"><span data-stu-id="9606b-689">An optional template description localized by a language locale.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9606b-690">Version</span><span class="sxs-lookup"><span data-stu-id="9606b-690">Version</span></span></p></td>
<td align="left"><p><span data-ttu-id="9606b-691">Identifie la version du modèle d’emplacement des paramètres du suivi des modifications.</span><span class="sxs-lookup"><span data-stu-id="9606b-691">Identifies the version of the settings location template for administrative tracking of changes.</span></span> <span data-ttu-id="9606b-692">Pour plus d’informations, voir <a href="#version" data-raw-source="[Version](#version)"> version </a> .</span><span class="sxs-lookup"><span data-stu-id="9606b-692">For more information, see <a href="#version" data-raw-source="[Version](#version)">Version</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9606b-693">DeferToMSAccount</span><span class="sxs-lookup"><span data-stu-id="9606b-693">DeferToMSAccount</span></span></p></td>
<td align="left"><p><span data-ttu-id="9606b-694">Détermine si ce modèle est activé en conjonction avec un compte Microsoft.</span><span class="sxs-lookup"><span data-stu-id="9606b-694">Controls whether this template is enabled in conjunction with a Microsoft account or not.</span></span> <span data-ttu-id="9606b-695">Si la synchronisation MSA est activée pour un utilisateur sur un ordinateur, ce modèle sera automatiquement désactivé.</span><span class="sxs-lookup"><span data-stu-id="9606b-695">If MSA syncing is enabled for a user on a machine, then this template will automatically be disabled.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9606b-696">DeferToOffice365</span><span class="sxs-lookup"><span data-stu-id="9606b-696">DeferToOffice365</span></span></p></td>
<td align="left"><p><span data-ttu-id="9606b-697">Comme pour MSA, cette option détermine si ce modèle est activé en conjonction avec Office 365.</span><span class="sxs-lookup"><span data-stu-id="9606b-697">Similar to MSA, this controls whether this template is enabled in conjunction with Office365.</span></span> <span data-ttu-id="9606b-698">Si Office 365 est utilisé pour synchroniser les paramètres, ce modèle sera automatiquement désactivé.</span><span class="sxs-lookup"><span data-stu-id="9606b-698">If Office 365 is being used to sync settings, this template will automatically be disabled.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9606b-699">Processus</span><span class="sxs-lookup"><span data-stu-id="9606b-699">Processes</span></span></p></td>
<td align="left"><p><span data-ttu-id="9606b-700">Conteneur pour une collection d’un ou de plusieurs éléments de processus.</span><span class="sxs-lookup"><span data-stu-id="9606b-700">A container for a collection of one or more Process elements.</span></span> <span data-ttu-id="9606b-701">Pour plus d’informations, reportez-vous à la section <a href="#processes" data-raw-source="[Processes](#processes)"> processus </a> .</span><span class="sxs-lookup"><span data-stu-id="9606b-701">For more information, see <a href="#processes" data-raw-source="[Processes](#processes)">Processes</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9606b-702">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9606b-702">Settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="9606b-703">Conteneur de tous les paramètres qui s’appliquent à un modèle spécifique.</span><span class="sxs-lookup"><span data-stu-id="9606b-703">A container for all the settings that apply to a particular template.</span></span> <span data-ttu-id="9606b-704">Il contient des instances des paramètres de Registre, de fichier, de SystemParameter et de CustomAction.</span><span class="sxs-lookup"><span data-stu-id="9606b-704">It contains instances of the Registry, File, SystemParameter, and CustomAction settings.</span></span> <span data-ttu-id="9606b-705">Pour plus d’informations, consultez la section <strong> paramètres </strong> des <a href="#data" data-raw-source="[Data types](#data)"> types de données </a> .</span><span class="sxs-lookup"><span data-stu-id="9606b-705">For more information, see <strong>Settings</strong> in <a href="#data" data-raw-source="[Data types](#data)">Data types</a>.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="common"></a><span data-ttu-id="9606b-706">Élément commun</span><span class="sxs-lookup"><span data-stu-id="9606b-706">Common Element</span></span>

<span data-ttu-id="9606b-707">Common est semblable à un élément application, mais il est toujours associé à deux éléments d’application ou davantage.</span><span class="sxs-lookup"><span data-stu-id="9606b-707">Common is similar to an Application element, but it is always associated with two or more Application elements.</span></span> <span data-ttu-id="9606b-708">La section commune représente l’ensemble des paramètres qui sont partagés entre ces instances d’application.</span><span class="sxs-lookup"><span data-stu-id="9606b-708">The Common section represents the set of settings that are shared between those Application instances.</span></span> <span data-ttu-id="9606b-709">Il s’agit d’un ensemble de champs/types suivants.</span><span class="sxs-lookup"><span data-stu-id="9606b-709">It is a collection of the following fields/types.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9606b-710">Champ/type</span><span class="sxs-lookup"><span data-stu-id="9606b-710">Field/Type</span></span></th>
<th align="left"><span data-ttu-id="9606b-711">Description</span><span class="sxs-lookup"><span data-stu-id="9606b-711">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9606b-712">Name</span><span class="sxs-lookup"><span data-stu-id="9606b-712">Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="9606b-713">Spécifie un nom unique pour le modèle d’emplacement des paramètres.</span><span class="sxs-lookup"><span data-stu-id="9606b-713">Specifies a unique name for the settings location template.</span></span> <span data-ttu-id="9606b-714">Il est utilisé à des fins d’affichage lors du référencement du modèle dans WMI, PowerShell, Observateur d’événements et journaux de débogage.</span><span class="sxs-lookup"><span data-stu-id="9606b-714">This is used for display purposes when referencing the template in WMI, PowerShell, Event Viewer and debug logs.</span></span> <span data-ttu-id="9606b-715">Pour plus d’informations, reportez-vous à la section <a href="#name" data-raw-source="[Name](#name)"> nom </a> .</span><span class="sxs-lookup"><span data-stu-id="9606b-715">For more information, see <a href="#name" data-raw-source="[Name](#name)">Name</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9606b-716">ID</span><span class="sxs-lookup"><span data-stu-id="9606b-716">ID</span></span></p></td>
<td align="left"><p><span data-ttu-id="9606b-717">Remplit un identificateur unique pour un modèle particulier.</span><span class="sxs-lookup"><span data-stu-id="9606b-717">Populates a unique identifier for a particular template.</span></span> <span data-ttu-id="9606b-718">Cette balise devient l’identificateur principal utilisé par l’agent UE-V pour référencer le modèle lors de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="9606b-718">This tag becomes the primary identifier that the UE-V Agent uses to reference the template at runtime.</span></span> <span data-ttu-id="9606b-719">Pour plus d’informations, consultez la section <a href="#id" data-raw-source="[ID](#id)"> ID </a> .</span><span class="sxs-lookup"><span data-stu-id="9606b-719">For more information, see <a href="#id" data-raw-source="[ID](#id)">ID</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9606b-720">Description</span><span class="sxs-lookup"><span data-stu-id="9606b-720">Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="9606b-721">Description facultative du modèle.</span><span class="sxs-lookup"><span data-stu-id="9606b-721">An optional description of the template.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9606b-722">LocalizedNames</span><span class="sxs-lookup"><span data-stu-id="9606b-722">LocalizedNames</span></span></p></td>
<td align="left"><p><span data-ttu-id="9606b-723">Nom facultatif affiché dans l’interface utilisateur, localisé par des paramètres régionaux de langue.</span><span class="sxs-lookup"><span data-stu-id="9606b-723">An optional name displayed in the UI, localized by a language locale.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9606b-724">LocalizedDescriptions</span><span class="sxs-lookup"><span data-stu-id="9606b-724">LocalizedDescriptions</span></span></p></td>
<td align="left"><p><span data-ttu-id="9606b-725">Description de modèle facultative localisée par un paramètre régional de langue.</span><span class="sxs-lookup"><span data-stu-id="9606b-725">An optional template description localized by a language locale.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9606b-726">Version</span><span class="sxs-lookup"><span data-stu-id="9606b-726">Version</span></span></p></td>
<td align="left"><p><span data-ttu-id="9606b-727">Identifie la version du modèle d’emplacement des paramètres du suivi des modifications.</span><span class="sxs-lookup"><span data-stu-id="9606b-727">Identifies the version of the settings location template for administrative tracking of changes.</span></span> <span data-ttu-id="9606b-728">Pour plus d’informations, voir <a href="#version" data-raw-source="[Version](#version)"> version </a> .</span><span class="sxs-lookup"><span data-stu-id="9606b-728">For more information, see <a href="#version" data-raw-source="[Version](#version)">Version</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9606b-729">DeferToMSAccount</span><span class="sxs-lookup"><span data-stu-id="9606b-729">DeferToMSAccount</span></span></p></td>
<td align="left"><p><span data-ttu-id="9606b-730">Détermine si ce modèle est activé en conjonction avec un compte Microsoft.</span><span class="sxs-lookup"><span data-stu-id="9606b-730">Controls whether this template is enabled in conjunction with a Microsoft account or not.</span></span> <span data-ttu-id="9606b-731">Si la synchronisation MSA est activée pour un utilisateur sur un ordinateur, ce modèle sera automatiquement désactivé.</span><span class="sxs-lookup"><span data-stu-id="9606b-731">If MSA syncing is enabled for a user on a machine, then this template will automatically be disabled.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9606b-732">DeferToOffice365</span><span class="sxs-lookup"><span data-stu-id="9606b-732">DeferToOffice365</span></span></p></td>
<td align="left"><p><span data-ttu-id="9606b-733">Comme pour MSA, cette option détermine si ce modèle est activé en conjonction avec Office 365.</span><span class="sxs-lookup"><span data-stu-id="9606b-733">Similar to MSA, this controls whether this template is enabled in conjunction with Office365.</span></span> <span data-ttu-id="9606b-734">Si Office 365 est utilisé pour synchroniser les paramètres, ce modèle sera automatiquement désactivé.</span><span class="sxs-lookup"><span data-stu-id="9606b-734">If Office 365 is being used to sync settings, this template will automatically be disabled.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9606b-735">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9606b-735">Settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="9606b-736">Conteneur de tous les paramètres qui s’appliquent à un modèle spécifique.</span><span class="sxs-lookup"><span data-stu-id="9606b-736">A container for all the settings that apply to a particular template.</span></span> <span data-ttu-id="9606b-737">Il contient des instances des paramètres de Registre, de fichier, de SystemParameter et de CustomAction.</span><span class="sxs-lookup"><span data-stu-id="9606b-737">It contains instances of the Registry, File, SystemParameter, and CustomAction settings.</span></span> <span data-ttu-id="9606b-738">Pour plus d’informations, consultez la section <strong> paramètres </strong> des <a href="#data" data-raw-source="[Data types](#data)"> types de données </a> .</span><span class="sxs-lookup"><span data-stu-id="9606b-738">For more information, see <strong>Settings</strong> in <a href="#data" data-raw-source="[Data types](#data)">Data types</a>.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="settingslocationtemplate"></a><span data-ttu-id="9606b-739">Élément SettingsLocationTemplate</span><span class="sxs-lookup"><span data-stu-id="9606b-739">SettingsLocationTemplate Element</span></span>

<span data-ttu-id="9606b-740">Cet élément définit les paramètres d’une application unique ou d’une suite d’applications.</span><span class="sxs-lookup"><span data-stu-id="9606b-740">This element defines the settings for a single application or a suite of applications.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9606b-741">Champ/type</span><span class="sxs-lookup"><span data-stu-id="9606b-741">Field/Type</span></span></th>
<th align="left"><span data-ttu-id="9606b-742">Description</span><span class="sxs-lookup"><span data-stu-id="9606b-742">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9606b-743">Name</span><span class="sxs-lookup"><span data-stu-id="9606b-743">Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="9606b-744">Spécifie un nom unique pour le modèle d’emplacement des paramètres.</span><span class="sxs-lookup"><span data-stu-id="9606b-744">Specifies a unique name for the settings location template.</span></span> <span data-ttu-id="9606b-745">Il est utilisé à des fins d’affichage lors du référencement du modèle dans WMI, PowerShell, Observateur d’événements et journaux de débogage.</span><span class="sxs-lookup"><span data-stu-id="9606b-745">This is used for display purposes when referencing the template in WMI, PowerShell, Event Viewer and debug logs.</span></span> <span data-ttu-id="9606b-746">Pour plus d’informations, reportez-vous à la section <a href="#name" data-raw-source="[Name](#name)"> nom </a> .</span><span class="sxs-lookup"><span data-stu-id="9606b-746">For more information, see <a href="#name" data-raw-source="[Name](#name)">Name</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9606b-747">ID</span><span class="sxs-lookup"><span data-stu-id="9606b-747">ID</span></span></p></td>
<td align="left"><p><span data-ttu-id="9606b-748">Remplit un identificateur unique pour un modèle particulier.</span><span class="sxs-lookup"><span data-stu-id="9606b-748">Populates a unique identifier for a particular template.</span></span> <span data-ttu-id="9606b-749">Cette balise devient l’identificateur principal utilisé par l’agent UE-V pour référencer le modèle lors de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="9606b-749">This tag becomes the primary identifier that the UE-V Agent uses to reference the template at runtime.</span></span> <span data-ttu-id="9606b-750">Pour plus d’informations, consultez la section <a href="#id" data-raw-source="[ID](#id)"> ID </a> .</span><span class="sxs-lookup"><span data-stu-id="9606b-750">For more information, see <a href="#id" data-raw-source="[ID](#id)">ID</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9606b-751">Description</span><span class="sxs-lookup"><span data-stu-id="9606b-751">Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="9606b-752">Description facultative du modèle.</span><span class="sxs-lookup"><span data-stu-id="9606b-752">An optional description of the template.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9606b-753">LocalizedNames</span><span class="sxs-lookup"><span data-stu-id="9606b-753">LocalizedNames</span></span></p></td>
<td align="left"><p><span data-ttu-id="9606b-754">Nom facultatif affiché dans l’interface utilisateur, localisé par des paramètres régionaux de langue.</span><span class="sxs-lookup"><span data-stu-id="9606b-754">An optional name displayed in the UI, localized by a language locale.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9606b-755">LocalizedDescriptions</span><span class="sxs-lookup"><span data-stu-id="9606b-755">LocalizedDescriptions</span></span></p></td>
<td align="left"><p><span data-ttu-id="9606b-756">Description de modèle facultative localisée par un paramètre régional de langue.</span><span class="sxs-lookup"><span data-stu-id="9606b-756">An optional template description localized by a language locale.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="appendix"></a><span data-ttu-id="9606b-757">Annexe: SettingsLocationTemplate. xsd</span><span class="sxs-lookup"><span data-stu-id="9606b-757">Appendix: SettingsLocationTemplate.xsd</span></span>

<span data-ttu-id="9606b-758">Voici le fichier SettingsLocationTemplate. xsd montrant ses éléments, éléments enfants, attributs et paramètres:</span><span class="sxs-lookup"><span data-stu-id="9606b-758">Here is the SettingsLocationTemplate.xsd file showing its elements, child elements, attributes, and parameters:</span></span>

```xml
<?xml version="1.0" encoding="utf-8"?>
<xs:schema id="UevSettingsLocationTemplate"
  targetNamespace="https://schemas.microsoft.com/UserExperienceVirtualization/2013/SettingsLocationTemplate"
  elementFormDefault="qualified"
  xmlns="https://schemas.microsoft.com/UserExperienceVirtualization/2013/SettingsLocationTemplate"
  xmlns:mstns="https://schemas.microsoft.com/UserExperienceVirtualization/2013/SettingsLocationTemplate"
  xmlns:xs="http://www.w3.org/2001/XMLSchema">

  <xs:simpleType name="Guid">
    <xs:restriction base="xs:string">
      <xs:pattern value="\{[a-fA-F0-9]{8}-[a-fA-F0-9]{4}-[a-fA-F0-9]{4}-[a-fA-F0-9]{4}-[a-fA-F0-9]{12}\}" />
    </xs:restriction>
  </xs:simpleType>

  <xs:simpleType name="FilenameString">
    <xs:restriction base="xs:string">
      <xs:pattern value="[^\\\?\*\|&lt;&gt;/:]+" />
    </xs:restriction>
  </xs:simpleType>

  <xs:simpleType name="IDString">
    <xs:restriction base="xs:string">
      <xs:pattern value="[^\\\?\*\|&lt;&gt;/:.]+" />
    </xs:restriction>
  </xs:simpleType>

  <xs:simpleType name="TemplateVersion">
    <xs:restriction base="xs:integer">
      <xs:minInclusive value="0" />
      <xs:maxInclusive value="2147483647" />
    </xs:restriction>
  </xs:simpleType>

  <xs:complexType name="Empty">
    <xs:sequence/>
  </xs:complexType>

  <xs:complexType name="LocalizedString">
    <xs:simpleContent>
      <xs:extension base="xs:string">
        <xs:attribute name="Locale" type="xs:string" use="required"/>
      </xs:extension>
    </xs:simpleContent>
  </xs:complexType>

  <xs:complexType name="LocalizedName">
    <xs:sequence>
      <xs:element name="Name" type="LocalizedString" minOccurs="1" maxOccurs="unbounded" />
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="LocalizedDescription">
    <xs:sequence>
      <xs:element name="Description" type="LocalizedString" minOccurs="1" maxOccurs="unbounded" />
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="Author">
    <xs:all>
      <xs:element name="Name" type="xs:string" minOccurs="1" />
      <xs:element name="Email" type="xs:string" minOccurs="0" />
    </xs:all>
  </xs:complexType>

  <xs:complexType name="Range">
    <xs:attribute name="Minimum" type="xs:integer" use="required"/>
    <xs:attribute name="Maximum" type="xs:integer" use="required"/>
  </xs:complexType>

  <xs:complexType name="ProcessVersion">
    <xs:sequence>
      <xs:element name="Major" type="Range" minOccurs="1" />
      <xs:element name="Minor" type="Range" minOccurs="0" />
      <xs:element name="Build" type="Range" minOccurs="0" />
      <xs:element name="Patch" type="Range" minOccurs="0" />
    </xs:sequence>
  </xs:complexType>

  <xs:simpleType name="Architecture">
    <xs:restriction base="xs:string">
      <xs:enumeration value="Win32"/>
      <xs:enumeration value="Win64"/>
    </xs:restriction>
  </xs:simpleType>

  <xs:complexType name="Process">
    <xs:sequence>
      <xs:element name="Filename" type="FilenameString" minOccurs="1" />
      <xs:element name="Architecture" type="Architecture" minOccurs="0" />
      <xs:element name="ProductName" type="xs:string" minOccurs="0" />
      <xs:element name="FileDescription" type="xs:string" minOccurs="0" />
      <xs:element name="ProductVersion" type="ProcessVersion" minOccurs="0" maxOccurs="unbounded"/>
      <xs:element name="FileVersion" type="ProcessVersion" minOccurs="0" maxOccurs="unbounded"/>
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="Processes">
    <xs:sequence>
      <xs:choice minOccurs="1">
        <xs:element name="Process" type="Process" />
        <xs:element name="ShellProcess" type="Empty" />
      </xs:choice>
      <xs:element name="Process" type="Process" minOccurs="0" maxOccurs="unbounded" />
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="Path">
    <xs:simpleContent>
      <xs:extension base="xs:string">
        <xs:attribute name="Recursive" type="xs:boolean" default="false"/>
        <xs:attribute name="DeleteIfNotFound" type="xs:boolean" default="false"/>
      </xs:extension>
    </xs:simpleContent>
  </xs:complexType>

  <xs:complexType name="RegistrySetting">
    <xs:sequence>
      <xs:element name="Path" type="Path" />
      <xs:element name="Name" type="xs:string" minOccurs="0" maxOccurs="unbounded" />
      <xs:element name="Exclude" minOccurs="0" maxOccurs="unbounded">
        <xs:complexType>
          <xs:sequence>
            <xs:element name="Path" type="Path" minOccurs="0" />
            <xs:element name="Name" type="xs:string" minOccurs="0" maxOccurs="unbounded" />
          </xs:sequence>
        </xs:complexType>
      </xs:element>
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="FileSetting">
    <xs:sequence>

      <xs:element name="Root">
        <xs:complexType>
          <xs:choice>
            <xs:element name="KnownFolder" type="Guid" />
            <xs:element name="RegistryEntry" type="xs:string" />
            <xs:element name="EnvironmentVariable" type="xs:string" />
          </xs:choice>
        </xs:complexType>
      </xs:element>

      <xs:element name="Path" minOccurs="0" type="Path" />
      <xs:element name="FileMask" type="xs:string" minOccurs="0" maxOccurs="unbounded"/>

      <xs:element name="Exclude" minOccurs="0" maxOccurs="unbounded">
        <xs:complexType>
          <xs:sequence>
            <xs:element name="Path" type="Path" minOccurs="0" />
            <xs:element name="FileMask" type="xs:string" minOccurs="0" maxOccurs="unbounded" />
          </xs:sequence>
        </xs:complexType>
      </xs:element>

    </xs:sequence>
  </xs:complexType>

  <xs:simpleType name="SystemParameterSetting">
    <xs:restriction base="xs:string">

      <!-- Accessibility parameters -->
      <xs:enumeration value="AccessTimeout"/>
      <xs:enumeration value="AudioDescription"/>
      <xs:enumeration value="ClientAreaAnimation"/>
      <xs:enumeration value="DisableOverlappedContent"/>
      <xs:enumeration value="FilterKeys"/>
      <xs:enumeration value="FocusBorderHeight"/>
      <xs:enumeration value="FocusBorderWidth"/>
      <xs:enumeration value="HighContrast"/>
      <xs:enumeration value="MessageDuration"/>
      <xs:enumeration value="MouseClickLock"/>
      <xs:enumeration value="MouseClickLockTime"/>
      <xs:enumeration value="MouseKeys"/>
      <xs:enumeration value="MouseSonar"/>
      <xs:enumeration value="MouseVanish"/>
      <xs:enumeration value="ScreenReader"/>
      <xs:enumeration value="ShowSounds"/>
      <xs:enumeration value="SoundSentry"/>
      <xs:enumeration value="StickyKeys"/>
      <xs:enumeration value="ToggleKeys"/>

      <!-- Input parameters -->
      <xs:enumeration value="Beep"/>
      <xs:enumeration value="BlockSendInputResets"/>
      <xs:enumeration value="DefaultInputLang"/>
      <xs:enumeration value="DoubleClickTime"/>
      <xs:enumeration value="DoubleClkHeight"/>
      <xs:enumeration value="DoubleClkWidth"/>
      <xs:enumeration value="KeyboardCues"/>
      <xs:enumeration value="KeyboardDelay"/>
      <xs:enumeration value="KeyboardPref"/>
      <xs:enumeration value="KeyboardSpeed"/>
      <xs:enumeration value="Mouse"/>
      <xs:enumeration value="MouseButtonSwap"/>
      <xs:enumeration value="MouseHoverHeight"/>
      <xs:enumeration value="MouseHoverTime"/>
      <xs:enumeration value="MouseHoverWidth"/>
      <xs:enumeration value="MouseSpeed"/>
      <xs:enumeration value="MouseTrails"/>
      <xs:enumeration value="SnapToDefButton"/>
      <xs:enumeration value="WheelScrollChars"/>
      <xs:enumeration value="WheelScrollLines"/>

      <!-- Desktop parameters (limited subset) -->
      <xs:enumeration value="DeskWallpaper"/>
      <xs:enumeration value="DesktopColor"/>

    </xs:restriction>
  </xs:simpleType>

  <xs:complexType name="Settings">
    <xs:sequence>
      <xs:element name="Asynchronous" type="xs:boolean" minOccurs="0" />
      <xs:element name="PreventOverlappingSynchronization" type="xs:boolean" minOccurs="0" />
      <xs:choice minOccurs="0" maxOccurs="unbounded">
        <xs:element name="Registry" type="RegistrySetting" />
        <xs:element name="File" type="FileSetting" />
        <xs:element name="SystemParameter" type="SystemParameterSetting" />
      </xs:choice>
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="Common">
    <xs:sequence>
      <xs:element name="Name" type="xs:string" />
      <xs:element name="ID" type="IDString" />
      <xs:element name="Description" type="xs:string" minOccurs="0" />
      <xs:element name="LocalizedNames" type="LocalizedName" minOccurs="0" />
      <xs:element name="LocalizedDescriptions" type="LocalizedDescription" minOccurs="0" />
      <xs:element name="Version" type="xs:integer" />
      <xs:element name="DeferToMSAccount" type="Empty"  minOccurs="0" />
      <xs:element name="Settings" type="Settings" />
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="Application">
    <xs:sequence>
      <xs:element name="Name" type="xs:string" />
      <xs:element name="ID" type="IDString" />
      <xs:element name="Description" type="xs:string" minOccurs="0" />
      <xs:element name="LocalizedNames" type="LocalizedName" minOccurs="0" />
      <xs:element name="LocalizedDescriptions" type="LocalizedDescription" minOccurs="0" />
      <xs:element name="Version" type="xs:integer" />
      <xs:element name="DeferToMSAccount" type="Empty"  minOccurs="0" />
      <xs:element name="Processes" type="Processes" />
      <xs:element name="Settings" type="Settings" />
    </xs:sequence>
  </xs:complexType>


  <xs:element name="SettingsLocationTemplate">
    <xs:complexType>
      <xs:sequence>

        <xs:element name="Name" type="xs:string" />
        <xs:element name="ID" type="IDString" />
        <xs:element name="Description" type="xs:string" minOccurs="0" />
        <xs:element name="LocalizedNames" type="LocalizedName" minOccurs="0" />
        <xs:element name="LocalizedDescriptions" type="LocalizedDescription" minOccurs="0" />

        <xs:choice>

          <!-- Single application -->
          <xs:sequence>
            <xs:element name="Version" type="TemplateVersion" />
            <xs:element name="Author" type="Author" minOccurs="0" />
            <xs:element name="DeferToMSAccount" type="Empty"  minOccurs="0" />
            <xs:element name="Processes" type="Processes" />
            <xs:element name="Settings" type="Settings" />
          </xs:sequence>

          <!-- Suite of applications -->
          <xs:sequence>
            <xs:element name="ManageSuiteOnly" type="xs:boolean" minOccurs="0" />
            <xs:element name="Author" type="Author" minOccurs="0" />
            <xs:element name="Common" type="Common" />
            <xs:element name="Application" type="Application" minOccurs="2" maxOccurs="unbounded" />
          </xs:sequence>

        </xs:choice>

      </xs:sequence>
    </xs:complexType>
  </xs:element>
  <!-- SettingsLocationTemplate -->

</xs:schema>
```






## <span data-ttu-id="9606b-759">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9606b-759">Related topics</span></span>


[<span data-ttu-id="9606b-760">Utilisation de modèles UE-V 2 ou x personnalisés et du générateur UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="9606b-760">Working with Custom UE-V 2.x Templates and the UE-V 2.x Generator</span></span>](working-with-custom-ue-v-2x-templates-and-the-ue-v-2x-generator-new-uevv2.md)

[<span data-ttu-id="9606b-761">Informations techniques de référence sur UE-V2.x</span><span class="sxs-lookup"><span data-stu-id="9606b-761">Technical Reference for UE-V 2.x</span></span>](technical-reference-for-ue-v-2x-both-uevv2.md)

 

 





