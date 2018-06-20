---
title: Zelle "Y" (Abschnitt "Annotation")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60095
localization_priority: Normal
ms.assetid: 527a4615-2013-a4b4-81cd-7f5d71c1803c
description: Die y-Koordinate des kommentarmarkers in Seitenkoordinaten.
ms.openlocfilehash: cc2399de7919512796a39ca39c705c214f4c51a2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798448"
---
# <a name="y-cell-annotation-section"></a>Y Cell (Annotation Section)

Die *y* -Koordinate des kommentarmarkers in Seitenkoordinaten. 
  
> [!NOTE]
> Diese Zelle wird für Kommentare zur Überwachung nur, wenn eine VSD-Datei in Microsoft Visio 2013 öffnen oder eine vsdx-Datei im VSD-Format speichern. Es wird nicht zum Nachverfolgen von Kommentaren in .vsdx Dokumente in Visio 2013 verwendet. 
  
## <a name="remarks"></a>Hinweise

Wenn Sie einen Verweis auf die Zelle Y nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Annotation.Y [ *i* ] wobei *i* = < 1 >, 2, 3...  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Y aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionAnnotation** <br/> |
| Zeilenindex:  <br/> |**VisRowAnnotation** +  *i* wobei *i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visAnnotationY** <br/> |
   

