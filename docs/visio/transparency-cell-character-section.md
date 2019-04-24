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
ms.openlocfilehash: 8619ec25372ae163fff1759aca36ff6693820e39
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280983"
---
# <a name="transparency-cell-character-section"></a>Zelle "Transparency" (Abschnitt "Character")

Definiert die Transparenzstufe für einen Bereich der Textfarbe eines Shapes.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|0 - 100  <br/> |Stellt die Transparenz in Prozent dar. Der Standardwert ist 0% (vollständig undurchsichtig).  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Die Werte werden auf ein halbes Prozent gerundet. Ein Wert von 100 % bezeichnet völlige Transparenz. Ein Shape, dem ein völlig transparenter Text zugewiesen wurde, verhält sich auf dem Zeichenblatt zwar genauso wie ein Shape ohne Text, die Interaktion mit anderen Objekten auf dem Zeichenblatt erfolgt aber genauso wie bei einer Transparenz von 0 %.
  
Sie können diesen Wert auch festlegen, indem Sie das Schieberegler-Steuerelement auf der Registerkarte **Schriftart** im Dialogfeld **Text** verwenden (Klicken Sie auf der Registerkarte **Start** auf den Pfeil **Schriftart** ). 
  
Wenn der Abschnitt Character über mehrere Zeilen verfügt, enthält die Zelle Transparency Formatierungsinformationen für einen Unterbereich des Texts eines Shapes. Andernfalls enthält diese Zelle Formatierungsinformationen für den gesamten Text des Shapes.
  
Wenn Sie einen Verweis auf die Zelle Transparency aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Char. ColorTrans [ *i* ] wobei *i* = <1>, 2, 3...  <br/> |
   
Wenn Sie einen Verweis auf die Zelle "Transparency" aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionCharacter** <br/> |
|Zeilenindex:  <br/> |**visRowCharacter** +  *i* , wobei *i* = 0, 1, 2...  <br/> |
|Zellenindex:  <br/> |**visCharacterColorTrans** <br/> |
   

