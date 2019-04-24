---
title: Zelle "PageLineJumpDirX" (Abschnitt "Page Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251656
localization_priority: Normal
ms.assetid: 77892ec7-4c6a-78a5-5af4-5b6be7709e77
description: Bestimmt die Richtung von Liniensprüngen auf horizontalen dynamischen Verbindern auf dem Zeichenblatt, für die Sie keine lokale Liniensprungrichtung festgelegt haben.
ms.openlocfilehash: 4e1213990877e1260cc8cecd5a55beda4592a844
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283737"
---
# <a name="pagelinejumpdirx-cell-page-layout-section"></a>Zelle "PageLineJumpDirX" (Abschnitt "Page Layout")

Bestimmt die Richtung von Liniensprüngen auf horizontalen dynamischen Verbindern auf dem Zeichenblatt, für die Sie keine lokale Liniensprungrichtung festgelegt haben.
  
|**Wert**|**Liniensprungrichtung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
| 0  <br/> | Standard, nach links oder die Einstellung des Zeichenblatts für Shapes  <br/> |**visLOJumpDirXDefault** <br/> |
| 1  <br/> | Nach oben  <br/> |**visLOJumpDirXUp** <br/> |
| 2  <br/> | Nach unten  <br/> |**visLOJumpDirXDown** <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle Zelle PageLineJumpDirX aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Zelle PageLineJumpDirX  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Zelle PageLineJumpDirX aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowPageLayout** <br/> |
| Zellenindex:  <br/> |**visPLOJumpDirX** <br/> |
   

