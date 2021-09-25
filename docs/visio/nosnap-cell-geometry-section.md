---
title: Zelle "NoSnap" (Abschnitt "Geometry")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm740
ms.localizationpriority: medium
ms.assetid: 0e6c8621-868c-9eac-926b-3049f18023b0
description: Definiert, ob andere Shapes an einem Pfad einrasten.
ms.openlocfilehash: ffb32cf8c0506eb8b4064f455258a7153bc123df
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59623320"
---
# <a name="nosnap-cell-geometry-section"></a>Zelle "NoSnap" (Abschnitt "Geometry")

Definiert, ob andere Shapes an einem Pfad einrasten.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
| TRUE  <br/> | Andere Shapes können nicht an diesem Pfad einrasten.  <br/> |
| FALSE  <br/> | Andere Shapes können an diesem Pfad einrasten.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Verwenden Sie zum Abrufen eines Verweises auf die Zelle "NoSnap" anhand des Namens einer anderen Formel oder eines Programms mithilfe der **CellsU-Eigenschaft** Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Geometry  *i*  . NoSnap where  *i*  = <1>, 2, 3...  <br/> |
   
Um einen Verweis auf die Zelle "NoSnap" anhand des Indexes eines Programms abzurufen, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionFirstComponent**  +   *i* where *i* = 0, 1, 2...  <br/> |
| Zeilenindex:  <br/> |**visRowComponent** <br/> |
| Zeilenindex:  <br/> |**visCompNoSnap** <br/> |
   

