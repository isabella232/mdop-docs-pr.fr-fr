---
title: Comment inscrire et désinscrire un serveur de publication à l’aide de la console de gestion
description: Comment inscrire et désinscrire un serveur de publication à l’aide de la console de gestion
author: dansimp
ms.assetid: c24f3b43-4888-41a9-9a39-973657f2b917
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5241af748029b7976c49b6474e5ef7c050699dd7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805221"
---
# <span data-ttu-id="81e1a-103">Comment inscrire et désinscrire un serveur de publication à l’aide de la console de gestion</span><span class="sxs-lookup"><span data-stu-id="81e1a-103">How to Register and Unregister a Publishing Server by Using the Management Console</span></span>


<span data-ttu-id="81e1a-104">Vous pouvez enregistrer et annuler l’enregistrement des serveurs de publication qui seront synchronisés avec le serveur de gestion App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="81e1a-104">You can register and unregister publishing servers that will synchronize with the App-V 5.0 management server.</span></span> <span data-ttu-id="81e1a-105">Vous pouvez également consulter la dernière tentative faite par le serveur de publication pour synchroniser les informations avec le serveur de gestion.</span><span class="sxs-lookup"><span data-stu-id="81e1a-105">You can also see the last attempt that the publishing server made to synchronize the information with the management server.</span></span>

<span data-ttu-id="81e1a-106">Utilisez la procédure suivante pour inscrire ou annuler l’inscription d’un serveur de publication.</span><span class="sxs-lookup"><span data-stu-id="81e1a-106">Use the following procedure to register or unregister a publishing server.</span></span>

**<span data-ttu-id="81e1a-107">Pour inscrire un serveur de publication à l’aide de la console de gestion</span><span class="sxs-lookup"><span data-stu-id="81e1a-107">To register a publishing server using the Management Console</span></span>**

1.  <span data-ttu-id="81e1a-108">Connectez-vous à la console de gestion et sélectionnez **serveurs**.</span><span class="sxs-lookup"><span data-stu-id="81e1a-108">Connect to the Management Console and select **Servers**.</span></span> <span data-ttu-id="81e1a-109">Pour plus d’informations sur la connexion à la console de gestion, voir [Comment se connecter à la console de gestion](how-to-connect-to-the-management-console-beta.md).</span><span class="sxs-lookup"><span data-stu-id="81e1a-109">For more information about how to connect to the Management Console, see [How to Connect to the Management Console](how-to-connect-to-the-management-console-beta.md).</span></span>

2.  <span data-ttu-id="81e1a-110">La liste des serveurs de publication déjà synchronisés avec le serveur de gestion s’affiche.</span><span class="sxs-lookup"><span data-stu-id="81e1a-110">A list of publishing servers that already synchronize with the management server is displayed.</span></span> <span data-ttu-id="81e1a-111">Cliquez sur inscrire un nouveau serveur pour inscrire un nouveau serveur.</span><span class="sxs-lookup"><span data-stu-id="81e1a-111">Click Register New Server to register a new server.</span></span>

3.  <span data-ttu-id="81e1a-112">Tapez le nom d’un ordinateur appartenant à un domaine dans la ligne **nom du serveur** pour spécifier un nom pour le serveur.</span><span class="sxs-lookup"><span data-stu-id="81e1a-112">Type a computer name of a domain joined computer on the **Server Name** line, to specify a name for the server.</span></span> <span data-ttu-id="81e1a-113">Vous devez également inclure un nom de domaine (par exemple, **MyDomain\\TestServer**.</span><span class="sxs-lookup"><span data-stu-id="81e1a-113">You should also include a domain name, for example, **MyDomain\\TestServer**.</span></span> <span data-ttu-id="81e1a-114">Cliquez sur **vérifier**.</span><span class="sxs-lookup"><span data-stu-id="81e1a-114">Click **Check**.</span></span>

4.  <span data-ttu-id="81e1a-115">Sélectionnez l’ordinateur, puis cliquez sur **Ajouter** pour ajouter l’ordinateur à la liste de serveurs.</span><span class="sxs-lookup"><span data-stu-id="81e1a-115">Select the computer and click **Add** to add the computer to the list of servers.</span></span> <span data-ttu-id="81e1a-116">Le nouveau serveur est affiché dans la liste.</span><span class="sxs-lookup"><span data-stu-id="81e1a-116">The new server will be displayed in the list.</span></span>

**<span data-ttu-id="81e1a-117">Pour annuler l’inscription d’un serveur de publication à l’aide de la console de gestion</span><span class="sxs-lookup"><span data-stu-id="81e1a-117">To unregister a publishing server using the Management Console</span></span>**

1.  <span data-ttu-id="81e1a-118">Connectez-vous à la console de gestion et sélectionnez **serveurs**.</span><span class="sxs-lookup"><span data-stu-id="81e1a-118">Connect to the Management Console and select **Servers**.</span></span> <span data-ttu-id="81e1a-119">Pour plus d’informations sur la connexion à la console de gestion, voir [Comment se connecter à la console de gestion](how-to-connect-to-the-management-console-beta.md).</span><span class="sxs-lookup"><span data-stu-id="81e1a-119">For more information about how to connect to the Management Console, see [How to Connect to the Management Console](how-to-connect-to-the-management-console-beta.md).</span></span>

2.  <span data-ttu-id="81e1a-120">La liste des serveurs de publication qui sont synchronisés avec le serveur de gestion s’affiche.</span><span class="sxs-lookup"><span data-stu-id="81e1a-120">A list of publishing servers that synchronize with the management server is displayed.</span></span>

3.  <span data-ttu-id="81e1a-121">Pour annuler l’inscription du serveur, cliquez avec le bouton droit sur le nom de l’ordinateur, puis sélectionnez le nom de l’ordinateur et sélectionnez **Annuler l’inscription de serveur**.</span><span class="sxs-lookup"><span data-stu-id="81e1a-121">To unregister the server, right-click the computer name and select the computer name and select **unregister server**.</span></span>

    <span data-ttu-id="81e1a-122">Vous **avez une suggestion pour App-V**?</span><span class="sxs-lookup"><span data-stu-id="81e1a-122">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="81e1a-123">Ajoutez ou Votez en fonction [de suggestions.](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)</span><span class="sxs-lookup"><span data-stu-id="81e1a-123">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="81e1a-124">Vous avez un problème lié à l’application-V?</span><span class="sxs-lookup"><span data-stu-id="81e1a-124">Got an App-V issue?</span></span>** <span data-ttu-id="81e1a-125">Utilisez le [Forum TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="81e1a-125">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="81e1a-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="81e1a-126">Related topics</span></span>


[<span data-ttu-id="81e1a-127">Opérations d'App-V5.0</span><span class="sxs-lookup"><span data-stu-id="81e1a-127">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 





