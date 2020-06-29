---
title: Notes de publication pour App-V5.0
description: Notes de publication pour App-V5.0
author: dansimp
ms.assetid: 68a6a5a1-4b3c-4c09-b00c-9ca4237695d5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e49f6072d738b45afe25de24f2ee9a2d09d64a2e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804890"
---
# <span data-ttu-id="27173-103">Notes de publication pour App-V5.0</span><span class="sxs-lookup"><span data-stu-id="27173-103">Release Notes for App-V 5.0</span></span>


**<span data-ttu-id="27173-104">Pour rechercher un problème spécifique dans ces notes de publication, appuyez sur CTRL + F.</span><span class="sxs-lookup"><span data-stu-id="27173-104">To search for a specific issue in these release notes, press CTRL+F.</span></span>**

<span data-ttu-id="27173-105">Lisez attentivement ces notes de publication avant d’installer App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="27173-105">Read these release notes thoroughly before you install App-V 5.0.</span></span>

<span data-ttu-id="27173-106">Ces notes de publication contiennent des informations requises pour l’installation de l’application-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="27173-106">These release notes contain information that is required to successfully install App-V 5.0.</span></span> <span data-ttu-id="27173-107">Les notes de publication contiennent également des informations qui ne sont pas disponibles dans la documentation du produit.</span><span class="sxs-lookup"><span data-stu-id="27173-107">The release notes also contain information that is not available in the product documentation.</span></span> <span data-ttu-id="27173-108">S’il existe une différence entre ces notes de publication et d’autres documents App-V 5,0, la dernière modification doit être considérée comme faisant autorité.</span><span class="sxs-lookup"><span data-stu-id="27173-108">If there is a difference between these release notes and other App-V 5.0 documentation, the latest change should be considered authoritative.</span></span> <span data-ttu-id="27173-109">Ces notes de publication remplacent le contenu qui est inclus dans ce produit.</span><span class="sxs-lookup"><span data-stu-id="27173-109">These release notes supersede the content that is included with this product.</span></span>

## <span data-ttu-id="27173-110">À propos de la documentation relative aux produits</span><span class="sxs-lookup"><span data-stu-id="27173-110">About the Product Documentation</span></span>


<span data-ttu-id="27173-111">Pour plus d’informations sur la documentation App-V 5,0, consultez la page d’accueil App-V 5,0 sur Microsoft TechNet.</span><span class="sxs-lookup"><span data-stu-id="27173-111">For information about App-V 5.0 documentation, see the App-V 5.0 home page on Microsoft TechNet.</span></span>

## <span data-ttu-id="27173-112">Fournir des commentaires</span><span class="sxs-lookup"><span data-stu-id="27173-112">Provide Feedback</span></span>


<span data-ttu-id="27173-113">Vos commentaires vous intéressent sur App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="27173-113">We are interested in your feedback on App-V 5.0.</span></span> <span data-ttu-id="27173-114">Vous pouvez envoyer vos commentaires à <mdopdocs@microsoft.com> .</span><span class="sxs-lookup"><span data-stu-id="27173-114">You can send your feedback to <mdopdocs@microsoft.com>.</span></span>

<span data-ttu-id="27173-115">**Remarques**  Cette adresse de messagerie n’est pas un canal de support, mais vos commentaires nous aideront à planifier des changements ultérieurs dans la documentation et les versions de nos produits.</span><span class="sxs-lookup"><span data-stu-id="27173-115">**Note** This email address is not a support channel, but your feedback will help us to plan for future changes in our documentation and product releases.</span></span>

 

<span data-ttu-id="27173-116">Pour obtenir les informations les plus récentes sur MDOP et les ressources de formation supplémentaires, voir la page d' [utilisation de MDOP](https://go.microsoft.com/fwlink/p/?LinkId=236032) .</span><span class="sxs-lookup"><span data-stu-id="27173-116">For the latest information about MDOP and additional learning resources, see the [MDOP Information Experience](https://go.microsoft.com/fwlink/p/?LinkId=236032) page.</span></span>

<span data-ttu-id="27173-117">Pour en savoir plus sur les nouvelles mises à jour ou pour nous faire part de vos commentaires, suivez-nous sur [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) ou [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447).</span><span class="sxs-lookup"><span data-stu-id="27173-117">For more information about new updates or to provide feedback, follow us on [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) or [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447).</span></span>

