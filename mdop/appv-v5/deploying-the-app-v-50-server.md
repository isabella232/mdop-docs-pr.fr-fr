---
title: Déploiement du serveur App-V5.0
description: Déploiement du serveur App-V5.0
author: dansimp
ms.assetid: a47f0dc8-2971-4e4d-8d57-6b69bbed4b63
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e8fb65015a172a88d5e27d377037348dbc044654
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805827"
---
# Déploiement du serveur App-V5.0


Vous pouvez installer les fonctionnalités du serveur App-V 5,0 à l’aide de différentes configurations de déploiement, décrites dans cette rubrique. Avant d’installer les fonctionnalités du serveur, consultez la section serveur des [considérations relatives à la sécurité dans App-V 5,0](app-v-50-security-considerations.md).

Pour plus d’informations sur le déploiement du serveur App-V 5,0 SP3, voir [à propos de App-v 5,0 SP3](about-app-v-50-sp3.md#bkmk-migrate-to-50sp3).

**Important**  Avant d’installer et de configurer les serveurs App-V 5,0, vous devez spécifier un port sur lequel chaque composant sera hébergé. Vous devez également ajouter les règles de pare-feu associées pour permettre aux demandes entrantes d’accéder aux ports spécifiés. Le programme d’installation ne modifie pas les paramètres du pare-feu.

 

## <a href="" id="---------app-v-5-0-server-overview"></a> Vue d’ensemble de App-V 5,0 Server


Le serveur App-V 5,0 est composé de cinq composants. Chaque composant a un but différent au sein de l’environnement App-V 5,0. Chacun des cinq composants est brièvement décrit ici:

-   Serveur de gestion: fournit une fonctionnalité de gestion générale de l’infrastructure App-V 5,0.

-   Base de données de gestion: facilite le déploiement de base de données pour la gestion d’App-V 5,0.

-   Serveur de publication: fournit des fonctionnalités d’hébergement et de streaming pour les applications virtuelles.

-   Serveur de création de rapports-fournit une application-V 5,0 Reporting Services.

-   Base de données de création de rapports: facilite les déploiements de base de données pour la création de rapports App-V 5,0.

## <a href="" id="---------app-v-5-0-stand-alone-deployment"></a> Déploiement autonome App-V 5,0


Le déploiement autonome de App-V 5,0 fournit une bonne topologie pour un déploiement ou un environnement de test de petite taille. Lorsque vous utilisez ce type d’implémentation, tous les composants serveur sont déployés sur un seul ordinateur. Les services et bases de données associées font concurrence pour les ressources de l’ordinateur qui exécute les composants App-V 5,0. Par conséquent, vous ne devez pas utiliser cette topologie pour les déploiements de plus grande envergure.

[Comment déployer le serveur App-V5.0](how-to-deploy-the-app-v-50-server-50sp3.md)

[Déploiement du serveur App-V5.0 à l'aide d'un script](how-to-deploy-the-app-v-50-server-using-a-script.md)

## <a href="" id="---------app-v-5-0-server-distributed-deployment"></a> Déploiement distribué de App-V 5,0 Server


La topologie de déploiement distribué peut prendre en charge une base de clients App-V 5,0 de grande taille et vous permet de gérer plus facilement votre environnement. Lorsque vous utilisez ce type de déploiement, les composants serveur App-V 5,0 sont déployés sur plusieurs ordinateurs, en fonction de la structure et des besoins de l’organisation.

[Comment installer les bases de données de gestion et de rapports sur des ordinateurs distincts des services de gestion et de rapports](how-to-install-the-management-and-reporting-databases-on-separate-computers-from-the-management-and-reporting-services.md)

[Comment installer le serveur de rapports sur un ordinateur autonome et le connecter à la base de données](how-to-install-the-reporting-server-on-a-standalone-computer-and-connect-it-to-the-database.md)

[Déploiement du serveur App-V5.0 à l'aide d'un script](how-to-deploy-the-app-v-50-server-using-a-script.md)

[Comment installer le serveur de publication sur un ordinateur distant](how-to-install-the-publishing-server-on-a-remote-computer.md)

[Comment installer le serveur de gestion sur un ordinateur autonome et le connecter à la base de données](how-to-install-the-management-server-on-a-standalone-computer-and-connect-it-to-the-database.md)

## Utilisation d’une solution de distribution de logiciels d’entreprise (ESD) et App-V 5,0


Vous pouvez également déployer les clients et packages App-V 5,0 à l’aide d’une ESD sans déployer App-V 5,0. Les fonctionnalités complètes d’intégration varient en fonction du niveau de ESD que vous utilisez.

**Remarques**  Le serveur et la base de données de création de rapports App-V 5,0 peuvent toujours être déployés avec la fonctionnalité ESD pour collecter les données de rapport à partir des clients App-V 5,0. Toutefois, les trois autres composants serveur ne doivent pas être déployés, car ils vont entrer en conflit avec la fonctionnalité ESD.

 

[Déploiement de packages App-V5.0 à l'aide d'une solution de distribution électronique de logiciels (ESD)](deploying-app-v-50-packages-by-using-electronic-software-distribution--esd-.md)

## <a href="" id="---------app-v-5-0-server-logs"></a> Journaux de l’App-V 5,0 Server


Vous pouvez utiliser les informations du journal du serveur App-V 5,0 pour résoudre les problèmes liés à l’installation du serveur et aux événements opérationnels lors de l’utilisation d’App-V 5,0. Les informations du journal relatives au serveur peuvent être examinées à l’aide de l' **Observateur d’événements**. La ligne suivante affiche le chemin d’accès spécifique aux événements liés au serveur:

**Journaux de l’observateur d’événements \ \ applications et services**

Les journaux d’installation associés sont enregistrés dans l’annuaire suivant:

**temporaire**

Dans App-V 5,0 SP3, certains journaux ont été consolidés et déplacés. Voir [à propos de App-V 5,0 SP3](about-app-v-50-sp3.md#bkmk-event-logs-moved).

## <a href="" id="---------app-v-5-0-reporting"></a> Rapports App-V 5,0


Les rapports App-V 5,0 permettent aux clients App-V 5,0 de collecter des données, puis de les renvoyer dans un référentiel central. Vous pouvez utiliser ces informations pour obtenir un meilleur aperçu de l’utilisation des applications virtuelles au sein de votre organisation. La liste suivante présente certains types d’informations recueillies par le client App-V 5,0:

-   Des informations sur l’ordinateur qui exécute le client App-V 5,0.

-   Des informations sur les packages virtualisés sur un ordinateur spécifique exécutant le client App-V 5,0.

-   Des informations sur l’ouverture et l’arrêt du package pour un utilisateur spécifique.

Les informations de rapport seront conservées jusqu’à ce qu’elles soient correctement envoyées à la base de données du serveur de rapports. Une fois les données dans la base de données, vous pouvez utiliser Microsoft SQL Server Reporting Services pour générer les rapports nécessaires.

Si vous souhaitez récupérer des informations de rapport, vous devez utiliser Microsoft SQL Server Reporting Services (SSRS) disponible avec Microsoft SQL. SSRS n’est pas installé lors de l’installation du serveur de rapports App-V 5,0 et doit être déployé séparément pour générer les rapports associés.

Pour plus d’informations [sur la création de rapports App-V 5,0](about-app-v-50-reporting.md), utilisez le lien suivant.

[Activation de la création de rapports sur App-V5.0 Client à l'aide de PowerShell](how-to-enable-reporting-on-the-app-v-50-client-by-using-powershell.md)

## Autres ressources pour le serveur App-V


[Déploiement d'App-V5.0](deploying-app-v-50.md)






 

 





