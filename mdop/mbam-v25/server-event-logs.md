---
title: Journaux des événements serveur
description: Journaux des événements serveur
author: dansimp
ms.assetid: 04e724d2-28cc-4fa8-86a1-0d4ab0234b11
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 269e9b4bc2644fae4dc5796652c7587bb0ef6076
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809923"
---
# Journaux des événements serveur


Les tableaux de cette section fournissent des informations sur les ID d’événement du journal de MBAM Server.

## Configuration


Le tableau suivant contient des messages et des informations de dépannage pour les ID d’événement qui peuvent se produire sur le serveur MBAM lors de la configuration.

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
<th align="left">ID d’événement</th>
<th align="left">Source</th>
<th align="left">Symbole d’événement</th>
<th align="left">Message</th>
<th align="left">Résolution des problèmes</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>103</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/opérationnel</p></td>
<td align="left"><p>VssRegistrationException</p></td>
<td align="left"><p>Une exception s’est produite lors de l’inscription à VSS.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>104</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/opérationnel</p></td>
<td align="left"><p>VssDeregistrationException</p></td>
<td align="left"><p>Une exception s’est produite lors de la suppression de l’enregistrement VSS.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>300</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/Admin</p></td>
<td align="left"><p>CmdletError</p></td>
<td align="left"><p>Échec de la suppression du dossier.</p></td>
<td align="left"><p>Indique qu’une erreur de fin s’est produite lors de l’exécution d’une tâche. Examinez d’autres messages d’événement dans le journal pour diagnostiquer davantage le MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>301</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/Admin</p></td>
<td align="left"><p>cmdletUnexpectedError</p></td>
<td align="left"><p>Erreur d’applet de passe inattendue.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>302</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/Admin</p></td>
<td align="left"><p>CmdletWarning</p></td>
<td align="left"><p>Avertissement sur l’applet de applet.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>303</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/opérationnel</p></td>
<td align="left"><p>CmdletInformation</p></td>
<td align="left"><p>Informations sur l’applet de passe.</p></td>
<td align="left"><p>Information uniquement; aucun dépannage n’est requis. L’événement indique qu’une tâche est en cours de réalisation par les applets de commande, par exemple enabling\disabling une fonctionnalité ou en annulant une opération.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>400</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/Admin</p></td>
<td align="left"><p>ConfiguratorError</p></td>
<td align="left"><p>Erreur du configurateur.</p></td>
<td align="left"><p>Indique qu’une erreur s’est produite lors du lancement de MBAM Configurator. Assurez-vous que l’utilisateur dispose des droits appropriés pour lancer le configurateur MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>401</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/Admin</p></td>
<td align="left"><p>ConfiguratorUnexpectedError</p></td>
<td align="left"><p>Erreur de Configurateur inattendue.</p></td>
<td align="left"><p>Indique qu’une erreur de terminaison s’est produite lors de l’exécution d’une tâche Configurator du configurateur MBAM. Le message d’erreur contient plus d’informations sur l’erreur. Examinez d’autres messages d’erreur dans le journal des événements pour diagnostiquer davantage le problème de configuration de MBAM. Les erreurs connues sont les suivantes:</p>
<ul>
<li><p>Impossible de récupérer ou de valider un certificat sélectionné par l’utilisateur</p></li>
<li><p>Échec de l’analyse de l’URL du rapport</p></li>
<li><p>Impossible d’ouvrir les journaux d’événements pour l’utilisateur</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>402</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/Admin</p></td>
<td align="left"><p>ConfiguratorWarning</p></td>
<td align="left"><p>Avertissement du configurateur.</p></td>
<td align="left"><p>Indique qu’une tâche de Configurateur MBAM ne se termine pas comme prévu, mais qu’elle n’a pas été complètement en échec. Les tâches connues incluent un certificat manquant dans le LocalMachine\My Store configuré dans la fonctionnalité de l’application Web, ou un délai d’expiration pour une tâche en attente.</p></td>
</tr>
<tr class="even">
<td align="left"><p>410</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/opérationnel</p></td>
<td align="left"><p>ConfiguratorInformation</p></td>
<td align="left"><p>Informations de configurateur.</p></td>
<td align="left"><p>Information uniquement; aucun dépannage n’est requis. L’événement indique qu’une tâche est appelée par le configurateur MBAM. Les tâches connues sont les suivantes:</p>
<ul>
<li><p>Lancement du Configurateur</p></li>
<li><p>Vérification de la configuration logicielle requise pour une fonctionnalité MBAM</p></li>
<li><p>Validation de paramètres pour une fonctionnalité de MBAM</p></li>
<li><p>Enabling\disabling\committing une fonctionnalité MBAM</p></li>
<li><p>Génération d’un script PowerShell à partir du Configurateur</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>500</p></td>
<td align="left"><p>Microsoft_Windows_MBAM_Server_Admin</p></td>
<td align="left"><p>WebProviderUnexpectedError</p></td>
<td align="left"><p>Erreur inattendu du fournisseur d’applications Web.</p></td>
<td align="left"><p>Indique qu’une erreur s’est produite lors de l’activation et de la configuration d’un site Web ou d’un service Web MBAM dans IIS. Les erreurs connues sont les suivantes:</p>
<ul>
<li><p>Échec de la recherche du dossier racine WWW d’IIS</p></li>
<li><p>Échec de l’accès à la configuration IIS dans le web.config en raison de fichiers mal formés ou de paramètres manquants</p></li>
<li><p>Échec de la création ou de la suppression d’une application Web</p></li>
<li><p>Violation d’accès IIS</p></li>
</ul>
<p>Cette erreur est également enregistrée si MBAM ne peut pas accéder à Active Directory (AD) pour valider les comptes d’utilisateurs. Vérifiez que les services IIS sont installés, configurés correctement et que le service IIS est en cours d’exécution. Vérifiez que tous les tests prérequis par le logiciel MBAM réussissent. Vérifiez que l’utilisateur dispose des autorisations appropriées pour créer des applications Web sur l’instance IIS. Vérifiez que l’utilisateur a accès aux objets de compte d’utilisateur lus dans AD.</p></td>
</tr>
<tr class="even">
<td align="left"><p>501</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/Admin</p></td>
<td align="left"><p>WebProviderError</p></td>
<td align="left"><p>Erreur inattendu du fournisseur d’applications Web.</p></td>
<td align="left"><p>Indique qu’une erreur s’est produite pendant l’activation, la désactivation ou la configuration d’un site Web ou d’un service Web MBAM dans IIS. Les erreurs connues sont les suivantes:</p>
<ul>
<li><p>Impossible de lire les informations de liaison de base ou WSHttp à partir d’IIS</p></li>
<li><p>Section Identity manquante ou entrée DNS dans la section Identity des fichiers de configuration IIS</p></li>
<li><p>Impossible d’ouvrir la clé de Registre HKLM\SOFTWARE\Microsoft\InetStp</p></li>
<li><p>Impossible de lire la valeur PathWWWRoot à partir de la clé de Registre HKLM\SOFTWARE\Microsoft\InetStp</p></li>
<li><p>Un utilisateur tente de spécifier un nom de répertoire virtuel avec un nom réservé pour MBAM</p></li>
</ul>
<p>Vérifiez que les services Internet sont installés et correctement configurés. Vérifiez que la clé de Registre HKLM\SOFTWARE\Microsoft\InetStp: PathWWWRoot existe et qu’elle est accessible. Vérifiez que les informations de liaison dans IIS ne sont pas corrompues.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>502</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/Admin</p></td>
<td align="left"><p>WebProviderWarning</p></td>
<td align="left"><p>Avertissement du fournisseur d’applications Web.</p></td>
<td align="left"><p>Indique qu’une erreur sans fin s’est produite lors de l’activation d’un site Web ou d’un service Web MBAM. Les erreurs connues sont les suivantes:</p>
<ul>
<li><p>Impossible d’accéder à AD pour valider le nom de principal de service (SPN) sur le compte du pool d’applications</p></li>
<li><p>Échec de la validation du SPN car il est affecté à plusieurs comptes dans AD</p></li>
<li><p>Échec de l’inscription d’un SPN sur le compte du pool d’applications dans AD</p></li>
<li><p>Le SPN est enregistré sur un compte différent du pool d’applications dans AD</p></li>
<li><p>Échec de la suppression du SPN du compte du pool d’applications dans AD lors d’une opération de restauration.</p></li>
<li><p>L’impossibilité de vérifier si le groupe de IIS_IUSRS a reçu le privilège connexion en tant que lot sur le serveur IIS</p></li>
</ul>
<p>Le message d’événement contient plus d’informations sur l’erreur spécifique. Vérifiez que la publicité est accessible à partir du serveur sur lequel MBAM est en cours d’exécution. Vérifiez que l’utilisateur qui exécute le programme d’installation MBAM possède des autorisations de lecture sur le compte du pool d’applications dans AD. Si un SPN est déjà enregistré sur le compte du pool d’applications dans AD, assurez-vous qu’il n’est pas enregistré sur d’autres comptes.</p></td>
</tr>
<tr class="even">
<td align="left"><p>503</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/opérationnel</p></td>
<td align="left"><p>WebProviderInformation</p></td>
<td align="left"><p>Informations relatives aux fournisseurs d’applications Web. Description</p></td>
<td align="left"><p>Information uniquement; aucun dépannage n’est requis. L’événement indique qu’une tâche est appelée par la configuration MBAM. Les tâches connues incluent la configuration IIS, telle que les informations de liaison et le site racine, et la configuration du nom de principal de service (SPN).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>600</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/Admin</p></td>
<td align="left"><p>SetupUnexpectedError</p></td>
<td align="left"><p>Erreur d’installation inattendue.</p></td>
<td align="left"><p>Indique qu’une erreur de fin s’est produite lors de la enabling\disabling ou de la configuration d’une fonctionnalité MBAM. Les erreurs connues sont les suivantes:</p>
<ul>
<li><p>Échec de l’annulation d’une tâche après une erreur</p></li>
<li><p>Échec de la lecture à partir du Registre</p></li>
<li><p>Échec de la création ou de la suppression d’un dossier dans le système de fichiers</p></li>
<li><p>Impossible de lire les informations de la version SQL</p></li>
<li><p>Impossible d’inscrire VSS Writer dans SQL</p></li>
</ul>
<p>Le message d’événement contient plus d’informations sur l’erreur spécifique. Vérifiez que tous les tests prérequis par le logiciel MBAM réussissent. Vérifiez que le chemin d’accès du Registre MBAM, le cas échéant, HKEY_LOCAL_MACHINE \SOFTWARE\Microsoft\MBAM Server et toutes les sous-clés sont lisibles. Vérifiez que la publicité est accessible à partir du serveur sur lequel MBAM est en cours d’exécution. Vérifiez que l’utilisateur qui exécute le programme d’installation MBAM possède des autorisations de lecture dans AD.</p>
<p>Pour une inscription réussie du writer VSS, vérifiez qu’une version prise en charge de SQL est installée et qu’une instance est accessible à l’utilisateur qui exécute la configuration MBAM. Si la désactivation d’une fonction MBAM ou la désinstallation de MBAM Vérifiez que tous les fichiers, tels que les fichiers journaux et les fichiers web.config sont fermés, de sorte que MBAM puisse supprimer ses sites Web et services Web.</p></td>
</tr>
<tr class="even">
<td align="left"><p>601</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/Admin</p></td>
<td align="left"><p>SetupError</p></td>
<td align="left"><p>Erreur d’installation.</p></td>
<td align="left"><p>Indique qu’une erreur de fin s’est produite lors de la enabling\disabling ou de la configuration d’une fonctionnalité MBAM. Les erreurs connues sont les suivantes:</p>
<ul>
<li><p>Échec de la lecture de la configuration de MBAM dans IIS</p></li>
<li><p>Section appSettings endommagée dans la configuration IIS ou paramètres incorrectement configurés</p></li>
<li><p>Échec de la validation du nom d’hôte</p></li>
<li><p>Impossible de lire les informations de la version SQL</p></li>
<li><p>Impossible d’inscrire VSS Writer dans SQL</p></li>
</ul>
<p>Le message d’événement contient plus d’informations sur l’erreur spécifique. Vérifiez que les services Internet sont installés et configurés correctement. Vérifiez que tous les tests prérequis par le logiciel MBAM réussissent. Pour une inscription réussie du writer VSS, vérifiez qu’une version prise en charge de SQL est installée et qu’une instance est accessible à l’utilisateur qui exécute la configuration MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>602</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/Admin</p></td>
<td align="left"><p>SetupWarning</p></td>
<td align="left"><p>Avertissement de configuration</p></td>
<td align="left"><p>Indique qu’une erreur de non-terminaison s’est produite pendant enabling\disabling ou la configuration d’une fonctionnalité MBAM telle que l’intégration de Configuration Manager (CM) ou l’application Web MBAM. Les erreurs connues incluent: échec de la suppression des rapports MBAM à partir du point de rôle SRS au centimètre et de l’échec de la résolution d’un nom d’hôte à partir du contrôleur de domaine. Le message d’événement contient plus d’informations sur l’erreur spécifique.</p>
<p>Vérifiez que la publicité est accessible à partir du serveur sur lequel MBAM est en cours d’exécution. Vérifiez que l’utilisateur qui exécute le programme d’installation MBAM possède des autorisations de suppression sur l’instance SSRS configurée comme point de rôle de SRS en CENTIMÈTREs.</p></td>
</tr>
<tr class="even">
<td align="left"><p>603</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/opérationnel</p></td>
<td align="left"><p>SetupInformation</p></td>
<td align="left"><p>Informations de configuration.</p></td>
<td align="left"><p>Information uniquement; aucun dépannage n’est requis.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>605</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/Admin</p></td>
<td align="left"><p>WebProviderSoftwareCheckFailure</p></td>
<td align="left"><p>L’application Web ne peut pas être activée car une ou plusieurs dépendances logicielles ne sont pas satisfaites.</p></td>
<td align="left"><p>Lors de l’installation d’un site Web ou d’un service Web MBAM, le programme d’installation de MBAM vérifie si les conditions requises sont en place. Ce message indique que MBAM n’a pas réussi à installer le site Web/service Web demandé, car la configuration requise requise est manquante. Pour plus d’informations sur les conditions préalables manquantes, voir messages d’erreur précédant ce message.</p></td>
</tr>
<tr class="even">
<td align="left"><p>606</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/Admin</p></td>
<td align="left"><p>SetupParameterValidationFailure</p></td>
<td align="left"><p>Le paramètre requis pour activer la fonctionnalité serveur n’a pas été spécifié ou n’a pas réussi la validation.</p></td>
<td align="left"><p>Indique que le paramètre requis pour configurer une fonctionnalité MBAM n’a pas été spécifié ou qu’elle n’a pas réussi la validation.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>607</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/Admin</p></td>
<td align="left"><p>SetupParameterValidationFailureWithError</p></td>
<td align="left"><p>Erreur rencontrée lors de la tentative de validation du paramètre spécifié requis pour activer la fonctionnalité de serveur.</p></td>
<td align="left"><p>Indique qu’une erreur s’est produite lors d’une tentative de validation du paramètre spécifié requis pour activer la fonctionnalité du serveur.</p></td>
</tr>
<tr class="even">
<td align="left"><p>700</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/Admin</p></td>
<td align="left"><p>DbProviderUnexpectedError</p></td>
<td align="left"><p>Erreur inattendu du fournisseur de BDD.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>701</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/Admin</p></td>
<td align="left"><p>DbProviderError</p></td>
<td align="left"><p>Erreur du fournisseur de BDD.</p></td>
<td align="left"><p>Le message contenu dans la section EventDetails doit fournir plus d’informations sur l’erreur réelle. Voici quelques points à vérifier:</p>
<ul>
<li><p>MBAM échec de la connexion à la base de données à l’aide des informations de connexion fournies. Vérifiez les informations de la chaîne de connexion fournies à la configuration de MBAM.</p></li>
<li><p>MBAM le programme d’installation n’a pas pu se connecter à la base de données fournie en utilisant les informations d’identification du compte de domaine fournies. Vérifiez que le nom d’utilisateur et le mot de passe du compte de domaine sont valides.</p></li>
<li><p>MBAM le programme d’installation n’a pas pu se connecter à la base de données fournie en utilisant les informations d’identification du compte de domaine fournies. Vérifiez que le compte de domaine fourni dispose des autorisations nécessaires pour vous connecter à la base de données MBAM.</p></li>
<li><p>Le PAC de MBAM ne fonctionnera pas si une nouvelle version de la base de données MBAM est déjà installée. Vérifiez qu’une nouvelle version de MBAM DBs n’existe pas sur le serveur SQL Server indiqué.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>702</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/Admin</p></td>
<td align="left"><p>DbProviderWarning</p></td>
<td align="left"><p>Avertissement du fournisseur de BDD.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>703</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/opérationnel</p></td>
<td align="left"><p>DbProviderInformation</p></td>
<td align="left"><p>Informations du fournisseur de base de données</p></td>
<td align="left"><p>Information uniquement; aucun dépannage n’est requis.</p></td>
</tr>
<tr class="even">
<td align="left"><p>704</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/Admin</p></td>
<td align="left"><p>DbProviderDacError</p></td>
<td align="left"><p>Une erreur s’est produite lors du déploiement de l’application de couche de données.</p></td>
<td align="left"><p>MBAM packages ses bases de données en tant qu’applications de couche données et tente de les inscrire à l’aide de Microsoft. SqlServer. DAC. DacServices. Le message d’erreur en contexte est signalé par le service DAC. L’événement doit contenir des informations détaillées sur ce qui l’a causé. Lisez les informations du message d’erreur pour résoudre le problème.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>705</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/Admin</p></td>
<td align="left"><p>DbProviderDacWarning</p></td>
<td align="left"><p>Un avertissement s’est produit lors du déploiement de l’application de couche de données.</p></td>
<td align="left"><p>MBAM compresse ses bases de données en tant qu’application de niveau de données et tente de les inscrire à l’aide de Microsoft. SqlServer. DAC. DacServices. Le message d’avertissement de contexte est signalé par le service DAC. L’événement doit contenir des informations détaillées sur ce qui l’a causé. Lisez les informations figurant dans le message d’avertissement pour résoudre le problème.</p></td>
</tr>
<tr class="even">
<td align="left"><p>706</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/opérationnel</p></td>
<td align="left"><p>DbProviderDacInformation</p></td>
<td align="left"><p>Un message a été déclenché lors du déploiement de l’application de couche de données.</p></td>
<td align="left"><p>Information uniquement; aucun dépannage n’est requis.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>800</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/Admin</p></td>
<td align="left"><p>ReportProviderUnexpectedError</p></td>
<td align="left"><p>Erreur inattendue du fournisseur de rapports.</p></td>
<td align="left"><p>Erreur inattendue du fournisseur de rapports. Description {exceptionDetails} Voici quelques-uns des détails sur les exceptions possibles:</p>
<p><strong>Une erreur s’est produite lors de l’affichage du nom de l’annuaire &#39; {directoryName} &#39;</strong></p>
<p><strong>Une exception s’est produite lors de la réception de fichiers pour l’annuaire &#39; {directoryName} &#39;</strong></p>
<p><strong>Une exception s’est produite lors de l’énumération des répertoires dans l’annuaire &#39; {directoryName} &#39;</strong></p>
<p><strong>Une exception s’est produite lors de la lecture de tous les octets pour le fichier &#39; {fileName} &#39;</strong></p>
<p>Lors de l’installation d’MBAM, MBAM Setup décompresse tous les fichiers de rapport dans le chemin d’installation spécifié. Dans le cadre de l’installation de rapport, le module d’installation tente d’accéder aux fichiers de rapport décompressés sur le chemin d’installation et communique avec les services de rapport SQL pour publier les fichiers de rapport. Les erreurs ci-dessus se produisent lorsque MBAM ne peut pas accéder aux fichiers/dossiers dans le chemin d’installation décompressé. Voici quelques conseils pour résoudre ce problème:</p>
<ul>
<li><p>Vérifiez que MBAM est installé.</p></li>
<li><p>Vérifiez que RegKey HKEY_LOCAL_MACHINE \SOFTWARE\Microsoft\MBAM Server\InstallationPath est présent et accessible à l’utilisateur exécutant.</p></li>
<li><p>Vérifiez que le chemin d’accès aux fichiers sous MBAM InstallationPath ne dépasse pas 248 caractères.</p></li>
<li><p>Vérifiez que le dossier d’installation d’MBAM ou les fichiers contenus dans MBAM Path installation ne sont pas modifiés depuis l’installation.</p></li>
<li><p>Vérifiez que l’utilisateur qui exécute le programme d’installation est autorisé à lire dans le dossier d’installation MBAM.</p></li>
</ul>
<p><strong>Échec de la connectivité Reporting Services. {exceptionDetails}</strong></p>
<p>Lors de l’installation de rapports MBAM, les modules essaient de communiquer avec des services Web SSRS pour créer des dossiers et publier des rapports. Le message ci-dessus indique que MBAM n’a pas pu détecter ou communiquer avec des services Web SSRS. Voici quelques conseils pour résoudre ce problème:</p>
<ul>
<li><p>Vérifiez que le SSRS est installé sur l’ordinateur spécifié.</p></li>
<li><p>L’utilisation de la console SSRS vérifie que le SSRS est activé et en cours d’exécution.</p></li>
<li><p>Vérifiez que l’utilisateur qui exécute le programme d’installation est autorisé à accéder à SSRS.</p></li>
</ul>
<p><strong>Échec de la suppression des rapports MBAM à l’aide de l’URL d’instance Reporting Services &#39; {SSRSInstanceUrl} &#39;. Assurez-vous que l’instance SSRS requise pour les rapports MBAM est en cours d’exécution et configurée correctement.</strong></p>
<p>Lorsque l’installation d’MBAM échoue ou lorsque l’utilisateur désactive les fonctionnalités de création de rapports MBAM, le module d’installation supprime les rapports SSRS Le message ci-dessus indique que MBAM n’a pas réussi à supprimer des rapports SSRS. Voici quelques conseils pour résoudre ce problème:</p>
<ul>
<li><p>Vérifiez que le SSRS est installé sur l’ordinateur spécifié.</p></li>
<li><p>L’utilisation de la console SSRS vérifie que le SSRS est activé et en cours d’exécution.</p></li>
<li><p>Vérifiez que l’utilisateur qui exécute le programme d’installation est autorisé à accéder à SSRS.</p></li>
</ul>
<p><strong>Une erreur s’est produite lors de la publication de rapports. {exceptionDetails}.</strong></p>
<p>Lors de l’installation de rapports MBAM, les modules essaient de communiquer avec des services Web SSRS pour créer des dossiers et publier des rapports. Le message ci-dessus indique que le service Web SSRS a été signalé et qu’il n’est pas en cours de publication. Voici quelques conseils pour résoudre ce problème:</p>
<ul>
<li><p>L’utilisation de la console SSRS vérifie que le SSRS est activé et en cours d’exécution.</p></li>
<li><p>Vérifiez que l’utilisateur qui exécute le programme d’installation est autorisé à accéder/publier des rapports sur SSRS.</p></li>
</ul>
<p><strong>Une stratégie pour le nom d’utilisateur de groupe &#39; {userName} &#39; existe déjà. Si ce n’est pas le cas, révisez manuellement le service de création de rapports pour les stratégies en double ou non valides.</strong></p>
<p>Après la publication de rapports MBAM, MBAM programme d’installation tente de créer des rôles utilisateurs de rapport MBAM (s’il n’existe pas déjà) et définit la stratégie d’utilisateur correspondante. L’erreur ci-dessus indique que le service Web SSRS a levé une exception lors de la configuration de la stratégie de rôle utilisateur du rapport. Suivez les instructions du message d’événement et reportez-vous à la rubrique &quot; <a href="https://www.microsoft.com/technet/support/ee/transform.aspx?ProdName=SQL+Server+Reporting+Services&amp;ProdVer=8.00&amp;EvtID=rsInvalidPolicyDefinition&amp;EvtSrc=Microsoft.ReportingServices.Diagnostics.ErrorStrings.resources.Strings&amp;LCID=1033&amp;quot" data-raw-source="https://www.microsoft.com/technet/support/ee/transform.aspx?ProdName=SQL+Server+Reporting+Services&amp;amp;ProdVer=8.00&amp;amp;EvtID=rsInvalidPolicyDefinition&amp;amp;EvtSrc=Microsoft.ReportingServices.Diagnostics.ErrorStrings.resources.Strings&amp;amp;LCID=1033&amp;quot"> https://www.microsoft.com/technet/support/ee/transform.aspx?ProdName=SQL+Server+Reporting+Services&amp . ProdVer = &amp; EvtID = rsInvalidPolicyDefinition &amp; EvtSrc = Microsoft. ReportingServices. Diagnostics. ErrorStrings. resources. Strings &amp; LCID = 1033&quote </a> ; pour obtenir de l’aide.</p>
<p><strong>Une erreur s’est produite lors de la validation de l’accès à SSRS {exceptionDetails}.</strong></p>
<p>Dans le cadre de la vérification de la configuration requise, le programme d’installation de MBAM vérifie que l’utilisateur dispose des autorisations nécessaires pour accéder à un dossier ou le créer sous SSRS. Le message d’erreur indique qu’une exception s’est produite lors de la vérification de l’accès à SSRS. Référez-vous aux détails de l’exception pour obtenir des conseils de débogage.</p>
<p><strong>Une erreur SOAP s’est produite lors de la vérification de l’URL SSRS. {exceptionDetails}</strong></p>
<p><strong>Une erreur Web s’est produite lors de la vérification de l’URL SSRS. {exceptionDetails}</strong></p>
<p><strong>Une erreur HTTP/HTTPS s’est produite lors de la vérification de l’URL SSRS. {exceptionDetails}</strong></p>
<p><strong>Une erreur s’est produite lors de la vérification de l’URL SSRS. {exceptionDetails}</strong></p>
<p>Dans le cadre de la vérification de la configuration requise, le programme d’installation de MBAM récupère les URL associées à l’instance SSRS fournie et tente de communiquer avec le service Web SSRS. Le message d’erreur ci-dessus indique que le service Web SSRS sur l’URL donnée a levé une exception, reportez-vous à la rubrique Détails de l’exception pour plus d’informations. Voici quelques conseils pour résoudre les problèmes de communication SSRS.</p>
<ul>
<li><p>Vérifiez que le SSRS est installé sur l’ordinateur spécifié.</p></li>
<li><p>L’utilisation de la console SSRS vérifie que le SSRS est activé et en cours d’exécution.</p></li>
<li><p>Vérifiez que l’utilisateur qui exécute le programme d’installation est autorisé à accéder à SSRS.</p></li>
</ul>
<p><strong>Une erreur s’est produite lors de la récupération de la version SSRS. {exceptionDetails}</strong></p>
<p>Dans le cadre de la vérification de la configuration requise, le programme d’installation d’MBAM interroge WMI pour récupérer le numéro de version associé à l’instance SSRS fournie. Le message d’erreur ci-dessus indique qu’une exception s’est produite lors de l’interrogation de WMI. Pour plus d’informations, consultez exceptionDetails. Voici quelques tests que vous pouvez effectuer:</p>
<ul>
<li><p>Vérifiez que le SSRS avec nom d’instance donné est installé sur l’ordinateur spécifié.</p></li>
<li><p>L’utilisation de la console SSRS vérifie que le SSRS est activé et en cours d’exécution.</p></li>
<li><p>Vérifiez que l’utilisateur qui exécute le programme d’installation est autorisé à interroger la classe SSRS sous l’espace de noms WMI.</p></li>
</ul>
<p><strong>L’utilisateur actuel n’est pas autorisé à accéder à l’espace de noms WMI &#39; {ssrsWMINamespace} &#39;.</strong></p>
<p><strong>Une erreur s’est produite lors de l’énumération de l’espace de noms &#39; {ssrsWMINamespace} &#39;. Le serveur RPC pour le fournisseur WMI SSRS sur l’hôte local est introuvable.</strong></p>
<p><strong>Une erreur s’est produite lors de l’énumération de l’espace de noms &#39; {ssrsNamespace} &#39;. Impossible de trouver une instance de SSRS sur l’hôte local.</strong></p>
<p><strong>Une erreur s’est produite lors de l’accès à WMI. Le serveur RPC de l’instance &#39; {ssrsInstance} &#39; est introuvable.</strong></p>
<p><strong>Une erreur s’est produite lors de l’accès à WMI. Le nom de l’instance &#39; {ssrsInstanceName} &#39; n’est pas correct.</strong></p>
<p><strong>Une erreur s’est produite lors de l’accès à WMI. Impossible de trouver l’instance &#39; {ssrsInstanceName} &#39; sur l’hôte local.</strong></p>
<p>Dans le cadre de la vérification de la configuration requise, le programme d’installation d’MBAM interroge WMI pour récupérer l’espace de noms WMI associé à l’instance fournie. Le message d’erreur ci-dessus indique qu’une exception s’est produite lors de l’interrogation de WMI. Pour plus d’informations, consultez exceptionDetails. Voici quelques tests que vous pouvez effectuer:</p>
<ul>
<li><p>Vérifiez que le SSRS avec nom d’instance donné est installé sur l’ordinateur spécifié.</p></li>
<li><p>L’utilisation de la console SSRS vérifie que le SSRS est activé et en cours d’exécution.</p></li>
<li><p>Vérifiez que l’utilisateur qui exécute le programme d’installation est autorisé à accéder/à la classe SSRS en utilisant l’espace de noms WMI.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>801</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/Admin</p></td>
<td align="left"><p>ReportProviderError</p></td>
<td align="left"><p>Erreur inattendue du fournisseur de rapports.</p></td>
<td align="left"><p>En fonction du nom de l’instance SQL Server Reporting Services, MBAM tente de trouver l’espace de noms WMI correspondant à l’instance de création de rapports et de s’y connecter. Cette erreur se produit si MBAM rencontre une exception lorsque MBAM recherche ou essaie de se connecter à l’espace de noms de l’infrastructure WMI SSRS. Pour plus d’informations, lisez les informations contenues dans les messages d’erreur enregistrés dans le canal de configuration de MBAM. Voici quelques conseils que vous pouvez consulter:</p>
<ul>
<li><p>Vérifier que le SSRS avec le nom d’instance fourni est opérationnel</p></li>
<li><p>Vérifiez que le compte d’utilisateur exécutant l’installation de MBAM dispose des autorisations nécessaires pour interroger/se connecter à l’espace de noms WMI SSRS.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>802</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/Admin</p></td>
<td align="left"><p>ReportProviderWarning</p></td>
<td align="left"><p>Avertissement du fournisseur de rapports.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>803</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/opérationnel</p></td>
<td align="left"><p>ReportProviderInformation</p></td>
<td align="left"><p>Rapporter les informations sur le fournisseur.</p></td>
<td align="left"><p>Information uniquement; aucun dépannage n’est requis.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>900</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/Admin</p></td>
<td align="left"><p>CMProviderUnexpectedError</p></td>
<td align="left"><p>Erreur inattendu du fournisseur de CM.</p></td>
<td align="left"><p>Indique qu’une erreur de fin s’est produite lors de la enabling\disabling ou de la configuration de la fonctionnalité d’intégration de Configuration Manager (CM) dans MBAM. Les erreurs connues sont les suivantes:</p>
<ul>
<li><p>Échec de la connexion au serveur de site CM par le biais du fournisseur de SMS</p></li>
<li><p>Échec de la lecture à partir du Registre</p></li>
<li><p>Échec de la création ou de la suppression d’un dossier dans le système de fichiers</p></li>
<li><p>Échec de la localisation de l’installation de la console Configuration Manager sur l’ordinateur local</p></li>
<li><p>Impossible d’extraire des informations pour l’instance SSRS configurée comme point de rôle de SRS en CENTIMÈTREs</p></li>
</ul>
<p>Le message d’événement contient plus d’informations sur l’erreur spécifique. Vérifiez que tous les tests prérequis par le logiciel MBAM réussissent. Vérifiez que le chemin d’accès du Registre MBAM, le cas échéant, HKEY_LOCAL_MACHINE \SOFTWARE\Microsoft\MBAM Server et toutes les sous-clés sont lisibles. Vérifiez que MBAM est intégré à une version prise en charge de Configuration Manager. Vérifiez que la console Configuration Manager est installée sur l’ordinateur sur lequel est appelée la configuration de MBAM et que la console peut être utilisée pour se connecter au serveur de site cible. Vérifiez qu’une instance de SSRS valide est configurée en tant que point de rôle de SRS en CENTIMÈTREs et que l’utilisateur qui exécute l’installation MBAM dispose d’autorisations read\write sur l’instance SSRS.</p></td>
</tr>
<tr class="even">
<td align="left"><p>901</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/Admin</p></td>
<td align="left"><p>CMProviderError</p></td>
<td align="left"><p>Erreur inattendu du fournisseur de CM.</p></td>
<td align="left"><p>Indique qu’une erreur de fin s’est produite lors de la enabling\disabling ou de la configuration de la fonctionnalité d’intégration de Configuration Manager (CM) dans MBAM. Les erreurs connues sont les suivantes:</p>
<ul>
<li><p>échec de la connexion au serveur de site CM par le biais du fournisseur de SMS</p></li>
<li><p>échec de la lecture à partir du Registre</p></li>
<li><p>échec de la création ou de la suppression d’un dossier dans le système de fichiers</p></li>
<li><p>échec de la localisation de l’installation de la console Configuration Manager sur l’ordinateur local</p></li>
<li><p>dossier ConfigMgr manquant dans SSRS en tant que dossier racine pour les rapports de points de rôle de SRS</p></li>
<li><p>source de données partagée ConfigMgr manquante dans SSRS</p></li>
<li><p>échec du déploiement des rapports SSRS dans l’instance SSRS configurée comme point de rôle de SRS en CENTIMÈTREs</p></li>
<li><p>échec de la création des éléments de configuration et des points de comparaison en CENTIMÈTREs</p></li>
</ul>
<p>Le message d’événement contient plus d’informations sur l’erreur spécifique. Vérifiez que tous les tests prérequis par le logiciel MBAM réussissent. Vérifiez que le chemin d’accès du Registre MBAM, le cas échéant, HKEY_LOCAL_MACHINE \SOFTWARE\Microsoft\MBAM Server et toutes les sous-clés sont lisibles. Vérifiez que MBAM est intégré à une version prise en charge de Configuration Manager. Vérifiez que la console Configuration Manager est installée sur l’ordinateur sur lequel est appelée la configuration de MBAM et que la console peut être utilisée pour se connecter au serveur de site cible. Vérifiez que l’utilisateur dispose des autorisations read\write requises pour créer des éléments de configuration, des points de comparaison et des collections en CENTIMÈTREs. Vérifiez qu’une instance de SSRS valide est configurée en tant que point de rôle de SRS en CENTIMÈTREs et que l’utilisateur qui exécute l’installation MBAM dispose d’autorisations read\write sur l’instance SSRS.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>902</p></td>
<td align="left"><p>Microsoft_Windows_MBAM_Server_Admin</p></td>
<td align="left"><p>CMProviderWarning</p></td>
<td align="left"><p>Avertissement du fournisseur CM.</p></td>
<td align="left"><p>Indique qu’une erreur sans fin s’est produite lors de l’activation de la fonctionnalité d’intégration de Configuration Manager (CM). Les erreurs connues sont les suivantes: échec de la validation des règles de collection dans la collection d’ordinateurs pris en charge par MBAM, en CENTIMÈTREs, ainsi que d’autres erreurs sur le réseau et sur le réseau.</p>
<p>Le message d’événement contient plus d’informations sur l’erreur spécifique. Certaines opérations ayant entraîné cet avertissement sont supprimées après l’avertissement. Si après plusieurs tentatives d’erreur persistent, MBAM peut se terminer par une erreur réelle. Examinez d’autres messages d’événement dans le journal pour diagnostiquer davantage le MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>903</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/opérationnel</p></td>
<td align="left"><p>CMProviderInformation</p></td>
<td align="left"><p>CM informations sur le fournisseur.</p></td>
<td align="left"><p>Information uniquement; aucun dépannage n’est requis.</p></td>
</tr>
</tbody>
</table>

 

