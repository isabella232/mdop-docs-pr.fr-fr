---
title: Présentation technique d'AGPM
description: Présentation technique d'AGPM
author: dansimp
ms.assetid: 36bc0ab5-f752-474c-8559-721ea95169c2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 0cc635f46c2aabb0c9fa1f472a258a3e65a07b55
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807450"
---
# <span data-ttu-id="ab02f-103">Présentation technique d'AGPM</span><span class="sxs-lookup"><span data-stu-id="ab02f-103">Technical Overview of AGPM</span></span>


<span data-ttu-id="ab02f-104">Microsoft Advanced Group Policy Management (AGPM) est une application client/serveur.</span><span class="sxs-lookup"><span data-stu-id="ab02f-104">Microsoft Advanced Group Policy Management (AGPM) is a client/server application.</span></span> <span data-ttu-id="ab02f-105">Le serveur AGPM stocke les objets de stratégie de groupe hors connexion dans l’archive créée par AGPM sur le système de fichiers du serveur.</span><span class="sxs-lookup"><span data-stu-id="ab02f-105">The AGPM Server stores Group Policy Objects (GPOs) offline in the archive that AGPM creates on the server's file system.</span></span> <span data-ttu-id="ab02f-106">Les administrateurs de stratégie de groupe utilisent le composant logiciel enfichable AGPM pour la console de gestion des stratégies de groupe (GPMC) pour fonctionner avec les objets de stratégie de groupe sur le serveur qui héberge l’archive.</span><span class="sxs-lookup"><span data-stu-id="ab02f-106">Group Policy administrators use the AGPM snap-in for the Group Policy Management Console (GPMC) to work with GPOs on the server that hosts the archive.</span></span> <span data-ttu-id="ab02f-107">Le fait de comprendre les parties d’AGPM et des éléments apparentés, la façon dont les objets de stratégie de groupe peuvent être stockés dans le système de fichiers et la manière dont les autorisations contrôlent les actions disponibles pour chaque rôle d’utilisateur peuvent améliorer l’efficacité des administrateurs de stratégie de groupe pour AGPM.</span><span class="sxs-lookup"><span data-stu-id="ab02f-107">Understanding the parts of AGPM and related items, how they store GPOs in the file system, and how permissions control the actions available to each user role can improve Group Policy administrators' effectiveness with AGPM.</span></span>

## <span data-ttu-id="ab02f-108">Terminology</span><span class="sxs-lookup"><span data-stu-id="ab02f-108">Terminology</span></span>


<span data-ttu-id="ab02f-109">Les informations suivantes décrivent les termes d’AGPM de base.</span><span class="sxs-lookup"><span data-stu-id="ab02f-109">The following explains the basic AGPM terms.</span></span>

-   <span data-ttu-id="ab02f-110">**Client AGPM:** Un ordinateur qui exécute le composant logiciel enfichable AGPM pour la console de gestion des stratégies de groupe (GPMC) et dont les administrateurs de stratégie de groupe gèrent les objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="ab02f-110">**AGPM Client:** A computer that runs the AGPM snap-in for the Group Policy Management Console (GPMC) and from which Group Policy administrators manage GPOs.</span></span>

-   <span data-ttu-id="ab02f-111">**Composant logiciel enfichable AGPM:** Composants logiciels d’AGPM installés sur les clients AGPM de sorte qu’ils puissent gérer des objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="ab02f-111">**AGPM snap-in:** The software component of AGPM installed on AGPM Clients so that they can manage GPOs.</span></span>

-   <span data-ttu-id="ab02f-112">**Serveur AGPM:** Serveur qui exécute le service AGPM et gère une archive.</span><span class="sxs-lookup"><span data-stu-id="ab02f-112">**AGPM Server:** A server that runs the AGPM Service and manages an archive.</span></span> <span data-ttu-id="ab02f-113">Chaque serveur AGPM ne peut gérer qu’une seule archive, mais un serveur AGPM peut gérer les données d’archivage de plusieurs domaines dans une même archive.</span><span class="sxs-lookup"><span data-stu-id="ab02f-113">Each AGPM Server can manage only one archive, but one AGPM Server can manage archive data for multiple domains in one archive.</span></span> <span data-ttu-id="ab02f-114">Une archive peut être hébergée sur un ordinateur autre qu’un serveur AGPM.</span><span class="sxs-lookup"><span data-stu-id="ab02f-114">An archive can be hosted on a computer other than an AGPM Server.</span></span>

-   <span data-ttu-id="ab02f-115">**Service AGPM:** Composant logiciel d’AGPM qui s’exécute sur un serveur AGPM en tant que service.</span><span class="sxs-lookup"><span data-stu-id="ab02f-115">**AGPM Service:** The software component of AGPM that runs on an AGPM Server as a service.</span></span> <span data-ttu-id="ab02f-116">Le service gère les objets de stratégie de groupe dans l’archive et dans l’environnement de production de cette forêt.</span><span class="sxs-lookup"><span data-stu-id="ab02f-116">The service manages GPOs in the archive and in the production environment in that forest.</span></span>

