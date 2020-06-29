---
title: Comment configurer les applications Web MBAM2.5
description: Comment configurer les applications Web MBAM2.5
author: dansimp
ms.assetid: 909bf2d3-028c-4ac1-9247-171532a1eeae
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0336d24f51167a00c8565ccd081f4bc5dfb2c4cd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810590"
---
# <span data-ttu-id="5e3c0-103">Comment configurer les applications Web MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="5e3c0-103">How to Configure the MBAM 2.5 Web Applications</span></span>


<span data-ttu-id="5e3c0-104">Cet article explique comment configurer les applications Web Microsoft BitLocker Administration and Analysis (MBAM) 2,5 pour l' [architecture de niveau supérieur recommandée pour MBAM 2,5](high-level-architecture-for-mbam-25.md) en utilisant l’une des méthodes suivantes:</span><span class="sxs-lookup"><span data-stu-id="5e3c0-104">This topic explains how to configure the Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 web applications for the recommended [High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md) by using one of the following methods:</span></span>

-   <span data-ttu-id="5e3c0-105">Une applet de cmdlet Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="5e3c0-105">A Windows PowerShell cmdlet</span></span>

-   <span data-ttu-id="5e3c0-106">Assistant Configuration de MBAM Server</span><span class="sxs-lookup"><span data-stu-id="5e3c0-106">The MBAM Server Configuration wizard</span></span>

<span data-ttu-id="5e3c0-107">Les applications Web comprennent les sites Web suivants et leurs services Web correspondants:</span><span class="sxs-lookup"><span data-stu-id="5e3c0-107">The web applications comprise the following websites and their corresponding web services:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5e3c0-108">Website</span><span class="sxs-lookup"><span data-stu-id="5e3c0-108">Website</span></span></th>
<th align="left"><span data-ttu-id="5e3c0-109">Description</span><span class="sxs-lookup"><span data-stu-id="5e3c0-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5e3c0-110">Site Web d’administration et de surveillance</span><span class="sxs-lookup"><span data-stu-id="5e3c0-110">Administration and Monitoring Website</span></span></p></td>
<td align="left"><p><span data-ttu-id="5e3c0-111">Site Web dans lequel les utilisateurs spécifiques peuvent afficher des rapports et aider les utilisateurs finaux à récupérer leurs ordinateurs lors de leur oubli du code confidentiel ou du mot de passe</span><span class="sxs-lookup"><span data-stu-id="5e3c0-111">Website where specified users can view reports and help end users recover their computers when they forget their PIN or password</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5e3c0-112">Portail libre-service</span><span class="sxs-lookup"><span data-stu-id="5e3c0-112">Self-Service Portal</span></span></p></td>
<td align="left"><p><span data-ttu-id="5e3c0-113">Site Web: les utilisateurs finaux peuvent accéder de manière indépendante à leurs ordinateurs s’ils ont oublié leur code confidentiel ou leur mot de passe.</span><span class="sxs-lookup"><span data-stu-id="5e3c0-113">Website that end users can access to independently regain access to their computers if they forget their PIN or password</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="5e3c0-114">Avant de démarrer la configuration:</span><span class="sxs-lookup"><span data-stu-id="5e3c0-114">Before you start the configuration:</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5e3c0-115">Étape</span><span class="sxs-lookup"><span data-stu-id="5e3c0-115">Step</span></span></th>
<th align="left"><span data-ttu-id="5e3c0-116">Où obtenir des instructions</span><span class="sxs-lookup"><span data-stu-id="5e3c0-116">Where to get instructions</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5e3c0-117">Passez en revue l’architecture recommandée pour MBAM.</span><span class="sxs-lookup"><span data-stu-id="5e3c0-117">Review the recommended architecture for MBAM.</span></span></p></td>
<td align="left"><p><a href="high-level-architecture-for-mbam-25.md" data-raw-source="[High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md)"><span data-ttu-id="5e3c0-118">Architecture de hautniveau pour MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="5e3c0-118">High-Level Architecture for MBAM 2.5</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5e3c0-119">Passez en revue les configurations prises en charge pour MBAM.</span><span class="sxs-lookup"><span data-stu-id="5e3c0-119">Review the supported configurations for MBAM.</span></span></p></td>
<td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"><span data-ttu-id="5e3c0-120">Configurations prises en charge par MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="5e3c0-120">MBAM 2.5 Supported Configurations</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5e3c0-121">Remplissez les conditions préalables requises sur chaque serveur.</span><span class="sxs-lookup"><span data-stu-id="5e3c0-121">Complete the required prerequisites on each server.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="5e3c0-122">Remarque</span><span class="sxs-lookup"><span data-stu-id="5e3c0-122">Note</span></span></strong><br/><p><span data-ttu-id="5e3c0-123">Assurez-vous de configurer les services SQL ServerReporting (SSRS) pour utiliser le protocole SSL (Secure Sockets Layer) avant de configurer le site Web d’administration et de surveillance.</span><span class="sxs-lookup"><span data-stu-id="5e3c0-123">Ensure that you configure SQL ServerReporting Services (SSRS) to use the Secure Sockets Layer (SSL) before you configure the Administration and Monitoring Website.</span></span> <span data-ttu-id="5e3c0-124">Dans le cas contraire, la fonction rapports utilise HTTP au lieu de HTTPs.</span><span class="sxs-lookup"><span data-stu-id="5e3c0-124">Otherwise, the Reports feature will use HTTP instead of HTTPS.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><ul>
<li><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)"><span data-ttu-id="5e3c0-125">Conditions préalables pour le serveur MBAM2.5 pour les topologies Intégration Configuration Manager et autonome</span><span class="sxs-lookup"><span data-stu-id="5e3c0-125">MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies</span></span></a></p></li>
<li><p><a href="mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md" data-raw-source="[MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)"><span data-ttu-id="5e3c0-126">MBAM 2,5 requis par le serveur qui ne s’appliquent qu’à la topologie d’intégration de Configuration Manager </a> (le cas échéant)</span><span class="sxs-lookup"><span data-stu-id="5e3c0-126">MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology</a> (if applicable)</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5e3c0-127">Enregistrez les noms de principal de service (SPN) pour le compte du pool d’applications pour les sites Web.</span><span class="sxs-lookup"><span data-stu-id="5e3c0-127">Register service principal names (SPNs) for the application pool account for the websites.</span></span> <span data-ttu-id="5e3c0-128">Vous ne devez effectuer cette étape que si vous n’avez pas de privilèges d’administrateur dans les services de domaine Active Directory (AD DS).</span><span class="sxs-lookup"><span data-stu-id="5e3c0-128">You need to do this step only if you do not have administrative domain rights in Active Directory Domain Services (AD DS).</span></span> <span data-ttu-id="5e3c0-129">Si vous disposez de ces droits dans AD DS, MBAM créera les noms de services pour vous.</span><span class="sxs-lookup"><span data-stu-id="5e3c0-129">If you do have these rights in AD DS, MBAM will create the SPNs for you.</span></span></p></td>
<td align="left"><p><a href="planning-how-to-secure-the-mbam-websites.md#bkmk-regvirtualspn" data-raw-source="[Planning How to Secure the MBAM Websites](planning-how-to-secure-the-mbam-websites.md#bkmk-regvirtualspn)"><span data-ttu-id="5e3c0-130">Planification de la sécurisation des sites web MBAM</span><span class="sxs-lookup"><span data-stu-id="5e3c0-130">Planning How to Secure the MBAM Websites</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5e3c0-131">Installez le logiciel serveur MBAM sur chaque serveur sur lequel vous allez configurer une fonctionnalité de MBAM Server.</span><span class="sxs-lookup"><span data-stu-id="5e3c0-131">Install the MBAM Server software on each server where you will configure an MBAM Server feature.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="5e3c0-132">Remarque</span><span class="sxs-lookup"><span data-stu-id="5e3c0-132">Note</span></span></strong><br/><p><span data-ttu-id="5e3c0-133">Si vous envisagez d’installer le site Web sur un serveur et les services Web sur un autre serveur, vous pouvez les configurer uniquement à l’aide de la <strong> </strong> cmdlet Windows PowerShell Enable-MbamWebApplication.</span><span class="sxs-lookup"><span data-stu-id="5e3c0-133">If you plan to install the websites on one server and the web services on another, you will be able to configure them only by using the <strong>Enable-MbamWebApplication</strong> Windows PowerShell cmdlet.</span></span> <span data-ttu-id="5e3c0-134">L’Assistant Configuration du serveur MBAM ne prend pas en charge la configuration de ces éléments sur des serveurs distincts.</span><span class="sxs-lookup"><span data-stu-id="5e3c0-134">The MBAM Server Configuration wizard does not support configuring these items on separate servers.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)"><span data-ttu-id="5e3c0-135">Installation du logiciel serveur MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="5e3c0-135">Installing the MBAM 2.5 Server Software</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5e3c0-136">Consultez la configuration requise pour l’utilisation de Windows PowerShell Si vous envisagez d’utiliser des cmdlets pour configurer les fonctionnalités de MBAM Server.</span><span class="sxs-lookup"><span data-stu-id="5e3c0-136">Review the prerequisites for using Windows PowerShell if you plan to use cmdlets to configure MBAM Server features.</span></span></p></td>
<td align="left"><p><a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)"><span data-ttu-id="5e3c0-137">Configuration des composants du serveur MBAM2.5 à l'aide de Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="5e3c0-137">Configuring MBAM 2.5 Server Features by Using Windows PowerShell</span></span></a></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="5e3c0-138">Pour configurer les applications Web à l’aide de Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="5e3c0-138">To configure the web applications by using Windows PowerShell</span></span>**

