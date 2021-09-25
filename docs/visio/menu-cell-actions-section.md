---
title: Zelle "Menu" (Abschnitt "Actions")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm690
ms.localizationpriority: medium
ms.assetid: 29af746c-b081-24cf-a30d-a56353ee849e
description: Definiert den Namen eines Menüelements, das in einem Kontext- oder Aktionstagmenü für ein Shape oder Zeichenblatt angezeigt wird.
ms.openlocfilehash: b03986c20e578917331cb002850dbb62f9c2deef
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59577871"
---
# <a name="menu-cell-actions-section"></a>Zelle "Menu" (Abschnitt "Actions")

Definiert den Namen eines Menüelements, das in einem Kontext- oder Aktionstagmenü für ein Shape oder Zeichenblatt angezeigt wird. 
  
> [!NOTE]
> In früheren Versionen von Microsoft Visio werden Aktionstags als Smarttags bezeichnet. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Wenn Sie über diesem Element ein Trennzeichen in das Menü einfügen möchten, verwenden Sie die Zelle BeginGroup. Um den Befehl unten im Menü anzuzeigen, geben Sie vor dem Namen ein Prozentzeichen (%) ein.
  
Verwenden Sie Folgendes, um einen Verweis auf die Zelle "Menu" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Aktionen. *Name*  . Menuwhere Actions.  *Name*  ist der Name der Zeile "Aktionen"  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle Menu anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionAction** <br/> |
|Zeilenindex:  <br/> |**visRowAction**  +   *i* where i = 0, 1, 2, ...  <br/> |
|Zellenindex:  <br/> |**visActionMenu** <br/> |
   

