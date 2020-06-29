---
title: Sécurité d'App-V Desktop Client
description: Sécurité d'App-V Desktop Client
author: dansimp
ms.assetid: 216b9c16-7bb4-4f94-b9d8-810501285008
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 26add6f855780113613cf1591c41722643954477
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809282"
---
# Sécurité d'App-V Desktop Client


Le client de bureau App-V fournit de nombreuses améliorations liées à la sécurité qui ne sont pas disponibles dans les versions précédentes du produit. Ces modifications fournissent des niveaux de sécurité plus élevés par défaut et par le biais de la configuration des paramètres du client.

**Remarques**  Lorsque vous installez le client de bureau App-V sur un ordinateur, le logiciel utilise par défaut les paramètres les plus sécurisés. Toutefois, lors de la mise à niveau, les paramètres précédents du client persistent.

 

Par défaut, le client de bureau App-V est configuré uniquement avec les autorisations nécessaires pour permettre à un utilisateur non administratif d’effectuer une actualisation de publication et des applications de flux. D’autres améliorations apportées à la sécurité fournies dans le client de bureau App-V incluent les éléments suivants:

-   Par défaut, la mise à jour du cache OSD est autorisée uniquement par le processus d’actualisation de la publication.

-   Le fichier journal ( `sftlog.txt` ) est accessible uniquement par les comptes disposant d’un accès administratif local au client.

-   La taille du fichier journal est désormais maximale.

-   Les fichiers journaux sont gérés par le biais des paramètres d’archivage.

-   La journalisation des événements système est désormais effectuée.

## Autorisations


Après avoir installé le client de bureau, vous pouvez configurer d’autres paramètres de sécurité via la console MMC ou sur un client individuel à l’aide du registre ou du modèle ADM fourni par Microsoft. Le client de bureau App-V dispose d’autorisations que vous pouvez définir pour limiter les utilisateurs non administrateurs à l’accès à toutes les fonctionnalités du client de bureau. Pour obtenir la liste complète des autorisations, voir le fichier d’aide du client App-V ou le Guide de fonctionnement de l’application-v.

**Important**  Prenez soigneusement en considération les conséquences du changement de droits d’accès, en particulier sur les systèmes partagés par plusieurs utilisateurs, tels que les serveurs de terminaux.

 

**Remarques**  Si les utilisateurs de l’environnement disposent de privilèges d’administrateur local sur leurs ordinateurs, les autorisations ne sont pas prises en compte.

 

### Modèle ADM

Microsoft Application Virtualization (App-V) introduit un modèle ADM qui vous permet de configurer les paramètres de client les plus courants par le biais des stratégies de groupe. Ce modèle permet aux administrateurs d’implémenter et de modifier un grand nombre des paramètres du client par le biais d’un modèle d’administration centralisée. Certains des paramètres disponibles dans le modèle ADM sont paramètres de sécurité.

**Important**  Lorsque vous utilisez le modèle ADM, souvenez-vous que les paramètres sont des paramètres de préférence de stratégie de groupe et pas de stratégies de groupe entièrement gérées.

 

Pour obtenir une description complète du modèle ADM, des paramètres spécifiques et des recommandations pour le déploiement réussi de vos clients dans votre environnement, voir le livre blanc sur le modèle application-V ADM à l’adresse [https://go.microsoft.com/fwlink/LinkId=122063](https://go.microsoft.com/fwlink/?LinkId=122063) .

## Supprimer des associations de types de fichiers OSD


Si votre organisation n’a pas besoin d’ouvrir des applications directement à partir d’un fichier OSD, vous pouvez améliorer la sécurité en supprimant les associations de types de fichiers sur le client. Supprimez les `HKEY_CURRENT_USERS` clés pour l’OSD et `Softgird.osd.file` en utilisant l’éditeur du Registre. Vous pouvez placer ce processus dans un script d’ouverture de session ou dans un script de post-installation pour automatiser ces modifications.

 

 





