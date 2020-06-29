---
title: Configurer l'équilibrage de la charge réseau pour MBAM
description: Configurer l'équilibrage de la charge réseau pour MBAM
author: dansimp
ms.assetid: df2208c3-352b-4a48-9722-237b0c8cd6a5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a04bc74a9dab7bfe18eed8e5a3c1b6ca64d88b5b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811201"
---
# Configurer l'équilibrage de la charge réseau pour MBAM


Pour vérifier que vous remplissez les conditions préalables et que la configuration matérielle et logicielle requise pour l’installation de la fonctionnalité d’administration et de surveillance du serveur est satisfaites, consultez la configuration requise pour le [déploiement d’MBAM 1,0](mbam-10-deployment-prerequisites.md) et les [configurations MBAM 1,0 prises en charge](mbam-10-supported-configurations.md).

**Remarques**  Pour obtenir les fichiers journaux d’installation, vous devez installer Microsoft BitLocker administration et la surveillance (MBAM) à l’aide du package **msiexec** et de l’option **/l** &lt; emplacement &gt; . Les fichiers journaux sont créés à l’emplacement que vous spécifiez.

D’autres fichiers journaux d’installation sont créés dans le dossier% Temp% de l’utilisateur qui installe MBAM.

 

Les clusters de l’équilibrage de charge réseau (NLB) pour la fonctionnalité d’administration et de surveillance du serveur offrent une extensibilité dans MBAM et devraient prendre en charge plus de 55 000 ordinateurs client MBAM.

**Remarques**  L’équilibrage de charge réseau de Windows Server répartit les demandes de clients sur un ensemble de serveurs configurés dans un seul cluster de serveur. Lors de l’installation de l’équilibrage de charge réseau sur chacun des serveurs (hôtes) d’un cluster, le cluster présente une adresse IP virtuelle ou un nom de domaine complet (FQDN) aux demandes des clients. Les requêtes du client initial sont dirigées vers tous les hôtes du cluster, mais un seul hôte accepte et gère la requête.

Tous les ordinateurs qui font partie d’un cluster NLB présentent les exigences suivantes:

-   Tous les ordinateurs du cluster NLB doivent se trouver dans le même domaine.

-   Chaque ordinateur du cluster NLB doit utiliser une adresse IP statique.

-   L’équilibrage de charge réseau doit être activé sur chaque ordinateur du cluster NLB.

-   Le cluster NLB nécessite une adresse IP statique, et un enregistrement hôte doit être créé manuellement dans le DNS (Domain Name System).

 

## Configuration de l’équilibrage de charge réseau pour les serveurs d’administration et de surveillance de MBAM


Les étapes suivantes expliquent comment configurer un nom virtuel de cluster NLB et une adresse IP pour deux serveurs d’administration et de surveillance de MBAM, et comment configurer des clients MBAM pour utiliser le cluster NLB.

Avant de commencer les procédures décrites dans cette rubrique, vous devez disposer de la fonctionnalité de serveur d’administration et de surveillance de MBAM à l’aide de la même liaison de port IIS sur deux ordinateurs serveur distincts qui répondent à la configuration requise pour l’installation de la fonctionnalité MBAM Server et la configuration du cluster NLB.

