---
title: Wird Display Mode Cell (Action Tags section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60039
localization_priority: Normal
ms.assetid: 0dfad40b-f97e-0c4a-2102-7344d1317b82
description: Bestimmt, ob das Aktionstag angezeigt wird, wenn der Benutzer den Mauszeiger über das Tag bewegt, wenn das Shape ausgewählt ist, oder die ganze Zeit.
ms.openlocfilehash: 0254ad361c63dfdeddaf8a1c2173e99aa1c05398
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415817"
---
# <a name="displaymode-cell-action-tags-section"></a>Wird Display Mode Cell (Action Tags section)

Bestimmt, ob das Aktionstag angezeigt wird, wenn der Benutzer den Mauszeiger über das Tag bewegt, wenn das Shape ausgewählt ist, oder die ganze Zeit.
  
> [!NOTE]
> In früheren Versionen von Microsoft Visio werden Aktionstags als Smarttags bezeichnet. 
  
|**Wert**|**Anzeigemodus**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
| 0  <br/> | Wird angezeigt, wenn die Maus über dem Tag angehalten wird (Standardeinstellung).  <br/> |**visSmartTagDispModeMouseOver** <br/> |
| 1  <br/> | Wird angezeigt, wenn das Shape ausgewählt ist.  <br/> |**visSmartTagDispModeShapeSelected** <br/> |
| 2  <br/> | Wird immer angezeigt.  <br/> |**visSmartTagDispModeAlways** <br/> |
   
## <a name="remarks"></a>Bemerkungen

Aktionstags werden nicht in gedruckten oder veröffentlichten Ausgaben angezeigt. 
  
Wenn für ein Zeichenblatt ein Aktionstag definiert ist und die Zelle den Wert 1 aufweist, wird das Tag nie angezeigt, weil ein Zeichenblatt nicht ausgewählt werden kann. 
  
Wenn Sie einen Verweis auf die Zelle wird Display Mode aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Smarttags.  *Name* . Wird Display Mode, wobei SmartTags. *Name* ist der Name der Zeile mit dem Aktionstag.  <br/> |
   
Wenn Sie einen Verweis auf die Zelle wird Display Mode aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionSmartTag** <br/> |
| Zeilenindex:  <br/> |**visRowSmartTag** +  *i* , wobei *i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visSmartTagDisplayMode** <br/> |
   

