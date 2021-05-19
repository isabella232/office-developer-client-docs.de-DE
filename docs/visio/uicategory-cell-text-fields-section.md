---
title: Zelle "UICategory" (Abschnitt "Text Fields")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1070
localization_priority: Normal
ms.assetid: 365f7005-ba34-2311-4c5c-16344962fc3f
description: Bestimmt die Kategorie eines eingefügten Felds in Versionen von Visio vor Visio 2000.
ms.openlocfilehash: c67ced9e4f731e66bce0589929ac90fb9bb8d67c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434025"
---
# <a name="uicategory-cell-text-fields-section"></a>Zelle "UICategory" (Abschnitt "Text Fields")

Bestimmt die Kategorie eines eingefügten Felds in Versionen von Visio vor Visio 2000.
  
## <a name="remarks"></a>Hinweise

Diese Zelle wird im ShapeSheet-Fenster nicht angezeigt. Verwenden Sie bezüglich der Abwärtskompatibilität diese Zelle, wie etwa beim Speichern einer Visio Version 2000-Zeichnung im Visio Version 5.0-Dateiformat.
  
Um einen Verweis auf die Zelle UICategory anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Fields.UICat[  *i*  ] where  *i*  = <1>, 2, 3...  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle UICategory nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionTextField** <br/> |
| Zeilenindex:  <br/> |**visRowField**  +   *i,* *wobei i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visFieldUICategory** <br/> |
   

