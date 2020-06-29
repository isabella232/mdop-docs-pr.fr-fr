---
title: Comment configurer un package de déploiement
description: Comment configurer un package de déploiement
author: dansimp
ms.assetid: 748272a1-6af2-476e-a3f1-87435b8e94b1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: aba5e91a4da92f9e51a5ccc70502658ae724d76f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811460"
---
# <span data-ttu-id="8769b-103">Comment configurer un package de déploiement</span><span class="sxs-lookup"><span data-stu-id="8769b-103">How to Configure a Deployment Package</span></span>


<span data-ttu-id="8769b-104">L’Assistant Création de packages vous guide dans le processus de création d’un package en créant un dossier sur votre ordinateur local et en transférant tous les fichiers d’installation requis vers le dossier unique.</span><span class="sxs-lookup"><span data-stu-id="8769b-104">The Packaging wizard walks you through the creation of a package by creating a folder on your local computer and transferring all the required installation files to the single folder.</span></span> <span data-ttu-id="8769b-105">Le contenu du dossier peut ensuite être déplacé vers plusieurs lecteurs de médias amovibles pour distribution.</span><span class="sxs-lookup"><span data-stu-id="8769b-105">The contents of the folder can then be moved to multiple removable media drives for distribution.</span></span>

**<span data-ttu-id="8769b-106">Remarque</span><span class="sxs-lookup"><span data-stu-id="8769b-106">Note</span></span>**  
<span data-ttu-id="8769b-107">Un package unique ne peut pas contenir des fichiers d’installation pour les systèmes x86 et x64.</span><span class="sxs-lookup"><span data-stu-id="8769b-107">A single package cannot contain installation files for both x86 and x64 systems.</span></span>



## <span data-ttu-id="8769b-108">Créer un package de déploiement</span><span class="sxs-lookup"><span data-stu-id="8769b-108">How to Create a Deployment Package</span></span>


**<span data-ttu-id="8769b-109">Pour créer un package de déploiement</span><span class="sxs-lookup"><span data-stu-id="8769b-109">To create a deployment package</span></span>**

1. <span data-ttu-id="8769b-110">Dans le module **images** , vérifiez que vous avez créé au moins une image compactée locale.</span><span class="sxs-lookup"><span data-stu-id="8769b-110">Verify in the **Images** module that you have created at least one local packed image.</span></span>

2. <span data-ttu-id="8769b-111">Dans le menu **Outils** , sélectionnez **Assistant Empaquetage**.</span><span class="sxs-lookup"><span data-stu-id="8769b-111">On the **Tools** menu, select **Packaging wizard**.</span></span>

3. <span data-ttu-id="8769b-112">Sur la page d’accueil de l' **Assistant Packaging** , cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="8769b-112">On the **Packaging wizard** welcome page, click **Next**.</span></span>

4. <span data-ttu-id="8769b-113">Dans la page image de l' **espace de travail** , activez la case à cocher **inclure l’image dans le package** pour inclure une image dans le package.</span><span class="sxs-lookup"><span data-stu-id="8769b-113">On the **Workspace Image** page, select the **Include image in the package** check box to include an image in the package.</span></span>

   <span data-ttu-id="8769b-114">Le champ d' **image** est activé.</span><span class="sxs-lookup"><span data-stu-id="8769b-114">The **Image** field is enabled.</span></span>

   **<span data-ttu-id="8769b-115">Remarque</span><span class="sxs-lookup"><span data-stu-id="8769b-115">Note</span></span>**  
   <span data-ttu-id="8769b-116">Une image n’est pas requise dans un paquet MED-V; le package peut être créé sans image.</span><span class="sxs-lookup"><span data-stu-id="8769b-116">An image is not required in a MED-V package; the package can be created without an image.</span></span> <span data-ttu-id="8769b-117">Dans ce cas, l’image doit être téléchargée sur le serveur pour pouvoir être téléchargée par la suite via le réseau vers le client ou déplacée vers un dossier de préinstallation d’une image.</span><span class="sxs-lookup"><span data-stu-id="8769b-117">In such a case, the image should be uploaded to the server so that it can later be downloaded over the network to the client, or pushed to an image pre-stage folder.</span></span>



