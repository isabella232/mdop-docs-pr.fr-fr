---
title: Réinitialisation d'un verrouillage TPM
description: Réinitialisation d'un verrouillage TPM
author: dansimp
ms.assetid: 20719ab2-18ae-4d3b-989a-539341909816
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6453473ec09c2033346c7e464c08dbfdfe046d47
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810925"
---
# <span data-ttu-id="cb82d-103">Réinitialisation d'un verrouillage TPM</span><span class="sxs-lookup"><span data-stu-id="cb82d-103">How to Reset a TPM Lockout</span></span>


<span data-ttu-id="cb82d-104">La fonctionnalité de récupération de lecteur chiffrée de l’administration et de la surveillance de BitLocker (MBAM) englobe la capture et le stockage des données ainsi que la disponibilité des outils nécessaires pour gérer le module de plateforme sécurisée (TPM).</span><span class="sxs-lookup"><span data-stu-id="cb82d-104">The Encrypted Drive Recovery feature of Microsoft BitLocker Administration and Monitoring (MBAM) encompasses both the capture and storage of data and the availability for tools that are needed to manage the Trusted Platform Module (TPM).</span></span> <span data-ttu-id="cb82d-105">Cette rubrique décrit comment accéder au système de données de récupération de clés centralisées dans le site Web d’administration et de surveillance, qui peut fournir un fichier de mots de passe de propriétaire du TPM lorsqu’un ID d’ordinateur et un identificateur d’utilisateur associé sont fournis.</span><span class="sxs-lookup"><span data-stu-id="cb82d-105">This topic covers how to access the centralized Key Recovery data system in the Administration and Monitoring website, which can provide a TPM owner password file when a computer ID and associated user identifier are supplied.</span></span>

<span data-ttu-id="cb82d-106">Un verrouillage du TPM peut se produire si un utilisateur entre un code confidentiel incorrect trop souvent.</span><span class="sxs-lookup"><span data-stu-id="cb82d-106">A TPM lockout can occur if a user enters the incorrect PIN too many times.</span></span> <span data-ttu-id="cb82d-107">Le nombre de fois qu’un utilisateur peut entrer un code confidentiel incorrect avant que les verrouillages du TPM ne varient d’un fabricant au fabricant.</span><span class="sxs-lookup"><span data-stu-id="cb82d-107">The number of times that a user can enter an incorrect PIN before the TPM locks varies from manufacturer to manufacturer.</span></span>

<span data-ttu-id="cb82d-108">Vous pouvez réinitialiser un verrouillage du TPM uniquement si MBAM possède le module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="cb82d-108">You can reset a TPM lockout only if MBAM owns the TPM.</span></span>

**<span data-ttu-id="cb82d-109">Pour réinitialiser un verrouillage du TPM</span><span class="sxs-lookup"><span data-stu-id="cb82d-109">To reset a TPM lockout</span></span>**

1.  <span data-ttu-id="cb82d-110">Ouvrez un navigateur Web, puis accédez au site Web d’administration et de surveillance.</span><span class="sxs-lookup"><span data-stu-id="cb82d-110">Open a web browser and navigate to the Administration and Monitoring website.</span></span>

2.  <span data-ttu-id="cb82d-111">Dans le volet de navigation gauche, sélectionnez **gérer le TPM** pour ouvrir la page gérer le module de **plateforme sécurisée** .</span><span class="sxs-lookup"><span data-stu-id="cb82d-111">In the left navigation pane, select **Manage TPM** to open the **Manage TPM** page.</span></span>

3.  <span data-ttu-id="cb82d-112">Entrez le nom de domaine complet de l’ordinateur et le nom de l’ordinateur, puis entrez le domaine de connexion Windows de l’utilisateur et le nom d’utilisateur de l’utilisateur pour récupérer le fichier de mot de passe du propriétaire du module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="cb82d-112">Enter the fully qualified domain name for the computer and the computer name, and enter the user’s Windows logon domain and the user’s user name to retrieve the TPM owner password file.</span></span>

