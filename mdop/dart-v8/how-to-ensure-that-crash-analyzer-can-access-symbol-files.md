---
title: Procédure pour s'assurer que l'Analyseur d'incident puisse accéder aux fichiers de symboles
description: Procédure pour s'assurer que l'Analyseur d'incident puisse accéder aux fichiers de symboles
author: dansimp
ms.assetid: 99839013-1cd8-44d1-8484-0e15261c5a4b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 944198b95528a548acbe1229f9f3aad4c224af29
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808628"
---
# Procédure pour s'assurer que l'Analyseur d'incident puisse accéder aux fichiers de symboles


En général, les informations de débogage sont stockées dans un fichier de symboles différent du programme. Vous devez avoir accès aux informations de symbole lors du débogage d’une application qui a cessé de répondre.

Les fichiers de symboles sont automatiquement téléchargés lors de l’exécution de l' **analyseur d’incidents**. Si votre ordinateur n’est pas connecté à Internet ou si le réseau nécessite que l’ordinateur accède à un serveur proxy HTTP, les fichiers de symboles ne peuvent pas être téléchargés.

**Pour vous assurer que l’analyseur d’incidents peut accéder aux fichiers de symboles**

1.  **Copiez le fichier de vidage sur un autre ordinateur.** Si les symboles ne peuvent pas être téléchargés en raison d’un manque de connexion Internet, copiez le fichier de vidage de mémoire sur un ordinateur qui dispose d’une connexion Internet et exécutez l' **Assistant analyseur de blocage** autonome sur cet ordinateur.

2.  **Accéder aux fichiers de symboles à partir d’un autre ordinateur.** Si les symboles ne peuvent pas être téléchargés en raison d’un manque de connexion Internet, vous pouvez télécharger les symboles à partir d’un ordinateur qui dispose d’une connexion Internet, puis les copier sur l’ordinateur qui ne dispose pas d’une connexion Internet, ou vous pouvez mapper un lecteur réseau à un emplacement où les symboles sont disponibles sur le réseau local. Si vous exécutez l' **Analyseur de blocage** dans un environnement de récupération Windows (WindowsRE), vous pouvez inclure les fichiers de symboles dans l’image de récupération de l’outils de diagnostics et de récupération Microsoft (DaRT) 8,0.

3.  **Accéder aux fichiers de symboles par le biais d’un serveur proxy HTTP.** Si les symboles ne peuvent pas être téléchargés, car le serveur proxy HTTP doit être accessible, procédez comme suit pour accéder à un serveur proxy HTTP. Dans DaRT 8,0, l' **Assistant analyse de blocage** dispose d’un paramètre disponible dans la boîte de dialogue **spécifier l’emplacement des fichiers de symboles** , marquée avec le serveur proxy d’étiquette **(facultatif, en utilisant le format «serveur: port»)**. Vous pouvez utiliser cette zone de texte pour spécifier un serveur proxy. Entrez l’adresse de proxy sous la forme nom d' ** &lt; hôte &gt; : &lt; port &gt; **, où le nom d' &lt; **hôte** &gt; est un nom DNS ou une adresse IP et le &lt; **port** &gt; est un numéro de port TCP, généralement 80. Il existe deux modes dans lesquels l' **Analyseur de blocage** peut être exécuté. Vous trouverez ci-après l’utilisation du paramètre proxy dans chacun de ces modes:

    -   **Mode en ligne:** Dans ce mode, si le champ serveur proxy est vide, l’Assistant utilise les paramètres du proxy disponibles dans les options Internet du panneau de configuration. Si vous entrez une adresse de proxy dans la zone de texte fournie, l’adresse est utilisée et remplace le paramètre dans les options Internet.

    -   Environnement de récupération Windows (WindowsRE): lorsque vous exécutez l' **analyseur d’incidents** à partir de la fenêtre du **jeu d’outils de diagnostics et de récupération** , il n’existe pas d’adresse proxy par défaut. Si l’ordinateur est connecté directement à Internet, une adresse de proxy n’est pas requise. Par conséquent, vous pouvez laisser ce champ vide dans les paramètres de l’Assistant. Si l’ordinateur n’est pas connecté à Internet et qu’il se trouve dans un environnement réseau doté d’un serveur proxy, vous devez définir le champ proxy dans l’Assistant pour accéder au magasin de symboles. Vous pouvez obtenir l’adresse proxy auprès de l’administrateur réseau. Le paramétrage du serveur proxy est important uniquement lorsque le magasin de symboles publics est connecté à Internet. Si les symboles sont déjà présents sur l’image de récupération DaRT ou s’ils sont disponibles localement, la configuration du serveur proxy n’est pas requise.

## Rubriques connexes


[Diagnostic d'échecs du système avec l'Analyseur d'incident](diagnosing-system-failures-with-crash-analyzer--dart-8.md)

[Opérations de DaRT8.0](operations-for-dart-80-dart-8.md)

 

 





