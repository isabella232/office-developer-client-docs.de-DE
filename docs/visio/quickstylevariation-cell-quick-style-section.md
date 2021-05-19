---
title: Zelle "QuickStyleVariation" (Abschnitt "Quick Style")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: e3b58a19-9f1a-4f2b-9fe2-45cbb7ec6898
description: Bestimmt, ob die Formeln und Werte der Text-, Linien- und Füllfarbe (oder einer Kombination dieser Eigenschaften) mithilfe von Farben überschrieben werden, die mit dem Diagrammhintergrund kontrastieren. Der Wert ist ein bitweiser OR-Wert von 0, 1, 2, 4 und 8.
ms.openlocfilehash: 736e2287c00c24774ef8b677613235d642697f4b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433794"
---
# <a name="quickstylevariation-cell-quick-style-section"></a>Zelle "QuickStyleVariation" (Abschnitt "Quick Style")

Bestimmt, ob die Formeln und Werte der Text-, Linien- und Füllfarbe (oder einer Kombination dieser Eigenschaften) mithilfe von Farben überschrieben werden, die mit dem Diagrammhintergrund kontrastieren. Der Wert ist ein bitweiser OR-Wert von 0, 1, 2, 4 und 8.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|0  <br/> |Ändern Sie die Text-, Linien- oder Füllfarbe eines Shapes (oder eine Kombination dieser Eigenschaften) nicht, um für die angegebene Hintergrundfarbe eines Designs sichtbar zu bleiben.  <br/> |
|1  <br/> |Ändern Sie die Text-, Linien- oder Füllfarbe eines Shapes (oder eine Kombination dieser Eigenschaften) nicht, um für die angegebene Hintergrundfarbe eines Designs sichtbar zu bleiben.  <br/> |
|2  <br/> |Ändern Sie gegebenenfalls die Textfarbe eines Shapes, um für die angegebene Hintergrundfarbe eines Designs sichtbar zu bleiben.  <br/> |
|4   <br/> |Ändern Sie gegebenenfalls die Linienfarbe eines Shapes, um für die angegebene Hintergrundfarbe eines Designs sichtbar zu bleiben.  <br/> |
|8   <br/> |Ändern Sie die Füllfarbe eines Shapes, um bei Bedarf für die angegebene Hintergrundfarbe eines Designs sichtbar zu bleiben.  <br/> |
   
## <a name="remarks"></a>Hinweise

Verwenden Sie die Zelle QuickStyleVariation, um die Sichtbarkeit in Text oder Zeilen zu gewährleisten, wenn sie sich außerhalb einer sichtbaren Formgeometrie befinden (z. B. in einer Form, deren Textfeld sich unterhalb des unteren Rands der Form befindet, z. B. in Netzwerkdiagrammen). Der Standardwert der Zelle ist 0, was bedeutet, dass ihr Verhalten inaktiv ist. Jeder andere Wert löst das Verhalten der Zelle aus.
  
Der QuickStyleVariation-Wert überschreibt den von der THEMEVAL-Funktion erzeugten Wert, wenn er sich in den Zellen Color (Character Section), FillForegnd oder LineColor befindet (oder durch direkte Verweise auf diese drei Eigenschaften durch THEMEVAL("CharacterColor"), THEMEVAL("FillColor") und THEMEVAL("LineColor")) erzeugt wird.
  
Verwenden Sie zum Abrufen eines Verweises auf die **QuickStyleVariation-Zelle** anhand des Namens aus einer anderen Formel, indem Sie den Wert des **N-Attributs** eines **Cell-Elements** oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abrufen: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |QuickStyleVariation  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die **QuickStyleVariation-Zelle** nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowQuickStyleProperties** <br/> |
|Zellenindex:  <br/> |**visQuickStyleVariation** <br/> |
   

