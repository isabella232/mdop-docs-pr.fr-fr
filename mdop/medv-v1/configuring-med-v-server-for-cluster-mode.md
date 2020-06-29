---
title: Configuration de serveur MED-V pour le mode cluster
description: Configuration de serveur MED-V pour le mode cluster
author: dansimp
ms.assetid: 41f0b2a3-4ce9-48e1-a6fb-4c13c4228515
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ddb7dd5af65d8a465c5c1884bb27a3027621bac1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811922"
---
# Configuration de serveur MED-V pour le mode cluster


Vous pouvez configurer le serveur MED-V en mode cluster. En mode cluster, deux serveurs sont utilisés et tous les fichiers identifiés comme communs aux deux serveurs sont placés sur un système de fichiers. Le serveur accède aux fichiers à partir du système de fichiers plutôt qu’en stockant les fichiers localement.

## <a href="" id="bkmk-howtoconfigurethemedvserverinclustermode"></a>


**Pour configurer le serveur MED-V en mode cluster**

1.  Installez et configurez MED-V sur l’un des serveurs.

2.  Créez un réseau partagé dans un emplacement central accessible par tous les serveurs.

3.  Copiez le contenu du dossier * &lt; &gt; /Servers/ConfigurationServer de INSTALLDIR* sur le réseau partagé.

4.  Installez le serveur MED-V sur tous les serveurs désignés.

5.  Sur le réseau partagé, attribuez un accès total à tous les comptes système du serveur MED-V.

6.  Sur chaque serveur, procédez comme suit:

    1.  Dans le fichier de * &lt; ServerConfiguration.xmlde INSTALLDIR &gt; /Servers/* , définissez la valeur de * &lt; StorePath &gt; * sur le chemin réseau partagé.

    2.  Copiez le fichier * &lt; InstsallDir &gt; /Servers/KeyPair.xml* du serveur d’origine sur tous les serveurs MED-V.

    3.  Redémarrez le service MED-V.

**Remarques**  Si tous les serveurs ont les mêmes paramètres locaux (tels que les ports d’écoute, le serveur IIS, les autorisations de gestion, la base de données de rapports, etc.), le * &lt; ServerSettings.xmlde INSTALLDIR &gt; /Servers/* peut être partagé par tous les serveurs.

 

## Rubriques connexes


[Conception et planification de l'infrastructure de MED-V](med-v-infrastructure-planning-and-design.md)

 

 





