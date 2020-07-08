---
title: Procédure pour modifier la taille de cache et la désignation de lettre de lecteur
description: Procédure pour modifier la taille de cache et la désignation de lettre de lecteur
author: dansimp
ms.assetid: e7d7b635-079e-41aa-a5e6-655f33b4e317
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cf972f114845064ecf3027cf52d1a038dc6a5118
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807346"
---
# Procédure pour modifier la taille de cache et la désignation de lettre de lecteur


Vous pouvez modifier la taille du cache et la désignation de la lettre du lecteur directement à partir du nœud **virtualisation** des applications de la console de gestion du client de virtualisation d’applications.

**Remarque**  
Une fois la taille de cache définie, elle ne peut pas être réduite.



**Pour modifier la taille du cache**

1.  Cliquez avec le bouton droit sur le nœud **Application Virtualization** , puis sélectionnez **Propriétés** dans le menu contextuel.

2.  Dans la boîte de dialogue **Propriétés** , sélectionnez l’onglet **système de fichiers** . Dans la section **paramètres de configuration du cache du client** , cliquez sur l’une des cases d’option suivantes pour choisir le mode de gestion de l’espace de cache:

    **Important**  
    Si vous activez le paramètre **utiliser le seuil d’espace disque disponible** , la valeur que vous entrez définit la taille de cache sur la taille de disque totale moins le nombre de seuils d’espace disque libre que vous avez entré. Si vous souhaitez revenir à l’utilisation du paramètre **utiliser la taille maximale du cache** , vous devez spécifier un nombre plus grand que la taille de cache actuelle. Dans le cas contraire, l’erreur «une nouvelle taille doit être supérieure à la taille de cache existante» s’affiche.



~~~
-   **Use maximum cache size**

    Enter a numeric value from 100 to 1,048,576 (1 TB) in the **Maximum size (MB)** field to specify the maximum size of the cache. The value shown in **Reserved Cache Size** indicates the amount of cache in use.

-   **Use free disk space threshold**

    Enter a numeric value to specify the amount of free disk space, in MB, that the cache must leave available on the disk. This allows the cache to grow until the amount of free disk space reaches this limit. The value shown in **Free disk space remaining** indicates how much disk space is unused.
~~~

3. Cliquez sur **OK** ou sur **appliquer** pour modifier le paramètre.

**Pour modifier la désignation de lettre de lecteur**

1.  Cliquez avec le bouton droit sur le nœud **Application Virtualization** , puis sélectionnez **Propriétés** dans le menu contextuel.

2.  Dans l’onglet **système de fichiers** de la boîte de dialogue **Propriétés** , dans le champ **lecteur à utiliser** , sélectionnez la lettre de lecteur de votre choix dans la liste déroulante des lettres de lecteur disponibles. Ce paramètre est en vigueur au redémarrage de l’ordinateur.

3.  Cliquez sur **OK** ou sur **appliquer** pour modifier le paramètre.

## Rubriques connexes


[Procédure pour configurer le client dans Application Virtualization Client Management Console](how-to-configure-the-client-in-the-application-virtualization-client-management-console.md)









