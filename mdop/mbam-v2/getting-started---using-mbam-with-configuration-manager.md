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
ms.openlocfilehash: 9f23a0eba923608fb6e25e44ee2843f3cde4c2dc
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910809"
---
# <a name="getting-started---using-mbam-with-configuration-manager"></a>Prise en main - Utilisation de MBAM avec Configuration Manager


Lorsque vous installez Microsoft BitLocker Administration and Monitoring (MBAM), vous pouvez choisir une topologie qui intègre MBAM à Configuration Manager 2007 ou System Center 2012 Configuration Manager. Pour obtenir la liste des versions de Configuration Manager prise en charge par MBAM, voir [Planning to Deploy MBAM with Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md). Dans la topologie intégrée, les fonctionnalités de conformité matérielle et de rapport sont supprimées de MBAM et sont accessibles à partir de Configuration Manager.

**Important**  
Windows To Go n’est pas pris en charge lorsque vous installez la topologie intégrée de MBAM avec Configuration Manager 2007.

 

## <a name="using-mbam-with-configuration-manager"></a>Utilisation de MBAM avec Configuration Manager


L’intégration de MBAM est basée sur un nouveau pack de configuration qui installe les trois éléments suivants dans Configuration Manager 2007 ou System Center 2012 Configuration Manager, qui sont décrits en détail dans les sections suivantes :

Données de configuration constituées d’éléments de configuration et d’une ligne de base de configuration

Collection

Rapports

### <a name="configuration-data"></a>Données de configuration

Les données de configuration installent une ligne de base de configuration, appelée « BitLocker Protection », qui contient deux éléments de configuration : « BitLocker Operating System Drive Protection » et « BitLocker Fixed Data Drives Protection ». La ligne de base de configuration est déployée sur la collection, qui est également créée lors de l’installation de MBAM. Les deux éléments de configuration fournissent la base pour évaluer l’état de conformité des ordinateurs clients. Ces informations sont capturées, stockées et évaluées dans Configuration Manager. Les éléments de configuration sont basés sur les exigences de conformité des lecteurs de système d’exploitation (OSD) et des lecteurs de données fixes (FDD). Les détails requis pour les ordinateurs déployés sont collectés afin que la conformité de ces types de disques puisse être évaluée. Par défaut, la ligne de base de configuration évalue l’état de conformité toutes les 12 heures et envoie les données de conformité à Configuration Manager.

### <a name="collection"></a>Collection

MBAM crée une collection appelée Ordinateurs pris en charge par MBAM. La ligne de base de configuration est destinée aux ordinateurs clients qui font partie de cette collection. Il s’agit d’une collection dynamique qui, par défaut, s’exécute toutes les 12 heures et évalue l’appartenance. L’appartenance est basée sur trois critères :

-   Il s’agit d’une version prise en charge du Windows d’exploitation. Actuellement, MBAM prend uniquement en charge Windows 7 Entreprise et Windows 7 Édition Intégrale , Windows 8 Entreprise et Windows To Go, lorsque Windows To Go est en cours d’exécution sur Windows 8 Entreprise.

-   Il s’agit d’un ordinateur physique. Les machines virtuelles ne sont pas pris en charge.

-   Le module de plateforme fiable (TPM) est disponible. Une version compatible du TPM 1.2 ou version ultérieure est requise pour Windows 7. Windows 8 et Windows to go ne nécessitent pas de TPM.

La collection est évaluée par rapport à tous les ordinateurs et crée le sous-ensemble d’ordinateurs compatibles qui fournit la base pour l’évaluation de la conformité et la création de rapports pour l’intégration MBAM.

### <a name="reports"></a>Rapports

Il existe quatre rapports que vous pouvez utiliser pour afficher la conformité. Ils sont les suivants:

-   **BitLocker Entreprise** tableau de bord de conformité : offre aux administrateurs informatiques trois vues différentes des informations sur un seul rapport : Distribution de l’état de conformité, Non conforme – Distribution des erreurs et Distribution de l’état de conformité par type de lecteur. Les options d’analyse du rapport vous permet aux administrateurs informatiques de cliquer sur les données et d’afficher la liste des ordinateurs qui correspondent à l’état que vous sélectionnez.

-   BitLocker Entreprise conformité : permet aux **administrateurs** informatiques d’afficher des informations sur l’état de conformité du chiffrement BitLocker de l’entreprise et inclut l’état de conformité pour chaque ordinateur. Les options d’analyse du rapport vous permet aux administrateurs informatiques de cliquer sur les données et d’afficher la liste des ordinateurs qui correspondent à l’état que vous sélectionnez.

