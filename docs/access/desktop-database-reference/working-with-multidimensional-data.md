---
title: Verwenden von multidimensionalen Daten
TOCTitle: Working with Multidimensional Data
ms:assetid: a0c9ac73-04da-cfdd-8787-15c8a53ff819
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249740(v=office.15)
ms:contentKeyID: 48546717
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2210799fe46a0993a917a85a0e06a1a806b04548
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25945824"
---
# <a name="working-with-multidimensional-data"></a><span data-ttu-id="b0691-102">Verwenden von multidimensionalen Daten</span><span class="sxs-lookup"><span data-stu-id="b0691-102">Working with multidimensional data</span></span>


<span data-ttu-id="b0691-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b0691-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b0691-104">Einer *Zellmenge* ist das Ergebnis einer Abfrage auf mehrdimensionale Daten.</span><span class="sxs-lookup"><span data-stu-id="b0691-104">A *cellset* is the result of a query on multidimensional data.</span></span> <span data-ttu-id="b0691-105">Es besteht aus einer Sammlung von Achsen, in der Regel nicht mehr als vier Achsen und in der Regel nur zwei oder drei.</span><span class="sxs-lookup"><span data-stu-id="b0691-105">It consists of a collection of axes, usually no more than four axes and typically only two or three.</span></span> <span data-ttu-id="b0691-106">Einer *Achse* ist eine Auflistung von Elementen aus einer oder mehrerer Dimensionen, die zum Suchen oder Filtern bestimmte Werte in einem Cube verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b0691-106">An *axis* is a collection of members from one or more dimensions, which is used to locate or filter specific values in a cube.</span></span>

<span data-ttu-id="b0691-107">Eine *Position* ist ein Punkt auf einer Achse.</span><span class="sxs-lookup"><span data-stu-id="b0691-107">A *position* is a point along an axis.</span></span> <span data-ttu-id="b0691-108">Bei einer Achse, die aus einer einzigen Dimension besteht, sind diese Positionen eine Untermenge der Dimensionselemente.</span><span class="sxs-lookup"><span data-stu-id="b0691-108">For an axis consisting of a single dimension, these positions are a subset of the dimension members.</span></span> <span data-ttu-id="b0691-109">Wenn mehr als eine Dimension eine Achse besteht, ist jede Position eine zusammengesetzte Entität, die mit *n* Teilen, wobei *n* die Anzahl der Dimensionen, die an dieser Achse ausgerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="b0691-109">If an axis consists of more than one dimension, then each position is a compound entity, which has *n* parts where *n* is the number of dimensions oriented along that axis.</span></span> <span data-ttu-id="b0691-110">Jeder Teil der Position ist ein Element aus einer entsprechenden Dimension.</span><span class="sxs-lookup"><span data-stu-id="b0691-110">Each part of the position is a member from one constituent dimension.</span></span>

<span data-ttu-id="b0691-p103">Wenn beispielsweise die Dimensionen für Geografie und Artikel eines Cubes mit Verkaufsdaten an der X-Achse einer Zellmenge ausgerichtet sind, kann eine Position entlang dieser Achse die Elemente USA und Computer enthalten. In diesem Beispiel erfordert das Ermitteln einer Position an der X-Achse, dass Elemente aller Dimensionen an der Achse ausgerichtet sind.</span><span class="sxs-lookup"><span data-stu-id="b0691-p103">For example, if the Geography and Product dimensions from a cube containing sales data are oriented along the x-axis of a cellset, a position along this axis may contain the members "USA" and "Computers." In this example, determining a position along the x-axis requires that members from each dimension are oriented along the axis.</span></span>

