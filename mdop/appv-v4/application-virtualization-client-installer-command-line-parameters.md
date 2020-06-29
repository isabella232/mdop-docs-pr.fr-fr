---
title: Paramètres de ligne de commande du programme d'installation d'Application Virtualization Client
description: Paramètres de ligne de commande du programme d'installation d'Application Virtualization Client
author: dansimp
ms.assetid: 508fa404-52a5-4919-8788-2a3dfb00639b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 911d333c80060c1881c96430c1d2d0516b6a4855
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808018"
---
# <span data-ttu-id="92efc-103">Paramètres de ligne de commande du programme d'installation d'Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="92efc-103">Application Virtualization Client Installer Command-Line Parameters</span></span>


<span data-ttu-id="92efc-104">Le tableau suivant répertorie tous les paramètres de ligne de commande du programme d’installation du client Microsoft Application Virtualization disponibles, leurs valeurs et une brève description de chaque paramètre.</span><span class="sxs-lookup"><span data-stu-id="92efc-104">The following table lists all available Microsoft Application Virtualization Client installer command-line parameters, their values, and a brief description of each parameter.</span></span> <span data-ttu-id="92efc-105">Les paramètres respectent la casse et doivent être entrés en lettres minuscules.</span><span class="sxs-lookup"><span data-stu-id="92efc-105">Parameters are case-sensitive and must be entered as all-uppercase letters.</span></span> <span data-ttu-id="92efc-106">Toutes les valeurs de paramètre doivent être placées entre guillemets doubles.</span><span class="sxs-lookup"><span data-stu-id="92efc-106">All parameter values must be enclosed in double quotes.</span></span>

**<span data-ttu-id="92efc-107">Remarque</span><span class="sxs-lookup"><span data-stu-id="92efc-107">Note</span></span>**  
-   <span data-ttu-id="92efc-108">Pour App-V version 4,6, les paramètres de ligne de commande ne peuvent pas être utilisés lors d’une mise à niveau du client.</span><span class="sxs-lookup"><span data-stu-id="92efc-108">For App-V version 4.6, command-line parameters cannot be used during a client upgrade.</span></span>

-   <span data-ttu-id="92efc-109">Les paramètres *SWICACHESIZE* et *MINFREESPACEMB* ne peuvent pas être combinés sur la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="92efc-109">The *SWICACHESIZE* and *MINFREESPACEMB* parameters cannot be combined on the command line.</span></span> <span data-ttu-id="92efc-110">Si les deux sont utilisées, le paramètre *SWICACHESIZE* est ignoré.</span><span class="sxs-lookup"><span data-stu-id="92efc-110">If both are used, the *SWICACHESIZE* parameter will be ignored.</span></span>



