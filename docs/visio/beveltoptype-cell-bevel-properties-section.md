---
title: Zelle "BevelTopType" (Abschnitt "Fase Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3e29af0d-4183-41d1-8b0f-96450089f882
description: Bestimmt den abschrägtyp für den oberen Rand eines Shapes.
ms.openlocfilehash: 225600a3e39ec58622bcd8597e1115a52cb62a3f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315729"
---
# <a name="beveltoptype-cell-bevel-properties-section"></a>Zelle "BevelTopType" (Abschnitt "Fase Properties")

Bestimmt den abschrägtyp für den oberen Rand eines Shapes. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|0  <br/> |Keine Abschrägung  <br/> |
|1  <br/> |Kreis-Abschrägung  <br/> |
|2  <br/> |GeLockerte Abschrägung  <br/> |
|3  <br/> |Kreuz Abschrägung  <br/> |
|4  <br/> |Kühle schräg Fase  <br/> |
|5  <br/> |Winkel Abschrägung  <br/> |
|6  <br/> |Weiche Rundung  <br/> |
|7  <br/> |Konvexe Abschrägung  <br/> |
|8  <br/> |Neigungs Abschrägung  <br/> |
|9  <br/> |Divot-Abschrägung  <br/> |
|10  <br/> |Abrundung-Abschrägung  <br/> |
|11  <br/> |Kanten Abschrägung  <br/> |
|12  <br/> |Art-Deco-Fase  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle **BevelTopType** aus einer anderen Formel, nach dem Wert des **N** -Attributs eines **Cell** -Elements oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |BevelTopType  <br/> |
   
Wenn Sie einen Verweis auf die Zelle **BevelTopType** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowBevelProperties** <br/> |
|Zellenindex:  <br/> |**visBevelTopType** <br/> |
   

