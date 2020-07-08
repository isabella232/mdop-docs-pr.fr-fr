---
title: Planification des exigences en matière de stratégie de groupe MBAM2.5
description: Planification des exigences en matière de stratégie de groupe MBAM2.5
author: dansimp
ms.assetid: 82d545dc-3fbf-4b46-b62f-47fe178a7c44
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 4beeb9f88f16e7d48d145861c398a90fa29f3491
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810152"
---
# Planification des exigences en matière de stratégie de groupe MBAM2.5


Utilisez les informations suivantes pour déterminer les types de protecteurs BitLocker que vous pouvez utiliser pour gérer les ordinateurs client d’administration et de surveillance Microsoft BitLocker (MBAM) de votre entreprise.

## Types de protecteurs BitLocker pris en charge par MBAM


MBAM prend en charge les types de protecteurs BitLocker suivants.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Type de lecteur ou volume</th>
<th align="left">Protecteurs BitLocker pris en charge</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Volumes du système d’exploitation</p></td>
<td align="left"><ul>
<li><p><strong>Module de plateforme sécurisée</strong></p></li>
<li><p><strong>TPM + CODE CONFIDENTIEL</strong></p></li>
<li><p><strong>TPM + clé USB </strong> : prise en charge uniquement lorsque le volume du système d’exploitation est chiffré avant l’installation de MBAM</p></li>
<li><p><strong>TPM + punaise + clé USB </strong> - prise en charge uniquement lorsque le volume du système d’exploitation est chiffré avant l’installation d’MBAM</p></li>
<li><p><strong>Mot de passe </strong> - uniquement pris en charge pour les appareils Windows to Go, les lecteurs de données fixes et les appareils Windows 8, Windows 8,1 et Windows 10 qui n’ont pas de TPM</p></li>
<li><p><strong>Mot de passe numérique </strong> - appliqué automatiquement dans le cadre du chiffrement de volume et n’a pas besoin d’être configuré à l’exception du mode FIPS sur Windows 7</p></li>
<li><p><strong>Agent de récupération de données (DRA)</strong></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Lecteurs de données fixes</p></td>
<td align="left"><ul>
<li><p><strong>Mot de passe</strong></p></li>
<li><p><strong>Déverrouillage automatique</strong></p></li>
<li><p><strong>Mot de passe numérique </strong> - appliqué automatiquement dans le cadre du chiffrement de volume et n’a pas besoin d’être configuré à l’exception du mode FIPS sur Windows 7</p></li>
<li><p><strong>Agent de récupération de données (DRA)</strong></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Lecteurs amovibles</p></td>
<td align="left"><ul>
<li><p><strong>Mot de passe</strong></p></li>
<li><p><strong>Déverrouillage automatique</strong></p></li>
<li><p><strong>Mot de passe numérique </strong> - appliqué automatiquement dans le cadre du chiffrement de volume et inutile d’être configuré</p></li>
<li><p><strong>Agent de récupération de données (DRA)</strong></p></li>
</ul></td>
</tr>
</tbody>
</table>



### Prise en charge de la stratégie BitLocker de chiffrement d’espace utilisé

Dans MBAM 2,5 SP1, si vous activez le chiffrement d’espace utilisé via la stratégie de groupe BitLocker, le client MBAM le respecte.

Ce paramètre de stratégie de groupe est appelé **appliquer le type de chiffrement de lecteur sur les lecteurs du système d’exploitation** et il se trouve dans le nœud d’objet GPO suivant: **Configuration ordinateur** &gt; **modèles d’administration** &gt; **composants Windows** &gt; lecteurs du système d’exploitation **BitLocker Drive Encryption** &gt; **Operating System Drives**. Si vous activez cette stratégie et sélectionnez le type de chiffrement en tant qu' **espace utilisé uniquement pour le chiffrement**, MBAM honorera la stratégie et BitLocker cryptera uniquement l’espace disque utilisé sur le volume.

## Comment obtenir les modèles de stratégie de groupe MBAM et modifier les paramètres


Lorsque vous êtes prêt à configurer les paramètres de stratégie de groupe de MBAM que vous voulez, procédez comme suit:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Étapes à suivre</th>
<th align="left">Où obtenir des instructions</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Copiez les modèles de stratégie de groupe MBAM à partir de la <a href="https://go.microsoft.com/fwlink/p/?LinkId=393941" data-raw-source="[How to Get MDOP Group Policy (.admx) Templates](https://go.microsoft.com/fwlink/p/?LinkId=393941)"> section obtention de modèles de stratégie de groupe MDOP (. admx) </a> et installation sur un ordinateur capable d’exécuter la console de gestion des stratégies de groupe (GPMC) ou Advanced Group Policy Management (AGPM).</p></td>
<td align="left"><p><a href="copying-the-mbam-25-group-policy-templates.md" data-raw-source="[Copying the MBAM 2.5 Group Policy Templates](copying-the-mbam-25-group-policy-templates.md)">Copie des modèles de stratégie de groupe MBAM2.5</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Configurez les paramètres de stratégie de groupe que vous souhaitez utiliser au sein de votre entreprise.</p></td>
<td align="left"><p><a href="editing-the-mbam-25-group-policy-settings.md" data-raw-source="[Editing the MBAM 2.5 Group Policy Settings](editing-the-mbam-25-group-policy-settings.md)">Modification des paramètres de stratégie de groupe MBAM2.5</a></p></td>
</tr>
</tbody>
</table>



## Descriptions des paramètres de stratégie de groupe MBAM


Le nœud de l’objet de stratégie de groupe **MDOP MBAM (gestion du BitLocker)** contient quatre paramètres de stratégie globale et quatre nœuds d’objets de stratégie de groupe enfants: **gestion du client**, **lecteur fixe**, **lecteur du système d’exploitation**et **lecteur amovible**. Les sections suivantes décrivent et suggèrent des paramètres pour les paramètres de stratégie de groupe MBAM.

