---
title: Members-Auflistung (ADO MD)
TOCTitle: Members collection (ADO MD)
ms:assetid: 1389c554-e4f1-107d-22c6-7fe851d53d23
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248910(v=office.15)
ms:contentKeyID: 48543371
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 474b2ccb10fbd4d68e89c352fa8700e33a2923da
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59602213"
---
# <a name="members-collection-ado-md"></a>Members-Auflistung (ADO MD)


**Gilt für**: Access 2013, Office 2013

Enthält die[Member](member-object-ado-md.md)-Objekte einer Ebene oder einer Position entlang einer Achse.

## <a name="remarks"></a>HinwBemerkungeneise

Eine **Members**-Auflistung kann die folgenden Elementtypen enthalten:

  - The members that make up a level in a cube. These are contained in the **Members** collection of a [Level](level-object-ado-md.md) object. For example, using the sample from [Overview of Multidimensional Schemas and Data](overview-of-multidimensional-schemas-and-data.md), the four members of the Countries level are Canada, USA, UK, and Germany.

  - Die Elemente, die die untergeordneten Elemente eines bestimmten Elements in einer Hierarchie darstellen. Diese Elemente werden von der [Children](children-property-ado-md.md)-Eigenschaft des übergeordneten **Member** -Objekts zurückgegeben. In demselben Beispiel sind Canada-East und Canada-West die beiden Elemente, die dem Element Canada untergeordnet sind.

  - The members that define a specific position along an axis of a [cellset](cellset-object-ado-md.md). Using the cellset from [Working with Multidimensional Data](working-with-multidimensional-data.md) as an example, the two members of the first position on the x-axis are Valentine and Seattle. These members are contained by the **Members** collection of a [Position](position-object-ado-md.md) object.

**Members** ist eine ADO-Standardauflistung. Die Eigenschaften und Methoden einer Auflistung ermöglichen Folgendes:

  - Abrufen der Anzahl an Objekten in der Auflistung, indem Sie die [Count](count-property-ado.md)-Eigenschaft verwenden.

  - Zurückgeben eines Objekts aus der Auflistung, indem Sie die Standardeigenschaft [Item](item-property-ado.md) verwenden.

  - Aktualisieren der Objekte in der Auflistung aus dem Anbieter, indem Sie die [Refresh](refresh-method-ado.md)-Methode verwenden.

