---
title: Considérations relatives à la sécurité d'App-V5.1
description: Considérations relatives à la sécurité d'App-V5.1
author: dansimp
ms.assetid: 6bc6c1fc-f813-47d4-b763-06fd4faf6a72
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 8a5606b3e0ba5e6fb8c62f14e2ed8d93ea2cf134
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805971"
---
# Considérations relatives à la sécurité d'App-V5.1


Cette rubrique fournit une vue d’ensemble des comptes et des groupes, des fichiers journaux et d’autres considérations en matière de sécurité pour Microsoft Application Virtualization (App-V) 5,1.

**Important**  
App-V 5,1 n’est pas un produit de sécurité et ne fournit aucune garantie pour un environnement sécurisé.



## La fonctionnalité PackageStoreAccessControl (PSAC) est déconseillée


À compter de juin, 2014, PackageStoreAccessControl (PSAC), incluse dans Microsoft Application Virtualization (App-V) 5,0 Service Pack 2 (SP2), a été déconseillée dans les environnements à utilisateurs unique et à plusieurs utilisateurs.

## Considérations générales en matière de sécurité


**Comprenez les risques en matière de sécurité.** Le risque le plus sérieux pour App-V 5,1 est qu’il peut être détourné par un utilisateur non autorisé qui peut ensuite reconfigurer des données clés sur des clients App-V 5,1. La perte de fonctionnalité de l’application 5,1 App-V pour une courte période à cause d’une attaque par déni de service n’a généralement pas d’impact sur la catastrophe.

**Sécurisez vos ordinateurs de façon sécurisée**. La sécurité est incomplète sans sécurité physique. Toute personne disposant d’un accès physique à un serveur App-V 5,1 peut éventuellement attaquer la base de clients entière. Tout risque d’attaques physiques potentielles doit être considéré comme présentant un risque élevé et atténué de manière appropriée. Les serveurs App-V 5,1 doivent être stockés dans une salle serveur sécurisée avec accès contrôlé. Sécurisez ces ordinateurs lorsque les administrateurs ne sont pas présents physiquement en faisant en sorte que le système d’exploitation verrouille l’ordinateur ou à l’aide d’un économiseur d’écran sécurisé.

**Appliquez les mises à jour de sécurité les plus récentes à tous les ordinateurs**. Pour vous tenir informé des dernières mises à jour pour les systèmes d’exploitation, Microsoft SQL Server et App-V 5,1, abonnez-vous au service de notification de sécurité ( <https://go.microsoft.com/fwlink/p/?LinkId=28819> ).

**Utiliser des mots de passe forts ou des expressions de passe**. Utilisez toujours des mots de passe forts avec au moins 15 caractères pour tous les comptes d’administrateur App-V 5,1 et App-V 5,1. N’utilisez jamais de mots de passe vides. Pour plus d’informations sur les concepts de mot de passe, consultez le livre blanc «mots de passe et stratégies de compte» sur TechNet ( <https://go.microsoft.com/fwlink/p/?LinkId=30009> ).

## Comptes et groupes dans App-V 5,1


Pour la gestion des comptes d’utilisateur, il est recommandé de créer des groupes globaux de domaine et d’y ajouter des comptes d’utilisateurs. Ensuite, ajoutez les comptes globaux Domain aux groupes locaux App-V 5,1 nécessaires sur les serveurs App-V 5,1.

**Remarque**  
Les comptes d’ordinateur client App-V qui doivent se connecter au serveur de publication doivent faire partie du groupe local **utilisateurs** du serveur de publication. Par défaut, tous les ordinateurs du domaine font partie du groupe **utilisateurs autorisés** , qui fait partie du groupe local **utilisateurs** .



### <a href="" id="-------------app-v-5-1-server-security"></a> Sécurité du serveur App-V 5,1

Aucun groupe n’est créé automatiquement lors de la configuration de App-V 5,1. Il est recommandé de créer les groupes globaux services de domaine Active Directory suivants pour gérer les opérations du serveur App-V 5,1.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nom du groupe</th>
<th align="left">Détails</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Groupe d’administration de l’application-V</p></td>
<td align="left"><p>Utilisé pour gérer le serveur de gestion App-V 5,1. Ce groupe est créé pendant l’installation de l’application-V 5,1 Management Server.</p>
<div class="alert">
<strong>Important</strong><br/><p>Il n’existe aucune méthode de création du groupe à l’aide de la console de gestion une fois l’installation terminée.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Lecture/écriture de base de données pour le compte de service de gestion</p></td>
<td align="left"><p>Fournit un accès en lecture/écriture à la base de données de gestion. Ce compte doit être créé lors de l’installation de la base de données de gestion App-V 5,1.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Compte d’administrateur d’installation du service d’application-V</p>
<div class="alert">
<strong>Remarque</strong><br/><p>Ceci est requis uniquement si la base de données de gestion est installée séparément du service.</p>
</div>
<div>

</div></td>
<td align="left"><p>Fournit un accès public à la table de version de schéma dans la base de données de gestion. Ce compte doit être créé lors de l’installation de la base de données de gestion App-V 5,1.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Compte d’administrateur d’installation du service de création de rapports App-V</p>
<div class="alert">
<strong>Remarque</strong><br/><p>Ceci est requis uniquement si la base de données de création de rapports est installée séparément du service.</p>
</div>
<div>

</div></td>
<td align="left"><p>Accès public à la table Schema-Version dans la base de données de création de rapports. Ce compte doit être créé lors de l’installation de la base de données de création de rapports App-V 5,1.</p></td>
</tr>
</tbody>
</table>



Prenez en compte les informations supplémentaires suivantes:

-   Accès aux partages du package: s’il existe un partage sur le même ordinateur que le serveur de gestion, le service **réseau** doit avoir accès en lecture au partage. Par ailleurs, chaque ordinateur client App-V doit avoir accès en lecture au partage de package.

    **Remarque**  
    Dans les versions précédentes de App-V, le partage de package était appelé partage de contenu.



-   Inscription des serveurs de publication auprès du serveur de gestion: un serveur de publication doit être enregistré auprès du serveur de gestion. Par exemple, il doit être ajouté à la base de données, de sorte que les comptes d’ordinateur du serveur de publication puissent appeler l’API du service de gestion.

### <a href="" id="-------------app-v-5-1-package-security"></a> Sécurité du package App-V 5,1

Vous trouverez ci-après des informations sur la façon de garantir la sécurité des packages virtualisés.

-   Si un programme d’installation d’application applique une liste de contrôle d’accès (ACL) à un fichier ou un répertoire, il n’est pas conservé dans le package. Lorsque le package est déployé, si le fichier ou le répertoire est modifié par un utilisateur, il héritera de l’ACL dans le **% UserProfile%** ou héritera de la liste de contrôle d’accès de l’annuaire de l’ordinateur cible. Le premier cas se produit si le fichier ou le répertoire n’existe pas dans l’emplacement du système de fichiers virtuel; ce dernier cas se produit si le fichier ou répertoire existe dans l’emplacement du système de fichiers virtuel, par exemple **% windir%**.

## <a href="" id="---------app-v-5-1-log-files"></a> Fichiers journaux App-V 5,1


Lors de l’installation d’App-V 5,1, les fichiers journaux d’installation sont créés dans le dossier **% temp%** de l’utilisateur qui a installé l’application.






## Rubriques connexes


[Préparation de votre environnement pour App-V5.1](preparing-your-environment-for-app-v-51.md)









