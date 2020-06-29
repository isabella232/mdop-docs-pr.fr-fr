---
title: Mise à niveau des versions précédentes de MBAM
description: Mise à niveau des versions précédentes de MBAM
author: dansimp
ms.assetid: 73b425cf-9cd9-4ebc-a35e-1b3bf18596ce
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: af45d193a5e8001288e70389ff220cb5d8269918
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810176"
---
# <span data-ttu-id="be4cb-103">Mise à niveau des versions précédentes de MBAM</span><span class="sxs-lookup"><span data-stu-id="be4cb-103">Upgrading from Previous Versions of MBAM</span></span>


<span data-ttu-id="be4cb-104">Vous pouvez mettre à niveau l’administration et la surveillance de Microsoft BitLocker (MBAM) vers MBAM 2.0, avec la topologie autonome ou la topologie de Configuration Manager, en procédant comme suit:</span><span class="sxs-lookup"><span data-stu-id="be4cb-104">You can upgrade Microsoft BitLocker Administration and Monitoring (MBAM) to MBAM2.0, with the Stand-alone topology or Configuration Manager topology, by doing the following:</span></span>

-   <span data-ttu-id="be4cb-105">**Remplacement manuel du serveur sur place** : pour mettre à niveau le serveur MBAM, désinstallez MBAM manuellement à l’aide du programme d’installation ou du panneau de configuration, puis installez l’infrastructure MBAM 2.0.</span><span class="sxs-lookup"><span data-stu-id="be4cb-105">**Manual in-place server replacement** – To upgrade the MBAM Server, manually uninstall MBAM by using either the installer or Control Panel, and then install the MBAM2.0 infrastructure.</span></span> <span data-ttu-id="be4cb-106">Vous n’avez pas besoin de supprimer les bases de données.</span><span class="sxs-lookup"><span data-stu-id="be4cb-106">You do not have to remove the databases.</span></span> <span data-ttu-id="be4cb-107">La désinstallation du serveur MBAM 1,0 quitte les bases de données MBAM intactes.</span><span class="sxs-lookup"><span data-stu-id="be4cb-107">Uninstalling the MBAM 1.0 Server leaves the MBAM databases intact.</span></span> <span data-ttu-id="be4cb-108">Si vous spécifiez les mêmes bases de données que MBAM 1,0, l’installation de MBAM 2.0 conserve les données 1,0 MBAM dans les bases de données et convertit les bases de données pour qu’elles fonctionnent avec MBAM 2.0.</span><span class="sxs-lookup"><span data-stu-id="be4cb-108">If you specify the same databases that MBAM 1.0 was using, the MBAM2.0 installation retains MBAM 1.0 data in the databases and converts the databases to work with MBAM2.0.</span></span>

-   <span data-ttu-id="be4cb-109">**Mise à niveau du client distribué** : Si vous utilisez la topologie MBAM autonome, vous pouvez mettre à niveau les clients MBAM progressivement après l’installation de l’infrastructure du serveur MBAM 2,0.</span><span class="sxs-lookup"><span data-stu-id="be4cb-109">**Distributed Client Upgrade** - If you are using the Stand-alone MBAM topology, you can upgrade the MBAM Clients gradually after you install the MBAM 2.0 Server infrastructure.</span></span> <span data-ttu-id="be4cb-110">Le serveur MBAM 2,0 détecte la version du client existant et effectue les étapes requises pour effectuer une mise à niveau vers le client 2,0.</span><span class="sxs-lookup"><span data-stu-id="be4cb-110">The MBAM 2.0 Server detects the version of the existing Client and performs the required steps to upgrade to the 2.0 Client.</span></span>

    <span data-ttu-id="be4cb-111">Après avoir effectué la mise à niveau de l’infrastructure du serveur MBAM 2,0, les clients MBAM 1,0 continuent de signaler au serveur MBAM 2,0 les données de récupération par confiance, mais la conformité sera basée sur les stratégies de MBAM 1,0.</span><span class="sxs-lookup"><span data-stu-id="be4cb-111">After you upgrade the MBAM 2.0 Server infrastructure, MBAM 1.0 Clients continue to report to the MBAM 2.0 Server successfully, escrowing recovery data, but compliance will be based on the policies in MBAM 1.0.</span></span> <span data-ttu-id="be4cb-112">Vous devez mettre à niveau des clients vers MBAM 2,0 pour que les ordinateurs clients signalent de manière précise la conformité par rapport aux stratégies 2,0 MBAM.</span><span class="sxs-lookup"><span data-stu-id="be4cb-112">You must upgrade clients to MBAM 2.0 to have client computers accurately report compliance against the MBAM 2.0 policies.</span></span> <span data-ttu-id="be4cb-113">Vous pouvez mettre à niveau les clients vers le client MBAM 2,0 sans désinstaller le client précédent, et le client doit commencer à appliquer et à signaler les stratégies 2,0 MBAM.</span><span class="sxs-lookup"><span data-stu-id="be4cb-113">You can upgrade the clients to the MBAM 2.0 Client without uninstalling the previous client, and the client will start to apply and report MBAM 2.0 policies.</span></span>

    <span data-ttu-id="be4cb-114">Si vous utilisez MBAM avec Configuration Manager, vous devez mettre à niveau les clients 1,0 MBAM vers MBAM 2,0.</span><span class="sxs-lookup"><span data-stu-id="be4cb-114">If you are using MBAM with Configuration Manager, you must upgrade the MBAM 1.0 clients to MBAM 2.0.</span></span>

