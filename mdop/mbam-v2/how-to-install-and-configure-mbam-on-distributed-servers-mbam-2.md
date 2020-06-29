---
title: Installation et configuration de MBAM sur des serveurs distribués
description: Installation et configuration de MBAM sur des serveurs distribués
author: dansimp
ms.assetid: 67b91e6b-ae2e-4e47-9ef2-6819aba95976
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 841b894430d14604f0fd923703708d7a3f588c07
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810326"
---
# Installation et configuration de MBAM sur des serveurs distribués


Les procédures décrites dans cette rubrique décrivent l’installation de Microsoft BitLocker administration et de la surveillance (MBAM) 2,0 dans la topologie autonome sur des serveurs distribués. Pour afficher un diagramme de l’architecture recommandée, ainsi qu’une description des bases de données et des fonctionnalités, reportez-vous à la rubrique [déploiement de l’infrastructure du serveur MBAM 2,0](deploying-the-mbam-20-server-infrastructure-mbam-2.md). Pour installer et surveiller Microsoft BitLocker avec la topologie de Configuration Manager, consultez [déploiement d’MBAM avec Configuration Manager](deploying-mbam-with-configuration-manager-mbam2.md).

Chaque fonctionnalité de serveur comporte certaines conditions préalables. Pour vérifier que vous remplissez les conditions préalables et que vous avez besoin de la configuration matérielle et logicielle requise, voir Configuration requise pour le [déploiement d’MBAM 2,0](mbam-20-deployment-prerequisites-mbam-2.md) et [Configurations prises en charge par MBAM 2,0](mbam-20-supported-configurations-mbam-2.md). De plus, certaines fonctionnalités nécessitent que vous fournissez des informations lors du processus d’installation pour déployer la fonctionnalité correctement. Vous devez également consulter la [planification du déploiement de MBAM 2,0 Server avant de](planning-for-mbam-20-server-deployment-mbam-2.md) démarrer le déploiement d’MBAM.

**Remarque**  
Pour obtenir les fichiers journaux d’installation, vous devez utiliser le package msiexec et l’option **/l** &lt; emplacement &gt; pour installer MBAM. Les fichiers journaux sont créés à l’emplacement que vous spécifiez.

D’autres fichiers journaux d’installation sont créés dans le dossier% Temp% sur le serveur de l’utilisateur qui installe MBAM.



## <a href="" id="deploying-mbam-server-features-"></a>Déploiement de fonctionnalités du serveur MBAM


Les étapes suivantes expliquent comment installer les fonctionnalités MBAM générales.

**Pour démarrer l’Assistant Installation de MBAM Server**

1.  Sur le serveur sur lequel vous voulez installer l’administration et le contrôle Microsoft BitLocker, exécutez **MBAMSetup.exe** pour démarrer l’Assistant Installation d’MBAM.

2.  Dans la page d' **Accueil** , sélectionnez éventuellement le **programme d’amélioration**du produit, puis cliquez sur **Démarrer**.

3.  Lisez et acceptez le contrat de licence logiciel Microsoft, puis cliquez sur **suivant** pour continuer l’installation.

4.  Dans la page de sélection de la **topologie** , sélectionnez la topologie **autonome** , puis cliquez sur **suivant**.

    **Remarque**  
    Si vous souhaitez installer MBAM avec la topologie intégrée de Configuration Manager, consultez [déploiement de MBAM avec Configuration Manager](deploying-mbam-with-configuration-manager-mbam2.md).



5.  Sélectionnez les fonctionnalités que vous voulez installer. Par défaut, toutes les fonctionnalités de MBAM sont sélectionnées pour l’installation. Effacez les fonctionnalités que vous voulez installer ailleurs. Les fonctionnalités qui seront installées sur le même ordinateur doivent être installées en même temps. Vous devez installer les fonctionnalités d’MBAM dans l’ordre suivant:

    -   Base de données de récupération

    -   Base de données d’audit et de conformité

    -   Rapports de conformité et d’audit

    -   Portail libre-service

    -   Serveur d’administration et de surveillance

    -   Modèle de stratégie de groupe MBAM

    **Remarque**  
    L’Assistant installation vérifie la configuration requise pour votre installation et affiche les conditions préalables manquantes. Si toutes les conditions préalables sont remplies, l’installation continue. Si une condition préalable manquante est détectée, vous devez résoudre les conditions préalables manquantes, puis cliquer de **nouveau sur vérifier les conditions préalables**. Si toutes les conditions préalables sont remplies ce délai, l’installation reprend.



