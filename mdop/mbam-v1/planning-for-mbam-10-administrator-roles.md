---
title: Planification des rôles administrateur de MBAM1.0
description: Planification des rôles administrateur de MBAM1.0
author: dansimp
ms.assetid: 95be0eb4-25e9-43ca-a8e7-27373d35544d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 104d650824330ea990881c520a7811511f496dd1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811424"
---
# Planification des rôles administrateur de MBAM1.0


Cette rubrique inclut et décrit les rôles d’administrateur disponibles dans le cadre de la gestion et de l’analyse de BitLocker (MBAM), ainsi que les emplacements serveur où les groupes locaux sont créés.

## Rôles d’administrateur MBAM


<a href="" id="---------------mbam-system-administrators"></a> **Administrateurs système MBAM**  
Les administrateurs de ce rôle ont accès à toutes les fonctionnalités de MBAM. Le groupe local de ce rôle est installé sur le serveur d’administration et de surveillance.

<a href="" id="---------------mbam-hardware-users"></a> **Utilisateurs de matériel MBAM**  
Les administrateurs de ce rôle ont accès aux fonctionnalités de fonctionnalités matérielles de MBAM. Le groupe local de ce rôle est installé sur le serveur d’administration et de surveillance.

<a href="" id="---------------mbam-helpdesk-users"></a> **Utilisateurs du support technique MBAM**  
Les administrateurs de ce rôle ont accès aux fonctionnalités de support technique de MBAM. Le groupe local de ce rôle est installé sur le serveur d’administration et de surveillance.

<a href="" id="---------------mbam--report-users"></a> **Utilisateurs de rapports MBAM**  
Les administrateurs de ce rôle ont accès à la fonction rapports de conformité et d’audit à partir de MBAM. Le groupe local de ce rôle est installé sur le serveur d’administration et de surveillance, la base de données d’audit et de conformité, ainsi que sur le serveur qui héberge les rapports de conformité et d’audit.

<a href="" id="---------------mbam--advanced-helpdesk-users"></a> **Utilisateurs du support technique avancée MBAM**  
Les administrateurs de ce rôle ont accès aux fonctionnalités de support technique de MBAM. Le groupe local de ce rôle est installé sur le serveur d’administration et de surveillance. Si un utilisateur est membre des utilisateurs du support technique MBAM et des utilisateurs du support technique avancé MBAM, les autorisations de l’utilisateur du support technique MBAM MBAM seront remplacées par les autorisations des utilisateurs du support technique.

**Important**  Pour afficher les rapports, un utilisateur administratif doit être membre du groupe de sécurité des **utilisateurs du rapport MBAM** sur le serveur d’administration et de surveillance, de la base de données d’audit et de conformité, ainsi que du serveur hébergeant la fonctionnalité de conformité et de rapports. Il est recommandé de créer un groupe de sécurité dans Active Directory grâce aux droits du groupe de sécurité des **utilisateurs du rapport MBAM** local à la fois sur le serveur d’administration et de surveillance et sur le serveur qui héberge la conformité et les rapports.

 

## Rubriques connexes


[Préparation de votre environnement pour MBAM1.0](preparing-your-environment-for-mbam-10.md)

 

 