1.  <span data-ttu-id="5e3c0-139">Avant de commencer la configuration, reportez-vous à la rubrique [Configuration des fonctionnalités du serveur MBAM 2,5 à l’aide de Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md) pour consulter les conditions préalables à l’utilisation de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5e3c0-139">Before you start the configuration, see [Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md) to review the prerequisites for using Windows PowerShell.</span></span>

2.  <span data-ttu-id="5e3c0-140">Utilisez l’applet de ligne **Enable-MbamWebApplication** pour configurer les applications Web à l’aide de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5e3c0-140">Use the **Enable-MbamWebApplication** cmdlet to configure the web applications using Windows PowerShell.</span></span> <span data-ttu-id="5e3c0-141">Pour obtenir des informations sur cette cmdlet, tapez **Get-Help-MbamWebApplication**.</span><span class="sxs-lookup"><span data-stu-id="5e3c0-141">To get information about this cmdlet, type **Get-Help Enable-MbamWebApplication**.</span></span>

**<span data-ttu-id="5e3c0-142">Pour configurer les paramètres de toutes les applications Web à l’aide de l’Assistant</span><span class="sxs-lookup"><span data-stu-id="5e3c0-142">To configure the settings for all web applications using the wizard</span></span>**

1. <span data-ttu-id="5e3c0-143">Sur le serveur sur lequel vous voulez configurer les applications Web, démarrez l’Assistant Configuration de MBAM Server.</span><span class="sxs-lookup"><span data-stu-id="5e3c0-143">On the server where you want to configure the web applications, start the MBAM Server Configuration wizard.</span></span> <span data-ttu-id="5e3c0-144">Vous pouvez sélectionner **MBAM de configuration de serveur** dans le menu **Démarrer** pour ouvrir l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="5e3c0-144">You can select **MBAM Server Configuration** from the **Start** menu to open the wizard.</span></span>

