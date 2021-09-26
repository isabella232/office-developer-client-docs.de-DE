---
title: Zelle "LineJumpFactorY" (Abschnitt "Page Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm550
ms.localizationpriority: medium
ms.assetid: 5a14be0d-9e3c-23c4-7782-bda5470d1243
description: Bestimmt die Größe von Liniensprüngen auf vertikalen dynamischen Verbindern auf dem Zeichenblatt, und zwar relativ zum Wert der Zelle LineToLineY. Der Wert dieser Zelle kann im Bereich zwischen 0 und 10 liegen, jedoch sind Bruchwerte zwischen 0 und 1 empfehlenswert.
ms.openlocfilehash: b5faf545682f80cfcc1b6774144791b1083439cc
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59612526"
---
# <a name="linejumpfactory-cell-page-layout-section"></a>Zelle "LineJumpFactorY" (Abschnitt "Page Layout")

Bestimmt die Größe von Liniensprüngen auf vertikalen dynamischen Verbindern auf dem Zeichenblatt, und zwar relativ zum Wert der Zelle LineToLineY. Der Wert dieser Zelle kann im Bereich zwischen 0 und 10 liegen, jedoch sind Bruchwerte zwischen 0 und 1 empfehlenswert.
  
## <a name="remarks"></a>Bemerkungen

Sie können den Wert dieser Zelle auch im Dialogfeld **Seite einrichten** auf der Registerkarte **Layout und Routing** festlegen (klicken Sie dazu auf der Registerkarte **Entwurf** auf den Pfeil neben **Seite einrichten**, und klicken Sie dann auf **Layout und Routing**).
  
Um einen Verweis auf die Zelle "LineJumpFactorY" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |LineJumpFactorY  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle LineJumpFactorY anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowPageLayout** <br/> |
|Zellenindex:  <br/> |**visPLOJumpFactorY** <br/> |
   

