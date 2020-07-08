---
title: Vue d'ensemble du déploiement de MED-V2.0
description: Vue d'ensemble du déploiement de MED-V2.0
author: dansimp
ms.assetid: 0b8998ea-c46f-4c81-a304-f380b2ed7cf8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ec2a5f86ac7d63295bd7c550bcb0a90004987e42
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811556"
---
# Vue d'ensemble du déploiement de MED-V2.0


Cette section fournit des informations générales et des instructions sur l’installation et le déploiement de Microsoft Enterprise Desktop Virtualization (MED-V) 2,0.

## Vue d'ensemble


MED-V 2,0 est basé sur un modèle d’application, dans lequel les méthodes que vous utilisez pour déployer des applications peuvent être utilisées pour déployer et gérer MED-V. Une solution MED-V déployée comprend deux composants: l’agent d’hébergement MED-V et l’agent invité. L’agent d’hébergement MED-V est installé sur l’ordinateur de bureau Windows 7 et l’agent invité MED-V est installé sur Windows XP au sein de l’espace de travail MED-V. Le module de création de package de l’espace de travail MED-v inclut également des informations et outils nécessaires pour créer et configurer des espaces de travail MED-V.

**Important**  
MED-V ne prend en charge que l’installation du gestionnaire de package d’espace de travail MED-V, de l’agent hôte MED-V et de l’espace de travail MED-V pour tous les utilisateurs. L’installation de MED-V pour l’utilisateur actuel uniquement en sélectionnant **ALLUSERS = ""** entraîne des échecs lors de l’installation des composants et dans le programme d’installation de l’espace de travail MED-v.



### Fichiers d’installation de MED-V

MED-V inclut les fichiers d’installation suivants nécessaires à l’exécution de MED-V:

**Fichier d’installation de l’agent hôte MED-V**

Le fichier d’installation de l’agent hôte est nommé MED-V\_HostAgent\_Setup.exe. Ce fichier est distribué et installé sur les ordinateurs des utilisateurs finaux concernés dans le cadre de votre déploiement à l’échelle de l’entreprise de MED-V.

**Fichier d’installation du package de création de package de l’espace de travail MED-V**

Le fichier d’installation du package de création de package de l’espace de travail MED-V est nommé MED-V\_WorkspacePackager\_Setup.exe. Utilisez ce fichier pour installer le gestionnaire de package de l’espace de travail MED-V sur un ordinateur sur lequel vous disposez des droits d’administrateur et des autorisations. L’administrateur de bureau utilise le module de création de package de l’espace de travail MED-V pour créer et gérer les espaces de travail MED-V.

**Remarque**  
L’agent d’invité MED-V est automatiquement installé lors de la première configuration.



### Processus de déploiement MED-V

Vous trouverez ci-dessous une présentation générale de l’installation et du processus de déploiement de MED-V:

1.  Installez le gestionnaire de package d’espace de travail MED-V sur l’ordinateur sur lequel vous disposez des informations d’identification d’administration et que vous allez utiliser pour créer les packages d’espace de travail MED-V. Pour plus d’informations, reportez-vous [à la rubrique Comment installer le gestionnaire de package MED-V](how-to-install-the-med-v-workspace-packager.md).

2.  Préparez votre image MED-V et créez vos packages d’espace de travail MED-V en utilisant le gestionnaire de package d’espace de travail MED-V. Pour plus d’informations, reportez-vous à la rubrique [opérations pour MED-V](operations-for-med-v.md).

3.  Déployez les composants MED-V requis au sein de votre entreprise. Les composants requis de MED-V sont Windows Virtual PC, l’agent hôte MED-V et l’espace de travail MED-V.

**Important**  
L’installation des composants MED-V nécessite des informations d’identification d’administration. Si un utilisateur final installe MED-V, il est invité à entrer les informations d’identification d’administration. Vous pouvez également fournir des informations d’identification d’administrateur dans le contexte si vous effectuez une installation à l’aide d’un système de distribution de logiciels électronique (ESD).



### Composants MED-V

Les composants MED-V que vous déployez au sein de votre entreprise sont les suivants:

**PC virtuel Windows**

