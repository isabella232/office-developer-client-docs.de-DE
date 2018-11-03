---
title: Database.OpenRecordset-Methode (DAO)
TOCTitle: OpenRecordset Method
ms:assetid: a243bc79-cac4-fe12-768d-d3d017954e78
ms:mtpsurl: https://msdn.microsoft.com/library/Ff820966(v=office.15)
ms:contentKeyID: 48546753
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052939
f1_categories:
- Office.Version=v15
ms.openlocfilehash: ab969f2e26751a70a0f9ac9daf2ca17bcaa103c5
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925975"
---
# <a name="databaseopenrecordset-method-dao"></a><span data-ttu-id="93667-102">Database.OpenRecordset-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="93667-102">Database.OpenRecordset method (DAO)</span></span>

<span data-ttu-id="93667-103">**Gilt für:** Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="93667-103">**Applies to:** Access 2013 | Office 2013</span></span>

<span data-ttu-id="93667-104">Erstellt ein neues **[Recordset](recordset-object-dao.md)** -Objekt und fügt es an die **Recordsets**-Auflistung an.</span><span class="sxs-lookup"><span data-stu-id="93667-104">Creates a new **[Recordset](recordset-object-dao.md)** object and appends it to the **Recordsets** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="93667-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="93667-105">Syntax</span></span>

<span data-ttu-id="93667-106">*Ausdruck* . OpenRecordset (_**Name**_, _**Typ**_, _**Optionen**_, _**LockEdit**_)</span><span class="sxs-lookup"><span data-stu-id="93667-106">*expression* .OpenRecordset(_**Name**_, _**Type**_, _**Options**_, _**LockEdit**_)</span></span>

<span data-ttu-id="93667-107">*Ausdruck* Eine Variable, die ein **Database** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="93667-107">*expression* A variable that represents a **Database** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="93667-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="93667-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="93667-109">Name</span><span class="sxs-lookup"><span data-stu-id="93667-109">Name</span></span></p></th>
<th><p><span data-ttu-id="93667-110">Erforderlich/Optional</span><span class="sxs-lookup"><span data-stu-id="93667-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="93667-111">Datentyp</span><span class="sxs-lookup"><span data-stu-id="93667-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="93667-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="93667-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="93667-113">Name</span><span class="sxs-lookup"><span data-stu-id="93667-113">Name</span></span></p></td>
<td><p><span data-ttu-id="93667-114">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="93667-114">Required</span></span></p></td>
<td><p><span data-ttu-id="93667-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="93667-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="93667-p101">Die Quelle der Datensätze für das neue <strong>Recordset</strong>. Die Quelle kann ein Tabellenname, ein Abfragename oder eine SQL-Anweisung sein, die Datensätze zurückgibt. Für <strong>Recordset</strong> -Objekte vom "table"-Typ in Microsoft Access-Datenbankmodul-Datenbanken kann die Quelle nur ein Tabellenname sein.  </span><span class="sxs-lookup"><span data-stu-id="93667-p101">The source of the records for the new <strong>Recordset</strong>. The source can be a table name, a query name, or an SQL statement that returns records. For table-type <strong>Recordset</strong> objects in Microsoft Access database engine databases, the source can only be a table name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93667-119">Typ</span><span class="sxs-lookup"><span data-stu-id="93667-119">Type</span></span></p></td>
<td><p><span data-ttu-id="93667-120">Optional</span><span class="sxs-lookup"><span data-stu-id="93667-120">Optional</span></span></p></td>
<td><p><span data-ttu-id="93667-121"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="93667-121"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="93667-122">Eine <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong> -Konstante gibt den Typ des zu öffnenden <strong>Recordset</strong> an.</span><span class="sxs-lookup"><span data-stu-id="93667-122">A <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong> constant that indicates the type of <strong>Recordset</strong> to open.</span></span></p>

> [!NOTE]
> <span data-ttu-id="93667-p102">Wenn Sie ein **Recordset** in einem Microsoft Access-Arbeitsbereich öffnen und keinen Typ angeben, erstellt **OpenRecordset**, wenn möglich, ein **Recordset** vom "table"-Typ. Wenn sie eine verknüpfte Tabelle oder Abfrage angeben, erstellt **OpenRecordset** ein **Recordset** vom "dynaset"-Typ.</span><span class="sxs-lookup"><span data-stu-id="93667-p102">If you open a **Recordset** in a Microsoft Access workspace and you don't specify a type, **OpenRecordset** creates a table-type **Recordset**, if possible. If you specify a linked table or query, **OpenRecordset** creates a dynaset-type **Recordset**.</span></span>


