---
title: Zelle "NoShow" (Abschnitt "Geometry")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm735
localization_priority: Normal
ms.assetid: 831075ff-2875-b598-00bb-eb8481fee57b
description: Gibt an, ob ein Pfad auf dem Zeichenblatt angezeigt wird.
ms.openlocfilehash: bd42b069e6796b107aafaea3080f6970c4f678c5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410350"
---
# <a name="noshow-cell-geometry-section"></a>Zelle "NoShow" (Abschnitt "Geometry")

Gibt an, ob ein Pfad auf dem Zeichenblatt angezeigt wird.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
| TRUE  <br/> | Der Strich und die Füllung des Pfads, der durch den Abschnitt dargestellt wird, sind ausgeblendet.  <br/> |
| FALSE  <br/> | Der Strich und die Füllung des Pfades werden angezeigt.  <br/> |
   
## <a name="remarks"></a>Hinweise

Um einen Verweis auf die Zelle NoShow anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Geometry  *i*  . NoShow,  *wobei i*  = <1>, 2, 3...  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle NoShow nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionFirstComponent**  +   *i,* *wobei i* = 0, 1, 2...  <br/> |
| Zeilenindex:  <br/> |**visRowComponent** <br/> |
| Zellenindex:  <br/> |**visCompNoShow** <br/> |
   

