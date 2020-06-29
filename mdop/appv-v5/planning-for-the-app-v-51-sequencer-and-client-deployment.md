---
title: Planification du déploiement d'App-V5.1 Sequencer et Client
description: Planification du déploiement d'App-V5.1 Sequencer et Client
author: dansimp
ms.assetid: d92f8773-fa7d-4926-978a-433978f91202
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: 31a0296814b16ba1c776dca522423fc7b6b6ed96
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804993"
---
# Planification du déploiement d'App-V5.1 Sequencer et Client


Pour pouvoir commencer à utiliser Microsoft Application Virtualization (App-V) 5,1, vous devez installer le Sequencer App-V 5,1, le client App-V 5,1 et éventuellement le magasin de contenu partagé App-V 5,1. Les sections suivantes traitent de la planification de ces installations.

## Planification du déploiement de Sequencer App-V 5,1


App-V 5,1 utilise un processus appelé séquençage pour créer des applications virtuelles et des packages d’application. Le séquençage nécessite l’utilisation d’un ordinateur qui exécute le Sequencer App-V 5,1.

**Remarques**  Pour plus d’informations sur les nouvelles fonctionnalités de Sequencer App-V 5,1, voir la section **améliorations** de Sequencer [sur à propos de App-v 5,1](about-app-v-51.md).

 

L’ordinateur qui exécute le Sequencer App-V 5,1 doit respecter la configuration minimale requise. Pour obtenir la liste de ces exigences, voir [configurations App-V 5,1 prises en charge](app-v-51-supported-configurations.md).

Idéalement, il est recommandé d’installer le Sequencer sur un ordinateur exécutant en tant qu’ordinateur virtuel. Cela vous permet de rétablir plus facilement l’ordinateur exécutant le Sequencer dans l’État «Clean» avant de séquencer une autre application. Lorsque vous installez le Sequencer à l’aide d’une machine virtuelle, vous devez effectuer les étapes suivantes:

1.  Installez toutes les conditions préalables de Sequencer associées.

2.  Installez le Sequencer.

3.  Prenez une photo de l’environnement.

**Important**  L’équipe de sécurité de votre entreprise doit revoir et approuver le plan de processus de séquençage. Pour des raisons de sécurité, nous vous conseillons de conserver les opérations de Sequencer d’un laboratoire différent de l’environnement de production. La disposition de séparation peut être simple ou aussi complète que nécessaire, en fonction de vos besoins métiers. Le séquençage des ordinateurs doit être en mesure de se connecter au réseau d’entreprise pour copier les packages finis sur les serveurs de production. Toutefois, étant donné que les ordinateurs de séquençage sont généralement utilisés sans protection antivirus, ils ne doivent pas être sur le réseau d’entreprise non protégé. Par exemple, vous pouvez être en mesure de fonctionner derrière un pare-feu ou un segment réseau isolé. Vous pouvez également être en mesure d’utiliser des machines virtuelles configurées pour partager un réseau virtuel isolé. Suivez les stratégies de sécurité de votre entreprise pour répondre en toute sécurité à ces inquiétudes.

 

## Planification pour le déploiement du client App-V 5,1


Pour exécuter des packages virtualisés sur des ordinateurs cibles, vous devez installer le client App-V 5,1 sur les ordinateurs cibles. Le client App-V 5,1 est le composant qui exécute une application virtualisée sur un ordinateur cible. Le client permet aux utilisateurs d’interagir avec des icônes et des types de fichiers spécifiques pour démarrer des applications virtualisées. Le client permet également d’obtenir le contenu de l’application à partir du serveur de gestion et met en cache le contenu avant le démarrage de l’application par le client. Il existe deux types de clients différents: le client pour les services Bureau à distance, qui est utilisé sur les systèmes serveur hôte de session Bureau à distance et le client App-V 5,1, qui est utilisé pour tous les autres ordinateurs.

Le client App-V 5,1 doit être configuré à l’aide de la ligne de commande du programme d’installation ou d’un script PowerShell une fois l’installation terminée.

Ces paramètres doivent être définis soigneusement à l’avance afin d’accélérer le déploiement du logiciel client App-V 5,1. C’est particulièrement important lorsque vous avez des ordinateurs dans différents bureaux où les clients doivent être configurés pour utiliser des emplacements sources différents.

