---
title: Zelle "HideForApply" (Abschnitt "Style Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251698
localization_priority: Normal
ms.assetid: 62d87db9-b8ca-60b6-bf27-5168c718ec96
description: Bestimmt, wo eine Formatvorlage auf der Microsoft-Visio angezeigt wird.
ms.openlocfilehash: 7b3830488770a66d7be35923e1807dbcdcd1f1c3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423244"
---
# <a name="hideforapply-cell-style-properties-section"></a>Zelle "HideForApply" (Abschnitt "Style Properties")

Bestimmt, wo eine Formatvorlage auf der Microsoft-Visio angezeigt wird.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
| TRUE  <br/> | Formatvorlage nur im **Zeichnungsexplorer** anzeigen.  <br/> |
| FALSE  <br/> | Formatvorlage im **Zeichnungsexplorer** anzeigen.  <br/> |
   
## <a name="remarks"></a>Hinweise

Wenn Sie eine neue Formatvorlage auf der Grundlage einer ausgeblendeten Formatvorlage erstellen, erbt die neue Formatvorlage dieses Attribut nicht.
  
Um einen Verweis auf die Zelle HideForApply anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | HideForApply  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die HideForApply-Zelle nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowStyle** <br/> |
| Zellenindex:  <br/> |**visStyleHidden** <br/> |
   

