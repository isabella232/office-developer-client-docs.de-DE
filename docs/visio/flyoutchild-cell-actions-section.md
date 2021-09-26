---
title: Zelle "FlyoutChild" (Abschnitt "Aktionen")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm80003
ms.localizationpriority: medium
ms.assetid: b2405457-843c-0d46-5f4f-9c413826c3f1
description: Bestimmt, ob die Zeile ein untergeordnetes Erweiterungsmenü der letzten Zeile oberhalb befindlichen Zeile ist, bei der es sich nicht um eine untergeordnete Erweiterung handelt.
ms.openlocfilehash: e5409d16df7b91c855a95e7b9deb2121ec4e63b3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59612799"
---
# <a name="flyoutchild-cell-actions-section"></a>Zelle "FlyoutChild" (Abschnitt "Aktionen")

Bestimmt, ob die Zeile ein untergeordnetes Erweiterungsmenü der letzten Zeile oberhalb befindlichen Zeile ist, bei der es sich nicht um eine untergeordnete Erweiterung handelt. 
  
## <a name="remarks"></a>Bemerkungen

Um einen Verweis auf die Zelle "FlyoutChild" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes. 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Aktionen. *Name*  . FlyoutChildwhere Actions.  *Name*  ist der Name der Zeile "Aktionen"  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle FlyoutChild anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionAction** <br/> |
|Zeilenindex:  <br/> |**visRowAction**  +   *i* where *i* = 0, 1, 2...  <br/> |
|Zellenindex:  <br/> |**visActionFlyoutChild** <br/> |
   

