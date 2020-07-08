---
title: Activation de la création de rapports sur App-V5.0 Client à l'aide de PowerShell
description: Activation de la création de rapports sur App-V5.0 Client à l'aide de PowerShell
author: dansimp
ms.assetid: a7aaf553-0f83-4cd0-8df8-93a5f1ebe497
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c004b4900a9814a11cb2706659a2edb99de6cc1b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805466"
---
# Activation de la création de rapports sur App-V5.0 Client à l'aide de PowerShell


Utilisez la procédure suivante pour configurer l’application-V 5,0 pour la création de rapports.

**Pour configurer l’ordinateur exécutant le client App-V 5,0 pour la création de rapports**

1. Installez le client App-V 5,0. Pour plus d’informations sur l’installation du client [, voir comment déployer le client App-V](how-to-deploy-the-app-v-client-gb18030.md).

2. Après avoir installé le client App-V 5,0, utilisez **Set-AppvClientConfiguration** PowerShell pour configurer les paramètres de configuration de rapport appropriés:

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Paramètre</th>
   <th align="left">Description</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>ReportingEnabled</p></td>
   <td align="left"><p>Permet au client de renvoyer des informations vers un serveur de rapports. Ce paramètre est requis pour que le client récupère les données de rapport sur le client.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>ReportingServerURL</p></td>
   <td align="left"><p>Spécifie l’emplacement sur le serveur de création de rapports où les informations client sont enregistrées. Par exemple, http:// &lt; reportingservername &gt; : &lt; reportingportnumber &gt; .</p>
   <div class="alert">
   <strong>Remarque</strong><br/><p>Il s’agit du numéro de port attribué lors de la configuration du serveur de rapports.</p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>Heures de début de création de rapports</p></td>
   <td align="left"><p>Il est défini pour planifier le client pour envoyer automatiquement les données au serveur. Ce paramètre indique l’heure à laquelle les données de rapport doivent commencer à envoyer. Il est au format 24 heures et prend un numéro entre 0-23.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>ReportingRandomDelay</p></td>
   <td align="left"><p>Spécifie le délai maximal (en minutes) pour les données à envoyer au serveur de rapports. Lorsque la tâche planifiée est lancée, le client génère un délai aléatoire compris entre 0 et ReportingRandomDelay et attend la durée spécifiée avant d’envoyer des données.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>ReportingInterval</p></td>
   <td align="left"><p>Spécifie l’intervalle de réessayer que le client doit utiliser pour renvoyer les données au serveur de rapports.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>ReportingDataCacheLimit</p></td>
   <td align="left"><p>Spécifie la taille maximale en mégaoctets (Mo) du cache XML pour le stockage des informations de rapport. La taille s’applique au cache en mémoire. Lorsque la limite est atteinte, le fichier journal est restauré.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>ReportingDataBlockSize</p></td>
   <td align="left"><p>Spécifie la taille maximale en mégaoctets (Mo) du cache XML pour le stockage des informations de rapport. La taille s’applique au cache en mémoire. Lorsque la limite est atteinte, le fichier journal est restauré.</p></td>
   </tr>
   </tbody>
   </table>



3. Une fois les paramètres appropriés configurés, l’ordinateur exécutant le client App-V 5,0 collectera automatiquement les données et renverra les données au serveur de rapports.

   De plus, les administrateurs peuvent renvoyer les données manuellement en une méthode à la demande à l’aide de l’applet de requête PowerShell **Send-AppvClientReport** .

   Vous **avez une suggestion pour App-V**? Ajoutez ou Votez en fonction [de suggestions.](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization) **Vous avez un problème lié à l’application-V?** Utilisez le [Forum TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Rubriques connexes


[Administration d'App-V à l'aide de PowerShell](administering-app-v-by-using-powershell.md)









