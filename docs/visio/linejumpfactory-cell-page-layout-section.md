---
title: Zelle "LineJumpFactorY" (Abschnitt "Page Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm550
localization_priority: Normal
ms.assetid: 5a14be0d-9e3c-23c4-7782-bda5470d1243
description: Bestimmt die Größe von Liniensprüngen auf vertikalen dynamischen Verbindern auf dem Zeichenblatt, und zwar relativ zum Wert der Zelle LineToLineY. Der Wert dieser Zelle kann im Bereich zwischen 0 und 10 liegen, jedoch sind Bruchwerte zwischen 0 und 1 empfehlenswert.
ms.openlocfilehash: 36712c1558ff2f50309dc31e8f918061180c8fa4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411960"
---
# <a name="linejumpfactory-cell-page-layout-section"></a>Zelle "LineJumpFactorY" (Abschnitt "Page Layout")

Bestimmt die Größe von Liniensprüngen auf vertikalen dynamischen Verbindern auf dem Zeichenblatt, und zwar relativ zum Wert der Zelle LineToLineY. Der Wert dieser Zelle kann im Bereich zwischen 0 und 10 liegen, jedoch sind Bruchwerte zwischen 0 und 1 empfehlenswert.
  
## <a name="remarks"></a>Hinweise

Sie können den Wert dieser Zelle auch im Dialogfeld **Seite einrichten** auf der Registerkarte **Layout und Routing** festlegen (klicken Sie dazu auf der Registerkarte **Entwurf** auf den Pfeil neben **Seite einrichten**, und klicken Sie dann auf **Layout und Routing**).
  
Um einen Verweis auf die Zelle LineJumpFactorY anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |LineJumpFactorY  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die LineJumpFactorY-Zelle nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowPageLayout** <br/> |
|Zellenindex:  <br/> |**visPLOJumpFactorY** <br/> |
   

