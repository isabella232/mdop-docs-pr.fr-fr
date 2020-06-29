---
title: Notes de publication de MBAM2.5
description: Notes de publication de MBAM2.5
author: dansimp
ms.assetid: fcaf03e6-5e39-4771-af3c-a3cd468f3961
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 4bcc17d6295b14a7f3276146d5630b869b94b7f0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810883"
---
# <span data-ttu-id="bcffe-103">Notes de publication de MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="bcffe-103">Release Notes for MBAM 2.5</span></span>


<span data-ttu-id="bcffe-104">Pour effectuer une recherche dans ces notes de publication, appuyez sur Ctrl + F.</span><span class="sxs-lookup"><span data-stu-id="bcffe-104">To search these release notes, press Ctrl+F.</span></span>

<span data-ttu-id="bcffe-105">Lisez attentivement ces notes de publication avant d’installer Microsoft BitLocker Administration and Monitoring (MBAM) 2,5.</span><span class="sxs-lookup"><span data-stu-id="bcffe-105">Read these release notes thoroughly before you install Microsoft BitLocker Administration and Monitoring (MBAM) 2.5.</span></span> <span data-ttu-id="bcffe-106">Ces notes de publication contiennent des informations nécessaires à l’installation réussie de MBAM et contiennent des informations qui ne sont pas disponibles dans la documentation du produit.</span><span class="sxs-lookup"><span data-stu-id="bcffe-106">These release notes contain information that is required to successfully install MBAM and can contain information that is not available in the product documentation.</span></span> <span data-ttu-id="bcffe-107">Si ces notes de publication diffèrent d’autres documents de la 2,5 de MBAM, envisagez d’utiliser la dernière modification pour faire autorité.</span><span class="sxs-lookup"><span data-stu-id="bcffe-107">If these release notes differ from other MBAM 2.5 documentation, consider the latest change to be authoritative.</span></span> <span data-ttu-id="bcffe-108">Ces notes de publication remplacent le contenu qui est inclus dans ce produit.</span><span class="sxs-lookup"><span data-stu-id="bcffe-108">These release notes supersede the content that is included with this product.</span></span>

## <a href="" id="---------mbam-2-5-known-issues"></a> <span data-ttu-id="bcffe-109">Problèmes connus de MBAM 2,5</span><span class="sxs-lookup"><span data-stu-id="bcffe-109">MBAM 2.5 known issues</span></span>


<span data-ttu-id="bcffe-110">Cette section contient des notes de publication pour MBAM 2,5.</span><span class="sxs-lookup"><span data-stu-id="bcffe-110">This section contains release notes for MBAM 2.5.</span></span>

### <span data-ttu-id="bcffe-111">Navigateur Web exécuté involontairement en tant qu’administrateur</span><span class="sxs-lookup"><span data-stu-id="bcffe-111">Web browser unintentionally run as administrator</span></span>

<span data-ttu-id="bcffe-112">Les liens d’aide de l’outil de configuration de MBAM Server peuvent entraîner l’ouverture des fenêtres de navigateur avec des droits d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="bcffe-112">Help links in the MBAM Server Configuration tool can cause browser windows to open with administrator rights.</span></span>

<span data-ttu-id="bcffe-113">**Solution de contournement:** Activez la configuration de la sécurité améliorée d’Internet Explorer (IESC) ou fermez votre navigateur Web pour accéder à d’autres sites.</span><span class="sxs-lookup"><span data-stu-id="bcffe-113">**Workaround:** Enable Internet Explorer Enhanced Security Configuration (IESC) or close your web browser before navigating to other sites.</span></span>

<span data-ttu-id="bcffe-114">**Remarques**  Ce problème a été résolu dans MBAM 2,5 SP1.</span><span class="sxs-lookup"><span data-stu-id="bcffe-114">**Note** This is fixed in MBAM 2.5 SP1.</span></span>

 

