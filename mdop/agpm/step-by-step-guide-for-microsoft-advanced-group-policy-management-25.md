---
title: Guide pas à pas de la Gestion avancée des stratégies de groupe Microsoft2.5
description: Guide pas à pas de la Gestion avancée des stratégies de groupe Microsoft2.5
author: dansimp
ms.assetid: 454298c9-0fab-497a-9808-c0246a4c8db5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 67925e417e4fb1f5398dfd030f366936f1d36909
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808209"
---
# Guide pas à pas de la Gestion avancée des stratégies de groupe Microsoft2.5


Ce guide pas à pas décrit les techniques avancées de gestion des stratégies de groupe à l’aide de la console de gestion des stratégies de groupe (GPMC) et de la gestion de la stratégie de groupe Microsoft avancée (AGPM). AGPM augmente les capacités de la console de gestion des stratégies de GPMC et fournit les éléments suivants:

-   Rôles standard pour la délégation d’autorisations pour gérer des objets de stratégie de groupe pour plusieurs administrateurs de stratégie de groupe.

-   Archive permettant aux administrateurs de stratégie de groupe de créer et de modifier des objets de stratégie de groupe hors ligne avant de les déployer dans un environnement de production.

-   La possibilité de revenir à une version précédente d’un objet de stratégie de groupe.

-   La fonctionnalité d’archivage/extraction pour les objets de stratégie de groupe permet de s’assurer que les administrateurs de stratégie de groupe n’écrasent pas par inadvertance les tâches d’un autre groupe.

## Vue d’ensemble du scénario AGPM


Pour ce scénario, vous allez utiliser un compte d’utilisateur distinct pour chaque rôle dans AGPM et montrer comment la stratégie de groupe peut être gérée dans un environnement doté de plusieurs administrateurs de stratégie de groupe disposant de différents niveaux d’autorisation. Plus précisément, vous devez effectuer les tâches suivantes:

-   À l’aide d’un compte membre du groupe administrateurs de domaine, installez le serveur AGPM et attribuez le rôle d’administrateur AGPM à un compte ou à un groupe.

-   À l’aide des comptes auxquels vous allez attribuer des rôles AGPM, installez le client AGPM.

-   À l’aide d’un compte ayant le rôle d’administrateur AGPM, configurez l’accès AGPM et déléguez aux objets de stratégie de groupe en attribuant des rôles à d’autres comptes.

-   En utilisant un compte doté du rôle d’éditeur, demandez la création d’un objet de stratégie de groupe, que vous approuvez ensuite en utilisant un compte doté du rôle Approbateur. Avec le compte de l’éditeur, recherchez l’objet de stratégie de groupe à partir de l’archive, modifiez-le, puis consultez l’objet de stratégie de groupe dans l’archive et demandez le déploiement.

-   En utilisant un compte doté du rôle Approbateur, passez en revue l’objet de stratégie de groupe et déployez-le dans votre environnement de production.

-   À l’aide d’un compte avec le rôle d’éditeur, créez un modèle d’objet de stratégie de groupe et utilisez-le comme point de départ pour créer un nouvel objet de stratégie de groupe.

-   En utilisant un compte doté du rôle Approbateur, supprimez et restaurez un objet de stratégie de groupe.

![processus de développement d’objets de stratégie de groupe](images/ab77a1f3-f430-4e7d-be58-ee8f9bd1140e.gif)

## Configuration requise


Les ordinateurs sur lesquels vous souhaitez installer AGPM doivent respecter les exigences suivantes et vous devez créer des comptes à utiliser dans ce scénario.

### Configuration requise pour le serveur AGPM

Le serveur AGPM Server 2.5 nécessite Vista® (version 32 bits) sans Service Pack ou Windows Server® 2003 (32 bits), ainsi que la console de gestion des stratégies de GPMC. Par ailleurs, vous devez être membre du groupe Domain Admins pour installer le serveur AGPM.

Vous devez installer le serveur AGPM sur un serveur membre ou un contrôleur de domaine avec la version la plus récente de GPMC qui est disponible pour vous et pris en charge par AGPM. AGPM utilise la console GPMC pour sauvegarder et restaurer des objets de stratégie de groupe, et les versions plus récentes de la console GPMC fournissent des paramètres de stratégie supplémentaires qui ne sont pas disponibles dans les versions précédentes. Si la version de GPMC sur votre serveur AGPM est antérieure à la version sur les ordinateurs utilisés par les administrateurs pour gérer la stratégie de groupe, le serveur AGPM ne sera pas en mesure de stocker ces paramètres de stratégie qui ne sont pas disponibles dans l’ancienne version de GPMC.

Plus précisément, si votre serveur AGPM exécute Windows Server2003 et la version de la console de gestion des stratégies de groupe qui l’accompagnent et que les ordinateurs de l’administrateur de la stratégie de groupe exécutent Vista et la version de la console de gestion des stratégies de groupe, vous pouvez toujours gérer la plupart des paramètres de stratégie. Toutefois, les paramètres de stratégie de la console GPMC dans Windows Vista qui ne sont pas disponibles dans la console GPMC de Windows Server 2003, tels que ceux liés à la redirection de dossiers, au réseau sans fil (IEEE 802,11) et aux imprimantes déployées, ne peuvent pas être stockés par le serveur AGPM, même si les administrateurs peuvent les configurer à l’aide d’AGPM sur leur ordinateur.

