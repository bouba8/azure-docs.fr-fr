---
title: Langage de balisage de synthèse vocale (SSML) - Services Speech
titleSuffix: Azure Cognitive Services
description: Utilisation du langage de balisage de synthèse vocale pour contrôler la prononciation et la prosodie dans la synthèse vocale.
services: cognitive-services
author: erhopf
manager: nitinme
ms.service: cognitive-services
ms.subservice: speech-service
ms.topic: conceptual
ms.date: 12/13/2018
ms.author: erhopf
ms.custom: seodec18
ms.openlocfilehash: f721c91c828b5c7c8497c07bb0cfe79646daf0f8
ms.sourcegitcommit: 90cec6cccf303ad4767a343ce00befba020a10f6
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/07/2019
ms.locfileid: "55868835"
---
# <a name="speech-synthesis-markup-language"></a>Langage de balisage de synthèse vocale

Le langage de balisage de synthèse vocale (SSML) est un langage de balisage basé sur XML qui fournit un moyen de contrôler la prononciation et la *prosodie* de la synthèse vocale. La prosodie fait référence au rythme et la tonalité de la voix. C’est en quelque sorte sa musique. Vous pouvez indiquer des mots en phonétique, fournir des indications permettant d’interpréter les nombres, insérer des pauses, contrôler la hauteur de la voix, le volume, le débit, etc. Pour plus d’informations, consultez [Speech Synthesis Markup Language (SSML) Version 1.0](http://www.w3.org/TR/2009/REC-speech-synthesis-20090303/).

Pour obtenir la liste complète des langues, paramètres régionaux et voix (neuronales et standard) pris en charge, consultez [prise en charge linguistique](language-support.md#text-to-speech).

Les sections suivantes fournissent des exemples pour les tâches de synthèse vocale courantes.

>[!IMPORTANT]
> À l’heure actuelle, le balisage prosodique n’est disponible que pour les voix standard.

## <a name="add-a-break"></a>Ajouter une pause
```xml
<speak version='1.0' xmlns="http://www.w3.org/2001/10/synthesis" xml:lang='en-US'>
<voice  name='Microsoft Server Speech Text to Speech Voice (en-US, Jessa24kRUS)'>
    Welcome to Microsoft Cognitive Services <break time="100ms" /> Text-to-Speech API.
</voice> </speak>
```

## <a name="change-speaking-rate"></a>Modifier le débit
```xml
<speak version='1.0' xmlns="http://www.w3.org/2001/10/synthesis" xml:lang='en-US'>
<voice  name='Microsoft Server Speech Text to Speech Voice (en-US, Guy24kRUS)'>
<prosody rate="+30.00%">
    Welcome to Microsoft Cognitive Services Text-to-Speech API.
</prosody></voice> </speak>
```

## <a name="pronunciation"></a>Prononcer
```xml
<speak version='1.0' xmlns="http://www.w3.org/2001/10/synthesis" xml:lang='en-US'>
<voice  name='Microsoft Server Speech Text to Speech Voice (en-US, Jessa24kRUS)'>
    <phoneme alphabet="ipa" ph="t&#x259;mei&#x325;&#x27E;ou&#x325;"> tomato </phoneme>
</voice> </speak>
```

## <a name="change-volume"></a>Modifier le volume
```xml
<speak version='1.0' xmlns="http://www.w3.org/2001/10/synthesis" xml:lang='en-US'>
<voice  name='Microsoft Server Speech Text to Speech Voice (en-US, JessaRUS)'>
<prosody volume="+20.00%">
    Welcome to Microsoft Cognitive Services Text-to-Speech API.
</prosody></voice> </speak>
```

## <a name="change-pitch"></a>Modifier la tonalité
```xml
<speak version='1.0' xmlns="http://www.w3.org/2001/10/synthesis" xml:lang='en-US'>
    <voice  name='Microsoft Server Speech Text to Speech Voice (en-US, Guy24kRUS)'>
    Welcome to <prosody pitch="high">Microsoft Cognitive Services Text-to-Speech API.</prosody>
</voice> </speak>
```

## <a name="change-pitch-contour"></a>Modifier le contour intonatif
```xml
<speak version='1.0' xmlns="http://www.w3.org/2001/10/synthesis" xml:lang='en-US'>
<voice  name='Microsoft Server Speech Text to Speech Voice (en-US, JessaRUS)'>
<prosody contour="(80%,+20%) (90%,+30%)" >
    Good morning.
</prosody></voice> </speak>
```

## <a name="use-multiple-voices"></a>Utiliser plusieurs voix
```xml
<speak version='1.0' xmlns="http://www.w3.org/2001/10/synthesis" xml:lang='en-US'>
<voice  name='Microsoft Server Speech Text to Speech Voice (en-US, JessaRUS)'>
    Good morning!
</voice>
<voice  name='Microsoft Server Speech Text to Speech Voice (en-US, Guy24kRUS)'>
    Good morning to you too Jessa!
</voice> </speak>
```

## <a name="next-steps"></a>Étapes suivantes

* [Prise en charge linguistique : voix, paramètres régionaux, langues](language-support.md)
