---
title: Zelle "Transparency" (Abschnitt "Character")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm50135
ms.localizationpriority: medium
ms.assetid: ab835a1a-9e90-126e-279f-463882c48e93
description: Definiert die Transparenzstufe für einen Bereich der Textfarbe eines Shapes.
ms.openlocfilehash: 78818abb78e1a96cb35977ec9920bab98d4546f8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59569895"
---
# <a name="transparency-cell-character-section"></a>Zelle "Transparency" (Abschnitt "Character")

Definiert die Transparenzstufe für einen Bereich der Textfarbe eines Shapes.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|0 - 100  <br/> |Stellt die Transparenz in Prozent dar. Der Standardwert ist 0% (vollständig undurchsichtig).  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Die Werte werden auf ein halbes Prozent gerundet. Ein Wert von 100 % bezeichnet völlige Transparenz. Ein Shape, dem ein völlig transparenter Text zugewiesen wurde, verhält sich auf dem Zeichenblatt zwar genauso wie ein Shape ohne Text, die Interaktion mit anderen Objekten auf dem Zeichenblatt erfolgt aber genauso wie bei einer Transparenz von 0 %.
  
Sie können diesen Wert auch mithilfe des Schieberegler-Steuerelements auf der Registerkarte **Schriftart** im Dialogfeld **Text** festlegen (klicken Sie auf der Registerkarte **"Start"** auf den **Schriftartpfeil).** 
  
Wenn der Abschnitt Character über mehrere Zeilen verfügt, enthält die Zelle Transparency Formatierungsinformationen für einen Unterbereich des Texts eines Shapes. Andernfalls enthält diese Zelle Formatierungsinformationen für den gesamten Text des Shapes.
  
Verwenden Sie Folgendes, um einen Verweis auf die Zelle Transparency anhand des Namens einer anderen Formel oder eines Programms mithilfe der **CellsU-Eigenschaft** abzurufen: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Char.ColorTrans[ *i*  ] where  *i*  = <1>, 2, 3...  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle Transparency anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionCharacter** <br/> |
|Zeilenindex:  <br/> |**visRowCharacter**  +   *i* where *i* = 0, 1, 2...  <br/> |
|Zellenindex:  <br/> |**visCharacterColorTrans** <br/> |
   