## <span data-ttu-id="be4cb-115">Mise à niveau de MBAM à partir d’une architecture à deux serveurs</span><span class="sxs-lookup"><span data-stu-id="be4cb-115">Upgrading MBAM from a Two-Server Architecture</span></span>


<span data-ttu-id="be4cb-116">Utilisez les instructions suivantes pour effectuer une mise à niveau à partir d’une version précédente de MBAM lorsque vous utilisez une architecture à deux serveurs, où un serveur héberge les composants Microsoft SQL Server, et l’autre serveur héberge les services et sites Web.</span><span class="sxs-lookup"><span data-stu-id="be4cb-116">Use the following instructions to upgrade from a previous version of MBAM when you are using a two-server architecture, where one server is hosting the Microsoft SQL Server components, and the other server is hosting the websites and services.</span></span>

**<span data-ttu-id="be4cb-117">Pour mettre à niveau MBAM à partir d’une architecture à deux serveurs</span><span class="sxs-lookup"><span data-stu-id="be4cb-117">To upgrade MBAM from a two-server architecture</span></span>**

1.  <span data-ttu-id="be4cb-118">Sur le serveur avec les fonctionnalités de SQL Server, dans le panneau de configuration, sélectionnez **programmes et fonctionnalités**, puis désinstallez l' **administration et la surveillance de Microsoft BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="be4cb-118">On the server with the SQL Server features, in Control Panel, select **Programs and Features**, and then uninstall **Microsoft BitLocker Administration and Monitoring**.</span></span> <span data-ttu-id="be4cb-119">La base de données de récupération et la base de données d’audit et de conformité restent inchangées.</span><span class="sxs-lookup"><span data-stu-id="be4cb-119">The Recovery Database and Compliance and Audit database remain unchanged.</span></span>

2.  <span data-ttu-id="be4cb-120">Exécutez **MBAMSetup.exe** pour la version MBAM 2,0, si vous le souhaitez, sélectionnez le **programme d’amélioration**du produit, puis cliquez sur **Démarrer**.</span><span class="sxs-lookup"><span data-stu-id="be4cb-120">Run **MBAMSetup.exe** for version MBAM 2.0, optionally select the **Customer Experience Improvement Program**, and then click **Start**.</span></span>

3.  <span data-ttu-id="be4cb-121">Lisez et acceptez le contrat de licence logiciel Microsoft, puis cliquez sur **suivant** pour continuer l’installation.</span><span class="sxs-lookup"><span data-stu-id="be4cb-121">Read and accept the Microsoft Software License Agreement, and then click **Next** to continue the installation.</span></span>

4.  <span data-ttu-id="be4cb-122">Dans la page de sélection de la **topologie** , sélectionnez la topologie d’intégration **autonome** ou **System Center Configuration Manager** , puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="be4cb-122">On the **Topology Selection** page, select the **Stand-alone** or **System Center Configuration Manager Integration** topology, and then click **Next**.</span></span>

5.  <span data-ttu-id="be4cb-123">Dans la page **Sélectionner les fonctionnalités à installer** , décochez la case **serveur libre-service** et fonctionnalités du **serveur d’administration** et de surveillance, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="be4cb-123">On the **Select features to install** page, clear the **Self-Service Server** and **Administration and Monitoring Server** features, and then click **Next**.</span></span>

