---
title: Prise en main d'UE-V2.x
description: Prise en main d'UE-V2.x
author: dansimp
ms.assetid: 526ecbf0-0dee-4f0b-b017-8f8d25357b14
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 02/13/2017
ms.openlocfilehash: d3f01dd67ea9e5f6cfcf5dc3425265deff3f7df1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809864"
---
# Prise en main d'UE-V2.x


Suivez les étapes décrites dans ce guide pour déployer rapidement Microsoft User Interface Virtualization (UE-V) 2,0 ou 2,1 dans un environnement de test de petite taille. Cela vous aide à déterminer si UE-V est la bonne solution pour gérer les paramètres utilisateur sur plusieurs appareils au sein de votre entreprise.

**Remarques**  Les informations contenues dans cette section sont répétées plus en détail dans le reste de la documentation. Par conséquent, si vous savez déjà qu’UE-V 2 est la bonne solution et que vous n’avez pas besoin de l’évaluer, vous pouvez juste vous rendre à la [préparation d’un déploiement UE-V 2. x](prepare-a-ue-v-2x-deployment-new-uevv2.md).

 

L’installation standard de UE-V synchronise les paramètres Microsoft Windows et Office par défaut ainsi que de nombreux paramètres d’application Windows. Assurez-vous que votre environnement de test inclut au moins deux ordinateurs utilisateurs qui partagent l’accès au réseau et que vous évaluez UE-V en une courte période.

