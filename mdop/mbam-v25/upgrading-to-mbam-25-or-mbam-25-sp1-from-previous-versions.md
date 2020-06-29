---
title: Mise à niveau vers MBAM2.5 ou MBAM2.5 SP1 àpartir de versions antérieures
description: Mise à niveau vers MBAM2.5 ou MBAM2.5 SP1 àpartir de versions antérieures
author: dansimp
ms.assetid: a9edb4b8-5d5e-42ab-8db6-619db2878e50
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 07a03ebbbfce45f7f69a85000e18ddf1a58e53ad
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804464"
---
# Mise à niveau vers MBAM2.5 ou MBAM2.5 SP1 àpartir de versions antérieures


Cette rubrique décrit la procédure de mise à niveau du serveur d’administration et de surveillance Microsoft BitLocker (MBAM) et du client MBAM à partir des versions précédentes de MBAM.

**Remarques**  Vous pouvez effectuer une mise à niveau directement vers MBAM 2,5 ou MBAM 2,5 SP1 à partir de n’importe quelle version précédente d’MBAM.

 

## Avant de commencer la mise à niveau


Passez en revue les informations suivantes avant de commencer la mise à niveau.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Ce que vous devez savoir avant de commencer</th>
<th align="left">Détails</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Si vous installez les sites Web MBAM sur un serveur et les services Web sur un autre serveur, vous devez utiliser les applets de cmdlets Windows PowerShell pour les configurer.</p></td>
<td align="left"><p>L’Assistant Configuration du serveur MBAM ne prend pas en charge la configuration des sites Web sur un serveur et les services Web sur un autre serveur.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Si vous effectuez une mise à niveau vers MBAM 2.5 ou 2,5 SP1 à partir de MBAM 2.0 ou 2,0 SP1 dans Windows Server 2008 R2:</p>
<p>Le site Web d’administration et de contrôle, le portail libre-service ne fonctionnera pas si vous installez le logiciel .NET Framework 4.5 requis après l’installation d’Internet Information Services (IIS).</p>
<p>Ce problème survient parce que ASP.NET ne peut pas être correctement inscrit dans IIS si .NET Framework est installé après l’installation d’IIS.</p></td>
<td align="left"><p><strong>Pour résoudre ce problème:</strong></p>
<p>Exécutez <strong> aspnet_regiis, </strong> à partir de l’emplacement suivant:</p>
<p>C:\windows\microsoft.net\Framework\v4.0.30319</p>
<p>Pour plus d’informations, reportez-vous à la rubrique: <a href="https://go.microsoft.com/fwlink/?LinkId=393272" data-raw-source="[ASP.NET IIS Registration Tool](https://go.microsoft.com/fwlink/?LinkId=393272)"> ASP.net de l’outil d’inscription </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Enregistrez un SPN sur le compte du pool d’applications si toutes les conditions suivantes sont vraies:</p>
<ul>
<li><p>Vous effectuez une mise à niveau à partir d’une version précédente de MBAM.</p></li>
<li><p>Pour le moment, vous n’utilisez pas le site Web MBAM dans une configuration à charge équilibrée ou distribuée, mais vous aimeriez le faire lorsque vous effectuez une mise à niveau vers MBAM 2.5 ou 2,5 SP1.</p></li>
</ul></td>
<td align="left"><p>Pour obtenir des instructions, voir <a href="planning-how-to-secure-the-mbam-websites.md#bkmk-registerspn" data-raw-source="[Planning How to Secure the MBAM Websites](planning-how-to-secure-the-mbam-websites.md#bkmk-registerspn)"> planification de la sécurisation des sites Web MBAM </a> .</p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Ce que nous recommandons</strong></p></td>
<td align="left"><p>Enregistrez un nom de principal de service (SPN) pour le compte du pool d’applications, même si vous disposez déjà de SPN enregistrés pour le compte d’ordinateur.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Pourquoi nous le recommandons</strong></p></td>
<td align="left"><p>Il est nécessaire de procéder à l’inscription d’un SPN sur le compte du pool d’applications pour configurer les sites Web dans une configuration distribuée ou dont le chargement est équilibré.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Que se passe-t-il si le SPN est déjà configuré sur un compte d’ordinateur?</strong></p></td>
<td align="left"><p>MBAM utilisera les SPN que vous avez déjà inscrits et vous n’avez pas besoin de configurer des SPN supplémentaires, mais vous n’êtes pas en mesure de configurer les sites Web dans une configuration à charge équilibrée ou distribuée.</p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>

 

## Procédure de mise à niveau de l’infrastructure du serveur MBAM


Suivez les étapes décrites dans les sections suivantes pour mettre à niveau MBAM pour la topologie autonome ou la topologie d’intégration de System Center Configuration Manager.

**Pour mettre à niveau l’infrastructure du serveur MBAM pour une topologie autonome**

