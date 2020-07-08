---
title: Informations pour résoudre les problèmes liés à Application Virtualization Client
description: Informations pour résoudre les problèmes liés à Application Virtualization Client
author: dansimp
ms.assetid: 260a8dad-847f-4ec0-b7dd-6e6bc52017ed
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4c2ab332f5f3b7f8cdc40f6d35e8712d55028a60
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806209"
---
# Informations pour résoudre les problèmes liés à Application Virtualization Client


Cette rubrique contient des informations que vous pouvez utiliser pour résoudre divers problèmes sur le client Application Virtualization (App-V).

## L’actualisation de la publication est très lente


Si l’actualisation de la publication sur un ordinateur spécifique prend beaucoup plus de temps que prévu et si le client est configuré pour utiliser le paramètre **IconSourceRoot** , déterminez si **IconSourceRoot** contient une URL non valide. Une URL non valide entraînera de longs retards lors de l’actualisation de la publication.

## Les utilisateurs ne peuvent pas se connecter au serveur et passer en mode opérations hors connexion


Lorsque vous utilisez un serveur de gestion application-V configuré avec le protocole RTSP, si les utilisateurs ne parviennent pas à se connecter et sont dans le mode opérations déconnectées, déterminez si le certificat utilisé sur le serveur est valide. Si ce n’est pas le cas, les utilisateurs ne pourront pas se connecter et pourront y accéder en mode hors connexion.

## <a href="" id="users-experience-slow-performance-when-applications-are-not-fully-cached-"></a>Les utilisateurs connaissent une dégradation des performances lorsque les applications ne sont pas entièrement mises en cache


Lorsque les applications ne sont pas entièrement mises en cache, les utilisateurs peuvent occasionnellement découvrir des performances intermittentes ou intermittentes au démarrage ou à l’utilisation de l’application. Il peut y avoir plusieurs raisons à cela, par exemple lorsque le client App-V est dans le processus de chargement automatique d’une application ou lors du traitement d’une demande d’absence de séquence. Lorsque les applications sont entièrement mises en cache, ces problèmes ne se produiront plus.

## <a href="" id="error-displayed-after-an-update-is-removed-"></a>Erreur affichée après la suppression d’une mise à jour


Vous devez utiliser le format de commande Windows Installer 3,1 approprié pour supprimer une mise à jour du client App-V, comme suit:

`Msiexec /I {F82584A0-D706-4D2D-9BC1-7E6D8BE3BB0F} MSIPATCHREMOVE={BE3DD018-9A1F-40FD-9538-C0A995CBD254} /qb /l*v "Uninstall.log"`

L’utilisation de l’ancien format de commande `msiexec /package <GUID> /uninstall <GUID>` entraîne l’erreur 6003 «le client de virtualisation des applications n’a pas pu être démarré».

## Code d’erreur 0A-0000E01E se produit lorsque vous essayez de démarrer une application


Code d’erreur 0A-0000E01E indique que le package d’application séquencé est peut-être endommagé. La solution consiste à reséquencer le package.

## Les utilisateurs ne peuvent pas accéder aux fichiers qu’ils ont créés sur le lecteur Q:


Si les utilisateurs enregistrent des fichiers sur le lecteur **Q:** , ils ne peuvent pas les récupérer, car ils ne disposent pas de droits de lecture sur le lecteur. Les utilisateurs ne peuvent pas enregistrer des fichiers sur le lecteur **Q:** .

## L’utilisateur est invité à entrer une erreur 1D1


Lorsque l’URL de diffusion de fichier est définie de manière incorrecte dans le fichier d’OSD (Open Software Descriptor), le client App-V renvoie une erreur 1d1 au lieu d’une erreur «fichier introuvable». Cette erreur indique que le démarrage de l’application a échoué et que l’utilisateur a été forcé de basculer en mode opérations hors connexion. Corrigez l’URL de diffusion du fichier.

## Icônes incorrectes associées à certaines applications


Lorsqu’une icône doit être utilisée dans une opération de publication, le client App-V détermine d’abord s’il possède déjà une copie mise en cache de l’icône, en consultant le cache d’icônes pour un élément dont le chemin source d’origine correspond au chemin d’accès de l’icône fournie à l’opération de publication. Si le client App-V trouve une correspondance, il utilise l’icône déjà mise en cache; dans le cas contraire, il télécharge la nouvelle icône dans le cache. Si le chemin d’accès à l’icône est un répertoire de travail ou s’il est réutilisé pour de nouvelles icônes ou packages, la recherche dans le cache peut sélectionner l’icône incorrecte d’une opération précédente.

## Les utilisateurs sont invités à entrer leurs informations d’identification lors du démarrage d’une application.


Si un utilisateur tente de démarrer une application virtuelle à laquelle l’administrateur système a restreint l’accès, il est possible qu’il soit invité à entrer les informations d’identification. L’utilisateur doit taper le nom d’utilisateur et le mot de passe d’un compte qui est autorisé à lancer l’application, puis appuyez sur entrée.

## Échec de l’actualisation de publication après la mise à niveau du client App-V vers la version 4,5


Si le répertoire de données utilisateur a été placé auparavant dans un emplacement standard (%*ALLUSERSPROFILE*%\\Documents\\SoftGrid Client\\Users\\%*nom_utilisateur*%), les utilisateurs ne disposant pas des droits d’administrateur sur l’ordinateur constateront que l’actualisation de publication échoue après la mise à niveau du client App-V. Lors de la mise à niveau, le répertoire de données global du client App-V et tous ses sous-répertoires sont configurés avec des droits d’accès restreints pour les administrateurs uniquement. Pour éviter ce problème, vous pouvez modifier le répertoire des données utilisateur avant de procéder à la mise à niveau afin qu’il ne s’agit pas d’un sous-répertoire du répertoire global Data.

## Redémarrage requis après l’installation


Si l’installation du client échoue pour une raison quelconque et si des tentatives ultérieures d’installation du client échouent, consultez le journal du programme d’installation Windows pour savoir si le message d’erreur «sftplay Fail, erreur = possède 1072 au» s’affiche. Si tel est le cas, redémarrez l’ordinateur avant d’essayer de réinstaller le client.

## Réparer une application virtuelle endommagée


Si, pour une raison quelconque, un package d’application virtuelle installé à l’aide d’un fichier MSI (Windows Installer Package) est endommagé, réinstallez le package. La fonction de réparation disponible dans le programme d’installation Windows n’entraîne pas la mise à jour des volumes utilisateurs.

## Rubriques connexes


[Référence d'Application Virtualization Client](application-virtualization-client-reference.md)

 

 