2. <span data-ttu-id="5e3c0-145">Cliquez sur **ajouter de nouvelles fonctionnalités**, sélectionnez **administration et analyse du site Web** et du **portail libre-service**, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="5e3c0-145">Click **Add New Features**, select **Administration and Monitoring Website** and **Self-Service Portal**, and then click **Next**.</span></span> <span data-ttu-id="5e3c0-146">L’Assistant vérifie que toutes les conditions préalables pour les applications Web sont remplies.</span><span class="sxs-lookup"><span data-stu-id="5e3c0-146">The wizard checks that all prerequisites for the web applications have been met.</span></span>

3. <span data-ttu-id="5e3c0-147">Si la vérification de la configuration requise est réussie, cliquez sur **suivant** pour continuer.</span><span class="sxs-lookup"><span data-stu-id="5e3c0-147">If the prerequisite check is successful, click **Next** to continue.</span></span> <span data-ttu-id="5e3c0-148">Dans le cas contraire, résolvez les conditions préalables manquantes, puis cliquez **à nouveau sur vérifier les conditions préalables**.</span><span class="sxs-lookup"><span data-stu-id="5e3c0-148">Otherwise, resolve any missing prerequisites, and then click **Check prerequisites again**.</span></span>

4. <span data-ttu-id="5e3c0-149">Utilisez les descriptions suivantes pour entrer les valeurs de champ dans l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="5e3c0-149">Use the following descriptions to enter the field values in the wizard.</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><strong><span data-ttu-id="5e3c0-150">Champ</span><span class="sxs-lookup"><span data-stu-id="5e3c0-150">Field</span></span></strong></th>
   <th align="left"><span data-ttu-id="5e3c0-151">Description</span><span class="sxs-lookup"><span data-stu-id="5e3c0-151">Description</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="5e3c0-152">Certificat de sécurité</span><span class="sxs-lookup"><span data-stu-id="5e3c0-152">Security certificate</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="5e3c0-153">Sélectionnez un certificat créé précédemment pour chiffrer éventuellement la communication entre les services Web et le serveur sur lequel vous configurez les sites Web.</span><span class="sxs-lookup"><span data-stu-id="5e3c0-153">Select a previously created certificate to optionally encrypt the communication between the web services and the server on which you are configuring the websites.</span></span> <span data-ttu-id="5e3c0-154">Si vous choisissez <strong> ne pas utiliser de certificat </strong> , votre communication Web risque de ne pas être sécurisée.</span><span class="sxs-lookup"><span data-stu-id="5e3c0-154">If you choose <strong>Do not use a certificate</strong>, your web communication may not be secure.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="5e3c0-155">Nom de l'hôte</span><span class="sxs-lookup"><span data-stu-id="5e3c0-155">Host name</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="5e3c0-156">Nom de l’ordinateur hôte sur lequel vous configurez les sites Web.</span><span class="sxs-lookup"><span data-stu-id="5e3c0-156">Name of the host computer where you are configuring the websites.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="5e3c0-157">Chemin d’installation</span><span class="sxs-lookup"><span data-stu-id="5e3c0-157">Installation path</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="5e3c0-158">Emplacement d’installation des sites Web.</span><span class="sxs-lookup"><span data-stu-id="5e3c0-158">Path where you are installing the websites.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="5e3c0-159">Port</span><span class="sxs-lookup"><span data-stu-id="5e3c0-159">Port</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="5e3c0-160">Numéro de port à utiliser pour la communication avec les sites Web et les services.</span><span class="sxs-lookup"><span data-stu-id="5e3c0-160">Port number to use for website and service communication.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="5e3c0-161">Remarque</span><span class="sxs-lookup"><span data-stu-id="5e3c0-161">Note</span></span></strong><br/><p><span data-ttu-id="5e3c0-162">Vous devez définir une exception de pare-feu pour autoriser les communications via le port spécifié.</span><span class="sxs-lookup"><span data-stu-id="5e3c0-162">You must set a firewall exception to enable communication through the specified port.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="5e3c0-163">Compte et mot de passe du pool d’applications de service Web</span><span class="sxs-lookup"><span data-stu-id="5e3c0-163">Web service application pool domain account and password</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="5e3c0-164">Compte d’utilisateur de domaine et mot de passe pour le pool d’applications de service Web.</span><span class="sxs-lookup"><span data-stu-id="5e3c0-164">Domain user account and password for the web service application pool.</span></span></p>
   <p><span data-ttu-id="5e3c0-165">Si vous entrez un nom d’utilisateur dans le <strong> champ d’utilisateur ou de groupe de domaine d’accès en lecture/écriture </strong> sur la <strong> page configurer des bases de données </strong> , vous devez entrer cette même valeur dans ce champ.</span><span class="sxs-lookup"><span data-stu-id="5e3c0-165">If you enter a user name in the <strong>Read/write access domain user or group</strong> field on the <strong>Configure Databases</strong> page, you must enter that same value in this field.</span></span></p>
   <p><span data-ttu-id="5e3c0-166">Si vous entrez un nom de groupe dans le <strong> champ User ou Group (lecture/écriture </strong> ) sur la <strong> page configure databases </strong> , la valeur que vous entrez dans ce champ doit être membre du groupe.</span><span class="sxs-lookup"><span data-stu-id="5e3c0-166">If you enter a group name in the <strong>Read/write access domain user or group</strong> field on the <strong>Configure Databases</strong> page, the value you enter in this field must be a member of that group.</span></span></p>
   <p><span data-ttu-id="5e3c0-167">Si vous ne spécifiez pas les informations d’identification, les informations d’identification spécifiées pour une application Web précédemment activée seront utilisées.</span><span class="sxs-lookup"><span data-stu-id="5e3c0-167">If you do not specify credentials, the credentials that were specified for any previously enabled web application will be used.</span></span> <span data-ttu-id="5e3c0-168">Toutes les applications Web doivent utiliser les mêmes informations d’identification de pool d’applications.</span><span class="sxs-lookup"><span data-stu-id="5e3c0-168">All web applications must use the same application pool credentials.</span></span> <span data-ttu-id="5e3c0-169">Si vous spécifiez des informations d’identification différentes pour différentes applications Web, la valeur la plus récemment spécifiée est utilisée.</span><span class="sxs-lookup"><span data-stu-id="5e3c0-169">If you specify different credentials for different web applications, the most recently specified value will be used.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="5e3c0-170">Important</span><span class="sxs-lookup"><span data-stu-id="5e3c0-170">Important</span></span></strong><br/><p><span data-ttu-id="5e3c0-171">Pour une sécurité améliorée, définissez le compte spécifié dans les informations d’identification pour disposer de droits d’utilisateur limités.</span><span class="sxs-lookup"><span data-stu-id="5e3c0-171">For improved security, set the account that is specified in the credentials to have limited user rights.</span></span> <span data-ttu-id="5e3c0-172">Définissez également le mot de passe du compte pour qu’il n’expire jamais.</span><span class="sxs-lookup"><span data-stu-id="5e3c0-172">Also, set the password of the account to never expire.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   </tbody>
   </table>



