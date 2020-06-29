---
title: Configurer la connexion au serveur AGPM
description: Configurer la connexion au serveur AGPM
author: dansimp
ms.assetid: 9a42b5bc-41be-44ef-a6e2-6f56e2cf1996
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 88182f0e79f1a8bcce53e0d50c014e8d4aa29286
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807697"
---
# <span data-ttu-id="a58ca-103">Configurer la connexion au serveur AGPM</span><span class="sxs-lookup"><span data-stu-id="a58ca-103">Configure the AGPM Server Connection</span></span>


<span data-ttu-id="a58ca-104">La gestion avancée de la stratégie de groupe stocke toutes les versions de chaque objet de stratégie de groupe contrôlé (GPO) dans une archive centrale, de sorte que les administrateurs de stratégie de groupe peuvent afficher et modifier les objets de stratégie de groupe hors connexion sans avoir d’impact sur la version déployée de chaque GPO.</span><span class="sxs-lookup"><span data-stu-id="a58ca-104">Advanced Group Policy Management (AGPM) stores all versions of each controlled Group Policy object (GPO) in a central archive, so Group Policy administrators can view and modify GPOs offline without immediately impacting the deployed version of each GPO.</span></span>

<span data-ttu-id="a58ca-105">Un compte d’utilisateur ayant le rôle d’administrateur AGPM (contrôle total), le compte d’utilisateur de l’approbateur qui a créé l’objet de stratégie de groupe utilisé dans ces procédures, ou un compte d’utilisateur disposant des autorisations nécessaires dans la gestion avancée de la stratégie de groupe est requis pour effectuer ces procédures pour la configuration centralisée des emplacements d’archivage de tous les administrateurs</span><span class="sxs-lookup"><span data-stu-id="a58ca-105">A user account with the AGPM Administrator (Full Control) role, the user account of the Approver who created the GPO used in these procedures, or a user account with the necessary permissions in Advanced Group Policy Management is required to complete these procedures for centrally configuring archive locations for all Group Policy administrators.</span></span> <span data-ttu-id="a58ca-106">Passez en revue les détails dans «autres considérations» dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="a58ca-106">Review the details in "Additional considerations" in this topic.</span></span>

## <span data-ttu-id="a58ca-107">Configuration de la connexion au serveur AGPM</span><span class="sxs-lookup"><span data-stu-id="a58ca-107">Configuring the AGPM Server connection</span></span>


<span data-ttu-id="a58ca-108">En tant qu’administrateur AGPM (contrôle total), vous pouvez vous assurer que tous les administrateurs de stratégie de groupe se connectent au même serveur AGPM en configurant le paramètre de manière centralisée.</span><span class="sxs-lookup"><span data-stu-id="a58ca-108">As an AGPM Administrator (Full Control), you can ensure that all Group Policy administrators connect to the same AGPM Server by centrally configuring the setting.</span></span> <span data-ttu-id="a58ca-109">Si votre environnement nécessite des serveurs AGPM séparés pour tout ou partie des domaines, configurez ces serveurs AGPM supplémentaires en tant qu’exceptions par défaut.</span><span class="sxs-lookup"><span data-stu-id="a58ca-109">If your environment requires separate AGPM Servers for some or all domains, configure those additional AGPM Servers as exceptions to the default.</span></span> <span data-ttu-id="a58ca-110">Si vous ne configurez pas les connexions serveur AGPM de manière centralisée, chaque administrateur de stratégie de groupe doit configurer manuellement le serveur AGPM pour être affiché pour chaque domaine.</span><span class="sxs-lookup"><span data-stu-id="a58ca-110">If you do not centrally configure AGPM Server connections, each Group Policy administrator must manually configure the AGPM Server to be displayed for each domain.</span></span>

