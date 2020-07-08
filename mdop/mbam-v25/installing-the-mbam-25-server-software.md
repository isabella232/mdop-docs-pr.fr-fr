---
title: Installation du logiciel serveur MBAM2.5
description: Installation du logiciel serveur MBAM2.5
author: dansimp
ms.assetid: b9dbe697-5400-4bac-acfb-ee6dc6586c30
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6612bf52aa53ae693694d7ac02c5cab212d4e24f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809929"
---
# Installation du logiciel serveur MBAM2.5


Cette rubrique décrit comment installer le logiciel serveur d’administration et de surveillance de BitLocker (MBAM) 2,5 à l’aide de l’Assistant de configuration de l’administration et de la surveillance de BitLocker ou en utilisant des paramètres de ligne de commande. Répétez le processus d’installation du serveur pour chaque serveur sur lequel vous configurez les fonctionnalités du serveur MBAM 2,5. Une fois l’installation terminée, reportez-vous à [Configuration des fonctionnalités du serveur MBAM 2,5](configuring-the-mbam-25-server-features.md) pour connaître les étapes de configuration des fonctionnalités du serveur.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Avant de commencer</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Passez en revue les informations de planification de MBAM 2,5</p></td>
<td align="left"><ul>
<li><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)">Conditions préalables pour le serveur MBAM2.5 pour les topologies Intégration Configuration Manager et autonome</a></p></li>
<li><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">Configurations prises en charge par MBAM2.5</a></p></li>
<li><p><a href="high-level-architecture-for-mbam-25.md" data-raw-source="[High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md)">Architecture de hautniveau pour MBAM2.5</a></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Découvrir comment obtenir les fichiers journaux</p></td>
<td align="left"><p>Par défaut, les fichiers journaux sont créés dans le dossier% Temp% de l’ordinateur local. Pour enregistrer les fichiers journaux à un emplacement spécifique plutôt que dans le <strong> dossier% Temp </strong> %, utilisez l' <strong> </strong> &lt; <em> argument d’emplacement/log </em> &gt; .</p>
<p>Des événements supplémentaires peuvent être enregistrés dans l’observateur d’événements dans les <strong> nœuds mbam-setup </strong> ou <strong> MBAM-site Web </strong> sous <strong> applications et services consigne &gt; Microsoft &gt; Windows </strong> . Par exemple, si vous désinstallez MBAM, le programme de désinstallation désinstalle également les journaux MBAM-Setup et MBAM-Web dans EventViewer.</p></td>
</tr>
</tbody>
</table>

 

## Installation du logiciel serveur MBAM 2,5 à l’aide de l’Assistant Configuration et analyse de Microsoft BitLocker


Suivez les étapes ci-dessous pour installer le logiciel serveur MBAM à l’aide de l’Assistant Configuration et analyse de Microsoft BitLocker.

**Pour installer le logiciel serveur MBAM 2,5 à l’aide de l’Assistant**

1.  Sur le serveur sur lequel vous souhaitez installer MBAM, exécutez **MBAMserversetup.exe** pour démarrer l’Assistant de configuration de l’administration et de la surveillance de BitLocker.

2.  Dans la page **Bienvenue** , cliquez sur **suivant**.

3.  Lisez et acceptez le contrat de licence logiciel Microsoft, puis cliquez sur **suivant** pour continuer l’installation.

4.  Indiquez si vous souhaitez utiliser Microsoft Update lors de la recherche de mises à jour, puis cliquez sur **suivant**.

5.  Indiquez si vous souhaitez participer au programme d’amélioration du produit, puis cliquez sur **suivant**.

6.  Pour démarrer l’installation, cliquez sur **installer**.

7.  Pour configurer les fonctionnalités du serveur après l’installation du logiciel MBAM Server, activez la case à cocher **exécuter MBAM Server Configuration une fois l’Assistant fermé** . Vous pouvez également configurer MBAM plus tard en utilisant le raccourci de **configuration de MBAM Server** que le programme d’installation du serveur crée dans le menu **Démarrer** .

8.  Cliquez sur **Terminer**.

## Installation du logiciel serveur MBAM 2,5 à l’aide d’une fenêtre d’invite de commandes


À l’invite de commandes, tapez une commande similaire à la commande suivante pour installer le logiciel serveur MBAM.

``` syntax
MbamServerSetup.exe MBAMServerInstall.log
CEIPENABLED=True OPTIN_FOR_MICROFOST_UPDATES=True INSTALLDIR=c:\mbaminstall
```

Le tableau suivant décrit les paramètres de ligne de commande pour l’installation du logiciel MBAM 2,5 Server.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Paramètre</th>
<th align="left">Valeur du paramètre</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>CEIPENABLED</p></td>
<td align="left"><p>Vrai faux</p></td>
<td align="left"><p>Vrai-participer au programme d’amélioration du produit, qui permet à Microsoft d’identifier les fonctionnalités de MBAM à améliorer.</p>
<p>Faux – ne pas participer au programme d’amélioration du produit.</p></td>
</tr>
<tr class="even">
<td align="left"><p>OPTIN_FOR_MICROSOFT_UPDATES</p></td>
<td align="left"><p>Vrai faux</p></td>
<td align="left"><p>Vrai-utilisez Microsoft Update pour garantir la sécurité et la mise à jour de votre ordinateur pour Windows et d’autres produits Microsoft, y compris MBAM.</p>
<p>Faux – ne pas utiliser Microsoft Update</p></td>
</tr>
<tr class="odd">
<td align="left"><p>INSTALLDIR</p></td>
<td align="left"><p>&lt;Chemin d'accès&gt;</p></td>
<td align="left"><p>Emplacement où vous souhaitez installer MBAM.</p>
<p>Exemple :</p>
<p>INSTALLDIR = c:\mbaminstall</p></td>
</tr>
<tr class="even">
<td align="left"><p>FORCE_UNINSTALL</p></td>
<td align="left"><p>Vrai faux</p></td>
<td align="left"><p>Vrai-poursuivre le processus de désinstallation d’MBAM, même si des fonctionnalités ne peuvent pas être supprimées.</p>
<p>False (par défaut) si l’action personnalisée de désinstallation ne parvient pas à supprimer une fonctionnalité de serveur MBAM ajoutée, la désinstallation échoue et MBAM reste installé.</p>
<p>Dans les deux cas, toutes les fonctionnalités qui ont été correctement supprimées lors de la tentative de désinstallation de MBAM restent supprimées.</p></td>
</tr>
</tbody>
</table>

 



## Rubriques connexes


[Déploiement de MBAM2.5](deploying-mbam-25.md)

[Configuration des composants du serveur MBAM2.5](configuring-the-mbam-25-server-features.md)

 

## Vous avez une suggestion pour MBAM?
- Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring) 
- Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





