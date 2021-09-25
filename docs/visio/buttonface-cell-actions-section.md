---
title: Zelle "ButtonFace" (Abschnitt "Actions")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60025
ms.localizationpriority: medium
ms.assetid: cf15b879-a47e-a5a5-bfdd-1d7ea423742f
description: Bestimmt das Symbol, das neben einem Element in einem Kontext- oder Aktionstagmenü angezeigt wird.
ms.openlocfilehash: 96610ad6e1add550ab6ed940b7dc2ccbfb8373da
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59608613"
---
# <a name="buttonface-cell-actions-section"></a>Zelle "ButtonFace" (Abschnitt "Actions")

Bestimmt das Symbol, das neben einem Element in einem Kontext- oder Aktionstagmenü angezeigt wird.
  
> [!NOTE]
> In früheren Versionen von Microsoft Visio werden Aktionstags als Smarttags bezeichnet. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Die Zeichenfolge in einer ButtonFace-Zelle stellt die ID einer Microsoft Office-Schaltflächenoberseite dar. Der Wert Null (0) oder ein Leerzeichen bedeutet, dass kein Symbol angezeigt wird. 
  
Die IDs, die in der Zelle ButtonFace verwendet werden können, entsprechen den IDs, die mit der **FaceID-Eigenschaft** eines **CommandBarButton-Objekts** verwendet werden. Weitere Informationen zu diesen IDs erhalten Sie, indem Sie auf MSDN nach "Arbeiten mit Befehlsleisten-Schaltflächenbildern" suchen. 
  
Verwenden Sie Folgendes, um einen Verweis auf die Zelle "ButtonFace" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |**Aktionen**:  *Name*  . **ButtonFace**         where **Actions**.  *Name*  ist der Name der Aktionszeile  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle ButtonFace anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionAction** <br/> |
|Zeilenindex:  <br/> |**visRowAction**  +   *i* where **i** = 0, 1, 2...  <br/> |
|Zellenindex:  <br/> |**visActionButtonFace** <br/> |
   

