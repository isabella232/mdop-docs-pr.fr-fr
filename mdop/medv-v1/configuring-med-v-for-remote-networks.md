---
title: Configuration de MED-V pour les réseaux distants
description: Configuration de MED-V pour les réseaux distants
author: dansimp
ms.assetid: 4d2f0081-622f-4a6f-8d73-f8c2108036e0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 328376046ee5213f3d5bb09be7adf8c81f8508b1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811927"
---
# Configuration de MED-V pour les réseaux distants


Vous pouvez configurer MED-V de façon à ce qu’il fonctionne à l’intérieur d’un réseau, à distance ou les deux à l’intérieur du réseau et à distance.

## <a href="" id="bkmk-howtoconfiguremedvtoworkfrominsideanetworkorremotely"></a>


**Pour configurer MED-V de façon à ce qu’il fonctionne à l’intérieur d’un réseau**

-   Configurer un serveur MED-V et une distribution d’image à l’intérieur du réseau.

**Pour configurer MED-V de façon à ce qu’il fonctionne à distance**

1.  Configurer un serveur MED-V et un serveur de distribution d’images accessibles à partir d’Internet.

2.  Le cas échéant, configurez un proxy inverse (également appelé DMZ).

3.  Définissez la méthode d’authentification dans le fichier *ClientSettings.xml* , qui se trouve dans le dossier **Servers\\Configuration Server\\** .

**Pour configurer MED-V de façon à ce qu’il fonctionne à la fois à partir d’un réseau et à distance**

1.  Configurer un serveur et un serveur de distribution d’image MED-V à l’intérieur du réseau.

2.  Assurez-vous que les serveurs sont accessibles à partir d’Internet.

3.  Configuration de la résolution DNS de telle sorte que lorsque le client tente de se connecter à un serveur, il se connecte automatiquement au serveur approprié (au sein du réseau ou via Internet) en fonction de l’emplacement du client.

4.  Le cas échéant, configurez un proxy inverse de réseau de périmètre.

5.  Définissez la méthode d’authentification dans le fichier *ClientSettings.xml* , qui se trouve dans le dossier **Servers\\Configuration Server\\** .

**Remarques**  Le service doit être redémarré lors de l’application de nouveaux paramètres.

 

-   Vous pouvez remplacer le schéma d’authentification IIS par l’une des valeurs suivantes: BASIC, DIGEST, NTLM ou NEGOTIATE. La valeur par défaut est NEGOTIATE et utilise l’entrée suivante:

    ```xml
    <ImageDistribution>
    <!-- The authentication used for image download. Basic and digest authentication should be used only under SSL.-->
       <!-- The line below can be one of the following: -->
       <!--BG_AUTH_SCHEME>BG_AUTH_SCHEME_BASIC</BG_AUTH_SCHEME-->
       <!--BG_AUTH_SCHEME>BG_AUTH_SCHEME_DIGEST</BG_AUTH_SCHEME-->
       <!--BG_AUTH_SCHEME>BG_AUTH_SCHEME_NTLM</BG_AUTH_SCHEME-->
       <!--BG_AUTH_SCHEME>BG_AUTH_SCHEME_NEGOTIATE</BG_AUTH_SCHEME-->
       <Authentication type="Kidaro.Foundation.Bits.BG_AUTH_SCHEME">
          <BG_AUTH_SCHEME>BG_AUTH_SCHEME_NEGOTIATE</BG_AUTH_SCHEME>
       </Authentication>
    </ImageDistribution>
    ```

## Rubriques connexes


[Conception et planification de l'infrastructure de MED-V](med-v-infrastructure-planning-and-design.md)

 

 





