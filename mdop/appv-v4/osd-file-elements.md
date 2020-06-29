---
title: Éléments du fichier OSD
description: Éléments du fichier OSD
author: dansimp
ms.assetid: 8211b562-7549-4331-8321-144f52574e99
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a8e3ebcf53ff39ecd2ef7ad0feec0bbbcae199db
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806574"
---
# <span data-ttu-id="3aedc-103">Éléments du fichier OSD</span><span class="sxs-lookup"><span data-stu-id="3aedc-103">OSD File Elements</span></span>


<span data-ttu-id="3aedc-104">Le répertoire d’installation de Sequencer contient un fichier de schéma XML, **Softricity. xsd**, qui définit la structure valide d’un fichier d’OSD (Open Software Descriptor).</span><span class="sxs-lookup"><span data-stu-id="3aedc-104">The Sequencer installation directory contains an XML schema file, **Softricity.xsd**, which defines the valid structure of an Open Software Descriptor (OSD) file.</span></span> <span data-ttu-id="3aedc-105">Voici quelques-uns des éléments d’OSD les plus fréquemment utilisés.</span><span class="sxs-lookup"><span data-stu-id="3aedc-105">Following are some of the more frequently used OSD elements.</span></span>

<a href="" id="softpkg"></a><span data-ttu-id="3aedc-106">SOFTPKG</span><span class="sxs-lookup"><span data-stu-id="3aedc-106">SOFTPKG</span></span>  
<span data-ttu-id="3aedc-107">Élément racine du fichier OSD contenant tous les éléments définissant le package logiciel.</span><span class="sxs-lookup"><span data-stu-id="3aedc-107">The root element of the OSD file containing all elements defining the software package.</span></span>

<a href="" id="codebase"></a><span data-ttu-id="3aedc-108">CODE base</span><span class="sxs-lookup"><span data-stu-id="3aedc-108">CODEBASE</span></span>  
<span data-ttu-id="3aedc-109">Des informations sur le fichier. SFT pour ce package, notamment les attributs HREF, FILENAME et GUID.</span><span class="sxs-lookup"><span data-stu-id="3aedc-109">Information about the .sft file for this package, including the HREF, FILENAME, and GUID attributes.</span></span> <span data-ttu-id="3aedc-110">Vous pouvez modifier l’attribut HREF si vous modifiez le point de distribution de ce package particulier.</span><span class="sxs-lookup"><span data-stu-id="3aedc-110">You can edit the HREF attribute if you change the distribution point of this particular package.</span></span>

<a href="" id="os"></a><span data-ttu-id="3aedc-111">Système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="3aedc-111">OS</span></span>  
<span data-ttu-id="3aedc-112">Définit sur quels systèmes d’exploitation cette application peut s’exécuter en fonction de valeurs initialement définies dans l’Assistant séquençage.</span><span class="sxs-lookup"><span data-stu-id="3aedc-112">Defines on what operating systems this application can run based on values that are initially set in the Sequencing Wizard.</span></span> <span data-ttu-id="3aedc-113">Cette valeur ne peut contenir que les valeurs définies dans **Softricity. xsd**.</span><span class="sxs-lookup"><span data-stu-id="3aedc-113">This value can contain only the values defined in **Softricity.xsd**.</span></span>

<a href="" id="local-interaction-allowed"></a><span data-ttu-id="3aedc-114">_INTERACTION \ LOCAL \ _ALLOWED</span><span class="sxs-lookup"><span data-stu-id="3aedc-114">LOCAL\_INTERACTION\_ALLOWED</span></span>  
<span data-ttu-id="3aedc-115">Valeur définie sur TRUE, cette option permet de créer des objets nommés (événements, mutexes, sémaphores, mappages de fichiers et mailslots) et d’objets COM dans l’espace de noms global plutôt que d’être isolés au sein d’un environnement virtuel particulier, ce qui permet aux applications virtuelles d’interagir avec les applications du système d’exploitation hôte.</span><span class="sxs-lookup"><span data-stu-id="3aedc-115">Set to TRUE, this enables creation of named objects (events, mutexes, semaphores, file mappings, and mailslots) and COM objects in the global namespace rather than isolated inside a particular virtual environment, which allows virtual applications to interact with the host operating system's applications.</span></span>

<span data-ttu-id="3aedc-116">Exemple: &lt; implémentation de SOFTPKG &gt; &lt;&gt;</span><span class="sxs-lookup"><span data-stu-id="3aedc-116">Example:&lt;SOFTPKG&gt;&lt;IMPLEMENTATION&gt;</span></span>

<span data-ttu-id="3aedc-117">&lt;&gt; &lt; stratégies VIRTUALENV&gt;</span><span class="sxs-lookup"><span data-stu-id="3aedc-117">&lt;VIRTUALENV&gt;&lt;POLICIES&gt;</span></span>

<span data-ttu-id="3aedc-118">&lt;LOCAL \ _INTERACTION \ _ALLOWED &gt; vrai</span><span class="sxs-lookup"><span data-stu-id="3aedc-118">&lt;LOCAL\_INTERACTION\_ALLOWED&gt;TRUE</span></span>

<span data-ttu-id="3aedc-119">&lt;/LOCAL\ _INTERACTION \ _ALLOWED&gt;</span><span class="sxs-lookup"><span data-stu-id="3aedc-119">&lt;/LOCAL\_INTERACTION\_ALLOWED&gt;</span></span>

<span data-ttu-id="3aedc-120">&lt;/POLICIES &gt; &lt; /VIRTUALENV&gt;</span><span class="sxs-lookup"><span data-stu-id="3aedc-120">&lt;/POLICIES&gt;&lt;/VIRTUALENV&gt;</span></span>

