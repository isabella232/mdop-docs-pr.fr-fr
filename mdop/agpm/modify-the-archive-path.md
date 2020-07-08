---
title: Modifier le chemin d'accès de l'archive
description: Modifier le chemin d'accès de l'archive
author: dansimp
ms.assetid: 6d90daf9-58db-4166-b5b3-e84bb261164a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1fc6ba2bf415d3d1bc67144d0dec1030c6173026
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808329"
---
# Modifier le chemin d'accès de l'archive


Le chemin d’accès d’archive est l’emplacement de l’archivage relatif au serveur AGPM. Le chemin d’accès d’archive peut pointer vers un dossier sur le serveur AGPM ou sur un autre serveur dans la même forêt.

Le chemin d’accès d’archive et le compte de service AGPM sont configurés lors de l’installation d’AGPM Server et peuvent être modifiés par la suite via **Ajouter ou supprimer des programmes** sur le serveur AGPM.

Un compte d’utilisateur membre du groupe administrateurs de domaine et ayant accès au serveur AGPM (l’ordinateur sur lequel est installé le serveur de gestion de la stratégie de groupe Microsoft Advanced) est requis pour effectuer cette procédure.

**Pour modifier le chemin d’accès de l’archive**

1.  Sur l’ordinateur sur lequel est installé Microsoft Advanced Group Policy Management-serveur, cliquez sur **Démarrer**, puis sur **panneau de configuration**, cliquez sur **Ajouter ou supprimer des programmes**.

2.  Cliquez sur **gestion de la stratégie de groupe Microsoft avancée-serveur**, puis cliquez sur **modifier**.

3.  Cliquez sur **suivant**, puis sur **modifier**.

4.  Suivez les instructions à l’écran pour configurer les paramètres du service AGPM:

    1.  Pour le chemin d’accès de l’archive, entrez le nouvel emplacement de l’archivage relatif au serveur AGPM. Le chemin d’accès d’archive peut pointer vers un dossier sur le serveur AGPM ou un autre emplacement, mais l’espace disponible doit être suffisant pour stocker tous les objets de stratégie de groupe et les données d’historique gérés par ce serveur AGPM.

    2.  Entrez les informations d’identification du compte de service AGPM.

        **Important**  La modification de l’installation efface les informations d’identification du compte de service AGPM. Vous devez entrer de nouveau les informations d’identification, mais elles ne sont pas obligées de correspondre aux informations d’identification utilisées lors de l’installation d’origine.

        Le compte de service AGPM doit disposer d’un accès complet aux objets GPO qu’il doit gérer. S’il s’agit de gérer les objets de stratégie de groupe sur un domaine unique, vous pouvez créer le compte système local pour le contrôleur de domaine principal du compte de service AGPM.

        S’il s’agit de gérer des objets de stratégie de groupe sur plusieurs domaines ou si un serveur membre sera le serveur AGPM, vous devez configurer un autre compte en tant que compte de service AGPM, car le compte système local d’un contrôleur de domaine ne peut pas accéder aux objets de stratégie de groupe sur d’autres domaines.

         

    3.  Pour le propriétaire de l’archive, entrez les informations d’identification d’un administrateur AGPM (contrôle total).

5.  Cliquez sur **modifier**, et une fois l’installation terminée, cliquez sur **Terminer**.

### Références supplémentaires

-   [Gestion du service AGPM](managing-the-agpm-service.md)

 

 





