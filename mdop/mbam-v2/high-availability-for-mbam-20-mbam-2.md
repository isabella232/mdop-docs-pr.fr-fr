---
title: Haute disponibilité de MBAM2.0
description: Haute disponibilité de MBAM2.0
author: dansimp
ms.assetid: 244ee013-9e2a-48d2-b842-4e10594fd74f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6482a099d96aee731f81368b8b787325e592c453
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810728"
---
# Haute disponibilité de MBAM2.0


Cette rubrique fournit des informations de base sur une installation hautement disponible de Microsoft BitLocker administration et analyse (MBAM). Les scénarios de haute disponibilité ne sont pas entièrement pris en charge dans cette version de MBAM, ce qui signifie qu’ils ne sont pas décrits ici. Nous vous conseillons de rechercher des blogs et des forums connexes dans lesquels les utilisateurs décrivent la façon dont ils ont correctement configuré la haute disponibilité pour MBAM dans leur environnement.

## Scénarios de haute disponibilité pour MBAM


L’administration et la surveillance de Microsoft BitLocker sont conçues pour être tolérantes aux pannes. Si un serveur devient indisponible, l’utilisateur ne doit pas être touché de façon négative. Par exemple, si l’agent MBAM ne peut pas se connecter au serveur Web MBAM, les utilisateurs ne doivent pas être invités à effectuer une action.

Lorsque vous planifiez votre installation de MBAM, prenez en compte les éléments suivants qui peuvent affecter la disponibilité du service MBAM:

-   Le chiffrement du lecteur et le mot de passe de récupération: si un mot de passe de récupération ne peut pas être de confiance, le chiffrement ne démarre pas sur l’ordinateur client.

-   Chargement des données d’état de conformité: si le serveur qui héberge le service de rapport d’état de conformité n’est pas disponible, les données de conformité ne restent pas actuelles.

-   Accès à la clé de récupération du support technique: si le support technique ne peut pas accéder aux informations de la base de données MBAM, l’assistance technique ne peut pas fournir de clés de récupération aux utilisateurs.

-   Disponibilité des rapports: si le serveur qui héberge les rapports de compatibilité et d’audit n’est pas disponible, les rapports ne seront pas disponibles.

## <a href="" id="how-the-mbam-backup-uses-the-volume-shadow-copy-service--vss--"></a>Comment la sauvegarde MBAM utilise le service de cliché instantané de volume (VSS)


MBAM 2.0 fournit un writer de service de cliché instantané de volume (VSS) appelé Microsoft BitLocker Management and Management Writer, qui facilite la sauvegarde de la base de données d’audit et de conformité et de la base de données de récupération.

Le programme d’installation de MBAM Server Windows enregistre MBAM VSS Writer. Tout échec de l’inscription du writer VSS entraîne la restauration de l’installation de MBAM Server. Dans le cas où la base de données d’audit et de conformité, ainsi que la base de données de récupération, sont installées sur différents serveurs, une instance distincte de MBAM VSS Writer est inscrite sur chaque serveur. Le scripteur VSS MBAM dépend du writer SQL Server VSS. Le writer SQL Server VSS est inscrit dans le cadre de l’installation de Microsoft SQL Server. Toute technologie de sauvegarde qui utilise des Writers VSS pour effectuer une sauvegarde peut découvrir le scripteur VSS MBAM.

## Rubriques connexes


[Gestion de MBAM2.0](maintaining-mbam-20-mbam-2.md)

 

 





