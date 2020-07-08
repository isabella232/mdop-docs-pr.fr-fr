---
title: Procédure d'utilisation de l'Assistant Image de récupération DaRT pour créer l'image de récupération
description: Procédure d'utilisation de l'Assistant Image de récupération DaRT pour créer l'image de récupération
author: dansimp
ms.assetid: 1b8ef983-fff9-4d75-a2f6-53120c5c00c9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 49253a8c0bf9c9073b57712acc773e4a57e31d72
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809647"
---
# Procédure d'utilisation de l'Assistant Image de récupération DaRT pour créer l'image de récupération


Microsoft Diagnostics and Recovery Tools (DaRT) 7 inclut l' **Assistant image de récupération DART** utilisé dans Windows pour créer une image ISO (International Organization for Standardization) amorçable. Une image ISO est un fichier qui représente le contenu brut d’un CD.

L' **Assistant image de récupération DART** nécessite les informations suivantes:

-   **Image de démarrage**° ° vous devez fournir le chemin d’accès d’un DVD Windows 7 ou de fichiers sources Windows 7 requis pour créer l’image de récupération Dart.

-   **Sélection d’outil**n ° ° vous pouvez sélectionner les outils à inclure dans l’image de récupération Dart.

-   **Connexions distantes**n ° vous pouvez indiquer si vous souhaitez que l’image de récupération DART inclue la possibilité d’établir une connexion à distance entre le support technique et l’ordinateur de l’utilisateur final.

-   **Outils de débogage pour Windows**n ° vous êtes invité à fournir l’emplacement des outils de débogage pour Windows.

-   **Définitions pour le nettoyeur de systèmes autonome**n ° vous pouvez déterminer si vous souhaitez télécharger les dernières définitions au moment où vous créez l’image de récupération ou téléchargez les définitions ultérieurement.

-   Les **pilotes**° ° vous demandent si vous souhaitez ajouter des pilotes à l’image ISO.

-   **Fichiers supplémentaires**° ° vous pouvez ajouter des fichiers à l’image ISO qui peut vous aider à diagnostiquer des problèmes.

-   **Emplacement de l’image ISO**° ° vous êtes invité à spécifier l’emplacement de l’image ISO.

-   **Lecteur de CD-DVD**° ° vous êtes invité à indiquer si le CD ou le lecteur DVD doit être utilisé pour graver le CD ou DVD.

**Remarques**  La taille de l’image ISO peut varier en fonction des outils sélectionnés dans l' **Assistant image de récupération DART**.

 

## Pour créer l’image de récupération à l’aide de l’Assistant image de récupération DaRT


Suivez ces instructions pour utiliser l' **Assistant image de récupération DART** pour créer l’image de récupération Dart.

### Pour sélectionner les outils à inclure dans l’image de récupération DaRT

L' **Assistant image de récupération DART** présente une boîte de dialogue de **sélection d’outil** . Vous pouvez sélectionner ou supprimer des outils dans la liste d’outils à inclure dans l’image de récupération DaRT en mettant en surbrillance un outil, puis en cliquant sur les boutons **activer** ou **Désactiver** .

Lorsque vous avez sélectionné tous les outils que vous voulez inclure dans l’image de récupération, cliquez sur **suivant**.

### Pour ajouter l’option autorisant la connectivité à distance

Vous pouvez activer la case à cocher **autoriser les connexions à distance** pour proposer l’option dans la fenêtre du **jeu d’outils de diagnostics et de récupération** pour établir une connexion à distance entre l’agent de support technique et un ordinateur d’utilisateur final. Après avoir établi une connexion à distance, un agent de support technique peut exécuter les outils DaRT sur l’ordinateur de l’utilisateur final à partir d’un emplacement distant.

Vous pouvez activer la case à cocher **spécifier le numéro de port** pour entrer un numéro de port spécifique qui sera utilisé lors de l’établissement d’une connexion à distance. Vous pouvez spécifier un numéro de port compris entre 1 et 65535. Nous vous recommandons d’utiliser le numéro de port 1024 ou une version ultérieure pour réduire l’éventualité d’un conflit.

