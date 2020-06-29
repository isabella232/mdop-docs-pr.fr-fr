---
title: Gestion des paramètres d'espace de travail MED-V à l'aide du Gestionnaire de package de l'espace de travail MED-V
description: Gestion des paramètres d'espace de travail MED-V à l'aide du Gestionnaire de package de l'espace de travail MED-V
author: dansimp
ms.assetid: e4b2c516-b9f8-44f9-9eae-caac6c2af3e7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9905c8da0f1f0678cce9587296526e8f04493c20
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811567"
---
# Gestion des paramètres d'espace de travail MED-V à l'aide du Gestionnaire de package de l'espace de travail MED-V


Vous pouvez utiliser le gestionnaire de package de l’espace de travail MED-V pour gérer certains paramètres dans l’espace de travail MED-V.

**Pour gérer les paramètres dans un espace de travail MED-V**

1. Pour ouvrir le **Gestionnaire de package de l’espace de travail MED-v**, cliquez sur **Démarrer**, **tous les programmes**, cliquez sur **Microsoft Enterprise Desktop Virtualization**, puis sur **med-v Workspace**.

2. Dans le volet principal de l' **empaquetage de l’espace de travail MED-V** , cliquez sur **gérer les paramètres**.

3. Dans la fenêtre **Manage settings (gérer les paramètres** ), vous pouvez configurer les paramètres d’espace de travail MED-V suivants:

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong>Démarrer l’espace de travail MED-V</strong></p></td>
   <td align="left"><p>Indiquez si vous voulez démarrer l’espace de travail MED-V lors de l’ouverture de session de l’utilisateur, lors de la première utilisation, ou pour permettre à l’utilisateur final de décider du démarrage de l’espace de travail MED-V.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p></p></td>
   <td align="left"><p>L’espace de travail MED-V démarre de l’une des deux manières suivantes: lorsque l’utilisateur final se connecte ou lorsqu’il effectue une action qui nécessite MED-V, telle que l’ouverture d’une application publiée ou la saisie d’une URL nécessitant une redirection.</p>
   <p>Vous pouvez définir ce paramètre pour l’utilisateur final ou laisser l’utilisateur final contrôler le démarrage de MED-V.</p>
   <div class="alert">
   <strong>Remarque</strong><br/><p>Si vous spécifiez une décision définie par l’utilisateur final, le comportement par défaut qu’il présente est que l’espace de travail MED-V démarre lorsqu’il se connecte. Les utilisateurs peuvent modifier ce paramètre par défaut en cliquant avec le bouton droit sur l’icône MED-V dans la zone de notification et en sélectionnant <strong> paramètres utilisateur med-v </strong> . Si vous définissez ce paramètre pour l’utilisateur final, il ne peut pas modifier le mode de démarrage de MED-V.</p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>Réseaux</strong></p></td>
   <td align="left"><p>Sélectionnez <strong> partagé </strong> ou <strong> Bridged </strong> pour votre paramètre réseau. La valeur par défaut est <strong> Shared </strong> .</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p></p></td>
   <td align="left"><p><strong>Partagé </strong> - l’espace de travail MED-V utilise la traduction d’adresses réseau (NAT) pour partager les adresses IP de l’hôte&#39;s pour le trafic sortant.</p>
   <p><strong>Bridged </strong> - l’espace de travail MED-V dispose de sa propre adresse réseau, généralement obtenue via le protocole DHCP.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>Stocker les informations d’identification</strong></p></td>
   <td align="left"><p>Indiquez si vous souhaitez stocker les informations d’identification de l’utilisateur final.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p></p></td>
   <td align="left"><p>Le comportement par défaut est que le stockage des informations d’identification est désactivé de sorte que l’utilisateur final doit être authentifié à chaque ouverture de session.</p>
   <div class="alert">
   <strong>Important</strong><br/><p>Même si la mise en cache des informations d’identification de l’utilisateur final offre une meilleure utilisation de l’utilisateur, vous devez connaître les risques liés.</p>
   <p>Les informations d’identification de domaine de l’utilisateur final sont stockées dans un format réversible dans le gestionnaire d’informations d’identification Windows. Un attaquant peut écrire un programme qui récupère le mot de passe et accéder ainsi aux informations d’identification de l’utilisateur. Vous pouvez limiter ce risque uniquement en désactivant le stockage des informations d’identification de l’utilisateur final.</p>
   </div>
   <div>

   </div></td>
   </tr>
   </tbody>
   </table>



4. Cliquez sur **Enregistrer sous...** pour enregistrer les paramètres de configuration mis à jour dans le dossier spécifié. MED-V crée un fichier de registre contenant les paramètres mis à jour. Déployez le fichier de registre mis à jour à l’aide d’une stratégie de groupe. Pour plus d’informations sur l’utilisation d’une stratégie de groupe, voir [installation de logiciels de stratégie de groupe](https://go.microsoft.com/fwlink/?LinkId=195931) ( https://go.microsoft.com/fwlink/?LinkId=195931) .

   MED-V crée également un script Windows PowerShell dans le dossier spécifié que vous pouvez utiliser pour recréer ce fichier de registre mis à jour.

## Rubriques connexes


[Gestion des paramètres de configuration d'espace de travail MED-V](managing-med-v-workspace-configuration-settings.md)

[Gérer les paramètres de l'espace de travail MED-V](manage-med-v-workspace-settings.md)









