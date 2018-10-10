---
title: DataTypeEnum (Access PC-Datenbank-Referenz)
TOCTitle: DataTypeEnum
ms:assetid: a8ab7616-552f-ed5f-ed55-95254cfb374a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249780(v=office.15)
ms:contentKeyID: 48546904
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e8b70ad0067083373679286bdb452cb667d3de0e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475331"
---
# <a name="datatypeenum"></a>DataTypeEnum


**Betrifft**: Access 2013 | Office 2013

Gibt den Datentyp eines [Felds](field-object-ado.md), eines [Parameters](parameter-object-ado.md) oder einer [Eigenschaft](property-object-ado.md) an. Der entsprechende OLE DB-Typindikator wird in der Beschreibungsspalte der folgenden Tabelle in Klammern angezeigt. Weitere Informationen zu OLE DB-Datentypen finden Sie in Kapitel 13 und in Anhang A der *OLE DB Programmer's Reference*.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Konstante</p></th>
<th><p>Wert</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>AdArray<br />
</strong>(Gilt nicht für ADOX.)</p></td>
<td><p>0 x 2000</p></td>
<td><p>Ein Flagwert, immer kombiniert mit einer anderen Datentypkonstante, die einen Array dieses anderen Datentyps angibt.</p></td>
</tr>
<tr class="even">
<td><p><strong>adBigInt</strong></p></td>
<td><p>20</p></td>
<td><p>Gibt eine ganze Zahl mit Vorzeichen und einer Länge von 8 Bytes an (DBTYPE_I8).</p></td>
</tr>
<tr class="odd">
<td><p><strong>adBinary</strong></p></td>
<td><p>128</p></td>
<td><p>Gibt einen Binärwert an (DBTYPE_BYTES).</p></td>
</tr>
<tr class="even">
<td><p><strong>adBoolean</strong></p></td>
<td><p>11</p></td>
<td><p>Gibt einen booleschen Wert an (DBTYPE_BOOL).</p></td>
</tr>
<tr class="odd">
<td><p><strong>adBSTR</strong></p></td>
<td><p>8</p></td>
<td><p>Gibt eine mit Null endende Zeichenfolge (Unicode) an (DBTYPE_BSTR).</p></td>
</tr>
<tr class="even">
<td><p><strong>adChapter</strong></p></td>
<td><p>136</p></td>
<td><p>Gibt einen Kapitelwert mit 4 Bytes an, der Zeilen in einem untergeordneten Rowset (DBTYPE_HCHAPTER) kennzeichnet.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adChar</strong></p></td>
<td><p>129</p></td>
<td><p>Gibt einen Zeichenfolgenwert an (DBTYPE_STR).</p></td>
</tr>
<tr class="even">
<td><p><strong>adCurrency</strong></p></td>
<td><p>6</p></td>
<td><p>Gibt einen Währungswert an (DBTYPE_CY). Die Währung ist eine Festkommazahl mit vier Ziffern rechts vom Dezimalkomma. Sie ist in einer ganzen Zahl mit Vorzeichen und einer Länge von 8 Bytes gespeichert, die um 10.000 skaliert wird.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adDate</strong></p></td>
<td><p>7</p></td>
<td><p>Gibt einen Datumswert an (DBTYPE_DATE). Ein Datum wird als Double gespeichert, wobei der ganze Teil davon die Zahl der Tage seit dem 30. Dezember 1899 und der Bruchteil davon den Teil des Tages darstellt.</p></td>
</tr>
<tr class="even">
<td><p><strong>adDBDate</strong></p></td>
<td><p>133</p></td>
<td><p>Gibt einen Datumswert (jjjjmmtt) an (DBTYPE_DBDATE).</p></td>
</tr>
<tr class="odd">
<td><p><strong>adDBTime</strong></p></td>
<td><p>134</p></td>
<td><p>Gibt einen Zeitwert (hhmmss) an (DBTYPE_DBTIME).</p></td>
</tr>
<tr class="even">
<td><p><strong>adDBTimeStamp</strong></p></td>
<td><p>135</p></td>
<td><p>Gibt einen Datums-/Uhrzeitstempel (jjjjmmtthhmmss plus einen Bruchteil in Milliardstel) an (DBTYPE_DBTIMESTAMP).</p></td>
</tr>
<tr class="odd">
<td><p><strong>adDecimal</strong></p></td>
<td><p>14</p></td>
<td><p>Gibt einen genauen numerischen Wert mit einer festen Genauigkeit und einem festen Maßstab an (DBTYPE_DECIMAL).</p></td>
</tr>
<tr class="even">
<td><p><strong>adDouble</strong></p></td>
<td><p>5</p></td>
<td><p>Gibt einen Gleitkommawert mit doppelter Genauigkeit an (DBTYPE_R8).</p></td>
</tr>
<tr class="odd">
<td><p><strong>adEmpty</strong></p></td>
<td><p>0</p></td>
<td><p>Gibt keinen Wert an (DBTYPE_EMPTY).</p></td>
</tr>
<tr class="even">
<td><p><strong>adError</strong></p></td>
<td><p>10</p></td>
<td><p>Gibt einen 32-Bit-Fehlercode an (DBTYPE_ERROR).</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFileTime</strong></p></td>
<td><p>64</p></td>
<td><p>Gibt einen 64-Bit-Wert an, der die Zahl der 100-Nanosekunden-Intervalle seit 1. Januar 1601 darstellt (DBTYPE_FILETIME).</p></td>
</tr>
<tr class="even">
<td><p><strong>adGUID</strong></p></td>
<td><p>72</p></td>
<td><p>Gibt einen global eindeutigen Bezeichner (GUID) an (DBTYPE_GUID).</p></td>
</tr>
<tr class="odd">
<td><p><strong>adIDispatch</strong></p></td>
<td><p>9</p></td>
<td><p>Gibt einen Zeiger auf eine <strong>IDispatch</strong>-Schnittstelle in einem COM-Objekt an (DBTYPE_IDISPATCH).
</p>

