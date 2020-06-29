---
title: Configurer la connexion au serveur AGPM
description: Configurer la connexion au serveur AGPM
author: dansimp
ms.assetid: 9a42b5bc-41be-44ef-a6e2-6f56e2cf1996
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 88182f0e79f1a8bcce53e0d50c014e8d4aa29286
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807697"
---
# Configurer la connexion au serveur AGPM


La gestion avancée de la stratégie de groupe stocke toutes les versions de chaque objet de stratégie de groupe contrôlé (GPO) dans une archive centrale, de sorte que les administrateurs de stratégie de groupe peuvent afficher et modifier les objets de stratégie de groupe hors connexion sans avoir d’impact sur la version déployée de chaque GPO.

Un compte d’utilisateur ayant le rôle d’administrateur AGPM (contrôle total), le compte d’utilisateur de l’approbateur qui a créé l’objet de stratégie de groupe utilisé dans ces procédures, ou un compte d’utilisateur disposant des autorisations nécessaires dans la gestion avancée de la stratégie de groupe est requis pour effectuer ces procédures pour la configuration centralisée des emplacements d’archivage de tous les administrateurs Passez en revue les détails dans «autres considérations» dans cette rubrique.

## Configuration de la connexion au serveur AGPM


En tant qu’administrateur AGPM (contrôle total), vous pouvez vous assurer que tous les administrateurs de stratégie de groupe se connectent au même serveur AGPM en configurant le paramètre de manière centralisée. Si votre environnement nécessite des serveurs AGPM séparés pour tout ou partie des domaines, configurez ces serveurs AGPM supplémentaires en tant qu’exceptions par défaut. Si vous ne configurez pas les connexions serveur AGPM de manière centralisée, chaque administrateur de stratégie de groupe doit configurer manuellement le serveur AGPM pour être affiché pour chaque domaine.

