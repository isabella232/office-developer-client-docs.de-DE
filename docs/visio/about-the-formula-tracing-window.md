---
title: Informationen zum Formelprotokollierungsfenster
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm60118
ms.localizationpriority: medium
ms.assetid: 0cdacd4e-74dc-32c3-2eb2-219bf7fcb532
description: Das Fenster Formelprotokollierung bietet Shape-Entwicklern Informationen über gegenseitige Abhängigkeiten zwischen Zellen, sowohl für abhängige Zellen (Zellen mit einer Abhängigkeit gegenüber einer bestimmten Zelle) als auch für Vorgängerzellen (Zellen, von denen eine bestimmte Zelle abhängt).
ms.openlocfilehash: 77b058337bd1e8ea95f14015acc15fdccb14dbe4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59628934"
---
# <a name="about-the-formula-tracing-window"></a>Informationen zum Fenster "Formelprotokollierung"

Das Fenster **Formelprotokollierung** bietet Shape-Entwicklern Informationen über gegenseitige Abhängigkeiten zwischen Zellen, sowohl für abhängige Zellen (Zellen mit einer Abhängigkeit gegenüber einer bestimmten Zelle) als auch für Vorgängerzellen (Zellen, von denen eine bestimmte Zelle abhängt). 
  
Die Zellen in einem Microsoft Visio-ShapeSheet enthalten Werte und Formeln. Formeln können wiederum Verweise auf andere Zellen haben, sodass Sie einen Wert in einer Zelle basierend auf dem Wert einer anderen Zelle berechnen können. Beim Erstellen und Verwalten komplexer Shapes ist das Erkennen all dieser Abhängigkeiten jedoch unter Umständen sehr schwierig, da eine Formel auf eine beliebige Zelle in der Zeichnung verweisen kann, wobei es egal ist, ob es sich um eine Zelle in demselben ShapeSheet oder um eine Zelle eines anderen Objekts in der Zeichnung handelt, beispielsweise um eine Seite, eine Formatvorlage, einen Master oder ein anderes Shape. 
  
Das Fenster **Formelprotokollierung** enthält Informationen, die Ihnen dabei helfen, die Auswirkungen von Änderungen zu verstehen, die Sie an Zellen vornehmen. 
  
## <a name="displaying-the-formula-tracing-window"></a>Anzeigen des Fensters für die Formelablaufverfolgung

Klicken Sie zum Anzeigen des **Fensters Formelablaufverfolgung** mit aktivem ShapeSheet-Fenster unter **ShapeSheet-Tools** auf der Registerkarte **Entwurf ** in der Gruppe Formelablaufverfolgung auf Fenster **anzeigen.**  Das Fenster **"Formelablaufverfolgung"** wird standardmäßig im ShapeSheet-Fenster angedockt angezeigt, es handelt sich jedoch um ein verankertes Fenster, das verankert, verschoben oder mit anderen verfügbaren verankerten ShapeSheet-Fenstern zusammengeführt werden kann, z. B. dem **Fenster "Formatvorlagen-Explorer".** 
  
## <a name="tracing-dependent-cells"></a>Verfolgen abhängiger Zellen

Zum Anzeigen einer Liste von Zellen, die von einer bestimmten Zelle abhängig sind, wählen Sie die betreffende Zelle im ShapeSheet-Fenster aus. In diesem Beispiel ist die Zelle Width ausgewählt. 
  
![Zelle "Width" ist ausgewählt](media/ShapeSheetDependents_UI_01_ZA01039814.gif)
  
Klicken Sie zum Anzeigen der abhängigen Zellen in der Gruppe **Formula** Tracing auf **Trace Dependents.**
  
Eine Liste aller Zellen mit einer Abhängigkeit von der Zelle Width wird im Fenster **Formelablaufverfolgung** angezeigt. Sie können zu einer beliebigen Zelle in der Liste  navigieren, indem Sie im Fenster Formelablaufverfolgung auf den eintrag doppelklicken. 
  
![Alle Zellen mit einer Abhängigkeit von der Zelle Width werden im Fenster Formelablaufverfolgung angezeigt.](media/ShapeSheetDependents_UI_02_ZA01039815.gif)
  
## <a name="tracing-precendent-cells"></a>Ablaufverfolgung vorab abhängiger Zellen

Wenn eine Liste aller Zellen angezeigt werden soll, von denen eine bestimmte Zelle abhängt, wählen Sie zunächst die Zelle im ShapeSheet-Fenster aus. In diesem Beispiel ist die Zelle Geometry1.X2 ausgewählt. 
  
![Zelle Geometry1.X2 ist ausgewählt](media/ShapeSheetPrecedents_UI_01_ZA01039817.gif)
  
Klicken Sie zum Anzeigen der Vorgängerzellen in der Gruppe **"Formelablaufverfolgung"** auf **"Vorgängerverfolgung".**
  
Eine Liste aller Zellen, von denen die Zelle Geometry1.X2 abhängig ist, wird im Fenster Formelablaufverfolgung angezeigt.  Sie können zu einer beliebigen Zelle in der Liste  navigieren, indem Sie im Fenster Formelablaufverfolgung auf den eintrag doppelklicken. 
  
![Alle Zellen, von denen die Zelle Geometry1.X2 abhängig ist, werden im Fenster Formelablaufverfolgung angezeigt.](media/ShapeSheetPrecedents_UI_02_ZA01039818.gif)
  

