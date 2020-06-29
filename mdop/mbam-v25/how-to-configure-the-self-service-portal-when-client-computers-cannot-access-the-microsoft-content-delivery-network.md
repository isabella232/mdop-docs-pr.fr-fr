---
title: Comment configurer le portail libre-service lorsque les ordinateurs clients ne peuvent pas accéder au réseau de distribution de contenu Microsoft
description: Comment configurer le portail libre-service lorsque les ordinateurs clients ne peuvent pas accéder au réseau de distribution de contenu Microsoft
author: dansimp
ms.assetid: 90ee76db-9876-41b5-994a-118556d5ed3b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ffce3dd023cb6ff9bd5cdb13ea789b348661de24
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810589"
---
# <span data-ttu-id="8e1ab-103">Comment configurer le portail libre-service lorsque les ordinateurs clients ne peuvent pas accéder au réseau de distribution de contenu Microsoft</span><span class="sxs-lookup"><span data-stu-id="8e1ab-103">How to Configure the Self-Service Portal When Client Computers Cannot Access the Microsoft Content Delivery Network</span></span>


<span data-ttu-id="8e1ab-104">Suivez ces instructions si les ordinateurs clients de votre organisation n’ont pas accès au réseau de distribution de contenu (CDN) Microsoft Ajax.</span><span class="sxs-lookup"><span data-stu-id="8e1ab-104">Follow these instructions if the client computers in your organization do not have access to the Microsoft Ajax Content Delivery Network (CDN).</span></span>

**<span data-ttu-id="8e1ab-105">Pourquoi devez-vous configurer:</span><span class="sxs-lookup"><span data-stu-id="8e1ab-105">Why you need to configure this:</span></span>**

<span data-ttu-id="8e1ab-106">Vos ordinateurs clients doivent avoir accès au réseau de distribution de contenu (CDN), ce qui donne au portail libre-service l’accès requis à certains fichiers JavaScript.</span><span class="sxs-lookup"><span data-stu-id="8e1ab-106">Your client computers need access to the CDN, which gives the Self-Service Portal the required access to certain JavaScript files.</span></span> <span data-ttu-id="8e1ab-107">Si vous ne configurez pas le portail libre-service lorsque les ordinateurs clients ne peuvent pas accéder au CDN, seul le nom de la société et le compte sous lequel l’utilisateur final se connecte s’affiche.</span><span class="sxs-lookup"><span data-stu-id="8e1ab-107">If you don’t configure the Self-Service Portal when client computers cannot access CDN, only the company name and the account under which the end user logs in will be displayed.</span></span> <span data-ttu-id="8e1ab-108">Aucun message d’erreur ne s’affichera.</span><span class="sxs-lookup"><span data-stu-id="8e1ab-108">No error message will be shown.</span></span>

<span data-ttu-id="8e1ab-109">**Remarques**  Dans MBAM 2,5 SP1, les fichiers JavaScript sont inclus dans le produit, et vous n’avez pas besoin de suivre les instructions de cette section pour configurer le SSP pour la prise en charge des clients qui ne peuvent pas accéder à Internet.</span><span class="sxs-lookup"><span data-stu-id="8e1ab-109">**Note** In MBAM 2.5 SP1, the JavaScript files are included in the product, and you do not need to follow the instructions in this section to configure the SSP to support clients that cannot access the internet.</span></span>

 

**<span data-ttu-id="8e1ab-110">Configuration du portail libre-service lorsque les ordinateurs clients ne peuvent pas accéder au CDN</span><span class="sxs-lookup"><span data-stu-id="8e1ab-110">How to configure the Self-Service Portal when client computers cannot access the CDN</span></span>**

