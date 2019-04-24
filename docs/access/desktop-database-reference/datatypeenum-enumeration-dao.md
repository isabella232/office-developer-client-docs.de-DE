---
title: DataTypeEnum-Aufzählung (DAO)
TOCTitle: DataTypeEnum Enumeration
ms:assetid: 59ead483-52fc-53cd-02e6-084814f961ac
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194420(v=office.15)
ms:contentKeyID: 48545028
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 499513d706b254e72433d37d4eb5452ccbbaa257
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294449"
---
# <a name="datatypeenum-enumeration-dao"></a>DataTypeEnum-Aufzählung (DAO)


**Gilt für**: Access 2013, Office 2013

Gibt den Datentyp eines Objekts an.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Name</p></th>
<th><p>Wert</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>dbAttachment</p></td>
<td><p>101</p></td>
<td><p>Anlagedaten</p></td>
</tr>
<tr class="even">
<td><p>dbBigInt</p></td>
<td><p>16</p></td>
<td><p>Grosse Ganzzahldaten</p></td>
</tr>
<tr class="odd">
<td><p>dbBinary</p></td>
<td><p>9</p></td>
<td><p>Binärdaten</p></td>
</tr>
<tr class="even">
<td><p>dbBoolean</p></td>
<td><p>1</p></td>
<td><p>Boolesche Daten (True/False)</p></td>
</tr>
<tr class="odd">
<td><p>dbByte</p></td>
<td><p>2</p></td>
<td><p>Bytedaten (8-Bit)</p></td>
</tr>
<tr class="even">
<td><p>dbChar</p></td>
<td><p>18</p></td>
<td><p>Textdaten (feste Breite)</p></td>
</tr>
<tr class="odd">
<td><p>dbComplexByte</p></td>
<td><p>102</p></td>
<td><p>Mehrfachwert-Bytedaten</p></td>
</tr>
<tr class="even">
<td><p>dbComplexDecimal</p></td>
<td><p>108</p></td>
<td><p>Mehrfachwert-Dezimaldaten</p></td>
</tr>
<tr class="odd">
<td><p>dbComplexDouble</p></td>
<td><p>106</p></td>
<td><p>Mehrfachwert-Gleitkommadaten mit doppelter Genauigkeit</p></td>
</tr>
<tr class="even">
<td><p>dbComplexGUID</p></td>
<td><p>107</p></td>
<td><p>Mehrfachwert-GUID-Daten</p></td>
</tr>
<tr class="odd">
<td><p>dbComplexInteger</p></td>
<td><p>103</p></td>
<td><p>Ganzzahlige Mehrfachwertdaten</p></td>
</tr>
<tr class="even">
<td><p>dbComplexLong</p></td>
<td><p>104</p></td>
<td><p>Lange ganzzahlige Mehrfachwertdaten</p></td>
</tr>
<tr class="odd">
<td><p>dbComplexSingle</p></td>
<td><p>105</p></td>
<td><p>Mehrfachwert-Gleitkommadaten mit einfacher Genauigkeit</p></td>
</tr>
<tr class="even">
<td><p>dbComplexText</p></td>
<td><p>109</p></td>
<td><p>Mehrfachwert-Textdaten (variable Breite)</p></td>
</tr>
<tr class="odd">
<td><p>dbCurrency</p></td>
<td><p>5</p></td>
<td><p>Währungsdaten</p></td>
</tr>
<tr class="even">
<td><p>dbDate</p></td>
<td><p>8</p></td>
<td><p>Datumswertdaten</p></td>
</tr>
<tr class="odd">
<td><p>dbDecimal</p></td>
<td><p>20</p></td>
<td><p>Dezimaldaten (nur ODBCDirect)</p><p><strong>HINWEIS</strong>: ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt. Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul zu verwenden.</p>
</td>
</tr>
<tr class="even">
<td><p>dbDouble</p></td>
<td><p>7</p></td>
<td><p>Gleitkommadaten mit doppelter Genauigkeit</p></td>
</tr>
<tr class="odd">
<td><p>dbFloat</p></td>
<td><p>21</p></td>
<td><p>Gleitkommadaten (nur ODBCDirect)</p>

<br/>


</td>
</tr>
<tr class="even">
<td><p>dbGUID</p></td>
<td><p>15</p></td>
<td><p>GUID-Daten</p></td>
</tr>
<tr class="odd">
<td><p>dbInteger</p></td>
<td><p>3</p></td>
<td><p>Ganzzahlige Daten</p></td>
</tr>
<tr class="even">
<td><p>dbLong</p></td>
<td><p>4</p></td>
<td><p>Lange ganzzahlige Daten</p></td>
</tr>
<tr class="odd">
<td><p>dbLongBinary</p></td>
<td><p>11</p></td>
<td><p>Binärdaten (Bitmap)</p></td>
</tr>
<tr class="even">
<td><p>dbMemo</p></td>
<td><p>12</p></td>
<td><p>Memodaten (erweiterter Text)</p></td>
</tr>
<tr class="odd">
<td><p>dbNumeric</p></td>
<td><p>19</p></td>
<td><p>Numerische Daten (nur ODBCDirect)</p>

<br/>


</td>
</tr>
<tr class="even">
<td><p>dbSingle</p></td>
<td><p>6</p></td>
<td><p>Gleitkommadaten mit einfacher Genauigkeit</p></td>
</tr>
<tr class="odd">
<td><p>dbText</p></td>
<td><p>10</p></td>
<td><p>Textdaten (variable Breite)</p></td>
</tr>
<tr class="even">
<td><p>dbTime</p></td>
<td><p>22</p></td>
<td><p>Daten im Zeitformat (nur ODBCDirect)</p>

<br/>


</td>
</tr>
<tr class="odd">
<td><p>dbTimeStamp</p></td>
<td><p>23</p></td>
<td><p>Daten im Zeit- und Datumsformat (nur ODBCDirect)</p>

<br/>


</td>
</tr>
<tr class="even">
<td><p>dbVarBinary</p></td>
<td><p>17</p></td>
<td><p>Variable Binärdaten (nur ODBCDirect)</p>

<br/>


</td>
</tr>
</tbody>
</table>

