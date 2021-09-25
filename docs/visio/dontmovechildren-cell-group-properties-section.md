---
title: Zelle "DontMoveChildren" (Abschnitt "Group Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm255
ms.localizationpriority: medium
ms.assetid: ff5bbf05-4851-30ce-7ee1-f0ce7b2781ab
description: Legt fest, ob Shapes in einer Gruppe mithilfe der Maus verschoben werden können.
ms.openlocfilehash: 904d1cfceed285868279b8dafea6238eda0b638f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59574363"
---
# <a name="dontmovechildren-cell-group-properties-section"></a>Zelle "DontMoveChildren" (Abschnitt "Group Properties")

Legt fest, ob Shapes in einer Gruppe mithilfe der Maus verschoben werden können.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
| TRUE  <br/> | Shapes in einer Gruppe können mit der Maus nicht verschoben werden.  <br/> |
| FALSE  <br/> | Shapes in einer Gruppe können mit der Maus verschoben werden.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Wenn diese Zelle den Wert TRUE enthält, können Sie Shapes in Gruppen mithilfe anderer Methoden weiterhin kippen, drehen, größenmäßig anpassen oder neu positionieren.
  
Der Wert dieser Zelle ist TRUE bei Gruppen in Master-Shapes und Gruppen in Instanzen von Master-Shapes, die mit früheren Versionen von Microsoft Visio 2000 erstellt wurden.
  
Verwenden Sie Folgendes, um einen Verweis auf die Zelle DontMoveChildren anhand des Namens einer anderen Formel oder eines Programms mithilfe der **CellsU-Eigenschaft** abzurufen: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | DontMoveChildren  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle DontMoveChildren anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowGroup** <br/> |
| Zellenindex:  <br/> |**visGroupDontMoveChildren** <br/> |
   

