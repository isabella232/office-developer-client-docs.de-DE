---
title: Recordset2. FindPrevious-Methode (DAO)
TOCTitle: FindPrevious Method
ms:assetid: ec35faf4-20f2-a83f-54e4-ac1f66c3c2be
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836294(v=office.15)
ms:contentKeyID: 48548509
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9cf53526f9643737c7236bb2c98589e74f3f2eb5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307315"
---
# <a name="recordset2findprevious-method-dao"></a><span data-ttu-id="2e5d1-102">Recordset2. FindPrevious-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="2e5d1-102">Recordset2.FindPrevious method (DAO)</span></span>

<span data-ttu-id="2e5d1-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2e5d1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2e5d1-p101">Locates the previous record in a dynaset- or snapshot-type **[Recordset](recordset-object-dao.md)** object that satisfies the specified criteria and makes that record the current record (Microsoft Access workspaces only). .</span><span class="sxs-lookup"><span data-stu-id="2e5d1-p101">Locates the previous record in a dynaset- or snapshot-type **[Recordset](recordset-object-dao.md)** object that satisfies the specified criteria and makes that record the current record (Microsoft Access workspaces only). .</span></span>

## <a name="syntax"></a><span data-ttu-id="2e5d1-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="2e5d1-106">Syntax</span></span>

<span data-ttu-id="2e5d1-107">*Ausdruck* . FindPrevious (***Kriterien***)</span><span class="sxs-lookup"><span data-stu-id="2e5d1-107">*expression* .FindPrevious(***Criteria***)</span></span>

<span data-ttu-id="2e5d1-108">*Ausdruck* Eine Variable, die ein **Recordset2** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="2e5d1-108">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="2e5d1-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="2e5d1-109">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2e5d1-110">Name</span><span class="sxs-lookup"><span data-stu-id="2e5d1-110">Name</span></span></p></th>
<th><p><span data-ttu-id="2e5d1-111">Erforderlich/optional</span><span class="sxs-lookup"><span data-stu-id="2e5d1-111">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="2e5d1-112">Datentyp</span><span class="sxs-lookup"><span data-stu-id="2e5d1-112">Data type</span></span></p></th>
<th><p><span data-ttu-id="2e5d1-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2e5d1-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2e5d1-114"><em>Criteria</em></span><span class="sxs-lookup"><span data-stu-id="2e5d1-114"><em>Criteria</em></span></span></p></td>
<td><p><span data-ttu-id="2e5d1-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="2e5d1-115">Required</span></span></p></td>
<td><p><span data-ttu-id="2e5d1-116"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="2e5d1-116"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="2e5d1-p102">Eine Zeichenfolge, die zum Suchen des Datensatzes verwendet wird. Sie ähnelt der WHERE-Klausel in einer SQL-Anweisung, allerdings ohne das Wort WHERE.</span><span class="sxs-lookup"><span data-stu-id="2e5d1-p102">A String used to locate the record. It is like the WHERE clause in an SQL statement, but without the word WHERE.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="2e5d1-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2e5d1-119">Remarks</span></span>

<span data-ttu-id="2e5d1-p103">Wenn Sie alle Datensätze in die Suche einschließen möchten (nicht nur die, die eine bestimmte Bedingung erfüllen), verwenden Sie die **Move**-Methoden, um zwischen Datensätzen zu wechseln. Um einen Datensatz in einem Tabellentyp-**Recordset** zu suchen, verwenden Sie die **Seek**-Methode.</span><span class="sxs-lookup"><span data-stu-id="2e5d1-p103">If you want to include all the records in your search — not just those that meet a specific condition — use the **Move** methods to move from record to record. To locate a record in a table-type **Recordset**, use the **Seek** method.</span></span>

<span data-ttu-id="2e5d1-p104">Wenn ein Datensatz, der die Bedingungen erfüllt, nicht gefunden wird, ist der aktuelle Datensatzverweis unbekannt und die **NoMatch** -Eigenschaft wird auf **True** festgelegt. Wenn das Recordset mehrere Datensätze enthält, die die Kriterien erfüllen, sucht **FindFirst** das erste Auftreten, **FindNext** sucht das nächste Auftreten usw.</span><span class="sxs-lookup"><span data-stu-id="2e5d1-p104">If a record matching the criteria isn't located, the current record pointer is unknown, and the **NoMatch** property is set to **True**. If recordset contains more than one record that satisfies the criteria, **FindFirst** locates the first occurrence, **FindNext** locates the next occurrence, and so on.</span></span>

