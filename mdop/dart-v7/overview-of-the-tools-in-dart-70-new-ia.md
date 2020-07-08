---
title: Vue d'ensemble des outils de DaRT7.0
description: Vue d'ensemble des outils de DaRT7.0
author: dansimp
ms.assetid: 67c5991e-cbe6-4ce9-9fe5-f1761369d1fe
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d327e14fd1851f0e0d82e1c3ad692bcf7842a835
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809959"
---
# Vue d'ensemble des outils de DaRT7.0


À partir de la fenêtre du jeu d’outils de **Diagnostics et de récupération** dans Microsoft Diagnostics and Recovery Tools (DART) 7, vous pouvez démarrer tous les outils individuels qui ont été inclus lors de la création de l’image de récupération Dart. Pour plus d’informations sur la façon d’accéder à la fenêtre de **Diagnostics et** de l’ensemble d’outils de récupération, voir [Comment récupérer des ordinateurs locaux à l’aide de l’image de récupération DART](how-to-recover-local-computers-using-the-dart-recovery-image-dart-7.md).

S’il est disponible, vous pouvez utiliser l' **Assistant solution** dans la fenêtre **jeu d’outils de diagnostics et de récupération** pour sélectionner l’outil qui répond le mieux à votre problème spécifique, en fonction d’un bref entretien.

## Découvrir les outils DaRT


Cette section décrit les différents outils qui font partie de DaRT.

### Éditeur du Registre

Vous pouvez utiliser l' **éditeur du Registre** pour accéder à la clé de Registre du système d’exploitation Windows que vous analysez ou que vous réparez et modifier celle-ci. Il s’agit de l’ajout, de la suppression et de la modification de clés et de valeurs, et de l’importation de fichiers de Registre (. reg).

**Attention**  Cette rubrique explique comment modifier le Registre Windows à l’aide de l’éditeur du Registre. Si vous modifiez la clé de registre de Windows de manière incorrecte, vous pouvez être à l’origine de problèmes importants qui peuvent nécessiter la réinstallation de Windows. Vous devez faire une copie de sauvegarde des fichiers du Registre (System. dat et User. dat) avant de modifier le registre. Microsoft ne peut pas garantir que les problèmes qui peuvent survenir lorsque vous modifiez le registre peuvent être résolus. Changez de Registre à vos propres risques.

 

### Locksmith

L' **Assistant Locksmith** vous permet de définir ou de modifier le mot de passe d’un compte local du système d’exploitation Windows que vous analysez ou réparez. Il n’est pas nécessaire de connaître le mot de passe actuel. Toutefois, le mot de passe que vous définissez doit être conforme aux exigences définies par un objet de stratégie de groupe local. Cela inclut la longueur et la complexité des mots de passe.

Vous pouvez utiliser **Locksmith** quand le mot de passe d’un compte local, tel que le compte d’administrateur local, n’est pas connu. Vous ne pouvez pas utiliser **Locksmith** pour définir des mots de passe pour les comptes de domaine.

### Analyse Crash

Utilisez l' **Assistant analyse crash** pour déterminer rapidement la cause du blocage d’un ordinateur en analysant le fichier d’image mémoire sur le système d’exploitation Windows que vous réparez. **Crash Analyzer** examine le fichier de vidage sur incident pour le pilote à l’origine de l’échec d’un ordinateur. Vous pouvez ensuite désactiver le pilote de périphérique à l’aide du nœud **services et pilotes** dans l’outil de **gestion des ordinateurs** .

L' **Assistant analyse de blocage** nécessite les outils de débogage pour Windows et les fichiers de symboles pour le système d’exploitation que vous réparez. Vous pouvez inclure les deux conditions requises lors de la création de l’image de récupération DaRT. S’ils ne sont pas inclus dans l’image de récupération et que vous ne disposez pas de l’accès sur l’ordinateur sur lequel vous réparez, vous pouvez copier le fichier de vidage de mémoire sur un autre ordinateur et utiliser la version autonome d' **crash Analyzer** pour diagnostiquer le problème.

