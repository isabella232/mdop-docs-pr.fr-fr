---
title: Configurations prises en charge par MED-V2.0
description: Configurations prises en charge par MED-V2.0
author: dansimp
ms.assetid: 88f1d232-aa01-45ab-8da7-d086269250b5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0fed090ec04cf67a32b13533f4003c01ae167493
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811022"
---
# Configurations prises en charge par MED-V2.0


Votre environnement peut déjà respecter les exigences de configuration fournies ici pour pouvoir installer et exécuter Microsoft Enterprise Desktop Virtualization (MED-V) 2,0. Nous avons inclus une configuration requise incluant le système d’exploitation hôte, l’espace disque et les exigences en matière d’espace de travail MED-V.

## Configuration requise pour l’ordinateur hôte MED-V 2.0


### Configuration requise pour le système d’exploitation MED-V 2,0

Le tableau suivant répertorie les systèmes d’exploitation pris en charge pour l’installation de MED-V 2,0 sur l’ordinateur hôte.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Systèmed’exploitation</th>
<th align="left">Édition</th>
<th align="left">Service Pack</th>
<th align="left">Architecture système</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Plus de.</p></td>
<td align="left"><p>Professionnel, entreprise ou édition intégrale</p></td>
<td align="left"><p>Aucun ou SP1</p></td>
<td align="left"><p>x86 ou x64</p></td>
</tr>
</tbody>
</table>

 

Le tableau suivant répertorie la RAM minimale requise pour chaque système d’exploitation pris en charge dans MED-V 2,0.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Systèmed’exploitation</th>
<th align="left">RAM minimum requise</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Dans le x86</p></td>
<td align="left"><p>2Go</p></td>
</tr>
<tr class="even">
<td align="left"><p>X86</p></td>
<td align="left"><p>2Go</p></td>
</tr>
</tbody>
</table>

 

### Espace disque minimal recommandé

Nous vous recommandons d’utiliser un minimum de 10 Go de stockage disponible. Toutefois, l’espace disque requis varie considérablement et dépend du nombre d’applications publiées dans l’espace de travail MED-V.

### <a href="" id="med-v-2-0-host-configuration-"></a>Configuration d’hôte MED-V 2.0

**Version du .NET Framework**

La version .NET Framework 3.5 SP1 de Microsoft .NET Framework est requise pour MED-V 2,0. Toutefois, vous pouvez installer .NET Framework 4 ou version ultérieure si .NET Framework 3,5 est déjà installé.

**Moteur de virtualisation**

PCwith virtuel Windows le correctif décrit dans l’article 977206 de la base de connaissances Microsoft est pris en charge pour MED-V 2,0.

**Navigateur Internet**

Windows Internet Explorer8 et Windows Internet Explorer 9 sont pris en charge pour MED-V 2,0.

**Environnements Microsoft Server**

L’agent hôte MED-V et le package de l’espace de travail MED-V ne sont pas pris en charge dans les environnements serveur.

## Configuration requise pour les espaces de travail MED-V 2.0


### Configuration requise pour le système d’exploitation MED-V 2,0

Le tableau suivant répertorie les systèmes d’exploitation pris en charge pour les espaces de travail MED-V 2,0.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Systèmed’exploitation</th>
<th align="left">Édition</th>
<th align="left">Service Pack</th>
<th align="left">Architecture système</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>WindowsXP</p></td>
<td align="left"><p>Edition professionnelle</p></td>
<td align="left"><p>3</p></td>
<td align="left"><p>x86</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="med-v-2-0-workspace-configuration-"></a>Configuration de l’espace de travail MED-V 2.0

**Version du .NET Framework**

Seule la version .NET Framework 3.5 SP1 de Microsoft .NET Framework est prise en charge pour l’installation de l’espace de travail MED-V 2,0.

**Navigateur Internet**

Windows Internet Explorer6, Windows Internet Explorer7, Windows Internet Explorer8 et Windows Internet Explorer9 sont pris en charge pour l’installation de l’espace de travail 2,0 de MED-V.

### Création d’espace de travail MED-V 2,0

Le disque dur virtuel utilisé pour créer un package d’espace de travail 2,0 pour MED-V doit être créé à l’aide du PC virtuel Windows.

## Informations de globalisation MED-V 2,0


### Informations de globalisation de l’agent hôte MED-V 2,0

Les versions de langue du système d’exploitation Windows suivantes sont prises en charge pour l’agent hôte MED-V 2,0:

-   Français

-   Italien

-   Allemand

-   Espagnol

-   Coréen

-   Japonais

-   Portugais (Brésil)

-   Russe

-   Chinois (traditionnel)

-   Chinois simplifié

-   Néerlandais

-   Suédois

-   Danois

-   Finnois

-   Portugais

-   Norvégien

-   Polonais

-   Turc

-   Hongrois

-   Tchèque

-   Grec

-   Slovaque

-   Slovène

### Informations de globalisation du package d’espace de travail MED-V 2,0

Les versions suivantes du système d’exploitation Windows sont prises en charge pour le gestionnaire de package d’espace de travail MED-V 2,0:

-   Français

-   Italien

-   Allemand

-   Espagnol

-   Coréen

-   Japonais

-   Portugais (Brésil)

-   Russe

-   Chinois (traditionnel)

-   Chinois simplifié

## Rubriques connexes


[Déploiement de MED-V](deployment-of-med-v.md)

 

 





