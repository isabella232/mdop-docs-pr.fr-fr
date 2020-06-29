---
title: Comment localiser l'URL «HelpdeskURL» du portail libre-service
description: Comment localiser l'URL «HelpdeskURL» du portail libre-service
author: dansimp
ms.assetid: 86798460-077b-459b-8d54-4b605e07d2f1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 0d7ec4ce87bbe5aab56e9fa877ced5f51625a5dc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811916"
---
# <span data-ttu-id="03c45-103">Comment localiser l'URL «HelpdeskURL» du portail libre-service</span><span class="sxs-lookup"><span data-stu-id="03c45-103">How to Localize the Self-Service Portal “HelpdeskURL”</span></span>


<span data-ttu-id="03c45-104">Vous pouvez configurer une version localisée de l’URL du portail libre-service pour l’afficher par défaut aux utilisateurs finaux.</span><span class="sxs-lookup"><span data-stu-id="03c45-104">You can configure a localized version of the Self-Service Portal URL to display to end users by default.</span></span> <span data-ttu-id="03c45-105">L’URL du portail libre-service est représentée par le paramètre **HelpdeskURL**.</span><span class="sxs-lookup"><span data-stu-id="03c45-105">The Self-Service Portal URL is represented by the parameter **HelpdeskURL**.</span></span>

<span data-ttu-id="03c45-106">Si vous créez une version localisée, comme décrit dans les instructions ci-dessous, Microsoft BitLocker Administration and Monitoring (MBAM) recherche et affiche la version localisée.</span><span class="sxs-lookup"><span data-stu-id="03c45-106">If you create a localized version, as described in the following instructions, Microsoft BitLocker Administration and Monitoring (MBAM) finds and displays the localized version.</span></span> <span data-ttu-id="03c45-107">Si MBAM ne trouve pas de version localisée, il affiche l’URL configurée pour le paramètre **HelpDeskURL**.</span><span class="sxs-lookup"><span data-stu-id="03c45-107">If MBAM does not find a localized version, it displays the URL that is configured for the parameter **HelpDeskURL**.</span></span>

<span data-ttu-id="03c45-108">**Remarques**  Dans les instructions ci-dessous, *selfservice* est le nom de répertoire virtuel par défaut du portail libre-service.</span><span class="sxs-lookup"><span data-stu-id="03c45-108">**Note** In the following instructions, *SelfService* is the default virtual directory name for the Self-Service Portal.</span></span> <span data-ttu-id="03c45-109">Vous avez peut-être déjà utilisé un autre nom lorsque vous avez configuré le portail libre-service.</span><span class="sxs-lookup"><span data-stu-id="03c45-109">You might have used a different name when you configured the Self-Service Portal.</span></span>

 

**<span data-ttu-id="03c45-110">Pour localiser l’URL du portail libre-service</span><span class="sxs-lookup"><span data-stu-id="03c45-110">To localize the Self-Service Portal URL</span></span>**

1.  <span data-ttu-id="03c45-111">Sur le serveur sur lequel vous avez configuré le portail libre-service, accédez à **sites** &gt; **Microsoft BitLocker administration et analyse des paramètres de** l' &gt; **SelfService** &gt; **application**selfservice.</span><span class="sxs-lookup"><span data-stu-id="03c45-111">On the server where you configured the Self-Service Portal, browse to **Sites** &gt; **Microsoft BitLocker Administration and Monitoring** &gt; **SelfService** &gt; **Application Settings**.</span></span>

2.  <span data-ttu-id="03c45-112">Dans le volet **actions** , cliquez sur **Ajouter** pour ouvrir la boîte de dialogue Ajouter un **paramètre d’application** .</span><span class="sxs-lookup"><span data-stu-id="03c45-112">In the **Actions** pane, click **Add** to open the **Add Application Setting** dialog box.</span></span>

3.  <span data-ttu-id="03c45-113">Dans le champ **nom** , tapez **HelpdeskURL**\ _ &lt; *Language* &gt; , où &lt; *Language* &gt; correspond au code de langue approprié pour l’URL.</span><span class="sxs-lookup"><span data-stu-id="03c45-113">In the **Name** field, type **HelpdeskURL**\_&lt;*Language*&gt;, where &lt;*Language*&gt; is the appropriate language code for the URL.</span></span>

    <span data-ttu-id="03c45-114">Par exemple, pour créer une version localisée de la `HelpdeskURL` valeur en espagnol, nommez le paramètre **HelpdeskURL \ _es-es**.</span><span class="sxs-lookup"><span data-stu-id="03c45-114">For example, to create a localized version of the `HelpdeskURL` value in Spanish, name the parameter **HelpdeskURL\_es-es**.</span></span>

    <span data-ttu-id="03c45-115">Le nom du dossier Language peut également être le nom neutre des langues **au lieu** de **es-es**.</span><span class="sxs-lookup"><span data-stu-id="03c45-115">The name of the Language folder can also be the language neutral name **es** instead of **es-es**.</span></span> <span data-ttu-id="03c45-116">Si le navigateur de l’utilisateur final est défini sur **es-es** et que ce dossier n’existe pas, les paramètres régionaux du parent (tels qu’ils sont définis dans .net) sont récupérés et activés de manière récursive, ce qui a\\SelfServiceWebsite\\es\\Notice.txt pour effet d’arrêter &lt; &gt; le fichier de Notice.txt par défaut.</span><span class="sxs-lookup"><span data-stu-id="03c45-116">If the end user’s browser is set to **es-es** and that folder does not exist, the parent locale (as defined in .NET) is recursively retrieved and checked, resolving to &lt;MBAM Self-Service Install Directory&gt;\\SelfServiceWebsite\\es\\Notice.txt before finally becoming the default Notice.txt file.</span></span> <span data-ttu-id="03c45-117">Cette substitution récursive imite les règles de chargement des ressources .NET.</span><span class="sxs-lookup"><span data-stu-id="03c45-117">This recursive fallback mimics the .NET resource loading rules.</span></span>

    <span data-ttu-id="03c45-118">Pour obtenir la liste des codes de langue valides que vous pouvez utiliser, voir référence sur l' [API NLS (National Language Support)](https://go.microsoft.com/fwlink/?LinkId=317947).</span><span class="sxs-lookup"><span data-stu-id="03c45-118">For a list of the valid language codes you can use, see [National Language Support (NLS) API Reference](https://go.microsoft.com/fwlink/?LinkId=317947).</span></span>

4.  <span data-ttu-id="03c45-119">Dans le champ **valeur** , entrez la version localisée de la `HelpdeskURL` valeur que vous souhaitez afficher aux utilisateurs finaux.</span><span class="sxs-lookup"><span data-stu-id="03c45-119">In the **Value** field, type the localized version of the `HelpdeskURL` value that you want to display to end users.</span></span>



## <span data-ttu-id="03c45-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="03c45-120">Related topics</span></span>


[<span data-ttu-id="03c45-121">Personnalisation du portail libre-service de votre organisation</span><span class="sxs-lookup"><span data-stu-id="03c45-121">Customizing the Self-Service Portal for Your Organization</span></span>](customizing-the-self-service-portal-for-your-organization.md)

 

 
## <span data-ttu-id="03c45-122">Vous avez une suggestion pour MBAM?</span><span class="sxs-lookup"><span data-stu-id="03c45-122">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="03c45-123">Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)</span><span class="sxs-lookup"><span data-stu-id="03c45-123">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="03c45-124">Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="03c45-124">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>




