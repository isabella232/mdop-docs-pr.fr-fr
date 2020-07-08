---
title: Localisation de l'instruction «HelpdeskText» qui oriente les utilisateurs vers des informations supplémentaires sur le portail libre-service
description: Localisation de l'instruction «HelpdeskText» qui oriente les utilisateurs vers des informations supplémentaires sur le portail libre-service
author: dansimp
ms.assetid: 09ba2a07-3186-45d9-adef-4034c70ae7cf
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 2367424185da813a46fa52f3614c03083864f75f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809947"
---
# Localisation de l'instruction «HelpdeskText» qui oriente les utilisateurs vers des informations supplémentaires sur le portail libre-service


Vous pouvez configurer une version localisée de la déclaration «HelpdeskText» du portail libre-service, qui informe les utilisateurs finaux sur la manière d’obtenir de l’aide supplémentaire lors de l’utilisation du portail libre-service. Si vous configurez du texte localisé pour l’instruction, comme décrit dans les instructions ci-dessous, MBAM affiche la version localisée. Si MBAM ne trouve pas la version localisée, il affiche la valeur figurant dans le paramètre **HelpdeskText** .

**Remarques**  Dans les instructions ci-dessous, *selfservice* est le nom de répertoire virtuel par défaut du portail libre-service. Vous avez peut-être déjà utilisé un autre nom lorsque vous avez configuré le portail libre-service.

 

**Pour afficher une version localisée de l’instruction HelpdeskText**

1.  Sur le serveur sur lequel vous avez configuré le portail libre-service, accédez à **sites** &gt; **Microsoft BitLocker administration et analyse des paramètres de** l' &gt; **SelfService** &gt; **application**selfservice.

2.  Dans le volet **actions** , cliquez sur **Ajouter** pour ouvrir la boîte de dialogue Ajouter un **paramètre d’application** .

3.  Dans le champ **nom** , tapez **HelpdeskText**\ _ &lt; *Language* &gt; , où &lt; *Language* &gt; correspond au code de langue approprié pour le texte.

    Par exemple, pour créer une instruction HelpdeskText localisée en espagnol, nommez le paramètre **HelpdeskText \ _es-es**.

    Le nom du dossier Language peut également être le nom neutre des langues **au lieu** de **es-es**. Si le navigateur de l’utilisateur final est défini sur **es-es** et que ce dossier n’existe pas, les paramètres régionaux du parent (tels qu’ils sont définis dans .net) sont récupérés et activés de manière récursive, ce qui a\\SelfServiceWebsite\\es\\Notice.txt pour effet d’arrêter &lt; &gt; le fichier de Notice.txt par défaut. Cette substitution récursive imite les règles de chargement des ressources .NET.

    Pour obtenir la liste des codes de langue valides que vous pouvez utiliser, voir référence sur l' [API NLS (National Language Support)](https://go.microsoft.com/fwlink/?LinkId=317947).

4.  Dans le champ **valeur** , tapez le texte localisé que vous souhaitez afficher aux utilisateurs finaux.



## Rubriques connexes


[Personnalisation du portail libre-service de votre organisation](customizing-the-self-service-portal-for-your-organization.md)

 

 

## Vous avez une suggestion pour MBAM?
- Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring) 
- Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).



