---
title: Affichage et configuration des journaux MED-V
description: Affichage et configuration des journaux MED-V
author: dansimp
ms.assetid: a15537ce-981d-4f55-9c3c-e7fbf94b8fe5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7984cec072827136db9ea52a535c0ea44c6bc2c3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810128"
---
# Affichage et configuration des journaux MED-V


Lorsque vous résolvez des problèmes et rencontrez des problèmes avec MED-V, il est possible que vous trouviez utile ou nécessaire pour accéder aux journaux des événements MED-V. Vous pouvez ouvrir l’observateur d’événements pour l’ordinateur hôte et l’ordinateur virtuel invité à l’aide du kit de tâches d’administration MED-V. Vous pouvez également utiliser le kit de tâches d’administration de MED-V pour définir le niveau de journalisation des événements MED-v du journal des événements MED-v.

Pour plus d’informations sur l’ouverture du kit de tâches d’administration MED-V, voir [résolution des problèmes de med-v à l’aide du kit de tâches d’administration](troubleshooting-med-v-by-using-the-administration-toolkit.md).

## Afficher les journaux d’événements MED-V


Dans la fenêtre **Kit de tâches d’administration de MED-V** , cliquez sur événements d' **hébergement** pour ouvrir l’observateur d’événements de l’ordinateur hôte. Vous pouvez ou cliquer sur **événements invités** pour ouvrir l’observateur d’événements pour l’ordinateur virtuel invité.

L’observateur d’événements s’ouvre et affiche les journaux des événements correspondants que vous pouvez utiliser pour résoudre les problèmes que vous pouvez rencontrer lors du déploiement ou de la gestion de MED-V. Par défaut, seuls les erreurs et les avertissements sont affichés. Pour plus d’informations sur les ID d’événement et les messages spécifiques, voir [messages du journal des événements MED-V](med-v-event-log-messages.md).

**Remarques**  Les utilisateurs finaux peuvent uniquement enregistrer les fichiers journaux des événements sur l’invité s’ils disposent d’autorisations d’administration.

 

### Pour ouvrir manuellement l’observateur d’événements sur l’ordinateur hôte

1.  Cliquez sur **Démarrer**, sur **panneau de configuration**, puis sur **Outils d’administration**.

2.  Double-cliquez sur **Observateur d’événements**, puis cliquez sur **journaux des applications et des services**.

3.  Double-cliquez sur **medv**.

## Configuration des journaux des événements MED-V


Vous pouvez spécifier le niveau de journalisation des événements MED-V en sélectionnant le bouton d’option correspondant dans le kit de tâches d’administration de MED-V. Vous pouvez déterminer si la journalisation des événements inclut les erreurs uniquement, les erreurs et les avertissements, ou les erreurs, avertissements et messages d’information. Le niveau de journalisation des événements spécifié est défini pour l’ordinateur hôte et l’ordinateur virtuel invité.

Vous pouvez également spécifier le niveau de journalisation des événements en modifiant la valeur du Registre EventLogLevel. Pour plus d’informations, reportez-vous à [gestion des paramètres de configuration de l’espace de travail MED-V](managing-med-v-workspace-configuration-settings.md)

**Remarques**  Le niveau que vous spécifiez dans la fenêtre du **Kit de tâches d’administration med-v** s’applique aux futurs enregistrements d’événements med-v. Si vous définissez le niveau de capture de l’ensemble des erreurs, avertissements et messages d’information, les journaux d’événements sont retirés plus rapidement et les événements plus anciens sont supprimés.

 

## Rubriques connexes


[Redémarrage et réinitialisation d'un espace de travail MED-V](restarting-and-resetting-a-med-v-workspace.md)

[Affichage des configurations d'espace de travail MED-V](viewing-med-v-workspace-configurations.md)

 

 





