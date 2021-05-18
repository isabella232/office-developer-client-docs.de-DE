---
title: Zelle "CompoundType" (Abschnitt "Line Format")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3e2a88ad-d92c-4550-8da3-fa7fdd032e73
description: Bestimmt den zusammengesetzten Typ der Linie einer Form.
ms.openlocfilehash: 120975e419656234266cb8151b2fa37ef19602e5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407172"
---
# <a name="compoundtype-cell-line-format-section"></a>Zelle "CompoundType" (Abschnitt "Line Format")

Bestimmt den zusammengesetzten Typ der Linie einer Form. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|0  <br/> |Einfach  <br/> |
|1  <br/> |Gleitkommawert mit doppelter Genauigkeit  <br/> |
|2  <br/> |Dick dünn  <br/> |
|3  <br/> |Dünn dick  <br/> |
|4   <br/> |Triple  <br/> |
   
## <a name="remarks"></a>Hinweise

Verwenden Sie zum Erhalten eines Verweises auf die **Zelle CompoundType** anhand des Namens aus einer anderen Formel, nach dem Wert des **N-Attributs** eines **Cell-Elements** oder aus einem Programm mit der **CellsU-Eigenschaft:** 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | CompoundType  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die **Zelle CompoundType** nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowLine** <br/> |
| Zellenindex:  <br/> |**visCompoundType** <br/> |
   

