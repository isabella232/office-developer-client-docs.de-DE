---
title: Zelle "Flags" (Abschnitt "Paragraph")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033782
ms.localizationpriority: medium
ms.assetid: 898bf89d-d00f-9769-a89d-787ef708eca5
description: Gibt an, ob die Textrichtung von links nach rechts oder von rechts nach links verläuft.
ms.openlocfilehash: c2c32bb7316b4a2909c557ac4fdbc69705f481e3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59612813"
---
# <a name="flags-cell-paragraph-section"></a>Zelle "Flags" (Abschnitt "Paragraph")

Gibt an, ob die Textrichtung von links nach rechts oder von rechts nach links verläuft.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|0  <br/> |Die Textrichtung verläuft von links nach rechts (Standardwert).  <br/> |
|1  <br/> |Die Textrichtung verläuft von rechts nach links.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Der Wert in dieser Zelle entspricht der Einstellung **Richtung** auf der Registerkarte Absatz im Dialogfeld Text (klicken Sie auf der Registerkarte Start auf den Pfeil neben Schriftart), die nur angezeigt wird, wenn im Dialogfeld **"Spracheinstellungen" Microsoft Office** Sprache hinzugefügt wurde.     (Klicken Sie auf **"Start",** auf **"Alle Programme",** auf **Microsoft Office,** auf **Microsoft Office "Extras"** und dann auf **Microsoft Office "Spracheinstellungen".)** 
  
Um einen Verweis auf die Zelle "Flags" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Para.Flags[ *i*  ] where  *i*  = <1>, 2, 3...  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle "Flags" anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionParagraph** <br/> |
|Zeilenindex:  <br/> |**visRowParagraph**  +   *i* where *i* = 0, 1, 2...  <br/> |
|Zellenindex:  <br/> |**visFlags** <br/> |
   

