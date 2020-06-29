---
title: Procédure pour configurer un cache en lecture seule dans App-V Client (RDS)
description: Procédure pour configurer un cache en lecture seule dans App-V Client (RDS)
author: dansimp
ms.assetid: b6607fe2-6f92-4567-99f1-d8e3c8a591e0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a44844ae9ffc3497151be7713f6a43fda0ccd8fa
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807310"
---
# <span data-ttu-id="30b20-103">Procédure pour configurer un cache en lecture seule dans App-V Client (RDS)</span><span class="sxs-lookup"><span data-stu-id="30b20-103">How to Configure a Read-only Cache on the App-V Client (RDS)</span></span>


<span data-ttu-id="30b20-104">**Important**  Pour pouvoir utiliser cette procédure, vous devez exécuter App-V 4,6, SP1.</span><span class="sxs-lookup"><span data-stu-id="30b20-104">**Important** You must be running App-V 4.6, SP1 to use this procedure.</span></span>

 

<span data-ttu-id="30b20-105">Vous pouvez déployer le client App-V en utilisant un cache partagé rempli avec toutes les applications requises pour tous les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="30b20-105">You can deploy the App-V client by using a shared cache that is populated with all the applications required for all users.</span></span> <span data-ttu-id="30b20-106">Vous configurez ensuite les clients App-V Remote Desktop Services (RDS) pour utiliser le même fichier de cache.</span><span class="sxs-lookup"><span data-stu-id="30b20-106">Then you configure the App-V Remote Desktop Services (RDS) Clients to use the same cache file.</span></span> <span data-ttu-id="30b20-107">Les utilisateurs peuvent accéder à des applications spécifiques à l’aide du processus de publication d’application-V.</span><span class="sxs-lookup"><span data-stu-id="30b20-107">Users are granted access to specific applications by using the App-V publishing process.</span></span> <span data-ttu-id="30b20-108">Dans la mesure où le cache est déjà préchargé avec toutes les applications, aucun flux n’est déclenché lorsqu’un utilisateur démarre une application.</span><span class="sxs-lookup"><span data-stu-id="30b20-108">Because the cache is already preloaded with all applications, no streaming occurs when a user starts an application.</span></span> <span data-ttu-id="30b20-109">Toutefois, les packages utilisés pour préremplir le cache doivent être placés sur un serveur App-V qui prend en charge la diffusion en continu du protocole RTSP (Real Time Streaming Protocol) et qui accorde des autorisations d’accès aux clients App-V.</span><span class="sxs-lookup"><span data-stu-id="30b20-109">However, the packages used to prepopulate the cache must be put on an App-V server that supports Real Time Streaming Protocol (RTSP) streaming and that grants access permissions to the App-V Clients.</span></span> <span data-ttu-id="30b20-110">Si vous publiez les applications à l’aide d’un serveur de gestion App-V, vous pouvez l’utiliser pour fournir cette fonction de diffusion en continu.</span><span class="sxs-lookup"><span data-stu-id="30b20-110">If you publish the applications by using an App-V Management Server, you can use it to provide this streaming function.</span></span>

<span data-ttu-id="30b20-111">**Remarques**  Les détails décrits dans ces procédures sont uniquement destinés à des exemples.</span><span class="sxs-lookup"><span data-stu-id="30b20-111">**Note** The details outlined in these procedures are intended as examples only.</span></span> <span data-ttu-id="30b20-112">Vous pouvez utiliser différentes méthodes pour achever le processus global.</span><span class="sxs-lookup"><span data-stu-id="30b20-112">You might use different methods to complete the overall process.</span></span>

 

## <span data-ttu-id="30b20-113">Déploiement du client App-V dans un scénario RDS</span><span class="sxs-lookup"><span data-stu-id="30b20-113">Deploying the App-V Client in an RDS Scenario</span></span>


<span data-ttu-id="30b20-114">Le processus de déploiement comporte quatre tâches principales:</span><span class="sxs-lookup"><span data-stu-id="30b20-114">The deployment process consists of four primary tasks:</span></span>

