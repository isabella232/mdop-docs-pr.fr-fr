---
title: Procédure pour ajouter une version de package
description: Procédure pour ajouter une version de package
author: dansimp
ms.assetid: dbb829c1-e5cb-4a2f-bc17-9a9bb50c671c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a60252e8b43af61ad548df30a93d8fbc9bae0cb7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808735"
---
# <span data-ttu-id="9bff3-103">Procédure pour ajouter une version de package</span><span class="sxs-lookup"><span data-stu-id="9bff3-103">How to Add a Package Version</span></span>


<span data-ttu-id="9bff3-104">Dans la console de gestion de l’application virtualisation du serveur, lorsque vous recommandez un package, vous pouvez utiliser la procédure suivante pour ajouter la nouvelle version à vos serveurs pour la diffusion en continu.</span><span class="sxs-lookup"><span data-stu-id="9bff3-104">In the Application Virtualization Server Management Console, when you resequence a package, you can use the following procedure to add the new version to your servers for streaming.</span></span>

<span data-ttu-id="9bff3-105">**Remarques**  Lorsque vous effectuez une mise à niveau d’un package avec une nouvelle version, vous pouvez laisser la version existante en place ou la supprimer et ne conserver que la plus récente.</span><span class="sxs-lookup"><span data-stu-id="9bff3-105">**Note** When you upgrade a package with a new version, you can leave the existing version in place or delete it and leave only the newest one.</span></span> <span data-ttu-id="9bff3-106">Vous souhaiterez peut-être conserver l’ancienne version en vigueur pour la compatibilité avec les documents hérités ou pour tester la nouvelle version avant de la rendre disponible pour tous les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="9bff3-106">You might want to leave the old version in place for compatibility with legacy documents or so that you can test the new version before making it available to all users.</span></span>

 

**<span data-ttu-id="9bff3-107">Pour ajouter une version de package</span><span class="sxs-lookup"><span data-stu-id="9bff3-107">To add a package version</span></span>**

1.  <span data-ttu-id="9bff3-108">Copiez le nouveau fichier SFT dans le dossier Content du serveur d’applications.</span><span class="sxs-lookup"><span data-stu-id="9bff3-108">Copy the new SFT file to the application server's content folder.</span></span> <span data-ttu-id="9bff3-109">Si le reséquençage n’a pas ajouté de modifications aux fichiers Open Software Descriptor (OSD), Icon ou Sequencer (SPRJ), vous n’avez pas besoin de les copier.</span><span class="sxs-lookup"><span data-stu-id="9bff3-109">If resequencing did not add changes to the Open Software Descriptor (OSD), icon (ICO), or Sequencer Project (SPRJ) files, you do not need to copy those.</span></span> <span data-ttu-id="9bff3-110">Vous pouvez inclure ces fichiers si vous souhaitez que tous les fichiers affichent la même date.</span><span class="sxs-lookup"><span data-stu-id="9bff3-110">You can include those files if you want all the files to display the same date.</span></span>

2.  <span data-ttu-id="9bff3-111">Dans le volet gauche de la console de gestion du serveur d’applications, développez le nœud **packages** .</span><span class="sxs-lookup"><span data-stu-id="9bff3-111">In left pane of the Application Virtualization Server Management Console, expand the **Packages** node.</span></span>

3.  <span data-ttu-id="9bff3-112">Cliquez avec le bouton droit sur le package que vous voulez mettre à jour, puis choisissez **Ajouter une version**.</span><span class="sxs-lookup"><span data-stu-id="9bff3-112">Right-click the package you want to upgrade, and choose **Add Version**.</span></span>

4.  <span data-ttu-id="9bff3-113">Dans la boîte de dialogue **Ajouter une version de package** , recherchez ou tapez le chemin d’accès du nouveau fichier d’application dans le champ chemin d' **accès complet du fichier de package** .</span><span class="sxs-lookup"><span data-stu-id="9bff3-113">In the **Add Package Version** dialog box, browse for or type the path name for the new application file in the **Full path for package file** field.</span></span> <span data-ttu-id="9bff3-114">Il doit s’agir d’un fichier SFT.</span><span class="sxs-lookup"><span data-stu-id="9bff3-114">This must be an SFT file.</span></span>

5.  <span data-ttu-id="9bff3-115">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="9bff3-115">Click **Next**.</span></span>

6.  <span data-ttu-id="9bff3-116">La boîte de dialogue **récapitulative** montre l’emplacement du fichier et vous invite à le faire si vous ne l’avez pas déjà fait.</span><span class="sxs-lookup"><span data-stu-id="9bff3-116">The **Summary** dialog box shows the file location and prompts you to copy the file there if you have not already done so.</span></span> <span data-ttu-id="9bff3-117">Cliquez sur **Terminer** une fois que vous avez vérifié les informations.</span><span class="sxs-lookup"><span data-stu-id="9bff3-117">Click **Finish** after you have verified the information.</span></span>

    <span data-ttu-id="9bff3-118">La nouvelle version est maintenant terminée et prête à être diffusée.</span><span class="sxs-lookup"><span data-stu-id="9bff3-118">The new version is now complete and ready to stream.</span></span>

## <span data-ttu-id="9bff3-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9bff3-119">Related topics</span></span>


[<span data-ttu-id="9bff3-120">Procédure pour supprimer un package</span><span class="sxs-lookup"><span data-stu-id="9bff3-120">How to Delete a Package</span></span>](how-to-delete-a-packageserver.md)

[<span data-ttu-id="9bff3-121">Procédure pour gérer les packages dans Server Management Console</span><span class="sxs-lookup"><span data-stu-id="9bff3-121">How to Manage Packages in the Server Management Console</span></span>](how-to-manage-packages-in-the-server-management-console.md)

 

 





