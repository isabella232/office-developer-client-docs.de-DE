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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342861"
---
# <a name="shapeshdwtype-cell-fill-format-section"></a>Zelle "ShapeShdwType" (Abschnitt "Fill Format")

Gibt den Schattentyp für ein Shape an. 
  
|**Wert**|**Beschreibung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
|0  <br/> |Zeichenblattstandard verwenden (Standard)  <br/> |**visFSTPageDefault** <br/> |
|1  <br/> |Simple  <br/> |**visFSTSimple** <br/> |
|2  <br/> |Oblique  <br/> |**visFSTOblique** <br/> |
   
## <a name="remarks"></a>Bemerkungen

Verwenden Sie diese Zelle, um einen anderen Shape-Schatten als den Seiten Standard anzuwenden (der Standard Schattentyp der Seite ist in der Zelle "ShdwType im Abschnitt Page Properties definiert).
  
Einfache Schattentypen werden als Abstandsschatten auf der Benutzeroberfläche beschrieben. Ein einfacher Schatten hat den Effekt, dass das Shape auf einer zum Shape parallelen Ebene einen Schatten zu werfen scheint. Schräge Schatten werden als schräge Schatten auf der Benutzeroberfläche beschrieben und haben den Effekt, dass der Schatten auf einer zum Shape rechtwinkligen Ebene zu liegen scheint. 
  
Eine Liste vordefinierter einfacher und schräger Schatten finden Sie im Dialogfeld **Schatten** im Feld **Formatvorlage** (klicken Sie auf der Registerkarte **Start** in der Gruppe **Shape** auf **Schatten**, und klicken Sie dann auf **Schattenoptionen**).
  
Wenn Sie einen Verweis auf die Zelle Zelle aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Zelle  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Zelle aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowFill** <br/> |
|Zellenindex:  <br/> |**visFillShdwType** <br/> |
   

