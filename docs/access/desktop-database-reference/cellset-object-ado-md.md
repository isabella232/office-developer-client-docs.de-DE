---
title: Cellset-Objekt (ADO MD)
TOCTitle: Cellset object (ADO MD)
ms:assetid: 28d4b3b9-f907-9ec0-00e1-9666c887cdf0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249047(v=office.15)
ms:contentKeyID: 48543869
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c8cb75ad7277386cfe81b2edcffa234498318444
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28702187"
---
# <a name="cellset-object-ado-md"></a>Cellset-Objekt (ADO MD)

**Betrifft**: Access 2013, Office 2013

Stellt die Ergebnisse einer multidimensionalen Abfrage dar. Es ist eine Auflistung von Zellen, die aus Cubes oder anderen Zellmengen ausgewählt wurden.

## <a name="remarks"></a>Hinweise

Daten innerhalb einer Zellmenge werden per array-ähnlichem Direktzugriff abgerufen. Sie können einen Drilldown für ein bestimmtes Element ausführen, um Daten zu diesem Element abzurufen. Der folgende Code gibt beispielsweise die Beschriftung des ersten Elements in der ersten Position auf der ersten Achse der Zellmenge **cst** zurück:

`cst.Axes(0).Positions(0).Members(0).Caption`

Innerhalb einer Zellmenge gibt es keine aktuelle Zelle. Stattdessen ruft die [Item](item-property-ado-md-cellset.md)-Eigenschaft ein bestimmtes [Cell](cell-object-ado-md.md)-Objekt aus der Zellmenge ab. Die Argumente der **Item** -Eigenschaft bestimmen, welche Zelle abgerufen wird. Sie können den eindeutigen Ordnungswert einer Zelle angeben. Sie können Zellen auch anhand ihrer Positionsnummern entlang der einzelnen Achsen in der Zellmenge abrufen. Weitere Informationen zum Abrufen von Zellen finden Sie im Thema zur [Item](item-property-ado-md-cellset.md)-Eigenschaft.

Die Auflistungen, Methoden und Eigenschaften eines **Cellset** -Objekts ermöglichen Folgendes:

  - Zuordnen einer geöffneten Verbindung zu einem **Cellset** -Objekt, indem dessen [ActiveConnection](activeconnection-property-ado-md.md)-Eigenschaft festgelegt wird.

  - Ausführen einer multidimensionalen Abfrage und Abrufen der entsprechenden Ergebnisse, indem Sie die [Open](open-method-ado-md.md)-Methode verwenden.

  - Abrufen einer**** Zelle aus der**** Zellmenge, indem Sie die [Item](item-property-ado-md-cellset.md)-Eigenschaft verwenden.

  - Zurückgeben der [Axis](axis-object-ado-md.md)-Objekte, die die**** Zellmenge definieren, indem Sie die [Axes](axes-collection-ado-md.md)-Auflistung verwenden.

  - Abrufen von Informationen zu den Dimensionen, die zum Filtern der Daten in der**** Zellmenge verwendet werden, indem Sie die [FilterAxis](filteraxis-property-ado-md.md)-Eigenschaft verwenden.

  - Zurückgeben oder Angeben der Abfrage, mit der die**** Zellmenge definiert wird, indem Sie die [Source](source-property-ado-md.md)-Eigenschaft verwenden.

  - Zurückgeben des aktuellen Status der**** Zellmenge (geöffnet, geschlossen, wird ausgeführt oder Verbindung wird hergestellt), indem Sie die [State](state-property-ado-md.md)-Eigenschaft verwenden.

  - Schließen einer geöffneten**** Zellmenge, indem Sie die [Close](close-method-ado-md.md)-Methode verwenden.

  - Abrufen anbieterspezifischer Informationen zum**** Cellset (Zellmenge), indem Sie die ADO-Standardauflistung [Properties](properties-collection-ado.md) verwenden.

