---
title: Notes de publication pour DaRT8.0
description: Notes de publication pour DaRT8.0
author: dansimp
ms.assetid: e8b373c8-7aa5-4930-a8f9-743d26145dad
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 894708585ff4006c37085e71f365690b8424d43e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810764"
---
# Notes de publication pour DaRT8.0


**Pour effectuer une recherche dans ces notes de publication, appuyez sur CTRL + F.**

Lisez attentivement ces notes de publication avant de procéder à l’installation de Microsoft Diagnostics and Recovery Tools (DaRT) 8,0.

Ces notes de publication contiennent des informations nécessaires à l’installation réussie de DaRT 8,0. Les notes de publication contiennent également des informations qui ne sont pas disponibles dans la documentation du produit. S’il existe une différence entre ces notes de publication et d’autres documents DaRT, la dernière modification doit être considérée comme faisant autorité. Ces notes de publication remplacent le contenu qui est inclus dans ce produit.

Pour obtenir le logiciel DaRT, reportez-vous à la rubrique [obtention de MDOP](https://go.microsoft.com/fwlink/?LinkId=322049).

## À propos de la documentation relative aux produits


Pour plus d’informations sur la documentation pour DaRT, consultez la [page d’accueil de DART](https://go.microsoft.com/fwlink/?LinkID=252096) sur Microsoft TechNet.

Pour obtenir la version téléchargeable de la documentation DaRT, voir <https://go.microsoft.com/fwlink/?LinkID=267420> sur le centre de téléchargement Microsoft.

## Envoi de commentaires


Vos commentaires sur DaRT 8,0 vous intéressent. Vous pouvez envoyer vos commentaires à <mdopdocs@microsoft.com> .

**Remarques**  Cette adresse de messagerie n’est pas un canal de prise en charge, mais vos commentaires nous aideront à planifier des changements ultérieurs pour la documentation et les versions de nos produits.

 

Pour obtenir les informations les plus récentes sur MDOP et les ressources de formation supplémentaires, voir la page d' [utilisation de MDOP](https://go.microsoft.com/fwlink/p/?LinkId=236032) .

Pour en savoir plus sur les nouvelles mises à jour ou pour nous faire part de vos commentaires, suivez-nous sur [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) ou [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447).

## Problèmes connus avec le 8,0 DaRT


### La restauration du système échoue lorsque vous exécutez Locksmith ou l’éditeur du Registre

Si vous exécutez Locksmith, l’éditeur du Registre et éventuellement d’autres outils, la restauration du système échoue.

**Solution de contournement:** Fermez et redémarrez DaRT, puis démarrez la restauration du système.

### L’analyse SFC ne peut pas s’exécuter lorsque vous démarrez et fermez Locksmith ou la gestion de l’ordinateur

Si vous démarrez, puis fermez l’Locksmith ou les outils de gestion de l’ordinateur, le vérificateur de fichiers système ne s’exécute pas.

**Solution de contournement:** Fermez et redémarrez DaRT, puis démarrez SFC.

### <a href="" id="-------------dart-installer-does-not-fail-when-adk-has-not-been-installed"></a> Le programme d’installation de DaRT ne fonctionne pas lorsque ADK n’a pas été installé

Si vous installez DaRT 8,0 à l’aide de la ligne de commande pour exécuter le MSI et que le ADK n’a pas été installé, l’installation de DaRT doit échouer. Pour le moment, le programme d’installation 8,0 de DaRT installe tous les composants, à l’exception de l’image de récupération 8,0 de DaRT.

**Solution de contournement:** Néant.

### Le système Defender ne peut pas être lancé après le lancement de Locksmith, de l’analyseur de blocage et de la gestion de l’ordinateur

Le logiciel Defender ne se lance pas si vous avez déjà lancé Locksmith, RegEdit, analyse de blocage et gestion de l’ordinateur.

**Solution de contournement:** Fermez et redémarrez DaRT, puis lancez Defender.

### Le démarrage de Defender est ralenti

Le lancement de Defender peut prendre quelques minutes. La barre de progression indique l’état de chargement actuel.

**Solution de contournement:** Néant.

## Informations de copyright des notes de publication


Microsoft, Active Directory, ActiveX, Bing, Excel, Silverlight, SQLServer, Windows, MicrosoftIntune et WindowsPowerShell sont des marques commerciales du groupe de sociétés Microsoft. Toutes les autres marques déposées sont la propriété de leurs détenteurs respectifs.



## Rubriques connexes


[À propos de DaRT8.0](about-dart-80-dart-8.md)

 

 