<span data-ttu-id="2e5d1-124">Jede der **Find**-Methoden beginnt die Suche an der Position und in der Richtung, die in der folgenden Tabelle angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="2e5d1-124">Each of the **Find** methods begins its search from the location and in the direction specified in the following table.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2e5d1-125">Find-Methode</span><span class="sxs-lookup"><span data-stu-id="2e5d1-125">Find method</span></span></p></th>
<th><p><span data-ttu-id="2e5d1-126">Suche ab</span><span class="sxs-lookup"><span data-stu-id="2e5d1-126">Begins searching at</span></span></p></th>
<th><p><span data-ttu-id="2e5d1-127">Suchrichtung</span><span class="sxs-lookup"><span data-stu-id="2e5d1-127">Search direction</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2e5d1-128"><strong>FindFirst</strong></span><span class="sxs-lookup"><span data-stu-id="2e5d1-128"><strong>FindFirst</strong></span></span></p></td>
<td><p><span data-ttu-id="2e5d1-129">Anfang des Recordsets</span><span class="sxs-lookup"><span data-stu-id="2e5d1-129">Beginning of recordset</span></span></p></td>
<td><p><span data-ttu-id="2e5d1-130">Ende der Datensatzgruppe</span><span class="sxs-lookup"><span data-stu-id="2e5d1-130">End of recordset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2e5d1-131"><strong>FindLast</strong></span><span class="sxs-lookup"><span data-stu-id="2e5d1-131"><strong>FindLast</strong></span></span></p></td>
<td><p><span data-ttu-id="2e5d1-132">Ende des Recordsets</span><span class="sxs-lookup"><span data-stu-id="2e5d1-132">End of recordset</span></span></p></td>
<td><p><span data-ttu-id="2e5d1-133">Beginn der Datensatzgruppe</span><span class="sxs-lookup"><span data-stu-id="2e5d1-133">Beginning of recordset</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2e5d1-134"><strong>FindNext</strong></span><span class="sxs-lookup"><span data-stu-id="2e5d1-134"><strong>FindNext</strong></span></span></p></td>
<td><p><span data-ttu-id="2e5d1-135">Aktueller Datensatz</span><span class="sxs-lookup"><span data-stu-id="2e5d1-135">Current record</span></span></p></td>
<td><p><span data-ttu-id="2e5d1-136">Ende der Datensatzgruppe</span><span class="sxs-lookup"><span data-stu-id="2e5d1-136">End of recordset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2e5d1-137"><strong>FindPrevious</strong></span><span class="sxs-lookup"><span data-stu-id="2e5d1-137"><strong>FindPrevious</strong></span></span></p></td>
<td><p><span data-ttu-id="2e5d1-138">Aktueller Datensatz</span><span class="sxs-lookup"><span data-stu-id="2e5d1-138">Current record</span></span></p></td>
<td><p><span data-ttu-id="2e5d1-139">Beginn der Datensatzgruppe</span><span class="sxs-lookup"><span data-stu-id="2e5d1-139">Beginning of recordset</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2e5d1-p105">Das Verwenden einer der **Find** -Methoden entspricht jedoch nicht dem Verwenden einer **Move** -Methode, die einfach den ersten, letzten, nächsten oder vorherigen Datensatz zum aktuellen Datensatz macht, ohne eine Bedingung anzugeben. Sie können auf einen Find-Vorgang einen Move-Vorgang folgen lassen.</span><span class="sxs-lookup"><span data-stu-id="2e5d1-p105">Using one of the **Find** methods isn't the same as using a **Move** method, however, which simply makes the first, last, next, or previous record current without specifying a condition. You can follow a Find operation with a Move operation.</span></span>

<span data-ttu-id="2e5d1-p106">Überprüfen Sie stets den Wert der **NoMatch** -Eigenschaft, um zu bestimmen, ob der Find-Vorgang erfolgreich war. Wenn die Suche erfolgreich ist, ist **NoMatch** **False**. Bei einem Fehler ist **NoMatch** **True**, und der aktuelle Datensatz ist nicht definiert. In diesem Fall müssen Sie den aktuellen Datensatzzeiger wieder auf einem gültigen Datensatz positionieren.</span><span class="sxs-lookup"><span data-stu-id="2e5d1-p106">Always check the value of the **NoMatch** property to determine whether the Find operation has succeeded. If the search succeeds, **NoMatch** is **False**. If it fails, **NoMatch** is **True** and the current record isn't defined. In this case, you must position the current record pointer back to a valid record.</span></span>

<span data-ttu-id="2e5d1-p107">Das Verwenden von **Find** -Methoden mit ODBC-Zugriffsrecordsets, die mit dem Microsoft Access-Datenbankmodul verbunden sind, kann ineffizient sein. Das Neuformulieren der Kriterien zum Suchen eines bestimmten Datensatzes kann schneller sein, besonders, wenn Sie mit großen Recordsets arbeiten.</span><span class="sxs-lookup"><span data-stu-id="2e5d1-p107">Using the **Find** methods with Microsoft Access database engine-connected ODBC-accessed recordsets can be inefficient. You may find that rephrasing your criteria to locate a specific record is faster, especially when working with large recordsets.</span></span>

