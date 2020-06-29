---
title: Installation et configuration de MBAM sur des serveurs distribués
description: Installation et configuration de MBAM sur des serveurs distribués
author: dansimp
ms.assetid: 9ee766aa-6339-422a-8d00-4f58e4646a5e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 51f56a12d4e59226f834c7e474af0f1e96c1e8e9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811286"
---
# Installation et configuration de MBAM sur des serveurs distribués


Les procédures décrites dans cette rubrique décrivent l’installation complète des fonctionnalités d’administration et de surveillance de Microsoft BitLocker (MBAM) sur les serveurs distribués.

Chaque fonctionnalité de serveur comporte certaines conditions préalables. Pour vérifier que vous remplissez les conditions préalables et que vous avez besoin de la configuration matérielle et logicielle requise, voir Configuration requise pour le [déploiement d’MBAM 1,0](mbam-10-deployment-prerequisites.md) et [Configurations prises en charge par MBAM 1,0](mbam-10-supported-configurations.md). De plus, certaines fonctionnalités nécessitent que vous fournissez des informations lors du processus d’installation pour déployer la fonctionnalité correctement.

**Remarque**  
Pour obtenir les fichiers journaux d’installation, vous devez installer MBAM à l’aide du package **msiexec** et de l’option **/l &lt; emplacement &gt; ** . Les fichiers journaux sont créés à l’emplacement que vous spécifiez.

D’autres fichiers journaux d’installation sont créés dans le dossier% Temp% de l’utilisateur qui exécute l’installation MBAM.



## <a href="" id="deploy-the-mbam-server-features-"></a>Déployer les fonctionnalités du serveur MBAM


Les étapes suivantes expliquent comment installer les fonctionnalités MBAM générales.

**Remarque**  
Vérifiez que vous utilisez la configuration de 32 bits sur les serveurs 32 bits et la configuration 64 bits sur les serveurs 64.



**Pour déployer les fonctionnalités du serveur MBAM**

1.  Démarrez l’Assistant Installation de MBAM, puis cliquez sur **installer** sur la page d’accueil.

2.  Lisez et acceptez les termes du contrat de licence logiciel Microsoft, puis cliquez sur **suivant** pour continuer l’installation.

3.  Par défaut, toutes les fonctionnalités de MBAM sont sélectionnées pour l’installation. Effacez les fonctionnalités que vous voulez installer ailleurs. Les fonctionnalités que vous voulez installer sur le même ordinateur doivent être installées en même temps. Les fonctionnalités de MBAM doivent être installées dans l’ordre suivant:

    -   Base de données de récupération et de matériel

    -   Base de données d’audit et de conformité

    -   Rapports et audit de conformité

    -   Serveur d’administration et de surveillance

    -   Modèle de stratégie de groupe MBAM

    **Remarque**  
    L’Assistant installation vérifie la configuration requise pour votre installation et affiche les conditions préalables manquantes. Si toutes les conditions préalables sont remplies, l’installation continue. Si une condition préalable manquante est détectée, vous devez résoudre les conditions préalables manquantes, puis cliquer de **nouveau sur vérifier les conditions préalables**. Si toutes les conditions préalables sont remplies cette fois, l’installation sera reprise.



4.  L’Assistant de configuration de MBAM affiche les pages d’installation correspondant aux composants sélectionnés. Les sections suivantes décrivent les procédures d’installation pour chaque fonctionnalité.

    **Remarque**  
    En règle générale, chaque fonctionnalité est installée sur un serveur distinct. Si vous voulez installer plusieurs fonctionnalités sur un seul serveur, vous pouvez modifier ou supprimer les étapes suivantes.



~~~
**To install the Recovery and Hardware Database**

1.  Choose an option for MBAM communication encryption. MBAM can encrypt the communication between the Recovery and Hardware Database and the Administration and Monitoring servers. If you choose the option to encrypt communication, you are asked to select the authority-provisioned certificate that is used for encryption.

2.  Click **Next** to continue.

3.  Specify the names of the computers that will be running the Administration and Monitoring Server feature, to configure access to the Recovery and Hardware Database.. Once the Administration and Monitoring Server feature is deployed, it connects to the database by using its domain account.

4.  Click **Next** to continue.

5.  Specify the **Database Configuration** for the SQL Server instance that stores the recovery and hardware data. You must also specify where the database will be located and where the log information will be located.

6.  Click **Next** to continue with the MBAM Setup wizard.

**To install the Compliance and Audit Database**

1.  Choose an option for the MBAM communication encryption. MBAM can encrypt the communication between the Compliance and Audit Database and the Administration and Monitoring servers. If you choose the option to encrypt communication, you are asked to select the authority-provisioned certificate that will be used for encryption.

2.  Click **Next** to continue.

3.  Specify the user account that will be used to access the database for reports.

4.  Click **Next** to continue.

5.  Specify the computer names of the computers that you want to run the Administration and Monitoring Server and the Compliance and Audit Reports, to configure the access to the Compliance and Audit Database.. After the Administration and Monitoring and the Compliance and Audit Reports Server are deployed, they will connect to the databases by using their domain accounts.

