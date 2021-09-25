---
title: Zelle "Value" (Abschnitt "User-Defined Cells")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1100
ms.localizationpriority: medium
ms.assetid: 495b2aec-e197-75eb-9974-e7c92d26546f
description: Gibt einen Wert für die entsprechende benutzerdefinierte Zelle an.
ms.openlocfilehash: 00a96f98682ace7c66ddba8c7aa7ac3a284a224c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59559346"
---
# <a name="value-cell-user-defined-cells-section"></a>Zelle "Value" (Abschnitt "User-Defined Cells")

Gibt einen Wert für die entsprechende benutzerdefinierte Zelle an.
  
## <a name="remarks"></a>HinwBemerkungeneise

Wenn Sie auf diesen Wert in einer anderen Zelle verweisen möchten, geben Sie den in die Zeilenbeschriftung User.Row benutzerdefinierten Namen an.
  
Verwenden Sie Folgendes, um einen Verweis auf die Zelle Value anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Benutzer.  *Name*  . Wert, bei dem Benutzer.  *Name*  ist der Zeilenname  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle Value anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionUser** <br/> |
| Zeilenindex:  <br/> |**visRowUser**  +   *i* where *i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visUserValue** <br/> |
   

