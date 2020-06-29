---
title: Référence du schéma de modèle d’application pour UE-V 2. x
description: Référence du schéma de modèle d’application pour UE-V 2. x
author: dansimp
ms.assetid: be8735a5-6a3e-4b1f-ba14-2a3bc3e5a8b6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 03ff6eabae68f07c23d5977f901e6a90e292c6ac
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812336"
---
# Référence du schéma de modèle d’application pour UE-V 2. x


Microsoft User expérience Virtualization (UE-V) 2,0, 2,1 et 2,1 SP1 utilisez les modèles d’emplacement des paramètres XML pour définir les paramètres de l’application de bureau et les paramètres Windows qui sont capturés et appliqués par UE-V. UE-V inclut un ensemble de modèles d’emplacement des paramètres par défaut. Vous pouvez également créer des modèles d’emplacement des paramètres personnalisés avec le générateur UE-V.

Un utilisateur expérimenté peut personnaliser le fichier XML pour un modèle d’emplacement des paramètres. Cette rubrique décrit en détail la structure XML des modèles d’emplacement des paramètres UE-V 2,1 (SP1) et 2,0 et fournit des recommandations pour la modification de ces fichiers.

## Référence du schéma de modèle d’application UE-V 2,1 et 2,1 SP1


Cette section détaille la structure XML du modèle d’emplacement des paramètres UE-V 2,1 et 2,1 SP1 et fournit des instructions pour la modification de ce fichier.

### Dans cette section

