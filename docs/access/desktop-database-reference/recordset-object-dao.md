---
title: Recordset-Objekt (DAO)
TOCTitle: Recordset Object
ms:assetid: 9774232c-e6da-175b-fc7f-ed2ab7908fa0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197799(v=office.15)
ms:contentKeyID: 48546469
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a4ce9b3480cfa2a8eb074065016131e2c82752c3
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25921129"
---
# <a name="recordset-object-dao"></a>Recordset-Objekt (DAO)

**Betrifft**: Access 2013, Office 2013

Ein **Recordset** -Objekt stellt die Datensätze in einer Basistabelle oder die Datensätze dar, die aus einer Abfrageausführung resultieren.

## <a name="remarks"></a>Hinweise

Sie verwenden **Recordset** -Objekte, um Daten in einer Datenbank auf Datensatzebene zu ändern. Wenn Sie DAO-Objekte verwenden, ändern Sie Daten fast ausschließlich mit **Recordset** -Objekten. Alle **Recordset** -Objekte werden mit Datensätzen (Zeilen) und Feldern (Spalten) erstellt. Es gibt von Typen von **Recordset** -Objekten:

- Tabellentyp-Recordset: Darstellung im Code einer Basistabelle, den Sie verwenden können, um Datensätze in einer einzelnen Datenbanktabelle hinzuzufügen, zu ändern oder zu löschen (nur Microsoft Access-Arbeitsbereiche).

- Recordset vom "dynaset"-Typ: das Ergebnis einer Abfrage, die aktualisierbare Datensätze haben kann. Ein **Recordset** -Objekt vom "dynaset"-Typ ist eine dynamische Gruppe mit Datensätzen, die Sie verwenden können, um Datensätze aus einer zugrunde liegenden Tabelle oder zugrunde liegenden Tabellen hinzuzufügen, zu ändern oder zu löschen. Ein **Recordset** -Objekt vom "dynaset"-Typ kann Felder aus mindestens einer Tabelle in einer Datenbank enthalten. Der Typ entspricht einem ODBC-Keysetcursor.

- Recordset vom "snapshot"-Typ: eine statische Kopie einer Datensatzgruppe, die Sie verwenden können, um Daten zu suchen oder Berichte zu generieren. Ein **Recordset** -Objekt vom "snapshot"-Typ kann Felder aus mindestens einer Tabelle in einer Datenbank enthalten, kann aber nicht aktualisiert werden. Dieser Typ entspricht einem statischen ODBC-Cursor.

- Recordset vom "forward-only"-Typ: identnisch zum "snapshot"-Typ mit der Ausnahme, dass kein Cursor bereitgestellt wird. Sie können nur vorwärts durch Datensätze blättern. Auf diese Weise wird die Leistung in Situationen verbessert, in denen Sie ein Resultset lediglich einmal durchlaufen müssen. Dieser Typ entspricht einem ODBC-Cursor vom "forward-only"-Typ.

- Recordset vom "dynamic"-Typ: eine Abfragergebnisgruppe aus mindestens einer Basistabelle, in der Sie Datensätze einer Abfrage, die Zeilen zurückgibt, hinzufügen, ändern oder löschen können. Außerdem werden Datensätze, die andere Benutzer in den Basistabellen hinzufügen, löschen oder bearbeiten, ebenfalls im **Recordset** angezeigt. Dieser Typ entspricht einem dynamischen ODBC-Cursor (nur ODBCDirect-Arbeitsbereiche).

> [!NOTE]
> [!HINWEIS] ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt. Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul zu verwenden.

Sie können den Typ des **Recordset** -Objekts auswählen, den, die Sie mit dem Argument Type der **OpenRecordset** -Methode erstellen möchten.

In Microsoft Access-Arbeitsbereich Wenn Sie nicht, dass ein DAO Versuche zum Erstellen des Typs des **Recordset-Objekts** mit der meisten Funktionen zur Verfügung angeben, beginnend mit Table. Falls dieser Typ nicht verfügbar ist, probiert DAO ein "dynaset"-, dann ein "snapshot"- und schließlich ein "forward-only"- **Recordset** -Objekt aus.