<span data-ttu-id="3aedc-121">&lt;/IMPLEMENTATION &gt; &lt; /SOFTPKG&gt;</span><span class="sxs-lookup"><span data-stu-id="3aedc-121">&lt;/IMPLEMENTATION&gt;&lt;/SOFTPKG&gt;</span></span>

<a href="" id="dependencies"></a><span data-ttu-id="3aedc-122">Liens</span><span class="sxs-lookup"><span data-stu-id="3aedc-122">DEPENDENCIES</span></span>  
<span data-ttu-id="3aedc-123">Définit la composition de la suite dynamique (dépendances par rapport à d’autres packages) en utilisant une balise de code base à partir d’un autre package.</span><span class="sxs-lookup"><span data-stu-id="3aedc-123">Defines Dynamic Suite Composition (dependencies on other packages) by using a CODEBASE tag from another package.</span></span>

<span data-ttu-id="3aedc-124">Exemple: &lt; &gt; &lt; codebase Dependencies href = "RTSP://Server/Package.sft" GUID = "7579F4DF-2461-4219-BD43-494E1FDC69E3" SYSGUARDFILE = "pkg. 1 \ \ osguard. CP" size = "6572748" obligatoire = "false"/ &gt; &lt; /Dependencies&gt;</span><span class="sxs-lookup"><span data-stu-id="3aedc-124">Example:&lt;DEPENDENCIES&gt;&lt;CODEBASE HREF="rtsps://server/package.sft" GUID="7579F4DF-2461-4219-BD43-494E1FDC69E3" SYSGUARDFILE="pkg.1\\osguard.cp" SIZE="6572748" MANDATORY="FALSE"/&gt;&lt;/DEPENDENCIES&gt;</span></span>

<a href="" id="package-name"></a><span data-ttu-id="3aedc-125">NOM DU PACKAGE</span><span class="sxs-lookup"><span data-stu-id="3aedc-125">PACKAGE NAME</span></span>  
<span data-ttu-id="3aedc-126">Nom courant du package entré dans la page d' **informations sur le package** de l’Assistant séquençage, qui vous permet de spécifier un nom unique pour une application séquencée contenant plusieurs applications.</span><span class="sxs-lookup"><span data-stu-id="3aedc-126">A common name for the package entered into the Sequencing Wizard **Package Information** page, which enables you to specify a single name used for a sequenced application containing multiple applications.</span></span>

<a href="" id="title"></a><span data-ttu-id="3aedc-127">DROITS</span><span class="sxs-lookup"><span data-stu-id="3aedc-127">TITLE</span></span>  
<span data-ttu-id="3aedc-128">Nom descriptif facultatif de l’application que vous séquençage.</span><span class="sxs-lookup"><span data-stu-id="3aedc-128">Optional descriptive name of the application you are sequencing.</span></span>

<a href="" id="abstract"></a><span data-ttu-id="3aedc-129">EXTRACTION</span><span class="sxs-lookup"><span data-stu-id="3aedc-129">ABSTRACT</span></span>  
<span data-ttu-id="3aedc-130">Brève description du programme logiciel entré dans le champ **Commentaires** de **la page de** l’Assistant séquençage.</span><span class="sxs-lookup"><span data-stu-id="3aedc-130">Short description of the software package entered in the **Comments** field in the Sequencing Wizard **Package Information** page.</span></span> <span data-ttu-id="3aedc-131">Il est recommandé de spécifier des informations telles que le système d’exploitation et le niveau de service du poste de travail, la version Sequencer et le nom de l’ingénieur de séquençage.</span><span class="sxs-lookup"><span data-stu-id="3aedc-131">A best practice is to specify information such as the operating system and service-pack level of the Sequencer workstation, Sequencer version, and the sequencing engineer’s name.</span></span>

<a href="" id="script"></a><span data-ttu-id="3aedc-132">SCRIPT</span><span class="sxs-lookup"><span data-stu-id="3aedc-132">SCRIPT</span></span>  
<span data-ttu-id="3aedc-133">Définit des événements de script spécifiques qui se produisent au démarrage, à l’arrêt ou en flux continu.</span><span class="sxs-lookup"><span data-stu-id="3aedc-133">Defines specific scripted events to occur during startup, shutdown, or streaming.</span></span>

<a href="" id="mgmt-shortcutlist"></a><span data-ttu-id="3aedc-134">GESTION DES _SHORTCUTLIST</span><span class="sxs-lookup"><span data-stu-id="3aedc-134">MGMT\_SHORTCUTLIST</span></span>  
<span data-ttu-id="3aedc-135">Liste de tous les raccourcis définis dans l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="3aedc-135">List of all shortcuts defined in the wizard.</span></span>

<a href="" id="mgmt-fileassociations"></a><span data-ttu-id="3aedc-136">GESTION DES _FILEASSOCIATIONS</span><span class="sxs-lookup"><span data-stu-id="3aedc-136">MGMT\_FILEASSOCIATIONS</span></span>  
<span data-ttu-id="3aedc-137">Liste des types de fichiers spécifiés dans l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="3aedc-137">List of the file types specified in the wizard.</span></span>

## <span data-ttu-id="3aedc-138">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3aedc-138">Related topics</span></span>


[<span data-ttu-id="3aedc-139">À propos de l'onglet OSD</span><span class="sxs-lookup"><span data-stu-id="3aedc-139">About the OSD Tab</span></span>](about-the-osd-tab.md)

 

 





