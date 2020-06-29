---
title: Comment déployer les bases de données App-V à l'aide de scripts SQL
description: Comment déployer les bases de données App-V à l'aide de scripts SQL
author: dansimp
ms.assetid: 1183b1bc-d4d7-4914-a049-06e82bf2d96d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4695d105c1aa6732efb6b8ed05169cf29e7f972b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805478"
---
# <span data-ttu-id="47281-103">Comment déployer les bases de données App-V à l'aide de scripts SQL</span><span class="sxs-lookup"><span data-stu-id="47281-103">How to Deploy the App-V Databases by Using SQL Scripts</span></span>

<span data-ttu-id="47281-104">Pour utiliser les scripts SQL plutôt que le programme d’installation Windows, procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="47281-104">Use the following instructions to use SQL scripts, rather than the Windows Installer, to:</span></span>

- <span data-ttu-id="47281-105">Installer les bases de données App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="47281-105">Install the App-V 5.1 databases</span></span>
- <span data-ttu-id="47281-106">Mettre à niveau les bases de données d’application-V vers une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="47281-106">Upgrade the App-V databases to a later version</span></span>

> [!NOTE]
> <span data-ttu-id="47281-107">Si vous avez déjà déployé la base de données App-V 5,0 SP3, les scripts SQL ne sont pas obligés de procéder à la mise à niveau vers App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="47281-107">If you have already deployed the App-V 5.0 SP3 database, the SQL scripts are not required to upgrade to App-V 5.1.</span></span>

## <span data-ttu-id="47281-108">Comment installer les bases de données App-V à l’aide de scripts SQL</span><span class="sxs-lookup"><span data-stu-id="47281-108">How to install the App-V databases by using SQL scripts</span></span>

1. <span data-ttu-id="47281-109">Avant d’installer les scripts de base de données, passez en revue les termes du contrat de licence App-V et conservez-en une copie.</span><span class="sxs-lookup"><span data-stu-id="47281-109">Before you install the database scripts, review and keep a copy of the App-V license terms.</span></span> <span data-ttu-id="47281-110">En exécutant les scripts de base de données, vous acceptez les termes du contrat de licence.</span><span class="sxs-lookup"><span data-stu-id="47281-110">By running the database scripts, you are agreeing to the license terms.</span></span> <span data-ttu-id="47281-111">Si vous n’acceptez pas le logiciel, vous ne devez pas l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="47281-111">If you do not accept them, you should not use this software.</span></span>
1. <span data-ttu-id="47281-112">Copiez l' **appv\_server\_setup.exe** du média App-V Release vers un emplacement temporaire.</span><span class="sxs-lookup"><span data-stu-id="47281-112">Copy the **appv\_server\_setup.exe** from the App-V release media to a temporary location.</span></span>
1. <span data-ttu-id="47281-113">À partir d’une invite de commandes, exécutez **appv\_server\_setup.exe** et spécifiez un emplacement temporaire pour extraire les scripts de la base de données.</span><span class="sxs-lookup"><span data-stu-id="47281-113">From a command prompt, run **appv\_server\_setup.exe** and specify a temporary location for extracting the database scripts.</span></span>

    <span data-ttu-id="47281-114">Exemple: appv\_server\_setup.exe/layout c:\\ &lt; _chemin d’emplacement temporaire_&gt;</span><span class="sxs-lookup"><span data-stu-id="47281-114">Example: appv\_server\_setup.exe /layout c:\\&lt;_temporary location path_&gt;</span></span>

