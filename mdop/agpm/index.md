---
title: Gestion avancée des stratégies de groupe
description: Gestion avancée des stratégies de groupe
author: dansimp
ms.assetid: 493ca3c3-c3d6-4bb1-9430-dc1e43c86bb0
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 11/23/2017
ms.openlocfilehash: 457cca9db5d39466691b0bc7c41455910b4483d5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10795487"
---
# <span data-ttu-id="ce967-103">Gestion avancée des stratégies de groupe</span><span class="sxs-lookup"><span data-stu-id="ce967-103">Advanced Group Policy Management</span></span>


<span data-ttu-id="ce967-104">Microsoft Advanced Group Policy Management (AGPM) étend les fonctionnalités de la console de gestion des stratégies de groupe (GPMC) pour fournir un contrôle de modification complet et une gestion améliorée pour les objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="ce967-104">Microsoft Advanced Group Policy Management (AGPM) extends the capabilities of the Group Policy Management Console (GPMC) to provide comprehensive change control and improved management for Group Policy Objects (GPOs).</span></span> <span data-ttu-id="ce967-105">AGPM est disponible dans le cadre du pack d’optimisation de bureau Microsoft (MDOP) pour la Software Assurance.</span><span class="sxs-lookup"><span data-stu-id="ce967-105">AGPM is available as part of the Microsoft Desktop Optimization Pack (MDOP) for Software Assurance.</span></span>

## <span data-ttu-id="ce967-106">Informations sur la version d’AGPM</span><span class="sxs-lookup"><span data-stu-id="ce967-106">AGPM Version Information</span></span>


<span data-ttu-id="ce967-107">[AGPM 4,0 SP3](agpm-40-sp3-navengl.md) prend en charge Windows 10, windows server 2019, windows server 2016, windows server 2012 R2, Windows 7, Windows Server 8,1, windows server 2012 R2, Windows 7, windows Server 2008 et Windows Vista avec SP1.</span><span class="sxs-lookup"><span data-stu-id="ce967-107">[AGPM 4.0 SP3](agpm-40-sp3-navengl.md) supports Windows 10, Windows Server 2019, Windows Server 2016, Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows Server 2008 R2, Windows 7, Windows Server 2008, and Windows Vista with SP1.</span></span>

<span data-ttu-id="ce967-108">[AGPM 4,0 SP2](agpm-40-sp2-navengl.md) prend en charge windows server 2012 R2, Windows 8,1, windows server 2012, windows Server 2008 R2, Windows 7, windows Server 2008 et Windows Vista avec SP1.</span><span class="sxs-lookup"><span data-stu-id="ce967-108">[AGPM 4.0 SP2](agpm-40-sp2-navengl.md) supports Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows Server 2008 R2, Windows 7, Windows Server 2008, and Windows Vista with SP1.</span></span>

<span data-ttu-id="ce967-109">[AGPM 4,0 SP1](agpm-40-sp1-navengl.md) prend en charge windows server 2012, windows Server 2008 R2, Windows 7, windows Server 2008 et Windows Vista avec SP1.</span><span class="sxs-lookup"><span data-stu-id="ce967-109">[AGPM 4.0 SP1](agpm-40-sp1-navengl.md) supports Windows Server 2012, Windows Server 2008 R2, Windows 7, Windows Server 2008, and Windows Vista with SP1.</span></span>

<span data-ttu-id="ce967-110">[AGPM 4](agpm-4-navengl.md) prend en charge windows Server 2008 R2, Windows 7, windows Server 2008 et Windows Vista avec SP1.</span><span class="sxs-lookup"><span data-stu-id="ce967-110">[AGPM 4](agpm-4-navengl.md) supports Windows Server 2008 R2, Windows 7, Windows Server 2008, and Windows Vista with SP1.</span></span>

<span data-ttu-id="ce967-111">[AGPM 3](agpm-3-navengl.md) prend en charge windows Server 2008 et Windows Vista avec SP1.</span><span class="sxs-lookup"><span data-stu-id="ce967-111">[AGPM 3](agpm-3-navengl.md) supports Windows Server 2008 and Windows Vista with SP1.</span></span>

<span data-ttu-id="ce967-112">[AGPM 2,5](agpm-25-navengl.md) prend en charge Windows Vista (32 bits) sans Service Pack et windows Server 2003 (32-bit).</span><span class="sxs-lookup"><span data-stu-id="ce967-112">[AGPM 2.5](agpm-25-navengl.md) supports Windows Vista (32-bit) with no service pack and Windows Server 2003 (32-bit).</span></span>

## <span data-ttu-id="ce967-113">Recommandations supplémentaires sur le produit MDOP</span><span class="sxs-lookup"><span data-stu-id="ce967-113">Supplemental MDOP Product Guidance</span></span>


