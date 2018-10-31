---
title: SELECT-Anweisung (Microsoft Access SQL)
TOCTitle: SELECT statement (Microsoft Access SQL)
ms:assetid: a5c9da94-5f9e-0fc0-767a-4117f38a5ef3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821148(v=office.15)
ms:contentKeyID: 48546837
ms.date: 10/18/2018
mtps_version: v=office.15
dev_langs:
- sql
ms.openlocfilehash: 2b03834914c352a0e9c462c50bee48ac992276e3
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860581"
---
# <a name="select-statement-microsoft-access-sql"></a><span data-ttu-id="f7f28-102">SELECT-Anweisung (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="f7f28-102">SELECT statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="f7f28-103">**Gilt für:** Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="f7f28-103">**Applies to:** Access 2013 | Office 2013</span></span>

<span data-ttu-id="f7f28-104">Weist das Microsoft Access-Datenbankmodul an, Informationen aus der Datenbank als Gruppe von Datensätzen zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="f7f28-104">Instructs the Microsoft Access database engine to return information from the database as a set of records.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7f28-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f7f28-105">Syntax</span></span>

<span data-ttu-id="f7f28-106">Wählen Sie \[ *Prädikat* \] { \*  |  *Tabelle*.\*  |  \[ *Tabelle*. \] *Feld1* \[als *alias1* \] \[, \[ *Tabelle*. \] *field2* \[als *alias2* \] \[,... \] \]} FROM *Tabellenausdruck* \[,... \] \[IN *ExterneDatenbank* \] \[, in dem...</span><span class="sxs-lookup"><span data-stu-id="f7f28-106">SELECT \[*predicate*\] { \* | *table*.\* | \[*table*.\]*field1* \[AS *alias1*\] \[, \[*table*.\]*field2* \[AS *alias2*\] \[, …\]\]} FROM *tableexpression* \[, …\] \[IN *externaldatabase*\] \[WHERE…</span></span> <span data-ttu-id="f7f28-107">\]\[GROUP BY...</span><span class="sxs-lookup"><span data-stu-id="f7f28-107">\] \[GROUP BY…</span></span> <span data-ttu-id="f7f28-108">\]\[HAVING...</span><span class="sxs-lookup"><span data-stu-id="f7f28-108">\] \[HAVING…</span></span> <span data-ttu-id="f7f28-109">\]\[ORDER BY...</span><span class="sxs-lookup"><span data-stu-id="f7f28-109">\] \[ORDER BY…</span></span> <span data-ttu-id="f7f28-110">\]\[Mit OWNERACCESS OPTION\]</span><span class="sxs-lookup"><span data-stu-id="f7f28-110">\] \[WITH OWNERACCESS OPTION\]</span></span>

