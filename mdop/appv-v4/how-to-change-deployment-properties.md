---
title: Procédure pour modifier les propriétés de déploiement
description: Procédure pour modifier les propriétés de déploiement
author: dansimp
ms.assetid: 0a214a7a-cc83-4d04-89f9-5727153be918
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dfb42962d41159479db61da9c3beb3771ef35502
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807357"
---
# Procédure pour modifier les propriétés de déploiement


Vous pouvez utiliser les procédures suivantes pour modifier les informations de l’onglet **déploiement** d’une application que vous séquençage, y compris l’URL du serveur virtualisation des applications, les systèmes d’exploitation requis par les applications virtualisées et les options de sortie de l’application virtuelle à installer.

**Pour modifier l’URL du serveur**

1.  Dans la zone de liste déroulante, sélectionnez le protocole de diffusion.

2.  Entrez le nom d’hôte du serveur d’applications virtuel ou du solde de charge du groupe de serveurs. Vous pouvez utiliser le nom d’hôte réel ou l’adresse IP.

3.  Spécifiez le numéro de port sur lequel le serveur d’applications virtuelles ou l’équilibrage de charge doit écouter une demande de client de bureau de virtualisation d’application pour l’application en flux.

4.  Spécifiez le chemin d’accès relatif du serveur d’applications virtuel sur lequel est stocké le package logiciel.

**Pour modifier la configuration requise pour les systèmes d’exploitation des applications**

1.  Pour ajouter le ou les systèmes d’exploitation requis, sélectionnez-le dans la liste **disponible** et cliquez sur la flèche pointant sur le contrôle de liste systèmes d’exploitation **sélectionnés** .

2.  Pour supprimer un système d’exploitation, sélectionnez-le dans le contrôle de liste **sélectionné** , puis cliquez sur la flèche pointant sur le contrôle de liste systèmes d’exploitation **disponibles** .

**Pour modifier les options de sortie de l’application**

1.  Dans la liste déroulante **algorithme de compression** , sélectionnez la méthode de compression à utiliser lors de la diffusion de l’application.

2.  Cochez la case **appliquer les descripteurs de sécurité** pour vérifier que les descripteurs de sécurité des applications empaquetées sont appliqués lors du déploiement.

3.  Sélectionnez **générer un fichier de différences** pour générer un fichier de différences pour l’application à partir de la version séquencée précédente.

4.  Pour créer un package d’installation, sélectionnez **générer le package Microsoft Windows Installer (MSI)** .

## Rubriques connexes


[À propos de l'onglet Déploiement](about-the-deployment-tab.md)

[Console Sequencer](sequencer-console.md)

 

 





