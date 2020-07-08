---
title: Compréhension des rapports MBAM
description: Compréhension des rapports MBAM
author: dansimp
ms.assetid: 34e4aaeb-7f89-41a1-b816-c6fe8397b060
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa64a4724c87a42774e569b556013bfec2ed5514
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809612"
---
# Compréhension des rapports MBAM


Microsoft BitLocker administration et analyse (MBAM) génère divers rapports pour contrôler l’utilisation et la conformité de BitLocker. Cette rubrique décrit les rapports MBAM à des fins de conformité d’entreprise, d’ordinateurs individuels, de compatibilité matérielle et d’activité de récupération de clés.

## Présentation des rapports


Pour accéder à la fonctionnalité rapports d’MBAM, ouvrez le site Web d’administration MBAM. Sélectionnez **rapports** dans le volet de navigation. Ensuite, dans le volet contenu principal, cliquez sur l’onglet correspondant à votre type de rapport: **rapport de conformité d’entreprise**, rapport de conformité d' **ordinateur**, rapport **d’audit matériel**ou **rapport d’audit de récupération**.

### Rapport de conformité d’entreprise

Un rapport de conformité d’entreprise fournit des informations sur la conformité de BitLocker globale au sein de votre organisation. Les filtres disponibles pour ce rapport vous permettent d’affiner vos résultats de recherche en fonction de l’état de conformité et de l’état d’erreur. Ce rapport s’exécute toutes les six heures.

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
<td align="left"><p>État de la conformité de l’ordinateur, selon la stratégie spécifiée pour l’ordinateur. Les États possibles sont non conformes et conformes. Pour plus d’informations, reportez-vous à la section État de conformité des rapports de conformité d’entreprise.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Question</p></td>
<td align="left"><p>État du matériel de l’ordinateur pour déterminer l’identification du type de matériel et si l’ordinateur est exempté d’une stratégie. Il existe trois États possibles: matériel inconnu (le type de matériel n’a pas été identifié par MBAM), exonéré du matériel (le type de matériel a été identifié et marqué comme exempt de la stratégie de MBAM) et non exempté (le matériel a été identifié et n’est pas exempt de la stratégie).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Utilisateurs d’appareils</p></td>
<td align="left"><p>Utilisateurs connus sur l’ordinateur géré par MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Détails de l’état de conformité</p></td>
<td align="left"><p>Messages d’erreur et de statut concernant l’état de conformité de l’ordinateur conformément à la stratégie spécifiée.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Dernier contact</p></td>
<td align="left"><p>Date et heure de la dernière connexion de l’ordinateur au serveur pour signaler l’état de la conformité. Ce temps est configurable. Voir paramètres de stratégie MBAM.</p></td>
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
<td align="left"><p>L’ordinateur n’est pas conforme conformément à la stratégie spécifiée, et le type de matériel n’a pas été indiqué comme exempt de la stratégie.</p></td>
<td align="left"><p>Cliquez sur <strong> nom </strong> de l’ordinateur pour développer le rapport de conformité de l’ordinateur et déterminer si l’état de chaque lecteur répond à la stratégie spécifiée. S’il s’agit d’un état de chiffrement indiquant que l’ordinateur n’est pas chiffré, il est possible que le chiffrement soit en cours de traitement ou qu’il y ait une erreur sur l’ordinateur. S’il n’y a aucune erreur, il est probable que l’ordinateur est toujours en train de se connecter ou de définir l’état de cryptage. Revenez à l’étape précédente pour déterminer si l’état change.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Conformes</p></td>
<td align="left"><p>Ne pas exempter</p></td>
<td align="left"><p>L’ordinateur est conforme conformément à la stratégie spécifiée.</p></td>
<td align="left"><p>Aucune action nécessaire. Vous pouvez également afficher le rapport de conformité de l’ordinateur pour vérifier l’état de l’ordinateur.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Conformes</p></td>
<td align="left"><p>Exemption matérielle</p></td>
<td align="left"><p>Si le type de matériel est exonéré. Quelle que soit la façon dont la stratégie est définie ou du statut individuel de chaque disque dur, l’état global est considéré comme conforme.</p></td>
<td align="left"><p>Aucune action nécessaire.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Conformes</p></td>
<td align="left"><p>Matériel inconnu</p></td>
<td align="left"><p>MBAM reconnaît le type de matériel, mais MBAM ne sait pas s’il est exempté ou n’est pas exempté. Ce problème se produit si l’administrateur n’a pas défini l’État compatible du matériel. Par conséquent, MBAM rétablit l’État conforme par défaut.</p></td>
<td align="left"><p>Il s’agit de l’état initial d’un nouveau client MBAM déployé. Il s’agit généralement d’un état temporaire. Même si l’administrateur a marqué le matériel comme étant compatible, il est possible qu’il y ait un délai important ou un délai d’attente configuré pour signaler l’état de l’ordinateur client. Prenez note de l’heure du dernier contact et recommencez après l’intervalle spécifié pour voir si l’État a changé. Si l’État n’a pas changé, il est possible qu’il y ait une erreur pour ce type d’ordinateur ou de matériel.</p></td>
</tr>
</tbody>
</table>

 

