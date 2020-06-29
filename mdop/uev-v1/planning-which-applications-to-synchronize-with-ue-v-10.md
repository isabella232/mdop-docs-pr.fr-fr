---
title: Planification des applications à synchroniser avec UE-V1.0
description: Planification des applications à synchroniser avec UE-V1.0
author: dansimp
ms.assetid: c718274f-87b4-47f3-8ef7-5e1bd5557a9d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7f2b04942588d0f6efad03d5e0249534cd325c09
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804212"
---
# Planification des applications à synchroniser avec UE-V1.0


La virtualisation de l’utilisation de Microsoft User (UE-V) utilise des modèles d’emplacement des paramètres (fichiers XML) qui définissent les paramètres capturés et appliqués par UE-V. UE-V inclut un ensemble de modèles d’emplacements de paramètres prédéfinis et permet également aux administrateurs de créer des modèles d’emplacement des paramètres personnalisés pour les applications tierces ou métier utilisées dans l’entreprise.

En tant qu’administrateur, lorsque vous déterminez quelles applications inclure dans votre solution UE-V, vous devez déterminer quels paramètres peuvent être personnalisés par les utilisateurs et comment et où l’application stocke les paramètres. Toutes les applications n’ont pas de paramètres qui peuvent être personnalisés ou personnalisés de façon régulière par les utilisateurs. De plus, tous les paramètres d’application ne peuvent pas être déplacés en toute sécurité sur plusieurs ordinateurs ou environnements. Synchroniser les paramètres qui répondent aux critères suivants:

-   Paramètres stockés dans des emplacements accessibles aux utilisateurs. Par exemple, ne synchronisez pas les paramètres stockés dans la section system32 ou en dehors de la section HKCU du Registre.

-   Paramètres qui ne sont pas propres à l’ordinateur en particulier. Par exemple, excluez les configurations réseau ou matérielles.

-   Paramètres qui peuvent être synchronisés entre ordinateurs sans risque de corruption de données. Par exemple, n’utilisez pas de paramètres stockés dans un fichier de base de données.

## Modèles d’emplacement des paramètres inclus dans UE-V


**Les modèles d’emplacement des paramètres d’application UE-V**

Le logiciel d’installation de l’agent UE-V installe l’agent et inscrit un groupe par défaut de modèles d’emplacements des paramètres pour les applications Microsoft courantes. Ces paramètres de capture des paramètres de capture d’emplacements pour les applications suivantes:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong>Catégorie d’application</strong></th>
<th align="left"><strong>Description</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Applications Microsoft Office 2010</p></td>
<td align="left"><p>Microsoft Word 2010</p>
<p>Microsoft Excel 2010</p>
<p>Microsoft Outlook 2010</p>
<p>Microsoft Access 2010</p>
<p>Microsoft Project 2010</p>
<p>Microsoft PowerPoint 2010</p>
<p>Microsoft Publisher 2010</p>
<p>Microsoft Visio 2010</p>
<p>Microsoft SharePoint Workspace 2010</p>
<p>Microsoft InfoPath 2010</p>
<p>Microsoft Lync 2010</p>
<p>Microsoft OneNote 2010</p></td>
</tr>
<tr class="even">
<td align="left"><p>Options du navigateur (Internet Explorer 8, Internet Explorer 9 et Internet Explorer 10)</p></td>
<td align="left"><p>Favoris, page d’accueil, onglets et barres d’outils.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Accessoires Windows</p></td>
<td align="left"><p>Calculatrice, bloc-notes, WordPad.</p></td>
</tr>
</tbody>
</table>

 

Les paramètres d’application s’appliquent à l’application au démarrage de l’application. Ils sont enregistrés lors de la fermeture de l’application.

**UE-V-modèles d’emplacement des paramètres Windows**

La virtualisation de l’interface utilisateur inclut les modèles d’emplacement des paramètres qui capturent les valeurs de paramètres pour les paramètres Windows suivants:

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">paramètres Windows</th>
<th align="left">Description</th>
<th align="left">Appliquer le</th>
<th align="left">État par défaut</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Arrière-plan du Bureau</p></td>
<td align="left"><p>Arrière-plan actuellement actif sur le bureau.</p></td>
<td align="left"><p>Connexion, déverrouiller, connexion à distance.</p></td>
<td align="left"><p>Activé</p></td>
</tr>
<tr class="even">
<td align="left"><p>Options d’ergonomie</p></td>
<td align="left"><p>Accessibilité et paramètres d’entrée, loupe, narrateur et clavier visuel.</p></td>
<td align="left"><p>Connexion, déverrouiller, connexion à distance.</p></td>
<td align="left"><p>Désactivé</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Paramètres de bureau</p></td>
<td align="left"><p>Paramètres du menu Démarrer et de la barre des tâches, options des dossiers, icônes du bureau par défaut, horloges supplémentaires et paramètres régionaux et linguistiques.</p></td>
<td align="left"><p>Connexion uniquement.</p></td>
<td align="left"><p>Désactivé</p></td>
</tr>
</tbody>
</table>

 

