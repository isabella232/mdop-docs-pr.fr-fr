---
title: Planification de la capacité d'App-V5.1
description: Planification de la capacité d'App-V5.1
author: dansimp
ms.assetid: 7a98062f-5a60-49d6-ab40-dc6057e1dd5a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b152536b3c61e47f3fda84489b1e102c285e01c6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805988"
---
# Planification de la capacité d'App-V5.1


Les recommandations suivantes peuvent être utilisées comme planning de référence afin de vous aider à déterminer les informations de planification appropriées pour l’infrastructure App-V 5,1 de votre organisation.

**Important**  Utilisez les informations de cette section uniquement en tant que guide général pour la planification de votre déploiement d’application-V 5,1. La capacité requise de votre système dépend des détails spécifiques de votre matériel et de votre environnement applicatif. Par ailleurs, les numéros de performance indiqués dans ce document sont des exemples et vos résultats peuvent varier.

 

## Déterminez l’objectif du projet


Avant de concevoir l’infrastructure App-V 5,1, vous devez déterminer l’étendue du projet. L’étendue consiste à déterminer les applications qui seront disponibles virtuellement et à identifier les utilisateurs cibles et leurs emplacements. Ces informations vous aideront à déterminer le type d’infrastructure App-V 5,1 à implémenter. Les décisions relatives à l’étendue du projet doivent être basées sur les besoins spécifiques de votre organisation.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tâche</th>
<th align="left">Plus d’informations</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Déterminer l’étendue de l’application</p></td>
<td align="left"><p>En fonction des applications à virtualiser, l’infrastructure App-V 5,1 peut être définie de différentes manières. La première tâche consiste à définir les applications que vous voulez virtualiser.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Déterminer l’étendue de l’emplacement</p></td>
<td align="left"><p>Le champ étendue de l’emplacement fait référence aux emplacements physiques (par exemple, à l’échelle de l’entreprise ou à un emplacement géographique spécifique) sur lequel vous envisagez d’exécuter les applications virtualisées. Elle peut également faire référence à la population des utilisateurs (par exemple, un service unique) qui exécuteront les applications virtuelles. Vous devriez obtenir une carte réseau qui inclut les chemins de connexion ainsi que la bande passante disponible vers chaque emplacement et le nombre d’utilisateurs qui utilisent des applications virtualisées et la vitesse de liaison du réseau étendu.</p></td>
</tr>
</tbody>
</table>

 

## Déterminer l’infrastructure App-V 5,1 requise


**Important**  Les deux modèles suivants requièrent que le client App-V 5,1 soit installé sur l’ordinateur sur lequel vous envisagez d’exécuter des applications virtuelles.

Vous pouvez également gérer votre environnement App-V 5,1 à l’aide d’une solution de distribution de logiciels électronique (ESD) telle que Microsoft Systems Center Configuration Manager. Pour plus d’informations, reportez-vous [au déploiement de packages d’application V 5,1 à l’aide de la distribution de logiciels électroniques](how-to-deploy-app-v-51-packages-using-electronic-software-distribution.md).

 

-   **Modèle autonome** -le modèle autonome permet aux applications virtuelles d’être activées pour la distribution sans streaming. App-V 5,1 en mode autonome se compose du Sequencer et du client; aucun composant supplémentaire n’est requis. Les applications sont prêtes pour la virtualisation grâce à un processus appelé séquençage. Pour plus d’informations, reportez-vous [à la section planification du déploiement d’App-V 5,1 et du déploiement du client](planning-for-the-app-v-51-sequencer-and-client-deployment.md). Le modèle autonome est recommandé dans les cas suivants:

    -   Utilisateurs distants distants qui ne peuvent pas se connecter à l’infrastructure App-V 5,1.

    -   Lorsque vous exécutez un système de gestion de logiciels, tel que Configuration Manager 2012.

    -   Lorsque les limitations de bande passante réseau empêchent la distribution de logiciels électroniques.

