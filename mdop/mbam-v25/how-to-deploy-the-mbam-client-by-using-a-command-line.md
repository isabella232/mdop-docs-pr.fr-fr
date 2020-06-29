---
title: Déploiement du client MBAM àl'aide d'une ligne de commande
description: Déploiement du client MBAM àl'aide d'une ligne de commande
author: dansimp
ms.assetid: ac1d4ffe-c26d-41c9-9737-a4f2b37fde24
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 416d76ad876c5114e3a8764111b6a15c879b13b5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810584"
---
# <span data-ttu-id="d9379-103">Déploiement du client MBAM àl'aide d'une ligne de commande</span><span class="sxs-lookup"><span data-stu-id="d9379-103">How to Deploy the MBAM Client by Using a Command Line</span></span>


<span data-ttu-id="d9379-104">Vous pouvez utiliser une ligne de commande pour déployer le logiciel client Microsoft BitLocker Administration and Analysis (MBAM).</span><span class="sxs-lookup"><span data-stu-id="d9379-104">You can use a command line to deploy the Microsoft BitLocker Administration and Monitoring (MBAM) Client software.</span></span>

## <span data-ttu-id="d9379-105">Ligne de commande pour déployer le logiciel client MBAM</span><span class="sxs-lookup"><span data-stu-id="d9379-105">Command Line to deploy the MBAM Client software</span></span>


<span data-ttu-id="d9379-106">Tapez la commande suivante à l’invite de commandes pour accepter automatiquement le contrat de licence utilisateur final lors du déploiement du logiciel client MBAM.</span><span class="sxs-lookup"><span data-stu-id="d9379-106">Type the following command at the command prompt to automatically accept the end user license agreement when deploying the MBAM Client software.</span></span>

**<span data-ttu-id="d9379-107">MBAMClientSetup.exe/acceptEula = Oui</span><span class="sxs-lookup"><span data-stu-id="d9379-107">MBAMClientSetup.exe /acceptEula=Yes</span></span>**

<span data-ttu-id="d9379-108">**Remarques**  Les options de la ligne de commande **/Ju** et **/JM** ne sont pas prises en charge et ne peuvent pas être utilisées pour installer le logiciel client MBAM.</span><span class="sxs-lookup"><span data-stu-id="d9379-108">**Note** The **/ju** and **/jm** command-line options are not supported and cannot be used to install the MBAM Client software.</span></span>

 

<span data-ttu-id="d9379-109">Tapez la commande suivante à l’invite de commandes pour extraire et installer le MSP:</span><span class="sxs-lookup"><span data-stu-id="d9379-109">Type the following command at the command prompt to extract and install the MSP:</span></span>

**<span data-ttu-id="d9379-110">MBAMClientSetup.exe le &lt; chemin d’accès/Extract pour extraire MSI &gt; /AcceptEULA = Yes</span><span class="sxs-lookup"><span data-stu-id="d9379-110">MBAMClientSetup.exe /extract &lt;path to extract MSI&gt; /acceptEula=Yes</span></span>**

<span data-ttu-id="d9379-111">Ensuite, installez la version MSI silencieusement en exécutant la commande suivante:</span><span class="sxs-lookup"><span data-stu-id="d9379-111">Then, install the MSI silently by running the following command:</span></span>

**<span data-ttu-id="d9379-112">msiexec/i &lt; path pour extraire le MSI &gt; /qb = 1 redémarrage = ReallySuppress</span><span class="sxs-lookup"><span data-stu-id="d9379-112">msiexec /i &lt;path to extracted MSI&gt; /qb ALLUSERS=1 REBOOT=ReallySuppress</span></span>**

