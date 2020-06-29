---
title: Planification des exigences en matière de stratégie de groupe MBAM2.0
description: Planification des exigences en matière de stratégie de groupe MBAM2.0
author: dansimp
ms.assetid: f5e19dcb-eb15-4722-bb71-0734b3799eb8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f6092507996fe6f0234178c8b1abae5cea7bf836
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804519"
---
# Planification des exigences en matière de stratégie de groupe MBAM2.0


Pour gérer les ordinateurs client d’administration et de surveillance de Microsoft BitLocker (MBAM), vous devez prendre en compte les types de protecteurs BitLocker que vous voulez prendre en charge au sein de votre organisation, puis configurer les paramètres de stratégie de groupe correspondants que vous voulez appliquer. Cette rubrique décrit les paramètres de stratégie de groupe qui sont disponibles pour une utilisation lors de l’utilisation de l’administration et de la surveillance de BitLocker pour la gestion du chiffrement de lecteur BitLocker au sein de l’entreprise.

MBAM prend en charge les types suivants de protecteurs BitLocker pour les lecteurs de systèmes d’exploitation: module de plateforme sécurisée (TPM), TPM + code confidentiel, TPM + USB, mot de passe, mot de passe numérique et agent de récupération de données. Le protecteur de mot de passe est uniquement pris en charge pour les appareils Windows to Go et pour les appareils Windows 8 qui n’ont pas de TPM. MBAM prend en charge la clé USB et le module de plateforme sécurisée (TPM) et les protecteurs de clés USB et TPM + PIN + USB uniquement lorsque le volume du système d’exploitation est crypté avant l’installation d’MBAM.

MBAM prend en charge les types de protections BitLocker suivants pour les lecteurs de données fixes: mot de passe, déverrouillage automatique, mot de passe numérique et agent de récupération de données.

Le protecteur de mot de passe numérique est appliqué automatiquement dans le cadre du chiffrement de volume et n’a pas besoin d’être configuré.

**Important**  
Les paramètres par défaut de l’objet de stratégie de groupe de lecteurs BitLocker Windows (GPO) ne sont pas utilisés par MBAM et peuvent entraîner un comportement en conflit s’ils sont activés. Pour permettre à MBAM de gérer BitLocker, vous devez définir les paramètres de stratégie de groupe MBAM uniquement après l’installation du modèle de stratégie de groupe MBAM.



Les codes confidentiels de démarrage étendus peuvent contenir des caractères, tels que les majuscules et les minuscules, ainsi que des chiffres. À la différence de BitLocker, MBAM ne prend pas en charge l’utilisation de symboles et d’espaces pour les broches améliorées.

Installez le modèle de stratégie de groupe MBAM sur un ordinateur capable d’exécuter la console de gestion des stratégies de groupe (GPMC) ou la technologie de gestion des stratégies de groupe avancée (AGPM). Pour modifier les paramètres de l’objet de stratégie de groupe qui activent la fonctionnalité MBAM, vous devez d’abord installer le modèle de stratégie de groupe MBAM, ouvrir le GPMC ou AGPM pour modifier l’objet de stratégie de groupe applicable, puis accéder au nœud d’objet de stratégie de groupe suivant: stratégies de configuration de l' **ordinateur**: \\ **Policies** \\ **modèles d’administration** \\ **composants Windows** \\ **MDOP MBAM (gestion de BitLocker).**

Le nœud de l’objet de stratégie de groupe MDOP MBAM (gestion du BitLocker) contient quatre paramètres de stratégie globale et quatre nœuds de paramètres d’objets de stratégie de groupe enfants: gestion du client, lecteur fixe, lecteur du système d’exploitation et lecteur amovible. Les sections suivantes fournissent des définitions de stratégie et des paramètres de stratégie suggérés pour vous aider à planifier la configuration requise pour les stratégies d’objets de stratégie de MBAM.

**Remarque**  
Pour plus d’informations sur la configuration des paramètres d’objets de stratégie de groupe minimum recommandés pour permettre à MBAM de gérer le chiffrement BitLocker, voir [Comment modifier les paramètres de l’objet de stratégie de groupe MBAM 2,0](how-to-edit-mbam-20-gpo-settings-mbam-2.md).



