---
title: QuickStyleVariation Cell (Quick Style section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: e3b58a19-9f1a-4f2b-9fe2-45cbb7ec6898
description: Bestimmt, ob die Formeln und Werte der Text-, Linien-und Füllfarbe (oder einer Kombination dieser Eigenschaften) mithilfe von Farben außer Kraft gesetzt werden, die mit dem Diagrammhintergrund in Kontrast stehen. Der Wert ist ein bitweises OR von 0, 1, 2, 4 und 8.
ms.openlocfilehash: 736e2287c00c24774ef8b677613235d642697f4b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360014"
---
# <a name="quickstylevariation-cell-quick-style-section"></a>QuickStyleVariation Cell (Quick Style section)

Bestimmt, ob die Formeln und Werte der Text-, Linien-und Füllfarbe (oder einer Kombination dieser Eigenschaften) mithilfe von Farben außer Kraft gesetzt werden, die mit dem Diagrammhintergrund in Kontrast stehen. Der Wert ist ein bitweises OR von 0, 1, 2, 4 und 8.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|0  <br/> |Ändern Sie die Text-, Linien-oder Füllfarbe einer Form (oder eine Kombination dieser Eigenschaften) nicht so, dass Sie für die Hintergrundfarbe eines Designs sichtbar bleibt.  <br/> |
|1  <br/> |Ändern Sie die Text-, Linien-oder Füllfarbe einer Form (oder eine Kombination dieser Eigenschaften) nicht so, dass Sie für die Hintergrundfarbe eines Designs sichtbar bleibt.  <br/> |
|2  <br/> |Ändern Sie bei Bedarf die Textfarbe eines Shapes, damit es für die Hintergrundfarbe eines Designs sichtbar bleibt.  <br/> |
|4  <br/> |Ändern Sie bei Bedarf die Linienfarbe eines Shapes, damit es für die Hintergrundfarbe eines Designs sichtbar bleibt.  <br/> |
|8  <br/> |Ändern Sie bei Bedarf die Füllfarbe einer Form, um Sie für die Hintergrundfarbe eines Designs sichtbar zu machen.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Verwenden Sie die Zelle QuickStyleVariation, um die Sichtbarkeit von Text oder Zeilen zu gewährleisten, wenn Sie sich außerhalb einer sichtbaren Formen Geometrie befinden (beispielsweise in einem Shape, dessen TextBox sich unter dem unteren Rand der Form befindet, beispielsweise in Netzplänen). Der Standardwert der Zelle ist 0, was bedeutet, dass das Verhalten inaktiv ist. Jeder andere Wert löst das Verhalten der Zelle aus.
  
Der QuickStyleVariation-Wert überschreibt den von der THEMEVAL-Funktion erzeugten Wert, wenn er sich in den Zellen Color (Character section), Zelle FillForegnd oder Zelle LineColor (oder durch direkte Verweise auf diese drei Eigenschaften mittels THEMEVAL) befindet. Zu benutzende "), THEMEVAL (" FillColor ") und THEMEVAL (" Zelle LineColor ")).
  
Wenn Sie einen Verweis auf die Zelle **QuickStyleVariation** aus einer anderen Formel nach Namen erhalten möchten, indem Sie den Wert des **N** -Attributs eines **Cell** -Elements oder mithilfe der **CellsU** -Eigenschaft aus einem Programm abrufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |QuickStyleVariation  <br/> |
   
Wenn Sie einen Verweis auf die Zelle **QuickStyleVariation** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowQuickStyleProperties** <br/> |
|Zellenindex:  <br/> |**visQuickStyleVariation** <br/> |
   

