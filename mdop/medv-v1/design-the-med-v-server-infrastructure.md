---
title: Concevoir l'infrastructure de serveur MED-V
description: Concevoir l'infrastructure de serveur MED-V
author: dansimp
ms.assetid: 2781040f-880e-4e16-945d-a38c0adb4151
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 4ba4c38328c5484b7daa292f9fc33a4e59824327
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810403"
---
# Concevoir l'infrastructure de serveur MED-V


Dans cette rubrique, vous allez concevoir l’infrastructure du serveur pour chaque instance MED-V. Cela permet de déterminer si l’instance SQL Server existe sur le serveur MED-V ou sur un serveur distant, ainsi que la taille de la base de données SQL Server. Vous déterminez également l’emplacement de la console de gestion.

## Conception et placement du serveur pour chaque instance de MED-V


Le serveur MED-V implémente les stratégies et stocke les données de l’État et de l’historique concernant ses clients.

### Facteur de forme

MED-V recommande d’utiliser un serveur processeur double cœur 2,8 GHz avec 2 Go de RAM. Cette recommandation repose sur l’hypothèse que le serveur MED-V sera exécuté sur un ordinateur dédié et que SQL Server et la console de gestion MED-V s’exécutent sur des machines distinctes.

À partir de cette charge de travail, le serveur MED-V doit être relativement légèrement chargé. En l’absence de recommandations architecturales spécifiques sur le facteur de forme serveur, concevez le serveur à l’aide de la recommandation MED-V, en utilisant une mémoire qui correspond au facteur de forme standard de l’organisation. Le serveur MED-V peut être exécuté sur une machine virtuelle (VM) sur Windows Server 2008 Hyper-V. Si une machine virtuelle est utilisée, assurez-vous qu’elle a accès aux ressources de l’UC et de la mémoire équivalentes à celles spécifiées pour une machine physique.

La capacité de disque requise par le serveur MED-V doit être suffisante pour stocker les fichiers de configuration de l’espace de travail MED-V. Un espace de travail MED-V peut uniquement utiliser un ordinateur virtuel, et une stratégie pour un ou plusieurs utilisateurs. Par conséquent, le nombre d’espaces de travail MED-V qui doivent être stockés dépend du degré d’utilisation de stratégies différentes pour les utilisateurs de l’ordinateur virtuel, ainsi que du nombre d’ordinateurs virtuels qui seront utilisés. Les fichiers XML d’espace de travail MED-V sont en taille 30KB pour un espace de travail MED-V standard. Pour déterminer la capacité de disque requise, multipliez 30 Ko par le nombre d’espaces de travail MED-V que le serveur MED-V va stocker.

Les connexions réseau les plus importantes du serveur MED-V sont les liens vers ses clients et placent donc le serveur à un emplacement réseau qui fournit la bande passante la plus disponible et les liens les plus puissants vers ses clients.

### Tolérance de panne

Il ne peut y avoir qu’un seul serveur MED-V dans une instance MED-v, et MED-V n’inclut pas de fonctionnalités standard pour placer le serveur dans un cluster Microsoft Cluster Server (MSCS) pour fournir la tolérance de panne. Il est possible de configurer manuellement un serveur de sauvegarde passif.

Pour déterminer si un serveur de sauvegarde passif doit être configuré manuellement pour l’instance MED-V, déterminez si les utilisateurs sont autorisés à utiliser les images MED-V en mode hors connexion. Pour plus d’informations sur le mode hors connexion, voir [Comment configurer un utilisateur ou un groupe de domaines](how-to-configure-a-domain-user-or-groupmedvv2.md). Si les utilisateurs ne sont pas autorisés à travailler en mode hors connexion, ils ne seront pas en mesure de continuer à fonctionner en cas de panne du serveur MED-V, même si l’espace de travail MED-V est déjà démarré sur le client. Si le fonctionnement hors connexion est autorisé, pour chaque espace de travail MED-V, déterminez la durée pendant laquelle le client est autorisé à travailler en mode hors connexion avant de devoir s’authentifier. Il s’agit du laps de temps maximal que le serveur peut rendre indisponible.

## Conception et placement de la base de données SQL Server


Le serveur MED-V utilise la base de données SQL Server pour stocker l’État et les événements du client. Vous pouvez installer la base de données SQL Server sur le même ordinateur que le serveur MED-V ou vous pouvez la placer sur un serveur distinct exécutant SQL Server, qui peut éventuellement être distant. Vous pouvez partager la base de données avec d’autres instances MED-V, auquel cas les événements et les alertes de ces instances seront stockés dans la même base de données et les rapports incluront des événements de toutes les instances. Vous pouvez installer la base de données dans une instance SQL Server existante, et les bases de données d’autres serveurs MED-V peuvent résider dans la même instance.

Si vous placez le serveur de base de données à un emplacement distant distant du serveur MED-V, les liens réseau qui ne disposent pas de suffisamment de bande passante disponible permettent de charger les rapports dans la console et de ne pas afficher les données les plus récentes des clients. Reportez-vous aux attentes de niveau de service de l’organisation que vous avez définies dans [définir l’étendue du projet](define-the-project-scope.md) et utiliser ces informations pour décider de l’emplacement de la base de données SQL Server.

### Facteur de forme

