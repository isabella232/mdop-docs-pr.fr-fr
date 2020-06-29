---
title: Présentation des rapports MBAM dans Configuration Manager
description: Présentation des rapports MBAM dans Configuration Manager
author: dansimp
ms.assetid: b2582190-c9de-4e64-bd5a-f31ac1916f53
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 995d628cafd03c8bdd209e467c9d22169b7e03c3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810187"
---
# Présentation des rapports MBAM dans Configuration Manager


Lorsque Microsoft BitLocker administration et la surveillance (MBAM) sont installés avec la topologie intégrée de Configuration Manager, les fonctionnalités de compatibilité matérielle et de création de rapports sont déplacées vers l’infrastructure de Configuration Manager et hors MBAM. Lorsque vous utilisez la topologie Configuration Manager, vous exécutez des rapports à partir de Configuration Manager plutôt que de MBAM, à l’exception du rapport d’audit de récupération, auquel vous pouvez toujours accéder à l’aide du site Web d’administration et de surveillance.

Les rapports pour la topologie intégrée de Configuration Manager présentent la conformité BitLocker pour l’entreprise et pour les ordinateurs et appareils individuels gérés par MBAM. Les rapports fournissent des informations tabulaires et des graphiques, et vous permettent de filtrer des États pour afficher les données de différentes perspectives.

Les informations fournies dans cette rubrique décrivent les rapports MBAM que vous exécutez à partir de Configuration Manager. Pour plus d’informations sur les rapports MBAM pour la topologie autonome, voir [Présentation des rapports MBAM](understanding-mbam-reports-mbam-2.md).

## Accès aux rapports dans Configuration Manager


Pour accéder à la fonctionnalité rapports dans Configuration Manager, ouvrez la **console Configuration Manager**. Pour afficher la liste des rapports disponibles:

-   Dans Configuration Manager 2007, développez le nœud gestion de l' **ordinateur** , puis développez le nœud **création de rapports** .

-   Dans SystemCenter2012 ConfigurationManager, dans l’espace de travail analyse sous **vue d’ensemble**, développez le nœud **rapports** , puis cliquez sur **rapports**.

### Tableau de bord de conformité de BitLocker Enterprise

Le tableau de bord de conformité de BitLocker Enterprise fournit les graphiques suivants, qui indiquent l’état de conformité de BitLocker au sein de l’entreprise:

-   Distribution de l’état de conformité

-   Distribution d’erreurs non conformes

-   Répartition de l’état de conformité par type de lecteur

**Distribution de l’état de conformité**

Ce graphique en secteurs affiche le statut de conformité de l’ordinateur au sein de l’entreprise et indique le pourcentage d’ordinateurs par rapport au nombre total d’ordinateurs de la collection sélectionnée qui présentent l’état de conformité. Le nombre réel d’ordinateurs avec chaque statut est également affiché. Le graphique en secteurs présente les États de conformité suivants:

-   Conformes

-   Non conforme

-   Exonéré d’utilisateur

-   Exemption d’utilisateur temporaire

-   Stratégie non appliquée

-   Inconnu: il s’agit d’ordinateurs dont l’État a été signalé comme une erreur ou ceux qui font partie de la collection, mais qui n’ont jamais signalé leur état de conformité, par exemple, s’ils sont déconnectés de l’organisation.

**Distribution d’erreurs non conformes**

Ce graphique en secteurs présente les catégories d’ordinateurs de l’entreprise qui ne sont pas conformes à la stratégie de chiffrement de lecteur BitLocker et indique le nombre d’ordinateurs dans chaque catégorie. Chaque pourcentage de catégorie est calculé à partir du nombre total d’ordinateurs non conformes de la collection.

-   Chiffrement différé par l’utilisateur

-   Impossible de trouver le TPM compatible

-   Partition système non disponible ou trop grande

-   Conflit de stratégie

-   En attente de la mise en service automatique du module de plateforme sécurisée

-   Une erreur inconnue s’est produite

-   Aucune information – les ordinateurs sur lesquels le client MBAM n’est pas installé, ou qui ont installé le client MBAM mais qui ne sont pas activés, par exemple, le service ne fonctionne pas

