---
title: Zelle "Alignment" (Abschnitt "Tabs")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm35
localization_priority: Normal
ms.assetid: 84234177-a2df-6acc-2761-230bc5d12627
description: Legt die Tabausrichtung fest.
ms.openlocfilehash: a2178c63d0005ee8b2f0c8ebcfbc25854a5b1567
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796385"
---
# <a name="alignment-cell-tabs-section"></a>Alignment Cell (Tabs Section)

Legt die Tabausrichtung fest.
  
|**Wert**|**Ausrichtung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
| 0  <br/> | Links  <br/> |**visTabStopLeft** <br/> |
| 1  <br/> | Mittig  <br/> |**visTabStopCenter** <br/> |
| 2  <br/> | Nach rechts  <br/> |**visTabStopRight** <br/> |
| 3  <br/> | Dezimalwert  <br/> |**visTabStopDecimal** <br/> |
| 4  <br/> | Komma  <br/> |**visTabStopComma** <br/> |
   
## <a name="remarks"></a>Hinweise

Wenn Sie einen Verweis auf die Zelle Alignment nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Registerkarten.  *Ij* , in dem *i und j =* < 1 >, 2, 3  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Alignment aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionTab** <br/> |
| Zeilenindex:  <br/> |**VisRowTab +** *i* wobei *i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> | (*j* * 3) **+ VisTabAlign** <br/> |
   