## Définitions de stratégies globales


Cette section décrit les définitions de stratégies globales de MBAM trouvées au nœud d’objet de stratégie de groupe suivant: stratégies de **Configuration ordinateur** \\ **Policies** \\ **modèles d’administration** \\ **composants Windows** \\ **MDOP MBAM (gestion de BitLocker)**.

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


Cette section décrit les définitions de la stratégie de gestion des clients pour l’administration et la surveillance de BitLocker disponibles sur le nœud d’objet GPO suivant: stratégies de **Configuration ordinateur** \\ **Policies** \\ **modèles d’administration** \\ **composants Windows** \\ **MBAM (gestion de BitLocker)** \\ **gestion du client**.

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
<li><p><strong>Point de terminaison du service matériel et de récupération MBAM </strong> . Utilisez ce paramètre pour activer la gestion du chiffrement BitLocker du client MBAM. Entrez un emplacement de point de terminaison similaire à l’exemple suivant: <strong> http:// </strong><em> &lt; MBAM administration du serveur et surveiller &gt; </em><strong> son nom: </strong><em> &lt; port le service Web est lié à &gt; </em><strong> /MBAMRecoveryAndHardwareService/CoreService.svc </strong> .</p></li>
<li><p><strong>Sélectionnez les informations de récupération BitLocker à stocker </strong> . Ce paramètre de stratégie vous permet de configurer le service de récupération de clés pour sauvegarder les informations de récupération de BitLocker. Il vous permet également de configurer le service de rapport d’État pour la collecte des rapports de conformité et d’audit. La stratégie fournit une méthode d’administration de récupération des données chiffrées par BitLocker pour éviter la perte de données en raison de l’absence d’informations clés. Le rapport d’État et l’activité de récupération de clés seront automatiquement et en silence vers l’emplacement du serveur du rapport configuré.</p>
<p>Si vous ne configurez pas ou si vous désactivez ce paramètre de stratégie, les informations de récupération de clé ne seront pas enregistrées, et le rapport d’État et les activités de récupération de clés ne seront pas signalés au serveur. Lorsque ce paramètre est défini sur <strong> mot de passe de récupération et sur le package de clé </strong> , le mot de passe de récupération et le package de clé seront automatiquement sauvegardés sur l’emplacement du serveur de récupération de clé configuré.</p></li>
<li><p><strong>Entrez la fréquence de vérification de l’état du client en minutes </strong> . Ce paramètre de stratégie gère la fréquence à laquelle le client vérifie les stratégies de protection BitLocker et l’état de l’ordinateur client. Ce paramètre gère également la fréquence d’enregistrement de l’état de conformité du client sur le serveur. Le client vérifie les stratégies de protection BitLocker et l’État sur l’ordinateur client et sauvegarde également la clé de récupération du client à la fréquence configurée.</p>
<p>Définissez cette fréquence en fonction de la configuration requise définie par votre société sur la fréquence de vérification de l’état de conformité de l’ordinateur et la fréquence de sauvegarde de la clé de récupération du client.</p></li>
<li><p><strong>Point de terminaison du service de rapport d’État MBAM </strong> . Vous devez configurer ce paramètre pour activer la gestion du chiffrement BitLocker du client MBAM. Entrez un emplacement de point de terminaison similaire à l’exemple suivant: <strong> http:// </strong><em> &lt; MBAM administration du serveur et surveiller &gt; </em><strong> son nom: </strong><em> &lt; port le service Web est lié à &gt; </em><strong> /MBAMComplianceStatusService/StatusReportingService.svc </strong> .</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Configurer une stratégie d’exemption des utilisateurs</p></td>
<td align="left"><p>Configuration suggérée: <strong> non configuré</strong></p>
<p>Ce paramètre de stratégie vous permet de configurer une adresse de site Web, une adresse de messagerie ou un numéro de téléphone qui demande à l’utilisateur d’être exempté du chiffrement BitLocker.</p>
<p>Si vous activez ce paramètre de stratégie et indiquez une adresse de site Web, une adresse de messagerie ou un numéro de téléphone, les utilisateurs voient s’afficher une boîte de dialogue vous proposant des instructions sur la façon d’appliquer une exemption de protection BitLocker. Pour plus d’informations sur l’activation des exemptions de chiffrement BitLocker pour les utilisateurs, voir <a href="how-to-manage-user-bitlocker-encryption-exemptions-mbam-2.md" data-raw-source="[How to Manage User BitLocker Encryption Exemptions](how-to-manage-user-bitlocker-encryption-exemptions-mbam-2.md)"> Comment gérer les exemptions de chiffrement BitLocker utilisateur </a> .</p>
<p>Si vous désactivez ou ne configurez pas ce paramètre de stratégie, les instructions de demande d’exemption ne seront pas présentées aux utilisateurs.</p>
<div class="alert">
<strong>Remarque</strong><br/><p>L’exemption des utilisateurs est gérée par utilisateur et non par ordinateur. Si plusieurs utilisateurs se connectent sur le même ordinateur et qu’un utilisateur n’est pas exempté, l’ordinateur est crypté.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>Configurer le programme d’amélioration du produit</p></td>
<td align="left"><p>Ce paramètre de stratégie vous permet de configurer la manière dont les utilisateurs de MBAM peuvent participer au programme d’amélioration du produit. Ce programme collecte des informations sur le matériel informatique et la façon dont les utilisateurs utilisent MBAM sans interrompre leur fonctionnement. Les informations permettent à Microsoft d’identifier les fonctionnalités MBAM à améliorer. Microsoft n’utilise pas ces informations pour identifier ou contacter les utilisateurs de MBAM.</p>
<p>Si vous activez ce paramètre de stratégie, les utilisateurs peuvent participer au programme d’amélioration du produit.</p>
<p>Si vous désactivez ce paramètre de stratégie, les utilisateurs ne peuvent pas rejoindre le programme d’amélioration du produit.</p>
<p>Si vous ne configurez pas ce paramètre de stratégie, les utilisateurs ont la possibilité de participer au programme d’amélioration du produit.</p></td>
</tr>
</tbody>
</table>