-   <span data-ttu-id="30b20-115">Création et remplissage du fichier cache principal partagé</span><span class="sxs-lookup"><span data-stu-id="30b20-115">Creating and populating the master shared cache file</span></span>

-   <span data-ttu-id="30b20-116">Copie du fichier cache partagé sur le serveur de stockage</span><span class="sxs-lookup"><span data-stu-id="30b20-116">Copying the shared cache file to the server storage</span></span>

-   <span data-ttu-id="30b20-117">Configuration du logiciel client App-V</span><span class="sxs-lookup"><span data-stu-id="30b20-117">Configuring the App-V client software</span></span>

-   <span data-ttu-id="30b20-118">Gestion du cycle de déploiement des mises à jour pour le fichier cache partagé après le déploiement initial</span><span class="sxs-lookup"><span data-stu-id="30b20-118">Managing the update deployment cycle for the shared cache file after the initial deployment</span></span>

<span data-ttu-id="30b20-119">Les tâches suivantes nécessitent une planification soigneuse.</span><span class="sxs-lookup"><span data-stu-id="30b20-119">These tasks require careful planning.</span></span> <span data-ttu-id="30b20-120">Nous vous recommandons de préparer et de documenter un processus méthodique et reproductible à respecter par votre organisation.</span><span class="sxs-lookup"><span data-stu-id="30b20-120">We recommend that you prepare and document a methodical, reproducible process for your organization to follow.</span></span> <span data-ttu-id="30b20-121">Cela est particulièrement important pour la préparation et le déploiement du fichier cache principal partagé et pour la gestion en continu des mises à jour de l’application, qui requièrent chacune une mise à jour du cache partagé principal.</span><span class="sxs-lookup"><span data-stu-id="30b20-121">This is especially important for the preparation and deployment of the master shared cache file, and for the ongoing management of application updates, each of which require an update to the master shared cache.</span></span> <span data-ttu-id="30b20-122">Utilisez les procédures suivantes pour effectuer ces tâches principales.</span><span class="sxs-lookup"><span data-stu-id="30b20-122">Use the following procedures to complete these primary tasks.</span></span>

<span data-ttu-id="30b20-123">**Remarques**  Même si vous pouvez publier les applications à l’aide de plusieurs méthodes différentes, les procédures suivantes sont basées sur l’utilisation d’un serveur d’administration d’applications-V pour la publication.</span><span class="sxs-lookup"><span data-stu-id="30b20-123">**Note** Although you can publish the applications by using several different methods, the following procedures are based on your using an App-V Management Server for publishing.</span></span>

 

**<span data-ttu-id="30b20-124">Pour configurer le cache en lecture seule pour le déploiement initial</span><span class="sxs-lookup"><span data-stu-id="30b20-124">To configure the read-only cache for initial deployment</span></span>**

1. <span data-ttu-id="30b20-125">Configurez et configurez un serveur de gestion d’application-V pour la prise en charge de l’authentification des utilisateurs et de la publication.</span><span class="sxs-lookup"><span data-stu-id="30b20-125">Set up and configure an App-V Management Server to provide user authentication and publishing support.</span></span>

2. <span data-ttu-id="30b20-126">Remplissez le dossier de contenu de ce serveur de gestion avec tous les packages d’application requis pour tous les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="30b20-126">Populate the Content folder of this Management Server with all the application packages required for all users.</span></span>

