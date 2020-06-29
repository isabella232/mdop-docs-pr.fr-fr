---
title: Configurer les connexions du serveur AGPM
description: Configurer les connexions du serveur AGPM
author: dansimp
ms.assetid: bbbb15e8-35e7-403c-b695-7a6ebeb87839
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9b6b065b9855c6edf44456026baa32e8d9a4674f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807761"
---
# <span data-ttu-id="b70e4-103">Configurer les connexions du serveur AGPM</span><span class="sxs-lookup"><span data-stu-id="b70e4-103">Configure AGPM Server Connections</span></span>


<span data-ttu-id="b70e4-104">Toutes les versions de chaque objet de stratégie de groupe contrôlé (GPO) sont stockées dans une archive centrale de sorte que les administrateurs de stratégie de groupe puissent afficher et modifier les objets de stratégie de groupe hors connexion sans affecter immédiatement la version déployée de chaque GPO.</span><span class="sxs-lookup"><span data-stu-id="b70e4-104">All versions of each controlled Group Policy Object (GPO) are stored in a central archive so that Group Policy administrators can view and modify GPOs offline without immediately impacting the deployed version of each GPO.</span></span>

<span data-ttu-id="b70e4-105">Un compte d’utilisateur ayant le rôle d’administrateur AGPM (contrôle total), le compte d’utilisateur de l’approbateur qui a créé l’objet de stratégie de groupe utilisé dans ces procédures, ou un compte d’utilisateur disposant des autorisations nécessaires dans Advanced Group Policy Management (AGPM) est requis pour effectuer ces procédures pour la configuration centralisée des emplacements d’archivage de tous les administrateurs de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="b70e4-105">A user account with the AGPM Administrator (Full Control) role, the user account of the Approver who created the GPO used in these procedures, or a user account with the necessary permissions in Advanced Group Policy Management (AGPM) is required to complete these procedures for centrally configuring archive locations for all Group Policy administrators.</span></span> <span data-ttu-id="b70e4-106">Passez en revue les détails dans «autres considérations» dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="b70e4-106">Review the details in "Additional considerations" in this topic.</span></span>

## <span data-ttu-id="b70e4-107">Configuration des connexions au serveur AGPM</span><span class="sxs-lookup"><span data-stu-id="b70e4-107">Configuring AGPM Server connections</span></span>


<span data-ttu-id="b70e4-108">En tant qu’administrateur AGPM, vous pouvez vous assurer que tous les administrateurs de stratégie de groupe se connectent au même serveur AGPM en configurant le paramètre associé de manière centralisée.</span><span class="sxs-lookup"><span data-stu-id="b70e4-108">As an AGPM Administrator, you can ensure that all Group Policy administrators connect to the same AGPM Server by centrally configuring the associated setting.</span></span> <span data-ttu-id="b70e4-109">Si votre environnement nécessite des serveurs AGPM séparés pour tout ou partie des domaines, configurez ces serveurs AGPM supplémentaires en tant qu’exceptions par défaut.</span><span class="sxs-lookup"><span data-stu-id="b70e4-109">If your environment requires separate AGPM Servers for some or all domains, configure those additional AGPM Servers as exceptions to the default.</span></span> <span data-ttu-id="b70e4-110">Si vous ne configurez pas les connexions serveur AGPM de manière centralisée, chaque administrateur de stratégie de groupe doit configurer manuellement le serveur AGPM pour être affiché pour chaque domaine.</span><span class="sxs-lookup"><span data-stu-id="b70e4-110">If you do not centrally configure AGPM Server connections, each Group Policy administrator must manually configure the AGPM Server to be displayed for each domain.</span></span>

