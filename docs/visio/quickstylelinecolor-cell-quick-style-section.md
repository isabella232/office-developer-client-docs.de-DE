---
title: Zelle QuickStyleLineColor (Abschnitt "Quick Style")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: dcfb792f-e02a-4059-acec-a178d221097c
description: Bestimmt, welche Designfarbe die Linie eines Shapes als ganze Zahl von 0 bis 7 verwendet.
ms.openlocfilehash: 010b943f2266b1e0ee192e5f1341d73851d176fd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437043"
---
# <a name="quickstylelinecolor-cell-quick-style-section"></a>Zelle QuickStyleLineColor (Abschnitt "Quick Style")

Bestimmt, welche Designfarbe die Linie eines Shapes als ganze Zahl von 0 bis 7 verwendet.
  
|||
|:-----|:-----|
|Wert  <br/> |Beschreibung  <br/> |
|0  <br/> |Die Formlinienfarbe erbt von der Dunklen Designfarbe.  <br/> |
|1  <br/> |Die Formlinienfarbe erbt von der Farbe des Light-Designs.  <br/> |
|2  <br/> |Die Farbe der Formenlinie erbt von der Akzent 1-Designfarbe  <br/> |
|3  <br/> |Die Farbe der Formenlinie erbt von der Akzent 2-Designfarbe  <br/> |
|4   <br/> |Die Farbe der Formenlinie erbt von der Akzent 3-Designfarbe  <br/> |
|5   <br/> |Die Farbe der Formenlinie erbt von der Akzent 4-Designfarbe  <br/> |
|6   <br/> |Die Farbe der Formenlinie erbt von der Akzent 5-Designfarbe  <br/> |
|7   <br/> |Die Farbe der Formenlinie erbt von der Akzent 6-Designfarbe  <br/> |
   
## <a name="remarks"></a>Hinweise

Um einen Verweis auf die **QuickStyleLineColor-Zelle** anhand des Namens aus einer anderen Formel, nach dem Wert des **N-Attributs** eines **Cell-Elements** oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | QuickStyleLineColor  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die **QuickStyleLineColor-Zelle** nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowQuickStyleProperties** <br/> |
| Zellenindex:  <br/> |**visQuickStyleLineColor** <br/> |
   