1.  Désinstallez les versions précédentes de MBAM à partir de **programmes et fonctionnalités** , et de serveurs Web pour vous assurer que les informations ne sont pas écrites à partir des clients MBAM vers l’infrastructure MBAM. Pour obtenir des instructions, voir [suppression des fonctionnalités ou logiciels du serveur MBAM](removing-mbam-server-features-or-software.md#bkmk-removeserverfeatures).

2.  Sauvegardez vos bases de données.

3.  Désinstallez les versions précédentes de MBAM à partir de SQL Server à l’aide de **programmes et fonctionnalités**, y compris SQL Server hébergeant les rapports MBAM via SQL Server Reporting Services. Supprimez tous les fichiers ou dossiers temporaires du serveur MBAM du serveur de base de données et de Reporting Services.

    **Remarques**  Les bases de données ne seront pas supprimées, et toutes les données de conformité et de récupération sont conservées dans la base de données.

     

4.  Installez et configurez les bases de données, rapports et applications Web MBAM 2.5 ou 2,5 SP1 dans cet ordre. Les bases de données sont mises à niveau en place.

5.  Mettez à jour les objets de stratégie de groupe à l’aide des modèles MBAM 2,5 pour tirer parti des nouvelles fonctionnalités de MBAM, telles que le chiffrement appliqué. Si vous ne mettez pas à jour les objets de stratégie de groupe et le client MBAM sur MBAM 2,5, les versions antérieures de clients MBAM continuent de créer des rapports sur vos objets de stratégie de groupe actuels avec des fonctionnalités réduites. Découvrez [Comment obtenir des modèles de stratégie de groupe MDOP (. admx)](https://www.microsoft.com/download/details.aspx?id=41183) pour télécharger les derniers modèles ADMX.

    Après avoir effectué la mise à niveau de l’infrastructure du serveur MBAM, les ordinateurs clients existants continuent de rapporter au serveur MBAM 2.5 ou 2,5 SP1, et les données de récupération continuent d’être stockées.

6.  Installez la dernière version de MBAM ou du client 2,5 SP1. Il n’est pas nécessaire de redémarrer les ordinateurs clients après le déploiement.

**Pour mettre à niveau la topologie d’intégration de l’infrastructure MBAM pour System Center Configuration Manager**

1.  Désinstallez les versions précédentes de MBAM à partir de **programmes et fonctionnalités** , et de serveurs Web pour vous assurer que les informations ne sont pas écrites à partir des clients MBAM vers l’infrastructure MBAM. Pour obtenir des instructions, voir [suppression des fonctionnalités ou logiciels du serveur MBAM](removing-mbam-server-features-or-software.md#bkmk-removeserverfeatures).

2.  Sauvegardez vos bases de données.

3.  Désinstallez les versions précédentes de MBAM à partir de SQL Server à l’aide de **programmes et fonctionnalités**, y compris SQL Server hébergeant les rapports MBAM via SQL Server Reporting Services. Supprimez tous les fichiers ou dossiers temporaires du serveur MBAM du serveur de base de données et de Reporting Services.

4.  Désinstaller MBAM à partir du serveur Configuration Manager.

    **Remarques**  Les bases de données et les objets de Configuration Manager (Planning de référence, collection d’ordinateurs pris en charge par MBAM et rapports) ne seront pas supprimés, et toutes les données de conformité et de récupération sont conservées dans la base de données.

     

5.  Mettez à jour les fichiers. mof.

6.  Installez et configurez les bases de données, rapports, applications Web et intégration du gestionnaire de configuration MBAM 2.5 ou 2,5 SP1 dans cet ordre. Les bases de données et les objets gestionnaires de configuration sont mis à niveau en place.

7.  Vous pouvez également mettre à jour les objets de stratégie de groupe (GPO) et modifier les paramètres si vous voulez implémenter de nouvelles fonctionnalités dans MBAM, par exemple un chiffrement appliqué. Si vous ne mettez pas à jour les objets de stratégie de groupe, MBAM continuera à créer des rapports sur vos objets de stratégie de groupe actuels. Découvrez [Comment obtenir des modèles de stratégie de groupe MDOP (. admx)](https://docs.microsoft.com/microsoft-desktop-optimization-pack/solutions/how-to-download-and-deploy-mdop-group-policy--admx--templates) pour télécharger les derniers modèles ADMX.

    Après avoir effectué la mise à niveau de l’infrastructure du serveur MBAM, les ordinateurs clients existants continuent de rapporter au serveur MBAM 2.5 ou 2,5 SP1, et les données de récupération continuent d’être stockées.

8.  Installez la dernière version de MBAM ou du client 2,5 SP1. Il n’est pas nécessaire de redémarrer les ordinateurs clients après le déploiement.

## Prise en charge de la mise à niveau du client MBAM


MBAM prend en charge les mises à jour du client MBAM 2.5 à partir de n’importe quelle version antérieure du client MBAM.

**Procédures d’installation du client MBAM:**

-   Mettez à niveau les ordinateurs exécutant le client MBAM en une seule fois ou progressivement après l’installation de l’infrastructure du serveur MBAM 2.5.

-   Installez le client MBAM par le biais d’un système de distribution de logiciels électronique ou via des outils tels que Active Directory Domain Services ou System Center Configuration Manager.



## Rubriques connexes


[Déploiement de MBAM2.5](deploying-mbam-25.md)

[Déploiement du client MBAM2.5](deploying-the-mbam-25-client.md)

[Configuration des composants du serveur MBAM2.5](configuring-the-mbam-25-server-features.md)

 

## Vous avez une suggestion pour MBAM?
- Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)
- Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





