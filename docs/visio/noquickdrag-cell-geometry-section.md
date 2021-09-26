---
title: Zelle "NoQuickDrag" (Abschnitt "Geometrie")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm80004
ms.localizationpriority: medium
ms.assetid: 8491f459-9de2-8e75-5532-7d3bd0986734
description: Bestimmt, ob ein Shape ausgewählt oder gezogen werden kann, wenn der Benutzer auf den im Abschnitt Geometrie definierten ausgefüllten Bereich klickt.
ms.openlocfilehash: 052080f2334eb776e8a50d608724a6faa445d2ab
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59627870"
---
# <a name="noquickdrag-cell-geometry-section"></a>Zelle "NoQuickDrag" (Abschnitt "Geometrie")

Bestimmt, ob ein Shape ausgewählt oder gezogen werden kann, wenn der Benutzer auf den im Abschnitt Geometrie definierten ausgefüllten Bereich klickt.
  
## <a name="remarks"></a>Bemerkungen

Um einen Verweis auf die Zelle "NoQuickDrag" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Geometry  *i*  . NoQuickDrag, where * i * - <1>, 2, 3...  <br/> |
   
Verwenden Sie zum Abrufen eines Verweises auf die Zelle "NoQuickDrag" anhand des Indexes eines Programms die **CellsSRC-Eigenschaft** mit den folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionFirstComponent**  +   *i* , wobei *i* = 0, 1, 2...  <br/> |
|Zeilenindex:  <br/> |**visRowComponent** <br/> |
|Zellenindex:  <br/> |**visCompNoQuickDrag** <br/> |
   

