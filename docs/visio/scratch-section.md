---
title: Abschnitt "Scratch"
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm2125
localization_priority: Normal
ms.assetid: 144dd06f-7225-57db-fd19-a58d6bccf0e1
description: Eine Arbeitsumgebung für die Eingabe und das Testen von Formeln, auf die von anderen Zellen verwiesen werden kann.
ms.openlocfilehash: a7d2c6762e96fc19986521c2ba164666b925c928
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411603"
---
# <a name="scratch-section"></a>Abschnitt "Scratch"

Eine Arbeitsumgebung für die Eingabe und das Testen von Formeln, auf die von anderen Zellen verwiesen werden kann.
  
## <a name="remarks"></a>Hinweise

Sie können diesen Abschnitt über das Dialogfeld **Abschnitt einfügen** hinzufügen. Klicken Sie mit der rechten Maustaste in das ShapeSheet-Fenster, und klicken Sie dann auf **Abschnitt einfügen**.
  
Der **Abschnitt Scratch** wird in der Regel verwendet, um wiederholte komplexe Berechnungen zu isolieren. Wenn Ihre Lösung einen genau definierten Zweck hat, ist es  ratsamer, eine Zelle im Abschnitt Benutzerdefinierte Zellen zu verwenden, um Klarheit zu schaffen, da Benutzerzellen benannt werden können. 
  
Zellen im **Abschnitt Scratch** verwenden Einheiten auf zwei unterschiedliche Weise. X- und Y-Zellen verwenden Zeicheneinheiten. A- bis D-Zellen verwenden keine Einheiten. (Im Jargon der C-Programmierer sind X- und Y-Zellen "typiert", und die Zellen A bis D sind "void".) Die Zellen **Scratch X** und **Scratch Y** werden häufig zum Ableitung von X- und *Y-Koordinaten* wie **PinX** und **PinY** oder der *X-* und Y-Zellen in einer Geometry-Abschnittszelle verwendet.  Die Scratchzellen A bis D können alle von Ihnen angegebenen Einheiten anzeigen. 
  
Ein weiterer Unterschied besteht in der Art und Weise, wie diese Zellen Punktwerte speichern. Ein Punkt in Visio ist ein einzelnes Datenpaket für eine ( *x,y*)-Koordinate. Wenn eine Formel einen Punktwert zurückgibt, wird dieser Wert in Abhängigkeit von der ShapeSheet-Zelle, in der sich die Formel befindet, auf drei Arten interpretiert. Zellen, die sich *auf x-Koordinaten* (z. B. **PinX** oder Zellen in der X-Spalte eines Geometry-Abschnitts) beziehen, extrahieren nur den *x-Koordinatenteil* eines Punktwerts.  Zellen, die sich auf  *y-Koordinaten*  beziehen, extrahieren nur den  *y-Koordinatenteil*  eines Punktwerts. 
  
Beispiel: Visio die Formel auf `PNT(3,4)` diese drei Arten extrahiert. 
  
|**Cell**|**Eingabe**|**Behandlung durch Visio**|**Ergebnis**|
|:-----|:-----|:-----|:-----|
| X  <br/> | `PNT(3,4)` <br/> | `PNTX(PNT(3,4))` <br/> | 3,0000 Zoll  <br/> |
| v  <br/> | `PNT(3,4)` <br/> | `PNTY(PNT(3,4))` <br/> | 4,0000 Zoll  <br/> |
| A-D  <br/> | `PNT(3,4)` <br/> | `PNT(3,4)` <br/> | PNT(3.0000 in., 4.0000 in.)  <br/> |
   

