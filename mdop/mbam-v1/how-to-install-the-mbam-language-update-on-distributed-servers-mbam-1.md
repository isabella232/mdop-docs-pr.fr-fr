---
title: Installation de MBAM Language Update sur des serveurs distribués
description: Installation de MBAM Language Update sur des serveurs distribués
author: dansimp
ms.assetid: 5ddc64c6-0417-4a04-843e-b5e18d9f1a52
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6758463c6fc038c4d6ea86c0d49804f29bb543d3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811310"
---
# Installation de MBAM Language Update sur des serveurs distribués


L’administration et l’analyse de BitLocker Microsoft (MBAM) incluent quatre rôles de serveur qui peuvent être exécutés sur un ou plusieurs ordinateurs. Toutefois, seules deux fonctionnalités du serveur MBAM requièrent la mise à jour pour la prise en charge de l’installation de la version de MBAM 1,0 Language et du modèle de stratégie MBAM. Dans les configurations avec les fonctionnalités de MBAM Server installées sur plusieurs ordinateurs, seules les fonctionnalités serveur suivantes doivent être mises à jour:

-   Rapports de conformité et d’audit de MBAM

-   Serveur d’administration et de surveillance MBAM

**Important**  Les fonctionnalités du serveur MBAM doivent être mises à jour dans cet ordre: les rapports de conformité et d’audit d’abord, puis le serveur d’administration et de surveillance. Les modèles de stratégie de groupe MBAM peuvent être mis à jour à tout moment sans vous soucier de la séquence.

 

**Pour installer la mise à jour de langue MBAM sur la fonctionnalité serveur de rapport d’audit et de conformité MBAM**

1.  Sur l’ordinateur exécutant la fonctionnalité de compatibilité et d’audit de MBAM, recherchez et exécutez l’Assistant Configuration de la mise à jour de MBAM (MBAMsetup.exe).

2.  Terminez l’Assistant pour les rapports de conformité et d’audit, puis fermez l’Assistant.

**Pour installer la mise à jour de la langue MBAM sur la fonctionnalité serveur d’administration et de surveillance MBAM**

1.  Sur l’ordinateur qui exécute la fonctionnalité d’administration et de surveillance de MBAM, ouvrez la console de gestion des services Internet (IIS), accédez à **sites**, puis arrêtez le site Web d’administration et de contrôle Microsoft BitLocker.

2.  Choisissez de modifier les liaisons pour le site Web MBAM, puis modifiez les liaisons du site. Par exemple, changez le port de 443 vers 9443.

3.  Recherchez et exécutez l’Assistant Configuration de la mise à jour des langues de MBAM (MBAMsetup.exe). Suivez la procédure de l’Assistant pour la fonctionnalité d’administration et de surveillance du serveur, puis fermez l’Assistant.

4.  Après avoir effectué la mise à niveau de la base de données du serveur, ouvrez la console de gestion IIS et passez en revue les liaisons du site Web d’administration et de contrôle Microsoft BitLocker.

5.  Supprimez l’ancienne liaison et assurez-vous que la liaison restante dispose du nom d’hôte, du certificat et du numéro de port appropriés pour la configuration d’entreprise MBAM.

6.  Redémarrez le site Web MBAM.

7.  Testez la fonctionnalité du site Web MBAM:

    -   Ouvrez l’interface Web MBAM et assurez-vous que vous pouvez obtenir une clé de récupération pour un client.

    -   Mettre en place un chiffrement d’un ordinateur client nouveau ou déchiffré manuellement.

        **Remarques**  Le client MBAM s’ouvre uniquement s’il peut communiquer avec la base de données de récupération et de matériel.

         

## Rubriques connexes


[Déploiement de MBAM1.0 Language Release Update](deploying-the-mbam-10-language-release-update.md)

 

 





