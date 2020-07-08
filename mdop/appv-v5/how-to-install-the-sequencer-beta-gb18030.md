---
title: Installation de Sequencer
description: Installation de Sequencer
author: dansimp
ms.assetid: a122caf0-f408-458c-b119-dc84123c1d58
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a8542abfecd7f1d543228ab1a86a59b9ee918947
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805364"
---
# Installation de Sequencer


Utilisez la procédure suivante pour installer le Sequencer Microsoft Application Virtualization (App-V) 5,0. L’ordinateur qui exécute le Sequencer ne doit pas exécuter de version du client App-V 5,0.

La mise à niveau d’une installation antérieure du Sequencer App-V n’est pas prise en charge.

**Important**  Pour obtenir la liste complète de la configuration requise pour le Sequencer, voir sections de Sequencer de l' [application-v 5,0 requise](app-v-50-prerequisites.md) et [configurations de app-v 5,0 prises en charge](app-v-50-supported-configurations.md).

 

Vous pouvez également utiliser la ligne de commande pour installer le Sequencer App-V 5,0. La liste suivante présente des informations sur les options d’installation du Sequencer à l’aide de la ligne de commande et **appv\_sequencer\_setup.exe**:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Commande</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>/INSTALLDIR</p></td>
<td align="left"><p>Spécifie le répertoire d’installation.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/CEIPOPTIN</p></td>
<td align="left"><p>Permet de participer au programme d’amélioration du produit de Microsoft.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/Log</p></td>
<td align="left"><p>Spécifie l’emplacement dans lequel le journal d’installation sera enregistré, l’emplacement par défaut est <strong> % temp% </strong> . Par exemple, <strong> C:\ Consigne </strong> . log.</p></td>
</tr>
<tr class="even">
<td align="left"><p>établit</p></td>
<td align="left"><p>Spécifie une installation silencieuse ou silencieuse.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/Uninstall</p></td>
<td align="left"><p>Spécifie la suppression du Sequencer.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/ACCEPTEULA</p></td>
<td align="left"><p>Accepter le contrat de licence. Ce type de fichier est requis pour une installation sans assistance. Exemple d’utilisation: <strong> /AcceptEULA </strong> ou <strong> /ACCEPTEULA = 1 </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/LAYOUT</p></td>
<td align="left"><p>Spécifie l’action de disposition associée. Il extrait également les fichiers Windows Installer (. msi) et script dans un dossier sans installer App-V 5,0. Aucune valeur n’est attendue.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/LAYOUTDIR</p></td>
<td align="left"><p>Spécifie le répertoire de disposition. Nécessite une valeur de chaîne. Exemple d’utilisation: <strong> /LAYOUTDIR = «client de virtualisation C:\Application» </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/? Ou/h ou/Help</p></td>
<td align="left"><p>Affiche l’aide associée.</p></td>
</tr>
</tbody>
</table>

 

**Pour installer le Sequencer App-V 5,0**

1.  Copiez les fichiers d’installation de Sequencer App-V 5,0 sur l’ordinateur sur lequel il est installé. Double-cliquez sur **appv\_sequencer\_setup.exe** puis cliquez sur **installer**.

2.  Sur la page termes du contrat de **licence logiciel** , prenez connaissance des termes du contrat de licence. Pour accepter les termes du contrat de licence **, sélectionnez J’accepte les termes du contrat de licence.** Cliquez sur **Suivant**.

3.  Sur la page **utiliser Microsoft Update pour garantir la sécurité et** la mise à jour de votre ordinateur, activez la **case à cocher utiliser Microsoft Update lorsque je recherche des mises à jour (recommandé).** Pour désactiver l’exécution des mises à jour de Microsoft, sélectionnez **je ne veux pas utiliser Microsoft Update**. Cliquez sur **Suivant**.

4.  Sur la page du **programme d’amélioration** du produit, pour participer au programme, sélectionnez **participer au programme d’amélioration du**produit. Cela permettra d’obtenir des informations sur l’utilisation de l’application-V 5,0. Si vous ne voulez pas participer au programme, sélectionnez **je ne veux pas**participer au programme pour le moment. Cliquez sur **Installer**.

5.  Pour ouvrir le Sequencer, cliquez sur **Démarrer** , puis sur **Microsoft Application Virtualization Sequencer**.

**Pour résoudre les problèmes liés à l’installation de Sequencer App-V 5,0**

-   Pour plus d’informations sur l’installation de Sequencer, vous pouvez afficher le journal des erreurs dans le dossier **% temp%** . Pour passer en revue les fichiers journaux, cliquez sur **Démarrer**, tapez **% temp%**, puis recherchez le **Journal appv\_**.

    Vous **avez une suggestion pour App-V**? Ajoutez ou Votez en fonction [de suggestions.](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization) **Vous avez un problème lié à l’application-V?** Utilisez le [Forum TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Rubriques connexes


[Envisager de déployer App-V](planning-to-deploy-app-v.md)

 

 





