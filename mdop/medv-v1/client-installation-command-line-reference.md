---
title: Référence des lignes de commande d'installation du client
description: Référence des lignes de commande d'installation du client
author: dansimp
ms.assetid: 122a593d-3314-4e9b-858a-08a25ed00c32
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 708daf82699c63dfaa1f99ae595911cf6bad3737
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811928"
---
# <span data-ttu-id="d3396-103">Référence des lignes de commande d'installation du client</span><span class="sxs-lookup"><span data-stu-id="d3396-103">Client Installation Command Line Reference</span></span>


**<span data-ttu-id="d3396-104">Pour installer MED-V à partir de la ligne de commande</span><span class="sxs-lookup"><span data-stu-id="d3396-104">To install MED-V from the command line</span></span>**

1.  <span data-ttu-id="d3396-105">À partir de la ligne de commande, exécutez le package MED-V. msi suivi de tout paramètre facultatif décrit dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="d3396-105">From the command line, run the MED-V .msi package followed by any of the optional parameters described in the following table.</span></span>

2.  <span data-ttu-id="d3396-106">Le package MED-V. msi est appelé *MED-V\_x.msi*, où *x* représente le numéro de version.</span><span class="sxs-lookup"><span data-stu-id="d3396-106">The MED-V .msi package is called *MED-V\_x.msi*, where *x* is the version number.</span></span>

    <span data-ttu-id="d3396-107">Par exemple, *MED-V\_1.0.65.msi*.</span><span class="sxs-lookup"><span data-stu-id="d3396-107">For example, *MED-V\_1.0.65.msi*.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d3396-108">Paramètre</span><span class="sxs-lookup"><span data-stu-id="d3396-108">Parameter</span></span></th>
