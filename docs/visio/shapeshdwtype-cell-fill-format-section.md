---
title: Zelle "ShapeShdwType" (Abschnitt "Fill Format")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033173
ms.localizationpriority: medium
ms.assetid: 1461148d-90a9-6f7c-1b28-9310ffaf0e3b
description: Gibt den Schattentyp für ein Shape an.
ms.openlocfilehash: a2c82e41d00151202ee47c2863364e59a3688a66
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59598129"
---
# <a name="shapeshdwtype-cell-fill-format-section"></a>Zelle "ShapeShdwType" (Abschnitt "Fill Format")

Gibt den Schattentyp für ein Shape an. 
  
|**Wert**|**Beschreibung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
|0  <br/> |Zeichenblattstandard verwenden (Standard)  <br/> |**visFSTPageDefault** <br/> |
|1  <br/> |Einfach  <br/> |**visFSTSimple** <br/> |
|2  <br/> |Oblique  <br/> |**visFSTOblique** <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Verwenden Sie diese Zelle, um einen Formschatten anzuwenden, der sich vom Seitenstandard unterscheidet (der Standardschattentyp der Seite wird in der Zelle ShdwType im Abschnitt "Page Properties") definiert.
  
Einfache Schattentypen werden als Abstandsschatten auf der Benutzeroberfläche beschrieben. Ein einfacher Schatten hat den Effekt, dass das Shape auf einer zum Shape parallelen Ebene einen Schatten zu werfen scheint. Schräge Schatten werden als schräge Schatten auf der Benutzeroberfläche beschrieben und haben den Effekt, dass der Schatten auf einer zum Shape rechtwinkligen Ebene zu liegen scheint. 
  
Eine Liste vordefinierter einfacher und schräger Schatten finden Sie im Dialogfeld **Schatten** im Feld **Formatvorlage** (klicken Sie auf der Registerkarte **Start** in der Gruppe **Shape** auf **Schatten**, und klicken Sie dann auf **Schattenoptionen**).
  
Verwenden Sie Folgendes, um einen Verweis auf die Zelle ShapeShdwType anhand des Namens einer anderen Formel oder eines Programms mithilfe der **CellsU-Eigenschaft** abzurufen: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |ShapeShdwType  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle ShapeShdwType anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowFill** <br/> |
|Zellenindex:  <br/> |**visFillShdwType** <br/> |
   

