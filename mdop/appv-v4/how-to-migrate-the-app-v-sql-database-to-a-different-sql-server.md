---
title: Procédure pour migrer la base de données SQL d'App-V vers un autre SQL Server
description: Procédure pour migrer la base de données SQL d'App-V vers un autre SQL Server
author: dansimp
ms.assetid: 353892a1-9327-4489-a19c-4ec7bd1b736f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e3d84b0cb328873db3722ad3eb9af6a2b442fdcf
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806961"
---
# Procédure pour migrer la base de données SQL d'App-V vers un autre SQL Server


Les procédures suivantes décrivent en détail la migration de la base de données SQL du serveur de gestion Microsoft application (App-V) vers un autre serveur SQL Server.

**Important**  Cette procédure requiert l’arrêt du service App-V Server et cela empêchera les utilisateurs finaux d’utiliser leurs applications.

 

**Pour sauvegarder la base de données SQL App-V**

1.  Ouvrez le programme services. msc, puis arrêtez le service App-V Management Server sur tous les serveurs de gestion utilisant la base de données à migrer.

2.  Sur l’ordinateur sur lequel se trouve la base de données App-V, ouvrez SQL Server Management Studio.

3.  Développez le nœud **bases de données** et recherchez la base de données App-V (le nom par défaut est APPVIRT).

4.  Cliquez avec le bouton droit sur la base de données, puis sélectionnez **tâches** et **sauvegarder**.

5.  Vérifiez que le **modèle de récupération** est défini sur **simple** et que le **type de sauvegarde** est défini sur **complet**. Modifiez les paramètres de **destination** et de **jeu de sauvegarde** , le cas échéant.

6.  Cliquez sur **OK** pour sauvegarder la base de données. Lorsque la sauvegarde a été effectuée avec succès, cliquez sur **OK**.

