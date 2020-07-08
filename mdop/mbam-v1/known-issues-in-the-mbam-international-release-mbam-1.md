---
title: Problèmes connus dans MBAM International Release
description: Problèmes connus dans MBAM International Release
author: dansimp
ms.assetid: bbf888dc-93c1-4323-b43c-0ded098e9b93
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: af32551135ff297d25930f94b40bf04c0fcaaafe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811364"
---
# Problèmes connus dans MBAM International Release

Cette section contient des problèmes connus de la version internationale de Microsoft BitLocker (MBAM).

## Problèmes connus dans MBAM International Release

### Le processus d’installation ne spécifie pas de mise à jour

Lors de la mise à jour du serveur d’administration et de contrôle Microsoft BitLocker, le programme d’installation ne vérifie pas l’installation d’une mise à jour.

**Solution de contournement**: aucune.

### Certificats utilisés pour le rôle serveur d’administration et de surveillance

Si vous utilisez un certificat pour l’authentification entre MBAM Servers, après avoir mis à jour le serveur d’administration et de surveillance MBAM, vous devez vous assurer que le certificat est valide et qu’il n’est pas révoqué ou expiré.

**Solution de contournement**: aucune.

### MBAM svclog de remplissage de fichier

Si vous avez suivi les étapes de la [base de connaissances 2668170](https://go.microsoft.com/fwlink/?LinkID=247277), il se peut que vous deviez répéter les étapes Ko après l’installation de cette mise à jour.

**Solution de contournement**: aucune.

## Rubriques connexes

[Déploiement de MBAM1.0 Language Release Update](deploying-the-mbam-10-language-release-update.md)

 

 





