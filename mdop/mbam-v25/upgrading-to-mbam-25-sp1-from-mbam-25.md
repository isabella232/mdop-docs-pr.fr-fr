---
title: Mise à niveau de MBAM2.5 vers MBAM2.5SP1
description: Mise à niveau de MBAM2.5 vers MBAM2.5SP1
author: dansimp
ms.assetid: ''
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 2/16/2018
ms.openlocfilehash: 330ded822dd9da96a1c33eabcb31d744044dc28e
ms.sourcegitcommit: ae34c5cb5e7979b472b257a4691142e493d5d6fe
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/30/2020
ms.locfileid: "11091619"
---
# Mise à niveau de MBAM2.5 vers MBAM2.5SP1
Cette rubrique décrit la procédure de mise à niveau du client d’administration et de surveillance Microsoft BitLocker (MBAM) Server 2,5 et du client MBAM 2,5 vers MBAM 2,5 SP1.

### Avant de commencer
#### Télécharger la version de service de 2019
[Pack d’optimisation de bureau](https://www.microsoft.com/download/details.aspx?id=58345)

#### Télécharger la version de maintenance 2018 de juillet
[Pack d’optimisation de bureau](https://www.microsoft.com/download/details.aspx?id=57157)


#### Vérification de l’installation de documentaion
Vérifiez que vous disposez d’une documentation actuelle sur votre environnement MBAM, y compris tous les noms des serveurs, les noms de base de données, les comptes de service et leurs mots de passe.

### Étapes de mise à niveau
#### Procédure de mise à niveau de la base de données MBAM (SQL Server)
1. À l’aide du configurateur MBAM; Supprimez le rôle rapports sur le serveur SQL Server, ou à partir de l’emplacement de la base de données SSRS. En fonction de votre environnement, il peut s’agir du même serveur ou d’un autre serveur.
  > [!NOTE]
  > Vous ne verrez pas les options de suppression des bases de données. C’est attendu.  
2. Installez 2,5 SP1 (qui se trouve avec MDOP-Microsoft Desktop Optimization Pack 2015 à partir du site Centre de gestion de licences en volume:  <https://www.microsoft.com/Licensing/servicecenter/default.aspx>
3. Ne pas configurer pour le moment 
4. À l’aide du configurateur MBAM; rajouter le rôle de rapport
5. À l’aide du configurateur MBAM; rajouter le rôle de base de données SQL sur le serveur SQL Server
6. À la fin, vous recevez un avertissement indiquant que la BD existe déjà et qu’elle n’a pas été créée, mais cela est attendu.
7. Ce processus met à jour les bases de données existantes vers la version actuelle installée.              

#### Procédure de mise à niveau du serveur MBAM (exécutant MBAM et IIS)
1. À l’aide du configurateur MBAM; supprimer les portails d’administration et d’auto-service du serveur IIS
2. Installer MBAM 2,5 SP1
3. Ne pas configurer pour le moment  
4. À l’aide du configurateur MBAM; rajouter les portails d’administrateur et libre-service au serveur IIS 
5. Ouvrez une invite de commandes avec élévation de privilèges, tapez **IISReset**, puis appuyez sur entrée.
 
#### Procédure de mise à niveau des clients/points de terminaison MBAM
1. Désinstaller l’agent 2,5 des points de terminaison client
2. Installer l’agent 2,5 SP1 sur les points de terminaison client
3. Faire basculer la mise à jour du client de la 2019 ROLLUP pour les clients exécutant l’agent 2,5 SP1 
4. Il n’est pas nécessaire de désinstaller le client existant avant de procéder à l’installation du 2019 ROLLUP.  
