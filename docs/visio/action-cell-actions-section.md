---
title: Zelle "Action" (Abschnitt "Actions")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm5
ms.localizationpriority: medium
ms.assetid: 435e49ee-0b51-8ce3-0589-3f0717026f4a
description: Enthält die Formel, die ausgeführt werden soll, wenn ein Benutzer einen Befehl in einem Kontext- oder Aktionstagmenü auswählt.
ms.openlocfilehash: 8e1aec829904719f71dde6e87905784e78bd0a1d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59608697"
---
# <a name="action-cell-actions-section"></a>Zelle "Action" (Abschnitt "Actions")

Enthält die Formel, die ausgeführt werden soll, wenn ein Benutzer einen Befehl in einem Kontext- oder Aktionstagmenü auswählt.
  
> [!NOTE]
> In früheren Versionen von Microsoft Visio werden Aktionstags als Smarttags bezeichnet. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Die Zelle Action wird nur ausgewertet, wenn die Aktion stattfindet und nicht bei Eingabe der Formel.
  
Verwenden Sie zum Abrufen eines Verweises auf die Zelle Action anhand des Namens einer anderen Formel oder eines Programms mithilfe der **CellsU-Eigenschaft** Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Aktionen.  *Name*  . Aktion, wobei Aktionen. *Name*  ist der Name der Aktionszeile  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle Action anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionAction** <br/> |
| Zeilenindex:  <br/> |**visRowAction**  +   *i* where *i* = 0, 1, 2...  <br/> |
| Zeilenindex:  <br/> |**visActionAction** <br/> |
   

