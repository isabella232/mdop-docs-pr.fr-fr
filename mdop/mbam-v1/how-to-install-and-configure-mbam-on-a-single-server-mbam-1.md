---
title: Installation et configuration de MBAM sur un seul serveur
description: Installation et configuration de MBAM sur un seul serveur
author: dansimp
ms.assetid: 55841c63-bad9-44e7-b7fd-ea7037febbd7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 225f66493ceafce5461df3fcc6f701e9a2922a5f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810350"
---
# <span data-ttu-id="bc7af-103">Installation et configuration de MBAM sur un seul serveur</span><span class="sxs-lookup"><span data-stu-id="bc7af-103">How to Install and Configure MBAM on a Single Server</span></span>


<span data-ttu-id="bc7af-104">Les procédures décrites dans cette rubrique décrivent l’installation complète des fonctionnalités d’administration et de surveillance de Microsoft BitLocker (MBAM) sur un serveur unique.</span><span class="sxs-lookup"><span data-stu-id="bc7af-104">The procedures in this topic describe the full installation of the Microsoft BitLocker Administration and Monitoring (MBAM) features on a single server.</span></span>

<span data-ttu-id="bc7af-105">Chaque fonctionnalité de serveur comporte certaines conditions préalables.</span><span class="sxs-lookup"><span data-stu-id="bc7af-105">Each server feature has certain prerequisites.</span></span> <span data-ttu-id="bc7af-106">Pour vérifier que vous remplissez les conditions préalables et la configuration matérielle et logicielle requise, voir Configuration requise pour le [déploiement d’MBAM 1,0](mbam-10-deployment-prerequisites.md) et [Configurations prises en charge par MBAM 1,0](mbam-10-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="bc7af-106">To verify that you have met the prerequisites and the hardware and software requirements, see [MBAM 1.0 Deployment Prerequisites](mbam-10-deployment-prerequisites.md) and [MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md).</span></span> <span data-ttu-id="bc7af-107">De plus, certaines fonctions disposent également d’informations qui doivent être fournies pendant le processus d’installation pour le déploiement de la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="bc7af-107">In addition, some features also have information that must be provided during the installation process to successfully deploy the feature.</span></span> <span data-ttu-id="bc7af-108">Avant de commencer le déploiement MBAM, nous vous conseillons également [de consulter préparer votre environnement pour MBAM 1,0](preparing-your-environment-for-mbam-10.md) .</span><span class="sxs-lookup"><span data-stu-id="bc7af-108">You should also review [Preparing your Environment for MBAM 1.0](preparing-your-environment-for-mbam-10.md) before you begin the MBAM deployment.</span></span>

<span data-ttu-id="bc7af-109">**Remarques**  Pour obtenir les fichiers journaux d’installation, vous devez installer MBAM à l’aide du package **msiexec** et de l’option **/l** &lt; emplacement &gt; .</span><span class="sxs-lookup"><span data-stu-id="bc7af-109">**Note** To obtain the setup log files, you must install MBAM by using the **msiexec** package and the **/l** &lt;location&gt; option.</span></span> <span data-ttu-id="bc7af-110">Les fichiers journaux sont créés à l’emplacement que vous spécifiez.</span><span class="sxs-lookup"><span data-stu-id="bc7af-110">Log files are created in the location that you specify.</span></span>

<span data-ttu-id="bc7af-111">D’autres fichiers journaux d’installation sont créés dans le dossier% Temp% de l’utilisateur qui installe MBAM.</span><span class="sxs-lookup"><span data-stu-id="bc7af-111">Additional setup log files are created in the %temp% folder of the user who is installing MBAM.</span></span>

 

## <span data-ttu-id="bc7af-112">Pour installer les fonctionnalités du serveur MBAM sur un serveur unique</span><span class="sxs-lookup"><span data-stu-id="bc7af-112">To install MBAM Server features on a single server</span></span>


<span data-ttu-id="bc7af-113">Les étapes suivantes expliquent comment installer les fonctionnalités MBAM générales.</span><span class="sxs-lookup"><span data-stu-id="bc7af-113">The following steps describe how to install general MBAM features.</span></span>

<span data-ttu-id="bc7af-114">**Remarques**  Vérifiez que vous utilisez la configuration de 32 bits sur les serveurs 32 bits et la configuration 64 bits sur les serveurs 64.</span><span class="sxs-lookup"><span data-stu-id="bc7af-114">**Note** Make sure that you use the 32-bit setup on 32-bit servers and the 64-bit setup on 64-bit servers.</span></span>

 

**<span data-ttu-id="bc7af-115">Pour démarrer l’installation de fonctionnalités de MBAM Server</span><span class="sxs-lookup"><span data-stu-id="bc7af-115">To start MBAM Server features installation</span></span>**

1.  <span data-ttu-id="bc7af-116">Démarrez l’Assistant Installation de MBAM.</span><span class="sxs-lookup"><span data-stu-id="bc7af-116">Start the MBAM installation wizard.</span></span> <span data-ttu-id="bc7af-117">Cliquez sur **installer** sur la page d’accueil.</span><span class="sxs-lookup"><span data-stu-id="bc7af-117">Click **Install** at the Welcome page.</span></span>

2.  <span data-ttu-id="bc7af-118">Lisez et acceptez les termes du contrat de licence logiciel Microsoft, puis cliquez sur **suivant** pour continuer l’installation.</span><span class="sxs-lookup"><span data-stu-id="bc7af-118">Read and accept the Microsoft Software License Terms, and then click **Next** to continue the installation.</span></span>

3.  <span data-ttu-id="bc7af-119">Par défaut, toutes les fonctionnalités de MBAM sont sélectionnées pour l’installation.</span><span class="sxs-lookup"><span data-stu-id="bc7af-119">By default, all MBAM features are selected for installation.</span></span> <span data-ttu-id="bc7af-120">Les fonctionnalités qui seront installées sur le même ordinateur doivent être installées en même temps.</span><span class="sxs-lookup"><span data-stu-id="bc7af-120">Features that will be installed on the same computer must be installed together at the same time.</span></span> <span data-ttu-id="bc7af-121">Effacez les fonctionnalités que vous voulez installer ailleurs.</span><span class="sxs-lookup"><span data-stu-id="bc7af-121">Clear the features that you want to install elsewhere.</span></span> <span data-ttu-id="bc7af-122">Vous devez installer les fonctionnalités MBAM dans l’ordre suivant:</span><span class="sxs-lookup"><span data-stu-id="bc7af-122">You must install the MBAM features in the following order:</span></span>

    -   <span data-ttu-id="bc7af-123">Base de données de récupération et de matériel</span><span class="sxs-lookup"><span data-stu-id="bc7af-123">Recovery and Hardware Database</span></span>

    -   <span data-ttu-id="bc7af-124">Base de données d’audit et de conformité</span><span class="sxs-lookup"><span data-stu-id="bc7af-124">Compliance and Audit Database</span></span>

    -   <span data-ttu-id="bc7af-125">Rapports et audit de conformité</span><span class="sxs-lookup"><span data-stu-id="bc7af-125">Compliance Audit and Reports</span></span>

    -   <span data-ttu-id="bc7af-126">Serveur d’administration et de surveillance</span><span class="sxs-lookup"><span data-stu-id="bc7af-126">Administration and Monitoring Server</span></span>

    -   <span data-ttu-id="bc7af-127">Modèle de stratégie de groupe MBAM</span><span class="sxs-lookup"><span data-stu-id="bc7af-127">MBAM Group Policy Template</span></span>

    <span data-ttu-id="bc7af-128">**Remarques**  L’Assistant installation vérifie la configuration requise pour votre installation et affiche les conditions préalables manquantes.</span><span class="sxs-lookup"><span data-stu-id="bc7af-128">**Note** The installation wizard checks the prerequisites for your installation and displays the prerequisites that are missing.</span></span> <span data-ttu-id="bc7af-129">Si toutes les conditions préalables sont remplies, l’installation continue.</span><span class="sxs-lookup"><span data-stu-id="bc7af-129">If all the prerequisites are met, the installation continues.</span></span> <span data-ttu-id="bc7af-130">Si un prérequis manquant est détecté, vous devez résoudre les conditions préalables manquantes, puis cliquez à **nouveau sur vérifier les conditions préalables**.</span><span class="sxs-lookup"><span data-stu-id="bc7af-130">If a missing prerequisite is detected, you must resolve the missing prerequisites, and then click **Check prerequisites again**.</span></span> <span data-ttu-id="bc7af-131">Une fois que toutes les conditions préalables sont remplies, l’installation reprend.</span><span class="sxs-lookup"><span data-stu-id="bc7af-131">After all prerequisites are met, the installation resumes.</span></span>

     

4.  <span data-ttu-id="bc7af-132">Vous êtes invité à configurer la sécurité des communications réseau.</span><span class="sxs-lookup"><span data-stu-id="bc7af-132">You are prompted to configure the network communication security.</span></span> <span data-ttu-id="bc7af-133">MBAM peut crypter la communication entre la base de données de récupération et de matériel, le serveur d’administration et de surveillance, ainsi que les clients.</span><span class="sxs-lookup"><span data-stu-id="bc7af-133">MBAM can encrypt the communication between the Recovery and Hardware Database, the Administration and Monitoring Server, and the clients.</span></span> <span data-ttu-id="bc7af-134">Si vous décidez de chiffrer la communication, vous êtes invité à sélectionner le certificat de mise en service de l’autorité qui sera utilisé pour le chiffrement.</span><span class="sxs-lookup"><span data-stu-id="bc7af-134">If you decide to encrypt the communication, you are asked to select the authority-provisioned certificate that will be used for encryption.</span></span>

5.  <span data-ttu-id="bc7af-135">Cliquez sur **Suivant** pour poursuivre.</span><span class="sxs-lookup"><span data-stu-id="bc7af-135">Click **Next** to continue.</span></span>

6.  <span data-ttu-id="bc7af-136">L’Assistant de configuration de MBAM affiche les pages d’installation correspondant aux composants sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="bc7af-136">The MBAM Setup wizard will display the installation pages for the selected features.</span></span>

**<span data-ttu-id="bc7af-137">Pour déployer les fonctionnalités du serveur MBAM</span><span class="sxs-lookup"><span data-stu-id="bc7af-137">To deploy MBAM Server features</span></span>**

1.  <span data-ttu-id="bc7af-138">Dans la fenêtre **configurer la base de données de récupération et de matériel** , spécifiez l’instance de SQL Server et le nom de la base de données qui stockera les données de récupération et de matériel.</span><span class="sxs-lookup"><span data-stu-id="bc7af-138">In the **Configure the Recovery and Hardware database** window, specify the instance of SQL Server and the name of the database that will store the recovery and hardware data.</span></span> <span data-ttu-id="bc7af-139">Vous devez également spécifier l’emplacement des fichiers de base de données et l’emplacement des informations de journal.</span><span class="sxs-lookup"><span data-stu-id="bc7af-139">You must also specify both the database files location and the log information location.</span></span>

2.  <span data-ttu-id="bc7af-140">Cliquez sur **Suivant** pour poursuivre.</span><span class="sxs-lookup"><span data-stu-id="bc7af-140">Click **Next** to continue.</span></span>

3.  <span data-ttu-id="bc7af-141">Dans la fenêtre **configuration de la conformité et de la base de données d’audit** , spécifiez l’instance de SQL Server, ainsi que le nom de la base de données qui stockera les données d’audit et de conformité.</span><span class="sxs-lookup"><span data-stu-id="bc7af-141">In the **Configure the Compliance and Audit database** window, specify the instance of the SQL Server and the name of the database that will store the compliance and audit data.</span></span> <span data-ttu-id="bc7af-142">Spécifiez ensuite l’emplacement des fichiers de base de données et l’emplacement des informations de journal.</span><span class="sxs-lookup"><span data-stu-id="bc7af-142">Then, specify the database files location and the log information location.</span></span>

4.  <span data-ttu-id="bc7af-143">Cliquez sur **Suivant** pour poursuivre.</span><span class="sxs-lookup"><span data-stu-id="bc7af-143">Click **Next** to continue.</span></span>

5.  <span data-ttu-id="bc7af-144">Dans la fenêtre **rapports de conformité et d’audit** , spécifiez l’instance de service de rapport qui sera utilisée et attribuez un compte d’utilisateur de domaine pour accéder à la base de données.</span><span class="sxs-lookup"><span data-stu-id="bc7af-144">In the **Compliance and Audit Reports** window, specify the report service instance that will be used and provide a domain user account for accessing the database.</span></span> <span data-ttu-id="bc7af-145">Il doit s’agir d’un compte d’utilisateur configuré spécifiquement pour cette utilisation.</span><span class="sxs-lookup"><span data-stu-id="bc7af-145">This should be a user account that is provisioned specifically for this use.</span></span> <span data-ttu-id="bc7af-146">Le compte d’utilisateur doit être en mesure d’accéder à toutes les données disponibles dans le groupe utilisateurs de reports MBAM.</span><span class="sxs-lookup"><span data-stu-id="bc7af-146">The user account should be able to access all data available to the MBAM Reports Users group.</span></span>

6.  <span data-ttu-id="bc7af-147">Cliquez sur **Suivant** pour poursuivre.</span><span class="sxs-lookup"><span data-stu-id="bc7af-147">Click **Next** to continue.</span></span>

7.  <span data-ttu-id="bc7af-148">Dans la fenêtre **configurer le serveur d’administration et de surveillance** , entrez la **liaison de port**, le nom d' **hôte** (facultatif) et le **chemin d’installation** du serveur d’administration et de surveillance MBAM.</span><span class="sxs-lookup"><span data-stu-id="bc7af-148">In the **Configure the Administration and Monitoring Server** window, enter the **Port Binding**, the **Host Name** (optional), and the **Installation Path** for the MBAM Administration and Monitoring server.</span></span>

    <span data-ttu-id="bc7af-149">**Avertissement**  Le numéro de port que vous spécifiez doit être un numéro de port inutilisé sur le serveur d’administration et de surveillance, sauf s’il s’agit d’un nom d’en-tête d’hôte unique.</span><span class="sxs-lookup"><span data-stu-id="bc7af-149">**Warning** The port number that you specify must be an unused port number on the Administration and Monitoring server, unless a unique host header name is specified.</span></span>

     

8.  <span data-ttu-id="bc7af-150">Cliquez sur **Suivant** pour poursuivre.</span><span class="sxs-lookup"><span data-stu-id="bc7af-150">Click **Next** to continue.</span></span>

9.  <span data-ttu-id="bc7af-151">Indiquez si vous souhaitez utiliser les mises à jour de Microsoft pour renforcer la sécurité de votre ordinateur, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="bc7af-151">Specify whether to use Microsoft Updates to help keep your computer secure, and then click **Next**.</span></span> <span data-ttu-id="bc7af-152">L’option Microsoft Updates n’active pas les mises à jour automatiques dans Windows.</span><span class="sxs-lookup"><span data-stu-id="bc7af-152">The Microsoft Updates option does not turn on the Automatic Updates in Windows.</span></span>

10. <span data-ttu-id="bc7af-153">Lorsque l’Assistant installation a collecté les informations de fonctionnalité nécessaires, l’installation MBAM est prête à démarrer.</span><span class="sxs-lookup"><span data-stu-id="bc7af-153">When the Setup wizard has collected the necessary feature information, the MBAM installation is ready to start.</span></span> <span data-ttu-id="bc7af-154">Cliquez sur **retour** pour revenir à l’Assistant pour consulter ou modifier vos paramètres d’installation.</span><span class="sxs-lookup"><span data-stu-id="bc7af-154">Click **Back** to move back through the wizard if you want to review or change your installation settings.</span></span> <span data-ttu-id="bc7af-155">Cliquez sur **installer** pour lancer l’installation.</span><span class="sxs-lookup"><span data-stu-id="bc7af-155">Click **Install** to begin the installation.</span></span> <span data-ttu-id="bc7af-156">Cliquez sur **Annuler** pour quitter le programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="bc7af-156">Click **Cancel** to exit Setup.</span></span> <span data-ttu-id="bc7af-157">Le programme d’installation installe les fonctionnalités de MBAM et vous signale que l’installation est terminée.</span><span class="sxs-lookup"><span data-stu-id="bc7af-157">Setup installs the MBAM features and notifies you that the installation is completed.</span></span>

11. <span data-ttu-id="bc7af-158">Cliquez sur **Terminer** pour quitter l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="bc7af-158">Click **Finish** to exit the wizard.</span></span>

12. <span data-ttu-id="bc7af-159">Après avoir installé les fonctionnalités du serveur MBAM, vous devez ajouter des utilisateurs aux rôles MBAM.</span><span class="sxs-lookup"><span data-stu-id="bc7af-159">After you install MBAM server features, you must add users to the MBAM roles.</span></span> <span data-ttu-id="bc7af-160">Pour plus d’informations, reportez-vous [à planification des rôles d’administrateur MBAM 1,0](planning-for-mbam-10-administrator-roles.md).</span><span class="sxs-lookup"><span data-stu-id="bc7af-160">For more information, see [Planning for MBAM 1.0 Administrator Roles](planning-for-mbam-10-administrator-roles.md).</span></span>

**<span data-ttu-id="bc7af-161">Pour effectuer une configuration de post-installation</span><span class="sxs-lookup"><span data-stu-id="bc7af-161">To perform post installation configuration</span></span>**

1.  <span data-ttu-id="bc7af-162">Une fois l’installation terminée, vous devez ajouter des rôles d’utilisateur afin de permettre aux utilisateurs d’accéder aux fonctionnalités dans le site Web d’administration MBAM.</span><span class="sxs-lookup"><span data-stu-id="bc7af-162">After Setup is finished, you must add user roles so that you can give users access to features in the MBAM administration website.</span></span> <span data-ttu-id="bc7af-163">Sur le serveur d’administration et de surveillance, ajoutez des utilisateurs aux groupes locaux suivants:</span><span class="sxs-lookup"><span data-stu-id="bc7af-163">On the Administration and Monitoring Server, add users to the following local groups:</span></span>

    -   <span data-ttu-id="bc7af-164">**Utilisateurs matériels MBAM**: les membres de ce groupe local peuvent accéder à la fonctionnalité matérielle dans le site Web d’administration MBAM.</span><span class="sxs-lookup"><span data-stu-id="bc7af-164">**MBAM Hardware Users**: Members of this local group can access the Hardware feature in the MBAM administration website.</span></span>

    -   <span data-ttu-id="bc7af-165">**Utilisateurs du support technique MBAM**: les membres de ce groupe local peuvent accéder à la récupération du lecteur et gérer les fonctionnalités du TPM dans le site Web d’administration MBAM.</span><span class="sxs-lookup"><span data-stu-id="bc7af-165">**MBAM Helpdesk Users**: Members of this local group can access the Drive Recovery and Manage TPM features in the MBAM administration website.</span></span> <span data-ttu-id="bc7af-166">Pour un utilisateur du support technique, tous les champs de la récupération de lecteur et de la gestion de TPM sont obligatoires.</span><span class="sxs-lookup"><span data-stu-id="bc7af-166">All fields in Drive Recovery and Manage TPM are required fields for a Helpdesk User.</span></span>

    -   <span data-ttu-id="bc7af-167">**Utilisateurs expérimentés du support technique MBAM**: les membres de ce groupe local disposent d’un accès avancé aux fonctionnalités de récupération de lecteur et de gestion des composants de plateforme dans le site Web d’administration MBAM.</span><span class="sxs-lookup"><span data-stu-id="bc7af-167">**MBAM Advanced Helpdesk Users**: Members of this local group have advanced access to the Drive Recovery and Manage TPM features in the MBAM administration website.</span></span> <span data-ttu-id="bc7af-168">Pour les utilisateurs expérimentés du support technique, seul le champ ID clé est requis pour la récupération du lecteur.</span><span class="sxs-lookup"><span data-stu-id="bc7af-168">For Advanced Helpdesk Users, only the Key ID field is required in Drive Recovery.</span></span> <span data-ttu-id="bc7af-169">Pour gérer les utilisateurs de GPC, seuls le champ domaine de l’ordinateur et le champ nom de l’ordinateur sont obligatoires.</span><span class="sxs-lookup"><span data-stu-id="bc7af-169">For Manage TPM users, only the Computer Domain field and Computer Name field are required.</span></span>

2.  <span data-ttu-id="bc7af-170">Sur la base de données d’administration et de surveillance du serveur, de la conformité et de l’audit, et de l’ordinateur qui héberge les rapports de conformité et d’audit, ajoutez des utilisateurs au groupe local suivant pour leur permettre d’accéder à la fonctionnalité rapports dans le site Web d’administration MBAM:</span><span class="sxs-lookup"><span data-stu-id="bc7af-170">On the Administration and Monitoring Server, Compliance and Audit Database, and on the computer that hosts the Compliance and Audit Reports, add users to the following local group to enable them to access the Reports feature in the MBAM administration website:</span></span>

    -   <span data-ttu-id="bc7af-171">**Utilisateurs du rapport MBAM**: les membres de ce groupe local peuvent accéder aux fonctionnalités de rapport dans le site Web d’administration MBAM.</span><span class="sxs-lookup"><span data-stu-id="bc7af-171">**MBAM Report Users**: Members of this local group can access the Reports features in the MBAM administration website.</span></span>

    <span data-ttu-id="bc7af-172">**Remarques**  Il est possible de mettre à jour les membres d’une appartenance à un groupe ou d’une appartenance de groupe du groupe local du **rapport MBAM** sur tous les ordinateurs sur lesquels les rapports d’administration et de surveillance des fonctionnalités du serveur</span><span class="sxs-lookup"><span data-stu-id="bc7af-172">**Note** Identical user membership or group membership of the **MBAM Report Users** local group must be maintained on all computers where the Administration and Monitoring Server features, Compliance and Audit Database, and Compliance and Audit Reports are installed.</span></span>

    <span data-ttu-id="bc7af-173">Pour conserver une appartenance identique sur tous les ordinateurs, vous devez créer un groupe de sécurité de domaine et ajouter ce groupe de domaine à chaque groupe utilisateurs de rapports MBAM locaux.</span><span class="sxs-lookup"><span data-stu-id="bc7af-173">To maintain identical memberships on all computers, you should create a domain security group and add that domain group to each local MBAM Report Users group.</span></span> <span data-ttu-id="bc7af-174">Lorsque vous procédez ainsi, vous pouvez gérer l’appartenance à un groupe à l’aide du groupe de domaines.</span><span class="sxs-lookup"><span data-stu-id="bc7af-174">When you do this, you can manage the group memberships by using the domain group.</span></span>

     

## <span data-ttu-id="bc7af-175">Validation de l’installation de la fonctionnalité MBAM Server</span><span class="sxs-lookup"><span data-stu-id="bc7af-175">Validating the MBAM Server feature installation</span></span>


<span data-ttu-id="bc7af-176">À l’issue de l’installation d’MBAM, vérifiez que l’installation a correctement configuré toutes les fonctionnalités MBAM nécessaires pour la gestion de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="bc7af-176">When the MBAM installation is complete, validate that the installation has successfully set up all the necessary MBAM features that are required for BitLocker management.</span></span> <span data-ttu-id="bc7af-177">Utilisez la procédure suivante pour vérifier que le service MBAM fonctionne:</span><span class="sxs-lookup"><span data-stu-id="bc7af-177">Use the following procedure to confirm that the MBAM service is functional:</span></span>

**<span data-ttu-id="bc7af-178">Pour valider l’installation de la fonctionnalité MBAM Server</span><span class="sxs-lookup"><span data-stu-id="bc7af-178">To validate MBAM Server feature installation</span></span>**

1. <span data-ttu-id="bc7af-179">Sur chaque serveur sur lequel est déployée une fonctionnalité MBAM, ouvrez **le panneau de configuration**.</span><span class="sxs-lookup"><span data-stu-id="bc7af-179">On each server where an MBAM feature is deployed, open **Control Panel**.</span></span> <span data-ttu-id="bc7af-180">Cliquez sur **programmes**, puis sur **programmes et fonctionnalités**.</span><span class="sxs-lookup"><span data-stu-id="bc7af-180">Click **Programs**, and then click **Programs and Features**.</span></span> <span data-ttu-id="bc7af-181">Vérifiez que la fonctionnalité **administration et analyse de BitLocker Microsoft** s’affiche dans la liste **programmes et fonctionnalités** .</span><span class="sxs-lookup"><span data-stu-id="bc7af-181">Verify that **Microsoft BitLocker Administration and Monitoring** appears in the **Programs and Features** list.</span></span>

   **<span data-ttu-id="bc7af-182">Remarque</span><span class="sxs-lookup"><span data-stu-id="bc7af-182">Note</span></span>**  
   <span data-ttu-id="bc7af-183">Pour valider l’installation, vous devez utiliser un compte de domaine disposant d’informations d’identification d’administrateur local sur chaque serveur.</span><span class="sxs-lookup"><span data-stu-id="bc7af-183">To validate the installation, you must use a Domain Account that has local computer administrative credentials on each server.</span></span>

     

2. <span data-ttu-id="bc7af-184">Sur le serveur sur lequel la base de données de récupération et de matériel est installée, ouvrez SQL Server Management Studio, puis vérifiez que la base de données **MBAM et de récupération** de la base de données est installée.</span><span class="sxs-lookup"><span data-stu-id="bc7af-184">On the server where the Recovery and Hardware Database is installed, open SQL Server Management Studio and verify that the **MBAM Recovery and Hardware** database is installed.</span></span>

3. <span data-ttu-id="bc7af-185">Sur le serveur sur lequel la base de données d’audit et de conformité est installée, ouvrez SQL Server Management Studio, puis vérifiez que la **base de données d’audit et de conformité MBAM** est installée.</span><span class="sxs-lookup"><span data-stu-id="bc7af-185">On the server where the Compliance and Audit Database is installed, open SQL Server Management Studio and verify that the **MBAM Compliance and Audit Database** is installed.</span></span>

4. <span data-ttu-id="bc7af-186">Sur le serveur sur lequel sont installés les rapports de conformité et d’audit, ouvrez un navigateur Web doté de privilèges d’administration et naviguez jusqu’au site «Home» du site SQL Server Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="bc7af-186">On the server where the Compliance and Audit Reports are installed, open a web browser with administrative privileges and browse to the “Home” of the SQL Server Reporting Services site.</span></span>

   <span data-ttu-id="bc7af-187">L’emplacement d’accueil par défaut d’une instance de site SQL Server Reporting Services se trouve sur http:// <em> &lt; NameofMBAMReportsServer &gt; </em> /reports.</span><span class="sxs-lookup"><span data-stu-id="bc7af-187">The default Home location of a SQL Server Reporting Services site instance is at http://<em>&lt;NameofMBAMReportsServer&gt;</em>/Reports.</span></span> <span data-ttu-id="bc7af-188">Pour trouver l’URL réelle, utilisez l’outil Gestionnaire de configuration Reporting Services et sélectionnez les instances spécifiées lors de l’installation.</span><span class="sxs-lookup"><span data-stu-id="bc7af-188">To find the actual URL, use the Reporting Services Configuration Manager tool and select the instances specified during setup.</span></span>

   <span data-ttu-id="bc7af-189">Vérifiez qu’un dossier nommé **rapports de conformité Malte** figure et qu’il contient cinq rapports et une seule source de données.</span><span class="sxs-lookup"><span data-stu-id="bc7af-189">Confirm that a folder named **Malta Compliance Reports** is listed and that it contains five reports and one data source.</span></span>

   **<span data-ttu-id="bc7af-190">Remarque</span><span class="sxs-lookup"><span data-stu-id="bc7af-190">Note</span></span>**  
   <span data-ttu-id="bc7af-191">Si SQL Server Reporting Services a été configuré en tant qu’instance nommée, l’URL doit ressembler à ce qui suit: http://\* &lt; NameofMBAMReportsServer &gt; */Reports\_* &lt; SRSInstanceName &gt; \*</span><span class="sxs-lookup"><span data-stu-id="bc7af-191">If SQL Server Reporting Services was configured as a named instance, the URL should resemble the following:http://*&lt;NameofMBAMReportsServer&gt;*/Reports\_*&lt;SRSInstanceName&gt;*</span></span>

     

5. <span data-ttu-id="bc7af-192">Sur le serveur sur lequel est installé la fonctionnalité d’administration et de surveillance, exécutez le **Gestionnaire de serveur** et naviguez jusqu’à **rôles**, sélectionnez **serveur Web (IIS)**, puis cliquez sur **Gestionnaire des services Internet (IIS)** .</span><span class="sxs-lookup"><span data-stu-id="bc7af-192">On the server where the Administration and Monitoring feature is installed, run **Server Manager** and browse to **Roles**, select **Web Server (IIS)**, and click **Internet Information Services (IIS) Manager**</span></span>

6. <span data-ttu-id="bc7af-193">Dans **connexions**, naviguez jusqu’à \* &lt; nomordinateur &gt; \*, sélectionnez **sites**, puis l’option **administration et analyse de Microsoft BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="bc7af-193">In **Connections**, browse to *&lt;computername&gt;*, select **Sites**, and select **Microsoft BitLocker Administration and Monitoring**.</span></span> <span data-ttu-id="bc7af-194">Vérifiez que **MBAMAdministrationService**, **MBAMComplianceStatusService**et **MBAMRecoveryAndHardwareService** apparaissent.</span><span class="sxs-lookup"><span data-stu-id="bc7af-194">Verify that **MBAMAdministrationService**, **MBAMComplianceStatusService**, and **MBAMRecoveryAndHardwareService** are listed.</span></span>

7. <span data-ttu-id="bc7af-195">Sur le serveur sur lequel est installé la fonctionnalité d’administration et de contrôle, ouvrez un navigateur Web avec des privilèges d’administration, puis accédez aux emplacements suivants dans le site Web MBAM pour vérifier qu’ils se chargent correctement:</span><span class="sxs-lookup"><span data-stu-id="bc7af-195">On the server where the Administration and Monitoring feature is installed, open a web browser with administrative privileges, and then browse to the following locations in the MBAM website to verify that they load successfully:</span></span>

   -   <span data-ttu-id="bc7af-196">*http:// &lt; nomordinateur &gt; /default.aspx* et confirmez chacun des liens pour la navigation et les rapports</span><span class="sxs-lookup"><span data-stu-id="bc7af-196">*http://&lt;computername&gt;/default.aspx* and confirm each of the links for navigation and reports</span></span>

   -   *<span data-ttu-id="bc7af-197">http:// &lt; nomordinateur &gt; /MBAMAdministrationService/AdministrationService.svc</span><span class="sxs-lookup"><span data-stu-id="bc7af-197">http://&lt;computername&gt;/MBAMAdministrationService/AdministrationService.svc</span></span>*

   -   *<span data-ttu-id="bc7af-198">http:// &lt; nomordinateur &gt; /MBAMComplianceStatusService/StatusReportingService.svc</span><span class="sxs-lookup"><span data-stu-id="bc7af-198">http://&lt;computername&gt;/MBAMComplianceStatusService/StatusReportingService.svc</span></span>*

   -   *<span data-ttu-id="bc7af-199">http:// &lt; nomordinateur &gt; /MBAMRecoveryAndHardwareService/CoreService.svc</span><span class="sxs-lookup"><span data-stu-id="bc7af-199">http://&lt;computername&gt;/MBAMRecoveryAndHardwareService/CoreService.svc</span></span>*

   **<span data-ttu-id="bc7af-200">Remarque</span><span class="sxs-lookup"><span data-stu-id="bc7af-200">Note</span></span>**  
   <span data-ttu-id="bc7af-201">En général, les services sont installés sur le port 80 par défaut sans chiffrement réseau.</span><span class="sxs-lookup"><span data-stu-id="bc7af-201">Typically, the services are installed on the default port 80 without network encryption.</span></span> <span data-ttu-id="bc7af-202">Si les services sont installés sur un autre port, modifiez les URL pour inclure le port approprié.</span><span class="sxs-lookup"><span data-stu-id="bc7af-202">If the services are installed on a different port, change the URLs to include the appropriate port.</span></span> <span data-ttu-id="bc7af-203">Par exemple, http://\* &lt; nomordinateur &gt; : &lt; port &gt; \*/default.aspx ou http:// <em> &lt; hostheadername &gt; / </em> default. aspx.</span><span class="sxs-lookup"><span data-stu-id="bc7af-203">For example, http://*&lt;computername&gt;:&lt;port&gt;*/default.aspx or http://<em>&lt;hostheadername&gt;/</em>default.aspx.</span></span>

   <span data-ttu-id="bc7af-204">Si les services sont installés en utilisant le chiffrement réseau, modifiez http://sur https://.</span><span class="sxs-lookup"><span data-stu-id="bc7af-204">If the services are installed with network encryption, change http:// to https://.</span></span>

     

## <span data-ttu-id="bc7af-205">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bc7af-205">Related topics</span></span>


[<span data-ttu-id="bc7af-206">Déploiement de l'infrastructure de serveur MBAM1.0</span><span class="sxs-lookup"><span data-stu-id="bc7af-206">Deploying the MBAM 1.0 Server Infrastructure</span></span>](deploying-the-mbam-10-server-infrastructure.md)

 

 





