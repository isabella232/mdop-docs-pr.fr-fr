---
title: Procédure pour installer le serveur Application Virtualization Management Server
description: Procédure pour installer le serveur Application Virtualization Management Server
author: dansimp
ms.assetid: 8184be79-8c27-4328-a3c1-183791b5556c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dfd06ee1d2448990d5a740f3d59b0e5e4b45be4d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807077"
---
# Procédure pour installer le serveur Application Virtualization Management Server


Le serveur de gestion de la virtualisation des applications publie ses applications sur les clients. Dans un environnement qui est équilibré, il s’agit généralement de déploiements volumineux, tous les serveurs d’un groupe de serveurs doivent diffuser les mêmes applications. Si les serveurs de gestion d’applications de la virtualisation doivent publier différentes applications, affectez-les à différents groupes de serveurs. Dans ce cas, il se peut que vous deviez augmenter la capacité d’un groupe de serveurs.

Si vous avez désigné un ordinateur cible sur le réseau et qu’un compte de connexion possède des privilèges d’administrateur local, vous pouvez utiliser la procédure suivante pour installer le serveur de gestion des applications et l’affecter au groupe de serveurs approprié.

**Remarque**  
L’Assistant installation peut créer un enregistrement de groupe de serveurs, s’il n’en existe pas, ainsi qu’un enregistrement de l’appartenance du serveur de gestion des applications à ce groupe.



Lorsque vous avez terminé le processus d’installation, redémarrez le serveur.

**Pour installer un serveur de gestion des applications virtuelles**

1.  Vérifiez et, si nécessaire, désinstallez les versions précédentes du serveur de gestion des applications qui sont installées sur l’ordinateur cible.

2.  Pour ouvrir l’Assistant **installation de Microsoft Application Virtualization Server** , accédez à l’emplacement du système de virtualisation des applications **setup.exe** programme sur le réseau, exécutez ce programme à partir du réseau ou copiez son annuaire vers l’ordinateur cible, puis double-cliquez sur le fichier **Setup.exe** .

3.  Dans la page **Bienvenue** , cliquez sur **suivant**.

4.  Sur la page **contrat de licence** , lisez le contrat de licence et acceptez le contrat de licence, puis sélectionnez **J’accepte les termes du**contrat de licence. Cliquez sur **Suivant**.

5.  Dans la page **informations d’inscription** , vous devez entrer le nom d’utilisateur et l' **organisation**. Cliquez sur **Suivant**.

6.  Dans la page **type d’installation** , sélectionnez **personnalisée**. Cliquez sur **Suivant**. Dans la page **configuration personnalisée** , désélectionnez tous les composants du système de virtualisation des applications, à l’exception du **serveur de virtualisation des applications**, puis cliquez sur **suivant**.

    **Vigilance**  
    Si un composant est déjà installé sur l’ordinateur, lorsque vous le désactivez dans la fenêtre **configuration personnalisée** , le composant est automatiquement désinstallé.



7.  Dans la page **de la base de données de configuration** , sélectionnez un serveur de base de données dans la liste des serveurs disponibles ou ajoutez un serveur en sélectionnant **utiliser le nom d’hôte suivant** et en spécifiant les données du **nom de serveur** et du numéro de **port** . Cliquez sur **Suivant**.

    **Remarque**  
    Le serveur de gestion des applications virtuelles ne prend pas en charge le code SQL sensible à la casse.



~~~
If a database is available, click the radio button, select the database from the list, and then click **Next**. Setup will upgrade it to this newer version. If the name does not appear in the list, enter the name in the space provided.

**Note**  
When naming a server, do not use the backslash character (/) in the server name.

If you need to install a database, see [How to Install a Database](how-to-install-a-database.md). If you would like to create a new database for this version, select **Create a new database** and specify the name that will be assigned to the new database. You can also specify a new location for the database by selecting the check box and entering the path.
~~~



8. Sur la page **mode de sécurité de connexion** , sélectionnez le certificat de votre choix dans la liste déroulante. Cliquez sur **Suivant**.

   **Remarque**  
   Le paramètre **mode de connexion sécurisée** exige que le serveur ait configuré un certificat de serveur à partir d’une infrastructure à clé publique. Si un certificat de serveur n’est pas installé sur le serveur, cette option n’est pas disponible et ne peut pas être sélectionnée. Vous devez accorder au compte de service réseau l’accès en lecture au certificat utilisé.



9. Dans la page **configuration de port TCP** , pour utiliser le port par défaut (554), sélectionnez **utiliser le port par défaut (554)**. Pour spécifier un port personnalisé, sélectionnez **utiliser un port personnalisé** et spécifiez le numéro de port qui sera utilisé. Cliquez sur **Suivant**.

   **Remarque**  
   Lorsque vous installez le serveur dans un environnement non sécurisé, vous pouvez utiliser le port par défaut (554) ou vous pouvez définir un port personnalisé.



10. Sur la page **groupe d’administrateurs** , spécifiez le nom du groupe de sécurité autorisé à gérer ce serveur dans nom du **groupe**. Cliquez sur **Suivant**. Confirmez le groupe spécifié, puis cliquez sur **suivant**.

11. Sur la page **groupe de fournisseurs par défaut** , spécifiez le nom du groupe de fournisseurs par défaut, puis cliquez sur **suivant**.

12. Dans la page **chemin d’accès au contenu** , spécifiez l’emplacement de l’ordinateur cible sur lequel les fichiers SFT seront enregistrés, puis cliquez sur **suivant**.

   **Remarque**  
   Si le port HTTP ou RTSP du serveur de gestion est déjà attribué, vous êtes invité à choisir un nouveau port. Sélectionnez le port de votre choix, puis cliquez sur **suivant**.



13. Dans la page **êtes-vous prêt à installer le programme** , cliquez sur **installer**pour installer le serveur de gestion des applications virtuelles.

   **Remarque**  
   Si l’erreur 25120 s’affiche lorsque vous essayez d’effectuer cette étape, vous devez activer **les scripts et les outils de gestion**IIS. Pour activer cette fonctionnalité Windows, ouvrez le panneau **de configuration programmes et fonctionnalités** , sélectionnez **activer ou désactiver des fonctionnalités Windows**, puis accédez à **Internet Information Services.**

   Dans les **outils de gestion Web**, activez **les scripts et les outils de gestion IIS**.



14. Dans l’écran de l' **Assistant installation terminé** , cliquez sur **Terminer**pour fermer l’Assistant.

   **Important**  
   Le processus d’installation peut prendre quelques minutes. Un message de statut clignote au-dessus de la zone de notification du bureau Windows, indiquant que l’installation a réussi.

   Le redémarrage de l’ordinateur n’est pas nécessaire lorsque vous y êtes invité. Toutefois, pour optimiser les performances du système, il est recommandé de redémarrer.



## Rubriques connexes


[Procédure pour installer les serveurs et les composants système](how-to-install-the-servers-and-system-components.md)









