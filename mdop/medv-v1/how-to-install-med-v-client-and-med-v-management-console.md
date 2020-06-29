---
title: Comment installer le client MED-V et la console de gestion MED-V
description: Comment installer le client MED-V et la console de gestion MED-V
author: dansimp
ms.assetid: 8a5f3010-3a50-487e-99d8-e352e5cb51c6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 24a486cc7cf5534171f80b08dc93742e03cd4a0d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812083"
---
# <span data-ttu-id="ed04f-103">Comment installer le client MED-V et la console de gestion MED-V</span><span class="sxs-lookup"><span data-stu-id="ed04f-103">How to Install MED-V Client and MED-V Management Console</span></span>


<span data-ttu-id="ed04f-104">Les composants MED-V suivants sont inclus dans le package client. msi:</span><span class="sxs-lookup"><span data-stu-id="ed04f-104">The following MED-V components are included in the client .msi package:</span></span>

-   <span data-ttu-id="ed04f-105">Client MED-V: logiciel MED-V qui doit être installé sur les ordinateurs clients pour exécuter des espaces de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="ed04f-105">MED-V client—The MED-V software that must be installed on client computers for running MED-V workspaces.</span></span>

-   <span data-ttu-id="ed04f-106">La console de gestion MED-V, l’outil d’administration que les administrateurs peuvent utiliser pour créer et gérer des images, des espaces de travail MED-V et des stratégies.</span><span class="sxs-lookup"><span data-stu-id="ed04f-106">MED-V management console—The administrative tool that administrators can use to create and maintain images, MED-V workspaces, and policies.</span></span>

<span data-ttu-id="ed04f-107">La console de gestion MED-V et le client MED-V sont tous deux installés à partir du package client MED-V.</span><span class="sxs-lookup"><span data-stu-id="ed04f-107">The MED-V management console and the MED-V client are both installed from the MED-V client .msi package.</span></span> <span data-ttu-id="ed04f-108">Toutefois, le client MED-V peut être installé indépendamment sans la console de gestion MED-V en désactivant la case à cocher **installer l’application de gestion Med-v** lors de l’installation.</span><span class="sxs-lookup"><span data-stu-id="ed04f-108">The MED-V client, however, can be installed independently without the MED-V management console by clearing the **Install the MED-V Management application** check box during installation.</span></span>

**<span data-ttu-id="ed04f-109">Remarque</span><span class="sxs-lookup"><span data-stu-id="ed04f-109">Note</span></span>**  
<span data-ttu-id="ed04f-110">Les clients MED-V et la console de gestion MED-V peuvent uniquement être installés sur des ordinateurs Windows 7, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ed04f-110">The MED-V client and MED-V management console can only be installed on Windows 7-, Windows Vista-, and Windows XP-based computers.</span></span> <span data-ttu-id="ed04f-111">Elles ne peuvent pas être installées sur les produits serveur.</span><span class="sxs-lookup"><span data-stu-id="ed04f-111">They cannot be installed on server products.</span></span>



**<span data-ttu-id="ed04f-112">Remarque</span><span class="sxs-lookup"><span data-stu-id="ed04f-112">Note</span></span>**  
<span data-ttu-id="ed04f-113">N’installez pas le client MED-V à l’aide de la commande Windows **runas** .</span><span class="sxs-lookup"><span data-stu-id="ed04f-113">Do not install the MED-V client using the Windows **runas** command.</span></span>



**<span data-ttu-id="ed04f-114">Pour installer le client MED-V</span><span class="sxs-lookup"><span data-stu-id="ed04f-114">To install the MED-V client</span></span>**

1.  <span data-ttu-id="ed04f-115">Connectez-vous en tant qu’utilisateur disposant de droits d’administrateur local sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="ed04f-115">Log in as a user with local administrator rights on the local computer.</span></span>

2.  <span data-ttu-id="ed04f-116">Exécutez le package MED-V. msi.</span><span class="sxs-lookup"><span data-stu-id="ed04f-116">Run the MED-V .msi package.</span></span>

    <span data-ttu-id="ed04f-117">Le package MED-V. msi est appelé *MED-V\_x.msi*, où *x* représente le numéro de version.</span><span class="sxs-lookup"><span data-stu-id="ed04f-117">The MED-V .msi package is called *MED-V\_x.msi*, where *x* is the version number.</span></span>

    <span data-ttu-id="ed04f-118">Par exemple, *MED-V\_1.0.65.msi*.</span><span class="sxs-lookup"><span data-stu-id="ed04f-118">For example, *MED-V\_1.0.65.msi*.</span></span>

3.  <span data-ttu-id="ed04f-119">Lorsque l’écran d’accueil de l' **Assistant InstallShield** s’affiche, cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="ed04f-119">When the **InstallShield Wizard Welcome** screen appears, click **Next**.</span></span>

