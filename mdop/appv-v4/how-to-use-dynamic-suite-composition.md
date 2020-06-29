---
title: Procédure d'utilisation de la composition de suite dynamique
description: Procédure d'utilisation de la composition de suite dynamique
author: dansimp
ms.assetid: 24147feb-a0a8-4791-a8e5-cbe5fe13c762
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3bff4c9721352785cf6db5c497234ceaa3c5e448
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806698"
---
# <span data-ttu-id="5bccd-103">Procédure d'utilisation de la composition de suite dynamique</span><span class="sxs-lookup"><span data-stu-id="5bccd-103">How To Use Dynamic Suite Composition</span></span>


<span data-ttu-id="5bccd-104">La composition de suite dynamique dans la virtualisation d’application vous permet de définir une application comme étant dépendante d’une autre application, telle qu’un middleware ou un plug-in.</span><span class="sxs-lookup"><span data-stu-id="5bccd-104">Dynamic Suite Composition in Application Virtualization enables you to define an application as being dependent on another application, such as middleware or a plug-in.</span></span> <span data-ttu-id="5bccd-105">Cela permet à l’application d’interagir avec le middleware ou le plug-in dans l’environnement virtuel, en règle générale, ce problème est empêché.</span><span class="sxs-lookup"><span data-stu-id="5bccd-105">This enables the application to interact with the middleware or plug-in in the virtual environment, where typically this is prevented.</span></span> <span data-ttu-id="5bccd-106">Cela est utile, car un package d’application secondaire peut être utilisé avec plusieurs autres applications, appelées *applications principales*, qui permettent à chaque application principale de référencer le même package secondaire.</span><span class="sxs-lookup"><span data-stu-id="5bccd-106">This is useful because a secondary application package can be used with several other applications, referred to as the *primary applications*, which enables each primary application to reference the same secondary package.</span></span>

<span data-ttu-id="5bccd-107">Vous pouvez utiliser la composition suite dynamique quand vous séquencez des applications qui dépendent de plug-ins tels que des contrôles ActiveX ou des applications qui dépendent de middleware tels qu’OLE DB ou Java Runtime Environment (JRE).</span><span class="sxs-lookup"><span data-stu-id="5bccd-107">You can use Dynamic Suite Composition when you sequence applications that depend on plug-ins such as ActiveX controls or for applications that depend on middleware such as OLE DB or the Java Runtime Environment (JRE).</span></span> <span data-ttu-id="5bccd-108">Si chaque application ayant utilisé ces composants dépendants a requis le séquençage, y compris les composants, les mises à jour apportées à ces composants nécessiteront de nouveau le séquençage de toutes les applications principales.</span><span class="sxs-lookup"><span data-stu-id="5bccd-108">If each application that used these dependent components required sequencing, including the components, updates to those components would require re-sequencing all the primary applications.</span></span> <span data-ttu-id="5bccd-109">Si vous avez séquencé les principales applications sans les composants, puis séquencé le middleware ou le plug-in en tant que package secondaire, seul le package secondaire doit être mis à jour.</span><span class="sxs-lookup"><span data-stu-id="5bccd-109">If you sequence the primary applications without the components and then sequence the middleware or plug-in as a secondary package, then only the secondary package must be updated.</span></span>

<span data-ttu-id="5bccd-110">L’un des avantages de cette approche réside dans le fait qu’elle permet de réduire la taille des packages principaux.</span><span class="sxs-lookup"><span data-stu-id="5bccd-110">One advantage of this approach is that it reduces the size of the primary packages.</span></span> <span data-ttu-id="5bccd-111">Un autre avantage réside dans le fait qu’il vous permet de mieux contrôler les autorisations d’accès aux applications secondaires.</span><span class="sxs-lookup"><span data-stu-id="5bccd-111">Another advantage is that it provides you with better control of access permissions on the secondary applications.</span></span> <span data-ttu-id="5bccd-112">Notez que l’application secondaire peut être diffusée de façon régulière et qu’elle n’a pas besoin d’être complètement mise en cache pour s’exécuter.</span><span class="sxs-lookup"><span data-stu-id="5bccd-112">Note that the secondary application can be streamed in the regular way and does not have to be fully cached to run.</span></span>

