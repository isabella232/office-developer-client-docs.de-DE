---
title: Zelle "DontMoveChildren" (Abschnitt "Group Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm255
localization_priority: Normal
ms.assetid: ff5bbf05-4851-30ce-7ee1-f0ce7b2781ab
description: Legt fest, ob Shapes in einer Gruppe mithilfe der Maus verschoben werden können.
ms.openlocfilehash: 2b15d75a98b5f5a72bce8b80758d27b197a346ed
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416594"
---
# <a name="dontmovechildren-cell-group-properties-section"></a>Zelle "DontMoveChildren" (Abschnitt "Group Properties")

Legt fest, ob Shapes in einer Gruppe mithilfe der Maus verschoben werden können.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
| TRUE  <br/> | Shapes in einer Gruppe können mit der Maus nicht verschoben werden.  <br/> |
| FALSE  <br/> | Shapes in einer Gruppe können mit der Maus verschoben werden.  <br/> |
   
## <a name="remarks"></a>Hinweise

Wenn diese Zelle den Wert TRUE enthält, können Sie Shapes in Gruppen mithilfe anderer Methoden weiterhin kippen, drehen, größenmäßig anpassen oder neu positionieren.
  
Der Wert dieser Zelle ist TRUE bei Gruppen in Master-Shapes und Gruppen in Instanzen von Master-Shapes, die mit früheren Versionen von Microsoft Visio 2000 erstellt wurden.
  
Um einen Verweis auf die Zelle DontMoveChildren anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | DontMoveChildren  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die DontMoveChildren-Zelle nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowGroup** <br/> |
| Zellenindex:  <br/> |**visGroupDontMoveChildren** <br/> |
   

