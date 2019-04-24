---
title: Zelle "NoFill" (Abschnitt "Geometry")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm710
localization_priority: Normal
ms.assetid: 0ba7f6da-681b-b749-fe72-afbca23d7e16
description: Gibt an, ob ein Pfad gefüllt werden kann.
ms.openlocfilehash: 301f30b644e338ff9e597a7a7d8226b9c8a4462f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357253"
---
# <a name="nofill-cell-geometry-section"></a>Zelle "NoFill" (Abschnitt "Geometry")

Gibt an, ob ein Pfad gefüllt werden kann.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
| TRUE  <br/> | Der Pfad ist nicht gefüllt, auch wenn andere Pfade im Shape gefüllt sind.  <br/> |
| FALSE  <br/> | Die Füllung des Shapes gilt für den Pfad, auch wenn dieser nicht geschlossen ist.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie das Füllmuster eines Shapes auf Null (=) setzen, wird keiner der Pfade gefüllt. Diese Zelle wird verwendet, um die Füllung für einen Pfad in einem Shape bei Bedarf auszuschalten.
  
Wenn Sie einen Verweis auf die Zelle nofill aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Geometrie *i* . NoFill Where *i* = <1>, 2, 3...  <br/> |
   
Wenn Sie einen Verweis auf die Zelle nofill aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionFirstComponent** +  *i* , wobei *i* = 0, 1, 2...  <br/> |
| Zeilenindex:  <br/> |**visRowComponent** <br/> |
| Zellenindex:  <br/> |**visCompNoFill** <br/> |
   