L’exécution de l' **Analyseur de blocage** est une bonne idée même si vous envisagez de réorganiser votre ordinateur. L’image peut présenter un pilote défectueux qui pose problème dans votre environnement. L’exécution de l' **Analyseur de blocage**vous permet d’identifier les pilotes de problèmes et d’améliorer la stabilité de l’image.

Pour plus d’informations sur l' **analyseur d’incidents**, voir [diagnostic des pannes système avec l’analyseur d’incidents](diagnosing-system-failures-with-crash-analyzer--dart-7.md).

### Restauration de fichiers

La **restauration de fichiers** vous permet d’essayer de restaurer des fichiers accidentellement supprimés ou trop volumineux pour être contenus dans la corbeille. La **restauration de fichiers** n’est pas limitée aux volumes de disque normaux, mais elle permet de rechercher et de restaurer des fichiers sur des volumes perdus ou sur des volumes chiffrés par BitLocker.

### Disk commander

**Disk commander** vous permet de récupérer et réparer des partitions ou volumes de disque à l’aide de l’un des processus de récupération suivants:

-   Restaurez l’enregistrement de démarrage principal (MBR)

-   Restaurer un ou plusieurs volumes perdus

-   Restauration de tables de partitions à partir de **Disk commander** Backup

-   Enregistrer les tables de partitions dans la sauvegarde de **Disk commander**

**Avertissement**  Nous vous recommandons de sauvegarder un disque avant d’utiliser **Disk commander** pour le réparer. En utilisant **Disk commander**, vous pouvez endommager des volumes et les rendre inaccessibles. De plus, les modifications apportées à un volume peuvent affecter d’autres volumes, car les volumes sur un disque partagent une table de partitions.

 

### Effacement de disque

Vous pouvez utiliser la **réinitialisation du disque** pour supprimer l’ensemble des données d’un disque ou d’un volume, même celles qui sont laissées après le reformatage d’un disque dur. L' **effacement de disque** vous permet d’effectuer une sélection à partir d’un remplacement à une seule passe ou d’une remplacement à quatre passes qui répond aux normes actuelles du ministère de la défense des États-Unis.

**Avertissement**  Après avoir essuyé un disque ou un volume, vous ne pouvez pas récupérer les données. Vérifiez la taille et l’étiquette d’un volume avant de l’effacer.

 

### Gestion de l'ordinateur

**Gestion** de l’ordinateur est un ensemble d’outils d’administration Windows qui vous aident à résoudre les problèmes liés à l’ordinateur. Vous pouvez utiliser les outils de **gestion d’ordinateur** dans DART pour afficher des informations système et des journaux des événements, gérer des disques, afficher des Autoruns et gérer les services et pilotes. La console de **gestion des ordinateurs** est personnalisée pour vous aider à diagnostiquer et réparer les problèmes susceptibles d’empêcher le démarrage du système d’exploitation Windows.

### Architecture

L’outil **Explorateur** vous permet de parcourir le système de fichiers et les partages réseau de l’ordinateur afin de supprimer les données importantes stockées sur le disque dur local avant d’essayer de réparer ou de réutiliser l’ordinateur. Dans la mesure où vous pouvez mapper des lettres de lecteur aux partages réseau, vous pouvez facilement copier et déplacer des fichiers de l’ordinateur vers le réseau pour être sûr ou du réseau à l’ordinateur pour les restaurer.

### Assistant solution

L' **Assistant solution** présente une série de questions et recommande le meilleur outil pour la situation, en fonction de vos réponses. Cet Assistant vous aide à déterminer quel outil utiliser lorsque vous ne connaissez pas les outils dans DaRT.

### Configuration TCP/IP

Lorsque vous démarrez un ordinateur problématique dans DaRT, il est configuré pour obtenir automatiquement sa configuration TCP/IP (adresse IP et serveur DNS) à partir du protocole DHCP (Dynamic Host Configuration Protocol). Si le protocole DHCP n’est pas disponible, vous pouvez configurer manuellement TCP/IP à l’aide de l’outil de **configuration TCP/IP** . Commencez par sélectionner une carte réseau, puis configurez l’adresse IP et le serveur DNS pour cette carte.