**Important**  
Ne modifiez pas les paramètres de stratégie de groupe du nœud **BitLocker Drive Encryption** , ou MBAM ne fonctionne pas correctement. MBAM configure automatiquement les paramètres de ce nœud pour vous lorsque vous configurez les paramètres du nœud **MDOP MBAM (gestion de BitLocker)** .



### Définitions de stratégie de groupe globales

Cette section décrit les définitions de stratégie de groupe globales de MBAM au nœud d’objet de stratégie de groupe suivant: stratégies de **Configuration ordinateur** &gt; **Policies** &gt; **modèles d’administration** &gt; **composants Windows** &gt; **MDOP MBAM (gestion de BitLocker)**.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nom de la stratégie</th>
<th align="left">Vue d’ensemble et paramètres de stratégie de groupe suggérés</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Choisir la méthode de chiffrement de lecteur et la puissance de chiffrement</p></td>
<td align="left"><p>Configuration suggérée: <strong> activée</strong></p>
<p>Configurez cette stratégie pour utiliser une méthode de chiffrement et une force de chiffrement spécifiques.</p>
<p>Lorsque cette stratégie n’est pas configurée, BitLocker utilise la méthode de chiffrement par défaut: AES 128-bit avec diffuseur.</p>
<div class="alert">
<strong>Remarque</strong><br/><p>Un problème avec le rapport de conformité de l’ordinateur BitLocker entraîne &quot; l’affichage du &quot; paramètre inconnu pour le chiffrement, même si vous utilisez la valeur par défaut. Pour contourner ce problème, assurez-vous d’activer ce paramètre et de définir une valeur pour le niveau de cryptage.</p>
</div>
<div>

</div>
<ul>
<li><p>AES 128-bit avec diffuseur-pour Windows 7 uniquement</p></li>
<li><p>AES 128 pour Windows 8, Windows 8,1 et Windows 10</p></li>
</ul></td>
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
<p>Lorsque cette stratégie n’est pas configurée, l’identificateur d’objet par défaut 1.3.6.1.4.1.311.67.1.1 est utilisé pour spécifier un certificat.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Fournir les identificateurs uniques pour votre organisation</p></td>
<td align="left"><p>Configuration suggérée: <strong> non configuré</strong></p>
<p>Configurez cette stratégie pour utiliser un agent de récupération des données basé sur un certificat ou le lecteur BitLocker to go.</p>
<p>Lorsque cette stratégie n’est pas configurée, le <strong> champ d’identification </strong> n’est pas utilisé.</p>
<p>Si votre entreprise utilise des mesures de sécurité plus importantes, vous pouvez configurer le <strong> </strong> champ d’identification pour vous assurer que tous les périphériques USB disposent de ce jeu de champs et qu’ils sont alignés avec ce paramètre de stratégie de groupe.</p></td>
</tr>
</tbody>
</table>



### Définitions de la stratégie de groupe gestion des clients

Cette section décrit les définitions de la stratégie de gestion des clients pour MBAM au nœud d’objet GPO suivant: stratégies de **Configuration ordinateur** &gt; **Policies** &gt; **modèles d’administration** &gt; **composants Windows** &gt; **MDOP MBAM (gestion de BitLocker)** &gt; **gestion du client**.