<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="92efc-111">Paramètre</span><span class="sxs-lookup"><span data-stu-id="92efc-111">Parameter</span></span></th>
<th align="left"><span data-ttu-id="92efc-112">Doubl</span><span class="sxs-lookup"><span data-stu-id="92efc-112">Values</span></span></th>
<th align="left"><span data-ttu-id="92efc-113">Description</span><span class="sxs-lookup"><span data-stu-id="92efc-113">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><em><span data-ttu-id="92efc-114">ALLOWINDEPENDENTFILESTREAMING</span><span class="sxs-lookup"><span data-stu-id="92efc-114">ALLOWINDEPENDENTFILESTREAMING</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="92efc-115">TRUE</span><span class="sxs-lookup"><span data-stu-id="92efc-115">TRUE</span></span></p>
<p><span data-ttu-id="92efc-116">FALSE</span><span class="sxs-lookup"><span data-stu-id="92efc-116">FALSE</span></span></p></td>
<td align="left"><p><span data-ttu-id="92efc-117">Indique si la diffusion en continu à partir du fichier sera activée quelle que soit la façon dont le client a été configuré avec le <em> </em> paramètre APPLICATIONSOURCEROOT.</span><span class="sxs-lookup"><span data-stu-id="92efc-117">Indicates whether streaming from file will be enabled regardless of how the client has been configured with the <em>APPLICATIONSOURCEROOT</em> parameter.</span></span> <span data-ttu-id="92efc-118">Si elle est définie sur FALSe, le transport n’active pas la diffusion en continu à partir de fichiers, même si le paramètre OSD HREF ou <em> APPLICATIONSOURCEROOT </em> contient un chemin d’accès au fichier.</span><span class="sxs-lookup"><span data-stu-id="92efc-118">If set to FALSE, the transport will not enable streaming from files even if the OSD HREF or the <em>APPLICATIONSOURCEROOT</em> parameter contains a file path.</span></span></p>
<p><span data-ttu-id="92efc-119">Valeurs possibles:</span><span class="sxs-lookup"><span data-stu-id="92efc-119">Possible values:</span></span></p>
<ul>
<li><p><span data-ttu-id="92efc-120">TRUE: une application déployée manuellement est susceptible d’être chargée à partir du disque.</span><span class="sxs-lookup"><span data-stu-id="92efc-120">TRUE—Manually deployed application may be loaded from disk.</span></span></p></li>
<li><p><span data-ttu-id="92efc-121">FALSe: toutes les applications doivent provient du serveur de diffusion de contenu source.</span><span class="sxs-lookup"><span data-stu-id="92efc-121">FALSE—All applications must come from source streaming server.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><em><span data-ttu-id="92efc-122">APPLICATIONSOURCEROOT</span><span class="sxs-lookup"><span data-stu-id="92efc-122">APPLICATIONSOURCEROOT</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="92efc-123"><em>URL RTSP:// </em> (pour la remise de package dynamique)</span><span class="sxs-lookup"><span data-stu-id="92efc-123">RTSP:// <em>URL</em> (for dynamic package delivery)</span></span></p>
<p><span data-ttu-id="92efc-124"><em>URL </em> ou UNC <em> file:// </em> (pour le chargement à partir d’une remise de package de fichier)</span><span class="sxs-lookup"><span data-stu-id="92efc-124">File:// <em>URL</em> or <em>UNC</em> (for load from file package delivery)</span></span></p></td>
<td align="left"><p><span data-ttu-id="92efc-125">Pour permettre à un administrateur ou à un système de distribution de logiciels électronique de garantir le chargement de l’application conformément au schéma de gestion topologique, autorise une substitution du code base OSD pour l’élément HREF de l’application (emplacement source).</span><span class="sxs-lookup"><span data-stu-id="92efc-125">To enable an administrator or an electronic software distribution system to ensure that application loading is performed in compliance with the topology management scheme, allows an override of the OSD CODEBASE for the application HREF element (the source location).</span></span> <span data-ttu-id="92efc-126">Si la valeur est «», qui est la valeur par défaut, les paramètres de fichier OSD existants sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="92efc-126">If the value is “”, which is the default value, the existing OSD file settings are used.</span></span></p>
<p><span data-ttu-id="92efc-127">Une URL est composée de plusieurs parties:</span><span class="sxs-lookup"><span data-stu-id="92efc-127">A URL has several parts:</span></span></p>
<p><span data-ttu-id="92efc-128">&lt;protocole &gt; :// &lt; serveur &gt; : &lt; chemin de port &gt; / &lt; &gt; / &lt; ? requête &gt; &lt; #fragment&gt;</span><span class="sxs-lookup"><span data-stu-id="92efc-128">&lt;protocol&gt;://&lt;server&gt;:&lt;port&gt;/&lt;path&gt;/&lt;?query&gt;&lt;#fragment&gt;</span></span></p>
<p><span data-ttu-id="92efc-129">Un chemin d’accès UNC comporte trois parties:</span><span class="sxs-lookup"><span data-stu-id="92efc-129">A UNC path has three parts:</span></span></p>
<p><span data-ttu-id="92efc-130">&amp;lt; NomOrdinateur &gt; &amp; lt; partager le dossier &gt; &amp; lt; ressource&gt;</span><span class="sxs-lookup"><span data-stu-id="92efc-130">&amp;lt;computername&gt;&amp;lt;share folder&gt;&amp;lt;resource&gt;</span></span></p>
<p><span data-ttu-id="92efc-131">Si le <em> </em> paramètre APPLICATIONSOURCEROOT est spécifié sur un client, le client rompt l’URL ou le chemin UNC d’un fichier OSD dans ses parties constitutives et remplace les sections d’OSD par les <em> sections APPLICATIONSOURCEROOT correspondantes </em> .</span><span class="sxs-lookup"><span data-stu-id="92efc-131">If the <em>APPLICATIONSOURCEROOT</em> parameter is specified on a client, the client will break the URL or UNC path from an OSD file into its constituent parts and replace the OSD sections with the corresponding <em>APPLICATIONSOURCEROOT</em> sections.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="92efc-132">Important</span><span class="sxs-lookup"><span data-stu-id="92efc-132">Important</span></span></strong><br/><p><span data-ttu-id="92efc-133">Veillez à utiliser le format approprié lors de l’utilisation de file://avec un chemin UNC.</span><span class="sxs-lookup"><span data-stu-id="92efc-133">Be sure to use the correct format when using file:// with a UNC path.</span></span> <span data-ttu-id="92efc-134">Le format approprié est file:// &amp; lt; Server &gt; &amp; lt; share &gt; .</span><span class="sxs-lookup"><span data-stu-id="92efc-134">The correct format is file://&amp;lt;server&gt;&amp;lt;share&gt;.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><em><span data-ttu-id="92efc-135">ICONSOURCEROOT</span><span class="sxs-lookup"><span data-stu-id="92efc-135">ICONSOURCEROOT</span></span></em></p></td>
<td align="left"><p><em><span data-ttu-id="92efc-136">UNC</span><span class="sxs-lookup"><span data-stu-id="92efc-136">UNC</span></span></em></p>
<p><span data-ttu-id="92efc-137">URL <em> http:// </em> ou https:// <em> URL</span><span class="sxs-lookup"><span data-stu-id="92efc-137">HTTP://<em>URL</em> or HTTPS://<em>URL</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="92efc-138">Permet à un administrateur de spécifier un emplacement source pour la récupération d’icône pour un package d’application séquencé lors de la publication.</span><span class="sxs-lookup"><span data-stu-id="92efc-138">Enables an administrator to specify a source location for icon retrieval for a sequenced application package during publication.</span></span> <span data-ttu-id="92efc-139">Les racines de source d’icône prennent en charge les chemins d’accès et les URL.</span><span class="sxs-lookup"><span data-stu-id="92efc-139">Icon source roots support UNC paths and URLs (HTTP or HTTPS).</span></span> <span data-ttu-id="92efc-140">Si la valeur est «», qui est la valeur par défaut, les paramètres de fichier OSD existants sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="92efc-140">If the value is “”, which is the default value, the existing OSD file settings are used.</span></span></p>
<p><span data-ttu-id="92efc-141">Une URL est composée de plusieurs parties:</span><span class="sxs-lookup"><span data-stu-id="92efc-141">A URL has several parts:</span></span></p>
<p><span data-ttu-id="92efc-142">&lt;protocole &gt; :// &lt; serveur &gt; : &lt; chemin de port &gt; / &lt; &gt; / &lt; ? requête &gt; &lt; #fragment&gt;</span><span class="sxs-lookup"><span data-stu-id="92efc-142">&lt;protocol&gt;://&lt;server&gt;:&lt;port&gt;/&lt;path&gt;/&lt;?query&gt;&lt;#fragment&gt;</span></span></p>
<p><span data-ttu-id="92efc-143">Un chemin d’accès UNC comporte trois parties:</span><span class="sxs-lookup"><span data-stu-id="92efc-143">A UNC path has three parts:</span></span></p>
<p><span data-ttu-id="92efc-144">&amp;lt; NomOrdinateur &gt; &amp; lt; partager le dossier &gt; &amp; lt; ressource&gt;</span><span class="sxs-lookup"><span data-stu-id="92efc-144">&amp;lt;computername&gt;&amp;lt;share folder&gt;&amp;lt;resource&gt;</span></span></p>
<div class="alert">
<strong><span data-ttu-id="92efc-145">Important</span><span class="sxs-lookup"><span data-stu-id="92efc-145">Important</span></span></strong><br/><p><span data-ttu-id="92efc-146">Veillez à utiliser le format approprié lors de l’utilisation d’un chemin UNC.</span><span class="sxs-lookup"><span data-stu-id="92efc-146">Be sure to use the correct format when using a UNC path.</span></span> <span data-ttu-id="92efc-147">Les formats admissibles sont &amp; lt; Server &gt; &amp; lt; share &gt; or &lt; Drive Letter &gt; : &amp; lt; Folder &gt; .</span><span class="sxs-lookup"><span data-stu-id="92efc-147">Acceptable formats are &amp;lt;server&gt;&amp;lt;share&gt; or &lt;drive letter&gt;:&amp;lt;folder&gt;.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><em><span data-ttu-id="92efc-148">OSDSOURCEROOT</span><span class="sxs-lookup"><span data-stu-id="92efc-148">OSDSOURCEROOT</span></span></em></p></td>
<td align="left"><p><em><span data-ttu-id="92efc-149">UNC</span><span class="sxs-lookup"><span data-stu-id="92efc-149">UNC</span></span></em></p>
<p><span data-ttu-id="92efc-150">URL <em> http:// </em> ou https:// <em> URL</span><span class="sxs-lookup"><span data-stu-id="92efc-150">HTTP://<em>URL</em> or HTTPS://<em>URL</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="92efc-151">Permet à un administrateur de spécifier l’emplacement source de récupération de fichier OSD pour un package d’application au cours de la publication.</span><span class="sxs-lookup"><span data-stu-id="92efc-151">Enables an administrator to specify a source location for OSD file retrieval for an application package during publication.</span></span> <span data-ttu-id="92efc-152">Les racines de source de l’OSD prennent en charge les chemins d’accès et les URL.</span><span class="sxs-lookup"><span data-stu-id="92efc-152">OSD source roots support UNC paths and URLs (HTTP or HTTPS).</span></span> <span data-ttu-id="92efc-153">Si la valeur est «», qui est la valeur par défaut, les paramètres de fichier OSD existants sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="92efc-153">If the value is “”, which is the default value, the existing OSD file settings are used.</span></span></p>
<p><span data-ttu-id="92efc-154">Une URL est composée de plusieurs parties:</span><span class="sxs-lookup"><span data-stu-id="92efc-154">A URL has several parts:</span></span></p>
<p><span data-ttu-id="92efc-155">&lt;protocole &gt; :// &lt; serveur &gt; : &lt; chemin de port &gt; / &lt; &gt; / &lt; ? requête &gt; &lt; #fragment&gt;</span><span class="sxs-lookup"><span data-stu-id="92efc-155">&lt;protocol&gt;://&lt;server&gt;:&lt;port&gt;/&lt;path&gt;/&lt;?query&gt;&lt;#fragment&gt;</span></span></p>
<p><span data-ttu-id="92efc-156">Un chemin d’accès UNC comporte trois parties:</span><span class="sxs-lookup"><span data-stu-id="92efc-156">A UNC path has three parts:</span></span></p>
<p><span data-ttu-id="92efc-157">&amp;lt; NomOrdinateur &gt; &amp; lt; partager le dossier &gt; &amp; lt; ressource&gt;</span><span class="sxs-lookup"><span data-stu-id="92efc-157">&amp;lt;computername&gt;&amp;lt;share folder&gt;&amp;lt;resource&gt;</span></span></p>
<div class="alert">
<strong><span data-ttu-id="92efc-158">Important</span><span class="sxs-lookup"><span data-stu-id="92efc-158">Important</span></span></strong><br/><p><span data-ttu-id="92efc-159">Veillez à utiliser le format approprié lors de l’utilisation d’un chemin UNC.</span><span class="sxs-lookup"><span data-stu-id="92efc-159">Be sure to use the correct format when using a UNC path.</span></span> <span data-ttu-id="92efc-160">Les formats admissibles sont &amp; lt; Server &gt; &amp; lt; share &gt; or &lt; Drive Letter &gt; : &amp; lt; Folder &gt; .</span><span class="sxs-lookup"><span data-stu-id="92efc-160">Acceptable formats are &amp;lt;server&gt;&amp;lt;share&gt; or &lt;drive letter&gt;:&amp;lt;folder&gt;.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><em><span data-ttu-id="92efc-161">AUTOLOADONLOGIN</span><span class="sxs-lookup"><span data-stu-id="92efc-161">AUTOLOADONLOGIN</span></span></em></p>
<p><em><span data-ttu-id="92efc-162">AUTOLOADONLAUNCH</span><span class="sxs-lookup"><span data-stu-id="92efc-162">AUTOLOADONLAUNCH</span></span></em></p>
<p><em><span data-ttu-id="92efc-163">AUTOLOADONREFRESH</span><span class="sxs-lookup"><span data-stu-id="92efc-163">AUTOLOADONREFRESH</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="92efc-164">[0 | 1]</span><span class="sxs-lookup"><span data-stu-id="92efc-164">[0|1]</span></span></p></td>
<td align="left"><p><span data-ttu-id="92efc-165">Déclencheurs de chargement automatique qui définissent les événements de démarrage automatique des applications.</span><span class="sxs-lookup"><span data-stu-id="92efc-165">The AutoLoad triggers that define the events that initiate auto-loading of applications.</span></span> <span data-ttu-id="92efc-166">Autoload utilise implicitement le streaming en arrière-plan pour permettre au chargement de l’application dans le cache.</span><span class="sxs-lookup"><span data-stu-id="92efc-166">AutoLoad implicitly uses background streaming to enable the application to be fully loaded into cache.</span></span></p>
<p><span data-ttu-id="92efc-167">Le bloc de fonctionnalité principal sera chargé le plus rapidement possible.</span><span class="sxs-lookup"><span data-stu-id="92efc-167">The primary feature block will be loaded as quickly as possible.</span></span> <span data-ttu-id="92efc-168">Les blocs de fonctionnalités restants sont chargés en arrière-plan pour permettre les opérations au premier plan, telles que l’interaction utilisateur avec les applications, de manière à obtenir une priorité et des performances optimales.</span><span class="sxs-lookup"><span data-stu-id="92efc-168">Remaining feature blocks will be loaded in the background to enable foreground operations, such as user interaction with applications, to take priority and provide optimal performance.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="92efc-169">Remarque</span><span class="sxs-lookup"><span data-stu-id="92efc-169">Note</span></span></strong><br/><p><span data-ttu-id="92efc-170">Le <em> </em> paramètre AUTOLOADTARGET détermine les applications qui sont chargées automatiquement.</span><span class="sxs-lookup"><span data-stu-id="92efc-170">The <em>AUTOLOADTARGET</em> parameter determines which applications are auto-loaded.</span></span> <span data-ttu-id="92efc-171">Par défaut, les packages qui ont été utilisés sont chargés automatiquement, sauf si <em> AUTOLOADTARGET </em> est défini.</span><span class="sxs-lookup"><span data-stu-id="92efc-171">By default, packages that have been used are auto-loaded unless <em>AUTOLOADTARGET</em> is set.</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="92efc-172">Chaque paramètre affecte le comportement de chargement comme suit:</span><span class="sxs-lookup"><span data-stu-id="92efc-172">Each parameter affects loading behavior as follows:</span></span></p>
<ul>
<li><p><em><span data-ttu-id="92efc-173">AUTOLOADONLOGIN </em> — le chargement s’exécute lorsque l’utilisateur se connecte.</span><span class="sxs-lookup"><span data-stu-id="92efc-173">AUTOLOADONLOGIN</em>—Loading starts when the user logs in.</span></span></p></li>
<li><p><em><span data-ttu-id="92efc-174">AUTOLOADONLAUNCH </em> — le chargement démarre lorsque l’utilisateur démarre une application.</span><span class="sxs-lookup"><span data-stu-id="92efc-174">AUTOLOADONLAUNCH</em>—Loading starts when the user starts an application.</span></span></p></li>
<li><p><em><span data-ttu-id="92efc-175">AUTOLOADONREFRESH </em> : le chargement s’exécute à l’actualisation de la publication.</span><span class="sxs-lookup"><span data-stu-id="92efc-175">AUTOLOADONREFRESH</em>—Loading starts when a publishing refresh occurs.</span></span></p></li>
</ul>
<p><span data-ttu-id="92efc-176">Les trois valeurs peuvent être combinées.</span><span class="sxs-lookup"><span data-stu-id="92efc-176">The three values can be combined.</span></span> <span data-ttu-id="92efc-177">Dans l’exemple suivant, les déclencheurs de chargement à deux utilisateurs sont activés lors de la connexion de l’utilisateur et lors de l’actualisation de la publication.</span><span class="sxs-lookup"><span data-stu-id="92efc-177">In the following example, AutoLoad triggers are enabled both at user login and when publishing refresh occurs:</span></span></p>
<p><em><span data-ttu-id="92efc-178">AUTOLOADONLOGIN AUTOLOADONREFRESH</span><span class="sxs-lookup"><span data-stu-id="92efc-178">AUTOLOADONLOGIN AUTOLOADONREFRESH</span></span></em></p>
<div class="alert">
<strong><span data-ttu-id="92efc-179">Remarque</span><span class="sxs-lookup"><span data-stu-id="92efc-179">Note</span></span></strong><br/><p><span data-ttu-id="92efc-180">Si le client est configuré à l’aide de ces valeurs lors de la première installation, ce dernier ne sera pas déclenché tant que la prochaine fois que l’utilisateur se déconnecte et se reconnecte.</span><span class="sxs-lookup"><span data-stu-id="92efc-180">If the client is configured with these values at first install, Autoload will not be triggered until the next time the user logs off and logs back on.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><em><span data-ttu-id="92efc-181">AUTOLOADTARGET</span><span class="sxs-lookup"><span data-stu-id="92efc-181">AUTOLOADTARGET</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="92efc-182">NÉANT</span><span class="sxs-lookup"><span data-stu-id="92efc-182">NONE</span></span></p>
<p><span data-ttu-id="92efc-183">SES</span><span class="sxs-lookup"><span data-stu-id="92efc-183">ALL</span></span></p>
<p><span data-ttu-id="92efc-184">PREVUSED</span><span class="sxs-lookup"><span data-stu-id="92efc-184">PREVUSED</span></span></p></td>
<td align="left"><p><span data-ttu-id="92efc-185">Indique ce qui sera chargé automatiquement lorsque des déclencheurs de chargement sont présents.</span><span class="sxs-lookup"><span data-stu-id="92efc-185">Indicates what will be auto-loaded when any given AutoLoad triggers occur.</span></span></p>
<p><span data-ttu-id="92efc-186">Valeurs possibles:</span><span class="sxs-lookup"><span data-stu-id="92efc-186">Possible values:</span></span></p>
<ul>
<li><p><span data-ttu-id="92efc-187">AUCUN: il n’y a pas de chargement automatique, quels que soient les déclencheurs définis.</span><span class="sxs-lookup"><span data-stu-id="92efc-187">NONE—No auto-loading, regardless of what triggers might be set.</span></span></p></li>
<li><p><span data-ttu-id="92efc-188">ALL: si aucun déclencheur de charge automatique n’est activé, tous les packages sont chargés automatiquement, qu’ils aient été ou non démarrés.</span><span class="sxs-lookup"><span data-stu-id="92efc-188">ALL—If any AutoLoad trigger is enabled, all packages are automatically loaded, whether or not they have ever been launched.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="92efc-189">Remarque</span><span class="sxs-lookup"><span data-stu-id="92efc-189">Note</span></span></strong><br/><p><span data-ttu-id="92efc-190">Ce paramètre est configuré pour des packages individuels à l’aide du SFTMIME <strong> Ajouter un package </strong> et <strong> configurer des commandes de package </strong> .</span><span class="sxs-lookup"><span data-stu-id="92efc-190">This setting is configured for individual packages by using the SFTMIME <strong>ADD PACKAGE</strong> and <strong>CONFIGURE PACKAGE</strong> commands.</span></span> <span data-ttu-id="92efc-191">Pour plus d’informations sur ces commandes, voir informations de référence sur les <a href="sftmime--command-reference.md" data-raw-source="[SFTMIME Command Reference](sftmime--command-reference.md)"> commandes SFTMIME </a> .</span><span class="sxs-lookup"><span data-stu-id="92efc-191">For more information about these commands, see <a href="sftmime--command-reference.md" data-raw-source="[SFTMIME Command Reference](sftmime--command-reference.md)">SFTMIME Command Reference</a>.</span></span></p>
</div>
<div>

