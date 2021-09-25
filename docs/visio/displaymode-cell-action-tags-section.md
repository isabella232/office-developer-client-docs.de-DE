---
title: Zelle "DisplayMode" (Abschnitt "Action Tags")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60039
ms.localizationpriority: medium
ms.assetid: 0dfad40b-f97e-0c4a-2102-7344d1317b82
description: Bestimmt, ob das Aktionstag angezeigt wird, wenn der Benutzer den Mauszeiger über das Tag bewegt, wenn das Shape ausgewählt ist oder immer.
ms.openlocfilehash: 382922d55e05ccaef7c5c8232e888fcd15e0143f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59582806"
---
# <a name="displaymode-cell-action-tags-section"></a>Zelle "DisplayMode" (Abschnitt "Action Tags")

Bestimmt, ob das Aktionstag angezeigt wird, wenn der Benutzer den Mauszeiger über das Tag bewegt, wenn das Shape ausgewählt ist oder immer.
  
> [!NOTE]
> In früheren Versionen von Microsoft Visio werden Aktionstags als Smarttags bezeichnet. 
  
|**Wert**|**Anzeigemodus**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
| 0  <br/> | Wird angezeigt, wenn die Maus über dem Tag angehalten wird (Standardeinstellung).  <br/> |**visSmartTagDispModeMouseOver** <br/> |
| 1  <br/> | Wird angezeigt, wenn das Shape ausgewählt ist.  <br/> |**visSmartTagDispModeShapeSelected** <br/> |
| 2  <br/> | Wird immer angezeigt.  <br/> |**visSmartTagDispModeAlways** <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Aktionstags werden nicht in gedruckten oder veröffentlichten Ausgaben angezeigt. 
  
Wenn für ein Zeichenblatt ein Aktionstag definiert ist und die Zelle den Wert 1 aufweist, wird das Tag nie angezeigt, weil ein Zeichenblatt nicht ausgewählt werden kann. 
  
Um einen Verweis auf die Zelle "DisplayMode" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | SmartTags.  *Name*  . DisplayMode where SmartTags. *Name*  ist der Name der Aktionstagzeile  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle DisplayMode anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionSmartTag** <br/> |
| Zeilenindex:  <br/> |**visRowSmartTag**  +   *i* where *i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visSmartTagDisplayMode** <br/> |
   

