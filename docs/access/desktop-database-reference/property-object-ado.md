---
title: Property-Objekt (ADO)
TOCTitle: Property object (ADO)
ms:assetid: eec318fd-f5ed-d9ef-9830-848439a8914d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250210(v=office.15)
ms:contentKeyID: 48548567
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 262f4873359508a985b27f3d4ea70a5fcbfd620f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302919"
---
# <a name="property-object-ado"></a>Property-Objekt (ADO)


**Gilt für**: Access 2013, Office 2013

Stellt ein dynamisches Merkmal eines ADO-Objekts dar, das vom Anbieter definiert wird.

## <a name="remarks"></a>Bemerkungen

ADO-Objekte weisen zwei Arten von Eigenschaften auf, nämlich integrierte und dynamische Eigenschaften.

Bei integrierten Eigenschaften handelt es sich um die Eigenschaften, die in ADO implementiert werden und die mit der Syntax sofort für jedes neue Objekt verfügbar sind. Sie erscheinen nicht als **Property** -Objekte in der [Properties](properties-collection-ado.md)-Auflistung eines Objekts, sodass Sie ihre Merkmale nicht ändern können, obwohl ihre Werte geändert werden können.

Dynamische Eigenschaften werden durch den zugrunde liegenden Datenanbieter definiert und in der **Properties** -Auflistung für das entsprechende ADO-Objekt angezeigt. Beispielsweise kann eine anbieterspezifische Eigenschaft kennzeichnen, ob Transaktionen oder Aktualisierungen von einem [Recordset](recordset-object-ado.md)-Objekt unterstützt werden. Diese zusätzlichen Eigenschaften werden als **Property**-Objekte in der **Properties**-Auflistung dieses **Recordset**-Objekts angezeigt. Auf dynamische Eigenschaften kann nur über die Auflistung mit der MyObject. Properties (0)-oder MyObject. Properties ("Name")-Syntax verwiesen werden.

Keiner der beiden Eigenschaftstypen kann gelöscht werden.

Ein dynamisches **Property**-Objekt weist vier integrierte Eigenschaften auf:

  - Die [Name](name-property-ado.md)-Eigenschaft ist eine Zeichenfolge zur Identifizierung der Eigenschaft.

  - Die [Type](type-property-ado.md)-Eigenschaft ist eine ganze Zahl zur Angabe des Datentyps der Eigenschaft.

  - The [Value](value-property-ado.md) property is a variant that contains the property setting. **Value** is the default property for a **Property** object.

  - The [Attributes](attributes-property-ado.md) property is a long value that indicates characteristics of the property specific to the provider.

