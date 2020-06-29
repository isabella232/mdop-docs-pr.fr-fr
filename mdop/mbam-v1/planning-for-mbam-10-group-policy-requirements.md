---
title: Planification des exigences en matière de stratégie de groupe MBAM1.0
description: Planification des exigences en matière de stratégie de groupe MBAM1.0
author: dansimp
ms.assetid: 0fc9c509-7850-4a8e-bb82-b949025bcb02
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f5061748107dc1d00baa41188b8cf240ec187317
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804225"
---
# <span data-ttu-id="dabad-103">Planification des exigences en matière de stratégie de groupe MBAM1.0</span><span class="sxs-lookup"><span data-stu-id="dabad-103">Planning for MBAM 1.0 Group Policy Requirements</span></span>


<span data-ttu-id="dabad-104">La gestion du client Microsoft BitLocker administration et surveillance (MBAM) nécessite l’application de paramètres de stratégie de groupe personnalisés.</span><span class="sxs-lookup"><span data-stu-id="dabad-104">Microsoft BitLocker Administration and Monitoring (MBAM) Client management requires custom Group Policy settings to be applied.</span></span> <span data-ttu-id="dabad-105">Cette rubrique décrit les options de stratégie disponibles pour l’objet de stratégie de groupe (GPO) lorsque vous utilisez MBAM pour gérer le chiffrement de lecteur BitLocker au sein de l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="dabad-105">This topic describes the available policy options for Group Policy Object (GPO) when you use MBAM to manage BitLocker Drive Encryption in the enterprise.</span></span>

**<span data-ttu-id="dabad-106">Important</span><span class="sxs-lookup"><span data-stu-id="dabad-106">Important</span></span>**  
<span data-ttu-id="dabad-107">MBAM n’utilise pas les paramètres d’objet GPO par défaut pour le chiffrement de lecteur BitLocker Windows.</span><span class="sxs-lookup"><span data-stu-id="dabad-107">MBAM does not use the default GPO settings for Windows BitLocker drive encryption.</span></span> <span data-ttu-id="dabad-108">Si les paramètres par défaut sont activés, ils peuvent entraîner un comportement en conflit.</span><span class="sxs-lookup"><span data-stu-id="dabad-108">If the default settings are enabled, they can cause conflicting behavior.</span></span> <span data-ttu-id="dabad-109">Pour permettre à MBAM de gérer BitLocker, vous devez définir les paramètres de stratégie d’objet de stratégie de groupe après avoir installé le modèle de stratégie de groupe MBAM.</span><span class="sxs-lookup"><span data-stu-id="dabad-109">To enable MBAM to manage BitLocker, you must define the GPO policy settings after you install the MBAM Group Policy Template.</span></span>



<span data-ttu-id="dabad-110">Après avoir installé le modèle de stratégie de groupe MBAM, vous pouvez afficher et modifier les paramètres de stratégie d’objets de stratégie de groupe MBAM personnalisés disponibles qui permettent à MBAM de gérer le chiffrement de l’entreprise BitLocker.</span><span class="sxs-lookup"><span data-stu-id="dabad-110">After you install the MBAM Group Policy template, you can view and modify the available custom MBAM GPO policy settings that enable MBAM to manage the enterprise BitLocker encryption.</span></span> <span data-ttu-id="dabad-111">Le modèle de stratégie de groupe MBAM doit être installé sur un ordinateur capable d’exécuter la console de gestion des stratégies de groupe (GPMC) ou la technologie de gestion des stratégies de groupe avancée (AGPM).</span><span class="sxs-lookup"><span data-stu-id="dabad-111">The MBAM Group Policy template must be installed on a computer that is capable of running the Group Policy Management Console (GPMC) or the Advanced Group Policy Management (AGPM) MDOP technology.</span></span> <span data-ttu-id="dabad-112">Pour modifier l’objet de stratégie de groupe applicable, ouvrez le GPMC ou AGPM, puis naviguez jusqu’au nœud d’objet de stratégie de groupe suivant: **Configuration ordinateur** \\ **modèles d’administration** \\ **composants Windows**- \\ **MDOP MBAM (gestion de BitLocker)**.</span><span class="sxs-lookup"><span data-stu-id="dabad-112">Next, to edit the applicable GPO, open the GPMC or AGPM, and then navigate to the following GPO node: **Computer Configuration**\\**Administrative Templates**\\**Windows Components**\\**MDOP MBAM (BitLocker Management)**.</span></span>

<span data-ttu-id="dabad-113">Le nœud de l’objet de stratégie de groupe MDOP MBAM (gestion de BitLocker) contient quatre paramètres de stratégie globale et quatre nœuds de paramètres d’objet de stratégie de groupe enfants, respectivement.</span><span class="sxs-lookup"><span data-stu-id="dabad-113">The MDOP MBAM (BitLocker Management) GPO node contains four global policy settings and four child GPO setting nodes, respectively.</span></span> <span data-ttu-id="dabad-114">Les quatre paramètres de stratégie globale de l’objet de stratégie de groupe sont: gestion du client, lecteur fixe, lecteur du système d’exploitation et lecteur amovible.</span><span class="sxs-lookup"><span data-stu-id="dabad-114">The four GPO global policy settings are: Client Management, Fixed Drive, Operating System Drive, and Removable Drive.</span></span> <span data-ttu-id="dabad-115">Les sections suivantes fournissent des définitions de stratégie et des paramètres de stratégie suggérés pour vous aider à planifier les exigences des paramètres de stratégie d’objet de stratégie de MBAM.</span><span class="sxs-lookup"><span data-stu-id="dabad-115">The following sections provide policy definitions and suggested policy settings to help you plan for the MBAM GPO policy setting requirements.</span></span>

**<span data-ttu-id="dabad-116">Remarque</span><span class="sxs-lookup"><span data-stu-id="dabad-116">Note</span></span>**  
<span data-ttu-id="dabad-117">Pour plus d’informations sur la configuration des paramètres d’objet de stratégie de groupe suggérés au minimum pour permettre à MBAM de gérer le chiffrement BitLocker, voir [Comment modifier les paramètres de l’objet de stratégie de groupe MBAM 1,0](how-to-edit-mbam-10-gpo-settings.md).</span><span class="sxs-lookup"><span data-stu-id="dabad-117">For more information about configuring the minimum suggested GPO settings to enable MBAM to manage BitLocker encryption, see [How to Edit MBAM 1.0 GPO Settings](how-to-edit-mbam-10-gpo-settings.md).</span></span>



## <span data-ttu-id="dabad-118">Définitions de stratégies globales</span><span class="sxs-lookup"><span data-stu-id="dabad-118">Global policy definitions</span></span>