3. <span data-ttu-id="30b20-127">Configurer un ordinateur intermédiaire sur lequel le client App-V est installé.</span><span class="sxs-lookup"><span data-stu-id="30b20-127">Set up a staging computer that has the App-V Client installed.</span></span> <span data-ttu-id="30b20-128">Connectez-vous à l’ordinateur intermédiaire à l’aide d’un compte qui a accès à toutes les applications de sorte que l’ensemble complet d’applications soit publié sur l’ordinateur, puis diffusez le cache des applications afin qu’elles soient entièrement chargées.</span><span class="sxs-lookup"><span data-stu-id="30b20-128">Log on to the staging computer by using an account that has access to all applications so that the complete set of applications are published to the computer, and then stream the applications to cache so that they are fully loaded.</span></span>

   **<span data-ttu-id="30b20-129">Important</span><span class="sxs-lookup"><span data-stu-id="30b20-129">Important</span></span>**  
   <span data-ttu-id="30b20-130">L’ordinateur intermédiaire doit utiliser le même type de système d’exploitation et l’même architecture système que ceux utilisés par les VM sur lesquelles le client App-V sera exécuté.</span><span class="sxs-lookup"><span data-stu-id="30b20-130">The staging computer must use the same operating system type and system architecture as those used by the VMs on which the App-V Client will run.</span></span>

     

4. <span data-ttu-id="30b20-131">Redémarrez l’ordinateur intermédiaire en mode sans échec pour vous assurer que les pilotes ne sont pas démarrés, car cela verrouille le fichier du cache.</span><span class="sxs-lookup"><span data-stu-id="30b20-131">Restart the staging computer in safe mode to make sure that the drivers are not started, because this would lock the cache file.</span></span>

   **<span data-ttu-id="30b20-132">Remarque</span><span class="sxs-lookup"><span data-stu-id="30b20-132">Note</span></span>**  
   <span data-ttu-id="30b20-133">Vous pouvez ou arrêter d’arrêter et de désactiver le service de virtualisation des applications, puis redémarrez l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="30b20-133">Or, you can stop and disable the Application Virtualization service, and then restart the computer.</span></span> <span data-ttu-id="30b20-134">Après avoir copié le fichier, n’oubliez pas d’activer et de redémarrer le service.</span><span class="sxs-lookup"><span data-stu-id="30b20-134">After the file is copied, remember to enable and start the service again.</span></span>

     

5. <span data-ttu-id="30b20-135">Copiez le fichier cache Sftfs. FSD sur un réseau SAN sur lequel tous les serveurs RDS peuvent y accéder, par exemple dans un dossier partagé.</span><span class="sxs-lookup"><span data-stu-id="30b20-135">Copy the Sftfs.fsd cache file to a SAN where all the RDS servers can access it, such as in a shared folder.</span></span> <span data-ttu-id="30b20-136">Définissez les autorisations d’accès aux dossiers sur lecture seule pour le groupe tout le monde et sur contrôle total pour les administrateurs qui gèrent les mises à jour de fichier cache.</span><span class="sxs-lookup"><span data-stu-id="30b20-136">Set the folder access permissions to Read-only for the group Everyone and to Full Control for administrators who will manage the cache file updates.</span></span> <span data-ttu-id="30b20-137">L’emplacement du fichier cache peut être obtenu à partir de l’AppFS\\FileName. de Registre</span><span class="sxs-lookup"><span data-stu-id="30b20-137">The location of the cache file can be obtained from the registry AppFS\\FileName.</span></span>

   **<span data-ttu-id="30b20-138">Important</span><span class="sxs-lookup"><span data-stu-id="30b20-138">Important</span></span>**  
   <span data-ttu-id="30b20-139">Le fichier FSD doit être placé dans un emplacement dont la réactivité et la fiabilité sont égales aux performances de stockage attachées localement, par exemple un réseau SAN.</span><span class="sxs-lookup"><span data-stu-id="30b20-139">You must put the FSD file in a location that has the responsiveness and reliability equal to locally attached storage performance, for example, a SAN.</span></span>

     

