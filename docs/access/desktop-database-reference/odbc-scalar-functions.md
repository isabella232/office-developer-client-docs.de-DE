---
title: ODBC-Skalarfunktionen
TOCTitle: ODBC Scalar Functions
ms:assetid: dc1096bf-8241-036a-14c6-b19afae45454
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835353(v=office.15)
ms:contentKeyID: 48548120
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277473
f1_categories:
- Office.Version=v15
ms.openlocfilehash: d01c5f02cc784518d58365480b30178d4d24a332
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473693"
---
# <a name="odbc-scalar-functions"></a>ODBC-Skalarfunktionen


**Betrifft**: Access 2013 | Office 2013

Microsoft® Access SQL unterstützt die Verwendung der über ODBC definierten Syntax für Skalarfunktionen. Beispielsweise gibt die Abfrage

SELECT DAILYCLOSE, DAILYCHANGE FROM DAILYQUOTE WHERE {fn ABS(DAILYCHANGE)} \> 5

alle Zeilen zurück, in denen der absolute Wert für die Preisänderung einer Aktie größer als fünf ist.

Es wird eine Untermenge der über ODBC definierten Skalarfunktionen unterstützt. In der folgenden Tabelle sind die unterstützten Funktionen aufgeführt.

Eine Beschreibung der Argumente und eine ausführliche Erläuterung der Escapesyntax für INCLUDE-Funktionen in einer SQL-Anweisung finden Sie in der ODBC-Dokumentation.

## <a name="string-functions"></a>Zeichenfolgenfunktionen

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>ASCII</p></td>
<td><p>LENGTH</p></td>
<td><p>RTRIM</p></td>
</tr>
<tr class="even">
<td><p>CHAR</p></td>
<td><p>LOCATE</p></td>
<td><p>SPACE</p></td>
</tr>
<tr class="odd">
<td><p>CONCAT</p></td>
<td><p>LTRIM</p></td>
<td><p>SUBSTRING</p></td>
</tr>
<tr class="even">
<td><p>LCASE</p></td>
<td><p>RIGHT</p></td>
<td><p>UCASE</p></td>
</tr>
<tr class="odd">
<td><p>LEFT</p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


## <a name="numeric-functions"></a>Numerische Funktionen

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>ABS</p></td>
<td><p>FLOOR</p></td>
<td><p>SIN</p></td>
</tr>
<tr class="even">
<td><p>ATAN</p></td>
<td><p>LOG</p></td>
<td><p>SQRT</p></td>
</tr>
<tr class="odd">
<td><p>CEILING</p></td>
<td><p>POWER</p></td>
<td><p>TAN</p></td>
</tr>
<tr class="even">
<td><p>COS</p></td>
<td><p>RAND</p></td>
<td><p>MOD</p></td>
</tr>
<tr class="odd">
<td><p>EXP</p></td>
<td><p>SIGN</p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


## <a name="time--date-functions"></a>Uhrzeit- und Datumsfunktionen

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>CURDATE</p></td>
<td><p>DAYOFYEAR</p></td>
<td><p>MONTH</p></td>
</tr>
<tr class="even">
<td><p>CURTIME</p></td>
<td><p>YEAR</p></td>
<td><p>WEEK</p></td>
</tr>
<tr class="odd">
<td><p>NOW</p></td>
<td><p>HOUR</p></td>
<td><p>QUARTER</p></td>
</tr>
<tr class="even">
<td><p>DAYOFMONTH</p></td>
<td><p>MINUTE</p></td>
<td><p>MONTHNAME</p></td>
</tr>
<tr class="odd">
<td><p>DAYOFWEEK</p></td>
<td><p>SECOND</p></td>
<td><p>DAYNAME</p></td>
</tr>
</tbody>
</table>


## <a name="data-type-conversion"></a>Datentypkonvertierung

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>CONVERT</p></td>
<td><p>Zeichenfolgenliterale können in folgende Datentypen konvertiert werden: SQL_FLOAT, SQL_DOUBLE, SQL_NUMERIC, SQL_INTEGER, SQL_REAL, SQL_SMALLINT, SQL_VARCHAR und SQL_DATETIME.</p></td>
</tr>
</tbody>
</table>
