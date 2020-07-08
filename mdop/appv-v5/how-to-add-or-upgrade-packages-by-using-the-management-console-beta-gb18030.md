---
title: Comment ajouter ou mettre à jour des packages à l’aide de la console de gestion
description: Comment ajouter ou mettre à jour des packages à l’aide de la console de gestion
author: dansimp
ms.assetid: 4e389d7e-f402-44a7-bc4c-42c2a8440573
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 583ac07168c44c7d0a605b81512ae01a6d979db2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805749"
---
# Comment ajouter ou mettre à jour des packages à l’aide de la console de gestion


Vous pouvez effectuer la procédure suivante pour ajouter ou mettre à niveau un package vers la console de gestion App-V 5,0. Pour mettre à niveau un package déjà existant dans la console de gestion, procédez comme suit et importez le package mis à niveau en utilisant le même **nom**de package.

**Pour ajouter un package à la console de gestion**

1.  Cliquez sur l’onglet **packages** dans le volet de navigation de l’écran de la console de gestion.

    La console affiche la liste des packages qui ont été ajoutés au serveur ainsi que des informations d’État sur chaque package. La sélection d’un package permet d’afficher des informations détaillées sur le package dans le volet **packages** .

    Cliquez sur la zone de liste déroulante **dissociée** et spécifiez le mode d’affichage des packages dans la console. Vous pouvez également cliquer sur l’en-tête de colonne associé pour trier les packages.

2.  Pour spécifier le package que vous voulez ajouter, cliquez sur **Ajouter ou mettre à niveau des packages**.

3.  Tapez le chemin d’accès complet au package que vous voulez ajouter. Utilisez le format de chemin d’accès UNC ou HTTP (par exemple, **\\\\servername\\sharename\\foldername\\packagename.AppV** ou), puis **http://server.1234/file.appv** cliquez sur **Ajouter**.

    **Important**  Vous devez sélectionner un package avec l’extension de nom de fichier **. AppV** .

     

4.  La page affiche le message d' **état &lt; ajouter &gt; PackageName**. Cliquez sur **importer le statut** pour vérifier l’état d’un package que vous avez importé.

    Cliquez sur **OK** pour ajouter le package et fermer la page **Ajouter un package** . S’il y a eu une erreur lors de l’importation, cliquez sur **Détails** dans la page **importation du package** pour plus d’informations. Le package que vous venez d’ajouter est désormais disponible dans le volet **packages** .

5.  Cliquez sur **Fermer** pour fermer la page **Ajouter ou mettre à niveau des packages** .

    Vous **avez une suggestion pour App-V**? Ajoutez ou Votez en fonction [de suggestions.](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization) **Vous avez un problème lié à l’application-V?** Utilisez le [Forum TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Rubriques connexes


[Opérations d'App-V5.0](operations-for-app-v-50.md)

 

 





