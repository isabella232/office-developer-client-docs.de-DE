---
title: CellSet-Objekt (ADO MD)
TOCTitle: Cellset object (ADO MD)
ms:assetid: 28d4b3b9-f907-9ec0-00e1-9666c887cdf0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249047(v=office.15)
ms:contentKeyID: 48543869
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c8cb75ad7277386cfe81b2edcffa234498318444
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296514"
---
# <a name="cellset-object-ado-md"></a>CellSet-Objekt (ADO MD)

**Gilt für**: Access 2013, Office 2013

Stellt die Ergebnisse einer multidimensionalen Abfrage dar. Es ist eine Auflistung von Zellen, die aus Cubes oder anderen Zellmengen ausgewählt wurden.

## <a name="remarks"></a>Bemerkungen

Daten innerhalb einer Zellmenge werden per array-ähnlichem Direktzugriff abgerufen. Sie können einen Drilldown für ein bestimmtes Element ausführen, um Daten zu diesem Element abzurufen. Der folgende Code gibt beispielsweise die Beschriftung des ersten Elements in der ersten Position auf der ersten Achse der Zellmenge **cst** zurück:

`cst.Axes(0).Positions(0).Members(0).Caption`

Innerhalb einer Zellmenge gibt es keine aktuelle Zelle. Stattdessen ruft die [Item](item-property-ado-md-cellset.md)-Eigenschaft ein bestimmtes [Cell](cell-object-ado-md.md)-Objekt aus der Zellmenge ab. Die Argumente der **Item** -Eigenschaft bestimmen, welche Zelle abgerufen wird. Sie können den eindeutigen Ordnungswert einer Zelle angeben. Sie können Zellen auch anhand ihrer Positionsnummern entlang der einzelnen Achsen in der Zellmenge abrufen. Weitere Informationen zum Abrufen von Zellen finden Sie im Thema zur [Item](item-property-ado-md-cellset.md)-Eigenschaft.

Die Auflistungen, Methoden und Eigenschaften eines **Cellset** -Objekts ermöglichen Folgendes:

  - Zuordnen einer geöffneten Verbindung zu einem **Cellset** -Objekt, indem dessen [ActiveConnection](activeconnection-property-ado-md.md)-Eigenschaft festgelegt wird.

  - Ausführen einer multidimensionalen Abfrage und Abrufen der entsprechenden Ergebnisse, indem Sie die [Open](open-method-ado-md.md)-Methode verwenden.

  - Retrieve a **Cell** from the **Cellset** with the [Item](item-property-ado-md-cellset.md) property.

  - Return the [Axis](axis-object-ado-md.md) objects that define the **Cellset** with the [Axes](axes-collection-ado-md.md) collection.

  - Retrieve information about the dimensions used to filter the data in the **Cellset** with the [FilterAxis](filteraxis-property-ado-md.md) property.

  - Return or specify the query used to define the **Cellset** with the [Source](source-property-ado-md.md) property.

  - Return the current state of the **Cellset** (open, closed, executing, or connecting) with the [State](state-property-ado-md.md) property.

  - Close an open **Cellset** with the [Close](close-method-ado-md.md) method.

  - Retrieve provider-specific information about the **Cellset** with the standard ADO [Properties](properties-collection-ado.md) collection.

