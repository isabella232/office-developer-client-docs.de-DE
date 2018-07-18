---
title: Zelle "Action" (Abschnitt "Actions")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm5
localization_priority: Normal
ms.assetid: 435e49ee-0b51-8ce3-0589-3f0717026f4a
description: Enthält die Formel, die ausgeführt werden soll, wenn ein Benutzer einen Befehl in einem Kontext- oder Aktionstagmenü auswählt.
ms.openlocfilehash: 123b05f9a08c4ffa656e08a51f019f888cf83ed4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796373"
---
# <a name="action-cell-actions-section"></a>Action Cell (Actions Section)

Enthält die Formel, die ausgeführt werden soll, wenn ein Benutzer einen Befehl in einem Kontext- oder Aktionstagmenü auswählt.
  
> [!NOTE]
> In früheren Versionen von Microsoft Visio werden Aktionstags als Smarttags bezeichnet. 
  
## <a name="remarks"></a>Hinweise

Die Zelle Action wird nur ausgewertet, wenn die Aktion stattfindet und nicht bei Eingabe der Formel.
  
Wenn Sie einen Verweis auf die Zelle Action aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Aktionen.  *Name* . Aktion wobei Aktionen. *Name* ist der Name der Zeile actions  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Action aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionAction** <br/> |
| Zeilenindex:  <br/> |**VisRowAction** +  *i* wobei *i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visActionAction** <br/> |
   