Vous pouvez définir les mêmes paramètres de stratégie de groupe pour les topologies d’intégration autonomes et System Center Configuration Manager, à l’exception: désactivez le paramètre **configurer les services de point de terminaison du service de rapport d' &gt; État MBAM de MBAM** .

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nom de la stratégie</th>
<th align="left">Vue d’ensemble et paramètres de stratégie de groupe suggérés</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Configurer les services de MBAM</p></td>
<td align="left"><p>Configuration suggérée: <strong> activée</strong></p>
<ul>
<li><p><strong>Point de terminaison du service matériel et de récupération MBAM </strong> . Utilisez ce paramètre pour activer la gestion du chiffrement BitLocker du client MBAM. Entrez un emplacement de point de terminaison similaire à l’exemple suivant: <strong> http (s):// </strong><em> &lt; MBAM administration et vérification &gt; </em><strong> du nom du serveur: </strong><em> &lt; le port que le service Web est lié à &gt; </em><strong> /MBAMRecoveryAndHardwareService/CoreService.svc </strong> .</p></li>
<li><p><strong>Sélectionnez les informations de récupération BitLocker à stocker </strong> . Ce paramètre de stratégie vous permet de configurer le service de récupération de clés pour sauvegarder les informations de récupération de BitLocker. Il vous permet également de configurer un service de rapport d’État pour la collecte de rapports. La stratégie fournit une méthode d’administration de récupération des données chiffrées par BitLocker pour éviter la perte de données en raison de l’absence d’informations clés. Le rapport d’État et l’activité de récupération de clés sont automatiquement et silencieusement envoyés à l’emplacement du serveur de rapports configuré.</p>
<p>Si vous ne configurez pas ce paramètre de stratégie ou si vous le désactivez, les informations de récupération de clés ne sont pas enregistrées, et le rapport d’État et l’activité de récupération de clés ne sont pas signalés au serveur. Lorsque ce paramètre est défini sur <strong> mot de passe de récupération et sur le package de clé </strong> , le mot de passe de récupération et le package de clé sont automatiquement sauvegardés sur l’emplacement du serveur de récupération de clés configuré.</p></li>
<li><p><strong>Entrez la fréquence de vérification de l’état du client en minutes </strong> . Ce paramètre de stratégie gère la fréquence à laquelle le client vérifie les stratégies de protection BitLocker et l’état de l’ordinateur client. Ce paramètre gère également la fréquence d’enregistrement de l’état de conformité du client sur le serveur. Le client vérifie les stratégies de protection BitLocker et l’État sur l’ordinateur client et sauvegarde également la clé de récupération du client à la fréquence configurée.</p>
<p>Définissez cette fréquence en fonction de la configuration requise définie par votre société sur la fréquence de vérification de l’état de conformité de l’ordinateur et la fréquence de sauvegarde de la clé de récupération du client.</p></li>
<li><p><strong>Point de terminaison du service de rapport d’État MBAM:</strong></p>
<p><strong>Pour MBAM dans une topologie autonome </strong> : vous devez configurer ce paramètre pour activer la gestion du chiffrement de BitLocker client MBAM.</p>
<p>Entrez un emplacement de point de terminaison similaire à l’exemple suivant:</p>
<p><strong>http (s):// </strong><em> &lt; MBAM administration et surveillance du nom du serveur &gt; </em><strong> : </strong><em> &lt; le port associé au service Web &gt; </em><strong> /MBAMComplianceStatusService/StatusReportingService.svc</strong></p>
<p><strong>Pour MBAM dans la topologie d’intégration de Configuration Manager </strong> : désactivez ce paramètre.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Configurer une stratégie d’exemption des utilisateurs</p></td>
<td align="left"><p>Configuration suggérée: <strong> non configuré</strong></p>
<p>Ce paramètre de stratégie vous permet de configurer une adresse de site Web, une adresse de messagerie ou un numéro de téléphone demandant à un utilisateur de demander une exemption du chiffrement BitLocker.</p>
<p>Si vous activez ce paramètre de stratégie et indiquez une adresse de site Web, une adresse de messagerie ou un numéro de téléphone, les utilisateurs voient s’afficher une boîte de dialogue contenant des instructions sur la façon d’appliquer une exemption de protection BitLocker. Pour plus d’informations sur l’activation des exemptions de chiffrement BitLocker pour les utilisateurs, voir <a href="how-to-manage-user-bitlocker-encryption-exemptions-mbam-25.md" data-raw-source="[How to Manage User BitLocker Encryption Exemptions](how-to-manage-user-bitlocker-encryption-exemptions-mbam-25.md)"> Comment gérer les exemptions de chiffrement BitLocker utilisateur </a> .</p>
<p>Si vous désactivez ou ne configurez pas ce paramètre de stratégie, les instructions de demande d’exemption ne sont pas affichées aux utilisateurs.</p>
<div class="alert">
<strong>Remarque</strong><br/><p>L’exemption des utilisateurs est gérée par utilisateur et non par ordinateur. Si plusieurs utilisateurs se connectent sur le même ordinateur et qu’un utilisateur n’est pas exempté, l’ordinateur est crypté.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>Configurer le programme d’amélioration du produit</p></td>
<td align="left"><p>Configuration suggérée: <strong> activée</strong></p>
<p>Ce paramètre de stratégie vous permet de configurer la manière dont les utilisateurs de MBAM peuvent participer au programme d’amélioration du produit. Ce programme collecte des informations sur le matériel informatique et la façon dont les utilisateurs utilisent MBAM sans interrompre leur fonctionnement. Les informations permettent à Microsoft d’identifier les fonctionnalités MBAM à améliorer. Microsoft n’utilise pas ces informations pour identifier ou contacter les utilisateurs de MBAM.</p>
<p>Si vous activez ce paramètre de stratégie, les utilisateurs peuvent participer au programme d’amélioration du produit.</p>
<p>Si vous désactivez ce paramètre de stratégie, les utilisateurs ne peuvent pas rejoindre le programme d’amélioration du produit.</p>
<p>Si vous ne configurez pas ce paramètre de stratégie, les utilisateurs ont la possibilité de participer au programme d’amélioration du produit.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Fournir l’URL du lien de stratégie de sécurité</p></td>
<td align="left"><p>Configuration suggérée: <strong> activée</strong></p>
<p>Utilisez ce paramètre de stratégie pour spécifier une URL qui s’affiche pour les utilisateurs finaux en tant que lien intitulé stratégie de sécurité de l' &quot; entreprise. &quot; Le lien pointe vers la politique de sécurité interne de votre entreprise et fournit aux utilisateurs finaux des informations sur les exigences en matière de chiffrement. Le lien apparaît lorsque les utilisateurs sont invités par MBAM à chiffrer un lecteur.</p>
<p>Si vous activez ce paramètre de stratégie, vous pouvez configurer l’URL du lien stratégie de sécurité.</p>
<p>Si vous désactivez ou ne configurez pas ce paramètre de stratégie, le lien stratégie de sécurité n’est pas visible aux utilisateurs.</p></td>
</tr>
</tbody>
</table>



### Définitions de la stratégie de groupe des disques fixes

