---
title: Zelle "NoFill" (Abschnitt "Geometry")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm710
ms.localizationpriority: medium
ms.assetid: 0ba7f6da-681b-b749-fe72-afbca23d7e16
description: Gibt an, ob ein Pfad gefüllt werden kann.
ms.openlocfilehash: 1e52e19e15f5a81d95e4509014e34614bed394a2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59627884"
---
# <a name="nofill-cell-geometry-section"></a>Zelle "NoFill" (Abschnitt "Geometry")

Gibt an, ob ein Pfad gefüllt werden kann.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
| TRUE  <br/> | Der Pfad ist nicht gefüllt, auch wenn andere Pfade im Shape gefüllt sind.  <br/> |
| FALSE  <br/> | Die Füllung des Shapes gilt für den Pfad, auch wenn dieser nicht geschlossen ist.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie das Füllmuster eines Shapes auf Null (=) setzen, wird keiner der Pfade gefüllt. Diese Zelle wird verwendet, um die Füllung für einen Pfad in einem Shape bei Bedarf auszuschalten.
  
Um einen Verweis auf die Zelle "NoFill" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Geometry  *i*  . NoFill where  *i*  = <1>, 2, 3...  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle NoFill anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionFirstComponent**  +   *i* where *i* = 0, 1, 2...  <br/> |
| Zeilenindex:  <br/> |**visRowComponent** <br/> |
| Zellenindex:  <br/> |**visCompNoFill** <br/> |
   

