---
title: Référence des lignes de commande d'installation du client
description: Référence des lignes de commande d'installation du client
author: dansimp
ms.assetid: 122a593d-3314-4e9b-858a-08a25ed00c32
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 708daf82699c63dfaa1f99ae595911cf6bad3737
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811928"
---
# Référence des lignes de commande d'installation du client


**Pour installer MED-V à partir de la ligne de commande**

1.  À partir de la ligne de commande, exécutez le package MED-V. msi suivi de tout paramètre facultatif décrit dans le tableau suivant.

2.  Le package MED-V. msi est appelé *MED-V\_x.msi*, où *x* représente le numéro de version.

    Par exemple, *MED-V\_1.0.65.msi*.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Paramètre</th>
<th align="left">Valeur</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>/quiet</p></td>
<td align="left"><p></p></td>
<td align="left"><p>Installation silencieuse</p></td>
</tr>
<tr class="even">
<td align="left"><p>/log &lt; chemin d’accès complet au fichier journal&gt;</p></td>
<td align="left"><p>Le chemin d’accès complet au fichier journal.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>INSTALLDIR</p></td>
<td align="left"><p>Le chemin d’accès complet au répertoire d’installation.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>VMSFOLDER</p></td>
<td align="left"><p>Le chemin d’accès complet au dossier de l’ordinateur virtuel.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>INSTALL_ADMIN_TOOLS</p></td>
<td align="left"><p><strong>1, 0</strong></p>
<p>Par défaut: <strong> 0</strong></p></td>
<td align="left"><p>Installe les outils d’administration de MED-V.</p></td>
</tr>
<tr class="even">
<td align="left"><p>START_AUTOMATICALLY</p></td>
<td align="left"><p><strong>1, 0</strong></p>
<p>Par défaut: <strong> 0</strong></p></td>
<td align="left"><p>Démarre automatiquement le client MED-V chaque fois que l’utilisateur ouvre une session Windows.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>SERVER_ADDRESS</p></td>
<td align="left"><p>nom d’hôte ou adresse IP</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>SERVER_PORT</p></td>
<td align="left"><p>port</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>SERVER_SSL</p></td>
<td align="left"><p><strong>1, 0</strong></p>
<p>pour <strong> https </strong> ou <strong> http</strong></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>START_MEDV</p></td>
<td align="left"><p><strong>1, 0</strong></p>
<p>Par défaut: <strong> 1</strong></p></td>
<td align="left"><p>Démarre MED-V à la fin de l’installation de MED-V.</p>
<div class="alert">
<strong>Remarque</strong><br/><p>Nous vous conseillons de définir START_MEDV = 0 si MED-V est installé par le système.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>DESKTOP_SHORTCUT</p></td>
<td align="left"><p><strong>1, 0</strong></p>
<p>Par défaut: <strong> 1</strong></p></td>
<td align="left"><p>Crée un raccourci sur le bureau, qui démarre le client MED-V.</p></td>
</tr>
<tr class="even">
<td align="left"><p>MINIMAL_RAM_REQUIRED</p></td>
<td align="left"><p>RAM en Mo</p></td>
<td align="left"><p>Lors de l’installation de MED-V, vérifie si le nombre minimal de RAM est spécifié pour l’ordinateur. Si ce n’est pas le cas, l’installation a été annulée.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>SKIP_OS_CHECK</p></td>
<td align="left"><p><strong>1, 0</strong></p></td>
<td align="left"><p>Omet la validation du système d’exploitation.</p></td>
</tr>
</tbody>
</table>











