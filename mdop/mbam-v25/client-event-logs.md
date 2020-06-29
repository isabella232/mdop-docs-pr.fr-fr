---
title: Journaux des événements clients
description: Journaux des événements clients
author: dansimp
ms.assetid: d5c2f270-db6a-45f1-8557-8c6fb28fd568
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7324d07bf018944fcbe24168bba2e9abea9cea41
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810409"
---
# <span data-ttu-id="9e0f1-103">Journaux des événements clients</span><span class="sxs-lookup"><span data-stu-id="9e0f1-103">Client Event Logs</span></span>

<span data-ttu-id="9e0f1-104">Les journaux d’événements du client MBAM sont situés dans l’observateur d’événements: journaux des applications et des services-Microsoft-Windows-MBAM-Path opérationnel.</span><span class="sxs-lookup"><span data-stu-id="9e0f1-104">MBAM Client event logs are located in Event Viewer – Applications and Services Logs – Microsoft – Windows – MBAM - Operational path.</span></span>
<span data-ttu-id="9e0f1-105">Le tableau suivant contient des ID d’événement qui peuvent se produire sur le client MBAM.</span><span class="sxs-lookup"><span data-stu-id="9e0f1-105">The following table contains event IDs that can occur on the MBAM Client.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9e0f1-106">ID d’événement</span><span class="sxs-lookup"><span data-stu-id="9e0f1-106">Event ID</span></span></th>
<th align="left"><span data-ttu-id="9e0f1-107">Canal</span><span class="sxs-lookup"><span data-stu-id="9e0f1-107">Channel</span></span></th>
<th align="left"><span data-ttu-id="9e0f1-108">Symbole d’événement</span><span class="sxs-lookup"><span data-stu-id="9e0f1-108">Event symbol</span></span></th>
<th align="left"><span data-ttu-id="9e0f1-109">Message</span><span class="sxs-lookup"><span data-stu-id="9e0f1-109">Message</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9e0f1-110">1</span><span class="sxs-lookup"><span data-stu-id="9e0f1-110">1</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-111">Opération</span><span class="sxs-lookup"><span data-stu-id="9e0f1-111">Operational</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-112">VolumeEnactmentSuccessful</span><span class="sxs-lookup"><span data-stu-id="9e0f1-112">VolumeEnactmentSuccessful</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-113">Les stratégies MBAM ont été appliquées correctement.</span><span class="sxs-lookup"><span data-stu-id="9e0f1-113">The MBAM policies were applied successfully.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9e0f1-114">deuxième</span><span class="sxs-lookup"><span data-stu-id="9e0f1-114">2</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-115">Admin</span><span class="sxs-lookup"><span data-stu-id="9e0f1-115">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-116">VolumeEnactmentFailed</span><span class="sxs-lookup"><span data-stu-id="9e0f1-116">VolumeEnactmentFailed</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-117">Une erreur s’est produite lors de l’application de stratégies MBAM.</span><span class="sxs-lookup"><span data-stu-id="9e0f1-117">An error occurred while applying MBAM policies.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9e0f1-118">3D</span><span class="sxs-lookup"><span data-stu-id="9e0f1-118">3</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-119">Opération</span><span class="sxs-lookup"><span data-stu-id="9e0f1-119">Operational</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-120">TransferStatusDataSuccessful</span><span class="sxs-lookup"><span data-stu-id="9e0f1-120">TransferStatusDataSuccessful</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-121">Les données d’état de cryptage ont bien été envoyées.</span><span class="sxs-lookup"><span data-stu-id="9e0f1-121">The encryption status data was sent successfully.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9e0f1-122">n°4</span><span class="sxs-lookup"><span data-stu-id="9e0f1-122">4</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-123">Admin</span><span class="sxs-lookup"><span data-stu-id="9e0f1-123">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-124">TransferStatusDataFailed</span><span class="sxs-lookup"><span data-stu-id="9e0f1-124">TransferStatusDataFailed</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-125">Une erreur s’est produite lors de l’envoi des données d’état de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="9e0f1-125">An error occurred while sending encryption status data.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9e0f1-126">version8</span><span class="sxs-lookup"><span data-stu-id="9e0f1-126">8</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-127">Admin</span><span class="sxs-lookup"><span data-stu-id="9e0f1-127">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-128">SystemVolumeNotFound</span><span class="sxs-lookup"><span data-stu-id="9e0f1-128">SystemVolumeNotFound</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-129">Le volume système est manquant.</span><span class="sxs-lookup"><span data-stu-id="9e0f1-129">The system volume is missing.</span></span> <span data-ttu-id="9e0f1-130">SystemVolume est nécessaire pour chiffrer le lecteur du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="9e0f1-130">SystemVolume is needed to encrypt the operating system drive.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9e0f1-131">09</span><span class="sxs-lookup"><span data-stu-id="9e0f1-131">9</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-132">Admin</span><span class="sxs-lookup"><span data-stu-id="9e0f1-132">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-133">TPMNotFound</span><span class="sxs-lookup"><span data-stu-id="9e0f1-133">TPMNotFound</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-134">Le matériel du TPM est manquant.</span><span class="sxs-lookup"><span data-stu-id="9e0f1-134">The TPM hardware is missing.</span></span> <span data-ttu-id="9e0f1-135">Le module de plateforme sécurisée (TPM) est nécessaire pour chiffrer le lecteur du système d’exploitation avec tout protecteur de TPM.</span><span class="sxs-lookup"><span data-stu-id="9e0f1-135">TPM is needed to encrypt the operating system drive with any TPM protector.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9e0f1-136">0,10</span><span class="sxs-lookup"><span data-stu-id="9e0f1-136">10</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-137">Admin</span><span class="sxs-lookup"><span data-stu-id="9e0f1-137">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-138">MachineHWExempted</span><span class="sxs-lookup"><span data-stu-id="9e0f1-138">MachineHWExempted</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-139">L’ordinateur est exempté du chiffrement.</span><span class="sxs-lookup"><span data-stu-id="9e0f1-139">The computer is exempted from Encryption.</span></span> <span data-ttu-id="9e0f1-140">État matériel de l’ordinateur: exonéré</span><span class="sxs-lookup"><span data-stu-id="9e0f1-140">Machine’s hardware status: Exempted</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9e0f1-141">27,9</span><span class="sxs-lookup"><span data-stu-id="9e0f1-141">11</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-142">Admin</span><span class="sxs-lookup"><span data-stu-id="9e0f1-142">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-143">MachineHWUnknown</span><span class="sxs-lookup"><span data-stu-id="9e0f1-143">MachineHWUnknown</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-144">L’ordinateur est exempté du chiffrement.</span><span class="sxs-lookup"><span data-stu-id="9e0f1-144">The computer is exempted from encryption.</span></span> <span data-ttu-id="9e0f1-145">État matériel de l’ordinateur: inconnu</span><span class="sxs-lookup"><span data-stu-id="9e0f1-145">Machine’s hardware status: Unknown</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9e0f1-146">midi</span><span class="sxs-lookup"><span data-stu-id="9e0f1-146">12</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-147">Admin</span><span class="sxs-lookup"><span data-stu-id="9e0f1-147">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-148">HWCheckFailed</span><span class="sxs-lookup"><span data-stu-id="9e0f1-148">HWCheckFailed</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-149">La vérification de l’exemption matérielle a échoué.</span><span class="sxs-lookup"><span data-stu-id="9e0f1-149">Hardware exemption check failed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9e0f1-150">n°13</span><span class="sxs-lookup"><span data-stu-id="9e0f1-150">13</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-151">Admin</span><span class="sxs-lookup"><span data-stu-id="9e0f1-151">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-152">UserIsExempted</span><span class="sxs-lookup"><span data-stu-id="9e0f1-152">UserIsExempted</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-153">Le chiffrement est exempté pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9e0f1-153">The user is exempt from encryption.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9e0f1-154">13</span><span class="sxs-lookup"><span data-stu-id="9e0f1-154">14</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-155">Admin</span><span class="sxs-lookup"><span data-stu-id="9e0f1-155">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-156">UserIsWaiting</span><span class="sxs-lookup"><span data-stu-id="9e0f1-156">UserIsWaiting</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-157">L’utilisateur a demandé une exemption.</span><span class="sxs-lookup"><span data-stu-id="9e0f1-157">The user requested an exemption.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9e0f1-158">0,15</span><span class="sxs-lookup"><span data-stu-id="9e0f1-158">15</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-159">Admin</span><span class="sxs-lookup"><span data-stu-id="9e0f1-159">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-160">UserExemptionCheckFailed</span><span class="sxs-lookup"><span data-stu-id="9e0f1-160">UserExemptionCheckFailed</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-161">Échec de la vérification d’exemption des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="9e0f1-161">User exemption check failed.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9e0f1-162">Seiz</span><span class="sxs-lookup"><span data-stu-id="9e0f1-162">16</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-163">Admin</span><span class="sxs-lookup"><span data-stu-id="9e0f1-163">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-164">UserPostponed</span><span class="sxs-lookup"><span data-stu-id="9e0f1-164">UserPostponed</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-165">L’utilisateur a retardé le processus de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="9e0f1-165">The user postponed the encryption process.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9e0f1-166">Play</span><span class="sxs-lookup"><span data-stu-id="9e0f1-166">17</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-167">Admin</span><span class="sxs-lookup"><span data-stu-id="9e0f1-167">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-168">TPMInitializationFailed</span><span class="sxs-lookup"><span data-stu-id="9e0f1-168">TPMInitializationFailed</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-169">Échec de l’initialisation du module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="9e0f1-169">TPM initialization failed.</span></span> <span data-ttu-id="9e0f1-170">L’utilisateur a rejeté les modifications du BIOS.</span><span class="sxs-lookup"><span data-stu-id="9e0f1-170">The user rejected the BIOS changes.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9e0f1-171">19</span><span class="sxs-lookup"><span data-stu-id="9e0f1-171">18</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-172">Admin</span><span class="sxs-lookup"><span data-stu-id="9e0f1-172">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-173">CoreServiceDown</span><span class="sxs-lookup"><span data-stu-id="9e0f1-173">CoreServiceDown</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-174">Impossible de se connecter au service de récupération MBAM et de matériel.</span><span class="sxs-lookup"><span data-stu-id="9e0f1-174">Unable to connect to the MBAM Recovery and Hardware service.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9e0f1-175">19,6</span><span class="sxs-lookup"><span data-stu-id="9e0f1-175">19</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-176">Opération</span><span class="sxs-lookup"><span data-stu-id="9e0f1-176">Operational</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-177">CoreServiceUp</span><span class="sxs-lookup"><span data-stu-id="9e0f1-177">CoreServiceUp</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-178">Connexion réussie à la récupération MBAM et au service matériel.</span><span class="sxs-lookup"><span data-stu-id="9e0f1-178">Successfully connected to the MBAM Recovery and Hardware service.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9e0f1-179">CX3-20</span><span class="sxs-lookup"><span data-stu-id="9e0f1-179">20</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-180">Admin</span><span class="sxs-lookup"><span data-stu-id="9e0f1-180">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-181">PolicyMismatch</span><span class="sxs-lookup"><span data-stu-id="9e0f1-181">PolicyMismatch</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-182">La stratégie MBAM est en conflit ou est endommagée.</span><span class="sxs-lookup"><span data-stu-id="9e0f1-182">The MBAM policy is in conflict or corrupt.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9e0f1-183">vingt</span><span class="sxs-lookup"><span data-stu-id="9e0f1-183">21</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-184">Admin</span><span class="sxs-lookup"><span data-stu-id="9e0f1-184">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-185">ConflictingOSVolumePolicies</span><span class="sxs-lookup"><span data-stu-id="9e0f1-185">ConflictingOSVolumePolicies</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-186">Conflit de stratégies de chiffrement de volume du système d’exploitation détecté.</span><span class="sxs-lookup"><span data-stu-id="9e0f1-186">Detected OS volume encryption policies conflict.</span></span> <span data-ttu-id="9e0f1-187">Vérifie les stratégies BitLocker et MBAM associées aux protecteurs de lecteurs du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="9e0f1-187">Check BitLocker and MBAM policies related to OS drive protectors.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9e0f1-188">22</span><span class="sxs-lookup"><span data-stu-id="9e0f1-188">22</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-189">Admin</span><span class="sxs-lookup"><span data-stu-id="9e0f1-189">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-190">ConflictingFDDVolumePolicies</span><span class="sxs-lookup"><span data-stu-id="9e0f1-190">ConflictingFDDVolumePolicies</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-191">Conflit de stratégies de chiffrement de volume de données fixes détectées.</span><span class="sxs-lookup"><span data-stu-id="9e0f1-191">Detected Fixed Data Drive volume encryption policies conflict.</span></span> <span data-ttu-id="9e0f1-192">Vérifie les stratégies BitLocker et MBAM associées aux protecteurs de lecteur de FDD.</span><span class="sxs-lookup"><span data-stu-id="9e0f1-192">Check BitLocker and MBAM policies related to FDD drive protectors.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9e0f1-193">27</span><span class="sxs-lookup"><span data-stu-id="9e0f1-193">27</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-194">Admin</span><span class="sxs-lookup"><span data-stu-id="9e0f1-194">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-195">EncryptionFailedNoDra</span><span class="sxs-lookup"><span data-stu-id="9e0f1-195">EncryptionFailedNoDra</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-196">Une erreur s’est produite lors du chiffrement.</span><span class="sxs-lookup"><span data-stu-id="9e0f1-196">An error occurred while encrypting.</span></span> <span data-ttu-id="9e0f1-197">Un protecteur de l’agent de récupération de données est requis en mode FIPS pour les ordinateurs antérieurs à Windows 8,1.</span><span class="sxs-lookup"><span data-stu-id="9e0f1-197">A Data Recovery Agent (DRA) protector is required in FIPS mode for pre-Windows 8.1 machines.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9e0f1-198">12,70</span><span class="sxs-lookup"><span data-stu-id="9e0f1-198">28</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-199">Opération</span><span class="sxs-lookup"><span data-stu-id="9e0f1-199">Operational</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-200">TpmOwnerAuthEscrowed</span><span class="sxs-lookup"><span data-stu-id="9e0f1-200">TpmOwnerAuthEscrowed</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-201">Le module de plateforme sécurisée OwnerAuth a été offert par un tiers.</span><span class="sxs-lookup"><span data-stu-id="9e0f1-201">The TPM OwnerAuth has been escrowed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9e0f1-202">mai</span><span class="sxs-lookup"><span data-stu-id="9e0f1-202">29</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-203">Opération</span><span class="sxs-lookup"><span data-stu-id="9e0f1-203">Operational</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-204">RecoveryKeyEscrowed</span><span class="sxs-lookup"><span data-stu-id="9e0f1-204">RecoveryKeyEscrowed</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-205">La clé de récupération BitLocker pour le volume a été disposant d’une confiance.</span><span class="sxs-lookup"><span data-stu-id="9e0f1-205">The BitLocker recovery key for the volume has been escrowed.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9e0f1-206">trente</span><span class="sxs-lookup"><span data-stu-id="9e0f1-206">30</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-207">Opération</span><span class="sxs-lookup"><span data-stu-id="9e0f1-207">Operational</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-208">RecoveryKeyReset</span><span class="sxs-lookup"><span data-stu-id="9e0f1-208">RecoveryKeyReset</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-209">La clé de récupération BitLocker pour le volume a été mise à jour.</span><span class="sxs-lookup"><span data-stu-id="9e0f1-209">The BitLocker recovery key for the volume has been updated.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9e0f1-210">°</span><span class="sxs-lookup"><span data-stu-id="9e0f1-210">31</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-211">Opération</span><span class="sxs-lookup"><span data-stu-id="9e0f1-211">Operational</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-212">EnforcePolicyDateSet</span><span class="sxs-lookup"><span data-stu-id="9e0f1-212">EnforcePolicyDateSet</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-213">La date d’application de la stratégie de mise en <em> &lt; &gt; </em> place est définie pour le volume</span><span class="sxs-lookup"><span data-stu-id="9e0f1-213">The enforce policy date, <em>&lt;date&gt;</em>, has been set for the volume</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9e0f1-214">32</span><span class="sxs-lookup"><span data-stu-id="9e0f1-214">32</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-215">Opération</span><span class="sxs-lookup"><span data-stu-id="9e0f1-215">Operational</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-216">EnforcePolicyDateCleared</span><span class="sxs-lookup"><span data-stu-id="9e0f1-216">EnforcePolicyDateCleared</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-217">La <em> &lt; Date d’activation de la stratégie &gt; </em> a été effacée pour le volume.</span><span class="sxs-lookup"><span data-stu-id="9e0f1-217">The enforce policy date, <em>&lt;date&gt;</em>, has been cleared for the volume.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9e0f1-218">33</span><span class="sxs-lookup"><span data-stu-id="9e0f1-218">33</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-219">Opération</span><span class="sxs-lookup"><span data-stu-id="9e0f1-219">Operational</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-220">TpmLockOutResetSucceeded</span><span class="sxs-lookup"><span data-stu-id="9e0f1-220">TpmLockOutResetSucceeded</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-221">Réinitialisation du verrouillage du TPM.</span><span class="sxs-lookup"><span data-stu-id="9e0f1-221">Successfully reset TPM lockout.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9e0f1-222">34</span><span class="sxs-lookup"><span data-stu-id="9e0f1-222">34</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-223">Admin</span><span class="sxs-lookup"><span data-stu-id="9e0f1-223">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-224">TpmLockOutResetFailed</span><span class="sxs-lookup"><span data-stu-id="9e0f1-224">TpmLockOutResetFailed</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-225">Échec de la réinitialisation du verrouillage du TPM.</span><span class="sxs-lookup"><span data-stu-id="9e0f1-225">Failed to reset TPM lockout.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9e0f1-226">35</span><span class="sxs-lookup"><span data-stu-id="9e0f1-226">35</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-227">Opération</span><span class="sxs-lookup"><span data-stu-id="9e0f1-227">Operational</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-228">TpmOwnerAuthRetrievalSucceeded</span><span class="sxs-lookup"><span data-stu-id="9e0f1-228">TpmOwnerAuthRetrievalSucceeded</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-229">Réussite de l’extraction du TPM OwnerAuth des services MBAM.</span><span class="sxs-lookup"><span data-stu-id="9e0f1-229">Successfully retrieved TPM OwnerAuth from MBAM services.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9e0f1-230">36</span><span class="sxs-lookup"><span data-stu-id="9e0f1-230">36</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-231">Admin</span><span class="sxs-lookup"><span data-stu-id="9e0f1-231">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-232">TpmOwnerAuthRetrievalFailed</span><span class="sxs-lookup"><span data-stu-id="9e0f1-232">TpmOwnerAuthRetrievalFailed</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-233">Échec de l’extraction du module de plateforme sécurisée OwnerAuth des services MBAM.</span><span class="sxs-lookup"><span data-stu-id="9e0f1-233">Failed to retrieve TPM OwnerAuth from MBAM services.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9e0f1-234">37</span><span class="sxs-lookup"><span data-stu-id="9e0f1-234">37</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-235">Admin</span><span class="sxs-lookup"><span data-stu-id="9e0f1-235">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-236">WmiProviderDllSearchPathUpdateFailed</span><span class="sxs-lookup"><span data-stu-id="9e0f1-236">WmiProviderDllSearchPathUpdateFailed</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-237">Échec de la mise à jour du chemin de recherche de la DLL pour le fournisseur WMI.</span><span class="sxs-lookup"><span data-stu-id="9e0f1-237">Failed to update the DLL search path for WMI provider.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9e0f1-238">38</span><span class="sxs-lookup"><span data-stu-id="9e0f1-238">38</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-239">Admin</span><span class="sxs-lookup"><span data-stu-id="9e0f1-239">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-240">TimedOutWaitingForWmiProvider</span><span class="sxs-lookup"><span data-stu-id="9e0f1-240">TimedOutWaitingForWmiProvider</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-241">Arrêt de l’agent-dépassement du délai d’attente de l’instance du fournisseur WMI MBAM.</span><span class="sxs-lookup"><span data-stu-id="9e0f1-241">Agent Stopping - Timed-out waiting for MBAM WMI Provider Instance.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9e0f1-242">39</span><span class="sxs-lookup"><span data-stu-id="9e0f1-242">39</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-243">Opération</span><span class="sxs-lookup"><span data-stu-id="9e0f1-243">Operational</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-244">RemovableDriveMounted</span><span class="sxs-lookup"><span data-stu-id="9e0f1-244">RemovableDriveMounted</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-245">Le lecteur amovible a été monté.</span><span class="sxs-lookup"><span data-stu-id="9e0f1-245">Removable drive was mounted.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9e0f1-246">40</span><span class="sxs-lookup"><span data-stu-id="9e0f1-246">40</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-247">Opération</span><span class="sxs-lookup"><span data-stu-id="9e0f1-247">Operational</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-248">RemovableDriveDismounted</span><span class="sxs-lookup"><span data-stu-id="9e0f1-248">RemovableDriveDismounted</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-249">Le lecteur amovible a été démonté.</span><span class="sxs-lookup"><span data-stu-id="9e0f1-249">Removable drive was unmounted.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9e0f1-250">41</span><span class="sxs-lookup"><span data-stu-id="9e0f1-250">41</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-251">Opération</span><span class="sxs-lookup"><span data-stu-id="9e0f1-251">Operational</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-252">FailedToEnactEndpointUnreachable</span><span class="sxs-lookup"><span data-stu-id="9e0f1-252">FailedToEnactEndpointUnreachable</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-253">L’échec de la connexion à la récupération MBAM et au service matériel a empêché les stratégies MBAM d’être appliquées au volume.</span><span class="sxs-lookup"><span data-stu-id="9e0f1-253">Failure to connect to the MBAM Recovery and Hardware service prevented MBAM policies from being applied successfully to the volume.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9e0f1-254">42</span><span class="sxs-lookup"><span data-stu-id="9e0f1-254">42</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-255">Opération</span><span class="sxs-lookup"><span data-stu-id="9e0f1-255">Operational</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-256">FailedToEnactLockedVolume</span><span class="sxs-lookup"><span data-stu-id="9e0f1-256">FailedToEnactLockedVolume</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-257">L’état de volume verrouillé a empêché les stratégies MBAM de s’appliquer correctement au volume.</span><span class="sxs-lookup"><span data-stu-id="9e0f1-257">Locked volume state prevented MBAM policies from being applied successfully to the volume.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9e0f1-258">43</span><span class="sxs-lookup"><span data-stu-id="9e0f1-258">43</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-259">Opération</span><span class="sxs-lookup"><span data-stu-id="9e0f1-259">Operational</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-260">TransferStatusDataFailedEndpointUnreachable</span><span class="sxs-lookup"><span data-stu-id="9e0f1-260">TransferStatusDataFailedEndpointUnreachable</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e0f1-261">L’échec de la connexion à la compatibilité et au service d’État MBAM a empêché le transfert des données d’état de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="9e0f1-261">Failure to connect to the MBAM Compliance and Status service prevented the transfer of encryption status data.</span></span></p></td>
</tr>
</tbody>
</table>

 


## <span data-ttu-id="9e0f1-262">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9e0f1-262">Related topics</span></span>
[<span data-ttu-id="9e0f1-263">Document de référence technique pour MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="9e0f1-263">Technical Reference for MBAM 2.5</span></span>](technical-reference-for-mbam-25.md)

[<span data-ttu-id="9e0f1-264">Journaux des événements serveur</span><span class="sxs-lookup"><span data-stu-id="9e0f1-264">Server Event Logs</span></span>](server-event-logs.md)

 


## <span data-ttu-id="9e0f1-265">Vous avez une suggestion pour MBAM?</span><span class="sxs-lookup"><span data-stu-id="9e0f1-265">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="9e0f1-266">Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)</span><span class="sxs-lookup"><span data-stu-id="9e0f1-266">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="9e0f1-267">Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="9e0f1-267">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





