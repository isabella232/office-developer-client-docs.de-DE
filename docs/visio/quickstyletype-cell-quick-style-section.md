---
title: QuickStyleType Cell (Quick Style Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e7470417-0d70-433e-9496-604ca2eafee6
description: Bestimmt den Typ der Schnellformatvorlagen (2-dimensionale, 1-dimensionales oder Connector), die das Shape erbt.
ms.openlocfilehash: 211074800eee601d2658edbc03bb95d028920e54
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797760"
---
# <a name="quickstyletype-cell-quick-style-section"></a>QuickStyleType Cell (Quick Style Section)

Bestimmt den Typ der Schnellformatvorlagen (2-dimensionale, 1-dimensionales oder Connector), die das Shape erbt. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|0  <br/> |Visio wählt automatisch  <br/> |
|1  <br/> |1-dimensionales  <br/> |
|2  <br/> |2-dimensionale  <br/> |
|3  <br/> |Connector  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle **QuickStyleType** nach Namen aus, als Wert des Attributs **N** **ein Zellenelement** , einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | QuickStyleType  <br/> |
   
Wenn Sie einen Verweis auf die Zelle **QuickStyleType** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowQuickStyleProperties** <br/> |
| Zellenindex:  <br/> |**visQuickStyleType** <br/> |
   

