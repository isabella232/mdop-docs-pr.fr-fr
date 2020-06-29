---
title: Création de bases de données App-V4.5 à l'aide de scripts SQL
description: Création de bases de données App-V4.5 à l'aide de scripts SQL
author: dansimp
ms.assetid: 6cd0b180-163e-463f-a658-939ab9a7cfa1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d9ab2c102a43701bfdeaac49359b4ca3c4a063fa
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811478"
---
# <span data-ttu-id="69631-103">Création de bases de données App-V4.5 à l'aide de scripts SQL</span><span class="sxs-lookup"><span data-stu-id="69631-103">Creating App-V 4.5 Databases Using SQL Scripting</span></span>


**<span data-ttu-id="69631-104">À qui cette solution est-elle conçue pour?</span><span class="sxs-lookup"><span data-stu-id="69631-104">Who is this solution intended for?</span></span>** <span data-ttu-id="69631-105">Professionnels de l’informatique qui gèrent les bases de données 4,5 de virtualisation des applications (App-V).</span><span class="sxs-lookup"><span data-stu-id="69631-105">Information technology professionals who manage Application Virtualization (App-V) 4.5 databases.</span></span>

**<span data-ttu-id="69631-106">Comment ce guide peut-il vous aider?</span><span class="sxs-lookup"><span data-stu-id="69631-106">How can this guide help you?</span></span>** <span data-ttu-id="69631-107">Cette solution explique et décrit la procédure d’installation du serveur Microsoft Application Virtualization lors de l’installation d’un administrateur ne disposant pas de privilèges sysadmin sur le serveur SQL Server.</span><span class="sxs-lookup"><span data-stu-id="69631-107">This solution explains and documents the procedure to install the Microsoft Application Virtualization Server when the administrator installing does not have “sysadmin” privileges to the SQL Server.</span></span>

## <span data-ttu-id="69631-108">Vue d'ensemble</span><span class="sxs-lookup"><span data-stu-id="69631-108">Overview</span></span>


<span data-ttu-id="69631-109">L’un des problèmes liés à l’installation de Microsoft Application Virtualization 4,5 (App-V) est que le programme d’installation suppose que l’utilisateur qui installe les fonctionnalités du serveur n’est pas seulement un administrateur d’ordinateur local, mais qu’il dispose également de privilèges d’administrateur SQL sur le serveur SQL Server qui héberge le magasin de données.</span><span class="sxs-lookup"><span data-stu-id="69631-109">One of the challenges of installing Microsoft Application Virtualization 4.5 (App-V) is that the install program assumes that the user installing the server features will not only be a local computer administrator, but also have SQL administrator privileges on the SQL server that will host the Data Store.</span></span> <span data-ttu-id="69631-110">Cette condition est basée sur le fait que la base de données, ainsi que les rôles et les autorisations appropriés, sont créés dans le cadre de l’installation.</span><span class="sxs-lookup"><span data-stu-id="69631-110">This requirement is based on the fact that the database, as well as the appropriate roles and permissions, are created as part of the install.</span></span> <span data-ttu-id="69631-111">Toutefois, dans la plupart des entreprises, les serveurs SQL sont gérés indépendamment de l’équipe d’infrastructure qui va installer App-V.</span><span class="sxs-lookup"><span data-stu-id="69631-111">However, in most enterprises, SQL servers are managed separately from the infrastructure team who will be installing App-V.</span></span> <span data-ttu-id="69631-112">Ces exigences de sécurité compliquent la mise en route des administrateurs SQL pour permettre à l’administrateur d’infrastructure d’installer les droits appropriés App-V. de même, les administrateurs SQL ne disposent pas des privilèges requis pour installer le produit pour l’équipe d’infrastructure.</span><span class="sxs-lookup"><span data-stu-id="69631-112">These security requirements will make it difficult to get SQL administrators to give the infrastructure administrator installing App-V adequate rights; similarly, the SQL administrators will not have the required privileges to install the product for the infrastructure team.</span></span>

<span data-ttu-id="69631-113">Pour l’instant, un administrateur qui tente d’installer App-V doit disposer de privilèges SQL «sysadmin».</span><span class="sxs-lookup"><span data-stu-id="69631-113">Currently, an administrator attempting the installation of App-V must have SQL “sysadmin” privileges.</span></span> <span data-ttu-id="69631-114">Dans les versions précédentes du produit, le programme d’installation permettait aux administrateurs SQL de créer un compte «sysadmin» temporaire ou d’être présent au cours de l’installation pour fournir des informations d’identification avec des privilèges «sysadmin».</span><span class="sxs-lookup"><span data-stu-id="69631-114">In previous versions of the product the setup allowed for the SQL administrators to either create a temporary “sysadmin” account or be present during installation to provide credentials with “sysadmin” privileges.</span></span> <span data-ttu-id="69631-115">Dans cette version, les scripts sont fournis dans le produit publié pour que tous les administrateurs aient recours lors de l’implémentation de leur infrastructure.</span><span class="sxs-lookup"><span data-stu-id="69631-115">In this release, scripts are provided in the released product for all administrators to use when implementing their infrastructure.</span></span>

