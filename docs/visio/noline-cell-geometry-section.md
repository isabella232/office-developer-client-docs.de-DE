---
title: Zelle "NoLine" (Abschnitt "Geometry")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm715
ms.localizationpriority: medium
ms.assetid: f9624af2-c087-3dde-9140-339c438b3652
description: Legt fest, ob eine Linie um die Grenze des Pfads gezogen wird.
ms.openlocfilehash: 6631d30da00f63f89314d362f981d888256d36f9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59573873"
---
# <a name="noline-cell-geometry-section"></a>Zelle "NoLine" (Abschnitt "Geometry")

Legt fest, ob eine Linie um die Grenze des Pfads gezogen wird.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
| TRUE  <br/> | Es wird keine Linie um die Grenze eines Pfads gezogen, bei der es sich um die Grenze eines ausgefüllten Bereichs handelt.  <br/> |
| FALSE  <br/> | Es wird eine Linie um die Grenze eines Pfades gezogen.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Wenn Sie die Farbe einer Linie in weiß ändern, ist diese Linie immer noch vorhanden, auch wenn sie vor einem weißen Hintergrund nicht mehr angezeigt wird. Wenn Sie in diese Zelle den Wert WAHR einsetzen, wird keine Linie gezogen.
  
Um einen Verweis auf die Zelle "NoLine" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Geometry  *i*  . NoLine where  *i*  = <1>, 2, 3...  <br/> |
   
Um einen Verweis auf die Zelle "NoLine" anhand des Indexes eines Programms abzurufen, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionFirstComponent**  +   *i* where *i* = 0, 1, 2...  <br/> |
| Zeilenindex:  <br/> |**visRowComponent** <br/> |
| Zellenindex:  <br/> |**visCompNoLine** <br/> |
   

