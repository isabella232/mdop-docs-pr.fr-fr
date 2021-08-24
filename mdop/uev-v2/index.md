---
title: Microsoft User Experience Virtualization (UE-V) 2.x
description: Microsoft User Experience Virtualization (UE-V) 2.x
author: dansimp
ms.assetid: b860fed0-b846-415d-bdd6-ba60231a64be
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 04/19/2017
ms.openlocfilehash: 79748e04ae1a59afdc8f9dae3c5dc77c50e3c253
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910539"
---
# <a name="microsoft-user-experience-virtualization-ue-v-2x"></a>Microsoft User Experience Virtualization (UE-V) 2.x

>[!NOTE]
>Cette documentation est une version de UE-V incluse dans microsoft Desktop Optimization Pack (MDOP). Pour plus d’informations sur la dernière version de UE-V qui est incluse dans Windows 10 Entreprise, voir Prise en main [avec UE-V](https://docs.microsoft.com/windows/configuration/ue-v/uev-getting-started).


Capturez et centralisez les paramètres d’application et de système d’exploitation Windows de vos utilisateurs en implémentant Microsoft User Experience Virtualization (UE-V) 2.0 ou 2.1. Ensuite, appliquez ces paramètres aux appareils accessibles aux utilisateurs dans votre entreprise, tels que les ordinateurs de bureau, les ordinateurs portables ou les sessions VDI (Virtual Desktop Infrastructure).

**Avec UE-V vous pouvez...**

-   Spécifier les paramètres d’application et de bureau à synchroniser

-   Transmettre les paramètres à toute heure et en tout lieu de travail des utilisateurs au sein de l’entreprise

-   Créer des modèles personnalisés pour vos applications cœur de métier ou tierces

-   Récupérer les paramètres après le remplacement ou la mise à niveau du matériel, ou après avoir réinventé un ordinateur virtuel à son état initial

## <a name="components-of-ue-v-2x"></a>Composants de UE-V 2.x


Ce diagramme montre comment les composants déployés UE-V fonctionnent ensemble pour synchroniser les paramètres.

![diagramme architectural uev2.](images/uev2archdiagram.gif)

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Composant</th>
<th align="left">Fonction</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>UE-V Agent</strong></p></td>
<td align="left"><p>Installé sur chaque ordinateur qui doit synchroniser les paramètres, l’agent UE-V surveille les applications inscrites et le système d’exploitation pour les modifications de paramètres, puis synchronise ces paramètres entre les <strong> </strong> ordinateurs.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Paramètres packages</strong></p></td>
<td align="left"><p>Les paramètres et Windows d’application sont stockés dans les packages de <strong> paramètres créés par </strong> l’agent UE-V. Les packages de paramètres sont développés, stockés en local et copiés sur l’emplacement de stockage des paramètres.</p>
<ul>
<li><p>Les valeurs de paramètre <strong> pour les applications de bureau sont </strong> stockées lorsque l’utilisateur ferme l’application.</p></li>
<li><p>Les valeurs des Windows sont stockées lorsque l’utilisateur se déconnecte, lorsque l’ordinateur est verrouillé ou lorsqu’il se déconnecte à distance <strong> </strong> d’un ordinateur.</p></li>
</ul>
<p>Le fournisseur de synchronisation détermine quand les paramètres de l’application ou du système d’exploitation sont lus à partir Paramètres packages et <strong> </strong> synchronisés.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Paramètres de stockage</strong></p></td>
<td align="left"><p>Il s’agit d’un partage réseau standard accessible par vos utilisateurs. L’agent UE-V vérifie l’emplacement et crée un dossier système masqué dans lequel stocker et récupérer les paramètres utilisateur.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Paramètres d’emplacement</strong></p></td>
<td align="left"><p>UE-V utilise des fichiers XML comme modèles d’emplacement de paramètres pour surveiller et synchroniser les paramètres d’application de bureau et Windows paramètres de bureau entre les ordinateurs des utilisateurs. Par défaut, certains modèles d’emplacement de paramètres sont inclus dans UE-V . Vous pouvez également créer, modifier ou valider des modèles d’emplacement de paramètres personnalisés en gérant la synchronisation des <a href="#customapps" data-raw-source="[managing settings synchronization for custom applications](#customapps)"> paramètres pour les applications personnalisées. </a></p>
<div class="alert">
<strong>Remarque</strong><br/><p>Paramètres modèles d’emplacement ne sont pas requis pour Windows applications.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Windows d’application</strong></p></td>
<td align="left"><p>Paramètres pour Windows applications sont capturées et appliquées dynamiquement. Le développeur d’applications spécifie les paramètres synchronisés pour chaque application. UE-V détermine quelles applications Windows sont activées pour la synchronisation des paramètres à l’aide d’une liste gérée d’applications. Par défaut, cette liste inclut la plupart des Windows applications.</p>
<p>Vous pouvez ajouter ou supprimer des applications dans la Windows d’applications en suivant les procédures indiquées <a href="https://technet.microsoft.com/library/dn458925.aspx" data-raw-source="[here](https://technet.microsoft.com/library/dn458925.aspx)"> </a> ici.</p></td>
</tr>
</tbody>
</table>



### <a name="managing-settings-synchronization-for-custom-applications"></a><a href="" id="customapps"></a>Gestion Paramètres synchronisation des applications personnalisées

Utilisez ces UE-V pour créer et gérer des modèles personnalisés pour vos applications métiers ou tierces.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>UE-V Générateur</strong></p></td>
<td align="left"><p>Utilisez le générateur UE-V pour créer des modèles d’emplacement de paramètres personnalisés que vous pouvez ensuite distribuer <strong> </strong> aux ordinateurs des utilisateurs. Le UE-V Générateur de données vous permet également de modifier un modèle existant ou de valider un modèle créé à l’aide d’un autre éditeur XML.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Paramètres catalogue de modèles</strong></p></td>
<td align="left"><p>Le catalogue de modèles de paramètres est un chemin d’accès de dossier sur UE-V ou un partage réseau SMB (Server Message Block) qui stocke les modèles d’emplacement des <strong> </strong> paramètres personnalisés. L’agent UE-V vérifie cet emplacement une fois par jour, récupère les modèles nouveaux ou mis à jour et met à jour son comportement de synchronisation.</p>
<p>Si vous utilisez uniquement les modèles UE-V paramètres par défaut, un catalogue de modèles de paramètres est inutile. Pour plus d’informations sur les catalogues de déploiement de paramètres, voir Configurer UE-V catalogue de <a href="https://technet.microsoft.com/library/dn458942.aspx#deploycatalogue" data-raw-source="[Configure a UE-V settings template catalog](https://technet.microsoft.com/library/dn458942.aspx#deploycatalogue)"> modèles de paramètres. </a></p></td>
</tr>
</tbody>
</table>



![Processus du générateur ue-v.](images/ue-vgeneratorprocess.gif)

## <a name="settings-synchronized-by-default"></a>Paramètres Synchronisé par défaut


UE-V synchronise les paramètres de ces applications par défaut. Pour obtenir une liste complète et des informations plus détaillées, voir Paramètres qui sont automatiquement synchronisés dans [un déploiement UE-V.](https://technet.microsoft.com/library/dn458932.aspx#autosyncsettings)

Microsoft Office 2013 (UE-V 2.1 SP1 et 2.1)

Microsoft Office 2010 (UE-V 2.1 SP1, 2.1 et 2.0)

Microsoft Office applications 2007 (UE-V 2.0 uniquement)

Internet Explorer 8, 9 et 10

Internet Explorer 11 UE-V 2.1 SP1 et 2.1

De Windows applications, telles que Xbox

De Windows applications de bureau, telles que Bloc-notes

De nombreux Windows de bureau, tels que l’arrière-plan du bureau ou le papier peint

**Remarque**  
Vous pouvez également [personnaliser les UE-V pour synchroniser les paramètres](https://technet.microsoft.com/library/dn458942.aspx) des applications autres que celles synchronisées par défaut.



## <a name="compare-ue-v-to-other-microsoft-products"></a>Comparer UE-V à d’autres produits Microsoft


Utilisez ce tableau pour comparer les UE-V synchroniser les profils dans Windows 7, synchroniser les profils dans Windows 8 et la fonctionnalité de synchronisation Paramètres pc du compte Microsoft.

<table style="width:100%;">
<colgroup>
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Fonctionnalité</th>
<th align="left">Synchroniser les profils à l Windows 7</th>
<th align="left">Synchroniser les profils à l’aide Windows 8</th>
<th align="left">Synchroniser les profils à l’aide Windows 10</th>
<th align="left">Compte Microsoft</th>
<th align="left">UE-V 2.0</th>
<th align="left">UE-V 2.1 et 2.1 SP1</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Synchroniser les paramètres entre plusieurs ordinateurs</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
</tr>
<tr class="even">
<td align="left"><p>Synchroniser les paramètres entre les applications physiques et virtuelles</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Synchroniser Windows paramètres de l’application</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
</tr>
<tr class="even">
<td align="left"><p>Gérer via WMI</p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Synchroniser régulièrement les modifications des paramètres</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
</tr>
<tr class="even">
<td align="left"><p>Configuration minimale pour le programme d’installation</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Pris en charge sur les ordinateurs non joints à un domaine</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Prend en charge l’attribut Active Directory de l’ordinateur principal</p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Synchronise les paramètres entre l’infrastructure de bureau virtuel (VDI)/les services Bureau à distance (RDS) et les bureaux enrichis</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
</tr>
<tr class="even">
<td align="left"><p>Espace de stockage de paramètre illimité</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Choix des paramètres d’application à synchroniser</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
</tr>
<tr class="even">
<td align="left"><p>Sauvegarde/restauration pour les Pro</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>Partiel</p></td>
<td align="left"><p>●</p></td>
</tr>
</tbody>
</table>



## <a name="ue-v-2x-release-notes"></a>UE-V Notes de publication 2.x


Pour plus d’informations et pour les actualités de dernière heure qui n’ont pas été entrées dans la documentation, voir

-   [Notes de publication pour Microsoft User Experience Virtualization (UE-V) 2.1 SP1](microsoft-user-experience-virtualization--ue-v--21-sp1-release-notes.md)

-   [Notes de publication pour Microsoft User Experience Virtualization (UE-V) 2.1](microsoft-user-experience-virtualization--ue-v--21-release-notesuevv21.md)

-   [Notes de publication pour Microsoft User Experience Virtualization (UE-V) 2.0](microsoft-user-experience-virtualization--ue-v--20-release-notesuevv2.md)

## <a name="other-resources-for-this-product"></a>Autres ressources pour ce produit


-   [Prise en main d'UE-V 2.x](get-started-with-ue-v-2x-new-uevv2.md)

-   [Préparer un déploiement UE-V 2.x](prepare-a-ue-v-2x-deployment-new-uevv2.md)

-   [Administration UE-V 2.x](administering-ue-v-2x-new-uevv2.md)

-   [Résolution des problèmes UE-V 2.x](troubleshooting-ue-v-2x-both-uevv2.md)

-   [Informations techniques de référence sur UE-V 2.x](technical-reference-for-ue-v-2x-both-uevv2.md)

### <a name="more-information"></a>Plus d’informations

<a href="" id="mdop-techcenter-page"></a>[Page TechCenter MDOP](https://go.microsoft.com/fwlink/p/?LinkId=225286) Découvrez les dernières informations et ressources MDOP.

<a href="" id="mdop-information-experience"></a>[Expérience d’informations MDOP](https://go.microsoft.com/fwlink/p/?LinkId=236032) Recherchez de la documentation, des vidéos et d’autres ressources pour les technologies MDOP. Vous pouvez également [nous envoyer des commentaires ou](mailto:MDOPDocs@microsoft.com) en savoir plus sur les mises à jour en nous suivant sur [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) ou [Twitter.](https://go.microsoft.com/fwlink/p/?LinkId=242447)














