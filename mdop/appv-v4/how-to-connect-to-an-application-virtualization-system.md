---
title: Procédure pour se connecter à un système Application Virtualization
description: Procédure pour se connecter à un système Application Virtualization
author: dansimp
ms.assetid: ac38216c-5464-4c0b-a4d3-3949ba6358ac
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 30d60e187e1b7595fd0dce6641fa027a1df68f3d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807217"
---
# <span data-ttu-id="bd767-103">Procédure pour se connecter à un système Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="bd767-103">How to Connect to an Application Virtualization System</span></span>


<span data-ttu-id="bd767-104">Pour pouvoir utiliser la console de gestion pour gérer des applications, des associations de types de fichiers, des packages, des licences d’application, des groupes de serveurs, des stratégies de fournisseur et des administrateurs, vous devez connecter la console de gestion du serveur d’applications.</span><span class="sxs-lookup"><span data-stu-id="bd767-104">You must connect the Application Virtualization Server Management Console to an Application Virtualization System before you can use the management console to manage applications, file type associations, packages, application licenses, server groups, provider policies and administrators.</span></span> <span data-ttu-id="bd767-105">La procédure suivante décrit les étapes à suivre pour connecter la console à un système de virtualisation des applications.</span><span class="sxs-lookup"><span data-stu-id="bd767-105">The following procedure outlines the steps you must follow to connect the console to an Application Virtualization System.</span></span>

**<span data-ttu-id="bd767-106">Pour se connecter à un système de virtualisation des applications</span><span class="sxs-lookup"><span data-stu-id="bd767-106">To connect to an Application Virtualization System</span></span>**

