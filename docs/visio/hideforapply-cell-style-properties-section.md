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
description: Bestimmt, wo eine Formatvorlage auf der Microsoft Visio-Benutzeroberfläche angezeigt wird.
ms.openlocfilehash: 7b3830488770a66d7be35923e1807dbcdcd1f1c3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423244"
---
# <a name="hideforapply-cell-style-properties-section"></a>Zelle "HideForApply" (Abschnitt "Style Properties")

Bestimmt, wo eine Formatvorlage auf der Microsoft Visio-Benutzeroberfläche angezeigt wird.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
| TRUE  <br/> | Formatvorlage nur im **Zeichnungsexplorer** anzeigen.  <br/> |
| FALSE  <br/> | Formatvorlage im **Zeichnungsexplorer** anzeigen.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie eine neue Formatvorlage auf der Grundlage einer ausgeblendeten Formatvorlage erstellen, erbt die neue Formatvorlage dieses Attribut nicht.
  
Wenn Sie einen Verweis auf die Zelle "HideForApply aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | "HideForApply  <br/> |
   
Wenn Sie einen Verweis auf die Zelle "HideForApply aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowStyle** <br/> |
| Zellenindex:  <br/> |**visStyleHidden** <br/> |
   

