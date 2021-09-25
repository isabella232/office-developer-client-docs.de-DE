---
title: Zelle "Comment" (Abschnitt "Miscellaneous")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm170
ms.localizationpriority: medium
ms.assetid: 6f52ed60-d58b-86e6-f7e2-2ef19d4afa75
description: Enthält den Kommentartext im Zeichenformat für ein Shape.
ms.openlocfilehash: 6e243599d4f370e477f52868c980e37f461dc902
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59603746"
---
# <a name="comment-cell-miscellaneous-section"></a>Zelle "Comment" (Abschnitt "Miscellaneous")

Enthält den Kommentartext im Zeichenformat für ein Shape.
  
## <a name="remarks"></a>HinwBemerkungeneise

Sie können einen Kommentar auch einfügen, indem Sie auf der Registerkarte **Überprüfen** auf **Neuer Kommentar** klicken. 
  
Um einen Verweis auf die Zelle "Comment" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Kommentar  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle Comment anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowMisc** <br/> |
|Zellenindex:  <br/> |**visComment** <br/> |
   

