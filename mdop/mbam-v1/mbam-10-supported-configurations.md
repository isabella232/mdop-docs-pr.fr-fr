---
title: Configurations prises en charge par MBAM1.0
description: Configurations prises en charge par MBAM1.0
author: dansimp
ms.assetid: 1f5ac58e-6a3f-47df-8a9b-4b57631ab9ee
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 2c72320379d1c9328a6b40537d37998402b1b38b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811454"
---
# Configurations prises en charge par MBAM1.0


Cette rubrique spécifie les exigences nécessaires à l’installation et à l’exécution de Microsoft BitLocker administration et de la surveillance (MBAM) dans votre environnement.

## <a href="" id="---------mbam-server-system-requirements"></a> Configuration système requise pour MBAM Server


### Configuration requise du système d’exploitation serveur

Le tableau suivant répertorie les systèmes d’exploitation pris en charge pour l’installation du serveur d’administration et de surveillance de BitLocker.

**Remarque**  
Microsoft prend en charge le Service Pack actuel et, dans certains cas, le Service Pack immédiatement précédent. Pour savoir comment accéder aux délais de prise en charge de votre produit, voir les [Service Packs pris en charge](https://go.microsoft.com/fwlink/p/?LinkId=31975). Pour plus d’informations sur la politique de support Microsoft, voir FAQ sur la politique de support [Microsoft](https://go.microsoft.com/fwlink/p/?LinkId=31976).



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Systèmed’exploitation</th>
<th align="left">Édition</th>
<th align="left">Service Pack</th>
<th align="left">Architecture système</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>WindowsServer2008</p></td>
<td align="left"><p>Standard, entreprise, Datacenter ou serveur Web</p></td>
<td align="left"><p>SP2 uniquement</p></td>
<td align="left"><p>32bits ou 64bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008R2</p></td>
<td align="left"><p>Standard, entreprise, Datacenter ou serveur Web</p></td>
<td align="left"></td>
<td align="left"><p>64 bits</p></td>
</tr>
</tbody>
</table>



**Warning**  
Il n’y a pas de prise en charge pour l’installation des services ou des rapports MBAM sur un ordinateur contrôleur de domaine.



### <a href="" id="server-random-access-memory--ram--requirements-"></a>Configuration requise pour la mémoire RAM (Random Access Memory) du serveur

Il n’existe aucune exigence de RAM spécifique à l’installation de MBAM Server.

### <a href="" id="sql-server-database-requirements-"></a>Configuration requise pour la base de données SQL Server

Le tableau suivant répertorie les versions de SQL Server prises en charge pour l’installation de la fonctionnalité de serveur MBAM.

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Fonctionnalité du serveur MBAM</th>
<th align="left">Version de SQL Server</th>
<th align="left">Édition</th>
<th align="left">Service Pack</th>
<th align="left">Architecture système</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Rapports de conformité et d’audit</p></td>
<td align="left"><p>Microsoft SQL Server 2008 </p></td>
<td align="left"><p>R2, standard, entreprise, Datacenter ou édition développeur</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>32bits ou 64bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>Base de données de récupération et de matériel</p></td>
<td align="left"><p>Microsoft SQL Server 2008 </p></td>
<td align="left"><p>R2, entreprise, Datacenter ou édition développeur</p>
<div class="alert">
<strong>Important</strong><br/><p>Les éditions de SQL Server standard ne sont pas prises en charge pour l’installation de la fonctionnalité de restauration MBAM et de base de données matérielle.</p>
</div>
<div>

</div></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>32bits ou 64bits</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Base de données d’audit et de conformité</p></td>
<td align="left"><p>Microsoft SQL Server 2008 </p></td>
<td align="left"><p>R2, standard, entreprise, Datacenter ou édition développeur</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>32bits ou 64bits</p></td>
</tr>
</tbody>
</table>



## <a href="" id="---------mbam-client-system-requirements"></a> Configuration système requise pour le client MBAM


### Configuration requise du système d’exploitation client

Le tableau suivant répertorie les systèmes d’exploitation pris en charge pour l’installation du client MBAM.

**Remarque**  
Microsoft prend en charge le Service Pack actuel et, dans certains cas, le Service Pack immédiatement précédent. Pour savoir comment accéder aux délais de prise en charge de votre produit, voir les [Service Packs pris en charge](https://go.microsoft.com/fwlink/p/?LinkId=31975). Pour plus d’informations sur la politique de support Microsoft, voir FAQ sur la politique de support [Microsoft](https://go.microsoft.com/fwlink/p/?LinkId=31976).



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Systèmed’exploitation</th>
<th align="left">Édition</th>
<th align="left">Service Pack</th>
<th align="left">Architecture système</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows7</p></td>
<td align="left"><p>Édition Entreprise</p></td>
<td align="left"><p>Aucun, SP1</p></td>
<td align="left"><p>32bits ou 64bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows7</p></td>
<td align="left"><p>Édition intégrale</p></td>
<td align="left"><p>Aucun, SP1</p></td>
<td align="left"><p>32bits ou 64bits</p></td>
</tr>
</tbody>
</table>



### <a href="" id="client-ram-requirements-"></a>Configuration requise pour le client RAM

Il n’existe aucune exigence de RAM spécifique à l’installation du client MBAM.

## Rubriques connexes


[Planification du déploiement de MBAM1.0](planning-to-deploy-mbam-10.md)

[Conditions préalables au déploiement de MBAM1.0](mbam-10-deployment-prerequisites.md)