Cette section décrit les définitions de stratégie de disque corrigées pour l’administration et l’analyse du BitLocker sur le nœud d’objet de stratégie de groupe suivant: stratégies de **configuration** de l’ordinateur- &gt; **Policies** &gt; **modèles d’administration** &gt; **composants Windows** &gt; **MDOP MBAM** &gt; **Fixed Drive**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nom de la stratégie</th>
<th align="left">Vue d’ensemble et paramètres de stratégie de groupe suggérés</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Paramètres de chiffrement des lecteurs de données fixes</p></td>
<td align="left"><p>Configuration suggérée: <strong> activée</strong></p>
<p>Ce paramètre de stratégie vous permet de déterminer si les lecteurs de données fixes doivent être chiffrés.</p>
<p>Si le volume du système d’exploitation doit être chiffré, cliquez sur <strong> activer le verrouillage automatique des données du lecteur </strong> .</p>
<p>Lorsque vous activez cette stratégie, vous ne devez pas désactiver l' <strong> option configurer l’utilisation du mot de passe pour les lecteurs de données fixes </strong> , sauf si vous activez ou avez besoin d’utiliser le déverrouillage automatique pour les lecteurs de données fixes.</p>
<p>Si vous devez utiliser le déverrouillage automatique pour les lecteurs de données fixes, vous devez configurer le chiffrement des volumes du système d’exploitation.</p>
<p>Si vous activez ce paramètre de stratégie, les utilisateurs doivent placer tous les lecteurs de données fixes sous protection BitLocker, et les lecteurs de données sont ensuite chiffrés.</p>
<p>Si vous ne configurez pas ce paramètre de stratégie, les utilisateurs ne doivent pas placer de lecteurs de données fixes sous protection BitLocker. Si vous appliquez cette stratégie après le chiffrement de périphériques de données fixes, l’agent MBAM déchiffre les lecteurs de données fixes chiffrés.</p>
<p>Si vous désactivez ce paramètre de stratégie, les utilisateurs ne peuvent pas placer leurs lecteurs de données fixes sous protection BitLocker.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Refuser l’accès en écriture aux lecteurs fixes non protégés par BitLocker</p></td>
<td align="left"><p>Configuration suggérée: <strong> non configuré</strong></p>
<p>Ce paramètre de stratégie détermine s’il est nécessaire de procéder à la protection de BitLocker pour que les lecteurs de données fixes puissent être accessibles sur un ordinateur. Ce paramètre de stratégie est appliqué lorsque vous activez BitLocker.</p>
<p>Lorsque la stratégie n’est pas configurée, tous les lecteurs de données fixes de l’ordinateur sont montés avec une autorisation en lecture/écriture.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Autoriser l’accès à des disques durs fixes protégés par BitLocker provenant de versions antérieures de Windows</p></td>
<td align="left"><p>Configuration suggérée: <strong> non configuré</strong></p>
<p>Activez cette stratégie de manière à ce que les disques fixes avec le système de fichiers FAT puissent être déverrouillés et affichés sur des ordinateurs exécutant Windows Server 2008, Windows Vista, Windows XP avec SP3 ou Windows XP SP2.</p>
<p>Lorsque la stratégie est activée ou n’est pas configurée, les lecteurs fixes qui sont mis en forme avec le système de fichiers FAT peuvent être déverrouillés et leur contenu peut être affiché sur les ordinateurs exécutant Windows Server 2008, Windows Vista, Windows XP SP3 ou Windows XP SP2. Ces systèmes d’exploitation disposent d’autorisations en lecture seule sur les lecteurs protégés par BitLocker.</p>
<p>Lorsque la stratégie est désactivée, les disques fixes qui sont mis en forme avec le système de fichiers FAT ne peuvent pas être déverrouillés et leur contenu ne peut pas être affiché sur les ordinateurs exécutant Windows Server 2008, Windows Vista, Windows XP SP3 ou Windows XP SP2.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Configurer l’utilisation du mot de passe pour les disques fixes</p></td>
<td align="left"><p>Configuration suggérée: <strong> non configuré</strong></p>
<p>Utilisez cette stratégie pour spécifier si un mot de passe est requis pour déverrouiller des lecteurs de données fixes protégés par BitLocker.</p>
<p>Si vous activez ce paramètre de stratégie, les utilisateurs peuvent configurer un mot de passe qui remplit les conditions que vous définissez. BitLocker permet aux utilisateurs de déverrouiller un lecteur avec tout protecteur disponible sur le lecteur.</p>
<p>Ces paramètres sont appliqués lorsque vous activez BitLocker, et non lorsque vous déverrouillez un volume.</p>
<p>Si vous désactivez ce paramètre de stratégie, les utilisateurs ne peuvent pas utiliser de mot de passe.</p>
<p>Lorsque la stratégie n’est pas configurée, les mots de passe sont pris en charge avec les paramètres par défaut, qui n’incluent pas les exigences de complexité des mots de passe et ne nécessitent que huit caractères.</p>
<p>Pour une sécurité accrue, activez cette stratégie, puis sélectionnez <strong> exiger un mot de passe pour le lecteur de données fixes </strong> , cliquez sur <strong> exiger la complexité du mot de passe </strong> , puis définissez la <strong> longueur de mot de passe minimum souhaitée </strong> .</p>
<p>Si vous désactivez ce paramètre de stratégie, les utilisateurs ne peuvent pas utiliser de mot de passe.</p>
<p>Si vous ne configurez pas ce paramètre de stratégie, les mots de passe sont pris en charge avec les paramètres par défaut, qui n’incluent pas les exigences de complexité des mots de passe et ne nécessitent que huit caractères.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Choisir la manière dont les lecteurs fixes protégés par BitLocker peuvent être récupérés</p></td>
<td align="left"><p>Configuration suggérée: <strong> non configuré</strong></p>
<p>Configurez cette stratégie pour activer l’agent de récupération de données BitLocker ou enregistrer les informations de récupération BitLocker dans les services de domaine Active Directory (AD DS).</p>
<p>Lorsque la stratégie n’est pas configurée, l’agent de récupération de données BitLocker est autorisé et les informations de récupération ne sont pas sauvegardées dans AD DS. MBAM ne nécessite pas de sauvegarde des informations de récupération dans AD DS.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Paramètres d’application de la stratégie de chiffrement</p></td>
<td align="left"><p>Configuration suggérée: <strong> activée</strong></p>
<p>Utilisez ce paramètre de stratégie pour configurer le nombre de jours pendant lesquels les lecteurs de données fixes peuvent rester conformes jusqu’à ce qu’ils soient obligés de se conformer aux stratégies MBAM. Les utilisateurs ne peuvent pas différer l’action requise ou en demander une exonération après la période de grâce. La période de grâce commence lorsque le disque de données fixes est considéré comme non conforme. Toutefois, la stratégie de lecteur de données fixes n’est pas appliquée tant que le lecteur du système d’exploitation n’est pas conforme.</p>
<p>Si la période de grâce est expirée et que le lecteur de données fixes n’est toujours pas conforme, les utilisateurs n’ont pas la possibilité de différer ou de demander une exemption. Si le processus de cryptage nécessite une entrée de l’utilisateur, une boîte de dialogue s’affiche pour indiquer que les utilisateurs ne peuvent pas se fermer tant qu’ils ne fournissent pas les informations requises.</p>
<p>Entrez <strong> 0 </strong> dans le dossier <strong> configurer le nombre de jours de la période de grâce de non-conformité pour les lecteurs fixes pour </strong> que le processus de chiffrement commence immédiatement après l’expiration de la période de grâce pour le lecteur du système d’exploitation.</p>
<p>Si vous désactivez ou ne configurez pas ce paramètre, les utilisateurs ne sont pas obligés de se conformer aux stratégies MBAM.</p>
<p>Si aucune interaction utilisateur n’est nécessaire pour ajouter un protecteur, le chiffrement commence en arrière-plan une fois la période de grâce expirée.</p></td>
</tr>
</tbody>
</table>



