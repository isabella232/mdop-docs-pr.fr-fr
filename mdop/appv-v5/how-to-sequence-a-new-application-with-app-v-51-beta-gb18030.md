---
title: Comment séquencer une nouvelle application avec App-V5.1
description: Comment séquencer une nouvelle application avec App-V5.1
author: dansimp
ms.assetid: 7d7699b1-0cb8-450d-94e7-5af937e16c21
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 43edd9357e31f4884ed7baec3d35fa01bf2abe54
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805185"
---
# Comment séquencer une nouvelle application avec App-V5.1


**Pour revoir ou faire avant de commencer à effectuer le séquençage**

1.  Déterminez le type de package d’application virtualisé que vous souhaitez créer:

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Type d’application</th>
    <th align="left">Description</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Standard</p></td>
    <td align="left"><p>Crée un package qui contient une application ou une suite d’applications. Il s’agit de l’option la plus appropriée pour la plupart des types d’applications.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Module complémentaire ou plug-in</p></td>
    <td align="left"><p>Crée un package qui étend les fonctionnalités d’une application standard, par exemple un plug-in pour Microsoft Excel. De plus, vous pouvez utiliser les plug-ins pour les applications installées en mode natif ou pour un autre package lié à l’aide de groupes de connexion.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Intergiciels</p></td>
    <td align="left"><p>Crée un package requis par une application standard, par exemple Java. Les packages middleware permettent de créer des liens vers d’autres packages à l’aide de groupes de connexion.</p></td>
    </tr>
    </tbody>
    </table>



2.  Copiez tous les fichiers d’installation requis sur l’ordinateur exécutant le Sequencer.

3.  Créez une image de sauvegarde de votre environnement virtuel avant de séquencer une application, puis revenez à cette image dès que vous avez fini de Sequencer une application.

4.  Passez en revue les éléments suivants:

    -   Si un programme d’installation de l’application modifie l’accès de sécurité à un fichier ou un répertoire existant nouveau ou existant, ces modifications ne sont pas capturées dans le package.

    -   Si des chemins d’accès courts ont été désactivés pour le volume cible du package virtualisé, vous devez également le faire sur un volume qui a été créé et dont la trajectoire courte est désactivée. Ne peut pas être le volume système.

> [!NOTE]  
> Le Sequencer App-V 5. x ne peut pas séquencer des applications avec des noms de fichier correspondant à «CO_ &lt; x &gt; », où x est une valeur numérique. Le 0x8007139F d’erreur est généré.

**Pour séquencer une nouvelle application standard**

1.  Sur l’ordinateur qui exécute le Sequencer, cliquez sur **tous les programmes**, puis sur **virtualisation d’application Microsoft**, puis sur **Sequencer Microsoft Application Virtualization**.

2.  Dans le Sequencer, cliquez sur **créer un nouveau package d’application virtuel**. Sélectionnez **créer un package (par défaut)**, puis cliquez sur **suivant**.

3.  Sur la page **préparer l’ordinateur** , passez en revue les problèmes qui peuvent entraîner l’échec de la création du package ou amener le package à contenir des données inutiles. Vous devriez résoudre tous les problèmes potentiels avant de continuer. Après avoir effectué des corrections, cliquez sur **Actualiser** pour afficher les informations mises à jour. Lorsque vous avez résolu tous les problèmes potentiels, cliquez sur **suivant**.

    > [!IMPORTANT]
    > Si vous êtes tenu de désactiver le logiciel antivirus, vous devez d’abord analyser l’ordinateur qui exécute le Sequencer pour vous assurer qu’aucun fichier non souhaité ou malveillant ne peut être ajouté au package.



~~~
> [!NOTE]  
> There is currently no way to disable Windows Defender in Windows 10. If you receive a warning, you can safely ignore it. It is unlikely that Windows Defender will affect sequencing at all.
~~~



4. Dans la page **type d’application** , activez la case à cocher **application standard (par défaut)** , puis cliquez sur **suivant**.

5. Dans la page **Sélectionner le programme d’installation** , cliquez sur **Parcourir** , puis spécifiez le fichier d’installation de l’application.

   > [!NOTE]  
   > Si le programme d’installation de l’application spécifiée modifie l’accès de sécurité à un fichier ou un répertoire, existant ou nouveau, les modifications associées ne seront pas capturées dans le package.



~~~
If the application does not have an associated installer file and you plan to run all installation steps manually, select the **Perform a Custom Installation** check box, and then Click **Next**.
~~~

