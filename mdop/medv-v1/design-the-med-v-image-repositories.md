---
title: Concevoir les référentiel d'images MED-V
description: Concevoir les référentiel d'images MED-V
author: dansimp
ms.assetid: e153154d-2751-4990-b94d-a2d76242c15f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e0c59a0dd2d1b3a78bd211c6a6353a86c77d8fc2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810061"
---
# Concevoir les référentiel d'images MED-V


Une fois les images MED-V créées et conditionnées, elles peuvent être stockées sur un serveur de fichiers dans n’importe quel emplacement. Les fichiers sont envoyés sur HTTP ou HTTPs par un ou plusieurs serveurs IIS. Le référentiel d’images peut être partagé par plusieurs instances MED-V.

Pour concevoir les référentiels d’image, vous devez d’abord déterminer la façon dont les images seront déployées sur chaque client, puis si ce client nécessite un référentiel d’image local. Tout référentiel est alors conçu et placé, ainsi que le serveur IIS qui lui est associé.

## Déterminer la façon dont les images seront déployées


Pour chaque espace de travail MED-V, déterminez le mode de déploiement d’images MED-V vers le client. Il est important de déterminer le nombre de référentiels nécessaires au stockage des images compactées, où ces référentiels seront placés, puis de concevoir ces référentiels.

Les images compactées peuvent être déployées comme suit:

-   Téléchargé sur le réseau à partir d’un serveur de distribution d’images, qui comprend un serveur de fichiers et un serveur IIS.

-   Sur un support amovible, tel qu’un lecteur USB ou un DVD.

-   Pré-intermédiaire vers un répertoire de magasin d’images sur l’ordinateur client à l’aide d’un centre de distribution de logiciels d’entreprise.

Déterminez la méthode à utiliser pour déployer des images MED-V vers chacun des clients et si l’emplacement nécessite un référentiel d’image.

## Déterminer le nombre de référentiels d’images


À présent que vous avez déterminé le nombre minimum de référentiels dont vous avez besoin, ajoutez des informations supplémentaires si l’un des critères suivants s’applique:

-   Des raisons organisationnelles ou réglementaires permettant de séparer les images MED-V, il est possible que certaines images MED-V ne puissent pas coexister dans le même référentiel. Par exemple, les données personnelles sensibles peuvent exiger le stockage sur un serveur qui n’est disponible que pour un ensemble limité d’employés qui ont besoin d’accéder à ces données.

-   Clients sur réseaux isolés: si des images sont déployées sur le réseau, déterminez si des réseaux sont isolés et nécessitent un référentiel distinct. Par exemple, les organisations isolent souvent les réseaux de laboratoire des réseaux de production.

-   Clients sur réseaux distants: si des images sont déployées sur le réseau, il est possible que certains ordinateurs clients soient séparés du référentiel par des liens réseau disposant d’une bande passante insuffisante pour offrir une connaissance appropriée lorsqu’un client charge un espace de travail MED-V. Le cas échéant, concevez des instances MED-V supplémentaires pour répondre à ce besoin.

Ajoutez ces référentiels à la conception. Déterminez le nom de chaque référentiel et la raison pour le concevoir. Déterminez les images MED-V que les référentiels comprendront et quels sont les clients MED-v qui chargera des espaces de travail MED-v avec des images du référentiel.

## Conception et placement des référentiels d’images


Lorsqu’une nouvelle image est disponible pour les clients, les clients commencent à télécharger l’image en même temps. Cela crée une forte demande sur le référentiel et doit être pris en compte lors de la conception du référentiel d’images.

Pour chaque référentiel, déterminez la quantité de données qu’elle va stocker. Somme de la taille d’images qui seront stockées dans le référentiel. Il s’agit de la valeur de l’espace disque requis sur le serveur de fichiers.

Ensuite, ajoutez le nombre de clients susceptibles de télécharger des images MED-V à partir du référentiel. C’est le nombre maximal de téléchargements simultanés qui peuvent se produire quand une nouvelle image MED-V est chargée dans le référentiel. Le serveur de fichiers doit être conçu avec un sous-système de disque capable de répondre aux demandes d’e/s qui seront créées.

Le référentiel d’images peut résider sur le même système que le serveur MED-V et au serveur exécutant SQL Server, ou sur un partage de fichiers distant. Vous pouvez également l’exécuter sur un ordinateur virtuel Windows Server 2008 Hyper-V. Vérifiez l’emplacement réseau des clients que le référentiel d’images va traiter et placez le référentiel à un emplacement réseau où il disposera d’une bande passante suffisante pour répondre aux attentes du niveau de service de ces clients.

### Tolérance de panne

Si le référentiel d’image n’est pas disponible, les clients ne seront pas en mesure de télécharger les images MED-V nouvelles ou mises à jour. Pour concevoir des options de tolérance de panne pour le serveur de fichiers et les disques à tolérance de panne, voir le Guide de [planification et de conception de l’infrastructure Microsoft SQL server 2008](https://go.microsoft.com/fwlink/?LinkId=163302) .

## Conception et placement des serveurs IIS


Cette section ne concerne que les clients qui téléchargent des fichiers image à l’aide de HTTP ou HTTPs.

Le serveur IIS peut cohabiter sur le même système que le serveur MED-V et au serveur exécutant SQL Server. Il peut également être exécuté sur un ordinateur virtuel Windows Server 2008 Hyper-V. L’infrastructure du serveur IIS doit disposer d’un débit suffisant pour livrer des images aux clients au sein des attentes de niveau de service de l’organisation. Elle doit être conçue avec un sous-système de disque capable de répondre aux demandes d’e/s créées.

Pour chaque référentiel d’images, totalisez le nombre de clients qui peuvent télécharger des images MED-V à l’aide d’IIS. C’est le nombre maximal de téléchargements simultanés qui peuvent se produire lors du chargement d’une image dans le référentiel. Utiliser la somme du débit et les prévisions de niveau de service définies dans [définir l’étendue du projet](define-the-project-scope.md) pour planifier la conception de l’infrastructure du serveur IIS et déterminer la quantité de bande passante nécessaire à l’allocation pour le référentiel.

Pour concevoir l’infrastructure IIS, voir le Guide de [planification et de conception de l’infrastructure Microsoft Internet Information Services](https://go.microsoft.com/fwlink/?LinkId=160826) .

### Tolérance de panne

Si l’infrastructure du serveur IIS n’est pas disponible, les clients ne seront pas en mesure de télécharger des images nouvelles ou mises à jour. Pour configurer la tolérance de panne, le serveur IIS Server 2008 Windows peut être placé dans un cluster de basculement. Pour concevoir la tolérance de panne pour l’infrastructure du serveur IIS, voir le Guide de [planification et de conception de l’infrastructure Microsoft Internet Information Services](https://go.microsoft.com/fwlink/?LinkId=160826) .

## Rubriques connexes


[Déploiement d'un espace de travail MED-V à l'aide d'un système de distribution de logiciels d'entreprise](deploying-a-med-v-workspace-using-an-enterprise-software-distribution-system.md)

[Déploiement d'un espace de travail MED-V à l'aide d'un package de déploiement](deploying-a-med-v-workspace-using-a-deployment-package.md)

 

 





