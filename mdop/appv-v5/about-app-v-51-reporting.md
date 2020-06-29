---
title: À propos de la création de rapports d'App-V5.1
description: À propos de la création de rapports d'App-V5.1
author: dansimp
ms.assetid: 385dca00-7178-4e35-8d86-c58867ebd65c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 827343d538238ca638b57a74ae5d2d74bc6c5968
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806113"
---
# <span data-ttu-id="57ea5-103">À propos de la création de rapports d'App-V5.1</span><span class="sxs-lookup"><span data-stu-id="57ea5-103">About App-V 5.1 Reporting</span></span>

<span data-ttu-id="57ea5-104">Microsoft Application Virtualization (App-V) 5,1 inclut une fonctionnalité de création de rapports intégrée qui vous permet de collecter des informations sur les ordinateurs exécutant le client App-V 5,1 ainsi que des informations sur l’utilisation des packages d’applications virtuelles.</span><span class="sxs-lookup"><span data-stu-id="57ea5-104">Microsoft Application Virtualization (App-V) 5.1 includes a built-in reporting feature that helps you collect information about computers running the App-V 5.1 client as well as information about virtual application package usage.</span></span> <span data-ttu-id="57ea5-105">Vous pouvez utiliser ces informations pour générer des rapports à partir d’une base de données centralisée.</span><span class="sxs-lookup"><span data-stu-id="57ea5-105">You can use this information to generate reports from a centralized database.</span></span>

## <a href="" id="---------app-v-5-1-reporting-overview"></a> <span data-ttu-id="57ea5-106">Présentation de la création de rapports App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="57ea5-106">App-V 5.1 Reporting Overview</span></span>

<span data-ttu-id="57ea5-107">La liste suivante présente le flux de travail de haut en bas pour la création de rapports dans App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="57ea5-107">The following list displays the end–to-end high-level workflow for reporting in App-V 5.1.</span></span>

1. <span data-ttu-id="57ea5-108">Le serveur de création de rapports App-V 5,1 comporte les conditions préalables suivantes:</span><span class="sxs-lookup"><span data-stu-id="57ea5-108">The App-V 5.1 Reporting server has the following prerequisites:</span></span>

    - <span data-ttu-id="57ea5-109">Rôle du serveur Web Internet Information Services (IIS)</span><span class="sxs-lookup"><span data-stu-id="57ea5-109">Internet Information Service (IIS) web server role</span></span>

    - <span data-ttu-id="57ea5-110">Rôle d’authentification Windows (sous **IIS/sécurité**)</span><span class="sxs-lookup"><span data-stu-id="57ea5-110">Windows Authentication role (under **IIS / Security**)</span></span>

    - <span data-ttu-id="57ea5-111">SQL Server installé et exécuté avec SQL Server Reporting Services (SSRS)</span><span class="sxs-lookup"><span data-stu-id="57ea5-111">SQL Server installed and running with SQL Server Reporting Services (SSRS)</span></span>

    <span data-ttu-id="57ea5-112">Pour vérifier que SQL Server Reporting Services est en cours d’exécution, affichez- `http://localhost/Reports` le dans un navigateur Web en tant qu’administrateur sur le serveur qui héberge la création de rapports App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="57ea5-112">To confirm SQL Server Reporting Services is running, view `http://localhost/Reports` in a web browser as administrator on the server that will host App-V 5.1 Reporting.</span></span> <span data-ttu-id="57ea5-113">La page d’accueil de SQL Server Reporting Services doit s’afficher.</span><span class="sxs-lookup"><span data-stu-id="57ea5-113">The SQL Server Reporting Services Home page should display.</span></span>

2. <span data-ttu-id="57ea5-114">Installez le serveur de rapports App-V 5,1 et la base de données associée.</span><span class="sxs-lookup"><span data-stu-id="57ea5-114">Install the App-V 5.1 reporting server and associated database.</span></span> <span data-ttu-id="57ea5-115">Pour plus d’informations sur l’installation de Report Server [, voir comment installer le serveur de création de rapports sur un ordinateur autonome et le connecter à la base de données](how-to-install-the-reporting-server-on-a-standalone-computer-and-connect-it-to-the-database51.md).</span><span class="sxs-lookup"><span data-stu-id="57ea5-115">For more information about installing the reporting server see [How to install the Reporting Server on a Standalone Computer and Connect it to the Database](how-to-install-the-reporting-server-on-a-standalone-computer-and-connect-it-to-the-database51.md).</span></span> <span data-ttu-id="57ea5-116">Configurez le moment où l’ordinateur exécutant le client App-V 5,1 doit envoyer des données au serveur de rapports.</span><span class="sxs-lookup"><span data-stu-id="57ea5-116">Configure the time when the computer running the App-V 5.1 client should send data to the reporting server.</span></span>

