---
title: Database.OpenRecordset-Methode (DAO)
TOCTitle: OpenRecordset Method
ms:assetid: a243bc79-cac4-fe12-768d-d3d017954e78
ms:mtpsurl: https://msdn.microsoft.com/library/Ff820966(v=office.15)
ms:contentKeyID: 48546753
ms.date: 09/04/2019
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052939
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: b8a6e9a2204a60ecff33555d31f39591308f9b67
ms.sourcegitcommit: 27a9f3568318470e7ee09ad93a90c3f80d3ef0cd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2019
ms.locfileid: "36790764"
---
# <a name="databaseopenrecordset-method-dao"></a><span data-ttu-id="8b920-102">Database.OpenRecordset-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="8b920-102">Database.OpenRecordset method (DAO)</span></span>

<span data-ttu-id="8b920-103">**Gilt für:** Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="8b920-103">**Applies to:** Access 2013 | Office 2013</span></span>

<span data-ttu-id="8b920-104">Erstellt ein neues **[Recordset](recordset-object-dao.md)**-Objekt und fügt es an die **Recordsets**-Auflistung an.</span><span class="sxs-lookup"><span data-stu-id="8b920-104">Creates a new **[Recordset](recordset-object-dao.md)** object and appends it to the **Recordsets** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b920-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8b920-105">Syntax</span></span>

<span data-ttu-id="8b920-106">*Ausdruck*.**OpenRecordset** (_Name_, _ Typ_, _Optionen_, _LockEdit_)</span><span class="sxs-lookup"><span data-stu-id="8b920-106">*expression*.**OpenRecordset** (_Name_, _Type_, _Options_, _LockEdit_)</span></span>

