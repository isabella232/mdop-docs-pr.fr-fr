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
# <span data-ttu-id="b0866-103">Configuration de serveur MED-V pour le mode cluster</span><span class="sxs-lookup"><span data-stu-id="b0866-103">Configuring MED-V Server for Cluster Mode</span></span>


<span data-ttu-id="b0866-104">Vous pouvez configurer le serveur MED-V en mode cluster.</span><span class="sxs-lookup"><span data-stu-id="b0866-104">You can configure the MED-V server in cluster mode.</span></span> <span data-ttu-id="b0866-105">En mode cluster, deux serveurs sont utilisés et tous les fichiers identifiés comme communs aux deux serveurs sont placés sur un système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="b0866-105">In cluster mode, two servers are used and all files identified as mutual to both servers are placed on a file system.</span></span> <span data-ttu-id="b0866-106">Le serveur accède aux fichiers à partir du système de fichiers plutôt qu’en stockant les fichiers localement.</span><span class="sxs-lookup"><span data-stu-id="b0866-106">The server accesses the files from the file system rather than storing the files locally.</span></span>

## <a href="" id="bkmk-howtoconfigurethemedvserverinclustermode"></a>


**<span data-ttu-id="b0866-107">Pour configurer le serveur MED-V en mode cluster</span><span class="sxs-lookup"><span data-stu-id="b0866-107">To configure the MED-V server in cluster mode</span></span>**

1.  <span data-ttu-id="b0866-108">Installez et configurez MED-V sur l’un des serveurs.</span><span class="sxs-lookup"><span data-stu-id="b0866-108">Install and configure MED-V on one of the servers.</span></span>

2.  <span data-ttu-id="b0866-109">Créez un réseau partagé dans un emplacement central accessible par tous les serveurs.</span><span class="sxs-lookup"><span data-stu-id="b0866-109">Create a shared network in a central location where all of the servers can access it.</span></span>

3.  <span data-ttu-id="b0866-110">Copiez le contenu du dossier \* &lt; &gt; /Servers/ConfigurationServer de INSTALLDIR\* sur le réseau partagé.</span><span class="sxs-lookup"><span data-stu-id="b0866-110">Copy the contents of the *&lt;InstallDir&gt;/Servers/ConfigurationServer* folder to the shared network.</span></span>

4.  <span data-ttu-id="b0866-111">Installez le serveur MED-V sur tous les serveurs désignés.</span><span class="sxs-lookup"><span data-stu-id="b0866-111">Install MED-V server on all designated servers.</span></span>

5.  <span data-ttu-id="b0866-112">Sur le réseau partagé, attribuez un accès total à tous les comptes système du serveur MED-V.</span><span class="sxs-lookup"><span data-stu-id="b0866-112">On the shared network, assign full access to all MED-V server system accounts.</span></span>

6.  <span data-ttu-id="b0866-113">Sur chaque serveur, procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="b0866-113">On each server, do the following:</span></span>

    1.  <span data-ttu-id="b0866-114">Dans le fichier de \* &lt; ServerConfiguration.xmlde INSTALLDIR &gt; /Servers/\* , définissez la valeur de \* &lt; StorePath &gt; \* sur le chemin réseau partagé.</span><span class="sxs-lookup"><span data-stu-id="b0866-114">In the *&lt;InstallDir&gt;/Servers/ServerConfiguration.xml* file, set the value of *&lt;StorePath&gt;* to the shared network path.</span></span>

    2.  <span data-ttu-id="b0866-115">Copiez le fichier \* &lt; InstsallDir &gt; /Servers/KeyPair.xml\* du serveur d’origine sur tous les serveurs MED-V.</span><span class="sxs-lookup"><span data-stu-id="b0866-115">Copy the *&lt;InstsallDir&gt;/Servers/KeyPair.xml* file from the original server to all MED-V servers.</span></span>

    3.  <span data-ttu-id="b0866-116">Redémarrez le service MED-V.</span><span class="sxs-lookup"><span data-stu-id="b0866-116">Restart the MED-V service.</span></span>

<span data-ttu-id="b0866-117">**Remarques**  Si tous les serveurs ont les mêmes paramètres locaux (tels que les ports d’écoute, le serveur IIS, les autorisations de gestion, la base de données de rapports, etc.), le \* &lt; ServerSettings.xmlde INSTALLDIR &gt; /Servers/\* peut être partagé par tous les serveurs.</span><span class="sxs-lookup"><span data-stu-id="b0866-117">**Note** If all servers have the same local settings (such as listening ports, IIS server, management permissions, report database, and so on), the *&lt;InstallDir&gt;/Servers/ServerSettings.xml* can be shared by all servers as well.</span></span>

 

## <span data-ttu-id="b0866-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b0866-118">Related topics</span></span>


[<span data-ttu-id="b0866-119">Conception et planification de l'infrastructure de MED-V</span><span class="sxs-lookup"><span data-stu-id="b0866-119">MED-V Infrastructure Planning and Design</span></span>](med-v-infrastructure-planning-and-design.md)

 

 





