---
title: Installation des bases de données App-V et conversion des identificateurs de sécurité associés à l’aide de PowerShell
description: Installation des bases de données App-V et conversion des identificateurs de sécurité associés à l’aide de PowerShell
author: dansimp
ms.assetid: 9399342b-1ea7-41df-b988-33e302f9debe
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: bb4ff48a532d4c9ec7035421c6e8e7dcd41f5214
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805431"
---
# <span data-ttu-id="09090-103">Installation des bases de données App-V et conversion des identificateurs de sécurité associés à l’aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="09090-103">How to Install the App-V Databases and Convert the Associated Security Identifiers by Using PowerShell</span></span>


<span data-ttu-id="09090-104">Utilisez la procédure PowerShell suivante pour convertir n’importe quel nombre de comptes d’utilisateurs ou d’utilisateurs de services de domaine Active Directory (AD DS) dans des identificateurs de sécurité (SID) au format standard et dans le format hexadécimal utilisé par Microsoft SQL Server lors de l’exécution de scripts SQL.</span><span class="sxs-lookup"><span data-stu-id="09090-104">Use the following PowerShell procedure to convert any number of Active Directory Domain Services (AD DS) user or machine accounts into formatted Security Identifiers (SIDs) both in the standard format and in the hexadecimal format used by Microsoft SQL Server when running SQL scripts.</span></span>

<span data-ttu-id="09090-105">Avant d’essayer cette procédure, vous devez lire et comprendre les informations et les exemples affichés dans la liste suivante:</span><span class="sxs-lookup"><span data-stu-id="09090-105">Before attempting this procedure, you should read and understand the information and examples displayed in the following list:</span></span>

-   <span data-ttu-id="09090-106">**. ENTRÉES** : compte ou comptes utilisés pour la conversion au format sid.</span><span class="sxs-lookup"><span data-stu-id="09090-106">**.INPUTS** – The account or accounts used to convert to SID format.</span></span> <span data-ttu-id="09090-107">Il peut s’agir d’un nom de compte unique ou d’un tableau de noms de compte.</span><span class="sxs-lookup"><span data-stu-id="09090-107">This can be a single account name or an array of account names.</span></span>

-   <span data-ttu-id="09090-108">**. SORTIES** -liste des noms de compte avec le SID correspondant au format standard et hexadécimal.</span><span class="sxs-lookup"><span data-stu-id="09090-108">**.OUTPUTS** - A list of account names with the corresponding SID in standard and hexadecimal formats.</span></span>

-   <span data-ttu-id="09090-109">**Donnés** -</span><span class="sxs-lookup"><span data-stu-id="09090-109">**Examples** -</span></span>

    <span data-ttu-id="09090-110">**.\\ConvertToSID.ps1 DOMAIN\\user\ _account1 DOMAIN\\machine\ _account1 $ DOMAIN\\user\ _account2 | Format-liste**.</span><span class="sxs-lookup"><span data-stu-id="09090-110">**.\\ConvertToSID.ps1 DOMAIN\\user\_account1 DOMAIN\\machine\_account1$ DOMAIN\\user\_account2 | Format-List**.</span></span>

    **<span data-ttu-id="09090-111">$accountsArray = @ ("DOMAIN\\user\ _account1", "DOMAIN\\machine\ _account1 $", "DOMAIN \ _user \ _account2")</span><span class="sxs-lookup"><span data-stu-id="09090-111">$accountsArray = @("DOMAIN\\user\_account1", "DOMAIN\\machine\_account1$", "DOMAIN\_user\_account2")</span></span>**

    **<span data-ttu-id="09090-112">.\\ConvertToSID.ps1 $accountsArray | Ecriture-sortie-FilePath .\\SIDs.txt-Width 200</span><span class="sxs-lookup"><span data-stu-id="09090-112">.\\ConvertToSID.ps1 $accountsArray | Write-Output -FilePath .\\SIDs.txt -Width 200</span></span>**

    \#&gt;

