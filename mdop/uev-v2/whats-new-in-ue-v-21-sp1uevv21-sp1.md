---
title: Nouveautés dans UE-V2.1SP1
description: Nouveautés dans UE-V2.1SP1
author: dansimp
ms.assetid: 9a40c737-ad9a-4ec1-b42b-31bfabe0f170
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 1f4b6210d95795c352a7ef1402b0353c6f52774b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812348"
---
# Nouveautés dans UE-V2.1SP1


User performance Virtualization 2,1 SP1 fournit les nouvelles fonctionnalités par rapport à UE-V 2,1. Les [notes de publication de Microsoft User Interface Virtualization (UE-v) 2,1 SP1](microsoft-user-experience-virtualization--ue-v--21-sp1-release-notes.md) fournissent des informations supplémentaires sur la version d’UE-v 2,1 SP1.

## Prise en charge de Windows 10


UE-V 2,1 SP1 ajoute la prise en charge de Windows 10, en plus des logiciels pris en charge dans les versions antérieures d’UE-V.

### Compatibilité avec Microsoft Azure

Windows 10 permet aux utilisateurs d’entreprise de synchroniser les paramètres des applications Windows et les paramètres du système d’exploitation Windows sur Azure plutôt que sur OneDrive. Vous pouvez utiliser la fonctionnalité de synchronisation Windows 10 entreprise conjointement avec UE-V pour les ordinateurs appartenant à un domaine local uniquement. Pour activer la coexistence entre Windows 10 et UE-V, vous devez désactiver les modèles UE-V suivants à l’aide de PowerShell sur chaque client ou stratégie de groupe.

Dans stratégie de groupe, sous le nœud Microsoft User performance, configurez les paramètres de stratégie suivants:

-   Activer «ne pas synchroniser les applications Windows»

-   Désactiver «synchroniser les paramètres Windows»

### Comportement de la synchronisation des paramètres modifié pour la prise en charge de Windows 10

UE-V 2,1 SP1 répartir les paramètres de la barre des tâches entre les appareils Windows 10. Toutefois, UE-V ne synchronise pas les paramètres de la barre des tâches entre les appareils et appareils Windows 10 exécutant d’anciens systèmes d’exploitation.

Par ailleurs, UE-V 2,1 SP1 ne synchronise pas les paramètres entre Microsoft Calculator dans Windows 10 et la calculatrice Microsoft dans les systèmes d’exploitation précédents.

## Prise en charge ajoutée pour les imprimantes réseau itinérantes


UE-V 2,1 SP1 permet aux imprimantes réseau d’avoir accès aux périphériques de sorte que l’utilisateur ait accès à ses imprimantes réseau lorsqu’il est connecté à un appareil du réseau. Cela comprend l’itinérance de l’imprimante définie par défaut.

L’itinérance d’imprimantes dans UE-V nécessite l’un des scénarios suivants:

-   Le serveur d’impression peut télécharger le pilote requis lorsqu’il est itinérant vers un nouvel appareil.

-   Le pilote de l’imprimante du réseau errant est préinstallé sur n’importe quel appareil qui a besoin d’accéder à cette imprimante réseau.

-   Le pilote de l’imprimante peut être obtenu à partir de Windows Update.

**Remarques**  La fonctionnalité d’itinérance d’imprimante UE-V n’effectue **pas** de paramètres d’impression ou de préférences tels que l’impression recto verso.

 

## Modèle d’emplacement des paramètres d’Office 2013


UE-V 2,1 et 2,1 SP1 incluent le modèle d’emplacement des paramètres Microsoft Office 2013 avec une prise en charge améliorée des signatures Outlook. Nous avons ajouté la synchronisation des paramètres de signature par défaut pour les courriers électroniques, les réponses et les transferts. Les clients n’ont plus besoin de choisir les paramètres de signature par défaut.

**Remarques**  Un profil Outlook doit être créé pour tout appareil sur lequel un utilisateur souhaite synchroniser sa signature Outlook. Si ce n’est pas le cas, l’utilisateur peut en créer un, puis redémarrer Outlook sur cet appareil pour activer la synchronisation des signatures.

 

Auparavant, UE-V incluait les modèles d’emplacement des paramètres Microsoft Office 2010 qui ont été automatiquement distribués et enregistrés auprès de l’agent UE-V. UE-V 2,1 utilise Office 365 pour déterminer si les paramètres d’Office 2013 sont itinérants par Office 365. Si les paramètres sont itinérants par Office 365, ils ne sont pas itinérants par UE-V. La [vue d’ensemble des paramètres utilisateur et itinérance pour Office 2013](https://go.microsoft.com/fwlink/p/?LinkID=391220) fournit des informations supplémentaires.

Pour activer la synchronisation des paramètres avec UE-V 2,1, effectuez l’une des opérations suivantes:

-   Utiliser une stratégie de groupe pour désactiver la synchronisation d’Office 365

-   Ne pas activer l’interface de synchronisation Office 365 lors de l’installation d’Office 2013

UE-V 2,1 inclut [les modèles office 2013 et office 2010](https://technet.microsoft.com/library/dn458932.aspx#autosyncsettings). Cette version supprime les modèles Office 2007. Les utilisateurs peuvent toujours utiliser les modèles Office 2007 d’UE-V 2,0 ou une version antérieure et peuvent toujours obtenir les modèles de la Galerie de modèles UE-V située [ici](https://go.microsoft.com/fwlink/p/?LinkID=246589).






## Rubriques connexes


[Prise en main d'UE-V2.x](get-started-with-ue-v-2x-new-uevv2.md)

[Préparer un déploiement UE-V 2. x](prepare-a-ue-v-2x-deployment-new-uevv2.md)

[Notes de publication pour Microsoft User Experience Virtualization (UE-V)2.1SP1](microsoft-user-experience-virtualization--ue-v--21-sp1-release-notes.md)

 

 





