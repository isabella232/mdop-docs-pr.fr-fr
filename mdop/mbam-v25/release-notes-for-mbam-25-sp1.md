---
title: Notes de publication de MBAM2.5 SP1
description: Notes de publication de MBAM2.5 SP1
author: dansimp
ms.assetid: 3ac424c8-c490-4d62-aba4-1b462c02e962
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 09/06/2017
ms.openlocfilehash: 837892897aeca341433de54aca1228c0faeee124
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810884"
---
# <span data-ttu-id="dce31-103">Notes de publication de MBAM2.5 SP1</span><span class="sxs-lookup"><span data-stu-id="dce31-103">Release Notes for MBAM 2.5 SP1</span></span>


<span data-ttu-id="dce31-104">Pour effectuer une recherche dans ces notes de publication, appuyez sur Ctrl + F.</span><span class="sxs-lookup"><span data-stu-id="dce31-104">To search these release notes, press Ctrl+F.</span></span>

<span data-ttu-id="dce31-105">Lisez attentivement ces notes de publication avant d’installer Microsoft BitLocker Administration and Monitoring (MBAM) 2,5 SP1.</span><span class="sxs-lookup"><span data-stu-id="dce31-105">Read these release notes thoroughly before you install Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 SP1.</span></span> <span data-ttu-id="dce31-106">Ces notes de publication contiennent des informations nécessaires à l’installation réussie de MBAM et contiennent des informations qui ne sont pas disponibles dans la documentation du produit.</span><span class="sxs-lookup"><span data-stu-id="dce31-106">These release notes contain information that is required to successfully install MBAM and can contain information that is not available in the product documentation.</span></span> <span data-ttu-id="dce31-107">Si ces notes de publication diffèrent d’autres MBAM 2,5 SP1, considérez la dernière modification comme faisant autorité.</span><span class="sxs-lookup"><span data-stu-id="dce31-107">If these release notes differ from other MBAM 2.5 SP1 documentation, consider the latest change to be authoritative.</span></span> <span data-ttu-id="dce31-108">Ces notes de publication remplacent le contenu qui est inclus dans ce produit.</span><span class="sxs-lookup"><span data-stu-id="dce31-108">These release notes supersede the content that is included with this product.</span></span>

## <a href="" id="---------mbam-2-5-sp1-known-issues"></a> <span data-ttu-id="dce31-109">Problèmes connus de MBAM 2,5 SP1</span><span class="sxs-lookup"><span data-stu-id="dce31-109">MBAM 2.5 SP1 known issues</span></span>


<span data-ttu-id="dce31-110">Cette section contient des notes de publication pour MBAM 2,5 SP1.</span><span class="sxs-lookup"><span data-stu-id="dce31-110">This section contains release notes for MBAM 2.5 SP1.</span></span>

### <a href="" id="powershell-read-ad--cmdlets-do-not-provide-feedback-if-user-does-not-have-sufficient-rights"></a><span data-ttu-id="dce31-111">Les applets de cmdlet de lecture-publicité pour PowerShell ne fournissent pas de commentaires si l’utilisateur ne dispose pas de droits suffisants</span><span class="sxs-lookup"><span data-stu-id="dce31-111">PowerShell Read-AD\* cmdlets do not provide feedback if user does not have sufficient rights</span></span>

<span data-ttu-id="dce31-112">Si un utilisateur tente d’utiliser les applets de contrôle PowerShell lecture-AD pour le serveur MBAM n’a pas de droits d’utilisateur pour lire les informations de récupération Active Directory ou pour lire les informations du TPM, les applets de contrôle ne fournissent aucun message d’erreur ou d’avertissement à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="dce31-112">If a user trying to use the PowerShell Read-AD\* cmdlets for the MBAM Server does not have user rights to read the Active Directory recovery information or to read the TPM information, the cmdlets will not provide the user with any error or warning.</span></span>

<span data-ttu-id="dce31-113">**Solution de contournement:** Utilisez uniquement les applets de applet de lecture/publicité PowerShell Si vous disposez des droits d’utilisateur requis.</span><span class="sxs-lookup"><span data-stu-id="dce31-113">**Workaround:** Only use the PowerShell Read-AD\* cmdlets if you have the required user rights.</span></span>