L’arrière-plan du bureau Windows et les paramètres d’ergonomie sont appliqués lorsque l’utilisateur se connecte, lorsque l’ordinateur est déverrouillé ou lors d’une connexion à distance vers un autre ordinateur. L’agent enregistre ces paramètres lorsque l’utilisateur se déconnecte, lorsque l’ordinateur est verrouillé ou lorsqu’une connexion à distance est déconnectée. Par défaut, les paramètres d’arrière-plan du bureau Windows sont itinérants entre les ordinateurs utilisant la même version du système d’exploitation.

Les paramètres de bureau et d’ergonomie de Windows sont appliqués lors de l’ouverture de session avant que le Bureau ne s’affiche à l’utilisateur. Pour optimiser l’ouverture de session, ces paramètres ne sont pas itinérants par défaut. Les paramètres de bureau et d’ergonomie peuvent être activés en utilisant une stratégie de groupe, PowerShell et WMI.

UE-V ne prend pas en charge l’itinérance des paramètres entre les systèmes d’exploitation utilisant des langues différentes. Par exemple, la synchronisation entre l’anglais et l’allemand n’est pas prise en charge. La langue de tous les ordinateurs sur lesquels UE-V est itinérante doit correspondre aux paramètres de l’utilisateur.

**Remarques**  Si vous modifiez les modèles d’emplacement des paramètres fournis par Microsoft, la virtualisation de l’utilisation de l’utilisateur peut ne pas fonctionner correctement pour le groupe de paramètres Windows ou application désigné.

 

## <a href="" id="prevent-unintentional-user-settings-configuration-"></a>Empêcher la configuration involontaire des paramètres utilisateur


La virtualisation de l’utilisation de l’utilisateur vérifie la nouvelle information sur les paramètres utilisateur et télécharge ces informations en conséquence à partir d’un emplacement de stockage des paramètres. Ensuite, il applique les paramètres à l’ordinateur local dans les cas suivants:

-   Chaque fois qu’une application est lancée et dispose d’un modèle UE-V enregistré.

-   Lorsqu’un utilisateur ouvre une session sur son ordinateur.

-   Lorsqu’un utilisateur déverrouille son ordinateur.

-   Lorsqu’une connexion est établie à un ordinateur de bureau distant sur lequel UE-V est installé.

Si UE-V est installé sur l’ordinateur A et l’ordinateur B et si les paramètres souhaités pour l’application se trouvent sur l’ordinateur A, l’ordinateur a doit d’abord ouvrir et fermer l’application. Si une application est ouverte et fermée sur l’ordinateur B d’abord, les paramètres de l’application sur l’ordinateur A seront configurés de la même manière que les paramètres de l’application sur l’ordinateur B.

Ce scénario s’applique également aux paramètres Windows. Si les paramètres Windows sur l’ordinateur B doivent être identiques aux paramètres Windows sur l’ordinateur A, l’utilisateur doit d’abord se connecter et se déconnecter de l’ordinateur A.

Si les paramètres d’utilisateur souhaités sont appliqués dans un ordre incorrect, ils peuvent être récupérés en effectuant une opération de restauration pour la configuration de l’application ou de l’application spécifique sur l’ordinateur sur lequel les paramètres ont été écrasés. Pour plus d’informations, reportez-vous à [restauration des paramètres d’application et de fenêtre synchronisés avec UE-V 1,0](restoring-application-and-windows-settings-synchronized-with-ue-v-10.md).

## Modèles d’emplacement des paramètres d’UE-V personnalisés


Vous pouvez créer des modèles d’emplacement des paramètres personnalisés à l’aide du générateur UE-V. Après avoir créé et testé un modèle d’emplacement des paramètres personnalisés dans un environnement de test, vous pouvez déployer les modèles d’emplacement des paramètres sur les ordinateurs de l’entreprise. Les modèles d’emplacement des paramètres personnalisés doivent être déployés avec une infrastructure de déploiement existante, telle que la méthode de distribution de logiciels d’entreprise (ESD), avec des préférences ou en configurant un catalogue de modèles de paramètres UE-V. Les modèles déployés avec une stratégie de groupe ou par ESD doivent être enregistrés à l’aide de la version WMI ou PowerShell d’UE-V. Pour plus d’informations sur les modèles d’emplacement des paramètres personnalisés, voir [planification du déploiement de modèles personnalisés pour UE-V 1,0](planning-for-custom-template-deployment-for-ue-v-10.md).

Pour savoir si une application métier doit être synchronisée, voir [liste de contrôle pour évaluer les applications métier pour UE-V 1,0](checklist-for-evaluating-line-of-business-applications-for-ue-v-10.md).

## Rubriques connexes


[Planification pour UE-V1.0](planning-for-ue-v-10.md)

[Planification du déploiement de modèle personnalisé d'UE-V1.0](planning-for-custom-template-deployment-for-ue-v-10.md)

[Déploiement d'UE-V1.0](deploying-ue-v-10.md)

 

 