1. <span data-ttu-id="47281-115">Naviguez jusqu’à l’emplacement temporaire que vous avez créé, ouvrez le dossier **DatabaseScripts** extrait et examinez le fichier Readme.txt approprié pour obtenir des instructions:</span><span class="sxs-lookup"><span data-stu-id="47281-115">Browse to the temporary location that you created, open the extracted **DatabaseScripts** folder, and review the appropriate Readme.txt file for instructions:</span></span>

    | <span data-ttu-id="47281-116">Base de données</span><span class="sxs-lookup"><span data-stu-id="47281-116">Database</span></span> | <span data-ttu-id="47281-117">Emplacement du fichier Readme.txt à utiliser</span><span class="sxs-lookup"><span data-stu-id="47281-117">Location of Readme.txt file to use</span></span> |
    |--|--|
    | <span data-ttu-id="47281-118">Base de données de gestion</span><span class="sxs-lookup"><span data-stu-id="47281-118">Management database</span></span> | <span data-ttu-id="47281-119">Sous-dossier ManagementDatabase</span><span class="sxs-lookup"><span data-stu-id="47281-119">ManagementDatabase subfolder</span></span> |
    | <span data-ttu-id="47281-120">Base de données de création de rapports</span><span class="sxs-lookup"><span data-stu-id="47281-120">Reporting database</span></span> | <span data-ttu-id="47281-121">Sous-dossier ReportingDatabase</span><span class="sxs-lookup"><span data-stu-id="47281-121">ReportingDatabase subfolder</span></span> |

> [!CAUTION]
> <span data-ttu-id="47281-122">Le fichier readme.txt dans le sous-dossier ManagementDatabase est obsolète.</span><span class="sxs-lookup"><span data-stu-id="47281-122">The readme.txt file in the ManagementDatabase subfolder is out of date.</span></span> <span data-ttu-id="47281-123">Les informations contenues dans les fichiers Lisez-moi mis à jour ci-dessous sont les plus récentes et doivent remplacer les informations Lisez-moi fournies dans les dossiers **DatabaseScripts** .</span><span class="sxs-lookup"><span data-stu-id="47281-123">The information in the updated readme files below is the most current and should supersede the readme information provided in the **DatabaseScripts** folders.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="47281-124">Le script InsertVersionInfo. SQL n’est pas requis pour les versions de la base de données de gestion App-V ultérieure à l’application-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="47281-124">The InsertVersionInfo.sql script is not required for versions of the App-V management database later than App-V 5.0 SP3.</span></span>

<span data-ttu-id="47281-125">Le script Permissions. SQL doit être mis à jour en suivant l' **étape 2** de [l’article 3031340](https://support.microsoft.com/kb/3031340)de la base de connaissances.</span><span class="sxs-lookup"><span data-stu-id="47281-125">The Permissions.sql script should be updated according to **Step 2** in [KB article 3031340](https://support.microsoft.com/kb/3031340).</span></span> <span data-ttu-id="47281-126">L' **étape 1** n’est pas requise pour les versions de App-v ultérieures à l’application-v 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="47281-126">**Step 1** is not required for versions of App-V later than App-V 5.0 SP3.</span></span>

## <span data-ttu-id="47281-127">Contenu du fichier Lisezmoi de la base de données de gestion mis à jour</span><span class="sxs-lookup"><span data-stu-id="47281-127">Updated management database README file content</span></span>

```plaintext
******************************************************************
Before you install and use the Application Virtualization Database Scripts you must:
1.Review the Microsoft Application Virtualization Server 5.0 license terms.
2.Print and retain a copy of the license terms for your records.
By running the Microsoft Application Virtualization Database Scripts you agree to such license terms.  If you do not accept them, do not use the software.
******************************************************************


Steps to install "AppVManagement" schema in SQL SERVER.


## PREREQUISITES:

 1. Review the installation package.  The following files MUST exist:

    SQL files
    ---------
    Database.sql
    CreateTables.sql
    CreateStoredProcs.sql
    UpdateTables.sql
    Permissions.sql

 2. Ensure the target SQL Server instance and SQL Server Agent service are running.

 3. If you are not running the scripts directly on the server, ensure the
    necessary SQL Server client software is installed and available from
    the specified location.  Specifically, the "osql" command must
##     be supported for these scripts to run.



## PREPARATION:

 1. Review the database.sql file and modify as necessary.  Although the
    defaults are likely sufficient, it is suggested that the following
    settings be reviewed:

    DATABASE - ensure name is satisfactory - default is "AppVManagement".

 2. Review the Permissions.sql file and provide all the necessary account information
    for setting up read and write access on the database. Note: Default settings
##     in the file will not work.



## INSTALLATION:

 1. Run the database.sql against the "master" database.  Your user
    credential must have the ability to create databases.
    This script will create the database.

 2. Run the following scripts against the "AppVManagement" database using the
    same account as above in order.

    CreateTables.sql
    CreateStoredProcs.sql
    UpdateTables.sql
##     Permissions.sql

```