6.  <span data-ttu-id="be4cb-124">Attendez la fin de la vérification préalable, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="be4cb-124">Wait for the prerequisite checks to finish, and then click **Next**.</span></span> <span data-ttu-id="be4cb-125">Si une prérequis manquante est détecté, résolvez les conditions préalables manquantes, puis cliquez **à nouveau sur vérifier les conditions préalables**.</span><span class="sxs-lookup"><span data-stu-id="be4cb-125">If a missing prerequisite is detected, resolve the missing prerequisites, and then click **Check prerequisites again**.</span></span>

7.  <span data-ttu-id="be4cb-126">Sur la page **fournir le compte utilisé pour accéder à la base de données MBAM** , indiquez le nom de l’ordinateur qui hébergera les sites et services, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="be4cb-126">On the **Provide account used to access the MBAM databases** page, provide the computer name for the server that will host the sites and services, and then click **Next**.</span></span>

8.  <span data-ttu-id="be4cb-127">Sur la page **configurer la base de données de récupération** , spécifiez le nom de l’instance SQL Server et le nom de la base de données qui stockera les données de récupération.</span><span class="sxs-lookup"><span data-stu-id="be4cb-127">On the **Configure the Recovery database** page, specify the SQL Server instance name and the name of the database that will store the recovery data.</span></span> <span data-ttu-id="be4cb-128">Vous devez également spécifier l’emplacement où se trouvent les fichiers de base de données et les informations de journalisation.</span><span class="sxs-lookup"><span data-stu-id="be4cb-128">You must also specify where the database files and log information will be located.</span></span>

9.  <span data-ttu-id="be4cb-129">Cliquez sur **Suivant** pour poursuivre.</span><span class="sxs-lookup"><span data-stu-id="be4cb-129">Click **Next** to continue.</span></span>

10. <span data-ttu-id="be4cb-130">Sur la page **configurer la conformité et la base de données d’audit** , spécifiez le nom de l’instance SQL Server et le nom de la base de données qui stockera les données de conformité et d’audit.</span><span class="sxs-lookup"><span data-stu-id="be4cb-130">On the **Configure the Compliance and Audit database** page, specify the SQL Server instance name and the name of the database that will store the compliance and audit data.</span></span>

11. <span data-ttu-id="be4cb-131">Cliquez sur **Suivant** pour poursuivre.</span><span class="sxs-lookup"><span data-stu-id="be4cb-131">Click **Next** to continue.</span></span>

12. <span data-ttu-id="be4cb-132">Sur la page **configurer les rapports de conformité et d’audit** , spécifiez l’instance de SQL Server Reporting Services dans laquelle les rapports de conformité et d’audit seront installés, puis fournissez un compte d’utilisateur et un mot de passe de domaine pour accéder à la base de données d’audit et de conformité.</span><span class="sxs-lookup"><span data-stu-id="be4cb-132">On the **Configure the Compliance and Audit Reports** page, specify the SQL Server Reporting Services instance where the Compliance and Audit reports will be installed, and provide a domain user account and password to access the Compliance and Audit database.</span></span> <span data-ttu-id="be4cb-133">Configurez le mot de passe de ce compte pour qu’il n’expire jamais.</span><span class="sxs-lookup"><span data-stu-id="be4cb-133">Configure the password for this account to never expire.</span></span> <span data-ttu-id="be4cb-134">Le compte d’utilisateur peut accéder à toutes les données disponibles dans le groupe utilisateurs de reports MBAM.</span><span class="sxs-lookup"><span data-stu-id="be4cb-134">The user account can access all data available to the MBAM Reports Users group.</span></span>

13. <span data-ttu-id="be4cb-135">Cliquez sur **Suivant** pour poursuivre.</span><span class="sxs-lookup"><span data-stu-id="be4cb-135">Click **Next** to continue.</span></span>

