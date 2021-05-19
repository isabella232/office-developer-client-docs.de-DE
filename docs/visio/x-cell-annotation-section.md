---
title: Zelle "X" (Abschnitt "Annotation")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1028735
localization_priority: Normal
ms.assetid: f9db8623-9fcf-7037-2d11-d509f463025d
description: Die x-Koordinate der Kommentarmarkierung in Seitenkoordinaten.
ms.openlocfilehash: fdd9e2850a3285a2fcf4cc05fa056accd71052a9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434480"
---
# <a name="x-cell-annotation-section"></a>Zelle "X" (Abschnitt "Annotation")

Die  x-Koordinate der Kommentarmarkierung in Seitenkoordinaten. 
  
> [!NOTE]
> Diese Zelle wird nur zum Nachverfolgen von Kommentaren verwendet, wenn Sie eine VSD-Datei in Microsoft Visio 2013 öffnen oder eine VSDX-Datei im VSD-Dateiformat speichern. Es wird nicht zum Nachverfolgen von Kommentaren in VSDX-Dokumenten in Visio 2013 verwendet. 
  
## <a name="remarks"></a>Hinweise

Um einen Verweis auf die Zelle X anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Annotation.X[  *i*  ] wobei  *i*  = <1>, 2, 3...  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die X-Zelle nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionAnnotation** <br/> |
| Zeilenindex:  <br/> |**visRowAnnotation**  +   *i,* *wobei i* = 0, 1, 2...  <br/> |
| Zeilenindex:  <br/> |**visAnnotationX** <br/> |
   