In einem ODBCDirect-Arbeitsbereich Wenn Sie einen Typ nicht angeben versucht DAO den Typ des **Recordset-Objekts** mit die schnellstmögliche Antwortzeit für die Abfrage erstellen beginnend mit Vorwärtscursor. Falls dieser Typ nicht verfügbar ist, probiert DAO ein "snapshot"-, dann ein "dynaset"- und schließlich ein "dynamic"- **Recordset** -Objekt aus.

Wenn Sie ein **Recordset** -Objekt mit einem nicht verknüpften **[TableDef](tabledef-object-dao.md)** -Objekt in einem Microsoft Access-Arbeitsbereich erstellen, werden **Recordset** -Objekte vom "table"-Typ erstellt. Nur **Recordset** -Objekte vom "dynaset"- oder "snapshot"-Typ können mit verknüpften Tabellen oder Tabellen in ODBC-Datenbanken mit verbundenem Microsoft Access-Datenbankmodul erstellt werden.

Ein neues **Recordset** -Objekt wird automatisch der **Recordsets** -Auflistung hinzugefügt, wenn Sie das Objekt öffnen, und wird automatisch entfernt, wenn Sie das Objekt schließen.

> [!NOTE]
> [!HINWEIS] Wenn Sie Variablen verwenden, um ein **Recordset** -Objekt darzustellen, und das **Database** -Objekt das **Recordset** enthält, stellen Sie sicher, dass die Variablen den gleichen Umfang bzw. die gleiche Lebenszeit aufweisen. Wenn Sie beispielsweise eine öffentliche Variable deklarieren, die ein **Recordset** -Objekt darstellt, stellen Sie sicher, dass die Variable, die das **Database** -Objekt mit dem **Recordset** enthält, ebenfalls öffentlich ist oder in einer **Sub** - oder **Function** -Prozedur mit dem **Static** -Schlüsselwort deklariert wird.

Sie können beliebig viele **Recordset** -Objektvariablen erstellen. Unterschiedliche **Recordset** -Objekte können auf die gleichen Tabellen, Abfragen und Felder ohne Konflikte zugreifen.

Dynaset, Snapshot und Weiterleiten Typ **Recordset** -Objekte werden im lokalen Arbeitsspeicher gespeichert. Wenn zum Speichern dieser Daten im lokalen Arbeitsspeicher nicht genug Platz verfügbar ist, speichert das Microsoft Access-Datenbankmodul die zusätzlichen Daten in das Festplattenverzeichnis TEMP. Wenn dieser Platz aufgebraucht ist, tritt ein verfolgbarer Fehler auf.

Die Standardauflistung eines **Recordset** -Objekts ist die **Fields** -Auflistung und die Standardeigenschaft eines **[Field](field-object-dao.md)** -Objekts ist die **[Value](field-value-property-dao.md)** -Eigenschaft. Verwenden Sie diese Standardeinstellungen, um Ihren Code zu vereinfachen.

Wenn Sie ein **Recordset** -Objekt erstellen, wird der aktuelle Datensatz als erster Datensatz positioniert, falls Datensätze vorhanden sind. Falls keine Datensätze vorhanden sind, lautet die Einstellung der **RecordCount** -Eigenschaft "0", und die Einstellungen der **BOF** - und **EOF** -Eigenschaften sind **True**.

Sie können die Methoden **MoveNext**, **MovePrevious**, **MoveFirst** und **MoveLast** verwenden, um den aktuellen Datensatz neu zu positionieren. "Forward-only"-**Recordset**-Objekte unterstützen nur die **MoveNext**-Methode. Wenn Sie die Move-Methoden verwenden, um die einzelnen Datensätze aufzurufen (oder das **Recordset** "durchlaufen"), können Sie die **BOF**- und **EOF**-Eigenschaften verwenden, um nach dem Anfang oder Ende des **Recordset**-Objekts zu suchen.

