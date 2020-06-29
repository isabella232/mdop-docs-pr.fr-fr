---
title: Déploiement du client MBAM pour ordinateur de bureau ou ordinateurs portables
description: Déploiement du client MBAM pour ordinateur de bureau ou ordinateurs portables
author: dansimp
ms.assetid: 56744922-bfdd-48f6-ae01-645ff53b64a8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 49340ae970dafc9d263f5564e7981a402da40f19
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804656"
---
# Déploiement du client MBAM pour ordinateur de bureau ou ordinateurs portables


Le client Microsoft BitLocker Administration and Analysis (MBAM) permet aux administrateurs d’appliquer et de surveiller le chiffrement de lecteur BitLocker sur les ordinateurs de l’entreprise. Le client BitLocker peut être intégré à une organisation en déployant le client par le biais d’un système de distribution de logiciels électronique, tel que les services de domaine Active Directory ou MicrosoftSystemCenterConfigurationManager.

**Remarques**  Pour vérifier la configuration système requise pour le client d’administration et de surveillance de BitLocker, voir [Configurations prises en charge par MBAM 2,0](mbam-20-supported-configurations-mbam-2.md).

 

**Pour déployer le client MBAM sur un ordinateur portable ou de bureau**

1.  Recherchez les fichiers d’installation du client MBAM fournis avec le logiciel MBAM.

2.  Utilisez les services de domaine Active Directory ou un outil de déploiement de logiciels d’entreprise tel que MicrosoftSystemCenterConfigurationManager pour déployer le package Windows Installer sur les ordinateurs cibles.

3.  Pour exécuter le fichier d’installation du client MBAM, vous pouvez configurer les paramètres de distribution ou la stratégie de groupe. Après l’installation, le client MBAM applique les paramètres de stratégie de groupe qui sont reçus par un contrôleur de domaine pour commencer à effectuer le chiffrement et les fonctions de gestion de BitLocker. Pour plus d’informations sur les paramètres de stratégie de groupe de MBAM, reportez-vous [à la planification des exigences de stratégie de groupe MBAM 2,0](planning-for-mbam-20-group-policy-requirements-mbam-2.md).

    **Important**  Le client MBAM ne démarrera pas les actions de chiffrement BitLocker si une connexion de protocole de bureau à distance est active. Toutes les connexions de console distante doivent être fermées avant le début du chiffrement BitLocker.

     

## Rubriques connexes


[Déploiement du client MBAM2.0](deploying-the-mbam-20-client-mbam-2.md)

 

 





