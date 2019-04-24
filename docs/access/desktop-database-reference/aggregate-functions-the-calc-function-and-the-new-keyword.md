---
title: Aggregatfunktionen, die CALC-Funktion und das NEUE Schlüsselwort
TOCTitle: Aggregate functions, the CALC function, and the NEW keyword
ms:assetid: c91fef19-bf41-8d04-f195-5470fb18393f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249977(v=office.15)
ms:contentKeyID: 48547669
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 25f52489430465235a928fff3c38469ec6ba83ad
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297193"
---
# <a name="aggregate-functions-the-calc-function-and-the-new-keyword"></a><span data-ttu-id="e3d19-102">Aggregatfunktionen, die CALC-Funktion und das NEUE Schlüsselwort</span><span class="sxs-lookup"><span data-stu-id="e3d19-102">Aggregate functions, the CALC function, and the NEW keyword</span></span>


<span data-ttu-id="e3d19-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e3d19-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e3d19-104">Die Datenstrukturierung unterstützt die folgenden Funktionen.</span><span class="sxs-lookup"><span data-stu-id="e3d19-104">Data shaping supports the following functions.</span></span> <span data-ttu-id="e3d19-105">Der Name, der dem Kapitel mit der zu bearbeitenden Spalte zugewiesen wird, ist der *Kapitelalias*.</span><span class="sxs-lookup"><span data-stu-id="e3d19-105">The name assigned to the chapter containing the column to be operated on is the *chapter-alias*.</span></span>

