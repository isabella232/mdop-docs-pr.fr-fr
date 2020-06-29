---
title: Procédure de modification des paramètres d'objet de stratégie de groupe MBAM1.0
description: Procédure de modification des paramètres d'objet de stratégie de groupe MBAM1.0
author: dansimp
ms.assetid: 03d12fbc-4302-43fc-9b38-440607d778a1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 824fbc2fe0d8f2b00c32de177733e4e327cf4d44
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810463"
---
# Procédure de modification des paramètres d'objet de stratégie de groupe MBAM1.0


Pour réussir le déploiement de Microsoft BitLocker administration et de la surveillance (MBAM), vous devez d’abord déterminer les stratégies de groupe que vous utiliserez dans votre implémentation de l’administration et de la surveillance de Microsoft BitLocker. Pour plus d’informations sur les différentes stratégies disponibles, voir [planification des exigences de la stratégie de groupe MBAM 1,0](planning-for-mbam-10-group-policy-requirements.md). Après avoir déterminé les stratégies que vous allez utiliser, vous devez modifier un ou plusieurs objets de stratégie de groupe (GPO) incluant les paramètres de stratégie MBAM.

Les étapes suivantes expliquent comment configurer les paramètres de base d’un objet de stratégie de groupe (GPO) pour permettre à MBAM de gérer le chiffrement BitLocker pour les ordinateurs clients de votre organisation.

**Pour modifier les paramètres de l’objet de stratégie de MBAM client**

1.  Sur un ordinateur sur lequel le modèle de stratégie de groupe MBAM est installé, assurez-vous que les services MBAM sont activés.

2.  Utilisez la console de gestion des stratégies de groupe (GPMC. msc) ou le produit MDOP (Advanced Group Policy Management) pour les actions suivantes: sélectionnez **configuration**de l’ordinateur, sélectionnez **stratégies**, cliquez sur **modèles d’administration**, sélectionnez **composants Windows**, puis cliquez sur **MDOP MBAM (gestion BitLocker)**.

3.  Modifiez les paramètres d’objets de stratégie de groupe requis pour activer les services clients MBAM sur des ordinateurs clients. Pour chaque stratégie figurant dans le tableau suivant, sélectionnez **groupe de stratégies**, cliquez sur la **stratégie**, puis configurez le **paramètre**.

    Groupe de stratégies

    Stratégie

    Paramètre

    Gestion des clients

    Configurer les services de MBAM

    Activé. Définissez **MBAM point de terminaison du service matériel** et de récupération et **sélectionnez les informations de récupération BitLocker à stocker**.

    Définissez le **point de terminaison du service de conformité MBAM** et entrez la **fréquence du rapport d’État (minutes)**.

    Autoriser la vérification de compatibilité matérielle

    Désactivé. Cette stratégie est activée par défaut, mais n’est pas nécessaire pour une implémentation de base MBAM.

    Lecteur du système d’exploitation

    Paramètres de chiffrement de lecteur du système d’exploitation

    Activé. Définissez **Sélectionner un protecteur pour le lecteur du système d’exploitation**. Cela est requis pour enregistrer les données du lecteur du système d’exploitation sur le serveur de récupération de clé MBAM.

    Lecteur amovible

    Contrôler l’utilisation de BitLocker sur des lecteurs amovibles

    Activé. Cela est requis Si MBAM enregistre les données du lecteur amovible sur le serveur de récupération de clés MBAM.

    Lecteur fixe

    Contrôler l’utilisation de BitLocker sur des disques fixes

    Activé. Cela est requis Si MBAM enregistre des données de disque fixe sur le serveur de récupération de clés MBAM.

    Définissez **choisir la manière dont les lecteurs protégés par BitLocker peuvent être récupérés** et **autoriser l’agent de récupération de données**.



~~~
**Important**  
Depending on the policies that your organization decides to deploy, you may have to configure additional policies. See [Planning for MBAM 1.0 Group Policy Requirements](planning-for-mbam-10-group-policy-requirements.md) for Group Policy configuration details for all of the available MBAM GPO policy options.
~~~



## Rubriques connexes


[Déploiement d'objets de stratégie de groupe MBAM1.0](deploying-mbam-10-group-policy-objects.md)









