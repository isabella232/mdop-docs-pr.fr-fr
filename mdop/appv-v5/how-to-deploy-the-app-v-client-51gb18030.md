---
title: Comment déployer App-V Client
description: Comment déployer App-V Client
author: dansimp
ms.assetid: 981f57c9-56c3-45da-8261-0972bfad3e5b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: ea216f6b86820f752e0c0ac693470eac72cb847a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805491"
---
# <span data-ttu-id="b4f39-103">Comment déployer App-V Client</span><span class="sxs-lookup"><span data-stu-id="b4f39-103">How to Deploy the App-V Client</span></span>


<span data-ttu-id="b4f39-104">Utilisez la procédure suivante pour installer le client Microsoft Application Virtualization (App-V) 5,1 et le client services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="b4f39-104">Use the following procedure to install the Microsoft Application Virtualization (App-V) 5.1 client and Remote Desktop Services client.</span></span> <span data-ttu-id="b4f39-105">Vous devez installer la version du client qui correspond au système d’exploitation de l’ordinateur cible.</span><span class="sxs-lookup"><span data-stu-id="b4f39-105">You must install the version of the client that matches the operating system of the target computer.</span></span>

<a href="" id="bkmk-clt-install-prereqs"></a>**<span data-ttu-id="b4f39-106">Que faire avant de commencer</span><span class="sxs-lookup"><span data-stu-id="b4f39-106">What to do before you start</span></span>**