### Définitions de la stratégie de groupe du système d’exploitation

Cette section décrit l’utilisation de la stratégie de lecteur du système d’exploitation pour l’administration et la surveillance de BitLocker sur le nœud d’objet GPO suivant: stratégies de **Configuration ordinateur** &gt; **Policies** &gt; **modèles d’administration** &gt; **composants Windows** &gt; **MDOP MBAM (gestion de BitLocker)** &gt; **Operating System Drive**.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nom de la stratégie</th>
<th align="left">Vue d’ensemble et paramètres de stratégie de groupe suggérés</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Paramètres de chiffrement de lecteur du système d’exploitation</p></td>
<td align="left"><p>Configuration suggérée: <strong> activée</strong></p>
<p>Ce paramètre de stratégie vous permet de déterminer si le lecteur du système d’exploitation doit être chiffré.</p>
<p>Pour plus de sécurité, envisagez de désactiver les paramètres de stratégie suivants dans les paramètres de veille de la gestion de l' <strong> alimentation du système </strong> &gt; <strong> </strong> &gt; <strong> </strong> lorsque vous les activez avec le protecteur de TPM + pin:</p>
<ul>
<li><p>Autoriser les États de veille (S1-S3) lorsque vous êtes en veille (branché)</p></li>
<li><p>Autoriser les États de veille (S1-S3) en veille (sur batterie)</p></li>
</ul>
<p>Si vous exécutez Microsoft Windows 8 ou une version ultérieure et que vous souhaitez utiliser BitLocker sur un ordinateur dépourvu de TPM, activez la case <strong> </strong> à cocher Autoriser BitLocker sans module de plateforme sécurisée compatible. Dans ce mode, un mot de passe est requis au démarrage. Si vous oubliez le mot de passe, vous devez utiliser l’une des options de récupération de BitLocker pour accéder au lecteur.</p>
<p>Sur un ordinateur équipé d’un TPM compatible, deux types de méthodes d’authentification peuvent être utilisés au démarrage pour renforcer la protection des données chiffrées. Lorsque l’ordinateur démarre, il peut uniquement utiliser le TPM pour l’authentification, ou exiger l’entrée d’un code confidentiel (PIN).</p>
<p>Si vous activez ce paramètre de stratégie, les utilisateurs doivent placer le lecteur du système d’exploitation sous protection BitLocker, et le lecteur est alors chiffré.</p>
<p>Si vous désactivez ce paramètre, les utilisateurs ne peuvent pas placer le lecteur du système d’exploitation sous protection BitLocker. Si vous appliquez cette stratégie après le chiffrement du lecteur du système d’exploitation, le lecteur est alors déchiffré.</p>
<p>Si vous ne configurez pas cette stratégie, le lecteur du système d’exploitation ne doit pas nécessairement être placé sous protection BitLocker.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Autoriser les codes confidentiels améliorés pour le démarrage</p></td>
<td align="left"><p>Configuration suggérée: <strong> non configuré</strong></p>
<p>Utilisez ce paramètre de stratégie pour configurer l’utilisation des codes confidentiels de démarrage étendu avec BitLocker. Les broches de démarrage améliorées autorisent l’utilisation de caractères tels que les lettres majuscules et minuscules, les symboles, les nombres et les espaces. Ce paramètre de stratégie est appliqué lorsque vous activez BitLocker.</p>
<p>Si vous activez ce paramètre de stratégie, tous les nouveaux codes confidentiels de démarrage BitLocker permettent à l’utilisateur final de créer des épingles améliorées. Toutefois, tous les ordinateurs ne peuvent pas prendre en charge des épingles améliorées dans l’environnement de pré-démarrage. Nous vous conseillons vivement d’évaluer la compatibilité de leurs systèmes avec cette fonctionnalité avant de l’activer.</p>
<p>Activez la case à <strong> cocher exiger des broches ASCII uniquement </strong> pour rendre les codes plus compatibles avec les ordinateurs qui limitent le type ou le nombre de caractères pouvant être entrés dans l’environnement de pré-démarrage.</p>
<p>Si vous désactivez ou ne configurez pas ce paramètre de stratégie, les broches améliorées ne sont pas utilisées.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Choisir la manière dont les lecteurs du système d’exploitation protégés par BitLocker peuvent être récupérés</p></td>
<td align="left"><p>Configuration suggérée: <strong> non configuré</strong></p>
<p>Configurez cette stratégie pour activer l’agent de récupération de données BitLocker ou enregistrer les informations de récupération BitLocker dans les services de domaine Active Directory (AD DS).</p>
<p>Lorsque cette stratégie n’est pas configurée, l’agent de récupération de données est autorisé et les informations de récupération ne sont pas sauvegardées dans AD DS.</p>
<p>Dans le cas d’une opération MBAM, les informations de récupération ne doivent pas être sauvegardées dans AD DS.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Configurer l’utilisation des mots de passe pour les lecteurs du système d’exploitation</p></td>
<td align="left"><p>Configuration suggérée: <strong> non configuré</strong></p>
<p>Utilisez ce paramètre de stratégie pour définir les contraintes relatives aux mots de passe utilisés pour déverrouiller les lecteurs de systèmes d’exploitation protégés par BitLocker. Si les protections hors-TPM sont autorisées sur les lecteurs du système d’exploitation, vous pouvez fournir un mot de passe, appliquer les exigences de complexité du mot de passe et configurer une longueur minimale pour le mot de passe. Pour appliquer le paramètre de stratégie de complexité et être efficace, vous devez également activer le paramètre de stratégie de groupe le &quot; mot de passe doit respecter les exigences &quot; de complexité qui se trouvent dans la section Configuration de l’ordinateur &gt; &gt; &gt; &gt; stratégie de mot de passe stratégies de sécurité.</p>
<div class="alert">
<strong>Remarque</strong><br/><p>Ces paramètres sont appliqués lorsque vous activez BitLocker, et non lorsque vous déverrouillez un volume. BitLocker vous permet de déverrouiller un lecteur avec tout protecteur disponible sur le lecteur.</p>
</div>
<div>

