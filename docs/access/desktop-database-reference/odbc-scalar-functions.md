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
ms.openlocfilehash: f4a519f1853c0779777d59e6e6c314cbaaf60621
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25937456"
---
# <a name="odbc-scalar-functions"></a><span data-ttu-id="da606-102">ODBC-Skalarfunktionen</span><span class="sxs-lookup"><span data-stu-id="da606-102">ODBC Scalar Functions</span></span>


<span data-ttu-id="da606-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="da606-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="da606-104">Microsoft Access SQL unterstützt die Verwendung der ODBC definierten Syntax für Skalarfunktionen.</span><span class="sxs-lookup"><span data-stu-id="da606-104">Microsoft Access SQL supports the use of the ODBC defined syntax for scalar functions.</span></span> <span data-ttu-id="da606-105">Beispielsweise gibt die Abfrage</span><span class="sxs-lookup"><span data-stu-id="da606-105">For example, the query:</span></span>

<span data-ttu-id="da606-106">SELECT DAILYCLOSE, DAILYCHANGE FROM DAILYQUOTE WHERE {fn ABS(DAILYCHANGE)} \> 5</span><span class="sxs-lookup"><span data-stu-id="da606-106">SELECT DAILYCLOSE, DAILYCHANGE FROM DAILYQUOTE WHERE {fn ABS(DAILYCHANGE)} \> 5</span></span>

<span data-ttu-id="da606-107">alle Zeilen zurück, in denen der absolute Wert für die Preisänderung einer Aktie größer als fünf ist.</span><span class="sxs-lookup"><span data-stu-id="da606-107">Would return all rows where the absolute value of the change in the price of a stock was greater than five.</span></span>

<span data-ttu-id="da606-p102">Es wird eine Untermenge der über ODBC definierten Skalarfunktionen unterstützt. In der folgenden Tabelle sind die unterstützten Funktionen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="da606-p102">A subset of the ODBC defined scalar functions is supported. The following table lists the functions that are supported.</span></span>

<span data-ttu-id="da606-110">Eine Beschreibung der Argumente und eine ausführliche Erläuterung der Escapesyntax für INCLUDE-Funktionen in einer SQL-Anweisung finden Sie in der ODBC-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="da606-110">For a description of the arguments and a complete explanation of the escape syntax for including functions in a SQL statement, see the ODBC documentation.</span></span>

## <a name="string-functions"></a><span data-ttu-id="da606-111">Zeichenfolgenfunktionen</span><span class="sxs-lookup"><span data-stu-id="da606-111">String Functions</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="da606-112">ASCII</span><span class="sxs-lookup"><span data-stu-id="da606-112">ASCII</span></span></p></td>
<td><p><span data-ttu-id="da606-113">LENGTH</span><span class="sxs-lookup"><span data-stu-id="da606-113">LENGTH</span></span></p></td>
<td><p><span data-ttu-id="da606-114">RTRIM</span><span class="sxs-lookup"><span data-stu-id="da606-114">RTRIM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="da606-115">CHAR</span><span class="sxs-lookup"><span data-stu-id="da606-115">CHAR</span></span></p></td>
<td><p><span data-ttu-id="da606-116">LOCATE</span><span class="sxs-lookup"><span data-stu-id="da606-116">LOCATE</span></span></p></td>
<td><p><span data-ttu-id="da606-117">SPACE</span><span class="sxs-lookup"><span data-stu-id="da606-117">SPACE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="da606-118">CONCAT</span><span class="sxs-lookup"><span data-stu-id="da606-118">CONCAT</span></span></p></td>
<td><p><span data-ttu-id="da606-119">LTRIM</span><span class="sxs-lookup"><span data-stu-id="da606-119">LTRIM</span></span></p></td>
<td><p><span data-ttu-id="da606-120">SUBSTRING</span><span class="sxs-lookup"><span data-stu-id="da606-120">SUBSTRING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="da606-121">LCASE</span><span class="sxs-lookup"><span data-stu-id="da606-121">LCASE</span></span></p></td>
<td><p><span data-ttu-id="da606-122">RIGHT</span><span class="sxs-lookup"><span data-stu-id="da606-122">RIGHT</span></span></p></td>
<td><p><span data-ttu-id="da606-123">UCASE</span><span class="sxs-lookup"><span data-stu-id="da606-123">UCASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="da606-124">LEFT</span><span class="sxs-lookup"><span data-stu-id="da606-124">LEFT</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


