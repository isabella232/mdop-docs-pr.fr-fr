---
title: Gestion des mises à jour automatiques pour les espaces de travail MED-V
description: Gestion des mises à jour automatiques pour les espaces de travail MED-V
author: dansimp
ms.assetid: 306f28a2-d653-480d-b737-4b8b3132de5d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: b22d3250db806e740c1d62da4fed98d5956b0eeb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811069"
---
# Gestion des mises à jour automatiques pour les espaces de travail MED-V


L’espace de travail MED-V est une machine virtuelle qui contient un système d’exploitation distinct, dont le processus automatique de mise à jour des logiciels doit être géré de la même manière que les ordinateurs physiques de votre entreprise. Étant donné que le système d’exploitation invité n’est pas toujours en cours d’exécution quand le système d’exploitation hôte est en cours d’exécution, vous devez vous assurer que l’ordinateur virtuel MED-V est configuré de telle sorte que les mises à jour logicielles puissent être appliquées au système d’exploitation invité selon les besoins. La solution 2,0 de Microsoft Enterprise Desktop Virtualization (MED-V) fournit des fonctionnalités qui vous permettent de déterminer la façon dont les mises à jour logicielles automatiques sont traitées dans un espace de travail MED-V.

## Gestion de la stratégie de réveil d’un espace de travail MED-V


La politique de mise en éveil de l’espace de travail MED-V garantit que l’ordinateur virtuel MED-V est mis à disposition pour les mises à jour de la durée spécifiée dans les paramètres de configuration de MED-V. Cela s’applique aux mises à jour publiées par Microsoft via Windows Update et mises à jour déployées et contrôlées par d’autres solutions que Microsoft (par exemple, des applications antivirus).