5. <span data-ttu-id="5e3c0-173">Vérifiez que le compte intégré aux services Internet (IIS _IUSRS), ou au compte du pool d’applications a été ajouté à l' **identité d’un client après l’authentification** et **que le travail en fonction du traitement par lot** est défini sur paramètres de sécurité locale.</span><span class="sxs-lookup"><span data-stu-id="5e3c0-173">Verify that the built-in IIS\_IUSRS account or the application pool account has been added to the **Impersonate a client after authentication** and the **Log on as a batch job** local security settings.</span></span>

   <span data-ttu-id="5e3c0-174">Pour vérifier si l’application a été ajoutée aux paramètres de sécurité locaux, ouvrez l' **éditeur de stratégie de sécurité locale**, développez le nœud **stratégies locales** , cliquez sur le nœud d' **attribution de droits d’utilisateur** , puis double-cliquez sur emprunter l’identité d' **un client après authentification** et **Connectez-vous en tant que stratégies de travail par lot** dans le volet droit.</span><span class="sxs-lookup"><span data-stu-id="5e3c0-174">To check whether it has been added to the local security settings, open the **Local Security Policy editor**, expand the **Local Policies** node, click the **User Rights Assignment** node, and double-click **Impersonate a client after authentication** and **Log on as a batch job** policies in the right pane.</span></span>

**<span data-ttu-id="5e3c0-175">Pour configurer les informations de connexion des bases de données à l’aide de l’Assistant</span><span class="sxs-lookup"><span data-stu-id="5e3c0-175">To configure connection information for the databases by using the wizard</span></span>**

1.  <span data-ttu-id="5e3c0-176">Utilisez les descriptions de champs suivantes pour configurer les informations de connexion dans l’Assistant pour la base de données d’audit et de conformité.</span><span class="sxs-lookup"><span data-stu-id="5e3c0-176">Use the following field descriptions to configure the connection information in the wizard for the Compliance and Audit Database.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="5e3c0-177">Champ</span><span class="sxs-lookup"><span data-stu-id="5e3c0-177">Field</span></span></th>
    <th align="left"><span data-ttu-id="5e3c0-178">Description</span><span class="sxs-lookup"><span data-stu-id="5e3c0-178">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="5e3c0-179">Nom SQL Server</span><span class="sxs-lookup"><span data-stu-id="5e3c0-179">SQL Server name</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="5e3c0-180">Nom du serveur sur lequel la base de données d’audit et de conformité est configurée.</span><span class="sxs-lookup"><span data-stu-id="5e3c0-180">Name of the server where the Compliance and Audit Database is configured.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong><span data-ttu-id="5e3c0-181">Instance de base de données SQL Server</span><span class="sxs-lookup"><span data-stu-id="5e3c0-181">SQL Server database instance</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="5e3c0-182">Nom de l’instance SQL Server où la base de données d’audit et de conformité est configurée.</span><span class="sxs-lookup"><span data-stu-id="5e3c0-182">SQL Server instance name where the Compliance and Audit Database is configured.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="5e3c0-183">Nom de la base de données</span><span class="sxs-lookup"><span data-stu-id="5e3c0-183">Database name</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="5e3c0-184">Nom de la base de données d’audit et de conformité.</span><span class="sxs-lookup"><span data-stu-id="5e3c0-184">Name of the Compliance and Audit Database.</span></span></p></td>
    </tr>
    </tbody>
    </table>



