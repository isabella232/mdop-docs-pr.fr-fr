---
title: À propos de Microsoft Application Virtualization4.6 SP2
description: À propos de Microsoft Application Virtualization4.6 SP2
author: dansimp
ms.assetid: 1429e314-9c38-472b-8687-3bed6cf0015c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 16303380782a086cfd750c7a8b2f99bf4f4c8b5d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808138"
---
# À propos de Microsoft Application Virtualization4.6 SP2


Microsoft Application Virtualization (App-V) 4.6 SP2 fournit différentes améliorations et nouvelles fonctionnalités, décrites dans cette rubrique.

**Attention**  Cette rubrique explique comment modifier le Registre Windows à l’aide de l’éditeur du Registre. Si vous modifiez la clé de registre de Windows de manière incorrecte, vous pouvez être à l’origine de problèmes importants qui peuvent nécessiter la réinstallation de Windows. Vous devez faire une copie de sauvegarde des fichiers du Registre (System. dat et User. dat) avant de modifier le registre. Microsoft ne peut pas garantir que les problèmes qui peuvent survenir lorsque vous modifiez le registre peuvent être résolus. Changez de Registre à vos propres risques.

 

**Prise en charge de Windows 8 et Windows Server 2012**

App-V 4.6 SP2 ajoute la prise en charge des services Bureau à distance de Windows 8 et Windows Server 2012.

**Prise en charge de la coexistence avec le client App-V 5,0**

App-V 4.6 SP2 fournit une prise en charge de la coexistence avec le client Microsoft Application Virtualization 5,0. Pour obtenir des instructions sur la configuration du client App-v 5,0 pour la coexistence avec le client App-v 4.6 SP2, consultez la documentation de l’application-V 5,0. Pour plus d’informations sur App-V 5,0, voir [Application Virtualization 5](https://go.microsoft.com/fwlink/?LinkId=267599) sur TechNet.

**Possibilité de virtualiser Adobe Reader X avec le mode protégé**

Pour virtualiser Adobe Reader X, vous pouvez activer la fonction mode protégé en procédant comme suit. Auparavant, vous deviez désactiver le mode protégé afin de virtualiser Adobe Reader X.

Avant de lancer le Sequencer App-V, créez la valeur de Registre suivante sous HKEY \ _LOCAL \ _MACHINE \\SOFTWARE \\Microsoft\\SoftGrid\\4.5\\SystemGuard\\Overrides:

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>Nom</p></td>
<td align="left"><p>Type</p></td>
<td align="left"><p>Données</p></td>
<td align="left"><p>Description</p></td>
</tr>
<tr class="even">
<td align="left"><p>EnableVFSPassthrough</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>1</p></td>
<td align="left"><p>Définissez cette valeur sur <strong> 1 pour </strong> Démarrer Adobe Reader X en mode protégé lors de la phase de lancement.</p></td>
</tr>
</tbody>
</table>

 

**Remarques**  Sur un ordinateur exécutant un système d’exploitation 64 bits, créez la valeur Registry sous HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\SystemGuard\\Overrides.

 

Pour chaque fichier OSD dans votre package Adobe Reader X, ajoutez les éléments suivants sous l' &lt; élément policies &gt; :

`<VIRTUAL_FILE_SYSTEM_PASS_THROUGH>TRUE</VIRTUAL_FILE_SYSTEM_PASS_THROUGH>`

`<VIRTUAL_REGISTRY_PASS_THROUGH>TRUE</VIRTUAL_REGISTRY_PASS_THROUGH>`

`<ENFORCE_ACLS_ON_VREG_MODIFY>TRUE</ENFORCE_ACLS_ON_VREG_MODIFY>`

**Paramètre de ligne de commande du nouveau Sequencer**

Lorsque vous créez un accélérateur de package à l’aide de l’interface utilisateur de Sequencer, vous pouvez sélectionner un fichier RTF ou TXT qui fournit des instructions sur la création de packages et de déploiement aux administrateurs qui appliquent l’accélérateur de package. Cette fonctionnalité est désormais disponible à l’aide de l’interface CLI de Sequencer.

`/ACCELERATORDESCRIPTIONFILE:PathToDescriptionFile`

Spécifiez un chemin d’accès à un fichier RTF ou TXT qui fournit des instructions sur le déploiement et l’empaquetage lors de la création d’un accélérateur de package.

**Le signalement d’erreurs Microsoft application ne doit plus être installé**

Lorsque vous installez le client App-V 4.6 SP2 à l’aide de setup.msi, vous n’avez plus besoin d’installer le signalement d’erreurs d’application Microsoft (dw20shared.msi). App-V 4.6 SP2 utilise désormais le signalement d’erreurs Microsoft. Pour plus d’informations, reportez-vous [à comment installer le client App-V à l’aide de Setup.msi](https://go.microsoft.com/fwlink/?LinkId=267237).

**Commentaires des clients et ROLLUP de HotFix**

App-V 4.6 SP2 inclut un correctif cumulatif pour résoudre les problèmes détectés depuis la version App-V 4,6 SP1. App-V 4.6 SP2 contient les derniers correctifs de Microsoft Application Virtualization 4,6 SP1 Hotfix 6.

## Dans cette section


<a href="" id="app-v-4-6-sp2-release-notes"></a>[Notes de publication d'App-V4.6SP2](https://go.microsoft.com/fwlink/?LinkId=267600)  
Fournit les informations mises à jour sur les problèmes connus liés à l’application-V 4.6 SP2.

 

 