-   **Modèle d’infrastructure complète** -le modèle d’infrastructure complet fournit des fonctionnalités de distribution de logiciels, de gestion et de création de rapports. Il inclut également la diffusion en continu d’applications sur le réseau. Le modèle d’infrastructure complète App-V 5,1 comporte un ou plusieurs serveurs de gestion de l’application-V 5,1. Le serveur de gestion peut être utilisé pour publier des applications sur tous les clients. Le processus de publication place les icônes et raccourcis des applications virtuelles sur l’ordinateur cible. Il peut également diffuser des applications aux utilisateurs locaux. Pour plus d’informations sur l’installation du serveur de gestion, voir [planification du déploiement de l’application-V 5,1 Server](planning-for-the-app-v-51-server-deployment.md). Le modèle d’infrastructure complète est recommandé dans les cas suivants:

    **Important**  Le modèle d’infrastructure complète App-V 5,1 nécessite Microsoft SQL Server pour stocker des données de configuration. Pour plus d’informations, voir [Configurations prises en charge par App-V 5,1](app-v-51-supported-configurations.md).

     

    -   Lorsque vous souhaitez utiliser le serveur de gestion pour publier l’application sur des ordinateurs cibles.

    -   Pour la mise en service rapide des applications sur les ordinateurs cibles.

    -   Lorsque vous souhaitez utiliser la création de rapports App-V 5,1.

## Recommandations en matière de dimensionnement de serveur bout en bout


La section suivante fournit des informations sur la planification et le dimensionnement d’une application 5,1 de bout en bout. Pour plus d’informations, reportez-vous aux sections suivantes.

**Remarques**  Le temps de réponse en boucle sur le client correspond au temps écoulé par l’ordinateur exécutant le client App-V 5,1 pour recevoir une notification réussie du serveur de publication. Le temps de réponse en boucle sur le serveur de publication est le temps pris par l’ordinateur exécutant le serveur de publication pour recevoir une mise à jour de métadonnées de package réussie du serveur de gestion.

 

-   les clients 20 000 peuvent cibler un serveur de publication unique pour obtenir les actualisations du package pendant une durée de boucle acceptable. ( &lt; 3 secondes)

-   Un serveur de gestion unique peut prendre en charge jusqu’à 50 serveurs de publication pour les mises à jour de package de métadonnées pendant une durée de boucle acceptable. ( &lt; 5 secondes)

## <a href="" id="---------app-v-5-1-management-server-capacity-planning-recommendations"></a> Recommandations en matière de planification de la capacité du serveur de gestion d’application V 5,1


Les serveurs de publication App-V 5,1 nécessitent le serveur de gestion des demandes d’actualisation de package et des réponses d’actualisation de package. Le serveur de gestion envoie alors les informations à la base de données de gestion pour récupérer des informations. Pour plus d’informations sur les configurations prises en charge par App-V 5,1 Management Server, voir [Configurations prises en charge par app-v 5,1](app-v-51-supported-configurations.md).

**Remarques**  Le délai d’actualisation par défaut dans le serveur de publication 5,1 App-V est de 10 minutes.

 

Lorsque plusieurs serveurs de publication simultanés contactent un serveur de gestion unique pour les actualisations des métadonnées du package, les trois facteurs suivants influencent le temps de réponse en boucle sur le serveur de publication:

1.  Nombre de serveurs de publication effectuant des demandes simultanées.

2.  Nombre de groupes de connexion configurés sur le serveur de gestion.

3.  Nombre de groupes d’accès configurés sur le serveur de gestion.

Le tableau suivant fournit des informations supplémentaires sur chaque facteur ayant un impact sur la durée de l’aller-retour.