Vous devez également déterminer la façon dont vous allez déployer le logiciel client. Même s’il est possible de déployer le client manuellement sur chaque ordinateur, la plupart des organisations préfèrent déployer le client par le biais d’un processus automatisé. Une plus grande organisation peut avoir un système de distribution de logiciels électroniques (ESD) opérationnel, qui est un système de déploiement client idéal. S’il n’existe pas de système ESD, vous pouvez utiliser la méthode standard d’installation du logiciel de votre organisation. Les méthodes possibles incluent une stratégie de groupe ou différentes techniques de script. Ce processus de déploiement peut être complexe en fonction de la quantité et de l’emplacement disparate de vos ordinateurs clients. Vous devez utiliser une approche structurée pour vous assurer que tous les ordinateurs obtiennent le client avec la configuration correcte.

Pour obtenir la liste des conditions minimales requises pour le client [, voir conditions préalables pour App-V 5,1](app-v-51-prerequisites.md).

## <a href="" id="bkmk-client-coexist"></a>Planification de la coexistence du client App-V


Vous pouvez déployer le client App-V 5,1 côte à côte avec le client App-V 4,6. La coexistence du client nécessite que vous ajoutiez ou publiiez des applications virtualisées à l’aide d’un fichier de configuration de déploiement ou d’un fichier de configuration utilisateur, car il existe certains paramètres dans ces fichiers de configuration qui doivent être configurés pour que l’application-V 5,1 puisse fonctionner avec des clients App-V 4.6. Lors de la mise à niveau d’un package à l’aide du client ou du serveur, le package doit renvoyer le fichier de configuration. C’est vrai pour tout package doté d’un fichier de configuration correspondant, qui n’est pas spécifique à la coexistence du client. Toutefois, si vous ne soumettez pas le fichier de configuration lors de la mise à niveau du package, l’état du package ne fonctionnera pas comme prévu dans les scénarios de coexistence.

Fichiers de configuration dynamique App-V 5,1 personnaliser un package pour un utilisateur spécifique. Vous devez créer le fichier de configuration utilisateur dynamique (. Xml) ou le fichier de configuration de déploiement dynamique avant de pouvoir les utiliser. Pour créer le fichier, vous avez besoin d’une opération manuelle avancée.

Lorsqu’un fichier de configuration utilisateur dynamique est utilisé, aucune des informations d’application-V 5,1 pour l’extension dans le fichier manifeste n’est utilisée. Cela signifie que le fichier de configuration utilisateur dynamique doit inclure tout ce qui concerne l’extension spécifique à l’application-V 5,1 dans le fichier manifeste, ainsi que les modifications que vous souhaitez apporter (par exemple, suppressions et mises à jour). Pour plus d’informations sur la création d’un fichier de configuration personnalisé, voir [créer un fichier de configuration personnalisé à l’aide de la console de gestion App-V 5,1](how-to-create-a-custom-configuration-file-by-using-the-app-v-51-management-console.md).

## <a href="" id="bkmk-plan-for-scs"></a>Planification du magasin de contenus partagés App-V 5,1 (SCS)


Le mode de stockage de contenu partagé App-V 5,1 permet à l’ordinateur exécutant le client App-V 5,1 d’exécuter des applications virtualisées et aucun contenu de package n’est enregistré sur l’ordinateur exécutant le client App-V 5,1. Les applications virtuelles sont diffusées en continu sur les ordinateurs cibles uniquement lorsque le client le demande.

La liste suivante présente certains des avantages de l’utilisation du magasin de contenus partagés App-V 5,1:

-   Réduction des conflits d’application et d’application multi-utilisateur, et donc d’un besoin réduit de tests de régression

-   Déploiement d’applications accéléré par réduction du risque de déploiement

-   Gestion simplifiée des profils






## <a href="" id="other-resources-for-the-app-v-5-1-deployment-"></a>Autres ressources pour le déploiement d’App-V 5,1


[Envisager de déployer App-V](planning-to-deploy-app-v51.md)

## Rubriques connexes


[Installation de Sequencer](how-to-install-the-sequencer-51beta-gb18030.md)

[Comment déployer App-V Client](how-to-deploy-the-app-v-client-51gb18030.md)

[Déploiement de l’application-V 4,6 et du client App-V 5,1 sur le même ordinateur](how-to-deploy-the-app-v-46-and-the-app-v--51-client-on-the-same-computer.md)

[Installation d'App-V5.1 Client pour le mode Magasin de contenu partagé](how-to-install-the-app-v-51-client-for-shared-content-store-mode.md)

 

 