6. <span data-ttu-id="30b20-140">Installez le client App-V RDS sur chaque serveur RDS, puis configurez-le pour utiliser le cache en lecture seule en ajoutant les valeurs de clé de Registre suivantes à la clé AppFS sur le client.</span><span class="sxs-lookup"><span data-stu-id="30b20-140">Install the App-V RDS Client on each RDS server, and then configure it to use the read-only cache by adding the following registry key values to the AppFS key on the client.</span></span> <span data-ttu-id="30b20-141">La clé AppFS est située dans HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\\] Microsoft\\SoftGrid\\4.5\\Client\\AppFS pour les ordinateurs 32 bits et dans HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS pour les ordinateurs 64 bits.</span><span class="sxs-lookup"><span data-stu-id="30b20-141">The AppFS key is located at HKEY\_LOCAL\_MACHINE\\SOFTWARE\\\]Microsoft\\SoftGrid\\4.5\\Client\\AppFS for 32-bit computers and at HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS for 64-bit computers.</span></span>

   <table>
   <colgroup>
   <col width="25%" />
   <col width="25%" />
   <col width="25%" />
   <col width="25%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="30b20-142">Clé</span><span class="sxs-lookup"><span data-stu-id="30b20-142">Key</span></span></th>
   <th align="left"><span data-ttu-id="30b20-143">Type</span><span class="sxs-lookup"><span data-stu-id="30b20-143">Type</span></span></th>
   <th align="left"><span data-ttu-id="30b20-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="30b20-144">Value</span></span></th>
   <th align="left"><span data-ttu-id="30b20-145">Objectif</span><span class="sxs-lookup"><span data-stu-id="30b20-145">Purpose</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="30b20-146">FileName</span><span class="sxs-lookup"><span data-stu-id="30b20-146">FileName</span></span></p></td>
   <td align="left"><p><span data-ttu-id="30b20-147">String</span><span class="sxs-lookup"><span data-stu-id="30b20-147">String</span></span></p></td>
   <td align="left"><p><span data-ttu-id="30b20-148">chemin de FSD</span><span class="sxs-lookup"><span data-stu-id="30b20-148">path of FSD</span></span></p></td>
   <td align="left"><p><span data-ttu-id="30b20-149">Spécifie le chemin d’accès du fichier cache partagé, par exemple \RDSServername\Sharefolder\SFTFS. FSD (obligatoire).</span><span class="sxs-lookup"><span data-stu-id="30b20-149">Specifies the path of the shared cache file, for example, \RDSServername\Sharefolder\SFTFS.FSD (Required).</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="30b20-150">ReadOnlyFSD</span><span class="sxs-lookup"><span data-stu-id="30b20-150">ReadOnlyFSD</span></span></p></td>
   <td align="left"><p><span data-ttu-id="30b20-151">DWORD</span><span class="sxs-lookup"><span data-stu-id="30b20-151">DWORD</span></span></p></td>
   <td align="left"><p><span data-ttu-id="30b20-152">1</span><span class="sxs-lookup"><span data-stu-id="30b20-152">1</span></span></p></td>
   <td align="left"><p><span data-ttu-id="30b20-153">Configure le client pour qu’il fonctionne en mode lecture seule.</span><span class="sxs-lookup"><span data-stu-id="30b20-153">Configures the client to operate in Read-Only mode.</span></span> <span data-ttu-id="30b20-154">Cela permet de s’assurer que le client n’essaiera pas de transmettre les mises à jour au cache du package.</span><span class="sxs-lookup"><span data-stu-id="30b20-154">This ensures that the client will not try to stream updates to the package cache.</span></span> <span data-ttu-id="30b20-155">(obligatoire)</span><span class="sxs-lookup"><span data-stu-id="30b20-155">(Required)</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="30b20-156">ErrorLogLocation</span><span class="sxs-lookup"><span data-stu-id="30b20-156">ErrorLogLocation</span></span></p></td>
   <td align="left"><p><span data-ttu-id="30b20-157">String</span><span class="sxs-lookup"><span data-stu-id="30b20-157">String</span></span></p></td>
   <td align="left"><p><span data-ttu-id="30b20-158">chemin du fichier journal des erreurs (. ETL)</span><span class="sxs-lookup"><span data-stu-id="30b20-158">path of error log (.etl) file</span></span></p></td>
   <td align="left"><p><span data-ttu-id="30b20-159">Entrée utilisée pour spécifier le chemin d’accès du journal des erreurs.</span><span class="sxs-lookup"><span data-stu-id="30b20-159">Entry used to specify the path of the error log.</span></span> <span data-ttu-id="30b20-160">Recommande.</span><span class="sxs-lookup"><span data-stu-id="30b20-160">(Recommended.</span></span> <span data-ttu-id="30b20-161">Utiliser un chemin d’accès local tel que C:\Logs\Sftfs.etl).</span><span class="sxs-lookup"><span data-stu-id="30b20-161">Use a local path such as C:\Logs\Sftfs.etl).</span></span></p></td>
   </tr>
   </tbody>
   </table>

     

