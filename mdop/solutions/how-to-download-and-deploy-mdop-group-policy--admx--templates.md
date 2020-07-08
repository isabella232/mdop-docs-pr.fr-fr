---
title: Téléchargement et déploiement des modèles de stratégie de groupe MDOP (.admx)
description: Téléchargement et déploiement des modèles de stratégie de groupe MDOP (.admx)
author: dansimp
ms.assetid: fdb64505-6c66-4fdf-ad74-a6a161191e3f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/15/2018
ms.openlocfilehash: 5bc5f8d536c113ccbc0a1931e6c7e4ed3c7a9a37
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812042"
---
# Téléchargement et déploiement des modèles de stratégie de groupe MDOP (.admx)


Vous pouvez gérer les paramètres de fonctionnalité de certaines technologies du pack d’optimisation du bureau Microsoft (par exemple, app-v, UE-V ou MBAM) à l’aide de modèles de stratégie de groupe, fichiers. admx et. adml. Les modèles de stratégie de groupe MDOP peuvent être téléchargés dans un fichier auto-extractible, compressé, groupé par technologie et version.

## Modèles de stratégie de groupe MDOP

**Télécharger et déployer les modèles de stratégie de groupe MDOP**

1. Télécharger les derniers [modèles de stratégie de groupe MDOP](https://www.microsoft.com/download/details.aspx?id=55531) 

2. Développez le fichier téléchargé. cab en exécutant `expand <download_folder>\MDOP_ADMX_Templates.cab -F:* <destination_folder>`

   **Warning**  
   Ne récupérez pas les modèles directement dans le répertoire de déploiement de la stratégie de groupe. Plusieurs technologies et versions sont regroupées dans ce fichier.

3. Dans le dossier extraits, recherchez le fichier Technology-version. admx. Certaines technologies MDOP disposent de plusieurs ensembles d’objets de stratégie de groupe. Par exemple, MBAM inclut des paramètres de gestion MBAM et des paramètres utilisateur MBAM.

4. Recherchez le fichier. adml approprié par language-culture (c’est-à-dire, en *-US* pour English-France).

5. Copiez les fichiers. admx et. adml dans un dossier de définition de stratégie. En fonction de l’emplacement de stockage des modèles, vous pouvez configurer les paramètres de stratégie de groupe à partir de l’appareil local ou à partir de n’importe quel ordinateur du domaine.

   - **Fichiers locaux:** Pour configurer les paramètres de stratégie de groupe à partir de l’appareil local, copiez les fichiers de modèles aux emplacements suivants:

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
   <td align="left"><p>Modèle de stratégie de groupe (. admx)</p></td>
   <td align="left"><p><code>%systemroot%</code>&lt;forte &gt; PolicyDefinitions</strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Fichier de langue de la stratégie de groupe (. adml)</p></td>
   <td align="left"><p><code>%systemroot%</code>&lt;forte &gt; PolicyDefinitions</strong><code>[MUIculture]</code></p></td>
   </tr>
   </tbody>
   </table>

   - **Magasin central du domaine:** Pour activer la configuration des paramètres de stratégie de groupe par un administrateur de stratégie de groupe à partir de n’importe quel ordinateur du domaine, copiez les fichiers aux emplacements suivants sur le contrôleur de domaine:

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
   <td align="left"><p>Modèle de stratégie de groupe (. admx)</p></td>
   <td align="left"><p><code>%systemroot%</code>&lt;forte &gt; sysvol\domain\policies\PolicyDefinitions</strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Fichier de langue de la stratégie de groupe (. adml)</p></td>
   <td align="left"><p><code>%systemroot%</code>&lt;forte &gt; sysvol\domain\policies\PolicyDefinitions [MUIculture]</strong><code>[MUIculture]</code></p>
   <p>Par exemple, le fichier propre à la langue de l’anglais (États-Unis) est stocké dans%systemroot%\sysvol\domain\policies\PolicyDefinitions\en-us.</p></td>
   </tr>
   </tbody>
   </table>

6. Modifiez les paramètres de stratégie de groupe à l’aide de la console de gestion des stratégies de groupe (GPMC) ou de la gestion de la stratégie de groupe avancée (AGPM) pour configurer les paramètres de stratégie de groupe pour la technologie MDOP.

### Stratégie de groupe MDOP par technologie

Pour plus d’informations sur les stratégies de groupe MDOP prises en charge, voir la documentation spécifique de la technologie.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Technologie MDOP</th>
<th align="left">Ensembles de versions</th>
<th align="left">Remarques</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Application Virtualization (App-V)</strong></p></td>
<td align="left"><p>Service packs App-V 5,0 et App-V 5,0</p></td>
<td align="left"><p><a href="../appv-v5/how-to-modify-app-v-50-client-configuration-using-the-admx-template-and-group-policy.md" data-raw-source="[How to Modify App-V 5.0 Client Configuration Using the ADMX Template and Group Policy](../appv-v5/how-to-modify-app-v-50-client-configuration-using-the-admx-template-and-group-policy.md)">Modification de la configuration d'App-V5.0 Client à l'aide du modèle ADMX et d'une stratégie de groupe</a></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>User Experience Virtualization (UE-V)</strong></p></td>
<td align="left"><p>UE-V 2,0 et UE-V 2,1</p></td>
<td align="left"><p><a href="../uev-v2/configuring-ue-v-2x-with-group-policy-objects-both-uevv2.md" data-raw-source="[Configuring UE-V 2.x with Group Policy Objects](../uev-v2/configuring-ue-v-2x-with-group-policy-objects-both-uevv2.md)">Configuration d’UE-V 2. x avec des objets de stratégie de groupe</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p>UE-V 1,0, y compris 1,0 SP1</p></td>
<td align="left"><p><a href="../uev-v1/configuring-ue-v-with-group-policy-objects.md" data-raw-source="[Configuring UE-V with Group Policy Objects](../uev-v1/configuring-ue-v-with-group-policy-objects.md)">Configuration d’UE-V avec les objets de stratégie de groupe</a></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Microsoft BitLocker Administration and Monitoring (MBAM)</strong></p></td>
<td align="left"><p>MBAM 2,5</p></td>
<td align="left"><p><a href="../mbam-v25/planning-for-mbam-25-group-policy-requirements.md" data-raw-source="[Planning for MBAM 2.5 Group Policy Requirements](../mbam-v25/planning-for-mbam-25-group-policy-requirements.md)">Planification des exigences en matière de stratégie de groupe MBAM2.5</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p>MBAM 2,0, y compris 2,0 SP1</p></td>
<td align="left"><p><a href="../mbam-v2/planning-for-mbam-20-group-policy-requirements-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Group Policy Requirements](../mbam-v2/planning-for-mbam-20-group-policy-requirements-mbam-2.md)">Planification des exigences en matière de stratégie de groupe MBAM2.0</a></p>
<p><a href="../mbam-v2/deploying-mbam-20-group-policy-objects-mbam-2.md" data-raw-source="[Deploying MBAM 2.0 Group Policy Objects](../mbam-v2/deploying-mbam-20-group-policy-objects-mbam-2.md)">Déploiement d'objets de stratégie de groupe MBAM2.0</a></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p>MBAM 1,0</p></td>
<td align="left"><p><a href="../mbam-v1/how-to-edit-mbam-10-gpo-settings.md" data-raw-source="[How to Edit MBAM 1.0 GPO Settings](../mbam-v1/how-to-edit-mbam-10-gpo-settings.md)">Procédure de modification des paramètres d'objet de stratégie de groupe MBAM1.0</a></p></td>
</tr>
</tbody>
</table>

 

 

 





