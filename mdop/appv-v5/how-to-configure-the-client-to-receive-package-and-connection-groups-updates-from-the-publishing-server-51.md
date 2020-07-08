---
title: Comment configurer le client de manière à recevoir les mises à jour des groupes de connexion et des packages à partir du serveur de publication
description: Comment configurer le client de manière à recevoir les mises à jour des groupes de connexion et des packages à partir du serveur de publication
author: dansimp
ms.assetid: 23b2d03a-20ce-4973-99ee-748f3b682207
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 034cf5255d75bbaf6a5e65357bd5b3d472344f03
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805694"
---
# Comment configurer le client de manière à recevoir les mises à jour des groupes de connexion et des packages à partir du serveur de publication


Le déploiement de packages et de groupes de connexion à l’aide du serveur de publication App-V 5,1 est utile, car il offre une gestion à un point et une extensibilité élevée.

Procédez comme suit pour configurer le client App-V 5,1 pour recevoir des mises à jour du serveur de publication.

**Remarques**  Pour les procédures suivantes, le serveur de gestion a été installé sur un ordinateur nommé **MyMgmtSrv**et le serveur de publication a été installé sur un ordinateur nommé **MyPubSrv**.

 

**Pour configurer le client App-V 5,1 pour recevoir des mises à jour à partir du serveur de publication**

1.  Déployez les serveurs de publication et de gestion de l’application V 5,1, puis ajoutez les packages et groupes de connexion requis. Pour plus d’informations sur l’ajout de packages et de groupes de connexions, voir [Ajouter ou mettre à niveau des packages à l’aide de la console de gestion](how-to-add-or-upgrade-packages-by-using-the-management-console-51-gb18030.md) et [créer un groupe de connexion](how-to-create-a-connection-group51.md).

2.  Pour ouvrir la console de gestion, cliquez sur le lien suivant, ouvrez un navigateur et tapez les informations suivantes: http://MyMgmtSrv/AppvManagement/Console.html dans un navigateur Web, importez, publiez et activez tous les packages et groupes de connexion qui seront nécessaires pour un ensemble spécifique d’utilisateurs.

3.  Sur l’ordinateur exécutant le client App-V 5,1, ouvrez une invite de commandes PowerShell avec élévation de privilèges, exécutez la commande suivante:

    **Add-AppvPublishingServer-nom ABC-URL http://MyPubSrv/AppvPublishing**

    Cette commande configure le serveur de publication spécifié. La sortie doit apparaître comme suit:

    ID: 1

    SetByGroupPolicy: false

    Nom: ABC

    URL: http://MyPubSrv/AppvPublishing

    GlobalRefreshEnabled: false

    GlobalRefreshOnLogon: false

    GlobalRefreshInterval: 0

    GlobalRefreshIntervalUnit: jour

    UserRefreshEnabled: true

    UserRefreshOnLogon: true

    UserRefreshInterval: 0

    UserRefreshIntervalUnit: jour

    ID renvoyé, dans le cas présent 1

4.  Sur l’ordinateur exécutant le client App-V 5,1, ouvrez une invite de commandes PowerShell et tapez la commande suivante:

    **Synchronisation-AppvPublishingServer-ServerId 1**

    La commande interroge le serveur de publication pour les packages et groupes de connexion qui doivent être ajoutés ou supprimés pour ce client particulier en fonction des habilitations des packages et des groupes de connexion, comme configuré sur le serveur de gestion.

    Vous **avez une suggestion pour App-V**? Ajoutez ou Votez en fonction [de suggestions.](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization) **Vous avez un problème lié à l’application-V?** Utilisez le [Forum TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Rubriques connexes


[Opérations d'App-V5.1](operations-for-app-v-51.md)

 

 