7.  Ouvrez l’Explorateur Windows et naviguez jusqu’au dossier contenant le fichier de sauvegarde de la base de données (par exemple, APPVIRT. BAK. Copiez le fichier de sauvegarde de la base de données sur l’ordinateur de destination exécutant SQL Server.

**Pour restaurer la base de données SQL App-V sur l’ordinateur de destination**

1.  Sur l’ordinateur de destination, ouvrez SQL Server Management Studio, cliquez avec le bouton droit sur le nœud **bases de données** , puis sélectionnez **restaurer la base de données**.

2.  Sous **source pour la restauration**, choisissez **à partir de l’appareil** , puis cliquez sur «**...».** .

3.  Dans la boîte de dialogue **spécifier la sauvegarde** , assurez-vous que l’option **média de sauvegarde** est définie sur **fichier** , puis cliquez sur **Ajouter**.

4.  Sélectionnez le fichier de sauvegarde que vous avez copié à partir de l’ordinateur d’origine exécutant SQL Server, puis cliquez sur **OK**.

5.  Cliquez sur **OK** , puis sélectionnez le jeu de sauvegarde à restaurer.

6.  Sous **destination pour la restauration**, cliquez sur la liste déroulante pour la **base de données** , puis sélectionnez le nom de la base de données App-V (par exemple, APPVIRT.

7.  Cliquez sur **OK** pour démarrer la restauration. Lorsque la restauration s’est déroulée correctement, cliquez sur **OK**.

8.  Développez le nœud **sécurité** , cliquez avec le bouton droit sur **connexions** et sélectionnez **nouvelle connexion**.

9.  Dans le champ **nom de connexion** , entrez les informations de compte de service réseau pour le serveur de gestion de l’application-V au format DOMAIN\\SERVERNAME $.

10. Dans la page **général** de la **base de données par défaut** , sélectionnez le nom de la base de données App-V (par exemple, APPVIRT), puis cliquez sur **OK**.

11. Sous **Sélectionner une page**, cliquez sur la page de **mappage utilisateur** pour la sélectionner. Sous **utilisateurs mappés à cette connexion**, activez la case à cocher dans la colonne **carte** pour sélectionner la base de données App-V.

12. Sous **appartenance au rôle de base de données pour: &lt; &gt; appvdatabasename**, cliquez pour sélectionner **SFTEveryone** , puis cliquez sur **OK**.

13. Assurez-vous que le pare-feu Windows sur le nouvel ordinateur exécutant SQL Server est configuré pour permettre au serveur de gestion des applications d’accéder au système. Sous **Outils d’administration**, utilisez le programme **pare-feu Windows avec Advanced Security** pour créer une **règle de trafic entrant** pour le port utilisé par SQL Server (par défaut, le port 1433).

**Pour migrer les tâches de l’agent App-V SQL Server**

1.  Sur l’ordinateur d’origine exécutant SQL Server, dans SQL Server Management Studio, développez le nœud de l' **agent SQL Server** , puis développez le nœud **Jobs** .

2.  Cliquez avec le bouton droit sur les quatre tâches App-V suivantes, puis sélectionnez **tâche de script en tant que | CRÉER sur | **Enregistrez chaque script dans un dossier et attribuez un nom descriptif à chaque script.

    -   **Base de données SoftGrid (appvdbname) vérifier l’historique d’utilisation**

    -   **Base de données appvdbname pour fermer les sessions orphelines**

    -   **La base de données appvdbname est limitée à la taille**

    -   **Base de données sur le moniteur de base de données (appvdbname)**

3.  Dans l’ordinateur de destination exécutant SQL Server et Open SQL Server Management Studio, copiez les quatre fichiers de script (. Sql).

4.  Dans l’Explorateur Windows, cliquez avec le bouton droit sur chaque fichier. SQL, puis cliquez sur **exécuter**. Chaque script s’ouvre dans une fenêtre de requête dans SQL Server Management Studio. Cliquez sur **exécuter** pour chaque script et vérifiez que chacun d’eux est correctement exécuté.

5.  Actualisez le nœud **tâches** sous le nœud de l' **agent SQL Server** , puis vérifiez que les quatre tâches sont correctement créées.

**Pour mettre à jour la configuration du serveur de gestion App-V**

1.  Sur le serveur de gestion App-V, modifiez les clés de Registre suivantes:

    -   **SQLServerName**  =  SqlServerName &lt; newservername&gt;

    -   **SQLServerPort**  =  SQLServerPort &lt; newserverport&gt;

    Redémarrez ensuite le service App-V Server.

2.  Recherchez le fichier SftMgmt. UDL sous le répertoire d’installation de l’application-V Management Server (la valeur par défaut est C:\\Program Files\\Microsoft System Center App Virt Management Server\\App Virt Management Service). Cliquez avec le bouton droit sur le fichier, puis sélectionnez **ouvrir**.

3.  Dans l’onglet **connexion** , entrez le nom de l’ordinateur de destination exécutant SQL Server, puis cliquez sur **tester la connexion**. Une fois le test terminé, cliquez sur **OK** , puis de nouveau sur **OK** .

4.  Pour les versions Server App-V de gestion antérieures à 4,5 SP2, vous devez mettre à jour les paramètres de journalisation SQL. Sous **groupes de serveurs**, cliquez avec le bouton droit sur le groupe de serveurs dont le serveur est membre, puis sélectionnez **Propriétés**.

5.  Dans l’onglet **journalisation** , cliquez sur l’entrée **de la base de données SQL** pour la sélectionner, puis cliquez sur **modifier**.

6.  Remplacez le **nom d’hôte DNS** par le nom d’hôte du nouvel ordinateur exécutant SQL Server, puis cliquez sur **OK**. Cliquez sur **OK** deux fois de plus, puis redémarrez le service App-V Server.

7.  Ouvrez la console de gestion App-V, cliquez avec le bouton droit sur le nœud **applications** et sélectionnez **Actualiser**. La liste des applications doit être affichée comme auparavant.

 

 





