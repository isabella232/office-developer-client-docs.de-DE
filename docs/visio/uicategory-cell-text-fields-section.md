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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331199"
---
# <a name="uicategory-cell-text-fields-section"></a>Zelle "UICategory" (Abschnitt "Text Fields")

Bestimmt die Kategorie eines eingefügten Felds in Versionen von Visio vor Visio 2000.
  
## <a name="remarks"></a>Bemerkungen

Diese Zelle wird im ShapeSheet-Fenster nicht angezeigt. Verwenden Sie bezüglich der Abwärtskompatibilität diese Zelle, wie etwa beim Speichern einer Visio Version 2000-Zeichnung im Visio Version 5.0-Dateiformat.
  
Wenn Sie einen Verweis auf die Zelle Zelle UICategory aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Fields. UICategory [ *i* ] wobei *i* = <1>, 2, 3...  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Zelle UICategory aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionTextField** <br/> |
| Zeilenindex:  <br/> |**visRowField** +  *i* , wobei *i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visFieldUICategory** <br/> |
   