<span data-ttu-id="69631-116">Ce livre blanc traite du scénario dans lequel l’installation doit être divisée en deux tâches distinctes: création de la base de données SQL et installation des fonctionnalités du serveur App-V.</span><span class="sxs-lookup"><span data-stu-id="69631-116">This whitepaper discusses the scenario in which the install will need to be divided into two separate tasks: creating the SQL database, and installing the App-V server features.</span></span> <span data-ttu-id="69631-117">Les administrateurs SQL seraient en mesure de passer en revue les scripts SQL et de modifier les conflits avec d’autres bases de données ou de prendre en charge l’intégration avec d’autres outils.</span><span class="sxs-lookup"><span data-stu-id="69631-117">The SQL administrators would be able to review the SQL scripts and make modifications to resolve any conflicts with other databases, or to support integration with other tools.</span></span> <span data-ttu-id="69631-118">Le résultat des scripts doit permettre aux administrateurs SQL de préparer la base de données de sorte que les administrateurs d’infrastructure n’aient pas besoin d’avoir accès à des droits avancés sur le serveur SQL Server.</span><span class="sxs-lookup"><span data-stu-id="69631-118">The result of the scripts is to allow SQL administrators to prepare the database so that the infrastructure administrators do not have to be granted any advanced rights on the SQL server.</span></span> <span data-ttu-id="69631-119">C’est important dans les environnements dans lesquels les politiques de sécurité n’interdisent pas.</span><span class="sxs-lookup"><span data-stu-id="69631-119">This is important in environments where security policies would prohibit this.</span></span>

### <span data-ttu-id="69631-120">Processus de création d’une base de données SQL</span><span class="sxs-lookup"><span data-stu-id="69631-120">SQL Database Creation Process</span></span>

<span data-ttu-id="69631-121">Les scripts SQL permettent aux administrateurs SQL de créer la base de données requise et de configurer les privilèges d’administrateur d’application-V pour l’installation et la gestion de l’environnement.</span><span class="sxs-lookup"><span data-stu-id="69631-121">The SQL scripts allow for SQL administrators to create the required database and also set up the privileges for the App-V administrators to successfully install and manage the environment.</span></span> <span data-ttu-id="69631-122">Les étapes permettant d’effectuer ces tâches sont indiquées plus loin dans ce document.</span><span class="sxs-lookup"><span data-stu-id="69631-122">The steps for completing these tasks are listed later in this document.</span></span>

<span data-ttu-id="69631-123">Ce processus sépare les actions de création et de configuration de la base de données de l’installation App-V réelle.</span><span class="sxs-lookup"><span data-stu-id="69631-123">This process separates the database creation and configuration actions from the actual App-V installation.</span></span>

**<span data-ttu-id="69631-124">Informations à fournir aux administrateurs SQL</span><span class="sxs-lookup"><span data-stu-id="69631-124">Information to be provided to SQL administrators</span></span>**

-   <span data-ttu-id="69631-125">Nom du groupe d’annonces qui va être l’administrateur de l’application-V.</span><span class="sxs-lookup"><span data-stu-id="69631-125">Name of AD group that is going to be the App-V admin’s</span></span>

-   <span data-ttu-id="69631-126">Nom du serveur sur lequel est installé le serveur de gestion de l’application-V</span><span class="sxs-lookup"><span data-stu-id="69631-126">Name of the server where App-V Management Server will be installed</span></span>

**<span data-ttu-id="69631-127">Informations devant être renvoyées aux administrateurs d’infrastructure</span><span class="sxs-lookup"><span data-stu-id="69631-127">Information to be returned to the Infrastructure administrators</span></span>**

-   <span data-ttu-id="69631-128">Nom du serveur de base de données ou de l’instance et du nom de la base de données App-V.</span><span class="sxs-lookup"><span data-stu-id="69631-128">Name of the database server or instance and the name of the App-V database</span></span>

<span data-ttu-id="69631-129">Lorsque la base de données est préparée, les administrateurs de l’application-V peuvent exécuter l’installation d’App-V sans privilèges d’administrateur SQL.</span><span class="sxs-lookup"><span data-stu-id="69631-129">Once the database has been prepared, the App-V administrators can run the App-V installation without SQL administrator privileges.</span></span>

### <span data-ttu-id="69631-130">Utiliser les scripts de configuration SQL</span><span class="sxs-lookup"><span data-stu-id="69631-130">Using the SQL Setup Scripts</span></span>

**<span data-ttu-id="69631-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="69631-131">Requirements</span></span>**

<span data-ttu-id="69631-132">Voici une liste des conditions requises pour utiliser les scripts situés dans le dossier support\\createdb à la racine de l’emplacement d’extraction sélectionné.</span><span class="sxs-lookup"><span data-stu-id="69631-132">The following is a list of requirements for using the scripts which are located in the support\\createdb folder at the root of the selected extract location.</span></span>

