---
title: Recordset2.Seek-Methode (DAO)
TOCTitle: Seek Method
ms:assetid: 9871619b-a303-c97d-54c0-defc8d9b87f5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197940(v=office.15)
ms:contentKeyID: 48546489
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6db35b060d59891bfc33bb75c6e6bb370fb3dc9a
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998229"
---
# <a name="recordset2seek-method-dao"></a>Recordset2.Seek-Methode (DAO)

**Betrifft**: Access 2013, Office 2013

Sucht den Datensatz in einem indizierten **Recordset** -Objekt vom Typ Tabelle, das den angegebenen Kriterien für den aktuellen Index entspricht, und macht diesen Datensatz zum aktuellen Datensatz (gilt nur für Microsoft Access-Arbeitsbereiche).

## <a name="syntax"></a>Syntax

*Ausdruck* . Seek (***Vergleich***, ***Key1***, ***Key2***, ***Key3***, ***Schlüssel4***, ***Schlüssel bezieht. 5***, ***Key6***, ***Key7***, ***Key8***, ***"Key9" entsprechen***, ***Key10***, ***Key11***, ***Key12***, ***Key13***)

*Ausdruck* Eine Variable, die ein **Recordset2** -Objekt darstellt.

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
<th><p>Erforderlich oder optional</p></th>
<th><p>Datentyp</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Comparison</em></p></td>
<td><p>Erforderlich</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Einer der folgenden Zeichenfolgenausdrücke: &lt;, &lt;=, =, &gt;= oder &gt;.</p></td>
</tr>
<tr class="even">
<td><p><em>Key1, Key2...Key13</em></p></td>
<td><p>Erforderlich</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Mindestens ein Wert, der den Feldern im aktuellen Index des <strong>Recordset</strong> -Objekts gemäß der Angabe seiner Einstellungen für die Eigenschaft <strong>Index</strong> entspricht. Sie können bis zu 13 wichtige Argumente verwenden.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Hinweise

Bevor Sie **Seek** verwenden können, müssen Sie den aktuellen Index mit der **Index**-Eigenschaft festlegen. Wenn der Index ein nicht eindeutiges Schlüsselfeld identifiziert, sucht **Seek** nach dem ersten Datensatz, der die Kriterien erfüllt.

Die **Seek** -Methode werden die angegebenen Schlüsselfelder durchsucht und sucht den ersten Datensatz, der Key1 und Demgegenüber angegebenen Kriterien erfüllt. Wenn er gefunden wurde, wird er zum aktuellen Datensatz gemacht, und die **NoMatch**-Eigenschaft wird auf **False** festgelegt. Falls mit der **Seek**-Methode kein Suchergebnis erzielt wird, wird die **NoMatch**-Eigenschaft auf **True** festgelegt, und der aktuelle Datensatz ist nicht definiert.

Wenn Vergleich ist gleich (=), größer als oder gleich (\>=), größer oder gleich (\>), **Seek** beginnt am Anfang des Index und sucht vorwärts.

Wenn Vergleich ist kleiner als (\<) oder kleiner oder gleich (\<=), **Seek** beginnt am Ende des Index und sucht rückwärts. Wenn doppelte Einträge am Ende des Index vorhanden sind, **Seek** bei einem beliebigen Eintrag in der Duplikaten startet und sucht rückwärts.

Sie müssen für alle im Index definierten Felder Werte angeben. Wenn Sie **Seek** mit einem mehrspaltigen Index verwenden und Sie keinen Vergleichswert für jedes Feld im Index angeben, können Sie im Vergleich nicht den Operator "gleich" (=) verwenden. Dies liegt daran einige Kriterienfelder (key2, key3 usw.) auf NULL-Wert festgelegt wird, die wahrscheinlich nicht übereinstimmt, wird. Aus diesem Grund funktioniert der Operator "gleich" nur dann ordnungsgemäß, wenn Sie einen Datensatz verwenden, der außer bei dem Schlüssel, den Sie suchen, durchgängig **Null** ist. Es wird empfohlen, die Sie verwenden, die größer als oder gleich (\>=) Operator stattdessen.

Das Argument key1 muss dieselbe Feld Datentyp aufweisen wie das entsprechende Feld im aktuellen Index. Beispielsweise muss der aktuelle Index auf ein Zahlenfeld (wie Mitarbeiter-ID) verweist, numerisch key1 sein. Entsprechend muss der aktuelle Index auf ein Textfeld (beispielsweise Nachname) verweist, key1 eine Zeichenfolge sein.

Beim Verwenden von **Seek** muss kein aktueller Datensatz vorhanden sein.

Zum Auflisten der vorhandenen Indizes können Sie die **[Indexes](indexes-collection-dao.md)** -Auflistung verwenden.

Mithilfe der [**Find**](recordset2-findfirst-method-dao.md) -Methoden können Sie in einem **Recordset** -Objekt vom Typ "Dynaset" oder "Snapshot" nach einem Datensatz suchen, der einer bestimmten Bedingung entspricht, die nicht in vorhandenen Indizes vorhanden ist. Sollen alle Datensätze gefunden werden, nicht nur diejenigen, die eine bestimmte Bedingung erfüllen, bewegen Sie sich mithilfe der **[Move](recordset-movefirst-method-dao.md)** -Methoden von Datensatz zu Datensatz.

Sie können die **Seek** -Methode nicht auf eine verknüpfte Tabelle anwenden, da verknüpfte Tabellen als **Recordset** -Objekte vom Typ Tabelle nicht geöffnet werden können. Wenn Sie jedoch die **[OpenDatabase](dbengine-opendatabase-method-dao.md)** -Methode verwenden, um eine installierbare ISAM (nicht ODBC)-Datenbank direkt zu öffnen, können Sie **Seek** auf Tabellen in dieser Datenbank anwenden.

## <a name="example"></a>Beispiel

In diesem Beispiel wird die **Seek**-Methode veranschaulicht. Der Benutzer kann auf Basis einer ID-Nummer nach einem Produkt suchen.

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

In diesem Beispiel wird die **NoMatch** -Eigenschaft verwendet, um zu bestimmen, ob **Seek** und **FindFirst** erfolgreich waren, und falls nicht, entsprechendes Feedback zu geben. Die Prozeduren SeekMatch und FindMatch sind erforderlich, damit dieses Verfahren ausgeführt wird.

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
