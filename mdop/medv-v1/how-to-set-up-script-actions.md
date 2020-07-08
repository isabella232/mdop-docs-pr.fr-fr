---
title: Comment configurer des actions de script
description: Comment configurer des actions de script
author: dansimp
ms.assetid: 367e28f1-d8c2-4845-a01b-2fff9128ccfd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2bfa264be447a0a8560e4af16ccaadc2ec1db3f6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804189"
---
# Comment configurer des actions de script


L’éditeur d’actions de script permet à l’administrateur de créer des actions à effectuer lors de l’installation de l’espace de travail MED-V, ainsi que de définir l’ordre dans lequel ils sont exécutés.

La liste suivante répertorie les actions qui peuvent être ajoutées au script de configuration du domaine:

-   **Redémarrez Windows**, puis redémarrez Windows.

-   **Joindre le domaine**: Si vous rejoignez un domaine, incluez cette action et configurez le nom d’utilisateur, le mot de passe, le nom de domaine complet, le nom de domaine NetBIOS et l’unité d’organisation (facultatif).

-   **Vérifier la connectivité**: configurer un serveur auquel se connecter et vérifier que l’espace de travail MED-V peut se connecter à une ressource réseau (par exemple, le serveur de domaine).

-   **Ligne de commande**: configurez un script dans l’espace de travail MED-V et entrez une ligne de commande incluant le chemin d’accès du script et les arguments du script.

-   **Renommer l’ordinateur**: renommez l’ordinateur virtuel en fonction des paramètres définis.

-   **Désactiver la connexion automatique**, désactivez la connexion automatique Windows. Cette action doit être ajoutée à la fin des scripts qui ajoutent l’ordinateur au domaine.

## <a href="" id="how-to-set-up-script-actions-"></a>Comment configurer des actions de script


**Pour configurer les actions de script**

1.  Dans l’onglet Configuration de l' **ordinateur virtuel** , cliquez sur **éditeur de script**.

2.  Dans la boîte de dialogue **actions de script** , cliquez sur **Ajouter**, puis dans le sous-menu, cliquez sur les actions de votre choix.

3.  Configurez les actions comme décrit dans les tableaux suivants.

    **Remarques** 
     L’attribution d’un nom à un **ordinateur** est configurée dans l’onglet Paramètres de la **machine virtuelle** . Pour plus d’informations, reportez-vous [à configuration des propriétés de modèle de nom d’ordinateur VM](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md).

     

~~~
**Note**  
To rename a computer, Windows must be restarted. It is recommended to add a Restart Windows action following a Rename Computer action.
~~~



4. Définissez l’ordre des actions en sélectionnant une action, puis en cliquant sur **monter** ou **descendre**.

5. Cliquez sur **OK**.

**Remarque**  
Lorsque vous exécutez le script de domaine de jointure, l’utilisateur connecté à l’ordinateur virtuel de l’espace de travail MED-V doit disposer de droits d’administrateur local.



**Remarque**  
Lorsque vous exécutez le script de désactivation de la connexion automatique, il est recommandé de désactiver le compte invité local utilisé pour l’ouverture de session automatique une fois la configuration initiale terminée.



### <a href="" id="bkmk-joindomainproperties"></a>

**Joindre les propriétés de domaine**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Propriété</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Informations d’identification à utiliser lors de la connexion de l’ordinateur virtuel au domaine</p></td>
<td align="left"><p>Sélectionnez l’une des informations d’identification suivantes à utiliser lors de la connexion de l’ordinateur virtuel au domaine:</p>
<ul>
<li><p><strong>Utilisez les informations d’identification MED-V </strong> (informations d’identification de l’utilisateur final).</p></li>
<li><p><strong>Utilisez les informations d’identification suivantes </strong> : les informations d’identification spécifiées; entrez un nom d’utilisateur et un mot de passe dans les champs correspondants.</p></li>
</ul>
<div class="alert">
<strong>Remarque</strong><br/><p>Les informations d’identification que vous entrez sont visibles par tous les utilisateurs de l’espace de travail MED-V. Il est déconseillé de fournir des informations d’identification d’administrateur de domaine.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Domaine à joindre</p></td>
<td align="left"><p>Sélectionnez l’un des éléments suivants:</p>
<ul>
<li><p><strong>Utilisez le nom de domaine utilisé lors du démarrage de l’espace de travail </strong> , rejoignez le domaine entré par l’utilisateur final lors de la connexion au client MED-V.</p>
<p>Pour définir le mappage de NetBIOS sur les noms de domaine complets, cliquez sur <strong> table de mappage de domaine global </strong> . Dans la table de mappage de domaine global, cliquez sur <strong> ajouter </strong> , entrez un <strong> nom de domaine NetBIOS </strong> et un <strong> nom de domaine complet </strong> , puis cliquez sur <strong> OK </strong> .</p></li>
<li><p><strong>Utiliser le nom de domaine suivant </strong> : Rejoignez le domaine spécifié; entrez un nom de domaine et un nom de domaine NetBIOS dans les champs correspondants.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Unité d’organisation</p></td>
<td align="left"><p>Une unité d’organisation (UO) pourra être spécifiée pour joindre l’ordinateur à une UO spécifique. Le format doit suivre un nom distinctif d’unité d’organisation: UO = &lt; unité d’organisation &gt; , &lt; contrôleur &gt; de domaine (par exemple, UO = QATest, DC = il, DC = MED-V, DC = com).</p>
<div class="alert">
<strong>Warning</strong><br/><p>Une seule unité d’organisation de niveau est prise en charge, comme le montre l’exemple ci-dessus.</p>
</div>
<div>
 
