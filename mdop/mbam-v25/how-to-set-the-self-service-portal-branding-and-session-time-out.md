---
title: Personnalisation du portail libre-service et définition du délai d'expiration de session
description: Personnalisation du portail libre-service et définition du délai d'expiration de session
author: dansimp
ms.assetid: 031eedfc-fade-4d2f-8771-b329e1d38c0d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e222880b2d5557ef15cd7a4efd6421b9972541f4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804297"
---
# <span data-ttu-id="67956-103">Personnalisation du portail libre-service et définition du délai d'expiration de session</span><span class="sxs-lookup"><span data-stu-id="67956-103">How to Set the Self-Service Portal Branding and Session Time-out</span></span>


<span data-ttu-id="67956-104">Après avoir configuré le portail libre-service, vous pouvez le personnaliser en utilisant le nom de votre société, l’URL du support technique et le texte «avis».</span><span class="sxs-lookup"><span data-stu-id="67956-104">After you configure the Self-Service Portal, you can brand it with your company name, Help Desk URL, and "notice" text.</span></span> <span data-ttu-id="67956-105">Vous pouvez également modifier le paramètre de temporisation de la session pour que la session de l’utilisateur final expire après une période d’inactivité spécifiée.</span><span class="sxs-lookup"><span data-stu-id="67956-105">You can also change the Session Time-out setting to make the end user’s session expire after a specified period of inactivity.</span></span>

**<span data-ttu-id="67956-106">Remarque</span><span class="sxs-lookup"><span data-stu-id="67956-106">Note</span></span>**  
<span data-ttu-id="67956-107">Vous pouvez également personnaliser le portail libre-service à l’aide de l’applet de MbamWebApplication Windows PowerShell **Enable-** ou de l’Assistant Configuration de MBAM Server.</span><span class="sxs-lookup"><span data-stu-id="67956-107">You can also brand the Self-Service Portal by using the **Enable-MbamWebApplication** Windows PowerShell cmdlet or the MBAM Server Configuration wizard.</span></span> <span data-ttu-id="67956-108">Pour obtenir des instructions sur l’utilisation de l’Assistant, voir [Comment configurer les applications Web MBAM 2,5](how-to-configure-the-mbam-25-web-applications.md).</span><span class="sxs-lookup"><span data-stu-id="67956-108">For instructions on using the wizard, see [How to Configure the MBAM 2.5 Web Applications](how-to-configure-the-mbam-25-web-applications.md).</span></span>



**<span data-ttu-id="67956-109">Remarque</span><span class="sxs-lookup"><span data-stu-id="67956-109">Note</span></span>**  
<span data-ttu-id="67956-110">Dans les instructions ci-dessous, *selfservice* est le nom de répertoire virtuel par défaut du portail libre-service.</span><span class="sxs-lookup"><span data-stu-id="67956-110">In the following instructions, *SelfService* is the default virtual directory name for the Self-Service Portal.</span></span> <span data-ttu-id="67956-111">Vous avez peut-être déjà utilisé un autre nom lorsque vous avez configuré le portail libre-service.</span><span class="sxs-lookup"><span data-stu-id="67956-111">You might have used a different name when you configured the Self-Service Portal.</span></span>



**<span data-ttu-id="67956-112">Pour définir le délai d’expiration de la session et la personnalisation du portail libre-service</span><span class="sxs-lookup"><span data-stu-id="67956-112">To set the session time-out and branding for the Self-Service Portal</span></span>**

1.  <span data-ttu-id="67956-113">Pour définir le délai d’expiration de la session de l’utilisateur final, démarrez **Internet Information Services Manager**ou exécutez **inetmgr.exe**.</span><span class="sxs-lookup"><span data-stu-id="67956-113">To set the time-out period for the end user’s session, start the **Internet Information Services Manager**, or run **inetmgr.exe**.</span></span>

2.  <span data-ttu-id="67956-114">Accédez à **sites** &gt; **Microsoft BitLocker administration et analysez** &gt; **selfservice** &gt; **ASP.net** &gt; **État de session**, puis modifiez la valeur du **délai** d’expiration sous **paramètres de cookie** en le nombre de minutes après lequel la session de portail libre-service de l’utilisateur final expire.</span><span class="sxs-lookup"><span data-stu-id="67956-114">Browse to **Sites** &gt; **Microsoft BitLocker Administration and Monitoring** &gt; **SelfService** &gt; **ASP.NET** &gt; **Session State**, and change the **Time-out** value under **Cookie Settings** to the number of minutes after which the end user’s Self-Service Portal session expires.</span></span> <span data-ttu-id="67956-115">La valeur par défaut est **5**.</span><span class="sxs-lookup"><span data-stu-id="67956-115">The default value is **5**.</span></span> <span data-ttu-id="67956-116">Pour désactiver le paramètre afin qu’il n’y ait aucun délai d’expiration, définissez la valeur sur **0**.</span><span class="sxs-lookup"><span data-stu-id="67956-116">To disable the setting so that there is no time-out, set the value to **0**.</span></span>

