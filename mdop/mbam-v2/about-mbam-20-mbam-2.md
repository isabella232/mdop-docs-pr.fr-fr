---
title: À propos de MBAM2.0
description: À propos de MBAM2.0
author: dansimp
ms.assetid: b43a0ba9-1c83-4854-a2c5-14eea0070e36
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7bdf24d1f375dd1fa8b18ac90c2fc49d2887c6c5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810482"
---
# À propos de MBAM2.0


Microsoft BitLockerAdministration et surveillance (MBAM) 2.0 fournit une interface d’administration simplifiée pour le chiffrement de lecteur BitLocker. BitLocker fournit une protection améliorée contre le vol de données ou l’exposition des données pour les ordinateurs perdus ou volés. BitLocker chiffre toutes les données stockées sur le volume du système d’exploitation Windows et sur les volumes de données configurés.

## À propos de MBAM 2.0


BitLockerAdministration et monitoring 2.0 appliquent les options de stratégie de chiffrement BitLocker que vous avez définies pour votre entreprise, surveille la conformité des ordinateurs clients avec ces stratégies et signale l’état de chiffrement de l’entreprise et des ordinateurs individuels. De plus, MBAM vous permet d’accéder aux informations de clé de récupération lorsque les utilisateurs oublient leur code confidentiel ou leur mot de passe, ou lorsque leur enregistrement de BIOS ou de démarrage est modifié.

