---
title: Übersicht über multidimensionale Schemas und Daten
TOCTitle: Overview of multidimensional schemas and data
ms:assetid: a963e993-b7bf-eeb4-ecd5-d6fe43cf4bb5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249784(v=office.15)
ms:contentKeyID: 48546923
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 6b63a5d75bf4bc5d38e2b3efa3f53da5b221139b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59558156"
---
# <a name="overview-of-multidimensional-schemas-and-data"></a>Übersicht über multidimensionale Schemas und Daten

**Gilt für**: Access 2013, Office 2013

## <a name="understanding-multidimensional-schemas"></a>Grundlegendes zu multidimensionalen Schemas

Das zentrale Metadatenobjekt in ADO MD ist der *Cube*, der aus einer strukturierten Menge verwandter Dimensionen, Hierarchien, Ebenen und Elementen besteht.

Eine *Dimension* ist eine unabhängige Kategorie mit Daten aus der multidimensionalen Datenbank, die von Ihren Geschäftsentitäten abgeleitet wird. Eine Dimension enthält normalerweise Elemente, die als Abfragekriterien für die Maßeinheiten der Datenbank verwendet werden.

Eine *Hierarchie* ist ein Aggregationspfad einer Dimension. Eine Dimension kann mehrere Granularitätsebenen haben, die jeweils Beziehungen zwischen unter- und übergeordneten Elementen haben. Eine Hierarchie definiert, wie diese Ebenen miteinander verwandt sind.

Eine *Ebene* ist ein Aggregationsschritt in einer Hierarchie. Bei Dimensionen mit mehreren Informationsschichten stellt jede Schicht eine Ebene dar.

Ein *Element* ist ein Datenelement in einer Dimension. In der Regel erstellen Sie eine Beschriftung oder beschreiben Sie eine Maßeinheit der Datenbank, die Elemente verwendet.

Cubes werden durch [CubeDef](cubedef-object-ado-md.md)-Objekte in ADO MD dargestellt. Dimensionen, Hierarchien, Ebenen und Elemente werden ebenfalls durch die entsprechenden ADO MD-Objekte dargestellt: [Dimension](dimension-object-ado-md.md), [Hierarchy](hierarchy-object-ado-md.md), [Level](level-object-ado-md.md) und [Member](member-object-ado-md.md).

## <a name="dimensions"></a>Maße

Die Dimensionen eines Cubes hängen von Ihren Geschäftsentitäten und den Arten der Daten ab, die in der Datenbank dargestellt werden. In der Regel ist jede Dimension ein unabhängiger Einstiegspunkt oder Mechanismus zum Auswählen von Daten.

Ein Cube mit Verkaufsdaten enthält beispielsweise die folgenden fünf Dimensionen: Verkaufsberater, Geografie, Zeit, Artikel und Maßeinheiten. Die Dimension für Maßeinheiten enthält Werte der tatsächlichen Verkaufsdaten, während die anderen Dimensionen Möglichkeiten darstellen, die Verkaufsdatenwerte zu gruppieren und in Kategorien zu unterteilen.

Die Dimension für die Geografie enthält die folgenden Elementgruppen:

```text
 
{All, North America, Europe, Canada, USA, UK, Germany, Canada-West, 
Canada-East, USA-NW, USA-SW, USA-NE, USA-SE, England, Scotland,  
Wales,Ireland, Germany-North, Germany-South, Ottawa, Toronto,  
Vancouver, Calgary, Seattle, Boise, Los Angeles, Houston,  
Shreveport, Miami, Boston, New York, London, Dover, Glasgow,  
Edinburgh, Cardiff, Pembroke, Belfast, Berlin,  
Hamburg, Munich, Stuttgart} 
```

## <a name="hierarchies"></a>Hierarchien

Hierarchien definieren die Möglichkeiten, die Ebenen einer Dimension zusammenzufassen oder zu gruppieren. Eine Dimension kann mehrere Hierarchien enthalten.

## <a name="levels"></a>Abstufungen

Im oben dargestellten Beispiel der Dimension für die Geografie steht jedes Feld für eine Ebene in der Hierarchie.

Jede Ebene enthält eine Gruppe von Elementen:

  - Welt = {All}


  - 1993 = {Nordamerika, Europa}

  - Länder = {Kanada, USA, Vereinigtes Königreich, Deutschland}

  - Regions = {Canada-East, Canada-West, USA-NE, USA-NW, USA-SE, USA-SW, England, Ireland, Canada, Emea, Germany-North, Germany-South}

  - Cities = {Seattle, Seattle,Aufgelegen, Blätter, Seattle, Seattle, Seattle, Los Los Seattle, Kate, Shreveport, Kapseln, Ny, New York, London, Dover, Kate,Aufsingen, Blätter, Blätter, Pembroke,Aufgelegen, Berlin, Kapseln, Kate}

## <a name="members"></a>Members

Elemente auf der Blattebene einer Hierarchie haben keine untergeordneten Elemente, und Elemente auf der Stammebene haben keine übergeordneten Elemente. Alle anderen Elemente haben mindestens ein über- und ein untergeordnetes Element. Wenn beispielsweise die Hierarchiestruktur in der Dimension für die Geografie teilweise durchquert wird, werden folgende Beziehungen zwischen unter- und übergeordneten Elementen gefunden:

- {All} (übergeordnetes Element von) {Europa, Nordamerika}
- {Nordamerika} (übergeordnetes Element von) {Kanada, USA}
- {USA} (übergeordnetes Element von) {USA-NE, USA-NW, USA-SE, USA-SW}
- {USA-NW} (übergeordnetes Element von) {Seattlee, Seattle}

Elemente können entlang einer oder mehrerer Hierarchien pro Dimension konsolidiert werden.

In diesem Beispiel wird auch ein weiteres Merkmal veranschaulicht: Einige Elemente der Ebene Woche der Year-Week Hierarchie werden in keiner Ebene der Year-Quarter Hierarchie angezeigt. Eine Hierarchie muss also nicht alle Elemente einer Dimension enthalten.
