---
title: Installation et configuration de MBAM sur un seul serveur
description: Installation et configuration de MBAM sur un seul serveur
author: dansimp
ms.assetid: 55841c63-bad9-44e7-b7fd-ea7037febbd7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 225f66493ceafce5461df3fcc6f701e9a2922a5f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810350"
---
# Installation et configuration de MBAM sur un seul serveur


Les procédures décrites dans cette rubrique décrivent l’installation complète des fonctionnalités d’administration et de surveillance de Microsoft BitLocker (MBAM) sur un serveur unique.

Chaque fonctionnalité de serveur comporte certaines conditions préalables. Pour vérifier que vous remplissez les conditions préalables et la configuration matérielle et logicielle requise, voir Configuration requise pour le [déploiement d’MBAM 1,0](mbam-10-deployment-prerequisites.md) et [Configurations prises en charge par MBAM 1,0](mbam-10-supported-configurations.md). De plus, certaines fonctions disposent également d’informations qui doivent être fournies pendant le processus d’installation pour le déploiement de la fonctionnalité. Avant de commencer le déploiement MBAM, nous vous conseillons également [de consulter préparer votre environnement pour MBAM 1,0](preparing-your-environment-for-mbam-10.md) .

**Remarques**  Pour obtenir les fichiers journaux d’installation, vous devez installer MBAM à l’aide du package **msiexec** et de l’option **/l** &lt; emplacement &gt; . Les fichiers journaux sont créés à l’emplacement que vous spécifiez.

D’autres fichiers journaux d’installation sont créés dans le dossier% Temp% de l’utilisateur qui installe MBAM.

 

## Pour installer les fonctionnalités du serveur MBAM sur un serveur unique


Les étapes suivantes expliquent comment installer les fonctionnalités MBAM générales.

**Remarques**  Vérifiez que vous utilisez la configuration de 32 bits sur les serveurs 32 bits et la configuration 64 bits sur les serveurs 64.

 

**Pour démarrer l’installation de fonctionnalités de MBAM Server**

1.  Démarrez l’Assistant Installation de MBAM. Cliquez sur **installer** sur la page d’accueil.

2.  Lisez et acceptez les termes du contrat de licence logiciel Microsoft, puis cliquez sur **suivant** pour continuer l’installation.

3.  Par défaut, toutes les fonctionnalités de MBAM sont sélectionnées pour l’installation. Les fonctionnalités qui seront installées sur le même ordinateur doivent être installées en même temps. Effacez les fonctionnalités que vous voulez installer ailleurs. Vous devez installer les fonctionnalités MBAM dans l’ordre suivant:

    -   Base de données de récupération et de matériel

    -   Base de données d’audit et de conformité

    -   Rapports et audit de conformité

    -   Serveur d’administration et de surveillance

    -   Modèle de stratégie de groupe MBAM

    **Remarques**  L’Assistant installation vérifie la configuration requise pour votre installation et affiche les conditions préalables manquantes. Si toutes les conditions préalables sont remplies, l’installation continue. Si un prérequis manquant est détecté, vous devez résoudre les conditions préalables manquantes, puis cliquez à **nouveau sur vérifier les conditions préalables**. Une fois que toutes les conditions préalables sont remplies, l’installation reprend.

     

4.  Vous êtes invité à configurer la sécurité des communications réseau. MBAM peut crypter la communication entre la base de données de récupération et de matériel, le serveur d’administration et de surveillance, ainsi que les clients. Si vous décidez de chiffrer la communication, vous êtes invité à sélectionner le certificat de mise en service de l’autorité qui sera utilisé pour le chiffrement.

5.  Cliquez sur **Suivant** pour poursuivre.

6.  L’Assistant de configuration de MBAM affiche les pages d’installation correspondant aux composants sélectionnés.

**Pour déployer les fonctionnalités du serveur MBAM**

1.  Dans la fenêtre **configurer la base de données de récupération et de matériel** , spécifiez l’instance de SQL Server et le nom de la base de données qui stockera les données de récupération et de matériel. Vous devez également spécifier l’emplacement des fichiers de base de données et l’emplacement des informations de journal.

2.  Cliquez sur **Suivant** pour poursuivre.

3.  Dans la fenêtre **configuration de la conformité et de la base de données d’audit** , spécifiez l’instance de SQL Server, ainsi que le nom de la base de données qui stockera les données d’audit et de conformité. Spécifiez ensuite l’emplacement des fichiers de base de données et l’emplacement des informations de journal.