3. <span data-ttu-id="57ea5-117">Si vous n’utilisez pas un système électronique de distribution de logiciels tel que Configuration Manager pour afficher les rapports, vous pouvez définir des rapports dans SQL Server Reporting Service.</span><span class="sxs-lookup"><span data-stu-id="57ea5-117">If you are not using an electronic software distribution system such as Configuration Manager to view reports then you can define reports in SQL Server Reporting Service.</span></span> <span data-ttu-id="57ea5-118">Téléchargez des rapports SSRS prédéfinis à partir du [Centre de téléchargement](https://go.microsoft.com/fwlink/?LinkId=397255).</span><span class="sxs-lookup"><span data-stu-id="57ea5-118">Download predefined SSRS Reports from the [Download Center](https://go.microsoft.com/fwlink/?LinkId=397255).</span></span>

    > [!NOTE]
    > <span data-ttu-id="57ea5-119">Si vous utilisez l’intégration de Configuration Manager avec App-V 5,1, la plupart des rapports sont générés à partir de Configuration Manager plutôt que d’App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="57ea5-119">If you are using the Configuration Manager integration with App-V 5.1, most reports are generated from Configuration Manager rather than from App-V 5.1.</span></span>

4. <span data-ttu-id="57ea5-120">Après avoir importé le module App-V 5,1 PowerShell en `Import-Module AppvClient` tant qu’administrateur, activez le client App-v 5,1.</span><span class="sxs-lookup"><span data-stu-id="57ea5-120">After importing the App-V 5.1 PowerShell module using `Import-Module AppvClient` as administrator, enable the App-V 5.1 client.</span></span> <span data-ttu-id="57ea5-121">Cet exemple de cmdlet PowerShell permet la création de rapports 5,1 App-V:</span><span class="sxs-lookup"><span data-stu-id="57ea5-121">This sample PowerShell cmdlet enables App-V 5.1 reporting:</span></span>

    ```powershell
    Set-AppvClientConfiguration –reportingserverurl <url>:<port> -reportingenabled 1 – ReportingStartTime <0-23> - ReportingRandomDelay <#min>
    ```

    <span data-ttu-id="57ea5-122">Pour envoyer immédiatement les données du rapport App-V 5,1, exécutez `Send-AppvClientReport` le client App-v 5,1.</span><span class="sxs-lookup"><span data-stu-id="57ea5-122">To immediately send App-V 5.1 report data, run `Send-AppvClientReport` on the App-V 5.1 client.</span></span>

    <span data-ttu-id="57ea5-123">Pour plus d’informations sur l’installation du client App-V 5,1 avec la création de rapports activée, voir [à propos des paramètres de configuration du client](about-client-configuration-settings51.md).</span><span class="sxs-lookup"><span data-stu-id="57ea5-123">For more information about installing the App-V 5.1 client with reporting enabled see [About Client Configuration Settings](about-client-configuration-settings51.md).</span></span> <span data-ttu-id="57ea5-124">Pour gérer la création de rapports App-V 5,1 avec Windows PowerShell, reportez-vous [à la rubrique activation de la création de rapports sur le client App-v 5,1 à l’aide de PowerShell](how-to-enable-reporting-on-the-app-v-51-client-by-using-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="57ea5-124">To administer App-V 5.1 Reporting with Windows PowerShell, see [How to Enable Reporting on the App-V 5.1 Client by Using PowerShell](how-to-enable-reporting-on-the-app-v-51-client-by-using-powershell.md).</span></span>

5. <span data-ttu-id="57ea5-125">Après que le serveur de création de rapports a reçu les données du client App-V 5,1, il envoie les données à la base de données de création de rapports.</span><span class="sxs-lookup"><span data-stu-id="57ea5-125">After the reporting server receives the data from the App-V 5.1 client it sends the data to the reporting database.</span></span> <span data-ttu-id="57ea5-126">Lorsque la base de données reçoit et traite les données du client, une réponse réussie est envoyée au serveur de création de rapports, puis une notification est envoyée au client App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="57ea5-126">When the database receives and processes the client data, a successful reply is sent to the reporting server and then a notification is sent to the App-V 5.1 client.</span></span>

6. <span data-ttu-id="57ea5-127">Lorsque le client App-V 5,1 reçoit la notification de réussite, il vide le cache des données pour économiser de l’espace.</span><span class="sxs-lookup"><span data-stu-id="57ea5-127">When the App-V 5.1 client receives the success notification, it empties the data cache to conserve space.</span></span>

    > [!NOTE]
    > <span data-ttu-id="57ea5-128">Par défaut, le cache est vidé une fois le serveur confirmant la réception des données.</span><span class="sxs-lookup"><span data-stu-id="57ea5-128">By default the cache is cleared after the server confirms receipt of data.</span></span> <span data-ttu-id="57ea5-129">Vous pouvez configurer manuellement le client pour l’enregistrement du cache de données.</span><span class="sxs-lookup"><span data-stu-id="57ea5-129">You can manually configure the client to save the data cache.</span></span>

<span data-ttu-id="57ea5-130">Si l’appareil du client App-V 5,1 ne reçoit pas de notification de réussite du serveur, il conserve les données dans le cache et tente de renvoyer les données à l’intervalle configuré suivant.</span><span class="sxs-lookup"><span data-stu-id="57ea5-130">If the App-V 5.1 client device does not receive a success notification from the server, it retains data in the cache and tries to resend data at the next configured interval.</span></span> <span data-ttu-id="57ea5-131">Les clients continuent à collecter les données et à l’ajouter au cache.</span><span class="sxs-lookup"><span data-stu-id="57ea5-131">Clients continue to collect data and add it to the cache.</span></span>

### <a href="" id="-------------app-v-5-1-reporting-server-frequently-asked-questions"></a> <span data-ttu-id="57ea5-132">Forum aux questions sur le serveur de création de rapports App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="57ea5-132">App-V 5.1 reporting server frequently asked questions</span></span>

<span data-ttu-id="57ea5-133">Le tableau suivant contient des réponses aux questions fréquemment posées sur la création de rapports App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="57ea5-133">The following table displays answers to common questions about App-V 5.1 reporting</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="57ea5-134">Question</span><span class="sxs-lookup"><span data-stu-id="57ea5-134">Question</span></span></th>
<th align="left"><span data-ttu-id="57ea5-135">Plus d’informations</span><span class="sxs-lookup"><span data-stu-id="57ea5-135">More Information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="57ea5-136">Quelle est la fréquence d’envoi des informations de rapport à la base de données de création de rapports?</span><span class="sxs-lookup"><span data-stu-id="57ea5-136">What is the frequency that reporting information is sent to the reporting database?</span></span></p></td>
<td align="left"><p><span data-ttu-id="57ea5-137">La fréquence dépend du mode de configuration de la tâche de création de rapports sur l’ordinateur exécutant le client App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="57ea5-137">The frequency depends on how the reporting task is configured on the computer running the App-V 5.1 client.</span></span> <span data-ttu-id="57ea5-138">Vous devez configurer la fréquence/l’intervalle d’envoi des données de rapport.</span><span class="sxs-lookup"><span data-stu-id="57ea5-138">You must configure the frequency / interval for sending the reporting data.</span></span> <span data-ttu-id="57ea5-139">Le rapport App-V 5,1 n’est pas activé par défaut.</span><span class="sxs-lookup"><span data-stu-id="57ea5-139">App-V 5.1 Reporting is not enabled by default.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="57ea5-140">Quelles informations sont stockées dans la base de données du serveur de rapports?</span><span class="sxs-lookup"><span data-stu-id="57ea5-140">What information is stored in the reporting server database?</span></span></p></td>
<td align="left"><p><span data-ttu-id="57ea5-141">La liste suivante indique les éléments stockés dans la base de données de création de rapports:</span><span class="sxs-lookup"><span data-stu-id="57ea5-141">The following list displays what is stored in the reporting database:</span></span></p>
<ul>
<li><p><span data-ttu-id="57ea5-142">Le système d’exploitation exécuté sur l’ordinateur exécutant le client App-V 5,1: nom d’hôte, version, Service Pack, type-client/serveur, architecture du processeur.</span><span class="sxs-lookup"><span data-stu-id="57ea5-142">The operating system running on the computer running the App-V 5.1 client: host name, version, service pack, type - client/server, processor architecture.</span></span></p></li>
<li><p><span data-ttu-id="57ea5-143">Informations sur le client App-V 5,1: version.</span><span class="sxs-lookup"><span data-stu-id="57ea5-143">App-V 5.1 Client information: version.</span></span></p></li>
<li><p><span data-ttu-id="57ea5-144">Liste des packages publiés: GUID, GUID de version, nom.</span><span class="sxs-lookup"><span data-stu-id="57ea5-144">Published package list: GUID, version GUID, name.</span></span></p></li>
<li><p><span data-ttu-id="57ea5-145">Informations sur l’utilisation des applications: nom, version, Streaming Server, utilisateur (DOMAIN\alias), GUID de la version du package, état du lancement et temps d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="57ea5-145">Application usage information: name, version, streaming server, user (domain\alias), package version GUID, launch status and time, shutdown time.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="57ea5-146">Quel est le volume moyen d’informations envoyées au serveur de création de rapports?</span><span class="sxs-lookup"><span data-stu-id="57ea5-146">What is the average volume of information that is sent to the reporting server?</span></span></p></td>
<td align="left"><p><span data-ttu-id="57ea5-147">Ça dépend.</span><span class="sxs-lookup"><span data-stu-id="57ea5-147">It depends.</span></span> <span data-ttu-id="57ea5-148">La liste suivante présente les trois ensembles de données envoyés au serveur de rapports:</span><span class="sxs-lookup"><span data-stu-id="57ea5-148">The following list displays the three sets of the data sent to the reporting server:</span></span></p>
<ol>
<li><p><span data-ttu-id="57ea5-149">Informations sur le système d’exploitation et le client App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="57ea5-149">Operating system, and App-V 5.1 client information.</span></span> <span data-ttu-id="57ea5-150">~ 150 octets, chaque fois que les données sont envoyées.</span><span class="sxs-lookup"><span data-stu-id="57ea5-150">~150 Bytes, every time this data is sent.</span></span></p></li>
<li><p><span data-ttu-id="57ea5-151">Liste de packages publiée.</span><span class="sxs-lookup"><span data-stu-id="57ea5-151">Published package list.</span></span> <span data-ttu-id="57ea5-152">~ 7 Ko pour 30 Packages.</span><span class="sxs-lookup"><span data-stu-id="57ea5-152">~7 KB for 30 packages.</span></span> <span data-ttu-id="57ea5-153">Cette opération est envoyée uniquement lorsque la liste de packages est mise à jour avec une actualisation de publication, qui est exécutée fréquemment. s’il n’y a aucune modification, ces informations ne sont pas envoyées.</span><span class="sxs-lookup"><span data-stu-id="57ea5-153">This is sent only when the package list is updated with a publishing refresh, which is done infrequently; if there is no change, this information is not sent.</span></span></p></li>
<li><p><span data-ttu-id="57ea5-154">Informations sur l’utilisation des applications virtuelles: environ 0,25 Ko par événement.</span><span class="sxs-lookup"><span data-stu-id="57ea5-154">Virtual application usage information – about 0.25KB per event.</span></span> <span data-ttu-id="57ea5-155">Le compte d’ouverture et de fermeture en tant qu’événement s’il se produit avant l’envoi des informations.</span><span class="sxs-lookup"><span data-stu-id="57ea5-155">Opening and closing count as one event if both occur before sending the information.</span></span> <span data-ttu-id="57ea5-156">Lorsque vous envoyez du courrier à l’aide d’une tâche planifiée, seules les données depuis le dernier téléchargement réussi sont envoyées au serveur.</span><span class="sxs-lookup"><span data-stu-id="57ea5-156">When sending using a scheduled task, only the data since the last successful upload is sent to the server.</span></span> <span data-ttu-id="57ea5-157">S’il s’agit d’un envoi manuel par le biais de l’applet de commande PowerShell, il existe un argument facultatif qui contrôle si les données doivent être de nouveau envoyées une nouvelle fois, car cet argument est <strong> DeleteOnSuccess </strong> .</span><span class="sxs-lookup"><span data-stu-id="57ea5-157">If sending manually through the PowerShell cmdlet, there is an optional argument that controls if the data needs to be re-sent next time around – that argument is <strong>DeleteOnSuccess</strong>.</span></span></p>
<p></p>
<p><span data-ttu-id="57ea5-158">Par exemple, si vingt applications sont ouvertes et fermées, et que les informations de rapport doivent être envoyées quotidiennement, le trafic quotidien standard devrait être de 0,15 Ko + 20 x 0,25 Ko ou à propos de 5KB/utilisateur</span><span class="sxs-lookup"><span data-stu-id="57ea5-158">So for example, if twenty applications are opened and closed and reporting information is scheduled to be sent daily, the typical daily traffic should be about 0.15KB + 20 x 0.25KB, or about 5KB/user</span></span></p></li>
</ol></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="57ea5-159">La création de rapports peut-elle être planifiée?</span><span class="sxs-lookup"><span data-stu-id="57ea5-159">Can reporting be scheduled?</span></span></p></td>
<td align="left"><p><span data-ttu-id="57ea5-160">Oui.</span><span class="sxs-lookup"><span data-stu-id="57ea5-160">Yes.</span></span> <span data-ttu-id="57ea5-161">Outre l’envoi manuel de rapports à l’aide d’applets de cmdlet PowerShell ( <strong> Send-AppvClientReport </strong> ), la tâche peut être planifiée pour qu’elle se produise automatiquement.</span><span class="sxs-lookup"><span data-stu-id="57ea5-161">Besides manually sending reporting using PowerShell Cmdlets (<strong>Send-AppvClientReport</strong>), the task can be scheduled so it will happen automatically.</span></span> <span data-ttu-id="57ea5-162">Il existe deux méthodes pour planifier le rapport:</span><span class="sxs-lookup"><span data-stu-id="57ea5-162">There are two ways to schedule the reporting:</span></span></p>
<ol>
<li><p><span data-ttu-id="57ea5-163">Utilisation des cmdlets PowerShell- <strong> Set-AppvClientConfiguration </strong> .</span><span class="sxs-lookup"><span data-stu-id="57ea5-163">Using PowerShell cmdlets - <strong>Set-AppvClientConfiguration</strong>.</span></span> <span data-ttu-id="57ea5-164">Exemple:</span><span class="sxs-lookup"><span data-stu-id="57ea5-164">For example:</span></span></p>
<p><span data-ttu-id="57ea5-165">Set-AppvClientConfiguration-ReportingEnabled 1-ReportingServerURL<a href="http://any.com/appv-reporting" data-raw-source="http://any.com/appv-reporting">http://any.com/appv-reporting</span><span class="sxs-lookup"><span data-stu-id="57ea5-165">Set-AppvClientConfiguration -ReportingEnabled 1 - ReportingServerURL <a href="http://any.com/appv-reporting" data-raw-source="http://any.com/appv-reporting">http://any.com/appv-reporting</span></span></a></p>
<p></p>
<p><span data-ttu-id="57ea5-166">Pour obtenir la liste complète des paramètres de configuration du client, voir <a href="about-client-configuration-settings51.md" data-raw-source="[About Client Configuration Settings](about-client-configuration-settings51.md)"> à propos des paramètres de configuration du client </a> et recherchez les entrées suivantes: <strong> ReportingEnabled </strong> , <strong> ReportingServerURL </strong> , <strong> ReportingDataCacheLimit </strong> , <strong> ReportingDataBlockSize </strong> , <strong> ReportingStartTime </strong> , <strong> ReportingRandomDelay </strong> , <strong> ReportingInterval </strong> .</span><span class="sxs-lookup"><span data-stu-id="57ea5-166">For a complete list of client configuration settings see <a href="about-client-configuration-settings51.md" data-raw-source="[About Client Configuration Settings](about-client-configuration-settings51.md)">About Client Configuration Settings</a> and look for the following entries: <strong>ReportingEnabled</strong>, <strong>ReportingServerURL</strong>, <strong>ReportingDataCacheLimit</strong>, <strong>ReportingDataBlockSize</strong>, <strong>ReportingStartTime</strong>, <strong>ReportingRandomDelay</strong>, <strong>ReportingInterval</strong>.</span></span></p>
<p></p></li>
<li><p><span data-ttu-id="57ea5-167">À l’aide d’une stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="57ea5-167">By using Group Policy.</span></span> <span data-ttu-id="57ea5-168">S’il est distribué à l’aide du contrôleur de domaine, les paramètres sont les mêmes que ceux indiqués précédemment.</span><span class="sxs-lookup"><span data-stu-id="57ea5-168">If distributed using the domain controller, the settings are the same as previously listed.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="57ea5-169">Remarque</span><span class="sxs-lookup"><span data-stu-id="57ea5-169">Note</span></span></strong><br/><p><span data-ttu-id="57ea5-170">Les paramètres de stratégie de groupe remplacent les paramètres locaux configurés à l’aide de PowerShell.</span><span class="sxs-lookup"><span data-stu-id="57ea5-170">Group Policy settings override local settings configured using PowerShell.</span></span></p>
</div>
<div>
</div></li>
</ol></td>
</tr>
</tbody>
</table>

## <a href="" id="---------app-v-5-1-client-reporting"></a> <span data-ttu-id="57ea5-171">Rapports pour les clients App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="57ea5-171">App-V 5.1 Client Reporting</span></span>

<span data-ttu-id="57ea5-172">Pour utiliser la création de rapports App-V 5,1, vous devez installer et configurer le client App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="57ea5-172">To use App-V 5.1 reporting you must install and configure the App-V 5.1 client.</span></span> <span data-ttu-id="57ea5-173">Une fois le client installé, utilisez la cmdlet PowerShell **Set-AppVClientConfiguration** ou le **modèle ADMX** pour configurer la création de rapports.</span><span class="sxs-lookup"><span data-stu-id="57ea5-173">After the client has been installed, use the **Set-AppVClientConfiguration** PowerShell cmdlet or the **ADMX Template** to configure reporting.</span></span> <span data-ttu-id="57ea5-174">Les applets de commande de fonctionnalité de création de rapports sont disponibles en utilisant le lien suivant et sont précédés de **rapports**.</span><span class="sxs-lookup"><span data-stu-id="57ea5-174">The reporting feature cmdlets are available by using the following link and are prefaced by **Reporting**.</span></span> <span data-ttu-id="57ea5-175">Pour obtenir la liste complète des paramètres de configuration du client, voir [à propos des paramètres de configuration du client](about-client-configuration-settings51.md).</span><span class="sxs-lookup"><span data-stu-id="57ea5-175">For a complete list of client configuration settings see [About Client Configuration Settings](about-client-configuration-settings51.md).</span></span> <span data-ttu-id="57ea5-176">La section suivante fournit des exemples de configuration de création de rapports pour les clients App-V 5,1 utilisant PowerShell.</span><span class="sxs-lookup"><span data-stu-id="57ea5-176">The following section provides examples of App-V 5.1 client reporting configuration using PowerShell.</span></span>

### <span data-ttu-id="57ea5-177">Configuration de la création de rapports de clients App-V à l’aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="57ea5-177">Configuring App-V Client reporting using PowerShell</span></span>

<span data-ttu-id="57ea5-178">Les exemples suivants montrent comment les paramètres PowerShell peuvent configurer les fonctionnalités de création de rapports du client App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="57ea5-178">The following examples show how PowerShell parameters can configure the reporting features of the App-V 5.1 client.</span></span>

> [!NOTE]
> <span data-ttu-id="57ea5-179">La tâche de configuration suivante peut également être configurée à l’aide des paramètres de stratégie de groupe dans le modèle ADMX App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="57ea5-179">The following configuration task can also be configured using Group Policy settings in the App-V 5.1 ADMX template.</span></span> <span data-ttu-id="57ea5-180">Pour plus d’informations sur l’utilisation du modèle ADMX, voir modification de la [configuration du client App-V 5,1 à l’aide du modèle ADMX et de la stratégie de groupe](how-to-modify-app-v-51-client-configuration-using-the-admx-template-and-group-policy.md).</span><span class="sxs-lookup"><span data-stu-id="57ea5-180">For more information about using the ADMX template, see [How to Modify App-V 5.1 Client Configuration Using the ADMX Template and Group Policy](how-to-modify-app-v-51-client-configuration-using-the-admx-template-and-group-policy.md).</span></span>

<span data-ttu-id="57ea5-181">**Pour activer les rapports et lancer la collecte de données sur l’ordinateur exécutant le client App-V 5,1**:</span><span class="sxs-lookup"><span data-stu-id="57ea5-181">**To enable reporting and to initiate data collection on the computer running the App-V 5.1 client**:</span></span>

```powershell
Set-AppVClientConfiguration –ReportingEnabled 1
```

<span data-ttu-id="57ea5-182">**Pour configurer le client de manière à envoyer automatiquement des données à un serveur de rapports spécifique**:</span><span class="sxs-lookup"><span data-stu-id="57ea5-182">**To configure the client to automatically send data to a specific reporting server**:</span></span>

```powershell
Set-AppVClientConfiguration –ReportingServerURL http://MyReportingServer:MyPort/ -ReportingStartTime 20 -ReportingInterval 1 -ReportingRandomDelay 30 -ReportingInterval 1 -ReportingRandomDelay 30
```

<span data-ttu-id="57ea5-183">Cet exemple configure le client pour envoyer automatiquement les données de rapport à l’URL du serveur de rapports **http://MyReportingServer:MyPort/** .</span><span class="sxs-lookup"><span data-stu-id="57ea5-183">This example configures the client to automatically send the reporting data to the reporting server URL **http://MyReportingServer:MyPort/**.</span></span> <span data-ttu-id="57ea5-184">De plus, les données de rapport seront envoyées quotidiennement entre 8:00 et 8:30 PM, en fonction du retard aléatoire généré pour la session.</span><span class="sxs-lookup"><span data-stu-id="57ea5-184">Additionally, the reporting data will be sent daily between 8:00 and 8:30 PM, depending on the random delay generated for the session.</span></span>

<span data-ttu-id="57ea5-185">**Pour limiter la taille du cache de données sur le client**:</span><span class="sxs-lookup"><span data-stu-id="57ea5-185">**To limit the size of the data cache on the client**:</span></span>

```powershell
Set-AppvClientConfiguration –ReportingDataCacheLimit 100
```

<span data-ttu-id="57ea5-186">Configure la taille maximale du cache de création de rapports sur l’ordinateur exécutant le client App-V 5,1 sur 100 Mo.</span><span class="sxs-lookup"><span data-stu-id="57ea5-186">Configures the maximum size of the reporting cache on the computer running the App-V 5.1 client to 100 MB.</span></span> <span data-ttu-id="57ea5-187">Si la limite du cache est atteinte avant que les données soient envoyées au serveur, le journal est restauré et les données sont écrasées si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="57ea5-187">If the cache limit is reached before the data is sent to the server, then the log rolls over and data will be overwritten as necessary.</span></span>

<span data-ttu-id="57ea5-188">**Pour configurer la taille du bloc de données transmises sur le réseau entre le client et le serveur**:</span><span class="sxs-lookup"><span data-stu-id="57ea5-188">**To configure the data block size transmitted across the network between the client and the server**:</span></span>

```powershell
Set-AppvClientConfiguration –ReportingDataBlockSize 10240
```

<span data-ttu-id="57ea5-189">Spécifie le bloc de données maximal que le client envoie à 10240 Mo.</span><span class="sxs-lookup"><span data-stu-id="57ea5-189">Specifies the maximum data block that the client sends to 10240 MB.</span></span>

### <span data-ttu-id="57ea5-190">Types de données collectées</span><span class="sxs-lookup"><span data-stu-id="57ea5-190">Types of data collected</span></span>

<span data-ttu-id="57ea5-191">Le tableau suivant répertorie les types d’informations que vous pouvez collecter à l’aide de la création de rapports App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="57ea5-191">The following table displays the types of information you can collect by using App-V 5.1 reporting.</span></span>

|<span data-ttu-id="57ea5-192">Informations client</span><span class="sxs-lookup"><span data-stu-id="57ea5-192">Client Information</span></span>  |<span data-ttu-id="57ea5-193">Informations de package</span><span class="sxs-lookup"><span data-stu-id="57ea5-193">Package Information</span></span>  |<span data-ttu-id="57ea5-194">Utilisation des applications</span><span class="sxs-lookup"><span data-stu-id="57ea5-194">Application Usage</span></span>  |
|---------|---------|---------|
|<span data-ttu-id="57ea5-195">Nom d’hôte</span><span class="sxs-lookup"><span data-stu-id="57ea5-195">Host Name</span></span> |<span data-ttu-id="57ea5-196">Nom du package</span><span class="sxs-lookup"><span data-stu-id="57ea5-196">Package Name</span></span>|<span data-ttu-id="57ea5-197">Heures de début et de fin</span><span class="sxs-lookup"><span data-stu-id="57ea5-197">Start and End Times</span></span>|
|<span data-ttu-id="57ea5-198">Version du client App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="57ea5-198">App-V 5.1 Client Version</span></span> |<span data-ttu-id="57ea5-199">Version du package</span><span class="sxs-lookup"><span data-stu-id="57ea5-199">Package Version</span></span>|<span data-ttu-id="57ea5-200">État d’exécution</span><span class="sxs-lookup"><span data-stu-id="57ea5-200">Run Status</span></span>|
|<span data-ttu-id="57ea5-201">Architecture de processeur</span><span class="sxs-lookup"><span data-stu-id="57ea5-201">Processor Architecture</span></span> |<span data-ttu-id="57ea5-202">Source du package</span><span class="sxs-lookup"><span data-stu-id="57ea5-202">Package Source</span></span>|<span data-ttu-id="57ea5-203">État d’arrêt</span><span class="sxs-lookup"><span data-stu-id="57ea5-203">Shutdown State</span></span>|
|<span data-ttu-id="57ea5-204">Version du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="57ea5-204">Operating System Version</span></span>|<span data-ttu-id="57ea5-205">Pourcentage mis en cache</span><span class="sxs-lookup"><span data-stu-id="57ea5-205">Percent Cached</span></span>|<span data-ttu-id="57ea5-206">Nom de l’application</span><span class="sxs-lookup"><span data-stu-id="57ea5-206">Application Name</span></span>|
|<span data-ttu-id="57ea5-207">Niveau de Service Pack</span><span class="sxs-lookup"><span data-stu-id="57ea5-207">Service Pack Level</span></span>| |<span data-ttu-id="57ea5-208">Version de l’application</span><span class="sxs-lookup"><span data-stu-id="57ea5-208">Application Version</span></span>|
|<span data-ttu-id="57ea5-209">Type de système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="57ea5-209">Operating System Type</span></span>| |<span data-ttu-id="57ea5-210">Nom d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="57ea5-210">Username</span></span>|
| | |<span data-ttu-id="57ea5-211">Groupe de connexion</span><span class="sxs-lookup"><span data-stu-id="57ea5-211">Connection Group</span></span>|

<span data-ttu-id="57ea5-212">Le client recueille et enregistre les données dans un format **. xml** .</span><span class="sxs-lookup"><span data-stu-id="57ea5-212">The client collects and saves this data in an **.xml** format.</span></span> <span data-ttu-id="57ea5-213">Le cache des données est masqué par défaut et nécessite des droits d’administrateur pour ouvrir le fichier XML.</span><span class="sxs-lookup"><span data-stu-id="57ea5-213">The data cache is hidden by default and requires administrator rights to open the XML file.</span></span>

### <span data-ttu-id="57ea5-214">Envoyer des données au serveur</span><span class="sxs-lookup"><span data-stu-id="57ea5-214">Sending data to the server</span></span>

<span data-ttu-id="57ea5-215">Vous pouvez configurer l’ordinateur qui exécute le client App-V 5,1 pour envoyer automatiquement des données au serveur de rapports spécifié.</span><span class="sxs-lookup"><span data-stu-id="57ea5-215">You can configure the computer that is running the App-V 5.1 client to automatically send data to the specified reporting server.</span></span> <span data-ttu-id="57ea5-216">Pour spécifier le serveur, utilisez l’applet de commande **Set-AppvClientConfiguration** avec les paramètres suivants:</span><span class="sxs-lookup"><span data-stu-id="57ea5-216">To specify the server use the **Set-AppvClientConfiguration** cmdlet with the following settings:</span></span>

- <span data-ttu-id="57ea5-217">ReportingEnabled</span><span class="sxs-lookup"><span data-stu-id="57ea5-217">ReportingEnabled</span></span>
- <span data-ttu-id="57ea5-218">ReportingServerURL</span><span class="sxs-lookup"><span data-stu-id="57ea5-218">ReportingServerURL</span></span>
- <span data-ttu-id="57ea5-219">ReportingStartTime</span><span class="sxs-lookup"><span data-stu-id="57ea5-219">ReportingStartTime</span></span>
- <span data-ttu-id="57ea5-220">ReportingInterval</span><span class="sxs-lookup"><span data-stu-id="57ea5-220">ReportingInterval</span></span>
- <span data-ttu-id="57ea5-221">ReportingRandomDelay</span><span class="sxs-lookup"><span data-stu-id="57ea5-221">ReportingRandomDelay</span></span>

<span data-ttu-id="57ea5-222">Après avoir configuré les paramètres précédents, vous devez créer une tâche planifiée.</span><span class="sxs-lookup"><span data-stu-id="57ea5-222">After you configure the previous settings, you must create a scheduled task.</span></span> <span data-ttu-id="57ea5-223">La tâche planifiée contactera le serveur spécifié par le paramètre **ReportingServerURL** et lancera le transfert.</span><span class="sxs-lookup"><span data-stu-id="57ea5-223">The scheduled task will contact the server specified by the **ReportingServerURL** setting and will initiate the transfer.</span></span> <span data-ttu-id="57ea5-224">Si vous voulez envoyer les données manuellement en dehors des heures prévues, utilisez l’applet de commande PowerShell suivante:</span><span class="sxs-lookup"><span data-stu-id="57ea5-224">If you want to manually send data outside of the scheduled times, use the following PowerShell cmdlet:</span></span>

```powershell
Send-AppVClientReport –URL http://MyReportingServer:MyPort/ -DeleteOnSuccess
```

<span data-ttu-id="57ea5-225">Si le serveur de création de rapports a été configuré précédemment, le paramètre **– URL** peut être omis.</span><span class="sxs-lookup"><span data-stu-id="57ea5-225">If the reporting server has been previously configured, then the **–URL** parameter can be omitted.</span></span> <span data-ttu-id="57ea5-226">Si les données doivent être envoyées à un autre emplacement, vous pouvez aussi spécifier une autre URL pour remplacer le **ReportingServerURL** configuré pour cette collection de données.</span><span class="sxs-lookup"><span data-stu-id="57ea5-226">Alternatively, if the data should be sent to an alternate location, specify a different URL to override the configured **ReportingServerURL** for this data collection.</span></span>

<span data-ttu-id="57ea5-227">Le paramètre **-DeleteOnSuccess** indique que si le transfert est réussi, le cache des données est alors effacé.</span><span class="sxs-lookup"><span data-stu-id="57ea5-227">The **-DeleteOnSuccess** parameter indicates that if the transfer is successful, then the data cache is cleared.</span></span> <span data-ttu-id="57ea5-228">Si cette valeur n’est pas spécifiée, le cache ne sera pas vidé.</span><span class="sxs-lookup"><span data-stu-id="57ea5-228">If this is not specified, then the cache will not be cleared.</span></span>

### <span data-ttu-id="57ea5-229">Collection de données manuelle</span><span class="sxs-lookup"><span data-stu-id="57ea5-229">Manual Data Collection</span></span>

<span data-ttu-id="57ea5-230">Vous pouvez également utiliser l’applet de passe **Send-AppVClientReport** pour collecter des données manuellement.</span><span class="sxs-lookup"><span data-stu-id="57ea5-230">You can also use the **Send-AppVClientReport** cmdlet to manually collect data.</span></span> <span data-ttu-id="57ea5-231">Cette solution est utile avec ou sans serveur de création de rapports existant.</span><span class="sxs-lookup"><span data-stu-id="57ea5-231">This solution is helpful with or without an existing reporting server.</span></span> <span data-ttu-id="57ea5-232">La liste suivante présente des informations sur la collecte de données avec ou sans serveur de rapports.</span><span class="sxs-lookup"><span data-stu-id="57ea5-232">The following list displays information about collecting data with or without a reporting server.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="57ea5-233">Avec un serveur de création de rapports</span><span class="sxs-lookup"><span data-stu-id="57ea5-233">With a Reporting Server</span></span></th>
<th align="left"><span data-ttu-id="57ea5-234">Sans serveur de création de rapports</span><span class="sxs-lookup"><span data-stu-id="57ea5-234">Without a Reporting Server</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="57ea5-235">Si vous disposez d’un serveur de création de rapports App-V 5,1, créez une tâche planifiée ou un script personnalisé.</span><span class="sxs-lookup"><span data-stu-id="57ea5-235">If you have an existing App-V 5.1 reporting Server, create a customized scheduled task or script.</span></span> <span data-ttu-id="57ea5-236">Spécifiez que le client envoie les données à l’emplacement spécifié avec la fréquence de votre choix.</span><span class="sxs-lookup"><span data-stu-id="57ea5-236">Specify that the client send the data to the specified location with the desired frequency.</span></span></p></td>
<td align="left"><p><span data-ttu-id="57ea5-237">Si vous n’avez pas de serveur de création de rapports App-V 5,1, utilisez le <strong> paramètre – URL </strong> pour envoyer les données vers un partage spécifié.</span><span class="sxs-lookup"><span data-stu-id="57ea5-237">If you do not have an existing App-V 5.1 reporting Server, use the <strong>–URL</strong> parameter to send the data to a specified share.</span></span> <span data-ttu-id="57ea5-238">Exemple:</span><span class="sxs-lookup"><span data-stu-id="57ea5-238">For example:</span></span></p>
<p><code>Send-AppVClientReport –URL \Myshare\MyData\ -DeleteOnSuccess</code></p>
<p><span data-ttu-id="57ea5-239">L’exemple précédent envoie les données de rapport à <strong> l' &lt; emplacement \MyShare\MyData/Strong &gt; indiqué par le <strong> paramètre-URL </strong> .</span><span class="sxs-lookup"><span data-stu-id="57ea5-239">The previous example will send the reporting data to <strong>\MyShare\MyData&lt;/strong&gt; location indicated by the <strong>-URL</strong> parameter.</span></span> <span data-ttu-id="57ea5-240">Après l’envoi des données, le cache est vidé.</span><span class="sxs-lookup"><span data-stu-id="57ea5-240">After the data has been sent, the cache is cleared.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="57ea5-241">Remarque</span><span class="sxs-lookup"><span data-stu-id="57ea5-241">Note</span></span></strong><br/><p><span data-ttu-id="57ea5-242">S’il s’agit d’un emplacement autre que le serveur de création de rapports, les données sont envoyées au <strong> format. XML sans </strong> traitement supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="57ea5-242">If a location other than the Reporting Server is specified, the data is sent using <strong>.xml</strong> format with no additional processing.</span></span></p>
</div>
<div>
</div></td>
</tr>
</tbody>
</table>

### <span data-ttu-id="57ea5-243">Création de rapports</span><span class="sxs-lookup"><span data-stu-id="57ea5-243">Creating Reports</span></span>

<span data-ttu-id="57ea5-244">Pour récupérer des informations de rapport et créer des rapports à l’aide de App-V 5,1, vous devez utiliser l’une des méthodes suivantes:</span><span class="sxs-lookup"><span data-stu-id="57ea5-244">To retrieve report information and create reports using App-V 5.1 you must use one of the following methods:</span></span>

- <span data-ttu-id="57ea5-245">**Microsoft SQL Server Reporting Services (SSRS)** -Microsoft SQL Server Reporting Services est disponible avec Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="57ea5-245">**Microsoft SQL Server Reporting Services (SSRS)** - Microsoft SQL Server Reporting Services is available with Microsoft SQL Server.</span></span> <span data-ttu-id="57ea5-246">SSRS n’est pas installé lors de l’installation de l’App-V 5,1 Reporting Server.</span><span class="sxs-lookup"><span data-stu-id="57ea5-246">SSRS is not installed when you install the App-V 5.1 reporting server.</span></span> <span data-ttu-id="57ea5-247">Il doit être déployé séparément pour générer les rapports associés.</span><span class="sxs-lookup"><span data-stu-id="57ea5-247">It must be deployed separately to generate the associated reports.</span></span>

    <span data-ttu-id="57ea5-248">Utilisez le lien suivant pour plus d’informations sur l’utilisation de [Microsoft SQL Server Reporting Services](https://go.microsoft.com/fwlink/?LinkId=285596).</span><span class="sxs-lookup"><span data-stu-id="57ea5-248">Use the following link for more information about using [Microsoft SQL Server Reporting Services](https://go.microsoft.com/fwlink/?LinkId=285596).</span></span>

- <span data-ttu-id="57ea5-249">**Écriture de scripts** – vous pouvez générer des rapports en effectuant des scripts directement sur la base de données de création de rapports App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="57ea5-249">**Scripting** – You can generate reports by scripting directly against the App-V 5.1 reporting database.</span></span> <span data-ttu-id="57ea5-250">Exemple:</span><span class="sxs-lookup"><span data-stu-id="57ea5-250">For example:</span></span>

    **<span data-ttu-id="57ea5-251">Procédure stockée:</span><span class="sxs-lookup"><span data-stu-id="57ea5-251">Stored Procedure:</span></span>**

    <span data-ttu-id="57ea5-252">**spProcessClientReport** est programmé pour s’exécuter sur minuit ou 12:00 AM.</span><span class="sxs-lookup"><span data-stu-id="57ea5-252">**spProcessClientReport** is scheduled to run at midnight or 12:00 AM.</span></span>

    <span data-ttu-id="57ea5-253">Pour exécuter la procédure stockée planifiée Microsoft SQL Server, l’agent Microsoft SQL Server doit être en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="57ea5-253">To run the Microsoft SQL Server Scheduled Stored procedure, the Microsoft SQL Server Agent must be running.</span></span> <span data-ttu-id="57ea5-254">Assurez-vous que l’agent Microsoft SQL Server est défini sur **démarrage automatique**.</span><span class="sxs-lookup"><span data-stu-id="57ea5-254">You should ensure that the Microsoft SQL Server Agent is set to **AutoStart**.</span></span> <span data-ttu-id="57ea5-255">Pour plus d’informations, reportez-vous à [démarrage automatique de l’agent SQL Server (SQL Server Management Studio)](https://go.microsoft.com/fwlink/?LinkId=287045).</span><span class="sxs-lookup"><span data-stu-id="57ea5-255">For more information see [Autostart SQL Server Agent (SQL Server Management Studio)](https://go.microsoft.com/fwlink/?LinkId=287045).</span></span>

    <span data-ttu-id="57ea5-256">La procédure stockée est également créée lors de l’utilisation des scripts de base de données App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="57ea5-256">The stored procedure is also created when using the App-V 5.1 database scripts.</span></span>

<span data-ttu-id="57ea5-257">Vous devez également vous assurer que les **connexions concomitantes** du service Web serveur de création de rapports sont définies sur une valeur que le serveur pourra gérer sans influer sur la disponibilité.</span><span class="sxs-lookup"><span data-stu-id="57ea5-257">You should also ensure that the reporting server web service's **Maximum Concurrent Connections** is set to a value that the server will be able to manage without impacting availability.</span></span> <span data-ttu-id="57ea5-258">Le nombre maximal de **connexions simultanées autorisées** pour le **service Web de création de rapports** est **10 000**.</span><span class="sxs-lookup"><span data-stu-id="57ea5-258">The recommended number of **Maximum Concurrent Connections** for the **Reporting Web Service** is **10,000**.</span></span>

## <span data-ttu-id="57ea5-259">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="57ea5-259">Related topics</span></span>

[<span data-ttu-id="57ea5-260">Déploiement d'App-V5.1 Server</span><span class="sxs-lookup"><span data-stu-id="57ea5-260">Deploying the App-V 5.1 Server</span></span>](deploying-the-app-v-51-server.md)

[<span data-ttu-id="57ea5-261">Comment installer le serveur de rapports sur un ordinateur autonome et le connecter à la base de données</span><span class="sxs-lookup"><span data-stu-id="57ea5-261">How to install the Reporting Server on a Standalone Computer and Connect it to the Database</span></span>](how-to-install-the-reporting-server-on-a-standalone-computer-and-connect-it-to-the-database51.md)
