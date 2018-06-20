---
title: Zelle "IsSnapTarget" (Abschnitt "Group Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251626
localization_priority: Normal
ms.assetid: b58131f6-a566-d9ca-bad4-4f4b66e03aaf
description: Legt fest, ob der Einrastvorgang an einer Gruppe oder an einzelnen Shapes in dieser Gruppe erfolgt.
ms.openlocfilehash: 89536923617f80768d7c14658cb07c97595824ea
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797249"
---
# <a name="issnaptarget-cell-group-properties-section"></a>Zelle "IsSnapTarget" (Abschnitt "Group Properties")

Legt fest, ob der Einrastvorgang an einer Gruppe oder an einzelnen Shapes in dieser Gruppe erfolgt.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Einrasten an Shapes in einer Gruppe aktivieren.  <br/> |
|FALSE  <br/> |Nur an der Gruppe einrasten.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Sie können diesen Wert auch festlegen, indem Auswählen der Gruppe auf der Registerkarte [Entwicklertools](run-in-developer-mode-display-the-developer-tab.md) **Verhalten** klicken und anschließend das Kontrollkästchen **an Mitglieds-Shapes ausrichten** . 
  
Wenn Sie einen Verweis auf die Zelle IsSnapTarget nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |IsSnapTarget  <br/> |
   
Wenn Sie einen Verweis auf die Zelle IsSnapTarget aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowGroup** <br/> |
|Zellenindex:  <br/> |**visGroupIsSnapTarget** <br/> |
   

