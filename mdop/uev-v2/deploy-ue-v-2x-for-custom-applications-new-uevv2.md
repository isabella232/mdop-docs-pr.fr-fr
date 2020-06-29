---
title: Déployer UE-V 2. x pour des applications personnalisées
description: Déployer UE-V 2. x pour des applications personnalisées
author: dansimp
ms.assetid: f7cb089f-d764-4a93-82b6-926fe0385a23
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 07/19/2016
ms.openlocfilehash: 217f647d948df016c4a6b72736669c2b3305b705
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810535"
---
# Déployer UE-V 2. x pour des applications personnalisées


Microsoft User Interface Virtualization (UE-V) 2,0. 2,1 et 2,1 SP1 utilisent des fichiers XML appelés **modèles d’emplacement des paramètres** pour surveiller et synchroniser les paramètres des applications de bureau et les paramètres de bureau Windows entre les ordinateurs des utilisateurs. Par défaut, certains modèles d’emplacement de paramètres sont inclus dans UE-V. Toutefois, si vous voulez synchroniser les paramètres des applications de bureau autres que celles incluses dans les modèles par défaut, vous pouvez créer vos propres modèles d’emplacement des paramètres personnalisés à l’aide du générateur UE-V.

Une fois que vous avez lu le document de planification dans [préparer un déploiement UE-V 2. x](prepare-a-ue-v-2x-deployment-new-uevv2.md) et que vous avez décidé de synchroniser les paramètres pour des applications personnalisées (tierce partie, métier, etc.), vous déploierez les fonctionnalités d’UE-v comme décrit dans cette rubrique. Pour commencer, Voici les principales étapes à suivre pour synchroniser les paramètres des applications personnalisées:

