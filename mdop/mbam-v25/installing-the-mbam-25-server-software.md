---
title: Installation du logiciel serveur MBAM2.5
description: Installation du logiciel serveur MBAM2.5
author: dansimp
ms.assetid: b9dbe697-5400-4bac-acfb-ee6dc6586c30
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6612bf52aa53ae693694d7ac02c5cab212d4e24f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809929"
---
# <span data-ttu-id="d5c29-103">Installation du logiciel serveur MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="d5c29-103">Installing the MBAM 2.5 Server Software</span></span>


<span data-ttu-id="d5c29-104">Cette rubrique décrit comment installer le logiciel serveur d’administration et de surveillance de BitLocker (MBAM) 2,5 à l’aide de l’Assistant de configuration de l’administration et de la surveillance de BitLocker ou en utilisant des paramètres de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="d5c29-104">This topic describes how to install the Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 Server software by using the Microsoft BitLocker Administration and Monitoring Setup wizard or by using command-line parameters.</span></span> <span data-ttu-id="d5c29-105">Répétez le processus d’installation du serveur pour chaque serveur sur lequel vous configurez les fonctionnalités du serveur MBAM 2,5.</span><span class="sxs-lookup"><span data-stu-id="d5c29-105">Repeat the server installation process for each server on which you are configuring MBAM 2.5 Server features.</span></span> <span data-ttu-id="d5c29-106">Une fois l’installation terminée, reportez-vous à [Configuration des fonctionnalités du serveur MBAM 2,5](configuring-the-mbam-25-server-features.md) pour connaître les étapes de configuration des fonctionnalités du serveur.</span><span class="sxs-lookup"><span data-stu-id="d5c29-106">After you finish the installation, see [Configuring the MBAM 2.5 Server Features](configuring-the-mbam-25-server-features.md) for steps about configuring the Server features.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d5c29-107">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="d5c29-107">Before you start</span></span></th>
<th align="left"><span data-ttu-id="d5c29-108">Description</span><span class="sxs-lookup"><span data-stu-id="d5c29-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d5c29-109">Passez en revue les informations de planification de MBAM 2,5</span><span class="sxs-lookup"><span data-stu-id="d5c29-109">Review the MBAM 2.5 planning information</span></span></p></td>
<td align="left"><ul>
<li><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)"><span data-ttu-id="d5c29-110">Conditions préalables pour le serveur MBAM2.5 pour les topologies Intégration Configuration Manager et autonome</span><span class="sxs-lookup"><span data-stu-id="d5c29-110">MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies</span></span></a></p></li>
<li><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"><span data-ttu-id="d5c29-111">Configurations prises en charge par MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="d5c29-111">MBAM 2.5 Supported Configurations</span></span></a></p></li>
<li><p><a href="high-level-architecture-for-mbam-25.md" data-raw-source="[High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md)"><span data-ttu-id="d5c29-112">Architecture de hautniveau pour MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="d5c29-112">High-Level Architecture for MBAM 2.5</span></span></a></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d5c29-113">Découvrir comment obtenir les fichiers journaux</span><span class="sxs-lookup"><span data-stu-id="d5c29-113">Read how to get log files</span></span></p></td>
<td align="left"><p><span data-ttu-id="d5c29-114">Par défaut, les fichiers journaux sont créés dans le dossier% Temp% de l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="d5c29-114">By default, log files are created in the local computer’s %temp% folder.</span></span> <span data-ttu-id="d5c29-115">Pour enregistrer les fichiers journaux à un emplacement spécifique plutôt que dans le <strong> dossier% Temp </strong> %, utilisez l' <strong> </strong> &lt; <em> argument d’emplacement/log </em> &gt; .</span><span class="sxs-lookup"><span data-stu-id="d5c29-115">To write the log files to a specific location rather than to the <strong>%temp</strong>% folder, use the <strong>/log</strong> &lt;<em>location</em>&gt; argument.</span></span></p>
<p><span data-ttu-id="d5c29-116">Des événements supplémentaires peuvent être enregistrés dans l’observateur d’événements dans les <strong> nœuds mbam-setup </strong> ou <strong> MBAM-site Web </strong> sous <strong> applications et services consigne &gt; Microsoft &gt; Windows </strong> .</span><span class="sxs-lookup"><span data-stu-id="d5c29-116">Additional events might be logged in Event Viewer in the <strong>MBAM-Setup</strong> or <strong>MBAM-Web</strong> nodes under <strong>Applications and Services Logs &gt; Microsoft &gt; Windows</strong>.</span></span> <span data-ttu-id="d5c29-117">Par exemple, si vous désinstallez MBAM, le programme de désinstallation désinstalle également les journaux MBAM-Setup et MBAM-Web dans EventViewer.</span><span class="sxs-lookup"><span data-stu-id="d5c29-117">For example, if you uninstall MBAM, the uninstaller will also uninstall the MBAM-Setup and MBAM-Web logs in EventViewer.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="d5c29-118">Installation du logiciel serveur MBAM 2,5 à l’aide de l’Assistant Configuration et analyse de Microsoft BitLocker</span><span class="sxs-lookup"><span data-stu-id="d5c29-118">Installing the MBAM 2.5 Server software by using the Microsoft BitLocker Administration and Monitoring Setup wizard</span></span>


