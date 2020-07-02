---
title: Guide de l’administrateur des outils de diagnostics et de récupération
description: Guide de l’administrateur des outils de diagnostics et de récupération
author: dansimp
ms.assetid: 33685dd7-844f-4864-b504-3ef384ef01de
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 10/03/2017
ms.openlocfilehash: c4f4e7cb49b89759acc4c3c738ff74a4a197b120
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10795528"
---
# <span data-ttu-id="038c3-103">Guide de l’administrateur des outils de diagnostics et de récupération</span><span class="sxs-lookup"><span data-stu-id="038c3-103">Diagnostics and Recovery Toolset 8 Administrator's Guide</span></span>


<span data-ttu-id="038c3-104">Microsoft Diagnostics and Recovery Tools (DaRT) 8,0 vous permet de diagnostiquer et réparer un ordinateur qui ne peut pas être démarré ou qui a des problèmes de démarrage.</span><span class="sxs-lookup"><span data-stu-id="038c3-104">Microsoft Diagnostics and Recovery Toolset (DaRT) 8.0 lets you diagnose and repair a computer that cannot be started or that has problems starting as expected.</span></span> <span data-ttu-id="038c3-105">À l’aide de la 8,0 DaRT, vous pouvez récupérer les ordinateurs des utilisateurs finaux qui sont devenus inutilisables, diagnostiquer les causes probables des problèmes et réparer rapidement les ordinateurs non démarrés ou verrouillés.</span><span class="sxs-lookup"><span data-stu-id="038c3-105">By using DaRT 8.0, you can recover end-user computers that have become unusable, diagnose probable causes of issues, and quickly repair unbootable or locked-out computers.</span></span> <span data-ttu-id="038c3-106">Le cas échéant, vous pouvez également restaurer rapidement des fichiers perdus importants et détecter et supprimer les programmes malveillants, même lorsque l’ordinateur n’est pas connecté.</span><span class="sxs-lookup"><span data-stu-id="038c3-106">When it is necessary, you can also quickly restore important lost files and detect and remove malware, even when the computer is not online.</span></span>

<span data-ttu-id="038c3-107">Le DaRT 8,0 vous permet de créer une image de récupération DaRT dans les formats de fichier ISO (International Organization for Standardization) et d’imagerie Windows (WIM) et de graver l’image sur un CD, un DVD ou un lecteur USB.</span><span class="sxs-lookup"><span data-stu-id="038c3-107">DaRT 8.0 lets you create a DaRT recovery image in International Organization for Standardization (ISO) and Windows Imaging (WIM) file formats and burn the image to a CD, DVD, or USB.</span></span> <span data-ttu-id="038c3-108">Vous pouvez ensuite utiliser les fichiers image de récupération et les déployer localement ou sur une partition distante ou une partition de récupération.</span><span class="sxs-lookup"><span data-stu-id="038c3-108">You can then use the recovery image files and deploy them locally or to a remote partition or a recovery partition.</span></span>

<span data-ttu-id="038c3-109">Le DaRT 8,0 est une partie importante du pack d’optimisation de bureau de Microsoft (MDOP), une solution dynamique disponible pour les clients de la Software Assurance, qui permet de réduire les coûts d’installation de logiciels, de garantir la fourniture de services et de gérer et de contrôler les environnements de bureau d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="038c3-109">DaRT 8.0 is an important part of the Microsoft Desktop Optimization Pack (MDOP), a dynamic solution available to Software Assurance customers that helps reduce software installation costs, enables delivery of applications as services, and helps manage and control enterprise desktop environments.</span></span>

<a href="" id="getting-started-with-dart-8-0"></a>[<span data-ttu-id="038c3-110">Prise en main de DaRT8.0</span><span class="sxs-lookup"><span data-stu-id="038c3-110">Getting Started with DaRT 8.0</span></span>](getting-started-with-dart-80-dart-8.md)  

