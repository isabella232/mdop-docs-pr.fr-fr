---
title: Détection des modifications réseau qui affectent MED-V
description: Détection des modifications réseau qui affectent MED-V
author: dansimp
ms.assetid: fd29b95a-cda2-464d-b86d-50b6bd64b4ca
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b5f43c30dee9ef8e06a7ae226849a4f21e83257c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809917"
---
# Détection des modifications réseau qui affectent MED-V


La solution 2,0 de Microsoft Enterprise Desktop Virtualization (MED-V) vous permet de configurer votre environnement pour détecter certaines modifications réseau qui peuvent se produire après le déploiement des espaces de travail MED-v et qui peut affecter MED-V.

Cette fonctionnalité inclut un composant s’exécutant dans le système d’exploitation invité, qui est averti de la modification de la configuration réseau de l’ordinateur hôte. Il permet à une application non-Microsoft ou d’une autre application en cours d’exécution dans l’invité de résoudre les points de terminaison réseau pour lesquels l’application ESD ou l’application est résolue.

**Remarques**  Cette fonctionnalité n’est disponible que si l’ordinateur virtuel est configuré pour le mode traduction d’adresses réseau (NAT). S’il s’agit d’un ordinateur virtuel configuré pour le mode pont, aucune indication de modification n’est générée.

 

Cette section fournit des informations et des instructions pour vous aider à surveiller les changements de réseau qui peuvent affecter MED-V.

## Pour détecter les changements de réseau pour MED-V


Après avoir déployé vos espaces de travail MED-V, vous pouvez surveiller les modifications apportées à certaines configurations réseau en préformant les tâches suivantes:

1. Créez un fichier MOF (Managed Object Format) qui cherchera les modifications de configuration réseau que vous souhaitez surveiller. Le code suivant montre un exemple du fichier MOF que vous pouvez créer.

   ``` syntax
   #pragma namespace ("\\\\.\\root\\ccm\\NetworkConfig")

   class CCM_IPConfig
   {
       [NotNull: ToInstance ToSubClass] uint32 AddressFamily; // AF_INET, AF_INET6
       [Key, NotNull: ToInstance ToSubClass] string IPAddress; // IPv4 or IPv6 address
       [NotNull: ToInstance ToSubClass] string SubnetMask; // IPv4 subnet mask
   };

   class CCM_NetworkAdapter
   {
       [Key, NotNull: ToInstance ToSubClass] string Name;
       [NotNull: ToInstance ToSubClass] uint32 DHCPEnabled = 0; 
       [NotNull: ToInstance ToSubClass] uint32 Quarantined = 0; // To check if it is quarantined.
       CCM_IPConfig IPConfigInfo[];
   };

   [singleton]
   class CCM_NetworkAdapters
   {
       [NotNull: ToInstance ToSubClass] String ProviderName; // MED-V or other provider
       CCM_NetworkAdapter AdaptersInfo[];
   };
   ```

2. Compilez le fichier MOF.

3. Installez le fichier MOF dans l’invité.

Une fois que vous avez installé le fichier MOF, vous pouvez créer un abonnement Event qui s’abonne aux événements de création, de modification ou de suppression WMI pour la classe **CCM \ _NetworkAdapters** . Les modifications suivantes sont détectées sur l’hôte:

Quelles sont les modifications apportées à la configuration du réseau, par exemple les modifications apportées à l’adresse IP ou à la carte réseau?

Le réseau est-il disponible ou indisponible?

Le programme d’installation du réseau a-t-il été passé du mode pont au mode NAT?

Le programme d’installation du réseau a-t-il été passé du mode NAT au mode relié?

Un composant MED-V sur l’hôte surveille le réseau de ces modifications, puis signale l’invité du changement. Un composant de l’invité crée une instance WMI permettant de surveiller l’espace de travail MED-V pour ces modifications.

L’abonnement d’événements que vous avez créé avertit par le système WMI lorsque l’un ou plusieurs de ces changements de réseau (création, modification ou suppression) se produisent.

## Rubriques connexes


[Surveiller des espaces de travail MED-V](monitor-med-v-workspaces.md)

[Gérer les paramètres de l'espace de travail MED-V](manage-med-v-workspace-settings.md)

 

 





