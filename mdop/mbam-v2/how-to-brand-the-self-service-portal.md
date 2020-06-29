---
title: Personnaliser le portail libre-service
description: Personnaliser le portail libre-service
author: dansimp
ms.assetid: 3ef9e951-7c42-4f7f-b131-3765d39b3207
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fe4f4efc5852042671711ba5780cc78055957ba8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810980"
---
# <span data-ttu-id="fc6c9-103">Personnaliser le portail libre-service</span><span class="sxs-lookup"><span data-stu-id="fc6c9-103">How to Brand the Self-Service Portal</span></span>


<span data-ttu-id="fc6c9-104">Une fois que vous avez installé le portail libre-service Microsoft BitLocker administration et surveillance (MBAM), vous pouvez personnaliser le portail libre-service avec le nom de votre entreprise, l’URL du support technique et le texte «avis».</span><span class="sxs-lookup"><span data-stu-id="fc6c9-104">After you install the Microsoft BitLocker Administration and Monitoring (MBAM) Self-Service Portal, you can brand the Self-Service Portal with your company name, Help Desk URL, and “notice” text.</span></span> <span data-ttu-id="fc6c9-105">Vous pouvez également modifier le paramètre de délai d’expiration de session pour que la session de l’utilisateur final expire après une période d’inactivité spécifiée.</span><span class="sxs-lookup"><span data-stu-id="fc6c9-105">You can also change the Session Timeout setting to make the end user’s session expire after a specified period of inactivity.</span></span>

**<span data-ttu-id="fc6c9-106">Pour définir le délai d’expiration de la session et la personnalisation du portail libre-service</span><span class="sxs-lookup"><span data-stu-id="fc6c9-106">To set the session time-out and branding for the Self-Service Portal</span></span>**

1.  <span data-ttu-id="fc6c9-107">Pour définir le délai d’expiration de la session de l’utilisateur final, démarrez **Internet Information Services Manager**ou exécutez **inetmgr.exe**.</span><span class="sxs-lookup"><span data-stu-id="fc6c9-107">To set the time-out period for the end user’s session, start the **Internet Information Services Manager**, or run **inetmgr.exe**.</span></span>

2.  <span data-ttu-id="fc6c9-108">Accédez à **sites** &gt; **Microsoft BitLocker administration et analysez** &gt; **selfservice** &gt; **ASP.net** &gt; **État de session**, puis modifiez la valeur du **délai** d’expiration sous **paramètres de cookie** en le nombre de minutes après lequel la session de portail libre-service de l’utilisateur final va expirer.</span><span class="sxs-lookup"><span data-stu-id="fc6c9-108">Browse to **Sites** &gt; **Microsoft BitLocker Administration and Monitoring** &gt; **SelfService** &gt; **ASP.NET** &gt; **Session State**, and change the **Time-out** value under **Cookie Settings** to the number of minutes after which the end user’s Self-Service Portal session will expire.</span></span> <span data-ttu-id="fc6c9-109">La valeur par défaut est5.</span><span class="sxs-lookup"><span data-stu-id="fc6c9-109">The default is 5.</span></span> <span data-ttu-id="fc6c9-110">Pour désactiver le paramètre afin qu’il n’y ait aucun délai d’expiration, définissez la valeur sur **0**.</span><span class="sxs-lookup"><span data-stu-id="fc6c9-110">To disable the setting so that there is no time-out, set the value to **0**.</span></span>

3.  <span data-ttu-id="fc6c9-111">Pour définir les éléments de personnalisation du portail libre-service, démarrez **Internet Information Services Manager**ou exécutez **inetmgr.exe**.</span><span class="sxs-lookup"><span data-stu-id="fc6c9-111">To set the branding items for the Self-Service Portal, start the **Internet Information Services Manager**, or run **inetmgr.exe**.</span></span>

4.  <span data-ttu-id="fc6c9-112">Accédez à **sites** &gt; **Microsoft BitLocker administration et contrôle des** paramètres de l' &gt; **SelfService** &gt; **application**selfservice.</span><span class="sxs-lookup"><span data-stu-id="fc6c9-112">Browse to **Sites** &gt; **Microsoft BitLocker Administration and Monitoring** &gt; **SelfService** &gt; **Application Settings**.</span></span>

5.  <span data-ttu-id="fc6c9-113">Dans la colonne **nom** , sélectionnez l’élément que vous voulez modifier, puis modifiez la valeur par défaut pour refléter le nom que vous voulez utiliser.</span><span class="sxs-lookup"><span data-stu-id="fc6c9-113">From the **Name** column, select the item that you want to change, and change the default value to reflect the name that you want to use.</span></span> <span data-ttu-id="fc6c9-114">Le tableau suivant répertorie les valeurs que vous pouvez définir.</span><span class="sxs-lookup"><span data-stu-id="fc6c9-114">The following table lists the values that you can set.</span></span>

    **<span data-ttu-id="fc6c9-115">Vigilance</span><span class="sxs-lookup"><span data-stu-id="fc6c9-115">Caution</span></span>**  
    <span data-ttu-id="fc6c9-116">Ne modifiez pas la valeur de la colonne Name (CompanyName \ \*), car le portail libre-service cesse de fonctionner.</span><span class="sxs-lookup"><span data-stu-id="fc6c9-116">Do not change the value in the Name column (CompanyName\*), as it will cause the Self-Service Portal to stop working.</span></span>



~~~
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Name</th>
<th align="left">Default Value</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>CompanyName*</p></td>
<td align="left"><p>Contoso IT</p></td>
</tr>
<tr class="even">
<td align="left"><p>HelpdeskText*</p></td>
<td align="left"><p>Contact Help Desk or IT Department</p></td>
</tr>
<tr class="odd">
<td align="left"><p>HelpdeskUrl*</p></td>
<td align="left"><p>Http://www.microsoft.com</p></td>
</tr>
<tr class="even">
<td align="left"><p>jQueryPath</p></td>
<td align="left"><p>//ajax.aspnetcdn.com/ajax/jQuery/jquery-1.7.2.min.js</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MicrosoftAjaxPath</p></td>
<td align="left"><p>//ajax.aspnetcdn.com/ajax/3.5/MicrosoftAjax.js</p></td>
</tr>
<tr class="even">
<td align="left"><p>MicrosoftMvcAjaxPath</p></td>
<td align="left"><p>//ajax.aspnetcdn.com/ajax/mvc/2.0/MicrosoftMvcValidation.js</p></td>
</tr>
<tr class="odd">
<td align="left"><p>NoticeTextPath</p></td>
<td align="left"><p>Notice.txt</p>
<div class="alert">
<strong>Note</strong>  
<p>You can edit the Notice text either by using the IIS Manager or by opening and changing the Notice.txt file in the installation directory.</p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>
~~~



## <span data-ttu-id="fc6c9-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fc6c9-117">Related topics</span></span>


[<span data-ttu-id="fc6c9-118">Déploiement de l'infrastructure de serveur MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="fc6c9-118">Deploying the MBAM 2.0 Server Infrastructure</span></span>](deploying-the-mbam-20-server-infrastructure-mbam-2.md)









