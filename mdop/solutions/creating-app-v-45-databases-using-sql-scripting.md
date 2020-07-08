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
# Création de bases de données App-V4.5 à l'aide de scripts SQL


**À qui cette solution est-elle conçue pour?** Professionnels de l’informatique qui gèrent les bases de données 4,5 de virtualisation des applications (App-V).

**Comment ce guide peut-il vous aider?** Cette solution explique et décrit la procédure d’installation du serveur Microsoft Application Virtualization lors de l’installation d’un administrateur ne disposant pas de privilèges sysadmin sur le serveur SQL Server.

## Vue d'ensemble


L’un des problèmes liés à l’installation de Microsoft Application Virtualization 4,5 (App-V) est que le programme d’installation suppose que l’utilisateur qui installe les fonctionnalités du serveur n’est pas seulement un administrateur d’ordinateur local, mais qu’il dispose également de privilèges d’administrateur SQL sur le serveur SQL Server qui héberge le magasin de données. Cette condition est basée sur le fait que la base de données, ainsi que les rôles et les autorisations appropriés, sont créés dans le cadre de l’installation. Toutefois, dans la plupart des entreprises, les serveurs SQL sont gérés indépendamment de l’équipe d’infrastructure qui va installer App-V. Ces exigences de sécurité compliquent la mise en route des administrateurs SQL pour permettre à l’administrateur d’infrastructure d’installer les droits appropriés App-V. de même, les administrateurs SQL ne disposent pas des privilèges requis pour installer le produit pour l’équipe d’infrastructure.

Pour l’instant, un administrateur qui tente d’installer App-V doit disposer de privilèges SQL «sysadmin». Dans les versions précédentes du produit, le programme d’installation permettait aux administrateurs SQL de créer un compte «sysadmin» temporaire ou d’être présent au cours de l’installation pour fournir des informations d’identification avec des privilèges «sysadmin». Dans cette version, les scripts sont fournis dans le produit publié pour que tous les administrateurs aient recours lors de l’implémentation de leur infrastructure.

Ce livre blanc traite du scénario dans lequel l’installation doit être divisée en deux tâches distinctes: création de la base de données SQL et installation des fonctionnalités du serveur App-V. Les administrateurs SQL seraient en mesure de passer en revue les scripts SQL et de modifier les conflits avec d’autres bases de données ou de prendre en charge l’intégration avec d’autres outils. Le résultat des scripts doit permettre aux administrateurs SQL de préparer la base de données de sorte que les administrateurs d’infrastructure n’aient pas besoin d’avoir accès à des droits avancés sur le serveur SQL Server. C’est important dans les environnements dans lesquels les politiques de sécurité n’interdisent pas.

### Processus de création d’une base de données SQL

Les scripts SQL permettent aux administrateurs SQL de créer la base de données requise et de configurer les privilèges d’administrateur d’application-V pour l’installation et la gestion de l’environnement. Les étapes permettant d’effectuer ces tâches sont indiquées plus loin dans ce document.

Ce processus sépare les actions de création et de configuration de la base de données de l’installation App-V réelle.

**Informations à fournir aux administrateurs SQL**

-   Nom du groupe d’annonces qui va être l’administrateur de l’application-V.

-   Nom du serveur sur lequel est installé le serveur de gestion de l’application-V

**Informations devant être renvoyées aux administrateurs d’infrastructure**

-   Nom du serveur de base de données ou de l’instance et du nom de la base de données App-V.

Lorsque la base de données est préparée, les administrateurs de l’application-V peuvent exécuter l’installation d’App-V sans privilèges d’administrateur SQL.

### Utiliser les scripts de configuration SQL

**Configuration requise**

Voici une liste des conditions requises pour utiliser les scripts situés dans le dossier support\\createdb à la racine de l’emplacement d’extraction sélectionné.

-   Les scripts doivent être copiés vers un emplacement accessible en écriture sur l’ordinateur sur lequel ils seront exécutés (veillez à supprimer l’attribut lecture seule de ces scripts une fois qu’ils ont été copiés) et les outils clients SQL doivent être chargés sur cet ordinateur (OSQL est requis uniquement pour exécuter les fichiers de commandes d’exemple sur l’ordinateur local).

-   SQL Server doit prendre en charge l’authentification Windows.

-   Assurez-vous que les services SQL Server instance et SQL Agent s’exécutent.

-   Connectez-vous à l’aide d’un compte de domaine qui est un administrateur SQL (sysadmin) sur l’ordinateur sur lequel effectuer les scripts.

Les scripts s’exécutent sous les informations d’identification de domaine de l’utilisateur connecté.

**Création de base de données à l’aide de scripts SQL**

**Tâches devant être effectuées par les administrateurs SQL:**

