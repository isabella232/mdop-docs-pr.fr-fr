---
title: À propos de MBAM2.5
description: À propos de MBAM2.5
author: dansimp
ms.assetid: 1ce218ec-4d2e-4a75-8d1a-68d737a8f3c9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: d4c9ff0bc5ee3f7dc51a56cc428081a7c3783694
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810421"
---
# À propos de MBAM2.5


La gestion et l’analyse de BitLocker (MBAM) 2,5 fournit une interface d’administration simplifiée pour le chiffrement de lecteur BitLocker. BitLocker fournit une protection améliorée contre le vol de données ou l’exposition des données pour les ordinateurs perdus ou volés. BitLocker chiffre toutes les données stockées sur les volumes et lecteurs de systèmes d’exploitation Windows et les lecteurs de données configurés.

## Présentation de MBAM


MBAM 2,5 offre les fonctionnalités suivantes:

-   Permet aux administrateurs d’automatiser le processus de cryptage des volumes sur les ordinateurs clients au sein de l’entreprise.

-   Permet aux responsables de la sécurité de déterminer rapidement l’état de conformité de chaque ordinateur ou même de l’entreprise.

-   Fournit un rapport centralisé et une gestion du matériel avec Microsoft System Center Configuration Manager.

-   Réduit la charge de travail de l’assistance technique pour aider les utilisateurs finaux à utiliser le code confidentiel BitLocker et les requêtes de clé de récupération.

-   Permet aux utilisateurs finaux de récupérer des appareils chiffrés indépendamment via le portail libre-service.

-   Permet aux responsables de la sécurité d’auditer facilement l’accès pour récupérer des informations clés.

-   Permet aux utilisateurs de Windows d’entreprise de continuer à travailler en tout lieu et de garantir la protection des données d’entreprise.

MBAM applique les options de stratégie de chiffrement BitLocker que vous avez définies pour votre entreprise, surveille la conformité des ordinateurs clients avec ces stratégies et signale l’état de chiffrement de l’ordinateur de l’entreprise et de la personne. De plus, MBAM vous permet d’accéder aux informations de clé de récupération lorsque les utilisateurs oublient leur code confidentiel ou leur mot de passe, ou lorsque leurs enregistrements de BIOS ou de démarrage changent.

Les groupes suivants peuvent être intéressés par l’utilisation de MBAM pour gérer BitLocker:

-   Administrateurs, responsables de la sécurité informatique et responsables de la conformité chargés de veiller à ce que les données confidentielles ne soient pas divulguées sans autorisation.

-   Administrateurs responsables de la sécurité informatique de bureaux distants ou de succursales

-   Administrateurs responsables des ordinateurs clients exécutant Windows

