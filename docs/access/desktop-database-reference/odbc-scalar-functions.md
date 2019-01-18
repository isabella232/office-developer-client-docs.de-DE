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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718035"
---
# <a name="odbc-scalar-functions"></a><span data-ttu-id="adba0-102">ODBC-Skalarfunktionen</span><span class="sxs-lookup"><span data-stu-id="adba0-102">ODBC scalar functions</span></span>

<span data-ttu-id="adba0-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="adba0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="adba0-104">Microsoft Access SQL unterstützt die Verwendung der ODBC definierten Syntax für Skalarfunktionen.</span><span class="sxs-lookup"><span data-stu-id="adba0-104">Microsoft Access SQL supports the use of the ODBC defined syntax for scalar functions.</span></span> 

<span data-ttu-id="adba0-105">Beispiel: die Abfrage `SELECT DAILYCLOSE, DAILYCHANGE FROM DAILYQUOTE WHERE {fn ABS(DAILYCHANGE)} > 5` alle Zeilen, bei denen der Absolute Wert der Änderung in die Preisänderung einer Aktie größer als fünf war, zurück.</span><span class="sxs-lookup"><span data-stu-id="adba0-105">For example, the query `SELECT DAILYCLOSE, DAILYCHANGE FROM DAILYQUOTE WHERE {fn ABS(DAILYCHANGE)} > 5` would return all rows where the absolute value of the change in the price of a stock was greater than five.</span></span>

<span data-ttu-id="adba0-p101">Es wird eine Untermenge der über ODBC definierten Skalarfunktionen unterstützt. In der folgenden Tabelle sind die unterstützten Funktionen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="adba0-p101">A subset of the ODBC defined scalar functions is supported. The following table lists the functions that are supported.</span></span>

<span data-ttu-id="adba0-108">Eine Beschreibung der Argumente und eine ausführliche Erläuterung der Escapesyntax für INCLUDE-Funktionen in einer SQL-Anweisung finden Sie in der ODBC-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="adba0-108">For a description of the arguments and a complete explanation of the escape syntax for including functions in a SQL statement, see the ODBC documentation.</span></span>

## <a name="string-functions"></a><span data-ttu-id="adba0-109">Zeichenfolgenfunktionen</span><span class="sxs-lookup"><span data-stu-id="adba0-109">String functions</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="adba0-110">ASCII</span><span class="sxs-lookup"><span data-stu-id="adba0-110">ASCII</span></span></p></td>
<td><p><span data-ttu-id="adba0-111">LENGTH</span><span class="sxs-lookup"><span data-stu-id="adba0-111">LENGTH</span></span></p></td>
<td><p><span data-ttu-id="adba0-112">RTRIM</span><span class="sxs-lookup"><span data-stu-id="adba0-112">RTRIM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="adba0-113">CHAR</span><span class="sxs-lookup"><span data-stu-id="adba0-113">CHAR</span></span></p></td>
<td><p><span data-ttu-id="adba0-114">LOCATE</span><span class="sxs-lookup"><span data-stu-id="adba0-114">LOCATE</span></span></p></td>
<td><p><span data-ttu-id="adba0-115">SPACE</span><span class="sxs-lookup"><span data-stu-id="adba0-115">SPACE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="adba0-116">CONCAT</span><span class="sxs-lookup"><span data-stu-id="adba0-116">CONCAT</span></span></p></td>
<td><p><span data-ttu-id="adba0-117">LTRIM</span><span class="sxs-lookup"><span data-stu-id="adba0-117">LTRIM</span></span></p></td>
<td><p><span data-ttu-id="adba0-118">SUBSTRING</span><span class="sxs-lookup"><span data-stu-id="adba0-118">SUBSTRING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="adba0-119">LCASE</span><span class="sxs-lookup"><span data-stu-id="adba0-119">LCASE</span></span></p></td>
<td><p><span data-ttu-id="adba0-120">RIGHT</span><span class="sxs-lookup"><span data-stu-id="adba0-120">RIGHT</span></span></p></td>
<td><p><span data-ttu-id="adba0-121">UCASE</span><span class="sxs-lookup"><span data-stu-id="adba0-121">UCASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="adba0-122">LEFT</span><span class="sxs-lookup"><span data-stu-id="adba0-122">LEFT</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


