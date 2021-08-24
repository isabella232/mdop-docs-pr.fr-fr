---
title: Création de bases de données App-V 4.5 à l'aide de scripts SQL
description: Création de bases de données App-V 4.5 à l'aide de scripts SQL
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
ms.openlocfilehash: c119f1d43a70cce04dd6151697318f7cf6a8d1f2
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910589"
---
# <a name="creating-app-v-45-databases-using-sql-scripting"></a>Création de bases de données App-V 4.5 à l'aide de scripts SQL


**Qui cette solution est-elle destinée ?** Professionnels de l’informatique qui gèrent les bases de données Application Virtualization (App-V) 4.5.

**Comment ce guide peut-il vous aider ?** Cette solution explique et documente la procédure d’installation de Microsoft Application Virtualization Server lorsque l’installation de l’administrateur n’a pas de privilèges « sysadmin » sur le serveur SQL Server.

## <a name="overview"></a>Présentation


L’un des défis de l’installation de Microsoft Application Virtualization 4.5 (App-V) est que le programme d’installation suppose que l’utilisateur qui installe les fonctionnalités du serveur sera non seulement un administrateur d’ordinateur local, mais dispose également de privilèges d’administrateur SQL sur le serveur SQL qui hébergera le magasin de données. Cette exigence est basée sur le fait que la base de données, ainsi que les rôles et autorisations appropriés, sont créés dans le cadre de l’installation. Toutefois, dans la plupart des SQL, les serveurs sont gérés séparément de l’équipe d’infrastructure qui installera App-V. Ces exigences de sécurité rendent difficile l’accès SQL administrateurs de l’infrastructure pour accorder à l’administrateur d’infrastructure des droits appropriés pour l’installation d’App-V . De même, les administrateurs SQL n’auront pas les privilèges requis pour installer le produit pour l’équipe d’infrastructure.

Actuellement, un administrateur qui tente d’installer App-V doit SQL les privilèges « sysadmin ». Dans les versions précédentes du produit, le programme d’installation permettait aux administrateurs SQL de créer un compte « sysadmin » temporaire ou d’être présents pendant l’installation pour fournir des informations d’identification avec des privilèges « sysadmin ». Dans cette version, les scripts sont fournis dans le produit publié pour que tous les administrateurs les utilisent lors de l’implémentation de leur infrastructure.

Ce livre blanc décrit le scénario dans lequel l’installation doit être divisée en deux tâches distinctes : la création de la base de données SQL et l’installation des fonctionnalités du serveur App-V. Les administrateurs SQL peuvent examiner les scripts SQL et apporter des modifications pour résoudre les conflits avec d’autres bases de données ou pour prendre en charge l’intégration avec d’autres outils. Le résultat des scripts est de permettre aux administrateurs SQL de préparer la base de données afin que les administrateurs d’infrastructure n’ont pas à se voir accorder de droits avancés sur le serveur SQL. Ceci est important dans les environnements où les stratégies de sécurité l’interdisent.

### <a name="sql-database-creation-process"></a>SQL Database Processus de création

Les scripts SQL permettent aux administrateurs SQL de créer la base de données requise et de configurer les privilèges pour que les administrateurs App-V installent et gèrent correctement l’environnement. Les étapes d’exécution de ces tâches sont répertoriées plus loin dans ce document.

Ce processus sépare les actions de création et de configuration de base de données de l’installation App-V réelle.

**Informations à fournir aux administrateurs SQL administrateurs**

-   Nom du groupe AD qui va être l’administrateur d’App-V

-   Nom du serveur sur lequel App-V Management Server sera installé

**Informations à retourner aux administrateurs d’infrastructure**

-   Nom du serveur ou de l’instance de base de données et nom de la base de données App-V

Une fois la base de données préparée, les administrateurs App-V peuvent exécuter l’installation d’App-V sans SQL’administrateur.

