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
description: Der y-Offset der Aktionstagschaltfläche relativ zum durch die X- und Y-Zellen definierten Punkt.
ms.openlocfilehash: d7a1f5c1feda3624c9f96039e7247c737a91a813
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419982"
---
# <a name="y-justify-cell-action-tags-section"></a>Zelle "Y Justify" (Abschnitt "Action Tags")

Der  *y-Offset*  der Aktionstagschaltfläche relativ zum durch die X- und Y-Zellen definierten Punkt. 
  
> [!NOTE]
> In früheren Versionen von Microsoft Visio werden Aktionstags als Smarttags bezeichnet. 
  
|**Wert**|**Beschreibung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
| 0  <br/> | Oben ausgerichtet (Standard).  <br/> |**visSmartTagYJustifyTop** <br/> |
| 1  <br/> | Zentriert.  <br/> |**visSmartTagYJustifyMiddle** <br/> |
| 2  <br/> | Unten ausgerichtet.  <br/> |**visSmartTagYJustifyBottom** <br/> |
   
## <a name="remarks"></a>Hinweise

Die Zellen X Justify und Y Justify bestimmen, wo die Aktionstagschaltfläche im Verhältnis zum in den X- und Y-Zellen definierten Punkt platziert wird.
  
Um einen Verweis auf die Zelle "Y Justify" anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | SmartTags.  *Name*  . YJustify where SmartTags. *Name*  ist der Name der Aktionstagzeile  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle Y Justify nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionSmartTag** <br/> |
| Zeilenindex:  <br/> |**visRowSmartTag**  +   *i,* *wobei i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visSmartTagYJustify** <br/> |
   

