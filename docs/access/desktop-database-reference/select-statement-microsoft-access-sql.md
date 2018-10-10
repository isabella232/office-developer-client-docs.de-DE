---
title: SELECT-Anweisung (Microsoft Access SQL)
TOCTitle: SELECT Statement (Microsoft Access SQL)
ms:assetid: a5c9da94-5f9e-0fc0-767a-4117f38a5ef3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821148(v=office.15)
ms:contentKeyID: 48546837
ms.date: 09/18/2015
mtps_version: v=office.15
dev_langs:
- sql
ms.openlocfilehash: ae7a63a3fe7647dde117db80a52e2322b9af75b9
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473352"
---
# <a name="select-statement-microsoft-access-sql"></a>SELECT-Anweisung (Microsoft Access SQL)

**Gilt für:** Access 2013 | Office 2013

Weist das Microsoft Access-Datenbankmodul an, Informationen aus der Datenbank als Gruppe von Datensätzen zurückzugeben.

## <a name="syntax"></a>Syntax

Wählen Sie \[ *Prädikat* \] { \*  |  *Tabelle*.\*  |  \[ *Tabelle*. \] *Feld1* \[als *alias1* \] \[, \[ *Tabelle*. \] *field2* \[als *alias2* \] \[,... \] \]} FROM *Tabellenausdruck* \[,... \] \[IN *ExterneDatenbank* \] \[, in dem... \]\[GROUP BY... \]\[HAVING... \]\[ORDER BY... \]\[Mit OWNERACCESS OPTION\]

Die SELECT-Anweisung besteht aus folgenden Teilen:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Teil</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Prädikat</em></p></td>
<td><p>Eines der folgenden Prädikate: <a href="https://msdn.microsoft.com/library/ff195711(v=office.15)">ALL, DISTINCT, DISTINCTROW, or TOP</a>. Sie verwenden das Prädikat, um die Anzahl der zurückgegebenen Datensätze zu beschränken. Wenn keine Angabe erfolgt, ist die Standardeinstellung ALL.  </p></td>
</tr>
<tr class="even">
<td><p><em>*</em></p></td>
<td><p>Gibt an, dass alle Felder der angegebenen Tabelle oder Tabellen ausgewählt werden.</p></td>
</tr>
<tr class="odd">
<td><p><em>Tabelle</em></p></td>
<td><p>Der Name der Tabelle mit den Feldern, aus denen Datensätze ausgewählt werden.</p></td>
</tr>
<tr class="even">
<td><p><em>Feld1</em>, <em>Feld2</em></p></td>
<td><p>Die Namen der Felder mit den abzurufenden Daten. Wenn Sie mehr als ein Feld einschließen, werden sie in der aufgelisteten Reihenfolge abgerufen.</p></td>
</tr>
<tr class="odd">
<td><p><em>Alias1</em>, <em>Alias2</em></p></td>
<td><p>Die Namen, die als Spaltenüberschriften anstatt der ursprünglichen Spaltennamen in <em>Tabelle</em> verwendet werden sollen.</p></td>
</tr>
<tr class="even">
<td><p><em>Tabellenausdruck</em></p></td>
<td><p>Der Name der Tabelle oder Tabellen mit den abzurufenden Daten.</p></td>
</tr>
<tr class="odd">
<td><p><em>externeDatenbank</em></p></td>
<td><p>Der Name der Datenbank an, in den Tabellen unter <em>Tabellenausdruck</em> enthält, wenn sie nicht in der aktuellen Datenbank sind.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Hinweise

Um diesen Vorgang durchzuführen, sucht das Microsoft® Jet-Datenbankmodul die angegebene(n) Tabelle(n), extrahiert die ausgewählten Spalten, wählt Zeilen aus, die dem Krtierium entsprechen, und sortiert oder gruppiert die resultierenden Zeilen in der angegebenen Reihenfolge.

SELECT-Anweisungen ändern keine Daten in der Datenbank.

SELECT ist gewöhnlich das erste Wort in einer SQL-Anweisung. Die meisten SQL-Anweisungen sind SELECT- oder [SELECT…INTO](select-into-statement-microsoft-access-sql.md)-Anweisungen.

Die minimale Syntax für eine SELECT-Anweisung lautet:

