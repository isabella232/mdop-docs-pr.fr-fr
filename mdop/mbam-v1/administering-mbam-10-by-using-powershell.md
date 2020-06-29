---
title: Administration de MBAM1.0 à l'aide de PowerShell
description: Administration de MBAM1.0 à l'aide de PowerShell
author: dansimp
ms.assetid: 3bf2eca5-4ab7-4e84-9e80-c0c7d709647b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3547bee9b2efc58252bb6f0a1cb0aa4c484e4e80
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810974"
---
# <span data-ttu-id="02fff-103">Administration de MBAM1.0 à l'aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="02fff-103">Administering MBAM 1.0 by Using PowerShell</span></span>


<span data-ttu-id="02fff-104">La surveillance et l’administration de BitLocker Microsoft (MBAM) fournissent l’ensemble d’applets de commande Windows PowerShell suivant.</span><span class="sxs-lookup"><span data-stu-id="02fff-104">Microsoft BitLocker Administration and Monitoring (MBAM) provides the following listed set of Windows PowerShell cmdlets.</span></span> <span data-ttu-id="02fff-105">Les administrateurs peuvent utiliser les applets de commande PowerShell suivants pour effectuer diverses tâches serveur MBAM à partir de l’invite de commandes plutôt que du site Web d’administration MBAM.</span><span class="sxs-lookup"><span data-stu-id="02fff-105">Administrators can use these PowerShell cmdlets to perform various MBAM server tasks from the command prompt rather than from the MBAM administration website.</span></span>

## <span data-ttu-id="02fff-106">Administration de MBAM à l’aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="02fff-106">How to administer MBAM by using PowerShell</span></span>


<span data-ttu-id="02fff-107">Utilisez les applets de commande PowerShell décrites ici pour administrer MBAM.</span><span class="sxs-lookup"><span data-stu-id="02fff-107">Use the PowerShell cmdlets described here to administer MBAM.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="02fff-108">Nom</span><span class="sxs-lookup"><span data-stu-id="02fff-108">Name</span></span></th>
<th align="left"><span data-ttu-id="02fff-109">Description</span><span class="sxs-lookup"><span data-stu-id="02fff-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="02fff-110">Add-MbamHardwareType</span><span class="sxs-lookup"><span data-stu-id="02fff-110">Add-MbamHardwareType</span></span></p></td>
<td align="left"><p><span data-ttu-id="02fff-111">Ajoute un nouveau modèle matérielle à l’inventaire matériel MBAM.</span><span class="sxs-lookup"><span data-stu-id="02fff-111">Adds a new hardware model to the MBAM hardware inventory.</span></span> <span data-ttu-id="02fff-112">Cette applet de commande peut également indiquer si le matériel est pris en charge ou n’est pas pris en charge pour le chiffrement de lecteur BitLocker.</span><span class="sxs-lookup"><span data-stu-id="02fff-112">This cmdlet can also specify whether the hardware is supported or unsupported for BitLocker drive encryption.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="02fff-113">Get-MbamBitLockerRecoveryKey</span><span class="sxs-lookup"><span data-stu-id="02fff-113">Get-MbamBitLockerRecoveryKey</span></span></p></td>
<td align="left"><p><span data-ttu-id="02fff-114">Demande une clé de récupération MBAM qui permettra à un utilisateur de déverrouiller un ordinateur ou un lecteur chiffré.</span><span class="sxs-lookup"><span data-stu-id="02fff-114">Requests an MBAM recovery key that will enable a user to unlock a computer or encrypted drive.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="02fff-115">Get-MbamHardwareType</span><span class="sxs-lookup"><span data-stu-id="02fff-115">Get-MbamHardwareType</span></span></p></td>
<td align="left"><p><span data-ttu-id="02fff-116">Obtient un inventaire matériel principal qui contient des données indiquant si les modèles matériels sont compatibles ou incompatibles avec le chiffrement de lecteur BitLocker.</span><span class="sxs-lookup"><span data-stu-id="02fff-116">Gets a master hardware inventory that contains data that indicates whether hardware models are compatible or incompatible with BitLocker drive encryption.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="02fff-117">Get-MbamTPMOwnerPassword</span><span class="sxs-lookup"><span data-stu-id="02fff-117">Get-MbamTPMOwnerPassword</span></span></p></td>
<td align="left"><p><span data-ttu-id="02fff-118">Fournit un mot de passe de propriétaire de TPM à un utilisateur pour gérer son accès au module de plateforme sécurisée (TPM).</span><span class="sxs-lookup"><span data-stu-id="02fff-118">Provides a TPM owner password for a user to manage their TPM (Trusted Platform Module) access.</span></span> <span data-ttu-id="02fff-119">Aide les utilisateurs lorsque le TPM les a verrouillés et n’accepte plus son code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="02fff-119">Helps users when TPM has locked them out and will no longer accept their PIN.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="02fff-120">Installation-MBAM</span><span class="sxs-lookup"><span data-stu-id="02fff-120">Install-Mbam</span></span></p></td>
<td align="left"><p><span data-ttu-id="02fff-121">Installe des fonctionnalités MBAM qui fournissent des outils avancés de stratégie de groupe, de chiffrement, de récupération de clés et de création de rapports de conformité.</span><span class="sxs-lookup"><span data-stu-id="02fff-121">Installs MBAM features that provide advanced group policy, encryption, key recovery, and compliance reporting tools.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="02fff-122">Remove-MbamHardwareType</span><span class="sxs-lookup"><span data-stu-id="02fff-122">Remove-MbamHardwareType</span></span></p></td>
<td align="left"><p><span data-ttu-id="02fff-123">Supprime les modèles matériels de l’inventaire matériel.</span><span class="sxs-lookup"><span data-stu-id="02fff-123">Removes the hardware models from the hardware inventory.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="02fff-124">Set-MbamHardwareType</span><span class="sxs-lookup"><span data-stu-id="02fff-124">Set-MbamHardwareType</span></span></p></td>
<td align="left"><p><span data-ttu-id="02fff-125">Permet la gestion d’un inventaire principal du matériel pour indiquer si les modèles matériels sont compatibles ou ne peuvent pas effectuer le chiffrement BitLocker.</span><span class="sxs-lookup"><span data-stu-id="02fff-125">Allows management of a master hardware inventory to designate whether or not hardware models are capable or incapable to perform BitLocker encryption.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="02fff-126">Désinstaller-MBAM</span><span class="sxs-lookup"><span data-stu-id="02fff-126">Uninstall-Mbam</span></span></p></td>
<td align="left"><p><span data-ttu-id="02fff-127">Supprime les fonctionnalités MBAM déjà installées qui fournissent des outils avancés de stratégie, de chiffrement, de récupération de clés et de création de rapports de conformité.</span><span class="sxs-lookup"><span data-stu-id="02fff-127">Removes previously installed MBAM features that provide advanced policy, encryption, key recovery, and compliance reporting tools.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="02fff-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="02fff-128">Related topics</span></span>


[<span data-ttu-id="02fff-129">Opérations de MBAM1.0</span><span class="sxs-lookup"><span data-stu-id="02fff-129">Operations for MBAM 1.0</span></span>](operations-for-mbam-10.md)

 

 





