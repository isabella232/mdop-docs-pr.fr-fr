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
# <span data-ttu-id="f8b93-103">Déploiement du serveur App-V5.1 à l'aide d'un script</span><span class="sxs-lookup"><span data-stu-id="f8b93-103">How to Deploy the App-V 5.1 Server Using a Script</span></span>

<span data-ttu-id="f8b93-104">Pour pouvoir terminer la configuration du serveur **appv\_server\_setup.exe** à l’aide de la ligne de commande, vous devez spécifier et combiner plusieurs paramètres.</span><span class="sxs-lookup"><span data-stu-id="f8b93-104">In order to complete the **appv\_server\_setup.exe** Server setup successfully using the command line, you must specify and combine multiple parameters.</span></span>

## <span data-ttu-id="f8b93-105">Installer le serveur App-V 5,1 à l’aide d’un script</span><span class="sxs-lookup"><span data-stu-id="f8b93-105">Install the App-V 5.1 server using a script</span></span>

- <span data-ttu-id="f8b93-106">Utilisez les informations suivantes sur l’installation du serveur App-V 5,1 à l’aide de la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="f8b93-106">Use the following information about installing the App-V 5.1 server using the command line.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f8b93-107">Vous pouvez également accéder aux informations des tables suivantes à l’aide de la ligne de commande en entrant la commande suivante: **appv\_server\_setup.exe/?**.</span><span class="sxs-lookup"><span data-stu-id="f8b93-107">The information in the following tables can also be accessed using the command line by typing the following command: **appv\_server\_setup.exe /?**.</span></span>

### <span data-ttu-id="f8b93-108">Installer le serveur de gestion et la base de données de gestion sur un ordinateur local</span><span class="sxs-lookup"><span data-stu-id="f8b93-108">Install the Management server and Management database on a local machine</span></span>

<span data-ttu-id="f8b93-109">Les paramètres suivants sont valides avec des instances par défaut et personnalisées de Microsoft SQL Server:</span><span class="sxs-lookup"><span data-stu-id="f8b93-109">The following parameters are valid with both the default and custom instance of Microsoft SQL Server:</span></span>

- <span data-ttu-id="f8b93-110">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="f8b93-110">/MANAGEMENT_SERVER</span></span>
- <span data-ttu-id="f8b93-111">/MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="f8b93-111">/MANAGEMENT_ADMINACCOUNT</span></span>
- <span data-ttu-id="f8b93-112">/MANAGEMENT_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="f8b93-112">/MANAGEMENT_WEBSITE_NAME</span></span>
- <span data-ttu-id="f8b93-113">/MANAGEMENT_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="f8b93-113">/MANAGEMENT_WEBSITE_PORT</span></span>
- <span data-ttu-id="f8b93-114">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="f8b93-114">/DB_PREDEPLOY_MANAGEMENT</span></span>
- <span data-ttu-id="f8b93-115">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="f8b93-115">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span>
- <span data-ttu-id="f8b93-116">/MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="f8b93-116">/MANAGEMENT_DB_NAME</span></span>

**<span data-ttu-id="f8b93-117">Exemple: utilisation d’une instance personnalisée de Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="f8b93-117">Example: Using a custom instance of Microsoft SQL Server</span></span>**

```dos
appv_server_setup.exe /QUIET /MANAGEMENT_SERVER /MANAGEMENT_ADMINACCOUNT="Domain\AdminGroup" /MANAGEMENT_WEBSITE_NAME="Microsoft AppV Management Service" /MANAGEMENT_WEBSITE_PORT="8080" /DB_PREDEPLOY_MANAGEMENT /MANAGEMENT_DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /MANAGEMENT_DB_NAME="AppVManagement"
```

### <span data-ttu-id="f8b93-118">Installer le serveur de gestion à l’aide d’une base de données de gestion existante sur un ordinateur local</span><span class="sxs-lookup"><span data-stu-id="f8b93-118">Install the Management server using an existing Management database on a local machine</span></span>

<span data-ttu-id="f8b93-119">Pour utiliser l’instance par défaut de Microsoft SQL Server, utilisez les paramètres suivants (différence par rapport à une instance personnalisée en *italique*):</span><span class="sxs-lookup"><span data-stu-id="f8b93-119">To use the default instance of Microsoft SQL Server, use the following parameters (difference from custom instance in *italic*):</span></span>

- <span data-ttu-id="f8b93-120">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="f8b93-120">/MANAGEMENT_SERVER</span></span>
- <span data-ttu-id="f8b93-121">/MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="f8b93-121">/MANAGEMENT_ADMINACCOUNT</span></span>
- <span data-ttu-id="f8b93-122">/MANAGEMENT_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="f8b93-122">/MANAGEMENT_WEBSITE_NAME</span></span>
- <span data-ttu-id="f8b93-123">/MANAGEMENT_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="f8b93-123">/MANAGEMENT_WEBSITE_PORT</span></span>
- <span data-ttu-id="f8b93-124">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="f8b93-124">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span></span>
- *<span data-ttu-id="f8b93-125">/EXISTING_MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="f8b93-125">/EXISTING_MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span>*
- <span data-ttu-id="f8b93-126">/EXISTING_MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="f8b93-126">/EXISTING_MANAGEMENT_DB_NAME</span></span>

<span data-ttu-id="f8b93-127">Pour utiliser une instance personnalisée de Microsoft SQL Server, utilisez les paramètres suivants (différence par rapport à l’instance par défaut en *italique*):</span><span class="sxs-lookup"><span data-stu-id="f8b93-127">To use a custom instance of Microsoft SQL Server, use the following parameters (difference from default instance in *italic*):</span></span>

- <span data-ttu-id="f8b93-128">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="f8b93-128">/MANAGEMENT_SERVER</span></span>
- <span data-ttu-id="f8b93-129">/MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="f8b93-129">/MANAGEMENT_ADMINACCOUNT</span></span>
- <span data-ttu-id="f8b93-130">/MANAGEMENT_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="f8b93-130">/MANAGEMENT_WEBSITE_NAME</span></span>
- <span data-ttu-id="f8b93-131">/MANAGEMENT_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="f8b93-131">/MANAGEMENT_WEBSITE_PORT</span></span>
- <span data-ttu-id="f8b93-132">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="f8b93-132">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span></span>
- *<span data-ttu-id="f8b93-133">/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="f8b93-133">/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span></span>*
- <span data-ttu-id="f8b93-134">/EXISTING_MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="f8b93-134">/EXISTING_MANAGEMENT_DB_NAME</span></span>

**<span data-ttu-id="f8b93-135">Exemple: utilisation d’une instance personnalisée de Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="f8b93-135">Example: Using a custom instance of Microsoft SQL Server</span></span>**

```dos
appv_server_setup.exe /QUIET /MANAGEMENT_SERVER /MANAGEMENT_ADMINACCOUNT="Domain\AdminGroup" /MANAGEMENT_WEBSITE_NAME="Microsoft AppV Management Service" /MANAGEMENT_WEBSITE_PORT="8080" /EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL /EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE ="SqlInstanceName" /EXISTING_MANAGEMENT_DB_NAME ="AppVManagement"
```

### <span data-ttu-id="f8b93-136">Installer le serveur de gestion à l’aide d’une base de données de gestion existante sur un ordinateur distant</span><span class="sxs-lookup"><span data-stu-id="f8b93-136">Install the Management server using an existing Management database on a remote machine</span></span>

<span data-ttu-id="f8b93-137">Pour utiliser l’instance par défaut de Microsoft SQL Server, utilisez les paramètres suivants (différence par rapport à une instance personnalisée en *italique*):</span><span class="sxs-lookup"><span data-stu-id="f8b93-137">To use the default instance of Microsoft SQL Server, use the following parameters (difference from custom instance in *italic*):</span></span>

- <span data-ttu-id="f8b93-138">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="f8b93-138">/MANAGEMENT_SERVER</span></span>
- <span data-ttu-id="f8b93-139">/MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="f8b93-139">/MANAGEMENT_ADMINACCOUNT</span></span>
- <span data-ttu-id="f8b93-140">/MANAGEMENT_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="f8b93-140">/MANAGEMENT_WEBSITE_NAME</span></span>
- <span data-ttu-id="f8b93-141">/MANAGEMENT_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="f8b93-141">/MANAGEMENT_WEBSITE_PORT</span></span>
- <span data-ttu-id="f8b93-142">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="f8b93-142">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</span></span>
- *<span data-ttu-id="f8b93-143">/EXISTING_MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="f8b93-143">/EXISTING_MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span>*
- <span data-ttu-id="f8b93-144">/EXISTING_MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="f8b93-144">/EXISTING_MANAGEMENT_DB_NAME</span></span>