### <a name="using-the-sql-setup-scripts"></a>Utilisation des scripts SQL d’installation

**Conditions préalables**

Voici une liste des conditions requises pour l’utilisation des scripts qui se trouvent dans le dossier support\\createdb à la racine de l’emplacement d’extraction sélectionné.

-   Les scripts doivent être copiés à un emplacement accessible en écriture sur l’ordinateur sur lequel ils seront exécutés (assurez-vous de supprimer l’attribut en lecture seule de ces scripts après leur copie) et les outils clients SQL doivent être chargés sur cet ordinateur (osql est uniquement requis pour exécuter les exemples de fichiers de commandes sur l’ordinateur local).

-   Le SQL Server doit prendre en charge l Windows authentification par utilisateur.

-   Assurez-vous que les SQL Server instance et SQL service d’agent sont en cours d’exécution.

-   Connectez-vous avec un compte de domaine SQL administrateur (sysadmin) sur l’ordinateur sur lequel les scripts seront effectués.

Les scripts s’exécutent sous les informations d’identification de domaine de l’utilisateur connecté.

**Création de bases de données à l’aide SQL scripts**

**Tâches à effectuer par les administrateurs SQL:**

1.  Copiez les scripts contenus dans le dossier support\\createdb à partir de la racine de l’emplacement d’extraction sélectionné sur l’ordinateur sur lequel les scripts seront exécutés. Les fichiers suivants sont requis pour que les scripts s’exécutent correctement et doivent être appelés dans l’ordre présenté ci-dessous.

    -   database.sql

    -   roles.sql

    -   table\_CODES.sql

    -   functions\_before\_tables.sql

    -   tables.sql

    -   functions.sql

    -   views.sql

    -   procedures.sql

    -   triggers.sql

    -   data\_codes.sql

    -   data\_messages.sql

    -   data\_defaults.sql

    -   alerts\_jobs.sql

    -   dbversion.sql

2.  Examinez et modifiez, si nécessaire, le `database.sql` fichier. Les paramètres par défaut nommeront la base de données « APPVIRTDB ».

    -   Si nécessaire, remplacez les instances `APPVIRTDB` par celle qui sera `database name` utilisée.

    -   Modifiez la propriété dans le script avec le chemin d’accès approprié SQL Server où la base de données `FILENAME` sera créée.

3.  Examinez et modifiez, si nécessaire, le fichier utilisé dans le `database name [APPVIRTDB]` `roles.sql` fichier database.sql.

****

### <a name="example-of-how-to-automate-the-process-using-batch-files"></a>Exemple d’automatisation du processus à l’aide de fichiers de lots

S’ils sont utilisés, les deux exemples de fichiers de lots fournis exécutent SQL scripts de la manière suivante :

1.  **Create\_schema.bat (1)**

    -   database.sql

    -   roles.sql

2.  **Create\_tables.bat (2)**

    -   table\_CODES.sql

    -   functions\_before\_tables.sql

    -   tables.sql

    -   functions.sql

    -   views.sql

    -   procedures.sql

    -   triggers.sql

    -   data\_codes.sql

    -   data\_messages.sql

    -   data\_defaults.sql

    -   alerts\_jobs.sql

    -   dbversion.sql

**Remarque**  
Lorsque vous modifiez les scripts, vous devez prendre en considération attentivement cette modification et cette modification ne doit être effectuée que par une personne ayant les connaissances appropriées. En outre, des exemples de fichiers présentés, seuls les fichiers suivants doivent être modifiés : **create\_schema.bat**, **create\_tables.bat**, **database.sql**et **roles.sql**. Tous les autres fichiers ne doivent pas être modifiés, car cela peut entraîner une création incorrecte de la base de données, ce qui entraîne l’échec de l’installation des services App-V.



Les deux exemples de fichiers de commandes doivent être placés dans le même répertoire que les autres scripts SQL été copiés sur l’ordinateur.

