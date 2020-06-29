---
title: Comment affecter les informations d’identification appropriées pour Windows XP
description: Comment affecter les informations d’identification appropriées pour Windows XP
author: dansimp
ms.assetid: cddbd556-d8f9-4981-a947-6e8e3f552b70
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 81581b75a9b7d5ce35e1c50fd01e0b7bbd3f7ef5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807861"
---
# <span data-ttu-id="e865e-103">Comment affecter les informations d’identification appropriées pour Windows XP</span><span class="sxs-lookup"><span data-stu-id="e865e-103">How to Assign the Proper Credentials for Windows XP</span></span>


<span data-ttu-id="e865e-104">Utilisez la procédure suivante pour configurer le client de bureau App-V pour les informations d’identification WindowsXP appropriées.</span><span class="sxs-lookup"><span data-stu-id="e865e-104">Use the following procedure to configure the App-V Desktop Client for proper WindowsXP credentials.</span></span>

<span data-ttu-id="e865e-105">**Remarques**  Après avoir terminé cette procédure, le client sans domaine joint peut effectuer une actualisation de publication sans être joint à un domaine.</span><span class="sxs-lookup"><span data-stu-id="e865e-105">**Note** After finishing this procedure, the non-domain joined client can perform a publishing refresh without being joined to a domain.</span></span>

 

**<span data-ttu-id="e865e-106">Pour attribuer les informations d’identification appropriées pour les clients App-V exécutant WindowsXP</span><span class="sxs-lookup"><span data-stu-id="e865e-106">To assign the proper credentials for App-V clients running WindowsXP</span></span>**

1.  <span data-ttu-id="e865e-107">Si vous disposez de privilèges d’administrateur sur le client App-V exécutant WindowsXP, ouvrez le panneau de configuration des **comptes d’utilisateurs** (panneau de configuration classique).</span><span class="sxs-lookup"><span data-stu-id="e865e-107">With administrator privileges on the App-V Client running WindowsXP, open the **User Accounts** control panel (Classic Control Panel).</span></span>

2.  <span data-ttu-id="e865e-108">Cliquez sur l' **onglet Avancé**, puis sélectionnez **gérer les mots de passe**.</span><span class="sxs-lookup"><span data-stu-id="e865e-108">Click the **Advanced Tab**, and select **Manage Passwords**.</span></span>

3.  <span data-ttu-id="e865e-109">Dans l’écran **noms d’utilisateur et mots de passe enregistrés** , cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="e865e-109">On the **Stored User Names and Passwords** screen, click **Add**.</span></span>

4.  <span data-ttu-id="e865e-110">Dans l’écran de **Propriétés informations de connexion** , renseignez les champs suivants avec les informations de l’infrastructure App-V:</span><span class="sxs-lookup"><span data-stu-id="e865e-110">On the **Logon Information Properties** screen, fill out the following fields with information from the App-V infrastructure:</span></span>

    1.  <span data-ttu-id="e865e-111">**Serveur:** Nom du nom externe du serveur de publication.</span><span class="sxs-lookup"><span data-stu-id="e865e-111">**Server:** Name of publishing server external name.</span></span>

    2.  <span data-ttu-id="e865e-112">**Nom d’utilisateur:** Nom d’utilisateur de l’utilisateur externe sous la forme Domain\\username.</span><span class="sxs-lookup"><span data-stu-id="e865e-112">**User name:** User name for external user in the form Domain\\username.</span></span>

    3.  <span data-ttu-id="e865e-113">**Mot de passe:** Mot de passe du compte d’utilisateur entré dans le champ **nom d’utilisateur** .</span><span class="sxs-lookup"><span data-stu-id="e865e-113">**Password:** Password for the user account entered in the **User name** field.</span></span>

5.  <span data-ttu-id="e865e-114">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="e865e-114">Click **OK**.</span></span> <span data-ttu-id="e865e-115">Les informations d’identification seront stockées sur le client.</span><span class="sxs-lookup"><span data-stu-id="e865e-115">The credentials will be stored on the client.</span></span>

## <span data-ttu-id="e865e-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e865e-116">Related topics</span></span>


[<span data-ttu-id="e865e-117">Clients joints au domaine et non joints au domaine</span><span class="sxs-lookup"><span data-stu-id="e865e-117">Domain-Joined and Non-Domain-Joined Clients</span></span>](domain-joined-and-non-domain-joined-clients.md)

[<span data-ttu-id="e865e-118">Comment affecter les informations d’identification appropriées pour Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e865e-118">How to Assign the Proper Credentials for Windows Vista</span></span>](how-to-assign--the-proper-credentials-for-windows-vista.md)

 

 