<span data-ttu-id="dabad-119">Cette section décrit les définitions de stratégies globales de MBAM, qui se trouvent dans le nœud d’objet GPO suivant: **Configuration ordinateur** \\ **modèles d’administration** \\ **composants Windows** \\ **MDOP MBAM (gestion de BitLocker)**.</span><span class="sxs-lookup"><span data-stu-id="dabad-119">This section describes the MBAM Global policy definitions, which can be found at the following GPO node: **Computer Configuration**\\**Administrative Templates**\\**Windows Components**\\**MDOP MBAM (BitLocker Management)**.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="dabad-120">Nom de la stratégie</span><span class="sxs-lookup"><span data-stu-id="dabad-120">Policy Name</span></span></th>
<th align="left"><span data-ttu-id="dabad-121">Vue d’ensemble et paramètre de stratégie suggéré</span><span class="sxs-lookup"><span data-stu-id="dabad-121">Overview and Suggested Policy Setting</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="dabad-122">Choisir la méthode de chiffrement de lecteur et la puissance de chiffrement</span><span class="sxs-lookup"><span data-stu-id="dabad-122">Choose drive encryption method and cipher strength</span></span></p></td>
<td align="left"><p><span data-ttu-id="dabad-123">Configuration suggérée: <strong> non configuré</span><span class="sxs-lookup"><span data-stu-id="dabad-123">Suggested Configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="dabad-124">Configurez cette stratégie pour utiliser une méthode de chiffrement et une force de chiffrement spécifiques.</span><span class="sxs-lookup"><span data-stu-id="dabad-124">Configure this policy to use a specific encryption method and cipher strength.</span></span></p>
<p><span data-ttu-id="dabad-125">Lorsque cette stratégie n’est pas configurée, BitLocker utilise la méthode de chiffrement par défaut de AES 128-bit avec diffuseur ou la méthode de chiffrement spécifiée par le script de configuration.</span><span class="sxs-lookup"><span data-stu-id="dabad-125">When this policy is not configured, BitLocker uses the default encryption method of AES 128-bit with Diffuser or the encryption method specified by the setup script.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="dabad-126">Empêcher le remplacement de mémoire lors du redémarrage</span><span class="sxs-lookup"><span data-stu-id="dabad-126">Prevent memory overwrite on restart</span></span></p></td>
<td align="left"><p><span data-ttu-id="dabad-127">Configuration suggérée: <strong> non configuré</span><span class="sxs-lookup"><span data-stu-id="dabad-127">Suggested Configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="dabad-128">Configurez cette stratégie pour améliorer les performances de redémarrage sans remplacer les secrets de BitLocker en mémoire lors du redémarrage.</span><span class="sxs-lookup"><span data-stu-id="dabad-128">Configure this policy to improve restart performance without overwriting BitLocker secrets in memory on restart.</span></span></p>
<p><span data-ttu-id="dabad-129">Lorsque cette stratégie n’est pas configurée, les secrets BitLocker sont supprimés de la mémoire lors du redémarrage de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="dabad-129">When this policy is not configured, BitLocker secrets are removed from memory when the computer restarts.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="dabad-130">Valider la règle d’utilisation des certificats de carte à puce</span><span class="sxs-lookup"><span data-stu-id="dabad-130">Validate smart card certificate usage rule</span></span></p></td>
<td align="left"><p><span data-ttu-id="dabad-131">Configuration suggérée: <strong> non configuré</span><span class="sxs-lookup"><span data-stu-id="dabad-131">Suggested Configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="dabad-132">Configurez cette stratégie pour utiliser la protection BitLocker basée sur un certificat SmartCard.</span><span class="sxs-lookup"><span data-stu-id="dabad-132">Configure this policy to use smartcard certificate-based BitLocker protection.</span></span></p>
<p><span data-ttu-id="dabad-133">Lorsque cette stratégie n’est pas configurée, un identificateur d’objet par défaut 1.3.6.1.4.1.311.67.1.1 est utilisé pour spécifier un certificat.</span><span class="sxs-lookup"><span data-stu-id="dabad-133">When this policy is not configured, a default object identifier 1.3.6.1.4.1.311.67.1.1 is used to specify a certificate.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="dabad-134">Fournir les identificateurs uniques pour votre organisation</span><span class="sxs-lookup"><span data-stu-id="dabad-134">Provide the unique identifiers for your organization</span></span></p></td>
<td align="left"><p><span data-ttu-id="dabad-135">Configuration suggérée: <strong> non configuré</span><span class="sxs-lookup"><span data-stu-id="dabad-135">Suggested Configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="dabad-136">Configurez cette stratégie pour utiliser un agent de récupération des données basé sur un certificat ou le lecteur BitLocker to go.</span><span class="sxs-lookup"><span data-stu-id="dabad-136">Configure this policy to use a certificate-based data recovery agent or the BitLocker To Go reader.</span></span></p>
<p><span data-ttu-id="dabad-137">Lorsque cette stratégie n’est pas configurée, le <strong> champ d’identification </strong> n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="dabad-137">When this policy is not configured, the <strong>Identification</strong> field is not used.</span></span></p>
<p><span data-ttu-id="dabad-138">Si votre entreprise utilise des mesures de sécurité plus importantes, vous pouvez configurer <strong> le </strong> champ d’identification pour vous assurer que tous les périphériques USB disposent de ce jeu de champs et qu’ils sont alignés avec ce paramètre de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="dabad-138">If your company requires higher security measurements, you may want to configure the <strong>Identification</strong> field to make sure that all USB devices have this field set and that they are aligned with this Group Policy setting.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="dabad-139">Définitions de la stratégie de gestion du client</span><span class="sxs-lookup"><span data-stu-id="dabad-139">Client Management policy definitions</span></span>


