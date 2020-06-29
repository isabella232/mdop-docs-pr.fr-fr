---
title: Méthodes de synchronisation pour UE-V2.x
description: Méthodes de synchronisation pour UE-V2.x
author: dansimp
ms.assetid: af0ae894-dfdc-41d2-927b-c2ab1b355ffe
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a163442e2ab3dbd777aca133b13b0086cdb8ae1a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810038"
---
# <span data-ttu-id="027e0-103">Méthodes de synchronisation pour UE-V2.x</span><span class="sxs-lookup"><span data-stu-id="027e0-103">Sync Methods for UE-V 2.x</span></span>


<span data-ttu-id="027e0-104">L’agent Microsoft User Interface Virtualization (UE-V) 2,0, 2,1 et 2,1 SP1 vous permet de synchroniser les paramètres d’application et de Windows de l’utilisateur avec l’emplacement de stockage des paramètres.</span><span class="sxs-lookup"><span data-stu-id="027e0-104">The Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, and 2.1 SP1 Agent lets you synchronize users’ application and Windows settings with the settings storage location.</span></span> <span data-ttu-id="027e0-105">La configuration de la *méthode de synchronisation* définit le mode de chargement et de téléchargement de ces paramètres dans l’emplacement de stockage des paramètres.</span><span class="sxs-lookup"><span data-stu-id="027e0-105">The *Sync Method* configuration defines how the UE-V Agent uploads and downloads those settings to the settings storage location.</span></span> <span data-ttu-id="027e0-106">UE-V 2. x introduit un nouveau PowerSchool appelé *SyncProvider*.</span><span class="sxs-lookup"><span data-stu-id="027e0-106">UE-V 2.x introduces a new SyncMethod called the *SyncProvider*.</span></span> <span data-ttu-id="027e0-107">Pour plus d’informations sur les événements de déclenchement qui démarrent la synchronisation des paramètres d’application et de fenêtre, voir [événements de déclencheurs de synchronisation pour UE-V 2. x](sync-trigger-events-for-ue-v-2x-both-uevv2.md).</span><span class="sxs-lookup"><span data-stu-id="027e0-107">For more information about trigger events that start the synchronization of application and Windows settings, see [Sync Trigger Events for UE-V 2.x](sync-trigger-events-for-ue-v-2x-both-uevv2.md).</span></span>

## <span data-ttu-id="027e0-108">Configuration de PowerSchool</span><span class="sxs-lookup"><span data-stu-id="027e0-108">SyncMethod Configuration</span></span>


