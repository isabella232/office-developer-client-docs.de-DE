---
title: TableDef.OpenRecordset Method (DAO)
TOCTitle: OpenRecordset Method
ms:assetid: f4c9c89c-3348-d3c9-ce76-dd11e5ee11a7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836703(v=office.15)
ms:contentKeyID: 48548696
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d7b9b6ccac186f87d0a22a4a55108594cfc55ac9
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473782"
---
# <a name="tabledefopenrecordset-method-dao"></a>TableDef.OpenRecordset Method (DAO)


**Betrifft**: Access 2013 | Office 2013

Erstellt ein neues **[Recordset](recordset-object-dao.md)** -Objekt und fügt es an die **Recordsets**-Auflistung an.

## <a name="syntax"></a>Syntax

*Ausdruck* . OpenRecordset ("***Typ***", " ***Optionen***")

*Ausdruck* Eine Variable, die ein **TableDef** -Objekt darstellt.

### <a name="parameters"></a>Parameter

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Name</p></th>
<th><p>Erforderlich/Optional</p></th>
<th><p>Datentyp</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Name</p></td>
<td><p>Erforderlich</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Die Quelle der Datensätze für das neue <strong>Recordset</strong>. Die Quelle kann ein Tabellenname, ein Abfragename oder eine SQL-Anweisung sein, die Datensätze zurückgibt. Für <strong>Recordset</strong> -Objekte vom "table"-Typ in Microsoft Access-Datenbankmodul-Datenbanken kann die Quelle nur ein Tabellenname sein.  </p></td>
</tr>
<tr class="even">
<td><p>Typ</p></td>
<td><p>Optional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Eine <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong> -Konstante gibt den Typ des zu öffnenden <strong>Recordset</strong> an.</p>

> [!NOTE]
> <P>Wenn Sie ein <STRONG>Recordset</STRONG> in einem Microsoft Access-Arbeitsbereich öffnen und keinen Typ angeben, erstellt <STRONG>OpenRecordset</STRONG>, wenn möglich, ein <STRONG>Recordset</STRONG> vom "table"-Typ. Wenn sie eine verknüpfte Tabelle oder Abfrage angeben, erstellt <STRONG>OpenRecordset</STRONG> ein <STRONG>Recordset</STRONG> vom "dynaset"-Typ.</P>


</td>
</tr>
<tr class="odd">
<td><p>Options</p></td>
<td><p>Optional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Eine Kombination aus <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong> -Konstanten, die Merkmale des neuen <strong>Recordset</strong> angeben.</p>

> [!NOTE]
> <P>Die Konstanten <STRONG>dbConsistent</STRONG> und <STRONG>dbInconsistent</STRONG> schließen sich gegenseitig aus, und die Verwendung beider verursacht einen Fehler. Wenn in Options die <STRONG>dbReadOnly</STRONG>-Konstante verwendet wird, führt die Angabe eines lockedits-Arguments ebenfalls zu einem Fehler.</P>


</td>
</tr>
<tr class="even">
<td><p>LockEdit</p></td>
<td><p>Optional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Eine <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong> -Konstante, die die Sperre für das <strong>Recordset</strong> bestimmt.</p>

> [!NOTE]
> <P>Sie können <STRONG>dbReadOnly</STRONG> entweder im options-Argument oder im lockedits-Argument verwenden, aber nicht in beiden. Wenn Sie es für beide Argumente verwenden, tritt ein Laufzeitfehler auf.</P>


</td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Rückgabewert

Recordset

## <a name="remarks"></a>Hinweise

Wenn der Benutzer beim Aktualisieren eines Datensatzes diesen Fehler erhält, sollte der Code den Inhalt des Felds aktualisieren und die geänderten Werte abrufen. Tritt der Fehler beim Löschen eines Datensatzes auf, sollte der Code die Daten des neuen Datensatzes anzeigen und eine Meldung darüber ausgeben, dass die Daten kürzlich geändert wurden. An dieser Stelle könnte der Code bestätigen lassen, dass der Benutzer den Datensatz wirklich löschen möchte.

Sie sollten die **dbSeeChanges**-Konstante auch dann verwenden, wenn Sie ein **Recordset** in einem mit einem Microsoft Access-Datenbankmodul verbundenen ODBC-Arbeitsbereich in einer Microsoft SQL Server 6.0-Tabelle (oder höher) öffnen, die über eine IDENTITY-Spalte verfügt. Andernfalls tritt ein Fehler auf.

Das Öffnen mehrerer **Recordset**-Objekte in einer ODBC-Datenquelle kann fehlschlagen, wenn die Verbindung durch einen vorherigen **OpenRecordset**-Aufruf ausgelastet ist. Das könnten Sie beispielsweise dadurch verhindern, dass Sie das **Recordset**-Objekt mithilfe der **MoveLast**-Methode vollständig auffüllen, sobald das **Recordset**-Objekt geöffnet wird.

Beim Schließen eines **Recordset**-Objekts mit der **[Close](connection-close-method-dao.md)** -Methode wird es automatisch aus der **Recordsets**-Auflistung gelöscht.


> [!NOTE]
> <P>Wenn <EM>Quelle</EM> bezieht eine SQL-Anweisung besteht aus einer Zeichenfolge mit einem nicht-Integer-Wert verkettet und die Systemparameter angeben einer US-decimal Zeichen wie etwa ein Komma (beispielsweise StrSQL = "PRICE &gt; " &amp; LngPrice, und LngPrice = 125,50), tritt ein Fehler auf, wenn Sie, zum Öffnen des <STRONG>Recordset-Objekts versuchen</STRONG>. Das geschieht, weil die Zahl während der Verkettung mithilfe des standardmäßigen Dezimalzeichens des Systems in eine Zeichenfolge konvertiert wird und SQL nur US-amerikanische Dezimalzeichen akzeptiert.</P>


