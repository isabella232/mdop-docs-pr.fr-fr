---
title: Virtualisation de l’utilisation de l’utilisateur Microsoft (UE-V) 2. x
description: Virtualisation de l’utilisation de l’utilisateur Microsoft (UE-V) 2. x
author: dansimp
ms.assetid: b860fed0-b846-415d-bdd6-ba60231a64be
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 04/19/2017
ms.openlocfilehash: 573b8bb2027e5c7f117a8254005a43c656f047a9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10795817"
---
# <span data-ttu-id="c1327-103">Virtualisation de l’utilisation de l’utilisateur Microsoft (UE-V) 2. x</span><span class="sxs-lookup"><span data-stu-id="c1327-103">Microsoft User Experience Virtualization (UE-V) 2.x</span></span>

>[!NOTE]
><span data-ttu-id="c1327-104">Cette documentation est une version de UE-V incluse dans le pack d’optimisation du bureau Microsoft (MDOP).</span><span class="sxs-lookup"><span data-stu-id="c1327-104">This documentation is a for version of UE-V that was included in the Microsoft Desktop Optimization Pack (MDOP).</span></span> <span data-ttu-id="c1327-105">Pour plus d’informations sur la dernière version de UE-V incluse dans Windows 10 entreprise, voir [prise en main d’UE-v](https://docs.microsoft.com/windows/configuration/ue-v/uev-getting-started).</span><span class="sxs-lookup"><span data-stu-id="c1327-105">For information about the latest version of UE-V which is included in Windows 10 Enterprise, see [Get Started with UE-V](https://docs.microsoft.com/windows/configuration/ue-v/uev-getting-started).</span></span>


<span data-ttu-id="c1327-106">Capturez et centralisez les paramètres d’application de vos utilisateurs et les paramètres du système d’exploitation Windows en implémentant Microsoft User Interface Virtualization (UE-V) 2,0 ou 2,1.</span><span class="sxs-lookup"><span data-stu-id="c1327-106">Capture and centralize your users’ application settings and Windows OS settings by implementing Microsoft User Experience Virtualization (UE-V) 2.0 or 2.1.</span></span> <span data-ttu-id="c1327-107">Appliquez ensuite ces paramètres aux appareils accessibles aux utilisateurs de votre entreprise, par exemple, ordinateurs de bureau, ordinateurs portables ou sessions VDI (Virtual Desktop Infrastructure).</span><span class="sxs-lookup"><span data-stu-id="c1327-107">Then, apply these settings to the devices users access in your enterprise, like desktop computers, laptops, or virtual desktop infrastructure (VDI) sessions.</span></span>

**<span data-ttu-id="c1327-108">Avec UE-V, vous pouvez...</span><span class="sxs-lookup"><span data-stu-id="c1327-108">With UE-V you can…</span></span>**

-   <span data-ttu-id="c1327-109">Spécifier les paramètres de l’application et du bureau qui sont synchronisés</span><span class="sxs-lookup"><span data-stu-id="c1327-109">Specify which application and desktop settings synchronize</span></span>

-   <span data-ttu-id="c1327-110">Transmettre les paramètres à toute heure et en tout lieu de travail des utilisateurs au sein de l’entreprise</span><span class="sxs-lookup"><span data-stu-id="c1327-110">Deliver the settings anytime and anywhere users work throughout the enterprise</span></span>

-   <span data-ttu-id="c1327-111">Créer des modèles personnalisés pour vos applications cœur de métier ou tierces</span><span class="sxs-lookup"><span data-stu-id="c1327-111">Create custom templates for your third-party or line-of-business applications</span></span>

-   <span data-ttu-id="c1327-112">Récupérer les paramètres après un remplacement ou une mise à niveau du matériel, ou après la recréation de l’image d’une machine virtuelle à son état initial</span><span class="sxs-lookup"><span data-stu-id="c1327-112">Recover settings after hardware replacement or upgrade, or after reimaging a virtual machine to its initial state</span></span>

## <span data-ttu-id="c1327-113">Composants d’UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="c1327-113">Components of UE-V 2.x</span></span>


<span data-ttu-id="c1327-114">Le diagramme suivant montre comment les composants UE-V déployés collaborent pour synchroniser les paramètres.</span><span class="sxs-lookup"><span data-stu-id="c1327-114">This diagram shows how deployed UE-V components work together to synchronize settings.</span></span>

![diagramme d’architecture uev2](images/uev2archdiagram.gif)

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c1327-116">Composant</span><span class="sxs-lookup"><span data-stu-id="c1327-116">Component</span></span></th>
<th align="left"><span data-ttu-id="c1327-117">Fonction</span><span class="sxs-lookup"><span data-stu-id="c1327-117">Function</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="c1327-118">Agent UE-V</span><span class="sxs-lookup"><span data-stu-id="c1327-118">UE-V Agent</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="c1327-119">Installés sur tous les ordinateurs qui doivent synchroniser les paramètres, l' <strong> agent UE-V </strong> surveille les applications inscrites et le système d’exploitation en fonction des modifications apportées aux paramètres, puis synchronise ces paramètres entre eux.</span><span class="sxs-lookup"><span data-stu-id="c1327-119">Installed on every computer that needs to synchronize settings, the <strong>UE-V Agent</strong> monitors registered applications and the operating system for any settings changes, then synchronizes those settings between computers.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="c1327-120">Packages de paramètres</span><span class="sxs-lookup"><span data-stu-id="c1327-120">Settings packages</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="c1327-121">Les paramètres d’application et les paramètres Windows sont stockés dans <strong> les packages de paramètres </strong> créés par l’agent UE-V.</span><span class="sxs-lookup"><span data-stu-id="c1327-121">Application settings and Windows settings are stored in <strong>settings packages</strong> created by the UE-V Agent.</span></span> <span data-ttu-id="c1327-122">Les packages de paramètres sont développés, stockés en local et copiés sur l’emplacement de stockage des paramètres.</span><span class="sxs-lookup"><span data-stu-id="c1327-122">Settings packages are built, locally stored, and copied to the settings storage location.</span></span></p>
<ul>
<li><p><span data-ttu-id="c1327-123">Les valeurs de paramètres des <strong> applications de bureau </strong> sont stockées lorsque l’utilisateur ferme l’application.</span><span class="sxs-lookup"><span data-stu-id="c1327-123">The setting values for <strong>desktop applications</strong> are stored when the user closes the application.</span></span></p></li>
<li><p><span data-ttu-id="c1327-124">Les valeurs des <strong> Paramètres Windows </strong> sont stockées lorsque l’utilisateur se déconnecte, lorsque l’ordinateur est verrouillé, ou lorsque l’utilisateur se déconnecte à distance à partir d’un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c1327-124">Values for <strong>Windows settings</strong> are stored when the user logs off, when the computer is locked, or when the user disconnects remotely from a computer.</span></span></p></li>
</ul>
<p><span data-ttu-id="c1327-125">Le fournisseur de synchronisation détermine à quel moment les paramètres des applications ou du système d’exploitation sont lus à partir des <strong> packages de paramètres </strong> et synchronisés.</span><span class="sxs-lookup"><span data-stu-id="c1327-125">The sync provider determines when the application or operating system settings are read from the <strong>Settings Packages</strong> and synchronized.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="c1327-126">Emplacement de stockage des paramètres</span><span class="sxs-lookup"><span data-stu-id="c1327-126">Settings storage location</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="c1327-127">Ce partage réseau standard peut être accessible à vos utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="c1327-127">This is a standard network share that your users can access.</span></span> <span data-ttu-id="c1327-128">L’agent UE-V vérifie l’emplacement et crée un dossier système caché dans lequel stocker et récupérer des paramètres d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c1327-128">The UE-V Agent verifies the location and creates a hidden system folder in which to store and retrieve user settings.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="c1327-129">Modèles d’emplacement des paramètres</span><span class="sxs-lookup"><span data-stu-id="c1327-129">Settings location templates</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="c1327-130">UE-V utilise des fichiers XML comme modèles d’emplacement des paramètres pour surveiller et synchroniser les paramètres des applications de bureau et les paramètres de bureau Windows entre les ordinateurs des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="c1327-130">UE-V uses XML files as settings location templates to monitor and synchronize desktop application settings and Windows desktop settings between user computers.</span></span> <span data-ttu-id="c1327-131">Par défaut, certains modèles d’emplacement des paramètres sont inclus dans UE-V.</span><span class="sxs-lookup"><span data-stu-id="c1327-131">By default, some settings location templates are included in UE-V .</span></span> <span data-ttu-id="c1327-132">Vous pouvez également créer, modifier ou valider des modèles d’emplacements de paramètres personnalisés en <a href="#customapps" data-raw-source="[managing settings synchronization for custom applications](#customapps)"> gérant la synchronisation des paramètres pour des applications personnalisées </a> .</span><span class="sxs-lookup"><span data-stu-id="c1327-132">You can also create, edit, or validate custom settings location templates by <a href="#customapps" data-raw-source="[managing settings synchronization for custom applications](#customapps)">managing settings synchronization for custom applications</a>.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="c1327-133">Remarque</span><span class="sxs-lookup"><span data-stu-id="c1327-133">Note</span></span></strong><br/><p><span data-ttu-id="c1327-134">Les modèles d’emplacement des paramètres ne sont pas requis pour les applications Windows.</span><span class="sxs-lookup"><span data-stu-id="c1327-134">Settings location templates are not required for Windows apps.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="c1327-135">Liste des applications Windows</span><span class="sxs-lookup"><span data-stu-id="c1327-135">Windows app list</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="c1327-136">Les paramètres des applications Windows sont capturés et appliqués dynamiquement.</span><span class="sxs-lookup"><span data-stu-id="c1327-136">Settings for Windows apps are captured and applied dynamically.</span></span> <span data-ttu-id="c1327-137">Le développeur de l’application spécifie les paramètres qui sont synchronisés pour chaque application.</span><span class="sxs-lookup"><span data-stu-id="c1327-137">The app developer specifies the settings that are synchronized for each app.</span></span> <span data-ttu-id="c1327-138">UE-V détermine les applications Windows qui sont activées pour la synchronisation des paramètres à l’aide d’une liste gérée d’applications.</span><span class="sxs-lookup"><span data-stu-id="c1327-138">UE-V determines which Windows apps are enabled for settings synchronization using a managed list of apps.</span></span> <span data-ttu-id="c1327-139">Par défaut, cette liste inclut la plupart des applications Windows.</span><span class="sxs-lookup"><span data-stu-id="c1327-139">By default, this list includes most Windows apps.</span></span></p>
<p><span data-ttu-id="c1327-140">Vous pouvez ajouter ou supprimer des applications dans la liste des applications Windows en suivant les procédures décrites dans <a href="https://technet.microsoft.com/library/dn458925.aspx" data-raw-source="[here](https://technet.microsoft.com/library/dn458925.aspx)"> cet article </a> .</span><span class="sxs-lookup"><span data-stu-id="c1327-140">You can add or remove applications in the Windows app list by following the procedures shown <a href="https://technet.microsoft.com/library/dn458925.aspx" data-raw-source="[here](https://technet.microsoft.com/library/dn458925.aspx)">here</a>.</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="customapps"></a><span data-ttu-id="c1327-141">Gestion de la synchronisation des paramètres pour des applications personnalisées</span><span class="sxs-lookup"><span data-stu-id="c1327-141">Managing Settings Synchronization for Custom Applications</span></span>

<span data-ttu-id="c1327-142">Utilisez ces composants UE-V pour créer et gérer des modèles personnalisés pour vos applications tierces ou métier.</span><span class="sxs-lookup"><span data-stu-id="c1327-142">Use these UE-V components to create and manage custom templates for your third-party or line-of-business applications.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="c1327-143">Générateur UE-V</span><span class="sxs-lookup"><span data-stu-id="c1327-143">UE-V Generator</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="c1327-144">Servez <strong> -vous du générateur UE-V </strong> pour créer des modèles d’emplacements de paramètres personnalisés que vous pouvez distribuer ensuite sur les ordinateurs des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="c1327-144">Use the <strong>UE-V Generator</strong> to create custom settings location templates that you can then distribute to user computers.</span></span> <span data-ttu-id="c1327-145">Le générateur UE-V vous permet également de modifier un modèle existant ou de valider un modèle qui a été créé à l’aide d’un autre éditeur XML.</span><span class="sxs-lookup"><span data-stu-id="c1327-145">The UE-V Generator also lets you edit an existing template or validate a template that was created by using another XML editor.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="c1327-146">Catalogue de modèles de paramètres</span><span class="sxs-lookup"><span data-stu-id="c1327-146">Settings template catalog</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="c1327-147">Le <strong> catalogue de modèles </strong> de paramètres est un chemin de dossier sur les ordinateurs UE-V ou un partage réseau de blocs de messages serveur (SMB) qui stocke les modèles d’emplacement des paramètres personnalisés.</span><span class="sxs-lookup"><span data-stu-id="c1327-147">The <strong>settings template catalog</strong> is a folder path on UE-V computers or a Server Message Block (SMB) network share that stores the custom settings location templates.</span></span> <span data-ttu-id="c1327-148">L’agent UE-V vérifie cet emplacement une fois par jour, récupère les modèles nouveaux ou mis à jour et met à jour son comportement de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="c1327-148">The UE-V Agent checks this location once a day, retrieves new or updated templates, and updates its synchronization behavior.</span></span></p>
<p><span data-ttu-id="c1327-149">Si vous utilisez uniquement les modèles d’emplacement des paramètres par défaut UE-V, il est inutile d’utiliser un catalogue de modèles de paramètres.</span><span class="sxs-lookup"><span data-stu-id="c1327-149">If you use only the UE-V default settings location templates, then a settings template catalog is unnecessary.</span></span> <span data-ttu-id="c1327-150">Pour plus d’informations sur les paramètres des catalogues de déploiement, voir <a href="https://technet.microsoft.com/library/dn458942.aspx#deploycatalogue" data-raw-source="[Configure a UE-V settings template catalog](https://technet.microsoft.com/library/dn458942.aspx#deploycatalogue)"> configurer un catalogue de modèles de paramètres UE-V </a> .</span><span class="sxs-lookup"><span data-stu-id="c1327-150">For more information about settings deployment catalogs, see <a href="https://technet.microsoft.com/library/dn458942.aspx#deploycatalogue" data-raw-source="[Configure a UE-V settings template catalog](https://technet.microsoft.com/library/dn458942.aspx#deploycatalogue)">Configure a UE-V settings template catalog</a>.</span></span></p></td>
</tr>
</tbody>
</table>



![processus du générateur UE-v](images/ue-vgeneratorprocess.gif)

## <span data-ttu-id="c1327-152">Paramètres synchronisés par défaut</span><span class="sxs-lookup"><span data-stu-id="c1327-152">Settings Synchronized by Default</span></span>


<span data-ttu-id="c1327-153">UE-V synchronise les paramètres pour ces applications par défaut.</span><span class="sxs-lookup"><span data-stu-id="c1327-153">UE-V synchronizes settings for these applications by default.</span></span> <span data-ttu-id="c1327-154">Pour obtenir une liste complète et des informations plus détaillées, voir [paramètres qui sont synchronisés automatiquement dans un déploiement UE-V](https://technet.microsoft.com/library/dn458932.aspx#autosyncsettings).</span><span class="sxs-lookup"><span data-stu-id="c1327-154">For a complete list and more detailed information, see [Settings that are automatically synchronized in a UE-V deployment](https://technet.microsoft.com/library/dn458932.aspx#autosyncsettings).</span></span>

<span data-ttu-id="c1327-155">Applications Microsoft Office 2013 (UE-V 2,1 SP1 et 2,1)</span><span class="sxs-lookup"><span data-stu-id="c1327-155">Microsoft Office 2013 applications (UE-V 2.1 SP1 and 2.1)</span></span>

<span data-ttu-id="c1327-156">Applications Microsoft Office 2010 (UE-V 2,1 SP1, 2,1 et 2,0)</span><span class="sxs-lookup"><span data-stu-id="c1327-156">Microsoft Office 2010 applications (UE-V 2.1 SP1, 2.1, and 2.0)</span></span>

<span data-ttu-id="c1327-157">Applications Microsoft Office 2007 (UE-V 2,0 uniquement)</span><span class="sxs-lookup"><span data-stu-id="c1327-157">Microsoft Office 2007 applications (UE-V 2.0 only)</span></span>

<span data-ttu-id="c1327-158">Internet Explorer 8, 9 et 10</span><span class="sxs-lookup"><span data-stu-id="c1327-158">Internet Explorer 8, 9, and 10</span></span>

<span data-ttu-id="c1327-159">Internet Explorer 11 dans UE-V 2,1 SP1 et 2,1</span><span class="sxs-lookup"><span data-stu-id="c1327-159">Internet Explorer 11 in UE-V 2.1 SP1 and 2.1</span></span>

<span data-ttu-id="c1327-160">Plusieurs applications Windows, telles que Xbox</span><span class="sxs-lookup"><span data-stu-id="c1327-160">Many Windows applications, such as Xbox</span></span>

<span data-ttu-id="c1327-161">Plusieurs applications de bureau Windows, comme le bloc-notes</span><span class="sxs-lookup"><span data-stu-id="c1327-161">Many Windows desktop applications, such as Notepad</span></span>

<span data-ttu-id="c1327-162">De nombreux paramètres Windows, tels que l’arrière-plan ou le papier peint du Bureau;</span><span class="sxs-lookup"><span data-stu-id="c1327-162">Many Windows settings, such as desktop background or wallpaper</span></span>

**<span data-ttu-id="c1327-163">Remarque</span><span class="sxs-lookup"><span data-stu-id="c1327-163">Note</span></span>**  
<span data-ttu-id="c1327-164">Vous pouvez également [personnaliser UE-V pour synchroniser les paramètres](https://technet.microsoft.com/library/dn458942.aspx) d’applications autres que celles synchronisées par défaut.</span><span class="sxs-lookup"><span data-stu-id="c1327-164">You can also [customize UE-V to synchronize settings](https://technet.microsoft.com/library/dn458942.aspx) for applications other than those synchronized by default.</span></span>



## <span data-ttu-id="c1327-165">Comparer UE-V à d’autres produits Microsoft</span><span class="sxs-lookup"><span data-stu-id="c1327-165">Compare UE-V to other Microsoft products</span></span>


<span data-ttu-id="c1327-166">Utilisez ce tableau pour comparer UE-V afin de synchroniser les profils dans Windows 7, de synchroniser les profils dans Windows 8 et de la fonctionnalité de synchronisation des paramètres du PC de compte Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c1327-166">Use this table to compare UE-V to Synchronize Profiles in Windows 7, Synchronize Profiles in Windows 8, and the Sync PC Settings feature of Microsoft account.</span></span>

<table style="width:100%;">
<colgroup>
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c1327-167">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="c1327-167">Feature</span></span></th>
<th align="left"><span data-ttu-id="c1327-168">Synchroniser des profils à l’aide de Windows 7</span><span class="sxs-lookup"><span data-stu-id="c1327-168">Synchronize Profiles using Windows 7</span></span></th>
<th align="left"><span data-ttu-id="c1327-169">Synchroniser des profils à l’aide de Windows 8</span><span class="sxs-lookup"><span data-stu-id="c1327-169">Synchronize Profiles using Windows 8</span></span></th>
<th align="left"><span data-ttu-id="c1327-170">Synchroniser des profils à l’aide de Windows 10</span><span class="sxs-lookup"><span data-stu-id="c1327-170">Synchronize Profiles using Windows 10</span></span></th>
<th align="left"><span data-ttu-id="c1327-171">Compte Microsoft</span><span class="sxs-lookup"><span data-stu-id="c1327-171">Microsoft account</span></span></th>
<th align="left"><span data-ttu-id="c1327-172">UE-V 2,0</span><span class="sxs-lookup"><span data-stu-id="c1327-172">UE-V 2.0</span></span></th>
<th align="left"><span data-ttu-id="c1327-173">UE-V 2,1 et 2,1 SP1</span><span class="sxs-lookup"><span data-stu-id="c1327-173">UE-V 2.1 and 2.1 SP1</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c1327-174">Synchroniser les paramètres entre plusieurs ordinateurs</span><span class="sxs-lookup"><span data-stu-id="c1327-174">Synchronize settings between multiple computers</span></span></p></td>
<td align="left"><p><span data-ttu-id="c1327-175">●</span><span class="sxs-lookup"><span data-stu-id="c1327-175">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="c1327-176">●</span><span class="sxs-lookup"><span data-stu-id="c1327-176">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="c1327-177">●</span><span class="sxs-lookup"><span data-stu-id="c1327-177">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="c1327-178">●</span><span class="sxs-lookup"><span data-stu-id="c1327-178">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="c1327-179">●</span><span class="sxs-lookup"><span data-stu-id="c1327-179">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="c1327-180">●</span><span class="sxs-lookup"><span data-stu-id="c1327-180">●</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c1327-181">Synchroniser les paramètres entre les applications physiques et virtuelles</span><span class="sxs-lookup"><span data-stu-id="c1327-181">Synchronize settings between physical and virtual apps</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="c1327-182">●</span><span class="sxs-lookup"><span data-stu-id="c1327-182">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="c1327-183">●</span><span class="sxs-lookup"><span data-stu-id="c1327-183">●</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c1327-184">Synchroniser les paramètres des applications Windows</span><span class="sxs-lookup"><span data-stu-id="c1327-184">Synchronize Windows app settings</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="c1327-185">●</span><span class="sxs-lookup"><span data-stu-id="c1327-185">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="c1327-186">●</span><span class="sxs-lookup"><span data-stu-id="c1327-186">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="c1327-187">●</span><span class="sxs-lookup"><span data-stu-id="c1327-187">●</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c1327-188">Gérer via WMI</span><span class="sxs-lookup"><span data-stu-id="c1327-188">Manage via WMI</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="c1327-189">●</span><span class="sxs-lookup"><span data-stu-id="c1327-189">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="c1327-190">●</span><span class="sxs-lookup"><span data-stu-id="c1327-190">●</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="c1327-191">●</span><span class="sxs-lookup"><span data-stu-id="c1327-191">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="c1327-192">●</span><span class="sxs-lookup"><span data-stu-id="c1327-192">●</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c1327-193">Synchroniser les modifications de paramètres régulièrement</span><span class="sxs-lookup"><span data-stu-id="c1327-193">Synchronize settings changes on a regular basis</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="c1327-194">●</span><span class="sxs-lookup"><span data-stu-id="c1327-194">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="c1327-195">●</span><span class="sxs-lookup"><span data-stu-id="c1327-195">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="c1327-196">●</span><span class="sxs-lookup"><span data-stu-id="c1327-196">●</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c1327-197">Configuration minimale pour l’installation</span><span class="sxs-lookup"><span data-stu-id="c1327-197">Minimal configuration for Setup</span></span></p></td>
<td align="left"><p><span data-ttu-id="c1327-198">●</span><span class="sxs-lookup"><span data-stu-id="c1327-198">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="c1327-199">●</span><span class="sxs-lookup"><span data-stu-id="c1327-199">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="c1327-200">●</span><span class="sxs-lookup"><span data-stu-id="c1327-200">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="c1327-201">●</span><span class="sxs-lookup"><span data-stu-id="c1327-201">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="c1327-202">●</span><span class="sxs-lookup"><span data-stu-id="c1327-202">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="c1327-203">●</span><span class="sxs-lookup"><span data-stu-id="c1327-203">●</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c1327-204">Pris en charge sur les ordinateurs non membres du domaine</span><span class="sxs-lookup"><span data-stu-id="c1327-204">Supported on non-domain joined computers</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="c1327-205">●</span><span class="sxs-lookup"><span data-stu-id="c1327-205">●</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c1327-206">Prend en charge l’attribut Active Directory principal de l’ordinateur</span><span class="sxs-lookup"><span data-stu-id="c1327-206">Supports Primary Computer Active Directory attribute</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="c1327-207">●</span><span class="sxs-lookup"><span data-stu-id="c1327-207">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="c1327-208">●</span><span class="sxs-lookup"><span data-stu-id="c1327-208">●</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c1327-209">Synchronise les paramètres entre les services Bureau à distance et les services Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="c1327-209">Synchronizes settings between virtual desktop infrastructure (VDI)/Remote Desktop Services (RDS) and rich desktops</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="c1327-210">●</span><span class="sxs-lookup"><span data-stu-id="c1327-210">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="c1327-211">●</span><span class="sxs-lookup"><span data-stu-id="c1327-211">●</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c1327-212">Espace de stockage des paramètres illimités</span><span class="sxs-lookup"><span data-stu-id="c1327-212">Unlimited setting storage space</span></span></p></td>
<td align="left"><p><span data-ttu-id="c1327-213">●</span><span class="sxs-lookup"><span data-stu-id="c1327-213">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="c1327-214">●</span><span class="sxs-lookup"><span data-stu-id="c1327-214">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="c1327-215">●</span><span class="sxs-lookup"><span data-stu-id="c1327-215">●</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="c1327-216">●</span><span class="sxs-lookup"><span data-stu-id="c1327-216">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="c1327-217">●</span><span class="sxs-lookup"><span data-stu-id="c1327-217">●</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c1327-218">Choix dans les paramètres d’application à synchroniser</span><span class="sxs-lookup"><span data-stu-id="c1327-218">Choice in which app settings to synchronize</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="c1327-219">●</span><span class="sxs-lookup"><span data-stu-id="c1327-219">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="c1327-220">●</span><span class="sxs-lookup"><span data-stu-id="c1327-220">●</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c1327-221">Sauvegarde/restauration pour les professionnels de l’informatique</span><span class="sxs-lookup"><span data-stu-id="c1327-221">Backup/Restore for IT Pro</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="c1327-222">●</span><span class="sxs-lookup"><span data-stu-id="c1327-222">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="c1327-223">Partiel</span><span class="sxs-lookup"><span data-stu-id="c1327-223">Partial</span></span></p></td>
<td align="left"><p><span data-ttu-id="c1327-224">●</span><span class="sxs-lookup"><span data-stu-id="c1327-224">●</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="c1327-225">UE-V 2. x notes de publication</span><span class="sxs-lookup"><span data-stu-id="c1327-225">UE-V 2.x Release Notes</span></span>


<span data-ttu-id="c1327-226">Pour plus d’informations et pour les actualités de dernière minute qui n’ont pas été transportées en documentation, voir</span><span class="sxs-lookup"><span data-stu-id="c1327-226">For more information, and for late-breaking news that did not make it into the documentation, see</span></span>

-   [<span data-ttu-id="c1327-227">Notes de publication pour Microsoft User Experience Virtualization (UE-V)2.1SP1</span><span class="sxs-lookup"><span data-stu-id="c1327-227">Microsoft User Experience Virtualization (UE-V) 2.1 SP1 Release Notes</span></span>](microsoft-user-experience-virtualization--ue-v--21-sp1-release-notes.md)

-   [<span data-ttu-id="c1327-228">Notes de publication pour Microsoft User Experience Virtualization (UE-V)2.1</span><span class="sxs-lookup"><span data-stu-id="c1327-228">Microsoft User Experience Virtualization (UE-V) 2.1 Release Notes</span></span>](microsoft-user-experience-virtualization--ue-v--21-release-notesuevv21.md)

-   [<span data-ttu-id="c1327-229">Notes de publication pour Microsoft User Experience Virtualization (UE-V)2.0</span><span class="sxs-lookup"><span data-stu-id="c1327-229">Microsoft User Experience Virtualization (UE-V) 2.0 Release Notes</span></span>](microsoft-user-experience-virtualization--ue-v--20-release-notesuevv2.md)

## <span data-ttu-id="c1327-230">Autres ressources pour ce produit</span><span class="sxs-lookup"><span data-stu-id="c1327-230">Other resources for this product</span></span>


-   [<span data-ttu-id="c1327-231">Prise en main d'UE-V2.x</span><span class="sxs-lookup"><span data-stu-id="c1327-231">Get Started with UE-V 2.x</span></span>](get-started-with-ue-v-2x-new-uevv2.md)

-   [<span data-ttu-id="c1327-232">Préparer un déploiement UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="c1327-232">Prepare a UE-V 2.x Deployment</span></span>](prepare-a-ue-v-2x-deployment-new-uevv2.md)

-   [<span data-ttu-id="c1327-233">Administration d’UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="c1327-233">Administering UE-V 2.x</span></span>](administering-ue-v-2x-new-uevv2.md)

-   [<span data-ttu-id="c1327-234">Résolution des problèmes de UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="c1327-234">Troubleshooting UE-V 2.x</span></span>](troubleshooting-ue-v-2x-both-uevv2.md)

-   [<span data-ttu-id="c1327-235">Informations techniques de référence sur UE-V2.x</span><span class="sxs-lookup"><span data-stu-id="c1327-235">Technical Reference for UE-V 2.x</span></span>](technical-reference-for-ue-v-2x-both-uevv2.md)

### <span data-ttu-id="c1327-236">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="c1327-236">More information</span></span>

<a href="" id="mdop-techcenter-page"></a><span data-ttu-id="c1327-237">[Page TechCenter de MDOP](https://go.microsoft.com/fwlink/p/?LinkId=225286) En savoir plus sur les dernières informations et ressources de MDOP.</span><span class="sxs-lookup"><span data-stu-id="c1327-237">[MDOP TechCenter Page](https://go.microsoft.com/fwlink/p/?LinkId=225286) Learn about the latest MDOP information and resources.</span></span>

<a href="" id="mdop-information-experience"></a><span data-ttu-id="c1327-238">[Découverte des informations de MDOP](https://go.microsoft.com/fwlink/p/?LinkId=236032) Recherchez des documents, des vidéos et d’autres ressources pour MDOP technologies.</span><span class="sxs-lookup"><span data-stu-id="c1327-238">[MDOP Information Experience](https://go.microsoft.com/fwlink/p/?LinkId=236032) Find documentation, videos, and other resources for MDOP technologies.</span></span> <span data-ttu-id="c1327-239">Vous pouvez également [nous envoyer vos commentaires](mailto:MDOPDocs@microsoft.com) ou en savoir plus sur les mises à jour, en nous suivant sur [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) ou [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447).</span><span class="sxs-lookup"><span data-stu-id="c1327-239">You can also [send us feedback](mailto:MDOPDocs@microsoft.com) or learn about updates by following us on [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) or [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447).</span></span>














