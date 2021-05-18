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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421620"
---
# <a name="conlinejumpcode-cell-shape-layout-section"></a>Zelle "ConLineJumpCode" (Abschnitt "Shape Layout")

Bestimmt die Bedingungen für einen Verbindersprung.
  
|**Wert**|**Beschreibung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
|0  <br/> |Klicken Sie gemäß den Angaben auf dem Zeichenblatt auf der Registerkarte **Entwurf** in der Gruppe **Seite einrichten** auf den Pfeil, und klicken Sie anschließend auf die Registerkarte **Layout und Routing**, um die Zeichenblattspezifikationen anzuzeigen.  <br/> |**visSLOJumpDefault** <br/> |
|1  <br/> |Nie  <br/> |**visSLOJumpNever** <br/> |
|2  <br/> |Always  <br/> |**visSLOJumpAlways** <br/> |
|3  <br/> |Andere Verbindersprünge  <br/> |**visSLOJumpOther** <br/> |
|4   <br/> |Keine Verbindersprünge  <br/> |**visSLOJumpNeither** <br/> |
   
## <a name="remarks"></a>Hinweise

Sie können den Wert dieser Zelle auch festlegen, indem Sie einen dynamischen [](run-in-developer-mode-display-the-developer-tab.md) Connector auswählen, **auf** der Registerkarte Entwickler in der Gruppe **Shape-Entwurf** auf Verhalten klicken und dann auf die Registerkarte **Connector** klicken. 
  
Verwenden Sie zum Erhalten eines Verweises auf die Zelle ConLineJumpCode anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft:** 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |ConLineJumpCode  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die ConLineJumpCode-Zelle nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowShapeLayout** <br/> |
|Zellenindex:  <br/> |**visSLOJumpCode** <br/> |
   