## <a name="numeric-functions"></a><span data-ttu-id="adba0-123">Numerische Funktionen</span><span class="sxs-lookup"><span data-stu-id="adba0-123">Numeric functions</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="adba0-124">ABS</span><span class="sxs-lookup"><span data-stu-id="adba0-124">ABS</span></span></p></td>
<td><p><span data-ttu-id="adba0-125">FLOOR</span><span class="sxs-lookup"><span data-stu-id="adba0-125">FLOOR</span></span></p></td>
<td><p><span data-ttu-id="adba0-126">SIN</span><span class="sxs-lookup"><span data-stu-id="adba0-126">SIN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="adba0-127">ATAN</span><span class="sxs-lookup"><span data-stu-id="adba0-127">ATAN</span></span></p></td>
<td><p><span data-ttu-id="adba0-128">LOG</span><span class="sxs-lookup"><span data-stu-id="adba0-128">LOG</span></span></p></td>
<td><p><span data-ttu-id="adba0-129">SQRT</span><span class="sxs-lookup"><span data-stu-id="adba0-129">SQRT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="adba0-130">CEILING</span><span class="sxs-lookup"><span data-stu-id="adba0-130">CEILING</span></span></p></td>
<td><p><span data-ttu-id="adba0-131">POWER</span><span class="sxs-lookup"><span data-stu-id="adba0-131">POWER</span></span></p></td>
<td><p><span data-ttu-id="adba0-132">TAN</span><span class="sxs-lookup"><span data-stu-id="adba0-132">TAN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="adba0-133">COS</span><span class="sxs-lookup"><span data-stu-id="adba0-133">COS</span></span></p></td>
<td><p><span data-ttu-id="adba0-134">RAND</span><span class="sxs-lookup"><span data-stu-id="adba0-134">RAND</span></span></p></td>
<td><p><span data-ttu-id="adba0-135">MOD</span><span class="sxs-lookup"><span data-stu-id="adba0-135">MOD</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="adba0-136">EXP</span><span class="sxs-lookup"><span data-stu-id="adba0-136">EXP</span></span></p></td>
<td><p><span data-ttu-id="adba0-137">SIGN</span><span class="sxs-lookup"><span data-stu-id="adba0-137">SIGN</span></span></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


## <a name="time--date-functions"></a><span data-ttu-id="adba0-138">Zeit & Datumsfunktionen</span><span class="sxs-lookup"><span data-stu-id="adba0-138">Time & Date functions</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="adba0-139">CURDATE</span><span class="sxs-lookup"><span data-stu-id="adba0-139">CURDATE</span></span></p></td>
<td><p><span data-ttu-id="adba0-140">DAYOFYEAR</span><span class="sxs-lookup"><span data-stu-id="adba0-140">DAYOFYEAR</span></span></p></td>
<td><p><span data-ttu-id="adba0-141">MONTH</span><span class="sxs-lookup"><span data-stu-id="adba0-141">MONTH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="adba0-142">CURTIME</span><span class="sxs-lookup"><span data-stu-id="adba0-142">CURTIME</span></span></p></td>
<td><p><span data-ttu-id="adba0-143">YEAR</span><span class="sxs-lookup"><span data-stu-id="adba0-143">YEAR</span></span></p></td>
<td><p><span data-ttu-id="adba0-144">WEEK</span><span class="sxs-lookup"><span data-stu-id="adba0-144">WEEK</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="adba0-145">NOW</span><span class="sxs-lookup"><span data-stu-id="adba0-145">NOW</span></span></p></td>
<td><p><span data-ttu-id="adba0-146">HOUR</span><span class="sxs-lookup"><span data-stu-id="adba0-146">HOUR</span></span></p></td>
<td><p><span data-ttu-id="adba0-147">QUARTER</span><span class="sxs-lookup"><span data-stu-id="adba0-147">QUARTER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="adba0-148">DAYOFMONTH</span><span class="sxs-lookup"><span data-stu-id="adba0-148">DAYOFMONTH</span></span></p></td>
<td><p><span data-ttu-id="adba0-149">MINUTE</span><span class="sxs-lookup"><span data-stu-id="adba0-149">MINUTE</span></span></p></td>
<td><p><span data-ttu-id="adba0-150">MONTHNAME</span><span class="sxs-lookup"><span data-stu-id="adba0-150">MONTHNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="adba0-151">DAYOFWEEK</span><span class="sxs-lookup"><span data-stu-id="adba0-151">DAYOFWEEK</span></span></p></td>
<td><p><span data-ttu-id="adba0-152">SECOND</span><span class="sxs-lookup"><span data-stu-id="adba0-152">SECOND</span></span></p></td>
<td><p><span data-ttu-id="adba0-153">DAYNAME</span><span class="sxs-lookup"><span data-stu-id="adba0-153">DAYNAME</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="data-type-conversion"></a><span data-ttu-id="adba0-154">Datentypkonvertierung</span><span class="sxs-lookup"><span data-stu-id="adba0-154">Data type conversion</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="adba0-155">CONVERT</span><span class="sxs-lookup"><span data-stu-id="adba0-155">CONVERT</span></span></p></td>
<td><p><span data-ttu-id="adba0-156">Zeichenfolgenliterale können in folgende Datentypen konvertiert werden: SQL_FLOAT, SQL_DOUBLE, SQL_NUMERIC, SQL_INTEGER, SQL_REAL, SQL_SMALLINT, SQL_VARCHAR und SQL_DATETIME.</span><span class="sxs-lookup"><span data-stu-id="adba0-156">String literals can be converted to the following data types: SQL_FLOAT, SQL_DOUBLE, SQL_NUMERIC, SQL_INTEGER, SQL_REAL, SQL_SMALLINT, SQL_VARCHAR and SQL_DATETIME.</span></span></p></td>
</tr>
</tbody>
</table>

