---
title: Guide pas à pas de la Gestion avancée des stratégies de groupe Microsoft 4.0
description: Guide pas à pas de la Gestion avancée des stratégies de groupe Microsoft 4.0
author: dansimp
ms.assetid: dc6f9b16-b1d4-48f3-88bb-f29301f0131c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 567f9a8b14bc05a226b93947e6311ea93c0bf3b2
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910709"
---
# <a name="step-by-step-guide-for-microsoft-advanced-group-policy-management-40"></a>Guide pas à pas de la Gestion avancée des stratégies de groupe Microsoft 4.0


Ce guide pas à pas présente les techniques avancées de gestion des stratégies de groupe qui utilisent la Console de gestion des stratégies de groupe (GPMC) et la Gestion avancée des stratégies de groupe (AGPM) Microsoft. AGPM augmente les fonctionnalités de la GPMC, en fournissant :

-   Rôles standard pour la délégation des autorisations de gestion des objets de stratégie de groupe à plusieurs administrateurs de stratégie de groupe, en plus de la possibilité de déléguer l’accès aux objets de stratégie de groupe dans l’environnement de production.

-   Archive permettant aux administrateurs de stratégie de groupe de créer et de modifier des G STRATÉGIE de groupe hors connexion avant leur déploiement dans un environnement de production.

-   Possibilité de revenir à une version antérieure d’un GPO dans l’archive et de limiter le nombre de versions stockées dans l’archive.

-   Fonctionnalité d’enregistrement et d’check-out pour les G GPO afin de s’assurer que les administrateurs de stratégie de groupe n’ont pas accidentellement le travail des uns et des autres.

-   La possibilité de rechercher des G GPO avec des attributs spécifiques et de filtrer la liste des GGP affichés.

## <a name="agpm-scenario-overview"></a>Vue d’ensemble du scénario AGPM


Pour ce scénario, vous allez utiliser un compte d’utilisateur distinct pour chaque rôle dans AGPM afin de montrer comment la stratégie de groupe peut être gérée dans un environnement où plusieurs administrateurs de stratégie de groupe disposent de différents niveaux d’autorisations. Plus précisément, vous allez effectuer les tâches suivantes :

-   À l’aide d’un compte membre du groupe Administrateurs du domaine, installez le serveur AGPM et attribuez le rôle d’administrateur AGPM à un compte ou un groupe.

-   À l’aide des comptes pour lesquels vous allez attribuer des rôles AGPM, installez le client AGPM.

-   À l’aide d’un compte qui a le rôle d’administrateur AGPM, configurez AGPM et déléguer l’accès aux GPM en attribuant des rôles à d’autres comptes.

-   À partir d’un compte qui a le rôle d’éditeur, demandez la création d’un nouvel GPO que vous approuvez ensuite à l’aide d’un compte qui a le rôle d’approbation. Utilisez le compte d’éditeur pour vérifier l’GPO hors de l’archive, modifiez-le, archivez-le dans l’archive, puis demandez le déploiement.

-   À l’aide d’un compte qui a le rôle d’approbation, examinez l’GPO et déployez-le dans votre environnement de production.

-   À l’aide d’un compte qui a le rôle d’éditeur, créez un modèle d’GPO et utilisez-le comme point de départ pour créer un nouvel GPO.

-   À l’aide d’un compte qui a le rôle d’approbation, supprimez et restituer un GPO.

![processus de développement d’objets de stratégie de groupe.](images/ab77a1f3-f430-4e7d-be58-ee8f9bd1140e.gif)

## <a name="requirements"></a>Conditions préalables


Les ordinateurs sur lesquels vous souhaitez installer AGPM doivent répondre aux exigences suivantes et vous devez créer des comptes à utiliser dans ce scénario.

**Remarque**  
Si AGPM 2.5 est installé et que vous êtes en cours de mise à niveau depuis Windows Server® 2003 vers Windows Server 2008 R2 ou Windows Server 2008, ou sont en cours de mise à niveau à partir de Windows Vista sans service pack installé sur Windows 7 ou Windows Vista® avec Service Pack 1 (SP1), vous devez mettre à niveau le système d’exploitation avant de pouvoir mettre à niveau vers AGPM 4.0.

Si AGPM 3.0 est installé, vous n’avez pas besoin de mettre à niveau le système d’exploitation avant de mettre à niveau vers AGPM 4.0.

 

Dans un environnement mixte qui inclut des systèmes d’exploitation plus anciens et plus anciens, il existe certaines limitations aux fonctionnalités, comme indiqué dans le tableau suivant.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Système d’exploitation sur lequel AGPM Server 4.0 s’exécute</th>
<th align="left">Système d’exploitation sur lequel AGPM Client 4.0 s’exécute</th>
<th align="left">État de la prise en charge d’AGPM 4.0</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows Server 2008 R2 ou Windows 7</p></td>
<td align="left"><p>Windows Server 2008 R2 ou Windows 7</p></td>
<td align="left"><p>Pris en charge</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2008 R2 ou Windows 7</p></td>
<td align="left"><p>Windows Server 2008 ou Windows Vista avec SP1</p></td>
<td align="left"><p>Pris en charge, mais ne peut pas modifier les paramètres de stratégie ou les éléments de préférence qui existent uniquement dans Windows Server 2008 R2 ou Windows 7</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2008 ou Windows Vista avec SP1</p></td>
<td align="left"><p>Windows Server 2008 R2 ou Windows 7</p></td>
<td align="left"><p>Non pris en charge</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2008 ou Windows Vista avec SP1</p></td>
<td align="left"><p>Windows Server 2008 ou Windows Vista avec SP1</p></td>
<td align="left"><p>Pris en charge, mais ne peut pas signaler ou modifier les paramètres de stratégie ou les éléments de préférence qui existent uniquement dans Windows Server 2008 R2 ou Windows 7</p></td>
</tr>
</tbody>
</table>

 