2.  <span data-ttu-id="5e3c0-185">Utilisez les descriptions de champs suivantes pour configurer les informations de connexion dans l’Assistant pour la base de données de récupération.</span><span class="sxs-lookup"><span data-stu-id="5e3c0-185">Use the following field descriptions to configure the connection information in the wizard for the Recovery Database.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="5e3c0-186">Champ</span><span class="sxs-lookup"><span data-stu-id="5e3c0-186">Field</span></span></th>
    <th align="left"><span data-ttu-id="5e3c0-187">Description</span><span class="sxs-lookup"><span data-stu-id="5e3c0-187">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="5e3c0-188">Nom SQL Server</span><span class="sxs-lookup"><span data-stu-id="5e3c0-188">SQL Server name</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="5e3c0-189">Nom du serveur sur lequel la base de données de récupération est configurée.</span><span class="sxs-lookup"><span data-stu-id="5e3c0-189">Name of the server where the Recovery Database is configured.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong><span data-ttu-id="5e3c0-190">Instance de base de données SQL Server</span><span class="sxs-lookup"><span data-stu-id="5e3c0-190">SQL Server database instance</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="5e3c0-191">Nom de l’instance SQL Server où la base de données de récupération est configurée.</span><span class="sxs-lookup"><span data-stu-id="5e3c0-191">SQL Server instance name where the Recovery Database is configured.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="5e3c0-192">Nom de la base de données</span><span class="sxs-lookup"><span data-stu-id="5e3c0-192">Database name</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="5e3c0-193">Nom de la base de données de récupération.</span><span class="sxs-lookup"><span data-stu-id="5e3c0-193">Name of the Recovery Database.</span></span></p></td>
    </tr>
    </tbody>
    </table>



**<span data-ttu-id="5e3c0-194">Pour configurer les applications Web à l’aide de l’Assistant</span><span class="sxs-lookup"><span data-stu-id="5e3c0-194">To configure the web applications by using the wizard</span></span>**

1. <span data-ttu-id="5e3c0-195">Utilisez les descriptions suivantes pour entrer les valeurs de champ dans l’Assistant afin de configurer le site Web d’administration et de surveillance.</span><span class="sxs-lookup"><span data-stu-id="5e3c0-195">Use the following descriptions to enter the field values in the wizard to configure the Administration and Monitoring Website.</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="5e3c0-196">Champ</span><span class="sxs-lookup"><span data-stu-id="5e3c0-196">Field</span></span></th>
   <th align="left"><span data-ttu-id="5e3c0-197">Description</span><span class="sxs-lookup"><span data-stu-id="5e3c0-197">Description</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="5e3c0-198">Groupe de domaine de rôle de support avancé</span><span class="sxs-lookup"><span data-stu-id="5e3c0-198">Advanced Helpdesk role domain group</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="5e3c0-199">Groupe d’utilisateurs de domaine dont les membres ont accès à toutes les zones du site Web d’administration et de contrôle, à l’exception de la zone rapports.</span><span class="sxs-lookup"><span data-stu-id="5e3c0-199">Domain user group whose members have access to all areas of the Administration and Monitoring Website except the Reports area.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="5e3c0-200">Groupe de domaine du rôle de support technique</span><span class="sxs-lookup"><span data-stu-id="5e3c0-200">Helpdesk role domain group</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="5e3c0-201">Groupe d’utilisateurs de domaine dont les membres ont accès aux <strong> zones gérer le module de plateforme sécurisée </strong> et <strong> </strong> de récupération des lecteurs du site Web d’administration et de surveillance.</span><span class="sxs-lookup"><span data-stu-id="5e3c0-201">Domain user group whose members have access to the <strong>Manage TPM</strong> and <strong>Drive Recovery</strong> areas of the Administration and Monitoring Website.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="5e3c0-202">Utiliser System Center Configuration Manager Integration</span><span class="sxs-lookup"><span data-stu-id="5e3c0-202">Use System Center Configuration Manager Integration</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="5e3c0-203">Activez cette case à cocher si vous configurez MBAM avec la topologie d’intégration de Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="5e3c0-203">Select this check box if you are configuring MBAM with the Configuration Manager Integration topology.</span></span> <span data-ttu-id="5e3c0-204">L’activation de cette case à cocher permet d’afficher tous les rapports, à l’exception du rapport d’audit de récupération, dans Configuration Manager plutôt que sur le site Web d’administration et de surveillance.</span><span class="sxs-lookup"><span data-stu-id="5e3c0-204">Selecting this check box makes all reports, except the Recovery Audit report, appear in Configuration Manager instead of in the Administration and Monitoring Website.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="5e3c0-205">Groupe de domaine de rôle de rapport</span><span class="sxs-lookup"><span data-stu-id="5e3c0-205">Reporting role domain group</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="5e3c0-206">Groupe d’utilisateurs de domaine dont les membres disposent d’un accès en lecture seule à la zone rapports du site Web d’administration et de surveillance.</span><span class="sxs-lookup"><span data-stu-id="5e3c0-206">Domain user group whose members have read-only access to the Reports area of the Administration and Monitoring Website.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="5e3c0-207">URL SQL Server Reporting Services</span><span class="sxs-lookup"><span data-stu-id="5e3c0-207">SQL Server Reporting Services URL</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="5e3c0-208">URL du serveur SSRS sur lequel les rapports MBAM sont configurés.</span><span class="sxs-lookup"><span data-stu-id="5e3c0-208">URL for the SSRS server where the MBAM Reports are configured.</span></span></p>
   <p><span data-ttu-id="5e3c0-209">Exemples d’URL de rapport:</span><span class="sxs-lookup"><span data-stu-id="5e3c0-209">Examples of report URLs:</span></span></p>
   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="5e3c0-210">Type de nom d’hôte</span><span class="sxs-lookup"><span data-stu-id="5e3c0-210">Type of host name</span></span></th>
   <th align="left"><span data-ttu-id="5e3c0-211">Exemple</span><span class="sxs-lookup"><span data-stu-id="5e3c0-211">Example</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="5e3c0-212">Exemple avec nom de domaine complet</span><span class="sxs-lookup"><span data-stu-id="5e3c0-212">Example with a fully qualified domain name</span></span></p></td>
   <td align="left"><p><a href="https://MyReportServer.Contoso.com/ReportServer" data-raw-source="https://MyReportServer.Contoso.com/ReportServer">https://MyReportServer.Contoso.com/ReportServer</a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="5e3c0-213">Exemple avec nom d’hôte personnalisé</span><span class="sxs-lookup"><span data-stu-id="5e3c0-213">Example with a custom host name</span></span></p></td>
   <td align="left"><p><a href="https://MyReportServer/ReportServer" data-raw-source="https://MyReportServer/ReportServer">https://MyReportServer/ReportServer</a></p></td>
   </tr>
   </tbody>
   </table>
   <p> </p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="5e3c0-214">Répertoire virtuel</span><span class="sxs-lookup"><span data-stu-id="5e3c0-214">Virtual directory</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="5e3c0-215">Répertoire virtuel du site Web d’administration et de surveillance.</span><span class="sxs-lookup"><span data-stu-id="5e3c0-215">Virtual directory of the Administration and Monitoring Website.</span></span> <span data-ttu-id="5e3c0-216">Ce nom correspond au répertoire physique du site Web sur le serveur et est ajouté au nom d’hôte du site Web, par exemple:</span><span class="sxs-lookup"><span data-stu-id="5e3c0-216">This name corresponds to the website’s physical directory on the server and is appended to the website’s host name, for example:</span></span></p>
   <p><span data-ttu-id="5e3c0-217">http (s):// &lt; <em> hostname </em> &gt; : &lt; <em> port </em> &gt; /helpdesk/</span><span class="sxs-lookup"><span data-stu-id="5e3c0-217">http(s)://&lt;<em>hostname</em>&gt;:&lt;<em>port</em>&gt;/HelpDesk/</span></span></p>
   <p><span data-ttu-id="5e3c0-218">Si vous ne spécifiez pas de répertoire virtuel, la valeur du <strong> support technique est </strong> utilisée.</span><span class="sxs-lookup"><span data-stu-id="5e3c0-218">If you do not specify a virtual directory, the value <strong>HelpDesk</strong> will be used.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="5e3c0-219">Groupe de domaines du rôle de migration des données </strong> (facultatif)</span><span class="sxs-lookup"><span data-stu-id="5e3c0-219">Data Migration role domain group</strong> (optional)</span></span></p></td>
   <td align="left"><p><span data-ttu-id="5e3c0-220">Groupe d’utilisateurs de domaine dont les membres ont accès pour utiliser les applets de sélection d’information d’écriture-MBAM \* pour écrire des informations de récupération via ce point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="5e3c0-220">Domain user group whose members have access to use the Write-Mbam\*Information Cmdlets to write recovery information via this endpoint.</span></span></p></td>
   </tr>
   </tbody>
   </table>



