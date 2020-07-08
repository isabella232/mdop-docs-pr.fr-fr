---
title: Gérer des exemptions d'ordinateurs au chiffrement BitLocker
description: Gérer des exemptions d'ordinateurs au chiffrement BitLocker
author: dansimp
ms.assetid: d4400a0d-b36b-4cf5-a294-1f53ec47f9ee
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 51b93061468508900eaee7fce8a7827e2db61d19
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811298"
---
# Gérer des exemptions d'ordinateurs au chiffrement BitLocker


L’utilisation de Microsoft BitLocker administration et de la surveillance (MBAM) permet d’exempter certains ordinateurs de la protection BitLocker. Par exemple, une organisation risque de contrôler l’exemption de BitLocker en fonction de votre ordinateur.

Pour exempter un ordinateur d’un chiffrement BitLocker, vous devez ajouter l’ordinateur à un groupe de sécurité dans ActiveDirectoryDomainServices pour ignorer toutes les règles de protection BitLocker basées sur un ordinateur.

**Remarques**  Si l’ordinateur est déjà protégé par BitLocker, la stratégie d’exemption d’ordinateur n’a aucun effet.

 

**Pour exempter un ordinateur d’un chiffrement BitLocker**

1.  Ajoutez le compte d’ordinateur que vous souhaitez exempter d’un groupe de sécurité dans ActiveDirectoryDomainServices. Cela vous permet d’ignorer toutes les règles de protection BitLocker basées sur un ordinateur.

2.  Créez un objet de stratégie de groupe à l’aide du modèle de stratégie de groupe MBAM, puis associez l’objet de stratégie de groupe au groupe Active Directory que vous avez créé à l’étape précédente. Pour plus d’informations sur la création des objets de stratégie de groupe nécessaires, voir [déploiement d’objets de stratégie de groupe MBAM 1,0](deploying-mbam-10-group-policy-objects.md).

3.  Lors du démarrage d’un ordinateur exempté, le client MBAM vérifie le paramètre de stratégie d’exemption de l’ordinateur et suspend la protection en fonction de la présence de l’ordinateur dans le groupe de sécurité d’exemption BitLocker.

## Rubriques connexes


[Administration des composants de MBAM1.0](administering-mbam-10-features.md)

 

 





