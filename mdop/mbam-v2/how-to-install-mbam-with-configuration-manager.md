---
title: Installation de MBAM avec Configuration Manager
description: Installation de MBAM avec Configuration Manager
author: dansimp
ms.assetid: fd0832e4-3b79-4e56-9550-d2f396be6d09
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a556ce961e6a423caecdd0766cf8623383897b58
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810968"
---
# Installation de MBAM avec Configuration Manager


Cette section décrit la procédure d’installation d’MBAM avec Configuration Manager à l’aide de la configuration recommandée, illustrée dans la section [mise en route de MBAM avec Configuration Manager](getting-started---using-mbam-with-configuration-manager.md). Les étapes sont divisées en tâches suivantes:

-   Installer et configurer MBAM sur le serveur Configuration Manager

-   Installer les bases de données de récupération et d’audit sur le serveur de base de données

-   Installer les fonctionnalités d’administration et de surveillance du serveur sur le serveur d’administration et de surveillance

Avant de commencer l’installation, assurez-vous d’avoir modifié ou créé les fichiers MOF nécessaires. Pour obtenir des instructions, reportez-vous [à création ou modification des fichiers MOF](how-to-create-or-edit-the-mof-files.md).

**Important**  Si vous utilisez une instance de SQL Server Reporting Services (SSRS) qui n’est pas définie par défaut, vous devez démarrer la configuration d’MBAM à l’aide de la ligne de commande suivante pour spécifier l’instance nommée SSRS:

`MbamSetup.exe CM_SSRS_INSTANCE_NAME=<NamedInstance>`

 

**Pour installer MBAM sur le serveur Configuration Manager**

1.  Sur le serveur Configuration Manager, exécutez **MBAMSetup.exe** pour démarrer l’Assistant Installation de MBAM.

    **Remarques**  Pour obtenir les fichiers journaux d’installation, vous devez utiliser le package msiexec et l’option **/l** &lt; emplacement &gt; pour installer Configuration Manager. Les fichiers journaux sont créés à l’emplacement que vous spécifiez.

    D’autres fichiers journaux d’installation sont créés dans le dossier% Temp% sur l’ordinateur de l’utilisateur qui installe le gestionnaire de configuration.

     

2.  Dans la page d' **Accueil** , sélectionnez éventuellement le **programme d’amélioration**du produit, puis cliquez sur **Démarrer**.

3.  Lisez et acceptez le contrat de licence logiciel Microsoft, puis cliquez sur **suivant** pour continuer l’installation.

4.  Dans la page de sélection de la **topologie** , sélectionnez **intégration de System Center Configuration Manager**, puis cliquez sur **suivant**.

5.  Dans la page **Sélectionner les fonctionnalités à installer** , sélectionnez **intégration de System Center Configuration Manager**.

    **Remarques**  Sur la page **vérification des éléments requis** , cliquez sur **suivant** lorsque l’Assistant installation vérifie la configuration requise pour votre installation et confirme qu’aucun élément n’est manquant. Si une condition préalable manquante est détectée, vous devez résoudre les conditions préalables manquantes, puis cliquer de **nouveau sur vérifier les conditions préalables.**

     

6.  Indiquez si vous souhaitez utiliser les mises à jour de Microsoft pour renforcer la sécurité de votre ordinateur, puis cliquez sur **suivant**. L’utilisation des mises à jour de Microsoft n’active pas les mises à jour automatiques dans Windows.

7.  Cliquez sur **Suivant** pour poursuivre.

8.  Dans la page Résumé de l' **installation** , examinez la liste des fonctionnalités qui seront installées, puis cliquez sur **installer** pour commencer à installer les fonctionnalités MBAM. Cliquez sur **retour** pour revenir à l’Assistant pour revoir ou modifier vos paramètres d’installation ou cliquez sur **Annuler** pour quitter le programme d’installation. Le programme d’installation installe les fonctionnalités de MBAM et vous signale que l’installation est terminée.

9.  Cliquez sur **Terminer** pour quitter l’Assistant.

**Pour installer les bases de données de récupération et d’audit sur le serveur de base de données**

1.  Sur le serveur de base de données, exécutez **MBAMSetup.exe** pour démarrer l’Assistant Installation de MBAM.

2.  Dans la page d' **Accueil** , sélectionnez éventuellement le **programme d’amélioration**du produit, puis cliquez sur **Démarrer**.

3.  Lisez et acceptez le contrat de licence logiciel Microsoft, puis cliquez sur **suivant** pour continuer l’installation.

4.  Dans la page de sélection de la **topologie** , sélectionnez la topologie **intégration de System Center Configuration Manager** , puis cliquez sur **suivant**.

