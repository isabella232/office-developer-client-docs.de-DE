---
title: QueryDef.SQL-Eigenschaft (DAO)
TOCTitle: SQL property
ms:assetid: 16446789-c8be-bff0-eddd-b5f6a8530128
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845522(v=office.15)
ms:contentKeyID: 48543429
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053054
f1_categories:
- Office.Version=v15
ms.localizationpriority: high
ms.openlocfilehash: 3213cf90bc1f2b07f93f19561d24dbd2ee31dd8e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59576996"
---
# <a name="querydefsql-property-dao"></a>QueryDef.SQL-Eigenschaft (DAO)

**Gilt für**: Access 2013, Office 2013

Legt die SQL-Anweisung fest, die die Abfrage definiert, die von einem **[QueryDef](querydef-object-dao.md)**-Objekt ausgeführt wird, oder gibt sie zurück.

## <a name="syntax"></a>Syntax

*Ausdruck* .SQL

*Ausdruck* Eine Variable, die ein **QueryDef**-Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Die **SQL**-Eigenschaft enthält die SQL-Anweisung, die festlegt, wie viele Datensätze ausgewählt, gruppiert und sortiert werden, wenn Sie die Abfrage ausführen. Sie können die Abfrage verwenden, um Datensätze auszuwählen, die in ein **[Recordset](recordset-object-dao.md)**-Objekt einbezogen werden sollen. Sie können auch Aktionsabfragen definieren, um Daten zu ändern, ohne Datensätze zurückzugeben.

Die in einer Abfrage verwendete SQL-Syntax muss dem SQL-Dialekt des Abfragemoduls entsprechen, der vom Typ des Arbeitsbereichs festgelegt wird. In einem Microsoft Access-Arbeitsbereich verwenden Sie den Microsoft Access SQL-Dialekt, außer Sie erstellen eine SQL Pass-Through-Abfrage. In diesem Fall sollten Sie den Dialekt des Servers verwenden.

Wenn die SQL-Anweisung Parameter für die Abfrage enthält, müssen Sie sie vor der Ausführung festlegen. Wenn Sie die Parameter nicht neu festlegen, werden bei jeder Ausführung der Abfrage jeweils dieselben Parameterwerte verwendet.

In einem Microsoft Access-Arbeitsbereich wird vorzugsweise ein **QueryDef**-Objekt verwendet, um SQL Pass-Through-Vorgänge auf ODBC-Datenquellen auszuführen, die mit einem Microsoft Access-Datenbankmodul verbunden sind. Wenn Sie für das Objekt **QueryDef** die Eigenschaft **[Connect](querydef-connect-property-dao.md)** zu einer ODBC-Datenquelle festlegen, können Sie einen anderen SQL-Dialekt als Microsoft Access-Datenbank-SQL in der Abfrage verwenden und an den externen Server übergeben. Sie können z. B. TRANSACT SQL-Anweisungen verwenden (mit Microsoft SQL Server- oder Sybase SQL Server-Datenbanken), welche das Microsoft Access-Datenbankmodul andernfalls nicht verarbeiten würde.

> [!NOTE]
> Wenn Sie die Eigenschaft auf eine Zeichenfolge festlegen, die mit einem Wert verkettet ist, bei dem es sich nicht um eine Ganzzahl handelt, und die Systemparameter ein anderes als das US-amerikanische Dezimaltrennzeichen festlegen, wie etwa ein Komma (z. B. `strSQL = "PRICE > " & lngPrice, and lngPrice = 125,50`), tritt ein Fehler auf, wenn Sie versuchen, das **QueryDef**-Objekt in einer Microsoft Access-Datenbank auszuführen. Dies liegt daran, dass der Wert während der Verkettung mithilfe des Standard-Dezimaltrennzeichens in eine Zeichenfolge konvertiert wird und Microsoft Access SQL nur US-Dezimaltrennzeichen akzeptiert.

## <a name="example"></a>Beispiel

In diesem Beispiel wird die **SQL** -Eigenschaft veranschaulicht, indem die **SQL** -Eigenschaft eines temporären **QueryDef** -Objekts festgelegt und geändert wird. Zum Ausführen dieser Prozedur ist die SQLOutput-Funktion erforderlich.

```vb
    Sub SQLX() 
     
       Dim dbsNorthwind As Database 
       Dim qdfTemp As QueryDef 
       Dim rstEmployees As Recordset 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       Set qdfTemp = dbsNorthwind.CreateQueryDef("") 
     
       ' Open Recordset using temporary QueryDef object and  
       ' print report. 
       SQLOutput "SELECT * FROM Employees " & _ 
          "WHERE Country = 'USA' " & _ 
          "ORDER BY LastName", qdfTemp 
     
       ' Open Recordset using temporary QueryDef object and  
       ' print report. 
       SQLOutput "SELECT * FROM Employees " & _ 
          "WHERE Country = 'UK' " & _ 
          "ORDER BY LastName", qdfTemp 
     
       dbsNorthwind.Close 
     
    End Sub 
     
    Function SQLOutput(strSQL As String, qdfTemp As QueryDef) 
     
       Dim rstEmployees As Recordset 
     
       ' Set SQL property of temporary QueryDef object and open  
       ' a Recordset. 
       qdfTemp.SQL = strSQL 
       Set rstEmployees = qdfTemp.OpenRecordset 
     
       Debug.Print strSQL 
     
       With rstEmployees 
          ' Enumerate Recordset. 
          Do While Not .EOF 
             Debug.Print "  " & !FirstName & " " & _ 
                !LastName & ", " & !Country 
             .MoveNext 
          Loop 
          .Close 
       End With 
     
    End Function 
```

