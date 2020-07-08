---
title: Procédure pour configurer le fichier journal du client
description: Procédure pour configurer le fichier journal du client
author: dansimp
ms.assetid: dd79f8ce-61e2-4dc8-af03-2a353554a1b2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 729089d683c5d102eb7eb45314583023d3362639
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807250"
---
# Procédure pour configurer le fichier journal du client


Vous pouvez utiliser les procédures suivantes pour configurer le fichier journal du client de virtualisation des applications (App-V).

**Pour modifier l’emplacement du fichier journal**

-   Modifiez la valeur de clé de Registre suivante pour spécifier le nouveau chemin d’accès au fichier journal. Après avoir modifié cette valeur, vous devez redémarrer le service **sftlist** . Ce lieu peut également être modifié de manière interactive après l’installation.

    HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\LogFileName

**Pour modifier le niveau de rapport du journal**

-   Par défaut, le type de messages qui sont écrits dans le journal inclut tous les événements de niveau de gravité 4 (information) ou version ultérieure. Le niveau de gravité est stocké dans la valeur de clé suivante. Définissez cette valeur de clé sur 5 pour activer la journalisation détaillée. Utilisez la journalisation détaillée uniquement pour les courtes périodes lors de la résolution des problèmes, car elle génère un volume de messages de très grande taille et entraîne le remplissage rapide du journal.

    HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\LogMinSeverity

**Pour modifier la taille du journal**

-   Dans Application Virtualization (App-V) 4,5, la taille du journal est contrôlée par la valeur de clé de Registre suivante. Cette valeur est définie par défaut sur 256Mo et définit la taille maximale (en Mo) à laquelle le journal peut s’étendre avant de procéder à la réinitialisation.

    HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\LogMaxSize

    **Attention**  La valeur de cette clé de registre doit être définie sur une valeur supérieure à zéro pour garantir la réinitialisation du fichier journal.

     

**Pour modifier le nombre de copies de sauvegarde**

-   Lorsque le fichier journal atteint la taille maximale, une réinitialisation est imposée lors de l’écriture suivante du journal. Une réinitialisation entraîne la création d’un nouveau fichier journal et l’ancien fichier est renommé comme sauvegarde. Le paramètre de Registre suivant contrôle le nombre de copies de sauvegarde du fichier journal conservées lors de la réinitialisation du fichier. La valeur par défaut est 4.

    HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\LogRolloverCount

    Le format des noms de fichiers du journal de sauvegarde est le suivant: **sftlog\_YYYYMMDD\_hhmmss-uuu.txt** et repose sur l’heure de réinitialisation, en temps universel coordonné (UTC). Le tableau suivant répertorie les symboles utilisés lors de la création du nom de fichier et leurs descriptions.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Symbole</th>
    <th align="left">Description</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>MM</p></td>
    <td align="left"><p>année à 4 chiffres</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>HAUTEUR</p></td>
    <td align="left"><p>mois de 2 chiffres (01 à 12)</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>UTER</p></td>
    <td align="left"><p>jour sur 2 chiffres du mois (01 à 31)</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>hh</p></td>
    <td align="left"><p>heure (00 à 23)</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>hauteur</p></td>
    <td align="left"><p>minutes (00 à 59)</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>ss</p></td>
    <td align="left"><p>secondes (00 à 59)</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>uuu</p></td>
    <td align="left"><p>millisecondes (000 – 999)</p></td>
    </tr>
    </tbody>
    </table>

     

## Rubriques connexes


[Procédure pour configurer les paramètres de registre du client App-V Client à l'aide de la ligne de commande](how-to-configure-the-app-v-client-registry-settings-by-using-the-command-line.md)

 

 





