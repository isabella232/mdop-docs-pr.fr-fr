---
title: Guide pas à pas de la Gestion avancée des stratégies de groupe Microsoft4.0
description: Guide pas à pas de la Gestion avancée des stratégies de groupe Microsoft4.0
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
ms.openlocfilehash: 819d536451095d23080115799016aa0ac5242dee
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808210"
---
# Guide pas à pas de la Gestion avancée des stratégies de groupe Microsoft4.0


Ce guide pas à pas décrit les techniques avancées de gestion de la stratégie de groupe qui utilisent la console de gestion des stratégies de groupe (GPMC) et Microsoft Advanced Group Policy Management (AGPM). AGPM augmente les capacités de la console de gestion des stratégies de GPMC et fournit les éléments suivants:

-   Rôles standard pour la délégation d’autorisations pour gérer les objets de stratégie de groupe à plusieurs administrateurs de stratégie de groupe, en plus de la possibilité de déléguer l’accès aux objets de stratégie de groupe dans l’environnement de production.

-   Archive permettant aux administrateurs de stratégie de groupe de créer et de modifier des objets de stratégie de groupe hors ligne avant leur déploiement dans un environnement de production.

-   La possibilité de revenir à une version antérieure d’un objet de stratégie de groupe dans l’archive et de limiter le nombre de versions stockées dans l’archive;

-   Les fonctionnalités d’archivage et d’extraction des objets de stratégie de groupe vous permettent de vous assurer que les administrateurs de stratégie de groupe n’écrasent pas involontairement leurs tâches.

-   La possibilité de rechercher des objets de stratégie de groupe avec des attributs spécifiques et de filtrer la liste des objets de stratégie de groupe affichés.

## Vue d’ensemble du scénario AGPM


Pour ce scénario, vous allez utiliser un compte d’utilisateur distinct pour chaque rôle dans AGPM et montrer comment la stratégie de groupe peut être gérée dans un environnement doté de plusieurs administrateurs de stratégie de groupe disposant de différents niveaux d’autorisation. Plus précisément, vous devez effectuer les tâches suivantes:

-   À l’aide d’un compte membre du groupe administrateurs de domaine, installez le serveur AGPM et attribuez le rôle d’administrateur AGPM à un compte ou à un groupe.

-   À l’aide des comptes auxquels vous allez attribuer des rôles AGPM, installez le client AGPM.

-   À l’aide d’un compte ayant le rôle d’administrateur AGPM, configurez l’accès AGPM et de délégué aux objets de stratégie de groupe en attribuant des rôles à d’autres comptes.

-   À partir d’un compte ayant le rôle d’éditeur, demandez qu’un nouvel objet de stratégie de groupe soit créé et approuvé par le biais d’un compte doté du rôle Approbateur. Utiliser le compte de l’éditeur pour extraire l’objet de stratégie de groupe de l’archive, modifier l’objet de stratégie de groupe, archiver l’objet de stratégie de groupe dans l’archive, puis demander le déploiement.

-   À l’aide d’un compte doté du rôle Approbateur, passez en revue l’objet de stratégie de groupe et déployez-le dans votre environnement de production.

-   À l’aide d’un compte doté du rôle d’éditeur, créez un modèle d’objet de stratégie de groupe et utilisez-le comme point de départ pour créer un nouvel objet de stratégie de groupe.

-   À l’aide d’un compte doté du rôle Approbateur, supprimez et restaurez un objet de stratégie de groupe.

![processus de développement d’objets de stratégie de groupe](images/ab77a1f3-f430-4e7d-be58-ee8f9bd1140e.gif)

## Configuration requise


Les ordinateurs sur lesquels vous souhaitez installer AGPM doivent respecter les exigences suivantes et vous devez créer des comptes à utiliser dans ce scénario.

**Remarques**  Si AGPM 2,5 est installé et que vous effectuez une mise à niveau de Windows Server® 2003 vers Windows Server2008R2 ou Windows Server 2008, ou si vous effectuez une mise à niveau à partir d’Vista sans Service Pack d’Vista et de® avec Service Pack1 (SP1), vous devez mettre à niveau le système d’exploitation avant de procéder à la mise à niveau vers AGPM 4.0.

Si AGPM 3,0 est installé, vous ne devez pas mettre à niveau le système d’exploitation avant de procéder à la mise à niveau vers AGPM 4,0

 

Dans un environnement mixte incluant des systèmes d’exploitation plus récents et plus anciens, il existe certaines limitations aux fonctionnalités, comme indiqué dans le tableau suivant.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Système d’exploitation sur lequel un serveur AGPM 4,0 est exécuté</th>
<th align="left">Système d’exploitation sur lequel le client AGPM 4,0 s’exécute</th>
<th align="left">État de la prise en charge d’AGPM 4,0</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows Server2008R2 ou Windows.</p></td>
<td align="left"><p>Windows Server2008R2 ou Windows.</p></td>
<td align="left"><p>Pris en charge</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008R2 ou Windows.</p></td>
<td align="left"><p>Windows Server 2008 ou Windows Vista avec SP1</p></td>
<td align="left"><p>Pris en charge, mais ne peut pas modifier les paramètres de stratégie ou les éléments de préférence qui existent uniquement dans Windows Server2008R2 ou la touche Windows</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2008 ou Windows Vista avec SP1</p></td>
<td align="left"><p>Windows Server2008R2 ou Windows.</p></td>
<td align="left"><p>Non pris en charge</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2008 ou Windows Vista avec SP1</p></td>
<td align="left"><p>Windows Server 2008 ou Windows Vista avec SP1</p></td>
<td align="left"><p>Pris en charge, mais il est impossible de signaler ou de modifier des paramètres de stratégie ou des éléments de préférence qui existent uniquement dans Windows Server2008R2 ou une icône</p></td>
</tr>
</tbody>
</table>

 