### <span data-ttu-id="dce31-114">Les applets de commande de migration MBAM Active Directory (AD) ne récupèrent pas les informations de récupération de volume</span><span class="sxs-lookup"><span data-stu-id="dce31-114">MBAM Active Directory (AD) Migration cmdlets do not retrieve volume recovery information</span></span>

<span data-ttu-id="dce31-115">Les applets de commande de migration MBAM Active Directory (AD) ne peuvent pas récupérer les informations de récupération de volume pour les ordinateurs dans les unités d’organisation (UO) si le caractère barre oblique (/) fait partie du nom de l’unité d’organisation.</span><span class="sxs-lookup"><span data-stu-id="dce31-115">MBAM Active Directory (AD) Migration cmdlets fail to retrieve volume recovery information for computers in organizational units (OUs) if the forward slash character (/) is part of the OU name.</span></span> <span data-ttu-id="dce31-116">Les extractions publicitaires répétées échoueront en raison d’une erreur de canal de terminaison lorsque cette erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="dce31-116">Repeated AD pulls will fail with a pipeline terminating error when this error is encountered.</span></span>

<span data-ttu-id="dce31-117">**Détails techniques:** Ce message d’erreur s’affiche lorsque vous exécutez la commande suivante:</span><span class="sxs-lookup"><span data-stu-id="dce31-117">**Technical Details:** You will see this error when running the command:</span></span>

``` syntax
Read-ADRecoveryInformation : Unknown error (0x80005000)
At line:1 char:1
+ Read-ADRecoveryInformation -Server "…" -SearchBase " ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : NotSpecified: (:) [Read-ADRecoveryInformation], COMException
    + FullyQualifiedErrorId : System.Runtime.InteropServices.COMException,Microsoft.Mbam.Server.Commands.ADPullCommands.ReadADRecoveryInformationCommand
```

<span data-ttu-id="dce31-118">De plus, la trace de pile d’exception `Error[0].Exception.StackTrace` ressemble à ceci:</span><span class="sxs-lookup"><span data-stu-id="dce31-118">In addition, the Exception stack trace `Error[0].Exception.StackTrace` will look like this:</span></span>

``` syntax
   at System.DirectoryServices.DirectoryEntry.Bind(Boolean throwIfFail)
   at System.DirectoryServices.DirectoryEntry.Bind()
   at System.DirectoryServices.DirectoryEntry.get_AdsObject()
   at System.DirectoryServices.PropertyValueCollection.PopulateList()
   at System.DirectoryServices.PropertyValueCollection..ctor(DirectoryEntry entry, String propertyName)
   at System.DirectoryServices.PropertyCollection.get_Item(String propertyName)
   at Microsoft.Mbam.Server.Commands.ADPullCommands.ReadCore.VerifySettingsConnectivity()
   at Microsoft.Mbam.Server.Commands.ADPullCommands.ReadCore.ExecuteRead()
   at Microsoft.Mbam.Server.Commands.ADPullCommands.ReadADInformationBase.ProcessRecord()
   at System.Management.Automation.CommandProcessor.ProcessRecord()
```

<span data-ttu-id="dce31-119">**Solution de contournement:** Pour résoudre ce problème, effectuez l’une des opérations suivantes:</span><span class="sxs-lookup"><span data-stu-id="dce31-119">**Workaround:** Perform one of these tasks to resolve this situation:</span></span>

-   <span data-ttu-id="dce31-120">Renommez l’unité d’organisation pour supprimer le caractère barre oblique avant d’exécuter le script.</span><span class="sxs-lookup"><span data-stu-id="dce31-120">Rename the OU to remove the forward slash character and then run the script.</span></span>

-   <span data-ttu-id="dce31-121">Pour exclure toute unité d’organisation problématique du processus de sauvegarde, recherchez une liste d’unités d’organisation dont les noms ne contiennent pas de caractères de barre oblique.</span><span class="sxs-lookup"><span data-stu-id="dce31-121">To exclude any problematic OU from the backup process, find a list of OUs whose names do not contain the forward slash character.</span></span> <span data-ttu-id="dce31-122">Exécutez le script sur ces UO, une unité d’organisation à la fois.</span><span class="sxs-lookup"><span data-stu-id="dce31-122">Run the script on these OUs, one OU at a time.</span></span>