6. Dans la page **nom du package** , tapez un nom qui sera associé au package. Utilisez un nom qui permet d’identifier l’objet et la version de l’application qui sera ajoutée au package. Le nom du package s’affiche dans la console de gestion App-V 5,0.

   Cliquez sur **Suivant**.

7. Dans la page d' **installation** , lorsque le processus de séquence et de programme d’installation de l’application est prêt, vous pouvez poursuivre l’installation de l’application afin que le Sequencer puisse surveiller le processus d’installation.

   > [!IMPORTANT]
   > Vous devez toujours installer des applications à un emplacement sécurisé et vérifier qu’aucun utilisateur n’est connecté à l’ordinateur exécutant le Sequencer lors de l’analyse.



~~~
Use the application's installation process to perform the installation. If additional installation files must be run as part of the installation, click **Run** to locate and run the additional installation files. When you are finished with the installation, select **I am finished installing**. Click **Next**.
~~~

8. Dans la page **installation** , attendez que le Sequencer configure le package de l’application virtualisée.

9. Sur la page **configurer le logiciel** , exécutez éventuellement les programmes contenus dans le package. Cette étape vous permet d’effectuer toutes les tâches de configuration ou de licence nécessaires avant de déployer et d’exécuter le package sur des ordinateurs cibles. Pour exécuter tous les programmes en une seule fois, sélectionnez au moins un programme, puis cliquez sur **exécuter tout**. Pour exécuter des programmes spécifiques, sélectionnez le ou les programmes, puis cliquez sur **exécuter la sélection**. Effectuez les tâches de configuration requises, puis fermez les applications. Il est possible que vous deviez patienter quelques minutes pour que tous les programmes s’exécutent.

   > [!NOTE]  
   > Pour exécuter les tâches de première utilisation pour toutes les applications qui ne sont pas disponibles dans la liste, ouvrez l’application. Les informations associées seront capturées au cours de cette étape.



~~~
Click **Next**.
~~~

10. Dans la page **rapport d’installation** , vous pouvez passer en revue les informations relatives au package d’application virtualisé que vous venez de séquencer. Dans **informations supplémentaires**, double-cliquez sur un événement pour obtenir des informations plus détaillées. Pour continuer, cliquez sur **suivant**.

11. La page **personnaliser** s’affiche. Si vous avez terminé l’installation et la configuration de l’application virtuelle, sélectionnez **arrêter maintenant** et passez directement à l’étape 14 de cette procédure. Pour effectuer l’une des personnalisations suivantes, sélectionnez **personnaliser**.

    -   Préparez le package virtuel pour la diffusion en continu. La diffusion en continu améliore son fonctionnement lorsque le package d’application virtuelle est exécuté sur les ordinateurs cibles.

    -   Spécifiez les systèmes d’exploitation qui peuvent exécuter ce package.

    Cliquez sur **Suivant**.

12. Sur la page de **diffusion** , exécutez chaque programme de manière à optimiser son exécution et son exécution plus efficacement sur les ordinateurs cibles. L’exécution de toutes les applications peut prendre quelques minutes. Après l’exécution de toutes les applications, fermez chacune d’elles, puis cliquez sur **suivant**.

   > [!NOTE]  
   > Si vous n’ouvrez aucune application au cours de cette étape, la méthode de diffusion en continu par défaut est remise en continu à la demande. Cela signifie que les applications sont téléchargées sur un bit pour pouvoir être ouvertes, puis en fonction de la configuration du chargement en arrière-plan, le reste de l’application sera chargé.



13. Dans la page **cible du système d’exploitation** , spécifiez les systèmes d’exploitation qui peuvent exécuter ce package. Pour permettre à tous les systèmes d’exploitation pris en charge dans votre environnement d’exécuter ce package, sélectionnez **permettre l’exécution de ce package sur tout système d’exploitation**. Pour configurer ce package de sorte qu’il ne s’exécute que sur des systèmes d’exploitation spécifiques, sélectionnez **autoriser ce package à s’exécuter uniquement sur les systèmes d’exploitation suivants** et sélectionnez les systèmes d’exploitation qui peuvent exécuter ce package. Cliquez sur **Suivant**.

   > [!IMPORTANT]
   > Assurez-vous que les systèmes d’exploitation que vous spécifiez ici sont pris en charge par l’application que vous séquençage.



