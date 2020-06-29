---
title: Procédure pour désinstaller App-V Client
description: Procédure pour désinstaller App-V Client
author: dansimp
ms.assetid: 07591270-9651-4bb5-a5b3-e0fc009bd9e2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: acb3f53b42027ff2c1b84fd2ab2bdde3c52f96de
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806741"
---
# <span data-ttu-id="b43c6-103">Procédure pour désinstaller App-V Client</span><span class="sxs-lookup"><span data-stu-id="b43c6-103">How to Uninstall the App-V Client</span></span>


<span data-ttu-id="b43c6-104">Suivez la procédure ci-dessous pour désinstaller le client de virtualisation des applications de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="b43c6-104">Use the following procedure to uninstall the Application Virtualization Client from the computer.</span></span>

**<span data-ttu-id="b43c6-105">Pour désinstaller le client de bureau de virtualisation des applications</span><span class="sxs-lookup"><span data-stu-id="b43c6-105">To uninstall the Application Virtualization Desktop Client</span></span>**

1.  <span data-ttu-id="b43c6-106">Dans le panneau de configuration, double-cliquez sur **Ajout/suppression de programmes** (ou dans Windows Vista, **programmes et fonctionnalités**), puis double-cliquez sur **client de bureau Microsoft Application Virtualization**.</span><span class="sxs-lookup"><span data-stu-id="b43c6-106">In Control Panel, double-click **Add or Remove Programs** (or in Windows Vista, **Programs and Features**), and then double-click **Microsoft Application Virtualization Desktop Client**.</span></span>

2.  <span data-ttu-id="b43c6-107">Dans la boîte de dialogue qui s’affiche, cliquez sur **Oui** pour continuer le processus de désinstallation.</span><span class="sxs-lookup"><span data-stu-id="b43c6-107">In the dialog box that appears, click **Yes** to continue with the uninstall process.</span></span>

    <span data-ttu-id="b43c6-108">**Important**  Le processus de désinstallation ne peut pas être annulé ou interrompu.</span><span class="sxs-lookup"><span data-stu-id="b43c6-108">**Important** The uninstall process cannot be canceled or interrupted.</span></span>

     

3.  <span data-ttu-id="b43c6-109">Lorsqu’un message vous signale que l’application de barre des tâches du client de virtualisation des applications Microsoft doit être fermée, cliquez avec le bouton droit sur l’icône App-V dans la zone de notification et sélectionnez **quitter** pour fermer l’application.</span><span class="sxs-lookup"><span data-stu-id="b43c6-109">When a message stating that the Microsoft Application Virtualization Client Tray application must be closed before continuing appears, right-click the App-V icon in the notification area and select **Exit** to close the application.</span></span> <span data-ttu-id="b43c6-110">Cliquez ensuite sur **Réessayer** pour continuer le processus de désinstallation.</span><span class="sxs-lookup"><span data-stu-id="b43c6-110">Then click **Retry** to continue with the uninstall process.</span></span>

    <span data-ttu-id="b43c6-111">**Important**  Vous pouvez voir un message indiquant qu’une ou plusieurs applications virtuelles sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="b43c6-111">**Important** You might see a message stating that one or more virtual applications are in use.</span></span> <span data-ttu-id="b43c6-112">Fermez toutes les applications ouvertes et enregistrez vos données avant de continuer.</span><span class="sxs-lookup"><span data-stu-id="b43c6-112">Close any open applications and save your data before you continue.</span></span> <span data-ttu-id="b43c6-113">Cliquez sur **OK** pour continuer le processus de désinstallation.</span><span class="sxs-lookup"><span data-stu-id="b43c6-113">Then click **OK** to continue with the uninstall process.</span></span>

     

4.  <span data-ttu-id="b43c6-114">Une barre de progression indique le temps restant.</span><span class="sxs-lookup"><span data-stu-id="b43c6-114">A progress bar shows the time remaining.</span></span> <span data-ttu-id="b43c6-115">Lorsque cette étape est terminée, vous devez redémarrer l’ordinateur de manière à ce que tous les pilotes associés puissent être arrêtés pour achever le processus de désinstallation.</span><span class="sxs-lookup"><span data-stu-id="b43c6-115">When this step finishes, you must restart the computer so that all associated drivers can be stopped to complete the uninstall process.</span></span>

    <span data-ttu-id="b43c6-116">**Remarques**  Les clés de Registre suivantes demeurent après la fin du processus de désinstallation:</span><span class="sxs-lookup"><span data-stu-id="b43c6-116">**Note** The following registry keys remain after the uninstall process is complete:</span></span>

    -   <span data-ttu-id="b43c6-117">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid</span><span class="sxs-lookup"><span data-stu-id="b43c6-117">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid</span></span>

    -   <span data-ttu-id="b43c6-118">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5</span><span class="sxs-lookup"><span data-stu-id="b43c6-118">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5</span></span>

    -   <span data-ttu-id="b43c6-119">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\SystemGuard "client" = dword: 00000000</span><span class="sxs-lookup"><span data-stu-id="b43c6-119">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\SystemGuard"Client"=dword:00000000</span></span>

    -   <span data-ttu-id="b43c6-120">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\SystemGuard\\SecKey</span><span class="sxs-lookup"><span data-stu-id="b43c6-120">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\SystemGuard\\SecKey</span></span>

     

## <span data-ttu-id="b43c6-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b43c6-121">Related topics</span></span>


[<span data-ttu-id="b43c6-122">Procédure pour installer le client via la ligne de commande</span><span class="sxs-lookup"><span data-stu-id="b43c6-122">How to Install the Client by Using the Command Line</span></span>](how-to-install-the-client-by-using-the-command-line-new.md)

[<span data-ttu-id="b43c6-123">Procédure pour installer manuellement Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="b43c6-123">How to Manually Install the Application Virtualization Client</span></span>](how-to-manually-install-the-application-virtualization-client.md)

[<span data-ttu-id="b43c6-124">Procédure pour publier une application virtuelle sur le client</span><span class="sxs-lookup"><span data-stu-id="b43c6-124">How to Publish a Virtual Application on the Client</span></span>](how-to-publish-a-virtual-application-on-the-client.md)

 

 





