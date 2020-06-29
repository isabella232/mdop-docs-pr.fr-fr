---
title: Déploiement du serveur App-V5.0 à l'aide d'un script
description: Déploiement du serveur App-V5.0 à l'aide d'un script
author: dansimp
ms.assetid: b91a35c8-df9e-4065-9187-abafbe565b84
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/15/2018
ms.openlocfilehash: aeb16d166fe7b1c4bb418c212024c49f6b151b94
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805526"
---
# <span data-ttu-id="c3d8d-103">Déploiement du serveur App-V5.0 à l'aide d'un script</span><span class="sxs-lookup"><span data-stu-id="c3d8d-103">How to Deploy the App-V 5.0 Server Using a Script</span></span>


<span data-ttu-id="c3d8d-104">Pour pouvoir terminer la configuration du serveur **appv\_server\_setup.exe** à l’aide de la ligne de commande, vous devez spécifier et combiner plusieurs paramètres.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-104">In order to complete the **appv\_server\_setup.exe** Server setup successfully using the command line, you must specify and combine multiple parameters.</span></span>

<span data-ttu-id="c3d8d-105">Pour plus d’informations sur l’installation du serveur App-V 5,0 à l’aide de la ligne de commande, utilisez les tableaux suivants.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-105">Use the following tables for more information about installing the App-V 5.0 server using the command line.</span></span>

>[!NOTE]
> <span data-ttu-id="c3d8d-106">Vous pouvez également accéder aux informations des tables suivantes à l’aide de la ligne de commande en entrant la commande suivante:</span><span class="sxs-lookup"><span data-stu-id="c3d8d-106">The information in the following tables can also be accessed using the command line by typing the following command:</span></span>
>```
> appv\_server\_setup.exe /?
>```

## <span data-ttu-id="c3d8d-107">Paramètres courants et exemples</span><span class="sxs-lookup"><span data-stu-id="c3d8d-107">Common parameters and Examples</span></span>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="c3d8d-108">Pour installer le serveur de gestion et la base de données de gestion sur un ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-108">To Install the Management server and Management database on a local machine.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c3d8d-109">Pour utiliser l’instance par défaut de Microsoft SQL Server, utilisez les paramètres suivants:</span><span class="sxs-lookup"><span data-stu-id="c3d8d-109">To use the default instance of Microsoft SQL Server, use the following parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="c3d8d-110">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="c3d8d-110">/MANAGEMENT_SERVER</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-111">/MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="c3d8d-111">/MANAGEMENT_ADMINACCOUNT</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-112">/MANAGEMENT_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="c3d8d-112">/MANAGEMENT_WEBSITE_NAME</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-113">/MANAGEMENT_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="c3d8d-113">/MANAGEMENT_WEBSITE_PORT</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-114">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="c3d8d-114">/DB_PREDEPLOY_MANAGEMENT</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-115">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="c3d8d-115">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-116">/MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="c3d8d-116">/MANAGEMENT_DB_NAME</span></span></p></li>
    </ul>
    <p><span data-ttu-id="c3d8d-117">Pour utiliser une instance personnalisée de Microsoft SQL Server, utilisez les paramètres suivants:</span><span class="sxs-lookup"><span data-stu-id="c3d8d-117">To use a custom instance of Microsoft SQL Server, use the following parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="c3d8d-118">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="c3d8d-118">/MANAGEMENT_SERVER</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-119">/MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="c3d8d-119">/MANAGEMENT_ADMINACCOUNT</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-120">/MANAGEMENT_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="c3d8d-120">/MANAGEMENT_WEBSITE_NAME</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-121">/MANAGEMENT_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="c3d8d-121">/MANAGEMENT_WEBSITE_PORT</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-122">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="c3d8d-122">/DB_PREDEPLOY_MANAGEMENT</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-123">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="c3d8d-123">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-124">/MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="c3d8d-124">/MANAGEMENT_DB_NAME</span></span></p></li>
    </ul>
    <p><span data-ttu-id="c3d8d-125">Utilisation d’une instance personnalisée de Microsoft SQL Server par exemple:</span><span class="sxs-lookup"><span data-stu-id="c3d8d-125">Using a custom instance of Microsoft SQL Server example:</span></span></p>
    <p><span data-ttu-id="c3d8d-126">/appv_server_setup.exe/QUIET</span><span class="sxs-lookup"><span data-stu-id="c3d8d-126">/appv_server_setup.exe /QUIET</span></span></p>
    <p><span data-ttu-id="c3d8d-127">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="c3d8d-127">/MANAGEMENT_SERVER</span></span></p>
    <p><span data-ttu-id="c3d8d-128">/MANAGEMENT_ADMINACCOUNT = "Domain\AdminGroup"</span><span class="sxs-lookup"><span data-stu-id="c3d8d-128">/MANAGEMENT_ADMINACCOUNT=”Domain\AdminGroup”</span></span></p>
    <p><span data-ttu-id="c3d8d-129">/MANAGEMENT_WEBSITE_NAME = «service de gestion Microsoft AppV»</span><span class="sxs-lookup"><span data-stu-id="c3d8d-129">/MANAGEMENT_WEBSITE_NAME=”Microsoft AppV Management Service”</span></span></p>
    <p><span data-ttu-id="c3d8d-130">/MANAGEMENT_WEBSITE_PORT = "8080"</span><span class="sxs-lookup"><span data-stu-id="c3d8d-130">/MANAGEMENT_WEBSITE_PORT=”8080”</span></span></p>
    <p><span data-ttu-id="c3d8d-131">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="c3d8d-131">/DB_PREDEPLOY_MANAGEMENT</span></span></p>
    <p><span data-ttu-id="c3d8d-132">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</span><span class="sxs-lookup"><span data-stu-id="c3d8d-132">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE=”SqlInstanceName”</span></span></p>
    <p><span data-ttu-id="c3d8d-133">/MANAGEMENT_DB_NAME = "AppVManagement"</span><span class="sxs-lookup"><span data-stu-id="c3d8d-133">/MANAGEMENT_DB_NAME=”AppVManagement”</span></span></p></td>
    </tr>
    </tbody>
    </table>
     