Vous pouvez également créer un message personnalisé qui sera reçu par un utilisateur final lors de l’établissement d’une connexion à distance. Le message peut contenir jusqu’à 2048 caractères.

Pour plus d’informations sur l’utilisation à distance des outils DaRT, voir récupération [d’ordinateurs distants à l’aide de l’image de récupération DART](how-to-recover-remote-computers-using-the-dart-recovery-image-dart-7.md).

### Pour ajouter les outils de débogage pour Windows à l’image de récupération DaRT

Dans la boîte de dialogue **analyse crash** de l' **Assistant image de récupération DART**, vous êtes invité à spécifier l’emplacement des outils de débogage pour Windows. Si vous n’avez pas de copie des outils, vous pouvez les télécharger à partir de Microsoft. Le lien suivant pour accéder à la page de téléchargement est fourni dans l’Assistant: [Télécharger et installer les outils de débogage pour Windows](https://go.microsoft.com/fwlink/?LinkId=99934).

Vous pouvez spécifier l’emplacement des outils de débogage sur l’ordinateur sur lequel vous exécutez l' **Assistant image de récupération DART**ou vous pouvez choisir d’utiliser les outils présents sur l’ordinateur de destination. Si vous décidez d’utiliser une copie sur un autre ordinateur, vous devez vous assurer que les outils sont installés sur chaque ordinateur sur lequel vous diagnostiquez un blocage.

**Remarques**  Si vous incluez l' **analyseur d’incident** dans l’image ISO, nous vous recommandons d’inclure également les outils de débogage pour Windows.

 

Pour ajouter les outils de débogage pour Windows, procédez comme suit:

1.  Facultatif Cliquez sur le lien hypertexte pour télécharger les outils de débogage pour Windows.

2.  Sélectionnez l’une des options suivantes:

    -   **Utilisez les outils de débogage pour Windows à l’emplacement suivant**. Si vous sélectionnez cette option, vous pouvez accéder à l’emplacement des outils.

    -   **Recherchez les outils de débogage pour Windows sur le système que vous réparez**. Si vous sélectionnez cette option, l' **analyseur d’incident** ne fonctionnera pas si les outils de débogage pour Windows ne se trouvent pas sur le problème de l’ordinateur.

3.  Lorsque vous avez terminé, cliquez sur **suivant**.

### Pour ajouter les définitions du nettoyeur système autonome à l’image de récupération DaRT

Les définitions constituent un référentiel de logiciels malveillants connus et d’autres logiciels potentiellement indésirables. Dans la mesure où un logiciel malveillant est en **cours de développement, il** repose sur les définitions actuelles pour déterminer si un logiciel qui tente d’installer, d’exécuter ou de modifier des paramètres sur un ordinateur est potentiellement indésirable ou malveillant.

Pour inclure les dernières définitions dans l’image de récupération DaRT (recommandé), cliquez sur **Oui, puis téléchargez les dernières définitions.** La mise à jour des définitions démarre automatiquement. Vous devez être connecté à Internet pour terminer ce processus.

Pour ignorer la mise à jour de définition, cliquez sur **non, télécharger manuellement les définitions plus tard**. Les définitions ne seront pas incluses dans l’image de récupération DaRT.

Si vous décidez de ne pas inclure les dernières définitions sur l’image de récupération, ou si les définitions incluses dans l’image de récupération ne sont plus actuelles lorsque vous êtes prêt à utiliser un **nettoyeur système autonome**, vous pouvez obtenir les dernières définitions avant de commencer une analyse en suivant les instructions fournies dans la version **autonome du système**.

**Important**  Vous ne pouvez pas numériser s’il n’y a pas de définition.

 

Lorsque vous avez terminé, cliquez sur **suivant**.

### Pour ajouter des pilotes à l’image de récupération DaRT

**Attention**  Par défaut, lorsque vous ajoutez un pilote à l’image de récupération DaRT, tous les fichiers et sous-dossiers situés dans ce dossier sont ajoutés à l’image de récupération. Pour plus d’informations, reportez-vous à la rubrique [résolution des problèmes DaRT 7,0](troubleshooting-dart-70-new-ia.md).

 

