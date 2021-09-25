---
title: Zelle "SpLine" (Abschnitt "Paragraph")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm970
ms.localizationpriority: medium
ms.assetid: 84f4e5f1-7c28-9e83-8644-28d117bb10a5
description: Legt den Abstand zwischen einer Textzeile und der nächsten in Prozent fest. 100 % ist dabei die Höhe einer Textzeile.
ms.openlocfilehash: 38a565eafcdd64da9fe4dfb041e76c584e392322
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59553781"
---
# <a name="spline-cell-paragraph-section"></a>Zelle "SpLine" (Abschnitt "Paragraph")

Legt den Abstand zwischen einer Textzeile und der nächsten in Prozent fest. 100 % ist dabei die Höhe einer Textzeile.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
| \>0  <br/> | Absoluter Abstand, unabhängig vom Schriftgrad  <br/> |
| =0  <br/> | Fester Abstand (Abstand = 100 % des Schriftgrads)  <br/> |
| \<0  <br/> | Ein Prozentsatz des Schriftgrads (z. B. -120 % ergibt einen Abstand von 120 %)  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Um einen Verweis auf die Zelle "SpLine" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Para. SpLine [  *i*  ] where  *i*  = <1>, 2, 3...  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle "SpLine" anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionParagraph** <br/> |
| Zeilenindex:  <br/> |**visRowParagraph**  +   *i* where *i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visSpaceLine** <br/> |
   

