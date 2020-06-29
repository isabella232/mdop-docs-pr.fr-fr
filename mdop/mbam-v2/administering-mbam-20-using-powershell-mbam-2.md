---
title: Administration de MBAM2.0 à l'aide de PowerShell
description: Administration de MBAM2.0 à l'aide de PowerShell
author: dansimp
ms.assetid: d785a8df-0a8c-4d70-abd2-93a762b4f3de
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 736943e707b5d033b8ba6c26641393f02f0cdaf8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809995"
---
# <span data-ttu-id="89b8d-103">Administration de MBAM2.0 à l'aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="89b8d-103">Administering MBAM 2.0 Using PowerShell</span></span>


<span data-ttu-id="89b8d-104">La surveillance et l’administration de BitLocker Microsoft (MBAM) fournissent l’ensemble d’applets de commande Windows PowerShell suivant.</span><span class="sxs-lookup"><span data-stu-id="89b8d-104">Microsoft BitLocker Administration and Monitoring (MBAM) provides the following listed set of Windows PowerShell cmdlets.</span></span> <span data-ttu-id="89b8d-105">Les administrateurs peuvent utiliser les applets de commande PowerShell suivants pour effectuer diverses tâches d’administration et de surveillance du serveur Microsoft BitLocker à partir de la ligne de commande plutôt que sur le site Web d’administration MBAM.</span><span class="sxs-lookup"><span data-stu-id="89b8d-105">Administrators can use these PowerShell cmdlets to perform various Microsoft BitLocker Administration and Monitoring server tasks from the command line rather than from the MBAM administration website.</span></span>

## <span data-ttu-id="89b8d-106">Administration de MBAM à l’aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="89b8d-106">How to Administer MBAM Using PowerShell</span></span>


<span data-ttu-id="89b8d-107">Utilisez les applets de commande PowerShell décrites ici pour administrer MBAM.</span><span class="sxs-lookup"><span data-stu-id="89b8d-107">Use the PowerShell cmdlets described here to administer MBAM.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="89b8d-108">Nom</span><span class="sxs-lookup"><span data-stu-id="89b8d-108">Name</span></span></th>
<th align="left"><span data-ttu-id="89b8d-109">Description</span><span class="sxs-lookup"><span data-stu-id="89b8d-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="89b8d-110">Installation-MBAM</span><span class="sxs-lookup"><span data-stu-id="89b8d-110">Install-Mbam</span></span></p></td>
<td align="left"><p><span data-ttu-id="89b8d-111">Installe les fonctionnalités MBAM qui fournissent une stratégie avancée, le chiffrement, la récupération de clés et le rapport de conformité.</span><span class="sxs-lookup"><span data-stu-id="89b8d-111">Installs the MBAM features that provide advanced policy, encryption, key recovery, and compliance reporting.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="89b8d-112">Désinstaller-MBAM</span><span class="sxs-lookup"><span data-stu-id="89b8d-112">Uninstall-Mbam</span></span></p></td>
<td align="left"><p><span data-ttu-id="89b8d-113">Supprime les fonctionnalités MBAM qui fournissent une stratégie avancée, le chiffrement, la récupération de clés et les outils de création de rapports de conformité.</span><span class="sxs-lookup"><span data-stu-id="89b8d-113">Removes the MBAM features that provide advanced policy, encryption, key recovery, and compliance reporting tools.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="89b8d-114">Get-MbamBitLockerRecoveryKey</span><span class="sxs-lookup"><span data-stu-id="89b8d-114">Get-MbamBitLockerRecoveryKey</span></span></p></td>
<td align="left"><p><span data-ttu-id="89b8d-115">Demande une clé de récupération MBAM qui permettra aux utilisateurs de déverrouiller un ordinateur ou un lecteur chiffré.</span><span class="sxs-lookup"><span data-stu-id="89b8d-115">Requests an MBAM recovery key that will enable users to unlock a computer or encrypted drive.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="89b8d-116">Get-MbamTPMOwnerPassword</span><span class="sxs-lookup"><span data-stu-id="89b8d-116">Get-MbamTPMOwnerPassword</span></span></p></td>
<td align="left"><p><span data-ttu-id="89b8d-117">Fournit aux utilisateurs un mot de passe de propriétaire de TPM qu’ils peuvent utiliser pour déverrouiller un module de plateforme sécurisée (TPM) lorsque le TPM les a verrouillés et ne acceptera plus son code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="89b8d-117">Provides users with a TPM owner password that they can use to unlock a Trusted Platform Module (TPM) when the TPM has locked them out and will no longer accept their PIN.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="89b8d-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="89b8d-118">Related topics</span></span>


[<span data-ttu-id="89b8d-119">Opérations de MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="89b8d-119">Operations for MBAM 2.0</span></span>](operations-for-mbam-20-mbam-2.md)

 

 





