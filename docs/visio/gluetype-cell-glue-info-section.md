---
title: Zelle "GlueType" (Abschnitt "Glue Info")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm420
ms.localizationpriority: medium
ms.assetid: fffbefd6-8b0b-0023-6b03-026d1c6e885e
description: Bestimmt, ob ein 1D-Shape statischen (Punkt-zu-Punkt) oder dynamischen (Shape-zu-Shape) Kleber verwendet, wenn es an ein anderes Shape geklebt wird.
ms.openlocfilehash: 42fa54ffc9590db3eabc887a03b3bda6052a5335
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59598556"
---
# <a name="gluetype-cell-glue-info-section"></a>Zelle "GlueType" (Abschnitt "Glue Info")

Bestimmt, ob ein 1D-Shape statischen (Punkt-zu-Punkt) oder dynamischen (Shape-zu-Shape) Kleber verwendet, wenn es an ein anderes Shape geklebt wird.
  
|**Wert**|**Beschreibung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
| &amp;H0  <br/> | Standardeinstellung. Dynamischen Kleber nur für dynamische Verbinder zulassen, sonst statischen Kleber verwenden.  <br/> |**visGlueTypeDefault** <br/> |
| &amp;H1  <br/> | Dynamischen Kleber zulassen.  <br/> | Wird ab Visio 2002 nicht mehr verwendet.  <br/> |
| &amp;H2  <br/> | Dynamischen Kleber zulassen.  <br/> |**visGlueTypeOiring** <br/> |
| &amp;H4  <br/> | Dynamischen Kleber nicht zulassen.  <br/> |**visGlueTypeNoOiring** <br/> |
| &amp;H8  <br/> | Dieses 2D-Shape darf nicht mit dynamischem Kleber verbunden werden.  <br/> |**visGlueTypeNo GeometricingTo** <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Wenn diese Zelle den Wert 1, 2 oder 3 enthält, wird dynamischer Kleber verwendet, wenn eine der folgenden Bedingungen vorliegt:
  
- Shapes werden auf der Benutzeroberfläche dynamisch verklebt.
    
- Shapes werden an die Zelle PinX oder PinY eines anderen Shapes aus einem Programm geklebt.
    
Wenn Shapes von einem Programm an Shape-Zellen außer PinX oder PinY geklebt werden, wird statischer Kleber verwendet.
  
Wenn Sie diesen Wert ändern, sodass dynamisches Kleben nicht mehr zulässig ist, werden bereits vorhandene dynamisch geklebte Verbindungen weder getrennt noch verändert. Programme können dynamischen Kleber verwenden, auch wenn das dynamische Kleben in der Zelle GlueType deaktiviert ist.
  
Um einen Verweis auf die Zelle "GlueType" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | GlueType  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle "GlueType" anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowMisc** <br/> |
| Zellenindex:  <br/> |**visGlueType** <br/> |
   

