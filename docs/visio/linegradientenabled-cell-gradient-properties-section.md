---
title: Zelle "LineGradientEnabled" (Abschnitt "Gradient Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 276a661f-d14e-404a-a494-ae36601a8ce3
description: Bestimmt, ob ein Linienverlauf für eine Linie oder einen Rahmen einer Form aktiviert ist.
ms.openlocfilehash: 1d2b33275d26bb0c8e5550bcb7cf282c64d34544
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416377"
---
# <a name="linegradientenabled-cell-gradient-properties-section"></a>Zelle "LineGradientEnabled" (Abschnitt "Gradient Properties")

Bestimmt, ob ein Linienverlauf für eine Linie oder einen Rahmen einer Form aktiviert ist. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Der Farbverlauf wird auf der Linie oder dem Rahmen einer Form angezeigt.  <br/> |
|FALSE  <br/> |Farbverläufe werden nicht auf der Linie oder dem Rahmen einer Form angezeigt.  <br/> |
   
## <a name="remarks"></a>Hinweise

Um einen Verweis auf die **LineGradientEnabled-Zelle** anhand des Namens aus einer anderen Formel, nach dem Wert des **N-Attributs** eines **Cell-Elements** oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | LineGradientEnabled  <br/> |
   
Um einen Verweis auf die **LineGradientEnabled-Zelle** nach Index aus einem Programm zu erhalten, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowGradientProperties** <br/> |
| Zellenindex:  <br/> |**visLineGradientEnabled** <br/> |
   

