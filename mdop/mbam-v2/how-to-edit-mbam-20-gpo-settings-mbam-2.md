---
title: Procédure de modification des paramètres d'objet de stratégie de groupe MBAM2.0
description: Procédure de modification des paramètres d'objet de stratégie de groupe MBAM2.0
author: dansimp
ms.assetid: f5ffa93d-b4d2-4317-8a1c-7d2be0264fe3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: aaf7c7aab4baba66513edbfa2489fbe53c97dda8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810344"
---
# Procédure de modification des paramètres d'objet de stratégie de groupe MBAM2.0


Pour réussir le déploiement de Microsoft BitLocker administration et de la surveillance (MBAM), vous devez d’abord déterminer les stratégies de groupe que vous utiliserez dans votre implémentation de l’administration et de la surveillance de Microsoft BitLocker. Pour plus d’informations sur les différentes stratégies disponibles, voir [planification des exigences de la stratégie de groupe MBAM 2,0](planning-for-mbam-20-group-policy-requirements-mbam-2.md) . Après avoir déterminé les stratégies que vous allez utiliser, vous devez modifier un ou plusieurs objets de stratégie de groupe qui incluent les paramètres de stratégie pour MBAM.

Vous pouvez utiliser les étapes suivantes pour configurer les paramètres de l’objet de stratégie de groupe de base et recommandés pour permettre à MBAM de gérer le chiffrement BitLocker pour les ordinateurs clients de votre organisation.

**Pour modifier les paramètres de l’objet de stratégie de MBAM client**

1.  Sur un ordinateur sur lequel le modèle de stratégie de groupe MBAM est installé, assurez-vous que les services MBAM sont activés.

2.  À l’aide de la console de gestion des stratégies de groupe (GPMC. msc) ou du produit MDOP (Advanced Group Policy Management) sur un ordinateur sur lequel le modèle de stratégie de groupe MBAM est installé, sélectionnez **configuration**de l’ordinateur, cliquez sur **stratégies**, cliquez sur **modèles d’administration**, sélectionnez **composants Windows**, puis cliquez sur **MDOP MBAM (gestion BitLocker)**.

3.  Modifiez les paramètres d’objets de stratégie de groupe requis pour activer les services clients MBAM sur des ordinateurs clients. Pour chaque stratégie figurant dans le tableau suivant, sélectionnez **groupe de stratégies**, cliquez sur la **stratégie**, puis configurez le **paramètre**:

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Groupe de stratégies</th>
    <th align="left">Stratégie</th>
    <th align="left">Paramètre</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Gestion des clients</p></td>
    <td align="left"><p>Configurer les services de MBAM</p></td>
    <td align="left"><p>Activé. Définissez <strong> MBAM point de terminaison du service matériel et de récupération </strong> et <strong> sélectionnez les informations de récupération BitLocker à stocker </strong> . Définissez le <strong> point de terminaison </strong> du service de conformité MBAM et entrez la fréquence du rapport d’État (minutes).</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Lecteur du système d’exploitation</p></td>
    <td align="left"><p>Paramètres de chiffrement de lecteur du système d’exploitation</p></td>
    <td align="left"><p>Activé. Définissez <strong> Sélectionner un protecteur pour le lecteur du système d’exploitation </strong> . Requis pour enregistrer les données du lecteur du système d’exploitation sur le serveur de restauration MBAMKey.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Lecteur amovible</p></td>
    <td align="left"><p>Contrôler l’utilisation de BitLocker sur des lecteurs amovibles</p></td>
    <td align="left"><p>Activé. Obligatoire si MBAM enregistre les données du lecteur amovible sur le serveur de récupération de clés MBAM.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Lecteur fixe</p></td>
    <td align="left"><p>Contrôler l’utilisation de BitLocker sur des disques fixes</p></td>
    <td align="left"><p>Activé. Obligatoire si MBAM enregistre des données de disque fixe sur le serveur de récupération de clés MBAM.</p>
    <p>Définissez <strong> choisir la manière dont les lecteurs protégés par BitLocker peuvent être récupérés </strong> et <strong> autoriser l’agent de récupération de données </strong> .</p></td>
    </tr>
    </tbody>
    </table>



~~~
**Important**  
Depending on the policies that your organization decides to deploy, you may have to configure additional policies. See [Planning for MBAM 2.0 Group Policy Requirements](planning-for-mbam-20-group-policy-requirements-mbam-2.md) for Group Policy configuration details for all of the available MBAM GPO policy options.
~~~



## Rubriques connexes


[Déploiement d'objets de stratégie de groupe MBAM2.0](deploying-mbam-20-group-policy-objects-mbam-2.md)









