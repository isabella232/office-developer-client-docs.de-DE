---
title: Zelle "UIFormat" (Abschnitt "Text Fields")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1080
ms.localizationpriority: medium
ms.assetid: 0dddef20-c58e-2306-ab8e-6cac8e159f61
description: Bestimmt das Format eines eingefügten Felds in früheren Versionen von Visio vor Visio 2000.
ms.openlocfilehash: e94f2bf72a026450af93ce789e74b4652447d482
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59627212"
---
# <a name="uiformat-cell-text-fields-section"></a>Zelle "UIFormat" (Abschnitt "Text Fields")

Bestimmt das Format eines eingefügten Felds in früheren Versionen von Visio vor Visio 2000.
  
## <a name="remarks"></a>Bemerkungen

Diese Zelle wird im ShapeSheet-Fenster nicht angezeigt. Verwenden Sie diese Zelle, wenn es um die Abwärtskompatibilität geht, wie etwa beim Speichern einer Visio Version 2000-Zeichnung im Visio Version 5.0-Dateiformat.
  
Verwenden Sie Folgendes, um einen Verweis auf die ZELLE "UIFormat" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Fields.UIFmt[  *i*  ] where  *i*  = <1>, 2, 3...  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle "UIFormat" anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionTextField** <br/> |
| Zeilenindex:  <br/> |**visRowField**  +   *i* where *i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visFieldUIFormat** <br/> |
   

