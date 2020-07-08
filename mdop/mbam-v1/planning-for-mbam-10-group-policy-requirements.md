---
title: Planification des exigences en matière de stratégie de groupe MBAM1.0
description: Planification des exigences en matière de stratégie de groupe MBAM1.0
author: dansimp
ms.assetid: 0fc9c509-7850-4a8e-bb82-b949025bcb02
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f5061748107dc1d00baa41188b8cf240ec187317
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804225"
---
# Planification des exigences en matière de stratégie de groupe MBAM1.0


La gestion du client Microsoft BitLocker administration et surveillance (MBAM) nécessite l’application de paramètres de stratégie de groupe personnalisés. Cette rubrique décrit les options de stratégie disponibles pour l’objet de stratégie de groupe (GPO) lorsque vous utilisez MBAM pour gérer le chiffrement de lecteur BitLocker au sein de l’entreprise.

**Important**  
MBAM n’utilise pas les paramètres d’objet GPO par défaut pour le chiffrement de lecteur BitLocker Windows. Si les paramètres par défaut sont activés, ils peuvent entraîner un comportement en conflit. Pour permettre à MBAM de gérer BitLocker, vous devez définir les paramètres de stratégie d’objet de stratégie de groupe après avoir installé le modèle de stratégie de groupe MBAM.



Après avoir installé le modèle de stratégie de groupe MBAM, vous pouvez afficher et modifier les paramètres de stratégie d’objets de stratégie de groupe MBAM personnalisés disponibles qui permettent à MBAM de gérer le chiffrement de l’entreprise BitLocker. Le modèle de stratégie de groupe MBAM doit être installé sur un ordinateur capable d’exécuter la console de gestion des stratégies de groupe (GPMC) ou la technologie de gestion des stratégies de groupe avancée (AGPM). Pour modifier l’objet de stratégie de groupe applicable, ouvrez le GPMC ou AGPM, puis naviguez jusqu’au nœud d’objet de stratégie de groupe suivant: **Configuration ordinateur** \\ **modèles d’administration** \\ **composants Windows**- \\ **MDOP MBAM (gestion de BitLocker)**.

Le nœud de l’objet de stratégie de groupe MDOP MBAM (gestion de BitLocker) contient quatre paramètres de stratégie globale et quatre nœuds de paramètres d’objet de stratégie de groupe enfants, respectivement. Les quatre paramètres de stratégie globale de l’objet de stratégie de groupe sont: gestion du client, lecteur fixe, lecteur du système d’exploitation et lecteur amovible. Les sections suivantes fournissent des définitions de stratégie et des paramètres de stratégie suggérés pour vous aider à planifier les exigences des paramètres de stratégie d’objet de stratégie de MBAM.

**Remarque**  
Pour plus d’informations sur la configuration des paramètres d’objet de stratégie de groupe suggérés au minimum pour permettre à MBAM de gérer le chiffrement BitLocker, voir [Comment modifier les paramètres de l’objet de stratégie de groupe MBAM 1,0](how-to-edit-mbam-10-gpo-settings.md).



## Définitions de stratégies globales


Cette section décrit les définitions de stratégies globales de MBAM, qui se trouvent dans le nœud d’objet GPO suivant: **Configuration ordinateur** \\ **modèles d’administration** \\ **composants Windows** \\ **MDOP MBAM (gestion de BitLocker)**.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nom de la stratégie</th>
<th align="left">Vue d’ensemble et paramètre de stratégie suggéré</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Choisir la méthode de chiffrement de lecteur et la puissance de chiffrement</p></td>
<td align="left"><p>Configuration suggérée: <strong> non configuré</strong></p>
<p>Configurez cette stratégie pour utiliser une méthode de chiffrement et une force de chiffrement spécifiques.</p>
<p>Lorsque cette stratégie n’est pas configurée, BitLocker utilise la méthode de chiffrement par défaut de AES 128-bit avec diffuseur ou la méthode de chiffrement spécifiée par le script de configuration.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Empêcher le remplacement de mémoire lors du redémarrage</p></td>
<td align="left"><p>Configuration suggérée: <strong> non configuré</strong></p>
<p>Configurez cette stratégie pour améliorer les performances de redémarrage sans remplacer les secrets de BitLocker en mémoire lors du redémarrage.</p>
<p>Lorsque cette stratégie n’est pas configurée, les secrets BitLocker sont supprimés de la mémoire lors du redémarrage de l’ordinateur.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Valider la règle d’utilisation des certificats de carte à puce</p></td>
<td align="left"><p>Configuration suggérée: <strong> non configuré</strong></p>
<p>Configurez cette stratégie pour utiliser la protection BitLocker basée sur un certificat SmartCard.</p>
<p>Lorsque cette stratégie n’est pas configurée, un identificateur d’objet par défaut 1.3.6.1.4.1.311.67.1.1 est utilisé pour spécifier un certificat.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Fournir les identificateurs uniques pour votre organisation</p></td>
<td align="left"><p>Configuration suggérée: <strong> non configuré</strong></p>
<p>Configurez cette stratégie pour utiliser un agent de récupération des données basé sur un certificat ou le lecteur BitLocker to go.</p>
<p>Lorsque cette stratégie n’est pas configurée, le <strong> champ d’identification </strong> n’est pas utilisé.</p>
<p>Si votre entreprise utilise des mesures de sécurité plus importantes, vous pouvez configurer <strong> le </strong> champ d’identification pour vous assurer que tous les périphériques USB disposent de ce jeu de champs et qu’ils sont alignés avec ce paramètre de stratégie de groupe.</p></td>
</tr>
</tbody>
</table>