<span data-ttu-id="f8b93-145">Pour utiliser une instance personnalisée de Microsoft SQL Server, utilisez ces paramètres (différence par rapport à l’instance par défaut en *italique*):</span><span class="sxs-lookup"><span data-stu-id="f8b93-145">To use a custom instance of Microsoft SQL Server, use these parameters (difference from default instance in *italic*):</span></span>

- <span data-ttu-id="f8b93-146">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="f8b93-146">/MANAGEMENT_SERVER</span></span>
- <span data-ttu-id="f8b93-147">/MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="f8b93-147">/MANAGEMENT_ADMINACCOUNT</span></span>
- <span data-ttu-id="f8b93-148">/MANAGEMENT_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="f8b93-148">/MANAGEMENT_WEBSITE_NAME</span></span>
- <span data-ttu-id="f8b93-149">/MANAGEMENT_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="f8b93-149">/MANAGEMENT_WEBSITE_PORT</span></span>
- <span data-ttu-id="f8b93-150">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="f8b93-150">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</span></span>
- *<span data-ttu-id="f8b93-151">/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="f8b93-151">/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span></span>*
- <span data-ttu-id="f8b93-152">/EXISTING_MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="f8b93-152">/EXISTING_MANAGEMENT_DB_NAME</span></span>

**<span data-ttu-id="f8b93-153">Exemple: utilisation d’une instance personnalisée de Microsoft SQL Server:</span><span class="sxs-lookup"><span data-stu-id="f8b93-153">Example: Using a custom instance of Microsoft SQL Server:</span></span>**

```dos
appv_server_setup.exe /QUIET /MANAGEMENT_SERVER /MANAGEMENT_ADMINACCOUNT="Domain\AdminGroup" /MANAGEMENT_WEBSITE_NAME="Microsoft AppV Management Service" /MANAGEMENT_WEBSITE_PORT="8080" /EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME="SqlServermachine.domainName" /EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE ="SqlInstanceName" /EXISTING_MANAGEMENT_DB_NAME ="AppVManagement"
```

### <span data-ttu-id="f8b93-154">Installation de la base de données de gestion et du serveur de gestion sur le même ordinateur</span><span class="sxs-lookup"><span data-stu-id="f8b93-154">Install the Management database and the Management Server on the same computer</span></span>

<span data-ttu-id="f8b93-155">Pour utiliser l’instance par défaut de Microsoft SQL Server, utilisez les paramètres suivants (différence par rapport à une instance personnalisée en *italique*):</span><span class="sxs-lookup"><span data-stu-id="f8b93-155">To use the default instance of Microsoft SQL Server, use the following parameters (difference from custom instance in *italic*):</span></span>

- <span data-ttu-id="f8b93-156">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="f8b93-156">/DB_PREDEPLOY_MANAGEMENT</span></span>
- *<span data-ttu-id="f8b93-157">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="f8b93-157">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span>*
- <span data-ttu-id="f8b93-158">/MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="f8b93-158">/MANAGEMENT_DB_NAME</span></span>
- <span data-ttu-id="f8b93-159">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="f8b93-159">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span></span>
- <span data-ttu-id="f8b93-160">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="f8b93-160">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span></span>

<span data-ttu-id="f8b93-161">Pour utiliser une instance personnalisée de Microsoft SQL Server, utilisez ces paramètres (différence par rapport à l’instance par défaut en *italique*):</span><span class="sxs-lookup"><span data-stu-id="f8b93-161">To use a custom instance of Microsoft SQL Server, use these parameters (difference from default instance in *italic*):</span></span>

- <span data-ttu-id="f8b93-162">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="f8b93-162">/DB_PREDEPLOY_MANAGEMENT</span></span>
- *<span data-ttu-id="f8b93-163">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="f8b93-163">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span></span>*
- <span data-ttu-id="f8b93-164">/MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="f8b93-164">/MANAGEMENT_DB_NAME</span></span>
- <span data-ttu-id="f8b93-165">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="f8b93-165">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span></span>
- <span data-ttu-id="f8b93-166">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="f8b93-166">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span></span>

**<span data-ttu-id="f8b93-167">Exemple: utilisation d’une instance personnalisée de Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="f8b93-167">Example: Using a custom instance of Microsoft SQL Server</span></span>**

```dos
appv_server_setup.exe /QUIET /DB_PREDEPLOY_MANAGEMENT /MANAGEMENT_DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /MANAGEMENT_DB_NAME="AppVManagement" /MANAGEMENT_SERVER_MACHINE_USE_LOCAL /MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT="Domain\InstallAdminAccount"
```

### <span data-ttu-id="f8b93-168">Installation de la base de données de gestion sur un autre ordinateur que le serveur de gestion</span><span class="sxs-lookup"><span data-stu-id="f8b93-168">Install the Management database on a different computer than the Management server</span></span>

<span data-ttu-id="f8b93-169">Pour utiliser l’instance par défaut de Microsoft SQL Server, utilisez les paramètres suivants (différence par rapport à une instance personnalisée en *italique*):</span><span class="sxs-lookup"><span data-stu-id="f8b93-169">To use the default instance of Microsoft SQL Server, use the following parameters (difference from custom instance in *italic*):</span></span>

- <span data-ttu-id="f8b93-170">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="f8b93-170">/DB_PREDEPLOY_MANAGEMENT</span></span>
- *<span data-ttu-id="f8b93-171">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="f8b93-171">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span>*
- <span data-ttu-id="f8b93-172">/MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="f8b93-172">/MANAGEMENT_DB_NAME</span></span>
- <span data-ttu-id="f8b93-173">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="f8b93-173">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span></span>
- <span data-ttu-id="f8b93-174">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="f8b93-174">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span></span>

<span data-ttu-id="f8b93-175">Pour utiliser une instance personnalisée de Microsoft SQL Server, utilisez ces paramètres (différence par rapport à l’instance par défaut en *italique*):</span><span class="sxs-lookup"><span data-stu-id="f8b93-175">To use a custom instance of Microsoft SQL Server, use these parameters (difference from default instance in *italic*):</span></span>

- <span data-ttu-id="f8b93-176">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="f8b93-176">/DB_PREDEPLOY_MANAGEMENT</span></span>
- *<span data-ttu-id="f8b93-177">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="f8b93-177">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span></span>*
- <span data-ttu-id="f8b93-178">/MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="f8b93-178">/MANAGEMENT_DB_NAME</span></span>
- <span data-ttu-id="f8b93-179">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="f8b93-179">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span></span>
- <span data-ttu-id="f8b93-180">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="f8b93-180">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span></span>

**<span data-ttu-id="f8b93-181">Exemple: utilisation d’une instance personnalisée de Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="f8b93-181">Example: Using a custom instance of Microsoft SQL Server</span></span>**

```dos
appv_server_setup.exe /QUIET /DB_PREDEPLOY_MANAGEMENT /MANAGEMENT_DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /MANAGEMENT_DB_NAME="AppVManagement" /MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT="Domain\MachineAccount" /MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT="Domain\InstallAdminAccount"
```

### <span data-ttu-id="f8b93-182">Installer le serveur de publication</span><span class="sxs-lookup"><span data-stu-id="f8b93-182">Install the publishing server</span></span>

<span data-ttu-id="f8b93-183">Pour utiliser l’instance par défaut de Microsoft SQL Server, utilisez les paramètres suivants:</span><span class="sxs-lookup"><span data-stu-id="f8b93-183">To use the default instance of Microsoft SQL Server, use the following parameters:</span></span>

- <span data-ttu-id="f8b93-184">/PUBLISHING_SERVER</span><span class="sxs-lookup"><span data-stu-id="f8b93-184">/PUBLISHING_SERVER</span></span>
- <span data-ttu-id="f8b93-185">/PUBLISHING_MGT_SERVER</span><span class="sxs-lookup"><span data-stu-id="f8b93-185">/PUBLISHING_MGT_SERVER</span></span>
- <span data-ttu-id="f8b93-186">/PUBLISHING_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="f8b93-186">/PUBLISHING_WEBSITE_NAME</span></span>
- <span data-ttu-id="f8b93-187">/PUBLISHING_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="f8b93-187">/PUBLISHING_WEBSITE_PORT</span></span>

**<span data-ttu-id="f8b93-188">Exemple: utilisation d’une instance personnalisée de Microsoft SQL Server:</span><span class="sxs-lookup"><span data-stu-id="f8b93-188">Example: Using a custom instance of Microsoft SQL Server:</span></span>**

```dos
appv_server_setup.exe /QUIET /PUBLISHING_SERVER /PUBLISHING_MGT_SERVER="http://ManagementServerName:ManagementPort" /PUBLISHING_WEBSITE_NAME="Microsoft AppV Publishing Service" /PUBLISHING_WEBSITE_PORT="8081"
```