SELECT *Felder* FROM *Tabelle*

Sie können ein Sternchen (\*) verwenden, um alle Felder in einer Tabelle auszuwählen. Das folgende Beispiel wählt alle Felder in der Tabelle "Employees" aus:

```sql
SELECT * FROM Employees;
```

Wenn ein Feldname in mehr als einer Tabelle in der FROM-Klausel enthalten ist, stellen Sie den Tabellennamen und den **.** -Operator (Punkt) voran. Im folgenden Beispiel ist das Feld "Department" in der Tabelle "Employees" und in der Tabelle "Supervisors" enthalten. Die SQL-Anweisung wählt Abteilungen aus der Tabelle "Employees" und die Namen von Vorgesetzten aus der Tabelle "Supervisors" aus:

```sql
SELECT Employees.Department, Supervisors.SupvName 
FROM Employees INNER JOIN Supervisors 
WHERE Employees.Department = Supervisors.Department;
```

Wenn ein **Recordset** -Objekt erstellt wird, verwendet das Microsoft Jet-Datenbankmodul den Feldnamen der Tabelle als **Field** -Objektnamen im **Recordset** -Objekt. Wenn Sie einen anderen Feldnamen oder einen Namen verwenden möchten, der nicht durch den Ausdruck zum Generieren des Felds impliziert wird, verwenden Sie das reservierte Wort AS. Das folgende Beispiel verwendet den Titel "Birth", um das zurückgegebene **Field** -Objekt im resultierenden **Recordset** -Objekt zu benennen:

```sql
SELECT BirthDate 
AS Birth FROM Employees;
```

Wenn Sie zusammenfassende Funktionen oder Abfragen verwenden, die mehrdeutige oder doppelte **Field** -Objektnamen zurückgeben, müssen Sie die AS-Klausel verwenden, um einen alternativen Namen für das **Field** -Objekt anzugeben. Das folgende Beispiel verwendet den Titel "HeadCount", um das zurückgegebene **Field** -Objekt im resultierenden **Recordset** -Objekt zu benennen:

```sql
SELECT COUNT(EmployeeID)
AS HeadCount FROM Employees;
```

Sie können die anderen Klauseln in einer SELECT-Anweisung verwenden, um die zurückgegebenen Daten weiter einzuschränken und zu organisieren. Weitere Informationen finden Sie im Hilfethema zur verwendeten Klausel.

**Links bereitgestellt werden, von** der Community [UtterAccess](https://www.utteraccess.com) . UtterAccess ist das führende Microsoft Access-Wiki und -Hilfeforum.

- [SQL-zu-VBA-Formatierungsprogramm](https://www.utteraccess.com/forum/sql-vba-formatter-t1165308.html)

- [Anzeigen von Datensätzen innerhalb eines definierten Bereichs](https://www.utteraccess.com/wiki/index.php/records_within_a_defined_range)

## <a name="example"></a>Beispiel

Einige der folgenden Beispiele setzen das Vorhandensein einer hypothetischen Felds "Salary" in der Tabelle "Employees" voraus. Beachten Sie, dass dieses Feld in der Northwind-Datenbank "Employees" nicht wirklich vorhanden ist.

Dieses Beispiel erstellt ein **Recordset** vom Typ "Dynaset" basierend auf einer SQL-Anweisung, die die Felder "LastName" und "FirstName" aus allen Datensätzen in der Tabelle "Employees" auswählt. Es ruft die "EnumFields"-Prozedur auf, die die Inhalte eines **Recordset** -Objekts im Fenster **Debug** ausgibt.

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

Dieses Beispiel zählt die Anzahl der Datensätze, die einen Eintrag im Feld "PostalCode" haben, und benennt das zurückgegebene Feld "Tally".

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

Dieses Beispiel zeigt die Anzahl der Mitarbeiter und die durchschnittlichen und maximalen Gehälter.

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

Die **Sub** -Prozedur "EnumFields" wird an ein **Recordset** -Objekt von der aufrufenden Prozedur übergeben. Die Prozedur formatiert und zeigt dann die Felder des **Recordset** im Fenster **Debug**. Die Variable ist die gewünschte Breite des ausgegebenen Felds. Einige Felder können abgeschnitten sein.

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




