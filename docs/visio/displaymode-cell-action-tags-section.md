---
title: DisplayMode Cell (Action Tags Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60039
localization_priority: Normal
ms.assetid: 0dfad40b-f97e-0c4a-2102-7344d1317b82
description: Bestimmt, ob das Aktionstag angezeigt wird, wenn der Zeiger über das Tag bewegt wird, wenn das Shape ausgewählt ist oder immer.
ms.openlocfilehash: 4cb0666ca8de28247309de4fc0d2ff23e8b37d8a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796842"
---
# <a name="displaymode-cell-action-tags-section"></a>DisplayMode Cell (Action Tags Section)

Bestimmt, ob das Aktionstag angezeigt wird, wenn der Zeiger über das Tag bewegt wird, wenn das Shape ausgewählt ist oder immer.
  
> [!NOTE]
> In früheren Versionen von Microsoft Visio werden Aktionstags als Smarttags bezeichnet. 
  
|**Wert**|**Anzeigemodus**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
| 0  <br/> | Wird angezeigt, wenn die Maus über das Tag (Standardeinstellung) angehalten ist.  <br/> |**visSmartTagDispModeMouseOver** <br/> |
| 1  <br/> | Wird angezeigt, wenn das Shape ausgewählt ist.  <br/> |**visSmartTagDispModeShapeSelected** <br/> |
| 2  <br/> | Wird immer angezeigt.  <br/> |**visSmartTagDispModeAlways** <br/> |
   
## <a name="remarks"></a>Hinweise

Aktionstags werden nicht in gedruckten oder veröffentlichten Ausgaben angezeigt. 
  
Wenn für ein Zeichenblatt ein Aktionstag definiert ist und die Zelle den Wert 1 aufweist, wird das Tag nie angezeigt, weil ein Zeichenblatt nicht ausgewählt werden kann. 
  
Zum Abrufen eines Verweises auf die Zelle DisplayMode nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | SmartTags.  *Name* . DisplayMode wobei SmartTags. *Name* ist der Name der Zeile Aktionstag  <br/> |
   
Wenn Sie einen Verweis auf die Zelle DisplayMode aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionSmartTag** <br/> |
| Zeilenindex:  <br/> |**VisRowSmartTag** +  *i* wobei *i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visSmartTagDisplayMode** <br/> |
   