<span data-ttu-id="027e0-109">Le tableau suivant décrit les modifications apportées à PowerSchool de UE-V v 1.0 à v 2.0 à v 2.1, ainsi que les paramètres de chaque configuration:</span><span class="sxs-lookup"><span data-stu-id="027e0-109">This table explains the changes to SyncMethod from UE-V v1.0 to v2.0 to v2.1, as well as the settings for each configuration:</span></span>

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="027e0-110">Configuration de PowerSchool</span><span class="sxs-lookup"><span data-stu-id="027e0-110">SyncMethod Configuration</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="027e0-111">V 1.0</span><span class="sxs-lookup"><span data-stu-id="027e0-111">V1.0</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="027e0-112">V 2.0</span><span class="sxs-lookup"><span data-stu-id="027e0-112">V2.0</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="027e0-113">V 2.1 et V 2.1 SP1</span><span class="sxs-lookup"><span data-stu-id="027e0-113">V2.1 and V2.1 SP1</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="027e0-114">Description</span><span class="sxs-lookup"><span data-stu-id="027e0-114">Description</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="027e0-115">SyncProvider</span><span class="sxs-lookup"><span data-stu-id="027e0-115">SyncProvider</span></span></p></td>
<td align="left"><p><span data-ttu-id="027e0-116">Non applicable</span><span class="sxs-lookup"><span data-stu-id="027e0-116">n/a</span></span></p></td>
<td align="left"><p><span data-ttu-id="027e0-117">Par défaut</span><span class="sxs-lookup"><span data-stu-id="027e0-117">Default</span></span></p></td>
<td align="left"><p><span data-ttu-id="027e0-118">Par défaut</span><span class="sxs-lookup"><span data-stu-id="027e0-118">Default</span></span></p></td>
<td align="left"><p><span data-ttu-id="027e0-119">Les modifications apportées aux paramètres d’une application spécifique ou des paramètres globaux de bureau Windows sont enregistrés localement dans un dossier cache.</span><span class="sxs-lookup"><span data-stu-id="027e0-119">Settings changes for a specific application or for global Windows desktop settings are saved locally to a cache folder.</span></span> <span data-ttu-id="027e0-120">Ces modifications sont ensuite synchronisées avec l’emplacement de stockage des paramètres lorsqu’un événement de déclenchement de synchronisation intervient.</span><span class="sxs-lookup"><span data-stu-id="027e0-120">These changes are then synchronized with the settings storage location when a synchronization trigger event takes place.</span></span> <span data-ttu-id="027e0-121">Le fait de transférer les modifications enregistre les modifications locales apportées au chemin de stockage des paramètres.</span><span class="sxs-lookup"><span data-stu-id="027e0-121">Pushing out changes will save the local changes to the settings storage path.</span></span></p>
<p><span data-ttu-id="027e0-122">Ce paramètre par défaut est la norme d’or pour les ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="027e0-122">This default setting is the gold standard for computers.</span></span> <span data-ttu-id="027e0-123">Cette option tente de synchroniser ce paramètre et expire après un court délai pour s’assurer que le démarrage de l’application ou du système d’exploitation n’est pas retardé pendant un certain temps.</span><span class="sxs-lookup"><span data-stu-id="027e0-123">This option attempts to synchronize the setting and times out after a short delay to ensure that the application or operating system startup isn’t delayed for a long period of time.</span></span></p>
<p><span data-ttu-id="027e0-124">Cette fonctionnalité est également liée à l’application tâche planifiée – contrôleur de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="027e0-124">This functionality is also tied to the Scheduled task – Sync Controller Application.</span></span> <span data-ttu-id="027e0-125">L’administrateur contrôle la fréquence de la tâche planifiée.</span><span class="sxs-lookup"><span data-stu-id="027e0-125">The administrator controls the frequency of the Scheduled task.</span></span> <span data-ttu-id="027e0-126">Par défaut, les ordinateurs synchronisent leurs paramètres toutes les 30 minutes après la connexion.</span><span class="sxs-lookup"><span data-stu-id="027e0-126">By default, computers synchronize their settings every 30 min after logging on.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="027e0-127">OfflineFiles</span><span class="sxs-lookup"><span data-stu-id="027e0-127">OfflineFiles</span></span></p></td>
<td align="left"><p><span data-ttu-id="027e0-128">Par défaut</span><span class="sxs-lookup"><span data-stu-id="027e0-128">Default</span></span></p></td>
<td align="left"><p><span data-ttu-id="027e0-129">Obsolète</span><span class="sxs-lookup"><span data-stu-id="027e0-129">Deprecated</span></span></p></td>
<td align="left"><p><span data-ttu-id="027e0-130">Obsolète</span><span class="sxs-lookup"><span data-stu-id="027e0-130">Deprecated</span></span></p></td>
<td align="left"><p><span data-ttu-id="027e0-131">Se comporte comme SyncProvider dans V 2.0.</span><span class="sxs-lookup"><span data-stu-id="027e0-131">Behaves the same as SyncProvider in V2.0.</span></span></p>
<p><span data-ttu-id="027e0-132">Si les fichiers hors connexion sont activés et que le dossier est épinglé, UE-V détachera ce dossier et sera synchronisé directement avec le répertoire central SMB.</span><span class="sxs-lookup"><span data-stu-id="027e0-132">If Offline files are enabled and the folder is pinned then UE-V will unpin this folder and sync directly to the central SMB directory.</span></span></p>
<p><strong><span data-ttu-id="027e0-133">Remarque: </strong> si vous souhaitez utiliser UE-V dans un bureau d’assurance (ou en déplacement avec un ordinateur portable), vous pouvez utiliser les fichiers hors connexion pour vous assurer que vos paramètres sont itinérants.</span><span class="sxs-lookup"><span data-stu-id="027e0-133">NOTE:</strong> In V1.0 if you wanted to use UE-V in a CorpNet disconnected manner (aka traveling with a Laptop), then the guidance is to use Offline Files to ensure that your settings roamed.</span></span><span data-ttu-id="027e0-134">Nous avons reçu suffisamment de commentaires clientèle pour l’activation de fichiers hors connexion.</span><span class="sxs-lookup"><span data-stu-id="027e0-134"> We received sufficient customer feedback that turning on Offline files is a non-trivial enterprise blocker.</span></span> <span data-ttu-id="027e0-135">Par conséquent, dans UE-V 2, nous avons créé un moteur de synchronisation étroitement couplé pour mettre en cache vos données localement et synchroniser les paramètres avec le serveur central.</span><span class="sxs-lookup"><span data-stu-id="027e0-135">So in UE-V 2, we created a tightly coupled synchronization engine to cache your data locally and synchronize the settings to the central server.</span></span> <span data-ttu-id="027e0-136">Cette zone de fonctionnalité ne remplace pas les fichiers hors connexion ou la redirection de dossier.</span><span class="sxs-lookup"><span data-stu-id="027e0-136">This feature area does not replace Offline Files or Folder Redirection.</span></span></p>
<p><span data-ttu-id="027e0-137">UE-V 2 ne fonctionne pas correctement avec les dossiers en mode hors connexion, de sorte que les recommandations ne permettent pas de définir le chemin de stockage des paramètres sur un dossier en mode hors connexion ou CSC épinglé.</span><span class="sxs-lookup"><span data-stu-id="027e0-137">UE-V 2 does not work well with Offline folders so the guidance is not to set the settings storage path to a pinned Offline or CSC folder.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="027e0-138">Externe</span><span class="sxs-lookup"><span data-stu-id="027e0-138">External</span></span></p></td>
<td align="left"><p><span data-ttu-id="027e0-139">Non applicable</span><span class="sxs-lookup"><span data-stu-id="027e0-139">n/a</span></span></p></td>
<td align="left"><p><span data-ttu-id="027e0-140">Non applicable</span><span class="sxs-lookup"><span data-stu-id="027e0-140">n/a</span></span></p></td>
<td align="left"><p><span data-ttu-id="027e0-141">Pris en charge</span><span class="sxs-lookup"><span data-stu-id="027e0-141">Supported</span></span></p></td>
<td align="left"><p><span data-ttu-id="027e0-142">Dans le cadre de la nouvelle version d’UE-V 2,1, cette méthode de configuration spécifie que si les paramètres UE-V sont écrits dans un dossier local sur l’ordinateur de l’utilisateur, tout moteur de synchronisation externe (par exemple, OneDrive entreprise, dossiers de travail, SharePoint ou Dropbox) peut être utilisé pour appliquer ces paramètres aux différents ordinateurs auxquels les utilisateurs accèdent.</span><span class="sxs-lookup"><span data-stu-id="027e0-142">New in UE-V 2.1, this configuration method specifies that if UE-V settings are written to a local folder on the user computer, then any external sync engine (such as OneDrive for Business, Work Folders, Sharepoint, or Dropbox) can be used to apply these settings to the different computers that users access.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="027e0-143">None</span><span class="sxs-lookup"><span data-stu-id="027e0-143">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="027e0-144">Oui</span><span class="sxs-lookup"><span data-stu-id="027e0-144">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="027e0-145">Oui</span><span class="sxs-lookup"><span data-stu-id="027e0-145">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="027e0-146">Oui</span><span class="sxs-lookup"><span data-stu-id="027e0-146">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="027e0-147">Ce paramètre de configuration est conçu pour les applications VDI (Virtual Desktop Infrastructure) et en flux.</span><span class="sxs-lookup"><span data-stu-id="027e0-147">This configuration setting is designed for the Virtual Desktop Infrastructure (VDI) and Streamed Application experience primarily.</span></span> <span data-ttu-id="027e0-148">Ce paramètre doit être utilisé dans les zones Windows Server utilisées dans un centre de stockage, où la connexion sera toujours disponible.</span><span class="sxs-lookup"><span data-stu-id="027e0-148">This setting should be used on Windows Server boxes used in a datacenter, where the connection will always be available.</span></span></p>
<p><span data-ttu-id="027e0-149">Les modifications apportées aux paramètres sont enregistrées directement sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="027e0-149">Any settings changes are saved directly to the server.</span></span> <span data-ttu-id="027e0-150">Si la connexion réseau au chemin de stockage des paramètres n’est pas disponible, les modifications apportées aux paramètres sont mises en cache sur l’appareil et sont synchronisées lors de la prochaine exécution du fournisseur de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="027e0-150">If the network connection to the settings storage path is not available, then the settings changes are cached on the device and are synchronized the next time that the Sync Provider runs.</span></span> <span data-ttu-id="027e0-151">Si le chemin d’accès de stockage des paramètres est introuvable et que le profil utilisateur est supprimé d’un environnement VDI en pool lors de la fermeture de session, ces modifications de paramètres sont perdues et l’utilisateur doit réappliquer la modification lorsque l’ordinateur peut à nouveau joindre le chemin de stockage des paramètres.</span><span class="sxs-lookup"><span data-stu-id="027e0-151">If the settings storage path is not found and the user profile is removed from a pooled VDI environment on logoff, then these settings changes are lost, and the user must reapply the change when the computer can again reach the settings storage path.</span></span></p>
<p><span data-ttu-id="027e0-152">Les applications et le système d’exploitation attendent indéfiniment de la présence de l’emplacement.</span><span class="sxs-lookup"><span data-stu-id="027e0-152">Apps and OS will wait indefinitely for the location to be present.</span></span> <span data-ttu-id="027e0-153">Cela peut entraîner une augmentation spectaculaire du temps de chargement de l’application ou du système d’exploitation si l’emplacement est introuvable.</span><span class="sxs-lookup"><span data-stu-id="027e0-153">This could cause App load or OS logon time to dramatically increase if the location is not found.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="027e0-154">Vous pouvez configurer la méthode de synchronisation de différentes manières:</span><span class="sxs-lookup"><span data-stu-id="027e0-154">You can configure the sync method in these ways:</span></span>

