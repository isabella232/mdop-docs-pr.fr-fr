---
title: Identifier le nombre d'instances MED-V
description: Identifier le nombre d'instances MED-V
author: dansimp
ms.assetid: edea9bdf-a28c-4d24-9298-7bd6536c3a94
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 22f7d54318d2dc489461474e5531c5162d8c087d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810446"
---
# Identifier le nombre d'instances MED-V


Vous devez déterminer le nombre d’instances de MED-V et définir l’étendue de chaque instance pour pouvoir concevoir l’infrastructure du serveur. Une instance MED-V inclut les éléments suivants:

-   Serveur MED-V et espaces de travail MED-V stockés sur le serveur, y compris les autorisations Active Directory.

-   Une base de données SQL Server qui stocke des événements client. Il est possible que la base de données soit partagée par plusieurs instances MED-V.

-   Référentiel d’image pour les images MED-V compactées. Le référentiel est susceptible d’être partagé par plusieurs instances MED-V.

-   La console de gestion utilisée pour créer et empaqueter des images, et créer des espaces de travail MED-V. La console ne peut pas être utilisée simultanément par plusieurs instances MED-V, mais elle peut être déconnectée d’un serveur MED-V, puis connectée à un serveur MED-V différent.

-   Les clients MED-V qui reçoivent des espaces de travail MED-V et qui peuvent les utiliser à partir du serveur.

Les instances MED-V distinctes ne peuvent pas être intégrées ou partager des espaces de travail MED-V. Par conséquent, chaque instance supplémentaire décentralise la gestion de la virtualisation.

## Déterminer le nombre d’instances MED-V requises


Commencez par supposer que vous utilisez une instance MED-V. Prenez en compte les conditions suivantes et ajoutez des instances supplémentaires pour chaque condition qui s’appliquent à votre infrastructure.

-   Nombre d’utilisateurs pris en charge: chaque instance MED-V peut prendre en charge jusqu’à 5 000 de clients actifs simultanément. L’activation simultanée signifie que le client est en ligne avec le serveur MED-V et qu’il envoie des sondages au serveur pour les mises à jour de stratégie et d’image, ainsi que les événements. Si votre infrastructure inclura plus de 5 000 utilisateurs actifs, ajoutez une instance pour chaque utilisateur 5 000.

-   Utilisateurs des domaines non approuvés: MED-V Server associe les autorisations d’espace de travail MED-V aux utilisateurs et/ou groupes Active Directory. Cela nécessite que les utilisateurs MED-V existent dans la limite de confiance du serveur MED-V. Ajoutez une instance MED-V pour chaque groupe d’utilisateurs MED-V figurant dans un domaine distinct et non fiable.

-   Clients dans les réseaux isolés: Déterminez si des clients résident dans des réseaux isolés et nécessitent par conséquent une instance MED-V distincte. Par exemple, les organisations isolent souvent les réseaux de laboratoire des réseaux de production. Ajoutez une instance MED-V pour chaque réseau isolé qui contient des clients MED-V.

-   Exigences organisationnelles: l’organisation risque de nécessiter la gestion d’un groupe de clients par une instance MED-V distincte pour des raisons de sécurité, par exemple lorsque des applications sensibles sont transmises uniquement à un ensemble restreint d’utilisateurs au sein d’un domaine. Par exemple, le service Payroll risque de refuser aux utilisateurs d’autres services l’accès à l’instance MED-V qui stocke une stratégie de traitement de la paie. De plus, si l’organisation utilise un modèle de gestion distribuée, une instance MED-V séparée est susceptible d’être requise pour chaque groupe d’entreprise disposant de clients MED-V pour permettre au groupe de gérer son propre environnement virtualisé. Ajoutez une instance MED-V pour chaque exigence d’organisation distincte.

-   Considérations juridiques: les problèmes liés à la sécurité nationale ou à la confidentialité et à la législation fiduciaire peuvent nécessiter une séparation de certaines données ou empêcher d’autres données de traverser les frontières nationales. Le cas échéant, ajoutez d’autres instances MED-V pour répondre à ce besoin.

Après avoir déterminé le nombre d’instances MED-V requises pour votre infrastructure, ainsi que le raisonnement pour chacun d’eux, donnez un nom à chaque instance.

 

 





