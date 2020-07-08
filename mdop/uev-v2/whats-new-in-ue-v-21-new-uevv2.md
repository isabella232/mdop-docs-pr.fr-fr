---
title: Nouveautés dans UE-V2.1
description: Nouveautés dans UE-V2.1
author: dansimp
ms.assetid: 7f385183-7d97-4602-b19a-baa710334ade
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7816fc8309a29347048172b2104750140c483587
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811651"
---
# Nouveautés dans UE-V2.1


La virtualisation de l’utilisation des utilisateurs 2,1 fournit les nouvelles fonctionnalités par rapport à UE-V 2,0. Les [notes de publication de Microsoft User Interface Virtualization (UE-v) 2,1](microsoft-user-experience-virtualization--ue-v--21-release-notesuevv21.md) fournissent des informations supplémentaires sur la version d’UE-v 2,1.

## Modèle d’emplacement des paramètres d’Office 2013


UE-V 2,1 inclut le modèle d’emplacement des paramètres Microsoft Office 2013 avec une prise en charge améliorée des signatures Outlook. Dans UE-V 2,1, les données de signature sont synchronisées entre les appareils des utilisateurs. Nous avons ajouté la synchronisation des paramètres de signature par défaut pour les courriers électroniques, les réponses et les transferts. Les clients n’ont plus besoin de choisir les paramètres de signature par défaut.

**Remarques**  Un profil Outlook doit être créé pour tout appareil sur lequel un utilisateur souhaite synchroniser sa signature Outlook. Si ce n’est pas le cas, l’utilisateur peut en créer un, puis redémarrer Outlook sur cet appareil pour activer la synchronisation des signatures.

 

