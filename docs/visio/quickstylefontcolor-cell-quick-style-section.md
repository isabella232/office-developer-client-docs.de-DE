---
title: Zelle "QuickStyleFontColor" (Abschnitt "Quick Style")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 31c56d08-19ea-4b8b-8be7-42e1c736fbca
description: Bestimmt die Schriftfarbe aus den Schnellformatvorlagen, die der Text eines Shapes vom aktiven Design erbt, als ganze Zahl von 0 bis 1.
ms.openlocfilehash: bd645383df02260fcf6a2045764d9a1b44126090
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415026"
---
# <a name="quickstylefontcolor-cell-quick-style-section"></a>Zelle "QuickStyleFontColor" (Abschnitt "Quick Style")

Bestimmt die Schriftfarbe aus den Schnellformatvorlagen, die der Text eines Shapes vom aktiven Design erbt, als ganze Zahl von 0 bis 1. 
  
|||
|:-----|:-----|
|Wert  <br/> |Beschreibung  <br/> |
|0  <br/> |Der Formtext verwendet die Schriftfarbe Dunkel.  <br/> |
|1  <br/> |Der Formtext verwendet die Schriftfarbe Light.  <br/> |
   
## <a name="remarks"></a>Hinweise

Verwenden Sie zum Erhalten eines Verweises auf die **QuickStyleFontColor-Zelle** anhand des Namens aus einer anderen Formel, nach dem Wert des **N-Attributs** eines **Cell-Elements** oder aus einem Programm mit der **CellsU-Eigenschaft:** 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | QuickStyleFontColor  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die **QuickStyleFontColor-Zelle** nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowQuickStyleProperties** <br/> |
| Zellenindex:  <br/> |**visQuickStyleFontColor** <br/> |
   

