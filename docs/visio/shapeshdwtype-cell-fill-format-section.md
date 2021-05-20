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
ms.openlocfilehash: 607881e4a520f1376562394c6e40ab5d2508906d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430259"
---
# <a name="shapeshdwtype-cell-fill-format-section"></a>Zelle "ShapeShdwType" (Abschnitt "Fill Format")

Gibt den Schattentyp für ein Shape an. 
  
|**Wert**|**Beschreibung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
|0  <br/> |Zeichenblattstandard verwenden (Standard)  <br/> |**visFSTPageDefault** <br/> |
|1  <br/> |Einfach  <br/> |**visFSTSimple** <br/> |
|2  <br/> |Schräg  <br/> |**visFSTOblique** <br/> |
   
## <a name="remarks"></a>Hinweise

Verwenden Sie diese Zelle, um einen Formschatten anzuwenden, der sich von der Seiteneinstellung ablöst (der Standardmäßige Schattentyp der Seite wird in der Zelle ShdwType im Abschnitt Seiteneigenschaften definiert).
  
Einfache Schattentypen werden als Abstandsschatten auf der Benutzeroberfläche beschrieben. Ein einfacher Schatten hat den Effekt, dass das Shape auf einer zum Shape parallelen Ebene einen Schatten zu werfen scheint. Schräge Schatten werden als schräge Schatten auf der Benutzeroberfläche beschrieben und haben den Effekt, dass der Schatten auf einer zum Shape rechtwinkligen Ebene zu liegen scheint. 
  
Eine Liste vordefinierter einfacher und schräger Schatten finden Sie im Dialogfeld **Schatten** im Feld **Formatvorlage** (klicken Sie auf der Registerkarte **Start** in der Gruppe **Shape** auf **Schatten**, und klicken Sie dann auf **Schattenoptionen**).
  
Um einen Verweis auf die Zelle ShapeShdwType anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |ShapeShdwType  <br/> |
   
Um einen Verweis auf die Zelle ShapeShdwType nach Index aus einem Programm zu erhalten, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowFill** <br/> |
|Zellenindex:  <br/> |**visFillShdwType** <br/> |
   

