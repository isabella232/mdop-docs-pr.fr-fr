---
title: Procédure pour configurer le système App-V pour la mise à niveau d'un package
description: Procédure pour configurer le système App-V pour la mise à niveau d'un package
author: dansimp
ms.assetid: de133898-f887-46c1-9bc9-fbb03feac66a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5e5056f923c61aff39d9bd6e1d26f071177f7c12
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807270"
---
# Procédure pour configurer le système App-V pour la mise à niveau d'un package


Lorsque vous déployez une nouvelle version d’un package d’application existant qui a été mis à niveau dans le Sequencer App-V, vous pouvez la déployer de sorte que les clients App-V diffusent automatiquement la nouvelle version dans le cache local. En fonction de la solution de diffusion en continu utilisée, il existe différentes procédures de configuration de la mise à niveau du package. Les sections suivantes décrivent les cas les plus courants de publication et de diffusion en continu, et incluent les procédures nécessaires à la configuration de la mise à niveau du package pour chaque scénario.

## Utilisation d’un serveur de gestion pour la publication et la diffusion en continu


Dans ce scénario, un serveur d’administration d’applications-V unique est utilisé pour la publication et la diffusion en continu de packages et d’applications, et le protocole RTSP (S) requis. Lorsque le package d’origine est importé sur le serveur de gestion App-V, l’administrateur copie le dossier de package qui contient les fichiers créés par le Sequencer sur le dossier de contenu (par exemple, \\\\server\\CONTENT\\packagename.). L’administrateur modifie également l’entrée HREF du fichier OSD pour qu’il pointe sur le fichier SFT dans le dossier package, puis importe le package sur le serveur.

Lorsqu’un utilisateur est authentifié par le serveur de gestion, le serveur publie les applications de l’utilisateur en envoyant le fichier applist.xml au client. Le client récupère ensuite les fichiers et icônes d’OSD pour les applications à partir du serveur de gestion. Lorsque l’utilisateur double-clique sur l’icône d’une application, le contenu de l’application est transmis au cache client à partir du chemin d’accès spécifié dans le fichier OSD et l’application est démarrée.

### Pour mettre à niveau le package

Pour ajouter une nouvelle version d’une application qui a été mise à niveau dans le Sequencer App-V, l’administrateur doit copier le nouveau fichier SFT et tout autre fichier modifié dans le même dossier que la version d’origine de l’application. L’administrateur doit alors utiliser **Ajouter une version** dans la console de gestion du serveur pour ajouter la nouvelle version du package.

Lors du prochain démarrage de l’application par l’utilisateur, le serveur transmet automatiquement la nouvelle version au client. Cette méthode spécifique de mise à niveau d’un package était auparavant appelée mise à niveau active.

## Utilisation d’un serveur de gestion pour la publication et d’un serveur de diffusion en continu


Dans ce scénario, le serveur de gestion App-V est utilisé pour la publication des packages et le serveur de diffusion en continu est utilisé pour les packages et applications de diffusion en continu. Le protocole RTSP (S) est obligatoire. Lorsque le package d’origine est importé sur le serveur de gestion, l’administrateur copie le dossier de package qui contient les fichiers créés par le Sequencer sur le dossier de contenu, par exemple \\\\server\\CONTENT\\packagename. L’administrateur modifie l’entrée HREF dans le fichier OSD pour qu’il pointe sur le fichier SFT sur le serveur en flux continu, puis importe le package sur le serveur de gestion.

Pour configurer le serveur de diffusion en continu, l’administrateur copie le dossier du package à partir du serveur de gestion dans le dossier contenu du serveur de diffusion en continu. Ce dossier doit avoir le même nom et chemin d’accès relatif sous le dossier CONTENT du serveur de diffusion en tant que sur le serveur de gestion, par exemple \\\\streamingserver\\CONTENT\\packagename.

Si le paramètre de source de source d’application (ASR) du client est configuré de manière à pointer sur le serveur de diffusion en continu, le client utilise ce paramètre au lieu du nom du serveur dans l’entrée HREF du fichier OSD. Les champs ISR et OSR sur le client peuvent éventuellement être configurés de manière à pointer sur le serveur de gestion ou le serveur de diffusion en continu, en fonction de l’architecture système spécifique utilisée.

Lorsqu’un utilisateur est authentifié par le serveur de gestion, le serveur publie les applications de l’utilisateur en envoyant le fichier applist.xml au client. Le client récupère les fichiers et icônes d’OSD pour les applications à partir du serveur de diffusion en continu ou du serveur de gestion, en fonction des paramètres dans les champs OSR et ISR.