<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="c3d8d-134">Pour installer le serveur de gestion à l’aide d’une base de données de gestion existante sur un ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-134">To Install the Management server using an existing Management database on a local machine.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c3d8d-135">Pour utiliser l’instance par défaut de Microsoft SQL Server, utilisez les paramètres suivants:</span><span class="sxs-lookup"><span data-stu-id="c3d8d-135">To use the default instance of Microsoft SQL Server, use the following parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="c3d8d-136">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="c3d8d-136">/MANAGEMENT_SERVER</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-137">/MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="c3d8d-137">/MANAGEMENT_ADMINACCOUNT</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-138">/MANAGEMENT_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="c3d8d-138">/MANAGEMENT_WEBSITE_NAME</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-139">/MANAGEMENT_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="c3d8d-139">/MANAGEMENT_WEBSITE_PORT</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-140">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="c3d8d-140">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-141">/EXISTING_MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="c3d8d-141">/EXISTING_MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-142">/EXISTING_MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="c3d8d-142">/EXISTING_MANAGEMENT_DB_NAME</span></span></p></li>
    </ul>
    <p><span data-ttu-id="c3d8d-143">Pour utiliser une instance personnalisée de Microsoft SQL Server, utilisez les paramètres suivants:</span><span class="sxs-lookup"><span data-stu-id="c3d8d-143">To use a custom instance of Microsoft SQL Server, use these parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="c3d8d-144">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="c3d8d-144">/MANAGEMENT_SERVER</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-145">/MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="c3d8d-145">/MANAGEMENT_ADMINACCOUNT</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-146">/MANAGEMENT_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="c3d8d-146">/MANAGEMENT_WEBSITE_NAME</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-147">/MANAGEMENT_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="c3d8d-147">/MANAGEMENT_WEBSITE_PORT</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-148">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="c3d8d-148">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-149">/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="c3d8d-149">/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-150">/EXISTING_MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="c3d8d-150">/EXISTING_MANAGEMENT_DB_NAME</span></span></p></li>
    </ul>
    <p><span data-ttu-id="c3d8d-151">Utilisation d’une instance personnalisée de Microsoft SQL Server par exemple:</span><span class="sxs-lookup"><span data-stu-id="c3d8d-151">Using a custom instance of Microsoft SQL Server example:</span></span></p>
    <p><span data-ttu-id="c3d8d-152">/appv_server_setup.exe/QUIET</span><span class="sxs-lookup"><span data-stu-id="c3d8d-152">/appv_server_setup.exe /QUIET</span></span></p>
    <p><span data-ttu-id="c3d8d-153">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="c3d8d-153">/MANAGEMENT_SERVER</span></span></p>
    <p><span data-ttu-id="c3d8d-154">/MANAGEMENT_ADMINACCOUNT = "Domain\AdminGroup"</span><span class="sxs-lookup"><span data-stu-id="c3d8d-154">/MANAGEMENT_ADMINACCOUNT=”Domain\AdminGroup”</span></span></p>
    <p><span data-ttu-id="c3d8d-155">/MANAGEMENT_WEBSITE_NAME = «service de gestion Microsoft AppV»</span><span class="sxs-lookup"><span data-stu-id="c3d8d-155">/MANAGEMENT_WEBSITE_NAME=”Microsoft AppV Management Service”</span></span></p>
    <p><span data-ttu-id="c3d8d-156">/MANAGEMENT_WEBSITE_PORT = "8080"</span><span class="sxs-lookup"><span data-stu-id="c3d8d-156">/MANAGEMENT_WEBSITE_PORT=”8080”</span></span></p>
    <p><span data-ttu-id="c3d8d-157">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="c3d8d-157">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span></span></p>
    <p><span data-ttu-id="c3d8d-158">/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</span><span class="sxs-lookup"><span data-stu-id="c3d8d-158">/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE =”SqlInstanceName”</span></span></p>
    <p><span data-ttu-id="c3d8d-159">/EXISTING_MANAGEMENT_DB_NAME = "AppVManagement"</span><span class="sxs-lookup"><span data-stu-id="c3d8d-159">/EXISTING_MANAGEMENT_DB_NAME =”AppVManagement”</span></span></p></td>
    </tr>
    </tbody>
    </table>  

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="c3d8d-160">Pour installer le serveur de gestion à l’aide d’une base de données de gestion existante sur un ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-160">To install the Management server using an existing Management database on a remote machine.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c3d8d-161">Pour utiliser l’instance par défaut de Microsoft SQL Server, utilisez les paramètres suivants:</span><span class="sxs-lookup"><span data-stu-id="c3d8d-161">To use the default instance of Microsoft SQL Server, use the following parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="c3d8d-162">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="c3d8d-162">/MANAGEMENT_SERVER</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-163">/MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="c3d8d-163">/MANAGEMENT_ADMINACCOUNT</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-164">/MANAGEMENT_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="c3d8d-164">/MANAGEMENT_WEBSITE_NAME</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-165">/MANAGEMENT_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="c3d8d-165">/MANAGEMENT_WEBSITE_PORT</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-166">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="c3d8d-166">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-167">/EXISTING_MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="c3d8d-167">/EXISTING_MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-168">/EXISTING_MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="c3d8d-168">/EXISTING_MANAGEMENT_DB_NAME</span></span></p></li>
    </ul>
    <p><span data-ttu-id="c3d8d-169">Pour utiliser une instance personnalisée de Microsoft SQL Server, utilisez les paramètres suivants:</span><span class="sxs-lookup"><span data-stu-id="c3d8d-169">To use a custom instance of Microsoft SQL Server, use these parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="c3d8d-170">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="c3d8d-170">/MANAGEMENT_SERVER</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-171">/MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="c3d8d-171">/MANAGEMENT_ADMINACCOUNT</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-172">/MANAGEMENT_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="c3d8d-172">/MANAGEMENT_WEBSITE_NAME</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-173">/MANAGEMENT_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="c3d8d-173">/MANAGEMENT_WEBSITE_PORT</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-174">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="c3d8d-174">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-175">/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="c3d8d-175">/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-176">/EXISTING_MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="c3d8d-176">/EXISTING_MANAGEMENT_DB_NAME</span></span></p></li>
    </ul>
    <p><span data-ttu-id="c3d8d-177">Utilisation d’une instance personnalisée de Microsoft SQL Server par exemple:</span><span class="sxs-lookup"><span data-stu-id="c3d8d-177">Using a custom instance of Microsoft SQL Server example:</span></span></p>
    <p><span data-ttu-id="c3d8d-178">/appv_server_setup.exe/QUIET</span><span class="sxs-lookup"><span data-stu-id="c3d8d-178">/appv_server_setup.exe /QUIET</span></span></p>
    <p><span data-ttu-id="c3d8d-179">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="c3d8d-179">/MANAGEMENT_SERVER</span></span></p>
    <p><span data-ttu-id="c3d8d-180">/MANAGEMENT_ADMINACCOUNT = "Domain\AdminGroup"</span><span class="sxs-lookup"><span data-stu-id="c3d8d-180">/MANAGEMENT_ADMINACCOUNT=”Domain\AdminGroup”</span></span></p>
    <p><span data-ttu-id="c3d8d-181">/MANAGEMENT_WEBSITE_NAME = «service de gestion Microsoft AppV»</span><span class="sxs-lookup"><span data-stu-id="c3d8d-181">/MANAGEMENT_WEBSITE_NAME=”Microsoft AppV Management Service”</span></span></p>
    <p><span data-ttu-id="c3d8d-182">/MANAGEMENT_WEBSITE_PORT = "8080"</span><span class="sxs-lookup"><span data-stu-id="c3d8d-182">/MANAGEMENT_WEBSITE_PORT=”8080”</span></span></p>
    <p><span data-ttu-id="c3d8d-183">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME = "SqlServermachine. nom_domaine"</span><span class="sxs-lookup"><span data-stu-id="c3d8d-183">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME=”SqlServermachine.domainName”</span></span></p>
    <p><span data-ttu-id="c3d8d-184">/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</span><span class="sxs-lookup"><span data-stu-id="c3d8d-184">/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE =”SqlInstanceName”</span></span></p>
    <p><span data-ttu-id="c3d8d-185">/EXISTING_MANAGEMENT_DB_NAME = "AppVManagement"</span><span class="sxs-lookup"><span data-stu-id="c3d8d-185">/EXISTING_MANAGEMENT_DB_NAME =”AppVManagement”</span></span></p></td>
    </tr>
    </tbody>
    </table>
    
