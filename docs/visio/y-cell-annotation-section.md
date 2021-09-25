---
title: Zelle "Y" (Abschnitt "Annotation")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60095
ms.localizationpriority: medium
ms.assetid: 527a4615-2013-a4b4-81cd-7f5d71c1803c
description: Die y-Koordinate der Kommentarmarkierung in Seitenkoordinaten.
ms.openlocfilehash: 669e395c751770dfe160abff6ee23e227989ce32
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59603102"
---
# <a name="y-cell-annotation-section"></a>Zelle "Y" (Abschnitt "Annotation")

Die  y-Koordinate der Kommentarmarkierung in Seitenkoordinaten. 
  
> [!NOTE]
> Diese Zelle wird nur zum Nachverfolgen von Kommentaren beim Öffnen einer VSD-Datei in Microsoft Visio 2013 oder beim Speichern einer VSDX-Datei im VSD-Dateiformat verwendet. Es wird nicht zum Nachverfolgen von Kommentaren in VSDX-Dokumenten in Visio 2013 verwendet. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Um einen Verweis auf die Zelle Y anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Annotation.Y [  *i*  ] where  *i*  = <1>, 2, 3...  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle Y anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionAnnotation** <br/> |
| Zeilenindex:  <br/> |**visRowAnnotation**  +   *i* where *i* = 0, 1, 2...  <br/> |
| Zeilenindex:  <br/> |**visAnnotationY** <br/> |
   

