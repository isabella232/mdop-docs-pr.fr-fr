---
title: Déploiement du serveur App-V5.1 à l'aide d'un script
description: Déploiement du serveur App-V5.1 à l'aide d'un script
author: dansimp
ms.assetid: 15c33d7b-9b61-4dbc-8674-399bb33e5f7e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 03/20/2020
ms.openlocfilehash: 579ca685f677aaaa4f5ebb6ac8d2969fdcbe2cd2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805496"
---
# Déploiement du serveur App-V5.1 à l'aide d'un script

Pour pouvoir terminer la configuration du serveur **appv\_server\_setup.exe** à l’aide de la ligne de commande, vous devez spécifier et combiner plusieurs paramètres.

## Installer le serveur App-V 5,1 à l’aide d’un script

- Utilisez les informations suivantes sur l’installation du serveur App-V 5,1 à l’aide de la ligne de commande.

    > [!NOTE]
    > Vous pouvez également accéder aux informations des tables suivantes à l’aide de la ligne de commande en entrant la commande suivante: **appv\_server\_setup.exe/?**.

### Installer le serveur de gestion et la base de données de gestion sur un ordinateur local

Les paramètres suivants sont valides avec des instances par défaut et personnalisées de Microsoft SQL Server:

- /MANAGEMENT_SERVER
- /MANAGEMENT_ADMINACCOUNT
- /MANAGEMENT_WEBSITE_NAME
- /MANAGEMENT_WEBSITE_PORT
- /DB_PREDEPLOY_MANAGEMENT
- /MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT
- /MANAGEMENT_DB_NAME

**Exemple: utilisation d’une instance personnalisée de Microsoft SQL Server**

```dos
appv_server_setup.exe /QUIET /MANAGEMENT_SERVER /MANAGEMENT_ADMINACCOUNT="Domain\AdminGroup" /MANAGEMENT_WEBSITE_NAME="Microsoft AppV Management Service" /MANAGEMENT_WEBSITE_PORT="8080" /DB_PREDEPLOY_MANAGEMENT /MANAGEMENT_DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /MANAGEMENT_DB_NAME="AppVManagement"
```

### Installer le serveur de gestion à l’aide d’une base de données de gestion existante sur un ordinateur local

Pour utiliser l’instance par défaut de Microsoft SQL Server, utilisez les paramètres suivants (différence par rapport à une instance personnalisée en *italique*):

- /MANAGEMENT_SERVER
- /MANAGEMENT_ADMINACCOUNT
- /MANAGEMENT_WEBSITE_NAME
- /MANAGEMENT_WEBSITE_PORT
- /EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL
- */EXISTING_MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT*
- /EXISTING_MANAGEMENT_DB_NAME

Pour utiliser une instance personnalisée de Microsoft SQL Server, utilisez les paramètres suivants (différence par rapport à l’instance par défaut en *italique*):

- /MANAGEMENT_SERVER
- /MANAGEMENT_ADMINACCOUNT
- /MANAGEMENT_WEBSITE_NAME
- /MANAGEMENT_WEBSITE_PORT
- /EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL
- */EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE*
- /EXISTING_MANAGEMENT_DB_NAME

**Exemple: utilisation d’une instance personnalisée de Microsoft SQL Server**

```dos
appv_server_setup.exe /QUIET /MANAGEMENT_SERVER /MANAGEMENT_ADMINACCOUNT="Domain\AdminGroup" /MANAGEMENT_WEBSITE_NAME="Microsoft AppV Management Service" /MANAGEMENT_WEBSITE_PORT="8080" /EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL /EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE ="SqlInstanceName" /EXISTING_MANAGEMENT_DB_NAME ="AppVManagement"
```

### Installer le serveur de gestion à l’aide d’une base de données de gestion existante sur un ordinateur distant

Pour utiliser l’instance par défaut de Microsoft SQL Server, utilisez les paramètres suivants (différence par rapport à une instance personnalisée en *italique*):

- /MANAGEMENT_SERVER
- /MANAGEMENT_ADMINACCOUNT
- /MANAGEMENT_WEBSITE_NAME
- /MANAGEMENT_WEBSITE_PORT
- /EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME
- */EXISTING_MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT*
- /EXISTING_MANAGEMENT_DB_NAME

