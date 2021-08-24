---
title: Préparer un déploiement UE-V 2.x
description: Préparer un déploiement UE-V 2.x
author: dansimp
ms.assetid: c429fd06-13ff-48c5-b9c9-fa1ec01ab800
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 04/19/2017
ms.openlocfilehash: 3e4d4b69975deda473372345733d8e8593a4775d
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910529"
---
# <a name="prepare-a-ue-v-2x-deployment"></a>Préparer un déploiement UE-V 2.x


Vous devez planifier et préparer avant de déployer Microsoft User Experience Virtualization (UE-V) 2.0 ou 2.1 comme solution de synchronisation des paramètres entre les appareils accessibles par les utilisateurs dans votre entreprise. Cette rubrique vous aide à déterminer le type de déploiement que vous allez effectuer et la préparation que vous pouvez effectuer au préalable afin que votre déploiement soit réussi.

Tout d’abord, examinons les tâches que vous allez effectuer pour déployer UE-V :

-   Planifier votre déploiement UE-V déploiement

    Avant de déployer quoi que ce soit, une bonne première étape consiste à faire un peu de planification afin de pouvoir déterminer UE-V fonctionnalités que vous allez déployer. Ainsi, si vous quittez cette page, veillez à revenir et à lire les informations de planification ci-dessous.

