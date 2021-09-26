---
title: Zelle "UICategory" (Abschnitt "Text Fields")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1070
ms.localizationpriority: medium
ms.assetid: 365f7005-ba34-2311-4c5c-16344962fc3f
description: Bestimmt die Kategorie eines eingefügten Felds in Versionen von Visio vor Visio 2000.
ms.openlocfilehash: c7733b73338fabee3759169cce9374f8d56bbf1e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59627221"
---
# <a name="uicategory-cell-text-fields-section"></a>Zelle "UICategory" (Abschnitt "Text Fields")

Bestimmt die Kategorie eines eingefügten Felds in Versionen von Visio vor Visio 2000.
  
## <a name="remarks"></a>Bemerkungen

Diese Zelle wird im ShapeSheet-Fenster nicht angezeigt. Verwenden Sie bezüglich der Abwärtskompatibilität diese Zelle, wie etwa beim Speichern einer Visio Version 2000-Zeichnung im Visio Version 5.0-Dateiformat.
  
Um einen Verweis auf die Zelle "UICategory" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Fields.UICat[  *i*  ] where  *i*  = <1>, 2, 3...  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle "UICategory" anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionTextField** <br/> |
| Zeilenindex:  <br/> |**visRowField**  +   *i* where *i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visFieldUICategory** <br/> |
   