</div></li>
<li><p><span data-ttu-id="92efc-192">PREVUSED: si des déclencheurs de chargement automatique sont activés, chargez uniquement les packages dans lesquels au moins une application dans le package a été précédemment utilisée (c’est-à-dire lancée ou prémise en cache).</span><span class="sxs-lookup"><span data-stu-id="92efc-192">PREVUSED—If any AutoLoad trigger is enabled, load only the packages where at least one application in the package has been previously used (that is, launched or precached).</span></span></p></li>
</ul>
<div class="alert">
<strong><span data-ttu-id="92efc-193">Remarque</span><span class="sxs-lookup"><span data-stu-id="92efc-193">Note</span></span></strong><br/><p><span data-ttu-id="92efc-194">Lorsque vous installez le client App-V pour utiliser un cache en lecture seule (par exemple, dans le cadre d’une implémentation de serveur VDI), vous devez définir le <em> </em> paramètre AUTOLOADTARGET sur None pour empêcher le client d’essayer de mettre à jour des applications dans le cache en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="92efc-194">When you install the App-V client to use a read-only cache, (for example, as a VDI server implementation), you must set the <em>AUTOLOADTARGET</em> parameter to NONE to prevent the client from trying to update applications in the read-only cache.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><em><span data-ttu-id="92efc-195">DOTIMEOUTMINUTES</span><span class="sxs-lookup"><span data-stu-id="92efc-195">DOTIMEOUTMINUTES</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="92efc-196">29600 (par défaut)</span><span class="sxs-lookup"><span data-stu-id="92efc-196">29600 (default)</span></span></p>
<p><span data-ttu-id="92efc-197">1 – 1439998560 minutes (plage)</span><span class="sxs-lookup"><span data-stu-id="92efc-197">1–1439998560 minutes (range)</span></span></p></td>
<td align="left"><p><span data-ttu-id="92efc-198">Indique le nombre de minutes d’utilisation d’une application en mode hors connexion.</span><span class="sxs-lookup"><span data-stu-id="92efc-198">Indicates how many minutes an application may be used in disconnected operation.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><em><span data-ttu-id="92efc-199">INSTALLDIR</span><span class="sxs-lookup"><span data-stu-id="92efc-199">INSTALLDIR</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="92efc-200">&lt;accès&gt;</span><span class="sxs-lookup"><span data-stu-id="92efc-200">&lt;pathname&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="92efc-201">Spécifie le répertoire d’installation du client App-V.</span><span class="sxs-lookup"><span data-stu-id="92efc-201">Specifies the installation directory of the App-V Client.</span></span></p>
<p><span data-ttu-id="92efc-202">Exemple: INSTALLDIR = &quot; C:\Program Files\Microsoft Application Virtualization Client&quot;</span><span class="sxs-lookup"><span data-stu-id="92efc-202">Example: INSTALLDIR=&quot;C:\Program Files\Microsoft Application Virtualization Client&quot;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><em><span data-ttu-id="92efc-203">OPTIONNEL</span><span class="sxs-lookup"><span data-stu-id="92efc-203">OPTIN</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="92efc-204">PROPRIÉTÉ</span><span class="sxs-lookup"><span data-stu-id="92efc-204">“TRUE”</span></span></p>
<p><span data-ttu-id="92efc-205">“”</span><span class="sxs-lookup"><span data-stu-id="92efc-205">“”</span></span></p></td>
<td align="left"><p><span data-ttu-id="92efc-206">Les composants clients de Microsoft Application Virtualization seront mis à niveau par le biais de Microsoft Update lorsque des mises à jour sont disponibles pour le grand public.</span><span class="sxs-lookup"><span data-stu-id="92efc-206">Microsoft Application Virtualization Client components will be upgradable through Microsoft Update when updates are made available to the general public.</span></span> <span data-ttu-id="92efc-207">L’agent Microsoft Update sur lequel sont installés les systèmes d’exploitation Windows nécessite qu’un utilisateur puisse explicitement choisir d’utiliser le service.</span><span class="sxs-lookup"><span data-stu-id="92efc-207">The Microsoft Update Agent installed on Windows operating systems requires a user to explicitly opt-in to use the service.</span></span> <span data-ttu-id="92efc-208">Ce choix n’est requis qu’une seule fois pour toutes les applications sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="92efc-208">This opt-in is required only one time for all applications on the device.</span></span> <span data-ttu-id="92efc-209">Si vous avez déjà choisi Microsoft Update, les composants Microsoft Application Virtualization sur l’appareil tirent automatiquement parti du service.</span><span class="sxs-lookup"><span data-stu-id="92efc-209">If you have already opted into Microsoft Update, the Microsoft Application Virtualization components on the device will automatically take advantage of the service.</span></span></p>
<p><span data-ttu-id="92efc-210">Dans le cadre de l’installation de la ligne de commande, l’utilisation de Microsoft Update est refusée par défaut (à moins qu’une application précédente ait déjà activé l’appareil à utiliser) en raison de la configuration manuelle de Microsoft Update.</span><span class="sxs-lookup"><span data-stu-id="92efc-210">For command-line installation, use of Microsoft Update is by default opt-out (unless a previous application already enabled the device to be opted in) due to the requirement for manually opting into Microsoft Update.</span></span> <span data-ttu-id="92efc-211">Par conséquent, l’option doit être explicite pour les installations de lignes de commande.</span><span class="sxs-lookup"><span data-stu-id="92efc-211">Therefore, opting in must be explicit for command-line installations.</span></span> <span data-ttu-id="92efc-212">La définition du paramètre de ligne de commande <em> optin </em> sur true force la définition de l’option de mise à jour de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="92efc-212">Setting the command-line parameter <em>OPTIN</em> to TRUE forces the Microsoft Update opt-in to be set.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><em><span data-ttu-id="92efc-213">REQUIREAUTHORIZATIONIFCACHED</span><span class="sxs-lookup"><span data-stu-id="92efc-213">REQUIREAUTHORIZATIONIFCACHED</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="92efc-214">TRUE</span><span class="sxs-lookup"><span data-stu-id="92efc-214">TRUE</span></span></p>
<p><span data-ttu-id="92efc-215">FALSE</span><span class="sxs-lookup"><span data-stu-id="92efc-215">FALSE</span></span></p></td>
<td align="left"><p><span data-ttu-id="92efc-216">Indique si une autorisation est toujours requise, qu’une application soit déjà en cache ou non.</span><span class="sxs-lookup"><span data-stu-id="92efc-216">Indicates whether authorization is always required, whether or not an application is already in cache.</span></span></p>
<p><span data-ttu-id="92efc-217">Valeurs possibles:</span><span class="sxs-lookup"><span data-stu-id="92efc-217">Possible values:</span></span></p>
<ul>
<li><p><span data-ttu-id="92efc-218">TRUE: l’application doit toujours être autorisée au démarrage.</span><span class="sxs-lookup"><span data-stu-id="92efc-218">TRUE—Application always must be authorized at startup.</span></span> <span data-ttu-id="92efc-219">Pour les applications RTSP transmis, le jeton d’autorisation de l’utilisateur est envoyé au serveur pour autorisation.</span><span class="sxs-lookup"><span data-stu-id="92efc-219">For RTSP streamed applications, the user authorization token is sent to the server for authorization.</span></span> <span data-ttu-id="92efc-220">Dans le cas des applications basées sur le fichier, les listes de Contrã’le d’accès de fichier indiquent si un utilisateur est susceptible d’accéder à l’application.</span><span class="sxs-lookup"><span data-stu-id="92efc-220">For file-based applications, file ACLs dictate whether a user may access the application.</span></span></p></li>
<li><p><span data-ttu-id="92efc-221">FALSe: Essayez toujours de vous connecter au serveur.</span><span class="sxs-lookup"><span data-stu-id="92efc-221">FALSE—Always try to connect to the server.</span></span> <span data-ttu-id="92efc-222">Si une connexion au serveur ne peut pas être établie, le client permet toujours à l’utilisateur de lancer une application qui a déjà été chargée dans le cache.</span><span class="sxs-lookup"><span data-stu-id="92efc-222">If a connection to the server cannot be established, the client still allows the user to launch an application that has previously been loaded into cache.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><em><span data-ttu-id="92efc-223">SWICACHESIZE</span><span class="sxs-lookup"><span data-stu-id="92efc-223">SWICACHESIZE</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="92efc-224">Taille du cache en Mo</span><span class="sxs-lookup"><span data-stu-id="92efc-224">Cache size in MB</span></span></p></td>
<td align="left"><p><span data-ttu-id="92efc-225">Spécifie la taille en mégaoctets du cache client.</span><span class="sxs-lookup"><span data-stu-id="92efc-225">Specifies the size in megabytes of the client cache.</span></span> <span data-ttu-id="92efc-226">La taille par défaut est 4096 Mo et la taille maximale est 1 048 576 Mo (1 to).</span><span class="sxs-lookup"><span data-stu-id="92efc-226">The default size is 4096 MB, and the maximum size is 1,048,576 MB (1 TB).</span></span> <span data-ttu-id="92efc-227">Le système vérifie l’espace disponible au moment de l’installation, mais l’espace n’est pas réservé.</span><span class="sxs-lookup"><span data-stu-id="92efc-227">The system checks for the available space at installation time, but the space is not reserved.</span></span></p>
<p><span data-ttu-id="92efc-228">Par exemple: <strong> SWICACHESIZE = &quot; 1024&quot;</span><span class="sxs-lookup"><span data-stu-id="92efc-228">Example: <strong>SWICACHESIZE=&quot;1024&quot;</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><em><span data-ttu-id="92efc-229">SWIPUBSVRDISPLAY</span><span class="sxs-lookup"><span data-stu-id="92efc-229">SWIPUBSVRDISPLAY</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="92efc-230">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="92efc-230">Display name</span></span></p></td>
<td align="left"><p><span data-ttu-id="92efc-231">Spécifie le nom affiché du serveur de publication; obligatoire lorsque <em> SWIPUBSVRHOST </em> est utilisé.</span><span class="sxs-lookup"><span data-stu-id="92efc-231">Specifies the displayed name of the publishing server; required when <em>SWIPUBSVRHOST</em> is used.</span></span></p>
<p><span data-ttu-id="92efc-232">Par exemple: <strong> SWIPUBSVRDISPLAY = &quot; environnement de production&quot;</span><span class="sxs-lookup"><span data-stu-id="92efc-232">Example: <strong>SWIPUBSVRDISPLAY=&quot;PRODUCTION ENVIRONMENT&quot;</span></span></strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><em><span data-ttu-id="92efc-233">SWIPUBSVRTYPE</span><span class="sxs-lookup"><span data-stu-id="92efc-233">SWIPUBSVRTYPE</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="92efc-234">[HTTP | RTSP</span><span class="sxs-lookup"><span data-stu-id="92efc-234">[HTTP|RTSP]</span></span></p></td>
<td align="left"><p><span data-ttu-id="92efc-235">Spécifie le type du serveur de publication.</span><span class="sxs-lookup"><span data-stu-id="92efc-235">Specifies the publishing server type.</span></span> <span data-ttu-id="92efc-236">Le type du serveur par défaut est le serveur de virtualisation des applications.</span><span class="sxs-lookup"><span data-stu-id="92efc-236">The default server type is Application Virtualization Server.</span></span> <span data-ttu-id="92efc-237">Le <strong> </strong> commutateur/Secure n’est pas sensible à la casse.</span><span class="sxs-lookup"><span data-stu-id="92efc-237">The <strong>/secure</strong> switch is not case sensitive.</span></span></p>
<ul>
<li><p><span data-ttu-id="92efc-238">HTTP: serveur HTTP standard</span><span class="sxs-lookup"><span data-stu-id="92efc-238">HTTP—Standard HTTP Server</span></span></p></li>
<li><p><span data-ttu-id="92efc-239">HTTP <strong> /Secure </strong> : serveur http de sécurité améliorée</span><span class="sxs-lookup"><span data-stu-id="92efc-239">HTTP <strong>/secure</strong>—Enhanced Security HTTP Server</span></span></p></li>
<li><p><span data-ttu-id="92efc-240">RTSP: serveur de virtualisation des applications</span><span class="sxs-lookup"><span data-stu-id="92efc-240">RTSP—Application Virtualization Server</span></span></p></li>
<li><p><span data-ttu-id="92efc-241">RTSP <strong> /Secure </strong> : serveur de virtualisation des applications de sécurité améliorée</span><span class="sxs-lookup"><span data-stu-id="92efc-241">RTSP <strong>/secure</strong>—Enhanced Security Application Virtualization Server</span></span></p></li>
</ul>
<p><span data-ttu-id="92efc-242">Par exemple: <strong> SWIPUBSVRTYPE = &quot; http/Secure&quot;</span><span class="sxs-lookup"><span data-stu-id="92efc-242">Example: <strong>SWIPUBSVRTYPE=&quot;HTTP /secure&quot;</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><em><span data-ttu-id="92efc-243">SWIPUBSVRHOST</span><span class="sxs-lookup"><span data-stu-id="92efc-243">SWIPUBSVRHOST</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="92efc-244">Adresse IP | nom d’hôte</span><span class="sxs-lookup"><span data-stu-id="92efc-244">IP address|host name</span></span></p></td>
<td align="left"><p><span data-ttu-id="92efc-245">Spécifie l’adresse IP du serveur de virtualisation d’applications ou le nom d’hôte du serveur résolu dans l’adresse IP du serveur&#39;s; obligatoire lorsque <em> SWIPUBSVRDISPLAY </em> est utilisé.</span><span class="sxs-lookup"><span data-stu-id="92efc-245">Specifies either the IP address of the Application Virtualization Server or a host name of the server that resolves into the server&#39;s IP address; required when <em>SWIPUBSVRDISPLAY</em> is used.</span></span></p>
<p><span data-ttu-id="92efc-246">Par exemple: <strong> SWIPUBSVRHOST = &quot; SERVEUR01&quot;</span><span class="sxs-lookup"><span data-stu-id="92efc-246">Example: <strong>SWIPUBSVRHOST=&quot;SERVER01&quot;</span></span></strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><em><span data-ttu-id="92efc-247">SWIPUBSVRPORT</span><span class="sxs-lookup"><span data-stu-id="92efc-247">SWIPUBSVRPORT</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="92efc-248">Numéro de port</span><span class="sxs-lookup"><span data-stu-id="92efc-248">Port number</span></span></p></td>
<td align="left"><p><span data-ttu-id="92efc-249">Spécifie le port logique qui est utilisé par le serveur de virtualisation de l’application pour détecter les demandes du client (par défaut, 554).</span><span class="sxs-lookup"><span data-stu-id="92efc-249">Specifies the logical port that is used by this Application Virtualization Server to listen for requests from the client (default = 554).</span></span></p>
<ul>
<li><p><span data-ttu-id="92efc-250">Serveur HTTP standard: par défaut, 80.</span><span class="sxs-lookup"><span data-stu-id="92efc-250">Standard HTTP server—Default = 80.</span></span></p></li>
<li><p><span data-ttu-id="92efc-251">Serveur HTTP amélioré-sécurité par défaut: 443.</span><span class="sxs-lookup"><span data-stu-id="92efc-251">Enhanced Security HTTP Server—Default = 443.</span></span></p></li>
<li><p><span data-ttu-id="92efc-252">Serveur de virtualisation des applications: par défaut = 554.</span><span class="sxs-lookup"><span data-stu-id="92efc-252">Application Virtualization Server—Default = 554.</span></span></p></li>
<li><p><span data-ttu-id="92efc-253">Serveur de virtualisation des applications de sécurité améliorée: par défaut, 322.</span><span class="sxs-lookup"><span data-stu-id="92efc-253">Enhanced Security Application Virtualization Server—Default = 322.</span></span></p></li>
</ul>
<p><span data-ttu-id="92efc-254">Par exemple: <strong> SWIPUBSVRPORT = &quot; 443&quot;</span><span class="sxs-lookup"><span data-stu-id="92efc-254">Example: <strong>SWIPUBSVRPORT=&quot;443&quot;</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><em><span data-ttu-id="92efc-255">SWIPUBSVRPATH</span><span class="sxs-lookup"><span data-stu-id="92efc-255">SWIPUBSVRPATH</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="92efc-256">Nom du chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="92efc-256">Path name</span></span></p></td>
<td align="left"><p><span data-ttu-id="92efc-257">Spécifie l’emplacement sur le serveur de publication du fichier qui définit les associations de type de fichier (par défaut =/); obligatoire lorsque la <em> </em> valeur du paramètre SWIPUBSVRTYPE est http.</span><span class="sxs-lookup"><span data-stu-id="92efc-257">Specifies the location on the publishing server of the file that defines file type associations (default = /); required when the <em>SWIPUBSVRTYPE</em> parameter value is HTTP.</span></span></p>
<p><span data-ttu-id="92efc-258">Par exemple: <strong> SWIPUBSVRPATH = &quot; /AppVirt/appsntypes.xml&quot;</span><span class="sxs-lookup"><span data-stu-id="92efc-258">Example: <strong>SWIPUBSVRPATH=&quot;/AppVirt/appsntypes.xml&quot;</span></span></strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><em><span data-ttu-id="92efc-259">SWIPUBSVRREFRESH</span><span class="sxs-lookup"><span data-stu-id="92efc-259">SWIPUBSVRREFRESH</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="92efc-260">[Sur | DÉCONNECTÉ</span><span class="sxs-lookup"><span data-stu-id="92efc-260">[ON|OFF]</span></span></p></td>
<td align="left"><p><span data-ttu-id="92efc-261">Indique si le client interroge automatiquement le serveur de publication pour les associations de types de fichiers et les applications lorsque l’utilisateur se connecte au client (par défaut, le = activé).</span><span class="sxs-lookup"><span data-stu-id="92efc-261">Specifies whether the client automatically queries the publishing server for file type associations and applications when a user logs in to the client (default = ON).</span></span></p>
<p><span data-ttu-id="92efc-262">Par exemple: <strong> SWIPUBSVRREFRESH = &quot; off&quot;</span><span class="sxs-lookup"><span data-stu-id="92efc-262">Example: <strong>SWIPUBSVRREFRESH=&quot;off&quot;</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><em><span data-ttu-id="92efc-263">SWIGLOBALDATA</span><span class="sxs-lookup"><span data-stu-id="92efc-263">SWIGLOBALDATA</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="92efc-264">Global Data Directory</span><span class="sxs-lookup"><span data-stu-id="92efc-264">Global data directory</span></span></p></td>
<td align="left"><p><span data-ttu-id="92efc-265">Spécifie le répertoire dans lequel les données seront stockées qui ne sont pas spécifiques aux utilisateurs spécifiques (par défaut, C:\Documents and Settings\All Users\Documents).</span><span class="sxs-lookup"><span data-stu-id="92efc-265">Specifies the directory where data will be stored that is not specific to particular users (default = C:\Documents and Settings\All Users\Documents).</span></span></p>
<p><span data-ttu-id="92efc-266">Exemple: <strong> SWIGLOBALDATA = &quot; D:\Microsoft Application Virtualization Client\Global&quot;</span><span class="sxs-lookup"><span data-stu-id="92efc-266">Example: <strong>SWIGLOBALDATA=&quot;D:\Microsoft Application Virtualization Client\Global&quot;</span></span></strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><em><span data-ttu-id="92efc-267">SWIUSERDATA</span><span class="sxs-lookup"><span data-stu-id="92efc-267">SWIUSERDATA</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="92efc-268">Répertoire de données utilisateur</span><span class="sxs-lookup"><span data-stu-id="92efc-268">User data directory</span></span></p></td>
<td align="left"><p><span data-ttu-id="92efc-269">Spécifie le répertoire dans lequel les données seront stockées qui sont spécifiques aux utilisateurs spécifiques (par défaut =% APPDATA%).</span><span class="sxs-lookup"><span data-stu-id="92efc-269">Specifies the directory where data will be stored that is specific to particular users (default = %APPDATA%).</span></span></p>
<p><span data-ttu-id="92efc-270">Exemple: <strong> SWIUSERDATA = &quot; H:\Windows\Microsoft application de virtualisation des applications&quot;</span><span class="sxs-lookup"><span data-stu-id="92efc-270">Example: <strong>SWIUSERDATA=&quot;H:\Windows\Microsoft Application Virtualization Client&quot;</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><em><span data-ttu-id="92efc-271">SWIFSDRIVE</span><span class="sxs-lookup"><span data-stu-id="92efc-271">SWIFSDRIVE</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="92efc-272">Lettre de lecteur préférée</span><span class="sxs-lookup"><span data-stu-id="92efc-272">Preferred drive letter</span></span></p></td>
<td align="left"><p><span data-ttu-id="92efc-273">Correspond à la lettre du lecteur que vous avez sélectionnée pour le lecteur virtuel.</span><span class="sxs-lookup"><span data-stu-id="92efc-273">Corresponds to the drive letter that you selected for the virtual drive.</span></span></p>
<p><span data-ttu-id="92efc-274">Par exemple: <strong> SWIFSDRIVE = &quot; S&quot;</span><span class="sxs-lookup"><span data-stu-id="92efc-274">Example: <strong>SWIFSDRIVE=&quot;S&quot;</span></span></strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><em><span data-ttu-id="92efc-275">SYSTEMEVENTLOGLEVEL</span><span class="sxs-lookup"><span data-stu-id="92efc-275">SYSTEMEVENTLOGLEVEL</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="92efc-276">0 à 4</span><span class="sxs-lookup"><span data-stu-id="92efc-276">0–4</span></span></p></td>
<td align="left"><p><span data-ttu-id="92efc-277">Indique le niveau de journalisation dans lequel les messages du journal sont écrits dans le journal des événements Windows.</span><span class="sxs-lookup"><span data-stu-id="92efc-277">Indicates the logging level at which log messages are written to the NT event Log.</span></span> <span data-ttu-id="92efc-278">La valeur indique un seuil de ce qui est enregistré, c’est-à-dire que tout est égal ou inférieur à cette valeur est consigné.</span><span class="sxs-lookup"><span data-stu-id="92efc-278">The value indicates a threshold of what is logged—that is, everything equal to or less than that value is logged.</span></span> <span data-ttu-id="92efc-279">Par exemple, une valeur de 0x3 (avertissement) indique que les avertissements (0x3), les erreurs (0X2) et les erreurs critiques (0x1) sont enregistrées.</span><span class="sxs-lookup"><span data-stu-id="92efc-279">For example, a value of 0x3 (Warning) indicates that Warnings (0x3), Errors (0x2), and Critical Errors (0x1) are logged.</span></span></p>
<p><span data-ttu-id="92efc-280">Valeurs possibles:</span><span class="sxs-lookup"><span data-stu-id="92efc-280">Possible values:</span></span></p>
<ul>
<li><p><span data-ttu-id="92efc-281">0 = = aucun</span><span class="sxs-lookup"><span data-stu-id="92efc-281">0 == None</span></span></p></li>
<li><p><span data-ttu-id="92efc-282">1 = = critique</span><span class="sxs-lookup"><span data-stu-id="92efc-282">1 == Critical</span></span></p></li>
<li><p><span data-ttu-id="92efc-283">2 = = erreur</span><span class="sxs-lookup"><span data-stu-id="92efc-283">2 == Error</span></span></p></li>
<li><p><span data-ttu-id="92efc-284">3 = = AVERTISSEMENT</span><span class="sxs-lookup"><span data-stu-id="92efc-284">3 == Warning</span></span></p></li>
<li><p><span data-ttu-id="92efc-285">4 = = informations</span><span class="sxs-lookup"><span data-stu-id="92efc-285">4 == Information</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><em><span data-ttu-id="92efc-286">MINFREESPACEMB</span><span class="sxs-lookup"><span data-stu-id="92efc-286">MINFREESPACEMB</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="92efc-287">En Mo</span><span class="sxs-lookup"><span data-stu-id="92efc-287">In MB</span></span></p></td>
<td align="left"><p><span data-ttu-id="92efc-288">Spécifie la quantité d’espace libre (en mégaoctets) qui doit être disponible sur l’hôte avant que la taille de cache ne puisse augmenter.</span><span class="sxs-lookup"><span data-stu-id="92efc-288">Specifies the amount of free space (in megabytes) that must be available on the host before the cache size can increase.</span></span> <span data-ttu-id="92efc-289">L’exemple suivant configure le client pour vérifier qu’il s’agit d’au moins 5 Go d’espace libre sur le disque avant d’autoriser l’augmentation de la taille du cache.</span><span class="sxs-lookup"><span data-stu-id="92efc-289">The following example would configure the client to ensure at least 5 GB of free space on the disk before allowing the size of the cache to increase.</span></span> <span data-ttu-id="92efc-290">La valeur par défaut est 5000 Mo d’espace libre disponible sur le disque au moment de l’installation.</span><span class="sxs-lookup"><span data-stu-id="92efc-290">The default is 5000 MB of free space available on disk at installation time.</span></span></p>
<p><span data-ttu-id="92efc-291">Exemple: <strong> MINFREESPACEMB = &quot; 5000 &quot; (5 Go)</span><span class="sxs-lookup"><span data-stu-id="92efc-291">Example: <strong>MINFREESPACEMB =&quot;5000&quot; (5 GB)</span></span></strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><em><span data-ttu-id="92efc-292">KEEPCURRENTSETTINGS</span><span class="sxs-lookup"><span data-stu-id="92efc-292">KEEPCURRENTSETTINGS</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="92efc-293">[0 | 1]</span><span class="sxs-lookup"><span data-stu-id="92efc-293">[0|1]</span></span></p></td>
<td align="left"><p><span data-ttu-id="92efc-294">Utilisé lorsque vous avez appliqué des paramètres de Registre avant de déployer un client, par exemple, à l’aide d’une stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="92efc-294">Used when you have applied registry settings prior to deploying a client—for example, by using Group Policy.</span></span> <span data-ttu-id="92efc-295">Lors du déploiement d’un client, définissez ce paramètre sur une valeur de 1 pour ne pas remplacer les paramètres du Registre.</span><span class="sxs-lookup"><span data-stu-id="92efc-295">When a client is deployed, set this parameter to a value of 1 so that it will not overwrite the registry settings.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="92efc-296">Important</span><span class="sxs-lookup"><span data-stu-id="92efc-296">Important</span></span></strong><br/><p><span data-ttu-id="92efc-297">Si la valeur est égale à 1, les paramètres de ligne de commande du programme d’installation du client suivants sont ignorés:</span><span class="sxs-lookup"><span data-stu-id="92efc-297">If set to a value of 1, the following client installer command-line parameters are ignored:</span></span></p>
<p><strong><span data-ttu-id="92efc-298">SWICACHESIZE </strong> , <strong> MINFREESPACEMB </strong> , <strong> ALLOWINDEPENDENTFILESTREAMING </strong> , <strong> APPLICATIONSOURCEROOT </strong> , <strong> IconSourceRoot </strong> , <strong> OSDSourceRoot </strong> , <strong> SYSTEMEVENTLOGLEVEL </strong> , <strong> SWIGLOBALDATA </strong> , <strong> DOTIMEOUTMINUTES </strong> , <strong> SWIFSDRIVE </strong> , <strong> AUTOLOADTARGET </strong> , <strong> AUTOLOADTRIGGERS et </strong> <strong> SWIUSERDATA </strong> .</span><span class="sxs-lookup"><span data-stu-id="92efc-298">SWICACHESIZE</strong>, <strong>MINFREESPACEMB</strong>, <strong>ALLOWINDEPENDENTFILESTREAMING</strong>, <strong>APPLICATIONSOURCEROOT</strong>, <strong>ICONSOURCEROOT</strong>, <strong>OSDSOURCEROOT</strong>, <strong>SYSTEMEVENTLOGLEVEL</strong>, <strong>SWIGLOBALDATA</strong>, <strong>DOTIMEOUTMINUTES</strong>, <strong>SWIFSDRIVE</strong>, <strong>AUTOLOADTARGET</strong>, <strong>AUTOLOADTRIGGERS</strong>, and <strong>SWIUSERDATA</strong>.</span></span></p>
<p><span data-ttu-id="92efc-299">Pour plus d’informations sur la définition de ces valeurs après l’installation, voir la section «Comment configurer les paramètres du registre des clients App-V à l’aide de la ligne de commande» dans le guide des opérations d’application (App-V) <a href="https://go.microsoft.com/fwlink/?LinkId=122939" data-raw-source="[https://go.microsoft.com/fwlink/?LinkId=122939](https://go.microsoft.com/fwlink/?LinkId=122939)"> https://go.microsoft.com/fwlink/?LinkId=122939 </a> .</span><span class="sxs-lookup"><span data-stu-id="92efc-299">For further information about setting these values after installation, see “How to Configure the App-V Client Registry Settings by Using the Command Line” in the Application Virtualization (App-V) Operations Guide (<a href="https://go.microsoft.com/fwlink/?LinkId=122939" data-raw-source="[https://go.microsoft.com/fwlink/?LinkId=122939](https://go.microsoft.com/fwlink/?LinkId=122939)">https://go.microsoft.com/fwlink/?LinkId=122939</a>).</span></span></p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="92efc-300">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="92efc-300">Related topics</span></span>


[<span data-ttu-id="92efc-301">Procédure pour installer manuellement Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="92efc-301">How to Manually Install the Application Virtualization Client</span></span>](how-to-manually-install-the-application-virtualization-client.md)

[<span data-ttu-id="92efc-302">Procédure pour mettre à niveau Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="92efc-302">How to Upgrade the Application Virtualization Client</span></span>](how-to-upgrade-the-application-virtualization-client.md)

[<span data-ttu-id="92efc-303">Référence de commande SFTMIME</span><span class="sxs-lookup"><span data-stu-id="92efc-303">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)