<span data-ttu-id="2e5d1-p108">Wenn Sie mit ODBC-Zugriffsrecordsets, die mit dem Microsoft Access-Datenbankmodul verbunden sind, und großen **Recordset** -Objekten vom Typ "Dynaset" arbeiten, bemerken Sie möglicherweise, dass das Verwenden der **Find** -Methoden oder der **Sort** - oder **Filter** -Eigenschaft langsam ist. Um die Leistung zu verbessern, verwenden Sie SQL-Abfragen mit angepassten ORDER BY- oder WHERE-Klauseln, Parameterabfragen oder **QueryDef** -Objekten, die bestimmte indizierte Datensätze abrufen.</span><span class="sxs-lookup"><span data-stu-id="2e5d1-p108">When working with Microsoft Access database engine-connected ODBC databases and large dynaset-type **Recordset** objects, you might discover that using the **Find** methods or using the **Sort** or **Filter** property is slow. To improve performance, use SQL queries with customized ORDER BY or WHERE clauses, parameter queries, or **QueryDef** objects that retrieve specific indexed records.</span></span>

<span data-ttu-id="2e5d1-p109">Auch wenn Sie nicht mit der US-Version des Microsoft Access-Datenbankmoduls arbeiten, sollten Sie bei der Suche nach Feldern mit Datumsangaben das US-Datumsformat (Monat-Tag-Jahr) verwenden, da die Daten sonst evtl. nicht gefunden werden. Mit der Visual Basic-Funktion **Format** können Sie das Datum konvertieren. Beispiel:</span><span class="sxs-lookup"><span data-stu-id="2e5d1-p109">You should use the U.S. date format (month-day-year) when you search for fields containing dates, even if you're not using the U.S. version of the Microsoft Access database engine; otherwise, the data may not be found. Use the Visual Basic **Format** function to convert the date. For example:</span></span>

```vb
rstEmployees.FindFirst "HireDate > #" _ 
        & Format(mydate, 'm-d-yy' ) & "#" 
```

<span data-ttu-id="2e5d1-153">Wenn criteria aus einer Zeichenfolge besteht, die mit einem nicht-ganzzahligen Wert verkettet ist, und die Systemparameter ein nicht-U. S. Decimal-Zeichen wie ein Komma (beispielsweise strSQL = " \> Price" & lngPrice und lngPrice = 125, 50) angeben, tritt ein Fehler auf, wenn Sie versuchen, Rufen Sie die Methode auf.</span><span class="sxs-lookup"><span data-stu-id="2e5d1-153">If criteria is composed of a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strSQL = "PRICE \> " & lngPrice, and lngPrice = 125,50), an error occurs when you try to call the method.</span></span> <span data-ttu-id="2e5d1-154">Der Grund ist, dass die Zahl bei der Verkettung mithilfe des Standarddezimalzeichens des Systems in eine Zeichenfolge umgewandelt wird und Microsoft Access SQL nur für die USA gültige Dezimalzeichen akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="2e5d1-154">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and Microsoft Access SQL only accepts U.S. decimal characters.</span></span>

> [!NOTE]
> - <span data-ttu-id="2e5d1-155">Um eine optimale Leistung zu erzielen, sollten die *Kriterien*\* entweder im Format "*Feldwert* = \**" enthalten sein, wobei *Field* ein indiziertes Feld in der zugrunde liegenden Basistabelle ist, oder "*Field\* like *prefix*", wobei *Field* ein indiziertes Feld in der zugrunde liegenden Basistabelle und dem *Präfix* ist eine Suchzeichenfolge für das Präfix (beispielsweise "Art \*").</span><span class="sxs-lookup"><span data-stu-id="2e5d1-155">For best performance, the *criteria*\* should be in either the form "*field* = *value*" where *field* is an indexed field in the underlying base table, or "*field* LIKE *prefix*" where *field* is an indexed field in the underlying base table and *prefix* is a prefix search string (for example, "ART\*").</span></span>
> - <span data-ttu-id="2e5d1-p111">In general, for equivalent types of searches, the **Seek** method provides better performance than the **Find** methods. This assumes that table-type **Recordset** objects alone can satisfy your needs.</span><span class="sxs-lookup"><span data-stu-id="2e5d1-p111">In general, for equivalent types of searches, the **Seek** method provides better performance than the **Find** methods. This assumes that table-type **Recordset** objects alone can satisfy your needs.</span></span>