<span data-ttu-id="5bccd-113">Un package principal peut avoir plusieurs packages secondaires.</span><span class="sxs-lookup"><span data-stu-id="5bccd-113">A primary package can have more than one secondary package.</span></span> <span data-ttu-id="5bccd-114">Toutefois, un seul niveau de dépendance est pris en charge, de sorte que vous ne pouvez pas définir un package secondaire comme dépendant d’un autre package secondaire.</span><span class="sxs-lookup"><span data-stu-id="5bccd-114">However, only one level of dependency is supported, so you cannot define a secondary package as dependent on another secondary package.</span></span> <span data-ttu-id="5bccd-115">Par ailleurs, l’application secondaire peut uniquement être middleware ou un plug-in et ne peut pas être un autre produit logiciel complet.</span><span class="sxs-lookup"><span data-stu-id="5bccd-115">Also the secondary application can only be middleware or a plug-in and cannot be another full software product.</span></span>

<span data-ttu-id="5bccd-116">Si vous envisagez de rendre différentes applications principales dépendantes d’un seul produit middleware, assurez-vous que vous testez cette configuration pour déterminer l’impact potentiel sur les performances système avant de procéder au déploiement.</span><span class="sxs-lookup"><span data-stu-id="5bccd-116">If you plan to make several primary applications dependent on a single middleware product, make sure that you test this configuration to determine the potential effect on system performance before you deploy it.</span></span>

<span data-ttu-id="5bccd-117">**Important**  Les dépendances de package peuvent être spécifiées comme obligatoires pour une application principale.</span><span class="sxs-lookup"><span data-stu-id="5bccd-117">**Important** Package dependencies can be specified as mandatory for a primary application.</span></span> <span data-ttu-id="5bccd-118">Si un package secondaire est marqué comme obligatoire et ne peut pas être utilisé pour une raison quelconque lors du chargement, le chargement du package secondaire échoue.</span><span class="sxs-lookup"><span data-stu-id="5bccd-118">If a secondary package is flagged as mandatory and it cannot be accessed for some reason during loading, the load of the secondary package will fail.</span></span> <span data-ttu-id="5bccd-119">Par ailleurs, l’application principale ne fonctionnera pas si l’utilisateur essaie de la démarrer.</span><span class="sxs-lookup"><span data-stu-id="5bccd-119">Also, the primary application will fail when the user tries to start it.</span></span>

 

<span data-ttu-id="5bccd-120">Vous pouvez utiliser les procédures suivantes pour créer un package secondaire, pour un plug-in ou un composant middleware, puis vous pouvez utiliser la procédure finale pour définir la dépendance dans le fichier OSD du package secondaire.</span><span class="sxs-lookup"><span data-stu-id="5bccd-120">You can use the following procedures to create a secondary package, for either a plug-in or a middleware component, and then you can use the final procedure to define the dependency in the OSD file of the secondary package.</span></span>

**<span data-ttu-id="5bccd-121">Pour créer un package secondaire pour un plug-in à l’aide de la composition suite dynamique</span><span class="sxs-lookup"><span data-stu-id="5bccd-121">To create a secondary package for a plug-in by using Dynamic Suite Composition</span></span>**

1.  <span data-ttu-id="5bccd-122">Sur un ordinateur de séquençage configuré avec une image saine, installez le Sequencer Application Virtualization et enregistrez l’état de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="5bccd-122">On a sequencing computer that is set up with a clean image, install Application Virtualization Sequencer and save the computer state.</span></span>

2.  <span data-ttu-id="5bccd-123">Séquencez l’application principale, puis enregistrez le package dans le dossier Content sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="5bccd-123">Sequence the primary application, and save the package to the Content folder on the server.</span></span>

3.  <span data-ttu-id="5bccd-124">Restaurez l’ordinateur de séquençage à son état d’enregistrement à partir de l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="5bccd-124">Restore the sequencing computer to its saved state from step 1.</span></span>