-   **Conformité de l’ordinateur BitLocker** : permet aux administrateurs informatiques d’afficher un ordinateur individuel et de déterminer pourquoi il a été signalé avec un état donné conforme ou non conforme. Le rapport affiche également l’état de chiffrement des lecteurs de système d’exploitation (OSD) et des lecteurs de données fixes (FDD).

-   **BitLocker Entreprise conformité –** permet aux administrateurs informatiques d’afficher l’état de conformité de l’entreprise avec la stratégie MBAM. L’état de chaque ordinateur est évalué et le rapport affiche un résumé de la conformité de tous les ordinateurs de l’entreprise par rapport à la stratégie. Les options d’analyse du rapport vous permet aux administrateurs informatiques de cliquer sur les données et d’afficher la liste des ordinateurs qui correspondent à l’état que vous sélectionnez.

## <a name="high-level-architecture-of-mbam-with-configuration-manager"></a>High-Level architecture de MBAM avec Configuration Manager


L’image suivante illustre l’architecture MBAM avec la topologie Configuration Manager. Cette configuration prend en charge jusqu’à 200 000 clients MBAM dans un environnement de production.

![Architecture mbam avec configuration Manager.](images/mbam2-cmserver.gif)

Voici une description des serveurs, des bases de données et des fonctionnalités de cette architecture. Les fonctionnalités serveur et les bases de données de l’image d’architecture sont répertoriées sous l’ordinateur ou le serveur sur lequel nous vous recommandons de les installer.

-   **Serveur de base de** données : **la**base de données de récupération, la base de données **d’audit**et les rapports **d’audit** sont installés sur un serveur Windows et pris en charge SQL Server instance. La base de données de récupération stocke les données de récupération collectées à partir des ordinateurs clients MBAM. La base de données d’audit stocke les données d’activité d’audit collectées sur les ordinateurs clients qui ont accédé aux données de récupération. Les rapports d’audit fournissent des données sur l’état de conformité des ordinateurs clients de votre entreprise.

-   **Serveur** de site principal Configuration Manager : le serveur Configuration Manager contient l’installation du serveur MBAM avec la topologie intégration System Center Configuration Manager, qui doit être installée sur un serveur de site principal Configuration Manager. Le serveur Configuration Manager collecte les informations d’inventaire matériel des ordinateurs clients et est utilisé pour signaler la conformité BitLocker des ordinateurs clients. Lorsque vous exécutez l’installation du serveur d’installation MBAM, une collection et les données de configuration sont installées sur le serveur de site principal Configuration Manager.

-   **Serveur d’administration** **** et de surveillance : le serveur d’administration et de surveillance est installé sur un serveur Windows et se compose du site web Administration et surveillance et des services web de surveillance. Le site Web Administration et surveillance est utilisé pour auditer l’activité et accéder aux données de récupération (par exemple, les clés de récupération BitLocker). Le **portail libre-service est** également installé sur le serveur d’administration et de surveillance. Le portail permet aux utilisateurs finaux sur les ordinateurs clients de se connecter indépendamment à un site web pour obtenir une clé de récupération s’ils perdent ou oublient leur mot de passe BitLocker. Les rapports d’audit sont également installés sur le serveur d’administration et de surveillance.

-   **Station de travail de gestion** : le modèle de stratégie se compose d’objets de stratégie de groupe qui définissent les paramètres d’implémentation MBAM pour le chiffrement de lecteur BitLocker. **** Vous pouvez installer le modèle de stratégie sur n’importe quel serveur ou station de travail, mais il est généralement installé sur une station de travail de gestion qui est un serveur Windows ou un ordinateur client pris en charge. La station de travail n’a pas besoin d’être un ordinateur dédié.

-   **Ordinateur client MBAM** et **client Configuration Manager**

    -   Le **client MBAM effectue** les tâches suivantes :

        -   Utilise des objets de stratégie de groupe pour appliquer le chiffrement BitLocker des ordinateurs clients dans l’entreprise.

        -   Collecte la clé de récupération pour les trois types de lecteur de données BitLocker : lecteurs de système d’exploitation, lecteurs de données fixes et lecteurs de données amovibles (USB).

        -   Collecte les informations de récupération et les informations d’ordinateur sur les ordinateurs clients.

    -   **Client Configuration Manager** : le client Configuration Manager permet à Configuration Manager de collecter des données de compatibilité matérielle sur les ordinateurs clients et permet à Configuration Manager de signaler les informations de conformité.

## <a name="related-topics"></a>Rubriques associées


[Utilisation de MBAM avec Configuration Manager](using-mbam-with-configuration-manager.md)

 

 





