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
# Personnaliser le portail libre-service


Une fois que vous avez installé le portail libre-service Microsoft BitLocker administration et surveillance (MBAM), vous pouvez personnaliser le portail libre-service avec le nom de votre entreprise, l’URL du support technique et le texte «avis». Vous pouvez également modifier le paramètre de délai d’expiration de session pour que la session de l’utilisateur final expire après une période d’inactivité spécifiée.

**Pour définir le délai d’expiration de la session et la personnalisation du portail libre-service**

1.  Pour définir le délai d’expiration de la session de l’utilisateur final, démarrez **Internet Information Services Manager**ou exécutez **inetmgr.exe**.

2.  Accédez à **sites** &gt; **Microsoft BitLocker administration et analysez** &gt; **selfservice** &gt; **ASP.net** &gt; **État de session**, puis modifiez la valeur du **délai** d’expiration sous **paramètres de cookie** en le nombre de minutes après lequel la session de portail libre-service de l’utilisateur final va expirer. La valeur par défaut est5. Pour désactiver le paramètre afin qu’il n’y ait aucun délai d’expiration, définissez la valeur sur **0**.

3.  Pour définir les éléments de personnalisation du portail libre-service, démarrez **Internet Information Services Manager**ou exécutez **inetmgr.exe**.

4.  Accédez à **sites** &gt; **Microsoft BitLocker administration et contrôle des** paramètres de l' &gt; **SelfService** &gt; **application**selfservice.

5.  Dans la colonne **nom** , sélectionnez l’élément que vous voulez modifier, puis modifiez la valeur par défaut pour refléter le nom que vous voulez utiliser. Le tableau suivant répertorie les valeurs que vous pouvez définir.

    **Vigilance**  
    Ne modifiez pas la valeur de la colonne Name (CompanyName \ *), car le portail libre-service cesse de fonctionner.



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



## Rubriques connexes


[Déploiement de l'infrastructure de serveur MBAM2.0](deploying-the-mbam-20-server-infrastructure-mbam-2.md)