**Remarques**  Le temps de réponse aller-retour est le temps écoulé par l’ordinateur exécutant le serveur de publication 5,1 App-V pour recevoir une mise à jour de package réussie du serveur de gestion.

 

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Facteurs affectant le temps de réponse en boucle</th>
<th align="left">Plus d’informations</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Nombre de serveurs de publication demandant des mises à jour de package simultanément.</p></td>
<td align="left"><p></p>
<ul>
<li><p>Un serveur de gestion unique peut répondre à des serveurs de publication 320 demandant des métadonnées de publication simultanément.</p></li>
<li><p>Le temps de réponse aller-retour pour les serveurs de publication 320 est de 40 secondes.</p></li>
<li><p>Pour &lt; les serveurs de publication 50 demandant des métadonnées simultanément, la durée de réponse d’un aller-retour est de &lt; 5 secondes.</p></li>
<li><p>De 50 à 320, le temps de réponse augmente de façon linéaire (approximativement 2x).</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Nombre de groupes de connexion configurés sur le serveur de gestion.</p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p>Pour les groupes de connexions 100, il n’y a aucun changement notable dans le temps de réponse en boucle sur le serveur de publication.</p></li>
<li><p>Pour les groupes de connexion 100-400, il existe une augmentation linéaire mineure du temps de réponse à un aller-retour.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Nombre de groupes d’accès configurés sur le serveur de gestion.</p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p>Dans le cas d’un maximum de groupes d’accès à 40, le temps de réponse d’un aller-retour est linéaire (approximativement 3 160) sur le serveur de publication.</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

Le tableau suivant présente des exemples de valeurs pour chacun des facteurs précédents. Dans chaque variante, les packages 120 sont actualisés à partir du serveur de gestion App-V 5.1.

<table>
<colgroup>
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Scénario</th>
<th align="left">Variante</th>
<th align="left">Nombre de groupes de connexion</th>
<th align="left">Nombre de groupes d’accès</th>
<th align="left">Nombre de serveurs de publication</th>
<th align="left">Serveur de publication de type de connexion réseau/serveur de gestion</th>
<th align="left">Temps de réponse aller-retour sur le serveur de publication (en secondes)</th>
<th align="left">Utilisation de l’UC sur le serveur de gestion</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Serveurs de publication contactant simultanément le serveur de gestion pour les métadonnées de publication.</p></td>
<td align="left"><p>Nombre de serveurs de publication</p></td>
<td align="left"><p></p>
<ul>
<li><p>0,4</p></li>
<li><p>0,4</p></li>
<li><p>0,4</p></li>
<li><p>0,4</p></li>
<li><p>0,4</p></li>
<li><p>0,4</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>1</p></li>
<li><p>1</p></li>
<li><p>1</p></li>
<li><p>1</p></li>
<li><p>1</p></li>
<li><p>1</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>50</p></li>
<li><p>100</p></li>
<li><p>200</p></li>
<li><p>300</p></li>
<li><p>315</p></li>
<li><p>320</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>Réseau local</p></li>
<li><p>Réseau local</p></li>
<li><p>Réseau local</p></li>
<li><p>Réseau local</p></li>
<li><p>Réseau local</p></li>
<li><p>Réseau local</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>n°5</p></li>
<li><p>0,10</p></li>
<li><p>19,6</p></li>
<li><p>32</p></li>
<li><p>trente</p></li>
<li><p>37</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>Play</p></li>
<li><p>Play</p></li>
<li><p>Play</p></li>
<li><p>0,15</p></li>
<li><p>Play</p></li>
<li><p>0,15</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Métadonnées de publication contenant des groupes de connexion</p></td>
<td align="left"><p>Nombre de groupes de connexion</p></td>
<td align="left"><p></p>
<ul>
<li><p>0,10</p></li>
<li><p>50</p></li>
<li><p>100</p></li>
<li><p>150</p></li>
<li><p>300</p></li>
<li><p>400</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>1</p></li>
<li><p>1</p></li>
<li><p>1</p></li>
<li><p>1</p></li>
<li><p>1</p></li>
<li><p>1</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>100</p></li>
<li><p>100</p></li>
<li><p>100</p></li>
<li><p>100</p></li>
<li><p>100</p></li>
<li><p>100</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>Réseau local</p></li>
<li><p>Réseau local</p></li>
<li><p>Réseau local</p></li>
<li><p>Réseau local</p></li>
<li><p>Réseau local</p></li>
<li><p>Réseau local</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>0,10</p></li>
<li><p>27,9</p></li>
<li><p>27,9</p></li>
<li><p>Seiz</p></li>
<li><p>22</p></li>
<li><p>1,25</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>Play</p></li>
<li><p>19,6</p></li>
<li><p>22</p></li>
<li><p>19,6</p></li>
<li><p>CX3-20</p></li>
<li><p>CX3-20</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Métadonnées de publication contenant des groupes d’accès</p></td>
<td align="left"><p>Nombre de groupes d’accès</p></td>
<td align="left"><p></p>
<ul>
<li><p>0,4</p></li>
<li><p>0,4</p></li>
<li><p>0,4</p></li>
<li><p>0,4</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>1</p></li>
<li><p>0,10</p></li>
<li><p>CX3-20</p></li>
<li><p>40</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>100</p></li>
<li><p>100</p></li>
<li><p>100</p></li>
<li><p>100</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>Réseau local</p></li>
<li><p>Réseau local</p></li>
<li><p>Réseau local</p></li>
<li><p>Réseau local</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>0,10</p></li>
<li><p>43</p></li>
<li><p>153</p></li>
<li><p>535</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>Play</p></li>
<li><p>26/08/03</p></li>
<li><p>24</p></li>
<li><p>24</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