4.  <span data-ttu-id="cb82d-113">Dans la liste des **fichiers de mots de passe du propriétaire du module de plateforme sécurisée** , sélectionnez une raison pour la demande, puis cliquez sur **valider**.</span><span class="sxs-lookup"><span data-stu-id="cb82d-113">From the **Reason for requesting TPM owner password file** list, select a reason for the request, and click **Submit**.</span></span>

    <span data-ttu-id="cb82d-114">MBAM renvoie l’une des valeurs suivantes:</span><span class="sxs-lookup"><span data-stu-id="cb82d-114">MBAM returns one of the following:</span></span>

    -   <span data-ttu-id="cb82d-115">Un message d’erreur s’il n’existe aucun fichier de mot de passe de propriétaire de TPM correspondant</span><span class="sxs-lookup"><span data-stu-id="cb82d-115">An error message, if no matching TPM owner password file is found</span></span>

    -   <span data-ttu-id="cb82d-116">Fichier de mot de passe du propriétaire du TPM de l’ordinateur soumis</span><span class="sxs-lookup"><span data-stu-id="cb82d-116">The TPM owner password file for the submitted computer</span></span>

    **<span data-ttu-id="cb82d-117">Remarque</span><span class="sxs-lookup"><span data-stu-id="cb82d-117">Note</span></span>**  
    <span data-ttu-id="cb82d-118">Si vous êtes un utilisateur expérimenté du support technique, les champs utilisateur et ID d’utilisateur ne sont pas obligatoires.</span><span class="sxs-lookup"><span data-stu-id="cb82d-118">If you are an Advanced Helpdesk user, the user domain and user ID fields are not required.</span></span>



~~~
After the TPM owner password is retrieved, the owner password is displayed.
~~~

5. <span data-ttu-id="cb82d-119">Pour enregistrer le mot de passe dans un fichier. TPM, cliquez sur le bouton **Enregistrer** .</span><span class="sxs-lookup"><span data-stu-id="cb82d-119">To save the password to a .tpm file, click the **Save** button.</span></span>

   <span data-ttu-id="cb82d-120">L’utilisateur exécutera la console de gestion du module de plateforme sécurisée, sélectionner l’option de **réinitialisation du verrouillage du TPM** et fournir le fichier de mot de passe du propriétaire du TPM pour réinitialiser le verrouillage du TPM.</span><span class="sxs-lookup"><span data-stu-id="cb82d-120">The user will run the TPM management console, select the **Reset TPM lockout** option, and provide the TPM owner password file to reset the TPM lockout.</span></span>

   **<span data-ttu-id="cb82d-121">Important</span><span class="sxs-lookup"><span data-stu-id="cb82d-121">Important</span></span>**  
   <span data-ttu-id="cb82d-122">Les administrateurs du support technique ne doivent pas donner à la valeur de hachage du TPM ou au fichier de mot de passe du propriétaire du TPM les utilisateurs finaux.</span><span class="sxs-lookup"><span data-stu-id="cb82d-122">Help Desk administrators should not give the TPM hash value or TPM owner password file to end users.</span></span> <span data-ttu-id="cb82d-123">Les informations sur le TPM ne changent pas, ce qui peut entraîner un risque de sécurité si le fichier est fourni aux utilisateurs finaux.</span><span class="sxs-lookup"><span data-stu-id="cb82d-123">The TPM information does not change, so it could pose a security risk if the file is given to end users.</span></span>



## <span data-ttu-id="cb82d-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="cb82d-124">Related topics</span></span>


[<span data-ttu-id="cb82d-125">Gestion de BitLocker avec MBAM</span><span class="sxs-lookup"><span data-stu-id="cb82d-125">Performing BitLocker Management with MBAM</span></span>](performing-bitlocker-management-with-mbam-mbam-2.md)