</td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93667-125">Options</span><span class="sxs-lookup"><span data-stu-id="93667-125">Options</span></span></p></td>
<td><p><span data-ttu-id="93667-126">Optional</span><span class="sxs-lookup"><span data-stu-id="93667-126">Optional</span></span></p></td>
<td><p><span data-ttu-id="93667-127"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="93667-127"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="93667-128">Eine Kombination aus <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong> -Konstanten, die Merkmale des neuen <strong>Recordset</strong> angeben.</span><span class="sxs-lookup"><span data-stu-id="93667-128">A combination of <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong> constants that specify characteristics of the new <strong>Recordset</strong>.</span></span></p>

> [!NOTE]
> <span data-ttu-id="93667-p103">Die Konstanten **dbConsistent** und **dbInconsistent** sind gegenseitig exklusiv. Die Verwendung von beiden verursacht einen Fehler. Auch das Angeben eines LockEdit-Arguments, wenn Options die **dbReadOnly**-Konstante verwendet, verursacht einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="93667-p103">The constants **dbConsistent** and **dbInconsistent** are mutually exclusive, and using both causes an error. Supplying a LockEdit argument when Options uses the **dbReadOnly** constant also causes an error.</span></span>


</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93667-131">LockEdit</span><span class="sxs-lookup"><span data-stu-id="93667-131">LockEdit</span></span></p></td>
<td><p><span data-ttu-id="93667-132">Optional</span><span class="sxs-lookup"><span data-stu-id="93667-132">Optional</span></span></p></td>
<td><p><span data-ttu-id="93667-133"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="93667-133"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="93667-134">Eine <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong> -Konstante, die die Sperre für das <strong>Recordset</strong> bestimmt.</span><span class="sxs-lookup"><span data-stu-id="93667-134">A <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong> constant that determines the locking for the <strong>Recordset</strong>.</span></span></p>

> [!NOTE]
> <span data-ttu-id="93667-p104">Sie können **dbReadOnly** im Options-Argument oder im LockedEdit-Argument verwenden, aber nicht in beiden. Wenn Sie es für beide Argumente verwenden, tritt ein Laufzeitfehler auf.</span><span class="sxs-lookup"><span data-stu-id="93667-p104">You can use **dbReadOnly** in either the Options argument or the LockedEdit argument, but not both. If you use it for both arguments, a run-time error occurs.</span></span>


</td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="93667-137">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="93667-137">Return value</span></span>

<span data-ttu-id="93667-138">Recordset</span><span class="sxs-lookup"><span data-stu-id="93667-138">Recordset</span></span>

## <a name="remarks"></a><span data-ttu-id="93667-139">Hinweise</span><span class="sxs-lookup"><span data-stu-id="93667-139">Remarks</span></span>

<span data-ttu-id="93667-p105">Wenn der Benutzer beim Aktualisieren eines Datensatzes diesen Fehler erhält, sollte der Code den Inhalt des Felds aktualisieren und die geänderten Werte abrufen. Tritt der Fehler beim Löschen eines Datensatzes auf, sollte der Code die Daten des neuen Datensatzes anzeigen und eine Meldung darüber ausgeben, dass die Daten kürzlich geändert wurden. An dieser Stelle könnte der Code bestätigen lassen, dass der Benutzer den Datensatz wirklich löschen möchte.</span><span class="sxs-lookup"><span data-stu-id="93667-p105">Typically, if the user gets this error while updating a record, your code should refresh the contents of the fields and retrieve the newly modified values. If the error occurs while deleting a record, your code could display the new record data to the user and a message indicating that the data has recently changed. At this point, your code can request a confirmation that the user still wants to delete the record.</span></span>

<span data-ttu-id="93667-143">Sie sollten die **dbSeeChanges**-Konstante auch dann verwenden, wenn Sie ein **Recordset** in einem mit einem Microsoft Access-Datenbankmodul verbundenen ODBC-Arbeitsbereich in einer Microsoft SQL Server 6.0-Tabelle (oder höher) öffnen, die über eine IDENTITY-Spalte verfügt. Andernfalls tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="93667-143">You should also use the **dbSeeChanges** constant if you open a **Recordset** in a Microsoft Access database engine-connected ODBC workspace against a Microsoft SQL Server 6.0 (or later) table that has an IDENTITY column, otherwise an error may result.</span></span>

<span data-ttu-id="93667-p106">Das Öffnen mehrerer **Recordset**-Objekte in einer ODBC-Datenquelle kann fehlschlagen, wenn die Verbindung durch einen vorherigen **OpenRecordset**-Aufruf ausgelastet ist. Das könnten Sie beispielsweise dadurch verhindern, dass Sie das **Recordset**-Objekt mithilfe der **MoveLast**-Methode vollständig auffüllen, sobald das **Recordset**-Objekt geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="93667-p106">Opening more than one **Recordset** on an ODBC data source may fail because the connection is busy with a prior **OpenRecordset** call. One way around this is to fully populate the **Recordset** by using the **MoveLast** method as soon as the **Recordset** is opened.</span></span>

