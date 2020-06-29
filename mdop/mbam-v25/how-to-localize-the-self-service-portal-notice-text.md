---
title: Comment localiser le texte d'avis du portail libre-service
description: Comment localiser le texte d'avis du portail libre-service
author: dansimp
ms.assetid: a4c878b7-e5c8-45af-a537-761bb2991659
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a2385f6b00713e7373bd1707b02324b80f300c0d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811921"
---
# <span data-ttu-id="ec975-103">Comment localiser le texte d'avis du portail libre-service</span><span class="sxs-lookup"><span data-stu-id="ec975-103">How to Localize the Self-Service Portal Notice Text</span></span>


<span data-ttu-id="ec975-104">Vous pouvez configurer le texte des notifications localisées pour qu’ils apparaissent par défaut aux utilisateurs finaux sur le portail libre-service.</span><span class="sxs-lookup"><span data-stu-id="ec975-104">You can configure localized notice text to display to end users by default in the Self-Service Portal.</span></span> <span data-ttu-id="ec975-105">Le fichier Notice.txt qui affiche le texte de l’avis figure dans le répertoire racine suivant:</span><span class="sxs-lookup"><span data-stu-id="ec975-105">The Notice.txt file that displays the notice text is in the following root directory:</span></span>

<span data-ttu-id="ec975-106">&lt;Répertoire d’installation *de MBAM self-service* &gt; \\Self service Website</span><span class="sxs-lookup"><span data-stu-id="ec975-106">&lt;*MBAM Self-Service Install Directory*&gt;\\Self Service Website</span></span>\\

<span data-ttu-id="ec975-107">Pour afficher un texte d’avis localisé, vous devez créer un fichier Notice.txt localisé, puis l’enregistrer sous un dossier de langue spécifique dans le répertoire de l’exemple suivant:</span><span class="sxs-lookup"><span data-stu-id="ec975-107">To display localized notice text, you create a localized Notice.txt file, and then save it under a specific language folder in the following example directory:</span></span>

<span data-ttu-id="ec975-108">&lt;Répertoire d’installation *de MBAM self-service* &gt; \\Self service Website</span><span class="sxs-lookup"><span data-stu-id="ec975-108">&lt;*MBAM Self-Service Install Directory*&gt;\\Self Service Website</span></span>\\

<span data-ttu-id="ec975-109">**Remarques**  Vous pouvez configurer le chemin d’accès à l’aide de l’élément **NoticeTextPath** dans les paramètres de l' **application**.</span><span class="sxs-lookup"><span data-stu-id="ec975-109">**Note** You can configure the path by using the **NoticeTextPath** item in **Application Settings**.</span></span>

 

<span data-ttu-id="ec975-110">MBAM affiche le texte de l’avis en fonction des règles suivantes:</span><span class="sxs-lookup"><span data-stu-id="ec975-110">MBAM displays the notice text, based on the following rules:</span></span>

-   <span data-ttu-id="ec975-111">Si vous créez un fichier **Notice.txt** localisé dans le dossier de langue approprié, MBAM affiche le texte du message localisé si le fichier **Notice.txt** par défaut existe.</span><span class="sxs-lookup"><span data-stu-id="ec975-111">If you create a localized **Notice.txt** file in the appropriate language folder, MBAM displays the localized notice text if the default **Notice.txt** file exists.</span></span> <span data-ttu-id="ec975-112">Si le fichier **Notice.txt** par défaut est manquant, un message s’affiche, indiquant que le fichier par défaut est manquant.</span><span class="sxs-lookup"><span data-stu-id="ec975-112">If the default **Notice.txt** file is missing, a message displays indicating that the default file is missing.</span></span>

-   <span data-ttu-id="ec975-113">Si MBAM ne trouve pas de version localisée du fichier Notice.txt, il affiche le texte dans le fichier de Notice.txt par défaut.</span><span class="sxs-lookup"><span data-stu-id="ec975-113">If MBAM does not find a localized version of the Notice.txt file, it displays the text in the default Notice.txt file.</span></span>

-   <span data-ttu-id="ec975-114">Si MBAM ne trouve pas de fichier Notice.txt par défaut, il affiche le texte par défaut dans le portail libre-service.</span><span class="sxs-lookup"><span data-stu-id="ec975-114">If MBAM does not find a default Notice.txt file, it displays the default text in the Self-Service Portal.</span></span>

<span data-ttu-id="ec975-115">**Remarques**  Si le navigateur d’un utilisateur final est défini sur une langue qui ne possède pas de sous-dossier de langue correspondant ou Notice.txt, le texte du fichier Notice.txt dans le répertoire racine suivant s’affiche:</span><span class="sxs-lookup"><span data-stu-id="ec975-115">**Note** If an end user’s browser is set to a language that does not have a corresponding language subfolder or Notice.txt, the text in the Notice.txt file in the following root directory is displayed:</span></span>

<span data-ttu-id="ec975-116">&lt;Répertoire d’installation *de MBAM self-service* &gt; \\Self service Website</span><span class="sxs-lookup"><span data-stu-id="ec975-116">&lt;*MBAM Self-Service Install Directory*&gt;\\Self Service Website</span></span>\\

 

