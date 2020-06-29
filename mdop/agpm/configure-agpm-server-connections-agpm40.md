---
title: Configurer les connexions du serveur AGPM
description: Configurer les connexions du serveur AGPM
author: dansimp
ms.assetid: bbbb15e8-35e7-403c-b695-7a6ebeb87839
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9b6b065b9855c6edf44456026baa32e8d9a4674f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807761"
---
# Configurer les connexions du serveur AGPM


Toutes les versions de chaque objet de stratégie de groupe contrôlé (GPO) sont stockées dans une archive centrale de sorte que les administrateurs de stratégie de groupe puissent afficher et modifier les objets de stratégie de groupe hors connexion sans affecter immédiatement la version déployée de chaque GPO.

Un compte d’utilisateur ayant le rôle d’administrateur AGPM (contrôle total), le compte d’utilisateur de l’approbateur qui a créé l’objet de stratégie de groupe utilisé dans ces procédures, ou un compte d’utilisateur disposant des autorisations nécessaires dans Advanced Group Policy Management (AGPM) est requis pour effectuer ces procédures pour la configuration centralisée des emplacements d’archivage de tous les administrateurs de stratégie de groupe Passez en revue les détails dans «autres considérations» dans cette rubrique.

## Configuration des connexions au serveur AGPM


En tant qu’administrateur AGPM, vous pouvez vous assurer que tous les administrateurs de stratégie de groupe se connectent au même serveur AGPM en configurant le paramètre associé de manière centralisée. Si votre environnement nécessite des serveurs AGPM séparés pour tout ou partie des domaines, configurez ces serveurs AGPM supplémentaires en tant qu’exceptions par défaut. Si vous ne configurez pas les connexions serveur AGPM de manière centralisée, chaque administrateur de stratégie de groupe doit configurer manuellement le serveur AGPM pour être affiché pour chaque domaine.

