---
title: Zelle "X" (Abschnitt "Annotation")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1028735
ms.localizationpriority: medium
ms.assetid: f9db8623-9fcf-7037-2d11-d509f463025d
description: Die X-Koordinate der Kommentarmarkierung in Seitenkoordinaten.
ms.openlocfilehash: 931ea0ea6a1397dc02d91a93a76cc702e748fbe9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59622606"
---
# <a name="x-cell-annotation-section"></a>Zelle "X" (Abschnitt "Annotation")

Die  X-Koordinate der Kommentarmarkierung in Seitenkoordinaten. 
  
> [!NOTE]
> Diese Zelle wird nur zum Nachverfolgen von Kommentaren beim Öffnen einer VSD-Datei in Microsoft Visio 2013 oder beim Speichern einer VSDX-Datei im VSD-Dateiformat verwendet. Es wird nicht zum Nachverfolgen von Kommentaren in VSDX-Dokumenten in Visio 2013 verwendet. 
  
## <a name="remarks"></a>Bemerkungen

Um einen Verweis auf die Zelle X anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Annotation.X[  *i*  ] where  *i*  = <1>, 2, 3...  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle X anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionAnnotation** <br/> |
| Zeilenindex:  <br/> |**visRowAnnotation**  +   *i* where *i* = 0, 1, 2...  <br/> |
| Zeilenindex:  <br/> |**visAnnotationX** <br/> |
   