<span data-ttu-id="8b920-107">*Ausdruck* Eine Variable, die ein **Database** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="8b920-107">*expression* A variable that represents a **Database** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="8b920-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="8b920-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8b920-109">Name</span><span class="sxs-lookup"><span data-stu-id="8b920-109">Name</span></span></p></th>
<th><p><span data-ttu-id="8b920-110">Erforderlich/optional</span><span class="sxs-lookup"><span data-stu-id="8b920-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="8b920-111">Datentyp</span><span class="sxs-lookup"><span data-stu-id="8b920-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="8b920-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8b920-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8b920-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="8b920-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="8b920-114">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="8b920-114">Required</span></span></p></td>
<td><p><span data-ttu-id="8b920-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="8b920-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="8b920-p101">Die Quelle der Datensätze für das neue  <strong>Recordset</strong>. Die Quelle kann ein Tabellenname, ein Abfragename oder eine SQL-Anweisung sein, die Datensätze zurückgibt. Für <strong>Recordset</strong>-Objekte vom "table"-Typ in Microsoft Access-Datenbankmodul-Datenbanken kann die Quelle nur ein Tabellenname sein.</span><span class="sxs-lookup"><span data-stu-id="8b920-p101">The source of the records for the new <strong>Recordset</strong>. The source can be a table name, a query name, or an SQL statement that returns records. For table-type <strong>Recordset</strong> objects in Microsoft Access database engine databases, the source can only be a table name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b920-119"><em>Typ</em></span><span class="sxs-lookup"><span data-stu-id="8b920-119"><em>Type</em></span></span></p></td>
<td><p><span data-ttu-id="8b920-120">Optional</span><span class="sxs-lookup"><span data-stu-id="8b920-120">Optional</span></span></p></td>
<td><p><span data-ttu-id="8b920-121"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="8b920-121"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="8b920-122">Eine <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong>-Konstante gibt den Typ des zu öffnenden <strong>Recordset</strong> an.</span><span class="sxs-lookup"><span data-stu-id="8b920-122">A <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong> constant that indicates the type of <strong>Recordset</strong> to open.</span></span></p><p><span data-ttu-id="8b920-123"><strong>Hinweis</strong>: Wenn Sie ein <strong>Recordset</strong> in einem Microsoft Access-Arbeitsbereich öffnen und keinen Typ angeben, erstellt <strong>OpenRecordset</strong>, wenn möglich, ein tabellenartiges <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="8b920-123"><strong>NOTE</strong>: If you open a <strong>Recordset</strong> in a Microsoft Access workspace and you don't specify a type, <strong>OpenRecordset</strong> creates a table-type <strong>Recordset</strong>, if possible.</span></span> <span data-ttu-id="8b920-124">If you specify a linked table or query, <strong>OpenRecordset</strong> creates a dynaset-type <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="8b920-124">If you specify a linked table or query, <strong>OpenRecordset</strong> creates a dynaset-type <strong>Recordset</strong>.</span></span></p>
</td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b920-125"><em>Optionen</em></span><span class="sxs-lookup"><span data-stu-id="8b920-125"><em>Options</em></span></span></p></td>
<td><p><span data-ttu-id="8b920-126">Optional</span><span class="sxs-lookup"><span data-stu-id="8b920-126">Optional</span></span></p></td>
<td><p><span data-ttu-id="8b920-127"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="8b920-127"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="8b920-128">Eine Kombination aus <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong>-Konstanten, die Merkmale des neuen <strong>Recordset</strong> angeben.</span><span class="sxs-lookup"><span data-stu-id="8b920-128">A combination of <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong> constants that specify characteristics of the new <strong>Recordset</strong>.</span></span></p><p><span data-ttu-id="8b920-129"><strong>Hinweis</strong>: Die Konstanten <strong>dbConsistent</strong> und <strong>dbInconsistent</strong>schließen sich gegenseitig aus, und die Verwendung beider verursacht einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="8b920-129"><strong>NOTE</strong>: The constants <strong>dbConsistent</strong> and <strong>dbInconsistent</strong> are mutually exclusive, and using both causes an error.</span></span> <span data-ttu-id="8b920-130">Das Bereitstellen eines LockEdit-Arguments, wenn Optionen die Konstante <strong>dbReadOnly</strong> verwendet, führt ebenfalls zu einem Fehler. </span><span class="sxs-lookup"><span data-stu-id="8b920-130">Supplying a LockEdit argument when Options uses the <strong>dbReadOnly</strong> constant also causes an error.</span></span></p>
</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b920-131"><em>LockEdit</em></span><span class="sxs-lookup"><span data-stu-id="8b920-131"><em>LockEdit</em></span></span></p></td>
<td><p><span data-ttu-id="8b920-132">Optional</span><span class="sxs-lookup"><span data-stu-id="8b920-132">Optional</span></span></p></td>
<td><p><span data-ttu-id="8b920-133"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="8b920-133"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="8b920-134">Eine <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong>-Konstante, die die Sperre für das <strong>Recordset</strong> bestimmt.</span><span class="sxs-lookup"><span data-stu-id="8b920-134">A <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong> constant that determines the locking for the <strong>Recordset</strong>.</span></span></p><p><span data-ttu-id="8b920-135"><strong>Hinweis</strong>: Sie können <strong>dbReadOnly</strong> im Options-Argument oder im LockedEdit-Argument verwenden, aber nicht in beiden.</span><span class="sxs-lookup"><span data-stu-id="8b920-135"><strong>NOTE</strong>: You can use <strong>dbReadOnly</strong> in either the Options argument or the LockedEdit argument, but not both.</span></span> <span data-ttu-id="8b920-136">Wenn Sie es für beide Argumente verwenden, tritt ein Laufzeitfehler auf.</span><span class="sxs-lookup"><span data-stu-id="8b920-136">If you use it for both arguments, a run-time error occurs.</span></span></p>
</td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="8b920-137">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8b920-137">Return value</span></span>

<span data-ttu-id="8b920-138">Recordset</span><span class="sxs-lookup"><span data-stu-id="8b920-138">Recordset</span></span>

## <a name="remarks"></a><span data-ttu-id="8b920-139">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8b920-139">Remarks</span></span>

<span data-ttu-id="8b920-p105">Wenn der Benutzer diesen Fehler beim Aktualisieren eines Datensatzes erhält, sollte Ihr Code normalerweise die Inhalte der Felder aktualisieren und die neu geänderten Werte abrufen. Wenn der Fehler beim Löschen eines Datensatzes auftritt, könnte Ihr Code dem Benutzer die neuen Datensatzdaten und eine Meldung anzeigen, dass die Daten kürzlich geändert wurden. An diesem Punkt kann Ihr Code eine Bestätigung anfordern, dass der Benutzer den Datensatz immer noch löschen möchte.</span><span class="sxs-lookup"><span data-stu-id="8b920-p105">Typically, if the user gets this error while updating a record, your code should refresh the contents of the fields and retrieve the newly modified values. If the error occurs while deleting a record, your code could display the new record data to the user and a message indicating that the data has recently changed. At this point, your code can request a confirmation that the user still wants to delete the record.</span></span>