Vous devez inclure des pilotes supplémentaires sur l’image de récupération pour DaRT7 que vous avez peut-être besoin lors de la réparation d’un ordinateur. En règle générale, ces contrôleurs de réseau ou de stockage ne sont pas inclus sur le DVD Windows.

**Important**  Lorsque vous sélectionnez les pilotes à inclure, sachez que la connectivité sans fil (par exemple, Bluetooth ou 802.11 a/b/g/n) n’est pas prise en charge dans DaRT.

 

**Pour ajouter un pilote de stockage ou de contrôleur de réseau à l’image de récupération**

1.  Dans la boîte de dialogue **pilotes supplémentaires** de l' **Assistant image de récupération DART**, cliquez sur **Ajouter un périphérique**.

2.  Recherchez le fichier à ajouter pour le pilote, puis cliquez sur **ouvrir**.

    **Remarques**  Le fichier de **pilote** est fourni par le fabricant du contrôleur de stockage ou de réseau.

     

3.  Répétez les étapes 1 et 2 pour chaque pilote que vous souhaitez inclure.

4.  Lorsque vous avez terminé, cliquez sur **suivant**.

### Pour ajouter des fichiers à l’image de récupération DaRT

Suivez ces étapes pour ajouter des fichiers à l’image de récupération afin de pouvoir les utiliser pour diagnostiquer des problèmes d’ordinateur.

1.  Dans la boîte de dialogue **fichiers supplémentaires** de l' **Assistant image de récupération DART**, cliquez sur **afficher les fichiers**. Une fenêtre de l’Explorateur s’ouvre et affiche le dossier contenant les fichiers partagés.

2.  Créez un sous-dossier dans le dossier qui est répertorié dans la boîte de dialogue.

3.  Copiez les fichiers que vous souhaitez inclure dans le nouveau sous-dossier.

4.  Lorsque vous avez terminé, cliquez sur **suivant.**

### Pour sélectionner l’emplacement de la feuille de style ISO qui contient l’image de récupération DaRT

Suivez ces étapes pour spécifier l’emplacement de création de l’image ISO:

1.  Dans la boîte de dialogue **créer une image de démarrage** de l' **Assistant image de récupération DART**, cliquez sur **Parcourir**.

2.  Naviguez jusqu’à l’emplacement préféré dans la fenêtre **Enregistrer sous** , puis cliquez sur **Enregistrer**.

3.  Lorsque vous avez terminé, cliquez sur **suivant**.

La taille de l’image ISO peut varier en fonction des outils sélectionnés et des fichiers que vous ajoutez dans l’Assistant.

L’Assistant nécessite que l’image ISO ait une extension de nom de fichier **. ISO** , car la plupart des programmes permettant de graver un CD ou un DVD nécessitent cette extension. Si vous ne spécifiez pas un autre emplacement, l’image ISO est créée sur votre ordinateur de bureau portant le nom **DaRT70. ISO**.

### Pour graver l’image de récupération sur un CD ou un DVD

Si l' **Assistant image de récupération de DART** détecte un lecteur CD-RW compatible sur votre ordinateur, il propose de graver l’image ISO sur un disque. Si vous voulez graver un CD ou un DVD et que l’Assistant ne reconnaît pas votre lecteur, vous devez utiliser un autre programme, tel que le programme fourni avec votre lecteur. Vous pouvez utiliser un dupliquateur, un service de duplication ou un logiciel de gravure de DVD ou de DVD pour apporter d’autres copies.

1.  Dans la boîte de dialogue **graver un CD ou un DVD enregistrable** de l' **Assistant image de récupération de DART**, sélectionnez **graver l’image sur le lecteur de CD/DVD enregistrable suivant**.

2.  Sélectionnez le lecteur de CD ou DVD.

    **Remarques**  Si un lecteur n’est pas reconnu et que vous installez un nouveau lecteur, vous pouvez cliquer sur **Actualiser la liste** des lecteurs pour obliger l’Assistant à mettre à jour la liste des lecteurs disponibles.

     

3.  Cliquez sur **Suivant**.

## Rubriques connexes


[Création de l'image de récupération DaRT7.0](creating-the-dart-70-recovery-image-dart-7.md)

 

 





