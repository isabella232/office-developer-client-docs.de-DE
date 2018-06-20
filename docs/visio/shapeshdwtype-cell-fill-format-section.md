---
title: Zelle "ShapeShdwType" (Abschnitt "Fill Format")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033173
localization_priority: Normal
ms.assetid: 1461148d-90a9-6f7c-1b28-9310ffaf0e3b
description: Gibt den Schattentyp für ein Shape an.
ms.openlocfilehash: b96ad4a877d72bf4457ec3cf038a29a2b414e0f0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798041"
---
# <a name="shapeshdwtype-cell-fill-format-section"></a>ShapeShdwType Cell (Fill Format Section)

Gibt den Schattentyp für ein Shape an. 
  
|**Wert**|**Beschreibung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
|0  <br/> |Zeichenblattstandard verwenden (Standard)  <br/> |**visFSTPageDefault** <br/> |
|1  <br/> |Einfach  <br/> |**visFSTSimple** <br/> |
|2  <br/> |Schräg  <br/> |**visFSTOblique** <br/> |
   
## <a name="remarks"></a>Hinweise

Verwenden Sie diese Zelle für einen Shape Schatten, der sich vom Zeichenblattstandard unterscheidet (der Schattentyp Seite wird in der Zelle ShdwType in den Abschnitt "Page Properties" definiert).
  
Einfacher Schatten werden als Offset Schatten auf der Benutzeroberfläche (UI) beschrieben. Ein einfacher Schatten hat den Effekt der Form wird auf eine parallele Ebene hinter dem Shape schattiert. Schräge Schatten werden als schräge Schatten auf der Benutzeroberfläche beschrieben, und weisen Sie die Auswirkung des einen Schatten auf eine senkrecht zum Shape. 
  
Eine Liste vordefinierter einfacher und schräger Schatten finden Sie unter Feld **Formatvorlage** im Dialogfeld **Schatten** (klicken Sie auf der Registerkarte **Start** in der Gruppe **Shape** klicken Sie auf **Schatten**, und klicken Sie dann auf **Schattenoptionen**).
  
Wenn Sie einen Verweis auf die Zelle ShapeShdwType nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |ShapeShdwType  <br/> |
   
Wenn Sie einen Verweis auf die Zelle ShapeShdwType aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowFill** <br/> |
|Zellenindex:  <br/> |**visFillShdwType** <br/> |
   

