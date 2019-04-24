---
title: Zelle "DrawingScaleType" (Abschnitt "Page Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm270
localization_priority: Normal
ms.assetid: 5d4f1cf8-bc1f-07b8-1da5-7253808e337e
description: Legt den im Dialogfeld Seite einrichten ausgewählten Zeichnungsmaßstab fest (klicken Sie auf der Registerkarte Start auf den Pfeil neben Seite einrichten).
ms.openlocfilehash: d1c1c00ffe025c566646a1f8b9fe034732ad86a8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359689"
---
# <a name="drawingscaletype-cell-page-properties-section"></a>Zelle "DrawingScaleType" (Abschnitt "Page Properties")

Legt den im Dialogfeld **Seite einrichten** ausgewählten Zeichnungsmaßstab fest (klicken Sie auf der Registerkarte **Start** auf den Pfeil neben **Seite einrichten**). 
  
|**Wert**|**Beschreibung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
| 0  <br/> | Kein Maßstab  <br/> |**visNoScale** <br/> |
| 1  <br/> | Architekturmaßstab  <br/> |**visArchitectural** <br/> |
| 2  <br/> | Tiefbaumaßstab  <br/> |**visEngineering** <br/> |
| 3  <br/> | Benutzerdefinierter Maßstab  <br/> |**visScaleCustom** <br/> |
| 4  <br/> | Metrik  <br/> |**visScaleMetric** <br/> |
| 5  <br/> | Maschinenbaumaßstab  <br/> |**visScaleMechanical** <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle "DrawingScaleType aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | "DrawingScaleType  <br/> |
   
Wenn Sie einen Verweis auf die Zelle "DrawingScaleType aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowPage** <br/> |
| Zellenindex:  <br/> |**visPageDrawScaleType** <br/> |
   

