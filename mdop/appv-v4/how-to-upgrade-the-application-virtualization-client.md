---
title: Procédure pour mettre à niveau Application Virtualization Client
description: Procédure pour mettre à niveau Application Virtualization Client
author: dansimp
ms.assetid: 2a75d8b5-da88-456c-85bb-f5bd3d470f7f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b9748fbdba7c8d2777a06c93295e4582be784dd1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806713"
---
# Procédure pour mettre à niveau Application Virtualization Client


Vous pouvez utiliser les procédures suivantes pour mettre à niveau le client de bureau App-V) ou le client App-V pour les services Bureau à distance (auparavant services Terminal Server). Pour effectuer une mise à niveau du client, installez une nouvelle version sur la version antérieure déjà installée. Lorsque vous procédez à la mise à niveau des clients, le logiciel d’installation conserve automatiquement et migre les paramètres de l’utilisateur pour les applications virtuelles. Des droits d’administration sont nécessaires pour exécuter le programme d’installation.

**Remarques**  Lors de la mise à niveau vers Application Virtualization (App-V) 4.5 ou versions ultérieures, les autorisations d’accès à la clé de Registre HKCU sont modifiées. Pour cette raison, les utilisateurs perdent des configurations utilisateur qui ont été définies auparavant, par exemple, des paramètres du mode déconnecté configurés par l’utilisateur. Si l’utilisateur n’est pas activement empêché de configurer le comportement de l’interface utilisateur du client par le biais d’un verrouillage des autorisations, l’utilisateur peut réinitialiser ces préférences après une actualisation de publication.

 

**Important**  Lorsque vous procédez à la mise à niveau vers la version 4.6 ou une version ultérieure du client App-V, vous devez utiliser le programme d’installation approprié pour le système d’exploitation de l’ordinateur, 32-bits ou 64 bits. L’installation échoue et un message d’erreur s’affiche si vous utilisez le mauvais programme d’installation.

 

**Pour mettre à niveau le client de bureau de virtualisation des applications**

1.  Fermez toutes les applications virtuelles, cliquez avec le bouton droit sur l’icône du client de bureau App-V affichée dans la zone de notification du bureau Windows, puis sélectionnez **quitter** pour arrêter le client existant.

2.  Lorsque vous avez obtenu le fichier d’archive du programme d’installation approprié et que vous l’avez enregistré sur votre ordinateur, double-cliquez dessus pour développer l’archive.

3.  Recherchez le fichier setup.exe, puis double-cliquez sur setup.exe pour démarrer l’installation.

4.  L’Assistant vérifie le système pour s’assurer que tous les logiciels requis sont installés et vous invite à installer l’une des opérations suivantes, le cas échéant:

    -   Package redistribuable Microsoft VisualC + + 2005SP1 (x86)

    -   Microsoft Core XML Services (MSXML) 6.0 SP1 (x86)

    -   Rapport d’erreurs d’application Microsoft

    **Remarques**  Pour la version 4.6 ou une version ultérieure, l’Assistant installe également la configuration logicielle requise suivante:

    -   Package redistribuable Microsoft VisualC + + 2008SP1 (x86)

     

5.  Cliquez sur **Installer**. La progression de l’installation s’affiche, et l’état passe de **en attente** à **l’installation**. L' **État d’installation passe à succès dès** que chaque étape est terminée.

6.  Lorsque la boîte de dialogue **client de bureau de virtualisation des applications** apparaît et affiche un message indiquant qu’une version plus ancienne du client est disponible sur l’ordinateur, cliquez sur en **regard** de mettre à niveau vers la nouvelle version.

7.  Lorsque l’écran du **contrat de licence** s’affiche, lisez le contrat de licence et, si vous êtes d’accord, cliquez sur **J’accepte les conditions du contrat de licence**, puis cliquez sur **suivant**.

8.  Lorsque l’Assistant InstallShield affiche la boîte **de dialogue préparer la mise à niveau de l’application** , cliquez sur **mettre** à niveau pour commencer la mise à niveau. L’écran suivant indique que le client est en cours d’installation.

    **Avertissement**  Si vous n’avez pas arrêté le programme client à l’étape 1, un message d’avertissement relatif **à l’utilisation du fichier** s’affiche. Si tel est le cas, cliquez avec le bouton droit sur l’icône du client App-V affichée dans la zone de notification du bureau et sélectionnez **quitter** pour arrêter le client existant. Cliquez ensuite sur **Réessayer** pour continuer.

     

9.  Lorsque l’installation est terminée, vous êtes invité à redémarrer votre ordinateur. Vous devez redémarrer l’ordinateur pour terminer l’installation.

    **Attention**  Si la mise à niveau échoue pour une raison quelconque, vous devez redémarrer votre ordinateur avant de réessayer la mise à niveau.

     

**Pour mettre à niveau le client de virtualisation des applications à l’aide de la ligne de commande**

1.  Si vous procédez à la mise à niveau du client App-V à l’aide du programme setup.msi, assurez-vous que tous les logiciels requis requis sont installés.

    **Important**  
    -   Pour la version 4.6 et une version ultérieure du client App-V, le programme de setup.msi vérifie le système et ne fonctionne pas avec un message d’erreur indiquant que l’installation ne peut pas continuer si le logiciel requis n’est pas installé.

    -   Pour App-V version 4.6, les paramètres de ligne de commande ne peuvent pas être utilisés lors d’une mise à niveau et seront ignorés.

     

2.  L’exemple de ligne de commande suivant utilise le fichier setup.msi pour mettre à niveau le client App-V. Vous devez utiliser le programme d’installation client approprié, selon que vous effectuez une mise à niveau du client de bureau App-V ou du client App-V pour les services Bureau à distance (anciennement services Terminal Server).

    **msiexec.exe/i "setup.msi"**

    **Important**  Les guillemets sont requis uniquement lorsque la valeur contient un espace. Par souci de cohérence, toutes les instances de l’exemple précédent sont indiquées par des guillemets.

     

**Pour mettre à niveau le client de virtualisation des applications pour les services Bureau à distance**

1.  Suivez les stratégies standard de votre organisation relatives à l’installation ou à la mise à niveau d’applications sur le serveur hôte de session Bureau à distance. Si le système fait partie d’une batterie de serveurs, supprimez l’hôte RDSession de la batterie de serveurs.

2.  Pour mettre à niveau le client App-V pour les services Bureau à distance (auparavant services Terminal Server), vous devez utiliser la ligne de commande car vous ne pouvez pas mettre à niveau le client manuellement sur l’hôte RDSession.

    **Remarques**  Dans l’App-V version 4,6 et les versions ultérieures, en plus de l’utilisation de la ligne de commande pour mettre à niveau le client, vous pouvez également utiliser une session de bureau à distance. Aucun paramètre spécial n’est requis pour démarrer la session Bureau à distance.

     

3.  Après l’exécution de la mise à niveau du client pour les services Bureau à distance, redémarrez et connectez-vous à l’hôte RDSession.

4.  Après le redémarrage du système, ajoutez le serveur à la batterie de serveurs.

    **Attention**  Si la mise à niveau échoue pour une raison quelconque, vous devez redémarrer votre ordinateur avant de réessayer la mise à niveau.

     

## Rubriques connexes


[Aspects à prendre en compte pour le déploiement et la mise à niveau d'Application Virtualization](application-virtualization-deployment-and-upgrade-considerations.md)

 

 