1. <span data-ttu-id="b4f39-107">Passez en revue et installez les logiciels requis:</span><span class="sxs-lookup"><span data-stu-id="b4f39-107">Review and install the software prerequisites:</span></span>

   <span data-ttu-id="b4f39-108">Installez les logiciels requis correspondant à la version d’App-V que vous installez:</span><span class="sxs-lookup"><span data-stu-id="b4f39-108">Install the prerequisite software that corresponds to the version of App-V that you are installing:</span></span>

   -   [<span data-ttu-id="b4f39-109">À propos d'App-V5.1</span><span class="sxs-lookup"><span data-stu-id="b4f39-109">About App-V 5.1</span></span>](about-app-v-51.md)

   -   [<span data-ttu-id="b4f39-110">Composants requis d'App-V5.1</span><span class="sxs-lookup"><span data-stu-id="b4f39-110">App-V 5.1 Prerequisites</span></span>](app-v-51-prerequisites.md)

2. <span data-ttu-id="b4f39-111">Passez en revue la coexistence du client et les scénarios non pris en charge, comme le concernent votre installation:</span><span class="sxs-lookup"><span data-stu-id="b4f39-111">Review the client coexistence and unsupported scenarios, as applicable to your installation:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="b4f39-112">Déploiement de clients App-V de coexistence</span><span class="sxs-lookup"><span data-stu-id="b4f39-112">Deploying coexisting App-V clients</span></span></p></td>
   <td align="left"><p><a href="planning-for-the-app-v-51-sequencer-and-client-deployment.md" data-raw-source="[Planning for the App-V 5.1 Sequencer and Client Deployment](planning-for-the-app-v-51-sequencer-and-client-deployment.md)"><span data-ttu-id="b4f39-113">Planification du déploiement d'App-V5.1 Sequencer et Client</span><span class="sxs-lookup"><span data-stu-id="b4f39-113">Planning for the App-V 5.1 Sequencer and Client Deployment</span></span></a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="b4f39-114">Scénarios d’installation non pris en charge ou limités</span><span class="sxs-lookup"><span data-stu-id="b4f39-114">Unsupported or limited installation scenarios</span></span></p></td>
   <td align="left"><p><span data-ttu-id="b4f39-115">Voir la section client dans les <a href="app-v-51-supported-configurations.md" data-raw-source="[App-V 5.1 Supported Configurations](app-v-51-supported-configurations.md)"> configurations App-V 5,1 prises en charge</span><span class="sxs-lookup"><span data-stu-id="b4f39-115">See the client section in <a href="app-v-51-supported-configurations.md" data-raw-source="[App-V 5.1 Supported Configurations](app-v-51-supported-configurations.md)">App-V 5.1 Supported Configurations</span></span></a></p></td>
   </tr>
   </tbody>
   </table>



3. <span data-ttu-id="b4f39-116">Passez en revue les emplacements du Registre, du journal et des informations de dépannage du client:</span><span class="sxs-lookup"><span data-stu-id="b4f39-116">Review the locations for client registry, log, and troubleshooting information:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b4f39-117">Informations de Registre du client</span><span class="sxs-lookup"><span data-stu-id="b4f39-117">Client registry information</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="b4f39-118">Par défaut, après avoir installé le client App-V 5,1, les informations sur le client sont stockées dans le registre dans la clé de Registre suivante:</span><span class="sxs-lookup"><span data-stu-id="b4f39-118">By default, after you install the App-V 5.1 client, the client information is stored in the registry in the following registry key:</span></span></p>
<p><strong><span data-ttu-id="b4f39-119">HKEY_LOCAL_MACHINE \ SOFTWARE \ MICROSOFT \ APPV \ CLIENT</span><span class="sxs-lookup"><span data-stu-id="b4f39-119">HKEY_LOCAL_MACHINE \ SOFTWARE \ MICROSOFT \ APPV \ CLIENT</span></span></strong></p></li>
<li><p><span data-ttu-id="b4f39-120">Lorsque vous déployez un package virtualisé sur un ordinateur exécutant le client App-V, les données de package associées sont stockées à l’emplacement suivant:</span><span class="sxs-lookup"><span data-stu-id="b4f39-120">When you deploy a virtualized package to a computer that is running the App-V client, the associated package data is stored in the following location:</span></span></p>
<p><strong><span data-ttu-id="b4f39-121">C: \ ProgramData \ App-V</span><span class="sxs-lookup"><span data-stu-id="b4f39-121">C: \ ProgramData \ App-V</span></span></strong></p>
<p><span data-ttu-id="b4f39-122">Toutefois, vous pouvez reconfigurer cet emplacement avec la clé de Registre suivante:</span><span class="sxs-lookup"><span data-stu-id="b4f39-122">However, you can reconfigure this location with the following registry key:</span></span></p>
<p><strong><span data-ttu-id="b4f39-123">HKEY_LOCAL_MACHINE \ SOFTWARE \ MICROSOFT \ SOFTWARE \ MICROSOFT \ APPV \ CLIENT \ STREAMING \ PACKAGEINSTALLATIONROOT</span><span class="sxs-lookup"><span data-stu-id="b4f39-123">HKEY_LOCAL_MACHINE \ SOFTWARE \ MICROSOFT \ SOFTWARE \ MICROSOFT \ APPV \ CLIENT \ STREAMING \ PACKAGEINSTALLATIONROOT</span></span></strong></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b4f39-124">Fichiers journaux du client</span><span class="sxs-lookup"><span data-stu-id="b4f39-124">Client log files</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="b4f39-125">Pour les informations de fichier journal associées au client App-V 5,1, recherchez dans le journal suivant:</span><span class="sxs-lookup"><span data-stu-id="b4f39-125">For log file information that is associated with the App-V 5.1 Client, search in the following log:</span></span></p>
<p><strong><span data-ttu-id="b4f39-126">Journaux d’événements/applications et journaux de services/Microsoft/AppV</span><span class="sxs-lookup"><span data-stu-id="b4f39-126">Event logs / Applications and Services Logs / Microsoft / AppV</span></span></strong></p></li>
<li><p><span data-ttu-id="b4f39-127">Dans App-V 5,0 SP3, certains journaux ont été consolidés et déplacés vers l’emplacement suivant:</span><span class="sxs-lookup"><span data-stu-id="b4f39-127">In App-V 5.0 SP3, some logs were consolidated and moved to the following location:</span></span></p>
<p><strong><span data-ttu-id="b4f39-128">Journaux d’événements/applications et services journaux de Microsoft/AppV/ServiceLog</span><span class="sxs-lookup"><span data-stu-id="b4f39-128">Event logs/Applications and Services Logs/Microsoft/AppV/ServiceLog</span></span></strong></p>
<p><span data-ttu-id="b4f39-129">Pour obtenir la liste des journaux déplacés, voir <a href="about-app-v-50-sp3.md#bkmk-event-logs-moved" data-raw-source="[About App-V 5.0 SP3](about-app-v-50-sp3.md#bkmk-event-logs-moved)"> à propos de App-V 5,0 SP3 </a> .</span><span class="sxs-lookup"><span data-stu-id="b4f39-129">For a list of the moved logs, see <a href="about-app-v-50-sp3.md#bkmk-event-logs-moved" data-raw-source="[About App-V 5.0 SP3](about-app-v-50-sp3.md#bkmk-event-logs-moved)">About App-V 5.0 SP3</a>.</span></span></p></li>
<li><p><span data-ttu-id="b4f39-130">Les packages actuellement stockés sur des ordinateurs exécutant le client App-V 5,1 sont enregistrés à l’emplacement suivant:</span><span class="sxs-lookup"><span data-stu-id="b4f39-130">Packages that are currently stored on computers that run the App-V 5.1 Client are saved to the following location:</span></span></p>
<p><strong><span data-ttu-id="b4f39-131">C:\ProgramData\App-V &amp; lt; ID de package &gt; &amp; lt; ID de version&gt;</span><span class="sxs-lookup"><span data-stu-id="b4f39-131">C:\ProgramData\App-V&amp;lt;package id&gt;&amp;lt;version id&gt;</span></span></strong></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b4f39-132">Informations de résolution des problèmes d’installation du client</span><span class="sxs-lookup"><span data-stu-id="b4f39-132">Client installation troubleshooting information</span></span></p></td>
<td align="left"><p><span data-ttu-id="b4f39-133">Consultez le journal des erreurs dans le <strong> dossier% Temp% </strong> .</span><span class="sxs-lookup"><span data-stu-id="b4f39-133">See the error log in the <strong>%temp%</strong> folder.</span></span> <span data-ttu-id="b4f39-134">Pour passer en revue les fichiers journaux, cliquez sur <strong> Démarrer </strong> , tapez <strong> % temp% </strong> , puis recherchez le <strong> Journal de appv_ </strong> .</span><span class="sxs-lookup"><span data-stu-id="b4f39-134">To review the log files, click <strong>Start</strong>, type <strong>%temp%</strong>, and then look for the <strong>appv_ log</strong>.</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="b4f39-135">Pour installer le client App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="b4f39-135">To install the App-V 5.1 Client</span></span>**

1.  <span data-ttu-id="b4f39-136">Copiez le fichier d’installation du client App-V 5,1 sur l’ordinateur sur lequel il est installé.</span><span class="sxs-lookup"><span data-stu-id="b4f39-136">Copy the App-V 5.1 client installation file to the computer on which it will be installed.</span></span> <span data-ttu-id="b4f39-137">Choisissez l’une des méthodes suivantes:</span><span class="sxs-lookup"><span data-stu-id="b4f39-137">Choose from the following client types:</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="b4f39-138">Type de client</span><span class="sxs-lookup"><span data-stu-id="b4f39-138">Client type</span></span></th>
    <th align="left"><span data-ttu-id="b4f39-139">Fichier à utiliser</span><span class="sxs-lookup"><span data-stu-id="b4f39-139">File to use</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="b4f39-140">Version standard du client</span><span class="sxs-lookup"><span data-stu-id="b4f39-140">Standard version of the client</span></span></p></td>
    <td align="left"><p><strong><span data-ttu-id="b4f39-141">appv_client_setup.exe</span><span class="sxs-lookup"><span data-stu-id="b4f39-141">appv_client_setup.exe</span></span></strong></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="b4f39-142">Version du service bureau à distance du client</span><span class="sxs-lookup"><span data-stu-id="b4f39-142">Remote Desktop Services version of the client</span></span></p></td>
    <td align="left"><p><strong><span data-ttu-id="b4f39-143">appv_client_setup_rds.exe</span><span class="sxs-lookup"><span data-stu-id="b4f39-143">appv_client_setup_rds.exe</span></span></strong></p></td>
    </tr>
    </tbody>
    </table>



2.  <span data-ttu-id="b4f39-144">Double-cliquez sur le fichier d’installation, puis cliquez sur **installer**.</span><span class="sxs-lookup"><span data-stu-id="b4f39-144">Double-click the installation file, and click **Install**.</span></span> <span data-ttu-id="b4f39-145">Avant le début de l’installation, le programme d’installation vérifie que l’ordinateur ne contient aucune [Configuration requise pour App-V 5,1](app-v-51-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="b4f39-145">Before the installation begins, the installer checks the computer for any missing [App-V 5.1 Prerequisites](app-v-51-prerequisites.md).</span></span>

3.  <span data-ttu-id="b4f39-146">Passez en revue et acceptez les termes du contrat de licence logiciel, spécifiez si vous souhaitez utiliser Microsoft Update et si vous souhaitez participer au programme d’amélioration de l’utilisation de Microsoft, puis cliquez sur **installer**.</span><span class="sxs-lookup"><span data-stu-id="b4f39-146">Review and accept the Software License Terms, choose whether to use Microsoft Update and whether to participate in the Microsoft Customer Experience Improvement Program, and click **Install**.</span></span>

4.  <span data-ttu-id="b4f39-147">Dans la page **Configuration terminée** , cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="b4f39-147">On the **Setup completed successfully** page, click **Close**.</span></span>

    <span data-ttu-id="b4f39-148">L’installation crée les entrées suivantes pour le client App-V dans les **programmes**:</span><span class="sxs-lookup"><span data-stu-id="b4f39-148">The installation creates the following entries for the App-V client in **Programs**:</span></span>

    -   **<span data-ttu-id="b4f39-149">.exe</span><span class="sxs-lookup"><span data-stu-id="b4f39-149">.exe</span></span>**

    -   **<span data-ttu-id="b4f39-150">.msi</span><span class="sxs-lookup"><span data-stu-id="b4f39-150">.msi</span></span>**

    -   **<span data-ttu-id="b4f39-151">module linguistique</span><span class="sxs-lookup"><span data-stu-id="b4f39-151">language pack</span></span>**

        **<span data-ttu-id="b4f39-152">Remarque</span><span class="sxs-lookup"><span data-stu-id="b4f39-152">Note</span></span>**  
        <span data-ttu-id="b4f39-153">Après l’installation, seul le fichier. exe peut être désinstallé.</span><span class="sxs-lookup"><span data-stu-id="b4f39-153">After the installation, only the .exe file can be uninstalled.</span></span>



**<span data-ttu-id="b4f39-154">Pour installer le client App-V 5,1 à l’aide d’un script</span><span class="sxs-lookup"><span data-stu-id="b4f39-154">To install the App-V 5.1 client using a script</span></span>**

1. <span data-ttu-id="b4f39-155">Installez tous les logiciels requis requis sur les ordinateurs cibles.</span><span class="sxs-lookup"><span data-stu-id="b4f39-155">Install all of the required prerequisite software on the target computers.</span></span> <span data-ttu-id="b4f39-156">Apprenez [à faire avant de commencer](#bkmk-clt-install-prereqs).</span><span class="sxs-lookup"><span data-stu-id="b4f39-156">See [What to do before you start](#bkmk-clt-install-prereqs).</span></span> <span data-ttu-id="b4f39-157">Si vous installez le client à l’aide d’un fichier. msi, l’installation échoue si une configuration requise est manquante.</span><span class="sxs-lookup"><span data-stu-id="b4f39-157">If you install the client by using an .msi file, the installation will fail if any prerequisites are missing.</span></span>

2. <span data-ttu-id="b4f39-158">Pour utiliser un script pour installer le client App-V 5,1, utilisez les paramètres suivants avec **appv\_client\_setup.exe**.</span><span class="sxs-lookup"><span data-stu-id="b4f39-158">To use a script to install the App-V 5.1 client, use the following parameters with **appv\_client\_setup.exe**.</span></span>

   **<span data-ttu-id="b4f39-159">Remarque</span><span class="sxs-lookup"><span data-stu-id="b4f39-159">Note</span></span>**  
   <span data-ttu-id="b4f39-160">Le client Windows Installer (. msi) prend en charge le même ensemble de commutateurs, à l’exception du paramètre **/log** .</span><span class="sxs-lookup"><span data-stu-id="b4f39-160">The client Windows Installer (.msi) supports the same set of switches, except for the **/LOG** parameter.</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="b4f39-161">/INSTALLDIR</span><span class="sxs-lookup"><span data-stu-id="b4f39-161">/INSTALLDIR</span></span></p></td>
   <td align="left"><p><span data-ttu-id="b4f39-162">Spécifie le répertoire d’installation.</span><span class="sxs-lookup"><span data-stu-id="b4f39-162">Specifies the installation directory.</span></span> <span data-ttu-id="b4f39-163">Exemple d’utilisation: <strong> /INSTALLDIR = C:\Program Files\AppV client</span><span class="sxs-lookup"><span data-stu-id="b4f39-163">Example usage: <strong>/INSTALLDIR=C:\Program Files\AppV Client</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="b4f39-164">/CEIPOPTIN</span><span class="sxs-lookup"><span data-stu-id="b4f39-164">/CEIPOPTIN</span></span></p></td>
   <td align="left"><p><span data-ttu-id="b4f39-165">Permet de participer au programme d’amélioration du produit.</span><span class="sxs-lookup"><span data-stu-id="b4f39-165">Enables participation in the Customer Experience Improvement Program.</span></span> <span data-ttu-id="b4f39-166">Exemple d’utilisation: <strong> /CEIPOPTIN = [0 | 1]</span><span class="sxs-lookup"><span data-stu-id="b4f39-166">Example usage: <strong>/CEIPOPTIN=[0|1]</span></span></strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="b4f39-167">/MUOPTIN</span><span class="sxs-lookup"><span data-stu-id="b4f39-167">/MUOPTIN</span></span></p></td>
   <td align="left"><p><span data-ttu-id="b4f39-168">Active Microsoft Update.</span><span class="sxs-lookup"><span data-stu-id="b4f39-168">Enables Microsoft Update.</span></span> <span data-ttu-id="b4f39-169">Exemple d’utilisation: <strong> /MUOPTIN = [0 | 1]</span><span class="sxs-lookup"><span data-stu-id="b4f39-169">Example usage: <strong>/MUOPTIN=[0|1]</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="b4f39-170">/PACKAGEINSTALLATIONROOT</span><span class="sxs-lookup"><span data-stu-id="b4f39-170">/PACKAGEINSTALLATIONROOT</span></span></p></td>
   <td align="left"><p><span data-ttu-id="b4f39-171">Spécifie le répertoire dans lequel installer toutes les nouvelles applications et mises à jour.</span><span class="sxs-lookup"><span data-stu-id="b4f39-171">Specifies the directory in which to install all new applications and updates.</span></span> <span data-ttu-id="b4f39-172">Exemple d’utilisation: <strong> /PACKAGEINSTALLATIONROOT =&#39;C:\App-V Packages&#39;</span><span class="sxs-lookup"><span data-stu-id="b4f39-172">Example usage: <strong>/PACKAGEINSTALLATIONROOT=&#39;C:\App-V Packages&#39;</span></span></strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="b4f39-173">/PACKAGESOURCEROOT</span><span class="sxs-lookup"><span data-stu-id="b4f39-173">/PACKAGESOURCEROOT</span></span></p></td>
   <td align="left"><p><span data-ttu-id="b4f39-174">Remplace l’emplacement source pour le téléchargement du contenu du package.</span><span class="sxs-lookup"><span data-stu-id="b4f39-174">Overrides the source location for downloading package content.</span></span> <span data-ttu-id="b4f39-175">Exemple d’utilisation: <strong> /PACKAGESOURCEROOT =&#39;<a href="http://packageStore" data-raw-source="http://packageStore"> http://packageStore </a>&#39;</span><span class="sxs-lookup"><span data-stu-id="b4f39-175">Example usage: <strong>/PACKAGESOURCEROOT=&#39;<a href="http://packageStore" data-raw-source="http://packageStore">http://packageStore</a>&#39;</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="b4f39-176">/AUTOLOAD</span><span class="sxs-lookup"><span data-stu-id="b4f39-176">/AUTOLOAD</span></span></p></td>
   <td align="left"><p><span data-ttu-id="b4f39-177">Spécifie la façon dont les nouveaux packages sont chargés par App-V 5,1 sur un ordinateur spécifique.</span><span class="sxs-lookup"><span data-stu-id="b4f39-177">Specifies how new packages will be loaded by App-V 5.1 on a specific computer.</span></span> <span data-ttu-id="b4f39-178">Les options suivantes sont activées: [1]; Chargez automatiquement tous les packages [2]; ou ne chargez pas automatiquement les packages [0]. <strong> Exemple d’utilisation:/AUTOLOAD = [0 | 1 | 2]</span><span class="sxs-lookup"><span data-stu-id="b4f39-178">The following options are enabled: [1]; automatically load all packages [2]; or automatically load no packages [0].<strong>Example usage: /AUTOLOAD=[0|1|2]</span></span></strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="b4f39-179">/SHAREDCONTENTSTOREMODE</span><span class="sxs-lookup"><span data-stu-id="b4f39-179">/SHAREDCONTENTSTOREMODE</span></span></p></td>
   <td align="left"><p><span data-ttu-id="b4f39-180">Spécifie que le contenu du package en flux ne sera pas enregistré sur le disque dur local.</span><span class="sxs-lookup"><span data-stu-id="b4f39-180">Specifies that streamed package contents will be not be saved to the local hard disk.</span></span> <span data-ttu-id="b4f39-181">Exemple d’utilisation: <strong> /SHAREDCONTENTSTOREMODE = [0 | 1]</span><span class="sxs-lookup"><span data-stu-id="b4f39-181">Example usage: <strong>/SHAREDCONTENTSTOREMODE=[0|1]</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="b4f39-182">/MIGRATIONMODE</span><span class="sxs-lookup"><span data-stu-id="b4f39-182">/MIGRATIONMODE</span></span></p></td>
   <td align="left"><p><span data-ttu-id="b4f39-183">Permet au client App-V 5,1 de modifier les raccourcis et FTAs associés aux packages créés avec une version précédente.</span><span class="sxs-lookup"><span data-stu-id="b4f39-183">Allows the App-V 5.1 client to modify the shortcuts and FTAs that are associated with the packages that are created with a previous version.</span></span> <span data-ttu-id="b4f39-184">Exemple d’utilisation: <strong> /MIGRATIONMODE = [0 | 1]</span><span class="sxs-lookup"><span data-stu-id="b4f39-184">Example usage: <strong>/MIGRATIONMODE=[0|1]</span></span></strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="b4f39-185">/ENABLEPACKAGESCRIPTS</span><span class="sxs-lookup"><span data-stu-id="b4f39-185">/ENABLEPACKAGESCRIPTS</span></span></p></td>
   <td align="left"><p><span data-ttu-id="b4f39-186">Active les scripts qui sont définis dans le fichier manifeste de package ou les fichiers de configuration qui doivent s’exécuter.</span><span class="sxs-lookup"><span data-stu-id="b4f39-186">Enables the scripts that are defined in the package manifest file or configuration files that should run.</span></span> <span data-ttu-id="b4f39-187">Exemple d’utilisation: <strong> /ENABLEPACKAGESCRIPTS = [0 | 1]</span><span class="sxs-lookup"><span data-stu-id="b4f39-187">Example usage: <strong>/ENABLEPACKAGESCRIPTS=[0|1]</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="b4f39-188">/ROAMINGREGISTRYEXCLUSIONS</span><span class="sxs-lookup"><span data-stu-id="b4f39-188">/ROAMINGREGISTRYEXCLUSIONS</span></span></p></td>
   <td align="left"><p><span data-ttu-id="b4f39-189">Spécifie les chemins de Registre qui ne sont pas itinérants avec un profil utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b4f39-189">Specifies the registry paths that will not roam with a user profile.</span></span> <span data-ttu-id="b4f39-190">Exemple d’utilisation: <strong> /ROAMINGREGISTRYEXCLUSIONS = software\classes; software\clients</span><span class="sxs-lookup"><span data-stu-id="b4f39-190">Example usage: <strong>/ROAMINGREGISTRYEXCLUSIONS=software\classes;software\clients</span></span></strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="b4f39-191">/ROAMINGFILEEXCLUSIONS</span><span class="sxs-lookup"><span data-stu-id="b4f39-191">/ROAMINGFILEEXCLUSIONS</span></span></p></td>
   <td align="left"><p><span data-ttu-id="b4f39-192">Spécifie les chemins d’accès relatifs au fichier% UserProfile% qui ne sont pas itinérants avec un profil utilisateur&#39;s.</span><span class="sxs-lookup"><span data-stu-id="b4f39-192">Specifies the file paths relative to %userprofile% that do not roam with a user&#39;s profile.</span></span> <span data-ttu-id="b4f39-193">Exemple d’utilisation: <strong> /ROAMINGFILEEXCLUSIONS &#39;ordinateur de bureau; mes images&#39;</span><span class="sxs-lookup"><span data-stu-id="b4f39-193">Example usage: <strong>/ROAMINGFILEEXCLUSIONS &#39;desktop;my pictures&#39;</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="b4f39-194">/S [1-5] PUBLISHINGSERVERNAME</span><span class="sxs-lookup"><span data-stu-id="b4f39-194">/S[1-5]PUBLISHINGSERVERNAME</span></span></p></td>
   <td align="left"><p><span data-ttu-id="b4f39-195">Affiche le nom du serveur de publication.</span><span class="sxs-lookup"><span data-stu-id="b4f39-195">Displays the name of the publishing server.</span></span> <span data-ttu-id="b4f39-196">Exemple d’utilisation: <strong> /S2PUBLISHINGSERVERNAME = MyPublishingServer</span><span class="sxs-lookup"><span data-stu-id="b4f39-196">Example usage: <strong>/S2PUBLISHINGSERVERNAME=MyPublishingServer</span></span></strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="b4f39-197">/S [1-5] PUBLISHINGSERVERURL</span><span class="sxs-lookup"><span data-stu-id="b4f39-197">/S[1-5]PUBLISHINGSERVERURL</span></span></p></td>
   <td align="left"><p><span data-ttu-id="b4f39-198">Affiche l’URL du serveur de publication.</span><span class="sxs-lookup"><span data-stu-id="b4f39-198">Displays the URL of the publishing server.</span></span> <span data-ttu-id="b4f39-199">Exemple d’utilisation: <strong> /S2PUBLISHINGSERVERURL = \pubserver</span><span class="sxs-lookup"><span data-stu-id="b4f39-199">Example usage: <strong>/S2PUBLISHINGSERVERURL=\pubserver</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="b4f39-200">/S [1-5] GLOBALREFRESHENABLED-</span><span class="sxs-lookup"><span data-stu-id="b4f39-200">/S[1-5]GLOBALREFRESHENABLED -</span></span></p></td>
   <td align="left"><p><span data-ttu-id="b4f39-201">Autorise une actualisation globale de la publication.</span><span class="sxs-lookup"><span data-stu-id="b4f39-201">Enables a global publishing refresh.</span></span> <span data-ttu-id="b4f39-202">Exemple d’utilisation: <strong> /S2GLOBALREFRESHENABLED = [0 | 1]</span><span class="sxs-lookup"><span data-stu-id="b4f39-202">Example usage: <strong>/S2GLOBALREFRESHENABLED=[0|1]</span></span></strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="b4f39-203">/S [1-5] GLOBALREFRESHONLOGON</span><span class="sxs-lookup"><span data-stu-id="b4f39-203">/S[1-5]GLOBALREFRESHONLOGON</span></span></p></td>
   <td align="left"><p><span data-ttu-id="b4f39-204">Lance une actualisation globale de la publication lors de la connexion d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b4f39-204">Initiates a global publishing refresh when a user logs on.</span></span> <span data-ttu-id="b4f39-205">Exemple d’utilisation: <strong> /S2LOGONREFRESH = [0 | 1]</span><span class="sxs-lookup"><span data-stu-id="b4f39-205">Example usage: <strong>/S2LOGONREFRESH=[0|1]</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="b4f39-206">/S [1-5] GLOBALREFRESHINTERVAL-</span><span class="sxs-lookup"><span data-stu-id="b4f39-206">/S[1-5]GLOBALREFRESHINTERVAL -</span></span></p></td>
   <td align="left"><p><span data-ttu-id="b4f39-207">Spécifie l’intervalle d’actualisation de publication, où <strong> 0 </strong> indique ne pas actualiser régulièrement.</span><span class="sxs-lookup"><span data-stu-id="b4f39-207">Specifies the publishing refresh interval, where <strong>0</strong> indicates do not periodically refresh.</span></span> <span data-ttu-id="b4f39-208">Exemple d’utilisation: <strong> /S2PERIODICREFRESHINTERVAL = [0-744]</span><span class="sxs-lookup"><span data-stu-id="b4f39-208">Example usage: <strong>/S2PERIODICREFRESHINTERVAL=[0-744]</span></span></strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="b4f39-209">/S [1-5] GLOBALREFRESHINTERVALUNIT</span><span class="sxs-lookup"><span data-stu-id="b4f39-209">/S[1-5]GLOBALREFRESHINTERVALUNIT</span></span></p></td>
   <td align="left"><p><span data-ttu-id="b4f39-210">Spécifie l’unité d’intervalle (heures [0], jours [1]).</span><span class="sxs-lookup"><span data-stu-id="b4f39-210">Specifies the interval unit (Hours[0], Days[1]).</span></span> <span data-ttu-id="b4f39-211">Exemple d’utilisation: <strong> /S2GLOBALREFRESHINTERVALUNIT = [0 | 1]</span><span class="sxs-lookup"><span data-stu-id="b4f39-211">Example usage: <strong>/S2GLOBALREFRESHINTERVALUNIT=[0|1]</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="b4f39-212">/S [1-5] USERREFRESHENABLED</span><span class="sxs-lookup"><span data-stu-id="b4f39-212">/S[1-5]USERREFRESHENABLED</span></span></p></td>
   <td align="left"><p><span data-ttu-id="b4f39-213">Active l’actualisation de la publication.</span><span class="sxs-lookup"><span data-stu-id="b4f39-213">Enables user publishing refresh.</span></span> <span data-ttu-id="b4f39-214">Exemple d’utilisation: <strong> /S2USERREFRESHENABLED = [0 | 1]</span><span class="sxs-lookup"><span data-stu-id="b4f39-214">Example usage: <strong>/S2USERREFRESHENABLED=[0|1]</span></span></strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="b4f39-215">/S [1-5] USERREFRESHONLOGON</span><span class="sxs-lookup"><span data-stu-id="b4f39-215">/S[1-5]USERREFRESHONLOGON</span></span></p></td>
   <td align="left"><p><span data-ttu-id="b4f39-216">Lance une actualisation de la publication des utilisateurs quand un utilisateur se connecte.</span><span class="sxs-lookup"><span data-stu-id="b4f39-216">Initiates a user publishing refresh when a user logs on.</span></span> <span data-ttu-id="b4f39-217">Exemple d’utilisation: <strong> /S2LOGONREFRESH = [0 | 1]</span><span class="sxs-lookup"><span data-stu-id="b4f39-217">Example usage: <strong>/S2LOGONREFRESH=[0|1]</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="b4f39-218">/S [1-5] USERREFRESHINTERVAL-</span><span class="sxs-lookup"><span data-stu-id="b4f39-218">/S[1-5]USERREFRESHINTERVAL -</span></span></p></td>
   <td align="left"><p><span data-ttu-id="b4f39-219">Spécifie l’intervalle d’actualisation de publication, où <strong> 0 </strong> indique ne pas actualiser régulièrement.</span><span class="sxs-lookup"><span data-stu-id="b4f39-219">Specifies the publishing refresh interval, where <strong>0</strong> indicates do not periodically refresh.</span></span> <span data-ttu-id="b4f39-220">Exemple d’utilisation: <strong> /S2PERIODICREFRESHINTERVAL = [0-744]</span><span class="sxs-lookup"><span data-stu-id="b4f39-220">Example usage: <strong>/S2PERIODICREFRESHINTERVAL=[0-744]</span></span></strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="b4f39-221">/S [1-5] USERREFRESHINTERVALUNIT</span><span class="sxs-lookup"><span data-stu-id="b4f39-221">/S[1-5]USERREFRESHINTERVALUNIT</span></span></p></td>
   <td align="left"><p><span data-ttu-id="b4f39-222">Spécifie l’unité d’intervalle (heures [0], jours [1]).</span><span class="sxs-lookup"><span data-stu-id="b4f39-222">Specifies the interval unit (Hours[0], Days[1]).</span></span> <span data-ttu-id="b4f39-223">Exemple d’utilisation: <strong> /S2USERREFRESHINTERVALUNIT = [0 | 1]</span><span class="sxs-lookup"><span data-stu-id="b4f39-223">Example usage: <strong>/S2USERREFRESHINTERVALUNIT=[0|1]</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="b4f39-224">/Log</span><span class="sxs-lookup"><span data-stu-id="b4f39-224">/Log</span></span></p></td>
   <td align="left"><p><span data-ttu-id="b4f39-225">Spécifie un emplacement où les informations du journal sont enregistrées.</span><span class="sxs-lookup"><span data-stu-id="b4f39-225">Specifies a location where the log information is saved.</span></span> <span data-ttu-id="b4f39-226">L’emplacement par défaut est% Temp%.</span><span class="sxs-lookup"><span data-stu-id="b4f39-226">The default location is %Temp%.</span></span> <span data-ttu-id="b4f39-227">Exemple d’utilisation: <strong> /log C:\logs\log.log</span><span class="sxs-lookup"><span data-stu-id="b4f39-227">Example usage: <strong>/log C:\logs\log.log</span></span></strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="b4f39-228">établit</span><span class="sxs-lookup"><span data-stu-id="b4f39-228">/q</span></span></p></td>
   <td align="left"><p><span data-ttu-id="b4f39-229">Spécifie une installation sans assistance.</span><span class="sxs-lookup"><span data-stu-id="b4f39-229">Specifies an unattended installation.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="b4f39-230">/REPAIR</span><span class="sxs-lookup"><span data-stu-id="b4f39-230">/REPAIR</span></span></p></td>
   <td align="left"><p><span data-ttu-id="b4f39-231">Répare une installation précédente d’un client.</span><span class="sxs-lookup"><span data-stu-id="b4f39-231">Repairs a previous client installation.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="b4f39-232">/NORESTART</span><span class="sxs-lookup"><span data-stu-id="b4f39-232">/NORESTART</span></span></p></td>
   <td align="left"><p><span data-ttu-id="b4f39-233">Empêche l’ordinateur de redémarrer après l’installation du client.</span><span class="sxs-lookup"><span data-stu-id="b4f39-233">Prevents the computer from rebooting after the client installation.</span></span></p>
   <p><span data-ttu-id="b4f39-234">Ce paramètre empêche l’ordinateur de l’utilisateur final de redémarrer après l’installation de chaque mise à jour et vous permet de planifier le redémarrage à votre convenance.</span><span class="sxs-lookup"><span data-stu-id="b4f39-234">The parameter prevents the end-user computer from rebooting after each update is installed and lets you schedule the reboot at your convenience.</span></span> <span data-ttu-id="b4f39-235">Par exemple, vous pouvez installer App-V 5,1, puis installer le package de correctif Y sans redémarrer après l’installation du Service Pack.</span><span class="sxs-lookup"><span data-stu-id="b4f39-235">For example, you can install App-V 5.1 and then install Hotfix Package Y without rebooting after the Service Pack installation.</span></span> <span data-ttu-id="b4f39-236">Après l’installation, vous devez redémarrer avant de commencer à utiliser App-V.</span><span class="sxs-lookup"><span data-stu-id="b4f39-236">After the installation, you must reboot before you start using App-V.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="b4f39-237">/UNINSTALL</span><span class="sxs-lookup"><span data-stu-id="b4f39-237">/UNINSTALL</span></span></p></td>
   <td align="left"><p><span data-ttu-id="b4f39-238">Désinstalle le client.</span><span class="sxs-lookup"><span data-stu-id="b4f39-238">Uninstalls the client.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="b4f39-239">/ACCEPTEULA</span><span class="sxs-lookup"><span data-stu-id="b4f39-239">/ACCEPTEULA</span></span></p></td>
   <td align="left"><p><span data-ttu-id="b4f39-240">Accepter le contrat de licence.</span><span class="sxs-lookup"><span data-stu-id="b4f39-240">Accepts the license agreement.</span></span> <span data-ttu-id="b4f39-241">Ce type de fichier est requis pour une installation sans assistance.</span><span class="sxs-lookup"><span data-stu-id="b4f39-241">This is required for an unattended installation.</span></span> <span data-ttu-id="b4f39-242">Exemple d’utilisation: <strong> /AcceptEULA </strong> ou <strong> /ACCEPTEULA = 1 </strong> .</span><span class="sxs-lookup"><span data-stu-id="b4f39-242">Example usage: <strong>/ACCEPTEULA</strong> or <strong>/ACCEPTEULA=1</strong>.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="b4f39-243">/LAYOUT</span><span class="sxs-lookup"><span data-stu-id="b4f39-243">/LAYOUT</span></span></p></td>
   <td align="left"><p><span data-ttu-id="b4f39-244">Spécifie l’action de disposition associée.</span><span class="sxs-lookup"><span data-stu-id="b4f39-244">Specifies the associated layout action.</span></span> <span data-ttu-id="b4f39-245">Il extrait également les fichiers Windows Installer (. msi) et script dans un dossier sans installer App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="b4f39-245">It also extracts the Windows Installer (.msi) and script files to a folder without installing App-V 5.1.</span></span> <span data-ttu-id="b4f39-246">Aucune valeur n’est attendue.</span><span class="sxs-lookup"><span data-stu-id="b4f39-246">No value is expected.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="b4f39-247">/LAYOUTDIR</span><span class="sxs-lookup"><span data-stu-id="b4f39-247">/LAYOUTDIR</span></span></p></td>
   <td align="left"><p><span data-ttu-id="b4f39-248">Spécifie le répertoire de disposition.</span><span class="sxs-lookup"><span data-stu-id="b4f39-248">Specifies the layout directory.</span></span> <span data-ttu-id="b4f39-249">Nécessite une valeur de chaîne.</span><span class="sxs-lookup"><span data-stu-id="b4f39-249">Requires a string value.</span></span> <span data-ttu-id="b4f39-250">Exemple d’utilisation: <strong> /LAYOUTDIR = «client de virtualisation C:\Application» </strong> .</span><span class="sxs-lookup"><span data-stu-id="b4f39-250">Example usage: <strong>/LAYOUTDIR=”C:\Application Virtualization Client”</strong>.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="b4f39-251">/?,/h,/Help</span><span class="sxs-lookup"><span data-stu-id="b4f39-251">/?, /h, /help</span></span></p></td>
   <td align="left"><p><span data-ttu-id="b4f39-252">Demande des informations sur les paramètres d’installation précédents.</span><span class="sxs-lookup"><span data-stu-id="b4f39-252">Requests help about the previous installation parameters.</span></span></p></td>
   </tr>
   </tbody>
   </table>



**<span data-ttu-id="b4f39-253">Pour installer le client App-V 5,1 à l’aide du fichier Windows Installer (. msi)</span><span class="sxs-lookup"><span data-stu-id="b4f39-253">To install the App-V 5.1 client by using the Windows Installer (.msi) file</span></span>**

1.  <span data-ttu-id="b4f39-254">Installez les prérequis requis sur les ordinateurs cibles.</span><span class="sxs-lookup"><span data-stu-id="b4f39-254">Install the required prerequisites on the target computers.</span></span> <span data-ttu-id="b4f39-255">Apprenez [à faire avant de commencer](#bkmk-clt-install-prereqs).</span><span class="sxs-lookup"><span data-stu-id="b4f39-255">See [What to do before you start](#bkmk-clt-install-prereqs).</span></span> <span data-ttu-id="b4f39-256">Si une configuration requise n’est pas respectée, l’installation échoue.</span><span class="sxs-lookup"><span data-stu-id="b4f39-256">If any prerequisites are not met, the installation will fail.</span></span>

2.  <span data-ttu-id="b4f39-257">Assurez-vous que les ordinateurs cibles ne disposent pas de redémarrages en attente avant de procéder à l’installation du client à l’aide des fichiers App-V 5,1 Windows Installer (. msi).</span><span class="sxs-lookup"><span data-stu-id="b4f39-257">Ensure that the target computers do not have any pending restarts before you install the client using the App-V 5.1 Windows Installer (.msi) files.</span></span> <span data-ttu-id="b4f39-258">Les fichiers Windows Installer n’indicateur pas de redémarrage en attente.</span><span class="sxs-lookup"><span data-stu-id="b4f39-258">The Windows Installer files do not flag a pending restart.</span></span>

3.  <span data-ttu-id="b4f39-259">Déploiement de l’un des fichiers Windows Installer suivants sur l’ordinateur cible.</span><span class="sxs-lookup"><span data-stu-id="b4f39-259">Deploy one of the following Windows Installer files to the target computer.</span></span> <span data-ttu-id="b4f39-260">Le fichier que vous spécifiez doit correspondre à la configuration de l’ordinateur cible.</span><span class="sxs-lookup"><span data-stu-id="b4f39-260">The file that you specify must match the configuration of the target computer.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="b4f39-261">Type de déploiement</span><span class="sxs-lookup"><span data-stu-id="b4f39-261">Type of deployment</span></span></th>
    <th align="left"><span data-ttu-id="b4f39-262">Déployer ce fichier</span><span class="sxs-lookup"><span data-stu-id="b4f39-262">Deploy this file</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="b4f39-263">Un ordinateur exécute un système d’exploitation Microsoft Windows 32 bits</span><span class="sxs-lookup"><span data-stu-id="b4f39-263">Computer is running a 32-bit Microsoft Windows operating system</span></span></p></td>
    <td align="left"><p><span data-ttu-id="b4f39-264">appv_client_MSI_x86.msi</span><span class="sxs-lookup"><span data-stu-id="b4f39-264">appv_client_MSI_x86.msi</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="b4f39-265">Un ordinateur exécute un système d’exploitation Microsoft Windows 64 bits</span><span class="sxs-lookup"><span data-stu-id="b4f39-265">Computer is running a 64-bit Microsoft Windows operating system</span></span></p></td>
    <td align="left"><p><span data-ttu-id="b4f39-266">appv_client_MSI_x64.msi</span><span class="sxs-lookup"><span data-stu-id="b4f39-266">appv_client_MSI_x64.msi</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="b4f39-267">Vous déployez le client App-V 5,1 Remote Desktop Services</span><span class="sxs-lookup"><span data-stu-id="b4f39-267">You are deploying the App-V 5.1 Remote Desktop Services client</span></span></p></td>
    <td align="left"><p><span data-ttu-id="b4f39-268">appv_client_rds_MSI_x64.msi</span><span class="sxs-lookup"><span data-stu-id="b4f39-268">appv_client_rds_MSI_x64.msi</span></span></p></td>
    </tr>
    </tbody>
    </table>



4.  <span data-ttu-id="b4f39-269">En utilisant les informations figurant dans le tableau suivant, sélectionnez le module linguistique approprié **. msi** à installer en fonction de la langue souhaitée pour l’ordinateur cible.</span><span class="sxs-lookup"><span data-stu-id="b4f39-269">Using the information in the following table, select the appropriate language pack **.msi** to install, based on the desired language for the target computer.</span></span> <span data-ttu-id="b4f39-270">Les **xxxx** du tableau font référence aux paramètres régionaux cibles du module linguistique.</span><span class="sxs-lookup"><span data-stu-id="b4f39-270">The **xxxx** in the table refers to the target locale of the language pack.</span></span>

    **<span data-ttu-id="b4f39-271">Ce que vous devez savoir avant de commencer:</span><span class="sxs-lookup"><span data-stu-id="b4f39-271">What to know before you start:</span></span>**

    -   <span data-ttu-id="b4f39-272">Les modules linguistiques sont communs au client App-V 5,1 standard et à la version Service Bureau à distance du client App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="b4f39-272">The language packs are common to both the standard App-V 5.1 client and the Remote Desktop Services version of the App-V 5.1 client.</span></span>

    -   <span data-ttu-id="b4f39-273">Si vous installez le client App-V 5,1 à l’aide du fichier **. exe**, le programme d’installation déploiera uniquement le module linguistique correspondant au système d’exploitation exécuté sur l’ordinateur cible.</span><span class="sxs-lookup"><span data-stu-id="b4f39-273">If you install the App-V 5.1 client using the **.exe**, the installer will deploy only the language pack that matches the operating system running on the target computer.</span></span>

    -   <span data-ttu-id="b4f39-274">Pour déployer des modules linguistiques supplémentaires sur un ordinateur cible, utilisez la procédure **d’installation du client App-V 5,1 à l’aide du fichier Windows Installer (. msi)**.</span><span class="sxs-lookup"><span data-stu-id="b4f39-274">To deploy additional language packs on a target computer, use the procedure **To install the App-V 5.1 client by using Windows Installer (.msi) file**.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="b4f39-275">Type de déploiement</span><span class="sxs-lookup"><span data-stu-id="b4f39-275">Type of deployment</span></span></th>
    <th align="left"><span data-ttu-id="b4f39-276">Déployer ce fichier</span><span class="sxs-lookup"><span data-stu-id="b4f39-276">Deploy this file</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="b4f39-277">Un ordinateur exécute un système d’exploitation Microsoft Windows 32 bits</span><span class="sxs-lookup"><span data-stu-id="b4f39-277">Computer is running a 32-bit Microsoft Windows operating system</span></span></p></td>
    <td align="left"><p><span data-ttu-id="b4f39-278">x86.msi appv_client_LP_xxxx_</span><span class="sxs-lookup"><span data-stu-id="b4f39-278">appv_client_LP_xxxx_ x86.msi</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="b4f39-279">Un ordinateur exécute un système d’exploitation Microsoft Windows 64 bits</span><span class="sxs-lookup"><span data-stu-id="b4f39-279">Computer is running a 64-bit Microsoft Windows operating system</span></span></p></td>
    <td align="left"><p><span data-ttu-id="b4f39-280">x64.msi appv_client_LP_xxxx_</span><span class="sxs-lookup"><span data-stu-id="b4f39-280">appv_client_LP_xxxx_ x64.msi</span></span></p></td>
    </tr>
    </tbody>
    </table>



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## <span data-ttu-id="b4f39-281">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b4f39-281">Related topics</span></span>


[<span data-ttu-id="b4f39-282">Déploiement d'App-V5.1</span><span class="sxs-lookup"><span data-stu-id="b4f39-282">Deploying App-V 5.1</span></span>](deploying-app-v-51.md)

[<span data-ttu-id="b4f39-283">À propos des paramètres de configuration du client</span><span class="sxs-lookup"><span data-stu-id="b4f39-283">About Client Configuration Settings</span></span>](about-client-configuration-settings51.md)

[<span data-ttu-id="b4f39-284">Désinstallation d'App-V5.1 Client</span><span class="sxs-lookup"><span data-stu-id="b4f39-284">How to Uninstall the App-V 5.1 Client</span></span>](how-to-uninstall-the-app-v-51-client.md)









