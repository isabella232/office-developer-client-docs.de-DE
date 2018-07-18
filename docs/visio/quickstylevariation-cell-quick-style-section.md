---
title: QuickStyleVariation Cell (Quick Style Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: e3b58a19-9f1a-4f2b-9fe2-45cbb7ec6898
description: Bestimmt, ob die Formeln und die Werte der Text, Linie, innen und Füllung Farbe (oder eine Kombination dieser Eigenschaften) mithilfe von Farben außer Kraft setzen, Kontrast, wobei der Diagrammhintergrund. Wert ist eine bitweise OR 0, 1, 2, 4 und 8.
ms.openlocfilehash: fe6462798b61a0713f98196974876144cf4606e7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797763"
---
# <a name="quickstylevariation-cell-quick-style-section"></a>QuickStyleVariation Cell (Quick Style Section)

Bestimmt, ob die Formeln und die Werte der Text, Linie, innen und Füllung Farbe (oder eine Kombination dieser Eigenschaften) mithilfe von Farben außer Kraft setzen, Kontrast, wobei der Diagrammhintergrund. Wert ist eine bitweise OR 0, 1, 2, 4 und 8.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|0  <br/> |Text eines Shapes, Zeile oder Füllung Farbe (oder eine beliebige Kombination dieser Eigenschaften), um anhand der angegebenen Hintergrundfarbe des Designs sichtbar bleiben, werden nicht geändert werden.  <br/> |
|1  <br/> |Text eines Shapes, Zeile oder Füllung Farbe (oder eine beliebige Kombination dieser Eigenschaften), um anhand der angegebenen Hintergrundfarbe des Designs sichtbar bleiben, werden nicht geändert werden.  <br/> |
|2  <br/> |Textfarbe eines Shapes, zu ändern, wenn erforderlich ist, um anhand eines Designs gegebene Hintergrundfarbe sichtbar bleiben.  <br/> |
|4  <br/> |Linienfarbe eines Shapes, zu ändern, wenn erforderlich ist, um anhand eines Designs gegebene Hintergrundfarbe sichtbar bleiben.  <br/> |
|8  <br/> |Füllfarbe einer Form zu ändern, wenn erforderlich ist, um anhand eines Designs gegebene Hintergrundfarbe sichtbar bleiben.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Verwenden Sie die Zelle QuickStyleVariation, um Sichtbarkeit in Text oder Zeilen zu gewährleisten, wenn diese außerhalb alle sichtbaren Shape-Geometrie (beispielsweise in ein Shape, dessen TextBox-Objekt den unteren Rand der Form, wie in Netzwerkdiagramm ist) werden. Die Zelle Standardwert ist 0, was bedeutet, dass ihr Verhalten inaktiv ist. Ein anderer Wert löst die Zelle Verhalten.
  
Der Wert QuickStyleVariation überschreibt den Wert, der von der Funktion THEMEVAL erzeugt wird, während es in die Farbe "(Abschnitt" Character "), FillForegnd oder LineColor Zellen befindet (oder durch direkte Verweise auf diese drei Eigenschaften über THEMEVAL hergestellt (" CharacterColor"), THEMEVAL("FillColor") und THEMEVAL("LineColor")).
  
Zum Abrufen eines Verweises auf die Zelle **QuickStyleVariation** nach Namen aus einer anderen Formel durch Abrufen des Werts des **N** -Attributs eines Elements **Zelle** oder aus einem Programm mithilfe der **CellsU** -Eigenschaft, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |QuickStyleVariation  <br/> |
   
Wenn Sie einen Verweis auf die Zelle **QuickStyleVariation** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowQuickStyleProperties** <br/> |
|Zellenindex:  <br/> |**visQuickStyleVariation** <br/> |
   

