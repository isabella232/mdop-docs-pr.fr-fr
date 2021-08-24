---
title: Installation et configuration de MBAM sur un seul serveur
description: Installation et configuration de MBAM sur un seul serveur
author: dansimp
ms.assetid: 45e6a012-6c8c-4d90-902c-d09de9a0cbea
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4dffe2e2dcb82866b86a3ac281aca8a0dcaab686
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910659"
---
# <a name="how-to-install-and-configure-mbam-on-a-single-server"></a>Installation et configuration de MBAM sur un seul serveur


Les procédures de cette rubrique décrivent comment installer Microsoft BitLocker Administration and Monitoring (MBAM) dans la topologie autonome sur un seul serveur. Utilisez la configuration à serveur unique uniquement dans un environnement de test. Pour les environnements de production, utilisez au moins deux serveurs. Si vous installez Microsoft BitLocker Administration and Monitoring à l’aide de la topologie Configuration Manager, voir [Deploying MBAM with Configuration Manager](deploying-mbam-with-configuration-manager-mbam2.md).

Le diagramme suivant illustre un exemple d’architecture à serveur unique. Pour obtenir une description des bases de données et des fonctionnalités, voir Architecture de haut niveau [pour MBAM 2.0.](high-level-architecture-for-mbam-20-mbam-2.md)

![Topologie de déploiement à serveur unique mbam 2.](images/mbam2-1-server.gif)

Chaque fonctionnalité de serveur a certaines conditions préalables. Pour vérifier que vous avez satisfait aux conditions préalables et à la configuration matérielle et logicielle requise, voir [MBAM 2.0 Deployment Prerequisites](mbam-20-deployment-prerequisites-mbam-2.md) et [MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md). En outre, certaines fonctionnalités ont également des informations qui doivent être fournies pendant le processus d’installation pour déployer correctement la fonctionnalité. Vous devez également passer en revue préparation de votre environnement [pour MBAM 2.0](preparing-your-environment-for-mbam-20-mbam-2.md) avant de commencer le déploiement de MBAM.

**Remarque**  
Pour obtenir les fichiers journaux d’installation, vous avez utilisé le package Msiexec et l’option **d’emplacement /L** &lt; pour installer &gt; MBAM. Les fichiers journaux sont créés à l’emplacement que vous spécifiez.

Des fichiers journaux d’installation supplémentaires sont créés dans le dossier %temp% sur le serveur de l’utilisateur qui installe MBAM.



## <a name="to-install-mbam-server-features-on-a-single-server"></a>Pour installer les fonctionnalités MBAM Server sur un serveur unique


Les étapes suivantes décrivent comment installer des fonctionnalités MBAM générales.

**Pour démarrer l’installation des fonctionnalités de MBAM Server**

1.  Sur le serveur sur lequel vous souhaitez installer MBAM, exécutez **MBAMSetup.exe** pour démarrer l’Assistant Installation de MBAM.

2.  Dans la page **d’accueil,** sélectionnez éventuellement **le**Programme d’amélioration du service, puis cliquez sur **Démarrer.**

3.  Lisez et acceptez le contrat de licence logiciel Microsoft, puis cliquez sur **Suivant** pour poursuivre l’installation.

4.  Dans la page **Sélection de la** topologie, sélectionnez la **topologie** autonome, puis cliquez sur **Suivant**.

5.  Dans la page **Sélectionner les fonctionnalités à installer,** sélectionnez les fonctionnalités que vous souhaitez installer. Par défaut, toutes les fonctionnalités MBAM sont sélectionnées pour l’installation. Les fonctionnalités qui doivent être installées sur le même ordinateur doivent être installées ensemble en même temps. Cochez les cases des fonctionnalités que vous souhaitez installer ailleurs. Vous devez installer les fonctionnalités MBAM dans l’ordre suivant :

    -   Base de données de récupération

    -   Base de données de conformité et d’audit

    -   Rapports de conformité et d’audit

    -   Self-Service Server

    -   Serveur d’administration et de surveillance

    -   Modèle de stratégie de groupe MBAM

    **Remarque**  
    L’Assistant Installation vérifie les conditions préalables pour votre installation et affiche les conditions préalables manquantes. Si toutes les conditions préalables sont remplies, l’installation se poursuit. Si un prérequis manquant est détecté, vous devez résoudre les conditions préalables manquantes, puis cliquer à nouveau sur Vérifier **les conditions préalables.** Si toutes les conditions préalables sont remplies cette fois, l’installation reprend.