</div></td>
</tr>
</tbody>
</table>

 

### <a href="" id="bkmk-checkconnectivityproperties"></a>

**Vérifier les propriétés de connectivité**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Propriété</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Adresse IP</p></td>
<td align="left"><p>Adresse IP du serveur sur lequel vous vérifiez la connexion.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Port</p></td>
<td align="left"><p>Port du serveur sur lequel vous vérifiez la connexion.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Délai d’expiration dépassé</p></td>
<td align="left"><p>Nombre de secondes d’attente avant le dépassement du délai d’une réponse.</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="bkmk-commandlineproperties"></a>

**Propriétés de la ligne de commande**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Propriété</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Path</p></td>
<td align="left"><p>Chemin d’accès de la ligne de commande.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Arguments</p></td>
<td align="left"><p>Arguments de ligne de commande.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Attendre la fin</p></td>
<td align="left"><p>Activez la case à cocher pour attendre un retour avant de poursuivre avec les actions de script.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Erreur Échec</p></td>
<td align="left"><p>Activez cette case à cocher si le retour est différent de la valeur spécifiée.</p>
<p>Entrez la valeur indiquant la réussite de la commande.</p>
<p>Par défaut: <strong> 0</strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Effectuer une seule fois</p></td>
<td align="left"><p>Activez cette case à cocher pour exécuter la ligne de commande une seule fois. Si le script échoue ou est annulé, cette commande n’est pas réexécutée.</p></td>
</tr>
<tr class="even">
<td align="left"><p>La ligne de commande suivante entraîne un redémarrage de Windows dans l’espace de travail</p></td>
<td align="left"><p>Activez cette case à cocher si la ligne de commande entraîne un redémarrage après achèvement.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Autoriser les interactions</p></td>
<td align="left"><p>Activez cette case à cocher si la commande nécessite une interaction utilisateur.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Message de progression</p></td>
<td align="left"><p>Message à afficher à l’utilisateur lorsque la commande est en cours d’exécution.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Message d’échec</p></td>
<td align="left"><p>Message à afficher à l’utilisateur en cas d’échec de la commande.</p></td>
</tr>
</tbody>
</table>

 

Lors de la configuration de l’action de ligne de commande, plusieurs variables peuvent être utilisées comme indiqué dans le tableau suivant.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Paramètre</th>
<th align="left">Valeur</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>%MEDVUser%</p></td>
<td align="left"><p>Nom d’utilisateur authentifié.</p></td>
<td align="left"><p>Nom d’utilisateur authentifié MED-V. Le nom d’utilisateur et le mot de passe peuvent être utilisés dans le script de configuration de l’ordinateur virtuel du domaine.</p></td>
</tr>
<tr class="even">
<td align="left"><p>%MEDVPassword%</p></td>
<td align="left"><p>Un mot de passe authentifié.</p></td>
<td align="left"><p>Mot de passe authentifié MED-V. Le nom d’utilisateur et le mot de passe peuvent être utilisés dans le script de configuration de l’ordinateur virtuel du domaine.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>%MEDVDomain%</p></td>
<td align="left"><p>Domaine configuré.</p></td>
<td align="left"><p>Domaine configuré dans l’authentification MED-V. Il peut être utilisé sur le script de configuration de l’ordinateur virtuel.</p></td>
</tr>
<tr class="even">
<td align="left"><p>%DesiredMachineName%</p></td>
<td align="left"><p>Nom de l’ordinateur.</p></td>
<td align="left"><p>Nom d’ordinateur unique configuré dans l’application de gestion. Il peut être utilisé dans le script de configuration de l’ordinateur virtuel.</p></td>
</tr>
</tbody>
</table>

 

## Rubriques connexes


[Comment configurer l'installation d'ordinateur virtuel pour un espace de travail MED-V](how-to-configure-the-virtual-machine-setup-for-a-med-v-workspacemedvv2.md)

[Comment configurer les propriétés du modèle de nom d'ordinateur virtuel](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md)

 

 





