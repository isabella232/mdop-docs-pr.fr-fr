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
# Planification de la sécurisation des sites web MBAM


Cette rubrique décrit les méthodes suivantes pour sécuriser le site Web d’administration et de surveillance de Microsoft BitLocker (MBAM 2,5), ainsi que le portail libre-service.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Méthode</th>
<th align="left">Obligatoire ou facultatif?</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Utiliser des certificats pour sécuriser les sites Web MBAM</p></td>
<td align="left"><p>Facultatif, mais fortement recommandé</p></td>
</tr>
<tr class="even">
<td align="left"><p>Inscription des noms de principal de service (SPN) pour le compte du pool d’applications</p></td>
<td align="left"><p>Requis</p></td>
</tr>
</tbody>
</table>



Pour plus d’informations sur la façon de sécuriser votre déploiement MBAM, voir [considérations relatives à la sécurité dans MBAM 2,5](mbam-25-security-considerations.md).

## Utiliser des certificats pour sécuriser les sites Web MBAM


Nous vous recommandons d’utiliser un certificat pour sécuriser la communication entre:

-   Client MBAM et services Web

-   Navigateur et site Web d’administration et de surveillance et sites Web de portail libre-service

Pour plus d’informations sur la demande et l’installation d’un certificat, voir [configurer des certificats de serveur Internet](https://technet.microsoft.com/library/cc731977.aspx).

**Remarque**  
Vous pouvez configurer les sites Web et services Web sur des serveurs différents uniquement si vous utilisez Windows PowerShell. Si vous utilisez l’Assistant Configuration de MBAM Server pour configurer les sites Web, vous devez configurer les sites Web et les services Web sur le même serveur.



Pour sécuriser la communication entre les services Web et les bases de données, nous vous conseillons également de forcer le chiffrement dans SQL Server. Pour plus d’informations sur la sécurisation de toutes les connexions à SQL Server, y compris la communication entre les services Web et SQL Server, voir [considérations relatives à la sécurité de MBAM 2,5](mbam-25-security-considerations.md#bkmk-secure-databases).

## Inscription de SPN pour le compte du pool d’applications


Pour permettre aux serveurs MBAM d’authentifier les communications à partir du site Web d’administration et de surveillance et du portail libre-service, vous devez inscrire un nom de principal de service (SPN) pour le nom d’hôte sous le compte de domaine que vous utilisez pour le pool d’applications Web.

Cette rubrique contient des instructions sur la façon d’enregistrer des noms de fichier SPN pour les types de noms d’hôtes suivants:

-   Nom de domaine complet

-   Nom NetBIOS

-   Nom virtuel

### Avant de créer des SPN pour une installation MBAM initiale

Passez en revue les informations figurant dans le tableau suivant avant de commencer à créer des SPN.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tâche ou élément</th>
<th align="left">Informations supplémentaires</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Créer un compte de service dans les services de domaine Active Directory (AD DS).</p></td>
<td align="left"><p>Le compte de service est un compte d’utilisateur que vous créez dans AD DS pour garantir la sécurité des sites Web MBAM. Les sites Web MBAM s’exécutent sous un pool d’applications, dont l’identité correspond au nom du compte de service. Le SPN est alors enregistré dans le compte du pool d’applications.</p>
<div class="alert">
<strong>Remarque</strong><br/><p>Vous devez utiliser le même compte de pool d’applications pour tous les serveurs Web.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Vérifiez que le compte de groupe IIS-IUSRS ou le compte du pool d’applications a reçu les droits nécessaires.</p></td>
<td align="left"><p>Pour cela, procédez comme suit:</p>
<ol>
<li><p>Ouvrez l' <strong> éditeur de stratégie de sécurité local </strong> et développez le <strong> nœud Stratégies locales </strong> .</p></li>
<li><p>Sélectionnez le <strong> nœud d’attribution de droits </strong> d’utilisateur, puis double-cliquez sur l’option <strong> emprunter l’identité d’un client après authentification </strong> et ouvrez une <strong> session en tant que </strong> paramètres de stratégie de groupe dans le volet droit.</p></li>
</ol></td>
</tr>
<tr class="odd">
<td align="left"><p>Si vous configurez les sites Web MBAM à l’aide d’un compte d’administrateur de domaine, MBAM créera les noms de domaine pour vous.</p></td>
<td align="left"><p>Si vous configurez les sites Web MBAM à l’aide d’un compte d’administrateur de domaine, suivez les étapes décrites dans cette rubrique pour inscrire les noms d’hôtes manuellement pour le type de nom d’hôte que vous utilisez.</p></td>
</tr>
</tbody>
</table>



### Inscription des SPN lorsque vous utilisez un nom d’hôte de domaine complet

Si vous utilisez un nom d’hôte de domaine complet lorsque vous configurez MBAM, vous devez enregistrer un seul SPN, comme indiqué dans l’exemple suivant.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Ce que vous devez faire</th>
<th align="left">Exemples et informations supplémentaires</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Enregistrez un SPN pour le nom de domaine complet.</p></td>
<td align="left"><p><code>Setspn -s http/mybitlockerrecovery.contoso.com contoso\mbamapppooluser</code></p>
<p>Le nom d’hôte complet est <strong> mybitlockerrecovery.contoso.com </strong> et le compte de domaine utilisé pour le pool d’applications Web est <strong> contoso\mbamapppooluser </strong> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Configurez la délégation contrainte pour le SPN que vous inscrivez pour le compte du pool d’applications.</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=394335" data-raw-source="[Configuring Constrained Delegation](https://go.microsoft.com/fwlink/?LinkId=394335)">Configuration de la délégation contrainte</a></p>
<p>Cette obligation ne s’applique qu’à MBAM 2,5; Il n’est pas nécessaire dans MBAM 2,5 SP1.</p></td>
</tr>
</tbody>
</table>



### Inscription des SPN lorsque vous utilisez un nom d’hôte NetBIOS

Si vous utilisez un nom d’hôte NetBIOS lorsque vous configurez MBAM, inscrivez un SPN pour le nom NetBIOS et un autre SPN pour le nom de domaine complet, comme indiqué dans les exemples suivants.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Ce que vous devez faire</th>
<th align="left">Exemples et informations supplémentaires</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Enregistrez un SPN pour le nom d’hôte NetBIOS.</p></td>
<td align="left"><p><code>Setspn -s http/nbname01 contoso\mbamapppooluser</code></p>
<p>Le nom d’hôte NetBIOS est <strong> nbname01 </strong> et le compte de domaine utilisé pour le pool d’applications Web est <strong> contoso\mbamapppooluser </strong> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Enregistrez un SPN pour le nom de domaine complet.</p></td>
<td align="left"><p><code>Setspn –s http/nbname01.corp.contoso.com contoso\mbamapppooluser</code></p>
<p>Le nom de domaine complet est <strong> nbname01.contoso.com </strong> et le compte de domaine utilisé pour le pool d’applications Web est <strong> contoso\mbamapppooluser </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Configurez la délégation contrainte pour les noms d’application (SPN) que vous inscrivez pour le compte du pool d’applications.</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=394335" data-raw-source="[Configuring Constrained Delegation](https://go.microsoft.com/fwlink/?LinkId=394335)">Configuration de la délégation contrainte</a></p>
<p>Cette obligation ne s’applique qu’à MBAM 2,5; Il n’est pas nécessaire dans MBAM 2,5 SP1.</p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-regvirtualspn"></a>Inscription des SPN lorsque vous utilisez un nom d’hôte virtuel

Si vous configurez MBAM avec un nom d’hôte virtuel qui est un nom de domaine complet, n’enregistrez qu’un SPN pour le nom d’hôte virtuel. Si le nom d’hôte virtuel que vous configurez n’est pas un nom de domaine complet, vous devez créer un deuxième SPN spécifiant le nom de domaine complet, comme décrit dans les exemples suivants.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Ce que vous devez faire</th>
<th align="left">Exemples et informations supplémentaires</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>S’il s’agit d’un nom de domaine complet, tel que dans cet exemple, n’enregistrez qu’un SPN.</p></td>
<td align="left"><p><code>Setspn -s http/mbamvirtual.contoso.com contoso\mbamapppooluser</code></p>
<p>Dans l’exemple, le nom d’hôte virtuel est <strong> mbamvirtual.contoso.com </strong> et le compte de domaine utilisé pour le pool d’applications Web est <strong> contoso\mbamapppooluser </strong> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Enregistrez ce SPN supplémentaire si votre nom d’hôte virtuel n’est pas un nom de domaine complet.</p></td>
<td align="left"><p><code>Setspn -s http/mbamvirtual contoso\mbamapppooluser</code></p>
<p>Dans l’exemple, le nom d’hôte virtuel est <strong> mbamvirtual </strong> et le compte de domaine utilisé pour le pool d’applications Web est <strong> contoso\mbamapppooluser </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Enregistrez ce SPN supplémentaire si votre nom d’hôte virtuel n’est pas un nom de domaine complet.</p></td>
<td align="left"><p><code>Setspn -s http/mbamvirtual.contoso.com contoso\mbamapppooluser</code></p>
<p>Dans l’exemple, le nom d’hôte virtuel est <strong> mbamvirtual.contoso.com </strong> et le compte de domaine utilisé pour le pool d’applications Web est <strong> contoso\mbamapppooluser </strong> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Sur le serveur DNS (Domain Name Server), créez un «A record» pour le nom d’hôte personnalisé et placez-le sur un serveur Web ou un équilibrage de charge.</p></td>
<td align="left"><p>Voir la section «Configuration de l’hôte DNS A Records» dans <a href="https://go.microsoft.com/fwlink/?LinkId=394337" data-raw-source="[Configure DNS Host Records](https://go.microsoft.com/fwlink/?LinkId=394337)"> configurer les enregistrements d’hôte DNS </a> .</p>
<p>Nous vous recommandons d’utiliser un enregistrement au lieu de CNAMe. Si vous utilisez les noms d’application (CNAMe) pour qu’ils pointent vers l’adresse de domaine, vous devez également inscrire les SPN pour le nom du serveur Web dans le compte du pool d’applications.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Configurez la délégation contrainte pour les noms d’application (SPN) que vous inscrivez pour le compte du pool d’applications.</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=394335" data-raw-source="[Configuring Constrained Delegation](https://go.microsoft.com/fwlink/?LinkId=394335)">Configuration de la délégation contrainte</a></p>
<p>Cette obligation ne s’applique qu’à MBAM 2,5; Il n’est pas nécessaire dans MBAM 2,5 SP1.</p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-registerspn"></a>Inscription d’un SPN lorsque vous effectuez une mise à niveau à partir d’une version précédente de MBAM

Suivez les étapes décrites dans cette section uniquement si vous souhaitez:

-   Effectuer une mise à niveau à partir d’une version précédente de MBAM.

-   Exécutez les sites Web dans MBAM 2,5 dans une configuration qui fonctionne de façon équilibrée ou distribuée et que vous êtes en train d’exécuter dans une configuration dont le solde de charge n’est pas équilibré.

Si vous avez déjà enregistré des SPN sur le compte de l’ordinateur plutôt que dans un compte du pool d’applications, MBAM utilise les noms d’application SPN existants et vous ne pouvez pas configurer les sites Web dans une configuration distribuée ou dont le chargement est équilibré.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Ce que vous devez faire</th>
<th align="left">Exemples et informations supplémentaires</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Créer un compte de pool d’applications dans les services de domaine Active Directory (AD DS).</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Supprimez les sites Web et services Web actuellement installés.</p></td>
<td align="left"><p><a href="removing-mbam-server-features-or-software.md" data-raw-source="[Removing MBAM Server Features or Software](removing-mbam-server-features-or-software.md)">Suppression du logiciel ou des composants serveur de MBAM</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Supprimer des SPN du compte d’ordinateur.</p></td>
<td align="left"><p><code>Setspn –d http/mbamwebserver mbamwebserver</code></p>
<p><code>Setspn –d http/mbamwebserver.contoso.com mbamwebserver</code></p></td>
</tr>
<tr class="even">
<td align="left"><p>Enregistrez des SPN dans le compte du pool d’applications.</p></td>
<td align="left"><p>Suivez les étapes permettant d' <a href="#bkmk-regvirtualspn" data-raw-source="[Registering SPNs when you use a virtual host name](#bkmk-regvirtualspn)"> inscrire des SPN lorsque vous utilisez un nom d’hôte virtuel </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Reconfigurez les applications Web et les services Web.</p></td>
<td align="left"><p><a href="how-to-configure-the-mbam-25-web-applications.md" data-raw-source="[How to Configure the MBAM 2.5 Web Applications](how-to-configure-the-mbam-25-web-applications.md)">Comment configurer les applications Web MBAM2.5</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Effectuez l’une des opérations suivantes, selon la méthode que vous utilisez pour la configuration:</p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Méthode</th>
<th align="left">Détails</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Assistant Configuration de MBAM Server</strong></p></td>
<td align="left"><p>Entrez le compte du pool d’applications dans le <strong> champ compte de domaine du pool d’applications de service Web </strong> .</p></td>
</tr>
<tr class="even">
<td align="left"><p><code>Enable-MbamWebApplication</code> Cmdlet Windows PowerShell</p></td>
<td align="left"><p>Entrez le compte dans le <code>WebServiceApplicationPoolCredential</code> paramètre.</p></td>
</tr>
</tbody>
</table>
<p> </p></td>
<td align="left"><div class="alert">
<strong>Important</strong><br/><p>Le nom d’hôte que vous entrez doit être identique à celui du nom d’hôte virtuel pour lequel vous créez le SPN. Par ailleurs, dans votre batterie de serveurs Web, les noms d’hôtes et les informations d’identification du pool d’applications doivent être identiques sur chaque serveur que vous configurez.</p>
</div>
<div>

</div>
<p>Lorsque MBAM configure les applications Web, elle tente de les inscrire pour vous, mais elle peut le faire uniquement si vous disposez des droits d’administrateur de domaine sur le serveur sur lequel vous installez MBAM. Si vous ne disposez pas de ces droits, vous pouvez achever la configuration, mais vous devez définir les noms d’affichage avant ou après la configuration de MBAM.</p></td>
</tr>
</tbody>
</table>

## Paramètres de filtrage de requête requis

 'Allow extensions de nom de fichier non répertoriées’est requis pour que l’application fonctionne comme prévu.  Vous pouvez y accéder en accédant à la section «Administration et analyse de la demande de > de Microsoft»-> modifier les paramètres des fonctionnalités.


## Rubriques connexes


[Préparation de votre environnement pour MBAM2.5](preparing-your-environment-for-mbam-25.md)

[Conditions préalables au déploiement de MBAM2.5](mbam-25-deployment-prerequisites.md)





## Vous avez une suggestion pour MBAM?
- Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)
- Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).