### <a name="agpm-server-requirements"></a>Conditions requises pour le serveur AGPM

AGPM Server 4.0 nécessite Windows Server 2008 R2, Windows Server 2008, Windows 7 et la GPMC des outils d’administration de serveur distant (RSAT), ou Windows Vista avec SP1 et la GPMC à partir de RSAT installés. Les versions 32 bits et 64 bits sont toutes deux pris en charge.

Avant d’installer le serveur AGPM, vous devez être membre du groupe Administrateurs du domaine et les fonctionnalités Windows suivantes doivent être présentes sauf indication contraire :

-   GPMC

    -   Windows Server 2008 R2 ou Windows Server 2008 : si la GPMC n’est pas présente, elle est automatiquement installée par AGPM.

    -   Windows 7 : vous devez installer la GPMC à partir de RSAT avant d’installer AGPM. Pour plus d’informations, [voir Outils d’administration](https://go.microsoft.com/fwlink/?LinkID=131280) de serveur distant pour Windows 7 ( https://go.microsoft.com/fwlink/?LinkID=131280) .

    -   Windows Vista avec SP1 : vous devez installer la GPMC à partir de RSAT avant d’installer AGPM. Pour plus d’informations, [voir Outils d’administration de serveur](https://go.microsoft.com/fwlink/?LinkID=116179) distant pour Windows Vista avec Service Pack 1 ( https://go.microsoft.com/fwlink/?LinkID=116179) .

-   Le .NET Framework version 3.5 ou ultérieure

    -   Windows Serveur 2008 R2 ou Windows 7 : si la version .NET Framework 3.5 ou ultérieure n’est pas présente, le .NET Framework 3.5 est automatiquement installé par AGPM.

    -   Windows Server 2008 ou Windows Vista avec SP1 : vous devez installer la version .NET Framework 3.5 ou une version ultérieure avant d’installer AGPM.

Les fonctionnalités Windows suivantes sont requises par AGPM Server et sont automatiquement installées si elles ne sont pas présentes :

-   Activation WCF ; Activation non HTTP

-   Service d'activation des processus Windows

    -   Modèle de processus

    -   Environnement .NET

    -   API de configuration

### <a name="agpm-client-requirements"></a>Conditions requises pour le client AGPM

AGPM Client 4.0 nécessite Windows Server 2008 R2, Windows Server 2008, Windows 7 et la GPMC à partir de RSAT, ou Windows Vista avec SP1 et la GPMC à partir de RSAT installés. Les versions 32 bits et 64 bits sont toutes deux pris en charge. Le client AGPM peut être installé sur un ordinateur qui exécute le serveur AGPM.

Les fonctionnalités Windows suivantes sont requises par le client AGPM et, sauf indication contraire, sont installées automatiquement si elles ne sont pas présentes :

-   GPMC

    -   Windows Server 2008 R2 ou Windows Server 2008 : si la GPMC n’est pas présente, elle est automatiquement installée par AGPM.

    -   Windows 7 : vous devez installer la GPMC à partir de RSAT avant d’installer AGPM. Pour plus d’informations, [voir Outils d’administration](https://go.microsoft.com/fwlink/?LinkID=131280) de serveur distant pour Windows 7 ( https://go.microsoft.com/fwlink/?LinkID=131280) .

    -   Windows Vista avec SP1 : vous devez installer la GPMC à partir de RSAT avant d’installer AGPM. Pour plus d’informations, [voir Outils d’administration de serveur](https://go.microsoft.com/fwlink/?LinkID=116179) distant pour Windows Vista avec Service Pack 1 ( https://go.microsoft.com/fwlink/?LinkID=116179) .

-   Le .NET Framework version 3.0 ou ultérieure

    -   Windows Serveur 2008 R2 ou Windows 7 : si la version .NET Framework 3.0 ou ultérieure n’est pas présente, le .NET Framework 3.5 est automatiquement installé par AGPM.

    -   Windows Server 2008 ou Windows Vista avec SP1 : si la version .NET Framework 3.0 ou ultérieure n’est pas présente, le .NET Framework 3.0 est automatiquement installé par AGPM.

### <a name="scenario-requirements"></a>Conditions requises pour le scénario

Avant de commencer ce scénario, créez quatre comptes d’utilisateur. Au cours du scénario, vous allez attribuer l’un des rôles AGPM suivants à chacun de ces comptes : Administrateur AGPM (Contrôle total), Approuver, Éditeur et Réviseur. Ces comptes doivent pouvoir envoyer et recevoir des messages électroniques. Attribuez **l’autorisation d’associer** des GPM aux comptes qui ont les rôles d’administrateur AGPM, d’approbation et d’éditeur (facultatif).

**Remarque**  
**L’autorisation d’os** de groupe de liens est attribuée aux membres des administrateurs de domaine Enterprise administrateurs de domaine par défaut. Pour **** attribuer l’autorisation d’associer des GPM à d’autres utilisateurs ou groupes (tels que les comptes **** qui ont les rôles d’administrateur AGPM ou d’approbation), cliquez sur le nœud du domaine, puis cliquez sur l’onglet Délégation, sélectionnez Lier des GPM, **** cliquez sur **Ajouter,** puis sélectionnez les utilisateurs ou groupes auquel vous souhaitez attribuer l’autorisation.

 

## <a name="steps-for-installing-and-configuring-agpm"></a>Étapes d’installation et de configuration d’AGPM


Vous devez effectuer les étapes suivantes pour installer et configurer AGPM.

[Étape 1 : Installer le serveur AGPM](#bkmk-config1)

[Étape 2 : Installer le client AGPM](#bkmk-config2)

[Étape 3 : Configurer une connexion de serveur AGPM](#bkmk-config3)

[Étape 4 : Configurer la notification par courrier électronique](#bkmk-config4)

[Étape 5 : Déléguer l’accès](#bkmk-config5)

### <a name="step-1-install-agpm-server"></a><a href="" id="bkmk-config1"></a>Étape 1 : Installer le serveur AGPM

Dans cette étape, vous installez le serveur AGPM sur le serveur membre ou le contrôleur de domaine qui exécutera le service AGPM et vous configurez l’archive. Toutes les opérations AGPM sont gérées par Windows service et sont exécutées avec les informations d’identification du service. L’archive gérée par un serveur AGPM peut être hébergée sur ce serveur ou sur un autre serveur de la même forêt.

**Pour installer le serveur AGPM sur l’ordinateur qui hébergera le service AGPM**

1.  Connectez-vous avec un compte membre du groupe Administrateurs du domaine.

2.  Démarrez le CD du Pack d’optimisation du bureau Microsoft et suivez les instructions à l’écran pour sélectionner **Advanced Group Policy Management - Server**.

3.  Dans la **boîte de dialogue** Bienvenue, cliquez sur **Suivant.**

4.  Dans la boîte de dialogue Termes du contrat de licence logiciel **Microsoft,** acceptez les termes, puis cliquez sur **Suivant**.

5.  Dans la boîte **de dialogue Chemin d’accès** de l’application, sélectionnez l’emplacement dans lequel installer le serveur AGPM. L’ordinateur sur lequel le serveur AGPM est installé hébergera le service AGPM et gérera l’archive. Cliquez sur **Suivant**.

6.  Dans la **boîte de dialogue Chemin** d’accès de l’archive, sélectionnez un emplacement pour l’archive par rapport au serveur AGPM. Le chemin d’accès d’archivage peut pointer vers un dossier sur le serveur AGPM ou ailleurs. Toutefois, vous devez sélectionner un emplacement avec suffisamment d’espace pour stocker tous les GPM et les données d’historique gérés par ce serveur AGPM. Cliquez sur **Suivant**.

7.  Dans la boîte de dialogue Compte de **service AGPM,** sélectionnez un compte de service sous lequel le service AGPM s’exécutera, puis cliquez sur **Suivant**.

    Ce compte doit être membre du groupe Administrateurs du domaine ou, pour une configuration avec privilèges minimum, des groupes suivants dans chaque domaine géré par le serveur AGPM :

    -   Propriétaires créateurs de stratégie de groupe

    -   Opérateurs de sauvegarde

    En outre, ce compte requiert l’autorisation Contrôle total pour les dossiers suivants :

    -   Dossier d’archivage AGPM, pour lequel cette autorisation est automatiquement accordée lors de l’installation du serveur AGPM s’il est installé sur un lecteur local.

    -   Dossier temporaire du système local, généralement %windir%\\temp.

8.  Dans la **boîte de dialogue Propriétaire** de l’archive, sélectionnez un compte ou un groupe auquel vous attribuez le rôle Administrateur AGPM (Contrôle total). Les administrateurs AGPM peuvent attribuer des rôles et des autorisations AGPM à d’autres administrateurs de stratégie de groupe, de sorte que vous pouvez ultérieurement attribuer le rôle d’administrateur AGPM à d’autres administrateurs de stratégie de groupe. Pour ce scénario, sélectionnez le compte à servir dans le rôle Administrateur AGPM. Cliquez sur **Suivant**.

9.  Dans la **boîte de dialogue Configuration** du port, tapez un port sur lequel le service AGPM doit écouter. Ne pas effacer la case à cocher Ajouter une exception de **port** au pare-feu, sauf si vous configurez manuellement des exceptions de port ou utilisez des règles pour configurer des exceptions de port. Cliquez sur **Suivant**.

10. Dans la **boîte de dialogue Langues,** sélectionnez une ou plusieurs langues d’affichage à installer pour le serveur AGPM.

11. Cliquez **sur Installer,** puis sur **Terminer** pour quitter l’Assistant Installation.

    **Attention**  
    Ne modifiez pas les paramètres du service AGPM par le biais **des outils** et **services** d’administration du système d’exploitation. Cela peut empêcher le démarrage du service AGPM. Pour plus d’informations sur la modification des paramètres du service, voir l’aide sur la gestion avancée des stratégies de groupe.

     

### <a name="step-2-install-agpm-client"></a><a href="" id="bkmk-config2"></a>Étape 2 : Installer le client AGPM

Chaque administrateur de stratégie de groupe (toute personne qui crée, modifie, déploie, examine ou supprime des GPM) doit avoir installé le client AGPM sur les ordinateurs qu’il utilise pour gérer les GPM. Le nœud Contrôle des changements, que vous utilisez pour effectuer de nombreuses tâches de gestion des GPO, apparaît dans la console de gestion des stratégies de groupe uniquement si vous installez le client AGPM. Dans ce scénario, vous installez le client AGPM sur au moins un ordinateur. Vous n’avez pas besoin d’installer le client AGPM sur les ordinateurs des utilisateurs finaux qui n’effectuent pas d’administration de stratégie de groupe.

**Pour installer le client AGPM sur l’ordinateur d’un administrateur de stratégie de groupe**

1.  Démarrez le CD du Pack d’optimisation du bureau Microsoft et suivez les instructions à l’écran pour sélectionner **Advanced Group Policy Management - Client**.

2.  Dans la **boîte de dialogue** Bienvenue, cliquez sur **Suivant.**

3.  Dans la boîte de dialogue Termes du contrat de licence logiciel **Microsoft,** acceptez les termes, puis cliquez sur **Suivant**.

4.  Dans la boîte **de dialogue Chemin d’accès** de l’application, sélectionnez l’emplacement dans lequel installer le client AGPM. Cliquez sur **Suivant**.

5.  Dans la **boîte de dialogue Serveur AGPM,** tapez le nom DNS ou l’adresse IP du serveur AGPM et le port auquel vous souhaitez vous connecter. Le port par défaut pour le service AGPM est 4600. Ne pas effacer la case à cocher Autoriser la console de gestion **Microsoft** via le pare-feu, sauf si vous configurez manuellement des exceptions de port ou utilisez des règles pour configurer les exceptions de port. Cliquez sur **Suivant**.

6.  Dans la **boîte de dialogue Langues,** sélectionnez une ou plusieurs langues d’affichage à installer pour le client AGPM.

7.  Cliquez **sur Installer,** puis sur **Terminer** pour quitter l’Assistant Installation.

### <a name="step-3-configure-an-agpm-server-connection"></a><a href="" id="bkmk-config3"></a>Étape 3 : Configurer une connexion de serveur AGPM

AGPM stocke toutes les versions de chaque objet de stratégie de groupe contrôlé, c’est-à-dire, chaque objet de stratégie de groupe pour lequel AGPM fournit le contrôle des changements, dans une archive centrale. Cela permet aux administrateurs de stratégie de groupe d’afficher et de modifier les GPO hors connexion sans affecter immédiatement la version déployée de chaque GPO.

Dans cette étape, vous configurez une connexion agpm server et assurez-vous que tous les administrateurs de stratégie de groupe se connectent au même serveur AGPM. (Pour plus d’informations sur la configuration de plusieurs serveurs AGPM, voir l’aide sur la gestion avancée des stratégies de groupe.)

**Pour configurer une connexion de serveur AGPM pour tous les administrateurs de stratégie de groupe**

1.  Sur un ordinateur sur lequel vous avez installé le client AGPM, connectez-vous avec le compte d’utilisateur que vous avez sélectionné en tant que propriétaire de l’archive. Cet utilisateur a le rôle d’administrateur AGPM (Contrôle total).

2.  Cliquez **sur Démarrer,** pointez **sur Outils**d’administration, puis cliquez sur **Gestion** des stratégies de groupe pour ouvrir la GPMC.

3.  Modifier un GPO qui est appliqué à tous les administrateurs de stratégie de groupe.

4.  Dans la fenêtre **Éditeur de** gestion des stratégies de groupe, double-cliquez sur **Configuration** **utilisateur,** **Stratégies, Modèles**d’administration, Windows **Composants**et **AGPM.**

5.  Dans le volet d’informations, double-cliquez sur AGPM : spécifiez le serveur AGPM par défaut **(tous les domaines).**

6.  Dans **la** fenêtre **** Propriétés, sélectionnez Activé et tapez le nom DNS ou l’adresse IP et le port (par exemple, **server.contoso.com:4600**) pour le serveur hébergeant l’archive. Par défaut, le service AGPM utilise le port 4600.

7.  Cliquez **sur OK,** puis fermez la fenêtre Éditeur de gestion **des stratégies de** groupe. Lorsque la stratégie de groupe est mise à jour, la connexion du serveur AGPM est configurée pour chaque administrateur de stratégie de groupe.

### <a name="step-4-configure-e-mail-notification"></a><a href="" id="bkmk-config4"></a>Étape 4 : Configurer la notification par courrier électronique

En tant qu’administrateur AGPM (Contrôle total), vous désignez les adresses de messagerie des approveurs et des administrateurs AGPM auxquels un message électronique contenant une demande est envoyé lorsqu’un éditeur tente de créer, déployer ou supprimer un GPO. Vous déterminez également l’alias à partir duquel ces messages sont envoyés.

**Pour configurer la notification par courrier électronique pour AGPM**

1.  Dans **l’Éditeur de gestion des stratégies de** groupe, accédez au **dossier Contrôle des** changements 

2.  Dans le volet d’informations, cliquez sur **l’onglet Délégation de** domaine.

3.  Dans le **champ Adresse de** messagerie De, tapez l’alias de messagerie pour AGPM à partir duquel les notifications doivent être envoyées.

4.  Dans le **champ Adresse de** messagerie À, tapez l’adresse de messagerie du compte d’utilisateur auquel vous avez l’intention d’attribuer le rôle d’approuveur.

5.  Dans le **champ serveur SMTP,** tapez un serveur de messagerie SMTP valide.

6.  Dans les **champs Nom d’utilisateur** et **Mot** de passe, tapez les informations d’identification d’un utilisateur ayant accès au service SMTP. Cliquez sur **Apply** (Appliquer).

### <a name="step-5-delegate-access"></a><a href="" id="bkmk-config5"></a>Étape 5 : Déléguer l’accès

En tant qu’administrateur AGPM (Contrôle total), vous déléguer l’accès au niveau du domaine aux GPM, en attribuant des rôles au compte de chaque administrateur de stratégie de groupe.

**Remarque**  
Vous pouvez également déléguer l’accès au niveau de l’GPO plutôt qu’au niveau du domaine. Pour plus d’informations, voir l’aide sur la gestion avancée des stratégies de groupe.

 

**Important**  
Vous devez restreindre l’appartenance au groupe Propriétaires créateurs de stratégie de groupe afin qu’il ne puisse pas être utilisé pour contourner la gestion AGPM de l’accès aux GPM. (Dans la **console**de gestion des **stratégies** de groupe, cliquez sur Objets de stratégie de groupe dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe, cliquez sur **Délégation,** puis configurez les paramètres pour répondre aux besoins de votre organisation.)

 

**Pour déléguer l’accès à tous les G GPO dans un domaine**

1.  Sous **l’onglet Délégation** **** de domaine, cliquez sur le bouton Ajouter, sélectionnez le compte d’utilisateur de l’administrateur de stratégie de groupe en tant qu’approuveur, puis cliquez sur **OK**.

2.  Dans la **boîte de dialogue** Ajouter **** un groupe ou un utilisateur, sélectionnez le rôle d’approbation pour attribuer ce rôle au compte, puis cliquez sur **OK.** (Ce rôle inclut le rôle Réviseur.)

3.  Cliquez sur **le bouton** Ajouter, sélectionnez le compte d’utilisateur de l’administrateur de stratégie de groupe en tant qu’éditeur, puis cliquez sur **OK.**

4.  Dans la boîte de dialogue Ajouter **** **un** groupe ou un utilisateur, sélectionnez le rôle d’éditeur pour attribuer ce rôle au compte, puis cliquez sur **OK.** (Ce rôle inclut le rôle Réviseur.)

5.  Cliquez sur **le bouton** Ajouter, sélectionnez le compte d’utilisateur de l’administrateur de stratégie de groupe à servir de réviseur, puis cliquez sur **OK**.

6.  Dans la **boîte de dialogue Ajouter un groupe ou** un utilisateur, sélectionnez le rôle **Réviseur** pour attribuer uniquement ce rôle au compte.

## <a name="steps-for-managing-gpos"></a>Étapes de gestion des G GPO


Vous devez effectuer les étapes suivantes pour créer, modifier, réviser et déployer des GPM à l’aide d’AGPM. En outre, vous allez créer un modèle, supprimer un GPO et restaurer un GPO supprimé.

[Étape 1 : Créer un GPO](#bkmk-manage1)

[Étape 2 : Modifier un GPO](#bkmk-manage2)

[Étape 3 : Examiner et déployer un GPO](#bkmk-manage3)

[Étape 4 : Utiliser un modèle pour créer un GPO](#bkmk-manage4)

[Étape 5 : Supprimer et restaurer un GPO](#bkmk-manage5)

### <a name="step-1-create-a-gpo"></a><a href="" id="bkmk-manage1"></a>Étape 1 : Créer un GPO

Dans un environnement qui dispose de plusieurs administrateurs de stratégie de groupe, ceux qui ont le rôle d’éditeur peuvent demander la création de nouveaux G STRATÉGIE de groupe. Toutefois, cette demande doit être approuvée par une personne ayant le rôle d’approbation.

Dans cette étape, vous utilisez un compte qui a le rôle d’éditeur pour demander la création d’un nouvel GPO. À l’aide d’un compte qui a le rôle d’approbation, vous approuvez cette demande pour créer l’GPO.

**Pour demander la création et la gestion d’un nouvel GPO via AGPM**

1.  Sur un ordinateur sur lequel vous avez installé le client AGPM, connectez-vous avec un compte d’utilisateur auquel est attribué le rôle Éditeur dans AGPM.

2.  Dans **l’arborescence de** la Console de gestion des stratégies de groupe, cliquez sur **Modifier** le contrôle dans la forêt et le domaine dans lesquels vous souhaitez gérer les GGP.

3.  Cliquez avec le bouton **droit sur le** nœud Contrôle des changements, puis cliquez sur Nouvel **GPO contrôlé.**

4.  Dans la **boîte de dialogue Nouvel GPO** contrôlé :

    1.  Pour recevoir une copie de la demande, tapez votre adresse de messagerie dans le **champ Cc.**

    2.  Tapez **MyGPO** comme nom pour le nouvel GPO.

    3.  Tapez un commentaire pour le nouvel GPO.

    4.  Cliquez **sur Créer en** direct afin que le nouvel GPO soit déployé dans l’environnement de production immédiatement après approbation. Cliquez sur **Envoyer**.

5.  Lorsque la fenêtre **Progression de l’AGPM** indique que la progression globale est terminée, cliquez sur **Fermer**. Le nouvel GPO s’affiche sous **l’onglet En** attente.

**Pour approuver la demande en attente de création d’un GPO**

1.  Sur un ordinateur sur lequel vous avez installé le client AGPM, connectez-vous avec un compte d’utilisateur ayant le rôle d’approuveur dans AGPM.

2.  Ouvrez la boîte de réception de messagerie du compte et notez que vous avez reçu un message électronique de l’alias AGPM avec la demande de l’éditeur de créer un GPO.

3.  Dans **l’arborescence de** la Console de gestion des stratégies de groupe, cliquez sur **Modifier** le contrôle dans la forêt et le domaine dans lesquels vous souhaitez gérer les GGP.

4.  Sous **l’onglet** Contenu, cliquez sur **l’onglet En attente** pour afficher les GGP en attente.

5.  Cliquez avec le bouton **droit sur MyGPO,** puis cliquez sur **Approuver.**

6.  Cliquez **sur Oui** pour confirmer l’approbation et déplacer l’GPO vers **l’onglet** Contrôlé.

### <a name="step-2-edit-a-gpo"></a><a href="" id="bkmk-manage2"></a>Étape 2 : Modifier un GPO

Vous pouvez utiliser des G GPO pour configurer les paramètres d’ordinateur ou d’utilisateur et les déployer sur de nombreux ordinateurs ou utilisateurs. Dans cette étape, vous utilisez un compte qui a le rôle d’éditeur pour consulter un GPO à partir de l’archive, modifier l’GPO hors connexion, vérifier l’GPO modifié dans l’archive et demander le déploiement de l’GPO dans l’environnement de production. Pour ce scénario, vous configurez un paramètre dans l’GPO pour exiger que le mot de passe soit d’au moins huit caractères.

**Pour vérifier l’GPO à partir de l’archive pour modification**

1.  Sur un ordinateur sur lequel vous avez installé le client AGPM, connectez-vous avec un compte d’utilisateur ayant le rôle Éditeur dans AGPM.

2.  Dans **l’arborescence de** la Console de gestion des stratégies de groupe, cliquez sur **Modifier** le contrôle dans la forêt et le domaine dans lesquels vous souhaitez gérer les GGP.

3.  Sous **l’onglet** Contenu du volet d’informations, cliquez sur l’onglet Contrôlé pour afficher les GOP contrôlés. ****

4.  Cliquez avec le bouton **droit sur MyGPO,** puis cliquez **sur Check Out**.

5.  Tapez un commentaire à afficher dans l’historique de l’GPO pendant qu’il est extrait, puis cliquez sur **OK**.

6.  Lorsque la fenêtre **Progression de l’AGPM** indique que la progression globale est terminée, cliquez sur **Fermer**. Sous **l’onglet** Contrôlé, l’état de l’GPO est identifié comme **extrait.**

**Pour modifier l’GPO hors connexion et configurer la longueur minimale du mot de passe**

1.  Sous **l’onglet** Contrôlé, cliquez avec le bouton **** droit sur **** **MyGPO,** puis cliquez sur Modifier pour ouvrir la fenêtre Éditeur de gestion des stratégies de groupe et modifier une copie hors connexion de l’GPO. Pour ce scénario, configurez la longueur minimale du mot de passe :

    1.  Sous **Configuration ordinateur,** double-cliquez sur **Stratégies,** **Windows Paramètres,** Sécurité **Paramètres,** **Stratégies**de compte et Stratégie de mot **de passe.**

    2.  Dans le volet d’informations, double-cliquez sur Longueur minimale **du mot de passe.**

    3.  Dans la fenêtre propriétés, cochez la case Définir ce paramètre de stratégie, définissez le nombre de caractères sur **8,** puis cliquez sur **** **OK**.

2.  Fermez la **fenêtre Éditeur de gestion des stratégies de** groupe.

**Pour vérifier l’GPO dans l’archive**

1.  Sous **l’onglet Contrôlé,** cliquez avec le bouton droit sur **MyGPO,** puis cliquez **sur Vérifier.**

2.  Tapez un commentaire, puis cliquez sur **OK.**

3.  Lorsque la fenêtre **Progression de l’AGPM** indique que la progression globale est terminée, cliquez sur **Fermer**. Sous **l’onglet** Contrôlé, l’état de l’GPO est identifié comme **Étant enregistré**.

**Pour demander le déploiement de l’GPO dans l’environnement de production**

1.  Sous **l’onglet Contrôlé,** cliquez avec le bouton droit sur **MyGPO,** puis cliquez sur **Déployer.**

2.  Étant donné que ce compte n’est pas un approuveur ou un administrateur AGPM, vous devez envoyer une demande de déploiement. Pour recevoir une copie de la demande, tapez votre adresse de messagerie dans le **champ Cc.** Tapez un commentaire à afficher dans l’historique de l’GPO, puis cliquez sur **Envoyer.**

3.  Lorsque la fenêtre **Progression de l’AGPM** indique que la progression globale est terminée, cliquez sur **Fermer**. **MyGPO s’affiche** dans la liste des GPO sous **l’onglet En** attente.

### <a name="step-3-review-and-deploy-a-gpo"></a><a href="" id="bkmk-manage3"></a>Étape 3 : Examiner et déployer un GPO

Dans cette étape, vous allez agir en tant qu’approuveur, en créant des rapports et en analysant les paramètres et les modifications apportées aux paramètres dans l’GPO pour déterminer si vous devez les approuver. Après avoir évalué l’objet de stratégie de groupe, vous le déployez dans l’environnement de production et liez l’objet de stratégie de groupe à un domaine ou à une unité d’organisation. L’GPO prend effet lors de l’actualisation de la stratégie de groupe pour les ordinateurs de ce domaine ou de cette ou cette même ou cette même ou même équipe.

**Pour passer en revue les paramètres de l’GPO**

1. Sur un ordinateur sur lequel vous avez installé le client AGPM, connectez-vous avec un compte d’utilisateur auquel est attribué le rôle d’approuveur dans AGPM. Tout administrateur de stratégie de groupe avec le rôle Réviseur, qui est inclus dans tous les autres rôles, peut passer en revue les paramètres d’un GPO.

2. Ouvrez la boîte de réception de messagerie du compte et notez que vous avez reçu un message électronique de l’alias AGPM avec une demande d’éditeur pour déployer un GPO.

3. Dans **l’arborescence de** la Console de gestion des stratégies de groupe, cliquez sur **Modifier** le contrôle dans la forêt et le domaine dans lesquels vous souhaitez gérer les GGP.

4. Sous **l’onglet** Contenu du volet d’informations, cliquez sur **l’onglet En** attente.

5. Double-cliquez sur **MyGPO** pour afficher son historique.

6. Examinez les paramètres de la version la plus récente de MyGPO :

   1.  Dans **** la fenêtre Historique, cliquez avec le bouton droit sur la version de l’GPO dont l’horodat est le plus récent, cliquez sur **Paramètres,** puis sur Rapport **HTML** pour afficher un résumé des paramètres de l’GPO.

   2.  Dans le navigateur Web, cliquez sur **Afficher tout** pour afficher tous les paramètres dans l’GPO. Fermez le navigateur.

7. Comparez la version la plus récente de MyGPO à la première version archivée dans l’archive :

   1. Dans la **fenêtre Historique,** cliquez sur la version de l’GPO avec l’horodat le plus récent. Appuyez sur Ctrl, puis cliquez sur la version la plus ancienne de l’GPO pour laquelle la **version** de l’ordinateur n’est pas **\\***.

   2. Cliquez sur **le bouton Différences.** La section **Stratégies de compte/Stratégie de** mot de passe est mise en surbrillance en vert et précédée **de \[+\]**. Cela indique que le paramètre est configuré uniquement dans la dernière version de l’GPO.

   3. Cliquez sur **Stratégies de compte/Stratégie de mot de passe.** Le **paramètre Longueur** minimale du mot de passe est également mis en surbrillance en vert et précédé de **\[+\],** indiquant qu’il est configuré uniquement dans la dernière version de l’GPO.

   4. Fermez le navigateur Web.

**Pour déployer l’GPO dans l’environnement de production**

1.  Sous **l’onglet En** attente, cliquez avec le bouton droit sur **MyGPO,** puis cliquez sur **Approuver.**

2.  Tapez un commentaire à inclure dans l’historique de l’GPO.

3.  Cliquez sur **Oui**. Lorsque la fenêtre **Progression de l’AGPM** indique que la progression globale est terminée, cliquez sur **Fermer**. L’GPO est déployé dans l’environnement de production.

**Pour lier l’GPO à un domaine ou une unité d’organisation**

1.  Dans la GMC, cliquez avec le bouton droit sur le domaine ou une unité d’organisation à laquelle vous souhaitez appliquer l’GPO que vous avez configuré, puis cliquez sur Lier un **GPO existant.**

2.  Dans la **boîte de dialogue Sélectionner un GPO,** cliquez sur **MyGPO,** puis sur **OK.**

### <a name="step-4-use-a-template-to-create-a-gpo"></a><a href="" id="bkmk-manage4"></a>Étape 4 : Utiliser un modèle pour créer un GPO

Dans cette étape, vous utilisez un compte qui a le rôle Éditeur pour créer et utiliser un modèle. Ce modèle est une version statique d’un GPO à utiliser comme point de départ pour la création de nouveaux objets de groupe. Bien que vous ne pouvez pas modifier un modèle, vous pouvez créer un nouvel GPO basé sur un modèle. Les modèles sont utiles pour créer rapidement plusieurs G STRATÉGIE de groupe qui incluent la plupart des mêmes paramètres de stratégie.

**Pour créer un modèle basé sur un GPO existant**

1.  Sur un ordinateur sur lequel vous avez installé le client AGPM, connectez-vous avec un compte d’utilisateur auquel est attribué le rôle Éditeur dans AGPM.

2.  Dans **l’arborescence de** la Console de gestion des stratégies de groupe, cliquez sur **Modifier** le contrôle dans la forêt et le domaine dans lesquels vous souhaitez gérer les GGP.

3.  Sous **l’onglet** Contenu du volet d’informations, cliquez sur **l’onglet** Contrôlé.

4.  Cliquez avec le bouton droit **** **sur MyGPO,** puis cliquez sur Enregistrer en tant que modèle pour créer un modèle incorporant tous les paramètres actuellement dans MyGPO.

5.  Tapez **MyTemplate comme** nom pour le modèle et un commentaire, puis cliquez sur **OK**.

6.  Lorsque la fenêtre **Progression de l’AGPM** indique que la progression globale est terminée, cliquez sur **Fermer**. Le nouveau modèle apparaît sous **l’onglet Modèles.**

**Pour demander la création et la gestion d’un nouvel GPO via AGPM**

1.  Cliquez sur **l’onglet** Contrôlé.

2.  Cliquez avec le bouton **droit sur le** nœud Contrôle des changements, puis cliquez sur Nouvel **GPO contrôlé.**

3.  Dans la **boîte de dialogue Nouvel GPO** contrôlé :

    1.  Pour recevoir une copie de la demande, tapez votre adresse de messagerie dans le **champ Cc.**

    2.  Tapez **MyOtherGPO** comme nom pour le nouvel GPO.

    3.  Tapez un commentaire pour le nouvel GPO.

    4.  Cliquez **sur Créer en** direct afin que le nouvel GPO soit déployé dans l’environnement de production immédiatement après approbation.

    5.  For **From GPO template,** select **MyTemplate**. Cliquez sur **Envoyer**.

4.  Lorsque la fenêtre **Progression de l’AGPM** indique que la progression globale est terminée, cliquez sur **Fermer**. Le nouvel GPO s’affiche sous **l’onglet En** attente.

Utilisez un compte qui se voit attribuer le rôle d’approuveur pour approuver la demande en attente de création de l’GPO comme vous l’avez fait à l’étape 1 : Créer [un GPO](#bkmk-manage1). MyTemplate intègre tous les paramètres que vous avez configurés dans MyGPO. Étant donné que MyOtherGPO a été créé à l’aide de MyTemplate, il contient d’abord tous les paramètres que MyGPO contenait au moment de la création de MyTemplate. Vous pouvez le confirmer en générant un rapport de différences pour comparer MyOtherGPO à MyTemplate.

**Pour vérifier l’GPO à partir de l’archive pour modification**

1.  Sur un ordinateur sur lequel vous avez installé le client AGPM, connectez-vous avec un compte d’utilisateur auquel est attribué le rôle Éditeur dans AGPM.

2.  Cliquez avec le bouton **droit sur MyOtherGPO,** puis cliquez sur **Check Out**.

3.  Tapez un commentaire à afficher dans l’historique de l’GPO pendant qu’il est extrait, puis cliquez sur **OK**.

4.  Lorsque la fenêtre **Progression de l’AGPM** indique que la progression globale est terminée, cliquez sur **Fermer**. Sous **l’onglet** Contrôlé, l’état de l’GPO est identifié comme **extrait.**

**Pour modifier l’GPO hors connexion et configurer la durée du verrouillage du compte**

1.  Sous **l’onglet** Contrôlé, cliquez avec le bouton droit **** sur **MyOtherGPO,** puis cliquez sur Modifier pour ouvrir la fenêtre Éditeur de gestion des stratégies de groupe et modifier une copie hors connexion de l’GPO. **** Pour ce scénario, configurez la longueur minimale du mot de passe :

    1.  Sous **Configuration ordinateur,** double-cliquez sur **Stratégies,** **Windows Paramètres,** Sécurité **Paramètres,** Stratégies de **compte**et Stratégie de verrouillage **de compte.**

    2.  Dans le volet d’informations, double-cliquez sur **Durée de verrouillage du compte.**

    3.  Dans la fenêtre propriétés, **cochez Définir**ce paramètre de stratégie, définissez la durée sur **30** minutes, puis cliquez sur **OK**.

2.  Fermez la **fenêtre Éditeur de gestion des stratégies de** groupe.

Vérifiez MyOtherGPO dans l’archive et demandez le déploiement comme vous l’avez fait pour MyGPO à l’étape [2 : Modifier un GPO](#bkmk-manage2). Vous pouvez comparer MyOtherGPO à MyGPO ou MyTemplate à l’aide de rapports de différences. Tout compte qui inclut le rôle Réviseur (ADMINISTRATEUR AGPM \[Contrôle total\], Approuver, Éditeur ou Réviseur) peut générer des rapports.

**Pour comparer un GPO à un autre GPO et à un modèle**

1.  Pour comparer MyGPO et MyOtherGPO :

    1.  Sous **l’onglet Contrôlé,** cliquez **sur MyGPO**. Appuyez sur Ctrl, puis cliquez **sur MyOtherGPO**.

    2.  Cliquez avec le bouton **droit sur MyOtherGPO,** pointez sur **Différences,** puis cliquez sur **Rapport HTML.**

2.  Pour comparer MyOtherGPO et MyTemplate :

    1.  Sous **l’onglet Contrôlé,** cliquez **sur MyOtherGPO**.

    2.  Cliquez avec le bouton **droit sur MyOtherGPO,** pointez sur **Différences,** puis cliquez sur **Modèle**.

    3.  Sélectionnez **MyTemplate et** **rapport HTML,** puis cliquez sur **OK.**

### <a name="step-5-delete-and-restore-a-gpo"></a><a href="" id="bkmk-manage5"></a>Étape 5 : Supprimer et restaurer un GPO

Dans cette étape, vous agissez en tant qu’approuveur pour supprimer un GPO.

**Pour supprimer un GPO**

1.  Sur un ordinateur sur lequel vous avez installé le client AGPM, connectez-vous avec un compte d’utilisateur auquel est attribué le rôle d’approuveur.

2.  Dans **l’arborescence de** la Console de gestion des stratégies de groupe, cliquez sur **Modifier** le contrôle dans la forêt et le domaine dans lesquels vous souhaitez gérer les GGP.

3.  Sous **l’onglet** Contenu, cliquez sur **l’onglet** Contrôlé pour afficher les G GPO contrôlés.

4.  Cliquez avec le bouton **droit sur MyGPO,** puis cliquez sur **Supprimer.** Cliquez **sur Supprimer un GPO de l’archive** et de la production pour supprimer la version dans l’archive et la version déployée de l’GPO dans l’environnement de production.

5.  Tapez un commentaire à afficher dans la piste d’audit de l’objet de groupe, puis cliquez sur **OK.**

6.  Lorsque la fenêtre **Progression de l’AGPM** indique que la progression globale est terminée, cliquez sur **Fermer**. L’GPO est supprimé **** de l’onglet Contrôlé **** et s’affiche sous l’onglet Corbeille, où il peut être restauré ou détruit.

Vous pouvez parfois découvrir après la suppression d’un GPO qu’il est toujours nécessaire. Dans cette étape, vous agissez en tant qu’approuveur pour restaurer un GPO qui a été supprimé.

**Pour restaurer un GPO supprimé**

1.  Sous **l’onglet** Contenu, cliquez sur **l’onglet Corbeille** pour afficher les objets de groupe supprimés.

2.  Cliquez avec le bouton **droit sur MyGPO,** puis cliquez sur **Restaurer.**

3.  Tapez un commentaire à afficher dans l’historique de l’GPO, puis cliquez sur **OK**.

4.  Lorsque la fenêtre **Progression de l’AGPM** indique que la progression globale est terminée, cliquez sur **Fermer**. L’GPO est supprimé de l’onglet **Corbeille** et s’affiche sous **l’onglet** Contrôlé.

    **Remarque**  
    La restauration d’un GPO dans l’archive ne le redéployera pas automatiquement dans l’environnement de production. Pour renvoyer l’GPO dans l’environnement de production, déployez l’GPO comme à l’étape 3 : Examiner [et déployer un GPO](#bkmk-manage3).

     

Après avoir modifié et déployé un GPO, vous pouvez découvrir que les modifications récentes apportées à l’GPO sont à l’origine d’un problème. Dans cette étape, vous agirez en tant qu’approuveur pour revenir à une version antérieure de l’GPO. Vous pouvez revenir à n’importe quelle version de l’historique de l’GPO. Vous pouvez utiliser des commentaires et des étiquettes pour identifier les bonnes versions connues et le moment où des modifications spécifiques ont été apportées.

**Pour revenir à une version antérieure d’un GPO**

1.  Sous **l’onglet** Contenu, cliquez sur **l’onglet** Contrôlé pour afficher les G GPO contrôlés.

2.  Double-cliquez sur **MyGPO** pour afficher son historique.

3.  Cliquez avec le bouton droit sur la version à déployer, **cliquez**sur Déployer, puis cliquez sur **Oui**.

4.  Lorsque la **fenêtre Progression** indique que la progression globale est terminée, cliquez sur **Fermer.** Dans la **fenêtre Historique,** cliquez sur **Fermer.**

    **Remarque**  
    Pour vérifier que la version qui a été redéployée est la version prévue, examinez un rapport de différences pour les deux versions. Dans la **fenêtre** Historique de l’GPO, sélectionnez les deux versions, cliquez dessus avec le bouton droit, pointez sur **Différence,** puis cliquez sur Rapport **HTML** ou **Rapport XML.**

     

 

 