~~~
The MBAM Setup wizard displays installation pages for the features that you select. The following sections describe the installation procedures for each feature.

**Note**  
For the following instructions, it is assumed that each feature is to be installed on a separate server. If you install multiple features on a single server, you can change or eliminate some steps.
~~~



**Pour installer la base de données de récupération**

1.  Dans la page **configurer la base de données de récupération** , spécifiez les noms des ordinateurs qui exécutent la fonctionnalité d’administration et de surveillance du serveur. Après le déploiement de la fonctionnalité d’administration et de surveillance du serveur, il utilise son compte de domaine pour se connecter à la base de données.

2.  Cliquez sur **Suivant** pour poursuivre.

3.  Spécifiez le nom de l’instance SQL Server et le nom de la base de données qui stockera les données de récupération. Vous devez également spécifier l’emplacement de la base de données et l’emplacement où se trouvent les informations de journalisation.

4.  Cliquez sur **suivant** pour continuer à utiliser l’Assistant Configuration de MBAM.

**Pour installer la base de données de conformité et d’audit**

1.  Dans la page **configuration de la conformité et de la base de données d’audit** , spécifiez le compte d’utilisateur qui sera utilisé pour accéder à la base de données pour les rapports.

2.  Spécifiez le nom de l’ordinateur qui sera exécuté sur le serveur d’administration et de surveillance ainsi que les rapports de conformité et d’audit. Après le déploiement de l’administration et de la surveillance et des rapports de conformité et d’audit, ils utilisent leurs comptes de domaine pour se connecter aux bases de données.

    **Remarque**  
    Si vous installez la base de données de conformité et d’audit sans les rapports de conformité et d’audit, vous devez ajouter une exception sur l’ordinateur de base de données de conformité et d’audit pour activer le trafic entrant sur le port Microsoft SQL Server. Le numéro de port par défaut est 1433.



3.  Spécifiez le nom de l’instance SQL Server et le nom de la base de données qui stockera les données d’audit et de conformité. Vous devez également spécifier l’emplacement des informations de base de données et de journalisation.

4.  Cliquez sur **suivant** pour continuer à utiliser l’Assistant de configuration de l’administration et de la surveillance de BitLocker.

**Pour installer les rapports de conformité et d’audit**

1.  Sur la page **configurer les rapports de conformité et d’audit** , spécifiez le nom de l’instance SQL Server distante (par exemple, &lt; ServerName &gt; ) où la base de données d’audit et de conformité a été installée.

    **Remarque**  
    Si vous installez des rapports de conformité et d’audit sans le serveur d’administration et de surveillance, vous devez ajouter une exception sur l’ordinateur du rapport de conformité et d’audit pour activer le trafic entrant sur le port du serveur de rapports (le port par défaut est 80).



2.  Spécifiez le nom de la base de données d’audit et de conformité. Par défaut, il s’agit du nom de la base de données MBAM, même si vous pouvez en modifier le nom lors de l’installation de la base de données d’audit et de conformité.

3.  Cliquez sur **Suivant** pour poursuivre.

4.  Sélectionnez l’instance de SQL Server Reporting Services dans laquelle les rapports de conformité et d’audit seront installés. Fournissez un compte d’utilisateur et un mot de passe de domaine pour accéder à la base de données d’audit et de conformité. Configurez le mot de passe de ce compte pour qu’il n’expire jamais. Le compte d’utilisateur doit être en mesure d’accéder à toutes les données disponibles pour le groupe utilisateurs de reports MBAM.

5.  Cliquez sur **suivant** pour continuer à utiliser l’Assistant de configuration de l’administration et de la surveillance de BitLocker.

**Pour installer le portail libre-service**

1.  Sur la page **configurer le portail libre-service** , vous pouvez également chiffrer la communication entre le portail libre-service et les serveurs d’administration et de surveillance. Si vous choisissez l’option permettant de chiffrer la communication, vous êtes invité à sélectionner le certificat d’autorité de certification à utiliser pour le chiffrement.

2.  Cliquez sur **Suivant** pour poursuivre.

3.  Spécifiez l’instance distante de SQL Server (par exemple, * &lt; ServerName &gt; *) où la base de données d’audit et de conformité est installée.

