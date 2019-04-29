---
title: Zelle "Y Justify" (Abschnitt "Action Tags")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1026937
localization_priority: Normal
ms.assetid: 27042b62-7623-95d7-7e10-f589d74605c7
description: Der y-Offset der Schaltfläche Aktionstag in Bezug auf den Punkt, der durch die Zellen X und Y definiert ist.
ms.openlocfilehash: d7a1f5c1feda3624c9f96039e7247c737a91a813
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419982"
---
# <a name="y-justify-cell-action-tags-section"></a>Zelle "Y Justify" (Abschnitt "Action Tags")

Der *y* -Offset der Schaltfläche Aktionstag in Bezug auf den Punkt, der durch die Zellen X und y definiert ist. 
  
> [!NOTE]
> In früheren Versionen von Microsoft Visio werden Aktionstags als Smarttags bezeichnet. 
  
|**Wert**|**Beschreibung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
| 0  <br/> | Oben ausgerichtet (Standard).  <br/> |**visSmartTagYJustifyTop** <br/> |
| 1  <br/> | Zentriert.  <br/> |**visSmartTagYJustifyMiddle** <br/> |
| 2  <br/> | Unten ausgerichtet.  <br/> |**visSmartTagYJustifyBottom** <br/> |
   
## <a name="remarks"></a>Bemerkungen

Die Zellen X Blocksatz und Y-Ausrichtung legen fest, wo die Schaltfläche Aktionstag in Bezug auf den in den Zellen X und Y definierten Punkt angeordnet wird.
  
Wenn Sie einen Verweis auf die Zelle Y Blocksatz aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Smarttags.  *Name* . YJustify, wobei SmartTags. *Name* ist der Name der Zeile mit dem Aktionstag.  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Y Blocksatz aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionSmartTag** <br/> |
| Zeilenindex:  <br/> |**visRowSmartTag** +  *i* , wobei *i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visSmartTagYJustify** <br/> |
   

