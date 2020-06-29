---
title: Procédure d'utilisation de la composition de suite dynamique
description: Procédure d'utilisation de la composition de suite dynamique
author: dansimp
ms.assetid: 24147feb-a0a8-4791-a8e5-cbe5fe13c762
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3bff4c9721352785cf6db5c497234ceaa3c5e448
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806698"
---
# Procédure d'utilisation de la composition de suite dynamique


La composition de suite dynamique dans la virtualisation d’application vous permet de définir une application comme étant dépendante d’une autre application, telle qu’un middleware ou un plug-in. Cela permet à l’application d’interagir avec le middleware ou le plug-in dans l’environnement virtuel, en règle générale, ce problème est empêché. Cela est utile, car un package d’application secondaire peut être utilisé avec plusieurs autres applications, appelées *applications principales*, qui permettent à chaque application principale de référencer le même package secondaire.

Vous pouvez utiliser la composition suite dynamique quand vous séquencez des applications qui dépendent de plug-ins tels que des contrôles ActiveX ou des applications qui dépendent de middleware tels qu’OLE DB ou Java Runtime Environment (JRE). Si chaque application ayant utilisé ces composants dépendants a requis le séquençage, y compris les composants, les mises à jour apportées à ces composants nécessiteront de nouveau le séquençage de toutes les applications principales. Si vous avez séquencé les principales applications sans les composants, puis séquencé le middleware ou le plug-in en tant que package secondaire, seul le package secondaire doit être mis à jour.

L’un des avantages de cette approche réside dans le fait qu’elle permet de réduire la taille des packages principaux. Un autre avantage réside dans le fait qu’il vous permet de mieux contrôler les autorisations d’accès aux applications secondaires. Notez que l’application secondaire peut être diffusée de façon régulière et qu’elle n’a pas besoin d’être complètement mise en cache pour s’exécuter.

Un package principal peut avoir plusieurs packages secondaires. Toutefois, un seul niveau de dépendance est pris en charge, de sorte que vous ne pouvez pas définir un package secondaire comme dépendant d’un autre package secondaire. Par ailleurs, l’application secondaire peut uniquement être middleware ou un plug-in et ne peut pas être un autre produit logiciel complet.

Si vous envisagez de rendre différentes applications principales dépendantes d’un seul produit middleware, assurez-vous que vous testez cette configuration pour déterminer l’impact potentiel sur les performances système avant de procéder au déploiement.

**Important**  Les dépendances de package peuvent être spécifiées comme obligatoires pour une application principale. Si un package secondaire est marqué comme obligatoire et ne peut pas être utilisé pour une raison quelconque lors du chargement, le chargement du package secondaire échoue. Par ailleurs, l’application principale ne fonctionnera pas si l’utilisateur essaie de la démarrer.

 

Vous pouvez utiliser les procédures suivantes pour créer un package secondaire, pour un plug-in ou un composant middleware, puis vous pouvez utiliser la procédure finale pour définir la dépendance dans le fichier OSD du package secondaire.

**Pour créer un package secondaire pour un plug-in à l’aide de la composition suite dynamique**

1.  Sur un ordinateur de séquençage configuré avec une image saine, installez le Sequencer Application Virtualization et enregistrez l’état de l’ordinateur.

2.  Séquencez l’application principale, puis enregistrez le package dans le dossier Content sur le serveur.

3.  Restaurez l’ordinateur de séquençage à son état d’enregistrement à partir de l’étape 1.

4.  Installez et configurez l’application principale localement sur l’ordinateur de séquençage.

    **Important**  Vous devez spécifier une nouvelle racine de package pour le package secondaire.

     

5.  Démarrez la phase de contrôle de Sequencer.

6.  Installez le plug-in sur l’ordinateur de séquençage et configurez-le selon vos besoins.

7.  Ouvrez l’application principale, puis vérifiez que le plug-in fonctionne correctement.

8.  Dans la console de Sequencer, créez une application factice pour représenter le package secondaire qui contient le plug-in et sélectionnez une icône.