**Remarques**  BitLocker n’est pas décrit en détail dans ce guide. Pour obtenir une vue d’ensemble de BitLocker, voir [vue d’ensemble du chiffrement de lecteur BitLocker](https://go.microsoft.com/fwlink/p/?LinkId=225013).

 

Les groupes suivants peuvent être intéressés par l’utilisation de MBAM pour gérer BitLocker:

-   Administrateurs, responsables de la sécurité informatique et responsables de la conformité chargés de veiller à ce que les données confidentielles ne soient pas divulguées sans autorisation.

-   Administrateurs responsables de la sécurité informatique de bureaux distants ou de succursales

-   Administrateurs responsables des ordinateurs clients exécutant Windows

## <a href="" id="what-s-new-in-mbam-2-0"></a>Nouveautés de MBAM 2.0


MBAM 2.0 fournit les nouvelles fonctionnalités et fonctionnalités suivantes.

### Intégration de System Center Configuration Manager avec MBAM

MBAM prend désormais en charge l’intégration à System Center Configuration Manager. Cette intégration transfère l’infrastructure de conformité MBAM dans l’environnement natif de Configuration Manager. Les administrateurs informatiques qui utilisent Configuration Manager au sein de leur entreprise peuvent désormais afficher l’état de la conformité de leurs entreprises dans la console de gestion Microsoft et explorer les rapports pour afficher des ordinateurs individuels.

### La compatibilité matérielle n’est disponible que dans la topologie d’intégration de Configuration Manager

L’intégration de Configuration Manager à MBAM permet de disposer de fonctionnalités de Configuration Manager qui autorisent ou empêchent l’utilisation de certains types de matériel avec MBAM et offre davantage de flexibilité que la compatibilité matérielle disponible dans MBAM 1,0. Les administrateurs informatiques peuvent créer leurs propres collections pour limiter le matériel et déployer le planning de référence de configuration MBAM sur ces collections. La compatibilité matérielle d’MBAM présente dans MBAM 1,0 est désormais uniquement disponible dans la topologie du gestionnaire de configurations MBAM et est administrée à partir de Configuration Manager.

### Politique flexible des protections

Les ordinateurs déjà chiffrés avec un protecteur (par exemple, module de plateforme sécurisée + code confidentiel ou de verrouillage automatique et mot de passe) et qui reçoivent une stratégie MBAM qui nécessite un sous-ensemble de ce chiffrement (par exemple, le TPM ou le déverrouillage automatique) sont considérés comme conformes. Dans l’exemple ci-dessus, les options code confidentiel et mot de passe ne sont pas supprimées automatiquement, sauf si l’administrateur informatique définit explicitement ces fonctionnalités comme n’étant plus autorisées.

Les ordinateurs qui ne sont pas chiffrés et qui reçoivent une stratégie MBAM (par exemple, GPC ou déverrouillage automatique) sont chiffrés en conséquence. Les utilisateurs disposant d’un administrateur local peuvent utiliser les outils de BitLocker (élément du panneau de configuration: chiffrement de lecteur BitLocker ou gérer-bde) pour ajouter ou modifier les protecteurs existants (par exemple, GPC + code confidentiel ou verrouillage automatique et mot de passe). Ils restent conformes sauf si les stratégies de MBAM les définissent spécifiquement.

### Possibilité de mise à niveau du client MBAM

Le programme d’installation du client MBAM 2.0 détecte la version du client existant et effectue les étapes requises pour effectuer une mise à niveau vers le client MBAM 2.0 à partir de versions précédentes.

### Possibilité de mettre à niveau le serveur MBAM à partir de versions précédentes

Vous pouvez mettre à niveau l’infrastructure du serveur MBAM 2.0 à partir des versions précédentes de MBAM comme suit:

**Remplacement manuel du serveur sur place** : vous devez désinstaller manuellement l’infrastructure du serveur MBAM existante, puis installer l’infrastructure du serveur 2,0 MBAM. Vous n’avez pas besoin de supprimer les bases de données pour procéder à la mise à niveau. Au lieu de cela, vous sélectionnez les bases de données existantes, lesquelles la version précédente du client MBAM a été créée. Le programme d’installation de la mise à niveau MBAM 2.0 effectue ensuite une migration des bases de données existantes vers MBAM 2,0.

**Mise à niveau du client distribué** : Si vous utilisez la topologie MBAM autonome, vous pouvez mettre à niveau les clients MBAM progressivement après l’installation de l’infrastructure du serveur MBAM 2,0. Le serveur MBAM 2,0 détecte la version du client existant et effectue les étapes requises pour effectuer une mise à niveau vers le client 2,0.

Après avoir effectué la mise à niveau de l’infrastructure du serveur MBAM 2,0, les clients MBAM 1,0 continuent de signaler au serveur MBAM 2,0 les données de récupération par confiance, mais la conformité sera basée sur les stratégies de MBAM 1,0. Vous devez mettre à niveau des clients vers MBAM 2,0 pour que les ordinateurs clients signalent de manière précise la conformité par rapport aux stratégies 2,0 MBAM. Vous pouvez mettre à niveau les clients vers le client MBAM 2,0 sans désinstaller le client précédent, et le client doit commencer à appliquer et à signaler les stratégies 2,0 MBAM.

Si vous utilisez MBAM avec Configuration Manager, vous devez mettre à niveau les clients 1,0 MBAM vers MBAM 2,0.

### <a href="" id="mbam-support-for-bitlocker-s-enterprise-scenarios-on-the-windows-8-platform"></a>MBAM prise en charge des scénarios d’entreprise de BitLocker sur la plateforme Windows 8

MBAM prend en charge le système d’exploitation Windows 8 comme plateforme cible pour l’installation du client MBAM. Cette prise en charge permet aux administrateurs informatiques d’installer l’agent MBAM pour chiffrer les lecteurs du système d’exploitation Windows 8 et de signaler la conformité des ordinateurs. MBAM tire parti des logiciels de protection de TPM et de TPM + PIN pour gérer le système d’exploitation Windows 8 comme le système d’exploitation Windows 7. MBAM 2.0 ajoute également la prise en charge du chiffrement des clients Windows to go.

### Ajout du portail libre-service

Les utilisateurs finaux peuvent désormais utiliser le portail libre-service pour récupérer leurs clés de récupération. Le portail libre-service peut être déployé sur un serveur unique à l’aide des autres fonctionnalités de MBAM, ou sur un serveur distinct qui offre aux administrateurs informatiques la possibilité d’exposer le portail libre serveur aux utilisateurs, selon les besoins. Lorsque le portail libre-service authentifie les utilisateurs, les utilisateurs doivent entrer uniquement les huit premiers chiffres de l’ID de clé de récupération pour recevoir leur clé de récupération.

MBAM sécurise également la clé en permettant aux utilisateurs de récupérer des clés uniquement pour les ordinateurs sur lesquels ils sont des utilisateurs, ce qui réduit le risque que d’autres utilisateurs accèdent à des accès non autorisés.

### Possibilité de reprise automatique de la protection BitLocker à partir d’un état suspendu

MBAM ne permet plus aux administrateurs informatiques de conserver BitLocker suspendu et non protégé pour des périodes prolongées. Si un administrateur informatique interrompt BitLocker, MBAM le réactive automatiquement au redémarrage de l’ordinateur, ce qui réduit le risque d’attaque de l’ordinateur.

### Les lecteurs de données fixes peuvent être configurés pour être déverrouillés automatiquement sans mot de passe

Une stratégie de lecteur de données fixe (FDD) peut désormais être configurée pour permettre le déverrouillage automatique du lecteur sans mot de passe. Les utilisateurs ne sont pas invités à entrer un mot de passe pour le chiffrement du FDD, et le FDD est sécurisé et déverrouillé automatiquement avec le lecteur du système d’exploitation.

## <a href="" id="---------mbam-2-0-release-notes"></a> Notes de publication de MBAM 2.0


Pour plus d’informations et pour les actualités de dernière minute qui ne sont pas incluses dans la documentation, voir les [notes de publication pour MBAM 2,0](release-notes-for-mbam-20-mbam-2.md).

## Obtention de MBAM 2.0


Cette technologie fait partie du pack d’optimisation de bureau Microsoft (MDOP). Les clients d’entreprise peuvent obtenir MDOP avec Microsoft Software Assurance. Pour plus d’informations sur l’utilisation de Microsoft Software Assurance et l’acquisition de MDOP, voir [Comment obtenir MDOP?](https://go.microsoft.com/fwlink/p/?LinkId=322049)

## Rubriques connexes


[Prise en main de MBAM2.0](getting-started-with-mbam-20-mbam-2.md)

 

 