## Définitions de la stratégie de gestion du client


Cette section décrit les définitions de la stratégie de gestion des clients pour MBAM, qui se trouvent sur le nœud d’objet GPO suivant: **Configuration ordinateur** \\ **modèles d’administration** \\ **composants Windows** \\ **MDOP MBAM (gestion de BitLocker)**  \\  **Client Management**.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nom de la stratégie</th>
<th align="left">Vue d’ensemble et paramètres de stratégie suggérés</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Configurer les services de MBAM</p></td>
<td align="left"><p>Configuration suggérée: <strong> activée</strong></p>
<ul>
<li><p><strong>Point de terminaison du service matériel et de récupération MBAM </strong> . Il s’agit du premier paramètre de stratégie que vous devez configurer pour activer la gestion du chiffrement BitLocker du client MBAM. Pour ce paramètre, entrez l’emplacement du point de terminaison de la même façon que l’exemple suivant: <strong> http:// </strong><em> &lt; MBAM administration et surveillance &gt; </em><strong> du nom du serveur: </strong><em> &lt; Portage le service Web est lié à &gt; </em><strong> /MBAMRecoveryAndHardwareService/CoreService.svc </strong> .</p></li>
<li><p><strong>Sélectionnez les informations de récupération BitLocker à stocker </strong> . Ce paramètre de stratégie vous permet de configurer le service de récupération de clés pour sauvegarder les informations de récupération de BitLocker. Il vous permet également de configurer le service de rapport d’État pour la collecte des rapports de conformité et d’audit. La stratégie fournit une méthode d’administration permettant de récupérer les données chiffrées par BitLocker afin d’éviter la perte de données en raison de l’absence d’informations clés. Le rapport d’État et l’activité de récupération de clés seront automatiquement et en silence vers l’emplacement du serveur du rapport configuré.</p>
<p>Si vous ne configurez pas ou si vous désactivez ce paramètre de stratégie, les informations de récupération de clé ne seront pas enregistrées, et le rapport d’État et les activités de récupération de clés ne seront pas signalés au serveur. Lorsque ce paramètre est défini sur <strong> mot de passe de récupération et sur le package de clé </strong> , le mot de passe de récupération et le package de clé seront automatiquement sauvegardés sur l’emplacement du serveur de récupération de clé configuré.</p></li>
<li><p><strong>Entrez la fréquence de vérification de l’état du client en minutes </strong> . Ce paramètre de stratégie gère la fréquence à laquelle le client vérifie les stratégies de protection BitLocker et l’état de l’ordinateur client. Ce paramètre gère également la fréquence d’enregistrement de l’état de conformité du client sur le serveur. Le client vérifie les stratégies de protection de BitLocker et l’État sur l’ordinateur client et il sauvegarde également la clé de récupération du client à la fréquence configurée.</p>
<p>Définissez cette fréquence en fonction de la configuration requise établie par votre entreprise sur la fréquence de vérification de l’état de conformité de l’ordinateur et la fréquence de sauvegarde de la clé de récupération du client.</p></li>
<li><p><strong>Point de terminaison du service de rapport d’État MBAM </strong> . Il s’agit du deuxième paramètre de stratégie que vous devez configurer pour activer la gestion du chiffrement BitLocker du client MBAM. Pour ce paramètre, entrez l’emplacement du point de terminaison en utilisant l’exemple suivant: <strong> http:// </strong><em> &lt; MBAM administration et surveillance &gt; </em><strong> du nom du serveur: </strong><em> &lt; Portage le service Web est lié à &gt; </em><strong> /MBAMComplianceStatusService/StatusReportingService. SVC </strong> .</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Autoriser la vérification de compatibilité matérielle</p></td>
<td align="left"><p>Configuration suggérée: <strong> activée</strong></p>
<p>Ce paramètre de stratégie vous permet de gérer la vérification de la compatibilité matérielle avant d’activer la protection de BitLocker sur des lecteurs d’ordinateurs clients MBAM.</p>
<p>Vous devez activer cette option de stratégie si votre entreprise dispose d’anciens matériels ou d’ordinateurs qui ne prennent pas en charge le module de plateforme sécurisée (TPM). Si l’un de ces critères est vrai, activez la vérification de compatibilité matérielle pour vous assurer que MBAM est appliqué uniquement aux modèles d’ordinateurs qui prennent en charge BitLocker. Si tous les ordinateurs de votre organisation prennent en charge BitLocker, vous n’avez pas à déployer la compatibilité matérielle et vous pouvez définir cette stratégie sur <strong> non configuré </strong> .</p>
<p>Si vous activez ce paramètre de stratégie, le modèle de l’ordinateur est validé par rapport à la liste de compatibilité matérielle une fois toutes les 24 heures, avant que la stratégie ne soit activée pour la protection BitLocker sur un lecteur d’ordinateur.</p>
<div class="alert">
<strong>Remarque</strong><br/><p>Avant d’activer ce paramètre de stratégie, assurez-vous d’avoir configuré le <strong> paramètre de point de terminaison de récupération et de service matériel MBAM </strong> dans les <strong> options configurer la stratégie des services MBAM </strong> .</p>
</div>
<div>