7. <span data-ttu-id="30b20-162">Configurez chaque serveur RDS dans la batterie de serveurs pour utiliser le serveur de publication et utiliser la mise à jour de publication lorsque les utilisateurs se connectent.</span><span class="sxs-lookup"><span data-stu-id="30b20-162">Configure each RDS server in the farm to use the publishing server and to use publishing update when users log on.</span></span> <span data-ttu-id="30b20-163">Lorsque l’utilisateur se connecte aux serveurs RDS, un cycle de mise à jour de publication se produit et publie toutes les applications pour lesquelles son compte est autorisé.</span><span class="sxs-lookup"><span data-stu-id="30b20-163">As users log on to the RDS servers, a publishing update cycle occurs and publishes all the applications for which their account is authorized.</span></span> <span data-ttu-id="30b20-164">Ces applications sont exécutées à partir du cache partagé.</span><span class="sxs-lookup"><span data-stu-id="30b20-164">These applications are run from the shared cache.</span></span>

**<span data-ttu-id="30b20-165">Pour configurer le client RDS pour la mise à niveau du package</span><span class="sxs-lookup"><span data-stu-id="30b20-165">To configure the RDS client for package upgrade</span></span>**

1.  <span data-ttu-id="30b20-166">Effectuez la mise à niveau et le test du package d’application.</span><span class="sxs-lookup"><span data-stu-id="30b20-166">Complete the upgrade and testing of the application package.</span></span>

2.  <span data-ttu-id="30b20-167">Mettez à niveau le package sur le serveur App-V.</span><span class="sxs-lookup"><span data-stu-id="30b20-167">Upgrade the package on the App-V server.</span></span> <span data-ttu-id="30b20-168">Ensuite, publiez et diffusez la nouvelle version des applications sur le client de l’ordinateur intermédiaire de sorte qu’elles soient entièrement chargées dans le cache.</span><span class="sxs-lookup"><span data-stu-id="30b20-168">Then, publish and stream the new version of the applications to the client on the staging computer so that they are fully loaded into cache.</span></span>

3.  <span data-ttu-id="30b20-169">Redémarrez l’ordinateur intermédiaire en mode sans échec pour vous assurer que les pilotes ne sont pas démarrés.</span><span class="sxs-lookup"><span data-stu-id="30b20-169">Restart the staging computer in safe mode to ensure the drivers are not started.</span></span>

    <span data-ttu-id="30b20-170">**Remarques**  Vous pouvez ou arrêter d’abord le service de virtualisation des applications dans services. msc, puis le redémarrer.</span><span class="sxs-lookup"><span data-stu-id="30b20-170">**Note** Or, you can first stop and then disable the Application Virtualization service in the Services.msc, and restart the computer.</span></span> <span data-ttu-id="30b20-171">Après avoir copié le fichier, n’oubliez pas d’activer et de redémarrer le service.</span><span class="sxs-lookup"><span data-stu-id="30b20-171">After the file has been copied, remember to enable and start the service again.</span></span>

     