Si vous exécutez SQL Server sur le même serveur que MED-V et que SQL Server sera uniquement utilisé pour stocker les données pour ce serveur, commencez par la recommandation MED-V et ajoutez des ressources pour la charge SQL Server. Si SQL Server stocke les événements et les alertes de plusieurs instances MED-V, pour plus d’informations sur la mise à l’échelle du facteur de forme du serveur, voir le Guide de [planification et de conception de l’infrastructure Microsoft SQL Server 2008](https://go.microsoft.com/fwlink/?LinkId=163302) (http://go.Microsoft.com/fwlink/?LinkId=163302).

La taille de la base de données dépend du nombre d’événements clients stockés par la base de données. Les événements sont créés par le fonctionnement normal du client, par exemple lorsqu’un espace de travail MED-V est démarré ou en cas d’erreur dans l’espace de travail MED-V. L’intervalle par défaut auquel le client envoie les événements est de 1 minute.

Pour estimer la taille de la base de données, déterminez les éléments suivants:

-   Nombre de clients de l’instance MED-V. La valeur maximale est 5 000.

-   Taux d’arrivée d’événements standard. Ce taux dépend du comportement d’utilisation du client, mais d’environ 15 à 20 événements par jour et par client.

-   Taille de l’événement. La taille est généralement de 200 octets.

-   Montant du stockage. Nombre de jours pendant lesquels les événements seront stockés.

Multipliez ces valeurs pour calculer la taille du stockage de données requis en octets, puis ajoutez un facteur de sécurité pour prendre en compte les éléments suivants:

-   Erreurs, qui peuvent créer un grand nombre d’événements à partir d’un client sur une courte période de temps.

-   Table de base de données et espace d’organisation.

Pour rapprocher la configuration requise pour l’optimisation de l’infrastructure (IOPs), utilisez les valeurs ci-dessus, en multipliant le taux d’arrivée des événements par défaut par le nombre de clients de l’instance. Le nombre d’enregistrements qu’il est possible d’écrire par jour est alors généré. Divisez ce nombre par 86 400 pour dériver le nombre d’enregistrements écrits par seconde. Si les opérations d’écriture peuvent être égales à l’aide d’une seule opération d’optimisation d’infrastructure, ce nombre est l’IOPs d’écriture requise. Ajoutez une mémoire tampon à l’activité de création de rapports. Il est difficile de déterminer le nombre de consoles utilisé avec l’instance et la fréquence à laquelle elles sont utilisées pour générer des rapports.

### Tolérance de panne

Lorsque le client MED-V est en cours d’exécution, si le serveur n’est pas disponible, les événements seront sauvegardés sur le client et les rapports seront indisponibles dans la console de gestion. Reportez-vous aux exigences de niveau de service de l’organisation définies dans [définir l’étendue du projet](define-the-project-scope.md) pour déterminer s’il est nécessaire de concevoir une infrastructure SQL Server tolérante aux pannes.

MED-V ne fournit pas de prise en charge pour exécuter SQL Server dans un cluster MSCS. Pour garantir la mise en veille chaude et éviter la perte de données en cas de panne, vous pouvez placer SQL Server dans une configuration d’envoi de journaux. Pour plus d’informations sur l’envoi de journaux, voir le Guide de [planification et de conception de l’infrastructure Microsoft SQL Server 2008](https://go.microsoft.com/fwlink/?LinkId=163302) ( https://go.microsoft.com/fwlink/?LinkId=163302) .

## Concevoir la console de gestion


Une partie de la fonctionnalité de la console de gestion MED-V consiste à tester les VM avant qu’elles ne soient compactes pour distribution aux clients MED-V. Par conséquent, la console de gestion doit être conçue à l’aide d’un facteur de forme semblable au facteur de forme d’un ordinateur client MED-V standard.

L’application console de gestion est installée conjointement avec le client MED-V et utilise Microsoft Virtual PC2007 SP1 avec le correctif décrit dans l’article 974918 de la base de connaissances Microsoft. Un système d’exploitation client doit être utilisé; la console de gestion MED-V ne peut pas s’exécuter sur le même système que le serveur MED-V.

Vous ne pouvez pas partager une console de gestion avec plusieurs instances de serveur MED-V. L’adresse du serveur MED-V est spécifiée lors de l’installation du client MED-V de la console de gestion. Cela peut être modifié après l’installation, mais à tout moment, la console de gestion ne peut fonctionner qu’avec un seul serveur MED-V.

Vous pouvez utiliser plusieurs consoles de gestion avec un seul serveur MED-V. Pour éviter les conflits, un mécanisme est disponible qui notifie les autres utilisateurs de la console lorsqu’une console a apporté des modifications à un espace de travail MED-V.

Pour chaque instance de MED-V, déterminez le nombre de consoles de gestion nécessaires et l’emplacement où elles seront placées. Sélectionnez un facteur de forme client MED-V standard à utiliser pour la console de gestion.

## Rubriques connexes


[Configurations prises en charge par MED-V1.0 SP1](med-v-10-sp1-supported-configurationsmedv-10-sp1.md)

[Configuration de serveur MED-V pour le mode cluster](configuring-med-v-server-for-cluster-mode.md)

[Comment installer le client MED-V et la console de gestion MED-V](how-to-install-med-v-client-and-med-v-management-console.md)

[Utilisation de l'interface utilisateur de la console de gestion MED-V](using-the-med-v-management-console-user-interface.md)

 

 





