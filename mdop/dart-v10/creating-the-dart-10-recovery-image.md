---
title: Création de l'image de récupération DaRT10
description: Création de l'image de récupération DaRT10
author: dansimp
ms.assetid: 173556de-2f20-4ea6-9e29-fc5ccc71ebd7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ebb48ee140a6e3f70e05acd3f6affc6e3b71ff37
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804806"
---
# Création de l'image de récupération DaRT10


Après l’installation de Microsoft Diagnostics and Recovery Tools (DaRT) 10, vous créez une image de récupération DaRT 10. L’image de récupération démarre Windows RE, à partir duquel vous pouvez démarrer les outils DaRT. Vous pouvez générer des fichiers ISO (International Organization for Standardization) et des images de format Windows Imaging. De plus, vous pouvez utiliser PowerShell pour générer des scripts qui utilisent les paramètres que vous avez sélectionnés dans l’Assistant image de récupération DaRT. Vous pouvez utiliser le script ultérieurement pour générer des images de récupération en utilisant les mêmes paramètres. L’image de récupération fournit de nombreux outils de récupération. Pour obtenir une description des outils, voir [vue d’ensemble des outils dans DART 10](overview-of-the-tools-in-dart-10.md).

Après avoir amorcé l’ordinateur dans DaRT, vous pouvez exécuter les différents outils DaRT pour essayer de diagnostiquer et de réparer l’ordinateur. Cette section vous guide dans le processus de création de l’image de récupération DaRT et vous permet de sélectionner les outils et fonctionnalités que vous voulez inclure dans l’image.

Vous pouvez créer l’image de récupération DaRT en utilisant l’une des deux méthodes suivantes:

-   Utilisez l’Assistant image de récupération DaRT qui s’exécute dans un environnement Windows.

-   Modifiez un exemple de script PowerShell avec les valeurs de votre choix. Pour plus d’informations, reportez-vous à la rubrique [utilisation d’un script PowerShell pour créer l’image de récupération](how-to-use-a-powershell-script-to-create-the-recovery-image-dart-10.md).

Vous pouvez enregistrer le fichier ISO sur un CD ou un DVD enregistrable, l’enregistrer sur un disque mémoire flash ou l’enregistrer dans un format que vous pouvez utiliser pour démarrer dans DaRT à partir d’une partition distante ou d’une partition de récupération.

Une fois l’image ISO créée, vous pouvez la graver sur un CD ou un DVD vierge (si votre ordinateur est équipé d’un CD ou d’un lecteur de DVD). Si ce n’est pas le cas, si votre ordinateur ne possède pas de lecteur, vous pouvez utiliser la plupart des programmes génériques utilisés pour graver des CD ou DVD.

## Sélectionnez l’architecture de l’image, puis spécifiez le chemin d’accès.


Sur la page multimédia de Windows 10, vous devez indiquer si vous voulez créer une image de récupération DaRT 32 ou 64 bits. Utilisez les fenêtres 32 bits pour générer des images de récupération DaRT 32 bits et des fenêtres 64 bits pour générer des images de récupération DaRT de 64 bits. Vous pouvez utiliser un ordinateur unique pour créer des images de récupération pour les deux types d’architectures, mais vous ne pouvez pas créer une image qui fonctionne sur les architectures 32 bits et 64 bits. Vous devez également indiquer le chemin d’accès du support d’installation de Windows 10. Choisissez l’architecture qui correspond à l’une des images de récupération que vous êtes en train de créer.

**Pour sélectionner l’architecture de l’image et spécifier le chemin**

1.  Sur la page **multimédia sur Windows 10** , sélectionnez l’une des options suivantes:

    -   Si vous créez une image de récupération pour les ordinateurs 64 bits, sélectionnez **créer une image au format x64 (64 bits)**.

    -   Si vous créez une image de récupération pour les ordinateurs 32 bits, sélectionnez **créer une image de type x86 (32 bits)**.

2.  Dans la zone **Spécifiez le chemin d’accès racine de la boîte de réception Windows 10 &lt; 64 bits ou 32 &gt; ** bits, tapez le chemin d’accès des fichiers d’installation de Windows 10. Utilisez une variable PATH qui correspond à l’architecture de l’image de récupération que vous êtes en train de créer.

3.  Cliquez sur **Suivant**.

## Sélectionner les outils à inclure dans l’image de récupération


Dans la page outils, vous pouvez sélectionner de nombreux outils à inclure dans l’image de récupération. Ces outils seront accessibles aux utilisateurs finaux au démarrage de l’image DaRT. Toutefois, si vous activez la connectivité à distance lors de la création de l’image DaRT, tous les outils seront disponibles lorsque le travailleur du support technique se connecte à l’ordinateur de l’utilisateur final, quels que soient les outils que vous avez choisi d’inclure dans l’image.

