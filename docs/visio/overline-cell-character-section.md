---
title: Zelle "Overline" (Abschnitt "Character")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251728
ms.localizationpriority: medium
ms.assetid: 102cce17-43ee-e313-3412-a72d6ee18fe6
description: Legt fest, ob der Text überstrichen ist.
ms.openlocfilehash: 4cf5c75f15fd9e40f5c59c9ff679de3de1dd9ae9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59623313"
---
# <a name="overline-cell-character-section"></a>Zelle "Overline" (Abschnitt "Character")

Legt fest, ob der Text überstrichen ist.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Text ist überstrichen.  <br/> |
|FALSE  <br/> |Text ist nicht überstrichen.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Sie können den Wert dieser Zelle auch festlegen, indem Sie das Dialogfeld **Text** verwenden (klicken Sie dazu auf der Registerkarte **Start** auf den Pfeil neben **Schriftart**). 
  
Um einen Verweis auf die Zelle "Overline" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Char.Overline[ *i*  ] where  *i*  = <1>, 2. 3...  <br/> |
   
Um einen Verweis auf die Zelle "Overline" anhand des Indexes eines Programms abzurufen, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionCharacter** <br/> |
|Zeilenindex:  <br/> |**visRowCharacter**  +   *i* where *i* = 0, 1, 2...  <br/> |
|Zellenindex:  <br/> |**visCharacterOverline** <br/> |
   