-   <span data-ttu-id="69631-133">Les scripts doivent être copiés vers un emplacement accessible en écriture sur l’ordinateur sur lequel ils seront exécutés (veillez à supprimer l’attribut lecture seule de ces scripts une fois qu’ils ont été copiés) et les outils clients SQL doivent être chargés sur cet ordinateur (OSQL est requis uniquement pour exécuter les fichiers de commandes d’exemple sur l’ordinateur local).</span><span class="sxs-lookup"><span data-stu-id="69631-133">Scripts must be copied to a writeable location on the computer where they will be run (be sure to remove the read only attribute from these scripts after they have been copied) and SQL client tools must be loaded on that computer (osql is only required for running the sample batch files on the local computer).</span></span>

-   <span data-ttu-id="69631-134">SQL Server doit prendre en charge l’authentification Windows.</span><span class="sxs-lookup"><span data-stu-id="69631-134">The SQL Server must support Windows Authentication.</span></span>

-   <span data-ttu-id="69631-135">Assurez-vous que les services SQL Server instance et SQL Agent s’exécutent.</span><span class="sxs-lookup"><span data-stu-id="69631-135">Ensure that the SQL Server Instance and SQL Agent Service are running.</span></span>

-   <span data-ttu-id="69631-136">Connectez-vous à l’aide d’un compte de domaine qui est un administrateur SQL (sysadmin) sur l’ordinateur sur lequel effectuer les scripts.</span><span class="sxs-lookup"><span data-stu-id="69631-136">Log on with a domain account that is a SQL administrator (sysadmin) on the computer where the scripts will be done.</span></span>

<span data-ttu-id="69631-137">Les scripts s’exécutent sous les informations d’identification de domaine de l’utilisateur connecté.</span><span class="sxs-lookup"><span data-stu-id="69631-137">The scripts runs under the logged-on user’s domain credentials.</span></span>

**<span data-ttu-id="69631-138">Création de base de données à l’aide de scripts SQL</span><span class="sxs-lookup"><span data-stu-id="69631-138">Database Creation Using SQL Scripts</span></span>**

**<span data-ttu-id="69631-139">Tâches devant être effectuées par les administrateurs SQL:</span><span class="sxs-lookup"><span data-stu-id="69631-139">Tasks to be performed by SQL administrators:</span></span>**

1.  <span data-ttu-id="69631-140">Copiez les scripts contenus dans le dossier support\\createdb à partir de la racine de l’emplacement d’extraction sélectionné vers l’ordinateur sur lequel les scripts seront exécutés.</span><span class="sxs-lookup"><span data-stu-id="69631-140">Copy the scripts contained in the support\\createdb folder from the root of the selected extract location to the computer where the scripts will be run.</span></span> <span data-ttu-id="69631-141">Pour que les scripts s’exécutent correctement, les fichiers suivants doivent être appelés dans l’ordre présenté ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="69631-141">The following files are required for the scripts to run properly and must be called in the order presented below.</span></span>

    -   <span data-ttu-id="69631-142">Database. SQL</span><span class="sxs-lookup"><span data-stu-id="69631-142">database.sql</span></span>

    -   <span data-ttu-id="69631-143">rôles. SQL</span><span class="sxs-lookup"><span data-stu-id="69631-143">roles.sql</span></span>

    -   <span data-ttu-id="69631-144">Tableau \ _CODES. SQL</span><span class="sxs-lookup"><span data-stu-id="69631-144">table\_CODES.sql</span></span>

    -   <span data-ttu-id="69631-145">fonctions \ _before \ _tables. SQL</span><span class="sxs-lookup"><span data-stu-id="69631-145">functions\_before\_tables.sql</span></span>

    -   <span data-ttu-id="69631-146">tables. SQL</span><span class="sxs-lookup"><span data-stu-id="69631-146">tables.sql</span></span>

    -   <span data-ttu-id="69631-147">fonctions. SQL</span><span class="sxs-lookup"><span data-stu-id="69631-147">functions.sql</span></span>

    -   <span data-ttu-id="69631-148">vues. SQL</span><span class="sxs-lookup"><span data-stu-id="69631-148">views.sql</span></span>

    -   <span data-ttu-id="69631-149">procédures. SQL</span><span class="sxs-lookup"><span data-stu-id="69631-149">procedures.sql</span></span>

    -   <span data-ttu-id="69631-150">déclencheurs. SQL</span><span class="sxs-lookup"><span data-stu-id="69631-150">triggers.sql</span></span>

    -   <span data-ttu-id="69631-151">données \ _codes. SQL</span><span class="sxs-lookup"><span data-stu-id="69631-151">data\_codes.sql</span></span>

    -   <span data-ttu-id="69631-152">données \ _messages. SQL</span><span class="sxs-lookup"><span data-stu-id="69631-152">data\_messages.sql</span></span>

    -   <span data-ttu-id="69631-153">données \ _defaults. SQL</span><span class="sxs-lookup"><span data-stu-id="69631-153">data\_defaults.sql</span></span>

    -   <span data-ttu-id="69631-154">alertes \ _jobs. SQL</span><span class="sxs-lookup"><span data-stu-id="69631-154">alerts\_jobs.sql</span></span>

    -   <span data-ttu-id="69631-155">DBVERSION. SQL</span><span class="sxs-lookup"><span data-stu-id="69631-155">dbversion.sql</span></span>

