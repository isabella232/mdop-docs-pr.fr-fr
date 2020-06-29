---
title: Création ou modification des fichiers mof
description: Création ou modification des fichiers mof
author: dansimp
ms.assetid: 4d19d707-b90f-4057-a6e9-e4221a607190
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5f59e9133dd25ecf45d16a5cb704d6ea00923d9e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811087"
---
# Création ou modification des fichiers mof


Avant d’installer Microsoft BitLocker administration et la surveillance (MBAM) avec Configuration Manager, vous devez modifier le fichier Configuration. mof. Vous devez également modifier ou créer le fichier SMS \ _def. mof, en fonction de la version de Configuration Manager que vous utilisez.

## Modifier le fichier Configuration.mof


Pour permettre aux ordinateurs clients de signaler les détails de conformité BitLocker par le biais des rapports du gestionnaire de configuration MBAM, vous devez modifier le fichier Configuration. mof pour Microsoft System Center Configuration Manager 2007 et SystemCenter2012 ConfigurationManager.

[Modifier le fichier Configuration.mof](edit-the-configurationmof-file.md)

## <a href="" id="create-or-edit-the-sms-def-mof-file"></a>Créer ou modifier le fichier SMS \ _def. mof


Pour permettre aux ordinateurs clients de signaler les détails de conformité BitLocker dans les rapports du gestionnaire de configuration MBAM, vous devez créer ou modifier le fichier SMS \ _def. mof. Dans Configuration Manager 2007, le fichier existe déjà, vous devez donc modifier le fichier existant, mais pas le remplacer. Si vous utilisez SystemCenter2012 ConfigurationManager, vous devez créer le fichier.

[Créer ou modifier le fichier SMS \ _def. mof](create-or-edit-the-sms-defmof-file.md)

## Rubriques connexes


[Déploiement de MBAM avec Configuration Manager](deploying-mbam-with-configuration-manager-mbam2.md)

 

 