<span data-ttu-id="93667-146">Beim Schließen eines **Recordset**-Objekts mit der **[Close](connection-close-method-dao.md)** -Methode wird es automatisch aus der **Recordsets**-Auflistung gelöscht.</span><span class="sxs-lookup"><span data-stu-id="93667-146">Closing a **Recordset** with the **[Close](connection-close-method-dao.md)** method automatically deletes it from the **Recordsets** collection.</span></span>


> [!NOTE]
> <span data-ttu-id="93667-147">Wenn *Quelle* bezieht eine SQL-Anweisung besteht aus einer Zeichenfolge mit einem nicht-Integer-Wert verkettet und die Systemparameter angeben einer US-decimal Zeichen wie etwa ein Komma (beispielsweise StrSQL = "PRICE &gt; " &amp; LngPrice, und LngPrice = 125,50), tritt ein Fehler auf, wenn Sie, zum Öffnen des **Recordset-Objekts versuchen**.</span><span class="sxs-lookup"><span data-stu-id="93667-147">If *source* refers to an SQL statement composed of a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strSQL = "PRICE &gt; " &amp; lngPrice, and lngPrice = 125,50), an error occurs when you try to open the **Recordset**.</span></span> <span data-ttu-id="93667-148">Das geschieht, weil die Zahl während der Verkettung mithilfe des standardmäßigen Dezimalzeichens des Systems in eine Zeichenfolge konvertiert wird und SQL nur US-amerikanische Dezimalzeichen akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="93667-148">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and SQL only accepts U.S. decimal characters.</span></span>

<span data-ttu-id="93667-149">**Link bereitgestellt, von** der Community [UtterAccess](https://www.utteraccess.com) .</span><span class="sxs-lookup"><span data-stu-id="93667-149">**Link provided by** the [UtterAccess](https://www.utteraccess.com) community.</span></span> <span data-ttu-id="93667-150">UtterAccess ist das führende Microsoft Access-Wiki und -Hilfeforum.</span><span class="sxs-lookup"><span data-stu-id="93667-150">UtterAccess is the premier Microsoft Access wiki and help forum.</span></span>

- [<span data-ttu-id="93667-151">Übertragen von Daten von Access nach Excel</span><span class="sxs-lookup"><span data-stu-id="93667-151">Transfer data from Access to Excel</span></span>](https://www.utteraccess.com/forum/transfer-data-access-ex-t1672619.html)

## <a name="example"></a><span data-ttu-id="93667-152">Beispiel</span><span class="sxs-lookup"><span data-stu-id="93667-152">Example</span></span>

<span data-ttu-id="93667-153">Das folgende Beispiel zeigt das Öffnen eines Recordset, das auf einer Parameterabfrage basiert.</span><span class="sxs-lookup"><span data-stu-id="93667-153">The following example shows how to open a Recordset that is based on a parameter query.</span></span>

<span data-ttu-id="93667-154">**Beispielcode von** der [Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="93667-154">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    Dim dbs As DAO.Database
    Dim qdf As DAO.QueryDef
    Dim rst As DAO.Recordset
    
    Set dbs = CurrentDb
    
    'Get the parameter query
    Set qfd = dbs.QueryDefs("qryMyParameterQuery")
    
    'Supply the parameter value
    qdf.Parameters("EnterStartDate") = Date
    qdf.Parameters("EnterEndDate") = Date + 7
    
    'Open a Recordset based on the parameter query
    Set rst = qdf.OpenRecordset()
```

<br/>

<span data-ttu-id="93667-155">Das folgende Beispiel zeigt das Öffnen eines Recordset, das auf einer Tabelle oder Abfrage basiert.</span><span class="sxs-lookup"><span data-stu-id="93667-155">The following example shows how to open a Recordset based on a table or a query.</span></span>

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

<span data-ttu-id="93667-156">Das folgende Beispiel zeigt das Öffnen eines Recordset, das auf einer SQL-Anweisung (Structured Query Language) basiert.</span><span class="sxs-lookup"><span data-stu-id="93667-156">The following example shows how to open a Recordset based on a Structured Query Language (SQL) statement.</span></span>

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

<span data-ttu-id="93667-157">Das folgende Beispiel zeigt das Verwenden der Filter-Eigenschaft zum Ermitteln der Datensätze, die in einem danach geöffneten Recordset enthalten sein sollen.</span><span class="sxs-lookup"><span data-stu-id="93667-157">The following sample shows how to use the Filter property to determine the records to be included in a subsequently opened Recordset.</span></span>

```vb
    Dim dbs As DAO.Database
    Dim rst As DAO.Recordset
    Dim rstFiltered As DAO.Recordset
    Dim strCity As String
    
    Set dbs = CurrentDb
    
    'Create the first filtered Recordset, returning customer records
    'for those visited between 30-60 days ago.
    Set rest = dbs.OpenRecordset(_ 
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



