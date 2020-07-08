---
title: Présentation des rapports autonomes MBAM2.5
description: Présentation des rapports autonomes MBAM2.5
author: dansimp
ms.assetid: 78b5aaf4-8257-4722-8eb9-e0de48db6a11
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 45e84c7c3b2bcb1602890c7c5a09592324da691e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804482"
---
# Présentation des rapports autonomes MBAM2.5


Cette rubrique décrit les rapports disponibles lors de l’exécution de Microsoft BitLocker administration et de la surveillance (MBAM) dans la topologie autonome.

**Remarque**  
Si vous exécutez MBAM avec la topologie d’intégration de Configuration Manager, vous générez des rapports à partir de Configuration Manager plutôt que d’MBAM. Pour plus d’informations sur ces rapports, voir [afficher des rapports 2,5 MBAM pour la topologie d’intégration de Configuration Manager](viewing-mbam-25-reports-for-the-configuration-manager-integration-topology.md) .



## Présentation des rapports de topologie autonomes de MBAM


MBAM fournit trois types de rapports que vous pouvez utiliser pour surveiller votre organisation pour la conformité avec BitLocker:

-   [Rapport de conformité d’entreprise](#bkmk-enterprisecompliance)

-   [Rapport de conformité ordinateur](#bkmk-compliance)

-   [Rapport d’audit de récupération](#bkmk-recovery)

Pour accéder aux rapports MBAM lorsque vous exécutez MBAM dans la topologie autonome, ouvrez un navigateur Web, puis ouvrez le site Web d’administration et de surveillance. Dans la barre de menus de gauche, sélectionnez **rapports** . Dans la barre de menus supérieure, sélectionnez le type de rapport que vous souhaitez générer. Pour plus d’informations sur la génération de ces rapports, voir [génération de rapports MBAM 2,5 autonomes](generating-mbam-25-stand-alone-reports.md).

### <a href="" id="bkmk-enterprisecompliance"></a>Rapport de conformité d’entreprise

Utilisez ce type de rapport pour collecter des informations sur la conformité de BitLocker globale dans votre organisation. Vous pouvez utiliser des filtres pour affiner vos résultats de recherche et en savoir plus sur l’état de conformité et l’état d’erreur des ordinateurs au sein de votre organisation.

**Présentation de la conformité entreprise**

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
<td align="left"><p>Pourcentage d’exonération</p></td>
<td align="left"><p>Pourcentage d’ordinateurs exemptés de l’exigence de cryptage BitLocker.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>% Non exempté</p></td>
<td align="left"><p>Pourcentage d’ordinateurs non exemptés de l’exigence de cryptage BitLocker.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Conformes</p></td>
<td align="left"><p>Pourcentage d’ordinateurs conformes dans l’entreprise.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Non conforme</p></td>
<td align="left"><p>Pourcentage d’ordinateurs non conformes dans l’entreprise.</p></td>
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



**Détails de l’ordinateur de conformité d’entreprise**

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
<td align="left"><p>État de la conformité de l’ordinateur, conformément à la stratégie spécifiée pour l’ordinateur. Les États ne sont pas conformes et conformes. Pour plus d’informations sur l’interprétation des États de conformité, reportez-vous au tableau des États de conformité des rapports de conformité d’entreprise suivants.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Question</p></td>
<td align="left"><p>État indiquant si cet ordinateur est exempté de la stratégie BitLocker.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Détails de l’état de conformité</p></td>
<td align="left"><p>Messages d’erreur et de statut concernant l’état de conformité de l’ordinateur conformément à la stratégie spécifiée.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Dernier contact</p></td>
<td align="left"><p>Date et heure de la dernière connexion de l’ordinateur au serveur pour signaler l’état de la conformité. La fréquence de contact est configurable. Pour plus d’informations, consultez les paramètres de stratégie de groupe MBAM.</p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-compliance"></a>Rapport de conformité ordinateur

Utilisez ce type de rapport pour collecter des informations spécifiques à un ordinateur ou à un utilisateur.

Pour afficher ce rapport, cliquez sur le nom de l’ordinateur dans le rapport de conformité d’entreprise, ou tapez le nom de l’ordinateur dans le rapport de conformité de l’ordinateur. Ce rapport affiche des informations de chiffrement détaillées sur chaque lecteur (système d’exploitation et lecteurs de données fixes) sur un ordinateur. Il indique également la stratégie qui s’applique à chaque type de lecteur de l’ordinateur. Pour afficher les détails de chaque lecteur, développez l’entrée nom de l’ordinateur.

**Remarque**  
Ce rapport ne montre aucun État de cryptage des volumes de données amovibles.



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
<td align="left"><p>Nom de domaine complet sur lequel se trouve l’ordinateur client et est géré par MBAM.</p></td>
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
<td align="left"><p>État de conformité global de l’ordinateur géré par MBAM. Les États valides sont conformes et non conformes.</p>
<p>Notez que l’état de la conformité par lecteur (voir le tableau ci-dessous) est susceptible d’indiquer les différents États de conformité. Toutefois, ce champ correspond à cet état de conformité, conformément à la stratégie spécifiée.</p></td>
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
<td align="left"><p>Question</p></td>
<td align="left"><p>État indiquant si cet ordinateur est exempté de la stratégie BitLocker.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Fabricant</p></td>
<td align="left"><p>Nom de fabricant de l’ordinateur, tel qu’il apparaît dans le BIOS de l’ordinateur.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Modèle</p></td>
<td align="left"><p>Nom de modèle du fabricant d’ordinateurs, tel qu’il apparaît dans le BIOS de l’ordinateur.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Détails de l’état de conformité</p></td>
<td align="left"><p>Messages d’erreur et de statut concernant l’état de conformité de l’ordinateur, conformément à la stratégie spécifiée.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Dernier contact</p></td>
<td align="left"><p>Date et heure de la dernière connexion de l’ordinateur au serveur pour signaler l’état de la conformité. La fréquence de contact est configurable. Pour plus d’informations, consultez les paramètres de stratégie de groupe MBAM.</p></td>
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
<td align="left"><p>Type de protecteur sélectionné par le biais du paramètre de stratégie de groupe utilisé pour chiffrer un système d’exploitation ou un volume de données fixe.</p></td>
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



### <a href="" id="bkmk-recovery"></a>Rapport d’audit de récupération

Utilisez ce type de rapport pour auditer les utilisateurs qui ont demandé l’accès aux clés de récupération BitLocker. Le rapport propose plusieurs filtres basés sur les critères de filtre souhaités. Vous pouvez filtrer sur un type spécifique d’utilisateur (un utilisateur du support technique ou un utilisateur final), si la demande a échoué ou a abouti, le type spécifique de clé demandée et une plage de dates pendant laquelle la récupération s’est produite.

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
<td align="left"><p>Source de requête d’audit</p></td>
<td align="left"><p>Site à partir duquel la demande a été lancée. Cette entrée aura une des deux valeurs suivantes: <strong> portail libre-service </strong> ou <strong> support technique </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>État de la demande</p></td>
<td align="left"><p>État de la demande. Les statuts valides sont réussis (la clé a été récupérée) ou FAILED (la clé n’a pas été récupérée).</p></td>
</tr>
<tr class="even">
<td align="left"><p>Utilisateur du support technique</p></td>
<td align="left"><p>Utilisateur du support technique à l’origine de la demande de récupération de clé.</p>
<div class="alert">
<strong>Remarque</strong><br/><p>Si un utilisateur expérimenté du support technique récupère la clé sans spécifier d’utilisateur final, le <strong> champ d’utilisateur final </strong> sera vide. Un utilisateur du support technique standard doit spécifier l’utilisateur final, et cet utilisateur s’affichera dans ce champ.</p>
<p>Une récupération par le biais du portail en libre-service entraîne la liste de l’utilisateur à l’origine de la demande dans ce champ et dans le <strong> champ utilisateur final </strong> .</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>Utilisateur final</p></td>
<td align="left"><p>Utilisateur final à l’origine de la demande de récupération de la clé.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Ordinateur</p></td>
<td align="left"><p>Nom de l’ordinateur qui a été récupéré.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Type de clé</p></td>
<td align="left"><p>Type de clé demandée par l’utilisateur du support technique ou par l’utilisateur final. Les trois types de clés que MBAM recueille sont les suivants:</p>
<ul>
<li><p>Mot de passe de clé de récupération (utilisé pour récupérer un ordinateur en mode de récupération)</p></li>
<li><p>ID de clé de récupération (utilisé pour récupérer un ordinateur en mode de récupération pour le compte d’un autre utilisateur)</p></li>
<li><p>Hachage du mot de passe TPM (utilisé pour récupérer un ordinateur équipé d’un TPM verrouillé)</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Description de raison</p></td>
<td align="left"><p>Raison le type de clé spécifié a été requis par l’utilisateur du support technique ou par l’utilisateur final. Les raisons sont indiquées dans les fonctionnalités de récupération des lecteurs et de gestion du TPM du site Web d’administration et de surveillance. Les entrées valides sont du texte entré par l’utilisateur ou l’un des codes de raison suivants:</p>
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



**Remarque**  
Vous pouvez enregistrer des résultats de rapport dans un fichier en cliquant sur le bouton **Exporter** dans la barre de menus **rapports** .




## Rubriques connexes


[Surveillance et création de rapports de la conformité BitLocker avec MBAM2.5](monitoring-and-reporting-bitlocker-compliance-with-mbam-25.md)

[Génération des rapports MBAM2.5 autonomes](generating-mbam-25-stand-alone-reports.md)



## Vous avez une suggestion pour MBAM?
- Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring) 
- Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





