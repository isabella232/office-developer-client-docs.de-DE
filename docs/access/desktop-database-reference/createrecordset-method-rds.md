---
title: CreateRecordset-Methode (RDS)
TOCTitle: CreateRecordset method (RDS)
ms:assetid: 19524509-31da-9af1-4062-cd3c59b51278
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248940(v=office.15)
ms:contentKeyID: 48543497
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3dda0840617c32e9dceea3bd1baa362c5652a373
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295338"
---
# <a name="createrecordset-method-rds"></a>CreateRecordset-Methode (RDS)

**Gilt für**: Access 2013, Office 2013

Erstellt ein leeres, getrenntes [Recordset](recordset-object-ado.md)-Objekt.

## <a name="syntax"></a>Syntax

- *Objekt*. CreateRecordset (*ColumnInfos*)

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*Object* |Eine Objektvariable, die ein [RDSServer.DataFactory](datafactory-object-rdsserver.md)- oder [RDS.DataControl](datacontrol-object-rds.md)-Objekt darstellt.|
|*ColumnsInfos* |Ein **Variant** -Array mit Attributen, das alle Spalten im erstellten **Recordset** -Objekt definiert. Jede Spaltendefinition enthält ein Array mit vier erforderlichen Attributen und einem optionalen Attribut. Der Satz der Spaltenarrays wird anschließend in einem Array gruppiert, das das **Recordset** -Objekt angibt. Eine Liste der Attribute finden Sie in der folgenden Tabelle.|

### <a name="variant-array-attributes"></a>Variant-Array Attribute

|Attribut|Beschreibung|
|:--------|:----------|
|Name |Bezeichnung des Spaltenkopfs|
|Typ |Ganzzahl des Datentyps.|
|Größe |Ganzzahl der Breite in Zeichen, unabhängig vom Datentyp.|
|Zulässigkeit |Boolescher Wert.|
|Skalierung (optional) |Dieses optionale Attribut definiert die Dezimalstellen von numerischen Feldern. Ist dieser Wert nicht angegeben, werden numerische Werte auf drei Dezimalstellen beschränkt. Dies wirkt sich nicht auf die Genauigkeit aus, die Anzahl der Ziffern nach dem Dezimaltrennzeichen ist jedoch auf drei Stellen beschränkt.|

## <a name="remarks"></a>Bemerkungen

Das serverseitige Geschäftsobjekt kann das resultierende **Recordset**-Objekt mit Daten von einem Nicht-OLE DB-Datenanbieter wie einer Betriebssystemdatei, die Bestandsquoten enthält, auffüllen.

In der folgenden Liste sind die [DataTypeEnum](datatypeenum.md)-Werte aufgeführt, die von der **CreateRecordset** -Methode unterstützt werden. Bei der angegebenen Zahl handelt es sich um die Referenznummer, die zum Definieren von Feldern verwendet wird.

Die einzelnen Datentypen haben entweder eine feste oder eine variable Länge. Bei Typen mit fester Länge sollte die Größe auf den Wert -1 festgelegt werden, da die Größe vorher festgelegt werden muss und eine Definition der Größe noch erforderlich ist. Bei Datentypen mit variabler Länge ist eine Größe zwischen 1 und 32767 zulässig.

For some of the variable data types, the type may be coerced to the type noted in the Substitution column. You won't see the substitutions until after the **Recordset** is created and filled. Then you can check for the actual data type, if necessary.

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Länge</p></th>
<th><p>Konstante</p></th>
<th><p>Zahl</p></th>
<th><p>Ersetzung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Fest</p></td>
<td><p><strong>addTinyInt</strong></p></td>
<td><p>16</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Fest</p></td>
<td><p><strong>SmallInt</strong></p></td>
<td><p>2</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Fest</p></td>
<td><p><strong>Ganzzahl</strong></p></td>
<td><p>3</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Fest</p></td>
<td><p><strong>Bigint</strong></p></td>
<td><p>20</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Fest</p></td>
<td><p><strong>adUnsignedTinyInt</strong></p></td>
<td><p>17</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Fest</p></td>
<td><p><strong>adUnsignedSmallInt</strong></p></td>
<td><p>18</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Fest</p></td>
<td><p><strong>adUnsignedInt</strong></p></td>
<td><p>19</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Fest</p></td>
<td><p><strong>adUnsignedBigInt</strong></p></td>
<td><p>21</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Fest</p></td>
<td><p><strong>Einzel</strong></p></td>
<td><p>4</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Fest</p></td>
<td><p><strong>adDouble</strong></p></td>
<td><p>5</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Fest</p></td>
<td><p><strong>Währung</strong></p></td>
<td><p>6</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Fest</p></td>
<td><p><strong>adDecimal</strong></p></td>
<td><p>14</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Fest</p></td>
<td><p><strong>adNumeric</strong></p></td>
<td><p>131</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Fest</p></td>
<td><p><strong>Boolean</strong></p></td>
<td><p>11</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Fest</p></td>
<td><p><strong>Fehler</strong></p></td>
<td><p>10</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Fest</p></td>
<td><p><strong>GUID</strong></p></td>
<td><p>72</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Fest</p></td>
<td><p><strong>Datum</strong></p></td>
<td><p>7</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Fest</p></td>
<td><p><strong>adDBDate</strong></p></td>
<td><p>133</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Fest</p></td>
<td><p><strong>adDBTime</strong></p></td>
<td><p>134</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Fest</p></td>
<td><p><strong>adDBTimestamp</strong></p></td>
<td><p>135</p></td>
<td><p>7</p></td>
</tr>
<tr class="odd">
<td><p>Variable</p></td>
<td><p><strong>-BSTR</strong></p></td>
<td><p>8</p></td>
<td><p>130</p></td>
</tr>
<tr class="even">
<td><p>Variable</p></td>
<td><p><strong>Char</strong></p></td>
<td><p>129</p></td>
<td><p>200</p></td>
</tr>
<tr class="odd">
<td><p>Variable</p></td>
<td><p><strong>-VarChar</strong></p></td>
<td><p>200</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Variable</p></td>
<td><p><strong>adLongVarChar</strong></p></td>
<td><p>201</p></td>
<td><p>200</p></td>
</tr>
<tr class="odd">
<td><p>Variable</p></td>
<td><p><strong>adWChar</strong></p></td>
<td><p>130</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Variable</p></td>
<td><p><strong>adVarWChar</strong></p></td>
<td><p>202</p></td>
<td><p>130</p></td>
</tr>
<tr class="odd">
<td><p>Variable</p></td>
<td><p><strong>adLongVarWChar</strong></p></td>
<td><p>203</p></td>
<td><p>130</p></td>
</tr>
<tr class="even">
<td><p>Variable</p></td>
<td><p><strong>die Binärdatei</strong></p></td>
<td><p>128</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Variable</p></td>
<td><p><strong>VarBinary</strong></p></td>
<td><p>204</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Variable</p></td>
<td><p><strong>adLongVarBinary</strong></p></td>
<td><p>205</p></td>
<td><p>204</p></td>
</tr>
</tbody>
</table>