2.  <span data-ttu-id="69631-156">Examinez et modifiez, si nécessaire, le `database.sql` fichier.</span><span class="sxs-lookup"><span data-stu-id="69631-156">Review and modify, if necessary, the `database.sql` file.</span></span> <span data-ttu-id="69631-157">Les paramètres par défaut nommeront la base de données «APPVIRTDB».</span><span class="sxs-lookup"><span data-stu-id="69631-157">The default settings will name the database “APPVIRTDB.”</span></span>

    -   <span data-ttu-id="69631-158">Le cas échéant, remplacez `APPVIRTDB` les instances de par le `database name` qui sera utilisé.</span><span class="sxs-lookup"><span data-stu-id="69631-158">If necessary replace instances of `APPVIRTDB` with the `database name` that will be used.</span></span>

    -   <span data-ttu-id="69631-159">Remplacez la `FILENAME` propriété du script par le chemin d’accès approprié pour le serveur SQL sur lequel la base de données sera créée.</span><span class="sxs-lookup"><span data-stu-id="69631-159">Modify the `FILENAME` property in the script with the appropriate path for the SQL Server where the database will be created.</span></span>

3.  <span data-ttu-id="69631-160">Examinez et modifiez, si nécessaire, la `database name [APPVIRTDB]` dans le `roles.sql` fichier qui a été utilisé dans le fichier Database. Sql.</span><span class="sxs-lookup"><span data-stu-id="69631-160">Review and modify, if necessary, the `database name [APPVIRTDB]` in the `roles.sql` file that was used in the database.sql file.</span></span>

****

### <span data-ttu-id="69631-161">Exemple illustrant comment automatiser le processus à l’aide de fichiers de commandes</span><span class="sxs-lookup"><span data-stu-id="69631-161">Example of how to automate the process using batch files</span></span>

<span data-ttu-id="69631-162">S’il est utilisé, les deux exemples de fichiers de commandes proposés exécutent les scripts SQL de la façon suivante:</span><span class="sxs-lookup"><span data-stu-id="69631-162">If used, the two sample batch files provided run the SQL scripts in the following manner:</span></span>

1.  **<span data-ttu-id="69631-163">Create\_schema.bat (1)</span><span class="sxs-lookup"><span data-stu-id="69631-163">Create\_schema.bat (1)</span></span>**

    -   <span data-ttu-id="69631-164">Database. SQL</span><span class="sxs-lookup"><span data-stu-id="69631-164">database.sql</span></span>

    -   <span data-ttu-id="69631-165">rôles. SQL</span><span class="sxs-lookup"><span data-stu-id="69631-165">roles.sql</span></span>

2.  **<span data-ttu-id="69631-166">Create\_tables.bat (2)</span><span class="sxs-lookup"><span data-stu-id="69631-166">Create\_tables.bat (2)</span></span>**

    -   <span data-ttu-id="69631-167">Tableau \ _CODES. SQL</span><span class="sxs-lookup"><span data-stu-id="69631-167">table\_CODES.sql</span></span>

    -   <span data-ttu-id="69631-168">fonctions \ _before \ _tables. SQL</span><span class="sxs-lookup"><span data-stu-id="69631-168">functions\_before\_tables.sql</span></span>

    -   <span data-ttu-id="69631-169">tables. SQL</span><span class="sxs-lookup"><span data-stu-id="69631-169">tables.sql</span></span>

    -   <span data-ttu-id="69631-170">fonctions. SQL</span><span class="sxs-lookup"><span data-stu-id="69631-170">functions.sql</span></span>

    -   <span data-ttu-id="69631-171">vues. SQL</span><span class="sxs-lookup"><span data-stu-id="69631-171">views.sql</span></span>

    -   <span data-ttu-id="69631-172">procédures. SQL</span><span class="sxs-lookup"><span data-stu-id="69631-172">procedures.sql</span></span>

    -   <span data-ttu-id="69631-173">déclencheurs. SQL</span><span class="sxs-lookup"><span data-stu-id="69631-173">triggers.sql</span></span>

    -   <span data-ttu-id="69631-174">données \ _codes. SQL</span><span class="sxs-lookup"><span data-stu-id="69631-174">data\_codes.sql</span></span>

    -   <span data-ttu-id="69631-175">données \ _messages. SQL</span><span class="sxs-lookup"><span data-stu-id="69631-175">data\_messages.sql</span></span>

    -   <span data-ttu-id="69631-176">données \ _defaults. SQL</span><span class="sxs-lookup"><span data-stu-id="69631-176">data\_defaults.sql</span></span>

    -   <span data-ttu-id="69631-177">alertes \ _jobs. SQL</span><span class="sxs-lookup"><span data-stu-id="69631-177">alerts\_jobs.sql</span></span>

    -   <span data-ttu-id="69631-178">DBVERSION. SQL</span><span class="sxs-lookup"><span data-stu-id="69631-178">dbversion.sql</span></span>

