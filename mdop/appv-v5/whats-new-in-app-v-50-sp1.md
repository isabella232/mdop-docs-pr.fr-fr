---
title: Nouveautés dans App-V5.0 SP1
description: Nouveautés dans App-V5.0 SP1
author: dansimp
ms.assetid: e97c2dbb-7b40-46a0-8137-9ee4fc2bd071
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2542d0cc5a544d26b3279b24063cf3ef428b9f39
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804812"
---
# Nouveautés dans App-V5.0 SP1


Cette section s’utilise pour les utilisateurs qui connaissent déjà App-V et qui souhaitent savoir ce qui a changé dans App-V 5,0 SP1. Si vous n’avez pas encore l’habitude d’utiliser l’application-V, vous devez commencer par lire la [planification pour App-v 5,0](planning-for-app-v-50-rc.md).

## Modifications apportées aux fonctionnalités standard


Les sections suivantes contiennent des informations sur les modifications apportées aux fonctionnalités standard pour App-V 5,0 SP1.

### Modifications apportées aux langues prises en charge

Pour plus d’informations, voir [à propos de App-V 5,0 SP1](about-app-v-50-sp1.md).

La liste suivante contient des informations supplémentaires sur les nouveaux modules linguistiques:

-   Les modules linguistiques App-V 5.0 SP1 sont intégrés au programme d’installation de **appv\_xxx\_setup.exe** pour tous les composants App-v 5,0.

-   Lorsque vous exécutez le programme d’installation, le module linguistique le plus approprié est automatiquement installé en fonction des paramètres régionaux du système d’exploitation associé exécuté sur l’ordinateur cible.

-   Si des modules linguistiques supplémentaires sont requis, vous devez extraire ces modules linguistiques du programme d’installation en exécutant la commande suivante: `appv_xxx_setup.exe /Layout /LayoutDir=”<path>”` . Après l’exécution, le contenu du programme d’installation est extrait à l’emplacement spécifié.

-   Vous devez installer le module linguistique souhaité en appliquant le fichier d’installation Windows du module linguistique approprié. Par exemple, **appv\_hib\_LP\_jmmb\_x86.msi** ou **appv\_hib\_LP\_jmmb\_x64.msi**, où **Hib** fait référence au composant et **jmmb** fait référence aux paramètres régionaux.

## Prise en charge améliorée de Microsoft Office 2010


**Kit de séquençage Microsoft Office 2010 pour la virtualisation des applications 5,0** : permet aux utilisateurs d’avoir une interface cohérente à l’aide d’une version virtualisée de Microsoft Office 2010. Le **Kit de séquençage Microsoft office 2010 pour application virtualization 5,0** est utilisé conjointement avec le **Kit de déploiement de Microsoft Office 2010 pour App-V** et fournit également le service de gestion des licences Microsoft Office 2010 requis.






## Rubriques connexes


[À propos d'App-V5.0](about-app-v-50.md)

 

 





