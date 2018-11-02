---
title: Property-Objekt (ADO)
TOCTitle: Property object (ADO)
ms:assetid: eec318fd-f5ed-d9ef-9830-848439a8914d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250210(v=office.15)
ms:contentKeyID: 48548567
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b26a305557e2b7244399c6c2c5513909846eaaff
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25929569"
---
# <a name="property-object-ado"></a>Property-Objekt (ADO)


**Betrifft**: Access 2013, Office 2013

Stellt ein dynamisches Merkmal eines ADO-Objekts dar, das vom Anbieter definiert wird.

## <a name="remarks"></a>Hinweise

ADO-Objekte weisen zwei Arten von Eigenschaften auf, nämlich integrierte und dynamische Eigenschaften.

Integrierte Eigenschaften sind diese Eigenschaften in ADO implementiert und für jedes neue Objekt mithilfe der Syntax. Sie erscheinen nicht als **Property** -Objekte in der [Properties](properties-collection-ado.md)-Auflistung eines Objekts, sodass Sie ihre Merkmale nicht ändern können, obwohl ihre Werte geändert werden können.

Dynamische Eigenschaften werden durch den zugrunde liegenden Datenanbieter definiert und in der **Properties** -Auflistung für das entsprechende ADO-Objekt angezeigt. Beispielsweise kann eine anbieterspezifische Eigenschaft anzeigen, ob Transaktionen oder Aktualisierungen von einem [Recordset](recordset-object-ado.md) -Objekt unterstützt werden. Diese zusätzlichen Eigenschaften werden als **Property** -Objekte in der **Properties** -Auflistung dieses **Recordset** -Objekts angezeigt. Dynamische Eigenschaften können nur über die Auflistung mithilfe der MyObject.Properties(0) verwiesen werden oder oder MyObject.Properties("Name") Syntax.

Keiner der beiden Eigenschaftstypen kann gelöscht werden.

Ein dynamisches **Property** -Objekt weist vier integrierte Eigenschaften auf:

  - Die [Name](name-property-ado.md) -Eigenschaft ist eine Zeichenfolge zur Identifizierung der Eigenschaft.

  - Die [Type](type-property-ado.md) -Eigenschaft ist eine ganze Zahl zur Angabe des Datentyps der Eigenschaft.

  - Die Value-Eigenschaft ist vom Datentyp Variant und enthält die Eigenschaftseinstellung. Value ist die Standardeigenschaft für ein Property-Objekt.

  - Die [Attributes](attributes-property-ado.md) -Eigenschaft ist ein long-Wert, der Merkmale der anbieterspezifischen Eigenschaft angibt.