</div>
<p>Si vous activez ce paramètre de stratégie, les utilisateurs peuvent configurer un mot de passe qui remplit les conditions que vous définissez. Pour appliquer les exigences de complexité au mot de passe, cliquez sur <strong> exiger la complexité du mot de passe </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Configurer le profil de validation de plateforme TPM pour les configurations de microprogrammes basées sur le BIOS</p></td>
<td align="left"><p>Configuration suggérée: <strong> non configuré</strong></p>
<p>Ce paramètre de stratégie vous permet de configurer la manière dont le matériel de sécurité du module de plateforme sécurisée par ordinateur&#39;s protège la clé de chiffrement BitLocker. Ce paramètre de stratégie ne s’applique pas si l’ordinateur ne possède pas de TPM compatible ou si BitLocker a déjà été activé avec la protection de la plateforme.</p>
<div class="alert">
<strong>Important</strong><br/><p>Ce paramètre de stratégie de groupe s’applique uniquement aux ordinateurs dotés de configurations BIOS ou d’ordinateurs avec le microprogramme UEFI sur lequel un module de service de compatibilité (CSM) est activé. Les ordinateurs qui utilisent un magasin de configuration de microprogramme UEFI natif différentes valeurs dans les registres de configuration de plateforme (PCRs). Utilisez le &quot; paramètre configurer le profil de validation de plateforme de TPM pour le paramètre de stratégie de groupe configurations de microprogrammes UEFI natifs &quot; pour configurer le profil PCR du TPM pour les ordinateurs qui utilisent le microprogramme UEFI natif.</p>
</div>
<div>

</div>
<p>Si vous activez ce paramètre de stratégie avant de procéder à l’activation de BitLocker, vous pouvez configurer les composants de démarrage validés par le TPM avant de déverrouiller l’accès au lecteur de système d’exploitation chiffré par BitLocker. Si l’un de ces composants change alors que la protection de BitLocker est en vigueur, le TPM ne libère pas la clé de chiffrement pour déverrouiller le lecteur et l’ordinateur affiche la console de récupération BitLocker et nécessite que vous fournissiez le mot de passe de récupération ou la clé de récupération pour déverrouiller le lecteur.</p>
<p>Si vous désactivez ou ne configurez pas ce paramètre de stratégie, BitLocker utilise le profil de validation de plateforme par défaut ou le profil de validation de plateforme spécifié par le script de configuration.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Configurer le profil de validation de plateforme TPM</p></td>
<td align="left"><p>Configuration suggérée: <strong> non configuré</strong></p>
<p>Ce paramètre de stratégie vous permet de configurer la manière dont le matériel de sécurité du module de plateforme sécurisée par ordinateur&#39;s protège la clé de chiffrement BitLocker. Ce paramètre de stratégie ne s’applique pas si l’ordinateur ne possède pas de TPM compatible ou si BitLocker a déjà été activé avec la protection de la plateforme.</p>
<p>Si vous activez ce paramètre de stratégie avant de procéder à l’activation de BitLocker, vous pouvez configurer les composants de démarrage validés par le TPM avant de déverrouiller l’accès au lecteur de système d’exploitation chiffré par BitLocker. Si l’un de ces composants change alors que la protection de BitLocker est en vigueur, le TPM ne libère pas la clé de chiffrement pour déverrouiller le lecteur et l’ordinateur affiche la console de récupération BitLocker et nécessite que vous fournissiez le mot de passe de récupération ou la clé de récupération pour déverrouiller le lecteur.</p>
<p>Si vous désactivez ou ne configurez pas ce paramètre de stratégie, BitLocker utilise le profil de validation de plateforme par défaut ou le profil de validation de plateforme spécifié par le script de configuration.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Configurer le profil de validation de la plateforme de GPC pour les configurations de microprogramme UEFI natifs</p></td>
<td align="left"><p>Configuration suggérée: <strong> non configuré</strong></p>
<p>Ce paramètre de stratégie vous permet de configurer la manière dont le matériel de sécurité du module de plateforme sécurisée par ordinateur&#39;s protège la clé de chiffrement BitLocker. Ce paramètre de stratégie ne s’applique pas si l’ordinateur ne possède pas de TPM compatible ou si BitLocker a déjà été activé avec la protection de la plateforme.</p>
<div class="alert">
<strong>Important</strong><br/><p>Ce paramètre de stratégie de groupe s’applique uniquement aux ordinateurs disposant d’une configuration de microprogramme UEFI native.</p>
</div>
<div>

