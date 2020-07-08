---
title: Notes de publication pour DaRT7.0
description: Notes de publication pour DaRT7.0
author: dansimp
ms.assetid: fad227d0-5c22-4efd-9187-0e5922f7250b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 5114acfe5a46a2c78f722a2bb6394c0dbef55dd4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809551"
---
# Notes de publication pour DaRT7.0


**Pour effectuer une recherche dans ces notes de publication, appuyez sur CTRL + F.**

Lisez attentivement ces notes de publication avant de procéder à l’installation de Microsoft Diagnostics and Recovery Tools (DaRT) 7.

## À propos de Microsoft Diagnostics and Recovery Tools Tools 7,0


Ces notes de publication contiennent des informations requises pour l’installation d’DaRT7 et contiennent des informations qui ne sont pas disponibles dans la documentation du produit. S’il existe une différence entre ces notes de publication et d’autres documents de la plateforme DaRT, la dernière modification doit être considérée comme faisant autorité. Ces notes de publication remplacent le contenu fourni avec ce produit.

## À propos de la documentation relative aux produits


La documentation pour Microsoft Diagnostics and Recovery Tools (DaRT) 7 est distribuée avec le produit et sur le site de connexion.

Pour obtenir une aide détaillée sur l’utilisation des outils dans DaRT7, consultez le fichier d’aide disponible dans le menu des **outils de diagnostics et de récupération** .

## Envoi de commentaires


Vos commentaires vous intéressent sur DaRT7. Vous pouvez envoyer vos commentaires à dart7feedback@microsoft.com. Cette adresse de messagerie n’est pas un canal de support, mais vos commentaires nous aideront à planifier des changements ultérieurs pour ces outils afin de les rendre plus utiles.

## Se protéger contre les failles de sécurité et les virus


Pour vous aider à vous protéger contre les failles de sécurité, nous vous recommandons d’installer les mises à jour de sécurité disponibles pour tout nouveau logiciel installé. Pour plus d’informations, reportez-vous à la rubrique [sécurité Microsoft](https://go.microsoft.com/fwlink/?LinkId=3482) ( https://go.microsoft.com/fwlink/?LinkId=3482) .

## Problèmes connus avec le 7,0 DaRT


### L’analyse SFC ne peut pas démarrer si le nettoyeur système autonome est ouvert

Si le nettoyeur système autonome est en cours d’exécution, l’analyse SFC ne peut pas démarrer ou s’exécuter en raison d’un conflit de ressources entre les deux outils.

**Solution de contournement:** Fermez le nettoyeur système autonome avant d’essayer d’ouvrir ou d’exécuter l’outil d’analyse SFC.

### Les caractères Unicode risquent de ne pas s’afficher dans les noms de fichiers

Si vous supprimez un fichier qui comporte des caractères Unicode dans son nom de fichier et que vous essayez de restaurer le fichier à l’aide de l’outil de restauration de fichiers, le fichier est introuvable. Cela se produit uniquement lorsque vous utilisez des caractères d’une langue autre que celle du DVD Windows utilisé pour créer l’image de récupération.

**Solution de contournement:** Assurez-vous que la langue utilisée par DaRT correspond à la langue utilisée par le système d’exploitation à partir duquel il tente de restaurer des fichiers.

### L’installation de la ligne de commande DaRT risque de ne pas fonctionner en silence

L’installation de l’outil de ligne de commande DaRT échoue en silence s’il est exécuté en mode quiet, sauf si elle est exécutée à l’aide d’autorisations d’administrateur élevés.

**Solution de contournement:** Exécutez l’installation de la ligne de commande à l’aide d’autorisations d’administrateur élevées. L’installation de DaRT prend en charge les options de Windows Installer standard pour l’installation de lignes de commande. Pour plus d’informations sur les différents commutateurs disponibles, voir [options de ligne de commande](https://go.microsoft.com/fwlink/?LinkId=160689) pour Windows Installer.

### La recherche de fichiers ne peut pas déplacer un dossier vers un autre volume

Le déplacement de dossiers entre des volumes n’est pas pris en charge par l’application de recherche de fichiers. Si vous tentez de déplacer un dossier vers un autre volume dans le cadre de la recherche de fichier, le message d’erreur suivant est retourné: «une erreur s’est produite lors de l’écriture du * &lt; nom &gt; *de fichier. Assurez-vous que le lecteur dispose de suffisamment d’espace et que le chemin de destination est accessible.

**Solution de contournement:** Utilisez l’Explorateur pour déplacer un dossier vers un autre volume.

### Certaines données risquent de ne pas être disponibles sur les ordinateurs sur lesquels les lettres de lecteur sont remappées

Ce problème peut se produire sur des ordinateurs compatibles avec BitLocker et sur des ordinateurs à démarrage multiple. Ce problème se produit car certaines informations du Registre hors connexion ont des lettres de lecteur codées en dur, et DaRT utilise des lettres différentes pour les mêmes volumes. Les effets courants incluent l’accès à certains comptes d’utilisateurs locaux dans l’éditeur du Registre. Par ailleurs, il est possible que certains outils ne soient pas en mesure d’obtenir des propriétés qui s’appuient sur la résolution des chemins d’accès aux fichiers.

**Solution de contournement:** Utilisez l’option pour remapper les lettres de lecteur au démarrage de DaRT. Cela aligne généralement les lettres de lecteur typiques sur ce qui est attendu.

### La désinstallation de HotFix ne peut pas désinstaller certaines mises à jour

Certains service packs et mises à jour ne peuvent pas être désinstallés parce qu’ils sont marqués comme étant désinstallés ou qu’ils doivent être désinstallés dans Windows 7. Dans ces cas, l’outil de désinstallation de correctif risque d’indiquer que ces mises à jour ont été désinstallées, même si elles ne le sont pas.

**Solution de contournement:** Désinstaller ces mises à jour problématiques de Windows 7.

### Effacement de disque: les disques contenant des volumes fractionnés, des volumes agrégés ou des volumes en miroir ne peuvent pas être supprimés.

La réinitialisation du disque ne prend pas en charge la suppression de disques qui sont fractionnés, en miroir ou en agrégats entre plusieurs volumes.

**Solution de contournement:** Sélectionnez et supprimez chaque disque dans le volume séparément.

## Informations de copyright des notes de publication


Ce document est fourni «en l’absence». Les informations et les vues exprimées dans le présent document, y compris les URL et les autres références de site Web Internet, risquent de changer sans préavis. Vous assumez le risque d’utilisation.

Quelques exemples présentés dans les présentes sont fournis à titre indicatif uniquement et sont fictifs.Aucune association ou connexion réelle ne doit être intentionnelle ou intentionnelle.

Ce document ne vous fournit aucun droit légal de propriété intellectuelle de tout produit Microsoft. Ce document est confidentiel et exclusif à Microsoft. Il est divulgué et ne peut être utilisé que dans le cadre d’un accord de non-divulgation.



Microsoft, Active Directory, ActiveSync, MS-DOS, Windows, windowsserver2003 et Windows Vista sont des marques commerciales du groupe de sociétés Microsoft.

Toutes les autres marques déposées sont la propriété de leurs détenteurs respectifs.

## Rubriques connexes


[À propos de DaRT7.0](about-dart-70-new-ia.md)

 

 