Pour utiliser une instance personnalisée de Microsoft SQL Server, utilisez ces paramètres (différence par rapport à l’instance par défaut en *italique*):

- /MANAGEMENT_SERVER
- /MANAGEMENT_ADMINACCOUNT
- /MANAGEMENT_WEBSITE_NAME
- /MANAGEMENT_WEBSITE_PORT
- /EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME
- */EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE*
- /EXISTING_MANAGEMENT_DB_NAME

**Exemple: utilisation d’une instance personnalisée de Microsoft SQL Server:**

```dos
appv_server_setup.exe /QUIET /MANAGEMENT_SERVER /MANAGEMENT_ADMINACCOUNT="Domain\AdminGroup" /MANAGEMENT_WEBSITE_NAME="Microsoft AppV Management Service" /MANAGEMENT_WEBSITE_PORT="8080" /EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME="SqlServermachine.domainName" /EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE ="SqlInstanceName" /EXISTING_MANAGEMENT_DB_NAME ="AppVManagement"
```

### Installation de la base de données de gestion et du serveur de gestion sur le même ordinateur

Pour utiliser l’instance par défaut de Microsoft SQL Server, utilisez les paramètres suivants (différence par rapport à une instance personnalisée en *italique*):

- /DB_PREDEPLOY_MANAGEMENT
- */MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT*
- /MANAGEMENT_DB_NAME
- /MANAGEMENT_SERVER_MACHINE_USE_LOCAL
- /MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT

Pour utiliser une instance personnalisée de Microsoft SQL Server, utilisez ces paramètres (différence par rapport à l’instance par défaut en *italique*):

- /DB_PREDEPLOY_MANAGEMENT
- */MANAGEMENT_DB_CUSTOM_SQLINSTANCE*
- /MANAGEMENT_DB_NAME
- /MANAGEMENT_SERVER_MACHINE_USE_LOCAL
- /MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT

**Exemple: utilisation d’une instance personnalisée de Microsoft SQL Server**

```dos
appv_server_setup.exe /QUIET /DB_PREDEPLOY_MANAGEMENT /MANAGEMENT_DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /MANAGEMENT_DB_NAME="AppVManagement" /MANAGEMENT_SERVER_MACHINE_USE_LOCAL /MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT="Domain\InstallAdminAccount"
```

### Installation de la base de données de gestion sur un autre ordinateur que le serveur de gestion

Pour utiliser l’instance par défaut de Microsoft SQL Server, utilisez les paramètres suivants (différence par rapport à une instance personnalisée en *italique*):

- /DB_PREDEPLOY_MANAGEMENT
- */MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT*
- /MANAGEMENT_DB_NAME
- /MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT
- /MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT

Pour utiliser une instance personnalisée de Microsoft SQL Server, utilisez ces paramètres (différence par rapport à l’instance par défaut en *italique*):

- /DB_PREDEPLOY_MANAGEMENT
- */MANAGEMENT_DB_CUSTOM_SQLINSTANCE*
- /MANAGEMENT_DB_NAME
- /MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT
- /MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT

**Exemple: utilisation d’une instance personnalisée de Microsoft SQL Server**

```dos
appv_server_setup.exe /QUIET /DB_PREDEPLOY_MANAGEMENT /MANAGEMENT_DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /MANAGEMENT_DB_NAME="AppVManagement" /MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT="Domain\MachineAccount" /MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT="Domain\InstallAdminAccount"
```

### Installer le serveur de publication

Pour utiliser l’instance par défaut de Microsoft SQL Server, utilisez les paramètres suivants:

- /PUBLISHING_SERVER
- /PUBLISHING_MGT_SERVER
- /PUBLISHING_WEBSITE_NAME
- /PUBLISHING_WEBSITE_PORT

**Exemple: utilisation d’une instance personnalisée de Microsoft SQL Server:**

```dos
appv_server_setup.exe /QUIET /PUBLISHING_SERVER /PUBLISHING_MGT_SERVER="http://ManagementServerName:ManagementPort" /PUBLISHING_WEBSITE_NAME="Microsoft AppV Publishing Service" /PUBLISHING_WEBSITE_PORT="8081"
```

### Installer le serveur de création de rapports et la base de données de création de rapports sur un ordinateur local

