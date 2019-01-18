---
title: Recordset2.FindPrevious-Methode (DAO)
TOCTitle: FindPrevious Method
ms:assetid: ec35faf4-20f2-a83f-54e4-ac1f66c3c2be
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836294(v=office.15)
ms:contentKeyID: 48548509
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9cf53526f9643737c7236bb2c98589e74f3f2eb5
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712113"
---
# <a name="recordset2findprevious-method-dao"></a><span data-ttu-id="e4c0d-102">Recordset2.FindPrevious-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="e4c0d-102">Recordset2.FindPrevious method (DAO)</span></span>

<span data-ttu-id="e4c0d-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e4c0d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e4c0d-p101">Sucht den vorherigen Datensatz in einem **[Recordset](recordset-object-dao.md)** -Objekt vom Typ "Dynaset" oder "Snapshot", der die angegebenen Kriterien erfüllt, und macht diesen Datensatz zum aktuellen Datensatz (nur Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="e4c0d-p101">Locates the previous record in a dynaset- or snapshot-type **[Recordset](recordset-object-dao.md)** object that satisfies the specified criteria and makes that record the current record (Microsoft Access workspaces only). .</span></span>

## <a name="syntax"></a><span data-ttu-id="e4c0d-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="e4c0d-106">Syntax</span></span>

<span data-ttu-id="e4c0d-107">*Ausdruck* . FindPrevious (***Kriterien***)</span><span class="sxs-lookup"><span data-stu-id="e4c0d-107">*expression* .FindPrevious(***Criteria***)</span></span>

<span data-ttu-id="e4c0d-108">*Ausdruck* Eine Variable, die ein **Recordset2** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="e4c0d-108">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="e4c0d-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="e4c0d-109">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e4c0d-110">Name</span><span class="sxs-lookup"><span data-stu-id="e4c0d-110">Name</span></span></p></th>
<th><p><span data-ttu-id="e4c0d-111">Erforderlich oder optional</span><span class="sxs-lookup"><span data-stu-id="e4c0d-111">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="e4c0d-112">Datentyp</span><span class="sxs-lookup"><span data-stu-id="e4c0d-112">Data type</span></span></p></th>
<th><p><span data-ttu-id="e4c0d-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e4c0d-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e4c0d-114"><em>Criteria</em></span><span class="sxs-lookup"><span data-stu-id="e4c0d-114"><em>Criteria</em></span></span></p></td>
<td><p><span data-ttu-id="e4c0d-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="e4c0d-115">Required</span></span></p></td>
<td><p><span data-ttu-id="e4c0d-116"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="e4c0d-116"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="e4c0d-p102">Eine Zeichenfolge, die zum Suchen des Datensatzes verwendet wird. Sie ähnelt der WHERE-Klausel in einer SQL-Anweisung, allerdings ohne das Wort WHERE.</span><span class="sxs-lookup"><span data-stu-id="e4c0d-p102">A String used to locate the record. It is like the WHERE clause in an SQL statement, but without the word WHERE.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="e4c0d-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e4c0d-119">Remarks</span></span>

<span data-ttu-id="e4c0d-p103">Wenn Sie alle Datensätze in die Suche einschließen möchten (nicht nur die, die eine bestimmte Bedingung erfüllen), verwenden Sie die **Move** -Methoden, um zwischen Datensätzen zu wechseln. Um einen Datensatz in einem Tabellentyp- **Recordset** zu suchen, verwenden Sie die **Seek** -Methode.</span><span class="sxs-lookup"><span data-stu-id="e4c0d-p103">If you want to include all the records in your search — not just those that meet a specific condition — use the **Move** methods to move from record to record. To locate a record in a table-type **Recordset**, use the **Seek** method.</span></span>

<span data-ttu-id="e4c0d-p104">Wenn ein Datensatz, der die Bedingungen erfüllt, nicht gefunden wird, ist der aktuelle Datensatzverweis unbekannt und die **NoMatch** -Eigenschaft wird auf **True** festgelegt. Wenn das Recordset mehrere Datensätze enthält, die die Kriterien erfüllen, sucht **FindFirst** das erste Auftreten, **FindNext** sucht das nächste Auftreten usw.</span><span class="sxs-lookup"><span data-stu-id="e4c0d-p104">If a record matching the criteria isn't located, the current record pointer is unknown, and the **NoMatch** property is set to **True**. If recordset contains more than one record that satisfies the criteria, **FindFirst** locates the first occurrence, **FindNext** locates the next occurrence, and so on.</span></span>

<span data-ttu-id="e4c0d-124">Jede der **Find** -Methoden beginnt die Suche an der Position und in der Richtung, die in der folgenden Tabelle angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="e4c0d-124">Each of the **Find** methods begins its search from the location and in the direction specified in the following table.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e4c0d-125">Find-Methode</span><span class="sxs-lookup"><span data-stu-id="e4c0d-125">Find method</span></span></p></th>
<th><p><span data-ttu-id="e4c0d-126">Beginnt die Suche bei</span><span class="sxs-lookup"><span data-stu-id="e4c0d-126">Begins searching at</span></span></p></th>
<th><p><span data-ttu-id="e4c0d-127">Suchrichtung</span><span class="sxs-lookup"><span data-stu-id="e4c0d-127">Search direction</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e4c0d-128"><strong>FindFirst</strong></span><span class="sxs-lookup"><span data-stu-id="e4c0d-128"><strong>FindFirst</strong></span></span></p></td>
<td><p><span data-ttu-id="e4c0d-129">Anfang des Recordsets</span><span class="sxs-lookup"><span data-stu-id="e4c0d-129">Beginning of recordset</span></span></p></td>
<td><p><span data-ttu-id="e4c0d-130">Ende des Recordsets</span><span class="sxs-lookup"><span data-stu-id="e4c0d-130">End of recordset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4c0d-131"><strong>FindLast</strong></span><span class="sxs-lookup"><span data-stu-id="e4c0d-131"><strong>FindLast</strong></span></span></p></td>
<td><p><span data-ttu-id="e4c0d-132">Ende des Recordsets</span><span class="sxs-lookup"><span data-stu-id="e4c0d-132">End of recordset</span></span></p></td>
<td><p><span data-ttu-id="e4c0d-133">Anfang des Recordsets</span><span class="sxs-lookup"><span data-stu-id="e4c0d-133">Beginning of recordset</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4c0d-134"><strong>FindNext</strong></span><span class="sxs-lookup"><span data-stu-id="e4c0d-134"><strong>FindNext</strong></span></span></p></td>
<td><p><span data-ttu-id="e4c0d-135">Aktueller Datensatz</span><span class="sxs-lookup"><span data-stu-id="e4c0d-135">Current record</span></span></p></td>
<td><p><span data-ttu-id="e4c0d-136">Ende des Recordsets</span><span class="sxs-lookup"><span data-stu-id="e4c0d-136">End of recordset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4c0d-137"><strong>FindPrevious</strong></span><span class="sxs-lookup"><span data-stu-id="e4c0d-137"><strong>FindPrevious</strong></span></span></p></td>
<td><p><span data-ttu-id="e4c0d-138">Aktueller Datensatz</span><span class="sxs-lookup"><span data-stu-id="e4c0d-138">Current record</span></span></p></td>
<td><p><span data-ttu-id="e4c0d-139">Anfang des Recordsets</span><span class="sxs-lookup"><span data-stu-id="e4c0d-139">Beginning of recordset</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e4c0d-p105">Das Verwenden einer der **Find** -Methoden entspricht jedoch nicht dem Verwenden einer **Move** -Methode, die einfach den ersten, letzten, nächsten oder vorherigen Datensatz zum aktuellen Datensatz macht, ohne eine Bedingung anzugeben. Sie können auf einen Find-Vorgang einen Move-Vorgang folgen lassen.</span><span class="sxs-lookup"><span data-stu-id="e4c0d-p105">Using one of the **Find** methods isn't the same as using a **Move** method, however, which simply makes the first, last, next, or previous record current without specifying a condition. You can follow a Find operation with a Move operation.</span></span>

<span data-ttu-id="e4c0d-p106">Überprüfen Sie stets den Wert der **NoMatch** -Eigenschaft, um zu bestimmen, ob der Find-Vorgang erfolgreich war. Wenn die Suche erfolgreich ist, ist **NoMatch** **False**. Bei einem Fehler ist **NoMatch** **True**, und der aktuelle Datensatz ist nicht definiert. In diesem Fall müssen Sie den aktuellen Datensatzzeiger wieder auf einem gültigen Datensatz positionieren.</span><span class="sxs-lookup"><span data-stu-id="e4c0d-p106">Always check the value of the **NoMatch** property to determine whether the Find operation has succeeded. If the search succeeds, **NoMatch** is **False**. If it fails, **NoMatch** is **True** and the current record isn't defined. In this case, you must position the current record pointer back to a valid record.</span></span>

<span data-ttu-id="e4c0d-p107">Das Verwenden von **Find** -Methoden mit ODBC-Zugriffsrecordsets, die mit dem Microsoft Access-Datenbankmodul verbunden sind, kann ineffizient sein. Das Neuformulieren der Kriterien zum Suchen eines bestimmten Datensatzes kann schneller sein, besonders, wenn Sie mit großen Recordsets arbeiten.</span><span class="sxs-lookup"><span data-stu-id="e4c0d-p107">Using the **Find** methods with Microsoft Access database engine-connected ODBC-accessed recordsets can be inefficient. You may find that rephrasing your criteria to locate a specific record is faster, especially when working with large recordsets.</span></span>

<span data-ttu-id="e4c0d-p108">Wenn Sie mit ODBC-Zugriffsrecordsets, die mit dem Microsoft Access-Datenbankmodul verbunden sind, und großen **Recordset** -Objekten vom Typ "Dynaset" arbeiten, bemerken Sie möglicherweise, dass das Verwenden der **Find** -Methoden oder der **Sort** - oder **Filter** -Eigenschaft langsam ist. Um die Leistung zu verbessern, verwenden Sie SQL-Abfragen mit angepassten ORDER BY- oder WHERE-Klauseln, Parameterabfragen oder **QueryDef** -Objekten, die bestimmte indizierte Datensätze abrufen.</span><span class="sxs-lookup"><span data-stu-id="e4c0d-p108">When working with Microsoft Access database engine-connected ODBC databases and large dynaset-type **Recordset** objects, you might discover that using the **Find** methods or using the **Sort** or **Filter** property is slow. To improve performance, use SQL queries with customized ORDER BY or WHERE clauses, parameter queries, or **QueryDef** objects that retrieve specific indexed records.</span></span>

<span data-ttu-id="e4c0d-p109">Sie sollten das amerikanische Datumsformat (Monat-Tag-Jahr) verwenden, wenn Sie nach Feldern mit Datumsangaben suchen, auch wenn Sie nicht die US-amerikanische Version des Microsoft Access-Datenbankmoduls verwenden. Andernfalls werden die Daten möglicherweise nicht gefunden. Verwenden Sie die **Format** -Funktion von Visual Basic, um das Datum zu konvertieren. Beispiel:</span><span class="sxs-lookup"><span data-stu-id="e4c0d-p109">You should use the U.S. date format (month-day-year) when you search for fields containing dates, even if you're not using the U.S. version of the Microsoft Access database engine; otherwise, the data may not be found. Use the Visual Basic **Format** function to convert the date. For example:</span></span>

```vb
rstEmployees.FindFirst "HireDate > #" _ 
        & Format(mydate, 'm-d-yy' ) & "#" 
```

<span data-ttu-id="e4c0d-153">Wenn Kriterien besteht aus einer Zeichenfolge mit einem nicht-Integer-Wert verkettet und die Systemparameter einer US-decimal Zeichen wie etwa ein Komma angeben (beispielsweise StrSQL = "PRICE \> " &-LngPrice und LngPrice = 125,50), ein Fehler tritt auf, wenn Sie versuchen, Rufen Sie die-Methode.</span><span class="sxs-lookup"><span data-stu-id="e4c0d-153">If criteria is composed of a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strSQL = "PRICE \> " & lngPrice, and lngPrice = 125,50), an error occurs when you try to call the method.</span></span> <span data-ttu-id="e4c0d-154">Das geschieht, weil die Zahl während der Verkettung mithilfe des standardmäßigen Dezimalzeichens des Systems in eine Zeichenfolge konvertiert wird und Microsoft Access SQL nur US-amerikanische Dezimalzeichen akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="e4c0d-154">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and Microsoft Access SQL only accepts U.S. decimal characters.</span></span>

