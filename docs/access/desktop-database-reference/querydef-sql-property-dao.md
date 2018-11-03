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
ms.openlocfilehash: 43acce256d3a46fd7b01122a8502e0af502eb3e9
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25937680"
---
# <a name="querydefsql-property-dao"></a>QueryDef.SQL-Eigenschaft (DAO)

**Betrifft**: Access 2013, Office 2013

Legt die SQL-Anweisung fest, die die Abfrage definiert, die von einem **[QueryDef](querydef-object-dao.md)** -Objekt ausgeführt wird, oder gibt sie zurück.

## <a name="syntax"></a>Syntax

*Ausdruck* . SQL

*Ausdruck* Eine Variable, die ein **QueryDef** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Die **SQL** -Eigenschaft enthält die SQL-Anweisung, die festlegt, wie viele Datensätze ausgewählt, gruppiert und sortiert werden, wenn Sie die Abfrage ausführen. Sie können die Abfrage verwenden, um Datensätze auszuwählen, die in ein **[Recordset](recordset-object-dao.md)** -Objekt einbezogen werden sollen. Sie können auch Aktionsabfragen definieren, um Daten zu ändern, ohne Datensätze zurückzugeben.

Die in einer Abfrage verwendete SQL-Syntax muss dem SQL-Dialekt des Abfragemoduls entsprechen, der vom Typ des Arbeitsbereichs festgelegt wird. In einem Microsoft Access-Arbeitsbereich verwenden Sie den Microsoft Access SQL-Dialekt, außer Sie erstellen eine SQL Pass-Through-Abfrage. In diesem Fall sollten Sie den Dialekt des Servers verwenden.

Wenn die SQL-Anweisung Parameter für die Abfrage enthält, müssen Sie sie vor der Ausführung festlegen. Wenn Sie die Parameter nicht neu festlegen, werden bei jeder Ausführung der Abfrage jeweils dieselben Parameterwerte verwendet.

In einem Microsoft Access-Arbeitsbereich ist Verwenden eines **QueryDef** -Objekts die bevorzugte Methode zum Ausführen von SQL-Pass-Through-Vorgänge auf Microsoft Access-Datenbank-Engine verbundene ODBC-Datenquelle aus. **[Connect](querydef-connect-property-dao.md)** -Eigenschaft des **QueryDef** -Objekts auf einer ODBC-Datenquelle festlegen, können Sie nicht Microsoft – Access-Datenbank von SQL in der Abfrage an den externen Server übergeben werden. Beispielsweise können Sie TRANSACT-SQL-Anweisungen (mit Microsoft SQL Server oder Sybase SQL Server-Datenbanken) verwenden, die Microsoft Access-Datenbankmodul nicht anderweitig verarbeiten würde.

> [!NOTE]
> Wenn Sie die Eigenschaft auf eine Zeichenfolge mit einem nicht-Integer-Wert verkettet festlegen und die Systemparameter einer US-decimal Zeichen wie etwa ein Komma angeben (z. B. `strSQL = "PRICE > " & lngPrice, and lngPrice = 125,50`), ein Fehler ausgegeben, wenn Sie versuchen, das **QueryDef** -Objekt in einem Microsoft ausführen Access-Datenbank. Das geschieht, weil die Zahl während der Verkettung mithilfe des standardmäßigen Dezimalzeichens des Systems in eine Zeichenfolge konvertiert wird und Microsoft Access SQL nur US-amerikanische Dezimalzeichen akzeptiert.

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

Im folgenden Beispiel wird die **CopyQueryDef** -Methode verwendet, um eine Kopie eines **QueryDef** -Objekts anhand eines vorhandenen **Recordset** -Objekts zu erstellen. Die Kopie wird verändert, indem der **SQL** -Eigenschaft eine Klausel hinzugefügt wird. Wenn Sie ein dauerhaftes **QueryDef** -Objekt erstellen, können der **SQL** -Eigenschaft Leerzeichen, Semikolons oder Zeilenvorschübe hinzugefügt werden. Diese zusätzlichen Zeichen müssen entfernt werden, bevor die neuen Klauseln in die SQL-Anweisung eingefügt werden.

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

Dieses Beispiel verwendet die **CreateQueryDef** - und **OpenRecordset** -Methode sowie die **SQL** -Eigenschaft zum Abfragen der Tabelle mit Titeln in der Microsoft SQL Server-Beispieldatenbank „Publikationen" und zum Zurückgeben des Titels und der Titel-ID des Bestsellers. Anschließend wird die Tabelle mit Autoren abgefragt, und der Benutzer wird angewiesen, einen Bonusscheck an jeden Autor zu senden, der auf dem jeweiligen Tantiemenanteil des Autors basiert (der Gesamtbonus beträgt 1.000 $, und jeder Autor soll einen Prozentsatz dieses Betrags erhalten).

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

Das folgende Beispiel zeigt, wie Sie eine Parameterabfrage erstellen. Eine Abfrage namens **MyQuery** wird mit zwei Parameter, mit dem Namen Param1 und Param2 erstellt. Hierzu wird die SQL-Eigenschaft der Abfrage auf eine SQL-Anweisung (Structured Query Language) festgelegt, die die Parameter definiert.

**Beispielcode von** der [Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

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

Das folgende Beispiel zeigt, wie Sie die Structured Query Language (SQL)-Anweisung in einer gespeicherten Abfrage ersetzen.

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
