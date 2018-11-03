---
title: Cell-Objekt (ADO MD)
TOCTitle: Cell object (ADO MD)
ms:assetid: b9d00b71-1f40-5bd1-4b89-fbdb59c552ba
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249892(v=office.15)
ms:contentKeyID: 48547356
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d1d34409b170f2747ee5652210379087015f83dc
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944083"
---
# <a name="cell-object-ado-md"></a>Cell-Objekt (ADO MD)


**Betrifft**: Access 2013, Office 2013

Stellt die Daten am Kreuzungspunkt von Achsenkoordinaten dar, die in einer Zellmenge enthalten sind.

## <a name="remarks"></a>Hinweise

Ein **Cell** -Objekt wird von der [Item](item-property-ado-md-cellset.md)-Eigenschaft eines [Cellset](cellset-object-ado-md.md)-Objekts zurückgegeben.

Die Auflistungen und Eigenschaften eines **Cell** -Objekts ermöglichen Folgendes:

- Zurückgeben der Daten in der**** Zelle, indem Sie die [Value](value-property-ado-md.md)-Eigenschaft verwenden.

- Zurückgeben der Zeichenfolge, die die formatierte **Value** -Eigenschaft darstellt, indem Sie die [FormattedValue](formattedvalue-property-ado-md.md)-Eigenschaft verwenden.

- Zurückgeben des Ordnungswerts der**** Zelle innerhalb der**** Zellmenge, indem Sie die [Ordinal](ordinal-property-ado-md-cell.md)-Eigenschaft verwenden.

- Bestimmen der Zellenposition**** innerhalb des [CubeDef](cubedef-object-ado-md.md)-Objekts, indem Sie die [Positions](positions-collection-ado-md.md)-Auflistung verwenden.

- Abrufen anderer Informationen zur**** Zelle, indem Sie die [Properties](properties-collection-ado.md)-ADO-Standardauflistung verwenden.

Die **Properties** -Auflistung enthält Eigenschaften, die vom Anbieter bereitgestellt werden. In der folgenden Tabelle sind Eigenschaften aufgeführt, die möglicherweise verfügbar sind. Die tatsächliche Eigenschaftenliste kann je nach Anbieterimplementierung davon abweichen. Eine ausführlichere Liste mit verfügbaren Eigenschaften finden Sie in Ihrer Anbieterdokumentation.

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
<td><p>FontFlags</p></td>
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