> [!NOTE]
> - <span data-ttu-id="e4c0d-155">Für eine optimale Leistung der *Kriterien*\* sollte das Formular in einem "*Feld* = *Wert*", in dem *Feld* einem indizierten Feld befindet sich in der zugrunde liegenden Basistabelle oder "*Feld* wie *Präfix*", in *das Feld* ist, ein indizierte Feld in der zugrunde liegenden Basistabelle und das *Präfix* ist eine Suchzeichenfolge Präfix (beispielsweise "ClipArt \*").</span><span class="sxs-lookup"><span data-stu-id="e4c0d-155">For best performance, the *criteria*\* should be in either the form "*field* = *value*" where *field* is an indexed field in the underlying base table, or "*field* LIKE *prefix*" where *field* is an indexed field in the underlying base table and *prefix* is a prefix search string (for example, "ART\*").</span></span>
> - <span data-ttu-id="e4c0d-p111">Allgemein stellt die **Seek**-Methode für ähnliche Suchtypen eine bessere Leistung als die **Find**-Methoden bereit. Dabei wird angenommen, dass nur Tabellentyp-**Recordset**-Objekte Ihre Anforderungen erfüllen können.</span><span class="sxs-lookup"><span data-stu-id="e4c0d-p111">In general, for equivalent types of searches, the **Seek** method provides better performance than the **Find** methods. This assumes that table-type **Recordset** objects alone can satisfy your needs.</span></span>


