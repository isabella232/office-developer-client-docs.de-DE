---
title: Zelle "X Justify" (Abschnitt "Action Tags")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1026936
localization_priority: Normal
ms.assetid: a8995020-3eaa-2b2c-eca0-dd475de4d06f
description: Die x - Abstand der Schaltfläche Aktionstag in Bezug auf den Punkt, der durch die Zellen X und Y definiert ist.
ms.openlocfilehash: 043d7b198ae5a529c623545fb54ef5aa1d32217d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798435"
---
# <a name="x-justify-cell-action-tags-section"></a>X Justify Cell (Action Tags Section)

Die *X* -Abstand der Schaltfläche Aktionstag in Bezug auf den Punkt, der durch die Zellen X und Y definiert ist. 
  
> [!NOTE]
> In früheren Versionen von Microsoft Visio werden Aktionstags als Smarttags bezeichnet. 
  
|**Wert**|**Beschreibung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
| 0  <br/> | Links ausgerichtet (Standard).  <br/> |**visSmartTagXJustifyLeft** <br/> |
| 1  <br/> | Zentriert.  <br/> |**visSmartTagXJustifyCenter** <br/> |
| 2  <br/> | Rechts ausgerichtet.  <br/> |**visSmartTagXJustifyRight** <br/> |
   
## <a name="remarks"></a>Hinweise

Die Zellen X Justify und Y Justify bestimmen, wo die Schaltfläche Aktionstag in Bezug auf die Zellen X und Y definierten Punkt platziert wird. 
  
Zum Abrufen eines Verweises auf die Zelle X Justify nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | SmartTags.  *Name* . XJustify wobei SmartTags. *Name* ist der Name der Zeile Aktionstag  <br/> |
   
Wenn Sie einen Verweis auf die Zelle X Justify aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionSmartTag** <br/> |
| Zeilenindex:  <br/> |**VisRowSmartTag** +  *i* wobei *i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visSmartTagXJustify** <br/> |
   