<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="c3d8d-186">Pour installer la base de données de gestion et le serveur de gestion sur le même ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-186">To Install the Management database and the Management Server on the same computer.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c3d8d-187">Pour utiliser l’instance par défaut de Microsoft SQL Server, utilisez les paramètres suivants:</span><span class="sxs-lookup"><span data-stu-id="c3d8d-187">To use the default instance of Microsoft SQL Server, use the following parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="c3d8d-188">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="c3d8d-188">/DB_PREDEPLOY_MANAGEMENT</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-189">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="c3d8d-189">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-190">/MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="c3d8d-190">/MANAGEMENT_DB_NAME</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-191">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="c3d8d-191">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-192">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="c3d8d-192">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></li>
    </ul>
    <p><span data-ttu-id="c3d8d-193">Pour utiliser une instance personnalisée de Microsoft SQL Server, utilisez les paramètres suivants:</span><span class="sxs-lookup"><span data-stu-id="c3d8d-193">To use a custom instance of Microsoft SQL Server, use these parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="c3d8d-194">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="c3d8d-194">/DB_PREDEPLOY_MANAGEMENT</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-195">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="c3d8d-195">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-196">/MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="c3d8d-196">/MANAGEMENT_DB_NAME</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-197">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="c3d8d-197">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-198">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="c3d8d-198">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></li>
    </ul>
    <p><span data-ttu-id="c3d8d-199">Utilisation d’une instance personnalisée de Microsoft SQL Server par exemple:</span><span class="sxs-lookup"><span data-stu-id="c3d8d-199">Using a custom instance of Microsoft SQL Server example:</span></span></p>
    <p><span data-ttu-id="c3d8d-200">/appv_server_setup.exe/QUIET</span><span class="sxs-lookup"><span data-stu-id="c3d8d-200">/appv_server_setup.exe /QUIET</span></span></p>
    <p><span data-ttu-id="c3d8d-201">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="c3d8d-201">/DB_PREDEPLOY_MANAGEMENT</span></span></p>
    <p><span data-ttu-id="c3d8d-202">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</span><span class="sxs-lookup"><span data-stu-id="c3d8d-202">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE=”SqlInstanceName”</span></span></p>
    <p><span data-ttu-id="c3d8d-203">/MANAGEMENT_DB_NAME = "AppVManagement"</span><span class="sxs-lookup"><span data-stu-id="c3d8d-203">/MANAGEMENT_DB_NAME=”AppVManagement”</span></span></p>
    <p><span data-ttu-id="c3d8d-204">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="c3d8d-204">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span></span></p>
    <p><span data-ttu-id="c3d8d-205">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT = "Domain\InstallAdminAccount"</span><span class="sxs-lookup"><span data-stu-id="c3d8d-205">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT=”Domain\InstallAdminAccount”</span></span></p></td>
    </tr>
    </tbody>
    </table>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="c3d8d-206">Pour installer la base de données de gestion sur un autre ordinateur que le serveur de gestion.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-206">To install the Management database on a different computer than the Management server.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c3d8d-207">Pour utiliser l’instance par défaut de Microsoft SQL Server, utilisez les paramètres suivants:</span><span class="sxs-lookup"><span data-stu-id="c3d8d-207">To use the default instance of Microsoft SQL Server, use the following parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="c3d8d-208">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="c3d8d-208">/DB_PREDEPLOY_MANAGEMENT</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-209">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="c3d8d-209">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-210">/MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="c3d8d-210">/MANAGEMENT_DB_NAME</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-211">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="c3d8d-211">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-212">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="c3d8d-212">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></li>
    </ul>
    <p><span data-ttu-id="c3d8d-213">Pour utiliser une instance personnalisée de Microsoft SQL Server, utilisez les paramètres suivants:</span><span class="sxs-lookup"><span data-stu-id="c3d8d-213">To use a custom instance of Microsoft SQL Server, use these parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="c3d8d-214">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="c3d8d-214">/DB_PREDEPLOY_MANAGEMENT</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-215">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="c3d8d-215">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-216">/MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="c3d8d-216">/MANAGEMENT_DB_NAME</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-217">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="c3d8d-217">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-218">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="c3d8d-218">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></li>
    </ul>
    <p><span data-ttu-id="c3d8d-219">Utilisation d’une instance personnalisée de Microsoft SQL Server par exemple:</span><span class="sxs-lookup"><span data-stu-id="c3d8d-219">Using a custom instance of Microsoft SQL Server example:</span></span></p>
    <p><span data-ttu-id="c3d8d-220">/appv_server_setup.exe/QUIET</span><span class="sxs-lookup"><span data-stu-id="c3d8d-220">/appv_server_setup.exe /QUIET</span></span></p>
    <p><span data-ttu-id="c3d8d-221">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="c3d8d-221">/DB_PREDEPLOY_MANAGEMENT</span></span></p>
    <p><span data-ttu-id="c3d8d-222">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</span><span class="sxs-lookup"><span data-stu-id="c3d8d-222">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE=”SqlInstanceName”</span></span></p>
    <p><span data-ttu-id="c3d8d-223">/MANAGEMENT_DB_NAME = "AppVManagement"</span><span class="sxs-lookup"><span data-stu-id="c3d8d-223">/MANAGEMENT_DB_NAME=”AppVManagement”</span></span></p>
    <p><span data-ttu-id="c3d8d-224">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT = "Domain\MachineAccount"</span><span class="sxs-lookup"><span data-stu-id="c3d8d-224">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT=”Domain\MachineAccount”</span></span></p>
    <p><span data-ttu-id="c3d8d-225">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT = "Domain\InstallAdminAccount"</span><span class="sxs-lookup"><span data-stu-id="c3d8d-225">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT=”Domain\InstallAdminAccount”</span></span></p></td>
    </tr>
    </tbody>
    </table>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="c3d8d-226">Pour installer le serveur de publication.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-226">To Install the publishing server.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c3d8d-227">Pour utiliser l’instance par défaut de Microsoft SQL Server, utilisez les paramètres suivants:</span><span class="sxs-lookup"><span data-stu-id="c3d8d-227">To use the default instance of Microsoft SQL Server, use the following parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="c3d8d-228">/PUBLISHING_SERVER</span><span class="sxs-lookup"><span data-stu-id="c3d8d-228">/PUBLISHING_SERVER</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-229">/PUBLISHING_MGT_SERVER</span><span class="sxs-lookup"><span data-stu-id="c3d8d-229">/PUBLISHING_MGT_SERVER</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-230">/PUBLISHING_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="c3d8d-230">/PUBLISHING_WEBSITE_NAME</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-231">/PUBLISHING_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="c3d8d-231">/PUBLISHING_WEBSITE_PORT</span></span></p></li>
    </ul>
    <p><span data-ttu-id="c3d8d-232">Utilisation d’une instance personnalisée de Microsoft SQL Server par exemple:</span><span class="sxs-lookup"><span data-stu-id="c3d8d-232">Using a custom instance of Microsoft SQL Server example:</span></span></p>
    <p><span data-ttu-id="c3d8d-233">/appv_server_setup.exe/QUIET</span><span class="sxs-lookup"><span data-stu-id="c3d8d-233">/appv_server_setup.exe /QUIET</span></span></p>
    <p><span data-ttu-id="c3d8d-234">/PUBLISHING_SERVER</span><span class="sxs-lookup"><span data-stu-id="c3d8d-234">/PUBLISHING_SERVER</span></span></p>
    <p><span data-ttu-id="c3d8d-235">/PUBLISHING_MGT_SERVER = " http://ManagementServerName:ManagementPort "</span><span class="sxs-lookup"><span data-stu-id="c3d8d-235">/PUBLISHING_MGT_SERVER=”http://ManagementServerName:ManagementPort”</span></span></p>
    <p><span data-ttu-id="c3d8d-236">/PUBLISHING_WEBSITE_NAME = «service de publication Microsoft AppV»</span><span class="sxs-lookup"><span data-stu-id="c3d8d-236">/PUBLISHING_WEBSITE_NAME=”Microsoft AppV Publishing Service”</span></span></p>
    <p><span data-ttu-id="c3d8d-237">/PUBLISHING_WEBSITE_PORT = "8081"</span><span class="sxs-lookup"><span data-stu-id="c3d8d-237">/PUBLISHING_WEBSITE_PORT=”8081”</span></span></p></td>
    </tr>
    </tbody>
    </table>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="c3d8d-238">Pour installer le serveur de création de rapports et la base de données de création de rapports sur un ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-238">To Install the Reporting server and Reporting database on a local machine.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c3d8d-239">Pour utiliser l’instance par défaut de Microsoft SQL Server, utilisez les paramètres suivants:</span><span class="sxs-lookup"><span data-stu-id="c3d8d-239">To use the default instance of Microsoft SQL Server, use the following parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="c3d8d-240">/REPORTING _SERVER</span><span class="sxs-lookup"><span data-stu-id="c3d8d-240">/REPORTING _SERVER</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-241">/REPORTING _WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="c3d8d-241">/REPORTING _WEBSITE_NAME</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-242">/REPORTING _WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="c3d8d-242">/REPORTING _WEBSITE_PORT</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-243">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="c3d8d-243">/DB_PREDEPLOY_REPORTING</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-244">/REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="c3d8d-244">/REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-245">/REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="c3d8d-245">/REPORTING _DB_NAME</span></span></p></li>
    </ul>
    <p><span data-ttu-id="c3d8d-246">Pour utiliser une instance personnalisée de Microsoft SQL Server, utilisez les paramètres suivants:</span><span class="sxs-lookup"><span data-stu-id="c3d8d-246">To use a custom instance of Microsoft SQL Server, use these parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="c3d8d-247">/REPORTING _SERVER</span><span class="sxs-lookup"><span data-stu-id="c3d8d-247">/REPORTING _SERVER</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-248">/REPORTING _ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="c3d8d-248">/REPORTING _ADMINACCOUNT</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-249">/REPORTING _WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="c3d8d-249">/REPORTING _WEBSITE_NAME</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-250">/REPORTING _WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="c3d8d-250">/REPORTING _WEBSITE_PORT</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-251">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="c3d8d-251">/DB_PREDEPLOY_REPORTING</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-252">/REPORTING _DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="c3d8d-252">/REPORTING _DB_CUSTOM_SQLINSTANCE</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-253">/REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="c3d8d-253">/REPORTING _DB_NAME</span></span></p></li>
    </ul>
    <p><span data-ttu-id="c3d8d-254">Utilisation d’une instance personnalisée de Microsoft SQL Server par exemple:</span><span class="sxs-lookup"><span data-stu-id="c3d8d-254">Using a custom instance of Microsoft SQL Server example:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="c3d8d-255">/appv_server_setup.exe/QUIET</span><span class="sxs-lookup"><span data-stu-id="c3d8d-255">/appv_server_setup.exe /QUIET</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-256">/REPORTING_SERVER</span><span class="sxs-lookup"><span data-stu-id="c3d8d-256">/REPORTING_SERVER</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-257">/REPORTING_WEBSITE_NAME = «service de rapport Microsoft AppV»</span><span class="sxs-lookup"><span data-stu-id="c3d8d-257">/REPORTING_WEBSITE_NAME=”Microsoft AppV Reporting Service”</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-258">/REPORTING_WEBSITE_PORT = "8082"</span><span class="sxs-lookup"><span data-stu-id="c3d8d-258">/REPORTING_WEBSITE_PORT=”8082”</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-259">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="c3d8d-259">/DB_PREDEPLOY_REPORTING</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-260">/REPORTING_DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</span><span class="sxs-lookup"><span data-stu-id="c3d8d-260">/REPORTING_DB_CUSTOM_SQLINSTANCE=”SqlInstanceName”</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-261">/REPORTING_DB_NAME = "AppVReporting"</span><span class="sxs-lookup"><span data-stu-id="c3d8d-261">/REPORTING_DB_NAME=”AppVReporting”</span></span></p></li>
    </ul></td>
    </tr>
    </tbody>
    </table>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="c3d8d-262">Pour installer le serveur de création de rapports et à l’aide d’une base de données de création de rapports existante sur un ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-262">To Install the Reporting server and using an existing Reporting database on a local machine.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c3d8d-263">Pour utiliser l’instance par défaut de Microsoft SQL Server, utilisez les paramètres suivants:</span><span class="sxs-lookup"><span data-stu-id="c3d8d-263">To use the default instance of Microsoft SQL Server, use the following parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="c3d8d-264">/REPORTING _SERVER</span><span class="sxs-lookup"><span data-stu-id="c3d8d-264">/REPORTING _SERVER</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-265">/REPORTING _WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="c3d8d-265">/REPORTING _WEBSITE_NAME</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-266">/REPORTING _WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="c3d8d-266">/REPORTING _WEBSITE_PORT</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-267">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="c3d8d-267">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-268">/EXISTING_REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="c3d8d-268">/EXISTING_REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-269">/EXISTING_REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="c3d8d-269">/EXISTING_REPORTING _DB_NAME</span></span></p></li>
    </ul>
    <p><span data-ttu-id="c3d8d-270">Pour utiliser une instance personnalisée de Microsoft SQL Server, utilisez les paramètres suivants:</span><span class="sxs-lookup"><span data-stu-id="c3d8d-270">To use a custom instance of Microsoft SQL Server, use these parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="c3d8d-271">/REPORTING _SERVER</span><span class="sxs-lookup"><span data-stu-id="c3d8d-271">/REPORTING _SERVER</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-272">/REPORTING _ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="c3d8d-272">/REPORTING _ADMINACCOUNT</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-273">/REPORTING _WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="c3d8d-273">/REPORTING _WEBSITE_NAME</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-274">/REPORTING _WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="c3d8d-274">/REPORTING _WEBSITE_PORT</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-275">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="c3d8d-275">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-276">/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="c3d8d-276">/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-277">/EXISTING_REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="c3d8d-277">/EXISTING_REPORTING _DB_NAME</span></span></p></li>
    </ul>
    <p><span data-ttu-id="c3d8d-278">Utilisation d’une instance personnalisée de Microsoft SQL Server par exemple:</span><span class="sxs-lookup"><span data-stu-id="c3d8d-278">Using a custom instance of Microsoft SQL Server example:</span></span></p>
    <p><span data-ttu-id="c3d8d-279">/appv_server_setup.exe/QUIET</span><span class="sxs-lookup"><span data-stu-id="c3d8d-279">/appv_server_setup.exe /QUIET</span></span></p>
    <p><span data-ttu-id="c3d8d-280">/REPORTING_SERVER</span><span class="sxs-lookup"><span data-stu-id="c3d8d-280">/REPORTING_SERVER</span></span></p>
    <p><span data-ttu-id="c3d8d-281">/REPORTING_WEBSITE_NAME = «service de rapport Microsoft AppV»</span><span class="sxs-lookup"><span data-stu-id="c3d8d-281">/REPORTING_WEBSITE_NAME=”Microsoft AppV Reporting Service”</span></span></p>
    <p><span data-ttu-id="c3d8d-282">/REPORTING_WEBSITE_PORT = "8082"</span><span class="sxs-lookup"><span data-stu-id="c3d8d-282">/REPORTING_WEBSITE_PORT=”8082”</span></span></p>
    <p><span data-ttu-id="c3d8d-283">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="c3d8d-283">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span></span></p>
    <p><span data-ttu-id="c3d8d-284">/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</span><span class="sxs-lookup"><span data-stu-id="c3d8d-284">/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE=”SqlInstanceName”</span></span></p>
    <p><span data-ttu-id="c3d8d-285">/EXITING_REPORTING_DB_NAME = "AppVReporting"</span><span class="sxs-lookup"><span data-stu-id="c3d8d-285">/EXITING_REPORTING_DB_NAME=”AppVReporting”</span></span></p></td>
    </tr>
    </tbody>
    </table>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="c3d8d-286">Pour installer le serveur de création de rapports à l’aide d’une base de données de création de rapports existante sur un ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-286">To Install the Reporting server using an existing Reporting database on a remote machine.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c3d8d-287">Pour utiliser l’instance par défaut de Microsoft SQL Server, utilisez les paramètres suivants:</span><span class="sxs-lookup"><span data-stu-id="c3d8d-287">To use the default instance of Microsoft SQL Server, use the following parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="c3d8d-288">/REPORTING _SERVER</span><span class="sxs-lookup"><span data-stu-id="c3d8d-288">/REPORTING _SERVER</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-289">/REPORTING _WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="c3d8d-289">/REPORTING _WEBSITE_NAME</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-290">/REPORTING _WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="c3d8d-290">/REPORTING _WEBSITE_PORT</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-291">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="c3d8d-291">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-292">/EXISTING_REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="c3d8d-292">/EXISTING_REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-293">/EXISTING_REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="c3d8d-293">/EXISTING_REPORTING _DB_NAME</span></span></p></li>
    </ul>
    <p><span data-ttu-id="c3d8d-294">Pour utiliser une instance personnalisée de Microsoft SQL Server, utilisez les paramètres suivants:</span><span class="sxs-lookup"><span data-stu-id="c3d8d-294">To use a custom instance of Microsoft SQL Server, use these parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="c3d8d-295">/REPORTING _SERVER</span><span class="sxs-lookup"><span data-stu-id="c3d8d-295">/REPORTING _SERVER</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-296">/REPORTING _ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="c3d8d-296">/REPORTING _ADMINACCOUNT</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-297">/REPORTING _WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="c3d8d-297">/REPORTING _WEBSITE_NAME</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-298">/REPORTING _WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="c3d8d-298">/REPORTING _WEBSITE_PORT</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-299">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="c3d8d-299">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-300">/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="c3d8d-300">/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-301">/EXISTING_REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="c3d8d-301">/EXISTING_REPORTING _DB_NAME</span></span></p></li>
    </ul>
    <p><span data-ttu-id="c3d8d-302">Utilisation d’une instance personnalisée de Microsoft SQL Server par exemple:</span><span class="sxs-lookup"><span data-stu-id="c3d8d-302">Using a custom instance of Microsoft SQL Server example:</span></span></p>
    <p><span data-ttu-id="c3d8d-303">/appv_server_setup.exe/QUIET</span><span class="sxs-lookup"><span data-stu-id="c3d8d-303">/appv_server_setup.exe /QUIET</span></span></p>
    <p><span data-ttu-id="c3d8d-304">/REPORTING_SERVER</span><span class="sxs-lookup"><span data-stu-id="c3d8d-304">/REPORTING_SERVER</span></span></p>
    <p><span data-ttu-id="c3d8d-305">/REPORTING_WEBSITE_NAME = «service de rapport Microsoft AppV»</span><span class="sxs-lookup"><span data-stu-id="c3d8d-305">/REPORTING_WEBSITE_NAME=”Microsoft AppV Reporting Service”</span></span></p>
    <p><span data-ttu-id="c3d8d-306">/REPORTING_WEBSITE_PORT = "8082"</span><span class="sxs-lookup"><span data-stu-id="c3d8d-306">/REPORTING_WEBSITE_PORT=”8082”</span></span></p>
    <p><span data-ttu-id="c3d8d-307">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME = "SqlServerMachine. nom_domaine"</span><span class="sxs-lookup"><span data-stu-id="c3d8d-307">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME=”SqlServerMachine.DomainName”</span></span></p>
    <p><span data-ttu-id="c3d8d-308">/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</span><span class="sxs-lookup"><span data-stu-id="c3d8d-308">/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE=”SqlInstanceName”</span></span></p>
    <p><span data-ttu-id="c3d8d-309">/EXITING_REPORTING_DB_NAME = "AppVReporting"</span><span class="sxs-lookup"><span data-stu-id="c3d8d-309">/EXITING_REPORTING_DB_NAME=”AppVReporting”</span></span></p></td>
    </tr>
    </tbody>
    </table>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="c3d8d-310">Pour installer la base de données de création de rapports sur le même ordinateur que le serveur de rapports.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-310">To install the Reporting database on the same computer as the Reporting server.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c3d8d-311">Pour utiliser l’instance par défaut de Microsoft SQL Server, utilisez les paramètres suivants:</span><span class="sxs-lookup"><span data-stu-id="c3d8d-311">To use the default instance of Microsoft SQL Server, use the following parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="c3d8d-312">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="c3d8d-312">/DB_PREDEPLOY_REPORTING</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-313">/REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="c3d8d-313">/REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-314">/REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="c3d8d-314">/REPORTING _DB_NAME</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-315">/REPORTING_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="c3d8d-315">/REPORTING_SERVER_MACHINE_USE_LOCAL</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-316">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="c3d8d-316">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></li>
    </ul>
    <p><span data-ttu-id="c3d8d-317">Pour utiliser une instance personnalisée de Microsoft SQL Server, utilisez les paramètres suivants:</span><span class="sxs-lookup"><span data-stu-id="c3d8d-317">To use a custom instance of Microsoft SQL Server, use these parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="c3d8d-318">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="c3d8d-318">/DB_PREDEPLOY_REPORTING</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-319">/REPORTING _DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="c3d8d-319">/REPORTING _DB_CUSTOM_SQLINSTANCE</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-320">/REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="c3d8d-320">/REPORTING _DB_NAME</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-321">/REPORTING_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="c3d8d-321">/REPORTING_SERVER_MACHINE_USE_LOCAL</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-322">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="c3d8d-322">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></li>
    </ul>
    <p><span data-ttu-id="c3d8d-323">Utilisation d’une instance personnalisée de Microsoft SQL Server par exemple:</span><span class="sxs-lookup"><span data-stu-id="c3d8d-323">Using a custom instance of Microsoft SQL Server example:</span></span></p>
    <p><span data-ttu-id="c3d8d-324">/appv_server_setup.exe/QUIET</span><span class="sxs-lookup"><span data-stu-id="c3d8d-324">/appv_server_setup.exe /QUIET</span></span></p>
    <p><span data-ttu-id="c3d8d-325">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="c3d8d-325">/DB_PREDEPLOY_REPORTING</span></span></p>
    <p><span data-ttu-id="c3d8d-326">/REPORTING_DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</span><span class="sxs-lookup"><span data-stu-id="c3d8d-326">/REPORTING_DB_CUSTOM_SQLINSTANCE=”SqlInstanceName”</span></span></p>
    <p><span data-ttu-id="c3d8d-327">/REPORTING_DB_NAME = "AppVReporting"</span><span class="sxs-lookup"><span data-stu-id="c3d8d-327">/REPORTING_DB_NAME=”AppVReporting”</span></span></p>
    <p><span data-ttu-id="c3d8d-328">/REPORTING_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="c3d8d-328">/REPORTING_SERVER_MACHINE_USE_LOCAL</span></span></p>
    <p><span data-ttu-id="c3d8d-329">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT = "Domain\InstallAdminAccount"</span><span class="sxs-lookup"><span data-stu-id="c3d8d-329">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT=”Domain\InstallAdminAccount”</span></span></p></td>
    </tr>
    </tbody>
    </table>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="c3d8d-330">Pour installer la base de données de création de rapports sur un autre ordinateur que le serveur de rapports.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-330">To install the Reporting database on a different computer than the Reporting server.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c3d8d-331">Pour utiliser l’instance par défaut de Microsoft SQL Server, utilisez les paramètres suivants:</span><span class="sxs-lookup"><span data-stu-id="c3d8d-331">To use the default instance of Microsoft SQL Server, use the following parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="c3d8d-332">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="c3d8d-332">/DB_PREDEPLOY_REPORTING</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-333">/REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="c3d8d-333">/REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-334">/REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="c3d8d-334">/REPORTING _DB_NAME</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-335">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="c3d8d-335">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-336">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="c3d8d-336">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></li>
    </ul>
    <p><span data-ttu-id="c3d8d-337">Pour utiliser une instance personnalisée de Microsoft SQL Server, utilisez les paramètres suivants:</span><span class="sxs-lookup"><span data-stu-id="c3d8d-337">To use a custom instance of Microsoft SQL Server, use these parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="c3d8d-338">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="c3d8d-338">/DB_PREDEPLOY_REPORTING</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-339">/REPORTING _DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="c3d8d-339">/REPORTING _DB_CUSTOM_SQLINSTANCE</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-340">/REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="c3d8d-340">/REPORTING _DB_NAME</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-341">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="c3d8d-341">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span></span></p></li>
    <li><p><span data-ttu-id="c3d8d-342">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="c3d8d-342">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></li>
    </ul>
    <p><span data-ttu-id="c3d8d-343">Utilisation d’une instance personnalisée de Microsoft SQL Server par exemple:</span><span class="sxs-lookup"><span data-stu-id="c3d8d-343">Using a custom instance of Microsoft SQL Server example:</span></span></p>
    <p><span data-ttu-id="c3d8d-344">/appv_server_setup.exe/QUIET</span><span class="sxs-lookup"><span data-stu-id="c3d8d-344">/appv_server_setup.exe /QUIET</span></span></p>
    <p><span data-ttu-id="c3d8d-345">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="c3d8d-345">/DB_PREDEPLOY_REPORTING</span></span></p>
    <p><span data-ttu-id="c3d8d-346">/REPORTING_DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</span><span class="sxs-lookup"><span data-stu-id="c3d8d-346">/REPORTING_DB_CUSTOM_SQLINSTANCE=”SqlInstanceName”</span></span></p>
    <p><span data-ttu-id="c3d8d-347">/REPORTING_DB_NAME = "AppVReporting"</span><span class="sxs-lookup"><span data-stu-id="c3d8d-347">/REPORTING_DB_NAME=”AppVReporting”</span></span></p>
    <p><span data-ttu-id="c3d8d-348">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT = "Domain\MachineAccount"</span><span class="sxs-lookup"><span data-stu-id="c3d8d-348">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT=”Domain\MachineAccount”</span></span></p>
    <p><span data-ttu-id="c3d8d-349">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT = "Domain\InstallAdminAccount"</span><span class="sxs-lookup"><span data-stu-id="c3d8d-349">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT=”Domain\InstallAdminAccount”</span></span></p></td>
    </tr>
    </tbody>
    </table>

