---
title: Zelle "FillBkgndTrans" (Abschnitt "Fill Format")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253230
ms.localizationpriority: medium
ms.assetid: 87065350-ba9a-aae8-47f6-f263f6700d08
description: Legt die Transparenzstufe fest, die für die Hintergrundfarbe (Füllbereich) des Füllmusters des Shapes verwendet wird.
ms.openlocfilehash: 6680213259873de7a6269a03ef1fb30c48170ec5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59570630"
---
# <a name="fillbkgndtrans-cell-fill-format-section"></a>Zelle "FillBkgndTrans" (Abschnitt "Fill Format")

Legt die Transparenzstufe fest, die für die Hintergrundfarbe (Füllbereich) des Füllmusters des Shapes verwendet wird.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|0 - 100  <br/> |Stellt die Transparenz in Prozent dar. Der Standardwert ist 0% (vollständig undurchsichtig).  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Werte werden auf ein halbes Prozent gerundet. Ein Wert von 100% bezeichnet völlige Transparenz. Ein Shape, dem ein völlig transparenter Füllbereich zugewiesen wurde, verhält sich auf dem Zeichenblatt zwar genauso wie ein Shape ohne Füllbereichzuweisung, die Interaktion mit anderen Objekten auf dem Zeichenblatt verläuft aber genauso wie bei Festlegen der Transparenz auf 0%.
  
Sie können diesen Wert auch festlegen, indem Sie den Schieberegler im Dialogfeld **Füllbereich** verwenden (klicken Sie dazu auf der Registerkarte **Start** in der Gruppe **Shape** auf **Füllbereich**, und klicken Sie dann auf **Füllbereichsoptionen**). Dieser Wert bestimmt sowohl den Wert der Fülltransparenz für den Hintergrund als auch den Wert für den Vordergrund. Wenn Sie diese Werte unabhängig voneinander festlegen möchten, müssen Sie sie im ShapeSheet-Fenster eingeben.
  
Um einen Verweis auf die Zelle "FillBkgndTrans" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |FillBkgndTrans  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle FillBkgndTrans anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowFill** <br/> |
|Zellenindex:  <br/> |**visFillBkgndTrans** <br/> |
   

