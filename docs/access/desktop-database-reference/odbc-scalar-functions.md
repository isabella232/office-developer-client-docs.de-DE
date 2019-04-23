---
title: ODBC-Skalarfunktionen
TOCTitle: ODBC scalar functions
ms:assetid: dc1096bf-8241-036a-14c6-b19afae45454
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835353(v=office.15)
ms:contentKeyID: 48548120
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277473
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 33443fda474b3785d34d457719e49f5e358bb254
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288511"
---
# <a name="odbc-scalar-functions"></a><span data-ttu-id="39fb8-102">ODBC-Skalarfunktionen</span><span class="sxs-lookup"><span data-stu-id="39fb8-102">ODBC scalar functions</span></span>

<span data-ttu-id="39fb8-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="39fb8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="39fb8-104">Microsoft Access SQL unterstützt die Verwendung der ODBC-Syntax für Skalarfunktionen.</span><span class="sxs-lookup"><span data-stu-id="39fb8-104">Microsoft Access SQL supports the use of the ODBC defined syntax for scalar functions.</span></span> 

<span data-ttu-id="39fb8-105">Die Abfrage `SELECT DAILYCLOSE, DAILYCHANGE FROM DAILYQUOTE WHERE {fn ABS(DAILYCHANGE)} > 5` würde beispielsweise alle Zeilen zurückgeben, bei denen der absolute Wert der Änderung des Kurses einer Aktie größer als fünf war.</span><span class="sxs-lookup"><span data-stu-id="39fb8-105">For example, the query `SELECT DAILYCLOSE, DAILYCHANGE FROM DAILYQUOTE WHERE {fn ABS(DAILYCHANGE)} > 5` would return all rows where the absolute value of the change in the price of a stock was greater than five.</span></span>

<span data-ttu-id="39fb8-p101">Es wird eine Untermenge der über ODBC definierten Skalarfunktionen unterstützt. In der folgenden Tabelle sind die unterstützten Funktionen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="39fb8-p101">A subset of the ODBC defined scalar functions is supported. The following table lists the functions that are supported.</span></span>

<span data-ttu-id="39fb8-108">Eine Beschreibung der Argumente und eine ausführliche Erläuterung der Escapesyntax für INCLUDE-Funktionen in einer SQL-Anweisung finden Sie in der ODBC-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="39fb8-108">For a description of the arguments and a complete explanation of the escape syntax for including functions in a SQL statement, see the ODBC documentation.</span></span>

## <a name="string-functions"></a><span data-ttu-id="39fb8-109">Zeichenfolgenfunktionen</span><span class="sxs-lookup"><span data-stu-id="39fb8-109">String functions</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="39fb8-110">ASCII</span><span class="sxs-lookup"><span data-stu-id="39fb8-110">ASCII</span></span></p></td>
<td><p><span data-ttu-id="39fb8-111">Länge</span><span class="sxs-lookup"><span data-stu-id="39fb8-111">LENGTH</span></span></p></td>
<td><p><span data-ttu-id="39fb8-112">RTRIM</span><span class="sxs-lookup"><span data-stu-id="39fb8-112">RTRIM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="39fb8-113">CHAR</span><span class="sxs-lookup"><span data-stu-id="39fb8-113">CHAR</span></span></p></td>
<td><p><span data-ttu-id="39fb8-114">Suchen</span><span class="sxs-lookup"><span data-stu-id="39fb8-114">LOCATE</span></span></p></td>
<td><p><span data-ttu-id="39fb8-115">LEERTASTE</span><span class="sxs-lookup"><span data-stu-id="39fb8-115">SPACE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="39fb8-116">CONCAT</span><span class="sxs-lookup"><span data-stu-id="39fb8-116">CONCAT</span></span></p></td>
<td><p><span data-ttu-id="39fb8-117">LTRIM</span><span class="sxs-lookup"><span data-stu-id="39fb8-117">LTRIM</span></span></p></td>
<td><p><span data-ttu-id="39fb8-118">Teilzeichenfolge</span><span class="sxs-lookup"><span data-stu-id="39fb8-118">SUBSTRING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="39fb8-119">LCASE</span><span class="sxs-lookup"><span data-stu-id="39fb8-119">LCASE</span></span></p></td>
<td><p><span data-ttu-id="39fb8-120">Richting</span><span class="sxs-lookup"><span data-stu-id="39fb8-120">RIGHT</span></span></p></td>
<td><p><span data-ttu-id="39fb8-121">UCASE</span><span class="sxs-lookup"><span data-stu-id="39fb8-121">UCASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="39fb8-122">Links</span><span class="sxs-lookup"><span data-stu-id="39fb8-122">LEFT</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