-   <span data-ttu-id="ab02f-117">**Archive:** Dans AGPM, magasin central qui contient les objets de stratégie de groupe contrôlés gérés par le serveur AGPM associé, en plus de l’historique de chacun de ces objets.</span><span class="sxs-lookup"><span data-stu-id="ab02f-117">**Archive:** In AGPM, a central store that contains the controlled GPOs that the associated AGPM Server manages, in addition to the history for each of those GPOs.</span></span> <span data-ttu-id="ab02f-118">Cela inclut toutes les versions contrôlées précédentes de chaque GPO.</span><span class="sxs-lookup"><span data-stu-id="ab02f-118">This includes all previous controlled versions of each GPO.</span></span> <span data-ttu-id="ab02f-119">Une archive est composée d’un fichier d’index d’archive et de données d’archive associées qui peuvent inclure des données pour les objets de stratégie de groupe dans plusieurs domaines.</span><span class="sxs-lookup"><span data-stu-id="ab02f-119">An archive consists of an archive index file and associated archive data that may include data for GPOs in multiple domains.</span></span> <span data-ttu-id="ab02f-120">Une archive peut être hébergée sur un ordinateur autre qu’un serveur AGPM.</span><span class="sxs-lookup"><span data-stu-id="ab02f-120">An archive can be hosted on a computer other than an AGPM Server.</span></span>

-   <span data-ttu-id="ab02f-121">**GPO contrôlé:** Un objet de stratégie de groupe géré par AGPM.</span><span class="sxs-lookup"><span data-stu-id="ab02f-121">**Controlled GPO:** A GPO that is being managed by AGPM.</span></span> <span data-ttu-id="ab02f-122">AGPM gère l’historique et les autorisations des objets de stratégie de groupe contrôlés qu’il stocke dans l’archive.</span><span class="sxs-lookup"><span data-stu-id="ab02f-122">AGPM manages the history and permissions of controlled GPOs, which it stores in the archive.</span></span>

-   <span data-ttu-id="ab02f-123">**Objet de stratégie de groupe non contrôlé:** Un objet GPO dans l’environnement de production d’un domaine et n’est pas géré par AGPM.</span><span class="sxs-lookup"><span data-stu-id="ab02f-123">**Uncontrolled GPO:** A GPO in the production environment for a domain and not managed by AGPM.</span></span>

## <span data-ttu-id="ab02f-124">Quelles installations d’AGPM, création et incidences;</span><span class="sxs-lookup"><span data-stu-id="ab02f-124">What AGPM installs, creates, and affects</span></span>


<span data-ttu-id="ab02f-125">Sur un serveur AGPM, le programme d’installation d’AGPM installe le service AGPM.</span><span class="sxs-lookup"><span data-stu-id="ab02f-125">On an AGPM Server, the AGPM Setup program installs the AGPM Service.</span></span> <span data-ttu-id="ab02f-126">AGPM ne modifie pas le service Active Directory® Directory ou le schéma.</span><span class="sxs-lookup"><span data-stu-id="ab02f-126">AGPM does not alter the Active Directory® directory service or the schema.</span></span> <span data-ttu-id="ab02f-127">Par défaut, les fichiers du programme serveur AGPM sont installés dans%ProgramFiles%\\Microsoft\\AGPM\\Server.</span><span class="sxs-lookup"><span data-stu-id="ab02f-127">By default, the AGPM Server program files are installed in %ProgramFiles%\\Microsoft\\AGPM\\Server.</span></span> <span data-ttu-id="ab02f-128">Vous pouvez installer le service AGPM sur un contrôleur de domaine, si nécessaire. Toutefois, nous vous recommandons d’installer le service AGPM sur un serveur membre.</span><span class="sxs-lookup"><span data-stu-id="ab02f-128">You can install the AGPM Service on a domain controller if you have to; however, we recommend that you install the AGPM Service on a member server.</span></span>

<span data-ttu-id="ab02f-129">Sur un client AGPM, le programme d’installation d’AGPM installe le composant logiciel enfichable AGPM, puis ajoute un dossier de **contrôle de modification** à chaque domaine figurant dans la console GPMC.</span><span class="sxs-lookup"><span data-stu-id="ab02f-129">On an AGPM Client, the AGPM Setup program installs the AGPM snap-in, adding a **Change Control** folder to each domain that appears in the GPMC.</span></span> <span data-ttu-id="ab02f-130">Par défaut, les fichiers du programme client AGPM sont installés dans%ProgramFiles%\\Microsoft\\AGPM\\Client.</span><span class="sxs-lookup"><span data-stu-id="ab02f-130">By default, the AGPM Client program files are installed in %ProgramFiles%\\Microsoft\\AGPM\\Client.</span></span>

<span data-ttu-id="ab02f-131">Le tableau 1 décrit à la fois les éléments installés ou créés par AGPM et les composants du système d’exploitation qui affectent le fonctionnement d’AGPM.</span><span class="sxs-lookup"><span data-stu-id="ab02f-131">Table 1 describes both the items that AGPM installs or creates and the parts of the operating system that affect AGPM operation.</span></span>