Pour utiliser l’instance par défaut de Microsoft SQL Server, utilisez les paramètres suivants (différence par rapport à une instance personnalisée en *italique*):

- /REPORTING _SERVER
- /REPORTING _WEBSITE_NAME
- /REPORTING _WEBSITE_PORT
- /DB_PREDEPLOY_REPORTING
- */REPORTING _DB_SQLINSTANCE_USE_DEFAULT*
- /REPORTING _DB_NAME

Pour utiliser une instance personnalisée de Microsoft SQL Server, utilisez ces paramètres (différence par rapport à l’instance par défaut en *italique*):

- /REPORTING _SERVER
- */REPORTING _ADMINACCOUNT*
- /REPORTING _WEBSITE_NAME
- /REPORTING _WEBSITE_PORT
- /DB_PREDEPLOY_REPORTING
- */REPORTING _DB_CUSTOM_SQLINSTANCE*
- /REPORTING _DB_NAME

**Exemple: utilisation d’une instance personnalisée de Microsoft SQL Server:**

```dos
appv_server_setup.exe /QUIET /REPORTING_SERVER /REPORTING_WEBSITE_NAME="Microsoft AppV Reporting Service" /REPORTING_WEBSITE_PORT="8082" /DB_PREDEPLOY_REPORTING /REPORTING_DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /REPORTING_DB_NAME="AppVReporting"
```

### Installer le serveur de création de rapports et en utilisant une base de données de création de rapports existante sur un ordinateur local

Pour utiliser l’instance par défaut de Microsoft SQL Server, utilisez les paramètres suivants (différence par rapport à une instance personnalisée en *italique*):

- /REPORTING _SERVER
- /REPORTING _WEBSITE_NAME
- /REPORTING _WEBSITE_PORT
- /EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL
- */EXISTING_REPORTING _DB_SQLINSTANCE_USE_DEFAULT*
- /EXISTING_REPORTING _DB_NAME

Pour utiliser une instance personnalisée de Microsoft SQL Server, utilisez ces paramètres (différence par rapport à l’instance par défaut en *italique*):

- /REPORTING _SERVER
- */REPORTING _ADMINACCOUNT*
- /REPORTING _WEBSITE_NAME
- /REPORTING _WEBSITE_PORT
- /EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL
- */EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE*
- /EXISTING_REPORTING _DB_NAME

**Exemple: utilisation d’une instance personnalisée de Microsoft SQL Server:**

```dos
appv_server_setup.exe /QUIET /REPORTING_SERVER /REPORTING_WEBSITE_NAME="Microsoft AppV Reporting Service" /REPORTING_WEBSITE_PORT="8082" /EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL /EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /EXITING_REPORTING_DB_NAME="AppVReporting"
```

### Installer le serveur de création de rapports à l’aide d’une base de données de création de rapports existante sur un ordinateur distant

Pour utiliser l’instance par défaut de Microsoft SQL Server, utilisez les paramètres suivants (différence par rapport à une instance personnalisée en *italique*):

- /REPORTING _SERVER
- /REPORTING _WEBSITE_NAME
- /REPORTING _WEBSITE_PORT
- /EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME
- */EXISTING_REPORTING _DB_SQLINSTANCE_USE_DEFAULT*
- /EXISTING_REPORTING _DB_NAME

Pour utiliser une instance personnalisée de Microsoft SQL Server, utilisez ces paramètres (différence par rapport à l’instance par défaut en *italique*):

- /REPORTING _SERVER
- */REPORTING _ADMINACCOUNT*
- /REPORTING _WEBSITE_NAME
- /REPORTING _WEBSITE_PORT
- /EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME
- */EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE*
- /EXISTING_REPORTING _DB_NAME

**Exemple: utilisation d’une instance personnalisée de Microsoft SQL Server:**

```dos
appv_server_setup.exe /QUIET /REPORTING_SERVER /REPORTING_WEBSITE_NAME="Microsoft AppV Reporting Service" /REPORTING_WEBSITE_PORT="8082" /EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME="SqlServerMachine.DomainName" /EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /EXITING_REPORTING_DB_NAME="AppVReporting"
```

### Installation de la base de données de création de rapports sur le même ordinateur que le serveur de création de rapports

Pour utiliser l’instance par défaut de Microsoft SQL Server, utilisez les paramètres suivants (différence par rapport à une instance personnalisée en *italique*):

