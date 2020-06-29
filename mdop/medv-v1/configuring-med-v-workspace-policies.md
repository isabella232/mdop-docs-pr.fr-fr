---
title: Configuration de stratégies d'espace de travail MED-V
description: Configuration de stratégies d'espace de travail MED-V
author: dansimp
ms.assetid: 0eaed981-cbf3-4b16-a4b7-4705c5705dc7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 84bdae38b1c801e2c2be2a3dd1d12dd2ca7d932d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810806"
---
# Configuration de stratégies d'espace de travail MED-V


Une stratégie d’espace de travail MED-V est un ensemble de paramètres configurables qui déterminent le mode d’exécution des applications et de l’environnement virtualisé sur l’ordinateur hôte. Les rubriques de cette section décrivent tous les paramètres configurables de la stratégie d’espace de travail MED-V ainsi que leur influence sur l’espace de travail MED-V.

Les types d’espace de travail MED-V suivants sont disponibles:

-   **Permanent**: dans un espace de travail MED-v persistant, toutes les modifications et ajouts apportées par l’utilisateur à l’espace de travail MED-v sont enregistrés dans l’espace de travail MED-v entre les sessions. Par ailleurs, un espace de travail MED-V permanent est généralement utilisé dans un environnement de domaine.

-   **Revertible**: dans un espace de travail Revertible med-v, à l’achèvement de chaque session (autrement dit, lorsque l’espace de travail MED-v est arrêté), l’espace de travail MED-v retrouve son état d’origine lors du déploiement. Aucune modification ou aucun complément n’est enregistré dans l’espace de travail MED-V entre les sessions. Un espace de travail revertible MED-V ne peut pas être utilisé dans un environnement de domaine.

Il est important de décider du type d’espace de travail MED-V que vous créez avant de déployer l’espace de travail MED-V, car il n’est pas recommandé de reconfigurer le type d’espace de travail MED-V après le déploiement d’une stratégie sur les utilisateurs.

**Remarques**  Lorsque vous configurez une stratégie, un symbole d’avertissement s’affiche en regard de champs obligatoires qui ne sont pas renseignés. Si un champ obligatoire n’est pas renseigné, le symbole s’affiche également dans l’onglet.

 

## Dans cette section


<a href="" id="how-to-apply-general-settings-to-a-med-v-workspace"></a>[Comment appliquer des paramètres généraux à un espace de travail MED-V](how-to-apply-general-settings-to-a-med-v-workspace.md)  
Décrit les paramètres généraux d’un espace de travail MED-V et comment les appliquer à une stratégie.

<a href="" id="how-to-apply-virtual-machine-settings-to-a-med-v-workspace"></a>[Comment appliquer des paramètres de machine virtuelle à un espace de travail MED-V](how-to-apply-virtual-machine-settings-to-a-med-v-workspace.md)  
Décrit les paramètres de la machine virtuelle pour un espace de travail MED-V et la façon de les appliquer à une stratégie.

<a href="" id="how-to-configure-a-domain-user-or-group"></a>[Comment configurer un utilisateur ou un groupe de domaine](how-to-configure-a-domain-user-or-groupmedvv2.md)  
Décrit comment configurer les utilisateurs et les groupes du domaine.

<a href="" id="how-to-configure-published-applications"></a>[Comment configurer des applications publiées](how-to-configure-published-applicationsmedvv2.md)  
Décrit les applications et les menus publiés et comment les appliquer à une stratégie.

<a href="" id="how-to-configure-web-settings-for-a-med-v-workspace"></a>[Comment configurer les paramètres Web pour un espace de travail MED-V](how-to-configure-web-settings-for-a-med-v-workspace.md)  
Décrit les paramètres Web disponibles pour un espace de travail MED-V et la façon de les appliquer à une stratégie.

<a href="" id="how-to-configure-the-virtual-machine-setup-for-a-med-v-workspace"></a>[Comment configurer l'installation d'ordinateur virtuel pour un espace de travail MED-V](how-to-configure-the-virtual-machine-setup-for-a-med-v-workspace.md)  
Décrit la configuration de l’ordinateur virtuel pour un espace de travail MED-V et l’appliquer à une stratégie.

<a href="" id="how-to-apply-network-settings-to-a-med-v-workspace"></a>[Comment appliquer des paramètres réseau à un espace de travail MED-V](how-to-apply-network-settings-to-a-med-v-workspace.md)  
Décrit les paramètres réseau d’un espace de travail MED-V et la façon de les appliquer à une stratégie.

<a href="" id="how-to-apply-performance-settings-to-a-med-v-workspace"></a>[Comment appliquer des paramètres de performances à un espace de travail MED-V](how-to-apply-performance-settings-to-a-med-v-workspace.md)  
Décrit les paramètres de performances d’un espace de travail MED-V et la façon de les appliquer à une stratégie.

<a href="" id="how-to-import-and-export-a-policy"></a>[Comment importer et exporter une stratégie](how-to-import-and-export-a-policy.md)  
Décrit comment importer et exporter une stratégie.

 

 





