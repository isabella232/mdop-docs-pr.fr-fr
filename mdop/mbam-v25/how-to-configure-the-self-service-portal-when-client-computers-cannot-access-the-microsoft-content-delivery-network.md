---
title: Comment configurer le portail libre-service lorsque les ordinateurs clients ne peuvent pas accéder au réseau de distribution de contenu Microsoft
description: Comment configurer le portail libre-service lorsque les ordinateurs clients ne peuvent pas accéder au réseau de distribution de contenu Microsoft
author: dansimp
ms.assetid: 90ee76db-9876-41b5-994a-118556d5ed3b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ffce3dd023cb6ff9bd5cdb13ea789b348661de24
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810589"
---
# Comment configurer le portail libre-service lorsque les ordinateurs clients ne peuvent pas accéder au réseau de distribution de contenu Microsoft


Suivez ces instructions si les ordinateurs clients de votre organisation n’ont pas accès au réseau de distribution de contenu (CDN) Microsoft Ajax.

**Pourquoi devez-vous configurer:**

Vos ordinateurs clients doivent avoir accès au réseau de distribution de contenu (CDN), ce qui donne au portail libre-service l’accès requis à certains fichiers JavaScript. Si vous ne configurez pas le portail libre-service lorsque les ordinateurs clients ne peuvent pas accéder au CDN, seul le nom de la société et le compte sous lequel l’utilisateur final se connecte s’affiche. Aucun message d’erreur ne s’affichera.

**Remarques**  Dans MBAM 2,5 SP1, les fichiers JavaScript sont inclus dans le produit, et vous n’avez pas besoin de suivre les instructions de cette section pour configurer le SSP pour la prise en charge des clients qui ne peuvent pas accéder à Internet.

 

**Configuration du portail libre-service lorsque les ordinateurs clients ne peuvent pas accéder au CDN**

1. Téléchargez les fichiers JavaScript suivants à partir du réseau de distribution de contenu (CDN):

   -   [jQuery-1.10.2.min.js](https://go.microsoft.com/fwlink/?LinkID=390515)

   -   [jQuery.validate.min.js](https://go.microsoft.com/fwlink/?LinkID=390516)

   -   [jQuery.validate.unobtrusive.min.js](https://go.microsoft.com/fwlink/?LinkID=390517)

2. Copiez les fichiers JavaScript dans le répertoire **scripts** du portail libre-service. Ce répertoire se trouve dans <em> &lt; MBAM répertoire d’installation de self-service &gt; \\ </em> Website\\Scripts.

3. Ouvrez le gestionnaire des services Internet (IIS).

4. Développez **sites** &gt; **Microsoft et surveillance de BitLocker**et mettez en surbrillance **selfservice**.

   **Remarque**  
   *Selfservice* est le nom de répertoire virtuel par défaut. Si vous avez choisi un autre nom pour ce répertoire lors de la configuration, n’oubliez pas de remplacer *selfservice* dans ces instructions par le nom que vous avez choisi.

     

5. Dans le volet du milieu, double-cliquez sur paramètres de l' **application**.

6. Pour chaque élément de la liste ci-dessous, modifiez les paramètres de l’application pour référencer le nouvel emplacement par remplacement/ &lt; *répertoire virtuel* &gt; /à l’aide de/selfservice/(ou du nom que vous avez choisi lors de la configuration). Par exemple, le chemin d’accès du répertoire virtuel est semblable à/selfservice/Scripts/jQuery-1.10.2.min.js.

   -   jQueryPath:/ &lt; *répertoire virtuel* &gt; /scripts/jQuery-1.10.2.min.js

   -   jQueryValidatePath:/ &lt; *répertoire virtuel* &gt; /scripts/jQuery.validate.min.js

   -   jQueryValidateUnobtrusivePath:/ &lt; *répertoire virtuel* &gt; /scripts/jQuery.validate.unobtrusive.min.js



## Rubriques connexes


[Comment configurer les applications Web MBAM2.5](how-to-configure-the-mbam-25-web-applications.md)

 

## Vous avez une suggestion pour MBAM?
- Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring) 
- Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





