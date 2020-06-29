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
ms.openlocfilehash: 53e170f421bdce8dd6f771af3902af627a15a085
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810332"
---
# Installation et configuration de MBAM sur un seul serveur


Les procédures décrites dans cette rubrique expliquent comment installer l’administration et la surveillance de BitLocker Microsoft (MBAM) dans la topologie autonome sur un serveur unique. Utilisez la configuration serveur unique uniquement dans un environnement de test. Pour les environnements de production, utilisez au moins deux serveurs. Si vous installez le contrôle et l’administration de BitLocker à l’aide de la topologie Configuration Manager, consultez [déploiement d’MBAM avec Configuration Manager](deploying-mbam-with-configuration-manager-mbam2.md).

Le schéma suivant illustre un exemple d’architecture à un serveur unique. Pour obtenir une description des bases de données et fonctionnalités, voir [architecture de haut niveau pour MBAM 2,0](high-level-architecture-for-mbam-20-mbam-2.md).

![topologie de déploiement de serveur unique MBAM 2](images/mbam2-1-server.gif)

Chaque fonctionnalité de serveur comporte certaines conditions préalables. Pour vérifier que vous remplissez les conditions préalables et que vous avez besoin de la configuration matérielle et logicielle requise, voir Configuration requise pour le [déploiement d’MBAM 2,0](mbam-20-deployment-prerequisites-mbam-2.md) et [Configurations prises en charge par MBAM 2,0](mbam-20-supported-configurations-mbam-2.md). De plus, certaines fonctions disposent également d’informations qui doivent être fournies pendant le processus d’installation pour le déploiement de la fonctionnalité. Vous devez également consulter [préparer votre environnement pour MBAM 2,0 avant de](preparing-your-environment-for-mbam-20-mbam-2.md) commencer MBAM déploiement.

**Remarque**  
Pour obtenir les fichiers journaux d’installation, vous devez utiliser le package msiexec et l’option **/l** &lt; emplacement &gt; pour installer MBAM. Les fichiers journaux sont créés à l’emplacement que vous spécifiez.

D’autres fichiers journaux d’installation sont créés dans le dossier% Temp% sur le serveur de l’utilisateur qui installe MBAM.



## Pour installer les fonctionnalités du serveur MBAM sur un serveur unique


Les étapes suivantes expliquent comment installer les fonctionnalités MBAM générales.

**Pour démarrer l’installation de fonctionnalités de MBAM Server**

1.  Sur le serveur sur lequel vous souhaitez installer MBAM, exécutez **MBAMSetup.exe** pour démarrer l’Assistant Installation d’MBAM.

2.  Dans la page d' **Accueil** , sélectionnez éventuellement le **programme d’amélioration**du produit, puis cliquez sur **Démarrer**.

3.  Lisez et acceptez le contrat de licence logiciel Microsoft, puis cliquez sur **suivant** pour continuer l’installation.

4.  Dans la page de sélection de la **topologie** , sélectionnez la topologie **autonome** , puis cliquez sur **suivant**.

5.  Dans la page **Sélectionner les fonctionnalités à installer** , sélectionnez les fonctionnalités que vous voulez installer. Par défaut, toutes les fonctionnalités de MBAM sont sélectionnées pour l’installation. Les fonctionnalités qui doivent être installées sur le même ordinateur doivent être installées en même temps. Désactivez les cases à cocher des fonctionnalités que vous voulez installer ailleurs. Vous devez installer les fonctionnalités d’MBAM dans l’ordre suivant:

    -   Base de données de récupération

    -   Base de données d’audit et de conformité

    -   Rapports de conformité et d’audit

    -   Serveur libre-service

    -   Serveur d’administration et de surveillance

    -   Modèle de stratégie de groupe MBAM

    **Remarque**  
    L’Assistant installation vérifie la configuration requise pour votre installation et affiche les conditions préalables manquantes. Si toutes les conditions préalables sont remplies, l’installation continue. Si une condition préalable manquante est détectée, vous devez résoudre les conditions préalables manquantes, puis cliquer de **nouveau sur vérifier les conditions préalables**. Si toutes les conditions préalables sont remplies ce délai, l’installation reprend.