9.  Enregistrez le package dans le dossier Content du serveur.

    **Remarques**  Pour vous aider à gérer les packages secondaires, il est recommandé que le nom du package inclue le terme «package secondaire» pour insister sur qu’il s’agit d’un package qui ne fonctionne pas comme une application autonome (par exemple, **\ [nom de connexion \] package secondaire**).

     

**Pour créer un package secondaire pour le middleware à l’aide de la composition suite dynamique**

1.  Sur un ordinateur de séquençage configuré avec une image saine, installez le Sequencer Application Virtualization et enregistrez l’état de l’ordinateur.

2.  Installez le middleware localement sur l’ordinateur de séquençage et configurez-le.

3.  Séquencez l’application principale, puis enregistrez le package dans le dossier Content sur le serveur.

4.  Restaurez l’ordinateur de séquençage à son état d’enregistrement à partir de l’étape 1.

5.  Démarrez le Sequencer pour créer un package.

6.  Démarrez la phase de contrôle de Sequencer.

7.  Installez l’application middleware sur l’ordinateur de séquençage et configurez-la comme dans une installation classique.

8.  Terminez le processus de séquençage.

9.  Enregistrez le package dans le dossier Content du serveur.

    **Remarques**  Pour vous aider à gérer les packages secondaires, il est recommandé que le nom du package inclue le terme «package secondaire» pour insister sur qu’il s’agit d’un package qui ne fonctionnera pas comme une application autonome (par exemple, **\ [nom du middleware \] package secondaire**).

     

**Pour définir la dépendance dans le package principal**

1. Sur le serveur, ouvrez le fichier OSD du package secondaire à des fins de modification. (Il est recommandé d’utiliser un éditeur XML pour apporter des modifications au fichier OSD; Toutefois, vous pouvez utiliser le bloc-notes comme alternative.)

2. Copiez la ligne **href de base** de ce fichier.

3. Ouvrez le fichier OSD du package principal à des fins de modification.

4. Insérez la <strong> &lt; &gt; </strong> balise Dependencies après la fermeture de la balise ** &lt; /ENVLIST &gt; ** à la fin de la section ** &lt; VIRTUALENV &gt; ** juste avant la balise ** &lt; /VIRTUALENV &gt; ** .

5. Collez la ligne **href du code base** à partir du package secondaire après la balise de ** &lt; &gt; dépendances** que vous venez de créer.

6. S’il s’agit d’un package obligatoire, ce qui signifie qu’il doit être démarré avant le démarrage du package principal, ajoutez la propriété **obligatoire = «true»** dans la balise de **code base** . Si ce n’est pas obligatoire, la propriété peut être omise.

7. Fermez la balise ** &lt; Dependencies &gt; ** en insérant ce qui suit:

   **&lt;/DEPENDENCIES&gt;**

8. Passez en revue les modifications que vous avez apportées au fichier OSD, puis enregistrez et fermez le fichier. L’exemple suivant montre comment la section ajoutée doit apparaître. Par exemple, les valeurs des balises affichées sont uniquement disponibles.

   **&lt;VIRTUALENV&gt;**

        **&lt;ENVLIST&gt;**

   **…**

        **&lt;/ENVLIST&gt;**

        **&lt;DEPENDENCIES&gt;**

             **&lt;CODEBASE HREF="rtsp://virt\_apps/package.1/package.1.sft" GUID="D54C80FA-9DFF-459D-AA33-DD852C9FBFBA" SYSGUARDFILE="package.1\\osguard.cp"/&gt;**

             **&lt;CODEBASE HREF="rtsp://sample\_apps/package.2/sample.sft" GUID="D54C80FA-9DFF-459D-AA33-DD852C9FBFBA" SYSGUARDFILE="package.2\\osguard.cp" MANDATORY="TRUE" /&gt;**

        **&lt;/DEPENDENCIES&gt;**

   **&lt;/VIRTUALENV&gt;**

9. Si le package secondaire comporte des entrées dans la section ** &lt; ENVLIST &gt; ** du fichier OSD, vous devez copier ces entrées dans la même section du package principal.

## Rubriques connexes


[Comment créer ou mettre à niveau des applications virtuelles à l’aide du Sequencer App-V](how-to-create-or-upgrade-virtual-applications-using--the-app-v-sequencer.md)

 

 





