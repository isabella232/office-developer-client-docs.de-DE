---
title: Zelle "EndTrigger" (Abschnitt "Glue Info")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251331
ms.localizationpriority: medium
ms.assetid: 8dc6515b-66ab-f1ac-18fd-820209f90991
description: Enthält eine von der Anwendung generierte Triggerformel, die festlegt, ob der Endpunkt eines 1D-Shapes zur Aufrechterhaltung seiner Verbindung zu einem anderen Shape verschoben werden soll.
ms.openlocfilehash: 395a53d792b8a9cad336c816be255d2ee4d15aca
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59619092"
---
# <a name="endtrigger-cell-glue-info-section"></a>Zelle "EndTrigger" (Abschnitt "Glue Info")

Enthält eine von der Anwendung generierte Triggerformel, die festlegt, ob der Endpunkt eines 1D-Shapes zur Aufrechterhaltung seiner Verbindung zu einem anderen Shape verschoben werden soll.
  
## <a name="remarks"></a>Bemerkungen

Wenn Sie ein 1D-Shape mit dynamischem Kleber an ein anderes Shape kleben, generiert Visio eine Formel, die sich auf die Zelle EventXFMod des anderen Shapes bezieht. Wird das Shape geändert, berechnet Visio erneut alle auf die Zelle EventXFMod bezogenen Formeln, einschließlich der Formel in der Zelle EndTrigger. Andere Formeln für das 1D-Shape beziehen sich auf die Zelle EndTrigger und verschieben den Endpunkt des 1D-Shapes oder verändern ggf. das Shape.
  
Verwenden Sie Folgendes, um einen Verweis auf die Zelle "EndTrigger" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | EndTrigger  <br/> |
   
Um einen Verweis auf die Zelle "EndTrigger" anhand des Indexes eines Programms abzurufen, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowMisc** <br/> |
| Zellenindex:  <br/> |**visEndTrigger** <br/> |
   