## Définitions de stratégies de disque fixes


Cette section décrit les définitions de stratégie de disque corrigées pour l’administration et le contrôle Microsoft BitLocker disponibles sur le nœud d’objet de stratégie de groupe suivant: stratégies de configuration de l' **ordinateur**: \\ **Policies** \\ **modèles d’administration** \\ **composants Windows** \\ **MBAM (gestion de BitLocker)** \\ **lecteur fixe**.

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
<td align="left"><p>Configuration suggérée: <strong> activée</strong></p>
<p>Ce paramètre de stratégie vous permet de gérer si les lecteurs fixes doivent être chiffrés.</p>
<p>Si le volume du système d’exploitation doit être chiffré, sélectionnez l' <strong> option Activer le lecteur de données à verrouillage automatique </strong> .</p>
<p>Lorsque vous activez cette stratégie, vous ne devez pas désactiver le <strong> paramètre configurer l’utilisation du mot de passe pour les lecteurs de données fixes </strong> , sauf si l’utilisation de la fonction de déverrouillage automatique pour les lecteurs de données fixes est autorisée ou obligatoire.</p>
<p>Si vous avez besoin d’utiliser le déverrouillage automatique pour les lecteurs de données fixes, vous devez configurer le chiffrement des volumes du système d’exploitation.</p>
<p>Si vous activez ce paramètre de stratégie, les utilisateurs doivent placer tous les disques fixes sous protection BitLocker et les lecteurs seront chiffrés.</p>
<p>Si vous ne configurez pas ce paramètre de stratégie, les utilisateurs ne sont pas obligés de placer des lecteurs fixes sous la protection de BitLocker. Si vous appliquez cette stratégie après le chiffrement de périphériques de données fixes, l’agent MBAM déchiffre les lecteurs fixes chiffrés.</p>
<p>Si vous désactivez ce paramètre de stratégie, les utilisateurs ne seront pas en mesure de placer leurs lecteurs de données fixes sous protection de BitLocker.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Refuser l’accès en écriture aux lecteurs fixes non protégés par BitLocker</p></td>
<td align="left"><p>Configuration suggérée: <strong> non configuré</strong></p>
<p>Ce paramètre de stratégie détermine s’il est nécessaire de procéder à la protection de BitLocker pour pouvoir écrire des lecteurs fixes sur un ordinateur. Ce paramètre de stratégie est appliqué lorsque vous activez BitLocker.</p>
<p>Lorsque la stratégie n’est pas configurée, tous les lecteurs de données fixes de l’ordinateur sont montés avec un accès en lecture/écriture.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Autoriser l’accès à des disques durs fixes protégés par BitLocker provenant de versions antérieures de Windows</p></td>
<td align="left"><p>Configuration suggérée: <strong> non configuré</strong></p>
<p>Activez cette stratégie pour permettre aux lecteurs fixes dotés du système de fichiers FAT d’être déverrouillés et affichés sur les ordinateurs exécutant Windows Server 2008, Windows Vista, Windows XP avec SP3 ou Windows XP SP2.</p>
<p>Lorsque la stratégie est activée ou n’est pas configurée, les disques fixes mis en forme avec le système de fichiers FAT peuvent être déverrouillés et leur contenu peut être affiché sur les ordinateurs exécutant Windows Server 2008, Windows Vista, Windows XP SP3 ou Windows XP SP2. Ces systèmes d’exploitation disposent d’un accès en lecture seule aux lecteurs protégés par BitLocker.</p>
<p>Lorsque la stratégie est désactivée, les disques fixes mis en forme avec le système de fichiers FAT ne peuvent pas être déverrouillés et leur contenu ne peut pas être affiché sur les ordinateurs exécutant Windows Server 2008, Windows Vista, Windows XP SP3 ou Windows XP SP2.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Configurer l’utilisation du mot de passe pour les disques fixes</p></td>
<td align="left"><p>Configuration suggérée: <strong> non configuré</strong></p>
<p>Utilisez cette stratégie pour spécifier si un mot de passe est requis pour déverrouiller des lecteurs de données fixes protégés par BitLocker.</p>
<p>Si vous activez ce paramètre de stratégie, les utilisateurs peuvent configurer un mot de passe qui répond aux conditions que vous définissez. BitLocker permettra aux utilisateurs de déverrouiller un lecteur avec tout protecteur disponible sur le lecteur.</p>
<p>Ces paramètres sont appliqués lors de l’activation de BitLocker sans avoir à déverrouiller un volume.</p>
<p>Si vous désactivez ce paramètre de stratégie, les utilisateurs ne peuvent pas utiliser de mot de passe.</p>
<p>Lorsque la stratégie n’est pas configurée, les mots de passe sont pris en charge avec les paramètres par défaut, qui n’incluent pas les exigences de complexité des mots de passe et ne nécessitent que huit caractères.</p>
<p>Pour une sécurité accrue, activez cette stratégie et sélectionnez <strong> exiger un mot de passe pour le lecteur de données fixes </strong> , sélectionnez <strong> nécessite une complexité du mot de passe </strong> , puis définissez la <strong> longueur de mot de passe minimale souhaitée </strong> .</p>
<p>Si vous désactivez ce paramètre de stratégie, les utilisateurs ne peuvent pas utiliser de mot de passe.</p>
<p>Si vous ne configurez pas ce paramètre de stratégie, les mots de passe seront pris en charge avec les paramètres par défaut, qui n’incluent pas les exigences de complexité des mots de passe et ne nécessitent que huit caractères.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Choisir la manière dont les lecteurs fixes protégés par BitLocker peuvent être récupérés</p></td>
<td align="left"><p>Configuration suggérée: <strong> non configuré</strong></p>
<p>Configurez cette stratégie pour activer l’agent de récupération de données BitLocker ou enregistrer les informations de récupération BitLocker dans les services de domaine Active Directory (AD DS).</p>
<p>Lorsque la stratégie n’est pas configurée, l’agent de récupération de données BitLocker est autorisé et les informations de récupération ne sont pas sauvegardées dans AD DS. MBAM ne nécessite pas de sauvegarde des informations de récupération dans AD DS.</p></td>
</tr>
</tbody>
</table>