### <span data-ttu-id="f8b93-189">Installer le serveur de création de rapports et la base de données de création de rapports sur un ordinateur local</span><span class="sxs-lookup"><span data-stu-id="f8b93-189">Install the Reporting server and Reporting database on a local machine</span></span>

<span data-ttu-id="f8b93-190">Pour utiliser l’instance par défaut de Microsoft SQL Server, utilisez les paramètres suivants (différence par rapport à une instance personnalisée en *italique*):</span><span class="sxs-lookup"><span data-stu-id="f8b93-190">To use the default instance of Microsoft SQL Server, use the following parameters (difference from custom instance in *italic*):</span></span>

- <span data-ttu-id="f8b93-191">/REPORTING _SERVER</span><span class="sxs-lookup"><span data-stu-id="f8b93-191">/REPORTING _SERVER</span></span>
- <span data-ttu-id="f8b93-192">/REPORTING _WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="f8b93-192">/REPORTING _WEBSITE_NAME</span></span>
- <span data-ttu-id="f8b93-193">/REPORTING _WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="f8b93-193">/REPORTING _WEBSITE_PORT</span></span>
- <span data-ttu-id="f8b93-194">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="f8b93-194">/DB_PREDEPLOY_REPORTING</span></span>
- *<span data-ttu-id="f8b93-195">/REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="f8b93-195">/REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span></span>*
- <span data-ttu-id="f8b93-196">/REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="f8b93-196">/REPORTING _DB_NAME</span></span>

<span data-ttu-id="f8b93-197">Pour utiliser une instance personnalisée de Microsoft SQL Server, utilisez ces paramètres (différence par rapport à l’instance par défaut en *italique*):</span><span class="sxs-lookup"><span data-stu-id="f8b93-197">To use a custom instance of Microsoft SQL Server, use these parameters (difference from default instance in *italic*):</span></span>

- <span data-ttu-id="f8b93-198">/REPORTING _SERVER</span><span class="sxs-lookup"><span data-stu-id="f8b93-198">/REPORTING _SERVER</span></span>
- *<span data-ttu-id="f8b93-199">/REPORTING _ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="f8b93-199">/REPORTING _ADMINACCOUNT</span></span>*
- <span data-ttu-id="f8b93-200">/REPORTING _WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="f8b93-200">/REPORTING _WEBSITE_NAME</span></span>
- <span data-ttu-id="f8b93-201">/REPORTING _WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="f8b93-201">/REPORTING _WEBSITE_PORT</span></span>
- <span data-ttu-id="f8b93-202">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="f8b93-202">/DB_PREDEPLOY_REPORTING</span></span>
- *<span data-ttu-id="f8b93-203">/REPORTING _DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="f8b93-203">/REPORTING _DB_CUSTOM_SQLINSTANCE</span></span>*
- <span data-ttu-id="f8b93-204">/REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="f8b93-204">/REPORTING _DB_NAME</span></span>

**<span data-ttu-id="f8b93-205">Exemple: utilisation d’une instance personnalisée de Microsoft SQL Server:</span><span class="sxs-lookup"><span data-stu-id="f8b93-205">Example: Using a custom instance of Microsoft SQL Server:</span></span>**

```dos
appv_server_setup.exe /QUIET /REPORTING_SERVER /REPORTING_WEBSITE_NAME="Microsoft AppV Reporting Service" /REPORTING_WEBSITE_PORT="8082" /DB_PREDEPLOY_REPORTING /REPORTING_DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /REPORTING_DB_NAME="AppVReporting"
```

### <span data-ttu-id="f8b93-206">Installer le serveur de création de rapports et en utilisant une base de données de création de rapports existante sur un ordinateur local</span><span class="sxs-lookup"><span data-stu-id="f8b93-206">Install the Reporting server and using an existing Reporting database on a local machine</span></span>

<span data-ttu-id="f8b93-207">Pour utiliser l’instance par défaut de Microsoft SQL Server, utilisez les paramètres suivants (différence par rapport à une instance personnalisée en *italique*):</span><span class="sxs-lookup"><span data-stu-id="f8b93-207">To use the default instance of Microsoft SQL Server, use the following parameters (difference from custom instance in *italic*):</span></span>

- <span data-ttu-id="f8b93-208">/REPORTING _SERVER</span><span class="sxs-lookup"><span data-stu-id="f8b93-208">/REPORTING _SERVER</span></span>
- <span data-ttu-id="f8b93-209">/REPORTING _WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="f8b93-209">/REPORTING _WEBSITE_NAME</span></span>
- <span data-ttu-id="f8b93-210">/REPORTING _WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="f8b93-210">/REPORTING _WEBSITE_PORT</span></span>
- <span data-ttu-id="f8b93-211">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="f8b93-211">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span></span>
- *<span data-ttu-id="f8b93-212">/EXISTING_REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="f8b93-212">/EXISTING_REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span></span>*
- <span data-ttu-id="f8b93-213">/EXISTING_REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="f8b93-213">/EXISTING_REPORTING _DB_NAME</span></span>

<span data-ttu-id="f8b93-214">Pour utiliser une instance personnalisée de Microsoft SQL Server, utilisez ces paramètres (différence par rapport à l’instance par défaut en *italique*):</span><span class="sxs-lookup"><span data-stu-id="f8b93-214">To use a custom instance of Microsoft SQL Server, use these parameters (difference from default instance in *italic*):</span></span>

- <span data-ttu-id="f8b93-215">/REPORTING _SERVER</span><span class="sxs-lookup"><span data-stu-id="f8b93-215">/REPORTING _SERVER</span></span>
- *<span data-ttu-id="f8b93-216">/REPORTING _ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="f8b93-216">/REPORTING _ADMINACCOUNT</span></span>*
- <span data-ttu-id="f8b93-217">/REPORTING _WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="f8b93-217">/REPORTING _WEBSITE_NAME</span></span>
- <span data-ttu-id="f8b93-218">/REPORTING _WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="f8b93-218">/REPORTING _WEBSITE_PORT</span></span>
- <span data-ttu-id="f8b93-219">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="f8b93-219">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span></span>
- *<span data-ttu-id="f8b93-220">/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="f8b93-220">/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE</span></span>*
- <span data-ttu-id="f8b93-221">/EXISTING_REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="f8b93-221">/EXISTING_REPORTING _DB_NAME</span></span>

**<span data-ttu-id="f8b93-222">Exemple: utilisation d’une instance personnalisée de Microsoft SQL Server:</span><span class="sxs-lookup"><span data-stu-id="f8b93-222">Example: Using a custom instance of Microsoft SQL Server:</span></span>**

```dos
appv_server_setup.exe /QUIET /REPORTING_SERVER /REPORTING_WEBSITE_NAME="Microsoft AppV Reporting Service" /REPORTING_WEBSITE_PORT="8082" /EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL /EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /EXITING_REPORTING_DB_NAME="AppVReporting"
```

### <span data-ttu-id="f8b93-223">Installer le serveur de création de rapports à l’aide d’une base de données de création de rapports existante sur un ordinateur distant</span><span class="sxs-lookup"><span data-stu-id="f8b93-223">Install the Reporting server using an existing Reporting database on a remote machine</span></span>

<span data-ttu-id="f8b93-224">Pour utiliser l’instance par défaut de Microsoft SQL Server, utilisez les paramètres suivants (différence par rapport à une instance personnalisée en *italique*):</span><span class="sxs-lookup"><span data-stu-id="f8b93-224">To use the default instance of Microsoft SQL Server, use the following parameters (difference from custom instance in *italic*):</span></span>

- <span data-ttu-id="f8b93-225">/REPORTING _SERVER</span><span class="sxs-lookup"><span data-stu-id="f8b93-225">/REPORTING _SERVER</span></span>
- <span data-ttu-id="f8b93-226">/REPORTING _WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="f8b93-226">/REPORTING _WEBSITE_NAME</span></span>
- <span data-ttu-id="f8b93-227">/REPORTING _WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="f8b93-227">/REPORTING _WEBSITE_PORT</span></span>
- <span data-ttu-id="f8b93-228">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="f8b93-228">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</span></span>
- *<span data-ttu-id="f8b93-229">/EXISTING_REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="f8b93-229">/EXISTING_REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span></span>*
- <span data-ttu-id="f8b93-230">/EXISTING_REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="f8b93-230">/EXISTING_REPORTING _DB_NAME</span></span>

<span data-ttu-id="f8b93-231">Pour utiliser une instance personnalisée de Microsoft SQL Server, utilisez ces paramètres (différence par rapport à l’instance par défaut en *italique*):</span><span class="sxs-lookup"><span data-stu-id="f8b93-231">To use a custom instance of Microsoft SQL Server, use these parameters (difference from default instance in *italic*):</span></span>