<span data-ttu-id="dabad-140">Cette section décrit les définitions de la stratégie de gestion des clients pour MBAM, qui se trouvent sur le nœud d’objet GPO suivant: **Configuration ordinateur** \\ **modèles d’administration** \\ **composants Windows** \\ **MDOP MBAM (gestion de BitLocker)**  \\  **Client Management**.</span><span class="sxs-lookup"><span data-stu-id="dabad-140">This section describes the Client Management policy definitions for MBAM, found at the following GPO node: **Computer Configuration**\\**Administrative Templates**\\**Windows Components**\\**MDOP MBAM (BitLocker Management)** \\ **Client Management**.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="dabad-141">Nom de la stratégie</span><span class="sxs-lookup"><span data-stu-id="dabad-141">Policy Name</span></span></th>
<th align="left"><span data-ttu-id="dabad-142">Vue d’ensemble et paramètres de stratégie suggérés</span><span class="sxs-lookup"><span data-stu-id="dabad-142">Overview and Suggested Policy Settings</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="dabad-143">Configurer les services de MBAM</span><span class="sxs-lookup"><span data-stu-id="dabad-143">Configure MBAM Services</span></span></p></td>
<td align="left"><p><span data-ttu-id="dabad-144">Configuration suggérée: <strong> activée</span><span class="sxs-lookup"><span data-stu-id="dabad-144">Suggested Configuration: <strong>Enabled</span></span></strong></p>
<ul>
<li><p><strong><span data-ttu-id="dabad-145">Point de terminaison du service matériel et de récupération MBAM </strong> .</span><span class="sxs-lookup"><span data-stu-id="dabad-145">MBAM Recovery and Hardware service endpoint</strong>.</span></span> <span data-ttu-id="dabad-146">Il s’agit du premier paramètre de stratégie que vous devez configurer pour activer la gestion du chiffrement BitLocker du client MBAM.</span><span class="sxs-lookup"><span data-stu-id="dabad-146">This is the first policy setting that you must configure to enable the MBAM Client BitLocker encryption management.</span></span> <span data-ttu-id="dabad-147">Pour ce paramètre, entrez l’emplacement du point de terminaison de la même façon que l’exemple suivant: <strong> http:// </strong><em> &lt; MBAM administration et surveillance &gt; </em><strong> du nom du serveur: </strong><em> &lt; Portage le service Web est lié à &gt; </em><strong> /MBAMRecoveryAndHardwareService/CoreService.svc </strong> .</span><span class="sxs-lookup"><span data-stu-id="dabad-147">For this setting, enter the endpoint location similar to the following example: <strong>http://</strong><em>&lt;MBAM Administration and Monitoring Server Name&gt;</em><strong>:</strong><em>&lt;port the web service is bound to&gt;</em><strong>/MBAMRecoveryAndHardwareService/CoreService.svc</strong>.</span></span></p></li>
<li><p><strong><span data-ttu-id="dabad-148">Sélectionnez les informations de récupération BitLocker à stocker </strong> .</span><span class="sxs-lookup"><span data-stu-id="dabad-148">Select BitLocker recovery information to store</strong>.</span></span> <span data-ttu-id="dabad-149">Ce paramètre de stratégie vous permet de configurer le service de récupération de clés pour sauvegarder les informations de récupération de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="dabad-149">This policy setting lets you configure the key recovery service to back up the BitLocker recovery information.</span></span> <span data-ttu-id="dabad-150">Il vous permet également de configurer le service de rapport d’État pour la collecte des rapports de conformité et d’audit.</span><span class="sxs-lookup"><span data-stu-id="dabad-150">It also lets you configure the status reporting service for collecting compliance and audit reports.</span></span> <span data-ttu-id="dabad-151">La stratégie fournit une méthode d’administration permettant de récupérer les données chiffrées par BitLocker afin d’éviter la perte de données en raison de l’absence d’informations clés.</span><span class="sxs-lookup"><span data-stu-id="dabad-151">The policy provides an administrative method of recovering data encrypted by BitLocker to help prevent data loss due to the lack of key information.</span></span> <span data-ttu-id="dabad-152">Le rapport d’État et l’activité de récupération de clés seront automatiquement et en silence vers l’emplacement du serveur du rapport configuré.</span><span class="sxs-lookup"><span data-stu-id="dabad-152">Status report and key recovery activity will automatically and silently be sent to the configured report server location.</span></span></p>
<p><span data-ttu-id="dabad-153">Si vous ne configurez pas ou si vous désactivez ce paramètre de stratégie, les informations de récupération de clé ne seront pas enregistrées, et le rapport d’État et les activités de récupération de clés ne seront pas signalés au serveur.</span><span class="sxs-lookup"><span data-stu-id="dabad-153">If you do not configure or if you disable this policy setting, the key recovery information will not be saved, and status report and key recovery activity will not be reported to server.</span></span> <span data-ttu-id="dabad-154">Lorsque ce paramètre est défini sur <strong> mot de passe de récupération et sur le package de clé </strong> , le mot de passe de récupération et le package de clé seront automatiquement sauvegardés sur l’emplacement du serveur de récupération de clé configuré.</span><span class="sxs-lookup"><span data-stu-id="dabad-154">When this setting is set to <strong>Recovery Password and key package</strong>, the recovery password and key package will be automatically and silently backed up to the configured key recovery server location.</span></span></p></li>
<li><p><strong><span data-ttu-id="dabad-155">Entrez la fréquence de vérification de l’état du client en minutes </strong> .</span><span class="sxs-lookup"><span data-stu-id="dabad-155">Enter the client checking status frequency in minutes</strong>.</span></span> <span data-ttu-id="dabad-156">Ce paramètre de stratégie gère la fréquence à laquelle le client vérifie les stratégies de protection BitLocker et l’état de l’ordinateur client.</span><span class="sxs-lookup"><span data-stu-id="dabad-156">This policy setting manages how frequently the client checks the BitLocker protection policies and the status on the client computer.</span></span> <span data-ttu-id="dabad-157">Ce paramètre gère également la fréquence d’enregistrement de l’état de conformité du client sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="dabad-157">This policy also manages how frequently the client compliance status is saved to the server.</span></span> <span data-ttu-id="dabad-158">Le client vérifie les stratégies de protection de BitLocker et l’État sur l’ordinateur client et il sauvegarde également la clé de récupération du client à la fréquence configurée.</span><span class="sxs-lookup"><span data-stu-id="dabad-158">The client checks the BitLocker protection policies and status on the client computer, and it also backs up the client recovery key at the configured frequency.</span></span></p>
<p><span data-ttu-id="dabad-159">Définissez cette fréquence en fonction de la configuration requise établie par votre entreprise sur la fréquence de vérification de l’état de conformité de l’ordinateur et la fréquence de sauvegarde de la clé de récupération du client.</span><span class="sxs-lookup"><span data-stu-id="dabad-159">Set this frequency based on the requirement established by your company on how frequently to check the compliance status of the computer, and how frequently to back up the client recovery key.</span></span></p></li>
<li><p><strong><span data-ttu-id="dabad-160">Point de terminaison du service de rapport d’État MBAM </strong> .</span><span class="sxs-lookup"><span data-stu-id="dabad-160">MBAM Status reporting service endpoint</strong>.</span></span> <span data-ttu-id="dabad-161">Il s’agit du deuxième paramètre de stratégie que vous devez configurer pour activer la gestion du chiffrement BitLocker du client MBAM.</span><span class="sxs-lookup"><span data-stu-id="dabad-161">This is the second policy setting that you must configure to enable MBAM Client BitLocker encryption management.</span></span> <span data-ttu-id="dabad-162">Pour ce paramètre, entrez l’emplacement du point de terminaison en utilisant l’exemple suivant: <strong> http:// </strong><em> &lt; MBAM administration et surveillance &gt; </em><strong> du nom du serveur: </strong><em> &lt; Portage le service Web est lié à &gt; </em><strong> /MBAMComplianceStatusService/StatusReportingService.</span><span class="sxs-lookup"><span data-stu-id="dabad-162">For this setting, enter the endpoint location by using the following example: <strong>http://</strong><em>&lt;MBAM Administration and Monitoring Server Name&gt;</em><strong>:</strong><em>&lt;port the web service is bound to&gt;</em><strong>/MBAMComplianceStatusService/StatusReportingService.</span></span> <span data-ttu-id="dabad-163">SVC </strong> .</span><span class="sxs-lookup"><span data-stu-id="dabad-163">svc</strong>.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="dabad-164">Autoriser la vérification de compatibilité matérielle</span><span class="sxs-lookup"><span data-stu-id="dabad-164">Allow hardware compatibility checking</span></span></p></td>
<td align="left"><p><span data-ttu-id="dabad-165">Configuration suggérée: <strong> activée</span><span class="sxs-lookup"><span data-stu-id="dabad-165">Suggested Configuration: <strong>Enabled</span></span></strong></p>
<p><span data-ttu-id="dabad-166">Ce paramètre de stratégie vous permet de gérer la vérification de la compatibilité matérielle avant d’activer la protection de BitLocker sur des lecteurs d’ordinateurs clients MBAM.</span><span class="sxs-lookup"><span data-stu-id="dabad-166">This policy setting lets you manage the verification of hardware compatibility before you enable BitLocker protection on drives of MBAM client computers.</span></span></p>
<p><span data-ttu-id="dabad-167">Vous devez activer cette option de stratégie si votre entreprise dispose d’anciens matériels ou d’ordinateurs qui ne prennent pas en charge le module de plateforme sécurisée (TPM).</span><span class="sxs-lookup"><span data-stu-id="dabad-167">You should enable this policy option if your enterprise has older computer hardware or computers that do not support Trusted Platform Module (TPM).</span></span> <span data-ttu-id="dabad-168">Si l’un de ces critères est vrai, activez la vérification de compatibilité matérielle pour vous assurer que MBAM est appliqué uniquement aux modèles d’ordinateurs qui prennent en charge BitLocker.</span><span class="sxs-lookup"><span data-stu-id="dabad-168">If either of these criteria is true, enable the hardware compatibility verification to make sure that MBAM is applied only to computer models that support BitLocker.</span></span> <span data-ttu-id="dabad-169">Si tous les ordinateurs de votre organisation prennent en charge BitLocker, vous n’avez pas à déployer la compatibilité matérielle et vous pouvez définir cette stratégie sur <strong> non configuré </strong> .</span><span class="sxs-lookup"><span data-stu-id="dabad-169">If all computers in your organization support BitLocker, you do not have to deploy the Hardware Compatibility, and you can set this policy to <strong>Not Configured</strong>.</span></span></p>
<p><span data-ttu-id="dabad-170">Si vous activez ce paramètre de stratégie, le modèle de l’ordinateur est validé par rapport à la liste de compatibilité matérielle une fois toutes les 24 heures, avant que la stratégie ne soit activée pour la protection BitLocker sur un lecteur d’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="dabad-170">If you enable this policy setting, the model of the computer is validated against the hardware compatibility list once every 24 hours, before the policy enables BitLocker protection on a computer drive.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="dabad-171">Remarque</span><span class="sxs-lookup"><span data-stu-id="dabad-171">Note</span></span></strong><br/><p><span data-ttu-id="dabad-172">Avant d’activer ce paramètre de stratégie, assurez-vous d’avoir configuré le <strong> paramètre de point de terminaison de récupération et de service matériel MBAM </strong> dans les <strong> options configurer la stratégie des services MBAM </strong> .</span><span class="sxs-lookup"><span data-stu-id="dabad-172">Before enabling this policy setting, make sure that you have configured the <strong>MBAM Recovery and Hardware service endpoint</strong> setting in the <strong>Configure MBAM Services</strong> policy options.</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="dabad-173">Si vous désactivez ou ne configurez pas ce paramètre de stratégie, le modèle ordinateur n’est pas validé par rapport à la liste de compatibilité matérielle.</span><span class="sxs-lookup"><span data-stu-id="dabad-173">If you either disable or do not configure this policy setting, the computer model is not validated against the hardware compatibility list.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="dabad-174">Configurer une stratégie d’exemption des utilisateurs</span><span class="sxs-lookup"><span data-stu-id="dabad-174">Configure user exemption policy</span></span></p></td>
<td align="left"><p><span data-ttu-id="dabad-175">Configuration suggérée: <strong> non configuré</span><span class="sxs-lookup"><span data-stu-id="dabad-175">Suggested Configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="dabad-176">Ce paramètre de stratégie vous permet de configurer une adresse de site Web, une adresse de messagerie ou un numéro de téléphone qui demande à l’utilisateur d’être exempté du chiffrement BitLocker.</span><span class="sxs-lookup"><span data-stu-id="dabad-176">This policy setting lets you configure a web site address, email address, or phone number that will instruct a user to request an exemption from BitLocker encryption.</span></span></p>
<p><span data-ttu-id="dabad-177">Si vous activez ce paramètre de stratégie et indiquez une adresse de site Web, une adresse de messagerie ou un numéro de téléphone, les utilisateurs verront une boîte de dialogue contenant des instructions sur la façon d’appliquer une exemption de protection BitLocker.</span><span class="sxs-lookup"><span data-stu-id="dabad-177">If you enable this policy setting and provide a web site address, email address, or phone number, users will see a dialog with instructions on how to apply for an exemption from BitLocker protection.</span></span> <span data-ttu-id="dabad-178">Pour plus d’informations sur l’activation des exemptions de chiffrement BitLocker pour les utilisateurs, voir <a href="how-to-manage-user-bitlocker-encryption-exemptions-mbam-1.md" data-raw-source="[How to Manage User BitLocker Encryption Exemptions](how-to-manage-user-bitlocker-encryption-exemptions-mbam-1.md)"> Comment gérer les exemptions de chiffrement BitLocker de l’utilisateur </a> .</span><span class="sxs-lookup"><span data-stu-id="dabad-178">For more information about how to enable BitLocker encryption exemptions for users, see <a href="how-to-manage-user-bitlocker-encryption-exemptions-mbam-1.md" data-raw-source="[How to Manage User BitLocker Encryption Exemptions](how-to-manage-user-bitlocker-encryption-exemptions-mbam-1.md)">How to Manage User BitLocker Encryption Exemptions</a>.</span></span></p>
<p><span data-ttu-id="dabad-179">Si vous désactivez ou ne configurez pas ce paramètre de stratégie, les instructions relatives à l’application d’une demande d’exemption ne seront pas présentées aux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="dabad-179">If you either disable or do not configure this policy setting, the instructions about how to apply for an exemption request will not be presented to users.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="dabad-180">Remarque</span><span class="sxs-lookup"><span data-stu-id="dabad-180">Note</span></span></strong><br/><p><span data-ttu-id="dabad-181">L’exemption des utilisateurs est gérée par utilisateur et non par ordinateur.</span><span class="sxs-lookup"><span data-stu-id="dabad-181">User exemption is managed per user, not per computer.</span></span> <span data-ttu-id="dabad-182">Si plusieurs utilisateurs se connectent sur le même ordinateur et qu’un utilisateur n’est pas exempté, l’ordinateur est crypté.</span><span class="sxs-lookup"><span data-stu-id="dabad-182">If multiple users log on to the same computer and one user is not exempt, the computer will be encrypted.</span></span></p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="dabad-183">Définitions de stratégies de disque fixes</span><span class="sxs-lookup"><span data-stu-id="dabad-183">Fixed Drive policy definitions</span></span>


