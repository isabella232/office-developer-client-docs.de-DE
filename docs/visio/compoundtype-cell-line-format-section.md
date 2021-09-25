---
title: Zelle "CompoundType" (Abschnitt "Line Format")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 3e2a88ad-d92c-4550-8da3-fa7fdd032e73
description: Bestimmt den zusammengesetzten Typ der Linie einer Form.
ms.openlocfilehash: c43175bc42e74bc18b8bf643976fdc859e3dbf8b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59608459"
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
   
## <a name="remarks"></a>HinwBemerkungeneise

Um einen Verweis auf die **Zelle "CompoundType"** anhand des Namens aus einer anderen Formel, anhand des Werts des **N-Attributs** eines **Cell-Elements** oder eines Programms mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | CompoundType  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die **Zelle CompoundType** anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowLine** <br/> |
| Zellenindex:  <br/> |**visCompoundType** <br/> |
   