4.  <span data-ttu-id="5bccd-125">Installez et configurez l’application principale localement sur l’ordinateur de séquençage.</span><span class="sxs-lookup"><span data-stu-id="5bccd-125">Install and configure the primary application locally on the sequencing computer.</span></span>

    <span data-ttu-id="5bccd-126">**Important**  Vous devez spécifier une nouvelle racine de package pour le package secondaire.</span><span class="sxs-lookup"><span data-stu-id="5bccd-126">**Important** You must specify a new package root for the secondary package.</span></span>

     

5.  <span data-ttu-id="5bccd-127">Démarrez la phase de contrôle de Sequencer.</span><span class="sxs-lookup"><span data-stu-id="5bccd-127">Start the sequencer monitoring phase.</span></span>

6.  <span data-ttu-id="5bccd-128">Installez le plug-in sur l’ordinateur de séquençage et configurez-le selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="5bccd-128">Install the plug-in on the sequencing computer and configure it as needed.</span></span>

7.  <span data-ttu-id="5bccd-129">Ouvrez l’application principale, puis vérifiez que le plug-in fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="5bccd-129">Open the primary application, and confirm that the plug-in is working correctly.</span></span>

8.  <span data-ttu-id="5bccd-130">Dans la console de Sequencer, créez une application factice pour représenter le package secondaire qui contient le plug-in et sélectionnez une icône.</span><span class="sxs-lookup"><span data-stu-id="5bccd-130">In the sequencer console, create a dummy application to represent the secondary package that will contain the plug-in and select an icon.</span></span>

9.  <span data-ttu-id="5bccd-131">Enregistrez le package dans le dossier Content du serveur.</span><span class="sxs-lookup"><span data-stu-id="5bccd-131">Save the package to the Content folder on the server.</span></span>

    <span data-ttu-id="5bccd-132">**Remarques**  Pour vous aider à gérer les packages secondaires, il est recommandé que le nom du package inclue le terme «package secondaire» pour insister sur qu’il s’agit d’un package qui ne fonctionne pas comme une application autonome (par exemple, **\ [nom de connexion \] package secondaire**).</span><span class="sxs-lookup"><span data-stu-id="5bccd-132">**Note** To assist with management of secondary packages, it is recommended that the package name include the term “Secondary package” to emphasize that this is a package that will not function as a stand-alone application—for example, **\[Plug In Name\] Secondary package**.</span></span>

     

**<span data-ttu-id="5bccd-133">Pour créer un package secondaire pour le middleware à l’aide de la composition suite dynamique</span><span class="sxs-lookup"><span data-stu-id="5bccd-133">To create a secondary package for middleware by using Dynamic Suite Composition</span></span>**

1.  <span data-ttu-id="5bccd-134">Sur un ordinateur de séquençage configuré avec une image saine, installez le Sequencer Application Virtualization et enregistrez l’état de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="5bccd-134">On a sequencing computer that is set up with a clean image, install Application Virtualization Sequencer and save the computer state.</span></span>

2.  <span data-ttu-id="5bccd-135">Installez le middleware localement sur l’ordinateur de séquençage et configurez-le.</span><span class="sxs-lookup"><span data-stu-id="5bccd-135">Install the middleware locally on the sequencing computer, and configure it.</span></span>

3.  <span data-ttu-id="5bccd-136">Séquencez l’application principale, puis enregistrez le package dans le dossier Content sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="5bccd-136">Sequence the primary application, and save the package to the Content folder on the server.</span></span>

4.  <span data-ttu-id="5bccd-137">Restaurez l’ordinateur de séquençage à son état d’enregistrement à partir de l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="5bccd-137">Restore the sequencing computer to its saved state from step 1.</span></span>

5.  <span data-ttu-id="5bccd-138">Démarrez le Sequencer pour créer un package.</span><span class="sxs-lookup"><span data-stu-id="5bccd-138">Start the sequencer to create a new package.</span></span>

6.  <span data-ttu-id="5bccd-139">Démarrez la phase de contrôle de Sequencer.</span><span class="sxs-lookup"><span data-stu-id="5bccd-139">Start the sequencer monitoring phase.</span></span>