<span data-ttu-id="dabad-184">Cette section décrit les définitions de stratégie de lecteur fixes pour MBAM, qui se trouvent dans le nœud d’objet de stratégie de groupe suivant: **Configuration ordinateur** \\ **modèles d’administration** \\ **composants Windows** \\ **MDOP MBAM (gestion de BitLocker)**  \\  **Fixed Drive**.</span><span class="sxs-lookup"><span data-stu-id="dabad-184">This section describes the Fixed Drive policy definitions for MBAM, which can be found at the following GPO node: **Computer Configuration**\\**Administrative Templates**\\**Windows Components**\\**MDOP MBAM (BitLocker Management)** \\ **Fixed Drive**.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="dabad-185">Nom de la stratégie</span><span class="sxs-lookup"><span data-stu-id="dabad-185">Policy Name</span></span></th>
<th align="left"><span data-ttu-id="dabad-186">Vue d’ensemble et paramètre de stratégie suggéré</span><span class="sxs-lookup"><span data-stu-id="dabad-186">Overview and Suggested Policy Setting</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="dabad-187">Paramètres de chiffrement des lecteurs de données fixes</span><span class="sxs-lookup"><span data-stu-id="dabad-187">Fixed data drive encryption settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="dabad-188">Configuration suggérée: <strong> activé </strong> , puis activez la case <strong> à cocher Activer le verrouillage automatique des données </strong> si le volume du système d’exploitation doit être chiffré.</span><span class="sxs-lookup"><span data-stu-id="dabad-188">Suggested Configuration: <strong>Enabled</strong>, and select the <strong>Enable auto-unlock fixed data drive</strong> check box if the operating system volume is required to be encrypted.</span></span></p>
<p><span data-ttu-id="dabad-189">Ce paramètre de stratégie vous permet de gérer l’activation ou non du chiffrement des lecteurs fixes.</span><span class="sxs-lookup"><span data-stu-id="dabad-189">This policy setting lets you manage whether or not to encrypt the fixed drives.</span></span></p>
<p><span data-ttu-id="dabad-190">Lorsque vous activez cette stratégie, ne désactivez pas la <strong> stratégie configurer l’utilisation du mot de passe pour les lecteurs de données fixes </strong> .</span><span class="sxs-lookup"><span data-stu-id="dabad-190">When you enable this policy, do not disable the <strong>Configure use of password for fixed data drives</strong> policy.</span></span></p>
<p><span data-ttu-id="dabad-191">Si la <strong> case à cocher Activer le verrouillage automatique des données du disque </strong> est activée, le volume du système d’exploitation doit être chiffré.</span><span class="sxs-lookup"><span data-stu-id="dabad-191">If the <strong>Enable auto-unlock fixed data drive</strong> check box is selected, the operating system volume must be encrypted.</span></span></p>
<p><span data-ttu-id="dabad-192">Si vous activez ce paramètre de stratégie, les utilisateurs doivent placer tous les disques fixes sous protection BitLocker, qui chiffreront les lecteurs.</span><span class="sxs-lookup"><span data-stu-id="dabad-192">If you enable this policy setting, users are required to put all fixed drives under BitLocker protection, which will encrypt the drives.</span></span></p>
<p><span data-ttu-id="dabad-193">Si vous ne configurez pas cette stratégie ou si vous désactivez ce paramètre, les utilisateurs ne sont pas obligés de placer des lecteurs corrigés dans la protection BitLocker.</span><span class="sxs-lookup"><span data-stu-id="dabad-193">If you do not configure this policy or if you disable this policy, users are not required to put fixed drives under BitLocker protection.</span></span></p>
<p><span data-ttu-id="dabad-194">Si vous désactivez cette stratégie, l’agent MBAM déchiffre les lecteurs fixes chiffrés.</span><span class="sxs-lookup"><span data-stu-id="dabad-194">If you disable this policy, the MBAM agent decrypts any encrypted fixed drives.</span></span></p>
<p><span data-ttu-id="dabad-195">Si le chiffrement du volume du système d’exploitation n’est pas nécessaire, décochez la <strong> case Activer le verrouillage automatique du lecteur de données </strong> .</span><span class="sxs-lookup"><span data-stu-id="dabad-195">If encrypting the operating system volume is not required, clear the <strong>Enable auto-unlock fixed data drive</strong> check box.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="dabad-196">Refuser l’autorisation «écrire» pour les disques fixes qui ne sont pas protégés par BitLocker</span><span class="sxs-lookup"><span data-stu-id="dabad-196">Deny “write” permission to fixed drives that are not protected by BitLocker</span></span></p></td>
<td align="left"><p><span data-ttu-id="dabad-197">Configuration suggérée: <strong> non configuré</span><span class="sxs-lookup"><span data-stu-id="dabad-197">Suggested Configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="dabad-198">Ce paramètre de stratégie détermine si la protection de BitLocker est requise pour les lecteurs fixes sur un ordinateur de sorte qu’ils soient accessibles en écriture.</span><span class="sxs-lookup"><span data-stu-id="dabad-198">This policy setting determines if BitLocker protection is required for fixed drives on a computer so that they are writable.</span></span> <span data-ttu-id="dabad-199">Ce paramètre de stratégie est appliqué lorsque vous activez BitLocker.</span><span class="sxs-lookup"><span data-stu-id="dabad-199">This policy setting is applied when you turn on BitLocker.</span></span></p>
<p><span data-ttu-id="dabad-200">Lorsque la stratégie n’est pas configurée, tous les lecteurs fixes de l’ordinateur sont montés avec des autorisations en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="dabad-200">When the policy is not configured, all fixed drives on the computer are mounted with read/write permissions.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="dabad-201">Autoriser l’accès à des disques durs fixes protégés par BitLocker provenant de versions antérieures de Windows</span><span class="sxs-lookup"><span data-stu-id="dabad-201">Allow access to BitLocker-protected fixed drives from earlier versions of Windows</span></span></p></td>
<td align="left"><p><span data-ttu-id="dabad-202">Configuration suggérée: <strong> non configuré</span><span class="sxs-lookup"><span data-stu-id="dabad-202">Suggested configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="dabad-203">Activez cette stratégie pour déverrouiller et afficher les disques fixes mis en forme à l’aide du système de fichiers FAT (File Allocation Table) sur les ordinateurs exécutant Windows Server 2008, Windows Vista, Windows XP SP3 ou Windows XP SP2.</span><span class="sxs-lookup"><span data-stu-id="dabad-203">Enable this policy to unlock and view the fixed drives that are formatted with the file allocation table (FAT) file system on computers that are running Windows Server 2008, Windows Vista, Windows XP with SP3, or Windows XP with SP2.</span></span></p>
<p><span data-ttu-id="dabad-204">Ces systèmes d’exploitation disposent d’autorisations en lecture seule sur les lecteurs protégés par BitLocker.</span><span class="sxs-lookup"><span data-stu-id="dabad-204">These operating systems have read-only permissions to BitLocker-protected drives.</span></span></p>
<p><span data-ttu-id="dabad-205">Lorsque la stratégie est désactivée, les disques fixes mis en forme avec le système de fichiers FAT ne peuvent pas être déverrouillés et leur contenu ne peut pas être affiché sur les ordinateurs exécutant Windows Server 2008, Windows Vista, Windows XP SP3 ou Windows XP SP2.</span><span class="sxs-lookup"><span data-stu-id="dabad-205">When the policy is disabled, fixed drives formatted with the FAT file system cannot be unlocked and their content cannot be viewed on computers that are running Windows Server 2008, Windows Vista, Windows XP with SP3, or Windows XP with SP2.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="dabad-206">Configurer l’utilisation du mot de passe pour les disques fixes</span><span class="sxs-lookup"><span data-stu-id="dabad-206">Configure use of password for fixed drives</span></span></p></td>
<td align="left"><p><span data-ttu-id="dabad-207">Configuration suggérée: <strong> non configuré</span><span class="sxs-lookup"><span data-stu-id="dabad-207">Suggested configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="dabad-208">Activez cette stratégie pour configurer la protection par mot de passe sur des disques fixes.</span><span class="sxs-lookup"><span data-stu-id="dabad-208">Enable this policy to configure password protection on fixed drives.</span></span></p>
<p><span data-ttu-id="dabad-209">Lorsque la stratégie n’est pas configurée, les mots de passe sont pris en charge avec les paramètres par défaut, qui n’incluent pas les exigences de complexité des mots de passe et ne nécessitent que huit caractères.</span><span class="sxs-lookup"><span data-stu-id="dabad-209">When the policy is not configured, passwords will be supported with the default settings, which do not include password complexity requirements and require only eight characters.</span></span></p>
<p><span data-ttu-id="dabad-210">Pour une sécurité accrue, activez cette stratégie et sélectionnez <strong> exiger un mot de passe pour le lecteur de données fixes </strong> , sélectionnez <strong> nécessite une complexité du mot de passe </strong> , puis définissez la <strong> longueur de mot de passe minimale souhaitée </strong> .</span><span class="sxs-lookup"><span data-stu-id="dabad-210">For higher security, enable this policy and select <strong>Require password for fixed data drive</strong>, select <strong>Require password complexity</strong>, and set the desired <strong>minimum password length</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="dabad-211">Choisir la manière dont les lecteurs fixes protégés par BitLocker peuvent être récupérés</span><span class="sxs-lookup"><span data-stu-id="dabad-211">Choose how BitLocker-protected fixed drives can be recovered</span></span></p></td>
<td align="left"><p><span data-ttu-id="dabad-212">Configuration suggérée: <strong> non configuré</span><span class="sxs-lookup"><span data-stu-id="dabad-212">Suggested Configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="dabad-213">Configurez cette stratégie pour activer l’agent de récupération de données BitLocker ou enregistrer les informations de récupération BitLocker dans les services de domaine Active Directory (AD DS).</span><span class="sxs-lookup"><span data-stu-id="dabad-213">Configure this policy to enable the BitLocker data recovery agent or to save BitLocker recovery information to Active Directory Domain Services (AD DS).</span></span></p>
<p><span data-ttu-id="dabad-214">Lorsque cette stratégie n’est pas configurée, l’agent de récupération de données BitLocker est autorisé et les informations de récupération ne sont pas sauvegardées dans AD DS.</span><span class="sxs-lookup"><span data-stu-id="dabad-214">When this policy is not configured, the BitLocker data recovery agent is allowed, and recovery information is not backed up to AD DS.</span></span> <span data-ttu-id="dabad-215">MBAM n’exige pas que les informations de récupération soient sauvegardées dans AD DS.</span><span class="sxs-lookup"><span data-stu-id="dabad-215">MBAM does not require the recovery information to be backed up to AD DS.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="dabad-216">Définitions de la stratégie de lecteur du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="dabad-216">Operating System Drive policy definitions</span></span>


