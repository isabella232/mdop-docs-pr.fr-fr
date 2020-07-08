---
title: Prise en main - Utilisation de MBAM avec Configuration Manager
description: Prise en main - Utilisation de MBAM avec Configuration Manager
author: dansimp
ms.assetid: b0a1d3cc-0b01-4b69-a2cd-fd09fb3beda4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 654de38918102a41395efe37dc593ce8f49113e4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810992"
---
# Prise en main - Utilisation de MBAM avec Configuration Manager


Lorsque vous installez Microsoft BitLocker administration et surveillance (MBAM), vous pouvez choisir une topologie qui intègre MBAM avec Configuration Manager 2007 ou SystemCenter2012 ConfigurationManager. Pour obtenir la liste des versions prises en charge du gestionnaire de configurations prises en charge par MBAM, voir [planification du déploiement d’MBAM avec Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md). Dans la topologie intégrée, les fonctionnalités de conformité matérielle et de création de rapports sont supprimées de MBAM et sont accessibles à partir de Configuration Manager.

**Important**  Windows to Go n’est pas pris en charge lorsque vous installez la topologie intégrée de MBAM avec Configuration Manager 2007.

 

## Utilisation de MBAM avec Configuration Manager


L’intégration de MBAM est basée sur un nouveau Pack de configuration qui installe les trois éléments suivants dans Configuration Manager 2007 ou SystemCenter2012 ConfigurationManager, qui est décrit en détail dans les sections suivantes:

Données de configuration composées d’éléments de configuration et d’un planning de référence de configuration

Collection

Rapports

### Données de configuration

Les données de configuration installent un planning de référence, appelé «protection BitLocker», qui contient deux éléments de configuration: «protection de lecteur du système d’exploitation BitLocker» et «protection des lecteurs de données fixes BitLocker». Le planning de référence de configuration est déployé sur la collection, qui est également créé lors de l’installation d’MBAM. Les deux éléments de configuration fournissent la base pour évaluer l’état de conformité des ordinateurs clients. Ces informations sont capturées, stockées et évaluées dans Configuration Manager. Les éléments de configuration sont basés sur les exigences en matière de conformité des lecteurs du système d’exploitation (OSDs) et des lecteurs de données fixes (FDDs). Les informations requises pour les ordinateurs déployés sont collectées afin de permettre d’évaluer la conformité de ces types de lecteurs. Par défaut, la planification de la configuration évalue le statut de conformité toutes les 12 heures et envoie les données de conformité à Configuration Manager.

### Collection

MBAM crée une collection appelée MBAM d’ordinateurs pris en charge. Le planning de référence de la configuration est ciblé vers les ordinateurs clients qui se trouvent dans cette collection. Il s’agit d’une collection dynamique qui, par défaut, s’exécute toutes les 12 heures et évalue l’appartenance. L’appartenance est basée sur trois critères:

-   Il s’agit d’une version prise en charge du système d’exploitation Windows. Pour l’instant, MBAM prend en charge uniquement Windows 7 entreprise et Windows 7 édition intégrale, Windows 8 entreprise et Windows to Go, lorsque Windows to Go est en cours d’exécution sur Windows 8 entreprise.

-   Il s’agit d’un ordinateur physique. Les machines virtuelles ne sont pas prises en charge.

-   Le module de plateforme sécurisée (TPM) est disponible. Une version compatible de TPM 1,2 ou version ultérieure est requise pour Windows 7. Windows 8 et Windows to Go ne nécessitent pas de module de plateforme sécurisée.

La collection est évaluée par rapport à tous les ordinateurs et crée le sous-ensemble d’ordinateurs compatibles assurant la base de l’évaluation de la conformité et de la création de rapports pour l’intégration d’MBAM.

### Rapports

Il existe quatre rapports que vous pouvez utiliser pour afficher la conformité. Ils sont les suivants:

-   **Tableau de bord de conformité de l’entreprise BitLocker** : fournit aux administrateurs trois différents affichages d’informations dans un seul rapport: distribution de l’état de conformité, distribution non conforme-erreurs et distribution de l’état de conformité par type de lecteur. Les options d’exploration du rapport permettent aux administrateurs informatiques de cliquer sur les données et d’afficher la liste des ordinateurs qui correspondent à l’état que vous avez sélectionné.

-   **Détails de la conformité d’entreprise BitLocker** -permet aux administrateurs informatiques d’afficher des informations sur l’état de conformité du chiffrement BitLocker de l’entreprise et inclut l’état de conformité de chaque ordinateur. Les options d’exploration du rapport permettent aux administrateurs informatiques de cliquer sur les données et d’afficher la liste des ordinateurs qui correspondent à l’état que vous avez sélectionné.

