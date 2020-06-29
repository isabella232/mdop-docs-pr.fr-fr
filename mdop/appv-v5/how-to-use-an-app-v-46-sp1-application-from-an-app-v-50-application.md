---
ms.reviewer: ''
title: Utiliser une application application-V 4,6 à partir d’une application App-V 5,0
description: Utiliser une application application-V 4,6 à partir d’une application App-V 5,0
ms.assetid: 4e78cb32-9c8b-478e-ae8b-c474a7e42487
author: msfttracyp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: 8b29e861b97d18e427f6a8247a1f731be2dc0889
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805131"
---
# Utiliser une application application-V 4,6 à partir d’une application App-V 5,0

*Remarque:** App-V 4,6 a quitté la version standard du support technique. Les éléments suivants s’appliquent à un package App-V 4,6 SP3.

Utilisez la procédure suivante pour exécuter une application App-V 4.6 avec des applications App-V 5,0 sur un client autonome.

**Pour exécuter des applications sur un client autonome**

1.  Sélectionnez deux applications dans votre environnement qui peuvent être ouvertes les unes des autres. Par exemple, Microsoft Outlook et Adobe Acrobat Reader. Vous pouvez accéder à une pièce jointe de message électronique créée à l’aide d’Adobe Acrobat.

2.  Convertir les packages, ou créer un package pour l’une de ces applications à l’aide du format App-V 5,0. Pour plus d’informations sur la conversion des packages, voir [Comment migrer des points d’extension d’un package App-v 4,6 vers un package App-v 5,0 pour tous les utilisateurs sur un ordinateur spécifique](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-50-package-for-all-users-on-a-specific-computer.md) ou [Comment migrer des points d’extension d’un package app-v 4,6 vers app-v 5,0 pour un utilisateur spécifique](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-50-for-a-specific-user.md).

3.  Ajoutez et mettez en service le package à l’aide de la console de gestion App-V 5,0. Pour plus d’informations sur l’ajout et la mise à jour des packages, voir [Ajout ou mise à niveau](how-to-add-or-upgrade-packages-by-using-the-management-console-beta-gb18030.md) de packages à l’aide de la console de gestion et configuration de l' [accès aux packages à l’aide de la console de gestion](how-to-configure-access-to-packages-by-using-the-management-console-50.md).

4.  L’application convertie s’exécute désormais avec App-V 5,0, et vous pouvez ouvrir une application à partir de l’autre. Par exemple, si vous avez converti un package Microsoft Office en un package App-V 5,0 et qu’Adobe Acrobat s’exécute toujours en tant que package App-V 4.6, vous pouvez ouvrir une pièce jointe Adobe Acrobat Reader à l’aide de Microsoft Outlook.

    Vous **avez une suggestion pour App-V**? Ajoutez ou Votez en fonction [de suggestions.](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization) **Vous avez un problème lié à l’application-V?** Utilisez le [Forum TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Rubriques connexes


[Opérations d'App-V5.0](operations-for-app-v-50.md)

 

 