## <span data-ttu-id="c3d8d-350">Définitions des paramètres</span><span class="sxs-lookup"><span data-stu-id="c3d8d-350">Parameter Definitions</span></span>

### <span data-ttu-id="c3d8d-351">Paramètres généraux</span><span class="sxs-lookup"><span data-stu-id="c3d8d-351">General Parameters</span></span>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="c3d8d-352">Paramètre</span><span class="sxs-lookup"><span data-stu-id="c3d8d-352">Parameter</span></span></th>
    <th align="left"><span data-ttu-id="c3d8d-353">Informations</span><span class="sxs-lookup"><span data-stu-id="c3d8d-353">Information</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="c3d8d-354">/QUIET</span><span class="sxs-lookup"><span data-stu-id="c3d8d-354">/QUIET</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c3d8d-355">Spécifie une installation silencieuse.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-355">Specifies silent install.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="c3d8d-356">/UNINSTALL</span><span class="sxs-lookup"><span data-stu-id="c3d8d-356">/UNINSTALL</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c3d8d-357">Spécifie une désinstallation.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-357">Specifies an uninstall.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="c3d8d-358">/LAYOUT</span><span class="sxs-lookup"><span data-stu-id="c3d8d-358">/LAYOUT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c3d8d-359">Spécifie l’action de disposition.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-359">Specifies layout action.</span></span> <span data-ttu-id="c3d8d-360">Le MSIs et les fichiers de script sont extraits dans un dossier sans réellement installer le produit.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-360">This extracts the MSIs and script files to a folder without actually installing the product.</span></span> <span data-ttu-id="c3d8d-361">Aucune valeur n’est attendue.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-361">No value is expected.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="c3d8d-362">/LAYOUTDIR</span><span class="sxs-lookup"><span data-stu-id="c3d8d-362">/LAYOUTDIR</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c3d8d-363">Spécifie le répertoire de disposition.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-363">Specifies the layout directory.</span></span> <span data-ttu-id="c3d8d-364">Prend une chaîne.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-364">Takes a string.</span></span> <span data-ttu-id="c3d8d-365">Par exemple,/LAYOUTDIR = «serveur de virtualisation C:\Application»</span><span class="sxs-lookup"><span data-stu-id="c3d8d-365">For example, /LAYOUTDIR=”C:\Application Virtualization Server”</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="c3d8d-366">/INSTALLDIR</span><span class="sxs-lookup"><span data-stu-id="c3d8d-366">/INSTALLDIR</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c3d8d-367">Spécifie le répertoire d’installation.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-367">Specifies the installation directory.</span></span> <span data-ttu-id="c3d8d-368">Prend une chaîne.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-368">Takes a string.</span></span> <span data-ttu-id="c3d8d-369">Par exemple,</span><span class="sxs-lookup"><span data-stu-id="c3d8d-369">E.g.</span></span> <span data-ttu-id="c3d8d-370">/INSTALLDIR = "C:\Program Files\Application Virtualization\Server"</span><span class="sxs-lookup"><span data-stu-id="c3d8d-370">/INSTALLDIR=”C:\Program Files\Application Virtualization\Server”</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="c3d8d-371">/MUOPTIN</span><span class="sxs-lookup"><span data-stu-id="c3d8d-371">/MUOPTIN</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c3d8d-372">Active Microsoft Update.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-372">Enables Microsoft Update.</span></span> <span data-ttu-id="c3d8d-373">Aucune valeur n’est attendue</span><span class="sxs-lookup"><span data-stu-id="c3d8d-373">No value is expected</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="c3d8d-374">/ACCEPTEULA</span><span class="sxs-lookup"><span data-stu-id="c3d8d-374">/ACCEPTEULA</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c3d8d-375">Accepter le contrat de licence.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-375">Accepts the license agreement.</span></span> <span data-ttu-id="c3d8d-376">Ce type de fichier est requis pour une installation sans assistance.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-376">This is required for an unattended installation.</span></span> <span data-ttu-id="c3d8d-377">Exemple d’utilisation: <strong> /AcceptEULA </strong> ou <strong> /ACCEPTEULA = 1 </strong> .</span><span class="sxs-lookup"><span data-stu-id="c3d8d-377">Example usage: <strong>/ACCEPTEULA</strong> or <strong>/ACCEPTEULA=1</strong>.</span></span></p></td>
    </tr>
    </tbody>
    </table>

