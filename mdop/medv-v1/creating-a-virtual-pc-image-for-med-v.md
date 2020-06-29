---
title: Création d'une image Virtual PC pour MED-V
description: Création d'une image Virtual PC pour MED-V
author: dansimp
ms.assetid: 5e02ea07-25b9-41a5-a803-d70c55eef586
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 84e45f9ff7213abdd6288bcd750238436d3ab68c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810091"
---
# Création d'une image Virtual PC pour MED-V


Pour créer une image Virtual PC (VPC) pour MED-V, vous devez effectuer les opérations suivantes:

1.  [Créer une image de VPC](#bkmk-creatingavirtualmachinebyusingmicrosoftvirtualpc).

2.  [Installez le package MED-V Workspace. msi sur l’image VPC](#bkmk-howtoinstallthemedvworkspacemsipackage).

3.  [Exécutez l’outil de configuration de l’ordinateur virtuel MED-V sur l’image VPC](#bkmk-howtorunthevirtualmachineprerequisitestool).

4.  [Configurez manuellement les composants requis pour les machines virtuelles sur l’image VPC](#bkmk-howtoconfiguremedvvirtualmachinemanualinstallationprerequisites).

5.  [Configurez Sysprep pour les images MED-V](#bkmk-howtoconfiguresysprepformedvimages) (facultatif).

6.  [Désactivez Microsoft Virtual PC](#bkmk-turningoffmicrosoftvirtualpc).

## <a href="" id="bkmk-creatingavirtualmachinebyusingmicrosoftvirtualpc"></a>Création d’une image Virtual PC à l’aide de Microsoft Virtual PC


Pour créer une image Virtual PC à l’aide de Microsoft Virtual PC, reportez-vous à la documentation sur le PC virtuel.

Pour plus d'informations, reportez-vous aux éléments suivants:

-   [Aide sur Windows Virtual PC](https://go.microsoft.com/fwlink/?LinkId=182378)

-   [Créer une machine virtuelle et installer un système d’exploitation invité](https://go.microsoft.com/fwlink/?LinkId=182379)

## <a href="" id="bkmk-howtoinstallthemedvworkspacemsipackage"></a>Installer le package MED-V Workspace. msi


Une fois l’image du PC virtuel créée, installez le package MED-V Workspace. msi sur l’image.

**Pour installer l’image d’espace de travail MED-V**

1.  Démarrez l’ordinateur virtuel et copiez le package MED-V Workspace. msi dans.

    Le package MED-V Workspace. msi est appelé *MED-V\_workspace\_x.msi*, où *x* correspond au numéro de version.

    Par exemple, *MED-V\_workspace\_1.0.65.msi*.

2.  Double-cliquez sur le package MED-V Workspace. msi, puis suivez les instructions de l’Assistant installation.

    **Remarque**  
    Lorsque vous relâchez une nouvelle version MED-V et qu’une image virtuelle de votre PC est mise à jour, désinstallez le package d’espace de travail MED-V de l’ordinateur existant, redémarrez l’ordinateur, puis installez le nouveau package MED-V Workspace. msi.



~~~
**Note**  
After the MED-V workspace .msi package is installed, other products that replace GINA cannot be installed.
~~~



## <a href="" id="bkmk-howtorunthevirtualmachineprerequisitestool"></a>Exécution de l’outil Configuration requise pour les machines virtuelles


L’outil Configuration requise pour machine virtuelle (VM) est un assistant qui permet d’automatiser plusieurs des éléments requis.

**Remarque**  
Bien que de nombreux paramètres soient configurables dans l’Assistant, les propriétés requises pour le bon fonctionnement de MED-V ne sont pas configurées.



**Pour exécuter l’outil Configuration requise pour les machines virtuelles**

1.  Une fois le package d’espace de travail MED-V installé, dans le menu **Démarrer** de Windows, sélectionnez **tous les programmes &gt; &gt; **.

    **Remarque**  
    L’utilisateur exécutant l’outil Configuration requise pour les machines virtuelles doit disposer de droits d’administrateur local et doit être le seul utilisateur connecté.



~~~
The **MED-V VM Prerequisite Wizard Welcome** page appears.
~~~

2. Cliquez sur **Suivant**.

3. Dans la page **Paramètres Windows** , à partir des propriétés configurables suivantes, sélectionnez celles que vous souhaitez configurer:

   -   **Effacement des informations de l’historique personnel de l’utilisateur**

   -   **Vider le répertoire temporaire des profils locaux**

   -   **Désactiver les sons sur les événements Windows suivants: démarrage, ouverture de session**

   **Remarque**  
   Ne l’activez pas dans une stratégie de groupe.



4. Cliquez sur **Suivant**.

5. Dans la page **paramètres d’Internet Explorer** , à partir des propriétés configurables suivantes, sélectionnez celles que vous souhaitez configurer:

   -   **Ne pas utiliser les fonctionnalités de saisie semi-automatique**

   -   **Désactiver la réutilisation de Windows pour les raccourcis de lancement**

   -   **Effacer l’historique de navigation**

   -   **Activation de la navigation par onglets dans Internet Explorer 7**

6. Cliquez sur **Suivant**.

7. Dans la page **services Windows** , à partir des propriétés configurables suivantes, sélectionnez celles que vous souhaitez configurer:

   -   **Service du centre de sécurité**

   -   **Service du planificateur de tâches**

   -   **Service mises à jour automatiques**

   -   **Service de restauration du système**

   -   **Service d’indexation**

   -   **Configuration automatique sans fil**

   -   **Compatibilité rapide du changement d’utilisateur**

8. Cliquez sur **Suivant**.

9. Dans la page de **connexion automatique Windows** , procédez comme suit:

   1.  Cochez la case **activer la connexion automatique Windows** .

   2.  Attribuez un **nom d’utilisateur** et un **mot de passe**.

10. Cliquez sur **appliquer**, puis, dans la boîte de confirmation qui s’affiche, cliquez sur **Oui**.

11. Dans la page **Résumé** , cliquez sur **Terminer** pour quitter l’Assistant.

**Remarque**  
Vérifiez que les stratégies de groupe n’écrasent pas les paramètres obligatoires définis dans l’outil éléments requis.



## <a href="" id="bkmk-howtoconfiguremedvvirtualmachinemanualinstallationprerequisites"></a>Comment configurer les conditions préalables à l’installation manuelle de l’ordinateur virtuel MED-V


Plusieurs configurations ne peuvent pas être configurées par le biais de l’outil Configuration requise pour les machines virtuelles et doivent être effectuées manuellement.

-   Paramètres d’ordinateur virtuel

    Il est recommandé de configurer les paramètres d’ordinateur virtuel suivants dans la console Microsoft Virtual PC:

    -   Désactivez les lecteurs de disquette.

    -   Désactivez annuler-Disks (**paramètres d' &gt; annulation de paramètres**).

    -   Assurez-vous que l’image est dotée d’un seul processeur virtuel.

    -   Éliminez les interactions entre la machine virtuelle et l’utilisateur, où elles ne sont pas liées aux applications publiées (par exemple, les messages nécessitant des entrées de l’utilisateur).

-   Paramètres d’image

    Configurez les paramètres manuels suivants dans l’image:

    1.  Dans la fenêtre **Propriétés de Power Options** , désactivez l’option mise en veille prolongée.

    2.  Appliquez les mises à jour Windows les plus récentes.

    3.  Dans la boîte de dialogue **démarrage et récupération de Windows** , dans la section **échec du système** , décochez la case **redémarrer automatiquement** .

    4.  Assurez-vous que l’image utilise une clé de licence VLK.

-   Installation des compléments VPC

    Dans le menu **action** , sélectionnez **installer ou mettre à jour les compléments d’ordinateurs virtuels**.

-   Configuration de l’impression

    Vous pouvez configurer l’impression à partir de l’espace de travail MED-V de l’une des façons suivantes:

    -   Ajoutez une imprimante à l’ordinateur virtuel.

    -   Autorisez l’impression avec les imprimantes configurées sur l’ordinateur hôte.

## <a href="" id="bkmk-howtoconfiguresysprepformedvimages"></a>Configuration de Sysprep pour les images MED-V


Dans un espace de travail MED-V, Sysprep peut être configuré afin d’affecter un ID de sécurité unique, en particulier lorsque plusieurs espaces de travail MED-V sont exécutés sur un seul ordinateur. Il n’est pas recommandé d’utiliser Sysprep pour rejoindre un domaine. au lieu de cela, utilisez l’action de script de participation de l’utilisateur MED-V, comme décrit dans [la rubrique Configurer les actions de script](how-to-set-up-script-actions.md).

**Remarque**  
Sysprep est l’utilitaire de préparation système de Microsoft pour le système d’exploitation Windows.



**Pour configurer Sysprep dans un espace de travail MED-V**

1.  Créez un répertoire à la racine du lecteur système nommé *Sysprep*.

2.  Sur le CD d’installation Windows, extrayez les *deploy.cab* à la racine du lecteur système ou téléchargez la mise à jour des outils de déploiement les plus récents à partir du site Web de Microsoft.

    -   Pour Windows 2000, voir [mise à jour des outils de déploiement pour windows 2000](https://go.microsoft.com/fwlink/?LinkId=143001).

    -   Pour Windows XP, voir [mise à jour des outils de déploiement pour Windows XP](https://go.microsoft.com/fwlink/?LinkId=143000).

3.  Exécutez **le gestionnaire d’installation** (setupmgr.exe).

4.  Suivez la procédure de l’Assistant gestion de l’installation.

Une fois Sysprep configuré et l’espace de travail MED-V créé, Sysprep doit être exécuté.

**Pour exécuter Sysprep**

1.  À partir du dossier Sysprep situé à la racine du lecteur système, exécutez l’outil de préparation du système (Sysprep.exe).

2.  Dans la boîte de message d’avertissement qui s’affiche, cliquez sur **OK**.

3.  Dans la boîte de dialogue **Propriétés de Sysprep** , activez la case à cocher **ne pas réinitialiser le délai de grâce pour l’activation** et utiliser la **mini-installation** .

4.  Cliquez sur **refermer**.

5.  Si vous n’êtes pas satisfait des informations indiquées dans la boîte de dialogue de confirmation qui s’affiche, cliquez sur **Annuler** et modifiez les sélections.

6.  Cliquez sur **OK** pour finaliser le processus de préparation du système.

## <a href="" id="bkmk-turningoffmicrosoftvirtualpc"></a>Désactivation de Microsoft Virtual PC


Une fois tous les composants installés et configurés, fermez Microsoft Virtual PC et sélectionnez **éteindre**.

## Rubriques connexes


Création d’une image MED-V [Comment configurer des actions de script](how-to-set-up-script-actions.md)









