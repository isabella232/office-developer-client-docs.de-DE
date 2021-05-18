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
description: Der x-Offset der Aktionstagschaltfläche relativ zum durch die X- und Y-Zellen definierten Punkt.
ms.openlocfilehash: f8542d2f3a22b12794d999323d202d7a5bece20b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414123"
---
# <a name="x-justify-cell-action-tags-section"></a>Zelle "X Justify" (Abschnitt "Action Tags")

Der  *x-Offset*  der Aktionstagschaltfläche relativ zum durch die X- und Y-Zellen definierten Punkt. 
  
> [!NOTE]
> In früheren Versionen von Microsoft Visio werden Aktionstags als Smarttags bezeichnet. 
  
|**Wert**|**Beschreibung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
| 0  <br/> | Links ausgerichtet (Standard).  <br/> |**visSmartTagXJustifyLeft** <br/> |
| 1  <br/> | Zentriert.  <br/> |**visSmartTagXJustifyCenter** <br/> |
| 2  <br/> | Rechts ausgerichtet.  <br/> |**visSmartTagXJustifyRight** <br/> |
   
## <a name="remarks"></a>Hinweise

Die Zellen X Justify und Y Justify bestimmen, wo die Aktionstagschaltfläche im Verhältnis zum in den X- und Y-Zellen definierten Punkt platziert wird. 
  
Verwenden Sie zum Erhalten eines Verweises auf die Zelle X Justify anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft:** 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | SmartTags.  *Name*  . XJustify where SmartTags. *Name*  ist der Name der Aktionstagzeile  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die X Justify-Zelle nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionSmartTag** <br/> |
| Zeilenindex:  <br/> |**visRowSmartTag**  +   *i,* *wobei i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visSmartTagXJustify** <br/> |
   

