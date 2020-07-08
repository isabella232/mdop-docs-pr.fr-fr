---
title: Affichage de rapports MBAM2.5 pour la topologie Intégration Configuration Manager
description: Affichage de rapports MBAM2.5 pour la topologie Intégration Configuration Manager
author: dansimp
ms.assetid: 60d11b2f-3a76-4023-8da4-f89e9f35b790
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3384fee62d302ac47775fe106265456ef119ab47
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810319"
---
# Affichage de rapports MBAM2.5 pour la topologie Intégration Configuration Manager


Cette rubrique décrit les rapports disponibles lorsque vous configurez l’administration et la surveillance de Microsoft BitLocker (MBAM) avec la topologie d’intégration de Configuration Manager. Les rapports indiquent la conformité de BitLocker pour l’entreprise et pour les ordinateurs et appareils individuels gérés par MBAM. Les rapports fournissent des informations tabulaires et des graphiques et disposent de filtres qui vous permettent d’afficher des données de différentes perspectives.

Dans la topologie d’intégration de Configuration Manager, vous affichez des rapports à partir de Configuration Manager plutôt qu’à partir du site Web Administration et analyse, à l’exception du **rapport d’audit de récupération**, que vous continuez à consulter à partir du site Web d’administration et de surveillance.

Pour plus d’informations sur les rapports MBAM pour la topologie autonome, voir [affichage de MBAM rapports 2,5 pour la topologie autonome](viewing-mbam-25-reports-for-the-stand-alone-topology.md).

## Accès aux rapports dans Configuration Manager


Pour accéder à la fonctionnalité rapports dans Configuration Manager, procédez comme suit:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Version de Configuration Manager</th>
<th align="left">Afficher les rapports</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>SystemCenter2012 ConfigurationManager</p></td>
<td align="left"><ol>
<li><p>Dans le volet gauche, sélectionnez l' <strong> </strong> espace de travail analyse.</p></li>
<li><p>Dans l’arborescence, développez <strong> vue d’ensemble des </strong> &gt; <strong> rapports de rapport </strong> &gt; <strong> </strong> &gt; <strong> MBAM </strong> .</p></li>
<li><p>Sélectionnez le dossier qui représente la langue dans laquelle vous souhaitez afficher les rapports, puis sélectionnez le rapport dans le volet droit.</p></li>
</ol></td>
</tr>
<tr class="even">
<td align="left"><p>Gestionnaire de configuration 2007</p></td>
<td align="left"><ol>
<li><p>Dans le volet gauche, développez Gestion de l’ordinateur création de rapports <strong> </strong> &gt; <strong> </strong> &gt; <strong> Reporting Services Reporting Services </strong> &gt; <strong> &lt; &gt; </strong> &gt; <strong> </strong> &gt; <strong> MBAM </strong> .</p></li>
<li><p>Sélectionnez le dossier qui représente la langue dans laquelle vous souhaitez afficher les rapports, puis sélectionnez le rapport dans le volet droit.</p></li>
</ol></td>
</tr>
</tbody>
</table>

 

## Description des rapports dans Configuration Manager


Il existe quelques différences mineures dans les rapports pour la topologie d’intégration de Configuration Manager et la topologie autonome. Les sections suivantes décrivent les données dans les rapports MBAM pour la topologie d’intégration de Configuration Manager:

