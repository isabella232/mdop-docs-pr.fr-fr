---
title: Procédure pour modifier la taille de mémoire cache du serveur
description: Procédure pour modifier la taille de mémoire cache du serveur
author: dansimp
ms.assetid: 24e63744-21c3-458e-b137-9592f4fe785c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 92e56a8a28f7a00d71805b497f9e404cca65919d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807342"
---
# <span data-ttu-id="c65a8-103">Procédure pour modifier la taille de mémoire cache du serveur</span><span class="sxs-lookup"><span data-stu-id="c65a8-103">How to Change the Server Cache Size</span></span>


<span data-ttu-id="c65a8-104">Vous pouvez utiliser la procédure suivante pour modifier la taille de cache pour n’importe quel serveur directement à partir de la console de gestion du serveur d’applications.</span><span class="sxs-lookup"><span data-stu-id="c65a8-104">You can use the following procedure to change the cache size for any server directly from the Application Virtualization Server Management Console.</span></span>

<span data-ttu-id="c65a8-105">**Remarques**  Même si vous pouvez modifier la taille du cache, à moins que votre configuration n’exige d’en modifier la taille, il est recommandé de conserver les valeurs par défaut définies sur taille du cache.</span><span class="sxs-lookup"><span data-stu-id="c65a8-105">**Note** Although you can change the cache size, unless your configuration specifically requires you to change the size, it is recommended that you leave the cache size set to the default values.</span></span>

 

**<span data-ttu-id="c65a8-106">Pour modifier la taille du cache du serveur</span><span class="sxs-lookup"><span data-stu-id="c65a8-106">To change the server cache size</span></span>**

1.  <span data-ttu-id="c65a8-107">Cliquez sur le nœud **groupes de serveurs** dans le volet gauche pour développer la liste des groupes de serveurs.</span><span class="sxs-lookup"><span data-stu-id="c65a8-107">Click the **Server Groups** node in the left pane to expand the list of server groups.</span></span>

2.  <span data-ttu-id="c65a8-108">Dans le volet **résultats** , double-cliquez sur le groupe de serveurs souhaité pour afficher la liste des serveurs du groupe.</span><span class="sxs-lookup"><span data-stu-id="c65a8-108">In the **Results** pane, double-click the desired server group to display the list of servers in the group.</span></span>

3.  <span data-ttu-id="c65a8-109">Dans le volet **résultats** , cliquez avec le bouton droit sur le serveur de votre choix, puis sélectionnez **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="c65a8-109">In the **Results** pane, right-click the desired server and select **Properties**.</span></span>

4.  <span data-ttu-id="c65a8-110">Sélectionnez l’onglet **avancé** .</span><span class="sxs-lookup"><span data-stu-id="c65a8-110">Select the **Advanced** tab.</span></span>

5.  <span data-ttu-id="c65a8-111">Entrez une valeur dans le champ **allocation de mémoire maximale** pour le cache du serveur, puis entrez une valeur pour le niveau d’avertissement de seuil dans le champ d’avertissement d' **allocation de mémoire** .</span><span class="sxs-lookup"><span data-stu-id="c65a8-111">Enter a value in the **Maximum Memory Allocation** field for the server cache, and enter a value for the threshold warning level in the **Warn Memory Allocation** field.</span></span>

6.  <span data-ttu-id="c65a8-112">Entrez une valeur dans le champ **taille de bloc maximale** .</span><span class="sxs-lookup"><span data-stu-id="c65a8-112">Enter a value in the **Maximum Block Size** field.</span></span> <span data-ttu-id="c65a8-113">Ce nombre doit être supérieur ou égal à la taille de blocs maximale du paquetage le plus grand qui sera transmis à partir du serveur.</span><span class="sxs-lookup"><span data-stu-id="c65a8-113">This number must be greater than or equal to the maximum block size of the largest package that will be streamed from the server.</span></span>

7.  <span data-ttu-id="c65a8-114">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="c65a8-114">Click **OK**.</span></span>

## <span data-ttu-id="c65a8-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c65a8-115">Related topics</span></span>


[<span data-ttu-id="c65a8-116">Procédure pour modifier le port du serveur</span><span class="sxs-lookup"><span data-stu-id="c65a8-116">How to Change the Server Port</span></span>](how-to-change-the-server-port.md)

[<span data-ttu-id="c65a8-117">Procédure pour gérer les serveurs dans Server Management Console</span><span class="sxs-lookup"><span data-stu-id="c65a8-117">How to Manage Servers in the Server Management Console</span></span>](how-to-manage-servers-in-the-server-management-console.md)

 

 





