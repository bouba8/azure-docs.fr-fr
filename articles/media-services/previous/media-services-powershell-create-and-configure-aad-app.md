---
title: Utiliser PowerShell pour créer une application Azure AD pour accéder à l’API Azure Media Services | Microsoft Docs
description: Découvrez comment utiliser PowerShell pour créer une application Azure Active Directory (Azure AD) et la configurer pour accéder à l’API Azure Media Services.
services: media-services
documentationcenter: ''
author: Juliako
manager: femila
editor: ''
ms.service: media-services
ms.workload: media
ms.tgt_pltfrm: na
ms.devlang: na
ms.topic: article
ms.date: 02/10/2019
ms.author: juliako
ms.openlocfilehash: bec7fdbbbedb44cb4e74206c05ecec18400a4dbb
ms.sourcegitcommit: e69fc381852ce8615ee318b5f77ae7c6123a744c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/11/2019
ms.locfileid: "55989009"
---
# <a name="use-powershell-to-create-an-azure-ad-app-to-use-with-the-azure-media-services-api"></a>Utiliser PowerShell pour créer une application Azure AD à utiliser avec l’API Azure Media Services

Découvrez comment utiliser un script PowerShell pour créer une application Azure Active Directory (Azure AD) et un principal du service pour accéder aux ressources Azure Media Services.  

## <a name="prerequisites"></a>Prérequis

- Un compte Azure. Si vous n’avez pas de compte, commencez avec un [essai gratuit Azure](https://azure.microsoft.com/pricing/free-trial/). 
- Un compte Media Services. Pour plus d’informations, voir [Création d’un compte Azure Media Services dans le portail Azure](media-services-portal-create-account.md).
- Azure PowerShell version 0.8.8 ou version ultérieure. Pour plus d’informations, découvrez l’[utilisation d’Azure PowerShell](https://docs.microsoft.com/powershell/azure/overview).
- Applets de commande Azure Resource Manager.  

## <a name="create-an-azure-ad-app-by-using-powershell"></a>Créer une application Azure AD à l’aide de PowerShell  

```powershell
Connect-AzureRmAccount
Import-Module AzureRM.Resources
Set-AzureRmContext -SubscriptionId $SubscriptionId
$ServicePrincipal = New-AzureRMADServicePrincipal -DisplayName $ApplicationDisplayName -Password $Password

Get-AzureRmADServicePrincipal -ObjectId $ServicePrincipal.Id 
$NewRole = $null
$Scope = "/subscriptions/your subscription id/resourceGroups/userresourcegroup/providers/microsoft.media/mediaservices/your media account"

$Retries = 0;While ($NewRole -eq $null -and $Retries -le 6)
{
    # Sleep here for a few seconds to allow the service principal application to become active (usually, it will take only a couple of seconds)
    Sleep 15
    New-AzureRMRoleAssignment -RoleDefinitionName Contributor -ServicePrincipalName $ServicePrincipal.ApplicationId -Scope $Scope | Write-Verbose -ErrorAction SilentlyContinue
    $NewRole = Get-AzureRMRoleAssignment -ServicePrincipalName $ServicePrincipal.ApplicationId -ErrorAction SilentlyContinue
    $Retries++;
}
```

Pour plus d’informations, consultez les articles suivants :

- [Créer un principal du service pour accéder aux ressources à l’aide d’Azure PowerShell](../../active-directory/develop/howto-authenticate-service-principal-powershell.md)
- [Gérer le contrôle d’accès en fonction du rôle à l’aide d’Azure PowerShell](../../role-based-access-control/role-assignments-powershell.md)
- [Comment configurer manuellement des applications démons à l’aide de certificats](https://github.com/Azure-Samples/active-directory-dotnet-daemon-certificate-credential/blob/master/Manual-Configuration-Steps.md#add-the-certificate-as-a-key-for-the-todolistdaemonwithcert-application-in-azure-ad)

## <a name="next-steps"></a>Étapes suivantes

Commencez le [chargement de fichiers sur votre compte](media-services-portal-upload-files.md).