<span data-ttu-id="038c3-111">[À propos de DaRT 8,0](about-dart-80-dart-8.md) **|** [Notes de publication pour DaRT 8,0](release-notes-for-dart-80--dart-8.md) **|** [À propos de DaRT 8,0 SP1](about-dart-80-sp1.md) **|** [Notes de publication pour DaRT 8,0 SP1](release-notes-for-dart-80-sp1.md) **|** [À propos de DaRT 8,1](about-dart-81.md) **|** [Notes de publication pour DaRT 8,1](release-notes-for-dart-81.md) **|** [Vue d’ensemble des outils dans DaRT 8,0](overview-of-the-tools-in-dart-80-dart-8.md) **|** [Accessibilité pour les 8,0 DART](accessibility-for-dart-80-dart-8.md)</span><span class="sxs-lookup"><span data-stu-id="038c3-111">[About DaRT 8.0](about-dart-80-dart-8.md)**|**[Release Notes for DaRT 8.0](release-notes-for-dart-80--dart-8.md)**|**[About DaRT 8.0 SP1](about-dart-80-sp1.md)**|**[Release Notes for DaRT 8.0 SP1](release-notes-for-dart-80-sp1.md)**|**[About DaRT 8.1](about-dart-81.md)**|**[Release Notes for DaRT 8.1](release-notes-for-dart-81.md)**|**[Overview of the Tools in DaRT 8.0](overview-of-the-tools-in-dart-80-dart-8.md)**|**[Accessibility for DaRT 8.0](accessibility-for-dart-80-dart-8.md)</span></span>

<a href="" id="planning-for-dart-8-0"></a>[<span data-ttu-id="038c3-112">Planification de DaRT8.0</span><span class="sxs-lookup"><span data-stu-id="038c3-112">Planning for DaRT 8.0</span></span>](planning-for-dart-80-dart-8.md)  

<span data-ttu-id="038c3-113">[Planification du déploiement de DaRT 8,0](planning-to-deploy-dart-80-dart-8.md) **|** Configurations DART 8,0 [prises en charge](dart-80-supported-configurations-dart-8.md) **|** [Planification de la création de l’image de récupération 8,0 de DART](planning-to-create-the-dart-80-recovery-image-dart-8.md) **|** [Planification de l’enregistrement et du déploiement de l’image](planning-how-to-save-and-deploy-the-dart-80-recovery-image-dart-8.md) **|** de récupération 8,0 de DART [Liste de contrôle de planification DaRT 8,0](dart-80-planning-checklist-dart-8.md)</span><span class="sxs-lookup"><span data-stu-id="038c3-113">[Planning to Deploy DaRT 8.0](planning-to-deploy-dart-80-dart-8.md)**|**[DaRT 8.0 Supported Configurations](dart-80-supported-configurations-dart-8.md)**|**[Planning to Create the DaRT 8.0 Recovery Image](planning-to-create-the-dart-80-recovery-image-dart-8.md)**|**[Planning How to Save and Deploy the DaRT 8.0 Recovery Image](planning-how-to-save-and-deploy-the-dart-80-recovery-image-dart-8.md)**|**[DaRT 8.0 Planning Checklist](dart-80-planning-checklist-dart-8.md)</span></span>

<a href="" id="deploying-dart-8-0"></a>[<span data-ttu-id="038c3-114">Déploiement de DaRT8.0</span><span class="sxs-lookup"><span data-stu-id="038c3-114">Deploying DaRT 8.0</span></span>](deploying-dart-80-dart-8.md)  

<span data-ttu-id="038c3-115">[Déploiement de DaRT 8,0 sur des ordinateurs](deploying-dart-80-to-administrator-computers-dart-8.md) **|** d’administration [Création de l’image de récupération 8,0 de DART](creating-the-dart-80-recovery-image-dart-8.md) **|** [Déploiement de l’image](deploying-the-dart-recovery-image-dart-8.md) **|** de récupération DART [Liste de vérification de déploiement de DaRT 8,0](dart-80-deployment-checklist-dart-8.md)</span><span class="sxs-lookup"><span data-stu-id="038c3-115">[Deploying DaRT 8.0 to Administrator Computers](deploying-dart-80-to-administrator-computers-dart-8.md)**|**[Creating the DaRT 8.0 Recovery Image](creating-the-dart-80-recovery-image-dart-8.md)**|**[Deploying the DaRT Recovery Image](deploying-the-dart-recovery-image-dart-8.md)**|**[DaRT 8.0 Deployment Checklist](dart-80-deployment-checklist-dart-8.md)</span></span>

<a href="" id="operations-for-dart-8-0"></a>[<span data-ttu-id="038c3-116">Opérations de DaRT8.0</span><span class="sxs-lookup"><span data-stu-id="038c3-116">Operations for DaRT 8.0</span></span>](operations-for-dart-80-dart-8.md)  

