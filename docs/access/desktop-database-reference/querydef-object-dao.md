---
title: QueryDef-Objekt (DAO)
TOCTitle: QueryDef Object
ms:assetid: 0b3d901c-345d-42a2-f5f1-fb09cc562e27
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845129(v=office.15)
ms:contentKeyID: 48543169
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 18889846b2f55fa13f9fa5fe002f233c955d9866
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25929951"
---
# <a name="querydef-object-dao"></a>QueryDef-Objekt (DAO)

**Gilt für:** Access 2013 | Office 2013 

Ein **QueryDef** -Objekt ist eine gespeicherte Definition einer Abfrage in einer Datenbank des Microsoft Access-Datenbankmoduls.

## <a name="remarks"></a>Hinweise

Sie können das **QueryDef** -Objekt verwenden, um eine Abfrage zu definieren. Sie haben beispielsweise folgende Möglichkeiten:

- Verwenden der **SQL** -Eigenschaft, um die Abfragedefinition festzulegen oder zurückzugeben.

- Verwenden der **Parameters** -Auflistung des **QueryDef** -Objekts, um Abfrageparameter festzulegen oder zurückzugeben.

- Verwenden der **Type** -Eigenschaft, um einen Wert zurückzugeben, der angibt, ob die Abfrage Datensätze aus einer vorhandenen Tabelle auswählt, eine neue Tabelle erstellt, Datensätze aus einer Tabelle in einer anderen Tabelle eingefügt, Datensätze löscht oder Datensätze aktualisiert.

- Verwenden der **MaxRecords** -Eigenschaft, um die Anzahl der von einer Abfrage zurückgegebenen Datensätze zu beschränken.

- Verwenden der **ODBCTimeout** -Eigenschaft, um anzugeben, wie lange gewartet werden soll, bevor die Abfrage Datensätze zurückgibt. Die **ODBCTimeout** -Eigenschaft gilt für alle Abfragen, die auf ODBC-Daten zugreifen.

- Verwenden der **ReturnsRecords** -Eigenschaft, um anzugeben, dass die Abfrage Datensätze zurückgibt. Die **ReturnsRecords** -Eigenschaft gilt nur für SQL-Pass-Through-Abfragen.

- Verwenden der **Connect** -Eigenschaft, um eine SQL-Pass-Through-Abfrage für eine ODBC-Datenbank durchzuführen.

Sie können auch temporäre **QueryDef** -Objekte erstellen. Im Gegensatz zu dauerhaften **QueryDef** -Objekten werden temporäre **QueryDef** -Objekte nicht auf Datenträger gespeichert oder an die **QueryDefs** -Auflistung angefügt. Temporäre **QueryDef** -Objekte sind für Abfragen nützlich, die Sie während der Laufzeit wiederholt ausführen, jedoch nicht auf einem Datenträger speichern müssen, insbesondere, wenn Sie die SQL-Anweisungen zur Laufzeit erstellen.

Sie können sich ein dauerhaftes **QueryDef** -Objekt in einem Microsoft Access-Arbeitsbereich als kompilierte SQL-Anweisung vorstellen. Wenn Sie eine Abfrage über ein dauerhaftes **QueryDef** -Objekt ausführen, wird die Abfrage schneller ausgeführt als die entsprechende SQL-Anweisung über die **OpenRecordset** -Methode. Dies liegt daran, das das Microsoft Access-Datenbankmodul die Abfrage vor der Ausführung nicht kompilieren muss.

Die bevorzugte Methode zum Verwenden des systemeigenen SQL-Dialekts eines externen Datenbankmoduls, auf das über das Microsoft Access-Datenbankmodul zugegriffen wird, ist über **QueryDef** -Objekte. Sie können z. B. eine Microsoft SQL Server-Abfrage erstellen und in einem **QueryDef** -Objekt speichern. Wenn Sie eine SQL-Abfrage aus einem anderen als dem Microsoft Access-Datenbankmodul verwenden möchten, müssen Sie eine **Connect** -Eigenschaftenzeichenfolge angeben, die auf die externe Datenquelle verweist. Abfragen mit gültigen **Connect** -Eigenschaften umgehen das Microsoft Access-Datenbankmodul und übergeben die Abfrage direkt zur Verarbeitung an den externen Datenbankserver.

Verwenden Sie zum Erstellen eines neuen **QueryDef** -Objekts die **CreateQueryDef** -Methode. In Microsoft Access-Arbeitsbereich erstellen Wenn Sie eine Zeichenfolge für das Namenargument bereitstellen oder wenn Sie die **Name** -Eigenschaft das neue **QueryDef** -Objekt explizit auf eine nicht – leere Zeichenfolge festgelegt Sie eine permanente **QueryDef-Objekt** , das automatisch an die **QueryDefs** -Auflistung angefügt und auf dem Datenträger gespeichert werden. Bereitstellung eine leere Zeichenfolge als Argument für den Namen oder die **Name** -Eigenschaft auf eine leere Zeichenfolge explizit festlegen führt zu einem temporäre **QueryDef** -Objekt.

