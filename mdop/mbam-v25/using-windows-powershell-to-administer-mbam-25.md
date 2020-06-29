---
title: Utilisation de Windows PowerShell pour administrer MBAM2.5
description: Utilisation de Windows PowerShell pour administrer MBAM2.5
author: dansimp
ms.assetid: 64668e76-2cba-433d-8d2d-50df0a4b2997
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 11/02/2016
ms.openlocfilehash: 8db305bfbdf79723da2b186dd5cc00406a4089cc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804452"
---
# <span data-ttu-id="4c667-103">Utilisation de Windows PowerShell pour administrer MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="4c667-103">Using Windows PowerShell to Administer MBAM 2.5</span></span>


<span data-ttu-id="4c667-104">Cette rubrique décrit les applets de contrôle Windows PowerShell pour le contrôle de l’administration et de la surveillance de Microsoft BitLocker (MBAM) qui concernent la récupération d’ordinateurs ou de lecteurs lorsque les utilisateurs sont verrouillés.</span><span class="sxs-lookup"><span data-stu-id="4c667-104">This topic describes Windows PowerShell cmdlets for Microsoft BitLocker Administration and Monitoring (MBAM) that relate to recovering computers or drives when users get locked out.</span></span>

<span data-ttu-id="4c667-105">Pour les applets de fonction qui vous permettent de configurer les fonctionnalités du serveur MBAM, voir [Configuration des fonctionnalités du serveur MBAM 2,5 à l’aide de Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="4c667-105">For cmdlets that you use to configure MBAM Server features, see [Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md).</span></span>

## <a href="" id="cmdlets-for-recovering-computers-or-drives-that-are-managed-by-mbam-"></a><span data-ttu-id="4c667-106">Cmdlets permettant de récupérer des ordinateurs ou des lecteurs gérés par MBAM</span><span class="sxs-lookup"><span data-stu-id="4c667-106">Cmdlets for recovering computers or drives that are managed by MBAM</span></span>


<span data-ttu-id="4c667-107">Utilisez les applets de commande Windows PowerShell suivantes pour récupérer des ordinateurs ou des lecteurs gérés par MBAM.</span><span class="sxs-lookup"><span data-stu-id="4c667-107">Use the following Windows PowerShell cmdlets to recover computers or drives that are managed by MBAM.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="4c667-108">Nom</span><span class="sxs-lookup"><span data-stu-id="4c667-108">Name</span></span></th>
<th align="left"><span data-ttu-id="4c667-109">Description</span><span class="sxs-lookup"><span data-stu-id="4c667-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4c667-110">Get-MbamBitLockerRecoveryKey</span><span class="sxs-lookup"><span data-stu-id="4c667-110">Get-MbamBitLockerRecoveryKey</span></span></p></td>
<td align="left"><p><span data-ttu-id="4c667-111">Demande une clé de récupération MBAM qui permet aux utilisateurs de déverrouiller un ordinateur ou un lecteur chiffré.</span><span class="sxs-lookup"><span data-stu-id="4c667-111">Requests an MBAM recovery key that enables users to unlock a computer or encrypted drive.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4c667-112">Get-MbamTPMOwnerPassword</span><span class="sxs-lookup"><span data-stu-id="4c667-112">Get-MbamTPMOwnerPassword</span></span></p></td>
<td align="left"><p><span data-ttu-id="4c667-113">Fournit aux utilisateurs un mot de passe de propriétaire de TPM qu’ils peuvent utiliser pour déverrouiller un module de plateforme sécurisée (TPM) lorsque le TPM les a verrouillés et ne acceptera plus son code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="4c667-113">Provides users with a TPM owner password that they can use to unlock a Trusted Platform Module (TPM) when the TPM has locked them out and will no longer accept their PIN.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="---------mbam-cmdlet-help"></a> <span data-ttu-id="4c667-114">Aide de l’applet de MBAM</span><span class="sxs-lookup"><span data-stu-id="4c667-114">MBAM cmdlet Help</span></span>


<span data-ttu-id="4c667-115">L’aide de Windows PowerShell pour les applets de commande MBAM est disponible dans les formats suivants:</span><span class="sxs-lookup"><span data-stu-id="4c667-115">Windows PowerShell Help for MBAM cmdlets is available in the following formats:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="4c667-116">Format d’aide de Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="4c667-116">Windows PowerShell Help format</span></span></th>
<th align="left"><span data-ttu-id="4c667-117">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="4c667-117">More information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4c667-118">À l’invite de commandes Windows PowerShell, tapez <strong> get- </strong> &lt; <em> cmdlet cmdlet.</em>&gt;</span><span class="sxs-lookup"><span data-stu-id="4c667-118">At a Windows PowerShell command prompt, type <strong>Get-Help</strong> &lt;<em>cmdlet</em>&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="4c667-119">Pour télécharger les dernières applets de cmdlet Windows PowerShell, suivez les instructions de <a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)"> Configuration des fonctionnalités du serveur MBAM 2,5 à l’aide de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4c667-119">To upload the latest Windows PowerShell cmdlets, follow the instructions in <a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)">Configuring MBAM 2.5 Server Features by Using Windows PowerShell</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4c667-120">Sur TechNet en tant que pages Web</span><span class="sxs-lookup"><span data-stu-id="4c667-120">On TechNet as webpages</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393498" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393498">https://go.microsoft.com/fwlink/?LinkId=393498</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4c667-121">Dans le centre de téléchargement en tant que fichier Word. docx</span><span class="sxs-lookup"><span data-stu-id="4c667-121">On the Download Center as a Word .docx file</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393497" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393497">https://go.microsoft.com/fwlink/?LinkId=393497</a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4c667-122">Dans le centre de téléchargement sous forme de fichier. pdf</span><span class="sxs-lookup"><span data-stu-id="4c667-122">On the Download Center as a .pdf file</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393499" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393499">https://go.microsoft.com/fwlink/?LinkId=393499</a></p></td>
</tr>
</tbody>
</table>

 



## <span data-ttu-id="4c667-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4c667-123">Related topics</span></span>


[<span data-ttu-id="4c667-124">Administration des composants de MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="4c667-124">Administering MBAM 2.5 Features</span></span>](administering-mbam-25-features.md)

[<span data-ttu-id="4c667-125">Configuration des composants du serveur MBAM2.5 à l'aide de Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="4c667-125">Configuring MBAM 2.5 Server Features by Using Windows PowerShell</span></span>](configuring-mbam-25-server-features-by-using-windows-powershell.md)

 

## <span data-ttu-id="4c667-126">Vous avez une suggestion pour MBAM?</span><span class="sxs-lookup"><span data-stu-id="4c667-126">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="4c667-127">Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)</span><span class="sxs-lookup"><span data-stu-id="4c667-127">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="4c667-128">Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="4c667-128">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