4.  Cliquez sur **Suivant** pour poursuivre.

5.  Dans la fenêtre **rapports de conformité et d’audit** , spécifiez l’instance de service de rapport qui sera utilisée et attribuez un compte d’utilisateur de domaine pour accéder à la base de données. Il doit s’agir d’un compte d’utilisateur configuré spécifiquement pour cette utilisation. Le compte d’utilisateur doit être en mesure d’accéder à toutes les données disponibles dans le groupe utilisateurs de reports MBAM.

6.  Cliquez sur **Suivant** pour poursuivre.

7.  Dans la fenêtre **configurer le serveur d’administration et de surveillance** , entrez la **liaison de port**, le nom d' **hôte** (facultatif) et le **chemin d’installation** du serveur d’administration et de surveillance MBAM.

    **Avertissement**  Le numéro de port que vous spécifiez doit être un numéro de port inutilisé sur le serveur d’administration et de surveillance, sauf s’il s’agit d’un nom d’en-tête d’hôte unique.

     

8.  Cliquez sur **Suivant** pour poursuivre.

9.  Indiquez si vous souhaitez utiliser les mises à jour de Microsoft pour renforcer la sécurité de votre ordinateur, puis cliquez sur **suivant**. L’option Microsoft Updates n’active pas les mises à jour automatiques dans Windows.

10. Lorsque l’Assistant installation a collecté les informations de fonctionnalité nécessaires, l’installation MBAM est prête à démarrer. Cliquez sur **retour** pour revenir à l’Assistant pour consulter ou modifier vos paramètres d’installation. Cliquez sur **installer** pour lancer l’installation. Cliquez sur **Annuler** pour quitter le programme d’installation. Le programme d’installation installe les fonctionnalités de MBAM et vous signale que l’installation est terminée.

11. Cliquez sur **Terminer** pour quitter l’Assistant.

12. Après avoir installé les fonctionnalités du serveur MBAM, vous devez ajouter des utilisateurs aux rôles MBAM. Pour plus d’informations, reportez-vous [à planification des rôles d’administrateur MBAM 1,0](planning-for-mbam-10-administrator-roles.md).

**Pour effectuer une configuration de post-installation**

1.  Une fois l’installation terminée, vous devez ajouter des rôles d’utilisateur afin de permettre aux utilisateurs d’accéder aux fonctionnalités dans le site Web d’administration MBAM. Sur le serveur d’administration et de surveillance, ajoutez des utilisateurs aux groupes locaux suivants:

    -   **Utilisateurs matériels MBAM**: les membres de ce groupe local peuvent accéder à la fonctionnalité matérielle dans le site Web d’administration MBAM.

    -   **Utilisateurs du support technique MBAM**: les membres de ce groupe local peuvent accéder à la récupération du lecteur et gérer les fonctionnalités du TPM dans le site Web d’administration MBAM. Pour un utilisateur du support technique, tous les champs de la récupération de lecteur et de la gestion de TPM sont obligatoires.

    -   **Utilisateurs expérimentés du support technique MBAM**: les membres de ce groupe local disposent d’un accès avancé aux fonctionnalités de récupération de lecteur et de gestion des composants de plateforme dans le site Web d’administration MBAM. Pour les utilisateurs expérimentés du support technique, seul le champ ID clé est requis pour la récupération du lecteur. Pour gérer les utilisateurs de GPC, seuls le champ domaine de l’ordinateur et le champ nom de l’ordinateur sont obligatoires.

2.  Sur la base de données d’administration et de surveillance du serveur, de la conformité et de l’audit, et de l’ordinateur qui héberge les rapports de conformité et d’audit, ajoutez des utilisateurs au groupe local suivant pour leur permettre d’accéder à la fonctionnalité rapports dans le site Web d’administration MBAM:

    -   **Utilisateurs du rapport MBAM**: les membres de ce groupe local peuvent accéder aux fonctionnalités de rapport dans le site Web d’administration MBAM.

    **Remarques**  Il est possible de mettre à jour les membres d’une appartenance à un groupe ou d’une appartenance de groupe du groupe local du **rapport MBAM** sur tous les ordinateurs sur lesquels les rapports d’administration et de surveillance des fonctionnalités du serveur

    Pour conserver une appartenance identique sur tous les ordinateurs, vous devez créer un groupe de sécurité de domaine et ajouter ce groupe de domaine à chaque groupe utilisateurs de rapports MBAM locaux. Lorsque vous procédez ainsi, vous pouvez gérer l’appartenance à un groupe à l’aide du groupe de domaines.

     