### Configuration requise pour le serveur AGPM

Pour AGPM Server 4.0, vous avez besoin de Windows Server2008R2, Windows Server 2008, de la fonction de GPMC et de la console de gestion des logiciels distants (RSAT) ou Windows Vista avec SP1 et de la console GPMC de RSAT. Les versions 32 bits et 64 bits sont prises en charge.

Avant d’installer le serveur AGPM, vous devez être membre du groupe administrateurs de domaine et les fonctionnalités Windows suivantes doivent être présentes sauf indication contraire:

-   GESTION

    -   Windows Server2008R2 ou Windows Server 2008: si le GPMC n’est pas présent, il est automatiquement installé par AGPM.

    -   -Vous: vous devez installer la console de gestion des stratégies de l’installation à partir du RSAT avant d’installer AGPM. Pour plus d’informations, reportez-vous à la rubrique [Outils d’administration de serveur distant pour Windows 7](https://go.microsoft.com/fwlink/?LinkID=131280) ( https://go.microsoft.com/fwlink/?LinkID=131280) .

    -   Windows Vista avec Service Pack 1: vous devez installer la console de gestion des stratégies de l’installation à partir de RSAT avant d’installer AGPM. Pour plus d’informations, reportez-vous à la rubrique [Outils d’administration de serveur distant pour Windows Vista avec Service Pack 1](https://go.microsoft.com/fwlink/?LinkID=116179) ( https://go.microsoft.com/fwlink/?LinkID=116179) .

-   .NET Framework 3,5 ou versions ultérieures

    -   Windows Server2008R2 ou une version d’Outlook: si .NET Framework 3,5 ou version ultérieure n’est pas présent, le .NET Framework 3,5 est automatiquement installé par AGPM.

    -   Windows Server 2008 ou Windows Vista avec Service Pack 1: vous devez installer .NET Framework 3,5 ou une version ultérieure avant d’installer AGPM.

Les fonctionnalités Windows suivantes sont requises par le serveur AGPM et sont installées automatiquement s’ils ne sont pas présents:

-   Activation WCF; Activation non HTTP

-   Service d'activation des processus Windows

    -   Modèle de processus

    -   Environnement .NET

    -   API de configuration

### Configuration requise pour le client AGPM

Le client d’AGPM est requis pour Windows Server2008R2, Windows Server 2008, la version 4 et la console GPMC de RSAT ou Windows Vista avec SP1 et la console de gestion des stratégies de poste de poste. Les versions 32 bits et 64 bits sont prises en charge. Le client AGPM peut être installé sur un ordinateur exécutant AGPM Server.

Les fonctionnalités Windows suivantes sont requises par le client AGPM et, sauf indication contraire, si elles ne sont pas installées, procédez comme suit:

-   GESTION

    -   Windows Server2008R2 ou Windows Server 2008: si le GPMC n’est pas présent, il est automatiquement installé par AGPM.

    -   -Vous: vous devez installer la console de gestion des stratégies de l’installation à partir du RSAT avant d’installer AGPM. Pour plus d’informations, reportez-vous à la rubrique [Outils d’administration de serveur distant pour Windows 7](https://go.microsoft.com/fwlink/?LinkID=131280) ( https://go.microsoft.com/fwlink/?LinkID=131280) .

    -   Windows Vista avec Service Pack 1: vous devez installer la console de gestion des stratégies de l’installation à partir de RSAT avant d’installer AGPM. Pour plus d’informations, reportez-vous à la rubrique [Outils d’administration de serveur distant pour Windows Vista avec Service Pack 1](https://go.microsoft.com/fwlink/?LinkID=116179) ( https://go.microsoft.com/fwlink/?LinkID=116179) .

-   .NET Framework 3,0 ou version ultérieure

    -   Windows Server2008R2 ou une version d’Outlook: si .NET Framework 3,0 ou version ultérieure n’est pas présent, le .NET Framework 3,5 est automatiquement installé par AGPM.

    -   Windows Server 2008 ou Windows Vista avec Service Pack 1: si .NET Framework 3,0 ou version ultérieure n’est pas présent, le .NET Framework 3,0 est automatiquement installé par AGPM.

### Exigences de scénarios

Avant de commencer ce scénario, vous devez créer quatre comptes d’utilisateurs. Pendant le scénario, vous devez attribuer l’un des rôles AGPM suivants à chacun de ces comptes: Administrateur AGPM (contrôle total), approbateur, éditeur et relecteur. Ces comptes doivent être en mesure d’envoyer et de recevoir des messages électroniques. Attribution d’autorisations d’accès aux **objets liés** aux comptes disposant des rôles d’administrateur AGPM, approbateur et (facultatif).

**Remarques** 
 L’autorisation **lier les objets de stratégie de groupe** est affectée par défaut aux membres des administrateurs de domaine et des administrateurs d’entreprise. Pour affecter des autorisations d’accès de l’utilisateur à des utilisateurs ou des groupes supplémentaires (par exemple, des comptes ayant le rôle d’administrateur ou d’approbation AGPM), cliquez sur le nœud du domaine, cliquez sur l’onglet **délégation** , sélectionnez **lier les objets de stratégie de groupe**, cliquez sur **Ajouter**, puis sélectionnez les utilisateurs ou groupes auxquels vous voulez accorder **l’autorisation.**

 

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

4.  Dans la boîte de dialogue **termes du contrat de licence logiciel Microsoft** , acceptez les termes, puis cliquez sur **suivant**.

5.  Dans la boîte de dialogue Path de l' **application** , sélectionnez un emplacement pour installer le serveur AGPM. L’ordinateur sur lequel le serveur AGPM est installé doit héberger le service AGPM et gérer l’archive. Cliquez sur **Suivant**.

6.  Dans la boîte de dialogue **path Archive** , sélectionnez un emplacement pour l’Archive par rapport au serveur AGPM. Le chemin d’accès d’archive peut pointer vers un dossier sur le serveur AGPM ou ailleurs. Toutefois, vous devez sélectionner un emplacement disposant d’un espace suffisant pour stocker tous les objets de stratégie de groupe et les données d’historique gérés par ce serveur AGPM. Cliquez sur **Suivant**.

7.  Dans la boîte de dialogue **compte de service AGPM** , sélectionnez un compte de service sous lequel le service AGPM sera exécuté, puis cliquez sur **suivant**.

    Ce compte doit être membre du groupe Domain Admins ou, pour une configuration de privilèges minimum, les groupes suivants dans chaque domaine géré par le serveur AGPM:

    -   Propriétaires de la stratégie de groupe

    -   Opérateurs de sauvegarde

    Par ailleurs, ce compte nécessite une autorisation contrôle total pour les dossiers suivants:

    -   Le dossier d’archive AGPM pour lequel cette autorisation est accordée automatiquement lors de l’installation d’AGPM Server s’il est installé sur un disque local.

    -   Le dossier temporaire du système local, généralement%windir%\\temp.

8.  Dans la boîte de dialogue **Archiver le propriétaire** , sélectionnez un compte ou un groupe auquel vous attribuez le rôle d’administrateur AGPM (contrôle total). Les administrateurs d’AGPM peuvent attribuer des rôles et autorisations d’AGPM aux autres administrateurs de stratégie de groupe, afin que vous puissiez affecter le rôle d’administrateur AGPM aux administrateurs de stratégie de groupe supplémentaires. Pour ce scénario, sélectionnez le compte que vous voulez faire dans le rôle administrateur d’AGPM. Cliquez sur **Suivant**.

9.  Dans la boîte de dialogue **configuration du port** , tapez un port sur lequel le service AGPM doit écouter. Ne désactivez pas la case à cocher **Ajouter une exception de port à un pare-feu** sauf si vous configurez manuellement les exceptions de port ou utilisez des règles pour configurer les exceptions de port Cliquez sur **Suivant**.

10. Dans la boîte de dialogue **langues** , sélectionnez une ou plusieurs langues d’affichage à installer pour le serveur AGPM.

11. Cliquez sur **installer**, puis cliquez sur **Terminer** pour quitter l’Assistant installation.

    **Attention**  Ne modifiez pas les paramètres du service AGPM via les outils et **services** **d’administration** du système d’exploitation. Cela peut empêcher le démarrage du service AGPM. Pour plus d’informations sur la modification des paramètres du service, voir aide pour la gestion avancée des stratégies de groupe.

     

### <a href="" id="bkmk-config2"></a>Étape 2: installer le client AGPM

Chaque administrateur de stratégie de groupe (qui crée, modifie, déploie, révise ou supprime des objets de stratégie de groupe) doit disposer d’un client AGPM sur les ordinateurs qu’il utilise pour gérer les objets de stratégie de groupe. Le nœud de contrôle de modification, qui vous permet d’effectuer de nombreuses tâches de gestion d’objets de stratégie de groupe, s’affiche dans la console de gestion des stratégies de groupe uniquement si vous installez le client AGPM. Pour ce scénario, vous installez le client AGPM sur au moins un ordinateur. Vous n’avez pas besoin d’installer le client AGPM sur les ordinateurs des utilisateurs finaux qui n’effectuent pas d’administration de la stratégie de groupe.

**Pour installer le client AGPM sur l’ordinateur d’un administrateur de stratégie de groupe**

1.  Démarrez le CD-ROM Microsoft Desktop Optimization Pack et suivez les instructions à l’écran pour sélectionner **Advanced Group Management Policy-client**.

2.  Dans la boîte de dialogue **Bienvenue** , cliquez sur **suivant**.

3.  Dans la boîte de dialogue **termes du contrat de licence logiciel Microsoft** , acceptez les termes, puis cliquez sur **suivant**.

4.  Dans la boîte de dialogue Path de l' **application** , sélectionnez un emplacement pour installer le client AGPM. Cliquez sur **Suivant**.

5.  Dans la boîte de dialogue **serveur AGPM** , tapez le nom DNS ou l’adresse IP du serveur AGPM et le port auquel vous voulez vous connecter. Le port par défaut du service AGPM est 4600. Ne désactivez pas la case à cocher **autoriser Microsoft Management Console via le pare-feu** sauf si vous configurez manuellement les exceptions de port ou utilisez des règles pour configurer les exceptions de port. Cliquez sur **Suivant**.

6.  Dans la boîte de dialogue **langues** , sélectionnez une ou plusieurs langues d’affichage à installer pour le client AGPM.

7.  Cliquez sur **installer**, puis cliquez sur **Terminer** pour quitter l’Assistant installation.

### <a href="" id="bkmk-config3"></a>Étape 3: configurer une connexion de serveur AGPM

AGPM stocke toutes les versions de chaque objet de stratégie de groupe contrôlé (GPO), c’est-à-dire, chaque GPO pour lequel AGPM fournit le contrôle des modifications, dans une archive centrale. Cela permet aux administrateurs de stratégie de groupe d’afficher et de modifier les objets de stratégie de groupe hors connexion sans affecter immédiatement la version déployée de chaque GPO.

Dans cette étape, vous configurez une connexion de serveur AGPM et assurez-vous que tous les administrateurs de stratégie de groupe se connectent au même serveur AGPM. (Pour plus d’informations sur la configuration de plusieurs serveurs AGPM, voir aide pour la gestion avancée des stratégies de groupe.)

**Pour configurer une connexion de serveur AGPM pour tous les administrateurs de stratégie de groupe**

1.  Sur un ordinateur sur lequel vous avez installé un client AGPM, connectez-vous à l’aide du compte d’utilisateur que vous avez sélectionné comme propriétaire d’archive. Cet utilisateur a le rôle d’administrateur AGPM (contrôle total).

2.  Cliquez sur **Démarrer**, pointez sur **Outils d’administration**, puis cliquez sur gestion de la **stratégie de groupe** pour ouvrir la console GPMC.

3.  Modification d’un objet de stratégie de groupe qui est appliqué à tous les administrateurs de stratégie de groupe.

4.  Dans la fenêtre de l' **éditeur de gestion des stratégies de groupe** , double-cliquez sur **Configuration utilisateur**, **stratégies**, **modèles d’administration**, **composants Windows**et **AGPM**.

5.  Dans le volet Détails, double-cliquez sur **AGPM: spécifiez le serveur AGPM par défaut (tous les domaines)**.

6.  Dans la fenêtre **Propriétés** , sélectionnez **activé** , puis entrez le nom DNS ou l’adresse IP et le port (par exemple, **Server.contoso.com:4600**) du serveur qui héberge l’archive. Par défaut, le service AGPM utilise le port 4600.

7.  Cliquez sur **OK**, puis fermez la fenêtre **éditeur de gestion des stratégies de groupe** . Lorsque la stratégie de groupe est mise à jour, la connexion au serveur AGPM est configurée pour chaque administrateur de stratégie de groupe.

### <a href="" id="bkmk-config4"></a>Étape 4: configurer les notifications par courrier électronique

En tant qu’administrateur AGPM (contrôle total), vous désignez les adresses de courrier des approbateurs et des administrateurs AGPM auxquels un message électronique contenant une demande est envoyé lorsqu’un éditeur tente de créer, de déployer ou de supprimer un objet de stratégie de groupe. Vous déterminez également l’alias à partir duquel ces messages sont envoyés.

**Pour configurer les notifications par courrier électronique pour AGPM**

1.  Dans l' **éditeur de gestion des stratégies de groupe** , accéder au dossier de contrôle de **modification** 

2.  Dans le volet Détails, cliquez sur l’onglet **délégation de domaine** .

3.  Dans le champ **à partir de l’adresse de messagerie** , entrez l’adresse de messagerie d’AGPM à partir de laquelle les notifications doivent être envoyées.

4.  Dans le champ **adresse de messagerie** , entrez l’adresse de messagerie du compte d’utilisateur auquel vous souhaitez attribuer le rôle d’approbateur.

5.  Dans le champ **serveur SMTP** , tapez un serveur de messagerie SMTP valide.

6.  Dans les champs **nom d’utilisateur** et **mot de passe** , tapez les informations d’identification d’un utilisateur qui a accès au service SMTP. Cliquez sur **Apply** (Appliquer).

### <a href="" id="bkmk-config5"></a>Étape 5: accès délégué

En tant qu’administrateur AGPM (contrôle total), vous déléguez l’accès au niveau du domaine aux objets de stratégie de groupe, en attribuant des rôles au compte de chaque administrateur de stratégie de groupe.

**Remarques**  Vous pouvez également déléguer l’accès au niveau de l’objet GPO plutôt qu’au niveau du domaine. Pour plus d’informations, voir aide pour la gestion avancée des stratégies de groupe.

 

**Important**  Vous devez limiter l’appartenance au groupe de propriétaires de la stratégie de groupe afin qu’elle ne puisse pas être utilisée pour contourner la gestion d’AGPM d’Access aux objets de stratégie de groupe. (Dans la **console de gestion des stratégies de groupe**, cliquez sur **objets de stratégie de groupe** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe, cliquez sur **délégation**, puis configurez les paramètres en fonction des besoins de votre organisation.)

 

**Pour déléguer l’accès à tous les objets de stratégie de groupe dans un domaine**

1.  Dans l’onglet **délégation de domaine** , cliquez sur le bouton **Ajouter** , sélectionnez le compte d’utilisateur de l’administrateur de stratégie de groupe comme approbateur, puis cliquez sur **OK**.

2.  Dans la boîte de dialogue **Ajouter un groupe ou un utilisateur** , sélectionnez le rôle **approbateur** pour attribuer le rôle au compte, puis cliquez sur **OK**. (Ce rôle inclut le rôle de réviseur.)

3.  Cliquez sur le bouton **Ajouter** , sélectionnez le compte d’utilisateur de l’administrateur de stratégie de groupe pour faire office d’éditeur, puis cliquez sur **OK**.

4.  Dans la boîte de dialogue **Ajouter un groupe ou un utilisateur** , sélectionnez le rôle d' **éditeur** pour attribuer le rôle au compte, puis cliquez sur **OK**. (Ce rôle inclut le rôle de réviseur.)

5.  Cliquez sur le bouton **Ajouter** , sélectionnez le compte d’utilisateur de l’administrateur de stratégie de groupe pour qu’il serve de relecteur, puis cliquez sur **OK**.

6.  Dans la boîte de dialogue **Ajouter un groupe ou un utilisateur** , sélectionnez le rôle de **réviseur** pour affecter uniquement ce rôle au compte.

## Procédure de gestion des objets de stratégie de groupe


Vous devez effectuer les étapes suivantes pour créer, modifier, réviser et déployer des objets de stratégie de groupe à l’aide d’AGPM. Par ailleurs, vous allez créer un modèle, supprimer un objet de stratégie de groupe, puis restaurer un objet GPO supprimé.

[Étape 1: créer un objet de stratégie de groupe](#bkmk-manage1)

[Étape 2: modifier un objet de stratégie de groupe](#bkmk-manage2)

[Étape 3: vérifier et déployer un objet de stratégie de groupe](#bkmk-manage3)

[Étape 4: utiliser un modèle pour créer un objet de stratégie de groupe](#bkmk-manage4)

[Étape 5: supprimer et restaurer un objet de stratégie de groupe](#bkmk-manage5)

### <a href="" id="bkmk-manage1"></a>Étape 1: créer un objet de stratégie de groupe

Dans un environnement doté de plusieurs administrateurs de stratégie de groupe, les utilisateurs dotés du rôle d’éditeur peuvent demander la création de nouveaux objets de stratégie de groupe. Toutefois, cette demande doit être approuvée par une personne ayant le rôle d’approbateur.

Dans cette étape, vous utilisez un compte qui est le rôle d’éditeur pour demander la création d’un nouvel objet de stratégie de groupe. À l’aide d’un compte ayant le rôle d’approbateur, vous approuvez cette demande de création de l’objet de stratégie de groupe.

**Pour demander la création et la gestion d’un objet de stratégie de groupe via AGPM**

1.  Sur un ordinateur sur lequel vous avez installé un client AGPM, connectez-vous à l’aide d’un compte d’utilisateur auquel est attribué le rôle d’éditeur dans AGPM.

2.  Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.

3.  Cliquez avec le bouton droit sur le nœud de **contrôle de modification** , puis cliquez sur **nouvel objet de stratégie de**contrôle.

4.  Dans la boîte de dialogue **nouvel objet GPO contrôlé** :

    1.  Pour recevoir une copie de la demande, tapez votre adresse de messagerie dans le champ **CC** .

    2.  Tapez **MyGPO** comme nom du nouvel objet de stratégie de groupe.

    3.  Tapez un commentaire pour le nouvel objet de stratégie de groupe.

    4.  Cliquez sur **créer en temps réel** pour que le nouvel objet GPO soit déployé sur l’environnement de production immédiatement après approbation. Cliquez sur **Envoyer**.

5.  Lorsque la fenêtre de **progression d’AGPM** indique la progression globale de l’opération, cliquez sur **Fermer**. Le nouvel objet GPO est affiché dans l’onglet **en attente** .

**Pour approuver la demande en attente de création d’un objet de stratégie de groupe**

1.  Sur un ordinateur sur lequel vous avez installé un client AGPM, connectez-vous avec un compte d’utilisateur ayant le rôle d’approbateur dans AGPM.

2.  Ouvrez la boîte de réception de votre compte et notez que vous avez reçu un message électronique de l’alias AGPM avec la demande de l’éditeur pour créer un objet de stratégie de groupe.

3.  Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.

4.  Dans l’onglet **contenu** , cliquez sur l’onglet **en attente** pour afficher les objets de stratégie de groupe en attente.

5.  Cliquez avec le bouton droit sur **MyGPO**, puis cliquez sur **approuver**.

6.  Cliquez sur **Oui** pour confirmer l’approbation et déplacez l’objet GPO sur l’onglet **contrôlé** .

### <a href="" id="bkmk-manage2"></a>Étape 2: modifier un objet de stratégie de groupe

Vous pouvez utiliser les objets de stratégie de groupe pour configurer les paramètres de l’ordinateur ou de l’utilisateur et les déployer sur de nombreux ordinateurs ou utilisateurs. Dans cette étape, vous utilisez un compte qui est le rôle d’éditeur permettant d’extraire un objet de stratégie de groupe de l’archive, de modifier l’objet de stratégie de groupe en mode hors connexion, de vérifier l’objet GPO modifié dans l’archive et de demander le déploiement de l’objet de stratégie de groupe dans l’environnement de production. Pour ce scénario, vous devez configurer un paramètre dans l’objet de stratégie de groupe pour exiger que le mot de passe comporte au moins huit caractères.

**Pour extraire l’objet de stratégie de groupe de l’archive en vue de le modifier**

1.  Sur un ordinateur sur lequel vous avez installé un client AGPM, connectez-vous avec un compte d’utilisateur ayant le rôle d’éditeur dans AGPM.

2.  Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.

3.  Dans l’onglet **contenu** du volet Détails, cliquez sur l’onglet **contrôlé** pour afficher les objets de stratégie de groupe contrôlés.

4.  Cliquez avec le bouton droit sur **MyGPO**, puis cliquez sur **extraire**.

5.  Tapez un commentaire à afficher dans l’historique de l’objet de stratégie de groupe lors de son extraction, puis cliquez sur **OK**.

6.  Lorsque la fenêtre de **progression d’AGPM** indique la progression globale de l’opération, cliquez sur **Fermer**. Dans l’onglet **contrôlé** , l’état de l’objet de stratégie de groupe est identifié comme **extrait**.

**Pour modifier l’objet de stratégie de groupe hors connexion et configurer la longueur de mot de passe minimum**

1.  Dans l’onglet **contrôlé** , cliquez avec le bouton droit sur **MyGPO**, puis cliquez sur **modifier** pour ouvrir la fenêtre Éditeur de gestion des stratégies de groupe et changer une copie hors connexion de l’objet de stratégie de **groupe** . Pour ce scénario, configurez la longueur minimale du mot de passe:

    1.  Sous **Configuration ordinateur**, double-cliquez sur **stratégies**, **Paramètres Windows**, **paramètres de sécurité**, stratégies de **compte**et **stratégie de mot de passe**.

    2.  Dans le volet Détails, double-cliquez sur **longueur minimale du mot de passe**.

    3.  Dans la fenêtre Propriétés, activez la case à cocher **définir ce paramètre de stratégie** , définissez le nombre de caractères sur **8**, puis cliquez sur **OK**.

2.  Fermez la fenêtre de l' **éditeur de gestion des stratégies de groupe** .

**Pour archiver l’objet de stratégie de groupe dans l’archive**

1.  Dans l’onglet **contrôlé** , cliquez avec le bouton droit sur **MyGPO** , puis cliquez sur **Archiver**.

2.  Tapez un commentaire, puis cliquez sur **OK**.

3.  Lorsque la fenêtre de **progression d’AGPM** indique la progression globale de l’opération, cliquez sur **Fermer**. Dans l’onglet **contrôlé** , l’état de l’objet de stratégie de groupe est identifié comme **Archivé**.

**Pour demander le déploiement de l’objet de stratégie de groupe dans l’environnement de production**

1.  Dans l’onglet **contrôlé** , cliquez avec le bouton droit sur **MyGPO** , puis cliquez sur **déployer**.

2.  Dans la mesure où ce compte n’est pas un approbateur ou un administrateur AGPM, vous devez fournir une demande de déploiement. Pour recevoir une copie de la demande, tapez votre adresse de messagerie dans le champ **CC** . Tapez un commentaire à afficher dans l’historique de l’objet de stratégie de groupe, puis cliquez sur **valider**.

3.  Lorsque la fenêtre de **progression d’AGPM** indique la progression globale de l’opération, cliquez sur **Fermer**. **MyGPO** s’affiche dans la liste des objets de stratégie de groupe sous l’onglet **en attente** .

### <a href="" id="bkmk-manage3"></a>Étape 3: vérifier et déployer un objet de stratégie de groupe

Dans le cadre de cette étape, vous agissez en tant qu’approbateur, vous créez des rapports et vous analysez les paramètres et les modifications apportées aux paramètres dans l’objet de stratégie de groupe pour déterminer s’ils doivent être approuvés. Après avoir évalué l’objet de stratégie de groupe, vous le déployez dans l’environnement de production et le liez à un domaine ou à une unité d’organisation (UO). L’objet GPO est appliqué lorsque la stratégie de groupe est actualisée pour les ordinateurs de ce domaine ou UO.

**Pour vérifier les paramètres de l’objet de stratégie de groupe**

1. Sur un ordinateur sur lequel vous avez installé un client AGPM, connectez-vous à l’aide d’un compte d’utilisateur affecté du rôle d’approbateur dans AGPM. Tout administrateur de stratégie de groupe avec le rôle relecteur, qui est inclus dans tous les autres rôles, peut consulter les paramètres d’un objet de stratégie de groupe.

2. Ouvrez la boîte de réception du compte et notez que vous avez reçu un message électronique de l’alias AGPM avec une demande d’éditeur pour le déploiement d’un objet de stratégie de groupe.

3. Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.

4. Dans l’onglet **contenu** du volet Détails, cliquez sur l’onglet **en attente** .

5. Double-cliquez sur **MyGPO** pour afficher son historique.

6. Passez en revue les paramètres dans la version la plus récente de MyGPO:

   1.  Dans la fenêtre **historique** , cliquez avec le bouton droit sur la version de l’objet de stratégie de groupe avec le cachet d’heure le plus récent, cliquez sur **paramètres**, puis sur **rapport HTML** pour afficher un résumé des paramètres de l’objet de stratégie de groupe.

   2.  Dans le navigateur Web, cliquez sur **Afficher tout** pour afficher tous les paramètres de l’objet de stratégie de groupe. Fermez le navigateur.

7. Comparez la version la plus récente de MyGPO à la première version archivée dans l’archive:

   1. Dans la fenêtre **historique** , cliquez sur la version de l’objet de stratégie de groupe avec le cachet d’heure le plus récent. Maintenez la touche CTRL enfoncée, puis cliquez sur la plus ancienne version d’objet de stratégie de groupe pour laquelle la version de l' **ordinateur** n’est pas * *.

   2. Cliquez sur le bouton **différences** . La section **stratégies de compte/stratégie de mot de passe** est mise en évidence en vert et précédée par **\ [+ \]**. Cela indique que le paramètre est configuré uniquement dans la dernière version de l’objet de stratégie de groupe.

   3. Cliquez sur **stratégies de compte/stratégie de mot de passe**. Le paramètre de **longueur minimum du mot de passe** est également mis en surbrillance en vert et précédé de **\ [+ \]** indiquant qu’il est configuré uniquement dans la dernière version de l’objet de stratégie de groupe.

   4. Fermez le navigateur Web.

**Pour déployer l’objet de stratégie de groupe dans l’environnement de production**

1.  Dans l’onglet **en attente** , cliquez avec le bouton droit sur **MyGPO** , puis cliquez sur **approuver**.

2.  Tapez un commentaire à inclure dans l’historique de l’objet de stratégie de groupe.

3.  Cliquez sur **Oui**. Lorsque la fenêtre de **progression d’AGPM** indique la progression globale de l’opération, cliquez sur **Fermer**. L’objet de stratégie de groupe est déployé dans l’environnement de production.

**Pour lier l’objet de stratégie de groupe à un domaine ou une unité d’organisation**

1.  Dans la console de gestion des stratégies de groupe, cliquez avec le bouton droit sur le domaine ou l’unité d’organisation auquel vous voulez appliquer l’objet de stratégie de groupe que vous avez configuré, puis cliquez sur **lier un objet de stratégie de groupe existant**.

2.  Dans la boîte de dialogue **Sélectionner un objet GPO** , cliquez sur **MyGPO**, puis cliquez sur **OK**.

### <a href="" id="bkmk-manage4"></a>Étape 4: utiliser un modèle pour créer un objet de stratégie de groupe

Dans cette étape, vous utilisez un compte doté du rôle d’éditeur pour créer et utiliser un modèle. Ce modèle est une version statique d’un objet de stratégie de groupe à utiliser comme point de départ pour la création de nouveaux objets de stratégie de groupe. Même si vous ne pouvez pas modifier un modèle, vous pouvez créer un nouvel objet de stratégie de groupe basé sur un modèle. Les modèles permettent de créer rapidement plusieurs objets de stratégie de groupe qui incluent un grand nombre des mêmes paramètres de stratégie.

**Pour créer un modèle sur la base d’un objet de stratégie de groupe existant**

1.  Sur un ordinateur sur lequel vous avez installé un client AGPM, connectez-vous à l’aide d’un compte d’utilisateur auquel le rôle d’éditeur est attribué dans AGPM.

2.  Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.

3.  Dans l’onglet **contenu** du volet Détails, cliquez sur l’onglet **contrôlé** .

4.  Cliquez avec le bouton droit sur **MyGPO**, puis cliquez sur **enregistrer en tant que modèle** pour créer un modèle contenant tous les paramètres actuellement dans MyGPO.

5.  Tapez **MyTemplate** comme nom pour le modèle et un commentaire, puis cliquez sur **OK**.

6.  Lorsque la fenêtre de **progression d’AGPM** indique la progression globale de l’opération, cliquez sur **Fermer**. Le nouveau modèle s’affiche sous l’onglet **modèles** .

**Pour demander la création et la gestion d’un objet de stratégie de groupe via AGPM**

1.  Cliquez sur l’onglet **contrôlé** .

2.  Cliquez avec le bouton droit sur le nœud de **contrôle de modification** , puis cliquez sur **nouvel objet de stratégie de**contrôle.

3.  Dans la boîte de dialogue **nouvel objet GPO contrôlé** :

    1.  Pour recevoir une copie de la demande, tapez votre adresse de messagerie dans le champ **CC** .

    2.  Tapez **MyOtherGPO** comme nom du nouvel objet de stratégie de groupe.

    3.  Tapez un commentaire pour le nouvel objet de stratégie de groupe.

    4.  Cliquez sur **créer en temps réel** pour que le nouvel objet GPO soit déployé sur l’environnement de production immédiatement après approbation.

    5.  Dans **modèle d’objet de stratégie de groupe**, sélectionnez **MyTemplate**. Cliquez sur **Envoyer**.

4.  Lorsque la fenêtre de **progression d’AGPM** indique la progression globale de l’opération, cliquez sur **Fermer**. Le nouvel objet GPO est affiché dans l’onglet **en attente** .

Utilisez un compte auquel est attribué le rôle d’approbateur pour approuver la demande en attente de création de l’objet de stratégie de groupe, comme vous l’avez fait à l' [étape 1: créer un objet de stratégie de groupe](#bkmk-manage1). MyTemplate incorpore tous les paramètres que vous avez configurés dans MyGPO. Dans la mesure où MyOtherGPO a été créé à l’aide de MyTemplate, il s’agit d’abord de tous les paramètres MyGPO contenus au moment de la création de MyTemplate. Pour confirmer cela, vous pouvez générer un rapport de différences et comparer MyOtherGPO à MyTemplate.

**Pour extraire l’objet de stratégie de groupe de l’archive en vue de le modifier**

1.  Sur un ordinateur sur lequel vous avez installé un client AGPM, connectez-vous à l’aide d’un compte d’utilisateur auquel le rôle d’éditeur est attribué dans AGPM.

2.  Cliquez avec le bouton droit sur **MyOtherGPO**, puis cliquez sur **extraire**.

3.  Tapez un commentaire à afficher dans l’historique de l’objet de stratégie de groupe lors de son extraction, puis cliquez sur **OK**.

4.  Lorsque la fenêtre de **progression d’AGPM** indique la progression globale de l’opération, cliquez sur **Fermer**. Dans l’onglet **contrôlé** , l’état de l’objet de stratégie de groupe est identifié comme **extrait**.

**Pour modifier l’objet de stratégie de groupe hors connexion et configurer la durée de verrouillage du compte**

1.  Dans l’onglet **contrôlé** , cliquez avec le bouton droit sur **MyOtherGPO**, puis cliquez sur **modifier** pour ouvrir la fenêtre Éditeur de gestion des stratégies de groupe et changer une copie hors connexion de l’objet de stratégie de **groupe** . Pour ce scénario, configurez la longueur minimale du mot de passe:

    1.  Sous **Configuration ordinateur**, double-cliquez sur **stratégies**, **Paramètres Windows**, **paramètres de sécurité**, stratégies de **compte**et stratégie de **verrouillage du compte**.

    2.  Dans le volet Détails, double-cliquez sur **durée de verrouillage du compte**.

    3.  Dans la fenêtre Propriétés, activez la case à cocher **définir ce paramètre de stratégie**, définissez une durée de **30** minutes, puis cliquez sur **OK**.

2.  Fermez la fenêtre de l' **éditeur de gestion des stratégies de groupe** .

Consultez MyOtherGPO dans l’archive et demandez le déploiement comme vous l’avez fait pour MyGPO à l' [étape 2: modifier un objet de stratégie de groupe](#bkmk-manage2). Vous pouvez comparer MyOtherGPO à MyGPO ou à MyTemplate à l’aide de rapports de différences. Tout compte qui inclut le rôle de réviseur (Administrateur AGPM [contrôle total \], approbateur, éditeur ou réviseur) peut générer des rapports.

**Pour comparer un objet GPO à un autre et à un modèle**

1.  Pour comparer MyGPO et MyOtherGPO:

    1.  Dans l’onglet **contrôlé** , cliquez sur **MyGPO**. Appuyez sur CTRL et cliquez sur **MyOtherGPO**.

    2.  Cliquez avec le bouton droit sur **MyOtherGPO**, pointez sur **différences**, puis cliquez sur **rapport HTML**.

2.  Pour comparer MyOtherGPO et MyTemplate:

    1.  Dans l’onglet **contrôlé** , cliquez sur **MyOtherGPO**.

    2.  Cliquez avec le bouton droit sur **MyOtherGPO**, pointez sur **différences**, puis cliquez sur **modèle**.

    3.  Sélectionnez **MyTemplate** et **HTML Report**, puis cliquez sur **OK**.

### <a href="" id="bkmk-manage5"></a>Étape 5: supprimer et restaurer un objet de stratégie de groupe

Dans le cadre de cette étape, vous jouerez le rôle d’approbateur pour supprimer un objet GPO.

**Pour supprimer un objet de stratégie de groupe**

1.  Sur un ordinateur sur lequel vous avez installé un client AGPM, connectez-vous avec un compte d’utilisateur auquel le rôle d’approbateur est attribué.

2.  Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.

3.  Dans l’onglet **contenu** , cliquez sur l’onglet **contrôlé** pour afficher les objets de stratégie de groupe contrôlés.

4.  Cliquez avec le bouton droit sur **MyGPO**, puis cliquez sur **supprimer**. Cliquez sur **Supprimer l’objet GPO d’archive et de production** pour supprimer la version dans l’archive et la version déployée de l’objet de stratégie de groupe dans l’environnement de production.

5.  Tapez un commentaire à afficher dans la trace d’audit de l’objet de stratégie de groupe, puis cliquez sur **OK**.

6.  Lorsque la fenêtre de **progression d’AGPM** indique la progression globale de l’opération, cliquez sur **Fermer**. L’objet de stratégie de groupe est supprimé de l’onglet **contrôlé** et s’affiche sous l’onglet de la **Corbeille** , où il peut être restauré ou détruit.

Occasionnellement, vous pouvez découvrir après avoir supprimé un objet de stratégie de groupe qui est toujours nécessaire. Dans le cadre de cette étape, vous vous attendez en tant qu’approbateur de la restauration d’un objet de stratégie de groupe qui a été supprimé.

**Pour restaurer un objet de stratégie de groupe supprimé**

1.  Dans l’onglet **contenu** , cliquez sur l’onglet **Corbeille** pour afficher les objets de stratégie de groupe supprimés.

2.  Cliquez avec le bouton droit sur **MyGPO**, puis cliquez sur **restaurer**.

3.  Tapez un commentaire à afficher dans l’historique de l’objet de stratégie de groupe, puis cliquez sur **OK**.

4.  Lorsque la fenêtre de **progression d’AGPM** indique la progression globale de l’opération, cliquez sur **Fermer**. L’objet de stratégie de groupe est supprimé de l’onglet **Corbeille** et s’affiche sous l’onglet **contrôlé** .

    **Remarques**  La restauration d’un objet de stratégie de groupe dans l’archive ne le redéploie pas automatiquement dans l’environnement de production. Pour renvoyer l’objet de stratégie de groupe à l’environnement de production, déployez l’objet GPO comme à l' [étape 3: passer en revue et déployer un objet de stratégie de groupe](#bkmk-manage3).

     

Après la modification et le déploiement d’un objet de stratégie de groupe, il est possible que les modifications récentes apportées à l’objet GPO causent un problème. Dans le cadre de cette étape, vous faites Office d’approbateur pour restaurer une version antérieure de l’objet de stratégie de groupe. Vous pouvez revenir à une version quelconque de l’historique de l’objet de stratégie de groupe. Vous pouvez utiliser des commentaires et des étiquettes pour identifier les versions connues et en cas de modifications spécifiques.

**Pour restaurer une version antérieure d’un objet de stratégie de groupe**

1.  Dans l’onglet **contenu** , cliquez sur l’onglet **contrôlé** pour afficher les objets de stratégie de groupe contrôlés.

2.  Double-cliquez sur **MyGPO** pour afficher son historique.

3.  Cliquez avec le bouton droit sur la version que vous voulez déployer, cliquez sur **déployer**, puis sur **Oui**.

4.  Lorsque la fenêtre de **progression** indique que l’avancement global est terminé, cliquez sur **Fermer**. Dans la fenêtre **historique** , cliquez sur **Fermer**.

    **Remarques**  Pour vérifier que la version qui a été redéployée est la version prévue, examinez un rapport de différences pour les deux versions. Dans la fenêtre **historique** de l’objet de stratégie de groupe, sélectionnez les deux versions, cliquez dessus avec le bouton droit, pointez sur **différence**, puis cliquez sur rapport **HTML** ou sur **rapport XML**.

     

 

 