2. <span data-ttu-id="5e3c0-221">Utilisez la description suivante pour entrer les valeurs de champ dans l’Assistant afin de configurer le portail libre-service.</span><span class="sxs-lookup"><span data-stu-id="5e3c0-221">Use the following description to enter the field values in the wizard to configure the Self-Service Portal.</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="5e3c0-222">Champ</span><span class="sxs-lookup"><span data-stu-id="5e3c0-222">Field</span></span></th>
   <th align="left"><span data-ttu-id="5e3c0-223">Description</span><span class="sxs-lookup"><span data-stu-id="5e3c0-223">Description</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="5e3c0-224">Répertoire virtuel</span><span class="sxs-lookup"><span data-stu-id="5e3c0-224">Virtual directory</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="5e3c0-225">Répertoire virtuel de l’application Web.</span><span class="sxs-lookup"><span data-stu-id="5e3c0-225">Virtual directory of the web application.</span></span> <span data-ttu-id="5e3c0-226">Ce nom correspond au répertoire physique du site Web sur le serveur et est ajouté au nom d’hôte du site Web, par exemple:</span><span class="sxs-lookup"><span data-stu-id="5e3c0-226">This name corresponds to the website’s physical directory on the server, and is appended to the website’s host name, for example:</span></span></p>
   <p><span data-ttu-id="5e3c0-227">http (s):// &lt; <em> hostname </em> &gt; : &lt; <em> port </em> &gt; /selfservice/</span><span class="sxs-lookup"><span data-stu-id="5e3c0-227">http(s)://&lt;<em>hostname</em>&gt;:&lt;<em>port</em>&gt;/SelfService/</span></span></p>
   <p><span data-ttu-id="5e3c0-228">Si vous ne spécifiez pas un répertoire virtuel, la valeur <strong> selfservice </strong> est utilisée.</span><span class="sxs-lookup"><span data-stu-id="5e3c0-228">If you do not specify a virtual directory, the value <strong>SelfService</strong> will be used.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="5e3c0-229">Nom de la société</span><span class="sxs-lookup"><span data-stu-id="5e3c0-229">Company name</span></span></p></td>
   <td align="left"><p><span data-ttu-id="5e3c0-230">Spécifiez le nom d’une entreprise du portail libre-service, par exemple:</span><span class="sxs-lookup"><span data-stu-id="5e3c0-230">Specify a company name for the Self-Service Portal, for example:</span></span></p>
   <p><span data-ttu-id="5e3c0-231">Contoso</span><span class="sxs-lookup"><span data-stu-id="5e3c0-231">Contoso IT</span></span></p>
   <p><span data-ttu-id="5e3c0-232">Le nom de cette société est affiché par tous les utilisateurs du portail libre-service.</span><span class="sxs-lookup"><span data-stu-id="5e3c0-232">This company name is viewed by all Self-Service Portal users.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="5e3c0-233">Texte de l’URL du support technique</span><span class="sxs-lookup"><span data-stu-id="5e3c0-233">Helpdesk URL text</span></span></p></td>
   <td align="left"><p><span data-ttu-id="5e3c0-234">Spécifiez une instruction de texte qui redirige les utilisateurs vers le site Web du support technique de votre organisation, par exemple:</span><span class="sxs-lookup"><span data-stu-id="5e3c0-234">Specify a text statement that directs users to your organization's Helpdesk website, for example:</span></span></p>
   <p><span data-ttu-id="5e3c0-235">Contacter le support technique ou le service informatique</span><span class="sxs-lookup"><span data-stu-id="5e3c0-235">Contact Helpdesk or IT department</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="5e3c0-236">URL du support technique</span><span class="sxs-lookup"><span data-stu-id="5e3c0-236">Helpdesk URL</span></span></p></td>
   <td align="left"><p><span data-ttu-id="5e3c0-237">Spécifiez l’URL du site Web d’assistance technique de votre organisation, par exemple:</span><span class="sxs-lookup"><span data-stu-id="5e3c0-237">Specify the URL for your organization's Helpdesk website, for example:</span></span></p>
   <p><span data-ttu-id="5e3c0-238">http (s):// &lt; <em> companyHelpdeskURL</em>&gt;/</span><span class="sxs-lookup"><span data-stu-id="5e3c0-238">http(s)://&lt;<em>companyHelpdeskURL</em>&gt;/</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="5e3c0-239">Fichier texte d’avis</span><span class="sxs-lookup"><span data-stu-id="5e3c0-239">Notice text file</span></span></p></td>
   <td align="left"><p><span data-ttu-id="5e3c0-240">Dans la page d’accueil du portail libre-service, sélectionnez un fichier qui contient la notification que vous souhaitez afficher aux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="5e3c0-240">Select a file that contains the notice you want displayed to users on the Self-Service Portal landing page.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="5e3c0-241">Ne pas afficher le texte d’avis aux utilisateurs</span><span class="sxs-lookup"><span data-stu-id="5e3c0-241">Do not display notice text to users</span></span></p></td>
   <td align="left"><p><span data-ttu-id="5e3c0-242">Activez cette case à cocher pour spécifier que le texte de l’avis ne s’affiche pas aux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="5e3c0-242">Select this check box to specify that the notice text is not displayed to users.</span></span></p></td>
   </tr>
   </tbody>
   </table>



