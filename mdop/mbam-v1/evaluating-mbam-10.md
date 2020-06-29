---
title: Évaluation de MBAM1.0
description: Évaluation de MBAM1.0
author: dansimp
ms.assetid: a1e2b674-eda9-4e1c-9b4c-e748470c71f2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: f09b06af52f5738fd50bfe727987b760d98552d9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811045"
---
# Évaluation de MBAM1.0


Avant de déployer l’administration et la surveillance Microsoft BitLocker (MBAM) dans un environnement de production, vous devez l’évaluer dans un environnement de laboratoire. Vous pouvez utiliser les informations fournies dans cette rubrique pour configurer MBAM dans un seul environnement Lab serveur à des fins d’évaluation.

Bien que les étapes du déploiement réel soient très similaires au scénario décrit dans [la rubrique Comment installer et configurer MBAM sur un seul serveur](how-to-install-and-configure-mbam-on-a-single-server-mbam-1.md), cette rubrique contient des informations supplémentaires pour vous permettre de configurer un environnement d’évaluation MBAM dans le moins de temps.

## Configurer l’environnement Lab


Même lorsque vous configurez une instance de MBAM qui n’est pas de production pour une évaluation dans un environnement Lab, vous devez toujours vérifier que vous avez satisfait aux conditions préalables de déploiement et à la configuration matérielle et logicielle requise. Pour plus d’informations, consultez la configuration requise pour le [déploiement d’MBAM 1,0](mbam-10-deployment-prerequisites.md) et les [Configurations prises en charge par MBAM 1,0](mbam-10-supported-configurations.md). Avant de commencer le déploiement d’évaluation d’MBAM, vous devez également consulter la [préparation de votre environnement pour MBAM 1,0](preparing-your-environment-for-mbam-10.md) .

### Planifier un déploiement d’une évaluation MBAM

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left">Tâche</th>
<th align="left">Références</th>
<th align="left">Remarques</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Passez en revue les informations de prise en main sur MBAM pour obtenir une connaissance de base du produit avant de commencer la planification du déploiement.</p></td>
<td align="left"><p><a href="getting-started-with-mbam-10.md" data-raw-source="[Getting Started with MBAM 1.0](getting-started-with-mbam-10.md)">Prise en main de MBAM1.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p></p>
<p>Préparez votre environnement informatique pour l’installation MBAM. Pour ce faire, vous devez activer le chiffrement de données transparent (TDE) sur les instances SQL Server qui hébergeront des bases de données MBAM. Pour activer TDE dans votre environnement de laboratoire, vous pouvez créer un fichier. SQL à exécuter sur la base de données maître hébergée sur l’instance de SQL Server qu’MBAM utilisera.</p>
<div class="alert">
<strong>Remarque</strong><br/><p>L’exemple suivant permet de créer un fichier. SQL pour votre environnement Lab afin d’activer rapidement TDE sur l’instance SQL Server qui héberge les bases de données MBAM. Les commandes SQL Server suivantes permettent à TDE à l’aide d’un certificat SQL Server signé en local. Assurez-vous de sauvegarder le certificat TDE et sa clé de chiffrement associée dans l’exemple de chemin de sauvegarde local de <em> C:\backup </em> . Le certificat et la clé TDE sont requis lors de la récupération de la base de données ou du déplacement du certificat et de la clé vers un autre serveur sur lequel le chiffrement TDE est activé.</p>
</div>
<div>