-   [Étape 1: confirmer les conditions préalables](#step1): s’assurer que votre environnement peut exécuter UE-V, y compris des détails sur les configurations prises en charge.

-   [Étape 2: déployer l’emplacement de stockage des paramètres pour UE-v 2](#step2): tous les déploiements d’UE-v nécessitent un emplacement pour les packages de paramètres qui contiennent les valeurs de paramètre synchronisées.

-   [Étape 3: déployer l’agent UE-V 2](#step3): pour synchroniser les paramètres à l’aide d’UE-v, l’agent UE-v doit être installé et exécuté sur les appareils.

-   [Étape 4: testez le déploiement de votre version d’évaluation d’UE-v 2](#step4): exécutez quelques tests sur deux ordinateurs sur lesquels l’agent UE-v est installé et découvrez le fonctionnement d’UE-v.

Voilà! Après avoir suivi ces étapes, vous serez en mesure d’évaluer la façon dont UE-V peut travailler au sein de votre entreprise.

**Nouvelle évaluation:** Vous pouvez également effectuer des étapes supplémentaires pour configurer certaines applications tierces et métier pour synchroniser leurs paramètres à l’aide d’UE-V, comme décrit dans la section [déployer UE-V 2. x pour des applications personnalisées](deploy-ue-v-2x-for-custom-applications-new-uevv2.md).

## <a href="" id="step1"></a>Étape 1: confirmer les conditions préalables


Avant de continuer, assurez-vous que votre environnement inclut les exigences requises pour exécuter UE-V.

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong>Système d’exploitation</strong></th>
<th align="left"><strong>Édition</strong></th>
<th align="left"><strong>Service Pack</strong></th>
<th align="left"><strong>Architecture système</strong></th>
<th align="left"><strong>Windows PowerShell</strong></th>
<th align="left"><strong>Microsoft .NET Framework</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Plus de.</p></td>
<td align="left"><p>Edition intégrale, entreprise ou édition professionnelle</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>32bits ou 64bits</p></td>
<td align="left"><p>Windows PowerShell 3,0 ou version ultérieure</p></td>
<td align="left"><p>.NET Framework 4 ou version ultérieure</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008R2</p></td>
<td align="left"><p>Standard, entreprise, Datacenter ou serveur Web</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64 bits</p></td>
<td align="left"><p>Windows PowerShell 3,0 ou version ultérieure</p></td>
<td align="left"><p>.NET Framework 4 ou version ultérieure</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows 8.1</p></td>
<td align="left"><p>Entreprise ou professionnel</p></td>
<td align="left"><p>None</p></td>
<td align="left"><p>32bits ou 64bits</p></td>
<td align="left"><p>Windows PowerShell 3,0 ou version ultérieure</p></td>
<td align="left"><p>.NET Framework 4,5</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2012R2 ou Windows Server2012</p></td>
<td align="left"><p>Standard ou Datacenter</p></td>
<td align="left"><p>None</p></td>
<td align="left"><p>64 bits</p></td>
<td align="left"><p>Windows PowerShell 3,0 ou version ultérieure</p></td>
<td align="left"><p>.NET Framework 4,5</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows 10, version pre-1607</p></td>
<td align="left"><p>Entreprise ou professionnel</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32bits ou 64bits</p></td>
<td align="left"><p>Windows PowerShell 3,0 ou version ultérieure</p></td>
<td align="left"><p>.NET Framework 4,5</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2016</p></td>
<td align="left"><p>Standard ou Datacenter</p></td>
<td align="left"><p>None</p></td>
<td align="left"><p>64 bits</p></td>
<td align="left"><p>Windows PowerShell 3,0 ou version ultérieure</p></td>
<td align="left"><p>.NET Framework 4,5</p></td>
</tr>
</tbody>
</table>

**Remarque:** À partir de Windows 10, la version 1607, UE-V est incluse dans [Windows 10 pour les entreprises](https://www.microsoft.com/WindowsForBusiness/windows-for-enterprise) et ne fait plus partie du pack d’optimisation de bureau Microsoft

En outre...

-   **Licence MDOP:** Cette technologie fait partie du pack d’optimisation de bureau Microsoft (MDOP). Les clients d’entreprise peuvent obtenir MDOP avec Microsoft Software Assurance. Pour plus d’informations sur le programme d’assurance logiciel Microsoft et sur l’acquisition de MDOP, voir comment obtenir MDOP ( https://go.microsoft.com/fwlink/p/?LinkId=322049) .

-   **Informations d’identification d’administration** pour les ordinateurs sur lesquels vous allez procéder à l’installation

## <a href="" id="step2"></a>Étape 2: déployer l’emplacement de stockage des paramètres pour UE-V 2


Vous devez déployer un emplacement de stockage des paramètres (un partage réseau standard où les paramètres utilisateur sont stockés dans un fichier de package de paramètres). Lorsque vous créez le partage de stockage des paramètres, vous devez limiter l’accès aux utilisateurs qui en ont besoin. [Le déploiement d’un emplacement de stockage des paramètres](https://technet.microsoft.com/library/dn458891.aspx#ssl) fournit des informations plus détaillées.

**Créer un partage réseau**

1.  Créer un groupe de sécurité et y ajouter des utilisateurs UE-V.

2.  Créez un dossier sur l’ordinateur central dans lequel sont stockés les packages de paramètres UE-V, puis accordez aux utilisateurs d’UE-V l’accès à un dossier. L’administrateur qui prend en charge UE-V doit disposer de l’autorisation d’accès à ce dossier partagé.

3.  Attribuez des autorisations aux utilisateurs d’UE-V pour créer un répertoire lors de leur connexion. Accordez l’autorisation complète à tous les sous-répertoires de ce répertoire, mais bloquez l’accès à un élément plus haut.

    1.  Définissez les autorisations de blocs de messages serveur au niveau du partage (SMB) suivantes pour le dossier emplacement de stockage des paramètres.

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
        <td align="left"><p>Groupe de sécurité des utilisateurs d’UE-V</p></td>
        <td align="left"><p>Contrôle total</p></td>
        </tr>
        </tbody>
        </table>

         

    2.  Définissez les autorisations de système de fichiers NTFS suivantes pour le dossier emplacement de stockage des paramètres.

        <table>
        <colgroup>
        <col width="33%" />
        <col width="33%" />
        <col width="33%" />
        </colgroup>
        <thead>
        <tr class="header">
        <th align="left"><strong>Compte d’utilisateur</strong></th>
        <th align="left"><strong>Autorisations recommandées</strong></th>
        <th align="left"><strong>Folder</strong></th>
        </tr>
        </thead>
        <tbody>
        <tr class="odd">
        <td align="left"><p>Créateur/propriétaire</p></td>
        <td align="left"><p>Contrôle total</p></td>
        <td align="left"><p>Sous-dossiers et fichiers uniquement</p></td>
        </tr>
        <tr class="even">
        <td align="left"><p>Groupe de sécurité des utilisateurs d’UE-V</p></td>
        <td align="left"><p>Afficher le dossier/lire les données, créer des dossiers/ajouter des données</p></td>
        <td align="left"><p>Ce dossier uniquement</p></td>
        </tr>
        </tbody>
        </table>

         

**Note de sécurité:**

Si vous créez le partage de stockage de paramètres sur un ordinateur exécutant un système d’exploitation Windows Server, configurez UE-V pour vérifier que le groupe Administrateurs local ou l’utilisateur actuel est le propriétaire du dossier dans lequel les packages de paramètres sont stockés. Pour activer cette sécurité supplémentaire, spécifiez ce paramètre dans l’éditeur du registre de Windows Server:

1.  Ajoutez une clé de Registre **reg \ _DWORD** nommée **«RepositoryOwnerCheckEnabled»** dans **HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\uev\\agent\\configuration**.

2.  Définissez la valeur de la clé de Registre sur *1*.

## <a href="" id="step3"></a>Étape 3: déployer l’agent UE-V 2


UE-V agent synchronise les paramètres d’application et de fenêtre entre les ordinateurs et appareils des utilisateurs. À des fins d’évaluation, installez l’agent sur au moins deux ordinateurs de votre environnement de test qui appartiennent au même utilisateur.

Exécutez le fichier AgentSetup.exe à partir de la ligne de commande pour installer l’agent UE-V. Il s’installe sur les systèmes d’exploitation 32 bits et 64 bits.

``` syntax
AgentSetup.exe SettingsStoragePath=\\server\settingsshare\%username%
```

Vous devez spécifier le paramètre de ligne de commande SettingsStoragePath comme partage réseau à partir de l’étape 2. [Le déploiement d’un agent UE-V](https://technet.microsoft.com/library/dn458891.aspx#agent) fournit des informations plus détaillées.

## <a href="" id="step4"></a>Étape 4: tester le déploiement de votre version d’évaluation d’UE-V 2


Vous pouvez maintenant exécuter quelques tests sur votre déploiement d’évaluation d’UE-V pour découvrir le fonctionnement d’UE-V.

****

1.  Sur le premier ordinateur (ordinateur A), effectuez une ou plusieurs des modifications suivantes:

    1.  Ouvrez le bureau Windows et déplacez la barre des tâches vers un emplacement différent dans la fenêtre.

    2.  Changer la police par défaut.

    3.  Ouvrez Calculator et sélectionnez **scientifique**.

    4.  Modifiez le comportement de toutes les applications Windows, comme décrit dans [gestion d’UE-V 2. x modèles d’emplacement des paramètres à l’aide de Windows PowerShell et WMI](managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md).

    5.  Désactivez la synchronisation des paramètres de compte Microsoft et les profils d’itinérance.

2.  Déconnectez-vous de l’ordinateur A. les paramètres sont enregistrés dans un package de paramètres d’UE-V lorsque les utilisateurs verrouillent, ferment ou quittent une application, ou lorsque le fournisseur de synchronisation s’exécute (toutes les 30 minutes par défaut).

3.  Connectez-vous au deuxième ordinateur (ordinateur B) en tant qu’utilisateur de l’ordinateur A.

4.  Ouvrez le bureau Windows et vérifiez que l’emplacement de la barre des tâches correspond à celui de l’ordinateur A. Vérifiez que les polices par défaut correspondent et que la calculatrice est définie sur **science**. Vérifiez également la modification apportée à une application Windows.

Vous pouvez redéfinir les paramètres de l’ordinateur B sur les paramètres de l’ordinateur d’origine. Déconnectez-vous de l’ordinateur B et connectez-vous à l’ordinateur A pour vérifier les modifications.

## Autres ressources pour ce produit


-   [Virtualisation de l’utilisation de l’utilisateur Microsoft (UE-V) 2. x](index.md)

-   [Préparer un déploiement UE-V 2. x](prepare-a-ue-v-2x-deployment-new-uevv2.md)

-   [Administration d’UE-V 2. x](administering-ue-v-2x-new-uevv2.md)

-   [Résolution des problèmes de UE-V 2. x](troubleshooting-ue-v-2x-both-uevv2.md)

-   [Informations techniques de référence sur UE-V2.x](technical-reference-for-ue-v-2x-both-uevv2.md)






 

 





