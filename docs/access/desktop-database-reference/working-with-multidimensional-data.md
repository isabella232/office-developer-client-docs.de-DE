---
title: Arbeiten mit mehrdimensionalen Daten
TOCTitle: Working with multidimensional data
ms:assetid: a0c9ac73-04da-cfdd-8787-15c8a53ff819
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249740(v=office.15)
ms:contentKeyID: 48546717
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 67b22219fdbbec8bf518b7be0fabd9a6adfbcf7f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306041"
---
# <a name="working-with-multidimensional-data"></a><span data-ttu-id="8de1c-102">Arbeiten mit mehrdimensionalen Daten</span><span class="sxs-lookup"><span data-stu-id="8de1c-102">Working with multidimensional data</span></span>

<span data-ttu-id="8de1c-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8de1c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8de1c-p101">Eine *Zellmenge* ist das Ergebnis einer Abfrage für multidimensionale Daten. Sie besteht aus einer Sammlung von Achsen, und zwar in der Regel aus zwei oder drei, höchstens vier Achsen. Eine *Achse* ist eine Sammlung von Elementen aus mindestens einer Dimension. Eine Achse wird zum Suchen oder Filtern bestimmter Werte in einem Cube verwendet.</span><span class="sxs-lookup"><span data-stu-id="8de1c-p101">A *cellset* is the result of a query on multidimensional data. It consists of a collection of axes, usually no more than four axes and typically only two or three. An *axis* is a collection of members from one or more dimensions, which is used to locate or filter specific values in a cube.</span></span>

<span data-ttu-id="8de1c-p102">Eine *Position* ist ein Punkt auf einer Achse. Bei einer Achse, die aus einer einzigen Dimension besteht, sind diese Positionen eine Untermenge der Dimensionselemente. Wenn eine Achse aus mehreren Dimensionen besteht, ist jede Position eine zusammengesetzte Entität mit *n* Teilen, wobei *n* die Anzahl der Dimensionen darstellt, die an dieser Achse ausgerichtet sind. Jeder Teil der Position ist ein Element aus einer entsprechenden Dimension.</span><span class="sxs-lookup"><span data-stu-id="8de1c-p102">A *position* is a point along an axis. For an axis consisting of a single dimension, these positions are a subset of the dimension members. If an axis consists of more than one dimension, then each position is a compound entity, which has *n* parts where *n* is the number of dimensions oriented along that axis. Each part of the position is a member from one constituent dimension.</span></span>

<span data-ttu-id="8de1c-p103">Wenn beispielsweise die Dimensionen für Geografie und Artikel eines Cubes mit Verkaufsdaten an der X-Achse einer Zellmenge ausgerichtet sind, kann eine Position entlang dieser Achse die Elemente USA und Computer enthalten. In diesem Beispiel erfordert das Ermitteln einer Position an der X-Achse, dass Elemente aller Dimensionen an der Achse ausgerichtet sind.</span><span class="sxs-lookup"><span data-stu-id="8de1c-p103">For example, if the Geography and Product dimensions from a cube containing sales data are oriented along the x-axis of a cellset, a position along this axis may contain the members "USA" and "Computers." In this example, determining a position along the x-axis requires that members from each dimension are oriented along the axis.</span></span>

<span data-ttu-id="8de1c-p104">Eine *Zelle* ist ein Objekt am Kreuzungspunkt von Achsenkoordinaten. Jede Zelle enthält mehrere mit ihr verknüpfte Informationen, wozu die Daten, eine formatierte Zeichenfolge (Zellendaten zum Anzeigen) und der Ordnungswert der Zelle gehören. (Jede Zelle stellt innerhalb der Zellmenge einen eindeutigen Ordnungswert dar. Der Ordnungswert der ersten Zelle in der Zellmenge ist Null, und die linke Zelle in der zweiten Zeile einer Zellmenge mit acht Spalten hat den Ordnungswert Acht.)</span><span class="sxs-lookup"><span data-stu-id="8de1c-p104">A *cell* is an object positioned at the intersection of axis coordinates. Each cell has multiple pieces of information associated with it, including the data itself, a formatted string (the displayable form of cell data), and the cell ordinal value. (Each cell is a unique ordinal value in the cellset. The ordinal value of the first cell in the cellset is zero, while the leftmost cell in the second row of a cellset with eight columns would have an ordinal value of eight.)</span></span>

<span data-ttu-id="8de1c-117">Ein Cube hat beispielsweise die folgenden sechs Dimensionen. (Dieses Cubeschema weicht leicht vom Beispiel unter [Übersicht über Multidimensionale Schemas und Daten](overview-of-multidimensional-schemas-and-data.md) ab):</span><span class="sxs-lookup"><span data-stu-id="8de1c-117">For example, a cube has the following six dimensions (note that this cube schema differs slightly from the example given in [Overview of Multidimensional Schemas and Data](overview-of-multidimensional-schemas-and-data.md)):</span></span>