3.  <span data-ttu-id="67956-117">Pour définir les éléments de personnalisation du portail libre-service, démarrez **Internet Information Services Manager** ou exécutez **inetmgr.exe**.</span><span class="sxs-lookup"><span data-stu-id="67956-117">To set the branding items for the Self-Service Portal, start the **Internet Information Services Manager** or run **inetmgr.exe**.</span></span>

4.  <span data-ttu-id="67956-118">Accédez à **sites** &gt; **Microsoft BitLocker administration et contrôle des** paramètres de l' &gt; **SelfService** &gt; **application**selfservice.</span><span class="sxs-lookup"><span data-stu-id="67956-118">Browse to **Sites** &gt; **Microsoft BitLocker Administration and Monitoring** &gt; **SelfService** &gt; **Application Settings**.</span></span>

5.  <span data-ttu-id="67956-119">Dans la colonne **nom** , sélectionnez l’élément que vous voulez modifier, puis modifiez la valeur par défaut pour refléter le nom que vous voulez utiliser.</span><span class="sxs-lookup"><span data-stu-id="67956-119">In the **Name** column, select the item that you want to change, and change the default value to reflect the name that you want to use.</span></span> <span data-ttu-id="67956-120">Le tableau suivant répertorie les valeurs que vous pouvez définir.</span><span class="sxs-lookup"><span data-stu-id="67956-120">The following table lists the values that you can set.</span></span>

    **<span data-ttu-id="67956-121">Vigilance</span><span class="sxs-lookup"><span data-stu-id="67956-121">Caution</span></span>**  
    <span data-ttu-id="67956-122">Ne modifiez pas la valeur de la colonne Name (CompanyName \ \*), car elle provoquera l’arrêt du portail libre-service.</span><span class="sxs-lookup"><span data-stu-id="67956-122">Do not change the value in the Name column (CompanyName\*), as it will cause Self-Service Portal to stop working.</span></span>



~~~
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Name</th>
<th align="left">Default value</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>ClientValidationEnabled</p></td>
<td align="left"><p>true</p></td>
</tr>
<tr class="even">
<td align="left"><p>CompanyName</p></td>
<td align="left"><p>Contoso IT</p></td>
</tr>
<tr class="odd">
<td align="left"><p>DisplayNotice</p></td>
<td align="left"><p>true</p></td>
</tr>
<tr class="even">
<td align="left"><p>HelpdeskText</p></td>
<td align="left"><p>Contact Helpdesk or IT Department</p></td>
</tr>
<tr class="odd">
<td align="left"><p>HelpdeskUrl</p></td>
<td align="left"><p>#</p>
<div class="alert">
<strong>Note</strong>  
<p>In MBAM 2.5 SP1, the HelpdeskUrl default value is empty.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>jQueryPath</p></td>
<td align="left"><p>[//go.microsoft.com/fwlink/?LinkID=390515](//go.microsoft.com/fwlink/?LinkID=390515)</p>
<div class="alert">
<strong>Note</strong>  
<p>In MBAM 2.5 SP1, this has been changed to a local JavaScript file shipped with the product, located at ~/Scripts/jquery-1.10.2.min.js</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>jQueryValidatePath</p></td>
<td align="left"><p>[//go.microsoft.com/fwlink/?LinkID=390516](//go.microsoft.com/fwlink/?LinkID=390516)</p>
<div class="alert">
<strong>Note</strong>  
<p>In MBAM 2.5 SP1, this has been changed to a local JavaScript file shipped with the product, located at ~/Scripts/jquery.validate.min.js</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>jQueryValidateUnobtrusivePath</p></td>
<td align="left"><p>[//go.microsoft.com/fwlink/?LinkID=390517](//go.microsoft.com/fwlink/?LinkID=390517)</p>
<div class="alert">
<strong>Note</strong>  
<p>In MBAM 2.5 SP1, this has been changed to a local JavaScript file shipped with the product, located at ~/Scripts/jquery.validate.unobtrusive.min.js</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>NoticeTextPath</p></td>
<td align="left"><p>Notice.txt</p>
<div class="alert">
<strong>Note</strong>  
<p>You can edit the notice text either by using the Internet Information Services (IIS) Manager or by opening and changing the Notice.txt file in the installation directory.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>UnobtrusiveJavaScriptEnabled</p></td>
<td align="left"><p>true</p></td>
</tr>
</tbody>
</table>
~~~





## <span data-ttu-id="67956-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="67956-123">Related topics</span></span>


[<span data-ttu-id="67956-124">Personnalisation du portail libre-service de votre organisation</span><span class="sxs-lookup"><span data-stu-id="67956-124">Customizing the Self-Service Portal for Your Organization</span></span>](customizing-the-self-service-portal-for-your-organization.md)



## <span data-ttu-id="67956-125">Vous avez une suggestion pour MBAM?</span><span class="sxs-lookup"><span data-stu-id="67956-125">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="67956-126">Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)</span><span class="sxs-lookup"><span data-stu-id="67956-126">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="67956-127">Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="67956-127">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