**Répartition de l’état de conformité par type de lecteur**

Ce graphique à barres affiche l’état de compatibilité BitLocker actuel par type de lecteur. Les statuts sont «conformes» et «non conformes». Des barres sont affichées pour les lecteurs de données fixes et les lecteurs de systèmes d’exploitation. Les ordinateurs qui n’ont pas de lecteur de données fixe ne sont inclus et n’affichent aucune valeur dans la barre du lecteur du système d’exploitation. Le graphique n’inclut pas les utilisateurs qui ont reçu une exemption de la stratégie de chiffrement de lecteur BitLocker ou de la catégorie «aucune stratégie».

### Rapport Détails de conformité de BitLocker Enterprise

Ce rapport affiche des informations sur la conformité de BitLocker globale dans votre entreprise pour la collection d’ordinateurs ciblés pour l’utilisation de BitLocker.

**Champs du rapport Détails de conformité BitLocker entreprise**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nom de la colonne</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Ordinateurs gérés</p></td>
<td align="left"><p>Nombre d’ordinateurs gérés par MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Compatibilité%</p></td>
<td align="left"><p>Pourcentage d’ordinateurs conformes dans l’entreprise.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>% Non conforme</p></td>
<td align="left"><p>Pourcentage d’ordinateurs non conformes dans l’entreprise.</p></td>
</tr>
<tr class="even">
<td align="left"><p>% De conformité inconnue</p></td>
<td align="left"><p>Pourcentage d’ordinateurs dont l’état de conformité n’est pas connu.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Pourcentage d’exonération</p></td>
<td align="left"><p>Pourcentage d’ordinateurs exemptés de l’exigence de cryptage BitLocker.</p></td>
</tr>
<tr class="even">
<td align="left"><p>% Non exempté</p></td>
<td align="left"><p>Pourcentage d’ordinateurs exemptés de l’exigence de cryptage BitLocker.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Conformes</p></td>
<td align="left"><p>Pourcentage d’ordinateurs conformes dans l’entreprise.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Non conforme</p></td>
<td align="left"><p>Pourcentage d’ordinateurs non conformes dans l’entreprise.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Conformité inconnue</p></td>
<td align="left"><p>Pourcentage d’ordinateurs dont l’état de conformité n’est pas connu.</p></td>
</tr>
<tr class="even">
<td align="left"><p>SIRET</p></td>
<td align="left"><p>Nombre total d’ordinateurs exemptés de l’exigence de cryptage BitLocker.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Non exempté</p></td>
<td align="left"><p>Nombre total d’ordinateurs qui ne sont pas exemptés de l’exigence de chiffrement BitLocker.</p></td>
</tr>
</tbody>
</table>

 

**Rapport des détails de conformité de BitLocker pour les entreprises-États de conformité**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">État de la conformité</th>
<th align="left">Question</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Non conforme</p></td>
<td align="left"><p>Ne pas exempter</p></td>
<td align="left"><p>L’ordinateur n’est pas conforme, conformément à la stratégie spécifiée.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Conformes</p></td>
<td align="left"><p>Ne pas exempter</p></td>
<td align="left"><p>L’ordinateur est conforme conformément à la stratégie spécifiée.</p></td>
</tr>
</tbody>
</table>

 

### Rapport synthèse de conformité de BitLocker Enterprise

Utilisez ce type de rapport pour afficher les informations relatives à la conformité de BitLocker globale dans votre entreprise et pour montrer la conformité d’ordinateurs individuels qui se trouvent dans la collection d’ordinateurs ciblés pour l’utilisation de BitLocker.

