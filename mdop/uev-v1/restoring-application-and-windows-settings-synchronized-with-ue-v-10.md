---
title: Restauration des applications et des paramètres Windows synchronisés avec UE-V1.0
description: Restauration des applications et des paramètres Windows synchronisés avec UE-V1.0
author: dansimp
ms.assetid: 254a16b1-f186-44a4-8e22-49a4ee87c734
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 31ae83e0a44f98b66a9930f8c5db2231992a4700
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804182"
---
# Restauration des applications et des paramètres Windows synchronisés avec UE-V1.0


Les fonctionnalités WMI et PowerShell de la virtualisation de l’interface utilisateur de Microsoft (UE-V) permettent de restaurer les packages de paramètres. Les commandes WMI et PowerShell vous permettent de restaurer les paramètres d’application et de Windows aux valeurs de paramètres de l’ordinateur lors du premier lancement de l’application après l’installation d’UE-V agent. Cette action de restauration est effectuée en fonction des paramètres par application ou Windows. Les paramètres sont restaurés lors de la prochaine exécution de l’application ou lorsque l’utilisateur ouvre une session sur le système d’exploitation.

**Pour restaurer les paramètres d’application et les paramètres Windows avec PowerShell**

1.  Ouvrez la fenêtre Windows PowerShell. Pour importer le module Microsoft UE-V PowerShell, entrez la commande suivante:

    ``` syntax
    Import-module UEV
    ```

2.  Entrez l’applet de commande PowerShell suivante pour restaurer les paramètres de l’application et les paramètres Windows.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong>Applet de commande PowerShell</strong></th>
    <th align="left"><strong>Description</strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Restaurer-UevUserSetting</p></td>
    <td align="left"><p>Restaure les paramètres utilisateur pour une application ou rétablit un groupe de paramètres Windows.</p></td>
    </tr>
    </tbody>
    </table>

     

**Pour restaurer les paramètres d’application et les paramètres Windows avec WMI**

1.  Ouvrez une fenêtre PowerShell.

2.  Entrez la commande WMI suivante pour restaurer les paramètres de l’application et les paramètres Windows.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong>Commande WMI</strong></th>
    <th align="left"><strong>Description</strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Invoke-WmiMethod-namespace root\Microsoft\UEV-Class UserSettings-Name RestoreByTemplateId-ArgumentList &lt; template_ID&gt;</p></td>
    <td align="left"><p>Restaure les paramètres utilisateur pour une application ou rétablit un groupe de paramètres Windows.</p></td>
    </tr>
    </tbody>
    </table>

     

## Rubriques connexes


[Administration d'UE-V1.0](administering-ue-v-10.md)

[Opérations d'UE-V1.0](operations-for-ue-v-10.md)

 

 





