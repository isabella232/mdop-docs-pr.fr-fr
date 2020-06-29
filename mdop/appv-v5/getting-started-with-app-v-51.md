---
title: Prise en main de l'application App-V5.1
description: Prise en main de l'application App-V5.1
author: dansimp
ms.assetid: 49a20e1f-0566-4e53-a417-1521393fc974
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ff10f12bc672a24f2837f50bfb1f0033ede3e46f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805809"
---
# Prise en main de l'application App-V5.1


Microsoft Application Virtualization (App-V) 5,1 permet aux administrateurs de déployer, de mettre à jour et de prendre en charge des applications en temps réel, en fonction de vos besoins. Les applications individuelles sont transformées à partir de produits installés en local en services gérés de manière centralisée et sont disponibles où vous le souhaitez, sans que vous ayez besoin de préconfigurer des ordinateurs ou de modifier les paramètres du système d’exploitation.

App-V se compose des éléments suivants:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Élément</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Serveur de gestion App-V</p></td>
<td align="left"><ul>
<li><p>Fournit un emplacement central pour la gestion de l’infrastructure App-V, qui offre des applications virtuelles au client de bureau App-V et au client de services Bureau à distance (anciennement services Terminal Server).</p></li>
<li><p>Utilise Microsoft SQL Server® pour le magasin de données, dans lequel un ou plusieurs serveurs d’administration d’applications-V peuvent partager un seul magasin de données SQL Server.</p></li>
<li><p>Authentifie les demandes et assure la sécurité, la mesure, la surveillance et la collecte des données. Le serveur utilise Active Directory et des outils de support pour gérer les utilisateurs et les applications.</p></li>
<li><p>Dispose d’un site de gestion qui vous permet de configurer l’infrastructure App-V sur n’importe quel ordinateur. Vous pouvez ajouter et supprimer des applications, manipuler des raccourcis, attribuer des autorisations d’accès à des utilisateurs et des groupes, et créer des groupes de connexion.</p></li>
<li><p>Autorise la communication entre la console de gestion Web App-V et le magasin de données SQL Server. Ces composants peuvent tous être installés sur un ordinateur serveur unique ou sur un ou plusieurs ordinateurs séparés, en fonction de l’architecture système requise.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Serveur de publication App-V</p></td>
<td align="left"><ul>
<li><p>Fournit aux clients App-V des applications d’habilitation pour un utilisateur spécifique</p></li>
<li><p>Héberge le package d’application virtuel pour le streaming.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Client de bureau App-V</p></td>
<td align="left"><ul>
<li><p>Récupère les applications virtuelles</p></li>
<li><p>Publie les applications sur les clients.</p></li>
<li><p>Configure et gère automatiquement les environnements virtuels lors de l’exécution sur les points de terminaison Windows.</p></li>
<li><p>Stocke des paramètres d’application virtuelle spécifiques à l’utilisateur, tels que des modifications de Registre et de fichier, dans chaque profil utilisateur&#39;s.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Client App-V Remote Desktop Services (RDS)</p></td>
<td align="left"><p>Permet aux serveurs hôtes de session Bureau à distance d’utiliser les fonctionnalités du client de bureau App-V pour les sessions de bureau partagées.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Séquenceur App-V</p></td>
<td align="left"><ul>
<li><p>Est un outil qui permet de transformer des applications traditionnelles en applications virtuelles.</p></li>
<li><p>Produit l’application «package», qui se compose des éléments suivants:</p>
<ol>
<li><p>fichier de l’application séquencé (APPV)</p></li>
<li><p>fichier Windows Installer (MSI) qui peut être déployé sur des clients configurés pour une opération autonome</p></li>
<li><p>Plusieurs fichiers XML, dont Report.XML, PackageName_DeploymentConfig.XML et PackageName_UserConfig.XML. Les fichiers XML UserConfig et DeploymentConfig permettent de configurer des modifications personnalisées du comportement par défaut du package.</p></li>
</ol></li>
</ul></td>
</tr>
</tbody>
</table>

 

Pour plus d’informations sur ces éléments, voir [architecture de haut niveau pour App-V 5,1](high-level-architecture-for-app-v-51.md).

Si vous débutez avec ce produit, nous vous conseillons de lire entièrement la documentation. Avant de déployer celle-ci dans un environnement de production, nous vous conseillons également de valider votre plan de déploiement dans un environnement réseau de test. Vous pouvez également envisager de prendre un cours sur les technologies pertinentes. Pour plus d’informations sur les opportunités de formation Microsoft, voir la présentation de la formation Microsoft à l’adresse <https://go.microsoft.com/fwlink/p/?LinkId=80347> .

**Remarques**  La version téléchargeable du Guide de l’administrateur n’est pas disponible. En revanche, vous pouvez en savoir plus sur un mode spécial de la bibliothèque TechNet qui vous permet de sélectionner des articles, de les regrouper dans une collection et de les imprimer ou de les exporter vers un fichier à partir de <https://go.microsoft.com/fwlink/?LinkId=272491> ( https://go.microsoft.com/fwlink/?LinkId=272491) .

 

Cette section du Guide de l’administrateur d’application-V 5,1 inclut des informations de haut niveau sur App-V 5,1 pour vous offrir une connaissance de base du produit avant de commencer la planification du déploiement.

## Commencer à utiliser App-V 5,1


-   [À propos d'App-V5.1](about-app-v-51.md)

    Fournit une vue d’ensemble détaillée de App-V 5,1 et de la manière dont il peut être utilisé au sein de votre organisation.

-   [Évaluation d'App-V5.1](evaluating-app-v-51.md)

    Fournit des informations sur la façon dont vous pouvez optimiser l’utilisation de App-V 5,1 au sein de votre organisation.

-   [Architecture de haut niveau pour App-V5.1](high-level-architecture-for-app-v-51.md)

    Décrit les fonctionnalités de 5,1 App-V et la façon dont elles fonctionnent ensemble.

-   [Accessibilité d'App-V5.1](accessibility-for-app-v-51.md)

    Fournit des informations sur les fonctionnalités et les services qui rendent ce produit et sa documentation correspondante plus accessibles aux personnes atteintes de handicaps.

## <a href="" id="other-resources-for-this-product-"></a>Autres ressources pour ce produit


-   [Guide de l’administrateur de Microsoft Application Virtualization 5,1](microsoft-application-virtualization-51-administrators-guide.md)

-   [Planification d'App-V5.1](planning-for-app-v-51.md)

-   [Déploiement d'App-V5.1](deploying-app-v-51.md)

-   [Opérations d'App-V5.1](operations-for-app-v-51.md)

-   [Résolution de problèmes d'App-V5.1](troubleshooting-app-v-51.md)

-   [Référence technique pour App-V5.1](technical-reference-for-app-v-51.md)






 

 





