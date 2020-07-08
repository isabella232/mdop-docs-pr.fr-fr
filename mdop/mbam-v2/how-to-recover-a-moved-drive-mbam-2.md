---
title: Récupération d'un lecteur déplacé
description: Récupération d'un lecteur déplacé
author: dansimp
ms.assetid: 697cd78d-962c-411e-901a-2e9220ba6552
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: bd0d43f2eea95fe71225a50e7fa68d4fb1c35485
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810931"
---
# Récupération d'un lecteur déplacé


Lorsque vous déplacez un lecteur de système d’exploitation qui est chiffré à l’aide de l’administration et de la surveillance de BitLocker (MBAM), le lecteur n’accepte pas le code confidentiel qui a été utilisé sur un ordinateur précédent en raison de la modification apportée au processeur du module de plateforme sécurisée (TPM). Pour utiliser le lecteur déplacé, vous avez besoin d’un moyen d’obtenir l’ID de clé de récupération pour récupérer le mot de passe de récupération. Utilisez la procédure suivante pour récupérer un lecteur qui a été déplacé.

**Pour récupérer un lecteur déplacé**

1.  Sur l’ordinateur qui contient le lecteur déplacé, démarrez l’ordinateur en mode WinRE (Windows Recovery Environment) ou démarrez l’ordinateur à l’aide de Microsoft diagnostic and Recovery Tools (DaRT).

2.  Une fois que l’ordinateur est démarré avec WinRE ou DaRT, l’administration et la surveillance de BitLocker utilise le lecteur du système d’exploitation déplacé comme lecteur de données. MBAM affiche alors l’ID du mot de passe de récupération du lecteur et vous demande le mot de passe de récupération.

    **Remarques**  Dans certains cas, vous serez peut-être en mesure de cliquer sur **j’ai oublié le code confidentiel** lors du processus de démarrage, puis d’entrer le mode de récupération pour afficher l’ID de la clé de récupération.

     

3.  Utilisez l’ID de clé de récupération pour récupérer le mot de passe de récupération et déverrouillez le lecteur à partir du site Web d’administration et de surveillance.

4.  Si le lecteur déplacé a été configuré de manière à utiliser un processeur de TPM sur l’ordinateur d’origine, vous devez effectuer des étapes supplémentaires après avoir déverrouillé le lecteur et terminer le processus de démarrage. Dans le mode WinRE, ouvrez une invite de commandes et utilisez l’outil **Manage-bde** pour déchiffrer le lecteur. L’utilisation de cet outil est le seul moyen de supprimer le protecteur du TPM plus code confidentiel sans le processeur du TPM d’origine.

5.  Lorsque la suppression est terminée, démarrez l’ordinateur normalement. L’agent MBAM va mettre en œuvre la stratégie pour chiffrer le lecteur avec le code confidentiel plus (TPM) de l’ordinateur.

## Rubriques connexes


[Gestion de BitLocker avec MBAM](performing-bitlocker-management-with-mbam-mbam-2.md)

 

 





