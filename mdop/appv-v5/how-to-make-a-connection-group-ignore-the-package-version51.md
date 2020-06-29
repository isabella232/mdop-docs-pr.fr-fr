---
title: Comment faire en sorte qu'un groupe de connexion ignore la version du package
description: Comment faire en sorte qu'un groupe de connexion ignore la version du package
author: dansimp
ms.assetid: db16b095-dbe2-42c7-863d-b0d5d91b2f4c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 026ef1b3a2aa073a684b1fe5da4f79aa1067072d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805347"
---
# <span data-ttu-id="f0950-103">Comment faire en sorte qu'un groupe de connexion ignore la version du package</span><span class="sxs-lookup"><span data-stu-id="f0950-103">How to Make a Connection Group Ignore the Package Version</span></span>


<span data-ttu-id="f0950-104">Microsoft Application Virtualization (App-V) 5,1 vous permet de configurer un groupe de connexion pour utiliser n’importe quelle version d’un package, qui simplifie les mises à jour de package et réduit le nombre de groupes de connexion que vous devez créer.</span><span class="sxs-lookup"><span data-stu-id="f0950-104">Microsoft Application Virtualization (App-V) 5.1 lets you configure a connection group to use any version of a package, which simplifies package upgrades and reduces the number of connection groups you need to create.</span></span>