> [!NOTE]
> <P>Dieser Datentyp wird derzeit nicht von ADO unterstützt. Seine Verwendung kann zu unvorhersehbaren Ergebnissen führen.</P>


<p></p></td>
</tr>
<tr class="even">
<td><p><strong>adInteger</strong></p></td>
<td><p>3</p></td>
<td><p>Gibt eine ganze Zahl mit Vorzeichen und einer Länge von 4 Bytes an (DBTYPE_I4).</p></td>
</tr>
<tr class="odd">
<td><p><strong>adIUnknown</strong></p></td>
<td><p>13</p></td>
<td><p>Gibt einen Zeiger auf eine <strong>IUnknown</strong>-Schnittstelle in einem COM-Objekt an (DBTYPE_IUNKNOWN).
</p>

> [!NOTE]
> <P>Dieser Datentyp wird derzeit nicht von ADO unterstützt. Seine Verwendung kann zu unvorhersehbaren Ergebnissen führen.</P>


<p></p></td>
</tr>
<tr class="even">
<td><p><strong>adLongVarBinary</strong></p></td>
<td><p>205</p></td>
<td><p>Gibt einen langen Binärwert an.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adLongVarChar</strong></p></td>
<td><p>201</p></td>
<td><p>Gibt einen langen Zeichenfolgenwert an.</p></td>
</tr>
<tr class="even">
<td><p><strong>adLongVarWChar</strong></p></td>
<td><p>203</p></td>
<td><p>Gibt einen mit Null endenden Unicode-Zeichenfolgenwert an.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adNumeric</strong></p></td>
<td><p>131</p></td>
<td><p>Gibt einen genauen numerischen Wert mit einer festen Genauigkeit und einem festen Maßstab an (DBTYPE_NUMERIC).</p></td>
</tr>
<tr class="even">
<td><p><strong>adPropVariant</strong></p></td>
<td><p>138</p></td>
<td><p>Gibt eine Automatisierungs-PROPVARIANT an (DBTYPE_PROP_VARIANT).</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSingle</strong></p></td>
<td><p>4</p></td>
<td><p>Gibt einen Gleitkommawert mit einfacher Genauigkeit an (DBTYPE_R4).</p></td>
</tr>
<tr class="even">
<td><p><strong>adSmallInt</strong></p></td>
<td><p>2</p></td>
<td><p>Gibt eine ganze Zahl mit Vorzeichen und einer Länge von 2 Bytes an (DBTYPE_I2).</p></td>
</tr>
<tr class="odd">
<td><p><strong>adTinyInt</strong></p></td>
<td><p>16</p></td>
<td><p>Gibt eine ganze Zahl mit Vorzeichen und einer Länge von 1 Byte an (DBTYPE_I1).</p></td>
</tr>
<tr class="even">
<td><p><strong>adUnsignedBigInt</strong></p></td>
<td><p>21</p></td>
<td><p>Gibt eine ganze Zahl ohne Vorzeichen und mit einer Länge von 8 Bytes an (DBTYPE_UI8).</p></td>
</tr>
<tr class="odd">
<td><p><strong>adUnsignedInt</strong></p></td>
<td><p>19</p></td>
<td><p>Gibt eine ganze Zahl ohne Vorzeichen und mit einer Länge von 4 Bytes an (DBTYPE_UI4).</p></td>
</tr>
<tr class="even">
<td><p><strong>adUnsignedSmallInt</strong></p></td>
<td><p>18</p></td>
<td><p>Gibt eine ganze Zahl ohne Vorzeichen und mit einer Länge von 2 Bytes an (DBTYPE_UI2).</p></td>
</tr>
<tr class="odd">
<td><p><strong>adUnsignedTinyInt</strong></p></td>
<td><p>17</p></td>
<td><p>Gibt eine ganze Zahl ohne Vorzeichen und mit einer Länge von 1 Byte an (DBTYPE_UI1).</p></td>
</tr>
<tr class="even">
<td><p><strong>adUserDefined</strong></p></td>
<td><p>132</p></td>
<td><p>Gibt eine benutzerdefinierte Variable an (DBTYPE_UDT).</p></td>
</tr>
<tr class="odd">
<td><p><strong>adVarBinary</strong></p></td>
<td><p>204</p></td>
<td><p>Gibt einen Binärwert an (nur für <strong>Parameter</strong>-Objekt).</p></td>
</tr>
<tr class="even">
<td><p><strong>adVarChar</strong></p></td>
<td><p>200</p></td>
<td><p>Gibt einen Zeichenfolgenwert an.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adVariant</strong></p></td>
<td><p>12</p></td>
<td><p>Gibt ein Automation <strong>Variant</strong> (DBTYPE_VARIANT).</p>

