---
title: Zelle "EnableFillProps" (Abschnitt "Style Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm300
localization_priority: Normal
ms.assetid: 2b3334de-588c-6cf3-bc88-be03ae71b1a6
description: Bestimmt, ob eine Formatvorlage Füllbereichseigenschaften enthält.
ms.openlocfilehash: 55191cb28d5777f7fb65a3a1e4be890e6dda4e8b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345563"
---
# <a name="enablefillprops-cell-style-properties-section"></a>Zelle "EnableFillProps" (Abschnitt "Style Properties")

Bestimmt, ob eine Formatvorlage Füllbereichseigenschaften enthält.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Füllbereichseigenschaften einschließen.  <br/> |
|FALSE  <br/> |Füllbereichseigenschaften ausschließen.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle "EnableFillProps aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |"EnableFillProps  <br/> |
   
Wenn Sie einen Verweis auf die Zelle "EnableFillProps aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowStyle** <br/> |
|Zellenindex:  <br/> |**visStyleIncludesFill** <br/> |
   

