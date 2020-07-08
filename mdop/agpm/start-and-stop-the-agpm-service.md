---
title: Démarrer et arrêter le service AGPM
description: Démarrer et arrêter le service AGPM
author: dansimp
ms.assetid: 769aa0ce-224a-446f-9958-9518af4ad159
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 33e797182d49157da0fe8f36dce17b4b35cdd623
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807461"
---
# Démarrer et arrêter le service AGPM


Le service AGPM est un service Windows agissant en tant que proxy de sécurité, gérant l’accès client aux objets de stratégie de groupe (GPO) dans l’environnement d’archivage et de production.

**Important**  L’arrêt ou la désactivation du service AGPM empêche les clients d’AGPM d’exécuter des opérations (par exemple, les listes ou les modifications d’objets de stratégie de groupe) par le biais du serveur.

 

Un compte d’utilisateur ayant accès au serveur AGPM (l’ordinateur sur lequel est installé le service AGPM) est requis pour effectuer cette procédure.

**Pour démarrer ou arrêter le service AGPM**

1.  Sur l’ordinateur sur lequel Microsoft Advanced Group Policy Management-Server (et par conséquent le service AGPM) est installé, cliquez sur **Démarrer**, sur **panneau de configuration**, sur **Outils d’administration**, puis sur **services**.

2.  Dans la liste des services, cliquez avec le bouton droit sur **service AGPM** et sélectionnez **Démarrer**, **redémarrer**ou **arrêter**.

    **Attention**  Ne modifiez pas les paramètres du service AGPM via les outils et **services** **d’administration** du système d’exploitation. Cela peut empêcher le démarrage du service AGPM. Pour modifier les paramètres du service, voir [gestion du service AGPM](managing-the-agpm-service.md).

     

### Références supplémentaires

-   [Gestion du service AGPM](managing-the-agpm-service.md)

 

 