</div>
<p>Si vous désactivez ou ne configurez pas ce paramètre de stratégie, le modèle ordinateur n’est pas validé par rapport à la liste de compatibilité matérielle.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Configurer une stratégie d’exemption des utilisateurs</p></td>
<td align="left"><p>Configuration suggérée: <strong> non configuré</strong></p>
<p>Ce paramètre de stratégie vous permet de configurer une adresse de site Web, une adresse de messagerie ou un numéro de téléphone qui demande à l’utilisateur d’être exempté du chiffrement BitLocker.</p>
<p>Si vous activez ce paramètre de stratégie et indiquez une adresse de site Web, une adresse de messagerie ou un numéro de téléphone, les utilisateurs verront une boîte de dialogue contenant des instructions sur la façon d’appliquer une exemption de protection BitLocker. Pour plus d’informations sur l’activation des exemptions de chiffrement BitLocker pour les utilisateurs, voir <a href="how-to-manage-user-bitlocker-encryption-exemptions-mbam-1.md" data-raw-source="[How to Manage User BitLocker Encryption Exemptions](how-to-manage-user-bitlocker-encryption-exemptions-mbam-1.md)"> Comment gérer les exemptions de chiffrement BitLocker de l’utilisateur </a> .</p>
<p>Si vous désactivez ou ne configurez pas ce paramètre de stratégie, les instructions relatives à l’application d’une demande d’exemption ne seront pas présentées aux utilisateurs.</p>
<div class="alert">
<strong>Remarque</strong><br/><p>L’exemption des utilisateurs est gérée par utilisateur et non par ordinateur. Si plusieurs utilisateurs se connectent sur le même ordinateur et qu’un utilisateur n’est pas exempté, l’ordinateur est crypté.</p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



## Définitions de stratégies de disque fixes


