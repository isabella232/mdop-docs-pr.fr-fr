---
title: Procédure pour installer manuellement Application Virtualization Client
description: Procédure pour installer manuellement Application Virtualization Client
author: dansimp
ms.assetid: bb67f70b-d525-4317-b254-e4f084c717ab
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 0cb41b5e51bd33c377b17c088e97cb54f1a57685
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806965"
---
# Procédure pour installer manuellement Application Virtualization Client

Il existe deux types de composants clients de la virtualisation des applications: le client de bureau Virtualization, qui est conçu pour une installation sur les ordinateurs de bureau et le client de virtualisation des applications pour les services Bureau à distance (anciennement services Terminal Server), que vous pouvez installer sur les serveurs de l’hôte de session Bureau à distance. Même si les deux programmes du programme d’installation du client sont différents, vous pouvez utiliser la procédure suivante pour installer manuellement le client de bureau virtuel d’application sur un ordinateur de bureau unique ou le client de virtualisation des applications pour les services Bureau à distance sur un seul serveur hôte de session Bureau à distance. Dans un environnement de production, il est très probable d’installer le client de bureau Virtualization d’applications sur plusieurs ordinateurs de bureau avec un processus d’installation par script automatisé. Pour plus d’informations sur l’installation de plusieurs clients à l’aide d’un processus d’installation par script, voir [Comment installer le client à l’aide de la ligne de commande](how-to-install-the-client-by-using-the-command-line-new.md).

**Remarque**  
1. Si vous installez le client de virtualisation d’application pour le logiciel de services Bureau à distance sur un serveur hôte de session Bureau à distance, invitez les utilisateurs qui ont une session de client RDP ou ICA ouverte auprès du serveur hôte de session Bureau à distance qu’ils doivent enregistrer leur travail et fermer leurs sessions. Dans une session de bureau à distance, vous pouvez installer le client manuellement. Pour plus d’informations sur la mise à niveau du client, voir [Comment mettre à niveau le client de virtualisation d’applications](how-to-upgrade-the-application-virtualization-client.md).

2. Si vous avez une configuration sur l’ordinateur de l’utilisateur qui dépend du chemin d’installation du client, Notez que le client de virtualisation des applications (App-V) 4,5 utilise un autre dossier d’installation que les versions précédentes. Par défaut, une nouvelle installation du client 4,5 de virtualisation des applications (App-V) est installée dans le dossier du client de virtualisation de l’application C:\\Program Files\\Microsoft. Si une version antérieure du client est déjà installée, l’installation du client App-V effectue une mise à niveau vers le dossier d’installation existant.

**Remarque**  
Pour App-V version 4,6 et ultérieure, lors de l’installation du client App-V, SFTLDR.DLL est installé dans le répertoire Windows\\system32. Si le client App-V est installé sur un système 64 bits, SFTLDR\_WOW64.DLL est installé dans le répertoire Windows\\SysWOW64.

**Pour installer manuellement le client de bureau de virtualisation des applications**

1. Lorsque vous avez obtenu le fichier d’archive du programme d’installation approprié et que vous l’avez enregistré sur votre ordinateur, vérifiez que vous êtes connecté avec un compte disposant de droits d’administrateur sur l’ordinateur, puis double-cliquez sur le fichier pour développer l’archive.

2. Choisissez le dossier dans lequel vous voulez enregistrer les fichiers, puis ouvrez le dossier une fois que les fichiers y ont été copiés.

3. Consultez les notes de publication, le cas échéant.

4. Recherchez le fichier setup.exe, puis double-cliquez sur setup.exe pour démarrer l’installation.

