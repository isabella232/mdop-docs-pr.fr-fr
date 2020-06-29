---
title: Messages du journal des événements MED-V
description: Messages du journal des événements MED-V
author: dansimp
ms.assetid: 7ba7344d-153b-4cc4-a00a-5d42aee9986b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b5d8dcf1cce48d6c1e29d46b4db7ac1550aa9477
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809738"
---
# Messages du journal des événements MED-V


Les fichiers journaux pour Microsoft Enterprise Desktop Virtualization (MED-V) 2,0 fournissent des informations détaillées sur le déploiement et la gestion de MED-V au sein de votre entreprise et permettent de vérifier les fonctionnalités ou d’aider à résoudre les problèmes.

## ID d’événement


Voici une liste des ID d’événement MED-V qui vous aideront à résoudre les problèmes que vous pouvez rencontrer lors du déploiement ou de la gestion de MED-V.

### FTS

Affiche les ID d’événement pour la première fois.

### ID d’événement 3066

Échec de l’opération de démarrage de l’ordinateur virtuel.

<a href="" id="description"></a>**Description**  
Il existe un problème potentiel avec le disque dur virtuel (VHD) que vous utilisez pour créer un espace de travail MED-V.

<a href="" id="solution"></a>**Solution**  
Vérifiez que vous pouvez créer une machine virtuelle avec le disque dur virtuel pour MED-V et qu’elle peut être démarrée.

### ID d’événement 3071

Échec de la préparation de l’ordinateur virtuel.

<a href="" id="description"></a>**Description**  
Un problème s’est produit lors de la première configuration qui aurait peut-être provoquée par différents problèmes. Ces problèmes concernent la connectivité réseau.

<a href="" id="solution"></a>**Solution**  
Redémarrez l’agent hôte MED-V pour réexécuter la première fois.

### ID d’événement 3078

Échec de la préparation de l’ordinateur virtuel.

<a href="" id="description"></a>**Description**  
Il existe un problème potentiel avec le disque dur virtuel que vous utilisez pour créer un espace de travail MED-V.

<a href="" id="solution"></a>**Solution**  
Vérifiez que vous pouvez créer une machine virtuelle avec le disque dur virtuel pour MED-V et qu’elle peut être démarrée.

### ID d’événement 3079

Nouvelle tentative de préparation de l’ordinateur virtuel.

<a href="" id="description"></a>**Description**  
MED-V tente de préparer l’ordinateur virtuel.

<a href="" id="solution"></a>**Solution**  
Aucune action n’est requise. Fin de la configuration pour la première fois.

### ID d’événement 3080

Le client a été arrêté lors de la préparation de l’ordinateur virtuel.

<a href="" id="description"></a>**Description**  
MED-V s’arrête de manière inattendue lorsqu’il tente de préparer l’ordinateur virtuel.

<a href="" id="solution"></a>**Solution**  
Démarrer l’agent d’hébergement MED-V et permettre la fin de la configuration pour la première fois

### ID d’événement 3084

Ordinateur virtuel non valide. La première fois que vous devez réexécuter le programme d’installation.

<a href="" id="description"></a>**Description**  
L’agent d’hébergement MED-V a détecté un problème avec la machine virtuelle.

<a href="" id="solution"></a>**Solution**  
Aucune action n’est requise. Fin de la configuration pour la première fois.

### ID d’événement 3099

Échec de l’appel pour démarrer l’ordinateur virtuel.

<a href="" id="description"></a>**Description**  
Il existe un problème potentiel lié au VHD que vous utilisez pour créer un espace de travail MED-V.

<a href="" id="solution"></a>**Solution**  
Vérifiez que vous pouvez créer une machine virtuelle avec le disque dur virtuel pour MED-V et qu’elle peut être ouverte.

### Gestion de l’ordinateur virtuel

### ID d’événement 4022

VMManagerException erreur irrécupérable lors de la création de la commande sur la machine virtuelle.

<a href="" id="description"></a>**Description**  
L’utilisateur final a essayé de quitter MED-V en vous déconnectant ou en arrêtant l’hôte MED-V, et le paramètre de configuration VMTaskTimeout a été dépassé.