Cette section décrit les définitions de stratégie de lecteur fixes pour MBAM, qui se trouvent dans le nœud d’objet de stratégie de groupe suivant: **Configuration ordinateur** \\ **modèles d’administration** \\ **composants Windows** \\ **MDOP MBAM (gestion de BitLocker)**  \\  **Fixed Drive**.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nom de la stratégie</th>
<th align="left">Vue d’ensemble et paramètre de stratégie suggéré</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Paramètres de chiffrement des lecteurs de données fixes</p></td>
<td align="left"><p>Configuration suggérée: <strong> activé </strong> , puis activez la case <strong> à cocher Activer le verrouillage automatique des données </strong> si le volume du système d’exploitation doit être chiffré.</p>
<p>Ce paramètre de stratégie vous permet de gérer l’activation ou non du chiffrement des lecteurs fixes.</p>
<p>Lorsque vous activez cette stratégie, ne désactivez pas la <strong> stratégie configurer l’utilisation du mot de passe pour les lecteurs de données fixes </strong> .</p>
<p>Si la <strong> case à cocher Activer le verrouillage automatique des données du disque </strong> est activée, le volume du système d’exploitation doit être chiffré.</p>
<p>Si vous activez ce paramètre de stratégie, les utilisateurs doivent placer tous les disques fixes sous protection BitLocker, qui chiffreront les lecteurs.</p>
<p>Si vous ne configurez pas cette stratégie ou si vous désactivez ce paramètre, les utilisateurs ne sont pas obligés de placer des lecteurs corrigés dans la protection BitLocker.</p>
<p>Si vous désactivez cette stratégie, l’agent MBAM déchiffre les lecteurs fixes chiffrés.</p>
<p>Si le chiffrement du volume du système d’exploitation n’est pas nécessaire, décochez la <strong> case Activer le verrouillage automatique du lecteur de données </strong> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Refuser l’autorisation «écrire» pour les disques fixes qui ne sont pas protégés par BitLocker</p></td>
<td align="left"><p>Configuration suggérée: <strong> non configuré</strong></p>
<p>Ce paramètre de stratégie détermine si la protection de BitLocker est requise pour les lecteurs fixes sur un ordinateur de sorte qu’ils soient accessibles en écriture. Ce paramètre de stratégie est appliqué lorsque vous activez BitLocker.</p>
<p>Lorsque la stratégie n’est pas configurée, tous les lecteurs fixes de l’ordinateur sont montés avec des autorisations en lecture/écriture.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Autoriser l’accès à des disques durs fixes protégés par BitLocker provenant de versions antérieures de Windows</p></td>
<td align="left"><p>Configuration suggérée: <strong> non configuré</strong></p>
<p>Activez cette stratégie pour déverrouiller et afficher les disques fixes mis en forme à l’aide du système de fichiers FAT (File Allocation Table) sur les ordinateurs exécutant Windows Server 2008, Windows Vista, Windows XP SP3 ou Windows XP SP2.</p>
<p>Ces systèmes d’exploitation disposent d’autorisations en lecture seule sur les lecteurs protégés par BitLocker.</p>
<p>Lorsque la stratégie est désactivée, les disques fixes mis en forme avec le système de fichiers FAT ne peuvent pas être déverrouillés et leur contenu ne peut pas être affiché sur les ordinateurs exécutant Windows Server 2008, Windows Vista, Windows XP SP3 ou Windows XP SP2.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Configurer l’utilisation du mot de passe pour les disques fixes</p></td>
<td align="left"><p>Configuration suggérée: <strong> non configuré</strong></p>
<p>Activez cette stratégie pour configurer la protection par mot de passe sur des disques fixes.</p>
<p>Lorsque la stratégie n’est pas configurée, les mots de passe sont pris en charge avec les paramètres par défaut, qui n’incluent pas les exigences de complexité des mots de passe et ne nécessitent que huit caractères.</p>
<p>Pour une sécurité accrue, activez cette stratégie et sélectionnez <strong> exiger un mot de passe pour le lecteur de données fixes </strong> , sélectionnez <strong> nécessite une complexité du mot de passe </strong> , puis définissez la <strong> longueur de mot de passe minimale souhaitée </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Choisir la manière dont les lecteurs fixes protégés par BitLocker peuvent être récupérés</p></td>
<td align="left"><p>Configuration suggérée: <strong> non configuré</strong></p>
<p>Configurez cette stratégie pour activer l’agent de récupération de données BitLocker ou enregistrer les informations de récupération BitLocker dans les services de domaine Active Directory (AD DS).</p>
<p>Lorsque cette stratégie n’est pas configurée, l’agent de récupération de données BitLocker est autorisé et les informations de récupération ne sont pas sauvegardées dans AD DS. MBAM n’exige pas que les informations de récupération soient sauvegardées dans AD DS.</p></td>
</tr>
</tbody>
</table>



## Définitions de la stratégie de lecteur du système d’exploitation


