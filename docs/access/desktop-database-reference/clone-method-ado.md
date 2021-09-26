---
title: Clone-Methode – ActiveX Data Objects (ADO)
TOCTitle: Clone method (ADO)
ms:assetid: ca9b2b76-90bf-9a60-2611-3cb4977d5591
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249984(v=office.15)
ms:contentKeyID: 48547693
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: ec081c42a219e7073041998826b533a1b0fa6c81
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59627079"
---
# <a name="clone-method-ado"></a>Clone-Methode (ADO)

**Gilt für**: Access 2013, Office 2013

Ein [Recordset](recordset-object-ado.md)-Objektduplikat wird aus einem vorhandenen **Recordset** -Objekt erstellt. Optional wird angegeben, dass der Klon schreibgeschützt ist.

## <a name="syntax"></a>Syntax

**Set** *rstDuplicate*  =  *rstOriginal*. Clone (*LockType*)

## <a name="return-value"></a>Rückgabewert

Ein **Recordset**-Objektverweis wird zurückgegeben.

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*rstDuplicate* |Eine Objektvariable, durch die das zu erstellende **Recordset** -Objektduplikat identifiziert wird.|
|*rstOriginal* |Eine Objektvariable, durch die das zu duplizierende **Recordset** -Objekt identifiziert wird.|
|*LockType* |Optional. Ein [LockTypeEnum](locktypeenum.md)-Wert, durch den der Sperrtyp des Original **recordsets** oder ein schreibgeschütztes **Recordset** angegeben wird. Gültige Werte sind **adLockUnspecified** oder **adLockReadOnly**.|

## <a name="remarks"></a>Bemerkungen

Verwenden Sie die **Clone** -Methode zum Erstellen mehrerer **Recordset** -Objektduplikate, insbesondere, wenn Sie mehrere aktuelle Datensätze in einem bestimmten Satz mit Datensätzen aufrechterhalten möchten. Das Verwenden der **Clone** -Methode ist effizienter als das Erstellen und Öffnen eines neuen **Recordset** -Objekts mit der gleichen Definition wie das Original.

Die [Filter](filter-property-ado.md)-Eigenschaft des Original **recordsets**, falls vorhanden, wird nicht auf den Klon angewendet. Legen Sie die **Filter** -Eigenschaft des neuen **Recordsets** fest, um die Ergebnisse zu filtern. Die einfachste Möglichkeit zum Kopieren vorhandener **Filter** -Werte ist das direkte Zuweisen:

Der aktuelle Datensatz eines neu erstellten Klons wird auf den ersten Datensatz festgelegt.

An einem **Recordset** -Objekt vorgenommene Änderungen werden unabhängig vom Cursortyp in allen Klonen des Objekts angezeigt. Nach dem Ausführen von [Requery](requery-method-ado.md) für das ursprüngliche **Recordset** -Objekt werden die Klone jedoch nicht mehr mit dem Original synchronisiert.

Durch das Schließen des Original **recordsets** werden die Kopien nicht geschlossen, und durch das Schließen einer Kopie werden das Original oder andere Kopien nicht geschlossen.

Sie können nur **Recordset** -Objekte klonen, von denen Textmarken unterstützt werden. Textmarkenwerte sind austauschbar; d. h., ein Textmarkenverweis eines **Recordset** -Objekts verweist auf den gleichen Datensatz in den Klonen.

Einige ausgelöste **Recordset** -Ereignisse werden auch in allen **Recordset** klonen ausgeführt. Die Ereignisse sind für den Klon jedoch möglicherweise nicht gültig, da sich der aktuelle Datensatz zwischen geklonten **Recordsets** unterscheiden kann.

Wenn Sie z. B. einen Wert eines Felds ändern, tritt im geänderten **Recordset** und in allen Klonen ein [WillChangeField](willchangefield-and-fieldchangecomplete-events-ado.md)-Ereignis auf. Durch den *Fields*-Parameter des **WillChangeField**-Ereignisses eines geklonten **Recordsets** (in dem die Änderung nicht vorgenommen wurde) wird einfach auf die Felder des aktuellen Datensatzes des Klons verwiesen, der ein anderer Datensatz sein kann als der aktuelle Datensatz des Original **recordsets**, in dem die Änderung auftrat.

In der folgenden Tabelle wird eine vollständige Liste aller **Recordset**-Ereignisse bereitgestellt, und es wird angegeben, ob sie gültig sind und für mit der **Clone**-Methode generierte Recordsetklone ausgelöst werden.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Ereignis</p></th>
<th><p>Auslösung in Klonen</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="endofrecordset-event-ado.md">EndOfRecordset</a></p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p><a href="fetchcomplete-event-ado.md">FetchComplete</a></p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p><a href="fetchprogress-event-ado.md">FetchProgress</a></p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p><a href="willchangefield-and-fieldchangecomplete-events-ado.md">FieldChangeComplete</a></p></td>
<td><p>Ja</p></td>
</tr>
<tr class="odd">
<td><p><a href="willmove-and-movecomplete-events-ado.md">MoveComplete</a></p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p><a href="willchangerecord-and-recordchangecomplete-events-ado.md">RecordChangeComplete</a></p></td>
<td><p>Ja</p></td>
</tr>
<tr class="odd">
<td><p><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">RecordsetChangeComplete</a></p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p><a href="willchangefield-and-fieldchangecomplete-events-ado.md">WillChangeField</a></p></td>
<td><p>Ja</p></td>
</tr>
<tr class="odd">
<td><p><a href="willchangerecord-and-recordchangecomplete-events-ado.md">WillChangeRecord</a></p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">WillChangeRecordset</a></p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p><a href="willmove-and-movecomplete-events-ado.md">WillMove</a></p></td>
<td><p>Nein</p></td>
</tr>
</tbody>
</table>

