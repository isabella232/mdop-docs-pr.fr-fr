---
title: Procédure pour mettre à niveau un package
description: Procédure pour mettre à niveau un package
author: dansimp
ms.assetid: 831c7556-6f6c-4b3a-aefb-26889094dc1a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0a9b3eca2c996337d79e551784818a421f495316
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806733"
---
# <span data-ttu-id="1028f-103">Procédure pour mettre à niveau un package</span><span class="sxs-lookup"><span data-stu-id="1028f-103">How to Upgrade a Package</span></span>


<span data-ttu-id="1028f-104">Le processus de mise à niveau automatique est le même que pour ajouter une version de package dans la console de gestion du serveur d’applications.</span><span class="sxs-lookup"><span data-stu-id="1028f-104">The process for an automatic upgrade is the same as for adding a package version in the Application Virtualization Server Management Console.</span></span> <span data-ttu-id="1028f-105">Une mise à niveau automatique est effectuée lorsque vous reséquencez l’application dans un package existant.</span><span class="sxs-lookup"><span data-stu-id="1028f-105">An automatic upgrade is performed when you resequence the application in an existing package.</span></span> <span data-ttu-id="1028f-106">Vous pouvez ensuite ajouter cette nouvelle version à vos serveurs pour la diffusion en continu.</span><span class="sxs-lookup"><span data-stu-id="1028f-106">Then you can add this new version to your servers for streaming.</span></span>

<span data-ttu-id="1028f-107">Lorsque vous effectuez une mise à niveau d’un package avec une nouvelle version, vous pouvez laisser la version existante en place ou la supprimer et ne conserver que la plus récente.</span><span class="sxs-lookup"><span data-stu-id="1028f-107">When you upgrade a package with a new version, you can leave the existing version in place or delete it and leave only the newest one.</span></span> <span data-ttu-id="1028f-108">Vous souhaiterez peut-être conserver l’ancienne version en vigueur pour la compatibilité avec les documents hérités ou pour tester la nouvelle version avant de la rendre disponible pour tous les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="1028f-108">You might want to leave the old version in place for compatibility with legacy documents or so that you can test the new version before making it available to all users.</span></span>

**<span data-ttu-id="1028f-109">Pour mettre à niveau un package automatiquement</span><span class="sxs-lookup"><span data-stu-id="1028f-109">To upgrade a package automatically</span></span>**

1.  <span data-ttu-id="1028f-110">Copiez le nouveau fichier SFT dans le dossier de contenu du serveur de virtualisation des applications.</span><span class="sxs-lookup"><span data-stu-id="1028f-110">Copy the new SFT file to the Application Virtualization Server's content folder.</span></span>

    <span data-ttu-id="1028f-111">**Remarques**  Si le reséquençage n’a pas ajouté de fonctionnalités qui ont modifié les fichiers de description de logiciel (OSD), d’icône (ICO) ou de projet de Sequencer (SPRJ), vous n’avez pas besoin de les copier.</span><span class="sxs-lookup"><span data-stu-id="1028f-111">**Note** If resequencing did not add features that changed the Open Software Descriptor (OSD), icon (ICO), or Sequencer Project (SPRJ) files, you do not need to copy those.</span></span> <span data-ttu-id="1028f-112">Vous pouvez inclure ces fichiers si vous souhaitez que ces fichiers affichent la même date.</span><span class="sxs-lookup"><span data-stu-id="1028f-112">You can include these files if you want all these files to display the same date.</span></span>

     

2.  <span data-ttu-id="1028f-113">Dans le volet gauche de la console de gestion du serveur d’applications, développez **packages**.</span><span class="sxs-lookup"><span data-stu-id="1028f-113">In left pane of the Application Virtualization Server Management Console, expand **Packages**.</span></span>

3.  <span data-ttu-id="1028f-114">Cliquez avec le bouton droit sur le package que vous voulez mettre à niveau, puis sélectionnez **Ajouter une version**.</span><span class="sxs-lookup"><span data-stu-id="1028f-114">Right-click the package you want to upgrade, and select **Add Version**.</span></span>

4.  <span data-ttu-id="1028f-115">Dans la boîte de dialogue **Ajouter une version de package** , recherchez ou tapez le chemin d’accès complet de la nouvelle version de l’application dans le chemin d' **accès complet pour le champ fichier** .</span><span class="sxs-lookup"><span data-stu-id="1028f-115">In the **Add Package Version** dialog box, browse for or type the full path name for the new application version in the **Full Path for the file** field.</span></span> <span data-ttu-id="1028f-116">Il doit s’agir d’un fichier SFT.</span><span class="sxs-lookup"><span data-stu-id="1028f-116">This must be an SFT file.</span></span>

5.  <span data-ttu-id="1028f-117">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="1028f-117">Click **Next**.</span></span>

6.  <span data-ttu-id="1028f-118">La boîte de dialogue **récapitulative** montre l’emplacement du fichier et vous invite à le faire si vous ne l’avez pas déjà fait.</span><span class="sxs-lookup"><span data-stu-id="1028f-118">The **Summary** dialog box shows the file location and prompts you to copy the file there if you have not already done so.</span></span> <span data-ttu-id="1028f-119">Cliquez sur **Terminer** une fois que vous avez vérifié les informations.</span><span class="sxs-lookup"><span data-stu-id="1028f-119">Click **Finish** after you have verified the information.</span></span>

    <span data-ttu-id="1028f-120">La nouvelle version est maintenant terminée et prête à être diffusée.</span><span class="sxs-lookup"><span data-stu-id="1028f-120">The new version is now complete and ready to stream.</span></span>

## <span data-ttu-id="1028f-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1028f-121">Related topics</span></span>


[<span data-ttu-id="1028f-122">Procédure pour gérer les packages dans Server Management Console</span><span class="sxs-lookup"><span data-stu-id="1028f-122">How to Manage Packages in the Server Management Console</span></span>](how-to-manage-packages-in-the-server-management-console.md)

 

 





