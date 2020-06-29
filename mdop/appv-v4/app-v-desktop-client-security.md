---
title: Sécurité d'App-V Desktop Client
description: Sécurité d'App-V Desktop Client
author: dansimp
ms.assetid: 216b9c16-7bb4-4f94-b9d8-810501285008
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 26add6f855780113613cf1591c41722643954477
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809282"
---
# <span data-ttu-id="a55a7-103">Sécurité d'App-V Desktop Client</span><span class="sxs-lookup"><span data-stu-id="a55a7-103">App-V Desktop Client Security</span></span>


<span data-ttu-id="a55a7-104">Le client de bureau App-V fournit de nombreuses améliorations liées à la sécurité qui ne sont pas disponibles dans les versions précédentes du produit.</span><span class="sxs-lookup"><span data-stu-id="a55a7-104">The App-V Desktop Client provides many security enhancements that were not available in previous versions of the product.</span></span> <span data-ttu-id="a55a7-105">Ces modifications fournissent des niveaux de sécurité plus élevés par défaut et par le biais de la configuration des paramètres du client.</span><span class="sxs-lookup"><span data-stu-id="a55a7-105">These changes provide higher levels of security by default and through configuration of the client settings.</span></span>

<span data-ttu-id="a55a7-106">**Remarques**  Lorsque vous installez le client de bureau App-V sur un ordinateur, le logiciel utilise par défaut les paramètres les plus sécurisés.</span><span class="sxs-lookup"><span data-stu-id="a55a7-106">**Note** When you install the App-V Desktop Client on a computer, the software defaults to the most secure settings.</span></span> <span data-ttu-id="a55a7-107">Toutefois, lors de la mise à niveau, les paramètres précédents du client persistent.</span><span class="sxs-lookup"><span data-stu-id="a55a7-107">However, when upgrading, the previous settings of the client persist.</span></span>

 

<span data-ttu-id="a55a7-108">Par défaut, le client de bureau App-V est configuré uniquement avec les autorisations nécessaires pour permettre à un utilisateur non administratif d’effectuer une actualisation de publication et des applications de flux.</span><span class="sxs-lookup"><span data-stu-id="a55a7-108">By default, the App-V Desktop Client is configured only with the permissions required to allow a non-administrative user to perform a publishing refresh and stream applications.</span></span> <span data-ttu-id="a55a7-109">D’autres améliorations apportées à la sécurité fournies dans le client de bureau App-V incluent les éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="a55a7-109">Additional security enhancements provided in the App-V Desktop Client include the following:</span></span>

-   <span data-ttu-id="a55a7-110">Par défaut, la mise à jour du cache OSD est autorisée uniquement par le processus d’actualisation de la publication.</span><span class="sxs-lookup"><span data-stu-id="a55a7-110">By default, an OSD cache update is allowed only by the publishing refresh process.</span></span>

-   <span data-ttu-id="a55a7-111">Le fichier journal ( `sftlog.txt` ) est accessible uniquement par les comptes disposant d’un accès administratif local au client.</span><span class="sxs-lookup"><span data-stu-id="a55a7-111">The log file (`sftlog.txt`) is accessible only by accounts with local administrative access to the client.</span></span>

-   <span data-ttu-id="a55a7-112">La taille du fichier journal est désormais maximale.</span><span class="sxs-lookup"><span data-stu-id="a55a7-112">The log file now has a maximum size.</span></span>

-   <span data-ttu-id="a55a7-113">Les fichiers journaux sont gérés par le biais des paramètres d’archivage.</span><span class="sxs-lookup"><span data-stu-id="a55a7-113">The log files are managed through archive settings.</span></span>

-   <span data-ttu-id="a55a7-114">La journalisation des événements système est désormais effectuée.</span><span class="sxs-lookup"><span data-stu-id="a55a7-114">System Event logging is now performed.</span></span>

## <span data-ttu-id="a55a7-115">Autorisations</span><span class="sxs-lookup"><span data-stu-id="a55a7-115">Permissions</span></span>


<span data-ttu-id="a55a7-116">Après avoir installé le client de bureau, vous pouvez configurer d’autres paramètres de sécurité via la console MMC ou sur un client individuel à l’aide du registre ou du modèle ADM fourni par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a55a7-116">After you install the Desktop Client, you can configure other security settings through the MMC, or on an individual client by using the registry or the ADM Template provided by Microsoft.</span></span> <span data-ttu-id="a55a7-117">Le client de bureau App-V dispose d’autorisations que vous pouvez définir pour limiter les utilisateurs non administrateurs à l’accès à toutes les fonctionnalités du client de bureau.</span><span class="sxs-lookup"><span data-stu-id="a55a7-117">The App-V Desktop Client has permissions that you can set to restrict non-administrative users from accessing all the features of the Desktop Client.</span></span> <span data-ttu-id="a55a7-118">Pour obtenir la liste complète des autorisations, voir le fichier d’aide du client App-V ou le Guide de fonctionnement de l’application-v.</span><span class="sxs-lookup"><span data-stu-id="a55a7-118">For a full list of permissions, please see the App-V Client Help file or App-V Operations Guide.</span></span>