### <span data-ttu-id="c3d8d-378">Paramètres d’installation du serveur de gestion</span><span class="sxs-lookup"><span data-stu-id="c3d8d-378">Management Server Installation Parameters</span></span>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="c3d8d-379">Paramètre</span><span class="sxs-lookup"><span data-stu-id="c3d8d-379">Parameter</span></span></th>
    <th align="left"><span data-ttu-id="c3d8d-380">Informations</span><span class="sxs-lookup"><span data-stu-id="c3d8d-380">Information</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="c3d8d-381">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="c3d8d-381">/MANAGEMENT_SERVER</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c3d8d-382">Spécifie que le serveur de gestion sera installé.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-382">Specifies that the management server will be installed.</span></span> <span data-ttu-id="c3d8d-383">Aucune valeur n’est attendue</span><span class="sxs-lookup"><span data-stu-id="c3d8d-383">No value is expected</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="c3d8d-384">/MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="c3d8d-384">/MANAGEMENT_ADMINACCOUNT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c3d8d-385">Spécifie le compte qui sera accordé aux administrateurs pour l’accès au serveur de gestion ce compte peut être un compte d’utilisateur individuel ou un groupe.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-385">Specifies the account that will be allowed to Administrator access to the management server This account can be an individual user account or a group.</span></span> <span data-ttu-id="c3d8d-386">Exemple d’utilisation: <strong> /MANAGEMENT_ADMINACCOUNT = «mydomain\admin» </strong> .</span><span class="sxs-lookup"><span data-stu-id="c3d8d-386">Example usage: <strong>/MANAGEMENT_ADMINACCOUNT=”mydomain\admin”</strong>.</span></span> <span data-ttu-id="c3d8d-387">Si <strong> /MANAGEMENT_SERVER </strong> n’est pas spécifié, la valeur est ignorée.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-387">If <strong>/MANAGEMENT_SERVER</strong> is not specified, this will be ignored.</span></span> <span data-ttu-id="c3d8d-388">Spécifie le compte à utiliser pour l’accès administrateur au serveur de gestion.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-388">Specifies the account that will be allowed to Administrator access to the management server.</span></span> <span data-ttu-id="c3d8d-389">Il peut s’agir d’un compte d’utilisateur ou d’un groupe.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-389">This can be a user account or a group.</span></span> <span data-ttu-id="c3d8d-390">Par exemple, <strong> /MANAGEMENT_ADMINACCOUNT = &quot; mydomain\admin &quot; </strong> .</span><span class="sxs-lookup"><span data-stu-id="c3d8d-390">For example, <strong>/MANAGEMENT_ADMINACCOUNT=&quot;mydomain\admin&quot;</strong>.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="c3d8d-391">/MANAGEMENT_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="c3d8d-391">/MANAGEMENT_WEBSITE_NAME</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c3d8d-392">Spécifie le nom du site Web qui sera créé pour le service de gestion.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-392">Specifies name of the website that will be created for the management service.</span></span> <span data-ttu-id="c3d8d-393">Par exemple,/MANAGEMENT_WEBSITE_NAME = "Microsoft App-V Management Service"</span><span class="sxs-lookup"><span data-stu-id="c3d8d-393">For example, /MANAGEMENT_WEBSITE_NAME=”Microsoft App-V Management Service”</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="c3d8d-394">MANAGEMENT_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="c3d8d-394">MANAGEMENT_WEBSITE_PORT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c3d8d-395">Spécifie le numéro de port utilisé par le service de gestion.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-395">Specifies the port number that will be used by the management service will use.</span></span> <span data-ttu-id="c3d8d-396">Par exemple,/MANAGEMENT_WEBSITE_PORT = 82.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-396">For example, /MANAGEMENT_WEBSITE_PORT=82.</span></span></p></td>
    </tr>
    </tbody>
    </table>

