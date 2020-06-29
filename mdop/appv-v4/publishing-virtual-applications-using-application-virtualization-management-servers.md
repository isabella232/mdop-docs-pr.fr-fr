---
title: Publication d'applications virtuelles à l'aide de serveurs Application Virtualization Management Server
description: Publication d'applications virtuelles à l'aide de serveurs Application Virtualization Management Server
author: dansimp
ms.assetid: f3d79284-3f82-4ca3-b741-1a80b61490da
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 01b85d73ed0a6a8bf723be381e947fbbc003bf6d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806438"
---
# Publication d'applications virtuelles à l'aide de serveurs Application Virtualization Management Server


Dans le déploiement d’un serveur de virtualisation des applications, les packages d’application virtuels qui ont été séquencés, testés et détectés déployés sont copiés sur le partage de contenu principal à utiliser par le serveur de gestion de la virtualisation des applications. Une fois les packages importés sur le serveur de gestion de la virtualisation des applications, ils peuvent être publiés aux utilisateurs finaux.

**Remarques**  Le partage de contenu doit se trouver sur le stockage de disque connecté du serveur. L’utilisation d’un périphérique de stockage réseau, tel qu’un réseau SAN ou un partage DFS, doit être considérée soigneusement en raison de l’impact sur le réseau.

 

Les applications sont configurées pour les groupes Active Directory. En règle générale, l’administrateur de virtualisation des applications va créer des groupes Active Directory pour chaque application virtuelle à publier, puis ajouter les utilisateurs appropriés à ces groupes. Lorsque les utilisateurs se connectent à leur station de travail, le client de virtualisation des applications effectue par défaut une actualisation de publication en utilisant les informations d’identification de l’utilisateur connecté. L’utilisateur peut alors lancer des applications à partir de n’importe quel emplacement. L’administrateur de virtualisation des applications détermine l’emplacement et le nombre de raccourcis situés sur le système client lors du séquençage de l’application.

**Remarques**  Une *actualisation* de la publication est un appel du serveur de virtualisation des applications qui est défini sur le client de virtualisation des applications, qui permet de déterminer quels raccourcis d’application virtuelle sont envoyés au client pour une utilisation par l’utilisateur final.

 

## Rubriques connexes


[Scénario basé sur un serveur Application Virtualization Server](application-virtualization-server-based-scenario.md)

[Procédure pour publier une application virtuelle sur le client](how-to-publish-a-virtual-application-on-the-client.md)

[Présentation des composants du système Application Virtualization](overview-of-the-application-virtualization-system-components.md)

[Planification de votre solution de diffusion en continu dans une implémentation basée sur un serveur Application Virtualization Server](planning-your-streaming-solution-in-an-application-virtualization-server-based-implementation.md)

 

 





