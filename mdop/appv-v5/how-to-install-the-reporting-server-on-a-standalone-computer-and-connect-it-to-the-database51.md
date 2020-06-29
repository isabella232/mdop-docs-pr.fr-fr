---
title: Comment installer le serveur de rapports sur un ordinateur autonome et le connecter à la base de données
description: Comment installer le serveur de rapports sur un ordinateur autonome et le connecter à la base de données
author: dansimp
ms.assetid: 11f07750-4045-4c8d-a583-7d70c9e9aa7b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 67866714ff6ae60097d9b368fd0eaf361b08eec6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805377"
---
# Comment installer le serveur de rapports sur un ordinateur autonome et le connecter à la base de données

Utilisez la procédure suivante pour installer le serveur de création de rapports sur un ordinateur autonome et le connecter à la base de données.

**Important** Avant d’exécuter la procédure suivante, vous devez lire et comprendre [à propos de la création de rapports App-V 5,1](about-app-v-51-reporting.md).

## Pour installer le serveur de création de rapports sur un ordinateur autonome et le connecter à la base de données

1. Copiez les fichiers d’installation de App-V 5,1 Server sur l’ordinateur sur lequel vous voulez procéder à l’installation. Pour démarrer l’installation de l’application-V 5,1 Server, cliquez avec le bouton droit et exécutez **appv\_server\_setup.exe** en tant qu’administrateur. Cliquez sur **Installer**.

2. Sur la page **mise en route** , consultez et acceptez les termes du contrat de licence, puis cliquez sur **suivant**.

3. Sur la page **utiliser Microsoft Update pour garantir la sécurité et** la mise à jour de votre ordinateur, vous pouvez activer les mises à jour Microsoft en sélectionnant **utiliser Microsoft Update lorsque je recherche les mises à jour (recommandé).** Pour désactiver les mises à jour Microsoft, sélectionnez **je ne veux pas utiliser Microsoft Update**. Cliquez sur **Suivant**.

4. Dans la page de **sélection des fonctionnalités** , activez la case à cocher serveur de **création de rapports** , puis cliquez sur **suivant**.

5. Dans la page **emplacement d’installation** , acceptez l’emplacement par défaut, puis cliquez sur **suivant**.

6. Dans la page **configurer la base de données de création de rapports existants** , sélectionnez **utiliser un serveur SQL distant**, puis tapez le nom de l’ordinateur exécutant Microsoft SQL Server, par exemple **SqlServerMachine**.

    > [!NOTE]
    > Si Microsoft SQL Server est déployé sur le même serveur, sélectionnez **use local SQL Server**.

    Pour l’instance SQL Server, sélectionnez **utiliser l’instance par défaut**. Si vous utilisez une instance de Microsoft SQL Server personnalisée, vous devez sélectionner **utiliser une instance personnalisée** , puis taper le nom de l’instance.

    Spécifiez le **nom de la base de données SQL Server** qu’utilisera ce serveur de création de rapports, par exemple, **AppvReporting**.

7. Dans la page **configuration du serveur de rapports** .

   - Spécifiez le nom du site Web que vous voulez utiliser pour le service de création de rapports. Ne modifiez pas la valeur par défaut si vous n’avez pas de nom personnalisé.

   - Pour la **liaison de port**, spécifiez un numéro de port unique qui sera utilisé par App-V 5,1, par exemple **55555**. Vous devez également vous assurer que le port spécifié n’est pas utilisé par un autre site Web.

8. Cliquez sur **Installer**.

**Vous avez un problème lié à l’application-V?** Utilisez le [Forum TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Rubriques connexes

[À propos de la création de rapports d'App-V5.1](about-app-v-51-reporting.md)

[Déploiement d'App-V5.1](deploying-app-v-51.md)

[Activation de la création de rapports sur App-V5.1 Client à l'aide de PowerShell](how-to-enable-reporting-on-the-app-v-51-client-by-using-powershell.md)
