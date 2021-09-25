---
title: Zelle "TextDirection" (Abschnitt "Text Block Format ")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm995
ms.localizationpriority: medium
ms.assetid: 1df3a50e-7ea5-9244-1286-c1d00c217a9a
description: Bestimmt die Richtung der Zeichen in einem Textblock.
ms.openlocfilehash: d70cf6152fcb3e7ffbda69f6a6e6aaf758074fd1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59553690"
---
# <a name="textdirection-cell-text-block-format-section"></a>Zelle "TextDirection" (Abschnitt "Text Block Format ")

Bestimmt die Richtung der Zeichen in einem Textblock.
  
|**Wert**|**Direction**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
| 0  <br/> | Horizontal  <br/> |**visTxtBlkLeftToRight** <br/> |
| 1  <br/> | Vertikal  <br/> |**visTxtBlkTopToBottom** <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

In der japanischen Ausgabe von Visio Version  5.0 wurde der Wert dieser Zelle in der Zelle VerticalText im Abschnitt Miscellaneous gespeichert.
  
Um einen Verweis auf die Zelle "TextDirection" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | TextDirection  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle "TextDirection" anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowText** <br/> |
| Zellenindex:  <br/> |**visTxtBlkDirection** <br/> |
   