7.  <span data-ttu-id="5bccd-140">Installez l’application middleware sur l’ordinateur de séquençage et configurez-la comme dans une installation classique.</span><span class="sxs-lookup"><span data-stu-id="5bccd-140">Install the middleware application on the sequencing computer, and configure it as in a typical installation.</span></span>

8.  <span data-ttu-id="5bccd-141">Terminez le processus de séquençage.</span><span class="sxs-lookup"><span data-stu-id="5bccd-141">Complete the sequencing process.</span></span>

9.  <span data-ttu-id="5bccd-142">Enregistrez le package dans le dossier Content du serveur.</span><span class="sxs-lookup"><span data-stu-id="5bccd-142">Save the package to the Content folder on the server.</span></span>

    <span data-ttu-id="5bccd-143">**Remarques**  Pour vous aider à gérer les packages secondaires, il est recommandé que le nom du package inclue le terme «package secondaire» pour insister sur qu’il s’agit d’un package qui ne fonctionnera pas comme une application autonome (par exemple, **\ [nom du middleware \] package secondaire**).</span><span class="sxs-lookup"><span data-stu-id="5bccd-143">**Note** To assist with management of secondary packages, it is recommended that the package name include the term “Secondary package” to emphasize that this is a package that will not function as a stand-alone application—for example, **\[Middleware Name\] Secondary package**.</span></span>

     

**<span data-ttu-id="5bccd-144">Pour définir la dépendance dans le package principal</span><span class="sxs-lookup"><span data-stu-id="5bccd-144">To define the dependency in the primary package</span></span>**

1. <span data-ttu-id="5bccd-145">Sur le serveur, ouvrez le fichier OSD du package secondaire à des fins de modification.</span><span class="sxs-lookup"><span data-stu-id="5bccd-145">On the server, open the OSD file of the secondary package for editing.</span></span> <span data-ttu-id="5bccd-146">(Il est recommandé d’utiliser un éditeur XML pour apporter des modifications au fichier OSD; Toutefois, vous pouvez utiliser le bloc-notes comme alternative.)</span><span class="sxs-lookup"><span data-stu-id="5bccd-146">(It is a good idea to use an XML editor to make changes to the OSD file; however, you can use Notepad as an alternative.)</span></span>

2. <span data-ttu-id="5bccd-147">Copiez la ligne **href de base** de ce fichier.</span><span class="sxs-lookup"><span data-stu-id="5bccd-147">Copy the **CODEBASE HREF** line from that file.</span></span>

3. <span data-ttu-id="5bccd-148">Ouvrez le fichier OSD du package principal à des fins de modification.</span><span class="sxs-lookup"><span data-stu-id="5bccd-148">Open the OSD file of the primary package for editing.</span></span>

4. <span data-ttu-id="5bccd-149">Insérez la <strong> &lt; &gt; </strong> balise Dependencies après la fermeture de la balise \*\* &lt; /ENVLIST &gt; \*\* à la fin de la section \*\* &lt; VIRTUALENV &gt; \*\* juste avant la balise \*\* &lt; /VIRTUALENV &gt; \*\* .</span><span class="sxs-lookup"><span data-stu-id="5bccd-149">Insert the <strong>&lt;DEPENDENCIES&gt;</strong>tag after the close of **&lt;/ENVLIST&gt;** tag at the end of the **&lt;VIRTUALENV&gt;** section just before the **&lt;/VIRTUALENV&gt;** tag.</span></span>

5. <span data-ttu-id="5bccd-150">Collez la ligne **href du code base** à partir du package secondaire après la balise de \*\* &lt; &gt; dépendances\*\* que vous venez de créer.</span><span class="sxs-lookup"><span data-stu-id="5bccd-150">Paste the **CODEBASE HREF** line from the secondary package after the **&lt;DEPENDENCIES&gt;** tag you just created.</span></span>

