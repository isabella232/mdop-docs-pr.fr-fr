---
title: Architecture globale de MBAM 2.5 avec la topologie autonome
description: Architecture globale de MBAM 2.5 avec la topologie autonome
author: dansimp
ms.assetid: 35f8c5f6-8be3-443d-baf0-56d68b08f3bc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9ec9b1e4391fde3083564f34b5f89d1c5bd174f7
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910669"
---
# <a name="high-level-architecture-of-mbam-25-with-stand-alone-topology"></a>Architecture globale de MBAM 2.5 avec la topologie autonome


Cette rubrique décrit l’architecture recommandée pour le déploiement de Microsoft BitLocker Administration and Monitoring (MBAM) avec la topologie autonome Configuration Manager. Dans cette topologie, MBAM est déployé en tant que produit autonome. Vous pouvez également déployer MBAM avec la topologie d’intégration Configuration Manager, qui intègre MBAM à Configuration Manager. Pour plus d’informations, voir Architecture de haut niveau [de MBAM 2.5 avec](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md)la topologie d’intégration configuration manager.

Pour obtenir la liste des versions du logiciel pris en charge mentionnées dans cette rubrique, voir CONFIGURATIONS prise en charge [par MBAM 2.5.](mbam-25-supported-configurations.md)

**Remarque**  
Nous vous recommandons d’utiliser une architecture à serveur unique uniquement dans les environnements de test.

 

## <a name="recommended-number-of-servers-and-supported-number-of-clients"></a>Nombre recommandé de serveurs et nombre de clients pris en charge


Le nombre recommandé de serveurs et le nombre de clients pris en charge dans un environnement de production sont les suivants :

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Architecture recommandée dans un environnement de production</th>
<th align="left">Détails</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Nombre de serveurs et autres ordinateurs</p></td>
<td align="left"><p>Deux serveurs</p>
<p>Une station de travail</p></td>
</tr>
<tr class="even">
<td align="left"><p>Nombre d’ordinateurs clients pris en charge</p></td>
<td align="left"><p>500,000</p></td>
</tr>
</tbody>
</table>

 

## <a name="recommended-mbam-high-level-architecture-with-the-stand-alone-topology"></a>Architecture de haut niveau MBAM recommandée avec la topologie autonome


Le diagramme et le tableau suivants décrivent l’architecture à deux serveurs de haut niveau recommandée pour MBAM avec la topologie autonome. Les déploiements MBAM à forêts multiples nécessitent une confiance à sens simple ou double. Les confiances à sens seul nécessitent que le domaine serveur l’truste au domaine client.

![mbam2.](images/mbam2-5-2servers.png)

Fonctionnalités serveur à configurer sur ce serveur de base de données de description

Base de données de conformité et d’audit

Cette fonctionnalité est configurée sur un serveur exécutant Windows Server et prise en charge SQL Server instance.

La **base de données de conformité et d’audit** stocke les données de conformité, qui sont principalement utilisées pour les rapports SQL Server Reporting Services hôtes.

Base de données de récupération

Cette fonctionnalité est configurée sur un serveur exécutant Windows Server et prise en charge SQL Server instance.

La base **de données de** récupération stocke les données de récupération collectées à partir des ordinateurs clients MBAM.

Rapports

Cette fonctionnalité est configurée sur un serveur exécutant Windows Server et prise en charge SQL Server instance.

Les rapports **fournissent** des données d’état d’audit et de conformité de récupération sur les ordinateurs clients de votre entreprise. Vous pouvez accéder aux rapports à partir du site Web d’administration et de surveillance ou directement depuis SQL Server Reporting Services.

Serveur d’administration et de surveillance

Site web d’administration et de surveillance

Cette fonctionnalité est configurée sur un ordinateur exécutant Windows Server.

Le site **Web d’administration** et de surveillance est utilisé pour :

-   Aidez les utilisateurs finaux à reprendre l’accès à leurs ordinateurs lorsqu’ils sont verrouillés. (Cette zone du site Web est communément appelée Help Desk.)

-   Afficher les rapports qui indiquent l’état de conformité et l’activité de récupération pour les ordinateurs clients.

Self-Service Portal

Cette fonctionnalité est configurée sur un ordinateur exécutant Windows Server.

Le **portail libre-service** est un site web qui permet aux utilisateurs finaux sur des ordinateurs clients de se connecter indépendamment à un site web pour obtenir une clé de récupération s’ils perdent ou oublient leur mot de passe BitLocker.

Surveillance des services web pour ce site web

Cette fonctionnalité est configurée sur un ordinateur exécutant Windows Server.

Les **services web de surveillance** sont utilisés par le client MBAM et les sites web pour communiquer avec la base de données.

**Important**  
Le service Web de surveillance n’est plus disponible dans Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 SP1, car les sites web MBAM communiquent directement avec la base de données de récupération.

 

Station de travail de gestion

Modèles de stratégie de groupe MBAM

-   Les modèles de stratégie de groupe MBAM sont des paramètres de stratégie de groupe qui définissent les paramètres d’implémentation de MBAM, qui vous permettent de gérer le chiffrement de lecteur BitLocker.

-   Avant d’exécuter MBAM, vous devez télécharger les modèles de stratégie de groupe à partir de la page Comment obtenir des modèles de stratégie de groupe [MDOP (.admx)](https://go.microsoft.com/fwlink/p/?LinkId=393941) et les copier sur un serveur ou une station de travail qui exécute un système d’exploitation Windows Server ou Windows pris en charge.

-   La station de travail n’a pas besoin d’être un ordinateur dédié.

Ordinateur client MBAM client et Configuration Manager

Logiciel client MBAM

Le client MBAM :

-   Utilise des objets de stratégie de groupe pour appliquer le chiffrement de lecteur BitLocker sur les ordinateurs clients de l’entreprise.

-   Collecte la clé de récupération Bitlocker pour trois types de lecteurs de données : lecteurs de système d’exploitation, lecteurs de données fixes et lecteurs de données amovibles (USB).

-   Collecte les informations de récupération et les informations d’ordinateur sur les ordinateurs clients.



## <a name="related-topics"></a>Rubriques associées


[Prise en main de MBAM 2.5](getting-started-with-mbam-25.md)

[Architecture globale de MBAM 2.5 avec la topologie Intégration Configuration Manager](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md)

[Illustration des composants d'un déploiement de MBAM 2.5](illustrated-features-of-an-mbam-25-deployment.md)

 

## <a name="got-a-suggestion-for-mbam"></a>Vous avez une suggestion pour MBAM ?
- Ajoutez ou votez sur les suggestions [ici.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring) 
- Pour les problèmes de MBAM, utilisez le [forum TechNet MBAM.](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam) 





