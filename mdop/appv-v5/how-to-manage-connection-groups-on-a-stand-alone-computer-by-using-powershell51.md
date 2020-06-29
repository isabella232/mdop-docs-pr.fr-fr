---
title: Comment gérer des groupes de connexion sur un ordinateur autonome à l'aide de PowerShell
description: Comment gérer des groupes de connexion sur un ordinateur autonome à l'aide de PowerShell
author: dansimp
ms.assetid: e1589eff-d306-40fb-a0ae-727190dafe26
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: ab120f7089619fa01885d5182313dc33fc47f827
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805316"
---
# Comment gérer des groupes de connexion sur un ordinateur autonome à l'aide de PowerShell


Un groupe de connexion App-V vous permet d’exécuter toutes les applications virtuelles en tant qu’ensemble de packages définis dans un environnement virtuel unique. Par exemple, vous pouvez virtualiser une application et ses plug-ins en utilisant des packages distincts, mais les exécuter au sein d’un groupe de connexion unique.

Un fichier XML de groupe de connexion définit le groupe de connexion qui s’exécute sur l’ordinateur sur lequel vous avez installé le client App-V. Pour plus d’informations sur le fichier XML du groupe de connexion et sur la manière de le configurer, voir [à propos du fichier de groupe de connexion](about-the-connection-group-file51.md).

Cette rubrique décrit les procédures suivantes:

-   [Pour ajouter et publier les packages App-V dans le groupe de connexions](#bkmk-add-pub-pkgs-in-cg)

-   [Pour ajouter et activer le groupe de connexions sur le client App-V](#bkmk-add-enable-cg-on-clt)

-   [Pour activer ou désactiver un groupe de connexions pour un utilisateur spécifique](#bkmk-enable-cg-for-user-poshtopic)

-   [Pour autoriser seuls les administrateurs à activer les groupes de connexion](#bkmk-admin-only-posh-topic-cg)

<a href="" id="bkmk-add-pub-pkgs-in-cg"></a>*Pour ajouter et publier les packages App-V dans le groupe de connexions**

1.  Pour ajouter et publier les packages App-V 5,1 sur l’ordinateur exécutant le client App-V, tapez la commande suivante:

    Add-AppvClientPackage-path c:\\tmpstore\\quartfin.AppV | Publisher-AppvClientPackage

2.  Répétez l' **étape 1** de cette procédure pour chaque package dans le groupe de connexion.

<a href="" id="bkmk-add-enable-cg-on-clt"></a>**Pour ajouter et activer le groupe de connexions sur le client App-V**

1.  Ajoutez le groupe de connexions en entrant la commande suivante:

    Add-AppvClientConnectionGroup-Path c:\\tmpstore\\financ.xml

2.  Activez le groupe de connexions en entrant la commande suivante:

    Enable-AppvClientConnectionGroup – nom «applications financières»

    Lorsque des applications virtuelles figurant dans les packages membres sont exécutées sur l’ordinateur cible, elles s’exécutent à l’intérieur de l’environnement virtuel du groupe de connexion et sont disponibles pour toutes les applications virtuelles dans les autres packages du groupe de connexion.

<a href="" id="bkmk-enable-cg-for-user-poshtopic"></a>**Pour activer ou désactiver un groupe de connexions pour un utilisateur spécifique**

1.  Passez en revue la description du paramètre et la configuration requise:

    -   Ce paramètre permet à un administrateur d’activer ou de désactiver un groupe de connexion pour un utilisateur spécifique.

    -   Pour utiliser ce paramètre, vous devez utiliser le correctif logiciel App-V 5,0 SP2 package 5 ou version ultérieure.

    -   Vous pouvez exécuter cette cmdlet à partir de la session utilisateur ou administrateur.

    -   Vous devez être connecté avec des informations d’identification d’administrateur pour utiliser le paramètre.

    -   L’utilisateur final doit être connecté.

    -   Vous devez indiquer l’identificateur de sécurité (SID) de l’utilisateur final.

2.  Utilisez les applets de commande suivantes, puis ajoutez le paramètre facultatif **-UserSid** **qui représente l’identificateur de sécurité** (SID) de l’utilisateur final:

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Applet de commande</th>
    <th align="left">Exemples</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Enable-AppVClientConnectionGroup</p></td>
    <td align="left"><p>Enable-AppVClientConnectionGroup "ConnectionGroupA"-UserSID S-1-2-34-56789012-3456789012-345678901-2345</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Disable-AppVClientConnectionGroup</p></td>
    <td align="left"><p>Disable-AppVClientConnectionGroup "ConnectionGroupA"-UserSID S-1-2-34-56789012-3456789012-345678901-2345</p></td>
    </tr>
    </tbody>
    </table>

<a href="" id="bkmk-admin-only-posh-topic-cg"></a>**Pour autoriser seuls les administrateurs à activer les groupes de connexion**

1.  Passez en revue la description et la configuration requise pour l’utilisation de cette cmdlet:

    -   Utilisez cette cmdlet et ce paramètre pour configurer le client App-V de façon à ce que seuls les administrateurs (et non les utilisateurs finaux) puissent activer ou désactiver les groupes de connexion.

    -   Vous devez utiliser au minimum App-V 5,0 SP3 pour pouvoir utiliser cette applet de cmdlet.

2.  Exécutez l’applet de commande et le paramètre suivants:

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Applet de commande</th>
    <th align="left">Paramètre et valeurs</th>
    <th align="left">Exemple</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Set-AppvClientConfiguration</p></td>
    <td align="left"><p>–RequirePublishAsAdmin</p>
    <ul>
    <li><p>0-faux</p></li>
    <li><p>1-vrai</p></li>
    </ul></td>
    <td align="left"><p>Set-AppvClientConfiguration – RequirePublishAsAdmin1</p></td>
    </tr>
    </tbody>
    </table>



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## Rubriques connexes


[Opérations d'App-V5.1](operations-for-app-v-51.md)

[Administration d'App-V5.1 à l'aide de PowerShell](administering-app-v-51-by-using-powershell.md)