</div>
<p>Si vous activez ce paramètre de stratégie avant de procéder à l’activation de BitLocker, vous pouvez configurer les composants de démarrage validés par le TPM avant de débloquer l’accès au lecteur de système d’exploitation chiffré par BitLocker. Si l’un de ces composants change alors que la protection de BitLocker est en vigueur, le TPM ne libère pas la clé de chiffrement pour déverrouiller le lecteur et l’ordinateur affiche la console de récupération BitLocker et nécessite que vous fournissiez le mot de passe de récupération ou la clé de récupération pour déverrouiller le lecteur.</p>
<p>Si vous désactivez ou ne configurez pas ce paramètre de stratégie, BitLocker utilise le profil de validation de plateforme par défaut ou le profil de validation de plateforme spécifié par le script de configuration.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Réinitialiser les données de validation de plateforme après la récupération de BitLocker</p></td>
<td align="left"><p>Configuration suggérée: <strong> non configuré</strong></p>
<p>Utilisez ce paramètre de stratégie pour déterminer si les données de validation de la plateforme sont actualisées lorsque Windows est démarré après la récupération de BitLocker.</p>
<p>Si vous activez ce paramètre de stratégie, les données de validation de la plateforme sont actualisées lorsque Windows est démarré après une récupération de BitLocker. Si vous désactivez ce paramètre de stratégie, les données de validation de plateforme ne sont pas actualisées lorsque Windows est démarré après la récupération de BitLocker. Si vous ne configurez pas ce paramètre de stratégie, les données de validation de plateforme sont actualisées lorsque Windows est démarré après la récupération de BitLocker.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Utiliser le profil de validation des données de configuration de démarrage améliorée</p></td>
<td align="left"><p>Configuration suggérée: <strong> non configuré</strong></p>
<p>Ce paramètre de stratégie vous permet de sélectionner des paramètres de données de configuration de démarrage spécifiques à vérifier lors de la validation de la plateforme.</p>
<p>Si vous activez ce paramètre de stratégie, vous pouvez ajouter des paramètres supplémentaires, supprimer les paramètres par défaut ou les deux. Si vous désactivez ce paramètre de stratégie, l’ordinateur bascule vers un profil BCD semblable au profil BCD par défaut utilisé par Windows 7. Si vous ne configurez pas ce paramètre de stratégie, l’ordinateur vérifie les paramètres de BCD Windows par défaut.</p>
<div class="alert">
<strong>Remarque</strong><br/><p>Lorsque BitLocker utilise le démarrage sécurisé pour la validation de l’intégrité des données de configuration de plateforme et de démarrage (BCD), telle que définie par la &quot; stratégie autoriser le démarrage sécurisé pour la validation de l’intégrité &quot; , la &quot; stratégie utiliser le profil de validation des données de configuration de démarrage améliorée &quot; est ignorée.</p>
</div>
<div>

</div>
<p>Le paramètre qui contrôle le débogage de démarrage (0x16000010) est toujours validé et n’a aucun effet s’il est inclus dans les champs fournis.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Paramètres d’application de la stratégie de chiffrement</p></td>
<td align="left"><p>Configuration suggérée: <strong> activée</strong></p>
<p>Utilisez ce paramètre de stratégie pour configurer le nombre de jours pendant lesquels les utilisateurs peuvent différer conformément aux stratégies MBAM pour le lecteur de leur système d’exploitation. La période de grâce commence alors que le système d’exploitation est détecté pour la première fois comme non conforme. Après l’expiration de cette période de grâce, les utilisateurs ne peuvent pas différer l’action requise ou demander une exemption.</p>
<p>Si le processus de cryptage nécessite une entrée de l’utilisateur, une boîte de dialogue s’affiche pour indiquer que les utilisateurs ne peuvent pas se fermer tant qu’ils ne fournissent pas les informations requises.</p>
<p>Si vous désactivez ou ne configurez pas ce paramètre, les utilisateurs ne sont pas obligés de se conformer aux stratégies MBAM.</p>
<p>Si aucune interaction utilisateur n’est nécessaire pour ajouter un protecteur, le chiffrement commence en arrière-plan une fois la période de grâce expirée.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Configurer le message et l’URL de récupération avant démarrage</p></td>
<td align="left"><p>Configuration suggérée: <strong> non configuré</strong></p>
<p>Activez ce paramètre de stratégie pour configurer un message de récupération personnalisé ou pour spécifier une URL qui s’affiche dans l’écran prédémarrage de la récupération BitLocker lorsque le lecteur du système d’exploitation est verrouillé. Ce paramètre est uniquement disponible sur les ordinateurs clients exécutant Windows 10.</p>
<p>Lorsque cette stratégie est activée, vous pouvez sélectionner l’une de ces options pour le message de récupération avant démarrage:</p>
<ul>
<li><p><strong>Utiliser un message de récupération personnalisé </strong> : sélectionnez cette option pour inclure un message personnalisé dans l’écran de récupération de BitLocker avant démarrage. Dans la <strong> boîte de dialogue de l’option de message de récupération personnalisé </strong> , tapez le message que vous souhaitez afficher. Si vous souhaitez également spécifier une URL de récupération, incluez-la dans le cadre de votre message de récupération personnalisé.</p></li>
<li><p><strong>Utiliser une URL de récupération personnalisée </strong> : sélectionnez cette option pour remplacer l’URL par défaut qui s’affiche dans l’écran de récupération de BitLocker avant démarrage. Dans l' <strong> option URL de récupération personnalisée </strong> , entrez l’URL que vous voulez afficher.</p></li>
<li><p><strong>Utiliser le message de récupération par défaut et l’URL </strong> : sélectionnez cette option pour afficher le message et l’URL de récupération de BitLocker par défaut dans l’écran de récupération de BitLocker avant démarrage. Si vous avez précédemment configuré un message de récupération personnalisé ou une URL et que vous souhaitez rétablir le message par défaut, vous devez activer cette stratégie et sélectionner l' <strong> option utiliser le message de récupération par défaut et l' </strong> option URL.</p></li>
</ul>
<div class="alert">
<strong>Remarque</strong><br/><p>Tous les caractères et langues ne sont pas pris en charge dans Pre-Boot. Nous vous recommandons d’essayer de vérifier que les caractères que vous utilisez pour le message personnalisé ou l’URL apparaissent correctement sur l’écran de récupération de BitLocker avant démarrage.</p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