## Validation de l’installation de la fonctionnalité MBAM Server


À l’issue de l’installation d’MBAM, vérifiez que l’installation a correctement configuré toutes les fonctionnalités MBAM nécessaires pour la gestion de BitLocker. Utilisez la procédure suivante pour vérifier que le service MBAM fonctionne:

**Pour valider l’installation de la fonctionnalité MBAM Server**

1. Sur chaque serveur sur lequel est déployée une fonctionnalité MBAM, ouvrez **le panneau de configuration**. Cliquez sur **programmes**, puis sur **programmes et fonctionnalités**. Vérifiez que la fonctionnalité **administration et analyse de BitLocker Microsoft** s’affiche dans la liste **programmes et fonctionnalités** .

   **Remarque**  
   Pour valider l’installation, vous devez utiliser un compte de domaine disposant d’informations d’identification d’administrateur local sur chaque serveur.

     

2. Sur le serveur sur lequel la base de données de récupération et de matériel est installée, ouvrez SQL Server Management Studio, puis vérifiez que la base de données **MBAM et de récupération** de la base de données est installée.

3. Sur le serveur sur lequel la base de données d’audit et de conformité est installée, ouvrez SQL Server Management Studio, puis vérifiez que la **base de données d’audit et de conformité MBAM** est installée.

4. Sur le serveur sur lequel sont installés les rapports de conformité et d’audit, ouvrez un navigateur Web doté de privilèges d’administration et naviguez jusqu’au site «Home» du site SQL Server Reporting Services.

   L’emplacement d’accueil par défaut d’une instance de site SQL Server Reporting Services se trouve sur http:// <em> &lt; NameofMBAMReportsServer &gt; </em> /reports. Pour trouver l’URL réelle, utilisez l’outil Gestionnaire de configuration Reporting Services et sélectionnez les instances spécifiées lors de l’installation.

   Vérifiez qu’un dossier nommé **rapports de conformité Malte** figure et qu’il contient cinq rapports et une seule source de données.

   **Remarque**  
   Si SQL Server Reporting Services a été configuré en tant qu’instance nommée, l’URL doit ressembler à ce qui suit: http://* &lt; NameofMBAMReportsServer &gt; */Reports\_* &lt; SRSInstanceName &gt; *

     

5. Sur le serveur sur lequel est installé la fonctionnalité d’administration et de surveillance, exécutez le **Gestionnaire de serveur** et naviguez jusqu’à **rôles**, sélectionnez **serveur Web (IIS)**, puis cliquez sur **Gestionnaire des services Internet (IIS)** .

6. Dans **connexions**, naviguez jusqu’à * &lt; nomordinateur &gt; *, sélectionnez **sites**, puis l’option **administration et analyse de Microsoft BitLocker**. Vérifiez que **MBAMAdministrationService**, **MBAMComplianceStatusService**et **MBAMRecoveryAndHardwareService** apparaissent.

7. Sur le serveur sur lequel est installé la fonctionnalité d’administration et de contrôle, ouvrez un navigateur Web avec des privilèges d’administration, puis accédez aux emplacements suivants dans le site Web MBAM pour vérifier qu’ils se chargent correctement:

   -   *http:// &lt; nomordinateur &gt; /default.aspx* et confirmez chacun des liens pour la navigation et les rapports

   -   *http:// &lt; nomordinateur &gt; /MBAMAdministrationService/AdministrationService.svc*

   -   *http:// &lt; nomordinateur &gt; /MBAMComplianceStatusService/StatusReportingService.svc*

   -   *http:// &lt; nomordinateur &gt; /MBAMRecoveryAndHardwareService/CoreService.svc*

   **Remarque**  
   En général, les services sont installés sur le port 80 par défaut sans chiffrement réseau. Si les services sont installés sur un autre port, modifiez les URL pour inclure le port approprié. Par exemple, http://* &lt; nomordinateur &gt; : &lt; port &gt; */default.aspx ou http:// <em> &lt; hostheadername &gt; / </em> default. aspx.

   Si les services sont installés en utilisant le chiffrement réseau, modifiez http://sur https://.

     

## Rubriques connexes


[Déploiement de l'infrastructure de serveur MBAM1.0](deploying-the-mbam-10-server-infrastructure.md)

 

 





