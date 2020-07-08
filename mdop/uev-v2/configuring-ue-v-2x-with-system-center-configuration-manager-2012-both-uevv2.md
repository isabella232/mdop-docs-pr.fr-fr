---
title: Configuration d’UE-V 2. x avec System Center Configuration Manager 2012
description: Configuration d’UE-V 2. x avec System Center Configuration Manager 2012
author: dansimp
ms.assetid: 9a4e2a74-7646-4a77-b58f-2b4456487295
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/02/2016
ms.openlocfilehash: 2ff9ccc1a17db31471549ece37461558768c3a2b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810536"
---
# Configuration d’UE-V 2. x avec System Center Configuration Manager 2012


Après l’installation de Microsoft User Interface Virtualization (UE-V) 2,0, 2,1 ou 2,1 SP1 et leurs fonctionnalités requises, UE-V doit être configurée. Le Pack de configuration UE-V permet aux administrateurs d’utiliser la fonctionnalité paramètres de conformité de System Center Configuration Manager 2012 SP1 ou une version ultérieure pour appliquer des configurations cohérentes sur les sites dans lesquels UE-V et Configuration Manager sont installés.

## Fonctionnalités prises en charge dans UE-V configuration Pack


Le Pack de configuration d’UE-V inclut des outils qui permettent d’effectuer les tâches suivantes:

-   Créer ou mettre à jour les paramètres de distribution de modèles d’emplacement des paramètres UE-V.

    -   Définir des modèles UE-V pour être inscrits ou désinscrits

    -   Mise à jour des éléments de configuration de modèle UE-V et des plannings de référence en tant que modèles ajoutés ou mis à jour

    -   Distribuer et enregistrer des modèles UE-V à l’aide de la correction standard des éléments de configuration

-   Créez ou mettez à jour un élément de configuration de la stratégie d’agent UE-V pour définir ou effacer ces paramètres.

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Taille maximale du package</p></td>
    <td align="left"><p>Activer/désactiver la synchronisation des applications Windows</p></td>
    <td align="left"><p>Attendez la fin de la synchronisation lors du démarrage de l’application</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Définir le délai d’importation</p></td>
    <td align="left"><p>Synchroniser les applications Windows non répertoriées</p></td>
    <td align="left"><p>Attendez la fin de la synchronisation lors de l’ouverture de session</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Notification d’importation de paramètres</p></td>
    <td align="left"><p>URL du contact</p></td>
    <td align="left"><p>Attendre le délai de synchronisation</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Emplacement de stockage des paramètres</p></td>
    <td align="left"><p>IL contacte un texte descriptif</p></td>
    <td align="left"><p>Chemin du catalogue de modèles de paramètres</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Activation de la synchronisation</p></td>
    <td align="left"><p>Icône de barre d’État activée</p></td>
    <td align="left"><p>Démarrer/arrêter le service d’agent UE-V</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Méthode de synchronisation</p></td>
    <td align="left"><p>Notification d’utilisation initiale</p></td>
    <td align="left"><p>Définir les applications Windows qui feront l’itinérance des paramètres</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Délai de synchronisation</p></td>
    <td align="left"><p></p></td>
    <td align="left"><p></p></td>
    </tr>
    </tbody>
    </table>

     

-   Vérifier la conformité en confirmant que UE-V est en cours d’exécution.

## Générer un élément de configuration de la stratégie d’agent UE-V


Toutes les stratégies et configuration de l’agent UE-V sont distribuées à l’aide d’un élément de configuration unique généré à l’aide de l’outil UevAgentPolicyGenerator.exe. Cet outil lit la configuration souhaitée à partir d’un fichier de configuration XML et crée un CI contenant les paramètres de découverte et de correction nécessaires à la mise en conformité de l’ordinateur.

Le fichier CAB de configuration de la stratégie d’agent UE-V est créé à l’aide de l’outil de ligne de commande UevTemplateBaselineGenerator.exe, qui comporte les paramètres suivants:

-   Code du site de site &lt;&gt;

-   Nom de l' &lt; &gt; argument PolicyName facultatif: est défini par défaut sur «UE-V Policy agent» en cas de non-présentation

-   &lt;Description &gt; de PolicyDescription facultatif: une description est fournie en cas de non-présentation

-   CabFilePath &lt; chemin d’accès complet de l’élément de configuration. Fichier CAB&gt;

-   ConfigurationFile &lt; chemin complet du fichier XML de configuration de l’agent&gt;