6.  Dans la page **configure Network Communication Security** , choisissez de chiffrer les communications entre les services Web sur le serveur d’administration et de surveillance et les clients. Si vous décidez de chiffrer la communication, sélectionnez le certificat de certification d’autorité de certification à utiliser pour le chiffrement. Le certificat doit être créé avant cette étape pour vous permettre de le sélectionner dans cette page.

    **Remarque**  
    Cette page s’affiche uniquement si vous avez sélectionné le portail libre-service ou la fonctionnalité de serveur administration et analyse dans la page **Sélectionner les fonctionnalités à installer** .



7.  Cliquez sur **suivant**, puis passez aux étapes suivantes pour configurer les fonctionnalités du serveur MBAM.

**Pour configurer les fonctionnalités du serveur MBAM**

1.  Sur la page **configurer la base de données de récupération** , spécifiez le nom de l’instance SQL Server et le nom de la base de données qui stockera les données de récupération. Vous devez également spécifier les emplacements où se trouvent les fichiers de base de données et l’emplacement où se trouvent les informations de journalisation.

2.  Cliquez sur **Suivant** pour poursuivre.

3.  Sur la page **configurer la conformité et la base de données d’audit** , spécifiez le nom de l’instance SQL Server et le nom de la base de données qui stockera les données de conformité et d’audit. Vous devez également spécifier l’emplacement où se trouvent les fichiers de base de données et l’emplacement où se trouvent les informations de journalisation.

4.  Cliquez sur **Suivant** pour poursuivre.

5.  Sur la page **configurer les rapports de conformité et d’audit** , spécifiez l’instance de SQL Server Reporting Services dans laquelle les rapports de conformité et d’audit seront installés, puis fournissez un compte d’utilisateur et un mot de passe de domaine pour accéder à la base de données d’audit et de conformité. Configurez le mot de passe de ce compte pour qu’il n’expire jamais. Le compte d’utilisateur doit être en mesure d’accéder à toutes les données disponibles dans le groupe utilisateurs de reports MBAM.

6.  Cliquez sur **Suivant** pour poursuivre.

7.  Dans la page **configurer le portail libre-service** , entrez le numéro de port, le nom d’hôte, le nom du répertoire virtuel et le chemin d’installation du portail libre-service.

    **Remarque**  
    Le numéro de port que vous spécifiez doit être un numéro de port inutilisé sur le serveur d’administration et de surveillance sauf si vous spécifiez un nom d’en-tête d’hôte unique. Si vous utilisez le pare-feu Windows, le port s’ouvre automatiquement.



8.  Cliquez sur **Suivant** pour poursuivre.

9.  Indiquez si vous souhaitez utiliser les mises à jour de Microsoft pour renforcer la sécurité de votre ordinateur, puis cliquez sur **suivant**. Les mises à jour automatiques ne sont pas activées dans Windows.

10. Sur la page **configurer le serveur d’administration et de surveillance** , entrez le numéro de port, le nom d’hôte, le nom du répertoire virtuel et le chemin d’installation du support technique du support technique.

    **Remarque**  
    Le numéro de port que vous spécifiez doit être un numéro de port inutilisé sur le serveur d’administration et de surveillance sauf si vous spécifiez un nom d’en-tête d’hôte unique. Si vous utilisez le pare-feu Windows, le port s’ouvre automatiquement.



11. Dans la page Résumé de l' **installation** , examinez la liste des fonctionnalités qui seront installées, puis cliquez sur **installer** pour commencer à installer les fonctionnalités MBAM. Cliquez sur **retour** pour revenir à l’Assistant pour revoir ou modifier vos paramètres d’installation ou cliquez sur **Annuler** pour quitter le programme d’installation. Le programme d’installation installe les fonctionnalités de MBAM et vous signale que l’installation est terminée.

