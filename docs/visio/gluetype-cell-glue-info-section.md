---
title: Zelle "GlueType" (Abschnitt "Glue Info")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm420
localization_priority: Normal
ms.assetid: fffbefd6-8b0b-0023-6b03-026d1c6e885e
description: Bestimmt, ob ein 1D-Shape statischen (Punkt-zu-Punkt) oder dynamischen (Shape-zu-Shape) Kleber verwendet, wenn es an ein anderes Shape geklebt wird.
ms.openlocfilehash: 162827521cda6fe4a37d17a8f7d36d7a36718519
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797104"
---
# <a name="gluetype-cell-glue-info-section"></a>GlueType Cell (Glue Info Section)

Bestimmt, ob ein 1D-Shape statischen (Punkt-zu-Punkt) oder dynamischen (Shape-zu-Shape) Kleber verwendet, wenn es an ein anderes Shape geklebt wird.
  
|**Wert**|**Beschreibung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
| &amp;H0  <br/> | Standardeinstellung. Dynamischen Kleber nur für dynamische Verbinder zulassen, sonst statischen Kleber verwenden.  <br/> |**visGlueTypeDefault** <br/> |
| &amp;H1  <br/> | Dynamischen Kleber zulassen.  <br/> | Wird ab Visio 2002 nicht mehr verwendet.  <br/> |
| &amp;H2  <br/> | Dynamischen Kleber zulassen.  <br/> |**visLOFlagsRoutable** <br/> |
| &amp;H4  <br/> | Dynamischen Kleber nicht zulassen.  <br/> |**visGlueTypeNoWalking** <br/> |
| &amp;H8  <br/> | Dieses 2D-Shape darf nicht mit dynamischem Kleber verbunden werden.  <br/> |**visGlueTypeNoWalkingTo** <br/> |
   
## <a name="remarks"></a>Hinweise

Wenn diese Zelle den Wert 1, 2 oder 3 enthält, wird dynamischer Kleber verwendet, wenn eine der folgenden Bedingungen vorliegt:
  
- Shapes werden auf der Benutzeroberfläche dynamisch verklebt.
    
- Shapes werden an die Zelle PinX oder PinY eines anderen Shapes aus einem Programm geklebt.
    
Wenn Shapes von einem Programm an Shape-Zellen außer PinX oder PinY geklebt werden, wird statischer Kleber verwendet.
  
Wenn Sie diesen Wert ändern, sodass dynamisches Kleben nicht mehr zulässig ist, werden bereits vorhandene dynamisch geklebte Verbindungen weder getrennt noch verändert. Programme können dynamischen Kleber verwenden, auch wenn das dynamische Kleben in der Zelle GlueType deaktiviert ist.
  
Wenn Sie einen Verweis auf die Zelle GlueType aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | GlueType  <br/> |
   
Wenn Sie einen Verweis auf die Zelle GlueType aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowMisc** <br/> |
| Zellenindex:  <br/> |**visGlueType** <br/> |
   

