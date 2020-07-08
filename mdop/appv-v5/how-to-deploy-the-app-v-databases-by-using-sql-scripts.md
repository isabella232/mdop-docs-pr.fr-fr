---
title: Comment déployer les bases de données App-V à l'aide de scripts SQL
description: Comment déployer les bases de données App-V à l'aide de scripts SQL
author: dansimp
ms.assetid: 23637936-475f-4ca5-adde-76bb27d2372b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 511d1020571eead25af9e9591fe1834a9f97f068
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805484"
---
# Comment déployer les bases de données App-V à l'aide de scripts SQL


Pour utiliser les scripts SQL plutôt que le programme d’installation Windows, procédez comme suit:

-   Installer les bases de données App-V 5,0

-   Mettre à niveau les bases de données 5,0 vers une version ultérieure

**Comment installer les bases de données App-V à l’aide de scripts SQL**

1. Avant d’installer les scripts de base de données, passez en revue les termes du contrat de licence App-V et conservez-en une copie. En exécutant les scripts de base de données, vous acceptez les termes du contrat de licence. Si vous n’acceptez pas le logiciel, vous ne devez pas l’utiliser.

2. Copiez l' **appv\_server\_setup.exe** du média App-V Release vers un emplacement temporaire.

3. À partir d’une invite de commandes, exécutez **appv\_server\_setup.exe** et spécifiez un emplacement temporaire pour extraire les scripts de la base de données.

   Exemple: appv\_server\_setup.exe/layout c:\\ &lt; chemin d’emplacement temporaire&gt;

4. Naviguez jusqu’à l’emplacement temporaire que vous avez créé, ouvrez le dossier **DatabaseScripts** extrait et examinez le fichier Readme.txt approprié pour obtenir des instructions:

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Base de données</th>
   <th align="left">Emplacement du fichier Readme.txt à utiliser</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>Base de données de gestion</p></td>
   <td align="left"><p>Sous-dossier ManagementDatabase</p>
   <div class="alert">
   <strong>Important</strong><br/><p>Si vous effectuez une mise à niveau vers ou l’installation de la base de données de gestion App-V 5,0 SP3, voir <a href="https://support.microsoft.com/kb/3031340" data-raw-source="[SQL scripts to install or upgrade the App-V 5.0 SP3 Management Server database fail](https://support.microsoft.com/kb/3031340)"> scripts SQL pour installer ou mettre à niveau la base de données App-v 5,0 SP3 Management Server </a> .</p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Base de données de création de rapports</p></td>
   <td align="left"><p>Sous-dossier ReportingDatabase</p></td>
   </tr>
   </tbody>
   </table>



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## Rubriques connexes


[Déploiement du serveur App-V5.0](deploying-the-app-v-50-server.md)

[Comment déployer le serveur App-V5.0](how-to-deploy-the-app-v-50-server-50sp3.md)









