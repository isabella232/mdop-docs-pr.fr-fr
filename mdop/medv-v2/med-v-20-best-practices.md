---
title: Meilleures pratiques concernant MED-V2.0
description: Meilleures pratiques concernant MED-V2.0
author: dansimp
ms.assetid: 47ba2dd1-6c6e-4d6e-8e18-b42291f8e02a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7b664d33b403b821ce6bc9c045d937380ab4f91b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811561"
---
# Meilleures pratiques concernant MED-V2.0


Lors de la planification, du déploiement et de la gestion de MED-V au sein de votre entreprise, il est possible que vous trouviez les recommandations recommandées.

### Configurer le programme pour qu’il soit exécuté pour la première fois

Même si vous pouvez spécifier les paramètres de votre choix, il est recommandé de créer le fichier Sysprep. inf pour permettre l’exécution du programme d' **installation pour la** première fois. Pour cela, vous devez fournir toutes les informations de paramètres requises lors de la poursuite de l’Assistant gestion de l' **installation** . Pour plus d’informations sur la configuration de l’image MED-V, voir [configuration d’une image de PC virtuel Windows pour med-v](configuring-a-windows-virtual-pc-image-for-med-v.md).

### Désactiver les points de restauration sur l’ordinateur virtuel

Avant de créer le package d’espace de travail MED-V, nous vous recommandons de désactiver les points de restauration sur l’ordinateur virtuel pour empêcher le disque de différenciation de croître. Pour plus d’informations, reportez-vous à la rubrique désactivation [et activation de la restauration du système dans Windows XP](https://go.microsoft.com/fwlink/?LinkId=195927) ( https://go.microsoft.com/fwlink/?LinkId=195927) .

### Configurer l’image MED-V pour utiliser les profils locaux

Nous vous recommandons d’appliquer uniquement ces stratégies qui sont utiles dans un environnement de compatibilité des applications pour Windows XP. Par exemple, la stratégie de personnalisation du Bureau ne doit généralement pas être appliquée et doit être désactivée. Pour plus d’informations sur la façon de n’autoriser que les profils locaux, voir [paramètres de stratégie de groupe pour les profils utilisateur errants](https://go.microsoft.com/fwlink/?LinkId=205072) ( https://go.microsoft.com/fwlink/?LinkId=205072) .

### Configurer une mise à jour de performance de la stratégie de groupe

Par défaut, la stratégie de groupe est téléchargée sur un ordinateur à la fois. Cela entraîne des retards lorsque MED-V est joint au domaine. Pour améliorer les performances de la stratégie de groupe, nous vous conseillons de définir la valeur de clé de Registre suivante sur le registre:

Sous-clé de Registre: HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Winlogon

Entrée: BufferPolicyReads

Type: DWORD

Valeur : 1

### Distribuer un avis légal par le biais d’une stratégie de groupe plutôt que dans l’image MED-V

Si vous souhaitez que les utilisateurs finaux puissent voir un contrat de niveau de service (SLA) avant d’accéder à MED-V, nous vous recommandons d’appliquer le SLA par le biais de la stratégie de groupe, de façon à ce qu’il soit présenté à l’utilisateur final une fois la première configuration terminée.

**Attention**  Même s’il est préférable d’exécuter la première configuration en mode **sans assistance** , si vous décidez de définir la stratégie locale ou l’entrée de Registre afin d’inclure un SLA dans votre image (disque dur virtuel), vous devez également spécifier la première fois que le programme d’installation s’exécute en mode **assisté** ou si le programme d’installation peut échouer.

 

### Compactez le disque dur virtuel

Nous vous recommandons de compacter votre disque dur virtuel pour récupérer l’espace libre sur le disque et de réduire la taille du disque dur virtuel. Pour plus d’informations sur la façon de compacter votre disque dur virtuel, voir [compactage du disque dur virtuel MED-V](compacting-the-med-v-virtual-hard-disk.md).

### Configurer l’ordinateur virtuel pour qu’il redémarre sur écran bleu

Nous vous recommandons de configurer l’ordinateur virtuel de l’espace de travail MED-V de façon à ce qu’il se bloque automatiquement lorsqu’il rencontre un blocage de l’écran bleu. Pour configurer ce paramètre dans l’invité, définissez la valeur de redémarrage dans la clé HKEY \ _LOCAL \ _MACHINE \\SYSTEM\\CurrentControlSet\\Control\\CrashControl sur «1».

Vous pouvez également configurer ce paramètre en cliquant sur **Démarrer**, puis sur **panneau**de configuration et sur **système**. Ensuite, dans la zone **démarrage et récupération** de l’onglet **avancé** , cliquez sur **paramètres**. Cochez la case **redémarrer automatiquement** , puis cliquez sur **OK**.

### Sauvegarder l’image MED-V avant de la sceller

Nous vous recommandons de créer une copie de sauvegarde de l’image MED-V avant de la sceller. Pour plus d’informations sur la façon de sceller votre image MED-V, voir [configurer une image de PC virtuel Windows pour med-v](configuring-a-windows-virtual-pc-image-for-med-v.md).

### Installer le PC virtuel Windows en dernier lors de l’installation à partir d’un fichier de commandes

Lorsque vous installez les composants MED-V à l’aide d’un fichier de commandes, spécifiez que le PC virtuel Windows et le correctif Windows Virtual PC sont installés après l’agent d’hébergement MED-v et les fichiers de package d’espace de travail MED-V. Cela permet de s’assurer que Windows Update n’entraîne aucune interférence avec le processus d’installation en nécessitant un redémarrage.

### Installer l’espace de travail MED-V à partir du dossier local

En raison de problèmes qui peuvent survenir lors de l’installation de MED-V à partir d’un emplacement réseau, il est recommandé de copier les fichiers de configuration de l’espace de travail MED-V localement, puis d’exécuter setup.exe.

### <a href="" id="manage-printer-redirection-in-one-manner-only-"></a>Gestion de la redirection d’imprimante en une seule fois

Si une imprimante est installée manuellement sur l’ordinateur virtuel de l’invité MED-V et si la même imprimante est installée sur l’ordinateur hôte, le résultat est qu’il est installé à deux reprises dans l’invité. Pour éviter ce problème, nous vous recommandons d’utiliser la meilleure pratique MED-V pour gérer la redirection d’imprimante en une seule fois: désactivez la redirection et l’installation manuelle de l’imprimante sur l’invité ou activez la redirection et n’installez pas les imprimantes manuellement sur l’invité.

### <a href="" id="configure-settings-for-med-v-guest-patching-"></a>Configurer les paramètres pour la mise à jour d’invité MED-V

Vous pouvez contrôler quand et Pendant combien de temps la machine virtuelle MED-V s’est désréveillé pour recevoir des mises à jour automatiques en définissant les valeurs de configuration pertinentes dans le registre. Dans le cadre de la meilleure pratique MED-V, vous devez configurer votre intervalle de mise en éveil pour qu’il corresponde à l’heure à laquelle vous avez planifié des mises à jour régulières des machines virtuelles MED-V. Par ailleurs, il est recommandé de configurer ces paramètres de manière à ce qu’ils ressemblent au comportement de l’ordinateur hôte.

Pour plus d’informations sur la configuration des paramètres de correction d’invité MED-V, voir [gestion des mises à jour automatiques pour les espaces de travail MED-v](managing-automatic-updates-for-med-v-workspaces.md).

### Configurer un logiciel antivirus/de sauvegarde

Pour empêcher l’activité de l’antivirus d’affecter les performances du bureau virtuel, nous vous conseillons de le faire à l’exclusion des types de fichiers d’ordinateur virtuel suivants de tout logiciel antivirus ou de processus de sauvegarde qui s’exécute sur l’ordinateur hôte MED-V:

-   \*. COMPATIBLE

-   \*. VUD

-   \*. VSV

-   \*. VIRTUELS

## Rubriques connexes


[Sécurité et protection de MED-V](security-and-protection-for-med-v.md)

 

 





