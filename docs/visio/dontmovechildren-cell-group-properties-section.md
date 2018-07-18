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
ms.openlocfilehash: df5d0d2b44e283ee8301d9c088d3ce55114e9a75
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796880"
---
# <a name="dontmovechildren-cell-group-properties-section"></a>DontMoveChildren Cell (Group Properties Section)

Legt fest, ob Shapes in einer Gruppe mithilfe der Maus verschoben werden können.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
| TRUE  <br/> | Shapes in einer Gruppe können mit der Maus nicht verschoben werden.  <br/> |
| FALSE  <br/> | Shapes in einer Gruppe können mit der Maus verschoben werden.  <br/> |
   
## <a name="remarks"></a>Hinweise

Wenn diese Zelle den Wert TRUE enthält, können Sie Shapes in Gruppen mithilfe anderer Methoden weiterhin kippen, drehen, größenmäßig anpassen oder neu positionieren.
  
Der Wert dieser Zelle ist TRUE bei Gruppen in Master-Shapes und Gruppen in Instanzen von Master-Shapes, die mit früheren Versionen von Microsoft Visio 2000 erstellt wurden.
  
Wenn Sie einen Verweis auf die Zelle DontMoveChildren aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | DontMoveChildren  <br/> |
   
Wenn Sie einen Verweis auf die Zelle DontMoveChildren aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowGroup** <br/> |
| Zellenindex:  <br/> |**visGroupDontMoveChildren** <br/> |
   

