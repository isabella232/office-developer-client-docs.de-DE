---
title: RelLineTo Row (Geometry Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a900e174-d26a-4314-ae4f-d89e186350ce
description: Enthält x - und y-Koordinaten des Endscheitelpunkts eines geraden Linienabschnitts relativ zur Breite und Höhe des Shapes.
ms.openlocfilehash: 26cb63ac6cc0708be4e5668174022af63391c129
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797810"
---
# <a name="rellineto-row-geometry-section"></a>RelLineTo Row (Geometry Section)

Enthält die *X* - und *y* -Koordinaten des Endscheitelpunkts eines geraden Linienabschnitts relativ zur Breite und Höhe des Shapes. 
  
> [!NOTE]
> Eine Zeile **RelLineTo** kann nur in den Dateiformaten .vsdx, .vsdm, .vstx, .vstm, .vssx und .vssm beibehalten werden. Wenn eine Datei in das Visio 2003-2010-Formate gespeichert wird, wird die Zeile **RelLineTo** in eine Zeile [LineTo](lineto-row-geometry-section.md) konvertiert. 
  
Eine Zeile **RelLineTo** enthält folgende Zellen. 
  
|**Cell**|**Beschreibung**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |Die *X* -Koordinate des Endscheitelpunkts eines geraden Linienabschnitts relativ zu der Breite des Shapes.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |Die *y* -Koordinate des Endscheitelpunkts eines geraden Linienabschnitts relativ zur Höhe des Shapes.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Werte in der Zeile **RelLineTo** entsprechen Werte in einer [LineTo](lineto-row-geometry-section.md) -Zeile, die die Breite und Höhe des Shapes multipliziert werden. Beispiel: eine Zeile **RelLineTo** , in denen der Wert der Zelle **X** ist "0" und der Wert der Zelle **Y** ist "0,5" kann mit der Zeile " **LineTo"** , in dem der Wert der Zelle **X** die Formel lautet, ersetzt werden "Breite*0" und die Zelle **Y** ist die Formel "Höhe*0,5." 
  

