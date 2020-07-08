---
title: Planification de la sécurité de Sequencer
description: Planification de la sécurité de Sequencer
author: dansimp
ms.assetid: 8043cb02-476d-4c28-a850-903a8ac5b2d3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: bf1e85e24d93d373add38b5efe51ceb40faae24e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806497"
---
# Planification de la sécurité de Sequencer


Intégrez les meilleures pratiques en matière d’implémentation, le plus tôt possible, lors de la configuration de la virtualisation des applications (App-V), afin que l’implémentation de votre Sequencer soit opérationnelle et plus sécurisée. Si vous avez déjà configuré le Sequencer, utilisez les recommandations suivantes pour revoir vos décisions de conception et les analyser du point de vue de la sécurité.

**Important**  
Le Sequencer App-V recueille et déploie toutes les informations sur l’application enregistrées sur l’ordinateur exécutant le Sequencer. Vous devez vous assurer que tous les utilisateurs qui accèdent à l’ordinateur exécutant le Sequencer possèdent des informations d’identification d’administration. Les utilisateurs disposant d’informations d’identification de compte d’utilisateur ne doivent pas avoir accès pour contrôler le contenu du package et les fichiers du package. Si vous effectuez un séquençage sur un ordinateur exécutant les services Bureau à distance (anciennement services Terminal Server), assurez-vous qu’il s’agit d’un ordinateur dédié au séquençage et que les utilisateurs auxquels des informations d’identification de compte d’utilisateur ne sont pas connectées lors du séquençage.



## Meilleures pratiques en matière de sécurité des séquenceurs


Tenez compte des scénarios suivants et des meilleures pratiques associées lors de l’implémentation et de l’utilisation du Sequencer Application Virtualization (App-V):

-   **Analyse antivirus sur l’ordinateur exécutant le Sequencer**, nous vous conseillons de numériser l’ordinateur exécutant le Sequencer pour détecter des virus, puis de désactiver tout logiciel antivirus et de détection de malware sur l’ordinateur exécutant le Sequencer lors du processus de séquençage. Cela accélère le processus de séquençage et empêche les composants logiciels antivirus et anti-programme malveillant d’interférer avec le processus de séquençage. Ensuite, installez le package séquencé sur un ordinateur qui n’exécute pas le Sequencer et, après l’installation réussie, analysez cet ordinateur pour détecter des virus. S’il détecte des virus, le fabricant du logiciel doit être contacté pour les informer des fichiers sources infectés et demander une mise à jour de la source d’installation sans virus. Le Sequencer peut éventuellement être analysé après la phase d’installation et, en cas de détection de virus, le fabricant du logiciel doit être contacté comme mentionné ci-dessus.

    **Remarque**  
    Si un virus est détecté dans une application, l’application ne doit pas être déployée sur des ordinateurs cibles.



-   **Capture des listes de contrôle d’accès (ACL) sur les fichiers NTFS**: le Sequencer App-V capture les autorisations du système de fichiers NTFS pour les fichiers surveillés lors de l’installation du produit. Cette fonctionnalité vous permet de reproduire plus précisément le comportement souhaité de l’application, comme s’il était installé en local et non virtualisé. Dans certains cas, une application peut stocker des informations auxquelles les utilisateurs ne sont pas destinés à accéder dans les fichiers de l’application. Par exemple, une application peut stocker des informations d’identification dans un fichier au sein de l’application. Si les ACL ne sont pas appliquées sur le package, un utilisateur peut potentiellement afficher puis utiliser ces informations en dehors de l’application.

    **Remarque**  
    Vous ne devez pas séquencer des applications qui stockent des informations spécifiques à la sécurité non chiffrées, telles que des mots de passe, etc.



~~~
During the installation phase, you can modify the default permissions of the files if necessary. After completion of the sequencing process, but before saving the package, you can choose whether to enforce security descriptors that were captured during the installation of the application. By default, App-V will enforce the security descriptors specified during the installation of the application. If you turn off security descriptor enforcement, you should test the application to ensure the removal of associated Access Control Lists (ACL) will not cause the application to perform unexpectedly.
~~~

-   Le **Sequencer ne capture pas les ACL du Registre**; bien que le Sequencer capture les listes de contrã’le d’accès du système de fichiers NTFS lors de la phase d’installation du séquençage, il n’enregistre pas les ACL pour le registre. Les utilisateurs auront un accès complet à toutes les clés de Registre pour les applications virtuelles à l’exception des services. Toutefois, si un utilisateur modifie le registre d’une application virtuelle, la modification sera stockée dans un magasin spécifique (**uservol \ _sftfs \ _V1. pkg**) et n’affectera pas les autres utilisateurs.

-   **Services d’application**: App-V fournit une prise en charge des services d’application qui font partie d’une application virtualisée. Toutefois, dans l’environnement virtuel, le contexte de sécurité qu’il exécute est limité. Les seuls contextes de sécurité pris en charge dans un environnement virtuel sont système local, service local et service réseau. Lors du séquençage, si un contexte de sécurité est spécifié pour un service d’application différent des trois prises en charge, le contexte de sécurité du système local est appliqué dans l’environnement virtuel. Si le service d’application est configuré pour utiliser un service local ou un service réseau, il sera honoré dans l’environnement virtuel. Il est possible de configurer le compte de service lors du processus de séquençage à l’aide des trois contextes de sécurité.

-   **Informations de sécurité persistantes**: lorsque vous séquençagez des applications, vous pouvez installer l’application en tant qu’utilisateur, ou vous pouvez développer une méthode automatisée pour l’installation de l’application lors d’une analyse. Toutes les informations qui ne sont pas exclues du package seront capturées dans le cadre de ce package afin que l’application puisse exécuter les ressources nécessaires dans un environnement virtualisé. Certaines applications stockent des informations de sécurité sensibles (par exemple, des mots de passe) lors de l’installation. en cas de non-protection persistante, ces informations de sécurité sont accessibles à d’autres utilisateurs ayant accès au package. Lors de l’installation, si l’installation d’une application demande un mot de passe ou d’autres informations sensibles à la sécurité, consultez la documentation pour vous assurer qu’elle n’est pas conservée (supprimée après l’installation) ou, si elle est persistée, qu’elle est protégée (chiffrée).

-   **Sécuriser les packages d’application virtuelle**: enregistrez toujours les packages d’application virtuels dans un emplacement sécurisé sur le réseau pour protéger le package contre toute falsification ou corruption.

## Rubriques connexes


[Planification de la sécurité et de la protection](planning-for-security-and-protection.md)









