---
title: Procédure de déploiement d'App-V5.1 Server
description: Procédure de déploiement d'App-V5.1 Server
author: dansimp
ms.assetid: 4729beda-b98f-481b-ae74-ad71c59b1d69
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4a367be7db4cea1835124657dbdfa3375474228e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805497"
---
# <span data-ttu-id="7c133-103">Procédure de déploiement d'App-V5.1 Server</span><span class="sxs-lookup"><span data-stu-id="7c133-103">How to Deploy the App-V 5.1 Server</span></span>


<span data-ttu-id="7c133-104">Utilisez la procédure suivante pour installer le serveur Microsoft Application Virtualization (App-V) 5,1.</span><span class="sxs-lookup"><span data-stu-id="7c133-104">Use the following procedure to install the Microsoft Application Virtualization (App-V) 5.1 server.</span></span> <span data-ttu-id="7c133-105">Pour plus d’informations sur le déploiement du serveur App-V 5,1, voir [à propos de App-v 5,1](about-app-v-51.md#bkmk-migrate-to-51).</span><span class="sxs-lookup"><span data-stu-id="7c133-105">For information about deploying the App-V 5.1 Server, see [About App-V 5.1](about-app-v-51.md#bkmk-migrate-to-51).</span></span>

**<span data-ttu-id="7c133-106">Avant de commencer:</span><span class="sxs-lookup"><span data-stu-id="7c133-106">Before you start:</span></span>**

-   <span data-ttu-id="7c133-107">Vérifiez que vous avez installé les logiciels requis.</span><span class="sxs-lookup"><span data-stu-id="7c133-107">Ensure that you’ve installed prerequisite software.</span></span> <span data-ttu-id="7c133-108">Voir la [Configuration requise pour App-V 5,1](app-v-51-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="7c133-108">See [App-V 5.1 Prerequisites](app-v-51-prerequisites.md).</span></span>

-   <span data-ttu-id="7c133-109">Passez en revue la section serveur de [considérations relatives à la sécurité dans App-V 5,1](app-v-51-security-considerations.md).</span><span class="sxs-lookup"><span data-stu-id="7c133-109">Review the server section of [App-V 5.1 Security Considerations](app-v-51-security-considerations.md).</span></span>

-   <span data-ttu-id="7c133-110">Spécifiez un port sur lequel chaque composant sera hébergé.</span><span class="sxs-lookup"><span data-stu-id="7c133-110">Specify a port where each component will be hosted.</span></span>

-   <span data-ttu-id="7c133-111">Ajoutez des règles de pare-feu pour permettre aux demandes entrantes d’accéder aux ports spécifiés.</span><span class="sxs-lookup"><span data-stu-id="7c133-111">Add firewall rules to allow incoming requests to access the specified ports.</span></span>

-   <span data-ttu-id="7c133-112">Si vous utilisez des scripts SQL, au lieu du programme d’installation Windows, pour configurer la base de données de gestion ou la base de données de création de rapports, vous devez exécuter les scripts SQL avant d’installer le serveur de gestion ou le serveur de rapports.</span><span class="sxs-lookup"><span data-stu-id="7c133-112">If you use SQL scripts, instead of the Windows Installer, to set up the Management database or Reporting database, you must run the SQL scripts before installing the Management Server or Reporting Server.</span></span> <span data-ttu-id="7c133-113">Découvrez [comment déployer les bases de données App-V à l’aide de scripts SQL](how-to-deploy-the-app-v-databases-by-using-sql-scripts51.md).</span><span class="sxs-lookup"><span data-stu-id="7c133-113">See [How to Deploy the App-V Databases by Using SQL Scripts](how-to-deploy-the-app-v-databases-by-using-sql-scripts51.md).</span></span>

**<span data-ttu-id="7c133-114">Pour installer le serveur App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="7c133-114">To install the App-V 5.1 server</span></span>**

1. <span data-ttu-id="7c133-115">Copiez les fichiers d’installation de App-V 5,1 Server sur l’ordinateur sur lequel vous voulez l’installer.</span><span class="sxs-lookup"><span data-stu-id="7c133-115">Copy the App-V 5.1 server installation files to the computer on which you want to install it.</span></span>

2. <span data-ttu-id="7c133-116">Démarrez l’installation de l’App-V 5,1 Server en cliquant avec le bouton droit sur le **appv\_server\_setup.exe** en tant qu’administrateur, puis cliquez sur **installer**.</span><span class="sxs-lookup"><span data-stu-id="7c133-116">Start the App-V 5.1 server installation by right-clicking and running **appv\_server\_setup.exe** as an administrator, and then click **Install**.</span></span>

3. <span data-ttu-id="7c133-117">Passez en revue et acceptez les termes du contrat de licence, puis indiquez si vous souhaitez activer les mises à jour Microsoft.</span><span class="sxs-lookup"><span data-stu-id="7c133-117">Review and accept the license terms, and choose whether to enable Microsoft updates.</span></span>

4. <span data-ttu-id="7c133-118">Dans la page de **sélection des fonctionnalités** , sélectionnez tous les composants suivants.</span><span class="sxs-lookup"><span data-stu-id="7c133-118">On the **Feature Selection** page, select all of the following components.</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="7c133-119">Composant</span><span class="sxs-lookup"><span data-stu-id="7c133-119">Component</span></span></th>
   <th align="left"><span data-ttu-id="7c133-120">Description</span><span class="sxs-lookup"><span data-stu-id="7c133-120">Description</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="7c133-121">Serveur de gestion</span><span class="sxs-lookup"><span data-stu-id="7c133-121">Management server</span></span></p></td>
   <td align="left"><p><span data-ttu-id="7c133-122">Fournit les fonctionnalités de gestion globales de l’infrastructure App-V.</span><span class="sxs-lookup"><span data-stu-id="7c133-122">Provides overall management functionality for the App-V infrastructure.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="7c133-123">Base de données de gestion</span><span class="sxs-lookup"><span data-stu-id="7c133-123">Management database</span></span></p></td>
   <td align="left"><p><span data-ttu-id="7c133-124">Facilite le déploiement de la base de données pour la gestion d’App-V.</span><span class="sxs-lookup"><span data-stu-id="7c133-124">Facilitates database predeployments for App-V management.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="7c133-125">Serveur de publication</span><span class="sxs-lookup"><span data-stu-id="7c133-125">Publishing server</span></span></p></td>
   <td align="left"><p><span data-ttu-id="7c133-126">Fournit des fonctionnalités d’hébergement et de streaming pour les applications virtuelles.</span><span class="sxs-lookup"><span data-stu-id="7c133-126">Provides hosting and streaming functionality for virtual applications.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="7c133-127">Serveur de création de rapports</span><span class="sxs-lookup"><span data-stu-id="7c133-127">Reporting server</span></span></p></td>
   <td align="left"><p><span data-ttu-id="7c133-128">Fournit App-V 5,1 Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="7c133-128">Provides App-V 5.1 reporting services.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="7c133-129">Base de données de création de rapports</span><span class="sxs-lookup"><span data-stu-id="7c133-129">Reporting database</span></span></p></td>
   <td align="left"><p><span data-ttu-id="7c133-130">Facilite le déploiement de la base de données pour la création de rapports App-V.</span><span class="sxs-lookup"><span data-stu-id="7c133-130">Facilitates database predeployments for App-V reporting.</span></span></p></td>
   </tr>
   </tbody>
   </table>

     

5. <span data-ttu-id="7c133-131">Dans la page emplacement de l' **installation** , acceptez l’emplacement par défaut où les composants sélectionnés seront installés ou modifiez l’emplacement en entrant un nouveau chemin dans la ligne emplacement de l' **installation** .</span><span class="sxs-lookup"><span data-stu-id="7c133-131">On the **Installation Location** page, accept the default location where the selected components will be installed, or change the location by typing a new path on the **Installation Location** line.</span></span>

6. <span data-ttu-id="7c133-132">Dans la page de **création de base de données de gestion** initiale, configurez la **base de données** **Microsoft SQL Server instance** and Management Server en sélectionnant l’option appropriée ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="7c133-132">On the initial **Create New Management Database** page, configure the **Microsoft SQL Server instance** and **Management Server database** by selecting the appropriate option below.</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="7c133-133">Méthode</span><span class="sxs-lookup"><span data-stu-id="7c133-133">Method</span></span></th>
   <th align="left"><span data-ttu-id="7c133-134">Ce que vous devez faire</span><span class="sxs-lookup"><span data-stu-id="7c133-134">What you need to do</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="7c133-135">Vous utilisez une instance de Microsoft SQL Server personnalisée.</span><span class="sxs-lookup"><span data-stu-id="7c133-135">You are using a custom Microsoft SQL Server instance.</span></span></p></td>
   <td align="left"><p><span data-ttu-id="7c133-136">Sélectionnez <strong> utiliser l’instance personnalisée </strong> , puis tapez le nom de l’instance.</span><span class="sxs-lookup"><span data-stu-id="7c133-136">Select <strong>Use the custom instance</strong>, and type the name of the instance.</span></span></p>
   <p><span data-ttu-id="7c133-137">Utilisez la mise en forme <strong> InstanceName </strong> .</span><span class="sxs-lookup"><span data-stu-id="7c133-137">Use the format <strong>INSTANCENAME</strong>.</span></span> <span data-ttu-id="7c133-138">L’emplacement d’installation supposé est l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="7c133-138">The assumed installation location is the local computer.</span></span></p>
   <p><span data-ttu-id="7c133-139">Non pris en charge: nom du serveur utilisant l’instance de nom de serveur <strong> ServerName </strong> &lt; &gt; </strong> .</span><span class="sxs-lookup"><span data-stu-id="7c133-139">Not supported: A server name using the format <strong>ServerName</strong>&lt;strong&gt;INSTANCE</strong>.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="7c133-140">Vous utilisez un nom de base de données personnalisé.</span><span class="sxs-lookup"><span data-stu-id="7c133-140">You are using a custom database name.</span></span></p></td>
   <td align="left"><p><span data-ttu-id="7c133-141">Sélectionnez <strong> configuration personnalisée </strong> et tapez le nom de la base de données.</span><span class="sxs-lookup"><span data-stu-id="7c133-141">Select <strong>Custom configuration</strong> and type the database name.</span></span></p>
   <p><span data-ttu-id="7c133-142">Le nom de la base de données doit être unique ou l’installation échoue.</span><span class="sxs-lookup"><span data-stu-id="7c133-142">The database name must be unique, or the installation will fail.</span></span></p></td>
   </tr>
   </tbody>
   </table>

     

7. <span data-ttu-id="7c133-143">Dans la page **configurer** , acceptez la valeur par défaut **utiliser cet ordinateur local**.</span><span class="sxs-lookup"><span data-stu-id="7c133-143">On the **Configure** page, accept the default value **Use this local computer**.</span></span>

   **<span data-ttu-id="7c133-144">Remarque</span><span class="sxs-lookup"><span data-stu-id="7c133-144">Note</span></span>**  
   <span data-ttu-id="7c133-145">Si vous installez le serveur de gestion et la base de données de gestion côte à côte, certaines options de cette page ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="7c133-145">If you are installing the Management server and Management database side by side, some options on this page are not available.</span></span> <span data-ttu-id="7c133-146">Dans ce cas, les options appropriées sont sélectionnées par défaut et ne peuvent pas être modifiées.</span><span class="sxs-lookup"><span data-stu-id="7c133-146">In this case, the appropriate options are selected by default and cannot be changed.</span></span>

     

8. <span data-ttu-id="7c133-147">Dans la page de **création de base de données initiale de création de rapports** , configurez l' **instance SQL Server** et la **base de données du serveur** de création de rapports en sélectionnant l’option appropriée ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="7c133-147">On the initial **Create New Reporting Database** page, configure the **Microsoft SQL Server instance** and **Reporting Server database** by selecting the appropriate option below.</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="7c133-148">Méthode</span><span class="sxs-lookup"><span data-stu-id="7c133-148">Method</span></span></th>
   <th align="left"><span data-ttu-id="7c133-149">Ce que vous devez faire</span><span class="sxs-lookup"><span data-stu-id="7c133-149">What you need to do</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="7c133-150">Vous utilisez une instance de Microsoft SQL Server personnalisée.</span><span class="sxs-lookup"><span data-stu-id="7c133-150">You are using a custom Microsoft SQL Server instance.</span></span></p></td>
   <td align="left"><p><span data-ttu-id="7c133-151">Sélectionnez <strong> utiliser l’instance personnalisée </strong> , puis tapez le nom de l’instance.</span><span class="sxs-lookup"><span data-stu-id="7c133-151">Select <strong>Use the custom instance</strong>, and type the name of the instance.</span></span></p>
   <p><span data-ttu-id="7c133-152">Utilisez la mise en forme <strong> InstanceName </strong> .</span><span class="sxs-lookup"><span data-stu-id="7c133-152">Use the format <strong>INSTANCENAME</strong>.</span></span> <span data-ttu-id="7c133-153">L’emplacement d’installation supposé est l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="7c133-153">The assumed installation location is the local computer.</span></span></p>
   <p><span data-ttu-id="7c133-154">Non pris en charge: nom du serveur utilisant l’instance de nom de serveur <strong> ServerName </strong> &lt; &gt; </strong> .</span><span class="sxs-lookup"><span data-stu-id="7c133-154">Not supported: A server name using the format <strong>ServerName</strong>&lt;strong&gt;INSTANCE</strong>.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="7c133-155">Vous utilisez un nom de base de données personnalisé.</span><span class="sxs-lookup"><span data-stu-id="7c133-155">You are using a custom database name.</span></span></p></td>
   <td align="left"><p><span data-ttu-id="7c133-156">Sélectionnez <strong> configuration personnalisée </strong> et tapez le nom de la base de données.</span><span class="sxs-lookup"><span data-stu-id="7c133-156">Select <strong>Custom configuration</strong> and type the database name.</span></span></p>
   <p><span data-ttu-id="7c133-157">Le nom de la base de données doit être unique ou l’installation échoue.</span><span class="sxs-lookup"><span data-stu-id="7c133-157">The database name must be unique, or the installation will fail.</span></span></p></td>
   </tr>
   </tbody>
   </table>

     

9. <span data-ttu-id="7c133-158">Dans la page **configurer** , acceptez la valeur par défaut: **Utilisez cet ordinateur local**.</span><span class="sxs-lookup"><span data-stu-id="7c133-158">On the **Configure** page, accept the default value: **Use this local computer**.</span></span>

   **<span data-ttu-id="7c133-159">Remarque</span><span class="sxs-lookup"><span data-stu-id="7c133-159">Note</span></span>**  
   <span data-ttu-id="7c133-160">Si vous installez le serveur de gestion et la base de données de gestion côte à côte, certaines options de cette page ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="7c133-160">If you are installing the Management server and Management database side by side, some options on this page are not available.</span></span> <span data-ttu-id="7c133-161">Dans ce cas, les options appropriées sont sélectionnées par défaut et ne peuvent pas être modifiées.</span><span class="sxs-lookup"><span data-stu-id="7c133-161">In this case, the appropriate options are selected by default and cannot be changed.</span></span>

     

10. <span data-ttu-id="7c133-162">Sur la page **configurer** (configuration du serveur de gestion), spécifiez les éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="7c133-162">On the **Configure** (Management Server Configuration) page, specify the following:</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="7c133-163">Élément à configurer</span><span class="sxs-lookup"><span data-stu-id="7c133-163">Item to configure</span></span></th>
    <th align="left"><span data-ttu-id="7c133-164">Description et exemples</span><span class="sxs-lookup"><span data-stu-id="7c133-164">Description and examples</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7c133-165">Entrez le groupe d’annonces disposant des autorisations nécessaires pour gérer l’environnement App-V.</span><span class="sxs-lookup"><span data-stu-id="7c133-165">Type the AD group with sufficient permissions to manage the App-V environment.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7c133-166">Par exemple: MyDomain\MyUser</span><span class="sxs-lookup"><span data-stu-id="7c133-166">Example: MyDomain\MyUser</span></span></p>
    <p><span data-ttu-id="7c133-167">Après l’installation, vous pouvez ajouter des utilisateurs ou des groupes supplémentaires à l’aide de la console de gestion.</span><span class="sxs-lookup"><span data-stu-id="7c133-167">After installation, you can add additional users or groups by using the Management console.</span></span> <span data-ttu-id="7c133-168">Toutefois, les groupes de distribution globale et les groupes de distribution AD DS (Active Directory Domain Services) ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="7c133-168">However, global security groups and Active Directory Domain Services (AD DS) distribution groups are not supported.</span></span> <span data-ttu-id="7c133-169"><strong> </strong> <strong> </strong> Pour effectuer cette action, vous devez utiliser les groupes locaux de domaine ou universels.</span><span class="sxs-lookup"><span data-stu-id="7c133-169">You must use <strong>Domain local</strong> or <strong>Universal</strong> groups are required to perform this action.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong><span data-ttu-id="7c133-170">Nom du site Web </strong> : spécifiez le nom personnalisé qui sera utilisé pour exécuter le service de publication.</span><span class="sxs-lookup"><span data-stu-id="7c133-170">Website name</strong>: Specify the custom name that will be used to run the publishing service.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7c133-171">Si vous n’avez pas de nom personnalisé, n’apportez aucune modification.</span><span class="sxs-lookup"><span data-stu-id="7c133-171">If you do not have a custom name, do not make any changes.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="7c133-172">Liaison de port </strong> : spécifiez un numéro de port unique qui sera utilisé par App-V.</span><span class="sxs-lookup"><span data-stu-id="7c133-172">Port binding</strong>: Specify a unique port number that will be used by App-V.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7c133-173">Par exemple: <strong> 12345</span><span class="sxs-lookup"><span data-stu-id="7c133-173">Example: <strong>12345</span></span></strong></p>
    <p><span data-ttu-id="7c133-174">Vérifiez que le port spécifié n’est pas utilisé par un autre site Web.</span><span class="sxs-lookup"><span data-stu-id="7c133-174">Ensure that the port specified is not being used by another website.</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

11. <span data-ttu-id="7c133-175">Dans la **page Configuration du** **serveur de publication** , spécifiez les éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="7c133-175">On the **Configure** **Publishing Server Configuration** page, specify the following:</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="7c133-176">Élément à configurer</span><span class="sxs-lookup"><span data-stu-id="7c133-176">Item to configure</span></span></th>
    <th align="left"><span data-ttu-id="7c133-177">Description et exemples</span><span class="sxs-lookup"><span data-stu-id="7c133-177">Description and examples</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7c133-178">Spécifiez l’URL du service de gestion.</span><span class="sxs-lookup"><span data-stu-id="7c133-178">Specify the URL for the management service.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7c133-179">Example<a href="http://localhost:12345" data-raw-source="http://localhost:12345">http://localhost:12345</span><span class="sxs-lookup"><span data-stu-id="7c133-179">Example: <a href="http://localhost:12345" data-raw-source="http://localhost:12345">http://localhost:12345</span></span></a></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong><span data-ttu-id="7c133-180">Nom du site Web </strong> : spécifiez le nom personnalisé qui sera utilisé pour exécuter le service de publication.</span><span class="sxs-lookup"><span data-stu-id="7c133-180">Website name</strong>: Specify the custom name that will be used to run the publishing service.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7c133-181">Si vous n’avez pas de nom personnalisé, n’apportez aucune modification.</span><span class="sxs-lookup"><span data-stu-id="7c133-181">If you do not have a custom name, do not make any changes.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="7c133-182">Liaison de port </strong> : spécifiez un numéro de port unique qui sera utilisé par App-V.</span><span class="sxs-lookup"><span data-stu-id="7c133-182">Port binding</strong>: Specify a unique port number that will be used by App-V.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7c133-183">Par exemple: 54321</span><span class="sxs-lookup"><span data-stu-id="7c133-183">Example: 54321</span></span></p>
    <p><span data-ttu-id="7c133-184">Vérifiez que le port spécifié n’est pas utilisé par un autre site Web.</span><span class="sxs-lookup"><span data-stu-id="7c133-184">Ensure that the port specified is not being used by another website.</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

12. <span data-ttu-id="7c133-185">Dans la page **Report Server** , spécifiez les éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="7c133-185">On the **Reporting Server** page, specify the following:</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="7c133-186">Élément à configurer</span><span class="sxs-lookup"><span data-stu-id="7c133-186">Item to configure</span></span></th>
    <th align="left"><span data-ttu-id="7c133-187">Description et exemples</span><span class="sxs-lookup"><span data-stu-id="7c133-187">Description and examples</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="7c133-188">Nom du site Web </strong> : spécifiez le nom personnalisé qui sera utilisé pour exécuter le service de création de rapports.</span><span class="sxs-lookup"><span data-stu-id="7c133-188">Website name</strong>: Specify the custom name that will be used to run the Reporting Service.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7c133-189">Si vous n’avez pas de nom personnalisé, n’apportez aucune modification.</span><span class="sxs-lookup"><span data-stu-id="7c133-189">If you do not have a custom name, do not make any changes.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong><span data-ttu-id="7c133-190">Liaison de port </strong> : spécifiez un numéro de port unique qui sera utilisé par App-V.</span><span class="sxs-lookup"><span data-stu-id="7c133-190">Port binding</strong>: Specify a unique port number that will be used by App-V.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7c133-191">Par exemple: 55555</span><span class="sxs-lookup"><span data-stu-id="7c133-191">Example: 55555</span></span></p>
    <p><span data-ttu-id="7c133-192">Vérifiez que le port spécifié n’est pas utilisé par un autre site Web.</span><span class="sxs-lookup"><span data-stu-id="7c133-192">Ensure that the port specified is not being used by another website.</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

13. <span data-ttu-id="7c133-193">Pour démarrer l’installation, cliquez sur **installer** dans la page **prêt** , puis cliquez sur **Fermer** dans la page **terminé** .</span><span class="sxs-lookup"><span data-stu-id="7c133-193">To start the installation, click **Install** on the **Ready** page, and then click **Close** on the **Finished** page.</span></span>

14. <span data-ttu-id="7c133-194">Pour vérifier que la configuration s’est déroulée correctement, ouvrez un navigateur Web, puis tapez l’URL suivante:</span><span class="sxs-lookup"><span data-stu-id="7c133-194">To verify that the setup completed successfully, open a web browser, and type the following URL:</span></span>

    <span data-ttu-id="7c133-195">**http:// &lt; Nom de l’ordinateur du serveur de gestion &gt; : &lt; numéro de port du service de gestion &gt; /Console.html**.</span><span class="sxs-lookup"><span data-stu-id="7c133-195">**http://&lt;Management server machine name&gt;:&lt;Management service port number&gt;/Console.html**.</span></span>

    <span data-ttu-id="7c133-196">Par exemple: **http://localhost:12345/console.html** .</span><span class="sxs-lookup"><span data-stu-id="7c133-196">Example: **http://localhost:12345/console.html**.</span></span> <span data-ttu-id="7c133-197">Si l’installation a réussi, la console de gestion App-V est affichée sans erreur.</span><span class="sxs-lookup"><span data-stu-id="7c133-197">If the installation succeeded, the App-V Management console is displayed with no errors.</span></span>

    <span data-ttu-id="7c133-198">Vous **avez une suggestion pour App-V**?</span><span class="sxs-lookup"><span data-stu-id="7c133-198">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="7c133-199">Ajoutez ou Votez en fonction [de suggestions.](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)</span><span class="sxs-lookup"><span data-stu-id="7c133-199">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="7c133-200">Vous avez un problème lié à l’application-V?</span><span class="sxs-lookup"><span data-stu-id="7c133-200">Got an App-V issue?</span></span>** <span data-ttu-id="7c133-201">Utilisez le [Forum TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="7c133-201">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="7c133-202">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7c133-202">Related topics</span></span>


[<span data-ttu-id="7c133-203">Déploiement d'App-V5.1</span><span class="sxs-lookup"><span data-stu-id="7c133-203">Deploying App-V 5.1</span></span>](deploying-app-v-51.md)

[<span data-ttu-id="7c133-204">Comment installer les bases de données de gestion et de rapports sur des ordinateurs distincts des services de gestion et de rapports</span><span class="sxs-lookup"><span data-stu-id="7c133-204">How to Install the Management and Reporting Databases on Separate Computers from the Management and Reporting Services</span></span>](how-to-install-the-management-and-reporting-databases-on-separate-computers-from-the-management-and-reporting-services51.md)

[<span data-ttu-id="7c133-205">Comment installer le serveur de publication sur un ordinateur distant</span><span class="sxs-lookup"><span data-stu-id="7c133-205">How to Install the Publishing Server on a Remote Computer</span></span>](how-to-install-the-publishing-server-on-a-remote-computer51.md)

[<span data-ttu-id="7c133-206">Déploiement du serveur App-V5.1 à l'aide d'un script</span><span class="sxs-lookup"><span data-stu-id="7c133-206">How to Deploy the App-V 5.1 Server Using a Script</span></span>](how-to-deploy-the-app-v-51-server-using-a-script.md)

 

 