3. <span data-ttu-id="5e3c0-243">Lorsque vous avez terminé, cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="5e3c0-243">When you finish your entries, click **Next**.</span></span>

   <span data-ttu-id="5e3c0-244">L’Assistant vérifie que toutes les conditions préalables pour les applications Web sont remplies.</span><span class="sxs-lookup"><span data-stu-id="5e3c0-244">The wizard checks that all prerequisites for the web applications have been met.</span></span>

4. <span data-ttu-id="5e3c0-245">Cliquez sur **Suivant** pour poursuivre.</span><span class="sxs-lookup"><span data-stu-id="5e3c0-245">Click **Next** to continue.</span></span>

5. <span data-ttu-id="5e3c0-246">Dans la page **Résumé** , passez en revue les fonctionnalités qui seront ajoutées.</span><span class="sxs-lookup"><span data-stu-id="5e3c0-246">On the **Summary** page, review the features that will be added.</span></span>

   **<span data-ttu-id="5e3c0-247">Remarque</span><span class="sxs-lookup"><span data-stu-id="5e3c0-247">Note</span></span>**  
   <span data-ttu-id="5e3c0-248">Pour créer un script Windows PowerShell pour les entrées que vous avez effectuées, cliquez sur **Exporter le script PowerShell** et enregistrez le script.</span><span class="sxs-lookup"><span data-stu-id="5e3c0-248">To create a Windows PowerShell script for the entries you made, click **Export PowerShell Script** and save the script.</span></span>



6. <span data-ttu-id="5e3c0-249">Cliquez sur **Ajouter** pour ajouter les applications Web au serveur, puis cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="5e3c0-249">Click **Add** to add the web applications to the server, and then click **Close**.</span></span>

   <span data-ttu-id="5e3c0-250">Pour personnaliser le portail libre-service en ajoutant un texte d’avis personnalisé, le nom de votre entreprise, des pointeurs vers des informations supplémentaires, etc., voir [Personnalisation du portail libre-service pour votre organisation](customizing-the-self-service-portal-for-your-organization.md).</span><span class="sxs-lookup"><span data-stu-id="5e3c0-250">To customize the Self-Service Portal by adding custom notice text, your company name, pointers to more information, and so on, see [Customizing the Self-Service Portal for Your Organization](customizing-the-self-service-portal-for-your-organization.md).</span></span>

**<span data-ttu-id="5e3c0-251">Pour configurer le portail libre-service si les ordinateurs clients ne peuvent pas accéder au CDN</span><span class="sxs-lookup"><span data-stu-id="5e3c0-251">To configure the Self-Service Portal if client computers cannot access the CDN</span></span>**

