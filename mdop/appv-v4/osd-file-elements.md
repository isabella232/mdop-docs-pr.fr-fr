---
title: Éléments du fichier OSD
description: Éléments du fichier OSD
author: dansimp
ms.assetid: 8211b562-7549-4331-8321-144f52574e99
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a8e3ebcf53ff39ecd2ef7ad0feec0bbbcae199db
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806574"
---
# Éléments du fichier OSD


Le répertoire d’installation de Sequencer contient un fichier de schéma XML, **Softricity. xsd**, qui définit la structure valide d’un fichier d’OSD (Open Software Descriptor). Voici quelques-uns des éléments d’OSD les plus fréquemment utilisés.

<a href="" id="softpkg"></a>SOFTPKG  
Élément racine du fichier OSD contenant tous les éléments définissant le package logiciel.

<a href="" id="codebase"></a>CODE base  
Des informations sur le fichier. SFT pour ce package, notamment les attributs HREF, FILENAME et GUID. Vous pouvez modifier l’attribut HREF si vous modifiez le point de distribution de ce package particulier.

<a href="" id="os"></a>Système d’exploitation  
Définit sur quels systèmes d’exploitation cette application peut s’exécuter en fonction de valeurs initialement définies dans l’Assistant séquençage. Cette valeur ne peut contenir que les valeurs définies dans **Softricity. xsd**.

<a href="" id="local-interaction-allowed"></a>_INTERACTION \ LOCAL \ _ALLOWED  
Valeur définie sur TRUE, cette option permet de créer des objets nommés (événements, mutexes, sémaphores, mappages de fichiers et mailslots) et d’objets COM dans l’espace de noms global plutôt que d’être isolés au sein d’un environnement virtuel particulier, ce qui permet aux applications virtuelles d’interagir avec les applications du système d’exploitation hôte.

Exemple: &lt; implémentation de SOFTPKG &gt; &lt;&gt;

&lt;&gt; &lt; stratégies VIRTUALENV&gt;

&lt;LOCAL \ _INTERACTION \ _ALLOWED &gt; vrai

&lt;/LOCAL\ _INTERACTION \ _ALLOWED&gt;

&lt;/POLICIES &gt; &lt; /VIRTUALENV&gt;

&lt;/IMPLEMENTATION &gt; &lt; /SOFTPKG&gt;

<a href="" id="dependencies"></a>Liens  
Définit la composition de la suite dynamique (dépendances par rapport à d’autres packages) en utilisant une balise de code base à partir d’un autre package.

Exemple: &lt; &gt; &lt; codebase Dependencies href = "RTSP://Server/Package.sft" GUID = "7579F4DF-2461-4219-BD43-494E1FDC69E3" SYSGUARDFILE = "pkg. 1 \ \ osguard. CP" size = "6572748" obligatoire = "false"/ &gt; &lt; /Dependencies&gt;

<a href="" id="package-name"></a>NOM DU PACKAGE  
Nom courant du package entré dans la page d' **informations sur le package** de l’Assistant séquençage, qui vous permet de spécifier un nom unique pour une application séquencée contenant plusieurs applications.

<a href="" id="title"></a>DROITS  
Nom descriptif facultatif de l’application que vous séquençage.

<a href="" id="abstract"></a>EXTRACTION  
Brève description du programme logiciel entré dans le champ **Commentaires** de **la page de** l’Assistant séquençage. Il est recommandé de spécifier des informations telles que le système d’exploitation et le niveau de service du poste de travail, la version Sequencer et le nom de l’ingénieur de séquençage.

<a href="" id="script"></a>SCRIPT  
Définit des événements de script spécifiques qui se produisent au démarrage, à l’arrêt ou en flux continu.

<a href="" id="mgmt-shortcutlist"></a>GESTION DES _SHORTCUTLIST  
Liste de tous les raccourcis définis dans l’Assistant.

<a href="" id="mgmt-fileassociations"></a>GESTION DES _FILEASSOCIATIONS  
Liste des types de fichiers spécifiés dans l’Assistant.

## Rubriques connexes


[À propos de l'onglet OSD](about-the-osd-tab.md)

 

 





