---
title: Comment installer les bases de données de gestion et de rapports sur des ordinateurs distincts des services de gestion et de rapports
description: Comment installer les bases de données de gestion et de rapports sur des ordinateurs distincts des services de gestion et de rapports
author: dansimp
ms.assetid: 2a67402e-3119-40ea-a247-24d166af1ced
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2332f674f10a9b60aa1cee814c6eac4ddbe4f5af
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805424"
---
# Comment installer les bases de données de gestion et de rapports sur des ordinateurs distincts des services de gestion et de rapports

Utilisez la procédure suivante pour installer le serveur de base de données et le serveur de gestion sur des ordinateurs différents. L’ordinateur sur lequel vous envisagez d’installer le serveur de base de données doit exécuter une version prise en charge de Microsoft SQL, ou l’installation échoue.

> [!NOTE]
> À la fin du déploiement, le nom de l’instance, le nom de l' **instance** et le nom **de la base de données** **Microsoft SQL Server**sont requis par l’administrateur qui installe le service pour pouvoir se connecter à ces bases de données.

## Pour installer la base de données de gestion et le serveur de gestion sur des ordinateurs séparés

1. Copiez les fichiers d’installation de App-V 5,1 Server sur l’ordinateur sur lequel vous voulez procéder à l’installation. Pour démarrer l’installation de l’application-V 5,1 Server, cliquez avec le bouton droit et exécutez **appv\_server\_setup.exe** en tant qu’administrateur. Cliquez sur **Installer**.
1. Sur la page **mise en route** , consultez et acceptez les termes du contrat de licence, puis cliquez sur **suivant**.
1. Sur la page **utiliser Microsoft Update pour garantir la sécurité et** la mise à jour de votre ordinateur, vous pouvez activer les mises à jour Microsoft en sélectionnant **utiliser Microsoft Update lorsque je recherche les mises à jour (recommandé).** Pour désactiver les mises à jour Microsoft, sélectionnez **je ne veux pas utiliser Microsoft Update**. Cliquez sur **Suivant**.
1. Dans la page de **sélection des fonctionnalités** , sélectionnez les composants que vous voulez installer en sélectionnant la case **de base de données du serveur de gestion** , puis cliquez sur **suivant**.
1. Dans la page **emplacement d’installation** , acceptez l’emplacement par défaut, puis cliquez sur **suivant**.
1. Dans la **page créer un serveur de base de données**initial, acceptez les sélections par défaut, puis cliquez sur **suivant**.

    Si vous utilisez une instance SQL Server personnalisée, sélectionnez **utiliser une instance personnalisée** et tapez le nom de l’instance.
    Si vous utilisez un nom de base de données personnalisé, sélectionnez **configuration personnalisée** , puis tapez le nom de la base de données.

1. Dans la page **créer une base de données de serveur de gestion** suivante, sélectionnez **utiliser un ordinateur distant**, puis entrez le compte d’ordinateur distant en utilisant le format suivant: **Domain\\MachineAccount**.

    > [!NOTE]
    > Si vous envisagez de déployer le serveur de gestion sur le même ordinateur, vous devez sélectionner **utiliser cet ordinateur local**.

1. Spécifiez le nom d’utilisateur de l' **administrateur d’installation** du serveur de gestion en utilisant le format suivant: **Domain\\AdministratorLoginName**. Cliquez sur **Suivant**.
1. Pour démarrer l’installation, cliquez sur **installer**.

## Pour installer la base de données de création de rapports et le serveur de rapports sur des ordinateurs distincts