<a href="" id="solution"></a>**Solution**  
Redémarrez MED-V.

### ID d’événement 4028

Dépassement du délai de l’opération VM.

<a href="" id="description"></a>**Description**  
L’utilisateur final a essayé de quitter MED-V en vous déconnectant ou en arrêtant l’hôte, et le paramètre de configuration VMTaskTimeout a été dépassé.

<a href="" id="solution"></a>**Solution**  
Redémarrez MED-V.

### ID d’événement 4038

Vmsal publié un message d’erreur pour l’utilisateur.

<a href="" id="description"></a>**Description**  
Un message d’erreur s’affiche à l’utilisateur final indiquant que MED-V n’a pas pu démarrer l’application virtuelle.

<a href="" id="solution"></a>**Solution**  
Si l’erreur est journalisée plusieurs fois dans une ligne, arrêtez MED-V, puis connectez-vous à l’ordinateur virtuel à l’aide de la console de l’ordinateur virtuel Windows et essayez de démarrer l’application en mode plein écran.

### ID d’événement 4040

Les ajouts de recyclage car TerminalServices n’est pas initialisé dans l’invité.

<a href="" id="description"></a>**Description**  
MED-V a redémarré l’ordinateur virtuel, car le service bureau à distance n’a pas été initialisé sur l’ordinateur virtuel.

<a href="" id="solution"></a>**Solution**  
Si l’erreur est journalisée plusieurs fois dans une ligne, arrêtez MED-V et connectez-vous à l’ordinateur virtuel à l’aide de la console Windows Virtual PC.

### ID d’événement 4042

Échec du recyclage des ajouts dans l’invité.

<a href="" id="description"></a>**Description**  
MED-V n’a pas réussi à recycler les ajouts de machines virtuelles sur l’ordinateur virtuel.

<a href="" id="solution"></a>**Solution**  
Si l’erreur est journalisée plusieurs fois dans une ligne, arrêtez MED-V et connectez-vous à l’ordinateur virtuel à l’aide de la console Windows Virtual PC.

### ID d’événement 4043

Échec de la réinitialisation du mot de passe expiré dans l’ordinateur virtuel.

<a href="" id="description"></a>**Description**  
L’utilisateur final n’a pas réinitialisé le mot de passe dans l’ordinateur virtuel avant son expiration. Par conséquent, l’utilisateur n’est peut-être pas en mesure d’accéder aux ressources réseau ou d’enregistrer le fonctionnement.

<a href="" id="solution"></a>**Solution**  
Arrêtez l’invité MED-V, puis redémarrez-le.

### Redirection d’URL

### ID d’événement 5005

Impossible d’obtenir le nom de l’ordinateur virtuel de la configuration; ne peut pas lancer le navigateur invité.

<a href="" id="description"></a>**Description**  
La redirection d’URL n’a pas pu obtenir le nom de l’espace de travail MED-V depuis la configuration. Par conséquent, il ne peut pas informer Windows Virtual PC de l’ouverture de l’URL redirigée dans le navigateur d’espace de travail MED-V.

<a href="" id="solution"></a>**Solution**  
Assurez-vous que le nom de l’espace de travail MED-V est défini et qu’il correspond à un nom de machine virtuelle dans l’annuaire de l' &lt; *utilisateur*C:\\Users\\ &gt; \\Virtual. Le nom de l’espace de travail MED-V se trouve sur HKLM\\SOFTWARE\\Microsoft\\Medv\\v2\\VM\\Name.

Par exemple, si l’utilisateur est «mat» et que le nom de l’espace de travail est «mattsworkspace», la valeur de HKLM\\SOFTWARE\\Microsoft\\Medv\\v2\\VM\\Name doit être «mattsworkspace» et il devrait y avoir un fichier nommé C:\\Users\\Matt\\Virtual Machines\\mattsworkspace.vcmx.

### ID d’événement 5006

Échec de la création du serveur de canaux.

<a href="" id="description"></a>**Description**  
Le service de redirection d’URL n’a pas pu créer le serveur de canaux pour communiquer avec Internet Explorer.

