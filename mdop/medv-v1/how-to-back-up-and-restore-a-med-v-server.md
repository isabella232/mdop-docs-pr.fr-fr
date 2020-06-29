---
title: Procédure de sauvegarde et de restauration d'un serveur MED-V
description: Procédure de sauvegarde et de restauration d'un serveur MED-V
author: dansimp
ms.assetid: 8d05e3a4-279b-4ce6-a319-8a09e7a30c60
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d51cfe3727896ed68a1fd67441174a294a1073cc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809744"
---
# Procédure de sauvegarde et de restauration d'un serveur MED-V


Les fichiers XML situés sur le serveur peuvent être sauvegardés, puis restaurés en cas de perte de données sur le serveur.

**Pour sauvegarder un serveur MED-V**

-   Sauvegardez les fichiers suivants situés dans * &lt; INSTALLDIR &gt; \\Servers\\ConfigurationServer*:

    **Remarques**  Si la configuration a été modifiée par défaut, les fichiers peuvent être stockés à un autre emplacement.

     

    -   ClientPolicy.xml

    -   ClientSettings.xml

    -   ConfigurationFiles.xml

    -   OrganizationPolicy.xml

    -   WorkspaceKeys.xml

    **Remarques**  Le fichier ServerSettings.xml peut également être sauvegardé. Toutefois, si une configuration spécifique a été modifiée (par exemple, sur le serveur d’origine, le répertoire des VM pour MED-V se trouve dans «*C:\\Vms*» et ce type d’annuaire n’existe pas sur le nouveau serveur), il est possible qu’elle génère une erreur.

     

**Pour restaurer un serveur MED-V**

1.  Installez un nouveau serveur MED-V.

2.  Copiez les fichiers de sauvegarde dans le répertoire suivant:

    *&lt;InstallDir &gt; \\Servers\\ConfigurationServer*

3.  Redémarrez le service MED-V.

 

 





