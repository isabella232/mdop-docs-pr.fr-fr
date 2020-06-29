---
title: Comment ajouter ou supprimer des informations de redirection des URL dans un espace de travail MED-V déployé
description: Comment ajouter ou supprimer des informations de redirection des URL dans un espace de travail MED-V déployé
author: dansimp
ms.assetid: bf55848d-bf77-452e-aaa5-4dd4868ff5bd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: f0892b16bfc10e6b3f28fe99c51c2c5cedb73d7f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811759"
---
# Comment ajouter ou supprimer des informations de redirection des URL dans un espace de travail MED-V déployé


Pour modifier les informations de redirection d’URL dans un espace de travail MED-V, nous vous recommandons de mettre à jour le Registre du système à l’aide d’une stratégie de groupe. Même si ce n’est pas le cas, vous pouvez également recréer et redéployer l’espace de travail MED-V avec les informations de redirection d’URL mises à jour.

La clé de Registre se trouve généralement sur:

Computer\\HKEY\ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\MEDV\\v2\\UserExperience

La valeur de chaîne multiple suivante doit être présente: `RedirectUrls`

Le champ données de la valeur pour `RedirectUrls` est une liste de l’ensemble des URL que vous avez spécifiées pour la redirection lors de la création du package d’espace de travail MED-v à l’aide du **Gestionnaire de package med-v**. Pour plus d’informations, voir [créer un package d’espace de travail MED-V](create-a-med-v-workspace-package.md).

Vous pouvez ajouter et supprimer des informations de redirection d’URL en effectuant l’une des tâches suivantes:

-   [Modifier la clé de registre de redirection d’URL et procéder au déploiement à l’aide d’une stratégie de groupe](#bkmk-editreg)

-   [Modifier le fichier texte de redirection d’URL et reconstruire l’espace de travail MED-V](#bkmk-edittext)

<a href="" id="bkmk-editreg"></a>**Pour mettre à jour les informations de redirection d’URL à l’aide d’une stratégie de groupe**

1.  Modifiez la valeur de la clé de Registre multichaîne nommée `RedirectUrls` . Cette valeur se trouve généralement sur:

    Computer\\HKEY\ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\MEDV\\v2\\UserExperience

    Si vous ajoutez des URL à la clé de Registre, entrez-les une par ligne, comme requis lors de la création du package d’espace de travail MED-V. Pour plus d’informations, voir [créer un package d’espace de travail MED-V](create-a-med-v-workspace-package.md).

2.  Déployez la clé de Registre mise à jour à l’aide d’une stratégie de groupe. Pour plus d’informations sur l’utilisation d’une stratégie de groupe, voir [installation de logiciels de stratégie de groupe](https://go.microsoft.com/fwlink/?LinkId=195931) ( https://go.microsoft.com/fwlink/?LinkId=195931) .

**Remarques**  Cette méthode de modification des informations de redirection d’URL est une meilleure pratique MED-V.

 

<a href="" id="bkmk-edittext"></a>**Pour recréer l’espace de travail MED-V en utilisant un fichier texte d’URL mis à jour**

-   Un autre moyen d’ajouter et de supprimer des URL de la liste de redirection consiste à mettre à jour le fichier texte de redirection d’URL et à l’utiliser pour créer un nouvel espace de travail MED-V. Vous pouvez ensuite redéployer l’espace de travail MED-V comme auparavant, à l’aide de votre processus de déploiement standard, tel qu’un système ESD.

    **Important**  Nous déconseillons cette méthode de modification des informations de redirection d’URL. De plus, à chaque fois que vous redéploiez l’espace de travail MED-V dans votre entreprise, la première fois que vous devez réexécuter le programme d’installation, toutes les données enregistrées dans l’ordinateur virtuel sont perdues.

     

## Rubriques connexes


[Comment tester la redirection d'URL](how-to-test-url-redirection.md)

[Gestion d'applications déployées sur les espaces de travail MED-V](managing-applications-deployed-to-med-v-workspaces.md)

[Créer un package d'espace de travail MED-V](create-a-med-v-workspace-package.md)

 

 