1.  Copiez les scripts contenus dans le dossier support\\createdb à partir de la racine de l’emplacement d’extraction sélectionné vers l’ordinateur sur lequel les scripts seront exécutés. Pour que les scripts s’exécutent correctement, les fichiers suivants doivent être appelés dans l’ordre présenté ci-dessous.

    -   Database. SQL

    -   rôles. SQL

    -   Tableau \ _CODES. SQL

    -   fonctions \ _before \ _tables. SQL

    -   tables. SQL

    -   fonctions. SQL

    -   vues. SQL

    -   procédures. SQL

    -   déclencheurs. SQL

    -   données \ _codes. SQL

    -   données \ _messages. SQL

    -   données \ _defaults. SQL

    -   alertes \ _jobs. SQL

    -   DBVERSION. SQL

2.  Examinez et modifiez, si nécessaire, le `database.sql` fichier. Les paramètres par défaut nommeront la base de données «APPVIRTDB».

    -   Le cas échéant, remplacez `APPVIRTDB` les instances de par le `database name` qui sera utilisé.

    -   Remplacez la `FILENAME` propriété du script par le chemin d’accès approprié pour le serveur SQL sur lequel la base de données sera créée.

3.  Examinez et modifiez, si nécessaire, la `database name [APPVIRTDB]` dans le `roles.sql` fichier qui a été utilisé dans le fichier Database. Sql.

****

### Exemple illustrant comment automatiser le processus à l’aide de fichiers de commandes

S’il est utilisé, les deux exemples de fichiers de commandes proposés exécutent les scripts SQL de la façon suivante:

1.  **Create\_schema.bat (1)**

    -   Database. SQL

    -   rôles. SQL

2.  **Create\_tables.bat (2)**

    -   Tableau \ _CODES. SQL

    -   fonctions \ _before \ _tables. SQL

    -   tables. SQL

    -   fonctions. SQL

    -   vues. SQL

    -   procédures. SQL

    -   déclencheurs. SQL

    -   données \ _codes. SQL

    -   données \ _messages. SQL

    -   données \ _defaults. SQL

    -   alertes \ _jobs. SQL

    -   DBVERSION. SQL

**Remarque**  
La modification des scripts doit être soigneusement prise en considération et ne doit être effectuée qu’par une personne ayant les connaissances appropriées. Par ailleurs, les fichiers d’exemple présentés uniquement aux éléments suivants doivent être modifiés: **create\_schema.bat**, **create\_tables.bat**, **Database. SQL**et **rôles. SQL**. Aucun autre fichier ne doit être modifié de quelque manière que ce qui pourrait entraîner la création incorrecte de la base de données, ce qui entraînera l’échec de l’installation des services App-V.



Les deux exemples de fichiers de commandes doivent être placés dans le même répertoire que le reste des scripts SQL sur votre ordinateur.

1.  Exécutez l’exemple de fichier **create\_schema.bat** pour créer la base de données. L’exécution de ce script peut prendre quelques secondes et ne peut pas être interrompu.

    -   Exécuter le fichier de création de schema.bat à partir du répertoire dans lequel il a été copié. La syntaxe est la suivante: "Create\_schema.bat `SQLSERVERNAME` "

        ![AppV46SQLcreatebat](images/appv46sqlcreatebat.bmp)

    -   Si ce script échoue lors de la création de la nouvelle base de données «APPVIRTDB», vérifiez le journal comme indiqué pour corriger le problème. Il est nécessaire de supprimer la base de données créée à l’aide d’une exécution partielle des scripts afin de vous assurer que les tentatives suivantes fonctionneront correctement.

2.  Exécutez le `create_tables.bat` fichier pour créer les tables dans la base de données. L’exécution de ce script peut prendre quelques secondes et ne peut pas être interrompu.

    -   Exécutez le fichier create\_tables.bat à partir du répertoire dans lequel il a été copié. La syntaxe est la suivante: "create\_tables.bat `SQLSERVERNAME DBNAME` "

        ![create\-table.bat SQL App-v 4,6](images/appv46sqlcreate-tablebat.gif)

        Si le script échoue lors de la création des tables, recherchez le journal comme indiqué pour corriger le problème. Il est nécessaire de supprimer la base de données et de lancer create\_schema.bat avant d’essayer d’exécuter le fichier create\_tables.bat lors de toutes les tentatives ultérieures.

### Définir des autorisations sur la base de données App-V

Les comptes suivants doivent être créés sur le serveur SQL Server avec des autorisations et des rôles spécifiques à la nouvelle base de données pour l’installation, le déploiement et l’administration continue de l’environnement App-V.

-   Créez une connexion pour le groupe d’administrateurs d’application-V sur le serveur SQL Server et la base de données APPVIRTDB pour les utilisateurs «domain\\App-V admins» (où «Domain» et «App-V admins» seront modifiés pour refléter votre propre environnement) et ajoutez-les au rôle de base de données SFTAdmin et SFTEveryone.

    ![autorisations et rôles du jeu de scripts SQL App-v 4,6](images/appv46sqlscriptsetpermsroles.gif)

