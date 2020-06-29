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
# Comment déployer les bases de données App-V à l'aide de scripts SQL

Pour utiliser les scripts SQL plutôt que le programme d’installation Windows, procédez comme suit:

- Installer les bases de données App-V 5,1
- Mettre à niveau les bases de données d’application-V vers une version ultérieure

> [!NOTE]
> Si vous avez déjà déployé la base de données App-V 5,0 SP3, les scripts SQL ne sont pas obligés de procéder à la mise à niveau vers App-V 5,1.

## Comment installer les bases de données App-V à l’aide de scripts SQL

1. Avant d’installer les scripts de base de données, passez en revue les termes du contrat de licence App-V et conservez-en une copie. En exécutant les scripts de base de données, vous acceptez les termes du contrat de licence. Si vous n’acceptez pas le logiciel, vous ne devez pas l’utiliser.
1. Copiez l' **appv\_server\_setup.exe** du média App-V Release vers un emplacement temporaire.
1. À partir d’une invite de commandes, exécutez **appv\_server\_setup.exe** et spécifiez un emplacement temporaire pour extraire les scripts de la base de données.

    Exemple: appv\_server\_setup.exe/layout c:\\ &lt; _chemin d’emplacement temporaire_&gt;

1. Naviguez jusqu’à l’emplacement temporaire que vous avez créé, ouvrez le dossier **DatabaseScripts** extrait et examinez le fichier Readme.txt approprié pour obtenir des instructions:

    | Base de données | Emplacement du fichier Readme.txt à utiliser |
    |--|--|
    | Base de données de gestion | Sous-dossier ManagementDatabase |
    | Base de données de création de rapports | Sous-dossier ReportingDatabase |

> [!CAUTION]
> Le fichier readme.txt dans le sous-dossier ManagementDatabase est obsolète. Les informations contenues dans les fichiers Lisez-moi mis à jour ci-dessous sont les plus récentes et doivent remplacer les informations Lisez-moi fournies dans les dossiers **DatabaseScripts** .

> [!IMPORTANT]
> Le script InsertVersionInfo. SQL n’est pas requis pour les versions de la base de données de gestion App-V ultérieure à l’application-V 5,0 SP3.

Le script Permissions. SQL doit être mis à jour en suivant l' **étape 2** de [l’article 3031340](https://support.microsoft.com/kb/3031340)de la base de connaissances. L' **étape 1** n’est pas requise pour les versions de App-v ultérieures à l’application-v 5,0 SP3.

## Contenu du fichier Lisezmoi de la base de données de gestion mis à jour

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

## Contenu du fichier Lisezmoi de la base de données de rapports mis à jour

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

**Vous avez un problème lié à l’application-V?** Utilisez le [Forum TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Rubriques connexes

[Déploiement d'App-V5.1 Server](deploying-the-app-v-51-server.md)

[Procédure de déploiement d'App-V5.1 Server](how-to-deploy-the-app-v-51-server.md)
