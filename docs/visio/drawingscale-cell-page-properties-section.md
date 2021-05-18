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
# <a name="drawingscale-cell-page-properties-section"></a><span data-ttu-id="bec6f-104">Zelle "DrawingScale" (Abschnitt "Page Properties")</span><span class="sxs-lookup"><span data-stu-id="bec6f-104">DrawingScale Cell (Page Properties Section)</span></span>

<span data-ttu-id="bec6f-p102">Stellt den Wert der Zeichnungseinheit im aktuellen Zeichnungsmaßstab dar. Der Zeichnungsmaßstab für die Seite ist das Verhältnis der in der Zelle PageScale angezeigten Seiteneinheit zur in der Zelle DrawingScale angezeigten Zeichnungseinheit.</span><span class="sxs-lookup"><span data-stu-id="bec6f-p102">Represents the value of the drawing unit in the current drawing scale. The drawing scale for the page is the ratio of the page unit shown in the PageScale cell to the drawing unit shown in the DrawingScale cell.</span></span>
  
<span data-ttu-id="bec6f-107">Sie können die Zelle DrawingScale so festlegen, dass die Einheiten der Lineale einer Seite aus einem Programm geändert werden.</span><span class="sxs-lookup"><span data-stu-id="bec6f-107">You can set the DrawingScale cell to change the units of a page's rulers from a program.</span></span> <span data-ttu-id="bec6f-108">Hier ist ein Beispiel für das Ändern der Maßeinheiten von Zoll in Zentimeter aus einem Programm.</span><span class="sxs-lookup"><span data-stu-id="bec6f-108">Here is an example of changing the measurement units from inches to centimeters from a program.</span></span> <span data-ttu-id="bec6f-109">In diesem Fall verwenden wir die **ConvertResult-Methode,** um den Abstand gleich zu halten, aber in verschiedenen Einheiten ausdrücken.</span><span class="sxs-lookup"><span data-stu-id="bec6f-109">In this case, we use the **ConvertResult** method to keep the distance the same but express it in different units.</span></span> 
  
```vb
Public Sub SetActivePageMeasurementToCM() 
Dim dsCell As Visio.Cell 
Set dsCell = ActivePage.PageSheet.Cells("DrawingScale") 
 dsCell.Result(visCentimeters) = _ 
 Application.ConvertResult _ 
 (dsCell.ResultIU,visInches,visCentimeters) 
End Sub 
```

<span data-ttu-id="bec6f-110">Sie können das Maßsystem in einer Zeichnung bestimmen, indem Sie die **Units-Eigenschaft** der DrawingScale-Zelle untersuchen.</span><span class="sxs-lookup"><span data-stu-id="bec6f-110">You can determine the measurement system in a drawing by examining the **Units** property of the DrawingScale cell.</span></span> <span data-ttu-id="bec6f-111">Nach dem Ausführen des obigen Makros gibt die folgende Anweisung, die im Fenster Visual Basic Editor Direkt ausgeführt wird, *True zurück.*</span><span class="sxs-lookup"><span data-stu-id="bec6f-111">After running the above macro the following statement executed in the Visual Basic Editor Immediate window will return  *True*  .</span></span> 
  
```vb
debug.print ActivePage.PageSheet.Cells("DrawingScale").Units = _ 
 visCentimeters 
```

## <a name="remarks"></a><span data-ttu-id="bec6f-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="bec6f-112">Remarks</span></span>

<span data-ttu-id="bec6f-113">Diese Zelle entspricht den Einstellungen im Dialogfeld **Seite einrichten** (klicken Sie auf der Registerkarte **Start** auf den Pfeil neben **Seite einrichten**).</span><span class="sxs-lookup"><span data-stu-id="bec6f-113">This cell corresponds to the settings in the **Page Setup** dialog box (click the **Page Setup** arrow on the **Home** tab).</span></span> 
  
<span data-ttu-id="bec6f-p105">Die Einheiten der Formel in der Zelle DrawingScale bestimmen die Maßeinheiten für die Lineale im Zeichnungsfenster. Wenn Sie den Maßstab der Zeichnung ebenfalls nicht ändern möchten, gehen Sie wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="bec6f-p105">The units of the formula in the DrawingScale cell determine the measurement units used by the rulers in the drawing window. If you do not want to also change the drawing's scale, you can do one of the following:</span></span>
  
- <span data-ttu-id="bec6f-116">Ändern Sie den in der Zelle DrawingScale aufgeführten Abstand nicht, sondern verwenden Sie andere Einheiten dafür.</span><span class="sxs-lookup"><span data-stu-id="bec6f-116">Keep the distance expressed in the DrawingScale cell the same but express it in different units.</span></span>
    
- <span data-ttu-id="bec6f-117">Ändern Sie den in der Zelle PageScale aufgeführten Abstand um denselben Faktor, den Sie zum Ändern von DrawingScale verwenden.</span><span class="sxs-lookup"><span data-stu-id="bec6f-117">Change the distance expressed in the PageScale cell by the same factor that you change DrawingScale.</span></span>
    
<span data-ttu-id="bec6f-118">Verwenden Sie zum Erhalten eines Verweises auf die DrawingScale-Zelle anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft:**</span><span class="sxs-lookup"><span data-stu-id="bec6f-118">To get a reference to the DrawingScale cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bec6f-119">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="bec6f-119">Cell name:</span></span>  <br/> |<span data-ttu-id="bec6f-120">DrawingScale</span><span class="sxs-lookup"><span data-stu-id="bec6f-120">DrawingScale</span></span>  <br/> |
   
<span data-ttu-id="bec6f-121">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die DrawingScale-Zelle nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="bec6f-121">To get a reference to the DrawingScale cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bec6f-122">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="bec6f-122">Section index:</span></span>  <br/> |<span data-ttu-id="bec6f-123">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="bec6f-123">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="bec6f-124">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="bec6f-124">Row index:</span></span>  <br/> |<span data-ttu-id="bec6f-125">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="bec6f-125">**visRowPage**</span></span> <br/> |
|<span data-ttu-id="bec6f-126">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="bec6f-126">Cell index:</span></span>  <br/> |<span data-ttu-id="bec6f-127">**visPageDrawingScale**</span><span class="sxs-lookup"><span data-stu-id="bec6f-127">**visPageDrawingScale**</span></span> <br/> |
   

