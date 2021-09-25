---
title: Recordset2.Seek-Methode (DAO)
TOCTitle: Seek Method
ms:assetid: 9871619b-a303-c97d-54c0-defc8d9b87f5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197940(v=office.15)
ms:contentKeyID: 48546489
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: f9789699e39bcb7b7532beb69aaf52c8f0d6e889
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59552654"
---
# <a name="recordset2seek-method-dao"></a>Recordset2.Seek-Methode (DAO)

**Gilt für**: Access 2013, Office 2013

Sucht den Datensatz in einem indizierten **Recordset**-Objekt vom Typ Tabelle, das den angegebenen Kriterien für den aktuellen Index entspricht, und macht diesen Datensatz zum aktuellen Datensatz (gilt nur für Microsoft Access-Arbeitsbereiche).

## <a name="syntax"></a>Syntax

*Ausdruck* . Seek(***Comparison** _, _*_Key1_*_, _*_Key2_*_, _*_Key3_*_, _*_Key4_*_, _*_Key5_*_, _*_Key6_*_, _*_Key7_*_, _*_Key8_*_, _*_Key9_*_, _*_Key10_*_, _*_Key11_*_, _*_Key12_*_, _*_Key13_**)

*Ausdruck* Eine Variable, die ein **Recordset2-Objekt** darstellt.

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
<td><p><em>Vergleich</em></p></td>
<td><p>Erforderlich</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Einer der folgenden Zeichenfolgenausdrücke: &lt;, &lt;=, =, &gt;= oder &gt;.</p></td>
</tr>
<tr class="even">
<td><p><em>Key1, Key2...Key13</em></p></td>
<td><p>Erforderlich</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Mindestens ein Wert, der den Feldern im aktuellen Index des <strong>Recordset</strong> -Objekts gemäß der Angabe seiner Einstellungen für die Eigenschaft <strong>Index</strong> entspricht. Sie können bis zu 13 key-Argumente verwenden.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Bemerkungen

Bevor Sie **Seek** verwenden können, müssen Sie den aktuellen Index mit der **Index**-Eigenschaft festlegen. Wenn der Index ein nicht eindeutiges Schlüsselfeld identifiziert, sucht **Seek** nach dem ersten Datensatz, der die Kriterien erfüllt.

Mit der **Seek**-Methode werden die angegebenen Schlüsselfelder nach dem ersten Datensatz durchsucht, der den durch die Argumente comparison und key1 angegebenen Kriterien entspricht. Wenn er gefunden wurde, wird er zum aktuellen Datensatz gemacht, und die **NoMatch**-Eigenschaft wird auf **False** festgelegt. Falls mit der **Seek**-Methode kein Suchergebnis erzielt wird, wird die **NoMatch**-Eigenschaft auf **True** festgelegt, und der aktuelle Datensatz ist nicht definiert.

Wenn für comparison gleich (=), größer gleich (\>=) oder größer als (\>) angegeben wird, beginnt **Seek** am Anfang des Indexes mit der Vorwärtssuche.

Wenn für comparison kleiner als (\<), kleiner als oder gleich (\<=) angegeben wird, beginnt **Seek** am Ende des Indexes mit der Rückwärtssuche. However, if there are duplicate index entries at the end of the index, **Seek** starts at an arbitrary entry among the duplicates and then searches backward.

You must specify values for all fields defined in the index. If you use **Seek** with a multiple-column index, and you don't specify a comparison value for every field in the index, then you cannot use the equal (=) operator in the comparison. Dies liegt daran, dass einige der Kriterienfelder (key2, key3 usw.) standardmäßig auf Null festgelegt werden, was möglicherweise nicht zutrifft. Daher funktioniert der Operator Gleich nur dann ordnungsgemäß, wenn Sie einen Datensatz besitzen, der ausgenommen von dem key, den Sie suchen, **null** aufweist. Wir empfehlen, stattdessen den Operator Größer als oder Gleich (\>=) zu verwenden.

Das key1-Argument muss den gleichen Felddatentyp besitzen wie das entsprechende Feld im aktuellen Index. Wenn der aktuelle Index beispielsweise auf ein Zahlenfeld (z. B. Mitarbeiter-ID) verweist, muss key1 numerisch sein. Wenn der aktuelle Index auf ein Textfeld (z. B. den Nachnamen) verweist, muss key1 eine Zeichenfolge sein.

Zum Verwenden von **Seek** muss kein aktueller Datensatz vorhanden sein.

Zum Auflisten der vorhandenen Indizes können Sie die **[Indexes](indexes-collection-dao.md)**-Auflistung verwenden.

Mithilfe der **[Find](recordset2-findfirst-method-dao.md)**-Methoden können Sie in einem **Recordset**-Objekt vom Typ "Dynaset" oder "Snapshot" nach einem Datensatz suchen, der einer bestimmten Bedingung entspricht, die nicht in vorhandenen Indizes vorhanden ist. Sollen alle Datensätze gefunden werden, nicht nur diejenigen, die eine bestimmte Bedingung erfüllen, bewegen Sie sich mithilfe der **[Move](recordset-movefirst-method-dao.md)**-Methoden von Datensatz zu Datensatz.

Sie können die **Seek**-Methode nicht auf eine verknüpfte Tabelle anwenden, da verknüpfte Tabellen als **Recordset**-Objekte vom Typ Tabelle nicht geöffnet werden können. Wenn Sie jedoch die **[OpenDatabase](dbengine-opendatabase-method-dao.md)**-Methode verwenden, um eine installierbare ISAM (nicht ODBC)-Datenbank direkt zu öffnen, können Sie **Seek** auf Tabellen in dieser Datenbank anwenden.