-   [Installer le générateur de UEV](#uevgen)

    Utilisez le générateur de UEV pour créer des modèles de localisation de paramètres XML personnalisés.

-   [Configurer un catalogue de modèles de paramètres UE-V](#deploycatalogue)

    Vous pouvez définir ce chemin d’accès à l’emplacement de stockage des modèles d’emplacement des paramètres personnalisés.

-   [Créer des modèles d’emplacement des paramètres personnalisés](#createcustomtemplates)

    Ces modèles personnalisés permettent aux utilisateurs de synchroniser les paramètres des applications personnalisées.

-   [Déployer les modèles d’emplacement des paramètres personnalisés](#deploycustomtemplates)

    Après avoir testé le modèle personnalisé pour vous assurer que les paramètres sont correctement synchronisés, vous pouvez déployer ces modèles de l’une des façons suivantes:

    -   Par le biais de votre infrastructure de déploiement existante, telle que Configuration Manager;

    -   En utilisant les préférences de stratégie de groupe

    -   [Déployer un catalogue de modèles de paramètres UE-V](#deploycatalogue)

    **Remarques**  Les modèles déployés à l’aide d’un ESD ou d’une stratégie de groupe doivent être enregistrés auprès d’UE-V Windows Management Instrumentation (WMI) ou Windows PowerShell.

     

## Préparer le déploiement d’UE-V 2. x pour des applications personnalisées


Avant de commencer à déployer les fonctionnalités d’UE-V qui gèrent les applications personnalisées, vous avez quelques points à revoir.

### Générateur UE-V

Le générateur UE-V analyse une application afin de détecter et de capturer les emplacements où l’application stocke ses paramètres. L’application surveillée doit être une application classique. Vous utilisez le générateur UE-V pour créer des modèles d’emplacement des paramètres, mais il ne peut pas créer de modèle d’emplacement de paramètres à partir des types d’applications suivants:

-   Applications virtualisées

-   Applications proposées via les services Terminal Server

-   Applications Java

-   Applications Windows  

**Remarques**  Les modèles d’emplacement des paramètres d’UE-V ne peuvent pas être créés à partir d’applications virtuelles ou d’applications de services Terminal Server. Toutefois, les paramètres qui sont synchronisés à l’aide des modèles peuvent être appliqués à ces applications. Pour créer des modèles qui prennent en charge les applications VDI (Virtual Desktop Infrastructure) et Terminal Services, ouvrez une version du package Windows Installer (. msi) de l’application à l’aide du générateur UE-V. Pour plus d’informations sur les paramètres de synchronisation des applications virtuelles, voir [utilisation de UE-V 2. x avec les applications de virtualisation des](using-ue-v-2x-with-application-virtualization-applications-both-uevv2.md)applications.

 

**Emplacements exclus:** Le processus de découverte exclut les emplacements qui stockent fréquemment les fichiers de logiciels d’application qui ne synchronisent pas correctement les paramètres entre les ordinateurs des utilisateurs ou les environnements informatiques. Par défaut, celles-ci sont exclues:

-   HKEY \ _CURRENT \ _USER clés de Registre et les fichiers auxquels l’utilisateur connecté ne peut pas écrire de valeurs

-   HKEY \ _CURRENT \ _USER clés de Registre et fichiers associés à la fonctionnalité principale du système d’exploitation Windows.

-   Toutes les clés de Registre se trouvant dans la ruche du _MACHINE HKEY \ _LOCAL

-   Fichiers situés dans les répertoires de fichiers du programme

-   Fichiers situés dans les utilisateurs \ \ \ [nom d’utilisateur \] \ \ AppData \ \ LocalLow

-   Fichiers du système d’exploitation Windows situés dans% SystemRoot%

Si les clés de Registre et les fichiers qui sont stockés dans des emplacements exclus sont requis pour synchroniser les paramètres d’application, vous pouvez ajouter manuellement les emplacements au modèle d’emplacement paramètres pendant le processus de création de modèle.
Toutefois, seules _CURRENT les modifications apportées à la ruche du _USER

### Remplacer les modèles Microsoft par défaut

L’agent UE-V installe un groupe par défaut de modèles d’emplacements de paramètres pour les applications Microsoft courantes et les paramètres Windows. Si vous personnalisez ces modèles ou créez des modèles d’emplacement des paramètres pour synchroniser les paramètres des applications personnalisées, l’agent UE-V peut être configuré de manière à utiliser un catalogue de modèles de paramètres pour stocker les modèles. Dans ce cas, vous devez inclure les modèles par défaut ainsi que les modèles personnalisés dans le catalogue de modèles de paramètres.

Lorsque vous [déployez un agent UE-V](https://technet.microsoft.com/library/dn458891.aspx#agent), vous pouvez utiliser le paramètre de ligne `RegisterMSTemplates` de commande pour désactiver l’inscription des modèles Microsoft par défaut.

Lorsque vous utilisez une stratégie de groupe pour configurer le chemin du catalogue de modèles de paramètres, vous pouvez choisir de remplacer les modèles Microsoft par défaut. Si vous configurez les paramètres de stratégie pour remplacer les modèles Microsoft par défaut, tous les modèles Microsoft par défaut installés par l’agent UE-V sont supprimés et seuls les modèles figurant dans le catalogue de modèles paramètres sont utilisés. Le paramètre de configuration de l’agent UE-V `RegisterMSTemplates` doit être défini sur *true* pour pouvoir remplacer le modèle Microsoft par défaut.

**Remarques**  Si vous désactivez ce paramètre de stratégie une fois qu’il est activé, l’agent UE-V ne restaure pas les modèles Microsoft par défaut.

 

S’il existe des modèles personnalisés dans le catalogue de modèles de paramètres qui utilisent le même IDENTIFIant que les modèles Microsoft par défaut, et que l’agent UE-V n’est pas configuré pour remplacer les modèles Microsoft par défaut, les modèles Microsoft ne sont pas pris en compte.

Vous pouvez également remplacer les modèles par défaut en utilisant les fonctionnalités de Windows PowerShell UE-V. Pour remplacer le modèle Microsoft par défaut par Windows PowerShell, annulez l’enregistrement de tous les modèles Microsoft par défaut, puis enregistrez les modèles personnalisés.

**Remarques**  Les packages d’anciens paramètres restent dans l’emplacement de stockage des paramètres même si vous déployez de nouveaux modèles d’emplacement pour une application. Ces packages ne sont pas lus par l’agent, mais aucun d’eux n’est automatiquement supprimé.

 

## <a href="" id="uevgen"></a>Installez le générateur UEV 2. x


Pour créer un modèle d’emplacement des paramètres personnalisés, installez le générateur de 2,0 de Microsoft User Interface Virtualization (UE-V) sur un ordinateur que vous pouvez utiliser. Les applications doivent être installées sur l’ordinateur pour pouvoir générer les modèles d’emplacement des paramètres personnalisés.

**Pour installer le générateur UE-V**

1.  En tant qu’utilisateur disposant de droits d’administrateur local, recherchez le fichier d’installation du générateur UE-V **ToolSetup.exe** fourni avec le logiciel UE-v. Ou, si vous connaissez l’architecture de l’ordinateur, vous pouvez exécuter le fichier Windows Installer (. msi) approprié, **ToolsSetupx64.msi** ou **ToolsSetupx86.msi**.

2.  Double-cliquez sur le fichier d’installation. L’Assistant de configuration du générateur de la virtualisation de l’utilisation de l’utilisateur s’ouvre. Cliquez sur **Suivant** pour poursuivre.

3.  Acceptez les termes du contrat de licence logiciel Microsoft, puis cliquez sur **suivant**.

4.  Cliquez sur les options pour les mises à jour Microsoft et le programme d’amélioration du produit.

5.  Sélectionnez le dossier de destination dans lequel installer le générateur UE-V, puis cliquez sur **suivant**.

6.  Cliquez sur **installer** pour lancer l’installation.

    **Remarques**  Une invite de **contrôle de compte d’utilisateur** apparaît avant l’installation de l’application. Une autorisation est requise pour l’installation d’UE-V Generator.

     

7.  Cliquez sur **Terminer** pour fermer l’Assistant une fois l’installation terminée. Vous devez redémarrer votre ordinateur avant de pouvoir exécuter le générateur UE-V.

    Pour vérifier que l’installation a réussi, cliquez sur **Démarrer**, sur **tous les programmes**, sur virtualisation de l’utilisation de l' **utilisateur Microsoft**, puis sur **Générateur de virtualisation Microsoft**.

    **Remarques**  Le générateur UE-V 2 ne peut être utilisé que pour créer des modèles pour les agents UE-V 2. Dans le cas d’un déploiement mixte d’UE-V 1,0 agents et d’acteurs de l’UE-V 2, vous devez continuer à utiliser le générateur de complément UE-V 1,0 jusqu’à ce que vous ayez procédé à la mise à niveau de tous les agents UE-V.

     

## <a href="" id="deploycatalogue"></a>Déployer un catalogue de modèles de paramètres


Le catalogue de modèles de paramètres de virtualisation de l’utilisation de l’utilisateur est un chemin de dossier sur les ordinateurs UE-V ou un partage réseau SMB qui stocke tous les modèles d’emplacement des paramètres personnalisés. Une tâche planifiée dans l’agent UE-V vérifie cet emplacement une fois par jour et met à jour son comportement de synchronisation, en fonction des modèles figurant dans ce dossier.

L’agent UE-V inscrit les modèles qui ont été ajoutés ou mis à jour dans ce dossier après la dernière vérification du dossier et l’annulation de l’inscription de modèles qui ont été supprimés. Par défaut, les modèles sont inscrits et annulés une fois par jour à 3:30 matin. heure locale par le planificateur de tâches et au démarrage du système. Pour personnaliser la fréquence de cette tâche planifiée, reportez-vous à [la rubrique modification de la fréquence des tâches planifiées UE-V 2.](changing-the-frequency-of-ue-v-2x-scheduled-tasks-both-uevv2.md)

Vous pouvez configurer le chemin du catalogue de modèles de paramètres à l’aide des options de ligne de commande d’installation, de stratégie de groupe, de WMI ou de Windows PowerShell. Les modèles stockés dans le modèle de modèle paramètres sont automatiquement inscrits et désinscrits par une tâche planifiée.

**Pour configurer le catalogue de modèles de paramètres pour UE-V 2. x**

1.  Créez un dossier sur l’ordinateur sur lequel est stocké le catalogue de modèles de paramètres UE-V.

2.  Définissez les autorisations de niveau de partage (SMB) suivantes pour le dossier du catalogue de modèles de paramètres.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong>Compte d’utilisateur</strong></th>
    <th align="left"><strong>Autorisations recommandées</strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Tout le monde</p></td>
    <td align="left"><p>Aucune autorisation</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Ordinateurs de domaine</p></td>
    <td align="left"><p>Lire les niveaux d’autorisation</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Administrateurs</p></td>
    <td align="left"><p>Niveaux d’autorisation en lecture/écriture</p></td>
    </tr>
    </tbody>
    </table>

     

3.  Définissez les autorisations de système de fichiers NTFS suivantes pour le dossier du catalogue de modèles de paramètres.

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Compte d’utilisateur</th>
    <th align="left">Autorisations recommandées</th>
    <th align="left">Appliquer à</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Créateur/propriétaire</p></td>
    <td align="left"><p>Contrôle total</p></td>
    <td align="left"><p>Ce dossier, les sous-dossiers et les fichiers</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Ordinateurs de domaine</p></td>
    <td align="left"><p>Afficher le contenu du dossier et lire</p></td>
    <td align="left"><p>Ce dossier, les sous-dossiers et les fichiers</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Tout le monde</p></td>
    <td align="left"><p>Aucune autorisation</p></td>
    <td align="left"><p>Aucune autorisation</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Administrateurs</p></td>
    <td align="left"><p>Contrôle total</p></td>
    <td align="left"><p>Ce dossier, les sous-dossiers et les fichiers</p></td>
    </tr>
    </tbody>
    </table>

     

4.  Cliquez sur **OK** pour fermer les boîtes de dialogue.

Au minimum, le partage réseau doit accorder des autorisations pour le groupe ordinateurs du domaine. Par ailleurs, accordez des autorisations d’accès au dossier de partage réseau aux administrateurs qui doivent gérer les modèles stockés.

## <a href="" id="createcustomtemplates"></a>Créer des modèles d’emplacement des paramètres personnalisés


Utilisez le générateur UE-V pour créer des modèles d’emplacement des paramètres pour les applications métier ou d’autres applications personnalisées. Une fois que le modèle d’application est créé, vous pouvez le déployer sur des ordinateurs de sorte que les paramètres soient synchronisés pour cette application.

**Pour créer un modèle d’emplacement des paramètres UE-V avec le générateur UE-V**

1.  Cliquez sur **Démarrer**, sur **tous les programmes**, sur virtualisation de l' **utilisation de Microsoft**, puis sur générateur de **virtualisation Microsoft User Interface**.

2.  Cliquez sur **créer un modèle d’emplacement des paramètres**.

3.  Spécifiez l’application. Naviguez jusqu’au chemin d’accès de l’application (. exe) ou du raccourci de l’application (. lnk) pour lequel vous voulez créer un modèle d’emplacement des paramètres. Spécifiez les arguments de ligne de commande, le cas échéant, et le répertoire de travail, le cas échéant. Cliquez sur **Suivant** pour poursuivre.

    **Remarques**  Avant le démarrage de l’application, le système affiche une invite de **contrôle de compte d’utilisateur**. Une autorisation est requise pour contrôler les emplacements du Registre et des fichiers utilisés par l’application pour le stockage des paramètres.

     

4.  Après le démarrage de l’application, fermez l’application. Le générateur UE-V enregistre les emplacements où l’application stocke ses paramètres.

5.  Une fois le processus terminé, cliquez sur **suivant** pour continuer.

6.  Passez en revue et activez les cases à cocher situées en regard des emplacements de paramètres de Registre et des emplacements de fichier de paramètres appropriés à synchroniser pour cette application. La liste inclut les deux catégories suivantes pour les emplacements de paramètres:

    -   **Standard**: les paramètres de l’application qui sont stockés dans le Registre sous les clés HKEY \ _CURRENT \ _USER ou dans les dossiers de fichiers sous \ \ **utilisateurs** \ \ \ [nom d’utilisateur \] \ \ **AppData**  \\  **itinérance**. UE-V Generator inclut ces paramètres par défaut.

    -   Non **standard**: les paramètres d’application stockés en dehors des emplacements sont spécifiés dans les recommandations en matière de stockage des données de paramètres (facultatif). Il s’agit des fichiers et dossiers sous **utilisateurs** \ \ \ [nom d’utilisateur \] \ \ **AppData**  \\  **local**. Passez en revue ces emplacements pour déterminer s’ils doivent figurer dans le modèle d’emplacement des paramètres. Activez les cases à cocher emplacements pour les inclure.

    Cliquez sur **Suivant** pour poursuivre.

7.  Examinez et modifiez les **Propriétés**, emplacements **du Registre** et emplacements des **fichiers** pour le modèle d’emplacement des paramètres.

    -   Modifiez les propriétés suivantes sous l’onglet **Propriétés** :

        -   **Nom**de l’application: nom de l’application qui est écrite dans la description des propriétés du programme files.

        -   **Nom du programme**: nom du programme provenant des propriétés du fichier programme. Ce nom est généralement l’extension de nom de fichier. exe.

        -   **Version du produit**: numéro de version du fichier. exe de l’application. En conjonction avec la version du **fichier**, cette propriété permet de déterminer quelles applications sont ciblées par le modèle d’emplacement des paramètres. Cette propriété accepte un numéro de version principal. Si cette propriété est vide, le modèle d’emplacement des paramètres s’applique à toutes les versions du produit.

        -   **Version du fichier**: numéro de version du fichier. exe de l’application. Combinée à la **version du produit**, cette propriété permet d’identifier les applications ciblées par le modèle d’emplacement des paramètres. Cette propriété accepte un numéro de version principal. Si cette propriété est vide, le modèle d’emplacement des paramètres s’applique à toutes les versions du programme.

        -   **Nom** de l’auteur du modèle (facultatif): nom de l’auteur du modèle d’emplacement des paramètres.

        -   **Courrier de création de modèles** (facultatif): adresse de messagerie de l’auteur du modèle d’emplacement des paramètres.

    -   L’onglet **Registre** recense la **clé** et l' **étendue** des emplacements du Registre inclus dans le modèle d’emplacement des paramètres. Modifiez les emplacements du Registre à l’aide du menu déroulant **tâches** . Les tâches vous permettent d’ajouter de nouvelles clés, de modifier le nom ou l’étendue des clés existantes, de supprimer des clés et de parcourir le registre où se trouvent les clés. Utilisez l’étendue **all settings** pour inclure tous les paramètres de Registre sous la clé spécifiée. Utilisez les **paramètres et** sous-clés pour inclure tous les paramètres de Registre sous les paramètres de clé, de sous-clé et de sous-clé spécifiés.

    -   L’onglet **fichiers** recense le chemin d’accès au fichier et le masque des fichiers des emplacements de fichier inclus dans le modèle d’emplacement des paramètres. Modifiez les emplacements des fichiers à l’aide du menu déroulant **tâches** . Les tâches d’emplacement des fichiers vous permettent d’ajouter de nouveaux fichiers ou dossiers, de modifier l’étendue des fichiers ou dossiers existants, de supprimer des fichiers ou des dossiers, et d’ouvrir l’emplacement sélectionné dans l’Explorateur Windows. Laissez le masque de fichiers vide pour inclure tous les fichiers dans le dossier spécifié.

8.  Cliquez sur **créer**, puis cliquez sur **Enregistrer** pour enregistrer le modèle d’emplacement des paramètres sur l’ordinateur.

9.  Cliquez sur **Fermer** pour fermer l’Assistant modèle de paramètres. Quittez l’application de générateur UE-V.

    Après avoir créé le modèle d’emplacement des paramètres pour une application, vous devez tester le modèle. Déployez le modèle dans un environnement de laboratoire avant de le mettre en production dans l’entreprise.

[Référence du schéma de modèle d’application pour UE-V](https://technet.microsoft.com/library/dn763947.aspx) détails de la structure XML du modèle d’emplacement des paramètres d’UE-v et fournit des instructions pour la modification de ces fichiers.

## <a href="" id="deploycustomtemplates"></a>Déployer les modèles d’emplacement des paramètres personnalisés


Après avoir créé un modèle d’emplacement des paramètres auprès du générateur UE-V, vous devez le tester pour vous assurer que les paramètres de l’application sont correctement synchronisés. Vous pouvez ensuite déployer en toute sécurité le modèle d’emplacement des paramètres sur les ordinateurs de l’entreprise.

Les modèles d’emplacement des paramètres peuvent être déployés en utilisant l’une des méthodes suivantes:

-   Système de distribution de logiciels d’entreprise (ESD) tel que System Center Configuration Manager

-   Stratégie de groupe Préférences

-   Catalogue de modèles de paramètres UE-V

Les modèles déployés à l’aide d’un système ESD ou d’objets de stratégie de groupe doivent être inscrits via le service WMI (Windows Management Instrumentation) ou Windows PowerShell. Les modèles stockés dans l’emplacement du catalogue de modèles de paramètres sont automatiquement inscrits par l’agent UE-V.

**Pour utiliser le chemin de catalogue du modèle de paramètres pour déployer les modèles d’emplacement des paramètres UE-V**

1.  Naviguez jusqu’au dossier de partage réseau défini comme catalogue de modèles de paramètres.

2.  Ajoutez, supprimez ou mettez à jour les modèles d’emplacement des paramètres dans le catalogue de modèles de paramètres pour refléter la configuration de modèle d’agent UE-V que vous voulez pour les ordinateurs UE-V.

    **Remarques**  Les modèles sur les ordinateurs sont mis à jour quotidiennement. La mise à jour dépend des modifications apportées au catalogue de modèles de paramètres.

     

3.  Pour mettre à jour manuellement des modèles sur un ordinateur qui exécute l’agent UE-V, ouvrez une invite de commandes avec élévation de privilèges et naviguez jusqu’à **% programme Files%\\Microsoft de l’utilisation de l’utilisateur \ \ agent \ \ &lt; x86 ou x64 &gt; **, puis exécutez **ApplySettingsTemplateCatalog.exe**.

    **Remarques**  Ce programme s’exécute automatiquement au démarrage de l’ordinateur et à tous les jours à 3:30 A. M. pour recueillir les nouveaux modèles récemment ajoutés au catalogue.

     






## Rubriques connexes


[Préparer un déploiement UE-V 2. x](prepare-a-ue-v-2x-deployment-new-uevv2.md)

[Déployer les fonctionnalités UE-V2.x requises](deploy-required-features-for-ue-v-2x-new-uevv2.md)

 

 





