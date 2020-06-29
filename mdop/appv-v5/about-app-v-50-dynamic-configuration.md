---
title: À propos de la configuration dynamique d'App-V5.0
description: À propos de la configuration dynamique d'App-V5.0
author: dansimp
ms.assetid: 88afaca1-68c5-45c4-a074-9371c56b5804
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0294a60570d6dea99193c8bd411639c4888ae6b1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806145"
---
# <span data-ttu-id="c2f1e-103">À propos de la configuration dynamique d'App-V5.0</span><span class="sxs-lookup"><span data-stu-id="c2f1e-103">About App-V 5.0 Dynamic Configuration</span></span>


<span data-ttu-id="c2f1e-104">Vous pouvez utiliser la configuration dynamique pour personnaliser un package App-V 5,0 pour un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c2f1e-104">You can use the dynamic configuration to customize an App-V 5.0 package for a user.</span></span> <span data-ttu-id="c2f1e-105">Utilisez les informations suivantes pour créer ou modifier un fichier de configuration dynamique existant.</span><span class="sxs-lookup"><span data-stu-id="c2f1e-105">Use the following information to create or edit an existing dynamic configuration file.</span></span>

<span data-ttu-id="c2f1e-106">Lorsque vous modifiez le fichier de configuration dynamique, il personnalise la façon dont un utilisateur ou un groupe peut exécuter un package App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="c2f1e-106">When you edit the dynamic configuration file it customizes how an App-V 5.0 package will run for a user or group.</span></span> <span data-ttu-id="c2f1e-107">Cela permet de fournir une méthode plus pratique pour la personnalisation du package en supprimant la nécessité de réorganiser les packages à l’aide des paramètres souhaités et permet de maintenir le contenu du package et les paramètres personnalisés indépendants.</span><span class="sxs-lookup"><span data-stu-id="c2f1e-107">This helps to provide a more convenient method for package customization by removing the need to re-sequence packages using the desired settings, and provides a way to keep package content and custom settings independent.</span></span>

## <span data-ttu-id="c2f1e-108">Avancé: configuration dynamique</span><span class="sxs-lookup"><span data-stu-id="c2f1e-108">Advanced: Dynamic Configuration</span></span>


<span data-ttu-id="c2f1e-109">Les packages d’application virtuels contiennent un manifeste qui fournit toutes les informations fondamentales pour le package.</span><span class="sxs-lookup"><span data-stu-id="c2f1e-109">Virtual application packages contain a manifest that provides all the core information for the package.</span></span> <span data-ttu-id="c2f1e-110">Ces informations incluent les valeurs par défaut des paramètres du package et déterminent les paramètres du formulaire le plus basique (sans personnalisation supplémentaire).</span><span class="sxs-lookup"><span data-stu-id="c2f1e-110">This information includes the defaults for the package settings and determines settings in the most basic form (with no additional customization).</span></span> <span data-ttu-id="c2f1e-111">Si vous voulez ajuster ces valeurs par défaut pour un utilisateur ou un groupe particulier, vous pouvez créer et modifier les fichiers suivants:</span><span class="sxs-lookup"><span data-stu-id="c2f1e-111">If you want to adjust these defaults for a particular user or group, you can create and edit the following files:</span></span>

-   <span data-ttu-id="c2f1e-112">Fichier de configuration de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="c2f1e-112">User Configuration file</span></span>

-   <span data-ttu-id="c2f1e-113">Fichier de configuration de déploiement</span><span class="sxs-lookup"><span data-stu-id="c2f1e-113">Deployment configuration file</span></span>

<span data-ttu-id="c2f1e-114">Les fichiers. xml précédents spécifient les paramètres du package et permettent la personnalisation des packages sans affecter directement les packages.</span><span class="sxs-lookup"><span data-stu-id="c2f1e-114">The previous .xml files specify package settings and allow for packages to be customized without directly affecting the packages.</span></span> <span data-ttu-id="c2f1e-115">Lors de la création d’un package, le Sequencer génère automatiquement les fichiers de déploiement par défaut et de configuration de l’utilisateur à l’aide des données de manifeste du package.</span><span class="sxs-lookup"><span data-stu-id="c2f1e-115">When a package is created, the sequencer automatically generates default deployment and user configuration .xml files using the package manifest data.</span></span> <span data-ttu-id="c2f1e-116">C’est la raison pour laquelle ces fichiers de configuration génèrent automatiquement des paramètres par défaut que le package de la part de l’utilisation de la configuration au cours de la séquence.</span><span class="sxs-lookup"><span data-stu-id="c2f1e-116">Therefore, these automatically generated configuration files simply reflect the default settings that the package innately as from how things were configured during sequencing.</span></span> <span data-ttu-id="c2f1e-117">Si vous appliquez ces fichiers de configuration à un package dans le formulaire généré par le Sequencer, les packages présentent les mêmes paramètres par défaut que le manifeste.</span><span class="sxs-lookup"><span data-stu-id="c2f1e-117">If you apply these configuration files to a package in the form generated by the sequencer, the packages will have the same default settings that came from their manifest.</span></span> <span data-ttu-id="c2f1e-118">Cela vous permet d’accéder à un modèle spécifique au package pour commencer si l’un des paramètres par défaut doit être modifié.</span><span class="sxs-lookup"><span data-stu-id="c2f1e-118">This provides you with a package-specific template to get started if any of the defaults must be changed.</span></span>

<span data-ttu-id="c2f1e-119">**Remarques**  Les informations suivantes peuvent uniquement être utilisées pour modifier les fichiers de configuration générés par Sequencer afin de personnaliser les packages pour répondre à des exigences spécifiques en matière d’utilisateur ou de groupe.</span><span class="sxs-lookup"><span data-stu-id="c2f1e-119">**Note** The following information can only be used to modify sequencer generated configuration files to customize packages to meet specific user or group requirements.</span></span>

 

### <span data-ttu-id="c2f1e-120">Contenu du fichier de configuration dynamique</span><span class="sxs-lookup"><span data-stu-id="c2f1e-120">Dynamic Configuration file contents</span></span>

<span data-ttu-id="c2f1e-121">Tous les ajouts, suppressions et mises à jour des fichiers de configuration doivent être effectués en relation avec les valeurs par défaut spécifiées par les informations de manifeste du package.</span><span class="sxs-lookup"><span data-stu-id="c2f1e-121">All of the additions, deletions, and updates in the configuration files need to be made in relation to the default values specified by the package's manifest information.</span></span> <span data-ttu-id="c2f1e-122">Consultez le tableau suivant:</span><span class="sxs-lookup"><span data-stu-id="c2f1e-122">Review the following table:</span></span>

<table>
<colgroup>
<col width="100%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c2f1e-123">Fichier de configuration de l’utilisateur. Xml</span><span class="sxs-lookup"><span data-stu-id="c2f1e-123">User Configuration .xml file</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c2f1e-124">Fichier Configuration. XML de déploiement</span><span class="sxs-lookup"><span data-stu-id="c2f1e-124">Deployment Configuration .xml file</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c2f1e-125">Manifeste du package</span><span class="sxs-lookup"><span data-stu-id="c2f1e-125">Package Manifest</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="c2f1e-126">Le tableau précédent représente la façon dont les fichiers sont lus.</span><span class="sxs-lookup"><span data-stu-id="c2f1e-126">The previous table represents how the files will be read.</span></span> <span data-ttu-id="c2f1e-127">La première entrée représente ce qui sera lu en dernier, par conséquent, son contenu est prioritaire.</span><span class="sxs-lookup"><span data-stu-id="c2f1e-127">The first entry represents what will be read last, therefore, its content takes precedence.</span></span> <span data-ttu-id="c2f1e-128">Par conséquent, tous les packages contiennent fondamentalement et fournissent des paramètres par défaut à partir du manifeste du package.</span><span class="sxs-lookup"><span data-stu-id="c2f1e-128">Therefore, all packages inherently contain and provide default settings from the package manifest.</span></span> <span data-ttu-id="c2f1e-129">Si un fichier de configuration de déploiement. XML avec des paramètres personnalisés est appliqué, il remplace les valeurs par défaut de manifeste de package.</span><span class="sxs-lookup"><span data-stu-id="c2f1e-129">If a deployment configuration .xml file with customized settings is applied, it will override the package manifest defaults.</span></span> <span data-ttu-id="c2f1e-130">Si un fichier de configuration utilisateur. XML avec des paramètres personnalisés est appliqué avant cela, la configuration du déploiement et les valeurs par défaut du manifeste du package sont ignorées.</span><span class="sxs-lookup"><span data-stu-id="c2f1e-130">If a user configuration .xml file with customized settings is applied prior to that, it will override both the deployment configuration and the package manifest defaults.</span></span>

<span data-ttu-id="c2f1e-131">La liste suivante présente des informations supplémentaires sur les deux types de fichiers:</span><span class="sxs-lookup"><span data-stu-id="c2f1e-131">The following list displays more information about the two file types:</span></span>

-   <span data-ttu-id="c2f1e-132">**Fichier de configuration utilisateur (UserConfig)** : permet de spécifier ou de modifier des paramètres personnalisés pour un package.</span><span class="sxs-lookup"><span data-stu-id="c2f1e-132">**User Configuration File (UserConfig)** – Allows you to specify or modify custom settings for a package.</span></span> <span data-ttu-id="c2f1e-133">Ces paramètres seront appliqués pour un utilisateur spécifique lorsque le package est déployé sur un ordinateur exécutant le client App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="c2f1e-133">These settings will be applied for a specific user when the package is deployed to a computer running the App-V 5.0 client.</span></span>

-   <span data-ttu-id="c2f1e-134">**Fichier de configuration de déploiement (DeploymentConfig)** : permet de spécifier ou de modifier les paramètres par défaut d’un package.</span><span class="sxs-lookup"><span data-stu-id="c2f1e-134">**Deployment Configuration File (DeploymentConfig)** – Allows you to specify or modify the default settings for a package.</span></span> <span data-ttu-id="c2f1e-135">Ces paramètres s’appliquent à tous les utilisateurs lors du déploiement d’un package sur un ordinateur exécutant le client App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="c2f1e-135">These settings will be applied for all users when a package is deployed to a computer running the App-V 5.0 client.</span></span>

<span data-ttu-id="c2f1e-136">Pour personnaliser les paramètres d’un package pour un ensemble spécifique d’utilisateurs sur un ordinateur ou pour apporter des modifications qui seront appliquées aux emplacements des utilisateurs locaux tels que HKCU, le fichier UserConfig doit être utilisé.</span><span class="sxs-lookup"><span data-stu-id="c2f1e-136">To customize the settings for a package for a specific set of users on a computer or to make changes that will be applied to local user locations such as HKCU, the UserConfig file should be used.</span></span> <span data-ttu-id="c2f1e-137">Pour modifier les paramètres par défaut d’un package pour tous les utilisateurs sur un ordinateur ou pour apporter des modifications qui seront appliquées aux emplacements globaux tels que HKEY \ _LOCAL \ _MACHINE et le dossier All Users, le fichier DeploymentConfig doit être utilisé.</span><span class="sxs-lookup"><span data-stu-id="c2f1e-137">To modify the default settings of a package for all users on a machine or to make changes that will be applied to global locations such as HKEY\_LOCAL\_MACHINE and the all users folder, the DeploymentConfig file should be used.</span></span>