Mit "dynaset"- und "snapshot"- **Recordset** -Objekten in einem Microsoft Access-Arbeitsbereich können Sie auch die Find-Methoden verwenden, zum Beispiel **FindFirst**, um einen bestimmten Datensatz basierend auf Kriterien zu suchen. Falls der Datensatz nicht gefunden wird, wird die **NoMatch** -Eigenschaft auf **True** festgelegt. Für **Recordset** -Objekte vom "table"-Typ können Sie Datensätze mithilfe der **Seek** -Methode suchen.

Die **Type** -Eigenschaft gibt den Typ des erstellten **Recordset** -Objekts an und die **Updatable** -Eigenschaft gibt an, ob Sie die Datensätze des Objekts ändern können.

Informationen zur Struktur einer Basistabelle, zum Beispiel zu den Namen und Datentypen der einzelnen **Field** -Objekte und **Index** -Objekte, werden in einem **TableDef** -Objekt gespeichert.

Wenn Sie auf ein **Recordset**-Objekt in einer Auflistung mit seiner Ordnungszahl oder mit der Einstellung seiner **Name**-Eigenschaft verweisen möchten, verwenden Sie eine der folgenden Syntaxformen:

- **Recordsets**(0)

- **Recordset-Objekte** ("Name")

- **Recordsets**\!\[Namen\]

> [!NOTE]
> [!HINWEIS] Sie können ein **Recordset**-Objekt derselben Datenquelle oder Datenbank mehrmals öffnen und dabei doppelte Namen in der **Recordsets**-Auflistung erstellen. Sie sollten Objektvariablen **Recordset**-Objekte zuweisen und mit Variablennamen auf sie verweisen.

## <a name="example"></a>Beispiel

Dieses Beispiel demonstriert **Recordset** -Objekte und die **Recordsets** -Auflistung durch Öffnen von vier verschiedenen **Recordsets**, Aufzählen der Recordsets-Auflistung des aktuellen **Database** -Objekts und Aufzählen der **Properties** -Auflistung jedes **Recordset** -Objekts.

```vb
    Sub RecordsetX() 
     
       Dim dbsNorthwind As Database 
       Dim rstTable As Recordset 
       Dim rstDynaset As Recordset 
       Dim rstSnapshot As Recordset 
       Dim rstForwardOnly As Recordset 
       Dim rstLoop As Recordset 
       Dim prpLoop As Property 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
       With dbsNorthwind 
     
          ' Open one of each type of Recordset object. 
          Set rstTable = .OpenRecordset("Categories", _ 
             dbOpenTable) 
          Set rstDynaset = .OpenRecordset("Employees", _ 
             dbOpenDynaset) 
          Set rstSnapshot = .OpenRecordset("Shippers", _ 
             dbOpenSnapshot) 
          Set rstForwardOnly = .OpenRecordset _  
             ("Employees", dbOpenForwardOnly) 
     
          Debug.Print "Recordsets in Recordsets " & _ 
             "collection of dbsNorthwind" 
     
          ' Enumerate Recordsets collection. 
          For Each rstLoop In .Recordsets 
     
             With rstLoop 
                Debug.Print "  " & .Name 
     
                ' Enumerate Properties collection of each 
                ' Recordset object. Trap for any  
                ' properties whose values are invalid in  
                ' this context. 
                For Each prpLoop In .Properties 
                   On Error Resume Next 
                   If prpLoop <> "" Then Debug.Print _ 
                      "    " & prpLoop.Name & _ 
                      " = " & prpLoop 
                   On Error GoTo 0 
                Next prpLoop 
     
             End With 
     
          Next rstLoop 
     
          rstTable.Close 
          rstDynaset.Close 
          rstSnapshot.Close 
          rstForwardOnly.Close 
     
          .Close 
       End With 
     
    End Sub 
```

<br/>

Dieses Beispiel verwendet die **OpenRecordset** -Methode, um fünf verschiedene **Recordset** -Objekte zu öffnen und ihre Inhalte anzuzeigen. Die OpenRecordsetOutput-Prozedur ist für die Ausführung dieser Prozedur erforderlich.

