---
title: Zelle "DrawingScale" (Abschnitt "Page Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm265
ms.localizationpriority: medium
ms.assetid: bc447f22-a188-2c61-e33c-df0d401a4725
description: Stellt den Wert der Zeichnungseinheit im aktuellen Zeichnungsmaßstab dar. Der Zeichnungsmaßstab für die Seite ist das Verhältnis der in der Zelle PageScale angezeigten Seiteneinheit zur in der Zelle DrawingScale angezeigten Zeichnungseinheit.
ms.openlocfilehash: f1e0ff314aea587334550568ae5067e3acdceec4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59586537"
---
# <a name="drawingscale-cell-page-properties-section"></a>Zelle "DrawingScale" (Abschnitt "Page Properties")

Stellt den Wert der Zeichnungseinheit im aktuellen Zeichnungsmaßstab dar. Der Zeichnungsmaßstab für die Seite ist das Verhältnis der in der Zelle PageScale angezeigten Seiteneinheit zur in der Zelle DrawingScale angezeigten Zeichnungseinheit.
  
Sie können die Zelle DrawingScale so festlegen, dass die Einheiten der Lineal eines Zeichenblatts aus einem Programm geändert werden. Nachfolgend sehen Sie ein Beispiel für das Ändern der Maßeinheiten von Zoll in Zentimeter aus einem Programm. In diesem Fall verwenden wir die **ConvertResult-Methode,** um den Abstand gleich zu halten, ihn jedoch in verschiedenen Einheiten auszudrücken. 
  
```vb
Public Sub SetActivePageMeasurementToCM() 
Dim dsCell As Visio.Cell 
Set dsCell = ActivePage.PageSheet.Cells("DrawingScale") 
 dsCell.Result(visCentimeters) = _ 
 Application.ConvertResult _ 
 (dsCell.ResultIU,visInches,visCentimeters) 
End Sub 
```

Sie können das Maßsystem in einer Zeichnung bestimmen, indem Sie **die** Units-Eigenschaft der Zelle DrawingScale untersuchen. Nach dem Ausführen des obigen Makros gibt die folgende Anweisung, die im direkt Visual Basic Editor-Fenster ausgeführt *wird, True* zurück. 
  
```vb
debug.print ActivePage.PageSheet.Cells("DrawingScale").Units = _ 
 visCentimeters 
```

## <a name="remarks"></a>HinwBemerkungeneise

Diese Zelle entspricht den Einstellungen im Dialogfeld **Seite einrichten** (klicken Sie auf der Registerkarte **Start** auf den Pfeil neben **Seite einrichten**). 
  
Die Einheiten der Formel in der Zelle DrawingScale bestimmen die Maßeinheiten für die Lineale im Zeichnungsfenster. Wenn Sie den Maßstab der Zeichnung ebenfalls nicht ändern möchten, gehen Sie wie folgt vor:
  
- Ändern Sie den in der Zelle DrawingScale aufgeführten Abstand nicht, sondern verwenden Sie andere Einheiten dafür.
    
- Ändern Sie den in der Zelle PageScale aufgeführten Abstand um denselben Faktor, den Sie zum Ändern von DrawingScale verwenden.
    
Verwenden Sie Folgendes, um einen Verweis auf die Zelle "DrawingScale" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |DrawingScale  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle DrawingScale anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowPage** <br/> |
|Zellenindex:  <br/> |**visPageDrawingScale** <br/> |
   

