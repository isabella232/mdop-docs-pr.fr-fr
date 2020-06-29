---
title: Déterminer pourquoi un appareil reçoit un message de non-conformité
description: Déterminer pourquoi un appareil reçoit un message de non-conformité
author: dansimp
ms.assetid: 793df330-a0ee-4759-b53a-95618ac74428
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/22/2017
ms.openlocfilehash: ce1d344676ebf4328506228f1bfa87c76e8036f9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810637"
---
# <span data-ttu-id="548ce-103">Déterminer pourquoi un appareil reçoit un message de non-conformité</span><span class="sxs-lookup"><span data-stu-id="548ce-103">Determining why a Device Receives a Noncompliance Message</span></span>


<span data-ttu-id="548ce-104">Les codes de non-conformité suivants sont fournis par WMI et décrivent les raisons pour lesquelles un appareil particulier est signalé par MBAM comme non conforme.</span><span class="sxs-lookup"><span data-stu-id="548ce-104">The following noncompliance codes are provided by WMI and describe the reasons why a particular device is reported by MBAM as noncompliant.</span></span>

<span data-ttu-id="548ce-105">Vous pouvez utiliser votre méthode préférée pour afficher WMI.</span><span class="sxs-lookup"><span data-stu-id="548ce-105">You can use your preferred method to view WMI.</span></span> <span data-ttu-id="548ce-106">Si vous utilisez PowerShell, exécutez `gwmi -class mbam_volume -Namespace root\microsoft\mbam` à partir d’une invite PowerShell et recherchez ReasonsForNoncompliance.</span><span class="sxs-lookup"><span data-stu-id="548ce-106">If you use PowerShell, run `gwmi -class mbam_volume -Namespace root\microsoft\mbam` from a PowerShell prompt and search for ReasonsForNoncompliance.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="548ce-107">Code de non-conformité</span><span class="sxs-lookup"><span data-stu-id="548ce-107">Non-Compliance Code</span></span></th>
<th align="left"><span data-ttu-id="548ce-108">Raison de l’absence de conformité</span><span class="sxs-lookup"><span data-stu-id="548ce-108">Reason for Non-Compliance</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="548ce-109">0,4</span><span class="sxs-lookup"><span data-stu-id="548ce-109">0</span></span></p></td>
<td align="left"><p><span data-ttu-id="548ce-110">Niveau de cryptage non AES 256.</span><span class="sxs-lookup"><span data-stu-id="548ce-110">Cipher strength not AES 256.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="548ce-111">1</span><span class="sxs-lookup"><span data-stu-id="548ce-111">1</span></span></p></td>
<td align="left"><p><span data-ttu-id="548ce-112">La stratégie MBAM nécessite que ce volume soit crypté, mais pas.</span><span class="sxs-lookup"><span data-stu-id="548ce-112">MBAM Policy requires this volume to be encrypted but it is not.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="548ce-113">deuxième</span><span class="sxs-lookup"><span data-stu-id="548ce-113">2</span></span></p></td>
<td align="left"><p><span data-ttu-id="548ce-114">La stratégie MBAM nécessite ce volume pour qu’elle soit chiffrée, mais elle est.</span><span class="sxs-lookup"><span data-stu-id="548ce-114">MBAM Policy requires this volume to NOT be encrypted, but it is.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="548ce-115">3D</span><span class="sxs-lookup"><span data-stu-id="548ce-115">3</span></span></p></td>
<td align="left"><p><span data-ttu-id="548ce-116">La stratégie MBAM nécessite ce volume utilise un protecteur de module de plateforme sécurisée, mais ce n’est pas le cas.</span><span class="sxs-lookup"><span data-stu-id="548ce-116">MBAM Policy requires this volume use a TPM protector, but it does not.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="548ce-117">n°4</span><span class="sxs-lookup"><span data-stu-id="548ce-117">4</span></span></p></td>
<td align="left"><p><span data-ttu-id="548ce-118">Pour utiliser une stratégie de MBAM, le volume doit utiliser un protecteur de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="548ce-118">MBAM Policy requires this volume use a TPM+PIN protector, but it does not.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="548ce-119">n°5</span><span class="sxs-lookup"><span data-stu-id="548ce-119">5</span></span></p></td>
<td align="left"><p><span data-ttu-id="548ce-120">La stratégie MBAM ne permet pas à un ordinateur de TPM de signaler comme compatible.</span><span class="sxs-lookup"><span data-stu-id="548ce-120">MBAM Policy does not allow non TPM machines to report as compliant.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="548ce-121">6</span><span class="sxs-lookup"><span data-stu-id="548ce-121">6</span></span></p></td>
<td align="left"><p><span data-ttu-id="548ce-122">Le volume possède un protecteur de TPM, mais le TPM n’est pas visible (amorcé avec la clé de récupération après la désactivation du TPM dans le BIOS?).</span><span class="sxs-lookup"><span data-stu-id="548ce-122">Volume has a TPM protector but the TPM is not visible (booted with recover key after disabling TPM in BIOS?).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="548ce-123">6</span><span class="sxs-lookup"><span data-stu-id="548ce-123">7</span></span></p></td>
<td align="left"><p><span data-ttu-id="548ce-124">La stratégie MBAM nécessite que ce volume utilise un protecteur de mot de passe, mais qu’il n’en possède pas.</span><span class="sxs-lookup"><span data-stu-id="548ce-124">MBAM Policy requires this volume use a password protector, but it does not have one.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="548ce-125">version8</span><span class="sxs-lookup"><span data-stu-id="548ce-125">8</span></span></p></td>
<td align="left"><p><span data-ttu-id="548ce-126">La stratégie MBAM nécessite que ce volume n’utilise pas un protecteur de mot de passe, mais qu’il en possède un.</span><span class="sxs-lookup"><span data-stu-id="548ce-126">MBAM Policy requires this volume NOT use a password protector, but it has one.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="548ce-127">09</span><span class="sxs-lookup"><span data-stu-id="548ce-127">9</span></span></p></td>
<td align="left"><p><span data-ttu-id="548ce-128">La stratégie MBAM nécessite que ce volume utilise un protecteur de déverrouillage automatique, mais qu’il n’en possède pas.</span><span class="sxs-lookup"><span data-stu-id="548ce-128">MBAM Policy requires this volume use an auto-unlock protector, but it does not have one.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="548ce-129">0,10</span><span class="sxs-lookup"><span data-stu-id="548ce-129">10</span></span></p></td>
<td align="left"><p><span data-ttu-id="548ce-130">La stratégie MBAM nécessite que ce volume n’utilise pas de protecteur de déverrouillage automatique, mais il en possède un.</span><span class="sxs-lookup"><span data-stu-id="548ce-130">MBAM Policy requires this volume NOT use an auto-unlock protector, but it has one.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="548ce-131">27,9</span><span class="sxs-lookup"><span data-stu-id="548ce-131">11</span></span></p></td>
<td align="left"><p><span data-ttu-id="548ce-132">Conflit de stratégie détecté qui empêche MBAM de signaler ce volume comme compatible.</span><span class="sxs-lookup"><span data-stu-id="548ce-132">Policy conflict detected preventing MBAM from reporting this volume as compliant.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="548ce-133">midi</span><span class="sxs-lookup"><span data-stu-id="548ce-133">12</span></span></p></td>
<td align="left"><p><span data-ttu-id="548ce-134">Un volume système est requis pour chiffrer le volume du système d’exploitation, mais il n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="548ce-134">A system volume is needed to encrypt the OS volume but it is not present.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="548ce-135">n°13</span><span class="sxs-lookup"><span data-stu-id="548ce-135">13</span></span></p></td>
<td align="left"><p><span data-ttu-id="548ce-136">La protection est suspendue pour le volume.</span><span class="sxs-lookup"><span data-stu-id="548ce-136">Protection is suspended for the volume.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="548ce-137">13</span><span class="sxs-lookup"><span data-stu-id="548ce-137">14</span></span></p></td>
<td align="left"><p><span data-ttu-id="548ce-138">Déverrouillez le code sans être sûr, sauf si le volume du système d’exploitation est crypté.</span><span class="sxs-lookup"><span data-stu-id="548ce-138">AutoUnlock unsafe unless the OS volume is encrypted.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="548ce-139">0,15</span><span class="sxs-lookup"><span data-stu-id="548ce-139">15</span></span></p></td>
<td align="left"><p><span data-ttu-id="548ce-140">La stratégie nécessite un minimum de Cypher, XTS-AES-128 bits, la force Cypher réelle est plus faible.</span><span class="sxs-lookup"><span data-stu-id="548ce-140">Policy requires minimum cypher strength is XTS-AES-128 bit, actual cypher strength is weaker than that.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="548ce-141">Seiz</span><span class="sxs-lookup"><span data-stu-id="548ce-141">16</span></span></p></td>
<td align="left"><p><span data-ttu-id="548ce-142">La stratégie nécessite un minimum de Cypher, XTS-AES-256 bits, la force Cypher réelle est plus faible.</span><span class="sxs-lookup"><span data-stu-id="548ce-142">Policy requires minimum cypher strength is XTS-AES-256 bit, actual cypher strength is weaker than that.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="548ce-143">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="548ce-143">Related topics</span></span>


[<span data-ttu-id="548ce-144">Document de référence technique pour MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="548ce-144">Technical Reference for MBAM 2.5</span></span>](technical-reference-for-mbam-25.md)

[<span data-ttu-id="548ce-145">Configuration des composants du serveur MBAM2.5 à l'aide de Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="548ce-145">Configuring MBAM 2.5 Server Features by Using Windows PowerShell</span></span>](configuring-mbam-25-server-features-by-using-windows-powershell.md)

 
## <span data-ttu-id="548ce-146">Vous avez une suggestion pour MBAM?</span><span class="sxs-lookup"><span data-stu-id="548ce-146">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="548ce-147">Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)</span><span class="sxs-lookup"><span data-stu-id="548ce-147">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="548ce-148">Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="548ce-148">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>
 





