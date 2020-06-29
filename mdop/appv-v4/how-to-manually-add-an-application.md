---
title: Procédure pour ajouter manuellement une application
description: Procédure pour ajouter manuellement une application
author: dansimp
ms.assetid: c635b07a-5c7f-4ab2-ba18-366457146cb9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 868939553fae6172ccca549ddc3f08aa76ee3c56
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806970"
---
# Procédure pour ajouter manuellement une application


Lors de l’ajout d’une application au serveur de gestion de la virtualisation des applications, il est recommandé de l’importer. Vous pouvez ajouter une application manuellement, mais vous devez fournir des informations précises et détaillées sur l’application appelée dans cette section.

**Pour ajouter manuellement une nouvelle application**

1.  Dans le volet gauche, cliquez avec le bouton droit sur le nœud **applications** et sélectionnez **nouvelle application**.

2.  Dans l' **Assistant Nouvelle application**, complétez la boîte de dialogue **informations générales** :

    1.  **Nom**de l’application: tapez le nom que vous voulez que les utilisateurs voient.

    2.  **Version**: tapez la version de l’application.

    3.  **Activée**: cette case doit être cochée pour diffuser l’application en continu après sa création.

    4.  **Description**: tapez éventuellement une description pour une utilisation administrative.

    5.  **Chemin d’accès**de l’OSD: Naviguez sur le réseau jusqu’au fichier Open Software Descriptor (OSD) de l’application. Ce fichier doit se trouver dans un dossier réseau partagé.

    6.  **Path d’icône**: Naviguez jusqu’au fichier. ico de l’application.

    7.  **Groupe de licences d’application**: Si vous avez configuré des groupes de licences, vous pouvez les affecter à un en le sélectionnant dans la liste déroulante.

    8.  **Groupe de serveurs**: Si vous disposez de plusieurs serveurs de virtualisation des applications, vous pouvez leur affecter une en le sélectionnant dans la liste déroulante.

3.  Cliquez sur **Suivant**.

4.  Dans la boîte de dialogue **Sélectionner un package** , sélectionnez le package associé, puis cliquez sur **suivant**.

5.  Dans l’écran **raccourcis clavier publiés** , activez les cases à cocher des emplacements dans lesquels vous souhaitez que les raccourcis des applications apparaissent sur les ordinateurs clients, puis cliquez sur **suivant**.

6.  Dans l’écran **associations de fichiers** , vous pouvez ajouter de nouvelles associations de fichiers de type à cette application. Pour cela, cliquez sur **Ajouter**, entrez l’extension (sans point précédent), entrez une description, puis cliquez sur **OK**.

7.  Cliquez sur **Suivant**.

8.  Dans la boîte de dialogue **autorisations d’accès** , cliquez sur **Ajouter**.

9.  Dans la boîte de dialogue **Ajouter/modifier un groupe d’utilisateurs** , accédez au groupe d’utilisateurs. Vous pouvez également entrer le domaine et le groupe en entrant les informations dans les champs correspondants. Lorsque vous avez terminé, cliquez sur **OK**. Vous pouvez ajouter d’autres groupes aux mêmes pages.

10. Cliquez sur **Suivant**.

11. Dans l’écran **Résumé** , vous pouvez consulter les paramètres d’importation. Cliquez sur **Terminer** pour ajouter l’application, cliquez sur **précédent** pour modifier les informations ou cliquez sur **Annuler**.

## Rubriques connexes


[Procédure pour gérer des applications dans Server Management Console](how-to-manage-applications-in-the-server-management-console.md)

 

 





