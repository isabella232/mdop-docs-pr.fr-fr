---
title: Procédure pour configurer des serveurs de publication
description: Procédure pour configurer des serveurs de publication
author: dansimp
ms.assetid: 2111f079-c202-4c49-b2a6-f4237068b2dc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2f060d862fd1449f5240ad495b53a1fa4e97697f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806742"
---
# <span data-ttu-id="c0fc8-103">Procédure pour configurer des serveurs de publication</span><span class="sxs-lookup"><span data-stu-id="c0fc8-103">How to Set Up Publishing Servers</span></span>


<span data-ttu-id="c0fc8-104">Vous pouvez utiliser les procédures suivantes pour ajouter et configurer des serveurs de virtualisation d’application directement à partir de la console de gestion des clients.</span><span class="sxs-lookup"><span data-stu-id="c0fc8-104">You can use the following procedures to add and configure Application Virtualization Servers directly from the Client Management Console.</span></span>

**<span data-ttu-id="c0fc8-105">Pour ajouter un serveur de publication d’applications</span><span class="sxs-lookup"><span data-stu-id="c0fc8-105">To add an application publishing server</span></span>**

1.  <span data-ttu-id="c0fc8-106">Dans le volet **résultats** , cliquez avec le bouton droit et sélectionnez **nouveau serveur** dans le menu contextuel pour démarrer l’Assistant Nouveau serveur d’applications de virtualisation ou cliquez avec le bouton droit sur le nœud du **serveur de publication** et sélectionnez **nouveau serveur** dans le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="c0fc8-106">In the **Results** pane, right-click and select **New Server** from the pop-up-menu to start the New Application Virtualization Server Wizard, or alternatively, right-click the **Publishing Server** node and select **New Server** from the pop-up-menu.</span></span>

2.  <span data-ttu-id="c0fc8-107">Dans la page de l’Assistant, entrez le nom du serveur dans le champ **nom d’affichage** , puis sélectionnez le type de serveur dans la liste déroulante **type** .</span><span class="sxs-lookup"><span data-stu-id="c0fc8-107">On page one of the wizard, enter the name of the server in the **Display Name** field and select the server type from the **Type** drop-down list.</span></span> <span data-ttu-id="c0fc8-108">Dans la liste déroulante des types de serveurs, vous pouvez choisir **serveur de virtualisation des applications**, serveur de virtualisation des applications de **sécurité améliorée**, serveur **http standard**ou **serveur http de sécurité améliorée** .</span><span class="sxs-lookup"><span data-stu-id="c0fc8-108">You can choose **Application Virtualization Server**, **Enhanced Security Application Virtualization Server**, **Standard HTTP Server**, or **Enhanced Security HTTP Server** from the drop-down list of server types.</span></span>

3.  <span data-ttu-id="c0fc8-109">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="c0fc8-109">Click **Next**.</span></span>

4.  <span data-ttu-id="c0fc8-110">Dans la page 2 de l’Assistant, tapez les informations appropriées dans les champs **nom d’hôte** et **port** .</span><span class="sxs-lookup"><span data-stu-id="c0fc8-110">On page two of the wizard, type the appropriate information into the **Host Name** and **Port** fields.</span></span> <span data-ttu-id="c0fc8-111">Le champ **path** ne peut pas être modifié pour les serveurs de virtualisation des applications.</span><span class="sxs-lookup"><span data-stu-id="c0fc8-111">The **Path** field is not editable for Application Virtualization Servers.</span></span> <span data-ttu-id="c0fc8-112">Entrez le chemin d’accès du serveur HTTP standard ou du serveur HTTP de sécurité améliorée.</span><span class="sxs-lookup"><span data-stu-id="c0fc8-112">You must enter a path for Standard HTTP Server or Enhanced Security HTTP Server.</span></span>