**Important**  La stratégie de réveil de l’espace de travail MED-V est optimisée pour l’infrastructure Microsoft Update. Si vous utilisez Microsoft System Center Configuration Manager pour déployer des mises à jour non Microsoft, nous vous conseillons d’utiliser également l’éditeur de mises à jour de System Center, qui tire parti de la même infrastructure que Microsoft Update et, par conséquent, les avantages de la stratégie de réveil de l’espace de travail MED-V. Pour plus d’informations, reportez-vous à la rubrique [Publisher System Center Updates](https://go.microsoft.com/fwlink/?LinkId=200035) ( https://go.microsoft.com/fwlink/?LinkId=200035) .

 

Lorsque vous avez créé votre package d’espace de travail MED-V, vous avez configuré le moment et le mode de démarrage de celui-ci lorsque l’utilisateur final se connecte (**démarrage rapide**) ou lorsque l’utilisateur final ouvre une application publiée (**début normal**). Vous pouvez également définir l’option pour permettre à l’utilisateur final de contrôler ce paramètre.

Quelle que soit la méthode choisie, chaque fois que l’option **démarrage rapide** est sélectionnée, l’ordinateur virtuel continue de s’exécuter tant que l’hôte MED-V est connecté en tant qu’utilisateur. Dans cette configuration, dans la mesure où MED-V est actif lorsque l’hôte est actif, des mises à jour automatiques sont appliquées sans nécessiter de traitement supplémentaire de MED-V.

Néanmoins, dans les cas où le **démarrage rapide** n’est pas spécifié ou la mise en veille prolongée de la machine virtuelle, med-v garantit que le système d’exploitation invité est mis à jour régulièrement, même lorsque MED-v n’est pas utilisé régulièrement. MED-V effectue cette fonction en réappliquant régulièrement l’ordinateur virtuel en fonction des paramètres de configuration que vous spécifiez. Cela permet aux clients de mise à jour automatique de l’ordinateur virtuel de s’exécuter en fonction de leurs configurations.Au terme de la période définie par le paramètre de configuration MED-V, MED-V renvoie l’ordinateur virtuel à son état antérieur.

**Remarques**  Si l’utilisateur final ouvre une application publiée pendant la période de mise à jour, les mises à jour requises sont appliquées, mais MED-V n’est pas automatiquement mis en veille ou n’est pas arrêté après la fin de la période de mise à jour. En revanche, MED-V continue de s’exécuter.

 

La stratégie de réveil de l’espace de travail MED-V comporte trois composants principaux:

**Gestionnaire de mise à jour invité**

Résidant sur l’hôte MED-V, ce programme exécutable autonome est responsable de la réactivation de la machine virtuelle en fonction d’une planification prédéfinie et configurable. Spécifiez les paramètres de configuration qui indiquent à quel moment le gestionnaire de mise à jour doit réveiller l’ordinateur virtuel tous les jours et la durée de conservation de l’ordinateur virtuel (en minutes) pour permettre l’application des mises à jour. Une fois que le nombre de minutes spécifié est atteint, le gestionnaire de mise à jour invité place l’ordinateur virtuel en hibernation, préparé pour une utilisation ultérieure. Vous pouvez planifier l’exécution de ce programme exécutable par le biais du gestionnaire des tâches Windows.

**Service de gestion de redémarrage d’invité**

Résidant sur l’hôte MED-V, ce service a trois responsabilités principales. Outre le gestionnaire de mise à jour des invités, il gère le redémarrage de l’ordinateur virtuel lors de la connexion de l’utilisateur, le cas échéant. Il détecte le redémarrage de l’ordinateur virtuel requis par le biais des mises à jour installées. Le gestionnaire de mise à jour des invités doit donc toujours être planifié en fonction de la configuration.

**Service de mise à jour invité**

Résidant sur la machine virtuelle MED-V, ce service Windows est responsable de la surveillance des mises à jour installées. Lorsque le service a été informé de la nécessité d’un redémarrage, il notifie le service de gestion de redémarrage invité de l’hôte.

### Paramètres de configuration de la stratégie de réveil de l’espace de travail MED-V

Vous pouvez contrôler le moment et la durée pendant laquelle l’ordinateur virtuel s’est réveillé pour recevoir les mises à jour automatiques en définissant les deux valeurs de configuration suivantes dans le registre. Ces deux valeurs se trouvent sous la clé HKLM\\Software\\Microsoft\\MEDV\\v2\\VM.

**GuestUpdateTime** : configure les heures et les minutes quotidiennement lorsque MED-V doit réveiller l’ordinateur virtuel pour la mise à jour, en fonction de la norme d’horloge de 24 heures. Spécifiez l’heure au format HH: MM. La valeur par défaut est 00:00 (minuit).

**GuestUpdateDuration** : configure le nombre de minutes pendant lesquelles MED-V doit conserver l’ordinateur virtuel éveillé pour la mise à jour, en commençant à l’heure spécifiée dans le paramètre de configuration GuestUpdateTime. La valeur par défaut est 240 (4 heures). Si vous définissez cette valeur sur zéro (0), la stratégie de réactivation de l’espace de travail MED-V est désactivée.

Pour plus d’informations sur la définition des valeurs de configuration de MED-V, voir [gérer les paramètres de configuration de l’espace de travail MED-v](managing-med-v-workspace-configuration-settings.md).

**Remarques**  Dans le cadre de la mise à jour des machines virtuelles MED-V, il est recommandé de définir votre intervalle de réveil en fonction de la date à laquelle les ordinateurs virtuels MED-V doivent être mis à jour régulièrement. Par ailleurs, il est recommandé de configurer ces paramètres de manière à ce qu’ils ressemblent au comportement de l’ordinateur hôte.

 

### Redémarrez la notification à l’aide de votre système ESD

Vous pouvez configurer votre système de ESD pour avertir MED-V dès qu’un redémarrage est nécessaire pour l’espace de travail MED-V après l’application des mises à jour automatiques. Lorsque vous appliquez des mises à jour automatiques par le biais de votre système ESD dont vous savez qu’un redémarrage est nécessaire, vous devez écrire un script pour signaler l’événement global suivant sur l’espace de travail MED-V:

**Important**  Vous devez ouvrir l’événement avec des droits de modification uniquement, puis le signaler. Si vous ne l’ouvrez pas avec les autorisations appropriées, il ne fonctionne pas.

 

``` syntax
/// <summary>
/// The guest is required to be restarted due to an ESD update.
/// </summary>
public const string MedvGuestRebootRequiredEventName = @"Global\MedvGuestRebootRequiredEvent";
using (EventWaitHandle notificationEvent = 
EventWaitHandle.OpenExisting(eventName, EventWaitHandleRights.Modify))
{
notificationEvent.Set();
}
```

Lorsque vous signalez cet événement, MED-V le capture et informe l’ordinateur virtuel qu’un redémarrage est nécessaire.

## Rubriques connexes


[Gestion des mises à jour de logiciels pour les espaces de travail MED-V](managing-software-updates-for-med-v-workspaces.md)

 

 