5. <span data-ttu-id="8769b-118">Cliquez sur la liste d' **images** pour afficher toutes les images disponibles.</span><span class="sxs-lookup"><span data-stu-id="8769b-118">Click the **Image** list to view all available images.</span></span> <span data-ttu-id="8769b-119">Sélectionnez l’image à copier dans le package.</span><span class="sxs-lookup"><span data-stu-id="8769b-119">Select the image to be copied to the package.</span></span> <span data-ttu-id="8769b-120">Cliquez sur **Actualiser** pour actualiser la liste des images disponibles.</span><span class="sxs-lookup"><span data-stu-id="8769b-120">Click **Refresh** to refresh the list of available images.</span></span>

6. <span data-ttu-id="8769b-121">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="8769b-121">Click **Next**.</span></span>

7. <span data-ttu-id="8769b-122">Dans la page **paramètres d’installation de med-v** , sélectionnez le fichier d’installation de med-v en effectuant l’une des opérations suivantes:</span><span class="sxs-lookup"><span data-stu-id="8769b-122">On the **MED-V Installation Settings** page, select the MED-V installation file by doing one of the following:</span></span>

   -   <span data-ttu-id="8769b-123">Dans le champ **fichier d’installation de MED-V** , tapez le chemin d’accès complet au répertoire dans lequel se trouve le fichier d’installation.</span><span class="sxs-lookup"><span data-stu-id="8769b-123">In the **MED-V installation file** field, type the full path to the directory where the installation file is located.</span></span>

   -   <span data-ttu-id="8769b-124">Cliquez sur **...** pour accéder au répertoire dans lequel se trouve le fichier d’installation.</span><span class="sxs-lookup"><span data-stu-id="8769b-124">Click **...** to browse to the directory where the installation file is located.</span></span>

   **<span data-ttu-id="8769b-125">Remarque</span><span class="sxs-lookup"><span data-stu-id="8769b-125">Note</span></span>**  
   <span data-ttu-id="8769b-126">Ce champ est obligatoire et ne s’applique pas sans nom de fichier valide.</span><span class="sxs-lookup"><span data-stu-id="8769b-126">This field is mandatory, and the wizard will not continue without a valid file name.</span></span>



8. <span data-ttu-id="8769b-127">Dans le champ **adresse du serveur** , tapez le nom ou l’adresse IP du serveur.</span><span class="sxs-lookup"><span data-stu-id="8769b-127">In the **Server address** field, type the server name or IP address.</span></span>

9. <span data-ttu-id="8769b-128">Dans le champ **port du serveur** , tapez le port du serveur.</span><span class="sxs-lookup"><span data-stu-id="8769b-128">In the **Server port** field, type the server port.</span></span>

10. <span data-ttu-id="8769b-129">Sélectionnez le **serveur est accessible à l’aide** de la case à cocher HTTPS pour exiger une connexion HTTPS pour la connexion au serveur.</span><span class="sxs-lookup"><span data-stu-id="8769b-129">Select the **Server is accessed using https** check box to require an https connection to connect to the server.</span></span>

11. <span data-ttu-id="8769b-130">Effectuez l'une des opérations suivantes:</span><span class="sxs-lookup"><span data-stu-id="8769b-130">Do one of the following:</span></span>

    -   <span data-ttu-id="8769b-131">Cliquez sur **paramètres d’installation par défaut**, puis cliquez sur **suivant** pour continuer et conserver les paramètres par défaut.</span><span class="sxs-lookup"><span data-stu-id="8769b-131">Click **Default installation settings**, and then click **Next** to continue and leave the default settings.</span></span>

    -   <span data-ttu-id="8769b-132">Cliquez sur **paramètres d’installation personnalisés**, puis cliquez sur **suivant** pour personnaliser les paramètres d’installation.</span><span class="sxs-lookup"><span data-stu-id="8769b-132">Click **Custom installation settings**, and then click **Next** to customize the installation settings.</span></span>

        1.  <span data-ttu-id="8769b-133">Dans la page **paramètres personnalisés de l’installation de med-v** , dans le champ **dossier d’installation** , tapez le chemin d’accès du dossier dans lequel les fichiers MED-V seront installés sur l’ordinateur hôte.</span><span class="sxs-lookup"><span data-stu-id="8769b-133">On the **MED-V Installation Custom Settings** page, in the **Installation folder** field, type the path of the folder where the MED-V files will be installed on the host computer.</span></span>

            **<span data-ttu-id="8769b-134">Remarque</span><span class="sxs-lookup"><span data-stu-id="8769b-134">Note</span></span>**  
            <span data-ttu-id="8769b-135">Il est recommandé d’utiliser des variables dans le chemin d’accès plutôt que des constantes, qui peuvent varier d’un ordinateur à un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="8769b-135">It is recommended to use variables in the path rather than constants, which might vary from computer to computer.</span></span>

            <span data-ttu-id="8769b-136">Par exemple, utilisez *%ProgramFiles%\\MED-V* à la place de *c:\\MED-V*.</span><span class="sxs-lookup"><span data-stu-id="8769b-136">For example, use *%ProgramFiles%\\MED-V* instead of *c:\\MED-V*.</span></span>



    ~~~
    2.  In the **Virtual machines images folder** field, type the path of the folder where the virtual images files will be installed on the host computer.

        **Note**  
        If you are using image pre-staging, this is the image pre-stage folder where the image is located.



    3.  In the **Minimal required RAM** field, enter the RAM required to install a MED-V package. If the user installing the MED-V package does not have the minimal required RAM, the installation will fail.

    4.  Select the **Install the MED-V management application** check box to include the MED-V management console application in the installation.

    5.  Select the **Create a shortcut to MED-V on the desktop** check box to create a shortcut to MED-V on the host's desktop.

    6.  Select the **Start automatically on computer startup** check box to start MED-V automatically on startup.

    7.  Click **Next**.
    ~~~

