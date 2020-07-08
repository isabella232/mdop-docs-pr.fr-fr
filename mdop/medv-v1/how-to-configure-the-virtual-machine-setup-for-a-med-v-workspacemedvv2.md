---
title: Comment configurer l'installation d'ordinateur virtuel pour un espace de travail MED-V
description: Comment configurer l'installation d'ordinateur virtuel pour un espace de travail MED-V
author: dansimp
ms.assetid: 50bbf58b-842c-4b63-bb93-3783903f6c7d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d0ba24f0e9aa5befeaf385acf06273a53feaae29
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812137"
---
# Comment configurer l'installation d'ordinateur virtuel pour un espace de travail MED-V


Tous les paramètres de configuration de l’ordinateur virtuel sont configurés dans le module de **stratégie** sous l’onglet Configuration de l' **ordinateur** virtuel.

## Comment configurer la configuration de l’ordinateur virtuel pour un espace de travail MED-V permanent


**Pour configurer la configuration de l’ordinateur virtuel pour un espace de travail MED-V permanent**

1.  Cliquez sur un espace de travail MED-V permanent à configurer.

2.  Dans la section Configuration de l' **ordinateur virtuel persistant** , configurez les propriétés comme décrit dans le tableau suivant.

    **Remarque**  
    Les propriétés d’installation du VM persistantes sont activées uniquement pour un espace de travail MED-V permanent.



3.  Dans le menu **stratégie** , cliquez sur **valider**.

**Propriétés d’installation d’un VM persistant**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Propriété</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Exécution de la configuration VM</p></td>
<td align="left"><p>Activez cette case à cocher pour exécuter un script de configuration la première fois que l’espace de travail MED-V est exécuté.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Éditeur de script</p></td>
<td align="left"><p>Cliquez pour configurer le script de configuration. Pour plus d’informations, reportez-vous <a href="how-to-set-up-script-actions.md" data-raw-source="[How to Set Up Script Actions](how-to-set-up-script-actions.md)"> à la rubrique Configuration d’actions de script </a> .</p>
<div class="alert">
<strong>Remarque</strong><br/><p>Ce bouton est activé uniquement lorsque l' <strong> option exécuter le script de configuration de l’ordinateur virtuel </strong> est sélectionnée.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>Message affiché lors de l’exécution d’un script</p></td>
<td align="left"><p>Message à afficher pendant l’exécution du script. S’il est vide, le message par défaut s’affiche.</p>
<div class="alert">
<strong>Remarque</strong><br/><p>Ce champ est activé uniquement lorsque <strong> le script de configuration de l’ordinateur virtuel </strong> est activé.</p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



## Comment configurer la configuration de l’ordinateur virtuel pour un espace de travail Revertible MED-V


**Pour configurer la configuration de l’ordinateur virtuel pour un espace de travail revertible MED-V**

1.  Cliquez sur un espace de travail revertible MED-V à configurer.

2.  Dans la section **installation de REVERTIBLE VM** , configurez les propriétés comme décrit dans le tableau suivant.

    **Remarque**  
    Les propriétés de l’installation de l’ordinateur virtuel revertible sont activées uniquement pour un espace de travail revertible MED-V.



3.  Dans le menu **stratégie** , cliquez sur **valider**.

**Propriétés de l’installation d’Revertible VM**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Propriété</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Renommer la VM en fonction du modèle de nom de l’ordinateur</p></td>
<td align="left"><p>Activez cette case à cocher pour affecter un nom unique à chaque ordinateur à l’aide de l’espace de travail MED-V de façon à faire la différence entre plusieurs ordinateurs utilisant le même espace de travail MED-V.</p>
<p>Pour plus d’informations sur la configuration des noms d’images d’ordinateur, voir <a href="how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md" data-raw-source="[How to Configure VM Computer Name Pattern Properties](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md)"> configurer les propriétés de modèle de nom d’ordinateur VM </a> .</p></td>
</tr>
</tbody>
</table>



## Rubriques connexes


[Utilisation de l'interface utilisateur de la console de gestion MED-V](using-the-med-v-management-console-user-interface.md)

[Création d'un espace de travail MED-V](creating-a-med-v-workspacemedv-10-sp1.md)

[Exemples de configurations d'ordinateur virtuel](examples-of-virtual-machine-configurationsv2.md)









