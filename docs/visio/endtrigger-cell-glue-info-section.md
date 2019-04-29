---
title: Zelle "EndTrigger" (Abschnitt "Glue Info")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251331
localization_priority: Normal
ms.assetid: 8dc6515b-66ab-f1ac-18fd-820209f90991
description: Enthält eine von der Anwendung generierte Triggerformel, die festlegt, ob der Endpunkt eines 1D-Shapes zur Aufrechterhaltung seiner Verbindung zu einem anderen Shape verschoben werden soll.
ms.openlocfilehash: 9093cca782d9262b2511198ed73f512a75bb8994
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418582"
---
# <a name="endtrigger-cell-glue-info-section"></a>Zelle "EndTrigger" (Abschnitt "Glue Info")

Enthält eine von der Anwendung generierte Triggerformel, die festlegt, ob der Endpunkt eines 1D-Shapes zur Aufrechterhaltung seiner Verbindung zu einem anderen Shape verschoben werden soll.
  
## <a name="remarks"></a>Bemerkungen

Wenn Sie ein 1D-Shape mit dynamischem Kleber an ein anderes Shape kleben, generiert Visio eine Formel, die sich auf die Zelle EventXFMod des anderen Shapes bezieht. Wird das Shape geändert, berechnet Visio erneut alle auf die Zelle EventXFMod bezogenen Formeln, einschließlich der Formel in der Zelle EndTrigger. Andere Formeln für das 1D-Shape beziehen sich auf die Zelle EndTrigger und verschieben den Endpunkt des 1D-Shapes oder verändern ggf. das Shape.
  
Wenn Sie einen Verweis auf die Zelle Zelle EndTrigger aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Zelle EndTrigger  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Zelle EndTrigger aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowMisc** <br/> |
| Zellenindex:  <br/> |**visEndTrigger** <br/> |
   

