---
title: QuickStyleLineColor Cell (Quick Style section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: dcfb792f-e02a-4059-acec-a178d221097c
description: Bestimmt die Design Farbe, die die Linien einer Form verwenden, als ganze Zahl zwischen 0 und 7.
ms.openlocfilehash: 010b943f2266b1e0ee192e5f1341d73851d176fd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437043"
---
# <a name="quickstylelinecolor-cell-quick-style-section"></a>QuickStyleLineColor Cell (Quick Style section)

Bestimmt die Design Farbe, die die Linien einer Form verwenden, als ganze Zahl zwischen 0 und 7.
  
|||
|:-----|:-----|
|Wert  <br/> |Beschreibung  <br/> |
|0  <br/> |Die Farbe der Shape-Linien erbt von der dunklen Design Farbe.  <br/> |
|1  <br/> |Die Farbe der Shape-Linien erbt von der Farbe des hellen Designs.  <br/> |
|2  <br/> |Die Farbe der Shape-Linien erbt von der Design Farbe Akzent 1.  <br/> |
|3  <br/> |Die Farbe der Shape-Linien erbt von der Design Farbe Akzent 2.  <br/> |
|4  <br/> |Die Farbe der Shape-Linien erbt von der Design Farbe Akzent 3.  <br/> |
|5  <br/> |Die Farbe der Shape-Linien erbt von der Design Farbe Akzent 4.  <br/> |
|6  <br/> |Die Farbe der Shape-Linien erbt von der Design Farbe Akzent 5.  <br/> |
|7  <br/> |Die Farbe der Shape-Linien erbt von der Design Farbe Akzent 6.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle **QuickStyleLineColor** aus einer anderen Formel, nach dem Wert des **N** -Attributs eines **Cell** -Elements oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | QuickStyleLineColor  <br/> |
   
Wenn Sie einen Verweis auf die Zelle **QuickStyleLineColor** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowQuickStyleProperties** <br/> |
| Zellenindex:  <br/> |**visQuickStyleLineColor** <br/> |
   