> [!NOTE]
> <P>Dieser Datentyp wird derzeit nicht von ADO unterstützt. Seine Verwendung kann zu unvorhersehbaren Ergebnissen führen.</P>


<p></p></td>
</tr>
<tr class="even">
<td><p><strong>adVarNumeric</strong></p></td>
<td><p>139</p></td>
<td><p>Gibt einen numerischen Wert an (nur für <strong>Parameter</strong>-Objekt).</p></td>
</tr>
<tr class="odd">
<td><p><strong>adVarWChar</strong></p></td>
<td><p>202</p></td>
<td><p>Gibt eine mit Null endende Unicode-Zeichenfolge an.</p></td>
</tr>
<tr class="even">
<td><p><strong>adWChar</strong></p></td>
<td><p>130</p></td>
<td><p>Gibt eine mit Null endende Unicode-Zeichenfolge an (DBTYPE_WSTR).</p></td>
</tr>
</tbody>
</table>


**ADO/WFC-Entsprechung**

Paket: **com.ms.wfc.data**

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Konstante</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>AdoEnums.DataType.ARRAY</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.DataType.BIGINT</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.DataType.BINARY</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.DataType.BOOLEAN</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.DataType.BSTR</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.DataType.CHAPTER</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.DataType.CHAR</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.DataType.CURRENCY</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.DataType.DATE</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.DataType.DBDATE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.DataType.DBTIME</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.DataType.DBTIMESTAMP</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.DataType.DECIMAL</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.DataType.DOUBLE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.DataType.EMPTY</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.DataType.ERROR</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.DataType.FILETIME</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.DataType.GUID</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.DataType.IDISPATCH</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.DataType.INTEGER</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.DataType.IUNKNOWN</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.DataType.LONGVARBINARY</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.DataType.LONGVARCHAR</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.DataType.LONGVARWCHAR</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.DataType.NUMERIC</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.DataType.PROPVARIANT</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.DataType.SINGLE</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.DataType.SMALLINT</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.DataType.TINYINT</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.DataType.UNSIGNEDBIGINT</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.DataType.UNSIGNEDINT</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.DataType.UNSIGNEDSMALLINT</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.DataType.UNSIGNEDTINYINT</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.DataType.USERDEFINED</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.DataType.VARBINARY</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.DataType.VARCHAR</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.DataType.VARIANT</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.DataType.VARNUMERIC</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.DataType.VARWCHAR</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.DataType.WCHAR</p></td>
</tr>
</tbody>
</table>