Si vous devez installer le serveur AGPM sur un ordinateur doté d’une version plus ancienne de GPMC que les administrateurs de stratégie de groupe en cours d’exécution, voir les informations de référence des paramètres de stratégie de groupe pour plus d’informations sur les paramètres de stratégie disponibles pour les systèmes d’exploitation. Pour télécharger la référence des paramètres de stratégie de groupe, reportez-vous à la section <https://go.microsoft.com/fwlink/?LinkID=106147> .

**Remarques**  Les archives ne peuvent pas être déplacées à partir d’un serveur AGPM ou d’un serveur GPOVault exécutant Windows Server2003 vers un serveur AGPM exécutant Vista.

Pour Windows Server2003, si GPOVault Server est installé sur l’ordinateur sur lequel vous voulez installer le serveur AGPM, il est recommandé de ne pas désinstaller GPOVault Server avant de commencer l’installation. L’installation d’AGPM Server désinstallera GPOVault Server et transférera automatiquement vos données d’archive GPOVault existantes vers une archive AGPM.

 

### Configuration requise pour le client AGPM

Le client AGPM est requis pour Vista (version 32 bits) sans Service Pack ou Windows Server2003 (version 32 bits), ainsi que la console GPMC. Le client AGPM peut être installé sur un ordinateur exécutant AGPM Server.

### Exigences de scénarios

Avant de commencer ce scénario, vous devez créer quatre comptes d’utilisateurs. Pendant le scénario, vous devez attribuer l’un des rôles AGPM suivants à chacun de ces comptes: Administrateur AGPM (contrôle total), approbateur, éditeur et relecteur. Ces comptes doivent être en mesure d’envoyer et de recevoir des messages électroniques. Attribution d’autorisations d’accès aux **objets liés** aux comptes avec l’administrateur d’AGPM, l’approbateur et (facultatif) des rôles d’éditeur.

**Remarques** 
 L’autorisation **lier les objets de stratégie de groupe** est affectée par défaut aux membres des administrateurs de domaine et des administrateurs d’entreprise. Pour affecter **des** autorisations d’accès de l’utilisateur à des groupes ou des utilisateurs supplémentaires (par exemple, des comptes ayant le rôle d’administrateur ou d’approbation AGPM), cliquez sur le nœud du domaine, puis cliquez sur l’onglet **délégation** , sélectionnez **lier les objets de stratégie de groupe**, cliquez sur **Ajouter**, et sélectionnez des utilisateurs ou des groupes auxquels vous voulez accorder l’autorisation.

 

Pour ce scénario, vous devez effectuer des actions avec différents comptes. Vous pouvez vous connecter avec chaque compte comme indiqué, ou utiliser la commande **exécuter en tant que** pour démarrer la console de gestion des stratégies de gestion des stratégies avec le compte indiqué.

**Remarques**  Pour utiliser la commande **exécuter en tant que** avec la console GPMC sur Windows Server2003, cliquez sur **Démarrer**, pointez sur **Outils d’administration**, cliquez avec le bouton droit sur **gestion des stratégies de groupe**, puis cliquez sur **exécuter en tant que**. Cliquez sur **l’utilisateur suivant** et entrez les informations d’identification d’un compte.

Pour utiliser la commande **exécuter en tant que** avec la console GPMC sur Windows Vista, cliquez sur le bouton **Démarrer** , pointez sur **exécuter**, puis tapez **runas/user:** <em> DomainName\\UserName </em> **"mmc%windir%\\system32\\gpmc.msc"**, puis cliquez sur **OK**. Lorsque vous y êtes invité, entrez le mot de passe du compte.

 

## Procédures d’installation et de configuration d’AGPM


Pour installer et configurer AGPM, vous devez procéder comme suit.

