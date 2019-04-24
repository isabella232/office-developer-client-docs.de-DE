---
title: Zelle "Checked" (Abschnitt "Actions")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm155
localization_priority: Normal
ms.assetid: 50937e29-eaa1-0cd0-53cc-dc17e7793e55
description: Gibt an, ob ein Element im Kontext- oder Aktionstagmenü aktiviert ist.
ms.openlocfilehash: 870823f28d802e7cafa81efbe5617f27b6714885
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341846"
---
# <a name="checked-cell-actions-section"></a>Zelle "Checked" (Abschnitt "Actions")

Gibt an, ob ein Element im Kontext- oder Aktionstagmenü aktiviert ist.
  
> [!NOTE]
> In früheren Versionen von Microsoft Visio werden Aktionstags als Smarttags bezeichnet. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Häkchen wird angezeigt.  <br/> |
|FALSE  <br/> |Häkchen wird nicht angezeigt (Standardeinstellung).  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die markierte Zelle aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Aktionen. *Name* . Überprüft, wo Aktionen. *Name* ist der Name der Zeile Actions.  <br/> |
   
Wenn Sie einen Bezug auf die Zelle checked aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionAction** <br/> |
|Zeilenindex:  <br/> |**visRowAction** +  *i* , wobei *i* = 0, 1, 2,...  <br/> |
|Zellenindex:  <br/> |**visActionChecked** <br/> |
   

