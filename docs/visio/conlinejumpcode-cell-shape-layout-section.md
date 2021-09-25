---
title: Zelle "ConLineJumpCode" (Abschnitt "Shape Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251652
ms.localizationpriority: medium
ms.assetid: af85588e-8e83-5168-7a8c-d7e8b4af5c27
description: Bestimmt die Bedingungen für einen Verbindersprung.
ms.openlocfilehash: e1caea1f839bb139c41051f288c7e6b160767768
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59582911"
---
# <a name="conlinejumpcode-cell-shape-layout-section"></a>Zelle "ConLineJumpCode" (Abschnitt "Shape Layout")

Bestimmt die Bedingungen für einen Verbindersprung.
  
|**Wert**|**Beschreibung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
|0  <br/> |Klicken Sie gemäß den Angaben auf dem Zeichenblatt auf der Registerkarte **Entwurf** in der Gruppe **Seite einrichten** auf den Pfeil, und klicken Sie anschließend auf die Registerkarte **Layout und Routing**, um die Zeichenblattspezifikationen anzuzeigen.  <br/> |**visSLOJumpDefault** <br/> |
|1  <br/> |Nie  <br/> |**visSLOJumpNever** <br/> |
|2  <br/> |Immer  <br/> |**visSLOJumpAlways** <br/> |
|3  <br/> |Andere Verbindersprünge  <br/> |**visSLOJumpOther** <br/> |
|4   <br/> |Keine Verbindersprünge  <br/> |**visSLOJumpNeither** <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Sie können den Wert dieser Zelle auch festlegen, indem Sie einen dynamischen Verbinder auswählen, in der Gruppe **"Shape-Design"** auf der Registerkarte ["Entwickler"](run-in-developer-mode-display-the-developer-tab.md) auf **"Verhalten"** klicken und dann auf die Registerkarte **"Connector"** klicken. 
  
Um einen Verweis auf die Zelle "ConLineJumpCode" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |ConLineJumpCode  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle ConLineJumpCode anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowShapeLayout** <br/> |
|Zellenindex:  <br/> |**visSLOJumpCode** <br/> |
   

