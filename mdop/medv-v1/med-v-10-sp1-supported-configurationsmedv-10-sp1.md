---
title: Configurations prises en charge par MED-V1.0 SP1
description: Configurations prises en charge par MED-V1.0 SP1
author: dansimp
ms.assetid: 4dcf37c4-a061-43d2-878c-28efc87c3cdd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 5a707e8a3d59a423308f9f735ff38df9e235fbf5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810392"
---
# Configurations prises en charge par MED-V1.0 SP1


Cette rubrique précise les exigences nécessaires à l’installation et à l’exécution de Microsoft Enterprise Desktop Virtualization (MED-V) 1,0 Service Pack 1 (SP1) dans votre environnement.

## Configuration système requise pour le client MED-V 1,0 SP1


### Configuration requise pour le système d’exploitation MED-V

Le tableau suivant répertorie les systèmes d’exploitation pris en charge pour l’installation du client MED-V 1,0 SP1.

**Remarque**  
Microsoft prend en charge le Service Pack actuel et, dans certains cas, le Service Pack immédiatement précédent. Pour savoir comment accéder aux délais de prise en charge de votre produit, voir les [Service Packs pris en charge](https://go.microsoft.com/fwlink/?LinkId=31975) https://go.microsoft.com/fwlink/?LinkId=31975) . Pour plus d’informations sur la politique de support Microsoft, voir FAQ sur la politique de support [Microsoft](https://go.microsoft.com/fwlink/?LinkId=31976) ( https://go.microsoft.com/fwlink/?LinkId=31976) .



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
<td align="left"><p>Windows XP</p></td>
<td align="left"><p>Edition professionnelle</p></td>
<td align="left"><p>SP2 ou SP3</p></td>
<td align="left"><p>x86</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Vista</p></td>
<td align="left"><p>Professionnel, entreprise ou intégrale</p></td>
<td align="left"><p>SP1 ou SP2</p></td>
<td align="left"><p>x86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows7</p></td>
<td align="left"><p>Professionnel, entreprise ou édition intégrale</p></td>
<td align="left"><p>None</p></td>
<td align="left"><p>x86 ou x64</p></td>
</tr>
</tbody>
</table>



**Remarque**  
Le client MED-V ne s’exécute pas en mode x64 natif. Au lieu de cela, MED-V s’exécute en mode Windows 64 bits (WOW64) sur les ordinateurs 64 bits.



Le tableau suivant répertorie la RAM minimale requise pour chaque système d’exploitation pris en charge dans MED-V 1,0 SP1.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Systèmed’exploitation</th>
<th align="left">RAM minimale requise</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows XP professionnel</p></td>
<td align="left"><p>1 Go</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Vista</p></td>
<td align="left"><p>2 Go</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows 7 x86</p></td>
<td align="left"><p>2 Go</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 7 x64</p></td>
<td align="left"><p>3 GO</p></td>
</tr>
</tbody>
</table>



### <a href="" id="med-v-1-0-sp1-client-configuration-"></a>Configuration du client MED-V 1,0 SP1

**Version du .NET Framework**

Les versions suivantes de Microsoft .NET Framework sont prises en charge pour l’installation du client MED-V 1,0 SP1:

-   .NET Framework 2,0 ou .NET Framework 2,0 SP1

-   .NET Framework 3,0 ou .NET Framework 3,0 SP1

-   .NET Framework 3,5 ou .NET Framework 3,5 SP1

**Moteur de virtualisation**

Microsoft Virtual PC 2007 SP1 avec le correctif décrit dans l’article 974918 de la base de connaissances Microsoft est pris en charge pour l’installation du client MED-V 1,0 SP1 dans les configurations suivantes:

-   Fichier de disque dur virtuel statique (VHD)

-   Plusieurs fichiers VHD situés dans le même répertoire

-   Fichier de disque dur virtuel dynamique

**Navigateur Internet**

Windows Internet Explorer 7 et Windows Internet Explorer 8 sont pris en charge pour l’installation du client MED-V 1,0 SP1.

**Microsoft Hyper-V Server**

Le client MED-V n’est pas pris en charge dans un environnement Microsoft Hyper-V Server.

## Configuration système requise pour l’espace de travail MED-V 1,0 SP1


MED-V 1,0 SP1 présente les modifications apportées à la configuration requise pour les systèmes MED-V 1,0.

### Configuration requise pour le système d’exploitation MED-V

Le tableau suivant répertorie les systèmes d’exploitation pris en charge pour les espaces de travail MED-V 1,0 SP1.

**Remarque**  
Microsoft prend en charge le Service Pack actuel et, dans certains cas, le Service Pack immédiatement précédent. Pour savoir comment accéder aux délais de prise en charge de votre produit, voir les [Service Packs pris en charge](https://go.microsoft.com/fwlink/?LinkId=31975) https://go.microsoft.com/fwlink/?LinkId=31975) . Pour plus d’informations sur la politique de support Microsoft, voir FAQ sur la politique de support [Microsoft](https://go.microsoft.com/fwlink/?LinkId=31976) ( https://go.microsoft.com/fwlink/?LinkId=31976) .



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
<td align="left"><p>Windows2000</p></td>
<td align="left"><p>Professionnel</p></td>
<td align="left"><p>REPLISTOR6.2SP4</p></td>
<td align="left"><p>Processeur</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows XP</p></td>
<td align="left"><p>Edition professionnelle</p></td>
<td align="left"><p>SP2 ou SP3</p>
<div class="alert">
<strong>Remarque</strong><br/><p>SP3 est recommandé de s’assurer que l’espace de travail MED-V est compatible avec des versions ultérieures de MED-V.</p>
</div>
<div>

</div></td>
<td align="left"><p>x86</p></td>
</tr>
</tbody>
</table>



### <a href="" id="med-v-1-0-sp1-workspace-configuration-"></a>Configuration de l’espace de travail MED-V 1,0 SP1

**Version du .NET Framework**

MED-V nécessite une des versions prises en charge suivantes de l’installation de Microsoft .NET Framework pour MED-V 1,0 SP1:

-   .NET Framework 2,0 SP1

-   .NET Framework 3,0 SP1

-   .NET Framework 3,5 ou .NET Framework 3,5 SP1

**Remarque**  
Nous recommandons .NET Framework 3,5 SP1 pour s’assurer que l’espace de travail MED-V est compatible avec des versions ultérieures de MED-V.



**Navigateur Internet**

Windows Internet Explorer 6 SP2 et Windows Internet Explorer 7 sont pris en charge pour l’installation de l’espace de travail 1,0 SP1 pour MED-V.

### <a href="" id="med-v-workspace-images-"></a>Images d’espace de travail MED-V

Les images d’espace de travail MED-V doivent être créées à l’aide de Virtual PC 2007 SP1.

## Configuration système requise pour MED-V 1,0 SP1


MED-V 1,0 SP1 présente les modifications apportées à la configuration requise pour les systèmes MED-V 1,0.

### Configuration requise pour le système d’exploitation MED-V 1,0

Le tableau suivant répertorie les systèmes d’exploitation pris en charge pour les installations du serveur MED-V 1,0 SP1.

**Remarque**  
Microsoft prend en charge le Service Pack actuel et, dans certains cas, le Service Pack immédiatement précédent. Pour savoir comment accéder aux délais de prise en charge de votre produit, voir les [Service Packs pris en charge](https://go.microsoft.com/fwlink/?LinkId=31975) https://go.microsoft.com/fwlink/?LinkId=31975) . Pour plus d’informations sur la politique de support Microsoft, voir FAQ sur la politique de support [Microsoft](https://go.microsoft.com/fwlink/?LinkId=31976) ( https://go.microsoft.com/fwlink/?LinkId=31976) .



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
<td align="left"><p>WindowsServer2008</p></td>
<td align="left"><p>Standard ou Entreprise</p></td>
<td align="left"><p>SP1 ou SP2</p></td>
<td align="left"><p>X86 ou x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008R2</p></td>
<td align="left"><p>Standard ou Entreprise</p></td>
<td align="left"><p>None</p></td>
<td align="left"><p>x64</p></td>
</tr>
</tbody>
</table>



### <a href="" id="med-v-1-0-sp1-server-configuration-"></a>Configuration du serveur MED-V 1,0 SP1

**Version du .NET Framework**

MED-V nécessite une des versions prises en charge suivantes de l’installation de Microsoft .NET Framework pour MED-V 1,0 SP1:

-   .NET Framework 2,0 ou .NET Framework 2,0 SP1

-   .NET Framework 3,0 ou .NET Framework 3,0 SP1

-   .NET Framework 3,5 ou .NET Framework 3,5 SP1

**Version de Microsoft SQL Server**

Les versions suivantes de Microsoft SQL Server sont prises en charge pour MED-V 1,0 SP1 lorsque SQL Server est installé en local ou à distance à partir du serveur MED-V 1,0 SP1:

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Version de SQL Server</th>
<th align="left">Édition</th>
<th align="left">Service Pack</th>
<th align="left">Architecture système</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>SQL Server 2005</p></td>
<td align="left"><p>Edition rapide, standard ou entreprise</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>X86 ou x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>SQL Server 2008</p></td>
<td align="left"><p>Express, standard ou entreprise</p></td>
<td align="left"><p>None</p></td>
<td align="left"><p>X86 ou x64</p></td>
</tr>
</tbody>
</table>



**Microsoft Hyper-V Server**

Le serveur MED-V est pris en charge dans un environnement Microsoft Hyper-V Server.

## Informations de globalisation MED-V 1,0 SP1


Même si MED-V n’est pas divulgué dans des langues autres que l’anglais, les versions suivantes du système d’exploitation Windows sont prises en charge pour le client et les installations serveur MED-V 1,0 SP1:

-   Anglais

-   Français

-   Allemand

-   Italien

-   Espagnol

-   Portugais (Brésil)

-   Néerlandais (Pays-Bas)

-   Japonais









