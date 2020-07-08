---
title: Gestion de MBAM1.0
description: Gestion de MBAM1.0
author: dansimp
ms.assetid: 02ffb093-c364-4837-bbe8-23d4c09fbd3d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7eecef4e82680b08fde1b1bef88487a6fc156fe4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811357"
---
# Gestion de MBAM1.0


Après avoir effectué toutes les opérations de planification nécessaires, puis déployé le programme d’administration et de surveillance de BitLocker (MBAM), vous pouvez configurer MBAM pour qu’il s’exécute de manière très disponible lors de son utilisation pour gérer les opérations de chiffrement d’entreprise BitLocker. Les informations contenues dans cette section décrivent les options de haute disponibilité pour MBAM, ainsi que le déplacement des fonctionnalités de MBAM Server si nécessaire.

## Pack d’administration MBAM


Le pack d’administration MicrosoftSystemCenterOperationsManager pour MBAM est disponible en téléchargement dans le centre de téléchargement Microsoft.

Ce pack d’administration surveille les interactions critiques dans l’infrastructure côté serveur, telles que les connexions entre les services Web et les bases de données et les appels opérationnels entre les sites Web et leur service Web de support technique. Il télécharge également les demandes entre les clients de bureau et leurs points de terminaison de service Web de réception correspondants.

[Pack d’administration et de surveillance Microsoft BitLocker](https://go.microsoft.com/fwlink/p/?LinkId=258390)

## Garantir une disponibilité élevée pour MBAM 1,0


MBAM est conçu pour être tolérant aux pannes. Si un serveur devient indisponible, les utilisateurs ne doivent pas être touchés par le négatif. Les informations contenues dans cette section peuvent être utilisées pour configurer une installation MBAM très disponible.

[Haute disponibilité de MBAM1.0](high-availability-for-mbam-10.md)

## Déplacer les fonctionnalités de MBAM 1,0 vers un autre serveur


Lorsque vous avez besoin de déplacer une fonctionnalité de MBAM Server d’un ordinateur serveur vers un autre, il existe un ordre spécifique et des étapes requises à suivre pour éviter la perte de productivité et de données. Cette section décrit les étapes à suivre pour déplacer une ou plusieurs fonctionnalités de MBAM Server vers un autre ordinateur.

[Déplacement de composants MBAM1.0 vers un autre ordinateur](how-to-move-mbam-10-features-to-another-computer.md)

## Autres ressources pour la mise à jour de MBAM


[Opérations de MBAM1.0](operations-for-mbam-10.md)

 

 





