---
title: Zelle "QuickStyleType" (Abschnitt "Quick Style")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: e7470417-0d70-433e-9496-604ca2eafee6
description: Bestimmt den Typ der Schnellformatvorlage (2-dimensional, 1-dimensional oder Verbinder), die das Shape erbt.
ms.openlocfilehash: 4dbdb470f3e9bf2db46a47e2efebfd6414256902
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59623152"
---
# <a name="quickstyletype-cell-quick-style-section"></a>Zelle "QuickStyleType" (Abschnitt "Quick Style")

Bestimmt den Typ der Schnellformatvorlage (2-dimensional, 1-dimensional oder Verbinder), die das Shape erbt. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|0  <br/> |Visio wird automatisch ausgewählt  <br/> |
|1  <br/> |1-dimensional  <br/> |
|2  <br/> |2-dimensional  <br/> |
|3  <br/> |Connector  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Um einen Verweis auf die **QuickStyleType-Zelle** anhand des Namens aus einer anderen Formel, anhand des Werts des **N-Attributs** eines **Cell-Elements** oder eines Programms mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | QuickStyleType  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die **Zelle "QuickStyleType"** anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowQuickStyleProperties** <br/> |
| Zellenindex:  <br/> |**visQuickStyleType** <br/> |
   

