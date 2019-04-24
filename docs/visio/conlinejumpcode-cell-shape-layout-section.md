---
title: Zelle "ConLineJumpCode" (Abschnitt "Shape Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251652
localization_priority: Normal
ms.assetid: af85588e-8e83-5168-7a8c-d7e8b4af5c27
description: Bestimmt die Bedingungen für einen Verbindersprung.
ms.openlocfilehash: 28bf506b8d3729fefec438d259746661fd28586e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32284088"
---
# <a name="conlinejumpcode-cell-shape-layout-section"></a>Zelle "ConLineJumpCode" (Abschnitt "Shape Layout")

Bestimmt die Bedingungen für einen Verbindersprung.
  
|**Wert**|**Beschreibung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
|0  <br/> |Klicken Sie gemäß den Angaben auf dem Zeichenblatt auf der Registerkarte **Entwurf** in der Gruppe **Seite einrichten** auf den Pfeil, und klicken Sie anschließend auf die Registerkarte **Layout und Routing**, um die Zeichenblattspezifikationen anzuzeigen.  <br/> |**visSLOJumpDefault** <br/> |
|1  <br/> |Never  <br/> |**visSLOJumpNever** <br/> |
|2  <br/> |Always  <br/> |**visSLOJumpAlways** <br/> |
|3  <br/> |Andere Verbindersprünge  <br/> |**visSLOJumpOther** <br/> |
|4  <br/> |Keine Verbindersprünge  <br/> |**visSLOJumpNeither** <br/> |
   
## <a name="remarks"></a>Bemerkungen

Sie können den Wert dieser Zelle auch festlegen, indem Sie einen dynamischen Verbinder auswählen, auf der Registerkarte [Entwickler](run-in-developer-mode-display-the-developer-tab.md) in der Gruppe **Shape-Design** auf **Verhalten** klicken und dann auf die Registerkarte **Verbinder** klicken. 
  
Wenn Sie einen Verweis auf die Zelle Zelle ConLineJumpCode aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Zelle ConLineJumpCode  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Zelle ConLineJumpCode aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowShapeLayout** <br/> |
|Zellenindex:  <br/> |**visSLOJumpCode** <br/> |
   