**<span data-ttu-id="ab02f-132">Tableau 1: éléments installés, créés ou affectés par AGPM</span><span class="sxs-lookup"><span data-stu-id="ab02f-132">Table 1: Items installed, created, or affected by AGPM</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ab02f-133">Élément</span><span class="sxs-lookup"><span data-stu-id="ab02f-133">Item</span></span></th>
<th align="left"><span data-ttu-id="ab02f-134">Description</span><span class="sxs-lookup"><span data-stu-id="ab02f-134">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ab02f-135">Service AGPM</span><span class="sxs-lookup"><span data-stu-id="ab02f-135">AGPM Service</span></span></p></td>
<td align="left"><p><span data-ttu-id="ab02f-136">Le service AGPM s’exécute sur le serveur AGPM.</span><span class="sxs-lookup"><span data-stu-id="ab02f-136">The AGPM Service runs on the AGPM Server.</span></span> <span data-ttu-id="ab02f-137">Le service gère l’archive qui contient les objets de stratégie de groupe hors ligne et les objets de stratégie de groupe contrôlés dans l’environnement de production.</span><span class="sxs-lookup"><span data-stu-id="ab02f-137">The service manages the archive, which contains offline GPOs, and controlled GPOs in the production environment.</span></span> <span data-ttu-id="ab02f-138">La configuration par défaut du service AGPM est la suivante:</span><span class="sxs-lookup"><span data-stu-id="ab02f-138">The default configuration of the AGPM Service is as follows:</span></span></p>
<ul>
<li><p><strong><span data-ttu-id="ab02f-139">Nom du service: </strong> service AGPM</span><span class="sxs-lookup"><span data-stu-id="ab02f-139">Service name:</strong> AGPM Service</span></span></p></li>
<li><p><strong><span data-ttu-id="ab02f-140">Nom d’affichage: </strong> service AGPM</span><span class="sxs-lookup"><span data-stu-id="ab02f-140">Display name:</strong> AGPM Service</span></span></p></li>
<li><p><strong><span data-ttu-id="ab02f-141">Chemin d’accès au fichier exécutable: </strong> % ProgramFiles% \Microsoft\AGPM\Server\Agpm.exe</span><span class="sxs-lookup"><span data-stu-id="ab02f-141">Path to executable:</strong> %ProgramFiles%\Microsoft\AGPM\Server\Agpm.exe</span></span></p></li>
<li><p><strong><span data-ttu-id="ab02f-142">Démarrage: </strong> automatique</span><span class="sxs-lookup"><span data-stu-id="ab02f-142">Startup:</strong> Automatic</span></span></p></li>
<li><p><strong><span data-ttu-id="ab02f-143">Ouvrez une session en tant que: </strong> compte de service AGPM spécifié lors de l’installation d’AGPM Server, qui peut être modifié à l’aide <strong> de programmes et fonctionnalités </strong> dans le <strong> panneau de configuration </strong> .</span><span class="sxs-lookup"><span data-stu-id="ab02f-143">Log on as:</strong> AGPM Service Account specified during installation of AGPM Server, which can be changed using <strong>Programs and Features</strong> in the <strong>Control Panel</strong>.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ab02f-144">Archive AGPM</span><span class="sxs-lookup"><span data-stu-id="ab02f-144">AGPM archive</span></span></p></td>
<td align="left"><p><span data-ttu-id="ab02f-145">Par défaut, AGPM crée l’archive dans%ProgramData%\Microsoft\AGPM sur le serveur AGPM.</span><span class="sxs-lookup"><span data-stu-id="ab02f-145">By default, AGPM creates the archive in %ProgramData%\Microsoft\AGPM on the AGPM Server.</span></span> <span data-ttu-id="ab02f-146">L’archive fournit un espace de stockage pour les objets de stratégie de connexion hors connexion et peut stocker plusieurs versions de chaque GPO.</span><span class="sxs-lookup"><span data-stu-id="ab02f-146">The archive provides storage for offline GPOs, and it can store multiple versions of each GPO.</span></span> <span data-ttu-id="ab02f-147">Les modifications apportées par AGPM aux objets de stratégie de groupe dans l’archive n’affectent pas l’environnement de production tant qu’un administrateur ou approbateur AGPM a déployé l’objet de stratégie de groupe dans l’environnement de production et relie l’objet de stratégie de groupe à une unité d’organisation.</span><span class="sxs-lookup"><span data-stu-id="ab02f-147">Changes that AGPM makes to GPOs in the archive do not affect the production environment until an AGPM Administrator or Approver deploys the GPO to the production environment and links the GPO to an organizational unit (OU).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ab02f-148">Pare-feu Windows</span><span class="sxs-lookup"><span data-stu-id="ab02f-148">Windows Firewall</span></span></p></td>
<td align="left"><p><span data-ttu-id="ab02f-149">Lors de l’installation, AGPM autorise une règle de pare-feu Windows entrant qui permet au client AGPM de communiquer avec le serveur AGPM.</span><span class="sxs-lookup"><span data-stu-id="ab02f-149">During installation, AGPM enables an inbound Windows Firewall rule that allows the AGPM Client to communicate with the AGPM Server.</span></span> <span data-ttu-id="ab02f-150">La règle de pare-feu Windows par défaut est la suivante:</span><span class="sxs-lookup"><span data-stu-id="ab02f-150">The default Windows Firewall rule is the following:</span></span></p>
<ul>
<li><p><strong><span data-ttu-id="ab02f-151">Nom: </strong> service AGPM</span><span class="sxs-lookup"><span data-stu-id="ab02f-151">Name:</strong> AGPM Service</span></span></p></li>
<li><p><strong><span data-ttu-id="ab02f-152">Action: </strong> autoriser la connexion</span><span class="sxs-lookup"><span data-stu-id="ab02f-152">Action:</strong> Allow the connection</span></span></p></li>
<li><p><strong><span data-ttu-id="ab02f-153">Programmes: </strong> tous les programmes qui répondent aux conditions spécifiées.</span><span class="sxs-lookup"><span data-stu-id="ab02f-153">Programs:</strong> All programs that meet the specified conditions</span></span></p></li>
<li><p><strong><span data-ttu-id="ab02f-154">Type de protocole: </strong> TCP</span><span class="sxs-lookup"><span data-stu-id="ab02f-154">Protocol type:</strong> TCP</span></span></p></li>
<li><p><strong><span data-ttu-id="ab02f-155">Port local: </strong> 4600</span><span class="sxs-lookup"><span data-stu-id="ab02f-155">Local port:</strong> 4600</span></span></p></li>
<li><p><strong><span data-ttu-id="ab02f-156">Port distant: </strong> tous les ports</span><span class="sxs-lookup"><span data-stu-id="ab02f-156">Remote port:</strong> All ports</span></span></p></li>
<li><p><strong><span data-ttu-id="ab02f-157">Adresse IP locale: </strong> tout</span><span class="sxs-lookup"><span data-stu-id="ab02f-157">Local IP address:</strong> Any</span></span></p></li>
<li><p><strong><span data-ttu-id="ab02f-158">Adresse IP distante: </strong> tout</span><span class="sxs-lookup"><span data-stu-id="ab02f-158">Remote IP address:</strong> Any</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ab02f-159">Serveur de courrier</span><span class="sxs-lookup"><span data-stu-id="ab02f-159">E-mail server</span></span></p></td>
<td align="left"><p><span data-ttu-id="ab02f-160">AGPM utilise le protocole SMTP (Simple Mail Transfer Protocol) pour envoyer des demandes de courrier électronique aux adresses configurées dans l' <strong> onglet délégation de domaine </strong> . Par exemple, lorsqu’un éditeur demande la création d’un objet de stratégie de groupe, AGPM avertit chaque adresse de messagerie spécifiée sous l' <strong> onglet délégation de domaine </strong> .</span><span class="sxs-lookup"><span data-stu-id="ab02f-160">AGPM uses Simple Mail Transfer Protocol (SMTP) to send e-mail requests to the addresses configured on the <strong>Domain Delegation</strong> tab. For example, when an Editor requests that a new GPO be created, AGPM notifies each e-mail address specified on the <strong>Domain Delegation</strong> tab.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ab02f-161">Composant logiciel enfichable AGPM</span><span class="sxs-lookup"><span data-stu-id="ab02f-161">AGPM snap-in</span></span></p></td>
<td align="left"><p><span data-ttu-id="ab02f-162">Le composant logiciel enfichable AGPM pour la console GPMC s’exécute sur les clients AGPM et est utilisé par les administrateurs de stratégie de groupe pour gérer les objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="ab02f-162">The AGPM snap-in for the GPMC runs on AGPM Clients and is used by Group Policy administrators to manage GPOs.</span></span> <span data-ttu-id="ab02f-163">Le composant logiciel enfichable s’affiche dans la boîte de dialogue GPMC en tant que <strong> </strong> dossier de contrôle de modification dans chaque domaine.</span><span class="sxs-lookup"><span data-stu-id="ab02f-163">The snap-in appears in the GPMC as a <strong>Change Control</strong> folder in each domain.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="ab02f-164">Références supplémentaires</span><span class="sxs-lookup"><span data-stu-id="ab02f-164">Additional references</span></span>

