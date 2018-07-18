---
title: Zelle "EnableTextProps" (Abschnitt "Style Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251697
localization_priority: Normal
ms.assetid: 8c59abaf-d2cc-94c9-08ba-004bc40efd9e
description: Bestimmt, ob eine Formatvorlage Texteigenschaften enthält.
ms.openlocfilehash: a51f83624192615e84292129d4788ae1e2779c6a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796929"
---
# <a name="enabletextprops-cell-style-properties-section"></a>EnableTextProps Cell (Style Properties Section)

Bestimmt, ob eine Formatvorlage Texteigenschaften enthält.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Texteigenschaften einschließen.  <br/> |
|FALSE  <br/> |Texteigenschaften ausschließen.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle EnableTextProps aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |EnableTextProps  <br/> |
   
Wenn Sie einen Verweis auf die Zelle EnableTextProps aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowStyle** <br/> |
|Zellenindex:  <br/> |**visStyleIncludesText** <br/> |
   

