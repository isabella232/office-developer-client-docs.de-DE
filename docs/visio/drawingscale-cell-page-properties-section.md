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
# <a name="drawingscale-cell-page-properties-section"></a><span data-ttu-id="d16e0-104">Zelle "DrawingScale" (Abschnitt "Page Properties")</span><span class="sxs-lookup"><span data-stu-id="d16e0-104">DrawingScale Cell (Page Properties Section)</span></span>

<span data-ttu-id="d16e0-p102">Stellt den Wert der Zeichnungseinheit im aktuellen Zeichnungsmaßstab dar. Der Zeichnungsmaßstab für die Seite ist das Verhältnis der in der Zelle PageScale angezeigten Seiteneinheit zur in der Zelle DrawingScale angezeigten Zeichnungseinheit.</span><span class="sxs-lookup"><span data-stu-id="d16e0-p102">Represents the value of the drawing unit in the current drawing scale. The drawing scale for the page is the ratio of the page unit shown in the PageScale cell to the drawing unit shown in the DrawingScale cell.</span></span>
  
<span data-ttu-id="d16e0-107">Sie können die Zelle DrawingScale so ändern Sie die Einheiten einer Seite Lineale aus einem Programm festlegen.</span><span class="sxs-lookup"><span data-stu-id="d16e0-107">You can set the DrawingScale cell to change the units of a page's rulers from a program.</span></span> <span data-ttu-id="d16e0-108">Hier ist ein Beispiel für die Maßeinheiten von Zoll in Zentimeter aus einem Programm ändern.</span><span class="sxs-lookup"><span data-stu-id="d16e0-108">Here is an example of changing the measurement units from inches to centimeters from a program.</span></span> <span data-ttu-id="d16e0-109">In diesem Fall verwenden wir die **ConvertResult** -Methode, lassen Sie dem Abstand identisch, ihn jedoch in anderen Einheiten.</span><span class="sxs-lookup"><span data-stu-id="d16e0-109">In this case, we use the **ConvertResult** method to keep the distance the same but express it in different units.</span></span> 
  
```vb
Public Sub SetActivePageMeasurementToCM() 
Dim dsCell As Visio.Cell 
Set dsCell = ActivePage.PageSheet.Cells("DrawingScale") 
 dsCell.Result(visCentimeters) = _ 
 Application.ConvertResult _ 
 (dsCell.ResultIU,visInches,visCentimeters) 
End Sub 
```

<span data-ttu-id="d16e0-110">Sie können das Maßsystem in einer Zeichnung durch Untersuchen der **Einheiten** -Eigenschaft der Zelle DrawingScale bestimmen.</span><span class="sxs-lookup"><span data-stu-id="d16e0-110">You can determine the measurement system in a drawing by examining the **Units** property of the DrawingScale cell.</span></span> <span data-ttu-id="d16e0-111">Nach dem Ausführen der oben genannten Makros ausgeführten, im Direktfenster Visual Basic-Editor mit der folgenden Anweisung wird das Fenster *True* zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d16e0-111">After running the above macro the following statement executed in the Visual Basic Editor Immediate window will return  *True*  .</span></span> 
  
```vb
debug.print ActivePage.PageSheet.Cells("DrawingScale").Units = _ 
 visCentimeters 
```

## <a name="remarks"></a><span data-ttu-id="d16e0-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d16e0-112">Remarks</span></span>

<span data-ttu-id="d16e0-113">Diese Zelle entspricht den Einstellungen im Dialogfeld **Seite einrichten** (klicken Sie auf den Pfeil neben **Seite einrichten** auf der Registerkarte **Start** ).</span><span class="sxs-lookup"><span data-stu-id="d16e0-113">This cell corresponds to the settings in the **Page Setup** dialog box (click the **Page Setup** arrow on the **Home** tab).</span></span> 
  
<span data-ttu-id="d16e0-p105">Die Einheiten der Formel in der Zelle DrawingScale bestimmen die Maßeinheiten für die Lineale im Zeichnungsfenster. Wenn Sie den Maßstab der Zeichnung ebenfalls nicht ändern möchten, gehen Sie wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="d16e0-p105">The units of the formula in the DrawingScale cell determine the measurement units used by the rulers in the drawing window. If you do not want to also change the drawing's scale, you can do one of the following:</span></span>
  
- <span data-ttu-id="d16e0-116">Ändern Sie den in der Zelle DrawingScale aufgeführten Abstand nicht, sondern verwenden Sie andere Einheiten dafür.</span><span class="sxs-lookup"><span data-stu-id="d16e0-116">Keep the distance expressed in the DrawingScale cell the same but express it in different units.</span></span>
    
- <span data-ttu-id="d16e0-117">Ändern Sie den in der Zelle PageScale aufgeführten Abstand um denselben Faktor, den Sie zum Ändern von DrawingScale verwenden.</span><span class="sxs-lookup"><span data-stu-id="d16e0-117">Change the distance expressed in the PageScale cell by the same factor that you change DrawingScale.</span></span>
    
<span data-ttu-id="d16e0-118">Wenn Sie einen Verweis auf die Zelle DrawingScale nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="d16e0-118">To get a reference to the DrawingScale cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d16e0-119">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="d16e0-119">Cell name:</span></span>  <br/> |<span data-ttu-id="d16e0-120">DrawingScale</span><span class="sxs-lookup"><span data-stu-id="d16e0-120">DrawingScale</span></span>  <br/> |
   
<span data-ttu-id="d16e0-121">Wenn Sie einen Verweis auf die Zelle DrawingScale aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="d16e0-121">To get a reference to the DrawingScale cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d16e0-122">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="d16e0-122">Section index:</span></span>  <br/> |<span data-ttu-id="d16e0-123">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="d16e0-123">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="d16e0-124">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="d16e0-124">Row index:</span></span>  <br/> |<span data-ttu-id="d16e0-125">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="d16e0-125">**visRowPage**</span></span> <br/> |
|<span data-ttu-id="d16e0-126">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="d16e0-126">Cell index:</span></span>  <br/> |<span data-ttu-id="d16e0-127">**visPageDrawingScale**</span><span class="sxs-lookup"><span data-stu-id="d16e0-127">**visPageDrawingScale**</span></span> <br/> |
   