Pour limiter l’accès de l’utilisateur final à ces outils, tout en conservant l’accès complet aux outils par le biais de la visionneuse de connexions à distance, ne sélectionnez pas ces outils dans la page outils. Les utilisateurs finaux pourront uniquement utiliser une connexion distante et pourront voir les outils que vous excluez de l’image de récupération.

**Pour sélectionner les outils à inclure dans l’image de récupération**

1.  Dans la page **Outils** , activez la case à cocher en regard de chaque outil que vous souhaitez inclure dans l’image.

2.  Cliquez sur **Suivant**.

## Choisir d’autoriser ou non la connectivité à distance par un support technique


Sur la page connexion à distance, vous pouvez choisir d’autoriser un employé du support technique à se connecter aux outils DaRT et à les exécuter sur l’ordinateur de l’utilisateur final. L’option connectivité à distance est alors affichée comme option disponible dans la fenêtre jeu d’outils de diagnostics et de récupération. Après avoir établi une connexion à distance, les utilisateurs du support technique peuvent exécuter les outils DaRT sur l’ordinateur de l’utilisateur final à partir d’un emplacement distant.

**Pour indiquer si vous souhaitez autoriser la connectivité à distance par des travailleurs du support technique**

1.  Dans la page **connexion à distance** , activez la case à cocher **autoriser les connexions à** distance pour autoriser les connexions à distance, ou désactivez la case à cocher pour empêcher les connexions à distance.

2.  Si vous avez désactivé la case à cocher **autoriser les connexions à distance** , cliquez sur **suivant**. Dans le cas contraire, passez à l’étape suivante pour poursuivre la configuration de la connectivité à distance.

3.  Sélectionnez l’un des éléments suivants:

    -   Laisser Windows choisir un numéro de port ouvert.

    -   Spécifiez le numéro de port. Si vous sélectionnez cette option, entrez un numéro de port compris entre 1 et 65535 dans le champ en dessous de l’option. Ce numéro de port sera utilisé lors de l’établissement d’une connexion à distance. Nous vous recommandons d’utiliser le numéro de port 1024 ou une version ultérieure pour réduire l’éventualité d’un conflit.

4.  (Facultatif) dans la zone message d’accueil de la **connexion à distance** , créez un message personnalisé que les utilisateurs finaux reçoivent lors de l’établissement d’une connexion à distance. Le message peut contenir jusqu’à 2048 caractères.

5.  Cliquez sur **Suivant**.

    Pour plus d’informations sur l’exécution des outils DaRT à distance, voir [Comment récupérer des ordinateurs distants à l’aide de l’image de récupération DART](how-to-recover-remote-computers-by-using-the-dart-recovery-image-dart-10.md).

## Ajouter des pilotes à l’image de récupération


Dans l’onglet pilotes de la page Options avancées, vous pouvez ajouter des pilotes de périphériques supplémentaires dont vous aurez besoin lors de la réparation d’un ordinateur. Celles-ci peuvent généralement inclure des contrôleurs de stockage ou de réseau qui ne sont pas fournis par Windows 10. Les pilotes sont installés lors de la création de l’image.

**Important**  Lorsque vous sélectionnez les pilotes à inclure, sachez que la connectivité sans fil (par exemple, Bluetooth ou 802.11 a/b/g/n) n’est pas prise en charge dans DaRT.

 

**Pour ajouter des pilotes à l’image de récupération**

1.  Dans la page **Options avancées** , cliquez sur l’onglet **pilotes** .

2.  Cliquez sur **Ajouter**.

3.  Recherchez le fichier à ajouter pour le pilote, puis cliquez sur **ouvrir**.

    **Remarques**  Le fichier de pilote est fourni par le fabricant du contrôleur de stockage ou de réseau.

     

4.  Répétez les étapes 2 et 3 pour chaque pilote que vous souhaitez inclure.

5.  Cliquez sur **Suivant**.

## Ajouter des packages facultatifs WinPE à l’image de récupération


Dans l’onglet WinPE de la page Options avancées, vous pouvez ajouter des packages facultatifs WinPE à l’image DaRT. Ces packages font partie de Windows ADK, qui est une condition d’installation requise pour l’Assistant image de récupération DaRT. Les outils que vous pouvez sélectionner tous sont facultatifs. Les packages requis sont ajoutés automatiquement en fonction des outils sélectionnés sur la page outils.

Vous pouvez également spécifier la taille de l’espace de travail. Espace de travail indique la quantité d’espace disque RAM qui est configurée de façon à ce qu’elle s’exécute. L’espace de travail est utile si le disque dur de l’utilisateur final n’est pas disponible. Si vous exécutez des outils et des pilotes supplémentaires, vous souhaiterez probablement augmenter l’espace de travail.