### Désinstallation de HotFix

L' **Assistant de désinstallation de correctif** vous permet de supprimer les correctifs ou les service packs du système d’exploitation Windows sur l’ordinateur que vous réparez. Utilisez cet outil lorsqu’un correctif ou un service pack est suspecté d’empêcher le démarrage du système d’exploitation.

Nous vous recommandons de désinstaller un seul correctif à la fois, même si cet outil vous permet d’en désinstaller plusieurs.

**Important**  Les programmes installés ou mis à jour après l’installation d’un correctif risquent de ne pas fonctionner correctement après la désinstallation d’un correctif.

 

### Analyse SFC

L’outil d' **analyse SFC** démarre l' **Assistant réparation de fichiers système** et vous permet de réparer les fichiers système qui empêchent le démarrage du système d’exploitation Windows installé. L' **Assistant réparation de fichier système** peut réparer automatiquement les fichiers système endommagés ou manquants, ou vous demander avant d’effectuer des réparations.

### Recherche

Avant de répartir sur un ordinateur, il est important de récupérer des fichiers à partir du disque dur local, en particulier lorsque l’utilisateur n’a pas pu sauvegarder ou stocké les fichiers ailleurs.

L’outil de **recherche** permet d’ouvrir une fenêtre de **recherche de fichiers** que vous pouvez utiliser pour rechercher des documents lorsque vous ne connaissez pas le chemin d’accès du fichier ou pour rechercher des types de fichiers généraux sur tous les disques durs locaux. Vous pouvez rechercher des modèles de nom de fichier spécifiques dans des chemins d’accès spécifiques. Vous pouvez également limiter les résultats à une plage de dates ou une plage de tailles.

### Nettoyeur système autonome

**Important**  Les environnements dotés du nettoyeur système autonome doivent plutôt utiliser l’image de protection Microsoft Defender offline (WDO) pour détecter les programmes malveillants. En raison du fonctionnement de l’outil de nettoyage du système autonome dans DaRT, tous les déploiements de la version DaRT prises en charge ne peuvent pas appliquer ces mises à jour de protection des logiciels malveillants à leurs images DaRT.

 

Le **nettoyeur système autonome** peut vous aider à détecter les logiciels malveillants et les logiciels indésirables et vous avertir des risques en matière de sécurité. Vous pouvez utiliser cet outil pour détecter et supprimer les programmes malveillants sur un ordinateur, même si le système d’exploitation Windows installé n’est pas en cours d’exécution. Lorsque le **nettoyeur système autonome** détecte un logiciel malveillant ou indésirable, il vous invite à supprimer, mettre en quarantaine ou autoriser chaque élément.

Le logiciel malveillant qui utilise des rootkits peut se masquer à partir du système d’exploitation en cours d’exécution. Si un virus ou un logiciel espion de rootkit est sur un ordinateur, la plupart des outils d’analyse et de suppression en temps réel ne le voient plus ou ne le suppriment pas. Dans la mesure où vous démarrez l’ordinateur défectueux dans DaRT et que le système d’exploitation installé est hors connexion, vous pouvez détecter le rootkit sans qu’il puisse s’en masquer.

### Connexion à distance

L’outil de **connexion à distance** dans DART vous permet d’exécuter à distance les outils DART sur un ordinateur d’utilisateur final. Après avoir fourni certaines informations spécifiques à l’utilisateur final (ou par un professionnel du support technique travaillant sur l’ordinateur de l’utilisateur final), l’administrateur peut prendre le contrôle de l’ordinateur de l’utilisateur final et exécuter les outils DaRT nécessaires à distance.

**Important**  Les deux ordinateurs qui établissent une connexion à distance doivent faire partie du même réseau.

 

## Rubriques connexes


[Prise en main de DaRT7.0](getting-started-with-dart-70-new-ia.md)

 

 





