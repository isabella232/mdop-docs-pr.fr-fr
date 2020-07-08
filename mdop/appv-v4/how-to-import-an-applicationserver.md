---
title: Procédure pour importer une application
description: Procédure pour importer une application
author: dansimp
ms.assetid: ab40acad-1025-478d-8e13-0e1ff1bd37e4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7d9cd6d065ca28b5d856acdae7d10a1280105e9d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807093"
---
# Procédure pour importer une application


En règle générale, vous importez des applications pour les rendre accessibles au flux d’un serveur de gestion des applications. Vous pouvez également ajouter une application manuellement, mais vous devez fournir des informations précises et détaillées sur celle-ci. Pour plus d’informations, voir [comment ajouter une application manuellement](how-to-manually-add-an-application.md).

**Remarques**  Pour importer une application, vous devez disposer d’un fichier d’OSD (Open Software Descriptor) en séquence ou du fichier de projet de séquence (SPRJ) sur le serveur.

 

Lors de l’importation d’une application, assurez-vous que le serveur est configuré à l’aide d’une valeur dans le champ **chemin d’accès par défaut** sous l’onglet **général** de la boîte de dialogue **Options système** (accessible en cliquant avec le bouton droit sur le nœud **système de virtualisation des applications** dans la console App-V Server). La valeur de chemin d’accès par défaut définit l’emplacement d’importation des applications, et Pendant le processus d’importation, cette valeur est utilisée pour modifier les chemins d’accès définis dans le fichier OSD du fichier SFT et des raccourcis d’icônes. Dans le fichier OSD, le chemin d’accès du fichier SFT est spécifié dans l’entrée du code base HREF et le chemin d’accès des icônes est indiqué dans l’entrée raccourcis.

Pendant le processus d’importation, le protocole, le serveur et, le cas échéant, le port spécifié dans ces deux chemins d’accès au fichier OSD est remplacé par la valeur du chemin d’accès au contenu par défaut. Le tableau suivant illustre un exemple de la façon dont le chemin d’importation sera affecté.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Chemin d’accès au contenu par défaut</th>
<th align="left">CODE base de fichier OSD HREF</th>
<th align="left">Valeur résultante</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>\server\content &lt; /p&gt;</td>
<td align="left"><p><a href="http://WebServer/myFolder/package.sft" data-raw-source="http://WebServer/myFolder/package.sft">http://WebServer/myFolder/package.sft</a></p></td>
<td align="left"><p>\server\content\myFolder\package.sft</p></td>
</tr>
</tbody>
</table>

 

**Pour importer une application**

1.  Dans le volet gauche, cliquez avec le bouton droit sur le nœud **applications** et sélectionnez **importer des applications**.

2.  Dans la boîte de dialogue **ouvrir** , accédez au fichier SPRJ ou OSD de l’application. Mettez en surbrillance le fichier, puis cliquez sur **ouvrir**.

3.  Dans l' **Assistant Nouvelle application**, assurez-vous que la case **activé** est cochée pour les applications que vous voulez diffuser. Vous pouvez également entrer une description et vérifier les chemins d’accès au serveur et aux fichiers. Par ailleurs, si vous avez configuré une licence et des groupes de serveurs, vous pouvez les sélectionner.

4.  Cliquez sur **Suivant**.

5.  Dans l’écran **raccourcis clavier publiés** , sélectionnez les zones correspondant aux emplacements dans lesquels vous souhaitez que les raccourcis d’application apparaissent sur les ordinateurs clients.

6.  Cliquez sur **Suivant**.

7.  Dans l’écran **associations de fichiers** , vous pouvez ajouter de nouvelles associations de fichiers à cette application. Pour cela, cliquez sur **Ajouter**, entrez l’extension (sans point précédent), entrez une description, puis cliquez sur **OK**.

    **Remarques**  Applications séquencées avec Sequencer 4,0 Complétez la boîte de dialogue **associations de fichiers** lors de l’importation ou de la création via la console de gestion. Les applications avec des packages de version de Sequencer antérieurs ne le sont pas.

     

8.  Cliquez sur **Suivant**.

9.  Dans l’écran **autorisations d’accès** , cliquez sur **Ajouter**.

10. Complétez la boîte de dialogue **Sélectionner des groupes** . Lorsque vous avez terminé, cliquez sur **OK**.

11. Cliquez sur **Suivant**.

12. Dans l’écran **Résumé** , vous pouvez consulter les paramètres d’importation. Cliquez sur **Terminer**, ou cliquez sur **précédent** pour changer d’importation ou cliquez sur **Annuler** pour annuler l’importation.

## Rubriques connexes


[Procédure pour gérer des groupes d'applications dans Server Management Console](how-to-manage-application-groups-in-the-server-management-console.md)

[Procédure pour gérer des applications dans Server Management Console](how-to-manage-applications-in-the-server-management-console.md)

[Procédure pour ajouter manuellement une application](how-to-manually-add-an-application.md)

 

 





