---
title: Zelle "UICode" (Abschnitt "Text Fields")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1075
localization_priority: Normal
ms.assetid: 1d9717c1-4310-0d62-874f-4df77cd81627
description: Bestimmt den Code eines eingefügten Felds in früheren Versionen von Visio vor Visio 2000.
ms.openlocfilehash: ce05f779bfebd5720555f1a2d92b1f9f92cfbdfd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798340"
---
# <a name="uicode-cell-text-fields-section"></a>UICode Cell (Text Fields Section)

Bestimmt den Code eines eingefügten Felds in früheren Versionen von Visio vor Visio 2000.
  
## <a name="remarks"></a>Hinweise

Diese Zelle wird im ShapeSheet-Fenster nicht angezeigt. Verwenden Sie diese Zelle, wenn es um die Abwärtskompatibilität geht, wie etwa beim Speichern einer Visio Version 2000-Zeichnung im Visio Version 5.0-Dateiformat.
  
Wenn Sie einen Verweis auf die Zelle UICode nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Fields.UICod [ *i* ] wobei *i* = < 1 >, 2, 3...  <br/> |
   
Wenn Sie einen Verweis auf die Zelle UICode aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionTextField** <br/> |
| Zeilenindex:  <br/> |**VisRowField** +  *i* wobei *i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visFieldUICode** <br/> |
   