**<span data-ttu-id="69631-179">Remarque</span><span class="sxs-lookup"><span data-stu-id="69631-179">Note</span></span>**  
<span data-ttu-id="69631-180">La modification des scripts doit être soigneusement prise en considération et ne doit être effectuée qu’par une personne ayant les connaissances appropriées.</span><span class="sxs-lookup"><span data-stu-id="69631-180">Careful consideration when modifying the scripts must be taken and should only be done by someone with the appropriate knowledge.</span></span> <span data-ttu-id="69631-181">Par ailleurs, les fichiers d’exemple présentés uniquement aux éléments suivants doivent être modifiés: **create\_schema.bat**, **create\_tables.bat**, **Database. SQL**et **rôles. SQL**.</span><span class="sxs-lookup"><span data-stu-id="69631-181">Also, of the sample files presented only the following should be changed: **create\_schema.bat**, **create\_tables.bat**, **database.sql**, and **roles.sql**.</span></span> <span data-ttu-id="69631-182">Aucun autre fichier ne doit être modifié de quelque manière que ce qui pourrait entraîner la création incorrecte de la base de données, ce qui entraînera l’échec de l’installation des services App-V.</span><span class="sxs-lookup"><span data-stu-id="69631-182">All other files should not be modified in any way as this could cause the database to be created incorrectly, which will lead to the failure of App-V services to be installed.</span></span>



<span data-ttu-id="69631-183">Les deux exemples de fichiers de commandes doivent être placés dans le même répertoire que le reste des scripts SQL sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="69631-183">The two sample batch files must be placed in the same directory where the rest of the SQL scripts were copied to on the computer.</span></span>

1.  <span data-ttu-id="69631-184">Exécutez l’exemple de fichier **create\_schema.bat** pour créer la base de données.</span><span class="sxs-lookup"><span data-stu-id="69631-184">Run the sample **create\_schema.bat** file to create the database.</span></span> <span data-ttu-id="69631-185">L’exécution de ce script peut prendre quelques secondes et ne peut pas être interrompu.</span><span class="sxs-lookup"><span data-stu-id="69631-185">This script will take several seconds to complete and should not be interrupted.</span></span>

    -   <span data-ttu-id="69631-186">Exécuter le fichier de création de schema.bat à partir du répertoire dans lequel il a été copié.</span><span class="sxs-lookup"><span data-stu-id="69631-186">Run the create schema.bat file from the directory where it was copied to.</span></span> <span data-ttu-id="69631-187">La syntaxe est la suivante: "Create\_schema.bat `SQLSERVERNAME` "</span><span class="sxs-lookup"><span data-stu-id="69631-187">Syntax is: “Create\_schema.bat `SQLSERVERNAME`”</span></span>

        ![AppV46SQLcreatebat](images/appv46sqlcreatebat.bmp)

    -   <span data-ttu-id="69631-189">Si ce script échoue lors de la création de la nouvelle base de données «APPVIRTDB», vérifiez le journal comme indiqué pour corriger le problème.</span><span class="sxs-lookup"><span data-stu-id="69631-189">If this script fails during the creation of the new “APPVIRTDB” database, check the log as indicated to correct the issue.</span></span> <span data-ttu-id="69631-190">Il est nécessaire de supprimer la base de données créée à l’aide d’une exécution partielle des scripts afin de vous assurer que les tentatives suivantes fonctionneront correctement.</span><span class="sxs-lookup"><span data-stu-id="69631-190">It will be necessary to delete the database that was created with a partial running of the scripts in order to ensure that subsequent attempts will work properly.</span></span>