### <a href="" id="-------------mbam-reports-as-noncompliant-a-client-encrypted-with-aes-256-bit-encryption-keys-and-diffuser"></a> <span data-ttu-id="bcffe-115">256 MBAM-xxx XXXXXXX XXXXXXX xxxx xxx XXXXXXX XXXXXXX XXXXXXX XXXXXXX XXXXXXX XXXXXXX</span><span class="sxs-lookup"><span data-stu-id="bcffe-115">MBAM reports as noncompliant a client encrypted with AES 256-bit encryption keys and Diffuser</span></span>

<span data-ttu-id="bcffe-116">Si le client MBAM 2,5 est installé et est chiffré à l’aide du système AES 256-bit avec la puissance de chiffrement du diffuseur, le client MBAM est signalé comme non conforme dans les rapports de conformité MBAM.</span><span class="sxs-lookup"><span data-stu-id="bcffe-116">If a computer has the MBAM 2.5 client installed and is encrypted by using the AES 256-bit with Diffuser cipher strength, the MBAM client is reported as noncompliant in the MBAM compliance reports.</span></span>

<span data-ttu-id="bcffe-117">**Solution de contournement:** Installez le correctif sur [KB2975636](https://go.microsoft.com/fwlink/?LinkId=511972).</span><span class="sxs-lookup"><span data-stu-id="bcffe-117">**Workaround:** Install the hotfix at [KB2975636](https://go.microsoft.com/fwlink/?LinkId=511972).</span></span>

### <a href="" id="-------------mbam-fails-to-encrypt-a-volume-and-reports-an-error-if-you-set-a-tpm---pin-protector-on-a-tablet-device"></a> <span data-ttu-id="bcffe-118">MBAM ne parvient pas à chiffrer un volume et signale une erreur si vous avez configuré un module de protection TPM + PIN sur un appareil de tablette</span><span class="sxs-lookup"><span data-stu-id="bcffe-118">MBAM fails to encrypt a volume and reports an error if you set a TPM + PIN protector on a tablet device</span></span>

<span data-ttu-id="bcffe-119">Si les utilisateurs finaux essaient de définir un protecteur de plateforme sécurisée + code confidentiel sur un appareil de tablette, MBAM ne peut pas être chiffré et signale une erreur.</span><span class="sxs-lookup"><span data-stu-id="bcffe-119">If end users try to set a TPM + PIN protector on a tablet device, MBAM fails to encrypt, and it reports an error.</span></span> <span data-ttu-id="bcffe-120">Ce problème survient parce que les appareils tablettes n’ont pas de clavier d’environnement de pré-démarrage.</span><span class="sxs-lookup"><span data-stu-id="bcffe-120">This issue occurs because tablet devices do not have a pre-boot environment keyboard.</span></span>

<span data-ttu-id="bcffe-121">**Solution de contournement:** Activez l’option **activer l’authentification BitLocker nécessitant une entrée au clavier prédémarrage sur des tablettes** .</span><span class="sxs-lookup"><span data-stu-id="bcffe-121">**Workaround:** Enable the **Enable use of BitLocker authentication requiring preboot keyboard input on tablets** Group Policy setting.</span></span> <span data-ttu-id="bcffe-122">Ce paramètre est un paramètre de stratégie de groupe BitLocker qui n’est pas disponible dans les modèles de stratégie de groupe MBAM.</span><span class="sxs-lookup"><span data-stu-id="bcffe-122">This setting is a BitLocker Group Policy setting and is not available in the MBAM Group Policy Templates.</span></span>

### <span data-ttu-id="bcffe-123">Le nom d’utilisateur principal est requis pour tous les comptes de service.</span><span class="sxs-lookup"><span data-stu-id="bcffe-123">User principal name is required for all service accounts</span></span>

<span data-ttu-id="bcffe-124">Un nom d’utilisateur principal (UPN) doit être défini pour tous les comptes de service dans MBAM.</span><span class="sxs-lookup"><span data-stu-id="bcffe-124">A user principal name (UPN) must be set for all service accounts in MBAM.</span></span> <span data-ttu-id="bcffe-125">Si vous ne parvenez pas à créer un UPN pour un compte, un message d’erreur s’affiche lors du processus de configuration pour indiquer que l’utilisateur ou le groupe est introuvable dans Active Directory.</span><span class="sxs-lookup"><span data-stu-id="bcffe-125">If you fail to create a UPN for an account, an error message appears during the configuration process to indicate that the user or group could not be found in Active Directory.</span></span>

<span data-ttu-id="bcffe-126">**Solution de contournement:** Ajoutez le nom d’utilisateur principal au compte de service.</span><span class="sxs-lookup"><span data-stu-id="bcffe-126">**Workaround:** Add the UPN to the service account.</span></span>

### <span data-ttu-id="bcffe-127">Le portail libre-service nécessite une configuration supplémentaire si les ordinateurs clients ne peuvent pas accéder au réseau de distribution de contenu de Microsoft Ajax</span><span class="sxs-lookup"><span data-stu-id="bcffe-127">Self-Service Portal requires additional configuration if client computers cannot access Microsoft Ajax Content Delivery Network</span></span>

<span data-ttu-id="bcffe-128">Si vos ordinateurs clients n’ont pas accès au réseau de distribution de contenu (CDN) Microsoft Ajax, ce qui donne au portail libre-service l’accès qu’il nécessite pour certains fichiers JavaScript, vous devez configurer le portail libre-service pour qu’il référence les fichiers JavaScript à partir d’une source accessible.</span><span class="sxs-lookup"><span data-stu-id="bcffe-128">If your client computers do not have access to the Microsoft Ajax Content Delivery Network (CDN), which gives the Self-Service Portal the access that it requires to certain JavaScript files, you must configure the Self-Service Portal to reference the JavaScript files from an accessible source.</span></span> <span data-ttu-id="bcffe-129">Si vous ne configurez pas le portail libre-service lorsque les ordinateurs clients ne peuvent pas accéder au CDN, seul le nom de la société et le compte sous lequel vous vous êtes connecté est affiché.</span><span class="sxs-lookup"><span data-stu-id="bcffe-129">If you don’t configure the Self-Service Portal when client computers cannot access CDN, only the company name and the account under which you logged on is displayed.</span></span> <span data-ttu-id="bcffe-130">Aucun message d’erreur ne s’affiche.</span><span class="sxs-lookup"><span data-stu-id="bcffe-130">No error message appears.</span></span>

<span data-ttu-id="bcffe-131">**Solution de contournement:** Installez MBAM 2,5 SP1.</span><span class="sxs-lookup"><span data-stu-id="bcffe-131">**Workaround:** Install MBAM 2.5 SP1.</span></span> <span data-ttu-id="bcffe-132">vous pouvez configurer le portail libre-service en suivant ces instructions: [Comment configurer le portail libre-service lorsque les ordinateurs clients ne peuvent pas accéder au réseau de distribution de contenu Microsoft](how-to-configure-the-self-service-portal-when-client-computers-cannot-access-the-microsoft-content-delivery-network.md).</span><span class="sxs-lookup"><span data-stu-id="bcffe-132">or configure the Self-Service Portal by following these instructions: [How to Configure the Self-Service Portal When Client Computers Cannot Access the Microsoft Content Delivery Network](how-to-configure-the-self-service-portal-when-client-computers-cannot-access-the-microsoft-content-delivery-network.md).</span></span>

### <span data-ttu-id="bcffe-133">Le portail libre-service et le site Web d’administration et de surveillance ne s’ouvrent pas après la mise à niveau d’IIS vers .NET Framework 4,5</span><span class="sxs-lookup"><span data-stu-id="bcffe-133">Self-Service Portal and the Administration and Monitoring Website do not open after you upgrade IIS to .NET Framework 4.5</span></span>

<span data-ttu-id="bcffe-134">Lorsque vous mettez à niveau Internet Information Services (IIS) vers Microsoft .NET Framework 4,5, le portail libre-service et le site Web d’administration et de surveillance ne s’ouvrent pas.</span><span class="sxs-lookup"><span data-stu-id="bcffe-134">When you upgrade Internet Information Services (IIS) to the Microsoft .NET Framework 4.5, the Self-Service Portal and the Administration and Monitoring Website do not open.</span></span>

<span data-ttu-id="bcffe-135">**Solution de contournement:** Voir le [message d’erreur suivant l’installation de .NET Framework 4,0: «impossible de charger le type «System. ServiceModel. activation. HttpModule»](https://go.microsoft.com/fwlink/?LinkId=393568).</span><span class="sxs-lookup"><span data-stu-id="bcffe-135">**Workaround:** See the article [Error message after you install the .NET Framework 4.0: "Could not load type 'System.ServiceModel.Activation.HttpModule'](https://go.microsoft.com/fwlink/?LinkId=393568).</span></span>

### <span data-ttu-id="bcffe-136">Le site Web d’administration et de surveillance affiche un message d’erreur «rapport introuvable» lorsque les rapports ne sont pas configurés</span><span class="sxs-lookup"><span data-stu-id="bcffe-136">Administration and Monitoring Website displays a "Report cannot be found" error message when Reports are not configured</span></span>

<span data-ttu-id="bcffe-137">Si vous configurez le site Web d’administration et de surveillance et que vous essayez d’afficher un rapport sans tout d’abord configurer la fonction rapports, un message d’erreur indique que le rapport est introuvable.</span><span class="sxs-lookup"><span data-stu-id="bcffe-137">If you configure the Administration and Monitoring Website and then try to view a report without configuring the Reports feature first, an error message indicates that the report cannot be found.</span></span>

<span data-ttu-id="bcffe-138">**Solution de contournement:** Configurez la fonctionnalité rapports avant de configurer les applications Web.</span><span class="sxs-lookup"><span data-stu-id="bcffe-138">**Workaround:** Configure the Reports feature before you configure the web applications.</span></span>

### <span data-ttu-id="bcffe-139">Les rapports figurant sur le site Web d’administration et de surveillance affichent un avertissement si SSL n’est pas configuré dans SSRS</span><span class="sxs-lookup"><span data-stu-id="bcffe-139">Reports in the Administration and Monitoring Website display a warning if SSL is not configured in SSRS</span></span>

<span data-ttu-id="bcffe-140">Si SQL Server Reporting Services (SSRS) n’a pas été configuré pour utiliser SSL (Secure Socket Layer), l’URL de la fonctionnalité rapports sera définie sur HTTP au lieu de HTTPs lorsque vous configurez le serveur MBAM.</span><span class="sxs-lookup"><span data-stu-id="bcffe-140">If SQL Server Reporting Services (SSRS) was not configured to use Secure Socket Layer (SSL), the URL for the Reports feature will be set to HTTP instead of to HTTPS when you configure the MBAM Server.</span></span> <span data-ttu-id="bcffe-141">Pour ouvrir le site Web d’administration et de surveillance et sélectionner un rapport, le message d’erreur suivant s’affiche: «seul le contenu sécurisé est affiché».</span><span class="sxs-lookup"><span data-stu-id="bcffe-141">If you then open the Administration and Monitoring Website and select a report, the following error message appears: "Only Secure Content is Displayed."</span></span>

<span data-ttu-id="bcffe-142">**Solution de contournement:** Pour afficher l’État, cliquez sur **Afficher tout le contenu**.</span><span class="sxs-lookup"><span data-stu-id="bcffe-142">**Workaround:** To show the report, click **Show All Content**.</span></span> <span data-ttu-id="bcffe-143">Pour résoudre ce problème, accédez à l’MBAM ordinateur sur lequel SQL Server Reporting Services est installé, exécutez le **Gestionnaire de configuration de Reporting Services**, puis cliquez sur **URL du service Web**.</span><span class="sxs-lookup"><span data-stu-id="bcffe-143">To correct this issue, go to the MBAM computer where SQL Server Reporting Services is installed, run **Reporting Services Configuration Manager**, and then click **Web Service URL**.</span></span> <span data-ttu-id="bcffe-144">Sélectionnez le certificat SSL approprié pour le serveur, entrez le port SSL approprié (le port par défaut est 443), puis cliquez sur **appliquer**.</span><span class="sxs-lookup"><span data-stu-id="bcffe-144">Select the appropriate SSL certificate for the server, enter the appropriate SSL port (the default port is 443), and then click **Apply**.</span></span>

### <span data-ttu-id="bcffe-145">Cliquer sur «retour» dans le rapport synthèse de conformité BitLocker peut générer une erreur</span><span class="sxs-lookup"><span data-stu-id="bcffe-145">Clicking "Back" in the BitLocker Compliance Summary report might throw an error</span></span>

<span data-ttu-id="bcffe-146">Si vous explorez un rapport de synthèse de conformité BitLocker, puis cliquez sur le lien **retour** dans le rapport SSRS, une erreur peut être levée.</span><span class="sxs-lookup"><span data-stu-id="bcffe-146">If you drill down into a BitLocker Compliance Summary report, and then click the **Back** link in the SSRS report, an error might be thrown.</span></span>

<span data-ttu-id="bcffe-147">**Solution de contournement:** Néant.</span><span class="sxs-lookup"><span data-stu-id="bcffe-147">**Workaround:** None.</span></span>

### <span data-ttu-id="bcffe-148">Le chiffrement de l’espace utilisé uniquement ne fonctionne pas correctement</span><span class="sxs-lookup"><span data-stu-id="bcffe-148">Used Space Only Encryption does not work correctly</span></span>

<span data-ttu-id="bcffe-149">Si vous chiffrez un ordinateur pour la première fois après avoir installé le client MBAM, et que vous avez configuré un paramètre de stratégie de groupe pour implémenter le chiffrement de l’espace utilisé uniquement, MBAM chiffre par erreur le disque entier au lieu de chiffrer uniquement l’espace utilisé du disque.</span><span class="sxs-lookup"><span data-stu-id="bcffe-149">If you encrypt a computer for the first time after you install the MBAM Client, and you have configured a Group Policy setting to implement Used Space Only encryption, MBAM erroneously encrypts the entire disk instead of encrypting only the disk’s used space.</span></span> <span data-ttu-id="bcffe-150">Si un ordinateur est déjà chiffré avec l’espace utilisé uniquement lors de l’installation du client MBAM et si vous avez configuré le même paramètre de stratégie de groupe, MBAM indique que le lecteur est correctement crypté et qu’il n’essaye pas de le chiffrer à nouveau.</span><span class="sxs-lookup"><span data-stu-id="bcffe-150">If a computer is already encrypted with Used Space Only when you install the MBAM Client, and you have configured the same Group Policy setting, MBAM reports that the drive is encrypted correctly, and does not try to re-encrypt the drive.</span></span>

<span data-ttu-id="bcffe-151">**Solution de contournement:** Néant.</span><span class="sxs-lookup"><span data-stu-id="bcffe-151">**Workaround:** None.</span></span>

### <span data-ttu-id="bcffe-152">Le niveau de cryptage ne s’affiche pas correctement dans le rapport de conformité de l’ordinateur BitLocker</span><span class="sxs-lookup"><span data-stu-id="bcffe-152">Cipher strength displays incorrectly on the BitLocker Computer Compliance report</span></span>

<span data-ttu-id="bcffe-153">Si vous ne définissez pas de niveau de chiffrement spécifique dans l’objet **choisir la méthode de chiffrement de lecteur et** la stratégie de groupe force de chiffrement, le rapport de conformité de l’ordinateur BitLocker dans le niveau d’intégration de Configuration Manager affiche toujours «inconnu» pour la puissance de chiffrement, même si la puissance de chiffrement utilise la valeur par défaut du chiffrement de 128 bits.</span><span class="sxs-lookup"><span data-stu-id="bcffe-153">If you do not set a specific cipher strength in the **Choose drive encryption method and cipher strength** Group Policy Object, the BitLocker Computer Compliance report in the Configuration Manager Integration topology always displays "unknown" for the cipher strength, even when the cipher strength uses the default of 128-bit encryption.</span></span> <span data-ttu-id="bcffe-154">Le rapport affiche le niveau de cryptage approprié si vous définissez un niveau de cryptage spécifique dans l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="bcffe-154">The report displays the correct cipher strength if you set a specific cipher strength in the Group Policy Object.</span></span>

<span data-ttu-id="bcffe-155">**Solution de contournement:** Définissez toujours une clé de chiffrement spécifique dans l’objet **choisir la méthode de chiffrement de lecteur et** l’objet de stratégie de groupe santé du chiffrement.</span><span class="sxs-lookup"><span data-stu-id="bcffe-155">**Workaround:** Always set a specific cipher strength in the **Choose drive encryption method and cipher strength** Group Policy Object.</span></span>

### <span data-ttu-id="bcffe-156">Distribution de l’état de conformité par type de lecteur affiche les anciennes données après la mise à jour des éléments de configuration</span><span class="sxs-lookup"><span data-stu-id="bcffe-156">Compliance Status Distribution by Drive Type displays old data after you update configuration items</span></span>

<span data-ttu-id="bcffe-157">Après avoir mis à jour les éléments de configuration MBAM dans SystemCenter2012 ConfigurationManager, le graphique barre de distribution de l’état de conformité par type de lecteur sur le tableau de bord de conformité de BitLocker Enterprise affiche des données basées sur des informations provenant de versions antérieures des éléments de configuration.</span><span class="sxs-lookup"><span data-stu-id="bcffe-157">After you update MBAM configuration items in SystemCenter2012 ConfigurationManager, the Compliance Status Distribution By Drive Type bar chart on the BitLocker Enterprise Compliance Dashboard shows data that is based on information from old versions of the configuration items.</span></span>

<span data-ttu-id="bcffe-158">**Solution de contournement:** Néant.</span><span class="sxs-lookup"><span data-stu-id="bcffe-158">**Workaround:** None.</span></span> <span data-ttu-id="bcffe-159">La modification des éléments de configuration MBAM n’est pas prise en charge et le rapport risque de ne pas apparaître comme prévu.</span><span class="sxs-lookup"><span data-stu-id="bcffe-159">Modification of the MBAM configuration items is not supported, and the report might not appear as expected.</span></span>

### <span data-ttu-id="bcffe-160">La configuration de la sécurité améliorée peut entraîner un affichage incorrect du message d’erreur</span><span class="sxs-lookup"><span data-stu-id="bcffe-160">Enhanced Security Configuration might cause reports to display an error message incorrectly</span></span>

<span data-ttu-id="bcffe-161">Si la configuration de sécurité améliorée d’Internet Explorer (ESC) est activée, un message d’erreur «Accès refusé» peut s’afficher lorsque vous tentez d’afficher des rapports sur le serveur MBAM.</span><span class="sxs-lookup"><span data-stu-id="bcffe-161">If Internet Explorer Enhanced Security Configuration (ESC) is turned on, an "Access Denied" error message might appear when you try to view reports on the MBAM Server.</span></span> <span data-ttu-id="bcffe-162">Par défaut, la fonction Échap est activée pour protéger le serveur en diminuant son exposition aux attaques potentielles qui peuvent se produire via le contenu Web et les scripts d’application.</span><span class="sxs-lookup"><span data-stu-id="bcffe-162">By default, ESC is turned on to protect the server by decreasing the server’s exposure to potential attacks that can occur through web content and application scripts.</span></span>

<span data-ttu-id="bcffe-163">**Solution de contournement:** Si le message d’erreur «Accès refusé» s’affiche lorsque vous essayez d’afficher des rapports sur le serveur MBAM, vous pouvez définir un objet de stratégie de groupe ou modifier manuellement la valeur par défaut de votre image pour désactiver la configuration de la sécurité améliorée.</span><span class="sxs-lookup"><span data-stu-id="bcffe-163">**Workaround:** If the "Access Denied" error message appears when you try to view reports on the MBAM Server, you can set a Group Policy Object or change the default manually in your image to disable Enhanced Security Configuration.</span></span> <span data-ttu-id="bcffe-164">Vous pouvez également afficher les rapports à partir d’un autre ordinateur sur lequel ESC n’est pas activé.</span><span class="sxs-lookup"><span data-stu-id="bcffe-164">You can also alternatively view the reports from another computer on which ESC is not enabled.</span></span>

## <a href="" id="hotfixes-and-knowledge-base-articles-for-mbam-2-5-"></a><span data-ttu-id="bcffe-165">Articles sur les correctifs et les Articles de la base de connaissances pour MBAM 2,5</span><span class="sxs-lookup"><span data-stu-id="bcffe-165">Hotfixes and Knowledge Base articles for MBAM 2.5</span></span>


<span data-ttu-id="bcffe-166">Le tableau suivant répertorie les articles sur les correctifs et les Articles de la base de connaissances pour MBAM 2,5.</span><span class="sxs-lookup"><span data-stu-id="bcffe-166">This table lists the hotfixes and KB articles for MBAM 2.5.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="bcffe-167">Article de la base de connaissances</span><span class="sxs-lookup"><span data-stu-id="bcffe-167">KB Article</span></span></strong></th>
<th align="left"><span data-ttu-id="bcffe-168">Title</span><span class="sxs-lookup"><span data-stu-id="bcffe-168">Title</span></span></th>
<th align="left"><strong><span data-ttu-id="bcffe-169">Link</span><span class="sxs-lookup"><span data-stu-id="bcffe-169">Link</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bcffe-170">2975636</span><span class="sxs-lookup"><span data-stu-id="bcffe-170">2975636</span></span></p></td>
<td align="left"><p><span data-ttu-id="bcffe-171">Correctif logiciel 1 pour l’administration et le contrôle de 2,5 de Microsoft BitLocker</span><span class="sxs-lookup"><span data-stu-id="bcffe-171">Hotfix Package 1 for Microsoft BitLocker Administration and Monitoring 2.5</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2975636/EN-US" data-raw-source="[support.microsoft.com/kb/2975636/EN-US](https://support.microsoft.com/kb/2975636/EN-US)"><span data-ttu-id="bcffe-172">support.microsoft.com/kb/2975636/EN-US</span><span class="sxs-lookup"><span data-stu-id="bcffe-172">support.microsoft.com/kb/2975636/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bcffe-173">3015477</span><span class="sxs-lookup"><span data-stu-id="bcffe-173">3015477</span></span></p></td>
<td align="left"><p><span data-ttu-id="bcffe-174">Package Hotfix 2 pour l’administration et l’analyse de BitLocker 2,5</span><span class="sxs-lookup"><span data-stu-id="bcffe-174">Hotfix Package 2 for BitLocker Administration and Monitoring 2.5</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/3015477" data-raw-source="[support.microsoft.com/kb/3015477](https://support.microsoft.com/kb/3015477)"><span data-ttu-id="bcffe-175">support.microsoft.com/kb/3015477</span><span class="sxs-lookup"><span data-stu-id="bcffe-175">support.microsoft.com/kb/3015477</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bcffe-176">3011022</span><span class="sxs-lookup"><span data-stu-id="bcffe-176">3011022</span></span></p></td>
<td align="left"><p><span data-ttu-id="bcffe-177">Échec de la création de rapports de l’installation d' 2,5 ou du gestionnaire de configuration MBAM si le nom de l’instance SSRS contient un trait de soulignement</span><span class="sxs-lookup"><span data-stu-id="bcffe-177">MBAM 2.5 installation or Configuration Manager reporting fails if the name of SSRS instance contains an underscore</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/3011022/EN-US" data-raw-source="[support.microsoft.com/kb/3011022/EN-US](https://support.microsoft.com/kb/3011022/EN-US)"><span data-ttu-id="bcffe-178">support.microsoft.com/kb/3011022/EN-US</span><span class="sxs-lookup"><span data-stu-id="bcffe-178">support.microsoft.com/kb/3011022/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bcffe-179">2756402</span><span class="sxs-lookup"><span data-stu-id="bcffe-179">2756402</span></span></p></td>
<td align="left"><p><span data-ttu-id="bcffe-180">Le client MBAM échoue avec l’ID d’événement 4 et le code d’erreur 0x8004100E dans la description de l’événement.</span><span class="sxs-lookup"><span data-stu-id="bcffe-180">MBAM client would fail with Event ID 4 and error code 0x8004100E in the Event description</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2756402/EN-US" data-raw-source="[support.microsoft.com/kb/2756402/EN-US](https://support.microsoft.com/kb/2756402/EN-US)"><span data-ttu-id="bcffe-181">support.microsoft.com/kb/2756402/EN-US</span><span class="sxs-lookup"><span data-stu-id="bcffe-181">support.microsoft.com/kb/2756402/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bcffe-182">2639518</span><span class="sxs-lookup"><span data-stu-id="bcffe-182">2639518</span></span></p></td>
<td align="left"><p><span data-ttu-id="bcffe-183">Erreur lors de l’ouverture des rapports de conformité entreprise ou ordinateur dans MBAM</span><span class="sxs-lookup"><span data-stu-id="bcffe-183">Error opening Enterprise or Computer Compliance Reports in MBAM</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2639518/EN-US" data-raw-source="[support.microsoft.com/kb/2639518/EN-US](https://support.microsoft.com/kb/2639518/EN-US)"><span data-ttu-id="bcffe-184">support.microsoft.com/kb/2639518/EN-US</span><span class="sxs-lookup"><span data-stu-id="bcffe-184">support.microsoft.com/kb/2639518/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bcffe-185">2870842</span><span class="sxs-lookup"><span data-stu-id="bcffe-185">2870842</span></span></p></td>
<td align="left"><p><span data-ttu-id="bcffe-186">Échec de l’installation de MBAM 2,0 lors du scénario d’intégration de Configuration Manager avec SQL Server 2008</span><span class="sxs-lookup"><span data-stu-id="bcffe-186">MBAM 2.0 Setup fails during Configuration Manager Integration Scenario with SQL Server 2008</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870842/EN-US" data-raw-source="[support.microsoft.com/kb/2870842/EN-US](https://support.microsoft.com/kb/2870842/EN-US)"><span data-ttu-id="bcffe-187">support.microsoft.com/kb/2870842/EN-US</span><span class="sxs-lookup"><span data-stu-id="bcffe-187">support.microsoft.com/kb/2870842/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bcffe-188">2975472</span><span class="sxs-lookup"><span data-stu-id="bcffe-188">2975472</span></span></p></td>
<td align="left"><p><span data-ttu-id="bcffe-189">Interblocages SQL lorsque de nombreux clients MBAM se connectent à la base de données de récupération MBAM</span><span class="sxs-lookup"><span data-stu-id="bcffe-189">SQL deadlocks when many MBAM clients connect to the MBAM recovery database</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2975472/EN-US" data-raw-source="[support.microsoft.com/kb/2975472/EN-US](https://support.microsoft.com/kb/2975472/EN-US)"><span data-ttu-id="bcffe-190">support.microsoft.com/kb/2975472/EN-US</span><span class="sxs-lookup"><span data-stu-id="bcffe-190">support.microsoft.com/kb/2975472/EN-US</span></span></a></p></td>
</tr>
</tbody>
</table>

 


## <span data-ttu-id="bcffe-191">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bcffe-191">Related topics</span></span>


[<span data-ttu-id="bcffe-192">À propos de MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="bcffe-192">About MBAM 2.5</span></span>](about-mbam-25.md)

 

## <span data-ttu-id="bcffe-193">Vous avez une suggestion pour MBAM?</span><span class="sxs-lookup"><span data-stu-id="bcffe-193">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="bcffe-194">Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)</span><span class="sxs-lookup"><span data-stu-id="bcffe-194">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span>
- <span data-ttu-id="bcffe-195">Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="bcffe-195">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