## <span data-ttu-id="47281-128">Contenu du fichier Lisezmoi de la base de données de rapports mis à jour</span><span class="sxs-lookup"><span data-stu-id="47281-128">Updated reporting database README file content</span></span>

```plaintext
******************************************************************
Before you install and use the Application Virtualization Database Scripts you must:
1.Review the Microsoft Application Virtualization Server 5.0 license terms.
2.Print and retain a copy of the license terms for your records.
By running the Microsoft Application Virtualization Database Scripts you agree to such license terms.  If you do not accept them, do not use the software.
******************************************************************

Steps to install "AppVReporting" schema in SQL SERVER.


## PREREQUISITES:

 1. Review the installation package.  The following files MUST exist:

    SQL files
    ---------
    Database.sql
    UpgradeDatabase.sql
    CreateTables.sql
    CreateReportingStoredProcs.sql
    CreateStoredProcs.sql
    CreateViews.sql
    InsertVersionInfo.sql
    Permissions.sql
    ScheduleReportingJob.sql

 2. Ensure the target SQL Server instance and SQL Server Agent service are running.

 3. If you are not running the scripts directly on the server, ensure the 
    necessary SQL Server client software is installed and executable from
    the location you have chosen.  Specifically, the "osql" command must
##     be supported for these scripts to run.



## PREPARATION:

 1. Review the database.sql file and modify as necessary.  Although the
    defaults are likely sufficient, it is suggested that the following
    settings be reviewed:

    DATABASE - ensure name is satisfactory - default is "AppVReporting".

 2. Review the Permissions.sql file and provide all the necessary account information
    for setting up read and write access on the database. Note: Default settings
    in the file will not work.

 3. Review the ScheduleReportingJob.sql file and make sure that the stored proc schedule
    time is acceptable. The default stored proc schedule time is at 12.01 AM (line 84). 
    If this time is not suitable, you can change this to a more suitable time. The time is
##     in the format HHMMSS.



## INSTALLATION:

 1. Run the database.sql against the "master" database.  Your user
    credential must have the ability to create databases.
    This script will create the database.

 2. If upgrading the database, run UpgradeDatabase.sql This will upgrade database schema.

 2. Run the following scripts against the "AppVReporting" database using the
    same account as above in order.

    CreateTables.sql
    CreateReportingStoredProcs.sql
    CreateStoredProcs.sql
    CreateViews.sql
    InsertVersionInfo.sql
    Permissions.sql
##     ScheduleReportingJob.sql

```

**<span data-ttu-id="47281-129">Vous avez un problème lié à l’application-V?</span><span class="sxs-lookup"><span data-stu-id="47281-129">Got an App-V issue?</span></span>** <span data-ttu-id="47281-130">Utilisez le [Forum TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="47281-130">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="47281-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="47281-131">Related topics</span></span>

[<span data-ttu-id="47281-132">Déploiement d'App-V5.1 Server</span><span class="sxs-lookup"><span data-stu-id="47281-132">Deploying the App-V 5.1 Server</span></span>](deploying-the-app-v-51-server.md)

[<span data-ttu-id="47281-133">Procédure de déploiement d'App-V5.1 Server</span><span class="sxs-lookup"><span data-stu-id="47281-133">How to Deploy the App-V 5.1 Server</span></span>](how-to-deploy-the-app-v-51-server.md)
