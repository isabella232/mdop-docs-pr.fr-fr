---
title: Déploiement de MBAM 2.5 dans une configuration autonome
description: Présentation du déploiement de MBAM 2.5 dans une configuration autonome.
author: Deland-Han
ms.reviewer: dcscontentpm
manager: dansimp
ms.author: delhan
ms.sitesec: library
ms.prod: w10
ms.date: 09/16/2019
ms.openlocfilehash: 1ceccf3973bb131484f91917c2b80cd676d1c31b
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910469"
---
# <a name="deploying-mbam-25-in-a-standalone-configuration"></a>Déploiement de MBAM 2.5 dans une configuration autonome

Cet article fournit des instructions détaillées sur l’installation de Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 dans une configuration autonome. Dans ce guide, nous allons utiliser une configuration à deux serveurs. L’un des deux serveurs sera un serveur de base de données exécutant Microsoft SQL Server 2012. Ce serveur hébergera les bases de données et les rapports MBAM. Le serveur supplémentaire sera un serveur web Windows Server 2012 hébergeant « Administration et serveur de surveillance » et « Portail libre-service ».

## <a name="preparation-steps-before-installing-mbam-25-server-software"></a>Étapes de préparation avant l’installation du logiciel serveur MBAM 2.5

### <a name="step-1-installation-and-configuration-of-servers"></a>Étape 1 : Installation et configuration des serveurs

