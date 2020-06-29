---
title: Méthodes de synchronisation pour UE-V2.x
description: Méthodes de synchronisation pour UE-V2.x
author: dansimp
ms.assetid: af0ae894-dfdc-41d2-927b-c2ab1b355ffe
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a163442e2ab3dbd777aca133b13b0086cdb8ae1a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810038"
---
# Méthodes de synchronisation pour UE-V2.x


L’agent Microsoft User Interface Virtualization (UE-V) 2,0, 2,1 et 2,1 SP1 vous permet de synchroniser les paramètres d’application et de Windows de l’utilisateur avec l’emplacement de stockage des paramètres. La configuration de la *méthode de synchronisation* définit le mode de chargement et de téléchargement de ces paramètres dans l’emplacement de stockage des paramètres. UE-V 2. x introduit un nouveau PowerSchool appelé *SyncProvider*. Pour plus d’informations sur les événements de déclenchement qui démarrent la synchronisation des paramètres d’application et de fenêtre, voir [événements de déclencheurs de synchronisation pour UE-V 2. x](sync-trigger-events-for-ue-v-2x-both-uevv2.md).

## Configuration de PowerSchool


Le tableau suivant décrit les modifications apportées à PowerSchool de UE-V v 1.0 à v 2.0 à v 2.1, ainsi que les paramètres de chaque configuration:

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Configuration de PowerSchool</strong></p></td>
<td align="left"><p><strong>V 1.0</strong></p></td>
<td align="left"><p><strong>V 2.0</strong></p></td>
<td align="left"><p><strong>V 2.1 et V 2.1 SP1</strong></p></td>
<td align="left"><p><strong>Description</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>SyncProvider</p></td>
<td align="left"><p>Non applicable</p></td>
<td align="left"><p>Par défaut</p></td>
<td align="left"><p>Par défaut</p></td>
<td align="left"><p>Les modifications apportées aux paramètres d’une application spécifique ou des paramètres globaux de bureau Windows sont enregistrés localement dans un dossier cache. Ces modifications sont ensuite synchronisées avec l’emplacement de stockage des paramètres lorsqu’un événement de déclenchement de synchronisation intervient. Le fait de transférer les modifications enregistre les modifications locales apportées au chemin de stockage des paramètres.</p>
<p>Ce paramètre par défaut est la norme d’or pour les ordinateurs. Cette option tente de synchroniser ce paramètre et expire après un court délai pour s’assurer que le démarrage de l’application ou du système d’exploitation n’est pas retardé pendant un certain temps.</p>
<p>Cette fonctionnalité est également liée à l’application tâche planifiée – contrôleur de synchronisation. L’administrateur contrôle la fréquence de la tâche planifiée. Par défaut, les ordinateurs synchronisent leurs paramètres toutes les 30 minutes après la connexion.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>OfflineFiles</p></td>
<td align="left"><p>Par défaut</p></td>
<td align="left"><p>Obsolète</p></td>
<td align="left"><p>Obsolète</p></td>
<td align="left"><p>Se comporte comme SyncProvider dans V 2.0.</p>
<p>Si les fichiers hors connexion sont activés et que le dossier est épinglé, UE-V détachera ce dossier et sera synchronisé directement avec le répertoire central SMB.</p>
<p><strong>Remarque: </strong> si vous souhaitez utiliser UE-V dans un bureau d’assurance (ou en déplacement avec un ordinateur portable), vous pouvez utiliser les fichiers hors connexion pour vous assurer que vos paramètres sont itinérants.Nous avons reçu suffisamment de commentaires clientèle pour l’activation de fichiers hors connexion. Par conséquent, dans UE-V 2, nous avons créé un moteur de synchronisation étroitement couplé pour mettre en cache vos données localement et synchroniser les paramètres avec le serveur central. Cette zone de fonctionnalité ne remplace pas les fichiers hors connexion ou la redirection de dossier.</p>
<p>UE-V 2 ne fonctionne pas correctement avec les dossiers en mode hors connexion, de sorte que les recommandations ne permettent pas de définir le chemin de stockage des paramètres sur un dossier en mode hors connexion ou CSC épinglé.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Externe</p></td>
<td align="left"><p>Non applicable</p></td>
<td align="left"><p>Non applicable</p></td>
<td align="left"><p>Pris en charge</p></td>
<td align="left"><p>Dans le cadre de la nouvelle version d’UE-V 2,1, cette méthode de configuration spécifie que si les paramètres UE-V sont écrits dans un dossier local sur l’ordinateur de l’utilisateur, tout moteur de synchronisation externe (par exemple, OneDrive entreprise, dossiers de travail, SharePoint ou Dropbox) peut être utilisé pour appliquer ces paramètres aux différents ordinateurs auxquels les utilisateurs accèdent.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>None</p></td>
<td align="left"><p>Oui</p></td>
<td align="left"><p>Oui</p></td>
<td align="left"><p>Oui</p></td>
<td align="left"><p>Ce paramètre de configuration est conçu pour les applications VDI (Virtual Desktop Infrastructure) et en flux. Ce paramètre doit être utilisé dans les zones Windows Server utilisées dans un centre de stockage, où la connexion sera toujours disponible.</p>
<p>Les modifications apportées aux paramètres sont enregistrées directement sur le serveur. Si la connexion réseau au chemin de stockage des paramètres n’est pas disponible, les modifications apportées aux paramètres sont mises en cache sur l’appareil et sont synchronisées lors de la prochaine exécution du fournisseur de synchronisation. Si le chemin d’accès de stockage des paramètres est introuvable et que le profil utilisateur est supprimé d’un environnement VDI en pool lors de la fermeture de session, ces modifications de paramètres sont perdues et l’utilisateur doit réappliquer la modification lorsque l’ordinateur peut à nouveau joindre le chemin de stockage des paramètres.</p>
<p>Les applications et le système d’exploitation attendent indéfiniment de la présence de l’emplacement. Cela peut entraîner une augmentation spectaculaire du temps de chargement de l’application ou du système d’exploitation si l’emplacement est introuvable.</p></td>
</tr>
</tbody>
</table>

 

Vous pouvez configurer la méthode de synchronisation de différentes manières:

-   Lorsque vous [déployez l’agent UE-V](https://technet.microsoft.com/library/dn458891.aspx#agent) par le biais d’un paramètre de ligne de commande ou d’un script de commandes

-   Par le biais des paramètres de [stratégie de groupe](https://technet.microsoft.com/library/dn458893.aspx)

-   [Module System Center Configuration](https://technet.microsoft.com/library/dn458917.aspx) pour UE-V

-   Après l’installation de l’agent UE-V, à l’aide de [Windows PowerShell ou WMI (Windows Management Instrumentation)](https://technet.microsoft.com/library/dn458937.aspx)






## Rubriques connexes


[Déployer les fonctionnalités UE-V2.x requises](deploy-required-features-for-ue-v-2x-new-uevv2.md#ssl)

[Déployer les fonctionnalités UE-V2.x requises](deploy-required-features-for-ue-v-2x-new-uevv2.md#config)

[Informations techniques de référence sur UE-V2.x](technical-reference-for-ue-v-2x-both-uevv2.md)

 

 





