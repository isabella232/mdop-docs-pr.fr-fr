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
# Journaux des événements clients

Les journaux d’événements du client MBAM sont situés dans l’observateur d’événements: journaux des applications et des services-Microsoft-Windows-MBAM-Path opérationnel.
Le tableau suivant contient des ID d’événement qui peuvent se produire sur le client MBAM.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">ID d’événement</th>
<th align="left">Canal</th>
<th align="left">Symbole d’événement</th>
<th align="left">Message</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>1</p></td>
<td align="left"><p>Opération</p></td>
<td align="left"><p>VolumeEnactmentSuccessful</p></td>
<td align="left"><p>Les stratégies MBAM ont été appliquées correctement.</p></td>
</tr>
<tr class="even">
<td align="left"><p>deuxième</p></td>
<td align="left"><p>Admin</p></td>
<td align="left"><p>VolumeEnactmentFailed</p></td>
<td align="left"><p>Une erreur s’est produite lors de l’application de stratégies MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>3D</p></td>
<td align="left"><p>Opération</p></td>
<td align="left"><p>TransferStatusDataSuccessful</p></td>
<td align="left"><p>Les données d’état de cryptage ont bien été envoyées.</p></td>
</tr>
<tr class="even">
<td align="left"><p>n°4</p></td>
<td align="left"><p>Admin</p></td>
<td align="left"><p>TransferStatusDataFailed</p></td>
<td align="left"><p>Une erreur s’est produite lors de l’envoi des données d’état de chiffrement.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>version8</p></td>
<td align="left"><p>Admin</p></td>
<td align="left"><p>SystemVolumeNotFound</p></td>
<td align="left"><p>Le volume système est manquant. SystemVolume est nécessaire pour chiffrer le lecteur du système d’exploitation.</p></td>
</tr>
<tr class="even">
<td align="left"><p>09</p></td>
<td align="left"><p>Admin</p></td>
<td align="left"><p>TPMNotFound</p></td>
<td align="left"><p>Le matériel du TPM est manquant. Le module de plateforme sécurisée (TPM) est nécessaire pour chiffrer le lecteur du système d’exploitation avec tout protecteur de TPM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>0,10</p></td>
<td align="left"><p>Admin</p></td>
<td align="left"><p>MachineHWExempted</p></td>
<td align="left"><p>L’ordinateur est exempté du chiffrement. État matériel de l’ordinateur: exonéré</p></td>
</tr>
<tr class="even">
<td align="left"><p>27,9</p></td>
<td align="left"><p>Admin</p></td>
<td align="left"><p>MachineHWUnknown</p></td>
<td align="left"><p>L’ordinateur est exempté du chiffrement. État matériel de l’ordinateur: inconnu</p></td>
</tr>
<tr class="odd">
<td align="left"><p>midi</p></td>
<td align="left"><p>Admin</p></td>
<td align="left"><p>HWCheckFailed</p></td>
<td align="left"><p>La vérification de l’exemption matérielle a échoué.</p></td>
</tr>
<tr class="even">
<td align="left"><p>n°13</p></td>
<td align="left"><p>Admin</p></td>
<td align="left"><p>UserIsExempted</p></td>
<td align="left"><p>Le chiffrement est exempté pour l’utilisateur.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>13</p></td>
<td align="left"><p>Admin</p></td>
<td align="left"><p>UserIsWaiting</p></td>
<td align="left"><p>L’utilisateur a demandé une exemption.</p></td>
</tr>
<tr class="even">
<td align="left"><p>0,15</p></td>
<td align="left"><p>Admin</p></td>
<td align="left"><p>UserExemptionCheckFailed</p></td>
<td align="left"><p>Échec de la vérification d’exemption des utilisateurs.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Seiz</p></td>
<td align="left"><p>Admin</p></td>
<td align="left"><p>UserPostponed</p></td>
<td align="left"><p>L’utilisateur a retardé le processus de chiffrement.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Play</p></td>
<td align="left"><p>Admin</p></td>
<td align="left"><p>TPMInitializationFailed</p></td>
<td align="left"><p>Échec de l’initialisation du module de plateforme sécurisée. L’utilisateur a rejeté les modifications du BIOS.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>19</p></td>
<td align="left"><p>Admin</p></td>
<td align="left"><p>CoreServiceDown</p></td>
<td align="left"><p>Impossible de se connecter au service de récupération MBAM et de matériel.</p></td>
</tr>
<tr class="even">
<td align="left"><p>19,6</p></td>
<td align="left"><p>Opération</p></td>
<td align="left"><p>CoreServiceUp</p></td>
<td align="left"><p>Connexion réussie à la récupération MBAM et au service matériel.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>CX3-20</p></td>
<td align="left"><p>Admin</p></td>
<td align="left"><p>PolicyMismatch</p></td>
<td align="left"><p>La stratégie MBAM est en conflit ou est endommagée.</p></td>
</tr>
<tr class="even">
<td align="left"><p>vingt</p></td>
<td align="left"><p>Admin</p></td>
<td align="left"><p>ConflictingOSVolumePolicies</p></td>
<td align="left"><p>Conflit de stratégies de chiffrement de volume du système d’exploitation détecté. Vérifie les stratégies BitLocker et MBAM associées aux protecteurs de lecteurs du système d’exploitation.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>22</p></td>
<td align="left"><p>Admin</p></td>
<td align="left"><p>ConflictingFDDVolumePolicies</p></td>
<td align="left"><p>Conflit de stratégies de chiffrement de volume de données fixes détectées. Vérifie les stratégies BitLocker et MBAM associées aux protecteurs de lecteur de FDD.</p></td>
</tr>
<tr class="even">
<td align="left"><p>27</p></td>
<td align="left"><p>Admin</p></td>
<td align="left"><p>EncryptionFailedNoDra</p></td>
<td align="left"><p>Une erreur s’est produite lors du chiffrement. Un protecteur de l’agent de récupération de données est requis en mode FIPS pour les ordinateurs antérieurs à Windows 8,1.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>12,70</p></td>
<td align="left"><p>Opération</p></td>
<td align="left"><p>TpmOwnerAuthEscrowed</p></td>
<td align="left"><p>Le module de plateforme sécurisée OwnerAuth a été offert par un tiers.</p></td>
</tr>
<tr class="even">
<td align="left"><p>mai</p></td>
<td align="left"><p>Opération</p></td>
<td align="left"><p>RecoveryKeyEscrowed</p></td>
<td align="left"><p>La clé de récupération BitLocker pour le volume a été disposant d’une confiance.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>trente</p></td>
<td align="left"><p>Opération</p></td>
<td align="left"><p>RecoveryKeyReset</p></td>
<td align="left"><p>La clé de récupération BitLocker pour le volume a été mise à jour.</p></td>
</tr>
<tr class="even">
<td align="left"><p>°</p></td>
<td align="left"><p>Opération</p></td>
<td align="left"><p>EnforcePolicyDateSet</p></td>
<td align="left"><p>La date d’application de la stratégie de mise en <em> &lt; &gt; </em> place est définie pour le volume</p></td>
</tr>
<tr class="odd">
<td align="left"><p>32</p></td>
<td align="left"><p>Opération</p></td>
<td align="left"><p>EnforcePolicyDateCleared</p></td>
<td align="left"><p>La <em> &lt; Date d’activation de la stratégie &gt; </em> a été effacée pour le volume.</p></td>
</tr>
<tr class="even">
<td align="left"><p>33</p></td>
<td align="left"><p>Opération</p></td>
<td align="left"><p>TpmLockOutResetSucceeded</p></td>
<td align="left"><p>Réinitialisation du verrouillage du TPM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>34</p></td>
<td align="left"><p>Admin</p></td>
<td align="left"><p>TpmLockOutResetFailed</p></td>
<td align="left"><p>Échec de la réinitialisation du verrouillage du TPM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>35</p></td>
<td align="left"><p>Opération</p></td>
<td align="left"><p>TpmOwnerAuthRetrievalSucceeded</p></td>
<td align="left"><p>Réussite de l’extraction du TPM OwnerAuth des services MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>36</p></td>
<td align="left"><p>Admin</p></td>
<td align="left"><p>TpmOwnerAuthRetrievalFailed</p></td>
<td align="left"><p>Échec de l’extraction du module de plateforme sécurisée OwnerAuth des services MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>37</p></td>
<td align="left"><p>Admin</p></td>
<td align="left"><p>WmiProviderDllSearchPathUpdateFailed</p></td>
<td align="left"><p>Échec de la mise à jour du chemin de recherche de la DLL pour le fournisseur WMI.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>38</p></td>
<td align="left"><p>Admin</p></td>
<td align="left"><p>TimedOutWaitingForWmiProvider</p></td>
<td align="left"><p>Arrêt de l’agent-dépassement du délai d’attente de l’instance du fournisseur WMI MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>39</p></td>
<td align="left"><p>Opération</p></td>
<td align="left"><p>RemovableDriveMounted</p></td>
<td align="left"><p>Le lecteur amovible a été monté.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>40</p></td>
<td align="left"><p>Opération</p></td>
<td align="left"><p>RemovableDriveDismounted</p></td>
<td align="left"><p>Le lecteur amovible a été démonté.</p></td>
</tr>
<tr class="even">
<td align="left"><p>41</p></td>
<td align="left"><p>Opération</p></td>
<td align="left"><p>FailedToEnactEndpointUnreachable</p></td>
<td align="left"><p>L’échec de la connexion à la récupération MBAM et au service matériel a empêché les stratégies MBAM d’être appliquées au volume.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>42</p></td>
<td align="left"><p>Opération</p></td>
<td align="left"><p>FailedToEnactLockedVolume</p></td>
<td align="left"><p>L’état de volume verrouillé a empêché les stratégies MBAM de s’appliquer correctement au volume.</p></td>
</tr>
<tr class="even">
<td align="left"><p>43</p></td>
<td align="left"><p>Opération</p></td>
<td align="left"><p>TransferStatusDataFailedEndpointUnreachable</p></td>
<td align="left"><p>L’échec de la connexion à la compatibilité et au service d’État MBAM a empêché le transfert des données d’état de chiffrement.</p></td>
</tr>
</tbody>
</table>

 


## Rubriques connexes
[Document de référence technique pour MBAM2.5](technical-reference-for-mbam-25.md)

[Journaux des événements serveur](server-event-logs.md)

 


## Vous avez une suggestion pour MBAM?
- Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring) 
- Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





