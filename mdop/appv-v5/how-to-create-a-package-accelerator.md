---
title: Comment créer un accélérateur de package
description: Comment créer un accélérateur de package
author: dansimp
ms.assetid: dfe305e5-7cf8-498f-9581-4805ffc722bd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0710bff5e5ea420119ac3c395c2e8917f7c582dd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805605"
---
# Comment créer un accélérateur de package


Les accélérateurs de package App-V 5,0 génèrent automatiquement de nouveaux packages d’application virtuelle.

**Remarque**  
Vous pouvez utiliser PowerShell pour créer un accélérateur de package. Pour plus d’informations, reportez-vous [à la rubrique Création d’un accélérateur de package à l’aide de PowerShell](how-to-create-a-package-accelerator-by-using-powershell.md).



Utilisez la procédure suivante pour créer un accélérateur de package.

**Important**  
Les accélérateurs de package peuvent contenir des informations relatives aux mots de passe et aux utilisateurs. Par conséquent, vous devez enregistrer les accélérateurs de packages et le média d’installation associé dans un emplacement sécurisé, et vous devez signer numériquement l’accélérateur de package après l’avoir créé, afin que l’éditeur puisse être vérifié lorsque l’accélérateur de package App-V 5,0 est appliqué.



**Important**  
Avant de commencer la procédure suivante, vous devez effectuer les opérations suivantes:

-   Copiez le package d’application virtuel que vous utiliserez pour créer l’accélérateur de package localement sur l’ordinateur exécutant le Sequencer.

-   Copiez tous les fichiers d’installation requis associés au package d’application virtuelle sur l’ordinateur exécutant le Sequencer.



**Pour créer un accélérateur de package**

1.  **Important**  
    Le Sequencer App-V 5,0 n’accorde aucun droit de licence à l’application logicielle utilisée pour créer l’accélérateur de package. Vous devez vous conformer aux termes du contrat de licence utilisateur final de l’application que vous utilisez. Il est de votre responsabilité de veiller à ce que les termes du contrat de licence de l’application logicielle vous permettent de créer un accélérateur de package à l’aide d’un Sequencer App-V 5,0.



~~~
To start the App-V 5.0 sequencer, on the computer that is running the sequencer, click **Start** / **All Programs** / **Microsoft Application Virtualization** / **Microsoft Application Virtualization Sequencer**.
~~~

2. Pour démarrer l’Assistant Création d’un **accélérateur de package** de l’application-v 5,0, dans la console de Sequencer App-v 5,0, cliquez sur **Outils**  /  **créer un accélérateur**.

3. Dans la page **Sélectionner un package** , pour spécifier un package d’application virtuelle existant à utiliser pour créer l’accélérateur de package, cliquez sur **Parcourir**, puis recherchez le package d’application virtuelle existant (fichier. AppV).

   **Astuce**  
   Copiez les fichiers associés au package d’application virtuel que vous envisagez d’utiliser localement sur l’ordinateur exécutant le Sequencer.



~~~
Click **Next**.
~~~

4. Dans la page **fichiers d’installation** , pour spécifier le dossier contenant les fichiers d’installation que vous avez utilisés pour créer le package d’application virtuelle d’origine, cliquez sur **Parcourir**, puis sélectionnez le répertoire contenant les fichiers d’installation.

   **Astuce**  
   Copiez le dossier contenant les fichiers d’installation requis sur l’ordinateur exécutant le Sequencer.



5. Si l’application est déjà installée sur l’ordinateur exécutant le Sequencer, pour spécifier le fichier d’installation, sélectionnez les **fichiers installés sur le système local**. Pour utiliser cette option, l’application doit déjà être installée dans l’emplacement d’installation par défaut.

6. Dans la page **collecte d’informations** , consultez les fichiers qui n’ont pas été trouvés dans l’emplacement spécifié dans la page fichiers d' **installation** de cet Assistant. Si les fichiers affichés ne sont pas obligatoires, sélectionnez **supprimer ces fichiers**, puis cliquez sur **suivant**. Si les fichiers sont requis, cliquez sur **précédent** , puis copiez les fichiers requis dans le répertoire spécifié dans la page **fichiers d’installation** .

   **Remarque**  
   Vous devez supprimer les fichiers non requis ou cliquer sur **précédent** , puis rechercher les fichiers requis pour passer à la page suivante de l’Assistant.



7. Dans la page **Sélectionner des fichiers** , passez en revue les fichiers qui ont été détectés et effacez les fichiers qui doivent être supprimés de l’accélérateur de package. Sélectionnez uniquement les fichiers nécessaires à l’exécution correcte de l’application, puis cliquez sur **suivant**.

8. Dans la page **verify applications (vérifier les applications** ), vérifiez que tous les fichiers d’installation requis pour générer le package sont affichés. Lorsque l’accélérateur de package est utilisé pour créer un nouveau package, tous les fichiers d’installation affichés dans le volet **applications** sont requis pour créer le package.

   Si nécessaire, pour ajouter d’autres fichiers du programme d’installation, cliquez sur **Ajouter**. Pour supprimer les fichiers d’installation inutiles, sélectionnez le fichier d’installation, puis cliquez sur **supprimer**. Pour modifier les propriétés associées à un programme d’installation, cliquez sur **modifier**. Les fichiers d’installation spécifiés dans cette étape seront nécessaires lorsque l’accélérateur de package sera utilisé pour créer un nouveau package d’application virtuelle. Après confirmation des informations affichées, cliquez sur **suivant**.

9. Dans la page **Sélectionner des recommandations** , pour spécifier un fichier contenant des informations sur la façon dont l’accélérateur de package s’affiche, cliquez sur **Parcourir**. Par exemple, ce fichier peut contenir des informations sur la façon dont l’ordinateur exécutant le Sequencer doit être configuré, les informations requises pour l’application pour les ordinateurs cibles et les notes générales. Vous devez fournir toutes les informations nécessaires à l’application de l’accélérateur de package. Le fichier que vous sélectionnez doit être au format texte enrichi (. rtf) ou fichier texte (. txt). Cliquez sur **Suivant**.

10. Dans la page **créer un accélérateur de package** , pour spécifier l’emplacement d’enregistrement de l’accélérateur de package, cliquez sur **Parcourir** , puis sélectionnez le répertoire.

11. Dans la page **dernière étape** , cliquez sur **Fermer**pour fermer l’Assistant Création d’un **accélérateur de package** .

   **Important**  
   Pour vous assurer que le package Accelerator est le plus sécurisé possible et que l’éditeur puisse être vérifié lors de l’application de l’accélérateur de package, vous devez toujours signer numériquement l’accélérateur de package.



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## Rubriques connexes


[Opérations d'App-V5.0](operations-for-app-v-50.md)

[Comment créer un package d'application virtuelle à l'aide d'un accélérateur de package App-V](how-to-create-a-virtual-application-package-using-an-app-v-package-accelerator.md)









