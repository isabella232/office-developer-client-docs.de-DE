---
title: Zelle "DrawingScaleType" (Abschnitt "Page Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm270
ms.localizationpriority: medium
ms.assetid: 5d4f1cf8-bc1f-07b8-1da5-7253808e337e
description: Legt den im Dialogfeld Seite einrichten ausgewählten Zeichnungsmaßstab fest (klicken Sie auf der Registerkarte Start auf den Pfeil neben Seite einrichten).
ms.openlocfilehash: 9cd48ab970b9de0987c655705cc86060ced5cbdb
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59590233"
---
# <a name="drawingscaletype-cell-page-properties-section"></a>Zelle "DrawingScaleType" (Abschnitt "Page Properties")

Legt den im Dialogfeld **Seite einrichten** ausgewählten Zeichnungsmaßstab fest (klicken Sie auf der Registerkarte **Start** auf den Pfeil neben **Seite einrichten**). 
  
|**Wert**|**Beschreibung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
| 0  <br/> | Kein Maßstab  <br/> |**visNoScale** <br/> |
| 1  <br/> | Architekturmaßstab  <br/> |**visArchitectural** <br/> |
| 2  <br/> | Tiefbaumaßstab  <br/> |**visEngineering** <br/> |
| 3  <br/> | Benutzerdefinierter Maßstab  <br/> |**visScaleCustom** <br/> |
| 4   <br/> | Metrik  <br/> |**visScaleMetric** <br/> |
| 5  <br/> | Maschinenbaumaßstab  <br/> |**visScaleMeical** <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Verwenden Sie Folgendes, um einen Verweis auf die Zelle DrawingScaleType anhand des Namens einer anderen Formel oder eines Programms mithilfe der **CellsU-Eigenschaft** abzurufen: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | DrawingScaleType  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle DrawingScaleType anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowPage** <br/> |
| Zellenindex:  <br/> |**visPageDrawScaleType** <br/> |
   

