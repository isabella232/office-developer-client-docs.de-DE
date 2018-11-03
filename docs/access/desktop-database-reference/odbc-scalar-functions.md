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
ms.openlocfilehash: 6e312bf0b6092df88f86f4bbf843d7951f3c86cc
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25947875"
---
# <a name="odbc-scalar-functions"></a><span data-ttu-id="a649f-102">ODBC-Skalarfunktionen</span><span class="sxs-lookup"><span data-stu-id="a649f-102">ODBC scalar functions</span></span>


<span data-ttu-id="a649f-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a649f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a649f-104">Microsoft Access SQL unterstützt die Verwendung der ODBC definierten Syntax für Skalarfunktionen.</span><span class="sxs-lookup"><span data-stu-id="a649f-104">Microsoft Access SQL supports the use of the ODBC defined syntax for scalar functions.</span></span> <span data-ttu-id="a649f-105">Beispielsweise gibt die Abfrage</span><span class="sxs-lookup"><span data-stu-id="a649f-105">For example, the query:</span></span>

<span data-ttu-id="a649f-106">SELECT DAILYCLOSE, DAILYCHANGE FROM DAILYQUOTE WHERE {fn ABS(DAILYCHANGE)} \> 5</span><span class="sxs-lookup"><span data-stu-id="a649f-106">SELECT DAILYCLOSE, DAILYCHANGE FROM DAILYQUOTE WHERE {fn ABS(DAILYCHANGE)} \> 5</span></span>

<span data-ttu-id="a649f-107">alle Zeilen zurück, in denen der absolute Wert für die Preisänderung einer Aktie größer als fünf ist.</span><span class="sxs-lookup"><span data-stu-id="a649f-107">Would return all rows where the absolute value of the change in the price of a stock was greater than five.</span></span>

<span data-ttu-id="a649f-p102">Es wird eine Untermenge der über ODBC definierten Skalarfunktionen unterstützt. In der folgenden Tabelle sind die unterstützten Funktionen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="a649f-p102">A subset of the ODBC defined scalar functions is supported. The following table lists the functions that are supported.</span></span>

<span data-ttu-id="a649f-110">Eine Beschreibung der Argumente und eine ausführliche Erläuterung der Escapesyntax für INCLUDE-Funktionen in einer SQL-Anweisung finden Sie in der ODBC-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="a649f-110">For a description of the arguments and a complete explanation of the escape syntax for including functions in a SQL statement, see the ODBC documentation.</span></span>

## <a name="string-functions"></a><span data-ttu-id="a649f-111">Zeichenfolgenfunktionen</span><span class="sxs-lookup"><span data-stu-id="a649f-111">String Functions</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a649f-112">ASCII</span><span class="sxs-lookup"><span data-stu-id="a649f-112">ASCII</span></span></p></td>
<td><p><span data-ttu-id="a649f-113">LENGTH</span><span class="sxs-lookup"><span data-stu-id="a649f-113">LENGTH</span></span></p></td>
<td><p><span data-ttu-id="a649f-114">RTRIM</span><span class="sxs-lookup"><span data-stu-id="a649f-114">RTRIM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a649f-115">CHAR</span><span class="sxs-lookup"><span data-stu-id="a649f-115">CHAR</span></span></p></td>
<td><p><span data-ttu-id="a649f-116">LOCATE</span><span class="sxs-lookup"><span data-stu-id="a649f-116">LOCATE</span></span></p></td>
<td><p><span data-ttu-id="a649f-117">SPACE</span><span class="sxs-lookup"><span data-stu-id="a649f-117">SPACE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a649f-118">CONCAT</span><span class="sxs-lookup"><span data-stu-id="a649f-118">CONCAT</span></span></p></td>
<td><p><span data-ttu-id="a649f-119">LTRIM</span><span class="sxs-lookup"><span data-stu-id="a649f-119">LTRIM</span></span></p></td>
<td><p><span data-ttu-id="a649f-120">SUBSTRING</span><span class="sxs-lookup"><span data-stu-id="a649f-120">SUBSTRING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a649f-121">LCASE</span><span class="sxs-lookup"><span data-stu-id="a649f-121">LCASE</span></span></p></td>
<td><p><span data-ttu-id="a649f-122">RIGHT</span><span class="sxs-lookup"><span data-stu-id="a649f-122">RIGHT</span></span></p></td>
<td><p><span data-ttu-id="a649f-123">UCASE</span><span class="sxs-lookup"><span data-stu-id="a649f-123">UCASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a649f-124">LEFT</span><span class="sxs-lookup"><span data-stu-id="a649f-124">LEFT</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


