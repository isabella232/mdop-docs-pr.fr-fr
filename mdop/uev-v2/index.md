---
title: Virtualisation de l’utilisation de l’utilisateur Microsoft (UE-V) 2. x
description: Virtualisation de l’utilisation de l’utilisateur Microsoft (UE-V) 2. x
author: dansimp
ms.assetid: b860fed0-b846-415d-bdd6-ba60231a64be
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 04/19/2017
ms.openlocfilehash: 573b8bb2027e5c7f117a8254005a43c656f047a9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10795817"
---
# Virtualisation de l’utilisation de l’utilisateur Microsoft (UE-V) 2. x

>[!NOTE]
>Cette documentation est une version de UE-V incluse dans le pack d’optimisation du bureau Microsoft (MDOP). Pour plus d’informations sur la dernière version de UE-V incluse dans Windows 10 entreprise, voir [prise en main d’UE-v](https://docs.microsoft.com/windows/configuration/ue-v/uev-getting-started).


Capturez et centralisez les paramètres d’application de vos utilisateurs et les paramètres du système d’exploitation Windows en implémentant Microsoft User Interface Virtualization (UE-V) 2,0 ou 2,1. Appliquez ensuite ces paramètres aux appareils accessibles aux utilisateurs de votre entreprise, par exemple, ordinateurs de bureau, ordinateurs portables ou sessions VDI (Virtual Desktop Infrastructure).

**Avec UE-V, vous pouvez...**

-   Spécifier les paramètres de l’application et du bureau qui sont synchronisés

-   Transmettre les paramètres à toute heure et en tout lieu de travail des utilisateurs au sein de l’entreprise

-   Créer des modèles personnalisés pour vos applications cœur de métier ou tierces

-   Récupérer les paramètres après un remplacement ou une mise à niveau du matériel, ou après la recréation de l’image d’une machine virtuelle à son état initial

## Composants d’UE-V 2. x


Le diagramme suivant montre comment les composants UE-V déployés collaborent pour synchroniser les paramètres.

![diagramme d’architecture uev2](images/uev2archdiagram.gif)

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
<td align="left"><p><strong>Agent UE-V</strong></p></td>
<td align="left"><p>Installés sur tous les ordinateurs qui doivent synchroniser les paramètres, l' <strong> agent UE-V </strong> surveille les applications inscrites et le système d’exploitation en fonction des modifications apportées aux paramètres, puis synchronise ces paramètres entre eux.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Packages de paramètres</strong></p></td>
<td align="left"><p>Les paramètres d’application et les paramètres Windows sont stockés dans <strong> les packages de paramètres </strong> créés par l’agent UE-V. Les packages de paramètres sont développés, stockés en local et copiés sur l’emplacement de stockage des paramètres.</p>
<ul>
<li><p>Les valeurs de paramètres des <strong> applications de bureau </strong> sont stockées lorsque l’utilisateur ferme l’application.</p></li>
<li><p>Les valeurs des <strong> Paramètres Windows </strong> sont stockées lorsque l’utilisateur se déconnecte, lorsque l’ordinateur est verrouillé, ou lorsque l’utilisateur se déconnecte à distance à partir d’un ordinateur.</p></li>
</ul>
<p>Le fournisseur de synchronisation détermine à quel moment les paramètres des applications ou du système d’exploitation sont lus à partir des <strong> packages de paramètres </strong> et synchronisés.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Emplacement de stockage des paramètres</strong></p></td>
<td align="left"><p>Ce partage réseau standard peut être accessible à vos utilisateurs. L’agent UE-V vérifie l’emplacement et crée un dossier système caché dans lequel stocker et récupérer des paramètres d’utilisateur.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Modèles d’emplacement des paramètres</strong></p></td>
<td align="left"><p>UE-V utilise des fichiers XML comme modèles d’emplacement des paramètres pour surveiller et synchroniser les paramètres des applications de bureau et les paramètres de bureau Windows entre les ordinateurs des utilisateurs. Par défaut, certains modèles d’emplacement des paramètres sont inclus dans UE-V. Vous pouvez également créer, modifier ou valider des modèles d’emplacements de paramètres personnalisés en <a href="#customapps" data-raw-source="[managing settings synchronization for custom applications](#customapps)"> gérant la synchronisation des paramètres pour des applications personnalisées </a> .</p>
<div class="alert">
<strong>Remarque</strong><br/><p>Les modèles d’emplacement des paramètres ne sont pas requis pour les applications Windows.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Liste des applications Windows</strong></p></td>
<td align="left"><p>Les paramètres des applications Windows sont capturés et appliqués dynamiquement. Le développeur de l’application spécifie les paramètres qui sont synchronisés pour chaque application. UE-V détermine les applications Windows qui sont activées pour la synchronisation des paramètres à l’aide d’une liste gérée d’applications. Par défaut, cette liste inclut la plupart des applications Windows.</p>
<p>Vous pouvez ajouter ou supprimer des applications dans la liste des applications Windows en suivant les procédures décrites dans <a href="https://technet.microsoft.com/library/dn458925.aspx" data-raw-source="[here](https://technet.microsoft.com/library/dn458925.aspx)"> cet article </a> .</p></td>
</tr>
</tbody>
</table>



### <a href="" id="customapps"></a>Gestion de la synchronisation des paramètres pour des applications personnalisées

Utilisez ces composants UE-V pour créer et gérer des modèles personnalisés pour vos applications tierces ou métier.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Générateur UE-V</strong></p></td>
<td align="left"><p>Servez <strong> -vous du générateur UE-V </strong> pour créer des modèles d’emplacements de paramètres personnalisés que vous pouvez distribuer ensuite sur les ordinateurs des utilisateurs. Le générateur UE-V vous permet également de modifier un modèle existant ou de valider un modèle qui a été créé à l’aide d’un autre éditeur XML.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Catalogue de modèles de paramètres</strong></p></td>
<td align="left"><p>Le <strong> catalogue de modèles </strong> de paramètres est un chemin de dossier sur les ordinateurs UE-V ou un partage réseau de blocs de messages serveur (SMB) qui stocke les modèles d’emplacement des paramètres personnalisés. L’agent UE-V vérifie cet emplacement une fois par jour, récupère les modèles nouveaux ou mis à jour et met à jour son comportement de synchronisation.</p>
<p>Si vous utilisez uniquement les modèles d’emplacement des paramètres par défaut UE-V, il est inutile d’utiliser un catalogue de modèles de paramètres. Pour plus d’informations sur les paramètres des catalogues de déploiement, voir <a href="https://technet.microsoft.com/library/dn458942.aspx#deploycatalogue" data-raw-source="[Configure a UE-V settings template catalog](https://technet.microsoft.com/library/dn458942.aspx#deploycatalogue)"> configurer un catalogue de modèles de paramètres UE-V </a> .</p></td>
</tr>
</tbody>
</table>



![processus du générateur UE-v](images/ue-vgeneratorprocess.gif)

## Paramètres synchronisés par défaut


UE-V synchronise les paramètres pour ces applications par défaut. Pour obtenir une liste complète et des informations plus détaillées, voir [paramètres qui sont synchronisés automatiquement dans un déploiement UE-V](https://technet.microsoft.com/library/dn458932.aspx#autosyncsettings).

Applications Microsoft Office 2013 (UE-V 2,1 SP1 et 2,1)

Applications Microsoft Office 2010 (UE-V 2,1 SP1, 2,1 et 2,0)

Applications Microsoft Office 2007 (UE-V 2,0 uniquement)

Internet Explorer 8, 9 et 10

Internet Explorer 11 dans UE-V 2,1 SP1 et 2,1

Plusieurs applications Windows, telles que Xbox

Plusieurs applications de bureau Windows, comme le bloc-notes

De nombreux paramètres Windows, tels que l’arrière-plan ou le papier peint du Bureau;

**Remarque**  
Vous pouvez également [personnaliser UE-V pour synchroniser les paramètres](https://technet.microsoft.com/library/dn458942.aspx) d’applications autres que celles synchronisées par défaut.



## Comparer UE-V à d’autres produits Microsoft


Utilisez ce tableau pour comparer UE-V afin de synchroniser les profils dans Windows 7, de synchroniser les profils dans Windows 8 et de la fonctionnalité de synchronisation des paramètres du PC de compte Microsoft.

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
<th align="left">Synchroniser des profils à l’aide de Windows 7</th>
<th align="left">Synchroniser des profils à l’aide de Windows 8</th>
<th align="left">Synchroniser des profils à l’aide de Windows 10</th>
<th align="left">Compte Microsoft</th>
<th align="left">UE-V 2,0</th>
<th align="left">UE-V 2,1 et 2,1 SP1</th>
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
<td align="left"><p>Synchroniser les paramètres des applications Windows</p></td>
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
<td align="left"><p>Synchroniser les modifications de paramètres régulièrement</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
</tr>
<tr class="even">
<td align="left"><p>Configuration minimale pour l’installation</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Pris en charge sur les ordinateurs non membres du domaine</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Prend en charge l’attribut Active Directory principal de l’ordinateur</p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Synchronise les paramètres entre les services Bureau à distance et les services Bureau à distance</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
</tr>
<tr class="even">
<td align="left"><p>Espace de stockage des paramètres illimités</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Choix dans les paramètres d’application à synchroniser</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
</tr>
<tr class="even">
<td align="left"><p>Sauvegarde/restauration pour les professionnels de l’informatique</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>Partiel</p></td>
<td align="left"><p>●</p></td>
</tr>
</tbody>
</table>



## UE-V 2. x notes de publication


Pour plus d’informations et pour les actualités de dernière minute qui n’ont pas été transportées en documentation, voir

-   [Notes de publication pour Microsoft User Experience Virtualization (UE-V)2.1SP1](microsoft-user-experience-virtualization--ue-v--21-sp1-release-notes.md)

-   [Notes de publication pour Microsoft User Experience Virtualization (UE-V)2.1](microsoft-user-experience-virtualization--ue-v--21-release-notesuevv21.md)

-   [Notes de publication pour Microsoft User Experience Virtualization (UE-V)2.0](microsoft-user-experience-virtualization--ue-v--20-release-notesuevv2.md)

## Autres ressources pour ce produit


-   [Prise en main d'UE-V2.x](get-started-with-ue-v-2x-new-uevv2.md)

-   [Préparer un déploiement UE-V 2. x](prepare-a-ue-v-2x-deployment-new-uevv2.md)

-   [Administration d’UE-V 2. x](administering-ue-v-2x-new-uevv2.md)

-   [Résolution des problèmes de UE-V 2. x](troubleshooting-ue-v-2x-both-uevv2.md)

-   [Informations techniques de référence sur UE-V2.x](technical-reference-for-ue-v-2x-both-uevv2.md)

### Informations supplémentaires

<a href="" id="mdop-techcenter-page"></a>[Page TechCenter de MDOP](https://go.microsoft.com/fwlink/p/?LinkId=225286) En savoir plus sur les dernières informations et ressources de MDOP.

<a href="" id="mdop-information-experience"></a>[Découverte des informations de MDOP](https://go.microsoft.com/fwlink/p/?LinkId=236032) Recherchez des documents, des vidéos et d’autres ressources pour MDOP technologies. Vous pouvez également [nous envoyer vos commentaires](mailto:MDOPDocs@microsoft.com) ou en savoir plus sur les mises à jour, en nous suivant sur [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) ou [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447).