-   **Conformité de l’ordinateur BitLocker** -permet aux administrateurs informatiques d’afficher un ordinateur individuel et de déterminer pourquoi il a été signalé avec un statut de conformité ou non conforme. Le rapport affiche également l’état de chiffrement des lecteurs du système d’exploitation (OSD) et des lecteurs de données fixes (FDDs).

-   **Résumé de conformité de BitLocker Enterprise** : permet aux administrateurs d’afficher l’état de la conformité de l’entreprise avec la stratégie MBAM. L’état de chaque ordinateur est évalué, et le rapport affiche un résumé de la conformité de tous les ordinateurs de l’entreprise par rapport à la stratégie. Les options d’exploration du rapport permettent aux administrateurs informatiques de cliquer sur les données et d’afficher la liste des ordinateurs qui correspondent à l’état que vous avez sélectionné.

## Architecture de haut niveau d’MBAM avec Configuration Manager


L’image ci-après illustre l’architecture MBAM avec la topologie de Configuration Manager. Cette configuration prend en charge jusqu’à 200 000 clients MBAM dans un environnement de production.

![architecture MBAM avec Configuration Manager](images/mbam2-cmserver.gif)

Voici une description des serveurs, des bases de données et des fonctionnalités de cette architecture. Les fonctionnalités de serveur et bases de données dans l’image d’architecture sont répertoriées sur l’ordinateur ou le serveur sur lequel nous vous recommandons de les installer.

-   **Serveur de base de données** : la **base de données de récupération**, la **base de données d’audit**et les **rapports d’audit** sont installés sur un serveur Windows et une instance SqlServer prise en charge. La base de données de récupération stocke les données de récupération collectées à partir des ordinateurs clients MBAM. La base de données d’audit stocke les données d’activité d’audit collectées sur les ordinateurs clients ayant accédé aux données de récupération. Les rapports d’audit fournissent des données sur l’état de conformité des ordinateurs clients de votre entreprise.

-   **Serveur de site principal de Configuration Manager** : le serveur Configuration Manager contient l’installation de MBAM Server avec la topologie d’intégration System Center Configuration Manager, qui doit être installée sur un serveur de site principal de Configuration Manager. Le serveur Configuration Manager collecte les informations d’inventaire matériel sur les ordinateurs clients et permet de signaler la compatibilité de BitLocker sur les ordinateurs clients. Lors de l’exécution de l’installation du serveur de configuration MBAM, une collection et les données de configuration sont installées sur le serveur de site principal de Configuration Manager.

-   **Serveur d’administration et de surveillance** : le **serveur d’administration et de surveillance** est installé sur un serveur Windows et se compose du site Web d’administration et de surveillance et des services Web de surveillance. Le site Web d’administration et de contrôle est utilisé pour effectuer des audits d’activité et accéder aux données de récupération (par exemple, les clés de récupération BitLocker). Le **portail libre-service** est également installé sur le serveur d’administration et de surveillance. Le portail permet aux utilisateurs finaux sur les ordinateurs clients de se connecter indépendamment à un site Web pour obtenir une clé de récupération en cas de perte ou d’oubli du mot de passe BitLocker. Les rapports d’audit sont également installés sur le serveur d’administration et de surveillance.

-   **Station de travail de gestion** : le **modèle de stratégie** est composé d’objets de stratégie de groupe définissant les paramètres d’implémentation de MBAM pour le chiffrement de lecteur BitLocker. Vous pouvez installer le modèle de stratégie sur n’importe quel serveur ou station de travail, mais celui-ci est généralement installé sur une station de travail de gestion prenant en charge un ordinateur client ou un serveur Windows. La station de travail ne doit pas nécessairement être un ordinateur dédié.

-   **Client MBAM** et ordinateur **client Configuration Manager**

    -   Le **client MBAM** effectue les tâches suivantes:

        -   Utilise des objets de stratégie de groupe pour appliquer le chiffrement BitLocker d’ordinateurs clients au sein de l’entreprise.

        -   Collecte la clé de récupération pour les trois types de lecteurs de données BitLocker: lecteurs du système d’exploitation, lecteurs de données fixes et lecteurs de données amovibles (USB).

        -   Recueille des informations de récupération et des informations informatiques sur les ordinateurs clients.

    -   **Client Configuration Manager** – le client Configuration Manager permet à Configuration Manager de collecter les données de compatibilité matérielle relatives aux ordinateurs clients, et permet à Configuration Manager de signaler les informations de conformité.

## Rubriques connexes


[Utilisation de MBAM avec Configuration Manager](using-mbam-with-configuration-manager.md)

 

 





