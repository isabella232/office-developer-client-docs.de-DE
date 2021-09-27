---
title: QueryDef.OpenRecordset-Methode (DAO)
TOCTitle: OpenRecordset Method
ms:assetid: b4908c36-c156-e269-e2ad-b1fa20ec4884
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822070(v=office.15)
ms:contentKeyID: 48547232
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: high
ms.openlocfilehash: 54350b61c59c53f173b491b8f4724c8c1c14f004
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59589246"
---
# <a name="querydefopenrecordset-method-dao"></a>QueryDef.OpenRecordset-Methode (DAO)

**Gilt für**: Access 2013, Office 2013

Erstellt ein neues **[Recordset](recordset-object-dao.md)**-Objekt und fügt es an die **Recordsets**-Auflistung an.

## <a name="syntax"></a>Syntax

*expression* .OpenRecordset(***Type** _, _*_Options_*_, _*_LockEdit_**)

*Ausdruck* Eine Variable, die ein **QueryDef**-Objekt darstellt.

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
<td><p><em>Typ</em></p></td>
<td><p>Optional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Eine <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong>-Konstante gibt den Typ des zu öffnenden <strong>Recordset</strong> an.</p><p><strong>Hinweis</strong>: Wenn Sie ein <STRONG>Recordset</STRONG> in einem Microsoft Access-Arbeitsbereich öffnen und keinen Typ angeben, erstellt <STRONG>OpenRecordset</STRONG>, wenn möglich, ein tabellenartiges <STRONG>Recordset</STRONG>. If you specify a linked table or query, <STRONG>OpenRecordset</STRONG> creates a dynaset-type <STRONG>Recordset</STRONG>.</p>
</td>
</tr>
<tr class="even">
<td><p><em>Optionen</em></p></td>
<td><p>Optional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Eine Kombination aus <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong>-Konstanten, die Merkmale des neuen <strong>Recordset</strong> angeben.</p></p><p><strong>Hinweis</strong>: Die Konstanten <STRONG>dbConsistent</STRONG> und <STRONG>dbInconsistent</STRONG> schließen sich gegenseitig aus, und die Verwendung beider verursacht einen Fehler. Supplying a lockedits argument when options uses the <STRONG>dbReadOnly</STRONG> constant also causes an error.</p>
</td>
</tr>
<tr class="odd">
<td><p><em>LockEdit</em></p></td>
<td><p>Optional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Eine <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong>-Konstante, die die Sperre für das <strong>Recordset</strong> bestimmt.</p></p><p><strong>HINWEIS</strong>:Sie können <STRONG>dbReadOnly</STRONG> entweder im options-Argument oder im lockedits-Argument verwenden, aber nicht in beiden. Wenn Sie es für beide Argumente verwenden, tritt ein Laufzeitfehler auf.</p>
</td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>Rückgabewert

Recordset

## <a name="remarks"></a>Bemerkungen

Sie sollten die **[dbSeeChanges](recordsetoptionenum-enumeration-dao.md)** -Konstante auch dann verwenden, wenn Sie ein **Recordset** in einem mit einem Microsoft Access-Datenbankmodul verbundenen ODBC-Arbeitsbereich in einer Microsoft SQL Server 6.0-Tabelle (oder höher) öffnen, die über eine IDENTITY-Spalte verfügt. Andernfalls tritt ein Fehler auf.

Das Öffnen mehrerer **Recordset** -Objekte in einer ODBC-Datenquelle kann fehlschlagen, wenn die Verbindung durch einen vorherigen **OpenRecordset** -Aufruf ausgelastet ist. Das könnten Sie beispielsweise dadurch verhindern, dass Sie das **Recordset** -Objekt mithilfe der **[MoveLast](recordset-movelast-method-dao.md)** -Methode vollständig auffüllen, sobald das **Recordset** -Objekt geöffnet wird.

Beim Schließen eines **Recordset** -Objekts mit der **Close** -Methode wird es automatisch aus der **Recordsets** -Auflistung gelöscht.

> [!NOTE]
> Wenn sich *source* auf eine SQL-Anweisung bezieht, die aus einer Zeichenfolge besteht, die mit einem nicht ganzzahligen Wert verkettet ist, und die Systemparameter ein nicht für die USA gültiges Dezimalzeichen, z. B. ein Komma, angeben (Beispiel: strSQL = "PRICE &gt; " &amp; lngPrice, und lngPrice = 125,50), tritt beim Versuch, das **Recordset** zu öffnen, ein Fehler auf. Der Grund ist, dass die Zahl bei der Verkettung mithilfe des Standarddezimalzeichens des Systems in eine Zeichenfolge umgewandelt wird und SQL nur für die USA gültige Dezimalzeichen akzeptiert.


