---
title: Recordset.FindNext-Methode (DAO)
TOCTitle: FindNext Method
ms:assetid: 5457dfc8-e561-5624-74d0-34278ba2e7cb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194099(v=office.15)
ms:contentKeyID: 48544893
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: a9ef8f1714244b02ed5423a38cf3fb8fa328ec1e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699268"
---
# <a name="recordsetfindnext-method-dao"></a><span data-ttu-id="52b27-102">Recordset.FindNext-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="52b27-102">Recordset.FindNext method (DAO)</span></span>

<span data-ttu-id="52b27-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="52b27-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="52b27-104">Sucht den nächsten Datensatz in einem **[Recordset](recordset-object-dao.md)** -Objekt vom Typ Dynaset oder Snapshot, der den angegebenen Kriterien entspricht, und macht diesen Datensatz zum aktuellen Datensatz (gilt nur für Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="52b27-104">Locates the next record in a dynaset- or snapshot-type **[Recordset](recordset-object-dao.md)** object that satisfies the specified criteria and makes that record the current record (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="52b27-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="52b27-105">Syntax</span></span>

<span data-ttu-id="52b27-106">*Ausdruck* . FindNext (***Kriterien***)</span><span class="sxs-lookup"><span data-stu-id="52b27-106">*expression* .FindNext(***Criteria***)</span></span>

<span data-ttu-id="52b27-107">*Ausdruck* Eine Variable, die ein **Recordset** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="52b27-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="52b27-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="52b27-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="52b27-109">Name</span><span class="sxs-lookup"><span data-stu-id="52b27-109">Name</span></span></p></th>
<th><p><span data-ttu-id="52b27-110">Erforderlich oder optional</span><span class="sxs-lookup"><span data-stu-id="52b27-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="52b27-111">Datentyp</span><span class="sxs-lookup"><span data-stu-id="52b27-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="52b27-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="52b27-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="52b27-113"><em>Criteria</em></span><span class="sxs-lookup"><span data-stu-id="52b27-113"><em>Criteria</em></span></span></p></td>
<td><p><span data-ttu-id="52b27-114">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="52b27-114">Required</span></span></p></td>
<td><p><span data-ttu-id="52b27-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="52b27-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="52b27-p101">Eine Zeichenfolge, die zum Suchen des Datensatzes verwendet wird. Sie ähnelt der WHERE-Klausel in einer SQL-Anweisung, allerdings ohne das Wort WHERE.</span><span class="sxs-lookup"><span data-stu-id="52b27-p101">A String used to locate the record. It is like the WHERE clause in an SQL statement, but without the word WHERE.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="52b27-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="52b27-118">Remarks</span></span>

<span data-ttu-id="52b27-p102">Wenn Sie alle Datensätze in die Suche einschließen möchten (nicht nur die, die eine bestimmte Bedingung erfüllen), verwenden Sie die **Move** -Methoden, um zwischen Datensätzen zu wechseln. Um einen Datensatz in einem Tabellentyp- **Recordset** zu suchen, verwenden Sie die **Seek** -Methode.</span><span class="sxs-lookup"><span data-stu-id="52b27-p102">If you want to include all the records in your search — not just those that meet a specific condition — use the **Move** methods to move from record to record. To locate a record in a table-type **Recordset**, use the **Seek** method.</span></span>

<span data-ttu-id="52b27-p103">Wenn ein Datensatz, der die Bedingungen erfüllt, nicht gefunden wird, ist der aktuelle Datensatzverweis unbekannt und die **NoMatch** -Eigenschaft wird auf **True** festgelegt. Wenn das Recordset mehrere Datensätze enthält, die die Kriterien erfüllen, sucht **FindFirst** das erste Auftreten, **FindNext** sucht das nächste Auftreten usw.</span><span class="sxs-lookup"><span data-stu-id="52b27-p103">If a record matching the criteria isn't located, the current record pointer is unknown, and the **NoMatch** property is set to **True**. If recordset contains more than one record that satisfies the criteria, **FindFirst** locates the first occurrence, **FindNext** locates the next occurrence, and so on.</span></span>

<span data-ttu-id="52b27-123">Jede der **Find** -Methoden beginnt die Suche an der Position und in der Richtung, die in der folgenden Tabelle angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="52b27-123">Each of the **Find** methods begins its search from the location and in the direction specified in the following table.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="52b27-124">Find-Methode</span><span class="sxs-lookup"><span data-stu-id="52b27-124">Find method</span></span></p></th>
<th><p><span data-ttu-id="52b27-125">Beginnt die Suche bei</span><span class="sxs-lookup"><span data-stu-id="52b27-125">Begins searching at</span></span></p></th>
<th><p><span data-ttu-id="52b27-126">Suchrichtung</span><span class="sxs-lookup"><span data-stu-id="52b27-126">Search direction</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="52b27-127"><strong>FindFirst</strong></span><span class="sxs-lookup"><span data-stu-id="52b27-127"><strong>FindFirst</strong></span></span></p></td>
<td><p><span data-ttu-id="52b27-128">Anfang des Recordsets</span><span class="sxs-lookup"><span data-stu-id="52b27-128">Beginning of recordset</span></span></p></td>
<td><p><span data-ttu-id="52b27-129">Ende des Recordsets</span><span class="sxs-lookup"><span data-stu-id="52b27-129">End of recordset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52b27-130"><strong>FindLast</strong></span><span class="sxs-lookup"><span data-stu-id="52b27-130"><strong>FindLast</strong></span></span></p></td>
<td><p><span data-ttu-id="52b27-131">Ende des Recordsets</span><span class="sxs-lookup"><span data-stu-id="52b27-131">End of recordset</span></span></p></td>
<td><p><span data-ttu-id="52b27-132">Anfang des Recordsets</span><span class="sxs-lookup"><span data-stu-id="52b27-132">Beginning of recordset</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52b27-133"><strong>FindNext</strong></span><span class="sxs-lookup"><span data-stu-id="52b27-133"><strong>FindNext</strong></span></span></p></td>
<td><p><span data-ttu-id="52b27-134">Aktueller Datensatz</span><span class="sxs-lookup"><span data-stu-id="52b27-134">Current record</span></span></p></td>
<td><p><span data-ttu-id="52b27-135">Ende des Recordsets</span><span class="sxs-lookup"><span data-stu-id="52b27-135">End of recordset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52b27-136"><strong>FindPrevious</strong></span><span class="sxs-lookup"><span data-stu-id="52b27-136"><strong>FindPrevious</strong></span></span></p></td>
<td><p><span data-ttu-id="52b27-137">Aktueller Datensatz</span><span class="sxs-lookup"><span data-stu-id="52b27-137">Current record</span></span></p></td>
<td><p><span data-ttu-id="52b27-138">Anfang des Recordsets</span><span class="sxs-lookup"><span data-stu-id="52b27-138">Beginning of recordset</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="52b27-p104">Das Verwenden einer der **Find** -Methoden entspricht jedoch nicht dem Verwenden einer **Move** -Methode, die einfach den ersten, letzten, nächsten oder vorherigen Datensatz zum aktuellen Datensatz macht, ohne eine Bedingung anzugeben. Sie können auf einen Find-Vorgang einen Move-Vorgang folgen lassen.</span><span class="sxs-lookup"><span data-stu-id="52b27-p104">Using one of the **Find** methods isn't the same as using a **Move** method, however, which simply makes the first, last, next, or previous record current without specifying a condition. You can follow a Find operation with a Move operation.</span></span>

<span data-ttu-id="52b27-p105">Überprüfen Sie stets den Wert der **NoMatch** -Eigenschaft, um zu bestimmen, ob der Find-Vorgang erfolgreich war. Wenn die Suche erfolgreich ist, ist **NoMatch** **False**. Bei einem Fehler ist **NoMatch** **True**, und der aktuelle Datensatz ist nicht definiert. In diesem Fall müssen Sie den aktuellen Datensatzzeiger wieder auf einem gültigen Datensatz positionieren.</span><span class="sxs-lookup"><span data-stu-id="52b27-p105">Always check the value of the **NoMatch** property to determine whether the Find operation has succeeded. If the search succeeds, **NoMatch** is **False**. If it fails, **NoMatch** is **True** and the current record isn't defined. In this case, you must position the current record pointer back to a valid record.</span></span>

<span data-ttu-id="52b27-p106">Das Verwenden von **Find** -Methoden mit ODBC-Zugriffsrecordsets, die mit dem Microsoft Access-Datenbankmodul verbunden sind, kann ineffizient sein. Das Neuformulieren der Kriterien zum Suchen eines bestimmten Datensatzes kann schneller sein, besonders, wenn Sie mit großen Recordsets arbeiten.</span><span class="sxs-lookup"><span data-stu-id="52b27-p106">Using the **Find** methods with Microsoft Access database engine-connected ODBC-accessed recordsets can be inefficient. You may find that rephrasing your criteria to locate a specific record is faster, especially when working with large recordsets.</span></span>

<span data-ttu-id="52b27-p107">In einem ODBCDirect-Arbeitsbereich sind die **Find** - und **Seek** -Methoden nicht für jeden **Recordset** -Objekttyp verfügbar, da das Ausführen einer **Find** - oder **Seek** -Methode mit einer ODBC-Verbindung über das Netzwerk nicht sehr effizient ist. Stattdessen sollten Sie beim Abfrageentwurf (d. h. Verwenden des Arguments source für die **OpenRecordset** -Methode) eine entsprechende WHERE-Klausel einfügen, um nur die Datensätze zurückzugeben, die den Kriterien entsprechen, die Sie sonst in einer **Find** - oder **Seek** -Methode verwenden würden.</span><span class="sxs-lookup"><span data-stu-id="52b27-p107">In an ODBCDirect workspace, the **Find** and **Seek** methods are not available on any type of **Recordset** object, because executing a **Find** or **Seek** through an ODBC connection is not very efficient over the network. Instead, you should design the query (that is, using the source argument to the **OpenRecordset** method) with an appropriate WHERE clause that restricts the returned records to only those that meet the criteria you would otherwise use in a **Find** or **Seek** method.</span></span>

<span data-ttu-id="52b27-p108">Wenn Sie mit einem Microsoft Access-Datenbankmodul verbundene ODBC-Datenbanken sowie große Objekte vom Typ Dynaset verwenden, kann es sein, dass das Arbeiten mit den **Find** -Methoden oder den **Sort** - bzw. **Filter** -Eigenschaften langsam ist. Sie können die Leistung verbessern, indem Sie SQL-Abfragen mit benutzerdefinierten ORDER BY- oder WHERE-Klauseln, Parameterabfragen oder **QueryDef** -Objekte verwenden, die bestimmte indizierte Datensätze abrufen.</span><span class="sxs-lookup"><span data-stu-id="52b27-p108">When working with Microsoft Access database engine-connected ODBC databases and large dynaset-type v objects, you might discover that using the **Find** methods or using the **Sort** or **Filter** property is slow. To improve performance, use SQL queries with customized ORDER BY or WHERE clauses, parameter queries, or **QueryDef** objects that retrieve specific indexed records.</span></span>

<span data-ttu-id="52b27-p109">Auch wenn Sie nicht mit der US-Version des Microsoft Access-Datenbankmoduls arbeiten, sollten Sie bei der Suche nach Feldern mit Datumsangaben das US-Datumsformat (Monat-Tag-Jahr) verwenden, da die Daten sonst evtl. nicht gefunden werden. Mit der Visual Basic-Funktion **Format** können Sie das Datum konvertieren. Beispiel:</span><span class="sxs-lookup"><span data-stu-id="52b27-p109">You should use the U.S. date format (month-day-year) when you search for fields containing dates, even if you're not using the U.S. version of the Microsoft Access database engine; otherwise, the data may not be found. Use the Visual Basic **Format** function to convert the date. For example:</span></span>

```vb
    rstEmployees.FindFirst "HireDate > #" _ 
        & Format(mydate, 'm-d-yy' ) & "#" 
```

<span data-ttu-id="52b27-154">Wenn Kriterien besteht aus einer Zeichenfolge mit einem nicht-Integer-Wert verkettet und die Systemparameter einer US-decimal Zeichen wie etwa ein Komma angeben (beispielsweise StrSQL = "PRICE \> " &-LngPrice und LngPrice = 125,50), ein Fehler tritt auf, wenn Sie versuchen, Rufen Sie die-Methode.</span><span class="sxs-lookup"><span data-stu-id="52b27-154">If criteria is composed of a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strSQL = "PRICE \> " & lngPrice, and lngPrice = 125,50), an error occurs when you try to call the method.</span></span> <span data-ttu-id="52b27-155">Das geschieht, weil die Zahl während der Verkettung mithilfe des standardmäßigen Dezimalzeichens des Systems in eine Zeichenfolge konvertiert wird und Microsoft Access SQL nur US-amerikanische Dezimalzeichen akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="52b27-155">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and Microsoft Access SQL only accepts U.S. decimal characters.</span></span>

> [!NOTE]
> - <span data-ttu-id="52b27-156">Für eine optimale Leistung der *Kriterien* sollte entweder in das Formular "*Feld* = *Wert*", in dem *Feld* einem indizierten Feld befindet sich in der zugrunde liegenden Basistabelle oder "*Feld* wie *Präfix*", in *das Feld* ist, ein indizierte Feld in der zugrunde liegenden Basistabelle und das *Präfix* ist eine Suchzeichenfolge Präfix (beispielsweise "ClipArt \*").</span><span class="sxs-lookup"><span data-stu-id="52b27-156">For best performance, the *criteria* should be in either the form "*field* = *value*" where *field* is an indexed field in the underlying base table, or "*field* LIKE *prefix*" where *field* is an indexed field in the underlying base table and *prefix* is a prefix search string (for example, "ART\*").</span></span>
> 
> - <span data-ttu-id="52b27-p111">Allgemein stellt die **Seek**-Methode für ähnliche Suchtypen eine bessere Leistung als die **Find**-Methoden bereit. Dabei wird angenommen, dass nur Tabellentyp-**Recordset**-Objekte Ihre Anforderungen erfüllen können.</span><span class="sxs-lookup"><span data-stu-id="52b27-p111">In general, for equivalent types of searches, the **Seek** method provides better performance than the **Find** methods. This assumes that table-type **Recordset** objects alone can satisfy your needs.</span></span>


## <a name="example"></a><span data-ttu-id="52b27-159">Beispiel</span><span class="sxs-lookup"><span data-stu-id="52b27-159">Example</span></span>

<span data-ttu-id="52b27-160">Das folgende Beispiel zeigt das Verwenden der FindFirst- und FindNext-Methoden zum Suchen eines Datensatzes in einem Recordset.</span><span class="sxs-lookup"><span data-stu-id="52b27-160">The following example shows how to use the FindFirst and FindNext methods to find a record in a Recordset.</span></span>

<span data-ttu-id="52b27-161">**Beispielcode von** der [Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="52b27-161">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>


```vb
    Sub FindOrgName()
    
        Dim dbs As DAO.Database
        Dim rst As DAO.Recordset
        
        'Get the database and Recordset
        Set dbs = CurrentDb
        Set rst = dbs.OpenRecordset("tblCustomers")
    
        'Search for the first matching record   
        rst.FindFirst "[OrgName] LIKE '*parts*'"
        
        'Check the result
        If rst.NoMatch Then
            MsgBox "Record not found."
            GotTo Cleanup
        Else
            Do While Not rst.NoMatch
                MsgBox "Customer name: " & rst!CustName
                rst.FindNext "[OrgName] LIKE '*parts*'"
            Loop
    
            'Search for the next matching record
            rst.FindNext "[OrgName] LIKE '*parts*'"
        End If
       
        Cleanup:
            rst.Close
            Set rst = Nothing
            Set dbs = Nothing
    
    End Sub
```
