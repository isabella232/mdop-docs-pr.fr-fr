---
title: Authentification des utilisateurs MED-V
description: Authentification des utilisateurs MED-V
author: dansimp
ms.assetid: aaf96eb6-91d1-4f4d-9854-5fc73c7ae7ab
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 14c1e95a94f2da76b6b6c5ebd9d4cf14dcf839a7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810824"
---
# Authentification des utilisateurs MED-V


L’authentification des utilisateurs finaux de Microsoft Enterprise Desktop Virtualization (MED-V) 2,0 est un problème de sécurité important. Dans ce contexte, l’authentification consiste à vérifier l’identité de l’utilisateur final de MED-V.

La section suivante fournit des informations et des instructions sur l’authentification des utilisateurs finaux dans MED-V.

## Authentification des utilisateurs dans MED-V


L’authentification dans MED-V se produit généralement à deux niveaux: lorsqu’un utilisateur accède d’abord à MED-V et chaque fois qu’il modifie son mot de passe.

En fonction de la manière dont vous avez configuré les paramètres MED-V pour l’authentification, l’utilisateur final est généralement invité à entrer son mot de passe lors de la première utilisation de MED-V ou lors de sa première tentative d’ouverture d’une application publiée.

Vous pouvez contrôler plusieurs aspects de l’authentification des utilisateurs finaux, y compris les éléments suivants:

Si les informations d’identification que l’utilisateur final entre sont stockées dans le gestionnaire d’informations d’identification

Quelle est la façon dont l’utilisateur final dispose de la possibilité d’entrer et d’enregistrer son mot de passe?

En fonction du processus préféré de votre entreprise pour gérer l’authentification des utilisateurs finaux, vous pouvez spécifier si la mise en cache des informations d’identification se produit pour un espace de travail MED-V particulier. La mise en cache des informations d’identification d’un utilisateur final est utile, car elles sont uniquement invitées une seule fois pour leur mot de passe. Si l’utilisateur final n’est pas autorisé à enregistrer son mot de passe ou s’il ne le décide pas à chaque fois qu’il entame une nouvelle session MED-V, il doit le retaper. Par exemple, si MED-V est configuré pour démarrer lorsque l’utilisateur final se connecte à l’hôte mais que l’authentification est désactivée, l’utilisateur final est uniquement invité une fois pendant l’ouverture de session. Dans ce cas, les informations d’identification sont valides jusqu’à ce que l’utilisateur final se déconnecte de l’hôte.

Le cas échéant, vous pouvez utiliser le gestionnaire d’informations d’identification pour supprimer les informations d’identification de l’utilisateur final stockées.

Par défaut, le stockage des informations d’identification est désactivé, mais vous pouvez modifier ce paramètre à l’aide de l’une des méthodes suivantes:

**Lors de la création du package d’espace de travail MED-V**. Pour plus d’informations, voir [créer un package d’espace de travail MED-V](create-a-med-v-workspace-package.md).

**Après avoir déployé l’espace de travail MED-V**. Modifiez le paramètre de cmdlet UxCredentialCacheEnabled pour définir la clé de Registre Terminal Services. Pour plus d’informations, consultez l’aide de Windows PowerShell.

Après le déploiement d’un espace de travail MED-V, vous pouvez définir votre préférence pour l’authentification des utilisateurs finaux en modifiant la stratégie des services Terminal Server nommée DisablePasswordSaving. DisablePasswordSaving indique si la case à cocher enregistrement du mot de passe s’affiche dans la fenêtre de dialogue du client RDP et si l’invite d’identification MED-V s’affiche.

Vous trouverez ci-après le chemin de stratégie de la stratégie des services Terminal Server nommée DisablePasswordSaving.

**Regedit**

HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Virtual Machine\\Policies\\DisablePasswordSaving

**Remarque**  
Les modifications que vous apportez à DisablePasswordSaving affectent uniquement l’invite RDP à une machine virtuelle.



Le tableau suivant répertorie les différentes façons dont vous pouvez configurer vos paramètres pour le stockage des informations d’identification et les effets des différentes configurations:

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Valeur</th>
<th align="left">Configuration</th>
<th align="left">Résultat</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>DisablePasswordSaving</p></td>
<td align="left"><p><strong>Désactivé</strong></p></td>
<td align="left"><p>L’invite MED-V est présentée et une case à cocher accepter est disponible et désactivée. Si l’utilisateur final sélectionne la case à cocher, les informations d’identification sont mises en cache pour une utilisation ultérieure. L’utilisateur final a également l’avantage d’être invité uniquement à l’expiration du mot de passe.</p>
<p></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>Si l’utilisateur n’a pas activé la case à cocher, l’invite du client Connexion Bureau à distance (RDC) est présentée à la place de l’invite MED-V et la case à cocher accepter est désactivée. Si l’utilisateur final sélectionne la case à cocher, les informations d’identification du client de RDC sont stockées pour une utilisation ultérieure.</p>
<div class="alert">
<strong>Important</strong><br/><p>RDC ne valide pas les informations d’identification à l’entrée de l’utilisateur final. Si l’utilisateur final met en cache les informations d’identification par le biais de l’invite CBD, il est possible que des informations d’identification incorrectes soient stockées. Dans ce cas, vous devez supprimer les informations d’identification incorrectes dans le gestionnaire d’informations d’identification Windows.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>DisablePasswordSaving</p></td>
<td align="left"><p><strong>Activé</strong></p></td>
<td align="left"><div class="alert">
<strong>Remarque</strong><br/><p>Cette configuration est plus sécurisée, car elle ne permet pas aux informations d’identification de l’utilisateur final d’être mises en cache.</p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



Par défaut, l’installation de MED-V définit une clé de Registre dans l’invité pour supprimer l’invite «mot de passe sur le point d’expirer». L’utilisateur final est invité à entrer un mot de passe pour la modification du mot de passe sur l’hôte. Les informations d’identification mises à jour sur l’hôte sont transmises à l’invité.

**Vigilance**  
Si vous utilisez une stratégie de groupe dans votre environnement, sachez qu’elle peut remplacer la clé de Registre à l’origine de la réapparition des invites de mot de passe.



### Problèmes de sécurité liés à l’authentification

Même si la mise en cache des informations d’identification de l’utilisateur final offre une meilleure utilisation de l’utilisateur, vous devez connaître les risques liés.

Lorsque la mise en cache des informations d’identification est activée, les informations d’identification de domaine de l’utilisateur final sont stockées dans un format réversible dans le gestionnaire d’informations d’identification Windows. Par conséquent, un attaquant peut écrire un outil qui s’exécute comme un processus de niveau système ou un processus utilisateur final, et qui récupère les informations d’identification de l’utilisateur final. Vous pouvez limiter ce risque uniquement en définissant DisablePasswordSaving sur **Enabled**.

Ce problème existe lorsque l’authentification MED-V est désactivée, mais que le paramètre de stratégie des services Terminal Server est activé.

## Rubriques connexes


[Meilleures pratiques de sécurité pour les opérations de MED-V](security-best-practices-for-med-v-operations.md)