6.  Dans la page Configurer la sécurité **des communications** réseau, choisissez s’il faut chiffrer la communication entre les services Web sur le serveur d’administration et de surveillance et les clients. Si vous décidez de chiffrer la communication, sélectionnez le certificat de l’autorité de certification à utiliser pour le chiffrement. Le certificat doit être créé avant cette étape pour vous permettre de le sélectionner sur cette page.

    **Remarque**  
    Cette page s’affiche uniquement si vous avez sélectionné le portail Self-Service ou la fonctionnalité Administration et serveur de surveillance sur la page Sélectionner les fonctionnalités **à installer.**



7.  Cliquez **sur**Suivant, puis poursuivez la procédure suivante pour configurer les fonctionnalités de MBAM Server.

**Pour configurer les fonctionnalités de MBAM Server**

1.  Dans la page **Configurer la base** de données de récupération, spécifiez le nom SQL Server’instance de récupération et le nom de la base de données qui stockera les données de récupération. Vous devez également spécifier l’emplacement des fichiers de base de données et les informations du journal.

2.  Cliquez sur **Suivant** pour poursuivre.

3.  Dans la page Configurer la base de données de conformité et **d’audit,** spécifiez le nom de l’instance SQL Server et le nom de la base de données qui stockera les données de conformité et d’audit. Vous devez également spécifier l’emplacement des fichiers de base de données et les informations du journal.

4.  Cliquez sur **Suivant** pour poursuivre.

5.  Dans la page Configurer les rapports de conformité et **d’audit,** spécifiez l’instance SQL Server Reporting Services dans laquelle les rapports de conformité et d’audit seront installés et fournissez un compte d’utilisateur de domaine et un mot de passe pour accéder à la base de données de conformité et d’audit. Configurez le mot de passe pour que ce compte n’expire jamais. Le compte d’utilisateur doit pouvoir accéder à toutes les données disponibles pour le groupe Utilisateurs de rapports MBAM.

6.  Cliquez sur **Suivant** pour poursuivre.

7.  Dans la page Configurer le portail **Self-Service,** entrez le numéro de port, le nom d’hôte, le nom du répertoire virtuel et le chemin d’installation du portail Self-Service.

    **Remarque**  
    Le numéro de port que vous spécifiez doit être un numéro de port inutilisé sur le serveur d’administration et de surveillance, sauf si vous spécifiez un nom d’en-tête d’hôte unique. Si vous utilisez Windows pare-feu, le port sera ouvert automatiquement.



8.  Cliquez sur **Suivant** pour poursuivre.

9.  Spécifiez s’il faut utiliser les mises à jour Microsoft pour sécuriser votre ordinateur, puis cliquez sur **Suivant**. Cela n’a pas pour fonction d’activer les mises à jour automatiques Windows.

10. Dans la page **Configurer l’administration** et le serveur de surveillance, entrez le numéro de port, le nom d’hôte, le nom du répertoire virtuel et le chemin d’installation du site web Help Desk.

    **Remarque**  
    Le numéro de port que vous spécifiez doit être un numéro de port inutilisé sur le serveur d’administration et de surveillance, sauf si vous spécifiez un nom d’en-tête d’hôte unique. Si vous utilisez Windows pare-feu, le port sera ouvert automatiquement.



11. Dans la page Résumé **de** l’installation, consultez la liste des fonctionnalités qui seront installées, puis cliquez sur **Installer** pour commencer à installer les fonctionnalités MBAM. Cliquez **sur Retour** pour revenir à l’Assistant si vous devez passer en revue ou modifier vos paramètres d’installation, ou cliquez sur **Annuler** pour quitter le programme d’installation. Le programme d’installation installe les fonctionnalités MBAM et vous informe que l’installation est terminée.