### <span data-ttu-id="c3d8d-397">Paramètres de la base de données du serveur de gestion</span><span class="sxs-lookup"><span data-stu-id="c3d8d-397">Parameters for the Management Server Database</span></span>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="c3d8d-398">Paramètre</span><span class="sxs-lookup"><span data-stu-id="c3d8d-398">Parameter</span></span></th>
    <th align="left"><span data-ttu-id="c3d8d-399">Informations</span><span class="sxs-lookup"><span data-stu-id="c3d8d-399">Information</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="c3d8d-400">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="c3d8d-400">/DB_PREDEPLOY_MANAGEMENT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c3d8d-401">Spécifie que la base de données de gestion sera installée.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-401">Specifies that the management database will be installed.</span></span> <span data-ttu-id="c3d8d-402">Vous devez disposer des autorisations de base de données suffisantes pour effectuer cette installation.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-402">You must have sufficient database permissions to complete this installation.</span></span> <span data-ttu-id="c3d8d-403">Aucune valeur n’est attendue</span><span class="sxs-lookup"><span data-stu-id="c3d8d-403">No value is expected</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="c3d8d-404">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="c3d8d-404">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c3d8d-405">Indique que l’instance SQL par défaut doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-405">Indicates that the default SQL instance should be used.</span></span> <span data-ttu-id="c3d8d-406">Aucune valeur n’est attendue.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-406">No value is expected.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="c3d8d-407">/MANAGEMENT_DB_ CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="c3d8d-407">/MANAGEMENT_DB_ CUSTOM_SQLINSTANCE</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c3d8d-408">Spécifie le nom de l’instance SQL personnalisée à utiliser pour créer une nouvelle base de données.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-408">Specifies the name of the custom SQL instance that should be used to create a new database.</span></span> <span data-ttu-id="c3d8d-409">Exemple d’utilisation: <strong> /MANAGEMENT_DB_ CUSTOM_SQLINSTANCE = "MYSQLSERVER" </strong> .</span><span class="sxs-lookup"><span data-stu-id="c3d8d-409">Example usage: <strong>/MANAGEMENT_DB_ CUSTOM_SQLINSTANCE=”MYSQLSERVER”</strong>.</span></span> <span data-ttu-id="c3d8d-410">Si/DB_PREDEPLOY_MANAGEMENT n’est pas spécifié, la valeur est ignorée.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-410">If /DB_PREDEPLOY_MANAGEMENT is not specified, this will be ignored.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="c3d8d-411">/MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="c3d8d-411">/MANAGEMENT_DB_NAME</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c3d8d-412">Spécifie le nom de la nouvelle base de données de gestion à créer.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-412">Specifies the name of the new management database that should be created.</span></span> <span data-ttu-id="c3d8d-413">Exemple d’utilisation: <strong> /MANAGEMENT_DB_NAME = «AppVMgmtDB» </strong> .</span><span class="sxs-lookup"><span data-stu-id="c3d8d-413">Example usage: <strong>/MANAGEMENT_DB_NAME=”AppVMgmtDB”</strong>.</span></span> <span data-ttu-id="c3d8d-414">Si/DB_PREDEPLOY_MANAGEMENT n’est pas spécifié, la valeur est ignorée.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-414">If /DB_PREDEPLOY_MANAGEMENT is not specified, this will be ignored.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="c3d8d-415">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="c3d8d-415">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c3d8d-416">Indique si le serveur de gestion qui accède à la base de données est installé sur le serveur local.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-416">Indicates if the management server that will be accessing the database is installed on the local server.</span></span> <span data-ttu-id="c3d8d-417">Basculez le paramètre de sorte qu’aucune valeur ne soit attendue.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-417">Switch parameter so no value is expected.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="c3d8d-418">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="c3d8d-418">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c3d8d-419">Spécifie le compte d’ordinateur de l’ordinateur distant sur lequel le serveur de gestion sera installé.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-419">Specifies the machine account of the remote machine that the management server will be installed on.</span></span> <span data-ttu-id="c3d8d-420">Exemple d’utilisation: <strong> /MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT = «domain\computername»</span><span class="sxs-lookup"><span data-stu-id="c3d8d-420">Example usage: <strong>/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT=”domain\computername”</span></span></strong></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="c3d8d-421">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="c3d8d-421">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c3d8d-422">Indique le compte d’administrateur qui sera utilisé pour installer le serveur de gestion.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-422">Indicates the Administrator account that will be used to install the management server.</span></span> <span data-ttu-id="c3d8d-423">Exemple d’utilisation: <strong> /MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT = «DOMAIN\alias»</span><span class="sxs-lookup"><span data-stu-id="c3d8d-423">Example usage: <strong>/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT =”domain\alias”</span></span></strong></p></td>
    </tr>
    </tbody>
    </table>

### <span data-ttu-id="c3d8d-424">Paramètres pour l’installation d’un serveur de publication</span><span class="sxs-lookup"><span data-stu-id="c3d8d-424">Parameters for Installing Publishing Server</span></span>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="c3d8d-425">Paramètre</span><span class="sxs-lookup"><span data-stu-id="c3d8d-425">Parameter</span></span></th>
    <th align="left"><span data-ttu-id="c3d8d-426">Informations</span><span class="sxs-lookup"><span data-stu-id="c3d8d-426">Information</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="c3d8d-427">/PUBLISHING_SERVER</span><span class="sxs-lookup"><span data-stu-id="c3d8d-427">/PUBLISHING_SERVER</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c3d8d-428">Spécifie que le serveur de publication sera installé.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-428">Specifies that the Publishing Server will be installed.</span></span> <span data-ttu-id="c3d8d-429">Aucune valeur n’est attendue</span><span class="sxs-lookup"><span data-stu-id="c3d8d-429">No value is expected</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="c3d8d-430">/PUBLISHING_MGT_SERVER</span><span class="sxs-lookup"><span data-stu-id="c3d8d-430">/PUBLISHING_MGT_SERVER</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c3d8d-431">Spécifie l’URL du service de gestion auquel est connecté le serveur de publication.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-431">Specifies the URL to Management Service the Publishing server will connect to.</span></span> <span data-ttu-id="c3d8d-432">Exemple d’utilisation: <strong> http:// &lt; Management Server name &gt; : numéro de port du serveur de &lt; gestion &gt; </strong> .</span><span class="sxs-lookup"><span data-stu-id="c3d8d-432">Example usage: <strong>http://&lt;management server name&gt;:&lt;Management server port number&gt;</strong>.</span></span> <span data-ttu-id="c3d8d-433">Si/PUBLISHING_SERVER n’est pas utilisé, ce paramètre est ignoré.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-433">If /PUBLISHING_SERVER is not used, this parameter will be ignored</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="c3d8d-434">/PUBLISHING_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="c3d8d-434">/PUBLISHING_WEBSITE_NAME</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c3d8d-435">Spécifie le nom du site Web qui sera créé pour le service de publication.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-435">Specifies name of the website that will be created for the publishing service.</span></span> <span data-ttu-id="c3d8d-436">Par exemple,/PUBLISHING_WEBSITE_NAME = "Microsoft App-V publication service"</span><span class="sxs-lookup"><span data-stu-id="c3d8d-436">For example, /PUBLISHING_WEBSITE_NAME=”Microsoft App-V Publishing Service”</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="c3d8d-437">/PUBLISHING_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="c3d8d-437">/PUBLISHING_WEBSITE_PORT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c3d8d-438">Spécifie le numéro de port utilisé par le service de publication.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-438">Specifies the port number used by the publishing service.</span></span> <span data-ttu-id="c3d8d-439">Par exemple,/PUBLISHING_WEBSITE_PORT = 83</span><span class="sxs-lookup"><span data-stu-id="c3d8d-439">For example, /PUBLISHING_WEBSITE_PORT=83</span></span></p></td>
    </tr>
    </tbody>
    </table>

