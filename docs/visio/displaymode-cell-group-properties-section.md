---
title: Zelle "DisplayMode" (Abschnitt "Group Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251623
localization_priority: Normal
ms.assetid: e6d72529-aa03-e94b-130c-79ed04336299
description: Bestimmt, wie das Gruppen-Shape und dessen Mitglieder angezeigt werden.
ms.openlocfilehash: 086685b47d8eaf170a8722f7cd00545230541e79
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796854"
---
# <a name="displaymode-cell-group-properties-section"></a>DisplayMode Cell (Group Properties Section)

Bestimmt, wie das Gruppen-Shape und dessen Mitglieder angezeigt werden.
  
|**Wert**|**Anzeigemodus**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
|0  <br/> |Blendet das Gruppen-Shape und den Text aus.  <br/> |**visGrpDispModeNone** <br/> |
|1  <br/> |Zeigt das Gruppen-Shape hinter den Mitglieds-Shapes an.  <br/> |**visGrpDispModeBack** <br/> |
|2  <br/> |Zeigt das Gruppen-Shape vor den Mitglieds-Shapes an.  <br/> |**visGrpDispModeFront** <br/> |
   
## <a name="remarks"></a>Bemerkungen

Sie können diesen Wert auch festlegen durch die Gruppe auswählen auf die Gruppe **Shape-Design** auf der Registerkarte [Entwicklertools](run-in-developer-mode-display-the-developer-tab.md) **Verhalten** klicken und anschließend einen Anzeigemodus aus der Liste **Gruppe** auswählen. 
  
Wenn Sie einen Verweis auf die Zelle DisplayMode aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |DisplayMode  <br/> |
   
Wenn Sie einen Verweis auf die Zelle DisplayMode aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowGroup** <br/> |
|Zellenindex:  <br/> |**visGroupDisplayMode** <br/> |
   

