---
title: Procédure pour configurer une actualisation de publication périodique
description: Procédure pour configurer une actualisation de publication périodique
author: dansimp
ms.assetid: c358c765-cb88-4881-b4e7-0a2e87304870
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a5bbea1c661d6cb5a78f0bb9de29538e0222cda6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806753"
---
# <span data-ttu-id="f692a-103">Procédure pour configurer une actualisation de publication périodique</span><span class="sxs-lookup"><span data-stu-id="f692a-103">How to Set Up Periodic Publishing Refresh</span></span>


<span data-ttu-id="f692a-104">Vous pouvez utiliser la procédure suivante pour configurer le client de manière à actualiser régulièrement les informations de publication des serveurs App-V.</span><span class="sxs-lookup"><span data-stu-id="f692a-104">You can use the following procedure to configure the client to periodically refresh the publishing information from the App-V servers.</span></span> <span data-ttu-id="f692a-105">Une fois le client configuré, l’opération d’actualisation est automatique.</span><span class="sxs-lookup"><span data-stu-id="f692a-105">After the client is configured, the refresh operation is automatic.</span></span> <span data-ttu-id="f692a-106">Ces paramètres configurent les paramètres par défaut pour le client de sorte que tous les utilisateurs de cet ordinateur puissent voir les mêmes paramètres.</span><span class="sxs-lookup"><span data-stu-id="f692a-106">These settings configure the default settings for the client so that all users on this computer will see the same settings.</span></span>

<span data-ttu-id="f692a-107">**Remarques**  Après avoir effectué cette procédure, les informations de publication sont actualisées conformément aux nouveaux paramètres après la première actualisation à la connexion.</span><span class="sxs-lookup"><span data-stu-id="f692a-107">**Note** After you have performed this procedure, the publishing information will be refreshed according to the new settings after the first refresh at login.</span></span> <span data-ttu-id="f692a-108">Lors de la première actualisation, le serveur peut remplacer les paramètres de l’ordinateur par d’autres paramètres, selon la manière dont il est configuré.</span><span class="sxs-lookup"><span data-stu-id="f692a-108">When this first refresh occurs, the server might override the computer settings with different settings, depending on how it is configured.</span></span> <span data-ttu-id="f692a-109">L’onglet **Actualiser** de la boîte de dialogue **Propriétés** affiche les paramètres de l’ordinateur client configurés en local ainsi que les paramètres susceptibles d’avoir été configurés pour l’utilisateur par le serveur de publication.</span><span class="sxs-lookup"><span data-stu-id="f692a-109">The **Refresh** tab in the **Properties** dialog box shows the locally configured client computer settings and any settings that might have been configured for the user by the publishing server.</span></span>

 

**<span data-ttu-id="f692a-110">Pour actualiser régulièrement les informations de publication des serveurs de virtualisation des applications</span><span class="sxs-lookup"><span data-stu-id="f692a-110">To periodically refresh the publishing information from the Application Virtualization Servers</span></span>**

1.  <span data-ttu-id="f692a-111">Cliquez sur **serveurs de publication** dans le volet de l' **étendue** .</span><span class="sxs-lookup"><span data-stu-id="f692a-111">Click **Publishing Servers** in the **Scope** pane.</span></span>

2.  <span data-ttu-id="f692a-112">Dans le volet **résultats** , cliquez avec le bouton droit sur le serveur de votre choix, puis sélectionnez **Propriétés** dans le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="f692a-112">In the **Results** pane, right-click the desired server and select **Properties** from the pop-up-menu.</span></span>

3.  <span data-ttu-id="f692a-113">Dans la boîte de dialogue **Propriétés** , sous l’onglet **Actualiser** , activez la case à cocher **Actualiser la configuration chaque fois** et entrez un nombre qui représente la fréquence dans le champ.</span><span class="sxs-lookup"><span data-stu-id="f692a-113">In the **Properties** dialog box, on the **Refresh** tab, select the **Refresh configuration every** check box and enter a number that represents the frequency in the field.</span></span> <span data-ttu-id="f692a-114">Dans le menu déroulant, sélectionnez **minutes**, **heures**et **jours** .</span><span class="sxs-lookup"><span data-stu-id="f692a-114">Then select **Minutes**, **Hours**, **Days** from the drop-down menu.</span></span>

    <span data-ttu-id="f692a-115">**Remarques**  Ce paramètre force le client à actualiser les informations de publication chaque fois que la période configurée est écoulée.</span><span class="sxs-lookup"><span data-stu-id="f692a-115">**Note** This setting will cause the client to refresh publishing information every time the configured period elapses.</span></span> <span data-ttu-id="f692a-116">Si l’utilisateur n’est pas connecté quand il est temps de procéder à une actualisation, l’actualisation intervient lors de la prochaine connexion de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f692a-116">If the user is not logged in when it's time to do a refresh, the refresh will take place when the user next logs in.</span></span> <span data-ttu-id="f692a-117">Le minuteur est alors redémarré pour la période suivante.</span><span class="sxs-lookup"><span data-stu-id="f692a-117">The timer is then started again for the next period.</span></span>

     

4.  <span data-ttu-id="f692a-118">Cliquez sur **appliquer** pour modifier la configuration.</span><span class="sxs-lookup"><span data-stu-id="f692a-118">Click **Apply** to change the configuration.</span></span>

5.  <span data-ttu-id="f692a-119">Lorsque vous avez terminé de configurer le serveur, cliquez sur **OK** pour quitter la boîte de dialogue et revenir à la console de gestion des clients Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="f692a-119">When you finish configuring the server, click **OK** to exit the dialog box and return to the Application Virtualization Client Management Console.</span></span>

## <span data-ttu-id="f692a-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f692a-120">Related topics</span></span>


[<span data-ttu-id="f692a-121">Procédure pour configurer le client dans Application Virtualization Client Management Console</span><span class="sxs-lookup"><span data-stu-id="f692a-121">How to Configure the Client in the Application Virtualization Client Management Console</span></span>](how-to-configure-the-client-in-the-application-virtualization-client-management-console.md)

 

 