**Remarques**  Il peut être nécessaire de modifier la stratégie d’exécution PowerShell pour autoriser l’exécution de ces scripts dans votre environnement. Procédez comme suit dans la console Configuration Manager:

1.  Sélectionner **les &gt; &gt; Propriétés de paramètres du client d’administration**

2.  Dans l’onglet **agent utilisateur** , définissez la **stratégie d’exécution PowerShell** sur **outrepasser**

<a href="" id="create"></a>**Créer le premier élément de configuration de stratégie UE-V**

1.  Copiez le fichier de configuration des paramètres par défaut à partir du répertoire d’installation d’UE-V.

    ``` syntax
    C:\Program Files (x86)\Microsoft User Experience Virtualization\ConfigPack\AgentConfiguration.xml c:\<target path>
    ```

    Le fichier de configuration par défaut comporte cinq sections:

    <a href="" id="computer-policy"></a>**Stratégie d’ordinateur**  
    Tous les paramètres au niveau d’UE-V. L’attribut DesiredState peut être

    -   **Définir** la valeur sur le registre

    -   **Effacer** pour supprimer le paramètre

    -   **Non géré** pour que l’élément de configuration reste à l’état actuel

    Ne pas supprimer les lignes de cette section. Définissez plutôt le DesiredState sur «non géré» si vous ne souhaitez pas que Configuration Manager modifie les valeurs actuelles ou par défaut.

    <a href="" id="currentcomputeruserpolicy"></a>**CurrentComputerUserPolicy**  
    Tout le niveau des utilisateurs d’UE-V. Ces entrées remplacent les paramètres de l’ordinateur d’un utilisateur. L’attribut DesiredState peut être

    -   **Définir** la valeur sur le registre

    -   **Effacer** pour supprimer le paramètre

    -   **Non géré** pour que l’élément de configuration reste à l’état actuel

    Ne pas supprimer les lignes de cette section. Définissez plutôt le DesiredState sur «non géré» si vous ne souhaitez pas que Configuration Manager modifie les valeurs actuelles ou par défaut.

    <a href="" id="services"></a>**Services**  
    Entrées de cette opération de service de contrôle de section. Le fichier de configuration par défaut contient une entrée unique pour le UevAgentService. L’attribut DesiredState peut être défini sur **en cours d’exécution** ou **arrêté**.

    <a href="" id="windows8appscomputerpolicy"></a>**Windows8AppsComputerPolicy**  
    Tous les paramètres de synchronisation des applications Windows au niveau machine. Chaque propriété packagefamilyname répertorié dans cette section peut être affectée à un DesiredState de

    -   **Activation** de l’itinérance des paramètres

    -   **Désactivé** pour empêcher les paramètres d’être en itinérance

    -   **Compensé** pour que l’entrée ne soit pas supprimée du contrôle UE-V

    Des lignes supplémentaires peuvent être ajoutées à cette section en fonction de la liste des applications Windows installées qui peuvent être consultées à l’aide de la cmdlet PowerShell GetAppxPackage.

    <a href="" id="windows8appscurrentcomputeruserpolicy"></a>**Windows8AppsCurrentComputerUserPolicy**  
    Identique à Windows8AppsComputerPolicy avec des paramètres qui remplacent les paramètres de l’ordinateur d’un utilisateur individuel.

2.  Modifiez le fichier de configuration en modifiant les champs état souhaité et valeur.

3.  Exécutez la commande suivante sur un ordinateur exécutant la console d’administration de ConfigMgr:

    ``` syntax
    C:\Program Files (x86)\Microsoft User Experience Virtualization\ConfigPack\UevAgentPolicyGenerator.exe –Site ABC –CabFilePath "C:\MyCabFiles\UevPolicyItem.cab" –ConfigurationFile "c:\AgentConfiguration.xml"
    ```

4.  Importer le fichier CAB en utilisant la console ConfigMgr ou l’importation PowerShell-CMConfigurationItem

**Mettre à jour un élément de configuration de stratégie UE-V**

1.  Modifiez le fichier de configuration en modifiant les champs état souhaité et valeur.