L’utilisation de l’UC de l’ordinateur exécutant le serveur de gestion est d’environ 25%, sans tenir compte du nombre de serveurs de publication ciblant celle-ci. Les transactions/s de base de données Microsoft SQL Server, les requêtes par lot/s et les connexions utilisateur sont identiques quel que soit le nombre de serveurs de publication. Par exemple: transactions/s est ~ 30, les demandes de lot ~ 200 et l’utilisateur connecte ~ 6.

Dans le cadre d’un déploiement distribué sur le graphique, lorsque le serveur de gestion & serveurs de publication utilise un réseau de liaison lente entre eux, le temps de réponse en boucle sur les serveurs de publication est limité à un délai de &lt; 5 secondes, même pour les demandes simultanées 100 sur un serveur de gestion unique.

<table>
<colgroup>
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Scénario</th>
<th align="left">Variante</th>
<th align="left">Nombre de groupes de connexion</th>
<th align="left">Nombre de groupes d’accès</th>
<th align="left">Nombre de serveurs de publication</th>
<th align="left">Serveur de publication de type de connexion réseau/serveur de gestion</th>
<th align="left">Temps de réponse aller-retour sur le serveur de publication (en secondes)</th>
<th align="left">Utilisation de l’UC sur le serveur de gestion</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Connexion réseau entre le serveur de publication et le serveur de gestion</p></td>
<td align="left"><p>Réseau de liaison lente 1,5 Mbps</p></td>
<td align="left"><p></p>
<ul>
<li><p>0,4</p></li>
<li><p>0,4</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>1</p></li>
<li><p>1</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>50</p></li>
<li><p>100</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>Câble ADSL de 1,5 MB/s</p></li>
<li><p>Câble ADSL de 1,5 MB/s</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>n°4</p></li>
<li><p>n°5</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>1</p></li>
<li><p>deuxième</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Connexion réseau entre le serveur de publication et le serveur de gestion</p></td>
<td align="left"><p>Réseau LAN/WIFI</p></td>
<td align="left"><p></p>
<ul>
<li><p>0,4</p></li>
<li><p>0,4</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>1</p></li>
<li><p>1</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>100</p></li>
<li><p>200</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>Wi-Fi</p></li>
<li><p>Wi-Fi</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>27,9</p></li>
<li><p>CX3-20</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>0,15</p></li>
<li><p>Play</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