<span data-ttu-id="8b920-143">Sie sollten auch die **dbSeeChanges**-Konstante verwenden, wenn Sie ein **Recordset** in einem ODBC-Arbeitsbereich mit verbundenem Microsoft Access-Datenbankmodul für eine Microsoft SQL Server 6.0-Tabelle (oder neuer) öffnen, die über eine  IDENTITY-Spalte verfügt. Andernfalls kann ein Fehler auftreten.</span><span class="sxs-lookup"><span data-stu-id="8b920-143">You should also use the **dbSeeChanges** constant if you open a **Recordset** in a Microsoft Access database engine-connected ODBC workspace against a Microsoft SQL Server 6.0 (or later) table that has an IDENTITY column, otherwise an error may result.</span></span>

<span data-ttu-id="8b920-p106">Wenn Sie mehr als ein **Recordset** in einer ODBC-Datenquelle öffnen, kann die Datenquelle ausfallen, da die Verbindung mit einem vorherigen **OpenRecordset**-Aufruf beschäftigt ist. Eine Lösungsmöglichkeit besteht im vollständigen Ausfüllen des **Recordset** mithilfe der **MoveLast**-Methode, sobald das **Recordset** geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="8b920-p106">Opening more than one **Recordset** on an ODBC data source may fail because the connection is busy with a prior **OpenRecordset** call. One way around this is to fully populate the **Recordset** by using the **MoveLast** method as soon as the **Recordset** is opened.</span></span>

<span data-ttu-id="8b920-146">Durch das Schließen eines **Recordset** mit der **[Close](connection-close-method-dao.md)**-Methode wird es automatisch aus der **Recordsets**-Auflistung gelöscht.</span><span class="sxs-lookup"><span data-stu-id="8b920-146">Closing a **Recordset** with the **[Close](connection-close-method-dao.md)** method automatically deletes it from the **Recordsets** collection.</span></span>


> [!NOTE]
> <span data-ttu-id="8b920-147">Wenn sich *source* auf eine SQL-Anweisung bezieht, die aus einer Zeichenfolge besteht, die mit einem nicht ganzzahligen Wert verkettet ist, und die Systemparameter ein nicht für die USA gültiges Dezimalzeichen, z. B. ein Komma, angeben (Beispiel: strSQL = "PRICE &gt; " &amp; lngPrice, und lngPrice = 125,50), tritt beim Versuch, das **Recordset** zu öffnen, ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="8b920-147">If *source* refers to an SQL statement composed of a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strSQL = "PRICE &gt; " &amp; lngPrice, and lngPrice = 125,50), an error occurs when you try to open the **Recordset**.</span></span> <span data-ttu-id="8b920-148">Der Grund ist, dass die Zahl bei der Verkettung mithilfe des Standarddezimalzeichens des Systems in eine Zeichenfolge umgewandelt wird und SQL nur für die USA gültige Dezimalzeichen akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="8b920-148">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and SQL only accepts U.S. decimal characters.</span></span>

