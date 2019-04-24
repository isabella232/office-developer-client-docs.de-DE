---
title: Reflexions Zelle (Abschnitt "Additional Effect Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7dfeb78e-a0fa-4492-b35f-70b1e2975d38
description: Bestimmt die Größe der Reflektion relativ zum Shape, als Prozentsatz von 0,0 bis 100,0%. Ein Shape mit dem Wert 0% in der Zelle reFlexe hat keine Reflexion; ein Wert von 100% zeigt ein vollständiges Spiegelbild der Form an.
ms.openlocfilehash: 60fcb315ec1b6187082bdcdbbdcfaa4b80bbcfb3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348356"
---
# <a name="reflectionsize-cell-additional-effect-properties-section"></a>Reflexions Zelle (Abschnitt "Additional Effect Properties")

Bestimmt die Größe der Reflektion relativ zum Shape, als Prozentsatz von 0,0 bis 100,0%. Ein Shape mit dem Wert 0% in der Zelle **** Reflexe hat keine Reflexion; ein Wert von 100% zeigt ein vollständiges Spiegelbild der Form an. 
  
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die **** Zelle Reflexe aus einer anderen Formel, nach dem Wert des **N** -Attributs eines **Cell** -Elements oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Reflexion  <br/> |
   
Wenn Sie einen Verweis auf die **** Zelle Reflexe aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowOtherEffectProperties** <br/> |
| Zellenindex:  <br/> |**visReflectionSize** <br/> |
   

