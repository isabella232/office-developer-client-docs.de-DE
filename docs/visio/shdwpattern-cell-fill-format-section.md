---
title: Zelle "ShdwPattern" (Abschnitt "Fill Format")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm935
ms.localizationpriority: medium
ms.assetid: eca73b80-9835-9011-1dce-187ccee92e76
description: Definiert das Füllmuster für den Schatten eines Shapes.
ms.openlocfilehash: 2216cc18149cf36be52b3c034d8c0634fa40e9b8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59559545"
---
# <a name="shdwpattern-cell-fill-format-section"></a>Zelle "ShdwPattern" (Abschnitt "Fill Format")

Definiert das Füllmuster für den Schatten eines Shapes.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|0  <br/> |Keins (transparente Füllung).  <br/> |
|1  <br/> |Einfarbige Vordergrundfarbe  <br/> |
|2 - 40  <br/> |Verschiedene Füllmuster  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Wenn Sie das Füllmuster festlegen möchten, geben Sie eine Zahl von 0 bis 40 ein. Diese Zahl ist ein Index für eine Mustersammlung. Sie können sich die Füllmustersammlung auch im Dialogfeld **Füllbereich** ansehen (klicken Sie dazu auf der Registerkarte **Start** in der Gruppe **Shape** auf **Füllbereich**, und klicken Sie dann auf **Füllbereichsoptionen**).
  
Um einen Verweis auf die Zelle "ShdwPattern" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |ShdwPattern  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle ShdwPattern anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowFill** <br/> |
|Zellenindex:  <br/> |**visFillShdwPattern** <br/> |
   

