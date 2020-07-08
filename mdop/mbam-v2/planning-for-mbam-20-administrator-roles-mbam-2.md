---
title: Planification des rôles administrateur de MBAM2.0
description: Planification des rôles administrateur de MBAM2.0
author: dansimp
ms.assetid: 6f813297-6479-42d3-a21b-896d54466b5b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a89a04c0ef074407dc3cd081d351d44023e65e70
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810829"
---
# Planification des rôles administrateur de MBAM2.0


Cette rubrique répertorie et décrit les rôles d’administrateur disponibles dans le cadre de l’administration et de la surveillance de BitLocker (MBAM), ainsi que les emplacements serveur où sont créés les groupes locaux.

## Rôles d’administrateur MBAM


<a href="" id="---------------mbam-system-administrators"></a> **Administrateurs système MBAM**  
Les administrateurs de ce rôle ont accès à toutes les fonctionnalités d’administration et de contrôle de Microsoft BitLocker. Le groupe local de ce rôle est installé sur le serveur d’administration et de surveillance.

<a href="" id="---------------mbam-helpdesk-users"></a> **Utilisateurs du support technique MBAM**  
Les administrateurs de ce rôle ont accès aux fonctionnalités du support technique de MBAM. Le groupe local de ce rôle est installé sur le serveur d’administration et de surveillance.

<a href="" id="---------------mbam-report-users"></a> **Utilisateurs de rapports MBAM**  
Les administrateurs de ce rôle ont accès aux rapports de conformité et d’audit de MBAM. Le groupe local de ce rôle est installé sur le serveur d’administration et de surveillance, la base de données d’audit et de conformité, ainsi que sur le serveur qui héberge les rapports de conformité et d’audit.

<a href="" id="---------------mbam-advanced-helpdesk-users"></a> **Utilisateurs du support technique avancée MBAM**  
Les administrateurs de ce rôle ont accès aux fonctionnalités du support technique de MBAM. Le groupe local de ce rôle est installé sur le serveur d’administration et de surveillance. Si un utilisateur est membre des utilisateurs du support technique MBAM et des utilisateurs du support technique avancé MBAM, les autorisations de l’utilisateur du support technique avancé MBAM remplacent les autorisations des utilisateurs du support technique MBAM.

**Important**  Pour afficher les rapports, un utilisateur administratif doit être membre du groupe de sécurité des **utilisateurs du rapport MBAM** sur la fonctionnalité d’administration et de surveillance du serveur, de la conformité et de la base de données d’audit, et sur le serveur qui héberge la fonctionnalité de rapport d’audit et de conformité. Il est recommandé de créer un groupe de sécurité dans les services de domaine Active Directory (AD FS) avec des droits sur le groupe de sécurité des **utilisateurs de rapports MBAM** locaux sur le serveur d’administration et de surveillance et sur le serveur qui héberge les rapports de conformité et d’audit.

 

## Rubriques connexes


[Préparation de votre environnement pour MBAM2.0](preparing-your-environment-for-mbam-20-mbam-2.md)

 

 