12. Cliquez sur **Terminer** pour quitter l’Assistant. Une fois les fonctionnalités d’administration et de contrôle du serveur Microsoft BitLocker installées, passez à la section suivante et suivez les étapes nécessaires pour ajouter des utilisateurs aux rôles d’administration et de contrôle Microsoft BitLocker. Pour plus d’informations sur les rôles, voir [planification des rôles d’administrateur MBAM 2,0](planning-for-mbam-20-administrator-roles-mbam-2.md).

**Pour effectuer une configuration après l’installation**

1.  Sur le serveur d’administration et de surveillance, ajoutez des utilisateurs aux groupes locaux suivants pour leur permettre d’accéder aux fonctionnalités de site Web du support technique MBAM:

    -   **Utilisateurs du support technique MBAM**: les membres de ce groupe local peuvent accéder à la récupération du lecteur et gérer les fonctionnalités du TPM sur le site Web d’administration et de surveillance MBAM. Pour un utilisateur du support technique, tous les champs de la récupération de lecteur et de la gestion de TPM sont obligatoires.

    -   **Utilisateurs de l’assistance technique avancée MBAM**: les membres de ce groupe local disposent d’un accès avancé aux fonctionnalités de récupération et de gestion du TPM sur le site Web d’administration et de surveillance des MBAM. Pour les utilisateurs expérimentés du support technique, seul le champ **ID clé** est requis pour la récupération du lecteur. Dans gérer le module de plateforme sécurisée, seul le champ domaine de l' **ordinateur** et le champ nom de l' **ordinateur** est requis.

2.  Sur le serveur d’administration et de surveillance, ajoutez des utilisateurs au groupe local suivant pour leur permettre d’accéder à la fonctionnalité rapports sur le site Web d’administration et de surveillance de MBAM:

    -   **Utilisateurs du rapport MBAM**: les membres de ce groupe local peuvent accéder aux fonctionnalités de rapport sur le site Web d’administration et de surveillance de MBAM.

    -   Marquez le portail libre-service avec le nom de votre société, le texte du message d’avis et d’autres informations spécifiques à la société. Pour obtenir des instructions, reportez-vous [à la rubrique Personnalisation du portail libre-service](how-to-brand-the-self-service-portal.md).

    **Remarque**  
    Il est possible d’avoir une appartenance similaire à un utilisateur ou un groupe du groupe local **utilisateurs de rapports MBAM** sur tous les ordinateurs sur lesquels les fonctionnalités d’administration et de surveillance des MBAM, ainsi que les rapports de conformité et d’audit sont installés. Pour cela, nous vous recommandons de créer un groupe de sécurité de domaine et d’ajouter ce groupe de domaine à chaque groupe de utilisateurs de rapport MBAM local. Lorsque vous utilisez ce processus, gérez les appartenances aux groupes par le biais du groupe de domaines.



## Validation de l’installation de la fonctionnalité MBAM Server


Lorsque l’installation de l’administration et du suivi de BitLocker est terminée, vérifiez que l’installation a correctement configuré toutes les fonctionnalités MBAM nécessaires pour la gestion de BitLocker. Utilisez la procédure suivante pour vérifier que le service MBAM est fonctionnel.

**Pour valider l’installation de la fonctionnalité MBAM Server**

1. Sur chaque serveur sur lequel est déployée une fonctionnalité MBAM, ouvrez **le panneau de configuration**. Sélectionnez **programmes**, puis sélectionnez **programmes et fonctionnalités**. Vérifiez que la fonctionnalité **administration et analyse de BitLocker Microsoft** s’affiche dans la liste **programmes et fonctionnalités** .

   **Remarque**  
   Pour valider l’installation, vous devez utiliser un compte de domaine disposant d’informations d’identification d’administrateur local sur chaque serveur.



2. Sur le serveur sur lequel la base de données de récupération est installée, ouvrez SQL Server Management Studio, puis vérifiez que la base de données **MBAM et de récupération** de la base de données est installée.