-   [<span data-ttu-id="a58ca-111">Configurer un serveur AGPM pour tous les administrateurs de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="a58ca-111">Configure an AGPM Server for all Group Policy administrators</span></span>](#bkmk-defaultarchiveloc)

-   [<span data-ttu-id="a58ca-112">Configurer des serveurs AGPM supplémentaires pour tous les administrateurs de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="a58ca-112">Configure additional AGPM Servers for all Group Policy administrators</span></span>](#bkmk-additionalarchiveloc)

-   [<span data-ttu-id="a58ca-113">Configurer manuellement un serveur AGPM pour votre compte</span><span class="sxs-lookup"><span data-stu-id="a58ca-113">Manually configure an AGPM Server for your account</span></span>](#bkmk-manuallyconfigurearchiveloc)

### <a href="" id="bkmk-defaultarchiveloc"></a>

**<span data-ttu-id="a58ca-114">Pour configurer un serveur AGPM pour tous les administrateurs de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="a58ca-114">To configure an AGPM Server for all Group Policy administrators</span></span>**

1.  <span data-ttu-id="a58ca-115">Dans l’arborescence de la **console de gestion des stratégies de groupe** , modifiez un objet GPO qui est appliqué à tous les administrateurs de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="a58ca-115">In the **Group Policy Management Console** tree, edit a GPO that is applied to all Group Policy administrators.</span></span> <span data-ttu-id="a58ca-116">Pour plus d’informations, voir [modification d’un objet de stratégie de groupe](editing-a-gpo.md).</span><span class="sxs-lookup"><span data-stu-id="a58ca-116">(For more information, see [Editing a GPO](editing-a-gpo.md).)</span></span>

2.  <span data-ttu-id="a58ca-117">Dans l' **éditeur d’objets de stratégie de groupe**, cliquez sur **Configuration utilisateur**, **modèles d’administration**et **composants Windows**.</span><span class="sxs-lookup"><span data-stu-id="a58ca-117">In the **Group Policy Object Editor**, click **User Configuration**, **Administrative Templates**, and **Windows Components**.</span></span>

3.  <span data-ttu-id="a58ca-118">Si **AGPM** ne figure pas dans la liste **composants Windows**:</span><span class="sxs-lookup"><span data-stu-id="a58ca-118">If **AGPM** is not listed under **Windows Components**:</span></span>

    1.  <span data-ttu-id="a58ca-119">Cliquez avec le bouton droit sur **modèles d’administration** et sélectionnez **Ajouter/supprimer des modèles**.</span><span class="sxs-lookup"><span data-stu-id="a58ca-119">Right-click **Administrative Templates** and click **Add/Remove Templates**.</span></span>

    2.  <span data-ttu-id="a58ca-120">Cliquez **sur Ajouter**, sélectionnez **AGPM. admx** ou **AGPM. adm**, cliquez sur **ouvrir**, puis sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="a58ca-120">Click **Add**, select **agpm.admx** or **agpm.adm**, click **Open**, and then click **Close**.</span></span>

4.  <span data-ttu-id="a58ca-121">Sous **composants Windows**, double-cliquez sur **AGPM**.</span><span class="sxs-lookup"><span data-stu-id="a58ca-121">Under **Windows Components**, double-click **AGPM**.</span></span>

5.  <span data-ttu-id="a58ca-122">Dans le volet Détails, double-cliquez sur le **serveur AGPM (tous les domaines)**.</span><span class="sxs-lookup"><span data-stu-id="a58ca-122">In the details pane, double-click **AGPM Server (all domains)**.</span></span>

6.  <span data-ttu-id="a58ca-123">Dans la fenêtre de **Propriétés de serveur AGPM (All domains)** , activez la case à cocher **activé** , puis entrez le nom de l’ordinateur et le port complet (par exemple, Server.contoso.com:4600).</span><span class="sxs-lookup"><span data-stu-id="a58ca-123">In the **AGPM Server (all domains) Properties** window, select the **Enabled** check box, and type the fully-qualified computer name and port (for example, server.contoso.com:4600).</span></span>

7.  <span data-ttu-id="a58ca-124">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="a58ca-124">Click **OK**.</span></span> <span data-ttu-id="a58ca-125">À moins que vous ne vouliez configurer des connexions de serveur AGPM supplémentaires, fermez l' **éditeur d’objets de stratégie de groupe** et déployez l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="a58ca-125">Unless you want to configure additional AGPM Server connections, close the **Group Policy Object Editor** and deploy the GPO.</span></span> <span data-ttu-id="a58ca-126">Pour plus d’informations, consultez [la rubrique déploiement d’un objet de stratégie de groupe](deploy-a-gpo.md). Lorsque la stratégie de groupe est mise à jour, la connexion au serveur AGPM est configurée pour tous les administrateurs de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="a58ca-126">(For more information, see [Deploy a GPO](deploy-a-gpo.md).) When Group Policy is updated, the AGPM Server connection is configured for all Group Policy administrators.</span></span>

### <a href="" id="bkmk-additionalarchiveloc"></a>

**<span data-ttu-id="a58ca-127">Pour configurer des serveurs AGPM supplémentaires pour tous les administrateurs de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="a58ca-127">To configure additional AGPM Servers for all Group Policy administrators</span></span>**

1.  <span data-ttu-id="a58ca-128">Si aucune connexion de serveur AGPM n’a été configurée, suivez la procédure ci-dessus pour configurer un serveur AGPM par défaut pour tous les domaines.</span><span class="sxs-lookup"><span data-stu-id="a58ca-128">If no AGPM Server connection has been configured, follow the preceding procedure to configure a default AGPM Server for all domains.</span></span>

2.  <span data-ttu-id="a58ca-129">Pour configurer des serveurs AGPM séparés pour tout ou partie des domaines (en remplaçant le serveur AGPM par défaut), dans l’arborescence de la **console de gestion des stratégies de groupe** , modifiez un objet GPO qui est appliqué à tous les administrateurs de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="a58ca-129">To configure separate AGPM Servers for some or all domains (overriding the default AGPM Server), in the **Group Policy Management Console** tree, edit a GPO that is applied to all Group Policy administrators.</span></span> <span data-ttu-id="a58ca-130">Pour plus d’informations, voir [modification d’un objet de stratégie de groupe](editing-a-gpo.md).</span><span class="sxs-lookup"><span data-stu-id="a58ca-130">(For more information, see [Editing a GPO](editing-a-gpo.md).)</span></span>

3.  <span data-ttu-id="a58ca-131">Sous **Configuration utilisateur** dans l' **éditeur d’objets de stratégie de groupe**, double-cliquez sur **modèles d’administration**, **composants Windows**, puis sur **AGPM**.</span><span class="sxs-lookup"><span data-stu-id="a58ca-131">Under **User Configuration** in the **Group Policy Object Editor**, double-click **Administrative Templates**, **Windows Components**, and then **AGPM**.</span></span>

4.  <span data-ttu-id="a58ca-132">Dans le volet Détails, double-cliquez sur le **serveur AGPM**.</span><span class="sxs-lookup"><span data-stu-id="a58ca-132">In the details pane, double-click **AGPM Server**.</span></span>

5.  <span data-ttu-id="a58ca-133">Dans la fenêtre **Propriétés de serveur AGPM** , activez la case à cocher **activé** , puis cliquez sur **Afficher**.</span><span class="sxs-lookup"><span data-stu-id="a58ca-133">In the **AGPM Server Properties** window, select the **Enabled** check box, and click **Show**.</span></span>

6.  <span data-ttu-id="a58ca-134">Dans la fenêtre **afficher les contenus** :</span><span class="sxs-lookup"><span data-stu-id="a58ca-134">In the **Show Contents** window:</span></span>

    1.  <span data-ttu-id="a58ca-135">Cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="a58ca-135">Click **Add**.</span></span>

    2.  <span data-ttu-id="a58ca-136">Pour **nom**de la valeur, tapez le nom de domaine (par exemple, server1.contoso.com).</span><span class="sxs-lookup"><span data-stu-id="a58ca-136">For **Value Name**, type the domain name (for example, server1.contoso.com).</span></span>

    3.  <span data-ttu-id="a58ca-137">Pour la **valeur**, tapez le nom du serveur AGPM et le port à utiliser pour ce domaine (par exemple, Server2.contoso.com:4600), puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="a58ca-137">For **Value**, type the AGPM Server name and port to use for this domain (for example, server2.contoso.com:4600), and then click **OK**.</span></span> <span data-ttu-id="a58ca-138">(Par défaut, le service AGPM écoute sur le port 4600.</span><span class="sxs-lookup"><span data-stu-id="a58ca-138">(By default, the AGPM Service listens on port 4600.</span></span> <span data-ttu-id="a58ca-139">Pour utiliser un autre port, voir [modifier le port sur lequel écoute le service AGPM](modify-the-port-on-which-the-agpm-service-listens.md).)</span><span class="sxs-lookup"><span data-stu-id="a58ca-139">To use a different port, see [Modify the Port on Which the AGPM Service Listens](modify-the-port-on-which-the-agpm-service-listens.md).)</span></span>

    4.  <span data-ttu-id="a58ca-140">Répétez cette procédure pour chaque domaine qui n’utilise pas le serveur AGPM par défaut.</span><span class="sxs-lookup"><span data-stu-id="a58ca-140">Repeat for each domain not using the default AGPM Server.</span></span>

7.  <span data-ttu-id="a58ca-141">Cliquez sur **OK** pour fermer les fenêtres **afficher le contenu** et les propriétés du **serveur AGPM** .</span><span class="sxs-lookup"><span data-stu-id="a58ca-141">Click **OK** to close the **Show Contents** and **AGPM Server Properties** windows.</span></span>

8.  <span data-ttu-id="a58ca-142">Fermez l' **éditeur d’objets de stratégie de groupe**.</span><span class="sxs-lookup"><span data-stu-id="a58ca-142">Close the **Group Policy Object Editor**.</span></span> <span data-ttu-id="a58ca-143">Pour plus d’informations, consultez [la rubrique déploiement d’un objet de stratégie de groupe](deploy-a-gpo.md). Lorsque la stratégie de groupe est mise à jour, les nouvelles connexions au serveur AGPM sont configurées pour tous les administrateurs de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="a58ca-143">(For more information, see [Deploy a GPO](deploy-a-gpo.md).) When Group Policy is updated, the new AGPM Server connections are configured for all Group Policy administrators.</span></span>

### <a href="" id="bkmk-manuallyconfigurearchiveloc"></a>

<span data-ttu-id="a58ca-144">Si vous avez configuré la connexion à un serveur AGPM de manière centralisée, l’option d’accès manuel n’est pas disponible pour tous les administrateurs de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="a58ca-144">If you have centrally configured the AGPM Server connection, the option to manually it is unavailable for all Group Policy administrators.</span></span>

**<span data-ttu-id="a58ca-145">Pour configurer manuellement le serveur AGPM de sorte qu’il s’affiche pour votre compte</span><span class="sxs-lookup"><span data-stu-id="a58ca-145">To manually configure the AGPM Server to display for your account</span></span>**

1.  <span data-ttu-id="a58ca-146">Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="a58ca-146">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="a58ca-147">Dans le volet Détails, cliquez sur l’onglet **serveur AGPM** .</span><span class="sxs-lookup"><span data-stu-id="a58ca-147">In the details pane, click the **AGPM Server** tab.</span></span>

3.  <span data-ttu-id="a58ca-148">Entrez le nom complet de l’ordinateur pour le serveur AGPM qui gère l’archive utilisée pour ce domaine (par exemple, server.contoso.com) et le port sur lequel le service AGPM écoute (par défaut, le port 4600).</span><span class="sxs-lookup"><span data-stu-id="a58ca-148">Enter the fully-qualified computer name for the AGPM Server that manages the archive used for this domain (for example, server.contoso.com) and the port on which the AGPM Service listens (by default, port 4600).</span></span>

4.  <span data-ttu-id="a58ca-149">Cliquez sur **appliquer**, puis sur **Oui** pour confirmer.</span><span class="sxs-lookup"><span data-stu-id="a58ca-149">Click **Apply**, then click **Yes** to confirm.</span></span>

### <span data-ttu-id="a58ca-150">Autres éléments à prendre en considération</span><span class="sxs-lookup"><span data-stu-id="a58ca-150">Additional considerations</span></span>

-   <span data-ttu-id="a58ca-151">Vous devez être en mesure de modifier et de déployer un objet de stratégie de groupe pour pouvoir exécuter les procédures de configuration centralisée des connexions serveur AGPM pour tous les administrateurs de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="a58ca-151">You must be able to edit and deploy a GPO to perform the procedures for centrally configuring AGPM Server connections for all Group Policy administrators.</span></span> <span data-ttu-id="a58ca-152">Pour plus d’informations, voir [modification d’un objet de stratégie de groupe](editing-a-gpo.md) et [déploiement d’un objet de stratégie de groupe](deploy-a-gpo.md)</span><span class="sxs-lookup"><span data-stu-id="a58ca-152">See [Editing a GPO](editing-a-gpo.md) and [Deploy a GPO](deploy-a-gpo.md) for additional detail.</span></span>

-   <span data-ttu-id="a58ca-153">Le serveur AGPM sélectionné détermine les objets de stratégie de groupe qui s’affichent sous l’onglet **contenu** , ainsi que l’emplacement dans lequel les paramètres de l’onglet **délégation de domaine** sont appliqués.</span><span class="sxs-lookup"><span data-stu-id="a58ca-153">The AGPM Server selected determines which GPOs are displayed on the **Contents** tab and to what location the **Domain Delegation** tab settings are applied.</span></span> <span data-ttu-id="a58ca-154">S’ils ne sont pas gérés de manière centralisée par le biais du modèle d’administration, chaque administrateur de stratégie de groupe doit configurer ce paramètre pour qu’il pointe vers le serveur AGPM du domaine.</span><span class="sxs-lookup"><span data-stu-id="a58ca-154">If not centrally managed through the Administrative Template, each Group Policy administrator must configure this setting to point to the AGPM Server for the domain.</span></span>

-   <span data-ttu-id="a58ca-155">L’appartenance au groupe de propriétaires de la stratégie de groupe doit être restreinte afin qu’elle ne soit pas utilisée pour contourner la gestion de l’accès aux objets de stratégie de groupe par AGPM.</span><span class="sxs-lookup"><span data-stu-id="a58ca-155">Membership in the Group Policy Creator Owners group should be restricted so that it is not used to circumvent the management of access to GPOs by AGPM.</span></span> <span data-ttu-id="a58ca-156">(Dans la **console de gestion des stratégies de groupe**, cliquez sur **objets de stratégie de groupe** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe, cliquez sur **délégation**, puis configurez les paramètres en fonction des besoins de votre organisation.)</span><span class="sxs-lookup"><span data-stu-id="a58ca-156">(In the **Group Policy Management Console**, click **Group Policy Objects** in the forest and domain in which you want to manage GPOs, click **Delegation**, and then configure the settings to meet the needs of your organization.)</span></span>

### <span data-ttu-id="a58ca-157">Références supplémentaires</span><span class="sxs-lookup"><span data-stu-id="a58ca-157">Additional references</span></span>

-   [<span data-ttu-id="a58ca-158">Exécution de tâches d'administrateur AGPM</span><span class="sxs-lookup"><span data-stu-id="a58ca-158">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks.md)

 

 