**<span data-ttu-id="ec975-117">Pour créer un fichier Notice.txt localisé</span><span class="sxs-lookup"><span data-stu-id="ec975-117">To create a localized Notice.txt file</span></span>**

1.  <span data-ttu-id="ec975-118">Sur le serveur sur lequel vous avez configuré le portail libre-service, créez un &lt; *Language* &gt; dossier de langue dans l’exemple d’annuaire suivant, où &lt; *Language* &gt; représente le nom de la langue localisée:</span><span class="sxs-lookup"><span data-stu-id="ec975-118">On the server where you configured the Self-Service Portal, create a &lt;*Language*&gt; folder in the following example directory, where &lt;*Language*&gt; represents the name of the localized language:</span></span>

    <span data-ttu-id="ec975-119">&lt;Répertoire d’installation *de MBAM self-service* &gt; \\Self service Website</span><span class="sxs-lookup"><span data-stu-id="ec975-119">&lt;*MBAM Self-Service Install Directory*&gt;\\Self Service Website</span></span>\\

    <span data-ttu-id="ec975-120">**Remarques**  Certains dossiers de langue existent déjà, il est donc possible que vous n’ayez pas à créer de dossier.</span><span class="sxs-lookup"><span data-stu-id="ec975-120">**Note** Some language folders already exist, so you might not have to create a folder.</span></span> <span data-ttu-id="ec975-121">Si vous avez besoin de créer un dossier de langue, reportez-vous à la rubrique référence sur l' [API NLS (National Language Support)](https://go.microsoft.com/fwlink/?LinkId=317947) pour obtenir la liste des noms valides que vous pouvez utiliser pour le &lt; dossier *Language* &gt; .</span><span class="sxs-lookup"><span data-stu-id="ec975-121">If you do have to create a language folder, see [National Language Support (NLS) API Reference](https://go.microsoft.com/fwlink/?LinkId=317947) for a list of the valid names that you can use for the &lt;*Language*&gt; folder.</span></span>

     

2.  <span data-ttu-id="ec975-122">Créez un fichier Notice.txt contenant le texte d’avis localisé.</span><span class="sxs-lookup"><span data-stu-id="ec975-122">Create a Notice.txt file that contains the localized notice text.</span></span>

3.  <span data-ttu-id="ec975-123">Enregistrez le fichier Notice.txt dans le &lt; dossier *Language* &gt; .</span><span class="sxs-lookup"><span data-stu-id="ec975-123">Save the Notice.txt file in the &lt;*Language*&gt; folder.</span></span> <span data-ttu-id="ec975-124">Par exemple, pour créer un fichier Notice.txt localisé en espagnol, enregistrez le fichier de Notice.txt localisé dans le répertoire de l’exemple suivant:</span><span class="sxs-lookup"><span data-stu-id="ec975-124">For example, to create a localized Notice.txt file in Spanish, save the localized Notice.txt file in the following example directory:</span></span>

    <span data-ttu-id="ec975-125">&lt;Répertoire d’installation *de MBAM self-service* &gt; \\Self service Website\\Es-es</span><span class="sxs-lookup"><span data-stu-id="ec975-125">&lt;*MBAM Self-Service Install Directory*&gt;\\Self Service Website\\Es-es</span></span>

    <span data-ttu-id="ec975-126">Le nom du dossier Language peut également être le nom neutre des langues **au lieu** de **es-es**.</span><span class="sxs-lookup"><span data-stu-id="ec975-126">The name of the Language folder can also be the language neutral name **es** instead of **es-es**.</span></span> <span data-ttu-id="ec975-127">Si le navigateur de l’utilisateur final est défini sur **es-es** et que ce dossier n’existe pas, les paramètres régionaux du parent (tels qu’ils sont définis dans .net) sont récupérés et activés de manière récursive, ce qui a\\SelfServiceWebsite\\es\\Notice.txt pour effet d’arrêter &lt; &gt; le fichier de Notice.txt par défaut.</span><span class="sxs-lookup"><span data-stu-id="ec975-127">If the end user’s browser is set to **es-es** and that folder does not exist, the parent locale (as defined in .NET) is recursively retrieved and checked, resolving to &lt;MBAM Self-Service Install Directory&gt;\\SelfServiceWebsite\\es\\Notice.txt before finally becoming the default Notice.txt file.</span></span> <span data-ttu-id="ec975-128">Cette substitution récursive imite les règles de chargement des ressources .NET.</span><span class="sxs-lookup"><span data-stu-id="ec975-128">This recursive fallback mimics the .NET resource loading rules.</span></span>



## <span data-ttu-id="ec975-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ec975-129">Related topics</span></span>


[<span data-ttu-id="ec975-130">Personnalisation du portail libre-service de votre organisation</span><span class="sxs-lookup"><span data-stu-id="ec975-130">Customizing the Self-Service Portal for Your Organization</span></span>](customizing-the-self-service-portal-for-your-organization.md)

 

## <span data-ttu-id="ec975-131">Vous avez une suggestion pour MBAM?</span><span class="sxs-lookup"><span data-stu-id="ec975-131">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="ec975-132">Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)</span><span class="sxs-lookup"><span data-stu-id="ec975-132">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="ec975-133">Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="ec975-133">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