## Opération


Le tableau suivant contient des messages et des informations de dépannage pour les ID d’événement qui peuvent se produire quand MBAM est en cours d’exécution.

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
<th align="left">ID d’événement</th>
<th align="left">Source</th>
<th align="left">Symbole d’événement</th>
<th align="left">Message</th>
<th align="left">Résolution des problèmes</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>1</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Web/Admin</p></td>
<td align="left"><p>WebAppSpnError</p></td>
<td align="left"><p>Application: {SiteName} {VirtualDirectory} ne comporte pas les noms de principal de service suivants: {ListOfSpns} Inscrivez les noms de services principaux requis sur le compte: {ExecutionAccount}.</p></td>
<td align="left"><p>Pour que l’authentification Windows intégrée réussisse, le SPN requis doit être en place. Ce message indique que le SPN requis pour l’application MBAM n’a pas été correctement configuré. Les informations contenues dans cet événement doivent fournir des informations supplémentaires.</p>
<p>Pour plus d’informations, voir «nom de principal de service (SPN)» dans la <a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md#bkmk-prereqsams" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md#bkmk-prereqsams)"> Configuration requise pour l’intégration de MBAM 2,5 Server </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>n°4</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Web/opérationnel</p></td>
<td align="left"><p>PerformanceCounterError</p></td>
<td align="left"><p>Une erreur s’est produite lors de la récupération d’un compteur de performance.</p>
<p>Message: {EventMessage} Category: {CategoryOfPerformanceCounter} compteur de performance: {NameOfPerformanceCounter} instance: {nom de l’instance de catégorie de compteur de performance} exception: {ExceptionThrown}</p>
<p>Le message de suivi contient le message d’exception réel, dont voici une explication:</p>
<p><strong>ArgumentNullException </strong> : cette exception est déclenchée si la catégorie, le compteur ou l’instance du compteur de performance requis n’est pas valide.</p>
<p><strong>System. InvalidOperationException </strong> : CategoryName est une chaîne vide ( &quot; &quot; ).-ou-counterName est une chaîne vide ( &quot; &quot; ).</p>
<p>-ou-le paramètre d’autorisation d’accès en lecture/écriture requis n’est pas valide pour ce compteur.</p>
<p>-ou-la catégorie spécifiée n’existe pas (si readOnly a la valeur true).</p>
<p>-ou-la catégorie spécifiée n’est pas une catégorie personnalisée .NET Framework (si readOnly a la valeur false).</p>
<p>-ou-la catégorie spécifiée est marquée comme multi-instance et nécessite que le compteur de performance soit créé avec un nom d’instance.</p>
<p>-or-instanceName est supérieur à 127 caractères.</p>
<p>-ou-categoryName et counterName ayant été localisés dans différentes langues.</p>
<p><strong>System. ComponentModel. Win32Exception </strong> : une erreur s’est produite lors de l’accès à une API système.</p>
<p><strong>System. PlatformNotSupportedException </strong> : la plateforme est windows 98 ou Windows Millennium Edition (me), qui ne prend pas en charge les compteurs de performance.</p>
<p><strong>System. UnauthorizedAccessException </strong> : le code qui s’exécute sans les privilèges d’administration essayait de lire un compteur de performance.</p></td>
<td align="left"><p>Le message contenu dans l’événement fournit des informations supplémentaires sur l’exception qui a été levée. Si une exception System. UnauthorizedAccessException a été levée, vérifiez que le compte d’exécution MBAM (pool d’applications) a accès aux API de compteurs de performance.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>100</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Web/Admin</p></td>
<td align="left"><p>AdminServiceRecoveryDbError</p></td>
<td align="left"><p><strong>GetMachineUsers </strong> : une erreur s’est produite lors de l’affichage des informations utilisateur dans la base de données. Message: {message}-ou-</p>
<p><strong>GetRecoveryKey </strong> : une erreur s’est produite lors de l’accès à la clé de récupération de la base de données. Message: {message}-ou-</p>
<p><strong>GetRecoveryKey </strong> : une erreur s’est produite lors de l’affichage des informations utilisateur dans la base de données. Message: {message}-ou-</p>
<p><strong>GetRecoveryKeyIds </strong> : une erreur s’est produite lors de l’accès aux ID de clé de récupération de la base de données. Message: {message}-ou-</p>
<p><strong>GetTpmHashForUser </strong> : une erreur s’est produite lors de l’accès aux données de hachage du TPM de la base de données de récupération. Message: {message}-ou-</p>
<p><strong>GetTpmHashForUser </strong> : une erreur s’est produite lors de l’accès aux données de hachage du TPM de la base de données de récupération. Message: {message}-ou-</p>
<p><strong>QueryDriveRecoveryData </strong> : une erreur s’est produite lors de l’accès aux données de récupération de disque à partir de la base de données. Message: {message}-ou-</p>
<p><strong>QueryRecoveryKeyIdsForUser </strong> : une erreur s’est produite lors de l’accès aux ID de clé de récupération de la base de données. Message: {message}-ou-</p>
<p><strong>QueryVolumeUsers </strong> : une erreur s’est produite lors de l’affichage des informations utilisateur dans la base de données.</p></td>
<td align="left"><p>Ce message est enregistré dès qu’il existe une exception lors de la communication avec la base de données de récupération MBAM. Lisez les informations contenues dans la trace pour obtenir des détails spécifiques sur l’exception.</p>
<p>Pour obtenir des instructions détaillées sur la résolution des problèmes, voir l’article TechNet <a href="https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx" data-raw-source="[How to Troubleshoot Connecting to the SQL Server Database Engine](https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx)"> Comment résoudre les problèmes de connexion au moteur de base de données SQL Server </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>101</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Web/Admin</p></td>
<td align="left"><p>AdminServiceComplianceDbError</p></td>
<td align="left"><p><strong>GetRecoveryKey </strong> : une erreur s’est produite lors de la journalisation d’un événement d’audit dans la base de données de conformité. Message: {message}-ou-</p>
<p><strong>GetRecoveryKeyIds </strong> : une erreur s’est produite lors de la journalisation d’un événement d’audit dans la base de données de conformité. Message: {message}-ou-</p>
<p><strong>GetTpmHashForUser </strong> : une erreur s’est produite lors de la journalisation d’un événement d’audit dans la base de données de conformité. Message: {message}-ou-</p>
<p><strong>QueryRecoveryKeyIdsForUser </strong> : une erreur s’est produite lors de la journalisation d’un événement d’audit dans la base de données de conformité. Message: {message}-ou-</p>
<p><strong>QueryDriveRecoveryData </strong> : une erreur s’est produite lors de la journalisation d’un événement d’audit dans la base de données de conformité. Message: {message}</p></td>
<td align="left"><p>Ce message est consigné dès qu’il existe une exception lors de la communication de la base de données de conformité MBAM. Lisez les informations contenues dans la trace pour obtenir des détails spécifiques sur l’exception.</p>
<p>Pour obtenir des instructions détaillées sur la résolution des problèmes, voir l’article TechNet <a href="https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx" data-raw-source="[How to Troubleshoot Connecting to the SQL Server Database Engine](https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx)"> Comment résoudre les problèmes de connexion au moteur de base de données SQL Server </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>102</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Web/Admin</p></td>
<td align="left"><p>AgentServiceRecoveryDbError</p></td>
<td align="left"><p></p></td>
<td align="left"><p>Ce message indique une exception lorsque le service d’agent MBAM tente de communiquer avec la base de données de récupération. Lisez le message contenu dans l’événement pour obtenir des informations spécifiques sur l’exception.</p>
<p>Reportez-vous à l’article TechNet <a href="https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx" data-raw-source="[How to Troubleshoot Connecting to the SQL Server Database Engine](https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx)"> Comment résoudre les problèmes de connexion au moteur de base de données SQL Server </a> pour vérifier si le compte du pool d’applications MBAM dispose des autorisations nécessaires pour se connecter ou s’exécuter sur MBAM récupération de base de données.</p></td>
</tr>
<tr class="even">
<td align="left"><p>103</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Web/Admin</p></td>
<td align="left"><p>AgentServiceError</p></td>
<td align="left"><p>Impossible de détecter un compte d’ordinateur client ou un compte d’utilisateur de migration des données. - ou -</p>
<p>Échec de la vérification du compte pour l’identité de l’appelant.</p></td>
<td align="left"><p>Chaque fois qu’un appel est passé &quot; aux &quot; &quot; méthodes Web PostKeyRecoveryInfo, IsRecoveryKeyResetRequired &quot; , &quot; CommitRecoveryKeyRest &quot; ou &quot; GetTpmHash sur les &quot; services d’agent MBAM, il récupère le contexte de l’appelant pour obtenir les informations d’identification de l’appelant. Si le contexte de l’appelant est null ou vide, le service d’agent MBAM &quot; ne peut pas détecter le compte de l’ordinateur client ou le compte d’utilisateur de migration des données.&quot;</p>
<p>La &quot; vérification du compte de message a échoué pour l’identité de l’appelant, &quot; si la méthode Web attend l’appelant qu’il s’agit d’un compte d’ordinateur, et s’il ne s’agit pas d’un compte d’ordinateur, ou si la méthode Web ne correspond pas à celle d’un compte d’utilisateur et que l’appelant n’est pas un compte d’utilisateur ou un compte de groupe de migration</p></td>
</tr>
<tr class="odd">
<td align="left"><p>104</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Web/Admin</p></td>
<td align="left"><p>StatusServiceComplianceDbConfigError</p></td>
<td align="left"><p>&quot;La chaîne de connexion de la base de données de conformité dans le Registre est vide.&quot;</p></td>
<td align="left"><p>Ce message est consigné chaque fois que la chaîne de connexion de la base de donnees de conformité n’est pas valide.</p>
<p>Vérifier la valeur de la clé de Registre HKLM\Software\Microsoft\MBAM Server\Web\ComplianceDBConnectionString</p></td>
</tr>
<tr class="even">
<td align="left"><p>105</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Web/Admin</p></td>
<td align="left"><p>StatusServiceComplianceDbError</p></td>
<td align="left"><p></p></td>
<td align="left"><p>Ce message d’erreur indique que les sites Web ou les services Web MBAM n’ont pas pu se connecter à la base de données MBAMCompliance.</p>
<p>Reportez-vous à l’article TechNet <a href="https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx" data-raw-source="[How to Troubleshoot Connecting to the SQL Server Database Engine](https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx)"> Comment résoudre les problèmes de connexion au moteur de base de données SQL Server </a> pour vérifier que le compte du pool d’applications IIS se connecte à la base de données de conformité MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>106</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Web/Admin</p></td>
<td align="left"><p>HelpdeskError</p></td>
<td align="left"><p>La demande d’URL {URL} a entraîné une erreur interne. - ou -</p>
<p>Une erreur s’est produite lors de l’obtention des informations de contexte d’exécution. Impossible de vérifier l’inscription au SPN (nom principal de service). - ou -</p>
<p>Une erreur s’est produite lors de la vérification de l’inscription au SPN (nom principal de service).</p></td>
<td align="left"><p>Indique qu’une exception non gérée a été levée dans l’application du support technique. Passez en revue les entrées du journal dans le canal opérationnel de l’administrateur MBAM pour trouver l’exception spécifique. ou</p>
<p>Lors de l’opération de chargement d’un site Web d’assistance initial, une vérification de SPN est effectuée. Pour vérifier le SPN, le support technique doit exécuter les informations de compte d’exécution, les informations de SiteName et ApplicationVirtualPath correspondant au site Web du support technique. Ce message d’erreur est consigné lorsque l’un ou plusieurs de ces éléments sont non valides ou manquants. ou</p>
<p>Ce message indique qu’une exception de sécurité est levée lors de la vérification SPN. Référez-vous à l’exception contenue dans la section Détails de l’événement.</p></td>
</tr>
<tr class="even">
<td align="left"><p>107</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Web/Admin</p></td>
<td align="left"><p>SelfServicePortalError</p></td>
<td align="left"><p>Une erreur s’est produite lors de l’accès à la clé de récupération pour un utilisateur. EventDetails: {ExceptionMessage}-ou-</p>
<p>Une erreur s’est produite lors de l’obtention des informations de contexte d’exécution. Impossible de vérifier l’inscription au SPN (nom principal de service). EventDetails: utilisateur: {nom_utilisateur Identity} application: {SiteName\ApplicationVirtualPath}-ou-</p>
<p>Une erreur s’est produite lors de la vérification de l’inscription au SPN (nom principal de service). EventDetails:{ExceptionMessage}</p></td>
<td align="left"><p>Indique qu’une exception inattendue a été levée lorsqu’une requête a été effectuée pour récupérer la clé de récupération. Voir le message d’exception contenu dans la section Détails de l’événement. Si le suivi est activé sur MBAM support technique, voir tracer les données pour obtenir des messages d’exception détaillés. ou</p>
<p>Au cours d’une opération de chargement initiale, le portail libre-service récupère les informations sur le compte d’exécution, le nom de l’application et le ApplicationVirtualPath correspondant au site Web libre-service pour vérifier le SPN. Ce message d’erreur est consigné lorsque l’un ou plusieurs de ces éléments ne sont pas valides. ou</p>
<p>Ce message indique qu’une exception de sécurité a été levée lors de la vérification SPN. Référez-vous à l’exception contenue dans la section Détails de l’événement.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>108</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Web/Admin</p></td>
<td align="left"><p>DomainControllerError</p></td>
<td align="left"><p>Une erreur s’est produite lors de la résolution du nom de domaine {nom_domaine}, une erreur d’allocation de mémoire s’est produite. - ou -</p>
<p>Impossible d’appeler la méthode DsGetDcName. EventDetails:{ExceptionMessage}</p></td>
<td align="left"><p>Pour résoudre le nom de domaine, MBAM tire parti de l' &quot; &quot; API Windows DsGetDcName. Ce message est consigné lorsque &quot; DsGetDcName &quot; renvoie &quot; ERROR_NOT_ENOUGH_MEMORY &quot; indiquant un échec d’allocation de mémoire. ou</p>
<p>Ce message indique que &quot; &quot; la méthode de l’API DsGetDcName n’est pas disponible sur le système d’hébergement.</p></td>
</tr>
<tr class="even">
<td align="left"><p>109</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Web/Admin</p></td>
<td align="left"><p>WebAppRecoveryDbError</p></td>
<td align="left"><p>Une erreur s’est produite lors de la lecture de la configuration de la base de données de récupération. La chaîne de connexion à la base de données de récupération n’est pas configurée. Message: {message}-ou-</p>
<p><strong>DoesUserHaveMatchingRecoveryKey </strong> : une erreur s’est produite lors de la récupération des ID de clé de récupération pour un utilisateur. Message: {message}-ou-</p>
<p><strong>QueryDriveRecoveryData </strong> : une erreur s’est produite lors de l’accès aux données de récupération du disque. Message: {message}-ou-</p>
<p><strong>QueryRecoveryKeyIdsForUser </strong> : une erreur s’est produite lors de la récupération des ID de clé de récupération pour un utilisateur. Message: {message}-ou-</p>
<p>Une erreur s’est produite lors de l’accès au hachage du mot de passe GPC de la base de données de récupération. EventDetails:{ExceptionMessage}</p></td>
<td align="left"><p>Ce message indique que les informations de la chaîne de connexion de la base de données de récupération à &quot; HKLM\Software\Microsoft\MBAM Server\Web\RecoveryDBConnectionString &quot; sont pas valides. Vérifiez la valeur de clé de Registre fournie. ou</p>
<p>Si l’un des messages restants est enregistré, reportez-vous à la procédure de dépannage décrite dans l’article TechNet <a href="https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx" data-raw-source="[How to Troubleshoot Connecting to the SQL Server Database Engine](https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx)"> Comment résoudre les problèmes de connexion au moteur de base de données SQL Server à l' </a> aide d’informations d’identification de pool d’applications.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>110</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Web/Admin</p></td>
<td align="left"><p>WebAppComplianceDbError</p></td>
<td align="left"><p>Une erreur s’est produite lors de la lecture de la configuration de la base de données de conformité. La chaîne de connexion à la base de données de conformité n’est pas configurée. - ou -</p>
<p><strong>GetRecoveryKeyForCurrentUser </strong> : une erreur s’est produite lors de la journalisation d’un événement d’audit dans la base de données de conformité. Message: {message}-ou-</p>
<p><strong>QueryRecoveryKeyIdsForUser </strong> : une erreur s’est produite lors de la journalisation d’un événement d’audit dans la base de données de conformité. Message: {message}-ou-</p>
<p><strong>QueryRecoveryKeyIdsForUser </strong> : une erreur s’est produite lors de la journalisation d’un événement d’audit dans la base de données de conformité. Message: {message}</p></td>
<td align="left"><p>Ce message indique que les informations de la chaîne de connexion de la base de données de conformité à &quot; HKLM\Software\Microsoft\MBAM Server\Web\ComplianceDBConnectionString &quot; ne sont pas valides. Vérifiez la valeur correspondant à la clé de Registre ci-dessus. ou</p>
<p>Si l’un des messages restants est enregistré, reportez-vous à la procédure de dépannage décrite dans l’article TechNet <a href="https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx" data-raw-source="[How to Troubleshoot Connecting to the SQL Server Database Engine](https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx)"> Comment résoudre les problèmes de connexion au moteur de base de données SQL Server à </a> l’aide d’informations d’identification de pool d’applications.</p></td>
</tr>
<tr class="even">
<td align="left"><p>111</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Web/Admin</p></td>
<td align="left"><p>WebAppDbError</p></td>
<td align="left"><p></p></td>
<td align="left"><p>Ces erreurs indiquent l’une des deux conditions suivantes:</p>
<ul>
<li><p>Les sites Web ou les services Web MBAM ne pouvaient pas se connecter à MBAMCompliance ou à une base de données MBAMRecovery</p></li>
<li><p>Le compte d’exécution MBAM sites Web/WebServices (compte du pool d’applications) n’a pas pu exécuter la procédure stockée GetVersion sur MBAMCompliance ou MBAMRecovery de base de données</p></li>
</ul>
<p>Le message contenu dans l’événement fournit davantage de détails sur l’exception.</p>
<p>Pour plus d’informations sur la procédure de résolution des problèmes répertoriés dans l’article TechNet, voir <a href="https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx" data-raw-source="[How to Troubleshoot Connecting to the SQL Server Database Engine](https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx)"> résolution des problèmes de connexion au moteur de base de données SQL Server </a> pour vérifier que le compte d’exécution MBAM (compte du pool d’applications) peut se connecter à MBAM la base de données de compatibilité/récupération et qu’il dispose des autorisations nécessaires pour exécuter la procédure stockée GetVersion.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>112</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Web/Admin</p></td>
<td align="left"><p>WebAppError</p></td>
<td align="left"><p>Une erreur s’est produite lors de la vérification de l’inscription au SPN (nom principal de service). EventDetails:{ExceptionMessage}</p></td>
<td align="left"><p>Pour procéder à la vérification de SPN, MBAM interroge Active Directory pour récupérer une liste de comptes d’exécution mappés avec SPN. MBAM interroge également le &quot;ApplicationHost.config&quot; pour obtenir les liaisons de sites Web MBAM. Ce message d’erreur indique que MBAM n’a pas pu communiquer avec Active Directory ou qu’il n’a pas pu charger le fichier applicationHost.config.</p>
<p>Vérifiez que le compte d’exécution (compte du pool d’applications) est autorisé à interroger AD ou le fichier ApplicationHost.config. Vérifiez également les entrées de liaison de site dans ApplicationHost.config fichier.</p></td>
</tr>
<tr class="even">
<td align="left"><p>200</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Web/opérationnel</p></td>
<td align="left"><p>HelpDeskInformation</p></td>
<td align="left"><p>L’application de site Web d’administration a été correctement trouvée et associée à une version prise en charge de la base de données de récupération. - ou -</p>
<p>L’application de site Web d’administration a été correctement trouvée et associée à une version prise en charge de la base de données de conformité.</p></td>
<td align="left"><p>Indique une connexion réussie à la base de données de récupération/conformité à partir du site Web du support technique MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>201</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Web/opérationnel</p></td>
<td align="left"><p>SelfServicePortalInformation</p></td>
<td align="left"><p>Application de portail libre-service correctement trouvée et connectée à une version prise en charge de la base de données de récupération. - ou -</p>
<p>Application de portail libre-service correctement trouvée et connectée à une version prise en charge de la base de données de conformité.</p></td>
<td align="left"><p>Indique une connexion réussie à la base de données de récupération/conformité du portail libre-service MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>202</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Web/opérationnel</p></td>
<td align="left"><p>WebAppInformation</p></td>
<td align="left"><p>Le SPN est enregistré correctement par l’application.</p></td>
<td align="left"><p>Indique que les SPN requis pour le site Web du support technique MBAM sont correctement inscrits au compte exécutant.</p></td>
</tr>
</tbody>
</table>

 


## Rubriques connexes


[Document de référence technique pour MBAM2.5](technical-reference-for-mbam-25.md)

[Journaux des événements clients](client-event-logs.md)

 
## Vous avez une suggestion pour MBAM?
- Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)
- Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).
 