- /DB_PREDEPLOY_REPORTING
- */REPORTING _DB_SQLINSTANCE_USE_DEFAULT*
- /REPORTING _DB_NAME
- /REPORTING_SERVER_MACHINE_USE_LOCAL
- /REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT

Pour utiliser une instance personnalisée de Microsoft SQL Server, utilisez ces paramètres (différence par rapport à l’instance par défaut en *italique*):

- /DB_PREDEPLOY_REPORTING
- */REPORTING _DB_CUSTOM_SQLINSTANCE*
- /REPORTING _DB_NAME
- /REPORTING_SERVER_MACHINE_USE_LOCAL
- /REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT

**Exemple: utilisation d’une instance personnalisée de Microsoft SQL Server:**

```dos
appv_server_setup.exe /QUIET /DB_PREDEPLOY_REPORTING /REPORTING_DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /REPORTING_DB_NAME="AppVReporting" /REPORTING_SERVER_MACHINE_USE_LOCAL /REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT="Domain\InstallAdminAccount"
```

### Installation de la base de données de création de rapports sur un autre ordinateur que le serveur de création de rapports

Pour utiliser l’instance par défaut de Microsoft SQL Server, utilisez les paramètres suivants (différence par rapport à une instance personnalisée en *italique*):

- /DB_PREDEPLOY_REPORTING
- /REPORTING _DB_SQLINSTANCE_USE_DEFAULT
- /REPORTING _DB_NAME
- /REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT
- /REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT

Pour utiliser une instance personnalisée de Microsoft SQL Server, utilisez ces paramètres (différence par rapport à l’instance par défaut en *italique*):

- /DB_PREDEPLOY_REPORTING
- /REPORTING _DB_CUSTOM_SQLINSTANCE
- /REPORTING _DB_NAME
- /REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT
- /REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT

**Exemple: utilisation d’une instance personnalisée de Microsoft SQL Server:**

```dos
 appv_server_setup.exe /QUIET /DB_PREDEPLOY_REPORTING /REPORTING_DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /REPORTING_DB_NAME="AppVReporting" /REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT="Domain\MachineAccount" /REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT="Domain\InstallAdminAccount"
```

### Définitions des paramètres

#### Paramètres généraux

| Paramètre | Informations |
|--|--|
| /QUIET | Spécifie une installation silencieuse. |
| /UNINSTALL | Spécifie une désinstallation. |
| /LAYOUT | Spécifie l’action de disposition. Le MSIs et les fichiers de script sont extraits dans un dossier sans réellement installer le produit. Aucune valeur n’est attendue. |
| /LAYOUTDIR | Spécifie le répertoire de disposition. Prend une chaîne. Exemple d’utilisation: **/LAYOUTDIR = «serveur de virtualisation C:\\Application»** |
| /INSTALLDIR | Spécifie le répertoire d’installation. Prend une chaîne. Exemple d’utilisation: **/INSTALLDIR = "C:\\Program Files\\Application Virtualization\\Server"** |
| /MUOPTIN | Active Microsoft Update. Aucune valeur n’est attendue. |
| /ACCEPTEULA | Accepter le contrat de licence. Ce type de fichier est requis pour une installation sans assistance. Exemple d’utilisation: **/AcceptEULA** ou **/ACCEPTEULA = 1** |

#### Paramètres d’installation du serveur de gestion

|Paramètre |Informations |
|--|--|
| /MANAGEMENT_SERVER | Spécifie que le serveur de gestion sera installé. Aucune valeur n’est attendue |
| /MANAGEMENT_ADMINACCOUNT | Spécifie le compte dont l’accès administrateur au serveur de gestion est autorisé. Il peut s’agir d’un compte d’utilisateur ou d’un groupe. Exemple d’utilisation: **/MANAGEMENT_ADMINACCOUNT = «mydomain\\admin»**. Si **/MANAGEMENT_SERVER** n’est pas spécifié, la valeur est ignorée. |
| /MANAGEMENT_WEBSITE_NAME | Spécifie le nom du site Web qui sera créé pour le service de gestion. Exemple d’utilisation: **/MANAGEMENT_WEBSITE_NAME = "Microsoft App-V Management Service"** |
| MANAGEMENT_WEBSITE_PORT | Spécifie le numéro de port utilisé par le service de gestion. Exemple d’utilisation: **/MANAGEMENT_WEBSITE_PORT = 82** |