<span data-ttu-id="d5c29-119">Suivez les étapes ci-dessous pour installer le logiciel serveur MBAM à l’aide de l’Assistant Configuration et analyse de Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="d5c29-119">Use these steps to install the MBAM Server software by using the Microsoft BitLocker Administration and Monitoring Setup wizard.</span></span>

**<span data-ttu-id="d5c29-120">Pour installer le logiciel serveur MBAM 2,5 à l’aide de l’Assistant</span><span class="sxs-lookup"><span data-stu-id="d5c29-120">To install the MBAM 2.5 Server software by using the wizard</span></span>**

1.  <span data-ttu-id="d5c29-121">Sur le serveur sur lequel vous souhaitez installer MBAM, exécutez **MBAMserversetup.exe** pour démarrer l’Assistant de configuration de l’administration et de la surveillance de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="d5c29-121">On the server where you want to install MBAM, run **MBAMserversetup.exe** to start the Microsoft BitLocker Administration and Monitoring Setup wizard.</span></span>

2.  <span data-ttu-id="d5c29-122">Dans la page **Bienvenue** , cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="d5c29-122">On the **Welcome** page, click **Next**.</span></span>

3.  <span data-ttu-id="d5c29-123">Lisez et acceptez le contrat de licence logiciel Microsoft, puis cliquez sur **suivant** pour continuer l’installation.</span><span class="sxs-lookup"><span data-stu-id="d5c29-123">Read and accept the Microsoft Software License Agreement, and then click **Next** to continue the installation.</span></span>

4.  <span data-ttu-id="d5c29-124">Indiquez si vous souhaitez utiliser Microsoft Update lors de la recherche de mises à jour, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="d5c29-124">Choose whether to use Microsoft Update when you check for updates, and then click **Next**.</span></span>

5.  <span data-ttu-id="d5c29-125">Indiquez si vous souhaitez participer au programme d’amélioration du produit, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="d5c29-125">Choose whether to participate in the Customer Experience Improvement Program, and then click **Next**.</span></span>

6.  <span data-ttu-id="d5c29-126">Pour démarrer l’installation, cliquez sur **installer**.</span><span class="sxs-lookup"><span data-stu-id="d5c29-126">To start the installation, click **Install**.</span></span>

