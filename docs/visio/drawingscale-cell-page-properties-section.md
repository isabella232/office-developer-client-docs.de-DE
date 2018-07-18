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
ms.openlocfilehash: cdd3222f5e56c34ac8947c9ef5a653cfe19fbd0f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796887"
---
# <a name="drawingscale-cell-page-properties-section"></a>DrawingScale Cell (Page Properties Section)

Stellt den Wert der Zeichnungseinheit im aktuellen Zeichnungsmaßstab dar. Der Zeichnungsmaßstab für die Seite ist das Verhältnis der in der Zelle PageScale angezeigten Seiteneinheit zur in der Zelle DrawingScale angezeigten Zeichnungseinheit.
  
Sie können die Zelle DrawingScale so festlegen, dass die Einheiten eines Seitenlineals von einem Programm geändert werden. Nachfolgend finden Sie ein Beispiel zum Ändern der Maßeinheiten von Zoll in Zentimeter durch ein Programm. In diesem Fall wird die ConvertResult-Methode verwendet, um den Abstand unverändert zu lassen, ihn jedoch in anderen Einheiten anzugeben. 
  
```vb
Public Sub SetActivePageMeasurementToCM() 
Dim dsCell As Visio.Cell 
Set dsCell = ActivePage.PageSheet.Cells("DrawingScale") 
 dsCell.Result(visCentimeters) = _ 
 Application.ConvertResult _ 
 (dsCell.ResultIU,visInches,visCentimeters) 
End Sub 
```

Sie können das Maßsystem in einer Zeichnung durch Untersuchen der **Einheiten** -Eigenschaft der Zelle DrawingScale bestimmen. Nach dem Ausführen der oben genannten Makros ausgeführten, im Direktfenster Visual Basic-Editor mit der folgenden Anweisung wird das Fenster *True* zurückgegeben. 
  
```vb
debug.print ActivePage.PageSheet.Cells("DrawingScale").Units = _ 
 visCentimeters 
```

## <a name="remarks"></a>Bemerkungen

Diese Zelle entspricht den Einstellungen im Dialogfeld **Seite einrichten** (klicken Sie auf der Registerkarte **Start** auf den Pfeil neben **Seite einrichten**). 
  
Die Einheiten der Formel in der Zelle DrawingScale bestimmen die Maßeinheiten für die Lineale im Zeichnungsfenster. Wenn Sie den Maßstab der Zeichnung ebenfalls nicht ändern möchten, gehen Sie wie folgt vor:
  
- Ändern Sie den in der Zelle DrawingScale aufgeführten Abstand nicht, sondern verwenden Sie andere Einheiten dafür.
    
- Ändern Sie den in der Zelle PageScale aufgeführten Abstand um denselben Faktor, den Sie zum Ändern von DrawingScale verwenden.
    
Wenn Sie einen Verweis auf die Zelle DrawingScale aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |DrawingScale  <br/> |
   
Wenn Sie einen Verweis auf die Zelle DrawingScale aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowPage** <br/> |
|Zellenindex:  <br/> |**visPageDrawingScale** <br/> |
   