Le serveur de gestion et les serveurs de publication sont connectés à un réseau de liaison lente ou d’un réseau haut débit, le serveur de gestion peut gérer approximativement 15 000 demandes d’actualisation de package dans 30 minutes.

## <a href="" id="---------app-v-5-1-reporting-server-capacity-planning-recommendations"></a> Recommandations pour la planification de la capacité du serveur App-V 5,1


Les clients App-V 5,1 envoient des données de création de rapports au serveur de rapports. Le serveur de création de rapports enregistre ensuite les informations dans la base de données Microsoft SQL Server et renvoie une notification réussie à l’ordinateur exécutant le client App-V 5,1. Pour plus d’informations sur les configurations prises en charge par App-V 5,1 Report Server, voir [Configurations prises en charge par app-v 5,1](app-v-51-supported-configurations.md).

**Remarques**  Le temps de réponse aller-retour est le temps écoulé par l’ordinateur exécutant le client App-V 5,1 pour envoyer les informations de rapport au serveur de création de rapports et recevoir une notification réussie du serveur de rapports.

 

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Scénario</th>
<th align="left">Résumé</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Plusieurs clients App-V 5,1 envoient simultanément des informations de rapport au serveur de rapports.</p></td>
<td align="left"><p></p>
<ul>
<li><p>Le temps de réponse en boucle du serveur de rapports est de 2,6 secondes pour les clients 500.</p></li>
<li><p>Le temps de réponse en boucle du serveur de rapports est de 5,65 secondes pour les clients 1000.</p></li>
<li><p>Le temps de réponse en boucle augmente de façon linéaire en fonction du nombre de clients.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Demandes par seconde traitées par le serveur de rapports.</p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p>Un serveur de création de rapports unique et une seule base de données peuvent traiter un maximum de demandes 139 par seconde. La moyenne est 121 demandes/secondes.</p></li>
<li><p>En utilisant deux serveurs de création de rapports sur la même base de données Microsoft SQL Server, la moyenne des demandes/secondes est similaire à un serveur de rapports unique = ~ 127, avec une limite de 278 demandes/seconde.</p></li>
<li><p>Un serveur de rapports unique peut traiter les connexions 500 concurrentes/actives.</p></li>
<li><p>Un serveur de rapports unique peut traiter une connexion simultanée 1500 maximum.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Base de données de création de rapports.</p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p>Le verrouillage du contenu sur l’ordinateur exécutant Microsoft SQL Server est le facteur de limitation pour les demandes/secondes.</p></li>
<li><p>Le débit et le temps de réponse sont indépendants de la taille de la base de données.</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

**Calcul du retard aléatoire**:

Le délai aléatoire spécifie le délai maximal (en minutes) pendant lequel les données doivent être envoyées au serveur de rapports. Lorsque la tâche planifiée est lancée, le client génère un délai aléatoire compris entre **0** et **ReportingRandomDelay** et attend la durée spécifiée avant d’envoyer des données.

Retard aléatoire = 4 \ * nombre de clients/demandes de moyenne par seconde.

Exemple: pour les clients 500, avec des demandes 120 par seconde, le délai aléatoire est de 4 \ * 500/120 = ~ 17 minutes.

## <a href="" id="---------app-v-5-1-publishing-server-capacity-planning-recommendations"></a> Recommandations en matière de planification de la capacité du serveur Publisher V 5,1


Les ordinateurs exécutant le client App-V 5,1 se connectent au serveur de publication App-V 5,1 pour envoyer une demande d’actualisation de publication et recevoir une réponse. La durée de réponse en boucle est mesurée sur l’ordinateur exécutant le client App-V 5,1. La durée du processeur est mesurée sur le serveur de publication. Pour plus d’informations sur les configurations prises en charge par le serveur de publication App-V 5,1, consultez la rubrique [configurations App-v 5,1 prises en charge](app-v-51-supported-configurations.md).

**Important**  La liste suivante indique les principaux facteurs à prendre en compte lors de la configuration du serveur de publication 5,1 App-V.