12. <span data-ttu-id="8769b-137">Sur la page **installations supplémentaires** , activez la case à cocher **inclure l’installation de la version du logiciel de virtualisation** pour inclure l’installation Virtual PC dans le package.</span><span class="sxs-lookup"><span data-stu-id="8769b-137">On the **Additional Installations** page, select the **Include installation of virtualization software** check box to include the Virtual PC installation in the package.</span></span>

    <span data-ttu-id="8769b-138">Le champ **fichier d’installation** est activé.</span><span class="sxs-lookup"><span data-stu-id="8769b-138">The **Installation file** field is enabled.</span></span> <span data-ttu-id="8769b-139">Tapez le chemin d’accès complet du fichier d’installation du logiciel de virtualisation ou cliquez sur **...** pour accéder au répertoire.</span><span class="sxs-lookup"><span data-stu-id="8769b-139">Type the full path of the virtualization software installation file, or click **...** to browse to the directory.</span></span>

13. <span data-ttu-id="8769b-140">Cochez la case **inclure l’installation de la version QFE de Virtual PC** pour inclure l’installation de la mise à jour Virtual PC dans le package.</span><span class="sxs-lookup"><span data-stu-id="8769b-140">Select the **Include installation of Virtual PC QFE** check box to include Virtual PC update installation in the package.</span></span>

    <span data-ttu-id="8769b-141">Le champ **fichier d’installation** est activé.</span><span class="sxs-lookup"><span data-stu-id="8769b-141">The **Installation file** field is enabled.</span></span> <span data-ttu-id="8769b-142">Tapez le chemin d’accès complet du fichier d’installation de la mise à jour Virtual PC ou cliquez sur **...** pour accéder au répertoire.</span><span class="sxs-lookup"><span data-stu-id="8769b-142">Type the full path of the Virtual PC update installation file, or click **...** to browse to the directory.</span></span>

14. <span data-ttu-id="8769b-143">Cochez la case **inclure l’installation de Microsoft .net framework 2,0** pour inclure l’installation de Microsoft .net Framework 2,0 dans le package.</span><span class="sxs-lookup"><span data-stu-id="8769b-143">Select the **Include installation of Microsoft .NET Framework 2.0** check box to include the Microsoft .NET Framework 2.0 installation in the package.</span></span>

    <span data-ttu-id="8769b-144">Le champ **fichier d’installation** est activé.</span><span class="sxs-lookup"><span data-stu-id="8769b-144">The **Installation file** field is enabled.</span></span> <span data-ttu-id="8769b-145">Tapez le chemin d’accès complet du fichier d’installation de Microsoft .NET Framework 2,0 ou cliquez sur **...** pour accéder au répertoire.</span><span class="sxs-lookup"><span data-stu-id="8769b-145">Type the full path of the Microsoft .NET Framework 2.0 installation file, or click **...** to browse to the directory.</span></span>

15. <span data-ttu-id="8769b-146">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="8769b-146">Click **Next**.</span></span>

