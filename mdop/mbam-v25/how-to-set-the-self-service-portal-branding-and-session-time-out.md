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
# Personnalisation du portail libre-service et définition du délai d'expiration de session


Après avoir configuré le portail libre-service, vous pouvez le personnaliser en utilisant le nom de votre société, l’URL du support technique et le texte «avis». Vous pouvez également modifier le paramètre de temporisation de la session pour que la session de l’utilisateur final expire après une période d’inactivité spécifiée.

**Remarque**  
Vous pouvez également personnaliser le portail libre-service à l’aide de l’applet de MbamWebApplication Windows PowerShell **Enable-** ou de l’Assistant Configuration de MBAM Server. Pour obtenir des instructions sur l’utilisation de l’Assistant, voir [Comment configurer les applications Web MBAM 2,5](how-to-configure-the-mbam-25-web-applications.md).



**Remarque**  
Dans les instructions ci-dessous, *selfservice* est le nom de répertoire virtuel par défaut du portail libre-service. Vous avez peut-être déjà utilisé un autre nom lorsque vous avez configuré le portail libre-service.



**Pour définir le délai d’expiration de la session et la personnalisation du portail libre-service**

1.  Pour définir le délai d’expiration de la session de l’utilisateur final, démarrez **Internet Information Services Manager**ou exécutez **inetmgr.exe**.

2.  Accédez à **sites** &gt; **Microsoft BitLocker administration et analysez** &gt; **selfservice** &gt; **ASP.net** &gt; **État de session**, puis modifiez la valeur du **délai** d’expiration sous **paramètres de cookie** en le nombre de minutes après lequel la session de portail libre-service de l’utilisateur final expire. La valeur par défaut est **5**. Pour désactiver le paramètre afin qu’il n’y ait aucun délai d’expiration, définissez la valeur sur **0**.

3.  Pour définir les éléments de personnalisation du portail libre-service, démarrez **Internet Information Services Manager** ou exécutez **inetmgr.exe**.

4.  Accédez à **sites** &gt; **Microsoft BitLocker administration et contrôle des** paramètres de l' &gt; **SelfService** &gt; **application**selfservice.

5.  Dans la colonne **nom** , sélectionnez l’élément que vous voulez modifier, puis modifiez la valeur par défaut pour refléter le nom que vous voulez utiliser. Le tableau suivant répertorie les valeurs que vous pouvez définir.

    **Vigilance**  
    Ne modifiez pas la valeur de la colonne Name (CompanyName \ *), car elle provoquera l’arrêt du portail libre-service.



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





## Rubriques connexes


[Personnalisation du portail libre-service de votre organisation](customizing-the-self-service-portal-for-your-organization.md)



## Vous avez une suggestion pour MBAM?
- Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring) 
- Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





