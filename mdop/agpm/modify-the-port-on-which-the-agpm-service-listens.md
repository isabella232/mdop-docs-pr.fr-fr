---
title: Modifier le port sur lequel le service AGPM écoute
description: Modifier le port sur lequel le service AGPM écoute
author: dansimp
ms.assetid: a82c6873-e916-4a04-b263-aa612cd6956b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c2af79ecb9bd05acbc55083163903ae14ab44d06
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808326"
---
# <span data-ttu-id="eb553-103">Modifier le port sur lequel le service AGPM écoute</span><span class="sxs-lookup"><span data-stu-id="eb553-103">Modify the Port on Which the AGPM Service Listens</span></span>


<span data-ttu-id="eb553-104">Le service AGPM est un service Windows agissant en tant que proxy de sécurité, gérant l’accès client aux objets de stratégie de groupe (GPO) dans l’environnement d’archivage et de production.</span><span class="sxs-lookup"><span data-stu-id="eb553-104">The AGPM Service is a Windows service that acts as a security proxy, managing client access to Group Policy objects (GPOs) in the archive and production environment.</span></span> <span data-ttu-id="eb553-105">Par défaut, le service AGPM écoute sur le port 4600.</span><span class="sxs-lookup"><span data-stu-id="eb553-105">By default, the AGPM Service listens on port 4600.</span></span> <span data-ttu-id="eb553-106">Vous pouvez modifier ce port en modifiant le fichier d’index d’archive Advanced Group Policy Management (AGPM) pour chaque archive.</span><span class="sxs-lookup"><span data-stu-id="eb553-106">You can change this port by modifying the Advanced Group Policy Management (AGPM) archive index file for each archive.</span></span>

<span data-ttu-id="eb553-107">**Remarques**  Avant de modifier le port que le service AGPM écoute, il est recommandé de sauvegarder le fichier d’index d’archive AGPM (gpostate.xml).</span><span class="sxs-lookup"><span data-stu-id="eb553-107">**Note** Before modifying the port on which the AGPM Service listens, it is recommended that you back up the AGPM archive index file (gpostate.xml).</span></span> <span data-ttu-id="eb553-108">Ce fichier se trouve dans le dossier entré comme chemin d’accès d’archive au cours de l’installation de gestion de la stratégie de groupe avancée-serveur.</span><span class="sxs-lookup"><span data-stu-id="eb553-108">This file is located in the folder entered as the archive path during the installation of Advanced Group Policy Management - Server.</span></span> <span data-ttu-id="eb553-109">Par défaut, cet emplacement de ce fichier est% CommonAppData% \\Microsoft\\AGPM\\gpostate.xml sur le serveur AGPM.</span><span class="sxs-lookup"><span data-stu-id="eb553-109">By default, this location of this file is %CommonAppData%\\Microsoft\\AGPM\\gpostate.xml on the AGPM Server.</span></span> <span data-ttu-id="eb553-110">Si vous ne savez pas quel ordinateur héberge l’archive, vous pouvez suivre la procédure de modification du chemin d’accès de l’Archive pour afficher le chemin d’accès actuel.</span><span class="sxs-lookup"><span data-stu-id="eb553-110">If you do not know which computer hosts the archive, you can follow the procedure for modifying the archive path to display the current archive path.</span></span> <span data-ttu-id="eb553-111">Pour plus d’informations, voir [modifier le chemin d’accès d’archive](modify-the-archive-path.md).</span><span class="sxs-lookup"><span data-stu-id="eb553-111">For more information, see [Modify the Archive Path](modify-the-archive-path.md).</span></span>

 

<span data-ttu-id="eb553-112">Un compte d’utilisateur ayant accès au serveur AGPM (l’ordinateur sur lequel est installé le service AGPM) et au fichier d’index d’archive est requis pour effectuer cette procédure.</span><span class="sxs-lookup"><span data-stu-id="eb553-112">A user account with access to the AGPM Server (the computer on which the AGPM Service is installed) and the archive index file is required to complete this procedure.</span></span>

**<span data-ttu-id="eb553-113">Pour modifier le port que le service AGPM écoute</span><span class="sxs-lookup"><span data-stu-id="eb553-113">To modify the port on which the AGPM Service listens</span></span>**

1.  <span data-ttu-id="eb553-114">Sur l’ordinateur hébergeant l’archive, ouvrez le fichier d’index d’archive (gpostate.xml) dans un éditeur de texte.</span><span class="sxs-lookup"><span data-stu-id="eb553-114">On the computer hosting the archive, open the archive index file (gpostate.xml) in a text editor.</span></span>

2.  <span data-ttu-id="eb553-115">Dans le fichier, recherchez **AGPM: port = «4600»**.</span><span class="sxs-lookup"><span data-stu-id="eb553-115">In the file, search for **agpm:port="4600"**.</span></span>

3.  <span data-ttu-id="eb553-116">Remplacez **4600** par le port sur lequel le service AGPM doit écouter; Enregistrez et fermez le fichier.</span><span class="sxs-lookup"><span data-stu-id="eb553-116">Replace **4600** with the port on which the AGPM Service should listen; then, save and close the file.</span></span>

4.  <span data-ttu-id="eb553-117">Sur le serveur AGPM, redémarrez le service AGPM.</span><span class="sxs-lookup"><span data-stu-id="eb553-117">On the AGPM Server, restart the AGPM Service.</span></span> <span data-ttu-id="eb553-118">(Pour plus d’informations, reportez-vous à [Démarrer et arrêter le service AGPM](start-and-stop-the-agpm-service.md).)</span><span class="sxs-lookup"><span data-stu-id="eb553-118">(For more information, see [Start and Stop the AGPM Service](start-and-stop-the-agpm-service.md).)</span></span>

5.  <span data-ttu-id="eb553-119">Modifiez le port dans la connexion de serveur AGPM pour chaque administrateur de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="eb553-119">Modify the port in the AGPM Server connection for each Group Policy administrator.</span></span> <span data-ttu-id="eb553-120">(Pour plus d’informations, voir [configurer la connexion à un serveur AGPM](configure-the-agpm-server-connection.md).)</span><span class="sxs-lookup"><span data-stu-id="eb553-120">(For more information, see [Configure the AGPM Server Connection](configure-the-agpm-server-connection.md).)</span></span>

6.  <span data-ttu-id="eb553-121">Répétez cette procédure pour chaque archive et serveur AGPM.</span><span class="sxs-lookup"><span data-stu-id="eb553-121">Repeat for each archive and AGPM Server.</span></span>

### <span data-ttu-id="eb553-122">Références supplémentaires</span><span class="sxs-lookup"><span data-stu-id="eb553-122">Additional references</span></span>

-   [<span data-ttu-id="eb553-123">Gestion du service AGPM</span><span class="sxs-lookup"><span data-stu-id="eb553-123">Managing the AGPM Service</span></span>](managing-the-agpm-service.md)

 

 





