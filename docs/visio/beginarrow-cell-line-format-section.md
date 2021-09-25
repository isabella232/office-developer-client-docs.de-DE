---
title: Zelle "BeginArrow" (Abschnitt "Line Format")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm51105
ms.localizationpriority: medium
ms.assetid: 0ab4044e-2d77-1fbe-ef20-5d029bc064ba
description: Zeigt an, ob eine Linie eine Pfeilspitze oder eine andere Linienendformatierung an ihrem ersten Scheitelpunkt hat. Geben Sie eine Zahl zwischen 0 und 45 oder die USE-Funktion zusammen mit dem Namen des benutzerdefinierten Linienendes ein, oder verwenden Sie das Dialogfeld Linie.
ms.openlocfilehash: 9ad6aa363e54f9c11b6f5c9fc9b38ab52d6cb7a9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59554922"
---
# <a name="beginarrow-cell-line-format-section"></a>Zelle "BeginArrow" (Abschnitt "Line Format")

Zeigt an, ob eine Linie eine Pfeilspitze oder eine andere Linienendformatierung an ihrem ersten Scheitelpunkt hat. Geben Sie eine Zahl zwischen 0 und 45 oder die USE-Funktion zusammen mit dem Namen des benutzerdefinierten Linienendes ein, oder verwenden Sie das Dialogfeld **Linie**. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
| 0  <br/> | Keine Pfeilspitze  <br/> |
| 1 - 45  <br/> | Verschiedene Pfeilspitzenformatvorlagen, die den indizierten Einträgen im Dialogfeld **Linie** entsprechen.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Die Größe der Pfeilspitze wird in der Zelle PfeilBeginnGröße angegeben.
  
Verwenden Sie Folgendes, um einen Verweis auf die Zelle "BeginArrow" anhand des Namens aus einer anderen Formel oder eines Programms mithilfe der **CellsU-Eigenschaft** abzurufen: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | BeginArrow  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle BeginArrow anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowLine** <br/> |
| Zellenindex:  <br/> |**visLineBeginArrow** <br/> |
   