## <a name="numeric-functions"></a><span data-ttu-id="a649f-125">Numerische Funktionen</span><span class="sxs-lookup"><span data-stu-id="a649f-125">Numeric Functions</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a649f-126">ABS</span><span class="sxs-lookup"><span data-stu-id="a649f-126">ABS</span></span></p></td>
<td><p><span data-ttu-id="a649f-127">FLOOR</span><span class="sxs-lookup"><span data-stu-id="a649f-127">FLOOR</span></span></p></td>
<td><p><span data-ttu-id="a649f-128">SIN</span><span class="sxs-lookup"><span data-stu-id="a649f-128">SIN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a649f-129">ATAN</span><span class="sxs-lookup"><span data-stu-id="a649f-129">ATAN</span></span></p></td>
<td><p><span data-ttu-id="a649f-130">LOG</span><span class="sxs-lookup"><span data-stu-id="a649f-130">LOG</span></span></p></td>
<td><p><span data-ttu-id="a649f-131">SQRT</span><span class="sxs-lookup"><span data-stu-id="a649f-131">SQRT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a649f-132">CEILING</span><span class="sxs-lookup"><span data-stu-id="a649f-132">CEILING</span></span></p></td>
<td><p><span data-ttu-id="a649f-133">POWER</span><span class="sxs-lookup"><span data-stu-id="a649f-133">POWER</span></span></p></td>
<td><p><span data-ttu-id="a649f-134">TAN</span><span class="sxs-lookup"><span data-stu-id="a649f-134">TAN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a649f-135">COS</span><span class="sxs-lookup"><span data-stu-id="a649f-135">COS</span></span></p></td>
<td><p><span data-ttu-id="a649f-136">RAND</span><span class="sxs-lookup"><span data-stu-id="a649f-136">RAND</span></span></p></td>
<td><p><span data-ttu-id="a649f-137">MOD</span><span class="sxs-lookup"><span data-stu-id="a649f-137">MOD</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a649f-138">EXP</span><span class="sxs-lookup"><span data-stu-id="a649f-138">EXP</span></span></p></td>
<td><p><span data-ttu-id="a649f-139">SIGN</span><span class="sxs-lookup"><span data-stu-id="a649f-139">SIGN</span></span></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


## <a name="time--date-functions"></a><span data-ttu-id="a649f-140">Uhrzeit- und Datumsfunktionen</span><span class="sxs-lookup"><span data-stu-id="a649f-140">Time & Date Functions</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a649f-141">CURDATE</span><span class="sxs-lookup"><span data-stu-id="a649f-141">CURDATE</span></span></p></td>
<td><p><span data-ttu-id="a649f-142">DAYOFYEAR</span><span class="sxs-lookup"><span data-stu-id="a649f-142">DAYOFYEAR</span></span></p></td>
<td><p><span data-ttu-id="a649f-143">MONTH</span><span class="sxs-lookup"><span data-stu-id="a649f-143">MONTH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a649f-144">CURTIME</span><span class="sxs-lookup"><span data-stu-id="a649f-144">CURTIME</span></span></p></td>
<td><p><span data-ttu-id="a649f-145">YEAR</span><span class="sxs-lookup"><span data-stu-id="a649f-145">YEAR</span></span></p></td>
<td><p><span data-ttu-id="a649f-146">WEEK</span><span class="sxs-lookup"><span data-stu-id="a649f-146">WEEK</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a649f-147">NOW</span><span class="sxs-lookup"><span data-stu-id="a649f-147">NOW</span></span></p></td>
<td><p><span data-ttu-id="a649f-148">HOUR</span><span class="sxs-lookup"><span data-stu-id="a649f-148">HOUR</span></span></p></td>
<td><p><span data-ttu-id="a649f-149">QUARTER</span><span class="sxs-lookup"><span data-stu-id="a649f-149">QUARTER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a649f-150">DAYOFMONTH</span><span class="sxs-lookup"><span data-stu-id="a649f-150">DAYOFMONTH</span></span></p></td>
<td><p><span data-ttu-id="a649f-151">MINUTE</span><span class="sxs-lookup"><span data-stu-id="a649f-151">MINUTE</span></span></p></td>
<td><p><span data-ttu-id="a649f-152">MONTHNAME</span><span class="sxs-lookup"><span data-stu-id="a649f-152">MONTHNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a649f-153">DAYOFWEEK</span><span class="sxs-lookup"><span data-stu-id="a649f-153">DAYOFWEEK</span></span></p></td>
<td><p><span data-ttu-id="a649f-154">SECOND</span><span class="sxs-lookup"><span data-stu-id="a649f-154">SECOND</span></span></p></td>
<td><p><span data-ttu-id="a649f-155">DAYNAME</span><span class="sxs-lookup"><span data-stu-id="a649f-155">DAYNAME</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="data-type-conversion"></a><span data-ttu-id="a649f-156">Datentypkonvertierung</span><span class="sxs-lookup"><span data-stu-id="a649f-156">Data Type Conversion</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a649f-157">CONVERT</span><span class="sxs-lookup"><span data-stu-id="a649f-157">CONVERT</span></span></p></td>
<td><p><span data-ttu-id="a649f-158">Zeichenfolgenliterale können in folgende Datentypen konvertiert werden: SQL_FLOAT, SQL_DOUBLE, SQL_NUMERIC, SQL_INTEGER, SQL_REAL, SQL_SMALLINT, SQL_VARCHAR und SQL_DATETIME.</span><span class="sxs-lookup"><span data-stu-id="a649f-158">String literals can be converted to the following data types: SQL_FLOAT, SQL_DOUBLE, SQL_NUMERIC, SQL_INTEGER, SQL_REAL, SQL_SMALLINT, SQL_VARCHAR and SQL_DATETIME.</span></span></p></td>
</tr>
</tbody>
</table>

