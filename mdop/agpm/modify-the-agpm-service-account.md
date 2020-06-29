---
title: Modifier le compte du service AGPM
description: Modifier le compte du service AGPM
author: dansimp
ms.assetid: 0d8d8c7b-f299-4fee-8414-406492156942
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0672ceed2fba17060e17d2ffcfa264da458b9897
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808341"
---
# Modifier le compte du service AGPM


Le service AGPM est un service Windows agissant en tant que proxy de sécurité, gérant l’accès client aux objets de stratégie de groupe (GPO) dans l’environnement d’archivage et de production. Si ce service est arrêté ou désactivé, les clients AGPM ne peuvent pas effectuer d’opérations via le serveur.

Le chemin d’accès d’archive et le compte de service AGPM sont configurés lors de l’installation d’AGPM Server et peuvent être modifiés par la suite via **Ajouter ou supprimer des programmes** sur le serveur AGPM.

**Attention**  Ne modifiez pas les paramètres du service AGPM via les outils et **services** **d’administration** du système d’exploitation. Cela peut empêcher le démarrage du service AGPM.

 

Un compte d’utilisateur membre du groupe administrateurs de domaine et ayant accès au serveur AGPM (l’ordinateur sur lequel est installé le serveur de gestion de la stratégie de groupe Microsoft Advanced) est requis pour effectuer cette procédure.

**Important**  Le compte de service AGPM doit disposer d’un accès complet aux objets de stratégie de groupe qu’il doit gérer et bénéficier d’une autorisation **de connexion en tant que service** . S’il s’agit de gérer les objets de stratégie de groupe sur un domaine unique, vous pouvez créer le compte système local pour le contrôleur de domaine principal du compte de service AGPM.

S’il s’agit de gérer des objets de stratégie de groupe sur plusieurs domaines ou si un serveur membre sera le serveur AGPM, vous devez configurer un autre compte en tant que compte de service AGPM, car le compte système local d’un contrôleur de domaine ne peut pas accéder aux objets de stratégie de groupe sur d’autres domaines.

 

**Pour modifier le compte de service AGPM**

1.  Sur l’ordinateur sur lequel est installé Microsoft Advanced Group Policy Management-serveur, cliquez sur **Démarrer**, puis sur **panneau de configuration**, cliquez sur **Ajouter ou supprimer des programmes**.

2.  Cliquez sur **gestion de la stratégie de groupe Microsoft avancée-serveur**, puis cliquez sur **modifier**.

3.  Cliquez sur **suivant**, puis sur **modifier**.

4.  Suivez les instructions à l’écran pour configurer les paramètres du service AGPM:

    1.  Pour le chemin d’accès de l’archive, confirmez ou modifiez l’emplacement de l’archivage par rapport au serveur AGPM. Le chemin d’accès d’archive peut pointer vers un dossier sur le serveur AGPM ou un autre emplacement, mais l’espace disponible doit être suffisant pour stocker tous les objets de stratégie de groupe et les données d’historique gérés par ce serveur AGPM.

    2.  Entrez les nouvelles informations d’identification pour le compte de service AGPM.

    3.  Pour le propriétaire de l’archive, entrez les informations d’identification d’un administrateur AGPM (contrôle total).

5.  Cliquez sur **modifier**, et une fois l’installation terminée, cliquez sur **Terminer**.

### Références supplémentaires

-   [Gestion du service AGPM](managing-the-agpm-service.md)

 

 





