---
title: Zelle "QuickStyleVariation" (Abschnitt "Quick Style")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: e3b58a19-9f1a-4f2b-9fe2-45cbb7ec6898
description: Bestimmt, ob die Formeln und Werte der Text-, Linien- und Füllfarbe (oder eine Kombination dieser Eigenschaften) mithilfe von Farben überschrieben werden, die mit dem Diagrammhintergrund in Kontrast stehen. Der Wert ist bitweise OR von 0, 1, 2, 4 und 8.
ms.openlocfilehash: 19936c4c1211c4202f52d1c8446d6b45ff5cbe83
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59607934"
---
# <a name="quickstylevariation-cell-quick-style-section"></a>Zelle "QuickStyleVariation" (Abschnitt "Quick Style")

Bestimmt, ob die Formeln und Werte der Text-, Linien- und Füllfarbe (oder eine Kombination dieser Eigenschaften) mithilfe von Farben überschrieben werden, die mit dem Diagrammhintergrund in Kontrast stehen. Der Wert ist bitweise OR von 0, 1, 2, 4 und 8.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|0  <br/> |Ändern Sie nicht die Text-, Linien- oder Füllfarbe einer Form (oder eine Beliebige Kombination dieser Eigenschaften), damit sie für die angegebene Hintergrundfarbe eines Designs sichtbar bleibt.  <br/> |
|1  <br/> |Ändern Sie nicht die Text-, Linien- oder Füllfarbe einer Form (oder eine Beliebige Kombination dieser Eigenschaften), damit sie für die angegebene Hintergrundfarbe eines Designs sichtbar bleibt.  <br/> |
|2  <br/> |Ändern Sie die Textfarbe einer Form, falls erforderlich, so, dass sie für die angegebene Hintergrundfarbe eines Designs sichtbar bleibt.  <br/> |
|4   <br/> |Ändern Sie die Linienfarbe einer Form, falls erforderlich, so, dass sie für die angegebene Hintergrundfarbe eines Designs sichtbar bleibt.  <br/> |
|8   <br/> |Ändern Sie die Füllfarbe einer Form, um bei Bedarf für die angegebene Hintergrundfarbe eines Designs sichtbar zu bleiben.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Verwenden Sie die Zelle QuickStyleVariation, um die Sichtbarkeit in Text oder Linien zu gewährleisten, wenn sie sich außerhalb sichtbarer Shape-Geometrie befinden (z. B. in einem Shape, dessen Textfeld sich unterhalb des Unterrands des Shapes befindet, z. B. in Netzplandiagrammen). Der Standardwert der Zelle ist 0, was bedeutet, dass das Verhalten inaktiv ist. Ein anderer Wert löst das Verhalten der Zelle aus.
  
Der QuickStyleVariation-Wert überschreibt den von der THEMEVAL-Funktion erzeugten Wert, wenn er sich in den Zellen Color (Character Section), FillForegnd oder LineColor befindet (oder durch direkte Verweise auf diese drei Eigenschaften mithilfe von THEMEVAL("CharacterColor"), THEMEVAL("FillColor") und THEMEVAL("LineColor")) erzeugt wird.
  
Verwenden Sie zum Abrufen eines Verweises auf die **QuickStyleVariation-Zelle** anhand des Namens aus einer anderen Formel, durch Abrufen des Werts des **N-Attributs** eines **Cell-Elements** oder eines Programms mithilfe der **CellsU-Eigenschaft** Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |QuickStyleVariation  <br/> |
   
Um einen Verweis auf die **Zelle "QuickStyleVariation"** anhand des Indexes eines Programms abzurufen, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowQuickStyleProperties** <br/> |
|Zellenindex:  <br/> |**visQuickStyleVariation** <br/> |
   