14. La page **créer un package** s’affiche. Pour modifier le package sans l’enregistrer, sélectionnez **continuer pour modifier le package sans l’enregistrer à l’aide de l’éditeur de package**. Cette option ouvre le package dans la console de Sequencer de sorte que vous puissiez modifier le package avant son enregistrement. Cliquez sur **Suivant**.

   Pour enregistrer le package immédiatement, sélectionnez **enregistrer le package maintenant** (par défaut). Ajoutez des **Commentaires** facultatifs à associer au package. Les commentaires sont utiles pour identifier la version du programme ainsi que d’autres informations sur le package.

   > [!IMPORTANT]
   > Le système ne prend pas en charge les caractères non imprimables dans les **Commentaires** et les **descriptions**.



~~~
The default **Save Location** is also displayed on this page. To change the default location, click **Browse** and specify the new location. Click **Create**.
~~~

15. La page de **fin** s’affiche. Passez en revue les informations du volet **rapport de package d’application virtuel** selon vos besoins, puis cliquez sur **Fermer**. Ces informations sont également disponibles dans le fichier **Report.xml** situé dans le répertoire où le package a été créé.

   Le package est désormais disponible dans le Sequencer.

   > [!IMPORTANT]
   > Une fois que vous avez créé un package d’application virtuelle, vous ne pouvez pas exécuter le package d’application virtuel sur l’ordinateur exécutant le Sequencer.



**Pour séquencer une application de complément ou une application enfichable**

1. > [!NOTE]  
   > Avant d’exécuter la procédure suivante, installez l’application parente localement sur l’ordinateur exécutant le Sequencer. Ou si l’application parent est virtualisée, vous pouvez suivre les étapes décrites dans le flux de travail du module complémentaire ou du plug-in pour décompresser l’application parent sur l’ordinateur.
   >
   > Par exemple, si vous séquençagez un plug-in pour Microsoft Excel, installez Microsoft Excel localement sur l’ordinateur exécutant le Sequencer. Installez également l’application parente dans le même répertoire où l’application est installée sur les ordinateurs cibles. Si le plug-in ou le complément doit être utilisé avec un package d’application virtuelle existant, installez l’application sur le même lecteur d’application virtuel que celui utilisé lors de la création du package d’application virtuelle parent.



~~~
On the computer that runs the sequencer, click **All Programs**, and then Click **Microsoft Application Virtualization**, and then click **Microsoft Application Virtualization Sequencer**.
~~~

2. *<strong><em>Dans le Sequencer, cliquez sur * </em> créer un nouveau package d’application virtuel </strong> . Sélectionnez **créer un package (par défaut)**, puis cliquez sur **suivant**.

3. Sur la page **préparer l’ordinateur** , passez en revue les problèmes qui peuvent entraîner l’échec de la création du package ou entraînent l’affichage de données inutiles par le package. Vous devriez résoudre tous les problèmes potentiels avant de continuer. Après avoir effectué des corrections, cliquez sur **Actualiser** pour afficher les informations mises à jour. Lorsque vous avez résolu tous les problèmes potentiels, cliquez sur **suivant**.

   > [!IMPORTANT]
   > Si vous êtes tenu de désactiver le logiciel antivirus, vous devez d’abord analyser l’ordinateur qui exécute le Sequencer pour vous assurer qu’aucun fichier non souhaité ou malveillant ne peut être ajouté au package.



4. Dans la page **type d’application** , sélectionnez **composant additionnel ou plug-in**, puis cliquez sur **suivant**.

5. Dans la page **Sélectionner le programme d’installation** , cliquez sur **Parcourir** , puis spécifiez le fichier d’installation de l’extension ou du plug-in. Si le module complémentaire ou le plug-in n’a pas de fichier d’installation associé et que vous envisagez d’exécuter toutes les étapes d’installation manuellement, activez la case à cocher **activer cette option pour effectuer une installation personnalisée** , puis cliquez sur **suivant**.

6. Dans la page principale de l' **installation** , assurez-vous que l’application principale est installée sur l’ordinateur qui exécute le Sequencer. Vous pouvez également développer un package existant qui a été enregistré localement sur l’ordinateur qui exécute le Sequencer. Pour cela, cliquez sur **développer le package**, puis sélectionnez le package. Après avoir développé ou installé le programme parent, sélectionnez **j’ai installé le programme parent principal**.

   Cliquez sur **Suivant**.

7. Dans la page **nom du package** , tapez un nom qui sera associé au package. Utilisez un nom qui permet d’identifier l’objet et la version de l’application qui sera ajoutée au package. Le nom du package s’affiche dans la console de gestion App-V 5,0.

   Cliquez sur **Suivant**.