**Pour ajouter des packages facultatifs WinPE à l’image de récupération**

1.  Dans la page **Options avancées** , cliquez sur l’onglet **WinPE** .

2.  Activez la case à cocher en regard de chaque package que vous voulez inclure dans l’image, ou cliquez sur la case à cocher **nom** pour sélectionner tous les packages.

3.  Dans le champ **espace de travail** , sélectionnez l’espace disque RAM à allouer pour l’exécution de DART dans le cas où le disque dur de l’utilisateur final n’est pas disponible.

4.  Cliquez sur **Suivant**.

## Ajouter des outils de débogage pour l’analyseur d’incidents


Si vous incluez l’outil Analyseur d’incident dans l’image ISO, vous devez également inclure les outils de débogage pour Windows. Dans l’onglet analyse crash de la page Options avancées, entrez le chemin d’accès des outils de débogage de Windows 10, que l’analyseur crash utilise pour analyser les fichiers de vidage de mémoire. Vous pouvez utiliser les outils de l’ordinateur sur lequel vous exécutez l’Assistant image de récupération DaRT ou vous pouvez utiliser les outils qui se trouvent sur l’ordinateur de l’utilisateur final. Si vous décidez d’utiliser les outils de l’ordinateur de l’utilisateur final, n’oubliez pas que tous les ordinateurs que vous diagnostiquez doivent avoir installés les outils de débogage.

Si vous avez installé le kit de développement logiciel (SDK) Microsoft Windows ou le kit de développement Microsoft Windows (WDK), les outils de débogage de Windows 10 sont ajoutés à l’image de récupération par défaut, et le chemin d’accès aux outils de débogage est automatiquement rempli. Vous pouvez modifier le chemin d’accès des outils de débogage de Windows 10 si les fichiers sont situés à un autre endroit que l’emplacement indiqué par le chemin d’accès par défaut du fichier. Un lien dans l’Assistant vous permet de télécharger et d’installer les outils de débogage pour Windows s’ils ne le sont pas déjà.

Pour télécharger les outils de débogage Windows, voir [outils de débogage pour Windows](https://go.microsoft.com/fwlink/?LinkId=266248). Installez les outils de débogage à l’emplacement par défaut.

**Remarques**  L’Assistant DaRT vérifie les outils dans la `HKLM\Software\Microsoft\Windows Kits\Installed Roots\WindowsDebuggersRoot` clé de registre. S’il n’y a pas de valeur de Registre, l’Assistant recherche dans l’un des emplacements suivants, selon votre architecture système:

`%ProgramFilesX86%\Windows Kits\10.0\Debuggers\x64`

`%ProgramFilesX86%\Windows Kits\10.0\Debuggers\x86`

 

**Pour ajouter les outils de débogage pour crash Analyzer**

1.  Dans la page **Options avancées** , cliquez sur l’onglet **analyse crash** .

2.  Facultatif Cliquez sur **Télécharger les outils de débogage** pour télécharger les outils de débogage pour Windows.

3.  Sélectionnez l’une des options suivantes:

    -   **Incluez les &lt; &gt; outils de débogage Windows 10 64 ou 32 bits**. Si vous sélectionnez cette option, recherchez et sélectionnez l’emplacement des outils si le chemin n’est pas déjà affiché.

    -   **Utilisez les outils de débogage du système en cours de débogage**. Si vous sélectionnez cette option, l’analyseur d’incident ne fonctionnera pas si les outils de débogage pour Windows ne se trouvent pas sur le problème de l’ordinateur.

4.  Cliquez sur **Suivant**.

## Sélectionner les types de fichiers image de récupération à créer


Dans la page créer une image, vous choisissez un dossier de sortie pour l’image de récupération, entrez un nom d’image, puis sélectionnez les types de fichiers image de récupération DaRT à créer. Pendant le processus de création d’image de récupération, les fichiers sources Windows sont décompressés et les fichiers DaRT sont copiés vers ce fichier, et l’image est alors «recompressée» dans les formats de fichier que vous avez sélectionnés sur cette page.

Les types de fichiers image disponibles sont les suivants:

-   **Fichier d’imagerie Windows (WIM)** -utilisé pour déployer DART dans un environnement d’exécution prédémarrage (PXE) ou une partition locale).

-   La **norme ISO (International Standards Organization)** – utilisée pour effectuer un déploiement sur un CD ou un DVD, ou pour une utilisation dans des machines virtuelles (VM). L’Assistant nécessite que l’image ISO possède une extension de nom de fichier. ISO, car la plupart des programmes permettant de graver un CD ou un DVD nécessitent cette extension. Si vous ne spécifiez pas un autre emplacement, l’image ISO est créée sur votre ordinateur de bureau portant le nom DaRT10. ISO.

