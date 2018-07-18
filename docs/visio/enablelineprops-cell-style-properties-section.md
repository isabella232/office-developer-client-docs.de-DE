---
title: Zelle "EnableLineProps" (Abschnitt "Style Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251696
localization_priority: Normal
ms.assetid: 9f619416-36ff-1479-6232-225c11827e01
description: Bestimmt, ob eine Formatvorlage Linieneigenschaften enthält.
ms.openlocfilehash: 0e1eb67528b3e87bcfff5281dd1e0b2db3a0a4d5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796927"
---
# <a name="enablelineprops-cell-style-properties-section"></a>EnableLineProps Cell (Style Properties Section)

Bestimmt, ob eine Formatvorlage Linieneigenschaften enthält.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Linieneigenschaften einschließen.  <br/> |
|FALSE  <br/> |Linieneigenschaften ausschließen.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle EnableLineProps aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |EnableLineProps  <br/> |
   
Wenn Sie einen Verweis auf die Zelle EnableLineProps aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowStyle** <br/> |
|Zellenindex:  <br/> |**visStyleIncludesLine** <br/> |
   