## <span data-ttu-id="27173-118">Problèmes connus avec App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="27173-118">Known Issues with App-V 5.0</span></span>


<span data-ttu-id="27173-119">Cette section contient des notes de publication relatives aux problèmes connus avec App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="27173-119">This section contains release notes about the known issues with App-V 5.0.</span></span>

### <span data-ttu-id="27173-120">Impossible d’arrêter l’ajout de packages lors de l’utilisation des cmdlets PowerShell du serveur</span><span class="sxs-lookup"><span data-stu-id="27173-120">Unable to terminate adding packages when using server PowerShell cmdlets</span></span>

<span data-ttu-id="27173-121">Lorsque vous ajoutez un package à l’aide de PowerShell, il n’existe aucune méthode de fermeture pour ajouter de nouveaux packages.</span><span class="sxs-lookup"><span data-stu-id="27173-121">When you add a package using PowerShell, there is no method to exit adding new packages.</span></span>

<span data-ttu-id="27173-122">Solution de contournement: pour arrêter l’ajout de packages, appuyez sur **entrée** après avoir ajouté le package final.</span><span class="sxs-lookup"><span data-stu-id="27173-122">WORKAROUND: To stop adding packages, press **enter** after you have added the final package.</span></span>

### <a href="" id="-------------app-v-5-0-client-rejects-packages-from-servers-whose-ssl-certificate-has-been-revoked"></a> <span data-ttu-id="27173-123">Le client App-V 5,0 rejette les packages des serveurs dont le certificat SSL a été révoqué</span><span class="sxs-lookup"><span data-stu-id="27173-123">App-V 5.0 client rejects packages from servers whose SSL certificate has been revoked</span></span>

<span data-ttu-id="27173-124">Dans le cadre de l’utilisation du protocole HTTPs, le client App-V 5,0 refusera par défaut les packages des serveurs dont le certificat SSL a été révoqué.</span><span class="sxs-lookup"><span data-stu-id="27173-124">When using the HTTPS protocol, the App-V 5.0 client will by default reject packages from servers whose SSL certificate has been revoked.</span></span> <span data-ttu-id="27173-125">Ce comportement peut être désactivé à l’aide de la configuration en modifiant le paramètre **VerifyCertificateRevocationList** .</span><span class="sxs-lookup"><span data-stu-id="27173-125">This behavior can be turned off through configuration by modifying the **VerifyCertificateRevocationList** setting.</span></span> <span data-ttu-id="27173-126">L’application d’une nouvelle configuration pour ce paramètre n’est pas appliquée tant que le service App-V 5,0 n’est pas redémarré.</span><span class="sxs-lookup"><span data-stu-id="27173-126">Applying new configuration for this setting will not take effect until the App-V 5.0 service is restarted.</span></span>

<span data-ttu-id="27173-127">Solution de contournement: redémarrez le service App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="27173-127">WORKAROUND: Restart the App-V 5.0 service.</span></span>

## <span data-ttu-id="27173-128">Informations de copyright des notes de publication</span><span class="sxs-lookup"><span data-stu-id="27173-128">Release Notes Copyright Information</span></span>


<span data-ttu-id="27173-129">Microsoft, Active Directory, ActiveX, Bing, Excel, Silverlight, SQLServer, Windows, MicrosoftIntune et WindowsPowerShell sont des marques commerciales du groupe de sociétés Microsoft.</span><span class="sxs-lookup"><span data-stu-id="27173-129">Microsoft, Active Directory, ActiveX, Bing, Excel, Silverlight, SQLServer, Windows, MicrosoftIntune, and WindowsPowerShell are trademarks of the Microsoft group of companies.</span></span> <span data-ttu-id="27173-130">Toutes les autres marques déposées sont la propriété de leurs détenteurs respectifs.</span><span class="sxs-lookup"><span data-stu-id="27173-130">All other trademarks are property of their respective owners.</span></span>








## <span data-ttu-id="27173-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="27173-131">Related topics</span></span>


[<span data-ttu-id="27173-132">À propos d'App-V5.0</span><span class="sxs-lookup"><span data-stu-id="27173-132">About App-V 5.0</span></span>](about-app-v-50.md)

 

 





