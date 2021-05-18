---
title: Zelle "BevelTopType" (Abschnitt "Bevel Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3e29af0d-4183-41d1-8b0f-96450089f882
description: Bestimmt den Abschrägungstyp an der oberen Kante eines Shapes.
ms.openlocfilehash: 225600a3e39ec58622bcd8597e1115a52cb62a3f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421494"
---
# <a name="beveltoptype-cell-bevel-properties-section"></a>Zelle "BevelTopType" (Abschnitt "Bevel Properties")

Bestimmt den Abschrägungstyp an der oberen Kante eines Shapes. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|0  <br/> |Keine Abschrägung  <br/> |
|1  <br/> |Kreis abschrägt  <br/> |
|2  <br/> |Entspannte Inset-Abschrägung  <br/> |
|3  <br/> |Abschrägung  <br/> |
|4   <br/> |Cool Slant Abschrägung  <br/> |
|5   <br/> |Winkelschrägung  <br/> |
|6   <br/> |Soft Round-Abschrägung  <br/> |
|7   <br/> |Konvexe Abschrägung  <br/> |
|8   <br/> |Neigungsabschrägung  <br/> |
|9   <br/> |Divot-Abschrägung  <br/> |
|10  <br/> |Abschrägung von Schrägen  <br/> |
|11  <br/> |Hard Edge-Abschrägung  <br/> |
|12   <br/> |Art-Deco-Abschrägung  <br/> |
   
## <a name="remarks"></a>Hinweise

Verwenden Sie zum Erhalten eines Verweises auf die **Zelle BevelTopType** anhand des Namens aus einer anderen Formel, nach dem Wert des **N-Attributs** eines **Cell-Elements** oder aus einem Programm mit der **CellsU-Eigenschaft:** 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |BevelTopType  <br/> |
   
Um einen Verweis auf die **Zelle BevelTopType** nach Index aus einem Programm zu erhalten, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowBevelProperties** <br/> |
|Zellenindex:  <br/> |**visBevelTopType** <br/> |
   