6. <span data-ttu-id="5bccd-151">S’il s’agit d’un package obligatoire, ce qui signifie qu’il doit être démarré avant le démarrage du package principal, ajoutez la propriété **obligatoire = «true»** dans la balise de **code base** .</span><span class="sxs-lookup"><span data-stu-id="5bccd-151">If the secondary package is a mandatory package, which means that it must be started before the primary package is started, add the **MANDATORY=”TRUE”** property inside the **CODEBASE** tag.</span></span> <span data-ttu-id="5bccd-152">Si ce n’est pas obligatoire, la propriété peut être omise.</span><span class="sxs-lookup"><span data-stu-id="5bccd-152">If it is not mandatory, the property can be omitted.</span></span>

7. <span data-ttu-id="5bccd-153">Fermez la balise \*\* &lt; Dependencies &gt; \*\* en insérant ce qui suit:</span><span class="sxs-lookup"><span data-stu-id="5bccd-153">Close the **&lt;DEPENDENCIES&gt;** tag by inserting the following:</span></span>

   **<span data-ttu-id="5bccd-154">&lt;/DEPENDENCIES&gt;</span><span class="sxs-lookup"><span data-stu-id="5bccd-154">&lt;/DEPENDENCIES&gt;</span></span>**

8. <span data-ttu-id="5bccd-155">Passez en revue les modifications que vous avez apportées au fichier OSD, puis enregistrez et fermez le fichier.</span><span class="sxs-lookup"><span data-stu-id="5bccd-155">Review the changes that you made to the OSD file, and then save and close the file.</span></span> <span data-ttu-id="5bccd-156">L’exemple suivant montre comment la section ajoutée doit apparaître.</span><span class="sxs-lookup"><span data-stu-id="5bccd-156">The following example shows how the added section should appear.</span></span> <span data-ttu-id="5bccd-157">Par exemple, les valeurs des balises affichées sont uniquement disponibles.</span><span class="sxs-lookup"><span data-stu-id="5bccd-157">The tag values shown here are for example only.</span></span>

   **<span data-ttu-id="5bccd-158">&lt;VIRTUALENV&gt;</span><span class="sxs-lookup"><span data-stu-id="5bccd-158">&lt;VIRTUALENV&gt;</span></span>**

        **&lt;ENVLIST&gt;**

   **<span data-ttu-id="5bccd-159">…</span><span class="sxs-lookup"><span data-stu-id="5bccd-159">…</span></span>**

        **&lt;/ENVLIST&gt;**

        **&lt;DEPENDENCIES&gt;**

             **&lt;CODEBASE HREF="rtsp://virt\_apps/package.1/package.1.sft" GUID="D54C80FA-9DFF-459D-AA33-DD852C9FBFBA" SYSGUARDFILE="package.1\\osguard.cp"/&gt;**

             **&lt;CODEBASE HREF="rtsp://sample\_apps/package.2/sample.sft" GUID="D54C80FA-9DFF-459D-AA33-DD852C9FBFBA" SYSGUARDFILE="package.2\\osguard.cp" MANDATORY="TRUE" /&gt;**

        **&lt;/DEPENDENCIES&gt;**

   **<span data-ttu-id="5bccd-160">&lt;/VIRTUALENV&gt;</span><span class="sxs-lookup"><span data-stu-id="5bccd-160">&lt;/VIRTUALENV&gt;</span></span>**

9. <span data-ttu-id="5bccd-161">Si le package secondaire comporte des entrées dans la section \*\* &lt; ENVLIST &gt; \*\* du fichier OSD, vous devez copier ces entrées dans la même section du package principal.</span><span class="sxs-lookup"><span data-stu-id="5bccd-161">If the secondary package has any entries in the **&lt;ENVLIST&gt;** section of the OSD file, you must copy those entries to the same section in the primary package.</span></span>

## <span data-ttu-id="5bccd-162">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5bccd-162">Related topics</span></span>


[<span data-ttu-id="5bccd-163">Comment créer ou mettre à niveau des applications virtuelles à l’aide du Sequencer App-V</span><span class="sxs-lookup"><span data-stu-id="5bccd-163">How to Create or Upgrade Virtual Applications Using the App-V Sequencer</span></span>](how-to-create-or-upgrade-virtual-applications-using--the-app-v-sequencer.md)

 

 





