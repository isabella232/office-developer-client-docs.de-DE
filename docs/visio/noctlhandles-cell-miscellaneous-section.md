---
title: Zelle "NoCtlHandles" (Abschnitt "Miscellaneous")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251319
localization_priority: Normal
ms.assetid: 4345b3e5-f522-e300-307c-4f8992a3ddce
description: Aktiviert bzw. deaktiviert die Anzeige der Steuerpunkte für das ausgewählte Shape.
ms.openlocfilehash: cbe4d6a8b6fdd4b66acf064884d20999ff7e3b4f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416125"
---
# <a name="noctlhandles-cell-miscellaneous-section"></a>Zelle "NoCtlHandles" (Abschnitt "Miscellaneous")

Aktiviert bzw. deaktiviert die Anzeige der Steuerpunkte für das ausgewählte Shape.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
| TRUE  <br/> | Steuerpunkte werden nicht angezeigt, wenn ein Shape ausgewählt wird.  <br/> |
| FALSE  <br/> | Steuerpunkte werden angezeigt, wenn ein Shape ausgewählt wird.  <br/> |
   
## <a name="remarks"></a>Hinweise

Um einen Verweis auf die Zelle NoCtlHandles anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | NoCtlHandles  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die NoCtlHandles-Zelle nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowMisc** <br/> |
| Zellenindex:  <br/> |**visNoCtlHandles** <br/> |
   