<th align="left"><span data-ttu-id="d3396-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="d3396-109">Value</span></span></th>
<th align="left"><span data-ttu-id="d3396-110">Description</span><span class="sxs-lookup"><span data-stu-id="d3396-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d3396-111">/quiet</span><span class="sxs-lookup"><span data-stu-id="d3396-111">/quiet</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="d3396-112">Installation silencieuse</span><span class="sxs-lookup"><span data-stu-id="d3396-112">Silent installation</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d3396-113">/log &lt; chemin d’accès complet au fichier journal&gt;</span><span class="sxs-lookup"><span data-stu-id="d3396-113">/log &lt;full path to log file&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="d3396-114">Le chemin d’accès complet au fichier journal.</span><span class="sxs-lookup"><span data-stu-id="d3396-114">The full path to the log file.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d3396-115">INSTALLDIR</span><span class="sxs-lookup"><span data-stu-id="d3396-115">INSTALLDIR</span></span></p></td>
<td align="left"><p><span data-ttu-id="d3396-116">Le chemin d’accès complet au répertoire d’installation.</span><span class="sxs-lookup"><span data-stu-id="d3396-116">The full path to the installation directory.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d3396-117">VMSFOLDER</span><span class="sxs-lookup"><span data-stu-id="d3396-117">VMSFOLDER</span></span></p></td>
<td align="left"><p><span data-ttu-id="d3396-118">Le chemin d’accès complet au dossier de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="d3396-118">The full path to the virtual machine folder.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d3396-119">INSTALL_ADMIN_TOOLS</span><span class="sxs-lookup"><span data-stu-id="d3396-119">INSTALL_ADMIN_TOOLS</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="d3396-120">1, 0</span><span class="sxs-lookup"><span data-stu-id="d3396-120">1,0</span></span></strong></p>
<p><span data-ttu-id="d3396-121">Par défaut: <strong> 0</span><span class="sxs-lookup"><span data-stu-id="d3396-121">Default: <strong>0</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="d3396-122">Installe les outils d’administration de MED-V.</span><span class="sxs-lookup"><span data-stu-id="d3396-122">Installs MED-V administration tools.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d3396-123">START_AUTOMATICALLY</span><span class="sxs-lookup"><span data-stu-id="d3396-123">START_AUTOMATICALLY</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="d3396-124">1, 0</span><span class="sxs-lookup"><span data-stu-id="d3396-124">1,0</span></span></strong></p>
<p><span data-ttu-id="d3396-125">Par défaut: <strong> 0</span><span class="sxs-lookup"><span data-stu-id="d3396-125">Default: <strong>0</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="d3396-126">Démarre automatiquement le client MED-V chaque fois que l’utilisateur ouvre une session Windows.</span><span class="sxs-lookup"><span data-stu-id="d3396-126">Automatically starts MED-V client every time the user logs on to Windows.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d3396-127">SERVER_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="d3396-127">SERVER_ADDRESS</span></span></p></td>
<td align="left"><p><span data-ttu-id="d3396-128">nom d’hôte ou adresse IP</span><span class="sxs-lookup"><span data-stu-id="d3396-128">host name or IP</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d3396-129">SERVER_PORT</span><span class="sxs-lookup"><span data-stu-id="d3396-129">SERVER_PORT</span></span></p></td>
<td align="left"><p><span data-ttu-id="d3396-130">port</span><span class="sxs-lookup"><span data-stu-id="d3396-130">port</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d3396-131">SERVER_SSL</span><span class="sxs-lookup"><span data-stu-id="d3396-131">SERVER_SSL</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="d3396-132">1, 0</span><span class="sxs-lookup"><span data-stu-id="d3396-132">1,0</span></span></strong></p>
<p><span data-ttu-id="d3396-133">pour <strong> https </strong> ou <strong> http</span><span class="sxs-lookup"><span data-stu-id="d3396-133">for <strong>https</strong> or <strong>http</span></span></strong></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d3396-134">START_MEDV</span><span class="sxs-lookup"><span data-stu-id="d3396-134">START_MEDV</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="d3396-135">1, 0</span><span class="sxs-lookup"><span data-stu-id="d3396-135">1,0</span></span></strong></p>
<p><span data-ttu-id="d3396-136">Par défaut: <strong> 1</span><span class="sxs-lookup"><span data-stu-id="d3396-136">Default: <strong>1</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="d3396-137">Démarre MED-V à la fin de l’installation de MED-V.</span><span class="sxs-lookup"><span data-stu-id="d3396-137">Starts MED-V at the completion of the MED-V installation.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="d3396-138">Remarque</span><span class="sxs-lookup"><span data-stu-id="d3396-138">Note</span></span></strong><br/><p><span data-ttu-id="d3396-139">Nous vous conseillons de définir START_MEDV = 0 si MED-V est installé par le système.</span><span class="sxs-lookup"><span data-stu-id="d3396-139">It is recommended to set START_MEDV=0 in case MED-V is installed by the system.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d3396-140">DESKTOP_SHORTCUT</span><span class="sxs-lookup"><span data-stu-id="d3396-140">DESKTOP_SHORTCUT</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="d3396-141">1, 0</span><span class="sxs-lookup"><span data-stu-id="d3396-141">1,0</span></span></strong></p>
<p><span data-ttu-id="d3396-142">Par défaut: <strong> 1</span><span class="sxs-lookup"><span data-stu-id="d3396-142">Default: <strong>1</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="d3396-143">Crée un raccourci sur le bureau, qui démarre le client MED-V.</span><span class="sxs-lookup"><span data-stu-id="d3396-143">Creates a shortcut on the desktop, which starts MED-V client.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d3396-144">MINIMAL_RAM_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="d3396-144">MINIMAL_RAM_REQUIRED</span></span></p></td>
<td align="left"><p><span data-ttu-id="d3396-145">RAM en Mo</span><span class="sxs-lookup"><span data-stu-id="d3396-145">RAM in MB</span></span></p></td>
<td align="left"><p><span data-ttu-id="d3396-146">Lors de l’installation de MED-V, vérifie si le nombre minimal de RAM est spécifié pour l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="d3396-146">When installing MED-V, checks whether the computer has the minimum amount of RAM specified.</span></span> <span data-ttu-id="d3396-147">Si ce n’est pas le cas, l’installation a été annulée.</span><span class="sxs-lookup"><span data-stu-id="d3396-147">If not, installation is aborted.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d3396-148">SKIP_OS_CHECK</span><span class="sxs-lookup"><span data-stu-id="d3396-148">SKIP_OS_CHECK</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="d3396-149">1, 0</span><span class="sxs-lookup"><span data-stu-id="d3396-149">1,0</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="d3396-150">Omet la validation du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="d3396-150">Omits the operating system validation.</span></span></p></td>
</tr>
</tbody>
</table>