Verwenden Sie eine der folgenden Syntaxformen, um auf ein **QueryDef** -Objekt in einer Auflistung anhand seiner Ordnungszahl oder seiner Einstellung der **Name** -Eigenschaft zu verweisen:

QueryDefs(0)

QueryDefs("name")

QueryDefs\! \[ Namen\]

Auf temporäre **QueryDef** -Objekte können Sie nur anhand der Objektvariablen verweisen, die Sie diesen zugewiesen haben.

**Link bereitgestellt, von** der Community [UtterAccess](https://www.utteraccess.com) . UtterAccess ist das führende Microsoft Access-Wiki und -Hilfeforum.

- [Abfragen: Dokument SQL zu Word](https://www.utteraccess.com/wiki/index.php/queries:_document_sql_to_word)

## <a name="example"></a>Beispiel

Mit diesem Beispiel wird ein neues **QueryDef** -Objekt erstellt, das an die **QueryDefs** -Auflistung des **Database** -Objekts der Northwind-Datenbank angehängt wird. Anschließend werden die **QueryDefs** -Auflistung und die **Properties** -Auflistung des neuen **QueryDef** -Objekts aufgeführt.

```vb
    Sub QueryDefX() 
     
       Dim dbsNorthwind As Database 
       Dim qdfNew As QueryDef 
       Dim qdfLoop As QueryDef 
       Dim prpLoop As Property 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
       ' Create new QueryDef object. Because it has a  
       ' name, it is automatically appended to the  
       ' QueryDefs collection. 
       Set qdfNew = dbsNorthwind.CreateQueryDef("NewQueryDef", _ 
             "SELECT * FROM Categories") 
     
       With dbsNorthwind 
          Debug.Print .QueryDefs.Count & _ 
             " QueryDefs in " & .Name 
     
          ' Enumerate QueryDefs collection. 
          For Each qdfLoop In .QueryDefs 
             Debug.Print "  " & qdfLoop.Name 
          Next qdfLoop 
     
          With qdfNew 
             Debug.Print "Properties of " & .Name 
     
             ' Enumerate Properties collection of new  
             ' QueryDef object. 
             For Each prpLoop In .Properties 
                On Error Resume Next 
                Debug.Print "  " & prpLoop.Name & " - " & _ 
                   IIf(prpLoop = "", "[empty]", prpLoop) 
                On Error Goto 0 
             Next prpLoop 
          End With 
     
          ' Delete new QueryDef because this is a  
          ' demonstration. 
          .QueryDefs.Delete qdfNew.Name 
          .Close 
       End With 
     
    End Sub 
```

<br/>

In diesem Beispiel wird die **CreateQueryDef** -Methode verwendet, um ein temporäres und ein dauerhaftes **QueryDef** -Objekt zu erstellen und auszuführen. Die GetrstTemp-Funktion wird zur Ausführung dieses Verfahrens benötigt.

```vb
    Sub CreateQueryDefX() 
     
       Dim dbsNorthwind As Database 
       Dim qdfTemp As QueryDef 
       Dim qdfNew As QueryDef 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
       With dbsNorthwind 
          ' Create temporary QueryDef. 
          Set qdfTemp = .CreateQueryDef("", _ 
             "SELECT * FROM Employees") 
          ' Open Recordset and print report. 
          GetrstTemp qdfTemp 
          ' Create permanent QueryDef. 
          Set qdfNew = .CreateQueryDef("NewQueryDef", _ 
             "SELECT * FROM Categories") 
          ' Open Recordset and print report. 
          GetrstTemp qdfNew 
          ' Delete new QueryDef because this is a demonstration. 
          .QueryDefs.Delete qdfNew.Name 
          .Close 
       End With 
     
    End Sub 
     
    Function GetrstTemp(qdfTemp As QueryDef) 
     
       Dim rstTemp As Recordset 
     
       With qdfTemp 
          Debug.Print .Name 
          Debug.Print "  " & .SQL 
          ' Open Recordset from QueryDef. 
          Set rstTemp = .OpenRecordset(dbOpenSnapshot) 
     
          With rstTemp 
             ' Populate Recordset and print number of records. 
             .MoveLast 
             Debug.Print "  Number of records = " & _ 
                .RecordCount 
             Debug.Print 
             .Close 
          End With 
     
       End With 
     
    End Function 
```

<br/>

Das folgende Beispiel zeigt, wie Sie die Structured Query Language (SQL)-Anweisung in einer gespeicherten Abfrage ersetzen.

**Beispielcode von** der [Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

```vb
    ‘To change the Where clause in a saved query  
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

