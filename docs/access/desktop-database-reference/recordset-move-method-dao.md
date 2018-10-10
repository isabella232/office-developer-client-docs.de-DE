---
title: Recordset.Move-Methode (DAO)
TOCTitle: Move Method
ms:assetid: 21ca5ab5-ff71-1ae8-21b3-8991d5f795cf
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191697(v=office.15)
ms:contentKeyID: 48543689
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052941
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 23de94392fb2d9f1b0106c39f21a8872783b6d7b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475061"
---
# <a name="recordsetmove-method-dao"></a>Recordset.Move-Methode (DAO)


**Betrifft**: Access 2013 | Office 2013

Verschiebt die Position des aktuellen Datensatzes in ein **[Recordset](recordset-object-dao.md)** -Objekt.

## <a name="syntax"></a>Syntax

*Ausdruck* . Move (***Zeilen***, ***Anfangslesezeichen***)

*Ausdruck* Eine Variable, die ein **Recordset** -Objekt darstellt.

### <a name="parameters"></a>Parameter

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
<th><p>Erforderlich/Optional</p></th>
<th><p>Datentyp</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Zeilen</p></td>
<td><p>Erforderlich</p></td>
<td><p><strong>Long</strong></p></td>
<td><p>Die Anzahl von Zeilen, um die sich die Position verschiebt. Ist rows größer als 0, wird die Position nach vorne verschoben (Richtung Dateiende). Ist rows kleiner als 0, wird die Position nach hinten verschoben (Richtung Dateianfang).</p></td>
</tr>
<tr class="even">
<td><p>Anfangslesezeichen</p></td>
<td><p>Optional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Ein Wert, der ein Lesezeichen identifiziert. Bei Angabe von startbookmark beginnt die Verschiebung relativ zu diesem Lesezeichen. Andernfalls beginnt Move mit dem aktuellen Datensatz.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Bemerkungen

Wenn Sie mithilfe von **Move** den aktuellen Datensatzzeiger vor dem ersten Datensatz positionieren, wird der aktuelle Datensatzzeiger an den Dateianfang verschoben. Falls das **Recordset** keine Datensätze enthält und seine **[BOF](recordset-bof-property-dao.md)** -Eigenschaft auf **True** festgelegt ist, wird ein Fehler zurückgegeben, wenn Sie sich mit dieser Methode rückwärts bewegen.

Wenn Sie mithilfe von **Move** den aktuellen Datensatzzeiger hinter dem letzten Datensatz positionieren, wird der aktuelle Datensatzzeiger an das Dateiende verschoben. Falls das **Recordset** keine Datensätze enthält und seine **[EOF](recordset-eof-property-dao.md)** -Eigenschaft auf **True** festgelegt ist, wird ein Fehler zurückgegeben, wenn Sie sich mit dieser Methode vorwärts bewegen.

Wenn für die **BOF**- oder die **EOF**-Eigenschaft der Wert **True** festgelegt ist und Sie versuchen, die **Move**-Methode ohne ein zulässiges Lesezeichen zu verwenden, tritt ein Laufzeitfehler auf.


> [!NOTE]
> <UL>
> <LI>
> <P>Wenn Sie <STRONG>Move</STRONG> auf ein <STRONG>Recordset</STRONG>-Objekt vom Typ Vorwärts anwenden, muss das Zeilenargument eine positive Ganzzahl sein, und Lesezeichen sind nicht zulässig. Sie können sich also nur vorwärts bewegen.</P>
> <LI>
> <P>Verwenden Sie eine der Methoden <STRONG>MoveFirst</STRONG>, <STRONG>MoveLast</STRONG>, <STRONG>MoveNext</STRONG> oder <STRONG>MovePrevious</STRONG>, um den ersten, letzten, nächsten oder vorherigen Datensatz in einem <STRONG>Recordset</STRONG> zum aktuellen Datensatz zu machen.</P>
> <LI>
> <P>Das Verwenden von <STRONG>Move</STRONG> mit einer Zeilenanzahl gleich 0 ist eine einfache Möglichkeit, die zugrunde liegenden Daten für den aktuellen Datensatz abzurufen. Das ist hilfreich, wenn Sie sicherstellen möchten, dass der aktuelle Datensatz die aktuellsten Daten aus den Basistabellen enthält. Außerdem werden alle anstehenden <STRONG><A href="recordset2-edit-method-dao.md">Edit</A></STRONG> - oder <STRONG><A href="recordset-addnew-method-dao.md">AddNew</A></STRONG> -Aufrufe abgebrochen.</P></LI></UL>



## <a name="example"></a>Beispiel

In diesem Beispiel wird die **Move**-Methode verwendet, um den Zeiger für den Datensatz auf der Grundlage der Benutzereingabe zu positionieren.

```vb
    Sub MoveX() 
     
       Dim dbsNorthwind As Database 
       Dim rstSuppliers As Recordset 
       Dim varBookmark As Variant 
       Dim strCommand As String 
       Dim lngMove As Long 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       Set rstSuppliers = _ 
          dbsNorthwind.OpenRecordset("SELECT CompanyName, " & _ 
          "City, Country FROM Suppliers ORDER BY CompanyName", _ 
          dbOpenDynaset) 
     
       With rstSuppliers 
          ' Populate recordset. 
          .MoveLast 
          .MoveFirst 
     
          Do While True 
             ' Display information about current record and ask  
             ' how many records to move. 
             strCommand = InputBox( _ 
                "Record " & (.AbsolutePosition + 1) & " of " & _ 
                .RecordCount & vbCr & "Company: " & _ 
                !CompanyName & vbCr & "Location: " & !City & _ 
                ", " & !Country & vbCr & vbCr & _ 
                "Enter number of records to Move " & _ 
                "(positive or negative).") 
     
             If strCommand = "" Then Exit Do 
     
             ' Store bookmark in case the Move doesn't work. 
             varBookmark = .Bookmark 
     
             ' Move method requires parameter of data type Long. 
             lngMove = CLng(strCommand) 
             .Move lngMove 
     
             ' Trap for BOF or EOF. 
             If .BOF Then 
                MsgBox "Too far backward! " & _ 
                   "Returning to current record." 
                .Bookmark = varBookmark 
             End If 
             If .EOF Then 
                MsgBox "Too far forward! " & _ 
                   "Returning to current record." 
                .Bookmark = varBookmark 
             End If 
          Loop 
          .Close 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub
```
