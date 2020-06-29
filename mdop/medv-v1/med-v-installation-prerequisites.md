---
title: Composants requis pour l'installation de MED-V
description: Composants requis pour l'installation de MED-V
author: dansimp
ms.assetid: cf3c0906-23eb-4c4a-8951-a65741720f95
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 2b432b8c2b06e171eb339aab6c7b15efb20d5919
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810872"
---
# Composants requis pour l'installation de MED-V


Vous trouverez ci-après les conditions préalables à l’installation de MED-V:

[Configuration requise pour Active Directory](#bkmk-activedirectoryrequirements)

[Rapport de base de données](#bkmk-howtoinstallthereportdatabase)

[Configuration de logiciels antivirus/de sauvegarde](#bkmk-antivirusbackupsoftwareconfiguration)

[Microsoft Virtual PC 2007 SP1](#bkmk-howtoinstallandconfiguremicrosoftvirtualpc2007sp1)

## <a href="" id="bkmk-activedirectoryrequirements"></a>Configuration requise pour Active Directory


Lors de la configuration du serveur MED-V, si les utilisateurs ne font pas partie du même domaine auquel le serveur appartient, une approbation doit être définie entre les domaines.

## <a href="" id="bkmk-howtoinstallthereportdatabase"></a>Comment installer la base de données de rapport


La base de données de rapports est nécessaire pour stocker tous les journaux d’espace de travail MED-V. La base de données journal est alors utilisée pour générer des rapports MED-V. Pour plus d’informations sur les rapports, voir [création de rapports MED-V](med-v-reporting.md).

SQL Server peut être installé sur le même serveur que le serveur MED-V ou sur un serveur distant. Si vous effectuez une installation sur un serveur distant, reportez-vous à la rubrique [installation de SQL Server sur un serveur distant](#bkmk-installingsqlserveronaremoteserver).

### <a href="" id="bkmk-installingsqlserveronaremoteserver"></a>Installation de SQL Server sur un serveur distant

**Pour installer SQL Server sur un serveur distant**

1.  Configurez les éléments suivants sur le serveur distant:

    -   Nom de l’instance: instance par défaut

    -   Mode d’authentification: mode mixte

    -   Utilisateur: l’utilisateur créé par défaut est «sa».

    -   Mot de passe: mot de passe souhaité

    -   Paramètres d’assemblage (par défaut)

    -   Erreur dans les paramètres des rapports d’utilisation (par défaut)

2.  Installez les fichiers suivants sur le serveur MED-V:

    -   Pour installer la configuration requise pour la collection d’objets du pack d’administration pour Microsoft SQL Server 2008, téléchargez le [client natif Microsoft SQL Server 2008](https://go.microsoft.com/fwlink/?LinkId=164039) à partir du centre de téléchargement Microsoft.

    -   Pour installer la configuration requise pour la collection d’objets du pack d’administration pour Microsoft SQL Server2005, téléchargez le [client natif Microsoft SQL Server2005](https://go.microsoft.com/fwlink/?LinkId=164038) à partir du centre de téléchargement Microsoft.

    -   Pour installer les fichiers dll requis pour Microsoft SQL Server 2008, téléchargez la [collection Microsoft SQL Server 2008 Management Objects](https://go.microsoft.com/fwlink/?LinkId=164041) à partir du centre de téléchargement Microsoft.

    -   Pour installer les fichiers dll requis pour Microsoft SQL Server2005, téléchargez [Microsoft SQL Server2005 Management Objects](https://go.microsoft.com/fwlink/?LinkId=164040) à partir du centre de téléchargement Microsoft.

    -   Pour installer les packages d’installation autonomes qui fournissent des valeurs supplémentaires pour SQL Server 2008, téléchargez le [Feature Pack Microsoft SQL Server 2008](https://go.microsoft.com/fwlink/?LinkId=163960) à partir du centre de téléchargement Microsoft.

    -   Pour installer les packages d’installation autonomes qui fournissent des valeurs supplémentaires pour SQL Server2005, téléchargez le [Pack de fonctionnalités pour Microsoft SQL Server2005]( https://go.microsoft.com/fwlink/?LinkId=163961) à partir du centre de téléchargement Microsoft.

    Pour plus d’informations sur ces fichiers, voir [module de fonctionnalités Microsoft SQL Server 2008](https://go.microsoft.com/fwlink/?LinkId=163960) sur le centre de téléchargement Microsoft ( https://go.microsoft.com/fwlink/?LinkId=163960) ou [Feature Pack pour Microsoft SQL Server2005](https://go.microsoft.com/fwlink/?LinkId=163961) sur le centre de téléchargement Microsoft ( https://go.microsoft.com/fwlink/?LinkId=163961) .

## <a href="" id="bkmk-antivirusbackupsoftwareconfiguration"></a>Configuration de logiciels antivirus/de sauvegarde


Pour empêcher les activités de protection antivirus d’affecter les performances de la version de bureau virtuelle, il est recommandé, dans la mesure du possible, d’exclure les types de fichiers d’ordinateur virtuel suivants de tout logiciel antivirus ou de processus de sauvegarde exécuté sur l’hôte:

-   \*. COMPATIBLE

-   \*. VUD

-   \*. VSV

-   \*. CKM

-   \*. EVHD

## <a href="" id="bkmk-howtoinstallandconfiguremicrosoftvirtualpc2007sp1"></a>Installer et configurer Microsoft Virtual PC2007 SP1


**Important**  S’il existe le PC virtuel pour Windows sur l’ordinateur hôte, désinstallez-le avant d’installer Virtual PC2007 SP1.

 

**Pour installer Microsoft Virtual PC2007 SP1**

1.  Téléchargez Virtual PC2007 SP1 à partir du centre de téléchargement Microsoft [Virtual PC 2007 SP1](https://go.microsoft.com/fwlink/?LinkId=142994).

2.  Exécutez le fichier d’installation sur l’ordinateur hôte, puis suivez l’Assistant.

3.  Installez la mise à jour virtuelle de PC2007 SP1 sur l’ordinateur hôte en mode d’élévation.

    Pour plus d’informations, reportez-vous à [la description du package de correctif logiciel pour Virtual PC 2007 SP1](https://go.microsoft.com/fwlink/?LinkId=150575).

    **Remarques**  La mise à jour virtuelle PC2007 SP1 est nécessaire pour exécuter Virtual PC2007 SP1.

     

## Rubriques connexes


[Configurations prises en charge](supported-configurationsmedv-orientation.md)

 

 





