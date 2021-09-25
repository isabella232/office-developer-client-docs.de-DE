---
title: Zelle "EnableFillProps" (Abschnitt "Style Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm300
ms.localizationpriority: medium
ms.assetid: 2b3334de-588c-6cf3-bc88-be03ae71b1a6
description: Bestimmt, ob eine Formatvorlage Füllbereichseigenschaften enthält.
ms.openlocfilehash: 4621b40287b8e03464e2f27db3a5639ac7eb6d6f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59570743"
---
# <a name="enablefillprops-cell-style-properties-section"></a>Zelle "EnableFillProps" (Abschnitt "Style Properties")

Bestimmt, ob eine Formatvorlage Füllbereichseigenschaften enthält.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Füllbereichseigenschaften einschließen.  <br/> |
|FALSE  <br/> |Füllbereichseigenschaften ausschließen.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Um einen Verweis auf die Zelle "EnableFillProps" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |EnableFillProps  <br/> |
   
Um einen Verweis auf die Zelle "EnableFillProps" anhand des Indexes eines Programms abzurufen, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowStyle** <br/> |
|Zellenindex:  <br/> |**visStyleIncludesFill** <br/> |
   

