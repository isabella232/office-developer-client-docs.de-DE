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
  
Die Zellen in einem Microsoft Visio-ShapeSheet enthalten Werte und Formeln. Formeln können wiederum Verweise auf andere Zellen haben, damit Sie einen Wert in einer Zelle basierend auf dem Wert einer anderen Zelle berechnen können. Beim Erstellen und Verwalten komplexer Shapes ist das Erkennen all dieser Abhängigkeiten jedoch unter Umständen sehr schwierig, da eine Formel auf eine beliebige Zelle in der Zeichnung verweisen kann, wobei es egal ist, ob es sich um eine Zelle in demselben ShapeSheet oder um eine Zelle eines anderen Objekts in der Zeichnung handelt, beispielsweise um eine Seite, eine Formatvorlage, einen Master oder ein anderes Shape. 
  
Das **Fenster Formelablaufverfolgung** enthält Informationen, die Ihnen helfen, die Auswirkungen von Änderungen an Zellen zu verstehen. 
  
## <a name="displaying-the-formula-tracing-window"></a>Anzeigen des Fensters für die Formelablaufverfolgung

Klicken Sie zum Anzeigen des **Fensters** Formelablaufverfolgung unter **ShapeSheet Tools** auf der Registerkarte ** Design ** in der Gruppe **Formelablaufverfolgung** auf **Fenster anzeigen.** Das **Fenster** Formelablaufverfolgung wird standardmäßig im ShapeSheet-Fenster angedockt angezeigt, ist jedoch ein verankertes Fenster, das angedockt, gleitet oder mit anderen verfügbaren verankerten ShapeSheet-Fenstern zusammengeführt werden kann, z. B. dem **Style** Explorer-Fenster. 
  
## <a name="tracing-dependent-cells"></a>Verfolgen abhängiger Zellen

Zum Anzeigen einer Liste von Zellen, die von einer bestimmten Zelle abhängig sind, wählen Sie die betreffende Zelle im ShapeSheet-Fenster aus. In diesem Beispiel ist die Zelle Width ausgewählt. 
  
![Zelle "Width" ist ausgewählt](media/ShapeSheetDependents_UI_01_ZA01039814.gif)
  
Klicken Sie zum Anzeigen der abhängigen Zellen in der **Gruppe Formelablaufverfolgung** auf **Ablaufverfolgungsabhängige Zellen.**
  
Im Fenster Formelablaufverfolgung wird eine Liste aller Zellen angezeigt, die von der Zelle Width **abhängig** sind. Sie können zu einer beliebigen Zelle in der Liste  navigieren, indem Sie im Fenster Formelablaufverfolgung auf den Eintrag doppelklicken. 
  
![Alle Zellen mit einer Abhängigkeit von der Zelle Width werden im Fenster Formelablaufverfolgung angezeigt.](media/ShapeSheetDependents_UI_02_ZA01039815.gif)
  
## <a name="tracing-precendent-cells"></a>Präzendente Zellen für die Ablaufverfolgung

Wenn eine Liste aller Zellen angezeigt werden soll, von denen eine bestimmte Zelle abhängt, wählen Sie zunächst die Zelle im ShapeSheet-Fenster aus. In diesem Beispiel ist die Zelle Geometry1.X2 ausgewählt. 
  
![Zelle Geometry1.X2 ist ausgewählt](media/ShapeSheetPrecedents_UI_01_ZA01039817.gif)
  
Klicken Sie zum Anzeigen der Vorgängerzellen in der **Gruppe Formelablaufverfolgung** auf **Präzedenzfälle nachverfolgen.**
  
Im Fenster Formelablaufverfolgung wird eine Liste aller Zellen angezeigt, von der die Zelle Geometry1.X2 **abhängig** ist. Sie können zu einer beliebigen Zelle in der Liste  navigieren, indem Sie im Fenster Formelablaufverfolgung auf den Eintrag doppelklicken. 
  
![Alle Zellen, von der die Zelle Geometry1.X2 abhängig ist, werden im Fenster Formelablaufverfolgung angezeigt.](media/ShapeSheetPrecedents_UI_02_ZA01039818.gif)
  

