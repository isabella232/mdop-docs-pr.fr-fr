---
title: Maintenance d'App-V5.1
description: Maintenance d'App-V5.1
author: dansimp
ms.assetid: 5abd17d3-e8af-4261-b914-741ae116b0e7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 431ad65507a5699358159c73eaf9f3cf0dee33b7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805107"
---
# Maintenance d'App-V5.1


Après avoir effectué toutes les opérations de planification nécessaires, puis le déploiement de App-V 5,1, vous pouvez utiliser les informations suivantes pour gérer l’infrastructure App-V 5,1.

## <a href="" id="move-the-app-v-5-1-server-"></a>Déplacer le serveur App-V 5,1


Le serveur App-V 5,1 se connecte à la base de données App-V 5,1. Par conséquent, vous pouvez installer le composant de gestion sur n’importe quel ordinateur du réseau, puis le connecter à la base de données App-V 5,1.

[Comment déplacer le serveur App-V vers un autre ordinateur](how-to-move-the-app-v-server-to-another-computer51.md)

## <a href="" id="determine-if-an-app-v-5-1-application-is-running-virtualized-"></a>Déterminer si une application application-V 5,1 est en cours d’exécution


Les éditeurs de logiciels indépendants qui souhaitent déterminer si une application est en cours d’exécution avec App-V 5,1 ou une version ultérieure, doivent ouvrir un objet nommé appelé **AppVVirtual &lt; - &gt; PID** dans l’espace de noms par défaut. Par exemple, l’API Windows **GetCurrentProcessId ()** peut être utilisée pour obtenir l’ID du processus actuel, par exemple 4052, et si un objet d’événement nommé appelé **AppVVirtual-4052** peut être ouvert avec succès à l’aide de **OpenEvent ()** dans l’espace de noms par défaut pour l’accès en lecture, l’application est virtuelle. En cas d’échec de l’appel de **OpenEvent ()** , l’application n’est pas virtuelle.

De plus, les éditeurs de logiciels indépendants qui souhaitent virtualiser ou ne pas virtualiser les appels sur des API spécifiques avec App-V 5,1 ou une version ultérieure peuvent utiliser les fonctions **VirtualizeCurrentThread ()** et **CurrentThreadIsVirtualized ()** implémentées dans le module AppEntSubsystems32.dll. Celles-ci fournissent un moyen d’attirer l’œil sur un composant en aval qui ne doit pas être virtualisé.






## Autres ressources pour la maintenance de App-V 5,1


[Opérations d'App-V5.1](operations-for-app-v-51.md)

 

 