-   <span data-ttu-id="027e0-155">Lorsque vous [déployez l’agent UE-V](https://technet.microsoft.com/library/dn458891.aspx#agent) par le biais d’un paramètre de ligne de commande ou d’un script de commandes</span><span class="sxs-lookup"><span data-stu-id="027e0-155">When you [Deploy the UE-V Agent](https://technet.microsoft.com/library/dn458891.aspx#agent) through a command-line parameter or in a batch script</span></span>

-   <span data-ttu-id="027e0-156">Par le biais des paramètres de [stratégie de groupe](https://technet.microsoft.com/library/dn458893.aspx)</span><span class="sxs-lookup"><span data-stu-id="027e0-156">Through [Group Policy](https://technet.microsoft.com/library/dn458893.aspx) settings</span></span>

-   <span data-ttu-id="027e0-157">[Module System Center Configuration](https://technet.microsoft.com/library/dn458917.aspx) pour UE-V</span><span class="sxs-lookup"><span data-stu-id="027e0-157">With the [System Center Configuration Pack](https://technet.microsoft.com/library/dn458917.aspx) for UE-V</span></span>

-   <span data-ttu-id="027e0-158">Après l’installation de l’agent UE-V, à l’aide de [Windows PowerShell ou WMI (Windows Management Instrumentation)](https://technet.microsoft.com/library/dn458937.aspx)</span><span class="sxs-lookup"><span data-stu-id="027e0-158">After installation of the UE-V Agent, by using [Windows PowerShell or Windows Management Instrumentation (WMI)](https://technet.microsoft.com/library/dn458937.aspx)</span></span>






## <span data-ttu-id="027e0-159">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="027e0-159">Related topics</span></span>


[<span data-ttu-id="027e0-160">Déployer les fonctionnalités UE-V2.x requises</span><span class="sxs-lookup"><span data-stu-id="027e0-160">Deploy Required Features for UE-V 2.x</span></span>](deploy-required-features-for-ue-v-2x-new-uevv2.md#ssl)

[<span data-ttu-id="027e0-161">Déployer les fonctionnalités UE-V2.x requises</span><span class="sxs-lookup"><span data-stu-id="027e0-161">Deploy Required Features for UE-V 2.x</span></span>](deploy-required-features-for-ue-v-2x-new-uevv2.md#config)

[<span data-ttu-id="027e0-162">Informations techniques de référence sur UE-V2.x</span><span class="sxs-lookup"><span data-stu-id="027e0-162">Technical Reference for UE-V 2.x</span></span>](technical-reference-for-ue-v-2x-both-uevv2.md)

 

 





