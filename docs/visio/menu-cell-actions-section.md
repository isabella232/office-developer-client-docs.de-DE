---
title: Zelle "Menu" (Abschnitt "Actions")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm690
localization_priority: Normal
ms.assetid: 29af746c-b081-24cf-a30d-a56353ee849e
description: Definiert den Namen eines Menüelements, das in einem Kontext- oder Aktionstagmenü für ein Shape oder Zeichenblatt angezeigt wird.
ms.openlocfilehash: adb6915c34946472ada8c4ab4d02fa88bab6651a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436328"
---
# <a name="menu-cell-actions-section"></a>Zelle "Menu" (Abschnitt "Actions")

Definiert den Namen eines Menüelements, das in einem Kontext- oder Aktionstagmenü für ein Shape oder Zeichenblatt angezeigt wird. 
  
> [!NOTE]
> In früheren Versionen von Microsoft Visio werden Aktionstags als Smarttags bezeichnet. 
  
## <a name="remarks"></a>Hinweise

Wenn Sie über diesem Element ein Trennzeichen in das Menü einfügen möchten, verwenden Sie die Zelle BeginGroup. Um den Befehl unten im Menü anzuzeigen, geben Sie vor dem Namen ein Prozentzeichen (%) ein.
  
Verwenden Sie zum Erhalten eines Verweises auf die Zelle Menu anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft:** 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Aktionen. *Name*  . Menuwhere-Aktionen.  *Name*  ist der Name der Zeile Aktionen  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle Menu nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionAction** <br/> |
|Zeilenindex:  <br/> |**visRowAction**  +   *i* where i = 0, 1, 2, ...  <br/> |
|Zellenindex:  <br/> |**visActionMenu** <br/> |
   

