---
title: Zelle "NoShow" (Abschnitt "Geometry")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm735
ms.localizationpriority: medium
ms.assetid: 831075ff-2875-b598-00bb-eb8481fee57b
description: Gibt an, ob ein Pfad auf dem Zeichenblatt angezeigt wird.
ms.openlocfilehash: 7d545fe9526cad6aca87998f7a62cfff0f9a314d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59577808"
---
# <a name="noshow-cell-geometry-section"></a>Zelle "NoShow" (Abschnitt "Geometry")

Gibt an, ob ein Pfad auf dem Zeichenblatt angezeigt wird.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
| TRUE  <br/> | Der Strich und die Füllung des Pfads, der durch den Abschnitt dargestellt wird, sind ausgeblendet.  <br/> |
| FALSE  <br/> | Der Strich und die Füllung des Pfades werden angezeigt.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Um einen Verweis auf die Zelle "NoShow" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Geometry  *i*  . NoShow where  *i*  = <1>, 2, 3...  <br/> |
   
Um einen Verweis auf die Zelle "NoShow" anhand des Indexes eines Programms abzurufen, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionFirstComponent**  +   *i* where *i* = 0, 1, 2...  <br/> |
| Zeilenindex:  <br/> |**visRowComponent** <br/> |
| Zellenindex:  <br/> |**visCompNoShow** <br/> |
   