4.  Spécifiez le nom de la base de données d’audit et de conformité. Par défaut, le nom de la base de données est MBAM de conformité. Toutefois, vous pouvez modifier le nom lors de l’installation de la base de données d’audit et de conformité.

5.  Cliquez sur **Suivant** pour poursuivre.

6.  Spécifiez l’instance distante de SQL Server (par exemple, * &lt; ServerName &gt; *) où la base de données de récupération a été installée.

7.  Spécifiez le nom de la base de données de récupération. Par défaut, il s’agit du nom de la base de données **MBAM**. Toutefois, vous pouvez modifier le nom lors de l’installation de la fonctionnalité de base de données de récupération.

8.  Cliquez sur **Suivant** pour poursuivre.

9.  Entrez le **numéro de port**, le **nom d’hôte** (facultatif), ainsi que le chemin d' **installation** du serveur d’administration et de surveillance de MBAM.

    **Remarque**  
    Le numéro de port que vous spécifiez doit être un numéro de port inutilisé sur le serveur d’administration et de surveillance sauf si vous spécifiez un nom d’en-tête d’hôte unique. Si vous utilisez le pare-feu Windows, le port s’ouvre automatiquement.



10. Pour éventuellement inscrire un nom de principal de service (SPN) pour le portail libre-service, sélectionnez **inscrire les noms de principal de service (SPN) de cet ordinateur auprès d’Active Directory (requis pour l’authentification Windows)**. Si vous activez cette case à cocher, le programme d’installation d’MBAM ne tente pas d’inscrire le SPN existant et vous pouvez inscrire manuellement le SPN avant ou après l’installation d’MBAM. Pour obtenir des instructions sur l’enregistrement manuel du SPN, voir [enregistrement de SPN manuel](https://go.microsoft.com/fwlink/?LinkId=286758).

11. Cliquez sur **suivant** pour continuer à utiliser l’Assistant de configuration de l’administration et de la surveillance de BitLocker.

12. Indiquez si vous souhaitez utiliser les mises à jour de Microsoft pour renforcer la sécurité de votre ordinateur, puis cliquez sur **suivant**.

13. Lorsque les informations de fonctionnalité de MBAM sélectionnées sont terminées, vous êtes prêt à démarrer l’installation d’MBAM à l’aide de l’Assistant de configuration. Cliquez sur **retour** pour parcourir l’Assistant si vous devez revoir ou modifier vos paramètres d’installation. Cliquez sur **installer** pour démarrer l’installation. Cliquez sur **Annuler** pour quitter l’Assistant. Le programme d’installation installe les fonctionnalités de MBAM que vous avez sélectionnées et vous signale que l’installation est terminée.

14. Cliquez sur **Terminer** pour quitter l’Assistant.

    **Remarque**  
    Pour configurer le portail libre-service une fois l’installation terminée, marquez le portail libre-service avec le nom de votre société et d’autres informations spécifiques à votre entreprise, voir [Comment personnaliser le portail libre-service](how-to-brand-the-self-service-portal.md) pour obtenir des instructions.



15. Si les ordinateurs clients ont accès au réseau de distribution de contenu (CDN) Microsoft, ce qui donne au portail libre-service l’accès requis à certains fichiers JavaScript, vous avez terminé l’installation du portail libre-service. Si les ordinateurs clients n’ont pas accès au réseau de distribution de contenu Microsoft, suivez les étapes décrites dans la section suivante pour configurer le portail libre-service pour référencer les fichiers JavaScript à partir d’une source accessible.

**Pour configurer le portail libre-service lorsque les utilisateurs finaux ne peuvent pas accéder au réseau de distribution de contenu Microsoft**

1. Si les ordinateurs clients ont accès au réseau de distribution de contenu (CDN) Microsoft, ce qui donne au portail libre-service l’accès requis à certains fichiers JavaScript, l’installation du portail libre-service est terminée. Si les ordinateurs client n’ont pas accès au réseau de distribution de contenu Microsoft, suivez les étapes restantes de cette section pour configurer le portail libre-service pour référencer les fichiers JavaScript à partir d’une source accessible.

2. Téléchargez les quatre fichiers JavaScript à partir du Microsoft CDN:

   -   jQuery-1.7.2.min.js-[https://go.microsoft.com/p/fwlink/?LinkID=271736](https://go.microsoft.com/fwlink/p/?LinkID=271736)

   -   MicrosoftAjax.js –[https://go.microsoft.com/p/fwlink/?LinkId=272283](https://go.microsoft.com/fwlink/p/?LinkId=272283)

   -   MicrosoftMvcAjax.js-[https://go.microsoft.com/p/fwlink/?LinkId=272284](https://go.microsoft.com/fwlink/p/?LinkId=272284)

   -   MicrosoftMvcValidation.js- <https://go.microsoft.com/fwlink/p/?LinkId=272285>

3. Copiez les fichiers JavaScript dans le répertoire **scripts** du portail libre-service. Ce répertoire se trouve dans <em> &lt; MBAM répertoire d’installation de self-service &gt; \\ </em> Website\\Scripts.

4. Ouvrez le **Gestionnaire des services Internet (IIS)**.

5. Développez **sites** &gt; **Microsoft et surveillance de BitLocker**et mettez en surbrillance **selfservice**.

   **Remarque**  
   *Selfservice* est le nom de répertoire virtuel par défaut. Si vous avez choisi un autre nom pour ce répertoire lors de l’installation, n’oubliez pas de remplacer *selfservice* dans le reste de ces instructions par le nom que vous avez choisi.



6. Dans le volet du milieu, double-cliquez sur paramètres de l' **application**.

7. Pour chaque élément de la liste suivante, modifiez les paramètres de l’application pour référencer le nouvel emplacement en remplaçant le &lt; répertoire virtuel &gt; par/selfservice/(ou le nom que vous avez choisi lors de l’installation). Par exemple, le chemin d’accès du répertoire virtuel est semblable à/selfservice/scripts/jquery-1.7.2.min.js.

   -   jQueryPath:/ &lt; répertoire virtuel &gt; /scripts/jQuery-1.7.2.min.js

   -   MicrosoftAjaxPath:/ &lt; répertoire virtuel &gt; /scripts/MicrosoftAjax.js

   -   MicrosoftMvcAjaxPath:/ &lt; répertoire virtuel &gt; /scripts/MicrosoftMvcAjax.js

   -   MicrosoftMvcValidationPath:/ &lt; répertoire virtuel &gt; /scripts/MicrosoftMvcValidation.js

**Pour installer la fonctionnalité serveur d’administration et de surveillance**

1. MBAM peut crypter la communication entre les services Web et les serveurs d’administration et de surveillance. Si vous choisissez l’option permettant de chiffrer la communication, vous êtes invité à sélectionner le certificat d’autorité de certification à utiliser pour le chiffrement.

2. Cliquez sur **Suivant** pour poursuivre.

3. Spécifiez l’instance distante de SQL Server (par exemple: * &lt; NomServeur &gt; *) où la base de données d’audit et de conformité est installée.

4. Spécifiez le nom de la base de données d’audit et de conformité. Par défaut, le nom de la base de données est MBAM de conformité. Toutefois, vous pouvez modifier le nom lors de l’installation de la base de données d’audit et de conformité.

5. Cliquez sur **Suivant** pour poursuivre.

6. Spécifiez l’instance distante de SQL Server (par exemple: * &lt; NomServeur &gt; *) où la base de données de récupération a été installée.

7. Spécifiez le nom de la base de données de récupération. Par défaut, il s’agit du nom de la base de données **MBAM**. Toutefois, vous pouvez modifier le nom lors de l’installation de la fonctionnalité de base de données de récupération.

8. Cliquez sur **Suivant** pour poursuivre.

9. Spécifiez l’URL du site «Home» (SRS) SQL Server Reporting Services (SRS). L’emplacement d’accueil par défaut d’une instance de site SQL Server Reporting Services est le suivant:

   http:// <em> &lt; NameofMBAMReportsServer &gt; / </em> reportserver

   **Remarque**  
   Si SQL Server Reporting Services a été configuré en tant qu’instance nommée, l’URL ressemble à ce qui suit: http://* &lt; NameofMBAMReportsServer &gt; */ReportServer\_* &lt; SRSInstanceName &gt; *.



10. Cliquez sur **Suivant** pour poursuivre.

11. Entrez le **numéro de port**, le **nom d’hôte** (facultatif), ainsi que le chemin d' **installation** du serveur d’administration et de surveillance de MBAM.

    **Remarque**  
    Le numéro de port que vous spécifiez doit être un numéro de port inutilisé sur le serveur d’administration et de surveillance sauf si vous spécifiez un nom d’en-tête d’hôte unique. Si vous utilisez le pare-feu Windows, le port s’ouvre automatiquement.



12. Pour éventuellement inscrire un nom de principal de service (SPN) pour le portail libre-service, sélectionnez **inscrire les noms de principal de service (SPN) de cet ordinateur auprès d’Active Directory (requis pour l’authentification Windows)**. Si vous activez cette case à cocher, le programme d’installation d’MBAM ne tente pas d’inscrire le SPN existant et vous pouvez inscrire manuellement le SPN avant ou après l’installation d’MBAM. Pour obtenir des instructions sur l’enregistrement manuel du SPN, voir [enregistrement de SPN manuel](https://go.microsoft.com/fwlink/?LinkId=286758).

13. Cliquez sur **suivant** pour continuer à utiliser l’Assistant de configuration de l’administration et de la surveillance de BitLocker.

14. Indiquez si vous souhaitez utiliser les mises à jour de Microsoft pour renforcer la sécurité de votre ordinateur, puis cliquez sur **suivant**.

15. Lorsque les informations de fonctionnalité de MBAM sélectionnées sont terminées, vous êtes prêt à démarrer l’installation d’MBAM à l’aide de l’Assistant de configuration. Cliquez sur **retour** pour parcourir l’Assistant si vous devez revoir ou modifier vos paramètres d’installation. Cliquez sur **installer pour procéder** à l’installation. Cliquez sur **Annuler** pour quitter l’Assistant. Le programme d’installation installe les fonctionnalités de MBAM que vous avez sélectionnées et vous signale que l’installation est terminée.

16. Cliquez sur **Terminer** pour quitter l’Assistant.

**Pour effectuer une configuration après l’installation**

1.  Sur le serveur d’administration et de surveillance, ajoutez des utilisateurs aux groupes locaux suivants pour leur permettre d’accéder aux fonctionnalités disponibles sur le site Web d’administration et de surveillance de MBAM.

    -   **Utilisateurs du support technique MBAM**: les membres de ce groupe local peuvent accéder à la récupération du lecteur et gérer les fonctionnalités du TPM sur le site Web d’administration et de surveillance MBAM. Pour un utilisateur du support technique, tous les champs de la récupération de lecteur et de la gestion de TPM sont obligatoires.

    -   **Utilisateurs de l’assistance technique avancée MBAM**: les membres de ce groupe local disposent d’un accès avancé aux fonctionnalités de récupération et de gestion du TPM sur le site Web d’administration et de surveillance des MBAM. Pour les utilisateurs expérimentés du support technique, seul le champ ID clé est requis pour la récupération du lecteur. Dans **gérer le module de plateforme sécurisée**, seul le champ domaine de l' **ordinateur** et le champ nom de l' **ordinateur** est requis.

2.  Sur le serveur hébergeant l’administration et la surveillance du serveur et la base de données de conformité et d’audit, et sur le serveur qui héberge les rapports de conformité et d’audit, ajoutez des utilisateurs au groupe local suivant pour leur permettre d’accéder à la fonctionnalité rapports sur le site Web d’administration et de surveillance de MBAM.

    -   **Utilisateurs du rapport MBAM**: les membres de ce groupe local peuvent accéder aux rapports sur le site Web d’administration et de surveillance de MBAM.

    **Remarque**  
    Il est possible d’avoir une appartenance similaire à un utilisateur ou un groupe du groupe local **utilisateurs de rapports MBAM** sur tous les ordinateurs sur lesquels les fonctionnalités d’administration de MBAM et de surveillance de la base de données de serveur et de conformité, ainsi que les rapports de conformité et d’audit sont installés.



## Validation de l’installation de la fonctionnalité MBAM Server


Lorsque l’installation de la fonctionnalité administration de Microsoft BitLocker et analyse du serveur est terminée, nous vous conseillons de vérifier que l’installation a correctement configuré toutes les fonctionnalités nécessaires à MBAM. Utilisez la procédure suivante pour vérifier que le service d’administration et de surveillance de BitLocker est opérationnel.

**Pour valider une installation de MBAM Server**

1. Sur chaque serveur sur lequel est déployée une fonctionnalité MBAM, ouvrez **le panneau de configuration**, sélectionnez **programmes**, puis sélectionnez **programmes et fonctionnalités**. Vérifiez que la fonctionnalité **administration et analyse de BitLocker Microsoft** s’affiche dans la liste **programmes et fonctionnalités** .

   **Remarque**  
   Pour valider l’installation d’MBAM, vous devez utiliser un compte de domaine disposant d’informations d’identification d’administrateur local sur chaque serveur.



2. Sur le serveur sur lequel la base de données de récupération est installée, ouvrez SQL Server Management Studio, puis vérifiez que la base de données de **récupération et de MBAM** est installée.

3. Sur le serveur sur lequel la base de données d’audit et de conformité est installée, ouvrez SQL Server Management Studio et vérifiez que la **base de données de statut de conformité MBAM** est installée.

4. Sur le serveur sur lequel sont installés les rapports de conformité et d’audit, ouvrez un navigateur Web contenant les informations d’identification d’administration et naviguez jusqu’au site «Home» du site SQL Server Reporting Services.

   L’emplacement local par défaut d’une instance de site SQL Server Reporting Services est disponible sur http:// <em> &lt; NameofMBAMReportsServer &gt; </em> /reports.aspx. Pour trouver l’URL réelle, utilisez l’outil Gestionnaire de configuration de Reporting Services et sélectionnez les instances spécifiées lors de l’installation.

   Confirmez qu’un dossier de rapports intitulé **Microsoft BitLocker administration et analyse** contient une source de données appelée **MaltaDataSource** et qu’un dossier **en-US** contient quatre rapports.

   **Remarque**  
   Si SQL Server Reporting Services a été configuré en tant qu’instance nommée, l’URL doit ressembler à ce qui suit: http://* &lt; NameofMBAMReportsServer &gt; */Reports\_* &lt; SRSInstanceName &gt; *



~~~
**Note**  
If SSRS was not configured to use Secure Socket Layer (SSL), the URL for the reports will be set to HTTP instead of HTTPS when you install the MBAM Server. If you then go to the Administration and Monitoring website and select a report, the following message appears: “Only Secure Content is Displayed.” To show the report, click **Show All Content**.
~~~



5. Sur le serveur sur lequel est installée la fonctionnalité d’administration et de surveillance, exécutez le **Gestionnaire de serveur** et naviguez jusqu’à **rôles**. Sélectionnez **serveur Web (IIS)**, puis cliquez sur **Gestionnaire des services Internet (IIS)**.

6. Dans **connexions**, naviguez jusqu’à * &lt; nomordinateur &gt; *, sélectionnez **sites**, puis l’option **administration et analyse de Microsoft BitLocker**. Vérifiez que **MBAMAdministrationService**, **MBAMComplianceStatusService**et **MBAMRecoveryAndHardwareService** apparaissent.

7. Sur le serveur sur lequel sont installés les fonctionnalités d’administration et de surveillance et de portail en libre-service, ouvrez un navigateur Web contenant les informations d’identification d’administration et naviguez jusqu’aux emplacements suivants pour vérifier qu’ils se chargent correctement.

   **Remarque**  
   Les URL se terminant par «. svc» n’affichent pas de site Web. Le succès est indiqué par le message «la publication des métadonnées pour ce service est actuellement désactivée» ou par des informations ressemblant à du code. Si un autre message d’erreur s’affiche ou si la page n’est pas disponible, cela dit qu’il n’a pas été correctement chargé.



~~~
-   *http://&lt;hostname&gt;/HelpDesk/default.aspx* and confirm each of the links for navigation and reports

-   *http://&lt;hostname&gt;/SelfService&gt;/*

-   *http://&lt;computername&gt;/MBAMAdministrationService/AdministrationService.svc*

-   *http://&lt;hostname&gt;/MBAMUserSupportService/UserSupportService.svc*

-   *http://&lt;computername&gt;/MBAMComplianceStatusService/StatusReportingService.svc*

-   *http://&lt;computername&gt;/MBAMRecoveryAndHardwareService/CoreService.svc*

**Note**  
It is assumed that the server features were installed on the default port without network encryption. If you installed the server features on a different port or virtual directory, change the URLs to include the appropriate port, for example, *http://&lt;hostname&gt;:&lt;port&gt;/HelpDesk/default.aspx* or*http://&lt;hostname&gt;:&lt;port&gt;/&lt;virtualdirectory&gt;/default.aspx*

If the server features were installed with network encryption, change http:// to https://.
~~~



8. Vérifiez que chaque page Web se charge correctement.

## Rubriques connexes


[Déploiement de l'infrastructure de serveur MBAM2.0](deploying-the-mbam-20-server-infrastructure-mbam-2.md)