1. <span data-ttu-id="bd767-107">Dans le volet **étendue** , cliquez avec le bouton droit sur le nœud système de virtualisation des applications, puis sélectionnez **se connecter au système de virtualisation d’applications** dans le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="bd767-107">Right-click the Application Virtualization System node in the **Scope** pane, and select **Connect to Application Virtualization System** from the pop-up menu.</span></span>

   **<span data-ttu-id="bd767-108">Remarque</span><span class="sxs-lookup"><span data-stu-id="bd767-108">Note</span></span>**  
   <span data-ttu-id="bd767-109">Il existe trois composants pour la gestion de serveur de la virtualisation des applications: la console de gestion des applications, le service Web de gestion et la Banque de magasin SQL.</span><span class="sxs-lookup"><span data-stu-id="bd767-109">There are three components to Application Virtualization server management: the Application Virtualization Management Console, the Management Web Service, and the SQL Datastore.</span></span> <span data-ttu-id="bd767-110">Si ces composants sont répartis sur différentes machines physiques, vous devez configurer la sécurité correctement pour que les composants puissent communiquer sur le système.</span><span class="sxs-lookup"><span data-stu-id="bd767-110">If these components are distributed across different physical machines, you must configure security properly for the components to communicate across the system.</span></span> <span data-ttu-id="bd767-111">Pour plus d’informations, consultez les manuels et articles suivants:</span><span class="sxs-lookup"><span data-stu-id="bd767-111">For more information, see the following manuals and articles:</span></span>

   <span data-ttu-id="bd767-112">[Comment configurer le serveur pour qu’il soit approuvé pour la délégation](https://go.microsoft.com/fwlink/?LinkID=166682) (https://go.microsoft.com/fwlink/?LinkID=166682)</span><span class="sxs-lookup"><span data-stu-id="bd767-112">[How to Configure the Server to be Trusted for Delegation](https://go.microsoft.com/fwlink/?LinkID=166682) (https://go.microsoft.com/fwlink/?LinkID=166682)</span></span>

   <span data-ttu-id="bd767-113">[Guide de planification et de déploiement pour le système de virtualisation des applications](https://go.microsoft.com/fwlink/?LinkID=122063) (https://go.microsoft.com/fwlink/?LinkID=122063)</span><span class="sxs-lookup"><span data-stu-id="bd767-113">[Planning and Deployment Guide for the Application Virtualization System](https://go.microsoft.com/fwlink/?LinkID=122063) (https://go.microsoft.com/fwlink/?LinkID=122063)</span></span>

   <span data-ttu-id="bd767-114">[Guide des opérations pour le système de virtualisation des applications](https://go.microsoft.com/fwlink/?LinkID=133129) (https://go.microsoft.com/fwlink/?LinkID=133129)</span><span class="sxs-lookup"><span data-stu-id="bd767-114">[Operations Guide for the Application Virtualization System](https://go.microsoft.com/fwlink/?LinkID=133129) (https://go.microsoft.com/fwlink/?LinkID=133129)</span></span>

   <span data-ttu-id="bd767-115">[Article 930472](https://go.microsoft.com/fwlink/?LinkId=114647) de la base de connaissances Microsoft (https://go.microsoft.com/fwlink/?LinkId=114647)</span><span class="sxs-lookup"><span data-stu-id="bd767-115">[Article 930472](https://go.microsoft.com/fwlink/?LinkId=114647) in the Microsoft Knowledge Base (https://go.microsoft.com/fwlink/?LinkId=114647)</span></span>

   <span data-ttu-id="bd767-116">[Article 930565](https://go.microsoft.com/fwlink/?LinkId=114648) de la base de connaissances Microsoft (https://go.microsoft.com/fwlink/?LinkId=114648)</span><span class="sxs-lookup"><span data-stu-id="bd767-116">[Article 930565](https://go.microsoft.com/fwlink/?LinkId=114648) in the Microsoft Knowledge Base (https://go.microsoft.com/fwlink/?LinkId=114648)</span></span>

     

2. <span data-ttu-id="bd767-117">Remplissez les champs de la boîte de dialogue **connexion à l’application de virtualisation du système** :</span><span class="sxs-lookup"><span data-stu-id="bd767-117">Complete the fields in the **Connect to Application Virtualization System** dialog box:</span></span>

   1. <span data-ttu-id="bd767-118">**Nom d’hôte du service Web**: entrez le nom du système de virtualisation d’applications auquel vous voulez vous connecter, ou entrez **localhost** pour vous connecter au serveur local.</span><span class="sxs-lookup"><span data-stu-id="bd767-118">**Web Service Host Name**—Enter the name of the Application Virtualization System to which you want to connect, or enter **localhost** to connect to the local server.</span></span>

   2. <span data-ttu-id="bd767-119">**Utiliser la connexion sécurisée**: activez cette case à cocher si vous voulez vous connecter au serveur avec une connexion sécurisée.</span><span class="sxs-lookup"><span data-stu-id="bd767-119">**Use Secure Connection**—Select this check box if you want to connect to the server with a secure connection.</span></span>

   3. <span data-ttu-id="bd767-120">**Port**: entrez le numéro de port que vous voulez utiliser pour la connexion.</span><span class="sxs-lookup"><span data-stu-id="bd767-120">**Port**—Enter the port number you want to use for the connection.</span></span> <span data-ttu-id="bd767-121">**80** est le numéro de port standard par défaut et **443** correspond au numéro de port sécurisé.</span><span class="sxs-lookup"><span data-stu-id="bd767-121">**80** is the default regular port number, and **443** is the secure-port number.</span></span>

   4. <span data-ttu-id="bd767-122">**Utiliser le compte Windows actuel**: sélectionnez cette case d’option pour utiliser les informations d’identification actuelles du compte Windows.</span><span class="sxs-lookup"><span data-stu-id="bd767-122">**Use Current Windows Account**—Select this radio button to use the current Windows account credentials.</span></span>

   5. <span data-ttu-id="bd767-123">**Spécifier le compte Windows**: sélectionnez cette case d’option si vous voulez vous connecter au serveur en tant qu’autre utilisateur.</span><span class="sxs-lookup"><span data-stu-id="bd767-123">**Specify Windows Account**—Select this radio button when you want to connect to the server as a different user.</span></span>

   6. <span data-ttu-id="bd767-124">**Nom**— entrez le nom du nouvel utilisateur en utilisant le *DOMAIN\\username* ou le format du <em> username@domain </em> .</span><span class="sxs-lookup"><span data-stu-id="bd767-124">**Name**—Enter the name of the new user by using either the *DOMAIN\\username* or the <em>username@domain</em> format.</span></span>

   7. <span data-ttu-id="bd767-125">**Mot de passe**: entrez le mot de passe correspondant au nouvel utilisateur.</span><span class="sxs-lookup"><span data-stu-id="bd767-125">**Password**—Enter the password that corresponds to the new user.</span></span>

3. <span data-ttu-id="bd767-126">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="bd767-126">Click **OK**.</span></span>

## <span data-ttu-id="bd767-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bd767-127">Related topics</span></span>


[<span data-ttu-id="bd767-128">Procédure pour effectuer des tâches d'administration dans Application Virtualization Server Management Console</span><span class="sxs-lookup"><span data-stu-id="bd767-128">How to Perform Administrative Tasks in the Application Virtualization Server Management Console</span></span>](how-to-perform-administrative-tasks-in-the-application-virtualization-server-management-console.md)

 

 