-   [Configurer une connexion de serveur AGPM pour tous les administrateurs de stratégie de groupe](#bkmk-defaultarchiveloc)

-   [Configurer des connexions serveur AGPM supplémentaires pour tous les administrateurs de stratégie de groupe](#bkmk-additionalarchiveloc)

-   [Configurer manuellement une connexion de serveur AGPM pour votre compte](#bkmk-manuallyconfigurearchiveloc)

### <a href="" id="bkmk-defaultarchiveloc"></a>

**Pour configurer une connexion de serveur AGPM pour tous les administrateurs de stratégie de groupe**

1.  Dans l’arborescence de la **console de gestion des stratégies de groupe** , modifiez un objet GPO qui est appliqué à tous les administrateurs de stratégie de groupe. Pour plus d’informations, voir [modification d’un objet de stratégie de groupe](editing-a-gpo-agpm40.md).

2.  Dans la **fenêtre Éditeur de gestion des stratégies de groupe** , cliquez sur **Configuration utilisateur**, **stratégies**, **modèles d’administration**, **composants Windows**et **AGPM**.

3.  Dans le volet Détails, double-cliquez sur **AGPM: spécifiez le serveur AGPM par défaut (tous les domaines)**.

4.  Dans la fenêtre **Propriétés** , activez la case à cocher **activé** , puis entrez le nom et le port complets de l’ordinateur (par exemple, Server.contoso.com:4600).

5.  Cliquez sur **OK**. À moins que vous ne vouliez configurer des connexions de serveur AGPM supplémentaires, fermez la fenêtre **éditeur de gestion des stratégies de groupe** et déployez l’objet de stratégie de groupe. Pour plus d’informations, consultez [la rubrique déploiement d’un objet de stratégie de groupe](deploy-a-gpo-agpm40.md). Lorsque la stratégie de groupe est mise à jour, la connexion au serveur AGPM est configurée pour tous les administrateurs de stratégie de groupe.

### <a href="" id="bkmk-additionalarchiveloc"></a>

**Pour configurer des connexions serveur AGPM supplémentaires pour tous les administrateurs de stratégie de groupe**

1.  Si aucune connexion de serveur AGPM n’a été configurée, suivez la procédure ci-dessus pour configurer un serveur AGPM par défaut pour tous les domaines.

2.  Pour configurer des serveurs AGPM séparés pour tout ou partie des domaines (en remplaçant le serveur AGPM par défaut), dans l’arborescence de la **console de gestion des stratégies de groupe** , modifiez un objet GPO qui est appliqué à tous les administrateurs de stratégie de groupe. Pour plus d’informations, voir [modification d’un objet de stratégie de groupe](editing-a-gpo-agpm40.md).

3.  Dans la fenêtre de l' **éditeur de gestion des stratégies de groupe** , cliquez sur **Configuration utilisateur**, **stratégies**, **modèles d’administration**, **composants Windows**, puis **AGPM**.

4.  Dans le volet Détails, double-cliquez sur **AGPM: spécifier les serveurs AGPM**.

5.  Dans la fenêtre **Propriétés** , activez la case à cocher **activé** , puis cliquez sur **Afficher**.

6.  Dans la fenêtre **afficher les contenus** :

    1.  Cliquez sur **Ajouter**.

    2.  Pour **nom**de la valeur, tapez le nom de domaine (par exemple, server1.contoso.com).

    3.  Pour la **valeur**, tapez le nom du serveur AGPM et le port à utiliser pour ce domaine (par exemple, Server2.contoso.com:4600), puis cliquez sur **OK**. (Par défaut, le service AGPM écoute sur le port 4600. Pour utiliser un autre port, voir [modifier le service AGPM](modify-the-agpm-service-agpm40.md).)

    4.  Répétez cette procédure pour chaque domaine qui n’utilise pas le serveur AGPM par défaut.

7.  Cliquez sur **OK** pour fermer les fenêtres **afficher le contenu** et les **Propriétés** .

8.  Fermez la fenêtre de l' **éditeur de gestion des stratégies de groupe** . Pour plus d’informations, consultez [la rubrique déploiement d’un objet de stratégie de groupe](deploy-a-gpo-agpm40.md). Lorsque la stratégie de groupe est mise à jour, les nouvelles connexions au serveur AGPM sont configurées pour tous les administrateurs de stratégie de groupe.

### <a href="" id="bkmk-manuallyconfigurearchiveloc"></a>

Si vous avez configuré la connexion à un serveur AGPM de manière centralisée, l’option de configuration manuelle n’est pas disponible pour tous les administrateurs de stratégie de groupe.

**Pour configurer manuellement le serveur AGPM à afficher pour votre compte**

1.  Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.

2.  Dans le volet Détails, cliquez sur l’onglet **serveur AGPM** .

3.  Entrez le nom complet de l’ordinateur pour le serveur AGPM qui gère l’archive utilisée pour ce domaine (par exemple, server.contoso.com) et le port sur lequel le service AGPM écoute (par défaut, le port 4600).

4.  Cliquez sur **appliquer**, puis sur **Oui** pour confirmer.

### Autres éléments à prendre en considération

-   Vous devez être en mesure de modifier et de déployer un objet de stratégie de groupe pour pouvoir exécuter les procédures de configuration centralisée des connexions serveur AGPM pour tous les administrateurs de stratégie de groupe. Pour plus d’informations, voir [modification d’un objet de stratégie de groupe](editing-a-gpo-agpm40.md) et [déploiement d’un objet de stratégie de groupe](deploy-a-gpo-agpm40.md)

-   Le serveur AGPM sélectionné détermine les objets de stratégie de groupe qui s’affichent dans l’onglet **Sommaire** et à quel emplacement les paramètres de l’onglet **délégation de domaine** sont appliqués. S’ils ne sont pas gérés de manière centralisée par le biais du modèle d’administration, chaque administrateur de stratégie de groupe doit configurer ce paramètre pour qu’il pointe vers le serveur AGPM du domaine.

-   L’appartenance au groupe de propriétaires de la stratégie de groupe doit être restreinte, soit n’est pas utilisé pour contourner la gestion d’accès d’AGPM aux objets de stratégie de groupe. (Dans la **console de gestion des stratégies de groupe**, cliquez sur **objets de stratégie de groupe** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe, cliquez sur **délégation**, puis configurez les paramètres en fonction des besoins de votre organisation.)

### Références supplémentaires

-   [Configuration de la Gestion avancée des stratégies de groupe](configuring-advanced-group-policy-management-agpm40.md)

 

 