<br/>

Im folgenden Beispiel wird die **CopyQueryDef**-Methode verwendet, um eine Kopie eines **QueryDef**-Objekts anhand eines vorhandenen **Recordset**-Objekts zu erstellen. Die Kopie wird verändert, indem der **SQL**-Eigenschaft eine Klausel hinzugefügt wird. Wenn Sie ein dauerhaftes **QueryDef**-Objekt erstellen, können der **SQL**-Eigenschaft Leerzeichen, Semikolons oder Zeilenvorschübe hinzugefügt werden. Diese zusätzlichen Zeichen müssen entfernt werden, bevor die neuen Klauseln in die SQL-Anweisung eingefügt werden.

```vb
    Function CopyQueryNew(rstTemp As Recordset, _ 
       strAdd As String) As QueryDef 
     
       Dim strSQL As String 
       Dim strRightSQL As String 
     
       Set CopyQueryNew = rstTemp.CopyQueryDef 
       With CopyQueryNew 
          ' Strip extra characters. 
          strSQL = .SQL 
          strRightSQL = Right(strSQL, 1) 
          Do While strRightSQL = " " Or strRightSQL = ";" Or _ 
                strRightSQL = Chr(10) Or strRightSQL = vbCr 
             strSQL = Left(strSQL, Len(strSQL) - 1) 
             strRightSQL = Right(strSQL, 1) 
          Loop 
          .SQL = strSQL & strAdd 
       End With 
     
    End Function 
```

<br/>

Dieses Beispiel zeigt eine mögliche Verwendung von CopyQueryNew(). 
     
```vb
    Sub CopyQueryDefX() 
     
       Dim dbsNorthwind As Database 
       Dim qdfEmployees As QueryDef 
       Dim rstEmployees As Recordset 
       Dim intCommand As Integer 
       Dim strOrderBy As String 
       Dim qdfCopy As QueryDef 
       Dim rstCopy As Recordset 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       Set qdfEmployees = dbsNorthwind.CreateQueryDef( _ 
          "NewQueryDef", "SELECT FirstName, LastName, " & _ 
          "BirthDate FROM Employees") 
       Set rstEmployees = qdfEmployees.OpenRecordset( _ 
          dbOpenForwardOnly) 
     
       Do While True 
          intCommand = Val(InputBox( _ 
             "Choose field on which to order a new " & _ 
             "Recordset:" & vbCr & "1 - FirstName" & vbCr & _ 
             "2 - LastName" & vbCr & "3 - BirthDate" & vbCr & _ 
             "[Cancel - exit]")) 
          Select Case intCommand 
             Case 1 
                strOrderBy = " ORDER BY FirstName" 
             Case 2 
                strOrderBy = " ORDER BY LastName" 
             Case 3 
                strOrderBy = " ORDER BY BirthDate" 
             Case Else 
                Exit Do 
          End Select 
          Set qdfCopy = CopyQueryNew(rstEmployees, strOrderBy) 
          Set rstCopy = qdfCopy.OpenRecordset(dbOpenSnapshot, _ 
             dbForwardOnly) 
          With rstCopy 
             Do While Not .EOF 
                Debug.Print !LastName & ", " & !FirstName & _ 
                   " - " & !BirthDate 
                .MoveNext 
             Loop 
             .Close 
          End With 
          Exit Do 
       Loop 
     
       rstEmployees.Close 
       ' Delete new QueryDef because this is a demonstration. 
       dbsNorthwind.QueryDefs.Delete qdfEmployees.Name 
       dbsNorthwind.Close 
     
    End Sub 
```

<br/>

In diesem Beispiel werden die **CreateQueryDef**- und die **OpenRecordset**-Methode sowie die **SQL**-Eigenschaft verwendet, um die Tabelle der Titel in der Microsoft SQL Server-Beispieldatenbank "Pubs" abzufragen und den Titel und die Titel-ID des Bestsellers zurückzugeben. Anschließend wird die Tabelle der Autoren abgefragt, und der Benutzer wird angewiesen, einen Bonusscheck an jeden Autor zu senden, der auf dem jeweiligen Tantiemenanteil des Autors basiert (der Gesamtbonus beträgt 1.000 $, und jeder Autor soll einen Prozentsatz dieses Betrags erhalten).