### Définitions de la stratégie de groupe du lecteur amovible

Cette section décrit les définitions de stratégie de groupe du lecteur amovible pour l’administration et la surveillance de BitLocker sur le nœud d’objet GPO suivant: stratégies de **Configuration ordinateur** &gt; **Policies** &gt; **modèles d’administration** &gt; **composants Windows** &gt; **MBAM (gestion de BitLocker)** - &gt; **lecteur amovible**.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nom de la stratégie</th>
<th align="left">Vue d’ensemble et paramètres de stratégie de groupe suggérés</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Contrôler l’utilisation de BitLocker sur des lecteurs amovibles</p></td>
<td align="left"><p>Configuration suggérée: <strong> activée</strong></p>
<p>Cette stratégie contrôle l’utilisation de BitLocker sur les lecteurs de données amovibles.</p>
<p>Cliquez sur <strong> autoriser les utilisateurs à appliquer la protection BitLocker sur les lecteurs de données amovibles </strong> pour permettre aux utilisateurs d’exécuter l’Assistant Configuration de BitLocker sur un lecteur de données amovible.</p>
<p>Cliquez sur <strong> autoriser les utilisateurs à suspendre et décrypter BitLocker sur des lecteurs de données amovibles </strong> pour permettre aux utilisateurs de supprimer le chiffrement de lecteur BitLocker du lecteur ou de suspendre le chiffrement lors de la maintenance.</p>
<p>Lorsque cette stratégie est activée et que vous cliquez sur <strong> autoriser les utilisateurs à appliquer la protection BitLocker sur des lecteurs de données amovibles </strong> , le client MBAM enregistre les informations de récupération relatives aux lecteurs amovibles sur le serveur de récupération de clés MBAM et permet aux utilisateurs de récupérer le lecteur en cas de perte du mot de passe.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Refuser l'accès en écriture aux lecteurs amovibles non protégés par BitLocker</p></td>
<td align="left"><p>Configuration suggérée: <strong> non configuré</strong></p>
<p>Activez cette stratégie pour autoriser uniquement les autorisations d’écriture sur les lecteurs protégés par BitLocker.</p>
<p>Lorsque cette stratégie est activée, tous les lecteurs de données amovibles de l’ordinateur doivent être chiffrés avant l’autorisation d’écriture.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Autoriser l’accès aux lecteurs amovibles protégés par BitLocker provenant de versions antérieures de Windows</p></td>
<td align="left"><p>Configuration suggérée: <strong> non configuré</strong></p>
<p>Activez cette stratégie pour autoriser le déverrouillage et l’affichage de disques fixes avec le système de fichiers FAT sur les ordinateurs exécutant Windows Server 2008, Windows Vista, Windows XP avec SP3 ou Windows XP SP2.</p>
<p>Lorsque cette stratégie n’est pas configurée, les lecteurs amovibles mis en forme avec le système de fichiers FAT peuvent être déverrouillés sur les ordinateurs exécutant Windows Server 2008, Windows Vista, Windows XP avec SP3 ou Windows XP SP2, et leur contenu peut être affiché. Ces systèmes d’exploitation disposent d’autorisations en lecture seule sur les lecteurs protégés par BitLocker.</p>
<p>Lorsque la stratégie est désactivée, les lecteurs amovibles mis en forme avec le système de fichiers FAT ne peuvent pas être déverrouillés et leur contenu ne peut pas être affiché sur les ordinateurs exécutant Windows Server 2008, Windows Vista, Windows XP SP3 ou Windows XP SP2.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Configurer l’utilisation du mot de passe pour les lecteurs de données amovibles</p></td>
<td align="left"><p>Configuration suggérée: <strong> non configuré</strong></p>
<p>Activez cette stratégie pour configurer la protection par mot de passe sur les lecteurs de données amovibles.</p>
<p>Lorsque cette stratégie n’est pas configurée, les mots de passe sont pris en charge avec les paramètres par défaut, qui n’incluent pas les exigences de complexité des mots de passe et ne nécessitent que huit caractères.</p>
<p>Pour une sécurité accrue, vous pouvez activer cette stratégie et sélectionner <strong> exiger un mot de passe pour le lecteur de données amovibles </strong> , cliquer sur <strong> exiger la complexité du mot de passe </strong> et définir la <strong> longueur de mot de passe minimum recommandée </strong> .</p></td>
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


[Préparation de votre environnement pour MBAM2.5](preparing-your-environment-for-mbam-25.md)

[Conditions préalables au déploiement de MBAM2.5](mbam-25-deployment-prerequisites.md)


## Vous avez une suggestion pour MBAM?
- Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring) 
- Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).






