---
title: Résoudre les problèmes de mise à niveau d’AGPM
description: Résoudre les problèmes de mise à niveau d’AGPM
author: dansimp
ms.assetid: 1abbf0c1-fd32-46a8-a3ba-c005f066523d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2089eac51803dca60da51f61ebdb112fbf0bda08
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807430"
---
# Résoudre les problèmes de mise à niveau d’AGPM

Cette section répertorie les problèmes courants que vous pouvez rencontrer lors de la mise à niveau de votre serveur de gestion des stratégies de groupe (AGPM) avancé vers une nouvelle version (par exemple, AGPM 4,0 vers AGPM 4,3). Pour diagnostiquer des problèmes qui ne sont pas répertoriés ici, il est possible que vous deviez Voir la [résolution des](troubleshooting-agpm-agpm40.md) problèmes d’AGPM ou d’un administrateur AGPM (contrôle total) pour utiliser la journalisation et le suivi. Pour plus d’informations, voir [configurer la journalisation et le suivi](configure-logging-and-tracing-agpm40.md).

## Quels problèmes rencontrez-vous?

-   [Échec de la génération d’un rapport de différences d’objets de stratégie de groupe HTML (code d’erreur 80004003)](#bkmk-error-80004003)

### <a href="" id="bkmk-error-80004003"></a>Échec de la génération d’un rapport de différences d’objets de stratégie de groupe HTML (code d’erreur 80004003)

-   **Cause**: vous avez installé le package de mise à niveau d’AGPM avec un compte incorrect.

-   **Solution**: vous devrez être un administrateur d’AGPM pour pouvoir résoudre ce problème.
    
    -   Vérifiez que vous connaissez le nom d’utilisateur & mot de passe de votre **compte de service AGPM**.

    -   Connectez-vous sur votre serveur AGPM de manière interactive en tant que compte de service AGPM.
        
        -   C’est essentiel, car l’installation échoue si vous utilisez un autre compte.

    -   Arrêtez le service AGPM.
    
    -   Installez le correctif requis.
    
    -   Connectez-vous à AGPM à l’aide d’un client AGPM pour vérifier que vos rapports de différences fonctionnent désormais.
    
## Installer le correctif logiciel 1 pour la gestion avancée de la stratégie de groupe Microsoft 4,0 SP3
    
**Problème résolu dans ce correctif**: AGPM ne peut pas générer de rapports de différences quand il contrôle ou gère de nouveaux objets de stratégie de groupe.

**Pour obtenir cette mise à jour**, procédez comme suit: Installez la dernière version de Microsoft Desktop Optimization Pack ([version de maintenance du 2017 mars](https://www.microsoft.com/download/details.aspx?id=54967)). Pour plus d’informations, voir [KB 4014009](https://support.microsoft.com/help/4014009/) .

Plus précisément, vous pouvez choisir de télécharger uniquement le premier fichier, `AGPM4.0SP1_Server_X64_KB4014009.exe` dans la liste qui s’affiche après avoir appuyé sur le bouton Télécharger.
      
Pour plus d’informations [, consultez le](https://www.microsoft.com/download/details.aspx?id=54967)lien de téléchargement du pack d’optimisation de bureau de Microsoft (version de service de mars 2017).
      
      
## Lien de référence
https://support.microsoft.com/help/3127165/hotfix-package-1-for-microsoft-advanced-group-policy-management-4-0-sp
      
