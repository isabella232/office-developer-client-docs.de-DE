---
title: Zelle "ResizeMode" (Abschnitt "Shape Transform")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251203
localization_priority: Normal
ms.assetid: 49816e46-fa83-3ee4-1451-9c85fbd0f519
description: Zeigt die aktuelle Einstellung für das Größenänderungsverhalten in Bezug auf das Shape an.
ms.openlocfilehash: a32f5dbc935e85a49ab585073ca6a31215fd102a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797884"
---
# <a name="resizemode-cell-shape-transform-section"></a>ResizeMode Cell (Shape Transform Section)

Zeigt die aktuelle Einstellung für das Größenänderungsverhalten in Bezug auf das Shape an.
  
|**Wert**|**Beschreibung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
|0  <br/> |Einstellung der Gruppe verwenden.  <br/> |**visXFormResizeDontCare** <br/> |
|1  <br/> |Nur neu positionieren.  <br/> |**visXFormResizeSpread** <br/> |
|2  <br/> |Mit Gruppe skalieren.  <br/> |**visXFormResizeScale** <br/> |
   
## <a name="remarks"></a>Bemerkungen

Sie können diesen Wert auch auf der Registerkarte **Verhalten** im Dialogfeld **Verhalten** festlegen (klicken Sie auf der Registerkarte [Entwicklertools](run-in-developer-mode-display-the-developer-tab.md)in der Gruppe **Shape-Design** auf **Verhalten**). Wenn Sie einen Verweis auf die Zelle ResizeMode nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |ResizeMode  <br/> |
   
Wenn Sie einen Verweis auf die Zelle ResizeMode aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowXFormOut** <br/> |
|Zellenindex:  <br/> |**visXFormResizeMode** <br/> |
   

