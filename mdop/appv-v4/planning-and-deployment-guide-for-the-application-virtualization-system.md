---
title: Guide de planification et de déploiement pour le système de virtualisation des applications
description: Guide de planification et de déploiement pour le système de virtualisation des applications
author: dansimp
ms.assetid: 6c012e33-9ac6-4cd8-84ff-54f40973833f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 10bcac26fddae2f0e5826dbd7335adda06d3987e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806514"
---
# Guide de planification et de déploiement pour le système de virtualisation des applications


Microsoft Application Virtualization Management permet de rendre les applications accessibles aux ordinateurs des utilisateurs finaux sans avoir à installer les applications directement sur ces ordinateurs. C’est possible par le biais d’un processus connu sous le nom de *Sequencer de l’application*, qui permet à chaque application de s’exécuter dans son propre environnement virtuel autonome sur l’ordinateur client. Les applications séquencées sont isolées les unes des autres, ce qui évite les conflits d’application, mais peut néanmoins interagir avec l’ordinateur client.

Le client de virtualisation des applications est le composant système de virtualisation des applications qui permet à l’utilisateur final d’interagir avec les applications une fois qu’elles ont été publiées sur l’ordinateur. Le client gère l’environnement virtuel dans lequel les applications virtuelles s’exécutent sur chaque ordinateur. Après avoir installé le client sur un ordinateur, les applications doivent être mises à disposition de l’ordinateur par le biais d’un processus connu sous le nom de *publication*, qui permet à l’utilisateur final d’exécuter les applications virtuelles. Le processus de publication place les icônes et raccourcis des applications virtuelles sur l’ordinateur, généralement sur le bureau Windows ou dans le menu **Démarrer** , et place également les informations relatives à la définition et au type de fichier dans l’ordinateur. La publication rend également le contenu du package d’application disponible pour l’ordinateur de l’utilisateur final.

Le contenu du package d’application virtuel peut être placé sur un ou plusieurs serveurs de virtualisation des applications afin de pouvoir être diffusé aux clients à la demande et mis en cache localement. Les serveurs de fichiers et les serveurs Web peuvent également être utilisés comme serveurs de diffusion en continu, ou le contenu peut être placé directement sur l’ordinateur de l’utilisateur final, par exemple, si vous utilisez un système de distribution de logiciels électronique, tel que Microsoft Endpoint Manager. Dans une implémentation multiserveur, la mise à jour du contenu du package et sa mise à jour sur tous les serveurs de diffusion en continu nécessite une solution complète de gestion des packages. En fonction de la taille de votre organisation, il se peut que vous deviez disposer de nombreuses applications virtuelles accessibles aux utilisateurs finaux dans le monde entier. Gestion des packages pour vous assurer que les applications appropriées soient disponibles pour tous les utilisateurs dans lesquels et quand ils ont besoin d’y accéder sont donc une exigence essentielle.

Le Guide de planification et de déploiement de l’Application Virtualization fournit des informations pour vous aider à mieux comprendre et déployer l’application virtualisation des applications Microsoft et ses composants. Il fournit également des procédures pas à pas permettant d’implémenter les scénarios de déploiement clés.

## Dans cette section


<a href="" id="planning-for-application-virtualization-system-deployment"></a>[Planification du déploiement du système Application Virtualization](planning-for-application-virtualization-system-deployment.md)  
Fournit les conseils nécessaires à la planification de l’implémentation et du déploiement de votre système de virtualisation d’applications.

<a href="" id="application-virtualization-deployment-and-upgrade-considerations"></a>[Aspects à prendre en compte pour le déploiement et la mise à niveau d'Application Virtualization](application-virtualization-deployment-and-upgrade-considerations.md)  
Fournit des informations sur la configuration matérielle et logicielle requise pour l’installation des différents composants de virtualisation des applications, ainsi que des informations de mise à niveau.

<a href="" id="electronic-software-distribution-based-scenario"></a>[Scénario basé sur une distribution électronique de logiciels](electronic-software-distribution-based-scenario.md)  
Fournit des informations sur le déploiement de la virtualisation des applications à l’aide d’un système de distribution de logiciels électronique (ESD).

<a href="" id="application-virtualization-server-based-scenario"></a>[Scénario basé sur un serveur Application Virtualization Server](application-virtualization-server-based-scenario.md)  
Fournit des informations sur le déploiement de la virtualisation des applications à l’aide du serveur de gestion de la virtualisation des applications.

<a href="" id="stand-alone-delivery-scenario-for-application-virtualization-clients"></a>[Scénario de distribution autonome pour les clients Application Virtualization Client](stand-alone-delivery-scenario-for-application-virtualization-clients.md)  
Décrit le déploiement de la virtualisation d’application en mode autonome, sans recours à des ressources serveur ou de type ESD.

<a href="" id="application-virtualization-reference"></a>[Référence à Application Virtualization](application-virtualization-reference.md)  
Contenu de référence technique détaillé relatif à l’installation et à la gestion des composants système.

 

 