1.  <span data-ttu-id="5e3c0-252">Déterminez si vous exécutez le service d’administration et de surveillance de BitLocker (MBAM) 2,5 SP1.</span><span class="sxs-lookup"><span data-stu-id="5e3c0-252">Determine whether you are running Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 SP1.</span></span> <span data-ttu-id="5e3c0-253">Si tel est le cas, ne faites rien.</span><span class="sxs-lookup"><span data-stu-id="5e3c0-253">If so, do nothing.</span></span> <span data-ttu-id="5e3c0-254">Votre configuration du portail libre-service est terminée.</span><span class="sxs-lookup"><span data-stu-id="5e3c0-254">Your Self-Service Portal configuration is complete.</span></span>

    **<span data-ttu-id="5e3c0-255">Remarque</span><span class="sxs-lookup"><span data-stu-id="5e3c0-255">Note</span></span>**  
    <span data-ttu-id="5e3c0-256">Le programme d’administration et de surveillance de BitLocker (MBAM) 2,5 SP1 installe les fichiers JavaScript dans le programme d’installation, il n’est donc pas nécessaire de se connecter au réseau de distribution de contenu Microsoft AJAX pour configurer le portail libre-service.</span><span class="sxs-lookup"><span data-stu-id="5e3c0-256">Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 SP1 installs the JavaScript files in setup, and so does not need to be connected to the Microsoft Ajax Content Delivery Network in order to configure the Self-Service Portal.</span></span> <span data-ttu-id="5e3c0-257">Les étapes suivantes sont nécessaires uniquement si vous utilisez une version de Microsoft BitLocker administration et analyse (MBAM) 2,5 antérieure à SP1.</span><span class="sxs-lookup"><span data-stu-id="5e3c0-257">The following steps are necessary only if you are using a version of Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 previous to SP1.</span></span>



2.  <span data-ttu-id="5e3c0-258">Déterminez si vos ordinateurs clients ont accès au réseau de distribution de contenu (CDN) Microsoft Ajax.</span><span class="sxs-lookup"><span data-stu-id="5e3c0-258">Determine if your client computers have access to the Microsoft Ajax Content Delivery Network (CDN).</span></span>

    <span data-ttu-id="5e3c0-259">Le CDN donne au portail libre-service le besoin d’accéder à certains fichiers JavaScript.</span><span class="sxs-lookup"><span data-stu-id="5e3c0-259">The CDN gives the Self-Service Portal the access it requires to certain JavaScript files.</span></span> <span data-ttu-id="5e3c0-260">Si vous ne configurez pas le portail libre-service lorsque les ordinateurs clients ne peuvent pas accéder au CDN, seul le nom de la société et le compte sous lequel l’utilisateur final s’est connecté est affiché.</span><span class="sxs-lookup"><span data-stu-id="5e3c0-260">If you don’t configure the Self-Service Portal when client computers cannot access the CDN, only the company name and the account under which the end user signed in will be displayed.</span></span> <span data-ttu-id="5e3c0-261">Aucun message d’erreur ne s’affichera.</span><span class="sxs-lookup"><span data-stu-id="5e3c0-261">No error message will be shown.</span></span>

3.  <span data-ttu-id="5e3c0-262">Effectuez l'une des opérations suivantes:</span><span class="sxs-lookup"><span data-stu-id="5e3c0-262">Do one of the following:</span></span>

    -   <span data-ttu-id="5e3c0-263">Si vos ordinateurs clients ont accès au réseau de distribution de contenu (CDN), ne faites rien.</span><span class="sxs-lookup"><span data-stu-id="5e3c0-263">If your client computers have access to the CDN, do nothing.</span></span> <span data-ttu-id="5e3c0-264">Votre configuration du portail libre-service est terminée.</span><span class="sxs-lookup"><span data-stu-id="5e3c0-264">Your Self-Service Portal configuration is complete.</span></span>

    -   <span data-ttu-id="5e3c0-265">Si vos ordinateurs clients n’ont pas accès au réseau de distribution de contenu (CDN), suivez les étapes décrites dans la [procédure de configuration du portail libre-service lorsque les ordinateurs clients ne peuvent pas accéder au réseau de distribution de contenu Microsoft](how-to-configure-the-self-service-portal-when-client-computers-cannot-access-the-microsoft-content-delivery-network.md).</span><span class="sxs-lookup"><span data-stu-id="5e3c0-265">If your client computers do not have access to the CDN, complete the steps in [How to Configure the Self-Service Portal When Client Computers Cannot Access the Microsoft Content Delivery Network](how-to-configure-the-self-service-portal-when-client-computers-cannot-access-the-microsoft-content-delivery-network.md).</span></span>


## <span data-ttu-id="5e3c0-266">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5e3c0-266">Related topics</span></span>


[<span data-ttu-id="5e3c0-267">Journaux des événements serveur</span><span class="sxs-lookup"><span data-stu-id="5e3c0-267">Server Event Logs</span></span>](server-event-logs.md)

[<span data-ttu-id="5e3c0-268">Configuration des composants du serveur MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="5e3c0-268">Configuring the MBAM 2.5 Server Features</span></span>](configuring-the-mbam-25-server-features.md)

[<span data-ttu-id="5e3c0-269">Comment configurer le portail libre-service lorsque les ordinateurs clients ne peuvent pas accéder au réseau de distribution de contenu Microsoft</span><span class="sxs-lookup"><span data-stu-id="5e3c0-269">How to Configure the Self-Service Portal When Client Computers Cannot Access the Microsoft Content Delivery Network</span></span>](how-to-configure-the-self-service-portal-when-client-computers-cannot-access-the-microsoft-content-delivery-network.md)

[<span data-ttu-id="5e3c0-270">Personnalisation du portail libre-service de votre organisation</span><span class="sxs-lookup"><span data-stu-id="5e3c0-270">Customizing the Self-Service Portal for Your Organization</span></span>](customizing-the-self-service-portal-for-your-organization.md)

[<span data-ttu-id="5e3c0-271">Validation de la configuration des composants serveur de MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="5e3c0-271">Validating the MBAM 2.5 Server Feature Configuration</span></span>](validating-the-mbam-25-server-feature-configuration.md)



## <span data-ttu-id="5e3c0-272">Vous avez une suggestion pour MBAM?</span><span class="sxs-lookup"><span data-stu-id="5e3c0-272">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="5e3c0-273">Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)</span><span class="sxs-lookup"><span data-stu-id="5e3c0-273">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="5e3c0-274">Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="5e3c0-274">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





