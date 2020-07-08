---
title: Publication d'applications et interaction avec le Client
description: Publication d'applications et interaction avec le Client
author: dansimp
ms.assetid: 36a4bf6f-a917-41a6-9856-6248686df352
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 69fcf119faaf35e53ae36f386bcb3480e2ee3b0e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805947"
---
# Publication d'applications et interaction avec le Client


Cet article fournit des informations techniques sur les opérations courantes du client d’application V et son intégration au système d’exploitation local.

-   [Fichiers de package App-V créés par le Sequencer](#bkmk-appv-pkg-files-list)

-   [Qu’est-ce que le fichier AppV?](#bkmk-appv-file-contents)

-   [Emplacements de stockage des données du client App-V](#bkmk-files-data-storage)

-   [Registre de package](#bkmk-pkg-registry)

-   [Comportement du magasin de packages App-V](#bkmk-pkg-store-behavior)

-   [Itinérance et Registre](#bkmk-roaming-reg-data)

-   [Gestion du cycle de vie des applications du client App-V](#bkmk-clt-app-lifecycle)

-   [Intégration des packages App-V](#bkmk-integr-appv-pkgs)

-   [Traitement dynamique des configurations](#bkmk-dynamic-config)

-   [Assemblys côte à côte](#bkmk-sidebyside-assemblies)

-   [Journalisation du client](#bkmk-client-logging)

Pour obtenir des informations de référence supplémentaires, voir [la page de téléchargement des ressources de documentation de Microsoft Application Virtualization (App-V)](https://www.microsoft.com/download/details.aspx?id=27760).

## <a href="" id="bkmk-appv-pkg-files-list"></a>Fichiers de package App-V créés par le Sequencer


Le Sequencer crée des packages App-V et génère une application virtualisée. Le processus de séquençage génère les fichiers suivants:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Fichier</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>. AppV</p></td>
<td align="left"><ul>
<li><p>Le fichier de package principal, qui contient les ressources capturées et les informations d’État du processus de séquençage.</p></li>
<li><p>Architecture du fichier de package, des informations de publication et du Registre sous la forme d’un jeton qui peut être réappliqué à un ordinateur et à un utilisateur spécifique lors de la remise.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>. PORTION</p></td>
<td align="left"><p>Wrapper de déploiement exécutable qui vous permet de déployer manuellement des fichiers. AppV ou en utilisant une plate-forme de déploiement tierce.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>_DeploymentConfig.XML</p></td>
<td align="left"><p>Fichier utilisé pour personnaliser les paramètres de publication par défaut de toutes les applications d’un package déployé globalement pour tous les utilisateurs sur un ordinateur exécutant le client App-V.</p></td>
</tr>
<tr class="even">
<td align="left"><p>_UserConfig.XML</p></td>
<td align="left"><p>Fichier utilisé pour personnaliser les paramètres de publication de toutes les applications d’un package déployés pour un utilisateur spécifique sur un ordinateur exécutant le client App-V.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Report.xml</p></td>
<td align="left"><p>Résumé des messages issus du processus de séquençage, y compris les pilotes, fichiers et emplacements de Registre omis.</p></td>
</tr>
<tr class="even">
<td align="left"><p>. CAB</p></td>
<td align="left"><p><em>Facultatif: </em> fichier d’accélérateur de package utilisé pour générer automatiquement un package d’application virtuelle précédemment séquencé.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>.appvt</p></td>
<td align="left"><p><em>Facultatif: </em> fichier de modèle de Sequencer permettant de conserver les paramètres de Sequencer fréquemment utilisés.</p></td>
</tr>
</tbody>
</table>

 

Pour plus d’informations sur le séquençage, voir [Guide de séquençage de l’application virtualisation](https://go.microsoft.com/fwlink/?LinkID=269810).

## <a href="" id="bkmk-appv-file-contents"></a>Qu’est-ce que le fichier AppV?


Le fichier AppV est un conteneur qui stocke les fichiers XML et non XML ensemble dans une seule entité. Ce fichier est créé à partir du format AppX, qui est basé sur le standard Open Packaging Conventions (OPC).

Pour afficher le contenu du fichier AppV, effectuez une copie du package, puis renommez le fichier copié en extension ZIP.

Le fichier AppV contient les dossiers et fichiers suivants qui sont utilisés lors de la création et de la publication d’une application virtuelle:

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nom</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Racine</p></td>
<td align="left"><p>Dossier de fichiers</p></td>
<td align="left"><p>Répertoire qui contient le système de fichiers de l’application virtualisée qui est capturée lors du séquençage.</p></td>
</tr>
<tr class="even">
<td align="left"><p>[Content_Types]. Xml</p></td>
<td align="left"><p>Fichier XML</p></td>
<td align="left"><p>Liste des types de contenu principaux dans le fichier AppV (par exemple, DLL, EXE, BIN).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>AppxBlockMap.xml</p></td>
<td align="left"><p>Fichier XML</p></td>
<td align="left"><p>Disposition du fichier AppV, qui utilise des éléments de fichier, de bloc et de BlockMap qui permettent d’organiser et de valider des fichiers dans le package App-V.</p></td>
</tr>
<tr class="even">
<td align="left"><p>AppxManifest.xml</p></td>
<td align="left"><p>Fichier XML</p></td>
<td align="left"><p>Métadonnées du package qui contient les informations requises pour l’ajout, la publication et le lancement du package. Inclut des points d’extension (associations et raccourcis de types de fichiers), ainsi que les noms et GUID associés au package.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>FilesystemMetadata.xml</p></td>
<td align="left"><p>Fichier XML</p></td>
<td align="left"><p>Liste des fichiers capturés lors du séquençage, y compris les attributs (par exemple, les répertoires, les fichiers, les répertoires opaques, les répertoires vides et les noms longs et courts).</p></td>
</tr>
<tr class="even">
<td align="left"><p>PackageHistory.xml</p></td>
<td align="left"><p>Fichier XML</p></td>
<td align="left"><p>Des informations sur le séquençage de l’ordinateur (version du système d’exploitation, version d’Internet Explorer, version du .NET Framework) et du processus (mise à niveau, version du package).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Registry. dat</p></td>
<td align="left"><p>Fichier DAT</p></td>
<td align="left"><p>Valeurs et clés de Registre capturées lors du processus de séquençage pour le package.</p></td>
</tr>
<tr class="even">
<td align="left"><p>StreamMap.xml</p></td>
<td align="left"><p>Fichier XML</p></td>
<td align="left"><p>Liste des fichiers pour le bloc de fonctionnalités principal et de publication. Le bloc de fonctionnalité de publication contient les fichiers ICO et les portions de fichiers requises (EXE et DLL) pour la publication du package. Lorsqu’il est présent, le bloc de fonctionnalités principal inclut les fichiers qui ont été optimisés pour la diffusion en continu lors du processus de séquençage.</p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-files-data-storage"></a>Emplacements de stockage des données du client App-V


Le client App-V effectue des tâches pour s’assurer que les applications virtuelles s’exécutent correctement et fonctionnent comme des applications installées localement. Le processus d’ouverture et d’exécution des applications virtuelles nécessite le mappage à partir du système de fichiers virtuel et du Registre pour s’assurer que l’application possède les composants requis d’une application traditionnelle attendue par les utilisateurs. Cette section décrit les ressources nécessaires à l’exécution d’applications virtuelles et indique l’emplacement dans lequel App-V stocke les ressources.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nom</th>
<th align="left">Emplacement</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Magasin de packages</p></td>
<td align="left"><p>%ProgramData%\App-V</p></td>
<td align="left"><p>Emplacement par défaut des fichiers de package en lecture seule</p></td>
</tr>
<tr class="even">
<td align="left"><p>Catalogue d’ordinateurs</p></td>
<td align="left"><p>%ProgramData%\Microsoft\AppV\Client\Catalog</p></td>
<td align="left"><p>Contient des documents de configuration par ordinateur</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Catalogue utilisateur</p></td>
<td align="left"><p>%AppData%\Microsoft\AppV\Client\Catalog</p></td>
<td align="left"><p>Contient des documents de configuration par utilisateur</p></td>
</tr>
<tr class="even">
<td align="left"><p>Sauvegardes de raccourci</p></td>
<td align="left"><p>%AppData%\Microsoft\AppV\Client\Integration\ShortCutBackups</p></td>
<td align="left"><p>Stocke les points d’intégration précédents qui permettent la restauration sur l’annulation de la publication d’un package.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Itinérance dans l’enregistrement</p></td>
<td align="left"><p>%AppData%\Microsoft\AppV\Client\VFS</p></td>
<td align="left"><p>Emplacement d’itinérance inscriptible pour la modification d’un package</p></td>
</tr>
<tr class="even">
<td align="left"><p>Copie lors de l’écriture (vache) locale</p></td>
<td align="left"><p>%LocalAppData%\Microsoft\AppV\Client\VFS</p></td>
<td align="left"><p>Emplacement sans itinérance pour la modification d’un package</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Registre de l’ordinateur</p></td>
<td align="left"><p>HKLM\Software\Microsoft\AppV</p></td>
<td align="left"><p>Contient des informations sur l’état du package, notamment les packages de VReg pour ordinateur ou les packages publiés globalement (ruche de l’ordinateur)</p></td>
</tr>
<tr class="even">
<td align="left"><p>Registre de l’utilisateur</p></td>
<td align="left"><p>HKCU\Software\Microsoft\AppV</p></td>
<td align="left"><p>Contient des informations sur l’état du package utilisateur, notamment VReg</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Classes Registry d’utilisateur</p></td>
<td align="left"><p>HKCU\Software\Classes\AppV</p></td>
<td align="left"><p>Contient des informations supplémentaires sur l’état du package utilisateur</p></td>
</tr>
</tbody>
</table>

 

Des informations supplémentaires sur le tableau sont fournies dans la section ci-dessous et dans l’ensemble du document.

### Magasin de packages

Le client App-V gère les ressources d’applications chargées dans le magasin de packages. Cet emplacement de stockage par défaut est `%ProgramData%\App-V` , mais vous pouvez le configurer pendant ou après l’installation à l’aide de la `Set-AppVClientConfiguration` commande PowerShell qui modifie le registre local ( `PackageInstallationRoot` valeur située sous la `HKLM\Software\Microsoft\AppV\Client\Streaming` clé). Le magasin de packages doit être localisé sur un chemin local du système d’exploitation du client. Les packages individuels sont stockés dans le magasin de packages dans les sous-répertoires nommés pour le GUID et le GUID de la version du package.

Exemple de chemin d’accès à une application spécifique:

``` syntax
C:\ProgramData\App-V\PackGUID\VersionGUID
```

Pour modifier l’emplacement par défaut du magasin de packages lors de l’installation, voir [comment déployer le client App-V](how-to-deploy-the-app-v-client-51gb18030.md).

### Magasin de contenus partagés

Si le client App-V est configuré en mode de magasin de contenus partagés, il est impossible d’écrire des données sur le disque quand une erreur de flux se produit, ce qui signifie que les packages nécessitent au moins un espace libre sur le disque local (publications de données). L’utilisation de moins d’espace disque est particulièrement utile dans les environnements VDI, où le stockage local peut être limité et la diffusion en continu des applications à partir d’un emplacement réseau haute performance (par exemple, un SAN) est préférable. Pour plus d’informations sur le mode magasin de contenu partagé, voir <https://go.microsoft.com/fwlink/p/?LinkId=392750> .

**Remarques**  Le magasin d’ordinateurs et de packages doit résider sur un disque local, même si vous utilisez des configurations de magasin de contenu partagé pour le client App-V.

 

### Catalogues de package

Le client App-V gère les deux emplacements suivants sur les fichiers:

-   **Catalogues (utilisateur et ordinateur).**

-   **Emplacements du Registre** : dépend de la manière dont le package est destiné à la publication. Il existe un catalogue (magasin de données) pour l’ordinateur ainsi qu’un catalogue pour chaque utilisateur individuel. Le catalogue d’ordinateurs stocke les informations globales applicables à tous les utilisateurs ou à tout utilisateur, et le catalogue de l’utilisateur stocke les informations applicables à un utilisateur spécifique. Le catalogue est une collection de configurations dynamiques et de fichiers manifeste; Il existe des données discrètes pour le fichier et le registre par version de package. 

### Catalogue d’ordinateurs

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>Description</p></td>
<td align="left"><p>Stocke les documents de package disponibles pour les utilisateurs sur l’ordinateur, lors de l’ajout et de la publication de packages. Toutefois, si un package est «global» au moment de la publication, les intégrations sont disponibles pour tous les utilisateurs.</p>
<p>Si un package n’est pas global, les intégrations sont uniquement publiées pour des utilisateurs spécifiques, mais il existe toujours des ressources globales qui sont modifiées et visibles par tout le monde sur l’ordinateur client (par exemple, le répertoire du package se trouve dans un emplacement sur le disque partagé).</p>
<p>Si un package est disponible pour un utilisateur de l’ordinateur (global ou non-global), le manifeste est stocké dans le catalogue d’ordinateur. Lorsqu’un package est publié globalement, il existe un fichier de configuration dynamique, qui est stocké dans le catalogue de l’ordinateur; par conséquent, la détermination de la présence d’un package global est définie en fonction de la présence d’un fichier de stratégie (fichier UserDeploymentConfiguration) dans le catalogue d’ordinateurs.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Emplacement de stockage par défaut</p></td>
<td align="left"><p><code>%programdata%\Microsoft\AppV\Client\Catalog&lt;/code&gt;</p>
<p>Cet emplacement n’est pas identique à l’emplacement de stockage du package. Le Windows Store est la copie du fichier de package.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Fichiers dans le catalogue d’ordinateurs</p></td>
<td align="left"><ul>
<li><p>Manifest.xml</p></li>
<li><p>DeploymentConfiguration.xml</p></li>
<li><p>UserManifest.xml (package publié globalement)</p></li>
<li><p>UserDeploymentConfiguration.xml (package publié globalement)</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Emplacement supplémentaire du catalogue d’ordinateurs, utilisé lorsque le package fait partie d’un groupe de connexion</p></td>
<td align="left"><p>L’emplacement suivant est en plus de l’emplacement de package spécifique mentionné ci-dessus:</p>
<p><code>%programdata%\Microsoft\AppV\Client\Catalog\PackageGroups\ConGroupGUID\ConGroupVerGUID</code></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Fichiers supplémentaires dans le catalogue d’ordinateurs lorsque le package fait partie d’un groupe de connexion</p></td>
<td align="left"><ul>
<li><p>PackageGroupDescriptor.xml</p></li>
<li><p>UserPackageGroupDescriptor.xml (groupe de connexions à publication globale)</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

### Catalogue utilisateur

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>Description</p></td>
<td align="left"><p>Créé lors du processus de publication. Contient des informations permettant de publier le package, ainsi que de l’utiliser au démarrage pour vérifier qu’un package est configuré pour un utilisateur spécifique. Créé à un emplacement itinérant et inclut des informations de publication spécifiques à l’utilisateur.</p>
<p>Lors de la publication d’un package pour un utilisateur, celui-ci est stocké dans le catalogue utilisateur. En même temps, une copie du manifeste est également stockée dans le catalogue utilisateur. Lorsqu’un utilisateur est supprimé, les fichiers de package pertinents sont supprimés du catalogue de l’utilisateur. En examinant le catalogue de l’utilisateur, un administrateur peut voir la présence d’un fichier de configuration dynamique, qui indique que le package est habilité pour cet utilisateur.</p>
<p>Pour les utilisateurs itinérants, le catalogue utilisateur doit se trouver dans un emplacement itinérant ou partagé pour conserver par défaut le comportement d’application-V hérité du ciblage des utilisateurs. Le droit d’utilisation et la politique sont liés à un utilisateur, et non à un ordinateur, afin qu’il ne soit pas itinérant auprès de l’utilisateur une fois qu’il est approvisionné.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Emplacement de stockage par défaut</p></td>
<td align="left"><p><code>appdata\roaming\Microsoft\AppV\Client\Catalog\Packages\PkgGUID\VerGUID</code></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Fichiers dans le catalogue utilisateur</p></td>
<td align="left"><ul>
<li><p>UserManifest.xml</p></li>
<li><p>DynamicConfiguration.xml ou UserDeploymentConfiguration.xml</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Emplacement supplémentaire du catalogue utilisateur, utilisé lorsque le package fait partie d’un groupe de connexion</p></td>
<td align="left"><p>L’emplacement suivant est en plus de l’emplacement de package spécifique mentionné ci-dessus:</p>
<p><code>appdata\roaming\Microsoft\AppV\Client\Catalog\PackageGroups\PkgGroupGUID\PkgGroupVerGUID</code></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Fichier supplémentaire dans le catalogue d’ordinateurs lorsque le package fait partie d’un groupe de connexions</p></td>
<td align="left"><p><code>UserPackageGroupDescriptor.xml</code></p></td>
</tr>
</tbody>
</table>

 

### Sauvegardes de raccourci

Pendant le processus de publication, le client App-V restaure les raccourcis et les points d’intégration de `%AppData%\Microsoft\AppV\Client\Integration\ShortCutBackups.` cette sauvegarde pour la restauration de ces points d’intégration aux versions précédentes lorsque le package n’est pas publié.

### Copier sur un fichier d’écriture

Le magasin de packages contient une copie de fichiers de package qui ont été diffusés en continu à partir du serveur de publication. Pendant le fonctionnement normal d’une application application V, l’utilisateur ou le service doit éventuellement modifier les fichiers. Ces modifications ne sont pas apportées dans le magasin de packages afin de préserver la possibilité de réparer l’application, ce qui a pour but de supprimer ces modifications. Ces emplacements, appelés copies lors de l’écriture (vache), prennent en charge les emplacements itinérants et non itinérants. L’emplacement où les modifications sont stockées dépend de l’application programmée pour écrire les modifications apportées à une expérimentation native.

### Itinérance COW

L’emplacement d’itinérance COW décrit ci-dessus enregistre les modifications apportées aux fichiers et répertoires ciblant l’emplacement par défaut de% AppData% ou l’emplacement \\Users\\{username}\\AppData\\Roaming. Ces fichiers et répertoires sont alors en itinérance en fonction des paramètres du système d’exploitation.

### VACHES locales

L’emplacement local de vache est semblable à l’emplacement d’itinérance, mais les répertoires et fichiers ne sont pas itinérants vers d’autres ordinateurs, même si la prise en charge de l’itinérance a été configurée. Dans l’emplacement local de vache décrit ci-dessus, les modifications sont apportées aux fenêtres standard et non à l’emplacement% AppData%. Les répertoires indiqués varient en fonction du type d’emplacement Windows (par exemple, AppData et Common AppDataS). Le **S** indique l’emplacement restreint lorsque le service virtuel demande la modification en tant qu’utilisateur à élévation de privilèges différent des utilisateurs connectés. L’emplacement non-**S** enregistre les modifications apportées par l’utilisateur.

## <a href="" id="bkmk-pkg-registry"></a>Registre de package


Pour qu’une application puisse accéder aux données du Registre du package, le client App-V doit rendre les données du Registre du package accessibles aux applications. Le client App-V utilise le registre réel comme magasin de stockage pour toutes les données du Registre.

Lors de l’ajout d’un nouveau package au client App-V, une copie du Registre. Un fichier DAT du package est créé à `%ProgramData%\Microsoft\AppV\Client\VREG\{Version GUID}.dat` . Le nom du fichier est le GUID de la version avec l’extension. Extension DAT. La raison pour laquelle il s’agit d’une copie est de s’assurer que le fichier de la ruche réel du package n’est jamais utilisé, ce qui empêche la suppression du package ultérieurement.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Registry. dat du package Store</strong></p></td>
<td align="left"><p><strong> &gt; </strong></p></td>
<td align="left"><p><strong>%ProgramData%\Microsoft\AppV\Client\Vreg {VersionGuid}. dat</strong></p></td>
</tr>
</tbody>
</table>

 

Lorsque la première application du package est lancée sur le client, le client exécute ou copie le contenu du fichier ruche, en recréant les données du Registre du package à un autre emplacement `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AppV\Client\Packages\PackageGuid\Versions\VersionGuid\REGISTRY` . Les données de Registre intermédiaire sont dotées de deux types de données d’ordinateur et de données utilisateur. Les données d’ordinateur sont partagées par tous les utilisateurs de l’ordinateur. Les données utilisateur sont transférées par utilisateur vers un emplacement userspecific `HKCU\Software\Microsoft\AppV\Client\Packages\PackageGuid\Registry\User` . Les données de l’ordinateur sont en définitive supprimées lors de la suppression du package, et les données utilisateur sont supprimées lors d’une opération de suppression de l’utilisateur.

### Échelonnement du Registre du package et de la mise en place du Registre du groupe de connexions

Lorsque des groupes de connexion sont présents, le processus précédent de staging du registre a la valeur true, mais au lieu d’avoir un fichier Hive à traiter, il en existe plusieurs. Les fichiers sont traités dans l’ordre dans lequel ils s’affichent dans le fichier XML du groupe de connexion, avec le premier scripteur qui gagne des conflits.

Le registre intermédiaire persiste de la même manière que dans le cas du package unique. Les données de registre de l’utilisateur intermédiaire restent pour le groupe de connexion tant qu’il n’est pas désactivé; les données de registre de l’ordinateur intermédiaire sont supprimées lors de la suppression du groupe de connexion.

### Registre virtuel

L’objectif du Registre virtuel (VREG) consiste à fournir une seule vue fusionnée du Registre du package et du Registre natif aux applications. Il fournit également une fonctionnalité de copie à l’écriture (vache), qui est une modification apportée au registre à partir du contexte de processus virtuel. Cela signifie que le VREG doit combiner trois emplacements du Registre distincts en une seule vue en fonction des emplacements remplis dans le registre COW- &gt; package- &gt; natif. Lorsqu’une demande de données de Registre est formulée, elle se trouve dans l’ordre jusqu’à ce qu’elle trouve les données demandées. C’est la raison pour laquelle il n’y a pas de valeur stockée à d’autres emplacements; Toutefois, s’il n’y a pas de données dans l’emplacement de la vache, il passe au package, puis à l’emplacement natif jusqu’à ce qu’il trouve les données appropriées.

### Emplacements du Registre

Il existe deux emplacements de registre de package et deux emplacements de groupe de connexion dans lesquels le client App-V stocke les informations de Registre, selon que le package est publié individuellement ou en tant que membre d’un groupe de connexion. Il existe trois emplacements de vache pour les packages et trois pour les groupes de connexion, qui sont créés et gérés par le VREG. Les paramètres des packages et des groupes de connexion ne sont pas partagés:

**Package VReg:**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Emplacement</strong></p></td>
<td align="left"><p><strong>Description</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>VACHE</strong></p></td>
<td align="left"><ul>
<li><p>Machine Registry\Client\Packages\PkgGUID\REGISTRY (seul le processus d’élévation peut écrire)</p></li>
<li><p>Utilisateur Registry\Client\Packages\PkgGUID\REGISTRY (utilisateur itinérance d’éléments écrits sous HKCU sauf Software\Classes</p></li>
<li><p>Classes\Client\Packages\PkgGUID\REGISTRY du registre des utilisateurs (HKCU\Software\Classes écrit et HKLM pour les processus non élevés)</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Package</strong></p></td>
<td align="left"><ul>
<li><p>Machine Registry\Client\Packages\PkgGUID\Versions\VerGuid\Registry\Machine</p></li>
<li><p>Classes\Client\Packages\PkgGUID\Versions\VerGUID\Registry Registre des utilisateurs</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><strong>En</strong></p></td>
<td align="left"><ul>
<li><p>Emplacement du registre d’application natif</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

 

**Groupe de connexion VReg:**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Emplacement</strong></p></td>
<td align="left"><p><strong>Description</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>VACHE</strong></p></td>
<td align="left"><ul>
<li><p>Machine Registry\Client\PackageGroups\GrpGUID\REGISTRY (seul le processus d’élévation peut écrire)</p></li>
<li><p>Registry\Client\PackageGroups\GrpGUID\REGISTRY utilisateur (ce que vous avez écrit dans HKCU sauf Software\Classes</p></li>
<li><p>Classes\Client\PackageGroups\GrpGUID\REGISTRY Registre des utilisateurs</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Package</strong></p></td>
<td align="left"><ul>
<li><p>Machine Registry\Client\PackageGroups\GrpGUID\Versions\VerGUID\REGISTRY</p></li>
<li><p>Classes\Client\PackageGroups\GrpGUID\Versions\VerGUID\REGISTRY Registre des utilisateurs</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><strong>En</strong></p></td>
<td align="left"><ul>
<li><p>Emplacement du registre d’application natif</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

 

Il existe deux emplacements de vache pour HKLM. processus élevés et non élevés. Les processus élevés écrivent toujours les modifications HKLM de Secure COW dans HKLM. Les processus non contrôlés par élévation écrivent toujours des modifications HKLM de la vache non sécurisée sous HKCU\\Software\\Classes. Lorsqu’une application lit les modifications apportées par HKLM, les processus élevés lisent les modifications de la COW sécurisée sous HKLM. Les lectures non élévations à la fois, en favorisant les changements apportés à la vache non sécurisée.

### Touches directes

Les clés directes permettent à un administrateur de configurer certaines touches afin qu’elles puissent être lues uniquement à partir du Registre natif, en ignorant les emplacements des packages et des vaches. Les emplacements de transfert sont globaux pour l’ordinateur (et non spécifiques au package) et peuvent être configurés en ajoutant le chemin d’accès à la clé, qui doit être traité comme directe à la valeur **reg \ _MULTI \ _SZ** appelée **PassThroughPaths** de la clé `HKLM\Software\Microsoft\AppV\Subsystem\VirtualRegistry` . Toute touche qui s’affiche sous cette valeur de chaîne multiple (et leurs enfants) sera traitée comme directe.

Les emplacements suivants sont configurés comme emplacements de transfert par défaut:

-   HKEY \ _CURRENT \ _USER \\SOFTWARE\\Classes\\Local Settings\\Software\\Microsoft\\Windows\\CurrentVersion\\AppModel

-   HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Classes\\Local Settings\\Software\\Microsoft\\Windows\\CurrentVersion\\AppModel

-   HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\WINEVT

-   HKEY \ _LOCAL \ _MACHINE \\SYSTEM\\CurrentControlSet\\services\\eventlog\\Application

-   HKEY \ _LOCAL \ _MACHINE \\SYSTEM\\CurrentControlSet\\Control\\WMI\\Autologger

-   HKEY \ _CURRENT \ _USER paramètres de \\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\Internet

-   HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Perflib

-   HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Policies

-   HKEY \ _CURRENT \ _USER \\SOFTWARE\\Policies

L’objectif des clés directes consiste à s’assurer qu’une application virtuelle n’écrit pas de données de Registre dans le VReg requis pour les applications non virtuelles pour une opération ou une intégration réussie. La clé stratégies vérifie que les paramètres basés sur les stratégies de groupe définis par l’administrateur sont utilisés et pas par rapport aux paramètres du package. La touche AppModel est nécessaire pour l’intégration aux applications basées sur les interfaces utilisateur modernes Windows. Il est recommandé de ne pas modifier les clés directes par défaut, mais dans certains cas, en fonction du comportement de l’application, il peut être nécessaire d’ajouter d’autres touches directes.

## <a href="" id="bkmk-pkg-store-behavior"></a>Comportement du magasin de packages App-V


App-V 5 gère le magasin de packages, qui est l’emplacement de stockage des fichiers de ressources développés à partir du fichier AppV. Par défaut, cet emplacement est stocké sur%ProgramData%\\App-V et est limité en termes de capacités de stockage uniquement par un espace libre sur le disque. Le magasin de packages est organisé selon les GUID pour le package et la version, comme indiqué dans la section précédente.

### Ajouter des packages

Les packages App-V sont intermédiaires en plus de l’ordinateur doté du client App-V. Le client App-V fournit le Staging à la demande. Lors de la publication ou d’une AppVClientPackage manuelle, la structure de données est intégrée à la Banque de packages (c:\\programdata\\App-V\\{PkgGUID}\\{VerGUID}). Les fichiers de package identifiés dans le bloc de publication définis dans le StreamMap.xml sont ajoutés au système et les dossiers de niveau supérieur et les fichiers enfants intermédiaires pour garantir l’existence de ressources d’application appropriées au lancement.

### Packages de montage

Les packages peuvent être chargés explicitement via PowerShell `Mount-AppVClientPackage` ou en utilisant l' **interface utilisateur du client App-V** pour télécharger un package. Cette opération charge entièrement le package complet dans le magasin de packages.

### Packages de diffusion en continu

Le client App-V peut être configuré pour modifier le comportement par défaut de la diffusion en continu. Toutes les stratégies de streaming sont stockées sous la clé de Registre `HKEY_LOCAL_MAcHINE\Software\Microsoft\AppV\Client\Streaming` suivante: Les stratégies sont définies à l’aide de l’applet de passe PowerShell `Set-AppvClientConfiguration` . Les stratégies suivantes s’appliquent à la diffusion en continu:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Stratégie</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>AllowHighCostLaunch</p></td>
<td align="left"><p>Sur Windows 8 et versions ultérieures, il permet de diffuser en continu des réseaux 3G et cellulaires.</p></td>
</tr>
<tr class="even">
<td align="left"><p>AutoLoad</p></td>
<td align="left"><p>Spécifie le paramètre de chargement en arrière-plan:</p>
<p><strong>0 </strong> - désactivé</p>
<p><strong>1 </strong> -packages auparavant utilisés</p>
<p><strong>2 </strong> – tous les packages</p></td>
</tr>
<tr class="odd">
<td align="left"><p>PackageInstallationRoot</p></td>
<td align="left"><p>Le dossier racine pour le magasin de packages de l’ordinateur local</p></td>
</tr>
<tr class="even">
<td align="left"><p>PackageSourceRoot</p></td>
<td align="left"><p>Remplacement de la racine où les packages doivent être diffusés en continu</p></td>
</tr>
<tr class="odd">
<td align="left"><p>SharedContentStoreMode</p></td>
<td align="left"><p>Active l’utilisation du magasin de contenu partagé pour les scénarios d’infrastructure VDI</p></td>
</tr>
</tbody>
</table>

 

 

Ces paramètres affectent le comportement de la diffusion de ressources de package App-V pour le client. Par défaut, App-V télécharge uniquement les ressources nécessaires après le téléchargement de la publication initiale et des blocs de fonctionnalités principaux. Il existe trois comportements spécifiques dans les packages de diffusion en continu qui doivent être décrits:

-   Lecture en arrière-plan

-   Streaming optimisée

-   Erreurs de flux

### Lecture en arrière-plan

L’applet de cmdlet PowerShell `Get-AppvClientConfiguration` peut être utilisée pour déterminer le mode actuel de diffusion en arrière-plan avec le paramètre autoload et modifié avec l’applet de cmdlet Set-AppvClientConfiguration ou à partir du Registre (clé HKLM\\SOFTWARE\\Microsoft\\AppV\\ClientStreaming). L’arrière-plan en arrière-plan est un paramètre par défaut dans lequel le paramètre autoload est défini pour télécharger les packages déjà utilisés. Le comportement en fonction du paramètre par défaut (valeur = 1) télécharge les blocs de données App-V en arrière-plan après le lancement de l’application. Ce paramètre peut être désactivé (valeur = 0) ou activé pour tous les packages (valeur = 2), qu’il ait été lancé.

### Streaming optimisée

Les packages App-V peuvent être configurés avec un bloc de fonctionnalités principal lors du séquençage. Ce paramètre permet à l’ingénieur de séquençage de surveiller les fichiers de démarrage pour une application spécifique, ou applications, et de marquer les blocs de données dans le package App-V pour la diffusion en continu lors du premier lancement de l’application dans le package.

### Erreurs de flux

Après le flux initial de toutes les données de publication et du bloc de fonctionnalités principal, les demandes de fichiers supplémentaires effectuent des erreurs de flux. Ces blocs de données sont téléchargés vers le magasin de packages le cas échéant. Cela permet à un utilisateur de télécharger uniquement une petite partie du package, qui suffit en général pour lancer le package et exécuter des tâches normales. Tous les autres blocs sont téléchargés lorsqu’un utilisateur lance une opération qui nécessite des données qui ne figurent pas actuellement dans le magasin de packages.

Pour plus d’informations sur la diffusion en continu de packages App-V, voir: <https://go.microsoft.com/fwlink/?LinkId=392770> .

Le séquençage pour l’optimisation de la diffusion en continu est disponible à l’adresse suivante: <https://go.microsoft.com/fwlink/?LinkId=392771> .

### Mises à jour de package

Les packages App-V nécessitent une mise à jour tout au long du cycle de vie de l’application. Les mises à niveau des packages App-V sont similaires à l’opération de publication de package, car chaque version sera créée dans son propre emplacement racine: `%ProgramData%\App-V\{PkgGUID}\{newVerGUID}` . L’opération de mise à niveau est optimisée en créant des liens durs vers des fichiers identiques et en continu à partir d’autres versions du même package.

### Suppression de package

Le comportement du client App-V lors de la suppression des packages dépend de la méthode de suppression utilisée. L’utilisation de l’infrastructure complète d’App-V pour annuler la publication de l’application, les fichiers de catalogue des utilisateurs (catalogue d’ordinateurs pour les applications publiées globalement) sont supprimés, mais conserve l’emplacement et les emplacements de la boutique du package. Lorsque l’applet de cmdlet PowerShell `Remove-AppVClientPackge` est utilisée pour supprimer un package App-V, l’emplacement du magasin de packages est nettoyé. N’oubliez pas que l’annulation de la publication d’un package App-V à partir du serveur de gestion n’effectue aucune opération de suppression. Aucune opération ne supprime les fichiers de package du magasin de packages.

## <a href="" id="bkmk-roaming-reg-data"></a>Itinérance et Registre


App-V 5 est en mesure de fournir une version proche du natif lors de l’itinérance, en fonction du mode d’écriture de l’application utilisée. Par défaut, App-V est une itinérance qui est stockée dans l’emplacement d’itinérance en fonction de la configuration d’itinérance du système d’exploitation. D’autres emplacements pour le stockage des données basées sur des fichiers ne peuvent pas être déplacés de l’ordinateur vers l’ordinateur, car ils se trouvent dans des emplacements qui ne sont pas en itinérance.

### <a href="" id="bkmk-clt-inter-roam-reqs"></a>Configuration requise pour l’itinérance et stockage des données de catalogue utilisateur

App-V stocke les données, qui représentent l’état du catalogue de l’utilisateur, sous la forme:

-   Fichiers sous%appdata%\\Microsoft\\AppV\\Client\\Catalog

-   Paramètres du Registre sous `HKEY_CURRENT_USER\Software\Microsoft\AppV\Client\Packages`

Ensemble, ces fichiers et paramètres de Registre représentent le catalogue de l’utilisateur, ce qui signifie que les deux doivent être itinérants ou qu’aucun autre utilisateur ne doit être itinérant pour un utilisateur donné. App-V ne prend pas en charge l’itinérance% AppData%, mais pas l’itinérance du profil de l’utilisateur (registre), ou vice-versa.

**Remarques**  L’applet de **AppvClientPackage de réparation** ne répare pas l’état de publication des packages dans lesquels l’État App-V de l’utilisateur `HKEY_CURRENT_USER` est manquant ou ne correspond pas aux données dans% AppData%.

 

### Données basées sur le registre

L’itinérance de Registre dans App-V est divisée en deux scénarios, comme indiqué dans le tableau suivant.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Scénario</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Applications exécutées en tant qu’utilisateurs standard</p></td>
<td align="left"><p>Lorsqu’un utilisateur standard lance une application App-V, les applications HKLM et HKCU pour les applications App-V sont stockées dans la ruche HKCU de l’ordinateur. Ce qui s’affiche sous la forme de deux trajectoires distinctes:</p>
<ul>
<li><p>HKLM: HKCU\SOFTWARE\Classes\AppV\Client\Packages {PkgGUID} \ REGISTRY\MACHINE\SOFTWARE</p></li>
<li><p>HKCU: HKCU\SOFTWARE\Microsoft\AppV\Client\Packages {PkgGUID} \ REGISTRY\USER {UserSID} \ logiciel</p></li>
</ul>
<p>Les emplacements sont activés pour l’itinérance en fonction des paramètres du système d’exploitation.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Applications qui sont exécutées avec l’élévation</p></td>
<td align="left"><p>Lorsqu’une application est lancée avec l’élévation:</p>
<ul>
<li><p>Les données HKLM sont stockées dans la ruche HKLM de l’ordinateur local.</p></li>
<li><p>Les données HKCU sont stockées dans l’emplacement du registre de l’utilisateur</p></li>
</ul>
<p>Dans ce scénario, ces paramètres ne sont pas itinérants avec des configurations d’itinérance de système d’exploitation normales, et les valeurs et clés de Registre obtenues sont stockées à l’emplacement suivant:</p>
<ul>
<li><p>HKLM\SOFTWARE\Microsoft\AppV\Client\Packages {PkgGUID} {UserSID} \ REGISTRY\MACHINE\SOFTWARE</p></li>
<li><p>HKCU\SOFTWARE\Microsoft\AppV\Client\Packages {PkgGUID} \ Registry\User {UserSID} \ logiciel</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

### Redirection d’App-V et de dossiers

App-V 5,1 prend en charge la redirection de dossiers du dossier AppData Roaming (% AppData%). Lorsque l’environnement virtuel est démarré, l’État AppData d’itinérance du répertoire de l’itinérance de l’utilisateur est copié dans le cache local. À l’inverse, lorsque l’environnement virtuel est arrêté, le cache local associé au AppData d’itinérance d’un utilisateur particulier est transféré vers l’emplacement réel du répertoire AppData errant de cet utilisateur.

Un package standard comporte plusieurs emplacements mappés dans le magasin de stockage de l’utilisateur pour les paramètres à la fois dans AppData\\Local et AppData\\Roaming. Il s’agit de la copie de l’emplacement d’écriture qui est stockée par utilisateur dans le profil de l’utilisateur et qui est utilisée pour enregistrer les modifications apportées aux répertoires VFS du package et pour protéger le fichier VFS de package par défaut.

Le tableau suivant indique les emplacements local et d’itinérance, lorsque la redirection de dossiers n’a pas été implémentée.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Répertoire VFS dans le package</th>
<th align="left">Emplacement mappé du magasin de stockage</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>ProgramFilesX86</p></td>
<td align="left"><p>C:\users\jsmith\AppData &lt; Strong &gt; local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \ProgramFilesX86</p></td>
</tr>
<tr class="even">
<td align="left"><p>SystemX86</p></td>
<td align="left"><p>C:\users\jsmith\AppData &lt; Strong &gt; local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \SystemX86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows</p></td>
<td align="left"><p>C:\users\jsmith\AppData &lt; Strong &gt; local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \Windows</p></td>
</tr>
<tr class="even">
<td align="left"><p>appv_ROOT</p></td>
<td align="left"><p>C:\users\jsmith\AppData &lt; Strong &gt; local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \ appv_ROOT</p></td>
</tr>
<tr class="odd">
<td align="left"><p>AppData</p></td>
<td align="left"><p>C:\users\jsmith\AppData &lt; &gt; </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \AppData</p></td>
</tr>
</tbody>
</table>

 

 

Le tableau suivant répertorie les emplacements local et d’itinérance, lorsque la redirection de dossiers a été implémentée pour% AppData% et que l’emplacement a été redirigé (généralement vers un emplacement réseau).

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Répertoire VFS dans le package</th>
<th align="left">Emplacement mappé du magasin de stockage</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>ProgramFilesX86</p></td>
<td align="left"><p>C:\users\jsmith\AppData &lt; Strong &gt; local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \ProgramFilesX86</p></td>
</tr>
<tr class="even">
<td align="left"><p>SystemX86</p></td>
<td align="left"><p>C:\users\jsmith\AppData &lt; Strong &gt; local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \SystemX86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows</p></td>
<td align="left"><p>C:\users\jsmith\AppData &lt; Strong &gt; local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \Windows</p></td>
</tr>
<tr class="even">
<td align="left"><p>appv_ROOT</p></td>
<td align="left"><p>C:\users\jsmith\AppData &lt; Strong &gt; local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \ appv_ROOT</p></td>
</tr>
<tr class="odd">
<td align="left"><p>AppData</p></td>
<td align="left"><p><strong>\Fileserver </strong> \users\jsmith\roaming\Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \AppData</p></td>
</tr>
</tbody>
</table>

 

 

Le pilote de client virtuel App-V ne peut pas écrire sur les emplacements réseau, de sorte que le client App-V détecte la présence d’une redirection de dossier et copie les données sur le disque local lors de la publication et au démarrage de l’environnement virtuel. Après que l’utilisateur a fermé l’application application-V et que le client App-V ferme l’environnement virtuel, le stockage local de VFS AppData est copié sur le réseau, ce qui permet d’utiliser l’itinérance sur des ordinateurs supplémentaires dans lesquels le processus est répété. Les étapes détaillées des processus sont les suivantes:

1.  Lors du démarrage d’une publication ou d’un environnement virtuel, le client App-V détecte l’emplacement du répertoire AppData.

2.  Si le chemin d’accès AppData d’itinérance est local ou INO AppData\\Roaming location est mappé, rien ne se produit.

3.  Si le chemin d’accès AppData d’itinérance n’est pas local, le répertoire de VFS AppData est mappé au répertoire AppData Local.

Ce processus résout le problème de% AppData% non local qui n’est pas pris en charge par le pilote VFS du client App-V. Toutefois, les données stockées dans ce nouvel emplacement ne sont pas itinérantes lors de la redirection de dossiers. Les modifications apportées lors de l’exécution de l’application se produisent dans l’emplacement AppData Local et doivent être copiées à l’emplacement Redirigé. Les étapes détaillées du processus sont les suivantes:

1.  L’application application-V s’arrête, ce qui arrête l’environnement virtuel.

2.  Le cache local de l’emplacement AppData d’itinérance est compressé et est stocké dans un fichier ZIP.

3.  Un horodatage à la fin du processus d’empaquetage ZIP est utilisé pour nommer le fichier.

4.  L’horodatage est enregistré dans le registre: HKEY \ _CURRENT \ _USER \\Software\\Microsoft\\AppV\\Client\\Packages\\ &lt; GUID &gt; \\AppDataTime en tant que dernier horodatage connu de AppData.

5.  Le processus de redirection de dossier est appelé pour évaluer et lancer le fichier ZIP chargé dans le répertoire AppData d’itinérance.

La date d’horodatage est utilisée pour déterminer un scénario de dernier scripteur WINS s’il existe un conflit et est utilisé pour optimiser le téléchargement des données lors de la publication de l’application App-V ou de l’environnement virtuel. La redirection de dossiers rend les données accessibles à tous les autres clients couverts par la stratégie de prise en charge et démarre le processus de stockage des données AppData\\Roaming à l’emplacement AppData Local sur le client. Les processus détaillés sont les suivants:

1.  L’utilisateur démarre l’environnement virtuel en démarrant une application.

2.  L’environnement virtuel de l’application vérifie le fichier ZIP le plus récent, le cas échéant.

3.  Le Registre est consulté pour le dernier horodatage téléchargé connu, le cas échéant.

4.  Le fichier ZIP le plus récent est téléchargé, sauf si le dernier horodatage de chargement connu est supérieur ou égal à la date d’horodatage du fichier ZIP.

5.  Si le dernier horodatage connu connu est antérieur à celui du fichier ZIP le plus récent dans l’emplacement AppData d’itinérance, le fichier ZIP est extrait dans le répertoire temporaire local du profil de l’utilisateur.

6.  Après l’extraction réussie du fichier ZIP, le cache local de l’annuaire AppData d’itinérance est renommé et les nouvelles données sont déplacées vers l’emplacement.

7.  L’annuaire renommé est supprimé et l’application s’ouvre avec le plus dernier enregistrement de données AppData.

Cette opération complète l’itinérance réussie des paramètres d’application présents dans les emplacements AppData\\Roaming. La seule autre condition devant être adressée est une opération de réparation de package. Les détails du processus sont les suivants:

1.  Lors de la réparation, détecter si le chemin d’accès au répertoire de l’itinérance de l’utilisateur n’est pas local.

2.  Mapper les cibles de chemin d’accès AppData non locales sont recréées en tant qu’itinérance attendue et en local AppData.

3.  Supprimez l’estampille qui est stockée dans le registre, le cas échéant.

Ce processus permet de recréer les emplacements local et réseau pour AppData et de supprimer l’enregistrement de registre de l’estampille.

## <a href="" id="bkmk-clt-app-lifecycle"></a>Gestion du cycle de vie des applications du client App-V


Dans une infrastructure complète App-V, une fois les applications séquencées, elles sont gérées et publiées sur des utilisateurs ou des ordinateurs via la gestion de l’application-V et des serveurs de publication. Cette section détaille les opérations effectuées pendant les opérations courantes du cycle de vie des applications (ajout, publication, lancement, mise à niveau et suppression), ainsi que les emplacements de fichiers et de Registre modifiés et modifiés du point de vue du client App-V. Les opérations clientes App-V sont exécutées sous la forme d’une série de commandes PowerShell démarrées sur l’ordinateur exécutant le client App-V.

Ce document porte sur les solutions d’infrastructure complète App-V. Pour obtenir des informations spécifiques sur l’intégration d’App-V à Configuration Manager 2012, consultez la page suivante: <https://go.microsoft.com/fwlink/?LinkId=392773>

Les tâches du cycle de vie de l’application-V sont déclenchées lors de la connexion utilisateur (par défaut), au démarrage de l’ordinateur ou en tant qu’opérations chronométrées en arrière-plan. Les paramètres des opérations clientes App-V, y compris les serveurs de publication, les intervalles d’actualisation, l’activation du script de package, etc., sont configurés lors de l’installation du client ou après l’installation de commandes PowerShell. Pour plus d’informations sur le déploiement du [client App-V](how-to-deploy-the-app-v-client-51gb18030.md) et sur l’utilisation de PowerShell, voir la section déploiement du client sur TechNet:

```powershell
get-command *appv*
```

### Actualisation de la publication

Le processus d’actualisation de publication inclut plusieurs opérations plus petites effectuées sur le client App-V. Dans la mesure où App-V est une technologie de virtualisation des applications qui n’est pas une technologie de planification de tâches, le planificateur de tâches Windows est utilisé pour activer le processus lors de l’ouverture de session de l’utilisateur, au démarrage de l’ordinateur et aux intervalles prévus. Dans le cadre de l’installation, la configuration du client est la méthode recommandée lors de la distribution du client à un grand groupe d’ordinateurs avec les paramètres appropriés. Ces paramètres client peuvent être configurés avec les applets de commande PowerShell suivantes:

-   **Add-AppVPublishingServer:** Configure le client avec un serveur de publication App-V qui fournit des packages App-V.

-   **Set-AppVPublishingServer:** Modifie les paramètres actuels du serveur de publication App-V.

-   **Set-AppVClientConfiguration:** Modifie les paramètres actuels pour le client App-V.

-   **Synchronisation-AppVPublishingServer:** Démarre un processus d’actualisation de la publication de l’application V manuellement. Il est également utilisé dans les tâches planifiées créées lors de la configuration du serveur de publication.

Les sections suivantes permettent de détailler les opérations qui se produisent pendant différentes phases d’actualisation de la publication d’une application. Les rubriques suivantes sont disponibles:

-   Ajout d’un package App-V

-   Publication d’un package App-V

### Ajout d’un package App-V

L’ajout d’un package App-V au client est la première étape du processus d’actualisation de la publication. Le résultat final est le même que celui `Add-AppVClientPackage` de l’applet de commande dans PowerShell, sauf lors du processus d’actualisation de la publication, le serveur de publication configuré est contacté et transmet une liste d’applications de niveau supérieur au client pour extraire des informations plus détaillées et non une opération d’ajout de package unique. Le processus se poursuit en configurant le client pour les ajouts ou mises à jour d’un package ou d’un groupe de connexions, puis accède au fichier AppV. Ensuite, le contenu du fichier AppV est développé et placé sur le système d’exploitation local aux emplacements appropriés. Vous trouverez ci-dessous un flux de travail détaillé du processus, en supposant que le package est configuré pour le streaming de panne.

**Comment ajouter un package App-V**

1.  Initiation manuelle via PowerShell ou le lancement de séquence de tâches du processus d’actualisation de la publication.

    1.  Le client App-V effectue une connexion HTTP et demande une liste d’applications basées sur la cible. Le processus d’actualisation de publication prend en charge le ciblage des ordinateurs ou des utilisateurs.

    2.  Le serveur de publication App-V utilise l’identité de la cible, de l’utilisateur ou de l’ordinateur de lancement et interroge la base de données pour obtenir la liste des applications autorisées. La liste des applications est fournie sous la forme d’une réponse XML, que le client utilise pour envoyer des demandes supplémentaires au serveur pour plus d’informations sur chaque package.

2.  L’agent de publication sur le client App-V effectue toutes les actions ci-dessous sérialisées.

    Évaluez les groupes de connexion qui sont non publiés ou désactivés, car les mises à jour de version de package qui font partie du groupe de connexion ne peuvent pas être traitées.

3.  Configurez les packages en identifiant des opérations d’ajout ou de mise à jour.

    1.  Le client App-V utilise l’API AppX de Windows et accède au fichier AppV à partir du serveur de publication.

    2.  Le fichier de package est ouvert, et les AppXManifest.xml et les StreamMap.xml sont téléchargés vers le magasin de packages.

    3.  La publication de flux entièrement bloque les données définies dans le StreamMap.xml. Stocke les données de bloc de publication dans le package Store\\PkgGUID\\VerGUID\\Root.

        -   Icônes: cibles de points d’extension.

        -   En-têtes d’exécutable portables (en-têtes PE): cibles de points d’extension qui contiennent les informations de base relatives à l’image nécessaires sur le disque, accessibles directement ou via des types de fichiers.

        -   Scripts: Télécharger le répertoire scripts à utiliser tout au long du processus de publication.

    4.  Peuplez le magasin de packages:

        1.  Créez des fichiers épars sur le disque qui représentent le package extrait pour les répertoires répertoriés.

        2.  Déphasez les fichiers et répertoires de niveau supérieur sous racine.

        3.  Tous les autres fichiers sont créés lorsque le répertoire est répertorié comme incomplet sur le disque et en flux à la demande.

    5.  Créer des entrées de catalogue d’ordinateur. Créez le Manifest.xml et le DeploymentConfiguration.xml des fichiers du package (si aucun fichier DeploymentConfiguration.xml du package n’est créé).

    6.  Créer l’emplacement du magasin de packages dans le HKLM\\Software\\Microsoft\\AppV\\Client\\Packages\\PkgGUID\\Versions\\VerGUID\\Catalog Registre

    7.  Créer le fichier Registry. dat à partir du Windows Store vers%ProgramData%\\Microsoft\\AppV\\Client\\VReg\\ {VersionGUID}. dat

    8.  Inscrire le package avec le pilote en mode noyau App-V HKLM\\Microsoft\\Software\\AppV\\MAV

    9.  Appelez le script à partir du fichier AppxManifest.xml ou DeploymentConfig.xml pour le minutage d’ajout du package.

4.  Configurez les groupes de connexions en ajoutant et en activant ou en désactivant.

5.  Supprimez les objets qui ne sont pas publiés sur la cible (utilisateur ou ordinateur).

    **Remarques**  Cette opération n’entraîne pas la suppression d’un package, mais la suppression de points d’intégration pour la cible spécifique (utilisateur ou ordinateur) et la suppression des fichiers de catalogue d’utilisateurs (fichiers de catalogue d’ordinateur pour une publication internationale).

     

6.  Invoquez le montage de chargement en arrière-plan en fonction de la configuration du client.

7.  Les packages qui ont déjà des informations de publication pour l’ordinateur ou l’utilisateur sont immédiatement restaurés.

    **Remarques**  Cette condition est en tant que produit de suppression sans annuler la publication avec l’ajout en arrière-plan du package.

     

Cela a pour fin un ajout de package App-V à la publication. L’étape suivante consiste à publier le package sur la cible spécifique (ordinateur ou utilisateur).

![créer un fichier et des données de registre de package](images/packageaddfileandregistrydata.png)

### Publication d’un package App-V

Pendant l’opération d’actualisation de la publication, l’opération de publication spécifique (publication-AppVClientPackage) ajoute des entrées au catalogue d’utilisateurs, des cartes de habilitation pour l’utilisateur, identifie le magasin local et se termine en effectuant les étapes d’intégration. Les étapes suivantes sont détaillées.

**Publication d’un package App-V**

1.  Des entrées de package sont ajoutées au catalogue utilisateur

    1.  Packages ciblés par l’utilisateur: le UserDeploymentConfiguration.xml et le UserManifest.xml sont placés sur l’ordinateur dans le catalogue de l’utilisateur.

    2.  Packages d’ordinateur ciblé (Global): le UserDeploymentConfiguration.xml est placé dans le catalogue d’ordinateurs

2.  Inscrire le package avec le pilote du mode noyau pour l’utilisateur sur HKLM\\Software\\Microsoft\\AppV\\MAV

3.  Effectuer des tâches d’intégration.

    1.  Créer des points d’extension.

    2.  Stocker les informations de sauvegarde dans le registre de l’utilisateur et le profil d’itinérance (sauvegardes de raccourci).

        **Remarques**  Cela permet de restaurer les points d’extension si le package n’est pas publié.

         

    3.  Exécutez les scripts destinés au minutage de la publication.

La publication d’un package App-V qui fait partie d’un groupe de connexions est très similaire au processus ci-dessus. Pour les groupes de connexion, le chemin d’accès qui stocke les informations de catalogue spécifiques inclut PackageGroups en tant qu’enfant du répertoire de catalogue. Pour plus d’informations, consultez les informations du catalogue de l’ordinateur et des utilisateurs.

![créer un fichier et des données de Registre globales du package](images/packageaddfileandregistrydata-global.png)

### Lancement d’une application

Après le processus d’actualisation de publication, l’utilisateur lance, puis redémarre une application application-V. Le processus est très simple et optimisé pour le lancement rapide avec un trafic réseau minimal. Le client App-V vérifie le chemin d’accès au catalogue utilisateur pour les fichiers créés lors de la publication. Une fois que les droits d’ouverture du package sont établis, le client App-V crée un environnement virtuel, commence à diffuser en continu les données nécessaires et applique les fichiers de configuration de manifeste et de déploiement appropriés lors de la création de l’environnement virtuel. Après avoir créé et configuré l’environnement virtuel pour le package et l’application spécifiques, l’application démarre.

**Comment lancer des applications App-V**

1.  Un utilisateur lance l’application en cliquant sur un raccourci ou un appel de type de fichier.

2.  Le client App-V vérifie qu’il existe dans le catalogue utilisateur les fichiers suivants.

    -   UserDeploymentConfiguration.xml

    -   UserManifest.xml

3.  S’il s’agit d’un fichier, l’application est autorisée pour cet utilisateur et l’application démarre le processus pour le lancement. Il n’y a pas de trafic réseau à ce stade.

4.  Ensuite, le client App-V vérifie que le chemin d’accès du package enregistré pour le service client App-V est disponible dans le registre.

5.  Lors de la recherche du chemin d’accès au magasin de packages, l’environnement virtuel est créé. S’il s’agit du premier lancement, le bloc de fonctionnalité principal télécharge le cas échéant.

6.  Après le téléchargement, le service client App-V utilise les fichiers de configuration de manifeste et de déploiement pour configurer l’environnement virtuel et tous les sous-systèmes App-V chargés.

7.  L’application est lancée. Dans le cas de tous les fichiers manquants du magasin de packages (fichiers fragmentés), l’application-V va provoquer une erreur de flux sur les fichiers selon les besoins.

    ![fichier d’ajout de package et flux de données du Registre](images/packageaddfileandregistrydata-stream.png)

### Mise à niveau d’un package App-V

Le processus de mise à niveau du package App-V 5 diffère de l’ancienne version de App-V. App-V prend en charge plusieurs versions du même package sur un ordinateur habilité à différents utilisateurs. Les versions de package peuvent être ajoutées à tout moment, car le magasin de packages et les catalogues sont mis à jour avec les nouvelles ressources. Le seul processus spécifique à l’ajout de nouvelles ressources de version est l’optimisation du stockage. Lors d’une mise à niveau, seuls les nouveaux fichiers sont ajoutés à la nouvelle position du magasin de versions et les liens durs sont créés pour les fichiers non modifiés. Ainsi, le stockage global est réduit en ne présentant que le fichier à un emplacement sur le disque, puis en le projetant dans tous les dossiers avec une entrée d’emplacement du fichier sur le disque. Les détails spécifiques de la mise à niveau d’un package App-V sont les suivants:

**Comment mettre à niveau un package App-V**

1.  Le client App-V effectue une actualisation de publication et découvre une nouvelle version d’un package App-V.

2.  Des entrées de package sont ajoutées dans le catalogue approprié pour la nouvelle version

    1.  Packages ciblés par l’utilisateur: le UserDeploymentConfiguration.xml et le UserManifest.xml sont placés sur l’ordinateur dans le catalogue utilisateur sur appdata\\roaming\\Microsoft\\AppV\\Client\\Catalog\\Packages\\PkgGUID\\VerGUID

    2.  Packages d’ordinateur ciblé (Global): le UserDeploymentConfiguration.xml est placé dans le catalogue d’ordinateurs sur%programdata%\\Microsoft\\AppV\\Client\\Catalog\\Packages\\PkgGUID\\VerGUID

3.  Inscrire le package avec le pilote du mode noyau pour l’utilisateur sur HKLM\\Software\\Microsoft\\AppV\\MAV

4.  Effectuer des tâches d’intégration.

    -   Intégrez les points d’extensions (EP) à partir du manifeste et des fichiers de configuration dynamiques.

    1.  Les données EP basées sur des fichiers sont stockées dans le dossier AppData à l’aide de points de jonction du magasin de packages.

    2.  Le EPs version 1 existe déjà lorsqu’une nouvelle version est disponible.

    3.  Les points d’extension sont basculés vers l’emplacement version 2 dans les catalogues d’ordinateur ou d’utilisateur pour les points d’extension plus récents ou mis à jour.

5.  Exécutez les scripts destinés au minutage de la publication.

6.  Installez les assemblys côte à côte selon les besoins.

### Mise à niveau d’un package App-V d’application en cours d’utilisation

À **partir de App-V 5 SP2**: Si vous tentez de mettre à niveau un package utilisé par un utilisateur final, la tâche de mise à niveau est placée dans un État en attente. La mise à niveau sera exécutée plus tard, conformément aux règles suivantes:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Type de tâche</th>
<th align="left">Règle applicable</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Tâche basée sur l’utilisateur (par exemple, publication d’un package pour un utilisateur);</p></td>
<td align="left"><p>La tâche en attente sera exécutée après que l’utilisateur se déconnecte, puis se reconnecte.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Une tâche basée sur le monde (par exemple, l’activation globale d’un groupe de connexions);</p></td>
<td align="left"><p>La tâche en attente sera effectuée lorsque l’ordinateur sera arrêté, puis redémarré.</p></td>
</tr>
</tbody>
</table>

 

Lorsqu’une tâche est placée dans un état d’attente, le client App-V génère également une clé de Registre pour la tâche en attente, comme suit:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tâche basée sur le niveau utilisateur ou global</th>
<th align="left">Emplacement de génération de la clé de Registre</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Tâches basées sur l’utilisateur</p></td>
<td align="left"><p>KEY_CURRENT_USER \Software\Microsoft\AppV\Client\PendingTasks</p></td>
</tr>
<tr class="even">
<td align="left"><p>Tâches globalement basées</p></td>
<td align="left"><p>HKEY_LOCAL_MACHINE \Software\Microsoft\AppV\Client\PendingTasks</p></td>
</tr>
</tbody>
</table>

 

Les opérations suivantes doivent être effectuées pour que les utilisateurs puissent utiliser la version la plus récente du package:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tâche</th>
<th align="left">Détails</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Ajouter le package à l’ordinateur</p></td>
<td align="left"><p>Cette tâche est spécifique à un ordinateur et vous pouvez l’exécuter à tout moment en suivant les étapes décrites dans la section Ajouter un package ci-dessus.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Publier le package</p></td>
<td align="left"><p>Pour connaître les étapes à suivre, voir la section publication de package ci-dessus. Ce processus nécessite la mise à jour des points d’extension sur le système. Les utilisateurs finaux ne peuvent pas utiliser l’application une fois cette tâche terminée.</p></td>
</tr>
</tbody>
</table>

 

Utilisez les scénarios d’exemples suivants comme guide pour la mise à jour des packages.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Scénario</th>
<th align="left">Configuration requise</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Le package App-V n’est pas utilisé lorsque vous essayez de procéder à la mise à niveau</p></td>
<td align="left"><p>Aucun des composants suivants du package ne peut être utilisé: application virtuelle, serveur COM ou extensions d’interpréteur de commande.</p>
<p>L’administrateur publie une nouvelle version du package et la mise à niveau fonctionne lors du lancement suivant d’un composant ou d’une application dans le package. La nouvelle version du package est diffusée et exécutée. Aucune modification n’a été apportée dans ce scénario dans App-V 5 SP2 à partir des versions précédentes de App-V 5.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Le package App-V est en cours d’utilisation lorsque l’administrateur publie une nouvelle version du package</p></td>
<td align="left"><p>L’opération de mise à niveau est définie sur en attente par le client App-V, ce qui signifie qu’elle est mise en file d’attente et exécutée ultérieurement lorsque le package n’est pas en cours d’utilisation.</p>
<p>Si l’application de package est utilisée, l’utilisateur ferme l’application virtuelle à l’issue de laquelle la mise à niveau peut avoir lieu.</p>
<p>Si le package dispose d’extensions d’interpréteur de charge (Office 2013), qui sont chargées définitivement par l’Explorateur Windows, l’utilisateur ne peut pas se connecter. Les utilisateurs doivent se déconnecter, puis se reconnecter pour lancer la mise à niveau du package App-V.</p></td>
</tr>
</tbody>
</table>

 

### Publication globale et par utilisateur

Les packages App-V peuvent être publiés de l’une des deux manières suivantes: Utilisateur qui s’applique à un package App-V à un utilisateur ou à un groupe d’utilisateurs spécifiques et au monde qui applique le package App-V à l’ensemble de l’ordinateur pour tous les utilisateurs de l’ordinateur. Dès qu’une mise à niveau de package est en attente et que le package App-V n’est pas en cours d’utilisation, considérez les deux types de publication:

-   **Publiées globalement**: l’application est publiée sur un ordinateur; tous les utilisateurs de cet ordinateur peuvent l’utiliser. La mise à niveau aura lieu lorsque le service client App-V démarre, ce qui signifie qu’un redémarrage de l’ordinateur est efficace.

-   **Utilisateur publié**: l’application est publiée à un utilisateur. S’il existe plusieurs utilisateurs sur l’ordinateur, l’application peut être publiée dans un sous-ensemble d’utilisateurs. La mise à niveau se produit lorsque l’utilisateur se connecte ou qu’il est à nouveau publié (périodiquement, l’actualisation de la stratégie ConfigMgr et son évaluation, ou une mise à jour ou une actualisation périodique de l’application).

### Suppression d’un package App-V

La suppression d’applications App-V dans une infrastructure complète est une opération de dépublication qui n’effectue pas de suppression de package. Le processus est le même que le processus de publication ci-dessus, mais au lieu d’ajouter le processus de suppression inverse les modifications apportées pour les packages App-V.

### Réparation d’un package App-V

L’opération de réparation est très simple, mais peut affecter de nombreux emplacements sur l’ordinateur. Le cliché mentionné précédemment lors de l’écriture (vache) est supprimé et les points d’extension sont désintégrés, puis intégrés à nouveau. Veuillez consulter les emplacements de placement des données de COW en passant en revue les emplacements enregistrés dans le registre. Cette opération s’effectue automatiquement et il n’y a pas de contrôle d’administration à l’origine d’une opération de réparation à partir de la console cliente App-V ou via PowerShell (réparation-AppVClientPackage).

## <a href="" id="bkmk-integr-appv-pkgs"></a>Intégration des packages App-V


Le client et l’architecture du package App-V fournissent une intégration spécifique au système d’exploitation local lors de l’ajout et de la publication de packages. Trois fichiers définissent les points d’intégration ou d’extension d’un package App-V:

-   AppXManifest.xml: stockées à l’intérieur du package avec des copies de secours stockées dans le magasin de packages et le profil utilisateur. Contient les options créées lors du processus de séquençage.

-   DeploymentConfig.xml: fournit des informations de configuration pour les points d’extension d’intégration basés sur les ordinateurs et les utilisateurs.

-   UserConfig.xml: sous-ensemble de l' Deploymentconfig.xml qui fournit uniquement des configurations utilisateur et cibles uniquement aux points d’extension utilisateur.

### Règles d’intégration

Lorsque les applications App-V sont publiées sur un ordinateur avec le client App-V, certaines actions spécifiques se produisent comme décrit dans la liste ci-dessous:

-   Publication globale: les raccourcis sont stockés dans l’emplacement du profil de tous les utilisateurs et d’autres points d’extension sont stockés dans le registre dans la ruche HKLM.

-   Publication des utilisateurs: les raccourcis sont stockés dans le profil de compte d’utilisateur actuel et d’autres points d’extension sont stockés dans le registre dans la ruche HKCU.

-   Sauvegarde et restauration: les données d’application natives existantes et le registre (par exemple, les inscriptions FTA) sont sauvegardés lors de la publication.

    1.  La propriété des packages App-V est attribuée en fonction du dernier package intégré pour lequel la propriété est transmise à la dernière application publiée par l’application.

    2.  Le transfert de propriété d’un package App-V à un autre lorsque le package App-V propriétaire n’est pas publié. Cette opération n’entraîne pas de restauration des données et du Registre.

    3.  Restaurez les données sauvegardées lorsque le dernier package n’est pas publié ou supprimé par point d’extension.

### Points d’extension

Les fichiers de publication App-V (manifeste et configuration dynamique) fournissent plusieurs points d’extension permettant à l’application d’être intégré au système d’exploitation local. Ces points d’extension effectuent des tâches standard d’installation des applications, telles que le placement de raccourcis, la création d’associations de types de fichiers et l’inscription des composants. Étant donné qu’il s’agit d’applications virtualisées qui ne sont pas installées de la même manière qu’une application traditionnelle, il existe des différences. La liste suivante répertorie les points d’extension abordés dans cette section:

-   Associés

-   Associations de types de fichiers

-   Extensions d’environnement

-   MODÈLE

-   Clients logiciels

-   Fonctionnalités des applications

-   Gestionnaire de protocole d’URL

-   AppPath

-   Application virtuelle

### Associés

Le raccourci est l’un des éléments de base de l’intégration avec le système d’exploitation et est l’interface pour le lancement d’une application application V directe par un utilisateur. Lors de la publication et de la dépublication des applications App-V.

À partir du manifeste du package et des fichiers XML de configuration dynamique, le chemin d’accès au fichier exécutable d’une application spécifique se trouve dans une section semblable à ce qui suit:

```xml
<Extension Category="AppV.Shortcut">
          <Shortcut>
            <File>[{Common Desktop}]\Adobe Reader 9.lnk</File>
            <Target>[{AppVPackageRoot}]\Reader\AcroRd32.exe</Target>
            <Icon>[{Windows}]\Installer\{AC76BA86-7AD7-1033-7B44-A94000000001}\SC_Reader.ico</Icon>
            <Arguments />
            <WorkingDirectory />
            <ShowCommand>1</ShowCommand>
            <ApplicationId>[{AppVPackageRoot}]\Reader\AcroRd32.exe</ApplicationId>
          </Shortcut>
        </Extension>
```

Comme indiqué précédemment, les raccourcis de l’application-V sont placés par défaut dans le profil de l’utilisateur en fonction de l’opération d’actualisation. Actualisation globale place les raccourcis dans le profil tous les utilisateurs et l’actualisation des utilisateurs dans le profil de l’utilisateur concerné. Le fichier exécutable réel est stocké dans le Windows Store. L’emplacement du fichier ICO est un emplacement sous-jeton dans le package App-V.

### Associations de types de fichiers

Le client App-V gère les associations de types de fichiers du système d’exploitation local lors de la publication, ce qui permet aux utilisateurs d’utiliser des appels de type de fichier ou d’ouvrir un fichier à l’aide d’une extension spécifiquement inscrite (. docx) pour démarrer une application application-V. Des associations de types de fichiers sont disponibles dans les fichiers de configuration de manifeste et de configuration dynamique, comme illustré dans l’exemple ci-dessous:

```xml
<Extension Category="AppV.FileTypeAssociation">
          <FileTypeAssociation>
            <FileExtension MimeAssociation="true">
              <Name>.xdp</Name>
              <ProgId>AcroExch.XDPDoc</ProgId>
              <ContentType>application/vnd.adobe.xdp+xml</ContentType>
            </FileExtension>
            <ProgId>
              <Name>AcroExch.XDPDoc</Name>
              <Description>Adobe Acrobat XML Data Package File</Description>
              <EditFlags>65536</EditFlags>
              <DefaultIcon>[{Windows}]\Installer\{AC76BA86-7AD7-1033-7B44-A94000000001}\XDPFile_8.ico</DefaultIcon>
              <ShellCommands>
                <DefaultCommand>Read</DefaultCommand>
                <ShellCommand>
                  <ApplicationId>[{AppVPackageRoot}]\Reader\AcroRd32.exe</ApplicationId>
                  <Name>Open</Name>
                  <CommandLine>"[{AppVPackageRoot}]\Reader\AcroRd32.exe" "%1"</CommandLine>
                </ShellCommand>
                <ShellCommand>
                  <ApplicationId>[{AppVPackageRoot}]\Reader\AcroRd32.exe</ApplicationId>
                  <Name>Printto</Name>
                  <CommandLine>"[{AppVPackageRoot}]\Reader\AcroRd32.exe"  /t "%1" "%2" "%3" "%4"</CommandLine>
                </ShellCommand>
                <ShellCommand>
                  <ApplicationId>[{AppVPackageRoot}]\Reader\AcroRd32.exe</ApplicationId>
                  <Name>Read</Name>
                  <FriendlyName>Open with Adobe Reader 9</FriendlyName>
                  <CommandLine>"[{AppVPackageRoot}]\Reader\AcroRd32.exe" "%1"</CommandLine>
                </ShellCommand>
              </ShellCommands>
            </ProgId>
          </FileTypeAssociation>
        </Extension>
```

**Remarques**  Dans cet exemple:

-   `<Name>.xdp</Name>` est l’extension

-   `<Name>AcroExch.XDPDoc</Name>` est la valeur ProgId (qui pointe vers l’ID de PROG adjacent)

-   `<CommandLine>"[{AppVPackageRoot}]\Reader\AcroRd32.exe" "%1"</CommandLine>` est la ligne de commande, qui pointe vers l’exécutable de l’application

 

### Extensions d'environnement

Les extensions d’interpréteur sont incorporées automatiquement dans le package lors du processus de séquençage. Lorsque le package est publié globalement, l’extension de l’interpréteur de Shell donne aux utilisateurs les mêmes fonctionnalités que si l’application a été installée localement. L’application ne nécessite aucune installation ou configuration supplémentaire sur le client pour activer la fonctionnalité d’extension du shell.

**Configuration requise pour l’utilisation des extensions d’interpréteur de tâches:**

-   Les packages contenant des extensions d’interpréteur de Troie doivent être publiés globalement.

-   Le nombre de bits d’application, de Sequencer et de client App-V doit correspondre ou les extensions de Shell ne fonctionnent pas. Exemple:

    -   La version de l’application est 64 bits.

    -   Le Sequencer s’exécute sur un ordinateur 64 bits.

    -   Le package est remis à un ordinateur client d’application 64 bits.

Le tableau suivant répertorie les extensions d’environnement prises en charge.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Gestionnaire d'</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Gestionnaire de menu contextuel</p></td>
<td align="left"><p>Ajoute des éléments de menu dans le menu contextuel. Il est appelé avant que le menu contextuel ne s’affiche.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Gestionnaire de glisser-déplacer</p></td>
<td align="left"><p>Contrôle l’action dès que vous cliquez avec le bouton droit sur un glisser-déplacer, puis modifie le menu contextuel qui s’affiche.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Supprimer le gestionnaire de cibles</p></td>
<td align="left"><p>Contrôle l’action après le glissement et la suppression d’un objet de données sur une cible de dépôt telle qu’un fichier.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Gestionnaire d’objets de données</p></td>
<td align="left"><p>Contrôle l’action après la copie d’un fichier dans le presse-papiers ou le glisser-déplacer sur une cible de déplacement. Il peut fournir des formats de presse-papiers supplémentaires à la cible de dépôt.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Gestionnaire de feuilles de propriétés</p></td>
<td align="left"><p>Remplace ou ajoute des pages dans la boîte de dialogue feuille de propriétés d’un objet.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Gestionnaire d’info-bulle</p></td>
<td align="left"><p>Permet de récupérer les indicateurs et les informations de l’info-bulle d’un élément et de l’afficher dans une info-bulle contextuelle lors du survol de la souris.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Gestionnaire de colonnes</p></td>
<td align="left"><p>Autorise la création et l’affichage de colonnes personnalisées dans l’affichage détaillé de l’Explorateur Windows <em> </em> . Elle peut être utilisée pour étendre le tri et le regroupement.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Gestionnaire d’aperçu</p></td>
<td align="left"><p>Permet d’afficher un aperçu d’un fichier dans le volet de visualisation de l’Explorateur Windows.</p></td>
</tr>
</tbody>
</table>

 

### MODÈLE

Le client App-V prend en charge la publication d’applications grâce à la prise en charge de l’intégration COM et de la virtualisation. L’intégration COM permet au client App-V d’inscrire des objets COM sur le système d’exploitation local et la virtualisation des objets. Dans le cadre de ce document, l’intégration d’objets COM nécessite des informations supplémentaires.

App-V prend en charge l’enregistrement d’objets COM du package sur le système d’exploitation local avec deux types de processus: hors processus et in-process. L’enregistrement d’objets COM s’effectue à l’aide d’un ou de plusieurs modes d’opération pour un package App-V spécifique incluant désactivé, isolé et intégré. Le mode intégré est configuré pour le type hors processus ou in-process. La configuration des types et modes COM s’effectue à l’aide des fichiers de configuration dynamiques (deploymentconfig.xml ou userconfig.xml).

Des informations sur l’intégration d’App-V sont disponibles à l’adresse suivante: <https://go.microsoft.com/fwlink/?LinkId=392834> .

### Clients logiciels et fonctionnalités d’application

App-V prend en charge des clients logiciels et des points d’extension de fonctionnalités d’application spécifiques qui permettent aux applications virtualisées d’être inscrites auprès du client logiciel du système d’exploitation. Cela permet aux utilisateurs de sélectionner des programmes par défaut pour les opérations telles que la messagerie, la messagerie instantanée et le lecteur multimédia. Cette opération est effectuée dans le panneau de configuration avec les valeurs par défaut de l’accès au programme et aux paramètres d’ordinateur, puis configurées lors du séquençage dans les fichiers de configuration de manifeste ou dynamiques. Les fonctionnalités d’application sont uniquement prises en charge lorsque les applications App-V sont publiées globalement.

Exemple d’inscription d’un client de messagerie application par le logiciel

```xml
    <SoftwareClients Enabled="true">
      <ClientConfiguration EmailEnabled="true" />
      <Extensions>
        <Extension Category="AppV.SoftwareClient">
          <SoftwareClients>
            <EMail MakeDefault="true">
              <Name>Mozilla Thunderbird</Name>
              <Description>Mozilla Thunderbird</Description>
              <DefaultIcon>[{ProgramFilesX86}]\Mozilla Thunderbird\thunderbird.exe,0</DefaultIcon>
              <InstallationInformation>
                <RegistrationCommands>
                  <Reinstall>"[{ProgramFilesX86}]\Mozilla Thunderbird\uninstall\helper.exe" /SetAsDefaultAppGlobal</Reinstall>
                  <HideIcons>"[{ProgramFilesX86}]\Mozilla Thunderbird\uninstall\helper.exe" /HideShortcuts</HideIcons>
                  <ShowIcons>"[{ProgramFilesX86}]\Mozilla Thunderbird\uninstall\helper.exe" /ShowShortcuts</ShowIcons>
                </RegistrationCommands>
                <IconsVisible>1</IconsVisible>
                <OEMSettings />
              </InstallationInformation>
              <ShellCommands>
                <ApplicationId>[{ProgramFilesX86}]\Mozilla Thunderbird\thunderbird.exe</ApplicationId>
                <Open>"[{ProgramFilesX86}]\Mozilla Thunderbird\thunderbird.exe" -mail</Open>
              </ShellCommands>
              <MAPILibrary>[{ProgramFilesX86}]\Mozilla Thunderbird\mozMapi32_InUse.dll</MAPILibrary>
              <MailToProtocol>
                <Description>Thunderbird URL</Description>
                <EditFlags>2</EditFlags>
                <DefaultIcon>[{ProgramFilesX86}]\Mozilla Thunderbird\thunderbird.exe,0</DefaultIcon>
                <ShellCommands>
                  <ApplicationId>[{ProgramFilesX86}]\Mozilla Thunderbird\thunderbird.exe</ApplicationId>
                  <Open>"[{ProgramFilesX86}]\Mozilla Thunderbird\thunderbird.exe" -osint -compose "%1"</Open>
                </ShellCommands>
              </MailToProtocol>
            </EMail>
          </SoftwareClients>
        </Extension>
      </Extensions>
    </SoftwareClients>
```

**Remarques**  Dans cet exemple:

-   `<ClientConfiguration EmailEnabled="true" />` est le paramètre global des clients logiciels pour intégrer les clients de messagerie

-   `<EMail MakeDefault="true">` est l’indicateur permettant de définir un client de messagerie particulier en tant que client de messagerie par défaut.

-   `<MAPILibrary>[{ProgramFilesX86}]\Mozilla Thunderbird\mozMapi32_InUse.dll</MAPILibrary>` est l’inscription de la dll MAPI

 

### Gestionnaire de protocole d’URL

Les applications ne sont pas toujours appelées applications virtuelles à l’aide d’un appel de type de fichier. Par exemple, dans une application qui prend en charge l’incorporation d’un lien mailto: à l’intérieur d’un document ou d’une page Web, l’utilisateur clique sur un lien mailto: et attend qu’il dispose d’un client de messagerie enregistré. App-V prend en charge les gestionnaires de protocole d’URL qui peuvent être inscrits en fonction de chaque package avec le système d’exploitation local. Lors du séquençage, les gestionnaires de protocole d’URL sont automatiquement ajoutés au package.

Dans le cas où plusieurs applications peuvent inscrire le gestionnaire de protocole d’URL spécifique, les fichiers de configuration dynamique peuvent être utilisés pour modifier le comportement et supprimer ou désactiver cette fonctionnalité pour une application qui ne doit pas être lancée.

### AppPath

Le point d’extension AppPath prend en charge l’appel des applications App-V directement à partir du système d’exploitation. Pour ce faire, vous devez généralement effectuer cette opération à partir de l’écran de démarrage ou d’ouverture, en fonction du système d’exploitation, qui permet aux administrateurs de fournir un accès aux applications App-V à partir de commandes ou de scripts du système d’exploitation sans appeler le chemin d’accès spécifique au fichier exécutable. Par conséquent, il n’est pas nécessaire de modifier la variable d’environnement de chemin d’accès système sur tous les systèmes, car elle est effectuée lors de la publication.

Le point d’extension AppPath est configuré dans le manifeste ou dans les fichiers de configuration dynamique et est stocké dans le registre de l’ordinateur local lors de la publication de l’utilisateur. Pour plus d’informations sur la révision de AppPath: <https://go.microsoft.com/fwlink/?LinkId=392835> .

### Application virtuelle

Ce sous-système fournit une liste des applications capturées lors du séquençage qui sont généralement consommées par d’autres composants App-V. L’intégration de points d’extension qui appartiennent à une application particulière peut être désactivée à l’aide de fichiers de configuration dynamiques. Par exemple, dans le cas d’un package contenant deux applications, il est possible de désactiver tous les points d’extension d’une application afin de permettre uniquement l’intégration de points d’extension d’autres applications.

### Règles de point d’extension

Les points d’extension décrits ci-dessus sont intégrés au système d’exploitation en fonction de la façon dont les packages ont été publiés. La publication globale place les points d’extension dans les emplacements des machines publiques, où la publication des utilisateurs place des points d’extension dans les emplacements des utilisateurs. Par exemple, un raccourci qui est créé sur le bureau et publié globalement aura pour effet de générer le raccourci (%Public%\\Desktop) et les données de Registre (HKLM\\Software\\Classes). Le même raccourci aurait des données de fichier (%UserProfile%\\Desktop) et des données de Registre (HKCU\\Software\\Classes).

Les points d’extension ne sont pas tous publiés de la même façon, dans la mesure où certains points d’extension nécessitent une publication globale et d’autres le séquençage sur le système d’exploitation et l’architecture spécifiques où ils sont remis. Vous trouverez ci-dessous un tableau qui décrit ces deux règles clés.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Extension virtuelle</th>
<th align="left">Nécessite le séquençage du système d’exploitation cible</th>
<th align="left">Nécessite une publication globale</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Raccourci</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Association de type de fichier</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Protocoles d’URL</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>AppPaths</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Mode COM</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Client logiciel</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Fonctionnalités des applications</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
</tr>
<tr class="even">
<td align="left"><p>Gestionnaire de menu contextuel</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Gestionnaire de glisser-déplacer</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Gestionnaire d’objets de données</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Gestionnaire de feuilles de propriétés</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Gestionnaire d’info-bulle</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Gestionnaire de colonnes</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Extensions d’environnement</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Objet d’assistance du navigateur</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
</tr>
<tr class="even">
<td align="left"><p>Objet Active X</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-dynamic-config"></a>Traitement dynamique des configurations


Le déploiement de packages App-V sur un ordinateur ou un utilisateur est très simple. Toutefois, au fur et à mesure que des organisations déploient des applications AppV sur des lignes métiers et des frontières géographiques et politiques, la possibilité de séquencer une application une seule fois avec un ensemble de paramètres devient impossible. App-V a été conçu pour ce scénario, au fur et à mesure de la capture de paramètres et configurations spécifiques lors du séquençage dans le fichier manifeste, mais également de la modification de fichiers de configuration dynamique.

La configuration dynamique App-V permet de spécifier une stratégie pour un package au niveau de l’ordinateur ou au niveau de l’utilisateur. Les fichiers de configuration dynamiques permettent aux ingénieurs de séquençage de modifier la configuration d’un package, après le séquençage, afin de répondre aux besoins des groupes d’utilisateurs ou de machines individuels. Dans certains cas, il est possible que les modifications apportées à l’application fournissent des fonctionnalités appropriées au sein de l’environnement App-V. Par exemple, il se peut qu’il soit nécessaire de modifier les fichiers \ _ \ * config.xml pour permettre l’exécution de certaines actions à une heure spécifique au cours de l’exécution de l’application, par exemple, la désactivation d’une extension mailto pour empêcher une application virtualisée de remplacer cette extension par une autre application.

Les packages App-V contiennent le fichier manifeste dans le fichier de package AppV, qui est représentatif des opérations de séquençage et est la stratégie de choix à moins que les fichiers de configuration dynamique ne soient assignés à un package spécifique. Après le séquençage, les fichiers de configuration dynamique peuvent être modifiés pour permettre la publication d’une application sur des ordinateurs de bureau ou des utilisateurs différents. Les deux fichiers de configuration dynamiques sont les fichiers de configuration de déploiement dynamique (DDC) et de configuration de l’utilisateur dynamique (DUC). Cette section porte sur la combinaison des fichiers de configuration de manifeste et de configuration dynamique.

### Exemple pour les fichiers de configuration dynamiques

L’exemple ci-dessous montre la combinaison du manifeste, de la configuration du déploiement et des fichiers de configuration utilisateur après la publication et l’opération normale. Ces exemples sont des exemples abrégés de chacun des fichiers. L’objectif est de montrer la combinaison des fichiers uniquement et de ne pas être une description complète des catégories spécifiques disponibles dans chacun des fichiers. Pour plus d’informations, reportez-vous au Guide de séquençage de l’App-V 5 à l’adresse suivante: <https://go.microsoft.com/fwlink/?LinkID=269810>

**Manifeste**

```xml
<appv:Extension Category="AppV.Shortcut">
     <appv:Shortcut>
          <appv:File>[{Common Programs}]\7-Zip\7-Zip File Manager.lnk</appv:File>
          <appv:Target>[{AppVPackageRoot}]\7zFM.exe</appv:Target>
          <appv:Icon>[{AppVPackageRoot}]\7zFM exe.O.ico</appv:Icon>
     </appv:Shortcut>
</appv:Extension>
```

**Configuration du déploiement**

```xml
<MachineConfiguration>
     <Subsystems>
          <Registry>
               <Include>
                    <Key Path= "\REGISTRY\Machine\Software\7zip">
                    <Value Type="REG_SZ" Name="Config" Data="1234"/>
                    </Key>
               </Include>
          </Registry>
     </Subsystems>
```

**Configuration utilisateur**

```xml
<UserConfiguration>
     <Subsystems>
<appv:ExtensionCategory="AppV.Shortcut">
     <appv:Shortcut>
          <appv:File>[{Desktop}]\7-Zip\7-Zip File Manager.lnk</appv:File>
          <appv:Target>[{AppVPackageRoot}]\7zFM.exe</appv:Target>
          <appv:Icon>[{AppVPackageRoot}]\7zFM exe.O.ico</appv:Icon>
     </appv:Shortcut>
</appv:Extension>
     </Subsystems>
<UserConfiguration>
     <Subsystems>
<appv:Extension Category="AppV.Shortcut">
     <appv:Shortcut>
          <appv:Fìle>[{Desktop}]\7-Zip\7-Zip File Manager.lnk</appv:File>
          <appv:Target>[{AppVPackageRoot}]\7zFM.exe</appv:Target>
          <appv:Icon>[{AppVPackageRoot}]\7zFM.exe.O.ico</appv:Icon>
     </appv:Shortcut>
     <appv:Shortcut>
          <appv:File>[{Common Programs}]\7-Zip\7-Zip File Manager.Ink</appv:File>
          <appv:Target>[{AppVPackageRoot}]\7zFM.exe</appv:Target>
          <appv:Icon>[{AppVPackageRoot)]\7zFM.exe.O.ico</appv: Icon>
     </appv:Shortcut>
</appv:Extension>
     </Subsystems>
<MachineConfiguration>
     <Subsystems>
          <Registry>
               <Include>
                    <Key Path="\REGISTRY\Machine\Software\7zip">
                    <Value Type=”REG_SZ" Name="Config" Data="1234"/>
               </Include>
          </Registry>
     </Subsystems>
```

## <a href="" id="bkmk-sidebyside-assemblies"></a>Assemblys côte à côte


App-V prend en charge l’emballage automatique d’assemblys côte à côte (SxS) lors du séquençage et du déploiement sur le client lors de la publication d’applications virtuelles. App-V 5 SP2 prend en charge la capture d’assemblys SxS lors du séquençage pour les assemblys non présents sur l’ordinateur de séquençage. Quant aux assemblys qui se composent de Visual C++ (version 8 et version ultérieure) et/ou du runtime MSXML, le Sequencer détectera et capturera automatiquement ces dépendances, même si celles-ci n’ont pas été installées lors de l’analyse. La fonctionnalité d’assemblys côte à côte supprime les limitations relatives aux versions précédentes d’App-V, car le Sequencer App-V n’a pas pu capturer les assemblys déjà présents sur la station de travail de séquençage et en privatisation les assemblys limités à une version de bit par package. Ce comportement entraînait le déploiement d’applications App-V pour les clients ayant manquant les assemblys SxS requis, provoquant des échecs de lancement d’applications. Cela forcé le processus d’empaquetage de document, puis de s’assurer que tous les assemblys requis pour les packages étaient installés localement sur le système d’exploitation client de l’utilisateur pour garantir la prise en charge des applications virtuelles. En fonction du nombre d’assemblys et de la documentation de l’application associée aux dépendances requises, cette tâche était une demande de gestion et d’implémentation.

La prise en charge des assemblys côte à côte dans App-V comporte les fonctionnalités suivantes.

-   Capture automatique de l’assembly SxS lors du séquençage, qu’il s’agisse d’un assembly ou d’un assembly déjà installé sur la station de travail de séquençage.

-   Le client App-V installe automatiquement les assemblys SxS requis sur l’ordinateur client au moment de la publication.

-   Le Sequencer signale la dépendance au moment de l’exécution VC dans le mécanisme de création de rapports de Sequencer.

-   Le Sequencer autorise ne pas empaqueter les assemblys déjà installés sur le Sequencer, qui prennent en charge les scénarios dans lesquels les assemblys ont déjà été installés sur les ordinateurs cibles.

### Publication automatique d’assemblys SxS

Lors de la publication d’un package App-V avec des assemblys SxS, le client App-V vérifie la présence de l’assembly sur l’ordinateur. S’il n’existe pas, le client déploie l’assembly vers l’ordinateur. Les packages qui font partie des groupes de connexion dépendent des installations d’assemblys côte à côte qui font partie des packages de base, car le groupe de connexion ne contient aucune information sur l’installation de l’assembly.

**Remarques**  L’annulation de la publication ou de la suppression d’un package avec un assembly ne supprime pas les assemblys pour ce package.

 

## <a href="" id="bkmk-client-logging"></a>Journalisation du client


Le client App-V enregistre les informations dans le journal des événements Windows au format ETW standard. Pour plus d’informations, reportez-vous à l’observateur d’événements, sous applications et services Logs\\Microsoft\\AppV\\Client.

**Remarques**  Dans App-V 5,0 SP3, certains journaux ont été consolidés et déplacés vers l’emplacement suivant:

`Event logs/Applications and Services Logs/Microsoft/AppV/ServiceLog`

Pour obtenir la liste des journaux déplacés, voir [à propos de App-V 5,0 SP3](about-app-v-50-sp3.md#bkmk-event-logs-moved).

 

Il existe trois catégories spécifiques d’événements enregistrés décrits ci-dessous.

**Administrateur**: consigne les événements relatifs aux configurations appliquées au client App-V, et contient les principales erreurs et les avertissements.

**Opérationnel**: consigne l’exécution générale de l’application et l’utilisation des composants individuels créant un journal d’audit des opérations App-v exécutées sur le client App-v.

**Application virtuelle**: consigne le lancement d’applications virtuelles et l’utilisation de sous-systèmes de virtualisation.






 

 





