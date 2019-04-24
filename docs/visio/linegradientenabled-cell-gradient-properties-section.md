---
title: Zelle "LineGradientEnabled" (Abschnitt "Gradient Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 276a661f-d14e-404a-a494-ae36601a8ce3
description: Bestimmt, ob ein Linienverlauf für eine Linie oder einen Rahmen einer Form aktiviert ist.
ms.openlocfilehash: 1d2b33275d26bb0c8e5550bcb7cf282c64d34544
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361138"
---
# <a name="linegradientenabled-cell-gradient-properties-section"></a>Zelle "LineGradientEnabled" (Abschnitt "Gradient Properties")

Bestimmt, ob ein Linienverlauf für eine Linie oder einen Rahmen einer Form aktiviert ist. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Der Farbverlauf wird auf der Linie oder dem Rahmen eines Shapes angezeigt.  <br/> |
|FALSE  <br/> |Farbverläufe werden nicht auf der Linie oder dem Rahmen eines Shapes angezeigt.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle **LineGradientEnabled** aus einer anderen Formel, nach dem Wert des **N** -Attributs eines **Cell** -Elements oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | LineGradientEnabled  <br/> |
   
Wenn Sie einen Verweis auf die Zelle **LineGradientEnabled** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowGradientProperties** <br/> |
| Zellenindex:  <br/> |**visLineGradientEnabled** <br/> |
   

