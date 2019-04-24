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
ms.openlocfilehash: 7e9080fcd4604e2dbdc1dae31992f05e5b512213
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326880"
---
# <a name="resizemode-cell-shape-transform-section"></a>Zelle "ResizeMode" (Abschnitt "Shape Transform")

Zeigt die aktuelle Einstellung für das Größenänderungsverhalten in Bezug auf das Shape an.
  
|**Wert**|**Beschreibung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
|0  <br/> |Einstellung der Gruppe verwenden.  <br/> |**visXFormResizeDontCare** <br/> |
|1  <br/> |Nur neu positionieren.  <br/> |**visXFormResizeSpread** <br/> |
|2  <br/> |Mit Gruppe skalieren.  <br/> |**visXFormResizeScale** <br/> |
   
## <a name="remarks"></a>Bemerkungen

Sie können diesen Wert auch im Dialogfeld **Verhalten** auf der Registerkarte **Verhalten** festlegen (Klicken Sie auf der Registerkarte [Entwicklertools](run-in-developer-mode-display-the-developer-tab.md)in der Gruppe **Shape-Design** auf **Verhalten**). Wenn Sie einen Verweis auf die Zelle Zelle ResizeMode aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Zelle ResizeMode  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Zelle ResizeMode aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowXFormOut** <br/> |
|Zellenindex:  <br/> |**visXFormResizeMode** <br/> |
   

