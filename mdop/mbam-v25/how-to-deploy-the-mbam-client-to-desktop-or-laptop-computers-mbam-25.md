---
title: Déploiement du client MBAM pour ordinateur de bureau ou ordinateurs portables
description: Déploiement du client MBAM pour ordinateur de bureau ou ordinateurs portables
author: dansimp
ms.assetid: 3a7639e0-468e-4496-8be2-ed29b8e07c53
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6b67533a555da4dabec6654ed3f95f91ad8d37bf
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810578"
---
# Déploiement du client MBAM pour ordinateur de bureau ou ordinateurs portables


Cette rubrique explique comment déployer le client MBAM sur les ordinateurs des utilisateurs finaux. Vous pouvez déployer le client MBAM par le biais d’un système de distribution de logiciels électronique, tel que Active Directory Domain Services ou MicrosoftSystemCenterConfiguration Manager.

Pour déployer le client MBAM dans le cadre d’un déploiement Windows, voir [Comment activer BitLocker en utilisant MBAM dans le cadre d’un déploiement Windows](how-to-enable-bitlocker-by-using-mbam-as-part-of-a-windows-deploymentmbam-25.md).

Avant de démarrer le déploiement du client MBAM, passez [en revue les configurations MBAM 2,5 prises en charge](mbam-25-supported-configurations.md).

**Pour déployer le client MBAM sur un ordinateur portable ou de bureau**

1.  Recherchez les fichiers d’installation du client MBAM fournis avec le logiciel MBAM.

2.  Utilisez les services de domaine Active Directory ou un outil de déploiement de logiciels d’entreprise tel que MicrosoftSystemCenterConfiguration Manager pour déployer le package Windows Installer sur les ordinateurs cibles.

3.  Pour exécuter le fichier d’installation du client MBAM, vous pouvez configurer les paramètres de distribution ou les paramètres de stratégie de groupe.

    Après l’installation, le client MBAM applique les paramètres de stratégie de groupe qui sont reçus d’un contrôleur de domaine pour commencer le chiffrement et les fonctions de gestion du lecteur BitLocker.

    **Important**  Le client MBAM ne démarre pas les actions de chiffrement de lecteur BitLocker si une connexion de protocole de bureau à distance est active. Toutes les connexions de console distante doivent être fermées et un utilisateur doit être connecté à une session de console physique avant le début du chiffrement de lecteur BitLocker.

     


## Rubriques connexes
[Déploiement du client MBAM2.5](deploying-the-mbam-25-client.md)

[Planification du déploiement de clients MBAM2.5](planning-for-mbam-25-client-deployment.md)

 

## Vous avez une suggestion pour MBAM?
- Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring) 
- Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





