---
title: Database.CreateQueryDef-Methode (DAO)
TOCTitle: CreateQueryDef Method
ms:assetid: 75ee7cac-dcd0-b4c5-b55b-9cbaaae2cbf0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195966(v=office.15)
ms:contentKeyID: 48545686
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: high
ms.openlocfilehash: 6ae1b84a3f1d99483c3ea1d7f54458ed53e8c4fe
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59558520"
---
# <a name="databasecreatequerydef-method-dao"></a>Database.CreateQueryDef-Methode (DAO)

**Gilt für**: Access 2013, Office 2013

Erstellt ein neues **[QueryDef](querydef-object-dao.md)**-Objekt.

## <a name="syntax"></a>Syntax

*expression* .CreateQueryDef(***Name** _, _*_SQLText_**)

*Ausdruck* Eine Variable, die ein **Database** -Objekt darstellt.

## <a name="parameters"></a>Parameter

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Name</p></th>
<th><p>Erforderlich/optional</p></th>
<th><p>Datentyp</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Name</em></p></td>
<td><p>Optional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Eine <strong>Variant</strong> (Untertyp <strong>String</strong>), die die neue <strong>QueryDef</strong> eindeutig benennt.</p></td>
</tr>
<tr class="even">
<td><p><em>SQLText</em></p></td>
<td><p>Optional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Ein <strong>Variant</strong>-Wert (Untertyp <strong>String</strong>), bei dem es sich um eine SQL-Anweisung handelt, die das <strong>QueryDef</strong>-Objekt definiert. Wenn Sie dieses Argument nicht angeben, können Sie das <strong>QueryDef</strong>-Objekt definieren, indem Sie seine <strong><a href="querydef-sql-property-dao.md">SQL</a></strong>-Eigenschaft festlegen, bevor oder nachdem Sie es an eine Auflistung anfügen.</p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>Rückgabewert

QueryDef

## <a name="remarks"></a>Bemerkungen

Wenn Sie in einem Microsoft Access-Arbeitsbereich bei der Erstellung einer **QueryDef** einen anderen Wert als eine Zeichenfolge der Länge 0 (null) für den Namen angeben, wird das resultierende **QueryDef**-Objekt automatisch an die **[QueryDefs](querydefs-collection-dao.md)**-Auflistung angefügt.

Wenn das durch Namen angegebene Objekt schon ein Mitglied der **QueryDefs** -Auflistung ist, tritt ein Laufzeitfehler auf. Sie können eine temporäre **QueryDef** erstellen, indem Sie beim Ausführen der **CreateQueryDef** -Methode eine Zeichenfolge der Länge 0 (null) für das Namenargument verwenden. Ein andere Methode besteht darin, die **[Name](querydef-name-property-dao.md)** -Eigenschaft einer neu erstellten **QueryDef** auf eine Zeichenfolge der Länge 0 ("") festzulegen.  

Temporäre **QueryDef** -Objekte sind nützlich, wenn Sie dynamische SQL-Anweisungen wiederholt verwenden möchten, ohne neue dauerhafte Objekte in der **QueryDefs** -Auflistung erstellen zu müssen. Sie können eine temporäre **QueryDef** nicht an jede Auflistung anhängen, da eine Zeichenfolge der Länge NULL kein gültiger Name für ein permanentes **QueryDef** -Objekt ist. Sie können jederzeit  den **Namen** und die **SQL** -Eigenschaften des zuletzt erstellten **QueryDef** -Objektes festlegen und so das **QueryDef** der **QueryDefs** -Auflistung anhängen.

Zum Ausführen der SQL-Anweisung in einem **QueryDef**-Objekt verwenden Sie die **[Execute](querydef-execute-method-dao.md)**- oder die **[OpenRecordset](database-openrecordset-method-dao.md)**-Methode.

Die Verwendung eines **QueryDef**-Objekts ist das bevorzugte Verfahren zum Ausführen von SQL-Pass-Through-Abfragen mit ODBC-Datenbanken.

Um ein **QueryDef**-Objekt aus einer **QueryDefs**-Auflistung in einer Datenbank des Microsoft Access-Datenbankmoduls zu entfernen, führen Sie die **[Delete](querydefs-delete-method-dao.md)**-Methode für die Auflistung aus.

## <a name="example"></a>Beispiel

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
