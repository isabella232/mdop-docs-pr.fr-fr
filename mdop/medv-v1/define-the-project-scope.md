---
title: Définir la portée du projet
description: Définir la portée du projet
author: dansimp
ms.assetid: 84637d2a-2e30-417d-b150-dc81f414b3a5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4f33562452327bba9036f56d9f6f96650f00c1f0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810079"
---
# Définir la portée du projet


Lors de la définition de l’étendue du projet, déterminez les éléments suivants:

1.  Utilisateurs finaux MED-V: l’emplacement et le nombre d’utilisateurs finaux sont utilisés pour déterminer l’emplacement des installations du client MED-V et le nombre d’instances MED-v, ainsi que le nombre et la position des référentiels d’image MED-V.

2.  Les images d’ordinateur virtuel (VM) devant être gérées par MED-V, afin de déterminer la méthode de distribution d’images et de placement des référentiels d’image.

3.  Les attentes en matière de niveau de service de l’organisation, afin de déterminer les besoins en matière de performances et de tolérance de panne pour le serveur et la base de données MED-V, ainsi que le référentiel d’images.

4.  Valider avec l’entreprise: Assurez-vous d’avoir une idée complète des répercussions de l’infrastructure planifiée sur l’entreprise.

## Définir les utilisateurs finaux de MED-V


Tout d’abord, déterminez où se trouvent les utilisateurs finaux, ainsi que le nombre d’utilisateurs dans chaque emplacement. Deuxièmement, procurez-vous un diagramme d’infrastructure réseau qui affiche les emplacements des utilisateurs et la bande passante disponible vers ces emplacements. Enfin, vérifiez si les utilisateurs voyagent entre eux. Si les utilisateurs voyagent, des capacités supplémentaires peuvent être nécessaires pour la conception de l’infrastructure du serveur et des référentiels d’image.

## Déterminez les images MED-V à gérer par MED-V.


Une fois les utilisateurs finaux MED-V définis, Déterminez quels ordinateurs virtuels seront gérés par MED-V pour les utilisateurs de chaque emplacement.

Si l’un des ordinateurs virtuels est stocké dans une bibliothèque centralisée, déterminez l’emplacement de la bibliothèque de manière à ce qu’il puisse être évalué pour une utilisation comme un référentiel MED-V.

## <a href="" id="determine-the-organization-s-service-level-expectations"></a>Déterminez les attentes en matière de niveau de service de l’organisation.


Pour chaque espace de travail MED-V, notez la durée acceptable du chargement d’une nouvelle image et la période de déploiement des mises à jour critiques.

Le cas échéant, notez les attentes en matière de niveau de service pour la création de rapports MED-V, qui doivent être utilisées dans la conception de l’infrastructure du serveur.

## Valider avec l’entreprise


Posez les questions suivantes aux parties prenantes et aux propriétaires d’applications:

-   Existe-t-il des images qui peuvent être combinées? Par exemple, si l’application A sur WindowsXP est une image VPC et que l’application B sur WindowsXP est une autre image VPC, il est possible qu’une seule image puisse contenir les deux applications, ce qui permet de réduire l’espace de stockage et la bande passante requise pour le téléchargement d’images.

-   Est-ce que les applications dans le cadre d’une licence peuvent être gérées et prises en charge dans le cadre d’une VM par MED-V? Contactez le fournisseur de l’application pour veiller à ce que le contrat de licence et d’assistance ne soit pas violé en livrant l’application par MED-V.

 

 