1.  Exécutez ** l’exemplecreate\_schema.bat** fichier pour créer la base de données. Ce script prend plusieurs secondes et ne doit pas être interrompu.

    -   Exécutez le fichier schema.bat créer à partir du répertoire dans lequel il a été copié. La syntaxe est la suivante : « Create\_schema.bat `SQLSERVERNAME` »

        ![AppV46SQLcreatebat.](images/appv46sqlcreatebat.bmp)

    -   Si ce script échoue lors de la création de la nouvelle base de données « APPVIRTDB », vérifiez le journal comme indiqué pour corriger le problème. Il sera nécessaire de supprimer la base de données qui a été créée avec une exécution partielle des scripts afin de garantir que les tentatives suivantes fonctionneront correctement.

2.  Exécutez le `create_tables.bat` fichier pour créer les tables dans la base de données. Ce script prend plusieurs secondes et ne doit pas être interrompu.

    -   Exécutez le create\_tables.bat à partir du répertoire où il a été copié. La syntaxe est la suivante : « create\_tables.bat `SQLSERVERNAME DBNAME` »

        ![app-v 4.6 sql create\-table.bat.](images/appv46sqlcreate-tablebat.gif)

        Si le script échoue lors de la création des tables, vérifiez le journal comme indiqué pour corriger le problème. Il est nécessaire de supprimer la base de données et d’exécuter create\_schema.bat avant de tenter d’exécuter le fichier create\_tables.bat toutes les tentatives suivantes.

### <a name="setting-permissions-on-the-app-v-database"></a>Définition d’autorisations sur la base de données App-V

Les comptes suivants doivent être créés sur le serveur SQL avec des autorisations et des rôles spécifiques sur la nouvelle base de données pour l’installation, le déploiement et l’administration continue de l’environnement App-V.

-   Créez une connexion pour le groupe Administrateurs App-V sur le SQL Server et la base de données APPVIRTDB pour les « administrateurs domaine\\App-V » (où « domaine » et « Administrateurs App-V » seront modifiés pour refléter votre propre environnement) et ajoutez-les au rôle de base de données SFTAdmin et SFTEveryone.

    ![app-v 4.6 sql script set permissions and roles.](images/appv46sqlscriptsetpermsroles.gif)

-   Accordez à ce groupe l’autorisation « AFFICHER TOUTE DÉFINITION » au niveau global (cela permet au processus d’installation de Microsoft Application Virtualization Management Server de vérifier que la connexion au serveur de gestion existe déjà). Sous MS-SQL 2005 et les restrictions d’accès supérieures aux métadonnées contenues dans master.db ont été ajoutées. Par défaut, l’utilisateur créé à l’étape précédente ne peut pas avoir les droits requis par l’installation du serveur. Ouvrez les propriétés de la connexion créée précédemment, Propriétés de connexion - &gt; Sécurisables. Ajoutez l’instance de base de données et activez « GRANT » pour « Afficher n’importe quelle définition », comme illustré dans la capture d’écran ci-dessous.

    ![app-v 4.6 sql script grant perm for view any def.](images/appv46sqlscriptviewanydef.gif)

-   Ajoutez un rôle à la table ROLE\_ASSIGNMENTS pour la connexion créée à l’étape précédente pour permettre aux administrateurs App-V d’accéder à la console de gestion Application Virtualization, avec le rôle = « ADMIN » et group\_ref = « domaine\\Administrateurs App-V » (où « domaine » et « Administrateurs App-V » seront modifiés pour refléter votre propre environnement).

    ![Attribution de rôle de script sql app-v 4.6.](images/appv46sqlscriptroleassign.gif)