1. Copiez les fichiers d’installation de App-V 5,1 Server sur l’ordinateur sur lequel vous voulez procéder à l’installation. Pour démarrer l’installation de l’application-V 5,1 Server, cliquez avec le bouton droit et exécutez **appv\_server\_setup.exe** en tant qu’administrateur. Cliquez sur **Installer**.
1. Sur la page **mise en route** , consultez et acceptez les termes du contrat de licence, puis cliquez sur **suivant**.
1. Sur la page **utiliser Microsoft Update pour garantir la sécurité et** la mise à jour de votre ordinateur, vous pouvez activer les mises à jour Microsoft en sélectionnant **utiliser Microsoft Update lorsque je recherche les mises à jour (recommandé).** Pour désactiver les mises à jour Microsoft, sélectionnez **je ne veux pas utiliser Microsoft Update**. Cliquez sur **Suivant**.
1. Dans la page de **sélection des fonctionnalités** , sélectionnez les composants que vous voulez installer en sélectionnant la case **de base de données du serveur de création de rapports** , puis cliquez sur **suivant**.
1. Dans la page **emplacement d’installation** , acceptez l’emplacement par défaut, puis cliquez sur **suivant**.
1. Dans la page **de création de base de données initiale de création de rapports** , acceptez les sélections par défaut le cas échéant, puis cliquez sur **suivant**.

    Si vous utilisez une instance SQL Server personnalisée, sélectionnez **utiliser une instance personnalisée** et tapez le nom de l’instance.
    Si vous utilisez un nom de base de données personnalisé, sélectionnez **configuration personnalisée** , puis tapez le nom de la base de données.

1. Dans la page **créer une base de données de serveur de** création de rapports, sélectionnez **utiliser un ordinateur distant**, puis entrez le compte d’ordinateur distant en utilisant le format suivant: **Domain\\MachineAccount**.

    > [!NOTE]
    > Si vous envisagez de déployer le serveur de création de rapports sur le même ordinateur, vous devez sélectionner **utiliser cet ordinateur local**.

1. Spécifiez le nom d’utilisateur pour le **serveur de** création de rapports à l’aide du format suivant: **Domain\\AdministratorLoginName**. Cliquez sur **Suivant**.
1. Pour démarrer l’installation, cliquez sur **installer**.

## Pour installer les bases de données de gestion et de création de rapports à l’aide de scripts de base de données App-V 5,1

1. Copiez les fichiers d’installation de App-V 5,1 Server sur l’ordinateur sur lequel vous voulez procéder à l’installation.
1. Pour extraire les scripts de base de données App-V 5,1, ouvrez une invite de commandes et spécifiez l’emplacement d’enregistrement des fichiers d’installation, puis exécutez la commande suivante:

    **appv\_server\_setup.exe** **/Layout** **/LAYOUTDIR = "InstallationExtractionLocation"**.

1. Une fois l’extraction terminée, pour accéder au fichier Lisez-moi scripts et instructions de la base de données App-V 5,1:

    - Les scripts et instructions de la base de données de gestion App-V 5,1 se trouvent dans **InstallationExtractionLocation**le dossier suivant:  \\  base de données de gestion des**scripts de base de données**InstallationExtractionLocation  \\  **Management Database**.
    - Les scripts et instructions de la base de données de création de rapports App-V 5,1 se **InstallationExtractionLocation**trouvent dans le dossier suivant:  \\  **Database Scripts**  \\  **base de données de création de rapports**de la base de données InstallationExtractionLocation.

1. Pour chaque base de données, copiez les scripts dans un partage et modifiez-les en suivant les instructions dans le fichier Lisez-moi.

    > [!NOTE]
    > Pour plus d’informations sur la modification des SID requis contenus dans les scripts, voir [Comment installer les bases de données App-V et convertir les identificateurs de sécurité associés à l’aide de PowerShell](how-to-install-the-app-v-databases-and-convert-the-associated-security-identifiers--by-using-powershell51.md).

1. Exécutez les scripts sur l’ordinateur exécutant Microsoft SQL Server.

**Vous avez un problème lié à l’application-V?** Utilisez le [Forum TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Rubriques connexes

[Déploiement d'App-V5.1](deploying-app-v-51.md)
