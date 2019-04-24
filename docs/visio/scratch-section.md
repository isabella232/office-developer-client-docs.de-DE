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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344527"
---
# <a name="scratch-section"></a>Abschnitt "Scratch"

Eine Arbeitsumgebung für die Eingabe und das Testen von Formeln, auf die von anderen Zellen verwiesen werden kann.
  
## <a name="remarks"></a>Bemerkungen

Sie können diesen Abschnitt über das Dialogfeld **Abschnitt einfügen** hinzufügen. Klicken Sie mit der rechten Maustaste in das ShapeSheet-Fenster, und klicken Sie dann auf **Abschnitt einfügen**.
  
Der Abschnitt **Scratch** wird in der Regel verwendet, um wiederholte komplexe Berechnungen zu isolieren. Wenn Ihre Lösung einen genau definierten Zweck hat, ist es klüger, eine Zelle im Abschnitt **benutzerdefinierte Zellen** zur besseren Übersichtlichkeit zu verwenden, da Benutzer Zellen benannt werden können. 
  
Zellen im **Scratch** -Abschnitt verwenden Einheiten auf zwei verschiedene Arten. X-und Y-Zellen verwenden Zeichnungseinheiten; A bis D-Zellen verwenden keine Einheiten. (Im Jargon von C-Programmierern werden die Zellen X und Y "typisiert", und die Zellen A bis D sind "void"). Die **** x-und **Scratch y** -Zellen werden häufig zum Ableiten von *x-* und *y-* Koordinaten, wie **PinX** und **PinY**, oder den x-und y-Zellen in einer **Geometry** -Abschnitts Zelle verwendet. Kratzer Zellen A bis D können anzeigen, welche Einheiten Sie angeben. 
  
Ein weiterer Unterschied ist die Art und Weise, in der diese Zellen Punktwerte speichern. Ein Punkt in Visio ist ein einzelnes Datenpaket für eine ( *x, y*)-Koordinate. Wenn eine Formel einen Point-Wert zurückgibt, wird dieser Wert auf eine von drei Arten interpretiert, abhängig von der ShapeSheet-Zelle, in der sich die Formel befindet. Zellen, die sich auf *x* -Koordinaten beziehen (beispielsweise **PinX**oder Zellen in der Spalte x eines **Geometry** -Abschnitts) extrahieren nur den *x* -Koordinate-Teil eines Punktwerts. Zellen, die sich auf *y* -Koordinaten beziehen, extrahieren nur den *y* -Koordinaten Teil eines Punktwerts. 
  
Visio extrahiert die Formel `PNT(3,4)` beispielsweise auf drei Arten. 
  
|**Cell**|**Eingabe**|**Behandlung durch Visio**|**Ergebnis**|
|:-----|:-----|:-----|:-----|
| X  <br/> | `PNT(3,4)` <br/> | `PNTX(PNT(3,4))` <br/> | 3,0000 Zoll  <br/> |
| v  <br/> | `PNT(3,4)` <br/> | `PNTY(PNT(3,4))` <br/> | 4,0000 Zoll  <br/> |
| A-D  <br/> | `PNT(3,4)` <br/> | `PNT(3,4)` <br/> | PNT (3.0000 in., 4,0000 in.)  <br/> |
   

