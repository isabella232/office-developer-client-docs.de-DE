---
title: Recordset.CancelUpdate-Methode (DAO)
TOCTitle: CancelUpdate method
ms:assetid: efc4f60b-876f-5e11-37fd-0fbbf225b15b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836421(v=office.15)
ms:contentKeyID: 48548590
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053072
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 6cb9823cec79a31f8ae26b2518d4368f6eefe2ce
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2018
ms.locfileid: "25999078"
---
# <a name="recordsetcancelupdate-method-dao"></a>Recordset.CancelUpdate-Methode (DAO)

**Betrifft**: Access 2013, Office 2013

Alle ausstehenden Aktualisierungen für ein **[Recordset](recordset-object-dao.md)** -Objekt werden abgebrochen.

## <a name="syntax"></a>Syntax

*Ausdruck* . CancelUpdate (***UpdateType***)

*Ausdruck* Eine Variable, die ein **Recordset** -Objekt darstellt.

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
<td><p><em>UpdateType</em></p></td>
<td><p>Optional</p></td>
<td><p><strong>Long</strong></p></td>
<td><p>Legen Sie auf einen der Werte <strong><a href="updatetypeenum-enumeration-dao.md">UpdateTypeEnum</a></strong> .</p><p><strong>Hinweis</strong>: die Werte <EM>DbUpdateRegular</EM> und <EM>DbUpdateBatch</EM> sind nur gültig, wenn Batchaktualisierungen aktiviert ist.</p>
</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Bemerkungen

Mit der **CancelUpdate**-Methode können Sie alle ausstehenden Aktualisierungen abbrechen, die aus einer **[Edit](recordset-edit-method-dao.md)** - oder **[AddNew](recordset-addnew-method-dao.md)** -Operation stammen. Wenn ein Benutzer z. B. die **Edit**- oder **AddNew**-Methode aufruft, ohne vorher die **Update**-Methode aufgerufen zu haben, werden durch die **CancelUpdate**-Methode alle Änderungen abgebrochen, die nach dem Aufrufen von **Edit** oder **AddNew** vorgenommen wurden.

Überprüfen Sie die **[EditMode](recordset-editmode-property-dao.md)** -Eigenschaft des **Recordset**-Objekts, um zu ermitteln, ob eine Operation aussteht, die abgebrochen werden kann.

> [!NOTE]
> [!HINWEIS] Die Verwendung der **CancelUpdate**-Methode hat dieselbe Wirkung wie das Verschieben zu einem anderen Datensatz, ohne die **[Update](recordset-update-method-dao.md)** -Methode zu verwenden. Der einzige Unterschied besteht darin, dass der aktuelle Datensatz nicht geändert wird und dass verschiedene Eigenschaften nicht aktualisiert werden, z. B. **[BOF](recordset-bof-property-dao.md)** und **[EOF](recordset-eof-property-dao.md)**.


## <a name="example"></a>Beispiel

Dieses Beispiel zeigt, wie die Methoden **CancelUpdate** und **AddNew** kombiniert werden.

```vb
    Sub CancelUpdateX() 
     
       Dim dbsNorthwind As Database 
       Dim rstEmployees As Recordset 
       Dim intCommand As Integer 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       Set rstEmployees = dbsNorthwind.OpenRecordset( _ 
          "Employees", dbOpenDynaset) 
     
       With rstEmployees 
          .AddNew 
          !FirstName = "Kimberly" 
          !LastName = "Bowen" 
          intCommand = MsgBox("Add new record for " & _ 
             !FirstName & " " & !LastName & "?", vbYesNo) 
          If intCommand = vbYes Then 
             .Update 
             MsgBox "Record added." 
             ' Delete new record because this is a  
             ' demonstration. 
             .Bookmark = .LastModified 
             .Delete 
          Else 
             .CancelUpdate 
             MsgBox "Record not added." 
          End If 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub 
```

<br/>

Dieses Beispiel zeigt, wie die Methoden **CancelUpdate** und **Edit** kombiniert werden.

```vb
Sub CancelUpdateX2() 
 
   Dim dbsNorthwind As Database 
   Dim rstEmployees As Recordset 
   Dim strFirst As String 
   Dim strLast As String 
   Dim intCommand As Integer 
 
   Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
   Set rstEmployees = dbsNorthwind.OpenRecordset( _ 
      "Employees", dbOpenDynaset) 
 
   With rstEmployees 
      strFirst = !FirstName 
      strLast = !LastName 
      .Edit 
      !FirstName = "Cora" 
      !LastName = "Edmonds" 
      intCommand = MsgBox("Replace current name with " & _ 
         !FirstName & " " & !LastName & "?", vbYesNo) 
      If intCommand = vbYes Then 
         .Update 
         MsgBox "Record modified." 
         ' Restore data because this is a demonstration. 
         .Bookmark = .LastModified 
         .Edit 
         !FirstName = strFirst 
         !LastName = strLast 
         .Update 
      Else 
         .CancelUpdate 
         MsgBox "Record not modified." 
      End If 
      .Close 
   End With 
 
   dbsNorthwind.Close 
 
End Sub 
 
```