2.  Exécutez la commande à partir de l’étape 3 de [la rubrique créer le premier élément de configuration de stratégie UE-V](#create). Si vous avez modifié le nom avec le paramètre PolicyName, assurez-vous d’entrer le même nom.

3.  Réimportez le fichier CAB. La version de ConfigMgr sera mise à jour.

## Générer une référence de modèle UE-V
Les modèles UE-V sont distribués à l’aide d’un planning de référence contenant plusieurs éléments de configuration. Chaque élément de configuration contient les scripts de découverte et de correction nécessaires à l’installation d’un modèle UE-V. Le modèle UE-V réel est incorporé dans le script de correction pour la distribution à l’aide de la fonctionnalité standard des éléments de configuration.

Le planning de référence de modèle UE-V est créé à l’aide de l’outil de ligne de commande UevTemplateBaselineGenerator.exe, qui comporte les paramètres suivants:

-   Code du site de site &lt;&gt;

-   Nom de BaselineName &lt; &gt; (facultatif: par défaut sur «UE-V» planning de référence, le cas échéant)

-   &lt;Description &gt; de BaselineDescription (facultatif: une description est fournie en cas de non-présentation)

-   &lt;Dossier de modèles TemplateFolder UE-V&gt;

-   Enregistrer la &lt; liste de fichiers de modèles séparés par des virgules&gt;

-   Annuler l’inscription de la &lt; liste des modèles séparés par des virgules&gt;

-   CabFilePath &lt; chemin complet du fichier CAB de référence pour générer&gt;

Le résultat est un fichier CAB de référence qui est prêt à être importé dans Configuration Manager. S’il s’agit d’une date ultérieure, vous pouvez mettre à jour ou ajouter un modèle, vous pouvez relancer la commande en utilisant le même nom de référence. L’importation des résultats du fichier CAB dans les mises à jour de la version CI sur les modèles modifiés.

### <a href="" id="create2"></a>Créer la première référence de modèle UE-V

1.  Créez un ensemble «maître» de modèles UE-V dans un emplacement de dossier stable visible pour l’ordinateur exécutant votre console d’administration ConfigMgr. À mesure que les modèles sont ajoutés ou mis à jour, il s’agit de ceux qui sont extraits pour distribution. La liste initiale des modèles peut être copiée à partir d’un ordinateur sur lequel est installé UE-V. L’emplacement du modèle par défaut est C:\\Program Files\\Microsoft user interface Virtualization\\Templates.

2.  Créez un fichier text.bat dans lequel vous pouvez ajouter la commande de générateur de modèles. Ce paramètre est facultatif, mais il est plus simple à régénérer si vous enregistrez les paramètres de commande.

3.  Ajoutez la commande et des paramètres au fichier. bat qui générera le planning de référence. L’exemple suivant crée un planning de référence qui répartit le bloc-notes et la calculatrice:

    ``` syntax
    C:\Program Files (x86)\Microsoft User Experience Virtualization\ConfigPack\UevTemplateBaselineGenerator.exe –Site "ABC" –TemplateFolder "C:\ProductionUevTemplates" –Register "MicrosoftNotepad.xml, MicrosoftCalculator.xml" –CabFilePath "C:\MyCabFiles\UevTemplateBaseline.cab"
    ```

4.  Exécutez le fichier. bat pour créer UevTemplateBaseline.cab prêtes à être importées dans Configuration Manager.

### Mise à jour d’une référence de modèle UE-V

Le générateur de modèles utilise la version du modèle pour déterminer si un modèle doit être mis à jour. Si vous effectuez un changement de modèle et mettez à jour la version, le générateur de ligne de base compare le modèle dans votre dossier principal avec le modèle contenu dans l’article CI du serveur ConfigMgr. S’il existe une différence, les versions de référence CI de base et de la base de référence générées sont mises à jour.

Pour distribuer un nouveau modèle de bloc-notes, vous devez effectuer les étapes suivantes:

1.  Mettez à jour le modèle et la version du modèle figurant dans l' &lt; &gt; élément version du modèle.

2.  Copiez le modèle dans votre répertoire de modèle maître.

3.  Exécutez la commande dans le fichier. bat que vous avez créé à l’étape 3 de [la rubrique créer le premier Planning UE-V de modèle](#create2).

4.  Importez le fichier CAB généré dans ConfigMgr à l’aide de la console ou de PowerShell Import-CMBaseline.

## Télécharger le Pack de configuration pour UE-V


Le module de configuration d’UE-V pour configurations Manager 2012 SP1 ou version ultérieure peut être téléchargé [ici](https://go.microsoft.com/fwlink/?LinkId=317263).






## Rubriques connexes


[Gérer les configurations pour UE-V2.x](manage-configurations-for-ue-v-2x-new-uevv2.md)

 

 





