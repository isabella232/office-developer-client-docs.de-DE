---
title: Informationen zum Formelprotokollierungsfenster
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm60118
localization_priority: Normal
ms.assetid: 0cdacd4e-74dc-32c3-2eb2-219bf7fcb532
description: Das Fenster Formelprotokollierung bietet Shape-Entwicklern Informationen über gegenseitige Abhängigkeiten zwischen Zellen, sowohl für abhängige Zellen (Zellen mit einer Abhängigkeit gegenüber einer bestimmten Zelle) als auch für Vorgängerzellen (Zellen, von denen eine bestimmte Zelle abhängt).
ms.openlocfilehash: f5f9d6a7ba3ab7049715d31342cfe7aa68ea053f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345320"
---
# <a name="about-the-formula-tracing-window"></a>Informationen zum Fenster "Formelprotokollierung"

Das Fenster **Formelprotokollierung** bietet Shape-Entwicklern Informationen über gegenseitige Abhängigkeiten zwischen Zellen, sowohl für abhängige Zellen (Zellen mit einer Abhängigkeit gegenüber einer bestimmten Zelle) als auch für Vorgängerzellen (Zellen, von denen eine bestimmte Zelle abhängt). 
  
Die Zellen in einem Microsoft Visio-ShapeSheet enthalten Werte und Formeln. Formeln können wiederum Verweise auf andere Zellen enthalten, sodass Sie die Möglichkeit haben, einen Wert in einer Zelle basierend auf dem Wert einer anderen Zelle zu berechnen. Beim Erstellen und Verwalten komplexer Shapes ist das Erkennen all dieser Abhängigkeiten jedoch unter Umständen sehr schwierig, da eine Formel auf eine beliebige Zelle in der Zeichnung verweisen kann, wobei es egal ist, ob es sich um eine Zelle in demselben ShapeSheet oder um eine Zelle eines anderen Objekts in der Zeichnung handelt, beispielsweise um eine Seite, eine Formatvorlage, einen Master oder ein anderes Shape. 
  
Das Fenster für die **Formelprotokollierung** enthält Informationen, die Ihnen helfen, die Auswirkungen von Änderungen, die Sie an Zellen vornehmen, zu verstehen. 
  
## <a name="displaying-the-formula-tracing-window"></a>Anzeigen des Fensters für die Formelprotokollierung

Klicken Sie zum Anzeigen des Fensters für die **Formel Ablaufverfolgung** , wobei das ShapeSheet-Fenster aktiv ist, unter **ShapeSheet-Tools** auf der Registerkarte * * Design * * in der Gruppe **Formelprotokollierung** auf **Fenster anzeigen**. Das Fenster für die **Formelprotokollierung** wird standardmäßig im ShapeSheet-Fenster angedockt, es handelt sich jedoch um ein verankertes Fenster, das angedockt, unverankert oder mit anderen verfügbaren verankerten ShapeSheet-Fenstern zusammengeführt werden kann, beispielsweise im Fenster **Format-Explorer** . 
  
## <a name="tracing-dependent-cells"></a>Verfolgen abhängiger Zellen

Zum Anzeigen einer Liste von Zellen, die von einer bestimmten Zelle abhängig sind, wählen Sie die betreffende Zelle im ShapeSheet-Fenster aus. In diesem Beispiel ist die Zelle Width ausgewählt. 
  
![Die Zelle "width" ist ausgewählt](media/ShapeSheetDependents_UI_01_ZA01039814.gif)
  
Um die abhängigen Zellen anzuzeigen, klicken Sie in der Gruppe **Formelprotokollierung**auf **Ablauf Verfolgungs abhängige**.
  
Eine Liste aller Zellen mit einer Abhängigkeit von der Zelle Breite wird im Fenster **Formelprotokollierung** angezeigt. Sie können zu einer beliebigen Zelle in der Liste navigieren, indem Sie im Fenster **Formelprotokollierung** auf den entsprechenden Eintrag doppelklicken. 
  
![Alle Zellen mit einer Abhängigkeit von der Zelle "Breite" werden im Fenster "Formel Ablaufverfolgung" angezeigt.](media/ShapeSheetDependents_UI_02_ZA01039815.gif)
  
## <a name="tracing-precendent-cells"></a>NachVerfolgen von precendent-Zellen

Wenn eine Liste aller Zellen angezeigt werden soll, von denen eine bestimmte Zelle abhängt, wählen Sie zunächst die Zelle im ShapeSheet-Fenster aus. In diesem Beispiel ist die Zelle Geometry1.X2 ausgewählt. 
  
![Zelle Geometry1. x2 ist ausgewählt](media/ShapeSheetPrecedents_UI_01_ZA01039817.gif)
  
Zum Anzeigen der Vorgängerzellen klicken Sie in der Gruppe **Formelprotokollierung**auf **Vorgänger**-Traces.
  
Eine Liste aller Zellen, von denen die Zelle Geometry1. x2 abhängig ist, wird im Fenster **Formelprotokollierung** angezeigt. Sie können zu einer beliebigen Zelle in der Liste navigieren, indem Sie im Fenster **Formelprotokollierung** auf den entsprechenden Eintrag doppelklicken. 
  
![Alle Zellen, von denen die Zelle Geometry1. x2 abhängig ist, werden im Fenster Formelprotokollierung angezeigt.](media/ShapeSheetPrecedents_UI_02_ZA01039818.gif)
  

