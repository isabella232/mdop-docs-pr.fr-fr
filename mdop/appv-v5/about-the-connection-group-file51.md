---
title: À propos du fichier de groupe de connexion
description: À propos du fichier de groupe de connexion
author: dansimp
ms.assetid: 1f4df515-f5f6-4b58-91a8-c71598cb3ea4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 31ef9dc9c4465ed8f261b73518348c05ceb78d15
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806096"
---
# À propos du fichier de groupe de connexion


**Contenu de cet article:**

-   [Objectif et emplacement du fichier de groupe de connexion](#bkmk-cg-purpose-loc)

-   [Structure du fichier XML de groupe de connexion](#bkmk-define-cg-5-0sp3)

-   [Configuration de la priorité des packages dans un groupe de connexion](#bkmk-config-pkg-priority-incg)

-   [Configurations de connexion d’applications virtuelles prises en charge](#bkmk-va-conn-configs)

## <a href="" id="bkmk-cg-purpose-loc"></a>Objectif et emplacement du fichier de groupe de connexion


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>Fonction de groupe de connexion</p></td>
<td align="left"><p>Un groupe de connexions est une fonctionnalité App-V qui vous permet de regrouper les packages pour créer un environnement virtuel dans lequel les applications de ces packages peuvent interagir entre elles.</p>
<p>Par exemple: vous voulez utiliser les plug-ins avec Microsoft Office. Vous pouvez créer un package qui contient les plug-ins et créer un autre package contenant Office, puis ajouter ces deux packages à un groupe de connexion pour permettre à Office d’utiliser ces plug-ins.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Fonctionnement du fichier de groupe de connexion</p></td>
<td align="left"><p>Lorsque vous appliquez un fichier de groupe de connexion App-V 5,1, les packages énumérés dans le fichier seront combinés au moment de l’exécution dans un environnement virtuel unique. Servez-vous du fichier de groupe de connexion 5,1 App-V) pour configurer des groupes de connexion App-V 5,1 existants.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Exemple de chemin d’accès au fichier</p></td>
<td align="left"><p>%APPDATA%\Microsoft\AppV\Client\Catalog\PackageGroups {6CCC7575-162E-4152-9407-ED411DA138F4} {4D1E16E1-8EF8-41ED-92D5-8910A8527F96}.</p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-define-cg-5-0sp3"></a>Structure du fichier XML de groupe de connexion


**Dans cette section:**

-   [Paramètres définissant le groupe de connexions](#bkmk-params-define-cg)

-   [Paramètres définissant les packages dans le groupe de connexion](#bkmk-params-define-pkgs-incg)

-   [Exemple de fichier XML de groupe de connexion App-V](#bkmk-50sp3-exp-cg-xml)

-   [App-V 5,0 via App-V 5,0 SP2-exemple de fichier XML de connexion](#bkmk-50thru50sp2-exp-cg-xm)

### <a href="" id="bkmk-params-define-cg"></a>Paramètres définissant le groupe de connexions

Le tableau suivant décrit les paramètres du fichier XML qui définissent le groupe de connexions lui-même, et non les packages.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Champ</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Nom du schéma</p></td>
<td align="left"><p>Nom du schéma.</p>
<p><strong>Applicable à partir de l’App-V 5,0 SP3 </strong> : Si vous voulez utiliser les nouvelles fonctionnalités «packages facultatifs» et «utiliser les versions» décrites dans ce tableau, vous devez spécifier le schéma suivant dans le fichier XML:</p>
<p><code>xmlns=&quot;<a href="https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup&amp;quot" data-raw-source="https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup&amp;quot">https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup&quot</a>;</code></p></td>
</tr>
<tr class="even">
<td align="left"><p>AppConnectionGroupId</p></td>
<td align="left"><p>Identificateur GUID unique pour ce groupe de connexion. L’état du groupe de connexions est associé à cet identificateur. Spécifiez cet identificateur uniquement lors de la création du groupe de connexions.</p>
<p>Vous pouvez créer un nouveau GUID en tapant: <strong>[Guid]::NewGuid()</strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>VersionId</p></td>
<td align="left"><p>Identificateur du GUID de version de cette version du groupe de connexion.</p>
<p>Lorsque vous mettez à jour un groupe de connexion (par exemple, en ajoutant ou en mettant à jour un nouveau package), vous devez mettre à jour le GUID de la version pour refléter la nouvelle version.</p></td>
</tr>
<tr class="even">
<td align="left"><p>DisplayName</p></td>
<td align="left"><p>Nom d’affichage du groupe de connexions.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Priority</p></td>
<td align="left"><p>Champ prioritaire facultatif pour le groupe de connexions.</p>
<p><strong>"0" </strong> - indique la priorité la plus élevée.</p>
<p>Si une priorité est requise, mais qu’elle n’a pas été configurée, le package échouera, car le groupe de connexion approprié à utiliser ne peut pas être déterminé.</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="bkmk-params-define-pkgs-incg"></a>Paramètres définissant les packages dans le groupe de connexion

Dans la &lt; &gt; section packages du fichier XML de groupe de connexion, vous répertoriez les packages de membres dans le groupe de connexions en spécifiant l’identificateur de package et l’identificateur de version uniques de chaque package, comme décrit dans le tableau suivant. Le premier package de la liste a la priorité la plus élevée.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Champ</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>PackageId</p></td>
<td align="left"><p>Identificateur GUID unique pour ce package. Ce GUID ne change pas lors de la publication de versions plus récentes du package.</p></td>
</tr>
<tr class="even">
<td align="left"><p>VersionId</p></td>
<td align="left"><p>Identificateur GUID unique pour la version du package.</p>
<p><strong>Applicable à partir de l’App-V 5,0 SP3 </strong> : Si vous spécifiez <strong> «*» </strong> pour la version du package, le GUID de la dernière version du package disponible est inséré dynamiquement.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>IsOptional</p></td>
<td align="left"><p><strong>Applicable à partir du paramètre App-V 5,0 SP3 </strong> : qui vous permet de rendre un package facultatif dans le groupe de connexions. Les entrées valides sont les suivantes:</p>
<ul>
<li><p><strong>"vrai" </strong> : le package est facultatif dans le groupe de connexions</p></li>
<li><p><strong>"false" </strong> – le package est requis dans le groupe de connexion</p></li>
</ul>
<p>Découvrez <a href="how-to-use-optional-packages-in-connection-groups51.md" data-raw-source="[How to Use Optional Packages in Connection Groups](how-to-use-optional-packages-in-connection-groups51.md)"> comment utiliser les packages facultatifs dans les groupes de connexion </a> .</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="bkmk-50sp3-exp-cg-xml"></a>Exemple de fichier XML de groupe de connexion App-V

L’exemple de fichier XML de groupe de connexion suivant présente des exemples de champs dans les tableaux précédents, et met en surbrillance les éléments qui sont nouveaux à partir de l’App-V 5,0 SP3.

```XML
<?xml version="1.0" encoding="UTF-16">
<appv:AppConnectionGroup 
  xmlns="https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup"
  xmlns:appv="https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup"  
  AppConnectionGroupId="61BE9B14-D2B4-41CE-A6E3-A1B658DE7000"
  VersionId="E6B6AA57-F2A7-49C9-ADF8-F2B5B3C8A42F"
  Priority="0"  
  DisplayName="Sample Connection Group">
  <appv:Packages>    
    <appv:Package
      PackageId="1DC709C8-309F-4AB4-BD47-F75926D04276"
      VersionId="*"
      IsOptional="true"    
    />
    <appv:Package
      PackageId="04220DCA-EE77-42BE-A9F5-96FD8E8593F2"
      VersionId="E15EFFE9-043D-4C01-BC52-AD2BD1E8BAFA"
      IsOptional="false"    
    />  
  </appv:Packages>
</appv:AppConnectionGroup>
```

### <a href="" id="bkmk-50thru50sp2-exp-cg-xm"></a>App-V 5,0 via App-V 5,0 SP2-exemple de fichier XML de connexion

L’exemple de fichier XML de groupe de connexion suivant s’applique à l’application-V 5,0 via App-V 5,0 SP2. Il s’agit de exemples de champs du tableau précédent, mais exclut les changements décrits ci-dessus pour App-V 5,0 SP3.

```XML
<?xml version="1.0" encoding="UTF-16">
<appv:AppConnectionGroup
  xmlns="https://schemas.microsoft.com/appv/2010/virtualapplicationconnectiongroup"
  xmlns:appv="https://schemas.microsoft.com/appv/2010/virtualapplicationconnectiongroup"
  AppConnectionGroupId="61BE9B14-D2B4-41CE-A6E3-A1B658DE7000"
  VersionId="E6B6AA57-F2A7-49C9-ADF8-F2B5B3C8A42F"
  Priority="0"
  DisplayName="Sample Connection Group">
  <appv:Packages>
    <appv:Package
      PackageId="1DC709C8-309F-4AB4-BD47-F75926D04276"
      VersionId="C7DF4F63-5288-439C-ACEF-EF06BF401EC5"
    />
    <appv:Package
     PackageId="04220DCA-EE77-42BE-A9F5-96FD8E8593F2"
     VersionId="E15EFFE9-043D-4C01-BC52-AD2BD1E8BAFA"
   />
 </appv:Packages>
<appv:AppConnectionGroup>
```

## <a href="" id="bkmk-config-pkg-priority-incg"></a>Configuration de la priorité des packages dans un groupe de connexion


La priorité des packages est configurée à l’aide de l’ordre de la liste des packages. Le premier package du document a la priorité la plus élevée. Les packages suivants de la liste ont une priorité décroissante.

La priorité des packages correspond à la résolution des conflits de ressources inévitables lors de l’initialisation de l’environnement virtuel. Par exemple, si deux packages qui s’ouvrent dans le même environnement virtuel définissent la même valeur DWORD de Registre, le package dont la priorité est la plus élevée détermine la valeur définie.

Vous pouvez utiliser le fichier de groupe de connexion pour configurer chaque groupe de connexions en utilisant les méthodes suivantes:

-   Spécifiez les priorités d’exécution des groupes de connexion. Pour modifier la priorité à l’aide de la console de gestion App-V, cliquez sur le groupe de connexions, puis cliquez sur **modifier**.

    **Remarques**  Priority est requis uniquement si le package est associé à plusieurs groupes de connexion.

     

-   Spécifiez l’ordre de priorité des packages dans le groupe de connexions.

Le champ Priority est requis pour une application virtuelle en cours d’exécution à partir d’une demande d’application native, par exemple Microsoft Windows Explorer. Le client App-V utilise la priorité pour déterminer l’environnement virtuel du groupe de connexion dans lequel l’application doit s’exécuter. Cette situation se produit si une application virtuelle fait partie de plusieurs groupes de connexion.

Si une application virtuelle est ouverte à l’aide d’une autre application virtuelle, l’environnement virtuel de l’application virtuelle d’origine est utilisé. Le champ priorité n’est pas utilisé dans le cas présent.

**Exemple :**

L’application virtuelle Microsoft Outlook est en cours d’exécution dans l’environnement virtuel **xyz**. Lorsque vous ouvrez un document Microsoft Word joint, une version virtualisée de Microsoft Word s’ouvre dans l’environnement virtuel **xyz**, quels que soient les groupes de connexions ou les priorités d’exécution qui sont virtualisés de Microsoft Word.

## <a href="" id="bkmk-va-conn-configs"></a>Configurations de connexion d’applications virtuelles prises en charge


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Configuration</th>
<th align="left">Exemple de scénario</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Aucun. fichier exe et plug-in (. dll)</p></td>
<td align="left"><ul>
<li><p>Vous souhaitez distribuer Microsoft Office à tous les utilisateurs, mais distribuer un plug-in Microsoft Excel uniquement à un sous-ensemble d’utilisateurs.</p></li>
<li><p>Activez le groupe de connexion pour les utilisateurs appropriés.</p></li>
<li><p>Mettez à jour chaque package individuellement selon vos besoins.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Aucun. fichier exe et application middleware</p></td>
<td align="left"><ul>
<li><p>Une application nécessite une application middleware ou plusieurs applications dépendent de la même version d’exécution du middleware.</p></li>
<li><p>Tous les ordinateurs qui nécessitent une ou plusieurs de ces applications reçoivent les groupes de connexion avec application et Runtime de l’application middleware.</p></li>
<li><p>Vous pouvez éventuellement combiner plusieurs applications middleware au sein d’un seul groupe de connexion.</p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Exemple</th>
<th align="left">Exemple de description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Groupe de connexion d’application virtuel pour la division financière</p></td>
<td align="left"><ul>
<li><p>Application middleware 1</p></li>
<li><p>Application middleware 2</p></li>
<li><p>Application middleware 3</p></li>
<li><p>Exécution de l’application middleware</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Groupe de connexion d’application virtuelle pour une division de ressources humaines</p></td>
<td align="left"><ul>
<li><p>Application middleware 5</p></li>
<li><p>Application middleware 6</p></li>
<li><p>Exécution de l’application middleware</p></li>
</ul></td>
</tr>
</tbody>
</table>
<p> </p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Aucun. fichier exe et fichier. exe</p></td>
<td align="left"><p>Vous disposez d’une application qui s’appuie sur une autre application, et vous voulez conserver les packages séparés pour l’efficacité opérationnelle, les restrictions de licence ou les chronologies de déploiement.</p>
<p><strong>Exemple :</strong></p>
<p>Si vous déployez Microsoft Lync 2010, vous pouvez utiliser trois packages:</p>
<ul>
<li><p>Microsoft Office 2010</p></li>
<li><p>Microsoft Communicator2007</p></li>
<li><p>Microsoft Lync2010</p></li>
</ul>
<p>Vous pouvez gérer le déploiement à l’aide des groupes de connexion suivants:</p>
<ul>
<li><p>Microsoft Office 2010 et Microsoft Communicator2007</p></li>
<li><p>Microsoft Office 2010 et Microsoft Lync2010</p></li>
</ul>
<p>Lorsque le déploiement s’est terminé, vous pouvez créer un seul compte Microsoft Office 2010 + Microsoft Lync2010, ou le conserver et le conserver en tant que packages distincts et les déployer à l’aide d’un groupe de connexion.</p></td>
</tr>
</tbody>
</table>

 






## Rubriques connexes


[Gestion des groupes de connexion](managing-connection-groups51.md)

 

 





