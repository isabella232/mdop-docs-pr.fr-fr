---
title: Configurations prises en charge par DaRT8.0
description: Configurations prises en charge par DaRT8.0
author: dansimp
ms.assetid: 95d68e5c-d202-4f4a-adef-d2098328172e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 02c891555992652bf2a9b2b674ab8377536ef9d6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810248"
---
# Configurations prises en charge par DaRT8.0


Cette rubrique spécifie les logiciels requis et la configuration requise pour les configurations prises en charge pour l’installation et l’exécution de Microsoft Diagnostics and Recovery Tools (DaRT) 8,0 dans votre environnement. La configuration requise du système d’exploitation et la configuration système requise pour exécuter DaRT 8,0 sont spécifiées. Pour plus d’informations sur les conditions préalables à envisager pour créer l’image de récupération DaRT, voir [planification de la création de l’image de récupération 8,0 de DART](planning-to-create-the-dart-80-recovery-image-dart-8.md).

Pour les configurations prises en charge qui s’appliquent aux versions ultérieures, consultez la documentation de la version en vigueur.

Vous pouvez installer DaRT de l’une des deux manières suivantes. Vous pouvez installer toutes les fonctionnalités sur un ordinateur d’administrateur informatique, où vous exécuterez toutes les tâches associées à l’exécution de DaRT. Vous pouvez également installer, sur l’ordinateur d’administration, uniquement la fonctionnalité DaRT qui crée l’image de récupération, puis installer la fonctionnalité utilisée pour exécuter DaRT (autrement dit, la visionneuse de connexion à distance DaRT) sur un ordinateur de bureau d’assistance.

## <a href="" id="---------dart-8-0-prerequisite-software"></a> Logiciels prérequis de DaRT 8,0


Assurez-vous que les conditions préalables suivantes sont remplies avant l’installation de DaRT.

### Configuration requise pour les ordinateurs d’administration

Le tableau suivant répertorie les conditions préalables à l’installation de l’ordinateur d’administration lors de l’installation de DaRT 8,0 et de tous les outils DaRT.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Prérequises</th>
<th align="left">Détails</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Kit d’évaluation et de développement Windows (ADK)</strong></p></td>
<td align="left"><p>Requis pour l’Assistant image de récupération DaRT. Contient les outils de déploiement, qui permettent de personnaliser, de déployer et de traiter les images Windows, et contient l’environnement de préinstallation Windows (Windows PE). Le logiciel ADK n’est pas nécessaire si vous installez uniquement la visionneuse de connexion à distance et/ou l’analyseur d’incident.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>.NET Framework 4,5</strong></p></td>
<td align="left"><p>Requis par l’Assistant image de récupération DaRT.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Kit de développement Windows ou kit de développement logiciel (facultatif)</strong></p></td>
<td align="left"><p>Crash Analyzer nécessite les outils de débogage de Windows 8 du kit de pilotes Windows pour analyser les fichiers de vidage de mémoire.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Image ISO Windows 8 64 bits</strong></p></td>
<td align="left"><p>DaRT nécessite l’image de l’environnement de récupération Windows sur Windows 8 Media. Téléchargez la version 32 bits ou 64 bits de Windows 8, en fonction du type d’image de récupération DaRT que vous voulez créer. Si vous prenez en charge les deux types de systèmes dans votre environnement, téléchargez les deux versions de Windows 8.</p></td>
</tr>
</tbody>
</table>

 

### Configuration requise pour l’ordinateur du support technique

Le tableau suivant répertorie les conditions préalables à l’installation de l’ordinateur de support technique lors de l’exécution de la visionneuse de connexion à distance DaRT 8,0.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Prérequises</th>
<th align="left">Détails</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Visionneuse de connexions à distance DaRT 8,0</strong></p></td>
<td align="left"><p>Doit être installé sur un système d’exploitation Windows 8.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>.NET Framework 4,5</strong></p></td>
<td align="left"><p>Requis par l’Assistant image de récupération DaRT</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Outils de débogage pour Windows</strong></p></td>
<td align="left"><p>Requis uniquement lors de l’installation de l’outil Analyseur de blocage</p></td>
</tr>
</tbody>
</table>

 

### Conditions préalables sur les ordinateurs des utilisateurs finaux

Aucun logiciel requis ne doit être installé sur les ordinateurs des utilisateurs finaux, autre que le système d’exploitation Windows 8.

## <a href="" id="---------dart-operating-system-requirements"></a> Configuration requise pour le système d’exploitation DaRT


### Configuration système requise pour l’ordinateur administrateur

Le tableau suivant répertorie les systèmes d’exploitation pris en charge pour l’installation de l’ordinateur d’administration DaRT.

**Remarques**  Vérifiez que vous attribuez suffisamment d’espace pour tout autre outil que vous souhaitez installer sur l’ordinateur d’administration.

 

