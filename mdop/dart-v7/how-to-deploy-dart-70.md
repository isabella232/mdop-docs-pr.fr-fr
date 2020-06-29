---
title: Procédure de déploiement de DaRT7.0
description: Procédure de déploiement de DaRT7.0
author: dansimp
ms.assetid: 30522441-40cb-4eca-99b4-dff758f5c647
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c2059b64e5f3ae7af8926bc00e5965598ede4288
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804686"
---
# Procédure de déploiement de DaRT7.0


Cette rubrique fournit des instructions sur le déploiement de Microsoft Diagnostics and Recovery Tools (DaRT) 7 dans votre environnement. La première procédure décrite dans cette rubrique part du principe que vous installez toutes les fonctionnalités sur un ordinateur d’administration. Lorsque vous devez déployer ou désinstaller DaRT sur plusieurs ordinateurs, à l’aide d’un système de distribution de logiciels électronique par exemple, il peut être plus facile d’utiliser les options d’installation de ligne de commande. Ces options sont définies dans la deuxième procédure de cette rubrique, qui fournit un exemple d’utilisation pour les options de ligne de commande disponibles.

**Important**  Avant d’installer DaRT, assurez-vous que l’ordinateur répond à la configuration minimale requise décrite dans [configurations dart 7,0 prises en charge](dart-70-supported-configurations-dart-7.md).

 

**Pour installer DaRT sur un ordinateur d’administration**

1.  Recherchez les fichiers d’installation de DaRT que vous avez reçus dans le cadre de votre téléchargement de logiciels.

2.  Double-cliquez sur le fichier d’installation DaRT qui correspond à la configuration système requise: 32-bits ou 64 bits. Le fichier d’installation de DaRT est nommé **MSDaRT70.msi**.

3.  Acceptez les termes du contrat de licence logiciel Microsoft, puis cliquez sur **suivant**.

4.  Sélectionnez le dossier de destination pour l’installation de DaRT, indiquez si le DaRT doit être installé pour tous les utilisateurs ou uniquement pour l’utilisateur actuel, puis cliquez sur **suivant**.

5.  Indiquez si l’installation doit être **normale**, **personnalisée**ou **complète**, puis cliquez sur **suivant**.

    -   Installations **typiques** les outils les plus fréquemment utilisés. Cette méthode est recommandée pour la plupart des utilisateurs.

    -   **Personnalisé** vous permet de sélectionner les outils qui sont installés et l’emplacement où ils seront installés. Cette option est recommandée pour les utilisateurs avancés, en particulier si vous installez différents outils DaRT sur différents ordinateurs du support technique.

    -   **Complète** installe tous les outils DART et nécessite le plus d’espace disque.

    Après avoir sélectionné votre mode d’installation, cliquez sur **suivant**.

6.  Pour démarrer l’installation, cliquez sur **installer**.

7.  Une fois l’installation terminée, cliquez sur **Terminer** pour quitter l’Assistant.

**Pour installer DaRT à l’invite de commandes**

1.  L’exemple suivant montre comment installer toutes les fonctionnalités de DaRT.

    ``` syntax
    msiexec /i MSDaRT70.msi ADDLOCAL=CommonFiles,MSDaRTHelp,DaRTRecoveryImage,CrashAnalyzer,RemoteViewer 
    ```

2.  L’exemple suivant montre comment installer uniquement l' **Assistant image de récupération DART**.

    ``` syntax
    msiexec /i MSDaRT70.msi ADDLOCAL=CommonFiles,MSDaRTHelp,DaRTRecoveryImage
    ```

3.  L’exemple suivant montre comment installer uniquement l’analyseur d’incidents et la visionneuse de connexion à distance DaRT.

    ``` syntax
    msiexec /i MSDaRT70.msi ADDLOCAL=CommonFiles,MSDaRTHelp,CrashAnalyzer,RemoteViewer 
    ```

4.  L’exemple suivant crée un journal d’installation pour le programme d’installation de Windows. Cela est utile pour le débogage.

    ``` syntax
    msiexec.exe /i MSDaRT70.msi /l*v log.txt 
    ```

**Remarques**  Vous pouvez ajouter/qn ou/qb aux options d’invite de commandes de l’installation de DaRT pour effectuer une installation silencieuse.

 

## Rubriques connexes


[Déploiement de DaRT7.0 sur les ordinateurs des administrateurs](deploying-dart-70-to-administrator-computers-dart-7.md)

 

 





