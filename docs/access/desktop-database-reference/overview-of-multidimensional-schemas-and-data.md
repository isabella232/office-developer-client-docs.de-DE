---
title: Übersicht über multidimensionale Schemas und Daten
TOCTitle: Overview of multidimensional schemas and data
ms:assetid: a963e993-b7bf-eeb4-ecd5-d6fe43cf4bb5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249784(v=office.15)
ms:contentKeyID: 48546923
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d65378bf964ad8c6e81a08cb653f09bf00a8431c
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28720219"
---
# <a name="overview-of-multidimensional-schemas-and-data"></a><span data-ttu-id="ce61a-102">Übersicht über multidimensionale Schemas und Daten</span><span class="sxs-lookup"><span data-stu-id="ce61a-102">Overview of multidimensional schemas and data</span></span>

<span data-ttu-id="ce61a-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ce61a-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="understanding-multidimensional-schemas"></a><span data-ttu-id="ce61a-104">Grundlegendes zu multidimensionalen Schemas</span><span class="sxs-lookup"><span data-stu-id="ce61a-104">Understanding Multidimensional Schemas</span></span>

<span data-ttu-id="ce61a-105">Das zentrale Metadatenobjekt in ADO MD ist der *Cube*, der aus einer strukturierten Menge verwandter Dimensionen, Hierarchien, Ebenen und Elementen besteht.</span><span class="sxs-lookup"><span data-stu-id="ce61a-105">The central metadata object in ADO MD is the *cube*, which consists of a structured set of related dimensions, hierarchies, levels, and members.</span></span>

<span data-ttu-id="ce61a-106">Eine *Dimension* ist eine unabhängige Kategorie mit Daten aus der multidimensionalen Datenbank, die von Ihrer Geschäftseinheiten abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="ce61a-106">A *dimension* is an independent category of data from your multidimensional database, derived from your business entities.</span></span> <span data-ttu-id="ce61a-107">Eine Dimension enthält normalerweise Elemente, die als Abfragekriterien für die Maßeinheiten der Datenbank verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ce61a-107">A dimension typically contains items to be used as query criteria for the measures of the database.</span></span>

<span data-ttu-id="ce61a-108">Eine *Hierarchie* ist ein Pfad einer Aggregation einer Dimension.</span><span class="sxs-lookup"><span data-stu-id="ce61a-108">A *hierarchy* is a path of aggregation of a dimension.</span></span> <span data-ttu-id="ce61a-109">Eine Dimension kann mehrere Granularitätsebenen haben, die jeweils Beziehungen zwischen unter- und übergeordneten Elementen haben.</span><span class="sxs-lookup"><span data-stu-id="ce61a-109">A dimension may have multiple levels of granularity, which have parent-child relationships.</span></span> <span data-ttu-id="ce61a-110">Eine Hierarchie definiert, wie diese Ebenen miteinander verwandt sind.</span><span class="sxs-lookup"><span data-stu-id="ce61a-110">A hierarchy defines how these levels are related.</span></span>

<span data-ttu-id="ce61a-111">Eine *Ebene* ist ein Schritt der Aggregation in einer Hierarchie.</span><span class="sxs-lookup"><span data-stu-id="ce61a-111">A *level* is a step of aggregation in a hierarchy.</span></span> <span data-ttu-id="ce61a-112">Bei Dimensionen mit mehreren Informationsschichten stellt jede Schicht eine Ebene dar.</span><span class="sxs-lookup"><span data-stu-id="ce61a-112">For dimensions with multiple layers of information, each layer is a level.</span></span>

<span data-ttu-id="ce61a-113">Ein *Member* ist ein Datenelement in einer Dimension.</span><span class="sxs-lookup"><span data-stu-id="ce61a-113">A *member* is a data item in a dimension.</span></span> <span data-ttu-id="ce61a-114">In der Regel erstellen Sie eine Beschriftung oder beschreiben Sie eine Maßeinheit der Datenbank, die Elemente verwendet.</span><span class="sxs-lookup"><span data-stu-id="ce61a-114">Typically, you create a caption or describe a measure of the database using members.</span></span>