<span data-ttu-id="b0691-113">Eine *Zelle* ist ein Objekt am Kreuzungspunkt von Achsenkoordinaten.</span><span class="sxs-lookup"><span data-stu-id="b0691-113">A *cell* is an object positioned at the intersection of axis coordinates.</span></span> <span data-ttu-id="b0691-114">Jede Zelle enthält mehrere mit ihr verknüpfte Informationen, wozu die Daten, eine formatierte Zeichenfolge (Zellendaten zum Anzeigen) und der Ordnungswert der Zelle gehören.</span><span class="sxs-lookup"><span data-stu-id="b0691-114">Each cell has multiple pieces of information associated with it, including the data itself, a formatted string (the displayable form of cell data), and the cell ordinal value.</span></span> <span data-ttu-id="b0691-115">(Jede Zelle stellt innerhalb der Zellmenge einen eindeutigen Ordnungswert dar.</span><span class="sxs-lookup"><span data-stu-id="b0691-115">(Each cell is a unique ordinal value in the cellset.</span></span> <span data-ttu-id="b0691-116">Der Ordnungswert der ersten Zelle in der Zellmenge ist Null, und die linke Zelle in der zweiten Zeile einer Zellmenge mit acht Spalten hat den Ordnungswert Acht.)</span><span class="sxs-lookup"><span data-stu-id="b0691-116">The ordinal value of the first cell in the cellset is zero, while the leftmost cell in the second row of a cellset with eight columns would have an ordinal value of eight.)</span></span>

<span data-ttu-id="b0691-117">Ein Cube hat beispielsweise die folgenden sechs Dimensionen. (Dieses Cubeschema weicht leicht vom Beispiel unter [Übersicht über Multidimensionale Schemas und Daten](overview-of-multidimensional-schemas-and-data.md) ab):</span><span class="sxs-lookup"><span data-stu-id="b0691-117">For example, a cube has the following six dimensions (note that this cube schema differs slightly from the example given in [Overview of Multidimensional Schemas and Data](overview-of-multidimensional-schemas-and-data.md)):</span></span>

  - <span data-ttu-id="b0691-118">Verkaufsberater</span><span class="sxs-lookup"><span data-stu-id="b0691-118">Salesperson</span></span>

  - <span data-ttu-id="b0691-119">Geografie (natürliche Hierarchie) - Kontinente, Länder/Regionen, Bundesländer/Kantone usw.</span><span class="sxs-lookup"><span data-stu-id="b0691-119">Geography (natural hierarchy) — Continents, Countries, States, and so on</span></span>

  - <span data-ttu-id="b0691-120">Quartale - Quartale, Monate, Tage</span><span class="sxs-lookup"><span data-stu-id="b0691-120">Quarters — Quarters, Months, Days</span></span>

  - <span data-ttu-id="b0691-121">Jahre</span><span class="sxs-lookup"><span data-stu-id="b0691-121">Years</span></span>

  - <span data-ttu-id="b0691-122">Maßeinheiten - Umsatz, Änderung in Prozent, geplanter Umsatz</span><span class="sxs-lookup"><span data-stu-id="b0691-122">Measures — Sales, PercentChange, BudgetedSales</span></span>

  - <span data-ttu-id="b0691-123">Artikel</span><span class="sxs-lookup"><span data-stu-id="b0691-123">Products</span></span>


> [!NOTE]
> <P><span data-ttu-id="b0691-124">[!HINWEIS] Die Zellwerte in diesem Beispiel können als Paare von Ordnungszahlen für die Achsenpositionen angezeigt werden, wobei die erste Ziffer die Position auf der X-Achse und die zweite Ziffer die Position auf der Y-Achse darstellt.</span><span class="sxs-lookup"><span data-stu-id="b0691-124">The cell values in the example can be viewed as ordered pairs of axis position ordinals where the first digit represents the x-axis position and the second digit the y-axis position.</span></span></P>