-   Nombre de clients qui se connectent simultanément à un serveur de publication unique.

-   Nombre de packages de chaque actualisation.

-   La bande passante réseau disponible dans votre environnement entre le client et le serveur de publication 5,1 de l’application.

 

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Scénario</th>
<th align="left">Résumé</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Plusieurs clients App-V 5,1 se connectent à un serveur de publication unique simultanément.</p></td>
<td align="left"><p></p>
<ul>
<li><p>Un serveur de publication exécutant des processeurs double cœur peut répondre à la plupart des clients 5000 demandant une actualisation simultanée.</p></li>
<li><p>Pour les clients 5000-10000, le serveur de publication nécessite un minimum de quatre cœurs.</p></li>
<li><p>Pour les clients 10000-20000, le serveur de publication doit disposer de deux cœurs pour des temps de réponse plus efficaces.</p></li>
<li><p>Un serveur de publication avec un noyau à quatre cœurs peut actualiser jusqu’à 10000 packages dans un délai de 3 secondes. (Prise en charge des clients simultanés 10000)</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Nombre de packages de chaque actualisation.</p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p>L’augmentation du nombre de packages augmente le délai de réponse de ~ 40% (jusqu’à 1000 Packages).</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Réseau entre le client App-V 5,1 et le serveur de publication.</p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p>Sur une connexion réseau lente (bande passante 1,5 Mbps), il existe un délai de réponse d' 97% par rapport au réseau local (jusqu’à 1000 utilisateurs).</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

**Remarques**  Le taux d’utilisation de l’UC du serveur de publication est toujours élevé pendant l’intervalle de temps pendant lequel il doit traiter les demandes simultanées ( &gt; 90% dans la plupart des cas). Le serveur de publication peut gérer les demandes du client ~ 1500 en 1 seconde.

 

<table>
<colgroup>
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Scénario</th>
<th align="left">Variante</th>
<th align="left">Nombre de clients App-V 5,1</th>
<th align="left">Nombre de packages</th>
<th align="left">Configuration du processeur sur le serveur de publication</th>
<th align="left">Type de connexion réseau-client de publication de type serveur/App-V 5,1</th>
<th align="left">Durée de l’aller-retour sur le client App-V 5,1 (en secondes)</th>
<th align="left">Utilisation de l’UC sur le serveur de publication (en%)</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Le client App-V 5,1 envoie une demande d’actualisation &amp; de publication reçoit une réponse, chaque requête contenant des packages 120</p></td>
<td align="left"><p>Nombre de clients</p></td>
<td align="left"><p></p>
<ul>
<li><p>100</p></li>
<li><p>1000</p></li>
<li><p>5000</p></li>
<li><p>10000</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>120</p></li>
<li><p>120</p></li>
<li><p>120</p></li>
<li><p>120</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>Double cœur</p></li>
<li><p>Double cœur</p></li>
<li><p>Quadruple cœur</p></li>
<li><p>Quadruple cœur</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>Réseau local</p></li>
<li><p>Réseau local</p></li>
<li><p>Réseau local</p></li>
<li><p>Réseau local</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>1</p></li>
<li><p>deuxième</p></li>
<li><p>deuxième</p></li>
<li><p>3D</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>100</p></li>
<li><p>99</p></li>
<li><p>89</p></li>
<li><p>77</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Plusieurs packages pour chaque actualisation</p></td>
<td align="left"><p>Nombre de packages</p></td>
<td align="left"><p></p>
<ul>
<li><p>1000</p></li>
<li><p>1000</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>500</p></li>
<li><p>1000</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>Quadruple cœur</p></li>
<li><p>Quadruple cœur</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>Réseau local</p></li>
<li><p>Réseau local</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>deuxième</p></li>
<li><p>3D</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>92</p></li>
<li><p>91</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Réseau entre le client et le serveur de publication</p></td>
<td align="left"><p>réseau de liaison lente 1,5 Mbps</p></td>
<td align="left"><p></p>
<ul>
<li><p>100</p></li>
<li><p>500</p></li>
<li><p>1000</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>120</p></li>
<li><p>120</p></li>
<li><p>120</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>Quadruple cœur</p></li>
<li><p>Quadruple cœur</p></li>
<li><p>Quadruple cœur</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>Réseau intra-continent 1,5 MB/s</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>3D</p></li>
<li><p>10 (avec le taux d’échec de 0,2%)</p></li>
<li><p>17 (avec un taux d’échec de 1%)</p></li>
</ul></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="---------app-v-5-1-streaming-capacity-planning-recommendations"></a> Recommandations en matière de planification de capacité de flux d’application V 5,1


