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
ms.openlocfilehash: a49d7a38eac75a2845de0ca3ad22f7cbf79a63df
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413185"
---
# <a name="displaymode-cell-group-properties-section"></a>Zelle "DisplayMode" (Abschnitt "Group Properties")

Bestimmt, wie das Gruppen-Shape und dessen Mitglieder angezeigt werden.
  
|**Wert**|**Anzeigemodus**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
|0  <br/> |Blendet das Gruppen-Shape und den Text aus.  <br/> |**visGrpDispModeNone** <br/> |
|1  <br/> |Zeigt das Gruppen-Shape hinter den Mitglieds-Shapes an.  <br/> |**visGrpDispModeBack** <br/> |
|2  <br/> |Zeigt das Gruppen-Shape vor den Mitglieds-Shapes an.  <br/> |**visGrpDispModeFront** <br/> |
   
## <a name="remarks"></a>Bemerkungen

Sie können diesen Wert auch festlegen, indem Sie die Gruppe auswählen, auf der Registerkarte [Entwickler](run-in-developer-mode-display-the-developer-tab.md) in der Gruppe **Shape-Design** auf **Verhalten** klicken und dann in der **Gruppe Daten** Liste einen Anzeigemodus auswählen. 
  
Wenn Sie einen Verweis auf die Zelle wird Display Mode aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |DisplayMode  <br/> |
   
Wenn Sie einen Verweis auf die Zelle wird Display Mode aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowGroup** <br/> |
|Zellenindex:  <br/> |**visGroupDisplayMode** <br/> |
   

