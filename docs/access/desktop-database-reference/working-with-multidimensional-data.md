---
title: Verwenden von multidimensionalen Daten
TOCTitle: Working with multidimensional data
ms:assetid: a0c9ac73-04da-cfdd-8787-15c8a53ff819
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249740(v=office.15)
ms:contentKeyID: 48546717
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1fc86aa61b9dda9db2246b7b5720eed31a595ea0
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998693"
---
# <a name="working-with-multidimensional-data"></a>Verwenden von multidimensionalen Daten

**Betrifft**: Access 2013, Office 2013

Einer *Zellmenge* ist das Ergebnis einer Abfrage auf mehrdimensionale Daten. Es besteht aus einer Sammlung von Achsen, in der Regel nicht mehr als vier Achsen und in der Regel nur zwei oder drei. Einer *Achse* ist eine Auflistung von Elementen aus einer oder mehrerer Dimensionen, die zum Suchen oder Filtern bestimmte Werte in einem Cube verwendet wird.

Eine *Position* ist ein Punkt auf einer Achse. Bei einer Achse, die aus einer einzigen Dimension besteht, sind diese Positionen eine Untermenge der Dimensionselemente. Wenn mehr als eine Dimension eine Achse besteht, ist jede Position eine zusammengesetzte Entität, die mit *n* Teilen, wobei *n* die Anzahl der Dimensionen, die an dieser Achse ausgerichtet ist. Jeder Teil der Position ist ein Element aus einer entsprechenden Dimension.

Wenn beispielsweise die Dimensionen für Geografie und Artikel eines Cubes mit Verkaufsdaten an der X-Achse einer Zellmenge ausgerichtet sind, kann eine Position entlang dieser Achse die Elemente USA und Computer enthalten. In diesem Beispiel erfordert das Ermitteln einer Position an der X-Achse, dass Elemente aller Dimensionen an der Achse ausgerichtet sind.

Eine *Zelle* ist ein Objekt am Kreuzungspunkt von Achsenkoordinaten. Jede Zelle enthält mehrere mit ihr verknüpfte Informationen, wozu die Daten, eine formatierte Zeichenfolge (Zellendaten zum Anzeigen) und der Ordnungswert der Zelle gehören. (Jede Zelle stellt innerhalb der Zellmenge einen eindeutigen Ordnungswert dar. Der Ordnungswert der ersten Zelle in der Zellmenge ist Null, und die linke Zelle in der zweiten Zeile einer Zellmenge mit acht Spalten hat den Ordnungswert Acht.)

Ein Cube hat beispielsweise die folgenden sechs Dimensionen. (Dieses Cubeschema weicht leicht vom Beispiel unter [Übersicht über Multidimensionale Schemas und Daten](overview-of-multidimensional-schemas-and-data.md) ab):

- Verkaufsberater
- Geografie (natürliche Hierarchie) - Kontinente, Länder/Regionen, Bundesländer/Kantone usw.
- Quartale - Quartale, Monate, Tage
- Jahre
- Maßeinheiten - Umsatz, Änderung in Prozent, geplanter Umsatz
- Artikel

> [!NOTE]
> [!HINWEIS] Die Zellwerte in diesem Beispiel können als Paare von Ordnungszahlen für die Achsenpositionen angezeigt werden, wobei die erste Ziffer die Position auf der X-Achse und die zweite Ziffer die Position auf der Y-Achse darstellt.

Diese Zellmenge weist die folgenden Merkmale auf:

- Achsendimensionen: Quartale, Verkaufsberater, Geografie

- Filterdimensionen: Maßeinheiten, Jahre, Artikel

- Zwei Achsen: SPALTE (X-Achse oder Achse 0) und ZEILE (Y-Achse oder Achse 1)

- X-Achse: zwei geschachtelte Dimensionen, Verkaufsberater und Geografie

- Y-Achse: Dimension Quartale

Die x-Achse enthält zwei geschachtelte Dimensionen: Verkaufsberater und Geografie. Aus Geografie, werden vier Elemente ausgewählt: Seattle, Boston, USA-South und Japan. Zwei Elemente von Verkäufer ausgewählt sind: Valentine und Nash. Daraus ergeben sich insgesamt acht Positionen auf dieser Achse (8 = 4\*2).

Jede Koordinate wird als eine Position mit zwei Elementen dargestellt – eins aus der Dimension Verkaufsberater und eins aus der Dimension Geografie:

```vb 
 
(Valentine, Seattle), (Valentine, Boston), (Valentine, USA_North), 
(Valentine, Japan), (Nash, Seattle), (Nash, Boston), (Nash, USA_North), 
(Nash, Japan) 
```

Die Y-Achse enthält nur eine Dimension mit den folgenden acht Positionen:

```vb 
 
Jan, Feb, Mar, Qtr2, Qtr3, Oct, Nov, Dec 
```

Zellmengen, Zellen, Achsen und Positionen werden in ADO MD durch die entsprechenden Objekte dargestellt: [Cellset](cellset-object-ado-md.md), [Cell](cell-object-ado-md.md), [Axis](axis-object-ado-md.md) und [Position](position-object-ado-md.md).

