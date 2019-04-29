---
title: GlowColor Cell (Additional Effect Properties section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 640d18c0-5b6a-4a2f-9c81-f74de5ba9eb1
description: Bestimmt die Farbe, die für den Strich des externen Glühens verwendet wird, der auf eine Form angewendet wird, als RGB-oder Design Wert.
ms.openlocfilehash: 726dbef7ae006af1a6ff9956d16eb73cfdd02974
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422635"
---
# <a name="glowcolor-cell-additional-effect-properties-section"></a>GlowColor Cell (Additional Effect Properties section)

Bestimmt die Farbe, die für den Strich des externen Glühens verwendet wird, der auf eine Form angewendet wird, als RGB-oder Design Wert.
  
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle **GlowColor** aus einer anderen Formel, nach dem Wert des **N** -Attributs eines **Cell** -Elements oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | GlowColor  <br/> |
   
Wenn Sie einen Verweis auf die Zelle **GlowColor** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowOtherEffectProperties** <br/> |
| Zellenindex:  <br/> |**visGlowColor** <br/> |
   

