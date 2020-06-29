---
title: Affichage et configuration des journaux MED-V
description: Affichage et configuration des journaux MED-V
author: dansimp
ms.assetid: a15537ce-981d-4f55-9c3c-e7fbf94b8fe5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7984cec072827136db9ea52a535c0ea44c6bc2c3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810128"
---
# <span data-ttu-id="c6e02-103">Affichage et configuration des journaux MED-V</span><span class="sxs-lookup"><span data-stu-id="c6e02-103">Viewing and Configuring MED-V Logs</span></span>


<span data-ttu-id="c6e02-104">Lorsque vous résolvez des problèmes et rencontrez des problèmes avec MED-V, il est possible que vous trouviez utile ou nécessaire pour accéder aux journaux des événements MED-V.</span><span class="sxs-lookup"><span data-stu-id="c6e02-104">When you are troubleshooting MED-V issues and problems, you may find it helpful or necessary to access the MED-V event logs.</span></span> <span data-ttu-id="c6e02-105">Vous pouvez ouvrir l’observateur d’événements pour l’ordinateur hôte et l’ordinateur virtuel invité à l’aide du kit de tâches d’administration MED-V.</span><span class="sxs-lookup"><span data-stu-id="c6e02-105">You can open Event Viewer for the host computer and the guest virtual machine by using the MED-V Administration Toolkit.</span></span> <span data-ttu-id="c6e02-106">Vous pouvez également utiliser le kit de tâches d’administration de MED-V pour définir le niveau de journalisation des événements MED-v du journal des événements MED-v.</span><span class="sxs-lookup"><span data-stu-id="c6e02-106">You can also use the MED-V Administration Toolkit to set the logging level at which the MED-V event logs report MED-V events.</span></span>

<span data-ttu-id="c6e02-107">Pour plus d’informations sur l’ouverture du kit de tâches d’administration MED-V, voir [résolution des problèmes de med-v à l’aide du kit de tâches d’administration](troubleshooting-med-v-by-using-the-administration-toolkit.md).</span><span class="sxs-lookup"><span data-stu-id="c6e02-107">For information about how to open the MED-V Administration Toolkit, see [Troubleshooting MED-V by Using the Administration Toolkit](troubleshooting-med-v-by-using-the-administration-toolkit.md).</span></span>

## <span data-ttu-id="c6e02-108">Afficher les journaux d’événements MED-V</span><span class="sxs-lookup"><span data-stu-id="c6e02-108">Viewing MED-V Event Logs</span></span>


<span data-ttu-id="c6e02-109">Dans la fenêtre **Kit de tâches d’administration de MED-V** , cliquez sur événements d' **hébergement** pour ouvrir l’observateur d’événements de l’ordinateur hôte.</span><span class="sxs-lookup"><span data-stu-id="c6e02-109">On the **MED-V Administration Toolkit** window, click **Host Events** to open the event viewer for the host computer.</span></span> <span data-ttu-id="c6e02-110">Vous pouvez ou cliquer sur **événements invités** pour ouvrir l’observateur d’événements pour l’ordinateur virtuel invité.</span><span class="sxs-lookup"><span data-stu-id="c6e02-110">Or, click **Guest Events** to open Event Viewer for the guest virtual machine.</span></span>

<span data-ttu-id="c6e02-111">L’observateur d’événements s’ouvre et affiche les journaux des événements correspondants que vous pouvez utiliser pour résoudre les problèmes que vous pouvez rencontrer lors du déploiement ou de la gestion de MED-V.</span><span class="sxs-lookup"><span data-stu-id="c6e02-111">Event Viewer opens and displays the corresponding event logs that you can use to troubleshoot the issues that you might encounter when you deploy or manage MED-V.</span></span> <span data-ttu-id="c6e02-112">Par défaut, seuls les erreurs et les avertissements sont affichés.</span><span class="sxs-lookup"><span data-stu-id="c6e02-112">By default, only errors and warnings are displayed.</span></span> <span data-ttu-id="c6e02-113">Pour plus d’informations sur les ID d’événement et les messages spécifiques, voir [messages du journal des événements MED-V](med-v-event-log-messages.md).</span><span class="sxs-lookup"><span data-stu-id="c6e02-113">For more information about specific event IDs and messages, see [MED-V Event Log Messages](med-v-event-log-messages.md).</span></span>

<span data-ttu-id="c6e02-114">**Remarques**  Les utilisateurs finaux peuvent uniquement enregistrer les fichiers journaux des événements sur l’invité s’ils disposent d’autorisations d’administration.</span><span class="sxs-lookup"><span data-stu-id="c6e02-114">**Note** End users can only save event log files in the guest if they have administrative permissions.</span></span>

 

