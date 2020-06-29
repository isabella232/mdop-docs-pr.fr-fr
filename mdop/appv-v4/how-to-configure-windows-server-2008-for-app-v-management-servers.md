---
title: Procédure pour configurer les serveurs Windows Server2008 pour App-V Management Server
description: Procédure pour configurer les serveurs Windows Server2008 pour App-V Management Server
author: dansimp
ms.assetid: 38b4016f-de82-4209-9159-387d20ddee25
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2d1cd7e84ffc0036c98e70a9a0ee1fd3a4ade790
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807221"
---
# <span data-ttu-id="c6aba-103">Procédure pour configurer les serveurs Windows Server2008 pour App-V Management Server</span><span class="sxs-lookup"><span data-stu-id="c6aba-103">How to Configure Windows Server 2008 for App-V Management Servers</span></span>


<span data-ttu-id="c6aba-104">Le serveur Windows Server 2008 sur lequel vous installez le service Web de gestion de Microsoft Application Virtualization (App-V) nécessite l’installation d’Internet Information Services (IIS) en tant que rôle sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="c6aba-104">The Windows Server 2008 server on which you install the Microsoft Application Virtualization (App-V) Management Web Service requires Internet Information Services (IIS) to be installed as a role on the server.</span></span> <span data-ttu-id="c6aba-105">Suivez la procédure ci-dessous pour configurer Windows Server 2008 de manière à prendre en charge l’installation de l’application vserver.</span><span class="sxs-lookup"><span data-stu-id="c6aba-105">Use the following procedure to configure Windows Server 2008 to support App-Vserver installation.</span></span>

**<span data-ttu-id="c6aba-106">Pour installer les services Internet (IIS) sur un ordinateur Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c6aba-106">To install IIS on a Windows Server2008 computer</span></span>**

1.  <span data-ttu-id="c6aba-107">Sur l’ordinateur Windows Server 2008, cliquez sur **Démarrer**, sur **tous les programmes**, sur **Outils d’administration**, puis sur **Gestionnaire de serveur** pour démarrer le gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="c6aba-107">On the Windows Server2008 computer, click **Start**, click **All Programs**, click **Administrative Tools**, and then click **Server Manager** to start Server Manager.</span></span> <span data-ttu-id="c6aba-108">Dans le gestionnaire de serveur, cliquez avec le bouton droit sur le nœud **rôles** , puis cliquez sur **Ajouter des rôles** pour démarrer l' **Assistant Ajout de rôles**.</span><span class="sxs-lookup"><span data-stu-id="c6aba-108">In Server Manager, right-click the **Roles** node, and click **Add Roles** to start the **Add Roles Wizard**.</span></span>

2.  <span data-ttu-id="c6aba-109">Dans l' **Assistant Ajout de rôles**, dans la page **Sélectionner des rôles de serveurs** , sélectionnez **serveur Web (IIS)**.</span><span class="sxs-lookup"><span data-stu-id="c6aba-109">In the **Add Roles Wizard**, on the **Select Server Roles** page, select **Web Server (IIS)**.</span></span> <span data-ttu-id="c6aba-110">Lorsque vous y êtes invité, cliquez sur **Ajouter les fonctionnalités requises** pour ajouter les fonctionnalités dépendantes.</span><span class="sxs-lookup"><span data-stu-id="c6aba-110">When prompted, click **Add Required Features** to add the dependent features.</span></span>

3.  <span data-ttu-id="c6aba-111">Dans la page **Sélectionner des rôles de serveur** , cliquez sur **suivant**, puis de nouveau sur **suivant** .</span><span class="sxs-lookup"><span data-stu-id="c6aba-111">On the **Select Server Roles** page, Click **Next**, and then click **Next** again.</span></span>

4.  <span data-ttu-id="c6aba-112">Dans l' **Assistant Ajout de rôles**, dans la page **Sélectionner des services de rôle** :</span><span class="sxs-lookup"><span data-stu-id="c6aba-112">In the **Add Roles Wizard**, on the **Select Role Services** page:</span></span>

    1.  <span data-ttu-id="c6aba-113">Sous **développement d’applications**, sélectionnez **ASP.net** , puis, lorsque vous y êtes invité, cliquez sur Ajouter les **services de rôle requis** pour ajouter les services et fonctionnalités de rôles dépendants.</span><span class="sxs-lookup"><span data-stu-id="c6aba-113">Under **Application Development**, select **ASP.NET** and, when prompted, click **Add Required Role Services** to add the dependent roles services and features.</span></span>

    2.  <span data-ttu-id="c6aba-114">Sous **sécurité**, sélectionnez **authentification Windows**.</span><span class="sxs-lookup"><span data-stu-id="c6aba-114">Under **Security**, select **Windows Authentication**.</span></span>

    3.  <span data-ttu-id="c6aba-115">Dans le nœud **outils de gestion** , sélectionnez **scripts et outils de gestion IIS**.</span><span class="sxs-lookup"><span data-stu-id="c6aba-115">In the **Management Tools** node, select **IIS Management Scripts and Tools**.</span></span> <span data-ttu-id="c6aba-116">Sous **compatibilité avec la gestion IIS6**, assurez-vous que la compatibilité avec la **métabase Iis6** et la **compatibilité WMI IIS6** sont sélectionnées, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="c6aba-116">Under **IIS6 Management Compatibility**, ensure that both **IIS6 Metabase Compatibility** and **IIS6 WMI Compatibility** are selected, and then click **Next**.</span></span>

5.  <span data-ttu-id="c6aba-117">Dans la page **confirmer les sélections** de l’installation, cliquez sur **installer**, puis suivez les instructions de l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="c6aba-117">On the **Confirm Installation Selections** page, click **Install**, and then complete the rest of the wizard.</span></span>

6.  <span data-ttu-id="c6aba-118">Cliquez sur **Fermer** pour quitter l' **Assistant Ajout de rôles**, puis fermez le gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="c6aba-118">Click **Close** to exit the **Add Roles Wizard**, and then close Server Manager.</span></span>

## <span data-ttu-id="c6aba-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c6aba-119">Related topics</span></span>


[<span data-ttu-id="c6aba-120">Configuration requise pour le déploiement d'Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="c6aba-120">Application Virtualization Deployment Requirements</span></span>](application-virtualization-deployment-requirements.md)

[<span data-ttu-id="c6aba-121">Listes de contrôle pour le déploiement et la mise à niveau d'Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="c6aba-121">Application Virtualization Deployment and Upgrade Checklists</span></span>](application-virtualization-deployment-and-upgrade-checklists.md)

 

 





