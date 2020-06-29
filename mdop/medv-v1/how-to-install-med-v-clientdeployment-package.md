---
title: Comment installer MED-V Client
description: Comment installer MED-V Client
author: dansimp
ms.assetid: bfac6de7-d96d-4b3e-bd8b-183e051e53c8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b2e4468b15c0c196bf605b1b5d129ab38678ec74
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812209"
---
# <span data-ttu-id="236d8-103">Comment installer MED-V Client</span><span class="sxs-lookup"><span data-stu-id="236d8-103">How to Install MED-V Client</span></span>


<span data-ttu-id="236d8-104">Dans un scénario basé sur un package de déploiement, l’installation du client MED-V est incluse dans le package de déploiement et installée directement à partir du package.</span><span class="sxs-lookup"><span data-stu-id="236d8-104">In a deployment package-based scenario, the MED-V client installation is included in the deployment package and installed directly from the package.</span></span>

**<span data-ttu-id="236d8-105">Important</span><span class="sxs-lookup"><span data-stu-id="236d8-105">Important</span></span>**  
<span data-ttu-id="236d8-106">Lors de l’utilisation d’un package de déploiement qui n’inclut pas d’image, assurez-vous que l’image est téléchargée sur le Web ou déplacée vers le dossier de préinstallation avant d’installer le package de déploiement.</span><span class="sxs-lookup"><span data-stu-id="236d8-106">When using a deployment package that does not include an image, ensure that the image is uploaded to the Web or pushed to the pre-stage folder prior to installing the deployment package.</span></span>



**<span data-ttu-id="236d8-107">Pour installer un package de déploiement</span><span class="sxs-lookup"><span data-stu-id="236d8-107">To install a deployment package</span></span>**

1.  <span data-ttu-id="236d8-108">Effectuez l'une des opérations suivantes:</span><span class="sxs-lookup"><span data-stu-id="236d8-108">Do one of the following:</span></span>

    -   <span data-ttu-id="236d8-109">Téléchargez le package MED-V à partir du Web.</span><span class="sxs-lookup"><span data-stu-id="236d8-109">Download the MED-V package from the Web.</span></span>

    -   <span data-ttu-id="236d8-110">Insérez le port USB ou DVD de déploiement dans le lecteur hôte.</span><span class="sxs-lookup"><span data-stu-id="236d8-110">Insert the deployment USB or DVD into the host drive.</span></span>

2.  <span data-ttu-id="236d8-111">Si MED-V ne démarre pas automatiquement, double-cliquez sur MED-VAutoInstaller.exe.</span><span class="sxs-lookup"><span data-stu-id="236d8-111">If MED-V does not launch automatically, double-click MED-VAutoInstaller.exe.</span></span>

    <span data-ttu-id="236d8-112">Une boîte de dialogue s’affiche, indiquant les composants déjà installés et ceux qui sont actuellement installés.</span><span class="sxs-lookup"><span data-stu-id="236d8-112">A dialog box appears listing the components that are already installed and those that are currently being installed.</span></span>

    **<span data-ttu-id="236d8-113">Remarque</span><span class="sxs-lookup"><span data-stu-id="236d8-113">Note</span></span>**  
    <span data-ttu-id="236d8-114">Si une version de Microsoft Virtual PC non prise en charge existe sur l’ordinateur hôte, un message s’affiche pour vous demander de désinstaller la version existante et de réexécuter le programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="236d8-114">If a version of the Microsoft Virtual PC that is not supported exists on the host computer, a message will appear telling you to uninstall the existing version and run the installer again.</span></span>



~~~
**Note**  
If an older version of the MED-V client exists, it will prompt you asking whether you want to upgrade.



Depending on the components that have been installed, you might need to reboot. If rebooting is necessary, a message appears notifying you that you must reboot.
~~~

3. <span data-ttu-id="236d8-115">Le cas échéant, redémarrez l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="236d8-115">If necessary, reboot the computer.</span></span>

   <span data-ttu-id="236d8-116">Lorsque l’installation est terminée, MED-V démarre et un message s’affiche, indiquant que l’installation est terminée.</span><span class="sxs-lookup"><span data-stu-id="236d8-116">When the installation is complete, MED-V starts and a message appears notifying you that the installation is complete.</span></span>

4. <span data-ttu-id="236d8-117">Connectez-vous à MED-V en utilisant le nom d’utilisateur et le mot de passe suivants:</span><span class="sxs-lookup"><span data-stu-id="236d8-117">Log in to MED-V using the following user name and password:</span></span>

   -   <span data-ttu-id="236d8-118">Entrez le nom de domaine et le nom d’utilisateur, suivis du mot de passe de l’utilisateur autorisé à travailler avec MED-V.</span><span class="sxs-lookup"><span data-stu-id="236d8-118">Type in the domain name and user name followed by the password of the domain user who is permitted to work with MED-V.</span></span>

       <span data-ttu-id="236d8-119">Exemple: "Domain \ _name \\user\ _name", "password"</span><span class="sxs-lookup"><span data-stu-id="236d8-119">Example: "domain\_name\\user\_name", "password"</span></span>

## <span data-ttu-id="236d8-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="236d8-120">Related topics</span></span>


[<span data-ttu-id="236d8-121">Comment configurer un package de déploiement</span><span class="sxs-lookup"><span data-stu-id="236d8-121">How to Configure a Deployment Package</span></span>](how-to-configure-a-deployment-package.md)

[<span data-ttu-id="236d8-122">Comment charger une image MED-V sur le serveur</span><span class="sxs-lookup"><span data-stu-id="236d8-122">How to Upload a MED-V Image to the Server</span></span>](how-to-upload-a-med-v-image-to-the-server.md)

[<span data-ttu-id="236d8-123">Référence des lignes de commande d'installation du client</span><span class="sxs-lookup"><span data-stu-id="236d8-123">Client Installation Command Line Reference</span></span>](client-installation-command-line-reference.md)









