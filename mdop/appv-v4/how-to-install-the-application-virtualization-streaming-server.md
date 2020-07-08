---
title: Procédure pour installer le serveur Application Virtualization Streaming Server
description: Procédure pour installer le serveur Application Virtualization Streaming Server
author: dansimp
ms.assetid: a3065257-fb5a-4d92-98f8-7ef996c61db9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c4e4f8421ef1c0e60a7df92d41be98a5d2bc0132
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807062"
---
# Procédure pour installer le serveur Application Virtualization Streaming Server


Le serveur de diffusion en continu d’applications publie ses applications sur les clients. Dans un environnement qui est équilibré, il s’agit généralement de déploiements volumineux, tous les serveurs d’un groupe de serveurs doivent diffuser les mêmes applications. Si les serveurs de diffusion en continu de la virtualisation des applications doivent diffuser différentes applications, affectez-les à différents groupes de serveurs. Dans ce cas, vous devrez peut-être également augmenter la capacité d’un groupe de serveurs.

Si vous avez désigné un ordinateur cible sur le réseau et qu’un compte d’ouverture de session possède des privilèges d’administrateur local, vous pouvez utiliser la procédure suivante pour installer le serveur de diffusion en continu de l’application et l’affecter au groupe de serveurs approprié.

**Remarques**  L’Assistant installation peut créer un enregistrement de groupe de serveurs, s’il n’en existe pas, et un enregistrement du serveur de diffusion en continu d’applications de ce groupe.

 

Lorsque vous avez terminé le processus d’installation, redémarrez le serveur.

**Pour installer un serveur de streaming de la virtualisation des applications**

1.  Vérifiez qu’aucune version antérieure du serveur de diffusion en continu d’applications n’est installée sur l’ordinateur cible.

    **Important**  Assurez-vous que le serveur de gestion de l’application-V n’est pas installé sur cet ordinateur. Les deux produits ne peuvent pas être installés sur le même ordinateur.

     

2.  Naviguez jusqu’à l’emplacement du programme d’installation du système de virtualisation des applications sur le réseau, exécutez ce programme à partir du réseau ou copiez son annuaire vers l’ordinateur cible, puis double-cliquez sur le fichier **Setup.exe** .

3.  Dans la page **Bienvenue** , cliquez sur **suivant**.

4.  Dans la page **contrat de licence** , pour accepter les termes du contrat de licence, cliquez sur **J’accepte les conditions générales du**contrat de licence, puis cliquez sur **suivant**.

5.  Dans la page informations sur le **client** , spécifiez le **nom d’utilisateur** et l’organisation, puis cliquez sur **suivant**.

6.  Dans la page **chemin d’installation** , cliquez sur **Parcourir**, spécifiez l’emplacement où vous voulez installer le serveur de diffusion en continu, puis cliquez sur **suivant**.

7.  Sur la page **mode de sécurité de connexion** , sélectionnez le certificat de votre choix dans la liste déroulante, puis cliquez sur **suivant**.

    **Remarques**  Le paramètre **mode de connexion sécurisée** exige que le serveur ait configuré un certificat de serveur à partir d’une infrastructure à clé publique. Si un certificat de serveur n’est pas installé sur le serveur, cette option n’est pas disponible et ne peut pas être sélectionnée. Vous devez accorder au compte de service réseau l’accès en lecture au certificat utilisé.

     

8.  Dans la page **configuration de port TCP** , pour utiliser le port standard (554), sélectionnez **utiliser le port par défaut (554)**. Pour spécifier un port personnalisé, sélectionnez **utiliser un port personnalisé**, spécifiez le numéro de port dans le champ prévu à cet effet, puis cliquez sur **suivant**.

    **Remarques**  Lorsque vous installez le serveur dans un scénario non sécurisé, vous pouvez utiliser le port par défaut (554), ou vous pouvez définir un port personnalisé.

     

9.  Dans la page **racine du contenu** , spécifiez l’emplacement de l’ordinateur cible sur lequel les fichiers SFT seront enregistrés, puis cliquez sur **suivant**.

    **Remarques**  Si le port HTTP ou RTSP pour le serveur de streaming d’application virtuel est déjà attribué, vous serez invité à sélectionner un nouveau port. Spécifiez le port de votre choix, puis cliquez sur **suivant**.

     

10. Dans l’écran **Paramètres avancés** , entrez les informations suivantes:

    1.  **Nombre maximal de connexions client**

    2.  **Délai de connexion (s)**

    3.  **Taille du pool de threads RTSP**

    4.  **Délai d’expiration RTSP (sec)**

    5.  **Nombre de processus principaux**

    6.  **Délai d’expiration principal (s)**

    7.  **Activer l’authentification des utilisateurs**

    8.  **Activer l’autorisation de l’utilisateur**

    9.  **Taille des blocs de cache (Ko)**

    10. **Taille maximale du cache (Mo)**

    **Remarques**  Le serveur de streaming App-V utilise les autorisations du système de fichiers NTFS pour contrôler l’accès aux applications sous le partage de contenu. Utiliser **activer l’authentification utilisateur** et **activer l’autorisation** de l’utilisateur pour contrôler si le serveur vérifie et applique les listes de contrôle d’accès (ACL) ou non.

     

11. Dans la page **êtes-vous prêt à installer le programme** , cliquez sur **installer**pour lancer l’installation.

12. Dans l’écran de l' **Assistant installation terminé** , cliquez sur **Terminer**pour fermer l’Assistant.

    **Important**  Le processus d’installation peut prendre quelques minutes. Un message de statut clignote au-dessus de la zone de notification du bureau Windows, indiquant que l’installation a réussi.

    Il n’est pas nécessaire de redémarrer votre ordinateur lorsque vous y êtes invité. Toutefois, pour optimiser les performances du système, nous vous conseillons de redémarrer.

     

13. Répétez les étapes 1 à 12 pour chaque serveur d’application virtuel que vous devez installer.

## Rubriques connexes


[Procédure pour installer les serveurs et les composants système](how-to-install-the-servers-and-system-components.md)

 

 





