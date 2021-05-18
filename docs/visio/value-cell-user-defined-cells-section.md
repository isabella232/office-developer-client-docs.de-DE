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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422989"
---
# <a name="value-cell-user-defined-cells-section"></a>Zelle "Value" (Abschnitt "User-Defined Cells")

Gibt einen Wert für die entsprechende benutzerdefinierte Zelle an.
  
## <a name="remarks"></a>Hinweise

Wenn Sie auf diesen Wert in einer anderen Zelle verweisen möchten, geben Sie den in die Zeilenbeschriftung User.Row benutzerdefinierten Namen an.
  
Um einen Verweis auf die Zelle Value anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | User.  *Name*  . Wert, wobei User.  *Name*  ist der Zeilenname  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle Value nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionUser** <br/> |
| Zeilenindex:  <br/> |**visRowUser**  +   *i,* *wobei i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visUserValue** <br/> |
   