Auparavant, UE-V incluait les modèles d’emplacement des paramètres Microsoft Office 2010 qui ont été automatiquement distribués et enregistrés auprès de l’agent UE-V. UE-V 2,1 utilise Office 365 pour déterminer si les paramètres d’Office 2013 sont itinérants par Office 365. Si les paramètres sont itinérants par Office 365, ils ne sont pas itinérants par UE-V. La [vue d’ensemble des paramètres utilisateur et itinérance pour Office 2013](https://go.microsoft.com/fwlink/p/?LinkID=391220) fournit des informations supplémentaires.

Pour activer la synchronisation des paramètres avec UE-V 2,1, effectuez l’une des opérations suivantes:

-   Utiliser une stratégie de groupe pour désactiver la synchronisation d’Office 365

-   Ne pas activer l’interface de synchronisation Office 365 lors de l’installation d’Office 2013

UE-V 2,1 inclut [les modèles office 2013 et office 2010](https://technet.microsoft.com/library/dn458932.aspx#autosyncsettings). Cette version supprime les modèles Office 2007. Les utilisateurs peuvent toujours utiliser les modèles Office 2007 d’UE-V 2,0 ou une version antérieure et peuvent toujours obtenir les modèles de la Galerie de modèles UE-V située [ici](https://go.microsoft.com/fwlink/p/?LinkID=246589).

## Résoudre les problèmes des utilisateurs d’espaces de noms du système de fichiers DFS


UE-V a amélioré la prise en charge du système de fichiers DFS en ajoutant une configuration UE-V appelée SyncProviderPingEnabled. La désactivation de cette configuration à l’aide de PowerShell ou WMI permet aux utilisateurs de désactiver le ping UE-V. Dans le cas d’un serveur DFSN, le test ping d’UE-V génère une erreur, car ces serveurs ne répondent pas aux pings. Le non-réponse empêche UE-V de synchroniser les paramètres. La désactivation de la commande ping UE-V autorise le fonctionnement normal de la synchronisation UE-V.

Pour désactiver la commande ping UE-V, utilisez l’applet de commande PowerShell suivante:

``` syntax
Set-UevConfiguration -DisableSyncProviderPing
```

## Synchronisation des informations d’identification


UE-V 2,1 permet aux clients de synchroniser les informations d’identification et les certificats stockés dans le gestionnaire d’informations d’identification Windows. Ce composant est désactivé par défaut. Lorsque ce composant est activé, les utilisateurs gardent leurs informations d’identification de domaine et leurs certificats synchronisés. Les utilisateurs peuvent se connecter une fois sur un appareil, et ces informations d’identification sont itinérantes pour cet utilisateur sur tous les appareils compatibles avec UE-V. La [gestion des informations d’identification avec UE-V 2,1](https://technet.microsoft.com/library/dn458932.aspx#creds) fournit des informations supplémentaires.

**Remarques**  Dans Windows 8 et versions ultérieures, le gestionnaire d’informations d’identification contient des informations d’identification Web. Ces informations d’identification ne sont pas synchronisées entre les appareils des utilisateurs.

 

## UE-V et synchronisation de compte Microsoft


UE-V détecte si les «paramètres de synchronisation avec OneDrive», également appelés «synchronisation de compte Microsoft», sont activés. Si le compte Microsoft n’est pas configuré pour synchroniser les paramètres, UE-V synchronise les applications Windows, les packages AppX et les paramètres de bureau Windows entre les appareils. Cela permet aux utilisateurs d’accéder à leurs applications du Windows Store, de la musique, des images et d’autres applications basées sur les comptes Microsoft sans être synchronisées en dehors du pare-feu de l’entreprise. UE-V vérifie si la stratégie de groupe arrêtera de synchroniser les paramètres avec OneDrive ou si l’utilisateur désactive la **synchronisation de vos paramètres sur cet ordinateur** dans les contrôles utilisateur.

## Support pour le PowerSchool externe


Une nouvelle [configuration de PowerSchool](https://technet.microsoft.com/library/dn554321.aspx) appelée **externe** spécifie que si les paramètres d’UE-V sont écrits dans un dossier local sur l’ordinateur de l’utilisateur, tout moteur de synchronisation externe (par exemple, OneDrive entreprise, dossiers de travail, SharePoint ou Dropbox) peut être utilisé pour appliquer ces paramètres aux différents ordinateurs auxquels les utilisateurs accèdent.

## Prise en charge améliorée du mode VDI


UE-V 2,1 inclut la [prise en charge des sessions VDI](https://technet.microsoft.com/library/dn458932.aspx#vdi) partagées entre les utilisateurs finaux. En tant qu’administrateur, vous pouvez enregistrer et configurer un modèle d’infrastructure VDI spéciale, qui permet de garantir le maintien de toutes ses fonctionnalités intactes pour les sessions VDI non persistantes.

**Remarques**  Si vous n’activez pas le mode VDI pour les sessions VDI non persistantes, il est possible que certaines fonctionnalités ne fonctionnent pas, telles que sauvegarde et restauration et LKG.

 

## Sauvegarde et restauration d’administration


Vous pouvez restaurer des paramètres supplémentaires quand un utilisateur a adopté un nouvel appareil en plaçant un modèle d’emplacement des paramètres dans l’applet de connexion **Backup** ou **itinérance (par défaut)** à l’aide de l’applet de connexion Set-UevTemplateProfile PowerShell. Cela permet aux paramètres de l’ordinateur de se synchroniser avec le nouvel ordinateur, en plus des paramètres utilisateur. Les modèles attribués au profil de sauvegarde sont sauvegardés pour cet appareil et configurés sur une base par appareil. Pour plus d’informations, retrouvez la [sauvegarde et la restauration d’administration dans UE-V 2. x](manage-administrative-backup-and-restore-in-ue-v-2x-new-topic-for-21.md) .

## Synchronisation pour les paramètres Windows supplémentaires


UE-V synchronise désormais la personnalisation du clavier visuel, le dictionnaire orthographique et permet le changement d’application pour les applications récentes et les paramètres de bord de l’écran à synchroniser entre les appareils Windows 8 et Windows 8,1.






## Rubriques connexes


[Prise en main d'UE-V2.x](get-started-with-ue-v-2x-new-uevv2.md)

[Préparer un déploiement UE-V 2. x](prepare-a-ue-v-2x-deployment-new-uevv2.md)

[Notes de publication pour Microsoft User Experience Virtualization (UE-V)2.1](microsoft-user-experience-virtualization--ue-v--21-release-notesuevv21.md)

 

 