12. Cliquez **sur Terminer** pour quitter l’Assistant. Une fois les fonctionnalités Microsoft BitLocker Administration and Monitoring Server installées, continuez à la section suivante et terminez les étapes pour ajouter des utilisateurs aux rôles d’administration et de surveillance de Microsoft BitLocker. Pour plus d’informations sur les rôles, voir [Planning for MBAM 2.0 Administrator Roles](planning-for-mbam-20-administrator-roles-mbam-2.md).

**Pour effectuer la configuration post-installation**

1.  Sur le serveur d’administration et de surveillance, ajoutez des utilisateurs aux groupes locaux suivants pour leur donner accès aux fonctionnalités du site web du service d’aide mbam :

    -   **Utilisateurs du helpdesk MBAM**: les membres de ce groupe local peuvent accéder aux fonctionnalités Drive Recovery et Manage TPM sur le site Web Administration et surveillance de MBAM. Tous les champs de récupération de lecteur et de gestion du TPM sont des champs obligatoires pour un utilisateur du helpdesk.

    -   Utilisateurs du **helpdesk**avancé MBAM : les membres de ce groupe local disposent d’un accès avancé aux fonctionnalités de récupération de disque et de gestion du TPM sur le site web Administration et surveillance de MBAM. Pour les utilisateurs du helpdesk avancé, seul le champ **ID de** clé est requis dans la récupération de lecteur. Dans Gérer le TPM, seuls le champ **Domaine** de l’ordinateur et le champ **Nom de** l’ordinateur sont requis.

2.  Sur le serveur d’administration et de surveillance, ajoutez des utilisateurs au groupe local suivant pour leur permettre d’accéder à la fonctionnalité Rapports sur le site Web Administration et surveillance de MBAM :

    -   **Utilisateurs de rapports MBAM**: les membres de ce groupe local peuvent accéder aux fonctionnalités de rapports sur le site web Administration et surveillance de MBAM.

    -   Brand the Self-Service Portal with your company name, notice text, and other company-specific information. Pour obtenir des instructions, [voir Comment Brand the Self-Service Portal](how-to-brand-the-self-service-portal.md).

    **Remarque**  
    L’appartenance identique d’un utilisateur ou d’un groupe au groupe local Utilisateurs du rapport **MBAM** doit être conservée sur tous les ordinateurs sur lequel les fonctionnalités du serveur d’administration et de surveillance MBAM, la base de données de conformité et d’audit, ainsi que les rapports de conformité et d’audit sont installés. Pour ce faire, il est recommandé de créer un groupe de sécurité de domaine et d’ajouter ce groupe de domaines à chaque groupe d’utilisateurs de rapports MBAM local. Lorsque vous utilisez ce processus, gérez les appartenances aux groupes par le moyen du groupe de domaine.



## <a name="validating-the-mbam-server-feature-installation"></a>Validation de l’installation de la fonctionnalité MBAM Server


Une fois l’installation de Microsoft BitLocker Administration and Monitoring terminée, validez que l’installation a correctement installé toutes les fonctionnalités MBAM nécessaires à la gestion de BitLocker. Utilisez la procédure suivante pour vérifier que le service MBAM est fonctionnel.

**Pour valider l’installation de la fonctionnalité MBAM Server**

1. Sur chaque serveur où une fonctionnalité MBAM est déployée, ouvrez **le Panneau de contrôle.** Sélectionnez **Programmes,** puis Programmes **et fonctionnalités.** Vérifiez que **Microsoft BitLocker Administration and Monitoring** apparaît dans la liste Programmes et **fonctionnalités.**

   **Remarque**  
   Pour valider l’installation, vous devez utiliser un compte de domaine qui dispose d’informations d’identification d’administration d’ordinateur local sur chaque serveur.



2. Sur le serveur sur lequel la base de données de récupération est installée, ouvrez SQL Server Management Studio et vérifiez que la base de données de récupération **mbam** et matérielle est installée.

