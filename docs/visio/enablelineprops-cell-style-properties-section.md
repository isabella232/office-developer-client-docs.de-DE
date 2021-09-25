---
title: Zelle "EnableLineProps" (Abschnitt "Style Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251696
ms.localizationpriority: medium
ms.assetid: 9f619416-36ff-1479-6232-225c11827e01
description: Bestimmt, ob eine Formatvorlage Linieneigenschaften enthält.
ms.openlocfilehash: f2e6c3c74329c196e2e527a2879c0604ef5c5c61
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59559906"
---
# <a name="enablelineprops-cell-style-properties-section"></a>Zelle "EnableLineProps" (Abschnitt "Style Properties")

Bestimmt, ob eine Formatvorlage Linieneigenschaften enthält.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Linieneigenschaften einschließen.  <br/> |
|FALSE  <br/> |Linieneigenschaften ausschließen.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Um einen Verweis auf die Zelle "EnableLineProps" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |EnableLineProps  <br/> |
   
Um einen Verweis auf die Zelle "EnableLineProps" anhand des Indexes eines Programms abzurufen, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowStyle** <br/> |
|Zellenindex:  <br/> |**visStyleIncludesLine** <br/> |
   