</div>
<pre class="syntax" space="preserve"><code>USE master;
GO
CREATE MASTER KEY ENCRYPTION BY PASSWORD = &#39;P@55w0rd&#39;;
GO
CREATE CERTIFICATE tdeCert WITH SUBJECT = &#39;TDE Certificate&#39;;
GO
BACKUP CERTIFICATE tdeCert TO FILE = &#39;C:\Backup\TDECertificate.cer&#39;
   WITH PRIVATE KEY (
         FILE = &#39;C:\Backup\TDECertificateKey.pvk&#39;,
         ENCRYPTION BY PASSWORD = &#39;P@55w0rd&#39;);
GO</code></pre></td>
<td align="left"><p><a href="mbam-10-deployment-prerequisites.md" data-raw-source="[MBAM 1.0 Deployment Prerequisites](mbam-10-deployment-prerequisites.md)">Conditions préalables au déploiement de MBAM1.0</a></p>
<p><a href="https://go.microsoft.com/fwlink/?LinkId=269703" data-raw-source="[Database Encryption in SQL Server 2008 Enterprise Edition](https://go.microsoft.com/fwlink/?LinkId=269703)">Chiffrement de base de données dans SQL Server 2008 Enterprise Edition</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Planifiez et configurez les exigences de stratégie de groupe MBAM.</p></td>
<td align="left"><p><a href="planning-for-mbam-10-group-policy-requirements.md" data-raw-source="[Planning for MBAM 1.0 Group Policy Requirements](planning-for-mbam-10-group-policy-requirements.md)">Planification des exigences en matière de stratégie de groupe MBAM1.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Planifiez et créez les groupes de sécurité de services de domaine Active Directory nécessaires et planifiez les exigences d’appartenance au groupe de sécurité local MBAM.</p></td>
<td align="left"><p><a href="planning-for-mbam-10-administrator-roles.md" data-raw-source="[Planning for MBAM 1.0 Administrator Roles](planning-for-mbam-10-administrator-roles.md)">Planification des rôles administrateur de MBAM1.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Planifier le déploiement de fonctionnalités de MBAM Server.</p></td>
<td align="left"><p><a href="planning-for-mbam-10-server-deployment.md" data-raw-source="[Planning for MBAM 1.0 Server Deployment](planning-for-mbam-10-server-deployment.md)">Planification du déploiement de serveursMBAM1.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Planifier le déploiement du client MBAM.</p></td>
<td align="left"><p><a href="planning-for-mbam-10-client-deployment.md" data-raw-source="[Planning for MBAM 1.0 Client Deployment](planning-for-mbam-10-client-deployment.md)">Planification du déploiement de clients MBAM1.0</a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



### Effectuer un déploiement d’évaluation MBAM

Après avoir effectué les installations de planification et de pré-installation requises pour préparer votre environnement informatique pour une installation MBAM, vous pouvez commencer le déploiement d’évaluation d’MBAM.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Passez en revue les informations de configurations prises en charge par MBAM pour vous assurer que les ordinateurs client et serveur sélectionnés sont pris en charge pour l’installation de la fonctionnalité MBAM.</p></td>
<td align="left"><p><a href="mbam-10-supported-configurations.md" data-raw-source="[MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md)">Configurations prises en charge par MBAM1.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Exécutez le programme d’installation de MBAM pour déployer les fonctionnalités serveur MBAM sur un serveur unique à des fins d’évaluation.</p></td>
<td align="left"><p><a href="how-to-install-and-configure-mbam-on-a-single-server-mbam-1.md" data-raw-source="[How to Install and Configure MBAM on a Single Server](how-to-install-and-configure-mbam-on-a-single-server-mbam-1.md)">Installation et configuration de MBAM sur un seul serveur</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Ajoutez les groupes de sécurité des services de domaine Active Directory (AD FS) que vous avez créés lors de la phase de planification aux groupes locaux du serveur MBAM local approprié sur le nouveau serveur MBAM.</p></td>
<td align="left"><p><a href="planning-for-mbam-10-administrator-roles.md" data-raw-source="[Planning for MBAM 1.0 Administrator Roles](planning-for-mbam-10-administrator-roles.md)">Planification des rôles d’administrateur MBAM 1,0 </a> et <a href="how-to-manage-mbam-administrator-roles-mbam-1.md" data-raw-source="[How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-1.md)"> Comment gérer les rôles d’administrateur MBAM</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Créez et déployez les objets de stratégie de groupe MBAM requis.</p></td>
<td align="left"><p><a href="deploying-mbam-10-group-policy-objects.md" data-raw-source="[Deploying MBAM 1.0 Group Policy Objects](deploying-mbam-10-group-policy-objects.md)">Déploiement d'objets de stratégie de groupe MBAM1.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Déployez le logiciel client MBAM.</p></td>
<td align="left"><p><a href="deploying-the-mbam-10-client.md" data-raw-source="[Deploying the MBAM 1.0 Client](deploying-the-mbam-10-client.md)">Déploiement du client MBAM1.0</a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



## Configurer les ordinateurs de laboratoire pour l’évaluation de MBAM


Vous pouvez modifier les paramètres de fréquence des rapports d’État du client MBAM à l’aide de l’éditeur du Registre. Toutefois, ces modifications doivent être utilisées uniquement à des fins de test.

**Warning**  
Cette rubrique explique comment modifier le Registre Windows à l’aide de l’éditeur du Registre. Si vous modifiez la clé de registre de Windows de manière incorrecte, vous pouvez être à l’origine de problèmes importants qui peuvent nécessiter la réinstallation de Windows. Vous devez faire une copie de sauvegarde des fichiers du Registre (System. dat et User. dat) avant de modifier le registre. Microsoft ne peut pas garantir que les problèmes qui peuvent survenir lorsque vous modifiez le registre peuvent être résolus. Changez de Registre à vos propres risques.



### <a href="" id="modify-the-frequency-settings-on-mbam-client-status-reporting-"></a>Modifier les paramètres de fréquence des rapports d’État du client MBAM

Les fréquences de rapport d’État et de réveil du client MBAM ont une valeur minimale de 90 minutes lorsqu’elles sont configurées pour utiliser une stratégie de groupe. Vous pouvez modifier ces fréquences sur les ordinateurs clients MBAM en modifiant le Registre Windows sur valeurs inférieures, ce qui permet d’accélérer les tests. Pour modifier les paramètres de fréquence de création de rapports de l’état du client MBAM, utilisez un éditeur du Registre pour accéder à **HKLM\\Software\\Policies\\FVE\\MDOPBitLockerManagement**, modifiez les valeurs pour **ClientWakeupFrequency** et **StatusReportingFrequency** sur **1** comme valeur minimale prise en charge du client, puis redémarrez le service client de gestion BitLocker. Lorsque vous effectuez cette modification, le client MBAM rapporte chaque minute. Vous pouvez définir des valeurs dont la valeur est faible uniquement lorsque vous effectuez cette opération manuellement dans le registre.

### <a href="" id="modify-the-startup-delay-on-mbam-client-service-"></a>Modifier le délai de démarrage sur le service client MBAM

En plus des fréquences de création de rapports d’État et de réveil du client MBAM, il existe un délai aléatoire de maximum de 90 minutes lorsque le service d’agent client MBAM démarre sur les ordinateurs clients. Si vous ne souhaitez pas utiliser le délai aléatoire, créez une valeur **DWORD** de **NoStartupDelay** sous **HKLM\\Software\\Microsoft\\MBAM**, définissez sa valeur sur **1**, puis redémarrez le service client de gestion BitLocker.

## Rubriques connexes


[Prise en main de MBAM1.0](getting-started-with-mbam-10.md)









