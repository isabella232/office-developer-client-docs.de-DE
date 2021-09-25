---
title: Zelle "LineJumpFactorX" (Abschnitt "Page Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm545
ms.localizationpriority: medium
ms.assetid: 0649672f-f496-ce80-6dc3-3affc9b6f913
description: Bestimmt die Größe von Liniensprüngen auf horizontalen dynamischen Verbindern auf dem Zeichenblatt, und zwar relativ zum Wert der Zelle LineToLineX. Der Wert dieser Zelle kann im Bereich zwischen 0 und 10 liegen, jedoch sind Bruchwerte zwischen 0 und 1 empfehlenswert.
ms.openlocfilehash: 10ca7e60fb809b6adcdef6960322002ee18d0f80
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59566003"
---
# <a name="linejumpfactorx-cell-page-layout-section"></a>Zelle "LineJumpFactorX" (Abschnitt "Page Layout")

Bestimmt die Größe von Liniensprüngen auf horizontalen dynamischen Verbindern auf dem Zeichenblatt, und zwar relativ zum Wert der Zelle LineToLineX. Der Wert dieser Zelle kann im Bereich zwischen 0 und 10 liegen, jedoch sind Bruchwerte zwischen 0 und 1 empfehlenswert.
  
## <a name="remarks"></a>HinwBemerkungeneise

Sie können den Wert dieser Zelle auch im Dialogfeld **Seite einrichten** auf der Registerkarte **Layout und Routing** festlegen (klicken Sie dazu auf der Registerkarte **Entwurf** auf den Pfeil neben **Seite einrichten**, und klicken Sie dann auf **Layout und Routing**).
  
Um einen Verweis auf die Zelle "LineJumpFactorX" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |LineJumpFactorX  <br/> |
   
Um einen Verweis auf die Zelle "LineJumpFactorX" anhand des Indexes eines Programms abzurufen, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowPageLayout** <br/> |
|Zellenindex:  <br/> |**visPLOJumpFactorX** <br/> |
   

