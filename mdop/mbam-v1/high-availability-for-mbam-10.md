---
title: Haute disponibilité de MBAM1.0
description: Haute disponibilité de MBAM1.0
author: dansimp
ms.assetid: 5869ecf8-1056-4c32-aecb-838a37e05d39
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 1227967d647cbfbc16967b5936066fd73d2412e2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811111"
---
# Haute disponibilité de MBAM1.0


Cette rubrique décrit comment configurer une installation hautement disponible de Microsoft BitLocker administration et de la surveillance (MBAM).

## Scénarios de haute disponibilité pour MBAM


La surveillance et l’administration de BitLocker Microsoft (MBAM) sont conçues pour être tolérantes aux pannes. Si un serveur devient indisponible, les utilisateurs ne doivent pas être touchés par le négatif. Par exemple, si l’agent MBAM ne peut pas se connecter au serveur Web MBAM, les utilisateurs ne doivent pas être invités à effectuer une action.

Lorsque vous planifiez votre installation de MBAM, prenez en compte les problèmes suivants qui peuvent affecter la disponibilité du service MBAM:

-   Chiffrement du lecteur et mot de passe de récupération: si un mot de passe de récupération ne peut pas être de confiance, le chiffrement ne démarrera pas sur l’ordinateur client.

-   Chargement des données d’état de conformité: si le serveur qui héberge le service de rapport d’état de conformité n’est pas disponible, les données de conformité ne seront pas conservées.

-   Accès à la clé de récupération du support technique: si l’assistance ne peut pas accéder aux informations de la base de données MBAM, ils ne seront pas en mesure de fournir des clés de récupération aux utilisateurs.

-   Disponibilité des rapports: les rapports ne seront pas disponibles si le serveur qui héberge les rapports de compatibilité et d’audit n’est pas disponible.

Le principal souci de la haute disponibilité MBAM est la disponibilité de la récupération de clé BitLocker. Si le support technique ne peut pas fournir de clés de récupération, les utilisateurs qui sont verrouillés ne peuvent pas déverrouiller leur ordinateur. Pour éviter ce problème, envisagez d’implémenter des serveurs et bases de données Web redondants pour garantir une disponibilité élevée.

Pour plus d’informations sur l’évolutivité et la disponibilité de MBAM, voir le [livre blanc](https://go.microsoft.com/fwlink/p/?LinkId=229025) sur l’évolutivité d’MBAM ( https://go.microsoft.com/fwlink/p/?LinkId=229025) .

Pour obtenir des instructions générales sur la haute disponibilité de Microsoft SQL Server, voir [haute disponibilité](https://go.microsoft.com/fwlink/p/?LinkId=221504) ( https://go.microsoft.com/fwlink/p/?LinkId=221504) .

Pour obtenir des instructions générales sur la disponibilité et l’extensibilité pour les serveurs Web, voir [disponibilité et extensibilité](https://go.microsoft.com/fwlink/p/?LinkId=221503) ( https://go.microsoft.com/fwlink/p/?LinkId=221503) .

## Rubriques connexes


[Gestion de MBAM1.0](maintaining-mbam-10.md)

 

 