<span data-ttu-id="c2f1e-138">Le fichier UserConfig fournit des paramètres de configuration qui peuvent être appliqués à un utilisateur unique sans affecter d’autres utilisateurs sur un client:</span><span class="sxs-lookup"><span data-stu-id="c2f1e-138">The UserConfig file provides configuration settings that can be applied to a single user without affecting any other users on a client:</span></span>

-   <span data-ttu-id="c2f1e-139">Extensions intégrées au système natif par utilisateur:-raccourcis, associations de types de fichiers, protocoles d’URL, AppPaths, clients logiciels et COM</span><span class="sxs-lookup"><span data-stu-id="c2f1e-139">Extensions that will be integrated into the native system per user:- shortcuts, File-Type associations, URL Protocols, AppPaths, Software Clients and COM</span></span>

-   <span data-ttu-id="c2f1e-140">Sous-systèmes virtuels:-objets d’application, variables d’environnement, modifications du Registre, services et polices</span><span class="sxs-lookup"><span data-stu-id="c2f1e-140">Virtual Subsystems:- Application Objects, Environment variables, Registry modifications, Services and Fonts</span></span>

-   <span data-ttu-id="c2f1e-141">Scripts (contexte utilisateur uniquement)</span><span class="sxs-lookup"><span data-stu-id="c2f1e-141">Scripts (User context only)</span></span>

-   <span data-ttu-id="c2f1e-142">Autorité de gestion (pour contrôler la co-existence d’un package avec App-V 4,6)</span><span class="sxs-lookup"><span data-stu-id="c2f1e-142">Managing Authority (for controlling co-existence of package with App-V 4.6)</span></span>

<span data-ttu-id="c2f1e-143">Le fichier DeploymentConfig fournit des paramètres de configuration dans deux sections, l’un pour le contexte de l’ordinateur et l’autre relatif au contexte de l’utilisateur, qui fournit les mêmes fonctionnalités que celles indiquées dans la liste UserConfig ci-dessus:</span><span class="sxs-lookup"><span data-stu-id="c2f1e-143">The DeploymentConfig file provides configuration settings in two sections, one relative to the machine context and one relative to the user context providing the same capabilities listed in the UserConfig list above:</span></span>

-   <span data-ttu-id="c2f1e-144">Tous les paramètres de UserConfig ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="c2f1e-144">All UserConfig settings above</span></span>

-   <span data-ttu-id="c2f1e-145">Extensions qui ne peuvent être appliquées globalement que par tous les utilisateurs</span><span class="sxs-lookup"><span data-stu-id="c2f1e-145">Extensions that can only be applied globally for all users</span></span>

-   <span data-ttu-id="c2f1e-146">Les sous-systèmes virtuels qui peuvent être configurés pour les emplacements globaux de l’ordinateur (par exemple, registre)</span><span class="sxs-lookup"><span data-stu-id="c2f1e-146">Virtual Subsystems that can be configured for global machine locations e.g. registry</span></span>

-   <span data-ttu-id="c2f1e-147">URL de la source de produit</span><span class="sxs-lookup"><span data-stu-id="c2f1e-147">Product Source URL</span></span>

-   <span data-ttu-id="c2f1e-148">Scripts (contexte de l’ordinateur uniquement)</span><span class="sxs-lookup"><span data-stu-id="c2f1e-148">Scripts (Machine context only)</span></span>

-   <span data-ttu-id="c2f1e-149">Contrôles pour arrêter les processus enfants</span><span class="sxs-lookup"><span data-stu-id="c2f1e-149">Controls to Terminate Child Processes</span></span>

### <span data-ttu-id="c2f1e-150">Structure de fichier</span><span class="sxs-lookup"><span data-stu-id="c2f1e-150">File structure</span></span>

<span data-ttu-id="c2f1e-151">La structure du fichier de configuration dynamique App-V 5,0 est expliquée dans la section suivante.</span><span class="sxs-lookup"><span data-stu-id="c2f1e-151">The structure of the App-V 5.0 Dynamic Configuration file is explained in the following section.</span></span>

### <span data-ttu-id="c2f1e-152">Fichier de configuration utilisateur dynamique</span><span class="sxs-lookup"><span data-stu-id="c2f1e-152">Dynamic User Configuration file</span></span>

<span data-ttu-id="c2f1e-153">**Header** : l’en-tête d’un fichier de configuration utilisateur dynamique se présente comme suit:</span><span class="sxs-lookup"><span data-stu-id="c2f1e-153">**Header** - the header of a dynamic user configuration file is as follows:</span></span>

<span data-ttu-id="c2f1e-154">&lt;? XML version = "1.0" Encoding = "UTF-8"? &gt; &lt; UserConfiguration **PackageId**= "1F8488bf-2257-46B4-B27F-09c9dbaae707" DisplayName = "réservé" xmlns = " <https://schemas.microsoft.com/appv/2010/userconfiguration"&gt> ;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-154">&lt;?xml version="1.0" encoding="utf-8"?&gt;&lt;UserConfiguration **PackageId**="1f8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName="Reserved" xmlns="<https://schemas.microsoft.com/appv/2010/userconfiguration"&gt>;</span></span>

<span data-ttu-id="c2f1e-155">**PackageId** est de la même valeur qu’existe dans le fichier manifeste.</span><span class="sxs-lookup"><span data-stu-id="c2f1e-155">The **PackageId** is the same value as exists in the Manifest file.</span></span>

<span data-ttu-id="c2f1e-156">**Corps** -le corps du fichier de configuration de l’utilisateur dynamique peut inclure tous les points d’extension d’application définis dans le fichier manifeste ainsi que les informations de configuration des applications virtuelles.</span><span class="sxs-lookup"><span data-stu-id="c2f1e-156">**Body** - the body of the Dynamic User Configuration file can include all the app extension points that are defined in the Manifest file, as well as information to configure virtual applications.</span></span> <span data-ttu-id="c2f1e-157">Quatre sous-sections sont autorisées dans le corps de texte:</span><span class="sxs-lookup"><span data-stu-id="c2f1e-157">There are four subsections allowed in the body:</span></span>

1. <span data-ttu-id="c2f1e-158">**Applications** : toutes les extensions d’application contenues dans le fichier manifeste au sein d’un package sont affectées avec un ID d’application, qui est également défini dans le fichier manifeste.</span><span class="sxs-lookup"><span data-stu-id="c2f1e-158">**Applications** - All app-extensions that are contained in the Manifest file within a package are assigned with an Application ID, which is also defined in the manifest file.</span></span> <span data-ttu-id="c2f1e-159">Cela vous permet d’activer ou de désactiver toutes les extensions pour une application donnée au sein d’un package.</span><span class="sxs-lookup"><span data-stu-id="c2f1e-159">This allows you to enable or disable all the extensions for a given application within a package.</span></span> <span data-ttu-id="c2f1e-160">L' **ID d’application** doit exister dans le fichier manifeste ou être ignoré.</span><span class="sxs-lookup"><span data-stu-id="c2f1e-160">The **Application ID** must exist in the Manifest file or it will be ignored.</span></span>

   <span data-ttu-id="c2f1e-161">&lt;UserConfiguration **PackageId**= "1F8488bf-2257-46B4-B27F-09c9dbaae707" DisplayName = "réservé" xmlns = " <https://schemas.microsoft.com/appv/2010/userconfiguration"&gt> ;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-161">&lt;UserConfiguration **PackageId**="1f8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName="Reserved" xmlns="<https://schemas.microsoft.com/appv/2010/userconfiguration"&gt>;</span></span>

   <span data-ttu-id="c2f1e-162">&lt;Applications&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-162">&lt;Applications&gt;</span></span>

   <span data-ttu-id="c2f1e-163">&lt;!--Aucune nouvelle application ne peut être définie dans Policy.</span><span class="sxs-lookup"><span data-stu-id="c2f1e-163">&lt;!-- No new application can be defined in policy.</span></span> <span data-ttu-id="c2f1e-164">Le client AppV ignorera tout ID d’application qui n’est pas également présent dans le fichier manifeste:&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-164">AppV Client will ignore any application ID that is not also in the Manifest file --&gt;</span></span>

   <span data-ttu-id="c2f1e-165">&lt;ID d’application = "{a56fa627-c35f-4A01-9e79-7d36aed8225a}" enabled = "false"&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-165">&lt;Application Id="{a56fa627-c35f-4a01-9e79-7d36aed8225a}" Enabled="false"&gt;</span></span>

   <span data-ttu-id="c2f1e-166">&lt;/Application&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-166">&lt;/Application&gt;</span></span>

   <span data-ttu-id="c2f1e-167">&lt;/Applications&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-167">&lt;/Applications&gt;</span></span>

   <span data-ttu-id="c2f1e-168">…</span><span class="sxs-lookup"><span data-stu-id="c2f1e-168">…</span></span>

   <span data-ttu-id="c2f1e-169">&lt;/UserConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-169">&lt;/UserConfiguration&gt;</span></span>