### Rapport de conformité ordinateur

Le rapport de conformité informatique affiche des informations spécifiques à un ordinateur ou à un utilisateur.

Le rapport de conformité informatique fournit des informations de chiffrement détaillées et des stratégies applicables pour chaque lecteur sur un ordinateur, notamment les lecteurs de systèmes d’exploitation et les lecteurs de données fixes. Pour afficher ce type de rapport, cliquez sur le nom de l’ordinateur dans le rapport de conformité d’entreprise ou tapez le nom de l’ordinateur dans le rapport de conformité de l’ordinateur. Pour afficher les détails de chaque lecteur, développez l’entrée nom de l’ordinateur.

**Remarques**  Ce rapport ne fournit pas d’état de chiffrement pour les volumes de données amovibles.

 

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
<td align="left"><p>Nom de l’ordinateur DNS spécifié par l’utilisateur qui est géré par MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Nom de domaine</p></td>
<td align="left"><p>Nom de domaine complet sur lequel se trouve l’ordinateur client et est géré par MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Type d’ordinateur</p></td>
<td align="left"><p>Type de portabilité de l’ordinateur. Les types valides ne sont pas portables et portables.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Systèmed’exploitation</p></td>
<td align="left"><p>Type de système d’exploitation installé sur l’ordinateur client géré MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>État de la conformité</p></td>
<td align="left"><p>État de conformité global de l’ordinateur géré par MBAM. Les États valides sont conformes et non conformes. S’il est possible d’utiliser des lecteurs compatibles et non conformes sur le même ordinateur, ce champ indique la conformité globale de l’ordinateur par stratégie spécifiée.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Force de Cypher de stratégie</p></td>
<td align="left"><p>Le niveau de cryptage sélectionné par l’administrateur lors de la spécification de la stratégie MBAM. Par exemple, 128-bit avec diffuseur</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Lecteur du système d’exploitation de la stratégie</p></td>
<td align="left"><p>Indique si le chiffrement est requis pour les e/S et le type de protecteur applicable.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Policy Data-Fixed Data</p></td>
<td align="left"><p>Indique si le chiffrement est requis pour le lecteur fixe.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Lecteur de données amovibles pour une stratégie</p></td>
<td align="left"><p>Indique si le chiffrement est requis pour le lecteur amovible.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Utilisateurs d’appareils</p></td>
<td align="left"><p>Fournit l’identité des utilisateurs connus de l’ordinateur.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Question</p></td>
<td align="left"><p>Indique si le type de matériel de l’ordinateur est reconnu par MBAM et, si ce dernier a été signalé comme exempt de la stratégie. Il existe trois États: matériel inconnu (le type de matériel n’a pas été identifié par MBAM); Exemption matérielle (le type de matériel a été identifié et est marqué comme exempt de la stratégie MBAM); et non exempté (le matériel a été identifié et n’est pas exempté de la stratégie).</p></td>
</tr>
<tr class="even">
<td align="left"><p>Fabricant</p></td>
<td align="left"><p>Le nom du fabricant de l’ordinateur tel qu’il apparaît dans le BIOS de l’ordinateur.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Modèle</p></td>
<td align="left"><p>Le nom du modèle de fabricant d’ordinateurs tel qu’il apparaît dans le BIOS de l’ordinateur.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Détails de l’état de conformité</p></td>
<td align="left"><p>Messages d’erreur et d’état de l’état de conformité de l’ordinateur conformément à la stratégie spécifiée.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Dernier contact</p></td>
<td align="left"><p>Date et heure de la dernière connexion de l’ordinateur au serveur pour signaler l’état de la conformité. T</p></td>
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
<td align="left"><p>Lettre du lecteur de l’ordinateur qui a été affectée à ce lecteur particulier par l’utilisateur.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Type de lecteur</p></td>
<td align="left"><p>Type de lecteur. Les valeurs valides sont le lecteur du système d’exploitation et le lecteur de données fixes. Il s’agit de disques physiques plutôt que de volumes logiques.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Cypher Strength</p></td>
<td align="left"><p>Force de cryptage sélectionnée par l’administrateur lors de la spécification de la stratégie MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Type de protecteur</p></td>
<td align="left"><p>Type de protecteur sélectionné via une stratégie utilisée pour chiffrer un système d’exploitation ou un volume fixe. Les types de protecteur valides sur un lecteur de système d’exploitation sont TPM ou TPM + NIP. Le seul type de protecteur valide pour un volume de données fixe est Password.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>État de protecteur</p></td>
<td align="left"><p>Ce champ indique si l’ordinateur a activé le type de protecteur spécifié dans la stratégie. Les États valides sont ACTIVÉs ou désactivés.</p></td>
</tr>
<tr class="even">
<td align="left"><p>État du chiffrement</p></td>
<td align="left"><p>Il s’agit de l’état de chiffrement actuel du lecteur. Les États valides sont chiffrés, non chiffrés et chiffrés.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>État de la conformité</p></td>
<td align="left"><p>Indique si le lecteur est conforme à la stratégie. Les États ne sont pas conformes et conformes.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Détails de l’état de conformité</p></td>
<td align="left"><p>Contient des messages d’erreur et de statut concernant l’état de conformité de l’ordinateur.</p></td>
</tr>
</tbody>
</table>

 