## <a name="numeric-functions"></a><span data-ttu-id="39fb8-123">Numerische Funktionen</span><span class="sxs-lookup"><span data-stu-id="39fb8-123">Numeric functions</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="39fb8-124">ABS</span><span class="sxs-lookup"><span data-stu-id="39fb8-124">ABS</span></span></p></td>
<td><p><span data-ttu-id="39fb8-125">FLOOR</span><span class="sxs-lookup"><span data-stu-id="39fb8-125">FLOOR</span></span></p></td>
<td><p><span data-ttu-id="39fb8-126">Sünde</span><span class="sxs-lookup"><span data-stu-id="39fb8-126">SIN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="39fb8-127">ARCTAN</span><span class="sxs-lookup"><span data-stu-id="39fb8-127">ATAN</span></span></p></td>
<td><p><span data-ttu-id="39fb8-128">Protokoll</span><span class="sxs-lookup"><span data-stu-id="39fb8-128">LOG</span></span></p></td>
<td><p><span data-ttu-id="39fb8-129">Wurzel</span><span class="sxs-lookup"><span data-stu-id="39fb8-129">SQRT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="39fb8-130">Decke</span><span class="sxs-lookup"><span data-stu-id="39fb8-130">CEILING</span></span></p></td>
<td><p><span data-ttu-id="39fb8-131">MACHT</span><span class="sxs-lookup"><span data-stu-id="39fb8-131">POWER</span></span></p></td>
<td><p><span data-ttu-id="39fb8-132">TAN</span><span class="sxs-lookup"><span data-stu-id="39fb8-132">TAN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="39fb8-133">COS</span><span class="sxs-lookup"><span data-stu-id="39fb8-133">COS</span></span></p></td>
<td><p><span data-ttu-id="39fb8-134">RAND</span><span class="sxs-lookup"><span data-stu-id="39fb8-134">RAND</span></span></p></td>
<td><p><span data-ttu-id="39fb8-135">MOD</span><span class="sxs-lookup"><span data-stu-id="39fb8-135">MOD</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="39fb8-136">EXP</span><span class="sxs-lookup"><span data-stu-id="39fb8-136">EXP</span></span></p></td>
<td><p><span data-ttu-id="39fb8-137">Zeichen</span><span class="sxs-lookup"><span data-stu-id="39fb8-137">SIGN</span></span></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


## <a name="time--date-functions"></a><span data-ttu-id="39fb8-138">Zeit & Datumsfunktionen</span><span class="sxs-lookup"><span data-stu-id="39fb8-138">Time & Date functions</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="39fb8-139">CURDATE</span><span class="sxs-lookup"><span data-stu-id="39fb8-139">CURDATE</span></span></p></td>
<td><p><span data-ttu-id="39fb8-140">DAYOFYEAR</span><span class="sxs-lookup"><span data-stu-id="39fb8-140">DAYOFYEAR</span></span></p></td>
<td><p><span data-ttu-id="39fb8-141">Monat</span><span class="sxs-lookup"><span data-stu-id="39fb8-141">MONTH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="39fb8-142">CURTIME</span><span class="sxs-lookup"><span data-stu-id="39fb8-142">CURTIME</span></span></p></td>
<td><p><span data-ttu-id="39fb8-143">Jahr</span><span class="sxs-lookup"><span data-stu-id="39fb8-143">YEAR</span></span></p></td>
<td><p><span data-ttu-id="39fb8-144">Woche</span><span class="sxs-lookup"><span data-stu-id="39fb8-144">WEEK</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="39fb8-145">JETZT</span><span class="sxs-lookup"><span data-stu-id="39fb8-145">NOW</span></span></p></td>
<td><p><span data-ttu-id="39fb8-146">Stunde</span><span class="sxs-lookup"><span data-stu-id="39fb8-146">HOUR</span></span></p></td>
<td><p><span data-ttu-id="39fb8-147">Quartal</span><span class="sxs-lookup"><span data-stu-id="39fb8-147">QUARTER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="39fb8-148">DAYOFMONTH</span><span class="sxs-lookup"><span data-stu-id="39fb8-148">DAYOFMONTH</span></span></p></td>
<td><p><span data-ttu-id="39fb8-149">MINUTE</span><span class="sxs-lookup"><span data-stu-id="39fb8-149">MINUTE</span></span></p></td>
<td><p><span data-ttu-id="39fb8-150">MONTHNAME</span><span class="sxs-lookup"><span data-stu-id="39fb8-150">MONTHNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="39fb8-151">DAYOFWEEK</span><span class="sxs-lookup"><span data-stu-id="39fb8-151">DAYOFWEEK</span></span></p></td>
<td><p><span data-ttu-id="39fb8-152">ZWEITEN</span><span class="sxs-lookup"><span data-stu-id="39fb8-152">SECOND</span></span></p></td>
<td><p><span data-ttu-id="39fb8-153">DAYNAME</span><span class="sxs-lookup"><span data-stu-id="39fb8-153">DAYNAME</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="data-type-conversion"></a><span data-ttu-id="39fb8-154">Datentypkonvertierung</span><span class="sxs-lookup"><span data-stu-id="39fb8-154">Data type conversion</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="39fb8-155">Konvertieren</span><span class="sxs-lookup"><span data-stu-id="39fb8-155">CONVERT</span></span></p></td>
<td><p><span data-ttu-id="39fb8-156">Zeichenfolgenliterale können in folgende Datentypen konvertiert werden: SQL_FLOAT, SQL_DOUBLE, SQL_NUMERIC, SQL_INTEGER, SQL_REAL, SQL_SMALLINT, SQL_VARCHAR und SQL_DATETIME.</span><span class="sxs-lookup"><span data-stu-id="39fb8-156">String literals can be converted to the following data types: SQL_FLOAT, SQL_DOUBLE, SQL_NUMERIC, SQL_INTEGER, SQL_REAL, SQL_SMALLINT, SQL_VARCHAR and SQL_DATETIME.</span></span></p></td>
</tr>
</tbody>
</table>