## Définitions de la stratégie de lecteur du système d’exploitation


Cette section décrit les définitions de la stratégie de lecteur du système d’exploitation pour l’administration et la surveillance de BitLocker disponibles sur le nœud d’objet de stratégie de groupe suivant: stratégies de **Configuration ordinateur** \\ **Policies** \\ **modèles d’administration** \\ **composants Windows** \\ **MBAM (gestion de BitLocker)** \\ **Operating System Drive**.

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
<p>Ce paramètre de stratégie vous permet de déterminer si le lecteur du système d’exploitation doit être chiffré.</p>
<p>Pour plus de sécurité, envisagez de désactiver les paramètres de stratégie suivants dans les <strong> paramètres système/gestion de l’alimentation/mise en veille </strong> lorsque vous les activez avec le protecteur de plateforme sécurisée.</p>
<ul>
<li><p>Autoriser les États de veille (S1-S3) lorsque vous êtes en veille (branché)</p></li>
<li><p>Autoriser les États de veille (S1-S3) en veille (sur batterie)</p></li>
</ul>
<p>Si vous exécutez Microsoft Windows 8 ou une version ultérieure et que vous souhaitez utiliser BitLocker sur un ordinateur dépourvu de TPM, activez la case <strong> </strong> à cocher Autoriser BitLocker sans module de plateforme sécurisée compatible. Dans ce mode, un mot de passe est requis au démarrage. Si vous oubliez le mot de passe, vous devez utiliser l’une des options de récupération de BitLocker pour accéder au lecteur.</p>
<p>Sur un ordinateur équipé d’un TPM compatible, deux types de méthodes d’authentification peuvent être utilisés au démarrage pour renforcer la protection des données chiffrées. Lorsque l’ordinateur démarre, il peut uniquement utiliser le TPM pour l’authentification, ou exiger l’entrée d’un code confidentiel (PIN).</p>
<p>Si vous activez ce paramètre de stratégie, les utilisateurs doivent placer le lecteur du système d’exploitation sous protection BitLocker et le lecteur sera crypté.</p>
<p>Si vous désactivez ce paramètre, les utilisateurs ne seront pas en mesure de placer le lecteur du système d’exploitation sous protection BitLocker. Si vous appliquez cette stratégie après le chiffrement du lecteur du système d’exploitation, le lecteur sera déchiffré.</p>
<p>Si vous ne configurez pas cette stratégie, le lecteur du système d’exploitation ne doit pas nécessairement être placé sous protection BitLocker.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Configurer le profil de validation de plateforme TPM</p></td>
<td align="left"><p>Configuration suggérée: <strong> non configuré</strong></p>
<p>Ce paramètre de stratégie vous permet de configurer la manière dont le matériel de sécurité du TPM sur un ordinateur sécurise la clé de chiffrement BitLocker. Ce paramètre de stratégie ne s’applique pas si l’ordinateur ne possède pas de TPM compatible ou si BitLocker a déjà été activé avec la protection de la plateforme.</p>
<p>Lorsque ce paramètre de stratégie n’est pas configuré, le TPM utilise le profil de validation de plateforme par défaut ou le profil de validation de plateforme spécifié par le script de configuration.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Choisir la manière dont les lecteurs du système d’exploitation protégés par BitLocker peuvent être récupérés</p></td>
<td align="left"><p>Configuration suggérée: <strong> non configuré</strong></p>
<p>Configurez cette stratégie pour activer l’agent de récupération de données BitLocker ou enregistrer les informations de récupération BitLocker dans les services de domaine Active Directory (AD DS).</p>
<p>Lorsque cette stratégie n’est pas configurée, l’agent de récupération de données est autorisé et les informations de récupération ne sont pas sauvegardées dans AD DS.</p>
<p>Dans le cas d’une opération MBAM, les informations de récupération ne doivent pas être sauvegardées dans AD DS.</p></td>
</tr>
</tbody>
</table>