Les ordinateurs exécutant le client App-V 5,1 diffusent le package de l’application virtuelle à partir du serveur de diffusion en continu. La durée de réponse en boucle est mesurée sur l’ordinateur exécutant le client App-V 5,1 et est le temps nécessaire pour diffuser l’intégralité du package.

**Important**  La liste suivante indique les principaux facteurs à prendre en compte lors de la configuration du serveur de streaming App-V 5,1:

-   Le nombre de clients en diffusant des packages d’application simultanément depuis un serveur de diffusion unique.

-   Taille du package en cours de diffusion.

-   La bande passante réseau disponible dans votre environnement entre le client et le serveur de diffusion.

 

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Scénario</th>
<th align="left">Résumé</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Plusieurs clients App-V 5,1 diffusent simultanément des applications à partir d’un serveur en flux unique.</p></td>
<td align="left"><p></p>
<ul>
<li><p>Si le nombre de clients diffusés en continu à partir du même serveur augmente, il existe une relation linéaire avec le temps de téléchargement/de diffusion du package.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Taille du package en cours de diffusion.</p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p>La taille du package a un impact significatif sur le temps de diffusion/téléchargement uniquement pour les packages plus grands dont la taille est de ~ 1 Go. Pour les tailles de packages comprises entre 3 Mo et 100 Mo, la durée de diffusion varie de 20 secondes à 100 secondes, avec les clients simultanés 100.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Réseau entre le client App-V 5,1 et le serveur de streaming.</p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p>Sur une connexion réseau lente (bande passante 1,5 Mbps), il existe un délai de réponse d' 70-80% par rapport au réseau local (jusqu’à 100 utilisateurs).</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

Le tableau suivant présente des exemples de valeurs pour chacun des facteurs de la liste précédente:

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Scénario</th>
<th align="left">Variante</th>
<th align="left">Nombre de clients App-V 5,1</th>
<th align="left">Taille de chaque package</th>
<th align="left">Serveur de type connexion réseau/client App-V 5,1</th>
<th align="left">Durée de l’aller-retour sur le client App-V 5,1 (en secondes)</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Plusieurs clients App-V 5,1 diffusent des packages d’application virtuels à partir d’un serveur en flux continu.</p></td>
<td align="left"><p>Nombre de clients.</p></td>
<td align="left"><p></p>
<ul>
<li><p>100</p></li>
<li><p>200</p></li>
<li><p>1000</p></li>
<li><p></p></li>
<li><p>100</p></li>
<li><p>200</p></li>
<li><p>1000</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>3,5 Mo</p></li>
<li><p>3,5 Mo</p></li>
<li><p>3,5 Mo</p></li>
<li><p></p></li>
<li><p>5 MO</p></li>
<li><p>5 MO</p></li>
<li><p>5 MO</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>Réseau local</p></li>
<li><p>Réseau local</p></li>
<li><p>Réseau local</p></li>
<li><p></p></li>
<li><p>Réseau local</p></li>
<li><p>Réseau local</p></li>
<li><p>Réseau local</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>mai</p></li>
<li><p>39</p></li>
<li><p>391</p></li>
<li><p></p></li>
<li><p>35</p></li>
<li><p>68</p></li>
<li><p>461</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Taille de chaque package en cours de diffusion.</p></td>
<td align="left"><p>Taille de chaque package.</p></td>
<td align="left"><p></p>
<ul>
<li><p>100</p></li>
<li><p>200</p></li>
<li><p></p></li>
<li><p>100</p></li>
<li><p>200</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>21 MO</p></li>
<li><p>21 MO</p></li>
<li><p></p></li>
<li><p>109</p></li>
<li><p>109</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>Réseau local</p></li>
<li><p>Réseau local</p></li>
<li><p></p></li>
<li><p>Réseau local</p></li>
<li><p>Réseau local</p></li>
</ul></td>
<td align="left"><p></p>
<p>33</p>
<p>83</p>
<p></p>
<p>100</p>
<p>160</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Connexion réseau entre le client et le serveur de streaming App-V 5,1.</p></td>
<td align="left"><p>1,5 Mbps réseau de liaison lente.</p></td>
<td align="left"><p></p>
<ul>
<li><p>100</p></li>
<li><p></p></li>
<li><p>100</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>3,5 Mo</p></li>
<li><p></p></li>
<li><p>5 MO</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>Réseau intra-continent 1,5 MB/s</p></li>
</ul></td>
<td align="left"><p></p>
<p>102</p>
<p></p>
<p>121</p></td>
</tr>
</tbody>
</table>

 

