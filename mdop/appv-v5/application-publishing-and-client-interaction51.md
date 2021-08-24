---
title: Publication d’applications et interaction avec le Client
description: Publication d’applications et interaction avec le Client
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
ms.openlocfilehash: b94ef87043d428ac92fe1656b3afeb8a8b743808
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910819"
---
# <a name="application-publishing-and-client-interaction"></a>Publication d’applications et interaction avec le Client


Cet article fournit des informations techniques sur les opérations courantes du client App-V et leur intégration avec le système d’exploitation local.

-   [Fichiers de package App-V créés par Sequencer](#bkmk-appv-pkg-files-list)

-   [Qu’y a-t-il dans le fichier appv ?](#bkmk-appv-file-contents)

-   [Emplacements de stockage de données client App-V](#bkmk-files-data-storage)

-   [Registre de package](#bkmk-pkg-registry)

-   [Comportement du magasin de packages App-V](#bkmk-pkg-store-behavior)

-   [Registre et données itinérants](#bkmk-roaming-reg-data)

-   [Gestion du cycle de vie des applications clientes App-V](#bkmk-clt-app-lifecycle)

-   [Intégration des packages App-V](#bkmk-integr-appv-pkgs)

-   [Traitement de configuration dynamique](#bkmk-dynamic-config)

-   [Assemblys côte à côte](#bkmk-sidebyside-assemblies)

-   [Journalisation du client](#bkmk-client-logging)

Pour plus d’informations de référence, voir la page de téléchargement des ressources de documentation de [Microsoft Application Virtualization (App-V).](https://www.microsoft.com/download/details.aspx?id=27760)

## <a name="app-v-package-files-created-by-the-sequencer"></a><a href="" id="bkmk-appv-pkg-files-list"></a>Fichiers de package App-V créés par Sequencer


Sequencer crée des packages App-V et produit une application virtualisée. Le processus de séquençage crée les fichiers suivants :

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
<td align="left"><p>.appv</p></td>
<td align="left"><ul>
<li><p>Le fichier de package principal, qui contient les ressources capturées et les informations d’état du processus de séquençage.</p></li>
<li><p>Architecture du fichier de package, informations de publication et registre sous forme de jetons qui peuvent être réapplées à un ordinateur et à un utilisateur spécifique lors de la remise.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>.MSI</p></td>
<td align="left"><p>Wrapper de déploiement exécutable que vous pouvez utiliser pour déployer des fichiers .appv manuellement ou à l’aide d’une plateforme de déploiement tierce.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>_DeploymentConfig.XML</p></td>
<td align="left"><p>Fichier utilisé pour personnaliser les paramètres de publication par défaut de toutes les applications d’un package déployé globalement pour tous les utilisateurs sur un ordinateur qui exécute le client App-V.</p></td>
</tr>
<tr class="even">
<td align="left"><p>_UserConfig.XML</p></td>
<td align="left"><p>Fichier utilisé pour personnaliser les paramètres de publication de toutes les applications d’un package déployé sur un utilisateur spécifique sur un ordinateur exécutant le client App-V.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Report.xml</p></td>
<td align="left"><p>Résumé des messages résultant du processus de séquençage, y compris les pilotes, fichiers et emplacements de Registre omis.</p></td>
</tr>
<tr class="even">
<td align="left"><p>.CAB</p></td>
<td align="left"><p><em>Facultatif : fichier accélérateur de package utilisé pour reconstruire automatiquement un </em> package d’application virtuelle précédemment séquencé.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>.appvt</p></td>
<td align="left"><p><em>Facultatif : </em> fichier de modèle sequenceur utilisé pour conserver les paramètres sequencer couramment réutilisés.</p></td>
</tr>
</tbody>
</table>

 

Pour plus d’informations sur le séquencement, voir [le Guide de séquencement d’Application Virtualization.](https://go.microsoft.com/fwlink/?LinkID=269810)

## <a name="whats-in-the-appv-file"></a><a href="" id="bkmk-appv-file-contents"></a>Qu’y a-t-il dans le fichier appv ?


Le fichier appv est un conteneur qui stocke les fichiers XML et non XML ensemble dans une seule entité. Ce fichier est créé à partir du format AppX, qui est basé sur la norme OPC (Open Packaging Conventions).

Pour afficher le contenu du fichier appv, copiez le package, puis renommez le fichier copié en extension ZIP.

Le fichier appv contient les dossiers et fichiers suivants, qui sont utilisés lors de la création et de la publication d’une application virtuelle :

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
<td align="left"><p>Répertoire qui contient le système de fichiers pour l’application virtualisée capturée pendant le séquençage.</p></td>
</tr>
<tr class="even">
<td align="left"><p>[Content_Types].xml</p></td>
<td align="left"><p>Fichier XML</p></td>
<td align="left"><p>Liste des principaux types de contenu dans le fichier appv (par exemple, DLL, EXE, BIN).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>AppxBlockMap.xml</p></td>
<td align="left"><p>Fichier XML</p></td>
<td align="left"><p>Disposition du fichier appv, qui utilise des éléments File, Block et BlockMap qui permettent l’emplacement et la validation des fichiers dans le package App-V.</p></td>
</tr>
<tr class="even">
<td align="left"><p>AppxManifest.xml</p></td>
<td align="left"><p>Fichier XML</p></td>
<td align="left"><p>Métadonnées du package qui contient les informations requises pour l’ajout, la publication et le lancement du package. Inclut les points d’extension (associations de types de fichiers et raccourcis) et les noms et LES GUID associés au package.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>FilesystemMetadata.xml</p></td>
<td align="left"><p>Fichier XML</p></td>
<td align="left"><p>Liste des fichiers capturés lors du séquençage, y compris les attributs (par exemple, répertoires, fichiers, répertoires opaques, répertoires vides et noms longs et courts).</p></td>
</tr>
<tr class="even">
<td align="left"><p>PackageHistory.xml</p></td>
<td align="left"><p>Fichier XML</p></td>
<td align="left"><p>Informations sur l’ordinateur de séquençage (version du système d’exploitation, version d’Internet Explorer, version de .Net Framework) et processus (mise à niveau, version du package).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Registry.dat</p></td>
<td align="left"><p>Fichier DAT</p></td>
<td align="left"><p>Clés de Registre et valeurs capturées pendant le processus de séquençage du package.</p></td>
</tr>
<tr class="even">
<td align="left"><p>StreamMap.xml</p></td>
<td align="left"><p>Fichier XML</p></td>
<td align="left"><p>Liste des fichiers pour le bloc de fonctionnalités principal et de publication. Le bloc de fonctionnalités de publication contient les fichiers ICO et les parties de fichiers requises (EXE et DLL) pour la publication du package. S’il est présent, le bloc de fonctionnalités principal inclut les fichiers qui ont été optimisés pour la diffusion en continu pendant le processus de séquençage.</p></td>
</tr>
</tbody>
</table>

 

## <a name="app-v-client-data-storage-locations"></a><a href="" id="bkmk-files-data-storage"></a>Emplacements de stockage de données client App-V


Le client App-V effectue des tâches pour s’assurer que les applications virtuelles s’exécutent correctement et fonctionnent comme les applications installées localement. Le processus d’ouverture et d’exécution d’applications virtuelles nécessite un mappage à partir du système de fichiers virtuel et du Registre pour s’assurer que l’application dispose des composants requis d’une application traditionnelle attendus par les utilisateurs. Cette section décrit les ressources requises pour exécuter des applications virtuelles et répertorie l’emplacement où App-V stocke les biens.

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
<td align="left"><p>Emplacement par défaut pour les fichiers de package en lecture seule</p></td>
</tr>
<tr class="even">
<td align="left"><p>Catalogue d’ordinateurs</p></td>
<td align="left"><p>%ProgramData%\Microsoft\AppV\Client\Catalog</p></td>
<td align="left"><p>Contient des documents de configuration par ordinateur</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Catalogue d’utilisateurs</p></td>
<td align="left"><p>%AppData%\Microsoft\AppV\Client\Catalog</p></td>
<td align="left"><p>Contient des documents de configuration par utilisateur</p></td>
</tr>
<tr class="even">
<td align="left"><p>Sauvegardes de raccourcis</p></td>
<td align="left"><p>%AppData%\Microsoft\AppV\Client\Integration\ShortCutBackups</p></td>
<td align="left"><p>Stocke les points d’intégration précédents qui permettent la restauration lors de la désinscriture de package</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Itinérance copy on Write (CAS)</p></td>
<td align="left"><p>%AppData%\Microsoft\AppV\Client\VFS</p></td>
<td align="left"><p>Emplacement itinérant accessible en écriture pour la modification du package</p></td>
</tr>
<tr class="even">
<td align="left"><p>Copy on Write (AUT) Local</p></td>
<td align="left"><p>%LocalAppData%\Microsoft\AppV\Client\VFS</p></td>
<td align="left"><p>Emplacement non itinérant accessible en écriture pour la modification du package</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Registre de l’ordinateur</p></td>
<td align="left"><p>HKLM\Software\Microsoft\AppV</p></td>
<td align="left"><p>Contient des informations sur l’état du package, y compris VReg pour l’ordinateur ou les packages publiés globalement (ruche de l’ordinateur)</p></td>
</tr>
<tr class="even">
<td align="left"><p>Registre utilisateur</p></td>
<td align="left"><p>HKCU\Software\Microsoft\AppV</p></td>
<td align="left"><p>Contient des informations sur l’état du package utilisateur, y compris VReg</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Classes de Registre d’utilisateur</p></td>
<td align="left"><p>HKCU\Software\Classes\AppV</p></td>
<td align="left"><p>Contient des informations supplémentaires sur l’état du package utilisateur</p></td>
</tr>
</tbody>
</table>

 

Des détails supplémentaires pour le tableau sont fournis dans la section ci-dessous et dans tout le document.

### <a name="package-store"></a>Magasin de packages

Le client App-V gère les ressources d’applications montées dans le magasin de packages. Cet emplacement de stockage par défaut est, mais vous pouvez le configurer pendant ou après l’installation à l’aide de la commande PowerShell, qui modifie le Registre local (valeur sous `%ProgramData%\App-V` `Set-AppVClientConfiguration` la `PackageInstallationRoot` `HKLM\Software\Microsoft\AppV\Client\Streaming` clé). Le magasin de packages doit se trouver à un chemin d’accès local sur le système d’exploitation client. Les packages individuels sont stockés dans le magasin de packages dans des sous-dossiers nommés pour le GUID du package et le GUID de version.

Exemple de chemin d’accès à une application spécifique :

``` syntax
C:\ProgramData\App-V\PackGUID\VersionGUID
```

Pour modifier l’emplacement par défaut du magasin de packages lors de l’installation, voir [Comment déployer le client App-V](how-to-deploy-the-app-v-client-51gb18030.md).

### <a name="shared-content-store"></a>Magasin de contenu partagé

Si le client App-V est configuré en mode magasin de contenu partagé, aucune donnée n’est écrite sur le disque en cas de panne du flux, ce qui signifie que les packages nécessitent un espace disque local minimal (données de publication). L’utilisation de moins d’espace disque est vivement souhaitable dans les environnements VDI, où le stockage local peut être limité, et la diffusion en continu des applications à partir d’un emplacement réseau hautes performances (tel qu’un SAN) est préférable. Pour plus d’informations sur le mode de magasin de contenu partagé, voir <https://go.microsoft.com/fwlink/p/?LinkId=392750> .

**Remarque**  
L’ordinateur et le magasin de packages doivent se trouver sur un lecteur local, même lorsque vous utilisez des configurations de magasin de contenu partagé pour le client App-V.

 

### <a name="package-catalogs"></a>Catalogues de packages

Le client App-V gère les deux emplacements basés sur des fichiers suivants :

-   **Catalogues (utilisateur et ordinateur).**

-   **Emplacements du Registre** : dépend de la façon dont le package est ciblé pour la publication. Il existe un catalogue (magasin de données) pour l’ordinateur et un catalogue pour chaque utilisateur individuel. Le catalogue d’ordinateurs stocke les informations globales applicables à tous les utilisateurs ou à tous les utilisateurs, et le catalogue d’utilisateurs stocke les informations applicables à un utilisateur spécifique. Le catalogue est une collection de configurations dynamiques et de fichiers manifeste . il existe des données discrètes pour le fichier et le Registre par version de package. 

### <a name="machine-catalog"></a>Catalogue d’ordinateurs

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>Description</p></td>
<td align="left"><p>Stocke les documents de package disponibles pour les utilisateurs sur l’ordinateur, lorsque des packages sont ajoutés et publiés. Toutefois, si un package est « global » au moment de la publication, les intégrations sont disponibles pour tous les utilisateurs.</p>
<p>Si un package n’est pas global, les intégrations sont publiées uniquement pour des utilisateurs spécifiques, mais des ressources globales sont toujours modifiées et visibles par tout le monde sur l’ordinateur client (par exemple, le répertoire du package se trouve dans un emplacement disque partagé).</p>
<p>Si un package est disponible pour un utilisateur sur l’ordinateur (global ou non global), le manifeste est stocké dans le catalogue d’ordinateurs. Lorsqu’un package est publié globalement, il existe un fichier de configuration dynamique, stocké dans le catalogue d’ordinateurs ; par conséquent, la détermination de la globalisation d’un package est définie selon qu’il existe ou non un fichier de stratégie (fichier UserDeploymentConfiguration) dans le catalogue d’ordinateurs.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Emplacement de stockage par défaut</p></td>
<td align="left"><p><code>%programdata%\Microsoft\AppV\Client\Catalog&lt;/code&gt;</p>
<p>Cet emplacement n’est pas le même que l’emplacement du magasin de packages. Le magasin de packages est la copie de premier plan ou la copie de l’archive des fichiers de package.</p></td>
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
<td align="left"><p>Emplacement supplémentaire du catalogue d’ordinateurs, utilisé lorsque le package fait partie d’un groupe de connexions</p></td>
<td align="left"><p>L’emplacement suivant s’ajoute à l’emplacement de package spécifique mentionné ci-dessus :</p>
<p><code>%programdata%\Microsoft\AppV\Client\Catalog\PackageGroups\ConGroupGUID\ConGroupVerGUID</code></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Fichiers supplémentaires dans le catalogue d’ordinateurs lorsque le package fait partie d’un groupe de connexions</p></td>
<td align="left"><ul>
<li><p>PackageGroupDescriptor.xml</p></li>
<li><p>UserPackageGroupDescriptor.xml (groupe de connexions publié globalement)</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

### <a name="user-catalog"></a>Catalogue d’utilisateurs

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>Description</p></td>
<td align="left"><p>Créé au cours du processus de publication. Contient des informations utilisées pour la publication du package et également utilisées au lancement pour s’assurer qu’un package est mis en service pour un utilisateur spécifique. Créé dans un emplacement itinérant et inclut des informations de publication spécifiques à l’utilisateur.</p>
<p>Lorsqu’un package est publié pour un utilisateur, le fichier de stratégie est stocké dans le catalogue d’utilisateurs. En même temps, une copie du manifeste est également stockée dans le catalogue d’utilisateurs. Lorsqu’un droit de package est supprimé pour un utilisateur, les fichiers de package appropriés sont supprimés du catalogue d’utilisateurs. En regardant le catalogue d’utilisateurs, un administrateur peut afficher la présence d’un fichier de configuration dynamique, ce qui indique que le package est autorisé pour cet utilisateur.</p>
<p>Pour les utilisateurs itinérants, le catalogue d’utilisateurs doit se trouver dans un emplacement itinérant ou partagé pour conserver le comportement App-V hérité du ciblage des utilisateurs par défaut. Les droits et stratégies sont liés à un utilisateur, et non à un ordinateur, de sorte qu’ils doivent se déplacer avec l’utilisateur une fois qu’ils sont provisionés.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Emplacement de stockage par défaut</p></td>
<td align="left"><p><code>appdata\roaming\Microsoft\AppV\Client\Catalog\Packages\PkgGUID\VerGUID</code></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Fichiers dans le catalogue d’utilisateurs</p></td>
<td align="left"><ul>
<li><p>UserManifest.xml</p></li>
<li><p>DynamicConfiguration.xml ou UserDeploymentConfiguration.xml</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Emplacement de catalogue utilisateur supplémentaire, utilisé lorsque le package fait partie d’un groupe de connexions</p></td>
<td align="left"><p>L’emplacement suivant s’ajoute à l’emplacement de package spécifique mentionné ci-dessus :</p>
<p><code>appdata\roaming\Microsoft\AppV\Client\Catalog\PackageGroups\PkgGroupGUID\PkgGroupVerGUID</code></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Fichier supplémentaire dans le catalogue d’ordinateurs lorsque le package fait partie d’un groupe de connexions</p></td>
<td align="left"><p><code>UserPackageGroupDescriptor.xml</code></p></td>
</tr>
</tbody>
</table>

 

### <a name="shortcut-backups"></a>Sauvegardes de raccourcis

Pendant le processus de publication, le client App-V sauvegarde tous les raccourcis et points d’intégration vers cette sauvegarde permet de restaurer ces points d’intégration vers les versions précédentes lorsque le package n’est pas `%AppData%\Microsoft\AppV\Client\Integration\ShortCutBackups.` publié.

### <a name="copy-on-write-files"></a>Copier sur les fichiers d’écriture

Le magasin de packages contient une copie des fichiers de package qui ont été diffusés en continu à partir du serveur de publication. Pendant le fonctionnement normal d’une application App-V, l’utilisateur ou le service peut nécessiter des modifications aux fichiers. Ces modifications ne sont pas apportées dans le magasin de packages afin de préserver votre capacité à réparer l’application, ce qui supprime ces modifications. Ces emplacements, appelés COPY (Copy on Write), assurent la prise en charge des emplacements itinérants et non itinérants. L’emplacement où les modifications sont stockées dépend de l’endroit où l’application a été programmée pour écrire les modifications dans une expérience native.

### <a name="cow-roaming"></a>ROAMing DE LAS

L’emplacement d’itinérance ZIP décrit ci-dessus stocke les modifications apportées aux fichiers et répertoires ciblés vers l’emplacement %AppData% classique ou \\Users\\{username}\\AppData\\Roaming. Ces répertoires et fichiers sont ensuite itinérants en fonction des paramètres du système d’exploitation.

### <a name="cow-local"></a>JOURNAL local

L’emplacement LOCAL DUS est similaire à l’emplacement d’itinérance, mais les répertoires et les fichiers ne sont pas itinérants vers d’autres ordinateurs, même si la prise en charge de l’itinérance a été configurée. L’emplacement LOCAL DUT DÉCRIT ci-dessus stocke les modifications applicables aux fenêtres classiques et non à l’emplacement %AppData%. Les répertoires répertoriés varient, mais il y aura deux emplacements pour tous les emplacements Windows types (par exemple, Common AppData et Common AppDataS). Le **S** signifie l’emplacement restreint lorsque le service virtuel demande la modification en tant qu’utilisateur élevé différent des utilisateurs connectés. L’emplacement non**S stocke** les modifications basées sur l’utilisateur.

## <a name="package-registry"></a><a href="" id="bkmk-pkg-registry"></a>Registre de package


Pour qu’une application puisse accéder aux données de Registre du package, le client App-V doit mettre les données de Registre du package à la disposition des applications. Le client App-V utilise le Registre réel comme magasin de données de base pour toutes les données de Registre.

Lorsqu’un nouveau package est ajouté au client App-V, une copie du Registre. Le fichier DAT du package est créé sur `%ProgramData%\Microsoft\AppV\Client\VREG\{Version GUID}.dat` . Le nom du fichier est le GUID de version avec le . Extension DAT. La raison pour laquelle cette copie est réalisée est de s’assurer que le fichier de ruche réel dans le package n’est jamais utilisé, ce qui empêcherait la suppression du package ultérieurement.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Registry.dat à partir du magasin de packages</strong></p></td>
<td align="left"><p><strong> &gt; </strong></p></td>
<td align="left"><p><strong>%ProgramData%\Microsoft\AppV\Client\Vreg{VersionGuid}.dat</strong></p></td>
</tr>
</tbody>
</table>

 

Lorsque la première application du package est lancée sur le client, le client par étapes ou copie le contenu du fichier de ruche, en re-créant les données de Registre du package à un autre `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AppV\Client\Packages\PackageGuid\Versions\VersionGuid\REGISTRY` emplacement. Les données de Registre par étapes ont deux types distincts de données d’ordinateur et de données utilisateur. Les données de l’ordinateur sont partagées entre tous les utilisateurs de l’ordinateur. Les données utilisateur sont mises à niveau pour chaque utilisateur vers un emplacement spécifique de `HKCU\Software\Microsoft\AppV\Client\Packages\PackageGuid\Registry\User` l’utilisateur. Les données de l’ordinateur sont finalement supprimées au moment de la suppression du package, et les données utilisateur sont supprimées lors d’une opération de désabonnement de l’utilisateur.

### <a name="package-registry-staging-vs-connection-group-registry-staging"></a>Mise en transit du Registre de package par rapport à la zone de registre de groupe de connexion

Lorsque des groupes de connexions sont présents, le processus précédent de transit du Registre est vrai, mais au lieu d’avoir un fichier de ruche à traiter, il en existe plusieurs. Les fichiers sont traitées dans l’ordre dans lequel ils apparaissent dans le fichier XML du groupe de connexions, avec le premier rédacteur qui a gagné les conflits.

Le Registre par étapes est persistant de la même manière que dans le cas d’un package unique. Les données de Registre d’utilisateurs par étapes restent pour le groupe de connexions jusqu’à ce qu’elles soient désactivées . Les données de Registre de l’ordinateur par étapes sont supprimées lors de la suppression du groupe de connexions.

### <a name="virtual-registry"></a>Registre virtuel

L’objectif du Registre virtuel (VREG) est de fournir une vue fusionnée unique du Registre de package et du Registre natif aux applications. Il fournit également une fonctionnalité de copie sur écriture (CAS), c’est-à-dire que toutes les modifications apportées au Registre à partir du contexte d’un processus virtuel sont apportées à un emplacement UNIQUE distinct. Cela signifie que le VREG doit combiner jusqu’à trois emplacements de Registre distincts dans un affichage unique basé sur les emplacements remplis dans le registre CAS - &gt; package - &gt; natif. Lorsqu’une demande de données de Registre est faite, elle recherche dans l’ordre jusqu’à ce qu’elle trouve les données qu’elle demandait. Cela signifie que s’il existe une valeur stockée dans un emplacement DE LASO, elle ne se poursuit pas à d’autres emplacements, toutefois, s’il n’y a pas de données dans l’emplacement DUSO, elle se poursuit vers l’emplacement package, puis l’emplacement natif jusqu’à ce qu’elle trouve les données appropriées.

### <a name="registry-locations"></a>Emplacements du Registre

Il existe deux emplacements de Registre de package et deux emplacements de groupe de connexions où le client App-V stocke les informations de Registre, selon que le package est publié individuellement ou dans le cadre d’un groupe de connexions. Il existe trois emplacements DNS pour les packages et trois pour les groupes de connexions, qui sont créés et gérés par le VREG. Paramètres pour les packages et les groupes de connexion ne sont pas partagés :

**VReg de package unique :**

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
<td align="left"><p><strong>LASER</strong></p></td>
<td align="left"><ul>
<li><p>Registre ordinateur\Client\Packages\PkgGUID\REGISTRY (seul le processus d’élévation de niveau peut écrire)</p></li>
<li><p>Registre utilisateur\Client\Packages\PkgGUID\REGISTRY (tout ce qui est écrit sous HKCU en itinérance de l’utilisateur à l’exception de Software\Classes</p></li>
<li><p>Classes du Registre utilisateur\Client\Packages\PkgGUID\REGISTRY (HKCU\Software\Classes writes and HKLM for non elevated process)</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Package</strong></p></td>
<td align="left"><ul>
<li><p>Registre ordinateur\Client\Packages\PkgGUID\Versions\VerGuid\Registry\Machine</p></li>
<li><p>Classes du Registre utilisateur\Client\Packages\PkgGUID\Versions\VerGUID\Registry</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Natif</strong></p></td>
<td align="left"><ul>
<li><p>Emplacement du Registre de l’application native</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

 

**Groupe de connexion VReg :**

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
<td align="left"><p><strong>LASER</strong></p></td>
<td align="left"><ul>
<li><p>Registre ordinateur\Client\PackageGroups\GrpGUID\REGISTRY (seul le processus d’élévation de niveau peut écrire)</p></li>
<li><p>Registre utilisateur\Client\PackageGroups\GrpGUID\REGISTRY (tout ce qui est écrit dans HKCU à l’exception de Software\Classes</p></li>
<li><p>Classes du Registre utilisateur\Client\PackageGroups\GrpGUID\REGISTRY</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Package</strong></p></td>
<td align="left"><ul>
<li><p>Registre ordinateur\Client\PackageGroups\GrpGUID\Versions\VerGUID\REGISTRY</p></li>
<li><p>Classes du Registre utilisateur\Client\PackageGroups\GrpGUID\Versions\VerGUID\REGISTRY</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Natif</strong></p></td>
<td align="left"><ul>
<li><p>Emplacement du Registre de l’application native</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

 

Il existe deux emplacements VHD pour HKLM ; processus élevés et non élevés; Les processus élevés écrivent toujours les modifications HKLM dans la sécurité CAS sous HKLM. Les processus non élevés écrivent toujours les modifications HKLM dans la CLASSE NON sécurisée SOUS HKCU\\Software\\Classes. Lorsqu’une application lit les modifications de HKLM, les processus élevés lisent les modifications à partir de la sécurité CAS sous HKLM. Les lectures non élevées des deux, ce qui favorise d’abord les modifications apportées dans l’autre.

### <a name="pass-through-keys"></a>Touches pass-through

Les clés pass-through permettent à un administrateur de configurer certaines clés afin qu’elles ne soient lues qu’à partir du Registre natif, en contournant les emplacements PACKAGE et KEYS. Les emplacements pass-through sont globaux pour l’ordinateur (et non spécifiques au package) et peuvent être configurés en ajoutant le chemin d’accès à la clé, qui doit être traité comme un passage à la valeur **REG\_MULTI\_SZ** appelée **PassThroughPaths de** la `HKLM\Software\Microsoft\AppV\Subsystem\VirtualRegistry` clé. Toute clé qui apparaît sous cette valeur à chaînes multiples (et ses enfants) sera traitée comme un chiffre pass-through.

Les emplacements suivants sont configurés comme emplacements pass-through par défaut :

-   HKEY\_CURRENT\_USER\\SOFTWARE\\Classes\\Local Paramètres\\Software\\Microsoft\\Windows\\CurrentVersion\\AppModel

-   HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes\\Local Paramètres\\Software\\Microsoft\\Windows\\CurrentVersion\\AppModel

-   HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\WINEVT

-   HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\services\\eventlog\\Application

-   HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Control\\WMI\\Autologger

-   HKEY\_CURRENT\_USER\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\Internet Paramètres

-   HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Perflib

-   HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Policies

-   HKEY\_CURRENT\_USER\\SOFTWARE\\Policies

L’objectif des clés pass-through est de s’assurer qu’une application virtuelle n’écrit pas de données de Registre dans le VReg requis pour les applications non virtuelles pour une opération ou une intégration réussie. La clé Stratégies garantit que les paramètres basés sur la stratégie de groupe définies par l’administrateur sont utilisés et non par les paramètres de package. La clé AppModel est nécessaire pour l’intégration à Windows applications modernes basées sur l’interface utilisateur. Il est recommandé que les administrations ne modifient aucune des clés pass-through par défaut, mais dans certains cas, en fonction du comportement de l’application peut nécessiter l’ajout de clés pass-through supplémentaires.

## <a name="app-v-package-store-behavior"></a><a href="" id="bkmk-pkg-store-behavior"></a>Comportement du magasin de packages App-V


App-V 5 gère le magasin de packages, qui est l’emplacement où sont stockés les fichiers de ressources étendus du fichier appv. Par défaut, cet emplacement est stocké dans %ProgramData%\\App-V et est limité en termes de fonctionnalités de stockage uniquement par l’espace disque disponible. Le magasin de packages est organisé par les GUID pour le package et la version, comme mentionné dans la section précédente.

### <a name="add-packages"></a>Ajouter des packages

Les packages App-V sont mis en place lors de l’ajout à l’ordinateur avec le client App-V. Le client App-V fournit une offre intermédiaire à la demande. Lors de la publication ou d’une commande Add-AppVClientPackage manuelle, la structure de données est intégrée au magasin de packages (c:\\programdata\\App-V\\{PkgGUID}\\{VerGUID}). Les fichiers de package identifiés dans le bloc de publication défini dans le StreamMap.xml sont ajoutés au système et les dossiers de niveau supérieur et les fichiers enfants sont mis à niveau pour garantir que les ressources d’application adéquates existent au lancement.

### <a name="mounting-packages"></a>Montage de packages

Les packages peuvent être explicitement chargés à l’aide de PowerShell ou à l’aide de l’interface utilisateur du `Mount-AppVClientPackage` **client App-V** pour télécharger un package. Cette opération charge entièrement l’intégralité du package dans le magasin de packages.

### <a name="streaming-packages"></a>Packages de diffusion en continu

Le client App-V peut être configuré pour modifier le comportement par défaut de la diffusion en continu. Toutes les stratégies de diffusion en continu sont stockées sous la clé de Registre suivante `HKEY_LOCAL_MAcHINE\Software\Microsoft\AppV\Client\Streaming` : Les stratégies sont définies à l’aide de l’cmdlet `Set-AppvClientConfiguration` PowerShell. Les stratégies suivantes s’appliquent à la diffusion en continu :

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
<td align="left"><p>Sur Windows 8 et ultérieures, il permet la diffusion en continu sur 3G réseaux cellulaires et mobiles</p></td>
</tr>
<tr class="even">
<td align="left"><p>AutoLoad</p></td>
<td align="left"><p>Spécifie le paramètre de chargement en arrière-plan :</p>
<p><strong>0 </strong> - Désactivé</p>
<p><strong>1 </strong> – Packages précédemment utilisés uniquement</p>
<p><strong>2 </strong> – Tous les packages</p></td>
</tr>
<tr class="odd">
<td align="left"><p>PackageInstallationRoot</p></td>
<td align="left"><p>Dossier racine du magasin de packages sur l’ordinateur local</p></td>
</tr>
<tr class="even">
<td align="left"><p>PackageSourceRoot</p></td>
<td align="left"><p>Remplacement racine à partir de laquelle les packages doivent être diffusés</p></td>
</tr>
<tr class="odd">
<td align="left"><p>SharedContentStoreMode</p></td>
<td align="left"><p>Permet l’utilisation du magasin de contenu partagé pour les scénarios VDI</p></td>
</tr>
</tbody>
</table>

 

 

Ces paramètres affectent le comportement des ressources de package App-V de diffusion en continu pour le client. Par défaut, App-V télécharge uniquement les ressources requises après le téléchargement des blocs de fonctionnalités principales et de publication initiale. Trois comportements spécifiques des packages de diffusion en continu doivent être expliqués :

-   Diffusion en arrière-plan

-   Diffusion en continu optimisée

-   Défauts de flux

### <a name="background-streaming"></a>Diffusion en arrière-plan

L’cmdlet PowerShell peut être utilisée pour déterminer le mode actuel de diffusion en continu en arrière-plan avec le paramètre AutoLoad et modifiée avec l'Set-AppvClientConfiguration de cmdlet ou à partir du Registre `Get-AppvClientConfiguration` (HKLM\\SOFTWARE\\Microsoft\\AppV\\ClientStreaming key). La diffusion en continu en arrière-plan est un paramètre par défaut dans lequel le paramètre De chargement automatique est définie pour télécharger les packages précédemment utilisés. Le comportement basé sur le paramètre par défaut (valeur=1) télécharge les blocs de données App-V en arrière-plan après le lancement de l’application. Ce paramètre peut être désactivé (valeur=0) ou activé pour tous les packages (valeur=2), qu’ils soient lancés ou non.

### <a name="optimized-streaming"></a>Diffusion en continu optimisée

Les packages App-V peuvent être configurés avec un bloc de fonctionnalités principal lors du séquençage. Ce paramètre permet à l’ingénieur de séquencement de surveiller les fichiers de lancement pour une ou plusieurs applications spécifiques, et de marquer les blocs de données du package App-V pour la diffusion en continu au premier lancement d’une application du package.

### <a name="stream-faults"></a>Défauts de flux

Après le flux initial des données de publication et le bloc de fonctionnalités principal, les demandes de fichiers supplémentaires effectuent des erreurs de flux. Ces blocs de données sont téléchargés dans le magasin de packages selon les besoins. Cela permet à un utilisateur de télécharger uniquement une petite partie du package, généralement suffisamment pour lancer le package et exécuter des tâches normales. Tous les autres blocs sont téléchargés lorsqu’un utilisateur lance une opération qui nécessite des données qui ne se trouve pas actuellement dans le magasin de packages.

Pour plus d’informations sur la visite de diffusion en continu du package App-V <https://go.microsoft.com/fwlink/?LinkId=392770> :

Le séquençage pour l’optimisation de la diffusion en continu est disponible sur : <https://go.microsoft.com/fwlink/?LinkId=392771> .

### <a name="package-upgrades"></a>Mises à niveau de package

Les packages App-V nécessitent une mise à jour tout au long du cycle de vie de l’application. Les mises à niveau de package App-V sont similaires à l’opération de publication du package, car chaque version sera créée dans son propre emplacement PackageRoot : `%ProgramData%\App-V\{PkgGUID}\{newVerGUID}` . L’opération de mise à niveau est optimisée en créant des liens durs vers des fichiers identiques et diffusés en continu à partir d’autres versions du même package.

### <a name="package-removal"></a>Suppression de package

Le comportement du client App-V lorsque des packages sont supprimés dépend de la méthode utilisée pour la suppression. À l’aide d’une infrastructure complète App-V pour dépublier l’application, les fichiers catalogue d’utilisateurs (catalogue d’ordinateurs pour les applications publiées globalement) sont supprimés, mais conservent l’emplacement du magasin de packages et les emplacements ZIP. Lorsque l’cmdlet PowerShell est utilisée pour supprimer un package App-V, l’emplacement du magasin de `Remove-AppVClientPackge` packages est nettoyé. N’oubliez pas que la suppression d’un package App-V à partir du serveur d’administration n’effectue pas d’opération suppression. Aucune des opérations ne supprime les fichiers de package du Package Store.

## <a name="roaming-registry-and-data"></a><a href="" id="bkmk-roaming-reg-data"></a>Registre et données itinérants


App-V 5 est en mesure de fournir une expérience quasi native lors de l’itinérance, en fonction de la façon dont l’application utilisée est écrite. Par défaut, App-V roams AppData qui est stocké dans l’emplacement d’itinérance, en fonction de la configuration d’itinérance du système d’exploitation. Les autres emplacements de stockage des données basées sur des fichiers ne sont pas itinérants d’un ordinateur à l’autre, car ils sont situés dans des emplacements qui ne sont pas itinérants.

### <a name="roaming-requirements-and-user-catalog-data-storage"></a><a href="" id="bkmk-clt-inter-roam-reqs"></a>Exigences d’itinérance et stockage des données du catalogue d’utilisateurs

App-V stocke les données, qui représentent l’état du catalogue de l’utilisateur, sous la forme :

-   Fichiers sous %appdata%\\Microsoft\\AppV\\Client\\Catalog

-   Paramètres du Registre sous `HKEY_CURRENT_USER\Software\Microsoft\AppV\Client\Packages`

Ensemble, ces fichiers et paramètres de Registre représentent le catalogue de l’utilisateur. Les deux doivent donc être itinérants ou non pour un utilisateur donné. App-V ne prend pas en charge l’itinérance %AppData%, mais pas l’itinérance du profil de l’utilisateur (Registre), et inversement.

**Remarque**  
L’cmdlet **Repair-AppvClientPackage** ne répare pas l’état de publication des packages, où l’état App-V de l’utilisateur est manquant ou inséparable avec les données dans `HKEY_CURRENT_USER` %appdata%.

 

### <a name="registry-based-data"></a>Données basées sur le Registre

L’itinérance du Registre App-V se situe dans deux scénarios, comme indiqué dans le tableau suivant.

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
<td align="left"><p>Applications qui sont exécutés en tant qu’utilisateurs standard</p></td>
<td align="left"><p>Lorsqu’un utilisateur standard lance une application App-V, HKLM et HKCU pour les applications App-V sont stockés dans la ruche HKCU sur l’ordinateur. Cela présente deux chemins d’accès distincts :</p>
<ul>
<li><p>HKLM : HKCU\SOFTWARE\Classes\AppV\Client\Packages{PkgGUID}\REGISTRY\MACHINE\SOFTWARE</p></li>
<li><p>HKCU : HKCU\SOFTWARE\Microsoft\AppV\Client\Packages{PkgGUID}\REGISTRY\USER{UserSID}\SOFTWARE</p></li>
</ul>
<p>Les emplacements sont activés pour l’itinérance en fonction des paramètres du système d’exploitation.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Applications qui sont exécutés avec élévation</p></td>
<td align="left"><p>Lorsqu’une application est lancée avec élévation :</p>
<ul>
<li><p>Les données HKLM sont stockées dans la ruche HKLM sur l’ordinateur local</p></li>
<li><p>Les données HKCU sont stockées à l’emplacement du Registre de l’utilisateur</p></li>
</ul>
<p>Dans ce scénario, ces paramètres ne sont pas itinérants avec les configurations d’itinérance normales du système d’exploitation, et les clés de Registre et les valeurs qui en résultent sont stockées à l’emplacement suivant :</p>
<ul>
<li><p>HKLM\SOFTWARE\Microsoft\AppV\Client\Packages{PkgGUID}{UserSID}\REGISTRY\MACHINE\SOFTWARE</p></li>
<li><p>HKCU\SOFTWARE\Microsoft\AppV\Client\Packages{PkgGUID}\Registry\User{UserSID}\SOFTWARE</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

### <a name="app-v-and-folder-redirection"></a>Redirection d’App-V et de dossiers

App-V 5.1 prend en charge la redirection de dossiers du dossier AppData itinérant (%AppData%). Lorsque l’environnement virtuel est démarré, l’état AppData itinérant à partir du répertoire AppData itinérant de l’utilisateur est copié dans le cache local. À l’inverse, lorsque l’environnement virtuel est arrêté, le cache local associé à appData itinérante d’un utilisateur spécifique est transféré vers l’emplacement réel du répertoire AppData itinérant de cet utilisateur.

Un package classique possède plusieurs emplacements mappés dans le magasin de backing de l’utilisateur pour les paramètres dans AppData\\Local et AppData\\Roaming. Ces emplacements sont les emplacements Copier sur écriture qui sont stockés par utilisateur dans le profil de l’utilisateur et qui sont utilisés pour stocker les modifications apportées aux répertoires VFS du package et pour protéger le package par défaut VFS.

Le tableau suivant indique les emplacements locaux et itinérants, lorsque la redirection de dossiers n’a pas été implémentée.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Répertoire VFS dans le package</th>
<th align="left">Emplacement mappé du magasin de backing</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>ProgramFilesX86</p></td>
<td align="left"><p>C:\users\jsmith\AppData &lt; strong &gt; Local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \ProgramFilesX86</p></td>
</tr>
<tr class="even">
<td align="left"><p>SystemX86</p></td>
<td align="left"><p>C:\users\jsmith\AppData &lt; strong &gt; Local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \SystemX86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows</p></td>
<td align="left"><p>C:\users\jsmith\AppData &lt; strong &gt; Local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \Windows</p></td>
</tr>
<tr class="even">
<td align="left"><p>appv_ROOT</p></td>
<td align="left"><p>C:\users\jsmith\AppData &lt; strong &gt; Local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \appv_ROOT</p></td>
</tr>
<tr class="odd">
<td align="left"><p>AppData</p></td>
<td align="left"><p>C:\users\jsmith\AppData &lt; strong &gt; Roaming </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \AppData</p></td>
</tr>
</tbody>
</table>

 

 

Le tableau suivant indique les emplacements locaux et itinérants, lorsque la redirection de dossiers a été implémentée pour %AppData%, et que l’emplacement a été redirigé (généralement vers un emplacement réseau).

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Répertoire VFS dans le package</th>
<th align="left">Emplacement mappé du magasin de backing</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>ProgramFilesX86</p></td>
<td align="left"><p>C:\users\jsmith\AppData &lt; strong &gt; Local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \ProgramFilesX86</p></td>
</tr>
<tr class="even">
<td align="left"><p>SystemX86</p></td>
<td align="left"><p>C:\users\jsmith\AppData &lt; strong &gt; Local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \SystemX86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows</p></td>
<td align="left"><p>C:\users\jsmith\AppData &lt; strong &gt; Local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \Windows</p></td>
</tr>
<tr class="even">
<td align="left"><p>appv_ROOT</p></td>
<td align="left"><p>C:\users\jsmith\AppData &lt; strong &gt; Local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \appv_ROOT</p></td>
</tr>
<tr class="odd">
<td align="left"><p>AppData</p></td>
<td align="left"><p><strong>\Fileserver </strong> \users\jsmith\roaming\Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \AppData</p></td>
</tr>
</tbody>
</table>

 

 

Le pilote VFS client App-V actuel ne peut pas écrire dans les emplacements réseau. Le client App-V détecte donc la présence de redirection de dossiers et copie les données sur le lecteur local lors de la publication et au démarrage de l’environnement virtuel. Une fois que l’utilisateur ferme l’application App-V et que le client App-V ferme l’environnement virtuel, le stockage local de l’appData VFS est copié sur le réseau, ce qui permet l’itinérance vers d’autres ordinateurs, où le processus sera répété. Les étapes détaillées des processus sont les suivantes :

1.  Lors du démarrage de la publication ou de l’environnement virtuel, le client App-V détecte l’emplacement du répertoire AppData.

2.  Si le chemin d’accès AppData itinérant est local ou ino AppData\\L’emplacement d’itinérance est mappé, rien ne se produit.

3.  Si le chemin d’accès AppData itinérant n’est pas local, le répertoire VFS AppData est mappé au répertoire AppData local.

Ce processus résout le problème d’un %AppData% non local qui n’est pas pris en charge par le pilote VFS du client App-V. Toutefois, les données stockées dans ce nouvel emplacement ne sont pas itinérantes avec la redirection de dossier. Toutes les modifications apportées au cours de l’exécution de l’application se produisent à l’emplacement AppData local et doivent être copiées vers l’emplacement redirigé. Les étapes détaillées de ce processus sont les suivantes :

1.  L’application App-V est fermée, ce qui arrête l’environnement virtuel.

2.  Le cache local de l’emplacement AppData itinérant est compressé et stocké dans un fichier ZIP.

3.  Un timestamp à la fin du processus d’empaquetage ZIP est utilisé pour nommer le fichier.

4.  L’homp est enregistré dans le Registre : HKEY\_CURRENT\_USER\\Software\\Microsoft\\AppV\\Client\\Packages\\ GUID \\AppDataTime en tant que dernier &lt; &gt; timestamp AppData connu.

5.  Le processus de redirection de dossier est appelé pour évaluer et lancer le fichier ZIP chargé dans le répertoire AppData itinérant.

L’timestamp est utilisé pour déterminer un scénario « Dernier rédacteur l’emporte » s’il existe un conflit et est utilisé pour optimiser le téléchargement des données lors de la publication de l’application App-V ou du début de l’environnement virtuel. La redirection de dossiers rend les données disponibles à partir de tous les autres clients couverts par la stratégie de prise en charge et lance le processus de stockage des données AppData\\Roaming vers l’emplacement AppData local sur le client. Les processus détaillés sont les :

1.  L’utilisateur démarre l’environnement virtuel en démarreant une application.

2.  L’environnement virtuel de l’application recherche le fichier ZIP horodaté le plus récent, s’il est présent.

3.  Le registre est vérifié pour le dernier timestamp téléchargé connu, s’il est présent.

4.  Le fichier ZIP le plus récent est téléchargé, sauf si le dernier timestamp de chargement connu local est supérieur ou égal à l’timestamp du fichier ZIP.

5.  Si le dernier timestamp de chargement connu local est antérieure à celui du fichier ZIP le plus récent dans l’emplacement AppData itinérant, le fichier ZIP est extrait dans le répertoire temp local du profil de l’utilisateur.

6.  Une fois le fichier ZIP extrait, le cache local du répertoire AppData itinérant est renommé et les nouvelles données sont déplacées sur place.

7.  Le répertoire renommé est supprimé et l’application s’ouvre avec les données AppData itinérantes les plus récemment enregistrées.

Cette opération termine l’itinérance réussie des paramètres d’application présents dans les emplacements AppData\\Roaming. La seule autre condition qui doit être traitée est une opération de réparation de package. Les détails du processus sont les ci-après :

1.  Pendant la réparation, détectez si le chemin d’accès au répertoire AppData itinérant de l’utilisateur n’est pas local.

2.  Map to the non-local roaming AppData path targets are recreated the expected roaming and local AppData locations.

3.  Supprimez l’timestamp stocké dans le Registre, s’il est présent.

Ce processus permet de créer à la fois les emplacements locaux et réseau pour AppData et de supprimer l’enregistrement de Registre de l’timestamp.

## <a name="app-v-client-application-lifecycle-management"></a><a href="" id="bkmk-clt-app-lifecycle"></a>Gestion du cycle de vie des applications clientes App-V


Dans une infrastructure complète App-V, une fois les applications séquencés, elles sont gérées et publiées sur des utilisateurs ou des ordinateurs via les serveurs de gestion et de publication d’App-V. Cette section détaille les opérations qui se produisent pendant les opérations courantes de cycle de vie des applications App-V (Ajouter, publier, lancer, mettre à niveau et supprimer), ainsi que les emplacements de fichier et de Registre qui sont modifiés et modifiés du point de vue du client App-V. Les opérations du client App-V sont effectuées sous la forme d’une série de commandes PowerShell lancées sur l’ordinateur exécutant le client App-V.

Ce document se concentre sur les solutions d’infrastructure complète App-V. Pour plus d’informations sur l’intégration d’App-V avec Configuration Manager 2012, visitez <https://go.microsoft.com/fwlink/?LinkId=392773> :

Les tâches de cycle de vie de l’application App-V sont déclenchées lors de la connexion de l’utilisateur (par défaut), du démarrage de l’ordinateur ou en tant qu’opérations de temps en arrière-plan. Les paramètres des opérations du client App-V, notamment les serveurs de publication, les intervalles d’actualisation, l’enablement de script de package, etc., sont configurés lors de l’installation du client ou après l’installation avec des commandes PowerShell. Consultez la section Comment déployer le client sur TechNet à l’article : Comment déployer le [client App-V](how-to-deploy-the-app-v-client-51gb18030.md) ou utiliser PowerShell :

```powershell
get-command *appv*
```

### <a name="publishing-refresh"></a>Actualisation de la publication

Le processus d’actualisation de publication se compose de plusieurs opérations de plus petite taille effectuées sur le client App-V. Étant donné qu’App-V est une technologie de virtualisation d’application et non une technologie de planification des tâches, le Programmeur de tâches Windows est utilisé pour activer le processus lors de l’inscription de l’utilisateur, du démarrage de l’ordinateur et à intervalles réguliers. La configuration du client lors de l’installation répertoriée ci-dessus est la méthode préférée lors de la distribution du client à un grand groupe d’ordinateurs avec les paramètres corrects. Ces paramètres clients peuvent être configurés avec les cmdlets PowerShell suivantes :

-   **Add-AppVPublishingServer :** Configure le client avec un serveur de publication App-V qui fournit des packages App-V.

-   **Set-AppVPublishingServer :** Modifie les paramètres actuels du serveur de publication App-V.

-   **Set-AppVClientConfiguration :** Modifie les paramètres actuels du client App-V.

-   **Sync-AppVPublishingServer :** Lance manuellement un processus d’actualisation de publication d’App-V. Il est également utilisé dans les tâches programmées créées lors de la configuration du serveur de publication.

L’objectif des sections suivantes est de détailler les opérations qui se produisent au cours de différentes phases d’une actualisation de publication d’App-V. Les rubriques sont les suivantes :

-   Ajout d’un package App-V

-   Publication d’un package App-V

### <a name="adding-an-app-v-package"></a>Ajout d’un package App-V

L’ajout d’un package App-V au client est la première étape du processus d’actualisation de publication. Le résultat final est le même que la cmdlet dans PowerShell, sauf que pendant le processus d’ajout d’actualisation de publication, le serveur de publication configuré est contacté et transmet une liste d’applications de haut niveau au client pour récupérer des informations plus détaillées et pas une seule opération d’ajout de `Add-AppVClientPackage` package. Le processus se poursuit en configurant le client pour les ajouts de packages ou de groupes de connexions ou les mises à jour, puis accède au fichier appv. Ensuite, le contenu du fichier appv est développé et placé sur le système d’exploitation local aux emplacements appropriés. Voici un flux de travail détaillé du processus, en supposant que le package est configuré pour la diffusion en continu des pannes.

**Comment ajouter un package App-V**

1.  Lancement manuel via PowerShell ou l’initiation de la séquence de tâches du processus d’actualisation de la publication.

    1.  Le client App-V effectue une connexion HTTP et demande une liste d’applications en fonction de la cible. Le processus d’actualisation de publication prend en charge le ciblage d’ordinateurs ou d’utilisateurs.

    2.  Le serveur de publication App-V utilise l’identité de la cible, de l’utilisateur ou de l’ordinateur à l’origine et interroge la base de données pour obtenir la liste des applications autorisées. La liste des applications est fournie en tant que réponse XML, que le client utilise pour envoyer des demandes supplémentaires au serveur pour plus d’informations par package.

2.  L’agent de publication sur le client App-V effectue toutes les actions ci-dessous sérialisées.

    Évaluez les groupes de connexion non publiés ou désactivés, car les mises à jour de version du package qui font partie du groupe de connexions ne peuvent pas être traitées.

3.  Configurez les packages en identifiant une opération d’ajout ou de mise à jour.

    1.  Le client App-V utilise l’API AppX à partir Windows et accède au fichier appv à partir du serveur de publication.

    2.  Le fichier de package est ouvert et les AppXManifest.xml et StreamMap.xml sont téléchargés vers le magasin de packages.

    3.  Données de bloc de publication de flux entièrement définies dans le StreamMap.xml. Stocke les données de bloc de publication dans le magasin de packages\\PkgGUID\\VerGUID\\Root.

        -   Icônes : cibles de points d’extension.

        -   En-têtes PE (Portable Executable Headers) : cibles de points d’extension qui contiennent les informations de base sur les besoins de l’image sur le disque, accessibles directement ou via des types de fichiers.

        -   Scripts : téléchargez le répertoire de scripts à utiliser tout au long du processus de publication.

    4.  Remplir le magasin de packages :

        1.  Créez des fichiers rares sur le disque qui représentent le package extrait pour tous les répertoires répertoriés.

        2.  Stage top level files and directories under root.

        3.  Tous les autres fichiers sont créés lorsque le répertoire est répertorié comme peu sollicité sur le disque et diffusé à la demande.

    5.  Créez les entrées du catalogue d’ordinateurs. Créez les Manifest.xml et DeploymentConfiguration.xml à partir des fichiers de package (si aucun fichier DeploymentConfiguration.xml dans le package un espace réservé n’est créé).

    6.  Créez l’emplacement du magasin de packages dans le Registre HKLM\\Software\\Microsoft\\AppV\\Client\\Packages\\PkgGUID\\Versions\\VerGUID\\Catalog

    7.  Créez le fichier Registry.dat à partir du magasin de packages dans %ProgramData%\\Microsoft\\AppV\\Client\\VReg\\{VersionGUID}.dat

    8.  Enregistrez le package avec le pilote du mode noyau App-V HKLM\\Microsoft\\Software\\AppV\\MAV

    9.  Appeler des scripts à partir du fichier AppxManifest.xml ou DeploymentConfig.xml pour le minutage d’ajout de package.

4.  Configurez les groupes de connexions en ajoutant et en activant ou désactivant.

5.  Supprimez les objets qui ne sont pas publiés sur la cible (utilisateur ou ordinateur).

    **Remarque**  
    Cela n’effectue pas de suppression de package, mais supprime les points d’intégration pour la cible spécifique (utilisateur ou ordinateur) et supprime les fichiers catalogue d’utilisateurs (fichiers catalogue d’ordinateurs pour la publication globale).

     

6.  Appeler le montage de charge en arrière-plan en fonction de la configuration du client.

7.  Les packages qui ont déjà des informations de publication pour l’ordinateur ou l’utilisateur sont immédiatement restaurés.

    **Remarque**  
    Cette condition se produit en tant que produit de la suppression sans la suppression de laublishing avec ajout en arrière-plan du package.

     

Cette opération termine l’ajout d’un package App-V au processus d’actualisation de publication. L’étape suivante consiste à publier le package sur la cible spécifique (ordinateur ou utilisateur).

![package ajoutez des données de fichier et de Registre.](images/packageaddfileandregistrydata.png)

### <a name="publishing-an-app-v-package"></a>Publication d’un package App-V

Pendant l’opération d’actualisation de la publication, l’opération de publication spécifique (Publish-AppVClientPackage) ajoute des entrées au catalogue d’utilisateurs, maie les droits à l’utilisateur, identifie le magasin local et se termine en effectuant les étapes d’intégration. Voici les étapes détaillées.

**Comment publier et package App-V**

1.  Les entrées de package sont ajoutées au catalogue d’utilisateurs

    1.  Packages ciblés par l’utilisateur : les UserDeploymentConfiguration.xml et UserManifest.xml sont placés sur l’ordinateur dans le catalogue d’utilisateurs

    2.  Packages (globaux) de l’ordinateur : le UserDeploymentConfiguration.xml est placé dans le catalogue d’ordinateurs

2.  Enregistrez le package avec le pilote en mode noyau pour l’utilisateur sur HKLM\\Software\\Microsoft\\AppV\\MAV

3.  Effectuer des tâches d’intégration.

    1.  Créez des points d’extension.

    2.  Stockez les informations de sauvegarde dans le Registre et le profil itinérant de l’utilisateur (sauvegardes de raccourcis).

        **Remarque**  
        Cela permet de restaurer des points d’extension si le package n’est pas publié.

         

    3.  Exécutez des scripts ciblés pour le minutage de publication.

La publication d’un package App-V faisant partie d’un groupe de connexions est très similaire au processus ci-dessus. Pour les groupes de connexions, le chemin d’accès qui stocke les informations de catalogue spécifiques inclut PackageGroups en tant qu’enfant de l’annuaire de catalogues. Pour plus d’informations, examinez les informations du catalogue de l’ordinateur et des utilisateurs ci-dessus.

![package ajouter un fichier et des données de Registre - global.](images/packageaddfileandregistrydata-global.png)

### <a name="application-launch"></a>Lancement de l’application

Après le processus d’actualisation de la publication, l’utilisateur lance, puis relance une application App-V. Le processus est très simple et optimisé pour être lancé rapidement avec un minimum de trafic réseau. Le client App-V vérifie le chemin d’accès au catalogue d’utilisateurs pour les fichiers créés lors de la publication. Une fois les droits de lancement du package établis, le client App-V crée un environnement virtuel, commence la diffusion en continu des données nécessaires et applique les fichiers de configuration de déploiement et de manifeste appropriés lors de la création de l’environnement virtuel. Une fois l’environnement virtuel créé et configuré pour le package et l’application spécifiques, l’application démarre.

**Comment lancer des applications App-V**

1.  L’utilisateur lance l’application en cliquant sur un raccourci ou un appel de type de fichier.

2.  Le client App-V vérifie l’existence des fichiers suivants dans le catalogue d’utilisateurs

    -   UserDeploymentConfiguration.xml

    -   UserManifest.xml

3.  Si les fichiers sont présents, l’application est autorisée pour cet utilisateur spécifique et l’application démarre le processus de lancement. Il n’y a pas de trafic réseau à ce stade.

4.  Ensuite, le client App-V vérifie que le chemin d’accès du package enregistré pour le service client App-V se trouve dans le Registre.

5.  Lorsque vous recherchez le chemin d’accès au magasin de packages, l’environnement virtuel est créé. S’il s’agit du premier lancement, le bloc de fonctionnalités principal est téléchargé s’il est présent.

6.  Après le téléchargement, le service client App-V utilise les fichiers de configuration de manifeste et de déploiement pour configurer l’environnement virtuel et tous les sous-systèmes App-V sont chargés.

7.  L’application démarre. Pour les fichiers manquants dans le magasin de packages (fichiers peu nombreux), App-V diffuse les fichiers en panne selon les besoins.

    ![package add file and registry data - stream.](images/packageaddfileandregistrydata-stream.png)

### <a name="upgrading-an-app-v-package"></a>Mise à niveau d’un package App-V

Le processus de mise à niveau du package App-V 5 diffère des versions antérieures d’App-V. App-V prend en charge plusieurs versions du même package sur un ordinateur autorisé à différents utilisateurs. Les versions de package peuvent être ajoutées à tout moment lorsque le magasin de packages et les catalogues sont mis à jour avec les nouvelles ressources. Le seul processus spécifique à l’ajout de nouvelles ressources de version est l’optimisation du stockage. Pendant une mise à niveau, seuls les nouveaux fichiers sont ajoutés au nouvel emplacement du magasin de versions et des liens durs sont créés pour les fichiers inchangés. Cela réduit le stockage global en présentant le fichier sur un seul emplacement de disque, puis en le projetant dans tous les dossiers avec une entrée d’emplacement de fichier sur le disque. Les détails spécifiques de la mise à niveau d’un package App-V sont les suivants :

**Comment mettre à niveau un package App-V**

1.  Le client App-V effectue une actualisation de publication et découvre une version plus récente d’un package App-V.

2.  Les entrées de package sont ajoutées au catalogue approprié pour la nouvelle version

    1.  Packages ciblés par l’utilisateur : les UserDeploymentConfiguration.xml et UserManifest.xml sont placés sur l’ordinateur dans le catalogue d’utilisateurs à l’adresse appdata\\roaming\\Microsoft\\AppV\\Client\\Catalog\\Packages\\PkgGUID\\VerGUID

    2.  Packages (globaux) ciblés sur l’ordinateur : le UserDeploymentConfiguration.xml est placé dans le catalogue d’ordinateurs à l’adresse %programdata%\\Microsoft\\AppV\\Client\\Catalog\\Packages\\PkgGUID\\VerGUID

3.  Enregistrez le package avec le pilote en mode noyau pour l’utilisateur sur HKLM\\Software\\Microsoft\\AppV\\MAV

4.  Effectuer des tâches d’intégration.

    -   Intégrer des points d’extension (EP) à partir des fichiers manifeste et de configuration dynamique.

    1.  Les données EP basées sur des fichiers sont stockées dans le dossier AppData à l’aide des points de jonction à partir du magasin de packages.

    2.  Les EPS de version 1 existent déjà lorsqu’une nouvelle version devient disponible.

    3.  Les points d’extension sont basculés vers l’emplacement version 2 dans les catalogues d’ordinateurs ou d’utilisateurs pour les points d’extension plus nouveaux ou mis à jour.

5.  Exécutez des scripts ciblés pour le minutage de publication.

6.  Installez les assemblys côte à côte selon les besoins.

### <a name="upgrading-an-in-use-app-v-package"></a>Mise à niveau d’un package App-V en cours d’utilisation

**À partir d’App-V 5 SP2 :** si vous essayez de mettre à niveau un package utilisé par un utilisateur final, la tâche de mise à niveau est placée dans un état en attente. La mise à niveau s’exécutera ultérieurement, conformément aux règles suivantes :

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
<td align="left"><p>Tâche basée sur l’utilisateur, par exemple, publication d’un package pour un utilisateur</p></td>
<td align="left"><p>La tâche en attente est effectuée une fois que l’utilisateur se déconnecte, puis se connecte à nouveau.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Tâche globale, par exemple, activation globale d’un groupe de connexions</p></td>
<td align="left"><p>La tâche en attente est effectuée lorsque l’ordinateur est arrêté, puis redémarré.</p></td>
</tr>
</tbody>
</table>

 

Lorsqu’une tâche est placée dans un état en attente, le client App-V génère également une clé de Registre pour la tâche en attente, comme suit :

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tâche basée sur l’utilisateur ou globale</th>
<th align="left">Où la clé de Registre est générée</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Tâches basées sur l’utilisateur</p></td>
<td align="left"><p>KEY_CURRENT_USER\Software\Microsoft\AppV\Client\PendingTasks</p></td>
</tr>
<tr class="even">
<td align="left"><p>Tâches globales</p></td>
<td align="left"><p>HKEY_LOCAL_MACHINE\Software\Microsoft\AppV\Client\PendingTasks</p></td>
</tr>
</tbody>
</table>

 

Les opérations suivantes doivent être effectuées pour que les utilisateurs peuvent utiliser la version la plus récente du package :

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
<td align="left"><p>Cette tâche est spécifique à l’ordinateur et vous pouvez l’effectuer à tout moment en complétant les étapes de la section Ajouter un package ci-dessus.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Publier le package</p></td>
<td align="left"><p>Consultez la section Publication de package ci-dessus pour obtenir la procédure à suivre. Ce processus nécessite la mise à jour des points d’extension sur le système. Les utilisateurs finaux ne peuvent pas utiliser l’application lorsque vous terminez cette tâche.</p></td>
</tr>
</tbody>
</table>

 

Utilisez les exemples de scénarios suivants comme guide pour la mise à jour des packages.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Scénario</th>
<th align="left">Conditions préalables</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Le package App-V n’est pas utilisé lorsque vous essayez de mettre à niveau</p></td>
<td align="left"><p>Aucun des composants suivants du package ne peut être utilisé : application virtuelle, serveur COM ou extensions de shell.</p>
<p>L’administrateur publie une version plus récente du package et la mise à niveau fonctionne lors du prochain lancement d’un composant ou d’une application à l’intérieur du package. La nouvelle version du package est diffusée en continu et s’exécute. Rien n’a changé dans ce scénario dans App-V 5 SP2 par rapport aux versions précédentes d’App-V 5.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Le package App-V est en cours d’utilisation lorsque l’administrateur publie une version plus récente du package.</p></td>
<td align="left"><p>L’opération de mise à niveau est définie sur En attente par le client App-V, ce qui signifie qu’elle est mise en file d’attente et exécutée ultérieurement lorsque le package n’est pas en cours d’utilisation.</p>
<p>Si l’application de package est en cours d’utilisation, l’utilisateur arrête l’application virtuelle, après quoi la mise à niveau peut se produire.</p>
<p>Si le package possède des extensions shell (Office 2013), qui sont chargées définitivement par Windows Explorer, l’utilisateur ne peut pas être connecté. Les utilisateurs doivent se déconnecter et se connecter à nouveau pour lancer la mise à niveau du package App-V.</p></td>
</tr>
</tbody>
</table>

 

### <a name="global-vs-user-publishing"></a>Publication globale et utilisateur

Les packages App-V peuvent être publiés de deux manières : Utilisateur qui autorise un package App-V à un utilisateur ou à un groupe d’utilisateurs spécifique et Global qui autorise le package App-V à l’ordinateur entier pour tous les utilisateurs de l’ordinateur. Une fois qu’une mise à niveau de package a été mise en place et que le package App-V n’est pas en cours d’utilisation, envisagez les deux types de publication :

-   **Publié globalement :** l’application est publiée sur un ordinateur ; Tous les utilisateurs de cet ordinateur peuvent l’utiliser. La mise à niveau se produit au démarrage du service client App-V, ce qui signifie effectivement un redémarrage de l’ordinateur.

-   **Utilisateur publié**: l’application est publiée pour un utilisateur. S’il y a plusieurs utilisateurs sur l’ordinateur, l’application peut être publiée sur un sous-ensemble des utilisateurs. La mise à niveau se produit lorsque l’utilisateur se connecte ou lorsqu’il est publié à nouveau (régulièrement, actualisation et évaluation de la stratégie ConfigMgr, ou publication/actualisation périodique d’App-V, ou explicitement via les commandes PowerShell).

### <a name="removing-an-app-v-package"></a>Suppression d’un package App-V

La suppression d’applications App-V dans une infrastructure complète est une opération d’unpublish et n’effectue pas de suppression de package. Le processus est identique au processus de publication ci-dessus, mais au lieu d’ajouter le processus de suppression, les modifications apportées aux packages App-V sont annulées.

### <a name="repairing-an-app-v-package"></a>Réparation d’un package App-V

L’opération de réparation est très simple, mais peut affecter de nombreux emplacements sur l’ordinateur. Les emplacements COPY (Copy on Write) mentionnés précédemment sont supprimés, et les points d’extension sont dés-intégrés, puis ré-intégrés. Consultez les emplacements de placement des données DE LASO en vous rapportant à l’emplacement où ils sont enregistrés dans le Registre. Cette opération est effectuée automatiquement et il n’existe aucun contrôle administratif autre que le fait de lancer une opération de réparation à partir de la console cliente App-V ou via PowerShell (Repair-AppVClientPackage).

## <a name="integration-of-app-v-packages"></a><a href="" id="bkmk-integr-appv-pkgs"></a>Intégration des packages App-V


L’architecture du client et du package App-V fournit une intégration spécifique avec le système d’exploitation local lors de l’ajout et de la publication de packages. Trois fichiers définissent les points d’intégration ou d’extension d’un package App-V :

-   AppXManifest.xml : stockées à l’intérieur du package avec des copies de base stockées dans le magasin de packages et le profil utilisateur. Contient les options créées pendant le processus de séquençage.

-   DeploymentConfig.xml : fournit des informations de configuration sur les points d’extension d’intégration de l’ordinateur et de l’utilisateur.

-   UserConfig.xml : sous-ensemble de la Deploymentconfig.xml qui fournit uniquement des configurations basées sur l’utilisateur et cible uniquement les points d’extension basés sur l’utilisateur.

### <a name="rules-of-integration"></a>Règles d’intégration

Lorsque des applications App-V sont publiées sur un ordinateur avec le client App-V, certaines actions spécifiques ont lieu comme décrit dans la liste ci-dessous :

-   Publication globale : les raccourcis sont stockés dans l’emplacement de profil Tous les utilisateurs et les autres points d’extension sont stockés dans le Registre dans la ruche HKLM.

-   Publication utilisateur : les raccourcis sont stockés dans le profil de compte d’utilisateur actuel et d’autres points d’extension sont stockés dans le Registre dans la ruche HKCU.

-   Sauvegarde et restauration : les données d’application natives existantes et le Registre (par exemple, les inscriptions DE LASO) sont sauvegardes lors de la publication.

    1.  La propriété des packages App-V est basée sur le dernier package intégré dont la propriété est transmise à la dernière application App-V publiée.

    2.  Transferts de propriété d’un package App-V vers un autre lorsque le package App-V propriétaire n’est pas publié. Cela n’initie pas la restauration des données ou du Registre.

    3.  Restituer les données restaurées lorsque le dernier package n’est pas publié ou supprimé par point d’extension.

### <a name="extension-points"></a>Points d’extension

Les fichiers de publication App-V (manifeste et configuration dynamique) fournissent plusieurs points d’extension qui permettent à l’application de s’intégrer au système d’exploitation local. Ces points d’extension effectuent des tâches d’installation d’application classiques, telles que le placement de raccourcis, la création d’associations de types de fichiers et l’inscription de composants. Comme il s’agit d’applications virtualisées qui ne sont pas installées de la même manière qu’une application traditionnelle, il existe certaines différences. Voici une liste des points d’extension abordés dans cette section :

-   Raccourcis

-   Associations de types de fichiers

-   Extensions de l’shell

-   COM

-   Clients logiciels

-   Fonctionnalités de l’application

-   URL Protocol Handler

-   AppPath

-   Application virtuelle

### <a name="shortcuts"></a>Raccourcis

La raccourcie est l’un des éléments de base de l’intégration avec le système d’exploitation et constitue l’interface pour le lancement direct par l’utilisateur d’une application App-V. Lors de la publication et de la publication des applications App-V.

À partir du manifeste du package et des fichiers XML de configuration dynamique, le chemin d’accès à un exécutable d’application spécifique se trouve dans une section semblable à la suivante :

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

Comme mentionné précédemment, les raccourcis App-V sont placés par défaut dans le profil de l’utilisateur en fonction de l’opération d’actualisation. L’actualisation globale place les raccourcis dans le profil Tous les utilisateurs et l’actualisation utilisateur les stocke dans le profil de l’utilisateur spécifique. Le exécutable réel est stocké dans le magasin de packages. L’emplacement du fichier ICO est un emplacement tokenisé dans le package App-V.

### <a name="file-type-associations"></a>Associations de types de fichiers

Le client App-V gère les associations de types de fichiers du système d’exploitation local lors de la publication, ce qui permet aux utilisateurs d’utiliser des appels de type de fichier ou d’ouvrir un fichier avec une extension spécifiquement inscrite (.docx) pour démarrer une application App-V. Les associations de types de fichiers sont présentes dans le manifeste et les fichiers de configuration dynamique, comme le représente l’exemple ci-dessous :

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

**Remarque**  
Dans cet exemple:

-   `<Name>.xdp</Name>` est l’extension

-   `<Name>AcroExch.XDPDoc</Name>` est la valeur ProgId (qui pointe vers le ProgId adjacent)

-   `<CommandLine>"[{AppVPackageRoot}]\Reader\AcroRd32.exe" "%1"</CommandLine>` est la ligne de commande, qui pointe vers l’exécutable de l’application

 

### <a name="shell-extensions"></a>Extensions d'environnement

Les extensions de l’shell sont incorporées automatiquement dans le package pendant le processus de séquençage. Lorsque le package est publié globalement, l’extension de shell offre aux utilisateurs les mêmes fonctionnalités que si l’application était installée localement. L’application ne nécessite aucune configuration ou configuration supplémentaire sur le client pour activer la fonctionnalité d’extension de shell.

**Conditions requises pour l’utilisation des extensions de shell :**

-   Les packages qui contiennent des extensions de shell incorporées doivent être publiés globalement.

-   Le « nombre de bits » de l’application, sequencer et client App-V doit correspondre, sinon les extensions de shell ne fonctionnent pas. Par exemple :

    -   La version de l’application est 64 bits.

    -   Sequencer est en cours d’exécution sur un ordinateur 64 bits.

    -   Le package est remis à un ordinateur client App-V 64 bits.

Le tableau suivant affiche les extensions d’shell pris en charge.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Handler</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Handler de menu contexto</p></td>
<td align="left"><p>Ajoute des éléments de menu au menu context. Elle est appelée avant l’affichage du menu contexto.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Drag-and-drop handler</p></td>
<td align="left"><p>Contrôle l’action lorsque vous cliquez avec le bouton droit sur glisser-déposer et modifie le menu contextiqué qui s’affiche.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Drop target handler</p></td>
<td align="left"><p>Contrôle l’action après qu’un objet de données a été glissé et déposé sur une cible de dépôt telle qu’un fichier.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Data object handler</p></td>
<td align="left"><p>Contrôle l’action après la copie d’un fichier dans le Presse-papiers ou le fait d’être glissé et déposé sur une cible de dépôt. Il peut fournir des formats de Presse-papiers supplémentaires à la cible de drop.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Handler de feuille de propriétés</p></td>
<td align="left"><p>Remplace ou ajoute des pages à la boîte de dialogue feuille de propriétés d’un objet.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Infotip handler</p></td>
<td align="left"><p>Permet de récupérer des indicateurs et des informations d’info-bulle pour un élément et de l’afficher à l’intérieur d’une info-bulle à l’aide de la souris.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Handler de colonnes</p></td>
<td align="left"><p>Permet de créer et d’afficher des colonnes personnalisées en <em> Windows’explorateur de </em> détails. Il peut être utilisé pour étendre le tri et le regroupement.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Handler d’aperçu</p></td>
<td align="left"><p>Permet d’afficher un aperçu d’un fichier dans le Windows d’aperçu de l’Explorateur.</p></td>
</tr>
</tbody>
</table>

 

### <a name="com"></a>COM

Le client App-V prend en charge la publication d’applications avec prise en charge de l’intégration et de la virtualisation COM. L’intégration COM permet au client App-V d’inscrire des objets COM sur le système d’exploitation local et la virtualisation des objets. Dans le cadre de ce document, l’intégration des objets COM nécessite des détails supplémentaires.

App-V prend en charge l’inscription d’objets COM du package vers le système d’exploitation local avec deux types de processus : hors processus et in-process. L’inscription d’objets COM s’accomplit avec un ou plusieurs modes de fonctionnement pour un package App-V spécifique qui inclut off, Isolated et Integrated. Le mode intégré est configuré pour le type hors processus ou in-process. La configuration des modes et types COM s’accomplit avec des fichiers de configuration dynamique (deploymentconfig.xml ou userconfig.xml).

Pour plus d’informations sur l’intégration d’App-V, vous disposez des informations ci-après <https://go.microsoft.com/fwlink/?LinkId=392834> :

### <a name="software-clients-and-application-capabilities"></a>Clients logiciels et fonctionnalités d’application

App-V prend en charge des clients logiciels et des points d’extension de fonctionnalités d’application spécifiques qui permettent aux applications virtualisées d’être inscrites auprès du client logiciel du système d’exploitation. Cela permet aux utilisateurs de sélectionner des programmes par défaut pour des opérations telles que la messagerie électronique, la messagerie instantanée et le lecteur multimédia. Cette opération est effectuée dans le panneau de configuration avec l’option Définir l’accès au programme et les paramètres par défaut de l’ordinateur, et configurée lors du séquençage dans le manifeste ou les fichiers de configuration dynamique. Les fonctionnalités d’application sont uniquement pris en charge lorsque les applications App-V sont publiées globalement.

Exemple d’inscription du client logiciel d’un client de messagerie app-V.

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

**Remarque**  
Dans cet exemple:

-   `<ClientConfiguration EmailEnabled="true" />` est le paramètre global des clients logiciels pour intégrer les clients de messagerie

-   `<EMail MakeDefault="true">` est l’indicateur pour définir un client de messagerie particulier comme client de messagerie par défaut

-   `<MAPILibrary>[{ProgramFilesX86}]\Mozilla Thunderbird\mozMapi32_InUse.dll</MAPILibrary>` est l’inscription de la DLL MAPI

 

### <a name="url-protocol-handler"></a>Handler de protocole d’URL

Les applications ne sont pas toujours spécifiquement appelées applications virtualisées utilisant l’appel de type de fichier. Par exemple, dans une application qui prend en charge l’incorporation d’un lien mailto: à l’intérieur d’un document ou d’une page web, l’utilisateur clique sur un lien mailto: et s’attend à obtenir son client de messagerie inscrit. App-V prend en charge les handlers de protocole d’URL qui peuvent être enregistrés par package auprès du système d’exploitation local. Pendant le séquencement, les handlers de protocole d’URL sont automatiquement ajoutés au package.

Dans les situations où plusieurs applications peuvent inscrire le handler de protocole d’URL spécifique, les fichiers de configuration dynamique peuvent être utilisés pour modifier le comportement et supprimer ou désactiver cette fonctionnalité pour une application qui ne doit pas être l’application principale lancée.

### <a name="apppath"></a>AppPath

Le point d’extension AppPath prend en charge l’appel d’applications App-V directement à partir du système d’exploitation. Cette opération est généralement réalisée à partir de l’écran d’exécution ou de démarrage, en fonction du système d’exploitation, ce qui permet aux administrateurs d’accéder aux applications App-V à partir de commandes ou de scripts de système d’exploitation sans appeler le chemin d’accès spécifique à l’exécutable. Par conséquent, il évite de modifier la variable d’environnement de chemin d’accès système sur tous les systèmes, comme cela est fait lors de la publication.

Le point d’extension AppPath est configuré dans le manifeste ou dans les fichiers de configuration dynamique et est stocké dans le Registre sur l’ordinateur local lors de la publication pour l’utilisateur. Pour plus d’informations sur la révision AppPath : <https://go.microsoft.com/fwlink/?LinkId=392835> .

### <a name="virtual-application"></a>Application virtuelle

Ce sous-système fournit une liste des applications capturées lors du séquençage, qui sont généralement consommées par d’autres composants App-V. L’intégration des points d’extension appartenant à une application particulière peut être désactivée à l’aide de fichiers de configuration dynamique. Par exemple, si un package contient deux applications, il est possible de désactiver tous les points d’extension appartenant à une application, afin d’autoriser uniquement l’intégration des points d’extension d’une autre application.

### <a name="extension-point-rules"></a>Règles de point d’extension

Les points d’extension décrits ci-dessus sont intégrés au système d’exploitation en fonction de la façon dont les packages ont été publiés. La publication globale place les points d’extension dans les emplacements des ordinateurs publics, où la publication des utilisateurs place les points d’extension dans les emplacements des utilisateurs. Par exemple, un raccourci créé sur le bureau et publié globalement entraîne l’utilisation des données de fichier pour le raccourci (%Public%\\Desktop) et les données du Registre (HKLM\\Software\\Classes). Le même raccourci aurait des données de fichier (%UserProfile%\\Desktop) et des données de Registre (HKCU\\Software\\Classes).

Les points d’extension ne sont pas tous publiés de la même façon, où certains points d’extension nécessitent une publication globale et d’autres nécessitent un séquençage sur le système d’exploitation et l’architecture spécifiques où ils sont remis. Vous trouverez ci-dessous un tableau qui décrit ces deux règles clés.

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
<td align="left"><p>Association des types de fichiers</p></td>
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
<td align="left"><p>COM Mode</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Client logiciel</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Fonctionnalités de l’application</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
</tr>
<tr class="even">
<td align="left"><p>Context Menu Handler</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Drag-and-drop Handler</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Data Object Handler</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Property Sheet Handler</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Infotip Handler</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Column Handler</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Extensions de l’shell</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Browser Helper, objet</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
</tr>
<tr class="even">
<td align="left"><p>Active X, objet</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
</tr>
</tbody>
</table>

 

## <a name="dynamic-configuration-processing"></a><a href="" id="bkmk-dynamic-config"></a>Traitement de configuration dynamique


Le déploiement de packages App-V sur un ordinateur ou un utilisateur est très simple. Toutefois, lorsque les organisations déploient des applications AppV au-delà des secteurs d’activité et des frontières géographiques et politiques, la possibilité de séquencer une application une seule fois avec un ensemble de paramètres devient impossible. App-V a été conçu pour ce scénario, car il capture des paramètres et des configurations spécifiques lors du séquençage dans le fichier manifeste, mais prend également en charge la modification avec les fichiers de configuration dynamique.

La configuration dynamique App-V permet de spécifier une stratégie pour un package au niveau de l’ordinateur ou au niveau de l’utilisateur. Les fichiers de configuration dynamique permettent aux ingénieurs de séquencement de modifier la configuration d’un package, après le séquençage, afin de répondre aux besoins de groupes individuels d’utilisateurs ou d’ordinateurs. Dans certains cas, il peut être nécessaire d’apporter des modifications à l’application pour fournir des fonctionnalités appropriées dans l’environnement App-V. Par exemple, il peut être nécessaire d’apporter des modifications aux fichiers \_\*config.xml pour permettre l’exécution de certaines actions à un moment spécifié pendant l’exécution de l’application, comme la désactivation d’une extension mailto pour empêcher une application virtualisée de la modifier à partir d’une autre application.

Les packages App-V contiennent le fichier manifeste à l’intérieur du fichier de package d’application, qui est représentatif des opérations de séquençage et constitue la stratégie de choix, sauf si des fichiers de configuration dynamique sont affectés à un package spécifique. Après le séquençage, les fichiers de configuration dynamique peuvent être modifiés pour permettre la publication d’une application sur différents ordinateurs de bureau ou utilisateurs avec des points d’extension différents. Les deux fichiers de configuration dynamique sont les fichiers de configuration de déploiement dynamique (DDC) et de configuration utilisateur dynamique (CAS). Cette section se concentre sur la combinaison des fichiers manifeste et de configuration dynamique.

### <a name="example-for-dynamic-configuration-files"></a>Exemple pour les fichiers de configuration dynamique

L’exemple ci-dessous illustre la combinaison des fichiers Manifeste, Configuration du déploiement et Configuration utilisateur après la publication et pendant le fonctionnement normal. Ces exemples sont des exemples abrégés de chacun des fichiers. L’objectif est d’afficher la combinaison des fichiers uniquement et de ne pas être une description complète des catégories spécifiques disponibles dans chacun des fichiers. Pour plus d’informations, examinez le Guide de séquençage d’App-V 5 à l’étape : <https://go.microsoft.com/fwlink/?LinkID=269810>

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

## <a name="side-by-side-assemblies"></a><a href="" id="bkmk-sidebyside-assemblies"></a>Assemblys côte à côte


App-V prend en charge l’empaquetage automatique des assemblys côte à côte (SxS) lors du séquençage et du déploiement sur le client lors de la publication d’applications virtuelles. App-V 5 SP2 prend en charge la capture d’assemblys SxS pendant le séquençage pour les assemblys qui ne sont pas présents sur l’ordinateur de séquençage. Et pour les assemblys composés de Visual C++ (version 8 et versions plus récentes) et/ou d’MSXML au moment de l’utilisation, le séquenceur détecte et capture automatiquement ces dépendances même si elles n’ont pas été installées pendant la surveillance. La fonctionnalité Assemblys côte à côte supprime les limitations des versions précédentes d’App-V, où le séquenceur App-V n’a pas capturé les assemblys déjà présents sur la station de travail de séquençage, ni les assemblys limités à une version bit par package. Ce comportement a entraîné le déploiement d’applications App-V pour les clients sans les assemblys SxS requis, ce qui a provoqué des échecs de lancement de l’application. Cela a forcé le processus d’empaquetage à documenter, puis à s’assurer que tous les assemblys requis pour les packages ont été installés localement sur le système d’exploitation client de l’utilisateur afin de garantir la prise en charge des applications virtuelles. En fonction du nombre d’assemblys et de l’absence de documentation d’application pour les dépendances requises, cette tâche était à la fois un défi de gestion et d’implémentation.

La prise en charge de l’assembly côte à côte dans App-V offre les fonctionnalités suivantes.

-   Captures automatiques de l’assembly SxS pendant le séquençage, que l’assembly soit déjà installé ou non sur la station de travail de séquençage.

-   Le client App-V installe automatiquement les assemblys SxS requis sur l’ordinateur client au moment de la publication lorsqu’ils ne sont pas présents.

-   Le séquenceur signale la dépendance d’run-time VC dans le mécanisme de rapport Sequencer.

-   Le sequenceur permet de ne pas mettre en package les assemblys qui sont déjà installés sur le séquenceur, ce qui permet de prendre en charge les scénarios où les assemblys ont été précédemment installés sur les ordinateurs cibles.

### <a name="automatic-publishing-of-sxs-assemblies"></a>Publication automatique des assemblys SxS

Lors de la publication d’un package App-V avec des assemblys SxS, le client App-V vérifie la présence de l’assembly sur l’ordinateur. Si l’assembly n’existe pas, le client déploie l’assembly sur l’ordinateur. Les packages qui font partie des groupes de connexions dépendent des installations d’assembly côte à côte qui font partie des packages de base, car le groupe de connexions ne contient aucune information sur l’installation de l’assembly.

**Remarque**  
La suppression ou la suppression d’un package avec un assembly ne supprime pas les assemblys de ce package.

 

## <a name="client-logging"></a><a href="" id="bkmk-client-logging"></a>Journalisation du client


Le client App-V enregistre les informations dans le journal Windows événements standard au format ETW. Les événements App-V spécifiques se trouvent dans l’observateur d’événements, sous Journaux des applications et des services\\Microsoft\\AppV\\Client.

**Remarque**  
Dans App-V 5.0 SP3, certains journaux ont été consolidés et déplacés vers l’emplacement suivant :

`Event logs/Applications and Services Logs/Microsoft/AppV/ServiceLog`

Pour obtenir la liste des journaux déplacés, voir [à propos d’App-V 5.0 SP3.](about-app-v-50-sp3.md#bkmk-event-logs-moved)

 

Il existe trois catégories spécifiques d’événements enregistrés ci-dessous.

**Admin**: enregistre les événements pour les configurations appliquées au client App-V et contient les principaux avertissements et erreurs.

**Opérationnel**: journalisation de l’exécution app-V générale et de l’utilisation de composants individuels créant un journal d’audit des opérations App-V qui ont été effectuées sur le client App-V.

**Application virtuelle**: enregistre les lancements d’applications virtuelles et l’utilisation de sous-systèmes de virtualisation.






 

 