### <a href="" id="-------------mbam-fails-to-encrypt-a-volume-and-reports-an-error-if-you-set-a-tpm---pin-protector-on-a-tablet-device"></a> <span data-ttu-id="dce31-123">MBAM ne parvient pas à chiffrer un volume et signale une erreur si vous avez configuré un module de protection TPM + PIN sur un appareil de tablette</span><span class="sxs-lookup"><span data-stu-id="dce31-123">MBAM fails to encrypt a volume and reports an error if you set a TPM + PIN protector on a tablet device</span></span>

<span data-ttu-id="dce31-124">Si les utilisateurs finaux essaient de définir un protecteur de plateforme sécurisée + code confidentiel sur un appareil de tablette, MBAM ne peut pas être chiffré et signale une erreur.</span><span class="sxs-lookup"><span data-stu-id="dce31-124">If end users try to set a TPM + PIN protector on a tablet device, MBAM fails to encrypt, and it reports an error.</span></span> <span data-ttu-id="dce31-125">Ce problème survient parce que les appareils tablettes n’ont pas de clavier d’environnement de pré-démarrage.</span><span class="sxs-lookup"><span data-stu-id="dce31-125">This issue occurs because tablet devices do not have a pre-boot environment keyboard.</span></span>

<span data-ttu-id="dce31-126">**Solution de contournement:** Activez l’option **activer l’authentification BitLocker nécessitant une entrée au clavier prédémarrage sur des tablettes** .</span><span class="sxs-lookup"><span data-stu-id="dce31-126">**Workaround:** Enable the **Enable use of BitLocker authentication requiring preboot keyboard input on tablets** Group Policy setting.</span></span> <span data-ttu-id="dce31-127">Ce paramètre est un paramètre de stratégie de groupe BitLocker qui n’est pas disponible dans les modèles de stratégie de groupe MBAM.</span><span class="sxs-lookup"><span data-stu-id="dce31-127">This setting is a BitLocker Group Policy setting and is not available in the MBAM Group Policy Templates.</span></span>

### <span data-ttu-id="dce31-128">Le nom d’utilisateur principal est requis pour tous les comptes de service.</span><span class="sxs-lookup"><span data-stu-id="dce31-128">User principal name is required for all service accounts</span></span>

<span data-ttu-id="dce31-129">Un nom d’utilisateur principal (UPN) doit être défini pour tous les comptes de service dans MBAM.</span><span class="sxs-lookup"><span data-stu-id="dce31-129">A user principal name (UPN) must be set for all service accounts in MBAM.</span></span> <span data-ttu-id="dce31-130">Si vous ne parvenez pas à créer un UPN pour un compte, un message d’erreur s’affiche lors du processus de configuration pour indiquer que l’utilisateur ou le groupe est introuvable dans Active Directory.</span><span class="sxs-lookup"><span data-stu-id="dce31-130">If you fail to create a UPN for an account, an error message appears during the configuration process to indicate that the user or group could not be found in Active Directory.</span></span>

<span data-ttu-id="dce31-131">**Solution de contournement:** Ajoutez le nom d’utilisateur principal au compte de service.</span><span class="sxs-lookup"><span data-stu-id="dce31-131">**Workaround:** Add the UPN to the service account.</span></span>

### <span data-ttu-id="dce31-132">Le portail libre-service et le site Web d’administration et de surveillance ne s’ouvrent pas après la mise à niveau d’IIS vers .NET Framework 4,5</span><span class="sxs-lookup"><span data-stu-id="dce31-132">Self-Service Portal and the Administration and Monitoring Website do not open after you upgrade IIS to .NET Framework 4.5</span></span>

<span data-ttu-id="dce31-133">Lorsque vous mettez à niveau Internet Information Services (IIS) vers Microsoft .NET Framework 4,5, le portail libre-service et le site Web d’administration et de surveillance ne s’ouvrent pas.</span><span class="sxs-lookup"><span data-stu-id="dce31-133">When you upgrade Internet Information Services (IIS) to the Microsoft .NET Framework 4.5, the Self-Service Portal and the Administration and Monitoring Website do not open.</span></span>

