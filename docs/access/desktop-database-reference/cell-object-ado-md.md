---
title: Cell-Objekt (ADO MD)
TOCTitle: Cell object (ADO MD)
ms:assetid: b9d00b71-1f40-5bd1-4b89-fbdb59c552ba
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249892(v=office.15)
ms:contentKeyID: 48547356
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 1fd28f453ef38b8a2e71f0e479c19fcd05c50aca
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59590100"
---
# <a name="cell-object-ado-md"></a>Cell-Objekt (ADO MD)


**Gilt für**: Access 2013, Office 2013

Stellt die Daten am Kreuzungspunkt von Achsenkoordinaten dar, die in einer Zellmenge enthalten sind.

## <a name="remarks"></a>HinwBemerkungeneise

Ein **Cell**-Objekt wird von der [Item](item-property-ado-md-cellset.md)-Eigenschaft eines [Cellset](cellset-object-ado-md.md)-Objekts zurückgegeben.

Die Auflistungen und Eigenschaften eines **Cell** -Objekts ermöglichen Folgendes:

- Return the data in the **Cell** with the [Value](value-property-ado-md.md) property.

- Zurückgeben der Zeichenfolge, die die formatierte **Value** -Eigenschaft darstellt, indem Sie die [FormattedValue](formattedvalue-property-ado-md.md)-Eigenschaft verwenden.

- Return the ordinal value of the **Cell** within the **Cellset** with the [Ordinal](ordinal-property-ado-md-cell.md) property.

- Determine the position of the **Cell** within the [CubeDef](cubedef-object-ado-md.md) with the [Positions](positions-collection-ado-md.md) collection.

- Retrieve other information about the **Cell** with the standard ADO [Properties](properties-collection-ado.md) collection.

Die **Properties**-Auflistung enthält Eigenschaften, die vom Anbieter bereitgestellt werden. In der folgenden Tabelle sind Eigenschaften aufgeführt, die möglicherweise verfügbar sind. Die tatsächliche Eigenschaftenliste kann je nach Anbieterimplementierung davon abweichen. Eine ausführlichere Liste mit verfügbaren Eigenschaften finden Sie in Ihrer Anbieterdokumentation.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Name</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>BackColor</p></td>
<td><p>Hintergrundfarbe, die beim Anzeigen der Zelle verwendet wird.</p></td>
</tr>
<tr class="even">
<td><p>Fontflags</p></td>
<td><p>Bitmaske für Schriftarteffekte.</p></td>
</tr>
<tr class="odd">
<td><p>FontName</p></td>
<td><p>Schriftart, die beim Anzeigen des Zellwerts verwendet wird.</p></td>
</tr>
<tr class="even">
<td><p>FontSize</p></td>
<td><p>Schriftgrad, der beim Anzeigen des Zellwerts verwendet wird.</p></td>
</tr>
<tr class="odd">
<td><p>ForeColor</p></td>
<td><p>Vordergrundfarbe, die beim Anzeigen der Zelle verwendet wird.</p></td>
</tr>
<tr class="even">
<td><p>FormatString</p></td>
<td><p>Wert in einer formatierten Zeichenfolge.</p></td>
</tr>
</tbody>
</table>

