---
title: Zelle "Value" (Abschnitt "Text Fields")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1095
ms.localizationpriority: medium
ms.assetid: 3ca662c8-1ce4-89a9-3264-1ba533fcd444
description: Enthält die Funktion für ein Feld.
ms.openlocfilehash: b81a384ac5a0327fb1725c2297389e334907579b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59569839"
---
# <a name="value-cell-text-fields-section"></a>Zelle "Value" (Abschnitt "Text Fields")

Enthält die Funktion für ein Feld.
  
## <a name="remarks"></a>HinwBemerkungeneise

Sie können den Wert dieser Zelle im Dialogfeld **Feld** festlegen (klicken Sie dazu auf der Registerkarte **Einfügen** in der Gruppe **Text** auf **Feld**).
  
Verwenden Sie Folgendes, um einen Verweis auf die Zelle Value anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Fields.Value[ *i*  ] where  *i*  = <1>, 2, 3...  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle Value anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionTextField** <br/> |
|Zeilenindex:  <br/> |**visRowField**  +   *i* where *i* = 0, 1, 2...  <br/> |
|Zellenindex:  <br/> |**visFieldCell** <br/> |
   

