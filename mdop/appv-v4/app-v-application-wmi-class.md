---
title: Classe WMI de l'application App-V
description: Classe WMI de l'application App-V
author: dansimp
ms.assetid: b79b0d5a-ba57-442f-8bb4-d7154fc056f9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a4e1e49e35b231ddb2a480a06c46e364121ac2d2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809287"
---
# Classe WMI de l'application App-V


Dans le client Application Virtualization (App-V), la classe **application** est une classe WMI (Windows Management Instrumentation) qui représente toutes les applications virtuelles sur le client.

La syntaxe suivante est simplifiée du code MOF (Managed Object Format). Le code inclut toutes les propriétés héritées.

## Syntaxe


``` syntax
class Application
{
      string Name;
      string Version;
      string PackageGUID;
      datetime LastLaunchOnSystem;
      uint32 GlobalRunningCount;
      boolean Loading;
      string OriginalOsdPath;
      string CachedOsdPath;
};
```

## Configuration requise


## Propriétés


<a href="" id="name"></a>**Nom**  
Type de données: **chaîne**

Type d’accès: lecture seule

Qualificateurs: clé

Nom d’affichage de l’application virtuelle.

<a href="" id="version"></a>**Version**  
Type de données: **chaîne**

Type d’accès: lecture seule

Qualificateurs: clé

Version de l’application virtuelle.

<a href="" id="packageguid"></a>**PackageGUID**  
Type de données: **chaîne**

Type d’accès: lecture seule

Qualificateurs: aucun

GUID du package auquel l’application virtuelle est associée.

<a href="" id="lastlaunchonsystem"></a>**LastLaunchOnSystem**  
Type de données: **DateTime**

Type d’accès: lecture seule

Qualificateurs: aucun

La date et l’heure auxquelles l’application virtuelle a été lancée pour la dernière fois.

<a href="" id="globalrunningcount"></a>**GlobalRunningCount**  
Type de données: **UInt32**

Type d’accès: lecture seule

Qualificateurs: aucun

Nombre d’instances en cours d’exécution de l’application virtuelle démarrées directement.

<a href="" id="loading"></a>**Chargement**  
Type de données: **booléen**

Type d’accès: lecture seule

Qualificateurs: aucun

**true** si l’application virtuelle est en cours de démarrage; Sinon, **false**.

<a href="" id="originalosdpath"></a>**OriginalOsdPath**  
Type de données: **chaîne**

Type d’accès: lecture seule

Qualificateurs: aucun

Le chemin d’accès au fichier d’OSD enregistré dans le client App-V.

<a href="" id="cachedosdpath"></a>**CachedOsdPath**  
Type de données: **chaîne**

Type d’accès: lecture seule

Qualificateurs: aucun

Le chemin d’accès du fichier OSD si le client App-V a mis en cache le fichier OSD en local.

 

 





