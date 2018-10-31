---
title: Aggregatfunktion, die CALC-Funktion und das NEW-Schlüsselwort
TOCTitle: Aggregate Functions, the CALC Function, and the NEW Keyword
ms:assetid: c91fef19-bf41-8d04-f195-5470fb18393f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249977(v=office.15)
ms:contentKeyID: 48547669
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8250d2a21f0c4a4d5af64310fc14f96f56a46b54
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860014"
---
# <a name="aggregate-functions-the-calc-function-and-the-new-keyword"></a><span data-ttu-id="41f03-102">Aggregatfunktion, die CALC-Funktion und das NEW-Schlüsselwort</span><span class="sxs-lookup"><span data-stu-id="41f03-102">Aggregate Functions, the CALC Function, and the NEW Keyword</span></span>


<span data-ttu-id="41f03-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="41f03-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="41f03-p101">Die Datenstrukturierung unterstützt die folgenden Funktionen. Der Name, der dem Kapitel mit der zu bearbeitenden Spalte zugewiesen wird, ist der *Kapitelalias*.</span><span class="sxs-lookup"><span data-stu-id="41f03-p101">Data shaping supports the following functions. The name assigned to the chapter containing the column to be operated on is the *chapter-alias*.</span></span>

<span data-ttu-id="41f03-p102">Ein Kapitelalias kann vollqualifiziert sein und aus den verschiedenen Kapitelspaltennamen bestehen, die zu dem jeweiligen Kapitel führen, das den Spaltennamen enthält, wobei alle Elemente durch Punkte voneinander getrennt werden. Wenn z. B. das übergeordnete Kapitel chap1 das untergeordnete Kapitel chap2 mit einer Spalte für den Betrag (amt) enthält, würde der qualifizierte Name chap1.chap2.amt lauten.</span><span class="sxs-lookup"><span data-stu-id="41f03-p102">A chapter-alias may be fully qualified, consisting of each chapter column name leading to the chapter containing the *column-name,* all separated by periods. For example, if the parent chapter, chap1, contains a child chapter, chap2, that has an amount column, amt, then the qualified name would be chap1.chap2.amt.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="41f03-108">Aggregatfunktionen</span><span class="sxs-lookup"><span data-stu-id="41f03-108">Aggregate Functions</span></span></p></th>
<th><p><span data-ttu-id="41f03-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="41f03-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="41f03-110">SUM (<em>Kapitel-Alias</em>.<em> Spaltenname</em>)</span><span class="sxs-lookup"><span data-stu-id="41f03-110">SUM(<em>chapter-alias</em>.<em>column-name</em>)</span></span></p></td>
<td><p><span data-ttu-id="41f03-111">Berechnet die Summe aller Werte in der angegebenen Spalte.</span><span class="sxs-lookup"><span data-stu-id="41f03-111">Calculates the sum of all values in the specified column.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="41f03-112">AVG (<em>Kapitel-Alias</em>.<em> Spaltenname</em>)</span><span class="sxs-lookup"><span data-stu-id="41f03-112">AVG(<em>chapter-alias</em>.<em>column-name</em>)</span></span></p></td>
<td><p><span data-ttu-id="41f03-113">Berechnet den Mittelwert aller Werte in der angegebenen Spalte.</span><span class="sxs-lookup"><span data-stu-id="41f03-113">Calculates the average of all values in the specified column.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="41f03-114">MAX (<em>Kapitel-Alias</em>.<em> Spaltenname</em>)</span><span class="sxs-lookup"><span data-stu-id="41f03-114">MAX(<em>chapter-alias</em>.<em>column-name</em>)</span></span></p></td>
<td><p><span data-ttu-id="41f03-115">Berechnet den Maximalwert in der angegebenen Spalte.</span><span class="sxs-lookup"><span data-stu-id="41f03-115">Calculates the maximum value in the specified column.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="41f03-116">MIN (<em>Kapitel-Alias</em>.<em> Spaltenname</em>)</span><span class="sxs-lookup"><span data-stu-id="41f03-116">MIN(<em>chapter-alias</em>.<em>column-name</em>)</span></span></p></td>
<td><p><span data-ttu-id="41f03-117">Berechnet den Minimalwert in der angegebenen Spalte.</span><span class="sxs-lookup"><span data-stu-id="41f03-117">Calculates the minimum value in the specified column.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="41f03-118">COUNT (<em>Kapitel-Alias</em>[.<em> Spaltenname</em>])</span><span class="sxs-lookup"><span data-stu-id="41f03-118">COUNT(<em>chapter-alias</em>[.<em>column-name</em>])</span></span></p></td>
<td><p><span data-ttu-id="41f03-p103">Berechnet die Anzahl von Zeilen im angegebenen Alias. Falls eine Spalte angegeben wird, werden nur Zeilen, für die diese Spalte ungleich NULL ist, in die Anzahl eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="41f03-p103">Counts the number of rows in the specified alias. If a column is specified, only rows for which that column is non-Null are included in the count.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="41f03-121">STDEV (<em>Kapitel-Alias</em>.<em> Spaltenname</em>)</span><span class="sxs-lookup"><span data-stu-id="41f03-121">STDEV(<em>chapter-alias</em>.<em>column-name</em>)</span></span></p></td>
<td><p><span data-ttu-id="41f03-122">Berechnet die Standardabweichung in der angegebenen Spalte.</span><span class="sxs-lookup"><span data-stu-id="41f03-122">Calculates the standard deviation in the specified column.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="41f03-123">Alle (<em>Kapitel-Alias</em>.<em> Spaltenname</em>)</span><span class="sxs-lookup"><span data-stu-id="41f03-123">ANY(<em>chapter-alias</em>.<em>column-name</em>)</span></span></p></td>
<td><p><span data-ttu-id="41f03-p104">Ein Wert der angegebenen Spalte. ANY hat nur dann einen vorhersagbaren Wert, wenn der Wert der Spalte für alle Zeilen im Kapitel identisch ist.
</span><span class="sxs-lookup"><span data-stu-id="41f03-p104">A value of the specified column. ANY has a predictable value only when the value of the column is the same for all rows in the chapter.</span></span></p>

