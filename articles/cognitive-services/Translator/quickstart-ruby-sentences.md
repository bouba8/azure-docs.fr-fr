---
title: 'Démarrage rapide : Obtenir la longueur de phrases, Ruby - API de traduction de texte Translator Text'
titleSuffix: Azure Cognitive Services
description: Dans ce guide de démarrage rapide, vous allez rechercher la longueur des phrases du texte à l’aide de l’API de traduction de texte Translator Text avec Ruby.
services: cognitive-services
author: erhopf
manager: nitinme
ms.service: cognitive-services
ms.subservice: translator-text
ms.topic: quickstart
ms.date: 02/08/2019
ms.author: erhopf
ms.openlocfilehash: fb448498a9622d0e3b149e4e3d4041b3a7ca580c
ms.sourcegitcommit: 943af92555ba640288464c11d84e01da948db5c0
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2019
ms.locfileid: "55975447"
---
# <a name="quickstart-get-sentence-lengths-with-the-translator-text-rest-api-ruby"></a>Démarrage rapide : Obtenir la longueur de phrases avec l’API REST de traduction de texte Translator Text (Ruby)

Dans ce démarrage rapide, vous allez rechercher les longueurs des phrases dans le texte à l’aide de l’API de traduction de texte Translator Text.

## <a name="prerequisites"></a>Prérequis

[Ruby 2.4](https://www.ruby-lang.org/en/downloads/) (ou une version ultérieure) est nécessaire pour exécuter ce code.

Pour utiliser l’API de traduction de texte Translator Text, vous avez également besoin d’une clé d’abonnement. Consultez [Comment s’inscrire à l’API de traduction de texte Translator Text](translator-text-how-to-signup.md).

## <a name="breaksentence-request"></a>Requête BreakSentence

Le code suivant fractionne le texte source en phrases à l’aide de la méthode [BreakSentence](./reference/v3-0-break-sentence.md).

1. Créez un nouveau projet Ruby dans votre éditeur de code favori.
2. Ajoutez le code ci-dessous.
3. Remplacez la valeur `key` par une clé d’accès valide pour votre abonnement.
4. Exécutez le programme.

```ruby
require 'net/https'
require 'uri'
require 'cgi'
require 'json'
require 'securerandom'

# **********************************************
# *** Update or verify the following values. ***
# **********************************************

# Replace the key string value with your valid subscription key.
key = 'ENTER KEY HERE'

host = 'https://api.cognitive.microsofttranslator.com'
path = '/breaksentence?api-version=3.0'

uri = URI (host + path)

text = 'How are you? I am fine. What did you do today?'

content = '[{"Text" : "' + text + '"}]'

request = Net::HTTP::Post.new(uri)
request['Content-type'] = 'application/json'
request['Content-length'] = content.length
request['Ocp-Apim-Subscription-Key'] = key
request['X-ClientTraceId'] = SecureRandom.uuid
request.body = content

response = Net::HTTP.start(uri.host, uri.port, :use_ssl => uri.scheme == 'https') do |http|
    http.request (request)
end

result = response.body.force_encoding("utf-8")

json = JSON.pretty_generate(JSON.parse(result))
puts json
```

## <a name="breaksentence-response"></a>Réponse BreakSentence

Une réponse correcte est renvoyée au format JSON, comme dans l’exemple suivant :

```json
[
  {
    "detectedLanguage": {
      "language": "en",
      "score": 1.0
    },
    "sentLen": [
      13,
      11,
      22
    ]
  }
]
```

## <a name="next-steps"></a>Étapes suivantes

Explorez l’exemple de code pour ce démarrage rapide et d’autres, y compris la traduction et la translittération, ainsi que d’autres exemples de projets de l’API de traduction de texte Translator Text sur GitHub.

> [!div class="nextstepaction"]
> [Explorer des exemples Ruby sur GitHub](https://aka.ms/TranslatorGitHub?type=&language=ruby)