<span data-ttu-id="dce31-134">**Solution de contournement:** Voir le [message d’erreur suivant l’installation de .NET Framework 4,0: «impossible de charger le type «System. ServiceModel. activation. HttpModule»](https://go.microsoft.com/fwlink/?LinkId=393568).</span><span class="sxs-lookup"><span data-stu-id="dce31-134">**Workaround:** See the article [Error message after you install the .NET Framework 4.0: "Could not load type 'System.ServiceModel.Activation.HttpModule'](https://go.microsoft.com/fwlink/?LinkId=393568).</span></span>

### <span data-ttu-id="dce31-135">Le site Web d’administration et de surveillance affiche un message d’erreur «rapport introuvable» lorsque les rapports ne sont pas configurés</span><span class="sxs-lookup"><span data-stu-id="dce31-135">Administration and Monitoring Website displays a "Report cannot be found" error message when Reports are not configured</span></span>

<span data-ttu-id="dce31-136">Si vous configurez le site Web d’administration et de surveillance et que vous essayez d’afficher un rapport sans tout d’abord configurer la fonction rapports, un message d’erreur indique que le rapport est introuvable.</span><span class="sxs-lookup"><span data-stu-id="dce31-136">If you configure the Administration and Monitoring Website and then try to view a report without configuring the Reports feature first, an error message indicates that the report cannot be found.</span></span>

<span data-ttu-id="dce31-137">**Solution de contournement:** Configurez la fonctionnalité rapports avant de configurer les applications Web.</span><span class="sxs-lookup"><span data-stu-id="dce31-137">**Workaround:** Configure the Reports feature before you configure the web applications.</span></span>

### <span data-ttu-id="dce31-138">Les rapports figurant sur le site Web d’administration et de surveillance affichent un avertissement si SSL n’est pas configuré dans SSRS</span><span class="sxs-lookup"><span data-stu-id="dce31-138">Reports in the Administration and Monitoring Website display a warning if SSL is not configured in SSRS</span></span>

<span data-ttu-id="dce31-139">Si SQL Server Reporting Services (SSRS) n’a pas été configuré pour utiliser SSL (Secure Socket Layer), l’URL de la fonctionnalité rapports sera définie sur HTTP au lieu de HTTPs lorsque vous configurez le serveur MBAM.</span><span class="sxs-lookup"><span data-stu-id="dce31-139">If SQL Server Reporting Services (SSRS) was not configured to use Secure Socket Layer (SSL), the URL for the Reports feature will be set to HTTP instead of to HTTPS when you configure the MBAM Server.</span></span> <span data-ttu-id="dce31-140">Pour ouvrir le site Web d’administration et de surveillance et sélectionner un rapport, le message d’erreur suivant s’affiche: «seul le contenu sécurisé est affiché».</span><span class="sxs-lookup"><span data-stu-id="dce31-140">If you then open the Administration and Monitoring Website and select a report, the following error message appears: "Only Secure Content is Displayed."</span></span>

<span data-ttu-id="dce31-141">**Solution de contournement:** Pour afficher l’État, cliquez sur **Afficher tout le contenu**.</span><span class="sxs-lookup"><span data-stu-id="dce31-141">**Workaround:** To show the report, click **Show All Content**.</span></span> <span data-ttu-id="dce31-142">Pour résoudre ce problème, accédez à l’MBAM ordinateur sur lequel SQL Server Reporting Services est installé, exécutez le **Gestionnaire de configuration de Reporting Services**, puis cliquez sur **URL du service Web**.</span><span class="sxs-lookup"><span data-stu-id="dce31-142">To correct this issue, go to the MBAM computer where SQL Server Reporting Services is installed, run **Reporting Services Configuration Manager**, and then click **Web Service URL**.</span></span> <span data-ttu-id="dce31-143">Sélectionnez le certificat SSL approprié pour le serveur, entrez le port SSL approprié (le port par défaut est 443), puis cliquez sur **appliquer**.</span><span class="sxs-lookup"><span data-stu-id="dce31-143">Select the appropriate SSL certificate for the server, enter the appropriate SSL port (the default port is 443), and then click **Apply**.</span></span>

### <span data-ttu-id="dce31-144">Cliquer sur «retour» dans le rapport synthèse de conformité BitLocker peut générer une erreur</span><span class="sxs-lookup"><span data-stu-id="dce31-144">Clicking "Back" in the BitLocker Compliance Summary report might throw an error</span></span>

<span data-ttu-id="dce31-145">Si vous explorez un rapport de synthèse de conformité BitLocker, puis cliquez sur le lien **retour** dans le rapport SSRS, une erreur peut être levée.</span><span class="sxs-lookup"><span data-stu-id="dce31-145">If you drill down into a BitLocker Compliance Summary report, and then click the **Back** link in the SSRS report, an error might be thrown.</span></span>

<span data-ttu-id="dce31-146">**Solution de contournement:** Néant.</span><span class="sxs-lookup"><span data-stu-id="dce31-146">**Workaround:** None.</span></span>

### <span data-ttu-id="dce31-147">Le niveau de cryptage ne s’affiche pas correctement dans le rapport de conformité de l’ordinateur BitLocker</span><span class="sxs-lookup"><span data-stu-id="dce31-147">Cipher strength displays incorrectly on the BitLocker Computer Compliance report</span></span>

<span data-ttu-id="dce31-148">Si vous ne définissez pas de niveau de chiffrement spécifique dans l’objet **choisir la méthode de chiffrement de lecteur et** la stratégie de groupe force de chiffrement, le rapport de conformité de l’ordinateur BitLocker dans le niveau d’intégration de Configuration Manager affiche toujours «inconnu» pour la puissance de chiffrement, même si la puissance de chiffrement utilise la valeur par défaut du chiffrement de 128 bits.</span><span class="sxs-lookup"><span data-stu-id="dce31-148">If you do not set a specific cipher strength in the **Choose drive encryption method and cipher strength** Group Policy Object, the BitLocker Computer Compliance report in the Configuration Manager Integration topology always displays "unknown" for the cipher strength, even when the cipher strength uses the default of 128-bit encryption.</span></span> <span data-ttu-id="dce31-149">Le rapport affiche le niveau de cryptage approprié si vous définissez un niveau de cryptage spécifique dans l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="dce31-149">The report displays the correct cipher strength if you set a specific cipher strength in the Group Policy Object.</span></span>

<span data-ttu-id="dce31-150">**Solution de contournement:** Définissez toujours une clé de chiffrement spécifique dans l’objet **choisir la méthode de chiffrement de lecteur et** l’objet de stratégie de groupe santé du chiffrement.</span><span class="sxs-lookup"><span data-stu-id="dce31-150">**Workaround:** Always set a specific cipher strength in the **Choose drive encryption method and cipher strength** Group Policy Object.</span></span>

### <span data-ttu-id="dce31-151">Distribution de l’état de conformité par type de lecteur affiche les anciennes données après la mise à jour des éléments de configuration</span><span class="sxs-lookup"><span data-stu-id="dce31-151">Compliance Status Distribution By Drive Type displays old data after you update configuration items</span></span>

<span data-ttu-id="dce31-152">Après avoir mis à jour les éléments de configuration MBAM dans SystemCenter2012 ConfigurationManager, le graphique barre de distribution de l’état de conformité par type de lecteur sur le tableau de bord de conformité de BitLocker Enterprise affiche des données basées sur des informations provenant de versions antérieures des éléments de configuration.</span><span class="sxs-lookup"><span data-stu-id="dce31-152">After you update MBAM configuration items in SystemCenter2012 ConfigurationManager, the Compliance Status Distribution By Drive Type bar chart on the BitLocker Enterprise Compliance Dashboard shows data that is based on information from old versions of the configuration items.</span></span>

<span data-ttu-id="dce31-153">**Solution de contournement:** Néant.</span><span class="sxs-lookup"><span data-stu-id="dce31-153">**Workaround:** None.</span></span> <span data-ttu-id="dce31-154">La modification des éléments de configuration MBAM n’est pas prise en charge et le rapport risque de ne pas apparaître comme prévu.</span><span class="sxs-lookup"><span data-stu-id="dce31-154">Modification of the MBAM configuration items is not supported, and the report might not appear as expected.</span></span>

### <span data-ttu-id="dce31-155">La configuration de la sécurité améliorée peut entraîner un affichage incorrect du message d’erreur</span><span class="sxs-lookup"><span data-stu-id="dce31-155">Enhanced Security Configuration might cause reports to display an error message incorrectly</span></span>

<span data-ttu-id="dce31-156">Si la configuration de sécurité améliorée d’Internet Explorer (ESC) est activée, un message d’erreur «Accès refusé» peut s’afficher lorsque vous tentez d’afficher des rapports sur le serveur MBAM.</span><span class="sxs-lookup"><span data-stu-id="dce31-156">If Internet Explorer Enhanced Security Configuration (ESC) is turned on, an "Access Denied" error message might appear when you try to view reports on the MBAM Server.</span></span> <span data-ttu-id="dce31-157">Par défaut, la fonction Échap est activée pour protéger le serveur en diminuant son exposition aux attaques potentielles qui peuvent se produire via le contenu Web et les scripts d’application.</span><span class="sxs-lookup"><span data-stu-id="dce31-157">By default, ESC is turned on to protect the server by decreasing the server’s exposure to potential attacks that can occur through web content and application scripts.</span></span>

<span data-ttu-id="dce31-158">**Solution de contournement:** Si le message d’erreur «Accès refusé» s’affiche lorsque vous essayez d’afficher des rapports sur le serveur MBAM, vous pouvez définir un objet de stratégie de groupe ou modifier manuellement la valeur par défaut de votre image pour désactiver la configuration de la sécurité améliorée.</span><span class="sxs-lookup"><span data-stu-id="dce31-158">**Workaround:** If the "Access Denied" error message appears when you try to view reports on the MBAM Server, you can set a Group Policy Object or change the default manually in your image to disable Enhanced Security Configuration.</span></span> <span data-ttu-id="dce31-159">Vous pouvez également afficher les rapports à partir d’un autre ordinateur sur lequel ESC n’est pas activé.</span><span class="sxs-lookup"><span data-stu-id="dce31-159">You can also alternatively view the reports from another computer on which ESC is not enabled.</span></span>

### <span data-ttu-id="dce31-160">Prise en charge de l’algorithme de chiffrement BitLocker XTS-AES</span><span class="sxs-lookup"><span data-stu-id="dce31-160">Support for Bitlocker XTS-AES encryption algorithm</span></span>
<span data-ttu-id="dce31-161">BitLocker a ajouté une prise en charge pour l’algorithme de chiffrement XTS-AES dans Windows 10, version 1511.</span><span class="sxs-lookup"><span data-stu-id="dce31-161">Bitlocker added support for the XTS-AES encryption algorithm in Windows 10, version 1511.</span></span> <span data-ttu-id="dce31-162">Avec HF02, MBAM a ajouté une prise en charge du client pour cette option BitLocker et dans HF04, la prise en charge côté serveur a été ajoutée.</span><span class="sxs-lookup"><span data-stu-id="dce31-162">With HF02, MBAM added client support for this Bitlocker option and in HF04, the server-side support was added.</span></span> <span data-ttu-id="dce31-163">Néanmoins, il existe une limite connue:</span><span class="sxs-lookup"><span data-stu-id="dce31-163">However, there is one known limitation:</span></span>

* <span data-ttu-id="dce31-164">Les clients doivent utiliser la même force de chiffrement pour le système d’exploitation et les volumes de données sur le même ordinateur.</span><span class="sxs-lookup"><span data-stu-id="dce31-164">Customers must use the same encryption strength for OS and data volumes on the same machine.</span></span>
<span data-ttu-id="dce31-165">Si les différents niveaux de cryptage sont utilisés, MBAM signale que l’ordinateur n’est **pas compatible**.</span><span class="sxs-lookup"><span data-stu-id="dce31-165">If different encryption strengths are used, MBAM will report the machine as **non-compliant**.</span></span>

### <span data-ttu-id="dce31-166">Le portail libre-service ajoute automatiquement «-» sur une entrée d’ID clé</span><span class="sxs-lookup"><span data-stu-id="dce31-166">Self-Service Portal automatically adds "-" on Key ID entry</span></span>
<span data-ttu-id="dce31-167">À partir de HF02, le portail libre-service MBAM ajoute automatiquement l’élément «-» à l’entrée d’ID clé.</span><span class="sxs-lookup"><span data-stu-id="dce31-167">As of HF02, the MBAM Self-Service Portal automatically adds the '-' on Key ID entry.</span></span>  
<span data-ttu-id="dce31-168">**Remarque:** Le serveur doit être reconfiguré pour que JavaScript prenne effet.</span><span class="sxs-lookup"><span data-stu-id="dce31-168">**Note:** The Server has to be reconfigured for the Javascript to take effect.</span></span>

### <span data-ttu-id="dce31-169">Les rapports MBAM 2,5 SP1 ne fonctionnent pas correctement</span><span class="sxs-lookup"><span data-stu-id="dce31-169">MBAM 2.5 Sp1 Reports does not work / render properly</span></span>
<span data-ttu-id="dce31-170">La page rapports ne s’affiche pas correctement lorsque SSRS est hébergé sur SQL Server 2016 Edition.</span><span class="sxs-lookup"><span data-stu-id="dce31-170">Reports Page does not render properly when SSRS is hosted on SQL Server 2016 edition.</span></span> 
<span data-ttu-id="dce31-171">Par exemple, pour accéder au support technique, vous pouvez cliquer sur rapports (en surbrillance avec «x» en surbrillance) en vous appuyant davantage sur 4,0 les États (en surbrillance).</span><span class="sxs-lookup"><span data-stu-id="dce31-171">For example – Browsing to Helpdesk – Clicking on Reports – ( Highlighted portion have “x” on it ) Digging this further with Fiddler – it does look like once we click on Reports – it calls the SSRS page with HTML 4.0 rendering format.</span></span>

<span data-ttu-id="dce31-172">**Solution de contournement:** En examinant le code site. Master et remarqué que le mode X-UA a été dicté par IE8.</span><span class="sxs-lookup"><span data-stu-id="dce31-172">**Workaround:** Looking at the site.master code and noticed the X-UA mode was dictated as IE8.</span></span> <span data-ttu-id="dce31-173">Comme IE8 est passé en fin de vie, et le client utilise IE11.</span><span class="sxs-lookup"><span data-stu-id="dce31-173">As IE8 is WAY past the end of life, and customer is using IE11.</span></span> <span data-ttu-id="dce31-174">Mettez à jour le paramètre vers le code ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="dce31-174">Update the setting to the below code.</span></span> <span data-ttu-id="dce31-175">Cela permet au site d’utiliser les technologies de rendu IE11</span><span class="sxs-lookup"><span data-stu-id="dce31-175">This allows the site to utilize IE11 rendering technologies</span></span>

    <meta http-equiv="X-UA-Compatible" content="IE=Edge" />

<span data-ttu-id="dce31-176">Le paramètre initial est le suivant:</span><span class="sxs-lookup"><span data-stu-id="dce31-176">Original setting is:</span></span> 

    <meta http-equiv="X-UA-Compatible" content="IE=8" />


<span data-ttu-id="dce31-177">C’est la raison pour laquelle le problème ne s’est pas produit avec d’autres navigateurs, tels que Chrome, Firefox etc.</span><span class="sxs-lookup"><span data-stu-id="dce31-177">This is the reason why the issue was not seen with other browsers like Chrome, Firefox etc.</span></span>



## <span data-ttu-id="dce31-178">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="dce31-178">Related topics</span></span>


[<span data-ttu-id="dce31-179">À propos de MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="dce31-179">About MBAM 2.5</span></span>](about-mbam-25.md)

 

## <span data-ttu-id="dce31-180">Vous avez une suggestion pour MBAM?</span><span class="sxs-lookup"><span data-stu-id="dce31-180">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="dce31-181">Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)</span><span class="sxs-lookup"><span data-stu-id="dce31-181">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="dce31-182">Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="dce31-182">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