-   [Déployer les fonctionnalités UE-V 2.x requises](deploy-required-features-for-ue-v-2x-new-uevv2.md)

    Chaque UE-V déploiement nécessite les activités ci-après :

    -   [Définir un emplacement de stockage des paramètres](https://technet.microsoft.com/library/dn458891.aspx#ssl)

    -   [Décider comment déployer l’agent UE-V et gérer les configurations UE-V de gestion](https://technet.microsoft.com/library/dn458891.aspx#config)

    -   [Installer l’agent UE-V sur](https://technet.microsoft.com/library/dn458891.aspx#agent) chaque ordinateur utilisateur qui a besoin de synchroniser les paramètres

-   Si vous le souhaitez, vous [pouvez déployer UE-V 2.x pour les applications personnalisées](deploy-ue-v-2x-for-custom-applications-new-uevv2.md)

    La planification vous aidera à déterminer si vous souhaitez que UE-V soit en mesure de prendre en charge la synchronisation des paramètres pour les applications personnalisées (tierces ou métiers), ce qui nécessite les fonctionnalités UE-V :

    -   [Installez le générateur UEV](https://technet.microsoft.com/library/dn458942.aspx#uevgen) afin de pouvoir créer, modifier et valider les modèles d’emplacement des paramètres personnalisés requis pour synchroniser les paramètres d’application personnalisée

    -   [Créer des modèles d’emplacement de paramètres personnalisés](https://technet.microsoft.com/library/dn458942.aspx#createcustomtemplates) à l’aide UE-V Generator

    -   [Déployer un catalogue UE-V de modèles de paramètres personnalisés](https://technet.microsoft.com/library/dn458942.aspx#deploycatalogue) que vous utilisez pour stocker vos modèles d’emplacement de paramètres personnalisés

Ce diagramme de flux de travail fournit une compréhension de haut niveau d’un déploiement UE-V et des décisions qui déterminent la façon dont vous UE-V dans votre entreprise.

![deploymentworkflow.](images/deploymentworkflow.png)

**Planification d’UE-V déploiement :** Tout d’abord, vous souhaitez faire un peu de planification afin de pouvoir déterminer UE-V composants que vous allez déployer. La planification d UE-V déploiement implique les éléments ci-après :

-   [Décider s’il faut synchroniser les paramètres pour les applications personnalisées](#deciding)

    Cela détermine si vous allez installer le générateur UE-V lors du déploiement, ce qui vous permet de créer des modèles d’emplacement de paramètres personnalisés. Elle implique les mesures suivantes :

    Examinez [les paramètres qui sont synchronisés automatiquement dans un déploiement UE-V.](#autosyncsettings)

    [Déterminez si vous avez besoin de synchroniser les paramètres pour d’autres applications.](#determinesettingssync)

-   Examiner [d’autres considérations pour le déploiement UE-V,](#considerations)telles que la haute disponibilité et la planification de la capacité.

-   [Confirmer les conditions préalables et les configurations pris en charge pour UE-V](#prereqs)

## <a name="decide-whether-to-synchronize-settings-for-custom-applications"></a><a href="" id="deciding"></a>Décider s’il faut synchroniser les Paramètres pour les applications personnalisées


Dans un déploiement UE-V, de nombreux paramètres sont automatiquement synchronisés. Toutefois, vous pouvez également personnaliser UE-V pour synchroniser les paramètres d’autres applications, telles que les applications métier et tierces.

Décider si vous souhaitez UE-V synchroniser les paramètres des applications personnalisées est probablement la partie la plus importante de la planification de UE-V déploiement. Les rubriques de cette section vous aideront à prendre cette décision.

### <a name="settings-that-are-automatically-synchronized-in-a-ue-v-deployment"></a><a href="" id="autosyncsettings"></a>Paramètres synchronisés automatiquement dans un déploiement UE-V de déploiement

Cette section fournit des informations sur les paramètres synchronisés par défaut dans UE-V, notamment :

Applications de bureau dont les paramètres sont synchronisés par défaut

Windows de bureau synchronisés par défaut

Déclaration de prise en charge de la synchronisation Windows paramètres d’application

Consultez les modèles de paramètres user [Experience Virtualization (UE-V)](https://www.microsoft.com/download/details.aspx?id=46367) pour Microsoft Office afin de télécharger la liste complète des paramètres Microsoft Office 2013, Microsoft Office 2010 et Microsoft Office 2007 qui sont synchronisés par UE-V.

### <a name="desktop-applications-synchronized-by-default-in-ue-v-21-and-ue-v-21-sp1"></a>Applications de bureau synchronisées par défaut dans UE-V 2.1 et UE-V 2.1 SP1

Lorsque vous installez l’agent UE-V 2.1 ou 2.1 SP1, il inscrit un groupe par défaut de modèles d’emplacement de paramètres qui capturent les valeurs des paramètres pour ces applications Microsoft courantes.

**Astuce**  
**Microsoft Office 2007 Paramètres Synchronization** : dans UE-V 2.1 et 2.1 SP1, un modèle d’emplacement de paramètres n’est plus inclus par défaut pour les applications Office 2007. Toutefois, vous pouvez toujours utiliser des modèles Office 2007 à partir de UE-V 2.0 ou une antérieure et vous pouvez obtenir les modèles à partir de la galerie de modèles [UE-V.](https://go.microsoft.com/fwlink/p/?LinkID=246589)



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
<td align="left"><p>Microsoft Office 2010</p>
<p>( <a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)"> Télécharger la liste de tous les paramètres synchronisés </a> )</p></td>
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
<p>Microsoft OneNote 2010</p>
<p>Microsoft SharePoint Designer 2010</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Office 2013</p>
<p>( <a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)"> Télécharger la liste de tous les paramètres synchronisés </a> )</p></td>
<td align="left"><p>Microsoft Word 2013</p>
<p>Microsoft Excel 2013</p>
<p>Microsoft Outlook 2013</p>
<p>Microsoft Access 2013</p>
<p>Microsoft Project 2013</p>
<p>Microsoft PowerPoint 2013</p>
<p>Microsoft Publisher 2013</p>
<p>Microsoft Visio 2013</p>
<p>Microsoft InfoPath 2013</p>
<p>Microsoft Lync 2013</p>
<p>Microsoft OneNote 2013</p>
<p>Microsoft SharePoint Designer 2013</p>
<p>Microsoft Office 2013 Télécharger Center</p>
<p>Microsoft OneDrive entreprise 2013</p>
<p>Les UE-V d’emplacement des paramètres 2.1 et 2.1 SP1 Microsoft Office 2013 incluent une prise en charge améliorée Outlook signatures. Nous avons ajouté la synchronisation des paramètres de signature par défaut pour les nouveaux messages électroniques, les réponses et les messages électroniques transmis.</p>
<div class="alert">
<strong>Remarque</strong><br/><p>Un Outlook doit être créé pour tout appareil sur lequel un utilisateur souhaite synchroniser Outlook signature. Si le profil n’est pas déjà créé, l’utilisateur peut en créer un, puis redémarrer Outlook sur cet appareil pour activer la synchronisation des signatures.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>Options de navigateur : Internet Explorer 8, Internet Explorer 9, Internet Explorer10 et Internet Explorer 11</p></td>
<td align="left"><p>Favoris, page d’accueil, onglets et barres d’outils.</p>
<div class="alert">
<strong>Remarque</strong><br/><p>UE-V n’utilise pas les paramètres d’itinérance pour les cookies Internet Explorer.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Windows accessoires</p></td>
<td align="left"><p>CalculatriceMicrosoft, Bloc-notes, WordPad.</p></td>
</tr>
</tbody>
</table>



**Remarque**  
UE-V 2.1 SP1 ne synchronise pas les paramètres entre les CalculatriceMicrosoft dans Windows 10 et les CalculatriceMicrosoft dans les systèmes d’exploitation précédents.



### <a name="desktop-applications-synchronized-by-default-in-ue-v-20"></a>Applications de bureau synchronisées par défaut dans UE-V 2.0

Lorsque vous installez l’agent UE-V 2.0, il inscrit un groupe par défaut de modèles d’emplacement de paramètres qui capturent les valeurs des paramètres pour ces applications Microsoft courantes.

**Astuce**  
**Microsoft Office 2013 Paramètres Synchronization** : dans UE-V 2.0, un modèle d’emplacement de paramètres n’est pas inclus par défaut pour les applications Office 2013, mais est disponible en téléchargement à partir de la galerie de modèles [UE-V.](https://go.microsoft.com/fwlink/p/?LinkID=246589) [La synchronisation Office 2013 avec UE-V 2.0](synchronizing-office-2013-with-ue-v-20-both-uevv2.md) fournit des détails sur les modèles pris en charge qui synchronisent Office 2013.



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
<td align="left"><p>Microsoft Office 2007</p>
<p>( <a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)"> Télécharger la liste de tous les paramètres synchronisés </a> )</p></td>
<td align="left"><p>Microsoft Access 2007</p>
<p>Microsoft Communicator 2007</p>
<p>Microsoft Excel 2007</p>
<p>Microsoft InfoPath 2007</p>
<p>Microsoft OneNote 2007</p>
<p>Microsoft Outlook 2007</p>
<p>Microsoft PowerPoint 2007</p>
<p>Microsoft Project 2007</p>
<p>Microsoft Publisher 2007</p>
<p>Microsoft SharePoint Designer 2007</p>
<p>Microsoft Visio 2007</p>
<p>Microsoft Word 2007</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Office 2010</p>
<p>( <a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)"> Télécharger la liste de tous les paramètres synchronisés </a> )</p></td>
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
<p>Microsoft OneNote 2010</p>
<p>Microsoft SharePoint Designer 2010</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Options de navigateur : Internet Explorer 8, Internet Explorer 9 et Internet Explorer10</p></td>
<td align="left"><p>Favoris, page d’accueil, onglets et barres d’outils.</p>
<div class="alert">
<strong>Remarque</strong><br/><p>UE-V n’utilise pas les paramètres d’itinérance pour les cookies Internet Explorer.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Windows accessoires</p></td>
<td align="left"><p>CalculatriceMicrosoft, Bloc-notes, WordPad.</p></td>
</tr>
</tbody>
</table>



### <a name="windows-settings-synchronized-by-default"></a><a href="" id="autosyncsettings2"></a>Windows paramètres de synchronisation par défaut

UE-V des modèles d’emplacement de paramètres qui capturent les valeurs des paramètres pour Windows paramètres.

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">paramètres Windows</th>
<th align="left">Description</th>
<th align="left">Appliquer sur</th>
<th align="left">Exporter sur</th>
<th align="left">État par défaut</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Arrière-plan du Bureau</p></td>
<td align="left"><p>Arrière-plan ou papier peint du bureau actuellement actif.</p></td>
<td align="left"><p>Connexion, déverrouillage, connexion à distance, événements de tâche programmée.</p></td>
<td align="left"><p>Déconnexion, verrouillage, déconnexion à distance, clic sur l’utilisateur sur Synchroniser maintenant dans le Centre Paramètres entreprise ou intervalle <strong> </strong> de tâche programmé</p></td>
<td align="left"><p>Activé</p></td>
</tr>
<tr class="even">
<td align="left"><p>Options d’ergonomie</p></td>
<td align="left"><p>Paramètres d’accessibilité et d’entrée, Loupe Microsoft, Narrateur et clavier à l’écran.</p></td>
<td align="left"><p>Logon uniquement.</p></td>
<td align="left"><p>Ffage de logo, clic sur l’utilisateur synchroniser maintenant dans le Centre Paramètres entreprise <strong> ou intervalle de tâche </strong> programmé</p></td>
<td align="left"><p>Activé</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Paramètres du bureau</p></td>
<td align="left"><p>menu Démarrer et la barre des tâches, options dossier, icônes de bureau par défaut, horloges supplémentaires et paramètres de région et de langue.</p></td>
<td align="left"><p>Logon uniquement.</p></td>
<td align="left"><p>Logoff, utilisateur cliquant sur Synchroniser maintenant dans le <strong> Centre Paramètres entreprise ou tâche </strong> programmée</p></td>
<td align="left"><p>Activé</p></td>
</tr>
</tbody>
</table>



**Remarque**  
À partir de Windows 8, UE-V n’affiche pas les paramètres d’itinérance liés à l’écran de démarrage, tels que les éléments et les emplacements. En outre, UE-V ne prend pas en charge la synchronisation des éléments de barre des tâches épinglés Windows raccourcis de fichier.



**Important**  
UE-V 2.1 SP1 roams taskbar settings between Windows 10 devices. Toutefois, UE-V ne synchronise pas les paramètres de barre des tâches entre les Windows 10 et les appareils exécutant des systèmes d’exploitation antérieurs.



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Groupe de paramètres</th>
<th align="left">Catégorie</th>
<th align="left">Capture</th>
<th align="left">Appliquer</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Application Paramètres</strong></p></td>
<td align="left"><p>Applications Windows  </p></td>
<td align="left"><p>Fermer l’application</p>
<p>Windows de modification des paramètres de l’application</p></td>
<td align="left"><p>Démarrer le moniteur UE-V’application au démarrage</p>
<p>Ouvrir l’application</p>
<p>Windows Événement de modification Paramètres’application</p>
<p>Arrivée d’un package de paramètres</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p>Applications de bureau</p></td>
<td align="left"><p>L’application se ferme</p></td>
<td align="left"><p>L’application s’ouvre et se ferme</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Paramètres du bureau</strong></p></td>
<td align="left"><p>Arrière-plan du Bureau</p></td>
<td align="left"><p>Verrouillage ou fermeture de logo</p></td>
<td align="left"><p>Connexion, déverrouillage, connexion à distance, notification d’arrivée d’un nouveau package, l’utilisateur clique sur Synchroniser maintenant dans le Centre Paramètres entreprise ou la tâche programmée <strong> </strong> s’exécute.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p>Facilité d’accès (courant : accessibilité, Narrateur, Loupe, Clavier à l’écran)</p></td>
<td align="left"><p>Verrouillage ou fermeture de logo</p></td>
<td align="left"><p>Logon</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p>Facilité d’accès (Shell - Audio, Accessibilité, Clavier, Souris)</p></td>
<td align="left"><p>Verrouillage ou fermeture de logo</p></td>
<td align="left"><p>Connexion, déverrouillage, connexion à distance, notification d’arrivée du nouveau package, clics de l’utilisateur sur Synchroniser maintenant dans le Centre Paramètres entreprise ou tâches <strong> </strong> programmées</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p>Paramètres du bureau</p></td>
<td align="left"><p>Verrouillage ou fermeture de logo</p></td>
<td align="left"><p>Logon</p></td>
</tr>
</tbody>
</table>



### <a name="ue-v-support-for-windows-apps"></a>UE-V prise en charge des Windows applications

Pour Windows applications, le développeur d’applications spécifie les paramètres qui sont synchronisés. Vous pouvez spécifier les Windows applications sont activées pour la synchronisation des paramètres.

Pour afficher la liste des applications Windows qui peuvent synchroniser les paramètres d’un ordinateur avec leur nom de famille de packages, leur état activé et leur source activée, à l’invite de commandes Windows PowerShell, entrez : `Get-UevAppxPackage`

**Remarque**  
À Windows 8, UE-V ne synchronise pas les paramètres Windows’application si l’utilisateur de domaine lie ses informations d’identification de connexion à son compte Microsoft. Cette liaison synchronise les paramètres Microsoft OneDrive de sorte UE-V, ce qui désactive la synchronisation des paramètres Windows’application.



### <a name="ue-v-support-for-roaming-printers"></a>UE-V prise en charge des imprimantes itinérantes

UE-V 2.1 SP1 permet aux imprimantes réseau d’être itinérantes entre les appareils afin qu’un utilisateur ait accès à ses imprimantes réseau lorsqu’il est connecté à un appareil du réseau. Cela inclut l’itinérance de l’imprimante qu’ils ont définie comme imprimante par défaut.

L’itinérance des imprimantes UE-V nécessite l’un des scénarios suivants :

-   Le serveur d’impression peut télécharger le pilote requis lorsqu’il se déplace vers un nouvel appareil.

-   Le pilote de l’imprimante réseau itinérante est préinstallé sur tout appareil qui doit accéder à cette imprimante réseau.

-   Le pilote d’imprimante peut être obtenu à partir de Windows Update.

**Remarque**  
La UE-V d’itinérance de **** l’imprimante n’itinérant pas les paramètres ou les préférences d’imprimante, tels que l’impression côté double.



### <a name="determine-whether-you-need-settings-synchronized-for-other-applications"></a><a href="" id="determinesettingssync"></a>Déterminer si vous avez besoin de synchroniser les paramètres pour d’autres applications

Après avoir examiné les paramètres qui sont synchronisés automatiquement dans un déploiement UE-V, vous souhaitez décider si vous synchronisez les paramètres pour d’autres applications, car cela détermine la façon dont vous déployez UE-V dans toute votre entreprise.

En tant qu’administrateur, lorsque vous envisagez les applications de bureau à inclure dans votre solution UE-V, réfléchissez aux paramètres qui peuvent être personnalisés par les utilisateurs et à la façon dont l’application stocke ses paramètres et à quel endroit. Toutes les applications de bureau n’ont pas de paramètres qui peuvent être personnalisés ou qui sont régulièrement personnalisés par les utilisateurs. En outre, tous les paramètres des applications de bureau ne peuvent pas être synchronisés en toute sécurité sur plusieurs ordinateurs ou environnements.

En règle générale, vous pouvez synchroniser les paramètres qui répondent aux critères suivants :

-   Paramètres sont stockés dans des emplacements accessibles aux utilisateurs. Par exemple, ne synchronisez pas les paramètres stockés dans System32 ou en dehors de la section HKEY\_CURRENT\_USER (HKCU) du Registre.

-   Paramètres qui ne sont pas spécifiques à l’ordinateur particulier. Par exemple, excluez les configurations réseau ou matérielles.

-   Paramètres qui peuvent être synchronisés entre les ordinateurs sans risque de données endommagées. Par exemple, n’utilisez pas les paramètres stockés dans un fichier de base de données.

### <a name="checklist-for-evaluating-custom-applications"></a><a href="" id="checklistsettingssync"></a>Liste de vérification pour l’évaluation des applications personnalisées

Si vous avez décidé que vous avez besoin de synchroniser les paramètres pour d’autres applications, vous pouvez utiliser cette liste de vérification pour déterminer les applications que vous inclurez.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Cette application contient-elle des paramètres que l’utilisateur peut personnaliser ?</p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Est-il important pour l’utilisateur que ces paramètres soient synchronisés ?</p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Ces paramètres utilisateur sont-ils déjà gérés par une solution de stratégie de gestion ou de paramètres d’application ? UE-V applique les paramètres d’application au démarrage de l’application et Windows paramètres lors des événements de connexion, de déverrouillage ou de connexion à distance. Si vous utilisez UE-V avec d’autres solutions de partage de paramètres, les utilisateurs peuvent être en cas d’incohérence entre les paramètres synchronisés.</p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Les paramètres de l’application sont-ils spécifiques à l’ordinateur ? Les préférences d’application et les personnalisations associées à du matériel ou à des configurations d’ordinateurs spécifiques ne sont pas synchronisées de manière cohérente entre les sessions et peuvent entraîner une expérience d’application médiocre.</p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Les paramètres du magasin d’applications se trouvent-ils dans le répertoire Program Files ou dans le répertoire de fichiers situé dans le répertoire AppData strong LocalLow users <strong> </strong> [User name] &lt; strong &gt; </strong> &lt; &gt; AppData </strong> ? Les données d’application stockées dans l’un de ces emplacements ne doivent généralement pas être synchronisées avec l’utilisateur, car ces données sont spécifiques à l’ordinateur ou parce que les données sont trop grandes pour être synchronisées.</p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>L’application stocke-t-elle des paramètres dans un fichier qui contient d’autres données d’application qui ne doivent pas être synchronisées ? UE-V synchronise les fichiers en une seule unité. Si les paramètres sont stockés dans des fichiers qui incluent des données d’application autres que des paramètres, la synchronisation de ces données supplémentaires peut entraîner une expérience d’application médiocre.</p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Quelle est la taille des fichiers qui contiennent les paramètres ? Les performances de la synchronisation des paramètres peuvent être affectées par des fichiers de grande taille. L’utilisation de fichiers de grande taille peut affecter les performances de la synchronisation des paramètres.</p></td>
</tr>
</tbody>
</table>



## <a name="other-considerations-when-preparing-a-ue-v-deployment"></a><a href="" id="considerations"></a>Autres considérations lors de la préparation d’un UE-V de déploiement


Vous devez également tenir compte des points ci-après lorsque vous préparez le déploiement UE-V :

-   [Gestion de la synchronisation des informations d’identification](#creds)

-   [Windows de paramètres d’application](#appxsettings)

-   [Modèles d’emplacement UE-V paramètres personnalisés](#custom)

-   [Configurations des paramètres utilisateur involontaires](#prevent)

-   [Performances et capacité](#capacity)

-   [Haute disponibilité](#high)

-   [Synchronisation de l’horloge de l’ordinateur](#clocksync)

### <a name="managing-credentials-synchronization-in-ue-v-21-and-ue-v-21-sp1"></a><a href="" id="creds"></a>Gestion de la synchronisation des informations d’identification UE-V 2.1 et UE-V 2.1 SP1

De nombreuses applications d’entreprise, notamment Microsoft Outlook et Lync, invitent les utilisateurs à accéder à leurs informations d’identification de domaine lors de la connexion. Les utilisateurs ont la possibilité d’enregistrer leurs informations d’identification sur le disque pour éviter d’avoir à les entrer chaque fois qu’ils ouvrent ces applications. L’activation de la synchronisation des informations d’identification itinérantes permet aux utilisateurs d’enregistrer leurs informations d’identification sur un ordinateur et d’éviter de les entrer à nouveau sur chaque ordinateur qu’ils utilisent dans leur environnement. Les utilisateurs peuvent synchroniser certaines informations d’identification de domaine UE-V 2.1 et 2.1 SP1.

**Important**  
La synchronisation des informations d’identification est désactivée par défaut. Vous devez activer explicitement la synchronisation des informations d’identification pendant le déploiement pour implémenter cette fonctionnalité.



UE-V 2.1 et 2.1 SP1 peuvent synchroniser les informations d’identification d’entreprise, mais n’itinérant pas les informations d’identification destinées uniquement à être utilisés sur l’ordinateur local.

Les informations d’identification sont des paramètres synchrones, ce qui signifie qu’ils sont appliqués à votre profil la première fois que vous vous connectez à votre ordinateur après UE-V synchronisation.

La synchronisation des informations d’identification est gérée par son propre modèle d’emplacement de paramètres, qui est désactivé par défaut. Vous pouvez activer ou désactiver ce modèle par le biais des mêmes méthodes que pour d’autres modèles. L’identificateur de modèle pour cette fonctionnalité est RoamingCredentialSettings.

**Important**  
Si vous utilisez l’itinérance des informations d’identification Active Directory dans votre environnement, nous vous recommandons de ne pas activer le modèle d’itinérance UE-V d’informations d’identification actives.



Utilisez l’une de ces méthodes pour activer la synchronisation des informations d’identification :

-   Centre de Paramètres entreprise

-   PowerShell

-   Stratégie de groupe

**Remarque**  
Les informations d’identification sont chiffrées lors de la synchronisation.



[Centre Paramètres entreprise](https://technet.microsoft.com/library/dn458903.aspx)**** : activez la case à cocher Paramètres informations d’identification itinérantes sous Windows Paramètres pour activer la synchronisation des informations d’identification. Décochez la case pour la désactiver. Cette case à cocher s’affiche uniquement dans Paramètres entreprise si votre compte n’est pas configuré pour synchroniser les paramètres à l’aide d’un compte Microsoft.

[PowerShell](https://technet.microsoft.com/library/dn458937.aspx)**: cette** cmdlet PowerShell permet la synchronisation des informations d’identification :

``` syntax
Enable-UevTemplate RoamingCredentialSettings
```

Cette cmdlet PowerShell désactive la synchronisation des informations d’identification :

``` syntax
Disable-UevTemplate RoamingCredentialSettings
```

[Stratégie de groupe](https://technet.microsoft.com/library/dn458893.aspx)**:** vous devez déployer le dernier [modèle MDOP ADMX](https://go.microsoft.com/fwlink/p/?LinkId=393944) pour activer la synchronisation des informations d’identification par le biais de la stratégie de groupe. La synchronisation des informations d’identification est gérée avec Windows paramètres. Pour gérer cette fonctionnalité avec la stratégie de groupe, activez la stratégie Synchroniser Windows paramètres.

1.  Ouvrez l’Éditeur de stratégie de groupe et accédez à Configuration utilisateur – Modèles d’administration **– Windows composants – Microsoft User Experience Virtualization**.

2.  Double-cliquez sur **Synchroniser Windows paramètres.**

3.  Si cette stratégie est activée, vous pouvez activer **** la synchronisation des informations d’identification en activant la case à cocher Informations d’identification itinérantes ou désactiver la synchronisation des informations d’identification en la désactivant.

4.  Cliquez sur **OK**.

### <a name="credential-locations-synchronized-by-ue-v"></a>Emplacements des informations d’identification synchronisés par UE-V

Les fichiers d’informations d’identification enregistrés par les applications aux emplacements suivants sont synchronisés :

-   %UserProfile%\\AppData\\Roaming\\Microsoft\\Credentials\\

-   %UserProfile%\\AppData\\Roaming\\Microsoft\\Crypto\\

-   %UserProfile%\\AppData\\Roaming\\Microsoft\\Protect\\

-   %UserProfile%\\AppData\\Roaming\\Microsoft\\SystemCertificates\\

Les informations d’identification enregistrées à d’autres emplacements ne sont pas synchronisées par UE-V.

### <a name="windows-app-settings-synchronization"></a><a href="" id="appxsettings"></a>Windows de paramètres d’application

UE-V gère la synchronisation Windows paramètres de l’application de trois manières :

-   **Synchroniser Windows applications :** Autoriser ou refuser toute synchronisation Windows’application

-   **Windows liste des applications :** Synchroniser une liste d’Windows applications

-   **Comportement de synchronisation par défaut non listé :** Déterminez le comportement de synchronisation des applications Windows qui ne sont pas dans la liste des Windows applications.

Pour plus d’informations, [voir la Windows d’applications.](https://technet.microsoft.com/library/dn458925.aspx#win8applist)

### <a name="custom-ue-v-settings-location-templates"></a><a href="" id="custom"></a>Modèles d’emplacement UE-V paramètres personnalisés

Si vous déployez UE-V pour synchroniser les paramètres des applications personnalisées, vous utiliserez le générateur UE-V pour créer des modèles d’emplacement de paramètres personnalisés pour ces applications de bureau. Après avoir créé et testé un modèle d’emplacement de paramètres personnalisé dans un environnement de test, vous pouvez déployer les modèles d’emplacement des paramètres sur les ordinateurs de l’entreprise.

Les modèles d’emplacement des paramètres personnalisés doivent être déployés avec une infrastructure de déploiement existante, comme une méthode de distribution de logiciels d’entreprise (ESD) telle que System Center Configuration Manager, avec des préférences ou en configurant un catalogue de modèles de paramètres UE-V. Les modèles déployés avec Configuration Manager ou une stratégie de groupe doivent être enregistrés à l’aide UE-V WMI ou Windows PowerShell.

Pour plus d’informations sur les modèles d’emplacement des paramètres personnalisés, voir [Deploy UE-V 2.x for Custom Applications](deploy-ue-v-2x-for-custom-applications-new-uevv2.md). Pour plus d’informations sur l UE-V’utilisation de Configuration Manager, voir [Configuration UE-V 2.x avec System Center Configuration Manager 2012](configuring-ue-v-2x-with-system-center-configuration-manager-2012-both-uevv2.md).

### <a name="prevent-unintentional-user-settings-configuration"></a><a href="" id="prevent"></a>Empêcher la configuration des paramètres utilisateur accidentels

UE-V télécharge les nouvelles informations de paramètres utilisateur à partir d’un emplacement de stockage de paramètres et applique les paramètres à l’ordinateur local dans les cas ci-après :

-   Chaque fois qu’une application est démarrée avec un modèle UE-V enregistré.

-   Lorsqu’un utilisateur se connecte à un ordinateur.

-   Lorsqu’un utilisateur déverrouille un ordinateur.

-   Lorsqu’une connexion est réalisée sur un ordinateur de bureau distant sur UE-V installé.

-   Lorsque la tâche programmée de l’application du contrôleur de synchronisation est exécuté.

Si UE-V est installé sur l’ordinateur A et l’ordinateur B, et que les paramètres que vous souhaitez pour l’application sont sur l’ordinateur A, l’ordinateur A doit d’abord ouvrir et fermer l’application. Si l’application est d’abord ouverte et fermée sur l’ordinateur B, les paramètres de l’application sur l’ordinateur A sont configurés en fonction des paramètres de l’application sur l’ordinateur B. Les Paramètres sont synchronisées entre les ordinateurs pour chaque application. Au fil du temps, les paramètres deviennent cohérents entre les ordinateurs à mesure qu’ils sont ouverts et fermés avec les paramètres préférés.

Ce scénario s’applique également aux Windows paramètres. Si les paramètres Windows sur l’ordinateur B doivent être les mêmes que les paramètres Windows de l’ordinateur A, l’utilisateur doit d’abord se connecter et se déconnecter de l’ordinateur A.

Si les paramètres utilisateur que l’utilisateur souhaite appliquer sont appliqués dans le mauvais ordre, ils peuvent être récupérés en faisant une opération de restauration pour l’application ou la configuration Windows spécifique sur l’ordinateur sur lequel les paramètres ont été remplacés. Pour plus d’informations, voir [Manage Administrative Backup and Restore in UE-V 2.x](manage-administrative-backup-and-restore-in-ue-v-2x-new-topic-for-21.md).

### <a name="performance-and-capacity-planning"></a><a href="" id="capacity"></a>Planification des performances et de la capacité

Spécifiez vos besoins en matière de UE-V avec la capacité de disque standard et la surveillance de l’état du réseau.

UE-V utilise un partage SMB (Server Message Block) pour le stockage des packages de paramètres. La taille des packages de paramètres varie en fonction des informations de paramètres de chaque application. Bien que la plupart des packages de paramètres soient de petite taille, la synchronisation de fichiers potentiellement importants, tels que les images de bureau, peut entraîner des performances médiocres, en particulier sur des réseaux plus lents.

Pour réduire les problèmes de latence du réseau, créez des emplacements de stockage de paramètres sur les mêmes réseaux locaux que les ordinateurs des utilisateurs. Nous recommandons 20 Mo d’espace disque par utilisateur pour l’emplacement de stockage des paramètres.

Par défaut, UE-V synchronisation s’est synchronisée au bout de 2 secondes pour éviter un retard excessif en raison d’un package de paramètres important. Vous pouvez configurer le paramètre SyncMethod=SyncProvider à l’aide des [objets de stratégie de groupe.](https://technet.microsoft.com/library/dn458893.aspx)

### <a name="high-availability-for-ue-v"></a><a href="" id="high"></a>Haute disponibilité pour les UE-V

Le catalogue UE-V’emplacement de stockage et de modèle de paramètres des paramètres permet de stocker les données utilisateur sur n’importe quel partage accessible en ligne. Pour garantir la haute disponibilité, suivez les critères suivants :

-   Formater le volume de stockage avec un système de fichiers NTFS.

-   Le partage peut utiliser le système de fichiers distribués (DFS), mais il existe des restrictions.
Plus précisément, la configuration cible unique de réplication du système de fichiers distribués (DFS-R) avec ou sans un espace de noms de système de fichiers distribués (DFS-N) est prise en charge.
De même, seule la configuration cible unique est prise en charge avec DFS-N.
Pour plus d’informations, voir [l’instruction](https://go.microsoft.com/fwlink/p/?LinkId=313991) de support de Microsoft concernant les données de profil utilisateur répliquées, ainsi que des informations sur la stratégie de support Microsoft pour un scénario de déploiement [DFS-R et DFS-N.](https://support.microsoft.com/kb/2533009)

    En outre, étant donné que SYSVOL utilise DFS-R pour la réplication, SYSVOL ne peut pas être utilisé pour la UE-V de données.

-   Configurez les autorisations de partage et les listes de contrôle d’accès NTFS comme spécifié dans [Deploying the Paramètres Stockage Location for UE-V 2.x](https://technet.microsoft.com/library/dn458891.aspx#ssl).

-   Utilisez le clustering de serveur de fichiers avec l’agent UE-V pour fournir l’accès à des copies des données d’état utilisateur en cas d’échec des communications.

-   Vous pouvez stocker les données de chemin d’accès de stockage des paramètres (données utilisateur) et les modèles de catalogue de paramètres sur des partages en cluster, sur des partages DFS-N ou sur les deux.

### <a name="synchronize-computer-clocks-for-ue-v-settings-synchronization"></a><a href="" id="clocksync"></a>Synchroniser les horloges des ordinateurs pour la synchronisation UE-V paramètres de synchronisation

Les ordinateurs qui exécutent l’agent UE-V doivent utiliser un serveur de temps pour maintenir une expérience de paramètres cohérente. UE-V utilise des horodaages pour déterminer si les paramètres doivent être synchronisés à partir de l’emplacement de stockage des paramètres. Si l’horloge de l’ordinateur n’est pas exacte, les anciens paramètres peuvent être plus anciens ou les nouveaux paramètres peuvent ne pas être enregistrés à l’emplacement de stockage des paramètres.

## <a name="confirm-prerequisites-and-supported-configurations-for-ue-v"></a><a href="" id="prereqs"></a>Confirmer les conditions préalables et les configurations pris en charge pour UE-V


Avant de poursuivre, assurez-vous que votre environnement inclut ces conditions requises pour l’UE-V.

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong>Système d’exploitation</strong></th>
<th align="left"><strong>Édition</strong></th>
<th align="left"><strong>Service Pack</strong></th>
<th align="left"><strong>Architecture système</strong></th>
<th align="left"><strong>Windows PowerShell</strong></th>
<th align="left"><strong>Microsoft .NET Framework</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows 7</p></td>
<td align="left"><p>Édition Ultimate, Enterprise ou Professional Edition</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>32bits ou 64bits</p></td>
<td align="left"><p>Windows PowerShell 3.0 ou supérieure</p></td>
<td align="left"><p>.NET Framework 4,5 ou supérieure pour UE-V 2.1.</p>
<p>.NET Framework 4 ou supérieure pour UE-V 2.0.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008R2</p></td>
<td align="left"><p>Standard, Enterprise, Datacenter ou Web Server</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64 bits</p></td>
<td align="left"><p>Windows PowerShell 3.0 ou supérieure</p></td>
<td align="left"><p>.NET Framework 4,5 ou supérieure pour UE-V 2.1.</p>
<p>.NET Framework 4 ou supérieure pour UE-V 2.0.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows 8 et Windows8.1</p></td>
<td align="left"><p>Enterprise ou Pro</p></td>
<td align="left"><p>Aucun(e)</p></td>
<td align="left"><p>32bits ou 64bits</p></td>
<td align="left"><p>Windows PowerShell 3.0 ou supérieure</p></td>
<td align="left"><p>.NET Framework 4.5 ou supérieure</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 10 version antérieure à 1607</p>
<div class="alert">
<strong>Remarque</strong><br/><p>Seul UE-V 2.1 SP1 prend en charge Windows 10 version antérieure à 1607</p>
</div>
<div>

</div></td>
<td align="left"><p>Enterprise ou Pro</p></td>
<td align="left"><p>Aucun(e)</p></td>
<td align="left"><p>32bits ou 64bits</p></td>
<td align="left"><p>Windows PowerShell 3.0 ou supérieure</p></td>
<td align="left"><p>.NET Framework 4.6</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2012 et Windows Server 2012 R2</p></td>
<td align="left"><p>Standard ou Datacenter</p></td>
<td align="left"><p>Aucun(e)</p></td>
<td align="left"><p>64 bits</p></td>
<td align="left"><p>Windows PowerShell 3.0 ou supérieure</p></td>
<td align="left"><p>.NET Framework 4.5 ou supérieure</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2016</p></td>
<td align="left"><p>Standard ou Datacenter</p></td>
<td align="left"><p>Aucun(e)</p></td>
<td align="left"><p>64 bits</p></td>
<td align="left"><p>Windows PowerShell 3.0 ou supérieure</p></td>
<td align="left"><p>.NET Framework 4.6 ou supérieure</p></td>
</tr>
</tbody>
</table>



En outre...

-   **Licence MDOP :** Cette technologie fait partie du Pack d’optimisation du bureau Microsoft (MDOP). Enterprise clients peuvent obtenir MDOP avec Microsoft Software Assurance. Pour plus d’informations sur Microsoft Software Assurance et l’acquisition de MDOP, voir How Do I Get MDOP ( https://go.microsoft.com/fwlink/p/?LinkId=322049) .

-   **Informations d’identification administratives** pour tout ordinateur sur lequel vous allez installer

**Remarque**  

-   À partir de WIndows 10, version 1607, UE-V est inclus dans Windows 10 pour [Enterprise](https://www.microsoft.com/WindowsForBusiness/windows-for-enterprise) et ne fait plus partie du pack d’optimisation du bureau Microsoft.

-   La UE-V Windows PowerShell de l’agent UE-V nécessite .NET Framework 4 ou supérieur Windows PowerShell 3.0 ou supérieur pour être activé. Téléchargez Windows PowerShell 3.0 [ici.](https://go.microsoft.com/fwlink/?LinkId=309609)

-   Installez .NET Framework 4 ou .NET Framework 4.5 sur les ordinateurs qui exécutent le système d’exploitation Windows 7 ou Windows Server 2008 R2. Les Windows 8, Windows8.1 et Windows Server 2012 d’exploitation sont .NET Framework 4.5. Le Windows 10 d’exploitation est .NET Framework 4.6 installé.
-   La stratégie « Supprimer le cache itinérant » pour les profils obligatoires n’est pas prise en charge avec UE-V et ne doit pas être utilisée.



Il n’existe aucune exigence spéciale de mémoire RAM (Random Access Memory) spécifique à UE-V.

### <a name="synchronization-of-settings-through-the-sync-provider"></a>Synchronisation des Paramètres via le fournisseur de synchronisation

Le fournisseur de synchronisation est le paramètre par défaut pour les utilisateurs, qui synchronise un cache local avec l’emplacement de stockage des paramètres dans les cas ci-après :

-   Logon/logoff

-   Verrouillage/déverrouillage

-   Connexion/déconnexion de bureau à distance

-   Application ouverte/close

Une tâche programmée gère cette synchronisation des paramètres toutes les 30 minutes ou par le biais de certains événements déclencheurs pour certaines applications. Pour plus d’informations, [voir Changing the Frequency of UE-V 2.x Scheduled Tasks](changing-the-frequency-of-ue-v-2x-scheduled-tasks-both-uevv2.md).

L’agent UE-V synchronise les paramètres utilisateur pour les ordinateurs qui ne sont pas toujours connectés au réseau d’entreprise (ordinateurs distants et ordinateurs portables) et les ordinateurs toujours connectés au réseau (ordinateurs qui exécutent Windows Server et hébergent des sessions VDI (Virtual Desktop Interface).

**Synchronisation pour les ordinateurs avec des connexions toujours disponibles :** Lorsque vous utilisez UE-V sur des ordinateurs qui sont toujours connectés au réseau, vous devez configurer l’agent UE-V pour synchroniser les paramètres à l’aide du paramètre *SyncMethod=None,* qui traite le serveur de stockage des paramètres comme un partage réseau standard. Dans cette configuration, l’agent UE-V peut être configuré pour signaler si l’importation des paramètres de l’application est retardée.

Activez cette configuration via l’une de ces méthodes :

-   Pendant UE-V’installation, à l’invite de commandes ou dans un fichier de commandes, définissez le paramètre AgentSetup.exe *SyncMethod = Aucun*. [Le déploiement de l UE-V agent 2.x fournit](https://technet.microsoft.com/library/dn458891.aspx#agent) plus d’informations.

-   Après l’installation UE-V, utilisez la fonctionnalité de gestion Paramètres dans System Center 2012 Configuration Manager ou les modèles ADMX MDOP pour pousser *syncMethod =* Aucune configuration.

-   Utilisez Windows PowerShell ou Windows Management Instrumentation (WMI) pour définir la configuration *SyncMethod = Aucune.*

    **Remarque**  
    Ces deux dernières méthodes ne fonctionnent pas pour les environnements d’infrastructure VDI (Virtual Desktop Infrastructure) en pool.



Vous devez redémarrer l’ordinateur avant que les paramètres ne commencent à se synchroniser.

**Remarque**  
Si vous définissez *SyncMethod = Aucun,* les modifications apportées aux paramètres sont enregistrées directement sur le serveur. Si la connexion réseau au chemin d’accès de stockage des paramètres n’est pas trouvée, les modifications apportées aux paramètres sont mises en cache sur l’appareil et synchronisées lors de la prochaine fois que le fournisseur de synchronisation s’exécute. Si le chemin d’accès de stockage des paramètres est in trouvé et que le profil utilisateur est supprimé d’un environnement VDI en pool lors de la suppression de la connexion, les modifications apportées aux paramètres sont perdues et l’utilisateur doit réappliquer la modification lorsque l’ordinateur est reconnecté au chemin de stockage des paramètres.



**Synchronisation pour les moteurs de synchronisation externes :** Le *paramètre SyncMethod=External* spécifie que si les paramètres UE-V sont écrits dans un dossier local sur l’ordinateur de l’utilisateur, tout moteur de synchronisation externe (tel que OneDrive Entreprise, Dossiers de travail, Sharepoint ou Dropbox) peut être utilisé pour appliquer ces paramètres aux différents ordinateurs accessibles aux utilisateurs.

Prise en charge des **sessions VDI partagées** : UE-V 2.1 et 2.1 SP1 assurent la prise en charge des sessions VDI partagées entre les utilisateurs finaux. Vous pouvez inscrire et configurer un modèle VDI spécial, ce qui garantit que UE-V conserve toutes ses fonctionnalités intactes pour les sessions VDI non persistantes.

**Remarque**  
Si vous n’activez pas le mode VDI pour les sessions VDI non persistantes, certaines fonctionnalités ne fonctionnent pas, telles que la [back-up/restore](https://technet.microsoft.com/library/dn878331.aspx)et la dernière bonne connue (LKG).



Le modèle VDI est fourni avec UE-V 2.1 et 2.1 SP1 et est généralement disponible ici après l’installation : C:\\Program Files\\Microsoft User Experience Virtualization\\Templates\\VdiState.xml

### <a name="prerequisites-for-ue-v-generator-support"></a>Conditions préalables à la prise en charge UE-V Générateur de prérequis

Installez le UE-V sur l’ordinateur utilisé pour créer des modèles d’emplacement de paramètres personnalisés. Cet ordinateur doit pouvoir exécuter les applications dont les paramètres sont synchronisés. Vous devez être membre du groupe Administrateurs sur l’ordinateur qui exécute le logiciel UE-V Generator.

Le UE-V générateur de fichiers doit être installé sur un ordinateur qui utilise un système de fichiers NTFS. Le logiciel UE-V Generator nécessite .NET Framework 4. Pour plus d’informations, [voir Deploy UE-V 2.x for Custom Applications](deploy-ue-v-2x-for-custom-applications-new-uevv2.md).

## <a name="other-resources-for-this-product"></a>Autres ressources pour ce produit


-   [Microsoft User Experience Virtualization (UE-V) 2.x](index.md)

-   [Prise en main d'UE-V 2.x](get-started-with-ue-v-2x-new-uevv2.md)

-   [Administration UE-V 2.x](administering-ue-v-2x-new-uevv2.md)

-   [Résolution des problèmes UE-V 2.x](troubleshooting-ue-v-2x-both-uevv2.md)

-   [Informations techniques de référence sur UE-V 2.x](technical-reference-for-ue-v-2x-both-uevv2.md)














