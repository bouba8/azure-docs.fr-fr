---
title: Limites d’Azure Data Box Gateway | Microsoft Docs
description: Décrit les limites système et les tailles recommandées pour Microsoft Azure Data Box Gateway.
services: databox
author: alkohli
ms.service: databox
ms.subservice: gateway
ms.topic: article
ms.date: 02/05/2019
ms.author: alkohli
ms.openlocfilehash: f785e9e540af01b74678cf75159775cd2888e09e
ms.sourcegitcommit: d1c5b4d9a5ccfa2c9a9f4ae5f078ef8c1c04a3b4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55959576"
---
# <a name="azure-data-box-gateway-limits-preview"></a>Limites d’Azure Data Box Gateway (préversion)


Tenez compte de ces limites quand vous déployez et utilisez votre solution Microsoft Azure Data Box Gateway. 

> [!IMPORTANT] 
> Data Box Gateway est disponible en préversion. Veuillez lire les [conditions d’utilisation de la préversion](https://azure.microsoft.com/support/legal/preview-supplemental-terms/) avant de déployer cette solution. 


## <a name="data-box-gateway-service-limits"></a>Limites de service Data Box Gateway

[!INCLUDE [data-box-edge-gateway-service-limits](../../includes/data-box-edge-gateway-service-limits.md)]

## <a name="data-box-gateway-device-limits"></a>Limites d’appareil Data Box Gateway

Le tableau suivant décrit les limites de l’appareil Data Box Gateway.

| Description | Valeur |
|---|---|
| Non. de fichiers par appareil |100 millions <br> La limite est d’environ 25 millions de fichiers pour 2 To d’espace disque avec une limite maximale à 100 millions |
| Non. de partages par appareil |24 |
| Non. de partages par conteneur |1 |
|Taille de fichier maximale écrite sur un partage|Pour un appareil virtuel de 2 To, la taille de fichier maximale est de 500 Go. <br> La taille maximale de fichier augmente proportionnellement avec la taille du disque de données, jusqu’à atteindre la taille maximale de 5 To. |

## <a name="azure-storage-limits"></a>Limites du stockage Azure

[!INCLUDE [data-box-edge-gateway-storage-limits](../../includes/data-box-edge-gateway-storage-limits.md)]

## <a name="data-upload-caveats"></a>Mises en garde relatives au chargement de données

[!INCLUDE [data-box-edge-gateway-storage-data-upload-caveats](../../includes/data-box-edge-gateway-storage-data-upload-caveats.md)]

## <a name="azure-storage-account-size-and-object-size-limits"></a>Limites de taille d’objet et de compte de stockage Azure

[!INCLUDE [data-box-edge-gateway-storage-acct-limits](../../includes/data-box-edge-gateway-storage-acct-limits.md)]

## <a name="azure-object-size-limits"></a>Limites de taille des objets Azure

[!INCLUDE [data-box-edge-gateway-storage-object-limits](../../includes/data-box-edge-gateway-storage-object-limits.md)]

## <a name="next-steps"></a>Étapes suivantes

- [Préparer le déploiement d’Azure Data Box Gateway](data-box-gateway-deploy-prep.md)