<span data-ttu-id="d9379-113">**Remarques**  À partir de MBAM 2,5 SP1, un MSI distinct n’est plus inclus dans le produit MBAM.</span><span class="sxs-lookup"><span data-stu-id="d9379-113">**Note** Beginning in MBAM 2.5 SP1, a separate MSI is no longer included with the MBAM product.</span></span> <span data-ttu-id="d9379-114">Toutefois, vous pouvez extraire le MSI du fichier exécutable (. exe) qui est inclus dans le produit, après avoir accepté le CLUF.</span><span class="sxs-lookup"><span data-stu-id="d9379-114">However, you can extract the MSI from the executable file (.exe) that is included with the product, after accepting the EULA.</span></span>

 

## <a href="" id="optin-for-microsoft-updates-1-command-line-option"></a><span data-ttu-id="d9379-115">OPTIN \ _FOR \ _MICROSOFT \ _UPDATES = 1 option de ligne de commande</span><span class="sxs-lookup"><span data-stu-id="d9379-115">OPTIN\_FOR\_MICROSOFT\_UPDATES=1 command-line option</span></span>


<span data-ttu-id="d9379-116">Si vous le souhaitez, vous pouvez spécifier l’option de ligne de commande `OPTIN_FOR_MICROSOFT_UPDATES=1` lors de l’installation du logiciel client pour installer automatiquement les mises à jour de Microsoft sur les ordinateurs clients.</span><span class="sxs-lookup"><span data-stu-id="d9379-116">You can optionally specify the command-line option `OPTIN_FOR_MICROSOFT_UPDATES=1` during the Client software installation to automatically install Microsoft Updates on client computers.</span></span> <span data-ttu-id="d9379-117">Cette option permet à Microsoft Update de démarrer automatiquement et de rechercher les mises à jour disponibles à installer après la fin de l’installation du logiciel client.</span><span class="sxs-lookup"><span data-stu-id="d9379-117">Specifying this option makes Microsoft Update automatically start and search for available updates to install after the Client software installation finishes.</span></span>

<span data-ttu-id="d9379-118">Vous pouvez utiliser cette option de ligne de commande avec l’une des méthodes d’installation suivantes.</span><span class="sxs-lookup"><span data-stu-id="d9379-118">You can use this command-line option with either of the following installation methods.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d9379-119">Installez le logiciel client MBAM à l’aide de</span><span class="sxs-lookup"><span data-stu-id="d9379-119">Install the MBAM Client software by using</span></span></th>
<th align="left"><span data-ttu-id="d9379-120">Exemple</span><span class="sxs-lookup"><span data-stu-id="d9379-120">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="d9379-121">MBAMClientSetup.exe</span><span class="sxs-lookup"><span data-stu-id="d9379-121">MBAMClientSetup.exe</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="d9379-122">MbamClientSetup.exe OPTIN_FOR_MICROSOFT_UPDATES = 1</span><span class="sxs-lookup"><span data-stu-id="d9379-122">MbamClientSetup.exe OPTIN_FOR_MICROSOFT_UPDATES=1</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="d9379-123">msiexec/i MBAMClient.msi</span><span class="sxs-lookup"><span data-stu-id="d9379-123">msiexec /i MBAMClient.msi</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="d9379-124">msiexec/i MBAMClient.msi OPTIN_FOR_MICROSOFT_UPDATES = 1</span><span class="sxs-lookup"><span data-stu-id="d9379-124">msiexec /i MBAMClient.msi OPTIN_FOR_MICROSOFT_UPDATES=1</span></span></strong></p></td>
</tr>
</tbody>
</table>

 


## <span data-ttu-id="d9379-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d9379-125">Related topics</span></span>


[<span data-ttu-id="d9379-126">Déploiement du client MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="d9379-126">Deploying the MBAM 2.5 Client</span></span>](deploying-the-mbam-25-client.md)

 

 
## <span data-ttu-id="d9379-127">Vous avez une suggestion pour MBAM?</span><span class="sxs-lookup"><span data-stu-id="d9379-127">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="d9379-128">Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)</span><span class="sxs-lookup"><span data-stu-id="d9379-128">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="d9379-129">Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="d9379-129">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>




