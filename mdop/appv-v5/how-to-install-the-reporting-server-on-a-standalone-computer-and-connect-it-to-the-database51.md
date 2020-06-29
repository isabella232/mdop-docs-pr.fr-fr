---
title: Comment installer le serveur de rapports sur un ordinateur autonome et le connecter à la base de données
description: Comment installer le serveur de rapports sur un ordinateur autonome et le connecter à la base de données
author: dansimp
ms.assetid: 11f07750-4045-4c8d-a583-7d70c9e9aa7b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 67866714ff6ae60097d9b368fd0eaf361b08eec6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805377"
---
# <span data-ttu-id="269c8-103">Comment installer le serveur de rapports sur un ordinateur autonome et le connecter à la base de données</span><span class="sxs-lookup"><span data-stu-id="269c8-103">How to install the Reporting Server on a Standalone Computer and Connect it to the Database</span></span>

<span data-ttu-id="269c8-104">Utilisez la procédure suivante pour installer le serveur de création de rapports sur un ordinateur autonome et le connecter à la base de données.</span><span class="sxs-lookup"><span data-stu-id="269c8-104">Use the following procedure to install the reporting server on a standalone computer and connect it to the database.</span></span>

<span data-ttu-id="269c8-105">**Important** Avant d’exécuter la procédure suivante, vous devez lire et comprendre [à propos de la création de rapports App-V 5,1](about-app-v-51-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="269c8-105">**Important** Before performing the following procedure you should read and understand [About App-V 5.1 Reporting](about-app-v-51-reporting.md).</span></span>

## <span data-ttu-id="269c8-106">Pour installer le serveur de création de rapports sur un ordinateur autonome et le connecter à la base de données</span><span class="sxs-lookup"><span data-stu-id="269c8-106">To install the reporting server on a standalone computer and connect it to the database</span></span>

1. <span data-ttu-id="269c8-107">Copiez les fichiers d’installation de App-V 5,1 Server sur l’ordinateur sur lequel vous voulez procéder à l’installation.</span><span class="sxs-lookup"><span data-stu-id="269c8-107">Copy the App-V 5.1 server installation files to the computer on which you want to install it on.</span></span> <span data-ttu-id="269c8-108">Pour démarrer l’installation de l’application-V 5,1 Server, cliquez avec le bouton droit et exécutez **appv\_server\_setup.exe** en tant qu’administrateur.</span><span class="sxs-lookup"><span data-stu-id="269c8-108">To start the App-V 5.1 server installation right-click and run **appv\_server\_setup.exe** as an administrator.</span></span> <span data-ttu-id="269c8-109">Cliquez sur **Installer**.</span><span class="sxs-lookup"><span data-stu-id="269c8-109">Click **Install**.</span></span>

2. <span data-ttu-id="269c8-110">Sur la page **mise en route** , consultez et acceptez les termes du contrat de licence, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="269c8-110">On the **Getting Started** page, review and accept the license terms, and click **Next**.</span></span>

3. <span data-ttu-id="269c8-111">Sur la page **utiliser Microsoft Update pour garantir la sécurité et** la mise à jour de votre ordinateur, vous pouvez activer les mises à jour Microsoft en sélectionnant **utiliser Microsoft Update lorsque je recherche les mises à jour (recommandé).**</span><span class="sxs-lookup"><span data-stu-id="269c8-111">On the **Use Microsoft Update to help keep your computer secure and up-to-date** page, to enable Microsoft updates, select **Use Microsoft Update when I check for updates (recommended).**</span></span> <span data-ttu-id="269c8-112">Pour désactiver les mises à jour Microsoft, sélectionnez **je ne veux pas utiliser Microsoft Update**.</span><span class="sxs-lookup"><span data-stu-id="269c8-112">To disable Microsoft updates, select **I don't want to use Microsoft Update**.</span></span> <span data-ttu-id="269c8-113">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="269c8-113">Click **Next**.</span></span>

4. <span data-ttu-id="269c8-114">Dans la page de **sélection des fonctionnalités** , activez la case à cocher serveur de **création de rapports** , puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="269c8-114">On the **Feature Selection** page, select the **Reporting Server** checkbox and click **Next**.</span></span>

5. <span data-ttu-id="269c8-115">Dans la page **emplacement d’installation** , acceptez l’emplacement par défaut, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="269c8-115">On the **Installation Location** page, accept the default location and click **Next**.</span></span>

6. <span data-ttu-id="269c8-116">Dans la page **configurer la base de données de création de rapports existants** , sélectionnez **utiliser un serveur SQL distant**, puis tapez le nom de l’ordinateur exécutant Microsoft SQL Server, par exemple **SqlServerMachine**.</span><span class="sxs-lookup"><span data-stu-id="269c8-116">On the **Configure Existing Reporting Database** page, select **Use a remote SQL Server**, and type the machine name of the computer running Microsoft SQL Server, for example **SqlServerMachine**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="269c8-117">Si Microsoft SQL Server est déployé sur le même serveur, sélectionnez **use local SQL Server**.</span><span class="sxs-lookup"><span data-stu-id="269c8-117">If the Microsoft SQL Server is deployed on the same server, select **Use local SQL Server**.</span></span>

    <span data-ttu-id="269c8-118">Pour l’instance SQL Server, sélectionnez **utiliser l’instance par défaut**.</span><span class="sxs-lookup"><span data-stu-id="269c8-118">For the SQL Server Instance, select **Use the default instance**.</span></span> <span data-ttu-id="269c8-119">Si vous utilisez une instance de Microsoft SQL Server personnalisée, vous devez sélectionner **utiliser une instance personnalisée** , puis taper le nom de l’instance.</span><span class="sxs-lookup"><span data-stu-id="269c8-119">If you are using a custom Microsoft SQL Server instance, you must select **Use a custom instance** and then type the name of the instance.</span></span>

    <span data-ttu-id="269c8-120">Spécifiez le **nom de la base de données SQL Server** qu’utilisera ce serveur de création de rapports, par exemple, **AppvReporting**.</span><span class="sxs-lookup"><span data-stu-id="269c8-120">Specify the **SQL Server Database name** that this reporting server will use, for example **AppvReporting**.</span></span>

7. <span data-ttu-id="269c8-121">Dans la page **configuration du serveur de rapports** .</span><span class="sxs-lookup"><span data-stu-id="269c8-121">On the **Configure Reporting Server Configuration** page.</span></span>

   - <span data-ttu-id="269c8-122">Spécifiez le nom du site Web que vous voulez utiliser pour le service de création de rapports.</span><span class="sxs-lookup"><span data-stu-id="269c8-122">Specify the Website Name that you want to use for the Reporting Service.</span></span> <span data-ttu-id="269c8-123">Ne modifiez pas la valeur par défaut si vous n’avez pas de nom personnalisé.</span><span class="sxs-lookup"><span data-stu-id="269c8-123">Leave the default unchanged if you do not have a custom name.</span></span>

   - <span data-ttu-id="269c8-124">Pour la **liaison de port**, spécifiez un numéro de port unique qui sera utilisé par App-V 5,1, par exemple **55555**.</span><span class="sxs-lookup"><span data-stu-id="269c8-124">For the **Port binding**, specify a unique port number that will be used by App-V 5.1, for example **55555**.</span></span> <span data-ttu-id="269c8-125">Vous devez également vous assurer que le port spécifié n’est pas utilisé par un autre site Web.</span><span class="sxs-lookup"><span data-stu-id="269c8-125">You should also ensure that the port specified is not being used by another website.</span></span>

8. <span data-ttu-id="269c8-126">Cliquez sur **Installer**.</span><span class="sxs-lookup"><span data-stu-id="269c8-126">Click **Install**.</span></span>

**<span data-ttu-id="269c8-127">Vous avez un problème lié à l’application-V?</span><span class="sxs-lookup"><span data-stu-id="269c8-127">Got an App-V issue?</span></span>** <span data-ttu-id="269c8-128">Utilisez le [Forum TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="269c8-128">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="269c8-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="269c8-129">Related topics</span></span>

[<span data-ttu-id="269c8-130">À propos de la création de rapports d'App-V5.1</span><span class="sxs-lookup"><span data-stu-id="269c8-130">About App-V 5.1 Reporting</span></span>](about-app-v-51-reporting.md)

[<span data-ttu-id="269c8-131">Déploiement d'App-V5.1</span><span class="sxs-lookup"><span data-stu-id="269c8-131">Deploying App-V 5.1</span></span>](deploying-app-v-51.md)

[<span data-ttu-id="269c8-132">Activation de la création de rapports sur App-V5.1 Client à l'aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="269c8-132">How to Enable Reporting on the App-V 5.1 Client by Using PowerShell</span></span>](how-to-enable-reporting-on-the-app-v-51-client-by-using-powershell.md)