## Définitions de la stratégie de lecteur amovible


Cette section décrit les définitions de stratégie de lecteur amovible pour l’administration et la surveillance de BitLocker disponibles sur le nœud d’objet GPO suivant: stratégies de **Configuration ordinateur** \\ **Policies** \\ **modèles d’administration** \\ **composants Windows** \\ **MBAM (gestion de BitLocker)**-  \\  **lecteur amovible**.

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
<p>Lorsque cette stratégie est activée et que l' <strong> option autoriser les utilisateurs à appliquer la protection BitLocker sur les lecteurs de données amovibles </strong> est activée, le client MBAM enregistre les informations de récupération relatives aux lecteurs amovibles sur le serveur de récupération de clés MBAM et permet aux utilisateurs de récupérer le lecteur en cas de perte du mot de passe.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Refuser l'accès en écriture aux lecteurs amovibles non protégés par BitLocker</p></td>
<td align="left"><p>Configuration suggérée: <strong> non configuré</strong></p>
<p>Activez cette stratégie pour autoriser l’accès en écriture uniquement aux lecteurs protégés par BitLocker.</p>
<p>Lorsque cette stratégie est activée, tous les lecteurs de données amovibles de l’ordinateur doivent être chiffrés avant l’autorisation d’accès en écriture.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Autoriser l’accès aux lecteurs amovibles protégés par BitLocker provenant de versions antérieures de Windows</p></td>
<td align="left"><p>Configuration suggérée: <strong> non configuré</strong></p>
<p>Activez cette stratégie pour autoriser le déverrouillage et l’affichage de disques fixes avec le système de fichiers FAT sur les ordinateurs exécutant Windows Server 2008, Windows Vista, Windows XP avec SP3 ou Windows XP SP2.</p>
<p>Lorsque cette stratégie n’est pas configurée, les lecteurs de données amovibles mis en forme avec le système de fichiers FAT peuvent être déverrouillés sur les ordinateurs exécutant Windows Server 2008, Windows Vista, Windows XP avec SP3 ou Windows XP SP2, et leur contenu peut être affiché. Ces systèmes d’exploitation disposent d’un accès en lecture seule aux lecteurs protégés par BitLocker.</p>
<p>Lorsque la stratégie est désactivée, les lecteurs amovibles mis en forme avec le système de fichiers FAT ne peuvent pas être déverrouillés et leur contenu ne peut pas être affiché sur les ordinateurs exécutant Windows Server 2008, Windows Vista, Windows XP SP3 ou Windows XP SP2.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Configurer l’utilisation du mot de passe pour les lecteurs de données amovibles</p></td>
<td align="left"><p>Configuration suggérée: <strong> non configuré</strong></p>
<p>Activez cette stratégie pour configurer la protection par mot de passe sur les lecteurs de données amovibles.</p>
<p>Lorsque cette stratégie n’est pas configurée, les mots de passe sont pris en charge avec les paramètres par défaut, qui n’incluent pas les exigences de complexité des mots de passe et ne nécessitent que huit caractères.</p>
<p>Pour une sécurité accrue, vous pouvez activer cette stratégie et activer la case à cocher <strong> exiger un mot de passe pour le lecteur de données amovible </strong> , sélectionner <strong> exiger la complexité du mot de passe </strong> et définir la <strong> longueur minimale du mot de passe </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Choisir la manière dont les lecteurs amovibles protégés par BitLocker peuvent être récupérés</p></td>
<td align="left"><p>Configuration suggérée: <strong> non configuré</strong></p>
<p>Configurez cette stratégie pour activer l’agent de récupération de données BitLocker ou enregistrer les informations de récupération BitLocker dans les services de domaine Active Directory (AD DS).</p>
<p>Lorsque la valeur est définie sur <strong> non configuré </strong> , l’agent de récupération de données est autorisé et les informations de récupération ne sont pas sauvegardées dans AD DS.</p>
<p>Dans le cas d’une opération MBAM, les informations de récupération ne doivent pas être sauvegardées dans AD DS.</p></td>
</tr>
</tbody>
</table>



## Rubriques connexes


[Conditions préalables au déploiement de MBAM2.0](mbam-20-deployment-prerequisites-mbam-2.md)









