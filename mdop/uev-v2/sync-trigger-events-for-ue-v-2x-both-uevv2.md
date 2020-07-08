---
title: Synchroniser les événements du déclencheur pour UE-V2.x
description: Synchroniser les événements du déclencheur pour UE-V2.x
author: dansimp
ms.assetid: 4ed71a13-6a4f-4376-996f-74b126536bbc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f3e89a0370790e7f462b2f469792128dba033460
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811970"
---
# Synchroniser les événements du déclencheur pour UE-V2.x


Microsoft User Interface Virtualization (UE-V) 2,0, 2,1 et 2,1 SP1 vous permet de synchroniser vos paramètres d’application et de Windows sur tous les appareils joints à votre domaine. Les *événements de déclencheurs de synchronisation* déterminent à quel moment UE-V agent synchronise ces paramètres avec l’emplacement de stockage des paramètres. UE-V 2 introduit une nouvelle *méthode de synchronisation* appelée *SyncProvider*. Pour plus d’informations sur la configuration de la méthode de synchronisation, voir [méthodes de synchronisation pour UE-V 2. x](sync-methods-for-ue-v-2x-both-uevv2.md).

## Événements du déclencheur de synchronisation UE-V 2


Le tableau suivant décrit les événements de déclenchement des paramètres Windows et applications classiques.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Événement déclencheur UE-V 2</strong></p></td>
<td align="left"><p><strong>PowerSchool = SyncProvider</strong></p></td>
<td align="left"><p><strong>PowerSchool = aucun</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Connexion Windows</strong></p></td>
<td align="left"><ul>
<li><p>Les paramètres d’application et de fenêtre sont importés dans le cache local à partir de l’emplacement de stockage des paramètres.</p></li>
<li><p><a href="https://technet.microsoft.com/library/dn458932.aspx#autosyncsettings2" data-raw-source="[Asynchronous Windows settings](https://technet.microsoft.com/library/dn458932.aspx#autosyncsettings2)">Les paramètres Windows asynchrones </a> sont appliqués.</p></li>
<li><p>Les paramètres Windows synchrones seront appliqués lors de la prochaine connexion Windows.</p></li>
<li><p>Les paramètres de l’application seront appliqués au démarrage de l’application.</p></li>
</ul></td>
<td align="left"><ul>
<li><p>Les paramètres d’application et de fenêtre sont lus directement à partir de l’emplacement de stockage des paramètres.</p></li>
<li><p>Les paramètres de fenêtre asynchrones et synchrones sont appliqués.</p></li>
<li><p>Les paramètres de l’application seront appliqués au démarrage de l’application.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Déconnexion Windows</strong></p></td>
<td align="left"><p>Stocker les modifications localement et mettre en cache et copier les paramètres de fenêtre asynchrones et synchrones sur le serveur emplacement de stockage des paramètres, le cas échéant.</p></td>
<td align="left"><p>Stocker les modifications apportées à l’emplacement de stockage des paramètres Windows asynchrones et synchrones</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Windows Connect (RDP)/déverrouiller</strong></p></td>
<td align="left"><p>Synchronisez les paramètres Windows asynchrones à partir de l’emplacement de stockage des paramètres au cache local, le cas échéant.</p>
<p>Appliquer les paramètres Windows mis en cache</p></td>
<td align="left"><p>Télécharger et appliquer des paramètres Windows asynchrones à partir de l’emplacement de stockage des paramètres</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Déconnexion Windows (RDP)/verrouillage</strong></p></td>
<td align="left"><p>Stocker les modifications apportées aux paramètres Windows asynchrones dans le cache local.</p>
<p>Synchroniser les paramètres Windows asynchrones du cache local à l’emplacement de stockage des paramètres, le cas échéant.</p></td>
<td align="left"><p>Stocker les modifications des paramètres Windows asynchrones dans l’emplacement de stockage des paramètres</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Démarrage de l’application</strong></p></td>
<td align="left"><p>Appliquer des paramètres d’application à partir du cache local au démarrage de l’application</p></td>
<td align="left"><p>Appliquer des paramètres d’application à partir de l’emplacement de stockage des paramètres au démarrage de l’application</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Application se ferme</strong></p></td>
<td align="left"><p>Enregistrez les modifications apportées aux paramètres d’application dans le cache local et copiez les paramètres dans l’emplacement de stockage des paramètres, le cas échéant.</p></td>
<td align="left"><p>Enregistrer les modifications apportées aux paramètres d’application dans l’emplacement de stockage des paramètres</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>La tâche planifiée du contrôleur de synchronisation ou «synchroniser maintenant» est exécutée à partir du centre de paramètres de l’entreprise</strong></p>
<p></p></td>
<td align="left"><p>Les paramètres d’application et de fenêtre sont synchronisés entre l’emplacement de stockage des paramètres et le cache local.</p>
<div class="alert">
<strong>Remarque</strong><br/><p>Les modifications apportées aux paramètres ne sont pas mises en cache localement avant la fermeture d’une application. Ce déclencheur n’exporte pas les modifications apportées à une application en cours d’exécution.</p>
<p>Pour les paramètres Windows, cela signifie que les modifications apportées ne seront pas mises en cache localement et exportées jusqu’à ce que le verrouillage suivant (asynchrone ou synchrone et asynchrone) soit mis en cache.</p>
</div>
<div>

</div>
<p>Les paramètres sont appliqués dans les cas suivants:</p>
<ul>
<li><p>Les paramètres Windows asynchrones sont directement appliqués.</p></li>
<li><p>Les paramètres de l’application sont appliqués au démarrage de l’application.</p></li>
<li><p>Les paramètres Windows asynchrones et synchrones sont appliqués lors du prochain ouverture de session Windows.</p></li>
<li><p>Les paramètres de l’application Windows (AppX) s’appliquent lors de l’actualisation suivante. <a href="https://technet.microsoft.com/library/dn458944.aspx" data-raw-source="[Monitor Application Settings](https://technet.microsoft.com/library/dn458944.aspx)"> </a> Pour plus d’informations, voir surveiller les paramètres d’application.</p></li>
</ul></td>
<td align="left"><p>N/A</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Paramètres asynchrones mis à jour dans le magasin distant *</strong></p></td>
<td align="left"><p>Chargez et appliquez de nouveaux paramètres asynchrones à partir du cache.</p></td>
<td align="left"><p>Charger et appliquer des paramètres à partir du serveur central</p></td>
</tr>
</tbody>
</table>








## Rubriques connexes


[Informations techniques de référence sur UE-V2.x](technical-reference-for-ue-v-2x-both-uevv2.md)

[Modification de la fréquence des tâches planifiées UE-V 2. x](changing-the-frequency-of-ue-v-2x-scheduled-tasks-both-uevv2.md)

[Choisissez la méthode de configuration pour UE-V 2. x](https://technet.microsoft.com/library/dn458891.aspx#config)