1. <span data-ttu-id="8e1ab-111">Téléchargez les fichiers JavaScript suivants à partir du réseau de distribution de contenu (CDN):</span><span class="sxs-lookup"><span data-stu-id="8e1ab-111">Download the following JavaScript files from the CDN:</span></span>

   -   [<span data-ttu-id="8e1ab-112">jQuery-1.10.2.min.js</span><span class="sxs-lookup"><span data-stu-id="8e1ab-112">jQuery-1.10.2.min.js</span></span>](https://go.microsoft.com/fwlink/?LinkID=390515)

   -   [<span data-ttu-id="8e1ab-113">jQuery.validate.min.js</span><span class="sxs-lookup"><span data-stu-id="8e1ab-113">jQuery.validate.min.js</span></span>](https://go.microsoft.com/fwlink/?LinkID=390516)

   -   [<span data-ttu-id="8e1ab-114">jQuery.validate.unobtrusive.min.js</span><span class="sxs-lookup"><span data-stu-id="8e1ab-114">jQuery.validate.unobtrusive.min.js</span></span>](https://go.microsoft.com/fwlink/?LinkID=390517)

2. <span data-ttu-id="8e1ab-115">Copiez les fichiers JavaScript dans le répertoire **scripts** du portail libre-service.</span><span class="sxs-lookup"><span data-stu-id="8e1ab-115">Copy the JavaScript files to the **Scripts** directory of the Self-Service Portal.</span></span> <span data-ttu-id="8e1ab-116">Ce répertoire se trouve dans <em> &lt; MBAM répertoire d’installation de self-service &gt; \\ </em> Website\\Scripts.</span><span class="sxs-lookup"><span data-stu-id="8e1ab-116">This directory is located in <em>&lt;MBAM Self-Service Install Directory&gt;\\</em>Self Service Website\\Scripts.</span></span>

3. <span data-ttu-id="8e1ab-117">Ouvrez le gestionnaire des services Internet (IIS).</span><span class="sxs-lookup"><span data-stu-id="8e1ab-117">Open Internet Information Services (IIS) Manager.</span></span>

4. <span data-ttu-id="8e1ab-118">Développez **sites** &gt; **Microsoft et surveillance de BitLocker**et mettez en surbrillance **selfservice**.</span><span class="sxs-lookup"><span data-stu-id="8e1ab-118">Expand **Sites** &gt; **Microsoft BitLocker Administration and Monitoring**, and highlight **SelfService**.</span></span>

   **<span data-ttu-id="8e1ab-119">Remarque</span><span class="sxs-lookup"><span data-stu-id="8e1ab-119">Note</span></span>**  
   <span data-ttu-id="8e1ab-120">*Selfservice* est le nom de répertoire virtuel par défaut.</span><span class="sxs-lookup"><span data-stu-id="8e1ab-120">*SelfService* is the default virtual directory name.</span></span> <span data-ttu-id="8e1ab-121">Si vous avez choisi un autre nom pour ce répertoire lors de la configuration, n’oubliez pas de remplacer *selfservice* dans ces instructions par le nom que vous avez choisi.</span><span class="sxs-lookup"><span data-stu-id="8e1ab-121">If you chose a different name for this directory during the configuration, remember to replace *SelfService* in these instructions with the name you chose.</span></span>

     

5. <span data-ttu-id="8e1ab-122">Dans le volet du milieu, double-cliquez sur paramètres de l' **application**.</span><span class="sxs-lookup"><span data-stu-id="8e1ab-122">In the middle pane, double-click **Application Settings**.</span></span>

6. <span data-ttu-id="8e1ab-123">Pour chaque élément de la liste ci-dessous, modifiez les paramètres de l’application pour référencer le nouvel emplacement par remplacement/ &lt; *répertoire virtuel* &gt; /à l’aide de/selfservice/(ou du nom que vous avez choisi lors de la configuration).</span><span class="sxs-lookup"><span data-stu-id="8e1ab-123">For each item in the following list, edit the application settings to reference the new location by replacing /&lt;*virtual directory*&gt;/ with /SelfService/ (or whatever name you chose during configuration).</span></span> <span data-ttu-id="8e1ab-124">Par exemple, le chemin d’accès du répertoire virtuel est semblable à/selfservice/Scripts/jQuery-1.10.2.min.js.</span><span class="sxs-lookup"><span data-stu-id="8e1ab-124">For example, the virtual directory path will be similar to /selfservice/Scripts/ jQuery-1.10.2.min.js.</span></span>

   -   <span data-ttu-id="8e1ab-125">jQueryPath:/ &lt; *répertoire virtuel* &gt; /scripts/jQuery-1.10.2.min.js</span><span class="sxs-lookup"><span data-stu-id="8e1ab-125">jQueryPath: /&lt;*virtual directory*&gt;/Scripts/jQuery-1.10.2.min.js</span></span>

   -   <span data-ttu-id="8e1ab-126">jQueryValidatePath:/ &lt; *répertoire virtuel* &gt; /scripts/jQuery.validate.min.js</span><span class="sxs-lookup"><span data-stu-id="8e1ab-126">jQueryValidatePath: /&lt;*virtual directory*&gt;/Scripts/jQuery.validate.min.js</span></span>

   -   <span data-ttu-id="8e1ab-127">jQueryValidateUnobtrusivePath:/ &lt; *répertoire virtuel* &gt; /scripts/jQuery.validate.unobtrusive.min.js</span><span class="sxs-lookup"><span data-stu-id="8e1ab-127">jQueryValidateUnobtrusivePath: /&lt;*virtual directory*&gt;/Scripts/jQuery.validate.unobtrusive.min.js</span></span>



## <span data-ttu-id="8e1ab-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8e1ab-128">Related topics</span></span>


[<span data-ttu-id="8e1ab-129">Comment configurer les applications Web MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="8e1ab-129">How to Configure the MBAM 2.5 Web Applications</span></span>](how-to-configure-the-mbam-25-web-applications.md)

 

## <span data-ttu-id="8e1ab-130">Vous avez une suggestion pour MBAM?</span><span class="sxs-lookup"><span data-stu-id="8e1ab-130">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="8e1ab-131">Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)</span><span class="sxs-lookup"><span data-stu-id="8e1ab-131">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="8e1ab-132">Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="8e1ab-132">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





