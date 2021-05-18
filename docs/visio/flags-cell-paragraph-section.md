---
title: Zelle "Flags" (Abschnitt "Paragraph")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033782
localization_priority: Normal
ms.assetid: 898bf89d-d00f-9769-a89d-787ef708eca5
description: Gibt an, ob die Textrichtung von links nach rechts oder von rechts nach links verläuft.
ms.openlocfilehash: af1e79b13d3d8bab2e7271eb79e68cf931871806
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413115"
---
# <a name="flags-cell-paragraph-section"></a>Zelle "Flags" (Abschnitt "Paragraph")

Gibt an, ob die Textrichtung von links nach rechts oder von rechts nach links verläuft.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|0  <br/> |Die Textrichtung verläuft von links nach rechts (Standardwert).  <br/> |
|1  <br/> |Die Textrichtung verläuft von rechts nach links.  <br/> |
   
## <a name="remarks"></a>Hinweise

Der Wert in dieser  Zelle entspricht  der Einstellung Richtung auf der  Registerkarte Absatz im  Dialogfeld **Text** (klicken Sie auf der Registerkarte Start auf den Pfeil Schriftart), die nur angezeigt wird, wenn eine Sprache, die komplexen Skripts Text verwendet, im Dialogfeld **Microsoft Office Spracheinstellungen** hinzugefügt wurde. (Klicken **Sie auf Start,** **klicken** Sie auf Alle Programme, **Microsoft Office**, klicken Sie **Microsoft Office Tools** und dann auf **Microsoft Office Spracheinstellungen**.) 
  
Um einen Verweis auf die Zelle Flags anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Para.Flags[ *i*  ] where  *i*  = <1>, 2, 3...  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Flags-Zelle nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionParagraph** <br/> |
|Zeilenindex:  <br/> |**visRowParagraph**  +   *i,* *wobei i* = 0, 1, 2...  <br/> |
|Zellenindex:  <br/> |**visFlags** <br/> |
   