Les fonctions MED-V au sein d’images virtuelles sur PC Windows pour sa solution de compatibilité. Le PC virtuel Windows et la mise à jour pour Windows 7 (KB977206) sont nécessaires. Pour plus d’informations, voir [configurer les conditions préalables à l’installation](configure-installation-prerequisites.md).

**Fichier d’installation de l’agent hôte MED-V**

MED-V\_HostAgent\_Setup.exe.

**Fichiers d’installation de l’espace de travail MED-V**

Les fichiers d’installation de l’espace de travail MED-V sont créés lorsque vous créez votre package d’espace de travail MED-V, qui se compose des éléments suivants:

Programme exécutable de setup.exe qui exécute l’installation de l’espace de travail MED-V.

Un &lt; programme d’installation du _name &gt; . msi pour MED-V \ _workspace

Un &lt; fichier VHD \ _FileName &gt; . medv, qui est le disque dur virtuel compressé

Fichiers pour paramètres de configuration ( &lt; espace de travail \ _name &gt; . reg et &lt; espace de travail \ _name &gt; . ps1)

Pour déployer MED-V, copiez tous les fichiers d’installation requis sur l’ordinateur hôte ou vers un partage accessible à partir de l’ordinateur hôte. Exécution des fichiers d’installation de composant pour Windows Virtual PC, l’agent hôte MED-V et l’espace de travail MED-V. Ensuite, démarrez l’agent hôte MED-V pour terminer la première fois que vous avez installé le programme MED-V.

Vous pouvez effectuer l’installation manuellement. Toutefois, nous vous recommandons d’utiliser une méthode de distribution de logiciels électronique pour automatiser le déploiement des composants. Pour plus d’informations, reportez-vous [à la rubrique déploiement d’un espace de travail MED-V par le biais d’un système de distribution de logiciels électronique](how-to-deploy-a-med-v-workspace-through-an-electronic-software-distribution-system.md).

**Remarque**  
Pour plus d’informations sur les arguments de ligne de commande disponibles pour contrôler les options d’installation, voir [options de ligne de commande pour les fichiers d’installation de MED-V](command-line-options-for-med-v-installation-files.md).



## Étapes du déploiement


Lorsque vous déployez MED-V au sein de votre entreprise, vous devez prendre en considération les deux points suivants: installation et première configuration.

### Installation

1.  **PC virtuel Windows** : au cours de l’installation, MED-V vérifie le PC virtuel Windows et sa mise à jour requise pour Windows 7 (KB977206). Pour plus d’informations, voir [configurer les conditions préalables à l’installation](configure-installation-prerequisites.md).

    Vous pouvez installer ces composants dans le cadre des installations de Windows 7 avant d’installer MED-V ou vous pouvez les installer dans le cadre de la distribution MED-V. Toutefois, MED-V n’inclut pas de mécanisme de déploiement; elles doivent être déployées à l’aide d’un système de distribution de logiciels électronique (ESD) ou dans le cadre de l’image Windows 7.

    **Important**  
    Lorsque vous installez les composants MED-V à l’aide d’un fichier de commandes, il est recommandé de spécifier le déploiement de PC virtuel Windows et de package de l’espace de travail de l’application MED-V. Cela signifie que Windows Update n’entraîne aucune interférence avec le processus d’installation en nécessitant un redémarrage.



~~~
**Note**  
After you install Windows Virtual PC, the computer must be restarted.
~~~



2. **Agent hôte MED-v** : Installez l’agent hôte MED-v sur l’ordinateur Windows 7 sur lequel med-v sera exécuté. Ce doit être installé avant d’installer l’espace de travail MED-V et de vérifier que le PC virtuel Windows est bien installé.

3. **Espace de travail MED-v** : vous créez les fichiers requis dans le setup.exe programme d’installation à l’aide du programme de création de package de l’espace de travail MED-v. Pour installer l’espace de travail MED-V, exécutez setup.exe. Cela déclenche les autres fichiers si nécessaire. L’installation place une entrée dans le Registre sous la clé d’exécution de l’ordinateur local pour démarrer l’agent hôte MED-V, qui exécute toujours MED-V au démarrage de Windows.

   **Important**  
   L’installation de l’espace de travail MED-V peut être exécutée de manière interactive par l’utilisateur final ou en silence via un système de distribution de logiciels électronique. L’installation de l’espace de travail MED-V nécessite des informations d’identification d’administration, de sorte que les utilisateurs finaux doivent être administrateurs de leur ordinateur pour installer l’espace de travail MED-V. Vous pouvez également faire en sorte qu’un système de distribution de logiciels électronique s’exécute généralement dans le contexte système et dispose d’autorisations suffisantes.



