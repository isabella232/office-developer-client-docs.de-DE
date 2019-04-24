---
title: Zelle "Value" (Abschnitt "User-Defined Cells")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1100
localization_priority: Normal
ms.assetid: 495b2aec-e197-75eb-9974-e7c92d26546f
description: Gibt einen Wert für die entsprechende benutzerdefinierte Zelle an.
ms.openlocfilehash: 137d22430829f96a9c6ad69a73a6b44e964d5f4f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355895"
---
# <a name="value-cell-user-defined-cells-section"></a>Zelle "Value" (Abschnitt "User-Defined Cells")

Gibt einen Wert für die entsprechende benutzerdefinierte Zelle an.
  
## <a name="remarks"></a>Bemerkungen

Wenn Sie auf diesen Wert in einer anderen Zelle verweisen möchten, geben Sie den in die Zeilenbeschriftung User.Row benutzerdefinierten Namen an.
  
Wenn Sie einen Verweis auf die Zelle Wert aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Benutzer.  *Name* . Wert, bei dem Benutzer.  *Name* ist der Name der Zeile  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Value nach Index aus einem Programm abrufen möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionUser** <br/> |
| Zeilenindex:  <br/> |**visRowUser** +  *i* , wobei *i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visUserValue** <br/> |
   

