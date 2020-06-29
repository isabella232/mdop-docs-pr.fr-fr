---
title: Planification de la sécurisation des sites web MBAM
description: Planification de la sécurisation des sites web MBAM
author: dansimp
ms.assetid: aea1d137-62cf-4da4-9989-541e0b5ad8d8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 223c9397ad7933e11051c289c3dbcab63940fbc5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810907"
---
# <span data-ttu-id="e831a-103">Planification de la sécurisation des sites web MBAM</span><span class="sxs-lookup"><span data-stu-id="e831a-103">Planning How to Secure the MBAM Websites</span></span>


<span data-ttu-id="e831a-104">Cette rubrique décrit les méthodes suivantes pour sécuriser le site Web d’administration et de surveillance de Microsoft BitLocker (MBAM 2,5), ainsi que le portail libre-service.</span><span class="sxs-lookup"><span data-stu-id="e831a-104">This topic describes the following methods for securing the Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 Administration and Monitoring Website and Self-Service Portal:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e831a-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="e831a-105">Method</span></span></th>
<th align="left"><span data-ttu-id="e831a-106">Obligatoire ou facultatif?</span><span class="sxs-lookup"><span data-stu-id="e831a-106">Required or optional?</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e831a-107">Utiliser des certificats pour sécuriser les sites Web MBAM</span><span class="sxs-lookup"><span data-stu-id="e831a-107">Using certificates to secure MBAM websites</span></span></p></td>
<td align="left"><p><span data-ttu-id="e831a-108">Facultatif, mais fortement recommandé</span><span class="sxs-lookup"><span data-stu-id="e831a-108">Optional, but highly recommended</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e831a-109">Inscription des noms de principal de service (SPN) pour le compte du pool d’applications</span><span class="sxs-lookup"><span data-stu-id="e831a-109">Registering Service Principal Names (SPN) for the application pool account</span></span></p></td>
<td align="left"><p><span data-ttu-id="e831a-110">Requis</span><span class="sxs-lookup"><span data-stu-id="e831a-110">Required</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="e831a-111">Pour plus d’informations sur la façon de sécuriser votre déploiement MBAM, voir [considérations relatives à la sécurité dans MBAM 2,5](mbam-25-security-considerations.md).</span><span class="sxs-lookup"><span data-stu-id="e831a-111">For more information about how to secure your MBAM deployment, see [MBAM 2.5 Security Considerations](mbam-25-security-considerations.md).</span></span>

## <span data-ttu-id="e831a-112">Utiliser des certificats pour sécuriser les sites Web MBAM</span><span class="sxs-lookup"><span data-stu-id="e831a-112">Using certificates to secure MBAM websites</span></span>


<span data-ttu-id="e831a-113">Nous vous recommandons d’utiliser un certificat pour sécuriser la communication entre:</span><span class="sxs-lookup"><span data-stu-id="e831a-113">We recommend that you use a certificate to secure the communication between the:</span></span>

-   <span data-ttu-id="e831a-114">Client MBAM et services Web</span><span class="sxs-lookup"><span data-stu-id="e831a-114">MBAM Client and the web services</span></span>

-   <span data-ttu-id="e831a-115">Navigateur et site Web d’administration et de surveillance et sites Web de portail libre-service</span><span class="sxs-lookup"><span data-stu-id="e831a-115">Browser and the Administration and Monitoring Website and the Self-Service Portal websites</span></span>

