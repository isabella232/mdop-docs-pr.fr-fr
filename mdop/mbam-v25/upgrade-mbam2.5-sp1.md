---
title: Mise à niveau de MBAM 2,5 vers MBAM 2,5 SP1 de maintenance de la mise à jour de maintenance
author: dansimp
ms.author: ksharma
manager: miaposto
audience: ITPro
ms.topic: article
ms.prod: w10
ms.localizationpriority: Normal
ms.openlocfilehash: 372822e1ec049871c62af9f429290b88bbfac949
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804476"
---
# Mise à niveau de MBAM 2,5 vers MBAM 2,5 SP1 maintenance Release Update

Cet article fournit des instructions pas à pas pour mettre à niveau l’administration et la surveillance de Microsoft BitLocker (MBAM) 2,5 vers MBAM 2,5 Service Pack 1 (SP1) conjointement avec le [2019 Pack d’optimisation de bureau Microsoft](https://support.microsoft.com/help/4505175/may-2019-servicing-release-for-microsoft-desktop-optimization-pack)

Dans ce guide, nous allons utiliser une configuration à deux serveurs. Un serveur sera un serveur de base de données exécutant Microsoft SQL Server 2016. Ce serveur va héberger les bases de données et les rapports MBAM. L’autre serveur sera un serveur Web Windows Server 2012 R2. Ce serveur va héberger «administration et surveillance» et «portail libre-service».

## Préparer la mise à niveau de MBAM 2,5 SP1

### Familiarisez-vous avec les serveurs MBAM dans votre environnement

1. Moteur de base de données SQL Server: serveur qui héberge les bases de données MBAM.
2. SQL Server Reporting Services: serveur qui héberge les rapports MBAM.
3. Serveurs Web Internet Information Services (IIS): serveur qui héberge les applications Web MBAM et services MBAM.
4. Facultatif Serveur de site principal Microsoft System Center Configuration Manager: l’application de configuration MBAM est exécutée sur ce serveur pour intégrer les rapports MBAM avec Configuration Manager. Ces rapports sont ensuite fusionnés avec des rapports Configuration Manager existants dans l’instance de configuration de SQL Server Reporting Services (SSRS).

### Identifier les comptes de service, les groupes, le nom du serveur et l’URL des rapports

1. Identifiez le compte de service de pool d’applications MBAM utilisé par les serveurs Web IIS pour lire et écrire des données dans des bases de données MBAM.
2. Identifiez les groupes qui sont utilisés dans le cadre de la configuration des fonctionnalités Web MBAM et l’URL du service Web de rapports.
3. Identifiez le nom du serveur SQL et le nom de l’instance. Regardez cette vidéo pour en savoir plus.

    > [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE3ANP1]

4. Identifiez le compte SQL Server Reporting Services utilisé pour lire les données de conformité de la base de données d’audit et de conformité. Regardez cette vidéo pour en savoir plus.

    > [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE3ALdZ]

## Mettez à niveau l’infrastructure MBAM vers la dernière version disponible.

MBAM ou la mise à niveau de l’infrastructure du serveur est toujours effectuée dans l’ordre indiqué ci-dessous:

- Moteur de base de données SQL Server: bases de données
- SQL Server Reporting Services: rapports
- Serveur Web: applications Web
- Serveur SCCM: rapports intégrés SCCM, le cas échéant.
- Clients: mise à jour de l’agent ou du client MBAM
- Modèles de stratégie de groupe: mettez à jour la stratégie de groupe existante avec de nouveaux modèles et activez les nouveaux paramètres sur une stratégie de groupe MBAM existante.

> [!NOTE]
> Nous vous recommandons de créer une sauvegarde de base de données complète des bases de données MBAM avant d’exécuter les mises à niveau.

### Mettre à niveau MBAM SQL Server

Regardez cette vidéo pour découvrir comment mettre à niveau le serveur SQL MBAM:

   > [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE3ALew]

### Mettre à niveau le serveur Web MBAM

Regardez cette vidéo pour découvrir comment mettre à niveau le serveur Web MBAM:

   > [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE3ALex]

## Informations supplémentaires

Pour plus d’informations sur les problèmes connus dans MBAM 2,5 SP1, voir [notes de publication pour MBAM 2,5 SP1](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/release-notes-for-mbam-25-sp1).