<span data-ttu-id="e3d19-106">Ein Kapitel-Alias kann vollständig qualifiziert sein, bestehend aus jedem Kapitelspalten Namen, der zu dem Kapitel mit dem *Spaltennamen führt,* alle durch Punkte getrennt.</span><span class="sxs-lookup"><span data-stu-id="e3d19-106">A chapter-alias may be fully qualified, consisting of each chapter column name leading to the chapter containing the *column-name,* all separated by periods.</span></span> <span data-ttu-id="e3d19-107">For example, if the parent chapter, chap1, contains a child chapter, chap2, that has an amount column, amt, then the qualified name would be chap1.chap2.amt.</span><span class="sxs-lookup"><span data-stu-id="e3d19-107">For example, if the parent chapter, chap1, contains a child chapter, chap2, that has an amount column, amt, then the qualified name would be chap1.chap2.amt.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e3d19-108">Aggregatfunktionen</span><span class="sxs-lookup"><span data-stu-id="e3d19-108">Aggregate functions</span></span></p></th>
<th><p><span data-ttu-id="e3d19-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e3d19-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e3d19-110">SUM (<em>Kapitel-Alias</em>.<em> Spaltenname</em>)</span><span class="sxs-lookup"><span data-stu-id="e3d19-110">SUM(<em>chapter-alias</em>.<em>column-name</em>)</span></span></p></td>
<td><p><span data-ttu-id="e3d19-111">Berechnet die Summe aller Werte in der angegebenen Spalte.</span><span class="sxs-lookup"><span data-stu-id="e3d19-111">Calculates the sum of all values in the specified column.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3d19-112">AVG (<em>Kapitel-Alias</em>.<em> Spaltenname</em>)</span><span class="sxs-lookup"><span data-stu-id="e3d19-112">AVG(<em>chapter-alias</em>.<em>column-name</em>)</span></span></p></td>
<td><p><span data-ttu-id="e3d19-113">Berechnet den Mittelwert aller Werte in der angegebenen Spalte.</span><span class="sxs-lookup"><span data-stu-id="e3d19-113">Calculates the average of all values in the specified column.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3d19-114">MAX (<em>Kapitel-Alias</em>.<em> Spaltenname</em>)</span><span class="sxs-lookup"><span data-stu-id="e3d19-114">MAX(<em>chapter-alias</em>.<em>column-name</em>)</span></span></p></td>
<td><p><span data-ttu-id="e3d19-115">Berechnet den Maximalwert in der angegebenen Spalte.</span><span class="sxs-lookup"><span data-stu-id="e3d19-115">Calculates the maximum value in the specified column.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3d19-116">MIN (<em>Kapitel-Alias</em>.<em> Spaltenname</em>)</span><span class="sxs-lookup"><span data-stu-id="e3d19-116">MIN(<em>chapter-alias</em>.<em>column-name</em>)</span></span></p></td>
<td><p><span data-ttu-id="e3d19-117">Berechnet den Minimalwert in der angegebenen Spalte.</span><span class="sxs-lookup"><span data-stu-id="e3d19-117">Calculates the minimum value in the specified column.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3d19-118">COUNT (<em>Chapter-Alias</em>[.<em> Spaltenname</em>])</span><span class="sxs-lookup"><span data-stu-id="e3d19-118">COUNT(<em>chapter-alias</em>[.<em>column-name</em>])</span></span></p></td>
<td><p><span data-ttu-id="e3d19-p103">Berechnet die Anzahl von Zeilen im angegebenen Alias. Falls eine Spalte angegeben wird, werden nur Zeilen, für die diese Spalte ungleich NULL ist, in die Anzahl eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="e3d19-p103">Counts the number of rows in the specified alias. If a column is specified, only rows for which that column is non-Null are included in the count.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3d19-121">STDEV (<em>Kapitel-Alias</em>.<em> Spaltenname</em>)</span><span class="sxs-lookup"><span data-stu-id="e3d19-121">STDEV(<em>chapter-alias</em>.<em>column-name</em>)</span></span></p></td>
<td><p><span data-ttu-id="e3d19-122">Berechnet die Standardabweichung in der angegebenen Spalte.</span><span class="sxs-lookup"><span data-stu-id="e3d19-122">Calculates the standard deviation in the specified column.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3d19-123">ANY (<em>Kapitel-Alias</em>.<em> Spaltenname</em>)</span><span class="sxs-lookup"><span data-stu-id="e3d19-123">ANY(<em>chapter-alias</em>.<em>column-name</em>)</span></span></p></td>
<td><p><span data-ttu-id="e3d19-124">Ein Wert der angegebenen Spalte.</span><span class="sxs-lookup"><span data-stu-id="e3d19-124">A value of the specified column.</span></span> <span data-ttu-id="e3d19-125">ANY hat nur dann einen vorhersagbaren Wert, wenn der Wert der Spalte für alle Zeilen im Kapitel identisch ist.</span><span class="sxs-lookup"><span data-stu-id="e3d19-125">ANY has a predictable value only when the value of the column is the same for all rows in the chapter.</span></span></p><p><span data-ttu-id="e3d19-126"><strong>Hinweis</strong>: Wenn die Spalte nicht den gleichen Wert für alle Zeilen im Kapitel enthält, gibt der Shape-Befehl willkürlich einen der Werte als Wert der any-Funktion zurück.</span><span class="sxs-lookup"><span data-stu-id="e3d19-126"><strong>NOTE</strong>: If the column does not contain the same value for all of the rows in the chapter, the SHAPE command arbitrarily returns one of the values to be the value of the ANY function.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e3d19-127">Berechneter Ausdruck</span><span class="sxs-lookup"><span data-stu-id="e3d19-127">Calculated expression</span></span></p></th>
<th><p><span data-ttu-id="e3d19-128">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e3d19-128">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e3d19-129">CALC (<em>Ausdruck</em>)</span><span class="sxs-lookup"><span data-stu-id="e3d19-129">CALC(<em>expression</em>)</span></span></p></td>
<td><p><span data-ttu-id="e3d19-p105">Berechnet einen beliebigen Ausdruck, jedoch nur in der Zeile des <strong>Recordset</strong>-Objekts, das die CALC-Funktion enthält. Jeder Ausdruck, der diese <a href="visual-basic-for-applications-functions.md">VIA-Funktionen (Visual Basic für Applikationen)</a> verwendet, ist zulässig.</span><span class="sxs-lookup"><span data-stu-id="e3d19-p105">Calculates an arbitrary expression, but only on the row of the <strong>Recordset</strong> containing the CALC function. Any expression using these <a href="visual-basic-for-applications-functions.md">Visual Basic for Applications (VBA) Functions</a> is allowed.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e3d19-132">NEW-Schlüsselwort</span><span class="sxs-lookup"><span data-stu-id="e3d19-132">NEW keyword</span></span></p></th>
<th><p><span data-ttu-id="e3d19-133">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e3d19-133">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e3d19-134">Neuer <em>Feldtyp</em> [(<em></em> | <em></em> | <em></em> | <em>Fehler beim</em> Skalieren der Genauigkeit [, <em>Skalierungs</em> | <em>Fehler</em>])]</span><span class="sxs-lookup"><span data-stu-id="e3d19-134">NEW <em>field-type</em> [(<em>width</em> | <em>scale</em> | <em>precision</em> | <em>error</em> [, <em>scale</em> | <em>error</em>])]</span></span></p></td>
<td><p><span data-ttu-id="e3d19-135">Fügt dem <strong>Recordset</strong> eine leere Spalte des angegebenen Typs hinzu.</span><span class="sxs-lookup"><span data-stu-id="e3d19-135">Adds an empty column of the specified type to the <strong>Recordset</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="e3d19-136">Für den mit dem NEW-Schlüsselwort übergebenen *Feldtyp* sind die folgenden Datentypen möglich.</span><span class="sxs-lookup"><span data-stu-id="e3d19-136">The *field-type* passed with the NEW keyword can be any of the following data types.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e3d19-137">OLE DB-Datentypen</span><span class="sxs-lookup"><span data-stu-id="e3d19-137">OLE DB data types</span></span></p></th>
<th><p><span data-ttu-id="e3d19-138">ADO-Datentypentsprechung(en)</span><span class="sxs-lookup"><span data-stu-id="e3d19-138">ADO data type equivalent(s)</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e3d19-139">DBTYPE_BSTR</span><span class="sxs-lookup"><span data-stu-id="e3d19-139">DBTYPE_BSTR</span></span></p></td>
<td><p><span data-ttu-id="e3d19-140">-BSTR</span><span class="sxs-lookup"><span data-stu-id="e3d19-140">adBSTR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3d19-141">DBTYPE_BOOL</span><span class="sxs-lookup"><span data-stu-id="e3d19-141">DBTYPE_BOOL</span></span></p></td>
<td><p><span data-ttu-id="e3d19-142">Boolean</span><span class="sxs-lookup"><span data-stu-id="e3d19-142">adBoolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3d19-143">DBTYPE_DECIMAL</span><span class="sxs-lookup"><span data-stu-id="e3d19-143">DBTYPE_DECIMAL</span></span></p></td>
<td><p><span data-ttu-id="e3d19-144">adDecimal</span><span class="sxs-lookup"><span data-stu-id="e3d19-144">adDecimal</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3d19-145">DBTYPE_UI1</span><span class="sxs-lookup"><span data-stu-id="e3d19-145">DBTYPE_UI1</span></span></p></td>
<td><p><span data-ttu-id="e3d19-146">adUnsignedTinyInt</span><span class="sxs-lookup"><span data-stu-id="e3d19-146">adUnsignedTinyInt</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3d19-147">DBTYPE_I1</span><span class="sxs-lookup"><span data-stu-id="e3d19-147">DBTYPE_I1</span></span></p></td>
<td><p><span data-ttu-id="e3d19-148">addTinyInt</span><span class="sxs-lookup"><span data-stu-id="e3d19-148">adTinyInt</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3d19-149">DBTYPE_UI2</span><span class="sxs-lookup"><span data-stu-id="e3d19-149">DBTYPE_UI2</span></span></p></td>
<td><p><span data-ttu-id="e3d19-150">adUnsignedSmallInt</span><span class="sxs-lookup"><span data-stu-id="e3d19-150">adUnsignedSmallInt</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3d19-151">DBTYPE_UI4</span><span class="sxs-lookup"><span data-stu-id="e3d19-151">DBTYPE_UI4</span></span></p></td>
<td><p><span data-ttu-id="e3d19-152">adUnsignedInt</span><span class="sxs-lookup"><span data-stu-id="e3d19-152">adUnsignedInt</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3d19-153">DBTYPE_I8</span><span class="sxs-lookup"><span data-stu-id="e3d19-153">DBTYPE_I8</span></span></p></td>
<td><p><span data-ttu-id="e3d19-154">Bigint</span><span class="sxs-lookup"><span data-stu-id="e3d19-154">adBigInt</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3d19-155">DBTYPE_UI8</span><span class="sxs-lookup"><span data-stu-id="e3d19-155">DBTYPE_UI8</span></span></p></td>
<td><p><span data-ttu-id="e3d19-156">adUnsignedBigInt</span><span class="sxs-lookup"><span data-stu-id="e3d19-156">adUnsignedBigInt</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3d19-157">DBTYPE_GUID</span><span class="sxs-lookup"><span data-stu-id="e3d19-157">DBTYPE_GUID</span></span></p></td>
<td><p><span data-ttu-id="e3d19-158">GUID</span><span class="sxs-lookup"><span data-stu-id="e3d19-158">adGuid</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3d19-159">DBTYPE_BYTES</span><span class="sxs-lookup"><span data-stu-id="e3d19-159">DBTYPE_BYTES</span></span></p></td>
<td><p><span data-ttu-id="e3d19-160">adLongVarBinary</span><span class="sxs-lookup"><span data-stu-id="e3d19-160">adBinary, AdVarBinary, adLongVarBinary</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3d19-161">DBTYPE_STR</span><span class="sxs-lookup"><span data-stu-id="e3d19-161">DBTYPE_STR</span></span></p></td>
<td><p><span data-ttu-id="e3d19-162">adLongVarChar</span><span class="sxs-lookup"><span data-stu-id="e3d19-162">adChar, adVarChar, adLongVarChar</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3d19-163">DBTYPE_WSTR</span><span class="sxs-lookup"><span data-stu-id="e3d19-163">DBTYPE_WSTR</span></span></p></td>
<td><p><span data-ttu-id="e3d19-164">adWChar, adVarWChar, adLongVarWChar</span><span class="sxs-lookup"><span data-stu-id="e3d19-164">adWChar, adVarWChar, adLongVarWChar</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3d19-165">DBTYPE_NUMERIC</span><span class="sxs-lookup"><span data-stu-id="e3d19-165">DBTYPE_NUMERIC</span></span></p></td>
<td><p><span data-ttu-id="e3d19-166">adNumeric</span><span class="sxs-lookup"><span data-stu-id="e3d19-166">adNumeric</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3d19-167">DBTYPE_DBDATE</span><span class="sxs-lookup"><span data-stu-id="e3d19-167">DBTYPE_DBDATE</span></span></p></td>
<td><p><span data-ttu-id="e3d19-168">adDBDate</span><span class="sxs-lookup"><span data-stu-id="e3d19-168">adDBDate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3d19-169">DBTYPE_DBTIME</span><span class="sxs-lookup"><span data-stu-id="e3d19-169">DBTYPE_DBTIME</span></span></p></td>
<td><p><span data-ttu-id="e3d19-170">adDBTime</span><span class="sxs-lookup"><span data-stu-id="e3d19-170">adDBTime</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3d19-171">DBTYPE_DBTIMESTAMP</span><span class="sxs-lookup"><span data-stu-id="e3d19-171">DBTYPE_DBTIMESTAMP</span></span></p></td>
<td><p><span data-ttu-id="e3d19-172">adDBTimeStamp</span><span class="sxs-lookup"><span data-stu-id="e3d19-172">adDBTimeStamp</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3d19-173">DBTYPE_VARNUMERIC</span><span class="sxs-lookup"><span data-stu-id="e3d19-173">DBTYPE_VARNUMERIC</span></span></p></td>
<td><p><span data-ttu-id="e3d19-174">adVarNumeric</span><span class="sxs-lookup"><span data-stu-id="e3d19-174">adVarNumeric</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3d19-175">DBTYPE_FILETIME</span><span class="sxs-lookup"><span data-stu-id="e3d19-175">DBTYPE_FILETIME</span></span></p></td>
<td><p><span data-ttu-id="e3d19-176">Dateien</span><span class="sxs-lookup"><span data-stu-id="e3d19-176">adFileTime</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3d19-177">DBTYPE_ERROR</span><span class="sxs-lookup"><span data-stu-id="e3d19-177">DBTYPE_ERROR</span></span></p></td>
<td><p><span data-ttu-id="e3d19-178">Fehler</span><span class="sxs-lookup"><span data-stu-id="e3d19-178">adError</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e3d19-179">Wenn das neue Feld vom Typ Decimal (in OLE DB, DBTYPE\_Decimal oder in ADO, Decimal) ist, müssen Sie die Genauigkeit und die Skalierungswerte angeben.</span><span class="sxs-lookup"><span data-stu-id="e3d19-179">When the new field is of type decimal (in OLE DB, DBTYPE\_DECIMAL, or in ADO, adDecimal), you must specify the precision and scale values.</span></span>