2.  <span data-ttu-id="69631-191">Exécutez le `create_tables.bat` fichier pour créer les tables dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="69631-191">Run the `create_tables.bat` file to create the tables in the database.</span></span> <span data-ttu-id="69631-192">L’exécution de ce script peut prendre quelques secondes et ne peut pas être interrompu.</span><span class="sxs-lookup"><span data-stu-id="69631-192">This script will take several seconds to complete and should not be interrupted.</span></span>

    -   <span data-ttu-id="69631-193">Exécutez le fichier create\_tables.bat à partir du répertoire dans lequel il a été copié.</span><span class="sxs-lookup"><span data-stu-id="69631-193">Run the create\_tables.bat file from the directory where it was copied.</span></span> <span data-ttu-id="69631-194">La syntaxe est la suivante: "create\_tables.bat `SQLSERVERNAME DBNAME` "</span><span class="sxs-lookup"><span data-stu-id="69631-194">Syntax is: “create\_tables.bat `SQLSERVERNAME DBNAME`”</span></span>

        ![create\-table.bat SQL App-v 4,6](images/appv46sqlcreate-tablebat.gif)

        <span data-ttu-id="69631-196">Si le script échoue lors de la création des tables, recherchez le journal comme indiqué pour corriger le problème.</span><span class="sxs-lookup"><span data-stu-id="69631-196">If the script fails during the creation of the tables, check the log as indicated to correct the issue.</span></span> <span data-ttu-id="69631-197">Il est nécessaire de supprimer la base de données et de lancer create\_schema.bat avant d’essayer d’exécuter le fichier create\_tables.bat lors de toutes les tentatives ultérieures.</span><span class="sxs-lookup"><span data-stu-id="69631-197">It will be necessary to delete the database and run create\_schema.bat before attempting to run the create\_tables.bat file on all subsequent attempts.</span></span>

### <span data-ttu-id="69631-198">Définir des autorisations sur la base de données App-V</span><span class="sxs-lookup"><span data-stu-id="69631-198">Setting permissions on the App-V database</span></span>

<span data-ttu-id="69631-199">Les comptes suivants doivent être créés sur le serveur SQL Server avec des autorisations et des rôles spécifiques à la nouvelle base de données pour l’installation, le déploiement et l’administration continue de l’environnement App-V.</span><span class="sxs-lookup"><span data-stu-id="69631-199">The following accounts will need to be created on the SQL server with specific permissions and roles to the new database for the installation, deployment and ongoing administration of the App-V environment.</span></span>

-   <span data-ttu-id="69631-200">Créez une connexion pour le groupe d’administrateurs d’application-V sur le serveur SQL Server et la base de données APPVIRTDB pour les utilisateurs «domain\\App-V admins» (où «Domain» et «App-V admins» seront modifiés pour refléter votre propre environnement) et ajoutez-les au rôle de base de données SFTAdmin et SFTEveryone.</span><span class="sxs-lookup"><span data-stu-id="69631-200">Create a login for the App-V administrators group on the SQL Server and the APPVIRTDB database for the “domain\\App-V Admins” (where “domain” and “App-V Admins” will be changed to reflect your own environment) and add them to the SFTAdmin and SFTEveryone database role.</span></span>

    ![autorisations et rôles du jeu de scripts SQL App-v 4,6](images/appv46sqlscriptsetpermsroles.gif)

-   <span data-ttu-id="69631-202">Octroyez à ce groupe l’autorisation «afficher toute définition» au niveau global (cela permet au service de configuration du serveur de gestion des applications Microsoft d’applications de vérifier que la connexion au serveur de gestion existe déjà).</span><span class="sxs-lookup"><span data-stu-id="69631-202">Grant this group “VIEW ANY DEFINITION” permission at the global level (This allows the Microsoft Application Virtualization Management Server setup process to verify that the Management Server login already exists).</span></span> <span data-ttu-id="69631-203">Sous MS-SQL 2005 et les restrictions d’accès au-dessus des métadonnées contenues dans Master. db ont été ajoutées.</span><span class="sxs-lookup"><span data-stu-id="69631-203">Under MS-SQL 2005 and above access restrictions to the metadata contained in master.db were added.</span></span> <span data-ttu-id="69631-204">Par défaut, l’utilisateur créé lors de l’étape précédente ne dispose pas des droits nécessaires à l’installation du serveur.</span><span class="sxs-lookup"><span data-stu-id="69631-204">The user created in the previous step will by default not have the rights needed by the server installation.</span></span> <span data-ttu-id="69631-205">Ouvrez les propriétés de la connexion précédemment créée, propriétés de connexion- &gt; consécurisées.</span><span class="sxs-lookup"><span data-stu-id="69631-205">Open the properties of the previously created login, Login Properties-&gt;Securables.</span></span> <span data-ttu-id="69631-206">Ajoutez l’instance de base de données et activez «accorder» pour «afficher une définition», comme illustré dans la capture d’écran ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="69631-206">Add the Database instance and enable “GRANT” for “View any definition” as shown in the screenshot below.</span></span>

    ![script SQL App-v 4,6 Grant Perm pour afficher tout déf](images/appv46sqlscriptviewanydef.gif)