<a href="" id="solution"></a>**Solution**  
Vérifiez les journaux d’événements système pour les tentatives de création d’un fichier ou d’une ressource dont le chemin d’accès commence comme suit: «\\\\.\\pipe\\MEDVUrlRedirectionPipe\_» et se termine par le nom d’utilisateur et le nom de domaine de l’utilisateur. Si ce n’est pas le cas, redémarrez l’ordinateur.

### ConfigMgr (invité)

### ID d’événement 7001

La mise en forme des données de configuration du réseau hôte n’est pas correcte.

<a href="" id="description"></a>**Description**  
La configuration réseau reçue de l’hôte est une chaîne XML incorrectement mise en forme ou les informations réseau renvoyées par l’hôte ne peuvent pas être écrites dans un document XML.

<a href="" id="solution"></a>**Solution**  
Redémarrez l’ordinateur hôte et l’ordinateur virtuel.

### ID d’événement 7005

Une modification apportée à la configuration du réseau hôte a été détectée, mais elle n’a pas pu être appliquée car les données de configuration du réseau hôte n’ont pas été correctement mises en forme.

<a href="" id="description"></a>**Description**  
Une modification apportée à la configuration du réseau hôte a été communiquée à l’ordinateur virtuel, mais elle n’a pas pu être traitée dans l’ordinateur virtuel en raison d’une erreur. Cette erreur peut être provoquée par des données mises en forme de manière incorrecte ou par l’impossibilité de définir les informations dans l’instance CCMNetworkAdapter WMI (Windows Management Instrumentation).

<a href="" id="solution"></a>**Solution**  
Redémarrez l’hôte et l’ordinateur virtuel.

### ConfigMgr (hôte)

### ID d’événement 8006

Ordinateur virtuel introuvable.

<a href="" id="description"></a>**Description**  
Windows Virtual PC 7 ne parvient pas à trouver l’ordinateur virtuel. Il est possible que l’ordinateur virtuel ait été supprimé, déplacé, supprimé ou que l’accès ait été refusé.

<a href="" id="solution"></a>**Solution**  
Réinstallez l’ordinateur virtuel.

### ID d’événement 8008

Les informations de configuration réseau du poste de travail n’ont pas pu être récupérées.

<a href="" id="description"></a>**Description**  
Les informations de configuration du réseau n’ont pas pu être collectées à partir de l’hôte MED-V, probablement en raison d’une défaillance d’un appel système dans le .NET Framework. Ce problème peut également se produire si les informations réseau renvoyées à partir de l’hôte MED-V ne peuvent pas être écrites dans un document XML.

<a href="" id="solution"></a>**Solution**  
Redémarrez la station de travail hôte.

### ID d’événement 8010

Les données de configuration réseau n’ont pas pu être définies dans l’ordinateur virtuel.

<a href="" id="description"></a>**Description**  
La traduction d’adresses réseau (NAT) MED-V hostnetwork n’a pas pu être communiquée à l’ordinateur virtuel, car c’est probablement parce que l’ordinateur virtuel est dans un état incorrect ou qu’il n’a pas été installé ou activé.

<a href="" id="solution"></a>**Solution**  
Fermez et redémarrez l’ordinateur virtuel. Par ailleurs, il se peut que vous deviez réinstaller l’ordinateur virtuel.

### ID d’événement 8011

Échec de la réinitialisation des données de configuration du réseau dans l’ordinateur virtuel.

<a href="" id="description"></a>**Description**  
La configuration de hostnetwork MED-V (BRIDGEd) n’a pas pu être communiquée à l’ordinateur virtuel, probablement en raison du mauvais état de l’ordinateur virtuel ou des ajouts de PC Windows n’ont pas été installés ou activés.

<a href="" id="solution"></a>**Solution**  
Fermez et redémarrez l’ordinateur virtuel. Par ailleurs, il se peut que vous deviez réinstaller l’ordinateur virtuel.

### Redirection d’imprimante

### ID d’événement 9001

Erreur d’autorisation de fichier.

