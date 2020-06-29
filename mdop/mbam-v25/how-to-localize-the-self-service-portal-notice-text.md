---
title: Comment localiser le texte d'avis du portail libre-service
description: Comment localiser le texte d'avis du portail libre-service
author: dansimp
ms.assetid: a4c878b7-e5c8-45af-a537-761bb2991659
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a2385f6b00713e7373bd1707b02324b80f300c0d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811921"
---
# Comment localiser le texte d'avis du portail libre-service


Vous pouvez configurer le texte des notifications localisées pour qu’ils apparaissent par défaut aux utilisateurs finaux sur le portail libre-service. Le fichier Notice.txt qui affiche le texte de l’avis figure dans le répertoire racine suivant:

&lt;Répertoire d’installation *de MBAM self-service* &gt; \\Self service Website\\

Pour afficher un texte d’avis localisé, vous devez créer un fichier Notice.txt localisé, puis l’enregistrer sous un dossier de langue spécifique dans le répertoire de l’exemple suivant:

&lt;Répertoire d’installation *de MBAM self-service* &gt; \\Self service Website\\

**Remarques**  Vous pouvez configurer le chemin d’accès à l’aide de l’élément **NoticeTextPath** dans les paramètres de l' **application**.

 

MBAM affiche le texte de l’avis en fonction des règles suivantes:

-   Si vous créez un fichier **Notice.txt** localisé dans le dossier de langue approprié, MBAM affiche le texte du message localisé si le fichier **Notice.txt** par défaut existe. Si le fichier **Notice.txt** par défaut est manquant, un message s’affiche, indiquant que le fichier par défaut est manquant.

-   Si MBAM ne trouve pas de version localisée du fichier Notice.txt, il affiche le texte dans le fichier de Notice.txt par défaut.

-   Si MBAM ne trouve pas de fichier Notice.txt par défaut, il affiche le texte par défaut dans le portail libre-service.

**Remarques**  Si le navigateur d’un utilisateur final est défini sur une langue qui ne possède pas de sous-dossier de langue correspondant ou Notice.txt, le texte du fichier Notice.txt dans le répertoire racine suivant s’affiche:

&lt;Répertoire d’installation *de MBAM self-service* &gt; \\Self service Website\\

 

**Pour créer un fichier Notice.txt localisé**

1.  Sur le serveur sur lequel vous avez configuré le portail libre-service, créez un &lt; *Language* &gt; dossier de langue dans l’exemple d’annuaire suivant, où &lt; *Language* &gt; représente le nom de la langue localisée:

    &lt;Répertoire d’installation *de MBAM self-service* &gt; \\Self service Website\\

    **Remarques**  Certains dossiers de langue existent déjà, il est donc possible que vous n’ayez pas à créer de dossier. Si vous avez besoin de créer un dossier de langue, reportez-vous à la rubrique référence sur l' [API NLS (National Language Support)](https://go.microsoft.com/fwlink/?LinkId=317947) pour obtenir la liste des noms valides que vous pouvez utiliser pour le &lt; dossier *Language* &gt; .

     

2.  Créez un fichier Notice.txt contenant le texte d’avis localisé.

3.  Enregistrez le fichier Notice.txt dans le &lt; dossier *Language* &gt; . Par exemple, pour créer un fichier Notice.txt localisé en espagnol, enregistrez le fichier de Notice.txt localisé dans le répertoire de l’exemple suivant:

    &lt;Répertoire d’installation *de MBAM self-service* &gt; \\Self service Website\\Es-es

    Le nom du dossier Language peut également être le nom neutre des langues **au lieu** de **es-es**. Si le navigateur de l’utilisateur final est défini sur **es-es** et que ce dossier n’existe pas, les paramètres régionaux du parent (tels qu’ils sont définis dans .net) sont récupérés et activés de manière récursive, ce qui a\\SelfServiceWebsite\\es\\Notice.txt pour effet d’arrêter &lt; &gt; le fichier de Notice.txt par défaut. Cette substitution récursive imite les règles de chargement des ressources .NET.



## Rubriques connexes


[Personnalisation du portail libre-service de votre organisation](customizing-the-self-service-portal-for-your-organization.md)

 

## Vous avez une suggestion pour MBAM?
- Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring) 
- Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





