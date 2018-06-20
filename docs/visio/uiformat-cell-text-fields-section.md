---
title: Zelle "UIFormat" (Abschnitt "Text Fields")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1080
localization_priority: Normal
ms.assetid: 0dddef20-c58e-2306-ab8e-6cac8e159f61
description: Bestimmt das Format eines eingefügten Felds in früheren Versionen von Visio vor Visio 2000.
ms.openlocfilehash: e9506404e8ccd6ae4452c10ecdcce2d4dfd7ac2a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798363"
---
# <a name="uiformat-cell-text-fields-section"></a>UIFormat Cell (Text Fields Section)

Bestimmt das Format eines eingefügten Felds in früheren Versionen von Visio vor Visio 2000.
  
## <a name="remarks"></a>Hinweise

Diese Zelle wird im ShapeSheet-Fenster nicht angezeigt. Verwenden Sie diese Zelle, wenn es um die Abwärtskompatibilität geht, wie etwa beim Speichern einer Visio Version 2000-Zeichnung im Visio Version 5.0-Dateiformat.
  
Wenn Sie einen Verweis auf die Zelle UIFormat nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Fields.UIFmt [ *i* ] wobei *i* = < 1 >, 2, 3...  <br/> |
   
Wenn Sie einen Verweis auf die Zelle UIFormat aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionTextField** <br/> |
| Zeilenindex:  <br/> |**VisRowField** +  *i* wobei *i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visFieldUIFormat** <br/> |
   