### <span data-ttu-id="c3d8d-440">Paramètres pour le serveur de création de rapports</span><span class="sxs-lookup"><span data-stu-id="c3d8d-440">Parameters for Reporting Server</span></span>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="c3d8d-441">Paramètre</span><span class="sxs-lookup"><span data-stu-id="c3d8d-441">Parameter</span></span></th>
    <th align="left"><span data-ttu-id="c3d8d-442">Informations</span><span class="sxs-lookup"><span data-stu-id="c3d8d-442">Information</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="c3d8d-443">/REPORTING_SERVER</span><span class="sxs-lookup"><span data-stu-id="c3d8d-443">/REPORTING_SERVER</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c3d8d-444">Spécifie que le serveur de rapports sera installé.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-444">Specifies that the Reporting Server will be installed.</span></span> <span data-ttu-id="c3d8d-445">Aucune valeur n’est attendue</span><span class="sxs-lookup"><span data-stu-id="c3d8d-445">No value is expected</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="c3d8d-446">/REPORTING_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="c3d8d-446">/REPORTING_WEBSITE_NAME</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c3d8d-447">Spécifie le nom du site Web qui sera créé pour le service de création de rapports.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-447">Specifies name of the website that will be created for the Reporting Service.</span></span> <span data-ttu-id="c3d8d-448">Par exemple,</span><span class="sxs-lookup"><span data-stu-id="c3d8d-448">E.g.</span></span> <span data-ttu-id="c3d8d-449">/REPORTING_WEBSITE_NAME = &quot; Microsoft App-V ReportingService&quot;</span><span class="sxs-lookup"><span data-stu-id="c3d8d-449">/REPORTING_WEBSITE_NAME=&quot;Microsoft App-V ReportingService&quot;</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="c3d8d-450">/REPORTING_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="c3d8d-450">/REPORTING_WEBSITE_PORT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c3d8d-451">Spécifie le numéro de port que le service de création de rapports utilisera.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-451">Specifies the port number that the Reporting Service will use.</span></span> <span data-ttu-id="c3d8d-452">Par exemple,</span><span class="sxs-lookup"><span data-stu-id="c3d8d-452">E.g.</span></span> <span data-ttu-id="c3d8d-453">/REPORTING_WEBSITE_PORT = 82</span><span class="sxs-lookup"><span data-stu-id="c3d8d-453">/REPORTING_WEBSITE_PORT=82</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

### <span data-ttu-id="c3d8d-454">Paramètres d’utilisation d’une base de données serveur de création de rapports existante</span><span class="sxs-lookup"><span data-stu-id="c3d8d-454">Parameters for using an Existing Reporting Server Database</span></span>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="c3d8d-455">Paramètre</span><span class="sxs-lookup"><span data-stu-id="c3d8d-455">Parameter</span></span></th>
    <th align="left"><span data-ttu-id="c3d8d-456">Informations</span><span class="sxs-lookup"><span data-stu-id="c3d8d-456">Information</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="c3d8d-457">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="c3d8d-457">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c3d8d-458">Indique que Microsoft SQL Server est installé sur le serveur local.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-458">Indicates that the Microsoft SQL Server is installed on the local server.</span></span> <span data-ttu-id="c3d8d-459">Basculez le paramètre de sorte qu’aucune valeur ne soit attendue.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-459">Switch parameter so no value is expected.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="c3d8d-460">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="c3d8d-460">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c3d8d-461">Spécifie le nom de l’ordinateur distant sur lequel SQL Server est installé.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-461">Specifies the name of the remote computer that SQL Server is installed on.</span></span> <span data-ttu-id="c3d8d-462">Prend une chaîne.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-462">Takes a string.</span></span> <span data-ttu-id="c3d8d-463">Par exemple,</span><span class="sxs-lookup"><span data-stu-id="c3d8d-463">E.g.</span></span> <span data-ttu-id="c3d8d-464">/EXISTING_REPORTING_DB_ REMOTE_SQL_SERVER_NAME = &quot; mycomputer1&quot;</span><span class="sxs-lookup"><span data-stu-id="c3d8d-464">/EXISTING_REPORTING_DB_ REMOTE_SQL_SERVER_NAME=&quot;mycomputer1&quot;</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="c3d8d-465">DB_SQLINSTANCE_USE_DEFAULT EXISTING_ de création de rapports <em></span><span class="sxs-lookup"><span data-stu-id="c3d8d-465">/EXISTING_ REPORTING <em>DB_SQLINSTANCE_USE_DEFAULT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c3d8d-466">Indique que l’instance SQL par défaut doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-466">Indicates that the default SQL instance is to be used.</span></span> <span data-ttu-id="c3d8d-467">Basculez le paramètre de sorte qu’aucune valeur ne soit attendue.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-467">Switch parameter so no value is expected.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="c3d8d-468">/EXISTING </em> REPORTING_DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="c3d8d-468">/EXISTING</em> REPORTING_DB_CUSTOM_SQLINSTANCE</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c3d8d-469">Spécifie le nom de l’instance SQL personnalisée qui doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-469">Specifies the name of the custom SQL instance that should be used.</span></span> <span data-ttu-id="c3d8d-470">Prend une chaîne.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-470">Takes a string.</span></span> <span data-ttu-id="c3d8d-471">Par exemple,</span><span class="sxs-lookup"><span data-stu-id="c3d8d-471">E.g.</span></span> <span data-ttu-id="c3d8d-472">/EXISTING_REPORTING_DB_ CUSTOM_SQLINSTANCE = &quot; MYSQLSERVER&quot;</span><span class="sxs-lookup"><span data-stu-id="c3d8d-472">/EXISTING_REPORTING_DB_ CUSTOM_SQLINSTANCE=&quot;MYSQLSERVER&quot;</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="c3d8d-473">_DB_NAME EXISTING_ DE CRÉATION DE RAPPORTS</span><span class="sxs-lookup"><span data-stu-id="c3d8d-473">/EXISTING_ REPORTING _DB_NAME</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c3d8d-474">Spécifie le nom de la base de données de création de rapports existante à utiliser.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-474">Specifies the name of the existing Reporting database that should be used.</span></span> <span data-ttu-id="c3d8d-475">Prend une chaîne.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-475">Takes a string.</span></span> <span data-ttu-id="c3d8d-476">Par exemple,</span><span class="sxs-lookup"><span data-stu-id="c3d8d-476">E.g.</span></span> <span data-ttu-id="c3d8d-477">/EXISTING_REPORTING_DB_NAME = &quot; AppVReporting&quot;</span><span class="sxs-lookup"><span data-stu-id="c3d8d-477">/EXISTING_REPORTING_DB_NAME=&quot;AppVReporting&quot;</span></span></p></td>
    </tr>
    </tbody>
    </table>

