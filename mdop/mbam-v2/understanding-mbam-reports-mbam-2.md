---
title: Compréhension des rapports MBAM
description: Compréhension des rapports MBAM
author: dansimp
ms.assetid: 8778f333-760e-4f26-acb4-4e73b6fbb536
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3c3ca5e4da4cbcea80c87520f0ecd05e1e7d6be0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810181"
---
# Compréhension des rapports MBAM


Si vous avez choisi la topologie autonome lors de l’installation de Microsoft BitLocker administration et de la surveillance (MBAM), vous pouvez exécuter différents rapports dans MBAM pour contrôler l’utilisation et la conformité de BitLocker. MBAM indique la conformité et d’autres informations sur tous les ordinateurs et appareils qu’il gère. Les informations contenues dans cette rubrique peuvent être utilisées pour vous aider à comprendre les rapports d’administration et de surveillance de BitLocker pour les entreprises et les rapports de compatibilité des ordinateurs individuels.

**Remarques**  Si vous avez choisi la topologie Configuration Manager lors de l’installation de Microsoft BitLocker administration et de la surveillance (MBAM), les rapports sont générés à partir de Configuration Manager plutôt que d’MBAM. Pour plus d’informations sur les rapports qui sont exécutés à partir de Configuration Manager, voir [Présentation des rapports MBAM dans Configuration Manager](understanding-mbam-reports-in-configuration-manager.md).

 

## Présentation des rapports


Pour accéder à la fonctionnalité rapports d’administration et de contrôle Microsoft BitLocker, ouvrez un navigateur Web et ouvrez le site Web d’administration et de surveillance. Dans la barre de menus de gauche, sélectionnez **rapports** , puis dans la barre de menus supérieure, sélectionnez le type de rapport que vous souhaitez générer.

### Rapport de conformité d’entreprise

Utilisez ce type de rapport pour collecter des informations sur la conformité de BitLocker globale dans votre organisation. Vous pouvez utiliser des filtres différents pour affiner vos résultats de recherche en fonction de l’état de conformité et de l’erreur. Les informations du rapport sont actualisées toutes les six heures.

**Champs rapport de conformité entreprise**

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
<td align="left"><p>Nom DNS spécifié par l’utilisateur géré par MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Nom de domaine</p></td>
<td align="left"><p>Nom de domaine complet sur lequel se trouve l’ordinateur client et est géré par MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>État de la conformité</p></td>
<td align="left"><p>État de la conformité de l’ordinateur, conformément à la stratégie spécifiée pour l’ordinateur. Les États ne sont pas conformes et conformes. Pour plus d’informations sur l’interprétation des États de conformité, voir le tableau des États de conformité des rapports de conformité d’entreprise.</p></td>
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

 

**États de conformité des rapports de conformité d’entreprise**

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">État de la conformité</th>
<th align="left">Question</th>
<th align="left">Description</th>
<th align="left">Action de l’utilisateur</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Non conforme</p></td>
<td align="left"><p>Ne pas exempter</p></td>
<td align="left"><p>L’ordinateur n’est pas conforme, conformément à la stratégie spécifiée.</p></td>
<td align="left"><p>Développez les détails du rapport de conformité de l’ordinateur en cliquant sur <strong> nom </strong> de l’ordinateur et déterminez si l’état de chaque lecteur répond à la stratégie spécifiée. S’il s’agit de l’état de chiffrement indiquant que l’ordinateur n’est pas chiffré, le chiffrement est peut-être en cours de traitement ou il y a une erreur sur l’ordinateur. S’il n’y a aucune erreur, il est probable que l’ordinateur est toujours en train de se connecter ou de définir l’état de cryptage. Revenez à l’étape précédente pour déterminer si l’état change.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Conformes</p></td>
<td align="left"><p>Ne pas exempter</p></td>
<td align="left"><p>Votre ordinateur est conforme, conformément à la stratégie spécifiée.</p></td>
<td align="left"><p>Aucune action n’est nécessaire; l’état de l’ordinateur peut être confirmé en consultant le rapport de conformité de l’ordinateur.</p></td>
</tr>
</tbody>
</table>

 