#### Paramètres de la base de données du serveur de gestion

| Paramètre | Informations |
|--|--|
| /DB_PREDEPLOY_MANAGEMENT | Spécifie que la base de données de gestion sera installée. Vous devez disposer des autorisations de base de données suffisantes pour effectuer cette installation. Aucune valeur n’est attendue. |
| /MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT | Indique que l’instance SQL par défaut doit être utilisée. Aucune valeur n’est attendue. |
| /MANAGEMENT_DB_ CUSTOM_SQLINSTANCE | Spécifie le nom de l’instance SQL personnalisée à utiliser pour créer une nouvelle base de données. Exemple d’utilisation: **/MANAGEMENT_DB_ CUSTOM_SQLINSTANCE = "MYSQLSERVER"**. Si **/DB_PREDEPLOY_MANAGEMENT** n’est pas spécifié, la valeur est ignorée. |
| /MANAGEMENT_DB_NAME | Spécifie le nom de la nouvelle base de données de gestion à créer. Exemple d’utilisation: **/MANAGEMENT_DB_NAME = «AppVMgmtDB»**. Si **/DB_PREDEPLOY_MANAGEMENT** n’est pas spécifié, la valeur est ignorée. |
| /MANAGEMENT_SERVER_MACHINE_USE_LOCAL | Indique si le serveur de gestion qui accède à la base de données est installé sur le serveur local. Basculez le paramètre de sorte qu’aucune valeur ne soit attendue. |
| /MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT | Spécifie le compte d’ordinateur de l’ordinateur distant sur lequel le serveur de gestion sera installé. Exemple d’utilisation: **/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT = «domain\\computername»** |
| /MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT | Indique le compte d’administrateur qui sera utilisé pour installer le serveur de gestion. Exemple d’utilisation: **/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT = «domain\\alias»** |

#### Paramètres pour l’installation d’un serveur de publication

| Paramètre | Informations |
|--|--|
| /PUBLISHING_SERVER | Spécifie que le serveur de publication sera installé. Aucune valeur n’est attendue. |
| /PUBLISHING_MGT_SERVER | Spécifie l’URL du service de gestion auquel est connecté le serveur de publication. Exemple d’utilisation: **http:// &lt; Management Server name &gt; : numéro &lt; &gt; de port du serveur de gestion**. Si **/PUBLISHING_SERVER** n’est pas utilisé, ce paramètre est ignoré. |
| /PUBLISHING_WEBSITE_NAME | Spécifie le nom du site Web qui sera créé pour le service de publication. Exemple d’utilisation: **/PUBLISHING_WEBSITE_NAME = «service de publication Microsoft App-V»** |
| /PUBLISHING_WEBSITE_PORT | Spécifie le numéro de port utilisé par le service de publication. Exemple d’utilisation: **/PUBLISHING_WEBSITE_PORT = 83** |

#### Paramètres pour le serveur de création de rapports

| Paramètre | Informations |
|--|--|
| /REPORTING_SERVER | Spécifie que le serveur de rapports sera installé. Aucune valeur n’est attendue. |
| /REPORTING_WEBSITE_NAME | Spécifie le nom du site Web qui sera créé pour le service de création de rapports. Exemple d’utilisation: **/REPORTING_WEBSITE_NAME = "Microsoft App-V ReportingService"** |
| /REPORTING_WEBSITE_PORT | Spécifie le numéro de port que le service de création de rapports utilisera. Exemple d’utilisation: **/REPORTING_WEBSITE_PORT = 82** |

#### Paramètres d’utilisation d’une base de données serveur de création de rapports existante