- <span data-ttu-id="f8b93-232">/REPORTING _SERVER</span><span class="sxs-lookup"><span data-stu-id="f8b93-232">/REPORTING _SERVER</span></span>
- *<span data-ttu-id="f8b93-233">/REPORTING _ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="f8b93-233">/REPORTING _ADMINACCOUNT</span></span>*
- <span data-ttu-id="f8b93-234">/REPORTING _WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="f8b93-234">/REPORTING _WEBSITE_NAME</span></span>
- <span data-ttu-id="f8b93-235">/REPORTING _WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="f8b93-235">/REPORTING _WEBSITE_PORT</span></span>
- <span data-ttu-id="f8b93-236">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="f8b93-236">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</span></span>
- *<span data-ttu-id="f8b93-237">/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="f8b93-237">/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE</span></span>*
- <span data-ttu-id="f8b93-238">/EXISTING_REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="f8b93-238">/EXISTING_REPORTING _DB_NAME</span></span>

**<span data-ttu-id="f8b93-239">Exemple: utilisation d’une instance personnalisée de Microsoft SQL Server:</span><span class="sxs-lookup"><span data-stu-id="f8b93-239">Example: Using a custom instance of Microsoft SQL Server:</span></span>**

```dos
appv_server_setup.exe /QUIET /REPORTING_SERVER /REPORTING_WEBSITE_NAME="Microsoft AppV Reporting Service" /REPORTING_WEBSITE_PORT="8082" /EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME="SqlServerMachine.DomainName" /EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /EXITING_REPORTING_DB_NAME="AppVReporting"
```

### <span data-ttu-id="f8b93-240">Installation de la base de données de création de rapports sur le même ordinateur que le serveur de création de rapports</span><span class="sxs-lookup"><span data-stu-id="f8b93-240">Install the Reporting database on the same computer as the Reporting server</span></span>

<span data-ttu-id="f8b93-241">Pour utiliser l’instance par défaut de Microsoft SQL Server, utilisez les paramètres suivants (différence par rapport à une instance personnalisée en *italique*):</span><span class="sxs-lookup"><span data-stu-id="f8b93-241">To use the default instance of Microsoft SQL Server, use the following parameters (difference from custom instance in *italic*):</span></span>

- <span data-ttu-id="f8b93-242">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="f8b93-242">/DB_PREDEPLOY_REPORTING</span></span>
- *<span data-ttu-id="f8b93-243">/REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="f8b93-243">/REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span></span>*
- <span data-ttu-id="f8b93-244">/REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="f8b93-244">/REPORTING _DB_NAME</span></span>
- <span data-ttu-id="f8b93-245">/REPORTING_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="f8b93-245">/REPORTING_SERVER_MACHINE_USE_LOCAL</span></span>
- <span data-ttu-id="f8b93-246">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="f8b93-246">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span></span>

<span data-ttu-id="f8b93-247">Pour utiliser une instance personnalisée de Microsoft SQL Server, utilisez ces paramètres (différence par rapport à l’instance par défaut en *italique*):</span><span class="sxs-lookup"><span data-stu-id="f8b93-247">To use a custom instance of Microsoft SQL Server, use these parameters (difference from default instance in *italic*):</span></span>

- <span data-ttu-id="f8b93-248">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="f8b93-248">/DB_PREDEPLOY_REPORTING</span></span>
- *<span data-ttu-id="f8b93-249">/REPORTING _DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="f8b93-249">/REPORTING _DB_CUSTOM_SQLINSTANCE</span></span>*
- <span data-ttu-id="f8b93-250">/REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="f8b93-250">/REPORTING _DB_NAME</span></span>
- <span data-ttu-id="f8b93-251">/REPORTING_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="f8b93-251">/REPORTING_SERVER_MACHINE_USE_LOCAL</span></span>
- <span data-ttu-id="f8b93-252">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="f8b93-252">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span></span>

**<span data-ttu-id="f8b93-253">Exemple: utilisation d’une instance personnalisée de Microsoft SQL Server:</span><span class="sxs-lookup"><span data-stu-id="f8b93-253">Example: Using a custom instance of Microsoft SQL Server:</span></span>**

```dos
appv_server_setup.exe /QUIET /DB_PREDEPLOY_REPORTING /REPORTING_DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /REPORTING_DB_NAME="AppVReporting" /REPORTING_SERVER_MACHINE_USE_LOCAL /REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT="Domain\InstallAdminAccount"
```

### <span data-ttu-id="f8b93-254">Installation de la base de données de création de rapports sur un autre ordinateur que le serveur de création de rapports</span><span class="sxs-lookup"><span data-stu-id="f8b93-254">Install the Reporting database on a different computer than the Reporting server</span></span>

<span data-ttu-id="f8b93-255">Pour utiliser l’instance par défaut de Microsoft SQL Server, utilisez les paramètres suivants (différence par rapport à une instance personnalisée en *italique*):</span><span class="sxs-lookup"><span data-stu-id="f8b93-255">To use the default instance of Microsoft SQL Server, use the following parameters (difference from custom instance in *italic*):</span></span>

- <span data-ttu-id="f8b93-256">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="f8b93-256">/DB_PREDEPLOY_REPORTING</span></span>
- <span data-ttu-id="f8b93-257">/REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="f8b93-257">/REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span></span>
- <span data-ttu-id="f8b93-258">/REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="f8b93-258">/REPORTING _DB_NAME</span></span>
- <span data-ttu-id="f8b93-259">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="f8b93-259">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span></span>
- <span data-ttu-id="f8b93-260">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="f8b93-260">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span></span>

<span data-ttu-id="f8b93-261">Pour utiliser une instance personnalisée de Microsoft SQL Server, utilisez ces paramètres (différence par rapport à l’instance par défaut en *italique*):</span><span class="sxs-lookup"><span data-stu-id="f8b93-261">To use a custom instance of Microsoft SQL Server, use these parameters (difference from default instance in *italic*):</span></span>

- <span data-ttu-id="f8b93-262">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="f8b93-262">/DB_PREDEPLOY_REPORTING</span></span>
- <span data-ttu-id="f8b93-263">/REPORTING _DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="f8b93-263">/REPORTING _DB_CUSTOM_SQLINSTANCE</span></span>
- <span data-ttu-id="f8b93-264">/REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="f8b93-264">/REPORTING _DB_NAME</span></span>
- <span data-ttu-id="f8b93-265">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="f8b93-265">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span></span>
- <span data-ttu-id="f8b93-266">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="f8b93-266">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span></span>

**<span data-ttu-id="f8b93-267">Exemple: utilisation d’une instance personnalisée de Microsoft SQL Server:</span><span class="sxs-lookup"><span data-stu-id="f8b93-267">Example: Using a custom instance of Microsoft SQL Server:</span></span>**

```dos
 appv_server_setup.exe /QUIET /DB_PREDEPLOY_REPORTING /REPORTING_DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /REPORTING_DB_NAME="AppVReporting" /REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT="Domain\MachineAccount" /REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT="Domain\InstallAdminAccount"
```

### <span data-ttu-id="f8b93-268">Définitions des paramètres</span><span class="sxs-lookup"><span data-stu-id="f8b93-268">Parameter Definitions</span></span>

#### <span data-ttu-id="f8b93-269">Paramètres généraux</span><span class="sxs-lookup"><span data-stu-id="f8b93-269">General Parameters</span></span>