**Champs du rapport de synthèse de conformité BitLocker Enterprise**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nom de la colonne</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Ordinateurs gérés</p></td>
<td align="left"><p>Nombre d’ordinateurs gérés par MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Compatibilité%</p></td>
<td align="left"><p>Pourcentage d’ordinateurs conformes dans l’entreprise.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>% Non conforme</p></td>
<td align="left"><p>Pourcentage d’ordinateurs non conformes dans l’entreprise.</p></td>
</tr>
<tr class="even">
<td align="left"><p>% De conformité inconnue</p></td>
<td align="left"><p>Pourcentage d’ordinateurs dont l’état de conformité n’est pas connu.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Pourcentage d’exonération</p></td>
<td align="left"><p>Pourcentage d’ordinateurs exemptés de l’exigence de cryptage BitLocker.</p></td>
</tr>
<tr class="even">
<td align="left"><p>% Non exempté</p></td>
<td align="left"><p>Pourcentage d’ordinateurs exemptés de l’exigence de cryptage BitLocker.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Conformes</p></td>
<td align="left"><p>Pourcentage d’ordinateurs conformes dans l’entreprise.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Non conforme</p></td>
<td align="left"><p>Pourcentage d’ordinateurs non conformes dans l’entreprise.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Conformité inconnue</p></td>
<td align="left"><p>Pourcentage d’ordinateurs dont l’état de conformité n’est pas connu.</p></td>
</tr>
<tr class="even">
<td align="left"><p>SIRET</p></td>
<td align="left"><p>Nombre total d’ordinateurs exemptés de l’exigence de cryptage BitLocker.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Non exempté</p></td>
<td align="left"><p>Nombre total d’ordinateurs qui ne sont pas exemptés de l’exigence de chiffrement BitLocker.</p></td>
</tr>
</tbody>
</table>

 

**Rapport de synthèse de conformité de BitLocker Enterprise-détails sur un ordinateur**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nom de la colonne</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Nom de l’ordinateur</p></td>
<td align="left"><p>Nom d’ordinateur DNS spécifié par l’utilisateur géré par MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Nom de domaine</p></td>
<td align="left"><p>Nom de domaine complet, où se trouve l’ordinateur client et est géré par MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>État de la conformité</p></td>
<td align="left"><p>État de conformité global de l’ordinateur géré par MBAM. Les États valides sont conformes et non conformes. Notez que l’état de conformité par lecteur (voir le tableau ci-dessous) risque d’indiquer des États de conformité différents. Toutefois, ce champ correspond à cet état de conformité, conformément à la stratégie spécifiée.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Question</p></td>
<td align="left"><p>État qui indique si l’utilisateur est exempté ou non exempt de la stratégie BitLocker.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Utilisateurs d’appareils</p></td>
<td align="left"><p>Utilisateur de l’appareil.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Détails de l’état de conformité</p></td>
<td align="left"><p>Messages d’erreur et d’état de l’état de conformité de l’ordinateur conformément à la politique spécifiée.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Dernier contact</p></td>
<td align="left"><p>Date et heure de la dernière connexion de l’ordinateur au serveur pour signaler l’état de la conformité. La fréquence de contact est configurable (voir paramètres de la stratégie MBAM).</p></td>
</tr>
</tbody>
</table>

 

### Rapport de conformité de l’ordinateur BitLocker

Utilisez ce type de rapport pour collecter des informations spécifiques à un ordinateur. Le rapport de conformité informatique fournit des informations de chiffrement détaillées sur chaque lecteur (système d’exploitation et lecteurs de données fixes) sur un ordinateur, ainsi que les indications de la stratégie appliquée à chaque type de lecteur de l’ordinateur. Pour afficher les détails de chaque lecteur, développez l’entrée nom de l’ordinateur.

**Remarques**  L’état du chiffrement du volume de données amovibles ne s’affiche pas dans le rapport.

 