<a href="" id="description"></a>**Description**  
L’utilisateur final n’est pas autorisé à accéder au dossier requis pour ouvrir ou créer le fichier d’imprimante MED-V pour la lecture.

<a href="" id="solution"></a>**Solution**  
Vérifiez que le chemin d’accès User\\AppData\\ est accessible et que l’utilisateur est autorisé à lire et écrire dessus. Par exemple, si l’utilisateur est «mat», le chemin d’accès C:\\Users\\Matt\\AppData\\ et tous les fichiers doivent avoir des autorisations de lecture et d’écriture. Si tel est le cas, le chemin C:\\Users\\Matt\\AppData\\Local\\Microsoft\\MEDV\\v2\\ et tous les fichiers qu’ils contiennent doivent avoir des autorisations de lecture et d’écriture.

### ID d’événement 9002

Erreur d’autorisation de fichier.

<a href="" id="description"></a>**Description**  
L’utilisateur final n’est pas autorisé à accéder au dossier requis pour ouvrir ou créer le fichier d’imprimante MED-V à des fins de rédaction.

<a href="" id="solution"></a>**Solution**  
Assurez-vous que le chemin d’accès User\\AppData\\ est accessible et que l’utilisateur est autorisé à lire et écrire dessus. Par exemple, si l’utilisateur est «mat», le chemin d’accès C:\\Users\\Matt\\AppData\\ et tous les fichiers qu’il contient doivent avoir des autorisations de lecture et d’écriture. Si tel est le cas, le chemin C:\\Users\\Matt\\AppData\\Local\\Microsoft\\MEDV\\v2\\ et tous les fichiers qu’ils contiennent doivent avoir des autorisations de lecture et d’écriture.

### ID d’événement 9004

Impossible de créer le chemin d’accès pour le stockage des fichiers d’imprimante MEDV.

<a href="" id="description"></a>**Description**  
Le service de redirection d’imprimante n’a pas pu accéder aux fichiers ou créer des répertoires requis pour le stockage des informations d’imprimante.

<a href="" id="solution"></a>**Solution**  
Vérifiez que le chemin d’accès User\\AppData\\ est accessible et que l’utilisateur est autorisé à lire et écrire dessus. Par exemple, si l’utilisateur est «mat», le chemin d’accès C:\\Users\\Matt\\AppData\\ et tous les fichiers qu’il contient doivent avoir des autorisations de lecture et d’écriture. Si tel est le cas, le chemin C:\\Users\\Matt\\AppData\\Local\\Microsoft\\MEDV\\v2\\ et tous les fichiers qu’ils contiennent doivent avoir des autorisations de lecture et d’écriture.

### ID d’événement 9005

Impossible d’obtenir le nom de l’ordinateur virtuel de la configuration; ne peut pas lancer le programme d’installation invité. Impossible de mettre à jour MED-V: aucun réseau hôte détecté.

<a href="" id="description"></a>**Description**  
Le service de redirection d’imprimante n’a pas pu obtenir le nom de l’espace de travail MED-V à partir de la configuration MED-v et ne peut pas informer Windows Virtual PC du démarrage du programme d’installation sur l’invité MED-V.

<a href="" id="solution"></a>**Solution**  
Assurez-vous que le nom de l’espace de travail MED-V est défini et qu’il correspond à un nom de machine virtuelle dans l’annuaire de l' &lt; *utilisateur*C:\\Users\\ &gt; \\Virtual. Le nom de l’espace de travail MED-V se trouve sur HKLM\\SOFTWARE\\Microsoft\\Medv\\v2\\VM\\Name.

Par exemple, si l’utilisateur est «mat» et que le nom de l’espace de travail est «mattsworkspace», la valeur de HKLM\\SOFTWARE\\Microsoft\\Medv\\v2\\VM\\Name doit être «mattsworkspace» et il devrait y avoir un fichier nommé C:\\Users\\Matt\\Virtual Machines\\mattsworkspace.vcmx.

### Publication d’applications

### ID d’événement 10015

Une erreur de système de fichiers s’est produite lors du processus de conciliation. Le processus de rapprochement ne traitera pas le nom de fichier, &lt; *filename* &gt; mais continuera à traiter tout autre changement.