<span data-ttu-id="8b920-149">\*\*Link zur Verfügung gestellt von: \*\* [UtterAccess](https://www.utteraccess.com)-Community.</span><span class="sxs-lookup"><span data-stu-id="8b920-149">**Link provided by** the [UtterAccess](https://www.utteraccess.com) community.</span></span> <span data-ttu-id="8b920-150">UtterAccess ist das führende Microsoft Access-Wiki und -Hilfeforum.</span><span class="sxs-lookup"><span data-stu-id="8b920-150">UtterAccess is the premier Microsoft Access wiki and help forum.</span></span>

- [<span data-ttu-id="8b920-151">Übertragen von Daten aus Access in Excel</span><span class="sxs-lookup"><span data-stu-id="8b920-151">Transfer data from Access to Excel</span></span>](https://www.utteraccess.com/forum/transfer-data-access-ex-t1672619.html)

## <a name="example"></a><span data-ttu-id="8b920-152">Beispiel</span><span class="sxs-lookup"><span data-stu-id="8b920-152">Example</span></span>

<span data-ttu-id="8b920-153">Das folgende Beispiel zeigt das Öffnen eines Recordset, das auf einer Parameterabfrage basiert.</span><span class="sxs-lookup"><span data-stu-id="8b920-153">The following example shows how to open a Recordset that is based on a parameter query.</span></span>

<span data-ttu-id="8b920-154">**Der Beispielcode stammt von:**[Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="8b920-154">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    Dim dbs As DAO.Database
    Dim qdf As DAO.QueryDef
    Dim rst As DAO.Recordset
    
    Set dbs = CurrentDb
    
    'Get the parameter query
    Set qdf = dbs.QueryDefs("qryMyParameterQuery")
    
    'Supply the parameter value
    qdf.Parameters("EnterStartDate") = Date
    qdf.Parameters("EnterEndDate") = Date + 7
    
    'Open a Recordset based on the parameter query
    Set rst = qdf.OpenRecordset()
```

<br/>

<span data-ttu-id="8b920-155">Das folgende Beispiel zeigt das Öffnen eines Recordset, das auf einer Tabelle oder Abfrage basiert.</span><span class="sxs-lookup"><span data-stu-id="8b920-155">The following example shows how to open a Recordset based on a table or a query.</span></span>

```vb 
    Dim dbs As DAO.Database
    Dim rsTable As DAO.Recordset
    Dim rsQuery As DAO.Recordset
    
    Set dbs = CurrentDb
    
    'Open a table-type Recordset
    Set rsTable = dbs.OpenRecordset("Table1", dbOpenTable)
    
    'Open a dynaset-type Recordset using a saved query
    Set rsQuery = dbs.OpenRecordset("qryMyQuery", dbOpenDynaset)
```

<br/>

<span data-ttu-id="8b920-156">Das folgende Beispiel zeigt das Öffnen eines Recordset, das auf einer SQL-Anweisung (Structured Query Language) basiert.</span><span class="sxs-lookup"><span data-stu-id="8b920-156">The following example shows how to open a Recordset based on a Structured Query Language (SQL) statement.</span></span>

```vb
    Dim dbs As DAO.Database
    Dim rsSQL As DAO.Recordset
    Dim strSQL As String
    
    Set dbs = CurrentDb
    
    'Open a snapshot-type Recordset based on an SQL statement
    strSQL = "SELECT * FROM Table1 WHERE Field2 = 33"
    Set rsSQL = dbs.OpenRecordset(strSQL, dbOpenSnapshot)
```

<br/>

<span data-ttu-id="8b920-157">Das folgende Beispiel zeigt das Verwenden der Filter-Eigenschaft zum Ermitteln der Datensätze, die in einem danach geöffneten Recordset enthalten sein sollen.</span><span class="sxs-lookup"><span data-stu-id="8b920-157">The following sample shows how to use the Filter property to determine the records to be included in a subsequently opened Recordset.</span></span>

```vb
    Dim dbs As DAO.Database
    Dim rst As DAO.Recordset
    Dim rstFiltered As DAO.Recordset
    Dim strCity As String
    
    Set dbs = CurrentDb
    
    'Create the first filtered Recordset, returning customer records
    'for those visited between 30-60 days ago.
    Set rst = dbs.OpenRecordset(_ 
        "SELECT * FROM Customers WHERE LastVisitDate BETWEEN Date()-60 " & _
        "AND Date()-30 ORDER BY LastVisitDate DESC")
    
    'Begin row processing
    Do While Not rst.EOF
        
        'Retrieve the name of the first city in the selected rows
        strCity = rst!City
    
        'Now filter the Recordset to return only the customers from that city
        rst.Filter = "City = '" & strCity & "'"
        Set rstFiltered = rst.OpenRecordset
    
        'Process the rows
        Do While Not rstFiltered.EOF
            rstFiltered.Edit
            rstFiltered!ToBeVisited = True
            rstFiltered.Update
            rstFiltered.MoveNext
        Loop
    
        'We've done what was needed. Now exit
        Exit Do
        rst.MoveNext
       
    Loop
    
    'Cleanup
    rstFiltered.Close
    rst.Close
    
    Set rstFiltered = Nothing
    Set rst = Nothing
```