<span data-ttu-id="e831a-116">Pour plus d’informations sur la demande et l’installation d’un certificat, voir [configurer des certificats de serveur Internet](https://technet.microsoft.com/library/cc731977.aspx).</span><span class="sxs-lookup"><span data-stu-id="e831a-116">For information about requesting and installing a certificate, see [Configuring Internet Server Certificates](https://technet.microsoft.com/library/cc731977.aspx).</span></span>

**<span data-ttu-id="e831a-117">Remarque</span><span class="sxs-lookup"><span data-stu-id="e831a-117">Note</span></span>**  
<span data-ttu-id="e831a-118">Vous pouvez configurer les sites Web et services Web sur des serveurs différents uniquement si vous utilisez Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e831a-118">You can configure the websites and web services on different servers only if you are using Windows PowerShell.</span></span> <span data-ttu-id="e831a-119">Si vous utilisez l’Assistant Configuration de MBAM Server pour configurer les sites Web, vous devez configurer les sites Web et les services Web sur le même serveur.</span><span class="sxs-lookup"><span data-stu-id="e831a-119">If you use the MBAM Server Configuration wizard to configure the websites, you must configure the websites and the web services on the same server.</span></span>



<span data-ttu-id="e831a-120">Pour sécuriser la communication entre les services Web et les bases de données, nous vous conseillons également de forcer le chiffrement dans SQL Server.</span><span class="sxs-lookup"><span data-stu-id="e831a-120">To secure the communication between the web services and the databases, we also recommend that you force encryption in SQL Server.</span></span> <span data-ttu-id="e831a-121">Pour plus d’informations sur la sécurisation de toutes les connexions à SQL Server, y compris la communication entre les services Web et SQL Server, voir [considérations relatives à la sécurité de MBAM 2,5](mbam-25-security-considerations.md#bkmk-secure-databases).</span><span class="sxs-lookup"><span data-stu-id="e831a-121">For information about securing all connections to SQL Server, including communication between the web services and SQL Server, see [MBAM 2.5 Security Considerations](mbam-25-security-considerations.md#bkmk-secure-databases).</span></span>

## <span data-ttu-id="e831a-122">Inscription de SPN pour le compte du pool d’applications</span><span class="sxs-lookup"><span data-stu-id="e831a-122">Registering SPNs for the application pool account</span></span>


<span data-ttu-id="e831a-123">Pour permettre aux serveurs MBAM d’authentifier les communications à partir du site Web d’administration et de surveillance et du portail libre-service, vous devez inscrire un nom de principal de service (SPN) pour le nom d’hôte sous le compte de domaine que vous utilisez pour le pool d’applications Web.</span><span class="sxs-lookup"><span data-stu-id="e831a-123">To enable the MBAM Servers to authenticate communication from the Administration and Monitoring Website and the Self-Service Portal, you must register a Service Principal Name (SPN) for the host name under the domain account that you are using for the web application pool.</span></span>

<span data-ttu-id="e831a-124">Cette rubrique contient des instructions sur la façon d’enregistrer des noms de fichier SPN pour les types de noms d’hôtes suivants:</span><span class="sxs-lookup"><span data-stu-id="e831a-124">This topic contains instructions on how to register SPNs for the following types of host names:</span></span>

-   <span data-ttu-id="e831a-125">Nom de domaine complet</span><span class="sxs-lookup"><span data-stu-id="e831a-125">Fully qualified domain name</span></span>

-   <span data-ttu-id="e831a-126">Nom NetBIOS</span><span class="sxs-lookup"><span data-stu-id="e831a-126">NetBIOS name</span></span>

-   <span data-ttu-id="e831a-127">Nom virtuel</span><span class="sxs-lookup"><span data-stu-id="e831a-127">Virtual name</span></span>

### <span data-ttu-id="e831a-128">Avant de créer des SPN pour une installation MBAM initiale</span><span class="sxs-lookup"><span data-stu-id="e831a-128">Before you create SPNs for an initial MBAM installation</span></span>

<span data-ttu-id="e831a-129">Passez en revue les informations figurant dans le tableau suivant avant de commencer à créer des SPN.</span><span class="sxs-lookup"><span data-stu-id="e831a-129">Review the information in the following table before you start creating SPNs.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e831a-130">Tâche ou élément</span><span class="sxs-lookup"><span data-stu-id="e831a-130">Task or item</span></span></th>
<th align="left"><span data-ttu-id="e831a-131">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="e831a-131">More information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e831a-132">Créer un compte de service dans les services de domaine Active Directory (AD DS).</span><span class="sxs-lookup"><span data-stu-id="e831a-132">Create a service account in Active Directory Domain Services (AD DS).</span></span></p></td>
<td align="left"><p><span data-ttu-id="e831a-133">Le compte de service est un compte d’utilisateur que vous créez dans AD DS pour garantir la sécurité des sites Web MBAM.</span><span class="sxs-lookup"><span data-stu-id="e831a-133">The service account is a user account that you create in AD DS to provide security for the MBAM websites.</span></span> <span data-ttu-id="e831a-134">Les sites Web MBAM s’exécutent sous un pool d’applications, dont l’identité correspond au nom du compte de service.</span><span class="sxs-lookup"><span data-stu-id="e831a-134">The MBAM websites run under an application pool, whose identity is the name of the service account.</span></span> <span data-ttu-id="e831a-135">Le SPN est alors enregistré dans le compte du pool d’applications.</span><span class="sxs-lookup"><span data-stu-id="e831a-135">The SPNs are then registered in the application pool account.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="e831a-136">Remarque</span><span class="sxs-lookup"><span data-stu-id="e831a-136">Note</span></span></strong><br/><p><span data-ttu-id="e831a-137">Vous devez utiliser le même compte de pool d’applications pour tous les serveurs Web.</span><span class="sxs-lookup"><span data-stu-id="e831a-137">You must use the same application pool account for all web servers.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e831a-138">Vérifiez que le compte de groupe IIS-IUSRS ou le compte du pool d’applications a reçu les droits nécessaires.</span><span class="sxs-lookup"><span data-stu-id="e831a-138">Verify that either the IIS-IUSRS group account or the application pool account has been granted the necessary rights.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e831a-139">Pour cela, procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="e831a-139">To check this, follow these steps:</span></span></p>
<ol>
<li><p><span data-ttu-id="e831a-140">Ouvrez l' <strong> éditeur de stratégie de sécurité local </strong> et développez le <strong> nœud Stratégies locales </strong> .</span><span class="sxs-lookup"><span data-stu-id="e831a-140">Open the <strong>Local Security Policy editor</strong> and expand the <strong>Local Policies</strong> node.</span></span></p></li>
<li><p><span data-ttu-id="e831a-141">Sélectionnez le <strong> nœud d’attribution de droits </strong> d’utilisateur, puis double-cliquez sur l’option <strong> emprunter l’identité d’un client après authentification </strong> et ouvrez une <strong> session en tant que </strong> paramètres de stratégie de groupe dans le volet droit.</span><span class="sxs-lookup"><span data-stu-id="e831a-141">Select the <strong>User Rights Assignment</strong> node, and double-click the <strong>Impersonate a client after authentication</strong> and <strong>Log on as a batch job</strong> Group Policy settings in the right pane.</span></span></p></li>
</ol></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e831a-142">Si vous configurez les sites Web MBAM à l’aide d’un compte d’administrateur de domaine, MBAM créera les noms de domaine pour vous.</span><span class="sxs-lookup"><span data-stu-id="e831a-142">If you configure the MBAM websites by using a domain administrative account, MBAM will create the SPNs for you.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e831a-143">Si vous configurez les sites Web MBAM à l’aide d’un compte d’administrateur de domaine, suivez les étapes décrites dans cette rubrique pour inscrire les noms d’hôtes manuellement pour le type de nom d’hôte que vous utilisez.</span><span class="sxs-lookup"><span data-stu-id="e831a-143">If you configure the MBAM websites by using a domain administrative account, follow the steps in this topic to register SPNs manually for the type of host name that you are using.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="e831a-144">Inscription des SPN lorsque vous utilisez un nom d’hôte de domaine complet</span><span class="sxs-lookup"><span data-stu-id="e831a-144">Registering SPNs when you use a fully qualified domain host name</span></span>

<span data-ttu-id="e831a-145">Si vous utilisez un nom d’hôte de domaine complet lorsque vous configurez MBAM, vous devez enregistrer un seul SPN, comme indiqué dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="e831a-145">If you use a fully qualified domain host name when you configure MBAM, you have to register only one SPN, as shown in the following example.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e831a-146">Ce que vous devez faire</span><span class="sxs-lookup"><span data-stu-id="e831a-146">What you need to do</span></span></th>
<th align="left"><span data-ttu-id="e831a-147">Exemples et informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="e831a-147">Examples and more information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e831a-148">Enregistrez un SPN pour le nom de domaine complet.</span><span class="sxs-lookup"><span data-stu-id="e831a-148">Register an SPN for the fully qualified domain name.</span></span></p></td>
<td align="left"><p><code>Setspn -s http/mybitlockerrecovery.contoso.com contoso\mbamapppooluser</code></p>
<p><span data-ttu-id="e831a-149">Le nom d’hôte complet est <strong> mybitlockerrecovery.contoso.com </strong> et le compte de domaine utilisé pour le pool d’applications Web est <strong> contoso\mbamapppooluser </strong> .</span><span class="sxs-lookup"><span data-stu-id="e831a-149">The fully qualified host name is <strong>mybitlockerrecovery.contoso.com</strong>, and the domain account used for the web application pool is <strong>contoso\mbamapppooluser</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e831a-150">Configurez la délégation contrainte pour le SPN que vous inscrivez pour le compte du pool d’applications.</span><span class="sxs-lookup"><span data-stu-id="e831a-150">Configure constrained delegation for the SPN that you are registering for the application pool account.</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=394335" data-raw-source="[Configuring Constrained Delegation](https://go.microsoft.com/fwlink/?LinkId=394335)"><span data-ttu-id="e831a-151">Configuration de la délégation contrainte</span><span class="sxs-lookup"><span data-stu-id="e831a-151">Configuring Constrained Delegation</span></span></a></p>
<p><span data-ttu-id="e831a-152">Cette obligation ne s’applique qu’à MBAM 2,5; Il n’est pas nécessaire dans MBAM 2,5 SP1.</span><span class="sxs-lookup"><span data-stu-id="e831a-152">This requirement only applies to MBAM 2.5; it is not necessary in MBAM 2.5 SP1.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="e831a-153">Inscription des SPN lorsque vous utilisez un nom d’hôte NetBIOS</span><span class="sxs-lookup"><span data-stu-id="e831a-153">Registering SPNs when you use a NetBIOS host name</span></span>

<span data-ttu-id="e831a-154">Si vous utilisez un nom d’hôte NetBIOS lorsque vous configurez MBAM, inscrivez un SPN pour le nom NetBIOS et un autre SPN pour le nom de domaine complet, comme indiqué dans les exemples suivants.</span><span class="sxs-lookup"><span data-stu-id="e831a-154">If you use a NetBIOS host name when you configure MBAM, register one SPN for the NetBIOS name, and another SPN for the fully qualified domain name, as shown in the following examples.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e831a-155">Ce que vous devez faire</span><span class="sxs-lookup"><span data-stu-id="e831a-155">What you need to do</span></span></th>
<th align="left"><span data-ttu-id="e831a-156">Exemples et informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="e831a-156">Examples and more information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e831a-157">Enregistrez un SPN pour le nom d’hôte NetBIOS.</span><span class="sxs-lookup"><span data-stu-id="e831a-157">Register an SPN for the NetBIOS host name.</span></span></p></td>
<td align="left"><p><code>Setspn -s http/nbname01 contoso\mbamapppooluser</code></p>
<p><span data-ttu-id="e831a-158">Le nom d’hôte NetBIOS est <strong> nbname01 </strong> et le compte de domaine utilisé pour le pool d’applications Web est <strong> contoso\mbamapppooluser </strong> .</span><span class="sxs-lookup"><span data-stu-id="e831a-158">The NetBIOS host name is <strong>nbname01</strong>, and the domain account used for the web application pool is <strong>contoso\mbamapppooluser</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e831a-159">Enregistrez un SPN pour le nom de domaine complet.</span><span class="sxs-lookup"><span data-stu-id="e831a-159">Register an SPN for the fully qualified domain name.</span></span></p></td>
<td align="left"><p><code>Setspn –s http/nbname01.corp.contoso.com contoso\mbamapppooluser</code></p>
<p><span data-ttu-id="e831a-160">Le nom de domaine complet est <strong> nbname01.contoso.com </strong> et le compte de domaine utilisé pour le pool d’applications Web est <strong> contoso\mbamapppooluser </strong> .</span><span class="sxs-lookup"><span data-stu-id="e831a-160">The fully qualified domain name is <strong>nbname01.contoso.com</strong>, and the domain account used for the web application pool is <strong>contoso\mbamapppooluser</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e831a-161">Configurez la délégation contrainte pour les noms d’application (SPN) que vous inscrivez pour le compte du pool d’applications.</span><span class="sxs-lookup"><span data-stu-id="e831a-161">Configure constrained delegation for the SPNs that you are registering for the application pool account.</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=394335" data-raw-source="[Configuring Constrained Delegation](https://go.microsoft.com/fwlink/?LinkId=394335)"><span data-ttu-id="e831a-162">Configuration de la délégation contrainte</span><span class="sxs-lookup"><span data-stu-id="e831a-162">Configuring Constrained Delegation</span></span></a></p>
<p><span data-ttu-id="e831a-163">Cette obligation ne s’applique qu’à MBAM 2,5; Il n’est pas nécessaire dans MBAM 2,5 SP1.</span><span class="sxs-lookup"><span data-stu-id="e831a-163">This requirement only applies to MBAM 2.5; it is not necessary in MBAM 2.5 SP1.</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-regvirtualspn"></a><span data-ttu-id="e831a-164">Inscription des SPN lorsque vous utilisez un nom d’hôte virtuel</span><span class="sxs-lookup"><span data-stu-id="e831a-164">Registering SPNs when you use a virtual host name</span></span>

<span data-ttu-id="e831a-165">Si vous configurez MBAM avec un nom d’hôte virtuel qui est un nom de domaine complet, n’enregistrez qu’un SPN pour le nom d’hôte virtuel.</span><span class="sxs-lookup"><span data-stu-id="e831a-165">If you configure MBAM with a virtual host name that is a fully qualified domain name, register only one SPN for the virtual host name.</span></span> <span data-ttu-id="e831a-166">Si le nom d’hôte virtuel que vous configurez n’est pas un nom de domaine complet, vous devez créer un deuxième SPN spécifiant le nom de domaine complet, comme décrit dans les exemples suivants.</span><span class="sxs-lookup"><span data-stu-id="e831a-166">If the virtual host name that you configure is not a fully qualified domain name, you must create a second SPN that specifies the fully qualified domain name, as described in the following examples.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e831a-167">Ce que vous devez faire</span><span class="sxs-lookup"><span data-stu-id="e831a-167">What you need to do</span></span></th>
<th align="left"><span data-ttu-id="e831a-168">Exemples et informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="e831a-168">Examples and more information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e831a-169">S’il s’agit d’un nom de domaine complet, tel que dans cet exemple, n’enregistrez qu’un SPN.</span><span class="sxs-lookup"><span data-stu-id="e831a-169">If your virtual host name is a fully qualified domain name, as in this example, register only one SPN.</span></span></p></td>
<td align="left"><p><code>Setspn -s http/mbamvirtual.contoso.com contoso\mbamapppooluser</code></p>
<p><span data-ttu-id="e831a-170">Dans l’exemple, le nom d’hôte virtuel est <strong> mbamvirtual.contoso.com </strong> et le compte de domaine utilisé pour le pool d’applications Web est <strong> contoso\mbamapppooluser </strong> .</span><span class="sxs-lookup"><span data-stu-id="e831a-170">In the example, the virtual host name is <strong>mbamvirtual.contoso.com</strong>, and the domain account used for the web application pool is <strong>contoso\mbamapppooluser</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e831a-171">Enregistrez ce SPN supplémentaire si votre nom d’hôte virtuel n’est pas un nom de domaine complet.</span><span class="sxs-lookup"><span data-stu-id="e831a-171">Register this additional SPN if your virtual host name is not a fully qualified domain name.</span></span></p></td>
<td align="left"><p><code>Setspn -s http/mbamvirtual contoso\mbamapppooluser</code></p>
<p><span data-ttu-id="e831a-172">Dans l’exemple, le nom d’hôte virtuel est <strong> mbamvirtual </strong> et le compte de domaine utilisé pour le pool d’applications Web est <strong> contoso\mbamapppooluser </strong> .</span><span class="sxs-lookup"><span data-stu-id="e831a-172">In the example, the virtual host name is <strong>mbamvirtual</strong>, and the domain account used for the web application pool is <strong>contoso\mbamapppooluser</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e831a-173">Enregistrez ce SPN supplémentaire si votre nom d’hôte virtuel n’est pas un nom de domaine complet.</span><span class="sxs-lookup"><span data-stu-id="e831a-173">Register this additional SPN if your virtual host name is not a fully qualified domain name.</span></span></p></td>
<td align="left"><p><code>Setspn -s http/mbamvirtual.contoso.com contoso\mbamapppooluser</code></p>
<p><span data-ttu-id="e831a-174">Dans l’exemple, le nom d’hôte virtuel est <strong> mbamvirtual.contoso.com </strong> et le compte de domaine utilisé pour le pool d’applications Web est <strong> contoso\mbamapppooluser </strong> .</span><span class="sxs-lookup"><span data-stu-id="e831a-174">In the example, the virtual host name is <strong>mbamvirtual.contoso.com</strong>, and the domain account used for the web application pool is <strong>contoso\mbamapppooluser</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e831a-175">Sur le serveur DNS (Domain Name Server), créez un «A record» pour le nom d’hôte personnalisé et placez-le sur un serveur Web ou un équilibrage de charge.</span><span class="sxs-lookup"><span data-stu-id="e831a-175">On the Domain Name Server (DNS) server, create an “A record” for the custom host name and point it to a web server or a load balancer.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e831a-176">Voir la section «Configuration de l’hôte DNS A Records» dans <a href="https://go.microsoft.com/fwlink/?LinkId=394337" data-raw-source="[Configure DNS Host Records](https://go.microsoft.com/fwlink/?LinkId=394337)"> configurer les enregistrements d’hôte DNS </a> .</span><span class="sxs-lookup"><span data-stu-id="e831a-176">See the “To configure DNS Host A Records” section in <a href="https://go.microsoft.com/fwlink/?LinkId=394337" data-raw-source="[Configure DNS Host Records](https://go.microsoft.com/fwlink/?LinkId=394337)">Configure DNS Host Records</a>.</span></span></p>
<p><span data-ttu-id="e831a-177">Nous vous recommandons d’utiliser un enregistrement au lieu de CNAMe.</span><span class="sxs-lookup"><span data-stu-id="e831a-177">We recommend that you use A records instead of CNAMES.</span></span> <span data-ttu-id="e831a-178">Si vous utilisez les noms d’application (CNAMe) pour qu’ils pointent vers l’adresse de domaine, vous devez également inscrire les SPN pour le nom du serveur Web dans le compte du pool d’applications.</span><span class="sxs-lookup"><span data-stu-id="e831a-178">If you use CNAMES to point to the domain address, you must also register SPNs for the web server name in the application pool account.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e831a-179">Configurez la délégation contrainte pour les noms d’application (SPN) que vous inscrivez pour le compte du pool d’applications.</span><span class="sxs-lookup"><span data-stu-id="e831a-179">Configure constrained delegation for the SPNs that you are registering for the application pool account.</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=394335" data-raw-source="[Configuring Constrained Delegation](https://go.microsoft.com/fwlink/?LinkId=394335)"><span data-ttu-id="e831a-180">Configuration de la délégation contrainte</span><span class="sxs-lookup"><span data-stu-id="e831a-180">Configuring Constrained Delegation</span></span></a></p>
<p><span data-ttu-id="e831a-181">Cette obligation ne s’applique qu’à MBAM 2,5; Il n’est pas nécessaire dans MBAM 2,5 SP1.</span><span class="sxs-lookup"><span data-stu-id="e831a-181">This requirement only applies to MBAM 2.5; it is not necessary in MBAM 2.5 SP1.</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-registerspn"></a><span data-ttu-id="e831a-182">Inscription d’un SPN lorsque vous effectuez une mise à niveau à partir d’une version précédente de MBAM</span><span class="sxs-lookup"><span data-stu-id="e831a-182">Registering an SPN when you upgrade from previous versions of MBAM</span></span>

<span data-ttu-id="e831a-183">Suivez les étapes décrites dans cette section uniquement si vous souhaitez:</span><span class="sxs-lookup"><span data-stu-id="e831a-183">Complete the steps in this section only if you want to:</span></span>

-   <span data-ttu-id="e831a-184">Effectuer une mise à niveau à partir d’une version précédente de MBAM.</span><span class="sxs-lookup"><span data-stu-id="e831a-184">Upgrade from a previous version of MBAM.</span></span>

-   <span data-ttu-id="e831a-185">Exécutez les sites Web dans MBAM 2,5 dans une configuration qui fonctionne de façon équilibrée ou distribuée et que vous êtes en train d’exécuter dans une configuration dont le solde de charge n’est pas équilibré.</span><span class="sxs-lookup"><span data-stu-id="e831a-185">Run the websites in MBAM 2.5 in a load-balanced or distributed configuration, and you are currently running in a configuration that is not load balanced.</span></span>

<span data-ttu-id="e831a-186">Si vous avez déjà enregistré des SPN sur le compte de l’ordinateur plutôt que dans un compte du pool d’applications, MBAM utilise les noms d’application SPN existants et vous ne pouvez pas configurer les sites Web dans une configuration distribuée ou dont le chargement est équilibré.</span><span class="sxs-lookup"><span data-stu-id="e831a-186">If you already registered SPNs on the machine account rather than in an application pool account, MBAM uses the existing SPNs, and you cannot configure the websites in a load-balanced or distributed configuration.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e831a-187">Ce que vous devez faire</span><span class="sxs-lookup"><span data-stu-id="e831a-187">What you need to do</span></span></th>
<th align="left"><span data-ttu-id="e831a-188">Exemples et informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="e831a-188">Examples and more information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e831a-189">Créer un compte de pool d’applications dans les services de domaine Active Directory (AD DS).</span><span class="sxs-lookup"><span data-stu-id="e831a-189">Create an application pool account in Active Directory Domain Services (AD DS).</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e831a-190">Supprimez les sites Web et services Web actuellement installés.</span><span class="sxs-lookup"><span data-stu-id="e831a-190">Remove the currently installed websites and web services.</span></span></p></td>
<td align="left"><p><a href="removing-mbam-server-features-or-software.md" data-raw-source="[Removing MBAM Server Features or Software](removing-mbam-server-features-or-software.md)"><span data-ttu-id="e831a-191">Suppression du logiciel ou des composants serveur de MBAM</span><span class="sxs-lookup"><span data-stu-id="e831a-191">Removing MBAM Server Features or Software</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e831a-192">Supprimer des SPN du compte d’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="e831a-192">Remove SPNs from the machine account.</span></span></p></td>
<td align="left"><p><code>Setspn –d http/mbamwebserver mbamwebserver</code></p>
<p><code>Setspn –d http/mbamwebserver.contoso.com mbamwebserver</code></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e831a-193">Enregistrez des SPN dans le compte du pool d’applications.</span><span class="sxs-lookup"><span data-stu-id="e831a-193">Register SPNs in the application pool account.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e831a-194">Suivez les étapes permettant d' <a href="#bkmk-regvirtualspn" data-raw-source="[Registering SPNs when you use a virtual host name](#bkmk-regvirtualspn)"> inscrire des SPN lorsque vous utilisez un nom d’hôte virtuel </a> .</span><span class="sxs-lookup"><span data-stu-id="e831a-194">Follow the steps for <a href="#bkmk-regvirtualspn" data-raw-source="[Registering SPNs when you use a virtual host name](#bkmk-regvirtualspn)">Registering SPNs when you use a virtual host name</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e831a-195">Reconfigurez les applications Web et les services Web.</span><span class="sxs-lookup"><span data-stu-id="e831a-195">Reconfigure the web applications and web services.</span></span></p></td>
<td align="left"><p><a href="how-to-configure-the-mbam-25-web-applications.md" data-raw-source="[How to Configure the MBAM 2.5 Web Applications](how-to-configure-the-mbam-25-web-applications.md)"><span data-ttu-id="e831a-196">Comment configurer les applications Web MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="e831a-196">How to Configure the MBAM 2.5 Web Applications</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e831a-197">Effectuez l’une des opérations suivantes, selon la méthode que vous utilisez pour la configuration:</span><span class="sxs-lookup"><span data-stu-id="e831a-197">Do one of the following, depending on the method you use for the configuration:</span></span></p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e831a-198">Méthode</span><span class="sxs-lookup"><span data-stu-id="e831a-198">Method</span></span></th>
<th align="left"><span data-ttu-id="e831a-199">Détails</span><span class="sxs-lookup"><span data-stu-id="e831a-199">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="e831a-200">Assistant Configuration de MBAM Server</span><span class="sxs-lookup"><span data-stu-id="e831a-200">MBAM Server Configuration wizard</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="e831a-201">Entrez le compte du pool d’applications dans le <strong> champ compte de domaine du pool d’applications de service Web </strong> .</span><span class="sxs-lookup"><span data-stu-id="e831a-201">Enter the application pool account in the <strong>Web service application pool domain account</strong> field.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><code>Enable-MbamWebApplication</code> <span data-ttu-id="e831a-202">Cmdlet Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="e831a-202">Windows PowerShell cmdlet</span></span></p></td>
<td align="left"><p><span data-ttu-id="e831a-203">Entrez le compte dans le <code>WebServiceApplicationPoolCredential</code> paramètre.</span><span class="sxs-lookup"><span data-stu-id="e831a-203">Enter the account in the <code>WebServiceApplicationPoolCredential</code> parameter.</span></span></p></td>
</tr>
</tbody>
</table>
<p> </p></td>
<td align="left"><div class="alert">
<strong><span data-ttu-id="e831a-204">Important</span><span class="sxs-lookup"><span data-stu-id="e831a-204">Important</span></span></strong><br/><p><span data-ttu-id="e831a-205">Le nom d’hôte que vous entrez doit être identique à celui du nom d’hôte virtuel pour lequel vous créez le SPN.</span><span class="sxs-lookup"><span data-stu-id="e831a-205">The host name that you enter must be the same name as the virtual host name for which you are creating the SPNs.</span></span> <span data-ttu-id="e831a-206">Par ailleurs, dans votre batterie de serveurs Web, les noms d’hôtes et les informations d’identification du pool d’applications doivent être identiques sur chaque serveur que vous configurez.</span><span class="sxs-lookup"><span data-stu-id="e831a-206">Also, in your web farm, the host names and the application pool credentials must be the same on every server that you are configuring.</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="e831a-207">Lorsque MBAM configure les applications Web, elle tente de les inscrire pour vous, mais elle peut le faire uniquement si vous disposez des droits d’administrateur de domaine sur le serveur sur lequel vous installez MBAM.</span><span class="sxs-lookup"><span data-stu-id="e831a-207">When MBAM configures the web applications, it will try to register the SPNs for you, but it can do so only if you have Domain Admin rights on the server on which you are installing MBAM.</span></span> <span data-ttu-id="e831a-208">Si vous ne disposez pas de ces droits, vous pouvez achever la configuration, mais vous devez définir les noms d’affichage avant ou après la configuration de MBAM.</span><span class="sxs-lookup"><span data-stu-id="e831a-208">If you do not have these rights, you can complete the configuration, but you will have to set the SPNs before or after you configure MBAM.</span></span></p></td>
</tr>
</tbody>
</table>

## <span data-ttu-id="e831a-209">Paramètres de filtrage de requête requis</span><span class="sxs-lookup"><span data-stu-id="e831a-209">Required Request Filtering Settings</span></span>

 <span data-ttu-id="e831a-210">'Allow extensions de nom de fichier non répertoriées’est requis pour que l’application fonctionne comme prévu.</span><span class="sxs-lookup"><span data-stu-id="e831a-210">'Allow unlisted file name extensions' is required for the application to operate as expected.</span></span>  <span data-ttu-id="e831a-211">Vous pouvez y accéder en accédant à la section «Administration et analyse de la demande de > de Microsoft»-> modifier les paramètres des fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="e831a-211">This can be found by navigating to the 'Microsoft BitLocker Administration and Monitoring' -> Request Filtering -> Edit Feature Settings.</span></span>


## <span data-ttu-id="e831a-212">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e831a-212">Related topics</span></span>


[<span data-ttu-id="e831a-213">Préparation de votre environnement pour MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="e831a-213">Preparing your Environment for MBAM 2.5</span></span>](preparing-your-environment-for-mbam-25.md)

[<span data-ttu-id="e831a-214">Conditions préalables au déploiement de MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="e831a-214">MBAM 2.5 Deployment Prerequisites</span></span>](mbam-25-deployment-prerequisites.md)





## <span data-ttu-id="e831a-215">Vous avez une suggestion pour MBAM?</span><span class="sxs-lookup"><span data-stu-id="e831a-215">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="e831a-216">Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)</span><span class="sxs-lookup"><span data-stu-id="e831a-216">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span>
- <span data-ttu-id="e831a-217">Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="e831a-217">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>