### Rapport d’audit matériel

Ce rapport peut vous aider à effectuer le suivi des modifications apportées à l’état de compatibilité matérielle de modèles et de modèles d’ordinateurs spécifiques. Pour vous aider à affiner vos résultats de recherche, ce rapport inclut le filtrage sur des critères tels que le type de modification et l’heure d’apparition. Le suivi de chaque modification d’état dépend de l’utilisateur et de la date et de l’heure. Le type de matériel est automatiquement rempli par l’agent MBAM qui s’exécute sur l’ordinateur client. Ce rapport effectue le suivi des modifications apportées par l’utilisateur aux informations collectées directement depuis l’ordinateur géré par MBAM. Un changement d’administration classique consiste à changer de compatibilité en incompatibilité. Toutefois, l’administrateur peut également modifier n’importe quel champ.

**Champs du rapport d’audit matériel**

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
<td align="left"><p>Date et heure</p></td>
<td align="left"><p>Date et heure auxquelles une modification a été apportée au type de matériel. Notez que chaque type de matériel unique est affecté à au moins une entrée.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Utilisateur</p></td>
<td align="left"><p>Utilisateur administratif ayant modifié le changement pour l’entrée en particulier.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Changer de type</p></td>
<td align="left"><p>Type de modification apportée aux informations de type de matériel. Les valeurs valides sont addition (nouvelle entrée), mise à jour (modifier une entrée existante) ou suppression (suppression d’entrée existante).</p></td>
</tr>
<tr class="even">
<td align="left"><p>Valeur d’origine</p></td>
<td align="left"><p>Valeur de la spécification du type de matériel avant la modification.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Valeur actuelle</p></td>
<td align="left"><p>Valeur de la spécification de type matérielle une fois la modification effectuée.</p></td>
</tr>
</tbody>
</table>

 

### Rapport d’audit de récupération

Le rapport d’audit de récupération peut vous aider à contrôler les utilisateurs qui ont demandé l’accès aux clés de récupération. Les critères de filtre pour ce rapport incluent le type d’utilisateur à l’origine de la demande, le type de clé demandée, l’heure d’apparition, la réussite ou l’échec, l’heure d’apparition et le type d’utilisateur demandant (support technique, utilisateur final). Ce rapport permet aux administrateurs de produire des rapports contextuels en fonction de vos besoins.

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
<td align="left"><p>État de la demande. Les statuts valides sont réussis (la clé a été récupérée) ou FAILED (la clé n’est pas récupérée).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Utilisateur du support technique</p></td>
<td align="left"><p>L’utilisateur du support technique ayant lancé la demande de récupération de la clé. Si l’utilisateur du support technique récupère la clé pour le compte d’un utilisateur final, le champ utilisateur final sera vide.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Utilisateur</p></td>
<td align="left"><p>Utilisateur final à l’origine de la demande de récupération de la clé.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Type de clé</p></td>
<td align="left"><p>Type de clé demandée. MBAM collecte trois types de clé: mot de passe de clé de récupération (pour récupérer un ordinateur en mode de récupération); ID de la clé de récupération (pour récupérer un ordinateur en mode de récupération pour le compte d’un autre utilisateur); et le hachage du mot de passe du module de plateforme sécurisée (TPM) (pour récupérer un ordinateur avec un TPM verrouillé).</p></td>
</tr>
<tr class="even">
<td align="left"><p>Description de raison</p></td>
<td align="left"><p>Raison d’une demande du type de clé spécifié. Les raisons sont indiquées dans les fonctionnalités de récupération des lecteurs et de gestion du TPM du site Web d’administration. Les entrées valides incluent le texte entré par l’utilisateur ou l’un des codes de raison suivants:</p>
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
</ul>
<p></p></td>
</tr>
</tbody>
</table>

 

**Remarques**  Pour enregistrer les résultats d’un rapport dans un fichier, cliquez sur le bouton **Exporter** dans la barre de menus rapports.

 

## Rubriques connexes


[Surveillance et création de rapports de la conformité BitLocker avec MBAM1.0](monitoring-and-reporting-bitlocker-compliance-with-mbam-10.md)

 

 