<span data-ttu-id="ab02f-165">Pour plus d’informations sur les fichiers installés par AGPM, voir le [Guide de planification pour AGPM](https://go.microsoft.com/fwlink/?LinkId=160060).</span><span class="sxs-lookup"><span data-stu-id="ab02f-165">For more information about the files installed by AGPM, see the [Planning Guide for AGPM](https://go.microsoft.com/fwlink/?LinkId=160060).</span></span>

## <span data-ttu-id="ab02f-166">Archive</span><span class="sxs-lookup"><span data-stu-id="ab02f-166">Archive</span></span>


<span data-ttu-id="ab02f-167">Par défaut, le processus d’installation d’AGPM Server crée l’archive sur le disque dur local du serveur AGPM sur%ProgramData%\\Microsoft\\AGPM.</span><span class="sxs-lookup"><span data-stu-id="ab02f-167">By default, the AGPM Server installation process creates the archive on the local hard disk of the AGPM Server at %ProgramData%\\Microsoft\\AGPM.</span></span> <span data-ttu-id="ab02f-168">Toutefois, vous pouvez modifier la trajectoire au cours de l’installation et même créer l’archive sur un serveur autre que le serveur AGPM.</span><span class="sxs-lookup"><span data-stu-id="ab02f-168">However, you can change the path during installation and even create the archive on a server other than the AGPM Server.</span></span>

<span data-ttu-id="ab02f-169">L’archive contient un sous-dossier pour chaque version de chaque GPO contenu dans l’archive.</span><span class="sxs-lookup"><span data-stu-id="ab02f-169">The archive contains a subfolder for each version of each GPO the archive contains.</span></span> <span data-ttu-id="ab02f-170">Le nom de chaque sous-dossier est un GUID qui identifie une version de l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="ab02f-170">The name of each subfolder is a GUID that identifies a version of the GPO.</span></span>

<span data-ttu-id="ab02f-171">Le fichier gpostate.xml enregistre l’état de chaque GPO dans l’archive.</span><span class="sxs-lookup"><span data-stu-id="ab02f-171">The gpostate.xml file records the state of each GPO in the archive.</span></span> <span data-ttu-id="ab02f-172">Le fichier est un manifeste qui décrit le contenu de l’archive.</span><span class="sxs-lookup"><span data-stu-id="ab02f-172">The file is a manifest that describes the contents of the archive.</span></span> <span data-ttu-id="ab02f-173">Par exemple, un objet de stratégie de groupe peut avoir plusieurs versions et chaque version figure dans son propre sous-dossier dans l’archive.</span><span class="sxs-lookup"><span data-stu-id="ab02f-173">For example, a GPO can have many versions, and each version is in its own subfolder in the archive.</span></span> <span data-ttu-id="ab02f-174">Le fichier gpostate.xml indique quels sous-dossiers contiennent différentes versions d’un objet de stratégie de groupe unique.</span><span class="sxs-lookup"><span data-stu-id="ab02f-174">The gpostate.xml file indicates which subfolders contain different versions of a single GPO.</span></span> <span data-ttu-id="ab02f-175">De plus, les modèles d’objets de stratégie de groupe possèdent des sous-dossiers dans l’archive, mais gpostate.xml indiquent qu’il s’agit de modèles et non de GPO contrôlés.</span><span class="sxs-lookup"><span data-stu-id="ab02f-175">Additionally, GPO templates have subfolders in the archive, but gpostate.xml indicates that these are templates and not controlled GPOs.</span></span> <span data-ttu-id="ab02f-176">De la même manière, lorsque les administrateurs de stratégie de groupe suppriment des objets de stratégie de groupe, AGPM modifie leurs États dans gpostate.xml pour indiquer qu’ils se trouvent dans la **Corbeille** , mais ne supprime pas réellement les sous-dossiers de l’archive.</span><span class="sxs-lookup"><span data-stu-id="ab02f-176">Similarly, when Group Policy administrators delete GPOs, AGPM changes their states in gpostate.xml to indicate that they are in the **Recycle Bin** but does not actually remove the GPOs' subfolders from the archive.</span></span>

<span data-ttu-id="ab02f-177">**Attention**  Ne modifiez pas manuellement gpostate.xml ou les objets de stratégie de groupe qu’il contient.</span><span class="sxs-lookup"><span data-stu-id="ab02f-177">**Caution** Do not manually edit gpostate.xml or the GPOs the archive contains.</span></span> <span data-ttu-id="ab02f-178">Ces informations sont fournies uniquement pour améliorer la compréhension de l’archive AGPM.</span><span class="sxs-lookup"><span data-stu-id="ab02f-178">This information is provided only to enhance understanding of the AGPM archive.</span></span> <span data-ttu-id="ab02f-179">À la place, utilisez le composant logiciel enfichable AGPM pour modifier les objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="ab02f-179">Instead, use the AGPM snap-in to change GPOs.</span></span>

 

<span data-ttu-id="ab02f-180">Lorsque AGPM crée l’archive, il accorde le contrôle total au système, aux administrateurs et au compte de service AGPM (spécifié dans le programme d’installation d’AGPM Server).</span><span class="sxs-lookup"><span data-stu-id="ab02f-180">When AGPM creates the archive, it gives Full Control to SYSTEM, Administrators, and the AGPM Service Account (specified in the setup of AGPM Server).</span></span> <span data-ttu-id="ab02f-181">La modification des autorisations à l’aide de l’interface utilisateur d’AGPM sur le composant additionnel AGPM ne modifie pas les autorisations sur l’archive, car le compte de service AGPM effectue toutes les opérations au nom de l’utilisateur connecté.</span><span class="sxs-lookup"><span data-stu-id="ab02f-181">Changing permissions by using the AGPM user interface on the AGPM snap-in does not alter permissions on the archive, because the AGPM Service Account performs all operations on behalf of the logged-on user.</span></span>

### <span data-ttu-id="ab02f-182">Références supplémentaires</span><span class="sxs-lookup"><span data-stu-id="ab02f-182">Additional references</span></span>

<span data-ttu-id="ab02f-183">Pour plus d’informations sur la sauvegarde de l’archive, la restauration de celle-ci à partir d’une sauvegarde ou le déplacement du serveur et de l’archive AGPM, voir la section «exécuter les tâches d’administration AGPM» dans le [Guide des opérations pour AGPM](https://go.microsoft.com/fwlink/?LinkId=160061).</span><span class="sxs-lookup"><span data-stu-id="ab02f-183">For information about how to back up the archive, restore the archive from a backup, or move both the AGPM Server and the archive, see the "Performing AGPM Administrator Tasks" section in the [Operations Guide for AGPM](https://go.microsoft.com/fwlink/?LinkId=160061).</span></span>

## <span data-ttu-id="ab02f-184">Rôles et autorisations</span><span class="sxs-lookup"><span data-stu-id="ab02f-184">Roles and permissions</span></span>


<span data-ttu-id="ab02f-185">Les rôles simplifient la délégation.</span><span class="sxs-lookup"><span data-stu-id="ab02f-185">Roles simplify delegation.</span></span> <span data-ttu-id="ab02f-186">Au lieu d’affecter des autorisations détaillées aux administrateurs de stratégie de groupe, les administrateurs d’AGPM peuvent attribuer un des quatre rôles aux administrateurs de stratégie de groupe pour leur permettre d’effectuer le fonctionnement lié à ce rôle.</span><span class="sxs-lookup"><span data-stu-id="ab02f-186">Instead of assigning detailed permissions to Group Policy administrators, AGPM Administrators can assign one of four roles to Group Policy administrators to let them perform work related to that role:</span></span>

-   <span data-ttu-id="ab02f-187">**Administrateur AGPM:** Les administrateurs de stratégie de groupe disposant du rôle Administrateur AGPM (contrôle total) peuvent effectuer n’importe quelle tâche dans AGPM.</span><span class="sxs-lookup"><span data-stu-id="ab02f-187">**AGPM Administrator:** Group Policy administrators assigned the AGPM Administrator (Full Control) role can perform any task in AGPM.</span></span> <span data-ttu-id="ab02f-188">Les administrateurs d’AGPM peuvent configurer des options à l’échelle du domaine et des autorisations de délégué aux autres administrateurs de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="ab02f-188">AGPM Administrators can configure domain-wide options and delegate permissions to other Group Policy administrators.</span></span>

-   <span data-ttu-id="ab02f-189">**Approbateur:** Les administrateurs de stratégie de groupe auxquels le rôle Approbateur peut déployer des objets de stratégie de groupe dans l’environnement de production d’un domaine.</span><span class="sxs-lookup"><span data-stu-id="ab02f-189">**Approver:** Group Policy administrators assigned the Approver role can deploy GPOs to the production environment for a domain.</span></span> <span data-ttu-id="ab02f-190">Les approbateurs peuvent également créer et supprimer des objets de stratégie de groupe et approuver ou refuser des demandes d’éditeur.</span><span class="sxs-lookup"><span data-stu-id="ab02f-190">Approvers can also create and delete GPOs and approve or reject requests from Editors.</span></span> <span data-ttu-id="ab02f-191">Les approbateurs peuvent afficher la liste des objets de stratégie de groupe dans un domaine, afficher les paramètres de stratégie dans les objets de stratégie de groupe et créer et afficher des rapports sur les paramètres de stratégie d’un objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="ab02f-191">Approvers can view the list of GPOs in a domain, view the policy settings in GPOs, and create and view reports of the policy settings in a GPO.</span></span> <span data-ttu-id="ab02f-192">Ils ne peuvent pas modifier les paramètres de stratégie dans les objets de stratégie de groupe, sauf s’ils reçoivent également le rôle d’éditeur.</span><span class="sxs-lookup"><span data-stu-id="ab02f-192">They cannot edit the policy settings in GPOs unless they are also assigned the Editor role.</span></span>

-   <span data-ttu-id="ab02f-193">**Éditeur:** Les administrateurs de stratégie de groupe auxquels le rôle d’éditeur peut afficher la liste des objets de stratégie de groupe dans un domaine, afficher les paramètres de stratégie dans les objets de stratégie de groupe, modifier les paramètres de stratégie dans les objets de stratégie de groupe et créer et afficher des rapports sur les paramètres de stratégie d’un objet</span><span class="sxs-lookup"><span data-stu-id="ab02f-193">**Editor:** Group Policy administrators assigned the Editor role can view the list of GPOs in a domain, view the policy settings in GPOs, edit the policy settings in GPOs, and create and view reports of the policy settings in a GPO.</span></span> <span data-ttu-id="ab02f-194">Sauf si le rôle Approbateur lui est également affecté, les éditeurs ne peuvent pas créer, déployer ou supprimer des objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="ab02f-194">Unless they are also assigned the Approver role, Editors cannot create, deploy, or delete GPOs.</span></span> <span data-ttu-id="ab02f-195">Toutefois, ils peuvent demander la création, le déploiement et la suppression d’objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="ab02f-195">However, they can request that GPOs be created, deployed, or deleted.</span></span>

-   <span data-ttu-id="ab02f-196">**Relecteur:** Les administrateurs de stratégie de groupe qui ont attribué le rôle de réviseur peuvent afficher la liste des objets de stratégie de groupe dans un domaine et créer et afficher des rapports sur les paramètres de stratégie d’un objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="ab02f-196">**Reviewer:** Group Policy administrators assigned the Reviewer role can view the list of GPOs in a domain and create and view reports of the policy settings in a GPO.</span></span> <span data-ttu-id="ab02f-197">Sauf si un rôle d’éditeur lui est affecté, il ne peut pas modifier les paramètres de stratégie d’un objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="ab02f-197">Unless they are also assigned the Editor role, they cannot edit policy settings in a GPO.</span></span>

<span data-ttu-id="ab02f-198">AGPM fournit aux administrateurs d’AGPM la possibilité de configurer des autorisations pour un niveau plus détaillé que les rôles à l’aide du composant logiciel enfichable AGPM.</span><span class="sxs-lookup"><span data-stu-id="ab02f-198">AGPM gives AGPM Administrators the flexibility to configure permissions at a more detailed level than roles by using the AGPM snap-in.</span></span> <span data-ttu-id="ab02f-199">Le tableau 2 décrit ces autorisations et indique les autorisations accordées à chaque rôle par défaut.</span><span class="sxs-lookup"><span data-stu-id="ab02f-199">Table 2 describes these permissions and indicates the permissions granted to each role by default.</span></span>

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ab02f-200">Autorisation</span><span class="sxs-lookup"><span data-stu-id="ab02f-200">Permission</span></span></th>
<th align="left"><span data-ttu-id="ab02f-201">Description</span><span class="sxs-lookup"><span data-stu-id="ab02f-201">Description</span></span></th>
<th align="left"><span data-ttu-id="ab02f-202">Administrateur d’AGPM</span><span class="sxs-lookup"><span data-stu-id="ab02f-202">AGPM Administrator</span></span></th>
<th align="left"><span data-ttu-id="ab02f-203">Approbateur</span><span class="sxs-lookup"><span data-stu-id="ab02f-203">Approver</span></span></th>
<th align="left"><span data-ttu-id="ab02f-204">Dacteur</span><span class="sxs-lookup"><span data-stu-id="ab02f-204">Editor</span></span></th>
<th align="left"><span data-ttu-id="ab02f-205">Relecteur</span><span class="sxs-lookup"><span data-stu-id="ab02f-205">Reviewer</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="ab02f-206">Contrôle total</span><span class="sxs-lookup"><span data-stu-id="ab02f-206">Full Control</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="ab02f-207">Disposer de toutes les autorisations.</span><span class="sxs-lookup"><span data-stu-id="ab02f-207">Have all permissions.</span></span></p></td>
<td align="left"><p><span data-ttu-id="ab02f-208">Oui</span><span class="sxs-lookup"><span data-stu-id="ab02f-208">Yes</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="ab02f-209">Créer un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="ab02f-209">Create GPO</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="ab02f-210">Créer des objets de stratégie de groupe dans un domaine.</span><span class="sxs-lookup"><span data-stu-id="ab02f-210">Create GPOs in a domain.</span></span></p></td>
<td align="left"><p><span data-ttu-id="ab02f-211">Oui</span><span class="sxs-lookup"><span data-stu-id="ab02f-211">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="ab02f-212">Oui</span><span class="sxs-lookup"><span data-stu-id="ab02f-212">Yes</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="ab02f-213">Contenu de la liste</span><span class="sxs-lookup"><span data-stu-id="ab02f-213">List Contents</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="ab02f-214">Répertorier les objets de stratégie de groupe dans un domaine.</span><span class="sxs-lookup"><span data-stu-id="ab02f-214">List the GPOs in a domain.</span></span></p></td>
<td align="left"><p><span data-ttu-id="ab02f-215">Oui</span><span class="sxs-lookup"><span data-stu-id="ab02f-215">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="ab02f-216">Oui</span><span class="sxs-lookup"><span data-stu-id="ab02f-216">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="ab02f-217">Oui</span><span class="sxs-lookup"><span data-stu-id="ab02f-217">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="ab02f-218">Oui</span><span class="sxs-lookup"><span data-stu-id="ab02f-218">Yes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="ab02f-219">Lire les paramètres</span><span class="sxs-lookup"><span data-stu-id="ab02f-219">Read Settings</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="ab02f-220">Lire les paramètres de stratégie au sein d’un objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="ab02f-220">Read the policy settings within a GPO.</span></span></p></td>
<td align="left"><p><span data-ttu-id="ab02f-221">Oui</span><span class="sxs-lookup"><span data-stu-id="ab02f-221">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="ab02f-222">Oui</span><span class="sxs-lookup"><span data-stu-id="ab02f-222">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="ab02f-223">Oui</span><span class="sxs-lookup"><span data-stu-id="ab02f-223">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="ab02f-224">Oui</span><span class="sxs-lookup"><span data-stu-id="ab02f-224">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="ab02f-225">Modifier les paramètres</span><span class="sxs-lookup"><span data-stu-id="ab02f-225">Edit Settings</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="ab02f-226">Modifiez les paramètres de stratégie d’un objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="ab02f-226">Change the policy settings in a GPO.</span></span></p></td>
<td align="left"><p><span data-ttu-id="ab02f-227">Oui</span><span class="sxs-lookup"><span data-stu-id="ab02f-227">Yes</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="ab02f-228">Oui</span><span class="sxs-lookup"><span data-stu-id="ab02f-228">Yes</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="ab02f-229">Supprimer un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="ab02f-229">Delete GPO</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="ab02f-230">Supprimer un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="ab02f-230">Delete a GPO.</span></span></p></td>
<td align="left"><p><span data-ttu-id="ab02f-231">Oui</span><span class="sxs-lookup"><span data-stu-id="ab02f-231">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="ab02f-232">Oui</span><span class="sxs-lookup"><span data-stu-id="ab02f-232">Yes</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="ab02f-233">Modifier la sécurité</span><span class="sxs-lookup"><span data-stu-id="ab02f-233">Modify Security</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="ab02f-234">Déléguez l’accès au niveau du domaine, déléguez l’accès à un objet GPO unique et déléguez l’accès à l’environnement de production.</span><span class="sxs-lookup"><span data-stu-id="ab02f-234">Delegate domain-level access, delegate access to a single GPO, and delegate access to the production environment.</span></span></p></td>
<td align="left"><p><span data-ttu-id="ab02f-235">Oui</span><span class="sxs-lookup"><span data-stu-id="ab02f-235">Yes</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="ab02f-236">Déploiement d’objets de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="ab02f-236">Deploy GPO</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="ab02f-237">Déploiement d’un objet de stratégie de groupe à partir de l’archive dans l’environnement de production.</span><span class="sxs-lookup"><span data-stu-id="ab02f-237">Deploy a GPO from the archive to the production environment.</span></span></p></td>
<td align="left"><p><span data-ttu-id="ab02f-238">Oui</span><span class="sxs-lookup"><span data-stu-id="ab02f-238">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="ab02f-239">Oui</span><span class="sxs-lookup"><span data-stu-id="ab02f-239">Yes</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="ab02f-240">Créer un modèle</span><span class="sxs-lookup"><span data-stu-id="ab02f-240">Create Template</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="ab02f-241">Créer un modèle d’objet de stratégie de groupe dans AGPM.</span><span class="sxs-lookup"><span data-stu-id="ab02f-241">Create a GPO template in AGPM.</span></span></p></td>
<td align="left"><p><span data-ttu-id="ab02f-242">Oui</span><span class="sxs-lookup"><span data-stu-id="ab02f-242">Yes</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="ab02f-243">Oui</span><span class="sxs-lookup"><span data-stu-id="ab02f-243">Yes</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="ab02f-244">Modification des options</span><span class="sxs-lookup"><span data-stu-id="ab02f-244">Modify Options</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="ab02f-245">Configurer les notifications par courrier électronique AGPM et limiter les versions d’objets de stratégie de groupe stockées dans l’archive.</span><span class="sxs-lookup"><span data-stu-id="ab02f-245">Configure AGPM e-mail notification and limit the GPO versions stored in the archive.</span></span></p></td>
<td align="left"><p><span data-ttu-id="ab02f-246">Oui</span><span class="sxs-lookup"><span data-stu-id="ab02f-246">Yes</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="ab02f-247">Exporter un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="ab02f-247">Export GPO</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="ab02f-248">Exporter un objet de stratégie de groupe dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="ab02f-248">Export a GPO to a file.</span></span></p></td>
<td align="left"><p><span data-ttu-id="ab02f-249">Oui</span><span class="sxs-lookup"><span data-stu-id="ab02f-249">Yes</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="ab02f-250">Oui</span><span class="sxs-lookup"><span data-stu-id="ab02f-250">Yes</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="ab02f-251">Importer un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="ab02f-251">Import GPO</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="ab02f-252">Importer un objet de stratégie de groupe à partir d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="ab02f-252">Import a GPO from a file.</span></span></p></td>
<td align="left"><p><span data-ttu-id="ab02f-253">Oui</span><span class="sxs-lookup"><span data-stu-id="ab02f-253">Yes</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="ab02f-254">Oui</span><span class="sxs-lookup"><span data-stu-id="ab02f-254">Yes</span></span></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="ab02f-255">**Remarques** 
 Les autorisations d' **exportation** d’objets de stratégie de groupe et d' **importation** ne sont pas disponibles dans AGPM 3,0 ou 2,5.</span><span class="sxs-lookup"><span data-stu-id="ab02f-255">**Note**
**Export GPO** and **Import GPO** permissions are not available in AGPM 3.0 or 2.5.</span></span>

<span data-ttu-id="ab02f-256">La possibilité de déléguer l’accès à des objets de stratégie de groupe dans l’environnement de production d’un domaine et la possibilité de limiter le nombre de versions d’objets de stratégie de groupe stockées ne sont pas disponibles dans AGPM 2,5.</span><span class="sxs-lookup"><span data-stu-id="ab02f-256">The ability to delegate access to GPOs in the production environment for a domain and the ability to limit the number of GPO versions stored are not available in AGPM 2.5.</span></span>

 

### <span data-ttu-id="ab02f-257">Références supplémentaires</span><span class="sxs-lookup"><span data-stu-id="ab02f-257">Additional references</span></span>

<span data-ttu-id="ab02f-258">Pour plus d’informations sur les tâches qui peuvent être effectuées par les administrateurs de stratégie de groupe ayant attribué un rôle particulier ou concernant les autorisations nécessaires à l’exécution d’une tâche spécifique, voir le [Guide des opérations pour AGPM](https://go.microsoft.com/fwlink/?LinkId=160061).</span><span class="sxs-lookup"><span data-stu-id="ab02f-258">For information about what tasks can be performed by Group Policy administrators assigned a particular role or about which permissions are required to perform a specific task, see the [Operations Guide for AGPM](https://go.microsoft.com/fwlink/?LinkId=160061).</span></span>

 

 





