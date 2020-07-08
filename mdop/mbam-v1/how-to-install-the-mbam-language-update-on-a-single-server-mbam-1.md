---
title: Installation de MBAM Language Update sur un serveur unique
description: Installation de MBAM Language Update sur un serveur unique
author: dansimp
ms.assetid: e6fe59a3-a3e1-455c-a059-1f23ee083cf6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 94814158335430aba433c180cdba83d0cf15b760
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810745"
---
# Installation de MBAM Language Update sur un serveur unique


L’administration et l’analyse de BitLocker Microsoft (MBAM) incluent quatre rôles de serveur qui peuvent être exécutés sur un ou plusieurs ordinateurs. Toutefois, seules deux fonctionnalités du serveur MBAM requièrent la mise à jour pour la prise en charge de l’installation de la version MBAM 1,0 et du modèle de stratégie MBAM. Pour mettre à jour les trois fonctionnalités MBAM requises devant être installées sur un ordinateur, suivez la procédure décrite dans cette rubrique.

**Pour installer la mise à jour de langue MBAM sur un serveur unique**

1.  Ouvrez la console de gestion d’Internet Information Services (IIS), accédez à **sites**, puis arrêtez le site Web d’administration et de contrôle Microsoft BitLocker.

2.  Modifiez les liaisons pour le site Web MBAM, puis modifiez temporairement les liaisons du site. Par exemple, changez le port de 443 vers 9443.

3.  Recherchez et exécutez l’Assistant Configuration de MBAM (MBAMsetup.exe), puis sélectionnez les trois fonctionnalités suivantes:

    1.  Rapports de conformité et d’audit

    2.  Serveur d’administration et de surveillance

    3.  Modèles de stratégie de groupe

    **Important**  Les fonctionnalités du serveur MBAM doivent être mises à jour dans l’ordre suivant: les rapports de conformité et d’audit d’abord, puis sur le serveur d’administration et de surveillance. Les modèles de stratégie de groupe peuvent être mis à jour à tout moment sans vous soucier de la séquence.

     

4.  Après avoir effectué la mise à niveau de la base de données du serveur, ouvrez la console de gestion IIS et passez en revue les liaisons du site Web d’administration et de contrôle Microsoft BitLocker.

5.  Supprimez l’une des liaisons et assurez-vous que la liaison restante dispose du nom d’hôte, du certificat et du numéro de port appropriés pour la configuration d’entreprise MBAM.

6.  Redémarrez le site Web MBAM.

7.  Testez la fonctionnalité de site Web MBAM:

    -   Ouvrez l’interface Web MBAM et assurez-vous que vous pouvez récupérer une clé de récupération pour un client.

    -   Mettre en place un chiffrement d’un ordinateur client nouveau ou déchiffré manuellement.

        **Remarques**  Le client MBAM s’ouvre uniquement s’il peut communiquer avec la base de données de récupération et de matériel.

         

## Rubriques connexes


[Déploiement de MBAM1.0 Language Release Update](deploying-the-mbam-10-language-release-update.md)

 

 