<span data-ttu-id="f7f28-111">Die SELECT-Anweisung besteht aus folgenden Teilen:</span><span class="sxs-lookup"><span data-stu-id="f7f28-111">The SELECT statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f7f28-112">Teil</span><span class="sxs-lookup"><span data-stu-id="f7f28-112">Part</span></span></p></th>
<th><p><span data-ttu-id="f7f28-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f7f28-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f7f28-114"><em>Prädikat</em></span><span class="sxs-lookup"><span data-stu-id="f7f28-114"><em>predicate</em></span></span></p></td>
<td><p><span data-ttu-id="f7f28-p102">Eines der folgenden Prädikate: <a href="https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/all-distinct-distinctrow-top-predicates-microsoft-access-sql">ALL, DISTINCT, DISTINCTROW, or TOP</a>. Sie verwenden das Prädikat, um die Anzahl der zurückgegebenen Datensätze zu beschränken. Wenn keine Angabe erfolgt, ist die Standardeinstellung ALL.  </span><span class="sxs-lookup"><span data-stu-id="f7f28-p102">One of the following predicates: <a href="https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/all-distinct-distinctrow-top-predicates-microsoft-access-sql">ALL, DISTINCT, DISTINCTROW, or TOP</a>. You use the predicate to restrict the number of records returned. If none is specified, the default is ALL.</span></span></p></td>
</tr>
<tr class="even">
<td><p><em>*</em></p></td>
<td><p><span data-ttu-id="f7f28-118">Gibt an, dass alle Felder der angegebenen Tabelle oder Tabellen ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="f7f28-118">Specifies that all fields from the specified table or tables are selected.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f7f28-119"><em>Tabelle</em></span><span class="sxs-lookup"><span data-stu-id="f7f28-119"><em>table</em></span></span></p></td>
<td><p><span data-ttu-id="f7f28-120">Der Name der Tabelle mit den Feldern, aus denen Datensätze ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="f7f28-120">The name of the table containing the fields from which records are selected.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f7f28-121"><em>Feld1</em>, <em>Feld2</em></span><span class="sxs-lookup"><span data-stu-id="f7f28-121"><em>field1</em>, <em>field2</em></span></span></p></td>
<td><p><span data-ttu-id="f7f28-p103">Die Namen der Felder mit den abzurufenden Daten. Wenn Sie mehr als ein Feld einschließen, werden sie in der aufgelisteten Reihenfolge abgerufen.</span><span class="sxs-lookup"><span data-stu-id="f7f28-p103">The names of the fields containing the data you want to retrieve. If you include more than one field, they are retrieved in the order listed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f7f28-124"><em>Alias1</em>, <em>Alias2</em></span><span class="sxs-lookup"><span data-stu-id="f7f28-124"><em>alias1</em>, <em>alias2</em></span></span></p></td>
<td><p><span data-ttu-id="f7f28-125">Die Namen, die als Spaltenüberschriften anstatt der ursprünglichen Spaltennamen in <em>Tabelle</em> verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f7f28-125">The names to use as column headers instead of the original column names in <em>table</em>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f7f28-126"><em>Tabellenausdruck</em></span><span class="sxs-lookup"><span data-stu-id="f7f28-126"><em>tableexpression</em></span></span></p></td>
<td><p><span data-ttu-id="f7f28-127">Der Name der Tabelle oder Tabellen mit den abzurufenden Daten.</span><span class="sxs-lookup"><span data-stu-id="f7f28-127">The name of the table or tables containing the data you want to retrieve.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f7f28-128"><em>externeDatenbank</em></span><span class="sxs-lookup"><span data-stu-id="f7f28-128"><em>externaldatabase</em></span></span></p></td>
<td><p><span data-ttu-id="f7f28-129">Der Name der Datenbank an, in den Tabellen unter <em>Tabellenausdruck</em> enthält, wenn sie nicht in der aktuellen Datenbank sind.</span><span class="sxs-lookup"><span data-stu-id="f7f28-129">The name of the database containing the tables in <em>tableexpression</em> if they are not in the current database.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="f7f28-130">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f7f28-130">Remarks</span></span>

<span data-ttu-id="f7f28-131">Zum Ausführen dieses Vorgangs Microsoft Jet-Datenbankmodul sucht nach der angegebenen Tabelle oder Tabellen extrahiert die ausgewählten Spalten, wählt Zeilen, die die Kriterien, und sortiert oder gruppiert die Zeilen in der angegebenen Reihenfolge zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="f7f28-131">To perform this operation, the Microsoft Jet database engine searches the specified table or tables, extracts the chosen columns, selects rows that meet the criterion, and sorts or groups the resulting rows into the order specified.</span></span>

<span data-ttu-id="f7f28-132">SELECT-Anweisungen ändern keine Daten in der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="f7f28-132">SELECT statements do not change data in the database.</span></span>

<span data-ttu-id="f7f28-p104">SELECT ist gewöhnlich das erste Wort in einer SQL-Anweisung. Die meisten SQL-Anweisungen sind SELECT- oder [SELECT…INTO](select-into-statement-microsoft-access-sql.md)-Anweisungen.</span><span class="sxs-lookup"><span data-stu-id="f7f28-p104">SELECT is usually the first word in an SQL statement. Most SQL statements are either SELECT or [SELECT…INTO](select-into-statement-microsoft-access-sql.md) statements.</span></span>