4.  <span data-ttu-id="ed04f-120">Sur l’écran **contrat de licence** , lisez le contrat de licence, cliquez sur **J’accepte les termes du contrat de licence**, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="ed04f-120">On the **License Agreement** screen, read the license agreement, click **I accept the terms in the license agreement**, and click **Next**.</span></span>

    <span data-ttu-id="ed04f-121">L’écran **dossier de destination** s’affiche avec le dossier d’installation par défaut affiché.</span><span class="sxs-lookup"><span data-stu-id="ed04f-121">The **Destination Folder** screen appears, with the default installation folder displayed.</span></span>

    <span data-ttu-id="ed04f-122">Le dossier d’installation par défaut est le répertoire dans lequel le système d’exploitation est installé.</span><span class="sxs-lookup"><span data-stu-id="ed04f-122">The default installation folder is the directory where the operating system is installed.</span></span>

    -   <span data-ttu-id="ed04f-123">Pour modifier le dossier dans lequel vous souhaitez installer MED-V, cliquez sur **modifier**, puis recherchez un dossier existant.</span><span class="sxs-lookup"><span data-stu-id="ed04f-123">To change the folder where MED-V should be installed, click **Change**, and browse to an existing folder.</span></span>

5.  <span data-ttu-id="ed04f-124">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="ed04f-124">Click **Next**.</span></span>

6.  <span data-ttu-id="ed04f-125">Dans l’écran **paramètres de med-v** , configurez l’installation de med-v comme suit:</span><span class="sxs-lookup"><span data-stu-id="ed04f-125">On the **MED-V Settings** screen, configure the MED-V installation as follows:</span></span>

    -   <span data-ttu-id="ed04f-126">Activez la case à cocher **installer l’application de gestion MED-V** pour inclure le composant de gestion dans l’installation.</span><span class="sxs-lookup"><span data-stu-id="ed04f-126">Select the **Install the MED-V management application** check box to include the management component in the installation.</span></span>

        **<span data-ttu-id="ed04f-127">Remarque</span><span class="sxs-lookup"><span data-stu-id="ed04f-127">Note</span></span>**  
        <span data-ttu-id="ed04f-128">Les administrateurs de virtualisation de bureau de l’entreprise doivent installer l’application de gestion MED-V.</span><span class="sxs-lookup"><span data-stu-id="ed04f-128">Enterprise Desktop Virtualization administrators should install the MED-V management application.</span></span> <span data-ttu-id="ed04f-129">Cette application est nécessaire pour la configuration des images de bureau et des espaces de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="ed04f-129">This application is required for configuring desktop images and MED-V workspaces.</span></span>



~~~
-   Select the **Load MED-V when Windows starts** check box to start MED-V automatically on startup.

-   Select the **Add a MED-V shortcut to my desktop** check box to create a MED-V shortcut on your desktop.

-   In the **Server address** field, type the server address.

-   In the **Server port** field, type the server's port.

-   Select the **Server requires encrypted connections (https)** check box to work with https.

-   The default virtual machine images folder is displayed. The default installation folder is *%systemdrive%\\MED-V Images\\*. To change the folder where MED-V should be installed, click **Change**, and browse to an existing folder.
~~~

7. <span data-ttu-id="ed04f-130">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="ed04f-130">Click **Next**.</span></span>

8. <span data-ttu-id="ed04f-131">Dans l’écran **prêt à installer le programme** , cliquez sur **installer**.</span><span class="sxs-lookup"><span data-stu-id="ed04f-131">On the **Ready to Install the Program** screen, click **Install**.</span></span>

   <span data-ttu-id="ed04f-132">L’installation du client MED-V démarre.</span><span class="sxs-lookup"><span data-stu-id="ed04f-132">The MED-V client installation starts.</span></span> <span data-ttu-id="ed04f-133">Cela peut prendre quelques minutes et l’écran risque de ne pas afficher de texte.</span><span class="sxs-lookup"><span data-stu-id="ed04f-133">This can take several minutes, and the screen might not display text.</span></span> <span data-ttu-id="ed04f-134">Lors de l’installation, plusieurs écrans de progression apparaissent.</span><span class="sxs-lookup"><span data-stu-id="ed04f-134">During installation, several progress screens appear.</span></span> <span data-ttu-id="ed04f-135">Si un message s’affiche, suivez les instructions fournies.</span><span class="sxs-lookup"><span data-stu-id="ed04f-135">If a message appears, follow the instructions provided.</span></span>

   <span data-ttu-id="ed04f-136">Une fois l’installation terminée, l’écran **InstallShield terminé** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="ed04f-136">Upon successful installation, the **InstallShield Wizard Completed** screen appears.</span></span>

9. <span data-ttu-id="ed04f-137">Cliquez sur **Terminer** pour fermer l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="ed04f-137">Click **Finish** to close the wizard.</span></span>

## <span data-ttu-id="ed04f-138">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ed04f-138">Related topics</span></span>


[<span data-ttu-id="ed04f-139">Configurations prises en charge</span><span class="sxs-lookup"><span data-stu-id="ed04f-139">Supported Configurations</span></span>](supported-configurationsmedv-orientation.md)

[<span data-ttu-id="ed04f-140">Listes de contrôle pour l'installation et la mise à niveau</span><span class="sxs-lookup"><span data-stu-id="ed04f-140">Installation and Upgrade Checklists</span></span>](installation-and-upgrade-checklists.md)









