---
title: Comment configurer le serveur de distribution Web d'images
description: Comment configurer le serveur de distribution Web d'images
author: dansimp
ms.assetid: 2d32ae79-dff5-4c05-a412-dd15452b6007
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 8a21b14fbaca6bbc09d4c35b4d8fb86365c42e3b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810986"
---
# Comment configurer le serveur de distribution Web d'images


Un référentiel d’image est un serveur facultatif utilisé pour la distribution d’images (qui permet aux administrateurs de télécharger de nouvelles images et d’autres ordinateurs clients de vérifier le serveur toutes les 15 minutes et de mettre à jour leur image s’il est disponible).

## <a href="" id="bkmk-configuringanimagereporitoryusingiis"></a>


Pour un serveur de distribution d’images, vous devez disposer des éléments suivants:

-   Internet Information Services (IIS) — pour plus d’informations, voir [Internet Information Services](https://go.microsoft.com/fwlink/?LinkId=142995).

    Pendant l’installation d’IIS, lors de l’ajout de services de rôle, sélectionnez les méthodes d’authentification prises en charge suivantes:

    -   **Authentification de base**

    -   **Authentification Windows**

    -   **Authentification du mappage de certificat client**

    Lorsque vous configurez IIS, incluez les éléments suivants:

    -   Ajoutez un répertoire virtuel avec l’alias nommé **MEDVImages**. Le chemin d’accès physique doit pointer vers l’emplacement des images.

    -   Activez BITS.

    -   Ajoutez les types MIME suivants:

        -   **. CKM (application/octet-stream)**

        -   **. index (application/octet-stream**)

    -   Sur le site MED-V, ajoutez des autorisations de lecture à **tout le monde**.

    -   Redémarrez IIS.

-   Extensions du serveur BITS pour IIS: pour plus d’informations, voir [installer des extensions de serveur bits](https://go.microsoft.com/fwlink/?LinkId=142996).

## Rubriques connexes


[Configurations prises en charge](supported-configurationsmedv-orientation.md)

[Concevoir les référentiel d'images MED-V](design-the-med-v-image-repositories.md)

 

 





