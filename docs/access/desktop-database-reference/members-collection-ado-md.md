---
title: Members-Auflistung (ADO MD)
TOCTitle: Members Collection (ADO MD)
ms:assetid: 1389c554-e4f1-107d-22c6-7fe851d53d23
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248910(v=office.15)
ms:contentKeyID: 48543371
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: dd467335102351fc0412b5c77685d6434b0c20a8
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474367"
---
# <a name="members-collection-ado-md"></a>Members-Auflistung (ADO MD)


**Betrifft**: Access 2013 | Office 2013

Enthält die[Member](member-object-ado-md.md)-Objekte einer Ebene oder einer Position entlang einer Achse.

## <a name="remarks"></a>Hinweise

Eine **Members** -Auflistung kann die folgenden Elementtypen enthalten:

  - Die Elemente, die eine Ebene in einem Cube bilden. Sie sind in der Members-Auflistung eines Level-Objekts enthalten. Im Beispiel aus Übersicht über Multidimensionale Schemas und Daten stellen Canada, USA, UK und Germany die vier Elemente der Länderebene dar.

  - Die Elemente, die die untergeordneten Elemente eines bestimmten Elements in einer Hierarchie darstellen. Diese Elemente werden von der [Children](children-property-ado-md.md)-Eigenschaft des übergeordneten **Member** -Objekts zurückgegeben. In demselben Beispiel sind Canada-East und Canada-West die beiden Elemente, die dem Element Canada untergeordnet sind.

  - Die Elemente, die eine bestimmte Position entlang der Achse einer Zellmenge definieren. Im Beispiel aus Verwenden von multidimensionalen Daten stellen Valentine und Seattle die beiden Elemente der ersten Position auf der X-Achse dar. Diese Elemente sind in der Members-Auflistung eines Position-Objekts enthalten.

**Members** ist eine ADO-Standardauflistung. Die Eigenschaften und Methoden einer Auflistung ermöglichen Folgendes:

  - Abrufen der Anzahl an Objekten in der Auflistung, indem Sie die [Count](count-property-ado.md)-Eigenschaft verwenden.

  - Zurückgeben eines Objekts aus der Auflistung, indem Sie die Standardeigenschaft [Item](item-property-ado.md) verwenden.

  - Aktualisieren der Objekte in der Auflistung aus dem Anbieter, indem Sie die [Refresh](refresh-method-ado.md)-Methode verwenden.