16. <span data-ttu-id="8769b-147">Sur la page **Finalize** , sélectionnez l’emplacement dans lequel enregistrer le package en effectuant l’une des opérations suivantes:</span><span class="sxs-lookup"><span data-stu-id="8769b-147">On the **Finalize** page, select the location where the package should be saved by doing one of the following:</span></span>

    -   <span data-ttu-id="8769b-148">Dans le champ **destination du package** , tapez le chemin d’accès complet au répertoire dans lequel le package doit être enregistré.</span><span class="sxs-lookup"><span data-stu-id="8769b-148">In the **Package destination** field, type the full path to the directory where the package should be saved.</span></span>

    -   <span data-ttu-id="8769b-149">Cliquez sur **...** pour accéder au répertoire dans lequel les fichiers d’installation doivent être enregistrés.</span><span class="sxs-lookup"><span data-stu-id="8769b-149">Click **...** to browse to the directory where the installation files should be saved.</span></span>

    **<span data-ttu-id="8769b-150">Remarque</span><span class="sxs-lookup"><span data-stu-id="8769b-150">Note</span></span>**  
    <span data-ttu-id="8769b-151">La création du package peut consommer davantage d’espace que la taille réelle du package.</span><span class="sxs-lookup"><span data-stu-id="8769b-151">Building the package might consume more space than the actual package size.</span></span> <span data-ttu-id="8769b-152">C’est pourquoi il est recommandé de générer le package sur le disque dur.</span><span class="sxs-lookup"><span data-stu-id="8769b-152">It is therefore recommended to build the package on the hard drive.</span></span> <span data-ttu-id="8769b-153">Une fois le package créé, il peut être copié sur le USB.</span><span class="sxs-lookup"><span data-stu-id="8769b-153">After the package is created, it can then be copied to the USB.</span></span>



17. <span data-ttu-id="8769b-154">Dans le champ **nom du package** , entrez le nom du package.</span><span class="sxs-lookup"><span data-stu-id="8769b-154">In the **Package name** field, enter a name for the package.</span></span>

18. <span data-ttu-id="8769b-155">Cliquez sur **Terminer** pour créer le package.</span><span class="sxs-lookup"><span data-stu-id="8769b-155">Click **Finish** to create the package.</span></span>

    <span data-ttu-id="8769b-156">Le package est créé.</span><span class="sxs-lookup"><span data-stu-id="8769b-156">The package is created.</span></span> <span data-ttu-id="8769b-157">Cela peut prendre quelques minutes.</span><span class="sxs-lookup"><span data-stu-id="8769b-157">This might take several minutes.</span></span>

    <span data-ttu-id="8769b-158">Une fois le package créé, un message s’affiche pour vous signaler qu’il s’est terminé correctement.</span><span class="sxs-lookup"><span data-stu-id="8769b-158">After the package is created, a message appears notifying you that it has been completed successfully.</span></span>

**<span data-ttu-id="8769b-159">Remarque</span><span class="sxs-lookup"><span data-stu-id="8769b-159">Note</span></span>**  
<span data-ttu-id="8769b-160">Si vous avez enregistré tous les fichiers localement et pas directement sur le média amovible, assurez-vous de copier uniquement le contenu du dossier et non le dossier proprement dit sur le média amovible.</span><span class="sxs-lookup"><span data-stu-id="8769b-160">If you saved all the files locally, and not directly on the removable media, ensure that you copy only the contents of the folder and not the folder itself to the removable media.</span></span>



**<span data-ttu-id="8769b-161">Remarque</span><span class="sxs-lookup"><span data-stu-id="8769b-161">Note</span></span>**  
<span data-ttu-id="8769b-162">Le média amovible doit être suffisamment grand pour que le contenu du package n’utilise que trois quarts de la mémoire du support amovible.</span><span class="sxs-lookup"><span data-stu-id="8769b-162">The removable media must be large enough so that the package contents consume a maximum of only three-quarters of the removable media's memory.</span></span>



**<span data-ttu-id="8769b-163">Remarque</span><span class="sxs-lookup"><span data-stu-id="8769b-163">Note</span></span>**  
<span data-ttu-id="8769b-164">Lors de la création du package, un maximum de deux fois la taille de package réelle peut être requis lorsque la build est terminée.</span><span class="sxs-lookup"><span data-stu-id="8769b-164">When creating the package, up to double the size of the actual package size might be required when the build is complete.</span></span>



## <span data-ttu-id="8769b-165">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8769b-165">Related topics</span></span>


[<span data-ttu-id="8769b-166">Création d'une image MED-V</span><span class="sxs-lookup"><span data-stu-id="8769b-166">Creating a MED-V Image</span></span>](creating-a-med-v-image.md)









