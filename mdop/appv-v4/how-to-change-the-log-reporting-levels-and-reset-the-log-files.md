---
title: Procédure pour modifier les niveaux de création de rapport de suivi et réinitialiser les fichiers journaux
description: Procédure pour modifier les niveaux de création de rapport de suivi et réinitialiser les fichiers journaux
author: dansimp
ms.assetid: 9561d6fb-b35c-491b-a355-000064583194
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7307dee0030d9c03a8107d9d0ceef2086a94df07
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807350"
---
# <span data-ttu-id="52dce-103">Procédure pour modifier les niveaux de création de rapport de suivi et réinitialiser les fichiers journaux</span><span class="sxs-lookup"><span data-stu-id="52dce-103">How to Change the Log Reporting Levels and Reset the Log Files</span></span>


<span data-ttu-id="52dce-104">Vous pouvez utiliser la procédure suivante pour modifier le niveau de rapport du journal à partir du nœud **virtualisation** des applications de la console de gestion des applications.</span><span class="sxs-lookup"><span data-stu-id="52dce-104">You can use the following procedure to change the log reporting level from the **Application Virtualization** node in the Application Virtualization Management Console.</span></span> <span data-ttu-id="52dce-105">Lorsque le fichier journal atteint la taille maximale (la valeur par défaut est 256 Mo), une réinitialisation est imposée lors de l’écriture suivante du journal.</span><span class="sxs-lookup"><span data-stu-id="52dce-105">When the log file reaches the maximum size (default is 256 MB), a reset is forced when the next write to the log occurs.</span></span> <span data-ttu-id="52dce-106">Une réinitialisation entraîne la création d’un nouveau fichier journal et l’ancien fichier est renommé comme sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="52dce-106">A reset causes a new log file to be created, and the old file is renamed as a backup.</span></span>

**<span data-ttu-id="52dce-107">Pour modifier le niveau de rapport du journal</span><span class="sxs-lookup"><span data-stu-id="52dce-107">To change the log reporting level</span></span>**

1.  <span data-ttu-id="52dce-108">Cliquez avec le bouton droit sur le nœud **Application Virtualization** , puis sélectionnez **Propriétés** dans le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="52dce-108">Right-click the **Application Virtualization** node, and select **Properties** from the pop-up menu.</span></span>

2.  <span data-ttu-id="52dce-109">Dans l’onglet **général** de la boîte de dialogue **Propriétés** , dans la liste déroulante **niveau du journal** , sélectionnez le niveau de journal souhaité.</span><span class="sxs-lookup"><span data-stu-id="52dce-109">On the **General** tab in the **Properties** dialog box, from the **Log Level** drop-down list, select the desired log level.</span></span>

    <span data-ttu-id="52dce-110">**Remarques**  Si vous choisissez l’affichage **détaillé** comme niveau de journalisation, les fichiers journaux seront considérablement volumineux.</span><span class="sxs-lookup"><span data-stu-id="52dce-110">**Note** If you choose **Verbose** as the logging level, the log files will grow large very quickly.</span></span> <span data-ttu-id="52dce-111">Comme cela peut inhiber les performances du client, il est recommandé d’utiliser ce niveau de journal uniquement pour diagnostiquer des problèmes spécifiques.</span><span class="sxs-lookup"><span data-stu-id="52dce-111">This might inhibit client performance, so best practice is to use this log level only for diagnosing specific problems.</span></span>

     

3.  <span data-ttu-id="52dce-112">Dans l’onglet **général** de la boîte de dialogue **Propriétés** , dans la liste déroulante **niveau du journal système** , sélectionnez le niveau de journal souhaité.</span><span class="sxs-lookup"><span data-stu-id="52dce-112">On the **General** tab in the **Properties** dialog box, from the **System Log Level** drop-down list, select the desired log level.</span></span>

    <span data-ttu-id="52dce-113">**Remarques**  Le paramètre **niveau du journal système** contrôle le niveau de messages envoyés au journal des événements système.</span><span class="sxs-lookup"><span data-stu-id="52dce-113">**Note** The **System Log Level** setting controls the level of messages sent to the system event log.</span></span> <span data-ttu-id="52dce-114">Les messages enregistrés sont identiques à ceux qui sont enregistrés dans le journal des événements du client, mais qui sont stockés à un autre emplacement.</span><span class="sxs-lookup"><span data-stu-id="52dce-114">The logged messages are identical to the messages that get logged to the client event log, but they are stored in a different location.</span></span>

     

4.  <span data-ttu-id="52dce-115">Cliquez sur **OK** ou sur **appliquer** pour modifier le paramètre.</span><span class="sxs-lookup"><span data-stu-id="52dce-115">Click **OK** or **Apply** to change the setting.</span></span>

**<span data-ttu-id="52dce-116">Pour réinitialiser le fichier journal</span><span class="sxs-lookup"><span data-stu-id="52dce-116">To reset the log file</span></span>**

1.  <span data-ttu-id="52dce-117">Cliquez avec le bouton droit sur le nœud **Application Virtualization** , puis sélectionnez **Propriétés** dans le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="52dce-117">Right-click the **Application Virtualization** node, and select **Properties** from the pop-up menu.</span></span>

2.  <span data-ttu-id="52dce-118">Dans l’onglet **général** de la boîte de dialogue **Propriétés** , cliquez sur **Réinitialiser le journal** pour sauvegarder le fichier journal actuel et commencer immédiatement un nouveau fichier journal.</span><span class="sxs-lookup"><span data-stu-id="52dce-118">On the **General** tab in the **Properties** dialog box, click **Reset Log** to back up the current log file and immediately start a new log file.</span></span> <span data-ttu-id="52dce-119">Les fichiers journaux de sauvegarde sont stockés dans le même dossier.</span><span class="sxs-lookup"><span data-stu-id="52dce-119">The backup log files are stored in the same folder.</span></span>

3.  <span data-ttu-id="52dce-120">Cliquez sur **OK** ou sur **appliquer** pour modifier le paramètre.</span><span class="sxs-lookup"><span data-stu-id="52dce-120">Click **OK** or **Apply** to change the setting.</span></span>

## <span data-ttu-id="52dce-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="52dce-121">Related topics</span></span>


[<span data-ttu-id="52dce-122">Procédure pour configurer le client dans Application Virtualization Client Management Console</span><span class="sxs-lookup"><span data-stu-id="52dce-122">How to Configure the Client in the Application Virtualization Client Management Console</span></span>](how-to-configure-the-client-in-the-application-virtualization-client-management-console.md)

[<span data-ttu-id="52dce-123">Autorisations d'accès utilisateur dans Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="52dce-123">User Access Permissions in Application Virtualization Client</span></span>](user-access-permissions-in-application-virtualization-client.md)

 

 





