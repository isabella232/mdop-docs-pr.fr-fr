---
title: Planification de la procédure pour enregistrer et déployer l'image de récupération DaRT10
description: Planification de la procédure pour enregistrer et déployer l'image de récupération DaRT10
author: dansimp
ms.assetid: 9a3e5413-2621-49ce-8bd2-992616691703
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: bbaa8c4160970de90561f5ff8cedcefd08ca1dd7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809684"
---
# Planification de la procédure pour enregistrer et déployer l'image de récupération DaRT10


Vous pouvez enregistrer et déployer l’image de récupération Microsoft Diagnostics et Recovery Tools (DaRT) 10 en utilisant les méthodes suivantes. Lorsque vous déterminez la méthode à utiliser, examinez les avantages et inconvénients de chacun d’eux. Prenez également en considération votre infrastructure et votre équipe de support technique. Si vous disposez d’une petite infrastructure, vous souhaiterez peut-être déployer DaRT 10 à l’aide d’un support amovible, car l’image de récupération sera toujours disponible si vous l’installez sur le disque dur local.

Si votre organisation utilise les services de domaine Active Directory (AD DS), il est possible que vous souhaitiez déployer des images de récupération en tant que service réseau en utilisant Windows DS. Les images de récupération sont toujours disponibles pour les ordinateurs connectés. Vous pouvez déployer plusieurs images à partir de Windows DS et les conserver toutes au même endroit.

**Remarques**  Il est possible que vous souhaitiez utiliser plusieurs méthodes au sein de votre organisation. Par exemple, vous pouvez démarrer dans DaRT à partir d’une partition distante dans la plupart des cas, et disposer d’un lecteur flash USB dans le cas où l’ordinateur de l’utilisateur final ne peut pas se connecter au réseau.

 

Le tableau suivant présente quelques avantages et inconvénients de chaque méthode d’utilisation de DaRT au sein de votre organisation.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Méthode de démarrage dans DaRT</th>
<th align="left">Avantages</th>
<th align="left">Inconvénients</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Support amovible</strong></p>
<p>L’image de récupération est écrite sur un CD, un DVD ou un lecteur USB pour permettre au personnel de support d’adopter les outils de récupération pour l’ordinateur instable.</p></td>
<td align="left"><p>Prend en charge les scénarios dans lesquels l’enregistrement de démarrage principal (MBR) est endommagé et que vous ne pouvez pas accéder au disque dur et ne prend pas en charge les cas où il n’y a aucune connexion réseau.</p>
<p>Vous permet de créer plusieurs images de récupération avec différents outils pour fournir différents niveaux de prise en charge.</p>
<p>Fournit un outil intégré pour la gravure d’images de récupération sur un support amovible.</p></td>
<td align="left"><p>Nécessite que le personnel du support technique se trouve physiquement sur l’ordinateur de l’utilisateur final pour démarrer sur DaRT.</p>
<p>Il est nécessaire de disposer du temps et de la maintenance pour créer plusieurs éléments multimédias avec des configurations différentes pour les ordinateurs 32 et 64 bits.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>À partir d’une partition distante (réseau)</strong></p>
<p>L’image de récupération est hébergée sur un serveur de démarrage réseau tel que les services de déploiement Windows, qui permet aux utilisateurs ou au personnel de support de les diffuser sur des ordinateurs à la demande.</p></td>
<td align="left"><p>Disponible pour tous les ordinateurs ayant accès au serveur d’amorçage réseau.</p>
<p>Les images de récupération sont hébergées sur un serveur central, qui permet des mises à jour centralisées.</p>
<p>Le personnel de support centralisé peut fournir des réparations via une connexion à distance.</p>
<p>Aucun espace de stockage local requis pour les clients.</p>
<p>Possibilité de créer plusieurs images de récupération avec différents outils pour des niveaux de support spécifiques.</p></td>
<td align="left"><p>Le besoin de sécuriser l’infrastructure Windows DS pour s’assurer que les utilisateurs normaux peuvent démarrer uniquement l’image de récupération DaRT et non le processus complet d’imagerie du système d’exploitation.</p>
<p></p>
<p></p>
<p>Nécessite que l’ordinateur de l’utilisateur final est connecté au réseau lors de l’exécution.</p>
<p>Nécessite que l’image de récupération soit placée sur le réseau.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>À partir d’une partition de récupération sur le disque dur local</strong></p>
<p>L’image de récupération est installée sur un disque dur local manuellement ou à l’aide de systèmes de distribution de logiciels électroniques tels que System Center Configuration Manager.</p></td>
<td align="left"><p>L’image de récupération est toujours disponible, car elle est prédéfinie sur l’ordinateur.</p>
<p>Le personnel de support centralisé peut fournir une assistance via une connexion à distance.</p>
<p>L’image de récupération est gérée de manière centralisée et déployée.</p>
<p>Des demandes de clé de récupération supplémentaires sur des ordinateurs qui sont protégés par le chiffrement de lecteur BitLocker Windows sont éliminées.</p></td>
<td align="left"><p>Le stockage local est requis.</p>
<p>Il est recommandé de limiter les risques liés à une partition de démarrage qui est dédiée et non chiffrée.</p>
<p>Lors de la mise à jour de DaRT, vous devez mettre à jour tous les ordinateurs de votre entreprise au lieu d’une seule partition (sur le réseau) ou d’un appareil amovible.</p>
<p>Des considérations supplémentaires sont nécessaires si vous déployez l’image de récupération après activation de BitLocker.</p></td>
</tr>
</tbody>
</table>

 

## Rubriques connexes


[Planification du déploiement de DaRT10](planning-to-deploy-dart-10.md)

 

 