-   [Configurer un serveur AGPM pour tous les administrateurs de stratégie de groupe](#bkmk-defaultarchiveloc)

-   [Configurer des serveurs AGPM supplémentaires pour tous les administrateurs de stratégie de groupe](#bkmk-additionalarchiveloc)

-   [Configurer manuellement un serveur AGPM pour votre compte](#bkmk-manuallyconfigurearchiveloc)

### <a href="" id="bkmk-defaultarchiveloc"></a>

**Pour configurer un serveur AGPM pour tous les administrateurs de stratégie de groupe**

1.  Dans l’arborescence de la **console de gestion des stratégies de groupe** , modifiez un objet GPO qui est appliqué à tous les administrateurs de stratégie de groupe. Pour plus d’informations, voir [modification d’un objet de stratégie de groupe](editing-a-gpo.md).

2.  Dans l' **éditeur d’objets de stratégie de groupe**, cliquez sur **Configuration utilisateur**, **modèles d’administration**et **composants Windows**.

3.  Si **AGPM** ne figure pas dans la liste **composants Windows**:

    1.  Cliquez avec le bouton droit sur **modèles d’administration** et sélectionnez **Ajouter/supprimer des modèles**.

    2.  Cliquez **sur Ajouter**, sélectionnez **AGPM. admx** ou **AGPM. adm**, cliquez sur **ouvrir**, puis sur **Fermer**.

4.  Sous **composants Windows**, double-cliquez sur **AGPM**.

5.  Dans le volet Détails, double-cliquez sur le **serveur AGPM (tous les domaines)**.

6.  Dans la fenêtre de **Propriétés de serveur AGPM (All domains)** , activez la case à cocher **activé** , puis entrez le nom de l’ordinateur et le port complet (par exemple, Server.contoso.com:4600).

7.  Cliquez sur **OK**. À moins que vous ne vouliez configurer des connexions de serveur AGPM supplémentaires, fermez l' **éditeur d’objets de stratégie de groupe** et déployez l’objet de stratégie de groupe. Pour plus d’informations, consultez [la rubrique déploiement d’un objet de stratégie de groupe](deploy-a-gpo.md). Lorsque la stratégie de groupe est mise à jour, la connexion au serveur AGPM est configurée pour tous les administrateurs de stratégie de groupe.

### <a href="" id="bkmk-additionalarchiveloc"></a>

**Pour configurer des serveurs AGPM supplémentaires pour tous les administrateurs de stratégie de groupe**

1.  Si aucune connexion de serveur AGPM n’a été configurée, suivez la procédure ci-dessus pour configurer un serveur AGPM par défaut pour tous les domaines.

2.  Pour configurer des serveurs AGPM séparés pour tout ou partie des domaines (en remplaçant le serveur AGPM par défaut), dans l’arborescence de la **console de gestion des stratégies de groupe** , modifiez un objet GPO qui est appliqué à tous les administrateurs de stratégie de groupe. Pour plus d’informations, voir [modification d’un objet de stratégie de groupe](editing-a-gpo.md).

3.  Sous **Configuration utilisateur** dans l' **éditeur d’objets de stratégie de groupe**, double-cliquez sur **modèles d’administration**, **composants Windows**, puis sur **AGPM**.

4.  Dans le volet Détails, double-cliquez sur le **serveur AGPM**.

5.  Dans la fenêtre **Propriétés de serveur AGPM** , activez la case à cocher **activé** , puis cliquez sur **Afficher**.

6.  Dans la fenêtre **afficher les contenus** :

    1.  Cliquez sur **Ajouter**.

    2.  Pour **nom**de la valeur, tapez le nom de domaine (par exemple, server1.contoso.com).

    3.  Pour la **valeur**, tapez le nom du serveur AGPM et le port à utiliser pour ce domaine (par exemple, Server2.contoso.com:4600), puis cliquez sur **OK**. (Par défaut, le service AGPM écoute sur le port 4600. Pour utiliser un autre port, voir [modifier le port sur lequel écoute le service AGPM](modify-the-port-on-which-the-agpm-service-listens.md).)

    4.  Répétez cette procédure pour chaque domaine qui n’utilise pas le serveur AGPM par défaut.

7.  Cliquez sur **OK** pour fermer les fenêtres **afficher le contenu** et les propriétés du **serveur AGPM** .

8.  Fermez l' **éditeur d’objets de stratégie de groupe**. Pour plus d’informations, consultez [la rubrique déploiement d’un objet de stratégie de groupe](deploy-a-gpo.md). Lorsque la stratégie de groupe est mise à jour, les nouvelles connexions au serveur AGPM sont configurées pour tous les administrateurs de stratégie de groupe.

### <a href="" id="bkmk-manuallyconfigurearchiveloc"></a>

Si vous avez configuré la connexion à un serveur AGPM de manière centralisée, l’option d’accès manuel n’est pas disponible pour tous les administrateurs de stratégie de groupe.

**Pour configurer manuellement le serveur AGPM de sorte qu’il s’affiche pour votre compte**

1.  Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.

2.  Dans le volet Détails, cliquez sur l’onglet **serveur AGPM** .

3.  Entrez le nom complet de l’ordinateur pour le serveur AGPM qui gère l’archive utilisée pour ce domaine (par exemple, server.contoso.com) et le port sur lequel le service AGPM écoute (par défaut, le port 4600).

4.  Cliquez sur **appliquer**, puis sur **Oui** pour confirmer.

### Autres éléments à prendre en considération

-   Vous devez être en mesure de modifier et de déployer un objet de stratégie de groupe pour pouvoir exécuter les procédures de configuration centralisée des connexions serveur AGPM pour tous les administrateurs de stratégie de groupe. Pour plus d’informations, voir [modification d’un objet de stratégie de groupe](editing-a-gpo.md) et [déploiement d’un objet de stratégie de groupe](deploy-a-gpo.md)

-   Le serveur AGPM sélectionné détermine les objets de stratégie de groupe qui s’affichent sous l’onglet **contenu** , ainsi que l’emplacement dans lequel les paramètres de l’onglet **délégation de domaine** sont appliqués. S’ils ne sont pas gérés de manière centralisée par le biais du modèle d’administration, chaque administrateur de stratégie de groupe doit configurer ce paramètre pour qu’il pointe vers le serveur AGPM du domaine.

-   L’appartenance au groupe de propriétaires de la stratégie de groupe doit être restreinte afin qu’elle ne soit pas utilisée pour contourner la gestion de l’accès aux objets de stratégie de groupe par AGPM. (Dans la **console de gestion des stratégies de groupe**, cliquez sur **objets de stratégie de groupe** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe, cliquez sur **délégation**, puis configurez les paramètres en fonction des besoins de votre organisation.)

### Références supplémentaires

-   [Exécution de tâches d'administrateur AGPM](performing-agpm-administrator-tasks.md)

 

 