5.  <span data-ttu-id="c0fc8-113">Cliquez sur **Terminer** pour ajouter le serveur.</span><span class="sxs-lookup"><span data-stu-id="c0fc8-113">Click **Finish** to add the server.</span></span>

**<span data-ttu-id="c0fc8-114">Pour configurer un serveur de publication d’application</span><span class="sxs-lookup"><span data-stu-id="c0fc8-114">To set up an application publishing server</span></span>**

1.  <span data-ttu-id="c0fc8-115">Dans le volet **résultats** , cliquez avec le bouton droit sur le serveur de votre choix, puis sélectionnez **Propriétés** dans le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="c0fc8-115">In the **Results** pane, right-click the desired server and select **Properties** from the pop-up menu.</span></span>

2.  <span data-ttu-id="c0fc8-116">Cliquez sur l’onglet **général** , dans lequel vous pouvez modifier le nom du serveur, sélectionnez un type dans la liste déroulante des types de serveurs, puis spécifiez le nom d’hôte et le port.</span><span class="sxs-lookup"><span data-stu-id="c0fc8-116">Click the **General** tab, where you can change the server name, select a type from the drop-down list of server types, and specify the host name and port.</span></span> <span data-ttu-id="c0fc8-117">Lorsque le type du serveur est standard HTTP Server ou serveur HTTP de sécurité améliorée, le champ **path** peut également être modifié.</span><span class="sxs-lookup"><span data-stu-id="c0fc8-117">When the server type is Standard HTTP Server or Enhanced Security HTTP Server, the **Path** field is also editable.</span></span>

3.  <span data-ttu-id="c0fc8-118">Cliquez sur l’onglet **Actualiser** , dans lequel la case à cocher **Actualiser la publication sur l’utilisateur** est activée par défaut.</span><span class="sxs-lookup"><span data-stu-id="c0fc8-118">Click the **Refresh** tab, where the **Refresh publishing on user login** check box is selected by default.</span></span> <span data-ttu-id="c0fc8-119">Pour modifier la fréquence d’actualisation, activez la case à cocher **Actualiser la publication chaque fois** et entrez un nombre qui représente la fréquence dans le champ.</span><span class="sxs-lookup"><span data-stu-id="c0fc8-119">To change the refresh rate, select the **Refresh publishing every** check box and enter a number that represents the frequency in the field.</span></span> <span data-ttu-id="c0fc8-120">Dans le menu déroulant, sélectionnez **minutes**, **heures**et **jours** .</span><span class="sxs-lookup"><span data-stu-id="c0fc8-120">Then select **Minutes**, **Hours**, **Days** from the drop-down menu.</span></span> <span data-ttu-id="c0fc8-121">(La durée minimum que vous pouvez entrer est de 30 minutes.)</span><span class="sxs-lookup"><span data-stu-id="c0fc8-121">(The minimum amount of time you can enter is 30 minutes.)</span></span>

4.  <span data-ttu-id="c0fc8-122">Cliquez sur **appliquer** pour modifier la configuration.</span><span class="sxs-lookup"><span data-stu-id="c0fc8-122">Click **Apply** to change the configuration.</span></span>

5.  <span data-ttu-id="c0fc8-123">Lorsque vous avez terminé la publication, cliquez sur **OK** pour quitter la boîte de dialogue et revenir à la console de gestion des clients.</span><span class="sxs-lookup"><span data-stu-id="c0fc8-123">When you are finished publishing, click **OK** to exit the dialog box and return to the Client Management Console.</span></span>

## <span data-ttu-id="c0fc8-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c0fc8-124">Related topics</span></span>


[<span data-ttu-id="c0fc8-125">Procédure pour désactiver ou modifier des paramètres de mode de fonctionnement déconnecté</span><span class="sxs-lookup"><span data-stu-id="c0fc8-125">How to Disable or Modify Disconnected Operation Mode Settings</span></span>](how-to-disable-or-modify-disconnected-operation-mode-settings.md)

 

 





