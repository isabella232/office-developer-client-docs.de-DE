---
title: Axis-Objekt (ADO MD)
TOCTitle: Axis object (ADO MD)
ms:assetid: a4332b69-8900-08f1-a4e2-9395d005ed42
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249763(v=office.15)
ms:contentKeyID: 48546807
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 057fa3c22c399f6f573a3ee2028cd7a80d8ad937
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59602920"
---
# <a name="axis-object-ado-md"></a>Axis-Objekt (ADO MD)


**Gilt für**: Access 2013, Office 2013

Stellt eine Positions- oder Filterachse einer Zellmenge dar, die ausgewählte Elemente einer oder mehrerer Dimensionen enthält.

## <a name="remarks"></a>HinwBemerkungeneise

Ein **Axis**-Objekt kann Bestandteil einer [Axes](axes-collection-ado-md.md)-Auflistung sein oder von der [FilterAxis](filteraxis-property-ado-md.md)-Eigenschaft einer [Zellmenge](cellset-object-ado-md.md) zurückgegeben werden.

Die Auflistungen und Eigenschaften eines **Axis**-Objekts ermöglichen Folgendes:

- Identifizieren derAchse, indem Sie die [Name](name-property-ado-md.md)-Eigenschaft verwenden.

- Durchlaufen der einzelnen Positionen entlang einerAchse, indem Sie die [Positions](positions-collection-ado-md.md)-Auflistung verwenden.

- Abrufen der Anzahl an Dimensionen auf derAchse, indem Sie die [DimensionCount](dimensioncount-property-ado-md.md)-Eigenschaft verwenden.

- Abrufen anbieterspezifischer Attribute für dieAchse, indem Sie die ADO-Standardauflistung [Properties](properties-collection-ado.md) verwenden.