-   [<span data-ttu-id="b70e4-111">Configurer une connexion de serveur AGPM pour tous les administrateurs de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="b70e4-111">Configure an AGPM Server connection for all Group Policy administrators</span></span>](#bkmk-defaultarchiveloc)

-   [<span data-ttu-id="b70e4-112">Configurer des connexions serveur AGPM supplémentaires pour tous les administrateurs de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="b70e4-112">Configure additional AGPM Server connections for all Group Policy administrators</span></span>](#bkmk-additionalarchiveloc)

-   [<span data-ttu-id="b70e4-113">Configurer manuellement une connexion de serveur AGPM pour votre compte</span><span class="sxs-lookup"><span data-stu-id="b70e4-113">Manually configure an AGPM Server connection for your account</span></span>](#bkmk-manuallyconfigurearchiveloc)

### <a href="" id="bkmk-defaultarchiveloc"></a>

**<span data-ttu-id="b70e4-114">Pour configurer une connexion de serveur AGPM pour tous les administrateurs de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="b70e4-114">To configure an AGPM Server connection for all Group Policy administrators</span></span>**

1.  <span data-ttu-id="b70e4-115">Dans l’arborescence de la **console de gestion des stratégies de groupe** , modifiez un objet GPO qui est appliqué à tous les administrateurs de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="b70e4-115">In the **Group Policy Management Console** tree, edit a GPO that is applied to all Group Policy administrators.</span></span> <span data-ttu-id="b70e4-116">Pour plus d’informations, voir [modification d’un objet de stratégie de groupe](editing-a-gpo-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="b70e4-116">(For more information, see [Editing a GPO](editing-a-gpo-agpm40.md).)</span></span>

2.  <span data-ttu-id="b70e4-117">Dans la **fenêtre Éditeur de gestion des stratégies de groupe** , cliquez sur **Configuration utilisateur**, **stratégies**, **modèles d’administration**, **composants Windows**et **AGPM**.</span><span class="sxs-lookup"><span data-stu-id="b70e4-117">In the **Group Policy Management Editor** window, click **User Configuration**, **Policies**, **Administrative Templates**, **Windows Components**, and **AGPM**.</span></span>

3.  <span data-ttu-id="b70e4-118">Dans le volet Détails, double-cliquez sur **AGPM: spécifiez le serveur AGPM par défaut (tous les domaines)**.</span><span class="sxs-lookup"><span data-stu-id="b70e4-118">In the details pane, double-click **AGPM: Specify default AGPM Server (all domains)**.</span></span>

4.  <span data-ttu-id="b70e4-119">Dans la fenêtre **Propriétés** , activez la case à cocher **activé** , puis entrez le nom et le port complets de l’ordinateur (par exemple, Server.contoso.com:4600).</span><span class="sxs-lookup"><span data-stu-id="b70e4-119">In the **Properties** window, select the **Enabled** check box, and type the fully-qualified computer name and port (for example, server.contoso.com:4600).</span></span>

5.  <span data-ttu-id="b70e4-120">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="b70e4-120">Click **OK**.</span></span> <span data-ttu-id="b70e4-121">À moins que vous ne vouliez configurer des connexions de serveur AGPM supplémentaires, fermez la fenêtre **éditeur de gestion des stratégies de groupe** et déployez l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="b70e4-121">Unless you want to configure additional AGPM Server connections, close the **Group Policy Management Editor** window and deploy the GPO.</span></span> <span data-ttu-id="b70e4-122">Pour plus d’informations, consultez [la rubrique déploiement d’un objet de stratégie de groupe](deploy-a-gpo-agpm40.md). Lorsque la stratégie de groupe est mise à jour, la connexion au serveur AGPM est configurée pour tous les administrateurs de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="b70e4-122">(For more information, see [Deploy a GPO](deploy-a-gpo-agpm40.md).) When Group Policy is updated, the AGPM Server connection is configured for all Group Policy administrators.</span></span>

### <a href="" id="bkmk-additionalarchiveloc"></a>

**<span data-ttu-id="b70e4-123">Pour configurer des connexions serveur AGPM supplémentaires pour tous les administrateurs de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="b70e4-123">To configure additional AGPM Server connections for all Group Policy administrators</span></span>**

1.  <span data-ttu-id="b70e4-124">Si aucune connexion de serveur AGPM n’a été configurée, suivez la procédure ci-dessus pour configurer un serveur AGPM par défaut pour tous les domaines.</span><span class="sxs-lookup"><span data-stu-id="b70e4-124">If no AGPM Server connection has been configured, follow the preceding procedure to configure a default AGPM Server for all domains.</span></span>

2.  <span data-ttu-id="b70e4-125">Pour configurer des serveurs AGPM séparés pour tout ou partie des domaines (en remplaçant le serveur AGPM par défaut), dans l’arborescence de la **console de gestion des stratégies de groupe** , modifiez un objet GPO qui est appliqué à tous les administrateurs de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="b70e4-125">To configure separate AGPM Servers for some or all domains (overriding the default AGPM Server), in the **Group Policy Management Console** tree, edit a GPO that is applied to all Group Policy administrators.</span></span> <span data-ttu-id="b70e4-126">Pour plus d’informations, voir [modification d’un objet de stratégie de groupe](editing-a-gpo-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="b70e4-126">(For more information, see [Editing a GPO](editing-a-gpo-agpm40.md).)</span></span>

3.  <span data-ttu-id="b70e4-127">Dans la fenêtre de l' **éditeur de gestion des stratégies de groupe** , cliquez sur **Configuration utilisateur**, **stratégies**, **modèles d’administration**, **composants Windows**, puis **AGPM**.</span><span class="sxs-lookup"><span data-stu-id="b70e4-127">In the **Group Policy Management Editor** window, click **User Configuration**, **Policies**, **Administrative Templates**, **Windows Components**, and then **AGPM**.</span></span>

4.  <span data-ttu-id="b70e4-128">Dans le volet Détails, double-cliquez sur **AGPM: spécifier les serveurs AGPM**.</span><span class="sxs-lookup"><span data-stu-id="b70e4-128">In the details pane, double-click **AGPM: Specify AGPM Servers**.</span></span>

5.  <span data-ttu-id="b70e4-129">Dans la fenêtre **Propriétés** , activez la case à cocher **activé** , puis cliquez sur **Afficher**.</span><span class="sxs-lookup"><span data-stu-id="b70e4-129">In the **Properties** window, select the **Enabled** check box, and click **Show**.</span></span>

6.  <span data-ttu-id="b70e4-130">Dans la fenêtre **afficher les contenus** :</span><span class="sxs-lookup"><span data-stu-id="b70e4-130">In the **Show Contents** window:</span></span>

    1.  <span data-ttu-id="b70e4-131">Cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="b70e4-131">Click **Add**.</span></span>

    2.  <span data-ttu-id="b70e4-132">Pour **nom**de la valeur, tapez le nom de domaine (par exemple, server1.contoso.com).</span><span class="sxs-lookup"><span data-stu-id="b70e4-132">For **Value Name**, type the domain name (for example, server1.contoso.com).</span></span>

    3.  <span data-ttu-id="b70e4-133">Pour la **valeur**, tapez le nom du serveur AGPM et le port à utiliser pour ce domaine (par exemple, Server2.contoso.com:4600), puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="b70e4-133">For **Value**, type the AGPM Server name and port to use for this domain (for example, server2.contoso.com:4600), and then click **OK**.</span></span> <span data-ttu-id="b70e4-134">(Par défaut, le service AGPM écoute sur le port 4600.</span><span class="sxs-lookup"><span data-stu-id="b70e4-134">(By default, the AGPM Service listens on port 4600.</span></span> <span data-ttu-id="b70e4-135">Pour utiliser un autre port, voir [modifier le service AGPM](modify-the-agpm-service-agpm40.md).)</span><span class="sxs-lookup"><span data-stu-id="b70e4-135">To use a different port, see [Modify the AGPM Service](modify-the-agpm-service-agpm40.md).)</span></span>

    4.  <span data-ttu-id="b70e4-136">Répétez cette procédure pour chaque domaine qui n’utilise pas le serveur AGPM par défaut.</span><span class="sxs-lookup"><span data-stu-id="b70e4-136">Repeat for each domain not using the default AGPM Server.</span></span>

7.  <span data-ttu-id="b70e4-137">Cliquez sur **OK** pour fermer les fenêtres **afficher le contenu** et les **Propriétés** .</span><span class="sxs-lookup"><span data-stu-id="b70e4-137">Click **OK** to close the **Show Contents** and **Properties** windows.</span></span>

8.  <span data-ttu-id="b70e4-138">Fermez la fenêtre de l' **éditeur de gestion des stratégies de groupe** .</span><span class="sxs-lookup"><span data-stu-id="b70e4-138">Close the **Group Policy Management Editor** window.</span></span> <span data-ttu-id="b70e4-139">Pour plus d’informations, consultez [la rubrique déploiement d’un objet de stratégie de groupe](deploy-a-gpo-agpm40.md). Lorsque la stratégie de groupe est mise à jour, les nouvelles connexions au serveur AGPM sont configurées pour tous les administrateurs de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="b70e4-139">(For more information, see [Deploy a GPO](deploy-a-gpo-agpm40.md).) When Group Policy is updated, the new AGPM Server connections are configured for all Group Policy administrators.</span></span>

### <a href="" id="bkmk-manuallyconfigurearchiveloc"></a>

<span data-ttu-id="b70e4-140">Si vous avez configuré la connexion à un serveur AGPM de manière centralisée, l’option de configuration manuelle n’est pas disponible pour tous les administrateurs de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="b70e4-140">If you have centrally configured the AGPM Server connection, the option to manually configure it is unavailable for all Group Policy administrators.</span></span>

**<span data-ttu-id="b70e4-141">Pour configurer manuellement le serveur AGPM à afficher pour votre compte</span><span class="sxs-lookup"><span data-stu-id="b70e4-141">To manually configure which AGPM Server to display for your account</span></span>**

1.  <span data-ttu-id="b70e4-142">Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="b70e4-142">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="b70e4-143">Dans le volet Détails, cliquez sur l’onglet **serveur AGPM** .</span><span class="sxs-lookup"><span data-stu-id="b70e4-143">In the details pane, click the **AGPM Server** tab.</span></span>

3.  <span data-ttu-id="b70e4-144">Entrez le nom complet de l’ordinateur pour le serveur AGPM qui gère l’archive utilisée pour ce domaine (par exemple, server.contoso.com) et le port sur lequel le service AGPM écoute (par défaut, le port 4600).</span><span class="sxs-lookup"><span data-stu-id="b70e4-144">Enter the fully-qualified computer name for the AGPM Server that manages the archive used for this domain (for example, server.contoso.com) and the port on which the AGPM Service listens (by default, port 4600).</span></span>

4.  <span data-ttu-id="b70e4-145">Cliquez sur **appliquer**, puis sur **Oui** pour confirmer.</span><span class="sxs-lookup"><span data-stu-id="b70e4-145">Click **Apply**, then click **Yes** to confirm.</span></span>

### <span data-ttu-id="b70e4-146">Autres éléments à prendre en considération</span><span class="sxs-lookup"><span data-stu-id="b70e4-146">Additional considerations</span></span>

-   <span data-ttu-id="b70e4-147">Vous devez être en mesure de modifier et de déployer un objet de stratégie de groupe pour pouvoir exécuter les procédures de configuration centralisée des connexions serveur AGPM pour tous les administrateurs de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="b70e4-147">You must be able to edit and deploy a GPO to perform the procedures for centrally configuring AGPM Server connections for all Group Policy administrators.</span></span> <span data-ttu-id="b70e4-148">Pour plus d’informations, voir [modification d’un objet de stratégie de groupe](editing-a-gpo-agpm40.md) et [déploiement d’un objet de stratégie de groupe](deploy-a-gpo-agpm40.md)</span><span class="sxs-lookup"><span data-stu-id="b70e4-148">See [Editing a GPO](editing-a-gpo-agpm40.md) and [Deploy a GPO](deploy-a-gpo-agpm40.md) for additional detail.</span></span>

-   <span data-ttu-id="b70e4-149">Le serveur AGPM sélectionné détermine les objets de stratégie de groupe qui s’affichent dans l’onglet **Sommaire** et à quel emplacement les paramètres de l’onglet **délégation de domaine** sont appliqués.</span><span class="sxs-lookup"><span data-stu-id="b70e4-149">The selected AGPM Server determines which GPOs are displayed on the **Contents** tab and to what location the **Domain Delegation** tab settings are applied.</span></span> <span data-ttu-id="b70e4-150">S’ils ne sont pas gérés de manière centralisée par le biais du modèle d’administration, chaque administrateur de stratégie de groupe doit configurer ce paramètre pour qu’il pointe vers le serveur AGPM du domaine.</span><span class="sxs-lookup"><span data-stu-id="b70e4-150">If not centrally managed through the Administrative template, each Group Policy administrator must configure this setting to point to the AGPM Server for the domain.</span></span>

-   <span data-ttu-id="b70e4-151">L’appartenance au groupe de propriétaires de la stratégie de groupe doit être restreinte, soit n’est pas utilisé pour contourner la gestion d’accès d’AGPM aux objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="b70e4-151">Membership in the Group Policy Creator Owners group should be restricted, soit is not used to circumvent AGPM management of access to GPOs.</span></span> <span data-ttu-id="b70e4-152">(Dans la **console de gestion des stratégies de groupe**, cliquez sur **objets de stratégie de groupe** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe, cliquez sur **délégation**, puis configurez les paramètres en fonction des besoins de votre organisation.)</span><span class="sxs-lookup"><span data-stu-id="b70e4-152">(In the **Group Policy Management Console**, click **Group Policy Objects** in the forest and domain in which you want to manage GPOs, click **Delegation**, and then configure the settings to meet the needs of your organization.)</span></span>

### <span data-ttu-id="b70e4-153">Références supplémentaires</span><span class="sxs-lookup"><span data-stu-id="b70e4-153">Additional references</span></span>

-   [<span data-ttu-id="b70e4-154">Configuration de la Gestion avancée des stratégies de groupe</span><span class="sxs-lookup"><span data-stu-id="b70e4-154">Configuring Advanced Group Policy Management</span></span>](configuring-advanced-group-policy-management-agpm40.md)

 

 