### <span data-ttu-id="c3d8d-478">Paramètres pour l’installation de la base de données serveur de création de rapports</span><span class="sxs-lookup"><span data-stu-id="c3d8d-478">Parameters for installing Reporting Server Database</span></span>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="c3d8d-479">Paramètre</span><span class="sxs-lookup"><span data-stu-id="c3d8d-479">Parameter</span></span></th>
    <th align="left"><span data-ttu-id="c3d8d-480">Informations</span><span class="sxs-lookup"><span data-stu-id="c3d8d-480">Information</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="c3d8d-481">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="c3d8d-481">/DB_PREDEPLOY_REPORTING</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c3d8d-482">Spécifie que la base de données de création de rapports sera installée.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-482">Specifies that the Reporting Database will be installed.</span></span> <span data-ttu-id="c3d8d-483">Des autorisations DBA sont nécessaires pour cette installation.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-483">DBA permissions are required for this installation.</span></span> <span data-ttu-id="c3d8d-484">Aucune valeur n’est attendue</span><span class="sxs-lookup"><span data-stu-id="c3d8d-484">No value is expected</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="c3d8d-485">/REPORTING_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="c3d8d-485">/REPORTING_DB_SQLINSTANCE_USE_DEFAULT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c3d8d-486">Spécifie le nom de l’instance SQL personnalisée qui doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-486">Specifies the name of the custom SQL instance that should be used.</span></span> <span data-ttu-id="c3d8d-487">Prend une chaîne.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-487">Takes a string.</span></span> <span data-ttu-id="c3d8d-488">Par exemple,</span><span class="sxs-lookup"><span data-stu-id="c3d8d-488">E.g.</span></span> <span data-ttu-id="c3d8d-489">/REPORTING_DB_ CUSTOM_SQLINSTANCE = &quot; MYSQLSERVER&quot;</span><span class="sxs-lookup"><span data-stu-id="c3d8d-489">/REPORTING_DB_ CUSTOM_SQLINSTANCE=&quot;MYSQLSERVER&quot;</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="c3d8d-490">/REPORTING_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="c3d8d-490">/REPORTING_DB_NAME</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c3d8d-491">Spécifie le nom de la nouvelle base de données de création de rapports à créer.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-491">Specifies the name of the new Reporting database that should be created.</span></span> <span data-ttu-id="c3d8d-492">Prend une chaîne.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-492">Takes a string.</span></span> <span data-ttu-id="c3d8d-493">Par exemple,</span><span class="sxs-lookup"><span data-stu-id="c3d8d-493">E.g.</span></span> <span data-ttu-id="c3d8d-494">/REPORTING_DB_NAME = &quot; AppVMgmtDB&quot;</span><span class="sxs-lookup"><span data-stu-id="c3d8d-494">/REPORTING_DB_NAME=&quot;AppVMgmtDB&quot;</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="c3d8d-495">/REPORTING_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="c3d8d-495">/REPORTING_SERVER_MACHINE_USE_LOCAL</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c3d8d-496">Indique que le serveur de création de rapports qui accède à la base de données est installé sur le serveur local.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-496">Indicates that the Reporting server that will be accessing the database is installed on the local server.</span></span> <span data-ttu-id="c3d8d-497">Basculez le paramètre de sorte qu’aucune valeur ne soit attendue.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-497">Switch parameter so no value is expected.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="c3d8d-498">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="c3d8d-498">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c3d8d-499">Spécifie le compte d’ordinateur de l’ordinateur distant sur lequel est installé le serveur de rapports.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-499">Specifies the machine account of the remote machine that the Reporting server will be installed on.</span></span> <span data-ttu-id="c3d8d-500">Prend une chaîne.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-500">Takes a string.</span></span> <span data-ttu-id="c3d8d-501">Par exemple,</span><span class="sxs-lookup"><span data-stu-id="c3d8d-501">E.g.</span></span> <span data-ttu-id="c3d8d-502">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT = &quot; domain\computername&quot;</span><span class="sxs-lookup"><span data-stu-id="c3d8d-502">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT = &quot;domain\computername&quot;</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="c3d8d-503">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="c3d8d-503">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c3d8d-504">Indique le compte d’administrateur qui sera utilisé pour installer le serveur de création de rapports App-V.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-504">Indicates the Administrator account that will be used to install the App-V Reporting Server.</span></span> <span data-ttu-id="c3d8d-505">Prend une chaîne.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-505">Takes a string.</span></span> <span data-ttu-id="c3d8d-506">Par exemple,</span><span class="sxs-lookup"><span data-stu-id="c3d8d-506">E.g.</span></span> <span data-ttu-id="c3d8d-507">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT = &quot; DOMAIN\alias&quot;</span><span class="sxs-lookup"><span data-stu-id="c3d8d-507">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT = &quot;domain\alias&quot;</span></span></p></td>
    </tr>
    </tbody>
    </table>

### <span data-ttu-id="c3d8d-508">Paramètres d’utilisation d’une base de données serveur de gestion existante</span><span class="sxs-lookup"><span data-stu-id="c3d8d-508">Parameters for using an existing Management Server Database</span></span>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="c3d8d-509">Paramètre</span><span class="sxs-lookup"><span data-stu-id="c3d8d-509">Parameter</span></span></th>
    <th align="left"><span data-ttu-id="c3d8d-510">Informations</span><span class="sxs-lookup"><span data-stu-id="c3d8d-510">Information</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="c3d8d-511">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="c3d8d-511">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c3d8d-512">Indique que SQL Server est installé sur le serveur local.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-512">Indicates that the SQL Server is installed on the local server.</span></span> <span data-ttu-id="c3d8d-513">Basculez le paramètre de sorte qu’aucune valeur ne soit attendue. Si/DB_PREDEPLOY_MANAGEMENT est spécifiée, la valeur est ignorée.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-513">Switch parameter so no value is expected.If /DB_PREDEPLOY_MANAGEMENT is specified, this will be ignored.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="c3d8d-514">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="c3d8d-514">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c3d8d-515">Spécifie le nom de l’ordinateur distant sur lequel SQL Server est installé.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-515">Specifies the name of the remote computer that SQL Server is installed on.</span></span> <span data-ttu-id="c3d8d-516">Prend une chaîne.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-516">Takes a string.</span></span> <span data-ttu-id="c3d8d-517">Par exemple,</span><span class="sxs-lookup"><span data-stu-id="c3d8d-517">E.g.</span></span> <span data-ttu-id="c3d8d-518">/EXISTING_MANAGEMENT_DB_ REMOTE_SQL_SERVER_NAME = &quot; mycomputer1&quot;</span><span class="sxs-lookup"><span data-stu-id="c3d8d-518">/EXISTING_MANAGEMENT_DB_ REMOTE_SQL_SERVER_NAME=&quot;mycomputer1&quot;</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="c3d8d-519">/EXISTING_ MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="c3d8d-519">/EXISTING_ MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c3d8d-520">Indique que l’instance SQL par défaut doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-520">Indicates that the default SQL instance is to be used.</span></span> <span data-ttu-id="c3d8d-521">Basculez le paramètre de sorte qu’aucune valeur ne soit attendue.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-521">Switch parameter so no value is expected.</span></span> <span data-ttu-id="c3d8d-522">Si/DB_PREDEPLOY_MANAGEMENT est spécifiée, la valeur est ignorée.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-522">If /DB_PREDEPLOY_MANAGEMENT is specified, this will be ignored.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="c3d8d-523">/EXISTING_MANAGEMENT_DB_ CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="c3d8d-523">/EXISTING_MANAGEMENT_DB_ CUSTOM_SQLINSTANCE</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c3d8d-524">Spécifie le nom de l’instance SQL personnalisée qui sera utilisée.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-524">Specifies the name of the custom SQL instance that will be used.</span></span> <span data-ttu-id="c3d8d-525">Exemple d’utilisation <strong> /EXISTING_MANAGEMENT_DB_ CUSTOM_SQLINSTANCE = "AppVManagement" </strong> .</span><span class="sxs-lookup"><span data-stu-id="c3d8d-525">Example usage <strong>/EXISTING_MANAGEMENT_DB_ CUSTOM_SQLINSTANCE=”AppVManagement”</strong>.</span></span> <span data-ttu-id="c3d8d-526">Si/DB_PREDEPLOY_MANAGEMENT est spécifiée, la valeur est ignorée.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-526">If /DB_PREDEPLOY_MANAGEMENT is specified, this will be ignored.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="c3d8d-527">/EXISTING_MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="c3d8d-527">/EXISTING_MANAGEMENT_DB_NAME</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c3d8d-528">Spécifie le nom de la base de données de gestion existante à utiliser.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-528">Specifies the name of the existing management database that should be used.</span></span> <span data-ttu-id="c3d8d-529">Exemple d’utilisation: <strong> /EXISTING_MANAGEMENT_DB_NAME = «AppVMgmtDB» </strong> .</span><span class="sxs-lookup"><span data-stu-id="c3d8d-529">Example usage: <strong>/EXISTING_MANAGEMENT_DB_NAME=”AppVMgmtDB”</strong>.</span></span> <span data-ttu-id="c3d8d-530">Si/DB_PREDEPLOY_MANAGEMENT est spécifiée, la valeur est ignorée.</span><span class="sxs-lookup"><span data-stu-id="c3d8d-530">If /DB_PREDEPLOY_MANAGEMENT is specified, this will be ignored.</span></span></p>
    <p></p>
    <p><strong><span data-ttu-id="c3d8d-531">Vous avez une suggestion pour App-V </strong> ?</span><span class="sxs-lookup"><span data-stu-id="c3d8d-531">Got a suggestion for App-V</strong>?</span></span> <span data-ttu-id="c3d8d-532">Ajoutez ou Votez en fonction de suggestions <a href="http://appv.uservoice.com/forums/280448-microsoft-application-virtualization" data-raw-source="[here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)"> </a> .</span><span class="sxs-lookup"><span data-stu-id="c3d8d-532">Add or vote on suggestions <a href="http://appv.uservoice.com/forums/280448-microsoft-application-virtualization" data-raw-source="[here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)">here</a>.</span></span> <strong><span data-ttu-id="c3d8d-533">Avez-vous une application-V issu </strong> e?</span><span class="sxs-lookup"><span data-stu-id="c3d8d-533">Got an App-V issu</strong>e?</span></span> <span data-ttu-id="c3d8d-534">Utilisez le <a href="https://social.technet.microsoft.com/Forums/home?forum=mdopappv" data-raw-source="[App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv)"> Forum TechNet App-V </a> .</span><span class="sxs-lookup"><span data-stu-id="c3d8d-534">Use the <a href="https://social.technet.microsoft.com/Forums/home?forum=mdopappv" data-raw-source="[App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv)">App-V TechNet Forum</a>.</span></span></p></td>
</tr>
</tbody>
</table>
  

## <span data-ttu-id="c3d8d-535">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c3d8d-535">Related topics</span></span>

[<span data-ttu-id="c3d8d-536">Déploiement du serveur App-V5.0</span><span class="sxs-lookup"><span data-stu-id="c3d8d-536">Deploying the App-V 5.0 Server</span></span>](deploying-the-app-v-50-server.md)

 

 