```vb
    Sub ClientServerX2() 
     
       Dim dbsCurrent As Database 
       Dim qdfBestSellers As QueryDef 
       Dim qdfBonusEarners As QueryDef 
       Dim rstTopSeller As Recordset 
       Dim rstBonusRecipients As Recordset 
       Dim strAuthorList As String 
     
       ' Open a database from which QueryDef objects can be  
       ' created. 
       Set dbsCurrent = OpenDatabase("DB1.mdb") 
     
       ' Create a temporary QueryDef object to retrieve 
       ' data from a Microsoft SQL Server database. 
       Set qdfBestSellers = dbsCurrent.CreateQueryDef("") 
       With qdfBestSellers 
          ' Note: The DSN referenced below must be configured to  
          '       use Microsoft Windows NT Authentication Mode to  
          '       authorize user access to the Microsoft SQL Server. 
          .Connect = "ODBC;DATABASE=pubs;DSN=Publishers" 
          .SQL = "SELECT title, title_id FROM titles " & _ 
             "ORDER BY ytd_sales DESC" 
          Set rstTopSeller = .OpenRecordset() 
          rstTopSeller.MoveFirst 
       End With 
     
       ' Create a temporary QueryDef to retrieve data from 
       ' a Microsoft SQL Server database based on the results from 
       ' the first query. 
       Set qdfBonusEarners = dbsCurrent.CreateQueryDef("") 
       With qdfBonusEarners 
          ' Note: The DSN referenced below must be configured to  
          '       use Microsoft Windows NT Authentication Mode to  
          '       authorize user access to the Microsoft SQL Server. 
          .Connect = "ODBC;DATABASE=pubs;DSN=Publishers" 
          .SQL = "SELECT * FROM titleauthor " & _ 
             "WHERE title_id = '" & _ 
             rstTopSeller!title_id & "'" 
          Set rstBonusRecipients = .OpenRecordset() 
       End With 
     
       ' Build the output string. 
       With rstBonusRecipients 
          Do While Not .EOF 
             strAuthorList = strAuthorList & "  " & _ 
                !au_id & ":  $" & (10 * !royaltyper) & vbCr 
             .MoveNext 
          Loop 
       End With 
     
       ' Display results. 
       MsgBox "Please send a check to the following " & _ 
          "authors in the amounts shown:" & vbCr & _ 
          strAuthorList & "for outstanding sales of " & _ 
          rstTopSeller!Title & "." 
     
       rstTopSeller.Close 
       dbsCurrent.Close 
     
    End Sub 
```

<br/>

Das folgende Beispiel zeigt, wie Sie eine Parameterabfrage erstellen. Eine Abfrage mit dem Namen **myQuery** wird mit zwei Parametern mit Namen Param1 und Param2 erstellt. Hierzu wird die SQL-Eigenschaft der Abfrage auf eine SQL-Anweisung (Structured Query Language) festgelegt, welche die Parameter definiert.

**Der Beispielcode stammt von:**[Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

```vb
    Sub CreateQueryWithParameters()
    
        Dim dbs As DAO.Database
        Dim qdf As DAO.QueryDef
        Dim strSQL As String
    
        Set dbs = CurrentDb
        Set qdf = dbs.CreateQueryDef("myQuery")
        Application.RefreshDatabaseWindow
    
        strSQL = "PARAMETERS Param1 TEXT, Param2 INT; "
        strSQL = strSQL & "SELECT * FROM [Table1] "
        strSQL = strSQL & "WHERE [Field1] = [Param1] AND [Field2] = [Param2];"
        qdf.SQL = strSQL
    
        qdf.Close
        Set qdf = Nothing
        Set dbs = Nothing
    
    End Sub
```

<br/>

Das folgende Beispiel zeigt, wie Sie die SQL-Anweisung (Structured Query Language) in einer gespeicherten Abfrage ersetzen.

```vb
    Dim qdf as QueryDef
    Dim db as Database
    Set db = CurrentDB
    Set qdf = db.QueryDefs("YourQueryName")
    qdf.SQL = ReplaceWhereClause(qdf.SQL, strYourNewWhereClause)
    set qdf = Nothing
    set db = Nothing
    
    Public Function ReplaceWhereClause(strSQL As Variant, strNewWHERE As Variant)
    On Error GoTo Error_Handler
    
    ‘This subroutine accepts a valid SQL string and Where clause, and
    ‘returns the same SQL statement with the original Where clause (if any)
    ‘replaced by the passed in Where clause.
    ‘
    ‘INPUT:
    ‘ strSQL valid SQL string to change
    ‘OUTPUT:
    ‘ strNewWHERE New WHERE clause to insert into SQL statement
    ‘
    Dim strSELECT As String, strWhere As String
    Dim strOrderBy As String, strGROUPBY As String, strHAVING As String
    
    Call ParseSQL(strSQL, strSELECT, strWhere, strOrderBy, _
    strGROUPBY, strHAVING)
    
    ReplaceWhereClause = strSELECT &""& strNewWHERE &""_
    & strGROUPBY &""& strHAVING &""& strOrderBy
    
    Exit_Procedure:
      Exit Function
    
    Error_Handler:
      MsgBox (Err.Number & ": " & Err.Description)
      Resume Exit_Procedure
    
    End Function
```
