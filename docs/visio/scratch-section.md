---
title: Abschnitt "Scratch"
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm2125
ms.localizationpriority: medium
ms.assetid: 144dd06f-7225-57db-fd19-a58d6bccf0e1
description: Eine Arbeitsumgebung für die Eingabe und das Testen von Formeln, auf die von anderen Zellen verwiesen werden kann.
ms.openlocfilehash: 331831b28fd5b06d685639822e7c46268f40abad
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59598164"
---
# <a name="scratch-section"></a>Abschnitt "Scratch"

Eine Arbeitsumgebung für die Eingabe und das Testen von Formeln, auf die von anderen Zellen verwiesen werden kann.
  
## <a name="remarks"></a>HinwBemerkungeneise

Sie können diesen Abschnitt über das Dialogfeld **Abschnitt einfügen** hinzufügen. Klicken Sie mit der rechten Maustaste in das ShapeSheet-Fenster, und klicken Sie dann auf **Abschnitt einfügen**.
  
Der Abschnitt **Scratch** wird in der Regel verwendet, um wiederholte komplexe Berechnungen zu isolieren. Wenn Ihre Lösung einen klar definierten Zweck hat, empfiehlt es sich, eine Zelle im Abschnitt **"Benutzerdefinierte Zellen"** zur Besseren Übersichtlichkeit zu verwenden, da Benutzerzellen benannt werden können. 
  
Zellen im Abschnitt **Scratch** verwenden Einheiten auf zwei verschiedene Arten. X- und Y-Zellen verwenden Zeichnungseinheiten; A- bis D-Zellen verwenden keine Einheiten. (Im Jargon der C-Programmierer werden die Zellen X und Y "eingegeben", und die Zellen A bis D sind "void".) Die Zellen **Scratch** X und Scratch Y werden häufig zum Ableiten von *X-* und *Y-Koordinaten* verwendet, z. B. **PinX** und **PinY** oder die X- und Y-Zellen in einer **Geometrie-Abschnittszelle.**  Die Zellen Scratch bis A bis D können alle angegebenen 
  
Ein weiterer Unterschied besteht darin, wie diese Zellen Punktwerte speichern. Ein Punkt in Visio ist ein einzelnes Datenpaket für eine ( *x,y*) Koordinate. Wenn eine Formel einen Punktwert zurückgibt, wird dieser Wert auf eine von drei Arten interpretiert, abhängig von der ShapeSheet-Zelle, in der sich die Formel befindet. Zellen, die sich auf *x-Koordinaten* (z. B. **PinX** oder Zellen in der X-Spalte eines **Geometry-Abschnitts)** beziehen, extrahieren nur den X-Koordinate-Teil eines Punktwerts.  Zellen, die sich auf  *y-Koordinaten*  beziehen, extrahieren nur den  *y-Koordinatenteil*  eines Punktwerts. 
  
Beispielsweise extrahiert Visio die Formel `PNT(3,4)` auf diese drei Arten. 
  
|**Cell**|**Eingabe**|**Behandlung durch Visio**|**Ergebnis**|
|:-----|:-----|:-----|:-----|
| X  <br/> | `PNT(3,4)` <br/> | `PNTX(PNT(3,4))` <br/> | 3,0000 Zoll  <br/> |
| J  <br/> | `PNT(3,4)` <br/> | `PNTY(PNT(3,4))` <br/> | 4,0000 Zoll  <br/> |
| A-D  <br/> | `PNT(3,4)` <br/> | `PNT(3,4)` <br/> | PNT(3.0000 Zoll, 4.0000 Zoll)  <br/> |
   