5. L’Assistant vérifie le système pour s’assurer que tous les logiciels requis sont installés et si l’une des conditions suivantes est manquante, l’Assistant vous invite automatiquement à les installer:

    - Package redistribuable Microsoft Visual C++ 2005 SP1 (x86)

    - Services Microsoft Core XML Services (MSXML) 6,0 SP1 (x86)

    - Rapport d’erreurs d’application Microsoft

    **Remarque**  
    Pour App-version 4,6 et les versions ultérieures, l’Assistant peut également installer le package redistribuable Microsoft Visual C++ 2008 SP1 (x86).

    Pour plus d’informations sur l’installation de Microsoft Visual C++ 2008 SP1 Redistributable Package (x86), voir [https://go.microsoft.com/fwlink/?LinkId=150700](https://go.microsoft.com/fwlink/?LinkId=150700) .

    Si vous y êtes invité, cliquez sur **installer**. La progression de l’installation s’affiche, et l’état passe de **en attente** à **l’installation**. L' **État d’installation passe à succès dès** que chaque étape est terminée.

6. Lorsque le **client de bureau Microsoft Application Virtualization-InstallShield** est affiché, cliquez sur **suivant**.

7. L’écran **contrat de licence** s’affiche. Lisez le contrat de licence et, si vous êtes d’accord, cliquez sur **J’accepte les termes du contrat de licence** , puis cliquez sur **suivant**.

   Vous pouvez également cliquer sur le bouton pour lire la déclaration de confidentialité. Vous devez être connecté à Internet pour accéder à la déclaration sur le respect de la vie privée.

8. Dans l’écran **type d’installation** , sélectionnez le type d’installation. Cliquez sur **standard** pour utiliser les valeurs par défaut du programme ou cliquez sur **personnalisé** si vous voulez configurer les paramètres du programme lors de l’installation.

9. Si vous choisissez par **défaut**, l’écran suivant apparaît **prêt à installer le programme**. Cliquez sur **installer** pour lancer l’installation.

10. Si vous choisissez **personnalisé**, l’écran du **dossier de destination** s’affiche.

11. Dans l’écran **dossier de destination** , cliquez sur **suivant** pour accepter le dossier par défaut ou cliquez sur **modifier** pour afficher l’écran modifier le **dossier de destination actuel** . Recherchez ou dans le champ **nom du dossier** , entrez le dossier de destination, cliquez sur **OK**, puis sur **suivant**.

12. Dans l’écran **emplacement des données de virtualisation des applications** , cliquez sur **suivant** pour accepter les emplacements de données par défaut ou effectuer les actions suivantes pour modifier l’emplacement de stockage des données:

    1. Cliquez sur **modifier**, puis recherchez ou accédez au champ **emplacement global des données** , entrez le dossier de destination pour l’emplacement des données globales, puis cliquez sur **OK**. Le répertoire de données globales permet de mettre en cache les données partagées par tous les utilisateurs sur l’ordinateur, tels que les fichiers OSD et les données de fichier SFT.

    2. Si vous voulez modifier la lettre de lecteur utilisée, sélectionnez la lettre de lecteur préférée dans la liste déroulante.

    3. Entrez une nouvelle trajectoire pour stocker les données spécifiques à l’utilisateur dans le champ d' **emplacement des données spécifiques** à l’utilisateur si vous souhaitez modifier l’emplacement des données. Le répertoire de données utilisateur est l’endroit où le client de bureau de virtualisation d’application stocke les informations spécifiques à l’utilisateur, telles que les paramètres personnels pour les applications virtualisées.

       **Remarque**  
       Ce chemin d’accès ne doit pas être différent pour chaque utilisateur, il doit donc inclure une variable d’environnement spécifique à l’utilisateur ou un lecteur mappé, ou un autre qui sera résolu en chemin unique pour chaque utilisateur.

    4. Lorsque vous avez terminé d’apporter les modifications, cliquez sur **suivant**.

13. Dans l’écran **paramètres de taille de cache** , vous pouvez accepter ou changer la taille de cache par défaut. Cliquez sur l’une des cases d’option suivantes pour choisir le mode de gestion de l’espace de cache:

    1. **Utilisez la taille maximale du cache**. Entrez une valeur numérique comprise entre 100 et 1048576 (1 to) dans le champ **taille maximale (Mo)** pour spécifier la taille maximale du cache.

    2. **Utilisez le seuil d’espace disque libre**. Entrer une valeur numérique pour spécifier la quantité d’espace libre sur le disque dur, en Mo, que le client de virtualisation des applications doit laisser disponible sur le disque. Cela permet au cache d’augmenter jusqu’à ce que la quantité d’espace disque disponible atteint cette limite. La valeur figurant dans **espace libre** sur le disque indique la quantité d’espace disque utilisée actuellement.

    **Important**  
    Pour vous assurer que le cache dispose de suffisamment d’espace alloué pour tous les packages qui peuvent être déployés, utilisez le paramètre **utiliser le seuil d’espace disque libre** lorsque vous configurez le client de manière à ce que le cache puisse augmenter selon les besoins. Par ailleurs, vous pouvez déterminer à l’avance la quantité d’espace disque nécessaire pour le cache de l’application V et au moment de l’installation, définir la taille de cache en conséquence. Pour plus d’informations sur la fonctionnalité de gestion de l’espace dans le cache, voir **utilisation de la fonctionnalité de gestion de l’espace**dans le cache dans le guide des opérations de Microsoft Application Virtualization (App-V).

    Cliquez sur **Suivant** pour poursuivre.

14. Dans les sections suivantes de l’écran de configuration de la **stratégie de package d’exécution** , vous pouvez modifier les paramètres qui affectent le comportement du client de virtualisation d’application au moment de l’exécution:

    1. **Racine**de l’application. Spécifie l’emplacement des fichiers SFT. Remplace les parties protocole, serveur et port de l’URL du code base HREF dans le fichier OSD.

    2. **Autorisation**de l’application. Lorsque l' **autorisation d’accès** de l’utilisateur est activée, les utilisateurs doivent se connecter à un serveur et valider leurs informations d’identification au moins une fois pour qu’ils puissent démarrer chaque application virtuelle.

    3. **Autoriser la lecture en continu à partir du fichier**. Indique si la diffusion en continu à partir du fichier est activée, quelle que soit la façon dont le champ racine de l' **application** est utilisé. Si ce n’est pas le cas, la diffusion en continu de fichiers est désactivée. Cette case à cocher doit être activée si la **racine source** de l’application contient un chemin d’accès UNC sous la forme \\\\server\\share.

    4. **Chargez automatiquement l’application**. Détermine quand et comment le chargement automatique en arrière-plan des applications intervient.

       **Remarque**  
       Lorsque vous installez le client App-V pour une utilisation avec un cache en lecture seule, par exemple, avec une implémentation de serveur VDI, définissez **les applications à charger** automatiquement de manière à **ne pas charger automatiquement** les applications pour empêcher le client d’essayer de mettre à jour des applications dans le cache en lecture seule.

    Cliquez sur **Suivant** pour poursuivre.

15. Dans l’écran **serveur de publication** , activez la case à cocher **configurer un serveur de publication maintenant** si vous voulez définir un serveur de publication ou cliquez sur **suivant** si vous voulez le terminer ultérieurement. Pour définir un serveur de publication, spécifiez les informations suivantes:

    1. **Nom d’affichage**— entrez le nom que vous voulez afficher pour le serveur.

    2. **Type**: sélectionnez le type de serveur dans la liste déroulante des types de serveurs.

    3. **Nom d’hôte** et **port**: entrez le nom d’hôte et le port dans les champs correspondants. Lorsque vous sélectionnez un type de serveur dans la liste déroulante, le champ port se remplit automatiquement avec les numéros de port standard. Pour modifier un numéro de port, cliquez sur le type de serveur dans la liste et modifiez le numéro de port selon vos besoins.

    4. **Path**: Si vous avez sélectionné un serveur **http standard** ou un **serveur http de sécurité améliorée**, vous devez entrer le chemin complet du fichier XML contenant les données de publication dans ce champ. Si vous sélectionnez **application de virtualisation des applications** ou **serveur de virtualisation des applications de sécurité améliorée**, ce champ n’est pas actif.

    5. **Contactez automatiquement ce serveur pour mettre à jour les paramètres lorsque l’utilisateur se connecte**: activez cette case à cocher si vous voulez que ce serveur soit interrogé automatiquement lorsque les utilisateurs se connectent à leur compte sur le client de virtualisation des applications.

    6. Lorsque vous avez terminé, cliquez sur **suivant**.

16. Dans l’écran **prêt à installer le programme** , cliquez sur **installer**. Un écran affiche la progression de l’installation.

17. Dans l’écran de l' **Assistant installation terminé** , cliquez sur **Terminer**.

    **Remarque**  
    Si l’installation échoue pour une raison quelconque, vous devrez peut-être redémarrer l’ordinateur avant de réessayer d’installer.

## Rubriques connexes

[Procédure pour installer le client via la ligne de commande](how-to-install-the-client-by-using-the-command-line-new.md)

[Présentation du scénario de distribution autonome](stand-alone-delivery-scenario-overview.md)
