---
title: Zelle "Transparency" (Abschnitt "Character")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm50135
localization_priority: Normal
ms.assetid: ab835a1a-9e90-126e-279f-463882c48e93
description: Definiert die Transparenzstufe für einen Bereich der Textfarbe eines Shapes.
ms.openlocfilehash: 5914a061b1bba2173b338544b05abda8780ff164
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798295"
---
# <a name="transparency-cell-character-section"></a>Transparency Cell (Character Section)

Definiert die Transparenzstufe für einen Bereich der Textfarbe eines Shapes.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|0 – 100  <br/> |Stellt die Transparenz in Prozent dar. Der Standardwert ist 0% (vollständig undurchsichtig).  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Die Werte werden auf ein halbes Prozent gerundet. Ein Wert von 100 % bezeichnet völlige Transparenz. Ein Shape, dem ein völlig transparenter Text zugewiesen wurde, verhält sich auf dem Zeichenblatt zwar genauso wie ein Shape ohne Text, die Interaktion mit anderen Objekten auf dem Zeichenblatt erfolgt aber genauso wie bei einer Transparenz von 0 %.
  
Sie können diesen Wert auch festlegen, durch den Schieberegler auf der Registerkarte **Schriftart** im Dialogfeld **Text** verwenden (klicken Sie auf der Registerkarte **Start** auf den Pfeil neben **Schriftart** ). 
  
Wenn der Abschnitt Character über mehrere Zeilen verfügt, enthält die Zelle Transparency Formatierungsinformationen für einen Unterbereich des Texts eines Shapes. Andernfalls enthält diese Zelle Formatierungsinformationen für den gesamten Text des Shapes.
  
Zum Abrufen eines Verweises auf die Zelle Transparency nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Char.ColorTrans [ *i* ] wobei *i* = < 1 >, 2, 3...  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Transparency aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionCharacter** <br/> |
|Zeilenindex:  <br/> |**VisRowCharacter** +  *i* wobei *i* = 0, 1, 2...  <br/> |
|Zellenindex:  <br/> |**visCharacterColorTrans** <br/> |
   

