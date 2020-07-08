---
title: Copie des modèles de stratégie de groupe MBAM2.5
description: Copie des modèles de stratégie de groupe MBAM2.5
author: dansimp
ms.assetid: e526ecec-07ff-435e-bc90-3084b617b84b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/28/2017
ms.openlocfilehash: a3436552256b1632a11037dc94751207cde89d5c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811027"
---
# Copie des modèles de stratégie de groupe MBAM2.5


Avant de déployer l’installation du client MBAM, vous devez télécharger les modèles de stratégie de groupe MBAM qui contiennent des paramètres de stratégie de groupe définissant les paramètres d’implémentation MBAM pour le chiffrement de lecteur BitLocker. Après avoir téléchargé les modèles, vous définissez les paramètres de stratégie de groupe à implémenter au sein de votre entreprise.

## Télécharger et déployer les modèles de stratégie de groupe MDOP


Les modèles de stratégie de groupe MDOP peuvent être téléchargés dans un fichier auto-extractible, compressé, groupé par technologie et version.

**Télécharger et déployer les modèles de stratégie de groupe MDOP**

1. Téléchargez les modèles de stratégie de groupe MDOP à partir des [modèles d’administration de la stratégie de groupe Microsoft Desktop Optimization](https://www.microsoft.com/download/details.aspx?id=55531).

2. Exécutez le fichier téléchargé pour extraire les dossiers du modèle.

   **Warning**  
   Ne récupérez pas les modèles directement dans le répertoire de déploiement de la stratégie de groupe. Plusieurs technologies et versions sont regroupées dans ce fichier.



3. Dans le dossier extraits, recherchez le fichier Technology-version. admx. Certaines technologies MDOP disposent de plusieurs ensembles d’objets de stratégie de groupe. Par exemple, MBAM inclut des paramètres de gestion MBAM et des paramètres utilisateur MBAM.

4. Recherchez le fichier. adml approprié par language-culture ( *c’est-à-dire, en* anglais-États-Unis).

5. Copiez les fichiers. admx et. adml dans un dossier de définition de stratégie. En fonction de l’emplacement de stockage des modèles, vous pouvez configurer les paramètres de stratégie de groupe à partir de l’appareil local ou à partir de n’importe quel ordinateur du domaine.

   **Fichiers locaux.** Pour configurer les paramètres de stratégie de groupe à partir de l’appareil local, copiez les fichiers de modèles aux emplacements suivants:

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



~~~
**Domain central store.** To enable Group Policy settings configuration by a Group Policy administrator from any computer on the domain, copy files to the following locations on the domain controller:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">File type</th>
<th align="left">File location</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Group Policy template (.admx)</p></td>
<td align="left"><p><code>%systemroot%</code>\<strong>sysvol\domain\policies\PolicyDefinitions</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>Group Policy language file (.adml)</p></td>
<td align="left"><p><code>%systemroot%</code>\<strong>sysvol\domain\policies\PolicyDefinitions\[MUIculture]</strong><code>\[MUIculture]</code></p>
<p>For example, the U.S. English ADML language-specific file will be stored in %systemroot%\sysvol\domain\policies\PolicyDefinitions\en-us.</p></td>
</tr>
</tbody>
</table>
~~~



6. Modifiez les paramètres de stratégie de groupe à l’aide de la console de gestion des stratégies de groupe (GPMC) ou de la gestion de la stratégie de groupe avancée (AGPM) pour configurer les paramètres de stratégie de groupe pour la technologie MDOP. Pour plus d’informations, reportez-vous à [modification des paramètres de stratégie de groupe MBAM 2,5](editing-the-mbam-25-group-policy-settings.md) .

   Pour obtenir une description des paramètres de stratégie de groupe, reportez-vous [à la planification des exigences de stratégie de groupe MBAM 2,5](planning-for-mbam-25-group-policy-requirements.md).


## Rubriques connexes


[Déploiement d'objets de stratégie de groupe MBAM2.5](deploying-mbam-25-group-policy-objects.md)


## Vous avez une suggestion pour MBAM?
- Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring) 
- Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).