7.  <span data-ttu-id="d5c29-127">Pour configurer les fonctionnalités du serveur après l’installation du logiciel MBAM Server, activez la case à cocher **exécuter MBAM Server Configuration une fois l’Assistant fermé** .</span><span class="sxs-lookup"><span data-stu-id="d5c29-127">To configure the server features after the MBAM Server software finishes installing, select the **Run MBAM Server Configuration after the wizard closes** check box.</span></span> <span data-ttu-id="d5c29-128">Vous pouvez également configurer MBAM plus tard en utilisant le raccourci de **configuration de MBAM Server** que le programme d’installation du serveur crée dans le menu **Démarrer** .</span><span class="sxs-lookup"><span data-stu-id="d5c29-128">Alternatively, you can configure MBAM later by using the **MBAM Server Configuration** shortcut that the server installation creates on your **Start** menu.</span></span>

8.  <span data-ttu-id="d5c29-129">Cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="d5c29-129">Click **Finish**.</span></span>

## <span data-ttu-id="d5c29-130">Installation du logiciel serveur MBAM 2,5 à l’aide d’une fenêtre d’invite de commandes</span><span class="sxs-lookup"><span data-stu-id="d5c29-130">Installing the MBAM 2.5 Server software by using a Command Prompt window</span></span>


<span data-ttu-id="d5c29-131">À l’invite de commandes, tapez une commande similaire à la commande suivante pour installer le logiciel serveur MBAM.</span><span class="sxs-lookup"><span data-stu-id="d5c29-131">At a command prompt, type a command similar to the following command to install the MBAM Server software.</span></span>

``` syntax
MbamServerSetup.exe MBAMServerInstall.log
CEIPENABLED=True OPTIN_FOR_MICROFOST_UPDATES=True INSTALLDIR=c:\mbaminstall
```

