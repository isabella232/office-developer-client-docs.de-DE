---
title: Axis-Objekt (ADO MD)
TOCTitle: Axis object (ADO MD)
ms:assetid: a4332b69-8900-08f1-a4e2-9395d005ed42
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249763(v=office.15)
ms:contentKeyID: 48546807
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ba1e32c3d2638589675a45c7cbc5a3e722651358
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25928432"
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