3. Sur le serveur sur lequel la base de données d’audit et de conformité est installée, ouvrez SQL Server Management Studio, puis vérifiez que la **base de données de statut de conformité MBAM** est installée.

4. Sur le serveur sur lequel sont installés les rapports de conformité et d’audit, ouvrez un navigateur Web contenant les informations d’identification d’administration et naviguez jusqu’au site «Home» du site SQL Server Reporting Services.

   L’emplacement d’accueil par défaut d’une instance de site SQL Server Reporting Services se trouve sur http:// <em> &lt; NameofMBAMReportsServer &gt; </em> /reports. Pour trouver l’URL réelle, utilisez l’outil Gestionnaire de configuration Reporting Services et sélectionnez les instances spécifiées lors de l’installation.

   Confirmez qu’un dossier de rapports intitulé Microsoft BitLocker administration et analyse contient une source de données appelée **MaltaDataSource** et qu’un dossier **en-US** contient quatre rapports.

   **Remarque**  
   Si SQL Server Reporting Services a été configuré en tant qu’instance nommée, l’URL doit ressembler à ce qui suit: http://* &lt; NameofMBAMReportsServer &gt; */Reports\_* &lt; SRSInstanceName &gt; *



~~~
**Note**  
If SSRS was not configured to use Secure Socket Layer (SSL), the URL for the reports will be set to HTTP instead of HTTPS when you install the MBAM Server. If you then go to the Administration and Monitoring website and select a report, the following message appears: “Only Secure Content is Displayed.” To show the report, click **Show All Content**.
~~~



5. Sur le serveur sur lequel est installée la fonctionnalité d’administration et de surveillance, exécutez le **Gestionnaire de serveur** et naviguez jusqu’à **rôles**. Sélectionnez **serveur Web (IIS)**, puis cliquez sur **Gestionnaire des services Internet (IIS).**

6. Dans **connexions,** naviguez jusqu’à * &lt; &gt; nomordinateur*, sélectionnez **sites**, puis cliquez sur **analyse et analyse BitLocker**. Vérifiez que **MBAMAdministrationService**, **MBAMUserSupportService**, **MBAMComplianceStatusService**et **MBAMRecoveryAndHardwareService** sont répertoriés.

7. Sur le serveur sur lequel sont installés les fonctionnalités d’administration et de surveillance et de portail en libre-service, ouvrez un navigateur Web contenant les informations d’identification d’administration et naviguez jusqu’aux emplacements suivants pour vérifier qu’ils se chargent correctement:

   -   *http:// &lt; hostname &gt; /helpdesk/default.aspx* et confirmez chacun des liens pour la navigation et les rapports

   -   *http:// &lt; hostname &gt; /selfservice&gt;/*

   -   *http:// &lt; nomordinateur &gt; /MBAMAdministrationService/AdministrationService.svc*

   -   *http:// &lt; hostname &gt; /MBAMUserSupportService/UserSupportService.svc*

   -   *http:// &lt; nomordinateur &gt; /MBAMComplianceStatusService/StatusReportingService.svc*

   -   *http:// &lt; nomordinateur &gt; /MBAMRecoveryAndHardwareService/CoreService.svc*

   **Remarque**  
   Les fonctionnalités du serveur sont supposées être installées sur le port par défaut sans chiffrement réseau. Si vous avez installé les fonctionnalités du serveur sur un autre port ou répertoire virtuel, modifiez les URL pour inclure le port approprié (par exemple, *http:// &lt; hostname &gt; : &lt; port &gt; /helpdesk/default.asp*x ou*http:// &lt; hostname &gt; : &lt; port &gt; / &lt; VirtualDirectory &gt; /default.aspx*

   Si les fonctionnalités du serveur ont été installées avec le chiffrement réseau, modifiez http://sur https://.



## Rubriques connexes


[Déploiement de l'infrastructure de serveur MBAM2.0](deploying-the-mbam-20-server-infrastructure-mbam-2.md)