<span data-ttu-id="f7f28-135">Die minimale Syntax für eine SELECT-Anweisung lautet:</span><span class="sxs-lookup"><span data-stu-id="f7f28-135">The minimum syntax for a SELECT statement is:</span></span>

<span data-ttu-id="f7f28-136">SELECT *Felder* FROM *Tabelle*</span><span class="sxs-lookup"><span data-stu-id="f7f28-136">SELECT *fields* FROM *table*</span></span>

<span data-ttu-id="f7f28-p105">Sie können ein Sternchen (\*) verwenden, um alle Felder in einer Tabelle auszuwählen. Das folgende Beispiel wählt alle Felder in der Tabelle "Employees" aus:</span><span class="sxs-lookup"><span data-stu-id="f7f28-p105">You can use an asterisk (\*) to select all fields in a table. The following example selects all of the fields in the Employees table:</span></span>

```sql
SELECT * FROM Employees;
```

<span data-ttu-id="f7f28-p106">Wenn ein Feldname in mehr als einer Tabelle in der FROM-Klausel enthalten ist, stellen Sie den Tabellennamen und den **.** -Operator (Punkt) voran. Im folgenden Beispiel ist das Feld "Department" in der Tabelle "Employees" und in der Tabelle "Supervisors" enthalten. Die SQL-Anweisung wählt Abteilungen aus der Tabelle "Employees" und die Namen von Vorgesetzten aus der Tabelle "Supervisors" aus:</span><span class="sxs-lookup"><span data-stu-id="f7f28-p106">If a field name is included in more than one table in the FROM clause, precede it with the table name and the **.** (dot) operator. In the following example, the Department field is in both the Employees table and the Supervisors table. The SQL statement selects departments from the Employees table and supervisor names from the Supervisors table:</span></span>

```sql
SELECT Employees.Department, Supervisors.SupvName 
FROM Employees INNER JOIN Supervisors 
WHERE Employees.Department = Supervisors.Department;
```

<span data-ttu-id="f7f28-p107">Wenn ein **Recordset** -Objekt erstellt wird, verwendet das Microsoft Jet-Datenbankmodul den Feldnamen der Tabelle als **Field** -Objektnamen im **Recordset** -Objekt. Wenn Sie einen anderen Feldnamen oder einen Namen verwenden möchten, der nicht durch den Ausdruck zum Generieren des Felds impliziert wird, verwenden Sie das reservierte Wort AS. Das folgende Beispiel verwendet den Titel "Birth", um das zurückgegebene **Field** -Objekt im resultierenden **Recordset** -Objekt zu benennen:</span><span class="sxs-lookup"><span data-stu-id="f7f28-p107">When a **Recordset** object is created, the Microsoft Jet database engine uses the table's field name as the **Field** object name in the **Recordset** object. If you want a different field name or a name is not implied by the expression used to generate the field, use the AS reserved word. The following example uses the title Birth to name the returned **Field** object in the resulting **Recordset** object:</span></span>

```sql
SELECT BirthDate 
AS Birth FROM Employees;
```

<span data-ttu-id="f7f28-p108">Wenn Sie zusammenfassende Funktionen oder Abfragen verwenden, die mehrdeutige oder doppelte **Field** -Objektnamen zurückgeben, müssen Sie die AS-Klausel verwenden, um einen alternativen Namen für das **Field** -Objekt anzugeben. Das folgende Beispiel verwendet den Titel "HeadCount", um das zurückgegebene **Field** -Objekt im resultierenden **Recordset** -Objekt zu benennen:</span><span class="sxs-lookup"><span data-stu-id="f7f28-p108">Whenever you use aggregate functions or queries that return ambiguous or duplicate **Field** object names, you must use the AS clause to provide an alternate name for the **Field** object. The following example uses the title HeadCount to name the returned **Field** object in the resulting **Recordset** object:</span></span>

```sql
SELECT COUNT(EmployeeID)
AS HeadCount FROM Employees;
```

