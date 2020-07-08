---
title: Déploiement du catalogue de modèles de paramètres pour UE-V1.0
description: Déploiement du catalogue de modèles de paramètres pour UE-V1.0
author: dansimp
ms.assetid: 0e6ab5ef-8eeb-40b4-be7b-a841bd83be96
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f342daa958607a077fa5eb2a27ec705c8d99e67f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811873"
---
# Déploiement du catalogue de modèles de paramètres pour UE-V1.0


Les modèles d’emplacement des paramètres personnalisés peuvent être stockés sur le chemin d’accès d’un dossier sur les ordinateurs Microsoft User Interface Virtualization (UE-V) ou sur un partage réseau SMB. Une tâche planifiée sur l’ordinateur vérifie la recherche de modèles nouveaux ou mis à jour à partir de cet emplacement. La tâche vérifie cet emplacement une fois par jour et met à jour son comportement de synchronisation en fonction des modèles figurant dans ce dossier. Les modèles ajoutés ou mis à jour dans ce dossier depuis la dernière vérification sont inscrits par l’agent UE-V. UE-V agent annule les modèles supprimés de ce dossier. La tâche planifiée s’exécute en tant que système. Au minimum, le partage réseau doit accorder des autorisations pour le groupe ordinateurs du domaine. Par ailleurs, accordez des autorisations d’accès au dossier de partage réseau aux administrateurs qui géreront les modèles stockés. Pour plus d’informations sur les modèles d’emplacement des paramètres personnalisés, voir [planification du déploiement de modèles personnalisés pour UE-V 1,0](planning-for-custom-template-deployment-for-ue-v-10.md).

**Pour configurer le catalogue de modèles de paramètres pour UE-V**

1.  Créez un dossier sur l’ordinateur qui stockera le catalogue de modèles de paramètres UE-V.

2.  Définissez les autorisations de niveau de partage (SMB) suivantes pour le dossier du catalogue de modèles de paramètres.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong>Compte d’utilisateur</strong></th>
    <th align="left"><strong>Recommander des autorisations</strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Tout le monde</p></td>
    <td align="left"><p>Aucune autorisation</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Ordinateurs de domaine</p></td>
    <td align="left"><p>Lire les niveaux d’autorisation</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Administrateurs</p></td>
    <td align="left"><p>Niveaux d’autorisation en lecture/écriture</p></td>
    </tr>
    </tbody>
    </table>

     

3.  Définissez les autorisations NTFS suivantes pour le dossier du catalogue de modèles de paramètres.

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Compte d’utilisateur</th>
    <th align="left">Autorisations recommandées</th>
    <th align="left">Appliquer à</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Créateur/propriétaire</p></td>
    <td align="left"><p>Contrôle total</p></td>
    <td align="left"><p>Ce dossier, les sous-dossiers et les fichiers</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Ordinateurs de domaine</p></td>
    <td align="left"><p>Afficher le contenu du dossier et lire</p></td>
    <td align="left"><p>Ce dossier, les sous-dossiers et les fichiers</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Tout le monde</p></td>
    <td align="left"><p>Aucune autorisation</p></td>
    <td align="left"><p>Aucune autorisation</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Administrateurs</p></td>
    <td align="left"><p>Contrôle total</p></td>
    <td align="left"><p>Ce dossier, les sous-dossiers et les fichiers</p></td>
    </tr>
    </tbody>
    </table>

     

4.  Cliquez sur **OK** pour fermer les boîtes de dialogue.

## Rubriques connexes


[Déploiement d'UE-V1.0](deploying-ue-v-10.md)

[Planification du déploiement de modèle personnalisé d'UE-V1.0](planning-for-custom-template-deployment-for-ue-v-10.md)

 

 