-   [Tableau de bord de conformité de BitLocker Enterprise](#bkmk-dashboard)

-   [Détails de la conformité à l’entreprise BitLocker](#bkmk-compliancedetails)

-   [Résumé de conformité de BitLocker Enterprise](#bkmk-compliancesummary)

-   [Rapport de conformité de l’ordinateur BitLocker](#bkmk-compliancereport)

### <a href="" id="bkmk-dashboard"></a>Tableau de bord de conformité de BitLocker Enterprise

Le tableau de bord de conformité de BitLocker Enterprise fournit les graphiques suivants, qui indiquent l’état de conformité de BitLocker au sein de l’entreprise:

-   Distribution de l’état de conformité

-   Distribution d’erreurs non conformes

-   Répartition de l’état de conformité par type de lecteur

**Distribution de l’état de conformité**

Ce graphique en secteurs montre l’état de la conformité pour les ordinateurs au sein de l’entreprise. Il indique également le pourcentage d’ordinateurs par rapport au nombre total d’ordinateurs de la collection sélectionnée dont l’état de conformité est défini. Le nombre réel d’ordinateurs avec chaque statut est également affiché. Le graphique en secteurs présente les États de conformité suivants:

-   Conformes

-   Non conforme

-   Exonéré d’utilisateur

-   Exemption d’utilisateur temporaire

-   Stratégie non appliquée

-   Encore. Ces ordinateurs ont signalé une erreur de statut ou font partie de la collection, mais n’ont jamais signalé leur état de conformité. L’absence de statut de conformité peut se produire si l’ordinateur est déconnecté de l’organisation.

**Distribution d’erreurs non conformes**

Ce graphique en secteurs présente les catégories d’ordinateurs de l’entreprise qui ne sont pas conformes à la stratégie de chiffrement de lecteur BitLocker et indique le nombre d’ordinateurs dans chaque catégorie. Chaque pourcentage de catégorie est calculé à partir du nombre total d’ordinateurs non conformes de la collection.

-   Chiffrement différé par l’utilisateur

-   Impossible de trouver le TPM compatible

-   Partition système non disponible ou trop grande

-   Conflit de stratégie

-   En attente de la mise en service automatique du module de plateforme sécurisée

-   Une erreur inconnue s’est produite

-   Aucune information. Sur ces ordinateurs, le client MBAM n’est pas installé ou le client MBAM est installé, mais n’est pas activé (par exemple, le service ne fonctionne pas).

**Répartition de l’état de conformité par type de lecteur**

Ce graphique à barres affiche l’état de compatibilité BitLocker actuel par type de lecteur. Les statuts sont **conformes** et **non conformes**. Des barres sont affichées pour les lecteurs de données fixes et les lecteurs de systèmes d’exploitation. Les ordinateurs qui n’ont pas de lecteur de données fixe ne sont inclus et n’affichent aucune valeur dans la barre du **lecteur du système d’exploitation** . Le graphique n’inclut pas les utilisateurs qui ont reçu une exemption de la stratégie de chiffrement de lecteur BitLocker ou de la catégorie aucune stratégie.

### <a href="" id="bkmk-compliancedetails"></a>Détails de la conformité à l’entreprise BitLocker

Ce rapport affiche des informations sur la conformité de BitLocker globale dans votre entreprise pour la collection d’ordinateurs ciblés pour l’utilisation de BitLocker.

**Champs détails de la conformité d’entreprise BitLocker**

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
<td align="left"><p>Pourcentage d’ordinateurs non exemptés de l’exigence de cryptage BitLocker.</p></td>
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

 

**États des détails de la conformité d’entreprise BitLocker**

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

 

### <a href="" id="bkmk-compliancesummary"></a>Résumé de conformité de BitLocker Enterprise

Utilisez ce type de rapport pour afficher les informations relatives à la conformité de BitLocker globale dans votre entreprise et pour montrer la conformité d’ordinateurs individuels qui se trouvent dans la collection d’ordinateurs ciblés pour l’utilisation de BitLocker.

**Champs de synthèse de conformité de BitLocker Enterprise**

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
<td align="left"><p>Pourcentage d’ordinateurs non exemptés de l’exigence de cryptage BitLocker.</p></td>
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

 

**Détails de l’ordinateur de synthèse de BitLocker Enterprise Compliance**

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
<td align="left"><p>Messages d’erreur et de statut concernant l’état de conformité de l’ordinateur conformément à la stratégie spécifiée.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Dernier contact</p></td>
<td align="left"><p>Date et heure de la dernière connexion de l’ordinateur au serveur pour signaler l’état de la conformité. La fréquence de contact est configurable par le biais des paramètres de stratégie de groupe.</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="bkmk-compliancereport"></a>Rapport de conformité de l’ordinateur BitLocker

Utilisez ce type de rapport pour collecter des informations spécifiques à un ordinateur. Le rapport de conformité de l’ordinateur BitLocker fournit des informations de chiffrement détaillées sur chaque lecteur sur un ordinateur (système d’exploitation et lecteurs de données fixes). Il fournit également une indication de la stratégie qui s’applique à chaque type de lecteur de l’ordinateur. Pour afficher les détails de chaque lecteur, développez l’entrée nom de l’ordinateur.

**Remarques**  Le statut de chiffrement du volume de données amovibles ne s’affiche pas dans ce rapport.

 

**Rapport de conformité de l’ordinateur BitLocker: champs détails de l’ordinateur**

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
<td align="left"><p>État de conformité global de l’ordinateur géré par MBAM. Les États valides sont conformes et non conformes. Notez que l’état de conformité par lecteur (voir le tableau ci-dessous) risque d’indiquer des États de conformité différents. Toutefois, ce champ correspond à cet état de conformité conformément à la stratégie spécifiée.</p></td>
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
<td align="left"><p>Date et heure de la dernière connexion de l’ordinateur au serveur pour signaler l’état de la conformité. La fréquence de contact est configurable par le biais des paramètres de stratégie de groupe.</p></td>
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
<td align="left"><p>Messages d’erreur et de statut concernant l’état de conformité de l’ordinateur conformément à la stratégie spécifiée.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Niveau de cryptage de la stratégie</p></td>
<td align="left"><p>Force de cryptage sélectionnée par l’administrateur lors de la spécification de la stratégie MBAM (par exemple, 128-bits avec diffuseur).</p></td>
</tr>
<tr class="even">
<td align="left"><p>Stratégie: lecteur du système d’exploitation</p></td>
<td align="left"><p>Indique si le chiffrement est requis pour le système d’exploitation et le type de protecteur approprié.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Stratégie: disque de données fixe</p></td>
<td align="left"><p>Indique si le chiffrement est requis pour le lecteur de données fixes.</p></td>
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

 

**Rapport de conformité de l’ordinateur BitLocker: champs volume de l’ordinateur**

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
<td align="left"><p>Type de protecteur sélectionné par le biais de la stratégie utilisée pour chiffrer un système d’exploitation ou un lecteur de données fixe. Les types de protecteur valides pour un système d’exploitation sont TPM ou TPM + NIP. Le type de protecteur valide pour un lecteur de données fixe est un mot de passe.</p></td>
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


[Surveillance et création de rapports de la conformité BitLocker avec MBAM2.5](monitoring-and-reporting-bitlocker-compliance-with-mbam-25.md)

 

## Vous avez une suggestion pour MBAM?
- Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring) 
- Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





