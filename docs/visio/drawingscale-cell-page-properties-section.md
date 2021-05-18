---
title: Zelle "DrawingScale" (Abschnitt "Page Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm265
localization_priority: Normal
ms.assetid: bc447f22-a188-2c61-e33c-df0d401a4725
description: Stellt den Wert der Zeichnungseinheit im aktuellen Zeichnungsmaßstab dar. Der Zeichnungsmaßstab für die Seite ist das Verhältnis der in der Zelle PageScale angezeigten Seiteneinheit zur in der Zelle DrawingScale angezeigten Zeichnungseinheit.
ms.openlocfilehash: 8a3a5f93ff096e42ba3c13b671b46bf1cf97df82
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413318"
---
# <a name="drawingscale-cell-page-properties-section"></a>Zelle "DrawingScale" (Abschnitt "Page Properties")

Stellt den Wert der Zeichnungseinheit im aktuellen Zeichnungsmaßstab dar. Der Zeichnungsmaßstab für die Seite ist das Verhältnis der in der Zelle PageScale angezeigten Seiteneinheit zur in der Zelle DrawingScale angezeigten Zeichnungseinheit.
  
Sie können die Zelle DrawingScale so festlegen, dass die Einheiten der Lineale einer Seite aus einem Programm geändert werden. Hier ist ein Beispiel für das Ändern der Maßeinheiten von Zoll in Zentimeter aus einem Programm. In diesem Fall verwenden wir die **ConvertResult-Methode,** um den Abstand gleich zu halten, aber in verschiedenen Einheiten ausdrücken. 
  
```vb
Public Sub SetActivePageMeasurementToCM() 
Dim dsCell As Visio.Cell 
Set dsCell = ActivePage.PageSheet.Cells("DrawingScale") 
 dsCell.Result(visCentimeters) = _ 
 Application.ConvertResult _ 
 (dsCell.ResultIU,visInches,visCentimeters) 
End Sub 
```

Sie können das Maßsystem in einer Zeichnung bestimmen, indem Sie die **Units-Eigenschaft** der DrawingScale-Zelle untersuchen. Nach dem Ausführen des obigen Makros gibt die folgende Anweisung, die im Fenster Visual Basic Editor Direkt ausgeführt wird, *True zurück.* 
  
```vb
debug.print ActivePage.PageSheet.Cells("DrawingScale").Units = _ 
 visCentimeters 
```

## <a name="remarks"></a>Hinweise

Diese Zelle entspricht den Einstellungen im Dialogfeld **Seite einrichten** (klicken Sie auf der Registerkarte **Start** auf den Pfeil neben **Seite einrichten**). 
  
Die Einheiten der Formel in der Zelle DrawingScale bestimmen die Maßeinheiten für die Lineale im Zeichnungsfenster. Wenn Sie den Maßstab der Zeichnung ebenfalls nicht ändern möchten, gehen Sie wie folgt vor:
  
- Ändern Sie den in der Zelle DrawingScale aufgeführten Abstand nicht, sondern verwenden Sie andere Einheiten dafür.
    
- Ändern Sie den in der Zelle PageScale aufgeführten Abstand um denselben Faktor, den Sie zum Ändern von DrawingScale verwenden.
    
Verwenden Sie zum Erhalten eines Verweises auf die DrawingScale-Zelle anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft:** 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |DrawingScale  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die DrawingScale-Zelle nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowPage** <br/> |
|Zellenindex:  <br/> |**visPageDrawingScale** <br/> |
   

