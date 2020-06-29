---
title: Surveillance des compteurs de performances pour les demandes de service web
description: Surveillance des compteurs de performances pour les demandes de service web
author: dansimp
ms.assetid: bdb812a1-465a-4098-b4c0-cb99890d1b0d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 2db96e3375562b48d289ea5a21dc7e89b800d1ad
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810218"
---
# Surveillance des compteurs de performances pour les demandes de service web


Le service d’administration et de surveillance de BitLocker Microsoft (MBAM) fournit des compteurs de performance qui enregistrent les performances des requêtes envoyées aux services Web suivants:

-   **StatusReportingService. svc** -service qui reçoit des demandes de statut de conformité

-   **CoreService. svc** -service qui reçoit des demandes de tentatives de récupération de clés

## Compteurs de performance fournis par MBAM


MBAM fournit les compteurs de performance suivants pour chacune des méthodes publiques qui sont implémentées par ses services Web StatusReportingService et CoreService:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Type de compteur de performance</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Nombre total de demandes</p></td>
<td align="left"><p>Fournit un nombre d’incréments commençant à zéro lors du démarrage ou du redémarrage du serveur.</p>
<p>Fournit une vue globale de l’activité du système. Peuvent être surveillés par des outils automatisés pour garantir l’intégrité du serveur et vérifier que le compteur est incrémenté d’une période donnée.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Demandes par seconde</p></td>
<td align="left"><p>Indique le débit actuel du serveur MBAM car il prend en charge la base de clients MBAM.</p>
<p>Permet aux administrateurs de sites d’effectuer les opérations suivantes:</p>
<ul>
<li><p>Calculez le nombre moyen de demandes par seconde, en fonction du nombre de clients MBAM et de la fréquence de création de rapports.</p></li>
<li><p>Vérifiez que le nombre de demandes par seconde est corrélé de manière générale avec le nombre moyen de demandes par seconde calculée. Une variance significative peut indiquer que le client MBAM n’est pas installé sur un pourcentage de la base du client ou qu’un objet de stratégie de groupe MBAM n’a pas été déployé correctement.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Durée de la demande</p></td>
<td align="left"><p>Enregistre la durée des demandes en millisecondes.</p>
<p>Même si ce compteur est mis à jour en fonction de la durée de chaque demande, les exemples de l’analyseur de performance Windows s’en trouvent périodiquement (en général, toutes les secondes), de sorte que vous pouvez voir la variabilité de la valeur. Pour cette raison, envisagez d’utiliser la valeur moyenne affichée par l’analyseur de performances.</p></td>
</tr>
</tbody>
</table>

 

## Résultats et recommandations relatifs aux compteurs de performance


Lorsque vous ajoutez de nouveaux clients MBAM à un serveur MBAM doté de capacités de secours, vous vous attendez à voir une augmentation du nombre de demandes par seconde. Ce renforcement sera proportionnel au nombre de nouveaux ordinateurs client. La durée de requête moyenne reste relativement statique. Lorsque le serveur est proche de sa capacité maximale, les demandes par seconde commencent à se mettre en niveau, et la durée de requête moyenne commence à être plus longue.

Si vos serveurs MBAM peuvent prendre en charge votre base de clients, envisagez de déployer MBAM par phases sur différentes collections d’ordinateurs clients. Lorsque vous déployez MBAM sur chaque collection d’ordinateurs clients, nous vous conseillons de prendre des instantanés des compteurs de performance pour voir l’impact relatif du déploiement vers chaque nouvelle collection de clients. Si le nombre de demandes par seconde commence au niveau inférieur et que la durée de la requête moyenne augmente, envisagez d’améliorer l’infrastructure de votre serveur MBAM en effectuant l’une des opérations suivantes:

-   Déplacement de la base de données MBAM vers un cluster Microsoft SQL Server ou SQL Server dédié

-   MBAM de l’équilibrage de charge sur plusieurs serveurs Web Internet Information Services (IIS)

-   Déploiement de MBAM sur un matériel serveur plus puissant

## Affichage des compteurs de performance


L’outil recommandé pour afficher les compteurs de performance MBAM est moniteur de performance Windows, qui est fourni avec Windows. Si vous utilisez Windows PowerShell, vous n’avez pas besoin d’activer les compteurs avant de les afficher, dans la mesure où ils sont automatiquement enregistrés par l’applet de cmdlet Windows PowerShell **Enable-WebApplication** .

Pour obtenir des instructions détaillées sur l’affichage des compteurs de performance, voir [comment afficher les compteurs de performances de MBAM](https://go.microsoft.com/fwlink/?LinkId=393457).



## Rubriques connexes


[Gestion de MBAM2.5](maintaining-mbam-25.md)

 

 


## Vous avez une suggestion pour MBAM?
- Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring) 
- Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).