[Étape 1: installer le serveur AGPM](#bkmk-config1)

[Étape 2: installer le client AGPM](#bkmk-config2)

[Étape 3: configurer une connexion de serveur AGPM](#bkmk-config3)

[Étape 4: configurer les notifications par courrier électronique](#bkmk-config4)

[Étape 5: accès délégué](#bkmk-config5)

### <a href="" id="bkmk-config1"></a>Étape 1: installer le serveur AGPM

Dans cette étape, vous installez le serveur AGPM sur le serveur membre ou le contrôleur de domaine qui exécute le service AGPM et vous configurez l’archive. Toutes les opérations AGPM sont gérées par le biais de ce service Windows et sont exécutées avec les informations d’identification du service. L’archive gérée par un serveur AGPM peut être hébergée sur ce serveur ou sur un autre serveur dans la même forêt.

**Pour installer le serveur AGPM sur l’ordinateur qui hébergera le service AGPM**

1.  Ouvrez une session avec un compte membre du groupe administrateurs de domaine.

2.  Démarrez le CD-ROM Microsoft Desktop Optimization Pack et suivez les instructions qui s’affichent à l’écran pour sélectionner **Advanced Group Management Policy-Server**.

3.  Dans la boîte de dialogue **Bienvenue** , cliquez sur **suivant**.

4.  Dans la boîte de dialogue **termes du contrat de licence logiciel Microsoft** , acceptez les termes du contrat de licence logiciel Microsoft, puis cliquez sur **suivant**.

5.  Dans la boîte de dialogue Path de l' **application** , sélectionnez un emplacement pour installer le serveur AGPM. L’ordinateur sur lequel le serveur AGPM est installé doit héberger le service AGPM et gérer l’archive. Cliquez sur **Suivant**.

6.  Dans la boîte de dialogue **path Archive** , sélectionnez un emplacement pour l’archivage relatif au serveur AGPM. Le chemin d’accès d’archive peut pointer vers un dossier sur le serveur AGPM ou un autre emplacement, mais vous devez sélectionner un emplacement dont l’espace disponible est suffisant pour stocker tous les objets de stratégie de groupe et les données d’historique gérés par ce serveur AGPM. Cliquez sur **Suivant**.

7.  Dans la boîte de dialogue **compte de service AGPM** , sélectionnez un compte de service sous lequel le service AGPM sera exécuté, puis cliquez sur **suivant**.

8.  Dans la boîte de dialogue **Archiver le propriétaire** , sélectionnez le compte ou le groupe auquel attribuer le rôle d’administrateur AGPM (contrôle total). Cet administrateur AGPM peut attribuer des rôles et autorisations d’AGPM aux autres administrateurs de stratégie de groupe (y compris le rôle d’administrateur AGPM). Pour ce scénario, sélectionnez le compte que vous voulez faire dans le rôle administrateur d’AGPM. Cliquez sur **Suivant**.

9.  Cliquez sur **installer**, puis cliquez sur **Terminer** pour quitter l’Assistant installation.

    **Attention**  Ne modifiez pas les paramètres du service AGPM via les outils et **services** **d’administration** du système d’exploitation. Cela peut empêcher le démarrage du service AGPM. Pour plus d’informations sur la modification des paramètres du service, voir aide pour la gestion avancée des stratégies de groupe.

     

### <a href="" id="bkmk-config2"></a>Étape 2: installer le client AGPM

Chaque administrateur de stratégie de groupe (qui crée, modifie, déploie, révise ou supprime des objets de stratégie de groupe) doit disposer d’un client AGPM sur les ordinateurs qu’il utilise pour gérer les objets de stratégie de groupe. Pour ce scénario, vous installez le client AGPM sur au moins un ordinateur. Vous n’avez pas besoin d’installer le client AGPM sur les ordinateurs des utilisateurs finaux qui n’effectuent pas d’administration de la stratégie de groupe.

**Pour installer le client AGPM sur l’ordinateur d’un administrateur de stratégie de groupe**

1.  Démarrez le CD-ROM Microsoft Desktop Optimization Pack et suivez les instructions à l’écran pour sélectionner **Advanced Group Management Policy-client**.

2.  Dans la boîte de dialogue **Bienvenue** , cliquez sur **suivant**.

3.  Dans la boîte de dialogue **termes du contrat de licence logiciel Microsoft** , acceptez les termes du contrat de licence logiciel Microsoft, puis cliquez sur **suivant**.

4.  Dans la boîte de dialogue Path de l' **application** , sélectionnez un emplacement pour installer le client AGPM. Cliquez sur **Suivant**.

5.  Dans la boîte de dialogue **serveur AGPM** , tapez le nom complet de l’ordinateur et le port du serveur AGPM auquel vous voulez vous connecter. Le port par défaut du service AGPM est 4600. Cliquez sur **Suivant**.

6.  Cliquez sur **installer**, puis cliquez sur **Terminer** pour quitter l’Assistant installation.

### <a href="" id="bkmk-config3"></a>Étape 3: configurer une connexion de serveur AGPM

AGPM stocke toutes les versions de chaque objet de stratégie de groupe contrôlé (GPO), c’est-à-dire un objet de stratégie de groupe pour lequel AGPM fournit le contrôle des modifications, dans une archive centrale, de sorte que les administrateurs de stratégie de groupe puissent afficher et modifier les objets de stratégie de groupe hors connexion sans avoir d’impact sur la version déployée de chaque GPO.

Dans cette étape, vous configurez une connexion de serveur AGPM et assurez-vous que tous les administrateurs de stratégie de groupe se connectent au même serveur AGPM. (Pour plus d’informations sur la configuration de plusieurs serveurs AGPM, voir aide pour la gestion avancée des stratégies de groupe.)

**Pour configurer une connexion de serveur AGPM pour tous les administrateurs de stratégie de groupe**

1.  Sur un ordinateur sur lequel vous avez installé un client AGPM, connectez-vous à l’aide du compte d’utilisateur que vous avez sélectionné comme propriétaire d’archive. Cet utilisateur a le rôle d’administrateur AGPM (contrôle total).

2.  Cliquez sur **Démarrer**, pointez sur **Outils d’administration**, puis cliquez sur **gestion des stratégies de groupe** pour ouvrir la console de gestion des stratégies de **groupe (GPMC)**.

3.  Dans l’arborescence de la **console de gestion des stratégies de groupe** , modifiez un objet GPO qui est appliqué à tous les administrateurs de stratégie de groupe.

4.  Dans la fenêtre de l' **éditeur d’objets de stratégie de groupe** , cliquez sur **Configuration utilisateur**, **modèles d’administration**et **composants Windows**.

5.  Si **AGPM** ne figure pas dans la liste **composants Windows**:

    1.  Cliquez avec le bouton droit sur **modèles d’administration** et sélectionnez **Ajouter/supprimer des modèles**.

    2.  Cliquez **sur Ajouter**, sélectionnez **AGPM. admx** ou **AGPM. adm**, cliquez sur **ouvrir**, puis sur **Fermer**.

6.  Sous **composants Windows**, double-cliquez sur **AGPM**.

7.  Dans le volet Détails, double-cliquez sur le **serveur AGPM (tous les domaines)**.

8.  Dans la fenêtre de **Propriétés de serveur AGPM (toutes les domaines)** , sélectionnez **activé** , puis entrez le nom et le port complets de l’ordinateur (par exemple, Server.contoso.com:4600) pour le serveur hébergeant l’archive. Le port utilisé par le service AGPM est le port 4600.

9.  Cliquez sur **OK**, puis fermez la fenêtre **éditeur d’objets de stratégie de groupe** . Lorsque la stratégie de groupe est mise à jour, la connexion au serveur AGPM est configurée pour chaque administrateur de stratégie de groupe.

### <a href="" id="bkmk-config4"></a>Étape 4: configurer les notifications par courrier électronique

En tant qu’administrateur AGPM (contrôle total), vous désignez les adresses de courrier des approbateurs et des administrateurs AGPM auxquels un message électronique contenant une demande est envoyé lorsqu’un éditeur tente de créer, de déployer ou de supprimer un objet de stratégie de groupe. Vous déterminez également l’alias à partir duquel ces messages sont envoyés.

**Pour configurer les notifications par courrier électronique pour AGPM**

1.  Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.

2.  Dans le volet Détails, cliquez sur l’onglet **délégation de domaine** .

3.  Dans le champ **de** , tapez l’alias de messagerie pour AGPM à partir duquel envoyer les notifications.

4.  Dans le champ **à** , tapez l’adresse de courrier du compte d’utilisateur auquel vous souhaitez attribuer le rôle d’approbateur.

5.  Dans le champ **serveur SMTP** , tapez un serveur de messagerie SMTP valide.

6.  Dans les champs **nom d’utilisateur** et **mot de passe** , tapez les informations d’identification d’un utilisateur ayant accès au service SMTP.

7.  Cliquez sur **Apply** (Appliquer).

### <a href="" id="bkmk-config5"></a>Étape 5: accès délégué

En tant qu’administrateur AGPM (contrôle total), vous déléguez l’accès au niveau du domaine aux objets de stratégie de groupe, en attribuant des rôles au compte de chaque administrateur de stratégie de groupe.

**Remarques**  Vous pouvez également déléguer l’accès au niveau de l’objet GPO plutôt qu’au niveau du domaine. Pour plus d’informations, consultez aide pour la gestion avancée des stratégies de groupe.

 

**Important**  Nous vous conseillons de limiter l’appartenance au groupe de propriétaires de la stratégie de groupe, afin qu’il ne puisse pas être utilisé pour contourner la gestion d’AGPM d’Access aux objets de stratégie de groupe. (Dans la **console de gestion des stratégies de groupe**, cliquez sur **objets de stratégie de groupe** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe, cliquez sur **délégation**, puis configurez les paramètres en fonction des besoins de votre organisation.)

 

**Pour déléguer l’accès à tous les objets de stratégie de groupe dans un domaine**

1.  Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.

2.  Dans l’onglet **délégation de domaine** , cliquez sur le bouton **avancé** .

3.  Dans la boîte de dialogue **autorisations** :

    1.  Cliquez sur le compte d’utilisateur d’un administrateur de stratégie de groupe, puis activez la case à cocher **approbateur** pour attribuer ce rôle au compte. Désactivez la case à cocher **éditeur** . (Ce rôle inclut le rôle de réviseur.)

    2.  Cliquez sur le compte d’utilisateur d’un autre administrateur de stratégie de groupe, puis activez la case à cocher **éditeur** pour attribuer ce rôle au compte. (Ce rôle inclut le rôle de réviseur.)

    3.  Cliquez sur un troisième compte, puis activez la case à cocher **relecteur** pour affecter uniquement le rôle de réviseur au compte de l’administrateur de la stratégie de groupe. Désactivez la case à cocher **éditeur** .

    4.  Cliquez sur le bouton **avancé** .

4.  Dans la boîte de dialogue **paramètres de sécurité avancés** :

    1.  Sélectionnez un administrateur de stratégie de groupe, puis cliquez sur **modifier**.

    2.  Pour **appliquer**à, sélectionnez **cet objet et les objets imbriqués**, puis cliquez sur **OK** dans la boîte de dialogue **entrée** d' **autorisation** .

    3.  Répétez l’opération pour chaque administrateur de la stratégie de groupe.

5.  Dans la boîte de dialogue **paramètres de sécurité avancés** , cliquez sur **OK**.

6.  Dans la boîte de dialogue **autorisations** , cliquez sur **OK**.

## Procédure de gestion des objets de stratégie de groupe


Vous devez effectuer les étapes suivantes pour créer, modifier, réviser et déployer des objets de stratégie de groupe à l’aide d’AGPM. Par ailleurs, vous allez créer un modèle, supprimer un objet de stratégie de groupe, puis restaurer un objet GPO supprimé.

[Étape 1: créer un objet de stratégie de groupe](#bkmk-manage1)

[Étape 2: modifier un objet de stratégie de groupe](#bkmk-manage2)

[Étape 3: vérifier et déployer un objet de stratégie de groupe](#bkmk-manage3)

[Étape 4: utiliser un modèle pour créer un objet de stratégie de groupe](#bkmk-manage4)

[Étape 5: supprimer et restaurer un objet de stratégie de groupe](#bkmk-manage5)

### <a href="" id="bkmk-manage1"></a>Étape 1: créer un objet de stratégie de groupe

Dans un environnement doté de plusieurs administrateurs de stratégie de groupe, les utilisateurs dotés du rôle d’éditeur peuvent demander la création de nouveaux objets de stratégie de groupe, mais une telle demande doit être approuvée par une personne ayant le rôle d’approbateur, car la création d’un nouvel objet GPO a un impact sur l’environnement de production.

Dans cette étape, vous utiliserez un compte avec le rôle d’éditeur pour demander la création d’un nouvel objet de stratégie de groupe. En utilisant un compte doté du rôle Approbateur, vous approuvez cette demande et terminerez la création d’un objet de stratégie de groupe.

**Pour demander la création d’un nouvel objet de stratégie de groupe géré via AGPM**

1.  Sur un ordinateur sur lequel vous avez installé un client AGPM, connectez-vous avec un compte d’utilisateur auquel le rôle d’éditeur a été attribué dans AGPM.

2.  Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.

3.  Cliquez avec le bouton droit sur le nœud de **contrôle de modification** , puis cliquez sur **nouvel objet de stratégie de**contrôle.

4.  Dans la boîte de dialogue **nouvel objet GPO contrôlé** :

    1.  Pour recevoir une copie de la demande, tapez votre adresse de messagerie dans le champ **CC** .

    2.  Tapez **MyGPO** comme nom du nouvel objet de stratégie de groupe.

    3.  Tapez un commentaire pour le nouvel objet de stratégie de groupe.

    4.  Cliquez sur **créer Live** pour que le nouvel objet GPO soit déployé sur l’environnement de production immédiatement après approbation.

    5.  Cliquez sur **Envoyer**.

5.  Lorsque la fenêtre de **progression d’AGPM** indique la progression globale de l’opération, cliquez sur **Fermer**. Le nouvel objet GPO est affiché dans l’onglet **en attente** .

**Pour approuver la demande en attente de création d’un objet de stratégie de groupe**

1.  Sur un ordinateur sur lequel vous avez installé un client AGPM, connectez-vous avec un compte d’utilisateur auquel le rôle d’approbateur dans AGPM s’est attribué.

2.  Ouvrez la boîte de réception de votre compte et notez que vous avez reçu un message électronique de l’alias AGPM avec la demande de l’éditeur pour créer un objet de stratégie de groupe.

3.  Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.

4.  Dans l’onglet **contenu** , cliquez sur l’onglet **en attente** pour afficher les objets de stratégie de groupe en attente.

5.  Cliquez avec le bouton droit sur **MyGPO**, puis cliquez sur **approuver**.

6.  Cliquez sur **Oui** pour confirmer l’approbation de la création de l’objet de stratégie de groupe. L’objet de stratégie de groupe est déplacé vers l’onglet **contrôlé** .

### <a href="" id="bkmk-manage2"></a>Étape 2: modifier un objet de stratégie de groupe

Vous pouvez utiliser les objets de stratégie de groupe pour configurer les paramètres de l’ordinateur ou de l’utilisateur et les déployer sur de nombreux ordinateurs ou utilisateurs. Dans cette étape, vous utiliserez un compte avec le rôle d’éditeur pour extraire un objet de stratégie de groupe de l’archive, modifier l’objet de stratégie de groupe en mode hors connexion, Rechercher l’objet GPO modifié dans l’archive et demander le déploiement de l’objet de stratégie de groupe dans l’environnement de production. Pour ce scénario, vous devez configurer un paramètre dans l’objet de stratégie de groupe pour exiger que le mot de passe comporte au moins huit caractères.

**Pour extraire l’objet de stratégie de groupe de l’archive en vue de le modifier**

1.  Sur un ordinateur sur lequel vous avez installé le client AGPM, connectez-vous avec un compte d’utilisateur auquel le rôle d’éditeur a été attribué dans AGPM.

2.  Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.

3.  Dans l’onglet **contenu** du volet Détails, cliquez sur l’onglet **contrôlé** pour afficher les objets de stratégie de groupe contrôlés.

4.  Cliquez avec le bouton droit sur **MyGPO**, puis cliquez sur **extraire**.

5.  Tapez un commentaire à afficher dans l' **historique** de l’objet de stratégie de groupe lors de son extraction, puis cliquez sur **OK**.

6.  Lorsque la fenêtre de **progression d’AGPM** indique la progression globale de l’opération, cliquez sur **Fermer**. Dans l’onglet **contrôlé** , l’état de l’objet de stratégie de groupe est identifié comme **extrait**.

**Pour modifier l’objet de stratégie de groupe hors connexion et configurer la longueur de mot de passe minimum**

1.  Dans l’onglet **contrôlé** , cliquez avec le bouton droit sur **MyGPO**, puis cliquez sur **modifier** pour ouvrir la fenêtre Éditeur d’objets de stratégie de groupe et apporter des modifications à une copie hors connexion de l’objet de stratégie de **groupe** . Pour ce scénario, configurez la longueur minimale du mot de passe:

    1.  Sous **Configuration ordinateur**, double-cliquez sur **Paramètres Windows**, cliquez deux fois sur **paramètres de sécurité**, double-cliquez sur stratégies de **compte**, puis double-cliquez sur **stratégie de mot de passe**.

    2.  Dans le volet Détails, double-cliquez sur **longueur minimale du mot de passe**.

    3.  Dans la fenêtre Propriétés, activez la case à cocher **définir ce paramètre de stratégie** , définissez le nombre de caractères sur **8**, puis cliquez sur **OK**.

2.  Fermez la fenêtre de l' **éditeur d’objets de stratégie de groupe** .

**Pour archiver l’objet de stratégie de groupe dans l’archive**

1.  Dans l’onglet **contrôlé** , cliquez avec le bouton droit sur **MyGPO** , puis cliquez sur **Archiver**.

2.  Tapez un commentaire, puis cliquez sur **OK**.

3.  Lorsque la fenêtre de **progression d’AGPM** indique la progression globale de l’opération, cliquez sur **Fermer**. Dans l’onglet **contrôlé** , l’état de l’objet de stratégie de groupe est identifié comme **Archivé**.

**Pour demander le déploiement de l’objet de stratégie de groupe dans l’environnement de production**

1.  Dans l’onglet **contrôlé** , cliquez avec le bouton droit sur **MyGPO** , puis cliquez sur **déployer**.

2.  Dans la mesure où ce compte n’est pas un approbateur ou un administrateur AGPM, vous devez fournir une demande de déploiement. Pour recevoir une copie de la demande, tapez votre adresse de messagerie dans le champ **CC** . Tapez un commentaire à afficher dans l' **historique** de l’objet de stratégie de groupe, puis cliquez sur **valider**.

3.  Lorsque la fenêtre de **progression d’AGPM** indique la progression globale de l’opération, cliquez sur **Fermer**. **MyGPO** s’affiche dans la liste des objets de stratégie de groupe sous l’onglet **en attente** .

### <a href="" id="bkmk-manage3"></a>Étape 3: vérifier et déployer un objet de stratégie de groupe

Dans le cadre de cette étape, vous agissez en tant qu’approbateur, vous créez des rapports et vous analysez les paramètres et les modifications apportées aux paramètres dans l’objet de stratégie de groupe pour déterminer s’ils doivent être approuvés. Après avoir évalué l’objet de stratégie de groupe, vous le déployez dans l’environnement de production et le liez à un domaine ou à une unité d’organisation (UO) de sorte qu’il soit appliqué lorsque la stratégie de groupe est actualisée pour les ordinateurs de ce domaine ou UO.

**Pour vérifier les paramètres de l’objet de stratégie de groupe**

1.  Sur un ordinateur sur lequel vous avez installé un client AGPM, connectez-vous avec un compte d’utilisateur auquel le rôle d’approbateur dans AGPM s’est attribué. (N’importe quel administrateur de stratégie de groupe avec le rôle de relecteur, qui est inclus dans tous les autres rôles, peut consulter les paramètres d’un objet de stratégie de groupe).

2.  Ouvrez la boîte de réception du compte et notez que vous avez reçu un message électronique de l’alias AGPM avec une demande d’éditeur pour le déploiement d’un objet de stratégie de groupe.

3.  Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.

4.  Dans l’onglet **contenu** du volet Détails, cliquez sur l’onglet **en attente** .

5.  Double-cliquez sur **MyGPO** pour afficher son historique.

6.  Passez en revue les paramètres dans la version la plus récente de MyGPO:

    1.  Dans la fenêtre **historique** , cliquez avec le bouton droit sur la version de l’objet de stratégie de groupe avec le dateur le plus récent, cliquez sur **paramètres**, puis sur **rapport HTML** pour afficher un récapitulatif des paramètres de l’objet de stratégie de groupe.

    2.  Dans le navigateur Web, cliquez sur **Afficher tout** pour afficher tous les paramètres de l’objet de stratégie de groupe.

    3.  Fermez le navigateur.

7.  Comparez la version la plus récente de MyGPO à la première version archivée dans l’archive:

    1.  Dans la fenêtre **historique** , cliquez sur la version de l’objet de stratégie de groupe avec le dateur le plus récent. Maintenez la **touche CTRL enfoncée** et cliquez sur la version de l’objet de stratégie de groupe le plus ancien avec l’état **Archivé**.

    2.  Cliquez sur le bouton **différences** . La section **stratégies de compte/stratégie de mot de passe** est mise en évidence en vert et précédée de **\ [+ \]**, ce qui indique que ce paramètre est configuré uniquement dans la dernière version de l’objet de stratégie de groupe.

    3.  Cliquez sur **stratégies de compte/stratégie de mot de passe**. Le paramètre de **longueur minimum du mot de passe** est également mis en surbrillance en vert et précédé de **\ [+ \]** indiquant qu’il est configuré uniquement dans la dernière version de l’objet de stratégie de groupe.

    4.  Fermez le navigateur Web.

**Pour déployer l’objet de stratégie de groupe dans l’environnement de production**

1.  Dans l’onglet **en attente** , cliquez avec le bouton droit sur **MyGPO** , puis cliquez sur **approuver**.

2.  Tapez un commentaire à inclure dans l’historique de l’objet de stratégie de groupe.

3.  Cliquez sur **Oui**. Lorsque la fenêtre de **progression d’AGPM** indique la progression globale de l’opération, cliquez sur **Fermer**. L’objet de stratégie de groupe est déployé dans l’environnement de production.

**Pour lier l’objet de stratégie de groupe à un domaine ou une unité d’organisation**

1.  Dans la console GPMC, cliquez avec le bouton droit sur le domaine ou l’unité d’organisation à laquelle vous voulez appliquer l’objet de stratégie de groupe que vous avez configuré, puis cliquez sur **lier un objet de stratégie de groupe existant**.

2.  Dans la boîte de dialogue **Sélectionner un objet GPO** , cliquez sur **MyGPO**, puis cliquez sur **OK**.

### <a href="" id="bkmk-manage4"></a>Étape 4: utiliser un modèle pour créer un objet de stratégie de groupe

Dans le cadre de cette étape, vous utiliserez un compte avec le rôle d’éditeur pour créer un modèle (version non modifiable et statique d’un objet de stratégie de groupe) à utiliser comme point de départ pour la création de nouveaux objets de stratégie de groupe, puis créez un nouvel objet de stratégie de groupe basé sur ce modèle. Les modèles permettent de créer rapidement plusieurs objets de stratégie de groupe qui incluent un grand nombre des mêmes paramètres.

**Pour créer un modèle sur la base d’un objet de stratégie de groupe existant**

1.  Sur un ordinateur sur lequel vous avez installé le client AGPM, connectez-vous avec un compte d’utilisateur auquel le rôle d’éditeur a été attribué dans AGPM.

2.  Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.

3.  Dans l’onglet **contenu** du volet Détails, cliquez sur l’onglet **contrôlé** .

4.  Cliquez avec le bouton droit sur **MyGPO**, puis cliquez sur **enregistrer en tant que modèle** pour créer un modèle contenant tous les paramètres actuellement dans MyGPO.

5.  Tapez **MyTemplate** comme nom pour le modèle et un commentaire, puis cliquez sur **OK**.

6.  Lorsque la fenêtre de **progression d’AGPM** indique la progression globale de l’opération, cliquez sur **Fermer**. Le nouveau modèle s’affiche sous l’onglet **modèles** .

**Pour demander la création d’un nouvel objet de stratégie de groupe géré via AGPM**

1.  Cliquez sur l’onglet **contrôlé** .

2.  Cliquez avec le bouton droit sur le nœud de **contrôle de modification** , puis cliquez sur **nouvel objet de stratégie de**contrôle.

3.  Dans la boîte de dialogue **nouvel objet GPO contrôlé** :

    1.  Pour recevoir une copie de la demande, tapez votre adresse de messagerie dans le champ **CC** .

    2.  Tapez **MyOtherGPO** comme nom du nouvel objet de stratégie de groupe.

    3.  Tapez un commentaire pour le nouvel objet de stratégie de groupe.

    4.  Cliquez sur **créer Live**pour que le nouvel objet GPO soit déployé sur l’environnement de production immédiatement après approbation.

    5.  Dans **modèle d’objet de stratégie de groupe**, sélectionnez **MyTemplate**.

    6.  Cliquez sur **Envoyer**.

4.  Lorsque la fenêtre de **progression d’AGPM** indique la progression globale de l’opération, cliquez sur **Fermer**. Le nouvel objet GPO est affiché dans l’onglet **en attente** .

Utilisez un compte qui a été affecté le rôle d’approbateur pour approuver la demande en attente de création de l’objet de stratégie de groupe, comme vous l’avez fait à l' [étape 1: créer un objet de stratégie de groupe](#bkmk-manage1). MyTemplate incorpore tous les paramètres que vous avez configurés dans MyGPO. Dans la mesure où MyOtherGPO a été créé à l’aide de MyTemplate, il contient tous les paramètres qui MyGPO contenus au moment de la création de MyTemplate. Pour confirmer cela, vous pouvez générer un rapport de différences et comparer MyOtherGPO à MyTemplate.

**Pour extraire l’objet de stratégie de groupe de l’archive en vue de le modifier**

1.  Sur un ordinateur sur lequel vous avez installé le client AGPM, connectez-vous avec un compte d’utilisateur auquel le rôle d’éditeur a été attribué dans AGPM.

2.  Cliquez avec le bouton droit sur **MyOtherGPO**, puis cliquez sur **extraire**.

3.  Tapez un commentaire à afficher dans l’historique de l’objet de stratégie de groupe lors de son extraction, puis cliquez sur **OK**.

4.  Lorsque la fenêtre de **progression d’AGPM** indique la progression globale de l’opération, cliquez sur **Fermer**. Dans l’onglet **contrôlé** , l’état de l’objet de stratégie de groupe est identifié comme **extrait**.

**Pour modifier l’objet de stratégie de groupe hors connexion et configurer la durée de verrouillage du compte**

1.  Dans l’onglet **contrôlé** , cliquez avec le bouton droit sur **MyOtherGPO**, puis cliquez sur **modifier** pour ouvrir la fenêtre Éditeur d’objets de stratégie de groupe et apporter des modifications à une copie hors connexion de l’objet de stratégie de **groupe** . Pour ce scénario, configurez la longueur minimale du mot de passe:

    1.  Sous **Configuration ordinateur**, double-cliquez sur **Paramètres Windows**, cliquez deux fois sur **paramètres de sécurité**, double-cliquez sur stratégies de **compte**, puis double-cliquez sur stratégie de **verrouillage du compte**.

    2.  Dans le volet Détails, double-cliquez sur **durée de verrouillage du compte**.

    3.  Dans la fenêtre Propriétés, activez la case à cocher **définir ce paramètre de stratégie**, définissez une durée de **30** minutes, puis cliquez sur **OK**.

2.  Fermez la fenêtre de l' **éditeur d’objets de stratégie de groupe** .

Consultez MyOtherGPO dans l’archive et demandez le déploiement comme vous l’avez fait pour MyGPO à l' [étape 2: modifier un objet de stratégie de groupe](#bkmk-manage2). Vous pouvez comparer MyOtherGPO à MyGPO ou à MyTemplate à l’aide de rapports de différences. Tout compte qui inclut le rôle de réviseur (Administrateur AGPM [contrôle total \], approbateur, éditeur ou réviseur) peut générer des rapports.

**Pour comparer un objet GPO à un autre et à un modèle**

1.  Pour comparer MyGPO et MyOtherGPO:

    1.  Dans l’onglet **contrôlé** , cliquez sur **MyGPO**. Appuyez sur **CTRL** et cliquez sur **MyOtherGPO**.

    2.  Cliquez avec le bouton droit sur **MyOtherGPO**, pointez sur **différences**, puis cliquez sur **rapport HTML**.

2.  Pour comparer MyOtherGPO et MyTemplate:

    1.  Dans l’onglet **contrôlé** , cliquez sur **MyOtherGPO**.

    2.  Cliquez avec le bouton droit sur **MyOtherGPO**, pointez sur **différences**, puis cliquez sur **modèle**.

    3.  Sélectionnez **MyTemplate** et **HTML Report**, puis cliquez sur **OK**.

### <a href="" id="bkmk-manage5"></a>Étape 5: supprimer et restaurer un objet de stratégie de groupe

Dans le cadre de cette étape, vous jouerez le rôle d’approbateur pour supprimer un objet GPO.

**Pour supprimer un objet de stratégie de groupe**

1.  Sur un ordinateur sur lequel vous avez installé un client AGPM, connectez-vous avec un compte d’utilisateur auquel le rôle d’approbateur a été attribué.

2.  Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.

3.  Dans l’onglet **contenu** , cliquez sur l’onglet **contrôlé** pour afficher les objets de stratégie de groupe contrôlés.

4.  Cliquez avec le bouton droit sur **MyGPO**, puis cliquez sur **supprimer**. Cliquez sur **Supprimer l’objet GPO d’archive et de production** pour supprimer la version dans l’archive ainsi que la version déployée de l’objet de stratégie de groupe dans l’environnement de production.

5.  Tapez un commentaire à afficher dans la trace d’audit de l’objet de stratégie de groupe, puis cliquez sur **OK**.

6.  Lorsque la fenêtre de **progression d’AGPM** indique la progression globale de l’opération, cliquez sur **Fermer**. L’objet de stratégie de groupe est supprimé de l’onglet **contrôlé** et s’affiche sous l’onglet de la **Corbeille** , où il peut être restauré ou détruit.

Occasionnellement, il est possible que vous puissiez découvrir après avoir supprimé un objet GPO qu’il est toujours nécessaire. Dans le cadre de cette étape, vous vous attendez en tant qu’approbateur de la restauration d’un objet de stratégie de groupe qui a été supprimé.

**Pour restaurer un objet de stratégie de groupe supprimé**

1.  Dans l’onglet **contenu** , cliquez sur l’onglet **Corbeille** pour afficher les objets de stratégie de groupe supprimés.

2.  Cliquez avec le bouton droit sur **MyGPO**, puis cliquez sur **restaurer**.

3.  Tapez un commentaire à afficher dans l’historique de l’objet de stratégie de groupe, puis cliquez sur **OK**.

4.  Lorsque la fenêtre de **progression d’AGPM** indique la progression globale de l’opération, cliquez sur **Fermer**. L’objet de stratégie de groupe est supprimé de l’onglet **Corbeille** et s’affiche sous l’onglet **contrôlé** .

    **Remarques**  La restauration d’un objet de stratégie de groupe dans l’archive ne le redéploie pas automatiquement dans l’environnement de production. Pour renvoyer l’objet de stratégie de groupe à l’environnement de production, déployez l’objet GPO comme à l' [étape 3: passer en revue et déployer un objet de stratégie de groupe](#bkmk-manage3).

     

Après la modification et le déploiement d’un objet de stratégie de groupe, il est possible que les modifications récentes apportées à l’objet GPO causent un problème. Dans le cadre de cette étape, vous faites Office d’approbateur pour restaurer une version précédente de l’objet de stratégie de groupe. Vous pouvez revenir à une version quelconque de l’historique de l’objet de stratégie de groupe. Vous pouvez utiliser des commentaires et des étiquettes pour identifier les versions connues et en cas de modifications spécifiques.

**Pour restaurer une version précédente d’un objet de stratégie de groupe**

1.  Dans l’onglet **contenu** , cliquez sur l’onglet **contrôlé** pour afficher les objets de stratégie de groupe contrôlés.

2.  Double-cliquez sur **MyGPO** pour afficher son historique.

3.  Cliquez avec le bouton droit sur la version que vous voulez déployer, cliquez sur **déployer**, puis sur **Oui**.

4.  Lorsque la fenêtre de **progression** indique que l’avancement global est terminé, cliquez sur **Fermer**. Dans la fenêtre **historique** , cliquez sur **Fermer**.

    **Remarques**  Pour vérifier que la version qui a été redéployée est la version prévue, examinez un rapport de différences pour les deux versions. Dans la fenêtre **historique** de l’objet de stratégie de groupe, sélectionnez les deux versions, cliquez dessus avec le bouton droit, pointez sur **différence**, puis cliquez sur rapport **HTML** ou sur **rapport XML**.

     

 

 





