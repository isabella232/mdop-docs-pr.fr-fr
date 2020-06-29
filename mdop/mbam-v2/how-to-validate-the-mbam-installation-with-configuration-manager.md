---
title: Validation de l'installation de MBAM avec Configuration Manager
description: Validation de l'installation de MBAM avec Configuration Manager
author: dansimp
ms.assetid: 8e268539-91c3-4e8a-baae-faf3605da818
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 500c6f6ee5138b5677bf1fa20e2627a56981df1f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809474"
---
# Validation de l'installation de MBAM avec Configuration Manager


Après l’installation de Microsoft BitLocker administration et de la surveillance (MBAM) avec Configuration Manager, vérifiez que l’installation a correctement configuré toutes les fonctionnalités nécessaires pour MBAM en effectuant les étapes suivantes.

**Pour valider l’installation de la fonctionnalité MBAM Server avec Configuration Manager**

1.  Sur le serveur sur lequel System Center Configuration Manager est déployé, ouvrez le **panneau**de configuration. Sélectionnez le programme utilisé pour désinstaller ou modifier un programme. Vérifiez que le **contrôle et l’administration de BitLocker Microsoft** s’affichent dans la liste des programmes et fonctionnalités.

    **Remarques**  Pour valider l’installation, vous devez utiliser un compte de domaine disposant d’informations d’identification d’administrateur local sur chaque serveur.

     

2.  Utilisez la console Configuration Manager pour vérifier qu’une nouvelle collection, appelée «MBAM d’ordinateurs pris en charge», s’affiche.

    Pour afficher la collection avec Configuration Manager 2007: cliquez sur **base de données de site** ( &lt; **SiteCode** &gt;  -  &lt; **serveur** &gt; , &lt; **SiteName** &gt; ), gestion de l' **ordinateur**.

    Pour afficher la collection avec SystemCenter2012 ConfigurationManager: cliquez sur l’espace de travail **ressources et conformité** , **collections de périphériques**.

3.  Utilisez la console Configuration Manager pour vérifier que les rapports suivants apparaissent dans le dossier **MBAM** :

    -   Compatibilité de l’ordinateur BitLocker

    -   Tableau de bord de conformité de BitLocker Enterprise

    -   Détails de la conformité à l’entreprise BitLocker

    -   Résumé de conformité de BitLocker Enterprise

    Pour afficher les rapports avec Configuration Manager 2007: cliquez sur **création**de rapports, **Reporting Services**, \ \ \ \ &lt; **NomServeur** &gt; , **dossiers de rapports** .

    Pour afficher les rapports avec SystemCenter2012 ConfigurationManager: cliquez sur l’espace de travail de **surveillance** , **création**de rapports, **rapports**.

4.  Utilisez la console Configuration Manager pour vérifier que la configuration de base de la sécurité de BitLocker figure dans la liste.

    Pour afficher les planifications de configuration à l’aide de Configuration Manager 2007: cliquez sur gestion de la **configuration souhaitée**, **planning de référence de configuration**.

    Pour afficher les lignes de base de configuration avec SystemCenter2012 ConfigurationManager: cliquez sur l’espace de travail **ressources et conformité** , **paramètres de conformité**, **planning de référence de configuration**.

5.  Utilisez la console Configuration Manager pour vérifier que les nouveaux éléments de configuration suivants sont affichés:

    -   Protection des lecteurs de données fixes BitLocker

    -   Protection des lecteurs du système d’exploitation BitLocker

    Pour afficher les éléments de configuration avec Configuration Manager 2007: cliquez sur gestion de la configuration, **éléments de configuration** **souhaités**.

    Pour afficher les éléments de configuration avec SystemCenter2012 ConfigurationManager: cliquez sur l’espace de travail **ressources et conformité** , **paramètres de conformité**et **éléments de configuration**.

## Rubriques connexes


[Déploiement de MBAM avec Configuration Manager](deploying-mbam-with-configuration-manager-mbam2.md)

 

 