~~~
**Tip**  
Because of problems that can occur when you install MED-V from a network location, we recommend that you copy the MED-V workspace setup files locally and then run setup.exe.
~~~



### Configuration pour la première fois

Après l’installation de MED-V et de ses composants requis, MED-V doit être configuré. La configuration de MED-V est connue sous le nom de configuration pour la première fois. À l’aide de l’outil de création de **package de l’espace de travail MED-V**, vous pouvez configurer la première fois le programme d’installation pour qu’il s’exécute en silence ou interactif. Lorsque le programme d’installation de MED-V est requis pour la première fois, l’utilisateur final doit entrer son mot de passe pour s’authentifier dans l’espace de travail MED-V, mais peut également être presque invisible pour l’utilisateur. Les notifications s’affichent dans la zone de notification, par exemple lors de la première configuration et des applications prêtes. Les actions qui se produisent lors de la première installation de MED-V sont les suivantes:

1.  Le disque dur virtuel doit être configuré. La mini-installation s’exécute et développe l’image Windows XP. En règle générale, ce problème se produit dans une fenêtre masquée, mais MED-V peut être configuré pour s’afficher lors de cette configuration.

2.  Une fois la mini-installation terminée, vous pouvez exécuter des commandes dont vous avez besoin pour une configuration supplémentaire, par exemple l’installation de logiciels ou d’autres applications ESD ou la configuration de l’image. Celles-ci peuvent être appelées dans le fichier Sysprep. inf et ne sont pas nécessaires. Pour plus d’informations, reportez-vous à [la rubrique Configuration d’une image de PC virtuel Windows pour MED-V](configuring-a-windows-virtual-pc-image-for-med-v.md).

3.  Ftscompletion.exe s’exécute comme la dernière étape de la configuration. Ce processus termine la configuration de MED-V, ajoute l’utilisateur au groupe RDP pour lui permettre d’accéder à l’espace de travail MED-v, de copier les journaux, de configurer le protocole MED-V et de relancer l’espace de travail MED-v. Ce processus peut également ajouter l’utilisateur en tant qu’administrateur de l’espace de travail MED-V s’il a été configuré lors de la création de l’espace de travail MED-V. Ftscompletion.exe est généralement appelé par le biais du fichier Sysprep, inf, mais peut également être exécuté par le biais d’une autre méthode, comme un script. Toutefois, Ftscompletion.exe doit être la dernière action effectuée lorsque la station de travail est configurée. Pour plus d’informations, reportez-vous à [la rubrique Configuration d’une image de PC virtuel Windows pour MED-V](configuring-a-windows-virtual-pc-image-for-med-v.md).

4.  Après le redémarrage de l’espace de travail MED-V par Ftscompletion.exe, l’utilisateur final est connecté. S’il n’a pas enregistré son mot de passe lors de la première installation, il est invité à le faire. L’espace de travail MED-V est alors démarré et configuré pour l’utilisateur. La configuration implique l’application d’une stratégie de groupe.

    Nous vous recommandons d’appliquer uniquement ces stratégies qui sont utiles dans un environnement de compatibilité des applications pour Windows XP. Par exemple, les stratégies de personnalisation de bureau n’ont généralement pas besoin d’être appliquées et doivent être désactivées. Pour plus d’informations sur la façon de n’autoriser que les profils locaux, voir [paramètres de stratégie de groupe pour les profils utilisateur errants](https://go.microsoft.com/fwlink/?LinkId=205072) ( https://go.microsoft.com/fwlink/?LinkId=205072) .

Après la première configuration, l’utilisateur final est averti que les applications publiées sont prêtes. Ils peuvent ensuite accéder aux applications installées dans l’espace de travail MED-V à partir du menu **Démarrer** .

## Rubriques connexes


[Préparer l'environnement de déploiement de MED-V](prepare-the-deployment-environment-for-med-v.md)

[Déploiement de MED-V](deployment-of-med-v.md)