```vb
    Sub OpenRecordsetX() 
     
       Dim wrkAcc As Workspace 
       Dim wrkODBC As Workspace 
       Dim dbsNorthwind As Database 
       Dim conPubs As Connection 
       Dim rstTemp As Recordset 
       Dim rstTemp2 As Recordset 
     
       ' Open Microsoft Access and ODBCDirect workspaces, Microsoft  
       ' Access database, and ODBCDirect connection. 
       Set wrkAcc = CreateWorkspace("", "admin", "", dbUseJet) 
       Set wrkODBC = CreateWorkspace("", "admin", "", dbUseODBC) 
       Set dbsNorthwind = wrkAcc.OpenDatabase("Northwind.mdb") 
        
       ' Note: The DSN referenced below must be set to  
       '       use Microsoft Windows NT Authentication Mode to  
       '       authorize user access to the Microsoft SQL Server. 
       Set conPubs = wrkODBC.OpenConnection("", , , _ 
          "ODBC;DATABASE=pubs;DSN=Publishers") 
     
       ' Open five different Recordset objects and display the  
       ' contents of each. 
     
       Debug.Print "Opening forward-only-type recordset " & _ 
          "where the source is a QueryDef object..." 
       Set rstTemp = dbsNorthwind.OpenRecordset( _ 
          "Ten Most Expensive Products", dbOpenForwardOnly) 
       OpenRecordsetOutput rstTemp 
     
       Debug.Print "Opening read-only dynaset-type " & _ 
          "recordset where the source is an SQL statement..." 
       Set rstTemp = dbsNorthwind.OpenRecordset( _ 
          "SELECT * FROM Employees", dbOpenDynaset, dbReadOnly) 
       OpenRecordsetOutput rstTemp 
     
       ' Use the Filter property to retrieve only certain  
       ' records with the next OpenRecordset call. 
       Debug.Print "Opening recordset from existing " & _ 
          "Recordset object to filter records..." 
       rstTemp.Filter = "LastName >= 'M'" 
       Set rstTemp2 = rstTemp.OpenRecordset() 
       OpenRecordsetOutput rstTemp2 
     
       Debug.Print "Opening dynamic-type recordset from " & _ 
          "an ODBC connection..." 
       Set rstTemp = conPubs.OpenRecordset( _ 
          "SELECT * FROM stores", dbOpenDynamic) 
       OpenRecordsetOutput rstTemp 
     
       ' Use the StillExecuting property to determine when the  
       ' Recordset is ready for manipulation. 
       Debug.Print "Opening snapshot-type recordset based " & _ 
          "on asynchronous query to ODBC connection..." 
       Set rstTemp = conPubs.OpenRecordset("publishers", _ 
          dbOpenSnapshot, dbRunAsync) 
       Do While rstTemp.StillExecuting 
          Debug.Print "  [still executing...]" 
       Loop 
       OpenRecordsetOutput rstTemp 
     
       rstTemp.Close 
       dbsNorthwind.Close 
       conPubs.Close 
       wrkAcc.Close 
       wrkODBC.Close 
     
    End Sub 
     
    Sub OpenRecordsetOutput(rstOutput As Recordset) 
     
       ' Enumerate the specified Recordset object. 
       With rstOutput 
          Do While Not .EOF 
             Debug.Print , .Fields(0), .Fields(1) 
             .MoveNext 
          Loop 
       End With 
     
    End Sub 
```

<br/>

Dieses Beispiel öffnet ein **Recordset** -Objekt vom "dynamic"-Typ und zählt seine Datensätze auf.

