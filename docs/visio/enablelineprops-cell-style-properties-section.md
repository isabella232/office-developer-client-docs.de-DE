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
ms.openlocfilehash: 38964194626be052b2a168fa929b69ebe4b28e01
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410000"
---
# <a name="enablelineprops-cell-style-properties-section"></a>Zelle "EnableLineProps" (Abschnitt "Style Properties")

Bestimmt, ob eine Formatvorlage Linieneigenschaften enthält.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Linieneigenschaften einschließen.  <br/> |
|FALSE  <br/> |Linieneigenschaften ausschließen.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle "EnableLineProps aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |"EnableLineProps  <br/> |
   
Wenn Sie einen Verweis auf die Zelle "EnableLineProps aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowStyle** <br/> |
|Zellenindex:  <br/> |**visStyleIncludesLine** <br/> |
   