### <span data-ttu-id="c6e02-115">Pour ouvrir manuellement l’observateur d’événements sur l’ordinateur hôte</span><span class="sxs-lookup"><span data-stu-id="c6e02-115">To manually open the Event Viewer in the host computer</span></span>

1.  <span data-ttu-id="c6e02-116">Cliquez sur **Démarrer**, sur **panneau de configuration**, puis sur **Outils d’administration**.</span><span class="sxs-lookup"><span data-stu-id="c6e02-116">Click **Start**, click **Control Panel**, and then click **Administrative Tools**.</span></span>

2.  <span data-ttu-id="c6e02-117">Double-cliquez sur **Observateur d’événements**, puis cliquez sur **journaux des applications et des services**.</span><span class="sxs-lookup"><span data-stu-id="c6e02-117">Double-click **Event Viewer**, and then click **Applications and Services Logs**.</span></span>

3.  <span data-ttu-id="c6e02-118">Double-cliquez sur **medv**.</span><span class="sxs-lookup"><span data-stu-id="c6e02-118">Double-click **MEDV**.</span></span>

## <span data-ttu-id="c6e02-119">Configuration des journaux des événements MED-V</span><span class="sxs-lookup"><span data-stu-id="c6e02-119">Configuring MED-V Event Logs</span></span>


<span data-ttu-id="c6e02-120">Vous pouvez spécifier le niveau de journalisation des événements MED-V en sélectionnant le bouton d’option correspondant dans le kit de tâches d’administration de MED-V.</span><span class="sxs-lookup"><span data-stu-id="c6e02-120">You can specify the MED-V event logging level by selecting the corresponding option button on the MED-V Administration Toolkit.</span></span> <span data-ttu-id="c6e02-121">Vous pouvez déterminer si la journalisation des événements inclut les erreurs uniquement, les erreurs et les avertissements, ou les erreurs, avertissements et messages d’information.</span><span class="sxs-lookup"><span data-stu-id="c6e02-121">You can decide whether event logging includes errors only, errors and warnings, or errors, warnings and informational messages.</span></span> <span data-ttu-id="c6e02-122">Le niveau de journalisation des événements spécifié est défini pour l’ordinateur hôte et l’ordinateur virtuel invité.</span><span class="sxs-lookup"><span data-stu-id="c6e02-122">The event logging level specified is set for both the host computer and the guest virtual machine.</span></span>

<span data-ttu-id="c6e02-123">Vous pouvez également spécifier le niveau de journalisation des événements en modifiant la valeur du Registre EventLogLevel.</span><span class="sxs-lookup"><span data-stu-id="c6e02-123">You can also specify the event logging level by editing the EventLogLevel registry value.</span></span> <span data-ttu-id="c6e02-124">Pour plus d’informations, reportez-vous à [gestion des paramètres de configuration de l’espace de travail MED-V](managing-med-v-workspace-configuration-settings.md)</span><span class="sxs-lookup"><span data-stu-id="c6e02-124">For more information, see [Managing MED-V Workspace Configuration Settings](managing-med-v-workspace-configuration-settings.md).</span></span>

<span data-ttu-id="c6e02-125">**Remarques**  Le niveau que vous spécifiez dans la fenêtre du **Kit de tâches d’administration med-v** s’applique aux futurs enregistrements d’événements med-v.</span><span class="sxs-lookup"><span data-stu-id="c6e02-125">**Note** The level you specify on the **MED-V Administration Toolkit** window applies to future MED-V event logging.</span></span> <span data-ttu-id="c6e02-126">Si vous définissez le niveau de capture de l’ensemble des erreurs, avertissements et messages d’information, les journaux d’événements sont retirés plus rapidement et les événements plus anciens sont supprimés.</span><span class="sxs-lookup"><span data-stu-id="c6e02-126">If you set the level to capture all errors, warnings, and informational messages, then the event logs fill more quickly and older events are removed.</span></span>

 

## <span data-ttu-id="c6e02-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c6e02-127">Related topics</span></span>


[<span data-ttu-id="c6e02-128">Redémarrage et réinitialisation d'un espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="c6e02-128">Restarting and Resetting a MED-V Workspace</span></span>](restarting-and-resetting-a-med-v-workspace.md)

[<span data-ttu-id="c6e02-129">Affichage des configurations d'espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="c6e02-129">Viewing MED-V Workspace Configurations</span></span>](viewing-med-v-workspace-configurations.md)

 

 





