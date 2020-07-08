---
title: Comment installer le serveur de gestion sur un ordinateur autonome et le connecter à la base de données
description: Comment installer le serveur de gestion sur un ordinateur autonome et le connecter à la base de données
author: dansimp
ms.assetid: 95281287-cb56-4117-befd-854268ea147c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 86f384e88b85101855287bb428e75376f7974219
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805419"
---
# Comment installer le serveur de gestion sur un ordinateur autonome et le connecter à la base de données


Utilisez la procédure suivante pour installer le serveur de gestion sur un ordinateur autonome et le connecter à la base de données.

**Pour installer le serveur de gestion sur un ordinateur autonome en le connectant à la base de données**

1.  Copiez les fichiers d’installation de App-V 5,0 Server sur l’ordinateur sur lequel vous voulez procéder à l’installation. Pour démarrer l’installation de l’application-V 5,0 Server, cliquez avec le bouton droit et exécutez **appv\_server\_setup.exe** en tant qu’administrateur. Cliquez sur **Installer**.

2.  Sur la page **mise en route** , consultez et acceptez les termes du contrat de licence, puis cliquez sur **suivant**.

3.  Sur la page **utiliser Microsoft Update pour garantir la sécurité et** la mise à jour de votre ordinateur, vous pouvez activer les mises à jour Microsoft en sélectionnant **utiliser Microsoft Update lorsque je recherche les mises à jour (recommandé).** Pour désactiver les mises à jour Microsoft, sélectionnez **je ne veux pas utiliser Microsoft Update**. Cliquez sur **Suivant**.

4.  Dans la page de **sélection des fonctionnalités** , activez la case à cocher **serveur de gestion** , puis cliquez sur **suivant**.

5.  Dans la page **emplacement d’installation** , acceptez l’emplacement par défaut, puis cliquez sur **suivant**.

6.  Sur la page **configurer la base de données de gestion existante** , sélectionnez **utiliser un serveur SQL distant**, puis tapez le nom de l’ordinateur exécutant Microsoft SQL SQL (par exemple, **SqlServerMachine**.

    **Remarque**  
    Si Microsoft SQL Server est déployé sur le même serveur, sélectionnez **use local SQL Server**.



~~~
For the SQL Server Instance, select **Use the default instance**. If you are using a custom Microsoft SQL Server instance, you must select **Use a custom instance** and then type the name of the instance.

Specify the **SQL Server Database name** that this management server will use, for example **AppvManagement**.
~~~

7. Dans la page Configuration du **serveur de gestion** , spécifiez le groupe d’annonces ou le compte qui sera connecté à la console de gestion à des fins d’administration, par exemple **MyDomain\\MyUser** ou **MyDomain\\AdminGroup**. Le compte ou le groupe d’annonces que vous spécifiez est activé pour gérer le serveur par le biais de la console de gestion. Vous pouvez ajouter des utilisateurs ou des groupes supplémentaires à l’aide de la console de gestion après l’installation.

   Spécifiez le **nom du site Web** que vous voulez utiliser pour le service de gestion. Acceptez la valeur par défaut si vous n’avez pas de nom personnalisé. Pour la **liaison de port**, spécifiez un numéro de port unique à utiliser (par exemple, **12345**).

8. Cliquez sur **Installer**.

9. Pour vérifier que la configuration s’est déroulée correctement, ouvrez un navigateur Web, puis tapez l’URL suivante: http://managementserver:portnumber/Console.html si l’installation a réussi, vous devriez voir la **console de gestion Silverlight** sans message d’erreur ou avertissement affiché.

   Vous **avez une suggestion pour App-V**? Ajoutez ou Votez en fonction [de suggestions.](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization) **Vous avez un problème lié à l’application-V?** Utilisez le [Forum TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Rubriques connexes


[Déploiement d'App-V5.0](deploying-app-v-50.md)









