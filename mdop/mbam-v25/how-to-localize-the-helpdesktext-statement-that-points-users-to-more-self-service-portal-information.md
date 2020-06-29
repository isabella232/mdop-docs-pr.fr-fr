---
title: Localisation de l'instruction «HelpdeskText» qui oriente les utilisateurs vers des informations supplémentaires sur le portail libre-service
description: Localisation de l'instruction «HelpdeskText» qui oriente les utilisateurs vers des informations supplémentaires sur le portail libre-service
author: dansimp
ms.assetid: 09ba2a07-3186-45d9-adef-4034c70ae7cf
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 2367424185da813a46fa52f3614c03083864f75f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809947"
---
# <span data-ttu-id="bffd3-103">Localisation de l'instruction «HelpdeskText» qui oriente les utilisateurs vers des informations supplémentaires sur le portail libre-service</span><span class="sxs-lookup"><span data-stu-id="bffd3-103">How to Localize the “HelpdeskText” Statement that Points Users to More Self-Service Portal Information</span></span>


<span data-ttu-id="bffd3-104">Vous pouvez configurer une version localisée de la déclaration «HelpdeskText» du portail libre-service, qui informe les utilisateurs finaux sur la manière d’obtenir de l’aide supplémentaire lors de l’utilisation du portail libre-service.</span><span class="sxs-lookup"><span data-stu-id="bffd3-104">You can configure a localized version of the Self-Service Portal "HelpdeskText" statement, which informs end users about how to get additional help when they are using the Self-Service Portal.</span></span> <span data-ttu-id="bffd3-105">Si vous configurez du texte localisé pour l’instruction, comme décrit dans les instructions ci-dessous, MBAM affiche la version localisée.</span><span class="sxs-lookup"><span data-stu-id="bffd3-105">If you configure localized text for the statement, as described in the following instructions, MBAM displays the localized version.</span></span> <span data-ttu-id="bffd3-106">Si MBAM ne trouve pas la version localisée, il affiche la valeur figurant dans le paramètre **HelpdeskText** .</span><span class="sxs-lookup"><span data-stu-id="bffd3-106">If MBAM does not find the localized version, it displays the value that is in the **HelpdeskText** parameter.</span></span>

<span data-ttu-id="bffd3-107">**Remarques**  Dans les instructions ci-dessous, *selfservice* est le nom de répertoire virtuel par défaut du portail libre-service.</span><span class="sxs-lookup"><span data-stu-id="bffd3-107">**Note** In the following instructions, *SelfService* is the default virtual directory name for the Self-Service Portal.</span></span> <span data-ttu-id="bffd3-108">Vous avez peut-être déjà utilisé un autre nom lorsque vous avez configuré le portail libre-service.</span><span class="sxs-lookup"><span data-stu-id="bffd3-108">You might have used a different name when you configured the Self-Service Portal.</span></span>

 

**<span data-ttu-id="bffd3-109">Pour afficher une version localisée de l’instruction HelpdeskText</span><span class="sxs-lookup"><span data-stu-id="bffd3-109">To display a localized version of the HelpdeskText statement</span></span>**

1.  <span data-ttu-id="bffd3-110">Sur le serveur sur lequel vous avez configuré le portail libre-service, accédez à **sites** &gt; **Microsoft BitLocker administration et analyse des paramètres de** l' &gt; **SelfService** &gt; **application**selfservice.</span><span class="sxs-lookup"><span data-stu-id="bffd3-110">On the server where you configured the Self-Service Portal, browse to **Sites** &gt; **Microsoft BitLocker Administration and Monitoring** &gt; **SelfService** &gt; **Application Settings**.</span></span>

2.  <span data-ttu-id="bffd3-111">Dans le volet **actions** , cliquez sur **Ajouter** pour ouvrir la boîte de dialogue Ajouter un **paramètre d’application** .</span><span class="sxs-lookup"><span data-stu-id="bffd3-111">In the **Actions** pane, click **Add** to open the **Add Application Setting** dialog box.</span></span>

3.  <span data-ttu-id="bffd3-112">Dans le champ **nom** , tapez **HelpdeskText**\ _ &lt; *Language* &gt; , où &lt; *Language* &gt; correspond au code de langue approprié pour le texte.</span><span class="sxs-lookup"><span data-stu-id="bffd3-112">In the **Name** field, type **HelpdeskText**\_&lt;*Language*&gt;, where &lt;*Language*&gt; is the appropriate language code for the text.</span></span>

    <span data-ttu-id="bffd3-113">Par exemple, pour créer une instruction HelpdeskText localisée en espagnol, nommez le paramètre **HelpdeskText \ _es-es**.</span><span class="sxs-lookup"><span data-stu-id="bffd3-113">For example, to create a localized HelpdeskText statement in Spanish, name the parameter **HelpdeskText\_es-es**.</span></span>

    <span data-ttu-id="bffd3-114">Le nom du dossier Language peut également être le nom neutre des langues **au lieu** de **es-es**.</span><span class="sxs-lookup"><span data-stu-id="bffd3-114">The name of the Language folder can also be the language neutral name **es** instead of **es-es**.</span></span> <span data-ttu-id="bffd3-115">Si le navigateur de l’utilisateur final est défini sur **es-es** et que ce dossier n’existe pas, les paramètres régionaux du parent (tels qu’ils sont définis dans .net) sont récupérés et activés de manière récursive, ce qui a\\SelfServiceWebsite\\es\\Notice.txt pour effet d’arrêter &lt; &gt; le fichier de Notice.txt par défaut.</span><span class="sxs-lookup"><span data-stu-id="bffd3-115">If the end user’s browser is set to **es-es** and that folder does not exist, the parent locale (as defined in .NET) is recursively retrieved and checked, resolving to &lt;MBAM Self-Service Install Directory&gt;\\SelfServiceWebsite\\es\\Notice.txt before finally becoming the default Notice.txt file.</span></span> <span data-ttu-id="bffd3-116">Cette substitution récursive imite les règles de chargement des ressources .NET.</span><span class="sxs-lookup"><span data-stu-id="bffd3-116">This recursive fallback mimics the .NET resource loading rules.</span></span>

    <span data-ttu-id="bffd3-117">Pour obtenir la liste des codes de langue valides que vous pouvez utiliser, voir référence sur l' [API NLS (National Language Support)](https://go.microsoft.com/fwlink/?LinkId=317947).</span><span class="sxs-lookup"><span data-stu-id="bffd3-117">For a list of the valid language codes you can use, see [National Language Support (NLS) API Reference](https://go.microsoft.com/fwlink/?LinkId=317947).</span></span>

4.  <span data-ttu-id="bffd3-118">Dans le champ **valeur** , tapez le texte localisé que vous souhaitez afficher aux utilisateurs finaux.</span><span class="sxs-lookup"><span data-stu-id="bffd3-118">In the **Value** field, type the localized text that you want to display to end users.</span></span>



## <span data-ttu-id="bffd3-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bffd3-119">Related topics</span></span>


[<span data-ttu-id="bffd3-120">Personnalisation du portail libre-service de votre organisation</span><span class="sxs-lookup"><span data-stu-id="bffd3-120">Customizing the Self-Service Portal for Your Organization</span></span>](customizing-the-self-service-portal-for-your-organization.md)

 

 

## <span data-ttu-id="bffd3-121">Vous avez une suggestion pour MBAM?</span><span class="sxs-lookup"><span data-stu-id="bffd3-121">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="bffd3-122">Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)</span><span class="sxs-lookup"><span data-stu-id="bffd3-122">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="bffd3-123">Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="bffd3-123">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>