## <a name="numeric-functions"></a><span data-ttu-id="da606-125">Numerische Funktionen</span><span class="sxs-lookup"><span data-stu-id="da606-125">Numeric Functions</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="da606-126">ABS</span><span class="sxs-lookup"><span data-stu-id="da606-126">ABS</span></span></p></td>
<td><p><span data-ttu-id="da606-127">FLOOR</span><span class="sxs-lookup"><span data-stu-id="da606-127">FLOOR</span></span></p></td>
<td><p><span data-ttu-id="da606-128">SIN</span><span class="sxs-lookup"><span data-stu-id="da606-128">SIN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="da606-129">ATAN</span><span class="sxs-lookup"><span data-stu-id="da606-129">ATAN</span></span></p></td>
<td><p><span data-ttu-id="da606-130">LOG</span><span class="sxs-lookup"><span data-stu-id="da606-130">LOG</span></span></p></td>
<td><p><span data-ttu-id="da606-131">SQRT</span><span class="sxs-lookup"><span data-stu-id="da606-131">SQRT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="da606-132">CEILING</span><span class="sxs-lookup"><span data-stu-id="da606-132">CEILING</span></span></p></td>
<td><p><span data-ttu-id="da606-133">POWER</span><span class="sxs-lookup"><span data-stu-id="da606-133">POWER</span></span></p></td>
<td><p><span data-ttu-id="da606-134">TAN</span><span class="sxs-lookup"><span data-stu-id="da606-134">TAN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="da606-135">COS</span><span class="sxs-lookup"><span data-stu-id="da606-135">COS</span></span></p></td>
<td><p><span data-ttu-id="da606-136">RAND</span><span class="sxs-lookup"><span data-stu-id="da606-136">RAND</span></span></p></td>
<td><p><span data-ttu-id="da606-137">MOD</span><span class="sxs-lookup"><span data-stu-id="da606-137">MOD</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="da606-138">EXP</span><span class="sxs-lookup"><span data-stu-id="da606-138">EXP</span></span></p></td>
<td><p><span data-ttu-id="da606-139">SIGN</span><span class="sxs-lookup"><span data-stu-id="da606-139">SIGN</span></span></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


## <a name="time--date-functions"></a><span data-ttu-id="da606-140">Uhrzeit- und Datumsfunktionen</span><span class="sxs-lookup"><span data-stu-id="da606-140">Time & Date Functions</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="da606-141">CURDATE</span><span class="sxs-lookup"><span data-stu-id="da606-141">CURDATE</span></span></p></td>
<td><p><span data-ttu-id="da606-142">DAYOFYEAR</span><span class="sxs-lookup"><span data-stu-id="da606-142">DAYOFYEAR</span></span></p></td>
<td><p><span data-ttu-id="da606-143">MONTH</span><span class="sxs-lookup"><span data-stu-id="da606-143">MONTH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="da606-144">CURTIME</span><span class="sxs-lookup"><span data-stu-id="da606-144">CURTIME</span></span></p></td>
<td><p><span data-ttu-id="da606-145">YEAR</span><span class="sxs-lookup"><span data-stu-id="da606-145">YEAR</span></span></p></td>
<td><p><span data-ttu-id="da606-146">WEEK</span><span class="sxs-lookup"><span data-stu-id="da606-146">WEEK</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="da606-147">NOW</span><span class="sxs-lookup"><span data-stu-id="da606-147">NOW</span></span></p></td>
<td><p><span data-ttu-id="da606-148">HOUR</span><span class="sxs-lookup"><span data-stu-id="da606-148">HOUR</span></span></p></td>
<td><p><span data-ttu-id="da606-149">QUARTER</span><span class="sxs-lookup"><span data-stu-id="da606-149">QUARTER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="da606-150">DAYOFMONTH</span><span class="sxs-lookup"><span data-stu-id="da606-150">DAYOFMONTH</span></span></p></td>
<td><p><span data-ttu-id="da606-151">MINUTE</span><span class="sxs-lookup"><span data-stu-id="da606-151">MINUTE</span></span></p></td>
<td><p><span data-ttu-id="da606-152">MONTHNAME</span><span class="sxs-lookup"><span data-stu-id="da606-152">MONTHNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="da606-153">DAYOFWEEK</span><span class="sxs-lookup"><span data-stu-id="da606-153">DAYOFWEEK</span></span></p></td>
<td><p><span data-ttu-id="da606-154">SECOND</span><span class="sxs-lookup"><span data-stu-id="da606-154">SECOND</span></span></p></td>
<td><p><span data-ttu-id="da606-155">DAYNAME</span><span class="sxs-lookup"><span data-stu-id="da606-155">DAYNAME</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="data-type-conversion"></a><span data-ttu-id="da606-156">Datentypkonvertierung</span><span class="sxs-lookup"><span data-stu-id="da606-156">Data Type Conversion</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="da606-157">CONVERT</span><span class="sxs-lookup"><span data-stu-id="da606-157">CONVERT</span></span></p></td>
<td><p><span data-ttu-id="da606-158">Zeichenfolgenliterale können in folgende Datentypen konvertiert werden: SQL_FLOAT, SQL_DOUBLE, SQL_NUMERIC, SQL_INTEGER, SQL_REAL, SQL_SMALLINT, SQL_VARCHAR und SQL_DATETIME.</span><span class="sxs-lookup"><span data-stu-id="da606-158">String literals can be converted to the following data types: SQL_FLOAT, SQL_DOUBLE, SQL_NUMERIC, SQL_INTEGER, SQL_REAL, SQL_SMALLINT, SQL_VARCHAR and SQL_DATETIME.</span></span></p></td>
</tr>
</tbody>
</table>

