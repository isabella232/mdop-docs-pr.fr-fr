---
title: Comment déployer un espace de travail MED-V dans une image Windows7
description: Comment déployer un espace de travail MED-V dans une image Windows7
author: dansimp
ms.assetid: a83aba4e-8681-4906-9872-f431c0bb15f9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 49dd796d6f6af425b9000b595a0d828c3cb0035a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812263"
---
# Comment déployer un espace de travail MED-V dans une image Windows7


Vous pouvez installer tous les composants MED-V dans une image Windows 7 que vous distribuez au sein de votre entreprise tout comme vous le feriez pour toute nouvelle installation de Windows 7. L’utilisateur final termine ensuite l’installation de l’espace de travail MED-V en cliquant sur le raccourci du menu **Démarrer** que vous avez configuré pour démarrer med-v. Le premier démarrage du programme d’installation et l’utilisateur final suivent les instructions pour terminer la configuration.

La section suivante fournit des informations et des instructions pour vous aider à déployer l’espace de travail MED-V au sein de votre entreprise à l’aide d’une image Windows 7.

**Pour déployer un espace de travail MED-V dans une image Windows 7**

1.  Créer une image standard de Windows 7. Pour plus d’informations, reportez-vous à [la rubrique Création d’une image standard de Windows 7: Guide détaillé](https://go.microsoft.com/fwlink/?LinkId=204843) ( https://go.microsoft.com/fwlink/?LinkId=204843) .

2.  Dans l’image Windows 7, installez le PC virtuel Windows et les mises à jour de PC virtuel Windows. Pour plus d’informations, voir [configurer les conditions préalables à l’installation](configure-installation-prerequisites.md).

3.  Installez l’agent hôte MED-V en utilisant le fichier d’installation MED-V \ _HostAgent \ _Setup. Pour plus d’informations, reportez-vous à la rubrique [installation manuelle de l’agent hôte MED-V](how-to-manually-install-the-med-v-host-agent.md).

    **Avertissement**  Internet Explorer doit être fermé avant l’installation de l’agent d’hébergement MED-V, sinon des conflits peuvent se produire plus tard avec la redirection d’URL. Vous pouvez également le faire en spécifiant un redémarrage de l’ordinateur lors d’une distribution.

     

4.  Copiez les fichiers du package d’espace de travail MED-V dans l’image Windows 7. Les fichiers de package d’espace de travail MED-V sont le programme d’installation de l’espace de travail MED-V, le fichier. medv et le fichier setup.exe que vous avez créé à l’aide du **Gestionnaire de package med-v**.

    **Important**  Le fichier. medv et setup.exe doit se trouver dans le même dossier que le programme d’installation de l’espace de travail MED-V. Installez ensuite l’espace de travail MED-V en exécutant setup.exe.

     

5.  Configurez un raccourci dans le menu **Démarrer** pour ouvrir l’installation du package d’espace de travail MED-V.

    Créez un raccourci du menu **Démarrer** dans le fichier setup.exe pour permettre à l’utilisateur final de démarrer une installation MED-V selon les besoins.

6.  En utilisant le processus de déploiement d’images standard de votre entreprise, vous pouvez distribuer l’image Windows 7 sur les ordinateurs de votre entreprise qui nécessitent MED-V.

Lorsque l’utilisateur final doit accéder à une application publiée dans l’espace de travail MED-V, il peut cliquer sur le raccourci du menu **Démarrer** pour installer l’espace de travail MED-v. Ce paramètre démarre automatiquement la première fois et termine la configuration de MED-V. Une fois l’installation terminée, l’utilisateur final peut accéder aux applications MED-V dans le menu **Démarrer** .

## Rubriques connexes


[Vue d'ensemble du déploiement de MED-V2.0](med-v-20-deployment-overview.md)

[Déploiement d'un espace de travail MED-V via un système de distribution électronique de logiciels](how-to-deploy-a-med-v-workspace-through-an-electronic-software-distribution-system.md)

 

 