<span data-ttu-id="dabad-217">Cette section décrit les définitions de la stratégie de lecteur du système d’exploitation pour MBAM, qui se trouvent dans le nœud d’objet GPO suivant: **Configuration ordinateur** \\ **modèles d’administration** \\ **composants Windows** \\ **MDOP MBAM (gestion de BitLocker)**  \\  **Operating System Drive**.</span><span class="sxs-lookup"><span data-stu-id="dabad-217">This section describes the Operating System Drive policy definitions for MBAM, found at the following GPO node: **Computer Configuration**\\**Administrative Templates**\\**Windows Components**\\**MDOP MBAM (BitLocker Management)** \\ **Operating System Drive**.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="dabad-218">Nom de la stratégie</span><span class="sxs-lookup"><span data-stu-id="dabad-218">Policy Name</span></span></th>
<th align="left"><span data-ttu-id="dabad-219">Vue d’ensemble et paramètre de stratégie suggéré</span><span class="sxs-lookup"><span data-stu-id="dabad-219">Overview and Suggested Policy Setting</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="dabad-220">Paramètres de chiffrement de lecteur du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="dabad-220">Operating system drive encryption settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="dabad-221">Configuration suggérée: <strong> activée</span><span class="sxs-lookup"><span data-stu-id="dabad-221">Suggested configuration: <strong>Enabled</span></span></strong></p>
<p><span data-ttu-id="dabad-222">Ce paramètre de stratégie détermine si le lecteur du système d’exploitation sera crypté.</span><span class="sxs-lookup"><span data-stu-id="dabad-222">This policy setting determines if the operating system drive will be encrypted.</span></span></p>
<p><span data-ttu-id="dabad-223">Configurez cette stratégie pour effectuer les opérations suivantes:</span><span class="sxs-lookup"><span data-stu-id="dabad-223">Configure this policy to do the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="dabad-224">Appliquez la protection BitLocker pour le lecteur du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="dabad-224">Enforce BitLocker protection for the operating system drive.</span></span></p></li>
<li><p><span data-ttu-id="dabad-225">Configurer l’utilisation du code confidentiel pour utiliser un code PIN de module de plateforme sécurisée (TPM) pour la protection du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="dabad-225">Configure PIN usage to use a Trusted Platform Module (TPM) PIN for operating system protection.</span></span></p></li>
<li><p><span data-ttu-id="dabad-226">Configurez les broches de démarrage améliorées pour autoriser les caractères tels que les lettres majuscules et minuscules et les nombres.</span><span class="sxs-lookup"><span data-stu-id="dabad-226">Configure enhanced startup PINs to permit characters such as uppercase and lowercase letters, and numbers.</span></span> <span data-ttu-id="dabad-227">MBAM ne prend pas en charge l’utilisation de symboles et d’espaces pour les broches améliorées, même si BitLocker prend en charge les symboles et les espaces.</span><span class="sxs-lookup"><span data-stu-id="dabad-227">MBAM does not support the use of symbols and spaces for enhanced PINs, even though BitLocker supports symbols and spaces.</span></span></p></li>
</ul>
<p><span data-ttu-id="dabad-228">Si vous activez ce paramètre de stratégie, les utilisateurs sont obligés de sécuriser le lecteur du système d’exploitation à l’aide de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="dabad-228">If you enable this policy setting, users are required to secure the operating system drive by using BitLocker.</span></span></p>
<p><span data-ttu-id="dabad-229">Si vous ne configurez pas ou si vous désactivez ce paramètre, les utilisateurs ne sont pas obligés de sécuriser le lecteur du système d’exploitation à l’aide de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="dabad-229">If you do not configure or if you disable the setting, users are not required to secure the operating system drive by using BitLocker.</span></span></p>
<p><span data-ttu-id="dabad-230">Si vous désactivez cette stratégie, l’agent MBAM déchiffre le volume du système d’exploitation s’il est chiffré.</span><span class="sxs-lookup"><span data-stu-id="dabad-230">If you disable this policy, the MBAM agent decrypts the operating system volume if it is encrypted.</span></span></p>
<p><span data-ttu-id="dabad-231">Lorsqu’il est activé, ce paramètre de stratégie demande aux utilisateurs de sécuriser le système d’exploitation à l’aide de la protection BitLocker et le lecteur est chiffré.</span><span class="sxs-lookup"><span data-stu-id="dabad-231">When it is enabled, this policy setting requires users to secure the operating system by using BitLocker protection, and the drive is encrypted.</span></span> <span data-ttu-id="dabad-232">En fonction de votre configuration requise pour le chiffrement, vous pouvez sélectionner la méthode de protection du lecteur du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="dabad-232">Based on your encryption requirements, you may select the method of protection for the operating system drive.</span></span></p>
<p><span data-ttu-id="dabad-233">Pour plus de sécurité, utilisez TPM + code confidentiel, autorisez les codes confidentiels et définissez une longueur minimale de huit caractères.</span><span class="sxs-lookup"><span data-stu-id="dabad-233">For higher security requirements, use TPM + PIN, allow enhanced PINs, and set the minimum PIN length to eight characters.</span></span></p>
<p><span data-ttu-id="dabad-234">Lorsque cette stratégie est activée avec le protecteur de code confidentiel, vous pouvez envisager de désactiver les stratégies suivantes dans les paramètres de veille de la gestion de l' <strong> </strong>  /  <strong> alimentation système </strong>  /  <strong> </strong> :</span><span class="sxs-lookup"><span data-stu-id="dabad-234">When this policy is enabled with the TPM + PIN protector, you can consider disabling the following policies under <strong>System</strong> / <strong>Power Management</strong> / <strong>Sleep Settings</strong>:</span></span></p>
<ul>
<li><p><span data-ttu-id="dabad-235">Autoriser les États de veille (S1-S3) lorsque vous êtes en veille (branché)</span><span class="sxs-lookup"><span data-stu-id="dabad-235">Allow Standby States (S1-S3) When Sleeping (Plugged In)</span></span></p></li>
<li><p><span data-ttu-id="dabad-236">Autoriser les États de veille (S1-S3) en veille (sur batterie)</span><span class="sxs-lookup"><span data-stu-id="dabad-236">Allow Standby States (S1-S3) When Sleeping (On Battery)</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="dabad-237">Configurer le profil de validation de plateforme TPM</span><span class="sxs-lookup"><span data-stu-id="dabad-237">Configure TPM platform validation profile</span></span></p></td>
<td align="left"><p><span data-ttu-id="dabad-238">Configuration suggérée: <strong> non configuré</span><span class="sxs-lookup"><span data-stu-id="dabad-238">Suggested Configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="dabad-239">Ce paramètre de stratégie vous permet de configurer la manière dont le matériel de sécurité du TPM sur un ordinateur sécurise la clé de chiffrement BitLocker.</span><span class="sxs-lookup"><span data-stu-id="dabad-239">This policy setting lets you configure how the TPM security hardware on a computer secures the BitLocker encryption key.</span></span> <span data-ttu-id="dabad-240">Ce paramètre de stratégie ne s’applique pas si l’ordinateur ne possède pas de TPM compatible ou s’il possède déjà une protection de module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="dabad-240">This policy setting does not apply if the computer does not have a compatible TPM or if BitLocker already has TPM protection enabled.</span></span></p>
<p><span data-ttu-id="dabad-241">Lorsque cette stratégie n’est pas configurée, le TPM utilise le profil de validation de plateforme par défaut ou le profil de validation de plateforme spécifié par le script de configuration.</span><span class="sxs-lookup"><span data-stu-id="dabad-241">When this policy is not configured, the TPM uses the default platform validation profile or the platform validation profile specified by the setup script.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="dabad-242">Choisir la méthode de récupération des lecteurs du système d’exploitation protégés par BitLocker</span><span class="sxs-lookup"><span data-stu-id="dabad-242">Choose how to recover BitLocker-protected operating system drives</span></span></p></td>
<td align="left"><p><span data-ttu-id="dabad-243">Configuration suggérée: <strong> non configuré</span><span class="sxs-lookup"><span data-stu-id="dabad-243">Suggested Configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="dabad-244">Configurez cette stratégie pour activer l’agent de récupération de données BitLocker ou enregistrer les informations de récupération BitLocker dans les services de domaine Active Directory (AD DS).</span><span class="sxs-lookup"><span data-stu-id="dabad-244">Configure this policy to enable the BitLocker data recovery agent or to save BitLocker recovery information to Active Directory Domain Services (AD DS).</span></span></p>
<p><span data-ttu-id="dabad-245">Lorsque cette stratégie n’est pas configurée, l’agent de récupération de données est autorisé et les informations de récupération ne sont pas sauvegardées dans AD DS.</span><span class="sxs-lookup"><span data-stu-id="dabad-245">When this policy is not configured, the data recovery agent is allowed, and the recovery information is not backed up to AD DS.</span></span></p>
<p><span data-ttu-id="dabad-246">MBAM opération ne nécessite pas que les informations de récupération soient sauvegardées dans AD DS.</span><span class="sxs-lookup"><span data-stu-id="dabad-246">MBAM operation does not require the recovery information to be backed up to AD DS.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="dabad-247">Définitions de la stratégie de lecteur amovible</span><span class="sxs-lookup"><span data-stu-id="dabad-247">Removable Drive policy definitions</span></span>


