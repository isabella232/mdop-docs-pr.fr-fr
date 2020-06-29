---
title: Déploiement de MBAM avec Configuration Manager
description: Déploiement de MBAM avec Configuration Manager
author: dansimp
ms.assetid: 89d03e29-457a-471d-b893-e0b74a83ec50
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c6cffc1cf51a26aeaa94fcb265199c19f0f34abe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809965"
---
# Déploiement de MBAM avec Configuration Manager


Les procédures suivantes décrivent le déploiement de l’administration et de la surveillance de l’utilisation de BitLocker (MBAM) Microsoft System Center Configuration Manager 2007 ou MicrosoftSystemCenter2012 (en anglais) par utilisantle configuration recommandée, décrite dans la rubrique [mise en route de MBAM avec Configuration Manager](getting-started---using-mbam-with-configuration-manager.md). La configuration recommandée consiste à installer les fonctionnalités d’administration et de surveillance sur un ou plusieurs serveurs d’administration et de surveillance Microsoft BitLocker, et à installer Microsoft System Center Configuration Manager 2007 ou MicrosoftSystemCenter2012 sur un serveur distinct.

Avant de commencer l’installation, assurez-vous que vous remplissez les conditions préalables et la configuration matérielle et logicielle requise pour l’installation d’MBAM avec Configuration Manager en passant en revue la [planification du déploiement d’MBAM avec Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md).

Si vous devez réinstaller MBAM avec la topologie Configuration Manager, vous devez d’abord supprimer certains objets de Configuration Manager. Pour plus d’informations, consultez l’article de la [base de connaissances](https://go.microsoft.com/fwlink/?LinkId=286306) .

Les étapes permettant d’installer MBAM avec Configuration Manager sont regroupées dans les catégories suivantes. Suivez les étapes de chaque catégorie pour terminer l’installation.

## Création ou modification des fichiers mof


Pour permettre aux ordinateurs clients de signaler les détails de conformité BitLocker par le biais des rapports du gestionnaire de configuration MBAM, vous devez modifier le fichier **Configuration. mof** , puis modifier ou créer le fichier Sms \ _def. mof, en fonction de la version de Configuration Manager que vous utilisez.

[Création ou modification des fichiers mof](how-to-create-or-edit-the-mof-files.md)

## Installation de MBAM avec Configuration Manager


Cette section présente les étapes à suivre pour installer les éléments suivants: MBAM sur le serveur Configuration Manager; les bases de données de récupération et d’audit sur le serveur de base de données; ainsi que les fonctionnalités d’administration et de surveillance du serveur sur le serveur d’administration et de surveillance.

[Installation de MBAM avec Configuration Manager](how-to-install-mbam-with-configuration-manager.md)

## Valider l’installation de la fonctionnalité MBAM Server sur le serveur Configuration Manager


Lorsque l’installation de l’administration et du suivi de BitLocker est terminée, vérifiez que l’installation a correctement configuré toutes les fonctionnalités MBAM nécessaires pour le serveur Configuration Manager.

[Validation de l'installation de MBAM avec Configuration Manager](how-to-validate-the-mbam-installation-with-configuration-manager.md)

## Rubriques connexes


[Utilisation de MBAM avec Configuration Manager](using-mbam-with-configuration-manager.md)

 

 