Chaque serveur de streaming App-V 5,1 doit être en mesure de gérer un minimum de clients 200 en continu à partir d’applications virtualisées.

**Remarques**  La durée réelle du flux est déterminée principalement par le nombre de clients diffusés en continu, le nombre de packages, la taille du package, l’activité réseau du serveur et les conditions du réseau.

 

Par exemple, un utilisateur moyen peut diffuser un package 100 Mo en moins de 2 minutes, lorsque 100 clients simultanés sont en continu à partir du serveur. Toutefois, un paquet d’une taille de 1 Go peut durer jusqu’à 30 minutes. Dans la plupart des environnements réalistes, la diffusion en continu n’est pas uniformément distribuée, vous devez comprendre les exigences de flux maximal en matière de diffusion actuelles dans votre environnement afin de dimensionner correctement le nombre de serveurs de diffusion en continu requis.

Le nombre de clients qu’un serveur en continu peut prendre en charge peut être considérablement augmenté et les exigences en matière de flux maximal réduites si vous prémettez vos applications en cache. Vous pouvez également augmenter le nombre de clients pris en charge par un serveur de diffusion en utilisant la diffusion en continu à la demande et des packages optimisés pour les flux.

## Combinaison des rôles de serveur App-V 5,1


Remise de la mise à l’échelle et des exigences de tolérance de panne, le nombre minimal de serveurs nécessaires pour un emplacement avec la connectivité à Active Directory est un. Ce serveur va héberger le serveur de gestion, le service serveur de gestion et les rôles Microsoft SQL Server. Les rôles de serveur peuvent donc être organisés selon n’importe quelle combinaison souhaitée, car ils ne sont pas en conflit entre eux.

En ignorant les exigences de mise à l’échelle, le nombre minimum de serveurs nécessaires à la fourniture d’une implémentation tolérante aux pannes est de quatre. Le serveur de gestion et les rôles Microsoft SQL Server pris en charge sont placés dans des configurations tolérantes aux pannes. Le service du serveur de gestion peut être combiné avec n’importe lequel des rôles, mais il reste un point de défaillance unique.

Bien qu’il existe un certain nombre de stratégies et de technologies de tolérance de panne disponibles, elles ne s’appliquent pas à un service donné. De plus, si les rôles App-V 5,1 sont combinés, certaines options de tolérance de panne risquent de ne plus être applicables en raison d’incompatibilités.






## Rubriques connexes


[Configurations prises en charge par App-V5.1](app-v-51-supported-configurations.md)

[Planification de la haute disponibilité avec App-V5.1](planning-for-high-availability-with-app-v-51.md)

[Envisager de déployer App-V](planning-to-deploy-app-v51.md)

 

 