-   [Attribut d’encodage et de déclaration XML](#xml21)

-   [Espace de noms et élément racine](#namespace21)

-   [Types de données](#data21)

-   [Élément Name](#name21)

-   [Élément ID](#id21)

-   [Élément version](#version21)

-   [Élément Author](#author21)

-   [Processus et élément de processus](#processes21)

-   [Élément application](#application21)

-   [Élément commun](#common21)

-   [Élément SettingsLocationTemplate](#settingslocationtemplate21)

-   [Annexe: SettingsLocationTemplate. xsd](#appendix21)

### <a href="" id="xml21"></a>Attribut d’encodage et de déclaration XML

**Obligatoire: vrai**

**Type: chaîne**

La déclaration XML doit spécifier l’attribut XML version 1,0 ( &lt; ? xml version = «1.0» &gt; ). Les modèles d’emplacement des paramètres créés par le générateur UE-V sont enregistrés au format UTF-8, même si le codage n’est pas explicitement spécifié. Nous vous recommandons d’inclure l’attribut Encoding = «UTF-8» dans cet élément comme meilleure pratique. Tous les modèles inclus dans le produit spécifient également cette balise (voir les documents dans l’interface utilisateur de%ProgramFiles%\\Microsoft Virtualization\\Templates pour référence). Exemple:

`<?xml version="1.0" encoding="UTF-8"?>`

### <a href="" id="namespace21"></a>Espace de noms et élément racine

**Obligatoire: vrai**

**Type: chaîne**

UE-V utilise l' https://schemas.microsoft.com/UserExperienceVirtualization/2012/SettingsLocationTemplate espace de noms pour toutes les applications. SettingsLocationTemplate est l’élément racine et contient tous les autres éléments. Référencez SettingsLocationTemplate dans tous les modèles à l’aide de cette balise:

`<SettingsLocationTemplate xmlns='https://schemas.microsoft.com/UserExperienceVirtualization/2012/SettingsLocationTemplate'>`

### <a href="" id="data21"></a>Types de données

Il s’agit des types de données pour le schéma de modèle d’application UE-V.

<a href="" id="guid"></a>**GUID** GUID décrit une expression régulière d’identificateur unique global standard au format «\ \ {\ [a-fA-F0-9 \] {8} -\ [a-FA-F0-9] {4} -\ [a------------------- {4} ---- {4} ---------------- {12} ---------------- Cette opération est utilisée dans l’élément Filesetting\\Root\\KnownFolder pour vérifier la mise en forme de dossiers bien connus.

<a href="" id="filenamestring"></a>**FilenameString** FilenameString fait référence au nom de fichier d’un processus à surveiller. Ses valeurs ne sont pas limitées par le caractère &lt; &gt; Regex \ [^ \ \ \ \ \ ^ /: \] +, (autrement dit, ils ne peuvent pas contenir de caractères de barre oblique inverse, d’astérisques ou de signes d’interrogation, de caractère de barre oblique, de signe supérieur ou inférieur à, de barre oblique ou de deux-points).

<a href="" id="idstring"></a>**IdString** IDString fait référence à la valeur d’ID des éléments d’application, SettingsLocationTemplate et éléments communs (utilisés pour décrire les suites d’applications qui partagent des paramètres communs). Ce dernier est limité par le même Regex que FilenameString (\ [^ \ \ \ \ \ \? &lt; &gt; /:\]+).

<a href="" id="templateversion"></a>**TemplateVersion** TemplateVersion est une valeur entière utilisée pour décrire la révision du modèle d’emplacement des paramètres. Sa valeur est comprise entre 0 et 2147483647.

<a href="" id="empty"></a>**Vides** Empty fait référence à une valeur null. Ce champ est utilisé dans Process\\ShellProcess pour indiquer qu’il n’y a pas de processus à surveiller. Cette valeur ne doit pas être utilisée dans les modèles d’application.

<a href="" id="author"></a>**Auteur** Le type de données auteur est un type complexe qui identifie l’auteur d’un modèle. Il contient deux éléments enfants: le **nom** et l' **adresse de courrier**. Dans le type de données auteur, l’élément nom est obligatoire lorsque l’élément de messagerie est facultatif. Ce type est décrit plus en détail dans l’élément SettingsLocationTemplate.

<a href="" id="range"></a>**Plage** Range définit une classe entière composée de deux éléments enfants: **minimum** et **maximum**. Ce type de données est implémenté dans le type de données ProcessVersion. Si ce paramètre est spécifié, les valeurs minimum et maximum doivent être incluses.

<a href="" id="processversion"></a>**ProcessVersion** ProcessVersion définit un type avec quatre éléments enfants: **major**, **Minor**, **Build**et **patch**. Ce type de données est utilisé par l’élément process pour remplir ses valeurs ProductVersion et FileVersion. Les données pour ce type constituent une valeur de plage. L’élément enfant principal est obligatoire et les autres sont facultatifs.

<a href="" id="architecture"></a>**Architecture** Architecture énumère deux valeurs possibles: **Win32** et **Win64**. Ces valeurs sont utilisées pour spécifier l’architecture de processus.

<a href="" id="process"></a>**Processus** Le type de données de processus est un conteneur utilisé pour décrire les processus à surveiller par UE-V. Il contient six éléments enfants: **filename**, **architecture**, **ProductName**, **FileDescription**, **ProductVersion**et **FileVersion**. Ce tableau présente les différents types de données de chaque élément:

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Élément</strong></p></td>
<td align="left"><p><strong>Type de données</strong></p></td>
<td align="left"><p><strong>Mandatory</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>Courts</p></td>
<td align="left"><p>FilenameString</p></td>
<td align="left"><p>Vrai</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Architecture</p></td>
<td align="left"><p>Architecture</p></td>
<td align="left"><p>Faux</p></td>
</tr>
<tr class="even">
<td align="left"><p>ProductName</p></td>
<td align="left"><p>String</p></td>
<td align="left"><p>Faux</p></td>
</tr>
<tr class="odd">
<td align="left"><p>FileDescription</p></td>
<td align="left"><p>String</p></td>
<td align="left"><p>Faux</p></td>
</tr>
<tr class="even">
<td align="left"><p>ProductVersion</p></td>
<td align="left"><p>ProcessVersion</p></td>
<td align="left"><p>Faux</p></td>
</tr>
<tr class="odd">
<td align="left"><p>FileVersion</p></td>
<td align="left"><p>ProcessVersion</p></td>
<td align="left"><p>Faux</p></td>
</tr>
</tbody>
</table>

 

<a href="" id="processes"></a>**Processus** Le type de données processus représente un conteneur pour une collection d’un ou plusieurs éléments de processus. Deux éléments enfants sont pris en charge dans le **type de séquence processus et** **ShellProcess**. Process est un élément de type process et ShellProcess est de type de données Empty. Au moins un élément doit être identifié dans la séquence.

<a href="" id="path"></a>**Path (chemin** ) Path est consommé par RegistrySetting et FileSetting pour faire référence aux chemins d’accès du Registre et des fichiers. Cet élément prend en charge deux attributs facultatifs: **récurrent** et **DeleteIfNotFound**. Les deux valeurs sont définies sur Default = «false».

La récursivité indique que le chemin d’accès et tous les sous-dossiers sont inclus pour les paramètres de fichier ou que toutes les clés de Registre enfant sont incluses pour les paramètres du Registre. Dans les deux cas, tous les éléments du niveau actuel sont inclus dans les données capturées. Pour un objet FileSettings, tous les fichiers dans le dossier spécifié sont inclus dans les données capturées par UE-V, mais les dossiers ne sont pas inclus. Pour les chemins d’accès de Registre, toutes les valeurs du chemin d’accès actuel sont capturées, mais les clés de Registre enfants ne sont pas capturées. Dans les deux cas, veillez à éviter de capturer des jeux de données volumineux ou d’un grand nombre d’éléments.

L’attribut DeleteIfNotFound supprime le paramètre des données de chemin d’accès au stockage des paramètres de l’utilisateur. Cela peut être souhaitable dans les cas où la suppression de ces paramètres du package permet d’économiser une grande quantité d’espace disque sur le serveur de fichiers de chemin d’accès de l’emplacement de stockage des paramètres.

<a href="" id="filemask"></a>**Filemask** FileMask spécifie uniquement certains types de fichiers définis par Path. Par exemple, path peut être `C:\users\username\files` et filemask peut être `*.txt` pour inclure uniquement des fichiers texte.

<a href="" id="registrysetting"></a>**RegistrySetting** RegistrySetting représente un conteneur pour les clés et les valeurs de Registre et le comportement souhaité associé au sein de l’agent UE-V. Quatre éléments enfants sont définis dans ce type: **path**, **Name**, **Exclude**et une séquence des valeurs **path** et **Name**.

<a href="" id="filesetting"></a>**FileSetting** FileSetting contient des paramètres associés à des fichiers et des chemins d’accès aux fichiers. Quatre éléments enfants sont définis: **root**, **path**, **filemask**et **Exclude**. La racine est obligatoire et les autres sont facultatifs.

<a href="" id="settings"></a>**Paramètres** Settings est un conteneur pour tous les paramètres qui s’appliquent à un modèle spécifique. Il contient des instances des paramètres de Registre, de fichier, de SystemParameter et d’CustomAction décrits plus haut. De plus, il peut également contenir les éléments enfants suivants avec des comportements décrits:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Élément</strong></p></td>
<td align="left"><p><strong>Description</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>Asynchrone</p></td>
<td align="left"><p>Les packages de paramètres asynchrones s’appliquent sans bloquer le démarrage de l’application afin que l’application démarre alors que les paramètres sont encore appliqués. Cela s’avère utile pour les paramètres qui peuvent être appliqués de manière asynchrone, par exemple par le <code>get/set</code> biais d’une API telle que SystemParameterSetting.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>PreventOverlappingSynchronization</p></td>
<td align="left"><p>Par défaut, UE-V enregistre uniquement les paramètres d’une application lorsque la dernière instance d’une application utilisant le modèle est fermée. Lorsque cet élément est défini sur «false», UE-V exporte les paramètres même si d’autres instances d’une application sont en cours d’exécution. Les modèles adaptés, qui incluent une section commune des éléments, qui sont livrés avec UE-V, utilisent cet indicateur pour permettre aux paramètres partagés de toujours exporter à la fermeture de l’application, tout en empêchant les paramètres spécifiques à l’application d’être exportés jusqu’à la fin de la dernière instance.</p></td>
</tr>
<tr class="even">
<td align="left"><p>AlwaysApplySettings</p></td>
<td align="left"><p>(introduite dans 2,1)</p>
<p>Ce paramètre force l’application d’un package de paramètres importés même s’il n’y a pas de différences entre le package et l’état actuel de l’application. Ce paramètre doit être utilisé uniquement dans les cas particuliers, car il peut ralentir l’importation des paramètres.</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="name21"></a>Élément Name

**Obligatoire: vrai**

**Type: chaîne**

Nom spécifie un nom unique pour le modèle d’emplacement des paramètres. Il est utilisé à des fins d’affichage lors du référencement du modèle dans WMI, PowerShell, Observateur d’événements et journaux de débogage. En règle générale, évitez de référencer les informations de version, car cela peut être objet à partir de l’élément ProductVersion. Par exemple, spécifiez `<Name>My Application</Name>` plutôt que `<Name>My Application 1.1</Name>` .

**Remarques**  UE-V ne référence pas les DTD externes, de sorte qu’il n’est pas possible d’utiliser des entités nommées dans un modèle d’emplacement des paramètres. Par exemple, n’utilisez pas &reg; pour se référer au signe de marque commerciale enregistré®. Au lieu de cela, utilisez des références numérotées canoniques pour inclure ces types de caractères spéciaux (par exemple, & \ #174 pour le caractère®. Cette règle s’applique à toutes les valeurs de chaîne dans ce document.

<http://www.w3.org/TR/xhtml1/dtds.html>Pour obtenir la liste complète des entités de caractères, voir. Les documents encodés au format UTF-8 peuvent inclure les caractères Unicode directement. L’enregistrement de modèles par le biais du générateur UE-V convertit automatiquement des entités de caractères en leur représentation Unicode.

 

### <a href="" id="id21"></a>Élément ID

**Obligatoire: vrai**

**Type: chaîne**

ID remplit un identificateur unique pour un modèle particulier. Cette balise devient l’identificateur principal utilisé par l’agent UE-V pour référencer le modèle lors de l’exécution (par exemple, voir la sortie des cmdlets Get-UevTemplate et Get-UevTemplateProgram PowerShell). Par Convention, cette balise ne doit contenir aucun espace, ce qui simplifie la création de scripts. Le numéro de version des applications doit être spécifié dans cet élément pour faciliter l’identification du modèle, par exemple `<ID>MicrosoftCalculator6</ID>` ou `<ID>MicrosoftOffice2010Win64</ID>` .

### <a href="" id="version21"></a>Élément version

**Obligatoire: vrai**

**Type: entier**

**Valeur minimale: 0**

**Valeur maximale: 2147483647**

Version identifie la version du modèle d’emplacement paramètres pour le suivi des modifications. Le générateur UE-V augmente automatiquement ce nombre de une unité chaque fois que le modèle est enregistré. Notez que ce champ doit contenir un nombre entier. les valeurs fractionnaires, par exemple, `<Version>2.5</Version>` ne sont pas autorisées.

**Astuce:** Vous pouvez enregistrer des notes sur les changements de version à l’aide d’indicateurs de commentaires XML `<!-- -->` , par exemple:

```xml
  <!--
     Version History

     Version 1 Jul 05, 2012 Initial template created by Generator - Denise@Contoso.com
     Version 2 Jul 31, 2012 Added support for app.exe v2.1.3 - Mark@Contoso.com
     Version 3 Jan 01, 2013 Added font settings support - Mark@Contoso.com
     Version 4 Jan 31, 2013 Added support for plugin settings - Tony@Contoso.com
   -->
  <Version>4</Version>
```

**Important**  Cette valeur est interrogée pour déterminer si une nouvelle version d’un modèle doit être appliquée à un modèle existant dans les cas suivants:

-   Lorsque la tâche de mise à jour automatique du modèle planifié s’exécute

-   Lors de l’exécution de la cmdlet PowerShell Update-UevTemplate

-   Lorsque la méthode microsoft\\uev: SettingsLocationTemplate Update est appelée via WMI

 

### <a href="" id="author21"></a>Élément Author

**Obligatoire: faux**

**Type: chaîne**

Auteur identifie le créateur du modèle d’emplacement des paramètres. Deux éléments enfants facultatifs sont pris en charge: **nom** et **adresse de messagerie**. Les deux attributs sont facultatifs, mais si l’élément enfant de l’élément email est spécifié, il doit être accompagné du nom de l’élément. Auteur fait référence au nom complet du contact pour le modèle d’emplacement des paramètres et la messagerie doit désigner une adresse de messagerie de l’auteur. Nous vous recommandons d’inclure ces informations dans les modèles publiés publiquement (par exemple, dans la [Galerie de modèles UE-V](https://gallery.technet.microsoft.com/site/search?f%5B0%5D.Type=RootCategory&f%5B0%5D.Value=UE-V)).

### <a href="" id="processes21"></a>Processus et élément de processus

**Obligatoire: vrai**

**Type: élément**

Processus contient au moins un `<Process>` élément, qui à son tour contient les éléments enfants suivants: **filename**, **architecture**, **ProductName**, **FileDescription**, **ProductVersion**et **FileVersion**. L’élément enfant de nom de fichier est obligatoire et les autres sont facultatifs. Un élément complet contient des balises similaires à ce qui suit:

```xml
<Process>
  <Filename>MyApplication.exe</Filename>
  <Architecture>Win64</Architecture>
  <ProductName> MyApplication </ProductName>
  <FileDescription>MyApplication.exe</FileDescription>
  <ProductVersion>
    <Major Minimum="2" Maximum="2" />
    <Minor Minimum="0" Maximum="0" />
    <Build Minimum="0" Maximum="0" />
    <Patch Minimum="5" Maximum="5" />
  </ProductVersion>
  <FileVersion>
    <Major Minimum="2" Maximum="2" />
    <Minor Minimum="0" Maximum="0" />
    <Build Minimum="0" Maximum="0" />
    <Patch Minimum="5" Maximum="5" />
  </FileVersion>
</Process>
```

### Courts

**Obligatoire: vrai**

**Type: chaîne**

Nom de fichier correspond au nom de fichier réel de l’exécutable tel qu’il apparaît dans le système de fichiers. Cet élément spécifie le critère principal utilisé par UE-V pour déterminer si un modèle s’applique à un processus ou non. Cet élément doit être spécifié dans le fichier XML du modèle d’emplacement des paramètres.

Les noms de fichier valides ne doivent pas correspondre à l’expression régulière \ [^ \ \ \ \ \ \? &lt; &gt; /: \] +, autrement dit, ils ne peuvent pas contenir de caractères de barre oblique inverse, d’astérisque ou de point d’interrogation, de caractère de barre oblique, de signe supérieur ou inférieur \* | &lt; &gt; /ou: caractères.).

**Astuce:** Pour tester une chaîne par rapport à cette expression régulière, utilisez une fenêtre de commande PowerShell et remplacez le nom de votre exécutable par **YourFileName**:

`"YourFileName.exe" -match  "[\\\?\*\|<>/:]+"`

La valeur **true** indique que la chaîne contient des caractères non valides. Voici quelques exemples de valeurs non valides:

-   \\\\server\\share\\program.exe

-   Programme \ *. exe

-   Pro? ram.exe

-   Programme &lt; 1 &gt; . exe

**Remarques**  Le générateur UE-V encode les caractères supérieur et inférieur, comme &gt; et &lt; respectivement.

 

Dans de rares cas, la valeur FileName n’inclura pas nécessairement l’extension. exe, mais elle doit être spécifiée dans le cadre de la valeur. Par exemple, `<Filename>MyApplictication.exe</Filename>` doit être spécifié au lieu de `<Filename>MyApplictication</Filename>` . Le second exemple n’applique pas le modèle au processus si le véritable nom du fichier exécutable est «MyApplication.exe».

### Architecture

**Obligatoire: faux**

**Type: architecture (chaîne)**

Architecture fait référence à l’architecture de processeur pour laquelle l’exécutable cible a été compilé. Les valeurs valides sont Win32 pour les applications 32 bits ou Win64 pour les applications 64 bits. Le cas échéant, cette balise limite l’applicabilité du modèle d’emplacement des paramètres à une architecture d’application particulière. Pour obtenir un exemple, comparez l’utilisation de l’interface utilisateur%ProgramFiles%\\Microsoft MicrosoftOffice2010Win32.xml Virtualization\\templates\\ MicrosoftOffice2010Win64.xml et les fichiers inclus avec UE-V. Cette fonctionnalité est utile lorsque des chemins relatifs changent entre différentes versions d’un fichier exécutable ou si des paramètres ont été ajoutés ou supprimés lors du passage d’une architecture de processeur à une autre.

Si cet élément est absent, le modèle d’emplacement des paramètres ignore l’architecture du processus et s’applique aux processus 32 et 64 bits en cas d’application du nom de fichier et d’autres attributs.

**Remarques**  UE-V ne prend pas en charge les processeurs ARM dans cette version.

 

### ProductName

**Obligatoire: faux**

**Type: chaîne**

ProductName est un élément facultatif utilisé pour identifier un produit à des fins d’administration ou de création de rapports. ProductName est différent du nom de fichier, car il n’y a pas de restrictions d’expression régulières sur sa valeur. Cela permet d’obtenir des descriptions plus faciles à comprendre du processus pour lequel le nom exécutable n’est pas évident. Exemple:

```xml
<Process>
  <Filename>MyApplication.exe</Filename>
  <ProductName>My Application 6.x by Contoso.com</ProductName>
  <ProductVersion>
    <Major Minimum="6" Maximum="6" />
  </ProductVersion>
</Process>
```

### FileDescription

**Obligatoire: faux**

**Type: chaîne**

FileDescription est une balise facultative qui permet d’obtenir une description administrative du fichier exécutable. Il s’agit d’un champ de texte libre qui peut être utile dans le cas d’un package logiciel permettant d’identifier la fonction du fichier exécutable.

Par exemple, dans une application adaptée, il peut être utile de fournir des rappels sur la fonction de deux exécutables (MyApplication.exe et MyApplicationHelper.exe), comme illustré ci-dessous:

```xml
<Processes>
  <Process>
    <Filename>MyApplication.exe</Filename>
    <FileDescription>My Application Main Engine</ FileDescription>
    <ProductVersion>
      <Major Minimum="6" Maximum="6" />
    </ProductVersion>
  </Process>
  <Process>
    <Filename>MyApplicationHelper.exe</Filename>
    <FileDescription>My Application Background Process Executable</FileDescription>
    <ProductVersion>
      <Major Minimum="6" Maximum="6" />
    </ProductVersion>
  </Process>
</Processes>
```

### ProductVersion

**Obligatoire: faux**

**Type: chaîne**

ProductVersion fait référence aux versions de produit principales et secondaires d’un fichier, ainsi qu’à un niveau de build et de correctif. ProductVersion est un élément facultatif, mais si ce paramètre est spécifié, il doit contenir au moins l’élément enfant principal. La valeur doit exprimer une plage au format minimum = «X» maximum = «Y» où X et Y sont des entiers. Les valeurs minimales et maximales peuvent être identiques.

Le produit et les éléments de version du fichier ne sont pas spécifiés. Cela rend le modèle «version agnostique», ce qui signifie que le modèle s’appliquera à toutes les versions du fichier exécutable spécifié.

**Exemple1:**

Version du produit: 1,0 spécifiée dans UE-V Generator génère le code XML suivant:

```xml
<ProductVersion>
  <Major Minimum="1" Maximum="1" />
  <Minor Minimum="0" Maximum="0" />
</ProductVersion>
```

**Exemple2:**

Version du fichier: 5.0.2.1000 spécifiée dans UE-V Generator génère le code XML suivant:

```xml
<FileVersion>
  <Major Minimum="5" Maximum="5" />
  <Minor Minimum="0" Maximum="0" />
  <Build Minimum="2" Maximum="2" />
  <Patch Minimum="1000" Maximum="1000" />
</FileVersion>
```

**Exemple incorrect 1 – plage incomplète:**

Seul l’attribut minimum est présent. La valeur maximale doit également être incluse dans une plage.

```xml
<ProductVersion>
  <Major Minimum="2" />
</ProductVersion>
```

**Exemple 2 incorrect: Minor spécifié sans élément principal:**

Seuls les éléments mineurs sont présents. Important doit également être inclus.

```xml
<ProductVersion>
  <Minor Minimum="0" Maximum="0" />
</ProductVersion>
```

### FileVersion

**Obligatoire: faux**

**Type: chaîne**

FileVersion fait la distinction entre la version commerciale d’une application publiée et les détails de la build interne d’un composant exécutable. Ces numéros sont identiques pour la plupart des applications commerciales. Le cas échéant, la version de produit d’un fichier indique une identification de version générique d’un fichier, tandis que la version du fichier indique une version spécifique d’un fichier (comme dans le cas d’un correctif ou d’une mise à jour). Cela identifie de façon unique les fichiers sans logique de détection de rupture.

Pour déterminer la version et la version du produit d’un fichier exécutable particulier, cliquez avec le bouton droit sur le fichier dans l’Explorateur Windows, sélectionnez Propriétés, puis cliquez sur l’onglet Détails.

L’inclusion d’un élément FileVersion pour une application permet d’améliorer la logique de détection, mais n’est pas nécessaire pour la plupart des applications. Les paramètres de l’élément ProductVersion sont vérifiés en premier, puis FileVersion est activé. Le paramètre le plus restrictif s’applique.

Les éléments enfants et les règles de syntaxe pour FileVersion sont identiques à ceux de ProductVersion.

```xml
<Process>
  <Filename>MSACCESS.EXE</Filename>
  <Architecture>Win32</Architecture>
  <ProductVersion>
    <Major Minimum="14" Maximum="14" />
    <Minor Minimum="0" Maximum="0" />
  </ProductVersion>
  <FileVersion>
    <Major Minimum="14" Maximum="14" />
    <Minor Minimum="0" Maximum="0" />
  </FileVersion>
</Process>
```

### <a href="" id="application21"></a>Élément application

Application est un conteneur pour les paramètres qui s’appliquent à une application particulière. Il s’agit d’un ensemble de champs/types suivants.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Champ/type</strong></p></td>
<td align="left"><p><strong>Description</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>Name</p></td>
<td align="left"><p>Spécifie un nom unique pour le modèle d’emplacement des paramètres. Il est utilisé à des fins d’affichage lors du référencement du modèle dans WMI, PowerShell, Observateur d’événements et journaux de débogage. Pour plus d’informations, reportez-vous à la section <a href="#name21" data-raw-source="[Name](#name21)"> nom </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ID</p></td>
<td align="left"><p>Remplit un identificateur unique pour un modèle particulier. Cette balise devient l’identificateur principal utilisé par l’agent UE-V pour référencer le modèle lors de l’exécution. Pour plus d’informations, consultez la section <a href="#id21" data-raw-source="[ID](#id21)"> ID </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Description</p></td>
<td align="left"><p>Description facultative du modèle.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>LocalizedNames</p></td>
<td align="left"><p>Nom facultatif affiché dans l’interface utilisateur, localisé par des paramètres régionaux de langue.</p></td>
</tr>
<tr class="even">
<td align="left"><p>LocalizedDescriptions</p></td>
<td align="left"><p>Description de modèle facultative localisée par un paramètre régional de langue.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Version</p></td>
<td align="left"><p>Identifie la version du modèle d’emplacement des paramètres du suivi des modifications. Pour plus d’informations, voir <a href="#version21" data-raw-source="[Version](#version21)"> version </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>DeferToMSAccount</p></td>
<td align="left"><p>Détermine si ce modèle est activé en conjonction avec un compte Microsoft. Si la synchronisation MSA est activée pour un utilisateur sur un ordinateur, ce modèle sera automatiquement désactivé.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>DeferToOffice365</p></td>
<td align="left"><p>Comme pour MSA, cette option détermine si ce modèle est activé en conjonction avec Office 365. Si Office 365 est utilisé pour synchroniser les paramètres, ce modèle sera automatiquement désactivé.</p></td>
</tr>
<tr class="even">
<td align="left"><p>FixedProfile (introduite dans 2,1)</p></td>
<td align="left"><p>Spécifie que ce modèle peut uniquement être associé au profil spécifié dans cet élément et ne peut pas être modifié via WMI ou PowerShell.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Processus</p></td>
<td align="left"><p>Conteneur pour une collection d’un ou de plusieurs éléments de processus. Pour plus d’informations, reportez-vous à la section <a href="#processes21" data-raw-source="[Processes](#processes21)"> processus </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Paramètres</p></td>
<td align="left"><p>Conteneur de tous les paramètres qui s’appliquent à un modèle spécifique. Il contient des instances des paramètres de Registre, de fichier, de SystemParameter et de CustomAction. Pour plus d’informations, consultez la section <strong> paramètres </strong> des <a href="#data21" data-raw-source="[Data types](#data21)"> types de données </a> .</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="common21"></a>Élément commun

Common est semblable à un élément application, mais il est toujours associé à deux éléments d’application ou davantage. La section commune représente l’ensemble des paramètres qui sont partagés entre ces instances d’application. Il s’agit d’un ensemble de champs/types suivants.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Champ/type</strong></p></td>
<td align="left"><p><strong>Description</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>Name</p></td>
<td align="left"><p>Spécifie un nom unique pour le modèle d’emplacement des paramètres. Il est utilisé à des fins d’affichage lors du référencement du modèle dans WMI, PowerShell, Observateur d’événements et journaux de débogage. Pour plus d’informations, reportez-vous à la section <a href="#name21" data-raw-source="[Name](#name21)"> nom </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ID</p></td>
<td align="left"><p>Remplit un identificateur unique pour un modèle particulier. Cette balise devient l’identificateur principal utilisé par l’agent UE-V pour référencer le modèle lors de l’exécution. Pour plus d’informations, consultez la section <a href="#id21" data-raw-source="[ID](#id21)"> ID </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Description</p></td>
<td align="left"><p>Description facultative du modèle.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>LocalizedNames</p></td>
<td align="left"><p>Nom facultatif affiché dans l’interface utilisateur, localisé par des paramètres régionaux de langue.</p></td>
</tr>
<tr class="even">
<td align="left"><p>LocalizedDescriptions</p></td>
<td align="left"><p>Description de modèle facultative localisée par un paramètre régional de langue.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Version</p></td>
<td align="left"><p>Identifie la version du modèle d’emplacement des paramètres du suivi des modifications. Pour plus d’informations, voir <a href="#version21" data-raw-source="[Version](#version21)"> version </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>DeferToMSAccount</p></td>
<td align="left"><p>Détermine si ce modèle est activé en conjonction avec un compte Microsoft. Si la synchronisation MSA est activée pour un utilisateur sur un ordinateur, ce modèle sera automatiquement désactivé.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>DeferToOffice365</p></td>
<td align="left"><p>Comme pour MSA, cette option détermine si ce modèle est activé en conjonction avec Office 365. Si Office 365 est utilisé pour synchroniser les paramètres, ce modèle sera automatiquement désactivé.</p></td>
</tr>
<tr class="even">
<td align="left"><p>FixedProfile (introduite dans 2,1)</p></td>
<td align="left"><p>Spécifie que ce modèle peut uniquement être associé au profil spécifié dans cet élément et ne peut pas être modifié via WMI ou PowerShell.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Paramètres</p></td>
<td align="left"><p>Conteneur de tous les paramètres qui s’appliquent à un modèle spécifique. Il contient des instances des paramètres de Registre, de fichier, de SystemParameter et de CustomAction. Pour plus d’informations, consultez la section <strong> paramètres </strong> des <a href="#data21" data-raw-source="[Data types](#data21)"> types de données </a> .</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="settingslocationtemplate21"></a>Élément SettingsLocationTemplate

Cet élément définit les paramètres d’une application unique ou d’une suite d’applications.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Champ/type</strong></p></td>
<td align="left"><p><strong>Description</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>Name</p></td>
<td align="left"><p>Spécifie un nom unique pour le modèle d’emplacement des paramètres. Il est utilisé à des fins d’affichage lors du référencement du modèle dans WMI, PowerShell, Observateur d’événements et journaux de débogage. Pour plus d’informations, reportez-vous à la section <a href="#name21" data-raw-source="[Name](#name21)"> nom </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ID</p></td>
<td align="left"><p>Remplit un identificateur unique pour un modèle particulier. Cette balise devient l’identificateur principal utilisé par l’agent UE-V pour référencer le modèle lors de l’exécution. Pour plus d’informations, consultez la section <a href="#id21" data-raw-source="[ID](#id21)"> ID </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Description</p></td>
<td align="left"><p>Description facultative du modèle.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>LocalizedNames</p></td>
<td align="left"><p>Nom facultatif affiché dans l’interface utilisateur, localisé par des paramètres régionaux de langue.</p></td>
</tr>
<tr class="even">
<td align="left"><p>LocalizedDescriptions</p></td>
<td align="left"><p>Description de modèle facultative localisée par un paramètre régional de langue.</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="appendix21"></a>Annexe: SettingsLocationTemplate. xsd

Voici le fichier SettingsLocationTemplate. xsd montrant ses éléments, éléments enfants, attributs et paramètres:

```xml
<?xml version="1.0" encoding="utf-8"?>
<xs:schema id="UevSettingsLocationTemplate"
  targetNamespace="https://schemas.microsoft.com/UserExperienceVirtualization/2013A/SettingsLocationTemplate"
  elementFormDefault="qualified"
  xmlns="https://schemas.microsoft.com/UserExperienceVirtualization/2013A/SettingsLocationTemplate"
  xmlns:mstns="https://schemas.microsoft.com/UserExperienceVirtualization/2013A/SettingsLocationTemplate"
  xmlns:xs="http://www.w3.org/2001/XMLSchema">

    <xs:simpleType name="Guid">
        <xs:restriction base="xs:string">
            <xs:pattern value="\{[a-fA-F0-9]{8}-[a-fA-F0-9]{4}-[a-fA-F0-9]{4}-[a-fA-F0-9]{4}-[a-fA-F0-9]{12}\}" />
        </xs:restriction>
    </xs:simpleType>

    <xs:simpleType name="FilenameString">
        <xs:restriction base="xs:string">
            <xs:pattern value="[^\\\?\*\|&lt;&gt;/:]+" />
        </xs:restriction>
    </xs:simpleType>

    <xs:simpleType name="IDString">
        <xs:restriction base="xs:string">
            <xs:pattern value="[^\\\?\*\|&lt;&gt;/:.]+" />
        </xs:restriction>
    </xs:simpleType>

    <xs:simpleType name="CompositeIDString">
        <xs:restriction base="xs:string">
            <xs:pattern value="[^\\\?\*\|&lt;&gt;/:.]+([.][^\\\?\*\|&lt;&gt;/:.]+)?" />
        </xs:restriction>
    </xs:simpleType>

    <xs:simpleType name="TemplateVersion">
        <xs:restriction base="xs:integer">
            <xs:minInclusive value="0" />
            <xs:maxInclusive value="2147483647" />
        </xs:restriction>
    </xs:simpleType>

    <xs:complexType name="Empty">
        <xs:sequence/>
    </xs:complexType>

    <xs:complexType name="LocalizedString">
        <xs:simpleContent>
            <xs:extension base="xs:string">
                <xs:attribute name="Locale" type="xs:string" use="required"/>
            </xs:extension>
        </xs:simpleContent>
    </xs:complexType>

    <xs:complexType name="LocalizedName">
        <xs:sequence>
            <xs:element name="Name" type="LocalizedString" minOccurs="1" maxOccurs="unbounded" />
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="LocalizedDescription">
        <xs:sequence>
            <xs:element name="Description" type="LocalizedString" minOccurs="1" maxOccurs="unbounded" />
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="ReplacedTemplates">
      <xs:sequence>
        <xs:element name="ID" type="CompositeIDString" minOccurs="1" maxOccurs="unbounded" />
    </xs:sequence>
    </xs:complexType>

    <xs:complexType name="Author">
        <xs:all>
            <xs:element name="Name" type="xs:string" minOccurs="1" />
            <xs:element name="Email" type="xs:string" minOccurs="0" />
        </xs:all>
    </xs:complexType>

    <xs:complexType name="Range">
        <xs:attribute name="Minimum" type="xs:integer" use="required"/>
        <xs:attribute name="Maximum" type="xs:integer" use="required"/>
    </xs:complexType>

    <xs:complexType name="ProcessVersion">
        <xs:sequence>
            <xs:element name="Major" type="Range" minOccurs="1" />
            <xs:element name="Minor" type="Range" minOccurs="0" />
            <xs:element name="Build" type="Range" minOccurs="0" />
            <xs:element name="Patch" type="Range" minOccurs="0" />
        </xs:sequence>
    </xs:complexType>

    <xs:simpleType name="Architecture">
        <xs:restriction base="xs:string">
            <xs:enumeration value="Win32"/>
            <xs:enumeration value="Win64"/>
        </xs:restriction>
    </xs:simpleType>

    <xs:complexType name="Process">
        <xs:sequence>
            <xs:element name="Filename" type="FilenameString" minOccurs="1" />
            <xs:element name="Architecture" type="Architecture" minOccurs="0" />
            <xs:element name="ProductName" type="xs:string" minOccurs="0" />
            <xs:element name="FileDescription" type="xs:string" minOccurs="0" />
            <xs:element name="ProductVersion" type="ProcessVersion" minOccurs="0" maxOccurs="unbounded"/>
            <xs:element name="FileVersion" type="ProcessVersion" minOccurs="0" maxOccurs="unbounded"/>
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="Processes">
        <xs:sequence>
            <xs:choice minOccurs="1">
                <xs:element name="Process" type="Process" />
                <xs:element name="ShellProcess" type="Empty" />
            </xs:choice>
            <xs:element name="Process" type="Process" minOccurs="0" maxOccurs="unbounded" />
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="Path">
        <xs:simpleContent>
            <xs:extension base="xs:string">
                <xs:attribute name="Recursive" type="xs:boolean" default="false"/>
                <xs:attribute name="DeleteIfNotFound" type="xs:boolean" default="false"/>
            </xs:extension>
        </xs:simpleContent>
    </xs:complexType>

    <xs:complexType name="RegistrySetting">
        <xs:sequence>
            <xs:element name="Path" type="Path" />
            <xs:element name="Name" type="xs:string" minOccurs="0" maxOccurs="unbounded" />
            <xs:element name="Exclude" minOccurs="0" maxOccurs="unbounded">
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="Path" type="Path" minOccurs="0" />
                        <xs:element name="Name" type="xs:string" minOccurs="0" maxOccurs="unbounded" />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="FileSetting">
        <xs:sequence>

            <xs:element name="Root">
                <xs:complexType>
                    <xs:choice>
                        <xs:element name="KnownFolder" type="Guid" />
                        <xs:element name="RegistryEntry" type="xs:string" />
                        <xs:element name="EnvironmentVariable" type="xs:string" />
                    </xs:choice>
                </xs:complexType>
            </xs:element>

            <xs:element name="Path" minOccurs="0" type="Path" />
            <xs:element name="FileMask" type="xs:string" minOccurs="0" maxOccurs="unbounded"/>

            <xs:element name="Exclude" minOccurs="0" maxOccurs="unbounded">
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="Path" type="Path" minOccurs="0" />
                        <xs:element name="FileMask" type="xs:string" minOccurs="0" maxOccurs="unbounded" />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>

        </xs:sequence>
    </xs:complexType>

    <xs:simpleType name="CustomActionSetting">
        <xs:restriction base="xs:anyURI"/>
    </xs:simpleType>

    <xs:simpleType name="SystemParameterSetting">
        <xs:restriction base="xs:string">

            <!-- Accessibility parameters -->
            <xs:enumeration value="AccessTimeout"/>
            <xs:enumeration value="AudioDescription"/>
            <xs:enumeration value="ClientAreaAnimation"/>
            <xs:enumeration value="DisableOverlappedContent"/>
            <xs:enumeration value="FilterKeys"/>
            <xs:enumeration value="FocusBorderHeight"/>
            <xs:enumeration value="FocusBorderWidth"/>
            <xs:enumeration value="HighContrast"/>
            <xs:enumeration value="MessageDuration"/>
            <xs:enumeration value="MouseClickLock"/>
            <xs:enumeration value="MouseClickLockTime"/>
            <xs:enumeration value="MouseKeys"/>
            <xs:enumeration value="MouseSonar"/>
            <xs:enumeration value="MouseVanish"/>
            <xs:enumeration value="ScreenReader"/>
            <xs:enumeration value="ShowSounds"/>
            <xs:enumeration value="SoundSentry"/>
            <xs:enumeration value="StickyKeys"/>
            <xs:enumeration value="ToggleKeys"/>

            <!-- Input parameters -->
            <xs:enumeration value="Beep"/>
            <xs:enumeration value="BlockSendInputResets"/>
            <xs:enumeration value="DefaultInputLang"/>
            <xs:enumeration value="DoubleClickTime"/>
            <xs:enumeration value="DoubleClkHeight"/>
            <xs:enumeration value="DoubleClkWidth"/>
            <xs:enumeration value="KeyboardCues"/>
            <xs:enumeration value="KeyboardDelay"/>
            <xs:enumeration value="KeyboardPref"/>
            <xs:enumeration value="KeyboardSpeed"/>
            <xs:enumeration value="Mouse"/>
            <xs:enumeration value="MouseButtonSwap"/>
            <xs:enumeration value="MouseHoverHeight"/>
            <xs:enumeration value="MouseHoverTime"/>
            <xs:enumeration value="MouseHoverWidth"/>
            <xs:enumeration value="MouseSpeed"/>
            <xs:enumeration value="MouseTrails"/>
            <xs:enumeration value="SnapToDefButton"/>
            <xs:enumeration value="WheelScrollChars"/>
            <xs:enumeration value="WheelScrollLines"/>

            <!-- Desktop parameters (limited subset) -->
            <xs:enumeration value="DeskWallpaper"/>
            <xs:enumeration value="DesktopColor"/>

        </xs:restriction>
    </xs:simpleType>

    <xs:complexType name="Settings">
        <xs:sequence>
            <xs:element name="Asynchronous" type="xs:boolean" minOccurs="0" />
            <xs:element name="PreventOverlappingSynchronization" type="xs:boolean" minOccurs="0" />
            <xs:element name="AlwaysApplySettings" type="xs:boolean" minOccurs="0" />
            <xs:choice minOccurs="0" maxOccurs="unbounded">
                <xs:element name="Registry" type="RegistrySetting" />
                <xs:element name="File" type="FileSetting" />
                <xs:element name="SystemParameter" type="SystemParameterSetting" />
                <xs:element name="CustomAction" type="CustomActionSetting" />
            </xs:choice>
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="Common">
        <xs:sequence>
            <xs:element name="Name" type="xs:string" />
            <xs:element name="ID" type="IDString" />
            <xs:element name="ReplacedTemplates" type="ReplacedTemplates" minOccurs="0" />
            <xs:element name="Description" type="xs:string" minOccurs="0" />
            <xs:element name="LocalizedNames" type="LocalizedName" minOccurs="0" />
            <xs:element name="LocalizedDescriptions" type="LocalizedDescription" minOccurs="0" />
            <xs:element name="Version" type="xs:integer" />
            <xs:element name="DeferToMSAccount" type="Empty"  minOccurs="0" />
            <xs:element name="DeferToOffice365" type="Empty" minOccurs="0" />
            <xs:element name="Settings" type="Settings" />
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="Application">
        <xs:sequence>
            <xs:element name="Name" type="xs:string" />
            <xs:element name="ID" type="IDString" />
            <xs:element name="ReplacedTemplates" type="ReplacedTemplates" minOccurs="0" />
            <xs:element name="Description" type="xs:string" minOccurs="0" />
            <xs:element name="LocalizedNames" type="LocalizedName" minOccurs="0" />
            <xs:element name="LocalizedDescriptions" type="LocalizedDescription" minOccurs="0" />
            <xs:element name="Version" type="xs:integer" />
            <xs:element name="DeferToMSAccount" type="Empty"  minOccurs="0" />
            <xs:element name="DeferToOffice365" type="Empty" minOccurs="0" />
            <xs:element name="Processes" type="Processes" />
            <xs:element name="Settings" type="Settings" />
        </xs:sequence>
    </xs:complexType>


    <xs:element name="SettingsLocationTemplate">
        <xs:complexType>
            <xs:sequence>

                <xs:element name="Name" type="xs:string" />
                <xs:element name="ID" type="IDString" />
                <xs:element name="Description" type="xs:string" minOccurs="0" />
                <xs:element name="LocalizedNames" type="LocalizedName" minOccurs="0" />
                <xs:element name="LocalizedDescriptions" type="LocalizedDescription" minOccurs="0" />

                <xs:choice>

                    <!-- Single application -->
                    <xs:sequence>
                        <xs:element name="ReplacedTemplates" type="ReplacedTemplates" minOccurs="0" />
                        <xs:element name="Version" type="TemplateVersion" />
                        <xs:element name="Author" type="Author" minOccurs="0" />
                        <xs:element name="FixedProfile" type="xs:string"  minOccurs="0" />
                        <xs:element name="DeferToMSAccount" type="Empty"  minOccurs="0" />
                        <xs:element name="DeferToOffice365" type="Empty" minOccurs="0" />
                        <xs:element name="Processes" type="Processes" />
                        <xs:element name="Settings" type="Settings" />
                    </xs:sequence>

                    <!-- Suite of applications -->
                    <xs:sequence>
                        <xs:element name="ManageSuiteOnly" type="xs:boolean" minOccurs="0" />
                        <xs:element name="Author" type="Author" minOccurs="0" />
                        <xs:element name="FixedProfile" type="xs:string"  minOccurs="0" />
                        <xs:element name="Common" type="Common" />
                        <xs:element name="Application" type="Application" minOccurs="2" maxOccurs="unbounded" />
                    </xs:sequence>

                </xs:choice>

            </xs:sequence>
        </xs:complexType>
    </xs:element>
    <!-- SettingsLocationTemplate -->

</xs:schema>
```

## Référence du schéma de modèle d’application UE-V 2,0


Cette section détaille la structure XML du modèle d’emplacement des paramètres d’UE-V 2,0 et fournit des recommandations pour la modification de ce fichier.

### Dans cette section

-   [Attribut d’encodage et de déclaration XML](#xml)

-   [Espace de noms et élément racine](#namespace)

-   [Types de données](#data)

-   [Élément Name](#name)

-   [Élément ID](#id)

-   [Élément version](#version)

-   [Élément Author](#author)

-   [Processus et élément de processus](#processes)

-   [Élément application](#application)

-   [Élément commun](#common)

-   [Élément SettingsLocationTemplate](#settingslocationtemplate)

-   [Annexe: SettingsLocationTemplate. xsd](#appendix)

### <a href="" id="xml"></a>Attribut d’encodage et de déclaration XML

**Obligatoire: vrai**

**Type: chaîne**

La déclaration XML doit spécifier l’attribut XML version 1,0 ( &lt; ? xml version = «1.0» &gt; ). Les modèles d’emplacement des paramètres créés par le générateur UE-V sont enregistrés au format UTF-8, même si le codage n’est pas explicitement spécifié. Nous vous recommandons d’inclure l’attribut Encoding = «UTF-8» dans cet élément comme meilleure pratique. Tous les modèles inclus dans le produit spécifient également cette balise (voir les documents dans l’interface utilisateur de%ProgramFiles%\\Microsoft Virtualization\\Templates pour référence). Exemple:

`<?xml version="1.0" encoding="UTF-8"?>`

### <a href="" id="namespace"></a>Espace de noms et élément racine

**Obligatoire: vrai**

**Type: chaîne**

UE-V utilise l' https://schemas.microsoft.com/UserExperienceVirtualization/2012/SettingsLocationTemplate espace de noms pour toutes les applications. SettingsLocationTemplate est l’élément racine et contient tous les autres éléments. Référencez SettingsLocationTemplate dans tous les modèles à l’aide de cette balise:

`<SettingsLocationTemplate xmlns='https://schemas.microsoft.com/UserExperienceVirtualization/2012/SettingsLocationTemplate'>`

### <a href="" id="data"></a>Types de données

Il s’agit des types de données pour le schéma de modèle d’application UE-V.

<a href="" id="guid"></a>**GUID** GUID décrit une expression régulière d’identificateur unique global standard au format «\ \ {\ [a-fA-F0-9 \] {8} -\ [a-FA-F0-9] {4} -\ [a------------------- {4} ---- {4} ---------------- {12} ---------------- Cette opération est utilisée dans l’élément Filesetting\\Root\\KnownFolder pour vérifier la mise en forme de dossiers bien connus.

<a href="" id="filenamestring"></a>**FilenameString** FilenameString fait référence au nom de fichier d’un processus à surveiller. Ses valeurs ne sont pas limitées par le caractère &lt; &gt; Regex \ [^ \ \ \ \ \ ^ /: \] +, (autrement dit, ils ne peuvent pas contenir de caractères de barre oblique inverse, d’astérisques ou de signes d’interrogation, de caractère de barre oblique, de signe supérieur ou inférieur à, de barre oblique ou de deux-points).

<a href="" id="idstring"></a>**IdString** IDString fait référence à la valeur d’ID des éléments d’application, SettingsLocationTemplate et éléments communs (utilisés pour décrire les suites d’applications qui partagent des paramètres communs). Ce dernier est limité par le même Regex que FilenameString (\ [^ \ \ \ \ \ \? &lt; &gt; /:\]+).

<a href="" id="templateversion"></a>**TemplateVersion** TemplateVersion est une valeur entière utilisée pour décrire la révision du modèle d’emplacement des paramètres. Sa valeur est comprise entre 0 et 2147483647.

<a href="" id="empty"></a>**Vides** Empty fait référence à une valeur null. Ce champ est utilisé dans Process\\ShellProcess pour indiquer qu’il n’y a pas de processus à surveiller. Cette valeur ne doit pas être utilisée dans les modèles d’application.

<a href="" id="author"></a>**Auteur** Le type de données auteur est un type complexe qui identifie l’auteur d’un modèle. Il contient deux éléments enfants: le **nom** et l' **adresse de courrier**. Dans le type de données auteur, l’élément nom est obligatoire lorsque l’élément de messagerie est facultatif. Ce type est décrit plus en détail dans l’élément SettingsLocationTemplate.

<a href="" id="range"></a>**Plage** Range définit une classe entière composée de deux éléments enfants: **minimum** et **maximum**. Ce type de données est implémenté dans le type de données ProcessVersion. Si ce paramètre est spécifié, les valeurs minimum et maximum doivent être incluses.

<a href="" id="processversion"></a>**ProcessVersion** ProcessVersion définit un type avec quatre éléments enfants: **major**, **Minor**, **Build**et **patch**. Ce type de données est utilisé par l’élément process pour remplir ses valeurs ProductVersion et FileVersion. Les données pour ce type constituent une valeur de plage. L’élément enfant principal est obligatoire et les autres sont facultatifs.

<a href="" id="architecture"></a>**Architecture** Architecture énumère deux valeurs possibles: **Win32** et **Win64**. Ces valeurs sont utilisées pour spécifier l’architecture de processus.

<a href="" id="process"></a>**Processus** Le type de données de processus est un conteneur utilisé pour décrire les processus à surveiller par UE-V. Il contient six éléments enfants: **filename**, **architecture**, **ProductName**, **FileDescription**, **ProductVersion**et **FileVersion**. Ce tableau présente les différents types de données de chaque élément:

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Élément</th>
<th align="left">Type de données</th>
<th align="left">Mandatory</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Courts</p></td>
<td align="left"><p>FilenameString</p></td>
<td align="left"><p>Vrai</p></td>
</tr>
<tr class="even">
<td align="left"><p>Architecture</p></td>
<td align="left"><p>Architecture</p></td>
<td align="left"><p>Faux</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ProductName</p></td>
<td align="left"><p>String</p></td>
<td align="left"><p>Faux</p></td>
</tr>
<tr class="even">
<td align="left"><p>FileDescription</p></td>
<td align="left"><p>String</p></td>
<td align="left"><p>Faux</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ProductVersion</p></td>
<td align="left"><p>ProcessVersion</p></td>
<td align="left"><p>Faux</p></td>
</tr>
<tr class="even">
<td align="left"><p>FileVersion</p></td>
<td align="left"><p>ProcessVersion</p></td>
<td align="left"><p>Faux</p></td>
</tr>
</tbody>
</table>

 

<a href="" id="processes"></a>**Processus** Le type de données processus représente un conteneur pour une collection d’un ou plusieurs éléments de processus. Deux éléments enfants sont pris en charge dans le **type de séquence processus et** **ShellProcess**. Process est un élément de type process et ShellProcess est de type de données Empty. Au moins un élément doit être identifié dans la séquence.

<a href="" id="path"></a>**Path (chemin** ) Path est consommé par RegistrySetting et FileSetting pour faire référence aux chemins d’accès du Registre et des fichiers. Cet élément prend en charge deux attributs facultatifs: **récurrent** et **DeleteIfNotFound**. Les deux valeurs sont définies sur Default = «false».

La récursivité indique que le chemin d’accès et tous les sous-dossiers sont inclus pour les paramètres de fichier ou que toutes les clés de Registre enfant sont incluses pour les paramètres du Registre. Dans les deux cas, tous les éléments du niveau actuel sont inclus dans les données capturées. Pour un objet FileSettings, tous les fichiers dans le dossier spécifié sont inclus dans les données capturées par UE-V, mais les dossiers ne sont pas inclus. Pour les chemins d’accès de Registre, toutes les valeurs du chemin d’accès actuel sont capturées, mais les clés de Registre enfants ne sont pas capturées. Dans les deux cas, veillez à éviter de capturer des jeux de données volumineux ou d’un grand nombre d’éléments.

L’attribut DeleteIfNotFound supprime le paramètre des données de chemin d’accès au stockage des paramètres de l’utilisateur. Cela peut être souhaitable dans les cas où la suppression de ces paramètres du package permet d’économiser une grande quantité d’espace disque sur le serveur de fichiers de chemin d’accès de l’emplacement de stockage des paramètres.

<a href="" id="filemask"></a>**Filemask** FileMask spécifie uniquement certains types de fichiers définis par Path. Par exemple, path peut être `C:\users\username\files` et filemask peut être `*.txt` pour inclure uniquement des fichiers texte.

<a href="" id="registrysetting"></a>**RegistrySetting** RegistrySetting représente un conteneur pour les clés et les valeurs de Registre et le comportement souhaité associé au sein de l’agent UE-V. Quatre éléments enfants sont définis dans ce type: **path**, **Name**, **Exclude**et une séquence des valeurs **path** et **Name**.

<a href="" id="filesetting"></a>**FileSetting** FileSetting contient des paramètres associés à des fichiers et des chemins d’accès aux fichiers. Quatre éléments enfants sont définis: **root**, **path**, **filemask**et **Exclude**. La racine est obligatoire et les autres sont facultatifs.

<a href="" id="settings"></a>**Paramètres** Settings est un conteneur pour tous les paramètres qui s’appliquent à un modèle spécifique. Il contient des instances des paramètres de Registre, de fichier, de SystemParameter et d’CustomAction décrits plus haut. De plus, il peut également contenir les éléments enfants suivants avec des comportements décrits:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Élément</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Asynchrone</p></td>
<td align="left"><p>Les packages de paramètres asynchrones s’appliquent sans bloquer le démarrage de l’application afin que l’application démarre alors que les paramètres sont encore appliqués. Cela s’avère utile pour les paramètres qui peuvent être appliqués de manière asynchrone, par exemple par le <code>get/set</code> biais d’une API telle que SystemParameterSetting.</p></td>
</tr>
<tr class="even">
<td align="left"><p>PreventOverlappingSynchronization</p></td>
<td align="left"><p>Par défaut, UE-V enregistre uniquement les paramètres d’une application lorsque la dernière instance d’une application utilisant le modèle est fermée. Lorsque cet élément est défini sur «false», UE-V exporte les paramètres même si d’autres instances d’une application sont en cours d’exécution. Les modèles adaptés, qui incluent une section commune des éléments, qui sont livrés avec UE-V, utilisent cet indicateur pour permettre aux paramètres partagés de toujours exporter à la fermeture de l’application, tout en empêchant les paramètres spécifiques à l’application d’être exportés jusqu’à la fin de la dernière instance.</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="name"></a>Élément Name

**Obligatoire: vrai**

**Type: chaîne**

Nom spécifie un nom unique pour le modèle d’emplacement des paramètres. Il est utilisé à des fins d’affichage lors du référencement du modèle dans WMI, PowerShell, Observateur d’événements et journaux de débogage. En règle générale, évitez de référencer les informations de version, car cela peut être objet à partir de l’élément ProductVersion. Par exemple, spécifiez `<Name>My Application</Name>` plutôt que `<Name>My Application 1.1</Name>` .

**Remarques**  UE-V ne référence pas les DTD externes, de sorte qu’il n’est pas possible d’utiliser des entités nommées dans un modèle d’emplacement des paramètres. Par exemple, n’utilisez pas &reg; pour se référer au signe de marque commerciale enregistré®. Au lieu de cela, utilisez des références numérotées canoniques pour inclure ces types de caractères spéciaux (par exemple, & \ #174 pour le caractère®. Cette règle s’applique à toutes les valeurs de chaîne dans ce document.

<http://www.w3.org/TR/xhtml1/dtds.html>Pour obtenir la liste complète des entités de caractères, voir. Les documents encodés au format UTF-8 peuvent inclure les caractères Unicode directement. L’enregistrement de modèles par le biais du générateur UE-V convertit automatiquement des entités de caractères en leur représentation Unicode.

 

### <a href="" id="id"></a>Élément ID

**Obligatoire: vrai**

**Type: chaîne**

ID remplit un identificateur unique pour un modèle particulier. Cette balise devient l’identificateur principal utilisé par l’agent UE-V pour référencer le modèle lors de l’exécution (par exemple, voir la sortie des cmdlets Get-UevTemplate et Get-UevTemplateProgram PowerShell). Par Convention, cette balise ne doit contenir aucun espace, ce qui simplifie la création de scripts. Le numéro de version des applications doit être spécifié dans cet élément pour faciliter l’identification du modèle, par exemple `<ID>MicrosoftCalculator6</ID>` ou `<ID>MicrosoftOffice2010Win64</ID>` .

### <a href="" id="version"></a>Élément version

**Obligatoire: vrai**

**Type: entier**

**Valeur minimale: 0**

**Valeur maximale: 2147483647**

Version identifie la version du modèle d’emplacement paramètres pour le suivi des modifications. Le générateur UE-V augmente automatiquement ce nombre de une unité chaque fois que le modèle est enregistré. Notez que ce champ doit contenir un nombre entier. les valeurs fractionnaires, par exemple, `<Version>2.5</Version>` ne sont pas autorisées.

**Astuce:** Vous pouvez enregistrer des notes sur les changements de version à l’aide d’indicateurs de commentaires XML `<!-- -->` , par exemple:

```xml
<!--
    Version History

    Version 1 Jul 05, 2012 Initial template created by Generator - Denise@Contoso.com
    Version 2 Jul 31, 2012 Added support for app.exe v2.1.3 - Mark@Contoso.com
    Version 3 Jan 01, 2013 Added font settings support - Mark@Contoso.com
    Version 4 Jan 31, 2013 Added support for plugin settings - Tony@Contoso.com
  -->
<Version>4</Version>
```

**Important**  Cette valeur est interrogée pour déterminer si une nouvelle version d’un modèle doit être appliquée à un modèle existant dans les cas suivants:

-   Lorsque la tâche de mise à jour automatique du modèle planifié s’exécute

-   Lors de l’exécution de la cmdlet PowerShell Update-UevTemplate

-   Lorsque la méthode microsoft\\uev: SettingsLocationTemplate Update est appelée via WMI

 

### <a href="" id="author"></a>Élément Author

**Obligatoire: faux**

**Type: chaîne**

Auteur identifie le créateur du modèle d’emplacement des paramètres. Deux éléments enfants facultatifs sont pris en charge: **nom** et **adresse de messagerie**. Les deux attributs sont facultatifs, mais si l’élément enfant de l’élément email est spécifié, il doit être accompagné du nom de l’élément. Auteur fait référence au nom complet du contact pour le modèle d’emplacement des paramètres et la messagerie doit désigner une adresse de messagerie de l’auteur. Nous vous recommandons d’inclure ces informations dans les modèles publiés publiquement (par exemple, dans la [Galerie de modèles UE-V](https://gallery.technet.microsoft.com/site/search?f%5B0%5D.Type=RootCategory&f%5B0%5D.Value=UE-V)).

### <a href="" id="processes"></a>Processus et élément de processus

**Obligatoire: vrai**

**Type: élément**

Processus contient au moins un `<Process>` élément, qui à son tour contient les éléments enfants suivants: **filename**, **architecture**, **ProductName**, **FileDescription**, **ProductVersion**et **FileVersion**. L’élément enfant de nom de fichier est obligatoire et les autres sont facultatifs. Un élément complet contient des balises similaires à ce qui suit:

```xml
<Process>
  <Filename>MyApplication.exe</Filename>
  <Architecture>Win64</Architecture>
  <ProductName> MyApplication </ProductName>
  <FileDescription>MyApplication.exe</FileDescription>
  <ProductVersion>
    <Major Minimum="2" Maximum="2" />
    <Minor Minimum="0" Maximum="0" />
    <Build Minimum="0" Maximum="0" />
    <Patch Minimum="5" Maximum="5" />
  </ProductVersion>
  <FileVersion>
    <Major Minimum="2" Maximum="2" />
    <Minor Minimum="0" Maximum="0" />
    <Build Minimum="0" Maximum="0" />
    <Patch Minimum="5" Maximum="5" />
  </FileVersion>
</Process>
```

### Courts

**Obligatoire: vrai**

**Type: chaîne**

Nom de fichier correspond au nom de fichier réel de l’exécutable tel qu’il apparaît dans le système de fichiers. Cet élément spécifie le critère principal utilisé par UE-V pour déterminer si un modèle s’applique à un processus ou non. Cet élément doit être spécifié dans le fichier XML du modèle d’emplacement des paramètres.

Les noms de fichier valides ne doivent pas correspondre à l’expression régulière \ [^ \ \ \ \ \ \? &lt; &gt; /: \] +, autrement dit, ils ne peuvent pas contenir de caractères de barre oblique inverse, d’astérisque ou de point d’interrogation, de caractère de barre oblique, de signe supérieur ou inférieur \* | &lt; &gt; /ou: caractères.).

**Astuce:** Pour tester une chaîne par rapport à cette expression régulière, utilisez une fenêtre de commande PowerShell et remplacez le nom de votre exécutable par **YourFileName**:

`"YourFileName.exe" -match  "[\\\?\*\|<>/:]+"`

La valeur **true** indique que la chaîne contient des caractères non valides. Voici quelques exemples de valeurs non valides:

-   \\\\server\\share\\program.exe

-   Programme \ *. exe

-   Pro? ram.exe

-   Programme &lt; 1 &gt; . exe

**Remarques**  Le générateur UE-V encode les caractères supérieur et inférieur, comme &gt; et &lt; respectivement.

 

Dans de rares cas, la valeur FileName n’inclura pas nécessairement l’extension. exe, mais elle doit être spécifiée dans le cadre de la valeur. Par exemple, `<Filename>MyApplictication.exe</Filename>` doit être spécifié au lieu de `<Filename>MyApplictication</Filename>` . Le second exemple n’applique pas le modèle au processus si le véritable nom du fichier exécutable est «MyApplication.exe».

### Architecture

**Obligatoire: faux**

**Type: architecture (chaîne)**

Architecture fait référence à l’architecture de processeur pour laquelle l’exécutable cible a été compilé. Les valeurs valides sont Win32 pour les applications 32 bits ou Win64 pour les applications 64 bits. Le cas échéant, cette balise limite l’applicabilité du modèle d’emplacement des paramètres à une architecture d’application particulière. Pour obtenir un exemple, comparez l’utilisation de l’interface utilisateur%ProgramFiles%\\Microsoft MicrosoftOffice2010Win32.xml Virtualization\\templates\\ MicrosoftOffice2010Win64.xml et les fichiers inclus avec UE-V. Cette fonctionnalité est utile lorsque des chemins relatifs changent entre différentes versions d’un fichier exécutable ou si des paramètres ont été ajoutés ou supprimés lors du passage d’une architecture de processeur à une autre.

Si cet élément est absent, le modèle d’emplacement des paramètres ignore l’architecture du processus et s’applique aux processus 32 et 64 bits en cas d’application du nom de fichier et d’autres attributs.

**Remarques**  UE-V ne prend pas en charge les processeurs ARM dans cette version.

 

### ProductName

**Obligatoire: faux**

**Type: chaîne**

ProductName est un élément facultatif utilisé pour identifier un produit à des fins d’administration ou de création de rapports. ProductName est différent du nom de fichier, car il n’y a pas de restrictions d’expression régulières sur sa valeur. Cela permet d’obtenir des descriptions plus faciles à comprendre du processus pour lequel le nom exécutable n’est pas évident. Exemple:

```xml
<Process>
  <Filename>MyApplication.exe</Filename>
  <ProductName>My Application 6.x by Contoso.com</ProductName>
  <ProductVersion>
    <Major Minimum="6" Maximum="6" />
  </ProductVersion>
</Process>
```

### FileDescription

**Obligatoire: faux**

**Type: chaîne**

FileDescription est une balise facultative qui permet d’obtenir une description administrative du fichier exécutable. Il s’agit d’un champ de texte libre qui peut être utile dans le cas d’un package logiciel permettant d’identifier la fonction du fichier exécutable.

Par exemple, dans une application adaptée, il peut être utile de fournir des rappels sur la fonction de deux exécutables (MyApplication.exe et MyApplicationHelper.exe), comme illustré ci-dessous:

```xml
<Processes>
  <Process>
    <Filename>MyApplication.exe</Filename>
    <FileDescription>My Application Main Engine</ FileDescription>
    <ProductVersion>
      <Major Minimum="6" Maximum="6" />
    </ProductVersion>
  </Process>
  <Process>
    <Filename>MyApplicationHelper.exe</Filename>
    <FileDescription>My Application Background Process Executable</FileDescription>
    <ProductVersion>
      <Major Minimum="6" Maximum="6" />
    </ProductVersion>
  </Process>
</Processes>
```

### ProductVersion

**Obligatoire: faux**

**Type: chaîne**

ProductVersion fait référence aux versions de produit principales et secondaires d’un fichier, ainsi qu’à un niveau de build et de correctif. ProductVersion est un élément facultatif, mais si ce paramètre est spécifié, il doit contenir au moins l’élément enfant principal. La valeur doit exprimer une plage au format minimum = «X» maximum = «Y» où X et Y sont des entiers. Les valeurs minimales et maximales peuvent être identiques.

Le produit et les éléments de version du fichier ne sont pas spécifiés. Cela rend le modèle «version agnostique», ce qui signifie que le modèle s’appliquera à toutes les versions du fichier exécutable spécifié.

**Exemple1:**

Version du produit: 1,0 spécifiée dans UE-V Generator génère le code XML suivant:

```xml
<ProductVersion>
  <Major Minimum="1" Maximum="1" />
  <Minor Minimum="0" Maximum="0" />
</ProductVersion>
```

**Exemple2:**

Version du fichier: 5.0.2.1000 spécifiée dans UE-V Generator génère le code XML suivant:

```xml
<FileVersion>
  <Major Minimum="5" Maximum="5" />
  <Minor Minimum="0" Maximum="0" />
  <Build Minimum="2" Maximum="2" />
  <Patch Minimum="1000" Maximum="1000" />
</FileVersion>
```

**Exemple incorrect 1 – plage incomplète:**

Seul l’attribut minimum est présent. La valeur maximale doit également être incluse dans une plage.

```xml
<ProductVersion>
  <Major Minimum="2" />
</ProductVersion>
```

**Exemple 2 incorrect: Minor spécifié sans élément principal:**

Seuls les éléments mineurs sont présents. Important doit également être inclus.

```xml
<ProductVersion>
  <Minor Minimum="0" Maximum="0" />
</ProductVersion>
```

### FileVersion

**Obligatoire: faux**

**Type: chaîne**

FileVersion fait la distinction entre la version commerciale d’une application publiée et les détails de la build interne d’un composant exécutable. Ces numéros sont identiques pour la plupart des applications commerciales. Le cas échéant, la version de produit d’un fichier indique une identification de version générique d’un fichier, tandis que la version du fichier indique une version spécifique d’un fichier (comme dans le cas d’un correctif ou d’une mise à jour). Cela identifie de façon unique les fichiers sans logique de détection de rupture.

Pour déterminer la version et la version du produit d’un fichier exécutable particulier, cliquez avec le bouton droit sur le fichier dans l’Explorateur Windows, sélectionnez Propriétés, puis cliquez sur l’onglet Détails.

L’inclusion d’un élément FileVersion pour une application permet d’améliorer la logique de détection, mais n’est pas nécessaire pour la plupart des applications. Les paramètres de l’élément ProductVersion sont vérifiés en premier, puis FileVersion est activé. Le paramètre le plus restrictif s’applique.

Les éléments enfants et les règles de syntaxe pour FileVersion sont identiques à ceux de ProductVersion.

```xml
<Process>
  <Filename>MSACCESS.EXE</Filename>
  <Architecture>Win32</Architecture>
  <ProductVersion>
    <Major Minimum="14" Maximum="14" />
    <Minor Minimum="0" Maximum="0" />
  </ProductVersion>
  <FileVersion>
    <Major Minimum="14" Maximum="14" />
    <Minor Minimum="0" Maximum="0" />
  </FileVersion>
</Process>
```

### <a href="" id="application"></a>Élément application

Application est un conteneur pour les paramètres qui s’appliquent à une application particulière. Il s’agit d’un ensemble de champs/types suivants.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Champ/type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Name</p></td>
<td align="left"><p>Spécifie un nom unique pour le modèle d’emplacement des paramètres. Il est utilisé à des fins d’affichage lors du référencement du modèle dans WMI, PowerShell, Observateur d’événements et journaux de débogage. Pour plus d’informations, reportez-vous à la section <a href="#name" data-raw-source="[Name](#name)"> nom </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>ID</p></td>
<td align="left"><p>Remplit un identificateur unique pour un modèle particulier. Cette balise devient l’identificateur principal utilisé par l’agent UE-V pour référencer le modèle lors de l’exécution. Pour plus d’informations, consultez la section <a href="#id" data-raw-source="[ID](#id)"> ID </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Description</p></td>
<td align="left"><p>Description facultative du modèle.</p></td>
</tr>
<tr class="even">
<td align="left"><p>LocalizedNames</p></td>
<td align="left"><p>Nom facultatif affiché dans l’interface utilisateur, localisé par des paramètres régionaux de langue.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>LocalizedDescriptions</p></td>
<td align="left"><p>Description de modèle facultative localisée par un paramètre régional de langue.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Version</p></td>
<td align="left"><p>Identifie la version du modèle d’emplacement des paramètres du suivi des modifications. Pour plus d’informations, voir <a href="#version" data-raw-source="[Version](#version)"> version </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>DeferToMSAccount</p></td>
<td align="left"><p>Détermine si ce modèle est activé en conjonction avec un compte Microsoft. Si la synchronisation MSA est activée pour un utilisateur sur un ordinateur, ce modèle sera automatiquement désactivé.</p></td>
</tr>
<tr class="even">
<td align="left"><p>DeferToOffice365</p></td>
<td align="left"><p>Comme pour MSA, cette option détermine si ce modèle est activé en conjonction avec Office 365. Si Office 365 est utilisé pour synchroniser les paramètres, ce modèle sera automatiquement désactivé.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Processus</p></td>
<td align="left"><p>Conteneur pour une collection d’un ou de plusieurs éléments de processus. Pour plus d’informations, reportez-vous à la section <a href="#processes" data-raw-source="[Processes](#processes)"> processus </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Paramètres</p></td>
<td align="left"><p>Conteneur de tous les paramètres qui s’appliquent à un modèle spécifique. Il contient des instances des paramètres de Registre, de fichier, de SystemParameter et de CustomAction. Pour plus d’informations, consultez la section <strong> paramètres </strong> des <a href="#data" data-raw-source="[Data types](#data)"> types de données </a> .</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="common"></a>Élément commun

Common est semblable à un élément application, mais il est toujours associé à deux éléments d’application ou davantage. La section commune représente l’ensemble des paramètres qui sont partagés entre ces instances d’application. Il s’agit d’un ensemble de champs/types suivants.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Champ/type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Name</p></td>
<td align="left"><p>Spécifie un nom unique pour le modèle d’emplacement des paramètres. Il est utilisé à des fins d’affichage lors du référencement du modèle dans WMI, PowerShell, Observateur d’événements et journaux de débogage. Pour plus d’informations, reportez-vous à la section <a href="#name" data-raw-source="[Name](#name)"> nom </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>ID</p></td>
<td align="left"><p>Remplit un identificateur unique pour un modèle particulier. Cette balise devient l’identificateur principal utilisé par l’agent UE-V pour référencer le modèle lors de l’exécution. Pour plus d’informations, consultez la section <a href="#id" data-raw-source="[ID](#id)"> ID </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Description</p></td>
<td align="left"><p>Description facultative du modèle.</p></td>
</tr>
<tr class="even">
<td align="left"><p>LocalizedNames</p></td>
<td align="left"><p>Nom facultatif affiché dans l’interface utilisateur, localisé par des paramètres régionaux de langue.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>LocalizedDescriptions</p></td>
<td align="left"><p>Description de modèle facultative localisée par un paramètre régional de langue.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Version</p></td>
<td align="left"><p>Identifie la version du modèle d’emplacement des paramètres du suivi des modifications. Pour plus d’informations, voir <a href="#version" data-raw-source="[Version](#version)"> version </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>DeferToMSAccount</p></td>
<td align="left"><p>Détermine si ce modèle est activé en conjonction avec un compte Microsoft. Si la synchronisation MSA est activée pour un utilisateur sur un ordinateur, ce modèle sera automatiquement désactivé.</p></td>
</tr>
<tr class="even">
<td align="left"><p>DeferToOffice365</p></td>
<td align="left"><p>Comme pour MSA, cette option détermine si ce modèle est activé en conjonction avec Office 365. Si Office 365 est utilisé pour synchroniser les paramètres, ce modèle sera automatiquement désactivé.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Paramètres</p></td>
<td align="left"><p>Conteneur de tous les paramètres qui s’appliquent à un modèle spécifique. Il contient des instances des paramètres de Registre, de fichier, de SystemParameter et de CustomAction. Pour plus d’informations, consultez la section <strong> paramètres </strong> des <a href="#data" data-raw-source="[Data types](#data)"> types de données </a> .</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="settingslocationtemplate"></a>Élément SettingsLocationTemplate

Cet élément définit les paramètres d’une application unique ou d’une suite d’applications.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Champ/type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Name</p></td>
<td align="left"><p>Spécifie un nom unique pour le modèle d’emplacement des paramètres. Il est utilisé à des fins d’affichage lors du référencement du modèle dans WMI, PowerShell, Observateur d’événements et journaux de débogage. Pour plus d’informations, reportez-vous à la section <a href="#name" data-raw-source="[Name](#name)"> nom </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>ID</p></td>
<td align="left"><p>Remplit un identificateur unique pour un modèle particulier. Cette balise devient l’identificateur principal utilisé par l’agent UE-V pour référencer le modèle lors de l’exécution. Pour plus d’informations, consultez la section <a href="#id" data-raw-source="[ID](#id)"> ID </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Description</p></td>
<td align="left"><p>Description facultative du modèle.</p></td>
</tr>
<tr class="even">
<td align="left"><p>LocalizedNames</p></td>
<td align="left"><p>Nom facultatif affiché dans l’interface utilisateur, localisé par des paramètres régionaux de langue.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>LocalizedDescriptions</p></td>
<td align="left"><p>Description de modèle facultative localisée par un paramètre régional de langue.</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="appendix"></a>Annexe: SettingsLocationTemplate. xsd

Voici le fichier SettingsLocationTemplate. xsd montrant ses éléments, éléments enfants, attributs et paramètres:

```xml
<?xml version="1.0" encoding="utf-8"?>
<xs:schema id="UevSettingsLocationTemplate"
  targetNamespace="https://schemas.microsoft.com/UserExperienceVirtualization/2013/SettingsLocationTemplate"
  elementFormDefault="qualified"
  xmlns="https://schemas.microsoft.com/UserExperienceVirtualization/2013/SettingsLocationTemplate"
  xmlns:mstns="https://schemas.microsoft.com/UserExperienceVirtualization/2013/SettingsLocationTemplate"
  xmlns:xs="http://www.w3.org/2001/XMLSchema">

  <xs:simpleType name="Guid">
    <xs:restriction base="xs:string">
      <xs:pattern value="\{[a-fA-F0-9]{8}-[a-fA-F0-9]{4}-[a-fA-F0-9]{4}-[a-fA-F0-9]{4}-[a-fA-F0-9]{12}\}" />
    </xs:restriction>
  </xs:simpleType>

  <xs:simpleType name="FilenameString">
    <xs:restriction base="xs:string">
      <xs:pattern value="[^\\\?\*\|&lt;&gt;/:]+" />
    </xs:restriction>
  </xs:simpleType>

  <xs:simpleType name="IDString">
    <xs:restriction base="xs:string">
      <xs:pattern value="[^\\\?\*\|&lt;&gt;/:.]+" />
    </xs:restriction>
  </xs:simpleType>

  <xs:simpleType name="TemplateVersion">
    <xs:restriction base="xs:integer">
      <xs:minInclusive value="0" />
      <xs:maxInclusive value="2147483647" />
    </xs:restriction>
  </xs:simpleType>

  <xs:complexType name="Empty">
    <xs:sequence/>
  </xs:complexType>

  <xs:complexType name="LocalizedString">
    <xs:simpleContent>
      <xs:extension base="xs:string">
        <xs:attribute name="Locale" type="xs:string" use="required"/>
      </xs:extension>
    </xs:simpleContent>
  </xs:complexType>

  <xs:complexType name="LocalizedName">
    <xs:sequence>
      <xs:element name="Name" type="LocalizedString" minOccurs="1" maxOccurs="unbounded" />
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="LocalizedDescription">
    <xs:sequence>
      <xs:element name="Description" type="LocalizedString" minOccurs="1" maxOccurs="unbounded" />
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="Author">
    <xs:all>
      <xs:element name="Name" type="xs:string" minOccurs="1" />
      <xs:element name="Email" type="xs:string" minOccurs="0" />
    </xs:all>
  </xs:complexType>

  <xs:complexType name="Range">
    <xs:attribute name="Minimum" type="xs:integer" use="required"/>
    <xs:attribute name="Maximum" type="xs:integer" use="required"/>
  </xs:complexType>

  <xs:complexType name="ProcessVersion">
    <xs:sequence>
      <xs:element name="Major" type="Range" minOccurs="1" />
      <xs:element name="Minor" type="Range" minOccurs="0" />
      <xs:element name="Build" type="Range" minOccurs="0" />
      <xs:element name="Patch" type="Range" minOccurs="0" />
    </xs:sequence>
  </xs:complexType>

  <xs:simpleType name="Architecture">
    <xs:restriction base="xs:string">
      <xs:enumeration value="Win32"/>
      <xs:enumeration value="Win64"/>
    </xs:restriction>
  </xs:simpleType>

  <xs:complexType name="Process">
    <xs:sequence>
      <xs:element name="Filename" type="FilenameString" minOccurs="1" />
      <xs:element name="Architecture" type="Architecture" minOccurs="0" />
      <xs:element name="ProductName" type="xs:string" minOccurs="0" />
      <xs:element name="FileDescription" type="xs:string" minOccurs="0" />
      <xs:element name="ProductVersion" type="ProcessVersion" minOccurs="0" maxOccurs="unbounded"/>
      <xs:element name="FileVersion" type="ProcessVersion" minOccurs="0" maxOccurs="unbounded"/>
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="Processes">
    <xs:sequence>
      <xs:choice minOccurs="1">
        <xs:element name="Process" type="Process" />
        <xs:element name="ShellProcess" type="Empty" />
      </xs:choice>
      <xs:element name="Process" type="Process" minOccurs="0" maxOccurs="unbounded" />
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="Path">
    <xs:simpleContent>
      <xs:extension base="xs:string">
        <xs:attribute name="Recursive" type="xs:boolean" default="false"/>
        <xs:attribute name="DeleteIfNotFound" type="xs:boolean" default="false"/>
      </xs:extension>
    </xs:simpleContent>
  </xs:complexType>

  <xs:complexType name="RegistrySetting">
    <xs:sequence>
      <xs:element name="Path" type="Path" />
      <xs:element name="Name" type="xs:string" minOccurs="0" maxOccurs="unbounded" />
      <xs:element name="Exclude" minOccurs="0" maxOccurs="unbounded">
        <xs:complexType>
          <xs:sequence>
            <xs:element name="Path" type="Path" minOccurs="0" />
            <xs:element name="Name" type="xs:string" minOccurs="0" maxOccurs="unbounded" />
          </xs:sequence>
        </xs:complexType>
      </xs:element>
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="FileSetting">
    <xs:sequence>

      <xs:element name="Root">
        <xs:complexType>
          <xs:choice>
            <xs:element name="KnownFolder" type="Guid" />
            <xs:element name="RegistryEntry" type="xs:string" />
            <xs:element name="EnvironmentVariable" type="xs:string" />
          </xs:choice>
        </xs:complexType>
      </xs:element>

      <xs:element name="Path" minOccurs="0" type="Path" />
      <xs:element name="FileMask" type="xs:string" minOccurs="0" maxOccurs="unbounded"/>

      <xs:element name="Exclude" minOccurs="0" maxOccurs="unbounded">
        <xs:complexType>
          <xs:sequence>
            <xs:element name="Path" type="Path" minOccurs="0" />
            <xs:element name="FileMask" type="xs:string" minOccurs="0" maxOccurs="unbounded" />
          </xs:sequence>
        </xs:complexType>
      </xs:element>

    </xs:sequence>
  </xs:complexType>

  <xs:simpleType name="SystemParameterSetting">
    <xs:restriction base="xs:string">

      <!-- Accessibility parameters -->
      <xs:enumeration value="AccessTimeout"/>
      <xs:enumeration value="AudioDescription"/>
      <xs:enumeration value="ClientAreaAnimation"/>
      <xs:enumeration value="DisableOverlappedContent"/>
      <xs:enumeration value="FilterKeys"/>
      <xs:enumeration value="FocusBorderHeight"/>
      <xs:enumeration value="FocusBorderWidth"/>
      <xs:enumeration value="HighContrast"/>
      <xs:enumeration value="MessageDuration"/>
      <xs:enumeration value="MouseClickLock"/>
      <xs:enumeration value="MouseClickLockTime"/>
      <xs:enumeration value="MouseKeys"/>
      <xs:enumeration value="MouseSonar"/>
      <xs:enumeration value="MouseVanish"/>
      <xs:enumeration value="ScreenReader"/>
      <xs:enumeration value="ShowSounds"/>
      <xs:enumeration value="SoundSentry"/>
      <xs:enumeration value="StickyKeys"/>
      <xs:enumeration value="ToggleKeys"/>

      <!-- Input parameters -->
      <xs:enumeration value="Beep"/>
      <xs:enumeration value="BlockSendInputResets"/>
      <xs:enumeration value="DefaultInputLang"/>
      <xs:enumeration value="DoubleClickTime"/>
      <xs:enumeration value="DoubleClkHeight"/>
      <xs:enumeration value="DoubleClkWidth"/>
      <xs:enumeration value="KeyboardCues"/>
      <xs:enumeration value="KeyboardDelay"/>
      <xs:enumeration value="KeyboardPref"/>
      <xs:enumeration value="KeyboardSpeed"/>
      <xs:enumeration value="Mouse"/>
      <xs:enumeration value="MouseButtonSwap"/>
      <xs:enumeration value="MouseHoverHeight"/>
      <xs:enumeration value="MouseHoverTime"/>
      <xs:enumeration value="MouseHoverWidth"/>
      <xs:enumeration value="MouseSpeed"/>
      <xs:enumeration value="MouseTrails"/>
      <xs:enumeration value="SnapToDefButton"/>
      <xs:enumeration value="WheelScrollChars"/>
      <xs:enumeration value="WheelScrollLines"/>

      <!-- Desktop parameters (limited subset) -->
      <xs:enumeration value="DeskWallpaper"/>
      <xs:enumeration value="DesktopColor"/>

    </xs:restriction>
  </xs:simpleType>

  <xs:complexType name="Settings">
    <xs:sequence>
      <xs:element name="Asynchronous" type="xs:boolean" minOccurs="0" />
      <xs:element name="PreventOverlappingSynchronization" type="xs:boolean" minOccurs="0" />
      <xs:choice minOccurs="0" maxOccurs="unbounded">
        <xs:element name="Registry" type="RegistrySetting" />
        <xs:element name="File" type="FileSetting" />
        <xs:element name="SystemParameter" type="SystemParameterSetting" />
      </xs:choice>
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="Common">
    <xs:sequence>
      <xs:element name="Name" type="xs:string" />
      <xs:element name="ID" type="IDString" />
      <xs:element name="Description" type="xs:string" minOccurs="0" />
      <xs:element name="LocalizedNames" type="LocalizedName" minOccurs="0" />
      <xs:element name="LocalizedDescriptions" type="LocalizedDescription" minOccurs="0" />
      <xs:element name="Version" type="xs:integer" />
      <xs:element name="DeferToMSAccount" type="Empty"  minOccurs="0" />
      <xs:element name="Settings" type="Settings" />
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="Application">
    <xs:sequence>
      <xs:element name="Name" type="xs:string" />
      <xs:element name="ID" type="IDString" />
      <xs:element name="Description" type="xs:string" minOccurs="0" />
      <xs:element name="LocalizedNames" type="LocalizedName" minOccurs="0" />
      <xs:element name="LocalizedDescriptions" type="LocalizedDescription" minOccurs="0" />
      <xs:element name="Version" type="xs:integer" />
      <xs:element name="DeferToMSAccount" type="Empty"  minOccurs="0" />
      <xs:element name="Processes" type="Processes" />
      <xs:element name="Settings" type="Settings" />
    </xs:sequence>
  </xs:complexType>


  <xs:element name="SettingsLocationTemplate">
    <xs:complexType>
      <xs:sequence>

        <xs:element name="Name" type="xs:string" />
        <xs:element name="ID" type="IDString" />
        <xs:element name="Description" type="xs:string" minOccurs="0" />
        <xs:element name="LocalizedNames" type="LocalizedName" minOccurs="0" />
        <xs:element name="LocalizedDescriptions" type="LocalizedDescription" minOccurs="0" />

        <xs:choice>

          <!-- Single application -->
          <xs:sequence>
            <xs:element name="Version" type="TemplateVersion" />
            <xs:element name="Author" type="Author" minOccurs="0" />
            <xs:element name="DeferToMSAccount" type="Empty"  minOccurs="0" />
            <xs:element name="Processes" type="Processes" />
            <xs:element name="Settings" type="Settings" />
          </xs:sequence>

          <!-- Suite of applications -->
          <xs:sequence>
            <xs:element name="ManageSuiteOnly" type="xs:boolean" minOccurs="0" />
            <xs:element name="Author" type="Author" minOccurs="0" />
            <xs:element name="Common" type="Common" />
            <xs:element name="Application" type="Application" minOccurs="2" maxOccurs="unbounded" />
          </xs:sequence>

        </xs:choice>

      </xs:sequence>
    </xs:complexType>
  </xs:element>
  <!-- SettingsLocationTemplate -->

</xs:schema>
```






## Rubriques connexes


[Utilisation de modèles UE-V 2 ou x personnalisés et du générateur UE-V 2. x](working-with-custom-ue-v-2x-templates-and-the-ue-v-2x-generator-new-uevv2.md)

[Informations techniques de référence sur UE-V2.x](technical-reference-for-ue-v-2x-both-uevv2.md)

 

 





