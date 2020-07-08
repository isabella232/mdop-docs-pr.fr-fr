---
title: Déploiement du client MBAM pour ordinateur de bureau ou ordinateurs portables
description: Déploiement du client MBAM pour ordinateur de bureau ou ordinateurs portables
author: dansimp
ms.assetid: f32927a2-4c05-4da8-acca-1108d1dfdb7e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ce4f8597cc182c037983a89efd60c5ef935712ce
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811219"
---
# Déploiement du client MBAM pour ordinateur de bureau ou ordinateurs portables


Le client Microsoft BitLocker Administration and Analysis (MBAM) permet aux administrateurs d’appliquer et de surveiller le chiffrement de lecteur BitLocker sur les ordinateurs de l’entreprise. Le client MBAM peut être intégré à une organisation en déployant le client par le biais d’outils, tels que les services de domaine Active Directory (AD FS) ou un outil de déploiement de logiciels d’entreprise tel que MicrosoftSystemCenter2012 ConfigurationManager.

**Remarques**  Pour vérifier la configuration système requise pour le client MBAM, voir [Configurations prises en charge par MBAM 1,0](mbam-10-supported-configurations.md).

 

**Pour déployer le client MBAM sur un ordinateur portable ou de bureau**

1.  Recherchez les fichiers d’installation du client MBAM fournis avec le logiciel MBAM.

2.  Déployez le package Windows Installer sur les ordinateurs cibles à l’aide des services de domaine Active Directory ou d’un outil déploiement de logiciels d’entreprise, tels que les ConfigurationManagers MicrosoftSystemCenter2012.

    **Remarques**  Vous ne devez pas utiliser de stratégie de groupe pour déployer le package Windows Installer.

     

3.  Pour exécuter le fichier d’installation du client MBAM, vous pouvez configurer les paramètres de distribution ou la stratégie de groupe. Après l’installation, le client MBAM applique les paramètres de stratégie de groupe qui sont reçus par un contrôleur de domaine pour commencer à effectuer le chiffrement et les fonctions de gestion de BitLocker. Pour plus d’informations sur les paramètres de stratégie de groupe de MBAM, reportez-vous [à la planification des exigences de stratégie de groupe MBAM 1,0](planning-for-mbam-10-group-policy-requirements.md).

    **Important**  Le client MBAM ne démarrera pas les actions de chiffrement BitLocker si une connexion de protocole de bureau à distance est active. Toutes les connexions de console distante doivent être fermées avant le début du chiffrement BitLocker.

     

## Rubriques connexes


[Déploiement du client MBAM1.0](deploying-the-mbam-10-client.md)

 

 