-   Créez une connexion pour SQL Server et la base de données App-V pour le serveur de gestion. Ce compte est utilisé par microsoft Application Virtualization Management Server pour se connecter au magasin de données et est responsable de la maintenance des demandes des clients pour les applications diffusées en continu. Deux options s’offrent à vous, selon l’emplacement SQL Server et le serveur d’administration à installer :

    1.  Si Management Server et SQL Server doivent être installés sur le même ordinateur, ajoutez une connexion pour NT AUTHORITY\\NETWORK SERVICE et ajoutez-la aux rôles de base de données SFTUser et SFTEveryone.

    2.  Si le serveur d’administration et SQL Server doivent être installés sur différents ordinateurs, ajoutez une connexion pour « domain\\App-V Server Name$ » (où « App-V Server Name » est le nom du serveur sur lequel le serveur de gestion App-V sera installé) et ajoutez-la aux rôles de base de données SFTUser et SFTEveryone.

-   Ouvrez la fenêtre de requête sur la SQL et exécutez la SQL :

    ``` syntax
    USE APPVIRTDB
    GRANT ALTER ON ROLE::SFTuser TO “domain\App-V Admins”
    ```

    Où APPVIRTDB est le nom de la base de données App-V créée sur le SQL Server à l’étape précédente, et où l’utilisateur qui va installer le serveur App-v doit être membre de « domain\\App-V Admins » (où « domaine » et « Administrateurs App-V » seront modifiés pour refléter votre propre environnement).

### <a name="tasks-to-be-performed-by-the-infrastructure-administrators"></a>Tâches à effectuer par les administrateurs de l’infrastructure

1.  L’administrateur du groupe « Administrateurs App-V » doit installer App-V.

    Utilisez les informations des administrateurs SQL pour sélectionner l’SQL Server et la base de données créées au cours des étapes précédentes.

2.  L’administrateur du groupe « Administrateurs App-V » se connecte à la console de gestion Application Virtualization et supprime les objets suivants de la console de gestion.

    **Warning**  
    Cette configuration est requise car le programme d’installation traditionnel remplit certains enregistrements de la base de données qui ne sont pas remplis si vous exécutez l’installation sur une base de données déjà existante. Supprimez les objets suivants :

    -   Sous « Groupes de serveurs », « Groupe de serveurs par défaut », supprimez « Application Virtualization Management Server »

    -   Sous « Groupes de serveurs », supprimez « Groupe de serveurs par défaut »

    -   Sous « Stratégies de fournisseur », supprimez « Fournisseur par défaut »



3.  L’administrateur du groupe Administrateurs App-V doit ensuite créer :

    -   Sous « Stratégies de fournisseur », créez une stratégie de fournisseur

    -   Créer un « groupe de serveurs par défaut »

        **Remarque**  
        Vous devez créer un groupe « Serveur par défaut » même si vous n’êtes pas utilisé. Le programme d’installation de serveur recherche uniquement le « groupe de serveurs par défaut » lors de la tentative d’ajout du serveur.  S’il n’existe aucun « groupe de serveurs par défaut », l’installation échoue. Si vous envisagez d’utiliser des groupes de serveurs autres que la valeur par défaut, il est simplement nécessaire de conserver le « groupe de serveurs par défaut » si vous envisagez d’ajouter des serveurs de gestion App-V ultérieurs à votre infrastructure.



~~~
-   Assign the App-V Users Group to the New Provider Policy created above

-   Under “Server Groups,” create a New Server Group, specifying the New Provider Policy

-   Under the New Server group, create a New Application Virtualization Management Server

    **Important**  
    Do not restart the service before completing all of the above steps!



-   Administrator restarts the Application Virtualization Management Server service.
~~~

## <a name="conclusion"></a>Conclusion


En conclusion, les informations de ce document permettent à un administrateur de travailler avec les administrateurs SQL pour développer un chemin d’accès de déploiement qui fonctionne pour les services de sécurité et d’administration d’une organisation. Après avoir lu ce document et testé les tâches documentées, un administrateur doit être prêt à implémenter son infrastructure App-V dans ce type d’environnement.









