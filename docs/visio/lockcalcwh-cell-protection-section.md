---
title: Zelle "LockCalcWH" (Abschnitt "Protection")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm605
localization_priority: Normal
ms.assetid: 6eb51e5a-03d8-3daa-b4e1-6107d540aed9
description: Sperrt das Auswahlrechteck eines Shapes, damit dieses nicht neu berechnet wird, wenn ein Scheitelpunkt bearbeitet oder ein Zeilentyp im Abschnitt Geometry geändert wird.
ms.openlocfilehash: f7f9c99eb4978e9b32968d3076b0341efe42faa6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797365"
---
# <a name="lockcalcwh-cell-protection-section"></a>LockCalcWH Cell (Protection Section)

Sperrt das Auswahlrechteck eines Shapes, damit dieses nicht neu berechnet wird, wenn ein Scheitelpunkt bearbeitet oder ein Zeilentyp im Abschnitt Geometry geändert wird.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
| TRUE  <br/> | Breite und Höhe können nicht neu berechnet werden.  <br/> |
| FALSE  <br/> | Breite und Höhe können neu berechnet werden.  <br/> |
   
## <a name="remarks"></a>Hinweise

Wenn Sie einen Verweis auf die Zelle LockCalcWH aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | LockCalcWH  <br/> |
   
Wenn Sie einen Verweis auf die Zelle LockCalcWH aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowLock** <br/> |
| Zellenindex:  <br/> |**visLockCalcWH** <br/> |
   

