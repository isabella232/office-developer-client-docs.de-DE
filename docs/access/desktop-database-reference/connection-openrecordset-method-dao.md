---
title: Connection.OpenRecordset-Methode (DAO)
TOCTitle: OpenRecordset Method
ms:assetid: 584a3e00-7589-90f1-aa6a-5d6116f0b5b6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194324(v=office.15)
ms:contentKeyID: 48544993
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: f8cdcd5313095992b9e3d0983dc1c6691ccb5e5f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59615777"
---
# <a name="connectionopenrecordset-method-dao"></a>Connection.OpenRecordset-Methode (DAO)

**Gilt für**: Access 2013, Office 2013

Erstellt ein neues **[Recordset](recordset-object-dao.md)**-Objekt und fügt es an die **Recordsets**-Auflistung an.

## <a name="syntax"></a>Syntax

*Ausdruck* . OpenRecordset(***Name** _, _*_Type_*_, _*_Options_*_, _*_LockEdit_**)

*Ausdruck* Eine Variable, die ein **Connection** -Objekt darstellt.

## <a name="parameters"></a>Parameter

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
<th><p>Erforderlich/optional</p></th>
<th><p>Datentyp</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Name</em></p></td>
<td><p>Erforderlich</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Die Quelle der Datensätze für das neue  <strong>Recordset</strong>. Die Quelle kann ein Tabellenname, ein Abfragename oder eine SQL-Anweisung sein, die Datensätze zurückgibt. Für <strong>Recordset</strong>-Objekte vom "table"-Typ in Microsoft Access-Datenbankmodul-Datenbanken kann die Quelle nur ein Tabellenname sein.</p></td>
</tr>
<tr class="even">
<td><p><em>Typ</em></p></td>
<td><p>Optional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Eine <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong>-Konstante gibt den Typ des zu öffnenden <strong>Recordset</strong> an.</p><p><strong>Hinweis</strong>: Wenn Sie ein <strong>Recordset</strong> in einem Microsoft Access-Arbeitsbereich öffnen und keinen Typ angeben, erstellt <strong>OpenRecordset</strong>, wenn möglich, ein tabellenartiges <strong>Recordset</strong>. If you specify a linked table or query, <strong>OpenRecordset</strong> creates a dynaset-type <strong>Recordset</strong>.</p>
</td>
</tr>
<tr class="odd">
<td><p><em>Optionen</em></p></td>
<td><p>Optional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Eine Kombination aus <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong>-Konstanten, die Merkmale des neuen <strong>Recordset</strong> angeben.</p><p><strong>Hinweis</strong>: Die Konstanten <strong>dbConsistent</strong> und <strong>dbInconsistent</strong>schließen sich gegenseitig aus, und die Verwendung beider verursacht einen Fehler. Wenn Sie ein lockedits-Argument angeben, wenn Optionen die <strong>dbReadOnly</strong> -Konstante verwenden, tritt ebenfalls ein Fehler auf.</p>
</td>
</tr>
<tr class="even">
<td><p><em>LockEdit</em></p></td>
<td><p>Optional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Eine <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong>-Konstante, die die Sperre für das <strong>Recordset</strong> bestimmt.</p><p><strong>HINWEIS</strong>:Sie können <strong>dbReadOnly</strong> entweder im options-Argument oder im lockedits-Argument verwenden, aber nicht in beiden. Wenn Sie es für beide Argumente verwenden, tritt ein Laufzeitfehler auf.</p>
</td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>Rückgabewert

Recordset

## <a name="remarks"></a>Hinweise

Wenn der Benutzer diesen Fehler beim Aktualisieren eines Datensatzes erhält, sollte Ihr Code normalerweise die Inhalte der Felder aktualisieren und die neu geänderten Werte abrufen. Wenn der Fehler beim Löschen eines Datensatzes auftritt, könnte Ihr Code dem Benutzer die neuen Datensatzdaten und eine Meldung anzeigen, dass die Daten kürzlich geändert wurden. An diesem Punkt kann Ihr Code eine Bestätigung anfordern, dass der Benutzer den Datensatz immer noch löschen möchte.

Sie sollten auch die **dbSeeChanges**-Konstante verwenden, wenn Sie ein **Recordset** in einem ODBC-Arbeitsbereich mit verbundenem Microsoft Access-Datenbankmodul für eine Microsoft SQL Server 6.0-Tabelle (oder neuer) öffnen, die über eine  IDENTITY-Spalte verfügt. Andernfalls kann ein Fehler auftreten.

Wenn Sie mehr als ein **Recordset** in einer ODBC-Datenquelle öffnen, kann die Datenquelle ausfallen, da die Verbindung mit einem vorherigen **OpenRecordset**-Aufruf beschäftigt ist. Eine Lösungsmöglichkeit besteht im vollständigen Ausfüllen des **Recordset** mithilfe der **MoveLast**-Methode, sobald das **Recordset** geöffnet wird.

Durch das Schließen eines **Recordset** mit der **[Close](connection-close-method-dao.md)**-Methode wird es automatisch aus der **Recordsets**-Auflistung gelöscht.

> [!NOTE]
> Wenn sich *source* auf eine SQL-Anweisung bezieht, die aus einer Zeichenfolge besteht, die mit einem nicht ganzzahligen Wert verkettet ist, und die Systemparameter ein nicht für die USA gültiges Dezimalzeichen, z. B. ein Komma, angeben (Beispiel: strSQL = "PRICE &gt; " &amp; lngPrice, und lngPrice = 125,50), tritt beim Versuch, das **Recordset** zu öffnen, ein Fehler auf. Der Grund ist, dass die Zahl bei der Verkettung mithilfe des Standarddezimalzeichens des Systems in eine Zeichenfolge umgewandelt wird und SQL nur für die USA gültige Dezimalzeichen akzeptiert.


