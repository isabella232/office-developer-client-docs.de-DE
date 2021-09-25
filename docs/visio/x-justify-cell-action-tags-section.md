---
title: Zelle "X Justify" (Abschnitt "Action Tags")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1026936
ms.localizationpriority: medium
ms.assetid: a8995020-3eaa-2b2c-eca0-dd475de4d06f
description: Der X-Offset der Aktionstag-Schaltfläche relativ zu dem von den Zellen X und Y definierten Punkt.
ms.openlocfilehash: 87c9e85923f1d1a9be836e3221ab3be3c1c4afc5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59582546"
---
# <a name="x-justify-cell-action-tags-section"></a>Zelle "X Justify" (Abschnitt "Action Tags")

Der  *X-Offset*  der Aktionstag-Schaltfläche relativ zu dem von den Zellen X und Y definierten Punkt. 
  
> [!NOTE]
> In früheren Versionen von Microsoft Visio werden Aktionstags als Smarttags bezeichnet. 
  
|**Wert**|**Beschreibung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
| 0  <br/> | Links ausgerichtet (Standard).  <br/> |**visSmartTagXJustifyLeft** <br/> |
| 1  <br/> | Zentriert.  <br/> |**visSmartTagXJustifyCenter** <br/> |
| 2  <br/> | Rechts ausgerichtet.  <br/> |**visSmartTagXJustifyRight** <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Die Zellen X Justify und Y Justify bestimmen, wo die Schaltfläche des Aktionstags in Bezug auf den in den Zellen X und Y definierten Punkt platziert wird. 
  
Um einen Verweis auf die Zelle "X Justify" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | SmartTags.  *Name*  . XJustify where SmartTags. *Name*  ist der Name der Aktionstagzeile  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle X Justify anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionSmartTag** <br/> |
| Zeilenindex:  <br/> |**visRowSmartTag**  +   *i* where *i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visSmartTagXJustify** <br/> |
   