> [!NOTE]
> <span data-ttu-id="41f03-126">Enthält die Spalte nicht denselben Wert für alle Zeilen im Kapitel, gibt der SHAPE-Befehl nach dem Zufallsprinzip einen der Werte als Wert der ANY-Funktion zurück.</span><span class="sxs-lookup"><span data-stu-id="41f03-126">If the column does not contain the same value for all of the rows in the chapter, the SHAPE command arbitrarily returns one of the values to be the value of the ANY function.</span></span>


<p></p></td>
</tr>
</tbody>
</table>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="41f03-127">Berechneter Ausdruck</span><span class="sxs-lookup"><span data-stu-id="41f03-127">Calculated expression</span></span></p></th>
<th><p><span data-ttu-id="41f03-128">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="41f03-128">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="41f03-129">CALC(<em>Ausdruck</em>)</span><span class="sxs-lookup"><span data-stu-id="41f03-129">CALC(<em>expression</em>)</span></span></p></td>
<td><p><span data-ttu-id="41f03-p105">Berechnet einen beliebigen Ausdruck, jedoch nur in der Zeile des <strong>Recordset</strong>-Objekts, das die CALC-Funktion enthält. Jeder Ausdruck, der diese <a href="visual-basic-for-applications-functions.md">VIA-Funktionen (Visual Basic für Applikationen)</a> verwendet, ist zulässig.</span><span class="sxs-lookup"><span data-stu-id="41f03-p105">Calculates an arbitrary expression, but only on the row of the <strong>Recordset</strong> containing the CALC function. Any expression using these <a href="visual-basic-for-applications-functions.md">Visual Basic for Applications (VBA) Functions</a> is allowed.</span></span></p></td>
</tr>
</tbody>
</table>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="41f03-132">NEW-Schlüsselwort</span><span class="sxs-lookup"><span data-stu-id="41f03-132">NEW keyword</span></span></p></th>
<th><p><span data-ttu-id="41f03-133">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="41f03-133">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="41f03-134">NEW <em>Feldtyp</em> [(<em>Breite</em> | <em>Skalierung</em> | <em>Genauigkeit</em> | <em>Fehler</em> [, <em>Scale</em> | <em>Fehler</em>])]</span><span class="sxs-lookup"><span data-stu-id="41f03-134">NEW <em>field-type</em> [(<em>width</em> | <em>scale</em> | <em>precision</em> | <em>error</em> [, <em>scale</em> | <em>error</em>])]</span></span></p></td>
<td><p><span data-ttu-id="41f03-135">Fügt dem <strong>Recordset</strong> eine leere Spalte des angegebenen Typs hinzu.</span><span class="sxs-lookup"><span data-stu-id="41f03-135">Adds an empty column of the specified type to the <strong>Recordset</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="41f03-136">Für den mit dem NEW-Schlüsselwort übergebenen *Feldtyp* sind die folgenden Datentypen möglich.</span><span class="sxs-lookup"><span data-stu-id="41f03-136">The *field-type* passed with the NEW keyword can be any of the following data types.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="41f03-137">OLE DB-Datentypen</span><span class="sxs-lookup"><span data-stu-id="41f03-137">OLE DB data types</span></span></p></th>
<th><p><span data-ttu-id="41f03-138">ADO-Datentypentsprechung(en)</span><span class="sxs-lookup"><span data-stu-id="41f03-138">ADO data type equivalent(s)</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="41f03-139">DBTYPE_BSTR</span><span class="sxs-lookup"><span data-stu-id="41f03-139">DBTYPE_BSTR</span></span></p></td>
<td><p><span data-ttu-id="41f03-140">adBSTR</span><span class="sxs-lookup"><span data-stu-id="41f03-140">adBSTR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="41f03-141">DBTYPE_BOOL</span><span class="sxs-lookup"><span data-stu-id="41f03-141">DBTYPE_BOOL</span></span></p></td>
<td><p><span data-ttu-id="41f03-142">adBoolean</span><span class="sxs-lookup"><span data-stu-id="41f03-142">adBoolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="41f03-143">DBTYPE_DECIMAL</span><span class="sxs-lookup"><span data-stu-id="41f03-143">DBTYPE_DECIMAL</span></span></p></td>
<td><p><span data-ttu-id="41f03-144">adDecimal</span><span class="sxs-lookup"><span data-stu-id="41f03-144">adDecimal</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="41f03-145">DBTYPE_UI1</span><span class="sxs-lookup"><span data-stu-id="41f03-145">DBTYPE_UI1</span></span></p></td>
<td><p><span data-ttu-id="41f03-146">adUnsignedTinyInt</span><span class="sxs-lookup"><span data-stu-id="41f03-146">adUnsignedTinyInt</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="41f03-147">DBTYPE_I1</span><span class="sxs-lookup"><span data-stu-id="41f03-147">DBTYPE_I1</span></span></p></td>
<td><p><span data-ttu-id="41f03-148">adTinyInt</span><span class="sxs-lookup"><span data-stu-id="41f03-148">adTinyInt</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="41f03-149">DBTYPE_UI2</span><span class="sxs-lookup"><span data-stu-id="41f03-149">DBTYPE_UI2</span></span></p></td>
<td><p><span data-ttu-id="41f03-150">adUnsignedSmallInt</span><span class="sxs-lookup"><span data-stu-id="41f03-150">adUnsignedSmallInt</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="41f03-151">DBTYPE_UI4</span><span class="sxs-lookup"><span data-stu-id="41f03-151">DBTYPE_UI4</span></span></p></td>
<td><p><span data-ttu-id="41f03-152">adUnsignedInt</span><span class="sxs-lookup"><span data-stu-id="41f03-152">adUnsignedInt</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="41f03-153">DBTYPE_I8</span><span class="sxs-lookup"><span data-stu-id="41f03-153">DBTYPE_I8</span></span></p></td>
<td><p><span data-ttu-id="41f03-154">adBigInt</span><span class="sxs-lookup"><span data-stu-id="41f03-154">adBigInt</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="41f03-155">DBTYPE_UI8</span><span class="sxs-lookup"><span data-stu-id="41f03-155">DBTYPE_UI8</span></span></p></td>
<td><p><span data-ttu-id="41f03-156">adUnsignedBigInt</span><span class="sxs-lookup"><span data-stu-id="41f03-156">adUnsignedBigInt</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="41f03-157">DBTYPE_GUID</span><span class="sxs-lookup"><span data-stu-id="41f03-157">DBTYPE_GUID</span></span></p></td>
<td><p><span data-ttu-id="41f03-158">adGuid</span><span class="sxs-lookup"><span data-stu-id="41f03-158">adGuid</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="41f03-159">DBTYPE_BYTES</span><span class="sxs-lookup"><span data-stu-id="41f03-159">DBTYPE_BYTES</span></span></p></td>
<td><p><span data-ttu-id="41f03-160">AdBinary, AdVarBinary, adLongVarBinary</span><span class="sxs-lookup"><span data-stu-id="41f03-160">adBinary, AdVarBinary, adLongVarBinary</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="41f03-161">DBTYPE_STR</span><span class="sxs-lookup"><span data-stu-id="41f03-161">DBTYPE_STR</span></span></p></td>
<td><p><span data-ttu-id="41f03-162">AdChar, AdVarChar, adLongVarChar</span><span class="sxs-lookup"><span data-stu-id="41f03-162">adChar, adVarChar, adLongVarChar</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="41f03-163">DBTYPE_WSTR</span><span class="sxs-lookup"><span data-stu-id="41f03-163">DBTYPE_WSTR</span></span></p></td>
<td><p><span data-ttu-id="41f03-164">AdWChar, AdVarWChar, adLongVarWChar</span><span class="sxs-lookup"><span data-stu-id="41f03-164">adWChar, adVarWChar, adLongVarWChar</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="41f03-165">DBTYPE_NUMERIC</span><span class="sxs-lookup"><span data-stu-id="41f03-165">DBTYPE_NUMERIC</span></span></p></td>
<td><p><span data-ttu-id="41f03-166">adNumeric</span><span class="sxs-lookup"><span data-stu-id="41f03-166">adNumeric</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="41f03-167">DBTYPE_DBDATE</span><span class="sxs-lookup"><span data-stu-id="41f03-167">DBTYPE_DBDATE</span></span></p></td>
<td><p><span data-ttu-id="41f03-168">adDBDate</span><span class="sxs-lookup"><span data-stu-id="41f03-168">adDBDate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="41f03-169">DBTYPE_DBTIME</span><span class="sxs-lookup"><span data-stu-id="41f03-169">DBTYPE_DBTIME</span></span></p></td>
<td><p><span data-ttu-id="41f03-170">adDBTime</span><span class="sxs-lookup"><span data-stu-id="41f03-170">adDBTime</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="41f03-171">DBTYPE_DBTIMESTAMP</span><span class="sxs-lookup"><span data-stu-id="41f03-171">DBTYPE_DBTIMESTAMP</span></span></p></td>
<td><p><span data-ttu-id="41f03-172">adDBTimeStamp</span><span class="sxs-lookup"><span data-stu-id="41f03-172">adDBTimeStamp</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="41f03-173">DBTYPE_VARNUMERIC ENTSPRECHENDE</span><span class="sxs-lookup"><span data-stu-id="41f03-173">DBTYPE_VARNUMERIC</span></span></p></td>
<td><p><span data-ttu-id="41f03-174">adVarNumeric</span><span class="sxs-lookup"><span data-stu-id="41f03-174">adVarNumeric</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="41f03-175">DBTYPE_FILETIME</span><span class="sxs-lookup"><span data-stu-id="41f03-175">DBTYPE_FILETIME</span></span></p></td>
<td><p><span data-ttu-id="41f03-176">adFileTime</span><span class="sxs-lookup"><span data-stu-id="41f03-176">adFileTime</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="41f03-177">DBTYPE_ERROR</span><span class="sxs-lookup"><span data-stu-id="41f03-177">DBTYPE_ERROR</span></span></p></td>
<td><p><span data-ttu-id="41f03-178">adError</span><span class="sxs-lookup"><span data-stu-id="41f03-178">adError</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="41f03-179">Wenn das neue Feld vom Typ Decimal ist (in OLE DB DATENBANKTYP\_Dezimal oder AdDecimal in ADO), müssen Sie die Genauigkeit und einem festen Maßstab Werte angeben.</span><span class="sxs-lookup"><span data-stu-id="41f03-179">When the new field is of type decimal (in OLE DB, DBTYPE\_DECIMAL, or in ADO, adDecimal), you must specify the precision and scale values.</span></span>