4.  <span data-ttu-id="30b20-172">Copiez le fichier cache Sftfs. FSD sur un réseau SAN sur lequel tous les serveurs RDS peuvent y accéder, par exemple dans un dossier partagé.</span><span class="sxs-lookup"><span data-stu-id="30b20-172">Copy the Sftfs.fsd cache file to a SAN where all the RDS servers can access it, such as in a shared folder.</span></span> <span data-ttu-id="30b20-173">Vous pouvez utiliser un autre nom de fichier, par exemple, SFTFS \ _V2. FSD, pour distinguer la nouvelle version.</span><span class="sxs-lookup"><span data-stu-id="30b20-173">You can use a different file name, for example, SFTFS\_V2.FSD, to distinguish the new version.</span></span>

5.  <span data-ttu-id="30b20-174">Pour configurer le client RDS App-V sur chaque serveur RDS dans la batterie de serveurs pour qu’il utilise le fichier cache partagé mis à jour, modifiez la valeur nom de fichier de la clé de Registre AppFS pour qu’elle pointe vers l’emplacement du fichier mis à jour, par exemple, \\\\RDSServername\\Sharefolder\\SFTFS\ _V2. FSD.</span><span class="sxs-lookup"><span data-stu-id="30b20-174">To configure the App-V RDS Client on each RDS server in the farm to use the updated shared cache file, change the AppFS registry key FILENAME value to point to the location of the updated file, for example, \\\\RDSServername\\Sharefolder\\SFTFS\_V2.FSD.</span></span> <span data-ttu-id="30b20-175">Cela garantit que chaque serveur RDS reçoit la copie mise à jour du cache lorsque les pilotes d’application-vclient redémarrent.</span><span class="sxs-lookup"><span data-stu-id="30b20-175">This guarantees that each RDS server receives the updated copy of the cache when the App-Vclient drivers restart.</span></span>

    <span data-ttu-id="30b20-176">**Important**  Vous devez redémarrer les serveurs RDS pour pouvoir utiliser le fichier cache partagé mis à jour.</span><span class="sxs-lookup"><span data-stu-id="30b20-176">**Important** You must restart the RDS servers in order to use the updated shared cache file.</span></span>

     

## <span data-ttu-id="30b20-177">Utiliser des liens symboliques lors de la mise à niveau du cache</span><span class="sxs-lookup"><span data-stu-id="30b20-177">How to Use Symbolic Links when Upgrading the Cache</span></span>