### Rapport de conformité ordinateur

Utilisez ce type de rapport pour collecter des informations spécifiques à un ordinateur ou à un utilisateur.

Ce rapport peut être affiché en cliquant sur le nom de l’ordinateur dans le rapport de conformité d’entreprise, ou en tapant le nom de l’ordinateur dans le rapport de conformité informatique. Le rapport de conformité informatique fournit des informations de chiffrement détaillées sur chaque lecteur (système d’exploitation et lecteurs de données fixes) sur un ordinateur, ainsi que les indications de la stratégie appliquée à chaque type de lecteur de l’ordinateur. Pour afficher les détails de chaque lecteur, développez l’entrée nom de l’ordinateur.

**Remarques**  L’état de chiffrement des volumes de données amovibles ne s’affiche pas dans le rapport.

 

**Champs du rapport de conformité ordinateur**

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
<td align="left"><p>Type de système d’exploitation détecté sur l’ordinateur client géré par MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>État de la conformité</p></td>
<td align="left"><p>État de conformité global de l’ordinateur géré par MBAM. Les États valides sont conformes et non conformes. Notez que l’état de la conformité par lecteur (voir le tableau ci-dessous) est susceptible d’indiquer les différents États de conformité. Toutefois, ce champ correspond à cet état de conformité, conformément à la stratégie spécifiée.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Niveau de cryptage de la stratégie</p></td>
<td align="left"><p>Force de cryptage sélectionnée par l’administrateur lors de la spécification de la stratégie MBAM (par exemple, 128-bits avec diffuseur).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Lecteur du système d’exploitation de la stratégie</p></td>
<td align="left"><p>Indique si le chiffrement est requis pour le système d’exploitation et le type de protecteur approprié.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Politique-lecteur de données fixes</p></td>
<td align="left"><p>Indique si le chiffrement est requis pour le lecteur de données fixes.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Lecteur de données amovibles pour une stratégie</p></td>
<td align="left"><p>Indique si le chiffrement est requis pour le lecteur amovible.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Utilisateurs d’appareils</p></td>
<td align="left"><p>Utilisateurs connus sur l’ordinateur géré par MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Fabricant</p></td>
<td align="left"><p>Nom de fabricant de l’ordinateur, tel qu’il apparaît dans le BIOS de l’ordinateur.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Modèle</p></td>
<td align="left"><p>Nom de modèle du fabricant d’ordinateurs, tel qu’il apparaît dans le BIOS de l’ordinateur.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Détails de l’état de conformité</p></td>
<td align="left"><p>Messages d’erreur et d’état de l’état de conformité de l’ordinateur, conformément à la stratégie spécifiée.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Dernier contact</p></td>
<td align="left"><p>Date et heure de la dernière connexion de l’ordinateur au serveur pour signaler l’état de la conformité. La fréquence de contact est configurable (voir paramètres de la stratégie MBAM).</p></td>
</tr>
</tbody>
</table>

 

**Champs du rapport de conformité informatique**

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
<td align="left"><p>Type de protecteur</p></td>
<td align="left"><p>Type de protecteur sélectionné par le biais de la stratégie utilisée pour chiffrer un système d’exploitation ou un volume de données fixe.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>État de protecteur</p></td>
<td align="left"><p>Indique que l’ordinateur géré par MBAM a activé le type de protecteur qui est spécifié dans la stratégie. Les États valides sont ACTIVÉs ou désactivés.</p></td>
</tr>
<tr class="even">
<td align="left"><p>État du chiffrement</p></td>
<td align="left"><p>État du chiffrement du lecteur. Les États valides sont chiffrés, non chiffrés et chiffrés.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>État de la conformité</p></td>
<td align="left"><p>État indiquant s’il est conforme à la stratégie. Les États ne sont pas conformes et conformes.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Détails de l’état de conformité</p></td>
<td align="left"><p>Messages d’erreur et de statut de l’état de conformité de l’ordinateur, conformément à la stratégie spécifiée.</p></td>
</tr>
</tbody>
</table>

 