| <span data-ttu-id="f8b93-270">Paramètre</span><span class="sxs-lookup"><span data-stu-id="f8b93-270">Parameter</span></span> | <span data-ttu-id="f8b93-271">Informations</span><span class="sxs-lookup"><span data-stu-id="f8b93-271">Information</span></span> |
|--|--|
| <span data-ttu-id="f8b93-272">/QUIET</span><span class="sxs-lookup"><span data-stu-id="f8b93-272">/QUIET</span></span> | <span data-ttu-id="f8b93-273">Spécifie une installation silencieuse.</span><span class="sxs-lookup"><span data-stu-id="f8b93-273">Specifies silent install.</span></span> |
| <span data-ttu-id="f8b93-274">/UNINSTALL</span><span class="sxs-lookup"><span data-stu-id="f8b93-274">/UNINSTALL</span></span> | <span data-ttu-id="f8b93-275">Spécifie une désinstallation.</span><span class="sxs-lookup"><span data-stu-id="f8b93-275">Specifies an uninstall.</span></span> |
| <span data-ttu-id="f8b93-276">/LAYOUT</span><span class="sxs-lookup"><span data-stu-id="f8b93-276">/LAYOUT</span></span> | <span data-ttu-id="f8b93-277">Spécifie l’action de disposition.</span><span class="sxs-lookup"><span data-stu-id="f8b93-277">Specifies layout action.</span></span> <span data-ttu-id="f8b93-278">Le MSIs et les fichiers de script sont extraits dans un dossier sans réellement installer le produit.</span><span class="sxs-lookup"><span data-stu-id="f8b93-278">This extracts the MSIs and script files to a folder without actually installing the product.</span></span> <span data-ttu-id="f8b93-279">Aucune valeur n’est attendue.</span><span class="sxs-lookup"><span data-stu-id="f8b93-279">No value is expected.</span></span> |
| <span data-ttu-id="f8b93-280">/LAYOUTDIR</span><span class="sxs-lookup"><span data-stu-id="f8b93-280">/LAYOUTDIR</span></span> | <span data-ttu-id="f8b93-281">Spécifie le répertoire de disposition.</span><span class="sxs-lookup"><span data-stu-id="f8b93-281">Specifies the layout directory.</span></span> <span data-ttu-id="f8b93-282">Prend une chaîne.</span><span class="sxs-lookup"><span data-stu-id="f8b93-282">Takes a string.</span></span> <span data-ttu-id="f8b93-283">Exemple d’utilisation: **/LAYOUTDIR = «serveur de virtualisation C:\\Application»**</span><span class="sxs-lookup"><span data-stu-id="f8b93-283">Example usage: **/LAYOUTDIR="C:\\Application Virtualization Server"**</span></span> |
| <span data-ttu-id="f8b93-284">/INSTALLDIR</span><span class="sxs-lookup"><span data-stu-id="f8b93-284">/INSTALLDIR</span></span> | <span data-ttu-id="f8b93-285">Spécifie le répertoire d’installation.</span><span class="sxs-lookup"><span data-stu-id="f8b93-285">Specifies the installation directory.</span></span> <span data-ttu-id="f8b93-286">Prend une chaîne.</span><span class="sxs-lookup"><span data-stu-id="f8b93-286">Takes a string.</span></span> <span data-ttu-id="f8b93-287">Exemple d’utilisation: **/INSTALLDIR = "C:\\Program Files\\Application Virtualization\\Server"**</span><span class="sxs-lookup"><span data-stu-id="f8b93-287">Example usage: **/INSTALLDIR="C:\\Program Files\\Application Virtualization\\Server"**</span></span> |
| <span data-ttu-id="f8b93-288">/MUOPTIN</span><span class="sxs-lookup"><span data-stu-id="f8b93-288">/MUOPTIN</span></span> | <span data-ttu-id="f8b93-289">Active Microsoft Update.</span><span class="sxs-lookup"><span data-stu-id="f8b93-289">Enables Microsoft Update.</span></span> <span data-ttu-id="f8b93-290">Aucune valeur n’est attendue.</span><span class="sxs-lookup"><span data-stu-id="f8b93-290">No value is expected.</span></span> |
| <span data-ttu-id="f8b93-291">/ACCEPTEULA</span><span class="sxs-lookup"><span data-stu-id="f8b93-291">/ACCEPTEULA</span></span> | <span data-ttu-id="f8b93-292">Accepter le contrat de licence.</span><span class="sxs-lookup"><span data-stu-id="f8b93-292">Accepts the license agreement.</span></span> <span data-ttu-id="f8b93-293">Ce type de fichier est requis pour une installation sans assistance.</span><span class="sxs-lookup"><span data-stu-id="f8b93-293">This is required for an unattended installation.</span></span> <span data-ttu-id="f8b93-294">Exemple d’utilisation: **/AcceptEULA** ou **/ACCEPTEULA = 1**</span><span class="sxs-lookup"><span data-stu-id="f8b93-294">Example usage: **/ACCEPTEULA** or **/ACCEPTEULA=1**</span></span> |

#### <span data-ttu-id="f8b93-295">Paramètres d’installation du serveur de gestion</span><span class="sxs-lookup"><span data-stu-id="f8b93-295">Management Server Installation Parameters</span></span>

|<span data-ttu-id="f8b93-296">Paramètre</span><span class="sxs-lookup"><span data-stu-id="f8b93-296">Parameter</span></span> |<span data-ttu-id="f8b93-297">Informations</span><span class="sxs-lookup"><span data-stu-id="f8b93-297">Information</span></span> |
|--|--|
| <span data-ttu-id="f8b93-298">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="f8b93-298">/MANAGEMENT_SERVER</span></span> | <span data-ttu-id="f8b93-299">Spécifie que le serveur de gestion sera installé.</span><span class="sxs-lookup"><span data-stu-id="f8b93-299">Specifies that the management server will be installed.</span></span> <span data-ttu-id="f8b93-300">Aucune valeur n’est attendue</span><span class="sxs-lookup"><span data-stu-id="f8b93-300">No value is expected</span></span> |
| <span data-ttu-id="f8b93-301">/MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="f8b93-301">/MANAGEMENT_ADMINACCOUNT</span></span> | <span data-ttu-id="f8b93-302">Spécifie le compte dont l’accès administrateur au serveur de gestion est autorisé.</span><span class="sxs-lookup"><span data-stu-id="f8b93-302">Specifies the account that will be allowed Administrator access to the management server.</span></span> <span data-ttu-id="f8b93-303">Il peut s’agir d’un compte d’utilisateur ou d’un groupe.</span><span class="sxs-lookup"><span data-stu-id="f8b93-303">This can be a user account or a group.</span></span> <span data-ttu-id="f8b93-304">Exemple d’utilisation: **/MANAGEMENT_ADMINACCOUNT = «mydomain\\admin»**.</span><span class="sxs-lookup"><span data-stu-id="f8b93-304">Example usage: **/MANAGEMENT_ADMINACCOUNT="mydomain\\admin"**.</span></span> <span data-ttu-id="f8b93-305">Si **/MANAGEMENT_SERVER** n’est pas spécifié, la valeur est ignorée.</span><span class="sxs-lookup"><span data-stu-id="f8b93-305">If **/MANAGEMENT_SERVER** is not specified, this will be ignored.</span></span> |
| <span data-ttu-id="f8b93-306">/MANAGEMENT_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="f8b93-306">/MANAGEMENT_WEBSITE_NAME</span></span> | <span data-ttu-id="f8b93-307">Spécifie le nom du site Web qui sera créé pour le service de gestion.</span><span class="sxs-lookup"><span data-stu-id="f8b93-307">Specifies name of the website that will be created for the management service.</span></span> <span data-ttu-id="f8b93-308">Exemple d’utilisation: **/MANAGEMENT_WEBSITE_NAME = "Microsoft App-V Management Service"**</span><span class="sxs-lookup"><span data-stu-id="f8b93-308">Example usage: **/MANAGEMENT_WEBSITE_NAME="Microsoft App-V Management Service"**</span></span> |
| <span data-ttu-id="f8b93-309">MANAGEMENT_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="f8b93-309">MANAGEMENT_WEBSITE_PORT</span></span> | <span data-ttu-id="f8b93-310">Spécifie le numéro de port utilisé par le service de gestion.</span><span class="sxs-lookup"><span data-stu-id="f8b93-310">Specifies the port number that will be used by the management service will use.</span></span> <span data-ttu-id="f8b93-311">Exemple d’utilisation: **/MANAGEMENT_WEBSITE_PORT = 82**</span><span class="sxs-lookup"><span data-stu-id="f8b93-311">Example usage: **/MANAGEMENT_WEBSITE_PORT=82**</span></span> |

#### <span data-ttu-id="f8b93-312">Paramètres de la base de données du serveur de gestion</span><span class="sxs-lookup"><span data-stu-id="f8b93-312">Parameters for the Management Server Database</span></span>