<span data-ttu-id="038c3-117">[Récupération d’ordinateurs à l’aide de DaRT 8,0](recovering-computers-using-dart-80-dart-8.md) **|** [Diagnostic des échecs système avec l’analyseur](diagnosing-system-failures-with-crash-analyzer--dart-8.md) **|** d’incidents [Sécurité et confidentialité pour DaRT 8,0](security-and-privacy-for-dart-80-dart-8.md) **|** [Administration de DaRT 8,0 à l’aide de PowerShell](administering-dart-80-using-powershell-dart-8.md)</span><span class="sxs-lookup"><span data-stu-id="038c3-117">[Recovering Computers Using DaRT 8.0](recovering-computers-using-dart-80-dart-8.md)**|**[Diagnosing System Failures with Crash Analyzer](diagnosing-system-failures-with-crash-analyzer--dart-8.md)**|**[Security and Privacy for DaRT 8.0](security-and-privacy-for-dart-80-dart-8.md)**|**[Administering DaRT 8.0 Using PowerShell](administering-dart-80-using-powershell-dart-8.md)</span></span>

<a href="" id="technical-reference-for-dart-8-0"></a>[<span data-ttu-id="038c3-118">Informations techniques de référence sur DaRT8.0</span><span class="sxs-lookup"><span data-stu-id="038c3-118">Technical Reference for DaRT 8.0</span></span>](technical-reference-for-dart-80-new-ia.md)  

[<span data-ttu-id="038c3-119">Les utilisateurs de Microsoft Diagnostics and Recovery Tools (DaRT) doivent utiliser Microsoft Defender offline (WDO) pour détecter les programmes malveillants--></span><span class="sxs-lookup"><span data-stu-id="038c3-119">Microsoft Diagnostics and Recovery Toolset (DaRT) users should use Microsoft Defender Offline (WDO) for malware detection--></span></span>](use-windows-defender-offline-wdo-for-malware-protection-not-dart.md)

<a href="" id="troubleshooting-dart-8-0"></a>[<span data-ttu-id="038c3-120">Résolution des problèmes liés à DaRT8.0</span><span class="sxs-lookup"><span data-stu-id="038c3-120">Troubleshooting DaRT 8.0</span></span>](troubleshooting-dart-80-dart-8.md)  

### <span data-ttu-id="038c3-121">Plus d’informations</span><span class="sxs-lookup"><span data-stu-id="038c3-121">More Information</span></span>

<a href="" id="how-do-i-get-mdop"></a>[<span data-ttu-id="038c3-122">Comment obtenir MDOP</span><span class="sxs-lookup"><span data-stu-id="038c3-122">How Do I Get MDOP</span></span>](https://go.microsoft.com/fwlink/?LinkId=322049)  
<span data-ttu-id="038c3-123">Obtenez des informations sur la façon de télécharger DaRT.</span><span class="sxs-lookup"><span data-stu-id="038c3-123">Get information about how to download DaRT.</span></span>

<a href="" id="release-notes-for-dart-8-0"></a>[<span data-ttu-id="038c3-124">Notes de publication pour DaRT8.0</span><span class="sxs-lookup"><span data-stu-id="038c3-124">Release Notes for DaRT 8.0</span></span>](release-notes-for-dart-80--dart-8.md)  
<span data-ttu-id="038c3-125">Affichez les informations mises à jour sur le produit et les problèmes connus de DaRT 8,0.</span><span class="sxs-lookup"><span data-stu-id="038c3-125">View updated product information and known issues for DaRT 8.0.</span></span>

<a href="" id="mdop-techcenter-page"></a>[<span data-ttu-id="038c3-126">Page TechCenter de MDOP</span><span class="sxs-lookup"><span data-stu-id="038c3-126">MDOP TechCenter Page</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=225286)  
<span data-ttu-id="038c3-127">En savoir plus sur les dernières informations et ressources de MDOP.</span><span class="sxs-lookup"><span data-stu-id="038c3-127">Learn about the latest MDOP information and resources.</span></span>

<a href="" id="mdop-information-experience"></a>[<span data-ttu-id="038c3-128">Découverte des informations de MDOP</span><span class="sxs-lookup"><span data-stu-id="038c3-128">MDOP Information Experience</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=236032)  
<span data-ttu-id="038c3-129">Recherchez des documents, des vidéos et d’autres ressources pour MDOP technologies.</span><span class="sxs-lookup"><span data-stu-id="038c3-129">Find documentation, videos, and other resources for MDOP technologies.</span></span> <span data-ttu-id="038c3-130">Vous pouvez également [nous envoyer vos commentaires](mailto:MDOPDocs@microsoft.com)ou en savoir plus sur les mises à jour en nous suivant sur [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) ou [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447).</span><span class="sxs-lookup"><span data-stu-id="038c3-130">You can also [send us feedback](mailto:MDOPDocs@microsoft.com), or learn about updates by following us on [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) or [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447).</span></span>

 

 





