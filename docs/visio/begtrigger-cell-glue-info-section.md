---
title: Zelle "BegTrigger" (Abschnitt "Glue Info")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm100
ms.localizationpriority: medium
ms.assetid: 0b7ffe39-ee6c-71eb-355c-9bb4660260f1
description: Enthält eine von der Anwendung generierte Triggerformel, die festlegt, ob der Anfangspunkt eines 1D-Shapes zur Aufrechterhaltung seiner Verbindung zu einem anderen Shape verschoben werden soll.
ms.openlocfilehash: 745dfed2762dc9b3f10d3da576609ec9b8cce36d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59598808"
---
# <a name="begtrigger-cell-glue-info-section"></a>Zelle "BegTrigger" (Abschnitt "Glue Info")

Enthält eine von der Anwendung generierte Triggerformel, die festlegt, ob der Anfangspunkt eines 1D-Shapes zur Aufrechterhaltung seiner Verbindung zu einem anderen Shape verschoben werden soll.
  
## <a name="remarks"></a>HinwBemerkungeneise

Wenn Sie ein 1D-Shape mit dynamischem Kleber an ein anderes Shape kleben, generiert die Anwendung eine Formel, die sich auf die Zelle EventXFMod eines anderen Shapes bezieht. Wenn das Shape geändert wird, berechnet Visio alle auf die Zelle EventXFMod bezogenen Formeln neu, einschließlich der Formel in der Zelle BegTrigger. Andere Formeln für das 1D-Shape beziehen sich auf die Zelle BegTrigger und verschieben den Anfangspunkt des 1D-Shape oder verändern ggf. das Shape entsprechend.
  
Um einen Verweis auf die Zelle "BegTrigger" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | BegTrigger  <br/> |
   
Um einen Verweis auf die Zelle "BegTrigger" anhand des Indexes eines Programms abzurufen, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowGroup** <br/> |
| Zellenindex:  <br/> |**visBegTrigger** <br/> |
   