8. Dans la page **installation** , lorsque le Sequencer et le programme d’installation de l’application sont prêts, vous pouvez procéder à l’installation du plug-in ou de l’application de complément de sorte que le Sequencer puisse surveiller le processus d’installation. Utilisez le processus d’installation de l’application pour procéder à l’installation. Si des fichiers d’installation supplémentaires doivent être exécutés dans le cadre de l’installation, cliquez sur **exécuter** et recherchez et exécutez les fichiers d’installation supplémentaires. Lorsque l’installation est terminée, sélectionnez J’ai **terminé d’installer**, puis cliquez sur **suivant**.

9. Dans la page **rapport d’installation** , vous pouvez consulter les informations relatives au package d’application virtuel que vous venez de créer. Pour obtenir une explication plus détaillée des informations affichées dans **informations supplémentaires**, double-cliquez sur l’événement. Après avoir consulté les informations, cliquez sur **suivant**.

10. La page **personnaliser** s’affiche. Si vous avez terminé l’installation et la configuration de l’application virtuelle, sélectionnez **arrêter maintenant** et passez directement à l’étape 12 de cette procédure. Pour effectuer l’une des personnalisations suivantes, sélectionnez **personnaliser**.

    -   Optimiser la façon dont le package s’exécutera sur un réseau lent ou peu fiable.

    -   Spécifiez les systèmes d’exploitation qui peuvent exécuter ce package.

    Cliquez sur **Suivant**.

11. Sur la page de **diffusion** , exécutez chaque programme de manière à optimiser son exécution et son exécution plus efficacement sur les ordinateurs cibles. La diffusion en continu améliore son fonctionnement lorsque le package d’application virtuelle est exécuté sur des ordinateurs cibles sur des réseaux à latence élevée. L’exécution de toutes les applications peut prendre quelques minutes. Après l’exécution de toutes les applications, fermez chacune des applications. Vous pouvez également configurer le package de manière à ce qu’il soit entièrement téléchargé avant ouverture en activant la case à cocher **forcer le téléchargement des applications** . Cliquez sur **Suivant**.

    > [!NOTE]  
    > Le cas échéant, vous pouvez empêcher le chargement d’une application au cours de cette étape. Dans la boîte de dialogue lancement de l' **application** , cliquez sur **arrêter** et sélectionnez l’une des cases à cocher: **arrêter toutes les applications** ou **arrêter cette application uniquement**.



12. Dans la page **cible du système d’exploitation** , spécifiez les systèmes d’exploitation qui peuvent exécuter ce package. Pour permettre à tous les systèmes d’exploitation pris en charge dans votre environnement d’exécuter ce package, activez la case à cocher **autoriser ce package à s’exécuter sur tous les systèmes d’exploitation** . Pour configurer ce package de sorte qu’il ne s’exécute que sur des systèmes d’exploitation spécifiques, activez la case à cocher **autoriser ce package à s’exécuter uniquement sur les systèmes d’exploitation suivants** , puis sélectionnez les systèmes d’exploitation qui peuvent exécuter ce package. Cliquez sur **Suivant**.

13. La page **créer un package** s’affiche. Pour modifier le package sans l’enregistrer, sélectionnez **continuer pour modifier le package sans l’enregistrer à l’aide de la** case à cocher éditeur de package. Cette option ouvre le package dans la console de Sequencer de sorte que vous puissiez modifier le package avant son enregistrement. Cliquez sur **Suivant**.

    Pour enregistrer le package immédiatement, sélectionnez **enregistrer le package maintenant**. Vous pouvez également ajouter une **Description** qui sera associée au package. Les descriptions sont utiles pour identifier la version et d’autres informations sur le package.

    > [!IMPORTANT]
    > Le système ne prend pas en charge les caractères non imprimables dans les commentaires et les descriptions.



~~~
The default **Save Location** is also displayed on this page. To change the default location, click **Browse** and specify the new location. Click **Create**.
~~~

**Pour séquencer une application middleware**

1. Sur l’ordinateur qui exécute le Sequencer, cliquez sur **tous les programmes**, puis sur **virtualisation d’application Microsoft**, puis sur **Sequencer Microsoft Application Virtualization**.

2. *<strong><em>Dans le Sequencer, cliquez sur * </em> créer un nouveau package d’application virtuel </strong> . Sélectionnez **créer un package (par défaut)**, puis cliquez sur **suivant**.

