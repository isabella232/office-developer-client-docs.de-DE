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
ms.openlocfilehash: 002f628841356ec8a22afbb9d4aeca8236058222
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796712"
---
# <a name="conlinejumpcode-cell-shape-layout-section"></a>ConLineJumpCode Cell (Shape Layout Section)

Bestimmt die Bedingungen für einen Verbindersprung.
  
|**Wert**|**Beschreibung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
|0  <br/> |
          Klicken Sie gemäß den Angaben auf dem Zeichenblatt auf der Registerkarte **Entwurf** in der Gruppe **Seite einrichten** auf den Pfeil, und klicken Sie anschließend auf die Registerkarte **Layout und Routing**, um die Zeichenblattspezifikationen anzuzeigen.
  <br/> |**visSLOJumpDefault** <br/> |
|1  <br/> |Nie  <br/> |**visSLOJumpNever** <br/> |
|2  <br/> |Immer  <br/> |**visSLOJumpAlways** <br/> |
|3  <br/> |Andere Verbindersprünge  <br/> |**visSLOJumpOther** <br/> |
|4  <br/> |
          Keine Verbindersprünge
  <br/> |**visSLOJumpNeither** <br/> |
   
## <a name="remarks"></a>Bemerkungen

Sie können auch den Wert für diese Zelle festlegen einen dynamischen Verbinder, indem Sie in der Gruppe **Shape-Design** auf der Registerkarte [Entwicklertools](run-in-developer-mode-display-the-developer-tab.md) auf **Verhalten** klicken und dann auf die Registerkarte **Verbinder** . 
  
Wenn Sie einen Verweis auf die Zelle ConLineJumpCode aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |ConLineJumpCode  <br/> |
   
Wenn Sie einen Verweis auf die Zelle ConLineJumpCode aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowShapeLayout** <br/> |
|Zellenindex:  <br/> |**visSLOJumpCode** <br/> |
   

