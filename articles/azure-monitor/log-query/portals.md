---
title: Affichage et analyse de données de journal dans Azure Monitor | Microsoft Docs
description: Cet article décrit l’utilisation de Log Analytics dans le portail Azure pour créer et modifier des requêtes de journal dans Azure Monitor.
services: log-analytics
documentationcenter: ''
author: bwren
manager: carmonm
editor: ''
ms.service: log-analytics
ms.workload: na
ms.tgt_pltfrm: na
ms.topic: conceptual
ms.date: 12/22/2018
ms.author: bwren
ms.openlocfilehash: 6e84344e1c0229d15891bd15a512880da6e20cfe
ms.sourcegitcommit: fec0e51a3af74b428d5cc23b6d0835ed0ac1e4d8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2019
ms.locfileid: "56110760"
---
# <a name="viewing-and-analyzing-log-data-in-azure-monitor"></a>Affichage et analyse de données de journal dans Azure Monitor
Log Analytics est la principale expérience d'utilisation de données de journal et de création de requêtes dans Azure Monitor. Ouvrez Log Analytics à partir de **Journaux** dans le menu **Azure Monitor**. Vous pouvez obtenir une introduction à ce portail et inspecter ses fonctionnalités dans la section [Prise en main de Log Analytics dans le portail Azure](get-started-portal.md).

Log Analytics offre les fonctionnalités d'utilisation de requêtes de journal suivantes.

* Plusieurs onglets : créez des onglets distincts pour travailler avec plusieurs requêtes.
* Visualisations enrichies : diverses options de création de graphiques.
* Amélioration de la saisie semi-automatique Intellisense et de langage.
* Mise en surbrillance syntaxique : améliore la lisibilité des requêtes. 
* Explorateur de requêtes : requêtes et fonctions avec enregistrement d’accès.
* Vie Schéma : examinez la structure de vos données pour faciliter l’écriture des requêtes.
* Partager : créez des liens vers des requêtes, ou épinglez des requêtes sur n’importe quel tableau de bord Azure partagé.
* Analyse intelligente : identifie les pics dans vos graphiques et en analyse rapidement la cause.
* Sélection de colonnes : triez et regroupez les colonnes dans les résultats de la requête.

> [!NOTE]
> Log Analytics affiche les mêmes fonctionnalités que le portail Analytics avancé, un outil externe au portail Azure. Le portail Analytics avancé est toujours disponible, mais les liens et les autres références à celui-ci dans le portail Azure sont remplacés par cette nouvelle page.

![Log Analytics](media/portals/log-analytics.png)

### <a name="resource-logs"></a>Journaux de ressources
Log Analytics s’intègre à différentes ressources Azure, comme les machines virtuelles. Cela signifie que vous pouvez ouvrir Log Analytics directement via le menu de surveillance de la ressource, sans passer par Azure Monitor (en perdant alors le contexte de la ressource). L’option **Journaux** n’a pas encore été activée pour toutes les ressources Azure, mais elle commence à apparaître dans le menu du portail pour plusieurs types de ressource.

Lorsque Log Analytics est ouvert à partir d’une ressource spécifique, il est automatiquement étendu pour journaliser les enregistrements de cette ressource uniquement.   Si vous voulez écrire une requête incluant d’autres enregistrements, vous devrez l’ouvrir à partir du menu d’Azure Monitor.

Les options suivantes ne sont pas encore disponibles via l’affichage des ressources de Log Analytics :

- Enregistrer
- Définir une alerte
- Explorateur de requêtes
- Basculer vers un autre espace de travail/ressource (pas planifiée à l’heure actuelle)


### <a name="firewall-requirements"></a>Configuration requise du pare-feu
Votre navigateur doit pouvoir accéder aux adresses suivantes pour accéder à Log Analytics.  Si votre navigateur accède au portail Azure par le biais d’un pare-feu, vous devez activer l’accès à ces adresses.

| Uri | IP | Ports |
|:---|:---|:---|
| portal.loganalytics.io | Dynamique | 80,443 |
| api.loganalytics.io    | Dynamique | 80,443 |
| docs.loganalytics.io   | Dynamique | 80,443 |


## <a name="log-search-classic"></a>Recherche dans les journaux (classique)
Recherche dans les journaux est l’expérience héritée du portail Azure pour interroger et analyser les données de journal dans Azure Monitor. Encore disponible, elle sera prochainement mise hors service. Ouvrez Recherche dans les journaux à partir de **Journaux (classiques)** dans le menu Log Analytics.



![Recherche dans les journaux](media/portals/log-search-portal.png)


## <a name="next-steps"></a>Étapes suivantes

- Suivez un [tutoriel sur l'utilisation de Log Analytics](../../azure-monitor/log-query/get-started-portal.md).
- Suivez un [tutoriel sur l'utilisation de Recherche dans les journaux](../../azure-monitor/learn/tutorial-viewdata.md).