**<span data-ttu-id="09090-113">Pour convertir un nombre quelconque de comptes d’utilisateur ou de services de domaine Active Directory (AD DS) en identificateurs de sécurité (SID)</span><span class="sxs-lookup"><span data-stu-id="09090-113">To convert any number of Active Directory Domain Services (AD DS) user or machine accounts into formatted Security Identifiers (SIDs)</span></span>**

1. <span data-ttu-id="09090-114">Copiez le script suivant dans un éditeur de texte et enregistrez-le en tant que fichier de script PowerShell, par exemple **ConvertToSIDs.ps1**.</span><span class="sxs-lookup"><span data-stu-id="09090-114">Copy the following script into a text editor and save it as a PowerShell script file, for example **ConvertToSIDs.ps1**.</span></span>

2. <span data-ttu-id="09090-115">Pour ouvrir une console PowerShell, cliquez sur **Démarrer** et tapez **PowerShell**.</span><span class="sxs-lookup"><span data-stu-id="09090-115">To open a PowerShell console click **Start** and type **PowerShell**.</span></span> <span data-ttu-id="09090-116">Cliquez avec le bouton droit sur **Windows PowerShell**, puis sélectionnez **Exécuter en tant qu’administrateur**.</span><span class="sxs-lookup"><span data-stu-id="09090-116">Right-click **Windows PowerShell** and select **Run as Administrator**.</span></span>

   ```powershell
   <#
   .SYNOPSIS
   This PowerShell script will take an array of account names and try to convert each of them to the corresponding SID in standard and hexadecimal formats.

   .DESCRIPTION
   This is a PowerShell script that converts any number of Active Directory (AD) user or machine accounts into formatted Security Identifiers (SIDs) both in the standard format and in the hexadecimal format used by SQL server when running SQL scripts.

   .INPUTS
   The account(s) to convert to SID format. This can be a single account name or an array of account names. Please see examples below.

   .OUTPUTS
   A list of account names with the corresponding SID in standard and hexadecimal formats

   .EXAMPLE
   .\ConvertToSID.ps1 DOMAIN\user_account1 DOMAIN\machine_account1$ DOMAIN\user_account2 | Format-List

   .EXAMPLE
   $accountsArray = @("DOMAIN\user_account1", "DOMAIN\machine_account1$", "DOMAIN_user_account2")

   .\ConvertToSID.ps1 $accountsArray | Write-Output -FilePath .\SIDs.txt -Width 200
   #>

   function ConvertSIDToHexFormat
   {
      param([System.Security.Principal.SecurityIdentifier]$sidToConvert)

      $sb = New-Object System.Text.StringBuilder

      [int] $binLength = $sidToConvert.BinaryLength

      [Byte[]] $byteArray = New-Object Byte[] $binLength

      $sidToConvert.GetBinaryForm($byteArray, 0)

      foreach($byte in $byteArray)
      {
          $sb.Append($byte.ToString("X2")) |Out-Null
      }
      return $sb.ToString()
   }

   [string[]]$myArgs = $args



   if(($myArgs.Length -lt 1) -or ($myArgs[0].CompareTo("/?") -eq 0))
   {
       [string]::Format("{0}====== Description ======{0}{0}" +
                  "  Converts any number of user or machine account names to string and hexadecimal SIDs.{0}" +
                  "  Pass the account(s) as space separated command line parameters. (For example 'ConvertToSID.exe DOMAIN\\Account1 DOMAIN\\Account2 ...'){0}" +
                  "  The output is written to the console in the format 'Account name    SID as string   SID as hexadecimal'{0}" +
                  "  And can be written out to a file using standard PowerShell redirection{0}" +
                  "  Please specify user accounts in the format 'DOMAIN\username'{0}" +
                  "  Please specify machine accounts in the format 'DOMAIN\machinename$'{0}" +
                  "  For more help content, please run 'Get-Help ConvertToSID.ps1'{0}" +
                  "{0}====== Arguments ======{0}" +



                  "{0}  /?    Show this help message", [Environment]::NewLine)
   }
   else
   {
       #If an array was passed in, try to split it
       if($myArgs.Length -eq 1)
       {
           $myArgs = $myArgs.Split(' ')
       }

       #Parse the arguments for account names
       foreach($accountName in $myArgs)
       {
           [string[]] $splitString = $accountName.Split('\')  # We're looking for the format "DOMAIN\Account" so anything that does not match, we reject

           if($splitString.Length -ne 2)
           {
               $message = [string]::Format("{0} is not a valid account name. Expected format 'Domain\username' for user accounts or 'DOMAIN\machinename$' for machine accounts.", $accountName)

               Write-Error -Message $message
               continue
           }

           #Convert any account names to SIDs
           try
           {
               [System.Security.Principal.NTAccount] $account = New-Object System.Security.Principal.NTAccount($splitString[0], $splitString[1])

               [System.Security.Principal.SecurityIdentifier] $SID = [System.Security.Principal.SecurityIdentifier]($account.Translate([System.Security.Principal.SecurityIdentifier]))
           }
           catch [System.Security.Principal.IdentityNotMappedException]
           {
               $message = [string]::Format("Failed to translate account object '{0}' to a SID. Please verify that this is a valid user or machine account.", $account.ToString())

               Write-Error -Message $message

               continue
           }

           #Convert regular SID to binary format used by SQL

           $hexSIDString = ConvertSIDToHexFormat $SID

           $SIDs = New-Object PSObject

           $SIDs | Add-Member NoteProperty Account $accountName

           $SIDs | Add-Member NoteProperty SID $SID.ToString()

           $SIDs | Add-Member NoteProperty Hexadecimal $hexSIDString

           Write-Output $SIDs
       }
   }
   ```