**Remarques**  BitLocker n’est pas expliqué en détail dans cette documentation MBAM. Pour plus d’informations, voir [vue d’ensemble du chiffrement de lecteur BitLocker](https://go.microsoft.com/fwlink/p/?LinkId=225013).

 

## <a href="" id="what-s-new-in-mbam-2-5"></a>Nouveautés de MBAM 2,5


Cette section décrit les nouvelles fonctionnalités de MBAM 2,5.

### Prise en charge de Microsoft SQL Server 2014

MBAM ajoute la prise en charge de Microsoft SQL Server 2014, en plus des logiciels pris en charge dans les versions antérieures d’MBAM.

### <a href="" id="-------------mbam-group-policy-templates-downloaded-separately"></a> Modèles de stratégie de groupe MBAM téléchargés séparément

Les modèles de stratégie de groupe MBAM doivent être téléchargés séparément de l’installation d’MBAM. Dans les versions précédentes de MBAM, le programme d’installation de MBAM inclut un modèle de stratégie MBAM, qui contenait les objets de stratégie de groupe spécifiques MBAM (GPO) qui définissent les paramètres d’implémentation de MBAM pour le chiffrement de lecteur BitLocker. Ces objets de stratégie de groupe ont été supprimés du programme d’installation MBAM. Vous pouvez à présent télécharger les objets de stratégie de groupe à partir de la [façon d’obtenir des modèles de stratégie de groupe MDOP (. admx)](https://go.microsoft.com/fwlink/p/?LinkId=393941) et de les copier sur un serveur ou une station de travail avant de commencer l’installation du client MBAM. Vous pouvez copier les modèles de stratégie de groupe sur n’importe quel serveur ou station de travail exécutant une version prise en charge du système d’exploitation Windows Server ou Windows.

**Important**  Ne modifiez pas les paramètres de stratégie de groupe du nœud **BitLocker Drive Encryption** , ou MBAM ne fonctionne pas correctement. Lorsque vous configurez les paramètres de stratégie de groupe dans le nœud **MDOP MBAM (gestion du BitLocker)** , MBAM configure automatiquement les paramètres de chiffrement de lecteur BitLocker pour vous.

 

Les fichiers de modèles que vous devez copier sur un serveur ou une station de travail sont les suivants:

-   BitLockerManagement. adml

-   BitLockerManagement. admx

-   BitLockerUserManagement. adml

-   BitLockerUserManagement. admx

Copiez les fichiers de modèles dans l’emplacement qui correspond le mieux à vos besoins. Pour les fichiers spécifiques à une langue, qui doivent être copiés dans un dossier spécifique à une langue, la console de gestion des stratégies de groupe est nécessaire pour afficher les fichiers.

- Pour installer les fichiers de modèle localement sur un serveur ou une station de travail, copiez les fichiers vers l’un des emplacements suivants.

  <table>
  <colgroup>
  <col width="50%" />
  <col width="50%" />
  </colgroup>
  <thead>
  <tr class="header">
  <th align="left">Type de fichier</th>
  <th align="left">Emplacement du fichier</th>
  </tr>
  </thead>
  <tbody>
  <tr class="odd">
  <td align="left"><p>langage neutre (. admx)</p></td>
  <td align="left"><p><em>% systemroot% </em> \policyDefinitions</p></td>
  </tr>
  <tr class="even">
  <td align="left"><p>spécifiques d’une langue (. adml)</p></td>
  <td align="left"><p><em>% systemroot% </em> \policyDefinitions [ <em> MUIculture </em> ] (par exemple, le fichier spécifique à la langue américaine sera stocké dans <em> % systemroot% &lt; /em &gt; policyDefinitions\en-US)</p></td>
  </tr>
  </tbody>
  </table>

     

- Pour que les modèles soient disponibles pour tous les administrateurs de stratégie de groupe dans un domaine, copiez les fichiers vers l’un des emplacements suivants sur un contrôleur de domaine.

  <table>
  <colgroup>
  <col width="50%" />
  <col width="50%" />
  </colgroup>
  <thead>
  <tr class="header">
  <th align="left">Type de fichier</th>
  <th align="left">Emplacement du fichier de contrôleur de domaine</th>
  </tr>
  </thead>
  <tbody>
  <tr class="odd">
  <td align="left"><p>Langage neutre (. admx)</p></td>
  <td align="left"><p><em>% systemroot% </em> sysvol\domain\policies\PolicyDefinitions</p></td>
  </tr>
  <tr class="even">
  <td align="left"><p>Spécifiques d’une langue (. adml)</p></td>
  <td align="left"><p><em>% systemroot% </em> \sysvol\domain\policies\PolicyDefinitions [ <em> MUIculture </em> ] (par exemple, le fichier spécifique à la langue américaine est stocké dans <em> % systemroot% </em> \sysvol\domain\policies\PolicyDefinitions\en-US)</p></td>
  </tr>
  </tbody>
  </table>

     

Pour plus d’informations sur les fichiers de modèles, voir [gestion détaillée des fichiers ADMX de stratégie de groupe](https://go.microsoft.com/fwlink/?LinkId=392818).

### Possibilité d’appliquer les stratégies de cryptage sur le système d’exploitation et les lecteurs de données fixes

MBAM 2.5 vous permet d’appliquer les stratégies de cryptage sur le système d’exploitation et les lecteurs de données fixes pour les ordinateurs de votre organisation et de limiter le nombre de jours pendant lesquels les utilisateurs finaux peuvent demander un ajournement de l’obligation de se conformer aux stratégies de chiffrement MBAM.

Pour vous permettre de configurer l’application d’une stratégie de chiffrement, un nouveau paramètre de stratégie de groupe appelé paramètres d’application de la stratégie de chiffrement a été ajouté pour les lecteurs du système d’exploitation et les lecteurs de données fixes. Ce paramètre est décrit dans le tableau suivant.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Paramètre de la stratégie de groupe</th>
<th align="left">Description</th>
<th align="left">Nœud de stratégie de groupe utilisé pour configurer ce paramètre</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Paramètres d’application de la stratégie de chiffrement (lecteur du système d’exploitation)</p></td>
<td align="left"><p>Pour ce paramètre, utilisez l’option <strong> configurer le nombre de jours de la période de grâce de non-conformité pour les lecteurs du système d’exploitation </strong> afin de configurer une période de grâce.</p>
<p>La période de grâce spécifie le nombre de jours pendant lesquels les utilisateurs finaux peuvent retarder la mise en conformité avec les stratégies MBAM pour le lecteur de leur système d’exploitation après que le lecteur a été détecté pour la première fois comme non conforme.</p>
<p>Après l’expiration de la période de grâce configurée, les utilisateurs ne peuvent pas différer l’action requise ou demander une exemption.</p>
<p>Si une interaction utilisateur est nécessaire (par exemple, si vous utilisez le module de plateforme sécurisée (TPM) + NIP ou à l’aide d’un protecteur de mot de passe), une boîte de dialogue s’affiche, et les utilisateurs ne peuvent pas la fermer tant qu’ils n’ont pas fourni les informations requises. S’il s’agit d’un module de plateforme sécurisée uniquement, le chiffrement commence immédiatement en arrière-plan sans aucune entrée utilisateur.</p>
<p>Les utilisateurs ne peuvent pas demander d’exemption par le biais de l’Assistant chiffrement de BitLocker. Au lieu de cela, ils doivent contacter leur support technique ou utiliser le processus que leur organisation utilise pour les demandes d’exemption.</p></td>
<td align="left"><p>Stratégies de Configuration ordinateur &gt; &gt; modèles d’administration &gt; composants Windows composants &gt; MDOP MBAM (gestion de BitLocker) &gt; lecteur du système d’exploitation</p></td>
</tr>
<tr class="even">
<td align="left"><p>Paramètres d’application de la stratégie de chiffrement (lecteurs de données fixes)</p></td>
<td align="left"><p>Pour ce paramètre, utilisez l’option <strong> configurer le nombre de jours de période de grâce de non-conformité pour les disques fixes </strong> pour configurer une période de grâce.</p>
<p>La période de grâce spécifie le nombre de jours pendant lesquels les utilisateurs finaux peuvent différer la conformité avec des stratégies MBAM pour leur lecteur fixe une fois que le lecteur a été détecté pour la première fois comme non conforme.</p>
<p>La période de grâce commence lorsque le disque fixe est considéré comme non conforme. Si vous utilisez le déverrouillage automatique, la stratégie ne sera pas appliquée tant que le lecteur du système d’exploitation ne sera pas conforme. Toutefois, si vous n’utilisez pas le déverrouillage automatique, le chiffrement du lecteur de données fixes peut commencer avant que le lecteur du système d’exploitation soit entièrement chiffré.</p>
<p>Après l’expiration de la période de grâce configurée, les utilisateurs ne peuvent pas différer l’action requise ou demander une exemption. Si une interaction utilisateur est requise, une boîte de dialogue s’affiche et les utilisateurs ne peuvent pas la fermer tant qu’ils n’ont pas fourni les informations requises.</p></td>
<td align="left"><p>Stratégies de Configuration ordinateur &gt; &gt; modèles d’administration &gt; composants Windows &gt; MDOP MBAM (gestion de BitLocker) &gt; lecteur fixe</p></td>
</tr>
</tbody>
</table>

 

### Possibilité de fournir une URL dans l’Assistant chiffrement de lecteur BitLocker pour pointer sur votre stratégie de sécurité

Un nouveau paramètre de stratégie de groupe, **Spécifiez l’URL du lien de stratégie de sécurité**, qui vous permet de configurer une URL qui sera présentée aux utilisateurs finaux en tant que lien appelé **stratégie de sécurité**de l’entreprise. Ce lien apparaît lorsque MBAM invite les utilisateurs à chiffrer un volume.

Si vous activez ce paramètre de stratégie, vous pouvez configurer l’URL du lien **stratégie de sécurité** de l’entreprise. Si vous désactivez ou ne configurez pas ce paramètre de stratégie, le lien **stratégie de sécurité** de l’entreprise n’est pas visible aux utilisateurs.

Le nouveau paramètre de stratégie de groupe se trouve dans le nœud d’objet de stratégie de groupe suivant: stratégies de **configuration** &gt; **Policies** &gt; **d’ordinateur modèles d’administration** &gt; **composants Windows** &gt; **de MDOP MBAM (gestion de BitLocker) &gt; gestion du client**.

### Prise en charge de clés de récupération compatibles FIPS

MBAM 2.5 prend en charge les clés de récupération de BitLocker compatibles FIPS (Federal Information Processing Standard) sur les appareils exécutant le système d’exploitation Windows 8.1. La clé de récupération n’était pas compatible FIPS dans les versions antérieures de Windows. Cette amélioration a pour effet d’améliorer le processus de récupération des lecteurs dans les organisations qui nécessitent une conformité FIPS, car cela permet aux utilisateurs finaux d’utiliser le portail libre-service ou le site Web d’administration et de surveillance (support technique) pour récupérer leurs lecteurs s’ils ont oublié leur code confidentiel ou leur mot de passe ou s’ils sont bloqués. La nouvelle fonctionnalité de conformité FIPS ne s’étend pas aux protecteurs de mot de passe.

Pour activer la conformité FIPS au sein de votre organisation, vous devez configurer les paramètres de stratégie de groupe FIPS (Federal Information Processing Standard). Pour obtenir des instructions de configuration, voir [paramètres de stratégie de groupe BitLocker](https://go.microsoft.com/fwlink/?LinkId=393560).

Pour les ordinateurs clients qui exécutent les systèmes d’exploitation Windows8 ou de contenu d’urgence sans le [correctif BitLocker installé](https://support.microsoft.com/kb/3015477), les administrateurs informatiques continuent à utiliser le protecteur DRA (Data Recovery agents) dans les environnements compatibles FIPS. Pour plus d’informations sur l’utilisation de DRA, voir [utilisation d’agents de récupération de données avec BitLocker](https://go.microsoft.com/fwlink/?LinkId=393557).

Pour télécharger et installer le correctif BitLocker pour les ordinateurs Windows 7 et Windows 8, voir [package de correctif 2 pour l’administration et la 2,5 surveillance de BitLocker](https://support.microsoft.com/kb/3015477) .

### Prise en charge des déploiements de haute disponibilité

MBAM prend en charge les scénarios de haute disponibilité suivants, en plus des topologies d’intégration à deux serveurs et Configuration Manager standard:

-   Groupes de disponibilité SQL Server AlwaysOn

-   Regroupement SQL Server

-   Équilibrage de charge réseau (NLB)

-   Mise en miroir SQL Server

-   Sauvegarde du service de cliché instantané de volume (VSS)

Pour plus d’informations sur ces fonctionnalités, reportez-vous à la rubrique [planification de la haute disponibilité MBAM 2,5](planning-for-mbam-25-high-availability.md).

### <a href="" id="management-of-roles-for-administration-and-monitoring-website-changed-"></a>Gestion des rôles pour le site Web d’administration et de surveillance modifié

Dans MBAM 2.5, vous devez créer des groupes de sécurité dans les services de domaine Active Directory (AD DS) pour gérer les rôles qui fournissent des droits d’accès au site Web d’administration et de surveillance. Les rôles permettent aux utilisateurs qui se trouvent dans des groupes de sécurité spécifiques d’effectuer différentes tâches sur le site Web (par exemple, affichage de rapports ou assistance des utilisateurs finaux pour récupérer des lecteurs chiffrés). Dans les versions précédentes de MBAM, les rôles étaient gérés en utilisant des groupes locaux.

Dans MBAM 2.5, le terme «rôles» remplace le terme «rôles d’administrateur» utilisé dans les versions antérieures d’MBAM. Par ailleurs, dans MBAM 2.5, le rôle «administrateurs système MBAM» a été supprimé.

Le tableau suivant répertorie les groupes de sécurité que vous devez créer dans AD DS. Vous pouvez utiliser n’importe quel nom pour les groupes de sécurité.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Rôle</th>
<th align="left">Droits d’accès pour ce rôle sur le site Web d’administration et de surveillance</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Utilisateurs du support technique MBAM</p></td>
<td align="left"><p>Donne accès aux zones gérer le module de plateforme sécurisée et de réparation du site Web d’administration et de surveillance de MBAM. Les utilisateurs qui ont accès à ces zones doivent remplir tous les champs lorsqu’ils utilisent les deux zones.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Utilisateurs de rapports MBAM</p></td>
<td align="left"><p>Donne accès aux rapports figurant sur le site Web d’administration et de surveillance.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Utilisateurs du support technique avancée MBAM</p></td>
<td align="left"><p>Donne accès à toutes les zones du site Web d’administration et de surveillance. Les utilisateurs de ce groupe doivent uniquement saisir la clé de récupération, pas le domaine et le nom d’utilisateur de l’utilisateur final, pour aider les utilisateurs finaux à récupérer leurs lecteurs. Si un utilisateur est membre du groupe MBAM du support technique et du groupe utilisateurs du support technique avancé MBAM, les autorisations du groupe utilisateurs du support technique avancé MBAM remplacent les autorisations du groupe utilisateurs du support technique MBAM.</p></td>
</tr>
</tbody>
</table>

 

Une fois les groupes de sécurité créés dans ADDS, attribuez des utilisateurs et/ou des groupes au groupe de sécurité approprié pour activer le niveau d’accès correspondant au site Web d’administration et de surveillance. Pour permettre aux utilisateurs disposant de chaque rôle d’accéder au site Web d’administration et de surveillance, vous devez également spécifier chaque groupe de sécurité lorsque vous configurez le site Web d’administration et de surveillance.

### Cmdlets Windows PowerShell pour la configuration des fonctionnalités de MBAM Server

Les applets de cmdlet Windows PowerShell pour MBAM 2.5 vous permettent de configurer et de gérer les fonctionnalités de MBAM Server. Chaque fonctionnalité est associée à une cmdlet Windows PowerShell correspondante que vous pouvez utiliser pour activer ou désactiver des fonctionnalités, ou pour obtenir des informations sur la fonctionnalité.

Pour la configuration requise et les conditions préalables à l’utilisation de Windows PowerShell, reportez-vous à [Configuration des fonctionnalités du serveur MBAM 2,5 à l’aide de Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md).

**Pour charger l’aide 2,5 de MBAM pour les applets de cmdlet Windows PowerShell après l’installation du logiciel serveur MBAM**

1.  Ouvrez l’environnement d’exécution de scripts Windows PowerShell ou Windows PowerShell intégré.

2.  Tapez **Update-aide – module Microsoft. mbam**.

L’aide de Windows PowerShell pour MBAM est disponible dans les formats suivants:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Format d’aide de Windows PowerShell</th>
<th align="left">Informations supplémentaires</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>À l’invite de commandes Windows PowerShell, tapez <strong> get- </strong> &lt; <em> cmdlet cmdlet.</em>&gt;</p></td>
<td align="left"><p>Pour télécharger les dernières cmdlets Windows PowerShell, suivez les instructions de la section précédente sur le chargement de l’aide de Windows PowerShell pour MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Sur TechNet en tant que pages Web</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393498" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393498">https://go.microsoft.com/fwlink/?LinkId=393498</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Dans le centre de téléchargement en tant que fichier Word. docx</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393497" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393497">https://go.microsoft.com/fwlink/?LinkId=393497</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Dans le centre de téléchargement sous forme de fichier. pdf</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393499" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393499">https://go.microsoft.com/fwlink/?LinkId=393499</a></p></td>
</tr>
</tbody>
</table>

 

### La prise en charge des épingles ASCII uniquement et améliorées et la possibilité d’éviter des caractères séquentiels et répétitifs

**Autoriser les codes confidentiels avancés pour le paramètre de stratégie de groupe de démarrage**

Le paramètre **de stratégie de groupe autoriser les codes confidentiels pour le démarrage**permet de configurer l’utilisation de codes secrets de démarrage étendus avec BitLocker. Les broches de démarrage avancées permettent aux utilisateurs d’entrer n’importe quelle touche sur un clavier complet, y compris les majuscules et les minuscules, les symboles, les nombres et les espaces. Si vous activez ce paramètre de stratégie, tous les nouveaux codes secrets de démarrage BitLocker qui sont définis seront des épingles améliorées. Si vous désactivez ou ne configurez pas ce paramètre de stratégie, les broches améliorées ne peuvent pas être utilisées.

Tous les ordinateurs ne prennent pas en charge l’entrée de broches améliorées dans l’environnement d’exécution de Pre-Boot (PXE). Avant d’activer ce paramètre de stratégie de groupe pour votre organisation, effectuez une vérification du système pendant le processus de configuration de BitLocker pour vous assurer que le BIOS de l’ordinateur prend en charge l’utilisation du clavier complet dans PXE. Pour plus d’informations, reportez-vous [à planification des exigences relatives aux stratégies de groupe MBAM 2,5](planning-for-mbam-25-group-policy-requirements.md).

**Case à cocher exiger des broches ASCII uniquement**

Le paramètre **autoriser les codes confidentiels pour une stratégie de groupe de démarrage** contient également une case à cocher nécessite un **code confidentiel en ASCII uniquement** . Si les ordinateurs de votre organisation ne prennent pas en charge l’utilisation du clavier complet dans PXE, vous pouvez activer le paramètre **autoriser les codes confidentiels optimisés pour le groupe de démarrage** , puis activer la case à cocher **exiger des broches ASCII uniquement** pour exiger que les broches améliorées utilisent uniquement des caractères ASCII imprimables.

**Utilisation appliquée de caractères non séquentiels et non répétitifs**

MBAM 2.5 empêche les utilisateurs finaux de créer des épingles qui se composent de chiffres répétitifs (par exemple, 1111) ou de numéros séquentiels (par exemple, 1234). Si les utilisateurs finaux essaient d’entrer un mot de passe contenant au moins trois numéros répétitifs ou séquentiels, l’Assistant chiffrement de lecteur BitLocker affiche un message d’erreur et empêche les utilisateurs d’entrer un code confidentiel aux caractères interdits.

### Ajout du certificat DRA au rapport de conformité de l’ordinateur BitLocker

Un nouveau type de protecteur, qui est le certificat de l’agent de récupération de données (DRA), a été ajouté au rapport de conformité de l’ordinateur BitLocker dans Configuration Manager. Ce type de protecteur s’applique aux lecteurs du système d’exploitation et il apparaît dans la section volume de l' **ordinateur** dans la colonne **types de protecteur** .

### Prise en charge des déploiements de prise en charge de plusieurs forêts

MBAM 2,5 prend en charge les types de déploiements de forêts multiples suivants:

-   Forêt unique avec domaine unique

-   Forêt unique avec une seule arborescence et plusieurs domaines

-   Forêt unique avec plusieurs arbres et espaces de noms disjoints

-   Plusieurs forêts dans une topologie de forêt centrale

-   Plusieurs forêts dans une topologie de forêt de ressources

Il n’y a pas de prise en charge de la migration de forêt (passage de l’un à l’autre, d’une ressource à une autre, d’une ressource à une autre, etc.) ou d’une mise à niveau ou d’une version antérieure.

La configuration requise pour le déploiement d’MBAM dans les déploiements de forêts multiples est la suivante:

-   La forêt doit être exécutée sur des versions prises en charge de Windows Server.

-   Une approbation bidirectionnelle ou à sens unique est obligatoire. Les approbations à sens unique requièrent que le domaine du serveur approuve le domaine du client. En d’autres termes, le domaine du serveur est pointé sur le domaine du client.

### Prise en charge du client MBAM pour les disques durs chiffrés

MBAM prend en charge BitLocker sur les disques durs chiffrés qui satisfont les exigences de spécification TCG pour Opal ainsi que les normes IEEE 1667. Lorsque BitLocker est activé sur ces appareils, il génère des clés et effectue des tâches de gestion sur le lecteur chiffré. Pour plus d’informations, voir [disque dur chiffré](https://technet.microsoft.com/library/hh831627.aspx) .

## Obtention de technologies MDOP


MBAM fait partie du pack d’optimisation du bureau Microsoft (MDOP). MDOP fait partie du programme Microsoft Software Assurance. Pour plus d’informations sur le programme Microsoft Software Assurance et sur l’acquisition de MDOP, voir [Comment obtenir MDOP?](https://go.microsoft.com/fwlink/?LinkId=322049).

## <a href="" id="---------mbam-2-5-release-notes"></a> Notes de publication de MBAM 2,5


Pour plus d’informations et des informations de dernière minute qui ne sont pas incluses dans cette documentation, voir [notes de publication pour MBAM 2,5](release-notes-for-mbam-25.md).

## Vous avez une suggestion pour MBAM?
- Envoyez-nous vos commentaires [ici](https://support.microsoft.com/help/4021566/windows-10-send-feedback-to-microsoft-with-feedback-hub). 
- Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).

## Rubriques connexes


[Microsoft BitLocker Administration and Monitoring2.5](index.md)

[Prise en main de MBAM2.5](getting-started-with-mbam-25.md)

 

 