14. <span data-ttu-id="be4cb-136">Indiquez si vous souhaitez utiliser les mises à jour de Microsoft pour renforcer la sécurité de votre ordinateur, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="be4cb-136">Specify whether to use Microsoft Updates to help keep your computer secure, and then click **Next**.</span></span> <span data-ttu-id="be4cb-137">Les mises à jour automatiques ne sont pas activées dans Windows.</span><span class="sxs-lookup"><span data-stu-id="be4cb-137">This does not turn on Automatic Updates in Windows.</span></span> <span data-ttu-id="be4cb-138">Si vous avez précédemment choisi d’utiliser Microsoft Update pour ce produit ou un autre produit, la page Microsoft Update ne s’affiche pas.</span><span class="sxs-lookup"><span data-stu-id="be4cb-138">If you previously chose to use Microsoft Update for this product or another product, the Microsoft Update page does not appear.</span></span>

15. <span data-ttu-id="be4cb-139">Dans la page Résumé de l' **installation** , passez en revue les fonctionnalités qui seront installées, puis cliquez sur **installer** pour démarrer l’installation.</span><span class="sxs-lookup"><span data-stu-id="be4cb-139">On the **Installation Summary** page, review the features that will be installed, and then click **Install** to start the installation.</span></span>

**<span data-ttu-id="be4cb-140">Pour désinstaller les fonctionnalités d’administration et de surveillance du serveur et procéder à la mise à niveau</span><span class="sxs-lookup"><span data-stu-id="be4cb-140">To uninstall the Administration and Monitoring Server features and to complete the upgrade</span></span>**

1.  <span data-ttu-id="be4cb-141">Sur l’ordinateur qui héberge les fonctionnalités d’administration et de surveillance du serveur, dans le panneau de configuration, sélectionnez **programmes et fonctionnalités**, puis désinstallez MBAM pour supprimer les services et sites Web déjà installés.</span><span class="sxs-lookup"><span data-stu-id="be4cb-141">On the computer that hosts the Administration and Monitoring Server features, in Control Panel, select **Programs and Features**, and then uninstall MBAM to remove the previously installed websites and services.</span></span>

2.  <span data-ttu-id="be4cb-142">Exécutez le **MBAMSetup.exe** pour la version 2,0, sélectionnez éventuellement le **programme d’amélioration**du produit, puis cliquez sur **Démarrer**.</span><span class="sxs-lookup"><span data-stu-id="be4cb-142">Run the **MBAMSetup.exe** for version 2.0, optionally select the **Customer Experience Improvement Program**, and then click **Start**.</span></span>

3.  <span data-ttu-id="be4cb-143">Lisez et acceptez le contrat de licence logiciel Microsoft, puis cliquez sur **suivant** pour continuer l’installation.</span><span class="sxs-lookup"><span data-stu-id="be4cb-143">Read and accept the Microsoft Software License Agreement, and then click **Next** to continue the installation.</span></span>

4.  <span data-ttu-id="be4cb-144">Dans la page de sélection de la **topologie** , sélectionnez la topologie d’intégration **autonome** ou **System Center Configuration Manager** , puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="be4cb-144">On the **Topology Selection** page, select the **Stand-alone** or **System Center Configuration Manager Integration** topology, and then click **Next**.</span></span>

5.  <span data-ttu-id="be4cb-145">Dans la **page Sélectionner les fonctionnalités à installer** , effacez les fonctionnalités de la **base de données de récupération** et **de la base de données d’audit et de** **conformité** et audit, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="be4cb-145">On the **Select features to install** page, clear the **Recovery Database** and **Compliance and Audit Database** and **Compliance and Audit Reports** features, and then click **Next**.</span></span>

6.  <span data-ttu-id="be4cb-146">Attendez la fin de la vérification préalable, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="be4cb-146">Wait for the prerequisite checks to finish, and then click **Next**.</span></span> <span data-ttu-id="be4cb-147">Si une condition préalable manquante est détectée, vous devez d’abord résoudre les conditions préalables manquantes, puis cliquez sur **vérifier les conditions préalables**.</span><span class="sxs-lookup"><span data-stu-id="be4cb-147">If a missing prerequisite is detected, resolve the missing prerequisites first, and then click **Check prerequisites again**.</span></span>