<span data-ttu-id="f0950-105">Pour mettre à niveau un package dans certaines versions antérieures de App-V, vous devez effectuer plusieurs étapes, notamment la désactivation du groupe de connexion et la modification du fichier de définition XML du groupe de connexion.</span><span class="sxs-lookup"><span data-stu-id="f0950-105">To upgrade a package in some earlier versions of App-V, you had to perform several steps, including disabling the connection group and modifying the connection group’s XML definition file.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f0950-106">Description de la tâche avec App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="f0950-106">Task description with App-V 5.1</span></span></th>
<th align="left"><span data-ttu-id="f0950-107">Exécution d’une tâche avec App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="f0950-107">How to perform the task with App-V 5.1</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f0950-108">Vous pouvez configurer un groupe de connexion pour accepter n’importe quelle version d’un package, qui vous permet de mettre à niveau le package sans avoir à désactiver le groupe de connexion.</span><span class="sxs-lookup"><span data-stu-id="f0950-108">You can configure a connection group to accept any version of a package, which enables you to upgrade the package without having to disable the connection group.</span></span></p>
<p><strong><span data-ttu-id="f0950-109">Fonctionnement de la fonctionnalité:</span><span class="sxs-lookup"><span data-stu-id="f0950-109">How the feature works:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="f0950-110">Si le groupe de connexion a accès à plusieurs versions d’un package, la version la plus récente est utilisée.</span><span class="sxs-lookup"><span data-stu-id="f0950-110">If the connection group has access to multiple versions of a package, the latest version is used.</span></span></p></li>
<li><p><span data-ttu-id="f0950-111">Si le groupe de connexion contient un package facultatif présentant une version incorrecte, le package est ignoré et ne bloque pas la création de l’environnement virtuel du groupe de connexion.</span><span class="sxs-lookup"><span data-stu-id="f0950-111">If the connection group contains an optional package that has an incorrect version, the package is ignored and won’t block the connection group’s virtual environment from being created.</span></span></p></li>
<li><p><span data-ttu-id="f0950-112">Si le groupe de connexion contient un package non facultatif présentant une version incorrecte, l’environnement virtuel du groupe de connexions ne peut pas être créé.</span><span class="sxs-lookup"><span data-stu-id="f0950-112">If the connection group contains a non-optional package that has an incorrect version, the connection group’s virtual environment cannot be created.</span></span></p></li>
</ul></td>
<td align="left"><table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f0950-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="f0950-113">Method</span></span></th>
<th align="left"><span data-ttu-id="f0950-114">Étapes</span><span class="sxs-lookup"><span data-stu-id="f0950-114">Steps</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f0950-115">App-V Server-console de gestion</span><span class="sxs-lookup"><span data-stu-id="f0950-115">App-V Server – Management Console</span></span></p></td>
<td align="left"><ol>
<li><p><span data-ttu-id="f0950-116">Dans la console de gestion, sélectionnez <strong> groupes de connexion </strong> .</span><span class="sxs-lookup"><span data-stu-id="f0950-116">In the Management Console, select <strong>CONNECTION GROUPS</strong>.</span></span></p></li>
<li><p><span data-ttu-id="f0950-117">Sélectionnez le groupe de connexion approprié dans la bibliothèque de groupes de connexion.</span><span class="sxs-lookup"><span data-stu-id="f0950-117">Select the correct connection group from the Connection Groups library.</span></span></p></li>
<li><p><span data-ttu-id="f0950-118">Cliquez sur <strong> modifier </strong> dans le volet packages connectés.</span><span class="sxs-lookup"><span data-stu-id="f0950-118">Click <strong>EDIT</strong> in the CONNECTED PACKAGES pane.</span></span></p></li>
<li><p><span data-ttu-id="f0950-119">Cochez <strong> la case utiliser une version </strong> située en regard du nom du package, puis cliquez sur <strong> appliquer </strong> .</span><span class="sxs-lookup"><span data-stu-id="f0950-119">Select <strong>Use Any Version</strong> check box next to the package name, and click <strong>Apply</strong>.</span></span></p></li>
</ol>
<p><span data-ttu-id="f0950-120">Pour plus d’informations sur l’ajout et la mise à niveau de packages, voir <a href="how-to-add-or-upgrade-packages-by-using-the-management-console-51-gb18030.md" data-raw-source="[How to Add or Upgrade Packages by Using the Management Console](how-to-add-or-upgrade-packages-by-using-the-management-console-51-gb18030.md)"> comment ajouter ou mettre à niveau des packages à l’aide de la console de gestion </a> .</span><span class="sxs-lookup"><span data-stu-id="f0950-120">For more about adding or upgrading packages, see <a href="how-to-add-or-upgrade-packages-by-using-the-management-console-51-gb18030.md" data-raw-source="[How to Add or Upgrade Packages by Using the Management Console](how-to-add-or-upgrade-packages-by-using-the-management-console-51-gb18030.md)">How to Add or Upgrade Packages by Using the Management Console</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f0950-121">Client App-V sur un ordinateur autonome</span><span class="sxs-lookup"><span data-stu-id="f0950-121">App-V Client on a Stand-alone computer</span></span></p></td>
<td align="left"><ol>
<li><p><span data-ttu-id="f0950-122">Créez le document XML de groupe de connexion.</span><span class="sxs-lookup"><span data-stu-id="f0950-122">Create the connection group XML document.</span></span></p></li>
<li><p><span data-ttu-id="f0950-123">Pour mettre à niveau le package, définissez l' <strong> </strong> attribut de balise <strong> de package VersionId </strong> sur un astérisque ( <strong>\*</strong> ).</span><span class="sxs-lookup"><span data-stu-id="f0950-123">For the package to be upgraded, set the <strong>Package</strong> tag attribute <strong>VersionID</strong> to an asterisk (<strong>\*</strong>).</span></span></p></li>
<li><p><span data-ttu-id="f0950-124">Utilisez l’applet de commande suivante pour ajouter le groupe de connexions, puis incluez le chemin d’accès au document XML de groupe de connexion:</span><span class="sxs-lookup"><span data-stu-id="f0950-124">Use the following cmdlet to add the connection group, and include the path to the connection group XML document:</span></span></p>
<p><strong><span data-ttu-id="f0950-125">Add-AppvClientConnectionGroup</span><span class="sxs-lookup"><span data-stu-id="f0950-125">Add-AppvClientConnectionGroup</span></span></strong></p></li>
<li><p><span data-ttu-id="f0950-126">Lorsque vous mettez à niveau un package, utilisez les applets de commande suivantes pour supprimer l’ancien package, ajouter le package mis à niveau et publier le package mis à niveau:</span><span class="sxs-lookup"><span data-stu-id="f0950-126">When you upgrade a package, use the following cmdlets to remove the old package, add the upgraded package, and publish the upgraded package:</span></span></p>
<ul>
<li><p><span data-ttu-id="f0950-127">RemoveAppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="f0950-127">RemoveAppvClientPackage</span></span></p></li>
<li><p><span data-ttu-id="f0950-128">Add-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="f0950-128">Add-AppvClientPackage</span></span></p></li>
<li><p><span data-ttu-id="f0950-129">Publisher-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="f0950-129">Publish-AppvClientPackage</span></span></p></li>
</ul></li>
</ol>
<p><span data-ttu-id="f0950-130">Pour plus d’informations, voir:</span><span class="sxs-lookup"><span data-stu-id="f0950-130">For more information, see:</span></span></p>
<ul>
<li><p><span data-ttu-id="f0950-131">Fichier XML d’exemple, <strong> fichier XML de groupe de connexion avec packages facultatifs </strong> , dans cette section: <a href="how-to-use-optional-packages-in-connection-groups51.md#bkmk-apps-plugs-optional" data-raw-source="[How to Use Optional Packages in Connection Groups](how-to-use-optional-packages-in-connection-groups51.md#bkmk-apps-plugs-optional)"> comment utiliser des packages facultatifs dans les groupes de connexion</span><span class="sxs-lookup"><span data-stu-id="f0950-131">The example XML file, <strong>Connection group XML file with optional packages</strong>, in this section: <a href="how-to-use-optional-packages-in-connection-groups51.md#bkmk-apps-plugs-optional" data-raw-source="[How to Use Optional Packages in Connection Groups](how-to-use-optional-packages-in-connection-groups51.md#bkmk-apps-plugs-optional)">How to Use Optional Packages in Connection Groups</span></span></a></p></li>
<li><p><a href="how-to-manage-app-v-51-packages-running-on-a-stand-alone-computer-by-using-powershell.md" data-raw-source="[How to Manage App-V 5.1 Packages Running on a Stand-Alone Computer by Using PowerShell](how-to-manage-app-v-51-packages-running-on-a-stand-alone-computer-by-using-powershell.md)"><span data-ttu-id="f0950-132">Gestion de packages App-V5.1 s'exécutant sur un ordinateur autonome à l'aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="f0950-132">How to Manage App-V 5.1 Packages Running on a Stand-Alone Computer by Using PowerShell</span></span></a></p></li>
</ul></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>

 






## <span data-ttu-id="f0950-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f0950-133">Related topics</span></span>


[<span data-ttu-id="f0950-134">Gestion des groupes de connexion</span><span class="sxs-lookup"><span data-stu-id="f0950-134">Managing Connection Groups</span></span>](managing-connection-groups51.md)

 

 





