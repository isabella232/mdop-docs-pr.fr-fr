---
title: Configurer les applications et les extensions d’application virtuelle par défaut dans la console de gestion
description: Comment afficher et configurer des applications et des extensions de l’application virtuelle par défaut à l’aide de la console de gestion
author: dansimp
ms.assetid: 1e1941d3-fb22-4077-8ec6-7a0cb80335d8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 09/26/2019
ms.openlocfilehash: 7c29ba0e40cf1adbc2b2297124cfb245a65a7ffe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805928"
---
#   Configurer les applications et les extensions d’application virtuelle par défaut dans la console de gestion

Utilisez la procédure suivante pour *Afficher* et *configurer* les extensions de package par défaut.

**Pour afficher et configurer les extensions d’application virtuelles par défaut**

1.  Pour afficher le package que vous voulez configurer, ouvrez la console de gestion App-V 5,1. Sélectionnez le package que vous voulez configurer, cliquez avec le bouton droit sur le nom du package, puis sélectionnez **modifier la configuration par défaut**.

2.  Pour afficher les applications contenues dans le package spécifié, dans le volet **configuration par défaut** , cliquez sur **applications**. Pour afficher les raccourcis pour ce package, cliquez sur **raccourcis**. Pour afficher les associations de type de fichier pour ce package, cliquez sur **types de fichiers**.

3.  Pour activer les extensions d’application, sélectionnez **activer**.

    Pour activer les raccourcis, sélectionnez **activer les raccourcis**. Pour ajouter un nouveau raccourci pour l’application sélectionnée, cliquez avec le bouton droit sur l’application dans le volet **raccourcis** et sélectionnez **Ajouter un nouveau raccourci**. Pour supprimer un raccourci, cliquez avec le bouton droit sur l’application dans le volet **raccourcis** et sélectionnez **supprimer le raccourci**. Pour modifier un raccourci existant, cliquez avec le bouton droit sur l’application, puis sélectionnez **modifier le raccourci**.

4.  Pour afficher d’autres extensions d’application, cliquez sur **avancé** , puis cliquez sur **Exporter la configuration**. Tapez un nom de fichier, puis cliquez sur **Enregistrer**. Vous pouvez afficher toutes les extensions d’application associées au package à l’aide du fichier de configuration.

5.  Pour modifier les autres extensions de l’application, modifiez le fichier de configuration, puis cliquez sur **Importer et remplacez cette configuration**. Sélectionnez le fichier modifié, puis cliquez sur **ouvrir**. Dans la boîte de dialogue, cliquez sur **remplacer** pour terminer le processus.

>**Remarques** Si le téléchargement échoue et que la taille de votre fichier de configuration est supérieure à 4 Mo, vous devrez augmenter la taille de fichier maximale autorisée par le serveur. Pour cela, il suffit d’ajouter l’attribut maxRequestLength avec une valeur supérieure à la taille de votre fichier de configuration (en Ko) pour l’élément httpRuntime de la ligne 26 `C:\Program Files\Microsoft Application Virtualization Server\ManagementService\Web.config` .  
Par exemple, si `<httpRuntime targetFramework="4.5"/>` vous modifiez la valeur sur pour `<httpRuntime targetFramework="4.5" maxRequestLength="8192"/>` augmenter la taille maximale de 8 Mo


Vous **avez une suggestion pour App-V**? Ajoutez ou Votez en fonction [de suggestions.](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization) **Vous avez un problème lié à l’application-V?** Utilisez le [Forum TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Rubriques connexes


[Opérations d'App-V5.1](operations-for-app-v-51.md)

 

 





