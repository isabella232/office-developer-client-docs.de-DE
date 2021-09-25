---
title: Zelle "Y Justify" (Abschnitt "Action Tags")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1026937
ms.localizationpriority: medium
ms.assetid: 27042b62-7623-95d7-7e10-f589d74605c7
description: Der y-Offset der Aktionstag-Schaltfläche relativ zu dem von den Zellen X und Y definierten Punkt.
ms.openlocfilehash: 2a06a0fc889ea5e88526da5656550050b5f46d08
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59581699"
---
# <a name="y-justify-cell-action-tags-section"></a>Zelle "Y Justify" (Abschnitt "Action Tags")

Der  *y-Offset*  der Aktionstag-Schaltfläche relativ zu dem von den Zellen X und Y definierten Punkt. 
  
> [!NOTE]
> In früheren Versionen von Microsoft Visio werden Aktionstags als Smarttags bezeichnet. 
  
|**Wert**|**Beschreibung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
| 0  <br/> | Oben ausgerichtet (Standard).  <br/> |**visSmartTagYJustifyTop** <br/> |
| 1  <br/> | Zentriert.  <br/> |**visSmartTagYJustifyMiddle** <br/> |
| 2  <br/> | Unten ausgerichtet.  <br/> |**visSmartTagYJustifyBottom** <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Die Zellen X Justify und Y Justify bestimmen, wo die Schaltfläche des Aktionstags in Bezug auf den in den Zellen X und Y definierten Punkt platziert wird.
  
Um einen Verweis auf die Zelle "Y Justify" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | SmartTags.  *Name*  . YJustify where SmartTags. *Name*  ist der Name der Aktionstagzeile  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle Y Justify anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionSmartTag** <br/> |
| Zeilenindex:  <br/> |**visRowSmartTag**  +   *i* where *i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visSmartTagYJustify** <br/> |
   