```vb
    Sub dbOpenDynamicX() 
     
       Dim wrkMain As Workspace 
       Dim conMain As Connection 
       Dim qdfTemp As QueryDef 
       Dim rstTemp As Recordset 
       Dim strSQL As String 
       Dim intLoop As Integer 
     
       ' Create ODBC workspace and open connection to 
       ' SQL Server database. 
       Set wrkMain = CreateWorkspace("ODBCWorkspace", _ 
          "admin", "", dbUseODBC) 
           
       ' Note: The DSN referenced below must be configured to  
       '       use Microsoft Windows NT Authentication Mode to  
       '       authorize user access to the Microsoft SQL Server.     
       Set conMain = wrkMain.OpenConnection("Publishers", _ 
          dbDriverNoPrompt, False, _ 
          "ODBC;DATABASE=pubs;DSN=Publishers") 
           
       ' Open dynamic-type recordset. 
       Set rstTemp = _ 
          conMain.OpenRecordset("authors", _ 
          dbOpenDynamic) 
     
       With rstTemp 
          Debug.Print "Dynamic-type recordset: " & .Name 
     
          ' Enumerate records. 
          Do While Not .EOF 
             Debug.Print "    " & !au_lname & ", " & _ 
                !au_fname 
             .MoveNext 
          Loop 
     
          .Close 
       End With 
     
       conMain.Close 
       wrkMain.Close 
     
    End Sub 
```

<br/>

Dieses Beispiel öffnet ein **Recordset** vom "dynaset"-Typ und zeigt den Umfang, in dem die Felder aktualisierbar sind.

```vb
    Sub dbOpenDynasetX() 
     
       Dim dbsNorthwind As Database 
       Dim rstInvoices As Recordset 
       Dim fldLoop As Field 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       Set rstInvoices = _ 
          dbsNorthwind.OpenRecordset("Invoices", dbOpenDynaset) 
     
       With rstInvoices 
          Debug.Print "Dynaset-type recordset: " & .Name 
     
          If .Updatable Then 
             Debug.Print "  Updatable fields:" 
     
             ' Enumerate Fields collection of dynaset-type 
             ' Recordset object, print only updatable 
             ' fields. 
             For Each fldLoop In .Fields 
                If fldLoop.DataUpdatable Then 
                   Debug.Print "    " & fldLoop.Name 
                End If 
             Next fldLoop 
     
          End If 
     
          .Close 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub 
```

<br/>

Dieses Beispiel öffnet ein **Recordset** vom "forward-only"-Typ, demonstriert die schreibgeschützten Merkmale und durchläuft das **Recordset** mit der **MoveNext** -Methode.

```vb 
Sub dbOpenForwardOnlyX() 
 
   Dim dbsNorthwind As Database 
   Dim rstEmployees As Recordset 
   Dim fldLoop As Field 
 
   Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
   ' Open a forward-only-type Recordset object. Only the  
   ' MoveNext and Move methods may be used to navigate  
   ' through the recordset. 
   Set rstEmployees = _ 
      dbsNorthwind.OpenRecordset("Employees", _ 
      dbOpenForwardOnly) 
 
   With rstEmployees 
      Debug.Print "Forward-only-type recordset: " & _ 
         .Name & ", Updatable = " & .Updatable 
 
      Debug.Print "  Field - DataUpdatable" 
      ' Enumerate Fields collection, printing the Name and  
      ' DataUpdatable properties of each Field object. 
      For Each fldLoop In .Fields 
         Debug.Print "    " & _ 
            fldLoop.Name & " - " & fldLoop.DataUpdatable 
      Next fldLoop 
 
      Debug.Print "  Data" 
      ' Enumerate the recordset. 
      Do While Not .EOF 
         Debug.Print "    " & !FirstName & " " & _ 
            !LastName 
         .MoveNext 
      Loop 
 
      .Close 
   End With 
 
   dbsNorthwind.Close 
 
End Sub 
```

<br/>

Dieses Beispiel öffnet ein **Recordset** vom "snapshot"-Typ und demonstriert die schreibgeschützten Merkmale.

```vb
    Sub dbOpenSnapshotX() 
     
       Dim dbsNorthwind As Database 
       Dim rstEmployees As Recordset 
       Dim prpLoop As Property 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       Set rstEmployees = _ 
          dbsNorthwind.OpenRecordset("Employees", _ 
          dbOpenSnapshot) 
     
       With rstEmployees 
          Debug.Print "Snapshot-type recordset: " & _ 
             .Name 
     
          ' Enumerate the Properties collection of the 
          ' snapshot-type Recordset object, trapping for 
          ' any properties whose values are invalid in  
          ' this context. 
          For Each prpLoop In .Properties 
             On Error Resume Next 
             Debug.Print "  " & _ 
                prpLoop.Name & " = " & prpLoop 
             On Error Goto 0 
          Next prpLoop 
     
          .Close 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub 
```