**Remarques**  Cette rubrique décrit la procédure de base d’utilisation du gestionnaire de l’équilibrage de charge réseau pour créer un cluster NLB. Les étapes exactes de configuration d’un serveur Windows dans le cadre d’un cluster NLB dépendent de la version de Windows Server utilisée. Pour plus d’informations sur la création d’NLBs sur WindowsServer2008, voir [création de clusters d’équilibrage de charge réseau](https://go.microsoft.com/fwlink/?LinkId=197176) dans la bibliothèque TechNet de Windows Server 2008.

 

**Pour configurer le nom virtuel et l’adresse IP d’un cluster NLB pour deux serveurs d’administration et de surveillance MBAM**

1.  Cliquez sur **Démarrer**, sur **tous les programmes**, sur **Outils d’administration**, puis sur gestionnaire d’équilibrage de la **charge réseau**.

    **Remarques**  Si le gestionnaire de NLB n’est pas présent, vous pouvez l’installer en tant que fonctionnalité de WindowsServer2003. Vous devez installer cette fonctionnalité sur les serveurs d’administration et de surveillance MBAM si vous souhaitez la configurer dans le cluster NLB.

     

2.  Dans la barre de menus, cliquez sur **cluster**, puis cliquez sur **nouveau** pour ouvrir la boîte de dialogue **paramètres du cluster** .

3.  Dans la boîte de dialogue **paramètres du cluster** , entrez les informations relatives à la configuration IP du cluster NLB:

    -   **Adresse IP:** Adresse IP du cluster NLB enregistrée dans DNS

    -   **Masque de sous-réseau:** Masque de sous-réseau d’adresse IP du cluster NLB inscrit dans DNS

    -   **Nom Internet complet:** Nom de domaine complet du nom de cluster NLB inscrit dans DNS

4.  Assurez-vous que la case à **cocast** est activée en **mode de fonctionnement du cluster**, puis cliquez sur **suivant**.

5.  Dans la page **adresses IP de cluster** , cliquez sur **suivant**.

6.  Dans la page **règles de port** , cliquez sur **modifier** pour définir les ports auxquels le cluster NLB répondra et configurer les ports utilisés pour la communication du système client à site dès qu’ils sont définis pour le site, ou cliquez sur **suivant** pour activer l’adresse IP du cluster NLB pour répondre à tous les ports TCP/IP.

    **Remarques**  Assurez-vous que l' **affinité** est définie sur **Single**.

     

7.  Dans la page **connexion** , entrez le nom d’hôte de l’instance du serveur d’administration MBAM et de surveillance qui fera partie du cluster NLB dans l' **hôte**, puis cliquez sur **se connecter**.

8.  Dans **interfaces disponibles pour la configuration d’un nouveau cluster**, sélectionnez l’interface réseau qui sera configurée pour répondre aux communications de cluster NLB, puis cliquez sur **suivant**.

9.  Dans la page **paramètres d’hôte** , passez en revue les informations affichées pour vous assurer que les paramètres de **configuration IP dédiée** affichent la configuration IP d’hôte dédiée pour l’hôte de cluster NLB approprié, vérifiez que l' **État par défaut** de l’état d’accueil initial est **démarré**, puis cliquez sur **Terminer**.

    **Remarques**  La page des **paramètres d’hôte** affiche également la priorité de l’hôte de cluster NLB, qui est de 1 à 32. À mesure que de nouveaux hôtes sont ajoutés au cluster NLB, la priorité de l’hôte doit être différente de celle des hôtes précédemment ajoutés. La priorité est automatiquement incrémentée lorsque vous utilisez le gestionnaire d’équilibrage de la charge réseau.

     

10. Cliquez sur ** &lt; nom &gt; du cluster NLB** et assurez-vous que l' **État** de l’interface du serveur NLB est **convergent** avant de continuer. Il est possible que vous n’ayez pas besoin d’actualiser l’affichage du cluster NLB en tant que configuration TCP/IP de l’hôte qui est modifiée par le gestionnaire NLB.

11. Pour ajouter d’autres hôtes au cluster NLB, cliquez avec le bouton droit sur ** &lt; nom &gt; du cluster NLB**, cliquez sur **Ajouter un hôte au cluster,** puis répétez les étapes 7 à 10 pour chaque système de site qui fera partie du cluster NLB.

12. Sur un ordinateur sur lequel le modèle de stratégie de groupe MBAM est installé, modifiez les paramètres de stratégie de groupe MBAM pour configurer les points de terminaison MBAM services de manière à utiliser le nom du cluster NLB et la liaison de port IIS appropriée pour accéder aux fonctionnalités d’administration et de contrôle du serveur MBAM qui sont installées sur les ordinateurs de cluster NLB. Pour plus d’informations sur la modification des paramètres de l’objet de stratégie de MBAM, voir [Comment modifier les paramètres de l’objet de stratégie de groupe MBAM 1,0](how-to-edit-mbam-10-gpo-settings.md). Si les serveurs d’administration et de surveillance de MBAM sont nouveaux dans votre environnement, assurez-vous que les appartenances au groupe de sécurité local requises ont été configurées correctement. Pour plus d’informations sur la configuration requise des groupes de sécurité, voir [planification de rôles d’administrateur MBAM 1,0](planning-for-mbam-10-administrator-roles.md).

13. À la fin de la configuration du cluster NLB, il est recommandé de valider le fonctionnement de l’administration MBAM et de l’analyse du cluster NLB. Pour ce faire, ouvrez un navigateur Web sur un ordinateur autre que celui qui est configuré dans le protocole NLB et assurez-vous que vous pouvez accéder au site Web d’administration et de surveillance de MBAM à l’aide du nom de domaine complet NLB.

## Rubriques connexes


[Déploiement de l'infrastructure de serveur MBAM1.0](deploying-the-mbam-10-server-infrastructure.md)

 

 