## <a name="example"></a>Beispiel

Dieses Beispiel veranschaulicht die **Seek**-Methode, indem dem Benutzer erlaubt wird, nach einem Produkt anhand einer ID-Nummer zu suchen.

```vb
    Sub SeekX() 
     
     Dim dbsNorthwind As Database 
     Dim rstProducts As Recordset2 
     Dim intFirst As Integer 
     Dim intLast As Integer 
     Dim strMessage As String 
     Dim strSeek As String 
     Dim varBookmark As Variant 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     ' You must open a table-type Recordset to use an index, 
     ' and hence the Seek method. 
     Set rstProducts = _ 
     dbsNorthwind.OpenRecordset("Products", dbOpenTable) 
     
     With rstProducts 
     ' Set the index. 
     .Index = "PrimaryKey" 
     
     ' Get the lowest and highest product IDs. 
     .MoveLast 
     intLast = !ProductID 
     .MoveFirst 
     intFirst = !ProductID 
     
     Do While True 
     ' Display current record information and ask user 
     ' for ID number. 
     strMessage = "Product ID: " & !ProductID & vbCr & _ 
     "Name: " & !ProductName & vbCr & vbCr & _ 
     "Enter a product ID between " & intFirst & _ 
     " and " & intLast & "." 
     strSeek = InputBox(strMessage) 
     
     If strSeek = "" Then Exit Do 
     
     ' Store current bookmark in case the Seek fails. 
     varBookmark = .Bookmark 
     
     .Seek "=", Val(strSeek) 
     
     ' Return to the current record if the Seek fails. 
     If .NoMatch Then 
     MsgBox "ID not found!" 
     .Bookmark = varBookmark 
     End If 
     Loop 
     
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
```

<br/>

This example uses the **NoMatch** property to determine whether a **Seek** and a **FindFirst** were successful, and if not, to give appropriate feedback. The SeekMatch and FindMatch procedures are required for this procedure to run.

```vb
    Sub NoMatchX() 
     
     Dim dbsNorthwind As Database 
     Dim rstProducts As Recordset2 
     Dim rstCustomers As Recordset2 
     Dim strMessage As String 
     Dim strSeek As String 
     Dim strCountry As String 
     Dim varBookmark As Variant 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     ' Default is dbOpenTable; required if Index property will 
     ' be used. 
     Set rstProducts = dbsNorthwind.OpenRecordset("Products") 
     
     With rstProducts 
     .Index = "PrimaryKey" 
     
     Do While True 
     ' Show current record information; ask user for 
     ' input. 
     strMessage = "NoMatch with Seek method" & vbCr & _ 
     "Product ID: " & !ProductID & vbCr & _ 
     "Product Name: " & !ProductName & vbCr & _ 
     "NoMatch = " & .NoMatch & vbCr & vbCr & _ 
     "Enter a product ID." 
     strSeek = InputBox(strMessage) 
     If strSeek = "" Then Exit Do 
     
     ' Call procedure that seeks for a record based on 
     ' the ID number supplied by the user. 
     SeekMatch rstProducts, Val(strSeek) 
     Loop 
     
     .Close 
     End With 
     
     Set rstCustomers = dbsNorthwind.OpenRecordset( _ 
     "SELECT CompanyName, Country FROM Customers " & _ 
     "ORDER BY CompanyName", dbOpenSnapshot) 
     
     With rstCustomers 
     
     Do While True 
     ' Show current record information; ask user for 
     ' input. 
     strMessage = "NoMatch with FindFirst method" & _ 
     vbCr & "Customer Name: " & !CompanyName & _ 
     vbCr & "Country: " & !Country & vbCr & _ 
     "NoMatch = " & .NoMatch & vbCr & vbCr & _ 
     "Enter country on which to search." 
     strCountry = Trim(InputBox(strMessage)) 
     If strCountry = "" Then Exit Do 
     
     ' Call procedure that finds a record based on 
     ' the country name supplied by the user. 
     FindMatch rstCustomers, _ 
     "Country = '" & strCountry & "'" 
     Loop 
     
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Sub SeekMatch(rstTemp As Recordset, _ 
     intSeek As Integer) 
     
     Dim varBookmark As Variant 
     Dim strMessage As String 
     
     With rstTemp 
     ' Store current record location. 
     varBookmark = .Bookmark 
     .Seek "=", intSeek 
     
     ' If Seek method fails, notify user and return to the 
     ' last current record. 
     If .NoMatch Then 
     strMessage = _ 
     "Not found! Returning to current record." & _ 
     vbCr & vbCr & "NoMatch = " & .NoMatch 
     MsgBox strMessage 
     .Bookmark = varBookmark 
     End If 
     
     End With 
     
    End Sub 
     
    Sub FindMatch(rstTemp As Recordset, _ 
     strFind As String) 
     
     Dim varBookmark As Variant 
     Dim strMessage As String 
     
     With rstTemp 
     ' Store current record location. 
     varBookmark = .Bookmark 
     .FindFirst strFind 
     
     ' If Find method fails, notify user and return to the 
     ' last current record. 
     If .NoMatch Then 
     strMessage = _ 
     "Not found! Returning to current record." & _ 
     vbCr & vbCr & "NoMatch = " & .NoMatch 
     MsgBox strMessage 
     .Bookmark = varBookmark 
     End If 
     
     End With 
     
    End Sub
```
