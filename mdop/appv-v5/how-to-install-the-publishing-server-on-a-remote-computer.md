---
title: Comment installer le serveur de publication sur un ordinateur distant
description: Comment installer le serveur de publication sur un ordinateur distant
author: dansimp
ms.assetid: 37970706-54ff-4799-9485-b9b49fd50f37
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9d711fa51ade856b3ac5880ba60a19315c358734
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805395"
---
# Comment installer le serveur de publication sur un ordinateur distant


Utilisez la procédure suivante pour installer le serveur de publication sur un autre ordinateur. Avant d’effectuer la procédure suivante, assurez-vous que le serveur de base de données et de gestion est disponible.

**Pour installer le serveur de publication sur un autre ordinateur**

1. Copiez les fichiers d’installation de App-V 5,0 Server sur l’ordinateur sur lequel vous voulez procéder à l’installation. Pour démarrer l’installation de l’application-V 5,0 Server, cliquez avec le bouton droit et exécutez **appv\_server\_setup.exe** en tant qu’administrateur. Cliquez sur **Installer**.

2. Sur la page **mise en route** , consultez et acceptez les termes du contrat de licence, puis cliquez sur **suivant**.

3. Sur la page **utiliser Microsoft Update pour garantir la sécurité et** la mise à jour de votre ordinateur, vous pouvez activer les mises à jour Microsoft en sélectionnant **utiliser Microsoft Update lorsque je recherche les mises à jour (recommandé).** Pour désactiver les mises à jour Microsoft, sélectionnez **je ne veux pas utiliser Microsoft Update**. Cliquez sur **Suivant**.

4. Dans la page de **sélection des fonctionnalités** , activez la case à cocher **serveur de publication** , puis cliquez sur **suivant**.

5. Dans la page **emplacement d’installation** , acceptez l’emplacement par défaut, puis cliquez sur **suivant**.

6. Dans la page Configuration du **serveur de publication** , spécifiez les éléments suivants:

   -   URL du service de gestion auquel est connecté le serveur de publication. Par exemple, **http://ManagementServerName:12345** .

   -   Spécifiez le nom du site Web que vous voulez utiliser pour le service de publication. Acceptez la valeur par défaut si vous n’avez pas de nom personnalisé.

   -   Pour la **liaison de port**, spécifiez un numéro de port unique qui sera utilisé par App-V 5,0, par exemple **54321**.

7. Sur la page **prêt pour l’installation** , cliquez sur **installer**.

8. Une fois l’installation terminée, le serveur de publication doit être enregistré auprès du serveur de gestion. Dans la console de gestion App-V 5,0, procédez comme suit pour inscrire le serveur:

   1.  Ouvrez la console App-V 5,0 Management Server.

   2.  Dans le volet gauche, sélectionnez **serveurs**, puis sélectionnez **inscrire un nouveau serveur**.

   3.  Entrez le nom de ce serveur et une description (si nécessaire), puis cliquez sur **Ajouter**.

9. Pour vérifier que le serveur de publication s’exécute correctement, importez un package sur le serveur de gestion, configurez le package dans un groupe d’annonces et publiez le package. À l’aide d’un navigateur Internet, ouvrez l’URL suivante: <strong> http://publishingserver:pubport </strong> . Si le serveur fonctionne correctement, des informations similaires à ce qui suit s’affichent:

   ```xml
   <Publishing Protocol="1.0">
     <Packages>
       <Package PackageId="28115343-06e2-44dc-a327-3a0b9b868bda" VersionId="5d03c08f-51dc-4026-8cf9-15ebe3d65a72" PackageUrl="\\server\share\file.appv" />
     </Packages>
     <NoGroup>
       <Package PackageId="28115343-06e2-44dc-a327-3a0b9b868bda" />
     </NoGroup>
   </Publishing>
   ```

   Vous **avez une suggestion pour App-V**? Ajoutez ou Votez en fonction [de suggestions.](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization) **Vous avez un problème lié à l’application-V?** Utilisez le [Forum TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Rubriques connexes


[Déploiement d'App-V5.0](deploying-app-v-50.md)

 

 





