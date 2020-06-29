---
title: Comment affecter les informations d’identification appropriées pour Windows Vista
description: Comment affecter les informations d’identification appropriées pour Windows Vista
author: dansimp
ms.assetid: cc11d2af-a350-4d16-ba7b-f9c1d89e14b4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 111dafea505133f123cf8531a2891a452e725ac2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808712"
---
# <span data-ttu-id="cb943-103">Comment affecter les informations d’identification appropriées pour Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cb943-103">How to Assign the Proper Credentials for Windows Vista</span></span>


<span data-ttu-id="cb943-104">Utilisez la procédure suivante pour configurer le client de bureau App-V pour les informations d’identification Vista appropriées.</span><span class="sxs-lookup"><span data-stu-id="cb943-104">Use the following procedure to configure the App-V Desktop Client for proper WindowsVista credentials.</span></span>

<span data-ttu-id="cb943-105">**Remarques**  Cette procédure doit être effectuée sur tous les ordinateurs non membres du domaine.</span><span class="sxs-lookup"><span data-stu-id="cb943-105">**Note** This procedure must be completed on each non-domain joined computer.</span></span> <span data-ttu-id="cb943-106">En fonction du nombre d’ordinateurs appartenant à un domaine différent dans votre environnement, il peut s’agir d’une opération laborieuse.</span><span class="sxs-lookup"><span data-stu-id="cb943-106">Depending on the number of non-domain joined computers in your environment, this could be a very tedious operation.</span></span> <span data-ttu-id="cb943-107">Vous pouvez utiliser les scripts et l’interface de ligne de commande pour le gestionnaire d’informations d’identification pour aider les administrateurs à automatiser ce processus.</span><span class="sxs-lookup"><span data-stu-id="cb943-107">You can use scripts and the command-line interface for Credential Manager to help administrators automate this process.</span></span>

 

**<span data-ttu-id="cb943-108">Pour attribuer les informations d’identification appropriées pour les clients App-V exécutant Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cb943-108">To assign the proper credentials for App-V clients running Windows Vista</span></span>**

1.  <span data-ttu-id="cb943-109">Pour les privilèges d’administrateur sur le client de bureau App-V exécutant Windows Vista, ouvrez le panneau de configuration des **comptes d’utilisateurs** (panneau de configuration classique).</span><span class="sxs-lookup"><span data-stu-id="cb943-109">With administrator privileges on the App-V Desktop Client running Windows Vista, open the **User Accounts** control panel (Classic Control Panel).</span></span>

2.  <span data-ttu-id="cb943-110">Sélectionnez **gérer vos mots de passe réseau** dans les **comptes d’utilisateurs** dans le volet tâches de gauche.</span><span class="sxs-lookup"><span data-stu-id="cb943-110">Select **Manage your network passwords** from **User Accounts** in the left tasks pane.</span></span>

3.  <span data-ttu-id="cb943-111">Sélectionnez **Ajouter** dans l’écran **noms et mots de passe des utilisateurs enregistrés** .</span><span class="sxs-lookup"><span data-stu-id="cb943-111">Select **Add** on the **Stored User Names and Passwords** screen.</span></span>

4.  <span data-ttu-id="cb943-112">Dans l’écran **propriétés d’informations d’identification stockées** , entrez les informations relatives à l’infrastructure App-V:</span><span class="sxs-lookup"><span data-stu-id="cb943-112">On the **Stored Credential Properties** screen, provide the information for the App-V infrastructure:</span></span>

    1.  <span data-ttu-id="cb943-113">**Connectez-vous à:** Nom externe du serveur de publication.</span><span class="sxs-lookup"><span data-stu-id="cb943-113">**Log on to:** External name of the publishing server.</span></span>

    2.  <span data-ttu-id="cb943-114">**Nom d’utilisateur:** Nom d’utilisateur de l’utilisateur externe sous la forme Domain\\Username.</span><span class="sxs-lookup"><span data-stu-id="cb943-114">**User name:** User name for the external user in the form Domain\\Username.</span></span>

    3.  <span data-ttu-id="cb943-115">**Mot de passe:** Mot de passe du compte d’utilisateur entré dans le champ **nom d’utilisateur** .</span><span class="sxs-lookup"><span data-stu-id="cb943-115">**Password:** Password for the user account entered in the **User name** field.</span></span>

    4.  <span data-ttu-id="cb943-116">Laissez **type d’informations d’identification** sélectionné, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="cb943-116">Leave **Credential Type** selected, and click **OK**.</span></span>

5.  <span data-ttu-id="cb943-117">Cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="cb943-117">Click **Close**.</span></span> <span data-ttu-id="cb943-118">Les informations d’identification sont stockées dans le magasin d’informations d’identification pour une authentification correcte auprès de l’infrastructure App-V.</span><span class="sxs-lookup"><span data-stu-id="cb943-118">The credentials are stored in the credential store for proper authentication to the App-V infrastructure.</span></span>

## <span data-ttu-id="cb943-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="cb943-119">Related topics</span></span>


[<span data-ttu-id="cb943-120">Clients joints au domaine et non joints au domaine</span><span class="sxs-lookup"><span data-stu-id="cb943-120">Domain-Joined and Non-Domain-Joined Clients</span></span>](domain-joined-and-non-domain-joined-clients.md)

[<span data-ttu-id="cb943-121">Comment affecter les informations d’identification appropriées pour Windows XP</span><span class="sxs-lookup"><span data-stu-id="cb943-121">How to Assign the Proper Credentials for Windows XP</span></span>](how-to-assign--the-proper-credentials-for-windows-xp.md)

 

 





