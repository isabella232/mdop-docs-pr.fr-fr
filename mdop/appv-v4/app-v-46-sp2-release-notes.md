---
title: Notes de publication d'App-V4.6SP2
description: Notes de publication d'App-V4.6SP2
author: dansimp
ms.assetid: abb536f0-e187-4c5b-952a-f837abd10ad2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: cf36a6361e6f49c2b868c6752e1b2eb379cc9a31
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809299"
---
# Notes de publication d'App-V4.6SP2


**Pour effectuer une recherche dans ces notes de publication, appuyez sur CTRL + F.**

Lisez attentivement ces notes de publication avant de procéder à l’installation de Microsoft Application Virtualization (App-V) 4.6 SP2.

Ces notes de publication contiennent des informations nécessaires à l’installation réussie du SP2 pour l’application virtualisation des applications 4,6. Les notes de publication contiennent également des informations qui ne sont pas disponibles dans la documentation du produit. S’il existe une différence entre ces notes de publication et la nouvelle documentation App-V 4.6 SP2, la dernière modification doit être considérée comme faisant autorité. Ces notes de publication remplacent le contenu qui est inclus dans ce produit.

## À propos de la documentation relative aux produits


Pour plus d’informations sur la documentation pour App-V, voir la page [virtualisation d’application](https://go.microsoft.com/fwlink/?LinkID=232982) sur Microsoft TechNet.

## Envoi de commentaires


Vos commentaires sur App-V 4.6 SP2 vous intéressent. Vous pouvez envoyer vos commentaires à <mdopdocs@microsoft.com> .

**Remarques**  Cette adresse de messagerie n’est pas un canal de prise en charge, mais vos commentaires nous aideront à planifier des changements ultérieurs pour la documentation et les versions de nos produits.

 

Pour obtenir les informations les plus récentes sur MDOP et les ressources de formation supplémentaires, voir la page d' [utilisation de MDOP](https://go.microsoft.com/fwlink/p/?LinkId=236032) .

Pour en savoir plus sur les nouvelles mises à jour ou pour nous faire part de vos commentaires, suivez-nous sur [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) ou [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447).

## <a href="" id="known-issues-with-app-v-4-6-sp2-"></a>Problèmes connus liés à l’application-V 4.6 SP2


### La prise en charge des noms de fichiers courts est désactivée pour les disques physiques non-systèmes lors de l’ordre

Lorsque vous séquencez sur Windows 8 ou Windows Server 2012, la prise en charge des noms de fichiers courts (8,3) est désactivée par défaut pour les lecteurs physiques non-système.

Le disque physique sous-jacent associé au répertoire principal de l’application virtuelle (par exemple, «Q:\\appname») sur la station de séquençage doit fournir une prise en charge de nom de fichier court (8,3), afin que le Sequencer App-V 4.6 SP2 puisse générer des noms de fichiers courts lors de la création de packages d’applications virtuelles. La prise en charge des noms de fichiers courts (8,3) est désactivée par défaut pour les lecteurs physiques non-systèmes sur Windows 8 ou Windows Server 2012.

**Solution de contournement:** Activer la prise en charge des noms de fichiers courts (8,3) sur les lecteurs physiques non-système. Vous pouvez utiliser la commande suivante pour activer la prise en charge des noms de fichiers courts sur Windows 8 ou Windows Server 2012.

``` syntax
fsutil 8dot3name set <virtual drive letter>:
```

Par exemple, utilisez la commande suivante si la lettre de lecteur est «Q:»:

``` syntax
fsutil 8dot3name set Q: 0
```

**Remarques**  Vous n’avez pas besoin de modifier ce paramètre sur le client App-V, car le système de fichiers App-V gère correctement les chemins d’accès courts sur Windows 8 ou Windows Server 2012.

 

### <a href="" id="-------------app-v-does-not-override-the-default-handler-for-file-type-or-protocol-associations-on-windows-8"></a> App-V ne remplace pas le gestionnaire par défaut pour les associations de types de fichiers ou de protocoles sur Windows 8

Si vous sélectionnez une application par défaut en utilisant les **programmes par défaut** du **panneau de configuration** dans Windows 8, l’application-V ne remplacera pas les associations de types de fichier associées pour cette application.

**Solution de contournement:** Néant.

### La fonction de virtualisation d’Outlook 2010 n’est pas proposée comme option de liens sur Windows 8

L’extension d’interpréteur de formations mailto ne propose pas de services virtuels Outlook 2010 sur Windows 8. Par exemple, si vous cliquez sur un lien mailto: de Microsoft Outlook 2010 exécuté sur Windows 8, une nouvelle fenêtre de courrier n’est pas créée. Cette option fonctionne correctement sur Windows 7 et les versions antérieures du système d’exploitation Windows.

**Solution de contournement:** Néant.

### <a href="" id="-------------application-virtualization-4-6-sp2-update-is-not-offered-on-all-locales-that-use-microsoft-update"></a> La mise à jour du SP2 Application Virtualization 4,6 n’est pas disponible sur les paramètres régionaux qui utilisent Microsoft Update

Lorsque vous utilisez Microsoft Update, la mise à jour pour App-V 4.6 SP2 n’est pas disponible pour les paramètres régionaux de langue suivants:

-   Kazakh

-   Hindi

-   Serbe-cyrillique

**Solution de contournement:** Si vous utilisez Microsoft Windows Server Update Services (WSUS), utilisez la version anglaise de la mise à jour ou téléchargez la mise à jour à partir du catalogue Microsoft Update.

## Informations de copyright des notes de publication


Microsoft, Active Directory, ActiveX, Bing, Excel, Silverlight, SQLServer, Windows, MicrosoftIntune et WindowsPowerShell sont des marques commerciales du groupe de sociétés Microsoft. Toutes les autres marques déposées sont la propriété de leurs détenteurs respectifs.



## Rubriques connexes


[À propos de Microsoft Application Virtualization4.6 SP2](about-microsoft-application-virtualization-46-sp2.md)

 

 





