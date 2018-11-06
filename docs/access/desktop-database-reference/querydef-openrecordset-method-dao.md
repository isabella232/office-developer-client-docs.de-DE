---
title: QueryDef.OpenRecordset-Methode (DAO)
TOCTitle: OpenRecordset Method
ms:assetid: b4908c36-c156-e269-e2ad-b1fa20ec4884
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822070(v=office.15)
ms:contentKeyID: 48547232
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b3948ba2bd8eb63176483a97942984823b9f45b0
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997147"
---
# <a name="querydefopenrecordset-method-dao"></a>QueryDef.OpenRecordset-Methode (DAO)

**Betrifft**: Access 2013, Office 2013

Erstellt ein neues **[Recordset](recordset-object-dao.md)** -Objekt und fügt es an die **Recordsets**-Auflistung an.

## <a name="syntax"></a>Syntax

*Ausdruck* . OpenRecordset (***Typ***, ***Optionen***, ***LockEdit***)

*Ausdruck* Eine Variable, die ein **QueryDef** -Objekt darstellt.

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
<th><p>Erforderlich oder optional</p></th>
<th><p>Datentyp</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Type</em></p></td>
<td><p>Optional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Eine <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong> -Konstante gibt den Typ des zu öffnenden <strong>Recordset</strong> an.</p><p><strong>Hinweis</strong>: Wenn Sie ein <STRONG>Recordset-Objekt</STRONG> in einer Microsoft Access-Arbeitsbereich öffnen, und Sie keinen Typ angeben, erstellt <STRONG>OpenRecordset</STRONG> eine vom Typ Tabelle <STRONG>Recordset</STRONG>, falls möglich. Wenn Sie einer verknüpften Tabelle oder Abfrage angeben, erstellt <STRONG>OpenRecordset</STRONG> ein vom Typ Dynaset- <STRONG>Recordset-Objekt</STRONG>.</p>
</td>
</tr>
<tr class="even">
<td><p><em>Options</em></p></td>
<td><p>Optional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Eine Kombination aus <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong> -Konstanten, die Merkmale des neuen <strong>Recordset</strong> angeben.</p></p><p><strong>Hinweis</strong>: die Konstanten <STRONG>DbConsistent</STRONG> und <STRONG>DbInconsistent</STRONG> schließen sich gegenseitig aus, und beide wird ein Fehler ausgegeben. Lockedits-Argument angeben, wenn <STRONG>beide</STRONG> Optionen verwendet, tritt ein Fehler auf.</p>
</td>
</tr>
<tr class="odd">
<td><p><em>LockEdit</em></p></td>
<td><p>Optional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Eine <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong> -Konstante, die die Sperre für das <strong>Recordset</strong> bestimmt.</p></p><p><strong>Hinweis</strong>: <STRONG>DbReadOnly</STRONG> Options-Argument oder das Argument sperren, jedoch nicht beide können. Wenn Sie für beide Argumente verwenden, tritt ein Laufzeitfehler auf.</p>
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
> Wenn *Quelle* bezieht eine SQL-Anweisung besteht aus einer Zeichenfolge mit einem nicht-Integer-Wert verkettet und die Systemparameter angeben einer US-decimal Zeichen wie etwa ein Komma (beispielsweise StrSQL = "PRICE &gt; " &amp; LngPrice, und LngPrice = 125,50), tritt ein Fehler auf, wenn Sie, zum Öffnen des **Recordset-Objekts versuchen**. Das geschieht, weil die Zahl während der Verkettung mithilfe des standardmäßigen Dezimalzeichens des Systems in eine Zeichenfolge konvertiert wird und SQL nur US-amerikanische Dezimalzeichen akzeptiert.