-   Octroyez à ce groupe l’autorisation «afficher toute définition» au niveau global (cela permet au service de configuration du serveur de gestion des applications Microsoft d’applications de vérifier que la connexion au serveur de gestion existe déjà). Sous MS-SQL 2005 et les restrictions d’accès au-dessus des métadonnées contenues dans Master. db ont été ajoutées. Par défaut, l’utilisateur créé lors de l’étape précédente ne dispose pas des droits nécessaires à l’installation du serveur. Ouvrez les propriétés de la connexion précédemment créée, propriétés de connexion- &gt; consécurisées. Ajoutez l’instance de base de données et activez «accorder» pour «afficher une définition», comme illustré dans la capture d’écran ci-dessous.

    ![script SQL App-v 4,6 Grant Perm pour afficher tout déf](images/appv46sqlscriptviewanydef.gif)

-   Ajoutez un rôle au rôle \ _ASSIGNMENTS table pour la connexion créée lors de l’étape précédente, afin de permettre aux administrateurs d’applications d’accéder à la console de gestion des applications d’application, à l’aide des rôles = «ADMIN» et du groupe \ _ref = «administrateurs domain\\App-V» (où «Domain» et «App-V admins» seront modifiés pour refléter votre environnement.

    ![attribution de rôle de script App-v 4,6 SQL](images/appv46sqlscriptroleassign.gif)

-   Créer une connexion pour SQL Server et base de données App-V pour le serveur de gestion. Ce compte est utilisé par le serveur de gestion des applications virtuelles Microsoft pour se connecter au magasin de données, et il est tenu de traiter les demandes des clients pour les applications diffusées. Vous avez le choix entre deux options, selon l’emplacement de l’installation de SQL Server et de Management Server:

    1.  Si le serveur de gestion et SQL Server vont être installés sur le même ordinateur, ajoutez une connexion pour le SERVICE AUTHORITY\\NETWORK NT et ajoutez-le aux rôles de base de données SFTUser et SFTEveryone.

    2.  Si le serveur de gestion et SQL Server doivent être installés sur plusieurs ordinateurs, ajoutez un nom de connexion pour «domain\\App-V Server Name $» (où «App-V Server Name» est le nom du serveur sur lequel est installé le serveur d’administration d’applications-V, puis ajoutez-le aux rôles de base de données SFTUser et SFTEveryone.

-   Ouvrez la fenêtre de requête dans la fenêtre SQL et exécutez le code SQL suivant:

    ``` syntax
    USE APPVIRTDB
    GRANT ALTER ON ROLE::SFTuser TO “domain\App-V Admins”
    ```

    Où APPVIRTDB est le nom de la base de données App-V créée sur le serveur SQL lors de l’étape précédente, et l’utilisateur qui va procéder à l’installation de l’application-v Server doit être membre de «domain\\App-V admins» (où «Domain» et «App-V admins» seront modifiés pour refléter votre environnement.

### Tâches devant être effectuées par les administrateurs d’infrastructure

1.  L’administrateur du groupe «administrateurs App-V» doit installer App-V.

    Utilisez les informations fournies par les administrateurs SQL pour sélectionner le serveur SQL et la base de données créés aux étapes précédentes.

2.  L’administrateur du groupe «administrateurs d’application-V» se connecte à la console de gestion de l’application virtualisation et supprime les objets suivants de la console de gestion.

    **Warning**  
    Ce paramètre est requis lorsque la configuration classique remplit certains enregistrements de la base de données qui ne sont pas remplis si vous exécutez l’installation sur une base de données existante. Supprimez les objets suivants:

    -   Sous «groupes de serveurs», «groupe de serveurs par défaut», «supprimer» serveur de gestion des applications virtuelles»

    -   Sous groupes de serveurs, "supprimer" groupe de serveurs par défaut "

    -   Sous stratégies du fournisseur, "supprimer" le fournisseur par défaut "



3.  L’administrateur dans le groupe d’administrateurs App-V doit alors créer les éléments suivants:

    -   Sous stratégies du fournisseur, créez une nouvelle stratégie de fournisseur.

    -   Créer un groupe de serveurs par défaut

        **Remarque**  
        Vous devez créer un groupe «serveur par défaut» même si vous ne l’utilisez pas. Le programme d’installation de serveur recherche uniquement le «groupe de serveurs par défaut» lorsque vous tentez d’ajouter le serveur.  S’il n’y a pas de «groupe de serveurs par défaut», l’installation échoue. Si vous envisagez d’utiliser des groupes de serveurs autres que ceux par défaut qui conviennent, il est nécessaire de conserver le «groupe de serveurs par défaut» si vous envisagez d’ajouter d’autres serveurs d’administration d’applications à votre infrastructure.



~~~
-   Assign the App-V Users Group to the New Provider Policy created above

-   Under “Server Groups,” create a New Server Group, specifying the New Provider Policy

-   Under the New Server group, create a New Application Virtualization Management Server

    **Important**  
    Do not restart the service before completing all of the above steps!



-   Administrator restarts the Application Virtualization Management Server service.
~~~

## Conclusion


En conclusion, les informations contenues dans ce document permettent à un administrateur de travailler avec les administrateurs SQL pour développer un chemin de déploiement adapté aux divisions de sécurité et d’administration au sein d’une organisation. Après avoir lu ce document et testé les tâches détaillées, un administrateur doit être prêt à implémenter son infrastructure App-V dans ce type d’environnement.









