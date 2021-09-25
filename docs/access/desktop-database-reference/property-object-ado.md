---
title: Property-Objekt (ADO)
TOCTitle: Property object (ADO)
ms:assetid: eec318fd-f5ed-d9ef-9830-848439a8914d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250210(v=office.15)
ms:contentKeyID: 48548567
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: a3fa2aad6506645db276d55d13257e8d2e2eafe5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59565107"
---
# <a name="property-object-ado"></a>Property-Objekt (ADO)


**Gilt für**: Access 2013, Office 2013

Stellt ein dynamisches Merkmal eines ADO-Objekts dar, das vom Anbieter definiert wird.

## <a name="remarks"></a>HinwBemerkungeneise

ADO-Objekte weisen zwei Arten von Eigenschaften auf, nämlich integrierte und dynamische Eigenschaften.

Integrierte Eigenschaften sind diese Eigenschaften, die in ADO implementiert sind und mithilfe der Syntax sofort für jedes neue Objekt verfügbar sind. Sie erscheinen nicht als **Property** -Objekte in der [Properties](properties-collection-ado.md)-Auflistung eines Objekts, sodass Sie ihre Merkmale nicht ändern können, obwohl ihre Werte geändert werden können.

Dynamische Eigenschaften werden durch den zugrunde liegenden Datenanbieter definiert und in der **Properties** -Auflistung für das entsprechende ADO-Objekt angezeigt. Beispielsweise kann eine anbieterspezifische Eigenschaft kennzeichnen, ob Transaktionen oder Aktualisierungen von einem [Recordset](recordset-object-ado.md)-Objekt unterstützt werden. Diese zusätzlichen Eigenschaften werden als **Property**-Objekte in der **Properties**-Auflistung dieses **Recordset**-Objekts angezeigt. Auf dynamische Eigenschaften kann nur über die Auflistung mithilfe der Syntax MyObject.Properties(0) oder MyObject.Properties("Name verwiesen werden.

Keiner der beiden Eigenschaftstypen kann gelöscht werden.

Ein dynamisches **Property**-Objekt weist vier integrierte Eigenschaften auf:

  - Die [Name](name-property-ado.md)-Eigenschaft ist eine Zeichenfolge zur Identifizierung der Eigenschaft.

  - Die [Type](type-property-ado.md)-Eigenschaft ist eine ganze Zahl zur Angabe des Datentyps der Eigenschaft.

  - The [Value](value-property-ado.md) property is a variant that contains the property setting. **Value** is the default property for a **Property** object.

  - The [Attributes](attributes-property-ado.md) property is a long value that indicates characteristics of the property specific to the provider.

