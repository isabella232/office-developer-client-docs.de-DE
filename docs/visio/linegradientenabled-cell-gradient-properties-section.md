---
title: LineGradientEnabled Cell (Gradient Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 276a661f-d14e-404a-a494-ae36601a8ce3
description: Bestimmt, ob für eine Linie oder den Rahmen eines Shapes ein Linie Farbverlauf aktiviert ist.
ms.openlocfilehash: d78a94a25c0290bd5e58522c9a45955868f31b32
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797316"
---
# <a name="linegradientenabled-cell-gradient-properties-section"></a>LineGradientEnabled Cell (Gradient Properties Section)

Bestimmt, ob für eine Linie oder den Rahmen eines Shapes ein Linie Farbverlauf aktiviert ist. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Farbverlauf wird in einer Zeile oder den Rahmen einer Form angezeigt.  <br/> |
|FALSE  <br/> |Verläufe werden nicht in einer Zeile oder den Rahmen einer Form angezeigt.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle **LineGradientEnabled** nach Namen aus, als Wert des Attributs **N** **ein Zellenelement** , einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | LineGradientEnabled  <br/> |
   
Wenn Sie einen Verweis auf die Zelle **LineGradientEnabled** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowGradientProperties** <br/> |
| Zellenindex:  <br/> |**visLineGradientEnabled** <br/> |
   

