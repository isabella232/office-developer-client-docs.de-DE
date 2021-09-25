---
title: Arbeiten mit mehrdimensionalen Daten
TOCTitle: Working with multidimensional data
ms:assetid: a0c9ac73-04da-cfdd-8787-15c8a53ff819
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249740(v=office.15)
ms:contentKeyID: 48546717
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 3d38a32f12c7d5362888c14458dd6a3a7ec03238
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59626043"
---
# <a name="working-with-multidimensional-data"></a>Arbeiten mit mehrdimensionalen Daten

**Gilt für**: Access 2013, Office 2013

Eine *Zellmenge* ist das Ergebnis einer Abfrage für multidimensionale Daten. Sie besteht aus einer Sammlung von Achsen, und zwar in der Regel aus zwei oder drei, höchstens vier Achsen. Eine *Achse* ist eine Sammlung von Elementen aus mindestens einer Dimension. Eine Achse wird zum Suchen oder Filtern bestimmter Werte in einem Cube verwendet.

Eine *Position* ist ein Punkt auf einer Achse. Bei einer Achse, die aus einer einzigen Dimension besteht, sind diese Positionen eine Untermenge der Dimensionselemente. Wenn eine Achse aus mehreren Dimensionen besteht, ist jede Position eine zusammengesetzte Entität mit *n* Teilen, wobei *n* die Anzahl der Dimensionen darstellt, die an dieser Achse ausgerichtet sind. Jeder Teil der Position ist ein Element aus einer entsprechenden Dimension.

Wenn beispielsweise die Dimensionen für Geografie und Artikel eines Cubes mit Verkaufsdaten an der X-Achse einer Zellmenge ausgerichtet sind, kann eine Position entlang dieser Achse die Elemente USA und Computer enthalten. In diesem Beispiel erfordert das Ermitteln einer Position an der X-Achse, dass Elemente aller Dimensionen an der Achse ausgerichtet sind.

Eine *Zelle* ist ein Objekt am Kreuzungspunkt von Achsenkoordinaten. Jede Zelle enthält mehrere mit ihr verknüpfte Informationen, wozu die Daten, eine formatierte Zeichenfolge (Zellendaten zum Anzeigen) und der Ordnungswert der Zelle gehören. (Jede Zelle stellt innerhalb der Zellmenge einen eindeutigen Ordnungswert dar. Der Ordnungswert der ersten Zelle in der Zellmenge ist Null, und die linke Zelle in der zweiten Zeile einer Zellmenge mit acht Spalten hat den Ordnungswert Acht.)

Ein Cube hat beispielsweise die folgenden sechs Dimensionen. (Dieses Cubeschema weicht leicht vom Beispiel unter [Übersicht über Multidimensionale Schemas und Daten](overview-of-multidimensional-schemas-and-data.md) ab):

- Verkaufsberater
- Geografie (natürliche Hierarchie) – Kontinente, Länder/Regionen, Bundesländer/Kantone usw.
- Quartale – Quartale, Monate, Tage
- Jahre
- Maßeinheiten – Umsatz, Änderung in Prozent, geplanter Umsatz
- Artikel

> [!NOTE]
> Die Zellwerte in diesem Beispiel können als Paare von Ordnungszahlen für die Achsenpositionen angezeigt werden, wobei die erste Ziffer die Position auf der X-Achse und die zweite Ziffer die Position auf der Y-Achse darstellt.

Diese Zellmenge weist die folgenden Merkmale auf:

- Achsendimensionen: Quartale, Verkaufsberater, Geografie

- Filterdimensionen: Maßeinheiten, Jahre, Artikel

- Zwei Achsen: SPALTE (X-Achse oder Achse 0) und ZEILE (Y-Achse oder Achse 1)

- X-Achse: zwei geschachtelte Dimensionen, Verkaufsberater und Geografie

- y-axis: Quarters dimension

The x-axis has two nested dimensions: Salesperson and Geography. From Geography, four members are selected: Seattle, Boston, USA-South, and Japan. Two members are selected from Salesperson: Valentine and Nash. This yields a total of eight positions on this axis (8 = 4\*2).

Each coordinate is represented as a position with two members — one from the Salesperson dimension and another from the Geography dimension:

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