3. <span data-ttu-id="09090-117">Exécutez le script que vous avez enregistré à l’étape 1 de cette procédure et transmettez les comptes à convertir en arguments.</span><span class="sxs-lookup"><span data-stu-id="09090-117">Run the script you saved in step one of this procedure passing the accounts to convert as arguments.</span></span>

   <span data-ttu-id="09090-118">Par exemple:</span><span class="sxs-lookup"><span data-stu-id="09090-118">For example,</span></span>

   **<span data-ttu-id="09090-119">.\\ConvertToSID.ps1 DOMAIN\\user\ _account1 DOMAIN\\machine\ _account1 $ DOMAIN\\user\ _account2 | Format-list "or" $accountsArray = @ ("DOMAIN\\user\ _account1", "DOMAIN\\machine\ _account1 $", "DOMAIN \ _user \ _account2")</span><span class="sxs-lookup"><span data-stu-id="09090-119">.\\ConvertToSID.ps1 DOMAIN\\user\_account1 DOMAIN\\machine\_account1$ DOMAIN\\user\_account2 | Format-List” or “$accountsArray = @("DOMAIN\\user\_account1", "DOMAIN\\machine\_account1$", "DOMAIN\_user\_account2")</span></span>**

   **<span data-ttu-id="09090-120">.\\ConvertToSID.ps1 $accountsArray | Ecriture-sortie-FilePath .\\SIDs.txt-Width 200 "</span><span class="sxs-lookup"><span data-stu-id="09090-120">.\\ConvertToSID.ps1 $accountsArray | Write-Output -FilePath .\\SIDs.txt -Width 200”</span></span>**

   <span data-ttu-id="09090-121">Vous **avez une suggestion pour App-V**?</span><span class="sxs-lookup"><span data-stu-id="09090-121">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="09090-122">Ajoutez ou Votez en fonction [de suggestions.](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)</span><span class="sxs-lookup"><span data-stu-id="09090-122">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="09090-123">Vous avez un problème lié à l’application-V?</span><span class="sxs-lookup"><span data-stu-id="09090-123">Got an App-V issue?</span></span>** <span data-ttu-id="09090-124">Utilisez le [Forum TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="09090-124">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="09090-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="09090-125">Related topics</span></span>


[<span data-ttu-id="09090-126">Administration d'App-V à l'aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="09090-126">Administering App-V by Using PowerShell</span></span>](administering-app-v-by-using-powershell.md)