| <span data-ttu-id="f8b93-313">Paramètre</span><span class="sxs-lookup"><span data-stu-id="f8b93-313">Parameter</span></span> | <span data-ttu-id="f8b93-314">Informations</span><span class="sxs-lookup"><span data-stu-id="f8b93-314">Information</span></span> |
|--|--|
| <span data-ttu-id="f8b93-315">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="f8b93-315">/DB_PREDEPLOY_MANAGEMENT</span></span> | <span data-ttu-id="f8b93-316">Spécifie que la base de données de gestion sera installée.</span><span class="sxs-lookup"><span data-stu-id="f8b93-316">Specifies that the management database will be installed.</span></span> <span data-ttu-id="f8b93-317">Vous devez disposer des autorisations de base de données suffisantes pour effectuer cette installation.</span><span class="sxs-lookup"><span data-stu-id="f8b93-317">You must have sufficient database permissions to complete this installation.</span></span> <span data-ttu-id="f8b93-318">Aucune valeur n’est attendue.</span><span class="sxs-lookup"><span data-stu-id="f8b93-318">No value is expected.</span></span> |
| <span data-ttu-id="f8b93-319">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="f8b93-319">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span> | <span data-ttu-id="f8b93-320">Indique que l’instance SQL par défaut doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="f8b93-320">Indicates that the default SQL instance should be used.</span></span> <span data-ttu-id="f8b93-321">Aucune valeur n’est attendue.</span><span class="sxs-lookup"><span data-stu-id="f8b93-321">No value is expected.</span></span> |
| <span data-ttu-id="f8b93-322">/MANAGEMENT_DB_ CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="f8b93-322">/MANAGEMENT_DB_ CUSTOM_SQLINSTANCE</span></span> | <span data-ttu-id="f8b93-323">Spécifie le nom de l’instance SQL personnalisée à utiliser pour créer une nouvelle base de données.</span><span class="sxs-lookup"><span data-stu-id="f8b93-323">Specifies the name of the custom SQL instance that should be used to create a new database.</span></span> <span data-ttu-id="f8b93-324">Exemple d’utilisation: **/MANAGEMENT_DB_ CUSTOM_SQLINSTANCE = "MYSQLSERVER"**.</span><span class="sxs-lookup"><span data-stu-id="f8b93-324">Example usage: **/MANAGEMENT_DB_ CUSTOM_SQLINSTANCE="MYSQLSERVER"**.</span></span> <span data-ttu-id="f8b93-325">Si **/DB_PREDEPLOY_MANAGEMENT** n’est pas spécifié, la valeur est ignorée.</span><span class="sxs-lookup"><span data-stu-id="f8b93-325">If **/DB_PREDEPLOY_MANAGEMENT** is not specified, this will be ignored.</span></span> |
| <span data-ttu-id="f8b93-326">/MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="f8b93-326">/MANAGEMENT_DB_NAME</span></span> | <span data-ttu-id="f8b93-327">Spécifie le nom de la nouvelle base de données de gestion à créer.</span><span class="sxs-lookup"><span data-stu-id="f8b93-327">Specifies the name of the new management database that should be created.</span></span> <span data-ttu-id="f8b93-328">Exemple d’utilisation: **/MANAGEMENT_DB_NAME = «AppVMgmtDB»**.</span><span class="sxs-lookup"><span data-stu-id="f8b93-328">Example usage: **/MANAGEMENT_DB_NAME="AppVMgmtDB"**.</span></span> <span data-ttu-id="f8b93-329">Si **/DB_PREDEPLOY_MANAGEMENT** n’est pas spécifié, la valeur est ignorée.</span><span class="sxs-lookup"><span data-stu-id="f8b93-329">If **/DB_PREDEPLOY_MANAGEMENT** is not specified, this will be ignored.</span></span> |
| <span data-ttu-id="f8b93-330">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="f8b93-330">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span></span> | <span data-ttu-id="f8b93-331">Indique si le serveur de gestion qui accède à la base de données est installé sur le serveur local.</span><span class="sxs-lookup"><span data-stu-id="f8b93-331">Indicates if the management server that will be accessing the database is installed on the local server.</span></span> <span data-ttu-id="f8b93-332">Basculez le paramètre de sorte qu’aucune valeur ne soit attendue.</span><span class="sxs-lookup"><span data-stu-id="f8b93-332">Switch parameter so no value is expected.</span></span> |
| <span data-ttu-id="f8b93-333">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="f8b93-333">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span></span> | <span data-ttu-id="f8b93-334">Spécifie le compte d’ordinateur de l’ordinateur distant sur lequel le serveur de gestion sera installé.</span><span class="sxs-lookup"><span data-stu-id="f8b93-334">Specifies the machine account of the remote machine that the management server will be installed on.</span></span> <span data-ttu-id="f8b93-335">Exemple d’utilisation: **/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT = «domain\\computername»**</span><span class="sxs-lookup"><span data-stu-id="f8b93-335">Example usage: **/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT="domain\\computername"**</span></span> |
| <span data-ttu-id="f8b93-336">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="f8b93-336">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span></span> | <span data-ttu-id="f8b93-337">Indique le compte d’administrateur qui sera utilisé pour installer le serveur de gestion.</span><span class="sxs-lookup"><span data-stu-id="f8b93-337">Indicates the Administrator account that will be used to install the management server.</span></span> <span data-ttu-id="f8b93-338">Exemple d’utilisation: **/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT = «domain\\alias»**</span><span class="sxs-lookup"><span data-stu-id="f8b93-338">Example usage: **/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT ="domain\\alias"**</span></span> |

#### <span data-ttu-id="f8b93-339">Paramètres pour l’installation d’un serveur de publication</span><span class="sxs-lookup"><span data-stu-id="f8b93-339">Parameters for Installing Publishing Server</span></span>

| <span data-ttu-id="f8b93-340">Paramètre</span><span class="sxs-lookup"><span data-stu-id="f8b93-340">Parameter</span></span> | <span data-ttu-id="f8b93-341">Informations</span><span class="sxs-lookup"><span data-stu-id="f8b93-341">Information</span></span> |
|--|--|
| <span data-ttu-id="f8b93-342">/PUBLISHING_SERVER</span><span class="sxs-lookup"><span data-stu-id="f8b93-342">/PUBLISHING_SERVER</span></span> | <span data-ttu-id="f8b93-343">Spécifie que le serveur de publication sera installé.</span><span class="sxs-lookup"><span data-stu-id="f8b93-343">Specifies that the Publishing Server will be installed.</span></span> <span data-ttu-id="f8b93-344">Aucune valeur n’est attendue.</span><span class="sxs-lookup"><span data-stu-id="f8b93-344">No value is expected.</span></span> |
| <span data-ttu-id="f8b93-345">/PUBLISHING_MGT_SERVER</span><span class="sxs-lookup"><span data-stu-id="f8b93-345">/PUBLISHING_MGT_SERVER</span></span> | <span data-ttu-id="f8b93-346">Spécifie l’URL du service de gestion auquel est connecté le serveur de publication.</span><span class="sxs-lookup"><span data-stu-id="f8b93-346">Specifies the URL to Management Service the Publishing server will connect to.</span></span> <span data-ttu-id="f8b93-347">Exemple d’utilisation: **http:// &lt; Management Server name &gt; : numéro &lt; &gt; de port du serveur de gestion**.</span><span class="sxs-lookup"><span data-stu-id="f8b93-347">Example usage: **http://&lt;management server name&gt;:&lt;Management server port number&gt;**.</span></span> <span data-ttu-id="f8b93-348">Si **/PUBLISHING_SERVER** n’est pas utilisé, ce paramètre est ignoré.</span><span class="sxs-lookup"><span data-stu-id="f8b93-348">If **/PUBLISHING_SERVER** is not used, this parameter will be ignored.</span></span> |
| <span data-ttu-id="f8b93-349">/PUBLISHING_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="f8b93-349">/PUBLISHING_WEBSITE_NAME</span></span> | <span data-ttu-id="f8b93-350">Spécifie le nom du site Web qui sera créé pour le service de publication.</span><span class="sxs-lookup"><span data-stu-id="f8b93-350">Specifies name of the website that will be created for the publishing service.</span></span> <span data-ttu-id="f8b93-351">Exemple d’utilisation: **/PUBLISHING_WEBSITE_NAME = «service de publication Microsoft App-V»**</span><span class="sxs-lookup"><span data-stu-id="f8b93-351">Example usage: **/PUBLISHING_WEBSITE_NAME="Microsoft App-V Publishing Service"**</span></span> |
| <span data-ttu-id="f8b93-352">/PUBLISHING_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="f8b93-352">/PUBLISHING_WEBSITE_PORT</span></span> | <span data-ttu-id="f8b93-353">Spécifie le numéro de port utilisé par le service de publication.</span><span class="sxs-lookup"><span data-stu-id="f8b93-353">Specifies the port number used by the publishing service.</span></span> <span data-ttu-id="f8b93-354">Exemple d’utilisation: **/PUBLISHING_WEBSITE_PORT = 83**</span><span class="sxs-lookup"><span data-stu-id="f8b93-354">Example usage: **/PUBLISHING_WEBSITE_PORT=83**</span></span> |

#### <span data-ttu-id="f8b93-355">Paramètres pour le serveur de création de rapports</span><span class="sxs-lookup"><span data-stu-id="f8b93-355">Parameters for Reporting Server</span></span>