3. Sur le serveur sur lequel la base de données de conformité et d’audit est installée, ouvrez SQL Server Management Studio et vérifiez que la base de données d’état de conformité **MBAM** est installée.

4. Sur le serveur sur lequel les rapports de conformité et d’audit sont installés, ouvrez un navigateur web avec des informations d’identification administratives et accédez à l'« accueil » du site SQL Server Reporting Services site.

   L’emplacement d’accueil par défaut d’SQL Server Reporting Services instance de site est http:// <em> &lt; NomofMBAMReportsServer &gt; </em> /Reports. Pour rechercher l’URL réelle, utilisez l’outil Gestionnaire de configuration de Reporting Services et sélectionnez les instances spécifiées lors de l’installation.

   Confirmez qu’un dossier Rapports nommé Microsoft BitLocker Administration and Monitoring contient une source de données appelée **MalteDataSource** et qu’un dossier **en-us** contient quatre rapports.

   **Remarque**  
   Si SQL Server Reporting Services a été configurée en tant qu’instance nommée, l’URL doit ressembler à ce qui suit : http://* &lt; NameofMBAMReportsServer &gt; */Reports\_* &lt; SRSInstanceName &gt; *



~~~
**Note**  
If SSRS was not configured to use Secure Socket Layer (SSL), the URL for the reports will be set to HTTP instead of HTTPS when you install the MBAM Server. If you then go to the Administration and Monitoring website and select a report, the following message appears: “Only Secure Content is Displayed.” To show the report, click **Show All Content**.
~~~



5. Sur le serveur sur lequel la fonctionnalité d’administration et de surveillance est installée, exécutez le Gestionnaire de **serveur** et accédez à **Rôles.** Sélectionnez **Serveur Web (IIS),** puis cliquez sur **Internet Information Services (IIS).**

6. Dans **Connexions, accédez** à * &lt; &gt; nom d’ordinateur,* sélectionnez **Sites,** puis sélectionnez Administration et surveillance **de Microsoft BitLocker.** Vérifiez que **MBAMAdministrationService,** **MBAMUserSupportService,** **MBAMComplianceStatusService**et **MBAMRecoveryAndHardwareService** sont répertoriés.

7. Sur le serveur sur lequel les fonctionnalités d’administration et de surveillance et le portail Self-Service sont installés, ouvrez un navigateur web avec des informations d’identification d’administration et accédez aux emplacements suivants pour vérifier qu’ils se chargent correctement :

   -   *http:// nom &lt; d’hôte &gt; /HelpDesk/default.aspx* et confirmez chacun des liens pour la navigation et les rapports

   -   *http:// &lt; nom d’hôte &gt; /SelfService&gt;/*

   -   *http:// nom &lt; de l’ordinateur &gt; /MBAMAdministrationService/AdministrationService.svc*

   -   *http:// &lt; hostname &gt; /MBAMUserSupportService/UserSupportService.svc*

   -   *http:// &lt; nom de &gt; l’ordinateur /MBAMComplianceStatusService/StatusReportingService.svc*

   -   *http:// nom &lt; de l’ordinateur &gt; /MBAMRecoveryAndHardwareService/CoreService.svc*

   **Remarque**  
   Il est supposé que les fonctionnalités du serveur ont été installées sur le port par défaut sans chiffrement réseau. Si vous avez installé les fonctionnalités serveur sur un autre port ou répertoire virtuel, modifiez les URL pour inclure le port approprié, par exemple, *http:// &lt; hostname &gt; : port &lt; &gt; /HelpDesk/default.asp*x ou*http:// &lt; hostname &gt; : port &lt; &gt; / &lt; virtualdirectory &gt; /default.aspx*

   Si les fonctionnalités du serveur ont été installées avec le chiffrement réseau, http:// en https://.



## <a name="related-topics"></a>Rubriques associées


[Déploiement de l'infrastructure de serveur MBAM 2.0](deploying-the-mbam-20-server-infrastructure-mbam-2.md)









