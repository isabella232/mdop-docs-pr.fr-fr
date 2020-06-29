---
title: Réinitialisation d'un verrouillage TPM
description: Réinitialisation d'un verrouillage TPM
author: dansimp
ms.assetid: 91ec6666-1ae2-4e76-9459-ad65c405f639
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dde77a12e97d050777dac15d4106124ec111b3cd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804590"
---
# <span data-ttu-id="7ae74-103">Réinitialisation d'un verrouillage TPM</span><span class="sxs-lookup"><span data-stu-id="7ae74-103">How to Reset a TPM Lockout</span></span>


<span data-ttu-id="7ae74-104">La fonctionnalité de récupération de lecteur chiffrée de l’administration et de la surveillance de BitLocker (MBAM) englobe la capture et le stockage des données et la disponibilité des outils requis pour gérer le module de plateforme sécurisée (TPM).</span><span class="sxs-lookup"><span data-stu-id="7ae74-104">The Encrypted Drive Recovery feature of Microsoft BitLocker Administration and Monitoring (MBAM) encompasses both the capture and storage of data and the availability for tools that are required to manage the Trusted Platform Module (TPM).</span></span> <span data-ttu-id="7ae74-105">Cette rubrique traite de l’accès au système de données de récupération de clés centralisées dans le site Web d’administration des bits \ _admmon \ _tlanextref.</span><span class="sxs-lookup"><span data-stu-id="7ae74-105">This topic covers how to access the centralized Key Recovery data system in the bit\_admmon\_tlanextref administration website.</span></span> <span data-ttu-id="7ae74-106">Le système de données de récupération de clé peut fournir un fichier de mot de passe propriétaire du TPM lorsque l’identité de l’ordinateur et l’identificateur d’utilisateur associé sont fournis.</span><span class="sxs-lookup"><span data-stu-id="7ae74-106">The Key Recovery data system can provide a TPM owner password file when the computer identity and the associated user identifier are supplied.</span></span>

<span data-ttu-id="7ae74-107">Un verrouillage du TPM peut se produire si un utilisateur entre un code confidentiel incorrect trop souvent.</span><span class="sxs-lookup"><span data-stu-id="7ae74-107">A TPM lockout can occur if a user enters an incorrect PIN too many times.</span></span> <span data-ttu-id="7ae74-108">Le nombre de fois qu’un utilisateur peut entrer un code confidentiel incorrect avant que le verrouillage du TPM ne repose sur les spécifications du fabricant de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="7ae74-108">The number of times that a user can enter an incorrect PIN before the TPM lockout is based on the computer manufacturer's specification.</span></span>

**<span data-ttu-id="7ae74-109">Pour réinitialiser un verrouillage du TPM</span><span class="sxs-lookup"><span data-stu-id="7ae74-109">To reset a TPM lockout</span></span>**

1.  <span data-ttu-id="7ae74-110">Ouvrez le site Web d’administration MBAM.</span><span class="sxs-lookup"><span data-stu-id="7ae74-110">Open the MBAM administration website.</span></span>

2.  <span data-ttu-id="7ae74-111">Dans le volet de navigation, sélectionnez **gérer le module de plateforme sécurisée**.</span><span class="sxs-lookup"><span data-stu-id="7ae74-111">In the navigation pane, select **Manage TPM**.</span></span> <span data-ttu-id="7ae74-112">Cette opération ouvre la page **gérer le module de plateforme sécurisée** .</span><span class="sxs-lookup"><span data-stu-id="7ae74-112">This opens the **Manage TPM** page.</span></span>

3.  <span data-ttu-id="7ae74-113">Entrez le nom de domaine complet (FQDN) de l’ordinateur et le nom de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="7ae74-113">Enter the fully qualified domain name (FQDN) for the computer and the computer name.</span></span> <span data-ttu-id="7ae74-114">Entrez le domaine de connexion Windows de l’utilisateur et le nom d’utilisateur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7ae74-114">Enter the user’s Windows Logon domain and the user’s user name.</span></span> <span data-ttu-id="7ae74-115">Sélectionnez l’une des options prédéfinies dans la zone de liste déroulante **raison du demande de mot de passe de propriétaire du TPM** .</span><span class="sxs-lookup"><span data-stu-id="7ae74-115">Select one of the predefined options in the **Reason for requesting TPM owner password file** drop-down menu.</span></span> <span data-ttu-id="7ae74-116">Cliquez sur **Envoyer**.</span><span class="sxs-lookup"><span data-stu-id="7ae74-116">Click **Submit**.</span></span>

4.  <span data-ttu-id="7ae74-117">MBAM renverra l’une des valeurs suivantes:</span><span class="sxs-lookup"><span data-stu-id="7ae74-117">MBAM will return one of the following:</span></span>

    -   <span data-ttu-id="7ae74-118">Message d’erreur s’il n’existe aucun fichier de mot de passe de propriétaire de TPM correspondant</span><span class="sxs-lookup"><span data-stu-id="7ae74-118">An error message if no matching TPM owner password file is found</span></span>

    -   <span data-ttu-id="7ae74-119">Fichier de mot de passe du propriétaire du TPM de l’ordinateur soumis</span><span class="sxs-lookup"><span data-stu-id="7ae74-119">The TPM owner password file for the submitted computer</span></span>

    <span data-ttu-id="7ae74-120">**Remarques**  Si vous êtes un utilisateur expérimenté du support technique, les champs utilisateur et ID d’utilisateur ne sont pas obligatoires.</span><span class="sxs-lookup"><span data-stu-id="7ae74-120">**Note** If you are an Advanced Helpdesk User, the user domain and user ID fields are not required.</span></span>

     

5.  <span data-ttu-id="7ae74-121">Lorsque vous récupérez le mot de passe propriétaire, le mot de passe est affiché.</span><span class="sxs-lookup"><span data-stu-id="7ae74-121">Upon retrieval, the owner password is displayed.</span></span> <span data-ttu-id="7ae74-122">Pour enregistrer ce mot de passe dans un fichier. TPM, cliquez sur le bouton **Enregistrer** .</span><span class="sxs-lookup"><span data-stu-id="7ae74-122">To save this password to a .tpm file, click the **Save** button.</span></span>

6.  <span data-ttu-id="7ae74-123">L’utilisateur doit exécuter la console de gestion du TPM et sélectionner l’option de **réinitialisation du verrouillage du TPM** et fournir le fichier de mot de passe du propriétaire du TPM pour réinitialiser le verrouillage du TPM.</span><span class="sxs-lookup"><span data-stu-id="7ae74-123">The user will run the TPM management console and select the **Reset TPM lockout** option and provide the TPM owner password file to reset the TPM lockout.</span></span>

## <span data-ttu-id="7ae74-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7ae74-124">Related topics</span></span>


[<span data-ttu-id="7ae74-125">Gestion de BitLocker avec MBAM</span><span class="sxs-lookup"><span data-stu-id="7ae74-125">Performing BitLocker Management with MBAM</span></span>](performing-bitlocker-management-with-mbam.md)

 

 