**Remarques**  Microsoft prend en charge le Service Pack actuel et, dans certains cas, le Service Pack immédiatement précédent. Pour savoir comment accéder aux délais de prise en charge de votre produit, voir les [Service Packs pris en charge](https://go.microsoft.com/fwlink/p/?LinkId=31975). Pour plus d’informations sur la politique de support Microsoft, voir FAQ sur la politique de support [Microsoft](https://go.microsoft.com/fwlink/p/?LinkId=31976).

 

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
<th align="left">Systèmed’exploitation</th>
<th align="left">Édition</th>
<th align="left">Service Pack</th>
<th align="left">Architecture système</th>
<th align="left">Configuration requise pour le système d’exploitation</th>
<th align="left">RAM requise pour l’utilisation de DaRT</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows8</p></td>
<td align="left"><p>Toutes les éditions</p></td>
<td align="left"><p>N/A</p></td>
<td align="left"><p>64 bits</p></td>
<td align="left"><p>2 Go</p></td>
<td align="left"><p>2,5 GO</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows8</p></td>
<td align="left"><p>Toutes les éditions</p></td>
<td align="left"><p>N/A</p></td>
<td align="left"><p>32 bits</p></td>
<td align="left"><p>1 Go</p></td>
<td align="left"><p>1,5 GO</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2012</p></td>
<td align="left"><p>Standard, entreprise, centre de données</p></td>
<td align="left"><p>N/A</p></td>
<td align="left"><p>64 bits</p></td>
<td align="left"><p>512 MO</p></td>
<td align="left"><p>1.0 GO</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="-------------dart-help-desk-computer-system-requirements"></a> Configuration système requise pour l’ordinateur du support technique DaRT

Si vous autorisez un support technique à résoudre des problèmes à distance, vous devez installer la visionneuse de connexions à distance sur l’ordinateur du support technique. Vous pouvez éventuellement installer l’outil Analyseur d’incident sur l’ordinateur du support technique.

Le DaRT 8,0 permet à un service d’assistance technique de se connecter à un ordinateur DaRT 8,0 à l’aide de la visionneuse de connexions à distance Dart 7,0 ou DaRT 8,0. La visionneuse de connexions à distance DaRT 7,0 nécessite un système d’exploitation Windows 7, tandis que la visionneuse de connexion à distance DaRT 8,0 nécessite Windows 8. La visionneuse de connexion à distance DaRT 8,0 et tous les autres outils DaRT 8,0 peuvent être installés uniquement sur un ordinateur exécutant Windows 8.

Le tableau suivant répertorie les systèmes d’exploitation pris en charge pour l’installation de l’ordinateur de bureau d’assistance DaRT.

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
<th align="left">Systèmed’exploitation</th>
<th align="left">Édition</th>
<th align="left">Service Pack</th>
<th align="left">Architecture système</th>
<th align="left">Configuration requise pour le système d’exploitation</th>
<th align="left">RAM requise pour l’utilisation de DaRT</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows8</p></td>
<td align="left"><p>Toutes les éditions</p></td>
<td align="left"><p>N/A</p></td>
<td align="left"><p>64 bits</p></td>
<td align="left"><p>2 Go</p></td>
<td align="left"><p>2,5 GO</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows8 (avec la visionneuse de connexion à distance 8,0 uniquement)</p></td>
<td align="left"><p>Toutes les éditions</p></td>
<td align="left"><p>N/A</p></td>
<td align="left"><p>32 bits</p></td>
<td align="left"><p>1 Go</p></td>
<td align="left"><p>1,5 GO</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows 7 (avec la visionneuse de connexions à distance 7,0 uniquement)</p></td>
<td align="left"><p>Toutes les éditions</p></td>
<td align="left"><p>SP1, SP2</p></td>
<td align="left"><p>64 bits ou 32 bits</p></td>
<td align="left"><p>1 Go</p></td>
<td align="left"><p>N/A</p></td>
</tr>
<tr class="even">
<td align="left"><p>WindowsServer2012</p></td>
<td align="left"><p>Standard, entreprise, centre de données</p></td>
<td align="left"><p>N/A</p></td>
<td align="left"><p>64 bits</p></td>
<td align="left"><p>51</p></td>
<td align="left"><p>1,0 GO</p></td>
</tr>
</tbody>
</table>

 

Le DaRT a également besoin de la configuration matérielle minimum suivante pour l’ordinateur de l’utilisateur final:

Un CD ou un DVD ou un port USB-requis uniquement si vous déployez DaRT au sein de votre entreprise à l’aide d’un CD, d’un DVD ou d’un lecteur USB.

Prise en charge du BIOS pour le démarrage de l’ordinateur à partir d’un CD ou d’un DVD, d’une clé USB ou d’une partition distante ou de restauration.

### <a href="" id="-------------dart-end-user-computer-system-requirements"></a> Configuration système requise pour l’ordinateur de l’utilisateur final DaRT

La fenêtre du jeu d’outils de diagnostics et de récupération dans DaRT nécessite que l’ordinateur de l’utilisateur final utilise l’un des systèmes d’exploitation suivants avec la quantité de mémoire système disponible pour DaRT:

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
<th align="left">Systèmed’exploitation</th>
<th align="left">Édition</th>
<th align="left">Service Pack</th>
<th align="left">Architecture système</th>
<th align="left">Configuration requise pour le système d’exploitation</th>
<th align="left">RAM requise</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows8</p></td>
<td align="left"><p>Toutes les éditions</p></td>
<td align="left"><p>N/A</p></td>
<td align="left"><p>64 bits</p></td>
<td align="left"><p>2 Go</p></td>
<td align="left"><p>2,5 GO</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows8</p></td>
<td align="left"><p>Toutes les éditions</p></td>
<td align="left"><p>N/A</p></td>
<td align="left"><p>32 bits</p></td>
<td align="left"><p>1 Go</p></td>
<td align="left"><p>1,5 GO</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2012</p></td>
<td align="left"><p>Standard, entreprise, centre de données</p></td>
<td align="left"><p>N/A</p></td>
<td align="left"><p>64 bits</p></td>
<td align="left"><p>512 MO</p></td>
<td align="left"><p>1,0 GO</p></td>
</tr>
</tbody>
</table>

 

## Rubriques connexes


[Planification du déploiement de DaRT8.0](planning-to-deploy-dart-80-dart-8.md)

 

 





