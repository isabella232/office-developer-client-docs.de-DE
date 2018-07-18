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
ms.openlocfilehash: 316ac219f548b2459ea2d0ad8cece0f693957fcf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796361"
---
# <a name="about-the-formula-tracing-window"></a>Informationen zur zum Formelablauffenster

Das Fenster **Formelprotokollierung** bietet Shape-Entwicklern Informationen über gegenseitige Abhängigkeiten zwischen Zellen, sowohl für abhängige Zellen (Zellen mit einer Abhängigkeit gegenüber einer bestimmten Zelle) als auch für Vorgängerzellen (Zellen, von denen eine bestimmte Zelle abhängt). 
  
Die Zellen in einem Microsoft Visio-ShapeSheet enthalten Werte und Formeln. Formeln können wiederum Verweise auf andere Zellen, was Ihnen die Möglichkeit, einen Wert in einer Zelle basierend auf einer anderen Zelle Wert berechnen lassen. Beim Erstellen oder Verwalten komplexer Shapes, kann jedoch es schwierig sein, alle diese Abhängigkeiten identifiziert werden, da eine Formel, die eine beliebige Zelle in der Zeichnung verwiesen werden kann, ob es sich um eine Zelle in der gleichen ShapeSheet oder eine Zelle, die in ein anderes Objekt in der Zeichnung gehören ist, beispielsweise einer Seite, Formatvorlage, Master-Shape oder eine andere Form. 
  
Im Fenster **Formelprotokollierung** enthält Informationen, mit denen das Verständnis die Auswirkungen von Änderungen, die Sie Zellen vornehmen. 
  
## <a name="displaying-the-formula-tracing-window"></a>Anzeigen von Formelprotokollierungsfenster

So zeigen Sie das Fenster **Formelprotokollierung** im ShapeSheet-Fenster aktiv ist, klicken Sie unter **ShapeSheet-Tools** auf an der ** Design ** klicken auf der Registerkarte in der Gruppe **Formelprotokollierung** **Fenster anzeigen**. **Das Formelprotokollierungsfenster** angedockten im ShapeSheet-Fenster wird standardmäßig angezeigt, jedoch ist ein verankertes Fenster, das angedockt, Mauszeiger halten oder zusammengeführt werden kann mit anderen verfügbaren verankerten ShapeSheet-Fenster, beispielsweise das **Format-Explorer** -Fenster. 
  
## <a name="tracing-dependent-cells"></a>Verfolgen abhängiger Zellen

Zum Anzeigen einer Liste von Zellen, die von einer bestimmten Zelle abhängig sind, wählen Sie die betreffende Zelle im ShapeSheet-Fenster aus. In diesem Beispiel ist die Zelle Width ausgewählt. 
  
![](media/ShapeSheetDependents_UI_01_ZA01039814.gif)
  
Klicken Sie zum Anzeigen von ihr abhängigen Zellen klicken, in der Gruppe **Formelprotokollierung**auf **Spur zum Nachfolger**.
  
Eine Liste aller von der Zelle Width abhängigen Zellen wird im Fenster Formelprotokollierung angezeigt. Sie können zu einer beliebigen Zelle in der Liste navigieren, indem Sie auf den entsprechenden Eintrag im Fenster Formelprotokollierung doppelklicken. 
  
![](media/ShapeSheetDependents_UI_02_ZA01039815.gif)
  
## <a name="tracing-precendent-cells"></a>Verfolgen Precendent Zellen

Wenn eine Liste aller Zellen angezeigt werden soll, von denen eine bestimmte Zelle abhängt, wählen Sie zunächst die Zelle im ShapeSheet-Fenster aus. In diesem Beispiel ist die Zelle Geometry1.X2 ausgewählt. 
  
![](media/ShapeSheetPrecedents_UI_01_ZA01039817.gif)
  
Klicken Sie zum Anzeigen ihrer Vorgängerzellen klicken, in der Gruppe **Formelprotokollierung**auf **Spur zum Vorgänger**.
  
Eine Liste aller Zellen, die die Zelle Geometry1.X2 abhängig ist, wird im Fenster **Formelprotokollierung** angezeigt. Sie können auf eine beliebige Zelle in der Liste navigieren, indem Sie den Eintrag im Fenster **Formelprotokollierung** doppelklicken. 
  
![](media/ShapeSheetPrecedents_UI_02_ZA01039818.gif)
  