<span data-ttu-id="dabad-248">Cette section décrit les définitions de stratégie de lecteur amovible pour MBAM, qui se trouvent dans le nœud d’objet GPO suivant: **Configuration ordinateur** \\ **modèles d’administration** \\ **composants Windows** \\ **MDOP MBAM (gestion de BitLocker)**  \\  **Removable Drive**.</span><span class="sxs-lookup"><span data-stu-id="dabad-248">This section describes the Removable Drive Policy definitions for MBAM, found at the following GPO node: **Computer Configuration**\\**Administrative Templates**\\**Windows Components**\\**MDOP MBAM (BitLocker Management)** \\ **Removable Drive**.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="dabad-249">Nom de la stratégie</span><span class="sxs-lookup"><span data-stu-id="dabad-249">Policy Name</span></span></th>
<th align="left"><span data-ttu-id="dabad-250">Vue d’ensemble et paramètre de stratégie suggéré</span><span class="sxs-lookup"><span data-stu-id="dabad-250">Overview and Suggested Policy Setting</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="dabad-251">Contrôler l’utilisation de BitLocker sur des lecteurs amovibles</span><span class="sxs-lookup"><span data-stu-id="dabad-251">Control the use of BitLocker on removable drives</span></span></p></td>
<td align="left"><p><span data-ttu-id="dabad-252">Configuration suggérée: <strong> activée</span><span class="sxs-lookup"><span data-stu-id="dabad-252">Suggested configuration: <strong>Enabled</span></span></strong></p>
<p><span data-ttu-id="dabad-253">Cette stratégie contrôle l’utilisation de BitLocker sur les lecteurs de données amovibles.</span><span class="sxs-lookup"><span data-stu-id="dabad-253">This policy controls the use of BitLocker on removable data drives.</span></span></p>
<p><span data-ttu-id="dabad-254">Activez l' <strong> option autoriser les utilisateurs à appliquer la protection BitLocker sur les lecteurs de données amovibles </strong> pour permettre aux utilisateurs d’exécuter l’Assistant Configuration de BitLocker sur un lecteur de données amovible.</span><span class="sxs-lookup"><span data-stu-id="dabad-254">Enable the <strong>Allow users to apply BitLocker protection on removable data drives</strong> option, to allow users to run the BitLocker setup wizard on a removable data drive.</span></span></p>
<p><span data-ttu-id="dabad-255">Activez l' <strong> option permettre aux utilisateurs de suspendre et de déchiffrer les disques BitLocker sur des lecteurs de données amovibles </strong> pour permettre aux utilisateurs de supprimer le chiffrement de lecteur BitLocker du lecteur ou de suspendre le chiffrement lors de la maintenance.</span><span class="sxs-lookup"><span data-stu-id="dabad-255">Enable the <strong>Allow users to suspend and decrypt BitLocker on removable data drives</strong> option to allow users to remove BitLocker drive encryption from the drive or to suspend the encryption while maintenance is performed.</span></span></p>
<p><span data-ttu-id="dabad-256">Lorsque cette stratégie est activée et que l' <strong> option autoriser les utilisateurs à appliquer la protection BitLocker sur les lecteurs de données amovibles </strong> est activée, le client MBAM enregistre les informations de récupération relatives aux lecteurs amovibles sur le serveur de récupération de clés MBAM, et permet aux utilisateurs de récupérer le lecteur en cas de perte du mot de passe.</span><span class="sxs-lookup"><span data-stu-id="dabad-256">When this policy is enabled and the <strong>Allow users to apply BitLocker protection on removable data drives</strong> option is selected, the MBAM Client saves the recovery information about removable drives to the MBAM key recovery server, and it allows users to recover the drive if the password is lost.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="dabad-257">Refuser les autorisations d’écriture sur des lecteurs amovibles qui ne sont pas protégés par BitLocker</span><span class="sxs-lookup"><span data-stu-id="dabad-257">Deny the “write” permissions to removable drives that are not protected by BitLocker</span></span></p></td>
<td align="left"><p><span data-ttu-id="dabad-258">Configuration suggérée: <strong> non configuré</span><span class="sxs-lookup"><span data-stu-id="dabad-258">Suggested Configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="dabad-259">Activez cette stratégie pour autoriser les autorisations d’écriture seule sur les lecteurs protégés par BitLocker.</span><span class="sxs-lookup"><span data-stu-id="dabad-259">Enable this policy to allow write-only permissions to BitLocker protected drives.</span></span></p>
<p><span data-ttu-id="dabad-260">Lorsque cette stratégie est activée, tous les lecteurs de données amovibles de l’ordinateur doivent être chiffrés avant que les autorisations d’écriture soient autorisées.</span><span class="sxs-lookup"><span data-stu-id="dabad-260">When this policy is enabled, all removable data drives on the computer require encryption before write permissions are allowed.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="dabad-261">Autoriser l’accès aux lecteurs amovibles protégés par BitLocker provenant de versions antérieures de Windows</span><span class="sxs-lookup"><span data-stu-id="dabad-261">Allow access to BitLocker-protected removable drives from earlier versions of Windows</span></span></p></td>
<td align="left"><p><span data-ttu-id="dabad-262">Configuration suggérée: <strong> non configuré</span><span class="sxs-lookup"><span data-stu-id="dabad-262">Suggested Configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="dabad-263">Activez cette stratégie pour déverrouiller et afficher les disques fixes qui sont mis en forme avec le système de fichiers (FAT) sur les ordinateurs exécutant Windows Server 2008, Windows Vista, Windows XP avec SP3 ou Windows XP SP2.</span><span class="sxs-lookup"><span data-stu-id="dabad-263">Enable this policy to unlock and view the fixed drives that are formatted with the (FAT) file system on computers that are running Windows Server 2008, Windows Vista, Windows XP with SP3, or Windows XP with SP2.</span></span></p>
<p><span data-ttu-id="dabad-264">Ces systèmes d’exploitation disposent d’autorisations en lecture seule sur les lecteurs protégés par BitLocker.</span><span class="sxs-lookup"><span data-stu-id="dabad-264">These operating systems have read-only permissions to BitLocker-protected drives.</span></span></p>
<p><span data-ttu-id="dabad-265">Lorsque la stratégie est désactivée, les lecteurs amovibles mis en forme avec le système de fichiers FAT ne peuvent pas être déverrouillés et leur contenu ne peut pas être affiché sur les ordinateurs exécutant Windows Server 2008, Windows Vista, Windows XP SP3 ou Windows XP SP2.</span><span class="sxs-lookup"><span data-stu-id="dabad-265">When the policy is disabled, removable drives formatted with the FAT file system cannot be unlocked and their content cannot be viewed on computers that are running Windows Server 2008, Windows Vista, Windows XP with SP3, or Windows XP with SP2.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="dabad-266">Configurer l’utilisation du mot de passe pour les lecteurs de données amovibles</span><span class="sxs-lookup"><span data-stu-id="dabad-266">Configure the use of password for removable data drives</span></span></p></td>
<td align="left"><p><span data-ttu-id="dabad-267">Configuration suggérée: <strong> non configuré</span><span class="sxs-lookup"><span data-stu-id="dabad-267">Suggested configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="dabad-268">Activez cette stratégie pour configurer la protection par mot de passe sur les lecteurs de données amovibles.</span><span class="sxs-lookup"><span data-stu-id="dabad-268">Enable this policy to configure password protection on removable data drives.</span></span></p>
<p><span data-ttu-id="dabad-269">Lorsque cette stratégie n’est pas configurée, les mots de passe sont pris en charge avec les paramètres par défaut, qui n’incluent pas les exigences de complexité des mots de passe et ne nécessitent que huit caractères.</span><span class="sxs-lookup"><span data-stu-id="dabad-269">When this policy is not configured, passwords are supported with the default settings, which do not include password complexity requirements and require only eight characters.</span></span></p>
<p><span data-ttu-id="dabad-270">Pour une sécurité accrue, vous pouvez activer cette stratégie et sélectionner <strong> exiger un mot de passe pour le lecteur de données amovibles </strong> , sélectionner <strong> exiger une complexité du mot de passe </strong> , puis définir la <strong> longueur minimale du mot de passe </strong> .</span><span class="sxs-lookup"><span data-stu-id="dabad-270">For increased security, you can enable this policy and select <strong>Require password for removable data drive</strong>, select <strong>Require password complexity</strong>, and then set the preferred <strong>minimum password length</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="dabad-271">Choisir la manière dont les lecteurs amovibles protégés par BitLocker peuvent être récupérés</span><span class="sxs-lookup"><span data-stu-id="dabad-271">Choose how BitLocker-protected removable drives can be recovered</span></span></p></td>
<td align="left"><p><span data-ttu-id="dabad-272">Configuration suggérée: <strong> non configuré</span><span class="sxs-lookup"><span data-stu-id="dabad-272">Suggested Configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="dabad-273">Vous pouvez configurer cette stratégie pour activer l’agent de récupération de données BitLocker ou enregistrer les informations de récupération BitLocker dans les services de domaine Active Directory (AD DS).</span><span class="sxs-lookup"><span data-stu-id="dabad-273">You can configure this policy to enable the BitLocker data recovery agent or to save BitLocker recovery information to Active Directory Domain Services (AD DS).</span></span></p>
<p><span data-ttu-id="dabad-274">Lorsque la stratégie est définie sur <strong> non configuré </strong> , l’agent de récupération de données est autorisé et les informations de récupération ne sont pas sauvegardées dans AD DS.</span><span class="sxs-lookup"><span data-stu-id="dabad-274">When the policy is set to <strong>Not Configured</strong>, the data recovery agent is allowed and recovery information is not backed up to AD DS.</span></span></p>
<p><span data-ttu-id="dabad-275">MBAM opération ne nécessite pas que les informations de récupération soient sauvegardées dans AD DS.</span><span class="sxs-lookup"><span data-stu-id="dabad-275">MBAM operation does not require the recovery information to be backed up to AD DS.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="dabad-276">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="dabad-276">Related topics</span></span>


[<span data-ttu-id="dabad-277">Préparation de votre environnement pour MBAM1.0</span><span class="sxs-lookup"><span data-stu-id="dabad-277">Preparing your Environment for MBAM 1.0</span></span>](preparing-your-environment-for-mbam-10.md)