<a href="" id="description"></a>**Description**  
Un accès non autorisé ou une erreur d’e/s s’est produit lors de la création ou de la suppression d’un raccourci.

<a href="" id="solution"></a>**Solution**  
Vérifiez que le chemin d’accès du fichier est accessible et que l’utilisateur dispose des autorisations nécessaires pour créer ou supprimer le fichier spécifié.

### ID d’événement 10021

&lt; *Erreur d’erreur \ _information* &gt; pour l’opération d’opération de fichier &lt; *\ _name* &gt; sur le &lt; *nom du*fichier &gt; .

<a href="" id="description"></a>**Description**  
Un accès non autorisé ou une erreur d’e/s s’est produit lors de la création ou de la suppression d’un raccourci.

<a href="" id="solution"></a>**Solution**  
Vérifiez que le chemin d’accès du fichier est accessible et que l’utilisateur dispose des autorisations nécessaires pour créer ou supprimer le fichier spécifié.

### Correction invité

### ID d’événement 11001

Message d’utilisation des tâches de réveil d’invité.

<a href="" id="description"></a>**Description**  
MedvHost.exe l’option/GuestWakeup est exécutée de manière incorrecte ou la commande est mise en forme de manière incorrecte.

<a href="" id="solution"></a>**Solution**  
Vérifiez que la commande est exécutée avec le format suivant:

Medvhost.exe/GuestWakeup/d: &lt; *duration \ _in \ _minutes* &gt; /v: " &lt; *espace de travail \ _name* &gt; " Where

&lt;*durée \ _in \ _minutes* &gt; est le nombre de minutes pendant lesquelles l’ordinateur virtuel doit rester éveillé (la valeur par défaut est 240) et

&lt;*espace de travail \ _name* &gt; est le nom de l’ordinateur virtuel qui doit être réveillé.

### ID d’événement 11002

Impossible de mettre à jour MED-V: aucun réseau hôte détecté.

<a href="" id="description"></a>**Description**  
Le correctif invité n’a pas pu s’achever car aucune connexion réseau hôte n’a été détectée.

<a href="" id="solution"></a>**Solution**  
Connectez l’hôte MED-V à une connexion réseau active avant d’exécuter le correctif invité.

### ID d’événement 11003

Ne peut pas mettre à jour MED-V-hôte qui ne s’exécute pas sur un/C powerFailed pour créer un serveur de canaux.

<a href="" id="description"></a>**Description**  
Le correctif invité n’a pas pu s’achever, car l’hôte semble fonctionner sur batterie plutôt que sur un cordon d’alimentation.

<a href="" id="solution"></a>**Solution**  
Connectez l’ordinateur hôte à un cordon d’alimentation avant d’exécuter le correctif invité.

### EXPÉRIENCE utilisateur

### ID d’événement 14003

Le message de statut de la barre d’état suivi est trop long et n’a pas pu s’afficher: &lt; *bac \ _status \ _message*&gt;

<a href="" id="description"></a>**Description**  
MED-V a créé une chaîne inattendue qui était trop longue pour l’info-bulle de la barre d’État ou le message. Le message affiché a donc été tronqué.

<a href="" id="solution"></a>**Solution**  
Il s’agit d’une erreur rares qui peut se produire lorsque MED-V crée de manière aléatoire le texte de l’info-bulle. Il n’existe aucune solution.

### ID d’événement 14004

MED-V arrêté en raison d’une exception non gérée.

<a href="" id="description"></a>**Description**  
Une exception non gérée a entraîné l’arrêt inattendu de MED-V.

<a href="" id="solution"></a>**Solution**  
Redémarrez MED-V.

### ID d’événement 14005

Le serveur a essayé de créer un mutex, mais il existait déjà.

<a href="" id="description"></a>**Description**  
Une deuxième instance de MedvHost.exe est bloquée en mémoire.

<a href="" id="solution"></a>**Solution**  
Ouvrez TaskManager et mettez fin à tous les processus MedvHost.exe.

### ID d’événement 14006

Erreur lors de la modification ou de la suppression de la valeur du Registre &lt; *\ _Value* &gt; .