| <span data-ttu-id="f8b93-356">Paramètre</span><span class="sxs-lookup"><span data-stu-id="f8b93-356">Parameter</span></span> | <span data-ttu-id="f8b93-357">Informations</span><span class="sxs-lookup"><span data-stu-id="f8b93-357">Information</span></span> |
|--|--|
| <span data-ttu-id="f8b93-358">/REPORTING_SERVER</span><span class="sxs-lookup"><span data-stu-id="f8b93-358">/REPORTING_SERVER</span></span> | <span data-ttu-id="f8b93-359">Spécifie que le serveur de rapports sera installé.</span><span class="sxs-lookup"><span data-stu-id="f8b93-359">Specifies that the Reporting Server will be installed.</span></span> <span data-ttu-id="f8b93-360">Aucune valeur n’est attendue.</span><span class="sxs-lookup"><span data-stu-id="f8b93-360">No value is expected.</span></span> |
| <span data-ttu-id="f8b93-361">/REPORTING_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="f8b93-361">/REPORTING_WEBSITE_NAME</span></span> | <span data-ttu-id="f8b93-362">Spécifie le nom du site Web qui sera créé pour le service de création de rapports.</span><span class="sxs-lookup"><span data-stu-id="f8b93-362">Specifies name of the website that will be created for the Reporting Service.</span></span> <span data-ttu-id="f8b93-363">Exemple d’utilisation: **/REPORTING_WEBSITE_NAME = "Microsoft App-V ReportingService"**</span><span class="sxs-lookup"><span data-stu-id="f8b93-363">Example usage: **/REPORTING_WEBSITE_NAME="Microsoft App-V ReportingService"**</span></span> |
| <span data-ttu-id="f8b93-364">/REPORTING_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="f8b93-364">/REPORTING_WEBSITE_PORT</span></span> | <span data-ttu-id="f8b93-365">Spécifie le numéro de port que le service de création de rapports utilisera.</span><span class="sxs-lookup"><span data-stu-id="f8b93-365">Specifies the port number that the Reporting Service will use.</span></span> <span data-ttu-id="f8b93-366">Exemple d’utilisation: **/REPORTING_WEBSITE_PORT = 82**</span><span class="sxs-lookup"><span data-stu-id="f8b93-366">Example usage: **/REPORTING_WEBSITE_PORT=82**</span></span> |

#### <span data-ttu-id="f8b93-367">Paramètres d’utilisation d’une base de données serveur de création de rapports existante</span><span class="sxs-lookup"><span data-stu-id="f8b93-367">Parameters for using an Existing Reporting Server Database</span></span>

| <span data-ttu-id="f8b93-368">Paramètre</span><span class="sxs-lookup"><span data-stu-id="f8b93-368">Parameter</span></span> | <span data-ttu-id="f8b93-369">Informations</span><span class="sxs-lookup"><span data-stu-id="f8b93-369">Information</span></span> |
|--|--|
| <span data-ttu-id="f8b93-370">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="f8b93-370">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span></span> | <span data-ttu-id="f8b93-371">Indique que Microsoft SQL Server est installé sur le serveur local.</span><span class="sxs-lookup"><span data-stu-id="f8b93-371">Indicates that the Microsoft SQL Server is installed on the local server.</span></span> <span data-ttu-id="f8b93-372">Basculez le paramètre de sorte qu’aucune valeur ne soit attendue.</span><span class="sxs-lookup"><span data-stu-id="f8b93-372">Switch parameter so no value is expected.</span></span> |
| <span data-ttu-id="f8b93-373">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="f8b93-373">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</span></span> | <span data-ttu-id="f8b93-374">Spécifie le nom de l’ordinateur distant sur lequel SQL Server est installé.</span><span class="sxs-lookup"><span data-stu-id="f8b93-374">Specifies the name of the remote computer that SQL Server is installed on.</span></span> <span data-ttu-id="f8b93-375">Prend une chaîne.</span><span class="sxs-lookup"><span data-stu-id="f8b93-375">Takes a string.</span></span> <span data-ttu-id="f8b93-376">Exemple d’utilisation: **/EXISTING_REPORTING_DB_ REMOTE_SQL_SERVER_NAME = "mycomputer1"**</span><span class="sxs-lookup"><span data-stu-id="f8b93-376">Example usage: **/EXISTING_REPORTING_DB_ REMOTE_SQL_SERVER_NAME="mycomputer1"**</span></span> |
| <span data-ttu-id="f8b93-377">_DB_SQLINSTANCE_USE_DEFAULT EXISTING_ DE CRÉATION DE RAPPORTS</span><span class="sxs-lookup"><span data-stu-id="f8b93-377">/EXISTING_ REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span></span> | <span data-ttu-id="f8b93-378">Indique que l’instance SQL par défaut doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="f8b93-378">Indicates that the default SQL instance is to be used.</span></span> <span data-ttu-id="f8b93-379">Basculez le paramètre de sorte qu’aucune valeur ne soit attendue.</span><span class="sxs-lookup"><span data-stu-id="f8b93-379">Switch parameter so no value is expected.</span></span> |
| <span data-ttu-id="f8b93-380">/EXISTING_ REPORTING_DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="f8b93-380">/EXISTING_ REPORTING_DB_CUSTOM_SQLINSTANCE</span></span> | <span data-ttu-id="f8b93-381">Spécifie le nom de l’instance SQL personnalisée qui doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="f8b93-381">Specifies the name of the custom SQL instance that should be used.</span></span> <span data-ttu-id="f8b93-382">Prend une chaîne.</span><span class="sxs-lookup"><span data-stu-id="f8b93-382">Takes a string.</span></span> <span data-ttu-id="f8b93-383">Exemple d’utilisation: **/EXISTING_REPORTING_DB_ CUSTOM_SQLINSTANCE = "MYSQLSERVER"**</span><span class="sxs-lookup"><span data-stu-id="f8b93-383">Example usage: **/EXISTING_REPORTING_DB_ CUSTOM_SQLINSTANCE="MYSQLSERVER"**</span></span> |
| <span data-ttu-id="f8b93-384">_DB_NAME EXISTING_ DE CRÉATION DE RAPPORTS</span><span class="sxs-lookup"><span data-stu-id="f8b93-384">/EXISTING_ REPORTING _DB_NAME</span></span> | <span data-ttu-id="f8b93-385">Spécifie le nom de la base de données de création de rapports existante à utiliser.</span><span class="sxs-lookup"><span data-stu-id="f8b93-385">Specifies the name of the existing Reporting database that should be used.</span></span> <span data-ttu-id="f8b93-386">Prend une chaîne.</span><span class="sxs-lookup"><span data-stu-id="f8b93-386">Takes a string.</span></span> <span data-ttu-id="f8b93-387">Exemple d’utilisation: **/EXISTING_REPORTING_DB_NAME = «AppVReporting»**</span><span class="sxs-lookup"><span data-stu-id="f8b93-387">Example usage: **/EXISTING_REPORTING_DB_NAME="AppVReporting"**</span></span> |

#### <span data-ttu-id="f8b93-388">Paramètres pour l’installation de la base de données serveur de création de rapports</span><span class="sxs-lookup"><span data-stu-id="f8b93-388">Parameters for installing Reporting Server Database</span></span>

