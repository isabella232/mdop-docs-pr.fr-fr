---
title: Déploiement de l'emplacement de stockage des paramètres pour UE-V1.0
description: Déploiement de l'emplacement de stockage des paramètres pour UE-V1.0
author: dansimp
ms.assetid: b187d44d-649b-487e-98d3-a61ee2be8c2f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c179be0882bc6a0efc0f11f21fc231f03b63b0fe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811874"
---
# Déploiement de l'emplacement de stockage des paramètres pour UE-V1.0


Le déploiement de Microsoft User Interface Virtualization (UE-V) nécessite un emplacement de stockage des paramètres où les paramètres utilisateur sont stockés dans un fichier de package de paramètres. Vous pouvez configurer l’emplacement de stockage des paramètres de l’une des deux manières suivantes:

-   **Répertoire de base Active Directory** : si un répertoire de base est défini pour l’utilisateur dans Active Directory, l’agent UE-V utilisera cet emplacement pour stocker les packages d’emplacements des paramètres. L’agent UE-V crée dynamiquement le dossier de stockage propre à l’utilisateur sous la racine de l’annuaire de base. L’agent utilise uniquement le répertoire de base de l’Active Directory si aucun emplacement de stockage des paramètres n’est défini.

-   **Créer un partage de stockage de paramètres** : le partage de stockage de paramètres est un partage réseau standard accessible aux utilisateurs d’UE-V.

## Déployer un partage de stockage de paramètres UE-V


Lorsque vous créez le partage de stockage des paramètres, vous devez limiter l’accès aux seuls utilisateurs qui ont besoin d’y accéder. Les autorisations nécessaires sont indiquées dans les tableaux ci-dessous.

**Pour déployer le partage réseau UE-V**

1.  Créer un groupe de sécurité pour les utilisateurs d’UE-V.

2.  Créez un dossier sur l’ordinateur central qui stockera les packages de paramètres UE-V, puis accordez aux utilisateurs d’UE-V des autorisations de groupe sur le dossier. L’administrateur prenant en charge UE-V aura besoin d’autorisations sur ce dossier partagé.

3.  Définissez les autorisations de niveau de partage (SMB) suivantes pour le dossier Setting Storage Location:

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong>Compte d’utilisateur</strong></th>
    <th align="left"><strong>Autorisations recommandées</strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Tout le monde</p></td>
    <td align="left"><p>Aucune autorisation</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Groupe de sécurité des utilisateurs d’UE-V</p></td>
    <td align="left"><p>Contrôle total</p></td>
    </tr>
    </tbody>
    </table>

     

4.  Définissez les autorisations NTFS suivantes pour le dossier emplacement de stockage des paramètres:

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong>Compte d’utilisateur</strong></th>
    <th align="left"><strong>Autorisations recommandées</strong></th>
    <th align="left"><strong>Folder</strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Créateur/propriétaire</p></td>
    <td align="left"><p>Contrôle total</p></td>
    <td align="left"><p>Sous-dossiers et fichiers uniquement</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Groupe de sécurité des utilisateurs d’UE-V</p></td>
    <td align="left"><p>Afficher le dossier/lire les données, créer des dossiers/ajouter des données</p></td>
    <td align="left"><p>Ce dossier uniquement</p></td>
    </tr>
    </tbody>
    </table>

     

5.  Cliquez sur **OK** pour fermer les boîtes de dialogue.

Cette configuration d’autorisation permet aux utilisateurs de créer des dossiers pour le stockage des paramètres. UE-V agent crée et sécurise un `settingspackage` dossier en cas d’exécution dans le contexte de l’utilisateur. L’utilisateur reçoit le contrôle total de son `settingspackage` dossier. Les autres utilisateurs n’héritent pas de l’accès à ce dossier. Vous n’avez pas besoin de créer et de sécuriser des répertoires utilisateur individuels, car cela s’effectue automatiquement par l’agent qui s’exécute dans le contexte de l’utilisateur.

**Remarques**  Une sécurité supplémentaire peut être configurée quand un serveur Windows est utilisé pour le partage de stockage de paramètres. UE-V peut être configuré pour vérifier que le groupe de l’administrateur local ou l’utilisateur actuel est le propriétaire du dossier dans lequel les packages de paramètres sont stockés. Pour activer une sécurité supplémentaire, procédez comme suit:

1.  Ajoutez une clé de Registre **reg \ _DWORD** nommée «RepositoryOwnerCheckEnabled» dans **HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\uev\\agent\\configuration.**

2.  Définissez la valeur de clé de Registre sur 1.

 

## Rubriques connexes


[Déploiement d'UE-V1.0](deploying-ue-v-10.md)

[Configurations prises en charge pour UE-V1.0](supported-configurations-for-ue-v-10.md)

Déploiement de l’espace de stockage central pour l’utilisation de l’interface utilisateur les modèles et packages de paramètres d' [installation du générateur UE-V](installing-the-ue-v-generator.md)

[Déploiement de l'agent UE-V](deploying-the-ue-v-agent.md)

 

 