Cette section décrit les définitions de la stratégie de lecteur du système d’exploitation pour MBAM, qui se trouvent dans le nœud d’objet GPO suivant: **Configuration ordinateur** \\ **modèles d’administration** \\ **composants Windows** \\ **MDOP MBAM (gestion de BitLocker)**  \\  **Operating System Drive**.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nom de la stratégie</th>
<th align="left">Vue d’ensemble et paramètre de stratégie suggéré</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Paramètres de chiffrement de lecteur du système d’exploitation</p></td>
<td align="left"><p>Configuration suggérée: <strong> activée</strong></p>
<p>Ce paramètre de stratégie détermine si le lecteur du système d’exploitation sera crypté.</p>
<p>Configurez cette stratégie pour effectuer les opérations suivantes:</p>
<ul>
<li><p>Appliquez la protection BitLocker pour le lecteur du système d’exploitation.</p></li>
<li><p>Configurer l’utilisation du code confidentiel pour utiliser un code PIN de module de plateforme sécurisée (TPM) pour la protection du système d’exploitation.</p></li>
<li><p>Configurez les broches de démarrage améliorées pour autoriser les caractères tels que les lettres majuscules et minuscules et les nombres. MBAM ne prend pas en charge l’utilisation de symboles et d’espaces pour les broches améliorées, même si BitLocker prend en charge les symboles et les espaces.</p></li>
</ul>
<p>Si vous activez ce paramètre de stratégie, les utilisateurs sont obligés de sécuriser le lecteur du système d’exploitation à l’aide de BitLocker.</p>
<p>Si vous ne configurez pas ou si vous désactivez ce paramètre, les utilisateurs ne sont pas obligés de sécuriser le lecteur du système d’exploitation à l’aide de BitLocker.</p>
<p>Si vous désactivez cette stratégie, l’agent MBAM déchiffre le volume du système d’exploitation s’il est chiffré.</p>
<p>Lorsqu’il est activé, ce paramètre de stratégie demande aux utilisateurs de sécuriser le système d’exploitation à l’aide de la protection BitLocker et le lecteur est chiffré. En fonction de votre configuration requise pour le chiffrement, vous pouvez sélectionner la méthode de protection du lecteur du système d’exploitation.</p>
<p>Pour plus de sécurité, utilisez TPM + code confidentiel, autorisez les codes confidentiels et définissez une longueur minimale de huit caractères.</p>
<p>Lorsque cette stratégie est activée avec le protecteur de code confidentiel, vous pouvez envisager de désactiver les stratégies suivantes dans les paramètres de veille de la gestion de l' <strong> </strong>  /  <strong> alimentation système </strong>  /  <strong> </strong> :</p>
<ul>
<li><p>Autoriser les États de veille (S1-S3) lorsque vous êtes en veille (branché)</p></li>
<li><p>Autoriser les États de veille (S1-S3) en veille (sur batterie)</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Configurer le profil de validation de plateforme TPM</p></td>
<td align="left"><p>Configuration suggérée: <strong> non configuré</strong></p>
<p>Ce paramètre de stratégie vous permet de configurer la manière dont le matériel de sécurité du TPM sur un ordinateur sécurise la clé de chiffrement BitLocker. Ce paramètre de stratégie ne s’applique pas si l’ordinateur ne possède pas de TPM compatible ou s’il possède déjà une protection de module de plateforme sécurisée.</p>
<p>Lorsque cette stratégie n’est pas configurée, le TPM utilise le profil de validation de plateforme par défaut ou le profil de validation de plateforme spécifié par le script de configuration.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Choisir la méthode de récupération des lecteurs du système d’exploitation protégés par BitLocker</p></td>
<td align="left"><p>Configuration suggérée: <strong> non configuré</strong></p>
<p>Configurez cette stratégie pour activer l’agent de récupération de données BitLocker ou enregistrer les informations de récupération BitLocker dans les services de domaine Active Directory (AD DS).</p>
<p>Lorsque cette stratégie n’est pas configurée, l’agent de récupération de données est autorisé et les informations de récupération ne sont pas sauvegardées dans AD DS.</p>
<p>MBAM opération ne nécessite pas que les informations de récupération soient sauvegardées dans AD DS.</p></td>
</tr>
</tbody>
</table>



## Définitions de la stratégie de lecteur amovible