6.  Specify the **Database Configuration** for the SQL Server instance that will store the compliance and audit data. You must also specify where the database will be located and where the log information will be located.

7.  Click **Next** to continue with the MBAM Setup wizard.

**To install the Compliance and Audit Reports**

1.  Specify the remote SQL Server instance. For example, *&lt;ServerName&gt;*,where the Compliance and Audit Database are installed.

2.  Specify the name of the Compliance and Audit Database. By default, the database name is “MBAM Compliance Status”, but you can change the name when you install the Compliance and Audit Database.

3.  Click **Next** to continue.

4.  Select the SQL Server Reporting Services instance where the Compliance and Audit Reports will be installed. Provide the username and password used to access the compliance database.

5.  Click **Next** to continue with the MBAM Setup wizard.

**To install the Administration and Monitoring Server feature**

1.  Choose an option for the MBAM communication encryption. MBAM can encrypt the communication between the Recovery and Hardware Database and the Administration and Monitoring servers. If you choose the option to encrypt communication, you are asked to select the authority-provisioned certificate that is used for encryption.

2.  Click **Next** to continue.

3.  Specify the remote SQL Server instance, For example, *&lt;ServerName&gt;*, where the Compliance and Audit Database are installed.

4.  Specify the name of the Compliance and Audit Database. By default, the database name is MBAM Compliance Status, but, you can change the name when you install the Compliance and Audit Database.

5.  Click **Next** to continue.

6.  Specify the remote SQL Server instance. For example, *&lt;ServerName&gt;*,where the Recovery and Hardware Database are installed.

7.  Specify the name of the Recovery and Hardware Database. By default, the database name is **MBAM Recovery and Hardware**, but you can change the name when you install the Recovery and Hardware Database feature.

8.  Click **Next** to continue.

9.  Specify the URL for the “Home” of the SQL Server Reporting Services (SRS) site. The default Home location of a SQL Server Reporting Services site instance is at:

    http://*&lt;NameofMBAMReportsServer&gt;/*ReportServer

    **Note**  
    If you configured the SQL Server Reporting Services as a named instance, the URL resembles the following:http://*&lt;NameofMBAMReportsServer&gt;*/ReportServer\_*&lt;SRSInstanceName&gt;*



10. Click **Next** to continue.

11. Enter the **Port Number**, the **Host Name** (optional), and the **Installation Path** for the MBAM Administration and Monitoring server

    **Warning**  
    The port number that you specify must be an unused port number on the Administration and Monitoring server, unless you specify a unique host header name.



12. Click **Next** to continue with the MBAM Setup wizard.
~~~

5. 

   Indiquez si vous souhaitez utiliser les mises à jour de Microsoft pour renforcer la sécurité de votre ordinateur, puis cliquez sur **suivant**.

6. Lorsque les informations de fonctionnalité de MBAM sélectionnées sont terminées, vous êtes prêt à démarrer l’installation d’MBAM à l’aide de l’Assistant de configuration. Cliquez sur **retour** pour parcourir l’Assistant si vous devez revoir ou modifier vos paramètres d’installation. Cliquez sur **installer** pour lancer l’installation. Cliquez sur **Annuler** pour quitter l’Assistant. Le programme d’installation installe les fonctionnalités de MBAM que vous avez sélectionnées et vous signale que l’installation est terminée.

7. Cliquez sur **Terminer** pour quitter l’Assistant.

8. Ajoutez des utilisateurs aux rôles MBAM appropriés, après l’installation des fonctionnalités de MBAM Server. Pour plus d’informations, reportez-vous [à planification des rôles d’administrateur MBAM 1,0](planning-for-mbam-10-administrator-roles.md).

**Configuration après l’installation**

1.  Après l’installation d’MBAM, vous devez ajouter des rôles d’utilisateur pour permettre aux utilisateurs d’accéder aux fonctionnalités dans le site Web d’administration MBAM. Sur le serveur d’administration et de surveillance, ajoutez des utilisateurs aux groupes locaux suivants.

    -   **Utilisateurs matériels MBAM**: les membres de ce groupe local peuvent accéder à la fonctionnalité matérielle dans le site Web d’administration MBAM.

    -   **Utilisateurs du support technique MBAM**: les membres de ce groupe local peuvent accéder aux fonctionnalités de récupération de lecteur et de gestion des modules de plateforme sécurisée (TPM) sur le site Web d’administration MBAM. Pour un utilisateur du support technique, tous les champs de la récupération de lecteur et de la gestion de TPM sont obligatoires.

    -   **Utilisateurs expérimentés du support technique MBAM**: les membres de ce groupe local disposent d’un accès avancé aux fonctionnalités de récupération de lecteur et de gestion des composants de plateforme dans le site Web d’administration MBAM. Pour les utilisateurs expérimentés du support technique, seul le champ ID clé est requis pour la récupération du lecteur. Dans gérer le module de plateforme sécurisée, seul le champ domaine de l’ordinateur et le champ nom de l’ordinateur est requis.

