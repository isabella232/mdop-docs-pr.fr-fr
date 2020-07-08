---
title: Création d'une image Windows Virtual PC pour MED-V
description: Création d'une image Windows Virtual PC pour MED-V
author: dansimp
ms.assetid: fd7c0b1a-0769-4e7b-ad1a-dad19cca081f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: f947479776e84a4c54edb10d583dd21d7ccf6f43
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804411"
---
# Création d'une image Windows Virtual PC pour MED-V


Pour pouvoir livrer une entreprise MED-V aux utilisateurs, vous devez commencer par préparer un disque dur virtuel qui vous permet de générer le package d’installation de l’espace de travail MED-V pour la virtualisation de l’ordinateur de bureau Microsoft entreprise (MED-V) 2,0. Pour préparer le disque dur virtuel requis, vous devez créer une image de PC virtuel Windows qui contient le système d’exploitation, les mises à jour et le logiciel requis pour vous permettre de déployer plus tard les informations relatives à la redirection des applications et de la redirection d’URL vers les utilisateurs. Cette section fournit des recommandations sur la création du disque dur virtuel.

Pour créer une image virtuelle pour MED-V, vous devez suivre les étapes ci-dessous.

1.  [Créer une image de PC virtuel Windows](#bkmk-creatingavirtualmachinebyusingmicrosoftvirtualpc)

2.  [Installer Windows XP sur l’image](#bkmk-installingwindowsxpontovpc)

3.  [Installation de .NET Framework sur l’image](#bkmk-installingnet)

4.  [Appliquer des mises à jour à l’image](#bkmk-applypatchestovpc)

5.  [Installer les composants d’intégration](#bkmk-installintegration)

## <a href="" id="bkmk-creatingavirtualmachinebyusingmicrosoftvirtualpc"></a>Créer une image de PC virtuel Windows


Pour créer une image de PC virtuel Windows, consultez la documentation sur le PC virtuel Windows:

-   [Page d’accueil de l’ordinateur virtuel Windows](https://go.microsoft.com/fwlink/?LinkId=148103) ( https://go.microsoft.com/fwlink/?LinkId=148103) .

-   [Aide de l’application Virtual PC Windows](https://go.microsoft.com/fwlink/?LinkId=182378) ( https://go.microsoft.com/fwlink/?LinkId=182378) .

Par ailleurs, si vous disposez déjà d’un fichier d’image Windows (WIM) que vous souhaitez utiliser comme base pour votre image virtuelle, vous pouvez le convertir en VHD qui vous permet de créer l’espace de travail MED-V. Pour plus d’informations sur la façon de convertir un WIM vers un disque dur virtuel, voir [prise en charge native de VHD dans Windows 7](https://go.microsoft.com/fwlink/?LinkId=195922) ( https://go.microsoft.com/fwlink/?LinkId=195922) .

**Important**  MED-V ne prend en charge qu’un disque dur virtuel par ordinateur virtuel et une seule partition sur chaque disque virtuel.

 

Une fois que vous avez créé votre disque dur virtuel, installez Windows XP sur l’image.

## <a href="" id="bkmk-installingwindowsxpontovpc"></a>Installation de Windows XP sur une image de PC virtuel Windows


MED-V nécessite l’installation de Windows XP SP3 sur l’image du PC virtuel Windows avant de créer l’espace de travail MED-V.

Pour plus d’informations sur l’installation de Windows XP, voir [créer une machine virtuelle et installer un système d’exploitation invité](https://go.microsoft.com/fwlink/?LinkId=182379) ( https://go.microsoft.com/fwlink/?LinkId=182379) .

## <a href="" id="bkmk-installingnet"></a>Installation de .NET Framework 3,5 SP1 sur une image de PC virtuel Windows


Vous devez installer manuellement .NET Framework 3,5 SP1 et la mise à jour KB959209 dans l’image du PC virtuel Windows que vous préparez pour une utilisation avec MED-V. Le [KB959209](https://go.microsoft.com/fwlink/?LinkId=204950) de mise à jour ( https://go.microsoft.com/fwlink/?LinkId=204950) résout plusieurs problèmes de compatibilité d’application connus.

## <a href="" id="bkmk-applypatchestovpc"></a>Appliquer des mises à jour à l’image du PC virtuel Windows


Une fois que vous avez installé Windows XP sur votre machine virtuelle, installez les mises à jour Windows XP requises sur l’image, par exemple SP3. Vous pouvez également installer certaines mises à jour facultatives pour de meilleures performances.

**Important**  Pour MED-V, Windows XP SP3 doit être en cours d’exécution sur le système d’exploitation invité.

 

**Avertissement**  Lorsque vous installez les mises à jour apportées à Windows XP, assurez-vous de conserver la version d’Internet Explorer que vous envisagez d’utiliser dans l’espace de travail MED-V. Par exemple, si vous envisagez d’exécuter Internet Explorer 6 dans l’espace de travail MED-V, assurez-vous que les mises à jour que vous installez ne comprennent pas Internet Explorer 7 ou Internet Explorer 8. Par ailleurs, nous vous recommandons de configurer le registre pour empêcher les mises à jour automatiques de mettre à niveau Internet Explorer.

 

### Installation d’une mise à jour de performance facultative

Même s’il est facultatif, nous vous recommandons d’installer la mise à jour suivante pour [Hotfix KB972435](https://go.microsoft.com/fwlink/?LinkId=201077) ( https://go.microsoft.com/fwlink/?LinkId=201077) . Cette mise à jour améliore les performances des dossiers partagés dans une session de services Terminal Server:

**Remarques**  La mise à jour est publiquement disponible. Toutefois, vous pouvez être invité à accepter un contrat pour les services Microsoft. Suivez les invites sur les pages Web successives pour récupérer ce correctif.

 

### Configuration d’une mise à jour de performance de la stratégie de groupe

Par défaut, la stratégie de groupe est téléchargée sur un ordinateur à la fois. Cela entraîne des retards lorsque MED-V est joint au domaine. Pour améliorer les performances de la stratégie de groupe, définissez la valeur de clé de Registre suivante sur le registre:

Sous-clé de Registre: HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Winlogon

Entrée: BufferPolicyReads

Type: DWORD

Valeur : 1

## <a href="" id="bkmk-installintegration"></a>Installation des composants d’intégration


Windows Virtual PC inclut le package composants d’intégration. Cela fournit des fonctionnalités qui améliorent l’interaction entre l’environnement virtuel et l’ordinateur physique. Par exemple, le package composants d’intégration vous permet de déplacer votre souris entre l’hôte et les ordinateurs invités.

**Important**  MED-V nécessite l’installation du package composants d’intégration.

 

Lorsque vous configurez l’image virtuelle pour qu’elle fonctionne avec MED-V, vous devez installer manuellement le package composants d’intégration sur le système d’exploitation invité pour pouvoir accéder aux fonctionnalités d’intégration disponibles.

Pour plus d’informations sur l’installation et l’utilisation du package composants d’intégration, voir les rubriques suivantes:

-   [Installer ou mettre à niveau le package des composants d’intégration](https://go.microsoft.com/fwlink/?LinkId=195923) ( https://go.microsoft.com/fwlink/?LinkId=195923) .

-   [À propos des fonctionnalités d’intégration](https://go.microsoft.com/fwlink/?LinkId=195924) ( https://go.microsoft.com/fwlink/?LinkId=195924) .

### Installation de la mise à jour RemoteApp

Une fois que vous avez installé le package des composants d’intégration, vous êtes invité à installer la mise à jour suivante: «mise à jour pour Windows XP SP3 pour activer RemoteApp». Il s’agit d’un composant requis pour MED-V.

**Important**  Si vous n’êtes pas invité à installer la mise à jour RemoteApp, vous devez la télécharger et l’installer manuellement. Pour plus d’informations et des instructions sur la façon de télécharger cette mise à jour, voir [mise à jour pour Windows XP SP3 pour activer](https://go.microsoft.com/fwlink/?LinkId=195925) le programme RemoteApp ( https://go.microsoft.com/fwlink/?LinkId=195925) .

 

### Activation de l’application Bureau à distance

Par défaut, la version bureau à distance est activée une fois que vous avez installé le package composants d’intégration. Pour que MED-V soit opérationnel, assurez-vous que l’option Bureau à distance est activée et ne Répartissez aucune stratégie de groupe qui la désactive.

Pour plus d’informations sur l’activation du Bureau à distance, voir [activer ou désactiver le Bureau à distance](https://go.microsoft.com/fwlink/?LinkId=201162) https://go.microsoft.com/fwlink/?LinkId=201162) .

## Personnalisation d’Internet Explorer à l’aide du kit d’administration d’Internet Explorer


Si vous le souhaitez, vous pouvez utiliser le kit d’administration d’Internet Explorer pour personnaliser Internet Explorer sur le système d’exploitation invité. Pour plus d’informations, reportez-vous au [Guide de déploiement et au kit d’administration d’Internet Explorer 6](https://go.microsoft.com/fwlink/?LinkId=200007) (http://go.Microsoft.com/fwlink/?LinkId=200007).

**Avertissement**  Prenez en compte les problèmes liés à la sécurité liés à la personnalisation d’Internet Explorer dans l’espace de travail MED-V. Pour plus d’informations, consultez [meilleures pratiques en matière de sécurité pour les opérations MED-V](security-best-practices-for-med-v-operations.md).

 

Après l’installation de votre disque dur virtuel avec un système d’exploitation invité à jour, vous pouvez installer des applications sur l’image.

## Rubriques connexes


[Installation d'applications sur une image WindowsVirtualPC](installing-applications-on-a-windows-virtual-pc-image.md)

[Configuration d'une image Windows Virtual PC pour MED-V](configuring-a-windows-virtual-pc-image-for-med-v.md)

 

 





