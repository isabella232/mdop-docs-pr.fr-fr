---
title: Récupération d'un lecteur déplacé
description: Récupération d'un lecteur déplacé
author: dansimp
ms.assetid: 0c7199d8-9463-4f44-9af3-b70eceeaff1d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e73e0878a3102d56494feb33efa69182029988c2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804596"
---
# Récupération d'un lecteur déplacé


Lorsque vous déplacez un lecteur de système d’exploitation déjà chiffré à l’aide du système d’administration et de surveillance Microsoft BitLocker (MBAM), vous devez résoudre certains problèmes. Une fois qu’un code confidentiel est attaché au nouvel ordinateur, il n’accepte pas le code confidentiel de démarrage utilisé dans l’ordinateur précédent. Le système considère que le code confidentiel n’est pas valide en raison de la modification apportée au processeur du module de plateforme sécurisée (TPM). Vous devez obtenir un ID de clé de récupération pour récupérer le mot de passe de récupération pour pouvoir utiliser le lecteur déplacé. Pour cela, procédez comme suit.

**Pour récupérer un lecteur déplacé**

1.  Sur l’ordinateur qui contient le lecteur déplacé, démarrez en mode WinRE (Windows Recovery Environment) ou démarrez l’ordinateur à l’aide de Microsoft Diagnostics and Recovery Tools (DaRT).

2.  Une fois que l’ordinateur est démarré avec WinRE ou DaRT, MBAM considère le lecteur du système d’exploitation déplacé comme un lecteur de données. MBAM affiche alors l’ID du mot de passe de récupération du lecteur et vous demande le mot de passe de récupération.

    **Remarques**  Dans certains cas, vous serez peut-être en mesure de cliquer sur **j’ai oublié le code confidentiel** lors du processus de démarrage pour entrer le mode de récupération. L’ID de la clé de récupération s’affiche également.

     

3.  Sur le site Web d’administration MBAM, utilisez l’ID de clé de récupération pour récupérer le mot de passe de récupération et déverrouillez le lecteur.

4.  Si le lecteur déplacé a été configuré de manière à utiliser un processeur de TPM sur l’ordinateur d’origine, vous devez effectuer des étapes supplémentaires après avoir déverrouillé le lecteur et terminer le processus de démarrage. Dans le mode WinRE, ouvrez une invite de commandes et utilisez l’outil **Manage-bde** pour déchiffrer le lecteur. L’utilisation de cet outil est le seul moyen de supprimer la protection du TPM-plus-PIN sans le processeur du TPM d’origine.

5.  Au terme de la suppression, démarrez le système normalement. L’agent MBAM va mettre en œuvre la politique de chiffrer le lecteur avec le code confidentiel plus le nouveau de l’ordinateur.

## Rubriques connexes


[Gestion de BitLocker avec MBAM](performing-bitlocker-management-with-mbam.md)

 

 