| <span data-ttu-id="f8b93-389">Paramètre</span><span class="sxs-lookup"><span data-stu-id="f8b93-389">Parameter</span></span> | <span data-ttu-id="f8b93-390">Informations</span><span class="sxs-lookup"><span data-stu-id="f8b93-390">Information</span></span> |
|--|--|
| <span data-ttu-id="f8b93-391">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="f8b93-391">/DB_PREDEPLOY_REPORTING</span></span> | <span data-ttu-id="f8b93-392">Spécifie que la base de données de création de rapports sera installée.</span><span class="sxs-lookup"><span data-stu-id="f8b93-392">Specifies that the Reporting Database will be installed.</span></span> <span data-ttu-id="f8b93-393">Des autorisations DBA sont nécessaires pour cette installation.</span><span class="sxs-lookup"><span data-stu-id="f8b93-393">DBA permissions are required for this installation.</span></span> <span data-ttu-id="f8b93-394">Aucune valeur n’est attendue.</span><span class="sxs-lookup"><span data-stu-id="f8b93-394">No value is expected.</span></span> |
| <span data-ttu-id="f8b93-395">/REPORTING_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="f8b93-395">/REPORTING_DB_SQLINSTANCE_USE_DEFAULT</span></span> | <span data-ttu-id="f8b93-396">Spécifie le nom de l’instance SQL personnalisée qui doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="f8b93-396">Specifies the name of the custom SQL instance that should be used.</span></span> <span data-ttu-id="f8b93-397">Prend une chaîne.</span><span class="sxs-lookup"><span data-stu-id="f8b93-397">Takes a string.</span></span> <span data-ttu-id="f8b93-398">Exemple d’utilisation: **/REPORTING_DB_ CUSTOM_SQLINSTANCE = "MYSQLSERVER"**</span><span class="sxs-lookup"><span data-stu-id="f8b93-398">Example usage: **/REPORTING_DB_ CUSTOM_SQLINSTANCE="MYSQLSERVER"**</span></span> |
| <span data-ttu-id="f8b93-399">/REPORTING_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="f8b93-399">/REPORTING_DB_NAME</span></span> | <span data-ttu-id="f8b93-400">Spécifie le nom de la nouvelle base de données de création de rapports à créer.</span><span class="sxs-lookup"><span data-stu-id="f8b93-400">Specifies the name of the new Reporting database that should be created.</span></span> <span data-ttu-id="f8b93-401">Prend une chaîne.</span><span class="sxs-lookup"><span data-stu-id="f8b93-401">Takes a string.</span></span> <span data-ttu-id="f8b93-402">Exemple d’utilisation: **/REPORTING_DB_NAME = «AppVMgmtDB»**</span><span class="sxs-lookup"><span data-stu-id="f8b93-402">Example usage: **/REPORTING_DB_NAME="AppVMgmtDB"**</span></span> |
| <span data-ttu-id="f8b93-403">/REPORTING_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="f8b93-403">/REPORTING_SERVER_MACHINE_USE_LOCAL</span></span> | <span data-ttu-id="f8b93-404">Indique que le serveur de création de rapports qui accède à la base de données est installé sur le serveur local.</span><span class="sxs-lookup"><span data-stu-id="f8b93-404">Indicates that the Reporting server that will be accessing the database is installed on the local server.</span></span> <span data-ttu-id="f8b93-405">Basculez le paramètre de sorte qu’aucune valeur ne soit attendue.</span><span class="sxs-lookup"><span data-stu-id="f8b93-405">Switch parameter so no value is expected.</span></span> |
| <span data-ttu-id="f8b93-406">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="f8b93-406">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span></span> | <span data-ttu-id="f8b93-407">Spécifie le compte d’ordinateur de l’ordinateur distant sur lequel est installé le serveur de rapports.</span><span class="sxs-lookup"><span data-stu-id="f8b93-407">Specifies the machine account of the remote machine that the Reporting server will be installed on.</span></span> <span data-ttu-id="f8b93-408">Prend une chaîne.</span><span class="sxs-lookup"><span data-stu-id="f8b93-408">Takes a string.</span></span> <span data-ttu-id="f8b93-409">Exemple d’utilisation: **/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT = «domain\computername»**</span><span class="sxs-lookup"><span data-stu-id="f8b93-409">Example usage: **/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT="domain\computername"**</span></span> |
| <span data-ttu-id="f8b93-410">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="f8b93-410">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span></span> | <span data-ttu-id="f8b93-411">Indique le compte d’administrateur qui sera utilisé pour installer le serveur de création de rapports App-V.</span><span class="sxs-lookup"><span data-stu-id="f8b93-411">Indicates the Administrator account that will be used to install the App-V Reporting Server.</span></span> <span data-ttu-id="f8b93-412">Prend une chaîne.</span><span class="sxs-lookup"><span data-stu-id="f8b93-412">Takes a string.</span></span> <span data-ttu-id="f8b93-413">Exemple d’utilisation: **/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT = «domain\\alias»**</span><span class="sxs-lookup"><span data-stu-id="f8b93-413">Example usage: **/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT="domain\\alias"**</span></span> |

#### <span data-ttu-id="f8b93-414">Paramètres d’utilisation d’une base de données serveur de gestion existante</span><span class="sxs-lookup"><span data-stu-id="f8b93-414">Parameters for using an existing Management Server Database</span></span>

| <span data-ttu-id="f8b93-415">Paramètre</span><span class="sxs-lookup"><span data-stu-id="f8b93-415">Parameter</span></span> | <span data-ttu-id="f8b93-416">Informations</span><span class="sxs-lookup"><span data-stu-id="f8b93-416">Information</span></span> |
|--|--|
| <span data-ttu-id="f8b93-417">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="f8b93-417">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span></span> | <span data-ttu-id="f8b93-418">Indique que SQL Server est installé sur le serveur local.</span><span class="sxs-lookup"><span data-stu-id="f8b93-418">Indicates that the SQL Server is installed on the local server.</span></span> <span data-ttu-id="f8b93-419">Basculez le paramètre de sorte qu’aucune valeur ne soit attendue. Si **/DB_PREDEPLOY_MANAGEMENT** est spécifiée, la valeur est ignorée.</span><span class="sxs-lookup"><span data-stu-id="f8b93-419">Switch parameter so no value is expected.If **/DB_PREDEPLOY_MANAGEMENT** is specified, this will be ignored.</span></span> |
| <span data-ttu-id="f8b93-420">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="f8b93-420">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</span></span> | <span data-ttu-id="f8b93-421">Spécifie le nom de l’ordinateur distant sur lequel SQL Server est installé.</span><span class="sxs-lookup"><span data-stu-id="f8b93-421">Specifies the name of the remote computer that SQL Server is installed on.</span></span> <span data-ttu-id="f8b93-422">Prend une chaîne.</span><span class="sxs-lookup"><span data-stu-id="f8b93-422">Takes a string.</span></span> <span data-ttu-id="f8b93-423">Exemple d’utilisation: **/EXISTING_MANAGEMENT_DB_ REMOTE_SQL_SERVER_NAME = "mycomputer1"**</span><span class="sxs-lookup"><span data-stu-id="f8b93-423">Example usage: **/EXISTING_MANAGEMENT_DB_ REMOTE_SQL_SERVER_NAME="mycomputer1"**</span></span> |
| <span data-ttu-id="f8b93-424">/EXISTING_ MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="f8b93-424">/EXISTING_ MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span> | <span data-ttu-id="f8b93-425">Indique que l’instance SQL par défaut doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="f8b93-425">Indicates that the default SQL instance is to be used.</span></span> <span data-ttu-id="f8b93-426">Basculez le paramètre de sorte qu’aucune valeur ne soit attendue.</span><span class="sxs-lookup"><span data-stu-id="f8b93-426">Switch parameter so no value is expected.</span></span> <span data-ttu-id="f8b93-427">Si **/DB_PREDEPLOY_MANAGEMENT** est spécifiée, la valeur est ignorée.</span><span class="sxs-lookup"><span data-stu-id="f8b93-427">If **/DB_PREDEPLOY_MANAGEMENT** is specified, this will be ignored.</span></span> |
| <span data-ttu-id="f8b93-428">/EXISTING_MANAGEMENT_DB_ CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="f8b93-428">/EXISTING_MANAGEMENT_DB_ CUSTOM_SQLINSTANCE</span></span> | <span data-ttu-id="f8b93-429">Spécifie le nom de l’instance SQL personnalisée qui sera utilisée.</span><span class="sxs-lookup"><span data-stu-id="f8b93-429">Specifies the name of the custom SQL instance that will be used.</span></span> <span data-ttu-id="f8b93-430">Exemple d’utilisation **/EXISTING_MANAGEMENT_DB_ CUSTOM_SQLINSTANCE = "AppVManagement"**.</span><span class="sxs-lookup"><span data-stu-id="f8b93-430">Example usage **/EXISTING_MANAGEMENT_DB_ CUSTOM_SQLINSTANCE="AppVManagement"**.</span></span> <span data-ttu-id="f8b93-431">Si **/DB_PREDEPLOY_MANAGEMENT** est spécifiée, la valeur est ignorée.</span><span class="sxs-lookup"><span data-stu-id="f8b93-431">If **/DB_PREDEPLOY_MANAGEMENT** is specified, this will be ignored.</span></span> |
| <span data-ttu-id="f8b93-432">/EXISTING_MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="f8b93-432">/EXISTING_MANAGEMENT_DB_NAME</span></span> | <span data-ttu-id="f8b93-433">Spécifie le nom de la base de données de gestion existante à utiliser.</span><span class="sxs-lookup"><span data-stu-id="f8b93-433">Specifies the name of the existing management database that should be used.</span></span> <span data-ttu-id="f8b93-434">Exemple d’utilisation: **/EXISTING_MANAGEMENT_DB_NAME = «AppVMgmtDB»**.</span><span class="sxs-lookup"><span data-stu-id="f8b93-434">Example usage: **/EXISTING_MANAGEMENT_DB_NAME="AppVMgmtDB"**.</span></span> <span data-ttu-id="f8b93-435">Si **/DB_PREDEPLOY_MANAGEMENT** est spécifiée, la valeur est ignorée.</span><span class="sxs-lookup"><span data-stu-id="f8b93-435">If **/DB_PREDEPLOY_MANAGEMENT** is specified, this will be ignored.</span></span> |

<span data-ttu-id="f8b93-436">Vous avez un problème lié à l’application-V?</span><span class="sxs-lookup"><span data-stu-id="f8b93-436">Got an App-V issue?</span></span> <span data-ttu-id="f8b93-437">Utilisez le [Forum TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="f8b93-437">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="f8b93-438">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f8b93-438">Related topics</span></span>

[<span data-ttu-id="f8b93-439">Déploiement d'App-V5.1 Server</span><span class="sxs-lookup"><span data-stu-id="f8b93-439">Deploying the App-V 5.1 Server</span></span>](deploying-the-app-v-51-server.md)
