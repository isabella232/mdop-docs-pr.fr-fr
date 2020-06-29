---
title: Comment charger les applets de commande PowerShell et obtenir de l'aide sur ces derniers
description: Comment charger les applets de commande PowerShell et obtenir de l'aide sur ces derniers
author: dansimp
ms.assetid: b6ae5460-2c3a-4030-b132-394d9d5a541e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/02/2016
ms.openlocfilehash: 32b5bb26331f204acffbf96ea119ac4209c3cd89
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805359"
---
# Comment charger les applets de commande PowerShell et obtenir de l'aide sur ces derniers


Contenu de cette rubrique:

-   [Configuration requise pour l’utilisation des cmdlets PowerShell](#bkmk-reqs-using-posh)

-   [Chargement des cmdlets PowerShell](#bkmk-load-cmdlets)

-   [Obtenir de l’aide pour les applets de applet PowerShell](#bkmk-get-cmdlet-help)

-   [Affichage de l’aide pour une cmdlet PowerShell](#bkmk-display-help-cmdlet)

## <a href="" id="bkmk-reqs-using-posh"></a>Configuration requise pour l’utilisation des cmdlets PowerShell


Pour plus d’informations sur l’utilisation des applets de commande PowerShell App-V, consultez la configuration suivante:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Condition requise</th>
<th align="left">Détails</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Les utilisateurs ne peuvent exécuter des cmdlets App-V Server que si vous leur octroyez l’accès à l’aide de l’une des méthodes suivantes:</p></td>
<td align="left"><ul>
<li><p><strong>Lorsque vous déployez et configurez le serveur App-V </strong> :</p>
<p>Spécifiez un groupe Active Directory ou un utilisateur qui dispose des autorisations pour gérer l’environnement App-V. Découvrez <a href="how-to-deploy-the-app-v-51-server.md" data-raw-source="[How to Deploy the App-V 5.1 Server](how-to-deploy-the-app-v-51-server.md)"> comment déployer le serveur App-V 5,1 </a> .</p></li>
<li><p><strong>Après avoir déployé le serveur App-V </strong> :</p>
<p>Utilisez la console de gestion App-V pour ajouter un utilisateur ou un groupe Active Directory supplémentaire. Découvrez <a href="how-to-add-or-remove-an-administrator-by-using-the-management-console51.md" data-raw-source="[How to Add or Remove an Administrator by Using the Management Console](how-to-add-or-remove-an-administrator-by-using-the-management-console51.md)"> comment ajouter ou supprimer un administrateur à l’aide de la console de gestion </a> .</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Applets de commande nécessitant une invite de commandes avec élévation de privilèges</p></td>
<td align="left"><ul>
<li><p>Add-AppvClientPackage</p></li>
<li><p>Remove-AppvClientPackage</p></li>
<li><p>Set-AppvClientConfiguration</p></li>
<li><p>Add-AppvClientConnectionGroup</p></li>
<li><p>Remove-AppvClientConnectionGroup</p></li>
<li><p>Add-AppvPublishingServer</p></li>
<li><p>Remove-AppvPublishingServer</p></li>
<li><p>Send-AppvClientReport</p></li>
<li><p>Set-AppvClientMode</p></li>
<li><p>Set-AppvClientPackage</p></li>
<li><p>Set-AppvPublishingServer</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Applets de commande que les utilisateurs finaux peuvent exécuter, sauf si vous les configurez pour exiger une invite de commandes avec élévation de privilèges</p></td>
<td align="left"><ul>
<li><p>Publisher-AppvClientPackage</p></li>
<li><p>Annuler la publication-AppvClientPackage</p></li>
</ul>
<p>Pour configurer ces applets de commande afin de nécessiter une invite de commandes avec élévation de privilèges, utilisez l’une des méthodes suivantes:</p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Méthode</th>
<th align="left">Ressources complémentaires</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Exécutez l' <strong> applet de cmdlet Set-AppvClientConfiguration </strong> à l’aide du <strong> paramètre-RequirePublishAsAdmin </strong> .</p></td>
<td align="left"><ul>
<li><p><a href="how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell51.md#bkmk-admin-only-posh-topic-cg" data-raw-source="[How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell](how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell51.md#bkmk-admin-only-posh-topic-cg)">Comment gérer des groupes de connexion sur un ordinateur autonome à l'aide de PowerShell</a></p></li>
<li><p><a href="how-to-manage-app-v-51-packages-running-on-a-stand-alone-computer-by-using-powershell.md" data-raw-source="[How to Manage App-V 5.1 Packages Running on a Stand-Alone Computer by Using PowerShell](how-to-manage-app-v-51-packages-running-on-a-stand-alone-computer-by-using-powershell.md)">Gestion de packages App-V5.1 s'exécutant sur un ordinateur autonome à l'aide de PowerShell</a></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Activez le paramètre de stratégie de groupe «exiger une publication en tant qu’administrateur» pour les clients App-V.</p></td>
<td align="left"><p><a href="how-to-publish-a-package-by-using-the-management-console-51.md" data-raw-source="[How to Publish a Package by Using the Management Console](how-to-publish-a-package-by-using-the-management-console-51.md)">Comment publier un package à l’aide de la console de gestion</a></p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-load-cmdlets"></a>Chargement des cmdlets PowerShell

Pour charger les modules de cmdlet PowerShell:

1.  Ouvrez l’environnement d’exécution de scripts Windows PowerShell ou Windows PowerShell intégré.

2.  Tapez l’une des commandes suivantes pour charger les applets de commande pour le module souhaité:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Composant App-V</th>
<th align="left">Commande pour taper</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>App-V Server</p></td>
<td align="left"><p>Importation-module AppvServer</p></td>
</tr>
<tr class="even">
<td align="left"><p>Séquenceur App-V</p></td>
<td align="left"><p>Importation-module AppvSequencer</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Client App-V</p></td>
<td align="left"><p>Importation-module AppvClient</p></td>
</tr>
</tbody>
</table>

## <a href="" id="bkmk-get-cmdlet-help"></a>Obtenir de l’aide pour les applets de applet PowerShell
À partir de App-V 5,0 SP3, l’aide de l’applet de cmdlet est disponible dans deux formats:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Format</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Module téléchargeable</p></td>
<td align="left"><p>Pour télécharger la dernière aide après le téléchargement du module de cmdlet:</p>
<ol>
<li><p>Ouvrez l’environnement d’exécution de scripts Windows PowerShell ou Windows PowerShell intégré.</p></li>
<li><p>Tapez l’une des commandes suivantes pour charger les applets de commande pour le module souhaité:</p></li>
</ol>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Composant App-V</th>
<th align="left">Commande pour taper</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>App-V Server</p></td>
<td align="left"><p>Mise à jour-aide-module AppvServer</p></td>
</tr>
<tr class="even">
<td align="left"><p>Séquenceur App-V</p></td>
<td align="left"><p>Mise à jour-aide-module AppvSequencer</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Client App-V</p></td>
<td align="left"><p>Mise à jour-aide-module AppvClient</p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
<tr class="even">
<td align="left"><p>Sur TechNet en tant que pages Web</p></td>
<td align="left"><p>Pour plus d’information, voir le nœud App-V sous l' <a href="https://technet.microsoft.com/library/dn520245.aspx" data-raw-source="[Microsoft Desktop Optimization Pack Automation with Windows PowerShell](https://technet.microsoft.com/library/dn520245.aspx)"> Automation Microsoft Desktop Optimization with Windows PowerShell </a> .</p></td>
</tr>
</tbody>
</table>

## <a href="" id="bkmk-display-help-cmdlet"></a>Affichage de l’aide pour une cmdlet PowerShell
Pour afficher de l’aide pour une cmdlet PowerShell spécifique:

1.  Ouvrez l’environnement d’exécution de scripts Windows PowerShell ou Windows PowerShell intégré.

2.  Tapez **Get-Help** &lt; *cmdlet* &gt; , par exemple, **Get-Help publishation-AppvClientPackage**.

Vous **avez une suggestion pour App-V**? Ajoutez ou Votez en fonction [de suggestions.](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization) **Vous avez un problème lié à l’application-V?** Utilisez le [Forum TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

 

 