7.  <span data-ttu-id="be4cb-148">Dans la page **configurer la sécurité du réseau** , choisissez si vous souhaitez utiliser le chiffrement SSL (Secure Socket Layer) pour les services et sites Web.</span><span class="sxs-lookup"><span data-stu-id="be4cb-148">On the **Configure network communication security** page, choose whether to use Secure Socket Layer (SSL) encryption for the websites and services.</span></span> <span data-ttu-id="be4cb-149">Si vous décidez de chiffrer la communication, sélectionnez le certificat d’autorité de certification à utiliser pour le chiffrement.</span><span class="sxs-lookup"><span data-stu-id="be4cb-149">If you decide to encrypt the communication, select the certification authority (CA) certificate to use for encryption.</span></span>

    <span data-ttu-id="be4cb-150">**Remarques**  Le certificat doit être créé avant cette étape pour vous permettre de le sélectionner dans cette page.</span><span class="sxs-lookup"><span data-stu-id="be4cb-150">**Note** The certificate must be created before this step to enable you to select it on this page.</span></span>

     

8.  <span data-ttu-id="be4cb-151">Dans la page **configurer l’emplacement de la base de données d’état de conformité** , spécifiez le nom de l’instance SQL Server et le nom de la base de données qui stocke les données de conformité et d’audit.</span><span class="sxs-lookup"><span data-stu-id="be4cb-151">On the **Configure the location of the Compliance Status database** page, specify the SQL Server instance name and the name of the database that stores the compliance and audit data.</span></span> <span data-ttu-id="be4cb-152">Vous devez également spécifier l’emplacement où se trouvent les fichiers de base de données et les informations de journalisation.</span><span class="sxs-lookup"><span data-stu-id="be4cb-152">You must also specify where the database files and log information will be located.</span></span>

9.  <span data-ttu-id="be4cb-153">Cliquez sur **Suivant** pour poursuivre.</span><span class="sxs-lookup"><span data-stu-id="be4cb-153">Click **Next** to continue.</span></span>

10. <span data-ttu-id="be4cb-154">Dans la page **configurez l’emplacement de la base de données de récupération** , spécifiez le nom de l’instance SQL Server et le nom de la base de données qui stocke les données de récupération.</span><span class="sxs-lookup"><span data-stu-id="be4cb-154">On the **Configure the location of the Recovery Database** page, specify the SQL Server instance name and the name of the database that stores the recovery data.</span></span>

11. <span data-ttu-id="be4cb-155">Cliquez sur **Suivant** pour poursuivre.</span><span class="sxs-lookup"><span data-stu-id="be4cb-155">Click **Next** to continue.</span></span>

12. <span data-ttu-id="be4cb-156">Dans la page **configurer les rapports de conformité et d’audit** , entrez l’URL de l’instance de rapport que vous avez configurée sur l’autre serveur.</span><span class="sxs-lookup"><span data-stu-id="be4cb-156">On the **Configure the Compliance and Audit Reports** page, enter the URL for the reporting instance that you configured on the other server.</span></span> <span data-ttu-id="be4cb-157">Utilisez le bouton **tester** pour vérifier que vous pouvez accéder au site.</span><span class="sxs-lookup"><span data-stu-id="be4cb-157">Use the **Test** button to verify that you can reach the site.</span></span>

13. <span data-ttu-id="be4cb-158">Cliquez sur **Suivant** pour poursuivre.</span><span class="sxs-lookup"><span data-stu-id="be4cb-158">Click **Next** to continue.</span></span>

14. <span data-ttu-id="be4cb-159">Dans la page **configurer le portail libre-service** , entrez le numéro de port, le nom d’hôte, le nom du répertoire virtuel et le chemin d’installation du portail libre-service.</span><span class="sxs-lookup"><span data-stu-id="be4cb-159">On the **Configure the Self-Service Portal** page, enter the port number, host name, virtual directory name, and installation path for the Self-Service Portal.</span></span>

    <span data-ttu-id="be4cb-160">**Remarques**  Le numéro de port que vous spécifiez doit être un numéro de port inutilisé sur le serveur d’administration et de surveillance sauf si vous spécifiez un nom d’en-tête d’hôte unique.</span><span class="sxs-lookup"><span data-stu-id="be4cb-160">**Note** The port number that you specify must be an unused port number on the Administration and Monitoring Server unless you specify a unique host header name.</span></span>

     

15. <span data-ttu-id="be4cb-161">Sur la page **configurer le serveur d’administration et de surveillance** , spécifiez le répertoire virtuel souhaité pour le site Web du support technique.</span><span class="sxs-lookup"><span data-stu-id="be4cb-161">On the **Configure the Administration and Monitoring Server** page, specify the desired virtual directory for the Help Desk website.</span></span>

