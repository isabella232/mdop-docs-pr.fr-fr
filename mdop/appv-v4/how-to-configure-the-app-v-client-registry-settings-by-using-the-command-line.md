---
title: Procédure pour configurer les paramètres de registre du client App-V Client à l'aide de la ligne de commande
description: Procédure pour configurer les paramètres de registre du client App-V Client à l'aide de la ligne de commande
author: dansimp
ms.assetid: 3e3d873f-13d2-402f-97b4-f62d0c399171
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c424f39c8209ca641f6073838ebcb8726acc9e25
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807290"
---
# Procédure pour configurer les paramètres de registre du client App-V Client à l'aide de la ligne de commande


Après le déploiement et la configuration du client App-V) au cours de l’installation à l’aide de la ligne de commande, il peut être nécessaire de modifier un ou plusieurs paramètres de configuration du client. Pour cela, il suffit de modifier les clés de Registre appropriées en utilisant l’une des méthodes suivantes:

-   Utilisation de l’éditeur du Registre directement

-   À l’aide d’un fichier. reg

-   Utiliser un langage de script tel que VBScript ou Windows PowerShell

Vous pouvez également utiliser un modèle ADM. Pour plus d’informations sur le modèle ADM, voir <https://go.microsoft.com/fwlink/?LinkId=121835> .

**Attention**  Soyez vigilant lorsque vous modifiez le registre, car des erreurs peuvent sortir de l’ordinateur dans un état inutilisable. Veillez à suivre les pratiques d’entreprise standard relatives aux modifications du Registre. Testez minutieusement toutes les modifications proposées dans un environnement de test avant de les déployer sur des ordinateurs de production.

 

## Dans cette section


**Important**  Sur un ordinateur 64 bits, les clés et les valeurs décrites dans les sections suivantes seront sous HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\Client.

 

<a href="" id="how-to-reset-the-filesystem-cache"></a>[Procédure pour réinitialiser le cache de FileSystem](how-to-reset-the-filesystem-cache.md)  
Fournit les informations nécessaires pour réinitialiser le cache de systèmes de fichiers.

<a href="" id="how-to-change-the-size-of-the-filesystem-cache"></a>[Procédure pour modifier la taille du cache de FileSystem](how-to-change-the-size-of-the-filesystem-cache.md)  
Décrit la manière dont vous pouvez modifier la taille du cache.

<a href="" id="how-to-use-the-cache-space-management-feature"></a>[Procédure d'utilisation de la fonction de gestion de l'espace du cache](how-to-use-the-cache-space-management-feature.md)  
Décrit la manière dont vous pouvez configurer la fonctionnalité de gestion de l’espace de cache.

<a href="" id="how-to-configure-the-client-log-file"></a>[Procédure pour configurer le fichier journal du client](how-to-configure-the-client-log-file.md)  
Décrit les différentes valeurs de clé de Registre qui contrôlent le fichier journal du client et la façon de les modifier.

<a href="" id="how-to-configure-user-permissions"></a>[Procédure pour configurer les autorisations des utilisateurs](how-to-configure-user-permissions.md)  
Identifie la clé de Registre qui contrôle les autorisations de l’utilisateur et donne des exemples de la manière dont vous pouvez modifier certaines autorisations.

<a href="" id="how-to-configure-the-client-for-application-package-retrieval"></a>[Procédure pour configurer le client afin d'extraire le package d'application](how-to-configure-the-client-for-application-package-retrieval.md)  
Décrit la configuration du client pour récupérer le contenu, les icônes et les associations de types de fichiers dans différentes sources et fournit plusieurs exemples du format de chemin d’accès correct.

<a href="" id="how-to-configure-the-client-for-disconnected-operation-mode"></a>[Procédure pour configurer le client en mode de fonctionnement hors connexion](how-to-configure-the-client-for-disconnected-operation-mode.md)  
Fournit des informations sur la configuration des différents paramètres associés au mode opérations hors connexion.

<a href="" id="how-to-configure-shortcut-and-file-type-association-behavior"></a>[Procédure pour configurer le comportement d'association de type de fichier et de raccourci](how-to-configure-shortcut-and-file-type-association-behavior-46-only.md)  
Décrit les valeurs de clé de Registre qui contrôlent les raccourcis et les associations de types de fichiers dans le client App-V, et fournit des détails sur la façon de les configurer.

## Rubriques connexes


[Application Virtualization Client](application-virtualization-client.md)

 

 





