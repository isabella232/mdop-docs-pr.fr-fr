---
title: Déploiement de MBAM2.5 dans une configuration autonome
description: Présentation de la procédure de déploiement d’MBAM 2,5 dans une configuration autonome.
author: Deland-Han
ms.reviewer: dcscontentpm
manager: dansimp
ms.author: delhan
ms.sitesec: library
ms.prod: w10
ms.date: 09/16/2019
ms.openlocfilehash: 905eb7a40483a7a7b499d6dced8472331c87b838
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811753"
---
# Déploiement de MBAM 2,5 dans une configuration autonome

Cet article fournit des instructions pas à pas pour l’installation de Microsoft BitLocker administration et de la surveillance (MBAM) 2,5 dans une configuration autonome. Dans ce guide, nous allons utiliser une configuration à deux serveurs. L’un des deux serveurs est un serveur de base de données exécutant Microsoft SQL Server 2012. Ce serveur va héberger les bases de données et les rapports MBAM. Le serveur supplémentaire est un serveur Web 2012 d’hébergement d’hébergement «administration et analyse du serveur» et «portail libre-service».

## Étapes de préparation avant d’installer le logiciel serveur MBAM 2,5

### Étape 1: installation et configuration de serveurs

Avant de commencer à configurer MBAM 2,5, nous devons nous assurer que les deux serveurs sont configurés en fonction de la configuration système requise pour MBAM. Voir la configuration [minimale requise pour MBAM](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/mbam-25-supported-configurations#-mbam-server-system-requirements)et sélectionnez une configuration qui répond à la configuration requise. 

#### Étape 1,1: déploiement des conditions préalables pour la base de données et le serveur de création de rapports

1. Installez et configurez un serveur exécutant le système d’exploitation Windows Server 2008 R2 (ou version ultérieure).

2. Installez Windows PowerShell 3,0.

3. Installez Microsoft SQL Server 2008 R2 ou une version ultérieure qui inclut le dernier Service Pack. Si vous installez une nouvelle instance de SQL Server pour MBAM, assurez-vous que le serveur SQL Server installé inclut le regroupement SQL_Latin1_General_CP1_CI_AS. Pour installer les fonctionnalités SQL Server suivantes:

    * Moteur de base de données
    * Reporting Services
    * Connectivité des outils clients
    * Outils de gestion-terminé

    > [!Note]
    > Si vous le souhaitez, vous pouvez également installer la [fonction de chiffrement de données (TDE) dans SQL Server](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/mbam-25-security-considerations).

    SQL Server Reporting Services doit être installé et configuré en mode «natif» et non en mode non configuré ou «SharePoint».

    ![Fonctionnalités nécessaires de SQL Server](images/deploying-MBAM-1.png)

4. Si vous envisagez d’utiliser SSL pour le site Web d’administration et de contrôle, assurez-vous de configurer SQL Server Reporting Services (SSRS) pour utiliser le protocole SSL (Secure Sockets Layer) avant de configurer le site Web d’administration et de surveillance. Dans le cas contraire, la fonction rapports utilise le transport de données non chiffrées (HTTP) au lieu de chiffrés (HTTPs).

    Vous pouvez suivre [configurer des connexions SSL](https://docs.microsoft.com/sql/reporting-services/security/configure-ssl-connections-on-a-native-mode-report-server?view=sql-server-2017) sur un serveur de rapports en mode natif pour configurer SSL sur le serveur de rapports.
    
    > [!Note]
    > Vous pouvez suivre le Guide d’installation de SQL Server pour votre version de SQL Server correspondante pour installer SQL Server. Les liens sont les suivants:
        > * [SQL Server 2014](https://docs.microsoft.com/sql/sql-server/install/planning-a-sql-server-installation?view=sql-server-2014)
        > * [SQL Server 2012](https://docs.microsoft.com/previous-versions/sql/sql-server-2012/bb500442(v=sql.110))
        > * [SQL Server 2008 R2](https://docs.microsoft.com/previous-versions/sql/sql-server-2012/bb500442(v=sql.110))

5. Dans le post-installation de SQL Server, assurez-vous de configurer le compte d’utilisateur dans SQL Server et attribuez les autorisations suivantes aux utilisateurs qui configureront la base de données MBAM et les rôles de rapport sur le serveur de base de données.

    Rôles de l’instance de SQL Server:
        
    * rôles
    * processadmin

    Droits de l’instance de SQL Server Reporting Services:
    
    * Créer des dossiers
    * Publier des rapports

Votre serveur de base de données est prêt pour la configuration des rôles MBAM 2,5. Allons passer au serveur suivant.

#### Étape 1,2: déploiement des conditions préalables pour le serveur d’administration et de surveillance

Choisissez un serveur qui répond à la configuration matérielle, comme expliqué dans le [document configuration requise pour MBAM](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/mbam-25-supported-configurations#-mbam-server-system-requirements). Il doit exécuter le système d’exploitation Windows Server 2008 R2 ou une version ultérieure, ainsi que le dernier Service Pack et les mises à jour. Lorsque le serveur est prêt, installez les rôles et fonctionnalités suivants:

##### Rôles

* Outils de gestion du serveur Web (IIS) (sélectionnez scripts et outils de gestion IIS).

* Services de rôle de serveur Web

    * Fonctionnalités HTTP courantes<br />
      Contenu statique<br />
      Document par défaut

    * Développement d’applications<br />
      ASP.NET<br />
      Extensibilité .NET<br />
      Extensions ISAPI<br />
      Filtres ISAPI<br />
      Sécurité<br />
      Authentification Windows<br />
      Filtrage de requête

    * Outils de gestion IIS de service Web

##### Fonctionnalité

* Fonctionnalités 4,5 de .NET Framework
  
  * Microsoft .NET Framework 4,5
  
    Pour Windows Server 2012 ou Windows Server 2012 R2, .NET Framework 4,5 est déjà installé pour ces versions de Windows Server. Néanmoins, vous devez l’activer.
  
    Pour Windows Server 2008 R2, .NET Framework 4,5 n’est pas inclus dans Windows Server 2008 R2. Par conséquent, vous devez télécharger .NET Framework 4,5 et l’installer séparément.
  
  * Activation WCF<br />
    Activation HTTP<br />
    Activation non HTTP
  
  * Activation TCP
  
  * Service d’activation de processus Windows:<br />
    Modèle de processus<br />
    Environnement .NET Framework<br />
    API de configuration

Pour que le portail libre-service fonctionne, vous devez également [Télécharger et installer ASP.NET MVC 4,0](https://go.microsoft.com/fwlink/?linkid=392271).

L’étape suivante consiste à créer les utilisateurs et groupes MBAM requis dans Active Directory.

### Étape 2: créer des utilisateurs et des groupes dans les services de domaine Active Directory
 
Dans le cadre de la configuration requise, vous devez définir certains rôles et comptes qui sont utilisés dans MBAM pour fournir une sécurité et des droits d’accès à des serveurs et des fonctionnalités spécifiques, comme les bases de données qui s’exécutent sur l’instance de SQL Server et les applications Web exécutées sur le serveur d’administration et de surveillance.

Créez les groupes et utilisateurs suivants dans Active Directory. (Vous pouvez utiliser n’importe quel nom pour les groupes et les utilisateurs.) Les utilisateurs ne doivent pas disposer de droits utilisateur plus importants. Un compte d’utilisateur de domaine suffit. Vous devez spécifier le nom de ces groupes lors de la configuration de MBAM 2,5:

* **MBAMAppPool**  

  **Type**: utilisateur du domaine

  **Description**: l’utilisateur d’un domaine qui dispose d’une autorisation de lecture ou d’écriture dans la base de données d’audit et de conformité, ainsi que dans la base de données de récupération pour permettre aux applications Web d’accéder aux données et aux rapports de ces bases de données. Il sera également utilisé par le pool d’applications pour les applications Web.

  **Rôles de compte (lors de la configuration de MBAM)**:

  1. Compte de domaine du pool d’applications de service Web

  2. Compatibilité et audit de la base de données et de la base de données de récupération utilisateur en lecture/écriture pour les rapports

* **MBAMROUser**

  **Type**: utilisateur du domaine

  **Description**: utilisateur de domaine qui dispose d’un accès en lecture seule à la base de données de conformité et d’audit pour permettre aux rapports d’accéder aux données de conformité et d’audit dans cette base de données. Il s’agit également du compte d’utilisateur de domaine que l’instance SQL Server Reporting Services utilise pour accéder à la base de données d’audit et de conformité.

  **Rôles de compte (lors de la configuration de MBAM)**:

  1. Conformité et audit utilisateur de la base de données en lecture seule pour les rapports

  2. Compte d’utilisateur de base de données et de conformité

* **MBAMAdvHelpDsk**

  **Type**: groupe de domaines

  **Description**: MBAM groupe d’accès utilisateurs du support technique avancé: groupe d’utilisateurs de domaine dont les membres ont accès à toutes les zones du site Web d’administration et de surveillance. Les utilisateurs qui ont ce rôle doivent entrer uniquement la clé de récupération, et non le domaine et le nom d’utilisateur de l’utilisateur, pour aider les utilisateurs à récupérer leurs lecteurs. Si un utilisateur est membre du groupe utilisateurs du support technique MBAM et du groupe utilisateurs du support technique avancée MBAM, les autorisations du groupe utilisateurs du support technique avancé MBAM remplacent les autorisations du groupe assistance technique MBAM.

  **Rôles de compte (lors de la configuration de MBAM)**: MBAM Advanced helpdesk Users

* **MBAMHelpDsk**

  **Type**: groupe de domaines

  **Description**: MBAM d’accès du support technique au groupe d’utilisateurs du support technique: groupe d’utilisateurs de domaine dont les membres ont accès aux zones gérer le module de plateforme sécurisée et de reprise du site Web Administration et analyse MBAM. Les personnes qui ont ce rôle doivent remplir tous les champs lorsqu’ils utilisent l’une des deux options. Cela inclut le domaine et le nom du compte de l’utilisateur.

  **Rôles de compte (lors de la configuration de MBAM)**: utilisateurs du support technique MBAM

* **MBAMRUGrp**

  **Type**: groupe de domaines

  **Description**: groupe d’utilisateurs de domaine dont les membres ont un accès en lecture seule aux rapports figurant dans la zone rapports du site Web Administration et analyse.

  **Rôles de compte (lors de la configuration de MBAM)**:

  1. Rapport de groupe d’accès de domaine en lecture seule

  2. Groupe accéder aux utilisateurs du rapport MBAM

### Étape 3 (facultative): configurer et installer un certificat SSL sur un serveur d’administration et de surveillance

Même s’il est facultatif, nous vous conseillons vivement d’utiliser un certificat pour sécuriser la communication entre le client MBAM et le site Web d’administration et de contrôle, ainsi que les sites Web de portail libre-service. Nous vous déconseillons d’utiliser des certificats auto-signés pour des raisons de sécurité évidentes. Nous vous suggérons d’utiliser un certificat de type de serveur Web auprès d’une autorité de certification approuvée. Pour ce faire, vous pouvez consulter la section «utiliser le certificat approuvé par l’autorité de certification» dans [KB 2754259](https://support.microsoft.com/help/2754259).

Une fois le certificat émis, vous devez ajouter le certificat au magasin personnel du serveur d’administration et de surveillance. Pour ajouter le certificat, ouvrez le magasin de certificats de l’ordinateur local. Pour cela, procédez comme suit:

1. Cliquez avec le bouton droit sur Démarrer, puis sélectionnez Exécuter.

   ![Sélectionner ](images/deploying-MBAM-2.png)

2. Tapez «MMC.EXE» (sans guillemets), puis sélectionnez **OK**.

   ![Champ exécuter](images/deploying-MBAM-3.png) 

3. Sélectionnez **fichier** dans la nouvelle console MMC que vous avez ouverte, puis sélectionnez **Ajouter/supprimer un composant logiciel enfichable**.
   
   ![Sélectionner](images/deploying-MBAM-4.png)

4. Mettez en surbrillance le composant logiciel enfichable **certificats** , puis sélectionnez **Ajouter**.

   ![Fenêtre Ajouter ou supprimer des composants enfichables](images/deploying-MBAM-5.png)

5. Sélectionnez l’option **compte d’ordinateur** , puis cliquez sur **suivant**.
   
   ![Fenêtre du composant logiciel enfichable Certificats](images/deploying-MBAM-6.png)

6. Dans l’écran suivant, sélectionnez **ordinateur local** , puis sélectionnez **Terminer**.
   
   ![Fenêtre Sélectionner un ordinateur](images/deploying-MBAM-7.png)

7. Vous avez à présent ajouté le composant logiciel enfichable Certificats. Cela vous permettra de travailler avec n’importe quel certificat dans le magasin de certificats de votre ordinateur.

   ![Fenêtre Ajouter ou supprimer des composants enfichables](images/deploying-MBAM-8.png)

8. Importez le certificat de serveur Web dans le magasin de certificats de votre ordinateur.

   À présent que vous avez accès au composant logiciel enfichable Certificats, vous pouvez importer le certificat de serveur Web dans le magasin de certificats de votre ordinateur. Pour cela, suivez les étapes suivantes.

9. Ouvrez le composant logiciel enfichable Certificats (ordinateur local), puis naviguez jusqu’à **personnel** , puis sur **certificats**.
   
   ![Fenêtre de composant logiciel enfichable Certificats (ordinateur local)](images/deploying-MBAM-9.png)

   > [!Note]
   > Le composant logiciel enfichable certificats ne figure pas dans la liste. Si ce n’est pas le cas, aucun certificat n’est installé.

10. Cliquez avec le bouton droit sur **certificats**, sélectionnez **toutes les tâches**, puis **Importer**.

    ![Fenêtre de composant logiciel enfichable Certificats (ordinateur local)](images/deploying-MBAM-10.png)

11. Lorsque l’Assistant démarre, sélectionnez **suivant**. Recherchez le fichier que vous avez créé qui contient votre certificat de serveur et votre clé privée, puis sélectionnez **suivant**.

    ![Fenêtre de l’Assistant importation de certificat](images/deploying-MBAM-11.png)

12. Entrez le mot de passe si vous en avez spécifié un pour le fichier lors de sa création.

   ![Fenêtre entrer un mot de passe](images/deploying-MBAM-12.png)

   > [!Note]
   > Assurez-vous que l’option **marquer la clé comme étant exportable** est sélectionnée si vous voulez être en mesure d’exporter de nouveau la paire de clés à partir de cet ordinateur. Dans le cadre d’une mesure de sécurité supplémentaire, vous souhaiterez peut-être activer cette option pour vous assurer que personne ne peut faire une sauvegarde de votre clé privée.
 
13. Sélectionnez **suivant**, puis sélectionnez le **magasin de certificats** dans lequel vous voulez enregistrer le certificat.

    ![Fenêtre de l’Assistant importation de certificat](images/deploying-MBAM-13.png)

    > [!Note]
    > Vous devez sélectionner **personnel**, car il s’agit d’un certificat de serveur Web. Si vous avez inclus le certificat dans la hiérarchie de certification, il est également ajouté au magasin.
 
14. Sélectionnez **suivant**, puis sélectionnez **Terminer**.

    ![Fenêtre de l’Assistant importation de certificat](images/deploying-MBAM-14.png)

Le certificat de serveur de votre serveur Web est désormais affiché dans la liste certificats personnels. Il sera indiqué par le nom usuel du serveur. (Vous pouvez le trouver dans la section objet du certificat.)

Pour en savoir plus:

[Considérations relatives à la sécurité pour MBAM2.5](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/mbam-25-security-considerations)

[Planification de la sécurisation des sites web MBAM](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/planning-how-to-secure-the-mbam-websites)

L’étape suivante consiste à inscrire un nom principal de service pour le compte du pool d’applications.

### Étape 4: configuration du certificat SSL pour le serveur Web MBAM

Si vous utilisez une communication SSL entre le client et le serveur, assurez-vous que le certificat est doté d’une clé d’utilisation améliorée de la clé (1.3.6.1.5.5.7.3.1) et (1.3.6.1.5.5.7.3.2). C’est pourquoi vous devez veiller à ce que l’authentification du serveur et l’authentification du client soient ajoutées.

Si un message d’erreur s’affiche lorsque vous essayez de parcourir les URL du service, vous utilisez un certificat qui a été émis pour un autre nom ou vous naviguez en utilisant une URL incorrecte.

Même si le navigateur peut vous avertir en utilisant un message d’erreur de certificat tout en vous permettant de continuer, le service Web MBAM n’ignore pas les erreurs de certificat et bloque la connexion. Vous remarquerez des erreurs liées au certificat dans le journal des événements d’administration MBAM du client MBAM. Si vous utilisez un alias pour vous connecter au serveur d’administration et de surveillance, vous devez envoyer un certificat sur le nom de l’alias. C’est-à-dire que le nom du sujet du certificat doit être le nom de l’alias et que le nom DNS du serveur local doit être ajouté au champ **autre nom** de l’objet du certificat.

Exemple :

Si le nom virtuel est «bitlocker.contoso.com» et que le nom du serveur d’administration et de surveillance MBAM est «adminserver.contoso.com», le certificat doit être délivré à bitlocker.contoso.com (nom du sujet), et adminserver.contoso.com doit être ajouté au champ **autre nom** de l’objet du certificat.

De même, si plusieurs serveurs d’administration et de surveillance sont installés pour équilibrer la charge à l’aide d’un équilibreur de charge, vous devez émettre le certificat SSL vers le nom virtuel. C’est-à-dire que le champ nom du sujet du certificat doit avoir le nom virtuel et que les noms de tous les serveurs locaux doivent être ajoutés dans le champ **nom** de l’objet du certificat.

Exemple :

Si le nom virtuel est «bitlocker.contoso.com» et que les serveurs sont «adminserver1.contoso.com» et «adminiserver2.contoso.com», le certificat doit être émis pour bitlocker.contoso.com (nom du sujet) et adminserver1.contoso.com, et adminiserver2.contoso.com doit être ajouté au champ **autre nom** de l’objet du certificat.

Les étapes de configuration de la communication SSL à l’aide de MBAM sont décrites dans l’article de la base de connaissances suivant: [KB 2754259](https://support.microsoft.com/help/2754259).

### Étape 5: inscrire des SPN pour le compte du pool d’applications et configurer la délégation contrainte

> [!Note]
> La délégation contrainte est uniquement requise pour 2,5 et n’est pas requise pour 2,5 Service Pack 1 et version ultérieure.

Pour permettre aux serveurs MBAM d’authentifier les communications à partir du site Web d’administration et de surveillance et du portail libre-service, vous devez inscrire un nom de principal de service (SPN) pour le nom d’hôte sous le compte de domaine que vous utilisez pour le pool d’applications Web. L’article suivant contient des instructions pas à pas pour inscrire des SPN: [planification de la sécurisation des sites Web MBAM](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/planning-how-to-secure-the-mbam-websites)

Une fois le SPN configuré, vous devez configurer la délégation contrainte sur le SPN. Pour cela, procédez comme suit:

1. Accédez à Active Directory et recherchez les informations d’identification du pool d’applications que vous avez configurées pour les sites Web MBAM au cours des étapes précédentes.

2. Cliquez avec le bouton droit sur les informations d’identification, puis sélectionnez **Propriétés**.

3. Sélectionnez l’onglet **délégation** .

4. Sélectionnez l’option d’authentification Kerberos.

5. Sélectionnez **Parcourir**, puis parcourez de nouveau les informations d’identification de votre pool d’applications. Vous devriez alors voir tous les SPN configurés sur le compte d’identification du pool d’applications. (Le SPN doit ressembler à «http/BitLocker. FQDN. com»). Mettez en surbrillance le SPN qui est le même que celui que vous avez spécifié lors de l’installation d’MBAM.

6. Sélectionnez **OK**.

C’est désormais bien avec les conditions préalables. Dans les étapes suivantes, vous allez installer le logiciel MBAM sur les serveurs et le configurer.

## Installer et configurer le logiciel serveur MBAM 2,5

### Étape 6: installer le logiciel serveur MBAM 2,5 

Pour installer le logiciel serveur MBAM à l’aide de l’Assistant de configuration de l’administration et de la surveillance de BitLocker sur un serveur de base de données et sur un serveur d’administration et de surveillance, procédez comme suit.

1. Sur le serveur sur lequel vous souhaitez installer MBAM, exécutez MBAMserversetup.exe pour démarrer l’Assistant Configuration de l’administration et de la surveillance de BitLocker.

2. Dans la page Bienvenue, sélectionnez **suivant**.

3. Lisez et acceptez le contrat de licence logiciel Microsoft, puis sélectionnez **Next (suivant** ) pour continuer l’installation.

4. Déterminez si vous souhaitez utiliser Microsoft Update lors de la recherche des mises à jour, puis sélectionnez **suivant**.

5. Décidez si vous souhaitez participer au programme d’amélioration du produit, puis sélectionnez **suivant**.

6. Pour démarrer l’installation, sélectionnez **installer**.

7. Pour configurer les fonctionnalités du serveur après l’installation du logiciel MBAM Server, activez la case à cocher **exécuter MBAM Server Configuration une fois l’Assistant fermé** . Vous pouvez ou configurer MBAM plus tard en utilisant le raccourci de **configuration de MBAM Server** que le programme d’installation du serveur crée dans le menu **Démarrer** .

8. Cliquez sur **Terminer**.

Pour plus d’informations, reportez-vous à [installation du logiciel serveur MBAM 2,5](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/installing-the-mbam-25-server-software).

### Étape 7: configurer le rôle de base de données et de rapports MBAM 2,5

Dans cette étape, nous allons configurer les bases de données et le composant de création de rapports MBAM 2,5 à l’aide de l’Assistant MBAM:

1. Configurez la base de données d’audit et de conformité avec la base de données de récupération en utilisant l’Assistant:
   
   1. Sur le serveur sur lequel vous voulez configurer les bases de données, démarrez l' **Assistant Configuration de MBAM Server**. Vous pouvez sélectionner **MBAM de configuration de serveur** dans le menu **Démarrer** pour ouvrir l’Assistant.

   2. Sélectionnez **ajouter de nouvelles fonctionnalités**, sélectionnez **conformité et audit de base de données**, **base de données de récupération et rapports**, puis sélectionnez **suivant**. L’Assistant vérifie que toutes les conditions préalables pour les bases de données sont remplies.

   3. Si la vérification de la configuration requise est réussie, sélectionnez **Next (suivant** ) pour continuer. Dans le cas contraire, résolvez les conditions préalables manquantes, puis sélectionnez de **nouveau vérifier les conditions préalables**.
   
   4. À l’aide des descriptions suivantes, entrez les valeurs de champ dans l’Assistant:

2. Base de données d’audit et de conformité

   |Champ   |Description|
   |-------|-------|
   |Nom SQL Server |Nom du serveur sur lequel vous configurez la base de données d’audit et de conformité. <br /> Vous devez ajouter une exception dans l’ordinateur de la base de données d’audit et de conformité pour activer le trafic entrant entrant sur le port SQL Server. Le numéro de port par défaut est 1433.|
   |Instance de base de données SQL Server    |Nom de l’instance de base de données dans laquelle les données d’audit et de conformité seront stockées. Si vous utilisez l’instance par défaut, vous devez laisser ce champ vide. Vous devez également spécifier l’emplacement des informations de la base de données.|
   |Nom de la base de données   |Nom de la base de données qui stockera les données de conformité. Vous devez noter le nom de la base de données que vous spécifiez ici, car vous devrez fournir ces informations dans les étapes suivantes.|
   |Autorisation en lecture/écriture le groupe ou l’utilisateur  |Spécifiez le nom de l’utilisateur MBAMAppPool tel que configuré à l’étape 2.|
   |Utilisateur ou groupe d’accès en lecture seule   |Spécifiez le nom de l’utilisateur MBAMROUser tel que configuré à l’étape 2.|

3. Base de données de récupération.

   |Champ   |Description|
   |-----|-----|
   |Nom SQL Server |Nom du serveur sur lequel vous configurez la base de données de récupération. Vous devez ajouter une exception dans l’ordinateur de la base de données de récupération pour activer le trafic entrant entrant sur le port SQL Server. Le numéro de port par défaut est 1433.|
   |Instance de base de données SQL Server    |Nom de l’instance de base de données dans laquelle les données de récupération seront stockées. Si vous utilisez l’instance par défaut, vous devez laisser ce champ vide. Vous devez également spécifier l’emplacement des informations de la base de données.|
   |Nom de la base de données   |Nom de la base de données qui stockera les données de récupération.|
   |Autorisation en lecture/écriture le groupe ou l’utilisateur  |Utilisateur ou groupe ayant une autorisation en lecture/écriture à cette base de données pour permettre aux applications Web d’accéder aux données et rapports de cette base de données. <br />Si vous entrez un utilisateur dans ce champ, il doit avoir la même valeur que la valeur figurant dans le champ **compte de domaine du pool d’applications de service Web** de la page configurer des **applications Web** . <br />Si vous entrez un groupe dans ce champ, la valeur du champ **compte de domaine du pool d’applications de service Web** de la page **configurer des applications Web** doit être membre du groupe que vous entrez dans ce champ.|
   
   Lorsque vous avez terminé, sélectionnez **suivant**. L’Assistant vérifie que toutes les conditions préalables pour les bases de données sont remplies.
   
   Si la vérification de la configuration requise est réussie, sélectionnez **Next (suivant** ) pour continuer. Dans le cas contraire, résolvez les conditions préalables manquantes, puis sélectionnez de nouveau **suivant** .

4. Rapports.

   |Champ   |Description|
   |----|----|
   |Instance de SQL Server Reporting Services  |Instance de SQL Server Reporting Services où les rapports seront configurés. Si vous utilisez l’instance par défaut, vous devez laisser ce champ vide.|
   |Groupe de domaine de rôle de rapport |Spécifiez le nom du MBAMRUGrp tel qu’indiqué à l’étape 2.|
   |Nom SQL Server |Nom du serveur sur lequel la base de données d’audit et de conformité est configurée.|
   |Instance de base de données SQL Server    |Nom de l’instance de base de données dans laquelle les données d’audit et de conformité sont configurées. Si vous utilisez l’instance par défaut, vous devez laisser ce champ vide. <br />Vous devez ajouter une exception sur l’ordinateur rapports pour activer le trafic entrant sur le port du serveur de rapports. (Le port par défaut est 80.)|
   |Nom de la base de données|  Nom de la base de données d’audit et de conformité. Par défaut, le nom de la base de données est MBAM de conformité.|
   |Vérification de la conformité et de la base de données du compte de domaine    |Spécifiez le nom de l’utilisateur MBAMROUser tel que configuré à l’étape 2.|
   
   Lorsque vous avez terminé, sélectionnez **suivant**. L’Assistant vérifie que toutes les conditions préalables pour la fonction rapports sont remplies. Sélectionnez Suivant pour continuer. Dans la page **Résumé** , passez en revue les fonctionnalités qui seront ajoutées.
   
   Pour plus d’informations, reportez-vous à l’article suivant: [configurer les bases de données 2,5 de MBAM](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-configure-the-mbam-25-databases).

### Étape 8: configurer le rôle des applications Web MBAM 2,5

1. Sur le serveur sur lequel vous voulez configurer les applications Web, démarrez l’Assistant Configuration de MBAM Server. Vous pouvez sélectionner **MBAM de configuration de serveur** dans le menu **Démarrer** pour ouvrir l’Assistant.

2. Cliquez sur **ajouter de nouvelles fonctionnalités**, sélectionnez le **site Web d’administration et de contrôle** et **le portail libre-service**, puis sélectionnez **suivant**. L’Assistant vérifie que toutes les conditions préalables pour les bases de données sont remplies.

3. Si la vérification de la configuration requise est réussie, sélectionnez **Next (suivant** ) pour continuer. Dans le cas contraire, résolvez les conditions préalables manquantes, puis sélectionnez de **nouveau vérifier les conditions préalables**.

4. Utilisez les descriptions suivantes pour entrer les valeurs de champ dans l’Assistant.

   |Champ   |Description|
   |-----|-----|
   |Certificat de sécurité    |Sélectionnez un certificat déjà créé à l’étape 3 pour chiffrer éventuellement la communication entre les services Web et le serveur sur lequel vous configurez le site Web d’administration et de surveillance. Si vous sélectionnez ne pas utiliser de certificat, votre communication Web risque de ne pas être sécurisée.|
   |Nom de l'hôte   |Nom de l’ordinateur hôte sur lequel vous configurez le site Web d’administration et de surveillance. <br />Il n’est pas nécessaire qu’il s’agisse du nom d’hôte de l’ordinateur, ce n’est pas tout. Toutefois, si le nom d’hôte est différent du nom NetBIOS de l’ordinateur, vous devez créer un enregistrement A et vérifier que le SPN utilise le nom d’hôte personnalisé et non le nom NetBIOS. Cette situation est courante dans les scénarios d’équilibrage de charge.|
   |Chemin d’installation   |Chemin sur lequel vous installez le site Web d’administration et de surveillance.|
   |Port    |Numéro de port à utiliser pour la communication sur le site Web. <br /> Vous devez définir une exception de pare-feu pour autoriser les communications via le port spécifié.|
   |Compte et mot de passe du pool d’applications de service Web    |Spécifiez le compte d’utilisateur et le mot de passe de l’utilisateur MBAMAppPool comme configuré à l’étape 2. <br /> Pour une sécurité améliorée, définissez le compte spécifié dans les informations d’identification pour disposer de droits d’utilisateur limités. Définissez également le mot de passe du compte pour qu’il n’expire jamais.|

5. Vérifiez que le compte intégré IIS_IUSRS ou le compte du pool d’applications a été ajouté à l’utilisateur disposant d' **une authentification** et du processus **de connexion en tant que** paramètre de sécurité locale.

   Pour vérifier si le compte a été ajouté aux paramètres de sécurité locaux, ouvrez l' **éditeur de stratégie de sécurité local**, développez le nœud **stratégies locales** , sélectionnez le nœud d' **attribution de droits d’utilisateur** , puis double-Sélectionnez emprunter l’identité d' **un client après authentification** et **Connectez-vous en tant que stratégies de travail par lot** dans le volet droit.

6. Utilisez les descriptions de champs suivantes pour configurer les informations de connexion dans l’Assistant pour la base de données d’audit et de conformité.
   |Champ   |Description|
   |------|------|
   |Nom SQL Server |Nom du serveur sur lequel la base de données d’audit et de conformité est configurée.|
   |Instance de base de données SQL Server    |Nom de l’instance de SQL Server (par exemple, \<Server Name\> ) et sur lequel la base de données d’audit et de conformité est configurée. Laissez ce champ vide si vous utilisez l’instance par défaut.|
   |Nom de la base de données   |Nom de la base de données d’audit et de conformité. Par défaut, il s’agit de «MBAM Compliance Status».|

7. Utilisez les descriptions de champs suivantes pour configurer les informations de connexion dans l’Assistant pour la base de données de récupération.
   |Champ   |Description|
   |----|----|
   |Nom SQL Server |Nom du serveur sur lequel la base de données de récupération est configurée.|
   |Instance de base de données SQL Server    |Nom de l’instance de SQL Server (par exemple, \<Server Name\> ) sur laquelle la base de données de récupération est configurée. Laissez ce champ vide si vous utilisez l’instance par défaut.|
   |Nom de la base de données   |Nom de la base de données de récupération. Par défaut, il s’agit de «restauration et de matériel MBAM».|

8. Utilisez les descriptions suivantes pour entrer les valeurs de champ dans l’Assistant afin de configurer le site Web d’administration et de surveillance.
   |Champ   |Description|
   |----|----|
   |Groupe de domaine de rôle de support avancé |Spécifiez le nom du groupe MBAMAdvHelpDsk tel que configuré à l’étape 2.|
   |Groupe de domaine du rôle de support technique  |Spécifiez le nom du groupe MBAMHelpDsk tel que configuré à l’étape 2.|
   |Utiliser System Center Configuration Manager Integration |Activez cette case à cocher pour désactiver cette case à cocher.     |
   |Groupe de domaine de rôle de rapport |Spécifiez le nom du groupe MBAMRUGrp tel que configuré à l’étape 2.    |
   |URL SQL Server Reporting Services   |Spécifiez l’URL du service Web pour le serveur SSRS sur lequel les rapports MBAM sont configurés. Vous pouvez trouver ces informations en vous connectant à Reporting Services Configuration Manager sur le serveur de base de données. <br /> Exemple de nom de domaine complet:https://MyReportServer.Contoso.com/ReportServer <br />Exemple de nom d’hôte personnalisé:https://MyReportServer/ReportServer|
   |Répertoire virtuel   |Répertoire virtuel du site Web d’administration et de surveillance. Ce nom correspond au répertoire physique du site Web sur le serveur et est ajouté au nom d’hôte du site Web. Exemple: <br />http (s):// *\<host name\>* : *\<port\>* /helpdesk/ <br />Si vous ne spécifiez pas de répertoire virtuel, la valeur du support technique est utilisée.     |

9. Utilisez la description suivante pour entrer les valeurs de champ dans l’Assistant afin de configurer le portail libre-service.

   |Champ   |Description|
   |----|----|
   |Répertoire virtuel   |Répertoire virtuel de l’application Web. Ce nom correspond au répertoire physique du site Web sur le serveur et est ajouté au nom d’hôte du site Web. Exemple:<br />http (s):// *\<host name\>* : *\<port\>* /selfservice/<br /> Si vous ne spécifiez pas un répertoire virtuel, la valeur «SelfService» est utilisée.|

10. Lorsque vous avez terminé, sélectionnez **suivant**. L’Assistant vérifie que toutes les conditions préalables pour les applications Web sont remplies.

11. Sélectionnez **Next (suivant** ) pour continuer.

12. Dans la page **Résumé** , passez en revue les fonctionnalités qui seront ajoutées.

13. Sélectionnez **Ajouter** pour ajouter les applications Web au serveur, puis cliquez sur **Fermer**.

## Personnalisation et validation des étapes après l’installation du logiciel MBAM 2,5 Server

### Étape 9: personnalisation du portail libre-serveur pour votre organisation

Pour personnaliser le portail libre-service en ajoutant un texte d’avis personnalisé, le nom de votre entreprise, des pointeurs vers des informations supplémentaires, etc., voir [Personnalisation du portail libre-service pour votre organisation](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/customizing-the-self-service-portal-for-your-organization).
 
### Étape 10: configurer le portail libre-serveur si les ordinateurs clients ne peuvent pas accéder au CDN 

Déterminez si vos ordinateurs clients ont accès au réseau de distribution de contenu (CDN) Microsoft AJAX. Le CDN donne au portail libre-service le besoin d’accéder à certains fichiers JavaScript. Si vous ne configurez pas le portail libre-service lorsque les ordinateurs clients ne peuvent pas accéder au CDN, seul le nom de la société et le compte sous lequel l’utilisateur s’est connecté s’affiche. Aucun message d’erreur ne s’affichera.

Effectuez l'une des opérations suivantes:

* Si vos ordinateurs clients ont accès au réseau de distribution de contenu (CDN), ne faites rien. Votre configuration du portail libre-service est terminée.

* Si vos ordinateurs clients n’ont pas accès au réseau de distribution de contenu (CDN), suivez les étapes décrites dans la [procédure de configuration du portail libre-service lorsque les ordinateurs clients ne peuvent pas accéder au réseau de distribution de contenu Microsoft](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-configure-the-self-service-portal-when-client-computers-cannot-access-the-microsoft-content-delivery-network).

### Étape 11: valider la configuration de fonctionnalité de serveur MBAM 2,5 

Pour valider le déploiement de votre serveur MBAM et utiliser la topologie autonome, procédez comme suit.

1. Sur chaque serveur sur lequel une fonctionnalité MBAM est déployée, **Control Panel**sélectionnez programmes  >  **Programs**  >  **et fonctionnalités**du panneau de configuration. Vérifiez que la fonctionnalité **administration et analyse de BitLocker Microsoft** s’affiche dans la liste **programmes et fonctionnalités** .
   > [!Note]
   > Pour effectuer la validation, vous devez utiliser un compte de domaine disposant d’informations d’identification d’administrateur local sur chaque serveur.

2. Sur le serveur sur lequel la base de données de récupération est configurée, ouvrez SQL Server Management Studio, puis vérifiez que la base de données **MBAM et de récupération** de la base de données est configurée.

3. Sur le serveur om sur lequel la base de données d’audit et de conformité est configurée, ouvrez SQL Server Management Studio, puis vérifiez que la base de données d’état de conformité MBAM est configurée.

4. Sur le serveur ONM lequel la fonctionnalité rapports est configurée, ouvrez un navigateur Web à l’aide des informations d’identification d’administration et naviguez jusqu’à la page d’accueil du site SQL Server Reporting Services.
   
   L’emplacement de la page d’accueil par défaut d’une instance de site SQL Server Reporting Services est le suivant: *\<MBAM Reports Server Name\>* *\<port\>* /reports.aspx
   
   Pour trouver l’URL réelle, utilisez l’outil Gestionnaire de configuration Reporting Services, puis sélectionnez les instances que vous avez spécifiées lors de l’installation.
   
5. Vérifiez qu’un dossier de rapports intitulé Microsoft BitLocker administration et analyse contient une source de données nommée MaltaDataSource. Cette source de données contient des dossiers dont les noms représentent des paramètres régionaux de langue (par exemple, en-US). Les rapports se trouvent dans les dossiers de langue.

   > [!Note]
   > Si SQL Server Reporting Services (SSRS) a été configuré en tant qu’instance nommée, l’URL doit ressembler à ce qui suit: http (s \<MBAM Reports Server Name\> \<port\> Reports_)\<SSRS Instance Name\>
   >
   > Si SSRS n’a pas été configuré pour utiliser SSL (Secure Socket Layer), l’URL des rapports sera définie sur «HTTP» au lieu de «HTTPs» lorsque vous installez le serveur MBAM. Si vous accédez ensuite au site Web Administration et contrôle (également appelé support technique) et sélectionnez un rapport, vous recevez le message suivant: «seul le contenu sécurisé est affiché». Pour afficher l’État, sélectionnez **Afficher tout le contenu**.

6. Sur le serveur sur lequel la fonctionnalité de site Web Administration et contrôle est configurée, exécutez le gestionnaire de serveur, accédez aux **rôles**et sélectionnez **serveur Web (IIS)**  >  Gestionnaire des**services Internet (IIS** ).

7. Dans **connexions**, accédez à, \<computer name\> puis sélectionnez **sites**  >  **administration et surveillance de Microsoft BitLocker**. Vérifiez que les éléments suivants s’affichent:

   * MBAMAdministrationService
   * MBAMComplianceStatusService
   * MBAMRecoveryAndHardwareService

8. Sur le serveur sur lequel sont configurés le site Web d’administration et de surveillance et le portail libre-service, ouvrez un navigateur Web à l’aide des informations d’identification d’administration.

9. Naviguez jusqu’au site Web suivant pour vérifier qu’il se charge correctement:
   * HTTPS (s):// \<MBAM Administration Server Name\> : \<port\> /Helpdesk/(confirmez chaque lien pour la navigation et les rapports)
   * http (s):// \<MBAM Administration Server Name\> : \<port\> /selfservice/

   > [!Note]
   > Il est supposé que vous avez configuré les fonctionnalités serveur sur le port par défaut sans chiffrement réseau. Si vous avez configuré les fonctionnalités du serveur sur un autre port ou répertoire virtuel, modifiez les URL pour inclure le port approprié. Par exemple: http (s):// \<host name\> : \<port\> /helpdesk/http (s):// \<host name\> : \<port\> / \<virtualdirectory\> /si les fonctionnalités du serveur ont été configurées pour utiliser le chiffrement réseau, remplacez http://par https://.
   
10. Accédez aux services Web suivants pour vérifier qu’ils se chargent correctement. Une page s’affiche pour indiquer que le service est en cours d’exécution. Toutefois, la page ne contient aucune métadonnée.

    * http (s):// \<MBAM Administration Server Name> : \<port> /MBAMAdministrationService/AdministrationService.svc
    * http (s):// \<MBAM Administration Server Name> : \<port> /MBAMUserSupportService/UserSupportService.svc
    * http (s):// \<MBAM Administration Server Name> : \<port> /MBAMComplianceStatusService/StatusReportingService.svc
    * http (s):// \<MBAM Administration Server Name> : \<port> /MBAMRecoveryAndHardwareService/CoreService.svc

### Étape 12: configurer les modèles de stratégie de groupe MBAM

Pour déployer MBAM, vous devez définir les paramètres de stratégie de groupe définissant les paramètres d’implémentation de MBAM pour le chiffrement de lecteur BitLocker. Pour effectuer cette tâche, vous devez copier les modèles de stratégie de groupe MBAM sur un serveur ou une station de travail qui peut exécuter la console de gestion des stratégies de groupe (GPMC) ou Advanced Group Policy Management (AGPM), puis modifier les paramètres.

> [!Important]
> Ne modifiez pas les paramètres de stratégie de groupe dans le nœud **BitLocker Drive Encryption** or MBAM ne fonctionne pas correctement. Lorsque vous configurez les paramètres de stratégie de groupe dans le nœud **MDOP MBAM (gestion du BitLocker)** , MBAM configure automatiquement les paramètres de **chiffrement de lecteur BitLocker** pour vous.
 
#### Copie des modèles de stratégie de groupe de MBAM 2,5

Avant d’installer le client MBAM, vous devez copier des objets de stratégie de groupe spécifiques MBAM (GPO) sur la station de travail de gestion. Ces objets de stratégie de groupe définissent les paramètres d’implémentation de MBAM pour BitLocker. Vous pouvez copier les modèles de stratégie de groupe sur n’importe quel serveur ou station de travail, qui est un serveur ou un ordinateur client compatible avec Windows, et qui peut exécuter la console de gestion des stratégies de groupe (GPMC) ou Advanced Group Policy Management (AGPM).

Pour plus d’informations, consultez [copie des modèles de stratégie de groupe MBAM 2,5](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/copying-the-mbam-25-group-policy-templates).
 
#### Modification des paramètres de l’objet de stratégie de MBAM 2,5

Après avoir créé les objets de stratégie de groupe nécessaires, vous devez déployer les paramètres de stratégie de groupe MBAM sur les ordinateurs clients de votre organisation. Pour afficher et créer des objets de stratégie de groupe, vous devez avoir installé la console de gestion des stratégies de groupe (GPMC) ou la gestion de la stratégie de groupe avancée.

Pour plus d’informations, reportez-vous à [modification des paramètres de stratégie de groupe MBAM 2,5](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/editing-the-mbam-25-group-policy-settings) et [planification des exigences de stratégie de groupe MBAM 2,5](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/planning-for-mbam-25-group-policy-requirements).
 
### Étape 13: déploiement du client MBAM 2,5

En fonction du moment où vous déployez le logiciel client d’administration et de surveillance de Microsoft BitLocker, vous pouvez activer BitLocker sur un ordinateur de votre organisation avant que l’utilisateur ne reçoive l’ordinateur ou ultérieurement en configurant une stratégie de groupe et en déployant le logiciel client MBAM à l’aide d’un système de déploiement de logiciels d’entreprise.
 
#### Déployer le client MBAM sur un ordinateur portable ou de bureau

Après avoir configuré les paramètres de stratégie de groupe, vous pouvez utiliser un produit système de déploiement de logiciels d’entreprise tel que Microsoft System Center 2012 Configuration Manager ou les services de domaine Active Directory (AD DS) pour déployer les fichiers du programme d’installation du client MBAM sur les ordinateurs cibles. Vous pouvez utiliser les fichiers MbamClientSetup.exe de la 32 ou de 64 bits ou les fichiers MBAMClient.msi 32 ou 64 bits. Celles-ci sont fournies conjointement avec le logiciel client MBAM.

Pour plus d’informations, reportez-vous à la rubrique [déploiement du client MBAM sur un ordinateur portable ou de bureau](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-deploy-the-mbam-client-to-desktop-or-laptop-computers-mbam-25).
 
#### Déploiement du client MBAM dans le cadre d’un déploiement Windows

Dans les organisations sur lesquelles les ordinateurs sont reçus et configurés de manière centralisée, vous pouvez installer le client MBAM pour gérer le chiffrement de lecteur BitLocker sur chaque ordinateur avant d’y écrire des données utilisateur. L’avantage de ce processus est que chaque ordinateur est alors conforme à BitLocker. Cette méthode ne repose pas sur l’action de l’utilisateur, car l’administrateur l’a déjà crypté. Une supposition essentielle pour ce scénario est que la stratégie de l’Organisation consiste à installer une image Windows d’entreprise avant que l’ordinateur ne soit remis à l’utilisateur. Si les paramètres de stratégie de groupe sont configurés pour exiger un code confidentiel, les utilisateurs sont invités à définir un code confidentiel après réception de la stratégie.

Pour plus d’informations, reportez-vous à la rubrique [déploiement du client MBAM dans le cadre d’un déploiement Windows](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-enable-bitlocker-by-using-mbam-as-part-of-a-windows-deploymentmbam-25).
 
#### Déploiement du client MBAM à l’aide d’une ligne de commande

Pour plus d’informations, reportez-vous à la rubrique [déploiement du client MBAM à l’aide d’une ligne de commande](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-deploy-the-mbam-client-by-using-a-command-line).

#### Post-déploiement de clients

À présent que vous avez terminé l’activité de déploiement, nous vous conseillons de passer en revue les journaux suivants et de déterminer s’il s’agit de rapports réussis avec la base de données MBAM.

## Forum Aux Questions

### Comment créer un serveur IIS dont le chargement est équilibré

* Le SPN doit être inscrit uniquement au nom convivial (par exemple: bitlocker.corp.net) et ne doit pas être inscrit aux serveurs IIS individuels.

* Si un certificat est utilisé, le certificat doit avoir les noms FQDN et NetBIOS entrés dans le champ **autre nom** de l’objet pour tous les serveurs IIS dans le groupe équilibrage de charge et également le nom convivial (par exemple: BitLocker.Corp.net). Dans le cas contraire, le certificat sera signalé comme n’étant pas approuvé par le navigateur lorsque vous naviguez vers des adresses à répartition de charge.

Pour plus d’informations, reportez-vous à la rubrique équilibrage de la [charge réseau IIS](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/planning-for-mbam-25-high-availability#a-href-idbkmk-load-balanceaiis-network-load-balancing) et [inscription des SPN pour le compte du pool d’applications](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/planning-how-to-secure-the-mbam-websites#registering-spns-for-the-application-pool-account).

### Comment configurer un certificat

* Vous devez avoir deux certificats. Un certificat est utilisé pour SQL Server et l’autre est utilisé pour les services Internet (IIS). Ils doivent être installés avant de démarrer l’installation d’MBAM.

* Nous vous recommandons d’utiliser le programme d’installation pour ajouter le certificat à la configuration IIS au lieu de modifier manuellement le fichier web.config.

* Le certificat n’est pas accepté par le configurateur MBAM si le champ «délivré à» sur le certificat ne correspond pas au nom du serveur. Dans ce cas, créez temporairement un certificat auto-signé à partir de la console IIS, puis utilisez-le dans le configurateur. Cette opération rend nsure que les applications Web sont installées pour SSL et HTTPs. Après cela, vous pouvez modifier le certificat en un à partir de liaisons IIS pour le site Web MBAM.

### Les autorisations SQL requises pour l’installation

Créez un compte pour le pool d’applications MBAM et attribuez-lui uniquement les autorisations SecurityAdmin, public et DBCreator.

Pour plus d’informations, voir Configuration d’une [base de données MBAM-autorisations minimum](https://blogs.technet.microsoft.com/dubaisec/2016/02/02/mbam-database-configuration-minimum-permissions/) .

> [!Note]
> * Dans certains cas, des autorisations supplémentaires sont requises pour les opérations d’installation et de mise à niveau initiales.
> * Utilisez un compte dont la SA est temporaire pour l’installation.
> * Ne démarrez pas le configurateur dans le contexte d’un compte d’utilisateur (exécuté en tant que) qui ne dispose pas des autorisations nécessaires pour modifier SQL Server, car cela entraînera des erreurs d’installation.
> * Vous devez être connecté en utilisant un compte disposant des autorisations sur SQL Server. Seules les bases de données SQL Server peuvent être créées ou mises à jour en exécutant MBAM Configurator à distance. Pour serveur SSRS, vous devez installer MBAM et exécuter le configurateur localement pour installer ou mettre à jour les rapports SSRS MBAM.

### Autorisation requise pour l’inscription de SPN

Un compte utilisé pour l’installation du portail IIS doit avoir une autorisation de type ServicePrincipalName et écrire des autorisations SPN validées. Sans ces autorisations, l’installation renverra un message d’avertissement indiquant qu’il n’est pas possible d’inscrire le SPN.

> [!Note]
> Le message d’avertissement suivant apparaît deux fois. Cela ne signifie pas que le SPN doit avoir deux objets enregistrés.

Pour plus d’informations, reportez-vous à la rubrique échec de la [configuration d’MBAM avec le message d’erreur «Register SPN différé»](https://support.microsoft.com/help/2754138/).

### Ai-je besoin de mettre à jour les modèles ADMX avec la dernière version?

Plusieurs options de système d’exploitation apparaissent dans le nœud racine MBAM de l’objet de stratégie de groupe après la mise à jour des modèles ADMX vers leurs dernières versions. Par exemple, Windows 7, Windows 8,1 et Windows 10, version 1511 et versions ultérieures.

Pour plus d’informations sur la mise à jour des modèles ADMX, voir les articles suivants:
* [Téléchargement et déploiement des modèles de stratégie de groupe MDOP (.admx)](https://docs.microsoft.com/microsoft-desktop-optimization-pack/solutions/how-to-download-and-deploy-mdop-group-policy--admx--templates)
* [Planification des exigences en matière de stratégie de groupe MBAM2.5](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/planning-for-mbam-25-group-policy-requirements)
* [Modèles d’administration de la stratégie de groupe Microsoft Desktop Optimization](https://www.microsoft.com/en-us/download/details.aspx?id=55531)
