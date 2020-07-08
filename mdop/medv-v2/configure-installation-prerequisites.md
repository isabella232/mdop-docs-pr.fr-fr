---
title: Configurer les composants requis pour l'installation
description: Configurer les composants requis pour l'installation
author: dansimp
ms.assetid: ff9cf28a-3eac-4b6c-8ce9-bfc202f57947
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 6cd9379804c45a2025064a6eecf363c010980369
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807854"
---
# Configurer les composants requis pour l'installation


Les instructions suivantes sont les conditions préalables à l’installation et à l’utilisation de Microsoft Enterprise Desktop Virtualization (MED-V) 2,0:

[PC virtuel Windows](#bkmk-howtoinstallandconfiguremicrosoftvirtualpc7)

[Mise à jour de Windows Virtual PC](#bkmk-howtoinstallandconfiguremicrosoftvirtualpc7update)

[Configuration de logiciels antivirus/de sauvegarde](#bkmk-antivirusbackupsoftwareconfiguration)

## <a href="" id="bkmk-howtoinstallandconfiguremicrosoftvirtualpc7"></a>Installer et configurer l’ordinateur virtuel Windows


**Important**  S’il existe déjà une version de Virtual PC pour Windows sur l’ordinateur hôte, vous devez la désinstaller avant d’installer le PC virtuel Windows.

 

**Pour installer l’ordinateur virtuel Windows**

1.  Téléchargez le [PC virtuel Windows](https://go.microsoft.com/fwlink/?LinkId=195918) à partir du centre de téléchargement Microsoft ( https://go.microsoft.com/fwlink/?LinkId=195918) .

2.  Exécutez le fichier d’installation sur l’ordinateur hôte, puis suivez les étapes de l’Assistant.

**Important**  Windows Virtual PC inclut le package composants d’intégration, qui fournit des fonctionnalités qui améliorent l’interaction entre l’environnement virtuel et l’ordinateur physique. Par exemple, il permet de déplacer la souris entre l’hôte et les ordinateurs invités. MED-V nécessite l’installation du package composants d’intégration.

 

## <a href="" id="bkmk-howtoinstallandconfiguremicrosoftvirtualpc7update"></a>Installation et configuration de la mise à jour de Windows Virtual PC


La mise à jour Microsoft associée à l’article KB977206 permet le mode Windows XP pour les ordinateurs sans technologie HAV. Nous vous recommandons d’installer cette mise à jour, car il est possible que certaines fonctionnalités d’intégration ne fonctionnent pas correctement si le package composants d’intégration du système d’exploitation invité ne correspond pas à la version de PC virtuel Windows installée sur l’ordinateur hôte.

**Important**  Vous n’avez pas besoin d’installer cette mise à jour lorsque vous installez MED-V sur des ordinateurs hôtes exécutant Windows 7 avec Service Pack 1.

 

**Astuce**  Outre la mise à jour répertoriée ici, nous vous conseillons de passer en revue toutes les mises à jour de PC virtuelles Windows disponibles et d’appliquer les mises à jour appropriées ou nécessaires pour votre environnement.

 

**Pour installer la mise à jour de Windows Virtual PC**

1.  Téléchargez la mise à jour de PC virtuel Windows requise à partir du centre de téléchargement Microsoft.

    [mise à jour 32 bits](https://go.microsoft.com/fwlink/?LinkId=195919) ( https://go.microsoft.com/fwlink/?LinkId=195919) .

    [mise à jour 64 bits](https://go.microsoft.com/fwlink/?LinkId=195920) ( https://go.microsoft.com/fwlink/?LinkId=195920) .

2.  Exécutez le fichier d’installation sur l’ordinateur hôte en mode avec élévation de privilèges, puis suivez les étapes de l’Assistant.

    Pour plus d’informations sur le correctif logiciel pour PC virtuel Windows, voir [l’article 977206](https://go.microsoft.com/fwlink/?LinkId=195921) ( https://go.microsoft.com/fwlink/?LinkId=195921) .

## <a href="" id="bkmk-antivirusbackupsoftwareconfiguration"></a>Comment configurer un logiciel antivirus/de sauvegarde


Pour empêcher les activités de protection antivirus d’affecter les performances de la version de bureau virtuelle, nous vous conseillons, par exemple, d’exclure les types de fichiers d’ordinateur virtuel suivants de tout logiciel antivirus ou de processus de sauvegarde qui s’exécute sur l’ordinateur hôte:

-   \*. COMPATIBLE

-   \*. VUD

-   \*. VSV

-   \*. VIRTUELS

## Rubriques connexes


[Configurer la configuration requise de l'environnement](configure-environment-prerequisites.md)

[Architecture de haut niveau](high-level-architecturemedv2.md)

[Configurations prises en charge par MED-V2.0](med-v-20-supported-configurations.md)

 

 