<span data-ttu-id="30b20-178">Au lieu de modifier la valeur de nom de fichier de la clé AppFS chaque fois qu’un nouveau fichier de cache est déployé contenant des packages nouveaux ou mis à niveau, vous pouvez utiliser un lien symbolique dans les systèmes d’exploitation suivants: Windows Vista, Windows 7 et Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="30b20-178">Instead of changing the AppFS key FILENAME value every time that a new cache file is deployed that contains new or upgraded packages, you can use a symbolic link in the following operating systems: Windows Vista, Windows 7, and Windows Server 2008.</span></span> <span data-ttu-id="30b20-179">Pour plus d’informations sur les liens symboliques, voir [liens symboliques](https://go.microsoft.com/fwlink/?LinkId=157626) ( https://go.microsoft.com/fwlink/?LinkId=157626) .</span><span class="sxs-lookup"><span data-stu-id="30b20-179">For more information about symbolic links, see [Symbolic Links](https://go.microsoft.com/fwlink/?LinkId=157626) (https://go.microsoft.com/fwlink/?LinkId=157626).</span></span> <span data-ttu-id="30b20-180">En revanche, Windows XP ne prend pas en charge l’utilisation de liens symboliques et vous devez plutôt utiliser des points de jonction.</span><span class="sxs-lookup"><span data-stu-id="30b20-180">In contrast, Windows XP does not support the use of symbolic links, and you must use junction points instead.</span></span> <span data-ttu-id="30b20-181">Pour plus d’informations sur les jointures, reportez-vous à [l’article 205524](https://go.microsoft.com/fwlink/?LinkId=182553) de la base de connaissances Microsoft ( https://go.microsoft.com/fwlink/?LinkId=182553) et également à la jointure d’outil [v 1.05](https://go.microsoft.com/fwlink/?LinkId=182554) () https://go.microsoft.com/fwlink/?LinkId=182554) .</span><span class="sxs-lookup"><span data-stu-id="30b20-181">For more information about junctions, see [article 205524](https://go.microsoft.com/fwlink/?LinkId=182553) in the Microsoft Knowledge Base (https://go.microsoft.com/fwlink/?LinkId=182553), and also the tool [Junction v1.05](https://go.microsoft.com/fwlink/?LinkId=182554) (https://go.microsoft.com/fwlink/?LinkId=182554).</span></span>

**<span data-ttu-id="30b20-182">Pour configurer un lien symbolique pour référencer le cache</span><span class="sxs-lookup"><span data-stu-id="30b20-182">To configure a symbolic link to reference the cache</span></span>**

1.  <span data-ttu-id="30b20-183">Pendant la phase de déploiement initiale, ouvrez une fenêtre d’invite de commandes en tant qu’administrateur local sur le système d’exploitation hôte du serveur RDS.</span><span class="sxs-lookup"><span data-stu-id="30b20-183">During the initial deployment stage, open a Command Prompt window as a local administrator on the RDS server host operating system.</span></span>

2.  <span data-ttu-id="30b20-184">Créez un lien symbolique à l’aide de la commande MKLINK, puis configurez-le pour qu’il pointe sur le fichier Sftfs. FSD.</span><span class="sxs-lookup"><span data-stu-id="30b20-184">Create a symbolic link by using the MKLINK command, and then configure it to point to the Sftfs.fsd file.</span></span>

    **     <span data-ttu-id="30b20-185">mklink symlinkname \\\\rdshostserver\\sharefolder\\sftfs.fsd</span><span class="sxs-lookup"><span data-stu-id="30b20-185">mklink symlinkname \\\\rdshostserver\\sharefolder\\sftfs.fsd</span></span>**

3.  <span data-ttu-id="30b20-186">Sur l’image de l’ordinateur virtuel VDI maître, ouvrez une fenêtre d’invite de commandes à l’aide de l’option **exécuter en tant qu’administrateur** , puis accordez des autorisations de lien distant pour permettre à l’ordinateur virtuel d’accéder au lien symbolique du système d’exploitation de l’hôte VDI.</span><span class="sxs-lookup"><span data-stu-id="30b20-186">On the VDI Master VM Image, open a Command Prompt window by using the **Run as administrator** option and grant remote link permissions so that the VM can access the symbolic link on the VDI Host operating system.</span></span> <span data-ttu-id="30b20-187">Par défaut, les autorisations de liaison distantes ne sont pas activées.</span><span class="sxs-lookup"><span data-stu-id="30b20-187">By default, remote link permissions are disabled.</span></span>

    **<span data-ttu-id="30b20-188">fsutil behavior Set SymlinkEvaluation R2R: 1</span><span class="sxs-lookup"><span data-stu-id="30b20-188">fsutil behavior set SymlinkEvaluation R2R:1</span></span>**

    <span data-ttu-id="30b20-189">**Remarques**  Sur le serveur de stockage, les autorisations de liaison appropriées doivent être activées.</span><span class="sxs-lookup"><span data-stu-id="30b20-189">**Note** On the storage server, appropriate link permissions must be enabled.</span></span> <span data-ttu-id="30b20-190">En fonction de l’emplacement du lien et du fichier Sftfs. FSD, les autorisations sont **L2L: 1** ou **L2R: 1** ou **R2L: 1** ou **R2R: 1**.</span><span class="sxs-lookup"><span data-stu-id="30b20-190">Depending on the location of link and the Sftfs.fsd file, the permissions are **L2L:1** or **L2R:1** or **R2L:1** or **R2R:1**.</span></span>

     

4.  <span data-ttu-id="30b20-191">Lorsque vous configurez le client RDS App-V, définissez la valeur nom de fichier clé AppFS sur le chemin d’accès UNC du fichier FSD qui utilise le lien symbolique.</span><span class="sxs-lookup"><span data-stu-id="30b20-191">When you configure the App-V RDS Client, set the AppFS key FILENAME value equal to the UNC path of the FSD file that is using the symbolic link.</span></span> <span data-ttu-id="30b20-192">Par exemple, définissez le nom de fichier sur \\\\VDIHostserver\\Symlinkname.</span><span class="sxs-lookup"><span data-stu-id="30b20-192">For example, set the file name to \\\\VDIHostserver\\Symlinkname.</span></span> <span data-ttu-id="30b20-193">Lorsque le client App-V accède au cache pour la première fois, le lien symbolique passe au client un handle vers le fichier du cache.</span><span class="sxs-lookup"><span data-stu-id="30b20-193">When the App-V client first accesses the cache, the symbolic link passes to the client a handle to the cache file.</span></span> <span data-ttu-id="30b20-194">Le client continue d’utiliser ce handle tant que le client est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="30b20-194">The client continues to use that handle as long as the client is running.</span></span> <span data-ttu-id="30b20-195">La valeur du lien symbolique peut être mise à jour en toute sécurité même si l’ancien cache partagé est ouvert.</span><span class="sxs-lookup"><span data-stu-id="30b20-195">The value of the symbolic link can safely be updated even if existing clients have the old shared cache open.</span></span>

5.  <span data-ttu-id="30b20-196">Lorsque vous devez mettre à niveau un package ou ajouter un nouveau package au cache, suivez les étapes 1 à 4 de la procédure de mise à niveau.</span><span class="sxs-lookup"><span data-stu-id="30b20-196">When you must upgrade a package or to add a new package to the cache, follow steps 1 through 4 of the upgrade procedure.</span></span> <span data-ttu-id="30b20-197">Ensuite, supprimez le lien symbolique et recréez-le pour qu’il pointe vers la nouvelle version du fichier cache partagé.</span><span class="sxs-lookup"><span data-stu-id="30b20-197">Then, delete the symbolic link and re-create it to point to the new version of the shared cache file.</span></span> <span data-ttu-id="30b20-198">Ainsi, chaque serveur RDS reçoit la copie mise à jour du cache lors du redémarrage des pilotes clients App-V.</span><span class="sxs-lookup"><span data-stu-id="30b20-198">This guarantees that each RDS server receives the updated copy of the cache when the App-V client drivers restart.</span></span> <span data-ttu-id="30b20-199">Lorsque le serveur RDS est redémarré, le client App-V reçoit un handle vers la copie mise à jour du cache, car le client utilise le chemin d’accès contenant le lien symbolique mis à jour.</span><span class="sxs-lookup"><span data-stu-id="30b20-199">When the RDS server is restarted, the App-V client receives a handle to the updated copy of the cache because the client uses the path that contains the updated symbolic link.</span></span> <span data-ttu-id="30b20-200">Les utilisateurs ont ensuite accès aux applications nouvelles et mises à jour.</span><span class="sxs-lookup"><span data-stu-id="30b20-200">Then, the users have access to the new and updated applications.</span></span>

## <span data-ttu-id="30b20-201">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="30b20-201">Related topics</span></span>


[<span data-ttu-id="30b20-202">Procédure pour installer le serveur Application Virtualization Management Server</span><span class="sxs-lookup"><span data-stu-id="30b20-202">How to Install Application Virtualization Management Server</span></span>](how-to-install-application-virtualization-management-server.md)

[<span data-ttu-id="30b20-203">Procédure pour installer manuellement Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="30b20-203">How to Manually Install the Application Virtualization Client</span></span>](how-to-manually-install-the-application-virtualization-client.md)

[<span data-ttu-id="30b20-204">Procédure pour installer le client via la ligne de commande</span><span class="sxs-lookup"><span data-stu-id="30b20-204">How to Install the Client by Using the Command Line</span></span>](how-to-install-the-client-by-using-the-command-line-new.md)

 

 





