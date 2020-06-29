---
title: Architecture de haut niveau
description: Architecture de haut niveau
author: dansimp
ms.assetid: a78e12ad-5aa6-40e0-ae8b-51acaf005712
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 00df29c751653645ab4bee9762af57576a40092a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811615"
---
# Architecture de haut niveau


La solution MED-V comprend les éléments suivants:

-   **Machine virtuelle définie par l’administrateur**, qui encapsule un environnement de bureau complet, y compris un système d’exploitation, des applications, ainsi que des outils de gestion et de sécurité facultatifs.

-   **Référentiel d’images**: stocke toutes les images virtuelles sur un serveur IIS standard et permet la gestion des versions d’images virtuelles, la récupération d’image authentifiée par le client et le téléchargement efficace (d’une nouvelle image ou mise à jour) via la technologie de transfert de découpage.

-   **Serveur de gestion**: associe les images virtuelles du référentiel d’images et les stratégies d’utilisation de l’administrateur à Active Directory® utilisateurs ou groupes. Le serveur de gestion agrège également les événements des clients et les stocke dans une base de données externe (Microsoft SQL Server®) à des fins de surveillance et de création de rapports.

-   **Console de gestion**: permet aux administrateurs de contrôler le serveur de gestion et le référentiel d’images.

-   **Client de l’utilisateur final**

    1.  Cycle de vie d’image virtuelle: authentification, récupération d’image, application de stratégies d’utilisation.

    2.  Gestion de session de machine virtuelle: démarrez, arrêtez et verrouillez l’ordinateur virtuel.

    3.  Expérience de bureau unique: les applications installées sur l’ordinateur virtuel sont accessibles en toute transparence par le biais du menu de démarrage standard du bureau et intégrées à d’autres applications sur le Bureau de l’utilisateur.

Toutes les communications entre le client et les serveurs (serveur de gestion et référentiel d’images) sont effectuées en haut d’un canal HTTP ou HTTPs standard.

![](images/506f54d0-38fa-446a-8070-17ae26da5355.gif)

 

 