Avant de commencer à configurer MBAM 2.5, nous devons nous assurer que les deux serveurs sont configurés en conformité avec la configuration système requise de MBAM. Consultez la [configuration minimale requise pour MBAM](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/mbam-25-supported-configurations#-mbam-server-system-requirements)et sélectionnez une configuration qui répond à ces exigences. 

#### <a name="step-11-deploying-prerequisites-for-database-and-reporting-server"></a>Étape 1.1 : Déploiement des conditions préalables pour la base de données et le serveur de rapports

1. Installez et configurez un serveur exécutant Windows système d’exploitation Server 2008 R2 (ou ultérieur).

2. Installez Windows PowerShell 3.0.

3. Installez Microsoft SQL Server 2008 R2 ou une version ultérieure qui inclut le dernier Service Pack. Si vous installez une nouvelle instance de SQL Server pour MBAM, assurez-vous que le SQL Server que vous installez inclut le classement SQL_Latin1_General_CP1_CI_AS. Vous devez installer les fonctionnalités SQL Server suivantes :

    * Moteur de base de données
    * Reporting Services
    * Connectivité des outils clients
    * Outils de gestion – Complet

    > [!Note]
    > Si vous le souhaitez, vous pouvez également installer [la fonctionnalité Transparent Data Encryption (TDE) dans SQL Server](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/mbam-25-security-considerations).

    SQL Server Reporting Services doit être installé et configuré en mode « natif » et non en mode non configuré ou « SharePoint ».

    ![Les fonctionnalités SQL Server requises.](images/deploying-MBAM-1.png)

4. Si vous prévoyez d’utiliser SSL pour le site web d’administration et de surveillance, veillez à configurer SQL Server Reporting Services (SSRS) pour utiliser le protocole SSL (Secure Sockets Layer) avant de configurer le site web Administration et surveillance. Dans le cas contraire, la fonctionnalité Rapports utilisera le transport de données non chiffré (HTTP) au lieu du protocole HTTPS (Encrypted).

    Vous pouvez suivre [Configurer les connexions SSL](https://docs.microsoft.com/sql/reporting-services/security/configure-ssl-connections-on-a-native-mode-report-server?view=sql-server-2017) sur un serveur de rapports en mode natif pour configurer SSL sur le serveur de rapports.
    
    > [!Note]
    > Vous pouvez suivre le guide SQL Server’installation de votre version respective de SQL Server pour installer SQL Server. Les liens sont les suivants :
        > * [SQL Server 2014](https://docs.microsoft.com/sql/sql-server/install/planning-a-sql-server-installation?view=sql-server-2014)
        > * [SQL Server 2012](https://docs.microsoft.com/previous-versions/sql/sql-server-2012/bb500442(v=sql.110))
        > * [SQL Server 2008 R2](https://docs.microsoft.com/previous-versions/sql/sql-server-2012/bb500442(v=sql.110))

5. Dans la post-installation de SQL Server, veillez à configurer le compte d’utilisateur dans SQL Server et à attribuer les autorisations suivantes à l’utilisateur qui configurera la base de données MBAM et les rôles de rapport sur le serveur de base de données.

    Rôles pour l’instance de SQL Server :
        
    * dbcreator
    * processadmin

    Droits pour l’instance de SQL Server Reporting Services :
    
    * Créer des dossiers
    * Publier des rapports

Votre serveur de base de données est prêt pour la configuration des rôles MBAM 2.5. Passons au serveur suivant.

#### <a name="step-12-deploying-prerequisites-for-administration-and-monitoring-server"></a>Étape 1.2 : Déploiement des conditions préalables pour l’administration et le serveur de surveillance

Choisissez un serveur qui répond à la configuration matérielle, comme expliqué dans le document de configuration [requise de MBAM.](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/mbam-25-supported-configurations#-mbam-server-system-requirements) Il doit être en cours d Windows Server 2008 R2 ou un système d’exploitation ultérieur avec les derniers Service Packs et mises à jour. Une fois le serveur prêt, installez les rôles et fonctionnalités suivants :

##### <a name="roles"></a>Rôles

* Web Server (IIS) Management Tools (Select IIS Management Scripts and Tools.)

* Services de rôle serveur web

    * Fonctionnalités HTTP courantes<br />
      Contenu statique<br />
      Document par défaut

    * Développement d’applications<br />
      ASP.NET<br />
      Extensibilité .NET<br />
      ISAPI Extensions<br />
      Filtres ISAPI<br />
      Sécurité<br />
      Authentification Windows<br />
      Filtrage des demandes

    * Outils de gestion IIS des services Web

##### <a name="feature"></a>Fonctionnalité

* .NET Framework 4.5
  
  * Microsoft .NET Framework 4.5
  
    Pour Windows Server 2012 ou Windows Server 2012 R2, .NET Framework 4.5 est déjà installé pour ces versions de Windows Server. Toutefois, vous devez l’activer.
  
    Pour Windows Server 2008 R2, .NET Framework 4.5 n’est pas inclus dans Windows Server 2008 R2. Par conséquent, vous devez télécharger .NET Framework 4.5 et l’installer séparément.
  
  * WCF Activation<br />
    HTTP Activation<br />
    Activation non HTTP
  
  * TCP Activation
  
  * Windows Service d’activation des processus :<br />
    Modèle de processus<br />
    .NET Framework Environnement<br />
    API de configuration

Pour que le portail libre-service fonctionne, vous devez également télécharger et installer [ASP.NET MVC 4.0](https://go.microsoft.com/fwlink/?linkid=392271).

L’étape suivante consiste à créer les utilisateurs et groupes MBAM requis dans Active Directory.

### <a name="step-2-creating-users-and-groups-in-active-directory-domain-services"></a>Étape 2 : Création d’utilisateurs et de groupes dans les services de domaine Active Directory
 
Dans le cadre des conditions préalables, vous devez définir certains rôles et comptes utilisés dans MBAM pour fournir des droits de sécurité et d’accès à des serveurs et fonctionnalités spécifiques, tels que les bases de données qui s’exécutent sur l’instance de SQL Server et les applications web qui s’exécutent sur le serveur d’administration et de surveillance.

Créez les groupes et utilisateurs suivants dans Active Directory. (Vous pouvez utiliser n’importe quel nom pour les groupes et les utilisateurs.) Les utilisateurs n’ont pas besoin d’avoir des droits d’utilisateur supérieurs. Un compte d’utilisateur de domaine est suffisant. Vous devez spécifier le nom de ces groupes lors de la configuration de MBAM 2.5 :

* **MBAMAppPool**  

  **Type**: Domain User

  **Description :** utilisateur de domaine qui dispose d’autorisations en lecture ou en écriture sur la base de données de conformité et d’audit et la base de données de récupération pour permettre aux applications web d’accéder aux données et aux rapports dans ces bases de données. Il sera également utilisé par le pool d’applications pour les applications web.

  **Rôles de compte (lors de la configuration de MBAM)**:

  1. Compte de domaine du pool d’applications de service Web

  2. Utilisateur en lecture/écriture de la base de données de conformité et d’audit et de la base de données de récupération pour les rapports

* **MBAMROUser**

  **Type**: Domain User

  **Description**: utilisateur de domaine qui aura Read-Only accès à la base de données de conformité et d’audit pour permettre aux rapports d’accéder aux données de conformité et d’audit dans cette base de données. Ce sera également le compte d’utilisateur de domaine que l’instance SQL Server Reporting Services locale utilise pour accéder à la base de données de conformité et d’audit.

  **Rôles de compte (lors de la configuration de MBAM)**:

  1. Utilisateur en lecture seule de la base de données de conformité et d’audit pour les rapports

  2. Compte d’utilisateur de domaine de la base de données de conformité et d’audit

* **MBAMAdvHelpDsk**

  **Type**: Groupe de domaines

  **Description**: Groupe d’accès Utilisateurs du helpdesk avancé MBAM : groupe d’utilisateurs de domaine dont les membres ont accès à toutes les zones du site Web d’administration et de surveillance. Les utilisateurs qui ont ce rôle doivent entrer uniquement la clé de récupération, et non le domaine et le nom d’utilisateur de l’utilisateur, lorsqu’ils aident les utilisateurs à récupérer leurs lecteurs. Si un utilisateur est membre du groupe Utilisateurs du helpdesk MBAM et du groupe Utilisateurs du helpdesk avancé MBAM, les autorisations du groupe Utilisateurs du helpdesk avancé MBAM remplacent les autorisations du groupe du helpdesk MBAM.

  **Rôles de compte (lors de la configuration de MBAM)**: utilisateurs du helpdesk avancé MBAM

* **MBAMHelpDsk**

  **Type**: Groupe de domaines

  **Description**: Groupe d’accès Utilisateurs du helpdesk MBAM : groupe d’utilisateurs de domaine dont les membres ont accès aux zones Gérer le TPM et Drive Recovery du site Web d’administration et de surveillance de MBAM. Les personnes qui ont ce rôle doivent remplir tous les champs lorsqu’elles utilisent l’une ou l’autre option. Cela inclut le nom de domaine et le nom de compte de l’utilisateur.

  **Rôles de compte (lors de la configuration de MBAM)**: utilisateurs du helpdesk MBAM

* **MBAMRUGrp**

  **Type**: Groupe de domaines

  **Description**: groupe d’utilisateurs de domaine dont les membres ont un accès en lecture seule aux rapports dans la zone Rapports du site Web d’administration et de surveillance.

  **Rôles de compte (lors de la configuration de MBAM)**:

  1. Signale un groupe d’accès au domaine en lecture seule

  2. Groupe d’accès Utilisateurs du rapport MBAM

### <a name="step-3-optional-configure-and-install-ssl-certificate-on-administration-and-monitoring-server"></a>Étape 3 (facultative) : configurer et installer le certificat SSL sur le serveur d’administration et de surveillance

Bien qu’il soit facultatif, nous vous recommandons vivement d’utiliser un certificat pour sécuriser la communication entre le client MBAM et le site Web d’administration et de surveillance et les sites web du portail Self-Service. Nous vous déconseillons d’utiliser des certificats auto-signés pour des raisons de sécurité évidentes. Nous vous suggérons d’utiliser un certificat de type serveur Web provenant d’une autorité de certification de confiance. Pour ce faire, vous pouvez faire référence à la section « Utilisation du certificat approuvé par l’autorité de certification » à partir de [la base](https://support.microsoft.com/help/2754259)de 2754259 .

Une fois le certificat émis, vous devez l’ajouter au magasin personnel du serveur d’administration et de surveillance. Pour ajouter le certificat, ouvrez le magasin de certificats sur l’ordinateur local. Pour ce faire, procédez comme suit :

1. Sélectionnez l’démarrer avec le côté droit, puis sélectionnez Exécuter.

   ![Sélectionnez.](images/deploying-MBAM-2.png)

2. Tapez « MMC.EXE » (sans les guillemets), puis sélectionnez **OK.**

   ![Zone d’exécuter.](images/deploying-MBAM-3.png) 

3. Sélectionnez **Fichier** dans la nouvelle MMC que vous avez ouverte, puis sélectionnez **Ajouter/Supprimer un logiciel en snap-in.**
   
   ![Sélectionnez.](images/deploying-MBAM-4.png)

4. Mettez en surbrillez le logiciel en snap-in **Certificats,** puis sélectionnez **Ajouter.**

   ![Ajouter ou supprimer des logiciels en snap-in.](images/deploying-MBAM-5.png)

5. Sélectionnez **l’option Compte** d’ordinateur, puis sélectionnez **Suivant.**
   
   ![Fenêtre en snap-in Certificats.](images/deploying-MBAM-6.png)

6. Sélectionnez **Ordinateur local** sur l’écran suivant, puis sélectionnez **Terminer.**
   
   ![Fenêtre Sélectionner un ordinateur.](images/deploying-MBAM-7.png)

7. Vous avez maintenant ajouté le logiciel en snap-in Certificats. Cela vous permettra d’utiliser des certificats dans le magasin de certificats de votre ordinateur.

   ![Ajouter ou supprimer des logiciels en snap-in.](images/deploying-MBAM-8.png)

8. Importez le certificat de serveur web dans le magasin de certificats de votre ordinateur.

   Maintenant que vous avez accès au logiciel en ligne Certificats, vous pouvez importer le certificat de serveur web dans le magasin de certificats de votre ordinateur. Pour ce faire, suivez les étapes suivantes.

9. Ouvrez le logiciel en snap-in Certificats (ordinateur local), puis accédez à **Personnel,** puis **Certificats**.
   
   ![Fenêtre de logiciel en snap-in Certificats (ordinateur local).](images/deploying-MBAM-9.png)

   > [!Note]
   > Le logiciel en snap-in Certificats n’est peut-être pas répertorié. Si ce n’est pas le cas, aucun certificat n’est installé.

10. Right-select **Certificates**, select **All Tasks,** and then select **Import**.

    ![Fenêtre de logiciel en snap-in Certificats (ordinateur local).](images/deploying-MBAM-10.png)

11. Lorsque l’Assistant démarre, sélectionnez **Suivant.** Accédez au fichier que vous avez créé qui contient votre certificat de serveur et votre clé privée, puis sélectionnez **Suivant**.

    ![Fenêtre De l’Assistant Importation de certificat.](images/deploying-MBAM-11.png)

12. Entrez le mot de passe si vous en avez spécifié un pour le fichier lors de sa création.

   ![Fenêtre Entrer le mot de passe.](images/deploying-MBAM-12.png)

   > [!Note]
   > Assurez-vous que l’option Marquer la clé comme **exportable** est sélectionnée si vous souhaitez pouvoir exporter à nouveau la paire de clés à partir de cet ordinateur. En tant que mesure de sécurité supplémentaire, vous pouvez laisser cette option effacée pour vous assurer que personne ne peut effectuer de sauvegarde de votre clé privée.
 
13. Sélectionnez **Suivant,** puis **sélectionnez** le magasin de certificats dans lequel vous souhaitez enregistrer le certificat.

    ![Fenêtre De l’Assistant Importation de certificat.](images/deploying-MBAM-13.png)

    > [!Note]
    > Vous devez sélectionner **Personnel,** car il s’agit d’un certificat de serveur web. Si vous avez inclus le certificat dans la hiérarchie de certification, il sera également ajouté à ce magasin.
 
14. Sélectionnez **Suivant,** puis **Terminer.**

    ![Fenêtre De l’Assistant Importation de certificat.](images/deploying-MBAM-14.png)

Vous verrez maintenant le certificat de serveur de votre serveur web dans la liste Certificats personnels. Elle sera notée par le nom commun du serveur. (Vous pouvez le trouver dans la section objet du certificat.)

Pour plus d’informations :

[Considérations relatives à la sécurité pour MBAM 2.5](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/mbam-25-security-considerations)

[Planification de la sécurisation des sites web MBAM](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/planning-how-to-secure-the-mbam-websites)

L’étape suivante consiste à inscrire un nom de principe de service pour le compte du pool d’applications.

### <a name="step-4-configuring-ssl-certificate-for-mbam-web-server"></a>Étape 4 : Configuration du certificat SSL pour le serveur web MBAM

Si vous utilisez la communication SSL entre le client et le serveur, vous devez vous assurer que le certificat possède des OID d’utilisation améliorée de la clé (1.3.6.1.5.5.7.3.1) et (1.3.6.1.5.5.7.3.2). Autrement dit, vous devez vous assurer que l’authentification serveur et l’authentification client sont ajoutées.

Si vous recevez une erreur de certificat lorsque vous essayez de parcourir les URL de service, vous utilisez un certificat qui a été émis sous un autre nom ou vous naviguez à l’aide d’une URL incorrecte.

Bien que le navigateur puisse vous envoyer un message d’erreur de certificat, mais vous laisser continuer, le service web MBAM n’ignorera pas les erreurs de certificat et bloquera la connexion. Vous remarquerez les erreurs liées aux certificats dans le journal des événements d’administration MBAM du client MBAM. Si vous utilisez un alias pour vous connecter au serveur d’administration et de surveillance, vous devez émettre un certificat pour le nom d’alias. Autrement dit, le nom du sujet du certificat doit être le nom d’alias et le nom DNS du serveur local doit être ajouté au champ **Autre** nom de l’objet du certificat.

Exemple :

Si le nom virtuel est « bitlocker.contoso.com » et que le nom du serveur d’administration et de surveillance MBAM est « adminserver.contoso.com », le certificat **** doit être émis à bitlocker.contoso.com (nom du sujet) et adminserver.contoso.com doit être ajouté au champ Autre nom du sujet du certificat.

De même, si plusieurs serveurs d’administration et de surveillance sont installés pour équilibrer la charge à l’aide d’un équilibrage de charge, vous devez émettre le certificat SSL au nom virtuel. Autrement dit, le champ nom du sujet du certificat doit avoir le nom virtuel **** et les noms de tous les serveurs locaux doivent être ajoutés dans le champ Autre nom de l’objet du certificat.

Exemple :

Si le nom virtuel est « bitlocker.contoso.com » et que les serveurs sont « adminserver1.contoso.com » et « adminiserver2.contoso.com », le certificat doit être émis à bitlocker.contoso.com (nom d’objet) et adminserver1.contoso.com, et adminiserver2.contoso.com doit être ajouté au champ Autre nom de l’objet du certificat. ****

Les étapes de configuration de la communication SSL à l’aide de MBAM sont décrites dans l’article suivant de la Base de [connaissances : KB 2754259](https://support.microsoft.com/help/2754259).

### <a name="step-5-register-spns-for-the-application-pool-account-and-configure-constrained-delegation"></a>Étape 5 : inscrire SPNS pour le compte du pool d’applications et configurer la délégation contrainte

> [!Note]
> La délégation contrainte est requise uniquement pour la 2.5 et n’est pas requise pour 2.5 Service Pack 1 et ultérieur.

Pour permettre aux serveurs MBAM d’authentifier les communications à partir du site Web d’administration et de surveillance et du portail Self-Service, vous devez inscrire un nom principal de service (SPN) pour le nom d’hôte sous le compte de domaine que vous utilisez pour le pool d’applications web. L’article suivant contient des instructions pas à pas pour inscrire des SNS : Planification de la sécurisation des sites [web MBAM](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/planning-how-to-secure-the-mbam-websites)

Une fois que le SPN est configuré, vous devez configurer la délégation contrainte sur le SPN. Pour ce faire, procédez comme suit :

1. Go to Active Directory, and find the app pool credentials that you configured for MBAM websites in the previous steps.

2. Cliquez avec le bouton droit sur les informations d’identification, puis sélectionnez les **propriétés.**

3. Sélectionnez **l’onglet** Délégation.

4. Sélectionnez l’option pour l’authentification Kerberos.

5. Sélectionnez **Parcourir,** puis recherchez à nouveau les informations d’identification de votre pool d’applications. Vous devriez ensuite voir tous les SNS qui sont mis en place sur le compte d’creds du pool d’applications. (Le SPN doit ressembler à « http/bitlocker.fqdn.com »). Mettez en surbrillez le nom de domaine complet identique au nom d’hôte que vous avez spécifié lors de l’installation de MBAM.

6. Sélectionnez **OK**.

Vous êtes maintenant en bonne condition préalable. Dans les étapes suivantes, vous installerez le logiciel MBAM sur les serveurs et le configurerez.

## <a name="installing-and-configuring-mbam-25-server-software"></a>Installation et configuration du logiciel serveur MBAM 2.5

### <a name="step-6-install-mbam-25-server-software"></a>Étape 6 : Installer le logiciel serveur MBAM 2.5 

Pour installer le logiciel MBAM Server à l’aide de l’Assistant Administration et installation de la surveillance de Microsoft BitLocker à la fois sur le serveur de base de données et sur le serveur d’administration et de surveillance, suivez ces étapes.

1. Sur le serveur sur lequel vous souhaitez installer MBAM, exécutez MBAMserversetup.exe pour démarrer l’Assistant Installation de l’administration et de la surveillance de Microsoft BitLocker.

2. Dans la page d’accueil, sélectionnez **Suivant.**

3. Lisez et acceptez le contrat de licence logiciel Microsoft, puis sélectionnez **Suivant** pour poursuivre l’installation.

4. Décidez s’il faut utiliser Microsoft Update lorsque vous recherchez des mises à jour, puis sélectionnez **Suivant**.

5. Décidez s’il faut participer au Programme d’amélioration du client, puis sélectionnez **Suivant.**

6. Pour démarrer l’installation, sélectionnez **Installer.**

7. Pour configurer les fonctionnalités serveur après l’installation du logiciel MBAM Server, cochez la case Exécuter la configuration du serveur **MBAM** après la fermeture de l’Assistant. Vous pouvez également configurer MBAM ultérieurement à l’aide du raccourci **Configuration de MBAM Server** créé par l’installation du serveur dans votre menu **Démarrer.**

8. Sélectionnez **Terminer.**

Pour plus d’informations, voir Installation du logiciel [serveur MBAM 2.5.](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/installing-the-mbam-25-server-software)

### <a name="step-7-configure-mbam-25-database-and-reports-role"></a>Étape 7 : Configurer le rôle de base de données et de rapports MBAM 2.5

Dans cette étape, nous allons configurer les bases de données MBAM 2.5 et le composant de rapports à l’aide de l’Assistant MBAM :

1. Configurez la base de données de conformité et d’audit et la base de données de récupération à l’aide de l’Assistant :
   
   1. Sur le serveur sur lequel vous souhaitez configurer les bases de données, démarrez **l’Assistant Configuration de MBAM Server.** Vous pouvez sélectionner **Configuration du serveur MBAM** dans le menu **Démarrer** pour ouvrir l’Assistant.

   2. Sélectionnez **Ajouter de nouvelles fonctionnalités,** sélectionnez Base de données de conformité **et d’audit,** Base de données de récupération et **rapports,** puis sélectionnez **Suivant**. L’Assistant vérifie que toutes les conditions préalables pour les bases de données sont remplies.

   3. Si la vérification des conditions préalables réussit, **sélectionnez Suivant** pour continuer. Dans le cas contraire, résolvez les conditions préalables manquantes, puis **sélectionnez Vérifier les conditions préalables à nouveau.**
   
   4. À l’aide des descriptions suivantes, entrez les valeurs de champ dans l’Assistant :

2. Base de données de conformité et d’audit

   |Champ   |Description|
   |-------|-------|
   |SQL Server nom |Nom du serveur sur lequel vous configurez la base de données de conformité et d’audit. <br /> Vous devez ajouter une exception sur l’ordinateur de la base de données de conformité et d’audit pour activer le trafic entrant entrant sur SQL Server port. Le numéro de port par défaut est 1433.|
   |SQL Server de base de données    |Nom de l’instance de base de données dans laquelle les données de conformité et d’audit seront stockées. Si vous utilisez l’instance par défaut, vous devez laisser ce champ vide. Vous devez également spécifier l’emplacement des informations de base de données.|
   |Nom de la base de données   |Nom de la base de données qui stockera les données de conformité. Vous devez noter le nom de la base de données que vous spécifiez ici, car vous de aurez à fournir ces informations dans les étapes ultérieures.|
   |Utilisateur ou groupe de domaines d’autorisation en lecture-écriture  |Spécifiez le nom de l’utilisateur MBAMAppPool tel que configuré à l’étape 2.|
   |Utilisateur ou groupe de domaines d’accès en lecture seule   |Spécifiez le nom de l’utilisateur MBAMROUser tel que configuré à l’étape 2.|

3. Base de données de récupération.

   |Champ   |Description|
   |-----|-----|
   |SQL Server nom |Nom du serveur sur lequel vous configurez la base de données de récupération. Vous devez ajouter une exception sur l’ordinateur de la base de données de récupération pour activer le trafic entrant entrant sur SQL Server port. Le numéro de port par défaut est 1433.|
   |SQL Server de base de données    |Nom de l’instance de base de données dans laquelle les données de récupération seront stockées. Si vous utilisez l’instance par défaut, vous devez laisser ce champ vide. Vous devez également spécifier l’emplacement des informations de base de données.|
   |Nom de la base de données   |Nom de la base de données qui stockera les données de récupération.|
   |Utilisateur ou groupe de domaines d’autorisation en lecture-écriture  |Utilisateur de domaine ou groupe autorisé à accéder en lecture/écriture à cette base de données pour permettre aux applications web d’accéder aux données et aux rapports de cette base de données. <br />Si vous entrez un utilisateur dans ce champ, il doit s’agit de la même valeur que la valeur du champ de compte de domaine du **pool d’applications** de service Web de la page Configurer les applications **Web.** <br />Si vous entrez un groupe dans ce champ, la valeur du champ de compte de domaine du **pool d’applications** de service Web de la page Configurer les applications **Web** doit être membre du groupe que vous entrez dans ce champ.|
   
   Lorsque vous avez terminé vos entrées, sélectionnez **Suivant**. L’Assistant vérifie que toutes les conditions préalables pour les bases de données sont remplies.
   
   Si la vérification des conditions préalables réussit, **sélectionnez Suivant** pour continuer. Dans le cas contraire, résolvez les conditions préalables manquantes, puis sélectionnez **à nouveau Suivant.**

4. Rapports.

   |Champ   |Description|
   |----|----|
   |SQL Server Reporting Services instance  |Instance de SQL Server Reporting Services où les rapports seront configurés. Si vous utilisez l’instance par défaut, vous devez laisser ce champ vide.|
   |Groupe de domaines de rôle de rapport |Spécifiez le nom de MBAMRUGrp comme mentionné à l’étape 2.|
   |SQL Server nom |Nom du serveur sur lequel la base de données de conformité et d’audit est configurée.|
   |SQL Server de base de données    |Nom de l’instance de base de données dans laquelle les données de conformité et d’audit sont configurées. Si vous utilisez l’instance par défaut, vous devez laisser ce champ vide. <br />Vous devez ajouter une exception sur l’ordinateur de rapports pour activer le trafic entrant sur le port du serveur de rapports. (Le port par défaut est 80.)|
   |Nom de la base de données|  Nom de la base de données de conformité et d’audit. Par défaut, le nom de la base de données est État de conformité MBAM.|
   |Compte de domaine de la base de données de conformité et d’audit    |Spécifiez le nom de l’utilisateur MBAMROUser tel que configuré à l’étape 2.|
   
   Lorsque vous avez terminé vos entrées, sélectionnez **Suivant**. L’Assistant vérifie que toutes les conditions préalables pour la fonctionnalité Rapports sont remplies. Sélectionnez Suivant pour continuer. Dans la page **Résumé,** examinez les fonctionnalités qui seront ajoutées.
   
   Pour plus d’informations, voir l’article suivant : Comment configurer les bases de données [MBAM 2.5](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-configure-the-mbam-25-databases).

### <a name="step-8-configure-the-mbam-25-web-applications-role"></a>Étape 8 : Configurer le rôle des applications Web MBAM 2.5

1. Sur le serveur sur lequel vous souhaitez configurer les applications web, démarrez l’Assistant Configuration de MBAM Server. Vous pouvez sélectionner **Configuration du serveur MBAM** dans le menu **Démarrer** pour ouvrir l’Assistant.

2. Sélectionnez **Ajouter de nouvelles fonctionnalités,** sélectionnez Le site **web d’administration** et de surveillance et le portail **libre-service,** puis sélectionnez **Suivant.** L’Assistant vérifie que toutes les conditions préalables pour les bases de données sont remplies.

3. Si la vérification des conditions préalables réussit, **sélectionnez Suivant** pour continuer. Dans le cas contraire, résolvez les conditions préalables manquantes, puis **sélectionnez Vérifier les conditions préalables à nouveau.**

4. Utilisez les descriptions suivantes pour entrer les valeurs de champ dans l’Assistant.

   |Champ   |Description|
   |-----|-----|
   |Certificat de sécurité    |Sélectionnez un certificat précédemment créé à l’étape 3 pour chiffrer éventuellement la communication entre les services web et le serveur sur lequel vous configurez le site Web d’administration et de surveillance. Si vous sélectionnez Ne pas utiliser de certificat, votre communication web risque de ne pas être sécurisée.|
   |Nom de l'hôte   |Nom de l’ordinateur hôte sur lequel vous configurez le site Web d’administration et de surveillance. <br />Il ne doit pas être le nom d’hôte de l’ordinateur, il peut s’agit de n’importe quoi. Toutefois, si le nom d’hôte est différent du nom netbios de l’ordinateur, vous devez créer un enregistrement A et vous assurer que le SPN utilise le nom d’hôte personnalisé, et non le nom netbios. Cela est courant dans les scénarios d’équilibrage de charge.|
   |Chemin d’installation   |Chemin d’accès sur lequel vous installez le site Web d’administration et de surveillance.|
   |Port    |Numéro de port à utiliser pour la communication de site web. <br /> Vous devez définir une exception de pare-feu pour activer la communication via le port spécifié.|
   |Compte de domaine et mot de passe du pool d’applications de service Web    |Spécifiez le compte d’utilisateur et le mot de passe de l’utilisateur MBAMAppPool comme configuré à l’étape 2. <br /> Pour une sécurité améliorée, définissez le compte spécifié dans les informations d’identification pour qu’il soit limité par des droits d’utilisateur. Définissez également le mot de passe du compte pour qu’il n’expire jamais.|

5. Vérifiez que le compte IIS_IUSRS intégré ou le compte du pool d’applications **a** été ajouté à l’emprunt d’identité d’un **client** après l’authentification et que les paramètres de sécurité locale se connectent en tant que travail par lot.

   Pour vérifier si le **** compte **a** été ajouté aux paramètres de sécurité **** locaux, ouvrez l’éditeur de stratégie de sécurité **locale,** développez le nœud Stratégies locales, sélectionnez le nœud Attribution des droits d’utilisateur, puis double-sélectionnez Emprunt d’identité d’un **client** après l’authentification et connectez-vous en tant que stratégies de travail par lot dans le volet droit.

6. Utilisez les descriptions de champ suivantes pour configurer les informations de connexion dans l’Assistant pour la base de données de conformité et d’audit.
   |Champ   |Description|
   |------|------|
   |SQL Server nom |Nom du serveur sur lequel la base de données de conformité et d’audit est configurée.|
   |SQL Server de base de données    |Nom de l’instance de SQL Server (par exemple) et sur laquelle la base de données de conformité et \<Server Name\> d’audit est configurée. Laissez ce paramètre vide si vous utilisez l’instance par défaut.|
   |Nom de la base de données   |Nom de la base de données de conformité et d’audit. Par défaut, il s’agit du « statut de conformité MBAM ».|

7. Utilisez les descriptions de champ suivantes pour configurer les informations de connexion dans l’Assistant pour la base de données de récupération.
   |Champ   |Description|
   |----|----|
   |SQL Server nom |Nom du serveur sur lequel la base de données de récupération est configurée.|
   |SQL Server de base de données    |Nom de l’instance de SQL Server (par exemple) sur laquelle la base de données \<Server Name\> de récupération est configurée. Laissez ce paramètre vide si vous utilisez l’instance par défaut.|
   |Nom de la base de données   |Nom de la base de données de récupération. Par défaut, il s’agit de « Récupération et matériel MBAM ».|

8. Utilisez les descriptions suivantes pour entrer les valeurs de champ dans l’Assistant afin de configurer le site Web d’administration et de surveillance.
   |Champ   |Description|
   |----|----|
   |Groupe de domaines de rôles d’aide avancée |Spécifiez le nom du groupe MBAMAdvHelpDsk tel que configuré à l’étape 2.|
   |Groupe de domaines de rôle du helpdesk  |Spécifiez le nom du groupe MBAMHelpDsk tel que configuré à l’étape 2.|
   |Utiliser l’intégration System Center Configuration Manager des données |Cochez cette case.     |
   |Groupe de domaines de rôle de rapport |Spécifiez le nom du groupe MBAMRUGrp tel que configuré à l’étape 2.    |
   |SQL Server Reporting Services URL   |Spécifiez l’URL du service Web pour le serveur SSRS sur lequel les rapports MBAM sont configurés. Vous trouverez ces informations en vous connectant à Reporting Services Configuration Manager sur le serveur de base de données. <br /> Exemple de nom de domaine complet : https://MyReportServer.Contoso.com/ReportServer <br />Exemple de nom d’hôte personnalisé : https://MyReportServer/ReportServer|
   |Répertoire virtuel   |Répertoire virtuel du site Web d’administration et de surveillance. Ce nom correspond au répertoire physique du site web sur le serveur et est appendé au nom d’hôte du site web. Par exemple : <br />http(s):// *\<host name\>* : *\<port\>* /HelpDesk/ <br />Si vous ne spécifiez pas de répertoire virtuel, la valeur HelpDesk sera utilisée.     |

9. Utilisez la description suivante pour entrer les valeurs de champ dans l’Assistant afin de configurer Self-Service Portal.

   |Champ   |Description|
   |----|----|
   |Répertoire virtuel   |Répertoire virtuel de l’application web. Ce nom correspond au répertoire physique du site web sur le serveur et est appendé au nom d’hôte du site web. Par exemple :<br />http(s):// *\<host name\>* : *\<port\>* /SelfService/<br /> Si vous ne spécifiez pas de répertoire virtuel, la valeur « SelfService » est utilisée.|

10. Lorsque vous avez terminé vos entrées, sélectionnez **Suivant**. L’Assistant vérifie que toutes les conditions préalables pour les applications web sont remplies.

11. Sélectionnez **Suivant** pour continuer.

12. Dans la page **Résumé,** examinez les fonctionnalités qui seront ajoutées.

13. Sélectionnez **Ajouter** pour ajouter les applications web au serveur, puis sélectionnez **Fermer.**

## <a name="customizing-and-validating-steps-after-installing-mbam-25-server-software"></a>Personnalisation et validation des étapes après l’installation du logiciel serveur MBAM 2.5

### <a name="step-9-customizing-the-self-server-portal-for-your-organization"></a>Étape 9 : Personnalisation du portail libre-serveur pour votre organisation

Pour personnaliser le portail Self-Service en ajoutant un texte d’avis personnalisé, le nom de votre société, des pointeurs vers plus d’informations, etc., voir Personnalisation du portail Self-Service pour votre [organisation.](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/customizing-the-self-service-portal-for-your-organization)
 
### <a name="step-10-configure-the-self-server-portal-if-client-computers-cannot-access-the-cdn"></a>Étape 10 : Configurer le portail libre-serveur si les ordinateurs clients ne peuvent pas accéder au CDN 

Déterminez si vos ordinateurs clients ont accès à microsoft AJAX réseau de distribution de contenu (CDN). Le CDN donne au portail Self-Service l’accès dont il a besoin pour certains fichiers JavaScript. Si vous ne configurez pas le portail Self-Service lorsque les ordinateurs clients ne peuvent pas accéder au CDN, seuls le nom de la société et le compte sous lesquels l’utilisateur s’est inscrit s’affichent. Aucun message d’erreur ne s’affiche.

Effectuez l'une des opérations suivantes :

* Si vos ordinateurs clients ont accès au CDN, ne faites rien. La configuration Self-Service portail d’entreprise est terminée.

* Si vos ordinateurs clients n’ont pas accès au CDN, suivez les étapes de la procédure de configuration du portail Self-Service lorsque les ordinateurs clients ne peuvent pas accéder à [Microsoft réseau de distribution de contenu](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-configure-the-self-service-portal-when-client-computers-cannot-access-the-microsoft-content-delivery-network).

### <a name="step-11-validate-the-mbam-25-server-feature-configuration"></a>Étape 11 : Valider la configuration de la fonctionnalité serveur MBAM 2.5 

Pour valider votre déploiement MBAM Server afin d’utiliser la topologie autonome, suivez ces étapes.

1. Sur chaque serveur sur lequel une fonctionnalité **** MBAM est déployée, sélectionnez Programmes et fonctionnalités du Panneau  >  ****  >  **de contrôle.** Vérifiez que **Microsoft BitLocker Administration and Monitoring** apparaît dans la liste Programmes et **fonctionnalités.**
   > [!Note]
   > Pour effectuer la validation, vous devez utiliser un compte de domaine qui dispose d’informations d’identification d’administration d’ordinateur local sur chaque serveur.

2. Sur le serveur sur lequel la base de données de récupération est configurée, ouvrez SQL Server Management Studio et vérifiez que la base de données de récupération et de matériel **MBAM** est configurée.

3. Sur le serveur sur lequel la base de données de conformité et d’audit est configurée, ouvrez SQL Server Management Studio et vérifiez que la base de données d’état de conformité MBAM est configurée.

4. Sur le serveur sur lequel la fonctionnalité Rapports est configurée, ouvrez un navigateur web à l’aide des informations d’identification d’administration et accédez à la page d’accueil du site SQL Server Reporting Services site.
   
   L’emplacement de la page d’accueil par SQL Server Reporting Services instance de site est le suivant : http(s):// *\<MBAM Reports Server Name\>* : *\<port\>* /Reports.aspx
   
   Pour rechercher l’URL réelle, utilisez l’outil Gestionnaire de configuration de Reporting Services et sélectionnez les instances que vous avez spécifiées lors de l’installation.
   
5. Vérifiez qu’un dossier de rapports nommé Microsoft BitLocker Administration and Monitoring contient une source de données nommée MalteDataSource. Cette source de données contient des dossiers dont les noms représentent les paramètres régionaux de langue (par exemple, en-us). Les rapports sont dans les dossiers de langue.

   > [!Note]
   > Si SQL Server Reporting Services (SSRS) a été configuré en tant qu’instance nommée, l’URL doit ressembler à ce qui suit : http(s):// \<MBAM Reports Server Name\> : \<port\> /Reports_\<SSRS Instance Name\>
   >
   > Si SSRS n’a pas été configuré pour utiliser le protocole SSL (Secure Socket Layer), l’URL des rapports est définie sur « HTTP » au lieu de « HTTPS » lorsque vous installez le serveur MBAM. Si vous allez ensuite sur le site Web d’administration et de surveillance (également appelé Helpdesk) et sélectionnez un rapport, vous recevez le message suivant : « Seul le contenu sécurisé est affiché ». Pour afficher le rapport, **sélectionnez Afficher tout le contenu.**

6. Sur le serveur sur lequel la fonctionnalité Site web d’administration et de surveillance est configurée, exécutez le Gestionnaire de serveur, accédez à **Rôles,** puis sélectionnez Serveur **Web (IIS)**  >  **Internet Information Services (IIS).**

7. Dans **Connexions,** accédez aux sites d’administration et de \<computer name\> surveillance de Microsoft ****  >  **BitLocker, puis sélectionnez-les.** Vérifiez que les informations suivantes sont répertoriées :

   * MBAMAdministrationService
   * MBAMComplianceStatusService
   * MBAMRecoveryAndHardwareService

8. Sur le serveur sur lequel le site Web d’administration et de surveillance et le portail Self-Service sont configurés, ouvrez un navigateur web à l’aide d’informations d’identification administratives.

9. Accédez aux sites web suivants pour vérifier qu’ils se chargent correctement :
   * https(s):// \<MBAM Administration Server Name\> : \<port\> /HelpDesk/ (confirmez chaque lien pour la navigation et les rapports)
   * http(s):// \<MBAM Administration Server Name\> : \<port\> /SelfService/

   > [!Note]
   > Il est supposé que vous avez configuré les fonctionnalités serveur sur le port par défaut sans chiffrement réseau. Si vous avez configuré les fonctionnalités serveur sur un autre port ou répertoire virtuel, modifiez les URL pour inclure le port approprié. Par exemple : http(s):// \<host name\> : \<port\> /HelpDesk/ http(s):// : / Si les fonctionnalités serveur ont été configurées pour utiliser le chiffrement réseau, modifiez http:// en \<host name\> \<port\> / \<virtualdirectory\> https://.
   
10. Accédez aux services web suivants pour vérifier qu’ils se chargent correctement. Une page s’ouvre pour indiquer que le service est en cours d’exécution. Toutefois, la page n’affiche aucune métadonnées.

    * http(s):// \<MBAM Administration Server Name> : \<port> /MBAMAdministrationService/AdministrationService.svc
    * http(s):// \<MBAM Administration Server Name> : \<port> /MBAMUserSupportService/UserSupportService.svc
    * http(s):// \<MBAM Administration Server Name> : \<port> /MBAMComplianceStatusService/StatusReportingService.svc
    * http(s):// \<MBAM Administration Server Name> : \<port> /MBAMRecoveryAndHardwareService/CoreService.svc

### <a name="step-12-configure-the-mbam-group-policy-templates"></a>Étape 12 : Configurer les modèles de stratégie de groupe MBAM

Pour déployer MBAM, vous devez définir des paramètres de stratégie de groupe qui définissent les paramètres d’implémentation MBAM pour le chiffrement de lecteur BitLocker. Pour effectuer cette tâche, vous devez copier les modèles de stratégie de groupe MBAM sur un serveur ou une station de travail qui peut exécuter la Console de gestion des stratégies de groupe (GPMC) ou la Gestion avancée des stratégies de groupe (AGPM), puis modifier les paramètres.

> [!Important]
> Ne modifiez pas les paramètres de stratégie de groupe dans le nœud chiffrement de lecteur **BitLocker,** sinon MBAM ne fonctionne pas correctement. Lorsque vous configurez les paramètres de stratégie de groupe dans le nœud **MDOP MBAM (BitLocker Management),** MBAM configure automatiquement les paramètres de chiffrement de lecteur **BitLocker** pour vous.
 
#### <a name="copying-the-mbam-25-group-policy-templates"></a>Copie des modèles de stratégie de groupe MBAM 2.5

Avant d’installer le client MBAM, vous devez copier des objets de stratégie de groupe spécifiques à MBAM sur la station de travail de gestion. Ces GFO définissent les paramètres d’implémentation MBAM pour BitLocker. Vous pouvez copier les modèles de stratégie de groupe sur n’importe quel serveur ou station de travail qui est un serveur ou un ordinateur client Windows pris en charge et qui peut exécuter la Console de gestion des stratégies de groupe (GPMC) ou la Gestion avancée des stratégies de groupe (AGPM).

Pour plus d’informations, voir Copier les modèles de stratégie de groupe [MBAM 2.5.](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/copying-the-mbam-25-group-policy-templates)
 
#### <a name="editing-mbam-25-gpo-settings"></a>Modification des paramètres d’un GPO MBAM 2.5

Après avoir créé les GGP nécessaires, vous devez déployer les paramètres de stratégie de groupe MBAM sur les ordinateurs clients de votre organisation. Pour afficher et créer des GPM, vous devez avoir installé la Console de gestion des stratégies de groupe (GPMC) ou la Gestion avancée des stratégies de groupe (AGPM).

Pour plus d’informations, voir [Editing the MBAM 2.5 Group Policy Paramètres](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/editing-the-mbam-25-group-policy-settings) and [Planning for MBAM 2.5 Group Policy Requirements](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/planning-for-mbam-25-group-policy-requirements).
 
### <a name="step-13-deploying-the-mbam-25-client"></a>Étape 13 : Déploiement du client MBAM 2.5

Selon le moment où vous déployez le logiciel client d’administration et de surveillance De Microsoft BitLocker, vous pouvez activer BitLocker sur un ordinateur de votre organisation avant que l’utilisateur ne reçoive l’ordinateur ou par la suite en configurant la stratégie de groupe et en déployant le logiciel client MBAM à l’aide d’un système de déploiement de logiciels d’entreprise.
 
#### <a name="deploy-the-mbam-client-to-desktop-or-portable-computers"></a>Déployer le client MBAM sur des ordinateurs de bureau ou portables

Après avoir configuré les paramètres de stratégie de groupe, vous pouvez utiliser un produit de système de déploiement de logiciels d’entreprise tel que Microsoft System Center 2012 Configuration Manager ou Active Directory Domain Services (AD DS) pour déployer les fichiers d’installation du client MBAM Windows Installer sur des ordinateurs cibles. Vous pouvez utiliser les fichiers MbamClientSetup.exe 32 bits ou 64 bits ou les fichiers MBAMClient.msi 32 ou 64 bits. Ils sont fournis avec le logiciel client MBAM.

Pour plus d’informations, [voir Comment déployer le client MBAM](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-deploy-the-mbam-client-to-desktop-or-laptop-computers-mbam-25)sur des ordinateurs de bureau ou portables .
 
#### <a name="deploy-the-mbam-client-as-part-of-a-windows-deployment"></a>Déployer le client MBAM dans le cadre d’un déploiement Windows de gestion

Dans les organisations dans lesquelles les ordinateurs sont reçus et configurés de manière centralisée, vous pouvez installer le client MBAM pour gérer le chiffrement de lecteur BitLocker sur chaque ordinateur avant d’y écrire des données utilisateur. L’avantage de ce processus est que chaque ordinateur est alors conforme à BitLocker. Cette méthode ne repose pas sur l’action de l’utilisateur, car l’administrateur a déjà chiffré l’ordinateur. L’une des hypothèses clés de ce scénario est que la stratégie de l’organisation consiste à installer une image d’Windows d’entreprise avant que l’ordinateur soit remis à l’utilisateur. Si les paramètres de stratégie de groupe sont configurés pour exiger un code confidentiel, les utilisateurs sont invités à définir un code confidentiel après avoir reçu la stratégie.

Pour plus d’informations, [voir How to Deploy the MBAM Client as Part of a Windows Deployment](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-enable-bitlocker-by-using-mbam-as-part-of-a-windows-deploymentmbam-25).
 
#### <a name="how-to-deploy-the-mbam-client-by-using-a-command-line"></a>Comment déployer le client MBAM à l’aide d’une ligne de commande

Pour plus d’informations, [voir Comment déployer le client MBAM à l’aide d’une ligne de commande](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-deploy-the-mbam-client-by-using-a-command-line).

#### <a name="post-deployment-of-clients"></a>Post-déploiement des clients

Maintenant que vous avez terminé l’activité de déploiement, vous devez consulter les journaux suivants et déterminer si les clients sont correctement signalés à la base de données MBAM.

## <a name="faq"></a>Forum Aux Questions

### <a name="how-to-create-a-load-balanced-iis-servers"></a>Comment créer des serveurs IIS à charge équilibrée

* SPN doit être enregistré uniquement sous le nom convivial (par exemple : bitlocker.corp.net) et ne doit pas être inscrit sur des serveurs IIS individuels.

* Si un certificat est utilisé, le certificat doit avoir les noms de domaine complet et NetBIOS entrés dans le champ **Autre** nom de l’objet pour tous les serveurs IIS du groupe d’équilibrage de charge, ainsi que comme nom convivial (par exemple : bitlocker.corp.net). Dans le cas contraire, le certificat sera signalé comme non approuvé par le navigateur lorsque vous parcourez des adresses à charge équilibrée.

Pour plus d’informations, voir [IIS Network Load Balancing](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/planning-for-mbam-25-high-availability#a-href-idbkmk-load-balanceaiis-network-load-balancing) and [Registering SPNs for the application pool account](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/planning-how-to-secure-the-mbam-websites#registering-spns-for-the-application-pool-account).

### <a name="how-to-configure-a-certificate"></a>Comment configurer un certificat

* Vous devez avoir deux certificats. Un certificat est utilisé pour SQL serveur et l’autre pour IIS. Ils doivent être installés avant de commencer l’installation de MBAM.

* Nous vous recommandons d’utiliser le programme d’installation pour ajouter le certificat à la configuration IIS au lieu de modifier manuellement web.config fichier.

* Le certificat n’est pas accepté par le configurateur MBAM si le champ « Délivré à » du certificat ne correspond pas au nom du serveur. Dans ce cas, créez temporairement un certificat auto-signé à partir de la console IIS et utilisez-le dans le Configurateur. Cela permet de s’assurer que les applications web sont installées pour SSL et HTTPS. Après cela, vous pouvez changer le certificat en un certificat à partir des liaisons IIS pour le site web MBAM.

### <a name="the-sql-permissions-requirement-for-installation"></a>La SQL d’autorisations requises pour l’installation

Créez un compte pour le pool d’applications MBAM et accordez-lui uniquement les autorisations SecurityAdmin, Public et DBCreator.

Voir [configuration de la base de données MBAM : autorisations minimales](https://blogs.technet.microsoft.com/dubaisec/2016/02/02/mbam-database-configuration-minimum-permissions/) pour plus d’informations.

> [!Note]
> * Dans certains cas, davantage d’autorisations sont requises pour les opérations d’installation et de mise à niveau initiales.
> * Utilisez un compte qui dispose d’une sa temporaire pour l’installation.
> * Ne démarrez pas le configurateur dans le contexte d’un compte d’utilisateur (Exécuter en tant que) qui ne comprend pas suffisamment d’autorisations pour apporter des modifications à SQL Server car cela provoquera des erreurs d’installation.
> * Vous devez être connecté à l’aide d’un compte qui dispose d’autorisations sur SQL Server. Seules SQL Server bases de données peuvent être créées ou mises à jour en exécutant MBAM Configurator à distance. Pour le serveur SSRS, vous devez installer MBAM et exécuter Configurator localement pour installer ou mettre à jour les rapports SSRS MBAM.

### <a name="the-permission-required-for-spn-registration"></a>Autorisation requise pour l’inscription SPN

Un compte utilisé pour l’installation du portail IIS doit avoir les autorisations Write ServicePrincipalName et Write Validated SPN. Sans ces autorisations, l’installation retourne un message d’avertissement qui indique qu’elle ne peut pas inscrire le SPN.

> [!Note]
> Vous recevrez ce message d’avertissement deux fois. Cela ne signifie pas que le SPN doit avoir deux objets inscrits sur celui-ci.

Pour plus d’informations, voir [Échec du programme d’installation de MBAM avec](https://support.microsoft.com/help/2754138/)le message d’erreur « Enregistrer le SPN différé ».

### <a name="did-i-have-to-update-the-admx-templates-to-the-latest-version"></a>Ai-je dû mettre à jour les modèles ADMX vers la dernière version ?

Vous verrez plusieurs options de système d’exploitation dans le nœud racine MBAM pour GPO après avoir mis à jour les modèles ADMX vers leurs dernières versions. Par exemple, Windows 7, Windows8.1 et Windows 10 version 1511 et versions ultérieures.

Pour plus d’informations sur la mise à jour des modèles ADMX, consultez les articles suivants :
* [Téléchargement et déploiement des modèles de stratégie de groupe MDOP (.admx)](https://docs.microsoft.com/microsoft-desktop-optimization-pack/solutions/how-to-download-and-deploy-mdop-group-policy--admx--templates)
* [Planification des exigences en matière de stratégie de groupe MBAM 2.5](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/planning-for-mbam-25-group-policy-requirements)
* [Modèles d’administration de stratégie de groupe Microsoft Desktop Optimization Pack](https://www.microsoft.com/en-us/download/details.aspx?id=55531)
