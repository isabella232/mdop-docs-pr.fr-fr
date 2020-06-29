---
title: Procédure pour configurer le serveur afin qu'il soit approuvé pour délégation
description: Procédure pour configurer le serveur afin qu'il soit approuvé pour délégation
author: dansimp
ms.assetid: d8d11588-17c0-4bcb-a7e6-86b5e4ba7e1c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7164b3046671853216b870d68e651fed4fd84695
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807230"
---
# Procédure pour configurer le serveur afin qu'il soit approuvé pour délégation


Lorsque vous installez le logiciel serveur de gestion Microsoft Application Virtualization (App-V), vous pouvez choisir de l’installer à l’aide d’une architecture système distribuée. Si vous installez la console, le service Web de gestion et la base de données sur des ordinateurs différents, vous devez configurer le serveur Internet Information Services (IIS) pour qu’il soit approuvé pour la délégation. Cela est nécessaire, car le service Web de gestion tente de se connecter au magasin de données App-V en utilisant les informations d’identification de l’administrateur d’application-V qui utilise la console. Le serveur de base de données sur lequel est installé le magasin de données n’accepte pas les informations d’identification de l’administrateur du serveur IIS, sauf si le serveur IIS est configuré pour être approuvé pour la délégation, et le service Web de gestion ne sera pas en mesure de se connecter au magasin de données App-V.

**Remarques**  Si vous installez le logiciel serveur d’administration des applications sur un serveur unique et placez le magasin de données sur un serveur distinct, il existe une situation dans laquelle vous devez tout de même configurer le serveur pour qu’il soit approuvé pour la délégation, même si le service Web de gestion et la console de gestion se trouvent sur le même serveur. Cette situation se produit si vous devez vous connecter au service Web de gestion dans la console à l’aide de l’option **utiliser d’autres informations d’identification** .

 

Le type de délégation que vous pouvez utiliser dépend du niveau de fonctionnement du domaine que vous avez configuré dans votre infrastructure services de domaine Active Directory (AD DS). Le tableau suivant répertorie les types de délégation qui peuvent être configurés pour chaque niveau fonctionnel de domaine pour App-V. Les instructions détaillées suivent le tableau.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Niveau fonctionnel du domaine</th>
<th align="left">Niveaux de délégation disponibles</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows 2000 natif</p></td>
<td align="left"><ul>
<li><p>Aucune délégation (par défaut)</p></li>
<li><p>Délégation sans contraintes</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2003, Windows Server 2008 ou Windows Server 2008 R2</p></td>
<td align="left"><ul>
<li><p>Aucune délégation (par défaut)</p></li>
<li><p>Délégation sans contraintes ¹</p></li>
<li><p>Délégation contrainte (utiliser des protocoles Kerberos uniquement)</p></li>
<li><p>Délégation contrainte (utiliser n’importe quel protocole d’authentification) ¹</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

¹ non recommandée.

## Pour configurer la délégation sans contraintes lorsque le niveau de fonctionnalité du domaine est Windows 2000 natif


Sur le contrôleur de domaine du domaine de votre serveur Web, procédez comme suit.

****

1.  Cliquez sur **Démarrer**, sur **Outils d’administration**, puis sur **utilisateurs et ordinateurs Active Directory**.

2.  Développez domaine, puis développez le dossier ordinateurs.

3.  Dans le volet droit, cliquez avec le bouton droit sur le nom de l’ordinateur du serveur Web, puis cliquez sur **Propriétés**.

4.  Dans l’onglet **général** , assurez-vous que la case à cocher **approuver l’ordinateur pour la délégation** est activée.

5.  Cliquez sur **OK**.

## Pour configurer la délégation sans contraintes lorsque le niveau de fonctionnalité du domaine est Windows Server 2003, Windows Server 2008 ou Windows Server 2008 R2


Sur le contrôleur de domaine du domaine de votre serveur Web, procédez comme suit.

****

1.  Cliquez sur **Démarrer**, sur **Outils d’administration**, puis sur **utilisateurs et ordinateurs Active Directory**.

2.  Développez domaine, puis développez le dossier ordinateurs.

3.  Dans le volet droit, cliquez avec le bouton droit sur le nom de l’ordinateur du serveur Web, sélectionnez **Propriétés**, puis cliquez sur l’onglet **délégation** .

4.  Cliquez pour sélectionner **approuver cet ordinateur pour la délégation à tout service (Kerberos uniquement)**.

5.  Cliquez sur **OK**.

## Pour configurer la délégation contrainte lorsque le niveau de fonctionnalité du domaine est Windows Server 2003, Windows Server 2008 ou Windows Server 2008 R2


Sur le contrôleur de domaine du domaine de votre serveur Web, procédez comme suit.

****

1.  Cliquez sur **Démarrer**, sur **Outils d’administration**, puis sur **utilisateurs et ordinateurs Active Directory**.

2.  Développez domaine, puis développez le dossier ordinateurs.

3.  Dans le volet droit, cliquez avec le bouton droit sur le nom de l’ordinateur du serveur Web, sélectionnez **Propriétés**, puis cliquez sur l’onglet **délégation** .

4.  Cliquez pour sélectionner **approuver cet ordinateur pour la délégation aux services spécifiés uniquement**.

5.  Vérifiez que l’option **utiliser le protocole Kerberos uniquement** est sélectionnée, puis cliquez sur **OK**.

6.  Cliquez sur le bouton **Ajouter** . Dans la boîte de dialogue **Ajouter des services** , cliquez sur **utilisateurs ou ordinateurs**, puis recherchez ou tapez le nom de Microsoft SQL Server qui dispose du magasin de données App-V et recevez les informations d’identification de l’utilisateur à partir d’IIS. Cliquez sur **OK**.

7.  Dans la liste **services disponibles** , sélectionnez le service MSSQLSvc qui indique le numéro de port sur lequel Microsoft SQL Server accepte les connexions pour la base de données App-V (le port par défaut est 1433). Cliquez sur **OK**.

### Étapes supplémentaires pour configurer IIS 7 pour la délégation contrainte

Si vous exécutez le service Web de gestion sur un serveur IIS 7, vous devez effectuer les étapes suivantes pour définir la variable *useAppPoolCredentials* de services Internet (IIS) sur true.

1.  Ouvrez une fenêtre d’invite de commandes avec élévation de privilèges. Pour ouvrir une fenêtre d’invite de commandes avec élévation de privilèges, cliquez sur **Démarrer**, sur **tous les programmes**, sur **accessoires**, cliquez avec le bouton droit sur **invite de commandes**, puis cliquez sur **exécuter en tant qu’administrateur**.

2.  Accédez à%windir%\\system32\\inetsrv.

3.  Tapez **appcmd.exe définir config-section: System. webServer/Security/Authentication/WindowsAuthentication-useAppPoolCredentials: true**, puis appuyez sur entrée.

 

 





