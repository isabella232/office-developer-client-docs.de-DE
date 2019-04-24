---
title: Zelle "BegTrigger" (Abschnitt "Glue Info")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm100
localization_priority: Normal
ms.assetid: 0b7ffe39-ee6c-71eb-355c-9bb4660260f1
description: Enthält eine von der Anwendung generierte Triggerformel, die festlegt, ob der Anfangspunkt eines 1D-Shapes zur Aufrechterhaltung seiner Verbindung zu einem anderen Shape verschoben werden soll.
ms.openlocfilehash: b401d349119337016a96b5fffbc26f7be2891864
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360355"
---
# <a name="begtrigger-cell-glue-info-section"></a>Zelle "BegTrigger" (Abschnitt "Glue Info")

Enthält eine von der Anwendung generierte Triggerformel, die festlegt, ob der Anfangspunkt eines 1D-Shapes zur Aufrechterhaltung seiner Verbindung zu einem anderen Shape verschoben werden soll.
  
## <a name="remarks"></a>Bemerkungen

Wenn Sie ein 1D-Shape mit dynamischem Kleber an ein anderes Shape kleben, generiert die Anwendung eine Formel, die sich auf die Zelle EventXFMod eines anderen Shapes bezieht. Wenn das Shape geändert wird, berechnet Visio alle auf die Zelle EventXFMod bezogenen Formeln neu, einschließlich der Formel in der Zelle BegTrigger. Andere Formeln für das 1D-Shape beziehen sich auf die Zelle BegTrigger und verschieben den Anfangspunkt des 1D-Shape oder verändern ggf. das Shape entsprechend.
  
Wenn Sie einen Verweis auf die Zelle Zelle BegTrigger aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Zelle BegTrigger  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Zelle BegTrigger aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowGroup** <br/> |
| Zellenindex:  <br/> |**visBegTrigger** <br/> |
   