**Rapport de conformité de l’ordinateur BitLocker – champs détails de l’ordinateur**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nom de la colonne</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Nom de l’ordinateur</p></td>
<td align="left"><p>Nom d’ordinateur DNS spécifié par l’utilisateur géré par MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Nom de domaine</p></td>
<td align="left"><p>Nom de domaine complet, où se trouve l’ordinateur client et est géré par MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Type d’ordinateur</p></td>
<td align="left"><p>Type d’ordinateur. Les types valides ne sont pas portables et portables.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Systèmed’exploitation</p></td>
<td align="left"><p>Type de système d’exploitation détecté sur l’ordinateur client géré MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Conformité globale</p></td>
<td align="left"><p>État de conformité global de l’ordinateur géré par MBAM. Les États valides sont conformes et non conformes. Notez que l’état de conformité par lecteur (voir le tableau ci-dessous) risque d’indiquer des États de conformité différents. Toutefois, ce champ correspond à cet état de conformité, conformément à la stratégie spécifiée.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Compatibilité du système d’exploitation</p></td>
<td align="left"><p>État de conformité du système d’exploitation géré par MBAM. Les États valides sont conformes et non conformes.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Compatibilité des lecteurs de données fixes</p></td>
<td align="left"><p>État de la conformité du lecteur de données fixes géré par MBAM. Les États valides sont conformes et non conformes.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Date de la dernière mise à jour</p></td>
<td align="left"><p>Date et heure de la dernière connexion de l’ordinateur au serveur pour signaler l’état de la conformité. La fréquence de contact est configurable (voir paramètres de la stratégie MBAM).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Question</p></td>
<td align="left"><p>État qui indique si l’utilisateur est exempté ou non exempt de la stratégie BitLocker.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Utilisateur exempté</p></td>
<td align="left"><p>Utilisateur exempt de la stratégie BitLocker.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Date d’exemption</p></td>
<td align="left"><p>Date à laquelle l’exemption a été accordée.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Détails de l’état de conformité</p></td>
<td align="left"><p>Messages d’erreur et d’état de l’état de conformité de l’ordinateur conformément à la politique spécifiée.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Niveau de cryptage de la stratégie</p></td>
<td align="left"><p>Force de cryptage sélectionnée par l’administrateur lors de la spécification de la stratégie MBAM. (par exemple, 128-bit avec diffuseur).</p></td>
</tr>
<tr class="even">
<td align="left"><p>Stratégie: lecteur du système d’exploitation</p></td>
<td align="left"><p>Indique si le chiffrement est requis pour les e/S et le type de protecteur approprié.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Stratégie: disque de données fixe</p></td>
<td align="left"><p>Indique si le chiffrement est requis pour le lecteur fixe.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Fabricant</p></td>
<td align="left"><p>Nom de fabricant de l’ordinateur tel qu’il apparaît dans le BIOS de l’ordinateur.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Modèle</p></td>
<td align="left"><p>Nom de modèle du fabricant d’ordinateurs tel qu’il apparaît dans le BIOS de l’ordinateur.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Utilisateurs d’appareils</p></td>
<td align="left"><p>Utilisateurs connus sur l’ordinateur géré par MBAM.</p></td>
</tr>
</tbody>
</table>

 

**Rapport de conformité de l’ordinateur BitLocker – champs volume de l’ordinateur**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nom de la colonne</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Lettre du lecteur</p></td>
<td align="left"><p>Lettre du lecteur de l’ordinateur qui a été affectée à l’utilisateur en particulier.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Type de lecteur</p></td>
<td align="left"><p>Type de lecteur. Les valeurs valides sont le lecteur du système d’exploitation et le lecteur de données fixes. Il s’agit de disques physiques plutôt que de volumes logiques.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Niveau de cryptage</p></td>
<td align="left"><p>Force de cryptage sélectionnée par l’administrateur lors de la spécification de la stratégie MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Types de protecteur</p></td>
<td align="left"><p>Type de protecteur sélectionné via une stratégie utilisée pour chiffrer un système d’exploitation ou un volume fixe. Les types de protecteur valides sur un système d’exploitation sont TPM ou TPM + NIP et un volume de données fixe est Password.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>État de protecteur</p></td>
<td align="left"><p>Indique que l’ordinateur géré par MBAM a activé le type de protecteur spécifié dans la stratégie. Les États valides sont ACTIVÉs ou désactivés.</p></td>
</tr>
<tr class="even">
<td align="left"><p>État du chiffrement</p></td>
<td align="left"><p>État du chiffrement du lecteur. Les États valides sont chiffrés, non chiffrés et chiffrés.</p></td>
</tr>
</tbody>
</table>

 

## Rubriques connexes


[Utilisation de MBAM avec Configuration Manager](using-mbam-with-configuration-manager.md)

 

 