<span data-ttu-id="ce61a-p105">Cubes werden durch [CubeDef](cubedef-object-ado-md.md)-Objekte in ADO MD dargestellt. Dimensionen, Hierarchien, Ebenen und Elemente werden ebenfalls durch die entsprechenden ADO MD-Objekte dargestellt: [Dimension](dimension-object-ado-md.md), [Hierarchy](hierarchy-object-ado-md.md), [Level](level-object-ado-md.md) und [Member](member-object-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="ce61a-p105">Cubes are represented by [CubeDef](cubedef-object-ado-md.md) objects in ADO MD. Dimensions, hierarchies, levels, and members are also represented by their corresponding ADO MD objects: [Dimension](dimension-object-ado-md.md), [Hierarchy](hierarchy-object-ado-md.md), [Level](level-object-ado-md.md), and [Member](member-object-ado-md.md).</span></span>

## <a name="dimensions"></a><span data-ttu-id="ce61a-117">Dimensions</span><span class="sxs-lookup"><span data-stu-id="ce61a-117">Dimensions</span></span>

<span data-ttu-id="ce61a-p106">Die Dimensionen eines Cubes hängen von Ihren Geschäftsentitäten und den Arten der Daten ab, die in der Datenbank dargestellt werden. In der Regel ist jede Dimension ein unabhängiger Einstiegspunkt oder Mechanismus zum Auswählen von Daten.</span><span class="sxs-lookup"><span data-stu-id="ce61a-p106">The dimensions of a cube depend on your business entities and types of data to be modeled in the database. Typically, each dimension is an independent entry point or mechanism for selecting data.</span></span>

<span data-ttu-id="ce61a-p107">Ein Cube mit Verkaufsdaten enthält beispielsweise die folgenden fünf Dimensionen: Verkaufsberater, Geografie, Zeit, Artikel und Maßeinheiten. Die Dimension für Maßeinheiten enthält Werte der tatsächlichen Verkaufsdaten, während die anderen Dimensionen Möglichkeiten darstellen, die Verkaufsdatenwerte zu gruppieren und in Kategorien zu unterteilen.</span><span class="sxs-lookup"><span data-stu-id="ce61a-p107">For example, a cube containing sales data has the following five dimensions: Salesperson, Geography, Time, Products, and Measures. The Measures dimension contains actual sales data values, while the other dimensions represent ways to categorize and group the sales data values.</span></span>

<span data-ttu-id="ce61a-122">Die Dimension für die Geografie enthält die folgenden Elementgruppen:</span><span class="sxs-lookup"><span data-stu-id="ce61a-122">The Geography dimension has the following set of members:</span></span>

```text
 
{All, North America, Europe, Canada, USA, UK, Germany, Canada-West, 
Canada-East, USA-NW, USA-SW, USA-NE, USA-SE, England, Scotland,  
Wales,Ireland, Germany-North, Germany-South, Ottawa, Toronto,  
Vancouver, Calgary, Seattle, Boise, Los Angeles, Houston,  
Shreveport, Miami, Boston, New York, London, Dover, Glasgow,  
Edinburgh, Cardiff, Pembroke, Belfast, Berlin,  
Hamburg, Munich, Stuttgart} 
```

## <a name="hierarchies"></a><span data-ttu-id="ce61a-123">Hierarchies</span><span class="sxs-lookup"><span data-stu-id="ce61a-123">Hierarchies</span></span>

<span data-ttu-id="ce61a-p108">Hierarchien definieren die Möglichkeiten, die Ebenen einer Dimension zusammenzufassen oder zu gruppieren. Eine Dimension kann mehrere Hierarchien enthalten.</span><span class="sxs-lookup"><span data-stu-id="ce61a-p108">Hierarchies define the ways in which the levels of a dimension can be "rolled up" or grouped. A dimension can have more than one hierarchy.</span></span>

## <a name="levels"></a><span data-ttu-id="ce61a-126">Levels</span><span class="sxs-lookup"><span data-stu-id="ce61a-126">Levels</span></span>

<span data-ttu-id="ce61a-127">Im oben dargestellten Beispiel der Dimension für die Geografie steht jedes Feld für eine Ebene in der Hierarchie.</span><span class="sxs-lookup"><span data-stu-id="ce61a-127">In the example Geography dimension pictured in the previous figure, each box represents a level in the hierarchy.</span></span>

<span data-ttu-id="ce61a-128">Jede Ebene enthält eine Gruppe von Elementen:</span><span class="sxs-lookup"><span data-stu-id="ce61a-128">Each level has a set of members, as follows:</span></span>

  - <span data-ttu-id="ce61a-129">Welt = {All}
</span><span class="sxs-lookup"><span data-stu-id="ce61a-129">The World = {All}</span></span>

  - <span data-ttu-id="ce61a-130">Kontinente = {North America, Europe}
</span><span class="sxs-lookup"><span data-stu-id="ce61a-130">Continents = {North America, Europe}</span></span>

  - <span data-ttu-id="ce61a-131">Länder = {Canada, USA, UK, Germany}
</span><span class="sxs-lookup"><span data-stu-id="ce61a-131">Countries = {Canada, USA, UK, Germany}</span></span>

  - <span data-ttu-id="ce61a-132">Regionen = {Canada-East, Canada-West, USA-NE, USA-NW, USA-SE, USA-SW, England, Ireland, Scotland, Wales, Germany-North, Germany-South}
</span><span class="sxs-lookup"><span data-stu-id="ce61a-132">Regions = {Canada-East, Canada-West, USA-NE, USA-NW, USA-SE, USA-SW, England, Ireland, Scotland, Wales, Germany-North, Germany-South}</span></span>

  - <span data-ttu-id="ce61a-133">Städte = {Ottawa, Toronto, Vancouver, Calgary, Seattle, Boise, Los Angeles, Houston, Shreveport, Miami, Boston, New York, London, Dover, Glasgow, Edinburgh, Cardiff, Pembroke, Belfast, Berlin, Hamburg, Munich, Stuttgart}
</span><span class="sxs-lookup"><span data-stu-id="ce61a-133">Cities = {Ottawa, Toronto, Vancouver, Calgary, Seattle, Boise, Los Angeles, Houston, Shreveport, Miami, Boston, New York, London, Dover, Glasgow, Edinburgh, Cardiff, Pembroke, Belfast, Berlin, Hamburg, Munich, Stuttgart}</span></span>

## <a name="members"></a><span data-ttu-id="ce61a-134">Members</span><span class="sxs-lookup"><span data-stu-id="ce61a-134">Members</span></span>

<span data-ttu-id="ce61a-p109">Elemente auf der Blattebene einer Hierarchie haben keine untergeordneten Elemente, und Elemente auf der Stammebene haben keine übergeordneten Elemente. Alle anderen Elemente haben mindestens ein über- und ein untergeordnetes Element. Wenn beispielsweise die Hierarchiestruktur in der Dimension für die Geografie teilweise durchquert wird, werden folgende Beziehungen zwischen unter- und übergeordneten Elementen gefunden:</span><span class="sxs-lookup"><span data-stu-id="ce61a-p109">Members at the leaf level of a hierarchy have no children, and members at the root level have no parent. All other members have at least one parent and at least one child. For example, a partial traversal of the hierarchy tree in the Geography dimension yields the following parent-child relationships:</span></span>

- <span data-ttu-id="ce61a-138">{All} (übergeordnete) {Europa, Nordamerika}</span><span class="sxs-lookup"><span data-stu-id="ce61a-138">{All} (parent of) {Europe, North America}</span></span>
- <span data-ttu-id="ce61a-139">{North America} (übergeordnete) {Canada, USA}</span><span class="sxs-lookup"><span data-stu-id="ce61a-139">{North America} (parent of) {Canada, USA}</span></span>
- <span data-ttu-id="ce61a-140">{USA} (übergeordnete) {USA-NE, USA-NW, USA-SE, USA-SW}</span><span class="sxs-lookup"><span data-stu-id="ce61a-140">{USA} (parent of) {USA-NE, USA-NW, USA-SE, USA-SW}</span></span>
- <span data-ttu-id="ce61a-141">{USA-NW} (übergeordnete) {Boise, Seattle}</span><span class="sxs-lookup"><span data-stu-id="ce61a-141">{USA-NW} (parent of) {Boise, Seattle}</span></span>

<span data-ttu-id="ce61a-142">Elemente können entlang einer oder mehrerer Hierarchien pro Dimension konsolidiert werden.</span><span class="sxs-lookup"><span data-stu-id="ce61a-142">Members can be consolidated along one or more hierarchies per dimension.</span></span>

<span data-ttu-id="ce61a-143">Dieses Beispiel veranschaulicht außerdem ein weiteres Merkmal: Einige Elemente der Wochenebene der Hierarchie Woche Jahr nicht in jeder Ebene der Hierarchie Jahr Quartal angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ce61a-143">This example also illustrates another characteristic: some members of the Week level of the Year-Week hierarchy do not appear in any level of the Year-Quarter hierarchy.</span></span> <span data-ttu-id="ce61a-144">Eine Hierarchie muss also nicht alle Elemente einer Dimension enthalten.</span><span class="sxs-lookup"><span data-stu-id="ce61a-144">Thus, a hierarchy need not include all members of a dimension.</span></span>

## <a name="understanding-multidimensional-schemas"></a><span data-ttu-id="ce61a-145">Grundlegendes zu multidimensionalen Schemas</span><span class="sxs-lookup"><span data-stu-id="ce61a-145">Understanding Multidimensional Schemas</span></span>

<span data-ttu-id="ce61a-146">Das zentrale Metadatenobjekt in ADO MD ist der *Cube*, der aus einer strukturierten Menge verwandter Dimensionen, Hierarchien, Ebenen und Elementen besteht.</span><span class="sxs-lookup"><span data-stu-id="ce61a-146">The central metadata object in ADO MD is the *cube*, which consists of a structured set of related dimensions, hierarchies, levels, and members.</span></span>

<span data-ttu-id="ce61a-147">Eine *Dimension* ist eine unabhängige Kategorie mit Daten aus der multidimensionalen Datenbank, die von Ihrer Geschäftseinheiten abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="ce61a-147">A *dimension* is an independent category of data from your multidimensional database, derived from your business entities.</span></span> <span data-ttu-id="ce61a-148">Eine Dimension enthält normalerweise Elemente, die als Abfragekriterien für die Maßeinheiten der Datenbank verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ce61a-148">A dimension typically contains items to be used as query criteria for the measures of the database.</span></span>

<span data-ttu-id="ce61a-149">Eine *Hierarchie* ist ein Pfad einer Aggregation einer Dimension.</span><span class="sxs-lookup"><span data-stu-id="ce61a-149">A *hierarchy* is a path of aggregation of a dimension.</span></span> <span data-ttu-id="ce61a-150">Eine Dimension kann mehrere Granularitätsebenen haben, die jeweils Beziehungen zwischen unter- und übergeordneten Elementen haben.</span><span class="sxs-lookup"><span data-stu-id="ce61a-150">A dimension may have multiple levels of granularity, which have parent-child relationships.</span></span> <span data-ttu-id="ce61a-151">Eine Hierarchie definiert, wie diese Ebenen miteinander verwandt sind.</span><span class="sxs-lookup"><span data-stu-id="ce61a-151">A hierarchy defines how these levels are related.</span></span>

<span data-ttu-id="ce61a-152">Eine *Ebene* ist ein Schritt der Aggregation in einer Hierarchie.</span><span class="sxs-lookup"><span data-stu-id="ce61a-152">A *level* is a step of aggregation in a hierarchy.</span></span> <span data-ttu-id="ce61a-153">Bei Dimensionen mit mehreren Informationsschichten stellt jede Schicht eine Ebene dar.</span><span class="sxs-lookup"><span data-stu-id="ce61a-153">For dimensions with multiple layers of information, each layer is a level.</span></span>

<span data-ttu-id="ce61a-154">Ein *Member* ist ein Datenelement in einer Dimension.</span><span class="sxs-lookup"><span data-stu-id="ce61a-154">A *member* is a data item in a dimension.</span></span> <span data-ttu-id="ce61a-155">In der Regel erstellen Sie eine Beschriftung oder beschreiben Sie eine Maßeinheit der Datenbank, die Elemente verwendet.</span><span class="sxs-lookup"><span data-stu-id="ce61a-155">Typically, you create a caption or describe a measure of the database using members.</span></span>

<span data-ttu-id="ce61a-p115">Cubes werden durch [CubeDef](cubedef-object-ado-md.md)-Objekte in ADO MD dargestellt. Dimensionen, Hierarchien, Ebenen und Elemente werden ebenfalls durch die entsprechenden ADO MD-Objekte dargestellt: [Dimension](dimension-object-ado-md.md), [Hierarchy](hierarchy-object-ado-md.md), [Level](level-object-ado-md.md) und [Member](member-object-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="ce61a-p115">Cubes are represented by [CubeDef](cubedef-object-ado-md.md) objects in ADO MD. Dimensions, hierarchies, levels, and members are also represented by their corresponding ADO MD objects: [Dimension](dimension-object-ado-md.md), [Hierarchy](hierarchy-object-ado-md.md), [Level](level-object-ado-md.md), and [Member](member-object-ado-md.md).</span></span>

## <a name="dimensions"></a><span data-ttu-id="ce61a-158">Dimensions</span><span class="sxs-lookup"><span data-stu-id="ce61a-158">Dimensions</span></span>

<span data-ttu-id="ce61a-p116">Die Dimensionen eines Cubes hängen von Ihren Geschäftsentitäten und den Arten der Daten ab, die in der Datenbank dargestellt werden. In der Regel ist jede Dimension ein unabhängiger Einstiegspunkt oder Mechanismus zum Auswählen von Daten.</span><span class="sxs-lookup"><span data-stu-id="ce61a-p116">The dimensions of a cube depend on your business entities and types of data to be modeled in the database. Typically, each dimension is an independent entry point or mechanism for selecting data.</span></span>

<span data-ttu-id="ce61a-p117">Ein Cube mit Verkaufsdaten enthält beispielsweise die folgenden fünf Dimensionen: Verkaufsberater, Geografie, Zeit, Artikel und Maßeinheiten. Die Dimension für Maßeinheiten enthält Werte der tatsächlichen Verkaufsdaten, während die anderen Dimensionen Möglichkeiten darstellen, die Verkaufsdatenwerte zu gruppieren und in Kategorien zu unterteilen.</span><span class="sxs-lookup"><span data-stu-id="ce61a-p117">For example, a cube containing sales data has the following five dimensions: Salesperson, Geography, Time, Products, and Measures. The Measures dimension contains actual sales data values, while the other dimensions represent ways to categorize and group the sales data values.</span></span>

<span data-ttu-id="ce61a-163">Die Dimension für die Geografie enthält die folgenden Elementgruppen:</span><span class="sxs-lookup"><span data-stu-id="ce61a-163">The Geography dimension has the following set of members:</span></span>

```text 
 
{All, North America, Europe, Canada, USA, UK, Germany, Canada-West, 
Canada-East, USA-NW, USA-SW, USA-NE, USA-SE, England, Scotland,  
Wales,Ireland, Germany-North, Germany-South, Ottawa, Toronto,  
Vancouver, Calgary, Seattle, Boise, Los Angeles, Houston,  
Shreveport, Miami, Boston, New York, London, Dover, Glasgow,  
Edinburgh, Cardiff, Pembroke, Belfast, Berlin,  
Hamburg, Munich, Stuttgart} 
```

## <a name="hierarchies"></a><span data-ttu-id="ce61a-164">Hierarchies</span><span class="sxs-lookup"><span data-stu-id="ce61a-164">Hierarchies</span></span>

<span data-ttu-id="ce61a-p118">Hierarchien definieren die Möglichkeiten, die Ebenen einer Dimension zusammenzufassen oder zu gruppieren. Eine Dimension kann mehrere Hierarchien enthalten.</span><span class="sxs-lookup"><span data-stu-id="ce61a-p118">Hierarchies define the ways in which the levels of a dimension can be "rolled up" or grouped. A dimension can have more than one hierarchy.</span></span>

## <a name="levels"></a><span data-ttu-id="ce61a-167">Levels</span><span class="sxs-lookup"><span data-stu-id="ce61a-167">Levels</span></span>

<span data-ttu-id="ce61a-168">Im oben dargestellten Beispiel der Dimension für die Geografie steht jedes Feld für eine Ebene in der Hierarchie.</span><span class="sxs-lookup"><span data-stu-id="ce61a-168">In the example Geography dimension pictured in the previous figure, each box represents a level in the hierarchy.</span></span>

<span data-ttu-id="ce61a-169">Jede Ebene enthält eine Gruppe von Elementen:</span><span class="sxs-lookup"><span data-stu-id="ce61a-169">Each level has a set of members, as follows:</span></span>

- <span data-ttu-id="ce61a-170">Welt = {All}
</span><span class="sxs-lookup"><span data-stu-id="ce61a-170">The World = {All}</span></span>

- <span data-ttu-id="ce61a-171">Kontinente = {North America, Europe}
</span><span class="sxs-lookup"><span data-stu-id="ce61a-171">Continents = {North America, Europe}</span></span>

- <span data-ttu-id="ce61a-172">Länder = {Canada, USA, UK, Germany}
</span><span class="sxs-lookup"><span data-stu-id="ce61a-172">Countries = {Canada, USA, UK, Germany}</span></span>

- <span data-ttu-id="ce61a-173">Regionen = {Canada-East, Canada-West, USA-NE, USA-NW, USA-SE, USA-SW, England, Ireland, Scotland, Wales, Germany-North, Germany-South}
</span><span class="sxs-lookup"><span data-stu-id="ce61a-173">Regions = {Canada-East, Canada-West, USA-NE, USA-NW, USA-SE, USA-SW, England, Ireland, Scotland, Wales, Germany-North, Germany-South}</span></span>

- <span data-ttu-id="ce61a-174">Städte = {Ottawa, Toronto, Vancouver, Calgary, Seattle, Boise, Los Angeles, Houston, Shreveport, Miami, Boston, New York, London, Dover, Glasgow, Edinburgh, Cardiff, Pembroke, Belfast, Berlin, Hamburg, Munich, Stuttgart}
</span><span class="sxs-lookup"><span data-stu-id="ce61a-174">Cities = {Ottawa, Toronto, Vancouver, Calgary, Seattle, Boise, Los Angeles, Houston, Shreveport, Miami, Boston, New York, London, Dover, Glasgow, Edinburgh, Cardiff, Pembroke, Belfast, Berlin, Hamburg, Munich, Stuttgart}</span></span>

## <a name="members"></a><span data-ttu-id="ce61a-175">Members</span><span class="sxs-lookup"><span data-stu-id="ce61a-175">Members</span></span>

<span data-ttu-id="ce61a-p119">Elemente auf der Blattebene einer Hierarchie haben keine untergeordneten Elemente, und Elemente auf der Stammebene haben keine übergeordneten Elemente. Alle anderen Elemente haben mindestens ein über- und ein untergeordnetes Element. Wenn beispielsweise die Hierarchiestruktur in der Dimension für die Geografie teilweise durchquert wird, werden folgende Beziehungen zwischen unter- und übergeordneten Elementen gefunden:</span><span class="sxs-lookup"><span data-stu-id="ce61a-p119">Members at the leaf level of a hierarchy have no children, and members at the root level have no parent. All other members have at least one parent and at least one child. For example, a partial traversal of the hierarchy tree in the Geography dimension yields the following parent-child relationships:</span></span>

- <span data-ttu-id="ce61a-179">{All} (übergeordnete) {Europa, Nordamerika}</span><span class="sxs-lookup"><span data-stu-id="ce61a-179">{All} (parent of) {Europe, North America}</span></span>

- <span data-ttu-id="ce61a-180">{North America} (übergeordnete) {Canada, USA}</span><span class="sxs-lookup"><span data-stu-id="ce61a-180">{North America} (parent of) {Canada, USA}</span></span>

- <span data-ttu-id="ce61a-181">{USA} (übergeordnete) {USA-NE, USA-NW, USA-SE, USA-SW}</span><span class="sxs-lookup"><span data-stu-id="ce61a-181">{USA} (parent of) {USA-NE, USA-NW, USA-SE, USA-SW}</span></span>

- <span data-ttu-id="ce61a-182">{USA-NW} (übergeordnete) {Boise, Seattle}</span><span class="sxs-lookup"><span data-stu-id="ce61a-182">{USA-NW} (parent of) {Boise, Seattle}</span></span>

<span data-ttu-id="ce61a-183">Elemente können entlang einer oder mehrerer Hierarchien pro Dimension konsolidiert werden.</span><span class="sxs-lookup"><span data-stu-id="ce61a-183">Members can be consolidated along one or more hierarchies per dimension.</span></span>

<span data-ttu-id="ce61a-184">Dieses Beispiel veranschaulicht außerdem ein weiteres Merkmal: Einige Elemente der Wochenebene der Hierarchie Woche Jahr nicht in jeder Ebene der Hierarchie Jahr Quartal angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ce61a-184">This example also illustrates another characteristic: some members of the Week level of the Year-Week hierarchy do not appear in any level of the Year-Quarter hierarchy.</span></span> <span data-ttu-id="ce61a-185">Eine Hierarchie muss also nicht alle Elemente einer Dimension enthalten.</span><span class="sxs-lookup"><span data-stu-id="ce61a-185">Thus, a hierarchy need not include all members of a dimension.</span></span>

