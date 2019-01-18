---
title: Field2.Type-Eigenschaft (DAO)
TOCTitle: Type Property
ms:assetid: 057d6ec9-b72c-cee6-005a-6d916e3dda29
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844921(v=office.15)
ms:contentKeyID: 48543032
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4da32f18a2b3e9dddbb0ae04e3257de34ba09761
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699786"
---
# <a name="field2type-property-dao"></a>Field2.Type-Eigenschaft (DAO)


**Betrifft**: Access 2013, Office 2013

Legt einen Wert fest, der den Funktions- oder Datentyp eines Objekts angibt, oder gibt einen solchen Wert zurück. Lese-/Schreibzugriff **Integer**.

## <a name="syntax"></a>Syntax

*Ausdruck* . Typ

*Ausdruck* Eine Variable, die ein **Field2** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Die Einstellung oder der Rückgabewert ist eine Konstante, die den Funktions- oder Datentyp angibt. Bei einem **Field2**-Objekt besteht für diese Eigenschaft Lese-/Schreibzugriff, bis das Objekt einer Auflistung oder einem andern Objekt angefügt wird. Dann ist sie schreibgeschützt.

Die möglichen Einstellungen und Rückgabewerte bei einem **Field2**-Objekt werden in der folgenden Tabelle aufgeführt.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Konstante</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>dbBigInt</strong></p></td>
<td><p>Große Ganzzahl</p></td>
</tr>
<tr class="even">
<td><p><strong>dbBinary</strong></p></td>
<td><p>Binär</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbBoolean</strong></p></td>
<td><p>Boolescher Wert</p></td>
</tr>
<tr class="even">
<td><p><strong>dbByte</strong></p></td>
<td><p>Byte</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbChar</strong></p></td>
<td><p>Zeichen</p></td>
</tr>
<tr class="even">
<td><p><strong>dbCurrency</strong></p></td>
<td><p>Währung</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbDate</strong></p></td>
<td><p>Datum/Uhrzeit</p></td>
</tr>
<tr class="even">
<td><p><strong>dbDecimal</strong></p></td>
<td><p>Dezimal</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbDouble</strong></p></td>
<td><p>Double</p></td>
</tr>
<tr class="even">
<td><p><strong>dbFloat</strong></p></td>
<td><p>Gleitkomma</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbGUID</strong></p></td>
<td><p>GUID</p></td>
</tr>
<tr class="even">
<td><p><strong>dbInteger</strong></p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLong</strong></p></td>
<td><p>Long</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLongBinary</strong></p></td>
<td><p>Langer Binärwert (OLE-Objekt)</p></td>
</tr>
<tr class="odd">
<td><p><strong>Wert dbMemo</strong></p></td>
<td><p>Memo</p></td>
</tr>
<tr class="even">
<td><p><strong>dbNumeric</strong></p></td>
<td><p>Numerisch</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbSingle</strong></p></td>
<td><p>Single</p></td>
</tr>
<tr class="even">
<td><p><strong>dbText</strong></p></td>
<td><p>Text</p></td>
</tr>
<tr class="odd">
<td><p><strong>Zeitpunkt</strong></p></td>
<td><p>Zeit</p></td>
</tr>
<tr class="even">
<td><p><strong>dbTimeStamp</strong></p></td>
<td><p>Zeitstempel</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbVarBinary</strong></p></td>
<td><p>VarBinary</p></td>
</tr>
</tbody>
</table>


Beim Anfügen eines neuen **Field2**-, **Parameter**- oder **Property**-Objekts zur Auflistung eines **Index**-, **QueryDef**-, **Recordset**- oder **TableDef**-Objekts tritt ein Fehler auf, wenn die zugrunde liegende Tabelle den für das neue Objekt angegebenen Datentyp nicht unterstützt.