-   **Script PowerShell** : crée une image de récupération DART avec des commandes qui fournissent essentiellement les mêmes options que celles que vous pouvez sélectionner à l’aide de l’Assistant image de récupération Dart. Le script vous permet également d’ajouter ou de modifier des fichiers dans l’image de récupération DaRT.

Si vous activez la case à cocher modifier l’image sur cette page, vous pouvez personnaliser l’image de récupération lors du processus de création d’image. Par exemple, vous pouvez modifier le fichier «winpeshl.ini» pour créer un ordre de démarrage personnalisé ou ajouter des outils tiers.

**Pour sélectionner les types de fichiers image de récupération à créer**

1.  Dans la page **créer une image** , cliquez sur **Parcourir** pour choisir le dossier de sortie du fichier image.

    **Remarques**  La taille de l’image peut varier en fonction des outils sélectionnés et des fichiers que vous ajoutez dans l’Assistant.

     

2.  Dans la zone nom de l' **image** , entrez un nom pour l’image de récupération DART, ou acceptez le nom par défaut DaRT10.

    L’Assistant crée un sous-dossier dans le chemin de sortie à l’aide de ce nom.

3.  Sélectionnez les types de fichiers image que vous souhaitez créer.

4.  Choisissez l’une des options suivantes:

    -   Pour modifier les fichiers dans l’image de récupération avant de créer les fichiers image, activez la case à cocher **modifier l’image** , puis cliquez sur **préparer**.

    -   Pour créer l’image de récupération sans modifier les fichiers, cliquez sur **créer**.

5.  

    Cliquez sur **Suivant**.

## Modifier les fichiers image de récupération


Vous pouvez modifier l’image de récupération uniquement si vous avez activé la case à cocher modifier l’image dans la page créer une image. Après avoir préparé l’image de récupération, vous pouvez ajouter et modifier les fichiers image de récupération avant de créer le média amorçable. Par exemple, vous pouvez créer une commande personnalisée pour le démarrage, ajouter différents outils tiers, etc.

**Pour modifier les fichiers image de récupération**

1.  Dans la page **modifier l’image** , cliquez sur **ouvrir** dans l’Explorateur Windows.

2.  Créez un sous-dossier dans le dossier qui est répertorié dans la boîte de dialogue.

3.  Copiez les fichiers que vous souhaitez inclure dans le nouveau sous-dossier ou supprimez ceux que vous ne voulez pas utiliser.

4.  Cliquez sur **créer** pour commencer à créer l’image de récupération.

## Générer les fichiers image de récupération


Sur la page générer des fichiers, l’image de récupération DaRT est générée pour les types de fichiers que vous avez sélectionnés sur la page créer une image.

**Pour générer les fichiers image de récupération**

-   Dans la page **générer des fichiers** , cliquez sur **suivant** pour générer les fichiers image de récupération.

## Copier l’image de récupération sur un CD, un DVD ou un lecteur USB


Sur la page créer un média amorçable, vous pouvez éventuellement copier le fichier image sur un CD, un DVD ou un lecteur flash USB (UFD). Vous pouvez également créer un média amorçable supplémentaire à partir de cette page en redémarrant l’Assistant.

**Remarques**  Le déploiement de l’environnement d’exécution prédémarrage (PXE) et du déploiement d’image locale n’est pas pris en charge en mode natif par cet outil, car ils nécessitent des outils d’entreprise supplémentaires, tels que System Center Configuration Manager et le kit de ressources de développement Microsoft.

 

**Pour copier l’image de récupération sur un CD, un DVD ou un lecteur USB**

1.  Dans la page **créer un média amorçable** , sélectionnez le fichier ISO que vous voulez copier.

2.  Insérez un CD, un DVD ou un lecteur USB, puis sélectionnez le lecteur.

    **Remarques**  Si un lecteur n’est pas reconnu et que vous installez un nouveau lecteur, vous pouvez cliquer sur **Actualiser** pour forcer l’Assistant à mettre à jour la liste des lecteurs disponibles.

     

3.  Cliquez sur le bouton **créer un média amorçable** .

4.  Pour créer une autre image de récupération, cliquez sur redémarrer ou cliquez sur **Fermer** si vous avez fini de créer tous les éléments multimédias de votre choix.

## Rubriques connexes


[Vue d'ensemble des outils dans DaRT10](overview-of-the-tools-in-dart-10.md)

[Déploiement de DaRT10](deploying-dart-10.md)

 

 