<span data-ttu-id="a55a7-119">**Important**  Prenez soigneusement en considération les conséquences du changement de droits d’accès, en particulier sur les systèmes partagés par plusieurs utilisateurs, tels que les serveurs de terminaux.</span><span class="sxs-lookup"><span data-stu-id="a55a7-119">**Important** Carefully consider the consequences of changing access rights, especially on systems that are shared by multiple users, such as Terminal Servers.</span></span>

 

<span data-ttu-id="a55a7-120">**Remarques**  Si les utilisateurs de l’environnement disposent de privilèges d’administrateur local sur leurs ordinateurs, les autorisations ne sont pas prises en compte.</span><span class="sxs-lookup"><span data-stu-id="a55a7-120">**Note** If users in the environment have local administrator privileges for their computers, the permissions are ignored.</span></span>

 

### <span data-ttu-id="a55a7-121">Modèle ADM</span><span class="sxs-lookup"><span data-stu-id="a55a7-121">ADM Template</span></span>

<span data-ttu-id="a55a7-122">Microsoft Application Virtualization (App-V) introduit un modèle ADM qui vous permet de configurer les paramètres de client les plus courants par le biais des stratégies de groupe.</span><span class="sxs-lookup"><span data-stu-id="a55a7-122">Microsoft Application Virtualization (App-V) introduces an ADM Template that you can use to configure the most common client settings through Group Policies.</span></span> <span data-ttu-id="a55a7-123">Ce modèle permet aux administrateurs d’implémenter et de modifier un grand nombre des paramètres du client par le biais d’un modèle d’administration centralisée.</span><span class="sxs-lookup"><span data-stu-id="a55a7-123">This template enables administrators to implement and change many of the client settings through a centralized administration model.</span></span> <span data-ttu-id="a55a7-124">Certains des paramètres disponibles dans le modèle ADM sont paramètres de sécurité.</span><span class="sxs-lookup"><span data-stu-id="a55a7-124">Some of the settings available in the ADM Template are security settings.</span></span>

<span data-ttu-id="a55a7-125">**Important**  Lorsque vous utilisez le modèle ADM, souvenez-vous que les paramètres sont des paramètres de préférence de stratégie de groupe et pas de stratégies de groupe entièrement gérées.</span><span class="sxs-lookup"><span data-stu-id="a55a7-125">**Important** When using the ADM Template, remember that the settings are Group Policy preference settings and not fully managed Group Policies.</span></span>

 

<span data-ttu-id="a55a7-126">Pour obtenir une description complète du modèle ADM, des paramètres spécifiques et des recommandations pour le déploiement réussi de vos clients dans votre environnement, voir le livre blanc sur le modèle application-V ADM à l’adresse [https://go.microsoft.com/fwlink/LinkId=122063](https://go.microsoft.com/fwlink/?LinkId=122063) .</span><span class="sxs-lookup"><span data-stu-id="a55a7-126">For a full description of the ADM Template, the specific settings, and guidance to successfully deploy clients in your environment, see the App-V ADM Template white paper at [https://go.microsoft.com/fwlink/LinkId=122063](https://go.microsoft.com/fwlink/?LinkId=122063).</span></span>

## <span data-ttu-id="a55a7-127">Supprimer des associations de types de fichiers OSD</span><span class="sxs-lookup"><span data-stu-id="a55a7-127">Removing OSD File Type Associations</span></span>


<span data-ttu-id="a55a7-128">Si votre organisation n’a pas besoin d’ouvrir des applications directement à partir d’un fichier OSD, vous pouvez améliorer la sécurité en supprimant les associations de types de fichiers sur le client.</span><span class="sxs-lookup"><span data-stu-id="a55a7-128">If your organization does not require users to open applications directly from an OSD file, you can enhance security by removing the file type associations on the client.</span></span> <span data-ttu-id="a55a7-129">Supprimez les `HKEY_CURRENT_USERS` clés pour l’OSD et `Softgird.osd.file` en utilisant l’éditeur du Registre.</span><span class="sxs-lookup"><span data-stu-id="a55a7-129">Remove the `HKEY_CURRENT_USERS` keys for OSD and `Softgird.osd.file` by using the registry editor.</span></span> <span data-ttu-id="a55a7-130">Vous pouvez placer ce processus dans un script d’ouverture de session ou dans un script de post-installation pour automatiser ces modifications.</span><span class="sxs-lookup"><span data-stu-id="a55a7-130">You can put this process into a logon script or into a post-installation script to automate these changes.</span></span>

 

 





