---
title: Récupération d'un lecteur déplacé
description: Récupération d'un lecteur déplacé
author: dansimp
ms.assetid: 0d38ce7e-bc64-473e-ae85-99b7099ca758
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: 9e7e03846e0a94902b699377043237c651939a07
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809899"
---
# Récupération d'un lecteur déplacé
Cette rubrique explique comment utiliser le site Web d’administration et de contrôle (également appelé support technique) pour récupérer un lecteur de système d’exploitation déplacé après avoir été chiffré par l’administration et la surveillance de Microsoft BitLocker (MBAM). Lorsqu’un lecteur est déplacé, il n’accepte plus le code confidentiel utilisé dans l’ordinateur précédent, car le processeur du module de plateforme sécurisée (TPM) a changé. Pour récupérer le lecteur déplacé, vous devez obtenir l’ID de clé de récupération pour récupérer le mot de passe de récupération.

Pour récupérer un lecteur déplacé, vous devez utiliser la zone de **récupération de lecteur** du site Web d’administration et de surveillance. Pour accéder à la zone de **récupération du lecteur** , vous devez disposer du rôle utilisateurs du support technique MBAM ou du rôle MBAM Advanced support Users. Pour plus d’informations sur ces rôles, voir [planification pour les comptes et groupes MBAM 2,5](planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles).

**Pour récupérer un lecteur déplacé**
1.  Sur l’ordinateur qui contient le lecteur déplacé, démarrez l’ordinateur en mode WinRE (Windows Recovery Environment) ou démarrez l’ordinateur à l’aide de Microsoft diagnostic and Recovery Tools (DaRT).

2.  Après le démarrage de l’ordinateur avec WinRE ou DaRT, MBAM traitera le lecteur du système d’exploitation déplacé comme un lecteur de données fixe. MBAM affiche alors l’ID du mot de passe de récupération du lecteur et vous demande le mot de passe de récupération.

    **Remarques**  Dans certains cas, vous serez peut-être en mesure de cliquer sur **j’ai oublié le code confidentiel** lors du processus de démarrage, puis d’entrer le mode de récupération pour afficher l’ID de la clé de récupération.

     

3.  Utilisez l’ID de clé de récupération pour récupérer le mot de passe de récupération et déverrouillez le lecteur à partir du site Web d’administration et de surveillance. Pour obtenir des instructions, reportez-vous à la rubrique récupération d' [un lecteur en mode récupération](how-to-recover-a-drive-in-recovery-mode-mbam-25.md).

    Si le lecteur déplacé a été configuré de manière à utiliser un processeur de TPM sur l’ordinateur d’origine, procédez comme suit. Dans le cas contraire, le processus de récupération est terminé.

4.  Après avoir déverrouillé le lecteur et terminé le processus de démarrage, ouvrez une invite de commandes en mode WinRE et utilisez la `manage-bde` commande pour déchiffrer le lecteur. L’utilisation de cet outil est le seul moyen de supprimer le TPM plus le protecteur de code confidentiel sans le processeur du TPM d’origine. Pour plus d’informations sur la `manage-bde` commande, voir [Manage-bde](https://go.microsoft.com/fwlink/?LinkId=393567).

5.  Lorsque la suppression est terminée, redémarrez l’ordinateur normalement. L’agent MBAM va mettre en œuvre la stratégie pour chiffrer le disque avec le TPM et le code confidentiel du nouvel ordinateur.



## Rubriques connexes


[Gestion de BitLocker avec MBAM2.5](performing-bitlocker-management-with-mbam-25.md)

 

## Vous avez une suggestion pour MBAM?
- Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring) 
- Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





