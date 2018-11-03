---
title: Axis-Objekt (ADO MD)
TOCTitle: Axis object (ADO MD)
ms:assetid: a4332b69-8900-08f1-a4e2-9395d005ed42
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249763(v=office.15)
ms:contentKeyID: 48546807
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6e90ff31c0b6a78a3f242927e2fa7e84c42d6ab3
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25945348"
---
# <a name="axis-object-ado-md"></a>Axis-Objekt (ADO MD)


**Betrifft**: Access 2013, Office 2013

Stellt eine Positions- oder Filterachse einer Zellmenge dar, die ausgewählte Elemente einer oder mehrerer Dimensionen enthält.

## <a name="remarks"></a>Hinweise

Ein **Axis** -Objekt kann Bestandteil einer [Axes](axes-collection-ado-md.md)-Auflistung sein oder von der [FilterAxis](filteraxis-property-ado-md.md)-Eigenschaft einer [Zellmenge](cellset-object-ado-md.md) zurückgegeben werden.

Die Auflistungen und Eigenschaften eines **Axis** -Objekts ermöglichen Folgendes:

- Identifizieren der**** Achse, indem Sie die [Name](name-property-ado-md.md)-Eigenschaft verwenden.

- Durchlaufen der einzelnen Positionen entlang einer**** Achse, indem Sie die [Positions](positions-collection-ado-md.md)-Auflistung verwenden.

- Abrufen der Anzahl an Dimensionen auf der**** Achse, indem Sie die [DimensionCount](dimensioncount-property-ado-md.md)-Eigenschaft verwenden.

- Abrufen anbieterspezifischer Attribute für die**** Achse, indem Sie die ADO-Standardauflistung [Properties](properties-collection-ado.md) verwenden.

