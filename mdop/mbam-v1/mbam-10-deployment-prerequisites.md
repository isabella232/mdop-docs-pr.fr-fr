---
title: Conditions préalables au déploiement de MBAM1.0
description: Conditions préalables au déploiement de MBAM1.0
author: dansimp
ms.assetid: bd9e1010-7d25-43e7-8dc6-b521226a659d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6ed14343d37a859364bcabbe6ca72c041502a23c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809491"
---
# Conditions préalables au déploiement de MBAM1.0


Avant de commencer la configuration de l’administration et de la surveillance de BitLocker (MBAM) Microsoft, assurez-vous que vous remplissez les conditions préalables nécessaires pour installer le produit. Cette section contient des informations pour vous aider à préparer votre environnement informatique avant de déployer les clients MBAM et les fonctionnalités du serveur.

## Conditions préalables à l’installation pour les fonctionnalités du serveur MBAM


Chacune des fonctionnalités du serveur MBAM possède des éléments requis spécifiques qui doivent être satisfaits pour pouvoir être installés correctement. La configuration de MBAM vérifie si toutes les conditions préalables sont remplies avant le démarrage de l’installation.

### Conditions préalables à l’installation du serveur d’administration et de surveillance

Le tableau suivant répertorie les conditions préalables à l’installation du serveur d’administration et de surveillance MBAM:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Prérequises</th>
<th align="left">Détails</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Rôle du serveur Windows ServerWeb</strong></p></td>
<td align="left"><p>Ce rôle doit être ajouté au système d’exploitation du serveur pris en charge pour la fonctionnalité d’administration et de contrôle du serveur MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Outils de gestion du serveur Web (IIS)</strong></p></td>
<td align="left"><p><strong>Outils et scripts de gestion IIS</strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Services de rôle de serveur Web</strong></p></td>
<td align="left"><p><strong>Fonctionnalités HTTP communes:</strong></p>
<ul>
<li><p>Contenu statique</p></li>
<li><p>Document par défaut</p></li>
</ul>
<p><strong>Développement d’applications:</strong></p>
<ul>
<li><p>ASP.NET</p></li>
<li><p>Extensibilité .NET</p></li>
<li><p>Extensions ISAPI</p></li>
<li><p>Filtres ISAPI</p></li>
</ul>
<p><strong>Sûreté</strong></p>
<ul>
<li><p>Authentification Windows</p></li>
<li><p>Filtrage de requête</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Fonctionnalités de Windows Server</strong></p></td>
<td align="left"><p><strong>Fonctionnalités de Microsoft .NET Framework 3.5.1:</strong></p>
<ul>
<li><p>.NET Framework 3.5.1</p></li>
<li><p>Activation WCF</p>
<ul>
<li><p>Activation HTTP</p></li>
<li><p>Activation non HTTP</p></li>
</ul></li>
</ul>
<p><strong>Service d'activation des processus Windows</strong></p>
<ul>
<li><p>Modèle de processus</p></li>
<li><p>Environnement .NET</p></li>
<li><p>API de configuration</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

**Remarques**  Pour obtenir la liste des systèmes d’exploitation pris en charge, voir [Configurations prises en charge par MBAM 1,0](mbam-10-supported-configurations.md).

 

### Conditions préalables à l’installation des rapports de conformité et d’audit

Les rapports de conformité et d’audit doivent être installés sur une version prise en charge de SQLServer. Les conditions préalables à l’installation de cette fonctionnalité incluent SQL Server Reporting Services (SSRS).

SSRS doit être installé et exécuté lors de l’installation de MBAM Server. SSRS doit également être configuré en mode «natif», pas dans le mode «non configuré» ou «SharePoint».

**Remarques**  Pour obtenir la liste des systèmes d’exploitation et versions SQLServer pris en charge, voir [Configurations prises en charge par MBAM 1,0](mbam-10-supported-configurations.md).

 

### Conditions préalables à l’installation de la base de données de récupération et de matériel

La base de données de récupération et de matériel doit être installée sur une version prise en charge de SQLServer.

Les services du moteur de base de données SQL Server doivent être installés et exécutés pendant l’installation du serveur MBAM. La fonction de chiffrement de données (TDE) doit être activée.

**Remarques**  Pour obtenir la liste des systèmes d’exploitation et versions SQLServer pris en charge, voir [Configurations prises en charge par MBAM 1,0](mbam-10-supported-configurations.md).

 

La fonctionnalité SQLServer TDE permet d’effectuer le chiffrement et le déchiffrement des données et des fichiers journaux en temps réel. TDE protège les données «au repos», qui incluent les données et les fichiers journaux. Elle offre la possibilité de se conformer à de nombreuses lois, règlements et recommandations définis dans divers secteurs.

**Remarques**  Dans la mesure où TDE effectue le déchiffrement en temps réel des informations de la base de données, les informations de la clé de récupération seront visibles si le compte sous lequel vous vous êtes connecté dispose des autorisations de la base de données lorsque vous affichez les tables SQL informations clés de récupération.

 

### Conditions préalables à l’installation de la base de données de conformité et d’audit

La base de données d’audit et de conformité doit être installée sur une version prise en charge de SQLServer.

Les services du moteur de base de données SQL Server doivent être installés et exécutés lors de l’installation de MBAM Server.

**Remarques**  Pour obtenir la liste des systèmes d’exploitation et versions SQLServer pris en charge, voir [Configurations prises en charge par MBAM 1,0](mbam-10-supported-configurations.md).

 

## Conditions préalables à l’installation pour les clients MBAM


Pour pouvoir commencer l’installation du client MBAM, vous devez disposer des éléments suivants:

-   Fonctionnalité du module de plateforme sécurisée (TPM) v 1.2

-   Le processeur du TPM doit être activé dans le BIOS et il doit être Resettable du système d’exploitation. Pour plus d’informations, consultez la documentation relative au BIOS.

**Avertissement**  Assurez-vous que le clavier, la souris et la vidéo sont directement connectés à l’ordinateur au lieu d’un clavier, d’une vidéo et d’un commutateur de souris (KVM). Un commutateur KVM peut interférer avec la capacité de l’ordinateur à détecter la présence physique du matériel.

 

## Rubriques connexes


[Planification du déploiement de MBAM1.0](planning-to-deploy-mbam-10.md)

[Configurations prises en charge par MBAM1.0](mbam-10-supported-configurations.md)

 

 





