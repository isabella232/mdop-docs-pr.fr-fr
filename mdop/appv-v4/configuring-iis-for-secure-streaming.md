---
title: Configuration d'IIS pour la diffusion en continu sécurisé
description: Configuration d'IIS pour la diffusion en continu sécurisé
author: dansimp
ms.assetid: 9a80a703-4642-4bec-b7af-dc7cb6b76925
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 724fd247d98c265421cea13f4b91c97049a2b4d4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809023"
---
# Configuration d'IIS pour la diffusion en continu sécurisé


Avec la version 4,5 de Microsoft Application Virtualization (App-V), vous pouvez utiliser HTTP et HTTPs en tant que protocoles pour la diffusion de packages d’application en continu vers les clients App-V. Cette option permet aux organisations d’exploiter l’évolutivité supplémentaire proposée par les services Internet (IIS). Lorsque vous utilisez IIS en tant que serveur de diffusion en continu, vous pouvez sécuriser les communications entre le client et le serveur en utilisant HTTPs au lieu de HTTP.

**Remarques**  Si vous voulez diffuser des applications à partir d’un serveur de fichiers, vous devez améliorer la sécurité des communications vers les packages d’application. Pour cela, vous pouvez utiliser le protocole IPsec. Pour plus d’informations, reportez-vous aux rubriques suivantes dans la bibliothèque TechNet:

-   Pour Windows Server2003, <https://go.microsoft.com/fwlink/?LinkId=133226>

-   Pour Windows Server 2008, <https://go.microsoft.com/fwlink/?LinkId=133227>

 

## Types MIME


Lorsque vous utilisez IIS pour diffuser des applications virtuelles à l’aide de HTTP ou HTTPs, pour prendre en charge l’application-V, vous devez ajouter les types MIME suivants au serveur IIS:

-   . OSD = TXT

-   . SFT = binaire

Pour plus d’informations sur l’ajout de types MIME, utilisez les Articles de la base de connaissances suivants:

6,0 IIS: <https://go.microsoft.com/fwlink/?LinkId=151973>

7,0 IIS: <https://go.microsoft.com/fwlink/?LinkId=151977>

## Authentification Kerberos


Lorsque vous utilisez l’authentification HTTP ou HTTPs et Kerberos pour diffuser des fichiers. ICO, OSD ou SFT, vous renforcez la sécurité de votre environnement. Toutefois, pour qu’IIS prenne en charge l’authentification Kerberos, vous devez configurer un nom de principal de service approprié (SPN). L' `setspn.exe` outil est disponible pour Windows Server2003 à partir des outils de support sur le CD d’installation et est intégré à Windows Server 2008.

Pour créer un SPN, exécutez `setspn.exe` à partir d’une invite de commandes lorsque vous êtes connecté en tant que membre du groupe administrateurs de domaine (par exemple,) `setspn.exe –A HTTP/FQDN of Server ServerName` .

## Rubriques connexes


[Configuration de Management ou Streaming Server pour sécuriser les communications post-installation](configuring-management-or-streaming-server-for-secure-communications-post-installation.md)

 

 