<span data-ttu-id="d5c29-132">Le tableau suivant décrit les paramètres de ligne de commande pour l’installation du logiciel MBAM 2,5 Server.</span><span class="sxs-lookup"><span data-stu-id="d5c29-132">The following table describes the command-line parameters for installing the MBAM 2.5 Server software.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d5c29-133">Paramètre</span><span class="sxs-lookup"><span data-stu-id="d5c29-133">Parameter</span></span></th>
<th align="left"><span data-ttu-id="d5c29-134">Valeur du paramètre</span><span class="sxs-lookup"><span data-stu-id="d5c29-134">Parameter value</span></span></th>
<th align="left"><span data-ttu-id="d5c29-135">Description</span><span class="sxs-lookup"><span data-stu-id="d5c29-135">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d5c29-136">CEIPENABLED</span><span class="sxs-lookup"><span data-stu-id="d5c29-136">CEIPENABLED</span></span></p></td>
<td align="left"><p><span data-ttu-id="d5c29-137">Vrai faux</span><span class="sxs-lookup"><span data-stu-id="d5c29-137">True False</span></span></p></td>
<td align="left"><p><span data-ttu-id="d5c29-138">Vrai-participer au programme d’amélioration du produit, qui permet à Microsoft d’identifier les fonctionnalités de MBAM à améliorer.</span><span class="sxs-lookup"><span data-stu-id="d5c29-138">True - participate in the Customer Improvement Experience Program, which helps Microsoft identify which MBAM features to improve.</span></span></p>
<p><span data-ttu-id="d5c29-139">Faux – ne pas participer au programme d’amélioration du produit.</span><span class="sxs-lookup"><span data-stu-id="d5c29-139">False – do not participate in the Customer Improvement Experience Program.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d5c29-140">OPTIN_FOR_MICROSOFT_UPDATES</span><span class="sxs-lookup"><span data-stu-id="d5c29-140">OPTIN_FOR_MICROSOFT_UPDATES</span></span></p></td>
<td align="left"><p><span data-ttu-id="d5c29-141">Vrai faux</span><span class="sxs-lookup"><span data-stu-id="d5c29-141">True False</span></span></p></td>
<td align="left"><p><span data-ttu-id="d5c29-142">Vrai-utilisez Microsoft Update pour garantir la sécurité et la mise à jour de votre ordinateur pour Windows et d’autres produits Microsoft, y compris MBAM.</span><span class="sxs-lookup"><span data-stu-id="d5c29-142">True - use Microsoft Update to keep your computer secure and up-to-date for Windows and other Microsoft products, including MBAM.</span></span></p>
<p><span data-ttu-id="d5c29-143">Faux – ne pas utiliser Microsoft Update</span><span class="sxs-lookup"><span data-stu-id="d5c29-143">False – do not use Microsoft Update</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d5c29-144">INSTALLDIR</span><span class="sxs-lookup"><span data-stu-id="d5c29-144">INSTALLDIR</span></span></p></td>
<td align="left"><p><span data-ttu-id="d5c29-145">&lt;Chemin d'accès&gt;</span><span class="sxs-lookup"><span data-stu-id="d5c29-145">&lt;Path&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="d5c29-146">Emplacement où vous souhaitez installer MBAM.</span><span class="sxs-lookup"><span data-stu-id="d5c29-146">Location where you want to install MBAM.</span></span></p>
<p><span data-ttu-id="d5c29-147">Exemple :</span><span class="sxs-lookup"><span data-stu-id="d5c29-147">Example:</span></span></p>
<p><span data-ttu-id="d5c29-148">INSTALLDIR = c:\mbaminstall</span><span class="sxs-lookup"><span data-stu-id="d5c29-148">INSTALLDIR=c:\mbaminstall</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d5c29-149">FORCE_UNINSTALL</span><span class="sxs-lookup"><span data-stu-id="d5c29-149">FORCE_UNINSTALL</span></span></p></td>
<td align="left"><p><span data-ttu-id="d5c29-150">Vrai faux</span><span class="sxs-lookup"><span data-stu-id="d5c29-150">True False</span></span></p></td>
<td align="left"><p><span data-ttu-id="d5c29-151">Vrai-poursuivre le processus de désinstallation d’MBAM, même si des fonctionnalités ne peuvent pas être supprimées.</span><span class="sxs-lookup"><span data-stu-id="d5c29-151">True - continue the process of uninstalling MBAM, even if any features fail to be removed.</span></span></p>
<p><span data-ttu-id="d5c29-152">False (par défaut) si l’action personnalisée de désinstallation ne parvient pas à supprimer une fonctionnalité de serveur MBAM ajoutée, la désinstallation échoue et MBAM reste installé.</span><span class="sxs-lookup"><span data-stu-id="d5c29-152">False (default) if the uninstallation custom action fails to remove an added MBAM Server feature, the uninstallation fails, and MBAM remains installed.</span></span></p>
<p><span data-ttu-id="d5c29-153">Dans les deux cas, toutes les fonctionnalités qui ont été correctement supprimées lors de la tentative de désinstallation de MBAM restent supprimées.</span><span class="sxs-lookup"><span data-stu-id="d5c29-153">In both instances, any features that were successfully removed during the attempt to uninstall MBAM stay removed.</span></span></p></td>
</tr>
</tbody>
</table>

 



## <span data-ttu-id="d5c29-154">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d5c29-154">Related topics</span></span>


[<span data-ttu-id="d5c29-155">Déploiement de MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="d5c29-155">Deploying MBAM 2.5</span></span>](deploying-mbam-25.md)

[<span data-ttu-id="d5c29-156">Configuration des composants du serveur MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="d5c29-156">Configuring the MBAM 2.5 Server Features</span></span>](configuring-the-mbam-25-server-features.md)

 

## <span data-ttu-id="d5c29-157">Vous avez une suggestion pour MBAM?</span><span class="sxs-lookup"><span data-stu-id="d5c29-157">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="d5c29-158">Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)</span><span class="sxs-lookup"><span data-stu-id="d5c29-158">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="d5c29-159">Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="d5c29-159">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