3. Sur la page **préparer l’ordinateur** , passez en revue les problèmes qui peuvent entraîner l’échec de la création du package ou amener le package à contenir des données inutiles. Vous devriez résoudre tous les problèmes potentiels avant de continuer. Après avoir effectué des corrections, cliquez sur **Actualiser** pour afficher les informations mises à jour. Lorsque vous avez résolu tous les problèmes potentiels, cliquez sur **suivant**.

   > [!IMPORTANT]
   > Si vous avez besoin de désactiver le logiciel antivirus, vous devez commencer par analyser l’ordinateur qui exécute le Sequencer App-V 5,0 pour vous assurer qu’aucun fichier non souhaité ou malveillant ne peut être ajouté au package.



4. Dans la page **type d’application** , sélectionnez **middleware**, puis cliquez sur **suivant**.

5. Dans la page **Sélectionner le programme d’installation** , cliquez sur **Parcourir** , puis spécifiez le fichier d’installation de l’application. Si l’application n’a pas de fichier d’installation associé et que vous envisagez d’exécuter toutes les étapes d’installation manuellement, activez la case à cocher **activer cette option pour effectuer une installation personnalisée** , puis cliquez sur **suivant**.

6. Dans la page **nom du package** , tapez un nom qui sera associé au package. Utilisez un nom qui permet d’identifier l’objet et la version de l’application qui sera ajoutée au package. Le nom du package s’affiche dans la console de gestion App-V 5,0.

   Cliquez sur **Suivant**.

7. Dans la page **installation** , lorsque le programme d’installation de Sequencer et de l’application middleware est prêt, vous pouvez continuer à installer l’application afin que le Sequencer puisse surveiller le processus d’installation. Utilisez le processus d’installation de l’application pour procéder à l’installation. Si des fichiers d’installation supplémentaires doivent être exécutés dans le cadre de l’installation, cliquez sur **exécuter**pour rechercher et exécuter les fichiers d’installation supplémentaires. Lorsque l’installation est terminée, activez la case à cocher **je suis fin** de l’installation, puis cliquez sur **suivant**.

8. Dans la page **installation** , attendez que le Sequencer configure le package d’application virtuelle.

9. Dans la page **rapport d’installation** , vous pouvez consulter les informations relatives au package d’application virtuel que vous venez de séquencer. Dans **informations supplémentaires**, double-cliquez sur un événement pour obtenir des informations plus détaillées. Pour continuer, cliquez sur **suivant**.

10. Dans la page **cible du système d’exploitation** , spécifiez les systèmes d’exploitation qui peuvent exécuter ce package. Pour permettre à tous les systèmes d’exploitation pris en charge dans votre environnement d’exécuter ce package, activez la case à cocher **autoriser ce package à s’exécuter sur tous les systèmes d’exploitation** . Pour configurer ce package de sorte qu’il ne s’exécute que sur des systèmes d’exploitation spécifiques, activez la case à cocher **autoriser ce package à s’exécuter uniquement sur les systèmes d’exploitation suivants** et sélectionnez les systèmes d’exploitation qui peuvent exécuter ce package. Cliquez sur **Suivant**.

11. Dans la page **créer un package** s’affiche. Pour modifier le package sans l’enregistrer, sélectionnez **continuer pour modifier le package sans l’enregistrer à l’aide de l’éditeur de package**. Cette option ouvre le package dans la console de Sequencer de sorte que vous puissiez modifier le package avant son enregistrement. Cliquez sur **Suivant**.

    Pour enregistrer le package immédiatement, sélectionnez **enregistrer le package maintenant**. Vous pouvez également ajouter une **Description** à associer au package. Les descriptions sont utiles pour identifier la version du programme ainsi que d’autres informations sur le package.

    > [!IMPORTANT]
    > Le système ne prend pas en charge les caractères non imprimables dans les commentaires et les descriptions.



~~~
The default **Save Location** is also displayed on this page. To change the default location, click **Browse** and specify the new location. Click **Create**.
~~~

12. La page de **fin** s’affiche. Passez en revue les informations du volet **rapport de package d’application virtuel** selon vos besoins, puis cliquez sur **Fermer**. Ces informations sont également disponibles dans le fichier **Report.xml** qui se trouve dans le répertoire spécifié à l’étape 11 de cette procédure.

   Le package est désormais disponible dans le Sequencer. Pour modifier les propriétés du package, cliquez sur **modifier \ [nom du package \]**.

   > [!IMPORTANT]
   > Une fois que vous avez créé un package d’application virtuelle, vous ne pouvez pas exécuter le package d’application virtuel sur l’ordinateur exécutant le Sequencer.



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## Rubriques connexes


[Opérations d'App-V5.1](operations-for-app-v-51.md)