Lorsque l’utilisateur double-clique sur une icône d’application, le client utilise le chemin d’accès au fichier de contenu du package (SFT) contenu dans l’élément de fichier OSD HREF. Si le système ASR est utilisé, le client remplace le nom du serveur (et le port et le protocole, le cas échéant) dans l’élément HREF par le chemin d’accès du serveur de diffusion spécifié dans ASR. L’application est alors transmise à partir du serveur de diffusion en continu vers le cache du client et est démarrée.

### Pour mettre à niveau le package

Pour ajouter une nouvelle version d’une application qui a été mise à niveau dans le Sequencer App-V, l’administrateur doit copier la nouvelle version du fichier SFT et tout autre fichier modifié dans le même dossier que la version d’origine de l’application sur le serveur de diffusion en continu.

Par souci de cohérence, il est recommandé de copier également les nouveaux fichiers dans le dossier sur le serveur de gestion. Par exemple, si vous utilisez les champs OSR ou ISR du client, copiez le fichier d’OSD et les icônes mis à jour sur le serveur spécifié dans les champs OSR et ISR.

Après que le serveur de diffusion en continu a détecté la nouvelle version, au prochain démarrage de l’application, le serveur transmet automatiquement la nouvelle version au client.

## Utilisation d’un serveur de gestion pour la publication et d’un serveur IIS pour la diffusion en continu


Dans ce scénario, le serveur de gestion App-V est utilisé pour la publication des packages, et le serveur IIS est utilisé pour les packages et applications de diffusion en continu. Lorsque le package d’origine est importé sur le serveur de gestion, l’administrateur copie le dossier de package qui contient les fichiers créés par le Sequencer sur le dossier de contenu, par exemple \\\\server\\CONTENT\\packagename. L’administrateur modifie l’entrée HREF dans le fichier OSD de sorte qu’il pointe vers le fichier SFT sur le serveur IIS, puis importe le package sur le serveur de gestion.

Pour configurer le serveur IIS pour la diffusion en continu, l’administrateur copie le dossier de package du serveur de gestion vers le dossier contenu sur le serveur IIS. Ce dossier doit avoir le même nom et chemin d’accès relatif sous le dossier de contenu Web du serveur IIS, en ce qui concerne le serveur de gestion. par exemple, il est possible d’accéder à l’URL du serveur IIS en utilisant http://IISserver/CONTENT/packagename ou https://IISserver/CONTENT/packagename .

Si le paramètre de racine de l’application du client (ASR) est configuré de manière à pointer sur le serveur IIS, le client utilise le système ASR au lieu du nom du serveur dans l’entrée HREF du fichier OSD. Vous pouvez éventuellement configurer les champs ISR et OSR sur le client de manière à ce qu’ils pointent vers le serveur de gestion ou le serveur IIS, en fonction de l’architecture système spécifique que vous utilisez.

Lorsque le serveur de gestion authentifie l’utilisateur, le serveur publie les applications de l’utilisateur en envoyant le fichier applist.xml au client. Le client récupère les fichiers et icônes d’OSD pour les applications à partir du serveur IIS ou du serveur de gestion, en fonction des paramètres définis dans les champs ISR et OSR.

Lorsque l’utilisateur double-clique sur une icône d’application, le client utilise le chemin d’accès au fichier de contenu du package (SFT) contenu dans l’élément de fichier OSD HREF. Si le système ASR est utilisé, le client remplace le nom du serveur (et le port et le protocole, le cas échéant) dans l’élément HREF par le chemin d’accès du serveur IIS spécifié dans le système ASR. L’application est alors transmise en continu à partir du serveur IIS au cache du client à l’aide du protocole HTTP (S) et est démarré.

### Pour mettre à niveau le package

Pour mettre à niveau le package, procédez comme suit:

-   Copiez la nouvelle version du fichier OSD dans le dossier du serveur de gestion, par exemple \\\\server\\CONTENT\\packagename, et remplacez le fichier OSD existant. Par souci de cohérence, copiez également les fichiers modifiés. Si les champs OSR ou ISR du client sont utilisés, copiez également les icônes et fichiers d’OSD mis à jour vers le serveur spécifié dans les champs OSR et ISR.

-   Copiez la nouvelle version du fichier SFT dans le dossier Package sous le dossier de contenu Web sur le serveur IIS. par exemple, il est possible d’accéder à l’URL du serveur IIS en utilisant http://IISserver/CONTENT/packagename ou https://IISserver/CONTENT/packagename .

Lors de l’actualisation de publication suivante, le client est mis à jour avec la nouvelle version du fichier OSD. Ce fichier pointe désormais vers la nouvelle version du fichier SFT. par conséquent, lorsque l’utilisateur double-clique ensuite sur l’icône d’une application, la nouvelle version est démarrée.

## Utilisation d’un serveur de gestion pour la publication et d’un partage de fichiers pour la diffusion en continu


