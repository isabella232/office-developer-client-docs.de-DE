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
ms.openlocfilehash: 16f0bac8f139c0b03d7826ac377a964d15296dd8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797976"
---
# <a name="scratch-section"></a>Scratch-Abschnitt

Eine Arbeitsumgebung für die Eingabe und das Testen von Formeln, auf die von anderen Zellen verwiesen werden kann.
  
## <a name="remarks"></a>Bemerkungen

Sie können diesen Abschnitt über das Dialogfeld **Abschnitt einfügen** hinzufügen. Klicken Sie mit der rechten Maustaste in das ShapeSheet-Fenster, und klicken Sie dann auf **Abschnitt einfügen**.
  
Im Abschnitt **"Scratch"** wird in der Regel wiederholte komplexe Berechnungen zu isolieren. Wenn Ihre Lösung einen eindeutig definierten Zweck hat, ist es weiser eine Zelle im Abschnitt **User-Defined Cells** aus Gründen der Übersichtlichkeit verwendet werden, da benannt werden kann. 
  
Zellen im Abschnitt **"Scratch"** verwenden Einheiten auf zwei verschiedene Arten. Die Zellen X und Y verwenden Zeichnungseinheiten; Zellen a bis D verwenden keine Einheiten. (Klicken Sie in der C-Programmierer benutzerdefinierten Desktops werden auch Zellen X und Y sind "typisiert" und Zellen A bis D sind "void".) Die Zellen **Scratch X** und **Y Scratch** werden häufig zum Ableiten von *x-* und *y -* Koordinaten wie **DrehbezX** und **DrehbezY**oder für die Zellen X und Y in einer Zelle der **Geometrie** -Abschnitt gefunden. Entwurfszellen Sie A bis D alle Einheiten anzeigen, können Sie angeben. 
  
Ein weiterer Unterschied besteht die Möglichkeit, die diese Zellen Punktwerte zu speichern. Ein Punkt in Visio ist ein single-Paket für eine Koordinate ( *X, y*). Wenn eine Formel einen Punktwert zurückgibt, wird dieser Wert in drei verschiedene Arten, abhängig von der ShapeSheet-Zelle interpretiert, die in die Formel ist. Zellen, die auf *x* beziehen-Koordinaten (beispielsweise **DrehbezX**oder Zellen in der Spalte X von einem Abschnitt **"Geometry"** ) extrahiert nur die *X* -Teil einer Punktwert koordinieren. Zellen, die sich, die *y beziehen* -Koordinaten extrahieren nur der *y* -Teil einer Punktwert koordinieren. 
  
Visio extrahiert beispielsweise die Formel `PNT(3,4)` auf diese drei Arten. 
  
|**Cell**|**Eingabe**|**Behandlung durch Visio**|**Ergebnis**|
|:-----|:-----|:-----|:-----|
| X  <br/> | `PNT(3,4)` <br/> | `PNTX(PNT(3,4))` <br/> | 3,0000 Zoll  <br/> |
| Y  <br/> | `PNT(3,4)` <br/> | `PNTY(PNT(3,4))` <br/> | 4,0000 Zoll  <br/> |
| A-D  <br/> | `PNT(3,4)` <br/> | `PNT(3,4)` <br/> | PNT (3.0000 Zoll, 4,0000 In.)  <br/> |
   

