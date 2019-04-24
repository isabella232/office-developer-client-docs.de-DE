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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341083"
---
# <a name="noshow-cell-geometry-section"></a>Zelle "NoShow" (Abschnitt "Geometry")

Gibt an, ob ein Pfad auf dem Zeichenblatt angezeigt wird.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
| TRUE  <br/> | Der Strich und die Füllung des Pfads, der durch den Abschnitt dargestellt wird, sind ausgeblendet.  <br/> |
| FALSE  <br/> | Der Strich und die Füllung des Pfades werden angezeigt.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle noShow aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Geometrie *i* . NoShow Where *i* = <1>, 2, 3...  <br/> |
   
Wenn Sie einen Verweis auf die Zelle noShow aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionFirstComponent** +  *i* , wobei *i* = 0, 1, 2...  <br/> |
| Zeilenindex:  <br/> |**visRowComponent** <br/> |
| Zellenindex:  <br/> |**visCompNoShow** <br/> |
   