### Rapport d’audit de récupération

Utilisez ce type de rapport pour auditer les utilisateurs qui ont demandé l’accès aux clés de récupération. Le rapport propose plusieurs filtres basés sur les critères de filtre souhaités. Les utilisateurs peuvent filtrer sur un type spécifique d’utilisateur, à savoir un utilisateur du support technique ou un utilisateur final, si la demande a échoué ou a abouti, le type spécifique de clé demandée et une plage de dates pendant laquelle la récupération s’est produite. L’administrateur peut générer des rapports contextuels en fonction de vos besoins.

**Champs du rapport d’audit de récupération**

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
<td align="left"><p>Demander une date et une heure</p></td>
<td align="left"><p>Date et heure auxquelles une demande de récupération de clé a été effectuée par un utilisateur final ou un utilisateur du support technique.</p></td>
</tr>
<tr class="even">
<td align="left"><p>État de la demande</p></td>
<td align="left"><p>État de la demande. Les statuts valides sont réussis (la clé a été récupérée) ou FAILED (la clé n’a pas été récupérée).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Utilisateur du support technique</p></td>
<td align="left"><p>Utilisateur de l’assistance technique ayant lancé la demande de récupération de la clé. Remarque: si l’utilisateur du support technique récupère la clé de la part d’un utilisateur final, le champ d’utilisateur final sera vide.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Utilisateur</p></td>
<td align="left"><p>Utilisateur final à l’origine de la demande de récupération de la clé.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Type de clé</p></td>
<td align="left"><p>Type de clé demandée par l’utilisateur du support technique ou par l’utilisateur final. Les trois types de clés que MBAM recueille sont: mot de passe de la clé de récupération (utilisé pour la récupération d’un ordinateur en mode récupération), ID de la clé de récupération (utilisé pour récupérer un ordinateur en mode de récupération pour le compte d’un autre utilisateur)</p></td>
</tr>
<tr class="even">
<td align="left"><p>Description de raison</p></td>
<td align="left"><p>Raison le type de clé spécifié a été requis par l’utilisateur du support technique ou par l’utilisateur final. Les raisons sont indiquées dans les fonctionnalités de récupération des lecteurs et de gestion du TPM du site Web d’administration et de surveillance. Le texte entré par l’utilisateur est le texte entré par l’utilisateur ou l’un des codes de raison suivants:</p>
<ul>
<li><p>Ordre d’amorçage du système d’exploitation modifié</p></li>
<li><p>Modification du BIOS</p></li>
<li><p>Modification des fichiers du système d’exploitation</p></li>
<li><p>Clé de démarrage perdue</p></li>
<li><p>Code confidentiel perdu</p></li>
<li><p>Réinitialisation du TPM</p></li>
<li><p>Phrase de passe perdue</p></li>
<li><p>Carte Smartcard perdue</p></li>
<li><p>Réinitialiser le verrouillage du code confidentiel</p></li>
<li><p>Activer le module de plateforme sécurisée</p></li>
<li><p>Désactiver le module de plateforme sécurisée</p></li>
<li><p>Changer le mot de passe du TPM</p></li>
<li><p>Vider le TPM</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

**Remarques**  Vous pouvez enregistrer des résultats de rapport dans un fichier en cliquant sur le bouton **Exporter** dans la barre de menus rapports. Pour plus d’informations sur l’exécution des rapports MBAM, voir [génération de rapports MBAM](how-to-generate-mbam-reports-mbam-2.md).

 

## Rubriques connexes


[Surveillance et création de rapports de la conformité BitLocker avec MBAM2.0](monitoring-and-reporting-bitlocker-compliance-with-mbam-20-mbam-2.md)

 

 