- <span data-ttu-id="8de1c-118">Verkaufsberater</span><span class="sxs-lookup"><span data-stu-id="8de1c-118">Salesperson</span></span>
- <span data-ttu-id="8de1c-119">Geografie (natürliche Hierarchie) – Kontinente, Länder/Regionen, Bundesländer/Kantone usw.</span><span class="sxs-lookup"><span data-stu-id="8de1c-119">Geography (natural hierarchy) — Continents, Countries, States, and so on</span></span>
- <span data-ttu-id="8de1c-120">Quartale – Quartale, Monate, Tage</span><span class="sxs-lookup"><span data-stu-id="8de1c-120">Quarters — Quarters, Months, Days</span></span>
- <span data-ttu-id="8de1c-121">Jahre</span><span class="sxs-lookup"><span data-stu-id="8de1c-121">Years</span></span>
- <span data-ttu-id="8de1c-122">Maßeinheiten – Umsatz, Änderung in Prozent, geplanter Umsatz</span><span class="sxs-lookup"><span data-stu-id="8de1c-122">Measures — Sales, PercentChange, BudgetedSales</span></span>
- <span data-ttu-id="8de1c-123">Artikel</span><span class="sxs-lookup"><span data-stu-id="8de1c-123">Products</span></span>

> [!NOTE]
> <span data-ttu-id="8de1c-124">Die Zellwerte in diesem Beispiel können als Paare von Ordnungszahlen für die Achsenpositionen angezeigt werden, wobei die erste Ziffer die Position auf der X-Achse und die zweite Ziffer die Position auf der Y-Achse darstellt.</span><span class="sxs-lookup"><span data-stu-id="8de1c-124">The cell values in the example can be viewed as ordered pairs of axis position ordinals where the first digit represents the x-axis position and the second digit the y-axis position.</span></span>

<span data-ttu-id="8de1c-125">Diese Zellmenge weist die folgenden Merkmale auf:</span><span class="sxs-lookup"><span data-stu-id="8de1c-125">The characteristics of this cellset are as follows:</span></span>

- <span data-ttu-id="8de1c-126">Achsendimensionen: Quartale, Verkaufsberater, Geografie</span><span class="sxs-lookup"><span data-stu-id="8de1c-126">Axis dimensions: Quarters, Salesperson, Geography</span></span>

- <span data-ttu-id="8de1c-127">Filterdimensionen: Maßeinheiten, Jahre, Artikel</span><span class="sxs-lookup"><span data-stu-id="8de1c-127">Filter dimensions: Measures, Years, Products</span></span>

- <span data-ttu-id="8de1c-128">Zwei Achsen: SPALTE (X-Achse oder Achse 0) und ZEILE (Y-Achse oder Achse 1)</span><span class="sxs-lookup"><span data-stu-id="8de1c-128">Two axes: COLUMN (x, or Axis 0) and ROW (y, or Axis 1)</span></span>

- <span data-ttu-id="8de1c-129">X-Achse: zwei geschachtelte Dimensionen, Verkaufsberater und Geografie</span><span class="sxs-lookup"><span data-stu-id="8de1c-129">x-axis: two nested dimensions, Salesperson and Geography</span></span>

- <span data-ttu-id="8de1c-130">y-axis: Quarters dimension</span><span class="sxs-lookup"><span data-stu-id="8de1c-130">y-axis: Quarters dimension</span></span>

<span data-ttu-id="8de1c-p105">The x-axis has two nested dimensions: Salesperson and Geography. From Geography, four members are selected: Seattle, Boston, USA-South, and Japan. Two members are selected from Salesperson: Valentine and Nash. This yields a total of eight positions on this axis (8 = 4\*2).</span><span class="sxs-lookup"><span data-stu-id="8de1c-p105">The x-axis has two nested dimensions: Salesperson and Geography. From Geography, four members are selected: Seattle, Boston, USA-South, and Japan. Two members are selected from Salesperson: Valentine and Nash. This yields a total of eight positions on this axis (8 = 4\*2).</span></span>

<span data-ttu-id="8de1c-135">Each coordinate is represented as a position with two members — one from the Salesperson dimension and another from the Geography dimension:</span><span class="sxs-lookup"><span data-stu-id="8de1c-135">Each coordinate is represented as a position with two members — one from the Salesperson dimension and another from the Geography dimension:</span></span>

```vb 
 
(Valentine, Seattle), (Valentine, Boston), (Valentine, USA_North), 
(Valentine, Japan), (Nash, Seattle), (Nash, Boston), (Nash, USA_North), 
(Nash, Japan) 
```

<span data-ttu-id="8de1c-136">Die Y-Achse enthält nur eine Dimension mit den folgenden acht Positionen:</span><span class="sxs-lookup"><span data-stu-id="8de1c-136">The y-axis has only one dimension, containing the following eight positions:</span></span>

```vb 
 
Jan, Feb, Mar, Qtr2, Qtr3, Oct, Nov, Dec 
```

<span data-ttu-id="8de1c-137">Zellmengen, Zellen, Achsen und Positionen werden in ADO MD durch die entsprechenden Objekte dargestellt: [Cellset](cellset-object-ado-md.md), [Cell](cell-object-ado-md.md), [Axis](axis-object-ado-md.md) und [Position](position-object-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="8de1c-137">Cellsets, cells, axes, and positions are all represented in ADO MD by corresponding objects: [Cellset](cellset-object-ado-md.md), [Cell](cell-object-ado-md.md), [Axis](axis-object-ado-md.md), and [Position](position-object-ado-md.md).</span></span>