<a href="" id="description"></a>**Description**  
MED-V ne peut pas modifier l’entrée spécifiée dans le registre.

<a href="" id="solution"></a>**Solution**  
Vérifiez que vous avez installé ou désinstallé MED-V avec les informations d’identification d’administration.

### ID d’événement 14007

Le fichier spécifié ( &lt; *nom*de fichier &gt; ) n’est pas valide.

<a href="" id="description"></a>**Description**  
Lors de l’installation ou de la désinstallation, un fichier temporaire endommagé a été transmis à l’hôte MED-V.

<a href="" id="solution"></a>**Solution**  
Supprimez tous les fichiers dans le dossier Temp, puis réinstallez ou désinstallez MED-V.

### ID d’événement 14008

Fichier introuvable: nom de fichier &lt; *filename* &gt; .

<a href="" id="description"></a>**Description**  
Lors de l’installation ou de la désinstallation, le chemin d’accès d’un fichier temporaire requis est introuvable.

<a href="" id="solution"></a>**Solution**  
Supprimez tous les fichiers dans le dossier Temp, puis réinstallez ou désinstallez MED-V.

### ID d’événement 14009

Impossible de lire le fichier de paramètres &lt; *nom_fichier* &gt; .

<a href="" id="description"></a>**Description**  
Pendant le processus d’installation ou de désinstallation, MED-V n’a pas pu lire un fichier temporaire.

<a href="" id="solution"></a>**Solution**  
Supprimez tous les fichiers dans le dossier Temp, puis réinstallez ou désinstallez MED-V. Par ailleurs, vérifiez que l’utilisateur dispose des droits et autorisations nécessaires sur le dossier Temp.

### ID d’événement 14010

Erreur de fichier de paramètre de désérialisation &lt; *filename* &gt; .

<a href="" id="description"></a>**Description**  
Pendant le processus d’installation ou de désinstallation, MED-V a détecté un fichier temporaire endommagé.

<a href="" id="solution"></a>**Solution**  
Supprimez tous les fichiers dans le dossier Temp, puis réinstallez ou désinstallez MED-V. Par ailleurs, vérifiez que l’utilisateur dispose des droits et autorisations nécessaires sur le dossier Temp.

### ID d’événement 14011

Erreur inattendue lors de la désérialisation &lt; *du nom*de fichier du paramètre &gt; .

<a href="" id="description"></a>**Description**  
Pendant le processus d’installation ou de désinstallation, MED-V a détecté un fichier temporaire endommagé.

<a href="" id="solution"></a>**Solution**  
Supprimez tous les fichiers dans le dossier Temp, puis réinstallez ou désinstallez MED-V. Par ailleurs, vérifiez que l’utilisateur dispose des droits et autorisations nécessaires sur le dossier Temp.

### ID d’événement 14012

Erreur inattendue lors de l’utilisation des droits de paramètres sur le &lt; *dossier de dossiers \ _name* &gt; pour &lt; *nom d'* utilisateur &gt; .

<a href="" id="description"></a>**Description**  
Une erreur se produit lorsque MED-V est incapable de définir des droits et des autorisations sur certains dossiers lors de l’installation.

<a href="" id="solution"></a>**Solution**  
Activez les droits d’administrateur pour les dossiers suivants:

@"%ProgramData%\\Microsoft\\Medv\\AllUsers"

@"%ProgramData%\\Microsoft\\Medv\\MedvLock"

@"%ProgramData%\\Microsoft\\Medv\\Monitoring"

### ID d’événement 14013

Erreur inattendue lors de la création d’un fichier verrouillé.

<a href="" id="description"></a>**Description**  
Une erreur se produit lorsque MED-V ne peut pas créer de fichier dans le dossier @ «%ProgramData%\\Microsoft\\Medv\\MedvLock» lors de l’installation.

<a href="" id="solution"></a>**Solution**  
Vérifiez les droits d’administrateur pour le dossier MedvLock.

## Rubriques connexes


[Résolution des problèmes liés à MED-V](troubleshooting-med-vmedv2.md)

 

 





