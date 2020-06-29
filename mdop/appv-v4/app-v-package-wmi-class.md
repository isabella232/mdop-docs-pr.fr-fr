---
title: Classe WMI de package App-V
description: Classe WMI de package App-V
author: dansimp
ms.assetid: 0fc26c3b-9706-4804-be2d-645771dc33ae
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa452afaaeb2f490c179a928b24de47207d6dc63
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808050"
---
# Classe WMI de package App-V


Dans le client Application Virtualization (App-V), la classe de **package** est une classe WMI (Windows Management Instrumentation) qui représente tous les packages virtuels sur le client. Les packages virtuels peuvent contenir plusieurs applications virtuelles.

## Syntaxe


``` syntax
class Package
{
      string Name;
      string Version;
      string PackageGUID;
      string SftPath;
      uint64 TotalSize;
      uint64 CachedSize;
      uint64 LaunchSize;
      uint64 CachedLaunchSize;
      boolean InUse;
      boolean Locked;
      uint16 CachedPercentage;
      string VersionGUID;
 };
```

## Propriétés


<a href="" id="name"></a>**Nom**  
Type de données: **chaîne**

Type d’accès: lecture seule

Qualificateurs: aucun

Nom convivial du package virtuel.

<a href="" id="version"></a>**Version**  
Type de données: **chaîne**

Type d’accès: lecture seule

Qualificateurs: aucun

Version du package virtuel.

<a href="" id="packageguid"></a>**PackageGUID**  
Type de données: **chaîne**

Type d’accès: lecture seule

Qualificateurs: clé

Identificateur GUID de la configuration du package et des fichiers sources.

<a href="" id="sftpath"></a>**SftPath**  
Type de données: **chaîne**

Type d’accès: lecture seule

Qualificateurs: aucun

Le chemin d’accès du fichier SFT.

<a href="" id="totalsize"></a>**TotalSize**  
Type de données: **UInt64**

Type d’accès: lecture seule

Qualificateurs: aucun

Taille totale du package virtuel, en kilo-octets.

<a href="" id="cachedsize"></a>**CachedSize**  
Type de données: **UInt64**

Type d’accès: lecture seule

Qualificateurs: aucun

Taille totale du cache pour le package virtuel, en kilo-octets.

<a href="" id="launchsize"></a>**LaunchSize**  
Type de données: **UInt64**

Type d’accès: lecture seule

Qualificateurs: aucun

Taille totale du bloc de fonctionnalités principal du package virtuel, en kilo-octets.

<a href="" id="cachedlaunchsize"></a>**CachedLaunchSize**  
Type de données: **UInt64**

Type d’accès: lecture seule

Qualificateurs: aucun

Taille totale du bloc de fonctionnalités principal du package virtuel qui a été mis en cache, en kilo-octets.

<a href="" id="inuse"></a>**InUse**  
Type de données: **booléen**

Type d’accès: lecture seule

Qualificateurs: aucun

**true** si une application virtuelle du package virtuel est en cours d’exécution; Sinon, **false**.

<a href="" id="locked"></a>**Verrouillé**  
Type de données: **booléen**

Type d’accès: lecture seule

Qualificateurs: aucun

**true** si le package virtuel est verrouillé; Sinon, **false**.

<a href="" id="cachedpercentage"></a>**CachedPercentage**  
Type de données: **UInt16**

Type d’accès: lecture seule

Qualificateurs: aucun

Pourcentage des fichiers cache. En fonction de la formule suivante: CachedSize/TotalSize × 100.

<a href="" id="versionguid"></a>**VersionGUID**  
Type de données: **chaîne**

Type d’accès: lecture seule

Qualificateurs: aucun

Identificateur GUID de la version du package.

 

 





