---
title: Comment déployer les bases de données App-V à l'aide de scripts SQL
description: Comment déployer les bases de données App-V à l'aide de scripts SQL
author: dansimp
ms.assetid: 23637936-475f-4ca5-adde-76bb27d2372b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 511d1020571eead25af9e9591fe1834a9f97f068
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805484"
---
# <span data-ttu-id="b28d5-103">Comment déployer les bases de données App-V à l'aide de scripts SQL</span><span class="sxs-lookup"><span data-stu-id="b28d5-103">How to Deploy the App-V Databases by Using SQL Scripts</span></span>


<span data-ttu-id="b28d5-104">Pour utiliser les scripts SQL plutôt que le programme d’installation Windows, procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="b28d5-104">Use the following instructions to use SQL scripts, rather than the Windows Installer, to:</span></span>

-   <span data-ttu-id="b28d5-105">Installer les bases de données App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="b28d5-105">Install the App-V 5.0 databases</span></span>

-   <span data-ttu-id="b28d5-106">Mettre à niveau les bases de données 5,0 vers une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="b28d5-106">Upgrade the 5.0 databases to a later version</span></span>

**<span data-ttu-id="b28d5-107">Comment installer les bases de données App-V à l’aide de scripts SQL</span><span class="sxs-lookup"><span data-stu-id="b28d5-107">How to install the App-V databases by using SQL scripts</span></span>**

1. <span data-ttu-id="b28d5-108">Avant d’installer les scripts de base de données, passez en revue les termes du contrat de licence App-V et conservez-en une copie.</span><span class="sxs-lookup"><span data-stu-id="b28d5-108">Before you install the database scripts, review and keep a copy of the App-V license terms.</span></span> <span data-ttu-id="b28d5-109">En exécutant les scripts de base de données, vous acceptez les termes du contrat de licence.</span><span class="sxs-lookup"><span data-stu-id="b28d5-109">By running the database scripts, you are agreeing to the license terms.</span></span> <span data-ttu-id="b28d5-110">Si vous n’acceptez pas le logiciel, vous ne devez pas l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="b28d5-110">If you do not accept them, you should not use this software.</span></span>

2. <span data-ttu-id="b28d5-111">Copiez l' **appv\_server\_setup.exe** du média App-V Release vers un emplacement temporaire.</span><span class="sxs-lookup"><span data-stu-id="b28d5-111">Copy the **appv\_server\_setup.exe** from the App-V release media to a temporary location.</span></span>

3. <span data-ttu-id="b28d5-112">À partir d’une invite de commandes, exécutez **appv\_server\_setup.exe** et spécifiez un emplacement temporaire pour extraire les scripts de la base de données.</span><span class="sxs-lookup"><span data-stu-id="b28d5-112">From a command prompt, run **appv\_server\_setup.exe** and specify a temporary location for extracting the database scripts.</span></span>

   <span data-ttu-id="b28d5-113">Exemple: appv\_server\_setup.exe/layout c:\\ &lt; chemin d’emplacement temporaire&gt;</span><span class="sxs-lookup"><span data-stu-id="b28d5-113">Example: appv\_server\_setup.exe /layout c:\\&lt;temporary location path&gt;</span></span>

4. <span data-ttu-id="b28d5-114">Naviguez jusqu’à l’emplacement temporaire que vous avez créé, ouvrez le dossier **DatabaseScripts** extrait et examinez le fichier Readme.txt approprié pour obtenir des instructions:</span><span class="sxs-lookup"><span data-stu-id="b28d5-114">Browse to the temporary location that you created, open the extracted **DatabaseScripts** folder, and review the appropriate Readme.txt file for instructions:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="b28d5-115">Base de données</span><span class="sxs-lookup"><span data-stu-id="b28d5-115">Database</span></span></th>
   <th align="left"><span data-ttu-id="b28d5-116">Emplacement du fichier Readme.txt à utiliser</span><span class="sxs-lookup"><span data-stu-id="b28d5-116">Location of Readme.txt file to use</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="b28d5-117">Base de données de gestion</span><span class="sxs-lookup"><span data-stu-id="b28d5-117">Management database</span></span></p></td>
   <td align="left"><p><span data-ttu-id="b28d5-118">Sous-dossier ManagementDatabase</span><span class="sxs-lookup"><span data-stu-id="b28d5-118">ManagementDatabase subfolder</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="b28d5-119">Important</span><span class="sxs-lookup"><span data-stu-id="b28d5-119">Important</span></span></strong><br/><p><span data-ttu-id="b28d5-120">Si vous effectuez une mise à niveau vers ou l’installation de la base de données de gestion App-V 5,0 SP3, voir <a href="https://support.microsoft.com/kb/3031340" data-raw-source="[SQL scripts to install or upgrade the App-V 5.0 SP3 Management Server database fail](https://support.microsoft.com/kb/3031340)"> scripts SQL pour installer ou mettre à niveau la base de données App-v 5,0 SP3 Management Server </a> .</span><span class="sxs-lookup"><span data-stu-id="b28d5-120">If you are upgrading to or installing the App-V 5.0 SP3 Management database, see <a href="https://support.microsoft.com/kb/3031340" data-raw-source="[SQL scripts to install or upgrade the App-V 5.0 SP3 Management Server database fail](https://support.microsoft.com/kb/3031340)">SQL scripts to install or upgrade the App-V 5.0 SP3 Management Server database fail</a>.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="b28d5-121">Base de données de création de rapports</span><span class="sxs-lookup"><span data-stu-id="b28d5-121">Reporting database</span></span></p></td>
   <td align="left"><p><span data-ttu-id="b28d5-122">Sous-dossier ReportingDatabase</span><span class="sxs-lookup"><span data-stu-id="b28d5-122">ReportingDatabase subfolder</span></span></p></td>
   </tr>
   </tbody>
   </table>



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## <span data-ttu-id="b28d5-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b28d5-123">Related topics</span></span>


[<span data-ttu-id="b28d5-124">Déploiement du serveur App-V5.0</span><span class="sxs-lookup"><span data-stu-id="b28d5-124">Deploying the App-V 5.0 Server</span></span>](deploying-the-app-v-50-server.md)

[<span data-ttu-id="b28d5-125">Comment déployer le serveur App-V5.0</span><span class="sxs-lookup"><span data-stu-id="b28d5-125">How to Deploy the App-V 5.0 Server</span></span>](how-to-deploy-the-app-v-50-server-50sp3.md)