<span data-ttu-id="f7f28-p109">Sie können die anderen Klauseln in einer SELECT-Anweisung verwenden, um die zurückgegebenen Daten weiter einzuschränken und zu organisieren. Weitere Informationen finden Sie im Hilfethema zur verwendeten Klausel.</span><span class="sxs-lookup"><span data-stu-id="f7f28-p109">You can use the other clauses in a SELECT statement to further restrict and organize your returned data. For more information, see the Help topic for the clause you are using.</span></span>

<span data-ttu-id="f7f28-150">**Links bereitgestellt werden, von** der Community [UtterAccess](https://www.utteraccess.com) .</span><span class="sxs-lookup"><span data-stu-id="f7f28-150">**Links provided by** the [UtterAccess](https://www.utteraccess.com) community.</span></span> <span data-ttu-id="f7f28-151">UtterAccess ist das führende Microsoft Access-Wiki und -Hilfeforum.</span><span class="sxs-lookup"><span data-stu-id="f7f28-151">UtterAccess is the premier Microsoft Access wiki and help forum.</span></span>

- [<span data-ttu-id="f7f28-152">SQL-zu-VBA-Formatierungsprogramm</span><span class="sxs-lookup"><span data-stu-id="f7f28-152">SQL to VBA Formatter</span></span>](https://www.utteraccess.com/forum/sql-vba-formatter-t1165308.html)

- [<span data-ttu-id="f7f28-153">Anzeigen von Datensätzen innerhalb eines definierten Bereichs</span><span class="sxs-lookup"><span data-stu-id="f7f28-153">Viewing Records Within A Defined Range</span></span>](https://www.utteraccess.com/wiki/index.php/records_within_a_defined_range)

## <a name="example"></a><span data-ttu-id="f7f28-154">Beispiel</span><span class="sxs-lookup"><span data-stu-id="f7f28-154">Example</span></span>

<span data-ttu-id="f7f28-p111">Einige der folgenden Beispiele setzen das Vorhandensein einer hypothetischen Felds "Salary" in der Tabelle "Employees" voraus. Beachten Sie, dass dieses Feld in der Northwind-Datenbank "Employees" nicht wirklich vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="f7f28-p111">Some of the following examples assume the existence of a hypothetical Salary field in an Employees table. Note that this field does not actually exist in the Northwind database Employees table.</span></span>

<span data-ttu-id="f7f28-p112">Dieses Beispiel erstellt ein **Recordset** vom Typ "Dynaset" basierend auf einer SQL-Anweisung, die die Felder "LastName" und "FirstName" aus allen Datensätzen in der Tabelle "Employees" auswählt. Es ruft die "EnumFields"-Prozedur auf, die die Inhalte eines **Recordset** -Objekts im Fenster **Debug** ausgibt.</span><span class="sxs-lookup"><span data-stu-id="f7f28-p112">This example creates a dynaset-type **Recordset** based on an SQL statement that selects the LastName and FirstName fields of all records in the Employees table. It calls the EnumFields procedure, which prints the contents of a **Recordset** object to the **Debug** window.</span></span>

```sql
    Sub SelectX1() 
     
        Dim dbs As Database, rst As Recordset 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Select the last name and first name values of all  
        ' records in the Employees table. 
        Set rst = dbs.OpenRecordset("SELECT LastName, " _ 
            & "FirstName FROM Employees;") 
     
        ' Populate the recordset. 
        rst.MoveLast 
     
        ' Call EnumFields to print the contents of the 
        ' Recordset. 
        EnumFields rst,12 
     
        dbs.Close 
     
    End Sub
```

<br/>

<span data-ttu-id="f7f28-159">Dieses Beispiel zählt die Anzahl der Datensätze, die einen Eintrag im Feld "PostalCode" haben, und benennt das zurückgegebene Feld "Tally".</span><span class="sxs-lookup"><span data-stu-id="f7f28-159">This example counts the number of records that have an entry in the PostalCode field and names the returned field Tally.</span></span>

```sql
    Sub SelectX2() 
     
        Dim dbs As Database, rst As Recordset 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Count the number of records with a PostalCode  
        ' value and return the total in the Tally field. 
        Set rst = dbs.OpenRecordset("SELECT Count " _ 
            & "(PostalCode) AS Tally FROM Customers;") 
     
        ' Populate the Recordset. 
        rst.MoveLast 
     
        ' Call EnumFields to print the contents of  
        ' the Recordset. Specify field width = 12. 
        EnumFields rst, 12 
     
        dbs.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="f7f28-160">Dieses Beispiel zeigt die Anzahl der Mitarbeiter und die durchschnittlichen und maximalen Gehälter.</span><span class="sxs-lookup"><span data-stu-id="f7f28-160">This example shows the number of employees and the average and maximum salaries.</span></span>

```sql
    Sub SelectX3() 
     
        Dim dbs As Database, rst As Recordset 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Count the number of employees, calculate the  
        ' average salary, and return the highest salary. 
        Set rst = dbs.OpenRecordset("SELECT Count (*) " _ 
            & "AS TotalEmployees, Avg(Salary) " _ 
            & "AS AverageSalary, Max(Salary) " _ 
            & "AS MaximumSalary FROM Employees;") 
     
        ' Populate the Recordset. 
        rst.MoveLast 
     
        ' Call EnumFields to print the contents of 
        ' the Recordset. Pass the Recordset object and 
        ' desired field width. 
        EnumFields rst, 17 
     
        dbs.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="f7f28-p113">Die **Sub** -Prozedur "EnumFields" wird an ein **Recordset** -Objekt von der aufrufenden Prozedur übergeben. Die Prozedur formatiert und zeigt dann die Felder des **Recordset** im Fenster **Debug**. Die Variable ist die gewünschte Breite des ausgegebenen Felds. Einige Felder können abgeschnitten sein.</span><span class="sxs-lookup"><span data-stu-id="f7f28-p113">The **Sub** procedure EnumFields is passed a **Recordset** object from the calling procedure. The procedure then formats and prints the fields of the **Recordset** to the **Debug** window. The variable is the desired printed field width. Some fields may be truncated.</span></span>

```sql
    Sub EnumFields(rst As Recordset, intFldLen As Integer) 
     
        Dim lngRecords As Long, lngFields As Long 
        Dim lngRecCount As Long, lngFldCount As Long 
        Dim strTitle As String, strTemp As String 
     
        ' Set the lngRecords variable to the number of 
        ' records in the Recordset. 
        lngRecords = rst.RecordCount 
     
        ' Set the lngFields variable to the number of 
        ' fields in the Recordset. 
        lngFields = rst.Fields.Count 
     
        Debug.Print "There are " & lngRecords _ 
            & " records containing " & lngFields _ 
            & " fields in the recordset." 
        Debug.Print 
     
        ' Form a string to print the column heading. 
        strTitle = "Record  " 
        For lngFldCount = 0 To lngFields - 1 
            strTitle = strTitle _ 
            & Left(rst.Fields(lngFldCount).Name _ 
            & Space(intFldLen), intFldLen) 
        Next lngFldCount     
     
        ' Print the column heading. 
        Debug.Print strTitle 
        Debug.Print 
     
        ' Loop through the Recordset; print the record 
        ' number and field values. 
        rst.MoveFirst 
     
        For lngRecCount = 0 To lngRecords - 1 
            Debug.Print Right(Space(6) & _ 
                Str(lngRecCount), 6) & "  "; 
     
            For lngFldCount = 0 To lngFields - 1 
                ' Check for Null values. 
                If IsNull(rst.Fields(lngFldCount)) Then 
                    strTemp = "<null>" 
                Else 
                    ' Set strTemp to the field contents.  
                    Select Case _ 
                        rst.Fields(lngFldCount).Type 
                        Case 11 
                            strTemp = "" 
                        Case dbText, dbMemo 
                            strTemp = _ 
                                rst.Fields(lngFldCount) 
                        Case Else 
                            strTemp = _ 
                                str(rst.Fields(lngFldCount)) 
                    End Select 
                End If 
     
                Debug.Print Left(strTemp _  
                    & Space(intFldLen), intFldLen); 
            Next lngFldCount 
     
            Debug.Print 
     
            rst.MoveNext 
     
        Next lngRecCount 
     
    End Sub 
```