<span data-ttu-id="ce967-114">Outre la documentation sur le produit disponible en ligne, des conseils supplémentaires sur le produit, tels que des vidéos d’information et des ateliers virtuels, sont disponibles pour la plupart des produits MDOP.</span><span class="sxs-lookup"><span data-stu-id="ce967-114">In addition to the product documentation available online, supplemental product guidance such as informational videos and virtual labs are available for most MDOP products.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="ce967-115">Laboratoires virtuels MDOP</span><span class="sxs-lookup"><span data-stu-id="ce967-115">MDOP Virtual Labs</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="ce967-116">Pour obtenir la liste des laboratoires virtuels MDOP disponibles, accédez aux <a href="https://go.microsoft.com/fwlink/?LinkId=234276" data-raw-source="[Microsoft Desktop Optimization Pack (MDOP) Virtual Labs](https://go.microsoft.com/fwlink/?LinkId=234276)"> ateliers virtuels Microsoft Desktop Optimization (MDOP) </a> ( <a href="https://go.microsoft.com/fwlink/?LinkId=234276" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=234276"> https://go.microsoft.com/fwlink/?LinkId=234276 </a> ).</span><span class="sxs-lookup"><span data-stu-id="ce967-116">For a list of available MDOP virtual labs, go to <a href="https://go.microsoft.com/fwlink/?LinkId=234276" data-raw-source="[Microsoft Desktop Optimization Pack (MDOP) Virtual Labs](https://go.microsoft.com/fwlink/?LinkId=234276)">Microsoft Desktop Optimization Pack (MDOP) Virtual Labs</a> (<a href="https://go.microsoft.com/fwlink/?LinkId=234276" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=234276">https://go.microsoft.com/fwlink/?LinkId=234276</a>).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="ce967-117">TechCenter MDOP</span><span class="sxs-lookup"><span data-stu-id="ce967-117">MDOP TechCenter</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="ce967-118">Pour en savoir plus sur les livres blancs, les supports d’évaluation, les blogs et les ressources MDOP supplémentaires, voir <a href="https://go.microsoft.com/fwlink/?LinkId=225286" data-raw-source="[MDOP TechCenter](https://go.microsoft.com/fwlink/?LinkId=225286)"> TechCenter de MDOP </a> ( <a href="https://go.microsoft.com/fwlink/?LinkId=225286" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=225286"> https://go.microsoft.com/fwlink/?LinkId=225286 </a> ).</span><span class="sxs-lookup"><span data-stu-id="ce967-118">For technical whitepapers, evaluation materials, blogs, and additional MDOP resources, go to <a href="https://go.microsoft.com/fwlink/?LinkId=225286" data-raw-source="[MDOP TechCenter](https://go.microsoft.com/fwlink/?LinkId=225286)">MDOP TechCenter</a> (<a href="https://go.microsoft.com/fwlink/?LinkId=225286" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=225286">https://go.microsoft.com/fwlink/?LinkId=225286</a>)</span></span></p>
<p></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-getmdop"></a><span data-ttu-id="ce967-119">Obtention de MDOP</span><span class="sxs-lookup"><span data-stu-id="ce967-119">How to Get MDOP</span></span>


<span data-ttu-id="ce967-120">MDOP est une suite de produits qui peut vous aider à rationaliser le déploiement, la gestion et l’assistance de bureau au sein de l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="ce967-120">MDOP is a suite of products that can help streamline desktop deployment, management, and support across the enterprise.</span></span> <span data-ttu-id="ce967-121">MDOP est disponible en tant qu’abonnement supplémentaire pour les clients Software Assurance.</span><span class="sxs-lookup"><span data-stu-id="ce967-121">MDOP is available as an additional subscription for Software Assurance customers.</span></span>

<a href="" id="evaluate-mdop"></a><span data-ttu-id="ce967-122">**Évaluer MDOP** MDOP est également disponible aux fins de test et d’évaluation pour les abonnés [MSDN](https://msdn.microsoft.com/subscriptions/downloads/default.aspx?PV=42:178) et [TechNet](https://technet.microsoft.com/subscriptions/downloads/default.aspx?PV=42:178) conformément aux contrats MSDN et TechNet.</span><span class="sxs-lookup"><span data-stu-id="ce967-122">**Evaluate MDOP** MDOP is also available for test and evaluation to [MSDN](https://msdn.microsoft.com/subscriptions/downloads/default.aspx?PV=42:178) and [TechNet](https://technet.microsoft.com/subscriptions/downloads/default.aspx?PV=42:178) subscribers in accordance with MSDN and TechNet agreements.</span></span>

<a href="" id="download-mdop"></a><span data-ttu-id="ce967-123">**Télécharger MDOP** Les abonnés MDOP peuvent télécharger le logiciel sur le site Web de gestion de [licences en volume Microsoft (MVLS)](https://go.microsoft.com/fwlink/?LinkId=166331).</span><span class="sxs-lookup"><span data-stu-id="ce967-123">**Download MDOP** MDOP subscribers can download the software at the [Microsoft Volume Licensing website (MVLS)](https://go.microsoft.com/fwlink/?LinkId=166331).</span></span>

<a href="" id="purchase-mdop"></a><span data-ttu-id="ce967-124">**Achat de MDOP** Pour plus d’informations sur l’achat de MDOP pour votre entreprise, consultez le site Web [d’achat](https://www.microsoft.com/windows/enterprise/how-to-buy.aspx) d’entreprise pour les entreprises.</span><span class="sxs-lookup"><span data-stu-id="ce967-124">**Purchase MDOP** Visit the enterprise [Purchase Windows Enterprise Licensing](https://www.microsoft.com/windows/enterprise/how-to-buy.aspx) website to find out how to purchase MDOP for your business.</span></span>

 

 





