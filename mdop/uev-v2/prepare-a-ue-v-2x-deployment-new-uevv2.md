---
title: Préparer un déploiement UE-V 2. x
description: Préparer un déploiement UE-V 2. x
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
ms.openlocfilehash: e6b2de407990536e1a08532632dcea19ea0d0ee9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811747"
---
# Préparer un déploiement UE-V 2. x


Il est possible de planifier et préparer la mise à niveau avant de déployer Microsoft User Interface Virtualization (UE-V) 2,0 ou 2,1 en tant que solution pour synchroniser les paramètres entre les appareils auxquels les utilisateurs accèdent au sein de votre entreprise. Cette rubrique vous aide à déterminer le type de déploiement que vous allez effectuer et la préparation que vous pouvez effectuer au préalable pour que votre déploiement réussisse.

Tout d’abord, examinons les tâches que vous devez effectuer pour déployer UE-V:

-   Planifier votre déploiement UE-V

    Avant de déployer quoi que ce soit, il est conseillé de procéder de manière appropriée pour déterminer les fonctionnalités d’UE-V que vous déploierez. Par conséquent, si vous quittez cette page, assurez-vous de revenir en revue les informations de planification ci-dessous.

-   [Déployer les fonctionnalités UE-V2.x requises](deploy-required-features-for-ue-v-2x-new-uevv2.md)

    Chaque déploiement d’UE-V nécessite les activités suivantes:

    -   [Définir un emplacement de stockage des paramètres](https://technet.microsoft.com/library/dn458891.aspx#ssl)

    -   [Décider du déploiement de l’agent UE-V et de la gestion des configurations UE-V](https://technet.microsoft.com/library/dn458891.aspx#config)

    -   [Installer l’agent UE-V](https://technet.microsoft.com/library/dn458891.aspx#agent) sur tous les ordinateurs des utilisateurs qui ont besoin de la synchronisation des paramètres

-   Vous pouvez également [déployer UE-V 2. x pour des applications personnalisées.](deploy-ue-v-2x-for-custom-applications-new-uevv2.md)

    La planification vous aidera à déterminer si vous souhaitez que UE-V prenne en charge la synchronisation des paramètres d’applications personnalisées (tiers ou métier), qui nécessitent ces fonctionnalités d’UE-V.

    -   [Installer le générateur de UEV](https://technet.microsoft.com/library/dn458942.aspx#uevgen) pour créer, modifier et valider les modèles d’emplacement des paramètres personnalisés requis pour synchroniser les paramètres d’application personnalisés

    -   [Créer des modèles d’emplacement de paramètres personnalisés](https://technet.microsoft.com/library/dn458942.aspx#createcustomtemplates) à l’aide du générateur UE-V

    -   [Déployer un catalogue de modèles de paramètres UE-V](https://technet.microsoft.com/library/dn458942.aspx#deploycatalogue) qui vous permet de stocker vos modèles d’emplacement des paramètres personnalisés

Ce diagramme de flux de travail fournit une connaissance de haut niveau d’un déploiement UE-V et des décisions qui déterminent le mode de déploiement d’UE-V au sein de votre entreprise.

![deploymentworkflow](images/deploymentworkflow.png)

**Planification d’un déploiement UE-V:** Tout d’abord, vous souhaiterez peut-être effectuer un léger déploiement pour déterminer les composants UE-V que vous déploierez. La planification d’un déploiement UE-V implique les éléments suivants:

-   [Choisir de synchroniser les paramètres des applications personnalisées](#deciding)

    Cela détermine si vous allez installer le générateur UE-V lors du déploiement, ce qui vous permet de créer des modèles d’emplacement des paramètres personnalisés. Ce service implique les éléments suivants:

    Passez en revue les [paramètres qui sont synchronisés automatiquement dans un déploiement UE-V](#autosyncsettings).

    [Déterminez si vous avez besoin que les paramètres soient synchronisés pour les autres applications](#determinesettingssync).

-   Passez en revue [d’autres considérations relatives au déploiement d’UE-V](#considerations), comme la haute disponibilité et la planification de la capacité.

-   [Confirmer les conditions préalables et les configurations prises en charge pour UE-V](#prereqs)

## <a href="" id="deciding"></a>Choisir de synchroniser les paramètres des applications personnalisées


Dans un déploiement UE-V, de nombreux paramètres sont synchronisés automatiquement. Toutefois, vous pouvez également personnaliser UE-V pour synchroniser les paramètres d’autres applications, telles que les applications métier et les applications tierces.

Le fait de décider d’utiliser UE-V pour synchroniser les paramètres des applications personnalisées est probablement la partie la plus importante de la planification de votre déploiement d’UE-V. Les rubriques de cette section vous aideront à prendre cette décision.

### <a href="" id="autosyncsettings"></a>Paramètres synchronisés automatiquement dans un déploiement UE-V

Cette section fournit des informations sur les paramètres qui sont synchronisés par défaut dans UE-V, notamment les suivants:

Applications de bureau dont les paramètres sont synchronisés par défaut

Paramètres de bureau Windows qui sont synchronisés par défaut

Une déclaration de prise en charge de la synchronisation des paramètres d’application Windows

Pour plus d’aide sur les paramètres de Microsoft Office 2013, Microsoft Office 2010 et Microsoft Office 2007 qui sont synchronisés avec UE-V, voir modèles d’utilisation de l' [interface utilisateur (UE-v)](https://www.microsoft.com/download/details.aspx?id=46367) .

### Applications de bureau synchronisées par défaut dans UE-V 2,1 et UE-V 2,1 SP1

Lorsque vous installez l’agent UE-V 2,1 ou 2,1 SP1, il inscrit un groupe par défaut de modèles d’emplacement des paramètres qui capture les valeurs de paramètres pour ces applications Microsoft courantes.

**Astuce**  
**Synchronisation des paramètres de Microsoft Office 2007** -dans UE-V 2,1 et 2,1 SP1, un modèle d’emplacement des paramètres n’est plus inclus par défaut pour les applications Office 2007. Toutefois, vous pouvez toujours utiliser les modèles Office 2007 d’UE-V 2,0 ou une version antérieure et télécharger les modèles à partir de la [Galerie de modèles UE-v](https://go.microsoft.com/fwlink/p/?LinkID=246589).



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
<td align="left"><p>Applications Microsoft Office 2010</p>
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
<td align="left"><p>Applications Microsoft Office 2013</p>
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
<p>Centre de téléchargement Microsoft Office 2013</p>
<p>Microsoft OneDrive entreprise 2013</p>
<p>Les modèles d’emplacement des paramètres d’UE-V 2,1 et 2,1 SP1 de Microsoft Office 2013 incluent une prise en charge améliorée des signatures Outlook. Nous avons ajouté la synchronisation des paramètres de signature par défaut pour les courriers électroniques, les réponses et les transferts.</p>
<div class="alert">
<strong>Remarque</strong><br/><p>Un profil Outlook doit être créé pour tout appareil sur lequel un utilisateur souhaite synchroniser sa signature Outlook. Si ce n’est pas le cas, l’utilisateur peut en créer un, puis redémarrer Outlook sur cet appareil pour activer la synchronisation des signatures.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>Options du navigateur: Internet Explorer 8, Internet Explorer 9, Internet Explorer 10 et Internet Explorer 11</p></td>
<td align="left"><p>Favoris, page d’accueil, onglets et barres d’outils.</p>
<div class="alert">
<strong>Remarque</strong><br/><p>UE-V n’utilise pas les paramètres d’itinérance pour les cookies Internet Explorer.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Accessoires Windows</p></td>
<td align="left"><p>Microsoft Calculator, bloc-notes, WordPad.</p></td>
</tr>
</tbody>
</table>



**Remarque**  
UE-V 2,1 SP1 ne synchronise pas les paramètres entre Microsoft Calculator dans Windows 10 et Microsoft Calculator dans les systèmes d’exploitation précédents.



### Applications de bureau synchronisées par défaut dans UE-V 2,0

Lors de l’installation de l’agent UE-V 2,0, il inscrit un groupe par défaut de modèles d’emplacement des paramètres qui capturent les valeurs de paramètres pour ces applications Microsoft courantes.

**Astuce**  
**Synchronisation des paramètres de Microsoft Office 2013** -dans UE-V 2,0, un modèle d’emplacement des paramètres n’est pas inclus par défaut pour les applications Office 2013, mais il est disponible en téléchargement à partir de la [Galerie de modèles UE-v](https://go.microsoft.com/fwlink/p/?LinkID=246589). La [synchronisation d’Office 2013 avec UE-V 2,0](synchronizing-office-2013-with-ue-v-20-both-uevv2.md) fournit des détails sur les modèles pris en charge permettant de synchroniser les paramètres d’Office 2013.



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
<td align="left"><p>Applications Microsoft Office 2007</p>
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
<td align="left"><p>Applications Microsoft Office 2010</p>
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
<td align="left"><p>Options du navigateur: Internet Explorer 8, Internet Explorer 9 et Internet Explorer 10</p></td>
<td align="left"><p>Favoris, page d’accueil, onglets et barres d’outils.</p>
<div class="alert">
<strong>Remarque</strong><br/><p>UE-V n’utilise pas les paramètres d’itinérance pour les cookies Internet Explorer.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Accessoires Windows</p></td>
<td align="left"><p>Microsoft Calculator, bloc-notes, WordPad.</p></td>
</tr>
</tbody>
</table>



### <a href="" id="autosyncsettings2"></a>Paramètres Windows synchronisés par défaut

UE-V inclut des modèles d’emplacement des paramètres qui capturent les valeurs des paramètres de ces paramètres Windows.

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
<th align="left">Appliquer le</th>
<th align="left">Exporter sur</th>
<th align="left">État par défaut</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Arrière-plan du Bureau</p></td>
<td align="left"><p>Arrière-plan ou papier peint actuellement actif.</p></td>
<td align="left"><p>Connexion, déverrouiller, connexion à distance, événements de tâche planifiés.</p></td>
<td align="left"><p>Déconnexion, verrouillage, disconnexion distante, utilisateur cliquant sur <strong> Synchroniser maintenant </strong> dans le centre de paramètres de l’entreprise ou intervalle de tâches planifiées</p></td>
<td align="left"><p>Activé</p></td>
</tr>
<tr class="even">
<td align="left"><p>Options d’ergonomie</p></td>
<td align="left"><p>Paramètres d’accessibilité et d’entrée, loupe Microsoft, narrateur et clavier visuel.</p></td>
<td align="left"><p>Connexion uniquement.</p></td>
<td align="left"><p>Fermer la session, un utilisateur clique sur <strong> Synchroniser maintenant </strong> dans le centre de paramètres de l’entreprise ou intervalle de tâches planifiées</p></td>
<td align="left"><p>Activé</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Paramètres de bureau</p></td>
<td align="left"><p>Paramètres du menu Démarrer et de la barre des tâches, options des dossiers, icônes du bureau par défaut, horloges supplémentaires et paramètres régionaux et linguistiques.</p></td>
<td align="left"><p>Connexion uniquement.</p></td>
<td align="left"><p>Fermer la session, un utilisateur clique sur <strong> Synchroniser maintenant </strong> dans le centre de paramètres d’une entreprise ou une tâche planifiée</p></td>
<td align="left"><p>Activé</p></td>
</tr>
</tbody>
</table>



**Remarque**  
À partir de Windows 8, UE-V n’itinérance pas les paramètres liés à l’écran d’accueil, tels que les éléments et les emplacements. Par ailleurs, UE-V ne prend pas en charge la synchronisation des éléments de la barre des tâches épinglés ou des raccourcis vers les fichiers Windows.



**Important**  
UE-V 2,1 SP1 répartir les paramètres de la barre des tâches entre les appareils Windows 10. Toutefois, UE-V ne synchronise pas les paramètres de la barre des tâches entre les appareils et appareils Windows 10 exécutant d’anciens systèmes d’exploitation.



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
<th align="left">Collecte</th>
<th align="left">Appliquer</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Paramètres de l’application</strong></p></td>
<td align="left"><p>Applications Windows  </p></td>
<td align="left"><p>Fermer l’application</p>
<p>Événement de modification des paramètres d’application Windows</p></td>
<td align="left"><p>Démarrer le moniteur d’application UE-V au démarrage</p>
<p>Ouvrir l’application</p>
<p>Événement de modification des paramètres d’application Windows</p>
<p>Arrivée d’un package de paramètres</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p>Applications de bureau</p></td>
<td align="left"><p>Application se ferme</p></td>
<td align="left"><p>L’application s’ouvre et se ferme</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Paramètres de bureau</strong></p></td>
<td align="left"><p>Arrière-plan du Bureau</p></td>
<td align="left"><p>Verrouiller ou déconnecter</p></td>
<td align="left"><p>Connexion, déverrouiller, connexion à distance, notification de nouvelle réception de package, l’utilisateur clique sur <strong> Synchroniser maintenant </strong> dans le centre de paramètres de l’entreprise ou la tâche planifiée s’exécute.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p>Options d’ergonomie (standard: accessibilité, narrateur, loupe, clavier visuel)</p></td>
<td align="left"><p>Verrouiller ou déconnecter</p></td>
<td align="left"><p>Accès</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p>Facilité d’accès (interpréteur audio, accessibilité, clavier, souris)</p></td>
<td align="left"><p>Verrouiller ou déconnecter</p></td>
<td align="left"><p>Connexion, déverrouiller, connexion à distance, notification de nouvelle réception de package, utilisateur clique sur <strong> Synchroniser maintenant </strong> dans le centre de paramètres de l’entreprise ou exécution d’une tâche planifiée</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p>Paramètres de bureau</p></td>
<td align="left"><p>Verrouiller ou déconnecter</p></td>
<td align="left"><p>Accès</p></td>
</tr>
</tbody>
</table>



### UE-V-support pour les applications Windows

Pour les applications Windows, le développeur de l’application spécifie les paramètres qui sont synchronisés. Vous pouvez spécifier les applications Windows activées pour la synchronisation des paramètres.

Pour afficher une liste des applications Windows qui peuvent synchroniser les paramètres sur un ordinateur dont le nom de la famille de packages, le statut activée et la source activée, à l’invite de commandes Windows PowerShell, entrez: `Get-UevAppxPackage`

**Remarque**  
Depuis Windows 8, UE-V ne synchronise pas les paramètres de l’application Windows si l’utilisateur du domaine associe les informations d’identification de connexion à son compte Microsoft. Ce lien permet de synchroniser les paramètres avec Microsoft OneDrive pour UE-V, qui désactive la synchronisation des paramètres d’application Windows.



### UE-V-support pour les imprimantes itinérantes

UE-V 2,1 SP1 permet aux imprimantes réseau d’avoir accès aux périphériques de sorte que l’utilisateur ait accès à ses imprimantes réseau lorsqu’il est connecté à un appareil du réseau. Cela comprend l’itinérance de l’imprimante définie par défaut.

L’itinérance d’imprimantes dans UE-V nécessite l’un des scénarios suivants:

-   Le serveur d’impression peut télécharger le pilote requis lorsqu’il est itinérant vers un nouvel appareil.

-   Le pilote de l’imprimante du réseau errant est préinstallé sur n’importe quel appareil qui a besoin d’accéder à cette imprimante réseau.

-   Le pilote de l’imprimante peut être obtenu à partir de Windows Update.

**Remarque**  
La fonctionnalité d’itinérance d’imprimante UE-V n’effectue **pas** de paramètres d’impression ou de préférences tels que l’impression recto verso.



### <a href="" id="determinesettingssync"></a>Déterminer si vous avez besoin des paramètres synchronisés pour d’autres applications

Une fois que vous avez examiné les paramètres qui sont synchronisés automatiquement dans le déploiement d’UE-V, vous pouvez choisir de synchroniser les paramètres d’autres applications, car cela détermine le mode de déploiement d’UE-V au sein de votre entreprise.

En tant qu’administrateur, lorsque vous considérez les applications de bureau à inclure dans votre solution UE-V, considérez les paramètres qui peuvent être personnalisés par les utilisateurs, la façon dont l’application stocke les paramètres correspondants. Certaines applications de bureau ne disposent pas de paramètres qui peuvent être personnalisés ou personnalisés de façon régulière par les utilisateurs. De plus, tous les paramètres des applications de bureau ne peuvent pas être synchronisés en toute sécurité sur plusieurs ordinateurs ou environnements.

En règle générale, vous pouvez synchroniser les paramètres qui répondent aux critères suivants:

-   Paramètres stockés dans des emplacements accessibles aux utilisateurs. Par exemple, ne synchronisez pas les paramètres stockés dans system32 ou en dehors de la section HKEY \ _CURRENT \ _USER (HKCU) du Registre.

-   Paramètres qui ne sont pas propres à l’ordinateur en particulier. Par exemple, excluez les configurations réseau ou matérielles.

-   Paramètres qui peuvent être synchronisés entre ordinateurs sans risque de corruption de données. Par exemple, n’utilisez pas de paramètres stockés dans un fichier de base de données.

### <a href="" id="checklistsettingssync"></a>Liste de vérification relative à l’évaluation d’applications personnalisées

Si vous avez décidé de synchroniser les paramètres d’autres applications, vous pouvez utiliser cette liste de vérification pour déterminer les applications que vous incluez.

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
<td align="left"><p>Cette application contient-elle des paramètres que l’utilisateur peut personnaliser?</p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Est-il important pour l’utilisateur de synchroniser ces paramètres?</p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Ces paramètres utilisateur sont-ils déjà gérés par une solution de gestion des applications ou de stratégie de paramètres? UE-V applique les paramètres d’application au démarrage de l’application et aux paramètres Windows à l’ouverture de session, le déverrouillage ou la connexion à distance. Si vous utilisez UE-V avec d’autres paramètres de partage de solutions, les utilisateurs peuvent rencontrer des incohérences entre les paramètres synchronisés.</p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Les paramètres de l’application sont-ils spécifiques de votre ordinateur? Les préférences et personnalisations apportées aux applications qui sont associées à des configurations matérielles ou spécifiques à des ordinateurs ne sont pas synchronisées uniformément entre les sessions et peuvent entraîner une mauvaise application de l’application.</p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Est-ce que les paramètres du Windows Store se trouvent dans le dossier Program Files ou dans le répertoire de fichiers qui se trouve dans le répertoire <strong> utilisateurs </strong> [nom d’utilisateur] &lt; Strong &gt; </strong> &lt; &gt; LocalLow </strong> Annuaire fort? Les données d’application stockées dans l’un de ces emplacements ne doivent généralement pas être synchronisées avec l’utilisateur, dans la mesure où ces données sont spécifiques de l’ordinateur ou que les données sont trop volumineuses pour être synchronisées.</p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>L’application stocke-t-elle des paramètres dans un fichier qui contient d’autres données d’application qui ne doivent pas être synchronisées? UE-V synchronise les fichiers comme une seule unité. Si les paramètres sont stockés dans des fichiers qui incluent des données d’application autres que des paramètres, la synchronisation de ces données supplémentaires peut entraîner une médiocre application.</p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Quelle est la taille des fichiers contenant les paramètres? Les performances de la synchronisation des paramètres peuvent être affectées par de gros fichiers. L’inclusion de fichiers volumineux peut affecter les performances de la synchronisation des paramètres.</p></td>
</tr>
</tbody>
</table>



## <a href="" id="considerations"></a>Autres considérations relatives à la préparation d’un déploiement UE-V


Vous devez également tenir compte des éléments suivants lorsque vous préparez le déploiement d’UE-V:

-   [Gestion de la synchronisation des informations d’identification](#creds)

-   [Synchronisation des paramètres d’application Windows](#appxsettings)

-   [Modèles d’emplacement des paramètres d’UE-V personnalisés](#custom)

-   [Configurations involontaires des paramètres utilisateur](#prevent)

-   [Performances et capacités](#capacity)

-   [Haute disponibilité](#high)

-   [Synchronisation de l’horloge de l’ordinateur](#clocksync)

### <a href="" id="creds"></a>Gestion de la synchronisation des informations d’identification dans UE-V 2,1 et UE-V 2,1 SP1

Dans de nombreuses applications d’entreprise, notamment Microsoft Outlook et Lync, invitez les utilisateurs à entrer leurs informations d’identification de domaine au moment de la connexion. Les utilisateurs ont la possibilité d’enregistrer leurs informations d’identification sur le disque pour éviter d’avoir à les entrer à chaque ouverture de ces applications. L’activation de la synchronisation des informations d’identification d’itinérance permet aux utilisateurs d’enregistrer leurs informations d’identification sur un ordinateur et de ne pas les retaper sur chaque ordinateur qu’ils utilisent dans leur environnement. Les utilisateurs peuvent synchroniser certaines informations d’identification de domaine avec UE-V 2,1 et 2,1 SP1.

**Important**  
La synchronisation des informations d’identification est désactivée par défaut. Pour implémenter cette fonctionnalité, vous devez activer la synchronisation des informations d’identification de manière explicite lors du déploiement.



UE-V 2,1 et 2,1 SP1 peuvent synchroniser les informations d’identification d’entreprise, mais pas les informations d’identification destinées à être utilisées uniquement sur l’ordinateur local.

Les informations d’identification sont des paramètres synchrones, ce qui signifie qu’elles s’appliquent à votre profil la première fois que vous vous connectez à votre ordinateur après la synchronisation d’UE-V.

La synchronisation des informations d’identification est gérée par son propre modèle d’emplacement des paramètres, qui est désactivé par défaut. Vous pouvez activer ou désactiver ce modèle par le biais des méthodes utilisées pour les autres modèles. L’identificateur de modèle de cette fonctionnalité est RoamingCredentialSettings.

**Important**  
Si vous utilisez l’itinérance d’informations d’identification Active Directory dans votre environnement, nous vous recommandons de ne pas activer le modèle d’itinérance d’informations d’identification d’UE-V.



Pour activer la synchronisation des informations d’identification, utilisez l’une des méthodes suivantes:

-   Centre de paramètres de la société

-   PowerShell

-   Stratégie de groupe

**Remarque**  
Les informations d’identification sont chiffrées lors de la synchronisation.



[Centre de paramètres de l’entreprise](https://technet.microsoft.com/library/dn458903.aspx)**:** activez la case à cocher paramètres d’informations d’identification d’itinérance sous Paramètres Windows pour activer la synchronisation des informations d’identification. Décochez la case pour la désactiver. Cette case à cocher apparaît dans le centre de paramètres de la société uniquement si votre compte n’est pas configuré pour synchroniser les paramètres à l’aide d’un compte Microsoft.

[PowerShell](https://technet.microsoft.com/library/dn458937.aspx)**:** cette applet de méthode PowerShell autorise la synchronisation des informations d’identification:

``` syntax
Enable-UevTemplate RoamingCredentialSettings
```

Cette applet de connexion PowerShell désactive la synchronisation des informations d’identification:

``` syntax
Disable-UevTemplate RoamingCredentialSettings
```

[Stratégie de groupe](https://technet.microsoft.com/library/dn458893.aspx)**:** vous devez [déployer le dernier modèle ADMX MDOP](https://go.microsoft.com/fwlink/p/?LinkId=393944) pour activer la synchronisation des informations d’identification via une stratégie de groupe. La synchronisation des informations d’identification est gérée à l’aide des paramètres Windows. Pour gérer cette fonctionnalité avec une stratégie de groupe, activez la stratégie de synchronisation des paramètres Windows.

1.  Ouvrez l’éditeur de stratégies de groupe et naviguez jusqu’à **Configuration utilisateur-modèles d’administration-Composants Windows-virtualisation**de l’utilisation de Microsoft.

2.  Double-cliquez sur **synchroniser les paramètres Windows**.

3.  Si cette stratégie est activée, vous pouvez activer la synchronisation des informations d’identification en activant la case à cocher **informations d’identification d’itinérance** , ou désactiver la synchronisation des informations d’identification en la désactivant.

4.  Cliquez sur **OK**.

### Emplacement des informations d’identification synchronisées par UE-V

Les fichiers d’informations d’identification enregistrés par les applications dans les emplacements suivants sont synchronisés:

-   %UserProfile%\\AppData\\Roaming\\Microsoft\\Credentials\\

-   %UserProfile%\\AppData\\Roaming\\Microsoft\\Crypto\\

-   %UserProfile%\\AppData\\Roaming\\Microsoft\\Protect\\

-   %UserProfile%\\AppData\\Roaming\\Microsoft\\SystemCertificates\\

Les informations d’identification enregistrées dans d’autres emplacements ne sont pas synchronisées par UE-V.

### <a href="" id="appxsettings"></a>Synchronisation des paramètres d’application Windows

UE-V gère la synchronisation des paramètres d’application Windows de trois manières:

-   **Synchroniser les applications Windows:** Autoriser ou refuser une synchronisation d’applications Windows

-   **Liste des applications Windows:** Synchroniser une liste d’applications Windows

-   **Comportement de synchronisation par défaut non répertorié:** Déterminez le comportement de synchronisation des applications Windows qui ne figurent pas dans la liste des applications Windows.

Pour plus d’informations, consultez la [liste des applications Windows](https://technet.microsoft.com/library/dn458925.aspx#win8applist).

### <a href="" id="custom"></a>Modèles d’emplacement des paramètres d’UE-V personnalisés

Si vous déployez UE-V pour synchroniser les paramètres des applications personnalisées, vous devez utiliser le générateur UE-V pour créer des modèles d’emplacement des paramètres personnalisés pour ces applications de bureau. Après avoir créé et testé un modèle d’emplacement des paramètres personnalisés dans un environnement de test, vous pouvez déployer les modèles d’emplacement des paramètres sur les ordinateurs de l’entreprise.

Les modèles d’emplacement des paramètres personnalisés doivent être déployés avec une infrastructure de déploiement existante (par exemple, une méthode de distribution de logiciels d’entreprise) telle que System Center Configuration Manager, des préférences ou en configurant un catalogue de modèles de paramètres UE-V. Les modèles déployés à l’aide de Configuration Manager ou d’une stratégie de groupe doivent être enregistrés à l’aide d’UE-V WMI ou de Windows PowerShell.

Pour plus d’informations sur les modèles d’emplacement des paramètres personnalisés, voir [déployer UE-V 2. x pour des applications personnalisées](deploy-ue-v-2x-for-custom-applications-new-uevv2.md). Pour plus d’informations sur l’utilisation de UE-V avec Configuration Manager, voir [configuration d’UE-v 2. x avec System Center Configuration manager 2012](configuring-ue-v-2x-with-system-center-configuration-manager-2012-both-uevv2.md).

### <a href="" id="prevent"></a>Empêcher la configuration involontaire des paramètres utilisateur

UE-V télécharge les nouvelles informations de paramètres utilisateur à partir d’un emplacement de stockage des paramètres et applique les paramètres à l’ordinateur local dans les cas suivants:

-   Chaque fois qu’une application est démarrée et dispose d’un modèle UE-V enregistré.

-   Lorsqu’un utilisateur ouvre une session sur un ordinateur.

-   Lorsqu’un utilisateur déverrouille un ordinateur.

-   Lorsqu’une connexion est établie à un ordinateur de bureau distant sur lequel UE-V est installé.

-   Lors de l’exécution de la tâche planifiée du contrôleur de synchronisation.

Si UE-V est installé sur l’ordinateur A et l’ordinateur B et les paramètres que vous voulez pour l’application se trouvent sur l’ordinateur A, l’ordinateur a doit d’abord ouvrir et fermer l’application. Si l’application est ouverte et fermée sur l’ordinateur B, vous devez d’abord les paramètres de l’application sur l’ordinateur A configurés sur les paramètres de l’application sur l’ordinateur B. les paramètres sont synchronisés entre les ordinateurs en fonction de chaque application. Dans le temps, les paramètres deviennent cohérents entre les ordinateurs tels qu’ils sont ouverts et fermés grâce aux paramètres préférés.

Ce scénario s’applique également aux paramètres Windows. Si les paramètres Windows sur l’ordinateur B doivent être identiques aux paramètres Windows sur l’ordinateur A, l’utilisateur doit se connecter et se déconnecter de l’ordinateur A.

Si les paramètres utilisateur que l’utilisateur souhaite appliquer dans un ordre incorrect, ils peuvent être récupérés en effectuant une opération de restauration pour la configuration de l’application ou de Windows spécifique sur l’ordinateur sur lequel les paramètres ont été écrasés. Pour plus d’informations, reportez-vous à [gérer la sauvegarde et la restauration d’administration dans UE-V 2. x](manage-administrative-backup-and-restore-in-ue-v-2x-new-topic-for-21.md).

### <a href="" id="capacity"></a>Planification des performances et de la capacité

Spécifiez vos exigences pour UE-V avec la capacité de disque standard et la surveillance de l’état du réseau.

UE-V utilise un partage SMB (Server Message Block) pour le stockage des packages de paramètres. La taille des packages varie en fonction des informations de configuration de chaque application. Bien que la plupart des packages de paramètres soient petits, la synchronisation de fichiers potentiellement volumineux, tels que les images de bureau, peut entraîner une médiocre performance, en particulier sur les réseaux plus lents.

Pour réduire les problèmes liés à la latence du réseau, créez des emplacements de stockage des paramètres sur les mêmes réseaux locaux où résident les ordinateurs des utilisateurs. Nous vous recommandons d’utiliser 20 Mo d’espace disque par utilisateur pour l’emplacement de stockage des paramètres.

Par défaut, la synchronisation UE-V a expiré après 2 secondes pour éviter un décalage excessif en raison d’un grand nombre de packages de paramètres volumineux. Vous pouvez configurer le paramètre PowerSchool = SyncProvider à l’aide d' [objets de stratégie de groupe](https://technet.microsoft.com/library/dn458893.aspx).

### <a href="" id="high"></a>Haute disponibilité pour UE-V

L’emplacement de stockage des paramètres d’UE-V et le catalogue de modèles de paramètres prennent en charge le stockage des données utilisateur sur tout partage accessible en écriture. Pour garantir une haute disponibilité, utilisez les critères suivants:

-   Mettre en forme le volume de stockage à l’aide d’un système de fichiers NTFS;

-   Le partage peut utiliser le système de fichiers DFS, mais il existe des restrictions.
Plus précisément, la configuration de cible unique de réplication de systèmes de fichiers DFS avec ou sans espace de noms DFS-N) est prise en charge.
De même, seule une configuration de cible unique est prise en charge avec le système de fichiers DFS-N.
Pour plus d’informations, consultez [l’énoncé de support de Microsoft relatif aux données de profil utilisateur répliquées](https://go.microsoft.com/fwlink/p/?LinkId=313991) ainsi que des [informations sur la politique de support Microsoft pour un scénario de déploiement DFS-R et DFS-N](https://support.microsoft.com/kb/2533009).

    Par ailleurs, dans la mesure où SYSVOL utilise le système de fichiers DFS-R pour la réplication, SYSVOL ne peut pas être utilisé pour la réplication de fichier de données UE-V.

-   Configurez les autorisations de partage et les listes de contrôle d’accès NTFS (ACL) comme indiqué dans [la section déploiement de l’emplacement de stockage des paramètres pour UE-V 2. x](https://technet.microsoft.com/library/dn458891.aspx#ssl).

-   Utilisez la fonction de regroupement de serveurs de fichiers avec l’agent UE-V pour donner accès à des copies de données d’état utilisateur en cas d’échec des communications.

-   Vous pouvez stocker les paramètres de données de chemin de stockage de paramètres (données utilisateur) et de modèles de catalogue de modèles sur les partages groupés, sur les partages DFS-N, ou sur les deux.

### <a href="" id="clocksync"></a>Synchroniser les horloges de l’ordinateur pour la synchronisation des paramètres d’UE-V

Les ordinateurs qui exécutent l’agent UE-V doivent utiliser un serveur de temps pour garantir une utilisation homogène des paramètres. UE-V utilise des horodatages pour déterminer si les paramètres doivent être synchronisés à partir de l’emplacement de stockage des paramètres. Si l’horloge de l’ordinateur est incorrecte, les paramètres plus anciens peuvent remplacer les paramètres plus récents, ou les nouveaux paramètres peuvent ne pas être enregistrés dans l’emplacement de stockage des paramètres.

## <a href="" id="prereqs"></a>Confirmer les conditions préalables et les configurations prises en charge pour UE-V


Avant de continuer, assurez-vous que votre environnement inclut les exigences requises pour exécuter UE-V.

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
<td align="left"><p>Windows7</p></td>
<td align="left"><p>Edition intégrale, entreprise ou édition professionnelle</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>32bits ou 64bits</p></td>
<td align="left"><p>Windows PowerShell 3,0 ou version ultérieure</p></td>
<td align="left"><p>.NET Framework 4,5 ou version ultérieure pour UE-V 2,1.</p>
<p>.NET Framework 4 ou version ultérieure pour UE-V 2,0.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008R2</p></td>
<td align="left"><p>Standard, entreprise, Datacenter ou serveur Web</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64 bits</p></td>
<td align="left"><p>Windows PowerShell 3,0 ou version ultérieure</p></td>
<td align="left"><p>.NET Framework 4,5 ou version ultérieure pour UE-V 2,1.</p>
<p>.NET Framework 4 ou version ultérieure pour UE-V 2,0.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows 8 et Windows 8,1</p></td>
<td align="left"><p>Entreprise ou professionnel</p></td>
<td align="left"><p>None</p></td>
<td align="left"><p>32bits ou 64bits</p></td>
<td align="left"><p>Windows PowerShell 3,0 ou version ultérieure</p></td>
<td align="left"><p>.NET Framework 4,5 ou version ultérieure</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 10, version pré-1607</p>
<div class="alert">
<strong>Remarque</strong><br/><p>Seule UE-V 2,1 SP1 prend en charge Windows 10, version antérieure-1607</p>
</div>
<div>

</div></td>
<td align="left"><p>Entreprise ou professionnel</p></td>
<td align="left"><p>None</p></td>
<td align="left"><p>32bits ou 64bits</p></td>
<td align="left"><p>Windows PowerShell 3,0 ou version ultérieure</p></td>
<td align="left"><p>.NET Framework 4.6</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2012 et Windows Server 2012 R2</p></td>
<td align="left"><p>Standard ou Datacenter</p></td>
<td align="left"><p>None</p></td>
<td align="left"><p>64 bits</p></td>
<td align="left"><p>Windows PowerShell 3,0 ou version ultérieure</p></td>
<td align="left"><p>.NET Framework 4,5 ou version ultérieure</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2016</p></td>
<td align="left"><p>Standard ou Datacenter</p></td>
<td align="left"><p>None</p></td>
<td align="left"><p>64 bits</p></td>
<td align="left"><p>Windows PowerShell 3,0 ou version ultérieure</p></td>
<td align="left"><p>.NET Framework 4,6 ou version ultérieure</p></td>
</tr>
</tbody>
</table>



En outre...

-   **Licence MDOP:** Cette technologie fait partie du pack d’optimisation de bureau Microsoft (MDOP). Les clients d’entreprise peuvent obtenir MDOP avec Microsoft Software Assurance. Pour plus d’informations sur le programme d’assurance logiciel Microsoft et sur l’acquisition de MDOP, voir comment obtenir MDOP ( https://go.microsoft.com/fwlink/p/?LinkId=322049) .

-   **Informations d’identification d’administration** pour les ordinateurs sur lesquels vous allez procéder à l’installation

**Remarque**  

-   À partir de WIndows 10, la version 1607, UE-V est incluse dans [Windows 10 pour les entreprises](https://www.microsoft.com/WindowsForBusiness/windows-for-enterprise) et ne fait plus partie du pack d’optimisation de bureau Microsoft.

-   Dans le cadre de l’activation de .NET Framework 4 ou d’une version ultérieure 3,0, vous devez activer l’option Windows PowerShell d’UE-V de l’agent UE-V. Téléchargez Windows PowerShell 3,0 [ici](https://go.microsoft.com/fwlink/?LinkId=309609).

-   Installez .NET Framework 4 ou .NET Framework 4,5 sur les ordinateurs exécutant Windows 7 ou le système d’exploitation Windows Server 2008 R2. .NET Framework 4,5 est fourni avec les systèmes d’exploitation Windows 8, Windows 8,1 et Windows Server 2012. Le système d’exploitation Windows 10 est fourni avec .NET Framework 4,6 installé.
-   La stratégie «supprimer le cache d’itinérance» pour les profils obligatoires n’est pas prise en charge avec UE-V et ne doit pas être utilisée.



Il n’existe aucune configuration spéciale de RAM (Random Access Memory) spécifique à UE-V.

### Synchronisation des paramètres via le fournisseur de synchronisation

Le fournisseur de synchronisation est le paramètre par défaut pour les utilisateurs qui synchronise un cache local avec l’emplacement de stockage des paramètres dans les cas suivants:

-   Connexion/déconnexion

-   Verrouillez/Déverrouillez

-   Connexion/déconnexion Bureau à distance

-   Ouvrir/fermer l’application

Une tâche planifiée gère cette synchronisation des paramètres toutes les 30 minutes ou par le biais de certains événements de déclencheurs pour certaines applications. Pour plus d’informations, reportez-vous à [modification de la fréquence des tâches planifiées UE-V 2.](changing-the-frequency-of-ue-v-2x-scheduled-tasks-both-uevv2.md)

L’agent UE-V synchronise les paramètres utilisateur pour les ordinateurs qui ne sont pas toujours connectés au réseau d’entreprise (ordinateurs distants et portables) et ceux qui sont toujours connectés au réseau (ordinateurs qui exécutent Windows Server et des sessions VDI (Virtual Desktop interface).

**Synchronisation pour les ordinateurs disposant de connexions toujours disponibles:** Lorsque vous utilisez UE-V sur des ordinateurs qui sont toujours connectés au réseau, vous devez configurer l’agent UE-V pour synchroniser les paramètres à l’aide du paramètre *PowerSchool = None* , qui traite le serveur de stockage des paramètres comme un partage réseau standard. Dans cette configuration, l’agent UE-V peut être configuré pour notifier si l’importation des paramètres d’application est retardée.

Activez cette configuration en utilisant l’une des méthodes suivantes:

-   Lors de l’installation d’UE-V, à l’invite de commandes ou dans un fichier de commandes, définissez le paramètre AgentSetup.exe *PowerSchool = aucun*. [Le déploiement de l’agent UE-V 2. x](https://technet.microsoft.com/library/dn458891.aspx#agent) fournit des informations supplémentaires.

-   Après l’installation d’UE-V, utilisez la fonctionnalité de gestion des paramètres de System Center 2012 Configuration Manager ou des modèles ADMX MDOP pour pousser la configuration *PowerSchool = aucune* .

-   Utilisez Windows PowerShell ou WMI (Windows Management Instrumentation) pour définir la configuration *PowerSchool = aucune* .

    **Remarque**  
    Ces deux dernières méthodes ne fonctionnent pas pour les environnements VDI (Virtual Desktop Infrastructure) en pool.



Vous devez redémarrer votre ordinateur pour que les paramètres commencent à être synchronisés.

**Remarque**  
Si vous définissez *PowerSchool = aucun*, les modifications apportées aux paramètres sont enregistrées directement sur le serveur. S’il n’y a pas de connexion réseau au chemin de stockage des paramètres, les modifications apportées aux paramètres sont mises en cache sur l’appareil et sont synchronisées lors de la prochaine exécution du fournisseur de synchronisation. Si le chemin d’accès de stockage des paramètres est introuvable et que le profil utilisateur est supprimé d’un environnement VDI en pool lors de la déconnexion, les modifications apportées aux paramètres sont perdues et l’utilisateur doit réappliquer la modification lors de la reconnexion de l’ordinateur au chemin de stockage des paramètres.



**Synchronisation pour les moteurs de synchronisation externes:** Le paramètre *PowerSchool = externe* spécifie que, si les paramètres UE-V sont écrits dans un dossier local sur l’ordinateur de l’utilisateur, tout moteur de synchronisation externe (par exemple, OneDrive entreprise, dossiers de travail, SharePoint ou Dropbox) peut être utilisé pour appliquer ces paramètres aux différents ordinateurs auxquels les utilisateurs accèdent.

**Support pour les sessions VDI partagées:** UE-V 2,1 et 2,1 SP1 fournissent la prise en charge des sessions VDI partagées entre les utilisateurs finaux. Vous pouvez enregistrer et configurer un modèle d’infrastructure VDI spéciale, qui garantit que UE-V conserve toutes ses fonctionnalités intactes pour les sessions VDI non persistantes.

**Remarque**  
Si vous n’activez pas le mode VDI pour les sessions VDI non persistantes, il est possible que certaines fonctionnalités ne fonctionnent pas, telles que [sauvegarde et restauration et dernière bonne qualité connue (LKG)](https://technet.microsoft.com/library/dn878331.aspx).



Le modèle VDI est fourni avec UE-V 2,1 et 2,1 SP1 et est en général disponible ici après l’installation: C:\\Program Files\\Microsoft user interface Virtualization\\Templates\\VdiState.xml

### Conditions préalables pour la prise en charge du générateur UE-V

Installez le générateur UE-V sur l’ordinateur utilisé pour créer des modèles d’emplacement des paramètres personnalisés. Cet ordinateur doit être en mesure d’exécuter les applications dont les paramètres sont synchronisés. Vous devez être membre du groupe Administrateurs sur l’ordinateur exécutant le logiciel UE-V Generator.

UE-V Generator doit être installé sur un ordinateur qui utilise un système de fichiers NTFS. Le logiciel de générateur UE-V nécessite .NET Framework 4. Pour plus d’informations, reportez-vous à la rubrique [déploiement d’UE-V 2. x pour des applications personnalisées](deploy-ue-v-2x-for-custom-applications-new-uevv2.md).

## Autres ressources pour ce produit


-   [Virtualisation de l’utilisation de l’utilisateur Microsoft (UE-V) 2. x](index.md)

-   [Prise en main d'UE-V2.x](get-started-with-ue-v-2x-new-uevv2.md)

-   [Administration d’UE-V 2. x](administering-ue-v-2x-new-uevv2.md)

-   [Résolution des problèmes de UE-V 2. x](troubleshooting-ue-v-2x-both-uevv2.md)

-   [Informations techniques de référence sur UE-V2.x](technical-reference-for-ue-v-2x-both-uevv2.md)