2.  Sur la base de données d’administration et de surveillance du serveur, de la conformité et de l’audit, et sur le serveur qui héberge les rapports de conformité et d’audit, ajoutez des utilisateurs au groupe local suivant pour leur permettre d’accéder à la fonctionnalité rapports dans le site Web d’administration MBAM.

    -   **Utilisateurs du rapport MBAM**: les membres de ce groupe local peuvent accéder aux rapports figurant sur le site Web d’administration MBAM.

    **Remarque**  
    Il est possible d’avoir une appartenance similaire à un utilisateur ou un groupe du groupe local **utilisateurs de rapports MBAM** sur tous les ordinateurs sur lesquels les fonctionnalités d’administration de MBAM et de surveillance de la base de données de serveur et de conformité, ainsi que les rapports de conformité et d’audit sont installés.



## Valider l’installation de la fonctionnalité MBAM Server


Lorsque l’installation de la fonctionnalité de serveur MBAM est terminée, vous devez vérifier que l’installation a correctement configuré toutes les fonctionnalités nécessaires à MBAM. Utilisez la procédure suivante pour vérifier que le service MBAM est fonctionnel.

**Pour valider une installation MBAM**

1. Sur chaque serveur sur lequel une fonctionnalité de MBAM est déployée, ouvrez **le panneau de configuration**, cliquez sur **programmes**, puis cliquez sur **programmes et fonctionnalités**. Vérifiez que la fonctionnalité **administration et analyse de BitLocker Microsoft** s’affiche dans la liste **programmes et fonctionnalités** .

   **Remarque**  
   Pour valider l’installation d’MBAM, vous devez utiliser un compte de domaine disposant d’informations d’identification d’administrateur local sur chaque serveur.



2. Sur le serveur sur lequel la base de données de récupération et de matériel est installée, ouvrez SQL Server Management Studio, puis vérifiez que la base de données **MBAM et de récupération** de la base de données est installée.

3. Sur le serveur sur lequel la base de données d’audit et de conformité est installée, ouvrez SQL Server Management Studio et vérifiez que la base de données de **statut de conformité MBAM** est installée.

4. Sur le serveur sur lequel sont installés les rapports de conformité et d’audit, ouvrez un navigateur Web doté de privilèges d’administration et naviguez jusqu’au site «Home» du site SQL Server Reporting Services.

   L’emplacement d’accueil par défaut d’une instance de site SQL Server Reporting Services est disponible sur http:// <em> &lt; NameofMBAMReportsServer &gt; </em> /reports.aspx. Pour trouver l’URL réelle, utilisez l’outil Gestionnaire de configuration Reporting Services et sélectionnez les instances spécifiées lors de l’installation.

   Vérifiez qu’un dossier nommé **rapports de conformité Malte** figure et qu’il contient cinq rapports et une seule source de données.

   **Remarque**  
   Si SQL Server Reporting Services a été configuré en tant qu’instance nommée, l’URL doit ressembler à ce qui suit: http://* &lt; NameofMBAMReportsServer &gt; */Reports\_* &lt; SRSInstanceName &gt; *



5. Sur le serveur sur lequel est installé la fonctionnalité d’administration et de surveillance, exécutez le **Gestionnaire de serveur** et recherchez les **rôles**, sélectionnez **serveur Web (IIS)**, puis cliquez sur **Gestionnaire des services Internet (IIS)**. Dans **connexions** , naviguez jusqu’à * &lt; nomordinateur &gt; *, cliquez sur **sites**, puis sur **analyse et administration de Microsoft BitLocker**. Vérifiez que **MBAMAdministrationService**, **MBAMComplianceStatusService**et **MBAMRecoveryAndHardwareService** apparaissent.

6. Sur le serveur sur lequel est installé la fonctionnalité d’administration et de contrôle, ouvrez un navigateur Web avec des privilèges d’administration et recherchez les emplacements suivants dans le site Web MBAM pour vérifier qu’ils se chargent correctement:

   -   *http:// &lt; nomordinateur &gt; /default.aspx* et confirmez chacun des liens pour la navigation et les rapports

   -   *http:// &lt; nomordinateur &gt; /MBAMAdministrationService/AdministrationService.svc*

   -   *http:// &lt; nomordinateur &gt; /MBAMComplianceStatusService/StatusReportingService.svc*

   -   *http:// &lt; nomordinateur &gt; /MBAMRecoveryAndHardwareService/CoreService.svc*

   **Remarque**  
   En général, les services sont installés sur le port 80 par défaut sans chiffrement réseau. Si les services sont installés sur un autre port, modifiez les URL pour inclure le port approprié. Par exemple, http://* &lt; nomordinateur &gt; : &lt; port &gt; */default.aspx ou http:// <em> &lt; hostheadername &gt; / </em> default. aspx

   Si les services ont été installés en utilisant le chiffrement réseau, modifiez http://sur https://.



~~~
Verify that each web page loads successfully.
~~~

## Rubriques connexes


[Déploiement de l'infrastructure de serveur MBAM1.0](deploying-the-mbam-10-server-infrastructure.md)