Cette section décrit les définitions de stratégie de lecteur amovible pour MBAM, qui se trouvent dans le nœud d’objet GPO suivant: **Configuration ordinateur** \\ **modèles d’administration** \\ **composants Windows** \\ **MDOP MBAM (gestion de BitLocker)**  \\  **Removable Drive**.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nom de la stratégie</th>
<th align="left">Vue d’ensemble et paramètre de stratégie suggéré</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Contrôler l’utilisation de BitLocker sur des lecteurs amovibles</p></td>
<td align="left"><p>Configuration suggérée: <strong> activée</strong></p>
<p>Cette stratégie contrôle l’utilisation de BitLocker sur les lecteurs de données amovibles.</p>
<p>Activez l' <strong> option autoriser les utilisateurs à appliquer la protection BitLocker sur les lecteurs de données amovibles </strong> pour permettre aux utilisateurs d’exécuter l’Assistant Configuration de BitLocker sur un lecteur de données amovible.</p>
<p>Activez l' <strong> option permettre aux utilisateurs de suspendre et de déchiffrer les disques BitLocker sur des lecteurs de données amovibles </strong> pour permettre aux utilisateurs de supprimer le chiffrement de lecteur BitLocker du lecteur ou de suspendre le chiffrement lors de la maintenance.</p>
<p>Lorsque cette stratégie est activée et que l' <strong> option autoriser les utilisateurs à appliquer la protection BitLocker sur les lecteurs de données amovibles </strong> est activée, le client MBAM enregistre les informations de récupération relatives aux lecteurs amovibles sur le serveur de récupération de clés MBAM, et permet aux utilisateurs de récupérer le lecteur en cas de perte du mot de passe.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Refuser les autorisations d’écriture sur des lecteurs amovibles qui ne sont pas protégés par BitLocker</p></td>
<td align="left"><p>Configuration suggérée: <strong> non configuré</strong></p>
<p>Activez cette stratégie pour autoriser les autorisations d’écriture seule sur les lecteurs protégés par BitLocker.</p>
<p>Lorsque cette stratégie est activée, tous les lecteurs de données amovibles de l’ordinateur doivent être chiffrés avant que les autorisations d’écriture soient autorisées.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Autoriser l’accès aux lecteurs amovibles protégés par BitLocker provenant de versions antérieures de Windows</p></td>
<td align="left"><p>Configuration suggérée: <strong> non configuré</strong></p>
<p>Activez cette stratégie pour déverrouiller et afficher les disques fixes qui sont mis en forme avec le système de fichiers (FAT) sur les ordinateurs exécutant Windows Server 2008, Windows Vista, Windows XP avec SP3 ou Windows XP SP2.</p>
<p>Ces systèmes d’exploitation disposent d’autorisations en lecture seule sur les lecteurs protégés par BitLocker.</p>
<p>Lorsque la stratégie est désactivée, les lecteurs amovibles mis en forme avec le système de fichiers FAT ne peuvent pas être déverrouillés et leur contenu ne peut pas être affiché sur les ordinateurs exécutant Windows Server 2008, Windows Vista, Windows XP SP3 ou Windows XP SP2.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Configurer l’utilisation du mot de passe pour les lecteurs de données amovibles</p></td>
<td align="left"><p>Configuration suggérée: <strong> non configuré</strong></p>
<p>Activez cette stratégie pour configurer la protection par mot de passe sur les lecteurs de données amovibles.</p>
<p>Lorsque cette stratégie n’est pas configurée, les mots de passe sont pris en charge avec les paramètres par défaut, qui n’incluent pas les exigences de complexité des mots de passe et ne nécessitent que huit caractères.</p>
<p>Pour une sécurité accrue, vous pouvez activer cette stratégie et sélectionner <strong> exiger un mot de passe pour le lecteur de données amovibles </strong> , sélectionner <strong> exiger une complexité du mot de passe </strong> , puis définir la <strong> longueur minimale du mot de passe </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Choisir la manière dont les lecteurs amovibles protégés par BitLocker peuvent être récupérés</p></td>
<td align="left"><p>Configuration suggérée: <strong> non configuré</strong></p>
<p>Vous pouvez configurer cette stratégie pour activer l’agent de récupération de données BitLocker ou enregistrer les informations de récupération BitLocker dans les services de domaine Active Directory (AD DS).</p>
<p>Lorsque la stratégie est définie sur <strong> non configuré </strong> , l’agent de récupération de données est autorisé et les informations de récupération ne sont pas sauvegardées dans AD DS.</p>
<p>MBAM opération ne nécessite pas que les informations de récupération soient sauvegardées dans AD DS.</p></td>
</tr>
</tbody>
</table>



## Rubriques connexes


[Préparation de votre environnement pour MBAM1.0](preparing-your-environment-for-mbam-10.md)