<br/>

Dieses Beispiel öffnet ein **Recordset** vom "table"-Typ, legt die **Index** -Eigenschaft fest und zählt die Datensätze auf.

```vb
    Sub dbOpenTableX() 
     
       Dim dbsNorthwind As Database 
       Dim rstEmployees As Recordset 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       ' dbOpenTable is default. 
       Set rstEmployees = _ 
          dbsNorthwind.OpenRecordset("Employees") 
     
       With rstEmployees 
          Debug.Print "Table-type recordset: " & .Name 
     
          ' Use predefined index. 
          .Index = "LastName" 
          Debug.Print "  Index = " & .Index 
     
          ' Enumerate records. 
          Do While Not .EOF 
             Debug.Print "    " & !LastName & ", " & _ 
                !FirstName 
             .MoveNext 
          Loop 
     
          .Close 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub 
```

<br/>

Das folgende Beispiel zeigt das Verwenden der Seek-Methode zum Suchen eines Datensatzes in einer verknüpften Tabelle.

**Beispielcode von** der [Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).


```vb
    Sub TestSeek()
        ' Get the path to the external database that contains
        ' the tblCustomers table we're going to search.
        Dim strMyExternalDatabase
        Dim dbs    As DAO.Database
        Dim dbsExt As DAO.Database
        Dim rst    As DAO.Recordset
        Dim tdf    As DAO.TableDef
        
        Set dbs = CurrentDb()
        Set tdf = dbs.TableDefs("tblCustomers")
        strMyExternalDatabase = Mid(tdf.Connect, 11)
        
        'Open the database that contains the table that is linked
        Set dbsExt = OpenDatabase(strMyExternalDatabase)
        
        'Open a table-type recordset against the external table
        Set rst = dbsExt.OpenRecordset("tblCustomers", dbOpenTable)
        
        'Specify which index to search on
        rst.Index = "PrimaryKey"
        
        'Specify the criteria
        rst.Seek "=", 123
        
        'Check the result
        If rst.NoMatch Then
            MsgBox "Record not found."
        Else
            MsgBox "Customer name: " & rst!CustName
        End If
        
        rst.Close
        dbs.Close
        dbsExt.Close
        Set rst = Nothing
        Set tdf = Nothing
        Set dbs = Nothing
        
        
    End Sub
```

<br/>

The following example shows how to open a Recordset that is based on a parameter query.

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

Das folgende Beispiel zeigt das Öffnen eines Recordset, das auf einer Tabelle oder Abfrage basiert.

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

Das folgende Beispiel zeigt das Öffnen eines Recordset, das auf einer SQL-Anweisung (Structured Query Language) basiert.

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

Das folgende Beispiel zeigt das Verwenden der FindFirst- und FindNext-Methoden zum Suchen eines Datensatzes in einem Recordset.

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

<br/>

Das folgende Beispiel zeigt das Kopieren der Ergebnisse einer Abfrage in ein Arbeitsblatt in einer neuen Microsoft Excel-Arbeitsmappe.

```vb
    Public Sub CopyDataFromQuery( _
        xlApp As Excel.Application, _
        strQueryName As String)
    
        ' If the xlApp object exists
        If Not xlApp Is Nothing Then
        
            ' If the Workbook exists
            If xlApp.Workbooks.Count = 1 Then
            
                ' Create Recrodset Object from the Query
                Dim rsQuery As DAO.Recordset
                Set rsQuery = Application.CurrentDb.OpenRecordset(strQueryName)
                
                ' Get the Cells object
                Dim Cells As Object
                Set Cells = xlApp.Workbooks(1).ActiveSheet.Cells
                
                ' Copy the Data from the Query into the Sheet
                Cells.CopyFromRecordset rsQuery
                
            End If
        End If
    
    End Sub
```