Dans ce scénario, le serveur de gestion App-V est utilisé pour la publication des packages et le serveur de fichiers est utilisé pour les packages et applications de diffusion en continu. Lorsque le package d’origine est importé sur le serveur de gestion, l’administrateur copie le dossier de package qui contient les fichiers créés par le Sequencer sur le dossier de contenu, par exemple \\\\server\\CONTENT\\packagename. L’administrateur modifie l’entrée HREF dans le fichier OSD de sorte qu’il pointe vers le fichier SFT sur le serveur de fichiers et importe le package sur le serveur de gestion.

Pour configurer le serveur de fichiers pour la diffusion en continu, l’administrateur copie le dossier du package à partir du serveur de gestion dans le dossier contenu du serveur de fichiers. Ce dossier doit avoir le même nom et chemin d’accès relatif sous le dossier de contenu du serveur de fichiers que sur le serveur de gestion, par exemple \\\\fileserver\\CONTENT\\packagename.

Si le paramètre racine de l’application du client (ASR) est configuré de manière à ce qu’il pointe vers le serveur de fichiers à l’aide d’un chemin UNC (par exemple, \\\\fileserver\\content), le client utilise ce paramètre à la place du nom du serveur dans l’entrée HREF du fichier OSD. L’administrateur peut éventuellement configurer les champs ISR et OSR sur le client de manière à ce qu’il pointe vers le serveur de gestion ou le serveur de fichiers, en fonction de l’architecture système spécifique utilisée.

Lorsque le serveur de gestion authentifie l’utilisateur, le serveur publie les applications de l’utilisateur en envoyant le fichier applist.xml au client. Le client récupère les fichiers et icônes d’OSD pour les applications à partir du serveur de fichiers ou du serveur de gestion, en fonction des paramètres définis dans les champs ISR et OSR.

Lorsque l’utilisateur double-clique sur une icône d’application, le client utilise le chemin d’accès au fichier de contenu du package (SFT) contenu dans l’élément de fichier OSD HREF. Si la valeur ASR est utilisée, le client remplace le nom du serveur (et le port et le protocole, le cas échéant) dans l’élément HREF par le chemin d’accès du serveur de fichiers qui est spécifié dans le système ASR. L’application est alors transmise en continu à partir du serveur de fichiers vers le cache client et est démarrée.

### Pour mettre à niveau le package

Pour mettre à niveau le package, procédez comme suit:

-   Copiez la nouvelle version du fichier OSD dans le dossier du serveur de gestion, par exemple \\\\server\\CONTENT\\packagename, en remplaçant le fichier OSD existant. Tout autre fichier modifié doit également être copié par souci de cohérence. Si les champs OSR ou ISR du client sont utilisés, copiez également les icônes et fichiers d’OSD mis à jour vers le serveur spécifié dans les champs OSR et ISR.

-   Copiez la nouvelle version du fichier SFT dans le dossier Package sous le dossier CONTENT sur le serveur de fichiers, par exemple \\\\fileserver\\CONTENT\\packagename. Copiez le fichier V2 SFT dans le dossier du partage de contenu sur le serveur de fichiers, par exemple \\\\fileserver\\CONTENT\\packagename\\V1.

Lors de la prochaine actualisation de publication, le client est mis à jour avec la nouvelle version du fichier OSD. Ce fichier pointe désormais vers une nouvelle version du fichier SFT, et lorsque l’utilisateur double-clique ensuite sur l’icône d’une application, la nouvelle version est démarrée.

## Mise à niveau du package en utilisant le mode de diffusion en continu MSI


Lorsque vous générez un fichier Windows Installer (MSI) lors du séquençage d’un package, le Sequencer crée une. Fichier MSI contenant toutes les informations de publication nécessaires. L’administrateur doit copier le. Fichier MSI au client et au. Fichier SFT contenant le contenu du package vers un partage réseau accessible à partir de l’ordinateur client.

Pour publier l’application sur le client, exécutez la commande suivante sur l’ordinateur client:

   **Msiexec.exe/i \\\\PathToMsi\\packagename.msi MODE = STREAMING OVERRIDEURL = \\\\\\\\server\\share\\package.sft**

Cette. MSP publie les applications sur le client, puis diffuse le fichier. Fichier SFT dans le cache du client.

### Pour mettre à niveau le package

Pour ajouter une nouvelle version, un administrateur doit déployer un nouveau. Fichier MSI au client et nouveau. Fichier SFT sur le partage réseau. L’administrateur doit alors exécuter la même commande utilisée pour déployer le package, mais utiliser le nouveau. Un fichier MSI et le nouveau. Fichier SFT, par exemple:

   **Msiexec.exe/i \\\\PathToMsi\\packagename\_2.msi MODE = STREAMING OVERRIDEURL = \\\\\\\\server\\share\\package\_2.sft**

 

 