16. <span data-ttu-id="be4cb-162">Indiquez si vous souhaitez utiliser les mises à jour de Microsoft pour renforcer la sécurité de votre ordinateur, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="be4cb-162">Specify whether to use Microsoft Updates to help keep your computer secure, and then click **Next**.</span></span> <span data-ttu-id="be4cb-163">Cette étape n’active pas les mises à jour automatiques dans Windows.</span><span class="sxs-lookup"><span data-stu-id="be4cb-163">This step does not turn on Automatic Updates in Windows.</span></span> <span data-ttu-id="be4cb-164">Si vous avez précédemment choisi d’utiliser Microsoft Update pour ce produit ou un autre produit, la page Microsoft Update ne s’affiche pas.</span><span class="sxs-lookup"><span data-stu-id="be4cb-164">If you previously chose to use Microsoft Update for this product or another product, the Microsoft Update page does not appear.</span></span>

17. <span data-ttu-id="be4cb-165">Dans la page Résumé de l' **installation** , passez en revue les fonctionnalités qui seront installées, puis cliquez sur **installer** pour démarrer l’installation.</span><span class="sxs-lookup"><span data-stu-id="be4cb-165">On the **Installation Summary** page, review the features that will be installed, and then click **Install** to start the installation.</span></span>

18. <span data-ttu-id="be4cb-166">Pour vérifier que la mise à niveau a réussi, vérifiez que vous pouvez joindre chaque site à partir d’un autre ordinateur du domaine.</span><span class="sxs-lookup"><span data-stu-id="be4cb-166">To validate that the upgrade was successful, verify that you can reach each site from another computer in the domain.</span></span>

## <span data-ttu-id="be4cb-167">Mise à niveau du client MBAM sur les ordinateurs des utilisateurs finaux</span><span class="sxs-lookup"><span data-stu-id="be4cb-167">Upgrading the MBAM Client on End-User Computers</span></span>


<span data-ttu-id="be4cb-168">Pour mettre à niveau les ordinateurs des utilisateurs finaux vers le client MBAM 2,0, exécutez **MbamClientSetup.exe** sur chaque ordinateur client.</span><span class="sxs-lookup"><span data-stu-id="be4cb-168">To upgrade end-user computers to the MBAM 2.0 Client, run **MbamClientSetup.exe** on each client computer.</span></span> <span data-ttu-id="be4cb-169">Le programme d’installation met automatiquement à jour le client vers le client MBAM 2,0.</span><span class="sxs-lookup"><span data-stu-id="be4cb-169">The installer automatically updates the Client to the MBAM 2.0 Client.</span></span> <span data-ttu-id="be4cb-170">Vous pouvez installer le client MBAM via un système de distribution de logiciels électronique, des outils tels que les services de domaine Active Directory ou System Center Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="be4cb-170">You can install the MBAM Client through an electronic software distribution system, tools such as Active Directory Domain Services or System Center Configuration Manager.</span></span>

<span data-ttu-id="be4cb-171">Pour valider la mise à niveau du client, procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="be4cb-171">To validate the Client upgrade, do the following:</span></span>

1.  <span data-ttu-id="be4cb-172">Attendez la fin du cycle de création de rapports configuré, puis démarrez **SQL Server Management Studio** sur l’ordinateur SQL Server.</span><span class="sxs-lookup"><span data-stu-id="be4cb-172">Wait until the configured reporting cycle is finished, and then start **SQL Server Management Studio** on the SQL Server computer.</span></span>

2.  <span data-ttu-id="be4cb-173">Sur l’ordinateur SQL Server, démarrez **SQL Server Management Studio**.</span><span class="sxs-lookup"><span data-stu-id="be4cb-173">On the SQL Server computer, start **SQL Server Management Studio**.</span></span>

3.  <span data-ttu-id="be4cb-174">Vérifiez que la table **RecoveryAndHardwareCore. machines** contient une ligne montrant le nom de l’ordinateur de l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="be4cb-174">Verify that the **RecoveryAndHardwareCore.Machines** table contains a row that shows the end-user’s computer name.</span></span>

## <span data-ttu-id="be4cb-175">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="be4cb-175">Related topics</span></span>


[<span data-ttu-id="be4cb-176">Déploiement de MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="be4cb-176">Deploying MBAM 2.0</span></span>](deploying-mbam-20-mbam-2.md)

 

 