5.  Dans la liste des fonctionnalités à installer, sélectionnez **base de données de récupération** et **base de données d’audit**, puis décochez les autres fonctionnalités.

    **Remarques**  L’Assistant installation vérifie la configuration requise pour votre installation et affiche les conditions préalables manquantes. Si toutes les conditions préalables sont remplies, l’installation continue. Si une condition préalable manquante est détectée, vous devez résoudre les conditions préalables manquantes, puis cliquer de **nouveau sur vérifier les conditions préalables**. Si toutes les conditions préalables sont remplies ce délai, l’installation reprend.

     

6.  Dans la page **configurer la base de données de récupération** , spécifiez les noms des ordinateurs qui exécutent la fonctionnalité d’administration et de surveillance du serveur. Après le déploiement de la fonctionnalité d’administration et de surveillance du serveur, il utilise son compte de domaine pour se connecter à la base de données.

7.  Cliquez sur **Suivant** pour poursuivre.

8.  Spécifiez le nom de l’instance SQL Server et le nom de la base de données qui stockera les données de récupération. Vous devez également spécifier l’emplacement de la base de données et l’emplacement où se trouvent les informations de journalisation.

9.  Cliquez sur **suivant** pour continuer avec l’Assistant Installation de MBAM.

10. Dans la page **configurer la base de données d’audit** , spécifiez le compte d’utilisateur qui sera utilisé pour accéder à la base de données pour les rapports.

11. Spécifiez le nom de l’ordinateur qui sera exécuté sur le serveur d’administration et de surveillance ainsi que les rapports d’audit. Après le déploiement des fonctionnalités d’administration et de surveillance et des rapports d’audit, leurs comptes de domaine sont utilisés pour se connecter aux bases de données.

    **Remarques**  Si vous installez la base de données d’audit sans la fonctionnalité rapports d’audit, vous devez ajouter une exception sur l’ordinateur de la base de données d’audit pour activer le trafic entrant sur le port Microsoft SQL Server. Le numéro de port par défaut est 1433.

     

12. Spécifiez le nom de l’instance SQL Server et le nom de la base de données qui stockera les données d’audit. Vous devez également spécifier l’emplacement des informations de base de données et de journalisation.

13. Cliquez sur **installer** pour démarrer l’installation, puis cliquez sur **Terminer** pour terminer l’installation.

**Pour installer les fonctionnalités d’administration et de surveillance du serveur sur le serveur d’administration et de surveillance**

1.  Sur le serveur d’administration et de surveillance, exécutez **MBAMSetup.exe** pour démarrer l’Assistant Installation de MBAM.

2.  Dans la page d' **Accueil** , sélectionnez éventuellement le **programme d’amélioration**du produit, puis cliquez sur **Démarrer**.

3.  Lisez et acceptez le contrat de licence logiciel Microsoft, puis cliquez sur **suivant** pour continuer l’installation.

4.  Dans la page de sélection de la **topologie** , sélectionnez la topologie **intégration de System Center Configuration Manager** , puis cliquez sur **suivant**.

5.  Dans la liste des fonctionnalités à installer, sélectionnez **administration et analyse du serveur** et du **portail libre-service**, puis désactivez les autres fonctionnalités.

    **Remarques**  L’Assistant installation vérifie la configuration requise pour votre installation et affiche les conditions préalables manquantes. Si toutes les conditions préalables sont remplies, l’installation continue. Si une condition préalable manquante est détectée, vous devez résoudre les conditions préalables manquantes, puis cliquer de **nouveau sur vérifier les conditions préalables**. Si toutes les conditions préalables sont remplies ce délai, l’installation reprend.

     

6.  Installez le portail libre-service en suivant les étapes décrites dans la section **installation du portail libre-service** de l' [installation et de la configuration de MBAM sur des serveurs distribués](how-to-install-and-configure-mbam-on-distributed-servers-mbam-2.md).

    **Remarques**  Si les ordinateurs clients n’ont pas accès au réseau de distribution de contenu (CDN) Microsoft, ce qui donne au portail libre-service l’accès requis à certains fichiers JavaScript, suivez les étapes décrites dans la section **pour configurer le portail libre-service lorsque les utilisateurs ne peuvent pas accéder à la section sur le réseau de distribution de contenu Microsoft** [Comment installer et configurer MBAM sur des serveurs distribués](how-to-install-and-configure-mbam-on-distributed-servers-mbam-2.md) pour configurer le portail libre-service de manière à référencer les fichiers JavaScript à partir d’une source accessible.

     

7.  Installez les fonctionnalités d’administration et de surveillance du serveur en suivant les étapes décrites dans la section **installation de la fonctionnalité d’administration et de surveillance du serveur** dans [Comment installer et configurer MBAM sur des serveurs distribués](how-to-install-and-configure-mbam-on-distributed-servers-mbam-2.md).

8.  Cliquez sur **Terminer** pour terminer l’installation.

## Rubriques connexes


[Validation de l'installation de MBAM avec Configuration Manager](how-to-validate-the-mbam-installation-with-configuration-manager.md)

[Déploiement de MBAM avec Configuration Manager](deploying-mbam-with-configuration-manager-mbam2.md)

 

 