<span data-ttu-id="b0691-125">Diese Zellmenge weist die folgenden Merkmale auf:</span><span class="sxs-lookup"><span data-stu-id="b0691-125">The characteristics of this cellset are as follows:</span></span>

  - <span data-ttu-id="b0691-126">Achsendimensionen: Quartale, Verkaufsberater, Geografie</span><span class="sxs-lookup"><span data-stu-id="b0691-126">Axis dimensions: Quarters, Salesperson, Geography</span></span>

  - <span data-ttu-id="b0691-127">Filterdimensionen: Maßeinheiten, Jahre, Artikel</span><span class="sxs-lookup"><span data-stu-id="b0691-127">Filter dimensions: Measures, Years, Products</span></span>

  - <span data-ttu-id="b0691-128">Zwei Achsen: SPALTE (X-Achse oder Achse 0) und ZEILE (Y-Achse oder Achse 1)</span><span class="sxs-lookup"><span data-stu-id="b0691-128">Two axes: COLUMN (x, or Axis 0) and ROW (y, or Axis 1)</span></span>

  - <span data-ttu-id="b0691-129">X-Achse: zwei geschachtelte Dimensionen, Verkaufsberater und Geografie</span><span class="sxs-lookup"><span data-stu-id="b0691-129">x-axis: two nested dimensions, Salesperson and Geography</span></span>

  - <span data-ttu-id="b0691-130">Y-Achse: Dimension Quartale</span><span class="sxs-lookup"><span data-stu-id="b0691-130">y-axis: Quarters dimension</span></span>

<span data-ttu-id="b0691-131">Die x-Achse enthält zwei geschachtelte Dimensionen: Verkaufsberater und Geografie.</span><span class="sxs-lookup"><span data-stu-id="b0691-131">The x-axis has two nested dimensions: Salesperson and Geography.</span></span> <span data-ttu-id="b0691-132">Aus Geografie, werden vier Elemente ausgewählt: Seattle, Boston, USA-South und Japan.</span><span class="sxs-lookup"><span data-stu-id="b0691-132">From Geography, four members are selected: Seattle, Boston, USA-South, and Japan.</span></span> <span data-ttu-id="b0691-133">Zwei Elemente von Verkäufer ausgewählt sind: Valentine und Nash.</span><span class="sxs-lookup"><span data-stu-id="b0691-133">Two members are selected from Salesperson: Valentine and Nash.</span></span> <span data-ttu-id="b0691-134">Daraus ergeben sich insgesamt acht Positionen auf dieser Achse (8 = 4\*2).</span><span class="sxs-lookup"><span data-stu-id="b0691-134">This yields a total of eight positions on this axis (8 = 4\*2).</span></span>

<span data-ttu-id="b0691-135">Jede Koordinate wird als eine Position mit zwei Elementen dargestellt – eins aus der Dimension Verkaufsberater und eins aus der Dimension Geografie:</span><span class="sxs-lookup"><span data-stu-id="b0691-135">Each coordinate is represented as a position with two members — one from the Salesperson dimension and another from the Geography dimension:</span></span>

```vb 
 
(Valentine, Seattle), (Valentine, Boston), (Valentine, USA_North), 
(Valentine, Japan), (Nash, Seattle), (Nash, Boston), (Nash, USA_North), 
(Nash, Japan) 
```

<span data-ttu-id="b0691-136">Die Y-Achse enthält nur eine Dimension mit den folgenden acht Positionen:</span><span class="sxs-lookup"><span data-stu-id="b0691-136">The y-axis has only one dimension, containing the following eight positions:</span></span>

```vb 
 
Jan, Feb, Mar, Qtr2, Qtr3, Oct, Nov, Dec 
```

<span data-ttu-id="b0691-137">Zellmengen, Zellen, Achsen und Positionen werden in ADO MD durch die entsprechenden Objekte dargestellt: [Cellset](cellset-object-ado-md.md), [Cell](cell-object-ado-md.md), [Axis](axis-object-ado-md.md) und [Position](position-object-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="b0691-137">Cellsets, cells, axes, and positions are all represented in ADO MD by corresponding objects: [Cellset](cellset-object-ado-md.md), [Cell](cell-object-ado-md.md), [Axis](axis-object-ado-md.md), and [Position](position-object-ado-md.md).</span></span>

