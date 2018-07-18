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
ms.openlocfilehash: 5b0221c54c17a3b9957cce5e890842def0ba7525
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797164"
---
# <a name="hideforapply-cell-style-properties-section"></a>HideForApply Cell (Style Properties Section)

Bestimmt, wo eine Formatvorlage auf der Microsoft Visio-Benutzeroberfläche angezeigt wird.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
| TRUE  <br/> | 
          Formatvorlage nur im **Zeichnungsexplorer** anzeigen.
  <br/> |
| FALSE  <br/> | 
          Formatvorlage im **Zeichnungsexplorer** anzeigen.
  <br/> |
   
## <a name="remarks"></a>Hinweise

Wenn Sie eine neue Formatvorlage auf der Grundlage einer ausgeblendeten Formatvorlage erstellen, erbt die neue Formatvorlage dieses Attribut nicht.
  
Wenn Sie einen Verweis auf die Zelle HideForApply aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | HideForApply  <br/> |
   
Wenn Sie einen Verweis auf die Zelle HideForApply aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowStyle** <br/> |
| Zellenindex:  <br/> |**visStyleHidden** <br/> |
   