2. <span data-ttu-id="c2f1e-170">Les sous- **systèmes** -nouvel appextensions et les autres sous-systèmes sont organisés en tant que sous-nœuds dans les sous &lt; -systèmes &gt; :</span><span class="sxs-lookup"><span data-stu-id="c2f1e-170">**Subsystems** - AppExtensions and other subsystems are arranged as subnodes under the &lt;Subsystems&gt;:</span></span>

   <span data-ttu-id="c2f1e-171">&lt;UserConfiguration **PackageId**= "1F8488bf-2257-46B4-B27F-09c9dbaae707" DisplayName = "réservé" xmlns = " <https://schemas.microsoft.com/appv/2010/userconfiguration"&gt> ;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-171">&lt;UserConfiguration **PackageId**="1f8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName="Reserved" xmlns="<https://schemas.microsoft.com/appv/2010/userconfiguration"&gt>;</span></span>

   <span data-ttu-id="c2f1e-172">&lt;Sous-systèmes&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-172">&lt;Subsystems&gt;</span></span>

   <span data-ttu-id="c2f1e-173">..</span><span class="sxs-lookup"><span data-stu-id="c2f1e-173">..</span></span>

   <span data-ttu-id="c2f1e-174">&lt;/Subsystems&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-174">&lt;/Subsystems&gt;</span></span>

   <span data-ttu-id="c2f1e-175">..</span><span class="sxs-lookup"><span data-stu-id="c2f1e-175">..</span></span>

   <span data-ttu-id="c2f1e-176">&lt;/UserConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-176">&lt;/UserConfiguration&gt;</span></span>

   <span data-ttu-id="c2f1e-177">Chaque sous-système peut être activé/désactivé à l’aide de l’attribut «**activé**».</span><span class="sxs-lookup"><span data-stu-id="c2f1e-177">Each subsystem can be enabled/disabled using the “**Enabled**” attribute.</span></span> <span data-ttu-id="c2f1e-178">Vous trouverez ci-dessous les divers exemples de sous-systèmes et d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="c2f1e-178">Below are the various subsystems and usage samples.</span></span>

   **<span data-ttu-id="c2f1e-179">Variable</span><span class="sxs-lookup"><span data-stu-id="c2f1e-179">Extensions:</span></span>**

   <span data-ttu-id="c2f1e-180">Quelques extensions de contrôle de sous-systèmes (sous-systèmes d’extension).</span><span class="sxs-lookup"><span data-stu-id="c2f1e-180">Some subsystems (Extension Subsystems) control Extensions.</span></span> <span data-ttu-id="c2f1e-181">Ces sous-systèmes sont: des raccourcis clavier, des associations de types de fichiers, des protocoles d’URL, des AppPaths, des clients logiciels et des COM</span><span class="sxs-lookup"><span data-stu-id="c2f1e-181">Those subsystems are:- shortcuts, File-Type associations, URL Protocols, AppPaths, Software Clients and COM</span></span>

   <span data-ttu-id="c2f1e-182">Les sous-systèmes d’extension peuvent être activés ou désactivés indépendamment du contenu.</span><span class="sxs-lookup"><span data-stu-id="c2f1e-182">Extension Subsystems can be enabled and disabled independently of the content.</span></span>  <span data-ttu-id="c2f1e-183">Par conséquent, si des raccourcis sont activés, le client utilisera par défaut les raccourcis contenus dans le manifeste.</span><span class="sxs-lookup"><span data-stu-id="c2f1e-183">Thus if Shortcuts are enabled, The client will use the shortcuts contained within the manifest by default.</span></span> <span data-ttu-id="c2f1e-184">Chaque sous-système d’extension peut contenir un &lt; &gt; nœud extensions.</span><span class="sxs-lookup"><span data-stu-id="c2f1e-184">Each Extension Subsystem can contain an &lt;Extensions&gt; node.</span></span> <span data-ttu-id="c2f1e-185">Si cet élément enfant est présent, le client ignore le contenu du fichier manifeste du sous-système et utilise uniquement le contenu du fichier de configuration.</span><span class="sxs-lookup"><span data-stu-id="c2f1e-185">If this child element is present, the client will ignore the content in the Manifest file for that subsystem and only use the content in the configuration file.</span></span>

   <span data-ttu-id="c2f1e-186">Exemple utilisant le sous-système de raccourcis:</span><span class="sxs-lookup"><span data-stu-id="c2f1e-186">Example using the shortcuts subsystem:</span></span>

   1.  <span data-ttu-id="c2f1e-187">Si l’utilisateur a défini cette valeur dans le fichier de configuration du déploiement ou du fichier dynamique:</span><span class="sxs-lookup"><span data-stu-id="c2f1e-187">If the user defined this in either the dynamic or deployment config file:</span></span>

                                    **&lt;Shortcuts  Enabled="true"&gt;**

                                                **&lt;Extensions&gt;**

                                                 ...

                                                **&lt;/Extensions&gt;**

                                    **&lt;/Shortcuts&gt;**

                         Content in the manifest will be ignored.   

   2.  <span data-ttu-id="c2f1e-188">Si l’utilisateur a défini uniquement ce qui suit:</span><span class="sxs-lookup"><span data-stu-id="c2f1e-188">If the user defined only the following:</span></span>

                                   **&lt;Shortcuts  Enabled="true"/&gt;**

                         Then the content in the Manifest will be integrated during publishing.

   3.  <span data-ttu-id="c2f1e-189">Si l’utilisateur définit ce qui suit:</span><span class="sxs-lookup"><span data-stu-id="c2f1e-189">If the user defines the following</span></span>

                                  **&lt;Shortcuts  Enabled="true"&gt;**

                                                **&lt;Extensions/&gt;**

                                    **&lt;/Shortcuts&gt;**

   <span data-ttu-id="c2f1e-190">Tous les raccourcis du manifeste seront tout de même ignorés.</span><span class="sxs-lookup"><span data-stu-id="c2f1e-190">Then all the shortcuts within the manifest will still be ignored.</span></span> <span data-ttu-id="c2f1e-191">Aucun raccourci n’est intégré.</span><span class="sxs-lookup"><span data-stu-id="c2f1e-191">There will be no shortcuts integrated.</span></span>

   <span data-ttu-id="c2f1e-192">Les sous-systèmes d’extension pris en charge sont les suivants:</span><span class="sxs-lookup"><span data-stu-id="c2f1e-192">The supported Extension Subsystems are:</span></span>

   <span data-ttu-id="c2f1e-193">**Raccourcis clavier:** Ce contrôle contrôle les raccourcis qui seront intégrés au système local.</span><span class="sxs-lookup"><span data-stu-id="c2f1e-193">**Shortcuts:** This controls shortcuts that will be integrated into the local system.</span></span> <span data-ttu-id="c2f1e-194">Vous trouverez ci-dessous un exemple avec 2 raccourcis:</span><span class="sxs-lookup"><span data-stu-id="c2f1e-194">Below is a sample with 2 shortcuts:</span></span>

   <span data-ttu-id="c2f1e-195">&lt;Sous-systèmes&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-195">&lt;Subsystems&gt;</span></span>

   <span data-ttu-id="c2f1e-196">&lt;Raccourcis activés: "vrai"&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-196">&lt;Shortcuts Enabled="true"&gt;</span></span>

     <span data-ttu-id="c2f1e-197">&lt;Extensions&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-197">&lt;Extensions&gt;</span></span>

       &lt;Extension Category="AppV.Shortcut"&gt;

         &lt;Shortcut&gt;

           &lt;File&gt;\[{Common Programs}\]\\Microsoft Contoso\\Microsoft ContosoApp Filler 2010.lnk&lt;/File&gt;

           &lt;Target&gt;\[{PackageRoot}\]\\Contoso\\ContosoApp.EXE&lt;/Target&gt;

           &lt;Icon&gt;\[{Windows}\]\\Installer\\{90140000-0011-0000-0000-0000000FF1CE}\\inficon.exe&lt;/Icon&gt;

           &lt;Arguments /&gt;

           &lt;WorkingDirectory /&gt;

           &lt;AppUserModelId&gt;ContosoApp.Filler.3&lt;/AppUserModelId&gt;

           &lt;Description&gt;Fill out dynamic forms to gather and reuse information throughout the organization using Microsoft ContosoApp.&lt;/Description&gt;

           &lt;Hotkey&gt;0&lt;/Hotkey&gt;

           &lt;ShowCommand&gt;1&lt;/ShowCommand&gt;

           &lt;ApplicationId&gt;\[{PackageRoot}\]\\Contoso\\ContosoApp.EXE&lt;/ApplicationId&gt;

         &lt;/Shortcut&gt;

     <span data-ttu-id="c2f1e-198">&lt;/Extension&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-198">&lt;/Extension&gt;</span></span>

     <span data-ttu-id="c2f1e-199">&lt;Extension catégorie = "AppV. Shortcut"&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-199">&lt;Extension Category="AppV.Shortcut"&gt;</span></span>

       &lt;Shortcut&gt;

         &lt;File&gt;\[{AppData}\]\\Microsoft\\Contoso\\Recent\\Templates.LNK&lt;/File&gt;

         &lt;Target&gt;\[{AppData}\]\\Microsoft\\Templates&lt;/Target&gt;

         &lt;Icon /&gt;

         &lt;Arguments /&gt;

         &lt;WorkingDirectory /&gt;

         &lt;AppUserModelId /&gt;

         &lt;Description /&gt;

         &lt;Hotkey&gt;0&lt;/Hotkey&gt;

         &lt;ShowCommand&gt;1&lt;/ShowCommand&gt;

         &lt;!-- Note the ApplicationId is optional --&gt;

       &lt;/Shortcut&gt;

     <span data-ttu-id="c2f1e-200">&lt;/Extension&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-200">&lt;/Extension&gt;</span></span>

    <span data-ttu-id="c2f1e-201">&lt;/Extensions&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-201">&lt;/Extensions&gt;</span></span>

   <span data-ttu-id="c2f1e-202">&lt;/Shortcuts&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-202">&lt;/Shortcuts&gt;</span></span>

   <span data-ttu-id="c2f1e-203">**Associations de types de fichiers:** Associe des types de fichiers à des programmes pour s’ouvrir par défaut et configure le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="c2f1e-203">**File-Type Associations:** Associates File-types with programs to open by default as well as setup the context menu.</span></span> <span data-ttu-id="c2f1e-204">(Le type MIME peut également être configuré à l’aide de ce susbsystem).</span><span class="sxs-lookup"><span data-stu-id="c2f1e-204">(MIME types can also be setup using this susbsystem).</span></span> <span data-ttu-id="c2f1e-205">L’exemple d’association de type de fichier est le suivant:</span><span class="sxs-lookup"><span data-stu-id="c2f1e-205">Sample File-type Association is below:</span></span>

   <span data-ttu-id="c2f1e-206">&lt;FileTypeAssociations activé = "vrai"&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-206">&lt;FileTypeAssociations Enabled="true"&gt;</span></span>

   <span data-ttu-id="c2f1e-207">&lt;Extensions&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-207">&lt;Extensions&gt;</span></span>

     <span data-ttu-id="c2f1e-208">&lt;Extension category = "AppV. FileTypeAssociation"&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-208">&lt;Extension Category="AppV.FileTypeAssociation"&gt;</span></span>

       &lt;FileTypeAssociation&gt;

         &lt;FileExtension MimeAssociation="true"&gt;

         &lt;Name&gt;.docm&lt;/Name&gt;

         &lt;ProgId&gt;contosowordpad.DocumentMacroEnabled.12&lt;/ProgId&gt;

         &lt;PerceivedType&gt;document&lt;/PerceivedType&gt;

         &lt;ContentType&gt;application/vnd.ms-contosowordpad.document.macroEnabled.12&lt;/ContentType&gt;

         &lt;OpenWithList&gt;

           &lt;ApplicationName&gt;wincontosowordpad.exe&lt;/ApplicationName&gt;

         &lt;/OpenWithList&gt;

        &lt;OpenWithProgIds&gt;

           &lt;ProgId&gt;contosowordpad.8&lt;/ProgId&gt;

         &lt;/OpenWithProgIds&gt;

         &lt;ShellNew&gt;

           &lt;Command /&gt;

           &lt;DataBinary /&gt;

           &lt;DataText /&gt;

           &lt;FileName /&gt;

           &lt;NullFile&gt;true&lt;/NullFile&gt;

           &lt;ItemName /&gt;

           &lt;IconPath /&gt;

           &lt;MenuText /&gt;

           &lt;Handler /&gt;

         &lt;/ShellNew&gt;

       &lt;/FileExtension&gt;

       &lt;ProgId&gt;

          &lt;Name&gt;contosowordpad.DocumentMacroEnabled.12&lt;/Name&gt;

           &lt;DefaultIcon&gt;\[{Windows}\]\\Installer\\{90140000-0011-0000-0000-0000000FF1CE}\\contosowordpadicon.exe,15&lt;/DefaultIcon&gt;

           &lt;Description&gt;Blah Blah Blah&lt;/Description&gt;

           &lt;FriendlyTypeName&gt;\[{FOLDERID\_ProgramFilesX86}\]\\Microsoft Contoso 14\\res.dll,9182&lt;/FriendlyTypeName&gt;

           &lt;InfoTip&gt;\[{FOLDERID\_ProgramFilesX86}\]\\Microsoft Contoso 14\\res.dll,1424&lt;/InfoTip&gt;

           &lt;EditFlags&gt;0&lt;/EditFlags&gt;

           &lt;ShellCommands&gt;

             &lt;DefaultCommand&gt;Open&lt;/DefaultCommand&gt;

             &lt;ShellCommand&gt;

                &lt;ApplicationId&gt;{e56fa627-c35f-4a01-9e79-7d36aed8225a}&lt;/ApplicationId&gt;

                &lt;Name&gt;Edit&lt;/Name&gt;

                &lt;FriendlyName&gt;&Edit&lt;/FriendlyName&gt;

                &lt;CommandLine&gt;"\[{PackageRoot}\]\\Contoso\\WINcontosowordpad.EXE" /vu "%1"&lt;/CommandLine&gt;

             &lt;/ShellCommand&gt;

             &lt;/ShellCommand&gt;

               &lt;ApplicationId&gt;{e56fa627-c35f-4a01-9e79-7d36aed8225a}&lt;/ApplicationId&gt;

               &lt;Name&gt;Open&lt;/Name&gt;

               &lt;FriendlyName&gt;&Open&lt;/FriendlyName&gt;

               &lt;CommandLine&gt;"\[{PackageRoot}\]\\Contoso\\WINcontosowordpad.EXE" /n "%1"&lt;/CommandLine&gt;

               &lt;DropTargetClassId /&gt;

               &lt;DdeExec&gt;

                 &lt;Application&gt;mscontosowordpad&lt;/Application&gt;

                 &lt;Topic&gt;ShellSystem&lt;/Topic&gt;

                 &lt;IfExec&gt;\[SHELLNOOP\]&lt;/IfExec&gt;

                 &lt;DdeCommand&gt;\[SetForeground\]\[ShellNewDatabase "%1"\]&lt;/DdeCommand&gt;

               &lt;/DdeExec&gt;

             &lt;/ShellCommand&gt;

           &lt;/ShellCommands&gt;

         &lt;/ProgId&gt;

        &lt;/FileTypeAssociation&gt;

      <span data-ttu-id="c2f1e-209">&lt;/Extension&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-209">&lt;/Extension&gt;</span></span>

     <span data-ttu-id="c2f1e-210">&lt;/Extensions&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-210">&lt;/Extensions&gt;</span></span>

     <span data-ttu-id="c2f1e-211">&lt;/FileTypeAssociations&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-211">&lt;/FileTypeAssociations&gt;</span></span>

   <span data-ttu-id="c2f1e-212">**Protocoles d’URL**: cette commande contrôle les protocoles d’URL intégrés au registre local de l’ordinateur client (par exemple, «mailto:»).</span><span class="sxs-lookup"><span data-stu-id="c2f1e-212">**URL Protocols**: This controls the URL Protocols that are integrated into the local registry of the client machine e.g. “mailto:”.</span></span>

   <span data-ttu-id="c2f1e-213">&lt;URLProtocols activé = "vrai"&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-213">&lt;URLProtocols Enabled="true"&gt;</span></span>

   <span data-ttu-id="c2f1e-214">&lt;Extensions&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-214">&lt;Extensions&gt;</span></span>

   <span data-ttu-id="c2f1e-215">&lt;Extension category = "AppV. URLProtocol"&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-215">&lt;Extension Category="AppV.URLProtocol"&gt;</span></span>

   <span data-ttu-id="c2f1e-216">&lt;URLProtocol&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-216">&lt;URLProtocol&gt;</span></span>

     <span data-ttu-id="c2f1e-217">&lt;Nom &gt; mailto &lt; /Name&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-217">&lt;Name&gt;mailto&lt;/Name&gt;</span></span>

     <span data-ttu-id="c2f1e-218">&lt;ApplicationURLProtocol&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-218">&lt;ApplicationURLProtocol&gt;</span></span>

     <span data-ttu-id="c2f1e-219">&lt;DefaultIcon &gt; \ [{ProgramFilesX86} \] \\Microsoft Contoso\\Contoso\\contosomail.EXE,-9403 &lt; /DefaultIcon&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-219">&lt;DefaultIcon&gt;\[{ProgramFilesX86}\]\\Microsoft Contoso\\Contoso\\contosomail.EXE,-9403&lt;/DefaultIcon&gt;</span></span>

     <span data-ttu-id="c2f1e-220">&lt;EditFlags &gt; 2 &lt; /EditFlags&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-220">&lt;EditFlags&gt;2&lt;/EditFlags&gt;</span></span>

     <span data-ttu-id="c2f1e-221">&lt;Description&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-221">&lt;Description /&gt;</span></span>

     <span data-ttu-id="c2f1e-222">&lt;Ayant&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-222">&lt;AppUserModelId /&gt;</span></span>

     <span data-ttu-id="c2f1e-223">&lt;FriendlyTypeName /&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-223">&lt;FriendlyTypeName /&gt;</span></span>

     <span data-ttu-id="c2f1e-224">&lt;Info&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-224">&lt;InfoTip /&gt;</span></span>

   <span data-ttu-id="c2f1e-225">&lt;SourceFilter /&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-225">&lt;SourceFilter /&gt;</span></span>

     <span data-ttu-id="c2f1e-226">&lt;ShellFolder /&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-226">&lt;ShellFolder /&gt;</span></span>

     <span data-ttu-id="c2f1e-227">&lt;WebNavigableCLSID /&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-227">&lt;WebNavigableCLSID /&gt;</span></span>

     <span data-ttu-id="c2f1e-228">&lt;ExplorerFlags &gt; 2 &lt; /ExplorerFlags&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-228">&lt;ExplorerFlags&gt;2&lt;/ExplorerFlags&gt;</span></span>

     <span data-ttu-id="c2f1e-229">&lt;CLSID&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-229">&lt;CLSID /&gt;</span></span>

     <span data-ttu-id="c2f1e-230">&lt;ShellCommands&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-230">&lt;ShellCommands&gt;</span></span>

     <span data-ttu-id="c2f1e-231">&lt;DefaultCommand &gt; ouvrir &lt; /DefaultCommand&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-231">&lt;DefaultCommand&gt;open&lt;/DefaultCommand&gt;</span></span>

     <span data-ttu-id="c2f1e-232">&lt;ShellCommand&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-232">&lt;ShellCommand&gt;</span></span>

     <span data-ttu-id="c2f1e-233">&lt;ApplicationId &gt; \ [{ProgramFilesX86} \] \\Microsoft Contoso\\Contoso\\contosomail.EXE&lt; /ApplicationId&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-233">&lt;ApplicationId&gt;\[{ProgramFilesX86}\]\\Microsoft Contoso\\Contoso\\contosomail.EXE&lt;/ApplicationId&gt;</span></span>

     <span data-ttu-id="c2f1e-234">&lt;Nom &gt; ouvert &lt; /Name&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-234">&lt;Name&gt;open&lt;/Name&gt;</span></span>

     <span data-ttu-id="c2f1e-235">&lt;CommandLine &gt; \ [{ProgramFilesX86} \\Microsoft Contoso\\Contoso\\contosomail.EXE "-c OEP. Remarque/m "%1" &lt; /CommandLine&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-235">&lt;CommandLine&gt;\[{ProgramFilesX86}\\Microsoft Contoso\\Contoso\\contosomail.EXE" -c OEP.Note /m "%1"&lt;/CommandLine&gt;</span></span>

     <span data-ttu-id="c2f1e-236">&lt;DropTargetClassId /&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-236">&lt;DropTargetClassId /&gt;</span></span>

     <span data-ttu-id="c2f1e-237">&lt;FriendlyName&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-237">&lt;FriendlyName /&gt;</span></span>

     <span data-ttu-id="c2f1e-238">&lt;Étendu &gt; 0 &lt; /Extended&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-238">&lt;Extended&gt;0&lt;/Extended&gt;</span></span>

     <span data-ttu-id="c2f1e-239">&lt;LegacyDisable &gt; 0 &lt; /LegacyDisable&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-239">&lt;LegacyDisable&gt;0&lt;/LegacyDisable&gt;</span></span>

     <span data-ttu-id="c2f1e-240">&lt;SuppressionPolicy &gt; 2 &lt; /SuppressionPolicy&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-240">&lt;SuppressionPolicy&gt;2&lt;/SuppressionPolicy&gt;</span></span>

      <span data-ttu-id="c2f1e-241">&lt;DdeExec&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-241">&lt;DdeExec&gt;</span></span>

     <span data-ttu-id="c2f1e-242">&lt;NoActivateHandler /&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-242">&lt;NoActivateHandler /&gt;</span></span>

     <span data-ttu-id="c2f1e-243">&lt;Application &gt; ContosoMail &lt; /application&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-243">&lt;Application&gt;contosomail&lt;/Application&gt;</span></span>

     <span data-ttu-id="c2f1e-244">&lt;Rubrique &gt; ShellSystem &lt; /topic&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-244">&lt;Topic&gt;ShellSystem&lt;/Topic&gt;</span></span>

     <span data-ttu-id="c2f1e-245">&lt;IfExec &gt; \ [SHELLNOOP \] &lt; /IfExec&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-245">&lt;IfExec&gt;\[SHELLNOOP\]&lt;/IfExec&gt;</span></span>

     <span data-ttu-id="c2f1e-246">&lt;DdeCommand &gt; \ [SetForeground \] \ [ShellNewDatabase "%1" \] &lt; /DdeCommand&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-246">&lt;DdeCommand&gt;\[SetForeground\]\[ShellNewDatabase "%1"\]&lt;/DdeCommand&gt;</span></span>

     <span data-ttu-id="c2f1e-247">&lt;/DdeExec&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-247">&lt;/DdeExec&gt;</span></span>

     <span data-ttu-id="c2f1e-248">&lt;/ShellCommand&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-248">&lt;/ShellCommand&gt;</span></span>

     <span data-ttu-id="c2f1e-249">&lt;/ShellCommands&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-249">&lt;/ShellCommands&gt;</span></span>

     <span data-ttu-id="c2f1e-250">&lt;/ApplicationURLProtocol&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-250">&lt;/ApplicationURLProtocol&gt;</span></span>

     <span data-ttu-id="c2f1e-251">&lt;/URLProtocol&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-251">&lt;/URLProtocol&gt;</span></span>

     <span data-ttu-id="c2f1e-252">&lt;/Extension&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-252">&lt;/Extension&gt;</span></span>

     <span data-ttu-id="c2f1e-253">&lt;/Extension&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-253">&lt;/Extension&gt;</span></span>

     <span data-ttu-id="c2f1e-254">&lt;/URLProtocols&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-254">&lt;/URLProtocols&gt;</span></span>

   <span data-ttu-id="c2f1e-255">**Clients logiciels**: permet à l’application de s’inscrire en tant que client de messagerie, lecteur de News, lecteur multimédia et rend l’application visible dans l’interface utilisateur définir l’accès aux programmes et aux paramètres de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c2f1e-255">**Software Clients**: Allows the app to register as an Email client, news reader, media player and makes the app visible in the Set Program Access and Computer Defaults UI.</span></span> <span data-ttu-id="c2f1e-256">Dans la plupart des cas, vous devez seulement les activer et les désactiver.</span><span class="sxs-lookup"><span data-stu-id="c2f1e-256">In most cases you should only need to enable and disable it.</span></span> <span data-ttu-id="c2f1e-257">Il existe également un contrôle permettant d’activer et de désactiver le client de messagerie de manière spécifique si vous souhaitez que les autres clients restent activés, à l’exception de ce client.</span><span class="sxs-lookup"><span data-stu-id="c2f1e-257">There is also a control to enable and disable the email client specifically if you want the other clients still enabled except for that client.</span></span>

   <span data-ttu-id="c2f1e-258">&lt;SoftwareClients activé = "vrai"&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-258">&lt;SoftwareClients Enabled="true"&gt;</span></span>

     <span data-ttu-id="c2f1e-259">&lt;ClientConfiguration EmailEnabled = "false"/&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-259">&lt;ClientConfiguration EmailEnabled="false" /&gt;</span></span>

   <span data-ttu-id="c2f1e-260">&lt;/SoftwareClients&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-260">&lt;/SoftwareClients&gt;</span></span>

   <span data-ttu-id="c2f1e-261">AppPaths:-si une application par exemple contoso.exe est inscrite à l’aide d’un nom appPath de «MyApp», elle permet de taper «MyApp» sous le menu Exécuter et il ouvre contoso.exe.</span><span class="sxs-lookup"><span data-stu-id="c2f1e-261">AppPaths:- If an application for example contoso.exe is registered with an apppath name of “myapp”, it allows you type “myapp” under the run menu and it will open contoso.exe.</span></span>

   <span data-ttu-id="c2f1e-262">&lt;AppPaths activé = "vrai"&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-262">&lt;AppPaths Enabled="true"&gt;</span></span>

   <span data-ttu-id="c2f1e-263">&lt;Extensions&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-263">&lt;Extensions&gt;</span></span>

   <span data-ttu-id="c2f1e-264">&lt;Extension category = "AppV. AppPath"&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-264">&lt;Extension Category="AppV.AppPath"&gt;</span></span>

   <span data-ttu-id="c2f1e-265">&lt;AppPath&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-265">&lt;AppPath&gt;</span></span>

     <span data-ttu-id="c2f1e-266">&lt;ApplicationId &gt; \ [{ProgramFilesX86} \] \\Microsoft Contoso\\Contoso\\contosomail.EXE&lt; /ApplicationId&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-266">&lt;ApplicationId&gt;\[{ProgramFilesX86}\]\\Microsoft Contoso\\Contoso\\contosomail.EXE&lt;/ApplicationId&gt;</span></span>

     <span data-ttu-id="c2f1e-267">&lt;Nom &gt;contosomail.exe&lt; /nom&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-267">&lt;Name&gt;contosomail.exe&lt;/Name&gt;</span></span>

     <span data-ttu-id="c2f1e-268">&lt;ApplicationPath &gt; \ [{ProgramFilesX86} \] \\Microsoft Contoso\\Contoso\\contosomail.EXE&lt; /ApplicationPath&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-268">&lt;ApplicationPath&gt;\[{ProgramFilesX86}\]\\Microsoft Contoso\\Contoso\\contosomail.EXE&lt;/ApplicationPath&gt;</span></span>

     <span data-ttu-id="c2f1e-269">&lt;PATHEnvironmentVariablePrefix /&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-269">&lt;PATHEnvironmentVariablePrefix /&gt;</span></span>

     <span data-ttu-id="c2f1e-270">&lt;CanAcceptUrl &gt; false &lt; /CanAcceptUrl&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-270">&lt;CanAcceptUrl&gt;false&lt;/CanAcceptUrl&gt;</span></span>

     <span data-ttu-id="c2f1e-271">&lt;SaveUrl /&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-271">&lt;SaveUrl /&gt;</span></span>

   <span data-ttu-id="c2f1e-272">&lt;/AppPath&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-272">&lt;/AppPath&gt;</span></span>

   <span data-ttu-id="c2f1e-273">&lt;/Extension&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-273">&lt;/Extension&gt;</span></span>

   <span data-ttu-id="c2f1e-274">&lt;/Extensions&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-274">&lt;/Extensions&gt;</span></span>

   <span data-ttu-id="c2f1e-275">&lt;/AppPaths&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-275">&lt;/AppPaths&gt;</span></span>

   <span data-ttu-id="c2f1e-276">**Com**: permet à une application de s’inscrire aux serveurs com locaux.</span><span class="sxs-lookup"><span data-stu-id="c2f1e-276">**COM**: Allows an Application register Local COM servers.</span></span> <span data-ttu-id="c2f1e-277">Le mode peut être intégré, isolé ou désactivé.</span><span class="sxs-lookup"><span data-stu-id="c2f1e-277">Mode can be Integration, Isolated or Off.</span></span> <span data-ttu-id="c2f1e-278">Lorsque isol.</span><span class="sxs-lookup"><span data-stu-id="c2f1e-278">When Isol.</span></span>

   <span data-ttu-id="c2f1e-279">&lt;Mode COM = "isolé"/&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-279">&lt;COM Mode="Isolated"/&gt;</span></span>

   <span data-ttu-id="c2f1e-280">**Autres paramètres**:</span><span class="sxs-lookup"><span data-stu-id="c2f1e-280">**Other Settings**:</span></span>

   <span data-ttu-id="c2f1e-281">Outre les extensions, il est possible d’activer/de désactiver et de modifier d’autres sous-systèmes:</span><span class="sxs-lookup"><span data-stu-id="c2f1e-281">In addition to Extensions, other subsystems can be enabled/disabled and edited:</span></span>

   <span data-ttu-id="c2f1e-282">**Objets de noyau virtuel**:</span><span class="sxs-lookup"><span data-stu-id="c2f1e-282">**Virtual Kernel Objects**:</span></span>

   <span data-ttu-id="c2f1e-283">&lt;Objets activés = "faux"/&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-283">&lt;Objects Enabled="false" /&gt;</span></span>

   <span data-ttu-id="c2f1e-284">**Registre virtuel**: utilisé si vous voulez définir un registre dans le registre virtuel dans HKCU</span><span class="sxs-lookup"><span data-stu-id="c2f1e-284">**Virtual Registry**: Used if you want to set a registry in the Virtual Registry within HKCU</span></span>

   <span data-ttu-id="c2f1e-285">&lt;Registry Enabled = "true"&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-285">&lt;Registry Enabled="true"&gt;</span></span>

   <span data-ttu-id="c2f1e-286">&lt;Agir&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-286">&lt;Include&gt;</span></span>

   <span data-ttu-id="c2f1e-287">&lt;Chemin clé = "\\REGISTRY\\USER\\\ [{AppVCurrentUserSID} \] \\Software\\ABC"&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-287">&lt;Key Path="\\REGISTRY\\USER\\\[{AppVCurrentUserSID}\]\\Software\\ABC"&gt;</span></span>

   <span data-ttu-id="c2f1e-288">&lt;Type de valeur = «REG \ _SZ» Name = «bar» Data = «NewValue»/&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-288">&lt;Value Type="REG\_SZ" Name="Bar" Data="NewValue" /&gt;</span></span>

    <span data-ttu-id="c2f1e-289">&lt;/Key&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-289">&lt;/Key&gt;</span></span>

     <span data-ttu-id="c2f1e-290">&lt;Chemin clé = "\\REGISTRY\\USER\\\ [{AppVCurrentUserSID} \] \\Software\\EmptyKey"/&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-290">&lt;Key Path="\\REGISTRY\\USER\\\[{AppVCurrentUserSID}\]\\Software\\EmptyKey" /&gt;</span></span>

    <span data-ttu-id="c2f1e-291">&lt;/Include&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-291">&lt;/Include&gt;</span></span>

   <span data-ttu-id="c2f1e-292">&lt;Annuler&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-292">&lt;Delete&gt;</span></span>

     <span data-ttu-id="c2f1e-293">&lt;/Registry&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-293">&lt;/Registry&gt;</span></span>

   **<span data-ttu-id="c2f1e-294">Système de fichiers virtuel</span><span class="sxs-lookup"><span data-stu-id="c2f1e-294">Virtual File System</span></span>**

         &lt;FileSystem Enabled="true" /&gt;

   **<span data-ttu-id="c2f1e-295">Polices virtuelles</span><span class="sxs-lookup"><span data-stu-id="c2f1e-295">Virtual Fonts</span></span>**

         &lt;Fonts Enabled="false" /&gt;

   **<span data-ttu-id="c2f1e-296">Variables d’environnement virtuel</span><span class="sxs-lookup"><span data-stu-id="c2f1e-296">Virtual Environment Variables</span></span>**

   <span data-ttu-id="c2f1e-297">&lt;EnvironmentVariables activé = "vrai"&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-297">&lt;EnvironmentVariables Enabled="true"&gt;</span></span>

   <span data-ttu-id="c2f1e-298">&lt;Agir&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-298">&lt;Include&gt;</span></span>

          &lt;Variable Name="UserPath" Value="%path%;%UserProfile%" /&gt;

          &lt;Variable Name="UserLib" Value="%UserProfile%\\ABC" /&gt;

          &lt;/Include&gt;

         &lt;Delete&gt;

          &lt;Variable Name="lib" /&gt;

           &lt;/Delete&gt;

           &lt;/EnvironmentVariables&gt;

   **<span data-ttu-id="c2f1e-299">Services virtuels</span><span class="sxs-lookup"><span data-stu-id="c2f1e-299">Virtual services</span></span>**

         &lt;Services Enabled="false" /&gt;

3. <span data-ttu-id="c2f1e-300">**Userscripts** : les scripts peuvent être utilisés pour configurer ou altérer l’environnement virtuel, ainsi que pour exécuter des scripts au moment du déploiement ou de la suppression, avant qu’une application s’exécute, ou qu’elle puisse être utilisée pour «nettoyer» l’environnement après l’arrêt de l’application.</span><span class="sxs-lookup"><span data-stu-id="c2f1e-300">**UserScripts** – Scripts can be used to setup or alter the virtual environment as well as execute scripts at time of deployment or removal, before an application executes, or they can be used to “clean up” the environment after the application terminates.</span></span> <span data-ttu-id="c2f1e-301">Pour voir un exemple de script, veuillez vous référer au fichier de configuration de l’utilisateur qui est généré par le Sequencer.</span><span class="sxs-lookup"><span data-stu-id="c2f1e-301">Please reference a sample User configuration file that is output by the sequencer to see a sample script.</span></span> <span data-ttu-id="c2f1e-302">La section scripts ci-dessous fournit des informations supplémentaires sur les différents déclencheurs qui peuvent être utilisés.</span><span class="sxs-lookup"><span data-stu-id="c2f1e-302">The Scripts section below provides more information on the various triggers that can be used.</span></span>

4. <span data-ttu-id="c2f1e-303">**ManagingAuthority** -peut être utilisé lorsque 2 versions de votre package sont coexistantes sur le même ordinateur, l’une ayant été déployée vers App-v 4,6 et l’autre déployée sur app-v 5,0.</span><span class="sxs-lookup"><span data-stu-id="c2f1e-303">**ManagingAuthority** – Can be used when 2 versions of your package are co-existing on the same machine, one deployed to App-V 4.6 and the other deployed on App-V 5.0.</span></span> <span data-ttu-id="c2f1e-304">Pour permettre à App-V vNext de prendre en charge les points d’extension 4,6 App-V pour le package nommé, entrez ce qui suit dans le fichier UserConfig (où PackageName est le GUID du package dans App-V 4,6:</span><span class="sxs-lookup"><span data-stu-id="c2f1e-304">To Allow App-V vNext to take over App-V 4.6 extension points for the named package enter the following in the UserConfig file (where PackageName is the Package GUID in App-V 4.6:</span></span>

   <span data-ttu-id="c2f1e-305">&lt;ManagingAuthority TakeoverExtensionPointsFrom46 = "true" PackageName = "032630c0-B8E2-417C-ACEF-76fc5297fe81"/&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-305">&lt;ManagingAuthority TakeoverExtensionPointsFrom46="true" PackageName="032630c0-b8e2-417c-acef-76fc5297fe81" /&gt;</span></span>

### <span data-ttu-id="c2f1e-306">Fichier de configuration du déploiement dynamique</span><span class="sxs-lookup"><span data-stu-id="c2f1e-306">Dynamic Deployment Configuration file</span></span>

<span data-ttu-id="c2f1e-307">**Header** : l’en-tête d’un fichier de configuration de déploiement est le suivant:</span><span class="sxs-lookup"><span data-stu-id="c2f1e-307">**Header** - The header of a Deployment Configuration file is as follows:</span></span>

<span data-ttu-id="c2f1e-308">&lt;? XML version = "1.0" Encoding = "UTF-8"? &gt; &lt; DeploymentConfiguration **PackageId**= "1F8488bf-2257-46B4-B27F-09c9dbaae707" DisplayName = "réservé" xmlns = " <https://schemas.microsoft.com/appv/2010/deploymentconfiguration"&gt> ;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-308">&lt;?xml version="1.0" encoding="utf-8"?&gt;&lt;DeploymentConfiguration **PackageId**="1f8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName="Reserved" xmlns="<https://schemas.microsoft.com/appv/2010/deploymentconfiguration"&gt>;</span></span>

<span data-ttu-id="c2f1e-309">**PackageId** est de la même valeur qu’existe dans le fichier manifeste.</span><span class="sxs-lookup"><span data-stu-id="c2f1e-309">The **PackageId** is the same value as exists in the manifest file.</span></span>

<span data-ttu-id="c2f1e-310">**Corps** -le corps du fichier de configuration de déploiement comporte deux sections:</span><span class="sxs-lookup"><span data-stu-id="c2f1e-310">**Body** - The body of the deployment configuration file includes two sections:</span></span>

-   <span data-ttu-id="c2f1e-311">Section Configuration utilisateur: autorise le même contenu que le fichier de configuration utilisateur décrit dans la section précédente.</span><span class="sxs-lookup"><span data-stu-id="c2f1e-311">User Configuration section –allows the same content as the User Configuration file described in the previous section.</span></span> <span data-ttu-id="c2f1e-312">Lorsque le package est publié par un utilisateur, tous les paramètres de configuration nouvel appextensions de cette section remplacent les paramètres correspondants dans le manifeste du package, sauf si un fichier de configuration utilisateur est également fourni.</span><span class="sxs-lookup"><span data-stu-id="c2f1e-312">When the package is published to a user, any appextensions configuration settings in this section will override corresponding settings in the Manifest within the package unless a user configuration file is also provided.</span></span> <span data-ttu-id="c2f1e-313">Si un fichier UserConfig est également fourni, il est utilisé à la place des paramètres utilisateur dans le fichier de configuration de déploiement.</span><span class="sxs-lookup"><span data-stu-id="c2f1e-313">If a UserConfig file is also provided, it will be used instead of the User settings in the deployment configuration file.</span></span> <span data-ttu-id="c2f1e-314">Si le package est publié globalement, seul le contenu du fichier de configuration de déploiement sera utilisé en combinaison avec le manifeste.</span><span class="sxs-lookup"><span data-stu-id="c2f1e-314">If the package is published globally, then only the contents of the deployment configuration file will be used in combination with the manifest.</span></span>

-   <span data-ttu-id="c2f1e-315">Section Configuration de l’ordinateur: contient des informations qui peuvent être configurées uniquement pour la totalité d’un ordinateur, et non pour un utilisateur spécifique de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c2f1e-315">Machine Configuration section–contains information that can be configured only for an entire machine, not for a specific user on the machine.</span></span> <span data-ttu-id="c2f1e-316">Par exemple, HKEY \ _LOCAL \ _MACHINE clés de Registre dans le VFS.</span><span class="sxs-lookup"><span data-stu-id="c2f1e-316">For example, HKEY\_LOCAL\_MACHINE registry keys in the VFS.</span></span>

<span data-ttu-id="c2f1e-317">&lt;DeploymentConfiguration **PackageId**= "1F8488bf-2257-46B4-B27F-09c9dbaae707" DisplayName = "réservé" xmlns = " <https://schemas.microsoft.com/appv/2010/deploymentconfiguration"&gt> ;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-317">&lt;DeploymentConfiguration **PackageId**="1f8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName="Reserved" xmlns="<https://schemas.microsoft.com/appv/2010/deploymentconfiguration"&gt>;</span></span>

<span data-ttu-id="c2f1e-318">&lt;UserConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-318">&lt;UserConfiguration&gt;</span></span>

  <span data-ttu-id="c2f1e-319">..</span><span class="sxs-lookup"><span data-stu-id="c2f1e-319">..</span></span>

<span data-ttu-id="c2f1e-320">&lt;/UserConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-320">&lt;/UserConfiguration&gt;</span></span>

<span data-ttu-id="c2f1e-321">&lt;MachineConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-321">&lt;MachineConfiguration&gt;</span></span>

<span data-ttu-id="c2f1e-322">..</span><span class="sxs-lookup"><span data-stu-id="c2f1e-322">..</span></span>

<span data-ttu-id="c2f1e-323">&lt;/MachineConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-323">&lt;/MachineConfiguration&gt;</span></span>

<span data-ttu-id="c2f1e-324">..</span><span class="sxs-lookup"><span data-stu-id="c2f1e-324">..</span></span>

<span data-ttu-id="c2f1e-325">&lt;/MachineConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-325">&lt;/MachineConfiguration&gt;</span></span>

<span data-ttu-id="c2f1e-326">&lt;/DeploymentConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-326">&lt;/DeploymentConfiguration&gt;</span></span>

<span data-ttu-id="c2f1e-327">**Configuration utilisateur** -utilisez la section précédente du **fichier de configuration utilisateur dynamique** pour plus d’informations sur les paramètres fournis dans la section Configuration de l’utilisateur du fichier de configuration du déploiement.</span><span class="sxs-lookup"><span data-stu-id="c2f1e-327">**User Configuration** - use the previous **Dynamic User Configuration file** section for information on settings that are provided in the user configuration section of the Deployment Configuration file.</span></span>

<span data-ttu-id="c2f1e-328">Configuration de l’ordinateur: la section Configuration de l’ordinateur du fichier de configuration du déploiement permet de configurer des informations qui ne peuvent être définies que sur un ordinateur entier, et non pour un utilisateur spécifique de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c2f1e-328">Machine Configuration - the Machine configuration section of the Deployment Configuration File is used to configure information that can be set only for an entire machine, not for a specific user on the computer.</span></span> <span data-ttu-id="c2f1e-329">Par exemple, HKEY \ _LOCAL \ _MACHINE clés de Registre dans le registre virtuel.</span><span class="sxs-lookup"><span data-stu-id="c2f1e-329">For example, HKEY\_LOCAL\_MACHINE registry keys in the Virtual Registry.</span></span> <span data-ttu-id="c2f1e-330">Quatre sous-sections sont autorisées dans cet élément.</span><span class="sxs-lookup"><span data-stu-id="c2f1e-330">There are four subsections allowed in under this element</span></span>

1.  <span data-ttu-id="c2f1e-331">Les sous- **systèmes** -nouvel appextensions et les autres sous-systèmes sont organisés en tant que sous-nœuds dans les sous &lt; -systèmes &gt; :</span><span class="sxs-lookup"><span data-stu-id="c2f1e-331">**Subsystems** - AppExtensions and other subsystems are arranged as subnodes under &lt;Subsystems&gt;:</span></span>

    <span data-ttu-id="c2f1e-332">&lt;MachineConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-332">&lt;MachineConfiguration&gt;</span></span>

      <span data-ttu-id="c2f1e-333">&lt;Sous-systèmes&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-333">&lt;Subsystems&gt;</span></span>

      <span data-ttu-id="c2f1e-334">..</span><span class="sxs-lookup"><span data-stu-id="c2f1e-334">..</span></span>

      <span data-ttu-id="c2f1e-335">&lt;/Subsystems&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-335">&lt;/Subsystems&gt;</span></span>

    <span data-ttu-id="c2f1e-336">..</span><span class="sxs-lookup"><span data-stu-id="c2f1e-336">..</span></span>

    <span data-ttu-id="c2f1e-337">&lt;/MachineConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-337">&lt;/MachineConfiguration&gt;</span></span>

    <span data-ttu-id="c2f1e-338">La section suivante présente les différents exemples d’utilisation et de sous-systèmes.</span><span class="sxs-lookup"><span data-stu-id="c2f1e-338">The following section displays the various subsystems and usage samples.</span></span>

    <span data-ttu-id="c2f1e-339">**Extensions**:</span><span class="sxs-lookup"><span data-stu-id="c2f1e-339">**Extensions**:</span></span>

    <span data-ttu-id="c2f1e-340">Certaines extensions de contrôle de sous-systèmes (sous-systèmes d’extension) qui ne peuvent être appliquées que par tous les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="c2f1e-340">Some subsystems (Extension Subsystems) control Extensions which can only apply to all users.</span></span> <span data-ttu-id="c2f1e-341">Le sous-système est une fonctionnalité de l’application.</span><span class="sxs-lookup"><span data-stu-id="c2f1e-341">The subsystem is application capabilities.</span></span> <span data-ttu-id="c2f1e-342">Dans la mesure où cela peut s’appliquer uniquement à tous les utilisateurs, le package doit être publié globalement pour que ce type d’extension soit intégré au système local.</span><span class="sxs-lookup"><span data-stu-id="c2f1e-342">Because this can only apply to all users, the package must be published globally in order for this type of extension to be integrated into the local system.</span></span> <span data-ttu-id="c2f1e-343">Les mêmes règles relatives aux contrôles et aux paramètres qui s’appliquent aux extensions de configuration utilisateur s’appliquent également à celles de la section MachineConfiguration.</span><span class="sxs-lookup"><span data-stu-id="c2f1e-343">The same rules for controls and settings that apply to the Extensions in the User Configuration also apply to those in the MachineConfiguration section.</span></span>

    <span data-ttu-id="c2f1e-344">**Fonctionnalités**de l’application: utilisée par défaut dans l’interface du système d’exploitation Windows.</span><span class="sxs-lookup"><span data-stu-id="c2f1e-344">**Application Capabilities**: Used by default programs in windows operating system Interface.</span></span> <span data-ttu-id="c2f1e-345">Permet à une application de s’enregistrer en tant qu’il est en mesure d’ouvrir certaines extensions de fichier (par exemple, pour le menu Démarrer, emplacement du navigateur Internet, capable d’ouvrir certains types MIME Windows).</span><span class="sxs-lookup"><span data-stu-id="c2f1e-345">Allows an application to register itself as capable of opening certain file extensions, as a contender for the start menu internet browser slot, as capable of opening certain windows MIME types.</span></span><span data-ttu-id="c2f1e-346">Par ailleurs, cette extension rend l’application virtuelle visible dans l’interface utilisateur définir les programmes par défaut.</span><span class="sxs-lookup"><span data-stu-id="c2f1e-346"> This extension also makes the virtual application visible in the Set Default Programs UI.:</span></span>

    <span data-ttu-id="c2f1e-347">&lt;ApplicationCapabilities activé = "vrai"&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-347">&lt;ApplicationCapabilities Enabled="true"&gt;</span></span>

      <span data-ttu-id="c2f1e-348">&lt;Extensions&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-348">&lt;Extensions&gt;</span></span>

       <span data-ttu-id="c2f1e-349">&lt;Extension category = "AppV. ApplicationCapabilities"&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-349">&lt;Extension Category="AppV.ApplicationCapabilities"&gt;</span></span>

        &lt;ApplicationCapabilities&gt;

         &lt;ApplicationId&gt;\[{PackageRoot}\]\\LitView\\LitViewBrowser.exe&lt;/ApplicationId&gt;

         &lt;Reference&gt;

          &lt;Name&gt;LitView Browser&lt;/Name&gt;

          &lt;Path&gt;SOFTWARE\\LitView\\Browser\\Capabilities&lt;/Path&gt;

         &lt;/Reference&gt;

       <span data-ttu-id="c2f1e-350">&lt;CapabilityGroup&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-350">&lt;CapabilityGroup&gt;</span></span>

        &lt;Capabilities&gt;

         &lt;Name&gt;@\[{ProgramFilesX86}\]\\LitView\\LitViewBrowser.exe,-12345&lt;/Name&gt;

         &lt;Description&gt;@\[{ProgramFilesX86}\]\\LitView\\LitViewBrowser.exe,-12346&lt;/Description&gt;

         &lt;Hidden&gt;0&lt;/Hidden&gt;

         &lt;EMailSoftwareClient&gt;Lit View E-Mail Client&lt;/EMailSoftwareClient&gt;

         &lt;FileAssociationList&gt;

          &lt;FileAssociation Extension=".htm" ProgID="LitViewHTML" /&gt;

          &lt;FileAssociation Extension=".html" ProgID="LitViewHTML" /&gt;

          &lt;FileAssociation Extension=".shtml" ProgID="LitViewHTML" /&gt;

         &lt;/FileAssociationList&gt;

         &lt;MIMEAssociationList&gt;

          &lt;MIMEAssociation Type="audio/mp3" ProgID="LitViewHTML" /&gt;

          &lt;MIMEAssociation Type="audio/mpeg" ProgID="LitViewHTML" /&gt;

         &lt;/MIMEAssociationList&gt;

        &lt;URLAssociationList&gt;

          &lt;URLAssociation Scheme="http" ProgID="LitViewHTML.URL.http" /&gt;

         &lt;/URLAssociationList&gt;

         &lt;/Capabilities&gt;

      <span data-ttu-id="c2f1e-351">&lt;/CapabilityGroup&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-351">&lt;/CapabilityGroup&gt;</span></span>

       <span data-ttu-id="c2f1e-352">&lt;/ApplicationCapabilities&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-352">&lt;/ApplicationCapabilities&gt;</span></span>

      <span data-ttu-id="c2f1e-353">&lt;/Extension&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-353">&lt;/Extension&gt;</span></span>

    <span data-ttu-id="c2f1e-354">&lt;/Extensions&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-354">&lt;/Extensions&gt;</span></span>

    <span data-ttu-id="c2f1e-355">&lt;/ApplicationCapabilities&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-355">&lt;/ApplicationCapabilities&gt;</span></span>

    <span data-ttu-id="c2f1e-356">**Autres paramètres**:</span><span class="sxs-lookup"><span data-stu-id="c2f1e-356">**Other Settings**:</span></span>

    <span data-ttu-id="c2f1e-357">Outre les extensions, d’autres sous-systèmes peuvent être modifiés:</span><span class="sxs-lookup"><span data-stu-id="c2f1e-357">In addition to Extensions, other subsystems can be edited:</span></span>

    <span data-ttu-id="c2f1e-358">**Registre virtuel d’ordinateur**à l’échelle: utilisé lorsque vous voulez définir une clé de Registre dans le registre virtuel dans HKEY \ _Local \ _Machine</span><span class="sxs-lookup"><span data-stu-id="c2f1e-358">**Machine Wide Virtual Registry**: Used when you want to set a registry key in the virtual registry within HKEY\_Local\_Machine</span></span>

    <span data-ttu-id="c2f1e-359">&lt;Registry&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-359">&lt;Registry&gt;</span></span>

    <span data-ttu-id="c2f1e-360">&lt;Agir&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-360">&lt;Include&gt;</span></span>

      <span data-ttu-id="c2f1e-361">&lt;Chemin clé = «\\REGISTRY\\Machine\\Software\\ABC»&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-361">&lt;Key Path="\\REGISTRY\\Machine\\Software\\ABC"&gt;</span></span>

        &lt;Value Type="REG\_SZ" Name="Bar" Data="Baz" /&gt;

       <span data-ttu-id="c2f1e-362">&lt;/Key&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-362">&lt;/Key&gt;</span></span>

      <span data-ttu-id="c2f1e-363">&lt;Clé path = "\\REGISTRY\\Machine\\Software\\EmptyKey"/&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-363">&lt;Key Path="\\REGISTRY\\Machine\\Software\\EmptyKey" /&gt;</span></span>

     <span data-ttu-id="c2f1e-364">&lt;/Include&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-364">&lt;/Include&gt;</span></span>

    <span data-ttu-id="c2f1e-365">&lt;Annuler&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-365">&lt;Delete&gt;</span></span>

    <span data-ttu-id="c2f1e-366">&lt;/Registry&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-366">&lt;/Registry&gt;</span></span>

    **<span data-ttu-id="c2f1e-367">Objets de noyau virtuel de l’ordinateur</span><span class="sxs-lookup"><span data-stu-id="c2f1e-367">Machine Wide Virtual Kernel Objects</span></span>**

    <span data-ttu-id="c2f1e-368">&lt;Objets&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-368">&lt;Objects&gt;</span></span>

    <span data-ttu-id="c2f1e-369">&lt;NotIsolate&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-369">&lt;NotIsolate&gt;</span></span>

       <span data-ttu-id="c2f1e-370">&lt;Nom de l’objet = "testObject"/&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-370">&lt;Object Name="testObject" /&gt;</span></span>

     <span data-ttu-id="c2f1e-371">&lt;/NotIsolate&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-371">&lt;/NotIsolate&gt;</span></span>

    <span data-ttu-id="c2f1e-372">&lt;/Objects&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-372">&lt;/Objects&gt;</span></span>

2.  <span data-ttu-id="c2f1e-373">**ProductSourceURLOptOut**: indique si l’URL du package peut être modifiée globalement via PackageSourceRoot (pour prendre en charge les scénarios de succursales).</span><span class="sxs-lookup"><span data-stu-id="c2f1e-373">**ProductSourceURLOptOut**: Indicates whether the URL for the package can be modified globally through PackageSourceRoot (to support branch office scenarios).</span></span> <span data-ttu-id="c2f1e-374">La valeur par défaut est false et la modification du paramètre est appliquée au prochain lancement.</span><span class="sxs-lookup"><span data-stu-id="c2f1e-374">Default is false and the setting change takes effect on the next launch.</span></span>  

    <span data-ttu-id="c2f1e-375">&lt;MachineConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-375">&lt;MachineConfiguration&gt;</span></span>

      <span data-ttu-id="c2f1e-376">..</span><span class="sxs-lookup"><span data-stu-id="c2f1e-376">..</span></span> 

      <span data-ttu-id="c2f1e-377">&lt;ProductSourceURLOptOut activé = "vrai"/&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-377">&lt;ProductSourceURLOptOut Enabled="true" /&gt;</span></span>

      <span data-ttu-id="c2f1e-378">..</span><span class="sxs-lookup"><span data-stu-id="c2f1e-378">..</span></span>

    <span data-ttu-id="c2f1e-379">&lt;/MachineConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-379">&lt;/MachineConfiguration&gt;</span></span>

3.  <span data-ttu-id="c2f1e-380">**MachineScripts** : package peut être configuré pour exécuter des scripts au moment du déploiement, de la publication ou de la suppression.</span><span class="sxs-lookup"><span data-stu-id="c2f1e-380">**MachineScripts** – Package can be configured to execute scripts at time of deployment, publishing or removal.</span></span> <span data-ttu-id="c2f1e-381">Veuillez référencer un exemple de fichier de configuration de déploiement généré par le Sequencer pour voir un exemple de script.</span><span class="sxs-lookup"><span data-stu-id="c2f1e-381">Please reference a sample deployment configuration file that is generated by the sequencer to see a sample script.</span></span> <span data-ttu-id="c2f1e-382">La section scripts ci-dessous fournit des informations supplémentaires sur les différents déclencheurs qui peuvent être utilisés.</span><span class="sxs-lookup"><span data-stu-id="c2f1e-382">The Scripts section below provides more information on the various triggers that can be used</span></span>

4.  <span data-ttu-id="c2f1e-383">**TerminateChildProcess**:-un exécutable de l’application peut être spécifié, dont le processus enfant va être arrêté lorsque le processus exe de l’application est arrêté.</span><span class="sxs-lookup"><span data-stu-id="c2f1e-383">**TerminateChildProcess**:- An application executable can be specified, whose child processes will be terminated when the application exe process is terminated.</span></span>

    <span data-ttu-id="c2f1e-384">&lt;MachineConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-384">&lt;MachineConfiguration&gt;</span></span>

      <span data-ttu-id="c2f1e-385">..</span><span class="sxs-lookup"><span data-stu-id="c2f1e-385">..</span></span>   

      <span data-ttu-id="c2f1e-386">&lt;TerminateChildProcesses&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-386">&lt;TerminateChildProcesses&gt;</span></span>

        &lt;Application Path="\[{PackageRoot}\]\\Contoso\\ContosoApp.EXE" /&gt;

        &lt;Application Path="\[{PackageRoot}\]\\LitView\\LitViewBrowser.exe" /&gt;

        &lt;Application Path="\[{ProgramFilesX86}\]\\Microsoft Contoso\\Contoso\\contosomail.EXE" /&gt;

      <span data-ttu-id="c2f1e-387">&lt;/TerminateChildProcesses&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-387">&lt;/TerminateChildProcesses&gt;</span></span>

      <span data-ttu-id="c2f1e-388">..</span><span class="sxs-lookup"><span data-stu-id="c2f1e-388">..</span></span>

    <span data-ttu-id="c2f1e-389">&lt;/MachineConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="c2f1e-389">&lt;/MachineConfiguration&gt;</span></span>

### <span data-ttu-id="c2f1e-390">Scripts</span><span class="sxs-lookup"><span data-stu-id="c2f1e-390">Scripts</span></span>

<span data-ttu-id="c2f1e-391">Le tableau suivant décrit les différents événements de script et le contexte dans lequel ils peuvent être exécutés.</span><span class="sxs-lookup"><span data-stu-id="c2f1e-391">The following table describes the various script events and the context under which they can be run.</span></span>

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c2f1e-392">Temps d’exécution du script</span><span class="sxs-lookup"><span data-stu-id="c2f1e-392">Script Execution Time</span></span></th>
<th align="left"><span data-ttu-id="c2f1e-393">Peuvent être spécifiées dans la configuration de déploiement</span><span class="sxs-lookup"><span data-stu-id="c2f1e-393">Can be specified in Deployment Configuration</span></span></th>
<th align="left"><span data-ttu-id="c2f1e-394">Peuvent être spécifiés dans la configuration de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="c2f1e-394">Can be specified in User Configuration</span></span></th>
<th align="left"><span data-ttu-id="c2f1e-395">Peut s’exécuter dans l’environnement virtuel du package</span><span class="sxs-lookup"><span data-stu-id="c2f1e-395">Can run in the Virtual Environment of the package</span></span></th>
<th align="left"><span data-ttu-id="c2f1e-396">Peut être exécuté dans le contexte d’une application spécifique.</span><span class="sxs-lookup"><span data-stu-id="c2f1e-396">Can be run in the context of a specific application</span></span></th>
<th align="left"><span data-ttu-id="c2f1e-397">S’exécute dans le contexte système/utilisateur (configuration du déploiement, configuration de l’utilisateur).</span><span class="sxs-lookup"><span data-stu-id="c2f1e-397">Runs in system/user context: (Deployment Configuration, User Configuration)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c2f1e-398">AddPackage</span><span class="sxs-lookup"><span data-stu-id="c2f1e-398">AddPackage</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2f1e-399">X</span><span class="sxs-lookup"><span data-stu-id="c2f1e-399">X</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="c2f1e-400">(SYSTÈME, NO/A)</span><span class="sxs-lookup"><span data-stu-id="c2f1e-400">(SYSTEM, N/A)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c2f1e-401">PublishPackage</span><span class="sxs-lookup"><span data-stu-id="c2f1e-401">PublishPackage</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2f1e-402">X</span><span class="sxs-lookup"><span data-stu-id="c2f1e-402">X</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2f1e-403">X</span><span class="sxs-lookup"><span data-stu-id="c2f1e-403">X</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="c2f1e-404">(Système, utilisateur)</span><span class="sxs-lookup"><span data-stu-id="c2f1e-404">(SYSTEM, User)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c2f1e-405">UnpublishPackage</span><span class="sxs-lookup"><span data-stu-id="c2f1e-405">UnpublishPackage</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2f1e-406">X</span><span class="sxs-lookup"><span data-stu-id="c2f1e-406">X</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2f1e-407">X</span><span class="sxs-lookup"><span data-stu-id="c2f1e-407">X</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="c2f1e-408">(Système, utilisateur)</span><span class="sxs-lookup"><span data-stu-id="c2f1e-408">(SYSTEM, User)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c2f1e-409">RemovePackage</span><span class="sxs-lookup"><span data-stu-id="c2f1e-409">RemovePackage</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2f1e-410">X</span><span class="sxs-lookup"><span data-stu-id="c2f1e-410">X</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="c2f1e-411">(SYSTÈME, NO/A)</span><span class="sxs-lookup"><span data-stu-id="c2f1e-411">(SYSTEM, N/A)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c2f1e-412">StartProcess</span><span class="sxs-lookup"><span data-stu-id="c2f1e-412">StartProcess</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2f1e-413">X</span><span class="sxs-lookup"><span data-stu-id="c2f1e-413">X</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2f1e-414">X</span><span class="sxs-lookup"><span data-stu-id="c2f1e-414">X</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2f1e-415">X</span><span class="sxs-lookup"><span data-stu-id="c2f1e-415">X</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2f1e-416">X</span><span class="sxs-lookup"><span data-stu-id="c2f1e-416">X</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2f1e-417">(Utilisateur, utilisateur)</span><span class="sxs-lookup"><span data-stu-id="c2f1e-417">(User, User)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c2f1e-418">ExitProcess</span><span class="sxs-lookup"><span data-stu-id="c2f1e-418">ExitProcess</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2f1e-419">X</span><span class="sxs-lookup"><span data-stu-id="c2f1e-419">X</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2f1e-420">X</span><span class="sxs-lookup"><span data-stu-id="c2f1e-420">X</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="c2f1e-421">X</span><span class="sxs-lookup"><span data-stu-id="c2f1e-421">X</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2f1e-422">(Utilisateur, utilisateur)</span><span class="sxs-lookup"><span data-stu-id="c2f1e-422">(User, User)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c2f1e-423">StartVirtualEnvironment</span><span class="sxs-lookup"><span data-stu-id="c2f1e-423">StartVirtualEnvironment</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2f1e-424">X</span><span class="sxs-lookup"><span data-stu-id="c2f1e-424">X</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2f1e-425">X</span><span class="sxs-lookup"><span data-stu-id="c2f1e-425">X</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2f1e-426">X</span><span class="sxs-lookup"><span data-stu-id="c2f1e-426">X</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="c2f1e-427">(Utilisateur, utilisateur)</span><span class="sxs-lookup"><span data-stu-id="c2f1e-427">(User, User)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c2f1e-428">TerminateVirtualEnvironment</span><span class="sxs-lookup"><span data-stu-id="c2f1e-428">TerminateVirtualEnvironment</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2f1e-429">X</span><span class="sxs-lookup"><span data-stu-id="c2f1e-429">X</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2f1e-430">X</span><span class="sxs-lookup"><span data-stu-id="c2f1e-430">X</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="c2f1e-431">(Utilisateur, utilisateur)</span><span class="sxs-lookup"><span data-stu-id="c2f1e-431">(User, User)</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="c2f1e-432">Créer un fichier de configuration dynamique à l’aide d’un fichier manifeste App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="c2f1e-432">Create a Dynamic Configuration file using an App-V 5.0 Manifest file</span></span>

<span data-ttu-id="c2f1e-433">Vous pouvez créer le fichier de configuration dynamique à l’aide de l’une des trois méthodes suivantes: manuellement, à l’aide de la console de gestion App-V 5,0 ou du séquençage d’un package, qui est généré avec 2 exemples de fichiers.</span><span class="sxs-lookup"><span data-stu-id="c2f1e-433">You can create the Dynamic Configuration file using one of three methods: either manually, using the App-V 5.0 Management Console or sequencing a package, which will be generated with 2 sample files.</span></span>

<span data-ttu-id="c2f1e-434">Pour plus d’informations sur la création du fichier à l’aide de la console de gestion de l’application-V 5,0, voir [créer un fichier de configuration personnalisé à l’aide de la console de gestion App-v 5,0](how-to-create-a-custom-configuration-file-by-using-the-app-v-50-management-console.md).</span><span class="sxs-lookup"><span data-stu-id="c2f1e-434">For more information about how to create the file using the App-V 5.0 Management Console see, [How to Create a Custom Configuration File by Using the App-V 5.0 Management Console](how-to-create-a-custom-configuration-file-by-using-the-app-v-50-management-console.md).</span></span>

<span data-ttu-id="c2f1e-435">Pour créer le fichier manuellement, les informations ci-dessus dans les sections précédentes peuvent être combinées dans un seul fichier.</span><span class="sxs-lookup"><span data-stu-id="c2f1e-435">To create the file manually, the information above in previous sections can be combined into a single file.</span></span> <span data-ttu-id="c2f1e-436">Nous vous recommandons d’utiliser des fichiers générés par le Sequencer.</span><span class="sxs-lookup"><span data-stu-id="c2f1e-436">We recommend you use files generated by the sequencer.</span></span>






## <span data-ttu-id="c2f1e-437">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c2f1e-437">Related topics</span></span>


[<span data-ttu-id="c2f1e-438">Comment appliquer le fichier de configuration du déploiement à l'aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="c2f1e-438">How to Apply the Deployment Configuration File by Using PowerShell</span></span>](how-to-apply-the-deployment-configuration-file-by-using-powershell.md)

[<span data-ttu-id="c2f1e-439">Comment appliquer le fichier de configuration utilisateur à l'aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="c2f1e-439">How to Apply the User Configuration File by Using PowerShell</span></span>](how-to-apply-the-user-configuration-file-by-using-powershell.md)

[<span data-ttu-id="c2f1e-440">Opérations d'App-V5.0</span><span class="sxs-lookup"><span data-stu-id="c2f1e-440">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 





