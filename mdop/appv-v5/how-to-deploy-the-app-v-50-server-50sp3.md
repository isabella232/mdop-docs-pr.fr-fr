---
title: Comment déployer le serveur App-V5.0
description: Comment déployer le serveur App-V5.0
author: dansimp
ms.assetid: 4f8f16af-7d74-42b4-84b8-b04ce668225d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b94bab16349751aacf0aca0f8c2e5ac5a6ae6da7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805532"
---
# <span data-ttu-id="2b8a1-103">Comment déployer le serveur App-V5.0</span><span class="sxs-lookup"><span data-stu-id="2b8a1-103">How to Deploy the App-V 5.0 Server</span></span>


<span data-ttu-id="2b8a1-104">Utilisez la procédure suivante pour installer le serveur App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="2b8a1-104">Use the following procedure to install the App-V 5.0 server.</span></span> <span data-ttu-id="2b8a1-105">Pour plus d’informations sur le déploiement du serveur App-V 5,0 SP3, voir [à propos de App-v 5,0 SP3](about-app-v-50-sp3.md#bkmk-migrate-to-50sp3).</span><span class="sxs-lookup"><span data-stu-id="2b8a1-105">For information about deploying the App-V 5.0 SP3 Server, see [About App-V 5.0 SP3](about-app-v-50-sp3.md#bkmk-migrate-to-50sp3).</span></span>

**<span data-ttu-id="2b8a1-106">Avant de commencer:</span><span class="sxs-lookup"><span data-stu-id="2b8a1-106">Before you start:</span></span>**

-   <span data-ttu-id="2b8a1-107">Vérifiez que vous avez installé les logiciels requis.</span><span class="sxs-lookup"><span data-stu-id="2b8a1-107">Ensure that you’ve installed prerequisite software.</span></span> <span data-ttu-id="2b8a1-108">Voir la [Configuration requise pour App-V 5,0](app-v-50-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="2b8a1-108">See [App-V 5.0 Prerequisites](app-v-50-prerequisites.md).</span></span>

-   <span data-ttu-id="2b8a1-109">Passez en revue la section serveur de [considérations relatives à la sécurité dans App-V 5,0](app-v-50-security-considerations.md).</span><span class="sxs-lookup"><span data-stu-id="2b8a1-109">Review the server section of [App-V 5.0 Security Considerations](app-v-50-security-considerations.md).</span></span>

-   <span data-ttu-id="2b8a1-110">Spécifiez un port sur lequel chaque composant sera hébergé.</span><span class="sxs-lookup"><span data-stu-id="2b8a1-110">Specify a port where each component will be hosted.</span></span>

-   <span data-ttu-id="2b8a1-111">Ajoutez des règles de pare-feu pour permettre aux demandes entrantes d’accéder aux ports spécifiés.</span><span class="sxs-lookup"><span data-stu-id="2b8a1-111">Add firewall rules to allow incoming requests to access the specified ports.</span></span>

-   <span data-ttu-id="2b8a1-112">Si vous utilisez des scripts SQL, au lieu du programme d’installation Windows, pour configurer la base de données de gestion ou la base de données de création de rapports, vous devez exécuter les scripts SQL avant d’installer le serveur de gestion ou le serveur de rapports.</span><span class="sxs-lookup"><span data-stu-id="2b8a1-112">If you use SQL scripts, instead of the Windows Installer, to set up the Management database or Reporting database, you must run the SQL scripts before installing the Management Server or Reporting Server.</span></span> <span data-ttu-id="2b8a1-113">Découvrez [comment déployer les bases de données App-V à l’aide de scripts SQL](how-to-deploy-the-app-v-databases-by-using-sql-scripts.md).</span><span class="sxs-lookup"><span data-stu-id="2b8a1-113">See [How to Deploy the App-V Databases by Using SQL Scripts](how-to-deploy-the-app-v-databases-by-using-sql-scripts.md).</span></span>

**<span data-ttu-id="2b8a1-114">Pour installer le serveur App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="2b8a1-114">To install the App-V 5.0 server</span></span>**

1. <span data-ttu-id="2b8a1-115">Copiez les fichiers d’installation de App-V 5,0 Server sur l’ordinateur sur lequel vous voulez l’installer.</span><span class="sxs-lookup"><span data-stu-id="2b8a1-115">Copy the App-V 5.0 server installation files to the computer on which you want to install it.</span></span>

2. <span data-ttu-id="2b8a1-116">Démarrez l’installation de l’App-V 5,0 Server en cliquant avec le bouton droit sur le **appv\_server\_setup.exe** en tant qu’administrateur, puis cliquez sur **installer**.</span><span class="sxs-lookup"><span data-stu-id="2b8a1-116">Start the App-V 5.0 server installation by right-clicking and running **appv\_server\_setup.exe** as an administrator, and then click **Install**.</span></span>

3. <span data-ttu-id="2b8a1-117">Passez en revue et acceptez les termes du contrat de licence, puis indiquez si vous souhaitez activer les mises à jour Microsoft.</span><span class="sxs-lookup"><span data-stu-id="2b8a1-117">Review and accept the license terms, and choose whether to enable Microsoft updates.</span></span>

4. <span data-ttu-id="2b8a1-118">Dans la page de **sélection des fonctionnalités** , sélectionnez tous les composants suivants.</span><span class="sxs-lookup"><span data-stu-id="2b8a1-118">On the **Feature Selection** page, select all of the following components.</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="2b8a1-119">Composant</span><span class="sxs-lookup"><span data-stu-id="2b8a1-119">Component</span></span></th>
   <th align="left"><span data-ttu-id="2b8a1-120">Description</span><span class="sxs-lookup"><span data-stu-id="2b8a1-120">Description</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="2b8a1-121">Serveur de gestion</span><span class="sxs-lookup"><span data-stu-id="2b8a1-121">Management server</span></span></p></td>
   <td align="left"><p><span data-ttu-id="2b8a1-122">Fournit les fonctionnalités de gestion globales de l’infrastructure App-V.</span><span class="sxs-lookup"><span data-stu-id="2b8a1-122">Provides overall management functionality for the App-V infrastructure.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="2b8a1-123">Base de données de gestion</span><span class="sxs-lookup"><span data-stu-id="2b8a1-123">Management database</span></span></p></td>
   <td align="left"><p><span data-ttu-id="2b8a1-124">Facilite le déploiement de la base de données pour la gestion d’App-V.</span><span class="sxs-lookup"><span data-stu-id="2b8a1-124">Facilitates database predeployments for App-V management.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="2b8a1-125">Serveur de publication</span><span class="sxs-lookup"><span data-stu-id="2b8a1-125">Publishing server</span></span></p></td>
   <td align="left"><p><span data-ttu-id="2b8a1-126">Fournit des fonctionnalités d’hébergement et de streaming pour les applications virtuelles.</span><span class="sxs-lookup"><span data-stu-id="2b8a1-126">Provides hosting and streaming functionality for virtual applications.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="2b8a1-127">Serveur de création de rapports</span><span class="sxs-lookup"><span data-stu-id="2b8a1-127">Reporting server</span></span></p></td>
   <td align="left"><p><span data-ttu-id="2b8a1-128">Fournit App-V 5,0 Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="2b8a1-128">Provides App-V 5.0 reporting services.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="2b8a1-129">Base de données de création de rapports</span><span class="sxs-lookup"><span data-stu-id="2b8a1-129">Reporting database</span></span></p></td>
   <td align="left"><p><span data-ttu-id="2b8a1-130">Facilite le déploiement de la base de données pour la création de rapports App-V.</span><span class="sxs-lookup"><span data-stu-id="2b8a1-130">Facilitates database predeployments for App-V reporting.</span></span></p></td>
   </tr>
   </tbody>
   </table>

     

5. <span data-ttu-id="2b8a1-131">Dans la page emplacement de l' **installation** , acceptez l’emplacement par défaut où les composants sélectionnés seront installés ou modifiez l’emplacement en entrant un nouveau chemin dans la ligne emplacement de l' **installation** .</span><span class="sxs-lookup"><span data-stu-id="2b8a1-131">On the **Installation Location** page, accept the default location where the selected components will be installed, or change the location by typing a new path on the **Installation Location** line.</span></span>

6. <span data-ttu-id="2b8a1-132">Dans la page de **création de base de données de gestion** initiale, configurez la **base de données** **Microsoft SQL Server instance** and Management Server en sélectionnant l’option appropriée ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="2b8a1-132">On the initial **Create New Management Database** page, configure the **Microsoft SQL Server instance** and **Management Server database** by selecting the appropriate option below.</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="2b8a1-133">Méthode</span><span class="sxs-lookup"><span data-stu-id="2b8a1-133">Method</span></span></th>
   <th align="left"><span data-ttu-id="2b8a1-134">Ce que vous devez faire</span><span class="sxs-lookup"><span data-stu-id="2b8a1-134">What you need to do</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="2b8a1-135">Vous utilisez une instance de Microsoft SQL Server personnalisée.</span><span class="sxs-lookup"><span data-stu-id="2b8a1-135">You are using a custom Microsoft SQL Server instance.</span></span></p></td>
   <td align="left"><p><span data-ttu-id="2b8a1-136">Sélectionnez <strong> utiliser l’instance personnalisée </strong> , puis tapez le nom de l’instance.</span><span class="sxs-lookup"><span data-stu-id="2b8a1-136">Select <strong>Use the custom instance</strong>, and type the name of the instance.</span></span></p>
   <p><span data-ttu-id="2b8a1-137">Utilisez la mise en forme <strong> InstanceName </strong> .</span><span class="sxs-lookup"><span data-stu-id="2b8a1-137">Use the format <strong>INSTANCENAME</strong>.</span></span> <span data-ttu-id="2b8a1-138">L’emplacement d’installation supposé est l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="2b8a1-138">The assumed installation location is the local computer.</span></span></p>
   <p><span data-ttu-id="2b8a1-139">Non pris en charge: nom du serveur utilisant l’instance de nom de serveur <strong> ServerName </strong> &lt; &gt; </strong> .</span><span class="sxs-lookup"><span data-stu-id="2b8a1-139">Not supported: A server name using the format <strong>ServerName</strong>&lt;strong&gt;INSTANCE</strong>.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="2b8a1-140">Vous utilisez un nom de base de données personnalisé.</span><span class="sxs-lookup"><span data-stu-id="2b8a1-140">You are using a custom database name.</span></span></p></td>
   <td align="left"><p><span data-ttu-id="2b8a1-141">Sélectionnez <strong> configuration personnalisée </strong> et tapez le nom de la base de données.</span><span class="sxs-lookup"><span data-stu-id="2b8a1-141">Select <strong>Custom configuration</strong> and type the database name.</span></span></p>
   <p><span data-ttu-id="2b8a1-142">Le nom de la base de données doit être unique ou l’installation échoue.</span><span class="sxs-lookup"><span data-stu-id="2b8a1-142">The database name must be unique, or the installation will fail.</span></span></p></td>
   </tr>
   </tbody>
   </table>

     

7. <span data-ttu-id="2b8a1-143">Dans la page **configurer** , acceptez la valeur par défaut **utiliser cet ordinateur local**.</span><span class="sxs-lookup"><span data-stu-id="2b8a1-143">On the **Configure** page, accept the default value **Use this local computer**.</span></span>

   **<span data-ttu-id="2b8a1-144">Remarque</span><span class="sxs-lookup"><span data-stu-id="2b8a1-144">Note</span></span>**  
   <span data-ttu-id="2b8a1-145">Si vous installez le serveur de gestion et la base de données de gestion côte à côte, certaines options de cette page ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="2b8a1-145">If you are installing the Management server and Management database side by side, some options on this page are not available.</span></span> <span data-ttu-id="2b8a1-146">Dans ce cas, les options appropriées sont sélectionnées par défaut et ne peuvent pas être modifiées.</span><span class="sxs-lookup"><span data-stu-id="2b8a1-146">In this case, the appropriate options are selected by default and cannot be changed.</span></span>

     

8. <span data-ttu-id="2b8a1-147">Dans la page de **création de base de données initiale de création de rapports** , configurez l' **instance SQL Server** et la **base de données du serveur** de création de rapports en sélectionnant l’option appropriée ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="2b8a1-147">On the initial **Create New Reporting Database** page, configure the **Microsoft SQL Server instance** and **Reporting Server database** by selecting the appropriate option below.</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="2b8a1-148">Méthode</span><span class="sxs-lookup"><span data-stu-id="2b8a1-148">Method</span></span></th>
   <th align="left"><span data-ttu-id="2b8a1-149">Ce que vous devez faire</span><span class="sxs-lookup"><span data-stu-id="2b8a1-149">What you need to do</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="2b8a1-150">Vous utilisez une instance de Microsoft SQL Server personnalisée.</span><span class="sxs-lookup"><span data-stu-id="2b8a1-150">You are using a custom Microsoft SQL Server instance.</span></span></p></td>
   <td align="left"><p><span data-ttu-id="2b8a1-151">Sélectionnez <strong> utiliser l’instance personnalisée </strong> , puis tapez le nom de l’instance.</span><span class="sxs-lookup"><span data-stu-id="2b8a1-151">Select <strong>Use the custom instance</strong>, and type the name of the instance.</span></span></p>
   <p><span data-ttu-id="2b8a1-152">Utilisez la mise en forme <strong> InstanceName </strong> .</span><span class="sxs-lookup"><span data-stu-id="2b8a1-152">Use the format <strong>INSTANCENAME</strong>.</span></span> <span data-ttu-id="2b8a1-153">L’emplacement d’installation supposé est l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="2b8a1-153">The assumed installation location is the local computer.</span></span></p>
   <p><span data-ttu-id="2b8a1-154">Non pris en charge: nom du serveur utilisant l’instance de nom de serveur <strong> ServerName </strong> &lt; &gt; </strong> .</span><span class="sxs-lookup"><span data-stu-id="2b8a1-154">Not supported: A server name using the format <strong>ServerName</strong>&lt;strong&gt;INSTANCE</strong>.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="2b8a1-155">Vous utilisez un nom de base de données personnalisé.</span><span class="sxs-lookup"><span data-stu-id="2b8a1-155">You are using a custom database name.</span></span></p></td>
   <td align="left"><p><span data-ttu-id="2b8a1-156">Sélectionnez <strong> configuration personnalisée </strong> et tapez le nom de la base de données.</span><span class="sxs-lookup"><span data-stu-id="2b8a1-156">Select <strong>Custom configuration</strong> and type the database name.</span></span></p>
   <p><span data-ttu-id="2b8a1-157">Le nom de la base de données doit être unique ou l’installation échoue.</span><span class="sxs-lookup"><span data-stu-id="2b8a1-157">The database name must be unique, or the installation will fail.</span></span></p></td>
   </tr>
   </tbody>
   </table>

     

9. <span data-ttu-id="2b8a1-158">Dans la page **configurer** , acceptez la valeur par défaut: **Utilisez cet ordinateur local**.</span><span class="sxs-lookup"><span data-stu-id="2b8a1-158">On the **Configure** page, accept the default value: **Use this local computer**.</span></span>

   **<span data-ttu-id="2b8a1-159">Remarque</span><span class="sxs-lookup"><span data-stu-id="2b8a1-159">Note</span></span>**  
   <span data-ttu-id="2b8a1-160">Si vous installez le serveur de gestion et la base de données de gestion côte à côte, certaines options de cette page ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="2b8a1-160">If you are installing the Management server and Management database side by side, some options on this page are not available.</span></span> <span data-ttu-id="2b8a1-161">Dans ce cas, les options appropriées sont sélectionnées par défaut et ne peuvent pas être modifiées.</span><span class="sxs-lookup"><span data-stu-id="2b8a1-161">In this case, the appropriate options are selected by default and cannot be changed.</span></span>

     

10. <span data-ttu-id="2b8a1-162">Sur la page **configurer** (configuration du serveur de gestion), spécifiez les éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="2b8a1-162">On the **Configure** (Management Server Configuration) page, specify the following:</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="2b8a1-163">Élément à configurer</span><span class="sxs-lookup"><span data-stu-id="2b8a1-163">Item to configure</span></span></th>
    <th align="left"><span data-ttu-id="2b8a1-164">Description et exemples</span><span class="sxs-lookup"><span data-stu-id="2b8a1-164">Description and examples</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="2b8a1-165">Entrez le groupe d’annonces disposant des autorisations nécessaires pour gérer l’environnement App-V.</span><span class="sxs-lookup"><span data-stu-id="2b8a1-165">Type the AD group with sufficient permissions to manage the App-V environment.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="2b8a1-166">Par exemple: MyDomain\MyUser</span><span class="sxs-lookup"><span data-stu-id="2b8a1-166">Example: MyDomain\MyUser</span></span></p>
    <p><span data-ttu-id="2b8a1-167">Après l’installation, vous pouvez ajouter des utilisateurs ou des groupes supplémentaires à l’aide de la console de gestion.</span><span class="sxs-lookup"><span data-stu-id="2b8a1-167">After installation, you can add additional users or groups by using the Management console.</span></span> <span data-ttu-id="2b8a1-168">Toutefois, les groupes de distribution globale et les groupes de distribution AD DS (Active Directory Domain Services) ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="2b8a1-168">However, global security groups and Active Directory Domain Services (AD DS) distribution groups are not supported.</span></span> <span data-ttu-id="2b8a1-169"><strong> </strong> <strong> </strong> Pour effectuer cette action, vous devez utiliser les groupes locaux de domaine ou universels.</span><span class="sxs-lookup"><span data-stu-id="2b8a1-169">You must use <strong>Domain local</strong> or <strong>Universal</strong> groups are required to perform this action.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong><span data-ttu-id="2b8a1-170">Nom du site Web </strong> : spécifiez le nom personnalisé qui sera utilisé pour exécuter le service de publication.</span><span class="sxs-lookup"><span data-stu-id="2b8a1-170">Website name</strong>: Specify the custom name that will be used to run the publishing service.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="2b8a1-171">Si vous n’avez pas de nom personnalisé, n’apportez aucune modification.</span><span class="sxs-lookup"><span data-stu-id="2b8a1-171">If you do not have a custom name, do not make any changes.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="2b8a1-172">Liaison de port </strong> : spécifiez un numéro de port unique qui sera utilisé par App-V.</span><span class="sxs-lookup"><span data-stu-id="2b8a1-172">Port binding</strong>: Specify a unique port number that will be used by App-V.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="2b8a1-173">Par exemple: <strong> 12345</span><span class="sxs-lookup"><span data-stu-id="2b8a1-173">Example: <strong>12345</span></span></strong></p>
    <p><span data-ttu-id="2b8a1-174">Vérifiez que le port spécifié n’est pas utilisé par un autre site Web.</span><span class="sxs-lookup"><span data-stu-id="2b8a1-174">Ensure that the port specified is not being used by another website.</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

11. <span data-ttu-id="2b8a1-175">Dans la **page Configuration du** **serveur de publication** , spécifiez les éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="2b8a1-175">On the **Configure** **Publishing Server Configuration** page, specify the following:</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="2b8a1-176">Élément à configurer</span><span class="sxs-lookup"><span data-stu-id="2b8a1-176">Item to configure</span></span></th>
    <th align="left"><span data-ttu-id="2b8a1-177">Description et exemples</span><span class="sxs-lookup"><span data-stu-id="2b8a1-177">Description and examples</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="2b8a1-178">Spécifiez l’URL du service de gestion.</span><span class="sxs-lookup"><span data-stu-id="2b8a1-178">Specify the URL for the management service.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="2b8a1-179">Example<a href="http://localhost:12345" data-raw-source="http://localhost:12345">http://localhost:12345</span><span class="sxs-lookup"><span data-stu-id="2b8a1-179">Example: <a href="http://localhost:12345" data-raw-source="http://localhost:12345">http://localhost:12345</span></span></a></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong><span data-ttu-id="2b8a1-180">Nom du site Web </strong> : spécifiez le nom personnalisé qui sera utilisé pour exécuter le service de publication.</span><span class="sxs-lookup"><span data-stu-id="2b8a1-180">Website name</strong>: Specify the custom name that will be used to run the publishing service.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="2b8a1-181">Si vous n’avez pas de nom personnalisé, n’apportez aucune modification.</span><span class="sxs-lookup"><span data-stu-id="2b8a1-181">If you do not have a custom name, do not make any changes.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="2b8a1-182">Liaison de port </strong> : spécifiez un numéro de port unique qui sera utilisé par App-V.</span><span class="sxs-lookup"><span data-stu-id="2b8a1-182">Port binding</strong>: Specify a unique port number that will be used by App-V.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="2b8a1-183">Par exemple: 54321</span><span class="sxs-lookup"><span data-stu-id="2b8a1-183">Example: 54321</span></span></p>
    <p><span data-ttu-id="2b8a1-184">Vérifiez que le port spécifié n’est pas utilisé par un autre site Web.</span><span class="sxs-lookup"><span data-stu-id="2b8a1-184">Ensure that the port specified is not being used by another website.</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

12. <span data-ttu-id="2b8a1-185">Dans la page **Report Server** , spécifiez les éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="2b8a1-185">On the **Reporting Server** page, specify the following:</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="2b8a1-186">Élément à configurer</span><span class="sxs-lookup"><span data-stu-id="2b8a1-186">Item to configure</span></span></th>
    <th align="left"><span data-ttu-id="2b8a1-187">Description et exemples</span><span class="sxs-lookup"><span data-stu-id="2b8a1-187">Description and examples</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="2b8a1-188">Nom du site Web </strong> : spécifiez le nom personnalisé qui sera utilisé pour exécuter le service de création de rapports.</span><span class="sxs-lookup"><span data-stu-id="2b8a1-188">Website name</strong>: Specify the custom name that will be used to run the Reporting Service.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="2b8a1-189">Si vous n’avez pas de nom personnalisé, n’apportez aucune modification.</span><span class="sxs-lookup"><span data-stu-id="2b8a1-189">If you do not have a custom name, do not make any changes.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong><span data-ttu-id="2b8a1-190">Liaison de port </strong> : spécifiez un numéro de port unique qui sera utilisé par App-V.</span><span class="sxs-lookup"><span data-stu-id="2b8a1-190">Port binding</strong>: Specify a unique port number that will be used by App-V.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="2b8a1-191">Par exemple: 55555</span><span class="sxs-lookup"><span data-stu-id="2b8a1-191">Example: 55555</span></span></p>
    <p><span data-ttu-id="2b8a1-192">Vérifiez que le port spécifié n’est pas utilisé par un autre site Web.</span><span class="sxs-lookup"><span data-stu-id="2b8a1-192">Ensure that the port specified is not being used by another website.</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

13. <span data-ttu-id="2b8a1-193">Pour démarrer l’installation, cliquez sur **installer** dans la page **prêt** , puis cliquez sur **Fermer** dans la page **terminé** .</span><span class="sxs-lookup"><span data-stu-id="2b8a1-193">To start the installation, click **Install** on the **Ready** page, and then click **Close** on the **Finished** page.</span></span>

14. <span data-ttu-id="2b8a1-194">Pour vérifier que la configuration s’est déroulée correctement, ouvrez un navigateur Web, puis tapez l’URL suivante:</span><span class="sxs-lookup"><span data-stu-id="2b8a1-194">To verify that the setup completed successfully, open a web browser, and type the following URL:</span></span>

    <span data-ttu-id="2b8a1-195">**http:// &lt; Nom de l’ordinateur du serveur de gestion &gt; : &lt; numéro de port du service de gestion &gt; /Console.html**.</span><span class="sxs-lookup"><span data-stu-id="2b8a1-195">**http://&lt;Management server machine name&gt;:&lt;Management service port number&gt;/Console.html**.</span></span>

    <span data-ttu-id="2b8a1-196">Par exemple: **http://localhost:12345/console.html** .</span><span class="sxs-lookup"><span data-stu-id="2b8a1-196">Example: **http://localhost:12345/console.html**.</span></span> <span data-ttu-id="2b8a1-197">Si l’installation a réussi, la console de gestion App-V est affichée sans erreur.</span><span class="sxs-lookup"><span data-stu-id="2b8a1-197">If the installation succeeded, the App-V Management console is displayed with no errors.</span></span>

    <span data-ttu-id="2b8a1-198">Vous **avez une suggestion pour App-V**?</span><span class="sxs-lookup"><span data-stu-id="2b8a1-198">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="2b8a1-199">Ajoutez ou Votez en fonction [de suggestions.](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)</span><span class="sxs-lookup"><span data-stu-id="2b8a1-199">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="2b8a1-200">Vous avez un problème lié à l’application-V?</span><span class="sxs-lookup"><span data-stu-id="2b8a1-200">Got an App-V issue?</span></span>** <span data-ttu-id="2b8a1-201">Utilisez le [Forum TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="2b8a1-201">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="2b8a1-202">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2b8a1-202">Related topics</span></span>


[<span data-ttu-id="2b8a1-203">Déploiement d'App-V5.0</span><span class="sxs-lookup"><span data-stu-id="2b8a1-203">Deploying App-V 5.0</span></span>](deploying-app-v-50.md)

[<span data-ttu-id="2b8a1-204">Comment installer les bases de données de gestion et de rapports sur des ordinateurs distincts des services de gestion et de rapports</span><span class="sxs-lookup"><span data-stu-id="2b8a1-204">How to Install the Management and Reporting Databases on Separate Computers from the Management and Reporting Services</span></span>](how-to-install-the-management-and-reporting-databases-on-separate-computers-from-the-management-and-reporting-services.md)

[<span data-ttu-id="2b8a1-205">Comment installer le serveur de publication sur un ordinateur distant</span><span class="sxs-lookup"><span data-stu-id="2b8a1-205">How to Install the Publishing Server on a Remote Computer</span></span>](how-to-install-the-publishing-server-on-a-remote-computer.md)

[<span data-ttu-id="2b8a1-206">Déploiement du serveur App-V5.0 à l'aide d'un script</span><span class="sxs-lookup"><span data-stu-id="2b8a1-206">How to Deploy the App-V 5.0 Server Using a Script</span></span>](how-to-deploy-the-app-v-50-server-using-a-script.md)

[<span data-ttu-id="2b8a1-207">Activation de la création de rapports sur App-V5.0 Client à l'aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="2b8a1-207">How to Enable Reporting on the App-V 5.0 Client by Using PowerShell</span></span>](how-to-enable-reporting-on-the-app-v-50-client-by-using-powershell.md)

 

 