-   <span data-ttu-id="69631-208">Ajoutez un rôle au rôle \ _ASSIGNMENTS table pour la connexion créée lors de l’étape précédente, afin de permettre aux administrateurs d’applications d’accéder à la console de gestion des applications d’application, à l’aide des rôles = «ADMIN» et du groupe \ _ref = «administrateurs domain\\App-V» (où «Domain» et «App-V admins» seront modifiés pour refléter votre environnement.</span><span class="sxs-lookup"><span data-stu-id="69631-208">Add a role to the ROLE\_ASSIGNMENTS table for the login created in the previous step to allow App-V administrators access to the Application Virtualization Management Console, with role = “ADMIN” and group\_ref = “domain\\App-V Admins” (where “domain” and “App-V Admins” will be changed to reflect your own environment).</span></span>

    ![attribution de rôle de script App-v 4,6 SQL](images/appv46sqlscriptroleassign.gif)

-   <span data-ttu-id="69631-210">Créer une connexion pour SQL Server et base de données App-V pour le serveur de gestion.</span><span class="sxs-lookup"><span data-stu-id="69631-210">Create login for SQL Server and App-V database for the Management Server.</span></span> <span data-ttu-id="69631-211">Ce compte est utilisé par le serveur de gestion des applications virtuelles Microsoft pour se connecter au magasin de données, et il est tenu de traiter les demandes des clients pour les applications diffusées.</span><span class="sxs-lookup"><span data-stu-id="69631-211">This account is used by the Microsoft Application Virtualization Management Server to connect to the data store and is responsible for servicing client requests for streamed applications.</span></span> <span data-ttu-id="69631-212">Vous avez le choix entre deux options, selon l’emplacement de l’installation de SQL Server et de Management Server:</span><span class="sxs-lookup"><span data-stu-id="69631-212">There are two options, depending on where the SQL Server and Management Server are to be installed:</span></span>

    1.  <span data-ttu-id="69631-213">Si le serveur de gestion et SQL Server vont être installés sur le même ordinateur, ajoutez une connexion pour le SERVICE AUTHORITY\\NETWORK NT et ajoutez-le aux rôles de base de données SFTUser et SFTEveryone.</span><span class="sxs-lookup"><span data-stu-id="69631-213">If Management Server and SQL Server are going to be installed on the same computer, add a login for NT AUTHORITY\\NETWORK SERVICE and add it to the SFTUser and SFTEveryone database roles.</span></span>

    2.  <span data-ttu-id="69631-214">Si le serveur de gestion et SQL Server doivent être installés sur plusieurs ordinateurs, ajoutez un nom de connexion pour «domain\\App-V Server Name $» (où «App-V Server Name» est le nom du serveur sur lequel est installé le serveur d’administration d’applications-V, puis ajoutez-le aux rôles de base de données SFTUser et SFTEveryone.</span><span class="sxs-lookup"><span data-stu-id="69631-214">If the Management Server and SQL Server are to be installed on different computers, add a login for “domain\\App-V Server Name$” (where “App-V Server Name” is the name of the server where the App-V Management Server will be installed) and add it to the SFTUser and SFTEveryone database roles.</span></span>

-   <span data-ttu-id="69631-215">Ouvrez la fenêtre de requête dans la fenêtre SQL et exécutez le code SQL suivant:</span><span class="sxs-lookup"><span data-stu-id="69631-215">Open the query window on the SQL window and run the following SQL:</span></span>

    ``` syntax
    USE APPVIRTDB
    GRANT ALTER ON ROLE::SFTuser TO “domain\App-V Admins”
    ```

    <span data-ttu-id="69631-216">Où APPVIRTDB est le nom de la base de données App-V créée sur le serveur SQL lors de l’étape précédente, et l’utilisateur qui va procéder à l’installation de l’application-v Server doit être membre de «domain\\App-V admins» (où «Domain» et «App-V admins» seront modifiés pour refléter votre environnement.</span><span class="sxs-lookup"><span data-stu-id="69631-216">Where the APPVIRTDB is the name of the App-V Database created on the SQL Server in the previous step, and the user who is going to do the install of the App-v server needs to be a member of “domain\\App-V Admins” (where “domain” and “App-V Admins” will be changed to reflect your own environment).</span></span>

### <span data-ttu-id="69631-217">Tâches devant être effectuées par les administrateurs d’infrastructure</span><span class="sxs-lookup"><span data-stu-id="69631-217">Tasks to be performed by the Infrastructure administrators</span></span>

1.  <span data-ttu-id="69631-218">L’administrateur du groupe «administrateurs App-V» doit installer App-V.</span><span class="sxs-lookup"><span data-stu-id="69631-218">Administrator in the “App-V Admins” group should install App-V.</span></span>

    <span data-ttu-id="69631-219">Utilisez les informations fournies par les administrateurs SQL pour sélectionner le serveur SQL et la base de données créés aux étapes précédentes.</span><span class="sxs-lookup"><span data-stu-id="69631-219">Use information from the SQL administrators for selecting the SQL Server and database created in the previous steps.</span></span>

2.  <span data-ttu-id="69631-220">L’administrateur du groupe «administrateurs d’application-V» se connecte à la console de gestion de l’application virtualisation et supprime les objets suivants de la console de gestion.</span><span class="sxs-lookup"><span data-stu-id="69631-220">Administrator in the “App-V Admins” group logs in to Application Virtualization Management Console and deletes the following objects from the Management Console.</span></span>

    **<span data-ttu-id="69631-221">Warning</span><span class="sxs-lookup"><span data-stu-id="69631-221">Warning</span></span>**  
    <span data-ttu-id="69631-222">Ce paramètre est requis lorsque la configuration classique remplit certains enregistrements de la base de données qui ne sont pas remplis si vous exécutez l’installation sur une base de données existante.</span><span class="sxs-lookup"><span data-stu-id="69631-222">This is required as the traditional setup populates certain records in the database that are not populated if you run the install against an already existing database.</span></span> <span data-ttu-id="69631-223">Supprimez les objets suivants:</span><span class="sxs-lookup"><span data-stu-id="69631-223">Delete the following objects:</span></span>

    -   <span data-ttu-id="69631-224">Sous «groupes de serveurs», «groupe de serveurs par défaut», «supprimer» serveur de gestion des applications virtuelles»</span><span class="sxs-lookup"><span data-stu-id="69631-224">Under “Server Groups,” “Default Server Group,” delete “Application Virtualization Management Server”</span></span>

    -   <span data-ttu-id="69631-225">Sous groupes de serveurs, "supprimer" groupe de serveurs par défaut "</span><span class="sxs-lookup"><span data-stu-id="69631-225">Under “Server Groups,” delete “Default Server Group”</span></span>

    -   <span data-ttu-id="69631-226">Sous stratégies du fournisseur, "supprimer" le fournisseur par défaut "</span><span class="sxs-lookup"><span data-stu-id="69631-226">Under “Provider Policies,” delete “Default Provider”</span></span>



3.  <span data-ttu-id="69631-227">L’administrateur dans le groupe d’administrateurs App-V doit alors créer les éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="69631-227">Administrator in the App-V admins group should then create:</span></span>

    -   <span data-ttu-id="69631-228">Sous stratégies du fournisseur, créez une nouvelle stratégie de fournisseur.</span><span class="sxs-lookup"><span data-stu-id="69631-228">Under “Provider Policies,” create a New Provider Policy</span></span>

    -   <span data-ttu-id="69631-229">Créer un groupe de serveurs par défaut</span><span class="sxs-lookup"><span data-stu-id="69631-229">Create a “Default Server Group”</span></span>

        **<span data-ttu-id="69631-230">Remarque</span><span class="sxs-lookup"><span data-stu-id="69631-230">Note</span></span>**  
        <span data-ttu-id="69631-231">Vous devez créer un groupe «serveur par défaut» même si vous ne l’utilisez pas.</span><span class="sxs-lookup"><span data-stu-id="69631-231">You must create a “Default Server” group even if you will not be used.</span></span> <span data-ttu-id="69631-232">Le programme d’installation de serveur recherche uniquement le «groupe de serveurs par défaut» lorsque vous tentez d’ajouter le serveur.</span><span class="sxs-lookup"><span data-stu-id="69631-232">The server installer only looks for the "Default Server Group" when trying to add the server.</span></span>  <span data-ttu-id="69631-233">S’il n’y a pas de «groupe de serveurs par défaut», l’installation échoue.</span><span class="sxs-lookup"><span data-stu-id="69631-233">If there is no "Default Server Group" then the installation will fail.</span></span> <span data-ttu-id="69631-234">Si vous envisagez d’utiliser des groupes de serveurs autres que ceux par défaut qui conviennent, il est nécessaire de conserver le «groupe de serveurs par défaut» si vous envisagez d’ajouter d’autres serveurs d’administration d’applications à votre infrastructure.</span><span class="sxs-lookup"><span data-stu-id="69631-234">If you plan on using server groups other than the default that is fine, it’s just necessary to retain the "Default Server Group" if you plan on adding subsequent App-V Management Servers to your infrastructure.</span></span>



~~~
-   Assign the App-V Users Group to the New Provider Policy created above

-   Under “Server Groups,” create a New Server Group, specifying the New Provider Policy

-   Under the New Server group, create a New Application Virtualization Management Server

    **Important**  
    Do not restart the service before completing all of the above steps!



-   Administrator restarts the Application Virtualization Management Server service.
~~~

## <span data-ttu-id="69631-235">Conclusion</span><span class="sxs-lookup"><span data-stu-id="69631-235">Conclusion</span></span>


<span data-ttu-id="69631-236">En conclusion, les informations contenues dans ce document permettent à un administrateur de travailler avec les administrateurs SQL pour développer un chemin de déploiement adapté aux divisions de sécurité et d’administration au sein d’une organisation.</span><span class="sxs-lookup"><span data-stu-id="69631-236">In conclusion, the information in this document allows an administrator to work with the SQL administrators to develop a deployment path that works for the security and administrative divisions in an organization.</span></span> <span data-ttu-id="69631-237">Après avoir lu ce document et testé les tâches détaillées, un administrateur doit être prêt à implémenter son infrastructure App-V dans ce type d’environnement.</span><span class="sxs-lookup"><span data-stu-id="69631-237">After reading this document and testing the tasks documented, an administrator should be ready to implement their App-V infrastructure in this type of environment.</span></span>









