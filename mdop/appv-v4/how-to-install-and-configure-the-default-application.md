---
title: Procédure pour installer et configurer l'application par défaut
description: Procédure pour installer et configurer l'application par défaut
author: dansimp
ms.assetid: 5c5d5ad1-af40-4f83-8234-39e972f2c29a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1083de7a8ebf94bce0b41c0d3c3edf350a9aff38
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807078"
---
# Procédure pour installer et configurer l'application par défaut


L’application par défaut est fournie dans le cadre de l’installation et est automatiquement copiée dans le serveur de gestion Microsoft Application Virtualization (App-V) lors de l’installation. Il est utilisé pour vérifier que le serveur de gestion a été correctement installé et configuré, mais qu’il doit être publié sur le client Microsoft Application Virtualization (App-V), afin que l’utilisateur puisse y accéder.

Utilisez les procédures suivantes pour publier l’application par défaut et la diffuser en continu.

**Pour publier l’application par défaut**

1.  Ouvrez une session sur le serveur de gestion App-V à l’aide d’un compte membre du groupe d’administrateurs d’application-V spécifié lors de l’installation.

2.  Sur le serveur d’administration App-V, cliquez sur **Démarrer**, sur **Outils d’administration**, puis sur **console de gestion des applications**.

3.  Dans la console de gestion App-V, cliquez sur **actions**, puis sur **se connecter au système de virtualisation des applications**.

4.  Dans la page Configuration de la **connexion** , décochez la case **utiliser une connexion sécurisée** .

5.  Dans la zone **nom d’hôte du service Web** , tapez le nom de domaine complet (FQDN) du serveur de gestion de l’application-V, puis cliquez sur **OK**.

    **Remarques**  Vous pouvez également utiliser **localhost** pour le nom d’hôte du service Web s’il est installé sur le serveur de gestion.

     

6.  Dans la console de gestion App-V, cliquez avec le bouton droit sur le nœud du **serveur** , puis cliquez sur **Options système**.

7.  Dans l’onglet **général** , dans la zone **chemin d’accès par défaut** , entrez le chemin UNC (Universal Naming Convention) du dossier de contenu que vous avez créé sur le serveur lors de l’installation. par exemple, \ \ \ \ &lt; Server name &gt; \\Content, puis cliquez sur **OK**.

    **Important**  Utilisez le nom de domaine complet (FQDN) du nom du serveur pour permettre au client de résoudre correctement le nom.

     

8.  Dans la console de gestion App-V, dans le volet de navigation, développez le nœud **serveur** , puis cliquez sur **applications**.

9.  Dans le volet des rubriques, cliquez sur **application par défaut**, puis, dans le volet **actions** , cliquez sur **Propriétés**.

10. Dans la boîte de dialogue **Propriétés** , en regard de la zone **chemin d’accès** de l’OSD, cliquez sur **Parcourir**.

11. Dans la boîte de dialogue **ouvrir** , entrez le chemin d’accès UNC du dossier de contenu créé sur le serveur lors de l’installation. par exemple, \ \ \ \ &lt; Server name &gt; \\Content, puis appuyez sur entrée. Vous devez utiliser le nom de serveur réel et ne pouvez pas utiliser **localhost** ici.

    **Important**  Assurez-vous que les valeurs des zones **chemin d’accès** de l’OSD et **chemin d’accès** de l’icône sont au format UNC (par exemple, \ \ \ \ &lt; nom &gt; du serveur \\Content\\DefaultApp.ico), et pointez sur le dossier de contenu que vous avez créé lors de l’installation du serveur. Ne pas utiliser **localhost** ou un chemin d’accès de fichier contenant une lettre de lecteur telle que C:\\Program Files\\.. \\.. Teneur.

     

12. Sélectionnez le fichier DefaultApp. OSD, puis cliquez sur **ouvrir**.

13. Répétez les étapes précédentes pour configurer le chemin d’accès à l’icône.

14. Cliquez sur l’onglet **autorisations d’accès** , puis vérifiez que le groupe utilisateurs d’App-V dispose d’autorisations d’accès à l’application.

15. Cliquez sur l’onglet **raccourcis** , puis sur **publier sur le Bureau de l’utilisateur**. Cliquez sur **OK**.

16. Ouvrez l’Explorateur Windows et recherchez le répertoire de contenu.

17. Double-cliquez sur le fichier DefaultApp. OSD et ouvrez-le avec le bloc-notes.

18. Recherchez la ligne contenant la balise **href** et remplacez-la par le code suivant:

         `CODEBASEHREF=”RTSP://<FQDN of your server>:554/DefaultApp.sft”`

    Ou, si vous utilisez RTSP:

         `CODEBASEHREF=”RTSPS://<FQDN of your server>:322/DefaultApp.sft”`

19. Fermez le fichier DefaultApp. OSD et enregistrez les modifications.

**Pour diffuser en continu l’application par défaut**

1.  Sur l’ordinateur sur lequel est installé le client App-V, ouvrez une session en tant qu’utilisateur membre du groupe utilisateurs de virtualisation d’application spécifié lors de l’installation du serveur.

2.  Sur le bureau, le raccourci de l' **application virtualisation d’application par défaut** s’affiche. Double-cliquez sur le raccourci pour démarrer l’application.

3.  Barre d’État, affichée au-dessus de la zone de notification Windows, qui indique que l’application a démarré. Si le démarrage de l’application réussit, l’écran de titre de l’application par défaut s’affiche. Cliquez sur **OK** pour fermer la boîte de dialogue. Vous avez vérifié que le système de l’application-V s’exécute correctement.

## Rubriques connexes


[Procédure pour configurer des serveurs pour un déploiement basé sur un serveur](how-to-configure-servers-for-server-based-deployment.md)

 

 