| Paramètre | Informations |
|--|--|
| /EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL | Indique que Microsoft SQL Server est installé sur le serveur local. Basculez le paramètre de sorte qu’aucune valeur ne soit attendue. |
| /EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME | Spécifie le nom de l’ordinateur distant sur lequel SQL Server est installé. Prend une chaîne. Exemple d’utilisation: **/EXISTING_REPORTING_DB_ REMOTE_SQL_SERVER_NAME = "mycomputer1"** |
| _DB_SQLINSTANCE_USE_DEFAULT EXISTING_ DE CRÉATION DE RAPPORTS | Indique que l’instance SQL par défaut doit être utilisée. Basculez le paramètre de sorte qu’aucune valeur ne soit attendue. |
| /EXISTING_ REPORTING_DB_CUSTOM_SQLINSTANCE | Spécifie le nom de l’instance SQL personnalisée qui doit être utilisée. Prend une chaîne. Exemple d’utilisation: **/EXISTING_REPORTING_DB_ CUSTOM_SQLINSTANCE = "MYSQLSERVER"** |
| _DB_NAME EXISTING_ DE CRÉATION DE RAPPORTS | Spécifie le nom de la base de données de création de rapports existante à utiliser. Prend une chaîne. Exemple d’utilisation: **/EXISTING_REPORTING_DB_NAME = «AppVReporting»** |

#### Paramètres pour l’installation de la base de données serveur de création de rapports

| Paramètre | Informations |
|--|--|
| /DB_PREDEPLOY_REPORTING | Spécifie que la base de données de création de rapports sera installée. Des autorisations DBA sont nécessaires pour cette installation. Aucune valeur n’est attendue. |
| /REPORTING_DB_SQLINSTANCE_USE_DEFAULT | Spécifie le nom de l’instance SQL personnalisée qui doit être utilisée. Prend une chaîne. Exemple d’utilisation: **/REPORTING_DB_ CUSTOM_SQLINSTANCE = "MYSQLSERVER"** |
| /REPORTING_DB_NAME | Spécifie le nom de la nouvelle base de données de création de rapports à créer. Prend une chaîne. Exemple d’utilisation: **/REPORTING_DB_NAME = «AppVMgmtDB»** |
| /REPORTING_SERVER_MACHINE_USE_LOCAL | Indique que le serveur de création de rapports qui accède à la base de données est installé sur le serveur local. Basculez le paramètre de sorte qu’aucune valeur ne soit attendue. |
| /REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT | Spécifie le compte d’ordinateur de l’ordinateur distant sur lequel est installé le serveur de rapports. Prend une chaîne. Exemple d’utilisation: **/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT = «domain\computername»** |
| /REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT | Indique le compte d’administrateur qui sera utilisé pour installer le serveur de création de rapports App-V. Prend une chaîne. Exemple d’utilisation: **/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT = «domain\\alias»** |

#### Paramètres d’utilisation d’une base de données serveur de gestion existante

| Paramètre | Informations |
|--|--|
| /EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL | Indique que SQL Server est installé sur le serveur local. Basculez le paramètre de sorte qu’aucune valeur ne soit attendue. Si **/DB_PREDEPLOY_MANAGEMENT** est spécifiée, la valeur est ignorée. |
| /EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME | Spécifie le nom de l’ordinateur distant sur lequel SQL Server est installé. Prend une chaîne. Exemple d’utilisation: **/EXISTING_MANAGEMENT_DB_ REMOTE_SQL_SERVER_NAME = "mycomputer1"** |
| /EXISTING_ MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT | Indique que l’instance SQL par défaut doit être utilisée. Basculez le paramètre de sorte qu’aucune valeur ne soit attendue. Si **/DB_PREDEPLOY_MANAGEMENT** est spécifiée, la valeur est ignorée. |
| /EXISTING_MANAGEMENT_DB_ CUSTOM_SQLINSTANCE | Spécifie le nom de l’instance SQL personnalisée qui sera utilisée. Exemple d’utilisation **/EXISTING_MANAGEMENT_DB_ CUSTOM_SQLINSTANCE = "AppVManagement"**. Si **/DB_PREDEPLOY_MANAGEMENT** est spécifiée, la valeur est ignorée. |
| /EXISTING_MANAGEMENT_DB_NAME | Spécifie le nom de la base de données de gestion existante à utiliser. Exemple d’utilisation: **/EXISTING_MANAGEMENT_DB_NAME = «AppVMgmtDB»**. Si **/DB_PREDEPLOY_MANAGEMENT** est spécifiée, la valeur est ignorée. |

Vous avez un problème lié à l’application-V? Utilisez le [Forum TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Rubriques connexes

[Déploiement d'App-V5.1 Server](deploying-the-app-v-51-server.md)
