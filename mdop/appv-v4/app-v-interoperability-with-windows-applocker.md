---
title: Interopérabilité d'App-V et de Windows AppLocker
description: Interopérabilité d'App-V et de Windows AppLocker
author: dansimp
ms.assetid: 9a488034-607d-411c-b495-ff184c726f49
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 6f67bb87c0a4474acee3c4982b65c930e86c4917
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809281"
---
# <span data-ttu-id="fe862-103">Interopérabilité d'App-V et de Windows AppLocker</span><span class="sxs-lookup"><span data-stu-id="fe862-103">App-V Interoperability with Windows AppLocker</span></span>


<span data-ttu-id="fe862-104">La version 4,5 SP1 du client Microsoft Application Virtualization (App-V) prend en charge la fonctionnalité AppLocker de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="fe862-104">Version 4.5 SP1 of the Microsoft Application Virtualization (App-V) client supports the AppLocker feature of Windows 7.</span></span> <span data-ttu-id="fe862-105">La fonctionnalité AppLocker permet aux administrateurs informatiques de spécifier les applications qui ne sont pas exécutées sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="fe862-105">The AppLocker feature enables IT administrators to specify which applications are restricted from running on computers.</span></span> <span data-ttu-id="fe862-106">Ce document décrit comment configurer les règles AppLocker pour fonctionner avec l’environnement virtuel App-V et les applications virtualisées.</span><span class="sxs-lookup"><span data-stu-id="fe862-106">This document describes how to configure the AppLocker rules to work with the App-V virtual environment and virtualized applications.</span></span>

<span data-ttu-id="fe862-107">**Remarques**  Windows AppLocker doit d’abord être activé avant de configurer des règles Windows AppLocker pour les applications virtuelles.</span><span class="sxs-lookup"><span data-stu-id="fe862-107">**Note** Windows AppLocker must first be enabled before configuring Windows AppLocker rules for virtual applications.</span></span> <span data-ttu-id="fe862-108">Pour plus d’informations sur l’activation de Windows AppLocker, [Windows AppLocker](https://go.microsoft.com/fwlink/?LinkId=156732) ( https://go.microsoft.com/fwlink/?LinkId=156732) .</span><span class="sxs-lookup"><span data-stu-id="fe862-108">For more information about enabling Windows AppLocker, [Windows AppLocker](https://go.microsoft.com/fwlink/?LinkId=156732) (https://go.microsoft.com/fwlink/?LinkId=156732).</span></span>

 

## <span data-ttu-id="fe862-109">Configuration de règles Windows AppLocker pour les applications virtuelles</span><span class="sxs-lookup"><span data-stu-id="fe862-109">Configuring Windows AppLocker Rules for Virtual Applications</span></span>


<span data-ttu-id="fe862-110">Les administrateurs locaux peuvent créer des règles AppLocker Windows qui limitent l’exécution de fichiers exécutables de programme (fichiers. exe), de fichiers Windows Installer (fichiers. msi et. msp) et de scripts (. PS,. bat,. cmd,. vbs et. js).</span><span class="sxs-lookup"><span data-stu-id="fe862-110">Local administrators can create Windows AppLocker rules that restrict the running of program executables (.exe files), Windows Installer files (.msi and .msp files), and scripts (.ps, .bat, .cmd, .vbs and .js files).</span></span> <span data-ttu-id="fe862-111">L’administrateur effectue cette opération à l’aide d’un ordinateur de référence sur lequel est installé le client App-V et qui a toutes les applications virtuelles pertinentes transmises au cache client.</span><span class="sxs-lookup"><span data-stu-id="fe862-111">The administrator does this by using a reference computer that has the App-V client installed and that has all the relevant virtual applications streamed to the client cache.</span></span> <span data-ttu-id="fe862-112">L’administrateur utilise ensuite la section Windows AppLocker de la stratégie de sécurité locale du composant logiciel enfichable Microsoft Management Console (MMC) sur l’ordinateur de référence pour créer des règles.</span><span class="sxs-lookup"><span data-stu-id="fe862-112">The administrator then uses the Windows AppLocker section of the Local Security Policy Microsoft Management Console (MMC) snap-in on the reference computer to create the rules.</span></span>

<span data-ttu-id="fe862-113">Lorsque vous naviguez vers le chemin d’accès d’un répertoire ou un fichier spécifique pour lequel vous voulez créer une règle, vous pouvez accéder au lecteur App-V en utilisant son chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="fe862-113">When you browse to find a directory path or specific file for which you want to create a rule, you can access the App-V drive by using the path to the hidden share.</span></span> <span data-ttu-id="fe862-114">Par exemple, vous pouvez accéder à \\\\localhost\\Q $, où le lecteur App-V est Drive Q. Toutefois, pour créer la règle, vous devez modifier le chemin d’accès pour supprimer la référence à \\\\localhost\\Q $ et utiliser Q:\\ à la place.</span><span class="sxs-lookup"><span data-stu-id="fe862-114">For example, you can browse to \\\\localhost\\Q$, where the App-V drive is drive Q. However, to create the rule, you must edit the path to remove the reference to \\\\localhost\\Q$ and use Q:\\ instead.</span></span> <span data-ttu-id="fe862-115">Pour accéder aux fichiers de l’application, vous devez démarrer chaque application sur l’ordinateur de référence, et les droits d’administration sont requis pour accéder à \\\\localhost\\Q $.</span><span class="sxs-lookup"><span data-stu-id="fe862-115">You must start each application on the reference computer to access the application’s files, and administrative rights are required to browse to \\\\localhost\\Q$.</span></span>

 

 





